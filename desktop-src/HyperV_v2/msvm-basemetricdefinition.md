---
description: Stellt die Definitions Aspekte einer Metrik dar.
ms.assetid: 861a69f6-a3bf-4e18-a9c2-931632e3cccc
title: Msvm_BaseMetricDefinition-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BaseMetricDefinition
- Msvm_BaseMetricDefinition.InstanceID
- Msvm_BaseMetricDefinition.Caption
- Msvm_BaseMetricDefinition.Description
- Msvm_BaseMetricDefinition.ElementName
- Msvm_BaseMetricDefinition.Id
- Msvm_BaseMetricDefinition.Name
- Msvm_BaseMetricDefinition.DataType
- Msvm_BaseMetricDefinition.Calculable
- Msvm_BaseMetricDefinition.Units
- Msvm_BaseMetricDefinition.BreakdownDimensions
- Msvm_BaseMetricDefinition.IsContinuous
- Msvm_BaseMetricDefinition.ChangeType
- Msvm_BaseMetricDefinition.TimeScope
- Msvm_BaseMetricDefinition.GatheringType
- Msvm_BaseMetricDefinition.ProgrammaticUnits
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8d1edbd722e3bf87631371b5650576917a7cfb39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106354854"
---
# <a name="msvm_basemetricdefinition-class"></a><span data-ttu-id="23790-103">MSVM \_ basemetricdefinition-Klasse</span><span class="sxs-lookup"><span data-stu-id="23790-103">Msvm\_BaseMetricDefinition class</span></span>

<span data-ttu-id="23790-104">Stellt die Definitions Aspekte einer Metrik dar.</span><span class="sxs-lookup"><span data-stu-id="23790-104">Represents the definition aspects of a metric.</span></span> <span data-ttu-id="23790-105">Die **MSVM \_ basemetricdefinition** -Klasse muss den CIM- [**\_ managedelements**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) zugeordnet werden, auf die Sie angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="23790-105">The **Msvm\_BaseMetricDefinition** class should be associated with the [**CIM\_ManagedElements**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) to which it applies.</span></span>

<span data-ttu-id="23790-106">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="23790-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="23790-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="23790-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BaseMetricDefinition : CIM_BaseMetricDefinition
{
  string  InstanceID;
  string  Caption;
  string  Description;
  string  ElementName;
  string  Id;
  string  Name;
  uint16  DataType;
  uint16  Calculable;
  string  Units;
  string  BreakdownDimensions[];
  boolean IsContinuous;
  uint16  ChangeType;
  uint16  TimeScope;
  uint16  GatheringType;
  string  ProgrammaticUnits;
};
```

## <a name="members"></a><span data-ttu-id="23790-108">Member</span><span class="sxs-lookup"><span data-stu-id="23790-108">Members</span></span>

<span data-ttu-id="23790-109">Die **MSVM \_ basemetricdefinition** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="23790-109">The **Msvm\_BaseMetricDefinition** class has these types of members:</span></span>

-   [<span data-ttu-id="23790-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="23790-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="23790-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="23790-111">Properties</span></span>

<span data-ttu-id="23790-112">Die **MSVM \_ basemetricdefinition** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="23790-112">The **Msvm\_BaseMetricDefinition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="23790-113">**Breakdowndimensionen**</span><span class="sxs-lookup"><span data-stu-id="23790-113">**BreakdownDimensions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23790-114">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="23790-114">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="23790-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23790-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23790-116">Definiert eine oder mehrere Zeichen folgen, die verwendet werden können, um Abfragen für die Metrikwerte in einer bestimmten Dimension zu verfeinern.</span><span class="sxs-lookup"><span data-stu-id="23790-116">Defines one or more strings that can be used to refine (break down) queries against the metric values along a certain dimension.</span></span> <span data-ttu-id="23790-117">Ein Beispiel hierfür ist ein Transaktions Name, der das Unterbrechen des Gesamtwerts für alle Transaktionen in eine Gruppe von Werten ermöglicht, eine für jeden Transaktions Namen.</span><span class="sxs-lookup"><span data-stu-id="23790-117">An example is a transaction name, allowing the break down of the total value for all transactions into a set of values, one for each transaction name.</span></span> <span data-ttu-id="23790-118">Andere Beispiele hierfür sind Anwendungssystem-oder Benutzergruppen Name.</span><span class="sxs-lookup"><span data-stu-id="23790-118">Other examples might be application system or user group name.</span></span> <span data-ttu-id="23790-119">Die Zeichen folgen sind ein kostenloses Format und sollten für die Endbenutzer der Metrikdaten sinnvoll sein.</span><span class="sxs-lookup"><span data-stu-id="23790-119">The strings are free format and should be meaningful to the end users of the metric data.</span></span> <span data-ttu-id="23790-120">Die Zeichen folgen geben an, welche aufbruchdimensionen für diese metrikdefinition von der zugrunde liegenden Instrumentation unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="23790-120">The strings indicate which break down dimensions are supported for this metric definition, by the underlying instrumentation.</span></span> <span data-ttu-id="23790-121">Diese Eigenschaft wird von **CIM \_ basemetricdefinition** geerbt.</span><span class="sxs-lookup"><span data-stu-id="23790-121">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> <dt>

<span data-ttu-id="23790-122">**Bares**</span><span class="sxs-lookup"><span data-stu-id="23790-122">**Calculable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23790-123">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23790-123">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="23790-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23790-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23790-125">Beschreibt die Merkmale der Metrik für die Durchführung von Berechnungen.</span><span class="sxs-lookup"><span data-stu-id="23790-125">Describes the characteristics of the metric for purposes of performing calculations.</span></span> <span data-ttu-id="23790-126">Diese Eigenschaft wird von **CIM \_ basemetricdefinition** geerbt.</span><span class="sxs-lookup"><span data-stu-id="23790-126">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span> <span data-ttu-id="23790-127">Dieser Wert kann **null** oder einer der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="23790-127">This may be **Null** or one of the following values.</span></span>



| <span data-ttu-id="23790-128">Wert</span><span class="sxs-lookup"><span data-stu-id="23790-128">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="23790-129">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="23790-129">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Non-calculable"></span><span id="non-calculable"></span><span id="NON-CALCULABLE"></span><dl> <span data-ttu-id="23790-130"><dt>**Nicht berechenbare**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="23790-130"><dt>**Non-calculable**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="23790-131">Der Wert kann nicht berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="23790-131">The value cannot be calculated.</span></span> <span data-ttu-id="23790-132">Z. b. eine Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="23790-132">For example, a string.</span></span><br/>                                                                                                                                                                                                                                                                                                         |
| <span id="Summable"></span><span id="summable"></span><span id="SUMMABLE"></span><dl> <span data-ttu-id="23790-133"><dt>**Summier Bare**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="23790-133"><dt>**Summable**</dt> <dt>2</dt></span></span> </dl>                         | <span data-ttu-id="23790-134">Der Wert kann über viele Instanzen summiert werden.</span><span class="sxs-lookup"><span data-stu-id="23790-134">The value can be summed over many instances.</span></span> <span data-ttu-id="23790-135">Wenn es sich bei jedem Sicherungsauftrag beispielsweise um eine Arbeitseinheit handelt und jeder Auftrag im Durchschnitt 27.000 Dateien sichert, werden 100 Sicherungsaufträge 2,7 Millionen Dateien verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="23790-135">For example, if each backup job is a unit of work, and each job backs up 27,000 files on average, then 100 backup jobs processed 2,700,000 files.</span></span><br/>                                                                                                                                                                 |
| <span id="Non-summable_"></span><span id="non-summable_"></span><span id="NON-SUMMABLE_"></span><dl> <span data-ttu-id="23790-136"><dt> **Nicht summier Bare**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="23790-136"><dt>**Non-summable** </dt> <dt>3 </dt></span></span> </dl>    | <span data-ttu-id="23790-137">Dieser Wert kann nicht über viele Instanzen summiert werden.</span><span class="sxs-lookup"><span data-stu-id="23790-137">This value cannot be summed over many instances.</span></span> <span data-ttu-id="23790-138">Ein Beispiel wäre eine Metrik, die die Länge der Warteschlange beim Eintreffen eines Auftrags auf einem Server misst.</span><span class="sxs-lookup"><span data-stu-id="23790-138">An example would be a metric that measures the queue length when a job arrives at a server.</span></span> <span data-ttu-id="23790-139">Wenn jeder Auftrag eine Arbeitseinheit ist und die durchschnittliche Warteschlangen Länge bei Eintreffen der einzelnen Aufträge 33 beträgt, ist es nicht sinnvoll, zu sagen, dass die Warteschlangen Länge für 100 Aufträge 3300 beträgt.</span><span class="sxs-lookup"><span data-stu-id="23790-139">If each job is a unit of work, and the average queue length when each job arrives is 33, it does not make sense to say that the queue length for 100 jobs is 3300.</span></span> <span data-ttu-id="23790-140">Es ist sinnvoll, zu sagen, dass der Mittelwert 33 ist.</span><span class="sxs-lookup"><span data-stu-id="23790-140">It does make sense to say that the mean is 33.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="23790-141">**Caption**</span><span class="sxs-lookup"><span data-stu-id="23790-141">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23790-142">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="23790-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23790-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23790-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23790-144">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="23790-144">A short description of the object.</span></span> <span data-ttu-id="23790-145">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="23790-145">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="23790-146">**ChangeType**</span><span class="sxs-lookup"><span data-stu-id="23790-146">**ChangeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23790-147">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23790-147">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="23790-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23790-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23790-149">Gibt an, wie sich der Metrikwert in Form typischer Kombinationen von präziserer Attributen ändert, wie z. b. Richtungsänderungen, Mindest-und Höchstwerte und Wrapping Semantik.</span><span class="sxs-lookup"><span data-stu-id="23790-149">Indicates how the metric value changes, in the form of typical combinations of finer grain attributes such as direction change, minimum and maximum values, and wrapping semantics.</span></span> <span data-ttu-id="23790-150">Diese Eigenschaft wird von **CIM \_ basemetricdefinition** geerbt.</span><span class="sxs-lookup"><span data-stu-id="23790-150">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>



| <span data-ttu-id="23790-151">Wert</span><span class="sxs-lookup"><span data-stu-id="23790-151">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="23790-152">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="23790-152">Meaning</span></span>                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="23790-153"><dt>**Unbekannter**</dt> Wert <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="23790-153"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="23790-154">Der Metrik-Designer hat den **ChangeType** nicht qualifiziert.</span><span class="sxs-lookup"><span data-stu-id="23790-154">The metric designer did not qualify the **ChangeType.**.</span></span><br/>                                                                                                                              |
| <span id="N_A"></span><span id="n_a"></span><dl> <span data-ttu-id="23790-155"><dt>**N/v**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="23790-155"><dt>**N/A**</dt> <dt>2</dt></span></span> </dl>                                                                                       | <span data-ttu-id="23790-156">Wenn die **iscontinuous** -Eigenschaft den Wert "false" hat, ist **ChangeType** nicht sinnvoll und muss auf "N/v" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="23790-156">If the **IsContinuous** property is "false", **ChangeType** does not make sense and must be set to "N/A".</span></span><br/>                                                                             |
| <span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span><dl> <span data-ttu-id="23790-157"><dt>**Gegen**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="23790-157"><dt>**Counter**</dt> <dt>3</dt></span></span> </dl>                                                 | <span data-ttu-id="23790-158">Die Metrik ist eine gegen Metrik.</span><span class="sxs-lookup"><span data-stu-id="23790-158">The metric is a counter metric.</span></span> <span data-ttu-id="23790-159">Diese haben nicht negative ganzzahlige Werte, die sich erhöhen, bis die maximale darstellbare Zahl erreicht ist, und dann umschließen und die Zunahme von 0 beginnen.</span><span class="sxs-lookup"><span data-stu-id="23790-159">These have nonnegative integer values that increase until reaching the maximum representable number and then wrap around and start increasing from 0.</span></span><br/> |
| <span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span><dl> <span data-ttu-id="23790-160"><dt>**Messgerät**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="23790-160"><dt>**Gauge**</dt> <dt>4</dt></span></span> </dl>                                                         | <span data-ttu-id="23790-161">Die Metrik ist eine Messgeräte Metrik.</span><span class="sxs-lookup"><span data-stu-id="23790-161">The metric is a gauge metric.</span></span> <span data-ttu-id="23790-162">Diese verfügen über ganzzahlige oder Gleit Komma Werte, die beliebig vergrößert und verringert werden können.</span><span class="sxs-lookup"><span data-stu-id="23790-162">These have integer or float values that can increase and decrease arbitrarily.</span></span><br/>                                                                          |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="23790-163"><dt>**DMTF reserviert**</dt> <dt>5.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="23790-163"><dt>**DMTF Reserved**</dt> <dt>5..32767</dt></span></span> </dl>                  |                                                                                                                                                                                                  |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="23790-164"><dt> **Anbieter reserviert**</dt> <dt>32768.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="23790-164"><dt>**Vendor Reserved** </dt> <dt>32768..65535 </dt></span></span> </dl> | <span data-ttu-id="23790-165">Anbieter können die **ChangeType** -Eigenschaft im reservierten Bereich des Anbieters erweitern.</span><span class="sxs-lookup"><span data-stu-id="23790-165">Vendors may extend the **ChangeType** property in the vendor reserved range.</span></span><br/>                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="23790-166">**DataType**</span><span class="sxs-lookup"><span data-stu-id="23790-166">**DataType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23790-167">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23790-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="23790-168">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23790-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23790-169">Der Datentyp der Metrik.</span><span class="sxs-lookup"><span data-stu-id="23790-169">The data type of the metric.</span></span> <span data-ttu-id="23790-170">Diese Eigenschaft wird von **CIM \_ basemetricdefinition** geerbt.</span><span class="sxs-lookup"><span data-stu-id="23790-170">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

<dl> <dt>

<span data-ttu-id="23790-171"><span id="boolean"></span><span id="BOOLEAN"></span>**boolescher** Wert (1)</span><span class="sxs-lookup"><span data-stu-id="23790-171"><span id="boolean"></span><span id="BOOLEAN"></span>**boolean** (1)</span></span>
</dt> <dt>

<span data-ttu-id="23790-172"><span id="char16"></span><span id="CHAR16"></span>**char16** (2)</span><span class="sxs-lookup"><span data-stu-id="23790-172"><span id="char16"></span><span id="CHAR16"></span>**char16** (2)</span></span>
</dt> <dt>

<span data-ttu-id="23790-173"><span id="datetime"></span><span id="DATETIME"></span>**DateTime** (3)</span><span class="sxs-lookup"><span data-stu-id="23790-173"><span id="datetime"></span><span id="DATETIME"></span>**datetime** (3)</span></span>
</dt> <dt>

<span data-ttu-id="23790-174"><span id="real32"></span><span id="REAL32"></span>**real32** (4)</span><span class="sxs-lookup"><span data-stu-id="23790-174"><span id="real32"></span><span id="REAL32"></span>**real32** (4)</span></span>
</dt> <dt>

<span data-ttu-id="23790-175"><span id="real64"></span><span id="REAL64"></span>**real64** (5)</span><span class="sxs-lookup"><span data-stu-id="23790-175"><span id="real64"></span><span id="REAL64"></span>**real64** (5)</span></span>
</dt> <dt>

<span data-ttu-id="23790-176"><span id="sint16"></span><span id="SINT16"></span>**sint16** (6)</span><span class="sxs-lookup"><span data-stu-id="23790-176"><span id="sint16"></span><span id="SINT16"></span>**sint16** (6)</span></span>
</dt> <dt>

<span data-ttu-id="23790-177"><span id="sint32"></span><span id="SINT32"></span>**sint32** (7)</span><span class="sxs-lookup"><span data-stu-id="23790-177"><span id="sint32"></span><span id="SINT32"></span>**sint32** (7)</span></span>
</dt> <dt>

<span data-ttu-id="23790-178"><span id="sint64"></span><span id="SINT64"></span>**sint64** (8)</span><span class="sxs-lookup"><span data-stu-id="23790-178"><span id="sint64"></span><span id="SINT64"></span>**sint64** (8)</span></span>
</dt> <dt>

<span data-ttu-id="23790-179"><span id="sint8"></span><span id="SINT8"></span>**sint8** (9)</span><span class="sxs-lookup"><span data-stu-id="23790-179"><span id="sint8"></span><span id="SINT8"></span>**sint8** (9)</span></span>
</dt> <dt>

<span data-ttu-id="23790-180"><span id="string"></span><span id="STRING"></span>**Zeichenfolge** (10)</span><span class="sxs-lookup"><span data-stu-id="23790-180"><span id="string"></span><span id="STRING"></span>**string** (10)</span></span>
</dt> <dt>

<span data-ttu-id="23790-181"><span id="uint16"></span><span id="UINT16"></span>**UInt16** (11)</span><span class="sxs-lookup"><span data-stu-id="23790-181"><span id="uint16"></span><span id="UINT16"></span>**uint16** (11)</span></span>
</dt> <dt>

<span data-ttu-id="23790-182"><span id="uint32"></span><span id="UINT32"></span>**UInt32** (12)</span><span class="sxs-lookup"><span data-stu-id="23790-182"><span id="uint32"></span><span id="UINT32"></span>**uint32** (12)</span></span>
</dt> <dt>

<span data-ttu-id="23790-183"><span id="uint64"></span><span id="UINT64"></span>**UInt64** (13)</span><span class="sxs-lookup"><span data-stu-id="23790-183"><span id="uint64"></span><span id="UINT64"></span>**uint64** (13)</span></span>
</dt> <dt>

<span data-ttu-id="23790-184"><span id="uint8_"></span><span id="UINT8_"></span>**Uint8** (14)</span><span class="sxs-lookup"><span data-stu-id="23790-184"><span id="uint8_"></span><span id="UINT8_"></span>**uint8** (14 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="23790-185">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="23790-185">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23790-186">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="23790-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23790-187">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23790-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23790-188">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="23790-188">A description of the object.</span></span> <span data-ttu-id="23790-189">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="23790-189">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="23790-190">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="23790-190">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23790-191">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="23790-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23790-192">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23790-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23790-193">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="23790-193">A display name for the object.</span></span> <span data-ttu-id="23790-194">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="23790-194">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="23790-195">**Gatheringtype**</span><span class="sxs-lookup"><span data-stu-id="23790-195">**GatheringType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23790-196">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23790-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="23790-197">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23790-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23790-198">Gibt an, wie die Metrikwerte von der zugrunde liegenden Instrumentation erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="23790-198">Indicates how the metric values are gathered by the underlying instrumentation.</span></span> <span data-ttu-id="23790-199">Dies ermöglicht es der Client Anwendung, die richtige Metrik für den Zweck auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="23790-199">This allows the client application to choose the right metric for the purpose.</span></span> <span data-ttu-id="23790-200">Diese Eigenschaft wird von **CIM \_ basemetricdefinition** geerbt.</span><span class="sxs-lookup"><span data-stu-id="23790-200">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span> <span data-ttu-id="23790-201">Dieser Wert kann **null** oder einer der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="23790-201">This may be **Null** or one of the following values.</span></span>



| <span data-ttu-id="23790-202">Wert</span><span class="sxs-lookup"><span data-stu-id="23790-202">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="23790-203">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="23790-203">Meaning</span></span>                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="23790-204"><dt>**Unbekannter**</dt> Wert <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="23790-204"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="23790-205">Der sammungstyp ist nicht bekannt.</span><span class="sxs-lookup"><span data-stu-id="23790-205">The gathering type is not known.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="OnChange"></span><span id="onchange"></span><span id="ONCHANGE"></span><dl> <span data-ttu-id="23790-206"><dt>**OnChange**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="23790-206"><dt>**OnChange**</dt> <dt>2</dt></span></span> </dl>                                             | <span data-ttu-id="23790-207">Die Metrikwerte werden sofort aktualisiert, wenn sich die Werte in der gemessenen Ressource ändern.</span><span class="sxs-lookup"><span data-stu-id="23790-207">The metric values get updated immediately when the values inside of the measured resource change.</span></span><br/>                                                                                                                                                              |
| <span id="Periodic"></span><span id="periodic"></span><span id="PERIODIC"></span><dl> <span data-ttu-id="23790-208"><dt>**Periodisch**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="23790-208"><dt>**Periodic**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="23790-209">Die Metrikwerte werden regelmäßig aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="23790-209">The metric values get updated periodically.</span></span> <span data-ttu-id="23790-210">Beispielsweise wird für eine Client Anwendung ein Metrikwert, der sich auf die aktuelle Zeit bezieht, während jedes Sammlungs Intervalls konstant angezeigt und dann am Ende jedes Sammlungs Intervalls auf den neuen Wert springt.</span><span class="sxs-lookup"><span data-stu-id="23790-210">For instance, to a client application, a metric value that applies to the current time will appear constant during each gathering interval, and then jumps to the new value at the end of each gathering interval.</span></span><br/> |
| <span id="OnRequest"></span><span id="onrequest"></span><span id="ONREQUEST"></span><dl> <span data-ttu-id="23790-211"><dt>**OnRequest**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="23790-211"><dt>**OnRequest**</dt> <dt>4</dt></span></span> </dl>                                         | <span data-ttu-id="23790-212">Der Metrikwert wird jedes Mal bestimmt, wenn er von einer Client Anwendung gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="23790-212">The metric value is determined each time a client application reads it.</span></span><br/>                                                                                                                                                                                        |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="23790-213"><dt>**DMTF reserviert**</dt> <dt>5.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="23790-213"><dt>**DMTF Reserved**</dt> <dt>5..32767</dt></span></span> </dl>                  |                                                                                                                                                                                                                                                                           |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="23790-214"><dt> **Anbieter reserviert**</dt> <dt>32768.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="23790-214"><dt>**Vendor Reserved** </dt> <dt>32768..65535 </dt></span></span> </dl> |                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="23790-215">**Id**</span><span class="sxs-lookup"><span data-stu-id="23790-215">**Id**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23790-216">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="23790-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23790-217">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23790-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23790-218">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="23790-218">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="23790-219">Eine Zeichenfolge, die die metrikdefinition eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="23790-219">A string that uniquely identifies the metric definition.</span></span> <span data-ttu-id="23790-220">Diese Eigenschaft wird von **CIM \_ basemetricdefinition** geerbt.</span><span class="sxs-lookup"><span data-stu-id="23790-220">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> <dt>

<span data-ttu-id="23790-221">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="23790-221">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23790-222">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="23790-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23790-223">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23790-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23790-224">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="23790-224">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="23790-225">Eine Zeichenfolge, die eine Instanz dieser Klasse eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="23790-225">A string that uniquely identifies an instance of this class.</span></span> <span data-ttu-id="23790-226">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="23790-226">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="23790-227">**IsContinuous**</span><span class="sxs-lookup"><span data-stu-id="23790-227">**IsContinuous**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23790-228">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="23790-228">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="23790-229">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23790-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23790-230">Gibt an, ob der Metrikwert kontinuierlich oder Skalar ist.</span><span class="sxs-lookup"><span data-stu-id="23790-230">Indicates whether the metric value is continuous or scalar.</span></span> <span data-ttu-id="23790-231">Leistungsmetriken sind ein Beispiel für eine kontinuierliche Metrik.</span><span class="sxs-lookup"><span data-stu-id="23790-231">Performance metrics are an example of a continuous metric.</span></span> <span data-ttu-id="23790-232">Beispiele für skalare Metriken sind Fehlercodes oder Betriebszustände.</span><span class="sxs-lookup"><span data-stu-id="23790-232">Examples of scalar metrics include error codes or operational states.</span></span> <span data-ttu-id="23790-233">Kontinuierliche Metriken können mit der "größer als"-Beziehung verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="23790-233">Continuous metrics can be compared by using the "greater than" relation.</span></span> <span data-ttu-id="23790-234">Diese Eigenschaft wird von **CIM \_ basemetricdefinition** geerbt.</span><span class="sxs-lookup"><span data-stu-id="23790-234">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> <dt>

<span data-ttu-id="23790-235">**Name**</span><span class="sxs-lookup"><span data-stu-id="23790-235">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23790-236">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="23790-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23790-237">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23790-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23790-238">Der Name der Metrik.</span><span class="sxs-lookup"><span data-stu-id="23790-238">The name of the metric.</span></span> <span data-ttu-id="23790-239">Diese Eigenschaft wird von **CIM \_ basemetricdefinition** geerbt.</span><span class="sxs-lookup"><span data-stu-id="23790-239">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> <dt>

<span data-ttu-id="23790-240">**Programmaticunits**</span><span class="sxs-lookup"><span data-stu-id="23790-240">**ProgrammaticUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23790-241">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="23790-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23790-242">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23790-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23790-243">Identifiziert die bestimmten Einheiten eines Werts.</span><span class="sxs-lookup"><span data-stu-id="23790-243">Identifies the specific units of a value.</span></span> <span data-ttu-id="23790-244">Der Wert dieser Eigenschaft ist ein gültiger Wert des Qualifizierers für programmatische Einheiten, wie in Anhang C. 1 von [DSP0004 v 2.4](https://www.dmtf.org/sites/default/files/standards/documents/DSP0004_2.5.0.pdf) oder höher definiert.</span><span class="sxs-lookup"><span data-stu-id="23790-244">The value of this property will be a legal value of the Programmatic Units qualifier as defined in Appendix C.1 of [DSP0004 V2.4](https://www.dmtf.org/sites/default/files/standards/documents/DSP0004_2.5.0.pdf) or later.</span></span> <span data-ttu-id="23790-245">Diese Eigenschaft wird von **CIM \_ basemetricdefinition** geerbt.</span><span class="sxs-lookup"><span data-stu-id="23790-245">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> <dt>

<span data-ttu-id="23790-246">**Timescope**</span><span class="sxs-lookup"><span data-stu-id="23790-246">**TimeScope**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23790-247">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23790-247">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="23790-248">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23790-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23790-249">Gibt den Zeitbereich an, für den der Metrikwert gilt.</span><span class="sxs-lookup"><span data-stu-id="23790-249">Indicates the time scope to which the metric value applies.</span></span> <span data-ttu-id="23790-250">Diese Eigenschaft wird von **CIM \_ basemetricdefinition** geerbt.</span><span class="sxs-lookup"><span data-stu-id="23790-250">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>



| <span data-ttu-id="23790-251">Wert</span><span class="sxs-lookup"><span data-stu-id="23790-251">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="23790-252">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="23790-252">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="23790-253"><dt>**Unbekannter**</dt> Wert <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="23790-253"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="23790-254">Der Zeitbereich wurde vom Metrik-Designer nicht qualifiziert oder ist dem Anbieter nicht bekannt.</span><span class="sxs-lookup"><span data-stu-id="23790-254">The time scope was not qualified by the metric designer or is unknown to the provider.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="Point"></span><span id="point"></span><span id="POINT"></span><dl> <span data-ttu-id="23790-255"><dt>**Punkt**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="23790-255"><dt>**Point**</dt> <dt>2</dt></span></span> </dl>                                                         | <span data-ttu-id="23790-256">Die Metrik gilt für einen bestimmten Zeitpunkt.</span><span class="sxs-lookup"><span data-stu-id="23790-256">The metric applies to a point in time.</span></span> <span data-ttu-id="23790-257">Die **timestamp** -Eigenschaft gibt auf der entsprechenden [**MSVM \_ basemetricvalue**](msvm-basemetricvalue.md) -Instanz den Zeitpunkt an, und die **Duration** -Eigenschaft ist immer 0.</span><span class="sxs-lookup"><span data-stu-id="23790-257">On the corresponding [**Msvm\_BaseMetricValue**](msvm-basemetricvalue.md) instances, the **TimeStamp** property specifies the point in time, and the **Duration** property is always 0.</span></span><br/>                                                                                                                                                                                                                                                                                              |
| <span id="Interval"></span><span id="interval"></span><span id="INTERVAL"></span><dl> <span data-ttu-id="23790-258"><dt>**Intervall**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="23790-258"><dt>**Interval**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="23790-259">Die Metrik gilt für ein Zeitintervall.</span><span class="sxs-lookup"><span data-stu-id="23790-259">The metric applies to a time interval.</span></span> <span data-ttu-id="23790-260">Die **timestamp** -Eigenschaft gibt das Ende des Zeitintervalls an, und die **Duration** -Eigenschaft gibt deren Dauer an. [**\_**](msvm-basemetricvalue.md)</span><span class="sxs-lookup"><span data-stu-id="23790-260">On the corresponding [**Msvm\_BaseMetricValue**](msvm-basemetricvalue.md) instances, the **TimeStamp** property specifies the end of the time interval, and the **Duration** property specifies its duration.</span></span><br/>                                                                                                                                                                                                                                                                        |
| <span id="StartupInterval"></span><span id="startupinterval"></span><span id="STARTUPINTERVAL"></span><dl> <span data-ttu-id="23790-261"><dt>**Startupinterval**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="23790-261"><dt>**StartupInterval**</dt> <dt>4</dt></span></span> </dl>                 | <span data-ttu-id="23790-262">Die Metrik bezieht sich auf ein Zeitintervall, das beim Start der gemessenen Ressource begonnen hat (d. h. das von metricdefforme zugeordnete managedelta).</span><span class="sxs-lookup"><span data-stu-id="23790-262">The metric applies to a time interval that began at the startup of the measured resource (that is, the ManagedElement associated by MetricDefForMe).</span></span> <span data-ttu-id="23790-263">Die **timestamp** -Eigenschaft gibt das Ende des Zeitintervalls in den entsprechenden [**MSVM \_ basemetricvalue**](msvm-basemetricvalue.md) -Instanzen an.</span><span class="sxs-lookup"><span data-stu-id="23790-263">On the corresponding [**Msvm\_BaseMetricValue**](msvm-basemetricvalue.md) instances, the **TimeStamp** property specifies the end of the time interval.</span></span> <span data-ttu-id="23790-264">Wenn die **Duration** -Eigenschaft den Wert 0 hat, gibt dies an, dass die Startzeit der gemessenen Ressource unbekannt ist.</span><span class="sxs-lookup"><span data-stu-id="23790-264">If the **Duration** property is 0, this indicates that the startup time of the measured resource is unknown.</span></span> <span data-ttu-id="23790-265">Andernfalls gibt **Duration** die Dauer zwischen dem Start der Ressource und dem **Zeitstempel** an.</span><span class="sxs-lookup"><span data-stu-id="23790-265">Otherwise, **Duration** specifies the duration between startup of the resource and **TimeStamp**.</span></span><br/> |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="23790-266"><dt>**DMTF reserviert**</dt> <dt>5.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="23790-266"><dt>**DMTF Reserved**</dt> <dt>5..32767</dt></span></span> </dl>                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="23790-267"><dt> **Anbieter reserviert**</dt> <dt>32768.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="23790-267"><dt>**Vendor Reserved** </dt> <dt>32768..65535 </dt></span></span> </dl> |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

</dd> <dt>

<span data-ttu-id="23790-268">**Einheiten**</span><span class="sxs-lookup"><span data-stu-id="23790-268">**Units**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23790-269">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="23790-269">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23790-270">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="23790-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23790-271">Identifiziert die bestimmten Einheiten eines Werts, z. b. "Megabyte".</span><span class="sxs-lookup"><span data-stu-id="23790-271">Identifies the specific units of a value, for example, "megabytes".</span></span> <span data-ttu-id="23790-272">Diese Eigenschaft wird von **CIM \_ basemetricdefinition** geerbt.</span><span class="sxs-lookup"><span data-stu-id="23790-272">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="23790-273">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="23790-273">Requirements</span></span>



| <span data-ttu-id="23790-274">Anforderung</span><span class="sxs-lookup"><span data-stu-id="23790-274">Requirement</span></span> | <span data-ttu-id="23790-275">Wert</span><span class="sxs-lookup"><span data-stu-id="23790-275">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23790-276">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="23790-276">Minimum supported client</span></span><br/> | <span data-ttu-id="23790-277">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="23790-277">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="23790-278">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="23790-278">Minimum supported server</span></span><br/> | <span data-ttu-id="23790-279">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="23790-279">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="23790-280">Namespace</span><span class="sxs-lookup"><span data-stu-id="23790-280">Namespace</span></span><br/>                | <span data-ttu-id="23790-281">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="23790-281">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="23790-282">MOF</span><span class="sxs-lookup"><span data-stu-id="23790-282">MOF</span></span><br/>                      | <dl> <span data-ttu-id="23790-283"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="23790-283"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="23790-284">DLL</span><span class="sxs-lookup"><span data-stu-id="23790-284">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23790-285"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="23790-285"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

