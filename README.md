# Identyfikacja wzorców i anomalii w deformacjach terenu na podstawie danych EGMS

## Cel ćwiczenia

W ćwiczeniu analizujemy szeregi czasowe przemieszczeń punktów PS-InSAR pochodzących z danych EGMS. Celem jest rozpoznanie różnych sposobów zachowania punktów w czasie oraz wskazanie tych, których przebieg deformacji różni się od typowego zachowania obserwowanego w analizowanym zbiorze.

Analiza ma odpowiedzieć na dwa główne pytania:

1. **Które punkty PS wykazują nietypowe zachowanie deformacyjne?**
Do ich identyfikacji wykorzystamy metodę Isolation Forest, która pozwala wskazać obserwacje różniące się od większości punktów pod względem analizowanych cech szeregu czasowego.

2. **Jakie typowe wzorce zachowania występują wśród punktów PS?**
Za pomocą metody K-means pogrupujemy punkty o podobnych charakterystykach deformacji i porównamy przebieg ich szeregów czasowych.



EGMS: https://egms.land.copernicus.eu/

Budynki: https://eubucco.com/data/download/v0.2

Dokumentacja: https://land.copernicus.eu/en/products/european-ground-motion-service?tab=documentation

## Zasięg danych

Plik EGMS obejmuje cały kafel 100 × 100 km. Przed analizą punkty są filtrowane według `data/AOI/Leczna.shp`. Współrzędne `easting` i `northing` w pliku EGMS są interpretowane jako EPSG:3035; AOI jest przekształcany do tego CRS przed filtrowaniem.
