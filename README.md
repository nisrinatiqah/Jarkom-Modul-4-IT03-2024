# Laporan Resmi Praktikum Jarkom Modul 4 2024

---

# Anggota Kelompok
| Nama  | NRP  |
|----------|----------|
| Nisrina Atiqah Dwiputri Ridzki | 5027231075 |
| Nicholas Arya Krisnugroho Rerangin | 5027231058 |

# Daftar Isi
- [Cisco Packet Tracer](#cisco_packet_tracer)
  - [Topologi CPT](#topologi_cpt)
  - [Rute CPT](#rute_cpt)
  - [Tree VLSM](#tree_vlsm)
  - [Pembagian IP-VLSM](#pembagian_ip_vlsm)
  - [Konfigurasi CPT](#konfigurasi_cpt)
  - [Testing CPT](#testing_cpt)
- [GNS3](#gns3)
  - [Topologi GNS3](#topologi_gns3)
  - [Rute GNS3](#rute_gns3)
  - [Tree CIDR](#tree_cidr)
  - [Pembagian IP-CIDR](#pembagian_ip_cidr)
  - [Konfigurasi GNS3](#konfigurasi_gns3)
 
# Cisco Packet Tracer
## Topologi CPT
  <img width="976" alt="topologi CPT MODUL 4" src="https://github.com/user-attachments/assets/9f460c85-b0db-4237-8002-501c7e6c62cb">

## Rute CPT
  https://docs.google.com/spreadsheets/d/1mTRZrkasedMP7LDwilHhliAe9xZxYaP1UW7B9fuT8tI/edit?usp=sharing
  
  ![image](https://github.com/user-attachments/assets/d3ef7279-064e-4bc9-bd74-8ae171816012)

## Tree VLSM
  ![TREE VLSM drawio](https://github.com/user-attachments/assets/7ad742d9-cf3d-4203-9978-a4904c3adac2)

## Pembagian IP-VLSM
  Pengurutan Kebutuhan
  | Netmask  | Subnet  |
  |--|--|
  |/21 | A12|
  |/22 | A18 |
  |/23 | A22 |
  |/23 | A13 |
  |/23 | A5 |
  |/25 | A15 |
  |/26 | A20 | 
  |/26 | A8 |
  | /27 | A3 |
  | /28 | A11 |
  |/29 | A6 |
  |/29 | A7 |
  |/29 | A10 |
  /30 | A1
  /30 | A2
  /30 | A4
  /30 | A9
  /30 | A14
  /30 | A16
  /30 | A17
  /30 | A19
  |/30 | A21 |
  
  ![image](https://github.com/user-attachments/assets/f4b26dee-2b60-4741-a1e3-684ed7f7178a)
  
## Konfigurasi CPT
  - A12

    GEN:0 
    ```
    enable
    configure terminal
    interface fa0/1
    ip address 192.245.0.1 255.255.248.0
    no shutdown
    ```
    
    GEN:1 
    ```
    enable
    configure terminal
    interface fa0/0
    ip address 192.245.0.2 255.255.248.0
    no shutdown
    ```

    MiComet
    ```
    Interface fa0
    IP Address: 192.245.0.3
    Subnet Mask: 255.255.248.0
    Gateway: 192.245.0.1
    ```

    Soro_Robo_AZK
    ```
    Interface fa0
    IP Address: 192.245.0.4
    Subnet Mask: 255.255.248.0
    Gateway: 192.245.0.1
    ```

  - A18

    AREA15
    ```
    enable
    configure terminal
    interface fa0/1
    ip address 192.245.8.1 255.255.252.0
    no shutdown
    ```

    Moona
    ```
    Interface fa0
    IP Address: 192.245.8.2
    Subnet Mask: 255.255.252.0
    Gateway: 192.245.8.1
    ```

    Risu
    ```
    Interface fa0
    IP Address: 192.245.8.3
    Subnet Mask: 255.255.252.0
    Gateway: 192.245.8.1
    ```

    lofi
    ```
    Interface fa0
    IP Address: 192.245.8.4
    Subnet Mask: 255.255.252.0
    Gateway: 192.245.8.1
    ```
