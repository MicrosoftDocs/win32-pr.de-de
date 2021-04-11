---
description: Die CIM- \_ Auftrags Klasse stellt eine Arbeitseinheit für ein System dar, z. b. einen Druckauftrag. Ein Auftrag unterscheidet sich von einem Prozess, weil ein Auftrag geplant werden kann.
ms.assetid: a689230e-2a62-4f0d-9961-9bbc055d3c6e
ms.tgt_platform: multiple
title: CIM_Job-Klasse (cimwin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Job
- CIM_Job.Caption
- CIM_Job.Description
- CIM_Job.InstallDate
- CIM_Job.Name
- CIM_Job.Status
- CIM_Job.ElapsedTime
- CIM_Job.JobStatus
- CIM_Job.Notify
- CIM_Job.Owner
- CIM_Job.Priority
- CIM_Job.StartTime
- CIM_Job.TimeSubmitted
- CIM_Job.UntilTime
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: cd527474309802a4c6d2315d8a9e61b6733e70d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126956"
---
# <a name="cim_job-class-cimwin32-wmi-providers"></a><span data-ttu-id="49c03-104">CIM_Job-Klasse (cimwin32-WMI-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="49c03-104">CIM_Job class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="49c03-105">Die **CIM- \_ Auftrags** Klasse stellt eine Arbeitseinheit für ein System dar, z. b. einen Druckauftrag.</span><span class="sxs-lookup"><span data-stu-id="49c03-105">The **CIM\_Job** class represents a unit of work for a system, such as a print job.</span></span> <span data-ttu-id="49c03-106">Ein Auftrag unterscheidet sich von einem Prozess, weil ein Auftrag geplant werden kann.</span><span class="sxs-lookup"><span data-stu-id="49c03-106">A job is distinct from a process because a job can be scheduled.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="49c03-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="49c03-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="49c03-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="49c03-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="49c03-109">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="49c03-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="49c03-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="49c03-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="49c03-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="49c03-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C564-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Job : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  datetime ElapsedTime;
  string   JobStatus;
  string   Notify;
  string   Owner;
  uint32   Priority;
  datetime StartTime;
  datetime TimeSubmitted;
  datetime UntilTime;
};
```

## <a name="members"></a><span data-ttu-id="49c03-112">Member</span><span class="sxs-lookup"><span data-stu-id="49c03-112">Members</span></span>

<span data-ttu-id="49c03-113">Die **CIM- \_ Auftrags** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="49c03-113">The **CIM\_Job** class has these types of members:</span></span>

-   [<span data-ttu-id="49c03-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="49c03-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="49c03-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="49c03-115">Properties</span></span>

<span data-ttu-id="49c03-116">Die **CIM- \_ Auftrags** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="49c03-116">The **CIM\_Job** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="49c03-117">**Caption**</span><span class="sxs-lookup"><span data-stu-id="49c03-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49c03-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="49c03-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49c03-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="49c03-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49c03-120">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="49c03-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="49c03-121">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="49c03-121">A short textual description of the object.</span></span>

<span data-ttu-id="49c03-122">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="49c03-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="49c03-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="49c03-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49c03-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="49c03-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49c03-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="49c03-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49c03-126">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="49c03-126">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="49c03-127">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="49c03-127">A textual description of the object.</span></span>

<span data-ttu-id="49c03-128">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="49c03-128">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="49c03-129">**Verweilzeit**</span><span class="sxs-lookup"><span data-stu-id="49c03-129">**ElapsedTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49c03-130">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="49c03-130">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="49c03-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="49c03-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49c03-132">Zeitspanne, für die der Auftrag ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="49c03-132">Length of time the job has been executing.</span></span>

</dd> <dt>

<span data-ttu-id="49c03-133">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="49c03-133">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49c03-134">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="49c03-134">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="49c03-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="49c03-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49c03-136">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="49c03-136">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="49c03-137">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="49c03-137">Indicates when the object was installed.</span></span> <span data-ttu-id="49c03-138">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="49c03-138">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="49c03-139">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="49c03-139">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="49c03-140">**Auftragsstatus**</span><span class="sxs-lookup"><span data-stu-id="49c03-140">**JobStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49c03-141">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="49c03-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49c03-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="49c03-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49c03-143">Eine frei Form Zeichenfolge, die den Auftragsstatus darstellt.</span><span class="sxs-lookup"><span data-stu-id="49c03-143">Free-form string that represents the job status.</span></span>

</dd> <dt>

<span data-ttu-id="49c03-144">**Name**</span><span class="sxs-lookup"><span data-stu-id="49c03-144">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49c03-145">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="49c03-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49c03-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="49c03-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49c03-147">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="49c03-147">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="49c03-148">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="49c03-148">Label by which the object is known.</span></span> <span data-ttu-id="49c03-149">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="49c03-149">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="49c03-150">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="49c03-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="49c03-151">**Benachrichtigen**</span><span class="sxs-lookup"><span data-stu-id="49c03-151">**Notify**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49c03-152">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="49c03-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49c03-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="49c03-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49c03-154">Der Benutzer wird nach Abschluss oder Fehler des Auftrags benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="49c03-154">User is notified upon job completion or failure.</span></span>

</dd> <dt>

<span data-ttu-id="49c03-155">**Besitzer**</span><span class="sxs-lookup"><span data-stu-id="49c03-155">**Owner**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49c03-156">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="49c03-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49c03-157">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="49c03-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49c03-158">Der Benutzer, der den Auftrag übermittelt hat.</span><span class="sxs-lookup"><span data-stu-id="49c03-158">User who submitted the job.</span></span>

</dd> <dt>

<span data-ttu-id="49c03-159">**Priority**</span><span class="sxs-lookup"><span data-stu-id="49c03-159">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49c03-160">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="49c03-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="49c03-161">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="49c03-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49c03-162">Wichtigkeit der Ausführung eines Auftrags.</span><span class="sxs-lookup"><span data-stu-id="49c03-162">Importance of a job's execution.</span></span>

</dd> <dt>

<span data-ttu-id="49c03-163">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="49c03-163">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49c03-164">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="49c03-164">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="49c03-165">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="49c03-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49c03-166">Zeitpunkt, zu dem der Auftrag gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="49c03-166">Time that the job began.</span></span>

</dd> <dt>

<span data-ttu-id="49c03-167">**Status**</span><span class="sxs-lookup"><span data-stu-id="49c03-167">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49c03-168">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="49c03-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49c03-169">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="49c03-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49c03-170">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="49c03-170">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="49c03-171">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="49c03-171">String that indicates the current status of the object.</span></span> <span data-ttu-id="49c03-172">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="49c03-172">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="49c03-173">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="49c03-173">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="49c03-174">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="49c03-174">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="49c03-175">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="49c03-175">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="49c03-176">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="49c03-176">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="49c03-177">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="49c03-177">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="49c03-178">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="49c03-178">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="49c03-179">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="49c03-179">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="49c03-180">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="49c03-180">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="49c03-181">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="49c03-181">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="49c03-182">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="49c03-182">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="49c03-183">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="49c03-183">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="49c03-184">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="49c03-184">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="49c03-185">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="49c03-185">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="49c03-186">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="49c03-186">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="49c03-187">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="49c03-187">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="49c03-188">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="49c03-188">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="49c03-189">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="49c03-189">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="49c03-190">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="49c03-190">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="49c03-191">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="49c03-191">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="49c03-192">**Timesub;**</span><span class="sxs-lookup"><span data-stu-id="49c03-192">**TimeSubmitted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49c03-193">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="49c03-193">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="49c03-194">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="49c03-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49c03-195">Zeitpunkt, zu dem der Auftrag übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="49c03-195">Time that the job was submitted.</span></span>

</dd> <dt>

<span data-ttu-id="49c03-196">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="49c03-196">**UntilTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49c03-197">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="49c03-197">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="49c03-198">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="49c03-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49c03-199">Der Zeitpunkt, zu dem der Auftrag ungültig ist oder angehalten werden soll.</span><span class="sxs-lookup"><span data-stu-id="49c03-199">Time at which the job is invalid or should be stopped.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="49c03-200">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="49c03-200">Remarks</span></span>

<span data-ttu-id="49c03-201">Die **CIM- \_ Auftrags** Klasse wird von [**CIM \_ LogicalElement**](cim-logicalelement.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="49c03-201">The **CIM\_Job** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="49c03-202">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="49c03-202">WMI does not implement this class.</span></span> <span data-ttu-id="49c03-203">Informationen zu Klassen, die vom **CIM- \_ Auftrag** abgeleitet sind, finden Sie unter [Win32](win32-provider.md)</span><span class="sxs-lookup"><span data-stu-id="49c03-203">For classes derived from **CIM\_Job**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="49c03-204">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="49c03-204">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="49c03-205">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="49c03-205">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="49c03-206">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="49c03-206">Requirements</span></span>



| <span data-ttu-id="49c03-207">Anforderung</span><span class="sxs-lookup"><span data-stu-id="49c03-207">Requirement</span></span> | <span data-ttu-id="49c03-208">Wert</span><span class="sxs-lookup"><span data-stu-id="49c03-208">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="49c03-209">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="49c03-209">Minimum supported client</span></span><br/> | <span data-ttu-id="49c03-210">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="49c03-210">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="49c03-211">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="49c03-211">Minimum supported server</span></span><br/> | <span data-ttu-id="49c03-212">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="49c03-212">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="49c03-213">Namespace</span><span class="sxs-lookup"><span data-stu-id="49c03-213">Namespace</span></span><br/>                | <span data-ttu-id="49c03-214">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="49c03-214">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="49c03-215">MOF</span><span class="sxs-lookup"><span data-stu-id="49c03-215">MOF</span></span><br/>                      | <dl> <span data-ttu-id="49c03-216"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="49c03-216"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="49c03-217">DLL</span><span class="sxs-lookup"><span data-stu-id="49c03-217">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49c03-218"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49c03-218"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49c03-219">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="49c03-219">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49c03-220">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="49c03-220">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

