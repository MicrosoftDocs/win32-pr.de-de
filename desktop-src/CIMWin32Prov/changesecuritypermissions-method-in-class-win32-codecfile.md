---
description: Ändert die Sicherheits Berechtigungen für die im Objekt Pfad angegebene logische Codec-Datei.
ms.assetid: d7945666-e514-4bfc-81bc-8e98aa90bcf0
ms.tgt_platform: multiple
title: Changesecurrityberechtigungs-Methode der Win32_CodecFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6b0789164b2bb28b5c3c84e907cf7ae2acb96e01
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346623"
---
# <a name="changesecuritypermissions-method-of-the-win32_codecfile-class"></a><span data-ttu-id="8e227-103">Changesecurrityberechtigungs-Methode der Win32 \_ codecfile-Klasse</span><span class="sxs-lookup"><span data-stu-id="8e227-103">ChangeSecurityPermissions method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="8e227-104">Die [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode **changesecurrityberechtigungs** Änderungen ändern die Sicherheits Berechtigungen für die im Objekt Pfad angegebene logische Codec-Datei.</span><span class="sxs-lookup"><span data-stu-id="8e227-104">The **ChangeSecurityPermissions** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method changes the security permissions for the logical codec file specified in the object path.</span></span> <span data-ttu-id="8e227-105">Wenn es sich bei der logischen Datei um ein Verzeichnis handelt, ist **changesekurityberechtigungen** rekursiv und ändert die Sicherheits Berechtigungen aller Dateien und Unterverzeichnisse, die im Verzeichnis enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="8e227-105">If the logical file is a directory, then **ChangeSecurityPermissions** is recursive, and changes the security permissions of all of the files and subdirectories the directory contains.</span></span> <span data-ttu-id="8e227-106">**Changesecurrityberechtigungen** geben einen ganzzahligen Wert von 0 (null) zurück, wenn die Berechtigungen geändert werden, und eine andere Zahl, die auf einen Fehler hinweist.</span><span class="sxs-lookup"><span data-stu-id="8e227-106">**ChangeSecurityPermissions** returns an integer value of 0 (zero) if the permissions are changed, and a different number to indicate an error.</span></span>

<span data-ttu-id="8e227-107">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="8e227-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="8e227-108">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="8e227-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="8e227-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e227-109">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a><span data-ttu-id="8e227-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e227-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e227-111">*SecurityDescriptor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8e227-111">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e227-112">Ein Ausdruck, der zu einer Instanz von [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="8e227-112">Expression that resolves to an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span> <span data-ttu-id="8e227-113">Dieser Deskriptor enthält neue Sicherheits Berechtigungen für die Instanz von [**Win32 \_ codecfile**](win32-codecfile.md).</span><span class="sxs-lookup"><span data-stu-id="8e227-113">This descriptor contains new security permissions for the instance of [**Win32\_CodecFile**](win32-codecfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e227-114">*Option* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8e227-114">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e227-115">Sicherheits Berechtigung, die geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="8e227-115">Security privilege to be modified.</span></span> <span data-ttu-id="8e227-116">Wenn Sie z. b. den Besitzer und die DACL-Sicherheit (die Zugriffs Steuerungs Liste) ändern möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="8e227-116">For example, to change the owner and discretionary access control list (DACL) security, use:</span></span>

`Option = 1 + 4`

<span data-ttu-id="8e227-117">Oder</span><span class="sxs-lookup"><span data-stu-id="8e227-117">-or-</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="8e227-118"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Ändern \_ \_Sicherheits \_ Informationen** für den Besitzer (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="8e227-118"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="8e227-119">Ändern Sie den Besitzer der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="8e227-119">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="8e227-120"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Ändern \_ Gruppen \_ Sicherheits \_ Informationen** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="8e227-120"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="8e227-121">Ändern Sie die Gruppe der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="8e227-121">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="8e227-122"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Ändern \_ DACL- \_ Sicherheits \_ Informationen** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="8e227-122"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="8e227-123">Ändern Sie die freigegebene Zugriffs Steuerungs Liste (DACL) der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="8e227-123">Change the discretionary access control list (DACL) of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="8e227-124"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Ändern \_ SACL- \_ Sicherheits \_ Informationen** (8 (0x8))</span><span class="sxs-lookup"><span data-stu-id="8e227-124"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="8e227-125">Ändern Sie die System Zugriffs Steuerungs Liste (SACL) der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="8e227-125">Change the system access control list (SACL) of the logical file.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e227-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8e227-126">Return value</span></span>

<span data-ttu-id="8e227-127">Gibt einen Wert von 0 (null) zurück, wenn die Berechtigungen geändert werden, und eine andere Zahl, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="8e227-127">Returns an value of 0 (zero) if the permissions are changed, and a different number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="8e227-128">**Erfolgreich**</span><span class="sxs-lookup"><span data-stu-id="8e227-128">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="8e227-129">0</span><span class="sxs-lookup"><span data-stu-id="8e227-129">0</span></span>

<span data-ttu-id="8e227-130">Die Anforderung ist erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="8e227-130">The request is successful.</span></span>

</dd> <dt>

<span data-ttu-id="8e227-131">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="8e227-131">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="8e227-132">2</span><span class="sxs-lookup"><span data-stu-id="8e227-132">2</span></span>

<span data-ttu-id="8e227-133">Zugriff verweigert.“</span><span class="sxs-lookup"><span data-stu-id="8e227-133">Access is denied.</span></span>

</dd> <dt>

<span data-ttu-id="8e227-134">**Nicht spezifizierter Fehler**</span><span class="sxs-lookup"><span data-stu-id="8e227-134">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="8e227-135">8</span><span class="sxs-lookup"><span data-stu-id="8e227-135">8</span></span>

<span data-ttu-id="8e227-136">Ein nicht angegebener Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="8e227-136">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="8e227-137">**Ungültiges Objekt**</span><span class="sxs-lookup"><span data-stu-id="8e227-137">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="8e227-138">9</span><span class="sxs-lookup"><span data-stu-id="8e227-138">9</span></span>

<span data-ttu-id="8e227-139">Der angegebene Name ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="8e227-139">The specified name is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="8e227-140">**Objekt ist bereits vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="8e227-140">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="8e227-141">10</span><span class="sxs-lookup"><span data-stu-id="8e227-141">10</span></span>

<span data-ttu-id="8e227-142">Das Objekt "" ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8e227-142">The specified object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="8e227-143">**Dateisystem nicht NTFS**</span><span class="sxs-lookup"><span data-stu-id="8e227-143">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="8e227-144">11</span><span class="sxs-lookup"><span data-stu-id="8e227-144">11</span></span>

<span data-ttu-id="8e227-145">Das Dateisystem ist kein NTFS-Dateisystem.</span><span class="sxs-lookup"><span data-stu-id="8e227-145">The file system is not an NTFS file system.</span></span>

</dd> <dt>

<span data-ttu-id="8e227-146">**Plattform nicht NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="8e227-146">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="8e227-147">12</span><span class="sxs-lookup"><span data-stu-id="8e227-147">12</span></span>

<span data-ttu-id="8e227-148">Die Plattform ist nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="8e227-148">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="8e227-149">**Laufwerk nicht identisch**</span><span class="sxs-lookup"><span data-stu-id="8e227-149">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="8e227-150">13</span><span class="sxs-lookup"><span data-stu-id="8e227-150">13</span></span>

<span data-ttu-id="8e227-151">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="8e227-151">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="8e227-152">**Verzeichnis nicht leer**</span><span class="sxs-lookup"><span data-stu-id="8e227-152">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="8e227-153">14</span><span class="sxs-lookup"><span data-stu-id="8e227-153">14</span></span>

<span data-ttu-id="8e227-154">Das Verzeichnis ist nicht leer.</span><span class="sxs-lookup"><span data-stu-id="8e227-154">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="8e227-155">**Freigabe Verletzung**</span><span class="sxs-lookup"><span data-stu-id="8e227-155">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="8e227-156">15</span><span class="sxs-lookup"><span data-stu-id="8e227-156">15</span></span>

<span data-ttu-id="8e227-157">Eine Freigabe Verletzung ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="8e227-157">There is a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="8e227-158">**Ungültige Startdatei**</span><span class="sxs-lookup"><span data-stu-id="8e227-158">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="8e227-159">16</span><span class="sxs-lookup"><span data-stu-id="8e227-159">16</span></span>

<span data-ttu-id="8e227-160">Die angegebene Startdatei ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="8e227-160">The specified start file is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="8e227-161">**Berechtigung nicht aufrechterhalten**</span><span class="sxs-lookup"><span data-stu-id="8e227-161">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="8e227-162">17</span><span class="sxs-lookup"><span data-stu-id="8e227-162">17</span></span>

<span data-ttu-id="8e227-163">Eine für den Vorgang erforderliche Berechtigung wird nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="8e227-163">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="8e227-164">**Ungültiger Parameter**</span><span class="sxs-lookup"><span data-stu-id="8e227-164">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="8e227-165">21</span><span class="sxs-lookup"><span data-stu-id="8e227-165">21</span></span>

<span data-ttu-id="8e227-166">Ein angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="8e227-166">A specified parameter is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8e227-167">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8e227-167">Requirements</span></span>



| <span data-ttu-id="8e227-168">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8e227-168">Requirement</span></span> | <span data-ttu-id="8e227-169">Wert</span><span class="sxs-lookup"><span data-stu-id="8e227-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e227-170">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8e227-170">Minimum supported client</span></span><br/> | <span data-ttu-id="8e227-171">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8e227-171">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8e227-172">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8e227-172">Minimum supported server</span></span><br/> | <span data-ttu-id="8e227-173">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8e227-173">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8e227-174">Namespace</span><span class="sxs-lookup"><span data-stu-id="8e227-174">Namespace</span></span><br/>                | <span data-ttu-id="8e227-175">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8e227-175">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8e227-176">MOF</span><span class="sxs-lookup"><span data-stu-id="8e227-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8e227-177"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8e227-177"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8e227-178">DLL</span><span class="sxs-lookup"><span data-stu-id="8e227-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e227-179"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e227-179"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e227-180">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8e227-180">See also</span></span>

<dl> <dt>

<span data-ttu-id="8e227-181">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8e227-181">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="8e227-182">**Win32- \_ codecfile**</span><span class="sxs-lookup"><span data-stu-id="8e227-182">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

