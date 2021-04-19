---
description: Stellt eine Zuordnung zwischen einem System und einem Ressourcenpool dar, bei dem es sich um eine Komponente des Systems handelt.
ms.assetid: 0ac60dbd-0498-4978-b2d6-f4c9926a83a8
title: CIM_HostedResourcePool-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedResourcePool
- CIM_HostedResourcePool.GroupComponent
- CIM_HostedResourcePool.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: dbb6d523b533d6e8b2f5bc1e21de93962cfd860f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106339730"
---
# <a name="cim_hostedresourcepool-class"></a><span data-ttu-id="3f997-103">CIM- \_ Klasse "hustedresourcepool"</span><span class="sxs-lookup"><span data-stu-id="3f997-103">CIM\_HostedResourcePool class</span></span>

<span data-ttu-id="3f997-104">Stellt eine Zuordnung zwischen einem System und einem Ressourcenpool dar, bei dem es sich um eine Komponente des Systems handelt.</span><span class="sxs-lookup"><span data-stu-id="3f997-104">Represents an association between a system and a resource pool that is a component of the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f997-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3f997-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Composition, Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource")]
class CIM_HostedResourcePool : CIM_SystemComponent
{
  CIM_System       REF GroupComponent;
  CIM_ResourcePool REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="3f997-106">Member</span><span class="sxs-lookup"><span data-stu-id="3f997-106">Members</span></span>

<span data-ttu-id="3f997-107">Die CIM-Klasse " **\_ hustedresourcepool** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="3f997-107">The **CIM\_HostedResourcePool** class has these types of members:</span></span>

-   [<span data-ttu-id="3f997-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3f997-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3f997-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3f997-109">Properties</span></span>

<span data-ttu-id="3f997-110">Die CIM-Klasse " **\_ hustedresourcepool** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3f997-110">The **CIM\_HostedResourcePool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3f997-111">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="3f997-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f997-112">Datentyp: **CIM- \_ System**</span><span class="sxs-lookup"><span data-stu-id="3f997-112">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="3f997-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3f997-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f997-114">Qualifizierer: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="3f997-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="3f997-115">Das übergeordnete System in der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="3f997-115">The parent system in the association.</span></span>

</dd> <dt>

<span data-ttu-id="3f997-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="3f997-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f997-117">Datentyp: **CIM \_ resourcepool**</span><span class="sxs-lookup"><span data-stu-id="3f997-117">Data type: **CIM\_ResourcePool**</span></span>
</dt> <dt>

<span data-ttu-id="3f997-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3f997-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f997-119">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="3f997-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="3f997-120">Der Ressourcenpool, bei dem es sich um eine Komponente des Systems handelt.</span><span class="sxs-lookup"><span data-stu-id="3f997-120">The resource pool that is a component of the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3f997-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3f997-121">Requirements</span></span>



| <span data-ttu-id="3f997-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3f997-122">Requirement</span></span> | <span data-ttu-id="3f997-123">Wert</span><span class="sxs-lookup"><span data-stu-id="3f997-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f997-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3f997-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3f997-125">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="3f997-125">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="3f997-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3f997-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3f997-127">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="3f997-127">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="3f997-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="3f997-128">Namespace</span></span><br/>                | <span data-ttu-id="3f997-129">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="3f997-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3f997-130">MOF</span><span class="sxs-lookup"><span data-stu-id="3f997-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3f997-131"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3f997-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3f997-132">DLL</span><span class="sxs-lookup"><span data-stu-id="3f997-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f997-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3f997-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3f997-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3f997-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f997-135">**CIM- \_ SystemComponent**</span><span class="sxs-lookup"><span data-stu-id="3f997-135">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> </dl>

 

