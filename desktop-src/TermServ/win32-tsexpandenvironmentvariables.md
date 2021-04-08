---
title: Win32_TSExpandEnvironmentVariables-Klasse
description: Erweitert System definierte Umgebungsvariablen. | Win32_TSExpandEnvironmentVariables-Klasse
ms.assetid: f79d4fa2-1a6e-4a2f-a637-b62f05cfd2ad
ms.tgt_platform: multiple
keywords:
- Win32_TSExpandEnvironmentVariables-Klasse Remotedesktopdienste
- Win32_TSExpandEnvironmentVariables Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TSExpandEnvironmentVariables
- Win32_TSExpandEnvironmentVariables.Caption
- Win32_TSExpandEnvironmentVariables.Description
- Win32_TSExpandEnvironmentVariables.InstallDate
- Win32_TSExpandEnvironmentVariables.Name
- Win32_TSExpandEnvironmentVariables.Status
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3d6bbd1a4167de703204fcf5abe345fd1bb216c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103869907"
---
# <a name="win32_tsexpandenvironmentvariables-class"></a><span data-ttu-id="680dc-106">Win32- \_ Klasse "tsexpandumgebdie Variables"</span><span class="sxs-lookup"><span data-stu-id="680dc-106">Win32\_TSExpandEnvironmentVariables class</span></span>

<span data-ttu-id="680dc-107">Erweitert System definierte Umgebungsvariablen.</span><span class="sxs-lookup"><span data-stu-id="680dc-107">Expands system-defined environment variables.</span></span>

## <a name="syntax"></a><span data-ttu-id="680dc-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="680dc-108">Syntax</span></span>

``` syntax
class Win32_TSExpandEnvironmentVariables : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="680dc-109">Member</span><span class="sxs-lookup"><span data-stu-id="680dc-109">Members</span></span>

<span data-ttu-id="680dc-110">Die Win32-Klasse " **\_ tsexpandumgebungsvariables** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="680dc-110">The **Win32\_TSExpandEnvironmentVariables** class has these types of members:</span></span>

-   [<span data-ttu-id="680dc-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="680dc-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="680dc-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="680dc-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="680dc-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="680dc-113">Methods</span></span>

<span data-ttu-id="680dc-114">Die **Win32-Klasse \_ tsexpandumgebungsvariables** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="680dc-114">The **Win32\_TSExpandEnvironmentVariables** class has these methods.</span></span>



| <span data-ttu-id="680dc-115">Methode</span><span class="sxs-lookup"><span data-stu-id="680dc-115">Method</span></span>                                                                                  | <span data-ttu-id="680dc-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="680dc-116">Description</span></span>                                              |
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------|
| [<span data-ttu-id="680dc-117">**EnvironmentVariables**</span><span class="sxs-lookup"><span data-stu-id="680dc-117">**EnvironmentVariables**</span></span>](environmentvariables-win32-tsexpandenvironmentvariables.md) | <span data-ttu-id="680dc-118">Erweitert System definierte Umgebungsvariablen.</span><span class="sxs-lookup"><span data-stu-id="680dc-118">Expands system-defined environment variables.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="680dc-119">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="680dc-119">Properties</span></span>

<span data-ttu-id="680dc-120">Die Win32-Klasse " **\_ tsexpandumgebungs variables** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="680dc-120">The **Win32\_TSExpandEnvironmentVariables** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="680dc-121">**Caption**</span><span class="sxs-lookup"><span data-stu-id="680dc-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="680dc-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="680dc-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="680dc-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="680dc-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="680dc-124">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="680dc-124">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="680dc-125">Kurze Beschreibung (einzeilige Zeichenfolge) des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="680dc-125">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="680dc-126">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="680dc-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="680dc-127">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="680dc-127">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="680dc-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="680dc-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="680dc-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="680dc-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="680dc-130">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="680dc-130">Description of the object.</span></span>

<span data-ttu-id="680dc-131">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="680dc-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="680dc-132">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="680dc-132">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="680dc-133">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="680dc-133">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="680dc-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="680dc-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="680dc-135">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="680dc-135">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="680dc-136">Das Datum, an dem das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="680dc-136">The date the object was installed.</span></span> <span data-ttu-id="680dc-137">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="680dc-137">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="680dc-138">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="680dc-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="680dc-139">**Name**</span><span class="sxs-lookup"><span data-stu-id="680dc-139">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="680dc-140">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="680dc-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="680dc-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="680dc-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="680dc-142">Der Name des Objekts.</span><span class="sxs-lookup"><span data-stu-id="680dc-142">The name of the object.</span></span>

<span data-ttu-id="680dc-143">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="680dc-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="680dc-144">**Status**</span><span class="sxs-lookup"><span data-stu-id="680dc-144">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="680dc-145">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="680dc-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="680dc-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="680dc-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="680dc-147">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="680dc-147">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="680dc-148">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="680dc-148">Current status of the object.</span></span> <span data-ttu-id="680dc-149">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="680dc-149">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="680dc-150">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="680dc-150">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="680dc-151">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="680dc-151">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="680dc-152">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="680dc-152">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="680dc-153">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="680dc-153">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="680dc-154">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="680dc-154">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="680dc-155">("OK")</span><span class="sxs-lookup"><span data-stu-id="680dc-155">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="680dc-156">("Fehler")</span><span class="sxs-lookup"><span data-stu-id="680dc-156">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="680dc-157">("Heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="680dc-157">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="680dc-158">("Unbekannt")</span><span class="sxs-lookup"><span data-stu-id="680dc-158">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="680dc-159">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="680dc-159">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="680dc-160">("Wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="680dc-160">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="680dc-161">("Wird beendet")</span><span class="sxs-lookup"><span data-stu-id="680dc-161">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="680dc-162">("Dienst")</span><span class="sxs-lookup"><span data-stu-id="680dc-162">("Service")</span></span>


<span data-ttu-id="680dc-163"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="680dc-163"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="680dc-164">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="680dc-164">Remarks</span></span>

<span data-ttu-id="680dc-165">Zum Herstellen einer Verbindung mit dem \\ root \\ CIMV2 \\ TerminalServices-Namespace muss die Authentifizierungs Ebene den Datenschutz für das Paket enthalten.</span><span class="sxs-lookup"><span data-stu-id="680dc-165">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="680dc-166">Bei C/C++-aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene für den **\_ \_ \_ \_ Pkt- \_ Datenschutz auf RPC-C-Ebene**, die mithilfe der com-Funktion [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) festgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="680dc-166">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, which can be set by using the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM function.</span></span> <span data-ttu-id="680dc-167">Bei Visual Basic-und Skript aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene von **wbemauthenticationlevelpzprivacy** oder "PKTPRIVACY" mit einem Wert von 6.</span><span class="sxs-lookup"><span data-stu-id="680dc-167">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="680dc-168">Im folgenden Visual Basic Scripting Edition (VBScript)-Beispiel wird gezeigt, wie eine Verbindung mit einem Remote Computer mit Paket Datenschutz hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="680dc-168">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="680dc-169">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="680dc-169">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="680dc-170">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="680dc-170">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="680dc-171">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="680dc-171">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="680dc-172">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="680dc-172">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="680dc-173">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="680dc-173">Requirements</span></span>



| <span data-ttu-id="680dc-174">Anforderung</span><span class="sxs-lookup"><span data-stu-id="680dc-174">Requirement</span></span> | <span data-ttu-id="680dc-175">Wert</span><span class="sxs-lookup"><span data-stu-id="680dc-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="680dc-176">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="680dc-176">Minimum supported client</span></span><br/> | <span data-ttu-id="680dc-177">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="680dc-177">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="680dc-178">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="680dc-178">Minimum supported server</span></span><br/> | <span data-ttu-id="680dc-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="680dc-179">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="680dc-180">Namespace</span><span class="sxs-lookup"><span data-stu-id="680dc-180">Namespace</span></span><br/>                | <span data-ttu-id="680dc-181">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="680dc-181">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="680dc-182">MOF</span><span class="sxs-lookup"><span data-stu-id="680dc-182">MOF</span></span><br/>                      | <dl> <span data-ttu-id="680dc-183"><dt>Tsallow. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="680dc-183"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="680dc-184">DLL</span><span class="sxs-lookup"><span data-stu-id="680dc-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="680dc-185"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="680dc-185"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

