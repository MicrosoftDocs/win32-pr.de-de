---
title: Win32_TSLegacyPlugin-Klasse
description: Stellt einen Remotedesktop Server dar, der von den integrierten RemoteApp-und Desktopverbindungsverwaltung Dienst-Plug-Ins für RemoteApp-Programme abgefragt wird.
ms.assetid: 99bec477-ae9d-4bc9-bf9d-11a4e439306b
ms.tgt_platform: multiple
keywords:
- Win32_TSLegacyPlugin-Klasse Remotedesktopdienste
- Win32_TSLegacyPlugin Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TSLegacyPlugin
- Win32_TSLegacyPlugin.Caption
- Win32_TSLegacyPlugin.Description
- Win32_TSLegacyPlugin.InstallDate
- Win32_TSLegacyPlugin.Name
- Win32_TSLegacyPlugin.Status
- Win32_TSLegacyPlugin.Type
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 548eadac272f6f87daf1c43020cb65485e434aec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338711"
---
# <a name="win32_tslegacyplugin-class"></a><span data-ttu-id="8f608-105">Win32- \_ Klasse "slegacyplugin"</span><span class="sxs-lookup"><span data-stu-id="8f608-105">Win32\_TSLegacyPlugin class</span></span>

<span data-ttu-id="8f608-106">Stellt einen Remotedesktop Server dar, der von den integrierten RemoteApp-und Desktopverbindungsverwaltung Dienst-Plug-Ins für RemoteApp-Programme abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="8f608-106">Represents a Remote Desktop server that the built-in RemoteApp and Desktop Connection Management Service plug-ins will query for RemoteApp programs.</span></span>

<span data-ttu-id="8f608-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8f608-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

<span data-ttu-id="8f608-108">Diese Klasse ist ab Windows Server 2012 veraltet.</span><span class="sxs-lookup"><span data-stu-id="8f608-108">This class is deprecated beginning with Windows Server 2012.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f608-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="8f608-109">Syntax</span></span>

``` syntax
[DEPRECATED, dynamic, provider("Win32_TSCentralPublisher_Prov")]
class Win32_TSLegacyPlugin : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  sint32   Type;
};
```

## <a name="members"></a><span data-ttu-id="8f608-110">Member</span><span class="sxs-lookup"><span data-stu-id="8f608-110">Members</span></span>

<span data-ttu-id="8f608-111">Die Win32-Klasse " **\_ zlegacyplugin** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="8f608-111">The **Win32\_TSLegacyPlugin** class has these types of members:</span></span>

-   [<span data-ttu-id="8f608-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8f608-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8f608-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8f608-113">Properties</span></span>

<span data-ttu-id="8f608-114">Die Win32-Klasse " **\_ slegacyplugin** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8f608-114">The **Win32\_TSLegacyPlugin** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8f608-115">**Caption**</span><span class="sxs-lookup"><span data-stu-id="8f608-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f608-116">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8f608-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f608-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f608-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f608-118">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="8f608-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="8f608-119">Kurze Beschreibung (einzeilige Zeichenfolge) des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="8f608-119">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="8f608-120">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8f608-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f608-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8f608-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f608-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8f608-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f608-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f608-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f608-124">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="8f608-124">Description of the object.</span></span>

<span data-ttu-id="8f608-125">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8f608-125">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f608-126">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8f608-126">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f608-127">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="8f608-127">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8f608-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f608-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f608-129">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="8f608-129">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="8f608-130">Das Datum, an dem das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="8f608-130">The date the object was installed.</span></span> <span data-ttu-id="8f608-131">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="8f608-131">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="8f608-132">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8f608-132">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f608-133">**Name**</span><span class="sxs-lookup"><span data-stu-id="8f608-133">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f608-134">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8f608-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f608-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f608-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f608-136">Der Name des Objekts.</span><span class="sxs-lookup"><span data-stu-id="8f608-136">The name of the object.</span></span>

<span data-ttu-id="8f608-137">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8f608-137">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f608-138">**Status**</span><span class="sxs-lookup"><span data-stu-id="8f608-138">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f608-139">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8f608-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f608-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8f608-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f608-141">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="8f608-141">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="8f608-142">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="8f608-142">Current status of the object.</span></span> <span data-ttu-id="8f608-143">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="8f608-143">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="8f608-144">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="8f608-144">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="8f608-145">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="8f608-145">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="8f608-146">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="8f608-146">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="8f608-147">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="8f608-147">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="8f608-148">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="8f608-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="8f608-149">("OK")</span><span class="sxs-lookup"><span data-stu-id="8f608-149">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8f608-150">("Fehler")</span><span class="sxs-lookup"><span data-stu-id="8f608-150">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8f608-151">("Heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="8f608-151">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8f608-152">("Unbekannt")</span><span class="sxs-lookup"><span data-stu-id="8f608-152">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8f608-153">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="8f608-153">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8f608-154">("Wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="8f608-154">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8f608-155">("Wird beendet")</span><span class="sxs-lookup"><span data-stu-id="8f608-155">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8f608-156">("Dienst")</span><span class="sxs-lookup"><span data-stu-id="8f608-156">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8f608-157">**Type**</span><span class="sxs-lookup"><span data-stu-id="8f608-157">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f608-158">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8f608-158">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f608-159">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8f608-159">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8f608-160">Der Typ des Remotedesktopdienste Servers.</span><span class="sxs-lookup"><span data-stu-id="8f608-160">The type of the Remote Desktop Services server.</span></span>

<dt>

<span id="Terminal_Server_0_"></span><span id="terminal_server_0_"></span><span id="TERMINAL_SERVER_0_"></span>

<span data-ttu-id="8f608-161"><span id="Terminal_Server_0_"></span><span id="terminal_server_0_"></span><span id="TERMINAL_SERVER_0_"></span>**Terminal Server (0)** (0)</span><span class="sxs-lookup"><span data-stu-id="8f608-161"><span id="Terminal_Server_0_"></span><span id="terminal_server_0_"></span><span id="TERMINAL_SERVER_0_"></span>**Terminal Server(0)** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8f608-162">Remotedesktop Server.</span><span class="sxs-lookup"><span data-stu-id="8f608-162">Remote Desktop server.</span></span>

</dd> <dt>

<span id="Dummy_Terminal_Server_for_VM_Farm_1_"></span><span id="dummy_terminal_server_for_vm_farm_1_"></span><span id="DUMMY_TERMINAL_SERVER_FOR_VM_FARM_1_"></span>

<span data-ttu-id="8f608-163"><span id="Dummy_Terminal_Server_for_VM_Farm_1_"></span><span id="dummy_terminal_server_for_vm_farm_1_"></span><span id="DUMMY_TERMINAL_SERVER_FOR_VM_FARM_1_"></span>**Dummy-Terminal Server für VM-Farm (1** ) (1)</span><span class="sxs-lookup"><span data-stu-id="8f608-163"><span id="Dummy_Terminal_Server_for_VM_Farm_1_"></span><span id="dummy_terminal_server_for_vm_farm_1_"></span><span id="DUMMY_TERMINAL_SERVER_FOR_VM_FARM_1_"></span>**Dummy Terminal Server for VM Farm(1)** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8f608-164">Künstliche Remotedesktop Server für eine VM-Farm.</span><span class="sxs-lookup"><span data-stu-id="8f608-164">Artificial Remote Desktop server for a VM farm.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8f608-165">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8f608-165">Requirements</span></span>



| <span data-ttu-id="8f608-166">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8f608-166">Requirement</span></span> | <span data-ttu-id="8f608-167">Wert</span><span class="sxs-lookup"><span data-stu-id="8f608-167">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f608-168">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8f608-168">Minimum supported client</span></span><br/> | <span data-ttu-id="8f608-169">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="8f608-169">None supported</span></span><br/>                                                                |
| <span data-ttu-id="8f608-170">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8f608-170">Minimum supported server</span></span><br/> | <span data-ttu-id="8f608-171">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8f608-171">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="8f608-172">Namespace</span><span class="sxs-lookup"><span data-stu-id="8f608-172">Namespace</span></span><br/>                | <span data-ttu-id="8f608-173">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="8f608-173">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="8f608-174">MOF</span><span class="sxs-lookup"><span data-stu-id="8f608-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8f608-175"><dt>Tscpub. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8f608-175"><dt>TscPub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="8f608-176">DLL</span><span class="sxs-lookup"><span data-stu-id="8f608-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f608-177"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f608-177"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

