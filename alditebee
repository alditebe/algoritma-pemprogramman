#include <iostream>
#include <string>
#include <vector>

using namespace std;

struct Barang {
    int id;
    string nama;
    int jumlah;
    double harga;
};

class InventarisBarang {
private:
    vector<Barang> ListBarang;

public:
    InventarisBarang() {
        // Inisialisasi dengan beberapa barang inventaris
        ListBarang.push_back({1, "Laptop", 10, 15000000.0});
        ListBarang.push_back({2, "Mouse", 50, 150000.0});
        ListBarang.push_back({3, "Keyboard", 30, 300000.0});
        ListBarang.push_back({4, "Monitor", 20, 2000000.0});
        ListBarang.push_back({5, "Printer", 5, 2500000.0});
        ListBarang.push_back({6, "Pulpen", 500, 25000.0});
        ListBarang.push_back({7, "Pensil", 120, 20000.0});
        ListBarang.push_back({8, "Penghapus", 46, 10000.0});
        ListBarang.push_back({9, "Buku", 50, 35000.0});
        ListBarang.push_back({10, "Kondom durex", 70, 70000.0});
    }

    void tambah_Barang() {
        Barang barang;

        std::cout << "Masukan Nama Barang: ";
        cin >> barang.nama;
        std::cout << "Masukan NO ID Barang: ";
        cin >> barang.id;
        std::cout << "Masukan Jumlah Barang: ";
        cin >> barang.jumlah;
        std::cout << "Masukan Harga Satuan: ";
        cin >> barang.harga;

        ListBarang.push_back(barang);
        std::cout << "Yeay Data Barang Telah Ditambahkan!.\n";
    }

    void edit_Barang(int id) {
        for (auto& barang : ListBarang) {
            if (barang.id == id) {
                std::cout << "Masukkan Nama Barang Baru dengan ID " << id << ": ";
                cin.ignore();
                getline(cin, barang.nama);
                std::cout << "Masukkan Jumlah Barang Baru dengan ID " << id << ": ";
                cin >> barang.jumlah;
                std::cout << "Masukkan Harga Barang Satuan Baru dengan ID " << id << ": ";
                cin >> barang.harga;
                std::cout << "Yeay Data Barang Berhasil Diubah!.\n";
                return;
            }
        }
        std::cout << "Yah Barang dengan ID " << id << " Tidak ada.\n";
    }

    void cari_Barang(int id) {
        for (const auto& barang : ListBarang) {
            if (barang.id == id) {
                std::cout << "Nama Barang: " << barang.nama << "\n";
                std::cout << "ID Barang: " << barang.id << "\n";
                std::cout << "Jumlah Barang: " << barang.jumlah << "\n";
                std::cout << "Harga Satuan Barang: " << barang.harga << "\n";
                return;
            }
        }
        std::cout << "Yah Barang dengan ID " << id << " Tidak ada.\n";
    }

    void hapus_Barang(int id) {
        for (auto it = ListBarang.begin(); it != ListBarang.end(); ++it) {
            if (it->id == id) {
                ListBarang.erase(it);
                std::cout << "Data barang dengan ID " << id << " berhasil dihapus!.\n";
                return;
            }
        }
        std::cout << "Yah Barang dengan ID " << id << " Tidak ada.\n";
    }

    void tampilkan_listBarang() {
        if (ListBarang.empty()) {
            std::cout << "Mohon Maaf List Tidak Ada!.\n";
        } else {
            std::cout << "List Barang:\n";
            for (const auto& barang : ListBarang) {
                std::cout << "ID Barang: " << barang.id << endl;
                std::cout << "Nama Barang: " << barang.nama << endl;
                std::cout << "Harga Satuan Barang: " << barang.harga << endl;
                std::cout << "Jumlah Barang: " << barang.jumlah << endl;
                std::cout << "-------------------------\n";
            }
        }
    }
};

int main() {
    InventarisBarang barang;
    string pilihan;

    do {
        std::cout << "1. Tambah Barang\n";
        std::cout << "2. Edit Barang\n";
        std::cout << "3. Cari Barang\n";
        std::cout << "4. Hapus Barang\n";
        std::cout << "5. List Barang\n";
        std::cout << "6. Keluar\n";
        std::cout << "Pilihan anda: ";

        getline(std::cin, pilihan);

        if (pilihan == "1") {
            barang.tambah_Barang();
        } else if (pilihan == "2") {
            int id;
            std::cout << "Masukkan ID: ";
            std::cin >> id;
            std::cin.ignore();
            barang.edit_Barang(id);
        } else if (pilihan == "3") {
            int id;
            std::cout << "Masukkan ID: ";
            std::cin >> id;
            std::cin.ignore();
            barang.cari_Barang(id);
        } else if (pilihan == "4") {
            int id;
            std::cout << "Masukkan ID: ";
            std::cin >> id;
            std::cin.ignore();
            barang.hapus_Barang(id);
        } else if (pilihan == "5") {
            barang.tampilkan_listBarang();
        } else if (pilihan != "6") {
            std::cout << "Pilihan tidak valid.\n";
        }
    } while (pilihan != "6");

    return 0;
}
