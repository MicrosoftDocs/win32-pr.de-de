---
description: Die Teilnahme eines Writers an einem Sicherungs-oder Wiederherstellungs Vorgang und der Daten, die gespeichert werden, hängt davon ab, welche Komponenten explizit als Teil des Dokuments der Sicherungs Komponenten eines Anforderers und der Beziehung zwischen diesen Komponenten und dem logischen Pfad anderer Komponenten innerhalb des Writer-Metadatendokuments enthalten sind.
ms.assetid: e8920cca-d944-437f-bf6a-7ce8d518746a
title: Arbeiten mit selekabilität und logischen Pfaden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42bc29d629df86562bc9b764b1d83bb8bb511d50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360043"
---
# <a name="working-with-selectability-and-logical-paths"></a>Arbeiten mit selekabilität und logischen Pfaden

Die Teilnahme eines Writers an einem Sicherungs-oder Wiederherstellungs Vorgang und der Daten, die gespeichert werden, hängt davon ab, welche Komponenten [*explizit*](vssgloss-e.md) als Teil des Dokuments der Sicherungs Komponenten eines Anforderers und der Beziehung zwischen diesen Komponenten und dem logischen Pfad anderer Komponenten innerhalb des Writer-Metadatendokuments enthalten sind.

Writer ohne Komponenten, die vor der Generierung eines [*PrepareForBackup*](vssgloss-p.md) -Ereignisses (im Fall von Sicherungs Vorgängen) oder eines [**vorab**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) Ereignisses (bei Wiederherstellungs Vorgängen) zum Sicherungs Komponenten Dokument eines Anforderers hinzugefügt wurden, erhalten nach diesem Zeitpunkt keine Ereignisse und werden nicht an dem Sicherungs-oder Wiederherstellungs Vorgang beteiligt.

Die Freiheit eines Anforderers, eine bestimmte Komponente in eine Sicherung oder Wiederherstellung einzubeziehen oder auszuschließen, wird jedoch durch Folgendes gesteuert:

-   Jede Hierarchie, die zwischen den von einem Writer verwalteten Komponenten besteht und durch [ *logische Pfade* ausgedrückt wird](vssgloss-l.md)
-   Gibt an, ob die Komponente [ *für die Sicherung ausgewählt* werden soll.](vssgloss-s.md)
-   Gibt an, ob es [ *für die Wiederherstellung ausgewählt* ist.](vssgloss-s.md)
-   Gibt an, ob eine explizite Abhängigkeit zwischen einer bestimmten Komponente in einem bestimmten Writer und anderen Komponenten in anderen Writern vorhanden ist.

Weitere Informationen zu diesen Problemen finden Sie in den folgenden Themen:

-   [Logische Komponente von Komponenten](logical-pathing-of-components.md)
-   [Arbeiten mit selekabilität für die Sicherung](working-with-selectability-for-backup.md)
-   [Arbeiten mit selekabilität für die Wiederherstellung und unter Komponenten](working-with-selectability-for-restore-and-subcomponents.md)
-   [Selekabilität und arbeiten mit Komponenteneigenschaften](selectability-and-working-with-component-properties.md)
-   [Abhängigkeiten zwischen Komponenten, die von unterschiedlichen Writern verwaltet werden](dependencies-between-components-managed-by-different-writers.md)

 

 



