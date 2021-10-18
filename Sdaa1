#include <iostream>
#include <string>
#include <fstream>

using namespace std;

struct {
	string barangArray[10] = {"Hoodie Zhongli", "Jaket Saitama", "T-Shirt Kaneki", "Topeng Kaneki"};
	string warnaArray[10] = {"Coklat", "Kuning", "Putih", "Hitam"}; 
	string ukuranArray[10] = {"XL", "L", "XXL", "-"};
	long long hargaArray[10] = {200000, 50000, 350000, 1000000};
	float ratingArray[10] = {9.5, 8.0, 9.8, 8.9};
}distro;


void show_menu();
int getOption();
void tmbhDataBarang();
void tampilDataBarang();
void updateDataBarang();
void hapusDataBarang();

int no;

int main()
{
	while(true){
		no = 0;
		show_menu();
	}

	return 0;
}

void show_menu(){
	system("cls");
	cout << "================================================" << endl;
	cout << "|  Program CRUD Manajemen Barang Distro Anime  |" << endl;
	cout << "|                                              |" << endl;
	cout << "|               Rivan Abdillah                 |" << endl;
	cout << "|                 2009106025                   |" << endl;
	cout << "|             Informatika A 2020               |" << endl;
	cout << "================================================" << endl;

	int opsi = getOption();

	while(opsi != 6){
		switch(opsi){
			case 1:
				tmbhDataBarang();
				break;
			case 2:
				tampilDataBarang();
				break;
			case 3:
				updateDataBarang();
				break;
			case 4:
				hapusDataBarang();
				break;
			case 5:
				cout << "==============================================" << endl;
				cout << "|   Terima Kasih Telah Menggunakan Program   |" << endl;
				cout << "|                                            |" << endl;
				cout << "|       Mohon Maaf Jika ada Salah Kata       |" << endl;
				cout << "==============================================" << endl;
				exit(0);
			default:
				cout << "Mohon masukkan angka sesuai perintah!" << endl;
				break;
			
		}
	}
}

void back_to_menu(){
	char opsi;
	cout << "\nKembali ke menu? y/n : "; cin >> opsi;
	if((opsi == 'Y') | (opsi == 'y')){
		show_menu();
	} else{
		cout << "==============================================" << endl;
		cout << "|   Terima Kasih Telah Menggunakan Program   |" << endl;
		cout << "|                                            |" << endl;
		cout << "|       Mohon Maaf Jika ada Salah Kata       |" << endl;
		cout << "==============================================" << endl;
		exit(0);
	}
}

void tmbhDataBarang(){

	int index = -1;
	int besar = *(&distro.barangArray + 1) - distro.barangArray;

	cout << "=========================================" << endl;
	cout << "|     Tambah Data Barang Pada Distro    |" << endl;
	cout << "=========================================" << endl;

	for(int i = 0; i < 10; i++) {
		if(distro.barangArray[i] == "") {
			index = i;
			break;
		}
	}

	if(index != -1){
		cout << "Nama Barang : "; getline(cin, *(distro.barangArray+index));
		cout << "Warna       : "; getline(cin, *(distro.warnaArray+index));
		cout << "Ukuran      : "; getline(cin, *(distro.ukuranArray+index));
		cout << "Rating      : "; cin >> *(distro.ratingArray+index);
		cout << "Harga       : "; cin >> *(distro.hargaArray+index);
	}

	cout << "=========================================" << endl;
	cout << "|       Data Berhasil Ditambahkan       |" << endl;
	cout << "=========================================" << endl;

	back_to_menu();

}



void updateDataBarang(){
	cout << "=========================================" << endl;
	cout << "|     Update Data Barang Pada Distro    |" << endl;
	cout << "=========================================" << endl;	

	int besar = *(&distro.barangArray + 1) - distro.barangArray;

	cout << "No.\tNama Barang.\tWarna.\tUkuran.\tRating.\tHarga." << endl;
	for(int i = 0; i < besar; i++) {
		if(distro.barangArray[i] == ""){
			continue;
		}else{
			cout << i+1 << "\t";
			cout << distro.barangArray[i] << "\t";
			cout << distro.warnaArray[i] << "\t";
			cout << distro.ukuranArray[i] << "\t";
			cout << distro.ratingArray[i] << "\t";
			cout << distro.hargaArray[i] << "\t\n";
			no++;
		}
	}
	int pilih;
	cout << "\nPilih barang yang ingin di update: "; cin >> pilih;
	cout << "Diupdate Menjadi: " << endl;

	cin.ignore();
	cout << "Nama Barang : "; getline(cin, *(distro.barangArray+pilih-1));
	cout << "Warna       : "; getline(cin, *(distro.warnaArray+pilih-1));
	cout << "Ukuran      : "; getline(cin, *(distro.ukuranArray+pilih-1));
	cout << "Rating      : "; cin >> *(distro.ratingArray+pilih-1);
	cout << "Harga       : "; cin >> *(distro.hargaArray+pilih-1);

	

	cout << "======================================" << endl;
	cout << "|       Data Berhasil Diupdate       |" << endl;
	cout << "======================================" << endl;	
	
	back_to_menu();

}

void hapusDataBarang(){

	cout << "============================================" << endl;
	cout << "|     Menghapus Data Barang Pada Distro    |" << endl;
	cout << "============================================" << endl;

	int besar = *(&distro.barangArray + 1) - distro.barangArray;
	cout << "No.\tNama Barang.\tWarna.\tUkuran.\tRating.\tHarga." << endl;
	for(int i = 0; i < besar; i++) {
		if(distro.barangArray[i] == ""){
			continue;
		}else{
			cout << i+1 << "\t";
			cout << distro.barangArray[i] << "\t";
			cout << distro.warnaArray[i] << "\t";
			cout << distro.ukuranArray[i] << "\t";
			cout << distro.ratingArray[i] << "\t";
			cout << distro.hargaArray[i] << "\t\n";
			no++;
		}
	}
	int hapus;
	cout << "Pilih Barang yang ingin dihapus: "; cin >> hapus;
	if (distro.barangArray[hapus-1] == ""){
		cout << "Data yang anda pilih tidak ada" <<endl;
		back_to_menu();
	}else{
		for(int i = hapus-1; i < no+1; i++){
			distro.barangArray[i] = distro.barangArray[i+1];
			if(no+1-i == 0){
				distro.barangArray[i] = "";
				distro.warnaArray[i] = "";
				distro.ukuranArray[i] = "";
				distro.ratingArray[i] = 0;
				distro.hargaArray[i] = 0;
			}
		}
	}
	cout << "=====================================" << endl;
	cout << "|       Data Berhasil Dihapus       |" << endl;
	cout << "=====================================" << endl;

	back_to_menu();

}

void tampilDataBarang(){

	cout << "============================================" << endl;
	cout << "|     Tampilkan Data Barang Pada Distro    |" << endl;
	cout << "============================================" << endl;

	int besar = *(&distro.barangArray + 1) - distro.barangArray;

	cout << "No.\tNama Barang.\tWarna.\tUkuran.\tRating.\tHarga." << endl;
	for(int i = 0; i < besar; i++) {
		if(distro.barangArray[i] == ""){
			continue;
		}else{
			cout << i+1 << "\t";
			cout << *(distro.barangArray+i) << "\t";
			cout << *(distro.warnaArray+i) << "\t";
			cout << *(distro.ukuranArray+i) << "\t";
			cout << *(distro.ratingArray+i) << "\t";
			cout << *(distro.hargaArray+i) << "\t\n";
			no++;
		}
	}

	back_to_menu();
}

int getOption(){
	int input;

	cout << "\n1. Tambah data barang baru di distro" << endl;
	cout << "2. Tampilkan data barang di distro" << endl;
	cout << "3. Mengubah data barang di distro" << endl;
	cout << "4. Hapus data barang di distro" << endl;
	cout << "5. Keluar dari program" << endl;
	cout << "=======================================" << endl;
	cout << "Tentukan pilihan 1-5: ";
	cin >> input;
	cin.ignore(1, '\n');
	return input;
}
