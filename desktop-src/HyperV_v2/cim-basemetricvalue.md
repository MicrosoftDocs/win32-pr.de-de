---
description: Stellt den Instanzwert einer Metrik dar.
ms.assetid: 6b272ae8-7684-45bb-bff8-6559680cc8b6
title: CIM_BaseMetricValue-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BaseMetricValue
- CIM_BaseMetricValue.InstanceID
- CIM_BaseMetricValue.MetricDefinitionId
- CIM_BaseMetricValue.MeasuredElementName
- CIM_BaseMetricValue.TimeStamp
- CIM_BaseMetricValue.Duration
- CIM_BaseMetricValue.MetricValue
- CIM_BaseMetricValue.BreakdownDimension
- CIM_BaseMetricValue.BreakdownValue
- CIM_BaseMetricValue.Volatile
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ca6c90a4b6b3ef3e690c13612f69480ec5f008be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960357"
---
# <a name="cim_basemetricvalue-class"></a><span data-ttu-id="2e50d-103">CIM \_ basemetricvalue-Klasse</span><span class="sxs-lookup"><span data-stu-id="2e50d-103">CIM\_BaseMetricValue class</span></span>

<span data-ttu-id="2e50d-104">Stellt den Instanzwert einer Metrik dar.</span><span class="sxs-lookup"><span data-stu-id="2e50d-104">Represents the instance value of a metric.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e50d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e50d-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.19.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_BaseMetricValue : CIM_ManagedElement
{
  string   InstanceID;
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

## <a name="members"></a><span data-ttu-id="2e50d-106">Member</span><span class="sxs-lookup"><span data-stu-id="2e50d-106">Members</span></span>

<span data-ttu-id="2e50d-107">Die **CIM \_ basemetricvalue** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2e50d-107">The **CIM\_BaseMetricValue** class has these types of members:</span></span>

-   [<span data-ttu-id="2e50d-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2e50d-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2e50d-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2e50d-109">Properties</span></span>

<span data-ttu-id="2e50d-110">Die **CIM \_ basemetricvalue** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2e50d-110">The **CIM\_BaseMetricValue** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2e50d-111">**Breakdowndimension**</span><span class="sxs-lookup"><span data-stu-id="2e50d-111">**BreakdownDimension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e50d-112">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2e50d-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e50d-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2e50d-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e50d-114">Die Dimension, für die dieser Satz von Metrikwerten basierend auf der **breakdowndimensions** -Eigenschaft des zugeordneten [**CIM \_ basemetricdefinition**](cim-basemetricdefinition.md) -Objekts aufgeteilt wird.</span><span class="sxs-lookup"><span data-stu-id="2e50d-114">The dimension for which this set of metric values is broken down based on **BreakdownDimensions** property of the associated [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="2e50d-115">**Breakdownwert**</span><span class="sxs-lookup"><span data-stu-id="2e50d-115">**BreakdownValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e50d-116">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2e50d-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e50d-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2e50d-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e50d-118">Der Wert der **breakdowndimension** -Eigenschaft, die für diesen Instanzwert definiert ist.</span><span class="sxs-lookup"><span data-stu-id="2e50d-118">The value of the **BreakdownDimension** property defined for this instance value.</span></span> <span data-ttu-id="2e50d-119">Wenn **breakdowndimension** z. b. "transaktionname" enthält, könnte diese Eigenschaft die tatsächliche Transaktion benennen, für die dieser bestimmte Metrikwert gilt.</span><span class="sxs-lookup"><span data-stu-id="2e50d-119">For example, if **BreakdownDimension** contains "TransactionName", this property could name the actual transaction to which this particular metric value applies.</span></span>

</dd> <dt>

<span data-ttu-id="2e50d-120">**Dauer**</span><span class="sxs-lookup"><span data-stu-id="2e50d-120">**Duration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e50d-121">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="2e50d-121">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2e50d-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2e50d-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e50d-123">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ basemetricdefinition**](cim-basemetricdefinition.md)".**Timescope**","**CIM \_ basemetricvalue**.**Zeitstempel**")</span><span class="sxs-lookup"><span data-stu-id="2e50d-123">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md).**TimeScope**", "**CIM\_BaseMetricValue**.**TimeStamp**")</span></span>
</dt> </dl>

<span data-ttu-id="2e50d-124">Die Zeitspanne, für die dieser Metrikwert gültig ist.</span><span class="sxs-lookup"><span data-stu-id="2e50d-124">The time duration over which this metric value is valid.</span></span> <span data-ttu-id="2e50d-125">Diese Eigenschaft darf nicht für Zeitstempel vorhanden sein, die nur auf einen bestimmten Zeitpunkt zutreffen, sondern sollte für Werte definiert werden, die für einen bestimmten Zeitraum gültig sind (z.</span><span class="sxs-lookup"><span data-stu-id="2e50d-125">This property should not exist for time stamps that only apply to a point in time, but should be defined for values that are considered valid for a certain time period (ex.</span></span> <span data-ttu-id="2e50d-126">Sampling).</span><span class="sxs-lookup"><span data-stu-id="2e50d-126">sampling).</span></span> <span data-ttu-id="2e50d-127">Wenn die **Duration** -Eigenschaft vorhanden ist und nicht NULL ist, sollte der **Zeitstempel** Wert das Ende des Intervalls sein.</span><span class="sxs-lookup"><span data-stu-id="2e50d-127">If the **Duration** property exists and is non-Null, the **TimeStamp** value should be the end of the interval.</span></span>

</dd> <dt>

<span data-ttu-id="2e50d-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2e50d-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e50d-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2e50d-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e50d-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2e50d-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e50d-131">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceId")</span><span class="sxs-lookup"><span data-stu-id="2e50d-131">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")</span></span>
</dt> </dl>

<span data-ttu-id="2e50d-132">Identifiziert eine Instanz dieser Klasse eindeutig innerhalb des Gültigkeits Bereichs des enthaltenden Namespace.</span><span class="sxs-lookup"><span data-stu-id="2e50d-132">Uniquely identifies an instance of this class within the scope of the containing namespace.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="2e50d-133">Um die Eindeutigkeit innerhalb des Namespaces sicherzustellen, sollte der Wert der **InstanceId-** Eigenschaft im folgenden Muster erstellt werden: *OrgId*:*localId*</span><span class="sxs-lookup"><span data-stu-id="2e50d-133">In order to ensure uniqueness within the namespace, the value of the **InstanceID** property should be constructed in the following pattern: *OrgID*:*LocalID*</span></span>
>
> <span data-ttu-id="2e50d-134">*OrgId* muss einen urheberrechtlich geschützten oder anderweitig eindeutigen Namen enthalten, der der Geschäfts Entität gehört, die die **InstanceId** definiert, oder eine registrierte ID ist, die von einer anerkannten globalen Autorität zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="2e50d-134">*OrgID* must include a copyrighted, trademarked or otherwise unique name that is owned by the business entity that defines the **InstanceID**, or be a registered ID that is assigned by a recognized global authority.</span></span> <span data-ttu-id="2e50d-135">Dieses Muster ähnelt der Struktur von Schema Klassennamen.</span><span class="sxs-lookup"><span data-stu-id="2e50d-135">This pattern is similar to the structure of schema class names.</span></span> <span data-ttu-id="2e50d-136">Um die Eindeutigkeit sicherzustellen, muss der erste Doppelpunkt in **InstanceId** zwischen der *OrgId* und der *Lok-* ID liegen.</span><span class="sxs-lookup"><span data-stu-id="2e50d-136">In addition, to ensure uniqueness, the first colon in **InstanceID** must be between the *OrgID* and *LocalID*.</span></span> <span data-ttu-id="2e50d-137">Daher darf die *OrgId* keinen Doppelpunkt (': ') enthalten.</span><span class="sxs-lookup"><span data-stu-id="2e50d-137">Therefore the *OrgID* must not contain a colon (':').</span></span>
>
> <span data-ttu-id="2e50d-138">*LocalId* wird von der Geschäfts Entität ausgewählt und sollte nicht erneut verwendet werden, um verschiedene zugrunde liegende reale Elemente zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="2e50d-138">*LocalID* is chosen by the business entity and should not be re-used to identify different underlying real-world elements.</span></span>
>
> <span data-ttu-id="2e50d-139">Wenn das obige Muster nicht verwendet wird, muss die definierende Entität sicherstellen, dass der resultierende **InstanceId** -Wert nicht für **InstanceId** -Eigenschaften wieder verwendet wird, die von diesem Anbieter oder von anderen Anbietern für diesen Namespace erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="2e50d-139">If the above pattern is not used, the defining entity must assure that the resultant **InstanceID** value is not re-used across any **InstanceID** properties that are produced by this provider or other providers for this namespace.</span></span>
>
> <span data-ttu-id="2e50d-140">Für von DMTF (verteilte Management Task Force) definierte Instanzen muss das Muster verwendet werden, wenn die *OrgId* auf CIM festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="2e50d-140">For Distributed Management Task Force (DMTF) defined instances, the pattern must be used with the *OrgID* set to CIM.</span></span>

 

</dd> <dt>

<span data-ttu-id="2e50d-141">**"Messredelta Name"**</span><span class="sxs-lookup"><span data-stu-id="2e50d-141">**MeasuredElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e50d-142">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2e50d-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e50d-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2e50d-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e50d-144">Ein beschreibender Name für das Element, das von der Metrik gemessen wird.</span><span class="sxs-lookup"><span data-stu-id="2e50d-144">A descriptive name for the element that is measure by the metric.</span></span>

<span data-ttu-id="2e50d-145">Diese Eigenschaft ist erforderlich, wenn die metrikdefinition keinem [**CIM \_ managedelta**](cim-managedelement.md) -Objekt zugeordnet ist und in anderen Fällen zum Bereitstellen zusätzlicher Informationen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="2e50d-145">This property is required if the metric definition is not associated with a [**CIM\_ManagedElement**](cim-managedelement.md) object, and may be used in other cases to provide supplemental information.</span></span> <span data-ttu-id="2e50d-146">Dadurch können Metriken unabhängig von einem CIM- **\_ managedelta** -Objekt erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="2e50d-146">This allows metrics to be captured independent of any **CIM\_ManagedElement** object.</span></span>

<span data-ttu-id="2e50d-147">Wenn dem Metrikwert mehrere [**CIM \_ managedelements**](cim-managedelement.md) -Objekte zugeordnet sind, können Sie eines der verwalteten Elemente auswählen, um die ergänzenden Informationen für die Metrik zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2e50d-147">If there are multiple [**CIM\_ManagedElement**](cim-managedelement.md) objects associated with the metric value, then you can choose one of the managed elements to create the supplemental information for the metric.</span></span> <span data-ttu-id="2e50d-148">Die-Eigenschaft ist nicht für die Verwendung als Fremdschlüssel zum Abfragen des gemessenen Elements vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="2e50d-148">The property is not meant to be used as a foreign key to query the measured element.</span></span> <span data-ttu-id="2e50d-149">Stattdessen sollte die Zuordnung zum **CIM- \_ managedelta** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2e50d-149">Instead, the association to the **CIM\_ManagedElement** should be used.</span></span>

</dd> <dt>

<span data-ttu-id="2e50d-150">**MetricDefinitionId**</span><span class="sxs-lookup"><span data-stu-id="2e50d-150">**MetricDefinitionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e50d-151">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2e50d-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e50d-152">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2e50d-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e50d-153">Qualifizierer: [**erforderlich**](/windows/desktop/WmiSdk/standard-qualifiers), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ basemetricdefinition**](cim-basemetricdefinition.md)".**ID**")</span><span class="sxs-lookup"><span data-stu-id="2e50d-153">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md).**Id**")</span></span>
</dt> </dl>

<span data-ttu-id="2e50d-154">Der Schlüssel der [**CIM- \_ basemetricdefinition**](cim-basemetricdefinition.md) -Instanz, die diesem Instanzwert zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="2e50d-154">The key of the [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) instance that is associated with this instance value.</span></span>

</dd> <dt>

<span data-ttu-id="2e50d-155">**Metricvalue**</span><span class="sxs-lookup"><span data-stu-id="2e50d-155">**MetricValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e50d-156">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2e50d-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e50d-157">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2e50d-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e50d-158">Qualifizierer: [ **erforderlich**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2e50d-158">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2e50d-159">Eine Zeichen folgen Darstellung des metrikwerts.</span><span class="sxs-lookup"><span data-stu-id="2e50d-159">A string representation of the metric value.</span></span> <span data-ttu-id="2e50d-160">Der ursprüngliche Datentyp des metrikwerts wird im zugehörigen [**CIM \_ basemetricdefinition**](cim-basemetricdefinition.md) -Objekt angegeben.</span><span class="sxs-lookup"><span data-stu-id="2e50d-160">The original data type of the metric value is specified in the associated [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="2e50d-161">**Zeitstempel**</span><span class="sxs-lookup"><span data-stu-id="2e50d-161">**TimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e50d-162">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="2e50d-162">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2e50d-163">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2e50d-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e50d-164">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ basemetricdefinition**](cim-basemetricdefinition.md)".**Timescope**","**CIM \_ basemetricvalue**.**Dauer**")</span><span class="sxs-lookup"><span data-stu-id="2e50d-164">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md).**TimeScope**", "**CIM\_BaseMetricValue**.**Duration**")</span></span>
</dt> </dl>

<span data-ttu-id="2e50d-165">Der Zeitpunkt, zu dem der Wert einer metrikinstanz berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="2e50d-165">The time when the value of a metric instance is computed.</span></span> <span data-ttu-id="2e50d-166">Dies unterscheidet sich von der Zeit, zu der die Instanz erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="2e50d-166">This is different from the time when the instance is created.</span></span> <span data-ttu-id="2e50d-167">Wenn die **volatile** -Eigenschaft den Wert true hat, ändert sich dieser Wert immer, wenn eine neue Mess Momentaufnahme erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="2e50d-167">If the **Volatile** property is true, this value changes whenever a new measurement snapshot is taken.</span></span>

<span data-ttu-id="2e50d-168">Eine Verwaltungs Anwendung kann eine Zeitreihe von Metrikdaten erstellen, indem Sie die Instanzen von **CIM \_ basemetricvalue** abruft und Sie entsprechend Ihres **Zeitstempel** Werts sortiert.</span><span class="sxs-lookup"><span data-stu-id="2e50d-168">A management application may establish a time series of metric data by retrieving the instances of **CIM\_BaseMetricValue** and sorting them according to their **TimeStamp** value.</span></span>

</dd> <dt>

<span data-ttu-id="2e50d-169">**Ständigem**</span><span class="sxs-lookup"><span data-stu-id="2e50d-169">**Volatile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e50d-170">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="2e50d-170">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2e50d-171">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2e50d-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e50d-172">True, wenn sich der **Zeitstempel** Wert ändert, wenn sich der Wert der metrikinstanz ändert.</span><span class="sxs-lookup"><span data-stu-id="2e50d-172">True if the **TimeStamp** value changes whenever the value of the metric instance changes.</span></span> <span data-ttu-id="2e50d-173">False, wenn dieses Objekt unverändert bleiben muss und ein neues-Objekt für den neuen **Zeitstempel** Wert erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="2e50d-173">False if this object must remain unchanged and a new object created for the new **TimeStamp** value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2e50d-174">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2e50d-174">Requirements</span></span>



| <span data-ttu-id="2e50d-175">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2e50d-175">Requirement</span></span> | <span data-ttu-id="2e50d-176">Wert</span><span class="sxs-lookup"><span data-stu-id="2e50d-176">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e50d-177">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2e50d-177">Minimum supported client</span></span><br/> | <span data-ttu-id="2e50d-178">Windows 8</span><span class="sxs-lookup"><span data-stu-id="2e50d-178">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="2e50d-179">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2e50d-179">Minimum supported server</span></span><br/> | <span data-ttu-id="2e50d-180">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2e50d-180">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="2e50d-181">Namespace</span><span class="sxs-lookup"><span data-stu-id="2e50d-181">Namespace</span></span><br/>                | <span data-ttu-id="2e50d-182">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="2e50d-182">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2e50d-183">MOF</span><span class="sxs-lookup"><span data-stu-id="2e50d-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2e50d-184"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2e50d-184"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2e50d-185">DLL</span><span class="sxs-lookup"><span data-stu-id="2e50d-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e50d-186"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2e50d-186"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2e50d-187">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2e50d-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e50d-188">**CIM- \_ managedelta**</span><span class="sxs-lookup"><span data-stu-id="2e50d-188">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> </dl>

 

