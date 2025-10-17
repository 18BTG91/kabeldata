# Kabeldata API

Ett öppet JSON-API för svenska kabeldata, avsett för elberäkningar (t.ex. Ik3 och Zför).

## Struktur
- `cables.json` — Huvudfil med länkar till tillverkarspecifika filer
- `nexans.json`, `nkt.json`, `draka.json` — Kabeldata per tillverkare

## Exempel på användning
```kotlin
interface CableApiService {
    @GET("https://dittnamn.github.io/kabeldata/cables.json")
    suspend fun getManufacturers(): CableRoot
}
