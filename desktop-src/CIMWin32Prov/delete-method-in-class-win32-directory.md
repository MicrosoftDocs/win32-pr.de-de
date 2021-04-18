---
description: Mit der DELETE WMI class-Methode wird die im Objekt Pfad angegebene logische Datei (oder das Verzeichnis) gelöscht.
ms.assetid: 5663b8a8-3089-475b-8a36-454a7315bfca
ms.tgt_platform: multiple
title: Delete-Methode der Win32_Directory-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 843583698c11c1b9ad8f08e83aa6e4b894b55db8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106340132"
---
# <a name="delete-method-of-the-win32_directory-class"></a><span data-ttu-id="2d526-103">Delete-Methode der Win32- \_ Verzeichnis Klasse</span><span class="sxs-lookup"><span data-stu-id="2d526-103">Delete method of the Win32\_Directory class</span></span>

<span data-ttu-id="2d526-104">Mit der **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) -Methode wird die im Objekt Pfad angegebene logische Datei (oder das Verzeichnis) gelöscht.</span><span class="sxs-lookup"><span data-stu-id="2d526-104">The **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method will delete the logical file (or directory) specified in the object path.</span></span>

<span data-ttu-id="2d526-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="2d526-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="2d526-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="2d526-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="2d526-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2d526-107">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="2d526-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2d526-108">Parameters</span></span>

<span data-ttu-id="2d526-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="2d526-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2d526-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2d526-110">Return value</span></span>

<span data-ttu-id="2d526-111">Gibt den Wert 0 (null) zurück, wenn die Datei erfolgreich gelöscht wurde, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="2d526-111">Returns a value of 0 (zero) if the file was successfully deleted, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="2d526-112">**0**</span><span class="sxs-lookup"><span data-stu-id="2d526-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="2d526-113">Die Anforderung wurde erfolgreich gesendet.</span><span class="sxs-lookup"><span data-stu-id="2d526-113">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="2d526-114">**2**</span><span class="sxs-lookup"><span data-stu-id="2d526-114">**2**</span></span>
</dt> <dd>

<span data-ttu-id="2d526-115">Der Zugriff wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="2d526-115">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="2d526-116">**8**</span><span class="sxs-lookup"><span data-stu-id="2d526-116">**8**</span></span>
</dt> <dd>

<span data-ttu-id="2d526-117">Ein nicht angegebener Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="2d526-117">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="2d526-118">**9**</span><span class="sxs-lookup"><span data-stu-id="2d526-118">**9**</span></span>
</dt> <dd>

<span data-ttu-id="2d526-119">Der angegebene Name war ungültig.</span><span class="sxs-lookup"><span data-stu-id="2d526-119">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="2d526-120">**10**</span><span class="sxs-lookup"><span data-stu-id="2d526-120">**10**</span></span>
</dt> <dd>

<span data-ttu-id="2d526-121">Das angegebene Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="2d526-121">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="2d526-122">**11**</span><span class="sxs-lookup"><span data-stu-id="2d526-122">**11**</span></span>
</dt> <dd>

<span data-ttu-id="2d526-123">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="2d526-123">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="2d526-124">**12**</span><span class="sxs-lookup"><span data-stu-id="2d526-124">**12**</span></span>
</dt> <dd>

<span data-ttu-id="2d526-125">Die Plattform ist nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="2d526-125">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="2d526-126">**13**</span><span class="sxs-lookup"><span data-stu-id="2d526-126">**13**</span></span>
</dt> <dd>

<span data-ttu-id="2d526-127">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="2d526-127">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="2d526-128">**14**</span><span class="sxs-lookup"><span data-stu-id="2d526-128">**14**</span></span>
</dt> <dd>

<span data-ttu-id="2d526-129">Das Verzeichnis ist nicht leer.</span><span class="sxs-lookup"><span data-stu-id="2d526-129">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="2d526-130">**15**</span><span class="sxs-lookup"><span data-stu-id="2d526-130">**15**</span></span>
</dt> <dd>

<span data-ttu-id="2d526-131">Es ist eine Freigabe Verletzung aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="2d526-131">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="2d526-132">**16**</span><span class="sxs-lookup"><span data-stu-id="2d526-132">**16**</span></span>
</dt> <dd>

<span data-ttu-id="2d526-133">Die angegebene Startdatei war ungültig.</span><span class="sxs-lookup"><span data-stu-id="2d526-133">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="2d526-134">**17**</span><span class="sxs-lookup"><span data-stu-id="2d526-134">**17**</span></span>
</dt> <dd>

<span data-ttu-id="2d526-135">Eine für den Vorgang erforderliche Berechtigung wird nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="2d526-135">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="2d526-136">**21**</span><span class="sxs-lookup"><span data-stu-id="2d526-136">**21**</span></span>
</dt> <dd>

<span data-ttu-id="2d526-137">Ein angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="2d526-137">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2d526-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2d526-138">Remarks</span></span>

<span data-ttu-id="2d526-139">Ordner sind nicht notwendigerweise permanente Ergänzungen zu einem Dateisystem.</span><span class="sxs-lookup"><span data-stu-id="2d526-139">Folders are not necessarily permanent additions to a file system.</span></span> <span data-ttu-id="2d526-140">Manchmal müssen Ordner gelöscht werden, da Sie möglicherweise nicht mehr benötigt werden, da sich die Rolle des Computers geändert hat oder die Ordner versehentlich erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="2d526-140">At some point, folders might need to be deleted, perhaps because they are no longer required, because the role of the computer has changed, or because the folders were created by mistake.</span></span>

<span data-ttu-id="2d526-141">Löschen ermöglicht es Ihnen, Ordner zu löschen: Sie binden einfach an den fraglichen Ordner und dann die Delete-Methode.</span><span class="sxs-lookup"><span data-stu-id="2d526-141">Delete allows you to delete folders: you simply bind to the folder in question and then call the Delete method.</span></span> <span data-ttu-id="2d526-142">Nachdem die Delete-Methode aufgerufen wurde, wird der Ordner dauerhaft aus dem Dateisystem entfernt. Er wird nicht an den Papierkorb gesendet.</span><span class="sxs-lookup"><span data-stu-id="2d526-142">After the Delete method is called, the folder is permanently removed from the file system; it is not sent to the Recycle Bin.</span></span> <span data-ttu-id="2d526-143">Außerdem wird keine Bestätigung angezeigt ("möchten Sie diesen Ordner wirklich löschen?").</span><span class="sxs-lookup"><span data-stu-id="2d526-143">In addition, no confirmation notice ("Are you sure you want to delete this folder?") is issued.</span></span> <span data-ttu-id="2d526-144">Stattdessen wird der Ordner sofort entfernt.</span><span class="sxs-lookup"><span data-stu-id="2d526-144">Instead, the folder is immediately removed.</span></span>

<span data-ttu-id="2d526-145">Sie können schreibgeschützte Ordner nicht mithilfe von FileSystemObject löschen. Dies kann jedoch mithilfe von WMI erfolgen.</span><span class="sxs-lookup"><span data-stu-id="2d526-145">You cannot delete read-only folders using the FileSystemObject; however, this can be done using WMI.</span></span> <span data-ttu-id="2d526-146">Wenn das Skript WMI verwendet und Sie keinen schreibgeschützten Ordner entfernen möchten, müssen Sie die lesbare Eigenschaft verwenden, um den Ordner Status zu überprüfen, bevor Sie ihn löschen.</span><span class="sxs-lookup"><span data-stu-id="2d526-146">If your script uses WMI and you do not want to remove a read-only folder, you must use the Readable property to check the folder status before deleting it.</span></span>

## <a name="examples"></a><span data-ttu-id="2d526-147">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2d526-147">Examples</span></span>

<span data-ttu-id="2d526-148">Das folgende VBScript-Codebeispiel löscht den Ordner C: \\ Scripts.</span><span class="sxs-lookup"><span data-stu-id="2d526-148">The following VBScript code sample deletes the folder C:\\Scripts.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFolders = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Directory WHERE Name = 'c:\\Scripts'")
For Each objFolder in colFolders
 errResults = objFolder.Delete
 Wscript.Echo errResults
Next
```



## <a name="requirements"></a><span data-ttu-id="2d526-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2d526-149">Requirements</span></span>



| <span data-ttu-id="2d526-150">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2d526-150">Requirement</span></span> | <span data-ttu-id="2d526-151">Wert</span><span class="sxs-lookup"><span data-stu-id="2d526-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2d526-152">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2d526-152">Minimum supported client</span></span><br/> | <span data-ttu-id="2d526-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2d526-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2d526-154">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2d526-154">Minimum supported server</span></span><br/> | <span data-ttu-id="2d526-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2d526-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2d526-156">Namespace</span><span class="sxs-lookup"><span data-stu-id="2d526-156">Namespace</span></span><br/>                | <span data-ttu-id="2d526-157">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="2d526-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2d526-158">MOF</span><span class="sxs-lookup"><span data-stu-id="2d526-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2d526-159"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2d526-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2d526-160">DLL</span><span class="sxs-lookup"><span data-stu-id="2d526-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d526-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d526-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d526-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2d526-162">See also</span></span>

<dl> <dt>

<span data-ttu-id="2d526-163">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2d526-163">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="2d526-164">**Win32- \_ Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="2d526-164">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

