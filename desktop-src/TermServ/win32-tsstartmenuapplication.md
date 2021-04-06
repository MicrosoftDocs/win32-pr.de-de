---
title: Win32_TSStartMenuApplication-Klasse
description: Beschreibt die Anwendungen im Startmenü eines Remotedesktop-Sitzungshost (RD-Sitzungshost)-Servers.
ms.assetid: 88b412b8-139f-4266-b7d8-c34f93940a72
ms.tgt_platform: multiple
keywords:
- Win32_TSStartMenuApplication-Klasse Remotedesktopdienste
- Win32_TSStartMenuApplication Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TSStartMenuApplication
- Win32_TSStartMenuApplication.Caption
- Win32_TSStartMenuApplication.Description
- Win32_TSStartMenuApplication.InstallDate
- Win32_TSStartMenuApplication.Name
- Win32_TSStartMenuApplication.Status
- Win32_TSStartMenuApplication.Path
- Win32_TSStartMenuApplication.VPath
- Win32_TSStartMenuApplication.IconPath
- Win32_TSStartMenuApplication.IconIndex
- Win32_TSStartMenuApplication.CommandLineArguments
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0dae7610381745f6ced2a01e76f8545b33d1205
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743593"
---
# <a name="win32_tsstartmenuapplication-class"></a><span data-ttu-id="5224a-105">Win32- \_ Klasse "ungstartmenuapplication"</span><span class="sxs-lookup"><span data-stu-id="5224a-105">Win32\_TSStartMenuApplication class</span></span>

<span data-ttu-id="5224a-106">Beschreibt die Anwendungen im Startmenü eines Remotedesktop-Sitzungshost (RD-Sitzungshost)-Servers.</span><span class="sxs-lookup"><span data-stu-id="5224a-106">Describes the applications that are on the Start menu of a Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="5224a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5224a-107">Syntax</span></span>

``` syntax
class Win32_TSStartMenuApplication : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   Path;
  string   VPath;
  string   IconPath;
  sint32   IconIndex;
  string   CommandLineArguments;
};
```

## <a name="members"></a><span data-ttu-id="5224a-108">Member</span><span class="sxs-lookup"><span data-stu-id="5224a-108">Members</span></span>

<span data-ttu-id="5224a-109">Die Win32-Klasse " **\_ sestartmenuapplication** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="5224a-109">The **Win32\_TSStartMenuApplication** class has these types of members:</span></span>

-   [<span data-ttu-id="5224a-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5224a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5224a-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5224a-111">Properties</span></span>

<span data-ttu-id="5224a-112">Die Win32-Klasse " **\_ ungstartmenuapplication** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5224a-112">The **Win32\_TSStartMenuApplication** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5224a-113">**Caption**</span><span class="sxs-lookup"><span data-stu-id="5224a-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5224a-114">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5224a-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5224a-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5224a-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5224a-116">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="5224a-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5224a-117">Kurze Beschreibung (einzeilige Zeichenfolge) des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="5224a-117">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="5224a-118">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5224a-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5224a-119">**CommandLineArguments**</span><span class="sxs-lookup"><span data-stu-id="5224a-119">**CommandLineArguments**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5224a-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5224a-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5224a-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5224a-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5224a-122">Die zu verwendenden Befehlszeilenargumente.</span><span class="sxs-lookup"><span data-stu-id="5224a-122">The command-line arguments to use.</span></span>

</dd> <dt>

<span data-ttu-id="5224a-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5224a-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5224a-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5224a-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5224a-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5224a-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5224a-126">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="5224a-126">Description of the object.</span></span>

<span data-ttu-id="5224a-127">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5224a-127">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5224a-128">**IconIndex**</span><span class="sxs-lookup"><span data-stu-id="5224a-128">**IconIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5224a-129">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5224a-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5224a-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5224a-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5224a-131">Der Index oder die ID des Symbols.</span><span class="sxs-lookup"><span data-stu-id="5224a-131">The index or ID of the icon.</span></span>

</dd> <dt>

<span data-ttu-id="5224a-132">**IconPath**</span><span class="sxs-lookup"><span data-stu-id="5224a-132">**IconPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5224a-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5224a-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5224a-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5224a-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5224a-135">Der Pfad des Anwendungs Symbols.</span><span class="sxs-lookup"><span data-stu-id="5224a-135">The path of the application icon.</span></span>

</dd> <dt>

<span data-ttu-id="5224a-136">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5224a-136">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5224a-137">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="5224a-137">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5224a-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5224a-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5224a-139">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="5224a-139">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="5224a-140">Das Datum, an dem das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="5224a-140">The date the object was installed.</span></span> <span data-ttu-id="5224a-141">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="5224a-141">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="5224a-142">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5224a-142">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5224a-143">**Name**</span><span class="sxs-lookup"><span data-stu-id="5224a-143">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5224a-144">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5224a-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5224a-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5224a-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5224a-146">Der Name des Objekts.</span><span class="sxs-lookup"><span data-stu-id="5224a-146">The name of the object.</span></span>

<span data-ttu-id="5224a-147">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5224a-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5224a-148">**Pfad**</span><span class="sxs-lookup"><span data-stu-id="5224a-148">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5224a-149">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5224a-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5224a-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5224a-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5224a-151">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="5224a-151">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="5224a-152">Pfad der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="5224a-152">The path of the application.</span></span>

</dd> <dt>

<span data-ttu-id="5224a-153">**Status**</span><span class="sxs-lookup"><span data-stu-id="5224a-153">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5224a-154">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5224a-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5224a-155">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5224a-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5224a-156">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="5224a-156">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="5224a-157">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="5224a-157">Current status of the object.</span></span> <span data-ttu-id="5224a-158">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="5224a-158">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="5224a-159">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="5224a-159">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="5224a-160">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="5224a-160">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="5224a-161">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="5224a-161">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="5224a-162">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="5224a-162">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="5224a-163">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5224a-163">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="5224a-164">("OK")</span><span class="sxs-lookup"><span data-stu-id="5224a-164">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5224a-165">("Fehler")</span><span class="sxs-lookup"><span data-stu-id="5224a-165">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5224a-166">("Heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="5224a-166">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5224a-167">("Unbekannt")</span><span class="sxs-lookup"><span data-stu-id="5224a-167">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5224a-168">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="5224a-168">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5224a-169">("Wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="5224a-169">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5224a-170">("Wird beendet")</span><span class="sxs-lookup"><span data-stu-id="5224a-170">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5224a-171">("Dienst")</span><span class="sxs-lookup"><span data-stu-id="5224a-171">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5224a-172">**Vpath**</span><span class="sxs-lookup"><span data-stu-id="5224a-172">**VPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5224a-173">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5224a-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5224a-174">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5224a-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5224a-175">Der virtuelle Pfad der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="5224a-175">The virtual path of the application.</span></span> <span data-ttu-id="5224a-176">Dies schließt System Umgebungsvariablen ein, z. b .% windir%.</span><span class="sxs-lookup"><span data-stu-id="5224a-176">This includes system environment variables, such as %windir%.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5224a-177">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5224a-177">Remarks</span></span>

<span data-ttu-id="5224a-178">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Klasse verwenden zu können.</span><span class="sxs-lookup"><span data-stu-id="5224a-178">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="5224a-179">Zum Herstellen einer Verbindung mit dem \\ root \\ CIMV2 \\ TerminalServices-Namespace muss die Authentifizierungs Ebene den Datenschutz für das Paket enthalten.</span><span class="sxs-lookup"><span data-stu-id="5224a-179">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="5224a-180">Bei C/C++-aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene für den **\_ \_ \_ \_ Pkt- \_ Datenschutz auf RPC-C-Ebene**, die mithilfe der com-Funktion [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) festgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="5224a-180">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, which can be set by using the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM function.</span></span> <span data-ttu-id="5224a-181">Bei Visual Basic-und Skript aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene von **wbemauthenticationlevelpzprivacy** oder "PKTPRIVACY" mit einem Wert von 6.</span><span class="sxs-lookup"><span data-stu-id="5224a-181">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="5224a-182">Im folgenden Visual Basic Scripting Edition (VBScript)-Beispiel wird gezeigt, wie eine Verbindung mit einem Remote Computer mit Paket Datenschutz hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="5224a-182">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="5224a-183">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="5224a-183">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5224a-184">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="5224a-184">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="5224a-185">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="5224a-185">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5224a-186">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="5224a-186">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="5224a-187">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5224a-187">Requirements</span></span>



| <span data-ttu-id="5224a-188">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5224a-188">Requirement</span></span> | <span data-ttu-id="5224a-189">Wert</span><span class="sxs-lookup"><span data-stu-id="5224a-189">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5224a-190">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5224a-190">Minimum supported client</span></span><br/> | <span data-ttu-id="5224a-191">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="5224a-191">None supported</span></span><br/>                                                               |
| <span data-ttu-id="5224a-192">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5224a-192">Minimum supported server</span></span><br/> | <span data-ttu-id="5224a-193">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5224a-193">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5224a-194">Namespace</span><span class="sxs-lookup"><span data-stu-id="5224a-194">Namespace</span></span><br/>                | <span data-ttu-id="5224a-195">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="5224a-195">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="5224a-196">MOF</span><span class="sxs-lookup"><span data-stu-id="5224a-196">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5224a-197"><dt>Tsallow. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5224a-197"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="5224a-198">DLL</span><span class="sxs-lookup"><span data-stu-id="5224a-198">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5224a-199"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5224a-199"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

