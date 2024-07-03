1.Mari kita cek langkah-langkah menggunakan algoritma Dijkstra untuk menemukan jalur terpendek dari A ke K.
Langkah-langkah Algoritma Dijkstra

	1.	Inisialisasi Jarak:
	•	Jarak awal: {A: 0, B: ∞, C: ∞, D: ∞, E: ∞, F: ∞, G: ∞, H: ∞, I: ∞, J: ∞, K: ∞}
	•	Antrian Prioritas: [(0, A)]
	2.	Proses Antrian:
	•	Ekstrak node dengan jarak terkecil dari antrian.
	•	Untuk setiap tetangga dari node ini, hitung jarak sementara.
	•	Jika jarak sementara lebih kecil dari jarak yang diketahui, perbarui jarak dan tambahkan tetangga ke antrian.

Proses Algoritma Dijkstra

Berikut adalah daftar adjacency berdasarkan graf berarah yang diberikan:

	•	A: [(B, 10), (C, 15), (D, 10)]
	•	B: [(E, 14)]
	•	C: [(E, 7), (H, 30), (I, 19)]
	•	D: [(G, 30)]
	•	E: [(H, 12)]
	•	F: [(K, 15)]
	•	G: [(I, 25)]
	•	H: [(K, 20), (I, 3)]
	•	I: [(J, 25)]
	•	J: [(K, 7)]

Inisialisasi:

	•	Jarak: {A: 0, B: ∞, C: ∞, D: ∞, E: ∞, F: ∞, G: ∞, H: ∞, I: ∞, J: ∞, K: ∞}
	•	Antrian Prioritas: [(0, A)]

Iterasi 1:

	•	Pop (0, A):
	•	Perbarui B: Jarak ke B = 10
	•	Perbarui C: Jarak ke C = 15
	•	Perbarui D: Jarak ke D = 10
	•	Antrian Prioritas: [(10, B), (15, C), (10, D)]

Iterasi 2:

	•	Pop (10, B):
	•	Perbarui E: Jarak ke E = 24
	•	Antrian Prioritas: [(10, D), (15, C), (24, E)]

Iterasi 3:

	•	Pop (10, D):
	•	Perbarui G: Jarak ke G = 40
	•	Antrian Prioritas: [(15, C), (24, E), (40, G)]

Iterasi 4:

	•	Pop (15, C):
	•	Perbarui E: Jarak ke E = 22 (lebih kecil dari sebelumnya 24)
	•	Perbarui H: Jarak ke H = 45
	•	Perbarui I: Jarak ke I = 34
	•	Antrian Prioritas: [(22, E), (34, I), (40, G), (45, H)]

Iterasi 5:

	•	Pop (22, E):
	•	Perbarui H: Jarak ke H = 34 (lebih kecil dari sebelumnya 45)
	•	Antrian Prioritas: [(34, I), (34, H), (40, G), (45, H)]

Iterasi 6:

	•	Pop (34, I):
	•	Perbarui J: Jarak ke J = 59
	•	Antrian Prioritas: [(34, H), (40, G), (45, H), (59, J)]

Iterasi 7:

	•	Pop (34, H):
	•	Perbarui K: Jarak ke K = 54
	•	Antrian Prioritas: [(40, G), (45, H), (54, K), (59, J)]

Iterasi 8:

	•	Pop (40, G):
	•	Tidak ada pembaruan karena G hanya memiliki tetangga I dengan jarak yang lebih besar.
	•	Antrian Prioritas: [(45, H), (54, K), (59, J)]

Iterasi 9:

	•	Pop (45, H):
	•	Perbarui K: Jarak ke K = 45 (lebih kecil dari sebelumnya 54)
	•	Antrian Prioritas: [(45, K), (54, K), (59, J)]

Iterasi 10:

	•	Pop (45, K):
	•	K tercapai dengan jarak terpendek 45.

Analisis Jalur A -> C -> E -> H -> J -> K

Mari kita cek jalur spesifik yang diusulkan: A -> C -> E -> H -> J -> K.

	•	A ke C: 15
	•	C ke E: 7
	•	E ke H: 12
	•	H ke J: 3
	•	J ke K: 7

Total jarak = 15 + 7 + 12 + 3 + 7 = 44

Dengan menggunakan algoritma Dijkstra dan memeriksa jalur yang diberikan:
Kesimpulan 
Jalur terpendek dari A ke K adalah A -> C -> E -> H -> J -> K dengan total jarak 44.




2. Edge edge yang terhubung berdasarkan Directed Graph
Edge = <A,C>, <B,A>, <C,D>, <C,H>, <C,G>, <E,C>, <F,E>, <F,H>, <H,I>, <I,G>, <I,J>, <J,K>, <K,H>, <K,F> 
