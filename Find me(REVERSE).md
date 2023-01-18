- Dùng tool Detect It Easy để xem file souce.exe sử dụng ngôn ngữ nào.</br>
- Vì sau khi chạy lệnh chương trình biến mất luôn và check thì thấy gài flag giả vào tất cả thư mục ổ C.</br>
- Kết quả file souce.exe được code bằng python.</br>
- File chạy mà không sử dụng python, nghĩa là đã được đóng gói.</br>
- Tìm trên Google một chút em có tool PyInstaller Extractor ở Github, sau đó đưa file souce.exe vào trong file pyinstxtractor để thực hiện việc giải nén.</br>
- Sử dụng câu lệnh: $ python pyinstxtractor.py souce.exe</br>
- Được file souce.exe_extracted, tìm thì thấy có file source.pyc thì việc còn lại chỉ là decompyle file souce.pyc về thành souce.py là có thể xem đc source code.</br>
- Em tìm được tool decompyle3 ở trên github và sử dụng nó với câu lệnh: decompyle3 souce.pyc và em đã xem được source.</br>
Em đã tìm thấy flag là: KCSC{T3t_n4y_4nh_kh0ng_th3m_d0t_ph4o_V1_ti3ng_cu0i_3m_r0n_r4_l0ng_4nh_r0i!}
