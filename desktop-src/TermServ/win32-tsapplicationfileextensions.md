---
title: Win32_TSApplicationFileExtensions-Klasse
description: Die Dateinamen Erweiterungen, die von einer Anwendung auf einem Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server behandelt werden.
ms.assetid: beefc266-5ad6-49ee-b761-98764e2905d6
ms.tgt_platform: multiple
keywords:
- Win32_TSApplicationFileExtensions-Klasse Remotedesktopdienste
- Win32_TSApplicationFileExtensions Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TSApplicationFileExtensions
- Win32_TSApplicationFileExtensions.Caption
- Win32_TSApplicationFileExtensions.Description
- Win32_TSApplicationFileExtensions.InstallDate
- Win32_TSApplicationFileExtensions.Name
- Win32_TSApplicationFileExtensions.Status
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e28f84ff122b77abf1474b5686edab627177424b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339589"
---
# <a name="win32_tsapplicationfileextensions-class"></a><span data-ttu-id="f1365-105">Win32- \_ Klasse "tyapplicationfileextensions"</span><span class="sxs-lookup"><span data-stu-id="f1365-105">Win32\_TSApplicationFileExtensions class</span></span>

<span data-ttu-id="f1365-106">Beschreibt die Dateinamen Erweiterungen, die von einer Anwendung auf einem Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="f1365-106">Describes the file name extensions that are handled by an application on a Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1365-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1365-107">Syntax</span></span>

``` syntax
class Win32_TSApplicationFileExtensions : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="f1365-108">Member</span><span class="sxs-lookup"><span data-stu-id="f1365-108">Members</span></span>

<span data-ttu-id="f1365-109">Die Win32-Klasse " **\_ tyapplicationfileextensions** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f1365-109">The **Win32\_TSApplicationFileExtensions** class has these types of members:</span></span>

-   [<span data-ttu-id="f1365-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="f1365-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="f1365-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f1365-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f1365-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="f1365-112">Methods</span></span>

<span data-ttu-id="f1365-113">Die Win32-Klasse " **\_ zapplicationfileextensions** " verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="f1365-113">The **Win32\_TSApplicationFileExtensions** class has these methods.</span></span>



| <span data-ttu-id="f1365-114">Methode</span><span class="sxs-lookup"><span data-stu-id="f1365-114">Method</span></span>                                                                         | <span data-ttu-id="f1365-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f1365-115">Description</span></span>                                                                                |
|:-------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f1365-116">**Dateizuordnungen**</span><span class="sxs-lookup"><span data-stu-id="f1365-116">**FileAssociations**</span></span>](fileassociations-win32-tsapplicationfileextensions.md) | <span data-ttu-id="f1365-117">Scannt die Registrierung, um die aktuellen Dateizuordnungen für eine Anwendung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f1365-117">Scans the registry to get the current file associations for an application.</span></span><br/>     |
| [<span data-ttu-id="f1365-118">**Dateierweiterungen**</span><span class="sxs-lookup"><span data-stu-id="f1365-118">**FileExtensions**</span></span>](fileextensions-win32-tsapplicationfileextensions.md)     | <span data-ttu-id="f1365-119">Stellt eine Liste der Dateinamen Erweiterungen bereit, die von einer Anwendung behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="f1365-119">Provides a list of the file name extensions that are handled by an application.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="f1365-120">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f1365-120">Properties</span></span>

<span data-ttu-id="f1365-121">Die Win32-Klasse " **\_ tyapplicationfileextensions** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f1365-121">The **Win32\_TSApplicationFileExtensions** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f1365-122">**Caption**</span><span class="sxs-lookup"><span data-stu-id="f1365-122">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1365-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f1365-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1365-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f1365-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1365-125">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="f1365-125">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f1365-126">Kurze Beschreibung (einzeilige Zeichenfolge) des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="f1365-126">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="f1365-127">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f1365-127">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1365-128">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f1365-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1365-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f1365-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1365-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f1365-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1365-131">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="f1365-131">Description of the object.</span></span>

<span data-ttu-id="f1365-132">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f1365-132">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1365-133">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f1365-133">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1365-134">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="f1365-134">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f1365-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f1365-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1365-136">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="f1365-136">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="f1365-137">Das Datum, an dem das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="f1365-137">The date the object was installed.</span></span> <span data-ttu-id="f1365-138">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="f1365-138">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="f1365-139">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f1365-139">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1365-140">**Name**</span><span class="sxs-lookup"><span data-stu-id="f1365-140">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1365-141">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f1365-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1365-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f1365-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1365-143">Der Name des Objekts.</span><span class="sxs-lookup"><span data-stu-id="f1365-143">The name of the object.</span></span>

<span data-ttu-id="f1365-144">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f1365-144">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1365-145">**Status**</span><span class="sxs-lookup"><span data-stu-id="f1365-145">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1365-146">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f1365-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1365-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f1365-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1365-148">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="f1365-148">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="f1365-149">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="f1365-149">Current status of the object.</span></span> <span data-ttu-id="f1365-150">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="f1365-150">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="f1365-151">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="f1365-151">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="f1365-152">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="f1365-152">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="f1365-153">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="f1365-153">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="f1365-154">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="f1365-154">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="f1365-155">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f1365-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="f1365-156">("OK")</span><span class="sxs-lookup"><span data-stu-id="f1365-156">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f1365-157">("Fehler")</span><span class="sxs-lookup"><span data-stu-id="f1365-157">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f1365-158">("Heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="f1365-158">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f1365-159">("Unbekannt")</span><span class="sxs-lookup"><span data-stu-id="f1365-159">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f1365-160">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="f1365-160">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f1365-161">("Wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="f1365-161">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f1365-162">("Wird beendet")</span><span class="sxs-lookup"><span data-stu-id="f1365-162">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f1365-163">("Dienst")</span><span class="sxs-lookup"><span data-stu-id="f1365-163">("Service")</span></span>


<span data-ttu-id="f1365-164"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="f1365-164"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="f1365-165">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f1365-165">Remarks</span></span>

<span data-ttu-id="f1365-166">Zum Herstellen einer Verbindung mit dem \\ root \\ CIMV2 \\ TerminalServices-Namespace muss die Authentifizierungs Ebene den Datenschutz für das Paket enthalten.</span><span class="sxs-lookup"><span data-stu-id="f1365-166">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="f1365-167">Bei C/C++-aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene für den **\_ \_ \_ \_ Pkt- \_ Datenschutz auf RPC-C-Ebene**, die mithilfe der com-Funktion [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) festgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="f1365-167">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, which can be set by using the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM function.</span></span> <span data-ttu-id="f1365-168">Bei Visual Basic-und Skript aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene von **wbemauthenticationlevelpzprivacy** oder "PKTPRIVACY" mit einem Wert von 6.</span><span class="sxs-lookup"><span data-stu-id="f1365-168">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span>

<span data-ttu-id="f1365-169">Im folgenden Visual Basic Scripting Edition (VBScript)-Beispiel wird gezeigt, wie eine Verbindung mit einem Remote Computer mit Paket Datenschutz hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="f1365-169">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="f1365-170">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="f1365-170">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f1365-171">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="f1365-171">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f1365-172">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="f1365-172">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f1365-173">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="f1365-173">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f1365-174">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f1365-174">Requirements</span></span>



| <span data-ttu-id="f1365-175">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f1365-175">Requirement</span></span> | <span data-ttu-id="f1365-176">Wert</span><span class="sxs-lookup"><span data-stu-id="f1365-176">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f1365-177">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f1365-177">Minimum supported client</span></span><br/> | <span data-ttu-id="f1365-178">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f1365-178">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f1365-179">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f1365-179">Minimum supported server</span></span><br/> | <span data-ttu-id="f1365-180">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f1365-180">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f1365-181">Namespace</span><span class="sxs-lookup"><span data-stu-id="f1365-181">Namespace</span></span><br/>                | <span data-ttu-id="f1365-182">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="f1365-182">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="f1365-183">MOF</span><span class="sxs-lookup"><span data-stu-id="f1365-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f1365-184"><dt>Tsallow. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f1365-184"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="f1365-185">DLL</span><span class="sxs-lookup"><span data-stu-id="f1365-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1365-186"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1365-186"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

