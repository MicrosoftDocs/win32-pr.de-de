---
description: Ändert die Sicherheits Berechtigungen für die logische Datei, die im Objekt Pfad angegeben ist (diese Methode ist eine erweiterte Version der changesecurrityberechtigungs Methode).
ms.assetid: 29155533-0898-4f8f-af08-f3ea46c8c1d3
ms.tgt_platform: multiple
title: Changesecurritypermissionsex-Methode der CIM_LogicalFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: af2dc82ef54b6f32eee20f17cd61c0769cc64b1a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523512"
---
# <a name="changesecuritypermissionsex-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="cbc02-103">Changesecurritypermissionsex-Methode der CIM \_ LogicalFile-Klasse</span><span class="sxs-lookup"><span data-stu-id="cbc02-103">ChangeSecurityPermissionsEx method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="cbc02-104">Die **changesecurritypermissionsex** -Methode ändert die Sicherheits Berechtigungen für die logische Datei, die im Objekt Pfad angegeben ist (diese Methode ist eine erweiterte Version der [**changesecurrityberechtigungs**](changesecuritypermissions-method-in-class-cim-logicalfile.md) -Methode).</span><span class="sxs-lookup"><span data-stu-id="cbc02-104">The **ChangeSecurityPermissionsEx** method changes the security permissions for the logical file specified in the object path (this method is an extended version of the [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-logicalfile.md) method).</span></span> <span data-ttu-id="cbc02-105">Wenn die logische Datei ein Verzeichnis ist, wird diese Methode rekursiv ausgeführt, und die Sicherheits Berechtigungen für alle Dateien und Unterverzeichnisse, die im Verzeichnis enthalten sind, werden geändert.</span><span class="sxs-lookup"><span data-stu-id="cbc02-105">If the logical file is a directory, then this method will act recursively, changing the security permissions for all of the files and sub-directories that the directory contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cbc02-106">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="cbc02-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="cbc02-107">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="cbc02-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="cbc02-108">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="cbc02-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="cbc02-109">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="cbc02-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="cbc02-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="cbc02-110">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissionsEx(
  [in]           Win32_SecurityDescriptor SecurityDescriptor,
  [in]           uint32                   Option,
  [out]          string                   StopFileName,
  [in, optional] string                   StartFileName,
  [in, optional] boolean                  Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="cbc02-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="cbc02-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbc02-112">*SecurityDescriptor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cbc02-112">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbc02-113">Gibt die Sicherheitsinformationen an.</span><span class="sxs-lookup"><span data-stu-id="cbc02-113">Specifies the security information.</span></span>

</dd> <dt>

<span data-ttu-id="cbc02-114">*Option* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cbc02-114">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbc02-115">Zu ändernde Sicherheits Berechtigung.</span><span class="sxs-lookup"><span data-stu-id="cbc02-115">Security privilege to modify.</span></span> <span data-ttu-id="cbc02-116">Wenn Sie z. b. den Besitzer und die DACL-Sicherheit ändern möchten, verwenden Sie</span><span class="sxs-lookup"><span data-stu-id="cbc02-116">For example, to change the owner and DACL security, use</span></span>

`Option = 1 + 4`

<span data-ttu-id="cbc02-117">oder</span><span class="sxs-lookup"><span data-stu-id="cbc02-117">or</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="Change_Owner_Security_Information"></span><span id="change_owner_security_information"></span><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span>

<span data-ttu-id="cbc02-118"><span id="Change_Owner_Security_Information"></span><span id="change_owner_security_information"></span><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span>**Ändern \_ \_Sicherheits \_ Informationen** für den Besitzer (1)</span><span class="sxs-lookup"><span data-stu-id="cbc02-118"><span id="Change_Owner_Security_Information"></span><span id="change_owner_security_information"></span><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span>**Change\_Owner\_Security\_Information** (1)</span></span>


</dt> <dd>

<span data-ttu-id="cbc02-119">Ändern Sie den Besitzer der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="cbc02-119">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="Change_Group_Security_Information"></span><span id="change_group_security_information"></span><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span>

<span data-ttu-id="cbc02-120"><span id="Change_Group_Security_Information"></span><span id="change_group_security_information"></span><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span>**Ändern \_ Gruppen \_ Sicherheits \_ Informationen** (2)</span><span class="sxs-lookup"><span data-stu-id="cbc02-120"><span id="Change_Group_Security_Information"></span><span id="change_group_security_information"></span><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span>**Change\_Group\_Security\_Information** (2)</span></span>


</dt> <dd>

<span data-ttu-id="cbc02-121">Ändern Sie die Gruppe der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="cbc02-121">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="Change_Dacl_Security_Information"></span><span id="change_dacl_security_information"></span><span id="CHANGE_DACL_SECURITY_INFORMATION"></span>

<span data-ttu-id="cbc02-122"><span id="Change_Dacl_Security_Information"></span><span id="change_dacl_security_information"></span><span id="CHANGE_DACL_SECURITY_INFORMATION"></span>**Ändern \_ DACL- \_ Sicherheits \_ Informationen** (4)</span><span class="sxs-lookup"><span data-stu-id="cbc02-122"><span id="Change_Dacl_Security_Information"></span><span id="change_dacl_security_information"></span><span id="CHANGE_DACL_SECURITY_INFORMATION"></span>**Change\_Dacl\_Security\_Information** (4)</span></span>


</dt> <dd>

<span data-ttu-id="cbc02-123">Ändern Sie die ACL der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="cbc02-123">Change the ACL of the logical file.</span></span>

</dd> <dt>

<span id="Change_Sacl_Security_Information"></span><span id="change_sacl_security_information"></span><span id="CHANGE_SACL_SECURITY_INFORMATION"></span>

<span data-ttu-id="cbc02-124"><span id="Change_Sacl_Security_Information"></span><span id="change_sacl_security_information"></span><span id="CHANGE_SACL_SECURITY_INFORMATION"></span>**Ändern \_ SACL- \_ Sicherheits \_ Informationen** (8)</span><span class="sxs-lookup"><span data-stu-id="cbc02-124"><span id="Change_Sacl_Security_Information"></span><span id="change_sacl_security_information"></span><span id="CHANGE_SACL_SECURITY_INFORMATION"></span>**Change\_Sacl\_Security\_Information** (8)</span></span>


</dt> <dd>

<span data-ttu-id="cbc02-125">Ändern Sie die System-ACL der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="cbc02-125">Change the system ACL of the logical file.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="cbc02-126">*Stop filename* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="cbc02-126">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cbc02-127">Eine Zeichenfolge, die den Namen der Datei (oder des Verzeichnisses) darstellt, in der die Methode fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="cbc02-127">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="cbc02-128">Dieser Parameter hat den Wert **null** , wenn die Methode erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="cbc02-128">This parameter has a value of **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="cbc02-129">*Startdateiname* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="cbc02-129">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cbc02-130">Eine Zeichenfolge, die die untergeordnete Datei (oder das Verzeichnis) darstellt, die als Ausgangspunkt für diese Methode verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cbc02-130">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="cbc02-131">In der Regel ist der Parameter " *StartFileName* " der Parameter " *StopFileName* ", der die Datei (oder das Verzeichnis) angibt, in der ein Fehler des vorherigen Methoden Aufrufes aufgetreten ist</span><span class="sxs-lookup"><span data-stu-id="cbc02-131">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file (or directory) at which an error occurred from the previous method call.</span></span> <span data-ttu-id="cbc02-132">Wenn der Parameterwert **null** ist, wird der Vorgang für die im [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) -Befehl angegebene Datei oder das Verzeichnis ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cbc02-132">If the parameter value is **null**, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="cbc02-133">*Rekursiv* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="cbc02-133">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cbc02-134">**True** gibt an, dass die Sicherheits Berechtigungen rekursiv auf Dateien und Verzeichnisse innerhalb des Verzeichnisses angewendet werden, das von der [**CIM \_ LogicalFile**](cim-logicalfile.md) -Instanz angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="cbc02-134">If **TRUE**, the security permissions are applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="cbc02-135">Bei Datei Instanzen wird dieser Parameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="cbc02-135">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbc02-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cbc02-136">Return value</span></span>

<span data-ttu-id="cbc02-137">Gibt bei Erfolg den Wert 0 (null) zurück, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="cbc02-137">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="cbc02-138">**Erfolgreich**</span><span class="sxs-lookup"><span data-stu-id="cbc02-138">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="cbc02-139">0</span><span class="sxs-lookup"><span data-stu-id="cbc02-139">0</span></span>

<span data-ttu-id="cbc02-140">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="cbc02-140">Success.</span></span>

</dd> <dt>

<span data-ttu-id="cbc02-141">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="cbc02-141">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="cbc02-142">2</span><span class="sxs-lookup"><span data-stu-id="cbc02-142">2</span></span>

<span data-ttu-id="cbc02-143">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="cbc02-143">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="cbc02-144">**Nicht spezifizierter Fehler**</span><span class="sxs-lookup"><span data-stu-id="cbc02-144">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="cbc02-145">8</span><span class="sxs-lookup"><span data-stu-id="cbc02-145">8</span></span>

<span data-ttu-id="cbc02-146">Nicht spezifizierter Fehler.</span><span class="sxs-lookup"><span data-stu-id="cbc02-146">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="cbc02-147">**Ungültiges Objekt**</span><span class="sxs-lookup"><span data-stu-id="cbc02-147">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="cbc02-148">9</span><span class="sxs-lookup"><span data-stu-id="cbc02-148">9</span></span>

<span data-ttu-id="cbc02-149">Ungültiges Objekt.</span><span class="sxs-lookup"><span data-stu-id="cbc02-149">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="cbc02-150">**Objekt ist bereits vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="cbc02-150">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="cbc02-151">10</span><span class="sxs-lookup"><span data-stu-id="cbc02-151">10</span></span>

<span data-ttu-id="cbc02-152">Das Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="cbc02-152">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="cbc02-153">**Dateisystem nicht NTFS**</span><span class="sxs-lookup"><span data-stu-id="cbc02-153">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="cbc02-154">11</span><span class="sxs-lookup"><span data-stu-id="cbc02-154">11</span></span>

<span data-ttu-id="cbc02-155">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="cbc02-155">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="cbc02-156">**Plattform nicht NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="cbc02-156">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="cbc02-157">12</span><span class="sxs-lookup"><span data-stu-id="cbc02-157">12</span></span>

<span data-ttu-id="cbc02-158">Plattform nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="cbc02-158">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="cbc02-159">**Laufwerk nicht identisch**</span><span class="sxs-lookup"><span data-stu-id="cbc02-159">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="cbc02-160">13</span><span class="sxs-lookup"><span data-stu-id="cbc02-160">13</span></span>

<span data-ttu-id="cbc02-161">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="cbc02-161">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="cbc02-162">**Verzeichnis nicht leer**</span><span class="sxs-lookup"><span data-stu-id="cbc02-162">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="cbc02-163">14</span><span class="sxs-lookup"><span data-stu-id="cbc02-163">14</span></span>

<span data-ttu-id="cbc02-164">„Verzeichnis ist nicht leer.“</span><span class="sxs-lookup"><span data-stu-id="cbc02-164">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="cbc02-165">**Freigabe Verletzung**</span><span class="sxs-lookup"><span data-stu-id="cbc02-165">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="cbc02-166">15</span><span class="sxs-lookup"><span data-stu-id="cbc02-166">15</span></span>

<span data-ttu-id="cbc02-167">Freigabeverletzung.</span><span class="sxs-lookup"><span data-stu-id="cbc02-167">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="cbc02-168">**Ungültige Startdatei**</span><span class="sxs-lookup"><span data-stu-id="cbc02-168">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="cbc02-169">16</span><span class="sxs-lookup"><span data-stu-id="cbc02-169">16</span></span>

<span data-ttu-id="cbc02-170">Ungültige Startdatei.</span><span class="sxs-lookup"><span data-stu-id="cbc02-170">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="cbc02-171">**Berechtigung nicht aufrechterhalten**</span><span class="sxs-lookup"><span data-stu-id="cbc02-171">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="cbc02-172">17</span><span class="sxs-lookup"><span data-stu-id="cbc02-172">17</span></span>

<span data-ttu-id="cbc02-173">Die Berechtigung wurde nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="cbc02-173">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="cbc02-174">**Ungültiger Parameter**</span><span class="sxs-lookup"><span data-stu-id="cbc02-174">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="cbc02-175">21</span><span class="sxs-lookup"><span data-stu-id="cbc02-175">21</span></span>

<span data-ttu-id="cbc02-176">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="cbc02-176">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cbc02-177">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cbc02-177">Remarks</span></span>

<span data-ttu-id="cbc02-178">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="cbc02-178">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="cbc02-179">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="cbc02-179">To use this method, you must implement it in your own provider.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbc02-180">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cbc02-180">Requirements</span></span>



| <span data-ttu-id="cbc02-181">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cbc02-181">Requirement</span></span> | <span data-ttu-id="cbc02-182">Wert</span><span class="sxs-lookup"><span data-stu-id="cbc02-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cbc02-183">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cbc02-183">Minimum supported client</span></span><br/> | <span data-ttu-id="cbc02-184">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cbc02-184">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cbc02-185">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cbc02-185">Minimum supported server</span></span><br/> | <span data-ttu-id="cbc02-186">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cbc02-186">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cbc02-187">Namespace</span><span class="sxs-lookup"><span data-stu-id="cbc02-187">Namespace</span></span><br/>                | <span data-ttu-id="cbc02-188">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="cbc02-188">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cbc02-189">MOF</span><span class="sxs-lookup"><span data-stu-id="cbc02-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cbc02-190"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="cbc02-190"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cbc02-191">DLL</span><span class="sxs-lookup"><span data-stu-id="cbc02-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cbc02-192"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cbc02-192"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbc02-193">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cbc02-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbc02-194">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="cbc02-194">**CIM\_LogicalFile**</span></span>](changesecuritypermissionsex-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="cbc02-195">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="cbc02-195">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

