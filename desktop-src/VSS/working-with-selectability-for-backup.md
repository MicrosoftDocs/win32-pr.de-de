---
description: In der folgenden Tabelle werden die vier Komponententypen beschrieben, die an einem Sicherungsvorgang beteiligt sein können.
ms.assetid: d94e015b-6735-4a88-9d24-b73f0b5f6542
title: Arbeiten mit Der Auswählbarkeit für die Sicherung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82081bb9cef51572afc2a8b5c08cf845ee22736dd8fdc20edf60fa0082ce8c9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118842314"
---
# <a name="working-with-selectability-for-backup"></a>Arbeiten mit Der Auswählbarkeit für die Sicherung

In der folgenden Tabelle werden die vier Komponententypen beschrieben, die an einem Sicherungsvorgang beteiligt sein können.



| Komponententyp                                                                                                                                                                                                               | BESCHREIBUNG                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span id="Nonselectable-for-backup_components"></span><span id="nonselectable-for-backup_components"></span><span id="NONSELECTABLE-FOR-BACKUP_COMPONENTS"></span>Nicht auswählbare Sicherungskomponenten<br/>             | Keine auswählbaren Für-Sicherung-Vorgänger in ihren logischen Pfaden.<br/>                              |
| <span id="Selectable-for-backup_components"></span><span id="selectable-for-backup_components"></span><span id="SELECTABLE-FOR-BACKUP_COMPONENTS"></span>Auswählbare Sicherungskomponenten<br/>                         | Keine auswählbaren Für-Sicherung-Vorgänger in ihren logischen Pfaden.<br/>                              |
| <span id="Nonselectable-for-backup_subcomponents"></span><span id="nonselectable-for-backup_subcomponents"></span><span id="NONSELECTABLE-FOR-BACKUP_SUBCOMPONENTS"></span>Nicht auswählbare Unterkomponenten für Sicherungen<br/> | Nicht auswählbare Sicherungskomponenten mit auswählbaren Vorgängern für Sicherungen in ihrem Pfad.<br/> |
| <span id="Selectable-for-backup_subcomponents"></span><span id="selectable-for-backup_subcomponents"></span><span id="SELECTABLE-FOR-BACKUP_SUBCOMPONENTS"></span>Auswählbare Unterkomponenten für Sicherungen<br/>             | Auswählbare Sicherungskomponenten mit auswählbaren Vorgängern für Sicherungen in ihrem Pfad.<br/>    |



 

Darüber hinaus definiert jede auswählbare Sicherungskomponente – unabhängig davon, ob sie über auswählbare Für-Sicherung-Vorgänger verfügt oder nicht – einen [*Komponentensatz,*](vssgloss-c.md) wenn andere Komponenten sie als Vorgänger in ihren logischen Pfaden haben.

Die Regeln für die Auswahl von Komponenten für die Sicherung können wie folgt zusammengefasst werden:

-   Wenn eine Komponente ohne einen auswählbaren Für-Sicherung-Vorgänger in ihrem logischen Pfad – unabhängig davon, ob die Komponente auswählbar für die Sicherung oder nicht selectable-for-backup ist – in einer Sicherung enthalten ist, muss sie [*explizit eingeschlossen*](vssgloss-e.md)werden. Dies bedeutet, dass Metadaten für diese Komponenten dem Sicherungskomponentendokument hinzugefügt werden.

    Anforderer fügen diese Komponenten explizit mithilfe der [**IVssBackupComponents::AddComponent-Methode**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) hinzu.

-   Nicht auswählbare Unterkomponenten für Sicherungen sind immer implizit in der Sicherung [*enthalten.*](vssgloss-i.md) Dies bedeutet, dass Metadaten für diese Komponenten nicht Teil des Sicherungskomponentendokuments sind.
-   Selectable-for-backup-Unterkomponenten werden implizit eingeschlossen, wenn dieser Vorgänger explizit in der Sicherung enthalten ist. In diesem Fall werden dem Sicherungskomponentendokument keine Metadaten für diese Komponenten hinzugefügt. Wenn eine implizit für die Sicherungsunterkomponente auswählbare einen Komponentensatz definiert, werden die Member dieses Komponentensatzes ebenfalls implizit ausgewählt.
-   Selectable-for-backup-Unterkomponenten, deren Vorgänger auswählbar für Sicherung nicht explizit in die Sicherung eingeschlossen ist, können vom Anfordernden weiterhin explizit mithilfe der [**IVssBackupComponents::AddComponent-Methode**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) eingeschlossen werden. Die Metadaten für die Komponente werden dann dem Sicherungskomponentendokument hinzugefügt. Wenn eine auswählbare Für-Sicherung-Unterkomponente einen Komponentensatz definiert, werden die Member dieses Komponentensatzes implizit in die Sicherung eingeschlossen.

Der fall "MyWriter", der unter [Logisches Pfading von Komponenten](logical-pathing-of-components.md) erläutert wird, kann als Beispiel verwendet werden, um die Auswählbarkeit für die Sicherung zu veranschaulichen.



| Komponentenname | Logischer Pfad            | Für die Sicherung auswählbar |
|----------------|-------------------------|-----------------------|
| "Ausführbare Dateien"  | ""                      | N                     |
| "ConfigFiles"  | "Ausführbare Dateien"           | N                     |
| "LicenseInfo"  | ""                      | J                     |
| "Security"     | ""                      | J                     |
| "UserInfo"     | "Security"              | N                     |
| "Zertifikate" | "Security"              | N                     |
| "writerData"   | ""                      | J                     |
| "Set1"         | "writerData"            | N                     |
| "Jan"          | "writerData \\ Set1"      | N                     |
| "Dec"          | "writerData \\ Set1"      | N                     |
| "Set2"         | "writerData"            | N                     |
| "Jan"          | "writerData \\ Set2"      | N                     |
| "Dec"          | "writerData \\ Set2"      | N                     |
| "Abfrage"        | "writerData \\ QueryLogs" | N                     |
| "Nutzung"        | "writerData"            | J                     |
| "Jan"          | "writerData \\ Usage"     | N                     |
| "Dec"          | "writerData \\ Usage"     | N                     |



 

Wenn "MyWriter" gesichert wird, schließt das explizite Einschließen der Komponente "Executables" mithilfe der [**IVssBackupComponents::AddComponent-Methode**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) implizit die Komponente "ConfigFiles" ein.

Die Komponente "LicenseInfo" ist eine eigenständige auswählbare Komponente für die Sicherung. Sie kann mithilfe der [**IVssBackupComponents::AddComponent-Methode**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) im Ermessen des Anfordernden ausgewählt werden, aber die Auswahl wählt keine anderen Komponenten aus.

Die komponente "Security" (Für Sicherung auswählbar) definiert einen einfachen Komponentensatz, der zwei nicht auswählbare Unterkomponenten für Sicherungen enthält: "UserInfo" und "Certificates". Wenn "Sicherheit" explizit für die Sicherung enthalten ist, sind "UserInfo" und "Certificates" immer ebenfalls implizit enthalten. Es gibt keine Möglichkeit, die Unterkomponenten "UserInfo" oder "Certificates" in einen Sicherungsvorgang einzubetten, es sei denn, "Sicherheit" ist enthalten.

Wenn die Komponente "writerData" ausgewählt ist, werden die nicht auswählbaren Sicherungskomponenten "Set1", "Set2" und "Query" sowie die auswählbare Für-Sicherung-Komponente "Usage" implizit ausgewählt. Jede dieser Komponenten verfügt über Unterkomponenten, die implizit für die Sicherung ausgewählt werden. Dem Sicherungskomponentendokument werden keine metadaten hinzugefügt.

Wenn die Komponente "writerData" nicht ausgewählt ist, sind die nicht auswählbaren Sicherungskomponenten "Set1", "Set2" und "Query" nicht für die Sicherung enthalten.

Anforderer können jedoch die für die Sicherungskomponente "Verwendung" auswählbare explizit einschließen. Metadaten für diese Komponente werden dem Dokument sicherungskomponenten hinzugefügt. Die Unterkomponenten "Jan" und "Dec" von "Usage" werden der Sicherung implizit hinzugefügt, aber ihre Informationen werden dem Sicherungskomponentendokument nicht hinzugefügt.

Durch das explizite Einschließen einer Komponente für die Sicherung wird eine entsprechende [**IVssComponent-Instanz**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) im Sicherungskomponentendokument erstellt.

Ein Anforderer ruft Informationen zu explizit eingeschlossenen Komponenten aus seinem Sicherungskomponentendokument ab, indem er diese Writer untersucht (mit [**IVssBackupComponents::GetWriterComponents),**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents)die in seinem Dokument enthalten sind, und die [**gespeicherten IVssComponent-Objekte abruft.**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)

Da weder die Dateisatzinformationen (Dateispezifikation, Pfad und Rekursionsflag) der im Sicherungskomponentendokument vorhandenen Komponenten noch Informationen zu implizit hinzugefügten Komponenten vorhanden sind, müssen anfordernde Benutzer Writer Metadata Documents abfragen, um vollständige Informationen zu allen Komponenten zu erhalten, die im Sicherungskomponentendokument enthalten sind.

 

 




