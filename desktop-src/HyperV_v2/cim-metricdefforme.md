---
description: Stellt eine Zuordnung dar, in der ein CIM \_ basemetricdefinition-Objekt Metriken für ein verwaltetes Element definiert.
ms.assetid: 10905038-fc23-4018-bae8-f336e4f001e7
title: CIM_MetricDefForME-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricDefForME
- CIM_MetricDefForME.Antecedent
- CIM_MetricDefForME.Dependent
- CIM_MetricDefForME.MetricCollectionEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d0bcc115bdb5d501567223a307dd30e62f624214
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866419"
---
# <a name="cim_metricdefforme-class"></a><span data-ttu-id="106e7-103">CIM- \_ metricdefforme-Klasse</span><span class="sxs-lookup"><span data-stu-id="106e7-103">CIM\_MetricDefForME class</span></span>

<span data-ttu-id="106e7-104">Stellt eine Zuordnung dar, in der ein [**CIM \_ basemetricdefinition**](cim-basemetricdefinition.md) -Objekt Metriken für ein verwaltetes Element definiert.</span><span class="sxs-lookup"><span data-stu-id="106e7-104">Represents an association in which a [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) object defines metrics for a managed element.</span></span>

## <a name="syntax"></a><span data-ttu-id="106e7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="106e7-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.22.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_MetricDefForME : CIM_Dependency
{
  CIM_ManagedElement       REF Antecedent;
  CIM_BaseMetricDefinition REF Dependent;
  uint16                       MetricCollectionEnabled = 2;
};
```

## <a name="members"></a><span data-ttu-id="106e7-106">Member</span><span class="sxs-lookup"><span data-stu-id="106e7-106">Members</span></span>

<span data-ttu-id="106e7-107">Die **CIM- \_ metricdefforme** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="106e7-107">The **CIM\_MetricDefForME** class has these types of members:</span></span>

-   [<span data-ttu-id="106e7-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="106e7-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="106e7-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="106e7-109">Properties</span></span>

<span data-ttu-id="106e7-110">Die **CIM- \_ metricdefforme** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="106e7-110">The **CIM\_MetricDefForME** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="106e7-111">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="106e7-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="106e7-112">Datentyp: **CIM \_ managedelta**</span><span class="sxs-lookup"><span data-stu-id="106e7-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="106e7-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="106e7-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="106e7-114">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="106e7-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="106e7-115">Das verwaltete Element, das der metrikdefinition zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="106e7-115">The managed element that is associated with the metric definition.</span></span>

</dd> <dt>

<span data-ttu-id="106e7-116">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="106e7-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="106e7-117">Datentyp: **CIM \_ basemetricdefinition**</span><span class="sxs-lookup"><span data-stu-id="106e7-117">Data type: **CIM\_BaseMetricDefinition**</span></span>
</dt> <dt>

<span data-ttu-id="106e7-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="106e7-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="106e7-119">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="106e7-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="106e7-120">Die metrikdefinition, die dem verwalteten Element zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="106e7-120">The metric definition that is associated with the managed element.</span></span>

</dd> <dt>

<span data-ttu-id="106e7-121">**Metriccollectionaktivierte**</span><span class="sxs-lookup"><span data-stu-id="106e7-121">**MetricCollectionEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="106e7-122">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="106e7-122">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="106e7-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="106e7-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="106e7-124">Gibt an, ob die Metrik für das verwaltete Element erfasst wird.</span><span class="sxs-lookup"><span data-stu-id="106e7-124">Indicates whether the metric is being collected for the managed element.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="106e7-125">**Aktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="106e7-125">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="106e7-126">**Deaktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="106e7-126">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="106e7-127">**Reserviert** (4)</span><span class="sxs-lookup"><span data-stu-id="106e7-127">**Reserved** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="106e7-128">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="106e7-128">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="106e7-129">**Anbieter reserviert** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="106e7-129">**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="106e7-130"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="106e7-130"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="106e7-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="106e7-131">Requirements</span></span>



| <span data-ttu-id="106e7-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="106e7-132">Requirement</span></span> | <span data-ttu-id="106e7-133">Wert</span><span class="sxs-lookup"><span data-stu-id="106e7-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="106e7-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="106e7-134">Minimum supported client</span></span><br/> | <span data-ttu-id="106e7-135">Windows 8</span><span class="sxs-lookup"><span data-stu-id="106e7-135">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="106e7-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="106e7-136">Minimum supported server</span></span><br/> | <span data-ttu-id="106e7-137">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="106e7-137">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="106e7-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="106e7-138">Namespace</span></span><br/>                | <span data-ttu-id="106e7-139">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="106e7-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="106e7-140">MOF</span><span class="sxs-lookup"><span data-stu-id="106e7-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="106e7-141"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="106e7-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="106e7-142">DLL</span><span class="sxs-lookup"><span data-stu-id="106e7-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="106e7-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="106e7-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="106e7-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="106e7-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="106e7-145">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="106e7-145">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

