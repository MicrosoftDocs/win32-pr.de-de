---
description: 'ChangeSecurityPermissions-Methode der CIM_Directory-Klasse: Ändert die Sicherheitsberechtigungen für die im Objektpfad angegebene logische Verzeichniseintragsdatei.'
ms.assetid: d3caeec1-fecc-4463-9349-d82869c11927
ms.tgt_platform: multiple
title: ChangeSecurityPermissions-Methode der CIM_Directory-Klasse
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
ms.openlocfilehash: 389ed5b7b0a43981c5eeb3d66a73bd19cbd99d88
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108091068"
---
# <a name="changesecuritypermissions-method-of-the-cim_directory-class"></a><span data-ttu-id="3eac0-103">ChangeSecurityPermissions-Methode der CIM \_ Directory-Klasse</span><span class="sxs-lookup"><span data-stu-id="3eac0-103">ChangeSecurityPermissions method of the CIM\_Directory class</span></span>

<span data-ttu-id="3eac0-104">Die **ChangeSecurityPermissions-Methode** ändert die Sicherheitsberechtigungen für die im Objektpfad angegebene Logische Verzeichniseintragsdatei.</span><span class="sxs-lookup"><span data-stu-id="3eac0-104">The **ChangeSecurityPermissions** method changes the security permissions for the logical directory entry file specified in the object path.</span></span> <span data-ttu-id="3eac0-105">Wenn die logische Datei ein Verzeichnis ist, reagiert diese Methode rekursiv und ändert die Sicherheitsberechtigungen für alle Dateien und Unterverzeichnisse, die das Verzeichnis enthält.</span><span class="sxs-lookup"><span data-stu-id="3eac0-105">If the logical file is a directory, then this method will act recursively, changing the security permissions for all of the files and sub-directories that the directory contains.</span></span> <span data-ttu-id="3eac0-106">Diese Methode wird von [**CIM \_ LogicalFile**](cim-logicalfile.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3eac0-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3eac0-107">Die CIM-Klassen (Distributed Management Task Force) (DMTF (Distributed Management Task Force) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="3eac0-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3eac0-108">WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)</span><span class="sxs-lookup"><span data-stu-id="3eac0-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="3eac0-109">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="3eac0-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="3eac0-110">Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)</span><span class="sxs-lookup"><span data-stu-id="3eac0-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="3eac0-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="3eac0-111">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a><span data-ttu-id="3eac0-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="3eac0-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3eac0-113">*SecurityDescriptor* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="3eac0-113">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3eac0-114">Gibt Sicherheitsinformationen an.</span><span class="sxs-lookup"><span data-stu-id="3eac0-114">Specifies security information.</span></span>

> [!Note]  
> <span data-ttu-id="3eac0-115">Eine  NULL-Zugriffssteuerungsliste (Access Control List, ACL) in der [**SECURITY \_ DESCRIPTOR-Struktur**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) gewährt unbegrenzten Zugriff.</span><span class="sxs-lookup"><span data-stu-id="3eac0-115">A **NULL** access control list (ACL) in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure grants unlimited access.</span></span>

 

</dd> <dt>

<span data-ttu-id="3eac0-116">*Option* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="3eac0-116">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3eac0-117">Sicherheitsberechtigung zum Ändern.</span><span class="sxs-lookup"><span data-stu-id="3eac0-117">Security privilege to modify.</span></span> <span data-ttu-id="3eac0-118">Verwenden Sie beispielsweise Folgendes, um den Besitzer und die DACL-Sicherheit zu ändern:</span><span class="sxs-lookup"><span data-stu-id="3eac0-118">For example, to change the owner and DACL security, use:</span></span>

`Option = 1 + 4`

<span data-ttu-id="3eac0-119">oder</span><span class="sxs-lookup"><span data-stu-id="3eac0-119">or</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="3eac0-120"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE \_ \_ \_ BESITZERSICHERHEITSINFORMATIONEN** (1)</span><span class="sxs-lookup"><span data-stu-id="3eac0-120"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="3eac0-121">Ändern Sie den Besitzer der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="3eac0-121">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="3eac0-122"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE \_ \_ \_ GRUPPENSICHERHEITSINFORMATIONEN** (2)</span><span class="sxs-lookup"><span data-stu-id="3eac0-122"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="3eac0-123">Ändern Sie die Gruppe der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="3eac0-123">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="3eac0-124"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE \_ \_ \_ DACL-SICHERHEITSINFORMATIONEN** (4)</span><span class="sxs-lookup"><span data-stu-id="3eac0-124"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="3eac0-125">Ändern Sie die ACL der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="3eac0-125">Change the ACL of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="3eac0-126"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE \_ \_ \_ SACL-SICHERHEITSINFORMATIONEN** (8)</span><span class="sxs-lookup"><span data-stu-id="3eac0-126"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="3eac0-127">Ändern Sie die System-ACL der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="3eac0-127">Change the system ACL of the logical file.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3eac0-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3eac0-128">Return value</span></span>

<span data-ttu-id="3eac0-129">Gibt bei Erfolg den Wert 0 (null) und eine beliebige andere Zahl zurück, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="3eac0-129">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="3eac0-130">0</span><span class="sxs-lookup"><span data-stu-id="3eac0-130">0</span></span>

<span data-ttu-id="3eac0-131">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="3eac0-131">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="3eac0-132">2</span><span class="sxs-lookup"><span data-stu-id="3eac0-132">2</span></span>

<span data-ttu-id="3eac0-133">Der Zugriff wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="3eac0-133">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="3eac0-134">8</span><span class="sxs-lookup"><span data-stu-id="3eac0-134">8</span></span>

<span data-ttu-id="3eac0-135">Nicht angegebener Fehler.</span><span class="sxs-lookup"><span data-stu-id="3eac0-135">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="3eac0-136">9</span><span class="sxs-lookup"><span data-stu-id="3eac0-136">9</span></span>

<span data-ttu-id="3eac0-137">Ungültiges Objekt.</span><span class="sxs-lookup"><span data-stu-id="3eac0-137">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="3eac0-138">10</span><span class="sxs-lookup"><span data-stu-id="3eac0-138">10</span></span>

<span data-ttu-id="3eac0-139">Das Objekt ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="3eac0-139">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="3eac0-140">11</span><span class="sxs-lookup"><span data-stu-id="3eac0-140">11</span></span>

<span data-ttu-id="3eac0-141">Dateisystem, nicht NTFS.</span><span class="sxs-lookup"><span data-stu-id="3eac0-141">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="3eac0-142">12</span><span class="sxs-lookup"><span data-stu-id="3eac0-142">12</span></span>

<span data-ttu-id="3eac0-143">Plattform, nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="3eac0-143">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="3eac0-144">13</span><span class="sxs-lookup"><span data-stu-id="3eac0-144">13</span></span>

<span data-ttu-id="3eac0-145">Laufwerk nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="3eac0-145">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="3eac0-146">14</span><span class="sxs-lookup"><span data-stu-id="3eac0-146">14</span></span>

<span data-ttu-id="3eac0-147">„Verzeichnis ist nicht leer.“</span><span class="sxs-lookup"><span data-stu-id="3eac0-147">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="3eac0-148">15</span><span class="sxs-lookup"><span data-stu-id="3eac0-148">15</span></span>

<span data-ttu-id="3eac0-149">Freigabeverletzung.</span><span class="sxs-lookup"><span data-stu-id="3eac0-149">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="3eac0-150">16</span><span class="sxs-lookup"><span data-stu-id="3eac0-150">16</span></span>

<span data-ttu-id="3eac0-151">Ungültige Startdatei.</span><span class="sxs-lookup"><span data-stu-id="3eac0-151">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="3eac0-152">17</span><span class="sxs-lookup"><span data-stu-id="3eac0-152">17</span></span>

<span data-ttu-id="3eac0-153">Die Berechtigung wurde nicht gehalten.</span><span class="sxs-lookup"><span data-stu-id="3eac0-153">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="3eac0-154">21</span><span class="sxs-lookup"><span data-stu-id="3eac0-154">21</span></span>

<span data-ttu-id="3eac0-155">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="3eac0-155">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3eac0-156">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3eac0-156">Remarks</span></span>

<span data-ttu-id="3eac0-157">Diese Methode wird derzeit nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="3eac0-157">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="3eac0-158">Um diese Methode zu verwenden, müssen Sie sie in Ihrem eigenen Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="3eac0-158">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="3eac0-159">Diese Dokumentation wird von den CIM-Klassenbeschreibungen abgeleitet, die von DMTF veröffentlicht wurden.</span><span class="sxs-lookup"><span data-stu-id="3eac0-159">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="3eac0-160">Microsoft hat möglicherweise Änderungen vorgenommen, um kleinere Fehler zu beheben, die Dokumentationsstandards des Microsoft SDK zu erfüllen oder weitere Informationen zur Verfügung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="3eac0-160">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3eac0-161">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3eac0-161">Requirements</span></span>



| <span data-ttu-id="3eac0-162">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3eac0-162">Requirement</span></span> | <span data-ttu-id="3eac0-163">Wert</span><span class="sxs-lookup"><span data-stu-id="3eac0-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3eac0-164">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3eac0-164">Minimum supported client</span></span><br/> | <span data-ttu-id="3eac0-165">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3eac0-165">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3eac0-166">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3eac0-166">Minimum supported server</span></span><br/> | <span data-ttu-id="3eac0-167">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3eac0-167">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3eac0-168">Namespace</span><span class="sxs-lookup"><span data-stu-id="3eac0-168">Namespace</span></span><br/>                | <span data-ttu-id="3eac0-169">\\Stamm-CIMV2</span><span class="sxs-lookup"><span data-stu-id="3eac0-169">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3eac0-170">MOF</span><span class="sxs-lookup"><span data-stu-id="3eac0-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3eac0-171"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="3eac0-171"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3eac0-172">DLL</span><span class="sxs-lookup"><span data-stu-id="3eac0-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3eac0-173"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3eac0-173"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3eac0-174">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3eac0-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3eac0-175">\_CIM-Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="3eac0-175">CIM\_Directory</span></span>](changesecuritypermissions-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="3eac0-176">**\_CIM-Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="3eac0-176">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

