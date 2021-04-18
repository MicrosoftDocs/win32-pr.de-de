---
description: Ändert die Sicherheits Berechtigungen für die im Objekt Pfad angegebene Verzeichniseintrags Datei (diese Methode ist eine erweiterte Version der changesecurrityberechtigungs-Methode).
ms.assetid: 787e48af-7cb4-4d0b-a2f1-ffa696466ef2
ms.tgt_platform: multiple
title: Changesecurritypermissionsex-Methode der Win32_Directory-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4bcadd4a4ad115a1a367db4f2a2f645eb6a4742c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214129"
---
# <a name="changesecuritypermissionsex-method-of-the-win32_directory-class"></a><span data-ttu-id="eafba-103">Changesecurritypermissionsex-Methode der Win32- \_ Verzeichnis Klasse</span><span class="sxs-lookup"><span data-stu-id="eafba-103">ChangeSecurityPermissionsEx method of the Win32\_Directory class</span></span>

<span data-ttu-id="eafba-104">Die [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode **changesecurritypermissionsex** ändert die Sicherheits Berechtigungen für die im Objekt Pfad angegebene Verzeichniseintrags Datei (diese Methode ist eine erweiterte Version der [**changesecurrityberechtigungs**](changesecuritypermissions-method-in-class-win32-directory.md) -Methode).</span><span class="sxs-lookup"><span data-stu-id="eafba-104">The **ChangeSecurityPermissionsEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method changes the security permissions for the directory entry file specified in the object path (this method is an extended version of the [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-win32-directory.md) method).</span></span> <span data-ttu-id="eafba-105">Wenn die logische Datei ein Verzeichnis ist, ist diese Methode rekursiv und ändert die Sicherheits Berechtigungen aller Dateien und Unterverzeichnisse, die im Verzeichnis enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="eafba-105">If the logical file is a directory, then this method is recursive, and changes the security permissions of all of the files and subdirectories that the directory contains.</span></span>

<span data-ttu-id="eafba-106">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="eafba-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="eafba-107">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="eafba-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="eafba-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="eafba-108">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissionsEx(
  [in]           Win32_SecurityDescriptor SecurityDescriptor,
  [in]           uint32                   Option,
  [out]          string                   StopFileName,
  [in, optional] string                   StartFileName,
  [in, optional] boolean                  Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="eafba-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="eafba-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eafba-110">*SecurityDescriptor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eafba-110">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eafba-111">Ein Ausdruck, der zu einer Instanz von [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="eafba-111">Expression that resolves to an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span> <span data-ttu-id="eafba-112">Dieser Parameter enthält neue Sicherheits Berechtigungen für die Instanz von [**Win32 \_ Page File**](win32-pagefile.md).</span><span class="sxs-lookup"><span data-stu-id="eafba-112">This parameter contains new security permissions for the instance of [**Win32\_PageFile**](win32-pagefile.md).</span></span>

</dd> <dt>

<span data-ttu-id="eafba-113">*Option* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eafba-113">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eafba-114">Sicherheits Berechtigung, die geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="eafba-114">Security privilege to be modified.</span></span> <span data-ttu-id="eafba-115">Wenn Sie z. b. den Besitzer und die DACL-Sicherheit (-Zugriffs Steuerungs Liste) ändern möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="eafba-115">For example, to change the owner and discretionary access control list (DACL) security, use the following:</span></span>

`Option = 1 + 4`

<span data-ttu-id="eafba-116">Oder</span><span class="sxs-lookup"><span data-stu-id="eafba-116">-or-</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="eafba-117"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Ändern \_ \_Sicherheits \_ Informationen** für den Besitzer (1)</span><span class="sxs-lookup"><span data-stu-id="eafba-117"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="eafba-118">Ändern Sie den Besitzer der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="eafba-118">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="eafba-119"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Ändern \_ Gruppen \_ Sicherheits \_ Informationen** (2)</span><span class="sxs-lookup"><span data-stu-id="eafba-119"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="eafba-120">Ändern Sie die Gruppe der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="eafba-120">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="eafba-121"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Ändern \_ DACL- \_ Sicherheits \_ Informationen** (4)</span><span class="sxs-lookup"><span data-stu-id="eafba-121"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="eafba-122">Ändern Sie die DACL-Liste der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="eafba-122">Change the DACL list of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="eafba-123"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Ändern \_ SACL- \_ Sicherheits \_ Informationen** (8)</span><span class="sxs-lookup"><span data-stu-id="eafba-123"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="eafba-124">Ändern Sie die System Zugriffs Steuerungs Liste (SACL) der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="eafba-124">Change the system access control list (SACL) of the logical file.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="eafba-125">*Stop filename* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="eafba-125">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eafba-126">Der Name der Datei oder des Verzeichnisses, in der die **changesecurritypermissionsex** -Methode fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="eafba-126">Name of the file or directory where the **ChangeSecurityPermissionsEx** method failed.</span></span> <span data-ttu-id="eafba-127">Dieser Parameter ist NULL, wenn die Methode erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="eafba-127">This parameter is null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="eafba-128">*Startdateiname* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="eafba-128">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="eafba-129">Benennt die untergeordnete Datei oder das Verzeichnis, die als Ausgangspunkt für **changesecurritypermissionsex** verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="eafba-129">Names the child file or directory to use as a starting point for **ChangeSecurityPermissionsEx**.</span></span> <span data-ttu-id="eafba-130">In der Regel ist der Parameter " *StartFileName* " der Parameter " *StopFileName* ", der die Datei oder das Verzeichnis angibt, in dem ein Fehler beim vorherigen Methoden aufzurufen aufgetreten ist</span><span class="sxs-lookup"><span data-stu-id="eafba-130">Typically, the *StartFileName* parameter is the *StopFileName* parameter that specifies the file or directory where an error occurred from the previous method call.</span></span> <span data-ttu-id="eafba-131">Wenn dieser Parameter NULL ist, wird der Vorgang für die Datei oder das Verzeichnis ausgeführt, das im **ExecMethod** -Befehl angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="eafba-131">If this parameter is null, the operation is performed on the file or directory that is specified in the **ExecMethod** call.</span></span> <span data-ttu-id="eafba-132">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="eafba-132">This parameter is optional.</span></span>

<span data-ttu-id="eafba-133">Wenn *StartFileName* verwendet wird, muss *rekursive* auch auf true festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="eafba-133">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="eafba-134">*Rekursiv* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="eafba-134">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="eafba-135">**True** gibt an, dass die Eigentums Änderung rekursiv auf Dateien und Verzeichnisse innerhalb des Verzeichnisses angewendet wird, das von der [**CIM \_ LogicalFile**](cim-logicalfile.md) -Instanz angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="eafba-135">If **true**, the change of ownership is applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="eafba-136">Bei Datei Instanzen wird der *rekursive* Eingabeparameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="eafba-136">For file instances, the *Recursive* input parameter is ignored.</span></span> <span data-ttu-id="eafba-137">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="eafba-137">This parameter is optional.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eafba-138">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eafba-138">Return value</span></span>

<span data-ttu-id="eafba-139">Gibt den Wert 0 (null) zurück, wenn die Berechtigungen geändert werden, und eine andere Zahl, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="eafba-139">Returns a value of 0 (zero) if the permissions are changed, and a different number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="eafba-140">**Erfolgreich**</span><span class="sxs-lookup"><span data-stu-id="eafba-140">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="eafba-141">0</span><span class="sxs-lookup"><span data-stu-id="eafba-141">0</span></span>

<span data-ttu-id="eafba-142">Die Anforderung ist erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="eafba-142">The request is successful.</span></span>

</dd> <dt>

<span data-ttu-id="eafba-143">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="eafba-143">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="eafba-144">2</span><span class="sxs-lookup"><span data-stu-id="eafba-144">2</span></span>

<span data-ttu-id="eafba-145">Zugriff verweigert.“</span><span class="sxs-lookup"><span data-stu-id="eafba-145">Access is denied.</span></span>

</dd> <dt>

<span data-ttu-id="eafba-146">**Nicht spezifizierter Fehler**</span><span class="sxs-lookup"><span data-stu-id="eafba-146">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="eafba-147">8</span><span class="sxs-lookup"><span data-stu-id="eafba-147">8</span></span>

<span data-ttu-id="eafba-148">Ein nicht angegebener Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="eafba-148">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="eafba-149">**Ungültiges Objekt**</span><span class="sxs-lookup"><span data-stu-id="eafba-149">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="eafba-150">9</span><span class="sxs-lookup"><span data-stu-id="eafba-150">9</span></span>

<span data-ttu-id="eafba-151">Der angegebene Name ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="eafba-151">The specified name is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="eafba-152">**Objekt ist bereits vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="eafba-152">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="eafba-153">10</span><span class="sxs-lookup"><span data-stu-id="eafba-153">10</span></span>

<span data-ttu-id="eafba-154">Das Objekt "" ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="eafba-154">The specified object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="eafba-155">**Dateisystem nicht NTFS**</span><span class="sxs-lookup"><span data-stu-id="eafba-155">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="eafba-156">11</span><span class="sxs-lookup"><span data-stu-id="eafba-156">11</span></span>

<span data-ttu-id="eafba-157">Das Dateisystem ist kein NTFS-Dateisystem.</span><span class="sxs-lookup"><span data-stu-id="eafba-157">The file system is not an NTFS file system.</span></span>

</dd> <dt>

<span data-ttu-id="eafba-158">**Plattform nicht NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="eafba-158">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="eafba-159">12</span><span class="sxs-lookup"><span data-stu-id="eafba-159">12</span></span>

<span data-ttu-id="eafba-160">Die Plattform ist nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="eafba-160">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="eafba-161">**Laufwerk nicht identisch**</span><span class="sxs-lookup"><span data-stu-id="eafba-161">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="eafba-162">13</span><span class="sxs-lookup"><span data-stu-id="eafba-162">13</span></span>

<span data-ttu-id="eafba-163">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="eafba-163">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="eafba-164">**Verzeichnis nicht leer**</span><span class="sxs-lookup"><span data-stu-id="eafba-164">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="eafba-165">14</span><span class="sxs-lookup"><span data-stu-id="eafba-165">14</span></span>

<span data-ttu-id="eafba-166">Das Verzeichnis ist nicht leer.</span><span class="sxs-lookup"><span data-stu-id="eafba-166">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="eafba-167">**Freigabe Verletzung**</span><span class="sxs-lookup"><span data-stu-id="eafba-167">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="eafba-168">15</span><span class="sxs-lookup"><span data-stu-id="eafba-168">15</span></span>

<span data-ttu-id="eafba-169">Eine Freigabe Verletzung ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="eafba-169">There is a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="eafba-170">**Ungültige Startdatei**</span><span class="sxs-lookup"><span data-stu-id="eafba-170">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="eafba-171">16</span><span class="sxs-lookup"><span data-stu-id="eafba-171">16</span></span>

<span data-ttu-id="eafba-172">Die angegebene Startdatei ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="eafba-172">The specified start file is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="eafba-173">**Berechtigung nicht aufrechterhalten**</span><span class="sxs-lookup"><span data-stu-id="eafba-173">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="eafba-174">17</span><span class="sxs-lookup"><span data-stu-id="eafba-174">17</span></span>

<span data-ttu-id="eafba-175">Eine für den Vorgang erforderliche Berechtigung wird nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="eafba-175">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="eafba-176">**Ungültiger Parameter**</span><span class="sxs-lookup"><span data-stu-id="eafba-176">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="eafba-177">21</span><span class="sxs-lookup"><span data-stu-id="eafba-177">21</span></span>

<span data-ttu-id="eafba-178">Ein angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="eafba-178">A specified parameter is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="eafba-179">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eafba-179">Requirements</span></span>



| <span data-ttu-id="eafba-180">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eafba-180">Requirement</span></span> | <span data-ttu-id="eafba-181">Wert</span><span class="sxs-lookup"><span data-stu-id="eafba-181">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eafba-182">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eafba-182">Minimum supported client</span></span><br/> | <span data-ttu-id="eafba-183">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eafba-183">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="eafba-184">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eafba-184">Minimum supported server</span></span><br/> | <span data-ttu-id="eafba-185">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eafba-185">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="eafba-186">Namespace</span><span class="sxs-lookup"><span data-stu-id="eafba-186">Namespace</span></span><br/>                | <span data-ttu-id="eafba-187">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="eafba-187">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="eafba-188">MOF</span><span class="sxs-lookup"><span data-stu-id="eafba-188">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eafba-189"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="eafba-189"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="eafba-190">DLL</span><span class="sxs-lookup"><span data-stu-id="eafba-190">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eafba-191"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eafba-191"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eafba-192">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eafba-192">See also</span></span>

<dl> <dt>

<span data-ttu-id="eafba-193">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="eafba-193">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="eafba-194">**Win32- \_ Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="eafba-194">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

