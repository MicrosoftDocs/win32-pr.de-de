---
description: Benennt die im Objekt Pfad angegebene Verzeichniseintrags Datei um.
ms.assetid: 8bfe1b69-5f93-4408-a742-f03a9cb16bfe
ms.tgt_platform: multiple
title: Rename-Methode der Win32_Directory-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 874151e1ff8c9feca375df3eb441665863d1070d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346621"
---
# <a name="rename-method-of-the-win32_directory-class"></a><span data-ttu-id="ab595-103">Rename-Methode der Win32- \_ Verzeichnis Klasse</span><span class="sxs-lookup"><span data-stu-id="ab595-103">Rename method of the Win32\_Directory class</span></span>

<span data-ttu-id="ab595-104">Die Methode zum **Umbenennen** der [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) benennt die Verzeichniseintrags Datei um, die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="ab595-104">The **Rename** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method renames the directory entry file specified in the object path.</span></span> <span data-ttu-id="ab595-105">Ein umbenennen wird nicht unterstützt, wenn sich das Ziel auf einem anderen Laufwerk befindet oder wenn eine vorhandene logische Datei überschrieben werden muss.</span><span class="sxs-lookup"><span data-stu-id="ab595-105">A rename is not supported if the destination is on another drive or if overwriting an existing logical file is required.</span></span>

<span data-ttu-id="ab595-106">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="ab595-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="ab595-107">Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="ab595-107">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="ab595-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ab595-108">Syntax</span></span>


```mof
uint32 Rename(
   string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="ab595-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ab595-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab595-110">*FileName*</span><span class="sxs-lookup"><span data-stu-id="ab595-110">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="ab595-111">Voll qualifizierter neuer Name der Datei (oder des Verzeichnisses).</span><span class="sxs-lookup"><span data-stu-id="ab595-111">Fully qualified new name of the file (or directory).</span></span> <span data-ttu-id="ab595-112">Beispiel: c: \\ Temp \\newfile.txt.</span><span class="sxs-lookup"><span data-stu-id="ab595-112">Example: c:\\temp\\newfile.txt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab595-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ab595-113">Return value</span></span>

<span data-ttu-id="ab595-114">Gibt den Wert 0 (null) zurück, wenn die Datei erfolgreich umbenannt wurde, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="ab595-114">Returns a value of 0 (zero) if the file was successfully renamed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="ab595-115">**0**</span><span class="sxs-lookup"><span data-stu-id="ab595-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="ab595-116">Die Anforderung wurde erfolgreich gesendet.</span><span class="sxs-lookup"><span data-stu-id="ab595-116">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="ab595-117">**2**</span><span class="sxs-lookup"><span data-stu-id="ab595-117">**2**</span></span>
</dt> <dd>

<span data-ttu-id="ab595-118">Der Zugriff wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="ab595-118">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="ab595-119">**8**</span><span class="sxs-lookup"><span data-stu-id="ab595-119">**8**</span></span>
</dt> <dd>

<span data-ttu-id="ab595-120">Ein nicht angegebener Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="ab595-120">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="ab595-121">**9**</span><span class="sxs-lookup"><span data-stu-id="ab595-121">**9**</span></span>
</dt> <dd>

<span data-ttu-id="ab595-122">Der angegebene Name war ungültig.</span><span class="sxs-lookup"><span data-stu-id="ab595-122">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="ab595-123">**10**</span><span class="sxs-lookup"><span data-stu-id="ab595-123">**10**</span></span>
</dt> <dd>

<span data-ttu-id="ab595-124">Das angegebene Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ab595-124">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="ab595-125">**11**</span><span class="sxs-lookup"><span data-stu-id="ab595-125">**11**</span></span>
</dt> <dd>

<span data-ttu-id="ab595-126">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="ab595-126">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="ab595-127">**12**</span><span class="sxs-lookup"><span data-stu-id="ab595-127">**12**</span></span>
</dt> <dd>

<span data-ttu-id="ab595-128">Die Plattform ist nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="ab595-128">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="ab595-129">**13**</span><span class="sxs-lookup"><span data-stu-id="ab595-129">**13**</span></span>
</dt> <dd>

<span data-ttu-id="ab595-130">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="ab595-130">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="ab595-131">**14**</span><span class="sxs-lookup"><span data-stu-id="ab595-131">**14**</span></span>
</dt> <dd>

<span data-ttu-id="ab595-132">Das Verzeichnis ist nicht leer.</span><span class="sxs-lookup"><span data-stu-id="ab595-132">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="ab595-133">**15**</span><span class="sxs-lookup"><span data-stu-id="ab595-133">**15**</span></span>
</dt> <dd>

<span data-ttu-id="ab595-134">Es ist eine Freigabe Verletzung aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="ab595-134">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="ab595-135">**16**</span><span class="sxs-lookup"><span data-stu-id="ab595-135">**16**</span></span>
</dt> <dd>

<span data-ttu-id="ab595-136">Die angegebene Startdatei war ungültig.</span><span class="sxs-lookup"><span data-stu-id="ab595-136">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="ab595-137">**17**</span><span class="sxs-lookup"><span data-stu-id="ab595-137">**17**</span></span>
</dt> <dd>

<span data-ttu-id="ab595-138">Eine für den Vorgang erforderliche Berechtigung wird nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="ab595-138">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="ab595-139">**21**</span><span class="sxs-lookup"><span data-stu-id="ab595-139">**21**</span></span>
</dt> <dd>

<span data-ttu-id="ab595-140">Ein angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="ab595-140">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ab595-141">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ab595-141">Remarks</span></span>

<span data-ttu-id="ab595-142">Zum Umbenennen eines Ordners müssen Sie zuerst eine Bindung an den fraglichen Ordner herstellen und dann die Rename-Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="ab595-142">To rename a folder, first bind to the folder in question and then call the Rename method.</span></span> <span data-ttu-id="ab595-143">Übergeben Sie als einzigen Parameter für die-Methode den neuen Namen für den Ordner als einen kompletten Pfadnamen.</span><span class="sxs-lookup"><span data-stu-id="ab595-143">As the sole parameter to the method, pass the new name for the folder as a complete path name.</span></span> <span data-ttu-id="ab595-144">Wenn beispielsweise der Ordner in der Datei "c: Scripts" die \\ \\ Sicherung " \\ c: Scripts Archive" umbenennen soll \\ \\ , müssen Sie c: \\ Scripts \\ Archive als den gesamten Ordnernamen übergeben.</span><span class="sxs-lookup"><span data-stu-id="ab595-144">For example, if the folder in the C:\\Scripts\\Logs\\Backup is to be renamed C:\\Scripts\\Archive, you must pass C:\\Scripts\\Archive as the complete folder name.</span></span> <span data-ttu-id="ab595-145">Wenn nur der Ordnername-Archive übergeben wird, führt dies zu einem ungültigen Pfad Fehler.</span><span class="sxs-lookup"><span data-stu-id="ab595-145">Passing only the folder name - Archive - results in an Invalid path error.</span></span>

<span data-ttu-id="ab595-146">Die Win32- \_ Verzeichnis Klasse bietet keine einstufige Methode zum Verschieben von Ordnern.</span><span class="sxs-lookup"><span data-stu-id="ab595-146">The Win32\_Directory class does not provide a one-step method for moving folders.</span></span> <span data-ttu-id="ab595-147">Stattdessen umfasst das Verschieben eines Ordners im Allgemeinen zwei Schritte:</span><span class="sxs-lookup"><span data-stu-id="ab595-147">Instead, moving a folder generally involves two steps:</span></span>

<dl> 1. <span data-ttu-id="ab595-148">Der Ordner wird an den neuen Speicherort kopiert.</span><span class="sxs-lookup"><span data-stu-id="ab595-148">Copying the folder to its new location</span></span>  
2. <span data-ttu-id="ab595-149">Löschen des ursprünglichen Ordners</span><span class="sxs-lookup"><span data-stu-id="ab595-149">Deleting the original folder</span></span>  
</dl>

<span data-ttu-id="ab595-150">Die einzige Ausnahme zu diesem zweistufigen Prozess besteht darin, einen Ordner an einen neuen Speicherort auf demselben Laufwerk zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="ab595-150">The one exception to this two-step process involves moving a folder to a new location on the same drive.</span></span> <span data-ttu-id="ab595-151">Nehmen Sie beispielsweise an, dass Sie "c: \\ Temp" in "c: \\ Scripts \\ temporäre Dateien \\ Archive" verschieben möchten.</span><span class="sxs-lookup"><span data-stu-id="ab595-151">For example, suppose you want to move C:\\Temp to C:\\Scripts\\Temporary Files\\Archive.</span></span> <span data-ttu-id="ab595-152">Solange sich der aktuelle Speicherort und der neue Speicherort auf demselben Laufwerk befinden, können Sie den Ordner verschieben, indem Sie einfach die Rename-Methode aufrufen und den neuen Speicherort als Methoden Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="ab595-152">As long as the current location and the new location are on the same drive, you can move the folder by simply calling the Rename method and passing the new location as the method parameter.</span></span> <span data-ttu-id="ab595-153">Diese Vorgehensweise ermöglicht es Ihnen, den Ordner in einem einzigen Schritt zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="ab595-153">This approach effectively allows you to move the folder in a single step.</span></span> <span data-ttu-id="ab595-154">Das Skript schlägt jedoch fehl, wenn sich das aktuelle Laufwerk und das neue Laufwerk unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="ab595-154">However, the script fails if the current drive and the new drive are different.</span></span> <span data-ttu-id="ab595-155">Der Versuch, C: \\ Temp in D: Temp umzubenennen, \\ schlägt mit dem Fehler "Laufwerk nicht identisch" fehl.</span><span class="sxs-lookup"><span data-stu-id="ab595-155">An attempt to rename C:\\Temp to D:\\Temp fails with a "Drive not the same" error.</span></span>

## <a name="examples"></a><span data-ttu-id="ab595-156">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ab595-156">Examples</span></span>

<span data-ttu-id="ab595-157">Der folgende Code aus dem Beispiel zum [Verschieben eines Ordners mit WMI](https://Gallery.TechNet.Microsoft.Com/f4f9643c-d7ed-4f54-b155-c6515396431f) VBScript in der TechNet Gallery verwendet die Rename-Methode, um den Ordner c: \\ Scripts in c: \\ Admins \\ Documents \\ Archive \\ VBScript zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="ab595-157">The following code, from the [Move a Folder Using WMI](https://Gallery.TechNet.Microsoft.Com/f4f9643c-d7ed-4f54-b155-c6515396431f) VBScript sample on TechNet Gallery, uses the Rename method to move the folder C:\\Scripts to C:\\Admins\\Documents\\Archive\\VBScript.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colFolders = objWMIService.ExecQuery _ 
    ("Select * from Win32_Directory where name = 'c:\\Scripts'") 
 
For Each objFolder in colFolders 
    errResults = objFolder.Rename("C:\Admins\Documents\Archive\VBScript") 
Next
```



## <a name="requirements"></a><span data-ttu-id="ab595-158">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ab595-158">Requirements</span></span>



| <span data-ttu-id="ab595-159">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ab595-159">Requirement</span></span> | <span data-ttu-id="ab595-160">Wert</span><span class="sxs-lookup"><span data-stu-id="ab595-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab595-161">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ab595-161">Minimum supported client</span></span><br/> | <span data-ttu-id="ab595-162">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ab595-162">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ab595-163">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ab595-163">Minimum supported server</span></span><br/> | <span data-ttu-id="ab595-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ab595-164">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ab595-165">Namespace</span><span class="sxs-lookup"><span data-stu-id="ab595-165">Namespace</span></span><br/>                | <span data-ttu-id="ab595-166">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ab595-166">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ab595-167">MOF</span><span class="sxs-lookup"><span data-stu-id="ab595-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ab595-168"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ab595-168"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ab595-169">DLL</span><span class="sxs-lookup"><span data-stu-id="ab595-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab595-170"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab595-170"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab595-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ab595-171">See also</span></span>

<dl> <dt>

<span data-ttu-id="ab595-172">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ab595-172">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="ab595-173">**Win32- \_ Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="ab595-173">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

