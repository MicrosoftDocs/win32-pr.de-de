---
description: Bestimmen Sie, ob ein Dateisystem Sparsedateien unterstützt, indem Sie die GetVolumeInformation-Funktion aufrufen.
ms.assetid: a08f6bbc-c139-4396-8964-4aa63285f3f5
title: Dateivorgänge mit geringer Dichte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9835d550a414c047e578eb90fc9b55afbefb760d31d8333a290f00da7162f839
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015108"
---
# <a name="sparse-file-operations"></a>Dateivorgänge mit geringer Dichte

Um zu bestimmen, ob ein Dateisystem Sparsedateien unterstützt, rufen Sie die [**GetVolumeInformation-Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) auf, und untersuchen Sie das Bitflag **FILE SUPPORTS \_ \_ SPARSE \_ FILES,** das über den *lpFileSystemFlags-Parameter* zurückgegeben wird.

Die meisten Anwendungen kennen Sparsedateien nicht und erstellen keine Sparsedateien. Die Tatsache, dass eine Anwendung eine Sparsedatei liest, ist für die Anwendung transparent. Eine Anwendung, die sparse-files kennt, sollte bestimmen, ob ihr Dataset für die Speicherung in einer Sparsedatei geeignet ist. Nachdem diese Bestimmung getroffen wurde, muss die Anwendung eine Datei mithilfe des [**FSCTL \_ SET \_ SPARSE-Steuerungscodes**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_sparse) explizit als Sparse deklarieren.

Nachdem eine Anwendung eine Datei mit geringer Dichte festgelegt hat, kann die Anwendung den [**FSCTL \_ SET ZERO \_ DATA-Steuerungscode \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data) verwenden, um einen Bereich der Datei auf 0 (null) festzulegen. Darüber hinaus kann die Anwendung den [**STEUERUNGscode FSCTL \_ QUERY ALLOCATED \_ \_ RANGES**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_allocated_ranges) verwenden, um Suchvorgänge für Daten ungleich 0 (null) in der Sparsedatei zu beschleunigen.

Wenn Sie einen Schreibvorgang (mit einer anderen Funktion oder einem anderen Vorgang als [**FSCTL \_ SET ZERO \_ \_ DATA)**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data)ausführen, dessen Daten nur aus Nullen bestehen, werden Nullen für die gesamte Länge des Schreibvorgangs auf den Datenträger geschrieben. Verwenden Sie **FSCTL \_ SET ZERO \_ \_ DATA,** um einen Bereich der Datei auf null zu setzen und die Sparsese zu gewährleisten.

Eine Anwendung mit geringer Dichte kann auch eine vorhandene Datei als sparse festlegen. Wenn eine Anwendung eine vorhandene Datei als sparse festlegt, sollte sie die Datei auf Regionen überprüfen, die Nullen enthalten, und [**FSCTL \_ SET ZERO \_ \_ DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data) verwenden, um diese Regionen zurückzusetzen, wodurch möglicherweise die Suche nach physischem Datenträgerspeicher eingestellt wird. Eine Anwendung, die auf Dateierkennung mit geringer Dichte aktualisiert wurde, sollte diese Konvertierung durchführen.

Wenn Sie einen Lesevorgang aus einem nicht entfernten Teil einer Sparsedatei ausführen, liest das Betriebssystem möglicherweise nicht von der Festplatte. Stattdessen erkennt das System, dass der zu lesende Teil der Datei Nullen enthält, und gibt einen Puffer mit Nullen zurück, ohne tatsächlich vom Datenträger zu lesen.

Wie bei jeder anderen Datei kann das System Daten in eine Datei mit geringer Dichte schreiben oder Daten von einer beliebigen Position aus lesen. Daten ohne 0 (null) daten, die in einen zuvor mit Null geschriebenen Teil der Datei geschrieben werden, können zur Zuordnung des Speicherplatzes führen. Nullen, die über Daten ungleich 0 (nur mit [**FSCTL \_ SET ZERO \_ \_ DATA)**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data)geschrieben werden, können zu einer Freigabe des Speicherplatzes führen.

> [!Note]  
> Es liegt an der Anwendung, die Sparseness beizubehalten, indem Nullen mit [**FSCTL \_ SET ZERO \_ \_ DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data)geschrieben werden.

 

Defragmentierungstools, die komprimierte Dateien auf NTFS-Dateisystemen verarbeiten, verarbeiten Sparsedateien auf NTFS-Dateisystemvolumes ordnungsgemäß. Große und stark fragmentierte Sparsedateien können die NTFS-Einschränkung für Datenträger-Erweiterungen überschreiten, bevor verfügbarer Speicherplatz belegt wird. Weitere Informationen finden Sie unter [Erweitern einer Datei schlägt möglicherweise mit dem Fehler "Datenträger voll" fehl, obwohl das Volume über freien Speicherplatz verfügt.](https://support.microsoft.com/default.aspx/kb/957180)

 

 
