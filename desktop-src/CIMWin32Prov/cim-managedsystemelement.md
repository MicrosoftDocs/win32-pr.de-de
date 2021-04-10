---
description: Die CIM \_ ManagedSystemElement-Klasse ist die Basisklasse für die System Element Hierarchie. Jede unterscheidbare Systemkomponente ist ein Kandidat für die Einbindung in diese Klasse.
ms.assetid: f1b952f4-4bed-4420-ad5d-62478846be8e
ms.tgt_platform: multiple
title: CIM_ManagedSystemElement-Klasse (cimwin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ManagedSystemElement
- CIM_ManagedSystemElement.Caption
- CIM_ManagedSystemElement.Description
- CIM_ManagedSystemElement.InstallDate
- CIM_ManagedSystemElement.Name
- CIM_ManagedSystemElement.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 60684d131a034f809a18898ec05ccc5f73f253f0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126944"
---
# <a name="cim_managedsystemelement-class-cimwin32-wmi-providers"></a><span data-ttu-id="a64a9-104">CIM_ManagedSystemElement-Klasse (cimwin32-WMI-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="a64a9-104">CIM_ManagedSystemElement class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="a64a9-105">Die **CIM \_ ManagedSystemElement** -Klasse ist die Basisklasse für die System Element Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="a64a9-105">The **CIM\_ManagedSystemElement** class is the base class for the system element hierarchy.</span></span> <span data-ttu-id="a64a9-106">Jede unterscheidbare Systemkomponente ist ein Kandidat für die Einbindung in diese Klasse.</span><span class="sxs-lookup"><span data-stu-id="a64a9-106">Any distinguishable system component is a candidate for inclusion in this class.</span></span> <span data-ttu-id="a64a9-107">Beispiele hierfür sind Softwarekomponenten wie z. b. Dateien. Geräte, z. b. Laufwerke und Controller und physische Komponenten, z. b. Chips und Karten.</span><span class="sxs-lookup"><span data-stu-id="a64a9-107">Examples include software components, such as files; devices, such as disk drives and controllers; and physical components, such as chips and cards.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a64a9-108">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="a64a9-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a64a9-109">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a64a9-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a64a9-110">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="a64a9-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="a64a9-111">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="a64a9-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a64a9-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="a64a9-112">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C517-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Managed System Elements (CIM)"), AMENDMENT]
class CIM_ManagedSystemElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="a64a9-113">Member</span><span class="sxs-lookup"><span data-stu-id="a64a9-113">Members</span></span>

<span data-ttu-id="a64a9-114">Die **CIM \_ ManagedSystemElement** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a64a9-114">The **CIM\_ManagedSystemElement** class has these types of members:</span></span>

-   [<span data-ttu-id="a64a9-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a64a9-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a64a9-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a64a9-116">Properties</span></span>

<span data-ttu-id="a64a9-117">Die **CIM \_ ManagedSystemElement** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a64a9-117">The **CIM\_ManagedSystemElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a64a9-118">**Caption**</span><span class="sxs-lookup"><span data-stu-id="a64a9-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a64a9-119">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a64a9-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a64a9-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a64a9-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a64a9-121">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="a64a9-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="a64a9-122">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="a64a9-122">A short textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="a64a9-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a64a9-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a64a9-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a64a9-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a64a9-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a64a9-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a64a9-126">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="a64a9-126">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="a64a9-127">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="a64a9-127">A textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="a64a9-128">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a64a9-128">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a64a9-129">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="a64a9-129">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a64a9-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a64a9-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a64a9-131">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="a64a9-131">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="a64a9-132">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="a64a9-132">Indicates when the object was installed.</span></span> <span data-ttu-id="a64a9-133">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="a64a9-133">Lack of a value does not indicate that the object is not installed.</span></span>

</dd> <dt>

<span data-ttu-id="a64a9-134">**Name**</span><span class="sxs-lookup"><span data-stu-id="a64a9-134">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a64a9-135">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a64a9-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a64a9-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a64a9-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a64a9-137">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="a64a9-137">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="a64a9-138">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="a64a9-138">Label by which the object is known.</span></span> <span data-ttu-id="a64a9-139">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="a64a9-139">When subclassed, this property can be overridden to be a key property.</span></span>

</dd> <dt>

<span data-ttu-id="a64a9-140">**Status**</span><span class="sxs-lookup"><span data-stu-id="a64a9-140">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a64a9-141">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a64a9-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a64a9-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a64a9-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a64a9-143">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="a64a9-143">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="a64a9-144">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="a64a9-144">String that indicates the current status of the object.</span></span> <span data-ttu-id="a64a9-145">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="a64a9-145">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="a64a9-146">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="a64a9-146">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="a64a9-147">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="a64a9-147">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="a64a9-148">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="a64a9-148">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="a64a9-149">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="a64a9-149">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="a64a9-150">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="a64a9-150">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="a64a9-151">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="a64a9-151">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="a64a9-152">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="a64a9-152">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="a64a9-153">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="a64a9-153">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a64a9-154">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="a64a9-154">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a64a9-155">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="a64a9-155">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="a64a9-156">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="a64a9-156">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="a64a9-157">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="a64a9-157">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="a64a9-158">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="a64a9-158">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="a64a9-159">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="a64a9-159">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="a64a9-160">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="a64a9-160">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="a64a9-161">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="a64a9-161">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="a64a9-162">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="a64a9-162">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="a64a9-163">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="a64a9-163">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="a64a9-164"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="a64a9-164"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="a64a9-165">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a64a9-165">Remarks</span></span>

<span data-ttu-id="a64a9-166">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="a64a9-166">WMI does not implement this class.</span></span> <span data-ttu-id="a64a9-167">Informationen zu WMI-Klassen, die von dieser Klasse abgeleitet werden, finden Sie unter [Win32 Classes](win32-provider.md)</span><span class="sxs-lookup"><span data-stu-id="a64a9-167">For WMI classes derived from this class, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="a64a9-168">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="a64a9-168">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a64a9-169">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="a64a9-169">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a64a9-170">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a64a9-170">Requirements</span></span>



| <span data-ttu-id="a64a9-171">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a64a9-171">Requirement</span></span> | <span data-ttu-id="a64a9-172">Wert</span><span class="sxs-lookup"><span data-stu-id="a64a9-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a64a9-173">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a64a9-173">Minimum supported client</span></span><br/> | <span data-ttu-id="a64a9-174">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a64a9-174">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a64a9-175">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a64a9-175">Minimum supported server</span></span><br/> | <span data-ttu-id="a64a9-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a64a9-176">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a64a9-177">Namespace</span><span class="sxs-lookup"><span data-stu-id="a64a9-177">Namespace</span></span><br/>                | <span data-ttu-id="a64a9-178">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a64a9-178">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a64a9-179">MOF</span><span class="sxs-lookup"><span data-stu-id="a64a9-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a64a9-180"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a64a9-180"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a64a9-181">DLL</span><span class="sxs-lookup"><span data-stu-id="a64a9-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a64a9-182"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a64a9-182"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

