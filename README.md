# Tugas-PEMROGRAMAN ORIENTASI OBJEK (OOP) Pertemuan 6

Nama  : Ghamma Pramana Putra Setyadin

Nim   : 312210247

Kelas : TI.22.B1



**Membuat class pegawai dengan setter dan getter**

1. Buat folder baru
2. Masukan code berikut seperti dibawah ini :

    using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace tugas6
{
    public class Pegawai
    {
        private string _nama;
        private double _gajiPokok;

        public void setNama(string paramNama)
        {
            _nama = paramNama;
        }
        // Ghamma Pramana Putra Setyadin (312210247)
        public string getNama()
        {
            return _nama;
        }
        public void setGajiPokok(double paramGaji)
        {
            _gajiPokok = paramGaji;
        }

        public double getGajiPokok()
        {
            return _gajiPokok;
        }

        public virtual void cetakInfo()
        {
            Console.WriteLine("Pegawai : " + getNama());
            Console.WriteLine("Gaji Pokok : " + getGajiPokok());
        }
    }
    public class Manager : Pegawai
    {
        private double _tunjangan;

        public void setTunjangan(double paramTunjangan)
        {
            _tunjangan = paramTunjangan;
        }
        public double getTunjangan()
        {
            return _tunjangan;
        }
        public void cetakTunjangan()
        {
            Console.WriteLine("Tunjangan Anda : " + getTunjangan());
        }
        public virtual void cetakInfo()
        {
            Console.WriteLine("Pegawai : " + getNama());
            Console.WriteLine("Posisi anda : Manager ");
            Console.WriteLine("Gaji Pokok Anda : " + getGajiPokok());
        }
    }
    // Ghamma Pramana Putra Setyadin (312210247)

    public class Programmer : Pegawai
    {
        private double _bonus;

        public void setBonus(double paramBonus)
        {
            _bonus = paramBonus;
        }

        public double getBonus()
        {
            return _bonus;
        }

        public void cetakBonus()
        {
            Console.WriteLine("Bonus Anda : " + getBonus());
        }

        public virtual void cetakInfo()
        {
            Console.WriteLine("Pegawai : " + getNama());
            Console.WriteLine("Posisi : Programer");
            Console.WriteLine("Gaji Pokok Anda : " + getGajiPokok());
        }
    }
    // Ghamma Pramana Putra Setyadin (312210247)

    class program{
        static void Main(string[] args)
        {
            Console.WriteLine("=====Pegawai Class=====");
            Pegawai pegawai = new Pegawai();
            pegawai.setNama("Asep Pegawai");
            pegawai.setGajiPokok(3000000);
            pegawai.cetakInfo();

            Console.WriteLine("=====Manager Class=====");
            Manager manager = new Manager();
            manager.setNama("Gambul Manager");
            manager.setGajiPokok(48000000);
            manager.setTunjangan(5000000);
            manager.cetakInfo();
            manager.cetakTunjangan();

            Console.WriteLine("=====Programer Class=====");
            Programmer programer = new Programmer();
            programer.setNama("Rayden Programer");
            programer.setGajiPokok(25000000);
            programer.setBonus(6000000);
            programer.cetakInfo();
            programer.cetakBonus();
        }
    }
}

3. Kemudian kita start
4. Untuk output seperti dibawah ini

   ![WhatsApp Image 2023-11-07 at 21 44 02](https://github.com/ghamma1928/Tugas-OOP/assets/115474950/7c978939-6439-4fc1-b186-25b70a8f58de)

