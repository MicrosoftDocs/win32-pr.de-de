---
description: 'GetAccessMask-Methode der Win32_Share-Klasse: Gibt eine uint32-Bitmap mit den Zugriffsrechten für die Freigabe zurück, die vom Benutzer oder der Gruppe gehalten wird, in dessen Auftrag die Instanz zurückgegeben wird.'
ms.assetid: 234f44a4-ffff-431d-a973-98f2bd313c7d
ms.tgt_platform: multiple
title: GetAccessMask-Methode der Win32_Share-Klasse
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
ms.openlocfilehash: fcd6396f6421060a67108e7c428c99bcd7ca9651
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097018"
---
# <a name="getaccessmask-method-of-the-win32_share-class"></a><span data-ttu-id="305d8-103">GetAccessMask-Methode der Win32 \_ Share-Klasse</span><span class="sxs-lookup"><span data-stu-id="305d8-103">GetAccessMask method of the Win32\_Share class</span></span>

<span data-ttu-id="305d8-104">Die **GetAccessMask-Methode** gibt eine uint32-Bitmap mit den Zugriffsrechten für die Freigabe zurück, die vom Benutzer oder der Gruppe gehalten wird, in dessen Auftrag die Instanz zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="305d8-104">The **GetAccessMask** method returns a uint32 bitmap with the access rights to the share held by the user or group on whose behalf the instance is returned.</span></span>

<span data-ttu-id="305d8-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="305d8-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="305d8-106">Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)</span><span class="sxs-lookup"><span data-stu-id="305d8-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="305d8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="305d8-107">Syntax</span></span>


```mof
uint32 GetAccessMask();
```



## <a name="parameters"></a><span data-ttu-id="305d8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="305d8-108">Parameters</span></span>

<span data-ttu-id="305d8-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="305d8-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="305d8-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="305d8-110">Return value</span></span>

<span data-ttu-id="305d8-111">Zugriffsrechte für die Freigabe des Benutzers oder der Gruppe.</span><span class="sxs-lookup"><span data-stu-id="305d8-111">Access rights to the share held by the user or group.</span></span>

<dl> <dt>

<span data-ttu-id="305d8-112">**\_ \_ DATEILISTENVERZEICHNIS**</span><span class="sxs-lookup"><span data-stu-id="305d8-112">**FILE\_LIST\_DIRECTORY**</span></span>
</dt> <dd>

<span data-ttu-id="305d8-113">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="305d8-113">1 (0x1)</span></span>

<span data-ttu-id="305d8-114">Gewährt das Recht, Daten aus der Datei zu lesen.</span><span class="sxs-lookup"><span data-stu-id="305d8-114">Grants the right to read data from the file.</span></span> <span data-ttu-id="305d8-115">Für ein Verzeichnis gewährt dieser Wert das Recht, den Inhalt des Verzeichnisses aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="305d8-115">For a directory, this value grants the right to list the contents of the directory.</span></span>

</dd> <dt>

<span data-ttu-id="305d8-116">**FILE \_ ADD \_ FILE**</span><span class="sxs-lookup"><span data-stu-id="305d8-116">**FILE\_ADD\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="305d8-117">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="305d8-117">2 (0x2)</span></span>

<span data-ttu-id="305d8-118">Gewährt das Recht, Daten in die Datei zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="305d8-118">Grants the right to write data to the file.</span></span> <span data-ttu-id="305d8-119">Für ein Verzeichnis gewährt dieser Wert das Recht, eine Datei im Verzeichnis zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="305d8-119">For a directory, this value grants the right to create a file in the directory.</span></span>

</dd> <dt>

<span data-ttu-id="305d8-120">**\_FILE \_ ADD-UNTERVERZEICHNIS**</span><span class="sxs-lookup"><span data-stu-id="305d8-120">**FILE\_ADD\_SUBDIRECTORY**</span></span>
</dt> <dd>

<span data-ttu-id="305d8-121">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="305d8-121">4 (0x4)</span></span>

<span data-ttu-id="305d8-122">Gewährt das Recht, Daten an die Datei anzufügen.</span><span class="sxs-lookup"><span data-stu-id="305d8-122">Grants the right to append data to the file.</span></span> <span data-ttu-id="305d8-123">Für ein Verzeichnis gewährt dieser Wert das Recht, ein Unterverzeichnis zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="305d8-123">For a directory, this value grants the right to create a subdirectory.</span></span>

</dd> <dt>

<span data-ttu-id="305d8-124">**FILE \_ READ \_ EA**</span><span class="sxs-lookup"><span data-stu-id="305d8-124">**FILE\_READ\_EA**</span></span>
</dt> <dd>

<span data-ttu-id="305d8-125">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="305d8-125">8 (0x8)</span></span>

<span data-ttu-id="305d8-126">Gewährt das Recht, erweiterte Attribute zu lesen.</span><span class="sxs-lookup"><span data-stu-id="305d8-126">Grants the right to read extended attributes.</span></span>

</dd> <dt>

<span data-ttu-id="305d8-127">**\_DATEI-SCHREIB-EA \_**</span><span class="sxs-lookup"><span data-stu-id="305d8-127">**FILE\_WRITE\_EA**</span></span>
</dt> <dd>

<span data-ttu-id="305d8-128">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="305d8-128">16 (0x10)</span></span>

<span data-ttu-id="305d8-129">Gewährt das Recht, erweiterte Attribute zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="305d8-129">Grants the right to write extended attributes.</span></span>

</dd> <dt>

<span data-ttu-id="305d8-130">**FILE \_ TRAVERSE**</span><span class="sxs-lookup"><span data-stu-id="305d8-130">**FILE\_TRAVERSE**</span></span>
</dt> <dd>

<span data-ttu-id="305d8-131">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="305d8-131">32 (0x20)</span></span>

<span data-ttu-id="305d8-132">Gewährt das Recht, eine Datei auszuführen.</span><span class="sxs-lookup"><span data-stu-id="305d8-132">Grants the right to execute a file.</span></span> <span data-ttu-id="305d8-133">Für ein Verzeichnis kann das Verzeichnis durchlaufen werden.</span><span class="sxs-lookup"><span data-stu-id="305d8-133">For a directory, the directory can be traversed.</span></span>

</dd> <dt>

<span data-ttu-id="305d8-134">**FILE \_ DELETE \_ CHILD**</span><span class="sxs-lookup"><span data-stu-id="305d8-134">**FILE\_DELETE\_CHILD**</span></span>
</dt> <dd>

<span data-ttu-id="305d8-135">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="305d8-135">64 (0x40)</span></span>

<span data-ttu-id="305d8-136">Gewährt das Recht, ein Verzeichnis und alle dateien zu löschen, die es enthält (seine unteren Elemente), auch wenn die Dateien schreibgeschützt sind.</span><span class="sxs-lookup"><span data-stu-id="305d8-136">Grants the right to delete a directory and all of the files it contains (its children), even if the files are read-only.</span></span>

</dd> <dt>

<span data-ttu-id="305d8-137">**\_ \_ DATEILESEATTRIBUTE**</span><span class="sxs-lookup"><span data-stu-id="305d8-137">**FILE\_READ\_ATTRIBUTES**</span></span>
</dt> <dd>

<span data-ttu-id="305d8-138">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="305d8-138">128 (0x80)</span></span>

<span data-ttu-id="305d8-139">Gewährt das Recht, Dateiattribute zu lesen.</span><span class="sxs-lookup"><span data-stu-id="305d8-139">Grants the right to read file attributes.</span></span>

</dd> <dt>

<span data-ttu-id="305d8-140">**\_ \_ DATEI-SCHREIBATTRIBUTE**</span><span class="sxs-lookup"><span data-stu-id="305d8-140">**FILE\_WRITE\_ATTRIBUTES**</span></span>
</dt> <dd>

<span data-ttu-id="305d8-141">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="305d8-141">256 (0x100)</span></span>

<span data-ttu-id="305d8-142">Gewährt das Recht, Dateiattribute zu ändern.</span><span class="sxs-lookup"><span data-stu-id="305d8-142">Grants the right to change file attributes.</span></span>

</dd> <dt>

<span data-ttu-id="305d8-143">**DELETE**</span><span class="sxs-lookup"><span data-stu-id="305d8-143">**DELETE**</span></span>
</dt> <dd>

<span data-ttu-id="305d8-144">65536 (0x10000)</span><span class="sxs-lookup"><span data-stu-id="305d8-144">65536 (0x10000)</span></span>

<span data-ttu-id="305d8-145">Gewährt Löschzugriff.</span><span class="sxs-lookup"><span data-stu-id="305d8-145">Grants delete access.</span></span>

</dd> <dt>

<span data-ttu-id="305d8-146">**\_READ-STEUERELEMENT**</span><span class="sxs-lookup"><span data-stu-id="305d8-146">**READ\_CONTROL**</span></span>
</dt> <dd>

<span data-ttu-id="305d8-147">131072 (0x20000)</span><span class="sxs-lookup"><span data-stu-id="305d8-147">131072 (0x20000)</span></span>

<span data-ttu-id="305d8-148">Gewährt Lesezugriff auf den Sicherheitsdeskriptor und den Besitzer.</span><span class="sxs-lookup"><span data-stu-id="305d8-148">Grants read access to the security descriptor and owner.</span></span>

</dd> <dt>

<span data-ttu-id="305d8-149">**WRITE \_ DAC**</span><span class="sxs-lookup"><span data-stu-id="305d8-149">**WRITE\_DAC**</span></span>
</dt> <dd>

<span data-ttu-id="305d8-150">262144 (0x40000)</span><span class="sxs-lookup"><span data-stu-id="305d8-150">262144 (0x40000)</span></span>

<span data-ttu-id="305d8-151">Gewährt Schreibzugriff auf die DACL (Discretionary Access Control List).</span><span class="sxs-lookup"><span data-stu-id="305d8-151">Grants write access to the discretionary access control list (DACL).</span></span>

</dd> <dt>

<span data-ttu-id="305d8-152">**WRITE \_ OWNER**</span><span class="sxs-lookup"><span data-stu-id="305d8-152">**WRITE\_OWNER**</span></span>
</dt> <dd>

<span data-ttu-id="305d8-153">524288 (0x80000)</span><span class="sxs-lookup"><span data-stu-id="305d8-153">524288 (0x80000)</span></span>

<span data-ttu-id="305d8-154">Weist den Schreibbesitzer zu.</span><span class="sxs-lookup"><span data-stu-id="305d8-154">Assigns the write owner.</span></span>

</dd> <dt>

<span data-ttu-id="305d8-155">**SYNCHRONIZE**</span><span class="sxs-lookup"><span data-stu-id="305d8-155">**SYNCHRONIZE**</span></span>
</dt> <dd>

<span data-ttu-id="305d8-156">1048576 (0x100000)</span><span class="sxs-lookup"><span data-stu-id="305d8-156">1048576 (0x100000)</span></span>

<span data-ttu-id="305d8-157">Synchronisiert den Zugriff und ermöglicht es einem Prozess, auf den Eintritt eines Objekts in den signalisierten Zustand zu warten.</span><span class="sxs-lookup"><span data-stu-id="305d8-157">Synchronizes access and allows a process to wait for an object to enter the signaled state.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="305d8-158">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="305d8-158">Remarks</span></span>

<span data-ttu-id="305d8-159">**Die GetAccessMask-Methode** ist eine Objektmethode und wird bei einem Vorkommen dieser Klasse verwendet.</span><span class="sxs-lookup"><span data-stu-id="305d8-159">**GetAccessMask** method is an object method and is used on an occurrence of this class.</span></span>

## <a name="examples"></a><span data-ttu-id="305d8-160">Beispiele</span><span class="sxs-lookup"><span data-stu-id="305d8-160">Examples</span></span>

<span data-ttu-id="305d8-161">Das folgende VBScript-Codebeispiel erstellt einen Freigabeordner und ruft dann den Wert der Zugriffsmaske in der Sicherheitsbeschreibung ab, die den Freigabeordner sichert.</span><span class="sxs-lookup"><span data-stu-id="305d8-161">The following VBScript code example creates a share folder and then gets the value of the access mask in the security descriptor that secures the share folder.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="305d8-162">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="305d8-162">Requirements</span></span>



| <span data-ttu-id="305d8-163">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="305d8-163">Requirement</span></span> | <span data-ttu-id="305d8-164">Wert</span><span class="sxs-lookup"><span data-stu-id="305d8-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="305d8-165">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="305d8-165">Minimum supported client</span></span><br/> | <span data-ttu-id="305d8-166">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="305d8-166">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="305d8-167">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="305d8-167">Minimum supported server</span></span><br/> | <span data-ttu-id="305d8-168">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="305d8-168">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="305d8-169">Namespace</span><span class="sxs-lookup"><span data-stu-id="305d8-169">Namespace</span></span><br/>                | <span data-ttu-id="305d8-170">Stamm \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="305d8-170">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="305d8-171">MOF</span><span class="sxs-lookup"><span data-stu-id="305d8-171">MOF</span></span><br/>                      | <dl> <span data-ttu-id="305d8-172"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="305d8-172"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="305d8-173">DLL</span><span class="sxs-lookup"><span data-stu-id="305d8-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="305d8-174"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="305d8-174"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="305d8-175">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="305d8-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="305d8-176">**\_Win32-Freigabe**</span><span class="sxs-lookup"><span data-stu-id="305d8-176">**Win32\_Share**</span></span>](win32-share.md)
</dt> </dl>

 

