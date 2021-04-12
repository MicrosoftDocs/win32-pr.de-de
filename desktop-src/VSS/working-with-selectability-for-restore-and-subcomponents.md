---
description: Die selekabilität für Restore ermöglicht es dem Anforderer zu bestimmen, wann eine Komponente einzeln wieder hergestellt werden kann.
ms.assetid: 684dc50f-5d7b-4c95-85dd-77c320d65fff
title: Arbeiten mit selekabilität für die Wiederherstellung und unter Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d988f4c4e029c7dd8623ad22fcaee7662d33e82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526261"
---
# <a name="working-with-selectability-for-restore-and-subcomponents"></a>Arbeiten mit selekabilität für die Wiederherstellung und unter Komponenten

Die selekabilität für Restore ermöglicht es dem Anforderer zu bestimmen, wann eine Komponente einzeln wieder hergestellt werden kann. Eine Komponente, die für die Sicherung enthalten ist, kann auf zwei Arten angezeigt werden:

-   Möglicherweise wurde eine Komponente [*explizit*](vssgloss-e.md) in die Sicherung eingeschlossen. Diese Komponenten verfügen über eine entsprechende [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) -Instanz im Sicherungs Komponenten Dokument. Diese Komponenten sind in einer Wiederherstellung mithilfe von [**IVssBackupComponents:: setselectedforrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore)enthalten.
-   Möglicherweise wurde eine Komponente [*implizit*](vssgloss-i.md) in die Sicherung eingeschlossen. Diese Komponenten verfügen im Dokument mit den Sicherungs Komponenten nicht über eine entsprechende [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) -Instanz. Es ist jedoch immer eine **IVssComponent** -Instanz für eine Vorgänger Komponente im Dokument vorhanden. Diese Komponenten sind in einer Wiederherstellung mithilfe von [**IVssBackupComponents:: adressstoresubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent)enthalten.

Jede Komponente, die explizit in der Sicherung enthalten ist, kann für die Wiederherstellung einzeln ausgewählt werden, unabhängig davon, ob Sie den Wert für die selekmentwiederherstellung auswählen. Der Anforderer ruft [**IVssBackupComponents:: setselectedforrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore)auf und übergibt die Writer-ID, den logischen Pfad und den Namen der jeweiligen Komponente. Komponenten, die implizit in die Sicherung eingeschlossen wurden, werden wieder hergestellt, wenn ein explizit enthaltener Vorgänger wieder hergestellt wird. Implizit enthaltene Komponenten können nur für die Wiederherstellung einzeln ausgewählt werden, wenn Sie für die Wiederherstellung als auswählbar markiert sind. Der Anforderer ruft zunächst **IVssBackupComponents:: setselectedforrestore** für die nächstgelegene explizit enthaltene Vorgänger Komponente auf und ruft dann [**IVssBackupComponents:: adressstoresubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent) auf der Vorgänger Komponente auf, um die implizit enthaltene Komponente für die Wiederherstellung auszuwählen. Nachdem dies abgeschlossen ist, wird nur die implizit ausgewählte Komponente wieder hergestellt. alle anderen Komponenten im Komponenten Satz werden nicht wieder hergestellt.

Anders als bei der Auswahl der Sicherungsfunktion für die Sicherung, die immer explizit festgelegt werden muss, wenn eine Komponente mit [**ivsskreateschreitermetadata:: addComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent)hinzugefügt wird, hat die Auswahlfunktion für Restore den Standardwert false, der überschrieben werden kann.

Da Komponenten der obersten Ebene (Komponenten mit einem leeren logischen Pfad) nur explizit in eine Sicherung eingeschlossen werden können, hat die Auswahl für die Wiederherstellung keine Bedeutung für diese Komponenten.

 

 



