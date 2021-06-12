---
title: Verwalten von DNS-Ressourceneinträgen
description: Erfahren Sie mehr über das Verwalten von Ressourcendatensätzen. Ein Ressourceneintrag ist die Informationseinheit in DNS-Zonendateien, die zum Auflösen aller DNS-Abfragen verwendet wird.
ms.assetid: ddad5f14-5a2d-4966-87b7-b354666f9e24
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba6c818899414cc541a1c89bfd11747051b2f5f1
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011113"
---
# <a name="managing-dns-resource-records"></a>Verwalten von DNS-Ressourceneinträgen

Ein Ressourceneintrag, der häufig als RR bezeichnet wird, ist die Informationseinheit in DNS-Zonendateien. RRs sind die grundlegenden Bausteine von Hostnamen und IP-Informationen und werden verwendet, um alle DNS-Abfragen aufzulösen. Ressourcendatensätze sind in einer recht vielzahl von Typen enthalten, um erweiterte Dienste zur Namensauflösung zu bieten.

Verschiedene Arten von RRs haben unterschiedliche Formate, da sie unterschiedliche Daten enthalten. Viele RRs verwenden ein gemeinsames Format. Jeder DNS-Server enthält RRs für den Teil des Namensraums, für den er autoritativ ist.

Der DNS-WMI-Anbieter unterstützt derzeit die folgenden RR-Typen. Klicken Sie auf den Namen des Ressourcendatensatz, um zur Referenzseite zu wechseln.



| Ressourcendatensatz (im Anbieter)                             | Beschreibung                                                  |
|-----------------------------------------------------------|--------------------------------------------------------------|
| [**MicrosoftDNS \_ AType**](microsoftdns-atype.md)         | Zuordnungsdatensatz "Name zu Adresse"                               |
| [**MicrosoftDNS \_ AAAAType**](microsoftdns-aaaatype.md)   | Host-zu-Ipv6-Adressdatensatz                                  |
| [**MicrosoftDNS \_ AFSDBType**](microsoftdns-afsdbtype.md) | Andrew File System Database Server-Datensatz                    |
| [**MicrosoftDNS \_ ATMAType**](microsoftdns-atmatype.md)   | ATM-Adress-zu-Name-Datensatz                                   |
| [**MicrosoftDNS \_ CNAMEType**](microsoftdns-cnametype.md) | [*Datensatz "Kanonischer Name"*](c-gly.md) |
| [**MicrosoftDNS \_ HINFOType**](microsoftdns-hinfotype.md) | Hostinformations-Datensatz                                      |
| [**MicrosoftDNS \_ ISDNType**](microsoftdns-isdntype.md)   | Digitale Netzwerkdatensatz für integrierte Dienste                   |
| [**MicrosoftDNS \_ KEYType**](microsoftdns-keytype.md)     | KEY-Datensatz. Siehe RFC 2535                                     |
| [**MicrosoftDNS \_ MBType**](microsoftdns-mbtype.md)       | Postfachdatensatz                                               |
| [**MicrosoftDNS \_ MDType**](microsoftdns-mdtype.md)       | E-Mail-Agent für den Domänendatensatz                             |
| [**MicrosoftDNS \_ MFType**](microsoftdns-mftype.md)       | E-Mail-Weiterleitungs-Agent für den Domänendatensatz                  |
| [**MicrosoftDNS \_ MGType**](microsoftdns-mgtype.md)       | E-Mail-Gruppendatensatz                                            |
| [**MicrosoftDNS \_ MINFOType**](microsoftdns-minfotype.md) | Datensatz mit E-Mail-Informationen                                      |
| [**MicrosoftDNS \_ MRType**](microsoftdns-mrtype.md)       | Postfach-Umbenennungsdatensatz                                        |
| [**MicrosoftDNS \_ MXType**](microsoftdns-mxtype.md)       | Datensatz des E-Mail-Austauschers                                        |
| [**MicrosoftDNS \_ NSType**](microsoftdns-nstype.md)       | Namensservereintrag                                           |
| [**MicrosoftDNS \_ NXTType**](microsoftdns-nxttype.md)     | Nächster Datensatz                                                  |
| [**MicrosoftDNS \_ PTRType**](microsoftdns-ptrtype.md)     | Zuordnungsdatensatz "Adresse zu Name"                               |
| [**MicrosoftDNS \_ RPType**](microsoftdns-rptype.md)       | Datensatz der verantwortlichen Person                                    |
| [**MicrosoftDNS \_ RTType**](microsoftdns-rttype.md)       | Route through record                                         |
| [**MicrosoftDNS \_ SIGType**](microsoftdns-sigtype.md)     | Signaturdatensatz                                             |
| [**MicrosoftDNS \_ SOAType**](microsoftdns-soatype.md)     | Autoritätsbeginn                                           |
| [**MicrosoftDNS \_ SRVType**](microsoftdns-srvtype.md)     | Dienstdatensatz                                               |
| [**MicrosoftDNS \_ TXTType**](microsoftdns-txttype.md)     | Textdatensatz                                                  |
| [**MicrosoftDNS \_ WINSType**](microsoftdns-winstype.md)   | WINS-Serverdatensatz                                           |
| [**MicrosoftDNS \_ WINSRType**](microsoftdns-winsrtype.md) | WINS-Reverse-Lookupdatensatz                                   |
| [**MicrosoftDNS \_ WKSType**](microsoftdns-wkstype.md)     | Datensatz für bekannte Dienste                                   |
| [**MicrosoftDNS \_ X25Type**](microsoftdns-x25type.md)     | X.121-Adress-zu-Name-Zuordnungsdatensatz                         |



 

## <a name="administration-steps"></a>Verwaltungsschritte

Der DNS-WMI-Anbieter ermöglicht die Verwaltung von RRs vom Server selbst oder von Remotehosts. Die allgemeinen Schritte, die zum Verwalten von RRs mithilfe des DNS-WMI-Anbieters erforderlich sind, sind:

-   Herstellen einer Verbindung mit dem DNS-WMI-Anbieter
-   Abrufen einer Ressourcendatensatzinstanz
-   Auflisten oder Ändern einer Ressourceneintragseigenschaft oder Verwenden einer Methode

Die folgenden Aufgaben sind mit den zugehörigen Skriptbeispielen verknüpft.

-   [Auflisten von Ressourcentypen](dns-wmi-provider-samples-managing-dns-resource-records.md)
-   [Hinzufügen eines Ressourcendatensatz](dns-wmi-provider-samples-managing-dns-resource-records.md)
-   [Löschen eines Ressourcendatensatz](dns-wmi-provider-samples-managing-dns-resource-records.md)
-   [Ändern eines Ressourcendatensatz](dns-wmi-provider-samples-managing-dns-resource-records.md)

 

 




