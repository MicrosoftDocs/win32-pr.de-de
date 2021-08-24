---
title: WDS-Transportclientfunktionen
description: Dieses Modul definiert die Strukturen und Funktionen, aus denen die Schnittstelle zwischen dem Inhaltsempfänger und dem Transportclient besteht.
ms.assetid: 20c3116b-3a0d-4048-b6f2-81c03e0a80ef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3f228370aa0973e124b1877dcf8a458d1356170fbb872a05a1867ac0489c00a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680400"
---
# <a name="wds-transport-client-functions"></a>WDS-Transportclientfunktionen

Dieses Modul definiert die Strukturen und Funktionen, aus denen die Schnittstelle zwischen dem Inhaltsempfänger und dem Transportclient besteht.



| Funktion                                                                              | Beschreibung                                                                                                                                                                 |
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*PFN \_ WdsTransportClientReceiveContents*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientreceivecontents) | Gibt an, dass ein Datenblock zur Verwendung bereit ist.                                                                                                                         |
| [*PFN \_ WdsTransportClientReceiveMetadata*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientreceivemetadata) | Empfängt Metadateninformationen zu einer Datei.                                                                                                                                 |
| [*PFN \_ WdsTransportClientSessionComplete*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientsessioncomplete) | Gibt an, dass die Sitzung erfolgreich abgeschlossen wurde oder ein Fehler aufgetreten ist.                                                                                                  |
| [*PFN \_ WdsTransportClientSessionStart*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientsessionstart)       | Gibt die Dateigröße und andere serverseitige Informationen über die Datei an den Consumer an.                                                                                   |
| [*PFN \_ WdsTransportClientSessionStartEx*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientsessionstartex)   | Gibt die Dateigröße und andere serverseitige Informationen über die Datei an den Consumer an.                                                                                   |
| [**WdsTransportClientAddRefBuffer**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientaddrefbuffer)              | Erhöht die Verweisanzahl für einen Puffer im Besitz des Multicastclients.                                                                                                   |
| [**WdsTransportClientCancelSession**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientcancelsession)            | Gibt die Ressourcen frei, die einer Sitzung im Client zugeordnet sind.                                                                                                             |
| [**WdsTransportClientCloseSession**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientclosesession)              | Gibt die Ressourcen frei, die einer Sitzung im Client zugeordnet sind.                                                                                                             |
| [**WdsTransportClientCompleteReceive**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientcompletereceive)        | Gibt an, dass die Verarbeitung für einen Datenblock abgeschlossen ist und dass der Multicastclient diesen Datenblock aus seinem Cache entfernen kann, um Platz für weitere Empfänge zu machen. |
| [**WdsTransportClientInitialize**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientinitialize)                  | Initialisiert den Multicastclient.                                                                                                                                           |
| [**WdsTransportClientInitializeSession**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientinitializesession)    | Initiiert eine Multicastdateiübertragung.                                                                                                                                        |
| [**WdsTransportClientQueryStatus**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientquerystatus)                | Ruft den aktuellen Status einer laufenden oder vollständigen Multicastübertragung vom Multicastclient ab.                                                                    |
| [**WdsTransportClientRegisterCallback**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientregistercallback)      | Registriert einen Rückruf beim Multicastclient.                                                                                                                             |
| [**WdsTransportClientReleaseBuffer**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientreleasebuffer)            | Dekrementiert die Verweisanzahl für einen Puffer, der sich im Besitz des Multicastclients befindet.                                                                                                   |
| [**WdsTransportClientShutdown**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientshutdown)                      | Fährt den Multicastclient herunter.                                                                                                                                            |
| [**WdsTransportClientStartSession**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientstartsession)              | Initiiert eine Multicastdateiübertragung.                                                                                                                                        |
| [**WdsTransportClientWaitForCompletion**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientwaitforcompletion)    | Blockiert, bis entweder die Multicastsitzung abgeschlossen ist oder das angegebene Timeout erreicht ist.                                                                                  |



 

 

 




