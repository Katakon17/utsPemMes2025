# utsPemMes2025
## 7. Kesimpulan

### a. Perbandingan K-Means dan DBSCAN
Berdasarkan skor Silhouette dan DBI, clustering dari K-Means memiliki beberapa cluster yang tersusun rapi tetapi tidak sedikit juga yang overlap. Sedangkan DBSCAN memiliki nilai negatif yang menandakan performa clusteringnya tidak sebagus K-Means dalam dataset ini, meskipun nilai DBI DBSCAN sedikit lebih baik dari K-Means (1.5123 dibanding 1.6843).

Secara overall, **K-Means lebih baik daripada DBSCAN** dikarenakan:
- K-Means memiliki nilai positif Silhouette (0.25) dibanding nilai negatif DBSCAN (-0.15)
- Nilai negatif Silhouette pada DBSCAN menandakan bahwa DBSCAN tidak berhasil menentukan cluster natural

### b. Nilai Metrik Terbaik
=== CLUSTERING EVALUATION ===
KMeans - Silhouette Score: 0.2479
KMeans - Davies-Bouldin Index: 1.6843
DBSCAN - Silhouette Score: -0.1482
DBSCAN - Davies-Bouldin Index: 1.5123

**Metrik terbaik:**
- **Silhouette Score**: 0.2479 (K-Means)
- **Davies-Bouldin Index**: 1.5123 (DBSCAN)

### c. Hasil Query Annoy
Berdasarkan hasil output, **hampir semua tetangga yang ditemukan termasuk dalam cluster yang sama (19 dari 20)**. 

Ini membuktikan bahwa algoritma KMeans berhasil membuat segmentasi yang konsisten dan meaningful, dimana pelanggan dengan karakteristik serupa benar-benar dikelompokkan bersama. Meskipun terdapat sedikit overlap antara Cluster 3 dan Cluster 0, hal ini merefleksikan kompleksitas data perilaku kartu kredit di dunia nyata.
