---
title: Win32_RdvhManagement-Klasse
description: Beschreibt einen Remotedesktop den Verwaltungsdienst für virtuelle Hosts (RDVH).
ms.assetid: 2a81786c-e772-4596-9846-a46828f9b48b
ms.tgt_platform: multiple
keywords:
- Win32_RdvhManagement-Klasse Remotedesktopdienste
- Win32_RdvhManagement Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_RdvhManagement
api_location:
- TSVmHostWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b01e2cde81173035d00587782dc45d9ddeb66fcf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345900"
---
# <a name="win32_rdvhmanagement-class"></a><span data-ttu-id="cc7ac-105">Win32 \_ rdvhmanagement-Klasse</span><span class="sxs-lookup"><span data-stu-id="cc7ac-105">Win32\_RdvhManagement class</span></span>

<span data-ttu-id="cc7ac-106">Beschreibt einen Remotedesktop den Verwaltungsdienst für virtuelle Hosts (RDVH).</span><span class="sxs-lookup"><span data-stu-id="cc7ac-106">Describes a Remote Desktop Virtual Host (RDVH) management service.</span></span>

<span data-ttu-id="cc7ac-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="cc7ac-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc7ac-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc7ac-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_TSVmHost_Prov"), AMENDMENT]
class Win32_RdvhManagement
{
};
```

## <a name="members"></a><span data-ttu-id="cc7ac-109">Member</span><span class="sxs-lookup"><span data-stu-id="cc7ac-109">Members</span></span>

<span data-ttu-id="cc7ac-110">Die **Win32- \_ rdvhmanagement** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="cc7ac-110">The **Win32\_RdvhManagement** class has these types of members:</span></span>

-   [<span data-ttu-id="cc7ac-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="cc7ac-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="cc7ac-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="cc7ac-112">Methods</span></span>

<span data-ttu-id="cc7ac-113">Die **Win32- \_ rdvhmanagement** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="cc7ac-113">The **Win32\_RdvhManagement** class has these methods.</span></span>



| <span data-ttu-id="cc7ac-114">Methode</span><span class="sxs-lookup"><span data-stu-id="cc7ac-114">Method</span></span>                                                                                  | <span data-ttu-id="cc7ac-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cc7ac-115">Description</span></span>                                                                                                                                                             |
|:----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cc7ac-116">**Rdvkreateuserdisktemplate**</span><span class="sxs-lookup"><span data-stu-id="cc7ac-116">**RdvCreateUserDiskTemplate**</span></span>](rdvcreateuserdisktemplate-win32-rdvhmanagement.md)     | <span data-ttu-id="cc7ac-117">Erstellt die Vorlage für Benutzer Datenträger mit der angegebenen maximalen Größe und am angegebenen Speicherort.</span><span class="sxs-lookup"><span data-stu-id="cc7ac-117">Creates User Disk Template of specified max size and at the specified location.</span></span> <span data-ttu-id="cc7ac-118">Alle erstellten Benutzer Datenträger verfügen über maximale Größe, die der maximalen Größe der Vorlage entspricht.</span><span class="sxs-lookup"><span data-stu-id="cc7ac-118">All User Disks created will have max sizes matching the Template's max size.</span></span><br/> |
| [<span data-ttu-id="cc7ac-119">**RdvMigrateVmToDifferentHost**</span><span class="sxs-lookup"><span data-stu-id="cc7ac-119">**RdvMigrateVmToDifferentHost**</span></span>](rdvmigratevmtodifferenthost-win32-rdvhmanagement.md) | <span data-ttu-id="cc7ac-120">Initiiert eine Live Migration virtueller Computer in VDI-Szenarios.</span><span class="sxs-lookup"><span data-stu-id="cc7ac-120">Initiates a live migration of virtual machine in VDI scenarios</span></span><br/>                                                                                               |
| [<span data-ttu-id="cc7ac-121">**Rdvcopybasevmlokal**</span><span class="sxs-lookup"><span data-stu-id="cc7ac-121">**RdvCopyBaseVmLocally**</span></span>](rdvcopybasevmlocally-win32-rdvhmanagement.md)               | <span data-ttu-id="cc7ac-122">Kopiert den Basis-VM-Speicherort lokal auf RDV-Host Server</span><span class="sxs-lookup"><span data-stu-id="cc7ac-122">Copies Base VM location locally to RDV Host server</span></span><br/>                                                                                                           |
| [<span data-ttu-id="cc7ac-123">**Rdvkreateuserdisktemplate**</span><span class="sxs-lookup"><span data-stu-id="cc7ac-123">**RdvCreateUserDiskTemplate**</span></span>](rdvcreateuserdisktemplate-win32-rdvhmanagement.md)     | <span data-ttu-id="cc7ac-124">Erstellt die Vorlage für Benutzer Datenträger mit der angegebenen maximalen Größe und am angegebenen Speicherort.</span><span class="sxs-lookup"><span data-stu-id="cc7ac-124">Creates User Disk Template of specified max size and at the specified location.</span></span> <span data-ttu-id="cc7ac-125">Alle erstellten Benutzer Datenträger verfügen über maximale Größe, die der maximalen Größe der Vorlage entspricht.</span><span class="sxs-lookup"><span data-stu-id="cc7ac-125">All User Disks created will have max sizes matching the Template's max size.</span></span><br/> |
| [<span data-ttu-id="cc7ac-126">**RdvMigrateVmToDifferentHost**</span><span class="sxs-lookup"><span data-stu-id="cc7ac-126">**RdvMigrateVmToDifferentHost**</span></span>](rdvmigratevmtodifferenthost-win32-rdvhmanagement.md) | <span data-ttu-id="cc7ac-127">Initiiert eine Live Migration virtueller Computer in VDI-Szenarien.</span><span class="sxs-lookup"><span data-stu-id="cc7ac-127">Initiates a live migration of virtual machine in VDI scenarios.</span></span><br/>                                                                                              |
| [<span data-ttu-id="cc7ac-128">**Rdvsetupvm-Berechtigungen**</span><span class="sxs-lookup"><span data-stu-id="cc7ac-128">**RdvSetupVMPermissions**</span></span>](rdvsetupvmpermissions-win32-rdvhmanagement.md)             | <span data-ttu-id="cc7ac-129">Legt Berechtigungen für die VM für den Aufrufer fest.</span><span class="sxs-lookup"><span data-stu-id="cc7ac-129">Sets permissions in VM for the caller</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="cc7ac-130">**Rdvundovm-Berechtigungen**</span><span class="sxs-lookup"><span data-stu-id="cc7ac-130">**RdvUndoVMPermissions**</span></span>](rdvundovmpermissions-win32-rdvhmanagement.md)               | <span data-ttu-id="cc7ac-131">Kehrt die Berechtigungen in der von rdvsetupvmberechtigungs Gruppe festgelegten VM zurück.</span><span class="sxs-lookup"><span data-stu-id="cc7ac-131">Reverts permissions in VM set by RdvSetupVMPermissions</span></span><br/>                                                                                                       |



 

## <a name="requirements"></a><span data-ttu-id="cc7ac-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cc7ac-132">Requirements</span></span>



| <span data-ttu-id="cc7ac-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc7ac-133">Requirement</span></span> | <span data-ttu-id="cc7ac-134">Wert</span><span class="sxs-lookup"><span data-stu-id="cc7ac-134">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc7ac-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cc7ac-135">Minimum supported client</span></span><br/> | <span data-ttu-id="cc7ac-136">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="cc7ac-136">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="cc7ac-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cc7ac-137">Minimum supported server</span></span><br/> | <span data-ttu-id="cc7ac-138">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cc7ac-138">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="cc7ac-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="cc7ac-139">Namespace</span></span><br/>                | <span data-ttu-id="cc7ac-140">Root \\ CIMV2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="cc7ac-140">Root\\cimv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="cc7ac-141">MOF</span><span class="sxs-lookup"><span data-stu-id="cc7ac-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cc7ac-142"><dt>"Zvmhost. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="cc7ac-142"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="cc7ac-143">DLL</span><span class="sxs-lookup"><span data-stu-id="cc7ac-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc7ac-144"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc7ac-144"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



 

 





