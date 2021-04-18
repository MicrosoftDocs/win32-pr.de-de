---
description: Bestimmen Sie, ob ein Dateisystem sparsesdateien unterstützt, indem Sie die GetVolumeInformation-Funktion aufrufen.
ms.assetid: a08f6bbc-c139-4396-8964-4aa63285f3f5
title: Vorgänge mit geringer Dichte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c23d26fc1c52db32ca7674aec2fc487a826e9a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357378"
---
# <a name="sparse-file-operations"></a>Vorgänge mit geringer Dichte

Um zu ermitteln, ob ein Dateisystem sparsesdateien unterstützt, können Sie die [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) -Funktion aufrufen und untersuchen, dass das Bitflag für die Datei mit geringer Dichte durch den *lpfilesystemflags* -Parameter **\_ \_ \_**

Bei den meisten Anwendungen werden Dateien mit geringer Dichte nicht beachtet, und es werden keine sparsesdateien erstellt. Die Tatsache, dass eine Anwendung eine sparsedatei liest, ist für die Anwendung transparent. Eine Anwendung, die sparsedateien kennt, sollte ermitteln, ob das Dataset für die Aufbewahrung in einer sparsedatei geeignet ist. Nachdem diese Bestimmung festgelegt wurde, muss die Anwendung eine Datei explizit als Sparse deklarieren, indem Sie den Code für die [**\_ \_ sparsespalte**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_sparse) mit geringer Dichte verwendet.

Nachdem eine Anwendung eine Datei als Sparse festgelegt hat, kann die Anwendung den [**FSCTL- \_ \_ \_ Daten Steuerungs Code Set Zero (null**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data) ) verwenden, um einen Bereich der Datei auf 0 (null) festzulegen. Darüber hinaus kann die Anwendung den Code der [**\_ \_ zugeordneten \_ Bereiche der FSCTL-Abfrage**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_allocated_ranges) verwenden, um die Suche nach Daten, die nicht NULL sind, in der sparsedatei zu beschleunigen.

Wenn Sie einen Schreibvorgang ausführen (mit einer Funktion oder einem anderen Vorgang als [**FSCTL \_ Set \_ zero \_ Data**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data)), deren Daten aus nur Nullen bestehen, werden Nullen für die gesamte Länge des Schreibvorgangs auf den Datenträger geschrieben. Verwenden Sie **FSCTL \_ Set \_ zero \_ Data**, um einen Bereich der Datei zu 0 (null) zu verwenden und die geringe Dichte beizubehalten.

Eine sparsesatfähige Anwendung kann auch eine vorhandene Datei als Sparse festlegen. Wenn eine Anwendung eine vorhandene Datei als sparsespalte festlegt, sollte Sie die Datei für Regionen mit Nullen scannen. verwenden Sie [**FSCTL \_ Set \_ zero \_ Data**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data) zum Zurücksetzen dieser Regionen, um die Zuordnung von physischem Speicherplatz zu verringern. Eine Anwendung, die auf die Erkennung von Daten mit geringer Dichte aktualisiert wurde, sollte diese Konvertierung

Wenn Sie einen Lesevorgang aus einem Teil einer Datei mit geringer Dichte ausführen, wird vom Betriebssystem möglicherweise kein Lesevorgang von der Festplatte ausgeführt. Stattdessen erkennt das System, dass der Teil der zu lesenden Datei Nullen enthält, und gibt einen Puffer ohne Nullen zurück, ohne tatsächlich vom Datenträger zu lesen.

Wie bei jeder anderen Datei kann das Systemdaten in eine Datei mit geringer Dichte schreiben oder von jeder beliebigen Position aus Daten lesen. Daten, die nicht 0 (null) sind, werden in einen zuvor Nullen Teil der Datei geschrieben. Dies kann zu Speicherplatz Belegung führen. Nullen, die über Daten ungleich 0 (null) geschrieben werden (nur bei der Verwendung von [**\_ NULL- \_ \_ Daten**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data)), können dazu führen, dass der Speicherplatz freigegeben wird.

> [!Note]  
> Es ist von der Anwendung bis zur Aufrechterhaltung der geringer Dichte, indem Nullen mit [**FSCTL \_ Set \_ zero \_ Data**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data)geschrieben werden.

 

Defragmentierungs Tools, die komprimierte Dateien auf NTFS-Dateisystemen verarbeiten, behandeln Dateien mit geringer Dichte auf NTFS-Dateisystemvolumes ordnungsgemäß. Große und hochgradig fragmentierte sparsesdateien können die NTFS-Einschränkung auf Datenträger Blöcken überschreiten, bevor der verfügbare Speicherplatz verwendet wird. Weitere Informationen finden Sie unter das [Erweitern einer Datei schlägt möglicherweise mit dem Fehler "Disk Full" fehl, auch wenn das Volume über freien Speicherplatz verfügt](https://support.microsoft.com/default.aspx/kb/957180).

 

 
