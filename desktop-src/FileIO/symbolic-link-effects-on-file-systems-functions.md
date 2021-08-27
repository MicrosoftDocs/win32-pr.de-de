---
description: Wie symbolische Verknüpfungen sich auf Standarddateifunktionen auswirken, die Pfadnamen verwenden, um eine oder mehrere Dateien anzugeben.
ms.assetid: afda53eb-d0db-4844-9dd0-8a7d93ca341f
title: Symbolische Verknüpfungseffekte für Dateisystemfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e1c5d140dc70de8ebc255b779b226b6da156aa2b8961c49d86f466ac01b26ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078455"
---
# <a name="symbolic-link-effects-on-file-systems-functions"></a>Symbolische Verknüpfungseffekte für Dateisystemfunktionen

Mehrere Standarddateifunktionen, die Pfadnamen verwenden, um eine oder mehrere Dateien anzugeben, sind von der Verwendung symbolischer Verknüpfungen betroffen. In diesem Thema werden diese Funktionen aufgeführt und die Verhaltensänderungen beschrieben:

-   [CopyFile und CopyFileTransacted](#copyfile-and-copyfiletransacted)
-   [CopyFileEx](#copyfileex)
-   [CreateFile und CreateFileTransacted](#createfile-and-createfiletransacted)
-   [CreateHardLink und CreateHardLinkTransacted](#createhardlink-and-createhardlinktransacted)
-   [DeleteFile und DeleteFileTransacted](#deletefile-and-deletefiletransacted)
-   [FindFirstChangeNotification](#findfirstchangenotification)
-   [FindFirstFile und FindFirstFileTransacted](#findfirstfile-and-findfirstfiletransacted)
-   [FindFirstFileEx](#findfirstfileex)
-   [FindNextFile](#findnextfile)
-   [GetBinaryType](#getbinarytype)
-   [GetCompressedFileSize und GetCompressedFileSizeTransacted](#getcompressedfilesize-and-getcompressedfilesizetransacted)
-   [GetDiskFreeSpace](#getdiskfreespaceex)
-   [Getdiskfreespaceex](#getdiskfreespaceex)
-   [GetFileAttributes](#getfileattributesex)
-   [GetFileAttributesEx](#getfileattributesex)
-   [GetFileSecurity](#getfilesecurity)
-   [GetTempPath](#gettemppath)
-   [GetVolumeInformation](#getvolumeinformation)
-   [SetFileAttributes](#setfileattributes)
-   [SetFileSecurity](#setfilesecurity)
-   [Zugehörige Themen](#related-topics)

In den folgenden Beschreibungen werden die folgenden Begriffe verwendet:

-   Quelldatei– Die ursprüngliche Datei, die kopiert werden soll.
-   Zieldatei– Die neu erstellte Kopie der Datei.
-   Ziel: Die Entität, auf die ein symbolischer Link zeigt.

> [!Note]  
> Das Verhalten von Funktionen, die ein handle akzeptieren, das mit der [**CreateFile-Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) erstellt wurde, z. B. die [**GetFileTime-Funktion,**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime) unterscheidet sich je nach Dem, ob die **CreateFile-Funktion** mit dem **FILE FLAG OPEN \_ \_ \_ REPARSE \_ POINT-Flag** aufgerufen wurde. Weitere Informationen finden Sie unter [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) und im folgenden [Abschnitt CreateFile und CreateFileTransacted.](#createfile-and-createfiletransacted)

 

## <a name="copyfile-and-copyfiletransacted"></a>CopyFile und CopyFileTransacted

Wenn die Quelldatei ein symbolischer Link ist, ist die tatsächlich kopierte Datei das Ziel der symbolischen Verknüpfung.

Wenn die Zieldatei bereits vorhanden ist und eine symbolische Verknüpfung ist, wird die symbolische Verknüpfung von der Quelldatei überschrieben.

## <a name="copyfileex"></a>CopyFileEx

Wenn **COPY FILE COPY \_ \_ \_ SYMLINK** angegeben ist, und:

-   Wenn es sich bei der Quelldatei um eine symbolische Verknüpfung handelt, wird die symbolische Verknüpfung kopiert, nicht die Zieldatei.
-   Wenn es sich bei der Quelldatei nicht um eine symbolische Verknüpfung handelt, ändert sich das Verhalten nicht.
-   Wenn es sich bei der Zieldatei um eine vorhandene symbolische Verknüpfung handelt, wird die symbolische Verknüpfung überschrieben, nicht die Zieldatei.
-   Wenn **COPY \_ FILE \_ \_ FAIL, wenn \_ EXISTS** ebenfalls angegeben ist und die Zieldatei eine vorhandene symbolische Verknüpfung ist, schlägt der Vorgang in allen Fällen fehl.

Wenn **COPY FILE COPY \_ \_ \_ SYMLINK** nicht angegeben ist, und:

-   Wenn **COPY \_ FILE \_ \_ FAIL, wenn \_ EXISTS** ebenfalls angegeben ist und die Zieldatei eine vorhandene symbolische Verknüpfung ist, schlägt der Vorgang nur fehl, wenn das Ziel der symbolischen Verknüpfung vorhanden ist.
-   Wenn **COPY \_ FILE \_ \_ FAIL, wenn \_ EXISTS** nicht angegeben ist, ändert sich das Verhalten nicht.

**Windows Server 2003 und Windows XP:** Das **COPY FILE COPY \_ \_ \_ SYMLINK-Flag** wird nicht unterstützt. Wenn die Quelldatei ein symbolischer Link ist, ist die tatsächlich kopierte Datei das Ziel der symbolischen Verknüpfung.

## <a name="createfile-and-createfiletransacted"></a>CreateFile und CreateFileTransacted

Wenn durch den Aufruf dieser Funktion eine neue Datei erstellt wird, ändert sich das Verhalten nicht.

Wenn **FILE FLAG OPEN \_ \_ \_ REPARSE \_ POINT** angegeben ist, und:

-   Wenn eine vorhandene Datei geöffnet wird und es sich um eine symbolische Verknüpfung handelt, ist das zurückgegebene Handle ein Handle für die symbolische Verknüpfung.
-   Wenn **CREATE \_ ALWAYS,** **TRUNCATE \_ EXISTING** oder **FILE FLAG DELETE ON \_ \_ \_ \_ CLOSE** angegeben wird, ist die betroffene Datei eine symbolische Verknüpfung.

Wenn **FILE FLAG OPEN \_ \_ \_ REPARSE \_ POINT** nicht angegeben ist, und:

-   Wenn eine vorhandene Datei geöffnet wird und es sich um eine symbolische Verknüpfung handelt, ist das zurückgegebene Handle ein Handle für das Ziel.
-   Wenn **CREATE \_ ALWAYS,** **TRUNCATE \_ EXISTING** oder **FILE FLAG DELETE ON \_ \_ \_ \_ CLOSE** angegeben wird, ist die betroffene Datei das Ziel.

## <a name="createhardlink-and-createhardlinktransacted"></a>CreateHardLink und CreateHardLinkTransacted

Wenn der Pfad auf eine symbolische Verknüpfung verweist, erstellt die Funktion eine harte Verknüpfung mit dem Ziel.

## <a name="deletefile-and-deletefiletransacted"></a>DeleteFile und DeleteFileTransacted

Wenn der Pfad auf eine symbolische Verknüpfung verweist, wird die symbolische Verknüpfung gelöscht, nicht das Ziel. Um ein Ziel zu löschen, müssen Sie [**CreateFile aufrufen**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) und **FILE FLAG DELETE ON CLOSE \_ \_ \_ \_ angeben.**

## <a name="findfirstchangenotification"></a>FindFirstChangeNotification

Wenn der Pfad auf eine symbolische Verknüpfung verweist, wird das Benachrichtigungshand handle für das Ziel erstellt. Wenn sich eine Anwendung für den Empfang von Änderungsbenachrichtigungen für ein Verzeichnis registriert hat, das symbolische Verknüpfungen enthält, wird die Anwendung nur benachrichtigt, wenn die symbolischen Verknüpfungen geändert wurden, nicht die Zieldateien.

## <a name="findfirstfile-and-findfirstfiletransacted"></a>FindFirstFile und FindFirstFileTransacted

Wenn der Pfad auf eine symbolische Verknüpfung verweist, enthält der [**WIN32 \_ FIND \_ DATA-Puffer**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) Informationen über die symbolische Verknüpfung, nicht über das Ziel.

## <a name="findfirstfileex"></a>FindFirstFileEx

Wenn der Pfad auf eine symbolische Verknüpfung verweist, enthält der [**WIN32 \_ FIND \_ DATA-Puffer**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) Informationen über die symbolische Verknüpfung, nicht über das Ziel.

## <a name="findnextfile"></a>FindNextFile

Wenn der Pfad auf eine symbolische Verknüpfung verweist, enthält der [**WIN32 \_ FIND \_ DATA-Puffer**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) Informationen über die symbolische Verknüpfung, nicht über das Ziel.

## <a name="getbinarytype"></a>GetBinaryType

Wenn der Pfad auf eine symbolische Verknüpfung verweist, wird die Zieldatei verwendet.

## <a name="getcompressedfilesize-and-getcompressedfilesizetransacted"></a>GetCompressedFileSize und GetCompressedFileSizeTransacted

Wenn der Pfad auf eine symbolische Verknüpfung zeigt, gibt die Funktion die Dateigröße des Ziels zurück.

## <a name="getdiskfreespace"></a>GetDiskFreeSpace

Wenn der Pfad auf eine symbolische Verknüpfung verweist, wird der Vorgang auf dem Ziel ausgeführt.

## <a name="getdiskfreespaceex"></a>Getdiskfreespaceex

Wenn der Pfad auf eine symbolische Verknüpfung verweist, wird der Vorgang auf dem Ziel ausgeführt.

## <a name="getfileattributes"></a>GetFileAttributes

Wenn der Pfad auf eine symbolische Verknüpfung zeigt, gibt die Funktion Attribute für die symbolische Verknüpfung zurück.

## <a name="getfileattributesex"></a>GetFileAttributesEx

Wenn der Pfad auf eine symbolische Verknüpfung zeigt, gibt die Funktion Attribute für die symbolische Verknüpfung zurück.

## <a name="getfilesecurity"></a>GetFileSecurity

Wenn der Pfad auf eine symbolische Verknüpfung zeigt, gibt die Funktion Attribute für die symbolische Verknüpfung zurück.

## <a name="gettemppath"></a>GetTempPath

Wenn der Pfad auf eine symbolische Verknüpfung verweist, behält der Name des temporären Pfads alle symbolischen Verknüpfungen bei.

## <a name="getvolumeinformation"></a>GetVolumeInformation

Wenn der Pfad auf eine symbolische Verknüpfung zeigt, gibt die Funktion Volumeinformationen für das Ziel zurück.

## <a name="setfileattributes"></a>SetFileAttributes

Wenn der Pfad auf eine symbolische Verknüpfung zeigt, ruft die Funktion Attribute für die symbolische Verknüpfung ab.

## <a name="setfilesecurity"></a>SetFileSecurity

Wenn der Pfad auf eine symbolische Verknüpfung zeigt, gibt die Funktion Attribute für die symbolische Verknüpfung zurück.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile)
</dt> <dt>

[**CopyFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-copyfiletransacteda)
</dt> <dt>

[**CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa)
</dt> <dt>

[**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda)
</dt> <dt>

[**CreateHardLink**](/windows/desktop/api/WinBase/nf-winbase-createhardlinka)
</dt> <dt>

[**CreateHardLinkTransacted**](/windows/desktop/api/WinBase/nf-winbase-createhardlinktransacteda)
</dt> <dt>

[**DeleteFile**](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea)
</dt> <dt>

[**DeleteFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-deletefiletransacteda)
</dt> <dt>

[**FindFirstChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa)
</dt> <dt>

[**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea)
</dt> <dt>

[**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa)
</dt> <dt>

[**FindFirstFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-findfirstfiletransacteda)
</dt> <dt>

[**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)
</dt> <dt>

[**GetBinaryType**](/windows/desktop/api/WinBase/nf-winbase-getbinarytypea)
</dt> <dt>

[**GetCompressedFileSize**](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea)
</dt> <dt>

[**GetCompressedFileSizeTransacted**](/windows/desktop/api/WinBase/nf-winbase-getcompressedfilesizetransacteda)
</dt> <dt>

[**GetDiskFreeSpace**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespacea)
</dt> <dt>

[**Getdiskfreespaceex**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespaceexa)
</dt> <dt>

[**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa)
</dt> <dt>

[**GetFileAttributesEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa)
</dt> <dt>

[**GetFileSecurity**](/windows/desktop/api/winbase/nf-winbase-getfilesecuritya)
</dt> <dt>

[**GetTempPath**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha)
</dt> <dt>

[**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa)
</dt> <dt>

[**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa)
</dt> <dt>

[**SetFileSecurity**](/windows/desktop/api/winbase/nf-winbase-setfilesecuritya)
</dt> </dl>

 

 
