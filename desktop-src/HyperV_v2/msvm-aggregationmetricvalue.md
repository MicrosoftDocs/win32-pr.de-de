---
description: Stellt den Instanzwert einer Metrik dar, die durch eine Instanz der MSVM \_ aggregationmetricdefinition-Klasse definiert wird.
ms.assetid: 6dfcb711-6137-492a-aff4-82facbd11949
title: Msvm_AggregationMetricValue-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AggregationMetricValue
- Msvm_AggregationMetricValue.InstanceID
- Msvm_AggregationMetricValue.Caption
- Msvm_AggregationMetricValue.Description
- Msvm_AggregationMetricValue.ElementName
- Msvm_AggregationMetricValue.MetricDefinitionId
- Msvm_AggregationMetricValue.MeasuredElementName
- Msvm_AggregationMetricValue.TimeStamp
- Msvm_AggregationMetricValue.Duration
- Msvm_AggregationMetricValue.MetricValue
- Msvm_AggregationMetricValue.BreakdownDimension
- Msvm_AggregationMetricValue.BreakdownValue
- Msvm_AggregationMetricValue.Volatile
- Msvm_AggregationMetricValue.AggregationTimeStamp
- Msvm_AggregationMetricValue.AggregationDuration
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f6842e5a23fbbf7cf1d639862cf5b9737bc1ff96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042709"
---
# <a name="msvm_aggregationmetricvalue-class"></a><span data-ttu-id="92d6b-103">MSVM \_ aggregationmetricvalue-Klasse</span><span class="sxs-lookup"><span data-stu-id="92d6b-103">Msvm\_AggregationMetricValue class</span></span>

<span data-ttu-id="92d6b-104">Stellt den Instanzwert einer Metrik dar, die durch eine Instanz der [**MSVM \_ aggregationmetricdefinition**](msvm-aggregationmetricdefinition.md) -Klasse definiert wird.</span><span class="sxs-lookup"><span data-stu-id="92d6b-104">Represents the instance value of a metric defined by an instance of the [**Msvm\_AggregationMetricDefinition**](msvm-aggregationmetricdefinition.md) class.</span></span> <span data-ttu-id="92d6b-105">Die von [**MSVM \_ basemetricvalue**](msvm-basemetricvalue.md) geerbten Eigenschaften stellen den tatsächlichen Metrikwert bereit.</span><span class="sxs-lookup"><span data-stu-id="92d6b-105">The properties inherited from [**Msvm\_BaseMetricValue**](msvm-basemetricvalue.md) provide the actual metric value.</span></span> <span data-ttu-id="92d6b-106">Die Eigenschaften, die von dieser Klasse definiert werden, enthalten Informationen über das Intervall, für das die Aggregations Funktion angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="92d6b-106">The properties defined by this class provide information about the interval over which the aggregation function was applied.</span></span>

<span data-ttu-id="92d6b-107">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="92d6b-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="92d6b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="92d6b-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AggregationMetricValue : CIM_AggregationMetricValue
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  string   MetricDefinitionId;
  string   MeasuredElementName;
  datetime TimeStamp;
  datetime Duration;
  string   MetricValue;
  string   BreakdownDimension;
  string   BreakdownValue;
  boolean  Volatile;
  datetime AggregationTimeStamp;
  datetime AggregationDuration;
};
```

## <a name="members"></a><span data-ttu-id="92d6b-109">Member</span><span class="sxs-lookup"><span data-stu-id="92d6b-109">Members</span></span>

<span data-ttu-id="92d6b-110">Die **MSVM \_ aggregationmetricvalue** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="92d6b-110">The **Msvm\_AggregationMetricValue** class has these types of members:</span></span>

-   [<span data-ttu-id="92d6b-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="92d6b-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="92d6b-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="92d6b-112">Properties</span></span>

<span data-ttu-id="92d6b-113">Die **MSVM \_ aggregationmetricvalue** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="92d6b-113">The **Msvm\_AggregationMetricValue** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="92d6b-114">**Aggregationduration**</span><span class="sxs-lookup"><span data-stu-id="92d6b-114">**AggregationDuration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92d6b-115">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="92d6b-115">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="92d6b-116">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="92d6b-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92d6b-117">Stellt die Zeitspanne dar, in der die Aggregation berechnet wurde.</span><span class="sxs-lookup"><span data-stu-id="92d6b-117">Represents the time duration over which the aggregation was computed.</span></span> <span data-ttu-id="92d6b-118">Der Start eines Überwachungs Intervalls, für das die Aggregations Funktion angewendet wird, wird durch Subtrahieren der **aggregationduration** vom **aggregationtimestamp** bestimmt.</span><span class="sxs-lookup"><span data-stu-id="92d6b-118">The start of a monitoring interval over which the aggregation function is applied is determined by subtracting the **AggregationDuration** from the **AggregationTimeStamp**.</span></span> <span data-ttu-id="92d6b-119">Diese Eigenschaft wird von **CIM \_ aggregationmetricvalue** geerbt.</span><span class="sxs-lookup"><span data-stu-id="92d6b-119">This property is inherited from **CIM\_AggregationMetricValue**.</span></span>

</dd> <dt>

<span data-ttu-id="92d6b-120">**Aggregationtimestamp**</span><span class="sxs-lookup"><span data-stu-id="92d6b-120">**AggregationTimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92d6b-121">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="92d6b-121">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="92d6b-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="92d6b-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92d6b-123">Gibt die Zeit an, zu der die Aggregations Funktion angewendet wurde, um den Wert der metrikinstanz zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="92d6b-123">Identifies the time when the aggregation function was applied to determine the value of the metric instance.</span></span> <span data-ttu-id="92d6b-124">Dies entspricht nicht der Uhrzeit, zu der die Instanz erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="92d6b-124">This is not the same as the time when the instance was created.</span></span> <span data-ttu-id="92d6b-125">Für eine bestimmte **CIM \_ aggregationmetricvalue** -Instanz ändert sich der **aggregationtimestamp** , wenn die Aggregations Funktion angewendet wird, um den Wert zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="92d6b-125">For a given **CIM\_AggregationMetricValue** instance, the **AggregationTimeStamp** changes whenever the aggregation function is applied to calculate the value.</span></span> <span data-ttu-id="92d6b-126">Diese Eigenschaft wird von **CIM \_ aggregationmetricvalue** geerbt.</span><span class="sxs-lookup"><span data-stu-id="92d6b-126">This property is inherited from **CIM\_AggregationMetricValue**.</span></span>

</dd> <dt>

<span data-ttu-id="92d6b-127">**Breakdowndimension**</span><span class="sxs-lookup"><span data-stu-id="92d6b-127">**BreakdownDimension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92d6b-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="92d6b-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92d6b-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="92d6b-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92d6b-130">Gibt eine zusammenteilungs Dimension aus dem **breakdowndimensions** -Array an, das in der zugeordneten [**MSVM \_ basemetricdefinition**](msvm-basemetricdefinition.md)definiert ist.</span><span class="sxs-lookup"><span data-stu-id="92d6b-130">Specifies one breakdown dimension from the **BreakdownDimensions** array defined in the associated [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md).</span></span> <span data-ttu-id="92d6b-131">Dies ist die Dimension, in der dieser Satz von Metrikwerten untergliedert ist.</span><span class="sxs-lookup"><span data-stu-id="92d6b-131">This is the dimension along which this set of metric values is broken down.</span></span> <span data-ttu-id="92d6b-132">Diese Eigenschaft wird von [**CIM \_ basemetricdefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="92d6b-132">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="92d6b-133">**Breakdownwert**</span><span class="sxs-lookup"><span data-stu-id="92d6b-133">**BreakdownValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92d6b-134">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="92d6b-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92d6b-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="92d6b-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92d6b-136">Definiert einen Wert der **breakdowndimension** -Eigenschaft, die für diese metrikwertinstanz definiert ist.</span><span class="sxs-lookup"><span data-stu-id="92d6b-136">Defines a value of the **BreakdownDimension** property defined for this metric value instance.</span></span> <span data-ttu-id="92d6b-137">Wenn die **breakdowndimension** z. b. "transaktionname" lautet, könnte diese Eigenschaft die tatsächliche Transaktion benennen, für die dieser bestimmte Metrikwert gilt.</span><span class="sxs-lookup"><span data-stu-id="92d6b-137">For example, if the **BreakdownDimension** is "TransactionName", this property could name the actual transaction to which this particular metric value applies.</span></span> <span data-ttu-id="92d6b-138">Diese Eigenschaft wird von [**CIM \_ basemetricdefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="92d6b-138">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="92d6b-139">**Caption**</span><span class="sxs-lookup"><span data-stu-id="92d6b-139">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92d6b-140">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="92d6b-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92d6b-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="92d6b-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92d6b-142">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="92d6b-142">A short description of the object.</span></span> <span data-ttu-id="92d6b-143">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="92d6b-143">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="92d6b-144">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="92d6b-144">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92d6b-145">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="92d6b-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92d6b-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="92d6b-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92d6b-147">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="92d6b-147">A description of the object.</span></span> <span data-ttu-id="92d6b-148">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="92d6b-148">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="92d6b-149">**Dauer**</span><span class="sxs-lookup"><span data-stu-id="92d6b-149">**Duration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92d6b-150">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="92d6b-150">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="92d6b-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="92d6b-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92d6b-152">Gibt die Zeitspanne an, für die dieser Metrikwert gültig ist.</span><span class="sxs-lookup"><span data-stu-id="92d6b-152">Specifies the time duration over which this metric value is valid.</span></span> <span data-ttu-id="92d6b-153">Diese Eigenschaft darf nicht für Zeitstempel vorhanden sein, die nur auf einen bestimmten Zeitpunkt zutreffen, sondern sollte für Werte angegeben werden, die für einen bestimmten Zeitraum gültig sind (z. b. Stichproben).</span><span class="sxs-lookup"><span data-stu-id="92d6b-153">This property should not exist for time stamps that apply only to a point in time, but should be specified for values that are considered valid for a certain time period (for example, sampling).</span></span> <span data-ttu-id="92d6b-154">Wenn die **Duration** -Eigenschaft vorhanden ist und nicht **null** ist, gibt die **timestamp** -Eigenschaft das Ende des Intervalls an.</span><span class="sxs-lookup"><span data-stu-id="92d6b-154">If the **Duration** property exists and is not **Null**, the **TimeStamp** property specifies the end of the interval.</span></span> <span data-ttu-id="92d6b-155">Diese Eigenschaft wird von [**CIM \_ basemetricdefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="92d6b-155">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="92d6b-156">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="92d6b-156">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92d6b-157">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="92d6b-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92d6b-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="92d6b-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92d6b-159">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="92d6b-159">A display name for the object.</span></span> <span data-ttu-id="92d6b-160">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="92d6b-160">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="92d6b-161">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="92d6b-161">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92d6b-162">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="92d6b-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92d6b-163">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="92d6b-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92d6b-164">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="92d6b-164">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="92d6b-165">Eine Zeichenfolge, die eine Instanz dieser Klasse eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="92d6b-165">A string that uniquely identifies an instance of this class.</span></span> <span data-ttu-id="92d6b-166">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="92d6b-166">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="92d6b-167">**"Messredelta Name"**</span><span class="sxs-lookup"><span data-stu-id="92d6b-167">**MeasuredElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92d6b-168">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="92d6b-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92d6b-169">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="92d6b-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92d6b-170">Ein beschreibender Name für das Element, zu dem der Metrikwert gehört (das gemessene Element).</span><span class="sxs-lookup"><span data-stu-id="92d6b-170">A descriptive name for the element to which the metric value belongs (the measured element).</span></span> <span data-ttu-id="92d6b-171">Diese Eigenschaft wird von [**CIM \_ basemetricdefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="92d6b-171">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="92d6b-172">**MetricDefinitionId**</span><span class="sxs-lookup"><span data-stu-id="92d6b-172">**MetricDefinitionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92d6b-173">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="92d6b-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92d6b-174">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="92d6b-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92d6b-175">Der Schlüssel der [**MSVM \_ basemetricdefinition**](msvm-basemetricdefinition.md) -Instanz für diesen Wert.</span><span class="sxs-lookup"><span data-stu-id="92d6b-175">The key of the [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md) instance for this value.</span></span> <span data-ttu-id="92d6b-176">Diese Eigenschaft wird von [**CIM \_ basemetricdefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="92d6b-176">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="92d6b-177">**Metricvalue**</span><span class="sxs-lookup"><span data-stu-id="92d6b-177">**MetricValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92d6b-178">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="92d6b-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92d6b-179">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="92d6b-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92d6b-180">Der Wert der Metrik, die als Zeichenfolge dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="92d6b-180">The value of the metric that is represented as a string.</span></span> <span data-ttu-id="92d6b-181">Diese Eigenschaft wird von [**CIM \_ basemetricdefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="92d6b-181">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="92d6b-182">**Zeitstempel**</span><span class="sxs-lookup"><span data-stu-id="92d6b-182">**TimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92d6b-183">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="92d6b-183">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="92d6b-184">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="92d6b-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92d6b-185">Gibt die Uhrzeit an, zu der der Metrikwert aufgezeichnet oder berechnet wurde.</span><span class="sxs-lookup"><span data-stu-id="92d6b-185">Specifies the time when the metric value was captured or computed.</span></span> <span data-ttu-id="92d6b-186">Beachten Sie, dass sich dies von dem Zeitpunkt der Erstellung der Instanz unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="92d6b-186">Be aware that this is different from the time when the instance was created.</span></span> <span data-ttu-id="92d6b-187">Diese Eigenschaft wird von [**CIM \_ basemetricdefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="92d6b-187">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="92d6b-188">**Ständigem**</span><span class="sxs-lookup"><span data-stu-id="92d6b-188">**Volatile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92d6b-189">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="92d6b-189">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="92d6b-190">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="92d6b-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92d6b-191">**True** , wenn der Wert für den nächsten Zeitpunkt die gleiche Klasseninstanz verwendet und nur die Eigenschaftswerte (z. b. der **Wert** oder der **Zeitstempel**) geändert werden.</span><span class="sxs-lookup"><span data-stu-id="92d6b-191">**True** if the value for the next point in time will use the same class instance and just change the property values (such as the **Value** or **TimeStamp**).</span></span> <span data-ttu-id="92d6b-192">**True** gibt an, dass die-Instanz wieder verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="92d6b-192">If **True**, the instance is reused.</span></span> <span data-ttu-id="92d6b-193">Wenn der Wert **false** ist, bleiben die vorhandenen Instanzen unverändert, und für den neuen Zeitpunkt wird eine neue Instanz erstellt.</span><span class="sxs-lookup"><span data-stu-id="92d6b-193">If **False**, the existing instances remain unchanged and a new instance is created for the new point in time.</span></span> <span data-ttu-id="92d6b-194">Diese Eigenschaft wird von [**CIM \_ basemetricdefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="92d6b-194">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="92d6b-195">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="92d6b-195">Requirements</span></span>



| <span data-ttu-id="92d6b-196">Anforderung</span><span class="sxs-lookup"><span data-stu-id="92d6b-196">Requirement</span></span> | <span data-ttu-id="92d6b-197">Wert</span><span class="sxs-lookup"><span data-stu-id="92d6b-197">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92d6b-198">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="92d6b-198">Minimum supported client</span></span><br/> | <span data-ttu-id="92d6b-199">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="92d6b-199">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="92d6b-200">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="92d6b-200">Minimum supported server</span></span><br/> | <span data-ttu-id="92d6b-201">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="92d6b-201">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="92d6b-202">Namespace</span><span class="sxs-lookup"><span data-stu-id="92d6b-202">Namespace</span></span><br/>                | <span data-ttu-id="92d6b-203">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="92d6b-203">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="92d6b-204">MOF</span><span class="sxs-lookup"><span data-stu-id="92d6b-204">MOF</span></span><br/>                      | <dl> <span data-ttu-id="92d6b-205"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="92d6b-205"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="92d6b-206">DLL</span><span class="sxs-lookup"><span data-stu-id="92d6b-206">DLL</span></span><br/>                      | <dl> <span data-ttu-id="92d6b-207"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="92d6b-207"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

