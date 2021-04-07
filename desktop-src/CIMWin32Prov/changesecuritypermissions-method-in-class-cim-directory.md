---
description: Ändert die Sicherheits Berechtigungen für die im Objekt Pfad angegebene Datei für den logischen Verzeichniseintrag.
ms.assetid: d3caeec1-fecc-4463-9349-d82869c11927
ms.tgt_platform: multiple
title: Changesecurrityberechtigungs-Methode der CIM_Directory-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2bf767dc45907a90354b2c00fb30c6b31ce6d09a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748625"
---
# <a name="changesecuritypermissions-method-of-the-cim_directory-class"></a><span data-ttu-id="7b907-103">Changesecurrityberechtigungs-Methode der CIM- \_ Verzeichnis Klasse</span><span class="sxs-lookup"><span data-stu-id="7b907-103">ChangeSecurityPermissions method of the CIM\_Directory class</span></span>

<span data-ttu-id="7b907-104">Die **changesecurrityberechtigungs** -Methode ändert die Sicherheits Berechtigungen für die im Objekt Pfad angegebene Datei für den logischen Verzeichniseintrag.</span><span class="sxs-lookup"><span data-stu-id="7b907-104">The **ChangeSecurityPermissions** method changes the security permissions for the logical directory entry file specified in the object path.</span></span> <span data-ttu-id="7b907-105">Wenn die logische Datei ein Verzeichnis ist, wird diese Methode rekursiv ausgeführt, und die Sicherheits Berechtigungen für alle Dateien und Unterverzeichnisse, die im Verzeichnis enthalten sind, werden geändert.</span><span class="sxs-lookup"><span data-stu-id="7b907-105">If the logical file is a directory, then this method will act recursively, changing the security permissions for all of the files and sub-directories that the directory contains.</span></span> <span data-ttu-id="7b907-106">Diese Methode wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7b907-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7b907-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="7b907-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="7b907-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="7b907-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="7b907-109">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="7b907-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="7b907-110">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="7b907-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="7b907-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b907-111">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a><span data-ttu-id="7b907-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="7b907-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b907-113">*SecurityDescriptor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7b907-113">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b907-114">Gibt Sicherheitsinformationen an.</span><span class="sxs-lookup"><span data-stu-id="7b907-114">Specifies security information.</span></span>

> [!Note]  
> <span data-ttu-id="7b907-115">Eine **Zugriffs** Steuerungs Liste (Access Control List, ACL) in der [**Sicherheits \_ Deskriptor**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) -Struktur gewährt uneingeschränkten Zugriff.</span><span class="sxs-lookup"><span data-stu-id="7b907-115">A **NULL** access control list (ACL) in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure grants unlimited access.</span></span>

 

</dd> <dt>

<span data-ttu-id="7b907-116">*Option* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7b907-116">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b907-117">Zu ändernde Sicherheits Berechtigung.</span><span class="sxs-lookup"><span data-stu-id="7b907-117">Security privilege to modify.</span></span> <span data-ttu-id="7b907-118">Um z. b. den Besitzer und die DACL-Sicherheit zu ändern, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="7b907-118">For example, to change the owner and DACL security, use:</span></span>

`Option = 1 + 4`

<span data-ttu-id="7b907-119">oder</span><span class="sxs-lookup"><span data-stu-id="7b907-119">or</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="7b907-120"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Ändern \_ \_Sicherheits \_ Informationen** für den Besitzer (1)</span><span class="sxs-lookup"><span data-stu-id="7b907-120"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="7b907-121">Ändern Sie den Besitzer der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="7b907-121">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="7b907-122"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Ändern \_ Gruppen \_ Sicherheits \_ Informationen** (2)</span><span class="sxs-lookup"><span data-stu-id="7b907-122"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="7b907-123">Ändern Sie die Gruppe der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="7b907-123">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="7b907-124"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Ändern \_ DACL- \_ Sicherheits \_ Informationen** (4)</span><span class="sxs-lookup"><span data-stu-id="7b907-124"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="7b907-125">Ändern Sie die ACL der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="7b907-125">Change the ACL of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="7b907-126"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Ändern \_ SACL- \_ Sicherheits \_ Informationen** (8)</span><span class="sxs-lookup"><span data-stu-id="7b907-126"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="7b907-127">Ändern Sie die System-ACL der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="7b907-127">Change the system ACL of the logical file.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b907-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7b907-128">Return value</span></span>

<span data-ttu-id="7b907-129">Gibt bei Erfolg den Wert 0 (null) zurück, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="7b907-129">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="7b907-130">0</span><span class="sxs-lookup"><span data-stu-id="7b907-130">0</span></span>

<span data-ttu-id="7b907-131">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="7b907-131">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="7b907-132">2</span><span class="sxs-lookup"><span data-stu-id="7b907-132">2</span></span>

<span data-ttu-id="7b907-133">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="7b907-133">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="7b907-134">8</span><span class="sxs-lookup"><span data-stu-id="7b907-134">8</span></span>

<span data-ttu-id="7b907-135">Nicht spezifizierter Fehler.</span><span class="sxs-lookup"><span data-stu-id="7b907-135">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="7b907-136">9</span><span class="sxs-lookup"><span data-stu-id="7b907-136">9</span></span>

<span data-ttu-id="7b907-137">Ungültiges Objekt.</span><span class="sxs-lookup"><span data-stu-id="7b907-137">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="7b907-138">10</span><span class="sxs-lookup"><span data-stu-id="7b907-138">10</span></span>

<span data-ttu-id="7b907-139">Das Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="7b907-139">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="7b907-140">11</span><span class="sxs-lookup"><span data-stu-id="7b907-140">11</span></span>

<span data-ttu-id="7b907-141">Das Dateisystem ist nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="7b907-141">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="7b907-142">12</span><span class="sxs-lookup"><span data-stu-id="7b907-142">12</span></span>

<span data-ttu-id="7b907-143">Plattform nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="7b907-143">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="7b907-144">13</span><span class="sxs-lookup"><span data-stu-id="7b907-144">13</span></span>

<span data-ttu-id="7b907-145">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="7b907-145">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="7b907-146">14</span><span class="sxs-lookup"><span data-stu-id="7b907-146">14</span></span>

<span data-ttu-id="7b907-147">„Verzeichnis ist nicht leer.“</span><span class="sxs-lookup"><span data-stu-id="7b907-147">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="7b907-148">15</span><span class="sxs-lookup"><span data-stu-id="7b907-148">15</span></span>

<span data-ttu-id="7b907-149">Freigabeverletzung.</span><span class="sxs-lookup"><span data-stu-id="7b907-149">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="7b907-150">16</span><span class="sxs-lookup"><span data-stu-id="7b907-150">16</span></span>

<span data-ttu-id="7b907-151">Ungültige Startdatei.</span><span class="sxs-lookup"><span data-stu-id="7b907-151">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="7b907-152">17</span><span class="sxs-lookup"><span data-stu-id="7b907-152">17</span></span>

<span data-ttu-id="7b907-153">Die Berechtigung wurde nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="7b907-153">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="7b907-154">21</span><span class="sxs-lookup"><span data-stu-id="7b907-154">21</span></span>

<span data-ttu-id="7b907-155">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="7b907-155">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7b907-156">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7b907-156">Remarks</span></span>

<span data-ttu-id="7b907-157">Diese Methode wird zurzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="7b907-157">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="7b907-158">Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="7b907-158">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="7b907-159">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="7b907-159">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="7b907-160">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="7b907-160">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b907-161">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7b907-161">Requirements</span></span>



| <span data-ttu-id="7b907-162">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7b907-162">Requirement</span></span> | <span data-ttu-id="7b907-163">Wert</span><span class="sxs-lookup"><span data-stu-id="7b907-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b907-164">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7b907-164">Minimum supported client</span></span><br/> | <span data-ttu-id="7b907-165">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7b907-165">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7b907-166">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7b907-166">Minimum supported server</span></span><br/> | <span data-ttu-id="7b907-167">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7b907-167">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7b907-168">Namespace</span><span class="sxs-lookup"><span data-stu-id="7b907-168">Namespace</span></span><br/>                | <span data-ttu-id="7b907-169">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7b907-169">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7b907-170">MOF</span><span class="sxs-lookup"><span data-stu-id="7b907-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7b907-171"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7b907-171"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7b907-172">DLL</span><span class="sxs-lookup"><span data-stu-id="7b907-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b907-173"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b907-173"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b907-174">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7b907-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b907-175">CIM- \_ Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="7b907-175">CIM\_Directory</span></span>](changesecuritypermissions-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="7b907-176">**CIM- \_ Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="7b907-176">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

