---
description: Die CIM \_ jobdestination-Klasse stellt dar, wo ein Auftrag zur Verarbeitung übermittelt wird.
ms.assetid: ad2a037d-a5d3-4422-972d-8ef10699bb60
ms.tgt_platform: multiple
title: CIM_JobDestination-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_JobDestination
- CIM_JobDestination.Caption
- CIM_JobDestination.Description
- CIM_JobDestination.InstallDate
- CIM_JobDestination.Name
- CIM_JobDestination.Status
- CIM_JobDestination.CreationClassName
- CIM_JobDestination.SystemCreationClassName
- CIM_JobDestination.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d01fbe3b6025795084bf0af4cca3d644fd3cf4a4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861240"
---
# <a name="cim_jobdestination-class"></a><span data-ttu-id="8fc08-103">CIM \_ jobdestination-Klasse</span><span class="sxs-lookup"><span data-stu-id="8fc08-103">CIM\_JobDestination class</span></span>

<span data-ttu-id="8fc08-104">Die **CIM \_ jobdestination** -Klasse stellt dar, wo ein Auftrag zur Verarbeitung übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="8fc08-104">The **CIM\_JobDestination** class represents where a job is submitted for processing.</span></span> <span data-ttu-id="8fc08-105">Sie kann auf eine Warteschlange verweisen, die NULL oder mehr Aufträge enthält, z. b. eine Druck Warteschlange, die Druckaufträge enthält.</span><span class="sxs-lookup"><span data-stu-id="8fc08-105">It can refer to a queue that contains zero or more jobs, such as a print queue containing print jobs.</span></span> <span data-ttu-id="8fc08-106">Auftrags Ziele werden auf Systemen gehostet, ähnlich der Art, in der Dienste auf Systemen gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="8fc08-106">Job destinations are hosted on systems, similar to the way in which services are hosted on systems.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8fc08-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="8fc08-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8fc08-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8fc08-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8fc08-109">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="8fc08-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="8fc08-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="8fc08-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fc08-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="8fc08-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{673E0A2C-E3D0-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_JobDestination : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CreationClassName;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="8fc08-112">Member</span><span class="sxs-lookup"><span data-stu-id="8fc08-112">Members</span></span>

<span data-ttu-id="8fc08-113">Die **CIM \_ jobdestination** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="8fc08-113">The **CIM\_JobDestination** class has these types of members:</span></span>

-   [<span data-ttu-id="8fc08-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8fc08-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8fc08-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8fc08-115">Properties</span></span>

<span data-ttu-id="8fc08-116">Die **CIM \_ jobdestination** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8fc08-116">The **CIM\_JobDestination** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8fc08-117">**Caption**</span><span class="sxs-lookup"><span data-stu-id="8fc08-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fc08-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8fc08-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8fc08-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8fc08-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8fc08-120">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="8fc08-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="8fc08-121">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="8fc08-121">A short textual description of the object.</span></span>

<span data-ttu-id="8fc08-122">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8fc08-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8fc08-123">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="8fc08-123">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fc08-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8fc08-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8fc08-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8fc08-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8fc08-126">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="8fc08-126">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8fc08-127">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8fc08-127">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="8fc08-128">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="8fc08-128">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="8fc08-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8fc08-129">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fc08-130">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8fc08-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8fc08-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8fc08-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8fc08-132">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="8fc08-132">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="8fc08-133">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="8fc08-133">A textual description of the object.</span></span>

<span data-ttu-id="8fc08-134">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8fc08-134">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8fc08-135">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8fc08-135">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fc08-136">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="8fc08-136">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8fc08-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8fc08-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8fc08-138">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="8fc08-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="8fc08-139">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="8fc08-139">Indicates when the object was installed.</span></span> <span data-ttu-id="8fc08-140">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="8fc08-140">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="8fc08-141">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8fc08-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8fc08-142">**Name**</span><span class="sxs-lookup"><span data-stu-id="8fc08-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fc08-143">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8fc08-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8fc08-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8fc08-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8fc08-145">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="8fc08-145">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="8fc08-146">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="8fc08-146">Label by which the object is known.</span></span> <span data-ttu-id="8fc08-147">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="8fc08-147">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="8fc08-148">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8fc08-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8fc08-149">**Status**</span><span class="sxs-lookup"><span data-stu-id="8fc08-149">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fc08-150">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8fc08-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8fc08-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8fc08-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8fc08-152">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="8fc08-152">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="8fc08-153">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="8fc08-153">String that indicates the current status of the object.</span></span> <span data-ttu-id="8fc08-154">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="8fc08-154">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="8fc08-155">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="8fc08-155">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="8fc08-156">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="8fc08-156">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="8fc08-157">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="8fc08-157">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="8fc08-158">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="8fc08-158">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="8fc08-159">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="8fc08-159">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="8fc08-160">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8fc08-160">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="8fc08-161">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="8fc08-161">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="8fc08-162">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="8fc08-162">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="8fc08-163">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="8fc08-163">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="8fc08-164">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="8fc08-164">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8fc08-165">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="8fc08-165">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="8fc08-166">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="8fc08-166">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="8fc08-167">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="8fc08-167">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="8fc08-168">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="8fc08-168">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="8fc08-169">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="8fc08-169">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="8fc08-170">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="8fc08-170">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="8fc08-171">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="8fc08-171">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="8fc08-172">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="8fc08-172">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="8fc08-173">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="8fc08-173">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8fc08-174">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="8fc08-174">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fc08-175">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8fc08-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8fc08-176">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8fc08-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8fc08-177">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagierter**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**")</span><span class="sxs-lookup"><span data-stu-id="8fc08-177">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="8fc08-178">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="8fc08-178">Scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="8fc08-179">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="8fc08-179">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8fc08-180">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8fc08-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8fc08-181">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8fc08-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8fc08-182">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagierter**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM- \_ System**](cim-system.md).**Name**")</span><span class="sxs-lookup"><span data-stu-id="8fc08-182">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="8fc08-183">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="8fc08-183">Scoping system's name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8fc08-184">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8fc08-184">Remarks</span></span>

<span data-ttu-id="8fc08-185">Die **CIM \_ jobdestination** -Klasse wird von [**CIM \_ LogicalElement**](cim-logicalelement.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="8fc08-185">The **CIM\_JobDestination** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="8fc08-186">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="8fc08-186">WMI does not implement this class.</span></span>

<span data-ttu-id="8fc08-187">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="8fc08-187">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8fc08-188">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="8fc08-188">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fc08-189">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8fc08-189">Requirements</span></span>



| <span data-ttu-id="8fc08-190">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8fc08-190">Requirement</span></span> | <span data-ttu-id="8fc08-191">Wert</span><span class="sxs-lookup"><span data-stu-id="8fc08-191">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8fc08-192">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8fc08-192">Minimum supported client</span></span><br/> | <span data-ttu-id="8fc08-193">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8fc08-193">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8fc08-194">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8fc08-194">Minimum supported server</span></span><br/> | <span data-ttu-id="8fc08-195">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8fc08-195">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8fc08-196">Namespace</span><span class="sxs-lookup"><span data-stu-id="8fc08-196">Namespace</span></span><br/>                | <span data-ttu-id="8fc08-197">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8fc08-197">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8fc08-198">MOF</span><span class="sxs-lookup"><span data-stu-id="8fc08-198">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8fc08-199"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8fc08-199"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8fc08-200">DLL</span><span class="sxs-lookup"><span data-stu-id="8fc08-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8fc08-201"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8fc08-201"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fc08-202">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8fc08-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fc08-203">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="8fc08-203">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

