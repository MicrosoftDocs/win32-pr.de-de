---
description: Defragmentierung ist der Prozess, bei dem Teile von Dateien auf einem Datenträger verschoben werden, um Dateien zu defragmentieren, d. h. der Prozess des Verschiebens von Datei Clustern auf einem Datenträger, um Sie zusammenhängend zu machen.
ms.assetid: 27ccaab7-ec89-489b-80dc-df9beb7969bc
title: Defragmentieren von Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b2d079f58ec98f320356a477531616788f84ccb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863884"
---
# <a name="defragmenting-files"></a>Defragmentieren von Dateien

Wenn eine Datei auf einen Datenträger geschrieben wird, kann die Datei manchmal nicht in zusammenhängenden Clustern geschrieben werden. Nicht zusammenhängende Cluster verlangsamen den Lese-und Schreibvorgang einer Datei. Je mehr auf einem Datenträger die nicht zusammenhängenden Cluster sind, desto schlechter ist das Problem, weil die Zeit zum Verschieben des Lese-/Schreibkopfes eines Festplatten Laufwerks benötigt wird. Eine Datei mit nicht zusammenhängenden Clustern ist *fragmentiert*. Um Dateien für den schnellen Zugriff zu optimieren, kann ein Volume defragmentiert werden.

*Defragmentierung* ist der Prozess, bei dem Teile von Dateien auf einem Datenträger verschoben werden, um Dateien zu defragmentieren, d. h. der Prozess des Verschiebens von Datei Clustern auf einem Datenträger, um Sie zusammenhängend zu machen. Weitere Informationen finden Sie in den folgenden Abschnitten:

-   [Defragmentieren einer Datei](#defragmenting-a-file)
-   [Minimieren von Interaktionen zwischen Defragmentierung und Schatten Kopien](#minimizing-interactions-between-defragmentation-and-shadow-copies)
-   [Dateien, Streams und Streamtypen, die für die Defragmentierung unterstützt werden](#files-streams-and-stream-types-supported-for-defragmentation)

## <a name="defragmenting-a-file"></a>Defragmentieren einer Datei

In einem einfachen Single-Tasking-Betriebssystem ist die Defragmentierungssoftware die einzige Aufgabe, und es gibt keine anderen Prozesse, die vom Datenträger gelesen oder geschrieben werden können. In einem Multitasking-Betriebssystem können jedoch einige Prozesse von einer Festplatte lesen und auf diese schreiben, während ein anderer Prozess das Festplattenlaufwerk defragmentiert. Der Trick besteht darin, Schreibvorgänge in eine Datei zu vermeiden, die defragmentiert wird, ohne den Schreibvorgang für sehr lange Zeit zu beenden. Das lösen dieses Problems ist nicht trivial, aber es ist möglich.

Um die Defragmentierung zuzulassen, ohne dass detaillierte Kenntnisse einer Dateisystem-Datenträger Struktur erforderlich sind, wird ein Satz von drei Steuerungs Codes bereitgestellt. Die Steuercodes bieten die folgenden Funktionen:

-   Aktivieren von Anwendungen zum Auffinden leerer Cluster
-   Bestimmen des Speicher Orts von Datei Clustern
-   Verschieben von Clustern auf einem Datenträger

Die Steuerungs Codes behandeln außerdem transparent das Problem, dass andere Prozesse während der Verschiebung aus Dateien lesen und in Dateien schreiben können.

Diese Vorgänge können ausgeführt werden, ohne dass andere Prozesse ausgeführt werden. Die anderen Prozesse haben jedoch langsamere Reaktionszeiten, während ein Laufwerk defragmentiert wird.

**So defragmentieren Sie eine Datei**

1.  Verwenden Sie den Code für das [**FSCTL- \_ \_ Volume \_ Bitmap**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_volume_bitmap) -Steuerelement, um einen Speicherort auf dem Volume zu finden, der groß genug ist, um eine gesamte Datei zu akzeptieren
    > [!Note]  
    > Verschieben Sie ggf. andere Dateien, um einen Platz zu schaffen, der groß genug ist. Im Idealfall sind nach dem ersten Block der Datei genügend nicht zugewiesene Cluster vorhanden, die nachfolgende Blöcke nach dem ersten Block in den Raum verschieben können.

     

2.  Verwenden Sie den Code zum [**\_ Abrufen von \_ Abruf \_ Zeigern für FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_retrieval_pointers) , um eine Zuordnung des aktuellen Layouts der Datei auf dem Datenträger zu erhalten.
3.  Durchlaufen Sie die [**\_ \_ Puffer Struktur für Abruf Zeiger**](/windows/desktop/api/WinIoCtl/ns-winioctl-retrieval_pointers_buffer) , die von den "f"- [**\_ \_ Abruf \_ Zeigern abgerufen**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_retrieval_pointers)wurde
4.  Verwenden Sie den [**FSCTL-Code zum \_ Verschieben von \_ Dateien**](/windows/win32/api/winioctl/ni-winioctl-fsctl_move_file) , um die einzelnen Cluster beim Durchlaufen der Struktur zu verschieben.
    > [!Note]  
    > Möglicherweise müssen Sie entweder die Bitmap oder die Abruf Struktur oder beides zu verschiedenen Zeitpunkten erneuern, da andere Prozesse auf den Datenträger schreiben.

     

Zwei der Vorgänge, die im Defragmentierungs Prozess verwendet werden, erfordern ein Handle für ein Volume. Nur Administratoren können ein Handle für ein Volume abrufen, sodass nur Administratoren ein Volume zerlegen können. Eine Anwendung sollte die Rechte eines Benutzers überprüfen, der versucht, Defragmentierungssoftware auszuführen, und einem Benutzer nicht gestatten, ein Volume zu defragmentieren, wenn der Benutzer nicht über die entsprechenden Rechte verfügt.

Wenn Sie zum Öffnen eines Verzeichnisses während der Defragmentierung eines FAT-oder FAT32-Dateisystem Volumes das Verzeichnis "Defragmentierung [**" verwenden,**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) geben Sie den Wert der **generischen \_ Lese** Zugriffs Maske an. Geben Sie nicht den Wert für die **maximal \_ zulässige** Zugriffs Maske an. Der Zugriff auf das Verzeichnis wird verweigert, wenn dies geschehen ist.

Versuchen Sie nicht, zugeordnete Cluster in einem NTFS-Dateisystem zu verschieben, das über die Größe der gerundeten Cluster Dateien hinausgeht, da das Ergebnis ein Fehler ist.

Die erneute Analyse von Punkten, Bitmaps und Attribut Listen in NTFS-Dateisystemvolumes kann defragmentiert, zum Lesen und Synchronisieren geöffnet und mit der Syntax " *File*:*Name*:*Type* " benannt werden. beispielsweise *dirname*: $i 30: $Index \_ Allocation, *maschinenlesbarer Pass*:: $Data, *maschinenlesbarer Pass*:: $REPARSE \_ Point und *maschinenlesbarer Pass*:: $Attribute \_ List.

Beim Defragmentieren von NTFS-Dateisystemvolumes ist das Defragmentieren eines virtuellen Clusters über die Zuordnungs Größe einer Datei hinaus zulässig.

## <a name="minimizing-interactions-between-defragmentation-and-shadow-copies"></a>Minimieren von Interaktionen zwischen Defragmentierung und Schatten Kopien

Verschieben Sie nach Möglichkeit Daten in Blöcke, die relativ zueinander ausgerichtet sind, in Schritten von 16 Kilobyte (KB). Dies reduziert den Kopier Aufwand bei aktiviertem Schatten Kopien, da der Schattenkopiebereich zunimmt und die Leistung reduziert wird, wenn die folgenden Bedingungen eintreten:

-   Die Blockgröße der Verschiebungs Anforderung ist kleiner als oder gleich 16 KB.
-   Das Verschiebungs Delta liegt nicht in Schritten von 16 KB.

Das Verschiebungs Delta entspricht der Anzahl von Bytes zwischen dem Start des Quell Blocks und dem Anfang des zielblocks. Anders ausgedrückt: ein Block, der bei Offset x (auf der Festplatte) beginnt, kann in den Start Offset Y verschoben werden, wenn der absolute Wert von X minus Y ein gleich Vielfaches von 16 KB ist. Daher wird bei 4-KB-Clustern eine Umstellung von Cluster 3 auf Cluster 27 optimiert, aber eine Umstellung von Cluster 18 auf Cluster 24 ist nicht durchgesetzt. Beachten Sie, dass mod (3, 4) = 3 = mod (27, 4). Mod 4 wird ausgewählt, da vier Cluster mit jeweils 4 KB mit 16 KB übereinstimmt. Daher führt ein Volume, das mit einer Clustergröße von 16 KB formatiert ist, dazu, dass alle Verschiebungs Dateien optimiert werden.

Weitere Informationen zu Schatten Kopien finden Sie unter [Volumeschattenkopie-Dienst](/windows/desktop/VSS/about-the-volume-shadow-copy-service).

## <a name="files-streams-and-stream-types-supported-for-defragmentation"></a>Dateien, Streams und Streamtypen, die für die Defragmentierung unterstützt werden

Obwohl die meisten Dateien mithilfe des Datei Steuerungs Codes der [**\_ Datei " \_ Datei verschieben**](/windows/win32/api/winioctl/ni-winioctl-fsctl_move_file) " verschoben werden können, können nicht alle Elemente verschoben werden. Im folgenden finden Sie eine Liste der Dateien, Streams und Streamtypen (auch als Attributtyp Codes bezeichnet), die von der **FSCTL-Verschiebungs \_ \_ Datei** unterstützt werden Andere Dateien, Streams und Streamtypen werden von der **\_ \_ Datei zum Verschieben** von Dateien nicht unterstützt.

Streamtypen werden für jede Datei oder jedes Verzeichnis unterstützt.

-   :: $Data
-   :: $Attribute \_ Liste
-   :: $REPARSE \_ Punkt
-   :: $EA
-   :: $Logged \_ Utility- \_ Stream

* * Windows 7, Windows Server 2008 R2, Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP: * *:: $EA und:: $Logged \_ Utility-Daten \_ Strom werden vor Windows 8 und Windows Server 2012 nicht unterstützt.

Streamtypen werden für jedes Verzeichnis unterstützt.

-   :: $Bitmap
-   :: $Index \_ Zuordnung

Im folgenden sind die Datei-, Datenstrom-und Streamtypen von Dateien aufgeführt, die von der [**\_ \_ Datei**](/windows/win32/api/winioctl/ni-winioctl-fsctl_move_file) "*Dateiname*:*streamName*: $*tykename*" unterstützt werden.

-   $MFT:: $Data
-   $MFT:: $Attribute \_ Liste
-   $MFT:: $Bitmap
-   $AttrDef:: $Data
-   $AttrDef:: $Attribute \_ Liste
-   $Secure: $SDS: $Data
-   $Secure:: $Attribute \_ Liste
-   $Secure: $SDH: $Index \_ Zuordnung
-   $Secure: $SDH: $Bitmap
-   $Secure: $SII: $Index \_ Zuordnung
-   $Secure: $SII: $Bitmap
-   $UpCase:: $Data
-   $UpCase:: $Attribute \_ Liste
-   $Extend: $I 30: $Index \_ Zuordnung
-   $Extend:: $Attribute \_ Liste
-   $Extend: $I 30: $Bitmap
-   $Extend \\ $UsnJrnl: $J: $Data
-   $Extend \\ $UsnJrnl:: $Attribute \_ Liste
-   $Extend \\ $UsnJrnl: $Max: $Data
-   $Extend \\ $quota: $Q: $Index \_ Zuordnung
-   $Extend \\ $quota:: $Attribute \_ Liste
-   $Extend \\ $quota: $Q: $Bitmap
-   $Extend \\ $quota: $O: $Index \_ Zuordnung
-   $Extend \\ $quota: $O: $Bitmap
-   $Extend \\ $objID: $O: $Index \_ Zuordnung
-   $Extend \\ $objID:: $Attribute \_ Liste
-   $Extend \\ $objID: $O: $Bitmap
-   $Extend \\ $Reparse: $R: $Index \_ Zuordnung
-   $Extend \\ $Reparse:: $Attribute \_ Liste
-   $Extend \\ $Reparse: $R: $Bitmap
-   $Extend \\ $RmMetadata: $I 30: $Index \_ Zuordnung
-   $Extend \\ $RmMetadata: $I 30: $Bitmap
-   $Extend \\ $RmMetadata:: $Attribute \_ Liste
-   $Extend \\ $RmMetadata \\ $Repair:: $Data
-   $Extend \\ $RmMetadata \\ $Repair:: $Attribute \_ Liste
-   $Extend \\ $RmMetadata \\ $Repair: $config: $Data
-   $Extend \\ $RmMetadata \\ $TxF: $I 30: $Index \_ Zuordnung
-   $Extend \\ $RmMetadata \\ $TxF:: $Attribute \_ Liste
-   $Extend \\ $RmMetadata \\ $TxF: $I 30: $Bitmap
-   $Extend \\ $RmMetadata \\ $TxF: $TxF \_ Daten: $Logged \_ Utility \_ Stream
-   $Extend \\ $RmMetadata \\ $TxfLog: $I 30: $Index \_ Zuordnung
-   $Extend \\ $RmMetadata \\ $TxfLog:: $Attribute \_ Liste
-   $Extend \\ $RmMetadata \\ $TxfLog: $I 30: $Bitmap
-   $Extend \\ $RmMetadata \\ $TxfLog \\ $Tops:: $Data
-   $Extend \\ $RmMetadata \\ $TxfLog \\ $Tops:: $Attribute \_ Liste
-   $Extend \\ $RmMetadata \\ $TxfLog \\ $Tops: $T: $Data
-   $Extend \\ $RmMetadata \\ $TxfLog \\ $TxfLog. BLF:: $Data
-   $Extend \\ $RmMetadata \\ $TxfLog \\ $TxfLog. BLF:: $Attribute \_ Liste

 

 
