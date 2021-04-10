---
title: Win32_TSPublishedApplicationList-Klasse
description: Stellt die Liste der Programme dar, die in der Liste der RemoteApp-Programme auf einem Remotedesktop-Sitzungshost-Server (RD-Sitzungshost) enthalten sind.
ms.assetid: 3dbefe54-8c31-439f-a87a-5148214a07d5
ms.tgt_platform: multiple
keywords:
- Win32_TSPublishedApplicationList-Klasse Remotedesktopdienste
- Win32_TSPublishedApplicationList Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TSPublishedApplicationList
- Win32_TSPublishedApplicationList.Caption
- Win32_TSPublishedApplicationList.Description
- Win32_TSPublishedApplicationList.InstallDate
- Win32_TSPublishedApplicationList.Name
- Win32_TSPublishedApplicationList.Status
- Win32_TSPublishedApplicationList.Disabled
- Win32_TSPublishedApplicationList.PolicySourceDisabled
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1f87a87dc6f95bcdb33c7dbd1364ad6b3114ddf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040475"
---
# <a name="win32_tspublishedapplicationlist-class"></a><span data-ttu-id="21727-105">Win32 \_ tspublishedapplicationlist-Klasse</span><span class="sxs-lookup"><span data-stu-id="21727-105">Win32\_TSPublishedApplicationList class</span></span>

<span data-ttu-id="21727-106">Stellt die Liste der Programme dar, die in der Liste der RemoteApp-Programme auf einem Remotedesktop-Sitzungshost-Server (RD-Sitzungshost) enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="21727-106">Represents the list of programs that are in the RemoteApp Programs list on a Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="21727-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="21727-107">Syntax</span></span>

``` syntax
class Win32_TSPublishedApplicationList : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  boolean  Disabled;
  uint32   PolicySourceDisabled;
};
```

## <a name="members"></a><span data-ttu-id="21727-108">Member</span><span class="sxs-lookup"><span data-stu-id="21727-108">Members</span></span>

<span data-ttu-id="21727-109">Die **Win32 \_ tspublishedapplicationlist** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="21727-109">The **Win32\_TSPublishedApplicationList** class has these types of members:</span></span>

-   [<span data-ttu-id="21727-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="21727-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="21727-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="21727-111">Properties</span></span>

<span data-ttu-id="21727-112">Die **Win32 \_ tspublishedapplicationlist** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="21727-112">The **Win32\_TSPublishedApplicationList** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="21727-113">**Caption**</span><span class="sxs-lookup"><span data-stu-id="21727-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21727-114">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21727-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21727-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21727-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21727-116">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="21727-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="21727-117">Kurze Beschreibung (einzeilige Zeichenfolge) des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="21727-117">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="21727-118">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21727-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="21727-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="21727-119">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21727-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21727-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21727-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21727-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="21727-122">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="21727-122">Description of the object.</span></span>

<span data-ttu-id="21727-123">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21727-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="21727-124">**Deaktiviert**</span><span class="sxs-lookup"><span data-stu-id="21727-124">**Disabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21727-125">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="21727-125">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="21727-126">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="21727-126">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="21727-127">Gibt an, ob der RD-Sitzungshost Server die Programme einschränkt, die ein Benutzer bei der anfänglichen Verbindung mit den Programmen in der RemoteApp-Programmliste starten darf.</span><span class="sxs-lookup"><span data-stu-id="21727-127">Indicates whether the RD Session Host server restricts the programs that a user can start on initial connection to the programs that are in the RemoteApp Programs list.</span></span>

</dd> <dt>

<span data-ttu-id="21727-128">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="21727-128">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21727-129">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="21727-129">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="21727-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21727-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21727-131">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="21727-131">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="21727-132">Das Datum, an dem das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="21727-132">The date the object was installed.</span></span> <span data-ttu-id="21727-133">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="21727-133">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="21727-134">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21727-134">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="21727-135">**Name**</span><span class="sxs-lookup"><span data-stu-id="21727-135">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21727-136">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21727-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21727-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21727-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="21727-138">Der Name des Objekts.</span><span class="sxs-lookup"><span data-stu-id="21727-138">The name of the object.</span></span>

<span data-ttu-id="21727-139">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21727-139">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="21727-140">**Policysourcedeaktiviert**</span><span class="sxs-lookup"><span data-stu-id="21727-140">**PolicySourceDisabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21727-141">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="21727-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="21727-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21727-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="21727-143">Gibt an, wo die **Deaktivierte** Eigenschaft konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="21727-143">Indicates where the **Disabled** property is configured.</span></span> <span data-ttu-id="21727-144">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="21727-144">Possible values include:</span></span>

<dt>

<span data-ttu-id="21727-145">0</span><span class="sxs-lookup"><span data-stu-id="21727-145">0</span></span>
</dt> <dd>

<span data-ttu-id="21727-146">Die Einstellung wird auf dem Server über RemoteApp-Manager oder den RemoteApp-WMI-Anbieter konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="21727-146">The setting is configured on the server through RemoteApp Manager or the RemoteApp WMI provider.</span></span>

</dd> <dt>

<span data-ttu-id="21727-147">1</span><span class="sxs-lookup"><span data-stu-id="21727-147">1</span></span>
</dt> <dd>

<span data-ttu-id="21727-148">Die Einstellung wird durch die Gruppenrichtlinie konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="21727-148">The setting is configured through group policy.</span></span>

</dd> <dt>

<span data-ttu-id="21727-149">2</span><span class="sxs-lookup"><span data-stu-id="21727-149">2</span></span>
</dt> <dd>

<span data-ttu-id="21727-150">Die Einstellung ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="21727-150">The setting is not configured.</span></span> <span data-ttu-id="21727-151">Der Standardwert **false** wird für die **Deaktivierte** Eigenschaft verwendet.</span><span class="sxs-lookup"><span data-stu-id="21727-151">The default value of **FALSE** is used for the **Disabled** property.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="21727-152">**Status**</span><span class="sxs-lookup"><span data-stu-id="21727-152">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21727-153">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="21727-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21727-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="21727-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21727-155">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="21727-155">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="21727-156">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="21727-156">Current status of the object.</span></span> <span data-ttu-id="21727-157">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="21727-157">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="21727-158">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="21727-158">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="21727-159">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="21727-159">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="21727-160">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="21727-160">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="21727-161">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="21727-161">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="21727-162">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="21727-162">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="21727-163">("OK")</span><span class="sxs-lookup"><span data-stu-id="21727-163">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="21727-164">("Fehler")</span><span class="sxs-lookup"><span data-stu-id="21727-164">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="21727-165">("Heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="21727-165">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="21727-166">("Unbekannt")</span><span class="sxs-lookup"><span data-stu-id="21727-166">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="21727-167">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="21727-167">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="21727-168">("Wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="21727-168">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="21727-169">("Wird beendet")</span><span class="sxs-lookup"><span data-stu-id="21727-169">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="21727-170">("Dienst")</span><span class="sxs-lookup"><span data-stu-id="21727-170">("Service")</span></span>


<span data-ttu-id="21727-171"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="21727-171"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="21727-172">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="21727-172">Remarks</span></span>

<span data-ttu-id="21727-173">Sie müssen Mitglied der Gruppe "Administratoren" sein, um Eigenschaften mithilfe dieser Klasse festzulegen.</span><span class="sxs-lookup"><span data-stu-id="21727-173">You must be a member of the Administrators group to set properties by using this class.</span></span>

<span data-ttu-id="21727-174">Durch die **Deaktivierte** Eigenschaft wird nicht verhindert, dass Benutzer nicht aufgelistete Programme remote starten, nachdem Sie mithilfe eines RemoteApp-Programms eine Verbindung mit dem RD-Sitzungshost Server hergestellt haben.</span><span class="sxs-lookup"><span data-stu-id="21727-174">The **Disabled** property does not prevent users from starting unlisted programs remotely after they connect to the RD Session Host server by using a RemoteApp program.</span></span>

<span data-ttu-id="21727-175">Die **Deaktivierte** Eigenschaft wird nur dann auf den Wert 2 festgelegt, wenn der folgende Registrierungs Eintrag fehlt:</span><span class="sxs-lookup"><span data-stu-id="21727-175">The **Disabled** property will be set to a value of 2 only if the following registry entry is missing:</span></span>

<span data-ttu-id="21727-176">**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Terminalserver** \\ **\appallowlist** \\ **fdisabledallowlist**</span><span class="sxs-lookup"><span data-stu-id="21727-176">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WindowsNT**\\**CurrentVersion**\\**TerminalServer**\\**TSAppAllowList**\\**fDisabledAllowList**</span></span>

<span data-ttu-id="21727-177">Zum Herstellen einer Verbindung mit dem \\ root \\ CIMV2 \\ TerminalServices-Namespace muss die Authentifizierungs Ebene den Datenschutz für das Paket enthalten.</span><span class="sxs-lookup"><span data-stu-id="21727-177">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="21727-178">Bei C/C++-aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene für den **\_ \_ \_ \_ Pkt- \_ Datenschutz auf RPC-C-Ebene**, die mithilfe der com-Funktion [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) festgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="21727-178">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, which can be set by using the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM function.</span></span> <span data-ttu-id="21727-179">Bei Visual Basic-und Skript aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene von **wbemauthenticationlevelpzprivacy** oder "PKTPRIVACY" mit einem Wert von 6.</span><span class="sxs-lookup"><span data-stu-id="21727-179">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="21727-180">Im folgenden Visual Basic Scripting Edition (VBScript)-Beispiel wird gezeigt, wie eine Verbindung mit einem Remote Computer mit Paket Datenschutz hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="21727-180">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="21727-181">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="21727-181">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="21727-182">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="21727-182">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="21727-183">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="21727-183">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="21727-184">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="21727-184">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="21727-185">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="21727-185">Requirements</span></span>



| <span data-ttu-id="21727-186">Anforderung</span><span class="sxs-lookup"><span data-stu-id="21727-186">Requirement</span></span> | <span data-ttu-id="21727-187">Wert</span><span class="sxs-lookup"><span data-stu-id="21727-187">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="21727-188">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="21727-188">Minimum supported client</span></span><br/> | <span data-ttu-id="21727-189">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="21727-189">None supported</span></span><br/>                                                               |
| <span data-ttu-id="21727-190">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="21727-190">Minimum supported server</span></span><br/> | <span data-ttu-id="21727-191">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="21727-191">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="21727-192">Namespace</span><span class="sxs-lookup"><span data-stu-id="21727-192">Namespace</span></span><br/>                | <span data-ttu-id="21727-193">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="21727-193">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="21727-194">MOF</span><span class="sxs-lookup"><span data-stu-id="21727-194">MOF</span></span><br/>                      | <dl> <span data-ttu-id="21727-195"><dt>Tsallow. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="21727-195"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="21727-196">DLL</span><span class="sxs-lookup"><span data-stu-id="21727-196">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21727-197"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21727-197"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

