---
description: Ändert die Sicherheits Berechtigungen für die logische Auslagerungs Datei, die im Objekt Pfad angegeben ist.
ms.assetid: 3abdfa1d-49d8-4676-b7a5-3be528938ec4
ms.tgt_platform: multiple
title: Changesecurrityberechtigungs-Methode der Win32_PageFile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: cc30d8780f7c0573b9a63ff83f16ad46b9d2a70f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958440"
---
# <a name="changesecuritypermissions-method-of-the-win32_pagefile-class"></a><span data-ttu-id="263c9-103">Changesecurrityberechtigungs-Methode der Win32- \_ Pagefile-Klasse</span><span class="sxs-lookup"><span data-stu-id="263c9-103">ChangeSecurityPermissions method of the Win32\_PageFile class</span></span>

<span data-ttu-id="263c9-104">Die [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode **changesecurrityberechtigungs** Änderungen ändern die Sicherheits Berechtigungen für die logische Auslagerungs Datei, die im Objekt Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="263c9-104">The **ChangeSecurityPermissions** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method changes the security permissions for the logical paging file specified in the object path.</span></span> <span data-ttu-id="263c9-105">Wenn es sich bei der logischen Datei um ein Verzeichnis handelt, ist **changesekurityberechtigungen** rekursiv und ändert die Sicherheits Berechtigungen aller Dateien und Unterverzeichnisse, die im Verzeichnis enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="263c9-105">If the logical file is a directory, then **ChangeSecurityPermissions** is recursive, and changes the security permissions of all of the files and subdirectories that the directory contains.</span></span>

<span data-ttu-id="263c9-106">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="263c9-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="263c9-107">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="263c9-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="263c9-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="263c9-108">Syntax</span></span>


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a><span data-ttu-id="263c9-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="263c9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="263c9-110">*SecurityDescriptor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="263c9-110">*SecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="263c9-111">Ein Ausdruck, der zu einer Instanz von [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="263c9-111">Expression that resolves to an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span> <span data-ttu-id="263c9-112">Dieser Deskriptor enthält neue Sicherheits Berechtigungen für die Instanz von [**Win32 \_ Page File**](win32-pagefile.md).</span><span class="sxs-lookup"><span data-stu-id="263c9-112">This descriptor contains new security permissions for the instance of [**Win32\_PageFile**](win32-pagefile.md).</span></span>

</dd> <dt>

<span data-ttu-id="263c9-113">*Option* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="263c9-113">*Option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="263c9-114">Sicherheits Berechtigung, die geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="263c9-114">Security privilege to be modified.</span></span> <span data-ttu-id="263c9-115">Wenn Sie z. b. den Besitzer und die DACL-Sicherheit (die Zugriffs Steuerungs Liste) ändern möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="263c9-115">For example, to change the owner and discretionary access control list (DACL) security, use:</span></span>

`Option = 1 + 4`

<span data-ttu-id="263c9-116">Oder</span><span class="sxs-lookup"><span data-stu-id="263c9-116">-or-</span></span>

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span data-ttu-id="263c9-117"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Ändern \_ \_Sicherheits \_ Informationen** für den Besitzer (1)</span><span class="sxs-lookup"><span data-stu-id="263c9-117"><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**CHANGE\_OWNER\_SECURITY\_INFORMATION** (1)</span></span>


</dt> <dd>

<span data-ttu-id="263c9-118">Ändern Sie den Besitzer der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="263c9-118">Change the owner of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span data-ttu-id="263c9-119"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Ändern \_ Gruppen \_ Sicherheits \_ Informationen** (2)</span><span class="sxs-lookup"><span data-stu-id="263c9-119"><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**CHANGE\_GROUP\_SECURITY\_INFORMATION** (2)</span></span>


</dt> <dd>

<span data-ttu-id="263c9-120">Ändern Sie die Gruppe der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="263c9-120">Change the group of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span data-ttu-id="263c9-121"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Ändern \_ DACL- \_ Sicherheits \_ Informationen** (4)</span><span class="sxs-lookup"><span data-stu-id="263c9-121"><span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**CHANGE\_DACL\_SECURITY\_INFORMATION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="263c9-122">Ändern Sie die DACL der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="263c9-122">Change the DACL of the logical file.</span></span>

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span data-ttu-id="263c9-123"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Ändern \_ SACL- \_ Sicherheits \_ Informationen** (8)</span><span class="sxs-lookup"><span data-stu-id="263c9-123"><span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**CHANGE\_SACL\_SECURITY\_INFORMATION** (8)</span></span>


</dt> <dd>

<span data-ttu-id="263c9-124">Ändern Sie die System Zugriffs Steuerungs Liste (SACL) der logischen Datei.</span><span class="sxs-lookup"><span data-stu-id="263c9-124">Change the system access control list (SACL) of the logical file.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="263c9-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="263c9-125">Return value</span></span>

<span data-ttu-id="263c9-126">Gibt den Wert 0 (null) zurück, wenn die Berechtigungen geändert werden, und eine andere Zahl, um einen Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="263c9-126">Returns a value of 0 (zero) if the permissions are changed, and a different number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="263c9-127">**Erfolgreich**</span><span class="sxs-lookup"><span data-stu-id="263c9-127">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="263c9-128">0</span><span class="sxs-lookup"><span data-stu-id="263c9-128">0</span></span>

<span data-ttu-id="263c9-129">Die Anforderung ist erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="263c9-129">The request is successful.</span></span>

</dd> <dt>

<span data-ttu-id="263c9-130">**Zugriff verweigert**</span><span class="sxs-lookup"><span data-stu-id="263c9-130">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="263c9-131">2</span><span class="sxs-lookup"><span data-stu-id="263c9-131">2</span></span>

<span data-ttu-id="263c9-132">Zugriff verweigert.“</span><span class="sxs-lookup"><span data-stu-id="263c9-132">Access is denied.</span></span>

</dd> <dt>

<span data-ttu-id="263c9-133">**Nicht spezifizierter Fehler**</span><span class="sxs-lookup"><span data-stu-id="263c9-133">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="263c9-134">8</span><span class="sxs-lookup"><span data-stu-id="263c9-134">8</span></span>

<span data-ttu-id="263c9-135">Ein nicht angegebener Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="263c9-135">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="263c9-136">**Ungültiges Objekt**</span><span class="sxs-lookup"><span data-stu-id="263c9-136">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="263c9-137">9</span><span class="sxs-lookup"><span data-stu-id="263c9-137">9</span></span>

<span data-ttu-id="263c9-138">Der angegebene Name ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="263c9-138">The specified name is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="263c9-139">**Objekt ist bereits vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="263c9-139">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="263c9-140">10</span><span class="sxs-lookup"><span data-stu-id="263c9-140">10</span></span>

<span data-ttu-id="263c9-141">Das Objekt "" ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="263c9-141">The specified object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="263c9-142">**Dateisystem nicht NTFS**</span><span class="sxs-lookup"><span data-stu-id="263c9-142">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="263c9-143">11</span><span class="sxs-lookup"><span data-stu-id="263c9-143">11</span></span>

<span data-ttu-id="263c9-144">Das Dateisystem ist kein NTFS-Dateisystem.</span><span class="sxs-lookup"><span data-stu-id="263c9-144">The file system is not an NTFS file system.</span></span>

</dd> <dt>

<span data-ttu-id="263c9-145">**Plattform nicht NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="263c9-145">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="263c9-146">12</span><span class="sxs-lookup"><span data-stu-id="263c9-146">12</span></span>

<span data-ttu-id="263c9-147">Die Plattform ist nicht Windows.</span><span class="sxs-lookup"><span data-stu-id="263c9-147">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="263c9-148">**Laufwerk nicht identisch**</span><span class="sxs-lookup"><span data-stu-id="263c9-148">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="263c9-149">13</span><span class="sxs-lookup"><span data-stu-id="263c9-149">13</span></span>

<span data-ttu-id="263c9-150">Das Laufwerk ist nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="263c9-150">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="263c9-151">**Verzeichnis nicht leer**</span><span class="sxs-lookup"><span data-stu-id="263c9-151">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="263c9-152">14</span><span class="sxs-lookup"><span data-stu-id="263c9-152">14</span></span>

<span data-ttu-id="263c9-153">Das Verzeichnis ist nicht leer.</span><span class="sxs-lookup"><span data-stu-id="263c9-153">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="263c9-154">**Freigabe Verletzung**</span><span class="sxs-lookup"><span data-stu-id="263c9-154">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="263c9-155">15</span><span class="sxs-lookup"><span data-stu-id="263c9-155">15</span></span>

<span data-ttu-id="263c9-156">Eine Freigabe Verletzung ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="263c9-156">There is a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="263c9-157">**Ungültige Startdatei**</span><span class="sxs-lookup"><span data-stu-id="263c9-157">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="263c9-158">16</span><span class="sxs-lookup"><span data-stu-id="263c9-158">16</span></span>

<span data-ttu-id="263c9-159">Die angegebene Startdatei ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="263c9-159">The specified start file is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="263c9-160">**Berechtigung nicht aufrechterhalten**</span><span class="sxs-lookup"><span data-stu-id="263c9-160">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="263c9-161">17</span><span class="sxs-lookup"><span data-stu-id="263c9-161">17</span></span>

<span data-ttu-id="263c9-162">Eine für den Vorgang erforderliche Berechtigung fehlt.</span><span class="sxs-lookup"><span data-stu-id="263c9-162">A privilege required for the operation is missing.</span></span>

</dd> <dt>

<span data-ttu-id="263c9-163">**Ungültiger Parameter**</span><span class="sxs-lookup"><span data-stu-id="263c9-163">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="263c9-164">21</span><span class="sxs-lookup"><span data-stu-id="263c9-164">21</span></span>

<span data-ttu-id="263c9-165">Ein angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="263c9-165">A specified parameter is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="263c9-166">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="263c9-166">Requirements</span></span>



| <span data-ttu-id="263c9-167">Anforderung</span><span class="sxs-lookup"><span data-stu-id="263c9-167">Requirement</span></span> | <span data-ttu-id="263c9-168">Wert</span><span class="sxs-lookup"><span data-stu-id="263c9-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="263c9-169">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="263c9-169">Minimum supported client</span></span><br/> | <span data-ttu-id="263c9-170">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="263c9-170">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="263c9-171">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="263c9-171">Minimum supported server</span></span><br/> | <span data-ttu-id="263c9-172">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="263c9-172">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="263c9-173">Namespace</span><span class="sxs-lookup"><span data-stu-id="263c9-173">Namespace</span></span><br/>                | <span data-ttu-id="263c9-174">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="263c9-174">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="263c9-175">MOF</span><span class="sxs-lookup"><span data-stu-id="263c9-175">MOF</span></span><br/>                      | <dl> <span data-ttu-id="263c9-176"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="263c9-176"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="263c9-177">DLL</span><span class="sxs-lookup"><span data-stu-id="263c9-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="263c9-178"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="263c9-178"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="263c9-179">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="263c9-179">See also</span></span>

<dl> <dt>

<span data-ttu-id="263c9-180">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="263c9-180">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="263c9-181">**Win32- \_ Pagefile**</span><span class="sxs-lookup"><span data-stu-id="263c9-181">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

