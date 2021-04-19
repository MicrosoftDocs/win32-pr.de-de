---
description: Stellt eine Zuordnung dar, in der für ein verwaltetes Element Metrikwerte gesammelt werden.
ms.assetid: 00752751-bc27-463b-a4ac-4db8e5040077
title: CIM_MetricForME-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricForME
- CIM_MetricForME.Antecedent
- CIM_MetricForME.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 89c119ad622b778d0402100a64ff15befe623685
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356259"
---
# <a name="cim_metricforme-class"></a><span data-ttu-id="4ecdb-103">CIM- \_ metricforme-Klasse</span><span class="sxs-lookup"><span data-stu-id="4ecdb-103">CIM\_MetricForME class</span></span>

<span data-ttu-id="4ecdb-104">Stellt eine Zuordnung dar, in der für ein verwaltetes Element Metrikwerte gesammelt werden.</span><span class="sxs-lookup"><span data-stu-id="4ecdb-104">Represents an association in which a metric values are collected for a managed element.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ecdb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ecdb-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.7.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_MetricForME : CIM_Dependency
{
  CIM_ManagedElement  REF Antecedent;
  CIM_BaseMetricValue REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="4ecdb-106">Member</span><span class="sxs-lookup"><span data-stu-id="4ecdb-106">Members</span></span>

<span data-ttu-id="4ecdb-107">Die **CIM- \_ metricforme** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="4ecdb-107">The **CIM\_MetricForME** class has these types of members:</span></span>

-   [<span data-ttu-id="4ecdb-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4ecdb-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4ecdb-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4ecdb-109">Properties</span></span>

<span data-ttu-id="4ecdb-110">Die **CIM- \_ metricforme** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4ecdb-110">The **CIM\_MetricForME** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4ecdb-111">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="4ecdb-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ecdb-112">Datentyp: **CIM \_ managedelta**</span><span class="sxs-lookup"><span data-stu-id="4ecdb-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="4ecdb-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ecdb-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ecdb-114">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="4ecdb-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="4ecdb-115">Das verwaltete Element in der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="4ecdb-115">The managed element in the association.</span></span>

</dd> <dt>

<span data-ttu-id="4ecdb-116">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="4ecdb-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ecdb-117">Datentyp: **CIM \_ basemetricvalue**</span><span class="sxs-lookup"><span data-stu-id="4ecdb-117">Data type: **CIM\_BaseMetricValue**</span></span>
</dt> <dt>

<span data-ttu-id="4ecdb-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ecdb-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ecdb-119">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="4ecdb-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="4ecdb-120">Der Metrikwert in der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="4ecdb-120">The metric value in the association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4ecdb-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4ecdb-121">Requirements</span></span>



| <span data-ttu-id="4ecdb-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4ecdb-122">Requirement</span></span> | <span data-ttu-id="4ecdb-123">Wert</span><span class="sxs-lookup"><span data-stu-id="4ecdb-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ecdb-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4ecdb-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4ecdb-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="4ecdb-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="4ecdb-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4ecdb-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4ecdb-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4ecdb-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="4ecdb-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="4ecdb-128">Namespace</span></span><br/>                | <span data-ttu-id="4ecdb-129">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="4ecdb-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="4ecdb-130">MOF</span><span class="sxs-lookup"><span data-stu-id="4ecdb-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4ecdb-131"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="4ecdb-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4ecdb-132">DLL</span><span class="sxs-lookup"><span data-stu-id="4ecdb-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ecdb-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4ecdb-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4ecdb-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4ecdb-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ecdb-135">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="4ecdb-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

