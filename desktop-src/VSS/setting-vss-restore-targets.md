---
description: Die IVssComponent-Schnittstelle ermöglicht es einem Writer, genau zu optimieren, wie Dateien komponentenweise wiederhergestellt werden.
ms.assetid: 362c6f44-ca67-4043-8d2c-4e46b5c8edd3
title: Festlegen von VSS-Wiederherstellungszielen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76f9378fe8175970a8ccacb196414f3afafbcd583ad74f9aca438a3e9b6cf6d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119394190"
---
# <a name="setting-vss-restore-targets"></a>Festlegen von VSS-Wiederherstellungszielen

Die [**IVssComponent-Schnittstelle**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) ermöglicht es einem Writer, genau zu optimieren, wie Dateien komponentenweise wiederhergestellt werden.

Da es möglich ist, dass die Systemkonfiguration während der Wiederherstellung etwas anderes ist als bei der Sicherung erwartet, wird der Wiederherstellungszielmechanismus bereitgestellt.

Er ermöglicht Es Writern, [**IVssComponent::SetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget) aufzurufen, um zu ändern, wie die Komponenten, die explizit im Sicherungskomponentendokument [*enthalten*](vssgloss-e.md) sind, wiederhergestellt werden. Dadurch wird auch der Wiederherstellungsmechanismus geändert, der für die Komponenten verwendet wird, die [*implizit enthalten*](vssgloss-i.md)sind.

Die Dateiwiederherstellung, die während eines Systemneustarts erfolgt (unter den [**VSS \_ \_ RESTOREMETHOD-Enumerationswerten**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) VSS \_ RME \_ RESTORE AT REBOOT \_ und \_ VSS \_ RME RESTORE AT REBOOT \_ IF CANNOT \_ \_ \_ \_ \_ REPLACE), kann von Wiederherstellungszielen nicht beeinflusst werden, da keine ausgeführten VSS-Dienste vorhanden sind, wenn **MoveFileEx** Dateien an ihren endgültigen Speicherort kopiert.

Auf ähnliche Weise können VSS \_ RME \_ CUSTOM-Wiederherstellungen beeinträchtigt werden, da jede benutzerdefinierte Wiederherstellung spezifisch für einen bestimmten Writer ist und wiederherstellungsziele berücksichtigt oder ignoriert werden kann.

Anforderer und Writer können [**IVssComponent::GetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget) verwenden, um das Wiederherstellungsziel eines Komponentensatzes zu überprüfen.

[**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) unterstützt die folgenden Wiederherstellungsziele, die auf Komponentensatzbasis festgelegt werden können:

-   VSS \_ RT \_ ORIGINAL. Die von der [**VSS \_ \_ RESTOREMETHOD-ENUM-Enumeration**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) angegebene Wiederherstellungsmethode wird berücksichtigt.
-   VSS \_ RT \_ ALTERNATE. Die Dateien werden an einem Speicherort wiederhergestellt, der von einer vorhandenen alternativen Speicherortzuordnung bestimmt wird. Wenn eine alternative Speicherortzuordnung vorhanden ist, die einem Pfad in einer Komponentensatzunterkomponente entspricht, stellen Sie nach Möglichkeit am alternativen Speicherort wieder her. Andernfalls wird ein Fehler zurückgegeben.

 

 



