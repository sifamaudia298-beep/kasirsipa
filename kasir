<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Kasir Sifa</title>

<style>
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
    font-family: Arial, sans-serif;
}

body {
    background: #f5f5f5;
    color: #333;
    padding-bottom: 30px;
}

.header {
    background: linear-gradient(135deg, #ec4899, #8b5cf6);
    color: white;
    padding: 25px 15px;
    text-align: center;
}

.header h1 {
    font-size: 26px;
    margin-bottom: 6px;
}

.header p {
    font-size: 14px;
}

.container {
    max-width: 650px;
    margin: auto;
    padding: 15px;
}

.card {
    background: white;
    padding: 18px;
    border-radius: 15px;
    margin-bottom: 15px;
    box-shadow: 0 3px 12px rgba(0,0,0,0.08);
}

.card h2 {
    font-size: 18px;
    margin-bottom: 15px;
    color: #8b5cf6;
}

label {
    display: block;
    font-size: 14px;
    font-weight: bold;
    margin-bottom: 6px;
}

input {
    width: 100%;
    padding: 12px;
    border: 1px solid #ddd;
    border-radius: 9px;
    margin-bottom: 12px;
    font-size: 15px;
    outline: none;
}

input:focus {
    border-color: #8b5cf6;
}

.btn {
    width: 100%;
    border: none;
    padding: 13px;
    border-radius: 9px;
    color: white;
    font-size: 15px;
    font-weight: bold;
    cursor: pointer;
    margin-top: 7px;
}

.btn-tambah {
    background: #8b5cf6;
}

.btn-bayar {
    background: #16a34a;
}

.btn-reset {
    background: #ef4444;
}

.btn-cetak {
    background: #2563eb;
}

.btn-hapus {
    background: #ef4444;
    color: white;
    border: none;
    padding: 6px 9px;
    border-radius: 6px;
    cursor: pointer;
    font-size: 11px;
}

.btn-edit {
    background: #f59e0b;
    color: white;
    border: none;
    padding: 6px 9px;
    border-radius: 6px;
    cursor: pointer;
    font-size: 11px;
}

.table-wrapper {
    width: 100%;
    overflow-x: auto;
}

table {
    width: 100%;
    border-collapse: collapse;
    margin-top: 10px;
    min-width: 580px;
}

th {
    background: #f3e8ff;
    color: #6b21a8;
    padding: 10px 5px;
    font-size: 12px;
}

td {
    padding: 10px 5px;
    border-bottom: 1px solid #eee;
    font-size: 12px;
    text-align: center;
}

.total-box {
    margin-top: 15px;
}

.total-row {
    display: flex;
    justify-content: space-between;
    padding: 8px 0;
    font-size: 15px;
}

.total-row.total {
    border-top: 2px solid #ddd;
    margin-top: 5px;
    padding-top: 12px;
    font-size: 19px;
    font-weight: bold;
    color: #8b5cf6;
}

.kembalian {
    background: #dcfce7;
    color: #166534;
    padding: 14px;
    border-radius: 10px;
    margin-top: 12px;
    text-align: center;
    font-size: 18px;
    font-weight: bold;
}

.empty {
    text-align: center;
    padding: 25px;
    color: #999;
}

.info {
    background: #f3e8ff;
    color: #6b21a8;
    padding: 12px;
    border-radius: 10px;
    margin-bottom: 15px;
    font-size: 13px;
}

.struk {
    background: white;
    border: 1px dashed #aaa;
    padding: 15px;
    margin-top: 15px;
    display: none;
}

.struk h3 {
    text-align: center;
    margin-bottom: 5px;
}

.struk p {
    font-size: 12px;
    margin: 4px 0;
}

.struk table {
    min-width: 0;
    margin-top: 10px;
}

.struk th,
.struk td {
    font-size: 11px;
    padding: 6px 2px;
}

.footer {
    text-align: center;
    color: #777;
    font-size: 12px;
    margin-top: 20px;
}

@media print {

    body {
        background: white;
    }

    .no-print {
        display: none !important;
    }

    .card {
        box-shadow: none;
        border-radius: 0;
    }

    .header {
        background: white;
        color: black;
    }

    .struk {
        display: block !important;
        border: none;
    }

    .footer {
        display: none;
    }
}
</style>
</head>

<body>

<!-- HEADER -->
<div class="header">
    <h1>🛍️ KASIR SIFA</h1>
    <p>Aplikasi Kasir Sederhana</p>
</div>

<div class="container">

    <!-- INFORMASI -->
    <div class="info">
        📅 Tanggal:
        <strong id="tanggal"></strong>
    </div>

    <!-- TAMBAH BARANG -->
    <div class="card no-print">

        <h2>➕ Tambah Barang</h2>

        <label>Nama Barang</label>
        <input
            type="text"
            id="namaBarang"
            placeholder="Contoh: Buku Tulis">

        <label>Harga</label>
        <input
            type="number"
            id="hargaBarang"
            placeholder="Contoh: 5000"
            min="1">

        <label>Jumlah</label>
        <input
            type="number"
            id="jumlahBarang"
            placeholder="Contoh: 2"
            min="1"
            value="1">

        <button
            class="btn btn-tambah"
            onclick="tambahBarang()">
            ➕ Tambah ke Keranjang
        </button>

    </div>

    <!-- KERANJANG -->
    <div class="card">

        <h2>🛒 Keranjang</h2>

        <div id="keranjang">
            <div class="empty">
                Belum ada barang
            </div>
        </div>

    </div>

    <!-- PEMBAYARAN -->
    <div class="card">

        <h2>💰 Pembayaran</h2>

        <label>Diskon (%)</label>

        <input
            type="number"
            id="diskon"
            value="0"
            min="0"
            max="100"
            oninput="hitungTotal()">

        <div class="total-box">

            <div class="total-row">
                <span>Subtotal</span>
                <strong id="subtotal">Rp 0</strong>
            </div>

            <div class="total-row">
                <span>Diskon</span>
                <strong id="nilaiDiskon">Rp 0</strong>
            </div>

            <div class="total-row total">
                <span>Total</span>
                <strong id="total">Rp 0</strong>
            </div>

        </div>

        <br>

        <label>Uang Bayar</label>

        <input
            type="number"
            id="uangBayar"
            placeholder="Masukkan uang pelanggan"
            min="0"
            oninput="hitungKembalian()">

        <div
            class="kembalian"
            id="kembalian">

            Kembalian: Rp 0

        </div>

    </div>

    <!-- TOMBOL -->
    <div class="card no-print">

        <button
            class="btn btn-bayar"
            onclick="prosesBayar()">
            ✅ Proses Pembayaran
        </button>

        <button
            class="btn btn-cetak"
            onclick="cetakStruk()">
            🖨️ Cetak Struk
        </button>

        <button
            class="btn btn-reset"
            onclick="resetTransaksi()">
            🔄 Transaksi Baru
        </button>

    </div>

    <!-- STRUK -->
    <div class="card struk" id="struk">

        <h3>🛍️ KASIR SIFA</h3>
        <p style="text-align:center;">
            Struk Pembayaran
        </p>

        <hr style="margin:10px 0;">

        <p>
            Tanggal:
            <span id="strukTanggal"></span>
        </p>

        <div id="isiStruk"></div>

        <hr style="margin:10px 0;">

        <p>
            Subtotal:
            <strong id="strukSubtotal"></strong>
        </p>

        <p>
            Diskon:
            <strong id="strukDiskon"></strong>
        </p>

        <p>
            Total:
            <strong id="strukTotal"></strong>
        </p>

        <p>
            Bayar:
            <strong id="strukBayar"></strong>
        </p>

        <p>
            Kembalian:
            <strong id="strukKembalian"></strong>
        </p>

        <p style="text-align:center;margin-top:15px;">
            Terima kasih 🙏
        </p>

    </div>

    <!-- FOOTER -->
    <div class="footer">
        <p>© 2026 Kasir Sifa</p>
        <p>Aplikasi Kasir Sederhana</p>
    </div>

</div>

<script>

/* ==============================
   DATA KERANJANG
============================== */

let keranjang = [];


/* ==============================
   FORMAT RUPIAH
============================== */

function rupiah(angka) {

    return new Intl.NumberFormat(
        "id-ID",
        {
            style: "currency",
            currency: "IDR",
            minimumFractionDigits: 0
        }
    ).format(angka);

}


/* ==============================
   TANGGAL
============================== */

function tampilkanTanggal() {

    let sekarang = new Date();

    let tanggal = sekarang.toLocaleDateString(
        "id-ID",
        {
            day: "2-digit",
            month: "long",
            year: "numeric"
        }
    );

    document.getElementById("tanggal")
        .innerText = tanggal;

}

tampilkanTanggal();


/* ==============================
   TAMBAH BARANG
============================== */

function tambahBarang() {

    let nama =
        document.getElementById("namaBarang")
        .value
        .trim();

    let harga =
        parseInt(
            document.getElementById("hargaBarang")
            .value
        );

    let jumlah =
        parseInt(
            document.getElementById("jumlahBarang")
            .value
        );


    if (nama === "") {

        alert("Nama barang harus diisi!");

        return;
    }


    if (isNaN(harga) || harga <= 0) {

        alert("Harga barang harus lebih dari 0!");

        return;
    }


    if (isNaN(jumlah) || jumlah <= 0) {

        alert("Jumlah barang harus lebih dari 0!");

        return;
    }


    let barangLama =
        keranjang.find(
            barang => barang.nama.toLowerCase() === nama.toLowerCase()
        );


    if (barangLama) {

        barangLama.jumlah += jumlah;

        barangLama.subtotal =
            barangLama.harga *
            barangLama.jumlah;

    } else {

        keranjang.push({

            nama: nama,

            harga: harga,

            jumlah: jumlah,

            subtotal: harga * jumlah

        });

    }


    document.getElementById("namaBarang")
        .value = "";

    document.getElementById("hargaBarang")
        .value = "";

    document.getElementById("jumlahBarang")
        .value = "1";


    tampilkanKeranjang();

    hitungTotal();

}


/* ==============================
   TAMPILKAN KERANJANG
============================== */

function tampilkanKeranjang() {

    let container =
        document.getElementById("keranjang");


    if (keranjang.length === 0) {

        container.innerHTML =
            '<div class="empty">🛒 Belum ada barang</div>';

        return;
    }


    let html = `
        <div class="table-wrapper">
        <table>

            <tr>
                <th>No</th>
                <th>Barang</th>
                <th>Harga</th>
                <th>Qty</th>
                <th>Total</th>
                <th>Aksi</th>
            </tr>
    `;


    keranjang.forEach(
        (barang, index) => {

        html += `
            <tr>

                <td>${index + 1}</td>

                <td>${barang.nama}</td>

                <td>${rupiah(barang.harga)}</td>

                <td>${barang.jumlah}</td>

                <td>${rupiah(barang.subtotal)}</td>

                <td>

                    <button
                        class="btn-edit"
                        onclick="editJumlah(${index})">
                        Edit
                    </button>

                    <button
                        class="btn-hapus"
                        onclick="hapusBarang(${index})">
                        Hapus
                    </button>

                </td>

            </tr>
        `;

    });


    html += `
        </table>
        </div>
    `;


    container.innerHTML = html;

}


/* ==============================
   EDIT JUMLAH
============================== */

function editJumlah(index) {

    let jumlahBaru =
        prompt(
            "Masukkan jumlah baru:",
            keranjang[index].jumlah
        );


    if (jumlahBaru === null) return;


    jumlahBaru =
        parseInt(jumlahBaru);


    if (isNaN(jumlahBaru) || jumlahBaru <= 0) {

        alert("Jumlah tidak valid!");

        return;
    }


    keranjang[index].jumlah =
        jumlahBaru;


    keranjang[index].subtotal =
        keranjang[index].harga *
        jumlahBaru;


    tampilkanKeranjang();

    hitungTotal();

}


/* ==============================
   HAPUS BARANG
============================== */

function hapusBarang(index) {

    let yakin =
        confirm(
            "Hapus barang ini dari keranjang?"
        );


    if (!yakin) return;


    keranjang.splice(index, 1);

    tampilkanKeranjang();

    hitungTotal();

}


/* ==============================
   HITUNG TOTAL
============================== */

function hitungTotal() {

    let subtotal = 0;


    keranjang.forEach(
        barang => {

        subtotal += barang.subtotal;

    });


    let diskon =
        parseFloat(
            document.getElementById("diskon")
            .value
        ) || 0;


    if (diskon < 0) diskon = 0;

    if (diskon > 100) diskon = 100;


    document.getElementById("diskon")
        .value = diskon;


    let nilaiDiskon =
        subtotal * diskon / 100;


    let total =
        subtotal - nilaiDiskon;


    document.getElementById("subtotal")
        .innerText = rupiah(subtotal);


    document.getElementById("nilaiDiskon")
        .innerText = rupiah(nilaiDiskon);


    document.getElementById("total")
        .innerText = rupiah(total);


    hitungKembalian();

}


/* ==============================
   HITUNG KEMBALIAN
============================== */

function hitungKembalian() {

    let subtotal = 0;


    keranjang.forEach(
        barang => {

        subtotal += barang.subtotal;

    });


    let diskon =
        parseFloat(
            document.getElementById("diskon")
            .value
        ) || 0;


    let total =
        subtotal -
        (subtotal * diskon / 100);


    let bayar =
        parseFloat(
            document.getElementById("uangBayar")
            .value
        ) || 0;


    let kembalian =
        bayar - total;


    let hasil =
        document.getElementById("kembalian");


    if (bayar === 0) {

        hasil.innerText =
            "Kembalian: Rp 0";

        hasil.style.background =
            "#dcfce7";

        hasil.style.color =
            "#166534";

        return;
    }


    if (kembalian < 0) {

        hasil.innerText =
            "⚠️ Uang kurang: " +
            rupiah(Math.abs(kembalian));

        hasil.style.background =
            "#fee2e2";

        hasil.style.color =
            "#991b1b";

    } else {

        hasil.innerText =
            "Kembalian: " +
            rupiah(kembalian);

        hasil.style.background =
            "#dcfce7";

        hasil.style.color =
            "#166534";

    }

}


/* ==============================
   PROSES PEMBAYARAN
============================== */

function prosesBayar() {

    if (keranjang.length === 0) {

        alert(
            "Keranjang masih kosong!"
        );

        return;
    }


    let subtotal = 0;


    keranjang.forEach(
        barang => {

        subtotal += barang.subtotal;

    });


    let diskon =
        parseFloat(
            document.getElementById("diskon")
            .value
        ) || 0;


    let nilaiDiskon =
        subtotal * diskon / 100;


    let total =
        subtotal - nilaiDiskon;


    let bayar =
        parseFloat(
            document.getElementById("uangBayar")
            .value
        ) || 0;


    if (bayar <= 0) {

        alert(
            "Masukkan uang pembayaran terlebih dahulu!"
        );

        return;
    }


    if (bayar < total) {

        alert(
            "Uang pembayaran masih kurang!\n\n" +
            "Total: " + rupiah(total) +
            "\nBayar: " + rupiah(bayar)
        );

        return;
    }


    let kembalian =
        bayar - total;


    buatStruk(
        subtotal,
        nilaiDiskon,
        total,
        bayar,
        kembalian
    );


    alert(
        "✅ PEMBAYARAN BERHASIL!\n\n" +

        "Total: " +
        rupiah(total) +

        "\nBayar: " +
        rupiah(bayar) +

        "\nKembalian: " +
        rupiah(kembalian)
    );

}


/* ==============================
   BUAT STRUK
============================== */

function buatStruk(
    subtotal,
    diskon,
    total,
    bayar,
    kembalian
) {

    let sekarang =
        new Date();


    let tanggal =
        sekarang.toLocaleString(
            "id-ID"
        );


    document.getElementById(
        "strukTanggal"
    ).innerText = tanggal;


    let html = `
        <table>

            <tr>
                <th>Barang</th>
                <th>Qty</th>
                <th>Total</th>
            </tr>
    `;


    keranjang.forEach(
        barang => {

        html += `
            <tr>

                <td>${barang.nama}</td>

                <td>${barang.jumlah}</td>

                <td>${rupiah(barang.subtotal)}</td>

            </tr>
        `;

    });


    html += `
        </table>
    `;


    document.getElementById(
        "isiStruk"
    ).innerHTML = html;


    document.getElementById(
        "strukSubtotal"
    ).innerText = rupiah(subtotal);


    document.getElementById(
        "strukDiskon"
    ).innerText = rupiah(diskon);


    document.getElementById(
        "strukTotal"
    ).innerText = rupiah(total);


    document.getElementById(
        "strukBayar"
    ).innerText = rupiah(bayar);


    document.getElementById(
        "strukKembalian"
    ).innerText = rupiah(kembalian);


    document.getElementById(
        "struk"
    ).style.display = "block";

}


/* ==============================
   CETAK STRUK
============================== */

function cetakStruk() {

    if (keranjang.length === 0) {

        alert(
            "Belum ada barang untuk dicetak!"
        );

        return;
    }


    let subtotal = 0;


    keranjang.forEach(
        barang => {

        subtotal += barang.subtotal;

    });


    let diskonPersen =
        parseFloat(
            document.getElementById("diskon")
            .value
        ) || 0;


    let nilaiDiskon =
        subtotal *
        diskonPersen / 100;


    let total =
        subtotal -
        nilaiDiskon;


    let bayar =
        parseFloat(
            document.getElementById("uangBayar")
            .value
        ) || 0;


    if (bayar < total) {

        alert(
            "Pembayaran belum cukup!"
        );

        return;
    }


    let kembalian =
        bayar - total;


    buatStruk(
        subtotal,
        nilaiDiskon,
        total,
        bayar,
        kembalian
    );


    window.print();

}


/* ==============================
   RESET TRANSAKSI
============================== */

function resetTransaksi() {

    let yakin =
        confirm(
            "Apakah ingin membuat transaksi baru?"
        );


    if (!yakin) return;


    keranjang = [];


    document.getElementById(
        "diskon"
    ).value = "0";


    document.getElementById(
        "uangBayar"
    ).value = "";


    document.getElementById(
        "struk"
    ).style.display = "none";


    tampilkanKeranjang();

    hitungTotal();

}


/* ==============================
   JALANKAN SAAT HALAMAN DIBUKA
============================== */

tampilkanKeranjang();

hitungTotal();

</script>

</body>
</html>
