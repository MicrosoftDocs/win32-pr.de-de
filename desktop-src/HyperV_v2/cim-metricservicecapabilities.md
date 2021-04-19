---
description: Beschreibt die Funktionen eines CIM \_ metricservice-Objekts.
ms.assetid: 3b4da02f-5298-46d4-876c-404baca38c03
title: CIM_MetricServiceCapabilities-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricServiceCapabilities
- CIM_MetricServiceCapabilities.ControllableMetrics
- CIM_MetricServiceCapabilities.MetricsControlTypes
- CIM_MetricServiceCapabilities.ControllableManagedElements
- CIM_MetricServiceCapabilities.ManagedElementControlTypes
- CIM_MetricServiceCapabilities.SupportedMethods
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f878cb0e616cb710a33d350df866160fc0eebb83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363529"
---
# <a name="cim_metricservicecapabilities-class"></a><span data-ttu-id="305e8-103">CIM \_ metricservicecapabili-Klasse</span><span class="sxs-lookup"><span data-stu-id="305e8-103">CIM\_MetricServiceCapabilities class</span></span>

<span data-ttu-id="305e8-104">Beschreibt die Funktionen eines [**CIM \_ metricservice**](cim-metricservice.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="305e8-104">Describes the capabilities of a [**CIM\_MetricService**](cim-metricservice.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="305e8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="305e8-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Metrics::BaseMetrics"), AMENDMENT]
class CIM_MetricServiceCapabilities : CIM_EnabledLogicalElementCapabilities
{
  string ControllableMetrics[];
  uint16 MetricsControlTypes[];
  string ControllableManagedElements[];
  uint16 ManagedElementControlTypes[];
  uint16 SupportedMethods[];
};
```

## <a name="members"></a><span data-ttu-id="305e8-106">Member</span><span class="sxs-lookup"><span data-stu-id="305e8-106">Members</span></span>

<span data-ttu-id="305e8-107">Die **CIM \_ metricservicecapabili-** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="305e8-107">The **CIM\_MetricServiceCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="305e8-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="305e8-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="305e8-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="305e8-109">Properties</span></span>

<span data-ttu-id="305e8-110">Die **CIM \_ metricservicecapabili-** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="305e8-110">The **CIM\_MetricServiceCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="305e8-111">**Controllablemanagedelements**</span><span class="sxs-lookup"><span data-stu-id="305e8-111">**ControllableManagedElements**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="305e8-112">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="305e8-112">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="305e8-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="305e8-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="305e8-114">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ metricservicecapabili.\*\*\*\*Managedelta Message Controller Types**")</span><span class="sxs-lookup"><span data-stu-id="305e8-114">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MetricServiceCapabilities**.**ManagedElementControlTypes**")</span></span>
</dt> </dl>

<span data-ttu-id="305e8-115">Ein Array, das Bezeichner der [**CIM- \_ managedelta**](cim-managedelement.md) -Instanzen enthält, die vom metrikdienst gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="305e8-115">An array that contains identifiers of the [**CIM\_ManagedElement**](cim-managedelement.md) instances that are controlled by the metric service.</span></span> <span data-ttu-id="305e8-116">Die Bezeichner müssen als Web-Based Enterprise Management (WBEM)-URIs formatiert sein.</span><span class="sxs-lookup"><span data-stu-id="305e8-116">The identifiers must be formatted as Web-Based Enterprise Management (WBEM) URIs.</span></span> <span data-ttu-id="305e8-117">Um diese Eigenschaft verwenden zu können, muss der metrikdienst das Aktivieren oder Deaktivieren von mindestens einer Metrik unterstützen, die für die **CIM- \_ managedelements** -Instanz definiert ist.</span><span class="sxs-lookup"><span data-stu-id="305e8-117">In order to use this property, the metric service must support enabling or disabling at least one metric that is defined for the **CIM\_ManagedElement** instance.</span></span>

</dd> <dt>

<span data-ttu-id="305e8-118">**Controllablemetrics**</span><span class="sxs-lookup"><span data-stu-id="305e8-118">**ControllableMetrics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="305e8-119">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="305e8-119">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="305e8-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="305e8-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="305e8-121">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ metricservicecapabili.\*\*\*\*Metriccontroltypes**")</span><span class="sxs-lookup"><span data-stu-id="305e8-121">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MetricServiceCapabilities**.**MetricControlTypes**")</span></span>
</dt> </dl>

<span data-ttu-id="305e8-122">Ein Array, das Bezeichner der [**CIM \_ basemetricdefinition**](cim-basemetricdefinition.md) enthält, die die vom metrikdienst verwalteten Metriken definiert.</span><span class="sxs-lookup"><span data-stu-id="305e8-122">An array that contains identifiers of the [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) that defines the metrics that are managed by the metric service.</span></span> <span data-ttu-id="305e8-123">Die Bezeichner müssen als Web-Based Enterprise Management (WBEM)-URIs formatiert sein.</span><span class="sxs-lookup"><span data-stu-id="305e8-123">The identifiers must be formatted as Web-Based Enterprise Management (WBEM) URIs.</span></span>

<span data-ttu-id="305e8-124">Um diese Eigenschaft zu verwenden, muss eine [**CIM \_ basemetricdefinition**](cim-basemetricdefinition.md) -Instanz über die [**CIM \_ serviceaffectselements**](cim-serviceaffectselement.md) -Klasse einer [**CIM- \_ metricservice**](cim-metricservice.md) -Instanz zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="305e8-124">In order to use this property, a [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) instance must be associated with a [**CIM\_MetricService**](cim-metricservice.md) instance through the [**CIM\_ServiceAffectsElement**](cim-serviceaffectselement.md) class.</span></span> <span data-ttu-id="305e8-125">Außerdem muss der metrikdienst das Aktivieren oder Deaktivieren von mindestens einer Metrik unterstützen, die von der **CIM \_ basemetricdefinition** -Instanz definiert wird.</span><span class="sxs-lookup"><span data-stu-id="305e8-125">In addition the metric service must support enabling or disabling at least one metric that is defined by the **CIM\_BaseMetricDefinition** instance.</span></span>

</dd> <dt>

<span data-ttu-id="305e8-126">**Managedelta Type Controller Types**</span><span class="sxs-lookup"><span data-stu-id="305e8-126">**ManagedElementControlTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="305e8-127">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="305e8-127">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="305e8-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="305e8-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="305e8-129">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ metricservicecapabili.\*\*\*\*Controllablemanagedelements**")</span><span class="sxs-lookup"><span data-stu-id="305e8-129">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MetricServiceCapabilities**.**ControllableManagedElements**")</span></span>
</dt> </dl>

<span data-ttu-id="305e8-130">Ein Array, das die Steuerelement Typen angibt, die vom metrikdienst für die verwalteten Elemente im **Steuerelement "controllablemanagedelements** " unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="305e8-130">An array that indicates the control types that are supported by the metric service for the managed elements in the **ControllableManagedElements** array.</span></span> <span data-ttu-id="305e8-131">Dieses Array entspricht dem **controllablemanagedelements** -Array.</span><span class="sxs-lookup"><span data-stu-id="305e8-131">This array corresponds to the **ControllableManagedElements** array.</span></span> <span data-ttu-id="305e8-132">Die Steuerelement Typen in diesem Array sind über das Steuerelement " **controllablemanagedelements** " mit Metriken verknüpft.</span><span class="sxs-lookup"><span data-stu-id="305e8-132">The control types in this array are associated with metrics through the **ControllableManagedElements** array.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="305e8-133">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="305e8-133">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Discrete"></span><span id="discrete"></span><span id="DISCRETE"></span>

<span data-ttu-id="305e8-134">**Diskret** (2)</span><span class="sxs-lookup"><span data-stu-id="305e8-134">**Discrete** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Bulk"></span><span id="bulk"></span><span id="BULK"></span>

<span data-ttu-id="305e8-135">**Massen** Vorgang (3)</span><span class="sxs-lookup"><span data-stu-id="305e8-135">**Bulk** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Both"></span><span id="both"></span><span id="BOTH"></span>

<span data-ttu-id="305e8-136">**Beides** (4)</span><span class="sxs-lookup"><span data-stu-id="305e8-136">**Both** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="305e8-137">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="305e8-137">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="305e8-138">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="305e8-138">**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="305e8-139">**Metricscontroltypes**</span><span class="sxs-lookup"><span data-stu-id="305e8-139">**MetricsControlTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="305e8-140">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="305e8-140">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="305e8-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="305e8-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="305e8-142">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ metricservicecapabili.\*\*\*\*Controllablemetrics**")</span><span class="sxs-lookup"><span data-stu-id="305e8-142">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MetricServiceCapabilities**.**ControllableMetrics**")</span></span>
</dt> </dl>

<span data-ttu-id="305e8-143">Ein Array, das die Steuerelement Typen angibt, die vom metrikdienst unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="305e8-143">An array that indicates the control types that are supported by the metric service.</span></span> <span data-ttu-id="305e8-144">Dieses Array entspricht dem **controllablemetrics** -Array.</span><span class="sxs-lookup"><span data-stu-id="305e8-144">This array corresponds to the **ControllableMetrics** array.</span></span> <span data-ttu-id="305e8-145">Die Steuerelement Typen in diesem Array werden Metriken über das **controllablemetrics** -Array zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="305e8-145">The control types in this array are associated with metrics through the **ControllableMetrics** array.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="305e8-146">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="305e8-146">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Discrete"></span><span id="discrete"></span><span id="DISCRETE"></span>

<span data-ttu-id="305e8-147">**Diskret** (2)</span><span class="sxs-lookup"><span data-stu-id="305e8-147">**Discrete** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Bulk"></span><span id="bulk"></span><span id="BULK"></span>

<span data-ttu-id="305e8-148">**Massen** Vorgang (3)</span><span class="sxs-lookup"><span data-stu-id="305e8-148">**Bulk** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Both"></span><span id="both"></span><span id="BOTH"></span>

<span data-ttu-id="305e8-149">**Beides** (4)</span><span class="sxs-lookup"><span data-stu-id="305e8-149">**Both** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="305e8-150">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="305e8-150">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="305e8-151">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="305e8-151">**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="305e8-152">**SupportedMethods**</span><span class="sxs-lookup"><span data-stu-id="305e8-152">**SupportedMethods**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="305e8-153">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="305e8-153">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="305e8-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="305e8-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="305e8-155">Ein Array, das die Namen der Methoden enthält, die vom metrikdienst unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="305e8-155">An array that contains names of methods that are supported by the metric service.</span></span>

<dt>

<span id="ControlMetrics"></span><span id="controlmetrics"></span><span id="CONTROLMETRICS"></span>

<span data-ttu-id="305e8-156">**Controlmetrics** (2)</span><span class="sxs-lookup"><span data-stu-id="305e8-156">**ControlMetrics** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="ControlMetricsByClass"></span><span id="controlmetricsbyclass"></span><span id="CONTROLMETRICSBYCLASS"></span>

<span data-ttu-id="305e8-157">**Controlmetricsbyclass** (3)</span><span class="sxs-lookup"><span data-stu-id="305e8-157">**ControlMetricsByClass** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ShowMetrics"></span><span id="showmetrics"></span><span id="SHOWMETRICS"></span>

<span data-ttu-id="305e8-158">**Showmetrics** (4)</span><span class="sxs-lookup"><span data-stu-id="305e8-158">**ShowMetrics** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="ShowMetricsByClass"></span><span id="showmetricsbyclass"></span><span id="SHOWMETRICSBYCLASS"></span>

<span data-ttu-id="305e8-159">**Showmetricsbyclass** (5)</span><span class="sxs-lookup"><span data-stu-id="305e8-159">**ShowMetricsByClass** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="GetMetricValues"></span><span id="getmetricvalues"></span><span id="GETMETRICVALUES"></span>

<span data-ttu-id="305e8-160">**Getmetricvalues** (6)</span><span class="sxs-lookup"><span data-stu-id="305e8-160">**GetMetricValues** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="ControlSampleTimes"></span><span id="controlsampletimes"></span><span id="CONTROLSAMPLETIMES"></span>

<span data-ttu-id="305e8-161">**Controlsampletimes** (7)</span><span class="sxs-lookup"><span data-stu-id="305e8-161">**ControlSampleTimes** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="305e8-162">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="305e8-162">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="305e8-163">**Hersteller spezifisch** (0X8000..)</span><span class="sxs-lookup"><span data-stu-id="305e8-163">**Vendor Specific** (0x8000..)</span></span>


<span data-ttu-id="305e8-164"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="305e8-164"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="305e8-165">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="305e8-165">Requirements</span></span>



| <span data-ttu-id="305e8-166">Anforderung</span><span class="sxs-lookup"><span data-stu-id="305e8-166">Requirement</span></span> | <span data-ttu-id="305e8-167">Wert</span><span class="sxs-lookup"><span data-stu-id="305e8-167">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="305e8-168">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="305e8-168">Minimum supported client</span></span><br/> | <span data-ttu-id="305e8-169">Windows 8</span><span class="sxs-lookup"><span data-stu-id="305e8-169">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="305e8-170">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="305e8-170">Minimum supported server</span></span><br/> | <span data-ttu-id="305e8-171">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="305e8-171">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="305e8-172">Namespace</span><span class="sxs-lookup"><span data-stu-id="305e8-172">Namespace</span></span><br/>                | <span data-ttu-id="305e8-173">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="305e8-173">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="305e8-174">MOF</span><span class="sxs-lookup"><span data-stu-id="305e8-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="305e8-175"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="305e8-175"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="305e8-176">DLL</span><span class="sxs-lookup"><span data-stu-id="305e8-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="305e8-177"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="305e8-177"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="305e8-178">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="305e8-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="305e8-179">**CIM \_ enabledlogicalelementfunktionalitäten**</span><span class="sxs-lookup"><span data-stu-id="305e8-179">**CIM\_EnabledLogicalElementCapabilities**</span></span>](cim-enabledlogicalelementcapabilities.md)
</dt> </dl>

 

