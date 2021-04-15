---
description: In der folgenden Tabelle werden die vier Komponenten Typen beschrieben, die an einem Sicherungs Vorgang beteiligt sein können.
ms.assetid: d94e015b-6735-4a88-9d24-b73f0b5f6542
title: Arbeiten mit selekabilität für die Sicherung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4bd20bd0c9139f8ed1c9f56cc8f499f1b6aaf14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485011"
---
# <a name="working-with-selectability-for-backup"></a>Arbeiten mit selekabilität für die Sicherung

In der folgenden Tabelle werden die vier Komponenten Typen beschrieben, die an einem Sicherungs Vorgang beteiligt sein können.



| Komponententyp                                                                                                                                                                                                               | BESCHREIBUNG                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span id="Nonselectable-for-backup_components"></span><span id="nonselectable-for-backup_components"></span><span id="NONSELECTABLE-FOR-BACKUP_COMPONENTS"></span>Nicht auswählbare-for-Backup-Komponenten<br/>             | In ihren logischen Pfaden sind keine auswählbaren Vorgänger vorhanden.<br/>                              |
| <span id="Selectable-for-backup_components"></span><span id="selectable-for-backup_components"></span><span id="SELECTABLE-FOR-BACKUP_COMPONENTS"></span>Auswählbare Sicherungs Komponenten<br/>                         | In ihren logischen Pfaden sind keine auswählbaren Vorgänger vorhanden.<br/>                              |
| <span id="Nonselectable-for-backup_subcomponents"></span><span id="nonselectable-for-backup_subcomponents"></span><span id="NONSELECTABLE-FOR-BACKUP_SUBCOMPONENTS"></span>Nicht auswählbare unter Komponenten für die Sicherung<br/> | Nicht auswählbare-for-Backup-Komponenten mit auswählbaren Vorgängerversionen in Ihrem Pfad.<br/> |
| <span id="Selectable-for-backup_subcomponents"></span><span id="selectable-for-backup_subcomponents"></span><span id="SELECTABLE-FOR-BACKUP_SUBCOMPONENTS"></span>Auswählbare for-Backup-unter Komponenten<br/>             | Wählbare-for-Backup-Komponenten mit auswählbaren als Sicherungs Elementen in Ihrem Pfad.<br/>    |



 

Außerdem wird für jede auswählbare Komponente – unabhängig davon, ob Sie über auswählbare/Sicherungs-Vorgänger oder nicht – verfügt, ein [*Komponenten Satz*](vssgloss-c.md) definiert, wenn Sie von anderen Komponenten als Vorgänger in ihren logischen Pfaden vorhanden sind.

Die Regeln für die Auswahl von Komponenten für die Sicherung können wie folgt zusammengefasst werden:

-   Wenn eine Komponente ohne einen auswählbaren Vorgänger in ihrem logischen Pfad – ob die Komponente auswählbar ist, für die Sicherung oder nicht auswählbar – in einer Sicherung enthalten ist, muss Sie [*explizit eingeschlossen*](vssgloss-e.md)werden. Dies bedeutet, dass Metadaten für diese Komponenten dem Dokument mit den Sicherungs Komponenten hinzugefügt werden.

    Anforderer fügen diese Komponenten explizit mithilfe der [**IVssBackupComponents:: addComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) -Methode hinzu.

-   Nicht auswählbare unter Komponenten für Sicherungen sind immer [*implizit*](vssgloss-i.md) in die Sicherung eingeschlossen. Dies bedeutet, dass die Metadaten für diese Komponenten nicht Teil des Dokuments mit den Sicherungs Komponenten sind.
-   Auswählbare unter Komponenten für Sicherungen werden implizit eingeschlossen, wenn dieser Vorgänger explizit in der Sicherung enthalten ist. In diesem Fall werden Metadaten für diese Komponenten nicht zum Dokument mit den Sicherungs Komponenten hinzugefügt. Wenn eine implizit auswählbare für Backup-Unterkomponente einen Komponenten Satz definiert, werden die Elemente dieses Komponenten Satzes ebenfalls implizit ausgewählt.
-   Auswählbare-for-Backup-unter Komponenten, deren Vorgänger für die Sicherung nicht explizit in der Sicherung enthalten sind, können nach wie vor explizit von der anfordernden Person mithilfe der [**IVssBackupComponents:: addComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) -Methode eingeschlossen werden. Die Metadaten für die Komponente werden dann dem Dokument mit den Sicherungs Komponenten hinzugefügt. Wenn außerdem eine auswählbare untergeordnete Komponente einen Komponenten Satz definiert, werden die Mitglieder dieser Komponente implizit in die Sicherung eingeschlossen.

Der Fall "myWriter", der in [logischen Komponenten von Komponenten](logical-pathing-of-components.md) erläutert wird, kann als Beispiel verwendet werden, um die Auswahlmöglichkeiten für die Sicherung zu veranschaulichen.



| Komponentenname | Logischer Pfad            | Für Sicherung auswählbar |
|----------------|-------------------------|-----------------------|
| Ausführbare Dateien  | ""                      | N                     |
| "Configfiles"  | Ausführbare Dateien           | N                     |
| "Licenseingefo"  | ""                      | J                     |
| "Security"     | ""                      | J                     |
| UserInfo     | "Security"              | N                     |
| Abschluss | "Security"              | N                     |
| "beschreibdaten"   | ""                      | J                     |
| Set1         | "beschreibdaten"            | N                     |
| Jan          | "Schreibdaten \\ set1"      | N                     |
| 31.12.2012          | "Schreibdaten \\ set1"      | N                     |
| Set2         | "beschreibdaten"            | N                     |
| Jan          | "Schreibdaten \\ set2"      | N                     |
| 31.12.2012          | "Schreibdaten \\ set2"      | N                     |
| Such        | "Write Data \\ querylogs" | N                     |
| Ungs        | "beschreibdaten"            | J                     |
| Jan          | "Verwendung von" Schreib Daten \\ "     | N                     |
| 31.12.2012          | "Verwendung von" Schreib Daten \\ "     | N                     |



 

Jedes Mal, wenn "myWriter" gesichert ist, wird die Komponente "configfiles" durch explizites einschließen der "Executables"-Komponente mithilfe der [**IVssBackupComponents:: addComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) -Methode implizit eingeschlossen.

Die Komponente "LicenseInfo" ist eine eigenständige auswählbare Komponente für die Sicherung. Sie kann mithilfe der [**IVssBackupComponents:: addComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) -Methode nach dem Ermessen der anfordernden Person ausgewählt werden, aber bei Ihrer Auswahl werden keine weiteren Komponenten ausgewählt.

Die auswählbare-for-Backup-Komponente "Sicherheit" definiert einen einfachen Komponenten Satz mit zwei nicht auswählbaren unter Komponenten für die Sicherung, "UserInfo" und "Zertifikate". Wenn "Security" explizit für die Sicherung eingeschlossen wird, werden "UserInfo" und "Zertifikate" immer implizit eingeschlossen. Es gibt keine Möglichkeit, die unter Komponenten "UserInfo" oder "Zertifikate" in einen Sicherungs Vorgang aufzunehmen, es sei denn, "Security" ist enthalten.

Wenn die Komponente "Schreib Daten" ausgewählt ist, werden die nicht auswählbaren Komponenten "set1", "set2" und "Query" und die auswählbare Komponente "Verwendung" implizit ausgewählt. Jede dieser Komponenten verfügt über unter Komponenten, die implizit für die Sicherung ausgewählt werden. Keine ihrer Metadaten wird dem Dokument mit den Sicherungs Komponenten hinzugefügt.

Wenn die Komponente "Schreib Daten" nicht ausgewählt ist, sind die nicht auswählbaren Komponenten "set1", "set2" und "Query" nicht für die Sicherung enthalten.

Allerdings können anfordernde Personen explizit die auswählbare für die Sicherungs Komponente "Usage" einschließen. Metadaten für diese Komponente werden dem Dokument mit den Sicherungs Komponenten hinzugefügt. "Usage"-unter Komponenten "Jan" und "Dec" werden der Sicherung implizit hinzugefügt, werden jedoch nicht zum Sicherungs Komponenten Dokument hinzugefügt.

Wenn Sie explizit eine Komponente für die Sicherung einschließen, wird im Dokument mit den Sicherungs Komponenten eine entsprechende [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) -Instanz erstellt.

Ein Anforderer Ruft Informationen zu explizit enthaltenen Komponenten aus seinem Sicherungs Komponenten Dokument ab, indem er diese Writer (mithilfe von [**IVssBackupComponents:: getwritercomponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents)) untersucht, die in seinem Dokument enthalten sind, und die gespeicherten [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) -Objekte abruft.

Da weder die Datei Satz Informationen (Datei Angabe, Pfad und Rekursions Kennzeichen) der im Sicherungs Komponenten Dokument vorhandenen Komponenten noch Informationen zu implizit hinzugefügten Komponenten vorhanden sind, müssen anfordernde Personen Writer-Metadatendokumente Abfragen, um vollständige Informationen zu allen Komponenten zu erhalten, die im Dokument mit den Sicherungs Komponenten enthalten sind.

 

 




