---
title: Win32_TSNetworkAdapterListSetting-Klasse
description: Listet die Netzwerkadapter auf \_ , die auf der Grundlage des angegebenen Terminal Protokolls und der Transportmethode für ein Win32-Terminal konfiguriert werden können.
ms.assetid: affe440a-1a7b-49be-a4aa-d792811c59ea
ms.tgt_platform: multiple
keywords:
- Win32_TSNetworkAdapterListSetting-Klasse Remotedesktopdienste
- Win32_TSNetworkAdapterListSetting Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TSNetworkAdapterListSetting
- Win32_TSNetworkAdapterListSetting.Caption
- Win32_TSNetworkAdapterListSetting.Description
- Win32_TSNetworkAdapterListSetting.InstallDate
- Win32_TSNetworkAdapterListSetting.Name
- Win32_TSNetworkAdapterListSetting.Status
- Win32_TSNetworkAdapterListSetting.TerminalName
- Win32_TSNetworkAdapterListSetting.NetworkAdapterID
- Win32_TSNetworkAdapterListSetting.NetworkAdapterIP
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e8c1ac9466d389924d0717748d7da9ec1f5b55f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339348"
---
# <a name="win32_tsnetworkadapterlistsetting-class"></a><span data-ttu-id="c93d0-105">Win32-Klasse "t \_ Network adapterlistsetting"</span><span class="sxs-lookup"><span data-stu-id="c93d0-105">Win32\_TSNetworkAdapterListSetting class</span></span>

<span data-ttu-id="c93d0-106">Die Win32-Klasse " **\_ tnetworkadapterlistsetting** " listet die Liste der Netzwerkadapter auf, die auf der Grundlage des angegebenen Terminal Protokolls und der Transportmethode für ein [**Win32- \_ Terminal**](win32-terminal.md)konfiguriert werden können.</span><span class="sxs-lookup"><span data-stu-id="c93d0-106">The **Win32\_TSNetworkAdapterListSetting** WMI class enumerates the list of network adapters that can be configured for a [**Win32\_Terminal**](win32-terminal.md), based on the specified terminal protocol and transport method.</span></span>

<span data-ttu-id="c93d0-107">Die folgende Syntax wird aus dem MOF-Code vereinfacht und umfasst alle definierten und geerbten Eigenschaften in alphabetischer Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="c93d0-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c93d0-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c93d0-108">Syntax</span></span>

``` syntax
[dynamic, overwrite, provider("Win32_WIN32_TSNETWORKADAPTERLISTSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSNetworkAdapterListSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  string   NetworkAdapterID;
  string   NetworkAdapterIP;
};
```

## <a name="members"></a><span data-ttu-id="c93d0-109">Member</span><span class="sxs-lookup"><span data-stu-id="c93d0-109">Members</span></span>

<span data-ttu-id="c93d0-110">Die Win32-Klasse "t **\_ Network adapterlistsetting** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c93d0-110">The **Win32\_TSNetworkAdapterListSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="c93d0-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c93d0-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c93d0-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c93d0-112">Properties</span></span>

<span data-ttu-id="c93d0-113">Die Win32-Klasse "t **\_ Network adapterlistsetting** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c93d0-113">The **Win32\_TSNetworkAdapterListSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c93d0-114">**Caption**</span><span class="sxs-lookup"><span data-stu-id="c93d0-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c93d0-115">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c93d0-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c93d0-116">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c93d0-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c93d0-117">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="c93d0-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="c93d0-118">Kurze Beschreibung (einzeilige Zeichenfolge) des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="c93d0-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="c93d0-119">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c93d0-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c93d0-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c93d0-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c93d0-121">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c93d0-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c93d0-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c93d0-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c93d0-123">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="c93d0-123">Description of the object.</span></span>

<span data-ttu-id="c93d0-124">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c93d0-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c93d0-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c93d0-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c93d0-126">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="c93d0-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c93d0-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c93d0-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c93d0-128">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="c93d0-128">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="c93d0-129">Das Datum, an dem das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="c93d0-129">The date the object was installed.</span></span> <span data-ttu-id="c93d0-130">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="c93d0-130">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="c93d0-131">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c93d0-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c93d0-132">**Name**</span><span class="sxs-lookup"><span data-stu-id="c93d0-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c93d0-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c93d0-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c93d0-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c93d0-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c93d0-135">Der Name des Objekts.</span><span class="sxs-lookup"><span data-stu-id="c93d0-135">The name of the object.</span></span>

<span data-ttu-id="c93d0-136">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c93d0-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c93d0-137">**NetworkAdapterID**</span><span class="sxs-lookup"><span data-stu-id="c93d0-137">**NetworkAdapterID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c93d0-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c93d0-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c93d0-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c93d0-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c93d0-140">Die GUID des Netzwerkadapters.</span><span class="sxs-lookup"><span data-stu-id="c93d0-140">The GUID of the network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="c93d0-141">**Network adapterip**</span><span class="sxs-lookup"><span data-stu-id="c93d0-141">**NetworkAdapterIP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c93d0-142">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c93d0-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c93d0-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c93d0-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c93d0-144">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c93d0-144">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c93d0-145">Die IP-Adresse des Netzwerkadapters.</span><span class="sxs-lookup"><span data-stu-id="c93d0-145">The IP address of the network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="c93d0-146">**Status**</span><span class="sxs-lookup"><span data-stu-id="c93d0-146">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c93d0-147">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c93d0-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c93d0-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c93d0-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c93d0-149">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="c93d0-149">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="c93d0-150">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="c93d0-150">Current status of the object.</span></span> <span data-ttu-id="c93d0-151">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="c93d0-151">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="c93d0-152">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="c93d0-152">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="c93d0-153">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="c93d0-153">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="c93d0-154">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="c93d0-154">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="c93d0-155">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="c93d0-155">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="c93d0-156">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c93d0-156">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="c93d0-157">("OK")</span><span class="sxs-lookup"><span data-stu-id="c93d0-157">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c93d0-158">("Fehler")</span><span class="sxs-lookup"><span data-stu-id="c93d0-158">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c93d0-159">("Heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="c93d0-159">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c93d0-160">("Unbekannt")</span><span class="sxs-lookup"><span data-stu-id="c93d0-160">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c93d0-161">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="c93d0-161">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c93d0-162">("Wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="c93d0-162">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c93d0-163">("Wird beendet")</span><span class="sxs-lookup"><span data-stu-id="c93d0-163">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c93d0-164">("Dienst")</span><span class="sxs-lookup"><span data-stu-id="c93d0-164">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c93d0-165">**Terminal Name**</span><span class="sxs-lookup"><span data-stu-id="c93d0-165">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c93d0-166">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c93d0-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c93d0-167">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c93d0-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c93d0-168">Der Name des Terminals.</span><span class="sxs-lookup"><span data-stu-id="c93d0-168">The name of the terminal.</span></span>

<span data-ttu-id="c93d0-169">Diese Eigenschaft wird von [**Win32 \_ TerminalSetting**](win32-terminalsetting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c93d0-169">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c93d0-170">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c93d0-170">Remarks</span></span>

<span data-ttu-id="c93d0-171">Zum Herstellen einer Verbindung mit dem \\ Namespace "root cimv2 \\ TerminalServices" muss die Authentifizierungs Ebene den Datenschutz für das Paket enthalten.</span><span class="sxs-lookup"><span data-stu-id="c93d0-171">To connect to the "Root\\CIMV2\\TerminalServices" namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="c93d0-172">Bei C/C++-aufrufen wäre dies eine Authentifizierungs Ebene der **RPC- \_ c- \_ authn- \_ Ebene \_ Pkt- \_ Datenschutz**.</span><span class="sxs-lookup"><span data-stu-id="c93d0-172">For C/C++ calls, this would be an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="c93d0-173">Bei Visual Basic-und Skript aufrufen wäre dies eine Authentifizierungs Ebene von **wbemauthenticationlevelpktprivacy** oder "PKTPRIVACY" mit einem Wert von 6.</span><span class="sxs-lookup"><span data-stu-id="c93d0-173">For Visual Basic and scripting calls, this would be an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="c93d0-174">Im folgenden Visual Basic Scripting Edition (VBScript)-Beispiel wird gezeigt, wie eine Verbindung mit einem Remote Computer mit Paket Datenschutz hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="c93d0-174">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="c93d0-175">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="c93d0-175">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c93d0-176">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="c93d0-176">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c93d0-177">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c93d0-177">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c93d0-178">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="c93d0-178">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="c93d0-179">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c93d0-179">Requirements</span></span>



| <span data-ttu-id="c93d0-180">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c93d0-180">Requirement</span></span> | <span data-ttu-id="c93d0-181">Wert</span><span class="sxs-lookup"><span data-stu-id="c93d0-181">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c93d0-182">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c93d0-182">Minimum supported client</span></span><br/> | <span data-ttu-id="c93d0-183">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c93d0-183">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c93d0-184">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c93d0-184">Minimum supported server</span></span><br/> | <span data-ttu-id="c93d0-185">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c93d0-185">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c93d0-186">Namespace</span><span class="sxs-lookup"><span data-stu-id="c93d0-186">Namespace</span></span><br/>                | <span data-ttu-id="c93d0-187">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="c93d0-187">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="c93d0-188">MOF</span><span class="sxs-lookup"><span data-stu-id="c93d0-188">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c93d0-189"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c93d0-189"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="c93d0-190">DLL</span><span class="sxs-lookup"><span data-stu-id="c93d0-190">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c93d0-191"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c93d0-191"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c93d0-192">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c93d0-192">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c93d0-193">**Win32 \_ TerminalSetting**</span><span class="sxs-lookup"><span data-stu-id="c93d0-193">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> <dt>

[<span data-ttu-id="c93d0-194">**Win32-Datei "t-Network \_ adaptersetting"**</span><span class="sxs-lookup"><span data-stu-id="c93d0-194">**Win32\_TSNetworkAdapterSetting**</span></span>](win32-tsnetworkadaptersetting.md)
</dt> </dl>

 

