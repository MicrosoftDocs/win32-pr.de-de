---
description: Ändert die Sicherheits Berechtigungen für die Datei des logischen Geräts, die im Objekt Pfad angegeben ist.
ms.assetid: 4b3e1a0e-3c9e-45bb-8c7b-cbbc8f9d1265
ms.tgt_platform: multiple
title: Changesecurrityberechtigungs-Methode der CIM_DeviceFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 73a772c17695a537e4a9a8518bf05b052c0417f6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483558"
---
# <a name="changesecuritypermissions-method-of-the-cim_devicefile-class"></a><span data-ttu-id="d19c8-103">Changesecurrityberechtigungs-Methode der CIM \_ Devicefile-Klasse</span><span class="sxs-lookup"><span data-stu-id="d19c8-103">ChangeSecurityPermissions method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="d19c8-104">Die **changesecurrityberechtigungs** -Methode ändert die Sicherheits Berechtigungen für die Datei des logischen Geräts, die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="d19c8-104">The **ChangeSecurityPermissions** method changes the security permissions for the logical device file specified in the object path.</span></span> <span data-ttu-id="d19c8-105">Wenn die logische Datei ein Verzeichnis ist, wird diese Methode rekursiv ausgeführt, und die Sicherheits Berechtigungen für alle Dateien und Unterverzeichnisse, die im Verzeichnis enthalten sind, werden geändert.</span><span class="sxs-lookup"><span data-stu-id="d19c8-105">If the logical file is a directory, then this method will act recursively, changing the security permissions for all of the files and sub-directories that the directory contains.</span></span> <span data-ttu-id="d19c8-106">Diese Methode wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d19c8-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d19c8-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d19c8-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d19c8-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d19c8-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d19c8-109">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="d19c8-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="d19c8-110">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="d19c8-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="d19c8-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="d19c8-111">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a><span data-ttu-id="d19c8-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="d19c8-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d19c8-113">*SecurityDescriptor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d19c8-113">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d19c8-114">Gibt die Sicherheitsinformationen an.</span><span class="sxs-lookup"><span data-stu-id="d19c8-114">Specifies the security information.</span></span>

> [!Caution]  
> <span data-ttu-id="d19c8-115">Eine **Zugriffs** Steuerungs Liste (Access Control List, ACL) in der [**Sicherheits \_ Deskriptor**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) -Struktur gewährt uneingeschränkten Zugriff.</span><span class="sxs-lookup"><span data-stu-id="d19c8-115">A **NULL** access control list (ACL) in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure grants unlimited access.</span></span>

 

</dd> <dt>

<span data-ttu-id="d19c8-116">*Option* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d19c8-116">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d19c8-117">Zu ändernde Sicherheits Berechtigung.</span><span class="sxs-lookup"><span data-stu-id="d19c8-117">Security privilege to modify.</span></span> <span data-ttu-id="d19c8-118">Um z. b. den Besitzer und die DACL-Sicherheit zu ändern, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="d19c8-118">For example, to change the owner and DACL security, use:</span></span>

`Option = 1 + 4`

<span data-ttu-id="d19c8-119">oder</span><span class="sxs-lookup"><span data-stu-id="d19c8-119">or</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="d19c8-120"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Ändern \_ \_Sicherheits \_ Informationen** für den Besitzer (1)</span><span class="sxs-lookup"><span data-stu-id="d19c8-120"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="d19c8-121">Ändern Sie den Besitzer der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="d19c8-121">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="d19c8-122"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Ändern \_ Gruppen \_ Sicherheits \_ Informationen** (2)</span><span class="sxs-lookup"><span data-stu-id="d19c8-122"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="d19c8-123">Ändern Sie die Gruppe der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="d19c8-123">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="d19c8-124"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Ändern \_ DACL- \_ Sicherheits \_ Informationen** (4)</span><span class="sxs-lookup"><span data-stu-id="d19c8-124"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="d19c8-125">Ändern Sie die ACL der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="d19c8-125">Change the ACL of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="d19c8-126"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Ändern \_ SACL- \_ Sicherheits \_ Informationen** (8)</span><span class="sxs-lookup"><span data-stu-id="d19c8-126"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="d19c8-127">Ändern Sie die System-ACL der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="d19c8-127">Change the system ACL of the logical file.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d19c8-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d19c8-128">Return value</span></span>

<span data-ttu-id="d19c8-129">Gibt bei Erfolg den Wert 0 (null) zurück, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="d19c8-129">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="d19c8-130">**Erfolgreich**</span><span class="sxs-lookup"><span data-stu-id="d19c8-130">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="d19c8-131">0</span><span class="sxs-lookup"><span data-stu-id="d19c8-131">0</span></span>

<span data-ttu-id="d19c8-132">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="d19c8-132">Success.</span></span>

</dd> <dt>

<span data-ttu-id="d19c8-133">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="d19c8-133">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="d19c8-134">2</span><span class="sxs-lookup"><span data-stu-id="d19c8-134">2</span></span>

<span data-ttu-id="d19c8-135">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="d19c8-135">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="d19c8-136">**Nicht spezifizierter Fehler**</span><span class="sxs-lookup"><span data-stu-id="d19c8-136">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="d19c8-137">8</span><span class="sxs-lookup"><span data-stu-id="d19c8-137">8</span></span>

<span data-ttu-id="d19c8-138">Nicht spezifizierter Fehler.</span><span class="sxs-lookup"><span data-stu-id="d19c8-138">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="d19c8-139">**Ungültiges Objekt**</span><span class="sxs-lookup"><span data-stu-id="d19c8-139">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="d19c8-140">9</span><span class="sxs-lookup"><span data-stu-id="d19c8-140">9</span></span>

<span data-ttu-id="d19c8-141">Ungültiges Objekt.</span><span class="sxs-lookup"><span data-stu-id="d19c8-141">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="d19c8-142">**Objekt ist bereits vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="d19c8-142">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="d19c8-143">10</span><span class="sxs-lookup"><span data-stu-id="d19c8-143">10</span></span>

<span data-ttu-id="d19c8-144">Das Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d19c8-144">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="d19c8-145">**Dateisystem nicht NTFS**</span><span class="sxs-lookup"><span data-stu-id="d19c8-145">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="d19c8-146">11</span><span class="sxs-lookup"><span data-stu-id="d19c8-146">11</span></span>

<span data-ttu-id="d19c8-147">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="d19c8-147">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="d19c8-148">**Plattform nicht NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="d19c8-148">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="d19c8-149">12</span><span class="sxs-lookup"><span data-stu-id="d19c8-149">12</span></span>

<span data-ttu-id="d19c8-150">Plattform nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="d19c8-150">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="d19c8-151">**Laufwerk nicht identisch**</span><span class="sxs-lookup"><span data-stu-id="d19c8-151">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="d19c8-152">13</span><span class="sxs-lookup"><span data-stu-id="d19c8-152">13</span></span>

<span data-ttu-id="d19c8-153">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="d19c8-153">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="d19c8-154">**Verzeichnis nicht leer**</span><span class="sxs-lookup"><span data-stu-id="d19c8-154">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="d19c8-155">14</span><span class="sxs-lookup"><span data-stu-id="d19c8-155">14</span></span>

<span data-ttu-id="d19c8-156">„Verzeichnis ist nicht leer.“</span><span class="sxs-lookup"><span data-stu-id="d19c8-156">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="d19c8-157">**Freigabe Verletzung**</span><span class="sxs-lookup"><span data-stu-id="d19c8-157">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="d19c8-158">15</span><span class="sxs-lookup"><span data-stu-id="d19c8-158">15</span></span>

<span data-ttu-id="d19c8-159">Freigabeverletzung.</span><span class="sxs-lookup"><span data-stu-id="d19c8-159">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="d19c8-160">**Ungültige Startdatei**</span><span class="sxs-lookup"><span data-stu-id="d19c8-160">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="d19c8-161">16</span><span class="sxs-lookup"><span data-stu-id="d19c8-161">16</span></span>

<span data-ttu-id="d19c8-162">Ungültige Startdatei.</span><span class="sxs-lookup"><span data-stu-id="d19c8-162">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="d19c8-163">**Berechtigung nicht aufrechterhalten**</span><span class="sxs-lookup"><span data-stu-id="d19c8-163">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="d19c8-164">17</span><span class="sxs-lookup"><span data-stu-id="d19c8-164">17</span></span>

<span data-ttu-id="d19c8-165">Die Berechtigung wurde nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="d19c8-165">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="d19c8-166">**Ungültiger Parameter**</span><span class="sxs-lookup"><span data-stu-id="d19c8-166">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="d19c8-167">21</span><span class="sxs-lookup"><span data-stu-id="d19c8-167">21</span></span>

<span data-ttu-id="d19c8-168">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="d19c8-168">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d19c8-169">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d19c8-169">Remarks</span></span>

<span data-ttu-id="d19c8-170">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="d19c8-170">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="d19c8-171">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="d19c8-171">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="d19c8-172">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="d19c8-172">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d19c8-173">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="d19c8-173">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d19c8-174">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d19c8-174">Requirements</span></span>



| <span data-ttu-id="d19c8-175">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d19c8-175">Requirement</span></span> | <span data-ttu-id="d19c8-176">Wert</span><span class="sxs-lookup"><span data-stu-id="d19c8-176">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d19c8-177">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d19c8-177">Minimum supported client</span></span><br/> | <span data-ttu-id="d19c8-178">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d19c8-178">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d19c8-179">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d19c8-179">Minimum supported server</span></span><br/> | <span data-ttu-id="d19c8-180">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d19c8-180">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d19c8-181">Namespace</span><span class="sxs-lookup"><span data-stu-id="d19c8-181">Namespace</span></span><br/>                | <span data-ttu-id="d19c8-182">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d19c8-182">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d19c8-183">MOF</span><span class="sxs-lookup"><span data-stu-id="d19c8-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d19c8-184"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="d19c8-184"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d19c8-185">DLL</span><span class="sxs-lookup"><span data-stu-id="d19c8-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d19c8-186"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d19c8-186"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d19c8-187">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d19c8-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d19c8-188">**CIM- \_ Devicefile**</span><span class="sxs-lookup"><span data-stu-id="d19c8-188">**CIM\_DeviceFile**</span></span>](changesecuritypermissions-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="d19c8-189">**CIM- \_ Devicefile**</span><span class="sxs-lookup"><span data-stu-id="d19c8-189">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

