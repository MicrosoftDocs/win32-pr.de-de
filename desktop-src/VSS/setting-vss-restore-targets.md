---
description: Mithilfe der IVssComponent-Schnittstelle kann ein Writer genau anpassen, wie Dateien auf Komponentenbasis wieder hergestellt werden.
ms.assetid: 362c6f44-ca67-4043-8d2c-4e46b5c8edd3
title: Festlegen von VSS-Wiederherstellungs Zielen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e8815e552db518c447bd63b9f02ba9228850384
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368255"
---
# <a name="setting-vss-restore-targets"></a>Festlegen von VSS-Wiederherstellungs Zielen

Mithilfe der [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) -Schnittstelle kann ein Writer genau anpassen, wie Dateien auf Komponentenbasis wieder hergestellt werden.

Da es möglich ist, dass die Systemkonfiguration während der Wiederherstellung etwas anderes als das bei der Sicherung erwartete ist, wird der Wiederherstellungs Ziel Mechanismus bereitgestellt.

Sie ermöglicht es Writer, [**IVssComponent:: abtrestoretarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget) aufzurufen, um zu ändern, wie die Komponenten, die explizit im Sicherungs Komponenten Dokument [*enthalten*](vssgloss-e.md) sind, wieder hergestellt werden. Dadurch wird auch der Wiederherstellungs Mechanismus geändert, der für die [*implizit enthaltenen*](vssgloss-i.md)Komponenten verwendet wird.

Dateiwiederherstellung, die während eines Systemneustarts stattfindet (unter den Enumerationswerten der [**VSS \_ restoremethod \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) Enumeration VSS \_ RME \_ Restore \_ at \_ Reboot und VSS \_ RME \_ Restore \_ at \_ Reboot \_ \_ , wenn nicht \_ ersetzen), kann von Wiederherstellungs Zielen nicht beeinflusst werden, da die Dateien von " **muvefileex** " an den endgültigen Speicherort kopiert werden.

Ebenso kann die \_ benutzerdefinierte VSS RME \_ -Wiederherstellung beeinträchtigt werden, da jede benutzerdefinierte Wiederherstellung für einen bestimmten Writer spezifisch ist und Wiederherstellungs Ziele berücksichtigen oder ignorieren kann.

Anforderer und Writer können [**IVssComponent:: getrestoretarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget) verwenden, um das Wiederherstellungs Ziel eines Komponenten Satzes zu überprüfen.

[**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) unterstützt die folgenden Wiederherstellungs Ziele, die für eine Komponente festgelegt werden können, die auf Komponentenebene festgelegt ist:

-   VSS \_ RT- \_ Original. Die von der [**VSS \_ restoremethod \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) Enumeration festgelegte Wiederherstellungsmethode wird beachtet.
-   VSS \_ RT- \_ Alternative. Die Dateien werden an einem Speicherort wieder hergestellt, der aus einer vorhandenen alternativen Speicherort Zuordnung ermittelt wurde. Wenn eine Alternative Speicherort Zuordnung vorhanden ist, die einem Pfad in einer Komponenten Satz-Unterkomponente entspricht, stellen Sie nach Möglichkeit eine Wiederherstellung am alternativen Speicherort Andernfalls wird ein Fehler zurückgegeben.

 

 



