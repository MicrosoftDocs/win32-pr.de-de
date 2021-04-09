---
description: Stellt einen Metrikwert dar, der durch eine Instanz der MSVM \_ basemetricdefinition-Klasse definiert wird.
ms.assetid: bd872f21-ab71-4ab7-88d3-b26dd2fbdbe5
title: Msvm_BaseMetricValue-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BaseMetricValue
- Msvm_BaseMetricValue.InstanceID
- Msvm_BaseMetricValue.Caption
- Msvm_BaseMetricValue.Description
- Msvm_BaseMetricValue.ElementName
- Msvm_BaseMetricValue.MetricDefinitionId
- Msvm_BaseMetricValue.MeasuredElementName
- Msvm_BaseMetricValue.TimeStamp
- Msvm_BaseMetricValue.Duration
- Msvm_BaseMetricValue.MetricValue
- Msvm_BaseMetricValue.BreakdownDimension
- Msvm_BaseMetricValue.BreakdownValue
- Msvm_BaseMetricValue.Volatile
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f0e566de4822b271dcd4633c3dba35f7c88495bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867975"
---
# <a name="msvm_basemetricvalue-class"></a><span data-ttu-id="69245-103">MSVM \_ basemetricvalue-Klasse</span><span class="sxs-lookup"><span data-stu-id="69245-103">Msvm\_BaseMetricValue class</span></span>

<span data-ttu-id="69245-104">Stellt einen Metrikwert dar, der durch eine Instanz der [**MSVM \_ basemetricdefinition**](msvm-basemetricdefinition.md) -Klasse definiert wird.</span><span class="sxs-lookup"><span data-stu-id="69245-104">Represents a metric value defined by an instance of the [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md) class.</span></span>

<span data-ttu-id="69245-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="69245-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="69245-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="69245-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BaseMetricValue : CIM_BaseMetricValue
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
};
```

## <a name="members"></a><span data-ttu-id="69245-107">Member</span><span class="sxs-lookup"><span data-stu-id="69245-107">Members</span></span>

<span data-ttu-id="69245-108">Die **MSVM \_ basemetricvalue** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="69245-108">The **Msvm\_BaseMetricValue** class has these types of members:</span></span>

-   [<span data-ttu-id="69245-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="69245-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="69245-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="69245-110">Properties</span></span>

<span data-ttu-id="69245-111">Die **MSVM \_ basemetricvalue** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="69245-111">The **Msvm\_BaseMetricValue** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="69245-112">**Breakdowndimension**</span><span class="sxs-lookup"><span data-stu-id="69245-112">**BreakdownDimension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69245-113">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="69245-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="69245-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="69245-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="69245-115">Gibt eine zusammenteilungs Dimension aus dem **breakdowndimensions** -Array an, das in der zugeordneten [**MSVM \_ basemetricdefinition**](msvm-basemetricdefinition.md)definiert ist.</span><span class="sxs-lookup"><span data-stu-id="69245-115">Specifies one breakdown dimension from the **BreakdownDimensions** array defined in the associated [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md).</span></span> <span data-ttu-id="69245-116">Dies ist die Dimension, in der dieser Satz von Metrikwerten untergliedert ist.</span><span class="sxs-lookup"><span data-stu-id="69245-116">This is the dimension along which this set of metric values is broken down.</span></span> <span data-ttu-id="69245-117">Diese Eigenschaft wird von [**CIM \_ basemetricdefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="69245-117">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="69245-118">**Breakdownwert**</span><span class="sxs-lookup"><span data-stu-id="69245-118">**BreakdownValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69245-119">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="69245-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="69245-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="69245-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="69245-121">Definiert einen Wert der **breakdowndimension** -Eigenschaft, die für diese metrikwertinstanz definiert ist.</span><span class="sxs-lookup"><span data-stu-id="69245-121">Defines a value of the **BreakdownDimension** property defined for this metric value instance.</span></span> <span data-ttu-id="69245-122">Wenn die **breakdowndimension** z. b. "transaktionname" lautet, könnte diese Eigenschaft die tatsächliche Transaktion benennen, für die dieser bestimmte Metrikwert gilt.</span><span class="sxs-lookup"><span data-stu-id="69245-122">For example, if the **BreakdownDimension** is "TransactionName", this property could name the actual transaction to which this particular metric value applies.</span></span> <span data-ttu-id="69245-123">Diese Eigenschaft wird von [**CIM \_ basemetricdefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="69245-123">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="69245-124">**Caption**</span><span class="sxs-lookup"><span data-stu-id="69245-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69245-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="69245-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="69245-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="69245-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="69245-127">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="69245-127">A short description of the object.</span></span> <span data-ttu-id="69245-128">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="69245-128">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="69245-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="69245-129">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69245-130">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="69245-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="69245-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="69245-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="69245-132">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="69245-132">A description of the object.</span></span> <span data-ttu-id="69245-133">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="69245-133">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="69245-134">**Dauer**</span><span class="sxs-lookup"><span data-stu-id="69245-134">**Duration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69245-135">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="69245-135">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="69245-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="69245-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="69245-137">Gibt die Zeitspanne an, für die dieser Metrikwert gültig ist.</span><span class="sxs-lookup"><span data-stu-id="69245-137">Specifies the time duration over which this metric value is valid.</span></span> <span data-ttu-id="69245-138">Diese Eigenschaft darf nicht für Zeitstempel vorhanden sein, die nur auf einen bestimmten Zeitpunkt zutreffen, sondern sollte für Werte angegeben werden, die für einen bestimmten Zeitraum gültig sind (z. b. Stichproben).</span><span class="sxs-lookup"><span data-stu-id="69245-138">This property should not exist for time stamps that apply only to a point in time, but should be specified for values that are considered valid for a certain time period (for example, sampling).</span></span> <span data-ttu-id="69245-139">Wenn die **Duration** -Eigenschaft vorhanden ist und nicht **null** ist, gibt die **timestamp** -Eigenschaft das Ende des Intervalls an.</span><span class="sxs-lookup"><span data-stu-id="69245-139">If the **Duration** property exists and is not **Null**, the **TimeStamp** property specifies the end of the interval.</span></span> <span data-ttu-id="69245-140">Diese Eigenschaft wird von [**CIM \_ basemetricdefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="69245-140">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="69245-141">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="69245-141">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69245-142">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="69245-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="69245-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="69245-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="69245-144">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="69245-144">A display name for the object.</span></span> <span data-ttu-id="69245-145">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="69245-145">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="69245-146">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="69245-146">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69245-147">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="69245-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="69245-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="69245-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="69245-149">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="69245-149">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="69245-150">Eine Zeichenfolge, die eine Instanz dieser Klasse eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="69245-150">A string that uniquely identifies an instance of this class.</span></span> <span data-ttu-id="69245-151">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="69245-151">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="69245-152">**"Messredelta Name"**</span><span class="sxs-lookup"><span data-stu-id="69245-152">**MeasuredElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69245-153">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="69245-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="69245-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="69245-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="69245-155">Ein beschreibender Name für das Element, zu dem der Metrikwert gehört (das gemessene Element).</span><span class="sxs-lookup"><span data-stu-id="69245-155">A descriptive name for the element to which the metric value belongs (the measured element).</span></span> <span data-ttu-id="69245-156">Diese Eigenschaft wird von [**CIM \_ basemetricdefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="69245-156">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="69245-157">**MetricDefinitionId**</span><span class="sxs-lookup"><span data-stu-id="69245-157">**MetricDefinitionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69245-158">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="69245-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="69245-159">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="69245-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="69245-160">Der Schlüssel der [**MSVM \_ basemetricdefinition**](msvm-basemetricdefinition.md) -Instanz für diesen Wert.</span><span class="sxs-lookup"><span data-stu-id="69245-160">The key of the [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md) instance for this value.</span></span> <span data-ttu-id="69245-161">Diese Eigenschaft wird von [**CIM \_ basemetricdefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="69245-161">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="69245-162">**Metricvalue**</span><span class="sxs-lookup"><span data-stu-id="69245-162">**MetricValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69245-163">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="69245-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="69245-164">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="69245-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="69245-165">Der Wert der Metrik, die als Zeichenfolge dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="69245-165">The value of the metric that is represented as a string.</span></span> <span data-ttu-id="69245-166">Diese Eigenschaft wird von [**CIM \_ basemetricdefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="69245-166">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="69245-167">**Zeitstempel**</span><span class="sxs-lookup"><span data-stu-id="69245-167">**TimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69245-168">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="69245-168">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="69245-169">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="69245-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="69245-170">Gibt die Uhrzeit an, zu der der Metrikwert aufgezeichnet oder berechnet wurde.</span><span class="sxs-lookup"><span data-stu-id="69245-170">Specifies the time when the metric value was captured or computed.</span></span> <span data-ttu-id="69245-171">Beachten Sie, dass sich dies von dem Zeitpunkt der Erstellung der Instanz unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="69245-171">Be aware that this is different from the time when the instance was created.</span></span> <span data-ttu-id="69245-172">Diese Eigenschaft wird von [**CIM \_ basemetricdefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="69245-172">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="69245-173">**Ständigem**</span><span class="sxs-lookup"><span data-stu-id="69245-173">**Volatile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69245-174">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="69245-174">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="69245-175">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="69245-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="69245-176">**True** , wenn der Wert für den nächsten Zeitpunkt die gleiche Klasseninstanz verwendet und nur die Eigenschaftswerte (z. b. der **Wert** oder der **Zeitstempel**) geändert werden.</span><span class="sxs-lookup"><span data-stu-id="69245-176">**True** if the value for the next point in time will use the same class instance and just change the property values (such as the **Value** or **TimeStamp**).</span></span> <span data-ttu-id="69245-177">**True** gibt an, dass die-Instanz wieder verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="69245-177">If **True**, the instance is reused.</span></span> <span data-ttu-id="69245-178">Wenn der Wert **false** ist, bleiben die vorhandenen Instanzen unverändert, und für den neuen Zeitpunkt wird eine neue Instanz erstellt.</span><span class="sxs-lookup"><span data-stu-id="69245-178">If **False**, the existing instances remain unchanged and a new instance is created for the new point in time.</span></span> <span data-ttu-id="69245-179">Diese Eigenschaft wird von [**CIM \_ basemetricdefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="69245-179">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="69245-180">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="69245-180">Requirements</span></span>



| <span data-ttu-id="69245-181">Anforderung</span><span class="sxs-lookup"><span data-stu-id="69245-181">Requirement</span></span> | <span data-ttu-id="69245-182">Wert</span><span class="sxs-lookup"><span data-stu-id="69245-182">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69245-183">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="69245-183">Minimum supported client</span></span><br/> | <span data-ttu-id="69245-184">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="69245-184">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="69245-185">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="69245-185">Minimum supported server</span></span><br/> | <span data-ttu-id="69245-186">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="69245-186">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="69245-187">Namespace</span><span class="sxs-lookup"><span data-stu-id="69245-187">Namespace</span></span><br/>                | <span data-ttu-id="69245-188">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="69245-188">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="69245-189">MOF</span><span class="sxs-lookup"><span data-stu-id="69245-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="69245-190"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="69245-190"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="69245-191">DLL</span><span class="sxs-lookup"><span data-stu-id="69245-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69245-192"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="69245-192"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

