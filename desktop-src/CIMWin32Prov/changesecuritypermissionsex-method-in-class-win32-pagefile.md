---
description: Ändert die Sicherheits Berechtigungen für die logische Auslagerungs Datei, die im Objekt Pfad angegeben ist (diese Methode ist eine erweiterte Version der changesecurrityberechtigungs-Methode).
ms.assetid: a852a7e6-f26a-4bd9-bb15-e4cdd577697c
ms.tgt_platform: multiple
title: Changesecurritypermissionsex-Methode der Win32_PageFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a01a214e626f9c64ccf460eb3f8c031d1b45ff85
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861036"
---
# <a name="changesecuritypermissionsex-method-of-the-win32_pagefile-class"></a><span data-ttu-id="0489d-103">Changesecurritypermissionsex-Methode der Win32- \_ Pagefile-Klasse</span><span class="sxs-lookup"><span data-stu-id="0489d-103">ChangeSecurityPermissionsEx method of the Win32\_PageFile class</span></span>

<span data-ttu-id="0489d-104">Die [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode **changesecurritypermissionsex** ändert die Sicherheits Berechtigungen für die logische Auslagerungs Datei, die im Objekt Pfad angegeben ist (diese Methode ist eine erweiterte Version der [**changesecurrityberechtigungs**](changesecuritypermissions-method-in-class-win32-directory.md) -Methode).</span><span class="sxs-lookup"><span data-stu-id="0489d-104">The **ChangeSecurityPermissionsEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method changes the security permissions for the logical paging file that is specified in the object path (this method is an extended version of the [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-win32-directory.md) method).</span></span> <span data-ttu-id="0489d-105">Wenn die logische Datei ein Verzeichnis ist, ist diese Methode rekursiv und ändert die Sicherheits Berechtigungen aller Dateien und Unterverzeichnisse, die im Verzeichnis enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="0489d-105">If the logical file is a directory, then this method is recursive, and changes the security permissions of all of the files and subdirectories that the directory contains.</span></span>

<span data-ttu-id="0489d-106">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="0489d-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="0489d-107">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="0489d-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="0489d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0489d-108">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissionsEx(
  [in]           Win32_SecurityDescriptor SecurityDescriptor,
  [in]           uint32                   Option,
  [out]          string                   StopFileName,
  [in, optional] string                   StartFileName,
  [in, optional] boolean                  Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="0489d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0489d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0489d-110">*SecurityDescriptor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0489d-110">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0489d-111">Ein Ausdruck, der zu einer Instanz von [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="0489d-111">Expression that resolves to an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span> <span data-ttu-id="0489d-112">Dieser Parameter enthält neue Sicherheits Berechtigungen für die Instanz von [**Win32 \_ Page File**](win32-pagefile.md).</span><span class="sxs-lookup"><span data-stu-id="0489d-112">This parameter contains new security permissions for the instance of [**Win32\_PageFile**](win32-pagefile.md).</span></span>

</dd> <dt>

<span data-ttu-id="0489d-113">*Option* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0489d-113">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0489d-114">Sicherheits Berechtigung, die geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="0489d-114">Security privilege to be modified.</span></span> <span data-ttu-id="0489d-115">Wenn Sie z. b. den Besitzer und die DACL-Sicherheit (-Zugriffs Steuerungs Liste) ändern möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="0489d-115">For example, to change the owner and discretionary access control list (DACL) security, use the following:</span></span>

`Option = 1 + 4`

<span data-ttu-id="0489d-116">Oder</span><span class="sxs-lookup"><span data-stu-id="0489d-116">-or-</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="0489d-117"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Ändern \_ \_Sicherheits \_ Informationen** für den Besitzer (1)</span><span class="sxs-lookup"><span data-stu-id="0489d-117"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="0489d-118">Ändern Sie den Besitzer der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="0489d-118">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="0489d-119"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Ändern \_ Gruppen \_ Sicherheits \_ Informationen** (2)</span><span class="sxs-lookup"><span data-stu-id="0489d-119"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="0489d-120">Ändern Sie die Gruppe der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="0489d-120">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="0489d-121"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Ändern \_ DACL- \_ Sicherheits \_ Informationen** (4)</span><span class="sxs-lookup"><span data-stu-id="0489d-121"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="0489d-122">Ändern Sie die DACL der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="0489d-122">Change the DACL of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="0489d-123"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Ändern \_ SACL- \_ Sicherheits \_ Informationen** (8)</span><span class="sxs-lookup"><span data-stu-id="0489d-123"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="0489d-124">Ändern Sie die Liste der System Zugriffs Teuerung (SACL) der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="0489d-124">Change the system access control (SACL) list of the logical file.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="0489d-125">*Stop filename* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0489d-125">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0489d-126">Der Name der Datei oder des Verzeichnisses, in der die **changesecurritypermissionsex** -Methode fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="0489d-126">Name of the file or directory where the **ChangeSecurityPermissionsEx** method failed.</span></span> <span data-ttu-id="0489d-127">Dieser Parameter ist **null** , wenn die Methode erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="0489d-127">This parameter is **NULL** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="0489d-128">*Startdateiname* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="0489d-128">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0489d-129">Benennt die untergeordnete Datei oder das Verzeichnis, die als Ausgangspunkt für **changesecurritypermissionsex** verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0489d-129">Names the child file or directory to use as a starting point for **ChangeSecurityPermissionsEx**.</span></span> <span data-ttu-id="0489d-130">In der Regel ist der *StartFileName* -Parameter der *StartFileName* -Parameter, der die Datei oder das Verzeichnis angibt, in dem ein Fehler aus dem vorherigen Methoden aufzurufen aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="0489d-130">Typically, the *StartFileName* parameter is the *StartFileName* parameter that specifies the file or directory where an error occurred from the previous method call.</span></span> <span data-ttu-id="0489d-131">Wenn dieser Parameter **null** ist, wird der Vorgang für die im [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) -Befehl angegebene Datei oder das Verzeichnis ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0489d-131">If this parameter is **null**, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="0489d-132">*Rekursiv* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="0489d-132">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0489d-133">**True** gibt an, dass die Eigentums Änderung rekursiv auf Dateien und Verzeichnisse in dem Verzeichnis angewendet wird, das von der [**CIM \_ LogicalFile**](cim-logicalfile.md) -Instanz angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0489d-133">If **true**, the change of ownership is applied recursively to files and directories in the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span>

> [!Note]  
> <span data-ttu-id="0489d-134">Bei Datei Instanzen wird der *rekursive* Parameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="0489d-134">For file instances, the *Recursive* parameter is ignored.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0489d-135">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0489d-135">Return value</span></span>

<span data-ttu-id="0489d-136">Gibt den Wert 0 (null) zurück, wenn die Berechtigungen geändert werden, und eine andere Zahl, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="0489d-136">Returns a value of 0 (zero) if the permissions are changed, and a different number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="0489d-137">**Erfolgreich**</span><span class="sxs-lookup"><span data-stu-id="0489d-137">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="0489d-138">0</span><span class="sxs-lookup"><span data-stu-id="0489d-138">0</span></span>

<span data-ttu-id="0489d-139">Die Anforderung ist erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="0489d-139">The request is successful.</span></span>

</dd> <dt>

<span data-ttu-id="0489d-140">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="0489d-140">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="0489d-141">2</span><span class="sxs-lookup"><span data-stu-id="0489d-141">2</span></span>

<span data-ttu-id="0489d-142">Zugriff verweigert.“</span><span class="sxs-lookup"><span data-stu-id="0489d-142">Access is denied.</span></span>

</dd> <dt>

<span data-ttu-id="0489d-143">**Nicht spezifizierter Fehler**</span><span class="sxs-lookup"><span data-stu-id="0489d-143">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="0489d-144">8</span><span class="sxs-lookup"><span data-stu-id="0489d-144">8</span></span>

<span data-ttu-id="0489d-145">Ein nicht angegebener Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="0489d-145">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="0489d-146">**Ungültiges Objekt**</span><span class="sxs-lookup"><span data-stu-id="0489d-146">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="0489d-147">9</span><span class="sxs-lookup"><span data-stu-id="0489d-147">9</span></span>

<span data-ttu-id="0489d-148">Der angegebene Name ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="0489d-148">The name specified is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="0489d-149">**Objekt ist bereits vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="0489d-149">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="0489d-150">10</span><span class="sxs-lookup"><span data-stu-id="0489d-150">10</span></span>

<span data-ttu-id="0489d-151">Das Objekt "" ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="0489d-151">The specified object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="0489d-152">**Dateisystem nicht NTFS**</span><span class="sxs-lookup"><span data-stu-id="0489d-152">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="0489d-153">11</span><span class="sxs-lookup"><span data-stu-id="0489d-153">11</span></span>

<span data-ttu-id="0489d-154">Das Dateisystem ist kein NTFS-Dateisystem.</span><span class="sxs-lookup"><span data-stu-id="0489d-154">The file system is not an NTFS file system.</span></span>

</dd> <dt>

<span data-ttu-id="0489d-155">**Plattform nicht NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="0489d-155">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="0489d-156">12</span><span class="sxs-lookup"><span data-stu-id="0489d-156">12</span></span>

<span data-ttu-id="0489d-157">Die Plattform ist nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="0489d-157">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="0489d-158">**Laufwerk nicht identisch**</span><span class="sxs-lookup"><span data-stu-id="0489d-158">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="0489d-159">13</span><span class="sxs-lookup"><span data-stu-id="0489d-159">13</span></span>

<span data-ttu-id="0489d-160">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="0489d-160">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="0489d-161">**Verzeichnis nicht leer**</span><span class="sxs-lookup"><span data-stu-id="0489d-161">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="0489d-162">14</span><span class="sxs-lookup"><span data-stu-id="0489d-162">14</span></span>

<span data-ttu-id="0489d-163">Das Verzeichnis ist nicht leer.</span><span class="sxs-lookup"><span data-stu-id="0489d-163">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="0489d-164">**Freigabe Verletzung**</span><span class="sxs-lookup"><span data-stu-id="0489d-164">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="0489d-165">15</span><span class="sxs-lookup"><span data-stu-id="0489d-165">15</span></span>

<span data-ttu-id="0489d-166">Eine Freigabe Verletzung ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="0489d-166">There is a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="0489d-167">**Ungültige Startdatei**</span><span class="sxs-lookup"><span data-stu-id="0489d-167">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="0489d-168">16</span><span class="sxs-lookup"><span data-stu-id="0489d-168">16</span></span>

<span data-ttu-id="0489d-169">Die angegebene Startdatei ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="0489d-169">The specified start file is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="0489d-170">**Berechtigung nicht aufrechterhalten**</span><span class="sxs-lookup"><span data-stu-id="0489d-170">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="0489d-171">17</span><span class="sxs-lookup"><span data-stu-id="0489d-171">17</span></span>

<span data-ttu-id="0489d-172">Eine für den Vorgang erforderliche Berechtigung fehlt.</span><span class="sxs-lookup"><span data-stu-id="0489d-172">A privilege required for the operation is missing.</span></span>

</dd> <dt>

<span data-ttu-id="0489d-173">**Ungültiger Parameter**</span><span class="sxs-lookup"><span data-stu-id="0489d-173">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="0489d-174">21</span><span class="sxs-lookup"><span data-stu-id="0489d-174">21</span></span>

<span data-ttu-id="0489d-175">Ein angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="0489d-175">A specified parameter is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0489d-176">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0489d-176">Requirements</span></span>



| <span data-ttu-id="0489d-177">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0489d-177">Requirement</span></span> | <span data-ttu-id="0489d-178">Wert</span><span class="sxs-lookup"><span data-stu-id="0489d-178">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0489d-179">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0489d-179">Minimum supported client</span></span><br/> | <span data-ttu-id="0489d-180">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0489d-180">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0489d-181">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0489d-181">Minimum supported server</span></span><br/> | <span data-ttu-id="0489d-182">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0489d-182">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0489d-183">Namespace</span><span class="sxs-lookup"><span data-stu-id="0489d-183">Namespace</span></span><br/>                | <span data-ttu-id="0489d-184">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0489d-184">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0489d-185">MOF</span><span class="sxs-lookup"><span data-stu-id="0489d-185">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0489d-186"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0489d-186"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0489d-187">DLL</span><span class="sxs-lookup"><span data-stu-id="0489d-187">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0489d-188"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0489d-188"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0489d-189">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0489d-189">See also</span></span>

<dl> <dt>

<span data-ttu-id="0489d-190">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0489d-190">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="0489d-191">**Win32- \_ Pagefile**</span><span class="sxs-lookup"><span data-stu-id="0489d-191">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

