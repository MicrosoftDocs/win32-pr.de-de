---
title: Win32_TSSessionSetting-Klasse
description: Definiert Konfigurationseinstellungen für die Win32 \_ -Terminal Klasse, z. b. Zeitlimits und Aktionen zum Trennen und Wiederherstellen von Verbindungen.
ms.assetid: e115f370-270c-404f-b6c6-7781c1ff376f
ms.tgt_platform: multiple
keywords:
- Win32_TSSessionSetting-Klasse Remotedesktopdienste
- Win32_TSSessionSetting Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TSSessionSetting
- Win32_TSSessionSetting.Caption
- Win32_TSSessionSetting.Description
- Win32_TSSessionSetting.InstallDate
- Win32_TSSessionSetting.Name
- Win32_TSSessionSetting.Status
- Win32_TSSessionSetting.TerminalName
- Win32_TSSessionSetting.ActiveSessionLimit
- Win32_TSSessionSetting.BrokenConnectionAction
- Win32_TSSessionSetting.BrokenConnectionPolicy
- Win32_TSSessionSetting.DisconnectedSessionLimit
- Win32_TSSessionSetting.IdleSessionLimit
- Win32_TSSessionSetting.PolicySourceActiveSessionLimit
- Win32_TSSessionSetting.PolicySourceBrokenConnectionAction
- Win32_TSSessionSetting.PolicySourceDisconnectedSessionLimit
- Win32_TSSessionSetting.PolicySourceIdleSessionLimit
- Win32_TSSessionSetting.PolicySourceReconnectionPolicy
- Win32_TSSessionSetting.ReconnectionPolicy
- Win32_TSSessionSetting.TimeLimitPolicy
- Win32_TSSessionSetting.EnableTimeoutWarning
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e780cdedee0fe447499bed5013dadc2ba9b448b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518977"
---
# <a name="win32_tssessionsetting-class"></a><span data-ttu-id="46e21-105">Win32- \_ Klasse "tssessionsetting"</span><span class="sxs-lookup"><span data-stu-id="46e21-105">Win32\_TSSessionSetting class</span></span>

<span data-ttu-id="46e21-106">Die **Win32 \_ tssessionsetting** -WMI-Klasse definiert Konfigurationseinstellungen für die [**Win32- \_ Terminal**](win32-terminal.md) Klasse, z. b. Zeitlimits und Aktionen zum Trennen und Wiederherstellen von Verbindungen.</span><span class="sxs-lookup"><span data-stu-id="46e21-106">The **Win32\_TSSessionSetting** WMI class defines configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class such as time-limits, and disconnection and reconnection actions.</span></span>

<span data-ttu-id="46e21-107">Die folgende Syntax wird aus dem MOF-Code vereinfacht und umfasst alle definierten und geerbten Eigenschaften in alphabetischer Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="46e21-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="46e21-108">Referenzinformationen zu-Methoden finden Sie in der Tabelle mit den Methoden weiter unten in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="46e21-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="46e21-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="46e21-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSSESSIONSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSSessionSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  uint32   ActiveSessionLimit;
  uint32   BrokenConnectionAction;
  uint32   BrokenConnectionPolicy;
  uint32   DisconnectedSessionLimit;
  uint32   IdleSessionLimit;
  uint32   PolicySourceActiveSessionLimit;
  uint32   PolicySourceBrokenConnectionAction;
  uint32   PolicySourceDisconnectedSessionLimit;
  uint32   PolicySourceIdleSessionLimit;
  uint32   PolicySourceReconnectionPolicy;
  uint32   ReconnectionPolicy;
  uint32   TimeLimitPolicy;
  uint32   EnableTimeoutWarning;
};
```

## <a name="members"></a><span data-ttu-id="46e21-110">Member</span><span class="sxs-lookup"><span data-stu-id="46e21-110">Members</span></span>

<span data-ttu-id="46e21-111">Die Win32-Klasse " **\_ tssessionsetting** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="46e21-111">The **Win32\_TSSessionSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="46e21-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="46e21-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="46e21-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="46e21-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="46e21-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="46e21-114">Methods</span></span>

<span data-ttu-id="46e21-115">Die Win32-Klasse " **\_ tssessionsetting** " verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="46e21-115">The **Win32\_TSSessionSetting** class has these methods.</span></span>



| <span data-ttu-id="46e21-116">Methode</span><span class="sxs-lookup"><span data-stu-id="46e21-116">Method</span></span>                                                              | <span data-ttu-id="46e21-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="46e21-117">Description</span></span>                                                              |
|:--------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [<span data-ttu-id="46e21-118">**Brokenconnection**</span><span class="sxs-lookup"><span data-stu-id="46e21-118">**BrokenConnection**</span></span>](win32-tssessionsetting-brokenconnection.md) | <span data-ttu-id="46e21-119">Legt die in dieser Klasse enthaltenen unterbrochenen Verbindungs Eigenschaften fest.</span><span class="sxs-lookup"><span data-stu-id="46e21-119">Sets the broken connection properties included in this class.</span></span><br/> |
| [<span data-ttu-id="46e21-120">**TimeLimit**</span><span class="sxs-lookup"><span data-stu-id="46e21-120">**TimeLimit**</span></span>](win32-tssessionsetting-timelimit.md)               | <span data-ttu-id="46e21-121">Legt die in dieser Klasse enthaltenen Zeit Limit Eigenschaften fest.</span><span class="sxs-lookup"><span data-stu-id="46e21-121">Sets the time-limit properties included in this class.</span></span><br/>        |



 

### <a name="properties"></a><span data-ttu-id="46e21-122">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="46e21-122">Properties</span></span>

<span data-ttu-id="46e21-123">Die Win32-Klasse " **\_ tssessionsetting** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="46e21-123">The **Win32\_TSSessionSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="46e21-124">**ActiveSessionLimit**</span><span class="sxs-lookup"><span data-stu-id="46e21-124">**ActiveSessionLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46e21-125">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="46e21-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="46e21-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="46e21-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46e21-127">Die maximale Zeitspanne (in Millisekunden), die einer aktiven Sitzung zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="46e21-127">The maximum amount of time, in milliseconds, allocated to an active session.</span></span> <span data-ttu-id="46e21-128">Der Wert 0 gibt einen unbegrenzten Zeitraum an.</span><span class="sxs-lookup"><span data-stu-id="46e21-128">A value of 0 specifies an infinite amount of time.</span></span>

</dd> <dt>

<span data-ttu-id="46e21-129">**BrokenConnectionAction**</span><span class="sxs-lookup"><span data-stu-id="46e21-129">**BrokenConnectionAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46e21-130">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="46e21-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="46e21-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="46e21-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46e21-132">Die Aktion, die der Server für die Sitzung durchführt, wenn eine Verbindung aufgrund von Netzwerk Verlusten oder einer Überschreitung der Zeitlimits unterbrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="46e21-132">The action the server takes on the session when a connection has been broken due to network loss or exceeded time-limits.</span></span>

<dt>

<span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>

<span data-ttu-id="46e21-133"><span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>Verbindung **trennen** (0)</span><span class="sxs-lookup"><span data-stu-id="46e21-133"><span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>**Disconnect** (0)</span></span>


</dt> <dd>

<span data-ttu-id="46e21-134">Der Benutzer ist von der Sitzung getrennt.</span><span class="sxs-lookup"><span data-stu-id="46e21-134">The user is disconnected from the session.</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="46e21-135"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Beenden** (1)</span><span class="sxs-lookup"><span data-stu-id="46e21-135"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (1)</span></span>


</dt> <dd>

<span data-ttu-id="46e21-136">Die Sitzung wird dauerhaft vom Server gelöscht.</span><span class="sxs-lookup"><span data-stu-id="46e21-136">The session is permanently deleted from the server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="46e21-137">**Brokenconnectionpolicy**</span><span class="sxs-lookup"><span data-stu-id="46e21-137">**BrokenConnectionPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46e21-138">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="46e21-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="46e21-139">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="46e21-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="46e21-140">Die Richtlinie, die der Server verwendet, um zu bestimmen, wann eine Verbindung aufgrund von Netzwerk Verlusten oder einer Überschreitung der Zeitlimits unterbrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="46e21-140">The policy the server uses to determine when to break a connection because of network loss or exceeded time-limits.</span></span>

<dt>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>

<span data-ttu-id="46e21-141"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Server-override** (1)</span><span class="sxs-lookup"><span data-stu-id="46e21-141"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Server-Override** (1)</span></span>


</dt> <dd>

<span data-ttu-id="46e21-142">Die Richtlinien Einstellungen für die Trennung der Benutzer werden vom Server überschrieben.</span><span class="sxs-lookup"><span data-stu-id="46e21-142">The user's disconnection policy settings are overridden by the server.</span></span>

</dd> <dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span data-ttu-id="46e21-143"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Pro Benutzer** (0)</span><span class="sxs-lookup"><span data-stu-id="46e21-143"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Per User** (0)</span></span>


</dt> <dd>

<span data-ttu-id="46e21-144">Die Richtlinien Einstellungen für die Trennung des Benutzers sind wirksam.</span><span class="sxs-lookup"><span data-stu-id="46e21-144">The user's disconnection policy settings are in effect.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="46e21-145">**Caption**</span><span class="sxs-lookup"><span data-stu-id="46e21-145">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46e21-146">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="46e21-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46e21-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="46e21-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46e21-148">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="46e21-148">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="46e21-149">Kurze Beschreibung (einzeilige Zeichenfolge) des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="46e21-149">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="46e21-150">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="46e21-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="46e21-151">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="46e21-151">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46e21-152">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="46e21-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46e21-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="46e21-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46e21-154">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="46e21-154">Description of the object.</span></span>

<span data-ttu-id="46e21-155">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="46e21-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="46e21-156">**DisconnectedSessionLimit**</span><span class="sxs-lookup"><span data-stu-id="46e21-156">**DisconnectedSessionLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46e21-157">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="46e21-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="46e21-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="46e21-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46e21-159">Das Zeitintervall (in Millisekunden), nach dem eine getrennte Sitzung beendet wird.</span><span class="sxs-lookup"><span data-stu-id="46e21-159">The time interval, in milliseconds, after which a disconnected session is terminated.</span></span> <span data-ttu-id="46e21-160">Der Wert 0 gibt einen unbegrenzten Zeitraum an.</span><span class="sxs-lookup"><span data-stu-id="46e21-160">A value of 0 specifies an infinite amount of time.</span></span>

</dd> <dt>

<span data-ttu-id="46e21-161">**Enabletimeoutwarning**</span><span class="sxs-lookup"><span data-stu-id="46e21-161">**EnableTimeoutWarning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46e21-162">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="46e21-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="46e21-163">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="46e21-163">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="46e21-164">Aktiviert die Timeout Warnung.</span><span class="sxs-lookup"><span data-stu-id="46e21-164">Enables the timeout warning.</span></span>

<span data-ttu-id="46e21-165">**Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Diese Eigenschaft ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="46e21-165">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="46e21-166">**IdleSessionLimit**</span><span class="sxs-lookup"><span data-stu-id="46e21-166">**IdleSessionLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46e21-167">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="46e21-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="46e21-168">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="46e21-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46e21-169">Das Zeitintervall (in Millisekunden), nach dem eine Sitzung im Leerlauf beendet wird.</span><span class="sxs-lookup"><span data-stu-id="46e21-169">The time interval, in milliseconds, after which an idle session is terminated.</span></span> <span data-ttu-id="46e21-170">Der Wert 0 gibt einen unbegrenzten Zeitraum an.</span><span class="sxs-lookup"><span data-stu-id="46e21-170">A value of 0 specifies an infinite amount of time.</span></span>

</dd> <dt>

<span data-ttu-id="46e21-171">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="46e21-171">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46e21-172">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="46e21-172">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="46e21-173">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="46e21-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46e21-174">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="46e21-174">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="46e21-175">Das Datum, an dem das Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="46e21-175">The date the object was installed.</span></span> <span data-ttu-id="46e21-176">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="46e21-176">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="46e21-177">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="46e21-177">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="46e21-178">**Name**</span><span class="sxs-lookup"><span data-stu-id="46e21-178">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46e21-179">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="46e21-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46e21-180">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="46e21-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46e21-181">Der Name des Objekts.</span><span class="sxs-lookup"><span data-stu-id="46e21-181">The name of the object.</span></span>

<span data-ttu-id="46e21-182">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="46e21-182">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="46e21-183">**Policysourceactivesessionlimit**</span><span class="sxs-lookup"><span data-stu-id="46e21-183">**PolicySourceActiveSessionLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46e21-184">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="46e21-184">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="46e21-185">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="46e21-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46e21-186">Gibt an, ob die **ActiveSessionLimit** -Eigenschaft vom Server, von der Gruppenrichtlinie oder standardmäßig konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="46e21-186">Indicates whether the **ActiveSessionLimit** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="46e21-187">0</span><span class="sxs-lookup"><span data-stu-id="46e21-187">0</span></span>
</dt> <dd>

<span data-ttu-id="46e21-188">Server</span><span class="sxs-lookup"><span data-stu-id="46e21-188">Server</span></span>

</dd> <dt>

<span data-ttu-id="46e21-189">1</span><span class="sxs-lookup"><span data-stu-id="46e21-189">1</span></span>
</dt> <dd>

<span data-ttu-id="46e21-190">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="46e21-190">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="46e21-191">2</span><span class="sxs-lookup"><span data-stu-id="46e21-191">2</span></span>
</dt> <dd>

<span data-ttu-id="46e21-192">Standard</span><span class="sxs-lookup"><span data-stu-id="46e21-192">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="46e21-193">**PolicySourceBrokenConnectionAction**</span><span class="sxs-lookup"><span data-stu-id="46e21-193">**PolicySourceBrokenConnectionAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46e21-194">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="46e21-194">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="46e21-195">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="46e21-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46e21-196">Gibt an, ob die **BrokenConnectionAction** -Eigenschaft vom Server, von der Gruppenrichtlinie oder standardmäßig konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="46e21-196">Indicates whether the **BrokenConnectionAction** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="46e21-197">0</span><span class="sxs-lookup"><span data-stu-id="46e21-197">0</span></span>
</dt> <dd>

<span data-ttu-id="46e21-198">Server</span><span class="sxs-lookup"><span data-stu-id="46e21-198">Server</span></span>

</dd> <dt>

<span data-ttu-id="46e21-199">1</span><span class="sxs-lookup"><span data-stu-id="46e21-199">1</span></span>
</dt> <dd>

<span data-ttu-id="46e21-200">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="46e21-200">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="46e21-201">2</span><span class="sxs-lookup"><span data-stu-id="46e21-201">2</span></span>
</dt> <dd>

<span data-ttu-id="46e21-202">Standard</span><span class="sxs-lookup"><span data-stu-id="46e21-202">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="46e21-203">**PolicySourceDisconnectedSessionLimit**</span><span class="sxs-lookup"><span data-stu-id="46e21-203">**PolicySourceDisconnectedSessionLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46e21-204">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="46e21-204">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="46e21-205">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="46e21-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46e21-206">Gibt an, ob die **DisconnectedSessionLimit** -Eigenschaft vom Server, von der Gruppenrichtlinie oder standardmäßig konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="46e21-206">Indicates whether the **DisconnectedSessionLimit** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="46e21-207">0</span><span class="sxs-lookup"><span data-stu-id="46e21-207">0</span></span>
</dt> <dd>

<span data-ttu-id="46e21-208">Server</span><span class="sxs-lookup"><span data-stu-id="46e21-208">Server</span></span>

</dd> <dt>

<span data-ttu-id="46e21-209">1</span><span class="sxs-lookup"><span data-stu-id="46e21-209">1</span></span>
</dt> <dd>

<span data-ttu-id="46e21-210">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="46e21-210">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="46e21-211">2</span><span class="sxs-lookup"><span data-stu-id="46e21-211">2</span></span>
</dt> <dd>

<span data-ttu-id="46e21-212">Standard</span><span class="sxs-lookup"><span data-stu-id="46e21-212">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="46e21-213">**Policysourceidlesessionlimit**</span><span class="sxs-lookup"><span data-stu-id="46e21-213">**PolicySourceIdleSessionLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46e21-214">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="46e21-214">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="46e21-215">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="46e21-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46e21-216">Gibt an, ob die **IdleSessionLimit** -Eigenschaft vom Server, von der Gruppenrichtlinie oder standardmäßig konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="46e21-216">Indicates whether the **IdleSessionLimit** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="46e21-217">0</span><span class="sxs-lookup"><span data-stu-id="46e21-217">0</span></span>
</dt> <dd>

<span data-ttu-id="46e21-218">Server</span><span class="sxs-lookup"><span data-stu-id="46e21-218">Server</span></span>

</dd> <dt>

<span data-ttu-id="46e21-219">1</span><span class="sxs-lookup"><span data-stu-id="46e21-219">1</span></span>
</dt> <dd>

<span data-ttu-id="46e21-220">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="46e21-220">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="46e21-221">2</span><span class="sxs-lookup"><span data-stu-id="46e21-221">2</span></span>
</dt> <dd>

<span data-ttu-id="46e21-222">Standard</span><span class="sxs-lookup"><span data-stu-id="46e21-222">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="46e21-223">**Policysourcereconnectionpolicy**</span><span class="sxs-lookup"><span data-stu-id="46e21-223">**PolicySourceReconnectionPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46e21-224">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="46e21-224">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="46e21-225">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="46e21-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46e21-226">Gibt an, ob die **reconnectpolicy** -Eigenschaft vom Server, von der Gruppenrichtlinie oder standardmäßig konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="46e21-226">Indicates whether the **ReconnectPolicy** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="46e21-227">0</span><span class="sxs-lookup"><span data-stu-id="46e21-227">0</span></span>
</dt> <dd>

<span data-ttu-id="46e21-228">Server</span><span class="sxs-lookup"><span data-stu-id="46e21-228">Server</span></span>

</dd> <dt>

<span data-ttu-id="46e21-229">1</span><span class="sxs-lookup"><span data-stu-id="46e21-229">1</span></span>
</dt> <dd>

<span data-ttu-id="46e21-230">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="46e21-230">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="46e21-231">2</span><span class="sxs-lookup"><span data-stu-id="46e21-231">2</span></span>
</dt> <dd>

<span data-ttu-id="46e21-232">Standard</span><span class="sxs-lookup"><span data-stu-id="46e21-232">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="46e21-233">**Reconnectionpolicy**</span><span class="sxs-lookup"><span data-stu-id="46e21-233">**ReconnectionPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46e21-234">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="46e21-234">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="46e21-235">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="46e21-235">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="46e21-236">Gibt an, ob ein Benutzer den vorherigen Client verwenden muss, um erneut eine Verbindung mit einer getrennten Sitzung herzustellen.</span><span class="sxs-lookup"><span data-stu-id="46e21-236">Specifies whether a user must use the previous client to reconnect to a disconnected session.</span></span>

<dt>

<span id="Any_Client"></span><span id="any_client"></span><span id="ANY_CLIENT"></span>

<span data-ttu-id="46e21-237"><span id="Any_Client"></span><span id="any_client"></span><span id="ANY_CLIENT"></span>**Beliebiger Client** (0)</span><span class="sxs-lookup"><span data-stu-id="46e21-237"><span id="Any_Client"></span><span id="any_client"></span><span id="ANY_CLIENT"></span>**Any Client** (0)</span></span>


</dt> <dd>

<span data-ttu-id="46e21-238">Jeder Client wird verwendet, um die Verbindung wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="46e21-238">Any client will be used to reconnect.</span></span>

</dd> <dt>

<span id="Previous_Client"></span><span id="previous_client"></span><span id="PREVIOUS_CLIENT"></span>

<span data-ttu-id="46e21-239"><span id="Previous_Client"></span><span id="previous_client"></span><span id="PREVIOUS_CLIENT"></span>**Vorheriger Client** (1)</span><span class="sxs-lookup"><span data-stu-id="46e21-239"><span id="Previous_Client"></span><span id="previous_client"></span><span id="PREVIOUS_CLIENT"></span>**Previous Client** (1)</span></span>


</dt> <dd>

<span data-ttu-id="46e21-240">Der vorherige Client, der in einer Verbindung verwendet wird, wird verwendet, um die Verbindung wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="46e21-240">The previous client used in a connection will be used to reconnect.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="46e21-241">**Status**</span><span class="sxs-lookup"><span data-stu-id="46e21-241">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46e21-242">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="46e21-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46e21-243">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="46e21-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46e21-244">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="46e21-244">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="46e21-245">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="46e21-245">Current status of the object.</span></span> <span data-ttu-id="46e21-246">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="46e21-246">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="46e21-247">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="46e21-247">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="46e21-248">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="46e21-248">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="46e21-249">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="46e21-249">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="46e21-250">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="46e21-250">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="46e21-251">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="46e21-251">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="46e21-252">("OK")</span><span class="sxs-lookup"><span data-stu-id="46e21-252">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="46e21-253">("Fehler")</span><span class="sxs-lookup"><span data-stu-id="46e21-253">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="46e21-254">("Heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="46e21-254">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="46e21-255">("Unbekannt")</span><span class="sxs-lookup"><span data-stu-id="46e21-255">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="46e21-256">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="46e21-256">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="46e21-257">("Wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="46e21-257">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="46e21-258">("Wird beendet")</span><span class="sxs-lookup"><span data-stu-id="46e21-258">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="46e21-259">("Dienst")</span><span class="sxs-lookup"><span data-stu-id="46e21-259">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="46e21-260">**Terminal Name**</span><span class="sxs-lookup"><span data-stu-id="46e21-260">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46e21-261">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="46e21-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46e21-262">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="46e21-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46e21-263">Der Name des Terminals.</span><span class="sxs-lookup"><span data-stu-id="46e21-263">The name of the terminal.</span></span>

<span data-ttu-id="46e21-264">Diese Eigenschaft wird von [**Win32 \_ TerminalSetting**](win32-terminalsetting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="46e21-264">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> <dt>

<span data-ttu-id="46e21-265">**Timelimitpolicy**</span><span class="sxs-lookup"><span data-stu-id="46e21-265">**TimeLimitPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46e21-266">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="46e21-266">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="46e21-267">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="46e21-267">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="46e21-268">Die Richtlinie, die der Server verwendet, um Zeitlimits für Benutzersitzungen festzulegen.</span><span class="sxs-lookup"><span data-stu-id="46e21-268">The policy the server uses to determine time-limits for user sessions.</span></span>

<dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span data-ttu-id="46e21-269"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Pro Benutzer** (0)</span><span class="sxs-lookup"><span data-stu-id="46e21-269"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Per User** (0)</span></span>


</dt> <dd>

<span data-ttu-id="46e21-270">Die Richtlinien Einstellungen für die Zeitlimits des Benutzers sind wirksam.</span><span class="sxs-lookup"><span data-stu-id="46e21-270">The user's time-limits policy settings are in effect.</span></span>

</dd> <dt>

<span id="Server_Override"></span><span id="server_override"></span><span id="SERVER_OVERRIDE"></span>

<span data-ttu-id="46e21-271"><span id="Server_Override"></span><span id="server_override"></span><span id="SERVER_OVERRIDE"></span>**Server Überschreibung** (1)</span><span class="sxs-lookup"><span data-stu-id="46e21-271"><span id="Server_Override"></span><span id="server_override"></span><span id="SERVER_OVERRIDE"></span>**Server Override** (1)</span></span>


</dt> <dd>

<span data-ttu-id="46e21-272">Die Richtlinien Einstellungen für die Zeitlimits des Benutzers werden vom Server überschrieben.</span><span class="sxs-lookup"><span data-stu-id="46e21-272">The user's time-limits policy settings are overridden by the server.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="46e21-273">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="46e21-273">Remarks</span></span>

<span data-ttu-id="46e21-274">Beachten Sie, dass die der Konsolen Sitzung zugeordneten Winstations nicht auf die Methoden und Eigenschaften dieser Klasse zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="46e21-274">Be aware that Winstations associated with the console session cannot access the methods and properties of this class.</span></span> <span data-ttu-id="46e21-275">Wenn ein Versuch unternommen wird, indem "Console" als Wert der Terminalname-Eigenschaft angegeben wird, wird **WBEM \_ E \_ \_** von Methoden dieses Objekts zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="46e21-275">If an attempt is made to do so by specifying "Console" as the value of the TerminalName property, methods of this object will return **WBEM\_E\_NOT\_SUPPORTED**.</span></span> <span data-ttu-id="46e21-276">Dieser Fehlercode wird auch zurückgegeben, wenn eine Fenster Station versucht, Methoden dieses Objekts zum Hinzufügen oder Ändern der Sicherheitseigenschaften der Konten "LocalSystem", "LocalService" oder "Network Service" aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="46e21-276">This error code will also be returned if a window station attempts to call methods of this object for the purpose of adding or modifying the security properties of the LocalSystem, LocalService, or NetworkService accounts.</span></span>

<span data-ttu-id="46e21-277">Zum Herstellen einer Verbindung mit dem \\ Namespace "root cimv2 \\ TerminalServices" muss die Authentifizierungs Ebene den Datenschutz für das Paket enthalten.</span><span class="sxs-lookup"><span data-stu-id="46e21-277">To connect to the "root\\CIMV2\\TerminalServices" namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="46e21-278">Bei C/C++-aufrufen wäre dies eine Authentifizierungs Ebene der **RPC- \_ c- \_ authn- \_ Ebene \_ Pkt- \_ Datenschutz**.</span><span class="sxs-lookup"><span data-stu-id="46e21-278">For C/C++ calls, this would be an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="46e21-279">Bei Visual Basic-und Skript aufrufen wäre dies eine Authentifizierungs Ebene von **wbemauthenticationlevelpktprivacy** oder "PKTPRIVACY" mit einem Wert von 6.</span><span class="sxs-lookup"><span data-stu-id="46e21-279">For Visual Basic and scripting calls, this would be an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="46e21-280">Im folgenden Visual Basic Scripting Edition (VBScript)-Beispiel wird gezeigt, wie eine Verbindung mit einem Remote Computer mit Paket Datenschutz hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="46e21-280">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="46e21-281">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="46e21-281">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="46e21-282">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="46e21-282">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="46e21-283">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="46e21-283">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="46e21-284">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="46e21-284">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="46e21-285">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="46e21-285">Requirements</span></span>



| <span data-ttu-id="46e21-286">Anforderung</span><span class="sxs-lookup"><span data-stu-id="46e21-286">Requirement</span></span> | <span data-ttu-id="46e21-287">Wert</span><span class="sxs-lookup"><span data-stu-id="46e21-287">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="46e21-288">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="46e21-288">Minimum supported client</span></span><br/> | <span data-ttu-id="46e21-289">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="46e21-289">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="46e21-290">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="46e21-290">Minimum supported server</span></span><br/> | <span data-ttu-id="46e21-291">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="46e21-291">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="46e21-292">Namespace</span><span class="sxs-lookup"><span data-stu-id="46e21-292">Namespace</span></span><br/>                | <span data-ttu-id="46e21-293">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="46e21-293">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="46e21-294">MOF</span><span class="sxs-lookup"><span data-stu-id="46e21-294">MOF</span></span><br/>                      | <dl> <span data-ttu-id="46e21-295"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="46e21-295"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="46e21-296">DLL</span><span class="sxs-lookup"><span data-stu-id="46e21-296">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46e21-297"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46e21-297"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46e21-298">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46e21-298">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46e21-299">**Win32 \_ TerminalSetting**</span><span class="sxs-lookup"><span data-stu-id="46e21-299">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> <dt>

[<span data-ttu-id="46e21-300">**CIM- \_ Einstellung**</span><span class="sxs-lookup"><span data-stu-id="46e21-300">**CIM\_Setting**</span></span>](/windows/desktop/CIMWin32Prov/cim-setting)
</dt> </dl>

 

