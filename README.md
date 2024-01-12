# PemesananMakanan

This program makes it easier to order food at the table using a C++ program


//code by Arya aditya 
#include <iostream>
#include <string>
using namespace std;

int main() {
    int jumlahMieAyam, totalHarga, jumlahPorsi;
    string requestBumbu;

    // Menampilkan daftar menu
    cout << "Menu Mie Ayam:\n";
    cout << "1. Mie Ayam Biasa - Rp. 10,000 per porsi\n";
    cout << "2. Mie Ayam Spesial - Rp. 15,000 per porsi\n";

    // Meminta pengguna untuk memilih menu
    cout << "Pilih nomor menu yang diinginkan (1 atau 2): ";
    cin >> jumlahMieAyam;

    // Meminta pengguna untuk memasukkan jumlah porsi yang diinginkan
    cout << "Berapa porsi yang ingin dipesan? ";
    cin >> jumlahPorsi;

    // Meminta pengguna untuk mengisi request bumbu
    cout << "Tambahkan request bumbu (opsional): ";
    cin.ignore(); // Membersihkan buffer sebelum mengambil string
    getline(cin, requestBumbu);

    // Menghitung total harga berdasarkan pilihan pengguna dan jumlah porsi
    switch (jumlahMieAyam) {
        case 1:
            totalHarga = 10000 * jumlahPorsi;
            break;
        case 2:
            totalHarga = 15000 * jumlahPorsi;
            break;
        default:
            cout << "Pilihan tidak valid.\n";
            return 1; // Keluar dari program dengan kode kesalahan
    }

    // Menampilkan rincian pemesanan
    cout << "Rincian Pemesanan:\n";
    cout << "Jumlah Porsi: " << jumlahPorsi << endl;
    cout << "Request Bumbu: " << requestBumbu << endl;
    cout << "Total Harga: Rp. " << totalHarga << endl;

    return 0;
}
