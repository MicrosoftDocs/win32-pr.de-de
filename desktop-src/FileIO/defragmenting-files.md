---
description: Defragmentierung ist der Prozess, bei dem Teile von Dateien auf einem Datenträger bewegt werden, um Dateien zu defragmentieren, d.&a0;b. der Prozess des Verschiebens von Dateiclustern auf einem Datenträger, um sie zusammenhängend zu machen.
ms.assetid: 27ccaab7-ec89-489b-80dc-df9beb7969bc
title: Defragmentieren von Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f04c0a3c961854b7e3ecab50d67db608178393113ca259b916db9623058e2f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696290"
---
# <a name="defragmenting-files"></a>Defragmentieren von Dateien

Wenn eine Datei auf einen Datenträger geschrieben wird, kann sie manchmal nicht in zusammenhängenden Clustern geschrieben werden. Nicht zusammenhängende Cluster verlangsamen das Lesen und Schreiben einer Datei. Wenn die nicht zusammenhängenden Cluster auf einem Datenträger weiter auseinander liegen, ist das Problem aufgrund der Zeit, die zum Verschieben des Lese-/Schreibkopfs eines Festplattenlaufwerks benötigt wird, noch schlechter. Eine Datei mit nicht zusammenhängenden Clustern ist *fragmentiert.* Um Dateien für schnellen Zugriff zu optimieren, kann ein Volume defragmentiert werden.

*Defragmentation* is the process of moving portions of files around on a disk to defragment files, that is, the process of moving file clusters on a disk to make them contiguous. Weitere Informationen finden Sie in den folgenden Abschnitten:

-   [Defragmentieren einer Datei](#defragmenting-a-file)
-   [Minimieren von Interaktionen zwischen Defragmentierung und Schattenkopien](#minimizing-interactions-between-defragmentation-and-shadow-copies)
-   [Dateien, Streams und Streamtypen, die für die Defragmentierung unterstützt werden](#files-streams-and-stream-types-supported-for-defragmentation)

## <a name="defragmenting-a-file"></a>Defragmentieren einer Datei

In einem einfachen Einzelaufgabe-Betriebssystem ist die Defragmentierungssoftware die einzige Aufgabe, und es gibt keine anderen Prozesse, von dem der Datenträger gelesen oder auf den Datenträger geschrieben werden kann. In einem Multitaskingbetriebssystem können einige Prozesse jedoch lesen und auf eine Festplatte schreiben, während ein anderer Prozess dieses Festplattenlaufwerk defragmentiert. Der Trick besteht in der Vermeidung von Schreibvorgängen in eine Datei, die defragmentiert wird, ohne den Schreibvorgang sehr lange zu beenden. Die Lösung dieses Problems ist nicht trivial, aber es ist möglich.

Um eine Defragmentierung zu ermöglichen, ohne dass ausführliche Kenntnisse über die Struktur eines Dateisystemdatenträgers erforderlich sind, wird ein Satz von drei Steuerelementcodes bereitgestellt. Die Steuerungscodes bieten die folgenden Funktionen:

-   Ermöglichen der Suche nach leeren Clustern durch Anwendungen
-   Bestimmen des Speicherorts von Dateiclustern auf dem Datenträger
-   Verschieben von Clustern auf einem Datenträger

Die Steuerungscodes behandeln auch transparent das Problem, dass andere Prozesse während der Verschiebevorgänge aus Dateien lesen und in diese schreiben können.

Diese Vorgänge können ausgeführt werden, ohne die Ausführung anderer Prozesse zu verhindern. Die anderen Prozesse haben jedoch langsamere Antwortzeiten, während ein Laufwerk defragmentiert wird.

**So defragmentieren Sie eine Datei**

1.  Verwenden Sie [**den FSCTL \_ GET VOLUME \_ BITMAP-Steuerungscode, \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_volume_bitmap) um einen Platz auf dem Volume zu finden, der groß genug ist, um eine gesamte Datei zu akzeptieren.
    > [!Note]  
    > Verschieben Sie bei Bedarf andere Dateien, um einen ausreichend großen Ort zu erstellen. Im Idealfall gibt es genügend nicht zugewiesene Cluster nach dem ersten Block der Datei, damit Sie nachfolgende Blöcke nach dem ersten Block in den Bereich verschieben können.

     

2.  Verwenden Sie [**den FSCTL \_ GET RETRIEVAL \_ POINTERS-Steuerungscode, \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_retrieval_pointers) um eine Zuordnung des aktuellen Layouts der Datei auf dem Datenträger zu erhalten.
3.  Gehen Sie die VON FSCTL GET RETRIEVAL POINTERS zurückgegebene [**RETRIEVAL \_ \_ POINTERS \_ BUFFER-Struktur durch.**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_retrieval_pointers) [**\_ \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-retrieval_pointers_buffer)
4.  Verwenden Sie [**den FSCTL \_ MOVE FILE-Steuerungscode, \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_move_file) um jeden Cluster zu verschieben, während Sie die Struktur durchziehen.
    > [!Note]  
    > Möglicherweise müssen Sie entweder die Bitmap oder die Abrufstruktur oder beides zu verschiedenen Zeiten erneuern, wenn andere Prozesse auf den Datenträger schreiben.

     

Zwei der Vorgänge, die im Defragmentierungsprozess verwendet werden, erfordern ein Handle für ein Volume. Nur Administratoren können ein Handle für ein Volume abrufen, sodass nur Administratoren ein Volume defragmentieren können. Eine Anwendung sollte die Rechte eines Benutzers überprüfen, der versucht, Defragmentierungssoftware ausführen zu lassen, und es einem Benutzer nicht erlauben, ein Volume zu defragmentieren, wenn der Benutzer nicht über die entsprechenden Rechte verfügt.

Wenn Sie [**CreateFile verwenden,**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) um ein Verzeichnis während der Defragmentierung eines FAT- oder FAT32-Dateisystemvolumens zu öffnen, geben Sie den Wert **generic \_ read** access mask an. Geben Sie nicht den **Wert maximum \_ allowed** access mask an. Wenn dies erfolgt, wird der Zugriff auf das Verzeichnis verweigert.

Versuchen Sie nicht, zugeordnete Cluster in einem NTFS-Dateisystem zu verschieben, die über die gerundete Clusterdateigröße hinausgehen, da das Ergebnis ein Fehler ist.

Punkte, Bitmaps und Attributlisten in NTFS-Dateisystemvolumes können neu analysiert, zum Lesen und Synchronisieren geöffnet und mit der Datei *benannt* werden:*name*: Typsyntax; Beispiel: *dirname*:$i 30:$INDEX \_ ALLOCATION, *mrp*::$DATA, *mrp*::$REPARSE \_ POINT und *mrp*::$ATTRIBUTE \_ LIST.

Beim Defragmentieren von NTFS-Dateisystemvolumes ist das Defragmentieren eines virtuellen Clusters über die Zuordnungsgröße einer Datei hinaus zulässig.

## <a name="minimizing-interactions-between-defragmentation-and-shadow-copies"></a>Minimieren von Interaktionen zwischen Defragmentierung und Schattenkopien

Verschieben Sie Daten nach Möglichkeit in Blöcken, die relativ zueinander in Schritten von 16 Kilobyte (KB) ausgerichtet sind. Dies reduziert den Aufwand beim Kopieren beim Schreiben, wenn Schattenkopien aktiviert werden, da der Schattenkopiespeicher erhöht und die Leistung reduziert wird, wenn die folgenden Bedingungen eintreten:

-   Die Blockgröße der Move Request ist kleiner oder gleich 16 KB.
-   Das Änderungsdelta befindet sich nicht in Schritten von 16 KB.

Das Änderungsdelta ist die Anzahl von Bytes zwischen dem Anfang des Quellblocks und dem Anfang des Zielblocks. Anders ausgedrückt: Ein Block, der bei Offset X (auf dem Datenträger) beginnt, kann in einen Startoffset Y verschoben werden, wenn der absolute Wert von X minus Y ein gleichmäßiges Vielfaches von 16 KB ist. Wenn also von 4-KB-Clustern ausgegangen wird, wird ein Wechsel von Cluster 3 zu Cluster 27 optimiert, aber ein Wechsel von Cluster 18 zu Cluster 24 wird nicht ausgeführt. Beachten Sie, dass mod(3,4) = 3 = mod(27,4) ist. Mod 4 wird ausgewählt, da vier Cluster mit jeweils 4 KB 16 KB entsprechen. Daher führt ein Volume, das auf eine Clustergröße von 16 KB formatiert ist, dazu, dass alle Verschiebendateien optimiert werden.

Weitere Informationen zu Schattenkopien finden Sie unter [Volumeschattenkopie-Dienst](/windows/desktop/VSS/about-the-volume-shadow-copy-service).

## <a name="files-streams-and-stream-types-supported-for-defragmentation"></a>Dateien, Streams und Streamtypen, die für die Defragmentierung unterstützt werden

Die meisten Dateien können zwar mit dem [**FSCTL \_ MOVE FILE-Steuerungscode \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_move_file) verschoben werden, aber nicht alle können verschoben werden. Im Folgenden finden Sie eine Liste der Dateien, Streams und Streamtypen (auch als Attributtypcodes bezeichnet), die von **FSCTL \_ MOVE FILE unterstützt \_ werden.** Andere Dateien, Streams und Streamtypen werden von **FSCTL \_ MOVE FILE nicht \_ unterstützt.**

Für jede Datei oder jedes Verzeichnis unterstützte Streamtypen.

-   ::$DATA
-   ::$ATTRIBUTE \_ LIST
-   ::$REPARSE \_ POINT
-   ::$EA
-   ::$LOGGED \_ UTILITY \_ STREAM

**Windows 7, Windows Server 2008 R2, Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP: **::$EA und ::$LOGGED UTILITY STREAM werden vor Windows 8 und \_ \_ Windows Server 2012

Für jedes Verzeichnis unterstützte Streamtypen.

-   ::$BITMAP
-   ::$INDEX \_ ALLOCATION

Im Folgenden finden Sie die Systemdatei-, Stream- und Streamtypen, die von [**FSCTL \_ MOVE \_ FILE**](/windows/win32/api/winioctl/ni-winioctl-fsctl_move_file) im Format *"Dateiname:**Streamname*:$*Typname"* unterstützt werden.

-   $MFT::$DATA
-   $MFT::$ATTRIBUTE \_ LIST
-   $MFT::$BITMAP
-   $AttrDef::$DATA
-   $AttrDef::$ATTRIBUTE \_ LIST
-   $Secure:$SDS:$DATA
-   $Secure::$ATTRIBUTE \_ LIST
-   $Secure:$SDH:$INDEX \_ ALLOCATION
-   $Secure:$SDH:$BITMAP
-   $Secure:$SII:$INDEX \_ ALLOCATION
-   $Secure:$SII:$BITMAP
-   $UpCase::$DATA
-   $UpCase::$ATTRIBUTE \_ LIST
-   $Extend:$I 30:$INDEX \_ ALLOCATION
-   $Extend::$ATTRIBUTE \_ LIST
-   $Extend:$I 30:$BITMAP
-   $Extend \\ $UsnJrnl:$J:$DATA
-   $Extend \\ $UsnJrnl::$ATTRIBUTE \_ LIST
-   $Extend \\ $UsnJrnl:$Max:$DATA
-   $Extend \\ $Quota:$Q:$INDEX \_ ALLOCATION
-   $Extend \\ $Quota::$ATTRIBUTE \_ LIST
-   $Extend \\ $Quota:$Q:$BITMAP
-   $Extend \\ $Quota:$O:$INDEX \_ ALLOCATION
-   $Extend \\ $Quota:$O:$BITMAP
-   $Extend \\ $ObjId:$O:$INDEX \_ ALLOCATION
-   $Extend \\ $ObjId::$ATTRIBUTE LISTE \_
-   $Extend \\ $ObjId:$O:$BITMAP
-   $Extend \\ $Reparse:$R:$INDEX \_ ALLOCATION
-   $Extend \\ $Reparse::$ATTRIBUTE \_ LIST
-   $Extend \\ $Reparse:$R:$BITMAP
-   $Extend \\ $RmMetadata:$I 30:$INDEX \_ ALLOCATION
-   $Extend \\ $RmMetadata:$I 30:$BITMAP
-   $Extend \\ $RmMetadata::$ATTRIBUTE \_ LIST
-   $Extend $RmMetadata \\ \\ $Repair::$DATA
-   $Extend $RmMetadata \\ \\ $Repair::$ATTRIBUTE \_ LIST
-   $Extend $RmMetadata \\ \\ $Repair:$Config:$DATA
-   $Extend $RmMetadata \\ \\ $Txf:$I 30:$INDEX \_ ALLOCATION
-   $Extend $RmMetadata \\ \\ $Txf::$ATTRIBUTE \_ LIST
-   $Extend \\ $RmMetadata \\ $Txf:$I 30:$BITMAP
-   $Extend $RmMetadata \\ \\ $Txf:$TXF \_ DATA:$LOGGED \_ UTILITY \_ STREAM
-   $Extend $RmMetadata \\ \\ $TxfLog:$I 30:$INDEX \_ ALLOCATION
-   $Extend \\ $RmMetadata \\ $TxfLog::$ATTRIBUTE \_ LIST
-   $Extend $RmMetadata \\ \\ $TxfLog:$I 30:$BITMAP
-   $Extend $RmMetadata \\ \\ $TxfLog \\ $Tops::$DATA
-   $Extend \\ $RmMetadata $TxfLog \\ \\ $Tops::$ATTRIBUTE LISTE \_
-   $Extend $RmMetadata \\ \\ $TxfLog \\ $Tops:$T:$DATA
-   $Extend \\ $RmMetadata $TxfLog \\ \\ $TxfLog.blf::$DATA
-   $Extend $RmMetadata \\ \\ $TxfLog \\ $TxfLog.blf::$ATTRIBUTE \_ LIST

 

 
