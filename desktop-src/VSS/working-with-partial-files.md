---
description: Manchmal ist es hilfreich, nur Abschnitte von Dateien zu sichern und wiederherzustellen. VSS bietet partielle Dateimechanismen, die es Writern ermöglichen, teildateisicherungen und -wiederherstellungen anzugeben, wenn sie von Anfordernden unterstützt werden.
ms.assetid: 02b74a4e-d69f-4eeb-866a-3399598b7035
title: Arbeiten mit Teildateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13e1aa2623788cc97d62c88d52ec7096829adc350e1d420e92cea12b8dd64d70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118590454"
---
# <a name="working-with-partial-files"></a>Arbeiten mit Teildateien

Manchmal ist es hilfreich, nur Abschnitte von Dateien zu sichern und wiederherzustellen. VSS bietet [*partielle Dateimechanismen,*](vssgloss-p.md) die es Writern ermöglichen, teildateisicherungen und -wiederherstellungen anzugeben, wenn sie von Anfordernden unterstützt werden.

Teildateivorgänge sind häufig am häufigsten für Writer von Nutzen, die sehr große Dateien verwalten, von denen sich nur ein kleiner Teil zwischen Sicherungsvorgängen ändert. In diesem Fall ist es häufig hilfreich, nur diesen Abschnitt zu kopieren, der auf Sicherungsmedien geändert wurde. Aus diesem Grund werden partielle Dateivorgänge in der Regel, aber nicht ausschließlich, verwendet, um inkrementelle Sicherungs- und Wiederherstellungsvorgänge zu unterstützen.

Wenn ein Writer einen partiellen Dateivorgang implementieren möchte, verwendet er [**CVssWriter::IsPartialFileSupportEnabled,**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-ispartialfilesupportenabled) um zu bestimmen, ob der Anforderer, mit dem er arbeitet, den Vorgang unterstützt.

Wenn der Anforderer Teildateivorgänge unterstützt und die Komponente, die die Datei verwaltet (oder die Komponente, die den Komponentensatz definiert, der die Datei enthält), dem Sicherungskomponentendokument hinzufügt, gibt ein Writer an, welche Abschnitte der Datei gespeichert werden sollen (in der Regel bei der Behandlung eines [**PrepareForBackup-**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) oder [*PostSnapshot-Ereignisses),*](vssgloss-p.md) indem [**er IVssComponent::AddPartialFile aufruft.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile)

Zusätzlich zu einem Pfad und einem Dateinamen stellt der Writer den Bereich und optionale Metadateninformationen an [**IVssComponent::AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile)bereit.

Die Bereichsinformationen werden als Zeichenfolge bereitgestellt, die eine der folgenden Angaben enthält:

-   Offsetpaare in der datei zu sichernden Datei (in Bytes) und die Länge des zu sichernden Abschnitts (in Bytes), der Offset und die Länge, die durch einen Doppelpunkt getrennt werden, und jedes Paar wird durch ein Komma getrennt, z. B. *Offset1*:_Length1_*_,_* *Offset2***:**_Length2_.

    Jeder Wert ist eine 64-Bit-Ganzzahl (im Hexadezimal- oder Dezimalformat), die einen Byteoffset bzw. eine Länge in Bytes angibt.

-   Der vollständige Pfad einschließlich des Dateinamens im aktuellen System einer Binärbereichsdatei, die Folgendes enthält:
    -   Die Zahl (ausgedrückt als 64-Bit-Ganzzahl) unterschiedlicher Dateibereiche, die in der Datei enthalten sind
    -   Jeder Bereich wird als Paar von 64-Bit-Ganzzahlen ausgedrückt: der erste Member des Paars ist der Offset in die datei, die gesichert wird (in Bytes), und der zweite Member ist die Länge der zu sichernden Daten (in Bytes).

Wenn ein Writer eine Ranges-Datei verwendet, um einen Teildateivorgang anzugeben, muss ein Anforderer sicherstellen, dass diese Datei entweder gesichert wird (auch wenn die Datei nicht notwendigerweise Teil des Standardsicherungssatzes ist) oder dass die Bereichsinformationen auf dem Sicherungsmedium auf andere Weise beibehalten werden. Wenn die Informationen der Ranges-Datei nicht gesichert werden, ist das Wiederherstellen der teilweise gesicherten Datei nicht möglich.

Der Writer kann auch eine Zeichenfolge mit Metadaten hinzufügen. Diese Metadaten können in einem writer-spezifischen Format vorliegen, da sie es dem Writer ermöglichen sollen, zukünftige Wiederherstellungen zu überprüfen.

Mit diesen Informationen kann ein unterstützender Anforderer eine Partielle Dateisicherung ausführen.

Betrachten Sie beispielsweise eine große Datei, deren Header (Bytes 64-512) eine Datensatzanzahl und andere häufig aktualisierte Informationen enthält und deren aktuelle Daten in den letzten 65536 Bytes der Datei zu finden sind– Bytes, die 0x1239E7577A 0x1239E8577A.

Ein Writer kann eine Bereichsliste als Zeichenfolge **"64:448,0x1239E8577A:65536"** angeben.

Bei der Wiederherstellung und vor der tatsächlichen Durchführung eines Wiederherstellungsvorgangs sollte ein Anforderer überprüfen, ob Dateien teilweise Dateiunterstützung erfordern.

Hierzu durchläuft der Anforderer zunächst die Writer mit gespeicherten Komponenten im Sicherungskomponentendokument mithilfe von [**IVssBackupComponents::GetWriterComponentsCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponentscount) und [**IVssBackupComponents::GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents).

Die [**IVssBackupComponents::GetWriterComponents-Schnittstelle**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents) wird dann verwendet, um Instanzen der [**IVssWriterComponentsExt-Schnittstelle**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) zurückzugeben, die [**IVssWriterComponentsExt::GetComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponent) und [**IVssWriterComponentsExt::GetComponentCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponentcount)bereitstellen, mit denen der Anforderer [**IVssComponent-Instanzen**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) abrufen kann.

Dadurch kann ein Anforderer Informationen zu den teilweise gesicherten Dateien abrufen, um an einer Wiederherstellung teilzunehmen, indem [**er IVssComponent::GetPartialFileCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfilecount) und [**IVssComponent::GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile) für die Instanz von [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) verwendet, die der Komponente entspricht, die die Datei verwaltet (oder die Komponente, die den Komponentensatz definiert, der die Datei enthält).

Wenn der Teildateivorgang durch eine Ranges-Datei gesteuert wurde, sollte diese Datei vor dem Kopieren von Daten zurück auf den Datenträger wiederhergestellt werden. Es kann vorkommen, dass der Anforderer die Ranges-Datei zurück an einen neuen Speicherort auf dem Datenträger kopieren muss. In diesem Fall wird angegeben, dass dies über [**die IVssBackupComponents::SetRangesFilePath**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrangesfilepath)erfolgt ist.

Der Anforderer fährt dann mit dem Kopieren von Daten an die entsprechenden Speicherorte im Wiederherstellungsziel fort, die sich bereits auf dem Datenträger befinden.

Ein Writer (während der Behandlung eines [**PostRestore-Ereignisses)**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) durch Untersuchen von [**IVssComponent::GetFileRestoreStatus**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getfilerestorestatus) für die von [**IVssComponent::GetPartialFile angegebenen**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile)Dateien bestimmt, ob der Teildateivorgang erfolgreich war. Der Writer sollte immer versuchen, die Richtigkeit dieser Wiederherstellung mithilfe der Offsetinformationen und aller Metadaten zu überprüfen, die im Sicherungskomponentendokument enthalten sind.

Wenn der Anforderer die Bereichsdatei an einem neuen Speicherort wiederherstellen musste, aktualisiert VSS diese Informationen so, dass der von [**IVssComponent::GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile) zurückgegebene Pfad korrekt ist.

 

 
