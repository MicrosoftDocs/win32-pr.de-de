---
description: Die CIM \_ RedundancyGroup-Klasse stellt eine Auflistung verwalteter Systemelemente dar, die angibt, dass die aggregierten Komponenten zusammen Redundanz bereitstellen.
ms.assetid: b47899cc-eafc-431f-96d4-edb01bf4bcd1
ms.tgt_platform: multiple
title: CIM_RedundancyGroup-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RedundancyGroup
- CIM_RedundancyGroup.Caption
- CIM_RedundancyGroup.Description
- CIM_RedundancyGroup.InstallDate
- CIM_RedundancyGroup.Name
- CIM_RedundancyGroup.Status
- CIM_RedundancyGroup.CreationClassName
- CIM_RedundancyGroup.RedundancyStatus
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1394e052b4741dee5b2646c903d83477bfa1ccf3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860644"
---
# <a name="cim_redundancygroup-class"></a><span data-ttu-id="142b1-103">CIM \_ redundant cygroup-Klasse</span><span class="sxs-lookup"><span data-stu-id="142b1-103">CIM\_RedundancyGroup class</span></span>

<span data-ttu-id="142b1-104">Die **CIM \_ RedundancyGroup** -Klasse stellt eine Auflistung verwalteter Systemelemente dar, die angibt, dass die aggregierten Komponenten zusammen Redundanz bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="142b1-104">The **CIM\_RedundancyGroup** class represents a collection of managed system elements, which indicates that the aggregated components, together, provide redundancy.</span></span> <span data-ttu-id="142b1-105">Alle Elemente, die in einer Redundanz Gruppe aggregiert werden, sollten Instanziierungen der gleichen Objektklasse sein.</span><span class="sxs-lookup"><span data-stu-id="142b1-105">All elements aggregated in a redundancy group should be instantiations of the same object class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="142b1-106">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="142b1-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="142b1-107">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="142b1-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="142b1-108">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="142b1-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="142b1-109">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="142b1-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="142b1-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="142b1-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{4C3A040A-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_RedundancyGroup : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CreationClassName;
  uint16   RedundancyStatus;
};
```

## <a name="members"></a><span data-ttu-id="142b1-111">Member</span><span class="sxs-lookup"><span data-stu-id="142b1-111">Members</span></span>

<span data-ttu-id="142b1-112">Die **CIM \_ RedundancyGroup** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="142b1-112">The **CIM\_RedundancyGroup** class has these types of members:</span></span>

-   [<span data-ttu-id="142b1-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="142b1-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="142b1-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="142b1-114">Properties</span></span>

<span data-ttu-id="142b1-115">Die **CIM \_ RedundancyGroup** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="142b1-115">The **CIM\_RedundancyGroup** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="142b1-116">**Caption**</span><span class="sxs-lookup"><span data-stu-id="142b1-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="142b1-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="142b1-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="142b1-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="142b1-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="142b1-119">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="142b1-119">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="142b1-120">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="142b1-120">A short textual description of the object.</span></span>

<span data-ttu-id="142b1-121">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="142b1-121">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="142b1-122">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="142b1-122">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="142b1-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="142b1-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="142b1-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="142b1-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="142b1-125">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="142b1-125">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="142b1-126">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="142b1-126">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="142b1-127">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="142b1-127">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="142b1-128">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="142b1-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="142b1-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="142b1-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="142b1-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="142b1-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="142b1-131">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="142b1-131">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="142b1-132">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="142b1-132">A textual description of the object.</span></span>

<span data-ttu-id="142b1-133">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="142b1-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="142b1-134">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="142b1-134">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="142b1-135">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="142b1-135">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="142b1-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="142b1-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="142b1-137">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="142b1-137">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="142b1-138">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="142b1-138">Indicates when the object was installed.</span></span> <span data-ttu-id="142b1-139">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="142b1-139">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="142b1-140">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="142b1-140">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="142b1-141">**Name**</span><span class="sxs-lookup"><span data-stu-id="142b1-141">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="142b1-142">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="142b1-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="142b1-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="142b1-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="142b1-144">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="142b1-144">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="142b1-145">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="142b1-145">Label by which the object is known.</span></span> <span data-ttu-id="142b1-146">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="142b1-146">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="142b1-147">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="142b1-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="142b1-148">**RedundancyStatus**</span><span class="sxs-lookup"><span data-stu-id="142b1-148">**RedundancyStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="142b1-149">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="142b1-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="142b1-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="142b1-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="142b1-151">Informationen zum Status der Redundanz Gruppe.</span><span class="sxs-lookup"><span data-stu-id="142b1-151">Information about the state of the redundancy group.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="142b1-152"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="142b1-152"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="142b1-153">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="142b1-153">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="142b1-154"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="142b1-154"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="142b1-155">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="142b1-155">Other.</span></span>

</dd> <dt>

<span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>

<span data-ttu-id="142b1-156"><span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>**Vollständig redundant** (2)</span><span class="sxs-lookup"><span data-stu-id="142b1-156"><span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>**Fully Redundant** (2)</span></span>


</dt> <dd>

<span data-ttu-id="142b1-157">Die gesamte konfigurierte Redundanz ist verfügbar.</span><span class="sxs-lookup"><span data-stu-id="142b1-157">All of the configured redundancy is available.</span></span>

</dd> <dt>

<span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>

<span data-ttu-id="142b1-158"><span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>**Verschlechterung der Redundanz** (3)</span><span class="sxs-lookup"><span data-stu-id="142b1-158"><span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>**Degraded Redundancy** (3)</span></span>


</dt> <dd>

<span data-ttu-id="142b1-159">Aufgrund einiger Fehler ist weniger Redundanz verfügbar.</span><span class="sxs-lookup"><span data-stu-id="142b1-159">Reduced amount of redundancy is available due to some failures.</span></span>

</dd> <dt>

<span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>

<span data-ttu-id="142b1-160"><span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>**Redundanz Verlust** (4)</span><span class="sxs-lookup"><span data-stu-id="142b1-160"><span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>**Redundancy Lost** (4)</span></span>


</dt> <dd>

<span data-ttu-id="142b1-161">Redundanz ist aufgrund einer ausreichenden Anzahl von Fehlern nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="142b1-161">Redundancy is unavailable due to a sufficient number of failures.</span></span> <span data-ttu-id="142b1-162">Der nächste Fehler führt zu einem Gesamtfehler.</span><span class="sxs-lookup"><span data-stu-id="142b1-162">The next failure will cause overall failure.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="142b1-163">**Status**</span><span class="sxs-lookup"><span data-stu-id="142b1-163">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="142b1-164">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="142b1-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="142b1-165">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="142b1-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="142b1-166">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="142b1-166">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="142b1-167">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="142b1-167">String that indicates the current status of the object.</span></span> <span data-ttu-id="142b1-168">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="142b1-168">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="142b1-169">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="142b1-169">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="142b1-170">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="142b1-170">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="142b1-171">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="142b1-171">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="142b1-172">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="142b1-172">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="142b1-173">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="142b1-173">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="142b1-174">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="142b1-174">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="142b1-175">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="142b1-175">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="142b1-176">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="142b1-176">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="142b1-177">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="142b1-177">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="142b1-178">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="142b1-178">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="142b1-179">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="142b1-179">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="142b1-180">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="142b1-180">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="142b1-181">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="142b1-181">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="142b1-182">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="142b1-182">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="142b1-183">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="142b1-183">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="142b1-184">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="142b1-184">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="142b1-185">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="142b1-185">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="142b1-186">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="142b1-186">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="142b1-187">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="142b1-187">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="142b1-188"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="142b1-188"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="142b1-189">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="142b1-189">Remarks</span></span>

<span data-ttu-id="142b1-190">Die **CIM \_ RedundancyGroup** -Klasse wird von [**CIM \_ LogicalElement**](cim-logicalelement.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="142b1-190">The **CIM\_RedundancyGroup** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="142b1-191">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="142b1-191">WMI does not implement this class.</span></span>

<span data-ttu-id="142b1-192">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="142b1-192">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="142b1-193">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="142b1-193">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="142b1-194">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="142b1-194">Requirements</span></span>



| <span data-ttu-id="142b1-195">Anforderung</span><span class="sxs-lookup"><span data-stu-id="142b1-195">Requirement</span></span> | <span data-ttu-id="142b1-196">Wert</span><span class="sxs-lookup"><span data-stu-id="142b1-196">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="142b1-197">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="142b1-197">Minimum supported client</span></span><br/> | <span data-ttu-id="142b1-198">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="142b1-198">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="142b1-199">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="142b1-199">Minimum supported server</span></span><br/> | <span data-ttu-id="142b1-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="142b1-200">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="142b1-201">Namespace</span><span class="sxs-lookup"><span data-stu-id="142b1-201">Namespace</span></span><br/>                | <span data-ttu-id="142b1-202">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="142b1-202">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="142b1-203">MOF</span><span class="sxs-lookup"><span data-stu-id="142b1-203">MOF</span></span><br/>                      | <dl> <span data-ttu-id="142b1-204"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="142b1-204"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="142b1-205">DLL</span><span class="sxs-lookup"><span data-stu-id="142b1-205">DLL</span></span><br/>                      | <dl> <span data-ttu-id="142b1-206"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="142b1-206"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="142b1-207">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="142b1-207">See also</span></span>

<dl> <dt>

[<span data-ttu-id="142b1-208">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="142b1-208">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

