---
description: 'ChangeSecurityPermissions-Methode der Win32_Directory-Klasse: Ändert die Sicherheitsberechtigungen für die im Objektpfad angegebene logische Verzeichniseintragsdatei.'
ms.assetid: de2b3269-61e0-484c-8bea-00578422491f
ms.tgt_platform: multiple
title: ChangeSecurityPermissions-Methode der Win32_Directory-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 98c6026497496ab758c71a8a0403557ad2cacc7f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108091058"
---
# <a name="changesecuritypermissions-method-of-the-win32_directory-class"></a><span data-ttu-id="14071-103">ChangeSecurityPermissions-Methode der Win32 \_ Directory-Klasse</span><span class="sxs-lookup"><span data-stu-id="14071-103">ChangeSecurityPermissions method of the Win32\_Directory class</span></span>

<span data-ttu-id="14071-104">Die **WMI-Klassenmethode ChangeSecurityPermissions** ändert die Sicherheitsberechtigungen für die im Objektpfad angegebene logische Verzeichniseintragsdatei.</span><span class="sxs-lookup"><span data-stu-id="14071-104">The **ChangeSecurityPermissions WMI class** method changes the security permissions for the logical directory entry file specified in the object path.</span></span> <span data-ttu-id="14071-105">Wenn die logische Datei ein Verzeichnis ist, ist **ChangeSecurityPermissions** rekursiv und ändert die Sicherheitsberechtigungen aller Dateien und Unterverzeichnisse, die das Verzeichnis enthält.</span><span class="sxs-lookup"><span data-stu-id="14071-105">If the logical file is a directory, then **ChangeSecurityPermissions** is recursive, and changes the security permissions of all of the files and subdirectories that the directory contains.</span></span> <span data-ttu-id="14071-106">Die **ChangeSecurityPermissions-Klasse** gibt einen ganzzahligen Wert von 0 (null) zurück, wenn die Berechtigungen geändert werden, und eine andere Zahl, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="14071-106">The **ChangeSecurityPermissions** class returns an integer value of 0 (zero) if the permissions are changed, and a different number to indicate an error.</span></span>

<span data-ttu-id="14071-107">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="14071-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="14071-108">Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)</span><span class="sxs-lookup"><span data-stu-id="14071-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="14071-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="14071-109">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a><span data-ttu-id="14071-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="14071-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14071-111">*SecurityDescriptor* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="14071-111">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14071-112">Ausdruck, der in eine Instanz von [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="14071-112">Expression that resolves to an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span> <span data-ttu-id="14071-113">Dieser Deskriptor enthält neue Sicherheitsberechtigungen für die Instanz von [**Win32 \_ PageFile**](win32-pagefile.md).</span><span class="sxs-lookup"><span data-stu-id="14071-113">This descriptor contains new security permissions for the instance of [**Win32\_PageFile**](win32-pagefile.md).</span></span>

</dd> <dt>

<span data-ttu-id="14071-114">*Option* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="14071-114">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14071-115">Zu ändernde Sicherheitsberechtigungen.</span><span class="sxs-lookup"><span data-stu-id="14071-115">Security privilege to be modified.</span></span> <span data-ttu-id="14071-116">Verwenden Sie beispielsweise Folgendes, um die Sicherheit der Besitzer- und der Dacl-Zugriffssteuerungsliste (Discretionary Access Control List, DACL) zu ändern:</span><span class="sxs-lookup"><span data-stu-id="14071-116">For example, to change the owner and discretionary access control list (DACL) security, use:</span></span>

`Option = 1 + 4`

<span data-ttu-id="14071-117">Oder</span><span class="sxs-lookup"><span data-stu-id="14071-117">-or-</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="14071-118"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE \_ \_ \_ BESITZERSICHERHEITSINFORMATIONEN** (1)</span><span class="sxs-lookup"><span data-stu-id="14071-118"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="14071-119">Ändern Sie den Besitzer der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="14071-119">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="14071-120"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE \_ \_ \_ GRUPPENSICHERHEITSINFORMATIONEN** (2)</span><span class="sxs-lookup"><span data-stu-id="14071-120"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="14071-121">Ändern Sie die Gruppe der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="14071-121">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="14071-122"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE \_ \_DACL-SICHERHEITSINFORMATIONEN \_** (4)</span><span class="sxs-lookup"><span data-stu-id="14071-122"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="14071-123">Ändern Sie die DACL der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="14071-123">Change the discretionary DACL of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="14071-124"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE \_ \_SACL-SICHERHEITSINFORMATIONEN \_** (8)</span><span class="sxs-lookup"><span data-stu-id="14071-124"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="14071-125">Ändern Sie die Systemzugriffssteuerungsliste (SACL) der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="14071-125">Change the system access control list (SACL) of the logical file.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14071-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="14071-126">Return value</span></span>

<span data-ttu-id="14071-127">Gibt den Wert 0 (null) zurück, wenn die Berechtigungen geändert werden, und eine andere Zahl, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="14071-127">Returns a value of 0 (zero) if the permissions are changed, and a different number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="14071-128">**Erfolgreich**</span><span class="sxs-lookup"><span data-stu-id="14071-128">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="14071-129">0</span><span class="sxs-lookup"><span data-stu-id="14071-129">0</span></span>

<span data-ttu-id="14071-130">Die Anforderung ist erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="14071-130">The request is successful.</span></span>

</dd> <dt>

<span data-ttu-id="14071-131">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="14071-131">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="14071-132">2</span><span class="sxs-lookup"><span data-stu-id="14071-132">2</span></span>

<span data-ttu-id="14071-133">Der Zugriff wird verweigert.</span><span class="sxs-lookup"><span data-stu-id="14071-133">Access is denied.</span></span>

</dd> <dt>

<span data-ttu-id="14071-134">**Nicht angegebener Fehler**</span><span class="sxs-lookup"><span data-stu-id="14071-134">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="14071-135">8</span><span class="sxs-lookup"><span data-stu-id="14071-135">8</span></span>

<span data-ttu-id="14071-136">Es ist ein nicht angegebener Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="14071-136">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="14071-137">**Ungültiges Objekt**</span><span class="sxs-lookup"><span data-stu-id="14071-137">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="14071-138">9</span><span class="sxs-lookup"><span data-stu-id="14071-138">9</span></span>

<span data-ttu-id="14071-139">Der angegebene Name ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="14071-139">The specified name is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="14071-140">**Objekt ist bereits vorhanden**</span><span class="sxs-lookup"><span data-stu-id="14071-140">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="14071-141">10</span><span class="sxs-lookup"><span data-stu-id="14071-141">10</span></span>

<span data-ttu-id="14071-142">Das Objekt "" ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="14071-142">The specified object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="14071-143">**Dateisystem nicht NTFS**</span><span class="sxs-lookup"><span data-stu-id="14071-143">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="14071-144">11</span><span class="sxs-lookup"><span data-stu-id="14071-144">11</span></span>

<span data-ttu-id="14071-145">Das Dateisystem ist kein NTFS-Dateisystem.</span><span class="sxs-lookup"><span data-stu-id="14071-145">The file system is not an NTFS file system.</span></span>

</dd> <dt>

<span data-ttu-id="14071-146">**Plattform nicht NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="14071-146">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="14071-147">12</span><span class="sxs-lookup"><span data-stu-id="14071-147">12</span></span>

<span data-ttu-id="14071-148">Die Plattform ist nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="14071-148">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="14071-149">**Laufwerk nicht identisch**</span><span class="sxs-lookup"><span data-stu-id="14071-149">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="14071-150">13</span><span class="sxs-lookup"><span data-stu-id="14071-150">13</span></span>

<span data-ttu-id="14071-151">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="14071-151">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="14071-152">**Verzeichnis nicht leer**</span><span class="sxs-lookup"><span data-stu-id="14071-152">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="14071-153">14</span><span class="sxs-lookup"><span data-stu-id="14071-153">14</span></span>

<span data-ttu-id="14071-154">Das Verzeichnis ist nicht leer.</span><span class="sxs-lookup"><span data-stu-id="14071-154">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="14071-155">**Verletzung der Freigabe**</span><span class="sxs-lookup"><span data-stu-id="14071-155">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="14071-156">15</span><span class="sxs-lookup"><span data-stu-id="14071-156">15</span></span>

<span data-ttu-id="14071-157">Es liegt ein Freigabeverstoß vor.</span><span class="sxs-lookup"><span data-stu-id="14071-157">There is a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="14071-158">**Ungültige Startdatei**</span><span class="sxs-lookup"><span data-stu-id="14071-158">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="14071-159">16</span><span class="sxs-lookup"><span data-stu-id="14071-159">16</span></span>

<span data-ttu-id="14071-160">Die angegebene Startdatei ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="14071-160">The specified start file is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="14071-161">**Nicht privileg**</span><span class="sxs-lookup"><span data-stu-id="14071-161">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="14071-162">17</span><span class="sxs-lookup"><span data-stu-id="14071-162">17</span></span>

<span data-ttu-id="14071-163">Für den Vorgang ist keine Berechtigung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="14071-163">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="14071-164">**Ungültiger Parameter**</span><span class="sxs-lookup"><span data-stu-id="14071-164">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="14071-165">21</span><span class="sxs-lookup"><span data-stu-id="14071-165">21</span></span>

<span data-ttu-id="14071-166">Ein angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="14071-166">A specified parameter is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="14071-167">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="14071-167">Requirements</span></span>



| <span data-ttu-id="14071-168">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="14071-168">Requirement</span></span> | <span data-ttu-id="14071-169">Wert</span><span class="sxs-lookup"><span data-stu-id="14071-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="14071-170">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="14071-170">Minimum supported client</span></span><br/> | <span data-ttu-id="14071-171">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="14071-171">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="14071-172">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="14071-172">Minimum supported server</span></span><br/> | <span data-ttu-id="14071-173">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="14071-173">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="14071-174">Namespace</span><span class="sxs-lookup"><span data-stu-id="14071-174">Namespace</span></span><br/>                | <span data-ttu-id="14071-175">\\Stamm-CIMV2</span><span class="sxs-lookup"><span data-stu-id="14071-175">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="14071-176">MOF</span><span class="sxs-lookup"><span data-stu-id="14071-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="14071-177"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="14071-177"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="14071-178">DLL</span><span class="sxs-lookup"><span data-stu-id="14071-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14071-179"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14071-179"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14071-180">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="14071-180">See also</span></span>

<dl> <dt>

<span data-ttu-id="14071-181">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="14071-181">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="14071-182">**Win32-Verzeichnis \_**</span><span class="sxs-lookup"><span data-stu-id="14071-182">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

