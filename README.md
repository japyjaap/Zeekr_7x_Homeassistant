# Zeekr Home Assistant Integratie (7X)

Deze integratie verbindt jouw Zeekr (geoptimaliseerd voor de 7X) met Home Assistant via de officiële API. 

## 🔑 Installatie & Configuratie

Voor de installatie zijn specifieke tokens nodig die je moet onderscheppen uit het netwerkverkeer van de Zeekr app (bijvoorbeeld via een proxy zoals Charles of HTTP Toolkit):

- **X-VIN**: Het unieke identificatienummer van je voertuig.
- **Access Token**: Je autorisatie-token. 
  - *Let op:* Dit token is momenteel slechts **één week geldig**. Hierna moet je het token handmatig vernieuwen in de configuratie.

## ✨ Functionaliteiten

### 🚗 Voertuig Status
- **Batterij:** Accu percentage, actieradius, laadstatus en laadvermogen.
- **Banden:** Real-time bandenspanning en temperatuur per wiel.
- **Onderhoud:** Kilometerstand, afstand en dagen tot de volgende onderhoudsbeurt.
- **Klimaat:** Binnentemperatuur en status van de pre-conditioning.

### 📅 Reisplanning (Travel Plan)
- **Flexibele Planning:** Ondersteuning voor zowel eenmalige ritten (Dagelijks) als een wekelijks schema (Cyclus).
- **Update Knop:** Pas tijden en dagen aan in HA en "push" de hele planning naar de auto.

## ⚠️ Bekende Problemen (Known Issues)

Hoewel de integratie stabiel is, zijn er enkele bekende beperkingen (vaak gerelateerd aan de Zeekr API):

1. **Airco Bediening:** Net als in de officiële Zeekr app reageert de auto niet altijd op het 'Stop' commando voor de airco. Soms moet je de airco **twee keer handmatig uitzetten** voordat deze daadwerkelijk stopt.
2. **Token Refresh:** Omdat de Access Token verloopt na 7 dagen, moet de integratie daarna opnieuw worden ingesteld met een vers token.

## 🛠 Installatie
1. Kopieer de map `Zeekr_7x` naar je `custom_components` map.
2. Herstart Home Assistant.
3. Voeg de integratie toe en vul je `X-VIN` en `Access Token` in.
