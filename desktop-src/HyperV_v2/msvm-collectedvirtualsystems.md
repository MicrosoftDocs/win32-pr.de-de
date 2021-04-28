---
description: 'Msvm_CollectedVirtualSystems-Klasse: Ordnet die Msvm \_ VirtualSystemCollection den enthaltenen Msvm \_ ComputerSystem-Objekten zu.'
ms.assetid: ad783188-b60a-4271-aa2d-8050c36e70eb
title: Msvm_CollectedVirtualSystems-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectedVirtualSystems
- Msvm_CollectedVirtualSystems.Collection
- Msvm_CollectedVirtualSystems.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d6775f41a6e2ae7e45bac642fcd32b8deaec3fda
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119278"
---
# <a name="msvm_collectedvirtualsystems-class"></a><span data-ttu-id="f2794-103">Msvm \_ CollectedVirtualSystems-Klasse</span><span class="sxs-lookup"><span data-stu-id="f2794-103">Msvm\_CollectedVirtualSystems class</span></span>

<span data-ttu-id="f2794-104">Ordnet die [**Msvm \_ VirtualSystemCollection**](msvm-virtualsystemcollection.md) den enthaltenen [**Msvm \_ ComputerSystem-Objekten**](msvm-computersystem.md) zu.</span><span class="sxs-lookup"><span data-stu-id="f2794-104">Associates the [**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md) to the contained [**Msvm\_ComputerSystem**](msvm-computersystem.md) objects.</span></span>

<span data-ttu-id="f2794-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f2794-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2794-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2794-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectedVirtualSystems : CIM_CollectedMSEs
{
  Msvm_VirtualSystemCollection REF Collection;
  Msvm_ComputerSystem          REF Member;
};
```

## <a name="members"></a><span data-ttu-id="f2794-107">Member</span><span class="sxs-lookup"><span data-stu-id="f2794-107">Members</span></span>

<span data-ttu-id="f2794-108">Die **Msvm \_ CollectedVirtualSystems-Klasse** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f2794-108">The **Msvm\_CollectedVirtualSystems** class has these types of members:</span></span>

-   [<span data-ttu-id="f2794-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f2794-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f2794-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f2794-110">Properties</span></span>

<span data-ttu-id="f2794-111">Die **Msvm \_ CollectedVirtualSystems-Klasse** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f2794-111">The **Msvm\_CollectedVirtualSystems** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f2794-112">**Sammlung**</span><span class="sxs-lookup"><span data-stu-id="f2794-112">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2794-113">Datentyp: **Msvm \_ VirtualSystemCollection**</span><span class="sxs-lookup"><span data-stu-id="f2794-113">Data type: **Msvm\_VirtualSystemCollection**</span></span>
</dt> <dt>

<span data-ttu-id="f2794-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f2794-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2794-115">Qualifizierer: [**Aggregieren,**](/windows/desktop/WmiSdk/standard-qualifiers) [**Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span><span class="sxs-lookup"><span data-stu-id="f2794-115">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span></span>
</dt> </dl>

<span data-ttu-id="f2794-116">Ein [**Msvm \_ VirtualSystemCollection-Gruppierungsobjekt**](msvm-virtualsystemcollection.md) oder ein Bag-Objekt, das die Auflistung darstellt.</span><span class="sxs-lookup"><span data-stu-id="f2794-116">An [**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md) grouping or 'bag' object that represents the collection.</span></span>

</dd> <dt>

<span data-ttu-id="f2794-117">**Member**</span><span class="sxs-lookup"><span data-stu-id="f2794-117">**Member**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2794-118">Datentyp: **Msvm \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="f2794-118">Data type: **Msvm\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="f2794-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f2794-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2794-120">Qualifizierer: [**Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span><span class="sxs-lookup"><span data-stu-id="f2794-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span></span>
</dt> </dl>

<span data-ttu-id="f2794-121">Ein [**Msvm \_ ComputerSystem-Objekt, das**](msvm-computersystem.md) die Member der Auflistung enthält.</span><span class="sxs-lookup"><span data-stu-id="f2794-121">An [**Msvm\_ComputerSystem**](msvm-computersystem.md) object containing the members of the collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f2794-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f2794-122">Requirements</span></span>



| <span data-ttu-id="f2794-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f2794-123">Requirement</span></span> | <span data-ttu-id="f2794-124">Wert</span><span class="sxs-lookup"><span data-stu-id="f2794-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2794-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f2794-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f2794-126">nur Windows 10 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f2794-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="f2794-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f2794-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f2794-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f2794-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="f2794-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="f2794-129">Namespace</span></span><br/>                | <span data-ttu-id="f2794-130">\\Root-Virtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="f2794-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f2794-131">MOF</span><span class="sxs-lookup"><span data-stu-id="f2794-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f2794-132"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="f2794-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f2794-133">DLL</span><span class="sxs-lookup"><span data-stu-id="f2794-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2794-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f2794-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f2794-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f2794-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2794-136">**CIM \_ CollectedMSEs**</span><span class="sxs-lookup"><span data-stu-id="f2794-136">**CIM\_CollectedMSEs**</span></span>](cim-collectedmses.md)
</dt> </dl>

 

