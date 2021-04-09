---
description: Die Win32- \_ Registrierung&\# 8194; WMI-Klasse stellt die Systemregistrierung auf einem Computersystem dar, auf dem Windows ausgeführt wird.
ms.assetid: 4a6cd7d7-2845-434d-b024-d6dbb77371ea
ms.tgt_platform: multiple
title: Win32_Registry-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Registry
- Win32_Registry.Caption
- Win32_Registry.Description
- Win32_Registry.InstallDate
- Win32_Registry.Status
- Win32_Registry.CurrentSize
- Win32_Registry.MaximumSize
- Win32_Registry.Name
- Win32_Registry.ProposedSize
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a1dc5fd89ee589aabda5da5f97632d86b39f6beb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958223"
---
# <a name="win32_registry-class"></a><span data-ttu-id="935b1-103">Win32- \_ Registrierungs Klasse</span><span class="sxs-lookup"><span data-stu-id="935b1-103">Win32\_Registry class</span></span>

<span data-ttu-id="935b1-104">Die  [WMI-Klasse](../wmisdk/retrieving-a-class.md) der **Win32- \_ Registrierung** stellt die Systemregistrierung auf einem Computersystem dar, das Windows ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="935b1-104">The **Win32\_Registry** [WMI class](../wmisdk/retrieving-a-class.md) represents the system registry on a computer system running Windows.</span></span>

<span data-ttu-id="935b1-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="935b1-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="935b1-106">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="935b1-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="935b1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="935b1-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4D7-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Registry : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  uint32   CurrentSize;
  uint32   MaximumSize;
  string   Name;
  uint32   ProposedSize;
};
```

## <a name="members"></a><span data-ttu-id="935b1-108">Member</span><span class="sxs-lookup"><span data-stu-id="935b1-108">Members</span></span>

<span data-ttu-id="935b1-109">Die **Win32- \_ Registrierungs** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="935b1-109">The **Win32\_Registry** class has these types of members:</span></span>

-   [<span data-ttu-id="935b1-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="935b1-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="935b1-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="935b1-111">Properties</span></span>

<span data-ttu-id="935b1-112">Die **Win32- \_ Registrierungs** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="935b1-112">The **Win32\_Registry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="935b1-113">**Caption**</span><span class="sxs-lookup"><span data-stu-id="935b1-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="935b1-114">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="935b1-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="935b1-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="935b1-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="935b1-116">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="935b1-116">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="935b1-117">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="935b1-117">A short textual description of the object.</span></span>

<span data-ttu-id="935b1-118">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="935b1-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="935b1-119">**CurrentSize**</span><span class="sxs-lookup"><span data-stu-id="935b1-119">**CurrentSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="935b1-120">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="935b1-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="935b1-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="935b1-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="935b1-122">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \|NTDLL.DLL\| [**NtQuerySystemInformation**](/windows/win32/api/winternl/nf-winternl-ntquerysysteminformation) \| systemregistryquotainformation"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Megabyte")</span><span class="sxs-lookup"><span data-stu-id="935b1-122">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|NTDLL.DLL\|[**NtQuerySystemInformation**](/windows/win32/api/winternl/nf-winternl-ntquerysysteminformation)\|SystemRegistryQuotaInformation"), [**Units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="935b1-123">Aktuelle physische Größe der Windows-Registrierung.</span><span class="sxs-lookup"><span data-stu-id="935b1-123">Current physical size of the Windows registry.</span></span>

<span data-ttu-id="935b1-124">Beispiel: 10</span><span class="sxs-lookup"><span data-stu-id="935b1-124">Example: 10</span></span>

</dd> <dt>

<span data-ttu-id="935b1-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="935b1-125">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="935b1-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="935b1-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="935b1-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="935b1-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="935b1-128">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="935b1-128">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="935b1-129">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="935b1-129">A textual description of the object.</span></span>

<span data-ttu-id="935b1-130">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="935b1-130">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="935b1-131">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="935b1-131">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="935b1-132">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="935b1-132">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="935b1-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="935b1-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="935b1-134">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="935b1-134">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="935b1-135">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="935b1-135">Indicates when the object was installed.</span></span> <span data-ttu-id="935b1-136">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="935b1-136">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="935b1-137">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="935b1-137">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="935b1-138">**MaximumSize**</span><span class="sxs-lookup"><span data-stu-id="935b1-138">**MaximumSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="935b1-139">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="935b1-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="935b1-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="935b1-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="935b1-141">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \| RegistrySizeLimit"), [**Units**](../wmisdk/standard-qualifiers.md) ("Megabytes")</span><span class="sxs-lookup"><span data-stu-id="935b1-141">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\|RegistrySizeLimit"), [**Units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="935b1-142">Maximale Größe der Windows-Registrierung.</span><span class="sxs-lookup"><span data-stu-id="935b1-142">Maximum size of the Windows registry.</span></span> <span data-ttu-id="935b1-143">Wenn das System mit der **proposedSize** -Eigenschaft erfolgreich ist, sollte **MaximumSize** denselben Wert enthalten.</span><span class="sxs-lookup"><span data-stu-id="935b1-143">If the system is successful in using the **ProposedSize** property, **MaximumSize** should contain the same value.</span></span>

</dd> <dt>

<span data-ttu-id="935b1-144">**Name**</span><span class="sxs-lookup"><span data-stu-id="935b1-144">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="935b1-145">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="935b1-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="935b1-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="935b1-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="935b1-147">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Name"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry")</span><span class="sxs-lookup"><span data-stu-id="935b1-147">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry")</span></span>
</dt> </dl>

<span data-ttu-id="935b1-148">Der Name der Windows-Registrierung.</span><span class="sxs-lookup"><span data-stu-id="935b1-148">Name of the Windows registry.</span></span> <span data-ttu-id="935b1-149">Die maximale Länge beträgt 256 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="935b1-149">The maximum length is 256 characters.</span></span>

</dd> <dt>

<span data-ttu-id="935b1-150">**ProposedSize**</span><span class="sxs-lookup"><span data-stu-id="935b1-150">**ProposedSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="935b1-151">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="935b1-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="935b1-152">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="935b1-152">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="935b1-153">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \| RegistrySizeLimit"), [**Units**](../wmisdk/standard-qualifiers.md) ("Megabytes")</span><span class="sxs-lookup"><span data-stu-id="935b1-153">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\|RegistrySizeLimit"), [**Units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="935b1-154">Vorgeschlagene Größe der Windows-Registrierung.</span><span class="sxs-lookup"><span data-stu-id="935b1-154">Proposed size of the Windows registry.</span></span> <span data-ttu-id="935b1-155">Es ist die einzige Registrierungs Einstellung, die geändert werden kann, und Ihr Vorschlag wird beim nächsten Systemstart versucht.</span><span class="sxs-lookup"><span data-stu-id="935b1-155">It is the only registry setting that can be modified, and its proposal is attempted the next time the system boots.</span></span>

</dd> <dt>

<span data-ttu-id="935b1-156">**Status**</span><span class="sxs-lookup"><span data-stu-id="935b1-156">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="935b1-157">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="935b1-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="935b1-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="935b1-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="935b1-159">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="935b1-159">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="935b1-160">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="935b1-160">String that indicates the current status of the object.</span></span> <span data-ttu-id="935b1-161">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="935b1-161">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="935b1-162">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="935b1-162">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="935b1-163">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="935b1-163">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="935b1-164">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="935b1-164">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="935b1-165">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="935b1-165">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="935b1-166">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="935b1-166">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="935b1-167">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="935b1-167">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="935b1-168">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="935b1-168">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="935b1-169">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="935b1-169">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="935b1-170">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="935b1-170">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="935b1-171">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="935b1-171">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="935b1-172">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="935b1-172">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="935b1-173">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="935b1-173">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="935b1-174">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="935b1-174">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="935b1-175">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="935b1-175">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="935b1-176">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="935b1-176">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="935b1-177">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="935b1-177">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="935b1-178">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="935b1-178">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="935b1-179">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="935b1-179">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="935b1-180">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="935b1-180">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="935b1-181"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="935b1-181"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="935b1-182">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="935b1-182">Remarks</span></span>

<span data-ttu-id="935b1-183">Die **Win32- \_ Registrierungs** Klasse wird von [**CIM \_ LogicalElement**](cim-logicalelement.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="935b1-183">The **Win32\_Registry** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="935b1-184">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="935b1-184">Requirements</span></span>



| <span data-ttu-id="935b1-185">Anforderung</span><span class="sxs-lookup"><span data-stu-id="935b1-185">Requirement</span></span> | <span data-ttu-id="935b1-186">Wert</span><span class="sxs-lookup"><span data-stu-id="935b1-186">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="935b1-187">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="935b1-187">Minimum supported client</span></span><br/> | <span data-ttu-id="935b1-188">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="935b1-188">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="935b1-189">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="935b1-189">Minimum supported server</span></span><br/> | <span data-ttu-id="935b1-190">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="935b1-190">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="935b1-191">Namespace</span><span class="sxs-lookup"><span data-stu-id="935b1-191">Namespace</span></span><br/>                | <span data-ttu-id="935b1-192">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="935b1-192">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="935b1-193">MOF</span><span class="sxs-lookup"><span data-stu-id="935b1-193">MOF</span></span><br/>                      | <dl> <span data-ttu-id="935b1-194"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="935b1-194"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="935b1-195">DLL</span><span class="sxs-lookup"><span data-stu-id="935b1-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="935b1-196"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="935b1-196"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="935b1-197">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="935b1-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="935b1-198">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="935b1-198">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="935b1-199">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="935b1-199">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
