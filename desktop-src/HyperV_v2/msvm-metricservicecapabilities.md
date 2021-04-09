---
description: Beschreibt die Funktionen der zugeordneten MSVM- \_ metricservice-Instanz.
ms.assetid: 4E24D675-8265-4B5E-9551-550510B138FE
title: Msvm_MetricServiceCapabilities-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricServiceCapabilities
- Msvm_MetricServiceCapabilities.InstanceID
- Msvm_MetricServiceCapabilities.Caption
- Msvm_MetricServiceCapabilities.Description
- Msvm_MetricServiceCapabilities.ElementName
- Msvm_MetricServiceCapabilities.ElementNameEditSupported
- Msvm_MetricServiceCapabilities.MaxElementNameLen
- Msvm_MetricServiceCapabilities.RequestedStatesSupported
- Msvm_MetricServiceCapabilities.ElementNameMask
- Msvm_MetricServiceCapabilities.ControllableMetrics
- Msvm_MetricServiceCapabilities.MetricsControlTypes
- Msvm_MetricServiceCapabilities.ControllableManagedElements
- Msvm_MetricServiceCapabilities.ManagedElementControlTypes
- Msvm_MetricServiceCapabilities.SupportedMethods
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 635e153d3184e74ea581a045e3d6d54a5fea199f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868500"
---
# <a name="msvm_metricservicecapabilities-class"></a><span data-ttu-id="9363c-103">MSVM \_ metricservicecapabili-Klasse</span><span class="sxs-lookup"><span data-stu-id="9363c-103">Msvm\_MetricServiceCapabilities class</span></span>

<span data-ttu-id="9363c-104">Beschreibt die Funktionen der zugeordneten [**MSVM- \_ metricservice**](msvm-metricservice.md) -Instanz.</span><span class="sxs-lookup"><span data-stu-id="9363c-104">Describes the capabilities of the associated [**Msvm\_MetricService**](msvm-metricservice.md) instance.</span></span>

<span data-ttu-id="9363c-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9363c-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9363c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9363c-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricServiceCapabilities : CIM_MetricServiceCapabilities
{
  string  InstanceID;
  string  Caption = "Hyper-V Metric Service Capabilities";
  string  Description = "Defines Hyper-V Metric Service Capabilities";
  string  ElementName = "Hyper-V Metric Service Capabilities";
  boolean ElementNameEditSupported;
  unit16  MaxElementNameLen;
  unit16  RequestedStatesSupported[];
  string  ElementNameMask;
  string  ControllableMetrics[];
  uint16  MetricsControlTypes[];
  string  ControllableManagedElements[];
  uint16  ManagedElementControlTypes[];
  uint16  SupportedMethods[];
};
```

## <a name="members"></a><span data-ttu-id="9363c-107">Member</span><span class="sxs-lookup"><span data-stu-id="9363c-107">Members</span></span>

<span data-ttu-id="9363c-108">Die **MSVM-Klasse " \_ metricservicecapabili"** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="9363c-108">The **Msvm\_MetricServiceCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="9363c-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9363c-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9363c-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9363c-110">Properties</span></span>

<span data-ttu-id="9363c-111">Die **MSVM- \_ metricservicecapabili-** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9363c-111">The **Msvm\_MetricServiceCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9363c-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="9363c-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9363c-113">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9363c-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9363c-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9363c-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9363c-115">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="9363c-115">A short description of the object.</span></span> <span data-ttu-id="9363c-116">Diese Eigenschaft wird vom [**CIM- \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Hyper-V Metric Service-Funktionen" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9363c-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Metric Service Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="9363c-117">**Controllablemanagedelements**</span><span class="sxs-lookup"><span data-stu-id="9363c-117">**ControllableManagedElements**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9363c-118">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="9363c-118">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9363c-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9363c-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9363c-120">Qualifizierer: **arrayType** ("indiziert")</span><span class="sxs-lookup"><span data-stu-id="9363c-120">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="9363c-121">Identifiziert die Instanzen von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) , die von der zugeordneten **CIM \_ metricservice** -Instanz gesteuert werden können.</span><span class="sxs-lookup"><span data-stu-id="9363c-121">Identifies the instances of [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) that can be controlled by the associated **CIM\_MetricService** instance.</span></span> <span data-ttu-id="9363c-122">Wenn diese Eigenschaft den Wert **null** hat, können alle Elemente gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="9363c-122">If this property is **Null**, all elements can be controlled.</span></span> <span data-ttu-id="9363c-123">Diese Eigenschaft wird von **CIM \_ metricservicecapabiligeerbt**.</span><span class="sxs-lookup"><span data-stu-id="9363c-123">This property is inherited from **CIM\_MetricServiceCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="9363c-124">**Controllablemetrics**</span><span class="sxs-lookup"><span data-stu-id="9363c-124">**ControllableMetrics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9363c-125">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="9363c-125">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9363c-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9363c-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9363c-127">Qualifizierer: **arrayType** ("indiziert")</span><span class="sxs-lookup"><span data-stu-id="9363c-127">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="9363c-128">Identifiziert die Instanzen von **CIM \_ basemetricdefinition** , die von der zugeordneten **CIM \_ metricservice** -Instanz gesteuert werden können.</span><span class="sxs-lookup"><span data-stu-id="9363c-128">Identifies the instances of **CIM\_BaseMetricDefinition** that can be controlled by the associated **CIM\_MetricService** instance.</span></span> <span data-ttu-id="9363c-129">Wenn diese Eigenschaft den Wert **null** hat, können alle Metriken gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="9363c-129">If this property is **Null**, all metrics can be controlled.</span></span> <span data-ttu-id="9363c-130">Diese Eigenschaft wird von **CIM \_ metricservicecapabiligeerbt**.</span><span class="sxs-lookup"><span data-stu-id="9363c-130">This property is inherited from **CIM\_MetricServiceCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="9363c-131">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9363c-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9363c-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9363c-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9363c-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9363c-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9363c-134">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="9363c-134">A description of the object.</span></span> <span data-ttu-id="9363c-135">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "definiert Hyper-V Metric Service-Funktionen" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9363c-135">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Defines Hyper-V Metric Service Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="9363c-136">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="9363c-136">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9363c-137">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9363c-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9363c-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9363c-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9363c-139">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="9363c-139">A display name for the object.</span></span> <span data-ttu-id="9363c-140">Diese Eigenschaft wird vom [**CIM- \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Hyper-V Metric Service-Funktionen" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9363c-140">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Metric Service Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="9363c-141">**Elementnameeditsupported**</span><span class="sxs-lookup"><span data-stu-id="9363c-141">**ElementNameEditSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9363c-142">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="9363c-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9363c-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9363c-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9363c-144">Gibt an, ob die **ElementName** -Eigenschaft geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="9363c-144">Indicates whether the **ElementName** property can be modified.</span></span> <span data-ttu-id="9363c-145">Diese Eigenschaft wird von **CIM \_ enabledlogicalelementfunktionalitäten** geerbt.</span><span class="sxs-lookup"><span data-stu-id="9363c-145">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="9363c-146">**Elementnamemask**</span><span class="sxs-lookup"><span data-stu-id="9363c-146">**ElementNameMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9363c-147">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9363c-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9363c-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9363c-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9363c-149">Gibt die Einschränkungen für **ElementName** an, ausgedrückt als regulärer Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="9363c-149">Specifies the restrictions on **ElementName**, expressed as a regular expression.</span></span> <span data-ttu-id="9363c-150">Diese Eigenschaft wird von **CIM \_ enabledlogicalelementfunktionalitäten** geerbt.</span><span class="sxs-lookup"><span data-stu-id="9363c-150">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="9363c-151">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9363c-151">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9363c-152">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9363c-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9363c-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9363c-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9363c-154">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="9363c-154">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="9363c-155">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="9363c-155">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="9363c-156">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9363c-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9363c-157">**Managedelta Type Controller Types**</span><span class="sxs-lookup"><span data-stu-id="9363c-157">**ManagedElementControlTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9363c-158">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="9363c-158">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9363c-159">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9363c-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9363c-160">Qualifizierer: **arrayType** ("indiziert")</span><span class="sxs-lookup"><span data-stu-id="9363c-160">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="9363c-161">Gibt den Typ des Steuer Elements an, der von der zugeordneten **CIM- \_ metricservice** -Instanz für das [**CIM- \_ managedelements**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) -Objekt unterstützt wird, das durch den Wert am selben Array Index in der Eigenschaft " **controllablemanagedelements** "</span><span class="sxs-lookup"><span data-stu-id="9363c-161">Identifies the type of control supported by the associated **CIM\_MetricService** instance for the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) object identified by the value at the same array index in the **ControllableManagedElements** property.</span></span> <span data-ttu-id="9363c-162">Wenn diese Eigenschaft **null** ist, werden alle Steuerelement Typen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9363c-162">If this property is **Null**, all control types are supported.</span></span> <span data-ttu-id="9363c-163">Diese Eigenschaft wird von **CIM \_ metricservicecapabiligeerbt**.</span><span class="sxs-lookup"><span data-stu-id="9363c-163">This property is inherited from **CIM\_MetricServiceCapabilities**.</span></span>



| <span data-ttu-id="9363c-164">Wert</span><span class="sxs-lookup"><span data-stu-id="9363c-164">Value</span></span>                                                                                   | <span data-ttu-id="9363c-165">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9363c-165">Meaning</span></span>                    |
|-----------------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="9363c-166"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9363c-166"><dt>0</dt></span></span> </dl>            | <span data-ttu-id="9363c-167">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="9363c-167">Unknown</span></span><br/>         |
| <dl> <span data-ttu-id="9363c-168"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9363c-168"><dt>2</dt></span></span> </dl>            | <span data-ttu-id="9363c-169">Discrete</span><span class="sxs-lookup"><span data-stu-id="9363c-169">Discrete</span></span><br/>        |
| <dl> <span data-ttu-id="9363c-170"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="9363c-170"><dt>3</dt></span></span> </dl>            | <span data-ttu-id="9363c-171">Massenvorgang</span><span class="sxs-lookup"><span data-stu-id="9363c-171">Bulk</span></span><br/>            |
| <dl> <span data-ttu-id="9363c-172"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="9363c-172"><dt>4</dt></span></span> </dl>            | <span data-ttu-id="9363c-173">Both</span><span class="sxs-lookup"><span data-stu-id="9363c-173">Both</span></span><br/>            |
| <dl> <span data-ttu-id="9363c-174"><dt>5.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="9363c-174"><dt>5..32767</dt></span></span> </dl>     | <span data-ttu-id="9363c-175">DMTF reserviert</span><span class="sxs-lookup"><span data-stu-id="9363c-175">DMTF reserved</span></span><br/>   |
| <dl> <span data-ttu-id="9363c-176"><dt>32768.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="9363c-176"><dt>32768..65535</dt></span></span> </dl> | <span data-ttu-id="9363c-177">Hersteller spezifisch</span><span class="sxs-lookup"><span data-stu-id="9363c-177">Vendor specific</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9363c-178">**Maxelementnamelen**</span><span class="sxs-lookup"><span data-stu-id="9363c-178">**MaxElementNameLen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9363c-179">Datentyp: **unit16**</span><span class="sxs-lookup"><span data-stu-id="9363c-179">Data type: **unit16**</span></span>
</dt> <dt>

<span data-ttu-id="9363c-180">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9363c-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9363c-181">Qualifizierer: **MaxValue** (256)</span><span class="sxs-lookup"><span data-stu-id="9363c-181">Qualifiers: **MaxValue** (256)</span></span>
</dt> </dl>

<span data-ttu-id="9363c-182">Gibt die maximal unterstützte Länge der **ElementName** -Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="9363c-182">Specifies the maximum supported length of the **ElementName** property.</span></span> <span data-ttu-id="9363c-183">Diese Eigenschaft wird von **CIM \_ enabledlogicalelementfunktionalitäten** geerbt.</span><span class="sxs-lookup"><span data-stu-id="9363c-183">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="9363c-184">**Metricscontroltypes**</span><span class="sxs-lookup"><span data-stu-id="9363c-184">**MetricsControlTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9363c-185">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="9363c-185">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9363c-186">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9363c-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9363c-187">Qualifizierer: **arrayType** ("indiziert")</span><span class="sxs-lookup"><span data-stu-id="9363c-187">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="9363c-188">Gibt den Typ des Steuer Elements an, der von der zugeordneten **CIM- \_ metricservice** -Instanz für die **CIM- \_ basemetricdefinition** unterstützt wird, die durch den Wert am selben Array Index in der **controllablemetrics** -Eigenschaft identifiziert wird</span><span class="sxs-lookup"><span data-stu-id="9363c-188">Identifies the type of control supported by the associated **CIM\_MetricService** instance for the **CIM\_BaseMetricDefinition** identified by the value at the same array index in the **ControllableMetrics** property.</span></span> <span data-ttu-id="9363c-189">Wenn diese Eigenschaft **null** ist, werden alle Steuerelement Typen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9363c-189">If this property is **Null**, all control types are supported.</span></span> <span data-ttu-id="9363c-190">Diese Eigenschaft wird von **CIM \_ metricservicecapabiligeerbt**.</span><span class="sxs-lookup"><span data-stu-id="9363c-190">This property is inherited from **CIM\_MetricServiceCapabilities**.</span></span>



| <span data-ttu-id="9363c-191">Wert</span><span class="sxs-lookup"><span data-stu-id="9363c-191">Value</span></span>                                                                                   | <span data-ttu-id="9363c-192">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9363c-192">Meaning</span></span>                    |
|-----------------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="9363c-193"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9363c-193"><dt>0</dt></span></span> </dl>            | <span data-ttu-id="9363c-194">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="9363c-194">Unknown</span></span><br/>         |
| <dl> <span data-ttu-id="9363c-195"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9363c-195"><dt>2</dt></span></span> </dl>            | <span data-ttu-id="9363c-196">Discrete</span><span class="sxs-lookup"><span data-stu-id="9363c-196">Discrete</span></span><br/>        |
| <dl> <span data-ttu-id="9363c-197"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="9363c-197"><dt>3</dt></span></span> </dl>            | <span data-ttu-id="9363c-198">Massenvorgang</span><span class="sxs-lookup"><span data-stu-id="9363c-198">Bulk</span></span><br/>            |
| <dl> <span data-ttu-id="9363c-199"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="9363c-199"><dt>4</dt></span></span> </dl>            | <span data-ttu-id="9363c-200">Both</span><span class="sxs-lookup"><span data-stu-id="9363c-200">Both</span></span><br/>            |
| <dl> <span data-ttu-id="9363c-201"><dt>5.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="9363c-201"><dt>5..32767</dt></span></span> </dl>     | <span data-ttu-id="9363c-202">DMTF reserviert</span><span class="sxs-lookup"><span data-stu-id="9363c-202">DMTF reserved</span></span><br/>   |
| <dl> <span data-ttu-id="9363c-203"><dt>32768.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="9363c-203"><dt>32768..65535</dt></span></span> </dl> | <span data-ttu-id="9363c-204">Hersteller spezifisch</span><span class="sxs-lookup"><span data-stu-id="9363c-204">Vendor specific</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9363c-205">**Requestedstaatunter stützt**</span><span class="sxs-lookup"><span data-stu-id="9363c-205">**RequestedStatesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9363c-206">Datentyp: **unit16** Array</span><span class="sxs-lookup"><span data-stu-id="9363c-206">Data type: **unit16** array</span></span>
</dt> <dt>

<span data-ttu-id="9363c-207">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9363c-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9363c-208">Gibt die möglichen Zustände an, die bei Verwendung der **requestStateChange** -Methode für das aktivierte logische Element angefordert werden können.</span><span class="sxs-lookup"><span data-stu-id="9363c-208">Indicates the possible states that can be requested when using the **RequestStateChange** method on the enabled logical element.</span></span> <span data-ttu-id="9363c-209">Diese Eigenschaft wird von **CIM \_ enabledlogicalelementfunktionalitäten** geerbt.</span><span class="sxs-lookup"><span data-stu-id="9363c-209">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>



| <span data-ttu-id="9363c-210">Wert</span><span class="sxs-lookup"><span data-stu-id="9363c-210">Value</span></span>                                                                         | <span data-ttu-id="9363c-211">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9363c-211">Meaning</span></span>              |
|-------------------------------------------------------------------------------|----------------------|
| <dl> <span data-ttu-id="9363c-212"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9363c-212"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="9363c-213">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="9363c-213">Enabled</span></span><br/>   |
| <dl> <span data-ttu-id="9363c-214"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="9363c-214"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="9363c-215">Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="9363c-215">Disables</span></span><br/>  |
| <dl> <span data-ttu-id="9363c-216"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="9363c-216"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="9363c-217">Herunterfahren</span><span class="sxs-lookup"><span data-stu-id="9363c-217">Shut Down</span></span><br/> |
| <dl> <span data-ttu-id="9363c-218"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="9363c-218"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="9363c-219">Offline</span><span class="sxs-lookup"><span data-stu-id="9363c-219">Offline</span></span><br/>   |
| <dl> <span data-ttu-id="9363c-220"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="9363c-220"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="9363c-221">Test</span><span class="sxs-lookup"><span data-stu-id="9363c-221">Test</span></span><br/>      |
| <dl> <span data-ttu-id="9363c-222"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="9363c-222"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="9363c-223">Wickeln</span><span class="sxs-lookup"><span data-stu-id="9363c-223">Defer</span></span><br/>     |
| <dl> <span data-ttu-id="9363c-224"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="9363c-224"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="9363c-225">Stilllegen</span><span class="sxs-lookup"><span data-stu-id="9363c-225">Quiesce</span></span><br/>   |
| <dl> <span data-ttu-id="9363c-226"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="9363c-226"><dt>10</dt></span></span> </dl> | <span data-ttu-id="9363c-227">Reboot</span><span class="sxs-lookup"><span data-stu-id="9363c-227">Reboot</span></span><br/>    |
| <dl> <span data-ttu-id="9363c-228"><dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="9363c-228"><dt>11</dt></span></span> </dl> | <span data-ttu-id="9363c-229">Reset</span><span class="sxs-lookup"><span data-stu-id="9363c-229">Reset</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="9363c-230">**SupportedMethods**</span><span class="sxs-lookup"><span data-stu-id="9363c-230">**SupportedMethods**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9363c-231">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="9363c-231">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9363c-232">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9363c-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9363c-233">Gibt die Methoden an, die vom metrikdienst unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="9363c-233">Specifies the methods supported by the metric service.</span></span> <span data-ttu-id="9363c-234">Diese Eigenschaft wird von **CIM \_ metricservicecapabiligeerbt**.</span><span class="sxs-lookup"><span data-stu-id="9363c-234">This property is inherited from **CIM\_MetricServiceCapabilities**.</span></span>



| <span data-ttu-id="9363c-235">Wert</span><span class="sxs-lookup"><span data-stu-id="9363c-235">Value</span></span>                                                                                   | <span data-ttu-id="9363c-236">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9363c-236">Meaning</span></span>                                                                                         |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9363c-237"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9363c-237"><dt>2</dt></span></span> </dl>            | <span data-ttu-id="9363c-238">Die [**controlmetrics**](controlmetrics-msvm-metricservice.md) -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9363c-238">The [**ControlMetrics**](controlmetrics-msvm-metricservice.md) method is supported.</span></span><br/> |
| <dl> <span data-ttu-id="9363c-239"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="9363c-239"><dt>3</dt></span></span> </dl>            | <span data-ttu-id="9363c-240">Die **controlmetricsbyclass** -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9363c-240">The **ControlMetricsByClass** method is supported.</span></span><br/>                                   |
| <dl> <span data-ttu-id="9363c-241"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="9363c-241"><dt>4</dt></span></span> </dl>            | <span data-ttu-id="9363c-242">Die **showmetrics** -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9363c-242">The **ShowMetrics** method is supported.</span></span><br/>                                             |
| <dl> <span data-ttu-id="9363c-243"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="9363c-243"><dt>5</dt></span></span> </dl>            | <span data-ttu-id="9363c-244">Die **showmetricsbyclass** -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9363c-244">The **ShowMetricsByClass** method is supported.</span></span><br/>                                      |
| <dl> <span data-ttu-id="9363c-245"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="9363c-245"><dt>6</dt></span></span> </dl>            | <span data-ttu-id="9363c-246">Die **getmetricvalues** -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9363c-246">The **GetMetricValues** method is supported.</span></span><br/>                                         |
| <dl> <span data-ttu-id="9363c-247"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="9363c-247"><dt>7</dt></span></span> </dl>            | <span data-ttu-id="9363c-248">Die **controlsampletimes** -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9363c-248">The **ControlSampleTimes** method is supported.</span></span><br/>                                      |
| <dl> <span data-ttu-id="9363c-249"><dt>8.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="9363c-249"><dt>8..32767</dt></span></span> </dl>     | <span data-ttu-id="9363c-250">DMTF reserviert</span><span class="sxs-lookup"><span data-stu-id="9363c-250">DMTF reserved</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="9363c-251"><dt>32768.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="9363c-251"><dt>32768..65535</dt></span></span> </dl> | <span data-ttu-id="9363c-252">Hersteller spezifisch</span><span class="sxs-lookup"><span data-stu-id="9363c-252">Vendor specific</span></span><br/>                                                                      |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9363c-253">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9363c-253">Requirements</span></span>



| <span data-ttu-id="9363c-254">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9363c-254">Requirement</span></span> | <span data-ttu-id="9363c-255">Wert</span><span class="sxs-lookup"><span data-stu-id="9363c-255">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9363c-256">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9363c-256">Minimum supported client</span></span><br/> | <span data-ttu-id="9363c-257">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9363c-257">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9363c-258">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9363c-258">Minimum supported server</span></span><br/> | <span data-ttu-id="9363c-259">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9363c-259">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9363c-260">Namespace</span><span class="sxs-lookup"><span data-stu-id="9363c-260">Namespace</span></span><br/>                | <span data-ttu-id="9363c-261">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="9363c-261">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9363c-262">MOF</span><span class="sxs-lookup"><span data-stu-id="9363c-262">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9363c-263"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9363c-263"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9363c-264">DLL</span><span class="sxs-lookup"><span data-stu-id="9363c-264">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9363c-265"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9363c-265"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9363c-266">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9363c-266">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9363c-267">**CIM \_ metricservicecapabilitäten**</span><span class="sxs-lookup"><span data-stu-id="9363c-267">**CIM\_MetricServiceCapabilities**</span></span>](cim-metricservicecapabilities.md)
</dt> <dt>

[<span data-ttu-id="9363c-268">**MSVM \_ metricservice**</span><span class="sxs-lookup"><span data-stu-id="9363c-268">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 

