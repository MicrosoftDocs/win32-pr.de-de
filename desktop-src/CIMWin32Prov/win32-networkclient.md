---
description: Die Win32 \_ Network Client-WMI-Klasse stellt einen Netzwerkclient auf einem Windows-System dar. Jedes Computersystem im Netzwerk mit einer Client Beziehung zum System ist ein Nachfolger (oder Mitglied) dieser Klasse.
ms.assetid: f0cc2cef-be23-42f4-a592-2c292aa5085f
ms.tgt_platform: multiple
title: Win32_NetworkClient-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkClient
- Win32_NetworkClient.Caption
- Win32_NetworkClient.Description
- Win32_NetworkClient.InstallDate
- Win32_NetworkClient.Status
- Win32_NetworkClient.Manufacturer
- Win32_NetworkClient.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 54579073b3974a6c4954ef95b1da3fe2e9fd8348
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958544"
---
# <a name="win32_networkclient-class"></a><span data-ttu-id="d1a86-104">Win32- \_ networkclient-Klasse</span><span class="sxs-lookup"><span data-stu-id="d1a86-104">Win32\_NetworkClient class</span></span>

<span data-ttu-id="d1a86-105">Die **Win32 \_ Network Client** - [WMI-Klasse](../wmisdk/retrieving-a-class.md) stellt einen Netzwerkclient auf einem Windows-System dar.</span><span class="sxs-lookup"><span data-stu-id="d1a86-105">The **Win32\_NetworkClient** [WMI class](../wmisdk/retrieving-a-class.md) represents a network client on a Windows system.</span></span> <span data-ttu-id="d1a86-106">Jedes Computersystem im Netzwerk mit einer Client Beziehung zum System ist ein Nachfolger (oder Mitglied) dieser Klasse.</span><span class="sxs-lookup"><span data-stu-id="d1a86-106">Any computer system on the network with a client relationship to the system is a descendant (or member) of this class.</span></span>

<span data-ttu-id="d1a86-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d1a86-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="d1a86-108">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="d1a86-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1a86-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1a86-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D5-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkClient : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   Manufacturer;
  string   Name;
};
```

## <a name="members"></a><span data-ttu-id="d1a86-110">Member</span><span class="sxs-lookup"><span data-stu-id="d1a86-110">Members</span></span>

<span data-ttu-id="d1a86-111">Die **Win32- \_ networkclient** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d1a86-111">The **Win32\_NetworkClient** class has these types of members:</span></span>

-   [<span data-ttu-id="d1a86-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d1a86-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d1a86-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d1a86-113">Properties</span></span>

<span data-ttu-id="d1a86-114">Die **Win32- \_ networkclient** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d1a86-114">The **Win32\_NetworkClient** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d1a86-115">**Caption**</span><span class="sxs-lookup"><span data-stu-id="d1a86-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1a86-116">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d1a86-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1a86-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d1a86-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1a86-118">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="d1a86-118">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="d1a86-119">Eine kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="d1a86-119">A short textual description of the object.</span></span>

<span data-ttu-id="d1a86-120">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d1a86-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1a86-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d1a86-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1a86-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d1a86-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1a86-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d1a86-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1a86-124">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="d1a86-124">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="d1a86-125">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="d1a86-125">A textual description of the object.</span></span>

<span data-ttu-id="d1a86-126">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d1a86-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1a86-127">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d1a86-127">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1a86-128">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="d1a86-128">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d1a86-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d1a86-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1a86-130">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="d1a86-130">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="d1a86-131">Gibt an, wann das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="d1a86-131">Indicates when the object was installed.</span></span> <span data-ttu-id="d1a86-132">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="d1a86-132">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="d1a86-133">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d1a86-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1a86-134">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="d1a86-134">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1a86-135">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d1a86-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1a86-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d1a86-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1a86-137">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ LanmanWorkstation \\ \\ NetworkProvider \| MFG")</span><span class="sxs-lookup"><span data-stu-id="d1a86-137">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\LanmanWorkstation\\\\NetworkProvider\|Mfg")</span></span>
</dt> </dl>

<span data-ttu-id="d1a86-138">Der Name des Herstellers des Netzwerk Clients, der auf dem Computersystem ausgeführt wird, auf dem Windows ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d1a86-138">Name of the manufacturer of the network client running on the computer system running Windows.</span></span>

<span data-ttu-id="d1a86-139">Beispiel: "Microsoft Corporation"</span><span class="sxs-lookup"><span data-stu-id="d1a86-139">Example: "Microsoft Corporation"</span></span>

</dd> <dt>

<span data-ttu-id="d1a86-140">**Name**</span><span class="sxs-lookup"><span data-stu-id="d1a86-140">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1a86-141">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d1a86-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1a86-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d1a86-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1a86-143">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Name"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ LanmanWorkstation \\ \\ Network Provider \| Name")</span><span class="sxs-lookup"><span data-stu-id="d1a86-143">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\LanmanWorkstation\\\\NetworkProvider\|Name")</span></span>
</dt> </dl>

<span data-ttu-id="d1a86-144">Netzwerkname des Netzwerk Clients, der auf dem Computersystem ausgeführt wird, auf dem Windows ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d1a86-144">Network name of the network client running on the computer system running Windows.</span></span>

<span data-ttu-id="d1a86-145">Beispiel: "Microsoft Windows-Netzwerk"</span><span class="sxs-lookup"><span data-stu-id="d1a86-145">Example: "Microsoft Windows Network"</span></span>

</dd> <dt>

<span data-ttu-id="d1a86-146">**Status**</span><span class="sxs-lookup"><span data-stu-id="d1a86-146">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1a86-147">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d1a86-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1a86-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d1a86-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1a86-149">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="d1a86-149">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="d1a86-150">Eine Zeichenfolge, die den aktuellen Status des Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="d1a86-150">String that indicates the current status of the object.</span></span> <span data-ttu-id="d1a86-151">Der Betriebsstatus und der nicht betriebliche Status können definiert werden.</span><span class="sxs-lookup"><span data-stu-id="d1a86-151">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="d1a86-152">Der Betriebsstatus kann "OK", "heruntergestuft" und "pred Fail" enthalten.</span><span class="sxs-lookup"><span data-stu-id="d1a86-152">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="d1a86-153">"Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. b. ein intelligent-fähiges Festplattenlaufwerk).</span><span class="sxs-lookup"><span data-stu-id="d1a86-153">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="d1a86-154">Der nicht betriebliche Status kann "Error", "Starting", "Stop" und "Service" enthalten.</span><span class="sxs-lookup"><span data-stu-id="d1a86-154">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="d1a86-155">"Service" kann während der Datenträger Spiegelung angewendet werden, indem eine Benutzer Berechtigungs Liste oder eine andere administrative Arbeit neu geladen wird.</span><span class="sxs-lookup"><span data-stu-id="d1a86-155">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="d1a86-156">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="d1a86-156">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="d1a86-157">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d1a86-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="d1a86-158">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="d1a86-158">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="d1a86-159">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="d1a86-159">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="d1a86-160">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="d1a86-160">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d1a86-161">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="d1a86-161">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d1a86-162">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="d1a86-162">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="d1a86-163">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="d1a86-163">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="d1a86-164">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="d1a86-164">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="d1a86-165">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="d1a86-165">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="d1a86-166">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="d1a86-166">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="d1a86-167">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="d1a86-167">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="d1a86-168">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="d1a86-168">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="d1a86-169">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="d1a86-169">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="d1a86-170">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="d1a86-170">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="d1a86-171"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="d1a86-171"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="d1a86-172">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d1a86-172">Remarks</span></span>

<span data-ttu-id="d1a86-173">Die **Win32- \_ networkclient** -Klasse wird von [**CIM \_ LogicalElement**](cim-logicalelement.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="d1a86-173">The **Win32\_NetworkClient** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d1a86-174">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d1a86-174">Requirements</span></span>



| <span data-ttu-id="d1a86-175">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d1a86-175">Requirement</span></span> | <span data-ttu-id="d1a86-176">Wert</span><span class="sxs-lookup"><span data-stu-id="d1a86-176">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1a86-177">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d1a86-177">Minimum supported client</span></span><br/> | <span data-ttu-id="d1a86-178">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d1a86-178">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d1a86-179">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d1a86-179">Minimum supported server</span></span><br/> | <span data-ttu-id="d1a86-180">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d1a86-180">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d1a86-181">Namespace</span><span class="sxs-lookup"><span data-stu-id="d1a86-181">Namespace</span></span><br/>                | <span data-ttu-id="d1a86-182">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d1a86-182">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d1a86-183">MOF</span><span class="sxs-lookup"><span data-stu-id="d1a86-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d1a86-184"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="d1a86-184"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d1a86-185">DLL</span><span class="sxs-lookup"><span data-stu-id="d1a86-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1a86-186"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1a86-186"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1a86-187">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d1a86-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1a86-188">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="d1a86-188">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="d1a86-189">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="d1a86-189">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
