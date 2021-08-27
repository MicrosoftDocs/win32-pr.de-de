---
description: Es gibt bestimmte Situationen, in denen die zu sichernden Dateien nicht der Standardspeicherort für diese Dateien sind.
ms.assetid: b9e96827-a678-45ca-8ede-4508a406f071
title: Arbeiten mit alternativen Pfaden während der Sicherung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62bc969c96d943b73a8a9d9609f004b4a0f738c46802af20a7dff22e34ebac56
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124450"
---
# <a name="working-with-alternate-paths-during-backup"></a>Arbeiten mit alternativen Pfaden während der Sicherung

Es gibt bestimmte Situationen, in denen die zu sichernden Dateien nicht der Standardspeicherort für diese Dateien sind.

Einige Writer können beispielsweise nicht garantieren, dass ihre Daten innerhalb des Zeitfensters zwischen [*Freeze-*](vssgloss-f.md) und [*Thaw-Ereignissen geleert*](vssgloss-t.md) wurden. Solche Writer können doppelte Dateien generieren, die eine letzte als gut bekannte Konfiguration in einem nicht standardmäßigen Quellverzeichnis oder einem alternativen [*Pfad enthalten.*](vssgloss-a.md)

Der Begriff alternativer Pfad, wie er mit VSS verwendet wird, sollte nicht mit dem Begriff alternativer Speicherortzuordnung [*verwechselt werden.*](vssgloss-a.md) Alternative Pfade werden nur während Sicherungsvorgängen verwendet und verweisen auf eine alternative Quelle, aus der gesichert werden soll. Alternative Speicherortzuordnungen werden nur bei Wiederherstellungsvorgängen verwendet und verweisen auf ein alternatives Ziel für Wiederherstellungsvorgänge.

**So verwenden Sie einen alternativen Pfad während der Sicherung**

1.  Während der Ermittlungsphase eines Sicherungsvorgang (siehe Übersicht über die Sicherungsermittlungsphase) [](overview-of-the-backup-discovery-phase.md)untersuchte ein An anfordernder Benutzer die Komponentendaten jedes Writers mithilfe von [**IVssExwriterMetadata::GetComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent) und dem Get-Instanzen der [**IVssWMComponent-Schnittstelle.**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent)
2.  Ein Anfordernder ruft dann [](vssgloss-f.md) den von jeder Komponente verwalteten Dateisatz ab, der durch Instanzen der [**IVssWMFiledesc-Schnittstelle**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) dargestellt wird, indem er die [**IVssWMComponent::GetFile-Methode**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getfile) aufruft.
3.  Zusätzlich zu einem Pfad ([**IVssWMFiledesc::GetPath),**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath)einer Dateispezifikation ([**IVssWMFiledesc::GetFilespec)**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getfilespec)und einem Rekursionsflag ([**IVssWMFiledesc::GetRecursive**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getrecursive)), ein [**IVssWMFiledesc-Objekt**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) kann einen alternativen Speicherort (verwendet als alternativer Pfad für Sicherungsvorgänge und eine alternative Speicherortzuordnung für Wiederherstellungsvorgänge) mithilfe der [**IVssWMFiledesc::GetAlternateLocation-Methode**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) enthalten.
4.  Wenn der von [**IVssWMFiledesc::GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) zurückgegebene Wert nicht NULL ist, verwenden Sicherungsanwendungen diesen Wert anstelle des Werts aus [**IVssWMFiledesc::GetPath,**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath) um zu sichernde Dateien auszuwählen und zu suchen.
5.  Trotz der Verwendung eines alternativen Pfads sollten anfordernde Benutzer weiterhin die Dateispezifikation und die rekursiven Einstellungen, die von [**IVssWMFiledesc::GetFilespec**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getfilespec) und [**IVssWMFiledesc::GetRecursive**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getrecursive)zurückgegeben werden, achten.

Beachten Sie, dass bei der Wiederherstellung jeder alternative Pfad , d.&160;, der von einer Instanz von [**IVssWMFiledesc::GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) von einer Instanz von [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent)abgerufen wurde, der wiederum von einer Instanz von [**IVssExosiWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) abgerufen wurde, die durch Abrufen eines gespeicherten Writer-Metadatendokuments abgerufen wurde, während der Wiederherstellung nicht verwendet wird.

Entweder wird der Standardpfad (der von der [**GetPath-Methode**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath) der gleichen Instanz von [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc)zurückgegeben wird) verwendet, um einen Wiederherstellungsort zu definieren, oder eine alternative Speicherortzuordnung , die mithilfe der [**IVssWMFiledesc::GetAlternateLocation-Methode**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) gefunden wird, gibt an, wo eine Datei wiederhergestellt werden soll (siehe Arbeiten mit alternativen Speicherorten während der Wiederherstellung [).](working-with-alternate-locations-during-restore.md)

 

 



