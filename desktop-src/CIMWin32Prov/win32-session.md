---
description: Die Win32- \_ Sitzungs Klasse definiert Zustandsinformationen zur Interaktion zwischen einem Benutzer und einer Ressource, z. b. einem Computersystem oder einer Terminalsitzung.
ms.assetid: 0649001a-914f-403f-9aee-0e9096392fe9
ms.tgt_platform: multiple
title: Win32_Session-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Session
- Win32_Session.Caption
- Win32_Session.Description
- Win32_Session.InstallDate
- Win32_Session.Name
- Win32_Session.Status
- Win32_Session.StartTime
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b7052eb922ec40aca214600f9389e76e5aec4609
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041354"
---
# <a name="win32_session-class"></a><span data-ttu-id="dce2e-103">Win32- \_ Sitzungs Klasse</span><span class="sxs-lookup"><span data-stu-id="dce2e-103">Win32\_Session class</span></span>

<span data-ttu-id="dce2e-104">Die **Win32- \_ Sitzungs** Klasse definiert Zustandsinformationen zur Interaktion zwischen einem Benutzer und einer Ressource, z. b. einem Computersystem oder einer Terminalsitzung.</span><span class="sxs-lookup"><span data-stu-id="dce2e-104">The **Win32\_Session** class defines state information about the interaction between a user and a resource, such as a computer system or a terminal session.</span></span>

<span data-ttu-id="dce2e-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="dce2e-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="dce2e-106">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="dce2e-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="dce2e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="dce2e-107">Syntax</span></span>

``` syntax
[Abstract, AMENDMENT]
class Win32_Session : CIM_logicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  datetime StartTime;
};
```

## <a name="members"></a><span data-ttu-id="dce2e-108">Member</span><span class="sxs-lookup"><span data-stu-id="dce2e-108">Members</span></span>

<span data-ttu-id="dce2e-109">Die **Win32- \_ Sitzungs** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="dce2e-109">The **Win32\_Session** class has these types of members:</span></span>

-   [<span data-ttu-id="dce2e-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dce2e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dce2e-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dce2e-111">Properties</span></span>

<span data-ttu-id="dce2e-112">Die **Win32- \_ Sitzungs** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="dce2e-112">The **Win32\_Session** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dce2e-113">**Caption**</span><span class="sxs-lookup"><span data-stu-id="dce2e-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dce2e-114">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dce2e-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dce2e-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dce2e-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dce2e-116">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="dce2e-116">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="dce2e-117">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="dce2e-117">A short textual description of the object.</span></span>

<span data-ttu-id="dce2e-118">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dce2e-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dce2e-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dce2e-119">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dce2e-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dce2e-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dce2e-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dce2e-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dce2e-122">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="dce2e-122">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="dce2e-123">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="dce2e-123">A textual description of the object.</span></span>

<span data-ttu-id="dce2e-124">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dce2e-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dce2e-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="dce2e-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dce2e-126">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="dce2e-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="dce2e-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dce2e-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dce2e-128">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="dce2e-128">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="dce2e-129">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="dce2e-129">Indicates when the object was installed.</span></span> <span data-ttu-id="dce2e-130">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="dce2e-130">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="dce2e-131">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dce2e-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dce2e-132">**Name**</span><span class="sxs-lookup"><span data-stu-id="dce2e-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dce2e-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dce2e-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dce2e-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dce2e-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dce2e-135">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="dce2e-135">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="dce2e-136">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="dce2e-136">Label by which the object is known.</span></span> <span data-ttu-id="dce2e-137">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="dce2e-137">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="dce2e-138">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dce2e-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dce2e-139">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="dce2e-139">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dce2e-140">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="dce2e-140">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="dce2e-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dce2e-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dce2e-142">Der Zeitpunkt, zu dem die Sitzung gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="dce2e-142">Time at which the session started.</span></span>

</dd> <dt>

<span data-ttu-id="dce2e-143">**Status**</span><span class="sxs-lookup"><span data-stu-id="dce2e-143">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dce2e-144">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dce2e-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dce2e-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dce2e-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dce2e-146">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="dce2e-146">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="dce2e-147">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="dce2e-147">String that indicates the current status of the object.</span></span> <span data-ttu-id="dce2e-148">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="dce2e-148">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="dce2e-149">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="dce2e-149">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="dce2e-150">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="dce2e-150">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="dce2e-151">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="dce2e-151">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="dce2e-152">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="dce2e-152">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="dce2e-153">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="dce2e-153">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="dce2e-154">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dce2e-154">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="dce2e-155">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="dce2e-155">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="dce2e-156">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="dce2e-156">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="dce2e-157">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="dce2e-157">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="dce2e-158">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="dce2e-158">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dce2e-159">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="dce2e-159">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="dce2e-160">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="dce2e-160">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="dce2e-161">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="dce2e-161">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="dce2e-162">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="dce2e-162">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="dce2e-163">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="dce2e-163">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="dce2e-164">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="dce2e-164">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="dce2e-165">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="dce2e-165">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="dce2e-166">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="dce2e-166">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="dce2e-167">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="dce2e-167">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="dce2e-168"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="dce2e-168"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="dce2e-169">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dce2e-169">Remarks</span></span>

<span data-ttu-id="dce2e-170">Die **Win32- \_ Sitzungs** Klasse wird von [**CIM \_ LogicalElement**](cim-logicalelement.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="dce2e-170">The **Win32\_Session** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dce2e-171">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dce2e-171">Requirements</span></span>



| <span data-ttu-id="dce2e-172">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dce2e-172">Requirement</span></span> | <span data-ttu-id="dce2e-173">Wert</span><span class="sxs-lookup"><span data-stu-id="dce2e-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dce2e-174">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dce2e-174">Minimum supported client</span></span><br/> | <span data-ttu-id="dce2e-175">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dce2e-175">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dce2e-176">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dce2e-176">Minimum supported server</span></span><br/> | <span data-ttu-id="dce2e-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dce2e-177">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dce2e-178">Namespace</span><span class="sxs-lookup"><span data-stu-id="dce2e-178">Namespace</span></span><br/>                | <span data-ttu-id="dce2e-179">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="dce2e-179">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="dce2e-180">MOF</span><span class="sxs-lookup"><span data-stu-id="dce2e-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dce2e-181"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="dce2e-181"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="dce2e-182">DLL</span><span class="sxs-lookup"><span data-stu-id="dce2e-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dce2e-183"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dce2e-183"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dce2e-184">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dce2e-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dce2e-185">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="dce2e-185">**CIM\_logicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

 
