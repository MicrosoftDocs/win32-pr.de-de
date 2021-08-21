---
description: Die Teilnahme von Writern an einer VSS-Sicherung ist so konzipiert, dass Anwendungen steuern können, was und wie ihre Wiederherstellungsdaten verwendet werden sollen.
ms.assetid: 076b2e6f-c2ca-4129-8827-1b18a655d634
title: Wiederherstellungen ohne Writer-Beteiligung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 896cbe81a2c3487bb00b01379b6b5bbe4760ecbb28c1bf94c661eeb0049a3d37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056368"
---
# <a name="restores-without-writer-participation"></a>Wiederherstellungen ohne Writer-Beteiligung

Die Teilnahme von Writern an einer VSS-Sicherung ist so konzipiert, dass Anwendungen steuern können, was und wie ihre Wiederherstellungsdaten verwendet werden sollen.

Wenn ein Writer auf einem System verfügbar ist, ist es im Allgemeinen nie ratsam, Daten ohne Beteiligung des Writers an seinem ursprünglichen Speicherort wiederherzustellen. Eine solche Wiederherstellung würde wahrscheinlich auf gesperrte Zieldateien stoßen und ein erhebliches Risiko der Beschädigung von Daten darstellen.

Es gibt jedoch Gründe, warum eine Sicherungsanwendung eine VSS-Sicherung ohne Beteiligung des Writers wiederherstellen möchte oder muss:

-   Daten werden von VSS-freien Anwendungen verwaltet. Fast jedes System hat einige Anwendungen – Text-Editoren, E-Mail-Reader, Textprozessoren usw.–, die vss nicht kennen. Diese Daten können nicht mit writer-Beteiligung wiederhergestellt werden.

    Im Allgemeinen ist diese Art von Daten nicht system- oder dienstkritisch, und die Wiederherstellung sollte nicht problematisch oder zumindest nicht problematischer sein als bei einer herkömmlichen Wiederherstellung.

    Wie bei den Vorbereitungen für herkömmliche Wiederherstellungen sollten Wiederherstellungsoperatoren nach Möglichkeit versuchen, solche Anwendungen vor dem Starten einer VSS-Wiederherstellung anzuhalten oder zu beenden.

-   Fehlende VSS-Writer. Diese Situation kann bei der Wiederherstellung des Zustands eines beschädigten Systems recht häufig auftreten. Ein Sicherungsvorgang muss bestimmen, ob es wünschenswert ist, Dateien für fehlende Writer wiederherzustellen. Wenn eine Wiederherstellung wünschenswert ist, können die Dateien genauso wie eine herkömmliche Sicherung wiederhergestellt werden.
-   Eine private Wiederherstellung der Daten eines Writers. Ein Anforderer kann die Daten eines ausgeführten Writers an einem privaten Speicherort wiederherstellen, ohne den Writer zu benachrichtigen. Ein Beispiel hierfür ist die Wiederherstellung der Daten des Writers zur Unterstützung des Offlinevergleichs. In einer solchen Situation möchte ein Anforderer den [*neuen Zielspeicherort*](vssgloss-n.md) während der Wiederherstellung nicht verwenden, da er nicht möchte, dass der Writer auf die Daten zugreift.
-   Ein Writer möchte nicht an der Wiederherstellung beteiligt sein. Ein Writer gibt dies an, indem VSS \_ WRE \_ NEVER für den *writerRestore-Parameter* von [**IVssCreateWriterMetadata::SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod)übergeben wird.
-   Ein Writer erfordert eine benutzerdefinierte Wiederherstellungsmethode. Ein Writer gibt an, dass eine benutzerdefinierte Wiederherstellung erforderlich ist, indem VSS \_ RME \_ CUSTOM für den *Methodenparameter* von [**IVssCreateWriterMetadata::SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod)übergeben wird. In diesem Fall sollte dieser Writer nicht am Wiederherstellungsprozess beteiligt sein, es sei denn, in der Dokumentation zur benutzerdefinierten Wiederherstellung für diesen Writer ist dies anders angegeben.

Ein Anforderer bezieht einen Writer in den Wiederherstellungsprozess ein, indem er eine der Komponenten dieses Writers in einem Aufruf von [**IVssBackupComponents::SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore)angibt. Die Daten eines Writers können ohne Einbeziehung des Writers wiederhergestellt werden, indem einfach keine der Komponenten dieses Writers in einem Aufruf von **IVssBackupComponents::SetSelectedForRestore** angegeben wird. Wenn ein Writer keine Wiederherstellungsereignisse erwartet, kann die Einbeziehung dieses Writers in den Wiederherstellungsprozess dazu führen, dass falsche Fehler für diesen Writer gemeldet werden.

 

 



