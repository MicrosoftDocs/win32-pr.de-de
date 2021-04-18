---
description: Die DRT-API (verteilte Routing Tabelle) nutzt die folgenden Funktionen.
ms.assetid: 1ceff217-d410-47fa-99a2-8588f001859e
title: Tabellen Funktionen für verteilte Routing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cd48c3a60f458285ce5f607f9ab6bcf7a557cd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358904"
---
# <a name="distributed-routing-table-functions"></a>Tabellen Funktionen für verteilte Routing

Die DRT-API (verteilte Routing Tabelle) nutzt die folgenden Funktionen.

## <a name="lifetime-management-functions"></a>Lebensdauer Verwaltungsfunktionen



| Funktion                                           | BESCHREIBUNG                                                                                                    |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**Drtopen**](/windows/desktop/api/drt/nf-drt-drtopen)                         | Erstellt eine lokale DRT-Instanz unter Verwendung der von der [**DRT- \_ Einstellungs**](/windows/desktop/api/drt/ns-drt-drt_settings) Struktur angegebenen Kriterien.  |
| [**Drtclose**](/windows/desktop/api/drt/nf-drt-drtclose)                       | Schließt die lokale Instanz der DRT und entfernt Sie.                                                              |
| [**Drtgeteventdata**](/windows/desktop/api/drt/nf-drt-drtgeteventdata)         | Ruft die einem signalisierten Ereignis zugeordneten Ereignisdaten ab.                                                         |
| [**Drtgeteventdatasize**](/windows/desktop/api/drt/nf-drt-drtgeteventdatasize) | Gibt die Größe der [**DRT- \_ Ereignis \_ Daten**](/windows/desktop/api/drt/ns-drt-drt_event_data) Struktur zurück, die einem signalisierten Ereignis zugeordnet ist. |



 

## <a name="module-management-functions"></a>Modul Verwaltungsfunktionen



| Funktion                                                                           | BESCHREIBUNG                                                                                                                           |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**Drtkreatepnrpbootstrapresolver**](/windows/desktop/api/drt/nf-drt-drtcreatepnrpbootstrapresolver)           | Erstellt einen Bootstrap-Konflikt Löser basierend auf dem PNRP-Protokoll.                                                                              |
| [**Drtdeletepnrpbootstrapresolver**](/windows/desktop/api/drt/nf-drt-drtdeletepnrpbootstrapresolver)           | Löscht einen Bootstrap-Konflikt Löser basierend auf dem PNRP-Protokoll.                                                                              |
| [**Drtkreatednsbootstrapresolver**](/windows/desktop/api/drt/nf-drt-drtcreatednsbootstrapresolver)             | Erstellt einen Bootstrap-Anbieter, der nach Namen einen bekannten Host kontaktiert.                                                             |
| [**Drtdeletednsbootstrapresolver**](/windows/desktop/api/drt/nf-drt-drtdeletednsbootstrapresolver)             | Löscht einen Bootstrap-Anbieter, der nach Namen einen bekannten Host kontaktiert.                                                             |
| [**DrtCreateIpv6UdpTransport**](/windows/desktop/api/drt/nf-drt-drtcreateipv6udptransport)                     | Erstellt einen Transport auf der Grundlage des IPv6-UDP-Protokolls.                                                                                   |
| [**DrtDeleteIpv6UdpTransport**](/windows/desktop/api/drt/nf-drt-drtdeleteipv6udptransport)                     | Löscht einen Transport auf der Grundlage des IPv6-UDP-Protokolls.                                                                                   |
| [**Drtkreatederivedkeysecurityprovider**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider) | Erstellt einen abgeleiteten Schlüssel Sicherheitsanbieter für das DRT.                                                                                  |
| [**Drtkreatederivedkey**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkey)                                 | Erstellt einen Schlüssel, der von [**drtregisterkey**](/windows/desktop/api/drt/nf-drt-drtregisterkey) verwendet werden kann, wenn der DRT einen abgeleiteten Schlüssel Sicherheitsanbieter verwendet. |
| [**Drtdeletederivedkeysecurityprovider**](/windows/desktop/api/drt/nf-drt-drtdeletederivedkeysecurityprovider) | Löscht einen abgeleiteten Schlüssel Sicherheitsanbieter für das DRT.                                                                                  |
| [**Drtkreatenullsecurityprovider**](/windows/desktop/api/drt/nf-drt-drtcreatenullsecurityprovider)             | Erstellt einen NULL-Sicherheitsanbieter. Dieser Sicherheitsanbieter erfordert keine Knoten zum Authentifizieren von Schlüsseln.                                 |
| [**Drtdeletenullsecurityprovider**](/windows/desktop/api/drt/nf-drt-drtdeletenullsecurityprovider)             | Löscht einen NULL-Sicherheitsanbieter.                                                                                                     |



 

## <a name="registration-functions"></a>Registrierungsfunktionen



| Funktion                                     | BESCHREIBUNG                                                    |
|----------------------------------------------|----------------------------------------------------------------|
| [**Drtregisterkey**](/windows/desktop/api/drt/nf-drt-drtregisterkey)     | Registriert einen Schlüssel in der DRT.                                    |
| [**Drtupdatekey**](/windows/desktop/api/drt/nf-drt-drtupdatekey)         | Aktualisiert die einem registrierten Schlüssel zugeordneten Anwendungsdaten. |
| [**Drtunregisterkey**](/windows/desktop/api/drt/nf-drt-drtunregisterkey) | Hebt die Registrierung eines Schlüssels aus dem DRT auf.                                |



 

## <a name="search-functions"></a>Suchfunktionen



| Funktion                                                 | BESCHREIBUNG                                                                                                                                                                                                             |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Drtstartsearch**](/windows/desktop/api/drt/nf-drt-drtstartsearch)                 | Durchsucht das DRT nach einem Schlüssel mithilfe der in der [**DRT- \_ Such \_ Informations**](/windows/desktop/api/drt/ns-drt-drt_search_info) Struktur angegebenen Kriterien.                                                                                                      |
| [**Drtcontinuesearch**](/windows/desktop/api/drt/nf-drt-drtcontinuesearch)           | Setzt die Suche nach einem DRT- \_ \_ \_ Suchpfad für einen Schlüssel in der DRT fort. Diese Funktion wird nur verwendet, wenn das **-Flag in der** zugeordneten [**DRT- \_ Such \_ Informations**](/windows/desktop/api/drt/ns-drt-drt_search_info) Struktur auf **true** festgelegt ist. |
| [**Drtgetsearchresult**](/windows/desktop/api/drt/nf-drt-drtgetsearchresult)         | Ruft die Suchergebnisse ab.                                                                                                                                                                                         |
| [**Drtgetsearchresultsize**](/windows/desktop/api/drt/nf-drt-drtgetsearchresultsize) | Gibt die Größe des nächsten verfügbaren Suchergebnisses zurück.                                                                                                                                                                   |
| [**Drtgetsearchpath**](/windows/desktop/api/drt/nf-drt-drtgetsearchpath)             | Gibt eine Liste der Knoten zurück, die während des Such Vorgangs kontaktiert wurden.                                                                                                                                                          |
| [**Drtgetsearchpathsize**](/windows/desktop/api/drt/nf-drt-drtgetsearchpathsize)     | Gibt die Größe des Suchpfads zurück, der die Anzahl der im Suchvorgang verwendeten Knoten darstellt.                                                                                                             |
| [**Drtendsearch**](/windows/desktop/api/drt/nf-drt-drtendsearch)                     | Bricht eine Suche nach einem Schlüssel in einem DRT ab. Folglich wird die Rückgabe von Ergebnissen über das [**DRT- \_ Such \_ Ergebnis**](/windows/desktop/api/drt/ns-drt-drt_search_result) angehalten. Diese API kann zu einem beliebigen Zeitpunkt aufgerufen werden, nachdem eine Suche ausgegeben wurde.              |



 

## <a name="instance-name-functions"></a>Instanznamensfunktionen



| Funktion                                                 | BESCHREIBUNG                                                      |
|----------------------------------------------------------|------------------------------------------------------------------|
| [**Drtgetinstancename**](/windows/desktop/api/drt/nf-drt-drtgetinstancename)         | Ruft den Namen ab, der einer DRT-Instanz zugeordnet ist.                    |
| [**Drtgetinstancenamesize**](/windows/desktop/api/drt/nf-drt-drtgetinstancenamesize) | Gibt die Größe des Tabellen Instanznamens der verteilten Routing Tabelle zurück. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verteilte Routing Tabellen-Enumerationen](distributed-routing-table-enumerations.md)
</dt> <dt>

[Strukturen verteilter Routing Tabellen](distributed-routing-table-structures.md)
</dt> <dt>

[Tabellen-API Referenz zu verteiltem Routing](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



