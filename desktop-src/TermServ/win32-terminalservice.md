---
title: Win32_TerminalService-Klasse
description: Eine Unterklasse der Win32- \_ Dienstklasse. Win32 \_ Terminalservice stellt die-Element Eigenschaft der Win32 \_ terminalservicedesetting-Zuordnung dar.
ms.assetid: 06c69d71-4e6f-48af-b13d-e593b8fcf376
ms.tgt_platform: multiple
keywords:
- Win32_TerminalService-Klasse Remotedesktopdienste
- Win32_TerminalService Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TerminalService
- Win32_TerminalService.AcceptPause
- Win32_TerminalService.AcceptStop
- Win32_TerminalService.Caption
- Win32_TerminalService.CheckPoint
- Win32_TerminalService.CreationClassName
- Win32_TerminalService.DelayedAutoStart
- Win32_TerminalService.Description
- Win32_TerminalService.DesktopInteract
- Win32_TerminalService.DisplayName
- Win32_TerminalService.ErrorControl
- Win32_TerminalService.ExitCode
- Win32_TerminalService.InstallDate
- Win32_TerminalService.Name
- Win32_TerminalService.PathName
- Win32_TerminalService.ProcessId
- Win32_TerminalService.ServiceSpecificExitCode
- Win32_TerminalService.ServiceType
- Win32_TerminalService.Started
- Win32_TerminalService.StartMode
- Win32_TerminalService.StartName
- Win32_TerminalService.State
- Win32_TerminalService.Status
- Win32_TerminalService.SystemCreationClassName
- Win32_TerminalService.SystemName
- Win32_TerminalService.TagId
- Win32_TerminalService.WaitHint
- Win32_TerminalService.DisconnectedSessions
- Win32_TerminalService.TotalSessions
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba5646c6ac9abf41fddc023ad39884e611681a71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478843"
---
# <a name="win32_terminalservice-class"></a><span data-ttu-id="b56b7-106">Win32 \_ Terminalservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="b56b7-106">Win32\_TerminalService class</span></span>

<span data-ttu-id="b56b7-107">Die **Win32 \_ Terminalservice** -WMI-Klasse ist eine Unterklasse der [**Win32- \_ Dienst**](/windows/desktop/CIMWin32Prov/win32-service) Klasse.</span><span class="sxs-lookup"><span data-stu-id="b56b7-107">The **Win32\_TerminalService** WMI class is a subclass of the [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) class.</span></span> <span data-ttu-id="b56b7-108">**Win32 \_ Terminalservice** stellt die- **Element** Eigenschaft der [**Win32 \_ terminalservicedesetting**](win32-terminalservicetosetting.md) -Zuordnung dar.</span><span class="sxs-lookup"><span data-stu-id="b56b7-108">**Win32\_TerminalService** represents the **Element** property of the [**Win32\_TerminalServiceToSetting**](win32-terminalservicetosetting.md) association.</span></span>

<span data-ttu-id="b56b7-109">Die folgende Syntax wird aus dem MOF-Code vereinfacht und umfasst alle definierten und geerbten Eigenschaften in alphabetischer Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="b56b7-109">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b56b7-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="b56b7-110">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TERMINALSERVICE_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer"), AMENDMENT]
class Win32_TerminalService : Win32_Service
{
  boolean  AcceptPause;
  boolean  AcceptStop;
  string   Caption;
  uint32   CheckPoint;
  string   CreationClassName;
  boolean  DelayedAutoStart;
  string   Description;
  boolean  DesktopInteract;
  string   DisplayName;
  string   ErrorControl;
  uint32   ExitCode;
  datetime InstallDate;
  string   Name;
  string   PathName;
  uint32   ProcessId;
  uint32   ServiceSpecificExitCode;
  string   ServiceType;
  boolean  Started;
  string   StartMode;
  string   StartName;
  string   State;
  string   Status;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   TagId;
  uint32   WaitHint;
  uint32   DisconnectedSessions;
  uint32   TotalSessions;
};
```

## <a name="members"></a><span data-ttu-id="b56b7-111">Member</span><span class="sxs-lookup"><span data-stu-id="b56b7-111">Members</span></span>

<span data-ttu-id="b56b7-112">Die **Win32 \_ Terminalservice** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b56b7-112">The **Win32\_TerminalService** class has these types of members:</span></span>

-   [<span data-ttu-id="b56b7-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="b56b7-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="b56b7-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b56b7-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b56b7-115">Methoden</span><span class="sxs-lookup"><span data-stu-id="b56b7-115">Methods</span></span>

<span data-ttu-id="b56b7-116">Die **Win32 \_ Terminalservice** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="b56b7-116">The **Win32\_TerminalService** class has these methods.</span></span>



| <span data-ttu-id="b56b7-117">Methode</span><span class="sxs-lookup"><span data-stu-id="b56b7-117">Method</span></span>                                                                       | <span data-ttu-id="b56b7-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b56b7-118">Description</span></span>                                                                                          |
|:-----------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b56b7-119">**Klima**</span><span class="sxs-lookup"><span data-stu-id="b56b7-119">**Change**</span></span>](win32-terminalservice-change.md)                               | <span data-ttu-id="b56b7-120">Ändert einen Dienst.</span><span class="sxs-lookup"><span data-stu-id="b56b7-120">Modifies a service.</span></span><br/>                                                                       |
| [<span data-ttu-id="b56b7-121">**ChangeStartMode**</span><span class="sxs-lookup"><span data-stu-id="b56b7-121">**ChangeStartMode**</span></span>](win32-terminalservice-changestartmode.md)             | <span data-ttu-id="b56b7-122">Ändert den Start Modus eines Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="b56b7-122">Modifies the start mode of a service.</span></span><br/>                                                     |
| [<span data-ttu-id="b56b7-123">**Stelle**</span><span class="sxs-lookup"><span data-stu-id="b56b7-123">**Create**</span></span>](win32-terminalservice-create.md)                               | <span data-ttu-id="b56b7-124">Erstellt einen neuen Dienst.</span><span class="sxs-lookup"><span data-stu-id="b56b7-124">Creates a new service.</span></span><br/>                                                                    |
| [<span data-ttu-id="b56b7-125">**Lösch**</span><span class="sxs-lookup"><span data-stu-id="b56b7-125">**Delete**</span></span>](win32-terminalservice-delete.md)                               | <span data-ttu-id="b56b7-126">Löscht einen vorhandenen Dienst.</span><span class="sxs-lookup"><span data-stu-id="b56b7-126">Deletes an existing service.</span></span><br/>                                                              |
| [<span data-ttu-id="b56b7-127">**GetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="b56b7-127">**GetSecurityDescriptor**</span></span>](win32-terminalservice-getsecuritydescriptor.md) | <span data-ttu-id="b56b7-128">Gibt die Sicherheits Beschreibung zurück, die den Zugriff auf den Dienst steuert.</span><span class="sxs-lookup"><span data-stu-id="b56b7-128">Returns the security descriptor that controls access to the service.</span></span><br/>                      |
| [<span data-ttu-id="b56b7-129">**"InterrogateService"**</span><span class="sxs-lookup"><span data-stu-id="b56b7-129">**InterrogateService**</span></span>](win32-terminalservice-interrogateservice.md)       | <span data-ttu-id="b56b7-130">Fordert an, dass ein Dienst seinen Status auf den Dienst-Manager aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="b56b7-130">Requests that a service update its state to the service manager.</span></span><br/>                          |
| [<span data-ttu-id="b56b7-131">**PauseService**</span><span class="sxs-lookup"><span data-stu-id="b56b7-131">**PauseService**</span></span>](win32-terminalservice-pauseservice.md)                   | <span data-ttu-id="b56b7-132">Versucht, einen Dienst in den angehaltenen Zustand zu versetzen.</span><span class="sxs-lookup"><span data-stu-id="b56b7-132">Attempts to place a service in the paused state.</span></span><br/>                                          |
| [<span data-ttu-id="b56b7-133">**ResumeService**</span><span class="sxs-lookup"><span data-stu-id="b56b7-133">**ResumeService**</span></span>](win32-terminalservice-resumeservice.md)                 | <span data-ttu-id="b56b7-134">Versucht, einen Dienst in den Status "wieder aufgenommen" zu versetzen.</span><span class="sxs-lookup"><span data-stu-id="b56b7-134">Attempts to place a service in the resumed state.</span></span><br/>                                         |
| [<span data-ttu-id="b56b7-135">**SETSECURITYDESCRIPTOR**</span><span class="sxs-lookup"><span data-stu-id="b56b7-135">**SetSecurityDescriptor**</span></span>](win32-terminalservice-setsecuritydescriptor.md) | <span data-ttu-id="b56b7-136">Schreibt eine aktualisierte Version der Sicherheits Beschreibung, die den Zugriff auf den Dienst steuert.</span><span class="sxs-lookup"><span data-stu-id="b56b7-136">Writes an updated version of the security descriptor that controls access to the service.</span></span><br/> |
| [<span data-ttu-id="b56b7-137">**Start Service**</span><span class="sxs-lookup"><span data-stu-id="b56b7-137">**StartService**</span></span>](win32-terminalservice-startservice.md)                   | <span data-ttu-id="b56b7-138">Versucht, einen Dienst in den Startzustand zu versetzen.</span><span class="sxs-lookup"><span data-stu-id="b56b7-138">Attempts to place a service into the startup state.</span></span><br/>                                       |
| [<span data-ttu-id="b56b7-139">**Stop Service**</span><span class="sxs-lookup"><span data-stu-id="b56b7-139">**StopService**</span></span>](win32-terminalservice-stopservice.md)                     | <span data-ttu-id="b56b7-140">Versetzt einen Dienst in den Status "beendet".</span><span class="sxs-lookup"><span data-stu-id="b56b7-140">Places a service in the stopped state.</span></span><br/>                                                    |
| [<span data-ttu-id="b56b7-141">**UserControlService**</span><span class="sxs-lookup"><span data-stu-id="b56b7-141">**UserControlService**</span></span>](win32-terminalservice-usercontrolservice.md)       | <span data-ttu-id="b56b7-142">Versucht, einen benutzerdefinierten Steuerelement Code an einen Dienst zu senden.</span><span class="sxs-lookup"><span data-stu-id="b56b7-142">Attempts to send a user-defined control code to a service.</span></span><br/>                                |



 

### <a name="properties"></a><span data-ttu-id="b56b7-143">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b56b7-143">Properties</span></span>

<span data-ttu-id="b56b7-144">Die **Win32 \_ Terminalservice** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b56b7-144">The **Win32\_TerminalService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b56b7-145">**AcceptPause**</span><span class="sxs-lookup"><span data-stu-id="b56b7-145">**AcceptPause**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b56b7-146">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b56b7-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b56b7-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b56b7-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b56b7-148">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API Service \| Structures \| [**Service \_ Status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwcontrolsaccepted \| Service \_ Accept \_ Pause \_ Continue"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Accept Pause")</span><span class="sxs-lookup"><span data-stu-id="b56b7-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwControlsAccepted\|SERVICE\_ACCEPT\_PAUSE\_CONTINUE"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Accepts Pause")</span></span>
</dt> </dl>

<span data-ttu-id="b56b7-149">Gibt an, ob der Dienst angehalten werden kann.</span><span class="sxs-lookup"><span data-stu-id="b56b7-149">Indicates whether the service can be paused.</span></span>

<span data-ttu-id="b56b7-150">Diese Eigenschaft wird von [**Win32 \_ baseservice**](/windows/desktop/CIMWin32Prov/win32-baseservice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b56b7-150">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="b56b7-151">**AcceptStop**</span><span class="sxs-lookup"><span data-stu-id="b56b7-151">**AcceptStop**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b56b7-152">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b56b7-152">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b56b7-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b56b7-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b56b7-154">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API Service \| Structures \| [**Service \_ Status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwcontrolsaccepted \| Service \_ Accept End \_ "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("der Dienst akzeptiert das Ende")</span><span class="sxs-lookup"><span data-stu-id="b56b7-154">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwControlsAccepted\|SERVICE\_ACCEPT\_STOP"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Accepts Stop")</span></span>
</dt> </dl>

<span data-ttu-id="b56b7-155">Gibt an, ob der Dienst beendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="b56b7-155">Indicates whether the service can be stopped.</span></span>

<span data-ttu-id="b56b7-156">Diese Eigenschaft wird von [**Win32 \_ baseservice**](/windows/desktop/CIMWin32Prov/win32-baseservice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b56b7-156">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="b56b7-157">**Caption**</span><span class="sxs-lookup"><span data-stu-id="b56b7-157">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b56b7-158">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b56b7-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b56b7-159">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b56b7-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b56b7-160">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="b56b7-160">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="b56b7-161">Kurze Beschreibung des Dienes für eine einzeilige Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="b56b7-161">Short description of the service  a one-line string.</span></span>

<span data-ttu-id="b56b7-162">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b56b7-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b56b7-163">**Kal**</span><span class="sxs-lookup"><span data-stu-id="b56b7-163">**CheckPoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b56b7-164">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b56b7-164">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b56b7-165">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b56b7-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b56b7-166">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Service \_ Status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwcheck"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Check Point count")</span><span class="sxs-lookup"><span data-stu-id="b56b7-166">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwCheckPoint"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Check Point Count")</span></span>
</dt> </dl>

<span data-ttu-id="b56b7-167">Der Wert, den der Dienst in regelmäßigen Abständen erhöht, um den Fortschritt während eines langen Starts, Anhaltevorgangs, anhalten oder fortsetzen zu melden.</span><span class="sxs-lookup"><span data-stu-id="b56b7-167">Value that the service increments periodically to report its progress during a long start, stop, pause, or continue operation.</span></span> <span data-ttu-id="b56b7-168">Der Dienst erhöht z. b. diesen Wert, da er die einzelnen Schritte seiner Initialisierung beim Starten abschließt.</span><span class="sxs-lookup"><span data-stu-id="b56b7-168">For example, the service increments this value as it completes each step of its initialization when it is starting up.</span></span> <span data-ttu-id="b56b7-169">Das Benutzeroberflächen Programm, das den-Vorgang für den Dienst aufruft, verwendet diesen Wert, um den Status des Dienstanbieter während eines langwierigen Vorgangs zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="b56b7-169">The user interface program that invokes the operation on the service uses this value to track the progress of the service during a lengthy operation.</span></span> <span data-ttu-id="b56b7-170">Dieser Wert ist ungültig und sollte NULL sein, wenn der Dienst nicht über einen Vorgang zum Starten, beenden, anhalten oder fortsetzen verfügt.</span><span class="sxs-lookup"><span data-stu-id="b56b7-170">This value is not valid and should be zero when the service does not have a start, stop, pause, or continue operation pending.</span></span>

<span data-ttu-id="b56b7-171">Diese Eigenschaft wird vom [**Win32- \_ Dienst**](/windows/desktop/CIMWin32Prov/win32-service)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b56b7-171">This property is inherited from [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span>

</dd> <dt>

<span data-ttu-id="b56b7-172">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="b56b7-172">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b56b7-173">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b56b7-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b56b7-174">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b56b7-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b56b7-175">Qualifizierer: [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span><span class="sxs-lookup"><span data-stu-id="b56b7-175">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="b56b7-176">Der Name der ersten konkreten Klasse, die in der Vererbungs Kette angezeigt werden soll, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b56b7-176">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="b56b7-177">Wenn diese Eigenschaft mit den anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="b56b7-177">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="b56b7-178">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b56b7-178">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="b56b7-179">**DelayedAutoStart**</span><span class="sxs-lookup"><span data-stu-id="b56b7-179">**DelayedAutoStart**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b56b7-180">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b56b7-180">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b56b7-181">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b56b7-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b56b7-182">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Service \_ verzögert \_ Auto \_ Start \_ Info**](/windows/desktop/api/winsvc/ns-winsvc-service_delayed_auto_start_info) \| f delayedautostart"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("verzögerter automatischer Start")</span><span class="sxs-lookup"><span data-stu-id="b56b7-182">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_DELAYED\_AUTO\_START\_INFO**](/windows/desktop/api/winsvc/ns-winsvc-service_delayed_auto_start_info)\|fDelayedAutostart"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Delayed Auto-Start")</span></span>
</dt> </dl>

<span data-ttu-id="b56b7-183">**True** gibt an, dass der Dienst gestartet wird, nachdem andere automatischen Start Dienste und eine kurze Verzögerung gestartet wurden.</span><span class="sxs-lookup"><span data-stu-id="b56b7-183">If **True**, the service is started after other auto-start services are started plus a short delay.</span></span>

<span data-ttu-id="b56b7-184">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Diese Eigenschaft wird vor Windows Server 2016 und Windows 10 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b56b7-184">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows Server 2016 and Windows 10.</span></span>

<span data-ttu-id="b56b7-185">Diese Eigenschaft wird vom [**Win32- \_ Dienst**](/windows/desktop/CIMWin32Prov/win32-service)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b56b7-185">This property is inherited from [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span>

</dd> <dt>

<span data-ttu-id="b56b7-186">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b56b7-186">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b56b7-187">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b56b7-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b56b7-188">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b56b7-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b56b7-189">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="b56b7-189">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="b56b7-190">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="b56b7-190">Description of the object.</span></span>

<span data-ttu-id="b56b7-191">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b56b7-191">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b56b7-192">**DesktopInteract**</span><span class="sxs-lookup"><span data-stu-id="b56b7-192">**DesktopInteract**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b56b7-193">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b56b7-193">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b56b7-194">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b56b7-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b56b7-195">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwservicetype \| Service \_ Interactive \_ Process"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("interagiert with Desktop")</span><span class="sxs-lookup"><span data-stu-id="b56b7-195">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|dwServiceType\|SERVICE\_INTERACTIVE\_PROCESS"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Interacts With Desktop")</span></span>
</dt> </dl>

<span data-ttu-id="b56b7-196">Gibt an, ob der Dienst Windows auf dem Desktop erstellen oder mit ihm kommunizieren kann, sodass er auf irgendeine Weise mit einem Benutzer interagieren kann.</span><span class="sxs-lookup"><span data-stu-id="b56b7-196">Indicates whether the service can create or communicate with windows on the desktop, and thus interact in some way with a user.</span></span> <span data-ttu-id="b56b7-197">Interaktive Dienste müssen unter dem lokalen System Konto ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b56b7-197">Interactive services must run under the Local System account.</span></span> <span data-ttu-id="b56b7-198">Die meisten Dienste sind nicht interaktiv. Das heißt, Sie kommunizieren in keiner Weise mit dem Benutzer.</span><span class="sxs-lookup"><span data-stu-id="b56b7-198">Most services are not interactive; that is, they do not communicate with the user in any way.</span></span>

<span data-ttu-id="b56b7-199">Diese Eigenschaft wird von [**Win32 \_ baseservice**](/windows/desktop/CIMWin32Prov/win32-baseservice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b56b7-199">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="b56b7-200">**Disconnectedsessions**</span><span class="sxs-lookup"><span data-stu-id="b56b7-200">**DisconnectedSessions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b56b7-201">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b56b7-201">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b56b7-202">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b56b7-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b56b7-203">Die Anzahl der getrennten Sitzungen auf dem aktuellen Server.</span><span class="sxs-lookup"><span data-stu-id="b56b7-203">The number of disconnected sessions on the current server.</span></span> <span data-ttu-id="b56b7-204">Diese Sitzungen verbrauchen möglicherweise weiterhin Server Ressourcen, aber Sie verfügen derzeit über keine Netzwerkverbindung mit einem Client.</span><span class="sxs-lookup"><span data-stu-id="b56b7-204">These sessions may still be actively consuming server resources, however they currently have no network connection with a client.</span></span>

</dd> <dt>

<span data-ttu-id="b56b7-205">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="b56b7-205">**DisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b56b7-206">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b56b7-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b56b7-207">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b56b7-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b56b7-208">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| lpdisplayname"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Anzeige Name")</span><span class="sxs-lookup"><span data-stu-id="b56b7-208">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|lpDisplayName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Display Name")</span></span>
</dt> </dl>

<span data-ttu-id="b56b7-209">Der Name des Diensts, wie im Dienste-Snap-in angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b56b7-209">Name of the service as viewed in the Services snap-in.</span></span> <span data-ttu-id="b56b7-210">Die maximale Länge der Zeichenfolge beträgt 256 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="b56b7-210">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="b56b7-211">Beachten Sie, dass der Anzeige Name und der Dienst Name (der in der Registrierung gespeichert ist) nicht immer identisch sind.</span><span class="sxs-lookup"><span data-stu-id="b56b7-211">Note that the display name and the service name (which is stored in the registry) are not always the same.</span></span> <span data-ttu-id="b56b7-212">Der DHCP-Client Dienst hat z. b. den Dienstnamen DHCP, aber den anzeigen Amen DHCP-Client.</span><span class="sxs-lookup"><span data-stu-id="b56b7-212">For example, the DHCP Client service has the service name Dhcp but the display name DHCP Client.</span></span> <span data-ttu-id="b56b7-213">Der Name wird im Dienststeuerungs-Manager nach Groß-/Kleinschreibung beibehalten.</span><span class="sxs-lookup"><span data-stu-id="b56b7-213">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="b56b7-214">Bei [**DisplayName**](/windows/desktop/CIMWin32Prov/win32-service) -vergleichen wird jedoch immer die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="b56b7-214">However, [**DisplayName**](/windows/desktop/CIMWin32Prov/win32-service) comparisons are always case-insensitive.</span></span>

<span data-ttu-id="b56b7-215">Einschränkung: akzeptiert denselben Wert wie die [**Name**](/windows/desktop/CIMWin32Prov/win32-service) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="b56b7-215">Constraint: Accepts the same value as the [**Name**](/windows/desktop/CIMWin32Prov/win32-service) property.</span></span>

<span data-ttu-id="b56b7-216">Beispiel: "ATDISK"</span><span class="sxs-lookup"><span data-stu-id="b56b7-216">Example: "Atdisk"</span></span>

<span data-ttu-id="b56b7-217">Diese Eigenschaft wird von [**Win32 \_ baseservice**](/windows/desktop/CIMWin32Prov/win32-baseservice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b56b7-217">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="b56b7-218">**ErrorControl**</span><span class="sxs-lookup"><span data-stu-id="b56b7-218">**ErrorControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b56b7-219">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b56b7-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b56b7-220">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b56b7-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b56b7-221">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwerrorcontrol"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Schweregrad des Start Fehlers")</span><span class="sxs-lookup"><span data-stu-id="b56b7-221">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|dwErrorControl"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Severity Of Startup Failure")</span></span>
</dt> </dl>

<span data-ttu-id="b56b7-222">Der Schweregrad des Fehlers, wenn dieser Dienst während des Starts nicht gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="b56b7-222">Severity of the error if this service fails to start during startup.</span></span> <span data-ttu-id="b56b7-223">Der Wert gibt die vom Start Programm ausgeführte Aktion an, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="b56b7-223">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="b56b7-224">Alle Fehler werden vom Computersystem protokolliert.</span><span class="sxs-lookup"><span data-stu-id="b56b7-224">All errors are logged by the computer system.</span></span>

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span data-ttu-id="b56b7-225"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignorieren** ("ignorieren")</span><span class="sxs-lookup"><span data-stu-id="b56b7-225"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignore** ("Ignore")</span></span>


</dt> <dd>

<span data-ttu-id="b56b7-226">Der Benutzer wird nicht benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="b56b7-226">User is not notified.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="b56b7-227"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** ("Normal")</span><span class="sxs-lookup"><span data-stu-id="b56b7-227"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** ("Normal")</span></span>


</dt> <dd>

<span data-ttu-id="b56b7-228">Der Benutzer wird benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="b56b7-228">User is notified.</span></span> <span data-ttu-id="b56b7-229">Normalerweise ist dies ein Meldungs Feld, in dem der Benutzer über das Problem benachrichtigt wird.</span><span class="sxs-lookup"><span data-stu-id="b56b7-229">Usually this will be a message box display notifying the user of the problem.</span></span>

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span data-ttu-id="b56b7-230"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Schwerwiegend** ("schwerwiegend")</span><span class="sxs-lookup"><span data-stu-id="b56b7-230"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Severe** ("Severe")</span></span>


</dt> <dd>

<span data-ttu-id="b56b7-231">Das System wird mit der letzten bekannten, fehlerfreien Konfiguration neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="b56b7-231">System is restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="b56b7-232"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Kritisch** ("kritisch")</span><span class="sxs-lookup"><span data-stu-id="b56b7-232"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** ("Critical")</span></span>


</dt> <dd>

<span data-ttu-id="b56b7-233">Das System versucht, mit einer fehlerfreien Konfiguration zu neu starten.</span><span class="sxs-lookup"><span data-stu-id="b56b7-233">System attempts to restart with a good configuration.</span></span> <span data-ttu-id="b56b7-234">Wenn der Dienst nicht ein zweites Mal gestartet werden kann, schlägt der Startvorgang fehl.</span><span class="sxs-lookup"><span data-stu-id="b56b7-234">If the service fails to start a second time, startup fails.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b56b7-235"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="b56b7-235"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** ("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="b56b7-236">Der Schweregrad des Fehlers ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="b56b7-236">Severity of the error is unknown.</span></span>

</dd> </dl>

<span data-ttu-id="b56b7-237">Diese Eigenschaft wird von [**Win32 \_ baseservice**](/windows/desktop/CIMWin32Prov/win32-baseservice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b56b7-237">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="b56b7-238">**Exitcode**</span><span class="sxs-lookup"><span data-stu-id="b56b7-238">**ExitCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b56b7-239">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b56b7-239">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b56b7-240">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b56b7-240">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b56b7-241">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Service \_ Status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwWin32ExitCode"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Exitcode")</span><span class="sxs-lookup"><span data-stu-id="b56b7-241">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwWin32ExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Exit Code")</span></span>
</dt> </dl>

<span data-ttu-id="b56b7-242">Windows-Fehlercode, der Fehler definiert, die beim Starten oder Beenden des Dienstes aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="b56b7-242">Windows error code that defines errors encountered in starting or stopping the service.</span></span> <span data-ttu-id="b56b7-243">Diese Eigenschaft ist auf **Fehler \_ Dienst \_ spezifischer \_ Fehler** (1066) festgelegt, wenn der Fehler für den Dienst eindeutig ist, der durch diese Klasse dargestellt wird. Informationen über den Fehler sind in der [**ServiceSpecificExitCode**](/windows/desktop/CIMWin32Prov/win32-service) -Eigenschaft verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b56b7-243">This property is set to **ERROR\_SERVICE\_SPECIFIC\_ERROR** (1066) when the error is unique to the service represented by this class, and information about the error is available in the [**ServiceSpecificExitCode**](/windows/desktop/CIMWin32Prov/win32-service) property.</span></span> <span data-ttu-id="b56b7-244">Der Dienst legt diesen Wert bei der Ausführung und erneut bei normaler Beendigung auf **keinen \_ Fehler** fest.</span><span class="sxs-lookup"><span data-stu-id="b56b7-244">The service sets this value to **NO\_ERROR** when running, and again upon normal termination.</span></span>

<span data-ttu-id="b56b7-245">Diese Eigenschaft wird von [**Win32 \_ baseservice**](/windows/desktop/CIMWin32Prov/win32-baseservice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b56b7-245">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="b56b7-246">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b56b7-246">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b56b7-247">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="b56b7-247">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b56b7-248">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b56b7-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b56b7-249">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="b56b7-249">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="b56b7-250">Date-Objekt ist installiert.</span><span class="sxs-lookup"><span data-stu-id="b56b7-250">Date object is installed.</span></span> <span data-ttu-id="b56b7-251">Diese Eigenschaft erfordert keinen Wert, um anzugeben, dass das-Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="b56b7-251">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="b56b7-252">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b56b7-252">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b56b7-253">**Name**</span><span class="sxs-lookup"><span data-stu-id="b56b7-253">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b56b7-254">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b56b7-254">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b56b7-255">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b56b7-255">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b56b7-256">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b56b7-256">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b56b7-257">Eindeutiger Bezeichner des dienstanweises, der angibt, welche Funktionen verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="b56b7-257">Unique identifier of the service that provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="b56b7-258">Diese Funktionalität wird in der [**Description**](/windows/desktop/CIMWin32Prov/win32-service) -Eigenschaft des-Objekts beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b56b7-258">This functionality is described in the [**Description**](/windows/desktop/CIMWin32Prov/win32-service) property of the object.</span></span>

<span data-ttu-id="b56b7-259">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b56b7-259">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b56b7-260">**PathName**</span><span class="sxs-lookup"><span data-stu-id="b56b7-260">**PathName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b56b7-261">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b56b7-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b56b7-262">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b56b7-262">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b56b7-263">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| lpbinarypathname"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dateipfadname")</span><span class="sxs-lookup"><span data-stu-id="b56b7-263">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|lpBinaryPathName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Path Name")</span></span>
</dt> </dl>

<span data-ttu-id="b56b7-264">Der voll qualifizierte Pfad der Dienst Binärdatei, die den Dienst implementiert.</span><span class="sxs-lookup"><span data-stu-id="b56b7-264">Fully qualified path to the service binary file that implements the service.</span></span>

<span data-ttu-id="b56b7-265">Beispiel: " \\ systemroot \\ system32 \\ Drivers \\afd.sys"</span><span class="sxs-lookup"><span data-stu-id="b56b7-265">Example: "\\SystemRoot\\System32\\drivers\\afd.sys"</span></span>

<span data-ttu-id="b56b7-266">Diese Eigenschaft wird von [**Win32 \_ baseservice**](/windows/desktop/CIMWin32Prov/win32-baseservice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b56b7-266">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="b56b7-267">**ProcessId**</span><span class="sxs-lookup"><span data-stu-id="b56b7-267">**ProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b56b7-268">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b56b7-268">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b56b7-269">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b56b7-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b56b7-270">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Service \_ Status \_ Process**](/windows/desktop/api/winsvc/ns-winsvc-service_status_process) \| dwProcessId"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Process ID")</span><span class="sxs-lookup"><span data-stu-id="b56b7-270">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS\_PROCESS**](/windows/desktop/api/winsvc/ns-winsvc-service_status_process)\|dwProcessId"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Process Id")</span></span>
</dt> </dl>

<span data-ttu-id="b56b7-271">Prozess Bezeichner des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="b56b7-271">Process identifier of the service.</span></span>

<span data-ttu-id="b56b7-272">Beispiel: 324</span><span class="sxs-lookup"><span data-stu-id="b56b7-272">Example: 324</span></span>

<span data-ttu-id="b56b7-273">Diese Eigenschaft wird vom [**Win32- \_ Dienst**](/windows/desktop/CIMWin32Prov/win32-service)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b56b7-273">This property is inherited from [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span>

</dd> <dt>

<span data-ttu-id="b56b7-274">**ServiceSpecificExitCode**</span><span class="sxs-lookup"><span data-stu-id="b56b7-274">**ServiceSpecificExitCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b56b7-275">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b56b7-275">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b56b7-276">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b56b7-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b56b7-277">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Service \_ Status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwservicespecificexitcode"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Server spezifischer Exitcode")</span><span class="sxs-lookup"><span data-stu-id="b56b7-277">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwServiceSpecificExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Server Specific Exit Code")</span></span>
</dt> </dl>

<span data-ttu-id="b56b7-278">Dienst spezifischer Fehlercode für Fehler, die auftreten, während der Dienst gestartet oder beendet wird.</span><span class="sxs-lookup"><span data-stu-id="b56b7-278">Service-specific error code for errors that occur while the service is either starting or stopping.</span></span> <span data-ttu-id="b56b7-279">Die Exitcodes werden von dem Dienst definiert, der durch diese Klasse dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="b56b7-279">The exit codes are defined by the service represented by this class.</span></span> <span data-ttu-id="b56b7-280">Dieser Wert wird nur festgelegt, wenn der [**Exitcode**](/windows/desktop/CIMWin32Prov/win32-service) -Eigenschafts Wert **Fehler \_ Dienst \_ spezifisch \_** ist (1066).</span><span class="sxs-lookup"><span data-stu-id="b56b7-280">This value is only set when the [**ExitCode**](/windows/desktop/CIMWin32Prov/win32-service) property value is **ERROR\_SERVICE\_SPECIFIC\_ERROR** (1066).</span></span>

<span data-ttu-id="b56b7-281">Diese Eigenschaft wird von [**Win32 \_ baseservice**](/windows/desktop/CIMWin32Prov/win32-baseservice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b56b7-281">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="b56b7-282">**ServiceType**</span><span class="sxs-lookup"><span data-stu-id="b56b7-282">**ServiceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b56b7-283">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b56b7-283">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b56b7-284">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b56b7-284">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b56b7-285">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwservicetype"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Type")</span><span class="sxs-lookup"><span data-stu-id="b56b7-285">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|dwServiceType"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Type")</span></span>
</dt> </dl>

<span data-ttu-id="b56b7-286">Der für aufrufende Prozesse bereitgestellte Diensttyp.</span><span class="sxs-lookup"><span data-stu-id="b56b7-286">Type of service provided to calling processes.</span></span>

<span data-ttu-id="b56b7-287">Die Werte sind:</span><span class="sxs-lookup"><span data-stu-id="b56b7-287">The values are:</span></span>

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

<span data-ttu-id="b56b7-288">**Kernel Treiber** ("Kernel Treiber")</span><span class="sxs-lookup"><span data-stu-id="b56b7-288">**Kernel Driver** ("Kernel Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

<span data-ttu-id="b56b7-289">**Dateisystem Treiber** ("Dateisystem Treiber")</span><span class="sxs-lookup"><span data-stu-id="b56b7-289">**File System Driver** ("File System Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

<span data-ttu-id="b56b7-290">**Adapter** ("Adapter")</span><span class="sxs-lookup"><span data-stu-id="b56b7-290">**Adapter** ("Adapter")</span></span>


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

<span data-ttu-id="b56b7-291">**Erkennungs Treiber** ("Erkennungs Treiber")</span><span class="sxs-lookup"><span data-stu-id="b56b7-291">**Recognizer Driver** ("Recognizer Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

<span data-ttu-id="b56b7-292">**Eigener Prozess** ("eigener Prozess")</span><span class="sxs-lookup"><span data-stu-id="b56b7-292">**Own Process** ("Own Process")</span></span>


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

<span data-ttu-id="b56b7-293">**Freigabeprozess** ("Freigabeprozess")</span><span class="sxs-lookup"><span data-stu-id="b56b7-293">**Share Process** ("Share Process")</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_Process"></span><span id="interactive_process"></span><span id="INTERACTIVE_PROCESS"></span>

<span data-ttu-id="b56b7-294">**Interaktiver Prozess** ("interaktiver Prozess")</span><span class="sxs-lookup"><span data-stu-id="b56b7-294">**Interactive Process** ("Interactive Process")</span></span>


<span data-ttu-id="b56b7-295"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="b56b7-295"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="b56b7-296">Diese Eigenschaft wird von [**Win32 \_ baseservice**](/windows/desktop/CIMWin32Prov/win32-baseservice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b56b7-296">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="b56b7-297">**Gestartet**</span><span class="sxs-lookup"><span data-stu-id="b56b7-297">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b56b7-298">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b56b7-298">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b56b7-299">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b56b7-299">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b56b7-300">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")</span><span class="sxs-lookup"><span data-stu-id="b56b7-300">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")</span></span>
</dt> </dl>

<span data-ttu-id="b56b7-301">Gibt an, ob der Dienst gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="b56b7-301">Indicates whether or not the service is started.</span></span>

<span data-ttu-id="b56b7-302">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b56b7-302">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="b56b7-303">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="b56b7-303">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b56b7-304">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b56b7-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b56b7-305">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b56b7-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b56b7-306">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Start Modus")</span><span class="sxs-lookup"><span data-stu-id="b56b7-306">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Start Mode")</span></span>
</dt> </dl>

<span data-ttu-id="b56b7-307">Der Start Modus des Windows-Basis Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="b56b7-307">Start mode of the Windows base service.</span></span>

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span data-ttu-id="b56b7-308"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Start** ("Start")</span><span class="sxs-lookup"><span data-stu-id="b56b7-308"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Boot** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="b56b7-309">Der Gerätetreiber wurde vom Betriebssystem Lader gestartet (nur für Treiber Dienste gültig).</span><span class="sxs-lookup"><span data-stu-id="b56b7-309">Device driver started by the operating system loader (valid only for driver services).</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="b56b7-310"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ("System")</span><span class="sxs-lookup"><span data-stu-id="b56b7-310"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="b56b7-311">Der Gerätetreiber wurde durch den Initialisierungs Prozess des Betriebssystems gestartet.</span><span class="sxs-lookup"><span data-stu-id="b56b7-311">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="b56b7-312">Dieses Wert ist nur für Treiberdienste gültig.</span><span class="sxs-lookup"><span data-stu-id="b56b7-312">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>

<span data-ttu-id="b56b7-313"><span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Auto** ("Auto")</span><span class="sxs-lookup"><span data-stu-id="b56b7-313"><span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Auto** ("Auto")</span></span>


</dt> <dd>

<span data-ttu-id="b56b7-314">Der Dienst soll während des Systemstarts automatisch vom Dienstkontroll-Manager gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="b56b7-314">Service to be started automatically by the service control manager during system startup.</span></span> <span data-ttu-id="b56b7-315">Automatische Dienste werden auch dann gestartet, wenn sich ein Benutzer nicht anmelden kann.</span><span class="sxs-lookup"><span data-stu-id="b56b7-315">Auto services are started even if a user does not log on.</span></span>

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="b56b7-316"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manuell** ("manuell")</span><span class="sxs-lookup"><span data-stu-id="b56b7-316"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="b56b7-317">Der Dienst, der vom Dienststeuerungs-Manager gestartet werden soll, wenn ein Prozess die [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) -Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="b56b7-317">Service to be started by the Service Control Manager when a process calls the [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) method.</span></span> <span data-ttu-id="b56b7-318">Diese Dienste werden erst gestartet, wenn sich ein Benutzer anmeldet und startet.</span><span class="sxs-lookup"><span data-stu-id="b56b7-318">These services do not start unless a user logs on and starts them.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b56b7-319"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** ("deaktiviert")</span><span class="sxs-lookup"><span data-stu-id="b56b7-319"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="b56b7-320">Dienst, der erst gestartet werden kann, wenn sein StartMode entweder in "Auto" oder "manuell" geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="b56b7-320">Service that cannot be started until its StartMode is changed to either Auto or Manual.</span></span>

</dd> </dl>

<span data-ttu-id="b56b7-321">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b56b7-321">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="b56b7-322">**StartName**</span><span class="sxs-lookup"><span data-stu-id="b56b7-322">**StartName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b56b7-323">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b56b7-323">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b56b7-324">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b56b7-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b56b7-325">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| lpservicestartname"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Starting Account Name")</span><span class="sxs-lookup"><span data-stu-id="b56b7-325">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|lpServiceStartName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Starting Account Name")</span></span>
</dt> </dl>

<span data-ttu-id="b56b7-326">Der Kontoname, unter dem ein Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b56b7-326">Account name under which a service runs.</span></span> <span data-ttu-id="b56b7-327">Abhängig vom Diensttyp kann der Kontoname die Form "Domainname \\ username" oder das UPN-Format (" *Username@DomainName* ") aufweisen.</span><span class="sxs-lookup"><span data-stu-id="b56b7-327">Depending on the service type, the account name may be in the form of "DomainName\\Username" or UPN format ("*Username@DomainName*").</span></span> <span data-ttu-id="b56b7-328">Der Dienst Prozess wird mit einer dieser beiden Formulare protokolliert, wenn er ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b56b7-328">The service process is logged by using one of these two forms when it runs.</span></span> <span data-ttu-id="b56b7-329">Wenn das Konto zur integrierten Domäne gehört, dann ". \\ Username "kann angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b56b7-329">If the account belongs to the built-in domain, then ".\\Username" can be specified.</span></span> <span data-ttu-id="b56b7-330">Für Treiber auf Kernel-oder Systemebene enthält [**StartName**](/windows/desktop/CIMWin32Prov/win32-service) den Treiber Objektnamen (d. h. " \\ File System \\ rdr" oder " \\ Driver \\ XNS"), den das e/a-System zum Laden des Gerätetreibers verwendet.</span><span class="sxs-lookup"><span data-stu-id="b56b7-330">For kernel or system-level drivers, [**StartName**](/windows/desktop/CIMWin32Prov/win32-service) contains the driver object name (that is, "\\FileSystem\\Rdr" or "\\Driver\\Xns") which the I/O system uses to load the device driver.</span></span> <span data-ttu-id="b56b7-331">Wenn **null** angegeben wird, wird der Treiber mit einem Standard Objektnamen ausgeführt, der vom e/a-System basierend auf dem Dienstnamen erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="b56b7-331">Additionally, if **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name.</span></span>

<span data-ttu-id="b56b7-332">Beispiel: "dwdom \\ Admin"</span><span class="sxs-lookup"><span data-stu-id="b56b7-332">Example: "DWDOM\\Admin"</span></span>

<span data-ttu-id="b56b7-333">Diese Eigenschaft wird von [**Win32 \_ baseservice**](/windows/desktop/CIMWin32Prov/win32-baseservice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b56b7-333">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="b56b7-334">**State**</span><span class="sxs-lookup"><span data-stu-id="b56b7-334">**State**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b56b7-335">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b56b7-335">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b56b7-336">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b56b7-336">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b56b7-337">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Service \_ Status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwcurrentstate"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("State")</span><span class="sxs-lookup"><span data-stu-id="b56b7-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwCurrentState "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("State")</span></span>
</dt> </dl>

<span data-ttu-id="b56b7-338">Aktueller Status des Basis Dienes.</span><span class="sxs-lookup"><span data-stu-id="b56b7-338">Current state of the base service.</span></span>

<span data-ttu-id="b56b7-339">Die Werte sind:</span><span class="sxs-lookup"><span data-stu-id="b56b7-339">The values are:</span></span>

<dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span data-ttu-id="b56b7-340">**Beendet** ("beendet")</span><span class="sxs-lookup"><span data-stu-id="b56b7-340">**Stopped** ("Stopped")</span></span>


</dt> <dd></dd> <dt>

<span id="Start_Pending"></span><span id="start_pending"></span><span id="START_PENDING"></span>

<span data-ttu-id="b56b7-341">**Start steht aus** ("ausstehende Start")</span><span class="sxs-lookup"><span data-stu-id="b56b7-341">**Start Pending** ("Start Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Stop_Pending"></span><span id="stop_pending"></span><span id="STOP_PENDING"></span>

<span data-ttu-id="b56b7-342">**Ausstehende Beendigung** ("ausstehenden Vorgang nicht mehr")</span><span class="sxs-lookup"><span data-stu-id="b56b7-342">**Stop Pending** ("Stop Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="b56b7-343">Wird **ausgeführt** ("wird ausgeführt")</span><span class="sxs-lookup"><span data-stu-id="b56b7-343">**Running** ("Running")</span></span>


</dt> <dd></dd> <dt>

<span id="Continue_Pending"></span><span id="continue_pending"></span><span id="CONTINUE_PENDING"></span>

<span data-ttu-id="b56b7-344">**Ausstehende Fortsetzung** ("ausstehende Fortsetzung")</span><span class="sxs-lookup"><span data-stu-id="b56b7-344">**Continue Pending** ("Continue Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Pause_Pending"></span><span id="pause_pending"></span><span id="PAUSE_PENDING"></span>

<span data-ttu-id="b56b7-345">Anhalten steht **aus** ("ausstehende Pause")</span><span class="sxs-lookup"><span data-stu-id="b56b7-345">**Pause Pending** ("Pause Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="b56b7-346">**Angeh** alten ("angehalten")</span><span class="sxs-lookup"><span data-stu-id="b56b7-346">**Paused** ("Paused")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b56b7-347">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="b56b7-347">**Unknown** ("Unknown")</span></span>


<span data-ttu-id="b56b7-348"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="b56b7-348"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="b56b7-349">**Windows Server 2008 und Windows Vista:** Diese Eigenschaft ist vor Windows 7 und Windows Server 2008 R2 schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="b56b7-349">**Windows Server 2008 and Windows Vista:** This property is read-only before Windows 7 and Windows Server 2008 R2.</span></span>

<span data-ttu-id="b56b7-350">Diese Eigenschaft wird von [**Win32 \_ baseservice**](/windows/desktop/CIMWin32Prov/win32-baseservice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b56b7-350">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="b56b7-351">**Status**</span><span class="sxs-lookup"><span data-stu-id="b56b7-351">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b56b7-352">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b56b7-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b56b7-353">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b56b7-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b56b7-354">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="b56b7-354">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="b56b7-355">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="b56b7-355">Current status of the object.</span></span> <span data-ttu-id="b56b7-356">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="b56b7-356">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="b56b7-357">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="b56b7-357">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="b56b7-358">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="b56b7-358">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="b56b7-359">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="b56b7-359">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="b56b7-360">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="b56b7-360">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="b56b7-361">Die Werte sind:</span><span class="sxs-lookup"><span data-stu-id="b56b7-361">The values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="b56b7-362">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="b56b7-362">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="b56b7-363">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="b56b7-363">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b56b7-364">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="b56b7-364">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b56b7-365">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="b56b7-365">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="b56b7-366">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="b56b7-366">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="b56b7-367">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="b56b7-367">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="b56b7-368">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="b56b7-368">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="b56b7-369">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="b56b7-369">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="b56b7-370">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="b56b7-370">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="b56b7-371">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="b56b7-371">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="b56b7-372">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="b56b7-372">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="b56b7-373">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="b56b7-373">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="b56b7-374"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="b56b7-374"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="b56b7-375">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b56b7-375">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b56b7-376">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="b56b7-376">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b56b7-377">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b56b7-377">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b56b7-378">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b56b7-378">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b56b7-379">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](/windows/desktop/CIMWin32Prov/cim-system). "Kreationclassname"), [**CIM- \_ Schlüssel**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Klassenname")</span><span class="sxs-lookup"><span data-stu-id="b56b7-379">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system).CreationClassName"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="b56b7-380">Der Typname des Systems, das den Dienst hostet.</span><span class="sxs-lookup"><span data-stu-id="b56b7-380">Type name of the system that hosts this service.</span></span>

<span data-ttu-id="b56b7-381">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b56b7-381">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="b56b7-382">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="b56b7-382">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b56b7-383">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b56b7-383">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b56b7-384">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b56b7-384">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b56b7-385">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](/windows/desktop/CIMWin32Prov/cim-system). Name "), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" System Name ")</span><span class="sxs-lookup"><span data-stu-id="b56b7-385">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system).Name"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Name")</span></span>
</dt> </dl>

<span data-ttu-id="b56b7-386">Der Name des Systems, das den Dienst hostet.</span><span class="sxs-lookup"><span data-stu-id="b56b7-386">Name of the system that hosts this service.</span></span>

<span data-ttu-id="b56b7-387">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b56b7-387">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="b56b7-388">**TagID**</span><span class="sxs-lookup"><span data-stu-id="b56b7-388">**TagId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b56b7-389">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b56b7-389">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b56b7-390">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b56b7-390">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b56b7-391">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwtagid"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tag ID")</span><span class="sxs-lookup"><span data-stu-id="b56b7-391">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|dwTagId"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tag Id")</span></span>
</dt> </dl>

<span data-ttu-id="b56b7-392">Eindeutiger Tagwert für diesen Dienst in der Gruppe.</span><span class="sxs-lookup"><span data-stu-id="b56b7-392">Unique tag value for this service in the group.</span></span> <span data-ttu-id="b56b7-393">Der Wert 0 (null) gibt an, dass der Dienst nicht über ein Tag verfügt.</span><span class="sxs-lookup"><span data-stu-id="b56b7-393">A value of 0 (zero) indicates that the service does not have a tag.</span></span> <span data-ttu-id="b56b7-394">Ein-Tag kann verwendet werden, um den Dienst Start innerhalb einer Gruppe von Lade Reihenfolgen zu sortieren, indem Sie in der Registrierung einen taganordnungs Vektor angeben:</span><span class="sxs-lookup"><span data-stu-id="b56b7-394">A tag can be used to order service startup within a load order group by specifying a tag order vector in the registry located at:</span></span>

<span data-ttu-id="b56b7-395">**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Steuer** Element \\ **grouporderlist**    </span><span class="sxs-lookup"><span data-stu-id="b56b7-395">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\    **GroupOrderList**</span></span>

<span data-ttu-id="b56b7-396">Tags werden nur für Kernel Treiber-und Datei System Treiber-Starttyp Dienste ausgewertet, die über Start-oder System Start Modi verfügen.</span><span class="sxs-lookup"><span data-stu-id="b56b7-396">Tags are only evaluated for Kernel Driver and File System Driver start type services that have Boot or System start modes.</span></span>

<span data-ttu-id="b56b7-397">Diese Eigenschaft wird von [**Win32 \_ baseservice**](/windows/desktop/CIMWin32Prov/win32-baseservice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b56b7-397">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="b56b7-398">**Totalsessions**</span><span class="sxs-lookup"><span data-stu-id="b56b7-398">**TotalSessions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b56b7-399">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b56b7-399">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b56b7-400">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b56b7-400">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b56b7-401">Die Gesamtanzahl der Sitzungen auf dem aktuellen Server.</span><span class="sxs-lookup"><span data-stu-id="b56b7-401">The total number of sessions on the current server.</span></span> <span data-ttu-id="b56b7-402">Dies schließt sowohl verbundene als auch getrennte Sitzungen ein.</span><span class="sxs-lookup"><span data-stu-id="b56b7-402">This includes both connected and disconnected sessions.</span></span>

</dd> <dt>

<span data-ttu-id="b56b7-403">**WaitHint**</span><span class="sxs-lookup"><span data-stu-id="b56b7-403">**WaitHint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b56b7-404">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b56b7-404">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b56b7-405">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b56b7-405">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b56b7-406">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Service \_ Status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwwaithint"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("geschätzte Wartezeit")</span><span class="sxs-lookup"><span data-stu-id="b56b7-406">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwWaitHint"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Estimated Wait Time")</span></span>
</dt> </dl>

<span data-ttu-id="b56b7-407">Geschätzte benötigte Zeit (in Millisekunden) für einen ausstehenden Start-, anhalte-, Anhaltevorgang-oder continue-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="b56b7-407">Estimated time required, in milliseconds, for a pending start, stop, pause, or continue operation.</span></span> <span data-ttu-id="b56b7-408">Nachdem die angegebene Zeit abgelaufen ist, führt der Dienst den nächsten Aufruf der **SetServiceStatus** -Methode mit einem [**inkrementierten**](/windows/desktop/CIMWin32Prov/win32-service) Prüf Punkt Wert oder einer Änderung in **CurrentState** aus.</span><span class="sxs-lookup"><span data-stu-id="b56b7-408">After the specified time has elapsed, the service makes its next call to the **SetServiceStatus** method with either an incremented [**CheckPoint**](/windows/desktop/CIMWin32Prov/win32-service) value or a change in **CurrentState**.</span></span> <span data-ttu-id="b56b7-409">Wenn die von **WaitHint** angegebene Zeitspanne verstrichen **ist und der** Prüfpunkt nicht inkrementiert wurde, oder **CurrentState** nicht geändert wurde, geht der Dienststeuerungs-Manager oder das Dienst Steuerungsprogramm davon aus, dass ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="b56b7-409">If the amount of time specified by **WaitHint** passes, and **CheckPoint** has not been incremented, or **CurrentState** has not changed, the service control manager or service control program assumes that an error has occurred.</span></span>

<span data-ttu-id="b56b7-410">Diese Eigenschaft wird vom [**Win32- \_ Dienst**](/windows/desktop/CIMWin32Prov/win32-service)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b56b7-410">This property is inherited from [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b56b7-411">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b56b7-411">Remarks</span></span>

<span data-ttu-id="b56b7-412">Da die **Win32 \_ Terminalservice** -Klasse eine Unterklasse der [**Win32- \_ Dienst**](/windows/desktop/CIMWin32Prov/win32-service) Klasse ist, erbt die-Klasse alle Eigenschaften und Methoden des **Win32- \_ Dienstanbieter**.</span><span class="sxs-lookup"><span data-stu-id="b56b7-412">Since the **Win32\_TerminalService** class is a subclass of the [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) class, the class inherits all properties and methods of **Win32\_Service**.</span></span>

<span data-ttu-id="b56b7-413">[**Win32 \_ Terminalservicesete**](win32-terminalservicesetting.md) ist **Win32 \_ Terminalservice** als **Einstellungs** Eigenschaft der [**Win32 \_ terminalservicedesetting**](win32-terminalservicetosetting.md) -Zuordnung zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="b56b7-413">[**Win32\_TerminalServiceSetting**](win32-terminalservicesetting.md) is associated to **Win32\_TerminalService** as the **Setting** property of the [**Win32\_TerminalServiceToSetting**](win32-terminalservicetosetting.md) association.</span></span>

<span data-ttu-id="b56b7-414">[**Win32 \_ Tssessiondirectory**](win32-tssessiondirectory.md) ist **Win32 \_ Terminalservice** als **Einstellungs** Eigenschaft der [**Win32 \_ tssessiondirectorysetting**](win32-tssessiondirectorysetting.md) -Zuordnung zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="b56b7-414">[**Win32\_TSSessionDirectory**](win32-tssessiondirectory.md) is associated to **Win32\_TerminalService** as the **Setting** property of the [**Win32\_TSSessionDirectorySetting**](win32-tssessiondirectorysetting.md) association.</span></span>

<span data-ttu-id="b56b7-415">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="b56b7-415">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b56b7-416">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="b56b7-416">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b56b7-417">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="b56b7-417">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b56b7-418">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="b56b7-418">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="b56b7-419">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b56b7-419">Requirements</span></span>



| <span data-ttu-id="b56b7-420">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b56b7-420">Requirement</span></span> | <span data-ttu-id="b56b7-421">Wert</span><span class="sxs-lookup"><span data-stu-id="b56b7-421">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b56b7-422">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b56b7-422">Minimum supported client</span></span><br/> | <span data-ttu-id="b56b7-423">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b56b7-423">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b56b7-424">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b56b7-424">Minimum supported server</span></span><br/> | <span data-ttu-id="b56b7-425">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b56b7-425">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b56b7-426">Namespace</span><span class="sxs-lookup"><span data-stu-id="b56b7-426">Namespace</span></span><br/>                | <span data-ttu-id="b56b7-427">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="b56b7-427">Root\\CIMv2</span></span><br/>                                                                  |
| <span data-ttu-id="b56b7-428">MOF</span><span class="sxs-lookup"><span data-stu-id="b56b7-428">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b56b7-429"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b56b7-429"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="b56b7-430">DLL</span><span class="sxs-lookup"><span data-stu-id="b56b7-430">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b56b7-431"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b56b7-431"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b56b7-432">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b56b7-432">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b56b7-433">**Win32- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="b56b7-433">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="b56b7-434">**Win32 \_ terminalservicede Setting**</span><span class="sxs-lookup"><span data-stu-id="b56b7-434">**Win32\_TerminalServiceToSetting**</span></span>](win32-terminalservicetosetting.md)
</dt> <dt>

[<span data-ttu-id="b56b7-435">**Win32- \_ tssessiondirectory**</span><span class="sxs-lookup"><span data-stu-id="b56b7-435">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> <dt>

[<span data-ttu-id="b56b7-436">**Win32- \_ baseservice**</span><span class="sxs-lookup"><span data-stu-id="b56b7-436">**Win32\_BaseService**</span></span>](/windows/desktop/CIMWin32Prov/win32-baseservice)
</dt> <dt>

[<span data-ttu-id="b56b7-437">**CIM- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="b56b7-437">**CIM\_Service**</span></span>](/windows/desktop/CIMWin32Prov/cim-service)
</dt> </dl>

 

