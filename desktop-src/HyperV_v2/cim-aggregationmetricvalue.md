---
description: Stellt den Instanzwert einer Metrik dar, die durch eine Instanz von CIM \_ aggregationmetricdefinition definiert wird.
ms.assetid: 663ef18a-0238-416f-9682-8809b271b4fc
title: CIM_AggregationMetricValue-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AggregationMetricValue
- CIM_AggregationMetricValue.AggregationTimeStamp
- CIM_AggregationMetricValue.AggregationDuration
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0af264b66838e7c039ef3f99a4f365ebab55c293
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368248"
---
# <a name="cim_aggregationmetricvalue-class"></a><span data-ttu-id="19d29-103">CIM \_ aggregationmetricvalue-Klasse</span><span class="sxs-lookup"><span data-stu-id="19d29-103">CIM\_AggregationMetricValue class</span></span>

<span data-ttu-id="19d29-104">Stellt den Instanzwert einer Metrik dar, die durch eine Instanz von **CIM \_ aggregationmetricdefinition** definiert wird.</span><span class="sxs-lookup"><span data-stu-id="19d29-104">Represents the instance value of a metric defined by an instance of **CIM\_AggregationMetricDefinition**.</span></span>

## <a name="syntax"></a><span data-ttu-id="19d29-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="19d29-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_AggregationMetricValue : CIM_BaseMetricValue
{
  datetime AggregationTimeStamp;
  datetime AggregationDuration;
};
```

## <a name="members"></a><span data-ttu-id="19d29-106">Member</span><span class="sxs-lookup"><span data-stu-id="19d29-106">Members</span></span>

<span data-ttu-id="19d29-107">Die **CIM \_ aggregationmetricvalue** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="19d29-107">The **CIM\_AggregationMetricValue** class has these types of members:</span></span>

-   [<span data-ttu-id="19d29-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="19d29-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="19d29-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="19d29-109">Properties</span></span>

<span data-ttu-id="19d29-110">Die **CIM \_ aggregationmetricvalue** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="19d29-110">The **CIM\_AggregationMetricValue** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="19d29-111">**Aggregationduration**</span><span class="sxs-lookup"><span data-stu-id="19d29-111">**AggregationDuration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19d29-112">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="19d29-112">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="19d29-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="19d29-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19d29-114">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ aggregationmetricvalue**".**Aggregationtimestamp**")</span><span class="sxs-lookup"><span data-stu-id="19d29-114">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AggregationMetricValue**.**AggregationTimeStamp**")</span></span>
</dt> </dl>

<span data-ttu-id="19d29-115">Stellt die Zeitspanne dar, in der die Aggregation berechnet wurde.</span><span class="sxs-lookup"><span data-stu-id="19d29-115">Represents the time duration over which the aggregation was computed.</span></span> <span data-ttu-id="19d29-116">Der Start eines Überwachungs Intervalls, für das die Aggregations Funktion angewendet wird, wird durch Subtrahieren des **aggregationduration** -Werts vom **aggregationtimestamp** -Wert bestimmt.</span><span class="sxs-lookup"><span data-stu-id="19d29-116">The start of a monitoring interval over which the aggregation function is applied is determined by subtracting the **AggregationDuration** value from the **AggregationTimestamp** value.</span></span>

</dd> <dt>

<span data-ttu-id="19d29-117">**Aggregationtimestamp**</span><span class="sxs-lookup"><span data-stu-id="19d29-117">**AggregationTimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19d29-118">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="19d29-118">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="19d29-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="19d29-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19d29-120">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ aggregationmetricvalue**".**Dauer**")</span><span class="sxs-lookup"><span data-stu-id="19d29-120">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AggregationMetricValue**.**Duration**")</span></span>
</dt> </dl>

<span data-ttu-id="19d29-121">Der Zeitpunkt, zu dem die Aggregations Funktion angewendet wurde, um den Wert der metrikinstanz zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="19d29-121">The time when the aggregation function was applied to determine the value of the metric instance.</span></span> <span data-ttu-id="19d29-122">Dies unterscheidet sich von der Zeit, zu der die Instanz erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="19d29-122">This is different from the time when the instance is created.</span></span> <span data-ttu-id="19d29-123">Der **aggregationtimestamp** -Wert ändert sich, wenn die Aggregations Funktion angewendet wird, um den Wert zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="19d29-123">The **AggregationTimeStamp** value changes whenever the aggregation function is applied to calculate the value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="19d29-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="19d29-124">Requirements</span></span>



| <span data-ttu-id="19d29-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="19d29-125">Requirement</span></span> | <span data-ttu-id="19d29-126">Wert</span><span class="sxs-lookup"><span data-stu-id="19d29-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19d29-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="19d29-127">Minimum supported client</span></span><br/> | <span data-ttu-id="19d29-128">Windows 8</span><span class="sxs-lookup"><span data-stu-id="19d29-128">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="19d29-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="19d29-129">Minimum supported server</span></span><br/> | <span data-ttu-id="19d29-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="19d29-130">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="19d29-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="19d29-131">Namespace</span></span><br/>                | <span data-ttu-id="19d29-132">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="19d29-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="19d29-133">MOF</span><span class="sxs-lookup"><span data-stu-id="19d29-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="19d29-134"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="19d29-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="19d29-135">DLL</span><span class="sxs-lookup"><span data-stu-id="19d29-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19d29-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="19d29-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="19d29-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="19d29-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19d29-138">**CIM \_ basemetricvalue**</span><span class="sxs-lookup"><span data-stu-id="19d29-138">**CIM\_BaseMetricValue**</span></span>](cim-basemetricvalue.md)
</dt> </dl>

 

