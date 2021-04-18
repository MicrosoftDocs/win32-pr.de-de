---
description: Es gibt bestimmte Situationen, in denen die zu sichernden Dateien nicht der Standard Speicherort für diese Dateien sind.
ms.assetid: b9e96827-a678-45ca-8ede-4508a406f071
title: Arbeiten mit alternativen Pfaden während der Sicherung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a98e93af4d12b804032a64841542e731ff77e048
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344445"
---
# <a name="working-with-alternate-paths-during-backup"></a>Arbeiten mit alternativen Pfaden während der Sicherung

Es gibt bestimmte Situationen, in denen die zu sichernden Dateien nicht der Standard Speicherort für diese Dateien sind.

Beispielsweise können einige Writer nicht garantieren, dass Ihre Daten innerhalb des Zeitfensters zwischen [*Freeze*](vssgloss-f.md) -und [*Thaw*](vssgloss-t.md) -Ereignissen geleert wurden. Diese Writer können doppelte Dateien generieren, die eine letzte als funktionierend bekannte, gute Konfiguration in einem nicht standardmäßigen Quellverzeichnis oder einen [*alternativen Pfad*](vssgloss-a.md)enthalten.

Der Begriff "Alternativer Pfad", wie er mit VSS verwendet wird, sollte nicht mit dem Begriff " [*Alternative Speicherort Zuordnung*](vssgloss-a.md)" verwechselt werden. Alternative Pfade werden nur während Sicherungs Vorgängen verwendet und verweisen auf eine alternative Quelle, von der Sie gesichert werden. Alternative Speicherort Zuordnungen werden nur während Wiederherstellungs Vorgängen verwendet und beziehen sich auf ein alternatives Ziel für Wiederherstellungs Vorgänge.

**So verwenden Sie einen alternativen Pfad während der Sicherung**

1.  Während der Ermittlungsphase eines Sicherungs Vorgangs (siehe [Übersicht über die Sicherungs Ermittlungsphase](overview-of-the-backup-discovery-phase.md)) überprüft ein Anforderer die Komponenten Daten der einzelnen Writer mithilfe von [**ivssexamineschreitermetadata:: getComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent) und Get-Instanzen der [**ivsswmcomponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) -Schnittstelle.
2.  Ein Anforderer erhält dann den von jeder Komponente verwalteten [*Datei Satz*](vssgloss-f.md) , der durch Instanzen der [**ivsswmfiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) -Schnittstelle dargestellt wird, indem er die [**ivsswmcomponent:: GetFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getfile) -Methode aufruft.
3.  Zusätzlich zu einem Pfad ([**ivsswmfiledesc:: getpath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath)), eine Datei Spezifikation ([**ivsswmfiledesc:: GetFileSpec**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getfilespec)) und ein Rekursions Kennzeichen ([**ivsswmfiledesc:: getrecursive**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getrecursive)), ein [**ivsswmfiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) -Objekt kann einen alternativen Speicherort (als alternativer Pfad für Sicherungs Vorgänge und eine Alternative Speicherort Zuordnung für Wiederherstellungs Vorgänge) mithilfe der [**ivsswmfiledesc:: getalternateloationmethode**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) enthalten.
4.  Wenn der von [**ivsswmfiledesc:: getalternateloation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) zurückgegebene Wert nicht NULL ist, verwenden Sicherungs Anwendungen diesen Wert anstelle des Werts, der von [**ivsswmfiledesc:: getpath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath) abgerufen wird, um die zu sichernden Dateien auszuwählen und zu sichern.
5.  Trotz der Verwendung eines alternativen Pfads sollten die Anforderer die Datei Spezifikation und die rekursiven Einstellungen beachten, die von [**ivsswmfiledesc:: GetFileSpec**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getfilespec) und [**ivsswmfiledesc:: getrecursive**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getrecursive)zurückgegeben werden.

Beachten Sie, dass bei der Wiederherstellung jeder Alternative Pfad – d. h. ein alternativer Speicherort, der von einer Instanz von [**ivsswmfiledesc:: getalternateloation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) zurückgegeben wird, die von einer Instanz von [**ivsswmcomponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent)abgerufen wurde, die wiederum von einer Instanz von [**ivssexamineschreibmetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) abgerufen wurde, die durch das Abrufen eines gespeicherten Writer-Metadatendokuments abgerufen wurde

Entweder der Standardpfad (von der [**GetPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath) -Methode der gleichen Instanz von [**ivsswmfiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc)zurückgegeben) wird verwendet, um einen Wiederherstellungs Speicherort zu definieren, oder eine Alternative Speicherort Zuordnung – mit der [**ivsswmfiledesc:: getalternateloation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) -Methode – gibt an, wo eine [Datei wieder hergestellt](working-with-alternate-locations-during-restore.md)werden soll

 

 



