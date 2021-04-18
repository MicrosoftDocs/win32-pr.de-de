---
description: Ändert die Sicherheits Berechtigungen für die logische Datei, die im Objekt Pfad angegeben ist.
ms.assetid: a3caa717-ad37-4e4f-9f4e-f37aed382fa4
ms.tgt_platform: multiple
title: Changesecurrityberechtigungs-Methode der CIM_LogicalFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 929e05047af203d8e2344afa8175228e3bd969fd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106340125"
---
# <a name="changesecuritypermissions-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="b82f8-103">Changesecurrityberechtigungs-Methode der CIM \_ LogicalFile-Klasse</span><span class="sxs-lookup"><span data-stu-id="b82f8-103">ChangeSecurityPermissions method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="b82f8-104">Die **changesecurrityberechtigungs** -Methode ändert die Sicherheits Berechtigungen für die logische Datei, die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="b82f8-104">The **ChangeSecurityPermissions** method changes the security permissions for the logical file specified in the object path.</span></span> <span data-ttu-id="b82f8-105">Wenn es sich bei der logischen Datei um ein Verzeichnis handelt, werden **changesekurityberechtigungen** rekursiv ausgeführt, und die Sicherheits Berechtigungen für alle Dateien und Unterverzeichnisse, die im Verzeichnis enthalten sind, werden geändert.</span><span class="sxs-lookup"><span data-stu-id="b82f8-105">If the logical file is a directory, then **ChangeSecurityPermissions** will act recursively, changing the security permissions for all of the files and sub-directories that the directory contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b82f8-106">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="b82f8-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b82f8-107">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b82f8-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b82f8-108">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="b82f8-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="b82f8-109">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="b82f8-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="b82f8-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="b82f8-110">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a><span data-ttu-id="b82f8-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="b82f8-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b82f8-112">*SecurityDescriptor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b82f8-112">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b82f8-113">Gibt Sicherheitsinformationen an.</span><span class="sxs-lookup"><span data-stu-id="b82f8-113">Specifies security information.</span></span>

> [!Note]  
> <span data-ttu-id="b82f8-114">Eine Zugriffs Steuerungs Liste (Access Control List, ACL) für **null** in der [**Sicherheits \_ Beschreibung**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) gewährt uneingeschränkten Zugriff.</span><span class="sxs-lookup"><span data-stu-id="b82f8-114">A **NULL** access control list (ACL) in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) grants unlimited access.</span></span>

 

</dd> <dt>

<span data-ttu-id="b82f8-115">*Option* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b82f8-115">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b82f8-116">Zu ändernde Sicherheits Berechtigung.</span><span class="sxs-lookup"><span data-stu-id="b82f8-116">Security privilege to modify.</span></span> <span data-ttu-id="b82f8-117">Um z. b. den Besitzer und die DACL-Sicherheit zu ändern, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="b82f8-117">For example, to change the owner and DACL security, use:</span></span>

`Option = 1 + 4`

<span data-ttu-id="b82f8-118">oder</span><span class="sxs-lookup"><span data-stu-id="b82f8-118">or</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="Change_Owner_Security_Information"></span><span id="change_owner_security_information"></span><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span>

<span data-ttu-id="b82f8-119"><span id="Change_Owner_Security_Information"></span><span id="change_owner_security_information"></span><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span>**Ändern \_ \_Sicherheits \_ Informationen** für den Besitzer (1)</span><span class="sxs-lookup"><span data-stu-id="b82f8-119"><span id="Change_Owner_Security_Information"></span><span id="change_owner_security_information"></span><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span>**Change\_Owner\_Security\_Information** (1)</span></span>


</dt> <dd>

<span data-ttu-id="b82f8-120">Ändern Sie den Besitzer der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="b82f8-120">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="Change_Group_Security_Information"></span><span id="change_group_security_information"></span><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span>

<span data-ttu-id="b82f8-121"><span id="Change_Group_Security_Information"></span><span id="change_group_security_information"></span><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span>**Ändern \_ Gruppen \_ Sicherheits \_ Informationen** (2)</span><span class="sxs-lookup"><span data-stu-id="b82f8-121"><span id="Change_Group_Security_Information"></span><span id="change_group_security_information"></span><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span>**Change\_Group\_Security\_Information** (2)</span></span>


</dt> <dd>

<span data-ttu-id="b82f8-122">Ändern Sie die Gruppe der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="b82f8-122">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="Change_Dacl_Security_Information"></span><span id="change_dacl_security_information"></span><span id="CHANGE_DACL_SECURITY_INFORMATION"></span>

<span data-ttu-id="b82f8-123"><span id="Change_Dacl_Security_Information"></span><span id="change_dacl_security_information"></span><span id="CHANGE_DACL_SECURITY_INFORMATION"></span>**Ändern \_ DACL- \_ Sicherheits \_ Informationen** (4)</span><span class="sxs-lookup"><span data-stu-id="b82f8-123"><span id="Change_Dacl_Security_Information"></span><span id="change_dacl_security_information"></span><span id="CHANGE_DACL_SECURITY_INFORMATION"></span>**Change\_Dacl\_Security\_Information** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b82f8-124">Ändern Sie die ACL der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="b82f8-124">Change the ACL of the logical file.</span></span>

</dd> <dt>

<span id="Change_Sacl_Security_Information"></span><span id="change_sacl_security_information"></span><span id="CHANGE_SACL_SECURITY_INFORMATION"></span>

<span data-ttu-id="b82f8-125"><span id="Change_Sacl_Security_Information"></span><span id="change_sacl_security_information"></span><span id="CHANGE_SACL_SECURITY_INFORMATION"></span>**Ändern \_ SACL- \_ Sicherheits \_ Informationen** (8)</span><span class="sxs-lookup"><span data-stu-id="b82f8-125"><span id="Change_Sacl_Security_Information"></span><span id="change_sacl_security_information"></span><span id="CHANGE_SACL_SECURITY_INFORMATION"></span>**Change\_Sacl\_Security\_Information** (8)</span></span>


</dt> <dd>

<span data-ttu-id="b82f8-126">Ändern Sie die System-ACL der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="b82f8-126">Change the system ACL of the logical file.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b82f8-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b82f8-127">Return value</span></span>

<span data-ttu-id="b82f8-128">Gibt bei Erfolg den Wert 0 zurück, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="b82f8-128">Returns a value of 0 on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="b82f8-129">**Erfolgreich**</span><span class="sxs-lookup"><span data-stu-id="b82f8-129">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="b82f8-130">0</span><span class="sxs-lookup"><span data-stu-id="b82f8-130">0</span></span>

<span data-ttu-id="b82f8-131">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="b82f8-131">Success.</span></span>

</dd> <dt>

<span data-ttu-id="b82f8-132">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="b82f8-132">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="b82f8-133">2</span><span class="sxs-lookup"><span data-stu-id="b82f8-133">2</span></span>

<span data-ttu-id="b82f8-134">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="b82f8-134">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="b82f8-135">**Nicht spezifizierter Fehler**</span><span class="sxs-lookup"><span data-stu-id="b82f8-135">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="b82f8-136">8</span><span class="sxs-lookup"><span data-stu-id="b82f8-136">8</span></span>

<span data-ttu-id="b82f8-137">Nicht spezifizierter Fehler.</span><span class="sxs-lookup"><span data-stu-id="b82f8-137">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="b82f8-138">**Ungültiges Objekt**</span><span class="sxs-lookup"><span data-stu-id="b82f8-138">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="b82f8-139">9</span><span class="sxs-lookup"><span data-stu-id="b82f8-139">9</span></span>

<span data-ttu-id="b82f8-140">Ungültiges Objekt.</span><span class="sxs-lookup"><span data-stu-id="b82f8-140">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="b82f8-141">**Objekt ist bereits vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="b82f8-141">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="b82f8-142">10</span><span class="sxs-lookup"><span data-stu-id="b82f8-142">10</span></span>

<span data-ttu-id="b82f8-143">Das Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="b82f8-143">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="b82f8-144">**Dateisystem nicht NTFS**</span><span class="sxs-lookup"><span data-stu-id="b82f8-144">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="b82f8-145">11</span><span class="sxs-lookup"><span data-stu-id="b82f8-145">11</span></span>

<span data-ttu-id="b82f8-146">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="b82f8-146">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="b82f8-147">**Plattform nicht NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="b82f8-147">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="b82f8-148">12</span><span class="sxs-lookup"><span data-stu-id="b82f8-148">12</span></span>

<span data-ttu-id="b82f8-149">Plattform nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="b82f8-149">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="b82f8-150">**Laufwerk nicht identisch**</span><span class="sxs-lookup"><span data-stu-id="b82f8-150">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="b82f8-151">13</span><span class="sxs-lookup"><span data-stu-id="b82f8-151">13</span></span>

<span data-ttu-id="b82f8-152">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="b82f8-152">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="b82f8-153">**Verzeichnis nicht leer**</span><span class="sxs-lookup"><span data-stu-id="b82f8-153">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="b82f8-154">14</span><span class="sxs-lookup"><span data-stu-id="b82f8-154">14</span></span>

<span data-ttu-id="b82f8-155">„Verzeichnis ist nicht leer.“</span><span class="sxs-lookup"><span data-stu-id="b82f8-155">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="b82f8-156">**Freigabe Verletzung**</span><span class="sxs-lookup"><span data-stu-id="b82f8-156">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="b82f8-157">15</span><span class="sxs-lookup"><span data-stu-id="b82f8-157">15</span></span>

<span data-ttu-id="b82f8-158">Freigabeverletzung.</span><span class="sxs-lookup"><span data-stu-id="b82f8-158">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="b82f8-159">**Ungültige Startdatei**</span><span class="sxs-lookup"><span data-stu-id="b82f8-159">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="b82f8-160">16</span><span class="sxs-lookup"><span data-stu-id="b82f8-160">16</span></span>

<span data-ttu-id="b82f8-161">Ungültige Startdatei.</span><span class="sxs-lookup"><span data-stu-id="b82f8-161">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="b82f8-162">**Berechtigung nicht aufrechterhalten**</span><span class="sxs-lookup"><span data-stu-id="b82f8-162">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="b82f8-163">17</span><span class="sxs-lookup"><span data-stu-id="b82f8-163">17</span></span>

<span data-ttu-id="b82f8-164">Die Berechtigung wurde nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="b82f8-164">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="b82f8-165">**Ungültiger Parameter**</span><span class="sxs-lookup"><span data-stu-id="b82f8-165">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="b82f8-166">21</span><span class="sxs-lookup"><span data-stu-id="b82f8-166">21</span></span>

<span data-ttu-id="b82f8-167">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="b82f8-167">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b82f8-168">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b82f8-168">Remarks</span></span>

<span data-ttu-id="b82f8-169">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="b82f8-169">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="b82f8-170">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="b82f8-170">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="b82f8-171">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="b82f8-171">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b82f8-172">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="b82f8-172">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b82f8-173">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b82f8-173">Requirements</span></span>



| <span data-ttu-id="b82f8-174">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b82f8-174">Requirement</span></span> | <span data-ttu-id="b82f8-175">Wert</span><span class="sxs-lookup"><span data-stu-id="b82f8-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b82f8-176">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b82f8-176">Minimum supported client</span></span><br/> | <span data-ttu-id="b82f8-177">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b82f8-177">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b82f8-178">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b82f8-178">Minimum supported server</span></span><br/> | <span data-ttu-id="b82f8-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b82f8-179">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b82f8-180">Namespace</span><span class="sxs-lookup"><span data-stu-id="b82f8-180">Namespace</span></span><br/>                | <span data-ttu-id="b82f8-181">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b82f8-181">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b82f8-182">MOF</span><span class="sxs-lookup"><span data-stu-id="b82f8-182">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b82f8-183"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b82f8-183"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b82f8-184">DLL</span><span class="sxs-lookup"><span data-stu-id="b82f8-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b82f8-185"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b82f8-185"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b82f8-186">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b82f8-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b82f8-187">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="b82f8-187">**CIM\_LogicalFile**</span></span>](changesecuritypermissions-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="b82f8-188">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="b82f8-188">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

