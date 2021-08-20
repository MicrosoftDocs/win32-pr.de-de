---
description: Ein Sicherungssatz ist eine Liste aller zu sichernden Dateien, deren Speicherorte und deren Sicherung.
ms.assetid: 34a66a9c-c1bc-437d-b034-59dc0c88228c
title: Generieren eines Sicherungssets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 120643c827afdabfbb9a2c347fa16290e03969f0e87f913b0c5d9fdb682f2619
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122119"
---
# <a name="generating-a-backup-set"></a>Generieren eines Sicherungssets

Ein Sicherungssatz ist eine Liste aller zu sichernden Dateien, deren Speicherorte und deren Sicherung.

Eine Anfordernde muss die Dateien auf den schattenkopierten Volumes verwenden, nachdem [**IVssBackupComponents::D oSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) erfolgreich zurückgegeben wurde, um die vollständige Liste der zu sichernden Dateien zu generieren.

Darüber hinaus muss ein Anfordernde die Möglichkeit [](vssgloss-a.md) behandeln, dass einige Dateien alternative Pfade haben und einige Dateien ausgeschlossen wurden.

Ein Algorithmus für die Auswahl der zu [](vssgloss-w.md) sichernden Dateien sollte auf einer Writer-Instanz nach Writerinstanz und Komponentenbasis (wie bei der Wiederherstellung; siehe Generieren eines Wiederherstellungssets [)](generating-a-restore-set.md)erfolgen und wie folgt vorgehen:

1.  Bestimmen der Volumes, die die Dateien des Writers und die entsprechenden Geräteobjekte enthalten
2.  Erstellen [](vssgloss-f.md) Sie mithilfe der Dateisatzinformationen (die in [**IVssWMFiledesc-Objekten**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) enthalten sind, die von [**IVssExassoWriterMetadata::GetExcludeFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getexcludefile)zurückgegeben werden), eine Liste der explizit ausgeschlossenen Dateien, falls erforderlich, mit **findFileFirst**, **FindFileFirstEx** und **FindNextFile**.
3.  Iterieren aller Komponenten eines Writers [**mithilfe von IVssExvervollständigenWriterMetadata::GetComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent). Wenn eine auswählbare Komponente ausgewählt ist, verwenden Sie [*den*](vssgloss-l.md) logischen Pfad, um die nicht auswählbaren Komponenten zu erhalten, die ihr in einem Komponentensatz zugeordnet sind. (Weitere Informationen [finden Sie unter Arbeiten mit Auswählbarkeit und logischen Pfaden.)](working-with-selectability-and-logical-paths.md)
4.  Abrufen der [*in jeder*](vssgloss-f.md) ausgewählten Komponente enthaltenen Dateisätze mithilfe der [**IVssWMComponent-Schnittstelle,**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) die jeder enthaltenen Komponente entspricht.
5.  Generieren einer Liste von Dateien aus den Spezifikationen – bei Bedarf mit **FindFileFirst**, **FindFileFirstEx** und **FindNextFile**.
6.  Überprüft jede Datei in der Liste, die aus Komponenteninformationen generiert wurde, mit der Liste der ausgeschlossenen Dateien, die oben generiert wurden. Dies sollte mithilfe des Standardpfads für die Datei erfolgen (zurückgegeben von [**IVssWMFiledesc::GetPath),**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath)nicht anhand des alternativen Pfads, der von [**IVssWMFiledesc::GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation)zurückgegeben wird. Wenn die Datei der ausgeschlossenen Liste entspricht, wird sie nicht sichern.
7.  Auswählen des tatsächlichen Speicherorts, von dem aus die Zu sichern ist (mithilfe des alternativen Pfads, wenn er festgelegt wurde)
8.  An diesem Punkt ist eine vollständige Liste der Dateien und deren Speicherorte verfügbar, und eine Sicherung kann beginnen.

Nachdem ein erster Sicherungssatz für alle Writer generiert wurde, die im System vorhanden sind, überprüft der Anfordernde den folgenden Registrierungsschlüssel:

**HKEY \_ LOCAL \_ MACHINE \\ System \\ CurrentControlSet \\ Control \\ BackupRestore \\ FilesNotToBackup**

Der Anfordernde verwendet die Unterschlüssel unter diesem Schlüssel wie folgt:

-   Wenn ein Writer im System vorhanden ist und ein Unterschlüssel vorhanden ist, dessen Name dem Namen des Writers entspricht, muss dieser Unterschlüssel ignoriert werden.
-   Wenn ein Writer auf dem System vorhanden war, aber derzeit nicht im Sicherungssatz vorhanden ist und ein übereinstimmende Unterschlüssel vorhanden ist, werden alle in den Daten des Unterschlüssels angegebenen Dateien ausgeschlossen und müssen aus dem Sicherungssatz entfernt werden.
-   Die Sicherungsanwendung fügt den Unterschlüsseldaten Dateien hinzu, indem sie einen MULTI SZ-Wert erstellt, der eine Liste von Dateispezifikationen für die Dateien enthält, die \_ nicht gesichert werden dürfen. Jede Zeichenfolge im MULTI \_ SZ-Wert sollte eine Dateispezifikation enthalten.
-   Dateispezifikationen können die ?-Datei enthalten. und \* Platzhalterzeichen. Eine Spezifikation kann rekursiv gemacht werden, indem /s am Ende angefügt wird. Wenn Sie beispielsweise "%TEMP% /s" angeben, werden alle Dateien im \\ Verzeichnis %TEMP% und in allen Unterverzeichnissen nicht \* sichern.

 

 



