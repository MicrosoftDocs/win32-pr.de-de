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
# <a name="symbolic-link-effects-on-file-systems-functions"></a><span data-ttu-id="7cb60-103">Symbolische Verknüpfungs Effekte in Dateisystemfunktionen</span><span class="sxs-lookup"><span data-stu-id="7cb60-103">Symbolic Link Effects on File Systems Functions</span></span>

<span data-ttu-id="7cb60-104">Die Verwendung von symbolischen Verknüpfungen wirkt sich auf mehrere Standarddatei Funktionen aus, die Pfadnamen verwenden, um eine oder mehrere Dateien anzugeben.</span><span class="sxs-lookup"><span data-stu-id="7cb60-104">Several standard file functions that use path names to specify one or more files are affected by the use of symbolic links.</span></span> <span data-ttu-id="7cb60-105">In diesem Thema werden diese Funktionen aufgelistet und die Änderungen im Verhalten beschrieben:</span><span class="sxs-lookup"><span data-stu-id="7cb60-105">This topic lists those functions and describes the changes in behavior:</span></span>

-   [<span data-ttu-id="7cb60-106">CopyFile und copyfiletransagiert</span><span class="sxs-lookup"><span data-stu-id="7cb60-106">CopyFile and CopyFileTransacted</span></span>](#copyfile-and-copyfiletransacted)
-   [<span data-ttu-id="7cb60-107">CopyFileEx</span><span class="sxs-lookup"><span data-stu-id="7cb60-107">CopyFileEx</span></span>](#copyfileex)
-   [<span data-ttu-id="7cb60-108">"Kreatefile" und "kreatefiletransagiert"</span><span class="sxs-lookup"><span data-stu-id="7cb60-108">CreateFile and CreateFileTransacted</span></span>](#createfile-and-createfiletransacted)
-   [<span data-ttu-id="7cb60-109">"Kreatehardlink" und "kreatehardlinktransagiert"</span><span class="sxs-lookup"><span data-stu-id="7cb60-109">CreateHardLink and CreateHardLinkTransacted</span></span>](#createhardlink-and-createhardlinktransacted)
-   [<span data-ttu-id="7cb60-110">DeleteFile und deletefiletranshandelten</span><span class="sxs-lookup"><span data-stu-id="7cb60-110">DeleteFile and DeleteFileTransacted</span></span>](#deletefile-and-deletefiletransacted)
-   [<span data-ttu-id="7cb60-111">FindFirstChangeNotification</span><span class="sxs-lookup"><span data-stu-id="7cb60-111">FindFirstChangeNotification</span></span>](#findfirstchangenotification)
-   [<span data-ttu-id="7cb60-112">"FindFirstFile" und "findfirstfiletransagiert"</span><span class="sxs-lookup"><span data-stu-id="7cb60-112">FindFirstFile and FindFirstFileTransacted</span></span>](#findfirstfile-and-findfirstfiletransacted)
-   [<span data-ttu-id="7cb60-113">Findfirstfileex</span><span class="sxs-lookup"><span data-stu-id="7cb60-113">FindFirstFileEx</span></span>](#findfirstfileex)
-   [<span data-ttu-id="7cb60-114">FindNextFile</span><span class="sxs-lookup"><span data-stu-id="7cb60-114">FindNextFile</span></span>](#findnextfile)
-   [<span data-ttu-id="7cb60-115">Getbinarytype</span><span class="sxs-lookup"><span data-stu-id="7cb60-115">GetBinaryType</span></span>](#getbinarytype)
-   [<span data-ttu-id="7cb60-116">Getcompressedfilesize und getcompressedfilesizetranshandelten</span><span class="sxs-lookup"><span data-stu-id="7cb60-116">GetCompressedFileSize and GetCompressedFileSizeTransacted</span></span>](#getcompressedfilesize-and-getcompressedfilesizetransacted)
-   [<span data-ttu-id="7cb60-117">GetDiskFreeSpace</span><span class="sxs-lookup"><span data-stu-id="7cb60-117">GetDiskFreeSpace</span></span>](#getdiskfreespaceex)
-   [<span data-ttu-id="7cb60-118">GetDiskFreeSpaceEx</span><span class="sxs-lookup"><span data-stu-id="7cb60-118">GetDiskFreeSpaceEx</span></span>](#getdiskfreespaceex)
-   [<span data-ttu-id="7cb60-119">GetFileAttributes</span><span class="sxs-lookup"><span data-stu-id="7cb60-119">GetFileAttributes</span></span>](#getfileattributesex)
-   [<span data-ttu-id="7cb60-120">Getfileattributesex</span><span class="sxs-lookup"><span data-stu-id="7cb60-120">GetFileAttributesEx</span></span>](#getfileattributesex)
-   [<span data-ttu-id="7cb60-121">Getfilesecurity</span><span class="sxs-lookup"><span data-stu-id="7cb60-121">GetFileSecurity</span></span>](#getfilesecurity)
-   [<span data-ttu-id="7cb60-122">GetTempPath</span><span class="sxs-lookup"><span data-stu-id="7cb60-122">GetTempPath</span></span>](#gettemppath)
-   [<span data-ttu-id="7cb60-123">GetVolumeInformation</span><span class="sxs-lookup"><span data-stu-id="7cb60-123">GetVolumeInformation</span></span>](#getvolumeinformation)
-   [<span data-ttu-id="7cb60-124">Setfileattribute</span><span class="sxs-lookup"><span data-stu-id="7cb60-124">SetFileAttributes</span></span>](#setfileattributes)
-   [<span data-ttu-id="7cb60-125">Setfilesecurity</span><span class="sxs-lookup"><span data-stu-id="7cb60-125">SetFileSecurity</span></span>](#setfilesecurity)
-   [<span data-ttu-id="7cb60-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7cb60-126">Related topics</span></span>](#related-topics)

<span data-ttu-id="7cb60-127">In den folgenden Beschreibungen werden die folgenden Begriffe verwendet:</span><span class="sxs-lookup"><span data-stu-id="7cb60-127">In the descriptions below, the following terms are used:</span></span>

-   <span data-ttu-id="7cb60-128">Quelldatei – die ursprüngliche Datei, die kopiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="7cb60-128">Source file—The original file that is to be copied.</span></span>
-   <span data-ttu-id="7cb60-129">Zieldatei – die neu erstellte Kopie der Datei.</span><span class="sxs-lookup"><span data-stu-id="7cb60-129">Destination file—The newly created copy of the file.</span></span>
-   <span data-ttu-id="7cb60-130">Target – die Entität, auf die ein symbolischer Link verweist.</span><span class="sxs-lookup"><span data-stu-id="7cb60-130">Target—The entity that a symbolic link points to.</span></span>

> [!Note]  
> <span data-ttu-id="7cb60-131">Das Verhalten von Funktionen, die ein Handle akzeptieren [**, das mit der Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) "-Funktion" (z. b. die Funktion " [**GetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime) ") erstellt wurde, unterscheidet sich abhängig davon, **ob die Funktion** "" mit dem **Dateiflag zum Öffnen des Analyse \_ \_ \_ \_ Punkts** aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="7cb60-131">The behavior of functions that accept a handle created using the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function, such as the [**GetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime) function, will differ based on whether or not the **CreateFile** function was called using the **FILE\_FLAG\_OPEN\_REPARSE\_POINT** flag.</span></span> <span data-ttu-id="7cb60-132">Weitere Informationen finden Sie unter " [**kreatefile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) " und im folgenden Abschnitt " [kreatefile" und "kreatefiletransfailed](#createfile-and-createfiletransacted) ".</span><span class="sxs-lookup"><span data-stu-id="7cb60-132">For more information, see [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) and the following [CreateFile and CreateFileTransacted](#createfile-and-createfiletransacted) section.</span></span>

 

## <a name="copyfile-and-copyfiletransacted"></a><span data-ttu-id="7cb60-133">CopyFile und copyfiletransagiert</span><span class="sxs-lookup"><span data-stu-id="7cb60-133">CopyFile and CopyFileTransacted</span></span>

<span data-ttu-id="7cb60-134">Wenn die Quelldatei eine symbolische Verknüpfung ist, ist die tatsächlich kopierte Datei das Ziel der symbolischen Verknüpfung.</span><span class="sxs-lookup"><span data-stu-id="7cb60-134">If the source file is a symbolic link, the actual file copied is the target of the symbolic link.</span></span>

<span data-ttu-id="7cb60-135">Wenn die Zieldatei bereits vorhanden ist und eine symbolische Verknüpfung ist, wird die symbolische Verknüpfung von der Quelldatei überschrieben.</span><span class="sxs-lookup"><span data-stu-id="7cb60-135">If the destination file already exists and is a symbolic link, the symbolic link is overwritten by the source file.</span></span>

## <a name="copyfileex"></a><span data-ttu-id="7cb60-136">CopyFileEx</span><span class="sxs-lookup"><span data-stu-id="7cb60-136">CopyFileEx</span></span>

<span data-ttu-id="7cb60-137">Wenn **Copy \_ file \_ Copy \_ symlink** und:</span><span class="sxs-lookup"><span data-stu-id="7cb60-137">If **COPY\_FILE\_COPY\_SYMLINK** is specified and:</span></span>

-   <span data-ttu-id="7cb60-138">Wenn die Quelldatei eine symbolische Verknüpfung ist, wird die symbolische Verknüpfung kopiert, nicht die Zieldatei.</span><span class="sxs-lookup"><span data-stu-id="7cb60-138">If the source file is a symbolic link, the symbolic link is copied, not the target file.</span></span>
-   <span data-ttu-id="7cb60-139">Wenn die Quelldatei keine symbolische Verknüpfung ist, ändert sich das Verhalten nicht.</span><span class="sxs-lookup"><span data-stu-id="7cb60-139">If the source file is not a symbolic link, there is no change in behavior.</span></span>
-   <span data-ttu-id="7cb60-140">Wenn es sich bei der Zieldatei um eine symbolische Verknüpfung handelt, wird die symbolische Verknüpfung überschrieben, nicht die Zieldatei.</span><span class="sxs-lookup"><span data-stu-id="7cb60-140">If the destination file is an existing symbolic link, the symbolic link is overwritten, not the target file.</span></span>
-   <span data-ttu-id="7cb60-141">Wenn beim Kopieren von Dateien ein Fehler auftritt, auch **\_ \_ \_ Wenn \_ vorhanden** angegeben ist, und die Zieldatei ein vorhandener symbolischer Link ist, schlägt der Vorgang in allen Fällen fehl.</span><span class="sxs-lookup"><span data-stu-id="7cb60-141">If **COPY\_FILE\_FAIL\_IF\_EXISTS** is also specified, and the destination file is an existing symbolic link, the operation fails in all cases.</span></span>

<span data-ttu-id="7cb60-142">Wenn **Copy \_ file \_ Copy \_ symlink** nicht angegeben ist, und:</span><span class="sxs-lookup"><span data-stu-id="7cb60-142">If **COPY\_FILE\_COPY\_SYMLINK** is not specified and:</span></span>

-   <span data-ttu-id="7cb60-143">Wenn beim Kopieren von Dateien ein Fehler auftritt, auch wenn **\_ \_ \_ \_ vorhanden** angegeben ist, und die Zieldatei ein vorhandener symbolischer Link ist, schlägt der Vorgang nur fehl, wenn das Ziel der symbolischen Verknüpfung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="7cb60-143">If **COPY\_FILE\_FAIL\_IF\_EXISTS** is also specified, and the destination file is an existing symbolic link, the operation fails only if the target of the symbolic link exists.</span></span>
-   <span data-ttu-id="7cb60-144">Wenn das **Kopieren von \_ Dateien \_ fehlschlägt, \_ Wenn \_ vorhanden** ist nicht angegeben wird, ändert sich das Verhalten nicht.</span><span class="sxs-lookup"><span data-stu-id="7cb60-144">If **COPY\_FILE\_FAIL\_IF\_EXISTS** is not specified, there is no change in behavior.</span></span>

<span data-ttu-id="7cb60-145">**Windows Server 2003 und Windows XP:** Das Flag **Copy \_ file \_ Copy \_ symlink** wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7cb60-145">**Windows Server 2003 and Windows XP:** The **COPY\_FILE\_COPY\_SYMLINK** flag is not supported.</span></span> <span data-ttu-id="7cb60-146">Wenn die Quelldatei eine symbolische Verknüpfung ist, ist die tatsächlich kopierte Datei das Ziel der symbolischen Verknüpfung.</span><span class="sxs-lookup"><span data-stu-id="7cb60-146">If the source file is a symbolic link, the actual file copied is the target of the symbolic link.</span></span>

## <a name="createfile-and-createfiletransacted"></a><span data-ttu-id="7cb60-147">"Kreatefile" und "kreatefiletransagiert"</span><span class="sxs-lookup"><span data-stu-id="7cb60-147">CreateFile and CreateFileTransacted</span></span>

<span data-ttu-id="7cb60-148">Wenn der-Aufrufe dieser Funktion eine neue Datei erstellt, gibt es keine Änderung des Verhaltens.</span><span class="sxs-lookup"><span data-stu-id="7cb60-148">If the call to this function creates a new file, there is no change in behavior.</span></span>

<span data-ttu-id="7cb60-149">Wenn **das \_ Dateiflag \_ geöffnet \_ \_** ist, wird der Analyse Punkt und Folgendes angegeben:</span><span class="sxs-lookup"><span data-stu-id="7cb60-149">If **FILE\_FLAG\_OPEN\_REPARSE\_POINT** is specified and:</span></span>

-   <span data-ttu-id="7cb60-150">Wenn eine vorhandene Datei geöffnet wird und es sich um eine symbolische Verknüpfung handelt, ist das zurückgegebene Handle ein Handle für die symbolische Verknüpfung.</span><span class="sxs-lookup"><span data-stu-id="7cb60-150">If an existing file is opened and it is a symbolic link, the handle returned is a handle to the symbolic link.</span></span>
-   <span data-ttu-id="7cb60-151">Wenn **Create \_ Always**, **Truncate \_ vorhandene** oder **file \_ Flag \_ Delete \_ on \_ Close** angegeben wird, ist die betroffene Datei eine symbolische Verknüpfung.</span><span class="sxs-lookup"><span data-stu-id="7cb60-151">If **CREATE\_ALWAYS**, **TRUNCATE\_EXISTING**, or **FILE\_FLAG\_DELETE\_ON\_CLOSE** are specified, the file affected is a symbolic link.</span></span>

<span data-ttu-id="7cb60-152">Wenn das **Dateiflag zum Öffnen des Analyse Punkts nicht angegeben ist, wird \_ \_ \_ \_ Folgendes** angegeben:</span><span class="sxs-lookup"><span data-stu-id="7cb60-152">If **FILE\_FLAG\_OPEN\_REPARSE\_POINT** is not specified and:</span></span>

-   <span data-ttu-id="7cb60-153">Wenn eine vorhandene Datei geöffnet wird und es sich um eine symbolische Verknüpfung handelt, ist das zurückgegebene Handle ein Handle für das Ziel.</span><span class="sxs-lookup"><span data-stu-id="7cb60-153">If an existing file is opened and it is a symbolic link, the handle returned is a handle to the target.</span></span>
-   <span data-ttu-id="7cb60-154">Wenn **Create \_ Always**, **Truncate \_ vorhandene** oder **file \_ Flag \_ Delete \_ on \_ Close** angegeben wird, ist die betroffene Datei das Ziel.</span><span class="sxs-lookup"><span data-stu-id="7cb60-154">If **CREATE\_ALWAYS**, **TRUNCATE\_EXISTING**, or **FILE\_FLAG\_DELETE\_ON\_CLOSE** are specified, the file affected is the target.</span></span>

## <a name="createhardlink-and-createhardlinktransacted"></a><span data-ttu-id="7cb60-155">"Kreatehardlink" und "kreatehardlinktransagiert"</span><span class="sxs-lookup"><span data-stu-id="7cb60-155">CreateHardLink and CreateHardLinkTransacted</span></span>

<span data-ttu-id="7cb60-156">Wenn der Pfad auf eine symbolische Verknüpfung zeigt, erstellt die Funktion einen festen Link zum Ziel.</span><span class="sxs-lookup"><span data-stu-id="7cb60-156">If the path points to a symbolic link, the function creates a hard link to the target.</span></span>

## <a name="deletefile-and-deletefiletransacted"></a><span data-ttu-id="7cb60-157">DeleteFile und deletefiletranshandelten</span><span class="sxs-lookup"><span data-stu-id="7cb60-157">DeleteFile and DeleteFileTransacted</span></span>

<span data-ttu-id="7cb60-158">Wenn der Pfad auf eine symbolische Verknüpfung zeigt, wird die symbolische Verknüpfung gelöscht, nicht das Ziel.</span><span class="sxs-lookup"><span data-stu-id="7cb60-158">If the path points to a symbolic link, the symbolic link is deleted, not the target.</span></span> <span data-ttu-id="7cb60-159">Wenn Sie ein Ziel löschen möchten, müssen Sie die Datei "up- [**File**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) " aufrufen und **\_ \_ \_ beim \_ schließen das Dateiflag löschen** angeben.</span><span class="sxs-lookup"><span data-stu-id="7cb60-159">To delete a target, you must call [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) and specify **FILE\_FLAG\_DELETE\_ON\_CLOSE**.</span></span>

## <a name="findfirstchangenotification"></a><span data-ttu-id="7cb60-160">FindFirstChangeNotification</span><span class="sxs-lookup"><span data-stu-id="7cb60-160">FindFirstChangeNotification</span></span>

<span data-ttu-id="7cb60-161">Wenn der Pfad auf eine symbolische Verknüpfung zeigt, wird das Benachrichtigungs Handle für das Ziel erstellt.</span><span class="sxs-lookup"><span data-stu-id="7cb60-161">If the path points to a symbolic link, the notification handle is created for the target.</span></span> <span data-ttu-id="7cb60-162">Wenn eine Anwendung registriert wurde, um Änderungs Benachrichtigungen für ein Verzeichnis zu erhalten, das symbolische Verknüpfungen enthält, wird die Anwendung nur benachrichtigt, wenn die symbolischen Verknüpfungen geändert wurden, nicht die Zieldateien.</span><span class="sxs-lookup"><span data-stu-id="7cb60-162">If an application has registered to receive change notifications for a directory that contains symbolic links, the application is only notified when the symbolic links have been changed, not the target files.</span></span>

## <a name="findfirstfile-and-findfirstfiletransacted"></a><span data-ttu-id="7cb60-163">"FindFirstFile" und "findfirstfiletransagiert"</span><span class="sxs-lookup"><span data-stu-id="7cb60-163">FindFirstFile and FindFirstFileTransacted</span></span>

<span data-ttu-id="7cb60-164">Wenn der Pfad auf eine symbolische Verknüpfung zeigt, enthält der Win32-Such [**\_ \_ Daten**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) Puffer Informationen über die symbolische Verknüpfung, nicht über das Ziel.</span><span class="sxs-lookup"><span data-stu-id="7cb60-164">If the path points to a symbolic link, the [**WIN32\_FIND\_DATA**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) buffer contains information about the symbolic link, not the target.</span></span>

## <a name="findfirstfileex"></a><span data-ttu-id="7cb60-165">Findfirstfileex</span><span class="sxs-lookup"><span data-stu-id="7cb60-165">FindFirstFileEx</span></span>

<span data-ttu-id="7cb60-166">Wenn der Pfad auf eine symbolische Verknüpfung zeigt, enthält der Win32-Such [**\_ \_ Daten**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) Puffer Informationen über die symbolische Verknüpfung, nicht über das Ziel.</span><span class="sxs-lookup"><span data-stu-id="7cb60-166">If the path points to a symbolic link, the [**WIN32\_FIND\_DATA**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) buffer contains information about the symbolic link, not the target.</span></span>

## <a name="findnextfile"></a><span data-ttu-id="7cb60-167">FindNextFile</span><span class="sxs-lookup"><span data-stu-id="7cb60-167">FindNextFile</span></span>

<span data-ttu-id="7cb60-168">Wenn der Pfad auf eine symbolische Verknüpfung zeigt, enthält der Win32-Such [**\_ \_ Daten**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) Puffer Informationen über die symbolische Verknüpfung, nicht über das Ziel.</span><span class="sxs-lookup"><span data-stu-id="7cb60-168">If the path points to a symbolic link, the [**WIN32\_FIND\_DATA**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) buffer contains information about the symbolic link, not the target.</span></span>

## <a name="getbinarytype"></a><span data-ttu-id="7cb60-169">Getbinarytype</span><span class="sxs-lookup"><span data-stu-id="7cb60-169">GetBinaryType</span></span>

<span data-ttu-id="7cb60-170">Wenn der Pfad auf eine symbolische Verknüpfung zeigt, wird die Zieldatei verwendet.</span><span class="sxs-lookup"><span data-stu-id="7cb60-170">If the path points to a symbolic link, the target file is used.</span></span>

## <a name="getcompressedfilesize-and-getcompressedfilesizetransacted"></a><span data-ttu-id="7cb60-171">Getcompressedfilesize und getcompressedfilesizetranshandelten</span><span class="sxs-lookup"><span data-stu-id="7cb60-171">GetCompressedFileSize and GetCompressedFileSizeTransacted</span></span>

<span data-ttu-id="7cb60-172">Wenn der Pfad auf eine symbolische Verknüpfung zeigt, gibt die Funktion die Dateigröße des Ziels zurück.</span><span class="sxs-lookup"><span data-stu-id="7cb60-172">If the path points to a symbolic link, the function returns the file size of the target.</span></span>

## <a name="getdiskfreespace"></a><span data-ttu-id="7cb60-173">GetDiskFreeSpace</span><span class="sxs-lookup"><span data-stu-id="7cb60-173">GetDiskFreeSpace</span></span>

<span data-ttu-id="7cb60-174">Wenn der Pfad auf eine symbolische Verknüpfung zeigt, wird der Vorgang auf dem Ziel ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7cb60-174">If the path points to a symbolic link, the operation is performed on the target.</span></span>

## <a name="getdiskfreespaceex"></a><span data-ttu-id="7cb60-175">GetDiskFreeSpaceEx</span><span class="sxs-lookup"><span data-stu-id="7cb60-175">GetDiskFreeSpaceEx</span></span>

<span data-ttu-id="7cb60-176">Wenn der Pfad auf eine symbolische Verknüpfung zeigt, wird der Vorgang auf dem Ziel ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7cb60-176">If the path points to a symbolic link, the operation is performed on the target.</span></span>

## <a name="getfileattributes"></a><span data-ttu-id="7cb60-177">GetFileAttributes</span><span class="sxs-lookup"><span data-stu-id="7cb60-177">GetFileAttributes</span></span>

<span data-ttu-id="7cb60-178">Wenn der Pfad auf eine symbolische Verknüpfung zeigt, gibt die Funktion Attribute für den symbolischen Link zurück.</span><span class="sxs-lookup"><span data-stu-id="7cb60-178">If the path points to a symbolic link, the function returns attributes for the symbolic link.</span></span>

## <a name="getfileattributesex"></a><span data-ttu-id="7cb60-179">Getfileattributesex</span><span class="sxs-lookup"><span data-stu-id="7cb60-179">GetFileAttributesEx</span></span>

<span data-ttu-id="7cb60-180">Wenn der Pfad auf eine symbolische Verknüpfung zeigt, gibt die Funktion Attribute für den symbolischen Link zurück.</span><span class="sxs-lookup"><span data-stu-id="7cb60-180">If the path points to a symbolic link, the function returns attributes for the symbolic link.</span></span>

## <a name="getfilesecurity"></a><span data-ttu-id="7cb60-181">Getfilesecurity</span><span class="sxs-lookup"><span data-stu-id="7cb60-181">GetFileSecurity</span></span>

<span data-ttu-id="7cb60-182">Wenn der Pfad auf eine symbolische Verknüpfung zeigt, gibt die Funktion Attribute für den symbolischen Link zurück.</span><span class="sxs-lookup"><span data-stu-id="7cb60-182">If the path points to a symbolic link, the function returns attributes for the symbolic link.</span></span>

## <a name="gettemppath"></a><span data-ttu-id="7cb60-183">GetTempPath</span><span class="sxs-lookup"><span data-stu-id="7cb60-183">GetTempPath</span></span>

<span data-ttu-id="7cb60-184">Wenn der Pfad auf eine symbolische Verknüpfung zeigt, verwaltet der temporäre Pfadname alle symbolischen Verknüpfungen.</span><span class="sxs-lookup"><span data-stu-id="7cb60-184">If the path points to a symbolic link, the temp path name maintains any symbolic links.</span></span>

## <a name="getvolumeinformation"></a><span data-ttu-id="7cb60-185">GetVolumeInformation</span><span class="sxs-lookup"><span data-stu-id="7cb60-185">GetVolumeInformation</span></span>

<span data-ttu-id="7cb60-186">Wenn der Pfad auf eine symbolische Verknüpfung zeigt, gibt die Funktion Volumeinformationen für das Ziel zurück.</span><span class="sxs-lookup"><span data-stu-id="7cb60-186">If the path points to a symbolic link, the function returns volume information for the target.</span></span>

## <a name="setfileattributes"></a><span data-ttu-id="7cb60-187">Setfileattribute</span><span class="sxs-lookup"><span data-stu-id="7cb60-187">SetFileAttributes</span></span>

<span data-ttu-id="7cb60-188">Wenn der Pfad auf eine symbolische Verknüpfung zeigt, ruft die Funktion Attribute für den symbolischen Link ab.</span><span class="sxs-lookup"><span data-stu-id="7cb60-188">If the path points to a symbolic link, the function retrieves attributes for the symbolic link.</span></span>

## <a name="setfilesecurity"></a><span data-ttu-id="7cb60-189">Setfilesecurity</span><span class="sxs-lookup"><span data-stu-id="7cb60-189">SetFileSecurity</span></span>

<span data-ttu-id="7cb60-190">Wenn der Pfad auf eine symbolische Verknüpfung zeigt, gibt die Funktion Attribute für den symbolischen Link zurück.</span><span class="sxs-lookup"><span data-stu-id="7cb60-190">If the path points to a symbolic link, the function returns attributes for the symbolic link.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7cb60-191">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7cb60-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7cb60-192">**CopyFile**</span><span class="sxs-lookup"><span data-stu-id="7cb60-192">**CopyFile**</span></span>](/windows/desktop/api/WinBase/nf-winbase-copyfile)
</dt> <dt>

[<span data-ttu-id="7cb60-193">**Copyfiletransagiert**</span><span class="sxs-lookup"><span data-stu-id="7cb60-193">**CopyFileTransacted**</span></span>](/windows/desktop/api/WinBase/nf-winbase-copyfiletransacteda)
</dt> <dt>

[<span data-ttu-id="7cb60-194">**CopyFileEx**</span><span class="sxs-lookup"><span data-stu-id="7cb60-194">**CopyFileEx**</span></span>](/windows/desktop/api/WinBase/nf-winbase-copyfileexa)
</dt> <dt>

[<span data-ttu-id="7cb60-195">**CreateFile**</span><span class="sxs-lookup"><span data-stu-id="7cb60-195">**CreateFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[<span data-ttu-id="7cb60-196">**"Kreatefiletransagiert"**</span><span class="sxs-lookup"><span data-stu-id="7cb60-196">**CreateFileTransacted**</span></span>](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda)
</dt> <dt>

[<span data-ttu-id="7cb60-197">**"Kreatehardlink"**</span><span class="sxs-lookup"><span data-stu-id="7cb60-197">**CreateHardLink**</span></span>](/windows/desktop/api/WinBase/nf-winbase-createhardlinka)
</dt> <dt>

[<span data-ttu-id="7cb60-198">**"Kreatehardlinktransagiert"**</span><span class="sxs-lookup"><span data-stu-id="7cb60-198">**CreateHardLinkTransacted**</span></span>](/windows/desktop/api/WinBase/nf-winbase-createhardlinktransacteda)
</dt> <dt>

[<span data-ttu-id="7cb60-199">**DeleteFile**</span><span class="sxs-lookup"><span data-stu-id="7cb60-199">**DeleteFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea)
</dt> <dt>

[<span data-ttu-id="7cb60-200">**Deletefiletransagiert**</span><span class="sxs-lookup"><span data-stu-id="7cb60-200">**DeleteFileTransacted**</span></span>](/windows/desktop/api/WinBase/nf-winbase-deletefiletransacteda)
</dt> <dt>

[<span data-ttu-id="7cb60-201">**FindFirstChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="7cb60-201">**FindFirstChangeNotification**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa)
</dt> <dt>

[<span data-ttu-id="7cb60-202">**FindFirstFile**</span><span class="sxs-lookup"><span data-stu-id="7cb60-202">**FindFirstFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea)
</dt> <dt>

[<span data-ttu-id="7cb60-203">**Findfirstfileex**</span><span class="sxs-lookup"><span data-stu-id="7cb60-203">**FindFirstFileEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa)
</dt> <dt>

[<span data-ttu-id="7cb60-204">**Findfirstfiletransagiert**</span><span class="sxs-lookup"><span data-stu-id="7cb60-204">**FindFirstFileTransacted**</span></span>](/windows/desktop/api/WinBase/nf-winbase-findfirstfiletransacteda)
</dt> <dt>

[<span data-ttu-id="7cb60-205">**FindNextFile**</span><span class="sxs-lookup"><span data-stu-id="7cb60-205">**FindNextFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)
</dt> <dt>

[<span data-ttu-id="7cb60-206">**Getbinarytype**</span><span class="sxs-lookup"><span data-stu-id="7cb60-206">**GetBinaryType**</span></span>](/windows/desktop/api/WinBase/nf-winbase-getbinarytypea)
</dt> <dt>

[<span data-ttu-id="7cb60-207">**Getcompressedfilesize**</span><span class="sxs-lookup"><span data-stu-id="7cb60-207">**GetCompressedFileSize**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea)
</dt> <dt>

[<span data-ttu-id="7cb60-208">**Getcompressedfilesizetranshandelten**</span><span class="sxs-lookup"><span data-stu-id="7cb60-208">**GetCompressedFileSizeTransacted**</span></span>](/windows/desktop/api/WinBase/nf-winbase-getcompressedfilesizetransacteda)
</dt> <dt>

[<span data-ttu-id="7cb60-209">**GetDiskFreeSpace**</span><span class="sxs-lookup"><span data-stu-id="7cb60-209">**GetDiskFreeSpace**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespacea)
</dt> <dt>

[<span data-ttu-id="7cb60-210">**GetDiskFreeSpaceEx**</span><span class="sxs-lookup"><span data-stu-id="7cb60-210">**GetDiskFreeSpaceEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespaceexa)
</dt> <dt>

[<span data-ttu-id="7cb60-211">**GetFileAttributes**</span><span class="sxs-lookup"><span data-stu-id="7cb60-211">**GetFileAttributes**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa)
</dt> <dt>

[<span data-ttu-id="7cb60-212">**Getfileattributesex**</span><span class="sxs-lookup"><span data-stu-id="7cb60-212">**GetFileAttributesEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa)
</dt> <dt>

[<span data-ttu-id="7cb60-213">**Getfilesecurity**</span><span class="sxs-lookup"><span data-stu-id="7cb60-213">**GetFileSecurity**</span></span>](/windows/desktop/api/winbase/nf-winbase-getfilesecuritya)
</dt> <dt>

[<span data-ttu-id="7cb60-214">**GetTempPath**</span><span class="sxs-lookup"><span data-stu-id="7cb60-214">**GetTempPath**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha)
</dt> <dt>

[<span data-ttu-id="7cb60-215">**GetVolumeInformation**</span><span class="sxs-lookup"><span data-stu-id="7cb60-215">**GetVolumeInformation**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa)
</dt> <dt>

[<span data-ttu-id="7cb60-216">**Setfileattribute**</span><span class="sxs-lookup"><span data-stu-id="7cb60-216">**SetFileAttributes**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa)
</dt> <dt>

[<span data-ttu-id="7cb60-217">**Setfilesecurity**</span><span class="sxs-lookup"><span data-stu-id="7cb60-217">**SetFileSecurity**</span></span>](/windows/desktop/api/winbase/nf-winbase-setfilesecuritya)
</dt> </dl>

 

 
