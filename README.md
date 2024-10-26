# **TUGAS PBO TM 10 (REPORT)**
___
## **Daftar Isi**
- [DbUtils](https://github.com/anisatanti/PBO_PertemuanKesepuluh/blob/main/DbUtils.java)
- [FrameMatkul.form](https://github.com/anisatanti/PBO_PertemuanKesepuluh/blob/main/FrameMataKuliah.form)
- [FrameMatkul.Java](https://github.com/anisatanti/PBO_PertemuanKesepuluh/blob/main/FrameMataKuliah.java)
- [Reportmatakuliah.jasper](https://github.com/anisatanti/PBO_PertemuanKesepuluh/blob/main/reportmatakuliah.jasper)
- [Reportmatakuliha.jrxml](https://github.com/anisatanti/PBO_PertemuanKesepuluh/blob/main/reportmatakuliah.jrxml)
___
## **_Deskripsi_**
Proyek ini merupakan Tugas Pertemuan Kesepuluh Mata Kuliah Pemrograman Berorientasi Objek. Membuat Aplikasi CRUD pada Netbeans Java yang terhubung dengan Aplikasi basis data PostgreSQL yang ditambah dengan button Cetak. Membuat report untuk mencetak data yang telah diinput pada database dan data yang ditampilkan pada tampilan GUI. Dalam proyek ini saya akan menjelaskan cara Instalasi Jasper Report Plugin Pada Netbeans Java beserta Penerapan Report Cetak Pada Tampilan GUI Netbeans Java.
___
## **Cara Instalasi Jasper Report Plugin Pada Netbeans Java**
1.	Download Jasperreport beserta LibraryJasperReport
   ![image](https://github.com/user-attachments/assets/2917b253-2a22-44ad-992e-90a7b3923c7f)
2.	Menambahkan Plugin Jasperreport pada Netbeans dengan cara klik Tools kemudian pilih Plugins.
   ![image](https://github.com/user-attachments/assets/433f7895-0000-4fc4-9ad0-dfdd3c22f00c)
3.	Pilih bagian “Downloaded” kemudian klik “Add Plugins”. Cari Lokasi File iReport, kemudian tekan Ctrl + A setelah semua file terpilih klik Open
   
    ![image](https://github.com/user-attachments/assets/e6db947a-f09a-4751-945e-a2d956c87042)
4.	Klik Install untuk menambahkan plugin jasperreport pada Netbeans.
   ![image](https://github.com/user-attachments/assets/50a2419b-0b92-4a0c-af01-03158decd518)
5.	Netbeans meminta menambahkan plugin org.jdesktop.layout versi 1.4.1 untuk proses instalasi jasperreport.
   ![image](https://github.com/user-attachments/assets/e0b32914-191d-40d1-a6b9-f965f3abfaa2)
6.	Download plugin org-jdesktop-layout-RELEASE65.nbm
   ![image](https://github.com/user-attachments/assets/07501224-43e4-4062-a6f6-a837e9377d74)
7.	Setelah terdownload kemudian Kembali ke Netbeans, klik Add Plugins, pilih plugin org-jdesktop-layout-RELEASE65.nbm kemudian klik Open.
   ![image](https://github.com/user-attachments/assets/86e5b197-8a34-40ff-bf4f-a6a9e2c9ab82)
8.	Setelah berhasil ditambahkan, klik Install.
   ![image](https://github.com/user-attachments/assets/e0fefaee-8496-4b15-a7e0-bc33c8783958)
9.	Klik Next pada pop up Netbeans IDE Installer.
    ![image](https://github.com/user-attachments/assets/cd4fde19-658c-49a5-b8d2-1f0db7c99fd6)
10.	Checklist “I accept the terms in all of the license agreements” kemudian klik Install.
    ![image](https://github.com/user-attachments/assets/740bcf64-6361-4ee0-a5ca-3a70650d488b)
11.	Klik continue pada pop up Validation Warning.
    ![image](https://github.com/user-attachments/assets/be8c69ec-9701-4892-8327-a04e48ffc0c4)
12.	Pilih “Restart IDE Now” kemudian klik Finish, maka Netbeans akan di restart ulang.
    ![image](https://github.com/user-attachments/assets/80d0816a-853c-445b-aa13-ced9b55c767d)
13.	Plugin JasperReport berhasil diinstal ditandai dengan tampilan seperti berikut ini.
    ![image](https://github.com/user-attachments/assets/8c0cea94-c1b2-4059-a030-c523fce00708)
___
## **Penerapan Report Cetak Pada Tampilan GUI Netbeans Java**
1.	Membuat Database baru pada aplikasi PostgreSQL dengan cara klik kanan icon database, klik Create kemudian klik Database.
   ![image](https://github.com/user-attachments/assets/60b42f09-ae8b-4a77-8fcf-4b3599c8b82f)
2.	Membuat tabel MataKuliah beserta atributnya.

  	![image](https://github.com/user-attachments/assets/a5f0434f-ad59-4dd9-ae50-4cf5088a0d2f)
  	
3.	Membuat project baru pada Netbeans dengan cara klik New Project, pada categories pilih Java with Ant, pada Projects pilih Java Aplication kemudian klik Next.
   
   ![image](https://github.com/user-attachments/assets/95fba5f3-5c61-4c4a-b82a-a23c2f196260)
   
4.	Beri nama project baru dengan nama PBO_Report, unchecklist pada Create Main Class kemudian klik Finish.
   
   ![image](https://github.com/user-attachments/assets/f30ee17f-643f-4af1-b5b6-95312220e302)
   
5.	Membuat Kelas koneksi dengan cara klik kana pada package report, klik New, klik Java Class.
   
   ![image](https://github.com/user-attachments/assets/9ba5bf3f-0e51-47e7-95e3-37bd76aafe64)
   
6.	Beri nama “DbUtils” pada kelas koneksi kemudian klik Finish.
   
   ![image](https://github.com/user-attachments/assets/dde33ce6-c10e-4efb-a6fe-792514fffbad)
   
7.	Mengisi Kelas DbUtils. Kelas DbUtils dibuat untuk menyederhanakan pengolahan data dari ResultSet agar bisa langsung digunakan dalam komponen GUI, khususnya JTable. Fungsinya adalah mengonversi data hasil query SQL (yang ada dalam ResultSet) menjadi TableModel, yang kemudian dapat digunakan untuk menampilkan data di JTable dengan cepat dan efisien.
   
   ![image](https://github.com/user-attachments/assets/419dd42a-999e-4627-b377-34186e479825)
   
8.	Membuat Frame GUI Mata Kuliah dengan cara klik kanan pada package kemudian klik New, klik JFrame Form.
   
   ![image](https://github.com/user-attachments/assets/5a5ecb7a-2c67-4173-bb68-a039f9a0b84c)
   
9.	Beri nama “FrameMataKuliah” kemudian klik Finish.
    
   ![image](https://github.com/user-attachments/assets/d8c7bea1-715c-444b-b27b-4a3d4dfd3a31)
   
10. Menambahkan Library PostgreSQL dengan cara klik kanan pada Library project kemudian klik Add Library.
    
   ![image](https://github.com/user-attachments/assets/98e08197-889e-4de3-8e37-14e2a9c3c174)
   
11. Setelah muncul pop up, pilih PostgreSQl JDBC Driver kemudian klik Add Library.
    
    ![image](https://github.com/user-attachments/assets/4dd9d60c-0d20-4957-80df-0655da54e429)
    
12. Menambahkan Library Jasperreport dengan cara klik kanan pada Libraries, klik Add Jar/Folder
    
    ![image](https://github.com/user-attachments/assets/4891095f-4dba-4363-b472-795bed01838a)
    
13. Pilih folder tempat menyimpan file library jasperreport, tekan Ctrl + A untuk memilih semua file kemudian klik Open.
    
    ![image](https://github.com/user-attachments/assets/27b66395-028b-49e5-8392-4d3ce9d79e0f)
    
    File library jasperreport berhasil ditambahkan.
    
    ![image](https://github.com/user-attachments/assets/a8d89059-a07e-4f3f-bef7-483e3be375f0)
    
14. Membuat Tampilan GUI Data Mata Kuliah berisi Kode MK, SKS, Nama MK, dan Semester Ajar yang harus diisi menggunakan JTextField, kemudian terdapat 5 button yakni Insert, Update, Delete, Clear, Cetak, dan Exit menggunakan JButton, serta JTable untuk menampilkan data dalam bentuk tabel.
    
    ![image](https://github.com/user-attachments/assets/179b29c6-0a4f-47a3-aee7-f194656b65c1)
    
15. Berikut beberapa import yang digunakan pada program GUI Data Mata Kuliah.

    ```
         import java.sql.Connection;
         import java.sql.DriverManager;
         import java.sql.PreparedStatement;
         import java.sql.ResultSet;
         import java.io.InputStreamReader;
         import java.io.BufferedReader;
         import javax.swing.JOptionPane;
         import java.sql.SQLException;
         import java.util.HashMap;
         import javax.swing.table.TableColumnModel;
         import net.sf.jasperreports.engine.JasperFillManager;
         import net.sf.jasperreports.engine.JasperPrint;
         import net.sf.jasperreports.view.JasperViewer;    
```
    
16. Berikut code untuk koneksi program dengan database postgresql disertai method koneksi.
    
```
public class FrameMataKuliah extends javax.swing.JFrame {
    Connection conn;
    PreparedStatement pst;
    ResultSet rs;

    String driver = "org.postgresql.Driver";
    String koneksi = "jdbc:postgresql://localhost:5432/uts_pbo";
    String user = "postgres";
    String password = "1234";
    InputStreamReader inputStreamReader = new InputStreamReader(System.in);
    BufferedReader input = new BufferedReader(inputStreamReader);
    /**
     * Creates new form FrameMataKuliah
     */
    public FrameMataKuliah() {
        initComponents();
        koneksi();
        tampil();
    }

    public void koneksi() {
        try {
            Class.forName(driver);
            conn = DriverManager.getConnection(koneksi, user, password);
            System.out.println("Koneksi berhasil!");
        } catch (Exception e) {
            e.printStackTrace();
            System.out.println("Koneksi gagal!");
        }
    }
    
    ```
17. Membuat method tampil untuk menampilkan semua data pada JTable. Kemudian method clear untuk menghapus text pada JTextField.

    ```
      public void tampil() {
    try {
        String sql = "SELECT * FROM MataKuliah";
        pst = conn.prepareStatement(sql);
        rs = pst.executeQuery();

        tblMK.setModel(DbUtils.resultSetToTableModel(rs));

        TableColumnModel tcm = tblMK.getColumnModel();
        tcm.getColumn(0).setHeaderValue("Kode Mata Kuliah"); 
        tcm.getColumn(1).setHeaderValue("Nama Mata Kuliah"); 
        tcm.getColumn(2).setHeaderValue("SKS");              
        tcm.getColumn(3).setHeaderValue("Semester");         

        tblMK.getTableHeader().repaint();
    } catch (Exception e) {
        e.printStackTrace();
    }
}

    public void clear() {
        tfKode.setText("");
        tfSks.setText("");
        tfNamaMK.setText("");
        tfSmt.setText("");
    }

```
18.	Berikut code btnInsert untuk menginput data ke dalam database yang akan ditampilkan pada tampilan GUI Data Mata Kuliah

    ```
   	 private void btnInsertActionPerformed(java.awt.event.ActionEvent evt) {                                          
        try {
            StringBuilder errorMessage = new StringBuilder();
        tfKode.setEditable(true);
            
            if (tfKode.getText().isEmpty()) {
                errorMessage.append("Kode Mata Kuliah diisi dulu yaa!\n");
            }
            if (tfSks.getText().isEmpty()) {
                errorMessage.append("SKS tidak boleh kosong!\n");
            }
            if (tfNamaMK.getText().isEmpty()) {
                errorMessage.append("Nama Mata Kuliah diisi dulu yaa!\n");
            }
            if (tfSmt.getText().isEmpty()) {
                errorMessage.append("Semester Ajar diisi dulu yaa!\n");
            }

            if (errorMessage.length() > 0) {
                JOptionPane.showMessageDialog(null, errorMessage.toString(), "Input Error", JOptionPane.WARNING_MESSAGE);
                return; 
            }
       
            int sks, semesterAjar;
            try {
                sks = Integer.parseInt(tfSks.getText());
                semesterAjar = Integer.parseInt(tfSmt.getText());
            } catch (NumberFormatException e) {
                JOptionPane.showMessageDialog(null, "SKS dan Semester Ajar harus berupa angka!", "Input Error", JOptionPane.WARNING_MESSAGE);
                return; 
            }

            String sql = "INSERT INTO MataKuliah (KodeMK, SKS, NamaMK, SemesterAjar) VALUES (?, ?, ?, ?)";
            pst = conn.prepareStatement(sql);

            pst.setString(1, tfKode.getText());
            pst.setInt(2, sks); 
            pst.setString(3, tfNamaMK.getText());
            pst.setInt(4, semesterAjar); 
            
            int rowsInserted = pst.executeUpdate();


            if (rowsInserted > 0) {
                tampil();

                JOptionPane.showMessageDialog(null, "Data Mata Kuliah berhasil ditambahkan", "Sukses", JOptionPane.INFORMATION_MESSAGE);
            }

        } catch (SQLException e) {
            JOptionPane.showMessageDialog(null, "Terjadi kesalahan: " + e.getMessage(), "Error", JOptionPane.ERROR_MESSAGE);
            e.printStackTrace();
        }

    }
   	```
   	
19.	Berikut code btnUpdate untuk mengupdate data yang telah di inputkan

    ```
   	private void btnUpdateActionPerformed(java.awt.event.ActionEvent evt) {                                          
        if (conn == null) {
        JOptionPane.showMessageDialog(null, "Koneksi ke database tidak tersedia.");
        return;
    }

    tfKode.setEditable(false);

    try {
        StringBuilder errorMessage = new StringBuilder();

        if (tfKode.getText().isEmpty()) {
            errorMessage.append("Kode Mata Kuliah harus diisi!\n");
        }
        if (tfSks.getText().isEmpty()) {
            errorMessage.append("SKS harus diisi!\n");
        }
        if (tfNamaMK.getText().isEmpty()) {
            errorMessage.append("Nama Mata Kuliah harus diisi!\n");
        }
        if (tfSmt.getText().isEmpty()) {
            errorMessage.append("Semester Ajar harus diisi!\n");
        }

        if (errorMessage.length() > 0) {
            JOptionPane.showMessageDialog(null, errorMessage.toString(), "Input Error", JOptionPane.WARNING_MESSAGE);
            return;
        }

        String sql = "UPDATE MataKuliah SET SKS=?, NamaMK=?, SemesterAjar=? WHERE KodeMK=?";
        pst = conn.prepareStatement(sql);
        
        pst.setInt(1, Integer.parseInt(tfSks.getText()));
        pst.setString(2, tfNamaMK.getText());
        pst.setInt(3, Integer.parseInt(tfSmt.getText()));
        pst.setString(4, tfKode.getText());

        // Eksekusi update
        int updated = pst.executeUpdate();

        if (updated > 0) {
            tampil();
            JOptionPane.showMessageDialog(null, "Data berhasil di-update", "Sukses", JOptionPane.INFORMATION_MESSAGE);
        } else {
            JOptionPane.showMessageDialog(null, "Data gagal di-update. Periksa Kode Mata Kuliah.");
        }

    } catch (Exception e) {
        e.printStackTrace();
        JOptionPane.showMessageDialog(null, "Terjadi kesalahan: " + e.getMessage(), "Error", JOptionPane.ERROR_MESSAGE);
    }
    }
   	
   	```

20.	Berikut code btnDelete untuk menghapus data yang telah tersedia pada database.

    ```
   	private void btnDeleteActionPerformed(java.awt.event.ActionEvent evt) {                                          
        String id = tfKode.getText();

        if (id.isEmpty()) {
            
            JOptionPane.showMessageDialog(null, "Kode MK diisi dulu yaa!", "Input Error", JOptionPane.WARNING_MESSAGE);
            return;
        }
        int confirm = JOptionPane.showConfirmDialog(null, "Yakin ingin menghapus data dengan Kode MK: " + id + "?",
                "Konfirmasi Hapus", JOptionPane.YES_NO_OPTION);

        if (confirm == JOptionPane.YES_OPTION) {
            try {
                
                String query = "DELETE FROM MataKuliah WHERE KodeMK = ?";
                pst = conn.prepareStatement(query);
                pst.setString(1, id);

               
                int deleted = pst.executeUpdate();
               
                tampil();
                String message = (deleted > 0) ? "Data berhasil dihapus!" : "Kode MK tidak ditemukan!";
                JOptionPane.showMessageDialog(null, message);

            } catch (Exception e) {
                JOptionPane.showMessageDialog(null, "Terjadi kesalahan: " + e.getMessage(), "Error",
                        JOptionPane.ERROR_MESSAGE);
                e.printStackTrace();
            }
        }
    }
   	                                     
```

21.	Berikut code btnClear, tblMK agar saat klik data pada tabel, data dapat tertampilkan pada JTextField, serta code btnExit untuk menutup tampilan GUI.

    ```
   	   private void btnClearActionPerformed(java.awt.event.ActionEvent evt) {                                         
    clear();
    }                                        

    private void tblMKMouseClicked(java.awt.event.MouseEvent evt) {                                   
        int row = tblMK.getSelectedRow();

        
        String kode = tblMK.getValueAt(row, 0).toString();
        String sks = tblMK.getValueAt(row, 1).toString();
        String namaMK = tblMK.getValueAt(row, 2).toString();
        String smt = tblMK.getValueAt(row, 3).toString();

      
        tfKode.setText(kode);
        tfSks.setText(sks);
        tfNamaMK.setText(namaMK);
        tfSmt.setText(smt);
    
    }                                  

    private void btnExitActionPerformed(java.awt.event.ActionEvent evt) {                                        
     System.exit(0);
    }
   	
   	```

22.	Berikut code btnCetak untuk mencetak report yang akan dibuat.

    ```
   	
   	 private void btnCetakActionPerformed(java.awt.event.ActionEvent evt) {                                         
        try {
         String reportPath = "src/report/reportmatakuliah.jasper";
         HashMap<String, Object> parameters = new HashMap<>();
         JasperPrint print = JasperFillManager.fillReport( reportPath, parameters, conn);
         JasperViewer viewer = new JasperViewer(print, false);
         viewer.setVisible(true);
     }catch (Exception e){
         JOptionPane.showMessageDialog(null, e.getMessage());
     }
     
    }

   	```

23.	Membuat report untuk mencetak data Mata Kuliah dengan cara klik kanan pada package report kemudian klik New, klik Report Wizard.

    ![image](https://github.com/user-attachments/assets/55e42d7f-e1bf-411a-af7e-cf8c27ff6a49)

24.	Pilih layout untuk report yang akan dibuat kemudian klik Next.

    ![image](https://github.com/user-attachments/assets/0cd52e04-bd3d-4a62-a710-c8929a3a9a6d)

25. Beri nama “reportmatakuliah.jrxml” pada report yang akan dibuat kemudian klik next.

    ![image](https://github.com/user-attachments/assets/6ccac5ae-bf73-40f9-9dd8-9d655a2a36df)

26. Pada step Fields, klik New,  klik Database JDBC connection kemudian klik Next.

    ![image](https://github.com/user-attachments/assets/2f121e1d-71ce-4ae3-b240-5a98e3c3dc5c)

    ![image](https://github.com/user-attachments/assets/6ae83001-9e17-46d9-9a58-81aa8ac25125)


27. Beri nama koneksi database “matakuliah_db”, pada JDBC URL isikan nama database yang telah dibuat pada PostgreSQL. Masukkan username “postgres” dan password PostgreSQL. Checklist Save Password kemudian klik Test. Jika berhasil maka akan muncul pop up Connection Test Succsessful. Klik Ok kemudian klik Save untuk melanjutkan tahap berikutnya.

    ![image](https://github.com/user-attachments/assets/2c552491-e4e1-43e2-afbf-0ad3ce932e7e)

Masukkan Query “select * from MataKuliah” kemudian klik Next.

   ![image](https://github.com/user-attachments/assets/5aefa31a-524f-4eef-bf92-599aa14c1396)

28. Pindahkan semua kolom tabel database ke sebelah kanan dengan menekan Ctrl + A kemudian klik >> setelah itu klik Next.

    ![image](https://github.com/user-attachments/assets/740f6670-8863-43c4-9074-38fc0c72549b)

    ![image](https://github.com/user-attachments/assets/1f8293ed-23ef-4650-b69f-8f4b5c32bc3d)

29. Pada bagian Group by klik Next.

    ![image](https://github.com/user-attachments/assets/ca5c37b1-10ba-4b94-a016-0f95baf86ad3)

30. Klik Finish, report berhasil dibuat.

    ![image](https://github.com/user-attachments/assets/7d9db00e-8210-4fed-a489-83ad5bd48554)

31. Membuat Desain jasperreport.

    ![image](https://github.com/user-attachments/assets/6ff26302-0d93-4cbb-9f7f-e190763aa0f3)

32. Hasil Eksekusi btnCetak untuk menampilkan report yang telah dibuat.

    ![image](https://github.com/user-attachments/assets/a1e09f04-6572-41fb-84f9-07a9e70519a2)











    


   



    



 










   	








