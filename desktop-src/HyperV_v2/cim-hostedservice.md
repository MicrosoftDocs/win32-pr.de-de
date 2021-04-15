---
description: Stellt eine Zuordnung zwischen einem Dienst und dem System dar, das den Dienst hostet. Ein System kann viele Dienste hosten, jedoch stellt diese Klasse keine Dienste dar, die auf mehreren Systemen gehostet werden.
ms.assetid: ede67a81-cf1b-41aa-b907-5b635cf80423
title: CIM_HostedService-Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedService
- CIM_HostedService.Antecedent
- CIM_HostedService.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 841c0e26898ed3baa4b4947779a395ee9ce870d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484206"
---
# <a name="cim_hostedservice-class-hyper-v-management"></a><span data-ttu-id="7fe2d-104">CIM_HostedService-Klasse (Hyper-V-Verwaltung)</span><span class="sxs-lookup"><span data-stu-id="7fe2d-104">CIM_HostedService class (Hyper-V management)</span></span>

<span data-ttu-id="7fe2d-105">Stellt eine Zuordnung zwischen einem Dienst und dem System dar, das den Dienst hostet.</span><span class="sxs-lookup"><span data-stu-id="7fe2d-105">Represents an association between a service and the system that hosts the service.</span></span> <span data-ttu-id="7fe2d-106">Ein System kann viele Dienste hosten, jedoch stellt diese Klasse keine Dienste dar, die auf mehreren Systemen gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="7fe2d-106">A System can host many services, however this class does not represent services hosted across multiple systems.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fe2d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7fe2d-107">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_HostedService : CIM_HostedDependency
{
  CIM_System  REF Antecedent;
  CIM_Service REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="7fe2d-108">Member</span><span class="sxs-lookup"><span data-stu-id="7fe2d-108">Members</span></span>

<span data-ttu-id="7fe2d-109">Die CIM-Klasse " **\_ hustedservice** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="7fe2d-109">The **CIM\_HostedService** class has these types of members:</span></span>

-   [<span data-ttu-id="7fe2d-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7fe2d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7fe2d-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7fe2d-111">Properties</span></span>

<span data-ttu-id="7fe2d-112">Die CIM-Klasse " **\_ hustedservice** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7fe2d-112">The **CIM\_HostedService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7fe2d-113">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="7fe2d-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fe2d-114">Datentyp: **CIM- \_ System**</span><span class="sxs-lookup"><span data-stu-id="7fe2d-114">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="7fe2d-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7fe2d-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fe2d-116">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="7fe2d-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="7fe2d-117">Das Host System.</span><span class="sxs-lookup"><span data-stu-id="7fe2d-117">The hosting System.</span></span>

</dd> <dt>

<span data-ttu-id="7fe2d-118">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="7fe2d-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fe2d-119">Datentyp: **CIM- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="7fe2d-119">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="7fe2d-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7fe2d-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fe2d-121">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig"), [**schwach**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7fe2d-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7fe2d-122">Der auf dem System gehostete Dienst.</span><span class="sxs-lookup"><span data-stu-id="7fe2d-122">The Service hosted on the System.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7fe2d-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7fe2d-123">Requirements</span></span>



| <span data-ttu-id="7fe2d-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7fe2d-124">Requirement</span></span> | <span data-ttu-id="7fe2d-125">Wert</span><span class="sxs-lookup"><span data-stu-id="7fe2d-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fe2d-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7fe2d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7fe2d-127">Windows 8</span><span class="sxs-lookup"><span data-stu-id="7fe2d-127">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="7fe2d-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7fe2d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7fe2d-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7fe2d-129">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="7fe2d-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="7fe2d-130">Namespace</span></span><br/>                | <span data-ttu-id="7fe2d-131">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="7fe2d-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7fe2d-132">MOF</span><span class="sxs-lookup"><span data-stu-id="7fe2d-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7fe2d-133"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7fe2d-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7fe2d-134">DLL</span><span class="sxs-lookup"><span data-stu-id="7fe2d-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7fe2d-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7fe2d-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7fe2d-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7fe2d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fe2d-137">**CIM- \_ hubabhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="7fe2d-137">**CIM\_HostedDependency**</span></span>](cim-hosteddependency.md)
</dt> </dl>

 

