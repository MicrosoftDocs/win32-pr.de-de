---
description: Die CIM \_ storageredundancygroup-Klasse stellt Massenspeicher bezogene Redundanz Informationen dar.
ms.assetid: 6bc81680-672a-4872-8951-11d7f10acbc7
ms.tgt_platform: multiple
title: CIM_StorageRedundancyGroup-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StorageRedundancyGroup
- CIM_StorageRedundancyGroup.Caption
- CIM_StorageRedundancyGroup.Description
- CIM_StorageRedundancyGroup.InstallDate
- CIM_StorageRedundancyGroup.Name
- CIM_StorageRedundancyGroup.Status
- CIM_StorageRedundancyGroup.CreationClassName
- CIM_StorageRedundancyGroup.RedundancyStatus
- CIM_StorageRedundancyGroup.TypeOfAlgorithm
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bef8cb8029c62957446ee5d7aefcf67fe5d7acb8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106340102"
---
# <a name="cim_storageredundancygroup-class"></a><span data-ttu-id="6de20-103">CIM- \_ Klasse von storageredundancygroup</span><span class="sxs-lookup"><span data-stu-id="6de20-103">CIM\_StorageRedundancyGroup class</span></span>

<span data-ttu-id="6de20-104">Die **CIM \_ storageredundancygroup** -Klasse stellt Massenspeicher bezogene Redundanz Informationen dar.</span><span class="sxs-lookup"><span data-stu-id="6de20-104">The **CIM\_StorageRedundancyGroup** class represents mass storage-related redundancy information.</span></span> <span data-ttu-id="6de20-105">Speicher Redundanz Gruppen werden verwendet, um Benutzerdaten zu schützen.</span><span class="sxs-lookup"><span data-stu-id="6de20-105">Storage redundancy groups are used to protect user data.</span></span> <span data-ttu-id="6de20-106">Sie bestehen aus mindestens einem physischen Blöcke oder einem oder mehreren aggregierten physischen Blöcken.</span><span class="sxs-lookup"><span data-stu-id="6de20-106">They are made up of one or more physical extents, or one or more aggregate physical extents.</span></span> <span data-ttu-id="6de20-107">Speicher Redundanz Gruppen können sich überlappen. die zugrunde liegenden Blöcke innerhalb der Überschneidung sollten jedoch keine Prüf Daten enthalten.</span><span class="sxs-lookup"><span data-stu-id="6de20-107">Storage redundancy groups may overlap; however, the underlying extents within the overlap should not contain any check data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6de20-108">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="6de20-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6de20-109">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6de20-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6de20-110">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6de20-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="6de20-111">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="6de20-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6de20-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="6de20-112">Syntax</span></span>

``` syntax
[Abstract, UUID("{6D477DBC-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_StorageRedundancyGroup : CIM_RedundancyGroup
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CreationClassName;
  uint16   RedundancyStatus;
  uint16   TypeOfAlgorithm;
};
```

## <a name="members"></a><span data-ttu-id="6de20-113">Member</span><span class="sxs-lookup"><span data-stu-id="6de20-113">Members</span></span>

<span data-ttu-id="6de20-114">Die **CIM-Klasse \_ storageredundancygroup** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6de20-114">The **CIM\_StorageRedundancyGroup** class has these types of members:</span></span>

-   [<span data-ttu-id="6de20-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6de20-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6de20-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6de20-116">Properties</span></span>

<span data-ttu-id="6de20-117">Die **CIM-Klasse \_ storageredundancygroup** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6de20-117">The **CIM\_StorageRedundancyGroup** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6de20-118">**Caption**</span><span class="sxs-lookup"><span data-stu-id="6de20-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6de20-119">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6de20-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6de20-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6de20-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6de20-121">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="6de20-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="6de20-122">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="6de20-122">A short textual description of the object.</span></span>

<span data-ttu-id="6de20-123">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6de20-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6de20-124">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="6de20-124">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6de20-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6de20-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6de20-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6de20-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6de20-127">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="6de20-127">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="6de20-128">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6de20-128">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="6de20-129">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="6de20-129">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="6de20-130">Diese Eigenschaft wird von [**CIM \_ redundant cygroup**](cim-redundancygroup.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6de20-130">This property is inherited from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

</dd> <dt>

<span data-ttu-id="6de20-131">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6de20-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6de20-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6de20-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6de20-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6de20-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6de20-134">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="6de20-134">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="6de20-135">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="6de20-135">A textual description of the object.</span></span>

<span data-ttu-id="6de20-136">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6de20-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6de20-137">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="6de20-137">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6de20-138">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="6de20-138">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6de20-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6de20-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6de20-140">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="6de20-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="6de20-141">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="6de20-141">Indicates when the object was installed.</span></span> <span data-ttu-id="6de20-142">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="6de20-142">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="6de20-143">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6de20-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6de20-144">**Name**</span><span class="sxs-lookup"><span data-stu-id="6de20-144">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6de20-145">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6de20-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6de20-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6de20-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6de20-147">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="6de20-147">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="6de20-148">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="6de20-148">Label by which the object is known.</span></span> <span data-ttu-id="6de20-149">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="6de20-149">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="6de20-150">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6de20-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6de20-151">**RedundancyStatus**</span><span class="sxs-lookup"><span data-stu-id="6de20-151">**RedundancyStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6de20-152">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6de20-152">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6de20-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6de20-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6de20-154">Informationen zum Status der Redundanz Gruppe.</span><span class="sxs-lookup"><span data-stu-id="6de20-154">Information about the state of the redundancy group.</span></span>

<span data-ttu-id="6de20-155">Diese Eigenschaft wird von [**CIM \_ redundant cygroup**](cim-redundancygroup.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6de20-155">This property is inherited from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6de20-156"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="6de20-156"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="6de20-157">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="6de20-157">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6de20-158"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="6de20-158"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="6de20-159">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="6de20-159">Other.</span></span>

</dd> <dt>

<span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>

<span data-ttu-id="6de20-160"><span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>**Vollständig redundant** (2)</span><span class="sxs-lookup"><span data-stu-id="6de20-160"><span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>**Fully Redundant** (2)</span></span>


</dt> <dd>

<span data-ttu-id="6de20-161">Die gesamte konfigurierte Redundanz ist verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6de20-161">All of the configured redundancy is available.</span></span>

</dd> <dt>

<span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>

<span data-ttu-id="6de20-162"><span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>**Verschlechterung der Redundanz** (3)</span><span class="sxs-lookup"><span data-stu-id="6de20-162"><span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>**Degraded Redundancy** (3)</span></span>


</dt> <dd>

<span data-ttu-id="6de20-163">Aufgrund einiger Fehler ist weniger Redundanz verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6de20-163">Reduced amount of redundancy is available due to some failures.</span></span>

</dd> <dt>

<span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>

<span data-ttu-id="6de20-164"><span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>**Redundanz Verlust** (4)</span><span class="sxs-lookup"><span data-stu-id="6de20-164"><span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>**Redundancy Lost** (4)</span></span>


</dt> <dd>

<span data-ttu-id="6de20-165">Redundanz ist aufgrund einer ausreichenden Anzahl von Fehlern nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6de20-165">Redundancy is unavailable due to a sufficient number of failures.</span></span> <span data-ttu-id="6de20-166">Der nächste Fehler führt zu einem Gesamtfehler.</span><span class="sxs-lookup"><span data-stu-id="6de20-166">The next failure will cause overall failure.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6de20-167">**Status**</span><span class="sxs-lookup"><span data-stu-id="6de20-167">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6de20-168">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6de20-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6de20-169">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6de20-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6de20-170">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="6de20-170">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="6de20-171">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="6de20-171">String that indicates the current status of the object.</span></span> <span data-ttu-id="6de20-172">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="6de20-172">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="6de20-173">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="6de20-173">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="6de20-174">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="6de20-174">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="6de20-175">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="6de20-175">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="6de20-176">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="6de20-176">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="6de20-177">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="6de20-177">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="6de20-178">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6de20-178">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="6de20-179">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="6de20-179">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="6de20-180">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="6de20-180">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="6de20-181">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="6de20-181">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="6de20-182">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="6de20-182">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6de20-183">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="6de20-183">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="6de20-184">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="6de20-184">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="6de20-185">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="6de20-185">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="6de20-186">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="6de20-186">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="6de20-187">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="6de20-187">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="6de20-188">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="6de20-188">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="6de20-189">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="6de20-189">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="6de20-190">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="6de20-190">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="6de20-191">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="6de20-191">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6de20-192">**TypeOfAlgorithm**</span><span class="sxs-lookup"><span data-stu-id="6de20-192">**TypeOfAlgorithm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6de20-193">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6de20-193">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6de20-194">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6de20-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6de20-195">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Redundanz Gruppe \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="6de20-195">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Redundancy Group\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="6de20-196">Der Algorithmus für die Datenredundanz und die Wiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="6de20-196">Algorithm used for data redundancy and reconstruction.</span></span> <span data-ttu-id="6de20-197">Der Wert 0 ist im CIM-Schema ungültig, da er angibt, dass keine Redundanz in DMI vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="6de20-197">The value 0 is not valid in the CIM schema since it represents that no redundancy exists in DMI.</span></span> <span data-ttu-id="6de20-198">In diesem Fall sollte das Objekt nicht instanziiert werden.</span><span class="sxs-lookup"><span data-stu-id="6de20-198">In which case, the object should not be instantiated.</span></span>

<dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="6de20-199">**Nicht definiert** (0)</span><span class="sxs-lookup"><span data-stu-id="6de20-199">**Undefined** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6de20-200">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="6de20-200">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6de20-201">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="6de20-201">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Copy"></span><span id="copy"></span><span id="COPY"></span>

<span data-ttu-id="6de20-202">**Kopieren** (3)</span><span class="sxs-lookup"><span data-stu-id="6de20-202">**Copy** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="XOR"></span><span id="xor"></span>

<span data-ttu-id="6de20-203">**Xor** (4)</span><span class="sxs-lookup"><span data-stu-id="6de20-203">**XOR** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="P_Q"></span><span id="p_q"></span>

<span data-ttu-id="6de20-204">**P + Q** (5)</span><span class="sxs-lookup"><span data-stu-id="6de20-204">**P+Q** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="S"></span><span id="s"></span>

<span data-ttu-id="6de20-205">**S** (6)</span><span class="sxs-lookup"><span data-stu-id="6de20-205">**S** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="P_S"></span><span id="p_s"></span>

<span data-ttu-id="6de20-206">**P + S** (7)</span><span class="sxs-lookup"><span data-stu-id="6de20-206">**P+S** (7)</span></span>


<span data-ttu-id="6de20-207"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="6de20-207"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="6de20-208">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6de20-208">Remarks</span></span>

<span data-ttu-id="6de20-209">Die **CIM-Klasse \_ storageredundancygroup** ist von [**CIM \_ redundant cygroup**](cim-redundancygroup.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="6de20-209">The **CIM\_StorageRedundancyGroup** class is derived from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

<span data-ttu-id="6de20-210">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="6de20-210">WMI does not implement this class.</span></span>

<span data-ttu-id="6de20-211">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="6de20-211">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6de20-212">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="6de20-212">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6de20-213">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6de20-213">Requirements</span></span>



| <span data-ttu-id="6de20-214">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6de20-214">Requirement</span></span> | <span data-ttu-id="6de20-215">Wert</span><span class="sxs-lookup"><span data-stu-id="6de20-215">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6de20-216">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6de20-216">Minimum supported client</span></span><br/> | <span data-ttu-id="6de20-217">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6de20-217">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6de20-218">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6de20-218">Minimum supported server</span></span><br/> | <span data-ttu-id="6de20-219">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6de20-219">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6de20-220">Namespace</span><span class="sxs-lookup"><span data-stu-id="6de20-220">Namespace</span></span><br/>                | <span data-ttu-id="6de20-221">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="6de20-221">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6de20-222">MOF</span><span class="sxs-lookup"><span data-stu-id="6de20-222">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6de20-223"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="6de20-223"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6de20-224">DLL</span><span class="sxs-lookup"><span data-stu-id="6de20-224">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6de20-225"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6de20-225"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6de20-226">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6de20-226">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6de20-227">**CIM- \_ RedundancyGroup**</span><span class="sxs-lookup"><span data-stu-id="6de20-227">**CIM\_RedundancyGroup**</span></span>](cim-redundancygroup.md)
</dt> </dl>

 

