# UAS-Kecerdasan-Buatan-
Alfia Rohmah Safara (23422039)
```python
import networkx as nx
import matplotlib.pyplot as plt

# Representasi Pohon 1 sebagai graph
pohon1 = nx.DiGraph()

# Menambahkan hubungan antar node untuk Pohon 1
edges_pohon1 = [
    ("Hadi", "Bayu"), ("Hadi", "Desi"), ("Hadi", "Wahyu"), ("Hadi", "Rina"), ("Hadi", "Ardi"),
    ("Bayu", "Fahrul"), ("Fahrul", "Tari"), ("Desi", "Nurul"), ("Nurul", "Wanda"), ("Nurul", "Aji"),
    ("Wahyu", "Yanto"), ("Yanto", "Gunawan"),
    ("Rina", "Hamzah"),
    ("Ardi", "Eka"), ("Ardi", "Mira"), ("Ardi", "Bastian"),
    ("Eka", "Anggun"), ("Mira", "Boy"),
    ("Ardi", "Ana")
]

pohon1.add_edges_from(edges_pohon1)

# Representasi Pohon 2 sebagai graph
pohon2 = nx.DiGraph()

# Menambahkan hubungan antar node untuk Pohon 2
edges_pohon2 = [
    (6, 1), (6, 2), (6, 8), (7, 3), (7, 4), (7, 5),
    (1, 0), (2, "Tari"), (2, "Nurul"), (8, "Yanto"), (8, "Gunawan"),
    (3, "Hamzah"), (4, "Eka"), (4, 9), (5, "Bastian"), (9, "Anggun"), (9, "Boy")
]

pohon2.add_edges_from(edges_pohon2)

# Fungsi untuk menggambar pohon
def draw_tree(tree, title):
    plt.figure(figsize=(12, 8))
    pos = nx.nx_pydot.graphviz_layout(tree, prog="dot")  # Menggunakan layout hierarkis
    nx.draw(tree, pos, with_labels=True, arrows=True, node_size=3000, node_color="lightblue", font_size=10, font_weight="bold")
    plt.title(title)
    plt.show()

# Visualisasi Pohon 1
draw_tree(pohon1, "Pohon 1")

# Visualisasi Pohon 2
draw_tree(pohon2, "Pohon 2")
```
