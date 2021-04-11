---
description: Die \_ WMI-Klasse "Win32 programgrouporitem" stellt eine logische Gruppierung von Programmen im Menü "Programme starten" des Benutzers dar \\ . Sie enthält Programm Gruppen und Programm Gruppenelemente.
ms.assetid: 48ec5436-e931-4f00-ab36-03b04ad33529
ms.tgt_platform: multiple
title: Win32_ProgramGroupOrItem-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ProgramGroupOrItem
- Win32_ProgramGroupOrItem.Caption
- Win32_ProgramGroupOrItem.Description
- Win32_ProgramGroupOrItem.InstallDate
- Win32_ProgramGroupOrItem.Name
- Win32_ProgramGroupOrItem.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bb12576acbc8b50befa5d0856343b61e325b9478
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126086"
---
# <a name="win32_programgrouporitem-class"></a><span data-ttu-id="6fac4-104">Win32 \_ programgrouporitem-Klasse</span><span class="sxs-lookup"><span data-stu-id="6fac4-104">Win32\_ProgramGroupOrItem class</span></span>

<span data-ttu-id="6fac4-105">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) " **Win32 \_ programgrouporitem** " stellt eine logische Gruppierung von Programmen im Menü **" \\ Programme starten** " des Benutzers dar.</span><span class="sxs-lookup"><span data-stu-id="6fac4-105">The **Win32\_ProgramGroupOrItem** abstract [WMI class](../wmisdk/retrieving-a-class.md) represents a logical grouping of programs on the user's **Start\\Programs** menu.</span></span> <span data-ttu-id="6fac4-106">Sie enthält Programm Gruppen und Programm Gruppenelemente.</span><span class="sxs-lookup"><span data-stu-id="6fac4-106">It contains program groups and program group items.</span></span>

<span data-ttu-id="6fac4-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6fac4-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="6fac4-108">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="6fac4-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fac4-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="6fac4-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{86E30E86-7DB2-11d2-90CB-0060081A46FD}"), AMENDMENT]
class Win32_ProgramGroupOrItem : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="6fac4-110">Member</span><span class="sxs-lookup"><span data-stu-id="6fac4-110">Members</span></span>

<span data-ttu-id="6fac4-111">Die **Win32 \_ programgrouporitem** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6fac4-111">The **Win32\_ProgramGroupOrItem** class has these types of members:</span></span>

-   [<span data-ttu-id="6fac4-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6fac4-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6fac4-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6fac4-113">Properties</span></span>

<span data-ttu-id="6fac4-114">Die **Win32 \_ programgrouporitem** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6fac4-114">The **Win32\_ProgramGroupOrItem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6fac4-115">**Caption**</span><span class="sxs-lookup"><span data-stu-id="6fac4-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fac4-116">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6fac4-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6fac4-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6fac4-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6fac4-118">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="6fac4-118">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="6fac4-119">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="6fac4-119">A short textual description of the object.</span></span>

<span data-ttu-id="6fac4-120">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6fac4-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6fac4-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6fac4-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fac4-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6fac4-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6fac4-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6fac4-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6fac4-124">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="6fac4-124">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="6fac4-125">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="6fac4-125">A textual description of the object.</span></span>

<span data-ttu-id="6fac4-126">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6fac4-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6fac4-127">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="6fac4-127">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fac4-128">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="6fac4-128">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6fac4-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6fac4-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6fac4-130">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="6fac4-130">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="6fac4-131">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="6fac4-131">Indicates when the object was installed.</span></span> <span data-ttu-id="6fac4-132">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="6fac4-132">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="6fac4-133">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6fac4-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6fac4-134">**Name**</span><span class="sxs-lookup"><span data-stu-id="6fac4-134">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fac4-135">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6fac4-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6fac4-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6fac4-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6fac4-137">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="6fac4-137">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="6fac4-138">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="6fac4-138">Label by which the object is known.</span></span> <span data-ttu-id="6fac4-139">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="6fac4-139">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="6fac4-140">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6fac4-140">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6fac4-141">**Status**</span><span class="sxs-lookup"><span data-stu-id="6fac4-141">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fac4-142">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6fac4-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6fac4-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6fac4-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6fac4-144">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="6fac4-144">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="6fac4-145">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="6fac4-145">String that indicates the current status of the object.</span></span> <span data-ttu-id="6fac4-146">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="6fac4-146">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="6fac4-147">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="6fac4-147">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="6fac4-148">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="6fac4-148">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="6fac4-149">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="6fac4-149">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="6fac4-150">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="6fac4-150">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="6fac4-151">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="6fac4-151">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="6fac4-152">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6fac4-152">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="6fac4-153">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="6fac4-153">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="6fac4-154">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="6fac4-154">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="6fac4-155">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="6fac4-155">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="6fac4-156">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="6fac4-156">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6fac4-157">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="6fac4-157">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="6fac4-158">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="6fac4-158">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="6fac4-159">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="6fac4-159">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="6fac4-160">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="6fac4-160">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="6fac4-161">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="6fac4-161">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="6fac4-162">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="6fac4-162">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="6fac4-163">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="6fac4-163">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="6fac4-164">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="6fac4-164">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="6fac4-165">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="6fac4-165">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="6fac4-166"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="6fac4-166"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="6fac4-167">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6fac4-167">Remarks</span></span>

<span data-ttu-id="6fac4-168">Die **Win32 \_ programgrouporitem** -Klasse wird von [**CIM \_ LogicalElement**](cim-logicalelement.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="6fac4-168">The **Win32\_ProgramGroupOrItem** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6fac4-169">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6fac4-169">Requirements</span></span>



| <span data-ttu-id="6fac4-170">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6fac4-170">Requirement</span></span> | <span data-ttu-id="6fac4-171">Wert</span><span class="sxs-lookup"><span data-stu-id="6fac4-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6fac4-172">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6fac4-172">Minimum supported client</span></span><br/> | <span data-ttu-id="6fac4-173">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6fac4-173">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6fac4-174">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6fac4-174">Minimum supported server</span></span><br/> | <span data-ttu-id="6fac4-175">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6fac4-175">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6fac4-176">Namespace</span><span class="sxs-lookup"><span data-stu-id="6fac4-176">Namespace</span></span><br/>                | <span data-ttu-id="6fac4-177">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="6fac4-177">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6fac4-178">MOF</span><span class="sxs-lookup"><span data-stu-id="6fac4-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6fac4-179"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="6fac4-179"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6fac4-180">DLL</span><span class="sxs-lookup"><span data-stu-id="6fac4-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6fac4-181"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6fac4-181"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fac4-182">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6fac4-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fac4-183">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="6fac4-183">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="6fac4-184">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="6fac4-184">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
