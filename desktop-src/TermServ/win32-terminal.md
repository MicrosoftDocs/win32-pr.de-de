---
title: Win32_Terminal-Klasse
description: Stellt ein Terminal dar.
ms.assetid: d56cc605-6c5a-46ae-96fd-d0a4f5b6074a
ms.tgt_platform: multiple
keywords:
- Win32_Terminal-Klasse Remotedesktopdienste
- Win32_Terminal Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_Terminal
- Win32_Terminal.Caption
- Win32_Terminal.Description
- Win32_Terminal.InstallDate
- Win32_Terminal.Name
- Win32_Terminal.Status
- Win32_Terminal.fEnableTerminal
- Win32_Terminal.LoggedOnUsers
- Win32_Terminal.TerminalName
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7ae74003f798049fbdb34c955db3f64112bfcd2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103147"
---
# <a name="win32_terminal-class"></a><span data-ttu-id="5118b-105">Win32- \_ Terminal Klasse</span><span class="sxs-lookup"><span data-stu-id="5118b-105">Win32\_Terminal class</span></span>

<span data-ttu-id="5118b-106">Die **Win32- \_ Terminal** -WMI-Klasse stellt ein Terminal dar.</span><span class="sxs-lookup"><span data-stu-id="5118b-106">The **Win32\_Terminal** WMI class represents a terminal.</span></span>

<span data-ttu-id="5118b-107">Die folgende Syntax wird aus dem MOF-Code vereinfacht und umfasst alle definierten und geerbten Eigenschaften in alphabetischer Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="5118b-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="5118b-108">Referenzinformationen zu-Methoden finden Sie in der Tabelle mit den Methoden weiter unten in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="5118b-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="5118b-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="5118b-109">Syntax</span></span>

``` syntax
[dynamic, overwrite, provider("Win32_WIN32_TERMINAL_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_Terminal : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint32   fEnableTerminal;
  uint32   LoggedOnUsers;
  string   TerminalName;
};
```

## <a name="members"></a><span data-ttu-id="5118b-110">Member</span><span class="sxs-lookup"><span data-stu-id="5118b-110">Members</span></span>

<span data-ttu-id="5118b-111">Die **Win32- \_ Terminal** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="5118b-111">The **Win32\_Terminal** class has these types of members:</span></span>

-   [<span data-ttu-id="5118b-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="5118b-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="5118b-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5118b-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5118b-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="5118b-114">Methods</span></span>

<span data-ttu-id="5118b-115">Die **Win32- \_ Terminal** Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="5118b-115">The **Win32\_Terminal** class has these methods.</span></span>



| <span data-ttu-id="5118b-116">Methode</span><span class="sxs-lookup"><span data-stu-id="5118b-116">Method</span></span>                                  | <span data-ttu-id="5118b-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5118b-117">Description</span></span>                                                                                                                                                                             |
|:----------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5118b-118">**Stelle**</span><span class="sxs-lookup"><span data-stu-id="5118b-118">**Create**</span></span>](create-win32-terminal.md) | <span data-ttu-id="5118b-119">Erstellt ein Terminal mit Standardeinstellungen, die mithilfe der Eigenschaften und Methoden der [**Win32 \_ TerminalSetting**](win32-terminalsetting.md) -Klassen angepasst werden können.</span><span class="sxs-lookup"><span data-stu-id="5118b-119">Creates a terminal with default settings which can be customized by using the properties and methods of the [**Win32\_TerminalSetting**](win32-terminalsetting.md) classes.</span></span><br/> |
| [<span data-ttu-id="5118b-120">**Lösch**</span><span class="sxs-lookup"><span data-stu-id="5118b-120">**Delete**</span></span>](delete-win32-terminal.md) | <span data-ttu-id="5118b-121">Löscht das angegebene Terminal.</span><span class="sxs-lookup"><span data-stu-id="5118b-121">Deletes the specified terminal.</span></span><br/>                                                                                                                                              |
| [<span data-ttu-id="5118b-122">**Aktivieren**</span><span class="sxs-lookup"><span data-stu-id="5118b-122">**Enable**</span></span>](win32-terminal-enable.md) | <span data-ttu-id="5118b-123">Deaktiviert oder aktiviert das Terminal.</span><span class="sxs-lookup"><span data-stu-id="5118b-123">Disables or enables the terminal.</span></span><br/>                                                                                                                                            |
| [<span data-ttu-id="5118b-124">**Benen**</span><span class="sxs-lookup"><span data-stu-id="5118b-124">**Rename**</span></span>](win32-terminal-rename.md) | <span data-ttu-id="5118b-125">Benennt das Terminal um.</span><span class="sxs-lookup"><span data-stu-id="5118b-125">Renames the terminal.</span></span><br/>                                                                                                                                                        |



 

### <a name="properties"></a><span data-ttu-id="5118b-126">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5118b-126">Properties</span></span>

<span data-ttu-id="5118b-127">Die **Win32- \_ Terminal** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5118b-127">The **Win32\_Terminal** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5118b-128">**Caption**</span><span class="sxs-lookup"><span data-stu-id="5118b-128">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5118b-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5118b-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5118b-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5118b-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5118b-131">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="5118b-131">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5118b-132">Kurze Beschreibung (einzeilige Zeichenfolge) des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="5118b-132">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="5118b-133">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5118b-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5118b-134">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5118b-134">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5118b-135">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5118b-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5118b-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5118b-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5118b-137">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="5118b-137">Description of the object.</span></span>

<span data-ttu-id="5118b-138">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5118b-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5118b-139">**fenableterminal**</span><span class="sxs-lookup"><span data-stu-id="5118b-139">**fEnableTerminal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5118b-140">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5118b-140">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5118b-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5118b-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5118b-142">Gibt an, ob das angegebene Terminal deaktiviert oder aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="5118b-142">Specifies whether the specified terminal is disabled or enabled.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="5118b-143"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="5118b-143"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="5118b-144">Das Terminal ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="5118b-144">The terminal is disabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="5118b-145"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="5118b-145"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="5118b-146">Das Terminal ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="5118b-146">The terminal is enabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5118b-147">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5118b-147">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5118b-148">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="5118b-148">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5118b-149">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5118b-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5118b-150">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="5118b-150">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="5118b-151">Das Datum, an dem das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="5118b-151">The date the object was installed.</span></span> <span data-ttu-id="5118b-152">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="5118b-152">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="5118b-153">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5118b-153">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5118b-154">**Loggedonusers**</span><span class="sxs-lookup"><span data-stu-id="5118b-154">**LoggedOnUsers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5118b-155">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5118b-155">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5118b-156">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5118b-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5118b-157">Anzahl der angemeldeten Sitzungen für das Terminal.</span><span class="sxs-lookup"><span data-stu-id="5118b-157">Number of logged-on sessions for the terminal.</span></span>

</dd> <dt>

<span data-ttu-id="5118b-158">**Name**</span><span class="sxs-lookup"><span data-stu-id="5118b-158">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5118b-159">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5118b-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5118b-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5118b-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5118b-161">Der Name des Objekts.</span><span class="sxs-lookup"><span data-stu-id="5118b-161">The name of the object.</span></span>

<span data-ttu-id="5118b-162">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5118b-162">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5118b-163">**Status**</span><span class="sxs-lookup"><span data-stu-id="5118b-163">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5118b-164">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5118b-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5118b-165">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5118b-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5118b-166">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="5118b-166">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="5118b-167">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="5118b-167">Current status of the object.</span></span> <span data-ttu-id="5118b-168">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="5118b-168">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="5118b-169">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="5118b-169">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="5118b-170">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="5118b-170">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="5118b-171">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="5118b-171">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="5118b-172">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="5118b-172">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="5118b-173">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5118b-173">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="5118b-174">("OK")</span><span class="sxs-lookup"><span data-stu-id="5118b-174">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5118b-175">("Fehler")</span><span class="sxs-lookup"><span data-stu-id="5118b-175">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5118b-176">("Heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="5118b-176">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5118b-177">("Unbekannt")</span><span class="sxs-lookup"><span data-stu-id="5118b-177">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5118b-178">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="5118b-178">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5118b-179">("Wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="5118b-179">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5118b-180">("Wird beendet")</span><span class="sxs-lookup"><span data-stu-id="5118b-180">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5118b-181">("Dienst")</span><span class="sxs-lookup"><span data-stu-id="5118b-181">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5118b-182">**Terminal Name**</span><span class="sxs-lookup"><span data-stu-id="5118b-182">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5118b-183">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5118b-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5118b-184">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5118b-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5118b-185">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5118b-185">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5118b-186">Der eindeutige Name, der die Instanz des Terminals identifiziert.</span><span class="sxs-lookup"><span data-stu-id="5118b-186">The unique name that identifies the instance of the terminal.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5118b-187">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5118b-187">Remarks</span></span>

<span data-ttu-id="5118b-188">**Win32 \_ Terminal** ist [**Win32 \_ TerminalSetting**](win32-terminalsetting.md) als **Element** Eigenschaft der [**Win32 \_ terminalterminalsetting**](win32-terminalterminalsetting.md) -Zuordnung zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="5118b-188">**Win32\_Terminal** is associated with [**Win32\_TerminalSetting**](win32-terminalsetting.md) as the **Element** property of the [**Win32\_TerminalTerminalSetting**](win32-terminalterminalsetting.md) association.</span></span>

<span data-ttu-id="5118b-189">Die folgenden Klassen sind Unterklassen der **Win32- \_ Terminal** Klasse: [**Win32 \_ tgeneralsetting**](win32-tsgeneralsetting.md), [**Win32 \_**](win32-tslogonsetting.md)-Anmelde Name, Win32 [**\_ tssessionsetting**](win32-tssessionsetting.md), [**Win32 \_ tsenvironmentsetting**](win32-tsenvironmentsetting.md), [**Win32 tspertecontrolsetting \_**](win32-tsremotecontrolsetting.md), [**Win32 \_ tsclientsetting**](win32-tsclientsetting.md), [**Win32 \_ tnetworkadaptersetting**](win32-tsnetworkadaptersetting.md), [**Win32 \_**](win32-tsnetworkadapterlistsetting.md) [**\_ tspermissionsetting**](win32-tspermissionssetting.md)und Win32- [**\_ Konto**](win32-tsaccount.md).</span><span class="sxs-lookup"><span data-stu-id="5118b-189">The following classes are subclasses of the **Win32\_Terminal** class: [**Win32\_TSGeneralSetting**](win32-tsgeneralsetting.md), [**Win32\_TSLogonSetting**](win32-tslogonsetting.md), [**Win32\_TSSessionSetting**](win32-tssessionsetting.md), [**Win32\_TSEnvironmentSetting**](win32-tsenvironmentsetting.md), [**Win32\_TSRemoteControlSetting**](win32-tsremotecontrolsetting.md), [**Win32\_TSClientSetting**](win32-tsclientsetting.md), [**Win32\_TSNetworkAdapterSetting**](win32-tsnetworkadaptersetting.md), [**Win32\_TSNetworkAdapterListSetting**](win32-tsnetworkadapterlistsetting.md), [**Win32\_TSPermissionsSetting**](win32-tspermissionssetting.md), and [**Win32\_TSAccount**](win32-tsaccount.md).</span></span>

<span data-ttu-id="5118b-190">Beachten Sie, dass die der Konsolen Sitzung zugeordneten Winstations nicht auf die Methoden und Eigenschaften dieser Klasse zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="5118b-190">Note that Winstations associated with the console session cannot access the methods and properties of this class.</span></span> <span data-ttu-id="5118b-191">Wenn ein Versuch unternommen wird, indem "Console" als Wert der **Terminalname** -Eigenschaft angegeben wird, geben die Methoden dieses Objekts **WBEM \_ E \_ nicht \_ unterstützt** zurück.</span><span class="sxs-lookup"><span data-stu-id="5118b-191">If an attempt is made to do so by specifying "Console" as the value of the **TerminalName** property, methods of this object return **WBEM\_E\_NOT\_SUPPORTED**.</span></span> <span data-ttu-id="5118b-192">Dieser Fehlercode wird auch zurückgegeben, wenn eine Fenster Station versucht, Methoden dieses Objekts aufzurufen, um die Sicherheitseigenschaften der Konten "LocalSystem", "LocalService" oder "Network Service" hinzuzufügen oder zu ändern.</span><span class="sxs-lookup"><span data-stu-id="5118b-192">This error code is also returned if a window station attempts to call methods of this object to add or modify the security properties of the LocalSystem, LocalService, or NetworkService accounts.</span></span>

<span data-ttu-id="5118b-193">Zum Herstellen einer Verbindung mit dem \\ root \\ CIMV2 \\ TerminalServices-Namespace muss die Authentifizierungs Ebene den Datenschutz für das Paket enthalten.</span><span class="sxs-lookup"><span data-stu-id="5118b-193">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="5118b-194">Bei C/C++-aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene der **RPC- \_ c- \_ authn- \_ Ebene \_ Pkt \_ Privacy**.</span><span class="sxs-lookup"><span data-stu-id="5118b-194">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="5118b-195">Bei Visual Basic-und Skript aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene von **wbemauthenticationlevelpzprivacy** oder "PKTPRIVACY" mit einem Wert von 6.</span><span class="sxs-lookup"><span data-stu-id="5118b-195">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="5118b-196">Im folgenden Visual Basic Scripting Edition (VBScript)-Beispiel wird gezeigt, wie eine Verbindung mit einem Remote Computer mit Paket Datenschutz hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="5118b-196">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="5118b-197">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="5118b-197">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5118b-198">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="5118b-198">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="5118b-199">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="5118b-199">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5118b-200">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="5118b-200">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="5118b-201">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5118b-201">Requirements</span></span>



| <span data-ttu-id="5118b-202">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5118b-202">Requirement</span></span> | <span data-ttu-id="5118b-203">Wert</span><span class="sxs-lookup"><span data-stu-id="5118b-203">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5118b-204">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5118b-204">Minimum supported client</span></span><br/> | <span data-ttu-id="5118b-205">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5118b-205">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5118b-206">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5118b-206">Minimum supported server</span></span><br/> | <span data-ttu-id="5118b-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5118b-207">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5118b-208">Namespace</span><span class="sxs-lookup"><span data-stu-id="5118b-208">Namespace</span></span><br/>                | <span data-ttu-id="5118b-209">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="5118b-209">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="5118b-210">MOF</span><span class="sxs-lookup"><span data-stu-id="5118b-210">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5118b-211"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5118b-211"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="5118b-212">DLL</span><span class="sxs-lookup"><span data-stu-id="5118b-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5118b-213"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5118b-213"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5118b-214">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5118b-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5118b-215">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="5118b-215">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="5118b-216">**Win32 \_ terminalservicesetts**</span><span class="sxs-lookup"><span data-stu-id="5118b-216">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="5118b-217">**Win32 \_ terminalterminalsetting**</span><span class="sxs-lookup"><span data-stu-id="5118b-217">**Win32\_TerminalTerminalSetting**</span></span>](win32-terminalterminalsetting.md)
</dt> </dl>

 

