---
title: Protokollierung (Windows Filterplattform)
description: Windows Die Filterplattform (WFP) ermöglicht die Protokollierung von Paketverlusten und IKE/AuthIP-Fehlern.
ms.assetid: 607b7664-6be4-4ae6-991b-58ac9175405a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1500be04837126e6907b663e4496c58c05380d313a1465b9c8db05b5ea39d832
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068910"
---
# <a name="logging-windows-filtering-platform"></a>Protokollierung (Windows Filterplattform)

Die Windows Filtering Platform (WFP) ermöglicht die Protokollierung von Paketverlusten und IKE/AuthIP-Fehlern.

Die protokollierten Ereignisse werden im [**aufzählten FWPM \_ NET \_ EVENT \_ TYPE-Typ**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_net_event_type) definiert und lauten wie folgt.

-   IKE/AuthIP-Hauptmodusfehler.
-   IKE/AuthIP-Schnellmodusfehler.
-   Fehler im erweiterten AuthIP-Modus.
-   Während der Klassifizierung verworfene Pakete.
-   Von IPsec verworfene Pakete.

Standardmäßig ist die Protokollierung für WFP für eingehende Unicastpakete und für alle ausgehenden Pakete (Unicast, Multicast und Broadcast) aktiviert. Die Protokollierung kann für die restlichen Pakete aktiviert oder für alle Pakete über die [**FwpmEngineSetOptions0-Verwaltungsfunktion**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0) deaktiviert werden. Ereigniseinstellungen bleiben bei Neustarts erhalten.

Protokollierte Ereignisse werden in einem zirkulären Protokoll gespeichert. Neue Ereignisse überschreiben alte Ereignisse, [](fwp-mgmt-functions.md) wenn das Protokoll seine maximale Größe erreicht, und können mithilfe der von WFP bereitgestellten Ereignisverwaltungsfunktionen analysiert werden. Das Ereignisprotokoll hat eine maximale Größe von 128 KB und kann etwa 100 bis 150 Ereignisse halten.

Enumerationsfunktionen im Allgemeinen und [**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0) / [**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1) im Besonderen erstellen eine Momentaufnahme des Protokolls zu dem Zeitpunkt, zu dem das Enumerationshand handle erstellt wird. Nachfolgende Aufrufe, die das gleiche Enumerationshand handle verwenden, geben die nächste Gruppe von Elementen zurück, die auf die elemente im letzten Ausgabepuffer folgen.

Wenn eine Anwendung die WFP-Protokollierung deaktiviert (durch Aufrufen [**von FwpmEngineSetOptions0),**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0)sind alle Anwendungen betroffen. Das Ereignisprotokoll wird erst bereinigt, wenn eine Anwendung die WFP-Protokollierung erneut aktiviert, aber das Ereignisprotokoll kann vorher nicht abgefragt werden.

Das WFP-Ereignisprotokoll wird nach einem Neustart geleert.

 

 




