---
description: Ändert die Sicherheits Berechtigungen für die im Objekt Pfad angegebene logische Verknüpfungs Datei.
ms.assetid: abd5aec8-4684-4b8d-8fdf-d3a7a5eec103
ms.tgt_platform: multiple
title: Changesecurrityberechtigungs-Methode der Win32_ShortcutFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ad2d482e0be93a1abec80fc710a1a43d7873dd99
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483502"
---
# <a name="changesecuritypermissions-method-of-the-win32_shortcutfile-class"></a><span data-ttu-id="0f8a1-103">Changesecurrityberechtigungs-Methode der Win32 \_ shortcutfile-Klasse</span><span class="sxs-lookup"><span data-stu-id="0f8a1-103">ChangeSecurityPermissions method of the Win32\_ShortcutFile class</span></span>

<span data-ttu-id="0f8a1-104">Die [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode **changesecurrityberechtigungs** Änderungen ändern die Sicherheits Berechtigungen für die logische Kurzform, die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="0f8a1-104">The **ChangeSecurityPermissions** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method changes the security permissions for the logical shortcut file specified in the object path.</span></span> <span data-ttu-id="0f8a1-105">Wenn es sich bei der logischen Datei um ein Verzeichnis handelt, ist **changesekurityberechtigungen** rekursiv und ändert die Sicherheits Berechtigungen aller Dateien und Unterverzeichnisse, die im Verzeichnis enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="0f8a1-105">If the logical file is a directory, then **ChangeSecurityPermissions** is recursive, and changes the security permissions of all of the files and subdirectories that the directory contains.</span></span> <span data-ttu-id="0f8a1-106">**Changesecurrityberechtigungen** geben einen ganzzahligen Wert von 0 (null) zurück, wenn die Berechtigungen geändert werden, und eine andere Zahl, die auf einen Fehler hinweist.</span><span class="sxs-lookup"><span data-stu-id="0f8a1-106">**ChangeSecurityPermissions** returns an integer value of 0 (zero) if the permissions are changed, and a different number to indicate an error.</span></span>

<span data-ttu-id="0f8a1-107">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="0f8a1-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="0f8a1-108">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="0f8a1-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="0f8a1-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f8a1-109">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a><span data-ttu-id="0f8a1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0f8a1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f8a1-111">*SecurityDescriptor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0f8a1-111">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f8a1-112">Ein Ausdruck, der zu einer Instanz von [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="0f8a1-112">Expression that resolves to an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span> <span data-ttu-id="0f8a1-113">Dieser Deskriptor enthält neue Sicherheits Berechtigungen für die Instanz von [**Win32 \_ Page File**](win32-pagefile.md).</span><span class="sxs-lookup"><span data-stu-id="0f8a1-113">This descriptor contains new security permissions for the instance of [**Win32\_PageFile**](win32-pagefile.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f8a1-114">*Option* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0f8a1-114">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f8a1-115">Die tatsächliche Sicherheits Berechtigung, die geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="0f8a1-115">Actual security privilege to be modified.</span></span> <span data-ttu-id="0f8a1-116">Um z. b. den Besitzer und die DACL-Sicherheit zu ändern, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="0f8a1-116">For example, to change the owner and DACL security, use:</span></span>

`Option = 1 + 4`

<span data-ttu-id="0f8a1-117">oder</span><span class="sxs-lookup"><span data-stu-id="0f8a1-117">or</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="0f8a1-118"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Ändern \_ \_Sicherheits \_ Informationen** für den Besitzer (1)</span><span class="sxs-lookup"><span data-stu-id="0f8a1-118"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="0f8a1-119">Ändern Sie den Besitzer der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="0f8a1-119">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="0f8a1-120"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Ändern \_ Gruppen \_ Sicherheits \_ Informationen** (2)</span><span class="sxs-lookup"><span data-stu-id="0f8a1-120"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="0f8a1-121">Ändern Sie die Gruppe der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="0f8a1-121">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="0f8a1-122"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Ändern \_ DACL- \_ Sicherheits \_ Informationen** (4)</span><span class="sxs-lookup"><span data-stu-id="0f8a1-122"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="0f8a1-123">Ändern Sie die freigegebene Zugriffs Steuerungs Liste (DACL) der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="0f8a1-123">Change the discretionary access control list (DACL) of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="0f8a1-124"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Ändern \_ SACL- \_ Sicherheits \_ Informationen** (8)</span><span class="sxs-lookup"><span data-stu-id="0f8a1-124"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="0f8a1-125">Ändern Sie die System Zugriffs Steuerungs Liste (SACL) der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="0f8a1-125">Change the system access control list (SACL) of the logical file.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f8a1-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0f8a1-126">Return value</span></span>

<span data-ttu-id="0f8a1-127">Gibt den Wert 0 (null) zurück, wenn die Berechtigungen geändert werden, und eine andere Zahl, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="0f8a1-127">Returns a value of 0 (zero) if the permissions are changed, and a different number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="0f8a1-128">**Erfolgreich**</span><span class="sxs-lookup"><span data-stu-id="0f8a1-128">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="0f8a1-129">0</span><span class="sxs-lookup"><span data-stu-id="0f8a1-129">0</span></span>

<span data-ttu-id="0f8a1-130">Die Anforderung ist erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="0f8a1-130">The request is successful.</span></span>

</dd> <dt>

<span data-ttu-id="0f8a1-131">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="0f8a1-131">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="0f8a1-132">2</span><span class="sxs-lookup"><span data-stu-id="0f8a1-132">2</span></span>

<span data-ttu-id="0f8a1-133">Zugriff verweigert.“</span><span class="sxs-lookup"><span data-stu-id="0f8a1-133">Access is denied.</span></span>

</dd> <dt>

<span data-ttu-id="0f8a1-134">**Nicht spezifizierter Fehler**</span><span class="sxs-lookup"><span data-stu-id="0f8a1-134">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="0f8a1-135">8</span><span class="sxs-lookup"><span data-stu-id="0f8a1-135">8</span></span>

<span data-ttu-id="0f8a1-136">Ein nicht angegebener Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="0f8a1-136">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="0f8a1-137">**Ungültiges Objekt**</span><span class="sxs-lookup"><span data-stu-id="0f8a1-137">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="0f8a1-138">9</span><span class="sxs-lookup"><span data-stu-id="0f8a1-138">9</span></span>

<span data-ttu-id="0f8a1-139">Der angegebene Name ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="0f8a1-139">The specified name is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="0f8a1-140">**Objekt ist bereits vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="0f8a1-140">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="0f8a1-141">10</span><span class="sxs-lookup"><span data-stu-id="0f8a1-141">10</span></span>

<span data-ttu-id="0f8a1-142">Das Objekt "" ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="0f8a1-142">The specified object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="0f8a1-143">**Dateisystem nicht NTFS**</span><span class="sxs-lookup"><span data-stu-id="0f8a1-143">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="0f8a1-144">11</span><span class="sxs-lookup"><span data-stu-id="0f8a1-144">11</span></span>

<span data-ttu-id="0f8a1-145">Das Dateisystem ist kein NTFS-Dateisystem.</span><span class="sxs-lookup"><span data-stu-id="0f8a1-145">The file system is not an NTFS file system.</span></span>

</dd> <dt>

<span data-ttu-id="0f8a1-146">**Plattform nicht NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="0f8a1-146">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="0f8a1-147">12</span><span class="sxs-lookup"><span data-stu-id="0f8a1-147">12</span></span>

<span data-ttu-id="0f8a1-148">Die Plattform ist nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="0f8a1-148">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="0f8a1-149">**Laufwerk nicht identisch**</span><span class="sxs-lookup"><span data-stu-id="0f8a1-149">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="0f8a1-150">13</span><span class="sxs-lookup"><span data-stu-id="0f8a1-150">13</span></span>

<span data-ttu-id="0f8a1-151">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="0f8a1-151">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="0f8a1-152">**Verzeichnis nicht leer**</span><span class="sxs-lookup"><span data-stu-id="0f8a1-152">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="0f8a1-153">14</span><span class="sxs-lookup"><span data-stu-id="0f8a1-153">14</span></span>

<span data-ttu-id="0f8a1-154">Das Verzeichnis ist nicht leer.</span><span class="sxs-lookup"><span data-stu-id="0f8a1-154">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="0f8a1-155">**Freigabe Verletzung**</span><span class="sxs-lookup"><span data-stu-id="0f8a1-155">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="0f8a1-156">15</span><span class="sxs-lookup"><span data-stu-id="0f8a1-156">15</span></span>

<span data-ttu-id="0f8a1-157">Eine Freigabe Verletzung ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="0f8a1-157">There is a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="0f8a1-158">**Ungültige Startdatei**</span><span class="sxs-lookup"><span data-stu-id="0f8a1-158">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="0f8a1-159">16</span><span class="sxs-lookup"><span data-stu-id="0f8a1-159">16</span></span>

<span data-ttu-id="0f8a1-160">Die angegebene Startdatei ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="0f8a1-160">The specified start file is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="0f8a1-161">**Berechtigung nicht aufrechterhalten**</span><span class="sxs-lookup"><span data-stu-id="0f8a1-161">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="0f8a1-162">17</span><span class="sxs-lookup"><span data-stu-id="0f8a1-162">17</span></span>

<span data-ttu-id="0f8a1-163">Eine für den Vorgang erforderliche Berechtigung wird nicht aufrechterhalten.</span><span class="sxs-lookup"><span data-stu-id="0f8a1-163">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="0f8a1-164">**Ungültiger Parameter**</span><span class="sxs-lookup"><span data-stu-id="0f8a1-164">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="0f8a1-165">21</span><span class="sxs-lookup"><span data-stu-id="0f8a1-165">21</span></span>

<span data-ttu-id="0f8a1-166">Ein angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="0f8a1-166">A specified parameter is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0f8a1-167">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0f8a1-167">Requirements</span></span>



| <span data-ttu-id="0f8a1-168">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0f8a1-168">Requirement</span></span> | <span data-ttu-id="0f8a1-169">Wert</span><span class="sxs-lookup"><span data-stu-id="0f8a1-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0f8a1-170">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0f8a1-170">Minimum supported client</span></span><br/> | <span data-ttu-id="0f8a1-171">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0f8a1-171">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0f8a1-172">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0f8a1-172">Minimum supported server</span></span><br/> | <span data-ttu-id="0f8a1-173">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0f8a1-173">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0f8a1-174">Namespace</span><span class="sxs-lookup"><span data-stu-id="0f8a1-174">Namespace</span></span><br/>                | <span data-ttu-id="0f8a1-175">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0f8a1-175">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0f8a1-176">MOF</span><span class="sxs-lookup"><span data-stu-id="0f8a1-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0f8a1-177"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0f8a1-177"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0f8a1-178">DLL</span><span class="sxs-lookup"><span data-stu-id="0f8a1-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f8a1-179"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f8a1-179"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f8a1-180">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0f8a1-180">See also</span></span>

<dl> <dt>

<span data-ttu-id="0f8a1-181">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0f8a1-181">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="0f8a1-182">**Win32- \_ shortcutfile**</span><span class="sxs-lookup"><span data-stu-id="0f8a1-182">**Win32\_ShortcutFile**</span></span>](win32-shortcutfile.md)
</dt> </dl>

 

