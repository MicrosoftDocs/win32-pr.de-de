---
description: Verwaltet die zustellbaren Geräte auf einem Host Computersystem.
ms.assetid: d958e978-682e-49eb-bd10-d31d9563fdbf
title: Msvm_AssignableDeviceService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AssignableDeviceService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c8aff620e9227000b2c4a03069f8a5f900a5fc82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369100"
---
# <a name="msvm_assignabledeviceservice-class"></a><span data-ttu-id="7ce9c-103">MSVM-Klasse ' zuder \_ Zustell barkeit '</span><span class="sxs-lookup"><span data-stu-id="7ce9c-103">Msvm\_AssignableDeviceService class</span></span>

<span data-ttu-id="7ce9c-104">Verwaltet die zustellbaren Geräte auf einem Host Computersystem.</span><span class="sxs-lookup"><span data-stu-id="7ce9c-104">Manages the assignable devices on a host computer system.</span></span>

<span data-ttu-id="7ce9c-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7ce9c-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ce9c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ce9c-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AssignableDeviceService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="7ce9c-107">Member</span><span class="sxs-lookup"><span data-stu-id="7ce9c-107">Members</span></span>

<span data-ttu-id="7ce9c-108">Die **MSVM \_** -Klasse "zuder Klasse" weist die folgenden Member auf:</span><span class="sxs-lookup"><span data-stu-id="7ce9c-108">The **Msvm\_AssignableDeviceService** class has these types of members:</span></span>

-   [<span data-ttu-id="7ce9c-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="7ce9c-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="7ce9c-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="7ce9c-110">Methods</span></span>

<span data-ttu-id="7ce9c-111">Die **MSVM-Klasse " \_ accessabledeviceservice** " verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="7ce9c-111">The **Msvm\_AssignableDeviceService** class has these methods.</span></span>



| <span data-ttu-id="7ce9c-112">Methode</span><span class="sxs-lookup"><span data-stu-id="7ce9c-112">Method</span></span>                                                                                    | <span data-ttu-id="7ce9c-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7ce9c-113">Description</span></span>                                                                                    |
|:------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7ce9c-114">**Dismountassignabledevice**</span><span class="sxs-lookup"><span data-stu-id="7ce9c-114">**DismountAssignableDevice**</span></span>](msvm-assignabledeviceservice-dismountassignabledevice.md) | <span data-ttu-id="7ce9c-115">Hebt die Einbindung des angegebenen PCI-Geräts auf, sodass es zugewiesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="7ce9c-115">Dismounts the specified PCI device so that it can be assigned.</span></span><br/>                      |
| [<span data-ttu-id="7ce9c-116">**Mountassignabledevice**</span><span class="sxs-lookup"><span data-stu-id="7ce9c-116">**MountAssignableDevice**</span></span>](msvm-assignabledeviceservice-mountassignabledevice.md)       | <span data-ttu-id="7ce9c-117">Stellt das angegebene PCI-Gerät bereit, sodass es vom Host Computersystem verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="7ce9c-117">Mounts the specified PCI device so that it can be used by the host computer system.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7ce9c-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7ce9c-118">Requirements</span></span>



| <span data-ttu-id="7ce9c-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7ce9c-119">Requirement</span></span> | <span data-ttu-id="7ce9c-120">Wert</span><span class="sxs-lookup"><span data-stu-id="7ce9c-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ce9c-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7ce9c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7ce9c-122">Windows 10, Version 1703, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7ce9c-122">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7ce9c-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7ce9c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7ce9c-124">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="7ce9c-124">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="7ce9c-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="7ce9c-125">Namespace</span></span><br/>                | <span data-ttu-id="7ce9c-126">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="7ce9c-126">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7ce9c-127">MOF</span><span class="sxs-lookup"><span data-stu-id="7ce9c-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7ce9c-128"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7ce9c-128"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7ce9c-129">DLL</span><span class="sxs-lookup"><span data-stu-id="7ce9c-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ce9c-130"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7ce9c-130"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7ce9c-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7ce9c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ce9c-132">**CIM- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="7ce9c-132">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




