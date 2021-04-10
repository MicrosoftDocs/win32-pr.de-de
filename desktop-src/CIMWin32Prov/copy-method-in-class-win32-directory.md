---
description: Kopiert die im Objekt Pfad angegebene Datei bzw. das Verzeichnis für den logischen Verzeichniseintrag an den Speicherort, der durch den Eingabeparameter angegeben wird.
ms.assetid: 038e23d7-71db-4db6-8fb1-e84e972510c9
ms.tgt_platform: multiple
title: Copy-Methode der Win32_Directory-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.Copy
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 25568167d9532303a7cbee794757bc674a378b39
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126924"
---
# <a name="copy-method-of-the-win32_directory-class"></a><span data-ttu-id="b20f9-103">Copy-Methode der Win32- \_ Verzeichnis Klasse</span><span class="sxs-lookup"><span data-stu-id="b20f9-103">Copy method of the Win32\_Directory class</span></span>

<span data-ttu-id="b20f9-104">Die **Copy** - [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode kopiert die im Objekt Pfad angegebene Datei bzw. das Verzeichnis für den logischen Verzeichniseintrag in den Speicherort, der durch den Eingabeparameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b20f9-104">The **Copy** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method copies the logical directory entry file or directory specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="b20f9-105">Eine Kopie wird nicht unterstützt, wenn eine vorhandene logische Datei überschrieben werden muss.</span><span class="sxs-lookup"><span data-stu-id="b20f9-105">A copy is not supported if overwriting an existing logical file is required.</span></span>

<span data-ttu-id="b20f9-106">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="b20f9-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="b20f9-107">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="b20f9-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="b20f9-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b20f9-108">Syntax</span></span>


```mof
uint32 Copy(
   string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="b20f9-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b20f9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b20f9-110">*FileName*</span><span class="sxs-lookup"><span data-stu-id="b20f9-110">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="b20f9-111">Der voll qualifizierte Name der Kopie der Datei (oder des Verzeichnisses).</span><span class="sxs-lookup"><span data-stu-id="b20f9-111">Fully qualified name of the copy of the file (or directory).</span></span> <span data-ttu-id="b20f9-112">Beispiel: c: \\ Temp \\ NewDirectory</span><span class="sxs-lookup"><span data-stu-id="b20f9-112">Example: c:\\temp\\newdirectory</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b20f9-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b20f9-113">Return value</span></span>

<span data-ttu-id="b20f9-114">Gibt den Wert 0 (null) zurück, wenn die Datei erfolgreich kopiert wurde, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="b20f9-114">Returns a value of 0 (zero) if the file was successfully copied, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="b20f9-115">**0**</span><span class="sxs-lookup"><span data-stu-id="b20f9-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="b20f9-116">Die Anforderung wurde erfolgreich gesendet.</span><span class="sxs-lookup"><span data-stu-id="b20f9-116">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="b20f9-117">**2**</span><span class="sxs-lookup"><span data-stu-id="b20f9-117">**2**</span></span>
</dt> <dd>

<span data-ttu-id="b20f9-118">Der Zugriff wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="b20f9-118">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="b20f9-119">**8**</span><span class="sxs-lookup"><span data-stu-id="b20f9-119">**8**</span></span>
</dt> <dd>

<span data-ttu-id="b20f9-120">Ein nicht angegebener Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="b20f9-120">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="b20f9-121">**9**</span><span class="sxs-lookup"><span data-stu-id="b20f9-121">**9**</span></span>
</dt> <dd>

<span data-ttu-id="b20f9-122">Der angegebene Name war ungültig.</span><span class="sxs-lookup"><span data-stu-id="b20f9-122">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="b20f9-123">**10**</span><span class="sxs-lookup"><span data-stu-id="b20f9-123">**10**</span></span>
</dt> <dd>

<span data-ttu-id="b20f9-124">Das angegebene Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="b20f9-124">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="b20f9-125">**11**</span><span class="sxs-lookup"><span data-stu-id="b20f9-125">**11**</span></span>
</dt> <dd>

<span data-ttu-id="b20f9-126">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="b20f9-126">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="b20f9-127">**12**</span><span class="sxs-lookup"><span data-stu-id="b20f9-127">**12**</span></span>
</dt> <dd>

<span data-ttu-id="b20f9-128">Die Plattform ist nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="b20f9-128">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="b20f9-129">**13**</span><span class="sxs-lookup"><span data-stu-id="b20f9-129">**13**</span></span>
</dt> <dd>

<span data-ttu-id="b20f9-130">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="b20f9-130">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="b20f9-131">**14**</span><span class="sxs-lookup"><span data-stu-id="b20f9-131">**14**</span></span>
</dt> <dd>

<span data-ttu-id="b20f9-132">Das Verzeichnis ist nicht leer.</span><span class="sxs-lookup"><span data-stu-id="b20f9-132">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="b20f9-133">**15**</span><span class="sxs-lookup"><span data-stu-id="b20f9-133">**15**</span></span>
</dt> <dd>

<span data-ttu-id="b20f9-134">Es ist eine Freigabe Verletzung aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="b20f9-134">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="b20f9-135">**16**</span><span class="sxs-lookup"><span data-stu-id="b20f9-135">**16**</span></span>
</dt> <dd>

<span data-ttu-id="b20f9-136">Die angegebene Startdatei war ungültig.</span><span class="sxs-lookup"><span data-stu-id="b20f9-136">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="b20f9-137">**17**</span><span class="sxs-lookup"><span data-stu-id="b20f9-137">**17**</span></span>
</dt> <dd>

<span data-ttu-id="b20f9-138">Eine für den Vorgang erforderliche Berechtigung wird nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="b20f9-138">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="b20f9-139">**21**</span><span class="sxs-lookup"><span data-stu-id="b20f9-139">**21**</span></span>
</dt> <dd>

<span data-ttu-id="b20f9-140">Ein angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="b20f9-140">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b20f9-141">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b20f9-141">Remarks</span></span>

<span data-ttu-id="b20f9-142">Ordner müssen häufig von einem Speicherort in einen anderen kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="b20f9-142">Folders often need to be copied from one location to another.</span></span> <span data-ttu-id="b20f9-143">Beispielsweise können Sie einen Ordner von einem Server auf einen anderen kopieren, um eine Sicherungskopie dieses Ordners zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b20f9-143">For example, you might copy a folder from one server to another to create a backup copy of that folder.</span></span> <span data-ttu-id="b20f9-144">Möglicherweise verfügen Sie auch über einen Vorlagen Ordner, der auf Benutzer Arbeitsstationen kopiert werden muss, oder einen Skript Ordner, der auf alle DNS-Server kopiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b20f9-144">Or you might have a templates folder that needs to be copied to user workstations, or a scripts folder that should be copied to all of your DNS servers.</span></span>

<span data-ttu-id="b20f9-145">Mit der Win32- \_ Verzeichnis Kopiermethode können Sie einen Ordner von einem Speicherort auf einen anderen kopieren (z. b. Kopieren eines Ordners von Laufwerk C auf Laufwerk D) oder auf einem Remote Computer.</span><span class="sxs-lookup"><span data-stu-id="b20f9-145">The Win32\_Directory Copy method enables you to copy a folder from one location to another, either on the same computer (for example, copying a folder from drive C to drive D) or on a remote computer.</span></span> <span data-ttu-id="b20f9-146">Um einen Ordner zu kopieren, geben Sie eine Instanz des Ordners zurück, die kopiert werden soll, und dann die Kopiermethode, wobei Sie als Parameter den Zielort für die neue Kopie des Ordners übergeben.</span><span class="sxs-lookup"><span data-stu-id="b20f9-146">To copy a folder, you return an instance of the folder to be copied and then call the Copy method, passing as a parameter the target location for the new copy of the folder.</span></span> <span data-ttu-id="b20f9-147">Diese Codezeile kopiert z. b. einen Ordner in den Ordner Scripts auf Laufwerk F:</span><span class="sxs-lookup"><span data-stu-id="b20f9-147">For example, this line of code copies a folder to the Scripts folder on drive F:</span></span>

`objFolder.Copy("F:\Scripts")`

<span data-ttu-id="b20f9-148">Ein vorhandener Ordner wird von WMI beim Ausführen der Kopiermethode nicht überschrieben.</span><span class="sxs-lookup"><span data-stu-id="b20f9-148">WMI will not overwrite an existing folder when executing the Copy method.</span></span> <span data-ttu-id="b20f9-149">Dies bedeutet, dass der Kopiervorgang fehlschlägt, wenn der Zielordner vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="b20f9-149">This means that the copy operation fails if the destination folder exists.</span></span> <span data-ttu-id="b20f9-150">Angenommen, Sie verfügen über einen Ordner mit dem Namen "Scripts", und Sie versuchen, diesen Ordner auf eine Remote Freigabe namens " \\ \\ ATL-fs-01 Archive" zu kopieren \\ .</span><span class="sxs-lookup"><span data-stu-id="b20f9-150">For example, suppose you have a folder named Scripts and you attempt to copy that folder to a remote share named \\\\atl-fs-01\\archive.</span></span> <span data-ttu-id="b20f9-151">Wenn ein Ordner mit dem Namen Skripts auf dieser Freigabe bereits vorhanden ist, schlägt der Kopiervorgang fehl.</span><span class="sxs-lookup"><span data-stu-id="b20f9-151">If a folder named Scripts already exists on that share, the copy operation fails.</span></span>

## <a name="examples"></a><span data-ttu-id="b20f9-152">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b20f9-152">Examples</span></span>

<span data-ttu-id="b20f9-153">Mit dem folgenden Codebeispiel, das aus dem [Kopieren eines Ordners mithilfe von WMI](https://Gallery.TechNet.Microsoft.Com/71b8f517-0240-42a2-be5c-e5a3921604d2)stammt, wird die Copy-Methode verwendet, um den Ordner C: \\ Scripts in D: Archive zu kopieren \\ .</span><span class="sxs-lookup"><span data-stu-id="b20f9-153">The followng code sample, taken from the [Copy a Folder Using WMI](https://Gallery.TechNet.Microsoft.Com/71b8f517-0240-42a2-be5c-e5a3921604d2), uses the Copy method to copy the folder C:\\Scripts to D:\\Archive.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colFolders = objWMIService.ExecQuery( _ 
    "Select * from Win32_Directory where Name = 'c:\\Scripts'") 
 
For Each objFolder in colFolders 
    errResults  = objFolder.Copy("D:\Archive") 
Next
```



## <a name="requirements"></a><span data-ttu-id="b20f9-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b20f9-154">Requirements</span></span>



| <span data-ttu-id="b20f9-155">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b20f9-155">Requirement</span></span> | <span data-ttu-id="b20f9-156">Wert</span><span class="sxs-lookup"><span data-stu-id="b20f9-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b20f9-157">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b20f9-157">Minimum supported client</span></span><br/> | <span data-ttu-id="b20f9-158">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b20f9-158">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b20f9-159">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b20f9-159">Minimum supported server</span></span><br/> | <span data-ttu-id="b20f9-160">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b20f9-160">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b20f9-161">Namespace</span><span class="sxs-lookup"><span data-stu-id="b20f9-161">Namespace</span></span><br/>                | <span data-ttu-id="b20f9-162">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b20f9-162">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b20f9-163">MOF</span><span class="sxs-lookup"><span data-stu-id="b20f9-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b20f9-164"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b20f9-164"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b20f9-165">DLL</span><span class="sxs-lookup"><span data-stu-id="b20f9-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b20f9-166"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b20f9-166"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b20f9-167">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b20f9-167">See also</span></span>

<dl> <dt>

<span data-ttu-id="b20f9-168">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b20f9-168">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="b20f9-169">**Win32- \_ Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="b20f9-169">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

