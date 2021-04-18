---
description: Stellt eine metrikdefinition dar, die die Metadaten für ein CIM \_ metricinstance-Objekt enthält.
ms.assetid: 6abfb0dc-e80b-4ca6-89d9-2e43283d0abe
title: CIM_BaseMetricDefinition-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BaseMetricDefinition
- CIM_BaseMetricDefinition.Id
- CIM_BaseMetricDefinition.Name
- CIM_BaseMetricDefinition.DataType
- CIM_BaseMetricDefinition.Calculable
- CIM_BaseMetricDefinition.Units
- CIM_BaseMetricDefinition.BreakdownDimensions
- CIM_BaseMetricDefinition.IsContinuous
- CIM_BaseMetricDefinition.ChangeType
- CIM_BaseMetricDefinition.TimeScope
- CIM_BaseMetricDefinition.GatheringType
- CIM_BaseMetricDefinition.ProgrammaticUnits
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cac965ed1eae59f1c269d897a12e9aa116183eb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350977"
---
# <a name="cim_basemetricdefinition-class"></a><span data-ttu-id="133ad-103">CIM \_ basemetricdefinition-Klasse</span><span class="sxs-lookup"><span data-stu-id="133ad-103">CIM\_BaseMetricDefinition class</span></span>

<span data-ttu-id="133ad-104">Stellt eine metrikdefinition dar, die die Metadaten für ein **CIM \_ metricinstance** -Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="133ad-104">Represents a metric definition that contains the meta data for a **CIM\_MetricInstance** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="133ad-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="133ad-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_BaseMetricDefinition : CIM_ManagedElement
{
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

## <a name="members"></a><span data-ttu-id="133ad-106">Member</span><span class="sxs-lookup"><span data-stu-id="133ad-106">Members</span></span>

<span data-ttu-id="133ad-107">Die **CIM \_ basemetricdefinition** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="133ad-107">The **CIM\_BaseMetricDefinition** class has these types of members:</span></span>

-   [<span data-ttu-id="133ad-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="133ad-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="133ad-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="133ad-109">Properties</span></span>

<span data-ttu-id="133ad-110">Die **CIM \_ basemetricdefinition** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="133ad-110">The **CIM\_BaseMetricDefinition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="133ad-111">**Breakdowndimensionen**</span><span class="sxs-lookup"><span data-stu-id="133ad-111">**BreakdownDimensions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="133ad-112">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="133ad-112">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="133ad-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="133ad-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="133ad-114">Ein Array, das freie Format Zeichenfolgen enthält, die verwendet werden können, um Abfragen von [**CIM \_ basemetricvalue**](cim-basemetricvalue.md) -Objekten an einer bestimmten Dimension zu unterbrechen.</span><span class="sxs-lookup"><span data-stu-id="133ad-114">An array that contains free format strings that can be used to break down queries of [**CIM\_BaseMetricValue**](cim-basemetricvalue.md) objects along a certain dimension.</span></span> <span data-ttu-id="133ad-115">Die Zeichen folgen sollten für die Endbenutzer der Metrikdaten sinnvoll sein.</span><span class="sxs-lookup"><span data-stu-id="133ad-115">The strings should be meaningful to the end users of the metric data.</span></span> <span data-ttu-id="133ad-116">Außerdem sollten die Zeichen folgen durch die zugrunde liegende Instrumentation angeben, welche aufbruchteil Dimensionen für die metrikdefinition unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="133ad-116">In addition, the strings should indicate which break down dimensions are supported for the metric definition, by the underlying instrumentation.</span></span>

<span data-ttu-id="133ad-117">Ein Beispiel hierfür ist ein Transaktions Name, der das Unterbrechen des Gesamtwerts für alle Transaktionen in eine Reihe von Werten zulässt, eine für jeden Transaktions Namen.</span><span class="sxs-lookup"><span data-stu-id="133ad-117">An example is a transaction name that allows the break down of the total value for all transactions into a set of values, one for each transaction name.</span></span> <span data-ttu-id="133ad-118">Bei anderen Beispielen handelt es sich um ein Anwendungssystem oder einen Benutzergruppen Namen.</span><span class="sxs-lookup"><span data-stu-id="133ad-118">Other examples are an application system, or a user group name.</span></span>

</dd> <dt>

<span data-ttu-id="133ad-119">**Bares**</span><span class="sxs-lookup"><span data-stu-id="133ad-119">**Calculable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="133ad-120">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="133ad-120">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="133ad-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="133ad-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="133ad-122">Die Merkmale der Metrik, die zum Durchführen von Berechnungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="133ad-122">The characteristics of the metric used to perform calculations.</span></span>

<dt>

<span id="Non-calculable"></span><span id="non-calculable"></span><span id="NON-CALCULABLE"></span>

<span data-ttu-id="133ad-123"><span id="Non-calculable"></span><span id="non-calculable"></span><span id="NON-CALCULABLE"></span>**Nicht berechenbar** (1)</span><span class="sxs-lookup"><span data-stu-id="133ad-123"><span id="Non-calculable"></span><span id="non-calculable"></span><span id="NON-CALCULABLE"></span>**Non-calculable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="133ad-124">Eine Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="133ad-124">A string.</span></span> <span data-ttu-id="133ad-125">Arithmetik ist nicht sinnvoll.</span><span class="sxs-lookup"><span data-stu-id="133ad-125">Arithmetic makes no sense.</span></span>

</dd> <dt>

<span id="Summable"></span><span id="summable"></span><span id="SUMMABLE"></span>

<span data-ttu-id="133ad-126"><span id="Summable"></span><span id="summable"></span><span id="SUMMABLE"></span>**Sumable** (2)</span><span class="sxs-lookup"><span data-stu-id="133ad-126"><span id="Summable"></span><span id="summable"></span><span id="SUMMABLE"></span>**Summable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="133ad-127">Es ist sinnvoll, diesen Wert über viele Instanzen von zu addieren, z. b. uni-fwork, wie z. b. die Anzahl der Dateien, die in einem Sicherungsauftrag verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="133ad-127">It is reasonable to sum this value over many instances of e.g., UnitOfWork, such as the number of files processed in a backup job.</span></span> <span data-ttu-id="133ad-128">Wenn es sich bei jedem Sicherungsauftrag beispielsweise um einen Unito-work-Vorgang handelt und jeder Auftrag 27.000 Dateien im Durchschnitt sichert, ist es sinnvoll, zu sagen, dass 100 Sicherungsaufträge 2,7 Millionen Dateien verarbeitet haben.</span><span class="sxs-lookup"><span data-stu-id="133ad-128">For example, if each backup job is a UnitOfWork, and each job backs up 27,000 files on average, then it makes sense to say that 100 backup jobs processed 2,700,000 files.</span></span>

</dd> <dt>

<span id="Non-summable"></span><span id="non-summable"></span><span id="NON-SUMMABLE"></span>

<span data-ttu-id="133ad-129"><span id="Non-summable"></span><span id="non-summable"></span><span id="NON-SUMMABLE"></span>**Nicht summier Bar** (3)</span><span class="sxs-lookup"><span data-stu-id="133ad-129"><span id="Non-summable"></span><span id="non-summable"></span><span id="NON-SUMMABLE"></span>**Non-summable** (3)</span></span>


</dt> <dd>

<span data-ttu-id="133ad-130">Es ist nicht sinnvoll, diesen Wert über viele Instanzen von Uni-fwork zu addieren.</span><span class="sxs-lookup"><span data-stu-id="133ad-130">It does not make sense to sum this value over many instances of UnitOfWork.</span></span> <span data-ttu-id="133ad-131">Ein Beispiel wäre eine Metrik, die die Länge der Warteschlange beim Eintreffen eines Auftrags auf einem Server misst.</span><span class="sxs-lookup"><span data-stu-id="133ad-131">An example would be a metric that measures the queue length when a job arrives at a server.</span></span> <span data-ttu-id="133ad-132">Wenn es sich bei jedem Auftrag um einen unitwork-Vorgang handelt und die durchschnittliche Warteschlangen Länge bei Eintreffen der einzelnen Aufträge 33 beträgt, ist es nicht sinnvoll, zu sagen, dass die Warteschlangen Länge für 100 Aufträge 3300 beträgt.</span><span class="sxs-lookup"><span data-stu-id="133ad-132">If each job is a UnitOfWork, and the average queue length when each job arrives is 33, it does not make sense to say that the queue length for 100 jobs is 3300.</span></span> <span data-ttu-id="133ad-133">Es ist sinnvoll, zu sagen, dass der Mittelwert 33 ist.</span><span class="sxs-lookup"><span data-stu-id="133ad-133">It does make sense to say that the mean is 33.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="133ad-134">**ChangeType**</span><span class="sxs-lookup"><span data-stu-id="133ad-134">**ChangeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="133ad-135">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="133ad-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="133ad-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="133ad-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="133ad-137">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ basemetricdefinition**".**Iscontinuous**")</span><span class="sxs-lookup"><span data-stu-id="133ad-137">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_BaseMetricDefinition**.**IsContinuous**")</span></span>
</dt> </dl>

<span data-ttu-id="133ad-138">Gibt an, wie sich der Metrikwert mithilfe allgemeiner Attribute ändert, wie z. b. Richtungsänderung, Mindest-und Höchstwerte und Wrapping Semantik.</span><span class="sxs-lookup"><span data-stu-id="133ad-138">Indicates how the metric value changes using common attributes such as direction change, minimum and maximum values, and wrapping semantics.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="133ad-139"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="133ad-139"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="133ad-140">Der Metrik-Designer hat den ChangeType nicht qualifiziert.</span><span class="sxs-lookup"><span data-stu-id="133ad-140">The metric designer did not qualify the ChangeType.</span></span>

</dd> <dt>

<span id="N_A"></span><span id="n_a"></span>

<span data-ttu-id="133ad-141"><span id="N_A"></span><span id="n_a"></span>**N/v** (2)</span><span class="sxs-lookup"><span data-stu-id="133ad-141"><span id="N_A"></span><span id="n_a"></span>**N/A** (2)</span></span>


</dt> <dd>

<span data-ttu-id="133ad-142">Wenn die Eigenschaft "iscontinuous" den Wert "false" hat, ist ChangeType nicht sinnvoll und muss auf "N/v" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="133ad-142">If the "IsContinuous" property is "false", ChangeType does not make sense and MUST be is set to "N/A".</span></span>

</dd> <dt>

<span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>

<span data-ttu-id="133ad-143"><span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>**Counter** (3)</span><span class="sxs-lookup"><span data-stu-id="133ad-143"><span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>**Counter** (3)</span></span>


</dt> <dd>

<span data-ttu-id="133ad-144">Die Metrik ist eine gegen Metrik.</span><span class="sxs-lookup"><span data-stu-id="133ad-144">The metric is a counter metric.</span></span> <span data-ttu-id="133ad-145">Diese verfügen über nicht negative ganzzahlige Werte, die monoton ansteigen, bis die maximale darstellbare Zahl erreicht und dann umbrochen wird und die Zunahme von 0 beginnt.</span><span class="sxs-lookup"><span data-stu-id="133ad-145">These have non-negative integer values which increase monotonically until reaching the maximum representable number and then wrap around and start increasing from 0.</span></span> <span data-ttu-id="133ad-146">Solche Leistungsindikatoren, auch als Rollover-Indikatoren bezeichnet, können zum Beispiel zum zählen der Anzahl von Netzwerkfehlern oder der Anzahl der verarbeiteten Transaktionen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="133ad-146">Such counters, also known as rollover counters, can be used for instance to count the number of network errors or the number of transactions processed.</span></span> <span data-ttu-id="133ad-147">Die einzige Möglichkeit für eine Client Anwendung, Wrap-Problem Umgehungen nachzuverfolgen, besteht darin, den Wert des Zählers in angemessenen kurzen Intervallen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="133ad-147">The only way for a client application to keep track of wrap arounds is to retrieve the value of the counter in appropriately short intervals.</span></span>

</dd> <dt>

<span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>

<span data-ttu-id="133ad-148"><span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>**Messgerät** (4)</span><span class="sxs-lookup"><span data-stu-id="133ad-148"><span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>**Gauge** (4)</span></span>


</dt> <dd>

<span data-ttu-id="133ad-149">Die Metrik ist eine Messgeräte Metrik.</span><span class="sxs-lookup"><span data-stu-id="133ad-149">The metric is a gauge metric.</span></span> <span data-ttu-id="133ad-150">Diese verfügen über ganzzahlige oder Gleit Komma Werte, die beliebig vergrößert und verringert werden können.</span><span class="sxs-lookup"><span data-stu-id="133ad-150">These have integer or float values that can increase and decrease arbitrarily.</span></span> <span data-ttu-id="133ad-151">Ein Messgerät darf nicht bei Erreichen der minimalen oder maximalen darstellbaren Zahl eingeschlossen werden, sondern der Wert "Sticks" an dieser Zahl.</span><span class="sxs-lookup"><span data-stu-id="133ad-151">A gauge MUST NOT wrap when reaching the minimum or maximum representable number, instead, the value "sticks" at that number.</span></span> <span data-ttu-id="133ad-152">Minimale oder maximale Werte innerhalb des darstellbaren Wertebereichs, bei dem der Metrikwert "Sticks" ist oder nicht definiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="133ad-152">Minimum or maximum values inside of the representable value range at which the metric value "sticks", may or may not be defined.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="133ad-153"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (5.. 32767)</span><span class="sxs-lookup"><span data-stu-id="133ad-153"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (5..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="133ad-154"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Anbieter reserviert** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="133ad-154"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="133ad-155">**DataType**</span><span class="sxs-lookup"><span data-stu-id="133ad-155">**DataType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="133ad-156">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="133ad-156">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="133ad-157">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="133ad-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="133ad-158">Der Datentyp der Metrik.</span><span class="sxs-lookup"><span data-stu-id="133ad-158">The data type of the metric.</span></span>

<dt>

<span id="boolean"></span><span id="BOOLEAN"></span>

<span data-ttu-id="133ad-159">**boolescher** Wert (1)</span><span class="sxs-lookup"><span data-stu-id="133ad-159">**boolean** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="char16"></span><span id="CHAR16"></span>

<span data-ttu-id="133ad-160">**char16** (2)</span><span class="sxs-lookup"><span data-stu-id="133ad-160">**char16** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="datetime"></span><span id="DATETIME"></span>

<span data-ttu-id="133ad-161">**DateTime** (3)</span><span class="sxs-lookup"><span data-stu-id="133ad-161">**datetime** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="real32"></span><span id="REAL32"></span>

<span data-ttu-id="133ad-162">**real32** (4)</span><span class="sxs-lookup"><span data-stu-id="133ad-162">**real32** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="real64"></span><span id="REAL64"></span>

<span data-ttu-id="133ad-163">**real64** (5)</span><span class="sxs-lookup"><span data-stu-id="133ad-163">**real64** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="sint16"></span><span id="SINT16"></span>

<span data-ttu-id="133ad-164">**sint16** (6)</span><span class="sxs-lookup"><span data-stu-id="133ad-164">**sint16** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="sint32"></span><span id="SINT32"></span>

<span data-ttu-id="133ad-165">**sint32** (7)</span><span class="sxs-lookup"><span data-stu-id="133ad-165">**sint32** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="sint64"></span><span id="SINT64"></span>

<span data-ttu-id="133ad-166">**sint64** (8)</span><span class="sxs-lookup"><span data-stu-id="133ad-166">**sint64** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="sint8"></span><span id="SINT8"></span>

<span data-ttu-id="133ad-167">**sint8** (9)</span><span class="sxs-lookup"><span data-stu-id="133ad-167">**sint8** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="string"></span><span id="STRING"></span>

<span data-ttu-id="133ad-168">**Zeichenfolge** (10)</span><span class="sxs-lookup"><span data-stu-id="133ad-168">**string** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="uint16"></span><span id="UINT16"></span>

<span data-ttu-id="133ad-169">**UInt16** (11)</span><span class="sxs-lookup"><span data-stu-id="133ad-169">**uint16** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="uint32"></span><span id="UINT32"></span>

<span data-ttu-id="133ad-170">**UInt32** (12)</span><span class="sxs-lookup"><span data-stu-id="133ad-170">**uint32** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="uint64"></span><span id="UINT64"></span>

<span data-ttu-id="133ad-171">**UInt64** (13)</span><span class="sxs-lookup"><span data-stu-id="133ad-171">**uint64** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="uint8"></span><span id="UINT8"></span>

<span data-ttu-id="133ad-172">**Uint8** (14)</span><span class="sxs-lookup"><span data-stu-id="133ad-172">**uint8** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="133ad-173">**Gatheringtype**</span><span class="sxs-lookup"><span data-stu-id="133ad-173">**GatheringType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="133ad-174">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="133ad-174">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="133ad-175">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="133ad-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="133ad-176">Gibt an, wie die Metrikwerte von der zugrunde liegenden Instrumentation erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="133ad-176">Indicates how the metric values are gathered by the underlying instrumentation.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="133ad-177"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="133ad-177"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="133ad-178">Gibt an, dass der gatheringtype nicht bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="133ad-178">Indicates that the GatheringType is not known.</span></span>

</dd> <dt>

<span id="OnChange"></span><span id="onchange"></span><span id="ONCHANGE"></span>

<span data-ttu-id="133ad-179"><span id="OnChange"></span><span id="onchange"></span><span id="ONCHANGE"></span>**OnChange** (2)</span><span class="sxs-lookup"><span data-stu-id="133ad-179"><span id="OnChange"></span><span id="onchange"></span><span id="ONCHANGE"></span>**OnChange** (2)</span></span>


</dt> <dd>

<span data-ttu-id="133ad-180">Gibt an, dass die CIM-Metrikwerte sofort aktualisiert werden, wenn sich die Werte in der gemessenen Ressource ändern.</span><span class="sxs-lookup"><span data-stu-id="133ad-180">Indicates that the CIM metric values get updated immediately when the values inside of the measured resource change.</span></span> <span data-ttu-id="133ad-181">Die Werte von OnChange-Metriken entsprechen wirklich der aktuellen Situation innerhalb der Ressource.</span><span class="sxs-lookup"><span data-stu-id="133ad-181">The values of OnChange metrics truly reflect the current situation within the resource at any time.</span></span> <span data-ttu-id="133ad-182">Ein Beispiel hierfür ist die Anzahl der angemeldeten Benutzer, die sofort aktualisiert werden, wenn sich Benutzer anmelden und abmelden.</span><span class="sxs-lookup"><span data-stu-id="133ad-182">An example is the number of logged on users that gets updated immediately as users log on and off.</span></span>

</dd> <dt>

<span id="Periodic"></span><span id="periodic"></span><span id="PERIODIC"></span>

<span data-ttu-id="133ad-183"><span id="Periodic"></span><span id="periodic"></span><span id="PERIODIC"></span>**Periodisch** (3)</span><span class="sxs-lookup"><span data-stu-id="133ad-183"><span id="Periodic"></span><span id="periodic"></span><span id="PERIODIC"></span>**Periodic** (3)</span></span>


</dt> <dd>

<span data-ttu-id="133ad-184">": Gibt an, dass die CIM-Metrikwerte regelmäßig aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="133ad-184">": Indicates that the CIM metric values get updated periodically.</span></span> <span data-ttu-id="133ad-185">Beispielsweise wird für eine Client Anwendung ein Metrikwert, der auf die aktuelle Zeit angewendet wird, während jedes Sammlungs Intervalls konstant angezeigt und dann am Ende jedes Sammlungs Intervalls auf den neuen Wert überspringt.</span><span class="sxs-lookup"><span data-stu-id="133ad-185">For instance, to a client application, a metric value applying to the current time will appear constant during each gathering interval, and then jumps to the new value at the end of each gathering interval.</span></span>

</dd> <dt>

<span id="OnRequest"></span><span id="onrequest"></span><span id="ONREQUEST"></span>

<span data-ttu-id="133ad-186"><span id="OnRequest"></span><span id="onrequest"></span><span id="ONREQUEST"></span>**OnRequest** (4)</span><span class="sxs-lookup"><span data-stu-id="133ad-186"><span id="OnRequest"></span><span id="onrequest"></span><span id="ONREQUEST"></span>**OnRequest** (4)</span></span>


</dt> <dd>

<span data-ttu-id="133ad-187">Gibt an, dass der CIM-Metrikwert bei jedem Lesen durch eine Client Anwendung bestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="133ad-187">Indicates that the CIM metric value is determined each time a client application reads it.</span></span> <span data-ttu-id="133ad-188">Die Werte von OnRequest-Metriken geben tatsächlich die aktuelle Situation innerhalb der Ressource zurück, wenn jemand Sie anfordert.</span><span class="sxs-lookup"><span data-stu-id="133ad-188">The values of OnRequest metrics truly return the current situation within the resource if somebody asks for it.</span></span> <span data-ttu-id="133ad-189">Allerdings werden Sie nicht als "nicht überwacht" geändert, weshalb das Abonnieren von Wertänderungen von OnRequest-Metriken nicht empfohlen wird.</span><span class="sxs-lookup"><span data-stu-id="133ad-189">However, they do not change "unobserved", and therefore subscribing for value changes of OnRequest metrics is NOT RECOMMENDED.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="133ad-190"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (5.. 32767)</span><span class="sxs-lookup"><span data-stu-id="133ad-190"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (5..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="133ad-191"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Anbieter reserviert** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="133ad-191"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="133ad-192">**Id**</span><span class="sxs-lookup"><span data-stu-id="133ad-192">**Id**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="133ad-193">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="133ad-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="133ad-194">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="133ad-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="133ad-195">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="133ad-195">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="133ad-196">Die eindeutige ID der metrikdefinition.</span><span class="sxs-lookup"><span data-stu-id="133ad-196">The unique ID of the metric definition.</span></span> <span data-ttu-id="133ad-197">Die UUID/GUIDs von Open Software Foundation (OSF) werden empfohlen.</span><span class="sxs-lookup"><span data-stu-id="133ad-197">Open Software Foundation (OSF) UUID/GUIDs are recommended.</span></span>

</dd> <dt>

<span data-ttu-id="133ad-198">**IsContinuous**</span><span class="sxs-lookup"><span data-stu-id="133ad-198">**IsContinuous**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="133ad-199">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="133ad-199">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="133ad-200">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="133ad-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="133ad-201">True, wenn der Metrikwert kontinuierlich ist. andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="133ad-201">True if the metric value is continuous; otherwise, false.</span></span>

</dd> <dt>

<span data-ttu-id="133ad-202">**Name**</span><span class="sxs-lookup"><span data-stu-id="133ad-202">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="133ad-203">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="133ad-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="133ad-204">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="133ad-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="133ad-205">Der Name der Metrik.</span><span class="sxs-lookup"><span data-stu-id="133ad-205">The name of the metric.</span></span> <span data-ttu-id="133ad-206">Dieser Name muss nicht eindeutig sein, sollte jedoch beschreibend sein und Leerzeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="133ad-206">This name does not have to be unique, but should be descriptive and may contain blank spaces.</span></span>

</dd> <dt>

<span data-ttu-id="133ad-207">**Programmaticunits**</span><span class="sxs-lookup"><span data-stu-id="133ad-207">**ProgrammaticUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="133ad-208">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="133ad-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="133ad-209">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="133ad-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="133ad-210">Die spezifischen Einheiten eines Werts.</span><span class="sxs-lookup"><span data-stu-id="133ad-210">The specific units of a value.</span></span> <span data-ttu-id="133ad-211">Der Wert dieser Eigenschaft muss ein gültiger Wert des Qualifizierers für programmgesteuerte Einheiten sein, wie in Anhang C. 1 von DSP0004 v 2.4 oder höher definiert.</span><span class="sxs-lookup"><span data-stu-id="133ad-211">The value of this property should be a legal value of the Programmatic Units qualifier as defined in Appendix C.1 of DSP0004 V2.4 or later.</span></span>

</dd> <dt>

<span data-ttu-id="133ad-212">**Timescope**</span><span class="sxs-lookup"><span data-stu-id="133ad-212">**TimeScope**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="133ad-213">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="133ad-213">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="133ad-214">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="133ad-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="133ad-215">Qualifizierer: [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ basemetricvalue**](cim-basemetricvalue.md)".**Zeitstempel**","**CIM \_ basemetricvalue**.**Dauer**")</span><span class="sxs-lookup"><span data-stu-id="133ad-215">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_BaseMetricValue**](cim-basemetricvalue.md).**TimeStamp**", "**CIM\_BaseMetricValue**.**Duration**")</span></span>
</dt> </dl>

<span data-ttu-id="133ad-216">Der Zeitbereich, der für den Metrik-Designer gilt.</span><span class="sxs-lookup"><span data-stu-id="133ad-216">The time scope that applies to the metric designer.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="133ad-217"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="133ad-217"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="133ad-218">Gibt an, dass der Zeitbereich vom Metrik-Designer nicht qualifiziert wurde oder dem Anbieter unbekannt ist.</span><span class="sxs-lookup"><span data-stu-id="133ad-218">Indicates the time scope was not qualified by the metric designer, or is unknown to the provider.</span></span>

</dd> <dt>

<span id="Point"></span><span id="point"></span><span id="POINT"></span>

<span data-ttu-id="133ad-219"><span id="Point"></span><span id="point"></span><span id="POINT"></span>**Punkt** (2)</span><span class="sxs-lookup"><span data-stu-id="133ad-219"><span id="Point"></span><span id="point"></span><span id="POINT"></span>**Point** (2)</span></span>


</dt> <dd>

<span data-ttu-id="133ad-220">Gibt an, dass die Metrik für einen bestimmten Zeitpunkt gilt.</span><span class="sxs-lookup"><span data-stu-id="133ad-220">Indicates that the metric applies to a point in time.</span></span> <span data-ttu-id="133ad-221">In den entsprechenden basemetricvalue-Instanzen gibt Timestamp den Zeitpunkt und die Dauer immer 0 an.</span><span class="sxs-lookup"><span data-stu-id="133ad-221">On the corresponding BaseMetricValue instances, TimeStamp specifies the point in time and Duration is always 0.</span></span>

</dd> <dt>

<span id="Interval"></span><span id="interval"></span><span id="INTERVAL"></span>

<span data-ttu-id="133ad-222"><span id="Interval"></span><span id="interval"></span><span id="INTERVAL"></span>**Intervall** (3)</span><span class="sxs-lookup"><span data-stu-id="133ad-222"><span id="Interval"></span><span id="interval"></span><span id="INTERVAL"></span>**Interval** (3)</span></span>


</dt> <dd>

<span data-ttu-id="133ad-223">Gibt an, dass die Metrik für ein Zeitintervall gilt.</span><span class="sxs-lookup"><span data-stu-id="133ad-223">Indicates that the metric applies to a time interval.</span></span> <span data-ttu-id="133ad-224">In den entsprechenden basemetricvalue-Instanzen gibt Timestamp das Ende des Zeitintervalls an, und die Dauer gibt deren Dauer an.</span><span class="sxs-lookup"><span data-stu-id="133ad-224">On the corresponding BaseMetricValue instances, TimeStamp specifies the end of the time interval and Duration specifies its duration</span></span>

</dd> <dt>

<span id="StartupInterval"></span><span id="startupinterval"></span><span id="STARTUPINTERVAL"></span>

<span data-ttu-id="133ad-225"><span id="StartupInterval"></span><span id="startupinterval"></span><span id="STARTUPINTERVAL"></span>**Startupinterval** (4)</span><span class="sxs-lookup"><span data-stu-id="133ad-225"><span id="StartupInterval"></span><span id="startupinterval"></span><span id="STARTUPINTERVAL"></span>**StartupInterval** (4)</span></span>


</dt> <dd>

<span data-ttu-id="133ad-226">Gibt an, dass die Metrik für ein Zeitintervall gilt, das beim Start der gemessenen Ressource begonnen hat (d. h. das von metricdefforme zugeordnete managedelta).</span><span class="sxs-lookup"><span data-stu-id="133ad-226">Indicates that the metric applies to a time interval that began at the startup of the measured resource (i.e. the ManagedElement associated by MetricDefForMe).</span></span> <span data-ttu-id="133ad-227">In den entsprechenden basemetricvalue-Instanzen gibt Timestamp das Ende des Zeitintervalls an.</span><span class="sxs-lookup"><span data-stu-id="133ad-227">On the corresponding BaseMetricValue instances, TimeStamp specifies the end of the time interval.</span></span> <span data-ttu-id="133ad-228">Wenn Duration gleich 0 ist, gibt dies an, dass die Startzeit der gemessenen Ressource unbekannt ist.</span><span class="sxs-lookup"><span data-stu-id="133ad-228">If Duration is 0, this indicates that the startup time of the measured resource is unknown.</span></span> <span data-ttu-id="133ad-229">Andernfalls gibt Duration die Dauer zwischen dem Start der Ressource und dem Zeitstempel an.</span><span class="sxs-lookup"><span data-stu-id="133ad-229">Else, Duration specifies the duration between startup of the resource and TimeStamp.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="133ad-230"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (5.. 32767)</span><span class="sxs-lookup"><span data-stu-id="133ad-230"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (5..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="133ad-231"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Anbieter reserviert** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="133ad-231"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="133ad-232">**Einheiten**</span><span class="sxs-lookup"><span data-stu-id="133ad-232">**Units**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="133ad-233">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="133ad-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="133ad-234">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="133ad-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="133ad-235">Die Einheiten der Metrik.</span><span class="sxs-lookup"><span data-stu-id="133ad-235">The units of the metric.</span></span> <span data-ttu-id="133ad-236">Beispiele hierfür sind bytes, Pakete, Aufträge, Dateien, Millisekunden und Amps.</span><span class="sxs-lookup"><span data-stu-id="133ad-236">Examples are bytes, packets, jobs, files, milliseconds, and amps.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="133ad-237">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="133ad-237">Requirements</span></span>



| <span data-ttu-id="133ad-238">Anforderung</span><span class="sxs-lookup"><span data-stu-id="133ad-238">Requirement</span></span> | <span data-ttu-id="133ad-239">Wert</span><span class="sxs-lookup"><span data-stu-id="133ad-239">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="133ad-240">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="133ad-240">Minimum supported client</span></span><br/> | <span data-ttu-id="133ad-241">Windows 8</span><span class="sxs-lookup"><span data-stu-id="133ad-241">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="133ad-242">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="133ad-242">Minimum supported server</span></span><br/> | <span data-ttu-id="133ad-243">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="133ad-243">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="133ad-244">Namespace</span><span class="sxs-lookup"><span data-stu-id="133ad-244">Namespace</span></span><br/>                | <span data-ttu-id="133ad-245">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="133ad-245">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="133ad-246">MOF</span><span class="sxs-lookup"><span data-stu-id="133ad-246">MOF</span></span><br/>                      | <dl> <span data-ttu-id="133ad-247"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="133ad-247"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="133ad-248">DLL</span><span class="sxs-lookup"><span data-stu-id="133ad-248">DLL</span></span><br/>                      | <dl> <span data-ttu-id="133ad-249"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="133ad-249"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="133ad-250">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="133ad-250">See also</span></span>

<dl> <dt>

[<span data-ttu-id="133ad-251">**CIM- \_ managedelta**</span><span class="sxs-lookup"><span data-stu-id="133ad-251">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> </dl>

 

