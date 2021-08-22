---
title: WDS-Transportanbieterfunktionen
description: Benutzerdefinierte Inhaltsanbieter können die folgenden Rückruffunktionen für den Multicastserver verfügbar machen.
ms.assetid: 30ec1969-4e90-458e-8a9f-39a7bbf4cd79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1044c923226dcc618e816219dcec9d7edf78855e03acf13b76ba4d7ed9ad15a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053258"
---
# <a name="wds-transport-provider-functions"></a>WDS-Transportanbieterfunktionen

Benutzerdefinierte Inhaltsanbieter können die folgenden Rückruffunktionen für den Multicastserver verfügbar machen.



| Funktion                                                                               | Beschreibung                                                                                                             |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [*WdsTransportProviderCloseContent*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderclosecontent)             | Schließt einen von einem Handle angegebenen Inhaltsstream.                                                                          |
| [*WdsTransportProviderCloseInstance*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidercloseinstance)           | Schließt eine Instanz eines Inhaltsanbieters, der durch ein Handle angegeben wird.                                                         |
| [*WdsTransportProviderCompareContent*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidercomparecontent)         | Vergleicht einen angegebenen Inhaltsnamen und eine angegebene Instanz mit einem geöffneten Inhaltsstream, um zu ermitteln, ob sie identisch sind.             |
| [*WdsTransportProviderCreateInstance*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidercreateinstance)         | Öffnet eine neue Instanz eines Inhaltsanbieters.                                                                             |
| [*WdsTransportProviderDumpState*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderdumpstate)                   | Weist den Transportanbieter an, eine Zusammenfassung seines Zustands und alle anderen relevanten Informationen im Ablaufverfolgungsprotokoll aus drucken. |
| [*WdsTransportProviderGetContentMetadata*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidergetcontentmetadata) | Ruft Metadaten für einen geöffneten Inhaltsstream ab.                                                                          |
| [*WdsTransportProviderGetContentSize*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidergetcontentsize)         | Ruft die Größe eines geöffneten Inhaltsstreams ab.                                                                           |
| [*WdsTransportProviderInitialize*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize)                 | Initialisiert einen Inhaltsanbieter.                                                                                         |
| [*WdsTransportProviderOpenContent*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovideropencontent)               | Öffnet eine neue statische Ansicht eines Inhaltsstreams.                                                                            |
| [*WdsTransportProviderReadContent*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderreadcontent)               | Liest Inhalt aus einem geöffneten Inhaltsstream.                                                                              |
| [*WdsTransportProviderRefreshSettings*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderrefreshsettings)       | Weist den Transportanbieter an, alle relevanten Einstellungen erneut zu überprüfen.                                                       |
| [*WdsTransportProviderShutdown*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidershutdown)                     | Fährt den Inhaltsanbieter herunter.                                                                                         |
| [*WdsTransportProviderUserAccessCheck*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovideruseraccesscheck)       | Gibt den Zugriff auf einen Inhaltsstream basierend auf dem Token eines Benutzers an.                                                           |



 

 

 




