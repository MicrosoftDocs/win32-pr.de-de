---
title: Win32_TSPermissionsSetting-Klasse
description: Enthält eine Methode zum Hinzufügen neuer Konten zum Terminal und eine Methode zum Wiederherstellen der Standard Berechtigungen für ein Terminal.
ms.assetid: ebc6e96a-668e-44aa-b589-c3e476fb3029
ms.tgt_platform: multiple
keywords:
- Win32_TSPermissionsSetting-Klasse Remotedesktopdienste
- Win32_TSPermissionsSetting Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TSPermissionsSetting
- Win32_TSPermissionsSetting.Caption
- Win32_TSPermissionsSetting.Description
- Win32_TSPermissionsSetting.InstallDate
- Win32_TSPermissionsSetting.Name
- Win32_TSPermissionsSetting.Status
- Win32_TSPermissionsSetting.TerminalName
- Win32_TSPermissionsSetting.DenyAdminPermissionForCustomization
- Win32_TSPermissionsSetting.PolicySourceDenyAdminPermissionForCustomization
- Win32_TSPermissionsSetting.StringSecurityDescriptor
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 877b8373667bf01010ceb63c0ec35e46db48f702
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343473"
---
# <a name="win32_tspermissionssetting-class"></a><span data-ttu-id="60d3b-105">Win32 \_ tspermissionssetting-Klasse</span><span class="sxs-lookup"><span data-stu-id="60d3b-105">Win32\_TSPermissionsSetting class</span></span>

<span data-ttu-id="60d3b-106">Die **Win32 \_ tspermissionssetting** -WMI-Klasse enthält eine Methode zum Hinzufügen neuer Konten zum Terminal und eine Methode zum Wiederherstellen der Standard Berechtigungen für ein Terminal.</span><span class="sxs-lookup"><span data-stu-id="60d3b-106">The **Win32\_TSPermissionsSetting** WMI class includes a method to add new accounts to the terminal and a method to restore the default permissions to a terminal.</span></span>

<span data-ttu-id="60d3b-107">Die folgende Syntax wird aus dem MOF-Code vereinfacht und umfasst alle definierten und geerbten Eigenschaften in alphabetischer Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="60d3b-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="60d3b-108">Referenzinformationen zu-Methoden finden Sie in der Tabelle mit den Methoden weiter unten in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="60d3b-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="60d3b-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="60d3b-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSPERMISSIONSSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSPermissionsSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  uint32   DenyAdminPermissionForCustomization;
  uint32   PolicySourceDenyAdminPermissionForCustomization;
  string   StringSecurityDescriptor;
};
```

## <a name="members"></a><span data-ttu-id="60d3b-110">Member</span><span class="sxs-lookup"><span data-stu-id="60d3b-110">Members</span></span>

<span data-ttu-id="60d3b-111">Die **Win32 \_ tspermissionssetting** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="60d3b-111">The **Win32\_TSPermissionsSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="60d3b-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="60d3b-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="60d3b-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="60d3b-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="60d3b-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="60d3b-114">Methods</span></span>

<span data-ttu-id="60d3b-115">Die **Win32 \_ tspermissionssetting** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="60d3b-115">The **Win32\_TSPermissionsSetting** class has these methods.</span></span>



| <span data-ttu-id="60d3b-116">Methode</span><span class="sxs-lookup"><span data-stu-id="60d3b-116">Method</span></span>                                                                | <span data-ttu-id="60d3b-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="60d3b-117">Description</span></span>                                                                                                                    |
|:----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="60d3b-118">**Addaccount**</span><span class="sxs-lookup"><span data-stu-id="60d3b-118">**AddAccount**</span></span>](win32-tspermissionssetting-addaccount.md)           | <span data-ttu-id="60d3b-119">Fügt dem Terminal ein Konto mit dem Berechtigungs Satz hinzu, der im Wert des *permissionvoreinstellung* -Parameters angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="60d3b-119">Adds an account to the terminal with the permission set specified in the value of the *PermissionPreSet* parameter.</span></span><br/> |
| [<span data-ttu-id="60d3b-120">**Restoredefaults**</span><span class="sxs-lookup"><span data-stu-id="60d3b-120">**RestoreDefaults**</span></span>](win32-tspermissionssetting-restoredefaults.md) | <span data-ttu-id="60d3b-121">Stellt die standardmäßigen Berechtigungs Satz Werte für das Terminal wieder her.</span><span class="sxs-lookup"><span data-stu-id="60d3b-121">Restores the default permission set values for the terminal.</span></span><br/>                                                        |



 

### <a name="properties"></a><span data-ttu-id="60d3b-122">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="60d3b-122">Properties</span></span>

<span data-ttu-id="60d3b-123">Die **Win32 \_ tspermissionssetting** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="60d3b-123">The **Win32\_TSPermissionsSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="60d3b-124">**Caption**</span><span class="sxs-lookup"><span data-stu-id="60d3b-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60d3b-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60d3b-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60d3b-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60d3b-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60d3b-127">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="60d3b-127">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="60d3b-128">Kurze Beschreibung (einzeilige Zeichenfolge) des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="60d3b-128">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="60d3b-129">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60d3b-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="60d3b-130">**Denyadminpermissionforanpassung**</span><span class="sxs-lookup"><span data-stu-id="60d3b-130">**DenyAdminPermissionForCustomization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60d3b-131">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="60d3b-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="60d3b-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60d3b-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60d3b-133">Gibt an, ob der lokale Administrator die Berechtigung zum Anpassen hat.</span><span class="sxs-lookup"><span data-stu-id="60d3b-133">Specifies whether local administrator has permission to customize.</span></span>

</dd> <dt>

<span data-ttu-id="60d3b-134">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="60d3b-134">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60d3b-135">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60d3b-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60d3b-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60d3b-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60d3b-137">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="60d3b-137">Description of the object.</span></span>

<span data-ttu-id="60d3b-138">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60d3b-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="60d3b-139">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="60d3b-139">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60d3b-140">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="60d3b-140">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="60d3b-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60d3b-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60d3b-142">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="60d3b-142">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="60d3b-143">Das Datum, an dem das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="60d3b-143">The date the object was installed.</span></span> <span data-ttu-id="60d3b-144">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="60d3b-144">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="60d3b-145">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60d3b-145">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="60d3b-146">**Name**</span><span class="sxs-lookup"><span data-stu-id="60d3b-146">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60d3b-147">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60d3b-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60d3b-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60d3b-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60d3b-149">Der Name des Objekts.</span><span class="sxs-lookup"><span data-stu-id="60d3b-149">The name of the object.</span></span>

<span data-ttu-id="60d3b-150">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60d3b-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="60d3b-151">**Policysourcedenyadminpermissionforanpassung**</span><span class="sxs-lookup"><span data-stu-id="60d3b-151">**PolicySourceDenyAdminPermissionForCustomization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60d3b-152">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="60d3b-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="60d3b-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60d3b-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60d3b-154">Gibt an, ob die **minverschlüsseltionlevel** -Eigenschaft vom Server, von der Gruppenrichtlinie oder standardmäßig konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="60d3b-154">Indicates whether the **MinEncryptionLevel** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="60d3b-155">0</span><span class="sxs-lookup"><span data-stu-id="60d3b-155">0</span></span>
</dt> <dd>

<span data-ttu-id="60d3b-156">Server</span><span class="sxs-lookup"><span data-stu-id="60d3b-156">Server</span></span>

</dd> <dt>

<span data-ttu-id="60d3b-157">1</span><span class="sxs-lookup"><span data-stu-id="60d3b-157">1</span></span>
</dt> <dd>

<span data-ttu-id="60d3b-158">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="60d3b-158">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="60d3b-159">**Status**</span><span class="sxs-lookup"><span data-stu-id="60d3b-159">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60d3b-160">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60d3b-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60d3b-161">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60d3b-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60d3b-162">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="60d3b-162">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="60d3b-163">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="60d3b-163">Current status of the object.</span></span> <span data-ttu-id="60d3b-164">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="60d3b-164">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="60d3b-165">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="60d3b-165">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="60d3b-166">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="60d3b-166">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="60d3b-167">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="60d3b-167">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="60d3b-168">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="60d3b-168">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="60d3b-169">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60d3b-169">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="60d3b-170">("OK")</span><span class="sxs-lookup"><span data-stu-id="60d3b-170">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="60d3b-171">("Fehler")</span><span class="sxs-lookup"><span data-stu-id="60d3b-171">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="60d3b-172">("Heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="60d3b-172">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="60d3b-173">("Unbekannt")</span><span class="sxs-lookup"><span data-stu-id="60d3b-173">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="60d3b-174">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="60d3b-174">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="60d3b-175">("Wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="60d3b-175">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="60d3b-176">("Wird beendet")</span><span class="sxs-lookup"><span data-stu-id="60d3b-176">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="60d3b-177">("Dienst")</span><span class="sxs-lookup"><span data-stu-id="60d3b-177">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="60d3b-178">**Stringsecuritydescriptor**</span><span class="sxs-lookup"><span data-stu-id="60d3b-178">**StringSecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60d3b-179">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60d3b-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60d3b-180">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="60d3b-180">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="60d3b-181">Dem Terminal zugeordneter Sicherheits Deskriptor im Format des binären Byte Arrays.</span><span class="sxs-lookup"><span data-stu-id="60d3b-181">Security descriptor associated with the terminal in binary byte array format.</span></span>

</dd> <dt>

<span data-ttu-id="60d3b-182">**Terminal Name**</span><span class="sxs-lookup"><span data-stu-id="60d3b-182">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60d3b-183">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60d3b-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60d3b-184">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60d3b-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60d3b-185">Der Name des Terminals.</span><span class="sxs-lookup"><span data-stu-id="60d3b-185">The name of the terminal.</span></span>

<span data-ttu-id="60d3b-186">Diese Eigenschaft wird von [**Win32 \_ TerminalSetting**](win32-terminalsetting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60d3b-186">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="60d3b-187">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="60d3b-187">Remarks</span></span>

<span data-ttu-id="60d3b-188">Zum Herstellen einer Verbindung mit dem \\ root \\ CIMV2 \\ TerminalServices-Namespace muss die Authentifizierungs Ebene den Datenschutz für das Paket enthalten.</span><span class="sxs-lookup"><span data-stu-id="60d3b-188">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="60d3b-189">Bei C/C++-aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene der **RPC- \_ c- \_ authn- \_ Ebene \_ Pkt \_ Privacy**.</span><span class="sxs-lookup"><span data-stu-id="60d3b-189">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="60d3b-190">Bei Visual Basic-und Skript aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene von **wbemauthenticationlevelpzprivacy** oder "PKTPRIVACY" mit einem Wert von 6.</span><span class="sxs-lookup"><span data-stu-id="60d3b-190">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="60d3b-191">Im folgenden Visual Basic Scripting Edition (VBScript)-Beispiel wird gezeigt, wie eine Verbindung mit einem Remote Computer mit Paket Datenschutz hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="60d3b-191">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="60d3b-192">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="60d3b-192">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="60d3b-193">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="60d3b-193">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="60d3b-194">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="60d3b-194">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="60d3b-195">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="60d3b-195">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="60d3b-196">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="60d3b-196">Requirements</span></span>



| <span data-ttu-id="60d3b-197">Anforderung</span><span class="sxs-lookup"><span data-stu-id="60d3b-197">Requirement</span></span> | <span data-ttu-id="60d3b-198">Wert</span><span class="sxs-lookup"><span data-stu-id="60d3b-198">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="60d3b-199">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="60d3b-199">Minimum supported client</span></span><br/> | <span data-ttu-id="60d3b-200">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="60d3b-200">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="60d3b-201">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="60d3b-201">Minimum supported server</span></span><br/> | <span data-ttu-id="60d3b-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="60d3b-202">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="60d3b-203">Namespace</span><span class="sxs-lookup"><span data-stu-id="60d3b-203">Namespace</span></span><br/>                | <span data-ttu-id="60d3b-204">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="60d3b-204">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="60d3b-205">MOF</span><span class="sxs-lookup"><span data-stu-id="60d3b-205">MOF</span></span><br/>                      | <dl> <span data-ttu-id="60d3b-206"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="60d3b-206"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="60d3b-207">DLL</span><span class="sxs-lookup"><span data-stu-id="60d3b-207">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60d3b-208"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60d3b-208"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60d3b-209">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="60d3b-209">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60d3b-210">**Win32 \_ TerminalSetting**</span><span class="sxs-lookup"><span data-stu-id="60d3b-210">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> </dl>

 

