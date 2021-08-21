---
description: Die DRT-API (Distributed Routing Table) verwendet die folgenden Funktionen.
ms.assetid: 1ceff217-d410-47fa-99a2-8588f001859e
title: Tabellenfunktionen für verteiltes Routing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00501a1a04a3acba23fe55f90acfbf7ca8fee7427c36ea1d36d8800fb8787321
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776350"
---
# <a name="distributed-routing-table-functions"></a>Tabellenfunktionen für verteiltes Routing

Die DRT-API (Distributed Routing Table) verwendet die folgenden Funktionen.

## <a name="lifetime-management-functions"></a>Funktionen für die Lebensdauerverwaltung



| Funktion                                           | Beschreibung                                                                                                    |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**DrtOpen**](/windows/desktop/api/drt/nf-drt-drtopen)                         | Erstellt eine lokale DRT-Instanz anhand von Kriterien, die von der [**DRT \_ SETTINGS-Struktur**](/windows/desktop/api/drt/ns-drt-drt_settings) angegeben werden.  |
| [**DrtClose**](/windows/desktop/api/drt/nf-drt-drtclose)                       | Schließt und entfernt die lokale Instanz des DRT.                                                              |
| [**DrtGetEventData**](/windows/desktop/api/drt/nf-drt-drtgeteventdata)         | Ruft Ereignisdaten ab, die einem signalisierten Ereignis zugeordnet sind.                                                         |
| [**DrtGetEventDataSize**](/windows/desktop/api/drt/nf-drt-drtgeteventdatasize) | Gibt die Größe der [**DRT \_ EVENT \_ DATA-Struktur**](/windows/desktop/api/drt/ns-drt-drt_event_data) zurück, die einem signalisierten Ereignis zugeordnet ist. |



 

## <a name="module-management-functions"></a>Modulverwaltungsfunktionen



| Funktion                                                                           | Beschreibung                                                                                                                           |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**DrtCreatePnrpBootstrapResolver**](/windows/desktop/api/drt/nf-drt-drtcreatepnrpbootstrapresolver)           | Erstellt einen Bootstrap-Resolver basierend auf dem PNRP-Protokoll.                                                                              |
| [**DrtDeletePnrpBootstrapResolver**](/windows/desktop/api/drt/nf-drt-drtdeletepnrpbootstrapresolver)           | Löscht einen Bootstrap-Konfliktlöser basierend auf dem PNRP-Protokoll.                                                                              |
| [**DrtCreateDnsBootstrapResolver**](/windows/desktop/api/drt/nf-drt-drtcreatednsbootstrapresolver)             | Erstellt einen Bootstrapanbieter, der einen bekannten Host anhand des Namens kontaktiert.                                                             |
| [**DrtDeleteDnsBootstrapResolver**](/windows/desktop/api/drt/nf-drt-drtdeletednsbootstrapresolver)             | Löscht einen Bootstrapanbieter, der einen bekannten Host anhand des Namens kontaktiert.                                                             |
| [**DrtCreateIpv6UdpTransport**](/windows/desktop/api/drt/nf-drt-drtcreateipv6udptransport)                     | Erstellt einen Transport basierend auf dem IPv6-UDP-Protokoll.                                                                                   |
| [**DrtDeleteIpv6UdpTransport**](/windows/desktop/api/drt/nf-drt-drtdeleteipv6udptransport)                     | Löscht einen Transport basierend auf dem IPv6-UDP-Protokoll.                                                                                   |
| [**DrtCreateDerivedKeySecurityProvider**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider) | Erstellt einen abgeleiteten Schlüsselsicherheitsanbieter für das DRT.                                                                                  |
| [**DrtCreateDerivedKey**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkey)                                 | Erstellt einen Schlüssel, der von [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey) verwendet werden kann, wenn das DRT einen abgeleiteten Schlüsselsicherheitsanbieter verwendet. |
| [**DrtDeleteDerivedKeySecurityProvider**](/windows/desktop/api/drt/nf-drt-drtdeletederivedkeysecurityprovider) | Löscht einen abgeleiteten Schlüsselsicherheitsanbieter für das DRT.                                                                                  |
| [**DrtCreateNullSecurityProvider**](/windows/desktop/api/drt/nf-drt-drtcreatenullsecurityprovider)             | Erstellt einen NULL-Sicherheitsanbieter. Dieser Sicherheitsanbieter erfordert keine Knoten zum Authentifizieren von Schlüsseln.                                 |
| [**DrtDeleteNullSecurityProvider**](/windows/desktop/api/drt/nf-drt-drtdeletenullsecurityprovider)             | Löscht einen NULL-Sicherheitsanbieter.                                                                                                     |



 

## <a name="registration-functions"></a>Registrierungsfunktionen



| Funktion                                     | Beschreibung                                                    |
|----------------------------------------------|----------------------------------------------------------------|
| [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey)     | Registriert einen Schlüssel im DRT.                                    |
| [**DrtUpdateKey**](/windows/desktop/api/drt/nf-drt-drtupdatekey)         | Aktualisiert die Anwendungsdaten, die einem registrierten Schlüssel zugeordnet sind. |
| [**DrtUnregisterKey**](/windows/desktop/api/drt/nf-drt-drtunregisterkey) | Deregistrierung eines Schlüssels beim DRT.                                |



 

## <a name="search-functions"></a>Suchfunktionen



| Funktion                                                 | Beschreibung                                                                                                                                                                                                             |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DrtStartSearch**](/windows/desktop/api/drt/nf-drt-drtstartsearch)                 | Durchsucht das DRT anhand von Kriterien, die in der [**DRT \_ SEARCH \_ INFO-Struktur**](/windows/desktop/api/drt/ns-drt-drt_search_info) angegeben sind, nach einem Schlüssel.                                                                                                      |
| [**DrtContinueSearch**](/windows/desktop/api/drt/nf-drt-drtcontinuesearch)           | Setzt eine DRT \_ SEARCH \_ RETURN \_ PATH-Suche nach einem Schlüssel im DRT fort. Diese Funktion wird nur verwendet, wenn das **fIterative-Flag** in der zugeordneten [**DRT \_ SEARCH \_ INFO-Struktur**](/windows/desktop/api/drt/ns-drt-drt_search_info) auf **TRUE** festgelegt ist. |
| [**DrtGetSearchResult**](/windows/desktop/api/drt/nf-drt-drtgetsearchresult)         | Ruft die Suchergebnisse ab.                                                                                                                                                                                         |
| [**DrtGetSearchResultSize**](/windows/desktop/api/drt/nf-drt-drtgetsearchresultsize) | Gibt die Größe des nächsten verfügbaren Suchergebnisses zurück.                                                                                                                                                                   |
| [**DrtGetSearchPath**](/windows/desktop/api/drt/nf-drt-drtgetsearchpath)             | Gibt eine Liste der Knoten zurück, die während des Suchvorgangs kontaktiert wurden.                                                                                                                                                          |
| [**DrtGetSearchPathSize**](/windows/desktop/api/drt/nf-drt-drtgetsearchpathsize)     | Gibt die Größe des Suchpfads zurück, der die Anzahl der Knoten darstellt, die im Suchvorgang verwendet werden.                                                                                                             |
| [**DrtEndSearch**](/windows/desktop/api/drt/nf-drt-drtendsearch)                     | Bricht eine Suche nach einem Schlüssel in einem DRT ab, und daher wird die Rückgabe von Ergebnissen über [**DRT \_ SEARCH \_ RESULT**](/windows/desktop/api/drt/ns-drt-drt_search_result) beendet. Diese API kann jederzeit aufgerufen werden, nachdem eine Suche ausgegeben wurde.              |



 

## <a name="instance-name-functions"></a>Funktionen für Instanznamen



| Funktion                                                 | Beschreibung                                                      |
|----------------------------------------------------------|------------------------------------------------------------------|
| [**DrtGetInstanceName**](/windows/desktop/api/drt/nf-drt-drtgetinstancename)         | Ruft den einer DRT-Instanz zugeordneten Namen ab.                    |
| [**DrtGetInstanceNameSize**](/windows/desktop/api/drt/nf-drt-drtgetinstancenamesize) | Gibt die Größe des Instanznamens der verteilten Routingtabelle zurück. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verteilte Routingtabellenenumerationen](distributed-routing-table-enumerations.md)
</dt> <dt>

[Tabellenstrukturen für verteiltes Routing](distributed-routing-table-structures.md)
</dt> <dt>

[Referenz für verteiltes Routing Tabellen-API](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



