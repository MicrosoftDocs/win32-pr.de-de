---
description: Die Auswahlbarkeit für die Wiederherstellung ermöglicht dem Anfordernden zu bestimmen, wann eine Komponente einzeln wiederhergestellt werden kann.
ms.assetid: 684dc50f-5d7b-4c95-85dd-77c320d65fff
title: Arbeiten mit Auswahlbarkeit für Wiederherstellungs- und Unterkomponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1186c9517af8e7e7b914b9508e10a2b4c8d1961afdbf6d68c2dadcede58c4c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117937381"
---
# <a name="working-with-selectability-for-restore-and-subcomponents"></a>Arbeiten mit Auswahlbarkeit für Wiederherstellungs- und Unterkomponenten

Die Auswahlbarkeit für die Wiederherstellung ermöglicht dem Anfordernden zu bestimmen, wann eine Komponente einzeln wiederhergestellt werden kann. Eine Komponente, die für die Sicherung eingeschlossen wurde, kann auf zwei Arten angezeigt werden:

-   Möglicherweise wurde eine Komponente explizit in [*die*](vssgloss-e.md) Sicherung eingeschlossen. Diese Komponenten verfügen über eine entsprechende [**IVssComponent-Instanz**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) im Dokument Sicherungskomponenten. Diese Komponenten sind in einer Wiederherstellung mithilfe von [**IVssBackupComponents::SetSelectedForRestore enthalten.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore)
-   Eine Komponente wurde möglicherweise implizit in [*die*](vssgloss-i.md) Sicherung eingeschlossen. Diese Komponenten verfügen nicht über eine entsprechende [**IVssComponent-Instanz**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) im Dokument Sicherungskomponenten. Es wird jedoch immer eine **IVssComponent-Instanz** für eine Vorgängerkomponente im Dokument geben. Diese Komponenten sind in einer Wiederherstellung mithilfe von [**IVssBackupComponents::AddRestoreSubcomponent enthalten.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent)

Jede Komponente, die explizit in die Sicherung eingeschlossen wurde, kann immer einzeln für die Wiederherstellung ausgewählt werden, unabhängig von ihrem Auswählbarkeitswert für die Wiederherstellung. Die Anfordernde ruft [**IVssBackupComponents::SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore)auf und übergibt die Writer-ID, den logischen Pfad und den Namen der jeweiligen Komponente. Komponenten, die implizit in die Sicherung eingeschlossen wurden, werden wiederhergestellt, wenn ein explizit eingeschlossener Vorgänger wiederhergestellt wird. Implizit eingeschlossene Komponenten können nur dann einzeln für die Wiederherstellung ausgewählt werden, wenn sie als für die Wiederherstellung auswählbar markiert sind. Die anfordernde Seite ruft zuerst **IVssBackupComponents::SetSelectedForRestore** für die nächstgelegene explizit eingeschlossene Vorgängerkomponente auf und ruft dann [**IVssBackupComponents::AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent) für die Vorgängerkomponente auf, um die implizit eingeschlossene Komponente für die Wiederherstellung auszuwählen. Danach wird nur die implizit ausgewählte Komponente wiederhergestellt. alle anderen Komponenten im Komponentensatz werden nicht wiederhergestellt.

Im Gegensatz zur Auswahl für die Sicherung, die immer explizit festgelegt werden muss, wenn eine Komponente mit [**IVssCreateWriterMetadata::AddComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent)hinzugefügt wird, hat die Auswählbarkeit für die Wiederherstellung den Standardwert false, der überschrieben werden kann.

Da Komponenten der obersten Ebene (Komponenten mit einem leeren logischen Pfad) nur explizit in eine Sicherung eingeschlossen werden können, hat die Auswahl der Wiederherstellung für diese Komponenten keine Bedeutung.

 

 



