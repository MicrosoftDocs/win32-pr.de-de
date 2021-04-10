---
description: Die Writer-Teilnahme an einer VSS-Sicherung ist so konzipiert, dass Anwendungen steuern können, was und wie Ihre Wiederherstellungsdaten verwendet werden sollen.
ms.assetid: 076b2e6f-c2ca-4129-8827-1b18a655d634
title: Wiederherstellungen ohne Writer-Beteiligung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f89fd5ea855d2d91701d351e860bf966148be587
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131264"
---
# <a name="restores-without-writer-participation"></a>Wiederherstellungen ohne Writer-Beteiligung

Die Writer-Teilnahme an einer VSS-Sicherung ist so konzipiert, dass Anwendungen steuern können, was und wie Ihre Wiederherstellungsdaten verwendet werden sollen.

Wenn ein Writer auf einem System verfügbar ist, empfiehlt es sich im Allgemeinen nicht, Daten an Ihrem ursprünglichen Speicherort ohne Writer-Beteiligung wiederherzustellen. Bei einer solchen Wiederherstellung werden wahrscheinlich gesperrte Zieldateien angezeigt, und es besteht ein erhebliches Risiko, dass Daten beschädigt werden.

Es gibt jedoch Gründe, warum eine Sicherungs Anwendung möglicherweise eine VSS-Sicherung ohne Writer-Beteiligung wiederherstellen will oder benötigt:

-   Daten werden von VSS-abhängigen Anwendungen verwaltet. Fast jedes System verfügt über einige Anwendungen – Texteditoren, e-Mail-Reader, Word-Prozessoren usw. –, die VSS nicht kennen. Diese Daten können nicht mithilfe der Writer-Teilnahme wieder hergestellt werden.

    Im Allgemeinen ist diese Art von Daten nicht System-oder Dienst kritisch, und die Wiederherstellung sollte nicht problematisch oder zumindest bei einer herkömmlichen Wiederherstellung nicht problematisch sein.

    Wie bei der Vorbereitung für konventionelle Wiederherstellungen sollten Wiederherstellungs Operatoren nach Möglichkeit versuchen, solche Anwendungen anzuhalten oder zu beenden, bevor eine VSS-Wiederherstellung gestartet wird.

-   Fehlende VSS-Writer. Diese Situation kann relativ häufig vorkommen, wenn der Zustand eines beschädigten Systems wieder hergestellt wird. Ein Sicherungs Vorgang muss bestimmen, ob es wünschenswert ist, Dateien für fehlende Writer wiederherzustellen. Wenn die Wiederherstellung wünschenswert ist, können die Dateien genau wie bei einer herkömmlichen Sicherung wieder hergestellt werden.
-   Eine private Wiederherstellung der Daten eines Writers. Ein Anforderer kann sich entscheiden, die Daten eines laufenden Writers an einem privaten Speicherort wiederherzustellen, ohne den Writer zu benachrichtigen. Ein Beispiel hierfür ist die Wiederherstellung der Writer-Daten zur Unterstützung des Offline Vergleichs. In dieser Situation möchte ein Anforderer nicht den [*neuen Zielort*](vssgloss-n.md) bei der Wiederherstellung verwenden, da er nicht möchte, dass der Writer auf die Daten zugreift.
-   Ein Writer möchte bei der Wiederherstellung nicht einbezogen werden. Ein Writer zeigt dies an, indem er VSS \_ WRE \_ Never für den " *Write Restore* "-Parameter von [**ivsskreateschreitermetadata:: "-trestoremethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod)" übergibt.
-   Ein Writer erfordert eine benutzerdefinierte Wiederherstellungsmethode. Ein Writer gibt an, dass er eine benutzerdefinierte Wiederherstellung erfordert, indem er VSS \_ RME \_ Custom für den *Methoden* Parameter von [**ivsskreateschreitermetadata:: abtrestoremethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod)übergibt. In diesem Fall sollte dieser Writer nicht an dem Wiederherstellungs Vorgang beteiligt sein, es sei denn, die Dokumentation zur benutzerdefinierten Wiederherstellung für diesen Writer zeigt andernfalls an.

Ein Anforderer bezieht einen Writer in den Wiederherstellungsprozess ein, indem er eine dieser Writer-Komponenten in einem Aufrufen von [**IVssBackupComponents:: setselectedforrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore)angibt. Die Daten eines Writers können wieder hergestellt werden, ohne dass Sie den Writer einbeziehen, indem Sie einfach keine der Komponenten dieses Writers in einem Aufrufen von **IVssBackupComponents:: setselectedforrestore** angeben. Wenn ein Writer keine Wiederherstellungs Ereignisse erwartet, kann dies dazu führen, dass für diesen Writer falsche Fehler gemeldet werden.

 

 



