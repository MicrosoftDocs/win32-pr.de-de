---
description: Stellt die Definition einer Metrik dar, die von einem anderen Metrikwert abgeleitet ist. Ein CIM \_ aggregationmetricdefinition-Objekt muss den CIM \_ managedelta-Objekten zugeordnet werden, auf die es angewendet wird.
ms.assetid: 0059bfd6-ecf3-41f0-be6b-0ce46dfbbb18
title: CIM_AggregationMetricDefinition-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AggregationMetricDefinition
- CIM_AggregationMetricDefinition.ChangeType
- CIM_AggregationMetricDefinition.SimpleFunction
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9a84eed5a725ebff3b39ca92bab530ef90cfca58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755448"
---
# <a name="cim_aggregationmetricdefinition-class"></a><span data-ttu-id="115c7-104">CIM \_ aggregationmetricdefinition-Klasse</span><span class="sxs-lookup"><span data-stu-id="115c7-104">CIM\_AggregationMetricDefinition class</span></span>

<span data-ttu-id="115c7-105">Stellt die Definition einer Metrik dar, die von einem anderen Metrikwert abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="115c7-105">Represents the definition of a metric that is derived from another metric value.</span></span> <span data-ttu-id="115c7-106">Ein **CIM \_ aggregationmetricdefinition** -Objekt muss den **CIM \_ managedelta** -Objekten zugeordnet werden, auf die es angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="115c7-106">A **CIM\_AggregationMetricDefinition** object should be associated with the **CIM\_ManagedElement** objects to which it applies.</span></span>

## <a name="syntax"></a><span data-ttu-id="115c7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="115c7-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_AggregationMetricDefinition : CIM_BaseMetricDefinition
{
  uint16 ChangeType = 5;
  uint16 SimpleFunction;
};
```

## <a name="members"></a><span data-ttu-id="115c7-108">Member</span><span class="sxs-lookup"><span data-stu-id="115c7-108">Members</span></span>

<span data-ttu-id="115c7-109">Die **CIM \_ aggregationmetricdefinition** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="115c7-109">The **CIM\_AggregationMetricDefinition** class has these types of members:</span></span>

-   [<span data-ttu-id="115c7-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="115c7-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="115c7-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="115c7-111">Properties</span></span>

<span data-ttu-id="115c7-112">Die **CIM \_ aggregationmetricdefinition** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="115c7-112">The **CIM\_AggregationMetricDefinition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="115c7-113">**ChangeType**</span><span class="sxs-lookup"><span data-stu-id="115c7-113">**ChangeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="115c7-114">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="115c7-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="115c7-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="115c7-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="115c7-116">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("ChangeType"), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ aggregationmetricdefinition**".**Iscontinuous**")</span><span class="sxs-lookup"><span data-stu-id="115c7-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ChangeType"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AggregationMetricDefinition**.**IsContinuous**")</span></span>
</dt> </dl>

<span data-ttu-id="115c7-117">Gibt an, wie sich der Metrikwert mithilfe allgemeiner Attribute ändert, wie z. b. Richtungsänderung, Mindest-und Höchstwerte und Wrapping Semantik.</span><span class="sxs-lookup"><span data-stu-id="115c7-117">Indicates how the metric value changes using common attributes such as direction change, minimum and maximum values, and wrapping semantics.</span></span>

<dt>

<span id="Simple_Function"></span><span id="simple_function"></span><span id="SIMPLE_FUNCTION"></span>

<span data-ttu-id="115c7-118">**Einfache Funktion** (5)</span><span class="sxs-lookup"><span data-stu-id="115c7-118">**Simple Function** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="115c7-119">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="115c7-119">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="115c7-120">**Anbieter reserviert** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="115c7-120">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="115c7-121">**Simplefunction**</span><span class="sxs-lookup"><span data-stu-id="115c7-121">**SimpleFunction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="115c7-122">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="115c7-122">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="115c7-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="115c7-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="115c7-124">Die grundlegende Berechnung für eine zugrunde liegende Metrik, die auf den Wert dieser abgeleiteten Metrik ankommt.</span><span class="sxs-lookup"><span data-stu-id="115c7-124">The basic computation performed on an underlying metric to arrive at the value of this derived metric.</span></span> <span data-ttu-id="115c7-125">Diese Eigenschaft ist **null** , wenn die **ChangeType** -Eigenschaft einen anderen Wert als "5" (einfache Funktion) aufweist.</span><span class="sxs-lookup"><span data-stu-id="115c7-125">This property is **NULL** when the **ChangeType** property has a value other than "5" (Simple Function).</span></span>

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="115c7-126"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="115c7-126"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>

<span data-ttu-id="115c7-127"><span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>**Minimal** (2)</span><span class="sxs-lookup"><span data-stu-id="115c7-127"><span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>**Minimum** (2)</span></span>


</dt> <dd>

<span data-ttu-id="115c7-128">Die Metrik meldet den niedrigsten für die zugeordneten überwachten Entität erkannten Wert.</span><span class="sxs-lookup"><span data-stu-id="115c7-128">The metric reports the lowest value detected for the associated monitored entity.</span></span> <span data-ttu-id="115c7-129">Dies wird auch als niedrige Grenze bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="115c7-129">This is also known as a low watermark.</span></span>

</dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span data-ttu-id="115c7-130"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Maximum** (3)</span><span class="sxs-lookup"><span data-stu-id="115c7-130"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Maximum** (3)</span></span>


</dt> <dd>

<span data-ttu-id="115c7-131">Die Metrik meldet den maximal für die zugeordneten überwachten Entität erkannten Wert.</span><span class="sxs-lookup"><span data-stu-id="115c7-131">The metric reports the maximum value detected for the associated monitored entity.</span></span> <span data-ttu-id="115c7-132">Dies wird auch als hohes Wasserzeichen bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="115c7-132">This is also known as a high watermark.</span></span>

</dd> <dt>

<span id="Average"></span><span id="average"></span><span id="AVERAGE"></span>

<span data-ttu-id="115c7-133"><span id="Average"></span><span id="average"></span><span id="AVERAGE"></span>**Durchschnitt** (4)</span><span class="sxs-lookup"><span data-stu-id="115c7-133"><span id="Average"></span><span id="average"></span><span id="AVERAGE"></span>**Average** (4)</span></span>


</dt> <dd>

<span data-ttu-id="115c7-134">Die Metrik meldet den durchschnittlichen Wert der zugrunde liegenden Metrikwerte.</span><span class="sxs-lookup"><span data-stu-id="115c7-134">The metric reports the average value of the underlying metric values.</span></span>

</dd> <dt>

<span id="Median"></span><span id="median"></span><span id="MEDIAN"></span>

<span data-ttu-id="115c7-135"><span id="Median"></span><span id="median"></span><span id="MEDIAN"></span>**Median** (5)</span><span class="sxs-lookup"><span data-stu-id="115c7-135"><span id="Median"></span><span id="median"></span><span id="MEDIAN"></span>**Median** (5)</span></span>


</dt> <dd>

<span data-ttu-id="115c7-136">Die Metrik meldet den Medianwert der zugrunde liegenden Metrikwerte.</span><span class="sxs-lookup"><span data-stu-id="115c7-136">The metric reports the median value of the underlying metric values.</span></span>

</dd> <dt>

<span id="Mode"></span><span id="mode"></span><span id="MODE"></span>

<span data-ttu-id="115c7-137"><span id="Mode"></span><span id="mode"></span><span id="MODE"></span>**Modus** (6)</span><span class="sxs-lookup"><span data-stu-id="115c7-137"><span id="Mode"></span><span id="mode"></span><span id="MODE"></span>**Mode** (6)</span></span>


</dt> <dd>

<span data-ttu-id="115c7-138">die Metrik meldet den modalen Wert der zugrunde liegenden Metrikwerte.</span><span class="sxs-lookup"><span data-stu-id="115c7-138">the metric reports the modal value of the underlying metric values.</span></span>

</dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="115c7-139"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Anbieter reserviert** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="115c7-139"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="115c7-140"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="115c7-140"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="115c7-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="115c7-141">Requirements</span></span>



| <span data-ttu-id="115c7-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="115c7-142">Requirement</span></span> | <span data-ttu-id="115c7-143">Wert</span><span class="sxs-lookup"><span data-stu-id="115c7-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="115c7-144">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="115c7-144">Minimum supported client</span></span><br/> | <span data-ttu-id="115c7-145">Windows 8</span><span class="sxs-lookup"><span data-stu-id="115c7-145">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="115c7-146">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="115c7-146">Minimum supported server</span></span><br/> | <span data-ttu-id="115c7-147">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="115c7-147">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="115c7-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="115c7-148">Namespace</span></span><br/>                | <span data-ttu-id="115c7-149">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="115c7-149">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="115c7-150">MOF</span><span class="sxs-lookup"><span data-stu-id="115c7-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="115c7-151"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="115c7-151"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="115c7-152">DLL</span><span class="sxs-lookup"><span data-stu-id="115c7-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="115c7-153"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="115c7-153"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="115c7-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="115c7-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="115c7-155">**CIM- \_ basemetricdefinition**</span><span class="sxs-lookup"><span data-stu-id="115c7-155">**CIM\_BaseMetricDefinition**</span></span>](cim-basemetricdefinition.md)
</dt> </dl>

 

