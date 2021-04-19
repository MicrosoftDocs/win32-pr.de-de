---
description: Stellt eine generische Zuordnung dar, in der ein verwaltetes Element von einem anderen abhängig ist. CIM- \_ Unterklassen-CIM- \_ Abhängigkeit, um eine konkrete Klassen Version der CIM-Abhängigkeit bereitzustellen \_ .
ms.assetid: c0e1527d-d350-410d-9b5f-c9d4dedf7393
title: CIM_ConcreteDependency-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConcreteDependency
- CIM_ConcreteDependency.Antecedent
- CIM_ConcreteDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 253f57b1fd29c3844f0e87d488974ced7bec98bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355284"
---
# <a name="cim_concretedependency-class"></a><span data-ttu-id="4a362-104">CIM- \_ Klasse "concretedepeng</span><span class="sxs-lookup"><span data-stu-id="4a362-104">CIM\_ConcreteDependency class</span></span>

<span data-ttu-id="4a362-105">Stellt eine generische Zuordnung dar, in der ein verwaltetes Element von einem anderen abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="4a362-105">Represents a generic association in which a managed element depends on another.</span></span> <span data-ttu-id="4a362-106">**CIM \_ Konkrete Unterklassen** - [**CIM- \_ Abhängigkeit**](cim-dependency.md) , um eine konkrete Klassen Version der **CIM- \_ Abhängigkeit** bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="4a362-106">**CIM\_ConcreteDependency** subclasses [**CIM\_Dependency**](cim-dependency.md) to provide a concrete class version of **CIM\_Dependency**.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a362-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a362-107">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_ConcreteDependency : CIM_Dependency
{
  CIM_ManagedElement REF Antecedent;
  CIM_ManagedElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="4a362-108">Member</span><span class="sxs-lookup"><span data-stu-id="4a362-108">Members</span></span>

<span data-ttu-id="4a362-109">Die CIM-Klasse " **\_ concretedependenz** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="4a362-109">The **CIM\_ConcreteDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="4a362-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4a362-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4a362-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4a362-111">Properties</span></span>

<span data-ttu-id="4a362-112">Die CIM-Klasse " **\_ concretedepen"** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4a362-112">The **CIM\_ConcreteDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4a362-113">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="4a362-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a362-114">Datentyp: **CIM \_ managedelta**</span><span class="sxs-lookup"><span data-stu-id="4a362-114">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="4a362-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4a362-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4a362-116">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="4a362-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="4a362-117">Das unabhängige Objekt in der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="4a362-117">The independent object in the association.</span></span>

</dd> <dt>

<span data-ttu-id="4a362-118">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="4a362-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a362-119">Datentyp: **CIM \_ managedelta**</span><span class="sxs-lookup"><span data-stu-id="4a362-119">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="4a362-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4a362-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4a362-121">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="4a362-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="4a362-122">Das abhängige Objekt in der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="4a362-122">The dependent object in the association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4a362-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4a362-123">Requirements</span></span>



| <span data-ttu-id="4a362-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4a362-124">Requirement</span></span> | <span data-ttu-id="4a362-125">Wert</span><span class="sxs-lookup"><span data-stu-id="4a362-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a362-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4a362-126">Minimum supported client</span></span><br/> | <span data-ttu-id="4a362-127">Windows 8</span><span class="sxs-lookup"><span data-stu-id="4a362-127">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="4a362-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4a362-128">Minimum supported server</span></span><br/> | <span data-ttu-id="4a362-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4a362-129">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="4a362-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="4a362-130">Namespace</span></span><br/>                | <span data-ttu-id="4a362-131">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="4a362-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="4a362-132">MOF</span><span class="sxs-lookup"><span data-stu-id="4a362-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4a362-133"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="4a362-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4a362-134">DLL</span><span class="sxs-lookup"><span data-stu-id="4a362-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a362-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4a362-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4a362-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4a362-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a362-137">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="4a362-137">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

