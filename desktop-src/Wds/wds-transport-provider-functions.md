---
title: WDS-Transport Anbieter Funktionen
description: Benutzerdefinierte Inhaltsanbieter können dem Multicast Server die folgenden Rückruf Funktionen zur Verfügung stellen.
ms.assetid: 30ec1969-4e90-458e-8a9f-39a7bbf4cd79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a2e67747d8ef5738a4bf3bee8ff2ffb3b35cf43
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713854"
---
# <a name="wds-transport-provider-functions"></a>WDS-Transport Anbieter Funktionen

Benutzerdefinierte Inhaltsanbieter können dem Multicast Server die folgenden Rückruf Funktionen zur Verfügung stellen.



| Funktion                                                                               | BESCHREIBUNG                                                                                                             |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [*Wdstransportproviderclosecontent*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderclosecontent)             | Schließt einen von einem Handle angegebenen Inhaltsdaten Strom.                                                                          |
| [*Wdstransportprovidercloseinstance*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidercloseinstance)           | Schließt eine Instanz eines Inhalts Anbieters, der durch ein Handle angegeben wird.                                                         |
| [*Wdstransportprovidercomparecontent*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidercomparecontent)         | Vergleicht einen angegebenen Inhalts Namen und eine Instanz mit einem geöffneten Inhaltsstream, um zu bestimmen, ob diese identisch sind.             |
| [*Wdstransportproviderkreateinstance*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidercreateinstance)         | Öffnet eine neue Instanz eines Inhalts Anbieters.                                                                             |
| [*Wdstransportproviderdumpstate*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderdumpstate)                   | Weist den Transportanbieter an, eine Zusammenfassung seines Zustands und alle anderen relevanten Informationen in das Ablauf Verfolgungs Protokoll zu drucken. |
| [*Wdstransportprovidergetcontentmetadata*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidergetcontentmetadata) | Ruft Metadaten für einen geöffneten Inhaltsstream ab.                                                                          |
| [*Wdstransportprovidergetcontentsize*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidergetcontentsize)         | Ruft die Größe eines geöffneten Inhaltsstreams ab.                                                                           |
| [*Wdstransportproviderinitialize*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize)                 | Initialisiert einen Inhaltsanbieter.                                                                                         |
| [*Wdstransportprovideropencontent*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovideropencontent)               | Öffnet eine neue statische Ansicht eines Inhaltsstreams.                                                                            |
| [*Wdstransportproviderlescontent*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderreadcontent)               | Liest Inhalt aus einem geöffneten Inhaltsstream.                                                                              |
| [*Wdstransportprovidererfrischendes-Einstellungen*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderrefreshsettings)       | Weist den Transportanbieter an, alle relevanten Einstellungen erneut zu registrieren.                                                       |
| [*Wdstransportprovidershutdown*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidershutdown)                     | Herunterfahren des Inhalts Anbieters                                                                                         |
| [*Wdstransportprovideruseraccesscheck*](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovideruseraccesscheck)       | Gibt den Zugriff auf einen Inhaltsstream basierend auf dem Token eines Benutzers an.                                                           |



 

 

 




