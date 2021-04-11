---
description: Komprimiert die im Objekt Pfad angegebene logische Verzeichniseintrags Datei (oder das angegebene Verzeichnis).
ms.assetid: 4db13622-75c5-45db-8536-451059c0e477
ms.tgt_platform: multiple
title: Compress-Methode der Win32_Directory-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.Compress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ea694c09e11e5801016a4ea85b9774448c542991
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126116"
---
# <a name="compress-method-of-the-win32_directory-class"></a><span data-ttu-id="7caca-103">Methode komprimieren der Win32- \_ Verzeichnis Klasse</span><span class="sxs-lookup"><span data-stu-id="7caca-103">Compress method of the Win32\_Directory class</span></span>

<span data-ttu-id="7caca-104">Die  [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode komprimieren komprimiert die im Objekt Pfad angegebene logische Verzeichniseintrags Datei (oder das Verzeichnis).</span><span class="sxs-lookup"><span data-stu-id="7caca-104">The **Compress** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method compresses the logical directory entry file (or directory) specified in the object path.</span></span>

<span data-ttu-id="7caca-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="7caca-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="7caca-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="7caca-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="7caca-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7caca-107">Syntax</span></span>


```mof
uint32 Compress();
```



## <a name="parameters"></a><span data-ttu-id="7caca-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7caca-108">Parameters</span></span>

<span data-ttu-id="7caca-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="7caca-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7caca-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7caca-110">Return value</span></span>

<span data-ttu-id="7caca-111">Gibt den Wert 0 (null) zurück, wenn die Datei erfolgreich komprimiert wurde, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="7caca-111">Returns a value of 0 (zero) if the file was successfully compressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="7caca-112">**0**</span><span class="sxs-lookup"><span data-stu-id="7caca-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="7caca-113">Die Anforderung wurde erfolgreich gesendet.</span><span class="sxs-lookup"><span data-stu-id="7caca-113">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="7caca-114">**2**</span><span class="sxs-lookup"><span data-stu-id="7caca-114">**2**</span></span>
</dt> <dd>

<span data-ttu-id="7caca-115">Der Zugriff wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="7caca-115">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="7caca-116">**8**</span><span class="sxs-lookup"><span data-stu-id="7caca-116">**8**</span></span>
</dt> <dd>

<span data-ttu-id="7caca-117">Ein nicht angegebener Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="7caca-117">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="7caca-118">**9**</span><span class="sxs-lookup"><span data-stu-id="7caca-118">**9**</span></span>
</dt> <dd>

<span data-ttu-id="7caca-119">Der angegebene Name war ungültig.</span><span class="sxs-lookup"><span data-stu-id="7caca-119">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="7caca-120">**10**</span><span class="sxs-lookup"><span data-stu-id="7caca-120">**10**</span></span>
</dt> <dd>

<span data-ttu-id="7caca-121">Das angegebene Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="7caca-121">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="7caca-122">**11**</span><span class="sxs-lookup"><span data-stu-id="7caca-122">**11**</span></span>
</dt> <dd>

<span data-ttu-id="7caca-123">Das Dateisystem ist kein NTFS.</span><span class="sxs-lookup"><span data-stu-id="7caca-123">The file system is not an NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="7caca-124">**12**</span><span class="sxs-lookup"><span data-stu-id="7caca-124">**12**</span></span>
</dt> <dd>

<span data-ttu-id="7caca-125">Die Plattform ist nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="7caca-125">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="7caca-126">**13**</span><span class="sxs-lookup"><span data-stu-id="7caca-126">**13**</span></span>
</dt> <dd>

<span data-ttu-id="7caca-127">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="7caca-127">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="7caca-128">**14**</span><span class="sxs-lookup"><span data-stu-id="7caca-128">**14**</span></span>
</dt> <dd>

<span data-ttu-id="7caca-129">Das Verzeichnis ist nicht leer.</span><span class="sxs-lookup"><span data-stu-id="7caca-129">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="7caca-130">**15**</span><span class="sxs-lookup"><span data-stu-id="7caca-130">**15**</span></span>
</dt> <dd>

<span data-ttu-id="7caca-131">Es ist eine Freigabe Verletzung aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="7caca-131">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="7caca-132">**16**</span><span class="sxs-lookup"><span data-stu-id="7caca-132">**16**</span></span>
</dt> <dd>

<span data-ttu-id="7caca-133">Die angegebene Startdatei war ungültig.</span><span class="sxs-lookup"><span data-stu-id="7caca-133">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="7caca-134">**17**</span><span class="sxs-lookup"><span data-stu-id="7caca-134">**17**</span></span>
</dt> <dd>

<span data-ttu-id="7caca-135">Eine für den Vorgang erforderliche Berechtigung wird nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="7caca-135">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="7caca-136">**21**</span><span class="sxs-lookup"><span data-stu-id="7caca-136">**21**</span></span>
</dt> <dd>

<span data-ttu-id="7caca-137">Ein angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="7caca-137">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7caca-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7caca-138">Remarks</span></span>

<span data-ttu-id="7caca-139">Mit der Komprimierung können Sie zusätzlichen Speicherplatz auf einem Laufwerk freigeben, ohne neue Hardware kaufen und Dateien oder Ordner nicht entfernen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="7caca-139">Compression provides a way to free additional storage space on a disk drive without purchasing new hardware and without removing files or folders.</span></span> <span data-ttu-id="7caca-140">Abhängig von der Größe der Festplatte und dem Dateityp, der auf diesem Datenträger gespeichert ist, können Sie möglicherweise Hunderte von Megabyte Speicherplatz wiederherstellen. dadurch ist es nicht mehr erforderlich, dass Sie eine neue Festplatte kaufen und den Computer offline schalten, bis das neue Laufwerk installiert ist.</span><span class="sxs-lookup"><span data-stu-id="7caca-140">Depending on the size of your hard disk and the type of files stored on that disk, you might be able to recover hundreds of megabytes of disk space and thus preclude the need to purchase a new hard drive and to take the computer offline until the new drive is installed.</span></span>

<span data-ttu-id="7caca-141">Die Methode komprimieren komprimiert alle Dateien und Unterordner innerhalb eines angegebenen Ordners.</span><span class="sxs-lookup"><span data-stu-id="7caca-141">The Compress method compresses all the files and subfolders within a specified folder.</span></span> <span data-ttu-id="7caca-142">Darüber hinaus enthält die-Klasse auch eine uncompress-Methode, die die Komprimierung aus allen Dateien und Unterordnern in einem Ordner entfernt.</span><span class="sxs-lookup"><span data-stu-id="7caca-142">In addition, the class also includes an Uncompress method that removes compression from all the files and subfolders in a folder.</span></span> <span data-ttu-id="7caca-143">Ähnliche Methoden werden auch mit der CIM \_ DataFile-Klasse bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="7caca-143">Similar methods are also provided with the CIM\_Datafile class.</span></span> <span data-ttu-id="7caca-144">Auf diese Weise können Sie bestimmte Dateien in einem Ordner selektiv komprimieren oder dekomprimieren.</span><span class="sxs-lookup"><span data-stu-id="7caca-144">This allows you to selectively compress or uncompress specific files within a folder.</span></span>

<span data-ttu-id="7caca-145">Da die Komprimierung eine geringfügige Leistungs Einbuße eingibt, wird Sie nicht für Dateien oder Ordner empfohlen, auf die routinemäßig zugegriffen wird. beispielsweise möchten Sie wahrscheinlich nicht Datenbankdateien, Protokolldateien oder Benutzerprofil Ordner komprimieren.</span><span class="sxs-lookup"><span data-stu-id="7caca-145">Because compression imparts a slight performance penalty, it is not recommended for files or folders that are accessed on a routine basis; for example, you probably do not want to compress database files, log files, or user profile folders.</span></span> <span data-ttu-id="7caca-146">Bessere Kandidaten für die Komprimierung sind Dateien und Ordner, auf die nicht sehr häufig zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="7caca-146">Better candidates for compression are files and folders that are not accessed very often.</span></span> <span data-ttu-id="7caca-147">Sie können z. b. ein Skript schreiben, um eine Sammlung von Ordnern auf einem Laufwerk zurückzugeben, auf die mindestens ein Monat lang nicht zugegriffen wurde, und dann alle diese Ordner komprimieren.</span><span class="sxs-lookup"><span data-stu-id="7caca-147">For example, you might write a script to return a collection of folders on a drive that have not been accessed for a month or more and then compress each of those folders.</span></span>

<span data-ttu-id="7caca-148">Der durch die Komprimierung von Ordnern freigegebene Speicherplatz variiert je nach Dateityp, der in diesem Ordner gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="7caca-148">The amount of disk space freed by compressing folders varies depending on the type of files stored in that folder.</span></span> <span data-ttu-id="7caca-149">Beispielsweise sind die JPG-Dateien bereits komprimiert, und die weitere Komprimierung hat kaum Auswirkungen auf die Größe der Datei.</span><span class="sxs-lookup"><span data-stu-id="7caca-149">For example, .jpg files are already compressed, and further compression has little effect on the size of the file.</span></span> <span data-ttu-id="7caca-150">Bei anderen Dateitypen können die Einsparungen jedoch beträchtlich sein.</span><span class="sxs-lookup"><span data-stu-id="7caca-150">With other file types, however, the savings can be considerable.</span></span> <span data-ttu-id="7caca-151">Beispielsweise wurde ein neuer Ordner auf einem Windows 2000-basierten Testcomputer erstellt, und es wurden 33 Microsoft Word-Dokumente mit einer Gesamtgröße von 15 Megabyte (MB) an Speicherplatz in diesen Ordner kopiert.</span><span class="sxs-lookup"><span data-stu-id="7caca-151">For example, a new folder was created on a Windows 2000-based test computer, and 33 Microsoft Word documents, taking up a total of 15 megabytes (MB) of disk space, were copied into that folder.</span></span> <span data-ttu-id="7caca-152">Wenn die Dokumente komprimiert wurden, benötigte der Ordner nur 7 MB Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="7caca-152">When the documents were compressed, the folder took up only 7 MB of disk space.</span></span>

## <a name="examples"></a><span data-ttu-id="7caca-153">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7caca-153">Examples</span></span>

<span data-ttu-id="7caca-154">Das folgende VBScript-Beispiel komprimiert den Ordner C: \\ Scripts.</span><span class="sxs-lookup"><span data-stu-id="7caca-154">The following VBScript sample compresses the folder C:\\Scripts.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFolders = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Directory WHERE Name = 'c:\\Scripts'")
For Each objFolder in colFolders
 errResults = objFolder.Compress
 Wscript.Echo errResults
Next
```



## <a name="requirements"></a><span data-ttu-id="7caca-155">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7caca-155">Requirements</span></span>



| <span data-ttu-id="7caca-156">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7caca-156">Requirement</span></span> | <span data-ttu-id="7caca-157">Wert</span><span class="sxs-lookup"><span data-stu-id="7caca-157">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7caca-158">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7caca-158">Minimum supported client</span></span><br/> | <span data-ttu-id="7caca-159">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7caca-159">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7caca-160">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7caca-160">Minimum supported server</span></span><br/> | <span data-ttu-id="7caca-161">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7caca-161">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7caca-162">Namespace</span><span class="sxs-lookup"><span data-stu-id="7caca-162">Namespace</span></span><br/>                | <span data-ttu-id="7caca-163">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7caca-163">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7caca-164">MOF</span><span class="sxs-lookup"><span data-stu-id="7caca-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7caca-165"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7caca-165"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7caca-166">DLL</span><span class="sxs-lookup"><span data-stu-id="7caca-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7caca-167"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7caca-167"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7caca-168">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7caca-168">See also</span></span>

<dl> <dt>

<span data-ttu-id="7caca-169">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7caca-169">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="7caca-170">**Win32- \_ Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="7caca-170">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> <dt>

[<span data-ttu-id="7caca-171">**Dekomprimieren**</span><span class="sxs-lookup"><span data-stu-id="7caca-171">**Uncompress**</span></span>](uncompress-method-in-class-win32-directory.md)
</dt> </dl>

 

