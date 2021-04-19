---
description: Ein Sicherungs Satz ist eine Liste aller zu sichernden Dateien, ihrer Standorte und deren Sicherung.
ms.assetid: 34a66a9c-c1bc-437d-b034-59dc0c88228c
title: Erstellen eines Sicherungs Satzes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 827d9ecb90ac376aa9818b61e8dab65550ff8c50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349787"
---
# <a name="generating-a-backup-set"></a>Erstellen eines Sicherungs Satzes

Ein Sicherungs Satz ist eine Liste aller zu sichernden Dateien, ihrer Standorte und deren Sicherung.

Ein Anforderer muss die Dateien verwenden, die auf den schattenkopierten Volumes enthalten sind, nachdem [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) erfolgreich zurückgegeben wurde, um die vollständige Liste der zu sichernden Dateien zu generieren.

Außerdem muss eine anfordernde Person die Möglichkeit behandeln, dass einige Dateien über [*alternative Pfade*](vssgloss-a.md) verfügen und einige Dateien ausgeschlossen wurden.

Ein Algorithmus zum Auswählen von zu sichernden Dateien sollte in einer [*Writer-Instanz*](vssgloss-w.md) von der Writer-Instanz, Komponenten Weise, (wie bei [der Wiederherstellung) erfolgen](generating-a-restore-set.md), und Sie können wie folgt vorgehen:

1.  Bestimmen der Volumes, die die Dateien des Writers und der entsprechenden Geräte Objekte enthalten
2.  Mithilfe der [*Datei Satz*](vssgloss-f.md) Informationen (die in [**ivsswmfiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) -Objekten enthalten sind, die von [**ivssexamineschreibmetadata:: getexcludefile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getexcludefile)zurückgegeben werden) können Sie ggf. eine Liste der explizit ausgeschlossenen Dateien erstellen, indem Sie **FindFileFirst**, **findfilefirstex** und **FindNextFile** verwenden.
3.  Iteration über alle Komponenten eines Writers mithilfe von [**ivssexaminewrite Metadata:: getComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent). Wenn eine auswählbare Komponente ausgewählt ist, verwenden Sie den [*logischen Pfad*](vssgloss-l.md) , um die ihm zugeordneten nicht auswählbaren Komponenten in einem Komponenten Satz abzurufen. (Weitere Informationen finden Sie [unter Arbeiten mit selekabilität und logischen Pfaden](working-with-selectability-and-logical-paths.md).)
4.  Abrufen der [*Datei Sätze*](vssgloss-f.md) , die in jeder ausgewählten Komponente enthalten sind, mithilfe der [**ivsswmcomponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) -Schnittstelle, die den einzelnen enthaltenen Komponenten entspricht.
5.  Erstellen einer Liste von Dateien aus den Spezifikationen – bei Bedarf mithilfe von **FindFileFirst**, **findfilefirstex** und **FindNextFile**.
6.  Überprüfen jeder in der Liste generierten Datei in der Liste anhand der Liste der ausgeschlossenen Dateien, die oben generiert wurden. Dies sollte mithilfe des Standard Pfads für die Datei (zurückgegeben von [**ivsswmfiledesc:: getpath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath)) erfolgen, nicht durch den alternativen Pfad, der von [**ivsswmfiledesc:: getalternateloation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation)zurückgegeben wird. Wenn die Datei mit der Ausschlussliste übereinstimmt, wird Sie nicht gesichert.
7.  Auswählen des tatsächlichen Speicher Orts für die Sicherungskopie (mit dem alternativen Pfad, wenn er festgelegt wurde)
8.  An diesem Punkt steht eine vollständige Liste der Dateien und ihrer Speicherorte zur Verfügung, und eine Sicherung kann beginnen.

Nachdem ein erster Sicherungs Satz für alle Writer generiert wurde, die auf dem System vorhanden sind, überprüft die Anforderer den folgenden Registrierungsschlüssel:

**HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Control \\ backuprestore \\ FilesNotToBackup**

Der Anforderer verwendet die untergeordneten Schlüssel unter diesem Schlüssel wie folgt:

-   Wenn ein Writer auf dem System vorhanden ist und ein Unterschlüssel vorhanden ist, dessen Name mit dem Namen des Writers übereinstimmt, muss dieser Unterschlüssel ignoriert werden.
-   Wenn ein Writer auf dem System vorhanden ist, aber derzeit nicht im Sicherungs Satz vorhanden ist und ein entsprechender Unterschlüssel vorhanden ist, werden alle in den Unterschlüssel Daten angegebenen Dateien ausgeschlossen und müssen aus dem Sicherungs Satz entfernt werden.
-   Die Sicherungs Anwendung fügt den Unterschlüssel Datendateien hinzu, indem Sie einen \_ MultiSZ-Wert erstellt, der eine Liste mit Datei Spezifikationen für die Dateien enthält, die nicht gesichert werden dürfen. Jede Zeichenfolge im \_ MultiSZ-Wert muss eine Datei Spezifikation enthalten.
-   Datei Spezifikationen können das enthalten? und Platzhalter \* Zeichen. Eine Spezifikation kann rekursiv gemacht werden, indem/s am Ende angehängt wird. Wenn Sie z. b. "% Temp% \\ \* /s" angeben, werden alle Dateien im Verzeichnis "% Temp%" und alle zugehörigen Unterverzeichnisse nicht gesichert.

 

 



