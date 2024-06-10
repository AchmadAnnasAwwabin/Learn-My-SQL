<h2>01.Querry Demo :</h2> <br>

SELECT nama_user
FROM user
WHERE jenis_kelamin="P"
ORDER BY nama_user ASC
<p align="center">
  <img src="https://github.com/AchmadAnnasAwwabin/Learn-My-SQL/assets/160121014/15626a20-bb74-4b10-a165-24305ec55e09">
</p>

<h2>02.Querry Soal :</h2> <br>

SELECT nama_user, tanggal_lahir
FROM user
WHERE jenis_kelamin="L"
ORDER BY tanggal_lahir DESC;
<p align="center">
  <img src="https://github.com/AchmadAnnasAwwabin/Learn-My-SQL/assets/160121014/4cff2033-84bf-4466-9aee-1246f1475b03">
</p>

<h2>03.Course Join :</h2> <br>

SELECT
  kursus.judul,
  SUM(transaksi.total) AS total
FROM kursus
JOIN detail_transaksi ON detail_transaksi.id_kursus=kursus.id
JOIN transaksi ON detail_transaksi.id_transaksi=transaksi.id
WHERE transaksi.status = 'Completed'
GROUP BY kursus.judul
ORDER BY total DESC;
<p align="center">
  <img src="https://github.com/AchmadAnnasAwwabin/Learn-My-SQL/assets/160121014/dea125d2-5258-4232-b3e4-ce3118610079">
</p>

<h2>04.Hewan Join :</h2> <br>

SELECT
  user.nama,
  SUM(pelayanan.harga) AS total
FROM reservasi
JOIN user ON user.id = reservasi.id_user
JOIN pelayanan ON reservasi.id_pelayanan = pelayanan.id
WHERE reservasi.status = 'Completed'
GROUP BY user.nama
ORDER BY total DESC
LIMIT 1;
<p align="center">
  <img src="https://github.com/AchmadAnnasAwwabin/Learn-My-SQL/assets/160121014/6d7b8a78-e57f-421e-9215-7808ea51af35">
</p>

<h2>05.Hewan Reservasi :</h2> <br>

SELECT jenis_peliharaan, COUNT(jenis_peliharaan) AS total
FROM reservasi
GROUP BY jenis_peliharaan;
<p align="center">
  <img src="https://github.com/AchmadAnnasAwwabin/Learn-My-SQL/assets/160121014/0be9b0dc-356d-4acd-8115-110a32da9385">
</p>
