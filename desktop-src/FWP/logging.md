---
title: Protokollierung (Windows-Filter Plattform)
description: Die Windows-Filter Plattform (WFP) ermöglicht das Protokollieren von Paket Ablage-und IKE/AuthIP-Fehlern.
ms.assetid: 607b7664-6be4-4ae6-991b-58ac9175405a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a27868c76a643a8e1b7b478152c100a2026bfc20
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106337481"
---
# <a name="logging-windows-filtering-platform"></a>Protokollierung (Windows-Filter Plattform)

Die Windows-Filter Plattform (Windows Filtering Platform, WFP) ermöglicht das Protokollieren von Paket Ablage-und IKE/AuthIP-Fehlern

Die protokollierten Ereignisse werden im enumerierten Typ des Typs "Typ des Typs [**" vom Typ \_ \_ \_**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_net_event_type) "Typ" definiert und lauten wie folgt.

-   IKE/AuthIP-hauptmodusfehler.
-   IKE/AuthIP-Schnellmodus Fehler.
-   AuthIP-Fehler im erweiterten Modus.
-   Während der Klassifizierung gelöschte Pakete.
-   Von IPSec gelöschte Pakete.

Standardmäßig ist die Protokollierung für WFP für eingehende Unicastpakete und für alle ausgehenden Pakete (Unicast, Multicast und Broadcast) aktiviert. Mithilfe der [**FwpmEngineSetOptions0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0) -Verwaltungsfunktion kann die Protokollierung für den Rest der Pakete aktiviert oder für alle Pakete deaktiviert werden. Ereignis Einstellungen bleiben bei Neustarts erhalten.

Protokollierte Ereignisse werden in einem Zirkel Protokoll gespeichert, d. h. neue Ereignisse überschreiben alte, wenn das Protokoll die maximale Größe erreicht, und können mithilfe der von WFP bereitgestellten [Ereignis Verwaltungs](fwp-mgmt-functions.md) Funktionen analysiert werden. Das Ereignisprotokoll hat eine maximale Größe von 128 KB und kann ungefähr 100 bis 150 Ereignisse enthalten.

Im Allgemeinen werden Enumerationsfunktionen und [**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0) / [**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1) insbesondere zum Zeitpunkt der Erstellung des enumerationshandles eine Momentaufnahme des Protokolls erstellt. Nachfolgende Aufrufe, die denselben enumerationshandle verwenden, geben den nächsten Satz von Elementen zurück, die dem letzten Ausgabepuffer folgen.

Wenn eine Anwendung die WFP-Protokollierung deaktiviert (durch Aufrufen von [**FwpmEngineSetOptions0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0)), sind alle Anwendungen betroffen. Das Ereignisprotokoll wird erst bereinigt, wenn eine Anwendung die WFP-Protokollierung erneut aktiviert, das Ereignisprotokoll aber vorher nicht abgefragt werden kann.

Das WFP-Ereignisprotokoll wird nach einem Neustart geleert.

 

 




