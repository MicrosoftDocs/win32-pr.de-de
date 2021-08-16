---
description: Die Teilnahme eines Writers an einem Sicherungs- oder Wiederherstellungsvorgang und die gespeicherten Daten hängen davon ab, welche seiner Komponenten explizit als Teil des Sicherungskomponentendokuments eines Anfordernden enthalten sind und welche Beziehung zwischen diesen Komponenten und dem logischen Pfad anderer Komponenten im Writer Metadata Document besteht.
ms.assetid: e8920cca-d944-437f-bf6a-7ce8d518746a
title: Arbeiten mit Selektivität und logischen Pfaden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f008b086ea50a1695a76f8b7beecab473b767fb1e2835fd5686197bb1b583175
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118344253"
---
# <a name="working-with-selectability-and-logical-paths"></a>Arbeiten mit Selektivität und logischen Pfaden

Die Teilnahme eines Writers an einem Sicherungs- oder Wiederherstellungsvorgang und die gespeicherten Daten hängen davon ab, welche seiner Komponenten explizit als Teil des Sicherungskomponentendokuments eines Anfordernden [*enthalten*](vssgloss-e.md) sind und welche Beziehung zwischen diesen Komponenten und dem logischen Pfad anderer Komponenten im Writer Metadata Document besteht.

Writer ohne Komponenten, die dem Sicherungskomponentendokument eines Anforderers vor der Generierung eines [*PrepareForBackup-Ereignisses*](vssgloss-p.md) (bei Sicherungsvorgängen) oder eines [**PreRestore-Ereignisses**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) (bei Wiederherstellungsvorgängen) hinzugefügt wurden, empfangen nach diesem Punkt keine Ereignisse und nehmen nicht am Sicherungs- oder Wiederherstellungsvorgang teil.

Die Möglichkeit eines Anforderers, eine bestimmte Komponente in eine Sicherung oder Wiederherstellung einzuschließen oder auszuschließen, wird jedoch wie folgt gesteuert:

-   Alle Hierarchien zwischen den Komponenten, die von einem Writer verwaltet und durch [ *logische Pfade* ausgedrückt werden](vssgloss-l.md)
-   Gibt an, ob die Komponente als für die [ *Sicherung auswählbar* festgelegt ist.](vssgloss-s.md)
-   Gibt an, ob sie als für die [ *Wiederherstellung auswählbar* festgelegt ist.](vssgloss-s.md)
-   Gibt an, ob eine explizite Abhängigkeit zwischen einer bestimmten Komponente in einem bestimmten Writer und anderen Komponenten in anderen Writern vorhanden ist.

Weitere Informationen zu diesen Problemen sind in den folgenden Themen enthalten:

-   [Logisches Pfading von Komponenten](logical-pathing-of-components.md)
-   [Arbeiten mit Der Auswählbarkeit für die Sicherung](working-with-selectability-for-backup.md)
-   [Arbeiten mit Auswahlfähigkeit für Wiederherstellungs- und Unterkomponenten](working-with-selectability-for-restore-and-subcomponents.md)
-   [Auswählbarkeit und Arbeiten mit Komponenteneigenschaften](selectability-and-working-with-component-properties.md)
-   [Abhängigkeiten zwischen Komponenten, die von verschiedenen Writern verwaltet werden](dependencies-between-components-managed-by-different-writers.md)

 

 



