---
description: Die CIM \_ LogicalElement-Klasse ist die Basisklasse für alle Systemkomponenten, die abstrakte Systemkomponenten, z. b. profile, Prozesse oder Systemfunktionen, in Form logischer Geräte darstellen.
ms.assetid: 81b2788a-96e8-4570-9a13-d11d229ad789
ms.tgt_platform: multiple
title: CIM_LogicalElement-Klasse (cimwin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalElement
- CIM_LogicalElement.Caption
- CIM_LogicalElement.Description
- CIM_LogicalElement.InstallDate
- CIM_LogicalElement.Name
- CIM_LogicalElement.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 281ba9f97dafb246917d602fcfe1061f4cb03f86
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860764"
---
# <a name="cim_logicalelement-class-cimwin32-wmi-providers"></a><span data-ttu-id="36e72-103">CIM_LogicalElement-Klasse (cimwin32-WMI-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="36e72-103">CIM_LogicalElement class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="36e72-104">Die **CIM \_ LogicalElement** -Klasse ist die Basisklasse für alle Systemkomponenten, die abstrakte Systemkomponenten, z. b. profile, Prozesse oder Systemfunktionen, in Form logischer Geräte darstellen.</span><span class="sxs-lookup"><span data-stu-id="36e72-104">The **CIM\_LogicalElement** class is the base class for all system components that represent abstract system components, such as profiles, processes, or system capabilities, in the form of logical devices.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="36e72-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="36e72-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="36e72-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="36e72-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="36e72-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="36e72-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="36e72-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="36e72-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="36e72-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="36e72-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C518-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Logical Elements (CIM)"), AMENDMENT]
class CIM_LogicalElement : CIM_ManagedSystemElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="36e72-110">Member</span><span class="sxs-lookup"><span data-stu-id="36e72-110">Members</span></span>

<span data-ttu-id="36e72-111">Die **CIM \_ LogicalElement** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="36e72-111">The **CIM\_LogicalElement** class has these types of members:</span></span>

-   [<span data-ttu-id="36e72-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="36e72-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="36e72-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="36e72-113">Properties</span></span>

<span data-ttu-id="36e72-114">Die **CIM \_ LogicalElement** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="36e72-114">The **CIM\_LogicalElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="36e72-115">**Caption**</span><span class="sxs-lookup"><span data-stu-id="36e72-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36e72-116">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="36e72-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36e72-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36e72-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36e72-118">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="36e72-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="36e72-119">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="36e72-119">A short textual description of the object.</span></span>

<span data-ttu-id="36e72-120">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="36e72-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="36e72-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="36e72-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36e72-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="36e72-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36e72-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36e72-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36e72-124">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="36e72-124">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="36e72-125">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="36e72-125">A textual description of the object.</span></span>

<span data-ttu-id="36e72-126">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="36e72-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="36e72-127">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="36e72-127">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36e72-128">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="36e72-128">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="36e72-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36e72-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36e72-130">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="36e72-130">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="36e72-131">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="36e72-131">Indicates when the object was installed.</span></span> <span data-ttu-id="36e72-132">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="36e72-132">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="36e72-133">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="36e72-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="36e72-134">**Name**</span><span class="sxs-lookup"><span data-stu-id="36e72-134">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36e72-135">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="36e72-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36e72-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36e72-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36e72-137">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="36e72-137">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="36e72-138">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="36e72-138">Label by which the object is known.</span></span> <span data-ttu-id="36e72-139">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="36e72-139">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="36e72-140">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="36e72-140">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="36e72-141">**Status**</span><span class="sxs-lookup"><span data-stu-id="36e72-141">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36e72-142">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="36e72-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="36e72-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="36e72-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36e72-144">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="36e72-144">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="36e72-145">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="36e72-145">String that indicates the current status of the object.</span></span> <span data-ttu-id="36e72-146">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="36e72-146">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="36e72-147">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="36e72-147">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="36e72-148">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="36e72-148">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="36e72-149">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="36e72-149">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="36e72-150">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="36e72-150">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="36e72-151">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="36e72-151">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="36e72-152">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="36e72-152">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="36e72-153">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="36e72-153">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="36e72-154">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="36e72-154">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="36e72-155">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="36e72-155">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="36e72-156">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="36e72-156">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="36e72-157">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="36e72-157">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="36e72-158">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="36e72-158">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="36e72-159">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="36e72-159">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="36e72-160">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="36e72-160">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="36e72-161">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="36e72-161">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="36e72-162">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="36e72-162">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="36e72-163">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="36e72-163">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="36e72-164">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="36e72-164">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="36e72-165">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="36e72-165">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="36e72-166"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="36e72-166"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="36e72-167">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="36e72-167">Remarks</span></span>

<span data-ttu-id="36e72-168">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="36e72-168">WMI does not implement this class.</span></span> <span data-ttu-id="36e72-169">Informationen zu Klassen, die von **CIM \_ LogicalElement** abgeleitet sind, finden Sie unter [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="36e72-169">For classes derived from **CIM\_LogicalElement**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="36e72-170">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="36e72-170">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="36e72-171">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="36e72-171">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="36e72-172">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="36e72-172">Requirements</span></span>



| <span data-ttu-id="36e72-173">Anforderung</span><span class="sxs-lookup"><span data-stu-id="36e72-173">Requirement</span></span> | <span data-ttu-id="36e72-174">Wert</span><span class="sxs-lookup"><span data-stu-id="36e72-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="36e72-175">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="36e72-175">Minimum supported client</span></span><br/> | <span data-ttu-id="36e72-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="36e72-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="36e72-177">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="36e72-177">Minimum supported server</span></span><br/> | <span data-ttu-id="36e72-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="36e72-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="36e72-179">Namespace</span><span class="sxs-lookup"><span data-stu-id="36e72-179">Namespace</span></span><br/>                | <span data-ttu-id="36e72-180">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="36e72-180">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="36e72-181">MOF</span><span class="sxs-lookup"><span data-stu-id="36e72-181">MOF</span></span><br/>                      | <dl> <span data-ttu-id="36e72-182"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="36e72-182"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="36e72-183">DLL</span><span class="sxs-lookup"><span data-stu-id="36e72-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36e72-184"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36e72-184"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36e72-185">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="36e72-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36e72-186">**CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="36e72-186">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> </dl>

 

