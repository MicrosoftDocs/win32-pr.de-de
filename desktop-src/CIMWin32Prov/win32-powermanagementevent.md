---
description: Das Win32- \_ powermanagementevent-&\# 32; Die WMI-Klasse stellt Energie Verwaltungs Ereignisse dar, die sich aus Energie Zustandsänderungen ergeben.
ms.assetid: b5781805-87c7-4eaf-afbb-a1770fcff41c
ms.tgt_platform: multiple
title: Win32_PowerManagementEvent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PowerManagementEvent
- Win32_PowerManagementEvent.SECURITY_DESCRIPTOR
- Win32_PowerManagementEvent.TIME_CREATED
- Win32_PowerManagementEvent.EventType
- Win32_PowerManagementEvent.OEMEventCode
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e0e7dfa68646dbefb6d6b70218fe99830b44a0c1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126841"
---
# <a name="win32_powermanagementevent-class"></a><span data-ttu-id="2e9a6-103">Win32- \_ Klasse "powermanagementevent"</span><span class="sxs-lookup"><span data-stu-id="2e9a6-103">Win32\_PowerManagementEvent class</span></span>

<span data-ttu-id="2e9a6-104">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) " **Win32 \_ powermanagementevent** " stellt Energie Verwaltungs Ereignisse dar, die sich aus Energie Zustandsänderungen ergeben.</span><span class="sxs-lookup"><span data-stu-id="2e9a6-104">The **Win32\_PowerManagementEvent** [WMI class](../wmisdk/retrieving-a-class.md) represents power management events resulting from power state changes.</span></span> <span data-ttu-id="2e9a6-105">Diese Zustandsänderungen sind entweder mit der Advanced Power Management (APM)-oder der Advanced Configuration and Power Interface (ACPI)-System Verwaltungs Protokolle verknüpft.</span><span class="sxs-lookup"><span data-stu-id="2e9a6-105">These state changes are associated with either the Advanced Power Management (APM) or the Advanced Configuration and Power Interface (ACPI) system management protocols.</span></span>

<span data-ttu-id="2e9a6-106">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2e9a6-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="2e9a6-107">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="2e9a6-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e9a6-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e9a6-108">Syntax</span></span>

``` syntax
[UUID("{86460B6B-E709-11d2-B139-00105A1F77A1}"), AMENDMENT]
class Win32_PowerManagementEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  uint16 EventType;
  uint16 OEMEventCode;
};
```

## <a name="members"></a><span data-ttu-id="2e9a6-109">Member</span><span class="sxs-lookup"><span data-stu-id="2e9a6-109">Members</span></span>

<span data-ttu-id="2e9a6-110">Die Win32-Klasse " **\_ powermanagementevent** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2e9a6-110">The **Win32\_PowerManagementEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="2e9a6-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2e9a6-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2e9a6-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2e9a6-112">Properties</span></span>

<span data-ttu-id="2e9a6-113">Die Win32-Klasse " **\_ powermanagementevent** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2e9a6-113">The **Win32\_PowerManagementEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2e9a6-114">**EventType**</span><span class="sxs-lookup"><span data-stu-id="2e9a6-114">**EventType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e9a6-115">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2e9a6-115">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2e9a6-116">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2e9a6-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e9a6-117">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Energie Verwaltungs Ereignisse")</span><span class="sxs-lookup"><span data-stu-id="2e9a6-117">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Power Management Events")</span></span>
</dt> </dl>

<span data-ttu-id="2e9a6-118">Der Typ der Änderung im System Energiezustand.</span><span class="sxs-lookup"><span data-stu-id="2e9a6-118">Type of change in the system power state.</span></span>

<dt>

<span id="Entering_Suspend"></span><span id="entering_suspend"></span><span id="ENTERING_SUSPEND"></span>

<span data-ttu-id="2e9a6-119"><span id="Entering_Suspend"></span><span id="entering_suspend"></span><span id="ENTERING_SUSPEND"></span>Wechseln **in Suspend** (4)</span><span class="sxs-lookup"><span data-stu-id="2e9a6-119"><span id="Entering_Suspend"></span><span id="entering_suspend"></span><span id="ENTERING_SUSPEND"></span>**Entering Suspend** (4)</span></span>


</dt> <dd>

<span data-ttu-id="2e9a6-120">Der Computer ist zwar angehalten, scheint aber deaktiviert zu sein. Allerdings kann Sie als Reaktion auf verschiedene Ereignisse wie Benutzereingaben (z. b. bewegen der Maus oder Drücken einer Taste auf der Tastatur) als "erwacht" angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="2e9a6-120">While suspended, the computer appears to be off; however, it can be "awakened" in response to various events, including user input (such as moving the mouse or pressing a key on the keyboard).</span></span> <span data-ttu-id="2e9a6-121">Während der Computer angehalten wird, wird der Stromverbrauch auf eine von mehreren Ebenen reduziert, je nachdem, wie das System verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2e9a6-121">While the computer is suspended, power consumption is reduced to one of several levels depending on how the system is to be used.</span></span> <span data-ttu-id="2e9a6-122">Je niedriger die Stromverbrauchs Ebene, desto länger dauert es, bis das System wieder in den Arbeitszustand wechselt.</span><span class="sxs-lookup"><span data-stu-id="2e9a6-122">The lower the level of power consumption, the more time it takes the system to return to the working state.</span></span> <span data-ttu-id="2e9a6-123">Wenn der Computer in den anhaltezustand wechselt, wird der Desktop gesperrt, und Sie müssen STRG + ALT + ENTF drücken und einen gültigen Benutzernamen und ein gültiges Kennwort angeben, um den Vorgang fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="2e9a6-123">When the computer enters the suspend state, the desktop is locked, and you must press CTRL+ALT+DELETE and provide a valid user name and password to resume operations</span></span>

</dd> <dt>

<span id="Resume_from_Suspend"></span><span id="resume_from_suspend"></span><span id="RESUME_FROM_SUSPEND"></span>

<span data-ttu-id="2e9a6-124"><span id="Resume_from_Suspend"></span><span id="resume_from_suspend"></span><span id="RESUME_FROM_SUSPEND"></span>Fortsetzen **von Suspend** (7)</span><span class="sxs-lookup"><span data-stu-id="2e9a6-124"><span id="Resume_from_Suspend"></span><span id="resume_from_suspend"></span><span id="RESUME_FROM_SUSPEND"></span>**Resume from Suspend** (7)</span></span>


</dt> <dd>

<span data-ttu-id="2e9a6-125">Gibt an, dass eine Nachricht zum Fortsetzen des Anhaltevorgangs gesendet wurde, sodass der Computer seinen regulären Energiezustand wiederherstellen kann.</span><span class="sxs-lookup"><span data-stu-id="2e9a6-125">Indicates that a Resume from Suspend message has been sent, enabling the computer to return to its regular power state.</span></span>

</dd> <dt>

<span id="Power_Status_Change"></span><span id="power_status_change"></span><span id="POWER_STATUS_CHANGE"></span>

<span data-ttu-id="2e9a6-126"><span id="Power_Status_Change"></span><span id="power_status_change"></span><span id="POWER_STATUS_CHANGE"></span>**Energie Status Änderung** (10)</span><span class="sxs-lookup"><span data-stu-id="2e9a6-126"><span id="Power_Status_Change"></span><span id="power_status_change"></span><span id="POWER_STATUS_CHANGE"></span>**Power Status Change** (10)</span></span>


</dt> <dd>

<span data-ttu-id="2e9a6-127">Gibt an, dass der Energiestatus des Computers geändert wird, z. b. ein Wechsel von Akku Strom in die Stromversorgung oder von einem Wechsel zu einer unterbrechungsfreien Stromversorgung.</span><span class="sxs-lookup"><span data-stu-id="2e9a6-127">Indicates a change in the power status of the computer, such as a switch from battery power to AC, or from AC to an uninterruptible power supply.</span></span> <span data-ttu-id="2e9a6-128">Das System leitet dieses Ereignis auch dann weiter, wenn die verbleibende Akkuleistung unter einen vom Benutzer festgelegten Wert sinkt oder sich um einen angegebenen Prozentsatz ändert.</span><span class="sxs-lookup"><span data-stu-id="2e9a6-128">The system also broadcasts this event when remaining battery power slips below the threshold specified by the user or if the battery power changes by a specified percentage.</span></span>

</dd> <dt>

<span id="OEM_Event"></span><span id="oem_event"></span><span id="OEM_EVENT"></span>

<span data-ttu-id="2e9a6-129"><span id="OEM_Event"></span><span id="oem_event"></span><span id="OEM_EVENT"></span>**OEM-Ereignis** (11)</span><span class="sxs-lookup"><span data-stu-id="2e9a6-129"><span id="OEM_Event"></span><span id="oem_event"></span><span id="OEM_EVENT"></span>**OEM Event** (11)</span></span>


</dt> <dd>

<span data-ttu-id="2e9a6-130">Gibt an, dass ein APM-BIOS (Advanced Power Management) ein OEM-Ereignis gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="2e9a6-130">Indicates that an Advanced Power Management (APM) BIOS has sent an OEM event.</span></span> <span data-ttu-id="2e9a6-131">Der Wert des Ereignisses wird in der Eigenschaft " **OEMEventCode** " aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="2e9a6-131">The value of the event will be captured in the **OEMEventCode** property.</span></span> <span data-ttu-id="2e9a6-132">Da einige APM-BIOS-Implementierungen keine OEM-Ereignis Benachrichtigungen bereitstellen, wird dieses Ereignis möglicherweise nie auf einigen Computern übertragen.</span><span class="sxs-lookup"><span data-stu-id="2e9a6-132">Because some APM BIOS implementations do not provide OEM event notifications, this event might never be broadcast on some computers.</span></span> <span data-ttu-id="2e9a6-133">APM ist ein Legacy-Energie Verwaltungs Schema.</span><span class="sxs-lookup"><span data-stu-id="2e9a6-133">APM is a legacy power management scheme.</span></span> <span data-ttu-id="2e9a6-134">Apm wird zwar weiterhin unterstützt, ist jedoch größtenteils durch ACPI abgelöst (Erweiterte Konfiguration und Energie Schnittstelle).</span><span class="sxs-lookup"><span data-stu-id="2e9a6-134">Although still supported, APM has been largely superseded by ACPI (Advanced Configuration and Power Interface).</span></span>

</dd> <dt>

<span id="Resume_Automatic"></span><span id="resume_automatic"></span><span id="RESUME_AUTOMATIC"></span>

<span data-ttu-id="2e9a6-135"><span id="Resume_Automatic"></span><span id="resume_automatic"></span><span id="RESUME_AUTOMATIC"></span>**Automatisch** fortsetzen (18)</span><span class="sxs-lookup"><span data-stu-id="2e9a6-135"><span id="Resume_Automatic"></span><span id="resume_automatic"></span><span id="RESUME_AUTOMATIC"></span>**Resume Automatic** (18)</span></span>


</dt> <dd>

<span data-ttu-id="2e9a6-136">Gibt an, dass der Computer als Reaktion auf ein Ereignis erwacht ist.</span><span class="sxs-lookup"><span data-stu-id="2e9a6-136">Indicates that the computer has awakened in response to an event.</span></span> <span data-ttu-id="2e9a6-137">Wenn das Systembenutzer Aktivitäten erkennt (z. b. einen Mausklick), wird die resumesuspend-Nachricht gesendet, sodass die Anwendungen wissen, dass Sie die vollständige Interaktivität mit dem Benutzer fortsetzen können.</span><span class="sxs-lookup"><span data-stu-id="2e9a6-137">If the system detects user activity (such as a mouse click), the ResumeSuspend message will be broadcast, letting applications know that they can resume full interactivity with the user.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2e9a6-138">**"OEMEventCode"**</span><span class="sxs-lookup"><span data-stu-id="2e9a6-138">**OEMEventCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e9a6-139">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2e9a6-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2e9a6-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2e9a6-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e9a6-141">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Energie Verwaltungs Ereignisse")</span><span class="sxs-lookup"><span data-stu-id="2e9a6-141">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Power Management Events")</span></span>
</dt> </dl>

<span data-ttu-id="2e9a6-142">Der vom Originalgerätehersteller (OEM) definierte System Energiezustand, wenn die **eventType** -Eigenschaft dieser Klasse auf 11 (OEM-Ereignis) festgelegt ist. Andernfalls wird diese Eigenschaft auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2e9a6-142">System power state defined by the original equipment manufacturer (OEM) when the **EventType** property of this class is set to 11 (OEM Event); otherwise, this property is set to **NULL**.</span></span> <span data-ttu-id="2e9a6-143">OEM-Ereignisse werden generiert, wenn ein APM-BIOS ein APM-OEM-Ereignis signalisiert.</span><span class="sxs-lookup"><span data-stu-id="2e9a6-143">OEM events are generated when an APM BIOS signals an APM OEM event.</span></span> <span data-ttu-id="2e9a6-144">OEM-Ereignis Codes liegen im Bereich 0x0200h-0x02ffh.</span><span class="sxs-lookup"><span data-stu-id="2e9a6-144">OEM event codes are in the range 0x0200h - 0x02FFh.</span></span>

</dd> <dt>

<span data-ttu-id="2e9a6-145">**Sicherheits \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2e9a6-145">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e9a6-146">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="2e9a6-146">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="2e9a6-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2e9a6-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e9a6-148">Deskriptor, der vom Ereignis Anbieter verwendet wird, um zu bestimmen, welche Benutzer das Ereignis empfangen können.</span><span class="sxs-lookup"><span data-stu-id="2e9a6-148">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="2e9a6-149">Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](../wmisdk/--event.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2e9a6-149">This property is inherited from [**\_\_Event**](../wmisdk/--event.md).</span></span> <span data-ttu-id="2e9a6-150">Weitere Informationen zu Konstanten, die verwendet werden, um diese Sicherheits Beschreibung festzulegen, finden Sie unter [WMI-Sicherheits Konstanten](../wmisdk/wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="2e9a6-150">For more information about constants used to set this security descriptor, see [WMI Security Constants](../wmisdk/wmi-security-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e9a6-151">**\_Erstellungszeit**</span><span class="sxs-lookup"><span data-stu-id="2e9a6-151">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e9a6-152">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2e9a6-152">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2e9a6-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2e9a6-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e9a6-154">Eindeutiger Wert, der die Uhrzeit angibt, zu der das Ereignis generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="2e9a6-154">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="2e9a6-155">Dies ist ein 64-Bit-Wert, der die Anzahl der 100-Nanosecond-Intervalle nach dem 1. Januar 1601 darstellt.</span><span class="sxs-lookup"><span data-stu-id="2e9a6-155">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="2e9a6-156">Die Informationen liegen im UTC-Format (koordiniert Universal Times) vor.</span><span class="sxs-lookup"><span data-stu-id="2e9a6-156">The information is in the Coordinated Universal Times (UTC) format.</span></span>

<span data-ttu-id="2e9a6-157">Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](../wmisdk/--event.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2e9a6-157">This property is inherited from [**\_\_Event**](../wmisdk/--event.md).</span></span>

<span data-ttu-id="2e9a6-158">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="2e9a6-158">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2e9a6-159">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2e9a6-159">Remarks</span></span>

<span data-ttu-id="2e9a6-160">Die Win32-Klasse " **\_ powermanagementevent** " ist von " [**\_ \_ ExtrinsicEvent**](../wmisdk/--extrinsicevent.md)" abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="2e9a6-160">The **Win32\_PowerManagementEvent** class is derived from [**\_\_ExtrinsicEvent**](../wmisdk/--extrinsicevent.md).</span></span>

<span data-ttu-id="2e9a6-161">Änderungen am Energiestatus weisen häufig darauf hin, dass ein Problem mit einem Computer oder mit einem anderen verwalteten Gerät aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="2e9a6-161">Changes in power status often indicate that a problem has occurred with a computer or with another managed device.</span></span> <span data-ttu-id="2e9a6-162">Wenn ein Server plötzlich von der Stromversorgung zu einer unterbrechungsfreien Stromversorgung wechselt, kann diese Änderung darauf hindeuten, dass ein elektrisches Problem aufgetreten ist, entweder mit dem Computer selbst oder mit dem elektrischen System in dem Raum, in dem der Computer aufbewahrt wird.</span><span class="sxs-lookup"><span data-stu-id="2e9a6-162">If a server suddenly switches from AC power to an uninterruptible power supply, this change can indicate that an electrical problem of some kind has occurred, either with the computer itself or with the electrical system in the room in which the computer is kept.</span></span>

<span data-ttu-id="2e9a6-163">Administratoren müssen diese Änderungen im Energiestatus überwachen und sofort über solche Änderungen benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="2e9a6-163">Administrators need to monitor these changes in power status and be notified of such changes immediately.</span></span> <span data-ttu-id="2e9a6-164">Dadurch können Sie Maßnahmen ergreifen, bevor das Gerät die Stromversorgung vollständig verliert.</span><span class="sxs-lookup"><span data-stu-id="2e9a6-164">This enables them to take action before the device loses power entirely.</span></span> <span data-ttu-id="2e9a6-165">(Unterbrechungsfreie Stromversorgungssysteme können z. b. nur für 15 Minuten oder vor dem Herunterfahren ausgeführt werden.)</span><span class="sxs-lookup"><span data-stu-id="2e9a6-165">(Uninterruptible power supply systems, for example, might run for only 15 minutes or so before shutting down.)</span></span>

<span data-ttu-id="2e9a6-166">Die Win32-Klasse " **\_ powermanagementevent** " kann verwendet werden, um Änderungen des Energiestatus auf einem Computer zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="2e9a6-166">The **Win32\_PowerManagementEvent** class can be used to monitor changes in power status on a computer.</span></span> <span data-ttu-id="2e9a6-167">Diese Änderungen können einen Wechsel von einer Stromquelle zu einer anderen und eine Änderung des Energie Zustands des Computers (z. b. Eingabe oder Beenden des anhaltemodus) einschließen.</span><span class="sxs-lookup"><span data-stu-id="2e9a6-167">These changes can include a switch from one power source to another as well as a change in computer power state (for example, entering or exiting Suspend mode).</span></span>

<span data-ttu-id="2e9a6-168">Die Win32-Klasse " **\_ powermanagementevent** " hat nur zwei Eigenschaften: EventType, mit dem der Typ des aufgetretenen Energie Änderungs Ereignisses angegeben wird, und "oemeventtype", der von einigen Originalgeräte Herstellern verwendet wird, um zusätzliche Energie Änderungs Ereignisse zu definieren.</span><span class="sxs-lookup"><span data-stu-id="2e9a6-168">The **Win32\_PowerManagementEvent** class has only two properties: EventType, used to indicate the type of power change event that occurred, and OEMEventType, which is used by some original equipment manufacturers to define additional power change events.</span></span>

<span data-ttu-id="2e9a6-169">Weitere Informationen zum reagieren auf Windows-Energie Ereignisse finden Sie im Artikel [überwachen und reagieren auf Windows powerevents mit PowerShell](https://blogs.technet.com/b/heyscriptingguy/archive/2011/08/16/monitor-and-respond-to-windows-power-events-with-powershell.aspx) auf der</span><span class="sxs-lookup"><span data-stu-id="2e9a6-169">For more information on responding to Windows power events, see the [Monitor and Respond to Windows Power Events with PowerShell](https://blogs.technet.com/b/heyscriptingguy/archive/2011/08/16/monitor-and-respond-to-windows-power-events-with-powershell.aspx) article on the Hey!</span></span> <span data-ttu-id="2e9a6-170">Scripting Guy!</span><span class="sxs-lookup"><span data-stu-id="2e9a6-170">Scripting Guy!</span></span> <span data-ttu-id="2e9a6-171">.</span><span class="sxs-lookup"><span data-stu-id="2e9a6-171">blog.</span></span>

## <a name="examples"></a><span data-ttu-id="2e9a6-172">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2e9a6-172">Examples</span></span>

<span data-ttu-id="2e9a6-173">Das folgende VBScript überwacht die Änderungen des Energiestatus auf einem Computer.</span><span class="sxs-lookup"><span data-stu-id="2e9a6-173">The following VBScript monitors changes in power status on a computer.</span></span>


```VB
Set colMonitoredEvents = GetObject("winmgmts:")._
 ExecNotificationQuery("SELECT * FROM Win32_PowerManagementEvent")
Do
 Set strLatestEvent = colMonitoredEvents.NextEvent
 Wscript.Echo strLatestEvent.EventType
Loop
```



## <a name="requirements"></a><span data-ttu-id="2e9a6-174">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2e9a6-174">Requirements</span></span>



| <span data-ttu-id="2e9a6-175">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2e9a6-175">Requirement</span></span> | <span data-ttu-id="2e9a6-176">Wert</span><span class="sxs-lookup"><span data-stu-id="2e9a6-176">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e9a6-177">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2e9a6-177">Minimum supported client</span></span><br/> | <span data-ttu-id="2e9a6-178">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2e9a6-178">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2e9a6-179">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2e9a6-179">Minimum supported server</span></span><br/> | <span data-ttu-id="2e9a6-180">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2e9a6-180">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2e9a6-181">Namespace</span><span class="sxs-lookup"><span data-stu-id="2e9a6-181">Namespace</span></span><br/>                | <span data-ttu-id="2e9a6-182">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="2e9a6-182">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2e9a6-183">MOF</span><span class="sxs-lookup"><span data-stu-id="2e9a6-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2e9a6-184"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2e9a6-184"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2e9a6-185">DLL</span><span class="sxs-lookup"><span data-stu-id="2e9a6-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e9a6-186"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e9a6-186"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e9a6-187">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2e9a6-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e9a6-188">**\_\_ExtrinsicEvent**</span><span class="sxs-lookup"><span data-stu-id="2e9a6-188">**\_\_ExtrinsicEvent**</span></span>](../wmisdk/--extrinsicevent.md)
</dt> <dt>

[<span data-ttu-id="2e9a6-189">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="2e9a6-189">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

<span data-ttu-id="2e9a6-190">[Überwachen von Änderungen im Energie Status des Computers](/previous-versions/tn-archive/ee176537(v=technet.10))</span><span class="sxs-lookup"><span data-stu-id="2e9a6-190">[Monitoring Changes in Computer Power Status](/previous-versions/tn-archive/ee176537(v=technet.10))</span></span>
</dt> </dl>

 

 
