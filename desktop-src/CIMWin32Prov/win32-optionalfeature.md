---
description: Stellt den Status der optionalen Funktionen dar, die auf dem Betriebssystem vorhanden sind.
ms.assetid: 3ac0c227-dfe1-4f33-b3d1-bcd1309c3635
ms.tgt_platform: multiple
title: Win32_OptionalFeature-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OptionalFeature
- Win32_OptionalFeature.Description
- Win32_OptionalFeature.InstallDate
- Win32_OptionalFeature.Status
- Win32_OptionalFeature.Caption
- Win32_OptionalFeature.Name
- Win32_OptionalFeature.InstallState
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9ee0a8fc631430401328170f15c0dd2653d0ce8b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343004"
---
# <a name="win32_optionalfeature-class"></a><span data-ttu-id="9e6de-103">Win32 \_ optionalfeature-Klasse</span><span class="sxs-lookup"><span data-stu-id="9e6de-103">Win32\_OptionalFeature class</span></span>

<span data-ttu-id="9e6de-104">Stellt den Status der optionalen Funktionen dar, die auf dem Betriebssystem vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="9e6de-104">Represents the status of the optional features that are present on the operating system.</span></span>

<span data-ttu-id="9e6de-105">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="9e6de-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e6de-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9e6de-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{0827250D-BA3E-11d2-B361-00105A1F77A2}"), AMENDMENT]
class Win32_OptionalFeature : CIM_LogicalElement
{
  string   Description;
  datetime InstallDate;
  string   Status;
  string   Caption;
  string   Name;
  uint32   InstallState;
};
```

## <a name="members"></a><span data-ttu-id="9e6de-107">Member</span><span class="sxs-lookup"><span data-stu-id="9e6de-107">Members</span></span>

<span data-ttu-id="9e6de-108">Die **Win32 \_ optionalfeature** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="9e6de-108">The **Win32\_OptionalFeature** class has these types of members:</span></span>

-   [<span data-ttu-id="9e6de-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9e6de-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9e6de-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9e6de-110">Properties</span></span>

<span data-ttu-id="9e6de-111">Die **Win32 \_ optionalfeature** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9e6de-111">The **Win32\_OptionalFeature** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9e6de-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="9e6de-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e6de-113">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9e6de-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e6de-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9e6de-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e6de-115">Qualifizierer: [**außer Kraft**](../wmisdk/standard-qualifiers.md) Setzung (Beschriftung), [**maxlen**](../wmisdk/standard-qualifiers.md) (260)</span><span class="sxs-lookup"><span data-stu-id="9e6de-115">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) (Caption), [**MaxLen**](../wmisdk/standard-qualifiers.md) (260)</span></span>
</dt> </dl>

<span data-ttu-id="9e6de-116">Ein optionaler Anzeige Name für die Funktion.</span><span class="sxs-lookup"><span data-stu-id="9e6de-116">An optional feature display name.</span></span>

</dd> <dt>

<span data-ttu-id="9e6de-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9e6de-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e6de-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9e6de-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e6de-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9e6de-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e6de-120">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="9e6de-120">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="9e6de-121">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="9e6de-121">A textual description of the object.</span></span>

<span data-ttu-id="9e6de-122">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9e6de-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e6de-123">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9e6de-123">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e6de-124">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="9e6de-124">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9e6de-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9e6de-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e6de-126">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="9e6de-126">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="9e6de-127">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="9e6de-127">Indicates when the object was installed.</span></span> <span data-ttu-id="9e6de-128">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="9e6de-128">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="9e6de-129">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9e6de-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e6de-130">**InstallState**</span><span class="sxs-lookup"><span data-stu-id="9e6de-130">**InstallState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e6de-131">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9e6de-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9e6de-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9e6de-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e6de-133">Gibt den Status der optionalen Funktion an.</span><span class="sxs-lookup"><span data-stu-id="9e6de-133">Identifies the state of the optional feature.</span></span> <span data-ttu-id="9e6de-134">Folgende Zustände sind möglich:</span><span class="sxs-lookup"><span data-stu-id="9e6de-134">The following states are possible:</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="9e6de-135">**Aktiviert** (1)</span><span class="sxs-lookup"><span data-stu-id="9e6de-135">**Enabled** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="9e6de-136">**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="9e6de-136">**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Absent"></span><span id="absent"></span><span id="ABSENT"></span>

<span data-ttu-id="9e6de-137">Nicht **vorhanden** (3)</span><span class="sxs-lookup"><span data-stu-id="9e6de-137">**Absent** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9e6de-138">**Unbekannt** (4)</span><span class="sxs-lookup"><span data-stu-id="9e6de-138">**Unknown** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9e6de-139">**Name**</span><span class="sxs-lookup"><span data-stu-id="9e6de-139">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e6de-140">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9e6de-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e6de-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9e6de-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e6de-142">Qualifizierer: [**override**](../wmisdk/standard-qualifiers.md) (Name), [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (260)</span><span class="sxs-lookup"><span data-stu-id="9e6de-142">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) (Name), [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (260)</span></span>
</dt> </dl>

<span data-ttu-id="9e6de-143">Stellt den Namen der optionalen Funktion dar.</span><span class="sxs-lookup"><span data-stu-id="9e6de-143">Represents the name of the optional feature.</span></span>

</dd> <dt>

<span data-ttu-id="9e6de-144">**Status**</span><span class="sxs-lookup"><span data-stu-id="9e6de-144">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e6de-145">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9e6de-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e6de-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9e6de-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e6de-147">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="9e6de-147">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="9e6de-148">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="9e6de-148">String that indicates the current status of the object.</span></span> <span data-ttu-id="9e6de-149">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="9e6de-149">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="9e6de-150">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="9e6de-150">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="9e6de-151">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="9e6de-151">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="9e6de-152">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="9e6de-152">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="9e6de-153">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="9e6de-153">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="9e6de-154">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="9e6de-154">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="9e6de-155">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9e6de-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="9e6de-156">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="9e6de-156">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="9e6de-157">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="9e6de-157">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="9e6de-158">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="9e6de-158">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="9e6de-159">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="9e6de-159">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9e6de-160">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="9e6de-160">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="9e6de-161">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="9e6de-161">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="9e6de-162">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="9e6de-162">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="9e6de-163">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="9e6de-163">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="9e6de-164">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="9e6de-164">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="9e6de-165">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="9e6de-165">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="9e6de-166">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="9e6de-166">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="9e6de-167">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="9e6de-167">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="9e6de-168">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="9e6de-168">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="9e6de-169"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="9e6de-169"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="9e6de-170">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9e6de-170">Requirements</span></span>



| <span data-ttu-id="9e6de-171">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9e6de-171">Requirement</span></span> | <span data-ttu-id="9e6de-172">Wert</span><span class="sxs-lookup"><span data-stu-id="9e6de-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e6de-173">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9e6de-173">Minimum supported client</span></span><br/> | <span data-ttu-id="9e6de-174">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9e6de-174">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="9e6de-175">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9e6de-175">Minimum supported server</span></span><br/> | <span data-ttu-id="9e6de-176">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9e6de-176">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="9e6de-177">Namespace</span><span class="sxs-lookup"><span data-stu-id="9e6de-177">Namespace</span></span><br/>                | <span data-ttu-id="9e6de-178">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="9e6de-178">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9e6de-179">MOF</span><span class="sxs-lookup"><span data-stu-id="9e6de-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9e6de-180"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9e6de-180"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9e6de-181">DLL</span><span class="sxs-lookup"><span data-stu-id="9e6de-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e6de-182"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e6de-182"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e6de-183">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9e6de-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e6de-184">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="9e6de-184">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="9e6de-185">**CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="9e6de-185">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> <dt>

[<span data-ttu-id="9e6de-186">Abfragen des Status optionaler Funktionen</span><span class="sxs-lookup"><span data-stu-id="9e6de-186">Querying the Status of Optional Features</span></span>](../wmisdk/querying-the-status-of-optional-features.md)
</dt> </dl>

 

 
