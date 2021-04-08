---
description: Stellt eine Spezialisierung der Systemkomponenten Zuordnung dar, die festlegt, dass der Ressourcenpool im Kontext des Systems definiert ist.
ms.assetid: 72b68687-2b5f-4fef-bdca-a5c0bbfa3564
title: Msvm_HostedResourcePool-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HostedResourcePool
- Msvm_HostedResourcePool.GroupComponent
- Msvm_HostedResourcePool.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d64488a845e8d51bfe27829b01ebcf0ac7d944c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862071"
---
# <a name="msvm_hostedresourcepool-class"></a><span data-ttu-id="abc5a-103">MSVM- \_ Klasse "hustedresourcepool"</span><span class="sxs-lookup"><span data-stu-id="abc5a-103">Msvm\_HostedResourcePool class</span></span>

<span data-ttu-id="abc5a-104">Stellt eine Spezialisierung der Systemkomponenten Zuordnung dar, die festlegt, dass der Ressourcenpool im Kontext des Systems definiert ist.</span><span class="sxs-lookup"><span data-stu-id="abc5a-104">Represents a specialization of the system component association that establishes that the resource pool is defined in the context of the system.</span></span>

<span data-ttu-id="abc5a-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="abc5a-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="abc5a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="abc5a-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Composition, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HostedResourcePool : CIM_SystemComponent
{
  Msvm_ComputerSystem REF GroupComponent;
  CIM_ResourcePool    REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="abc5a-107">Member</span><span class="sxs-lookup"><span data-stu-id="abc5a-107">Members</span></span>

<span data-ttu-id="abc5a-108">Die **MSVM-Klasse " \_ hustedresourcepool** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="abc5a-108">The **Msvm\_HostedResourcePool** class has these types of members:</span></span>

-   [<span data-ttu-id="abc5a-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="abc5a-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="abc5a-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="abc5a-110">Properties</span></span>

<span data-ttu-id="abc5a-111">Die **MSVM-Klasse " \_ hustedresourcepool** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="abc5a-111">The **Msvm\_HostedResourcePool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="abc5a-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="abc5a-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abc5a-113">Datentyp: **[ **MSVM \_ Computersystem**](msvm-computersystem.md)**</span><span class="sxs-lookup"><span data-stu-id="abc5a-113">Data type: **[**Msvm\_ComputerSystem**](msvm-computersystem.md)**</span></span>
</dt> <dt>

<span data-ttu-id="abc5a-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="abc5a-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abc5a-115">Qualifizierer: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="abc5a-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="abc5a-116">Das übergeordnete System in der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="abc5a-116">The parent system in the association.</span></span>

</dd> <dt>

<span data-ttu-id="abc5a-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="abc5a-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abc5a-118">Datentyp: **[ **CIM \_ resourcepool**](/previous-versions//cc136903(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="abc5a-118">Data type: **[**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="abc5a-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="abc5a-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abc5a-120">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="abc5a-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="abc5a-121">Der Ressourcenpool, bei dem es sich um eine Komponente des Systems handelt.</span><span class="sxs-lookup"><span data-stu-id="abc5a-121">The resource pool that is a component of the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="abc5a-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="abc5a-122">Requirements</span></span>



| <span data-ttu-id="abc5a-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="abc5a-123">Requirement</span></span> | <span data-ttu-id="abc5a-124">Wert</span><span class="sxs-lookup"><span data-stu-id="abc5a-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abc5a-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="abc5a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="abc5a-126">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="abc5a-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="abc5a-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="abc5a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="abc5a-128">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="abc5a-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="abc5a-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="abc5a-129">Namespace</span></span><br/>                | <span data-ttu-id="abc5a-130">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="abc5a-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="abc5a-131">MOF</span><span class="sxs-lookup"><span data-stu-id="abc5a-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="abc5a-132"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="abc5a-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="abc5a-133">DLL</span><span class="sxs-lookup"><span data-stu-id="abc5a-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="abc5a-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="abc5a-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

