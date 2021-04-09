---
description: Gibt eine UInt32-Bitmap mit den Zugriffsrechten für die Freigabe zurück, die der Benutzer oder die Gruppe hat, in deren Auftrag die Instanz zurückgegeben wird.
ms.assetid: 234f44a4-ffff-431d-a973-98f2bd313c7d
ms.tgt_platform: multiple
title: Getaccessmask-Methode der Win32_Share-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share.GetAccessMask
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 745ce6d607adf84827c14a588640572b5d92be00
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958312"
---
# <a name="getaccessmask-method-of-the-win32_share-class"></a><span data-ttu-id="df4a2-103">Getaccessmask-Methode der Win32- \_ Freigabe Klasse</span><span class="sxs-lookup"><span data-stu-id="df4a2-103">GetAccessMask method of the Win32\_Share class</span></span>

<span data-ttu-id="df4a2-104">Die **getaccessmask** -Methode gibt eine UInt32-Bitmap mit den Zugriffsrechten für die Freigabe zurück, die der Benutzer oder die Gruppe hat, in deren Auftrag die Instanz zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="df4a2-104">The **GetAccessMask** method returns a uint32 bitmap with the access rights to the share held by the user or group on whose behalf the instance is returned.</span></span>

<span data-ttu-id="df4a2-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="df4a2-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="df4a2-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="df4a2-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="df4a2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="df4a2-107">Syntax</span></span>


```mof
uint32 GetAccessMask();
```



## <a name="parameters"></a><span data-ttu-id="df4a2-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="df4a2-108">Parameters</span></span>

<span data-ttu-id="df4a2-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="df4a2-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="df4a2-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="df4a2-110">Return value</span></span>

<span data-ttu-id="df4a2-111">Zugriffsrechte für die Freigabe, die der Benutzer oder die Gruppe innehat.</span><span class="sxs-lookup"><span data-stu-id="df4a2-111">Access rights to the share held by the user or group.</span></span>

<dl> <dt>

<span data-ttu-id="df4a2-112">**Datei \_ Listen \_ Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="df4a2-112">**FILE\_LIST\_DIRECTORY**</span></span>
</dt> <dd>

<span data-ttu-id="df4a2-113">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="df4a2-113">1 (0x1)</span></span>

<span data-ttu-id="df4a2-114">Gewährt das Recht, Daten aus der Datei zu lesen.</span><span class="sxs-lookup"><span data-stu-id="df4a2-114">Grants the right to read data from the file.</span></span> <span data-ttu-id="df4a2-115">Bei einem Verzeichnis gewährt dieser Wert das Recht, den Inhalt des Verzeichnisses aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="df4a2-115">For a directory, this value grants the right to list the contents of the directory.</span></span>

</dd> <dt>

<span data-ttu-id="df4a2-116">**Datei \_ Hinzufügen \_**</span><span class="sxs-lookup"><span data-stu-id="df4a2-116">**FILE\_ADD\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="df4a2-117">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="df4a2-117">2 (0x2)</span></span>

<span data-ttu-id="df4a2-118">Gewährt das Recht, Daten in die Datei zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="df4a2-118">Grants the right to write data to the file.</span></span> <span data-ttu-id="df4a2-119">Bei einem Verzeichnis gewährt dieser Wert das Recht, eine Datei im Verzeichnis zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="df4a2-119">For a directory, this value grants the right to create a file in the directory.</span></span>

</dd> <dt>

<span data-ttu-id="df4a2-120">**\_Unterverzeichnis "Datei hinzufügen" \_**</span><span class="sxs-lookup"><span data-stu-id="df4a2-120">**FILE\_ADD\_SUBDIRECTORY**</span></span>
</dt> <dd>

<span data-ttu-id="df4a2-121">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="df4a2-121">4 (0x4)</span></span>

<span data-ttu-id="df4a2-122">Gewährt das Recht zum Anfügen von Daten an die Datei.</span><span class="sxs-lookup"><span data-stu-id="df4a2-122">Grants the right to append data to the file.</span></span> <span data-ttu-id="df4a2-123">Bei einem Verzeichnis gewährt dieser Wert das Recht, ein Unterverzeichnis zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="df4a2-123">For a directory, this value grants the right to create a subdirectory.</span></span>

</dd> <dt>

<span data-ttu-id="df4a2-124">**Datei \_ Lese- \_ EA**</span><span class="sxs-lookup"><span data-stu-id="df4a2-124">**FILE\_READ\_EA**</span></span>
</dt> <dd>

<span data-ttu-id="df4a2-125">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="df4a2-125">8 (0x8)</span></span>

<span data-ttu-id="df4a2-126">Gewährt das Recht zum Lesen erweiterter Attribute.</span><span class="sxs-lookup"><span data-stu-id="df4a2-126">Grants the right to read extended attributes.</span></span>

</dd> <dt>

<span data-ttu-id="df4a2-127">**Datei \_ Schreib- \_ EA**</span><span class="sxs-lookup"><span data-stu-id="df4a2-127">**FILE\_WRITE\_EA**</span></span>
</dt> <dd>

<span data-ttu-id="df4a2-128">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="df4a2-128">16 (0x10)</span></span>

<span data-ttu-id="df4a2-129">Gewährt das Recht, erweiterte Attribute zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="df4a2-129">Grants the right to write extended attributes.</span></span>

</dd> <dt>

<span data-ttu-id="df4a2-130">**Datei \_ Durchlauf**</span><span class="sxs-lookup"><span data-stu-id="df4a2-130">**FILE\_TRAVERSE**</span></span>
</dt> <dd>

<span data-ttu-id="df4a2-131">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="df4a2-131">32 (0x20)</span></span>

<span data-ttu-id="df4a2-132">Gewährt das Recht, eine Datei auszuführen.</span><span class="sxs-lookup"><span data-stu-id="df4a2-132">Grants the right to execute a file.</span></span> <span data-ttu-id="df4a2-133">Für ein Verzeichnis kann das Verzeichnis durchsucht werden.</span><span class="sxs-lookup"><span data-stu-id="df4a2-133">For a directory, the directory can be traversed.</span></span>

</dd> <dt>

<span data-ttu-id="df4a2-134">**Datei \_ Delete \_ Child**</span><span class="sxs-lookup"><span data-stu-id="df4a2-134">**FILE\_DELETE\_CHILD**</span></span>
</dt> <dd>

<span data-ttu-id="df4a2-135">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="df4a2-135">64 (0x40)</span></span>

<span data-ttu-id="df4a2-136">Gewährt das Recht, ein Verzeichnis und alle darin enthaltenen Dateien (seine untergeordneten Elemente) zu löschen, selbst wenn die Dateien schreibgeschützt sind.</span><span class="sxs-lookup"><span data-stu-id="df4a2-136">Grants the right to delete a directory and all of the files it contains (its children), even if the files are read-only.</span></span>

</dd> <dt>

<span data-ttu-id="df4a2-137">**Datei \_ Lese \_ Attribute**</span><span class="sxs-lookup"><span data-stu-id="df4a2-137">**FILE\_READ\_ATTRIBUTES**</span></span>
</dt> <dd>

<span data-ttu-id="df4a2-138">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="df4a2-138">128 (0x80)</span></span>

<span data-ttu-id="df4a2-139">Gewährt das Recht zum Lesen von Dateiattributen.</span><span class="sxs-lookup"><span data-stu-id="df4a2-139">Grants the right to read file attributes.</span></span>

</dd> <dt>

<span data-ttu-id="df4a2-140">**Datei \_ Schreib \_ Attribute**</span><span class="sxs-lookup"><span data-stu-id="df4a2-140">**FILE\_WRITE\_ATTRIBUTES**</span></span>
</dt> <dd>

<span data-ttu-id="df4a2-141">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="df4a2-141">256 (0x100)</span></span>

<span data-ttu-id="df4a2-142">Erteilt das Recht, Dateiattribute zu ändern.</span><span class="sxs-lookup"><span data-stu-id="df4a2-142">Grants the right to change file attributes.</span></span>

</dd> <dt>

<span data-ttu-id="df4a2-143">**DELETE**</span><span class="sxs-lookup"><span data-stu-id="df4a2-143">**DELETE**</span></span>
</dt> <dd>

<span data-ttu-id="df4a2-144">65536 (0x10000)</span><span class="sxs-lookup"><span data-stu-id="df4a2-144">65536 (0x10000)</span></span>

<span data-ttu-id="df4a2-145">Gewährt Lösch Zugriff.</span><span class="sxs-lookup"><span data-stu-id="df4a2-145">Grants delete access.</span></span>

</dd> <dt>

<span data-ttu-id="df4a2-146">**Lese \_ Steuerelement**</span><span class="sxs-lookup"><span data-stu-id="df4a2-146">**READ\_CONTROL**</span></span>
</dt> <dd>

<span data-ttu-id="df4a2-147">131072 (0x20000)</span><span class="sxs-lookup"><span data-stu-id="df4a2-147">131072 (0x20000)</span></span>

<span data-ttu-id="df4a2-148">Gewährt Lesezugriff auf die Sicherheits Beschreibung und den Besitzer.</span><span class="sxs-lookup"><span data-stu-id="df4a2-148">Grants read access to the security descriptor and owner.</span></span>

</dd> <dt>

<span data-ttu-id="df4a2-149">**\_DAC schreiben**</span><span class="sxs-lookup"><span data-stu-id="df4a2-149">**WRITE\_DAC**</span></span>
</dt> <dd>

<span data-ttu-id="df4a2-150">262144 (0x40000)</span><span class="sxs-lookup"><span data-stu-id="df4a2-150">262144 (0x40000)</span></span>

<span data-ttu-id="df4a2-151">Gewährt Schreibzugriff auf die freigegebene Zugriffs Steuerungs Liste (DACL).</span><span class="sxs-lookup"><span data-stu-id="df4a2-151">Grants write access to the discretionary access control list (DACL).</span></span>

</dd> <dt>

<span data-ttu-id="df4a2-152">**\_Besitzer schreiben**</span><span class="sxs-lookup"><span data-stu-id="df4a2-152">**WRITE\_OWNER**</span></span>
</dt> <dd>

<span data-ttu-id="df4a2-153">524288 (0x80000)</span><span class="sxs-lookup"><span data-stu-id="df4a2-153">524288 (0x80000)</span></span>

<span data-ttu-id="df4a2-154">Weist den Schreib Besitzer zu.</span><span class="sxs-lookup"><span data-stu-id="df4a2-154">Assigns the write owner.</span></span>

</dd> <dt>

<span data-ttu-id="df4a2-155">**SYNCHRONIZE**</span><span class="sxs-lookup"><span data-stu-id="df4a2-155">**SYNCHRONIZE**</span></span>
</dt> <dd>

<span data-ttu-id="df4a2-156">1048576 (0x100000)</span><span class="sxs-lookup"><span data-stu-id="df4a2-156">1048576 (0x100000)</span></span>

<span data-ttu-id="df4a2-157">Synchronisiert den Zugriff und ermöglicht es einem Prozess zu warten, bis ein Objekt in den signalisierten Zustand wechselt.</span><span class="sxs-lookup"><span data-stu-id="df4a2-157">Synchronizes access and allows a process to wait for an object to enter the signaled state.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="df4a2-158">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="df4a2-158">Remarks</span></span>

<span data-ttu-id="df4a2-159">Die **getaccessmask** -Methode ist eine Objektmethode und wird bei einem Vorkommen dieser Klasse verwendet.</span><span class="sxs-lookup"><span data-stu-id="df4a2-159">**GetAccessMask** method is an object method and is used on an occurrence of this class.</span></span>

## <a name="examples"></a><span data-ttu-id="df4a2-160">Beispiele</span><span class="sxs-lookup"><span data-stu-id="df4a2-160">Examples</span></span>

<span data-ttu-id="df4a2-161">Im folgenden VBScript-Codebeispiel wird ein Freigabe Ordner erstellt und dann der Wert der Zugriffs Maske in der Sicherheits Beschreibung abgerufen, mit der der Freigabe Ordner gesichert wird.</span><span class="sxs-lookup"><span data-stu-id="df4a2-161">The following VBScript code example creates a share folder and then gets the value of the access mask in the security descriptor that secures the share folder.</span></span>


```VB
Const FILE_SHARE = 0
Const MAXIMUM_CONNECTIONS = 4000 
strComputer = "."

Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set objNewShare = objWMIService.Get("Win32_Share")
Return = objNewShare.Create ("C:\Temp", "TestShare", FILE_SHARE, MAXIMUM_CONNECTIONS, "test share")

If Return <> 0 Then
          WScript.Echo Return
          WScript.Quit
End If

Set objShare = objWMIService.Get("Win32_Share.Name='TestShare'")
Return = objShare.GetAccessMask
WScript.Echo Return
```



## <a name="requirements"></a><span data-ttu-id="df4a2-162">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="df4a2-162">Requirements</span></span>



| <span data-ttu-id="df4a2-163">Anforderung</span><span class="sxs-lookup"><span data-stu-id="df4a2-163">Requirement</span></span> | <span data-ttu-id="df4a2-164">Wert</span><span class="sxs-lookup"><span data-stu-id="df4a2-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="df4a2-165">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="df4a2-165">Minimum supported client</span></span><br/> | <span data-ttu-id="df4a2-166">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="df4a2-166">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="df4a2-167">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="df4a2-167">Minimum supported server</span></span><br/> | <span data-ttu-id="df4a2-168">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="df4a2-168">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="df4a2-169">Namespace</span><span class="sxs-lookup"><span data-stu-id="df4a2-169">Namespace</span></span><br/>                | <span data-ttu-id="df4a2-170">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="df4a2-170">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="df4a2-171">MOF</span><span class="sxs-lookup"><span data-stu-id="df4a2-171">MOF</span></span><br/>                      | <dl> <span data-ttu-id="df4a2-172"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="df4a2-172"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="df4a2-173">DLL</span><span class="sxs-lookup"><span data-stu-id="df4a2-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df4a2-174"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df4a2-174"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df4a2-175">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="df4a2-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df4a2-176">**Win32- \_ Freigabe**</span><span class="sxs-lookup"><span data-stu-id="df4a2-176">**Win32\_Share**</span></span>](win32-share.md)
</dt> </dl>

 

