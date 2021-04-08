---
description: Die CIM \_ SpareGroup-Klasse wird von der CIM \_ redundant cygroup-Klasse abgeleitet und gibt an, dass mindestens eines der aggregierten Elemente geschont werden kann.
ms.assetid: e60f8cab-a9e8-4f5a-b8d7-833c7832ef7e
ms.tgt_platform: multiple
title: CIM_SpareGroup-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SpareGroup
- CIM_SpareGroup.Caption
- CIM_SpareGroup.Description
- CIM_SpareGroup.InstallDate
- CIM_SpareGroup.Name
- CIM_SpareGroup.Status
- CIM_SpareGroup.CreationClassName
- CIM_SpareGroup.RedundancyStatus
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 17907c62ace9f75c8d807e56d35b91f4c28e5f42
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747832"
---
# <a name="cim_sparegroup-class"></a><span data-ttu-id="4f9e4-103">CIM \_ SpareGroup-Klasse</span><span class="sxs-lookup"><span data-stu-id="4f9e4-103">CIM\_SpareGroup class</span></span>

<span data-ttu-id="4f9e4-104">Die **CIM \_ SpareGroup** -Klasse wird von der [**CIM \_ redundant cygroup**](cim-redundancygroup.md) -Klasse abgeleitet und gibt an, dass mindestens eines der aggregierten Elemente geschont werden kann.</span><span class="sxs-lookup"><span data-stu-id="4f9e4-104">The **CIM\_SpareGroup** class is derived from the [**CIM\_RedundancyGroup**](cim-redundancygroup.md) class and indicates that one or more of the aggregated elements can be spared.</span></span> <span data-ttu-id="4f9e4-105">Spares werden mithilfe der [**CIM- \_ aczasspare-Zuordnung**](cim-actsasspare.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="4f9e4-105">Spares are defined using the [**CIM\_ActsAsSpare**](cim-actsasspare.md) association.</span></span> <span data-ttu-id="4f9e4-106">Ein Beispiel für einen Ersatz ist die Verwendung redundanter NICs in einem Computersystem, bei dem eine NIC Primär und die andere als Ersatz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4f9e4-106">An example of a spare is the use of redundant NICs in a computer system, where one NIC is primary and the other is spare.</span></span> <span data-ttu-id="4f9e4-107">Die primäre NIC ist ein Mitglied der Gruppe "Spare", die mit der CIM-Klasse " [**\_ redundant cycomponent**](cim-redundancycomponent.md) " verknüpft ist, und die andere NIC wird mithilfe der **CIM- \_ aczasspare** -Beziehung zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="4f9e4-107">The primary NIC would be a member of the spare group, associated using the [**CIM\_RedundancyComponent**](cim-redundancycomponent.md) class, and the other NIC would be associated using the **CIM\_ActsAsSpare** relationship.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4f9e4-108">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="4f9e4-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4f9e4-109">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4f9e4-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4f9e4-110">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4f9e4-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="4f9e4-111">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="4f9e4-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f9e4-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f9e4-112">Syntax</span></span>

``` syntax
[Abstract, UUID("{64B86CA6-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_SpareGroup : CIM_RedundancyGroup
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

## <a name="members"></a><span data-ttu-id="4f9e4-113">Member</span><span class="sxs-lookup"><span data-stu-id="4f9e4-113">Members</span></span>

<span data-ttu-id="4f9e4-114">Die **CIM \_ SpareGroup** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="4f9e4-114">The **CIM\_SpareGroup** class has these types of members:</span></span>

-   [<span data-ttu-id="4f9e4-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4f9e4-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4f9e4-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4f9e4-116">Properties</span></span>

<span data-ttu-id="4f9e4-117">Die **CIM \_ SpareGroup** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4f9e4-117">The **CIM\_SpareGroup** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4f9e4-118">**Caption**</span><span class="sxs-lookup"><span data-stu-id="4f9e4-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f9e4-119">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4f9e4-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f9e4-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4f9e4-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f9e4-121">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="4f9e4-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="4f9e4-122">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="4f9e4-122">A short textual description of the object.</span></span>

<span data-ttu-id="4f9e4-123">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4f9e4-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f9e4-124">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="4f9e4-124">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f9e4-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4f9e4-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f9e4-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4f9e4-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f9e4-127">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="4f9e4-127">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="4f9e4-128">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4f9e4-128">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="4f9e4-129">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="4f9e4-129">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="4f9e4-130">Diese Eigenschaft wird von [**CIM \_ redundant cygroup**](cim-redundancygroup.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4f9e4-130">This property is inherited from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f9e4-131">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4f9e4-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f9e4-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4f9e4-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f9e4-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4f9e4-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f9e4-134">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="4f9e4-134">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="4f9e4-135">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="4f9e4-135">A textual description of the object.</span></span>

<span data-ttu-id="4f9e4-136">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4f9e4-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f9e4-137">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="4f9e4-137">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f9e4-138">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="4f9e4-138">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4f9e4-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4f9e4-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f9e4-140">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="4f9e4-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="4f9e4-141">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="4f9e4-141">Indicates when the object was installed.</span></span> <span data-ttu-id="4f9e4-142">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="4f9e4-142">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="4f9e4-143">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4f9e4-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f9e4-144">**Name**</span><span class="sxs-lookup"><span data-stu-id="4f9e4-144">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f9e4-145">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4f9e4-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f9e4-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4f9e4-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f9e4-147">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="4f9e4-147">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="4f9e4-148">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="4f9e4-148">Label by which the object is known.</span></span> <span data-ttu-id="4f9e4-149">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="4f9e4-149">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="4f9e4-150">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4f9e4-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f9e4-151">**RedundancyStatus**</span><span class="sxs-lookup"><span data-stu-id="4f9e4-151">**RedundancyStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f9e4-152">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4f9e4-152">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4f9e4-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4f9e4-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4f9e4-154">Informationen zum Status der Redundanz Gruppe.</span><span class="sxs-lookup"><span data-stu-id="4f9e4-154">Information about the state of the redundancy group.</span></span>

<span data-ttu-id="4f9e4-155">Diese Eigenschaft wird von [**CIM \_ redundant cygroup**](cim-redundancygroup.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4f9e4-155">This property is inherited from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4f9e4-156"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="4f9e4-156"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="4f9e4-157">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="4f9e4-157">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4f9e4-158"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="4f9e4-158"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="4f9e4-159">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="4f9e4-159">Other.</span></span>

</dd> <dt>

<span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>

<span data-ttu-id="4f9e4-160"><span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>**Vollständig redundant** (2)</span><span class="sxs-lookup"><span data-stu-id="4f9e4-160"><span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>**Fully Redundant** (2)</span></span>


</dt> <dd>

<span data-ttu-id="4f9e4-161">Die gesamte konfigurierte Redundanz ist verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4f9e4-161">All of the configured redundancy is available.</span></span>

</dd> <dt>

<span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>

<span data-ttu-id="4f9e4-162"><span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>**Verschlechterung der Redundanz** (3)</span><span class="sxs-lookup"><span data-stu-id="4f9e4-162"><span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>**Degraded Redundancy** (3)</span></span>


</dt> <dd>

<span data-ttu-id="4f9e4-163">Aufgrund einiger Fehler ist weniger Redundanz verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4f9e4-163">Reduced amount of redundancy is available due to some failures.</span></span>

</dd> <dt>

<span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>

<span data-ttu-id="4f9e4-164"><span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>**Redundanz Verlust** (4)</span><span class="sxs-lookup"><span data-stu-id="4f9e4-164"><span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>**Redundancy Lost** (4)</span></span>


</dt> <dd>

<span data-ttu-id="4f9e4-165">Redundanz ist aufgrund einer ausreichenden Anzahl von Fehlern nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4f9e4-165">Redundancy is unavailable due to a sufficient number of failures.</span></span> <span data-ttu-id="4f9e4-166">Der nächste Fehler führt zu einem Gesamtfehler.</span><span class="sxs-lookup"><span data-stu-id="4f9e4-166">The next failure will cause overall failure.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4f9e4-167">**Status**</span><span class="sxs-lookup"><span data-stu-id="4f9e4-167">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f9e4-168">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4f9e4-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4f9e4-169">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4f9e4-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f9e4-170">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="4f9e4-170">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="4f9e4-171">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="4f9e4-171">String that indicates the current status of the object.</span></span> <span data-ttu-id="4f9e4-172">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="4f9e4-172">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="4f9e4-173">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="4f9e4-173">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="4f9e4-174">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="4f9e4-174">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="4f9e4-175">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="4f9e4-175">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="4f9e4-176">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="4f9e4-176">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="4f9e4-177">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="4f9e4-177">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="4f9e4-178">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4f9e4-178">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="4f9e4-179">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="4f9e4-179">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="4f9e4-180">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="4f9e4-180">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="4f9e4-181">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="4f9e4-181">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="4f9e4-182">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="4f9e4-182">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4f9e4-183">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="4f9e4-183">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="4f9e4-184">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="4f9e4-184">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="4f9e4-185">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="4f9e4-185">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="4f9e4-186">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="4f9e4-186">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="4f9e4-187">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="4f9e4-187">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="4f9e4-188">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="4f9e4-188">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="4f9e4-189">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="4f9e4-189">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="4f9e4-190">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="4f9e4-190">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="4f9e4-191">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="4f9e4-191">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="4f9e4-192"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="4f9e4-192"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="4f9e4-193">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4f9e4-193">Remarks</span></span>

<span data-ttu-id="4f9e4-194">Die **CIM \_ SpareGroup** -Klasse wird von [**CIM \_ redundant cygroup**](cim-redundancygroup.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="4f9e4-194">The **CIM\_SpareGroup** class is derived from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

<span data-ttu-id="4f9e4-195">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="4f9e4-195">WMI does not implement this class.</span></span>

<span data-ttu-id="4f9e4-196">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="4f9e4-196">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4f9e4-197">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="4f9e4-197">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f9e4-198">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4f9e4-198">Requirements</span></span>



| <span data-ttu-id="4f9e4-199">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4f9e4-199">Requirement</span></span> | <span data-ttu-id="4f9e4-200">Wert</span><span class="sxs-lookup"><span data-stu-id="4f9e4-200">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f9e4-201">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4f9e4-201">Minimum supported client</span></span><br/> | <span data-ttu-id="4f9e4-202">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4f9e4-202">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4f9e4-203">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4f9e4-203">Minimum supported server</span></span><br/> | <span data-ttu-id="4f9e4-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4f9e4-204">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4f9e4-205">Namespace</span><span class="sxs-lookup"><span data-stu-id="4f9e4-205">Namespace</span></span><br/>                | <span data-ttu-id="4f9e4-206">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4f9e4-206">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4f9e4-207">MOF</span><span class="sxs-lookup"><span data-stu-id="4f9e4-207">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4f9e4-208"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="4f9e4-208"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4f9e4-209">DLL</span><span class="sxs-lookup"><span data-stu-id="4f9e4-209">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f9e4-210"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f9e4-210"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f9e4-211">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f9e4-211">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f9e4-212">**CIM- \_ RedundancyGroup**</span><span class="sxs-lookup"><span data-stu-id="4f9e4-212">**CIM\_RedundancyGroup**</span></span>](cim-redundancygroup.md)
</dt> </dl>

 

