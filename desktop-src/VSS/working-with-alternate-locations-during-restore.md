---
description: Es gibt zahlreiche Gründe, warum eine anfordernde Person entweder nicht oder nicht in der Lage sein sollte, Dateien von einem Sicherungsmedium an Ihrem ursprünglichen Speicherort wiederherzustellen.
ms.assetid: 2a9cfd99-5a2c-4c0c-98ff-11c745298cda
title: Arbeiten mit alternativen Speicherorten während der Wiederherstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1338d76f98153ccb388e86e738b408c03dd253b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346947"
---
# <a name="working-with-alternate-locations-during-restore"></a>Arbeiten mit alternativen Speicherorten während der Wiederherstellung

Es gibt zahlreiche Gründe, warum eine anfordernde Person entweder nicht oder nicht in der Lage sein sollte, Dateien von einem Sicherungsmedium an Ihrem ursprünglichen Speicherort wiederherzustellen. Beispielsweise kann eine Wiederherstellungsmethode oder ein Ziel eine solche Wiederherstellung erfordern, oder der aktuelle Wiederherstellungs Speicherort ist möglicherweise belegt und kann nicht geschrieben werden.

Zum behandeln solcher Fälle hat ein Writer möglicherweise eine [*Alternative Speicherort Zuordnung*](vssgloss-a.md)definiert, ein nicht standardmäßiges Wiederherstellungs Ziel, das für besondere Umstände verwendet werden soll.

Der Begriff "Alternative Speicherort Zuordnung", wie er mit VSS verwendet wird, sollte nicht mit dem Begriff " [*Alternativer Pfad*](vssgloss-a.md)" verwechselt werden. Alternative Speicherort Zuordnungen werden nur während Wiederherstellungs Vorgängen verwendet und beziehen sich auf ein alternatives Ziel für Wiederherstellungs Vorgänge. Alternative Pfade werden nur während Sicherungs Vorgängen verwendet und verweisen auf eine alternative Quelle, von der Sie gesichert werden.

Um bei der Wiederherstellung Alternative Speicherort Zuordnungen zu verwenden, würde ein Anforderer Folgendes tun (in der Regel nach der Generierung eines [**vorab**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) Ereignisses):

1.  Mithilfe einer Instanz der [**ivssexaminewrite Metadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) -Schnittstelle, die durch Abrufen eines gespeicherten Writers abgerufen wurde, verwendet ein Anforderer die [**ivssexaminewrite Metadata:: getalternatelocationmapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping) -Methode, um die alternativen Speicherort Zuordnungen eines Writers als Instanzen der [**ivsswmfiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) -Schnittstelle abzurufen.

    > [!Note]  
    > Der Anforderer verwendet [**ivssexaminewrite Metadata:: getalternatelocationmapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping), nicht [**IVssComponent:: getalternatelocationmapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping). Der erste gibt die alternativen Speicherort Zuordnungen zurück, die für die Verwendung durch einen Anforderer verfügbar sind. Letzteres wird verwendet, um die alternativen Speicherort Zuordnungen anzugeben, die tatsächlich von einem Anforderer verwendet werden.

     

2.  Der Aufruf von [**ivssexamineschreitermetadata:: getalternatelocationmapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping) gibt eine Instanz der [**ivsswmfiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) -Schnittstelle zurück. Diese Instanz enthält Datei Satz Informationen – einen Pfad, der von [**ivsswmfiledesc:: getpath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath)angegeben wird, eine Datei Spezifikation, die durch [**ivsswmfiledesc:: GetFileSpec**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getfilespec)zurückgegeben wurde, und ein Rekursions Flag, das von [**ivsswmfiledesc abgerufen wurde: getrecursive**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getrecursive)– Übereinstimmung mit einem der hinzugefügten Datei Sätze (unter Verwendung von [**ivsskreateschreitermetadata:: adddatabasefiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles), [**ivsskreateschreitermetadata:: adddatabaselogfiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)oder [**ivsskreateschreitermetadata:: addfilestofilegroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)) zu einer der vom Writer verwalteten Komponenten.

    Der von [**ivsswmfiledesc:: getalternateloation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) zurückgegebene Wert ist die Alternative Speicherort Zuordnung für diesen Datei Satz.

3.  Alternative Speicherort Zuordnungen enthalten keine Komponenten Informationen, daher ist es erforderlich, die Datei Satz Informationen (Pfad, Datei Spezifikation und Rekursions Flag) zu vergleichen, die durch den Aufruf von [**ivssexamineschreitermetadata:: getalternatelocationmapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping) abgerufen werden, der in den Komponenten des Writers enthalten ist.

    Diese Informationen können Sie finden, indem Sie die Komponenten des Writers durchlaufen und [**ivssexamineschreitermetadata:: getComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent) aufrufen, um eine Instanz der [**ivsswmcomponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) -Schnittstelle abzurufen, und [**ivsswmcomponent:: GetFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getfile) zum Abrufen einer [**ivsswmfiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) -Instanz verwenden, die die Komponenten Datei Satz Informationen enthält.

    Wenn die Datei Satz Informationen von der [**ivsswmfiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) -Instanz zurückgegeben werden, die von [**ivssexamineschreitermetadata abgerufen wurde: getComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent) und [**ivsswmcomponent:: GetFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getfile) stimmen überein, die von der **ivsswmfiledesc** -Instanz abgerufen werden, die von [**ivsswmfiledesc:: getalternateloation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation)abgeleitet wurde. die Komponente, die die Dateien mit der jeweiligen alternativen Speicherort Zuordnung verwaltet, wurde gefunden.

4.  Wenn Sie die Komponente gefunden haben, kann der Anforderer die Bedingungen ermitteln, unter denen eine Alternative Speicherort Zuordnung verwendet werden soll. gehen Sie hierzu wie folgt vor:

    -   Untersuchen der Restore-Methode der Komponente, die durch den Aufruf von [**ivssexamineschreitermetadata:: getrestoremethod**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getrestoremethod)abgerufen wird.
    -   Überprüfen, ob ein Wiederherstellungs Ziel die Restore-Methode überschreibt, indem [**IVssComponent:: getrestoretarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget)aufgerufen wird.

        Wenn die im Writer-Metadatendokument gefundene Komponente explizit in der Sicherung [*enthalten*](vssgloss-e.md) war, entspricht die Instanz der [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) -Schnittstelle dieser Komponente. Wenn die Komponente implizit in die Sicherung [*eingeschlossen*](vssgloss-i.md) wurde, entspricht die Instanz von **IVssComponent** der Komponente, die den Komponenten Satz definiert, von dem die Komponente im Writer-Metadatendokument eine untergeordnete Komponente ist.

5.  Mit diesen Informationen kann der Anforderer Komponenten Weise ermitteln, wenn er einen bestimmten Datei Satz einer bestimmten Komponente in einem Ziel wiederherstellen muss, das durch die Alternative Speicherort Zuordnung definiert ist.

6.  Bei Verwendung einer alternativen Speicherort Zuordnung respektiert der Anforderer den Dateideskriptor und das rekursive Flag des Datei Satzes und verwendet den Pfad, der von der alternativen Speicherort Zuordnung bereitgestellt wird.

    Der Anforderer zeigt an, dass er bei einem Wiederherstellungs Vorgang eine Alternative Speicherort Zuordnung verwendet hat, indem er [**IVssBackupComponents:: addalternativelocationmapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping) mit den Standard Speicherort Informationen des Datei Satzes, das alternative Wiederherstellungs Ziel und einen Komponentennamen aufgerufen hat.

    Wenn der Datei Satz von einer Komponente verwaltet wurde, die explizit in der Sicherung enthalten war, wird dieser Komponenten Name verwendet. Wenn der Datei Satz von einer Komponente verwaltet wurde, die implizit in der Sicherung enthalten war, wird als Name der Komponente verwendet, die den Komponenten Satz definiert, von dem die Komponente, die den Datei Satz verwaltet, eine untergeordnete Komponente ist.

Writer überprüfen, ob die Datei Sätze von einer ihrer Komponenten an einer alternativen Speicherort Zuordnung wieder hergestellt wurden, indem Sie [**IVssComponent:: getalternatelocationmapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping)aufrufen.

 

 



