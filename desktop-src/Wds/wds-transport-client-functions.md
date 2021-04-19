---
title: WDS-Transport Client Funktionen
description: Dieses Modul definiert die Strukturen und Funktionen, die die Schnittstelle zwischen dem Inhalts Empfänger und dem Transport Client bilden.
ms.assetid: 20c3116b-3a0d-4048-b6f2-81c03e0a80ef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8449f620eb04045d37e56499be998477d361871c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339224"
---
# <a name="wds-transport-client-functions"></a>WDS-Transport Client Funktionen

Dieses Modul definiert die Strukturen und Funktionen, die die Schnittstelle zwischen dem Inhalts Empfänger und dem Transport Client bilden.



| Funktion                                                                              | BESCHREIBUNG                                                                                                                                                                 |
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*PFN \_ wdstransportclientreceivecontents*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientreceivecontents) | Gibt an, dass ein Datenblock zur Verwendung bereit ist.                                                                                                                         |
| [*PFN \_ wdstransportclientreceivemetadata*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientreceivemetadata) | Empfängt Metadateninformationen zu einer Datei.                                                                                                                                 |
| [*PFN \_ wdstransportclientsessioncomplete*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientsessioncomplete) | Gibt an, dass die Sitzung erfolgreich abgeschlossen wurde oder einen Fehler festgestellt hat.                                                                                                  |
| [*PFN \_ wdstransportclientsessionstart*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientsessionstart)       | Gibt die Dateigröße und andere serverseitige Informationen über die Datei an den Consumer an.                                                                                   |
| [*PFN \_ wdstransportclientsessionstartex*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientsessionstartex)   | Gibt die Dateigröße und andere serverseitige Informationen über die Datei an den Consumer an.                                                                                   |
| [**Wdstransportclientadress-Puffer**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientaddrefbuffer)              | Erhöht den Verweis Zähler für einen Puffer, der im Besitz des Multicast Clients ist.                                                                                                   |
| [**Wdstransportclientcancelsession**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientcancelsession)            | Gibt die einer Sitzung im Client zugeordneten Ressourcen frei.                                                                                                             |
| [**Wdstransportclientclosesession**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientclosesession)              | Gibt die einer Sitzung im Client zugeordneten Ressourcen frei.                                                                                                             |
| [**Wdstransportclientcompletereceive**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientcompletereceive)        | Gibt an, dass die gesamte Verarbeitung in einem Datenblock abgeschlossen ist und dass der Multicast Client diesen Datenblock aus dem Cache entfernen kann, um Platz für weitere Empfangs Vorgänge zu schaffen. |
| [**Wdstransportclientinitialize**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientinitialize)                  | Initialisiert den Multicast Client.                                                                                                                                           |
| [**Wdstransportclientinitializesession**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientinitializesession)    | Initiiert eine Multicast Dateiübertragung.                                                                                                                                        |
| [**Wdstransportclientquerystatus**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientquerystatus)                | Ruft den aktuellen Status einer laufenden oder kompletten Multicast Übertragung vom Multicast Client ab.                                                                    |
| [**Wdstransportclientregistercallback**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientregistercallback)      | Registriert einen Rückruf beim Multicast Client.                                                                                                                             |
| [**Wdstransportclientreleasebuffer**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientreleasebuffer)            | Dekremente den Verweis Zähler für einen Puffer, der im Besitz des Multicast Clients ist.                                                                                                   |
| [**Wdstransportclientshutdown**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientshutdown)                      | Fährt den Multicast Client herunter.                                                                                                                                            |
| [**Wdstransportclientstarzession**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientstartsession)              | Initiiert eine Multicast Dateiübertragung.                                                                                                                                        |
| [**Wdstransportclientwaitforcompletion**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientwaitforcompletion)    | Blockiert, bis die Multicast Sitzung entweder beendet oder das angegebene Timeout erreicht wurde.                                                                                  |



 

 

 




