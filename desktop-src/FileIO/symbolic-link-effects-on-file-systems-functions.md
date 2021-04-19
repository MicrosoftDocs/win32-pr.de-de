---
description: Funktionsweise von symbolischen Verknüpfungen auf Standarddatei Funktionen, die Pfadnamen verwenden, um eine oder mehrere Dateien anzugeben.
ms.assetid: afda53eb-d0db-4844-9dd0-8a7d93ca341f
title: Symbolische Verknüpfungs Effekte in Dateisystemfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d4a2fe1696bf5260a0c55ba8b6e4f107270d6da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353895"
---
# <a name="symbolic-link-effects-on-file-systems-functions"></a>Symbolische Verknüpfungs Effekte in Dateisystemfunktionen

Die Verwendung von symbolischen Verknüpfungen wirkt sich auf mehrere Standarddatei Funktionen aus, die Pfadnamen verwenden, um eine oder mehrere Dateien anzugeben. In diesem Thema werden diese Funktionen aufgelistet und die Änderungen im Verhalten beschrieben:

-   [CopyFile und copyfiletransagiert](#copyfile-and-copyfiletransacted)
-   [CopyFileEx](#copyfileex)
-   ["Kreatefile" und "kreatefiletransagiert"](#createfile-and-createfiletransacted)
-   ["Kreatehardlink" und "kreatehardlinktransagiert"](#createhardlink-and-createhardlinktransacted)
-   [DeleteFile und deletefiletranshandelten](#deletefile-and-deletefiletransacted)
-   [FindFirstChangeNotification](#findfirstchangenotification)
-   ["FindFirstFile" und "findfirstfiletransagiert"](#findfirstfile-and-findfirstfiletransacted)
-   [Findfirstfileex](#findfirstfileex)
-   [FindNextFile](#findnextfile)
-   [Getbinarytype](#getbinarytype)
-   [Getcompressedfilesize und getcompressedfilesizetranshandelten](#getcompressedfilesize-and-getcompressedfilesizetransacted)
-   [GetDiskFreeSpace](#getdiskfreespaceex)
-   [GetDiskFreeSpaceEx](#getdiskfreespaceex)
-   [GetFileAttributes](#getfileattributesex)
-   [Getfileattributesex](#getfileattributesex)
-   [Getfilesecurity](#getfilesecurity)
-   [GetTempPath](#gettemppath)
-   [GetVolumeInformation](#getvolumeinformation)
-   [Setfileattribute](#setfileattributes)
-   [Setfilesecurity](#setfilesecurity)
-   [Zugehörige Themen](#related-topics)

In den folgenden Beschreibungen werden die folgenden Begriffe verwendet:

-   Quelldatei – die ursprüngliche Datei, die kopiert werden soll.
-   Zieldatei – die neu erstellte Kopie der Datei.
-   Target – die Entität, auf die ein symbolischer Link verweist.

> [!Note]  
> Das Verhalten von Funktionen, die ein Handle akzeptieren [**, das mit der Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) "-Funktion" (z. b. die Funktion " [**GetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime) ") erstellt wurde, unterscheidet sich abhängig davon, **ob die Funktion** "" mit dem **Dateiflag zum Öffnen des Analyse \_ \_ \_ \_ Punkts** aufgerufen wurde. Weitere Informationen finden Sie unter " [**kreatefile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) " und im folgenden Abschnitt " [kreatefile" und "kreatefiletransfailed](#createfile-and-createfiletransacted) ".

 

## <a name="copyfile-and-copyfiletransacted"></a>CopyFile und copyfiletransagiert

Wenn die Quelldatei eine symbolische Verknüpfung ist, ist die tatsächlich kopierte Datei das Ziel der symbolischen Verknüpfung.

Wenn die Zieldatei bereits vorhanden ist und eine symbolische Verknüpfung ist, wird die symbolische Verknüpfung von der Quelldatei überschrieben.

## <a name="copyfileex"></a>CopyFileEx

Wenn **Copy \_ file \_ Copy \_ symlink** und:

-   Wenn die Quelldatei eine symbolische Verknüpfung ist, wird die symbolische Verknüpfung kopiert, nicht die Zieldatei.
-   Wenn die Quelldatei keine symbolische Verknüpfung ist, ändert sich das Verhalten nicht.
-   Wenn es sich bei der Zieldatei um eine symbolische Verknüpfung handelt, wird die symbolische Verknüpfung überschrieben, nicht die Zieldatei.
-   Wenn beim Kopieren von Dateien ein Fehler auftritt, auch **\_ \_ \_ Wenn \_ vorhanden** angegeben ist, und die Zieldatei ein vorhandener symbolischer Link ist, schlägt der Vorgang in allen Fällen fehl.

Wenn **Copy \_ file \_ Copy \_ symlink** nicht angegeben ist, und:

-   Wenn beim Kopieren von Dateien ein Fehler auftritt, auch wenn **\_ \_ \_ \_ vorhanden** angegeben ist, und die Zieldatei ein vorhandener symbolischer Link ist, schlägt der Vorgang nur fehl, wenn das Ziel der symbolischen Verknüpfung vorhanden ist.
-   Wenn das **Kopieren von \_ Dateien \_ fehlschlägt, \_ Wenn \_ vorhanden** ist nicht angegeben wird, ändert sich das Verhalten nicht.

**Windows Server 2003 und Windows XP:** Das Flag **Copy \_ file \_ Copy \_ symlink** wird nicht unterstützt. Wenn die Quelldatei eine symbolische Verknüpfung ist, ist die tatsächlich kopierte Datei das Ziel der symbolischen Verknüpfung.

## <a name="createfile-and-createfiletransacted"></a>"Kreatefile" und "kreatefiletransagiert"

Wenn der-Aufrufe dieser Funktion eine neue Datei erstellt, gibt es keine Änderung des Verhaltens.

Wenn **das \_ Dateiflag \_ geöffnet \_ \_** ist, wird der Analyse Punkt und Folgendes angegeben:

-   Wenn eine vorhandene Datei geöffnet wird und es sich um eine symbolische Verknüpfung handelt, ist das zurückgegebene Handle ein Handle für die symbolische Verknüpfung.
-   Wenn **Create \_ Always**, **Truncate \_ vorhandene** oder **file \_ Flag \_ Delete \_ on \_ Close** angegeben wird, ist die betroffene Datei eine symbolische Verknüpfung.

Wenn das **Dateiflag zum Öffnen des Analyse Punkts nicht angegeben ist, wird \_ \_ \_ \_ Folgendes** angegeben:

-   Wenn eine vorhandene Datei geöffnet wird und es sich um eine symbolische Verknüpfung handelt, ist das zurückgegebene Handle ein Handle für das Ziel.
-   Wenn **Create \_ Always**, **Truncate \_ vorhandene** oder **file \_ Flag \_ Delete \_ on \_ Close** angegeben wird, ist die betroffene Datei das Ziel.

## <a name="createhardlink-and-createhardlinktransacted"></a>"Kreatehardlink" und "kreatehardlinktransagiert"

Wenn der Pfad auf eine symbolische Verknüpfung zeigt, erstellt die Funktion einen festen Link zum Ziel.

## <a name="deletefile-and-deletefiletransacted"></a>DeleteFile und deletefiletranshandelten

Wenn der Pfad auf eine symbolische Verknüpfung zeigt, wird die symbolische Verknüpfung gelöscht, nicht das Ziel. Wenn Sie ein Ziel löschen möchten, müssen Sie die Datei "up- [**File**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) " aufrufen und **\_ \_ \_ beim \_ schließen das Dateiflag löschen** angeben.

## <a name="findfirstchangenotification"></a>FindFirstChangeNotification

Wenn der Pfad auf eine symbolische Verknüpfung zeigt, wird das Benachrichtigungs Handle für das Ziel erstellt. Wenn eine Anwendung registriert wurde, um Änderungs Benachrichtigungen für ein Verzeichnis zu erhalten, das symbolische Verknüpfungen enthält, wird die Anwendung nur benachrichtigt, wenn die symbolischen Verknüpfungen geändert wurden, nicht die Zieldateien.

## <a name="findfirstfile-and-findfirstfiletransacted"></a>"FindFirstFile" und "findfirstfiletransagiert"

Wenn der Pfad auf eine symbolische Verknüpfung zeigt, enthält der Win32-Such [**\_ \_ Daten**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) Puffer Informationen über die symbolische Verknüpfung, nicht über das Ziel.

## <a name="findfirstfileex"></a>Findfirstfileex

Wenn der Pfad auf eine symbolische Verknüpfung zeigt, enthält der Win32-Such [**\_ \_ Daten**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) Puffer Informationen über die symbolische Verknüpfung, nicht über das Ziel.

## <a name="findnextfile"></a>FindNextFile

Wenn der Pfad auf eine symbolische Verknüpfung zeigt, enthält der Win32-Such [**\_ \_ Daten**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) Puffer Informationen über die symbolische Verknüpfung, nicht über das Ziel.

## <a name="getbinarytype"></a>Getbinarytype

Wenn der Pfad auf eine symbolische Verknüpfung zeigt, wird die Zieldatei verwendet.

## <a name="getcompressedfilesize-and-getcompressedfilesizetransacted"></a>Getcompressedfilesize und getcompressedfilesizetranshandelten

Wenn der Pfad auf eine symbolische Verknüpfung zeigt, gibt die Funktion die Dateigröße des Ziels zurück.

## <a name="getdiskfreespace"></a>GetDiskFreeSpace

Wenn der Pfad auf eine symbolische Verknüpfung zeigt, wird der Vorgang auf dem Ziel ausgeführt.

## <a name="getdiskfreespaceex"></a>GetDiskFreeSpaceEx

Wenn der Pfad auf eine symbolische Verknüpfung zeigt, wird der Vorgang auf dem Ziel ausgeführt.

## <a name="getfileattributes"></a>GetFileAttributes

Wenn der Pfad auf eine symbolische Verknüpfung zeigt, gibt die Funktion Attribute für den symbolischen Link zurück.

## <a name="getfileattributesex"></a>Getfileattributesex

Wenn der Pfad auf eine symbolische Verknüpfung zeigt, gibt die Funktion Attribute für den symbolischen Link zurück.

## <a name="getfilesecurity"></a>Getfilesecurity

Wenn der Pfad auf eine symbolische Verknüpfung zeigt, gibt die Funktion Attribute für den symbolischen Link zurück.

## <a name="gettemppath"></a>GetTempPath

Wenn der Pfad auf eine symbolische Verknüpfung zeigt, verwaltet der temporäre Pfadname alle symbolischen Verknüpfungen.

## <a name="getvolumeinformation"></a>GetVolumeInformation

Wenn der Pfad auf eine symbolische Verknüpfung zeigt, gibt die Funktion Volumeinformationen für das Ziel zurück.

## <a name="setfileattributes"></a>Setfileattribute

Wenn der Pfad auf eine symbolische Verknüpfung zeigt, ruft die Funktion Attribute für den symbolischen Link ab.

## <a name="setfilesecurity"></a>Setfilesecurity

Wenn der Pfad auf eine symbolische Verknüpfung zeigt, gibt die Funktion Attribute für den symbolischen Link zurück.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile)
</dt> <dt>

[**Copyfiletransagiert**](/windows/desktop/api/WinBase/nf-winbase-copyfiletransacteda)
</dt> <dt>

[**CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa)
</dt> <dt>

[**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[**"Kreatefiletransagiert"**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda)
</dt> <dt>

[**"Kreatehardlink"**](/windows/desktop/api/WinBase/nf-winbase-createhardlinka)
</dt> <dt>

[**"Kreatehardlinktransagiert"**](/windows/desktop/api/WinBase/nf-winbase-createhardlinktransacteda)
</dt> <dt>

[**DeleteFile**](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea)
</dt> <dt>

[**Deletefiletransagiert**](/windows/desktop/api/WinBase/nf-winbase-deletefiletransacteda)
</dt> <dt>

[**FindFirstChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa)
</dt> <dt>

[**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea)
</dt> <dt>

[**Findfirstfileex**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa)
</dt> <dt>

[**Findfirstfiletransagiert**](/windows/desktop/api/WinBase/nf-winbase-findfirstfiletransacteda)
</dt> <dt>

[**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)
</dt> <dt>

[**Getbinarytype**](/windows/desktop/api/WinBase/nf-winbase-getbinarytypea)
</dt> <dt>

[**Getcompressedfilesize**](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea)
</dt> <dt>

[**Getcompressedfilesizetranshandelten**](/windows/desktop/api/WinBase/nf-winbase-getcompressedfilesizetransacteda)
</dt> <dt>

[**GetDiskFreeSpace**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespacea)
</dt> <dt>

[**GetDiskFreeSpaceEx**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespaceexa)
</dt> <dt>

[**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa)
</dt> <dt>

[**Getfileattributesex**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa)
</dt> <dt>

[**Getfilesecurity**](/windows/desktop/api/winbase/nf-winbase-getfilesecuritya)
</dt> <dt>

[**GetTempPath**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha)
</dt> <dt>

[**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa)
</dt> <dt>

[**Setfileattribute**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa)
</dt> <dt>

[**Setfilesecurity**](/windows/desktop/api/winbase/nf-winbase-setfilesecuritya)
</dt> </dl>

 

 
