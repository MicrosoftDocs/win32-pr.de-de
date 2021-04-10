---
title: Verwalten von DNS-Ressourcen Einträgen
description: Ein Ressourcen Daten Satz, der häufig als RR bezeichnet wird, ist die Eintrags Einheit in DNS-Zonendateien. RRS sind die grundlegenden Bausteine von Hostnamen-und IP-Informationen und werden verwendet, um alle DNS-Abfragen aufzulösen.
ms.assetid: ddad5f14-5a2d-4966-87b7-b354666f9e24
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99edffa52b5137858468fd64122d2af826a896ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856520"
---
# <a name="managing-dns-resource-records"></a>Verwalten von DNS-Ressourcen Einträgen

Ein Ressourcen Daten Satz, der häufig als RR bezeichnet wird, ist die Eintrags Einheit in DNS-Zonendateien. RRS sind die grundlegenden Bausteine von Hostnamen-und IP-Informationen und werden verwendet, um alle DNS-Abfragen aufzulösen. Ressourcen Einträge sind in einer relativ großen Vielfalt von Typen enthalten, um erweiterte Namensauflösungsdienste bereitzustellen.

Verschiedene Arten von RRS haben unterschiedliche Formate, da Sie unterschiedliche Daten enthalten. Viele RRS haben ein gemeinsames Format. Jeder DNS-Server enthält RRS für den Teil des namesplatzes, für den er autorisierend ist.

Der DNS-WMI-Anbieter unterstützt derzeit die folgenden RR-Typen. Klicken Sie auf den Namen des Ressourceneinsatzes, um zur entsprechenden Referenzseite zu springen.



| Ressourcen Daten Satz (im Anbieter)                             | BESCHREIBUNG                                                  |
|-----------------------------------------------------------|--------------------------------------------------------------|
| [**MicrosoftDNS- \_ aType**](microsoftdns-atype.md)         | Name des Adressdaten Satzes                               |
| [**MicrosoftDNS \_ aaaatype**](microsoftdns-aaaatype.md)   | Host-zu-IPv6-Adress Datensatz                                  |
| [**MicrosoftDNS \_ afsdbtype**](microsoftdns-afsdbtype.md) | Daten Bank Server-Datensatz für Andrew-Datei System                    |
| [**MicrosoftDNS- \_ atmatype**](microsoftdns-atmatype.md)   | Datensatz Address-to-Name-Datensatz                                   |
| [**MicrosoftDNS \_ cnametype**](microsoftdns-cnametype.md) | [*Kanonischer namens*](c-gly.md) Daten Satz |
| [**MicrosoftDNS \_ hinfotype**](microsoftdns-hinfotype.md) | Host Informationsdaten Satz                                      |
| [**MicrosoftDNS \_ isdntype**](microsoftdns-isdntype.md)   | Digitaler Netzwerkdaten Satz integrierter Dienste                   |
| [**MicrosoftDNS- \_ KeyType**](microsoftdns-keytype.md)     | Schlüsseldaten Satz. Siehe RFC 2535                                     |
| [**MicrosoftDNS \_ mbtype**](microsoftdns-mbtype.md)       | Post Fach Daten Satz                                               |
| [**MicrosoftDNS- \_ mdtype**](microsoftdns-mdtype.md)       | Mail-Agent für den Domänen Daten Satz                             |
| [**MicrosoftDNS- \_ mftype**](microsoftdns-mftype.md)       | Postweiterleitungs-Agent für den Domänen Daten Satz                  |
| [**MicrosoftDNS- \_ mgtype**](microsoftdns-mgtype.md)       | Mail Gruppendaten Satz                                            |
| [**MicrosoftDNS- \_ minfotype**](microsoftdns-minfotype.md) | Datensatz mit Mail Informationen                                      |
| [**MicrosoftDNS- \_ mrtype**](microsoftdns-mrtype.md)       | Umbenennungs Daten Satz                                        |
| [**MicrosoftDNS- \_ mxtype**](microsoftdns-mxtype.md)       | Nachrichtenaustausch Daten Satz                                        |
| [**MicrosoftDNS \_ nstype**](microsoftdns-nstype.md)       | Namensservereintrag                                           |
| [**MicrosoftDNS \_ nxttype**](microsoftdns-nxttype.md)     | Nächster Datensatz                                                  |
| [**MicrosoftDNS \_ ptrtype**](microsoftdns-ptrtype.md)     | Address to Name Mapping Record                               |
| [**MicrosoftDNS- \_ rptype**](microsoftdns-rptype.md)       | Datensatz für Verantwortliche Personen                                    |
| [**MicrosoftDNS- \_ rttype**](microsoftdns-rttype.md)       | Weiterleiten durch Daten Satz                                         |
| [**MicrosoftDNS- \_ sigtype**](microsoftdns-sigtype.md)     | Signatur Daten Satz                                             |
| [**MicrosoftDNS- \_ soatype**](microsoftdns-soatype.md)     | Autoritäts Anfang                                           |
| [**MicrosoftDNS- \_ srvtype**](microsoftdns-srvtype.md)     | Dienst Daten Satz                                               |
| [**MicrosoftDNS- \_ txttype**](microsoftdns-txttype.md)     | Text Daten Satz                                                  |
| [**MicrosoftDNS \_ winstype**](microsoftdns-winstype.md)   | WINS-Serverdaten Satz                                           |
| [**MicrosoftDNS \_ winsrtype**](microsoftdns-winsrtype.md) | WINS-Datensatz für Reverse-Lookup                                   |
| [**MicrosoftDNS \_ wkstype**](microsoftdns-wkstype.md)     | Datensatz für bekannte Dienste                                   |
| [**MicrosoftDNS \_ X25Type**](microsoftdns-x25type.md)     | X. 121 Zuordnung von Address-to-Name-Zuordnung                         |



 

## <a name="administration-steps"></a>Verwaltungsschritte

Der DNS-WMI-Anbieter ermöglicht die Verwaltung von RRS vom Server selbst oder von Remote Hosts aus. Die folgenden allgemeinen Schritte zum Verwalten von RRS mit dem DNS-WMI-Anbieter sind erforderlich:

-   Herstellen einer Verbindung mit dem DNS-WMI-Anbieter
-   Eine Ressourcen Daten Satz Instanz wird erhalten.
-   Auflisten oder Ändern einer Ressourcen Daten Satz Eigenschaft oder Verwenden einer Methode

Die folgenden Aufgaben sind mit den zugehörigen Skript Beispielen verknüpft.

-   [Auflisten von Ressourcentypen](dns-wmi-provider-samples-managing-dns-resource-records.md)
-   [Hinzufügen eines Ressourcen Datensatzes](dns-wmi-provider-samples-managing-dns-resource-records.md)
-   [Löschen eines Ressourcen Datensatzes](dns-wmi-provider-samples-managing-dns-resource-records.md)
-   [Ändern eines Ressourcen Datensatzes](dns-wmi-provider-samples-managing-dns-resource-records.md)

 

 




