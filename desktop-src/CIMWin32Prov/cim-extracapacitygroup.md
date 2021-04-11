---
description: Die CIM \_ extracapacitygroup-Klasse wird von einer Redundanz Gruppe abgeleitet, die angibt, dass die aggregierten Elemente mehr Kapazität oder mehr Kapazität aufweisen, als erforderlich sind.
ms.assetid: fbbbd6ed-4a67-4917-8b0e-3cba4cac3b45
ms.tgt_platform: multiple
title: CIM_ExtraCapacityGroup-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ExtraCapacityGroup
- CIM_ExtraCapacityGroup.Caption
- CIM_ExtraCapacityGroup.Description
- CIM_ExtraCapacityGroup.InstallDate
- CIM_ExtraCapacityGroup.Name
- CIM_ExtraCapacityGroup.Status
- CIM_ExtraCapacityGroup.CreationClassName
- CIM_ExtraCapacityGroup.RedundancyStatus
- CIM_ExtraCapacityGroup.MinNumberNeeded
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 78f9aa79cfcc7b93d176859069d1b71f5adf450e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214192"
---
# <a name="cim_extracapacitygroup-class"></a><span data-ttu-id="cd461-103">CIM \_ extracapacitygroup-Klasse</span><span class="sxs-lookup"><span data-stu-id="cd461-103">CIM\_ExtraCapacityGroup class</span></span>

<span data-ttu-id="cd461-104">Die **CIM \_ extracapacitygroup** -Klasse wird von einer Redundanz Gruppe abgeleitet, die angibt, dass die aggregierten Elemente mehr Kapazität oder mehr Kapazität aufweisen, als erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="cd461-104">The **CIM\_ExtraCapacityGroup** class is derived from a redundancy group that indicates the aggregated elements have more capacity or capability than is needed.</span></span> <span data-ttu-id="cd461-105">Ein Beispiel für diese Art von Redundanz ist die Installation von N + 1 Stromversorgungen oder Lüfter in einem System.</span><span class="sxs-lookup"><span data-stu-id="cd461-105">An example of this type of redundancy is the installation of N+1 power supplies or fans in a system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cd461-106">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="cd461-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="cd461-107">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="cd461-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="cd461-108">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="cd461-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="cd461-109">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="cd461-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd461-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="cd461-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{570ED2E8-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_ExtraCapacityGroup : CIM_RedundancyGroup
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CreationClassName;
  uint16   RedundancyStatus;
  uint32   MinNumberNeeded;
};
```

## <a name="members"></a><span data-ttu-id="cd461-111">Member</span><span class="sxs-lookup"><span data-stu-id="cd461-111">Members</span></span>

<span data-ttu-id="cd461-112">Die **CIM \_ extracapacitygroup** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="cd461-112">The **CIM\_ExtraCapacityGroup** class has these types of members:</span></span>

-   [<span data-ttu-id="cd461-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cd461-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cd461-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cd461-114">Properties</span></span>

<span data-ttu-id="cd461-115">Die **CIM \_ extracapacitygroup** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="cd461-115">The **CIM\_ExtraCapacityGroup** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cd461-116">**Caption**</span><span class="sxs-lookup"><span data-stu-id="cd461-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd461-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cd461-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd461-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cd461-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd461-119">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="cd461-119">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="cd461-120">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="cd461-120">A short textual description of the object.</span></span>

<span data-ttu-id="cd461-121">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="cd461-121">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd461-122">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="cd461-122">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd461-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cd461-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd461-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cd461-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd461-125">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="cd461-125">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="cd461-126">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cd461-126">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="cd461-127">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="cd461-127">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="cd461-128">Diese Eigenschaft wird von [**CIM \_ redundant cygroup**](cim-redundancygroup.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="cd461-128">This property is inherited from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd461-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cd461-129">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd461-130">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cd461-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd461-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cd461-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd461-132">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="cd461-132">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="cd461-133">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="cd461-133">A textual description of the object.</span></span>

<span data-ttu-id="cd461-134">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="cd461-134">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd461-135">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="cd461-135">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd461-136">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="cd461-136">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="cd461-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cd461-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd461-138">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="cd461-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="cd461-139">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="cd461-139">Indicates when the object was installed.</span></span> <span data-ttu-id="cd461-140">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="cd461-140">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="cd461-141">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="cd461-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd461-142">**Minnuma**</span><span class="sxs-lookup"><span data-stu-id="cd461-142">**MinNumberNeeded**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd461-143">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd461-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd461-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cd461-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd461-145">Die kleinste Anzahl von Elementen, die in Betrieb sein müssen, um Redundanz zu haben.</span><span class="sxs-lookup"><span data-stu-id="cd461-145">Smallest number of elements that must be operational to have redundancy.</span></span> <span data-ttu-id="cd461-146">In einer Redundanz Beziehung mit n + 1 sollte diese Eigenschaft beispielsweise auf n festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="cd461-146">For example, in an N+1 redundancy relationship, this property should be set equal to N.</span></span>

</dd> <dt>

<span data-ttu-id="cd461-147">**Name**</span><span class="sxs-lookup"><span data-stu-id="cd461-147">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd461-148">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cd461-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd461-149">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cd461-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd461-150">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="cd461-150">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="cd461-151">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="cd461-151">Label by which the object is known.</span></span> <span data-ttu-id="cd461-152">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="cd461-152">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="cd461-153">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="cd461-153">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd461-154">**RedundancyStatus**</span><span class="sxs-lookup"><span data-stu-id="cd461-154">**RedundancyStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd461-155">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cd461-155">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cd461-156">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cd461-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd461-157">Informationen zum Status der Redundanz Gruppe.</span><span class="sxs-lookup"><span data-stu-id="cd461-157">Information about the state of the redundancy group.</span></span>

<span data-ttu-id="cd461-158">Diese Eigenschaft wird von [**CIM \_ redundant cygroup**](cim-redundancygroup.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="cd461-158">This property is inherited from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cd461-159"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="cd461-159"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="cd461-160">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="cd461-160">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="cd461-161"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="cd461-161"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="cd461-162">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="cd461-162">Other.</span></span>

</dd> <dt>

<span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>

<span data-ttu-id="cd461-163"><span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>**Vollständig redundant** (2)</span><span class="sxs-lookup"><span data-stu-id="cd461-163"><span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>**Fully Redundant** (2)</span></span>


</dt> <dd>

<span data-ttu-id="cd461-164">Die gesamte konfigurierte Redundanz ist verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cd461-164">All of the configured redundancy is available.</span></span>

</dd> <dt>

<span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>

<span data-ttu-id="cd461-165"><span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>**Verschlechterung der Redundanz** (3)</span><span class="sxs-lookup"><span data-stu-id="cd461-165"><span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>**Degraded Redundancy** (3)</span></span>


</dt> <dd>

<span data-ttu-id="cd461-166">Aufgrund einiger Fehler ist weniger Redundanz verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cd461-166">Reduced amount of redundancy is available due to some failures.</span></span>

</dd> <dt>

<span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>

<span data-ttu-id="cd461-167"><span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>**Redundanz Verlust** (4)</span><span class="sxs-lookup"><span data-stu-id="cd461-167"><span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>**Redundancy Lost** (4)</span></span>


</dt> <dd>

<span data-ttu-id="cd461-168">Redundanz ist aufgrund einer ausreichenden Anzahl von Fehlern nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cd461-168">Redundancy is unavailable due to a sufficient number of failures.</span></span> <span data-ttu-id="cd461-169">Der nächste Fehler führt zu einem Gesamtfehler.</span><span class="sxs-lookup"><span data-stu-id="cd461-169">The next failure will cause overall failure.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="cd461-170">**Status**</span><span class="sxs-lookup"><span data-stu-id="cd461-170">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd461-171">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cd461-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd461-172">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cd461-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd461-173">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="cd461-173">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="cd461-174">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="cd461-174">String that indicates the current status of the object.</span></span> <span data-ttu-id="cd461-175">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="cd461-175">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="cd461-176">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="cd461-176">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="cd461-177">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="cd461-177">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="cd461-178">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="cd461-178">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="cd461-179">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="cd461-179">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="cd461-180">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="cd461-180">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="cd461-181">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="cd461-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="cd461-182">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="cd461-182">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="cd461-183">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="cd461-183">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="cd461-184">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="cd461-184">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="cd461-185">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="cd461-185">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cd461-186">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="cd461-186">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="cd461-187">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="cd461-187">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="cd461-188">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="cd461-188">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="cd461-189">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="cd461-189">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="cd461-190">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="cd461-190">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="cd461-191">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="cd461-191">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="cd461-192">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="cd461-192">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="cd461-193">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="cd461-193">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="cd461-194">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="cd461-194">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="cd461-195"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="cd461-195"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="cd461-196">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cd461-196">Remarks</span></span>

<span data-ttu-id="cd461-197">Die **CIM \_ extracapacitygroup** -Klasse wird von [**CIM \_ redundant cygroup**](cim-redundancygroup.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="cd461-197">The **CIM\_ExtraCapacityGroup** class is derived from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

<span data-ttu-id="cd461-198">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="cd461-198">WMI does not implement this class.</span></span>

<span data-ttu-id="cd461-199">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="cd461-199">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="cd461-200">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="cd461-200">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd461-201">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cd461-201">Requirements</span></span>



| <span data-ttu-id="cd461-202">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cd461-202">Requirement</span></span> | <span data-ttu-id="cd461-203">Wert</span><span class="sxs-lookup"><span data-stu-id="cd461-203">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd461-204">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cd461-204">Minimum supported client</span></span><br/> | <span data-ttu-id="cd461-205">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cd461-205">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cd461-206">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cd461-206">Minimum supported server</span></span><br/> | <span data-ttu-id="cd461-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cd461-207">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cd461-208">Namespace</span><span class="sxs-lookup"><span data-stu-id="cd461-208">Namespace</span></span><br/>                | <span data-ttu-id="cd461-209">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="cd461-209">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cd461-210">MOF</span><span class="sxs-lookup"><span data-stu-id="cd461-210">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cd461-211"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="cd461-211"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cd461-212">DLL</span><span class="sxs-lookup"><span data-stu-id="cd461-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd461-213"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd461-213"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd461-214">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cd461-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd461-215">**CIM- \_ RedundancyGroup**</span><span class="sxs-lookup"><span data-stu-id="cd461-215">**CIM\_RedundancyGroup**</span></span>](cim-redundancygroup.md)
</dt> </dl>

 

