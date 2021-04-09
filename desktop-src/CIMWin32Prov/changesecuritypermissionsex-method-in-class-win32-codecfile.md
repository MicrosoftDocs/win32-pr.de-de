---
description: Ändert die Sicherheits Berechtigungen für die im Objekt Pfad angegebene Codec-Datei (diese Methode ist eine erweiterte Version der changesecurrityberechtigungs-Methode).
ms.assetid: 3eac4ae1-3c0e-4e81-8b23-9ad8698f723c
ms.tgt_platform: multiple
title: Changesecurritypermissionsex-Methode der Win32_CodecFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 549c55a5066bdaba4699ec76ed3b7be23eb28b96
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861039"
---
# <a name="changesecuritypermissionsex-method-of-the-win32_codecfile-class"></a><span data-ttu-id="3ccf8-103">Changesecurritypermissionsex-Methode der Win32- \_ codecfile-Klasse</span><span class="sxs-lookup"><span data-stu-id="3ccf8-103">ChangeSecurityPermissionsEx method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="3ccf8-104">Die **changesecurritypermissionsex** - [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode ändert die Sicherheits Berechtigungen für die im Objekt Pfad angegebene Codec-Datei (diese Methode ist eine erweiterte Version der [**changesecurrityberechtigungs**](changesecuritypermissions-method-in-class-win32-directory.md) -Methode).</span><span class="sxs-lookup"><span data-stu-id="3ccf8-104">The **ChangeSecurityPermissionsEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method changes the security permissions for the codec file specified in the object path (this method is an extended version of the [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-win32-directory.md) method).</span></span> <span data-ttu-id="3ccf8-105">Wenn die logische Datei ein Verzeichnis ist, ist diese Methode rekursiv und ändert die Sicherheits Berechtigungen aller Dateien und Unterverzeichnisse, die im Verzeichnis enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="3ccf8-105">If the logical file is a directory, then this method is recursive, and changes the security permissions of all the files and subdirectories that the directory contains.</span></span>

<span data-ttu-id="3ccf8-106">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="3ccf8-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="3ccf8-107">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="3ccf8-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="3ccf8-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3ccf8-108">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissionsEx(
  [in]           Win32_SecurityDescriptor SecurityDescriptor,
  [in]           uint32                   Option,
  [out]          string                   StopFileName,
  [in, optional] string                   StartFileName,
  [in, optional] boolean                  Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="3ccf8-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="3ccf8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ccf8-110">*SecurityDescriptor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3ccf8-110">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ccf8-111">Ein Ausdruck, der zu einer Instanz von [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="3ccf8-111">Expression that resolves to an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span> <span data-ttu-id="3ccf8-112">Dieser Deskriptor enthält neue Sicherheits Berechtigungen für die Instanz von [**Win32 \_ codecfile**](win32-codecfile.md).</span><span class="sxs-lookup"><span data-stu-id="3ccf8-112">This descriptor contains new security permissions for the instance of [**Win32\_CodecFile**](win32-codecfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3ccf8-113">*Option* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3ccf8-113">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ccf8-114">Die tatsächliche Sicherheits Berechtigung, die geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="3ccf8-114">Actual security privilege to be modified.</span></span> <span data-ttu-id="3ccf8-115">Wenn Sie z. b. den Besitzer und die DACL-Sicherheit (-Zugriffs Steuerungs Liste) ändern möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="3ccf8-115">For example, to change the owner and discretionary access control list (DACL) security, use the following:</span></span>

`Option = 1 + 4`

<span data-ttu-id="3ccf8-116">Oder</span><span class="sxs-lookup"><span data-stu-id="3ccf8-116">-or-</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="3ccf8-117"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Ändern \_ \_Sicherheits \_ Informationen** für den Besitzer (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="3ccf8-117"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="3ccf8-118">Ändern Sie den Besitzer der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="3ccf8-118">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="3ccf8-119"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Ändern \_ Gruppen \_ Sicherheits \_ Informationen** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="3ccf8-119"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="3ccf8-120">Ändern Sie die Gruppe der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="3ccf8-120">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="3ccf8-121"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Ändern \_ DACL- \_ Sicherheits \_ Informationen** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="3ccf8-121"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="3ccf8-122">Ändern Sie die freigegebene Zugriffs Steuerungs Liste (DACL) der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="3ccf8-122">Change the discretionary access control list (DACL) of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="3ccf8-123"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Ändern \_ SACL- \_ Sicherheits \_ Informationen** (8 (0x8))</span><span class="sxs-lookup"><span data-stu-id="3ccf8-123"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="3ccf8-124">Ändern Sie die System Zugriffs Steuerungs Liste (SACL) der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="3ccf8-124">Change the system access control list (SACL) of the logical file.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="3ccf8-125">*Stop filename* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3ccf8-125">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ccf8-126">Der Name der Datei oder des Verzeichnisses, in der die **changesecurritypermissionsex** -Methode fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="3ccf8-126">Name of the file or directory where the **ChangeSecurityPermissionsEx** method failed.</span></span> <span data-ttu-id="3ccf8-127">Dieser Parameter ist NULL, wenn die Methode erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3ccf8-127">This parameter is null when the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="3ccf8-128">*Startdateiname* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="3ccf8-128">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3ccf8-129">Benennt die untergeordnete Datei oder das Verzeichnis, die als Ausgangspunkt für **changesecurritypermissionsex** verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3ccf8-129">Names the child file or directory to use as a starting point for **ChangeSecurityPermissionsEx**.</span></span> <span data-ttu-id="3ccf8-130">In der Regel ist der Parameter " *StartFileName* " der Parameter " *StopFileName* ", der die Datei oder das Verzeichnis angibt, in dem ein Fehler beim vorherigen Methoden aufzurufen aufgetreten ist</span><span class="sxs-lookup"><span data-stu-id="3ccf8-130">Typically, the *StartFileName* parameter is the *StopFileName* parameter that specifies the file or directory where an error occurred from the previous method call.</span></span> <span data-ttu-id="3ccf8-131">Wenn dieser Parameter NULL ist, wird der Vorgang für die im [**ExecMethod**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethod) -Befehl angegebene Datei oder das Verzeichnis ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3ccf8-131">If this parameter is null, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="3ccf8-132">*Rekursiv* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="3ccf8-132">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3ccf8-133">**True** gibt an, dass die Eigentumsänderungen rekursiv auf Dateien und Verzeichnisse in dem Verzeichnis angewendet werden, das von der [**CIM \_ LogicalFile**](cim-logicalfile.md) -Instanz angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3ccf8-133">If **true**, the changes of ownership are applied recursively to files and directories in the directory that the [**CIM\_LogicalFile**](cim-logicalfile.md) instance specifies.</span></span> <span data-ttu-id="3ccf8-134">Bei Datei Instanzen wird der *rekursive* Eingabeparameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="3ccf8-134">For file instances, the *Recursive* input parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ccf8-135">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3ccf8-135">Return value</span></span>

<span data-ttu-id="3ccf8-136">Gibt einen Wert von 0 (null) zurück, wenn die Berechtigungen geändert werden, und eine andere Zahl, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="3ccf8-136">Returns an value of 0 (zero) if the permissions are changed, and a different number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="3ccf8-137">**Erfolgreich**</span><span class="sxs-lookup"><span data-stu-id="3ccf8-137">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="3ccf8-138">0</span><span class="sxs-lookup"><span data-stu-id="3ccf8-138">0</span></span>

<span data-ttu-id="3ccf8-139">Die Anforderung ist erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="3ccf8-139">The request is successful.</span></span>

</dd> <dt>

<span data-ttu-id="3ccf8-140">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="3ccf8-140">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="3ccf8-141">2</span><span class="sxs-lookup"><span data-stu-id="3ccf8-141">2</span></span>

<span data-ttu-id="3ccf8-142">Zugriff verweigert.“</span><span class="sxs-lookup"><span data-stu-id="3ccf8-142">Access is denied.</span></span>

</dd> <dt>

<span data-ttu-id="3ccf8-143">**Nicht spezifizierter Fehler**</span><span class="sxs-lookup"><span data-stu-id="3ccf8-143">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="3ccf8-144">8</span><span class="sxs-lookup"><span data-stu-id="3ccf8-144">8</span></span>

<span data-ttu-id="3ccf8-145">Ein nicht angegebener Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="3ccf8-145">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="3ccf8-146">**Ungültiges Objekt**</span><span class="sxs-lookup"><span data-stu-id="3ccf8-146">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="3ccf8-147">9</span><span class="sxs-lookup"><span data-stu-id="3ccf8-147">9</span></span>

<span data-ttu-id="3ccf8-148">Der angegebene Name ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="3ccf8-148">The specified name is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="3ccf8-149">**Objekt ist bereits vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="3ccf8-149">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="3ccf8-150">10</span><span class="sxs-lookup"><span data-stu-id="3ccf8-150">10</span></span>

<span data-ttu-id="3ccf8-151">Das Objekt "" ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="3ccf8-151">The specified object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="3ccf8-152">**Dateisystem nicht NTFS**</span><span class="sxs-lookup"><span data-stu-id="3ccf8-152">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="3ccf8-153">11</span><span class="sxs-lookup"><span data-stu-id="3ccf8-153">11</span></span>

<span data-ttu-id="3ccf8-154">Das Dateisystem ist kein NTFS-Dateisystem.</span><span class="sxs-lookup"><span data-stu-id="3ccf8-154">The file system is not an NTFS file system.</span></span>

</dd> <dt>

<span data-ttu-id="3ccf8-155">**Plattform nicht NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="3ccf8-155">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="3ccf8-156">12</span><span class="sxs-lookup"><span data-stu-id="3ccf8-156">12</span></span>

<span data-ttu-id="3ccf8-157">Die Plattform ist nicht Windows NT oder Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="3ccf8-157">The platform is not Windows NT or Windows 2000.</span></span>

</dd> <dt>

<span data-ttu-id="3ccf8-158">**Laufwerk nicht identisch**</span><span class="sxs-lookup"><span data-stu-id="3ccf8-158">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="3ccf8-159">13</span><span class="sxs-lookup"><span data-stu-id="3ccf8-159">13</span></span>

<span data-ttu-id="3ccf8-160">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="3ccf8-160">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="3ccf8-161">**Verzeichnis nicht leer**</span><span class="sxs-lookup"><span data-stu-id="3ccf8-161">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="3ccf8-162">14</span><span class="sxs-lookup"><span data-stu-id="3ccf8-162">14</span></span>

<span data-ttu-id="3ccf8-163">Das Verzeichnis ist nicht leer.</span><span class="sxs-lookup"><span data-stu-id="3ccf8-163">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="3ccf8-164">**Freigabe Verletzung**</span><span class="sxs-lookup"><span data-stu-id="3ccf8-164">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="3ccf8-165">15</span><span class="sxs-lookup"><span data-stu-id="3ccf8-165">15</span></span>

<span data-ttu-id="3ccf8-166">Eine Freigabe Verletzung ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="3ccf8-166">There is a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="3ccf8-167">**Ungültige Startdatei**</span><span class="sxs-lookup"><span data-stu-id="3ccf8-167">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="3ccf8-168">16</span><span class="sxs-lookup"><span data-stu-id="3ccf8-168">16</span></span>

<span data-ttu-id="3ccf8-169">Die angegebene Startdatei ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="3ccf8-169">The specified start file is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="3ccf8-170">**Berechtigung nicht aufrechterhalten**</span><span class="sxs-lookup"><span data-stu-id="3ccf8-170">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="3ccf8-171">17</span><span class="sxs-lookup"><span data-stu-id="3ccf8-171">17</span></span>

<span data-ttu-id="3ccf8-172">Eine für den Vorgang erforderliche Berechtigung wird nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="3ccf8-172">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="3ccf8-173">**Ungültiger Parameter**</span><span class="sxs-lookup"><span data-stu-id="3ccf8-173">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="3ccf8-174">21</span><span class="sxs-lookup"><span data-stu-id="3ccf8-174">21</span></span>

<span data-ttu-id="3ccf8-175">Ein angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="3ccf8-175">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3ccf8-176">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3ccf8-176">Requirements</span></span>



| <span data-ttu-id="3ccf8-177">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3ccf8-177">Requirement</span></span> | <span data-ttu-id="3ccf8-178">Wert</span><span class="sxs-lookup"><span data-stu-id="3ccf8-178">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ccf8-179">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3ccf8-179">Minimum supported client</span></span><br/> | <span data-ttu-id="3ccf8-180">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3ccf8-180">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3ccf8-181">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3ccf8-181">Minimum supported server</span></span><br/> | <span data-ttu-id="3ccf8-182">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3ccf8-182">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3ccf8-183">Namespace</span><span class="sxs-lookup"><span data-stu-id="3ccf8-183">Namespace</span></span><br/>                | <span data-ttu-id="3ccf8-184">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="3ccf8-184">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3ccf8-185">MOF</span><span class="sxs-lookup"><span data-stu-id="3ccf8-185">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3ccf8-186"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3ccf8-186"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3ccf8-187">DLL</span><span class="sxs-lookup"><span data-stu-id="3ccf8-187">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ccf8-188"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ccf8-188"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ccf8-189">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3ccf8-189">See also</span></span>

<dl> <dt>

<span data-ttu-id="3ccf8-190">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3ccf8-190">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="3ccf8-191">**Win32- \_ codecfile**</span><span class="sxs-lookup"><span data-stu-id="3ccf8-191">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

