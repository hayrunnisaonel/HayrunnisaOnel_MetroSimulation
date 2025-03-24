# HayrunnisaOnel_MetroSimulation
# Hayrunnisa Önel - Metro Rota Simülasyonu

Bu proje, sürücüsüz bir metro ağı üzerinde **en hızlı** ve **en az aktarmalı** rotaları bulabilen bir Python simülasyonudur. Ankara örnek metro ağı kullanılarak geliştirilmiştir.



## Proje Amacı

- Metro ağı bir **graf** veri yapısı ile modellenmiştir.
- Kullanıcıdan alınan başlangıç ve hedef istasyonlarına göre:
  - **BFS algoritması** ile en az aktarma yapılan rota bulunur.
  - **A\* algoritması** (heuristic’siz Dijkstra) ile en kısa sürede ulaşılan rota hesaplanır.



## Kullanılan Teknolojiler ve Kütüphaneler

 Teknoloji        | Açıklama                                     

  Python          | Proje dili                                   
 `collections`    | `deque` yapısı ile BFS için kuyruk sistemi   
 `heapq`          | A* için öncelik kuyruğu oluşturma                          



## Algoritmaların Çalışma Mantığı

### 1. En Az Aktarmalı Rota – **BFS (Breadth-First Search)**

- Her istasyon bir düğüm (node) olarak tanımlanır.
- Aynı hat üzerindeki geçişlerde aktarma sayılmaz.
- Hat değişikliği olduğunda bir aktarma sayılır.
- BFS ile en kısa (minimum aktarma) rota bulunur.

### 2. En Hızlı Rota – **A* (Heuristicsiz / Dijkstra)**

- Her kenar (edge) istasyonlar arası süre ile tanımlanır.
- A* algoritması ile toplam süre en az olan yol bulunur.
- Heuristik kullanılmadığı için Dijkstra gibi çalışır.



## Örnek Terminal Çıktısı

1. AŞTİ'den OSB'ye:
En az aktarmalı rota: AŞTİ -> Kızılay -> Ulus -> Demetevler -> OSB
En hızlı rota (18 dakika): AŞTİ -> Kızılay -> Ulus -> Demetevler -> OSB

2. Batıkent'ten Keçiören'e:
En az aktarmalı rota: Batıkent -> Demetevler -> Gar -> Keçiören
En hızlı rota (21 dakika): Batıkent -> Demetevler -> Gar -> Keçiören

3. Keçiören'den AŞTİ'ye:
En az aktarmalı rota: Keçiören -> Gar -> Sıhhiye -> Kızılay -> AŞTİ
En hızlı rota (19 dakika): Keçiören -> Gar -> Sıhhiye -> Kızılay -> AŞTİ

## Geliştirme Fikirleri

Metro hattı görselleştirmesi (örneğin: networkx, matplotlib ile)

Dash veya Tkinter kullanarak kullanıcı arayüzü oluşturulması

Geliştirici
Hayrunnisa Önel
