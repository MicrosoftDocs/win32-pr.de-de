---
title: Win32_RDMSVirtualDesktop-Klasse
description: Stellt einen virtuellen Desktop dar.
ms.assetid: e2952ec0-38d0-4a1c-b423-3ae1fbc701b3
ms.tgt_platform: multiple
keywords:
- Win32_RDMSVirtualDesktop-Klasse Remotedesktopdienste
- Win32_RDMSVirtualDesktop Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop
- Win32_RDMSVirtualDesktop.Name
- Win32_RDMSVirtualDesktop.HostName
- Win32_RDMSVirtualDesktop.Status
- Win32_RDMSVirtualDesktop.CollectionAlias
- Win32_RDMSVirtualDesktop.SessionState
- Win32_RDMSVirtualDesktop.SessionUserName
- Win32_RDMSVirtualDesktop.UserName
- Win32_RDMSVirtualDesktop.UserDomain
- Win32_RDMSVirtualDesktop.VMState
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 247c49c7ad069b4feff3469ac21ec803ebc9f741
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337732"
---
# <a name="win32_rdmsvirtualdesktop-class"></a><span data-ttu-id="12d47-105">Win32 \_ rdmsvirtualdesktop-Klasse</span><span class="sxs-lookup"><span data-stu-id="12d47-105">Win32\_RDMSVirtualDesktop class</span></span>

<span data-ttu-id="12d47-106">Stellt einen virtuellen Desktop dar.</span><span class="sxs-lookup"><span data-stu-id="12d47-106">Represents a virtual desktop.</span></span>

<span data-ttu-id="12d47-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="12d47-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="12d47-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="12d47-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSVirtualDesktop
{
  string Name;
  string HostName;
  uint32 Status;
  string CollectionAlias;
  string SessionState;
  string SessionUserName;
  string UserName;
  string UserDomain;
  uint32 VMState;
};
```

## <a name="members"></a><span data-ttu-id="12d47-109">Member</span><span class="sxs-lookup"><span data-stu-id="12d47-109">Members</span></span>

<span data-ttu-id="12d47-110">Die **Win32 \_ rdmsvirtualdesktop-** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="12d47-110">The **Win32\_RDMSVirtualDesktop** class has these types of members:</span></span>

-   [<span data-ttu-id="12d47-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="12d47-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="12d47-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="12d47-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="12d47-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="12d47-113">Methods</span></span>

<span data-ttu-id="12d47-114">Die **Win32 \_ rdmsvirtualdesktop-** Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="12d47-114">The **Win32\_RDMSVirtualDesktop** class has these methods.</span></span>



| <span data-ttu-id="12d47-115">Methode</span><span class="sxs-lookup"><span data-stu-id="12d47-115">Method</span></span>                                                                                              | <span data-ttu-id="12d47-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="12d47-116">Description</span></span>                                                                                            |
|:----------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="12d47-117">**Getuserzuweisung**</span><span class="sxs-lookup"><span data-stu-id="12d47-117">**GetUserAssignment**</span></span>](getuserassignment-win32-rdmsvirtualdesktop.md)                             | <span data-ttu-id="12d47-118">Ruft den Benutzernamen und den Domänen Namen des Benutzers ab, der dem virtuellen Desktop zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="12d47-118">Retrieves the username and domain name of the user that is assigned to the virtual desktop.</span></span><br/> |
| [<span data-ttu-id="12d47-119">**Getvirtualdesktopassignetdtouser**</span><span class="sxs-lookup"><span data-stu-id="12d47-119">**GetVirtualDesktopAssignedToUser**</span></span>](getvirtualdesktopassignedtouser-win32-rdmsvirtualdesktop.md) | <span data-ttu-id="12d47-120">Ruft den virtuellen Desktop ab, der dem angegebenen Benutzer zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="12d47-120">Retrieves the virtual desktop that is assigned to the specified user.</span></span><br/>                       |
| [<span data-ttu-id="12d47-121">**Getvirtualdesktopdetails**</span><span class="sxs-lookup"><span data-stu-id="12d47-121">**GetVirtualDesktopDetails**</span></span>](getvirtualdesktopdetails-win32-rdmsvirtualdesktop.md)               | <span data-ttu-id="12d47-122">Ruft die zusätzlichen Informationen zum virtuellen Desktop ab.</span><span class="sxs-lookup"><span data-stu-id="12d47-122">Retrieves the additional information about the virtual desktop.</span></span><br/>                             |
| [<span data-ttu-id="12d47-123">**Getvirtualdesktopstate**</span><span class="sxs-lookup"><span data-stu-id="12d47-123">**GetVirtualDesktopState**</span></span>](getvirtualdesktopstate-win32-rdmsvirtualdesktop.md)                   | <span data-ttu-id="12d47-124">Ruft den Zustand des virtuellen Desktops ab.</span><span class="sxs-lookup"><span data-stu-id="12d47-124">Retrieves the state of the virtual desktop.</span></span><br/>                                                 |
| [<span data-ttu-id="12d47-125">**Removeuserzuweisung**</span><span class="sxs-lookup"><span data-stu-id="12d47-125">**RemoveUserAssignment**</span></span>](removeuserassignment-win32-rdmsvirtualdesktop.md)                       | <span data-ttu-id="12d47-126">Entfernt die Benutzer Zuweisung vom virtuellen Desktop.</span><span class="sxs-lookup"><span data-stu-id="12d47-126">Removes the user assignment from the virtual desktop.</span></span><br/>                                       |
| [<span data-ttu-id="12d47-127">**Setuserzuweisung**</span><span class="sxs-lookup"><span data-stu-id="12d47-127">**SetUserAssignment**</span></span>](setuserassignment-win32-rdmsvirtualdesktop.md)                             | <span data-ttu-id="12d47-128">Weist einem Benutzer einen virtuellen Desktop zu.</span><span class="sxs-lookup"><span data-stu-id="12d47-128">Assigns a virtual desktop to a user.</span></span><br/>                                                        |
| [<span data-ttu-id="12d47-129">**Setvirtualdesktopstate**</span><span class="sxs-lookup"><span data-stu-id="12d47-129">**SetVirtualDesktopState**</span></span>](setvirtualdesktopstate-win32-rdmsvirtualdesktop.md)                   | <span data-ttu-id="12d47-130">Aktualisiert den Zustand des virtuellen Desktops.</span><span class="sxs-lookup"><span data-stu-id="12d47-130">Updates the state of the virtual desktop.</span></span><br/>                                                   |



 

### <a name="properties"></a><span data-ttu-id="12d47-131">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="12d47-131">Properties</span></span>

<span data-ttu-id="12d47-132">Die **Win32 \_ rdmsvirtualdesktop-** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="12d47-132">The **Win32\_RDMSVirtualDesktop** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="12d47-133">**Collectionalias**</span><span class="sxs-lookup"><span data-stu-id="12d47-133">**CollectionAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12d47-134">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="12d47-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12d47-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="12d47-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12d47-136">Qualifizierer: [ **optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="12d47-136">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="12d47-137">Ruft den Alias der virtuellen Desktop Sammlung ab, die den virtuellen Computer verwaltet.</span><span class="sxs-lookup"><span data-stu-id="12d47-137">Gets the alias to the virtual desktop collection that manages the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="12d47-138">**HostName**</span><span class="sxs-lookup"><span data-stu-id="12d47-138">**HostName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12d47-139">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="12d47-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12d47-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="12d47-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12d47-141">Ruft den Namen des Computers ab, auf dem der virtuelle Computer gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="12d47-141">Gets the name of the machine that hosts the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="12d47-142">**Name**</span><span class="sxs-lookup"><span data-stu-id="12d47-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12d47-143">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="12d47-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12d47-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="12d47-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12d47-145">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="12d47-145">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="12d47-146">Ruft den Namen des virtuellen Computers ab.</span><span class="sxs-lookup"><span data-stu-id="12d47-146">Gets the name of the of virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="12d47-147">**SessionState**</span><span class="sxs-lookup"><span data-stu-id="12d47-147">**SessionState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12d47-148">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="12d47-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12d47-149">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="12d47-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12d47-150">Qualifizierer: [ **optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="12d47-150">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="12d47-151">Ruft den Status der virtuellen Desktop Sitzung ab.</span><span class="sxs-lookup"><span data-stu-id="12d47-151">Gets the state of the virtual desktop session.</span></span>

</dd> <dt>

<span data-ttu-id="12d47-152">**Sessionusername**</span><span class="sxs-lookup"><span data-stu-id="12d47-152">**SessionUserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12d47-153">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="12d47-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12d47-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="12d47-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12d47-155">Qualifizierer: [ **optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="12d47-155">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="12d47-156">Ruft den Benutzernamen des Benutzers ab, der bei der virtuellen Desktop Sitzung angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="12d47-156">Gets the username of the user that is logged in to the virtual desktop session.</span></span>

</dd> <dt>

<span data-ttu-id="12d47-157">**Status**</span><span class="sxs-lookup"><span data-stu-id="12d47-157">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12d47-158">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="12d47-158">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="12d47-159">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="12d47-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12d47-160">Ruft den Status des virtuellen Computers ab.</span><span class="sxs-lookup"><span data-stu-id="12d47-160">Gets the status of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="12d47-161">**UserDomain**</span><span class="sxs-lookup"><span data-stu-id="12d47-161">**UserDomain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12d47-162">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="12d47-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12d47-163">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="12d47-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12d47-164">Qualifizierer: [ **optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="12d47-164">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="12d47-165">Ruft den Domänen Namen des Benutzers ab, der dem virtuellen Desktop zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="12d47-165">Gets the domain name of the user that is assigned to the virtual desktop.</span></span>

</dd> <dt>

<span data-ttu-id="12d47-166">**UserName**</span><span class="sxs-lookup"><span data-stu-id="12d47-166">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12d47-167">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="12d47-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="12d47-168">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="12d47-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12d47-169">Qualifizierer: [ **optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="12d47-169">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="12d47-170">Ruft den Benutzernamen des Benutzers ab, der dem virtuellen Desktop zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="12d47-170">Gets the username of the user that is assigned to the virtual desktop.</span></span>

</dd> <dt>

<span data-ttu-id="12d47-171">**VMState**</span><span class="sxs-lookup"><span data-stu-id="12d47-171">**VMState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12d47-172">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="12d47-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="12d47-173">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="12d47-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="12d47-174">Ruft den Zustand des virtuellen Desktops ab.</span><span class="sxs-lookup"><span data-stu-id="12d47-174">Gets the state of the virtual desktop.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="12d47-175">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="12d47-175">Requirements</span></span>



| <span data-ttu-id="12d47-176">Anforderung</span><span class="sxs-lookup"><span data-stu-id="12d47-176">Requirement</span></span> | <span data-ttu-id="12d47-177">Wert</span><span class="sxs-lookup"><span data-stu-id="12d47-177">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="12d47-178">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="12d47-178">Minimum supported client</span></span><br/> | <span data-ttu-id="12d47-179">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="12d47-179">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="12d47-180">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="12d47-180">Minimum supported server</span></span><br/> | <span data-ttu-id="12d47-181">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="12d47-181">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="12d47-182">Namespace</span><span class="sxs-lookup"><span data-stu-id="12d47-182">Namespace</span></span><br/>                | <span data-ttu-id="12d47-183">Root \\ CIMV2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="12d47-183">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="12d47-184">MOF</span><span class="sxs-lookup"><span data-stu-id="12d47-184">MOF</span></span><br/>                      | <dl> <span data-ttu-id="12d47-185"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="12d47-185"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="12d47-186">DLL</span><span class="sxs-lookup"><span data-stu-id="12d47-186">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12d47-187"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12d47-187"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="12d47-188">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="12d47-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12d47-189">Remotedesktop Management Services-Anbieter</span><span class="sxs-lookup"><span data-stu-id="12d47-189">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

