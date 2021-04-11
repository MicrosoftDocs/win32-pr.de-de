---
description: Ändert die Sicherheits Berechtigungen für die logische Datendatei, die im Objekt Pfad angegeben ist.
ms.assetid: b0a66411-f973-42ce-a3fe-25c31234a964
ms.tgt_platform: multiple
title: Changesecurrityberechtigungs-Methode der CIM_DataFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: faa2e3ce2f2454d76ff9e55cc10cf09e9b5f715e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127121"
---
# <a name="changesecuritypermissions-method-of-the-cim_datafile-class"></a><span data-ttu-id="2da60-103">Changesecurrityberechtigungs-Methode der CIM \_ DataFile-Klasse</span><span class="sxs-lookup"><span data-stu-id="2da60-103">ChangeSecurityPermissions method of the CIM\_DataFile class</span></span>

<span data-ttu-id="2da60-104">Die **changesecurrityberechtigungs** -Methode ändert die Sicherheits Berechtigungen für die logische Datendatei, die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="2da60-104">The **ChangeSecurityPermissions** method changes the security permissions for the logical data file specified in the object path.</span></span> <span data-ttu-id="2da60-105">Wenn die logische Datei ein Verzeichnis ist, wird diese Methode rekursiv ausgeführt, und die Sicherheits Berechtigungen für alle Dateien und Unterverzeichnisse, die im Verzeichnis enthalten sind, werden geändert.</span><span class="sxs-lookup"><span data-stu-id="2da60-105">If the logical file is a directory, then this method will act recursively, changing the security permissions for all of the files and sub-directories that the directory contains.</span></span> <span data-ttu-id="2da60-106">Diese Methode wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2da60-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2da60-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="2da60-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2da60-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2da60-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2da60-109">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="2da60-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="2da60-110">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="2da60-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="2da60-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="2da60-111">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a><span data-ttu-id="2da60-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="2da60-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2da60-113">*SecurityDescriptor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2da60-113">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2da60-114">Gibt die Sicherheitsinformationen an.</span><span class="sxs-lookup"><span data-stu-id="2da60-114">Specifies the security information.</span></span>

> [!Note]  
> <span data-ttu-id="2da60-115">Eine **Zugriffs** Steuerungs Liste (Access Control List, ACL) in der [**Sicherheits \_ Deskriptor**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) -Struktur gewährt uneingeschränkten Zugriff.</span><span class="sxs-lookup"><span data-stu-id="2da60-115">A **NULL** access control list (ACL) in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure grants unlimited access.</span></span> <span data-ttu-id="2da60-116">Informationen zu den Auswirkungen des unbegrenzten Zugriffs finden Sie unter [Erstellen einer Sicherheits Beschreibung für ein neues Objekt](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span><span class="sxs-lookup"><span data-stu-id="2da60-116">For information about the implications of unlimited access, see [Creating a Security Descriptor for a New Object](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span></span>

 

</dd> <dt>

<span data-ttu-id="2da60-117">*Option* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2da60-117">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2da60-118">Zu ändernde Sicherheits Berechtigung.</span><span class="sxs-lookup"><span data-stu-id="2da60-118">Security privilege to modify.</span></span> <span data-ttu-id="2da60-119">Um z. b. den Besitzer und die DACL-Sicherheit zu ändern, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="2da60-119">For example, to change the owner and DACL security, use:</span></span>

`Option = 1 + 4`

<span data-ttu-id="2da60-120">oder</span><span class="sxs-lookup"><span data-stu-id="2da60-120">or</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="2da60-121"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Ändern \_ \_Sicherheits \_ Informationen** für den Besitzer (1)</span><span class="sxs-lookup"><span data-stu-id="2da60-121"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="2da60-122">Ändern Sie den Besitzer der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="2da60-122">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="2da60-123"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Ändern \_ Gruppen \_ Sicherheits \_ Informationen** (2)</span><span class="sxs-lookup"><span data-stu-id="2da60-123"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="2da60-124">Ändern Sie die Gruppe der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="2da60-124">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="2da60-125"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Ändern \_ DACL- \_ Sicherheits \_ Informationen** (4)</span><span class="sxs-lookup"><span data-stu-id="2da60-125"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="2da60-126">Ändern Sie die ACL der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="2da60-126">Change the ACL of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="2da60-127"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Ändern \_ SACL- \_ Sicherheits \_ Informationen** (8)</span><span class="sxs-lookup"><span data-stu-id="2da60-127"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="2da60-128">Ändern Sie die System-ACL der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="2da60-128">Change the system ACL of the logical file.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2da60-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2da60-129">Return value</span></span>

<span data-ttu-id="2da60-130">Gibt bei Erfolg den Wert 0 zurück, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="2da60-130">Returns a value of 0 on success, and any other number to indicate an error.</span></span> <span data-ttu-id="2da60-131">Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="2da60-131">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="2da60-132">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="2da60-132">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="2da60-133">**Erfolgreich**</span><span class="sxs-lookup"><span data-stu-id="2da60-133">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="2da60-134">0</span><span class="sxs-lookup"><span data-stu-id="2da60-134">0</span></span>

<span data-ttu-id="2da60-135">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="2da60-135">Success.</span></span>

</dd> <dt>

<span data-ttu-id="2da60-136">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="2da60-136">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="2da60-137">2</span><span class="sxs-lookup"><span data-stu-id="2da60-137">2</span></span>

<span data-ttu-id="2da60-138">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="2da60-138">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="2da60-139">**Nicht spezifizierter Fehler**</span><span class="sxs-lookup"><span data-stu-id="2da60-139">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="2da60-140">8</span><span class="sxs-lookup"><span data-stu-id="2da60-140">8</span></span>

<span data-ttu-id="2da60-141">Nicht spezifizierter Fehler.</span><span class="sxs-lookup"><span data-stu-id="2da60-141">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="2da60-142">**Ungültiges Objekt**</span><span class="sxs-lookup"><span data-stu-id="2da60-142">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="2da60-143">9</span><span class="sxs-lookup"><span data-stu-id="2da60-143">9</span></span>

<span data-ttu-id="2da60-144">Ungültiges Objekt.</span><span class="sxs-lookup"><span data-stu-id="2da60-144">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="2da60-145">**Objekt ist bereits vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="2da60-145">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="2da60-146">10</span><span class="sxs-lookup"><span data-stu-id="2da60-146">10</span></span>

<span data-ttu-id="2da60-147">Das Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="2da60-147">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="2da60-148">**Dateisystem nicht NTFS**</span><span class="sxs-lookup"><span data-stu-id="2da60-148">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="2da60-149">11</span><span class="sxs-lookup"><span data-stu-id="2da60-149">11</span></span>

</dd> <dt>

<span data-ttu-id="2da60-150">**Plattform nicht NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="2da60-150">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="2da60-151">12</span><span class="sxs-lookup"><span data-stu-id="2da60-151">12</span></span>

<span data-ttu-id="2da60-152">Plattform nicht Windows NT-basiert.</span><span class="sxs-lookup"><span data-stu-id="2da60-152">Platform not Windows NT-based.</span></span>

</dd> <dt>

<span data-ttu-id="2da60-153">**Laufwerk nicht identisch**</span><span class="sxs-lookup"><span data-stu-id="2da60-153">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="2da60-154">13</span><span class="sxs-lookup"><span data-stu-id="2da60-154">13</span></span>

<span data-ttu-id="2da60-155">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="2da60-155">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="2da60-156">**Verzeichnis nicht leer**</span><span class="sxs-lookup"><span data-stu-id="2da60-156">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="2da60-157">14</span><span class="sxs-lookup"><span data-stu-id="2da60-157">14</span></span>

<span data-ttu-id="2da60-158">„Verzeichnis ist nicht leer.“</span><span class="sxs-lookup"><span data-stu-id="2da60-158">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="2da60-159">**Freigabe Verletzung**</span><span class="sxs-lookup"><span data-stu-id="2da60-159">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="2da60-160">15</span><span class="sxs-lookup"><span data-stu-id="2da60-160">15</span></span>

<span data-ttu-id="2da60-161">Freigabeverletzung.</span><span class="sxs-lookup"><span data-stu-id="2da60-161">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="2da60-162">**Ungültige Startdatei**</span><span class="sxs-lookup"><span data-stu-id="2da60-162">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="2da60-163">16</span><span class="sxs-lookup"><span data-stu-id="2da60-163">16</span></span>

<span data-ttu-id="2da60-164">Ungültige Startdatei.</span><span class="sxs-lookup"><span data-stu-id="2da60-164">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="2da60-165">**Berechtigung nicht aufrechterhalten**</span><span class="sxs-lookup"><span data-stu-id="2da60-165">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="2da60-166">17</span><span class="sxs-lookup"><span data-stu-id="2da60-166">17</span></span>

<span data-ttu-id="2da60-167">Die Berechtigung wurde nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="2da60-167">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="2da60-168">**Ungültiger Parameter**</span><span class="sxs-lookup"><span data-stu-id="2da60-168">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="2da60-169">21</span><span class="sxs-lookup"><span data-stu-id="2da60-169">21</span></span>

<span data-ttu-id="2da60-170">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="2da60-170">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2da60-171">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2da60-171">Remarks</span></span>

<span data-ttu-id="2da60-172">Die **changesecurrityberechtigungs** -Methode in [**CIM \_ DataFile**](cim-datafile.md) wird von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="2da60-172">The **ChangeSecurityPermissions** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="2da60-173">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="2da60-173">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2da60-174">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="2da60-174">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2da60-175">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2da60-175">Requirements</span></span>



| <span data-ttu-id="2da60-176">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2da60-176">Requirement</span></span> | <span data-ttu-id="2da60-177">Wert</span><span class="sxs-lookup"><span data-stu-id="2da60-177">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2da60-178">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2da60-178">Minimum supported client</span></span><br/> | <span data-ttu-id="2da60-179">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2da60-179">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2da60-180">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2da60-180">Minimum supported server</span></span><br/> | <span data-ttu-id="2da60-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2da60-181">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2da60-182">Namespace</span><span class="sxs-lookup"><span data-stu-id="2da60-182">Namespace</span></span><br/>                | <span data-ttu-id="2da60-183">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="2da60-183">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2da60-184">MOF</span><span class="sxs-lookup"><span data-stu-id="2da60-184">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2da60-185"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2da60-185"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2da60-186">DLL</span><span class="sxs-lookup"><span data-stu-id="2da60-186">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2da60-187"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2da60-187"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2da60-188">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2da60-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2da60-189">**CIM- \_ Datendatei**</span><span class="sxs-lookup"><span data-stu-id="2da60-189">**CIM\_DataFile**</span></span>](changesecuritypermissions-method-in-class-cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="2da60-190">**CIM- \_ Datendatei**</span><span class="sxs-lookup"><span data-stu-id="2da60-190">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="2da60-191">WMI-Tasks: Dateien und Ordner</span><span class="sxs-lookup"><span data-stu-id="2da60-191">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="2da60-192">**Datei-und Verzeichniszugriffs Rechte-Konstanten**</span><span class="sxs-lookup"><span data-stu-id="2da60-192">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

