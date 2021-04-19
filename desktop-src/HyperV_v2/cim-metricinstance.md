---
description: Stellt eine Zuordnung zwischen einer Instanz eines metrikwerts und einer metrikdefinition dar.
ms.assetid: 4c620a7a-8b15-49ad-ae84-246e2fca175d
title: CIM_MetricInstance-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricInstance
- CIM_MetricInstance.Antecedent
- CIM_MetricInstance.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: defba85f46e037c226a96cfaa8ffac44b99244f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359127"
---
# <a name="cim_metricinstance-class"></a><span data-ttu-id="f4091-103">CIM \_ metricinstance-Klasse</span><span class="sxs-lookup"><span data-stu-id="f4091-103">CIM\_MetricInstance class</span></span>

<span data-ttu-id="f4091-104">Stellt eine Zuordnung zwischen einer Instanz eines metrikwerts und einer metrikdefinition dar.</span><span class="sxs-lookup"><span data-stu-id="f4091-104">Represents an association between an instance of a metric value and a metric definition.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4091-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f4091-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.7.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_MetricInstance : CIM_Dependency
{
  CIM_BaseMetricDefinition REF Antecedent;
  CIM_BaseMetricValue      REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="f4091-106">Member</span><span class="sxs-lookup"><span data-stu-id="f4091-106">Members</span></span>

<span data-ttu-id="f4091-107">Die **CIM \_ metricinstance** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f4091-107">The **CIM\_MetricInstance** class has these types of members:</span></span>

-   [<span data-ttu-id="f4091-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f4091-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f4091-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f4091-109">Properties</span></span>

<span data-ttu-id="f4091-110">Die **CIM \_ metricinstance** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f4091-110">The **CIM\_MetricInstance** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f4091-111">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="f4091-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4091-112">Datentyp: **CIM \_ basemetricdefinition**</span><span class="sxs-lookup"><span data-stu-id="f4091-112">Data type: **CIM\_BaseMetricDefinition**</span></span>
</dt> <dt>

<span data-ttu-id="f4091-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f4091-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4091-114">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="f4091-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="f4091-115">Die Definition des metrikwerts.</span><span class="sxs-lookup"><span data-stu-id="f4091-115">The definition of the metric value.</span></span>

</dd> <dt>

<span data-ttu-id="f4091-116">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="f4091-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4091-117">Datentyp: **CIM \_ basemetricvalue**</span><span class="sxs-lookup"><span data-stu-id="f4091-117">Data type: **CIM\_BaseMetricValue**</span></span>
</dt> <dt>

<span data-ttu-id="f4091-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f4091-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4091-119">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="f4091-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="f4091-120">Der Metrikwert, der der metrikdefinition zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f4091-120">The metric value that is associated with the metric definition.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f4091-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f4091-121">Requirements</span></span>



| <span data-ttu-id="f4091-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f4091-122">Requirement</span></span> | <span data-ttu-id="f4091-123">Wert</span><span class="sxs-lookup"><span data-stu-id="f4091-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4091-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f4091-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f4091-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="f4091-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="f4091-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f4091-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f4091-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f4091-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="f4091-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="f4091-128">Namespace</span></span><br/>                | <span data-ttu-id="f4091-129">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="f4091-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f4091-130">MOF</span><span class="sxs-lookup"><span data-stu-id="f4091-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f4091-131"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f4091-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f4091-132">DLL</span><span class="sxs-lookup"><span data-stu-id="f4091-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f4091-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f4091-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f4091-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f4091-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4091-135">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="f4091-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

