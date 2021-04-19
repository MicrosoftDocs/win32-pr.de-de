---
description: Es ist manchmal hilfreich, nur Datei Abschnitte zu sichern und wiederherzustellen. VSS stellt partielle Datei Mechanismen bereit, die es Writer ermöglichen, Teil Dateien Sicherungen und-Wiederherstellungen anzugeben, wenn Sie von Anforderern unterstützt werden.
ms.assetid: 02b74a4e-d69f-4eeb-866a-3399598b7035
title: Arbeiten mit partiellen Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7194f01df11f6c0e368941e17ef6ab1620b17f67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344444"
---
# <a name="working-with-partial-files"></a>Arbeiten mit partiellen Dateien

Es ist manchmal hilfreich, nur Datei Abschnitte zu sichern und wiederherzustellen. VSS stellt [*partielle Datei*](vssgloss-p.md) Mechanismen bereit, die es Writer ermöglichen, Teil Dateien Sicherungen und-Wiederherstellungen anzugeben, wenn Sie von Anforderern unterstützt werden.

Partielle Datei Vorgänge sind häufig die beste Verwendung von Writern, die sehr große Dateien verwalten, nur ein kleiner Bruchteil der Änderung zwischen den Sicherungs Vorgängen. Dies ist der Fall, es ist häufig hilfreich, nur den Abschnitt zu kopieren, der auf Sicherungsmedien geändert wurde. Aus diesem Grund werden partielle Datei Vorgänge in der Regel, aber nicht exklusiv verwendet, um inkrementelle Sicherungs-und Wiederherstellungs Vorgänge zu unterstützen.

Wenn ein Writer eine partielle Dateioperation implementieren möchte, wird [**CVssWriter:: ispartialfilesupportenabled**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-ispartialfilesupportenabled) verwendet, um zu bestimmen, ob der Anforderer, mit dem er arbeitet, den Vorgang unterstützt.

Wenn die anfordernde Person partielle Datei Vorgänge unterstützt und die Komponente, mit der die Datei verwaltet wird (oder die Komponente, die den Komponenten Satz definiert, der die Datei enthält), in das Dokument mit den Sicherungs Komponenten eingefügt wird, gibt ein Writer an, welche [](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) Abschnitte der Datei gespeichert werden [](vssgloss-p.md) sollen [](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile)

Neben dem Pfad und dem Dateinamen stellt der Writer den Bereich optionale Metadateninformationen für [**IVssComponent:: addpartialfile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile)bereit.

Die Bereichs Informationen werden als Zeichenfolge bereitgestellt, die eine der folgenden Optionen enthält:

-   Paare von Offsets in die zu sichernde Datei (in Bytes) und die Länge des zu sichernden Abschnitts (in Bytes), der Offset und die Länge, die durch einen Doppelpunkt getrennt werden, und jedes Paar durch Kommas getrennt, z. b. *offset1 ***:**_Length1_*_,_* * Offset2 ***:**_Length2_.

    Jeder Wert ist eine 64-Bit-Ganzzahl (im Hexadezimal-oder Dezimal Format), die jeweils einen Byte Offset und eine Länge in Byte angibt.

-   Der vollständige Pfad, einschließlich des Datei namens, auf dem aktuellen System einer Binär Bereichs Datei, die Folgendes enthält:
    -   Die Zahl (ausgedrückt als 64-Bit-Ganzzahl) mit unterschiedlichen Datei Bereichen, die in der Datei enthalten sind.
    -   Jeder Bereich wird als Paar von 64-Bit-Ganzzahlen ausgedrückt: das erste Element des Paars ist der Offset in die zu sichernde Datei (in Bytes), und der zweite Member ist die Länge der zu sichernden Daten (in Bytes).

Wenn ein Writer eine Bereichs Datei zum Angeben eines partiellen Datei Vorgangs verwendet, muss ein Anforderer sicherstellen, dass entweder diese Datei gesichert wird (auch wenn die Datei nicht notwendigerweise Teil des Standard Sicherungs Satzes ist) oder dass die Bereichs Informationen auf den Sicherungsmedien auf andere Weise beibehalten werden. Wenn die Informationen zu den Bereichs Dateien nicht gesichert werden, ist das Wiederherstellen der teilweise gesicherten Datei nicht möglich.

Der Writer kann auch eine Zeichenfolge hinzufügen, die Metadaten enthält. Diese Metadaten können ein Schreib spezifisches Format aufweisen, da es dem Writer ermöglicht, zukünftige Wiederherstellungen zu überprüfen.

Mit diesen Informationen kann eine unterstützende Anforderer eine partielle Datei Sicherung ausführen.

Betrachten Sie als Beispiel eine große Datei, deren Header (Bytes 64-512) eine Daten Satz Anzahl und andere häufig aktualisierte Informationen enthält und deren aktuelle Daten in den letzten 65536 Bytes der Datei – Bytes 0x1239e8577a bis 0x1239e7577a zu finden sind.

Ein Writer könnte eine Bereichs Liste als Zeichenfolge "**64:448, 0x1239e8577a: 65536**" angeben.

Bei der Wiederherstellung und vor der tatsächlichen Ausführung eines Wiederherstellungs Vorgangs sollte ein Anforderer überprüfen, ob Dateien partielle Dateiunterstützung benötigen.

Zu diesem Zweck durchläuft der Anforderer zuerst die Writer mit gespeicherten Komponenten in seinem Sicherungs Komponenten Dokument mithilfe von [**IVssBackupComponents:: getwritercomponentscount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponentscount) und [**IVssBackupComponents:: getwritercomponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents).

Die [**IVssBackupComponents:: getschreitercomponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents) -Schnittstelle wird dann verwendet, um Instanzen der [**ivssschreitercomponentset**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) -Schnittstelle zurückzugeben, die [**ivssschreitercomponentset XT:: getComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponent) und [](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) [**ivssschreitercomponentset XT:: getcomponentcount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponentcount)angeben

Dadurch kann ein Anforderer Informationen über die teilweise gesicherten Dateien abrufen, um an einer Wiederherstellung teilzunehmen, indem [**IVssComponent:: GetPartialFileCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfilecount) und [**IVssComponent:: GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile) für die Instanz von [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) verwendet werden. Dies entspricht der Komponente, die die Datei verwaltet (oder der Komponente, die den Komponenten Satz definiert, der die Datei enthält).

Wenn der Teil Datei Vorgang durch eine Bereichs Datei gesteuert wurde, sollte diese Datei vor dem Kopieren der Daten auf den Datenträger wieder hergestellt werden. Es kann vorkommen, dass die anfordernde Person die Bereichs Datei an einen neuen Speicherort auf dem Datenträger Zurückkopieren muss. In diesem Fall ist dies ein Hinweis darauf, dass dies über den [**IVssBackupComponents:: Server File Path**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrangesfilepath)erfolgt ist.

Der Anforderer fährt dann mit dem Kopieren von Daten an die entsprechenden Speicherorte im Wiederherstellungs Ziel auf dem Datenträger fort.

Ein Writer (bei der Behandlung eines [**postrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) -Ereignisses) bestimmt durch Untersuchen von [**IVssComponent:: getfilerestorestatus**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getfilerestorestatus) für die durch [**IVssComponent:: GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile)festgelegten Dateien, ob der Teil Datei Vorgang erfolgreich war. Der Writer sollte immer versuchen, die Richtigkeit dieser Wiederherstellung mit den Offset Informationen und Metadaten zu überprüfen, die im Dokument mit den Sicherungs Komponenten enthalten sind.

Wenn der Anforderer die Bereichs Datei an einem neuen Speicherort wiederherstellen muss, aktualisiert VSS diese Informationen so, dass der von [**IVssComponent:: GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile) zurückgegebene Pfad richtig ist.

 

 
