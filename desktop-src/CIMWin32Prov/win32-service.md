---
description: Stellt einen Dienst auf einem Computersystem dar, auf dem Windows ausgeführt wird.
ms.assetid: 713402d3-ee73-4a6c-afb9-ad8033a4c580
ms.tgt_platform: multiple
title: Win32_Service-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service
- Win32_Service.AcceptPause
- Win32_Service.AcceptStop
- Win32_Service.Caption
- Win32_Service.CheckPoint
- Win32_Service.CreationClassName
- Win32_Service.DelayedAutoStart
- Win32_Service.Description
- Win32_Service.DesktopInteract
- Win32_Service.DisplayName
- Win32_Service.ErrorControl
- Win32_Service.ExitCode
- Win32_Service.InstallDate
- Win32_Service.Name
- Win32_Service.PathName
- Win32_Service.ProcessId
- Win32_Service.ServiceSpecificExitCode
- Win32_Service.ServiceType
- Win32_Service.Started
- Win32_Service.StartMode
- Win32_Service.StartName
- Win32_Service.State
- Win32_Service.Status
- Win32_Service.SystemCreationClassName
- Win32_Service.SystemName
- Win32_Service.TagId
- Win32_Service.WaitHint
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b342282bfa3b49fe72e62cf79377a0ead11276eb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041353"
---
# <a name="win32_service-class"></a><span data-ttu-id="4e9ef-103">Win32- \_ Dienstklasse</span><span class="sxs-lookup"><span data-stu-id="4e9ef-103">Win32\_Service class</span></span>

<span data-ttu-id="4e9ef-104">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) für den **Win32- \_ Dienst** stellt einen Dienst auf einem Computersystem mit Windows dar.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-104">The **Win32\_Service** [WMI class](../wmisdk/retrieving-a-class.md) represents a service on a computer system running Windows.</span></span>

<span data-ttu-id="4e9ef-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="4e9ef-106">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e9ef-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e9ef-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4D9-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Services"), AMENDMENT]
class Win32_Service : Win32_BaseService
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
};
```

## <a name="members"></a><span data-ttu-id="4e9ef-108">Member</span><span class="sxs-lookup"><span data-stu-id="4e9ef-108">Members</span></span>

<span data-ttu-id="4e9ef-109">Die **Win32- \_ Dienst** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="4e9ef-109">The **Win32\_Service** class has these types of members:</span></span>

-   [<span data-ttu-id="4e9ef-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="4e9ef-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="4e9ef-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4e9ef-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4e9ef-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="4e9ef-112">Methods</span></span>

<span data-ttu-id="4e9ef-113">Die **Win32- \_ Dienst** Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-113">The **Win32\_Service** class has these methods.</span></span>



| <span data-ttu-id="4e9ef-114">Methode</span><span class="sxs-lookup"><span data-stu-id="4e9ef-114">Method</span></span>                                                                               | <span data-ttu-id="4e9ef-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4e9ef-115">Description</span></span>                                                                                          |
|:-------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4e9ef-116">**Klima**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-116">**Change**</span></span>](change-method-in-class-win32-service.md)                               | <span data-ttu-id="4e9ef-117">Ändert einen Dienst.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-117">Modifies a service.</span></span><br/>                                                                       |
| [<span data-ttu-id="4e9ef-118">**ChangeStartMode**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-118">**ChangeStartMode**</span></span>](changestartmode-method-in-class-win32-service.md)             | <span data-ttu-id="4e9ef-119">Ändert den Start Modus eines Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-119">Modifies the start mode of a service.</span></span><br/>                                                     |
| [<span data-ttu-id="4e9ef-120">**Stelle**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-120">**Create**</span></span>](create-method-in-class-win32-service.md)                               | <span data-ttu-id="4e9ef-121">Erstellt einen neuen Dienst.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-121">Creates a new service.</span></span><br/>                                                                    |
| [<span data-ttu-id="4e9ef-122">**Lösch**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-122">**Delete**</span></span>](delete-method-in-class-win32-service.md)                               | <span data-ttu-id="4e9ef-123">Löscht einen vorhandenen Dienst.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-123">Deletes an existing service.</span></span><br/>                                                              |
| [<span data-ttu-id="4e9ef-124">**GetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-124">**GetSecurityDescriptor**</span></span>](getsecuritydescriptor-method-in-class-win32-service.md) | <span data-ttu-id="4e9ef-125">Gibt die Sicherheits Beschreibung zurück, die den Zugriff auf den Dienst steuert.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-125">Returns the security descriptor that controls access to the service.</span></span><br/>                      |
| [<span data-ttu-id="4e9ef-126">**"InterrogateService"**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-126">**InterrogateService**</span></span>](interrogateservice-method-in-class-win32-service.md)       | <span data-ttu-id="4e9ef-127">Fordert an, dass ein Dienst seinen Status auf den Dienst-Manager aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-127">Requests that a service update its state to the service manager.</span></span><br/>                          |
| [<span data-ttu-id="4e9ef-128">**PauseService**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-128">**PauseService**</span></span>](pauseservice-method-in-class-win32-service.md)                   | <span data-ttu-id="4e9ef-129">Versucht, einen Dienst in den angehaltenen Zustand zu versetzen.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-129">Attempts to place a service in the paused state.</span></span><br/>                                          |
| [<span data-ttu-id="4e9ef-130">**ResumeService**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-130">**ResumeService**</span></span>](resumeservice-method-in-class-win32-service.md)                 | <span data-ttu-id="4e9ef-131">Versucht, einen Dienst in den Status "wieder aufgenommen" zu versetzen.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-131">Attempts to place a service in the resumed state.</span></span><br/>                                         |
| [<span data-ttu-id="4e9ef-132">**SETSECURITYDESCRIPTOR**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-132">**SetSecurityDescriptor**</span></span>](setsecuritydescriptor-method-in-class-win32-service.md) | <span data-ttu-id="4e9ef-133">Schreibt eine aktualisierte Version der Sicherheits Beschreibung, die den Zugriff auf den Dienst steuert.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-133">Writes an updated version of the security descriptor that controls access to the service.</span></span><br/> |
| [<span data-ttu-id="4e9ef-134">**Start Service**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-134">**StartService**</span></span>](startservice-method-in-class-win32-service.md)                   | <span data-ttu-id="4e9ef-135">Versucht, einen Dienst in den Startzustand zu versetzen.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-135">Attempts to place a service into the startup state.</span></span><br/>                                       |
| [<span data-ttu-id="4e9ef-136">**Stop Service**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-136">**StopService**</span></span>](stopservice-method-in-class-win32-service.md)                     | <span data-ttu-id="4e9ef-137">Versetzt einen Dienst in den Status "beendet".</span><span class="sxs-lookup"><span data-stu-id="4e9ef-137">Places a service in the stopped state.</span></span><br/>                                                    |
| [<span data-ttu-id="4e9ef-138">**UserControlService**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-138">**UserControlService**</span></span>](usercontrolservice-method-in-class-win32-service.md)       | <span data-ttu-id="4e9ef-139">Versucht, einen benutzerdefinierten Steuerelement Code an einen Dienst zu senden.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-139">Attempts to send a user-defined control code to a service.</span></span><br/>                                |



 

### <a name="properties"></a><span data-ttu-id="4e9ef-140">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4e9ef-140">Properties</span></span>

<span data-ttu-id="4e9ef-141">Die **Win32- \_ Dienst** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-141">The **Win32\_Service** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4e9ef-142">**AcceptPause**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-142">**AcceptPause**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e9ef-143">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="4e9ef-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4e9ef-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4e9ef-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e9ef-145">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API Service \| Structures \| [**Service \_ Status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwcontrolsaccepted \| Service \_ Accept \_ Pause \_ Continue"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Service Accept Pause")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-145">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwControlsAccepted\|SERVICE\_ACCEPT\_PAUSE\_CONTINUE"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Service Accepts Pause")</span></span>
</dt> </dl>

<span data-ttu-id="4e9ef-146">Gibt an, ob der Dienst angehalten werden kann.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-146">Indicates whether the service can be paused.</span></span>

<span data-ttu-id="4e9ef-147">Diese Eigenschaft wird von [**Win32 \_ baseservice**](win32-baseservice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-147">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e9ef-148">**AcceptStop**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-148">**AcceptStop**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e9ef-149">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="4e9ef-149">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4e9ef-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4e9ef-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e9ef-151">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API Service \| Structures \| [**Service \_ Status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwcontrolsaccepted \| Service \_ Accept End \_ "), [**Display Name**](../wmisdk/standard-qualifiers.md) ("der Dienst akzeptiert das Ende")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-151">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwControlsAccepted\|SERVICE\_ACCEPT\_STOP"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Service Accepts Stop")</span></span>
</dt> </dl>

<span data-ttu-id="4e9ef-152">Gibt an, ob der Dienst beendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-152">Indicates whether the service can be stopped.</span></span>

<span data-ttu-id="4e9ef-153">Diese Eigenschaft wird von [**Win32 \_ baseservice**](win32-baseservice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-153">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e9ef-154">**Caption**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-154">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e9ef-155">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e9ef-156">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4e9ef-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e9ef-157">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-157">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="4e9ef-158">Kurze Beschreibung des Dienstanbieter – eine einzeilige Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-158">Short description of the service —a one-line string.</span></span>

<span data-ttu-id="4e9ef-159">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-159">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e9ef-160">**Kal**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-160">**CheckPoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e9ef-161">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4e9ef-162">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4e9ef-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e9ef-163">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**Service \_ Status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwcheck"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Check Point count")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-163">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwCheckPoint"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Check Point Count")</span></span>
</dt> </dl>

<span data-ttu-id="4e9ef-164">Der Wert, den der Dienst in regelmäßigen Abständen erhöht, um den Fortschritt während eines langen Starts, Anhaltevorgangs, anhalten oder fortsetzen zu melden.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-164">Value that the service increments periodically to report its progress during a long start, stop, pause, or continue operation.</span></span> <span data-ttu-id="4e9ef-165">Der Dienst erhöht z. b. diesen Wert, da er die einzelnen Schritte seiner Initialisierung beim Starten abschließt.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-165">For example, the service increments this value as it completes each step of its initialization when it is starting up.</span></span> <span data-ttu-id="4e9ef-166">Das Benutzeroberflächen Programm, das den-Vorgang für den Dienst aufruft, verwendet diesen Wert, um den Status des Dienstanbieter während eines langwierigen Vorgangs zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-166">The user interface program that invokes the operation on the service uses this value to track the progress of the service during a lengthy operation.</span></span> <span data-ttu-id="4e9ef-167">Dieser Wert ist ungültig und sollte NULL sein, wenn der Dienst nicht über einen Vorgang zum Starten, beenden, anhalten oder fortsetzen verfügt.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-167">This value is not valid and should be zero when the service does not have a start, stop, pause, or continue operation pending.</span></span>

</dd> <dt>

<span data-ttu-id="4e9ef-168">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-168">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e9ef-169">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e9ef-170">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4e9ef-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e9ef-171">Qualifizierer: [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Class Name")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-171">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="4e9ef-172">Der Name der ersten konkreten Klasse, die in der Vererbungs Kette angezeigt werden soll, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-172">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="4e9ef-173">Wenn diese Eigenschaft mit den anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-173">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="4e9ef-174">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](cim-service.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-174">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e9ef-175">**DelayedAutoStart**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-175">**DelayedAutoStart**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e9ef-176">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="4e9ef-176">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4e9ef-177">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4e9ef-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e9ef-178">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**Service \_ verzögert \_ Auto \_ Start \_ Info**](/windows/win32/api/winsvc/ns-winsvc-service_delayed_auto_start_info) \| f delayedautostart"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("verzögerter automatischer Start")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-178">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_DELAYED\_AUTO\_START\_INFO**](/windows/win32/api/winsvc/ns-winsvc-service_delayed_auto_start_info)\|fDelayedAutostart"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Delayed Auto-Start")</span></span>
</dt> </dl>

<span data-ttu-id="4e9ef-179">**True** gibt an, dass der Dienst gestartet wird, nachdem andere automatischen Start Dienste und eine kurze Verzögerung gestartet wurden.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-179">If **True**, the service is started after other auto-start services are started plus a short delay.</span></span>

<span data-ttu-id="4e9ef-180">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Diese Eigenschaft wird vor Windows Server 2016 und Windows 10 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-180">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows Server 2016 and Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="4e9ef-181">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-181">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e9ef-182">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e9ef-183">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4e9ef-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e9ef-184">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-184">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="4e9ef-185">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-185">Description of the object.</span></span>

<span data-ttu-id="4e9ef-186">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-186">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e9ef-187">**DesktopInteract**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-187">**DesktopInteract**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e9ef-188">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="4e9ef-188">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4e9ef-189">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4e9ef-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e9ef-190">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**Query \_ Service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| dwservicetype \| Service \_ Interactive \_ Process"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("interagiert with Desktop")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-190">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|dwServiceType\|SERVICE\_INTERACTIVE\_PROCESS"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Interacts With Desktop")</span></span>
</dt> </dl>

<span data-ttu-id="4e9ef-191">Gibt an, ob der Dienst Windows auf dem Desktop erstellen oder mit ihm kommunizieren kann, sodass er auf irgendeine Weise mit einem Benutzer interagieren kann.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-191">Indicates whether the service can create or communicate with windows on the desktop, and thus interact in some way with a user.</span></span> <span data-ttu-id="4e9ef-192">Interaktive Dienste müssen unter dem lokalen System Konto ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-192">Interactive services must run under the Local System account.</span></span> <span data-ttu-id="4e9ef-193">Die meisten Dienste sind nicht interaktiv. Das heißt, Sie kommunizieren in keiner Weise mit dem Benutzer.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-193">Most services are not interactive; that is, they do not communicate with the user in any way.</span></span>

<span data-ttu-id="4e9ef-194">Diese Eigenschaft wird von [**Win32 \_ baseservice**](win32-baseservice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-194">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e9ef-195">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-195">**DisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e9ef-196">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e9ef-197">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4e9ef-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e9ef-198">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**Query \_ Service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| lpdisplayname"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Anzeige Name")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-198">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|lpDisplayName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Display Name")</span></span>
</dt> </dl>

<span data-ttu-id="4e9ef-199">Der Name des Diensts, wie im Dienste-Snap-in angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-199">Name of the service as viewed in the Services snap-in.</span></span> <span data-ttu-id="4e9ef-200">Die maximale Länge der Zeichenfolge beträgt 256 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-200">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="4e9ef-201">Beachten Sie, dass der Anzeige Name und der Dienst Name (der in der Registrierung gespeichert ist) nicht immer identisch sind.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-201">Note that the display name and the service name (which is stored in the registry) are not always the same.</span></span> <span data-ttu-id="4e9ef-202">Der DHCP-Client Dienst hat z. b. den Dienstnamen DHCP, aber den anzeigen Amen DHCP-Client.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-202">For example, the DHCP Client service has the service name Dhcp but the display name DHCP Client.</span></span> <span data-ttu-id="4e9ef-203">Der Name wird im Dienststeuerungs-Manager nach Groß-/Kleinschreibung beibehalten.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-203">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="4e9ef-204">Bei **DisplayName** -vergleichen wird jedoch immer die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-204">However, **DisplayName** comparisons are always case-insensitive.</span></span>

<span data-ttu-id="4e9ef-205">Einschränkung: akzeptiert denselben Wert wie die **Name** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-205">Constraint: Accepts the same value as the **Name** property.</span></span>

<span data-ttu-id="4e9ef-206">Beispiel: "ATDISK"</span><span class="sxs-lookup"><span data-stu-id="4e9ef-206">Example: "Atdisk"</span></span>

<span data-ttu-id="4e9ef-207">Diese Eigenschaft wird von [**Win32 \_ baseservice**](win32-baseservice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-207">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e9ef-208">**ErrorControl**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-208">**ErrorControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e9ef-209">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e9ef-210">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4e9ef-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e9ef-211">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**Query \_ Service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| dwerrorcontrol"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Schweregrad des Start Fehlers")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-211">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|dwErrorControl"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Severity Of Startup Failure")</span></span>
</dt> </dl>

<span data-ttu-id="4e9ef-212">Der Schweregrad des Fehlers, wenn dieser Dienst während des Starts nicht gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-212">Severity of the error if this service fails to start during startup.</span></span> <span data-ttu-id="4e9ef-213">Der Wert gibt die vom Start Programm ausgeführte Aktion an, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-213">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="4e9ef-214">Alle Fehler werden vom Computersystem protokolliert.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-214">All errors are logged by the computer system.</span></span>

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span data-ttu-id="4e9ef-215"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignorieren** ("ignorieren")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-215"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignore** ("Ignore")</span></span>


</dt> <dd>

<span data-ttu-id="4e9ef-216">Der Benutzer wird nicht benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-216">User is not notified.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="4e9ef-217"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** ("Normal")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-217"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** ("Normal")</span></span>


</dt> <dd>

<span data-ttu-id="4e9ef-218">Der Benutzer wird benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-218">User is notified.</span></span> <span data-ttu-id="4e9ef-219">Normalerweise ist dies ein Meldungs Feld, in dem der Benutzer über das Problem benachrichtigt wird.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-219">Usually this will be a message box display notifying the user of the problem.</span></span>

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span data-ttu-id="4e9ef-220"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Schwerwiegend** ("schwerwiegend")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-220"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Severe** ("Severe")</span></span>


</dt> <dd>

<span data-ttu-id="4e9ef-221">Das System wird mit der letzten bekannten, fehlerfreien Konfiguration neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-221">System is restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="4e9ef-222"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Kritisch** ("kritisch")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-222"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** ("Critical")</span></span>


</dt> <dd>

<span data-ttu-id="4e9ef-223">Das System versucht, mit einer fehlerfreien Konfiguration zu neu starten.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-223">System attempts to restart with a good configuration.</span></span> <span data-ttu-id="4e9ef-224">Wenn der Dienst nicht ein zweites Mal gestartet werden kann, schlägt der Startvorgang fehl.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-224">If the service fails to start a second time, startup fails.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4e9ef-225"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-225"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** ("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="4e9ef-226">Der Schweregrad des Fehlers ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-226">Severity of the error is unknown.</span></span>

</dd> </dl>

<span data-ttu-id="4e9ef-227">Diese Eigenschaft wird von [**Win32 \_ baseservice**](win32-baseservice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-227">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e9ef-228">**Exitcode**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-228">**ExitCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e9ef-229">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-229">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4e9ef-230">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4e9ef-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e9ef-231">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**Service \_ Status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwWin32ExitCode"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Exitcode")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-231">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwWin32ExitCode"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Exit Code")</span></span>
</dt> </dl>

<span data-ttu-id="4e9ef-232">Windows-Fehlercode, der Fehler definiert, die beim Starten oder Beenden des Dienstes aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-232">Windows error code that defines errors encountered in starting or stopping the service.</span></span> <span data-ttu-id="4e9ef-233">Diese Eigenschaft ist auf **Fehler \_ Dienst \_ spezifischer \_ Fehler** (1066) festgelegt, wenn der Fehler für den Dienst eindeutig ist, der durch diese Klasse dargestellt wird. Informationen über den Fehler sind in der **ServiceSpecificExitCode** -Eigenschaft verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-233">This property is set to **ERROR\_SERVICE\_SPECIFIC\_ERROR** (1066) when the error is unique to the service represented by this class, and information about the error is available in the **ServiceSpecificExitCode** property.</span></span> <span data-ttu-id="4e9ef-234">Der Dienst legt diesen Wert bei der Ausführung und erneut bei normaler Beendigung auf **keinen \_ Fehler** fest.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-234">The service sets this value to **NO\_ERROR** when running, and again upon normal termination.</span></span>

<span data-ttu-id="4e9ef-235">Diese Eigenschaft wird von [**Win32 \_ baseservice**](win32-baseservice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-235">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e9ef-236">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-236">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e9ef-237">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-237">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4e9ef-238">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4e9ef-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e9ef-239">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-239">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="4e9ef-240">Date-Objekt ist installiert.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-240">Date object is installed.</span></span> <span data-ttu-id="4e9ef-241">Diese Eigenschaft erfordert keinen Wert, um anzugeben, dass das-Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-241">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="4e9ef-242">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-242">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e9ef-243">**Name**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-243">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e9ef-244">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e9ef-245">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4e9ef-245">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e9ef-246">Qualifizierer: [ **Schlüssel**](../wmisdk/key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="4e9ef-246">Qualifiers: [**Key**](../wmisdk/key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="4e9ef-247">Eindeutiger Bezeichner des dienstanweises, der angibt, welche Funktionen verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-247">Unique identifier of the service that provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="4e9ef-248">Diese Funktionalität wird in der **Description** -Eigenschaft des-Objekts beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-248">This functionality is described in the **Description** property of the object.</span></span>

<span data-ttu-id="4e9ef-249">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-249">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e9ef-250">**PathName**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-250">**PathName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e9ef-251">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e9ef-252">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4e9ef-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e9ef-253">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**Query \_ Service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| lpbinarypathname"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Dateipfadname")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-253">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|lpBinaryPathName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File Path Name")</span></span>
</dt> </dl>

<span data-ttu-id="4e9ef-254">Der voll qualifizierte Pfad der Dienst Binärdatei, die den Dienst implementiert.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-254">Fully qualified path to the service binary file that implements the service.</span></span>

<span data-ttu-id="4e9ef-255">Beispiel: " \\ systemroot \\ system32 \\ Drivers \\afd.sys"</span><span class="sxs-lookup"><span data-stu-id="4e9ef-255">Example: "\\SystemRoot\\System32\\drivers\\afd.sys"</span></span>

<span data-ttu-id="4e9ef-256">Diese Eigenschaft wird von [**Win32 \_ baseservice**](win32-baseservice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-256">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e9ef-257">**ProcessId**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-257">**ProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e9ef-258">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-258">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4e9ef-259">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4e9ef-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e9ef-260">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**Service \_ Status \_ Process**](/windows/win32/api/winsvc/ns-winsvc-service_status_process) \| dwProcessId"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Process ID")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-260">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS\_PROCESS**](/windows/win32/api/winsvc/ns-winsvc-service_status_process)\|dwProcessId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Process Id")</span></span>
</dt> </dl>

<span data-ttu-id="4e9ef-261">Prozess Bezeichner des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-261">Process identifier of the service.</span></span>

<span data-ttu-id="4e9ef-262">Beispiel: 324</span><span class="sxs-lookup"><span data-stu-id="4e9ef-262">Example: 324</span></span>

</dd> <dt>

<span data-ttu-id="4e9ef-263">**ServiceSpecificExitCode**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-263">**ServiceSpecificExitCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e9ef-264">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-264">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4e9ef-265">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4e9ef-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e9ef-266">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**Service \_ Status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwservicespecificexitcode"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Server spezifischer Exitcode")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-266">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwServiceSpecificExitCode"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Server Specific Exit Code")</span></span>
</dt> </dl>

<span data-ttu-id="4e9ef-267">Dienst spezifischer Fehlercode für Fehler, die auftreten, während der Dienst gestartet oder beendet wird.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-267">Service-specific error code for errors that occur while the service is either starting or stopping.</span></span> <span data-ttu-id="4e9ef-268">Die Exitcodes werden von dem Dienst definiert, der durch diese Klasse dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-268">The exit codes are defined by the service represented by this class.</span></span> <span data-ttu-id="4e9ef-269">Dieser Wert wird nur festgelegt, wenn der **Exitcode** -Eigenschafts Wert **Fehler \_ Dienst \_ spezifisch \_** ist (1066).</span><span class="sxs-lookup"><span data-stu-id="4e9ef-269">This value is only set when the **ExitCode** property value is **ERROR\_SERVICE\_SPECIFIC\_ERROR** (1066).</span></span>

<span data-ttu-id="4e9ef-270">Diese Eigenschaft wird von [**Win32 \_ baseservice**](win32-baseservice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-270">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e9ef-271">**ServiceType**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-271">**ServiceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e9ef-272">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-272">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e9ef-273">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4e9ef-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e9ef-274">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**Query \_ Service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| dwservicetype"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Service Type")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-274">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|dwServiceType"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Service Type")</span></span>
</dt> </dl>

<span data-ttu-id="4e9ef-275">Der für aufrufende Prozesse bereitgestellte Diensttyp.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-275">Type of service provided to calling processes.</span></span>

<span data-ttu-id="4e9ef-276">Die Werte sind:</span><span class="sxs-lookup"><span data-stu-id="4e9ef-276">The values are:</span></span>

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

<span data-ttu-id="4e9ef-277">**Kernel Treiber** ("Kernel Treiber")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-277">**Kernel Driver** ("Kernel Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

<span data-ttu-id="4e9ef-278">**Dateisystem Treiber** ("Dateisystem Treiber")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-278">**File System Driver** ("File System Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

<span data-ttu-id="4e9ef-279">**Adapter** ("Adapter")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-279">**Adapter** ("Adapter")</span></span>


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

<span data-ttu-id="4e9ef-280">**Erkennungs Treiber** ("Erkennungs Treiber")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-280">**Recognizer Driver** ("Recognizer Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

<span data-ttu-id="4e9ef-281">**Eigener Prozess** ("eigener Prozess")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-281">**Own Process** ("Own Process")</span></span>


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

<span data-ttu-id="4e9ef-282">**Freigabeprozess** ("Freigabeprozess")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-282">**Share Process** ("Share Process")</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_Process"></span><span id="interactive_process"></span><span id="INTERACTIVE_PROCESS"></span>

<span data-ttu-id="4e9ef-283">**Interaktiver Prozess** ("interaktiver Prozess")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-283">**Interactive Process** ("Interactive Process")</span></span>


<span data-ttu-id="4e9ef-284"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="4e9ef-284"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="4e9ef-285">Diese Eigenschaft wird von [**Win32 \_ baseservice**](win32-baseservice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-285">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e9ef-286">**Gestartet**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-286">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e9ef-287">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="4e9ef-287">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4e9ef-288">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4e9ef-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e9ef-289">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Started")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-289">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Started")</span></span>
</dt> </dl>

<span data-ttu-id="4e9ef-290">Gibt an, ob der Dienst gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-290">Indicates whether or not the service is started.</span></span>

<span data-ttu-id="4e9ef-291">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](cim-service.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-291">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e9ef-292">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-292">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e9ef-293">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e9ef-294">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4e9ef-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e9ef-295">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Start Modus")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-295">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Start Mode")</span></span>
</dt> </dl>

<span data-ttu-id="4e9ef-296">Der Start Modus des Windows-Basis Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-296">Start mode of the Windows base service.</span></span>

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span data-ttu-id="4e9ef-297"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Start** ("Start")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-297"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Boot** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="4e9ef-298">Der Gerätetreiber wurde vom Betriebssystem Lader gestartet (nur für Treiber Dienste gültig).</span><span class="sxs-lookup"><span data-stu-id="4e9ef-298">Device driver started by the operating system loader (valid only for driver services).</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="4e9ef-299"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ("System")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-299"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="4e9ef-300">Der Gerätetreiber wurde durch den Initialisierungs Prozess des Betriebssystems gestartet.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-300">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="4e9ef-301">Dieses Wert ist nur für Treiberdienste gültig.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-301">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>

<span data-ttu-id="4e9ef-302"><span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Auto** ("Auto")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-302"><span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Auto** ("Auto")</span></span>


</dt> <dd>

<span data-ttu-id="4e9ef-303">Der Dienst soll während des Systemstarts automatisch vom Dienstkontroll-Manager gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-303">Service to be started automatically by the service control manager during system startup.</span></span> <span data-ttu-id="4e9ef-304">Automatische Dienste werden auch dann gestartet, wenn sich ein Benutzer nicht anmelden kann.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-304">Auto services are started even if a user does not log on.</span></span>

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="4e9ef-305"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manuell** ("manuell")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-305"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="4e9ef-306">Der Dienst, der vom Dienststeuerungs-Manager gestartet werden soll, wenn ein Prozess die [**StartService**](startservice-method-in-class-win32-service.md) -Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-306">Service to be started by the Service Control Manager when a process calls the [**StartService**](startservice-method-in-class-win32-service.md) method.</span></span> <span data-ttu-id="4e9ef-307">Diese Dienste werden erst gestartet, wenn sich ein Benutzer anmeldet und startet.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-307">These services do not start unless a user logs on and starts them.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="4e9ef-308"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** ("deaktiviert")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-308"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="4e9ef-309">Dienst, der erst gestartet werden kann, wenn sein StartMode entweder in "Auto" oder "manuell" geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-309">Service that cannot be started until its StartMode is changed to either Auto or Manual.</span></span>

</dd> </dl>

<span data-ttu-id="4e9ef-310">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](cim-service.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-310">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e9ef-311">**StartName**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-311">**StartName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e9ef-312">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e9ef-313">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4e9ef-313">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e9ef-314">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**Query \_ Service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| lpservicestartname"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Starting Account Name")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-314">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|lpServiceStartName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Starting Account Name")</span></span>
</dt> </dl>

<span data-ttu-id="4e9ef-315">Der Kontoname, unter dem ein Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-315">Account name under which a service runs.</span></span> <span data-ttu-id="4e9ef-316">Abhängig vom Diensttyp kann der Kontoname die Form "Domainname \\ username" oder das UPN-Format (" *Username@DomainName* ") aufweisen.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-316">Depending on the service type, the account name may be in the form of "DomainName\\Username" or UPN format ("*Username@DomainName*").</span></span> <span data-ttu-id="4e9ef-317">Der Dienst Prozess wird mit einer dieser beiden Formulare protokolliert, wenn er ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-317">The service process is logged by using one of these two forms when it runs.</span></span> <span data-ttu-id="4e9ef-318">Wenn das Konto zur integrierten Domäne gehört, dann ". \\ Username "kann angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-318">If the account belongs to the built-in domain, then ".\\Username" can be specified.</span></span> <span data-ttu-id="4e9ef-319">Für Treiber auf Kernel-oder Systemebene enthält **StartName** den Treiber Objektnamen (d. h. " \\ File System \\ rdr" oder " \\ Driver \\ XNS"), den das e/a-System zum Laden des Gerätetreibers verwendet.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-319">For kernel or system-level drivers, **StartName** contains the driver object name (that is, "\\FileSystem\\Rdr" or "\\Driver\\Xns") which the I/O system uses to load the device driver.</span></span> <span data-ttu-id="4e9ef-320">Wenn **null** angegeben wird, wird der Treiber mit einem Standard Objektnamen ausgeführt, der vom e/a-System basierend auf dem Dienstnamen erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-320">Additionally, if **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name.</span></span>

<span data-ttu-id="4e9ef-321">Beispiel: "dwdom \\ Admin"</span><span class="sxs-lookup"><span data-stu-id="4e9ef-321">Example: "DWDOM\\Admin"</span></span>

<span data-ttu-id="4e9ef-322">Diese Eigenschaft wird von [**Win32 \_ baseservice**](win32-baseservice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-322">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e9ef-323">**State**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-323">**State**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e9ef-324">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e9ef-325">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="4e9ef-325">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4e9ef-326">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**Service \_ Status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwcurrentstate"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("State")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-326">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwCurrentState "), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("State")</span></span>
</dt> </dl>

<span data-ttu-id="4e9ef-327">Aktueller Status des Basis Dienes.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-327">Current state of the base service.</span></span>

<span data-ttu-id="4e9ef-328">Die Werte sind:</span><span class="sxs-lookup"><span data-stu-id="4e9ef-328">The values are:</span></span>

<dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span data-ttu-id="4e9ef-329">**Beendet** ("beendet")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-329">**Stopped** ("Stopped")</span></span>


</dt> <dd></dd> <dt>

<span id="Start_Pending"></span><span id="start_pending"></span><span id="START_PENDING"></span>

<span data-ttu-id="4e9ef-330">**Start steht aus** ("ausstehende Start")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-330">**Start Pending** ("Start Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Stop_Pending"></span><span id="stop_pending"></span><span id="STOP_PENDING"></span>

<span data-ttu-id="4e9ef-331">**Ausstehende Beendigung** ("ausstehenden Vorgang nicht mehr")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-331">**Stop Pending** ("Stop Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="4e9ef-332">Wird **ausgeführt** ("wird ausgeführt")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-332">**Running** ("Running")</span></span>


</dt> <dd></dd> <dt>

<span id="Continue_Pending"></span><span id="continue_pending"></span><span id="CONTINUE_PENDING"></span>

<span data-ttu-id="4e9ef-333">**Ausstehende Fortsetzung** ("ausstehende Fortsetzung")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-333">**Continue Pending** ("Continue Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Pause_Pending"></span><span id="pause_pending"></span><span id="PAUSE_PENDING"></span>

<span data-ttu-id="4e9ef-334">Anhalten steht **aus** ("ausstehende Pause")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-334">**Pause Pending** ("Pause Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="4e9ef-335">**Angeh** alten ("angehalten")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-335">**Paused** ("Paused")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4e9ef-336">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-336">**Unknown** ("Unknown")</span></span>


<span data-ttu-id="4e9ef-337"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="4e9ef-337"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="4e9ef-338">**Windows Server 2008 und Windows Vista:** Diese Eigenschaft ist vor Windows 7 und Windows Server 2008 R2 schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-338">**Windows Server 2008 and Windows Vista:** This property is read-only before Windows 7 and Windows Server 2008 R2.</span></span>

<span data-ttu-id="4e9ef-339">Diese Eigenschaft wird von [**Win32 \_ baseservice**](win32-baseservice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-339">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e9ef-340">**Status**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-340">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e9ef-341">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-341">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e9ef-342">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4e9ef-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e9ef-343">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-343">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="4e9ef-344">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-344">Current status of the object.</span></span> <span data-ttu-id="4e9ef-345">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-345">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="4e9ef-346">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="4e9ef-346">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="4e9ef-347">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="4e9ef-347">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="4e9ef-348">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-348">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="4e9ef-349">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-349">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="4e9ef-350">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-350">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="4e9ef-351">Die Werte sind:</span><span class="sxs-lookup"><span data-stu-id="4e9ef-351">The values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="4e9ef-352">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-352">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="4e9ef-353">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-353">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="4e9ef-354">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-354">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4e9ef-355">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-355">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="4e9ef-356">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-356">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="4e9ef-357">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-357">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="4e9ef-358">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-358">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="4e9ef-359">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-359">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="4e9ef-360">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-360">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="4e9ef-361">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-361">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="4e9ef-362">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-362">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="4e9ef-363">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-363">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4e9ef-364">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-364">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e9ef-365">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-365">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e9ef-366">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4e9ef-366">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e9ef-367">Qualifizierer [**: weiter**](../wmisdk/standard-qualifiers.md) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Schlüssel**](../wmisdk/standard-wmi-qualifiers.md), [**Display Name**](../wmisdk/standard-qualifiers.md) ("System Klassenname")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-367">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="4e9ef-368">Der Typname des Systems, das den Dienst hostet.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-368">Type name of the system that hosts this service.</span></span>

<span data-ttu-id="4e9ef-369">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](cim-service.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-369">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e9ef-370">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-370">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e9ef-371">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-371">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e9ef-372">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4e9ef-372">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e9ef-373">Qualifizierer [**: weiter**](../wmisdk/standard-qualifiers.md) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md), [**Display Name**](../wmisdk/standard-qualifiers.md) (" System Name ")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-373">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("System Name")</span></span>
</dt> </dl>

<span data-ttu-id="4e9ef-374">Der Name des Systems, das den Dienst hostet.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-374">Name of the system that hosts this service.</span></span>

<span data-ttu-id="4e9ef-375">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](cim-service.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-375">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e9ef-376">**TagID**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-376">**TagId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e9ef-377">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-377">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4e9ef-378">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4e9ef-378">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e9ef-379">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**Query \_ Service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| dwtagid"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Tag ID")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-379">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|dwTagId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Tag Id")</span></span>
</dt> </dl>

<span data-ttu-id="4e9ef-380">Eindeutiger Tagwert für diesen Dienst in der Gruppe.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-380">Unique tag value for this service in the group.</span></span> <span data-ttu-id="4e9ef-381">Der Wert 0 (null) gibt an, dass der Dienst nicht über ein Tag verfügt.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-381">A value of 0 (zero) indicates that the service does not have a tag.</span></span> <span data-ttu-id="4e9ef-382">Ein-Tag kann verwendet werden, um den Dienst Start innerhalb einer Gruppe von Lade Reihenfolgen zu sortieren, indem Sie in der Registrierung einen taganordnungs Vektor angeben:</span><span class="sxs-lookup"><span data-stu-id="4e9ef-382">A tag can be used to order service startup within a load order group by specifying a tag order vector in the registry located at:</span></span>

<span data-ttu-id="4e9ef-383">**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Steuer** Element \\ **grouporderlist**    </span><span class="sxs-lookup"><span data-stu-id="4e9ef-383">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\    **GroupOrderList**</span></span>

<span data-ttu-id="4e9ef-384">Tags werden nur für Kernel Treiber-und Datei System Treiber-Starttyp Dienste ausgewertet, die über Start-oder System Start Modi verfügen.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-384">Tags are only evaluated for Kernel Driver and File System Driver start type services that have Boot or System start modes.</span></span>

<span data-ttu-id="4e9ef-385">Diese Eigenschaft wird von [**Win32 \_ baseservice**](win32-baseservice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-385">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e9ef-386">**WaitHint**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-386">**WaitHint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e9ef-387">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-387">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4e9ef-388">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4e9ef-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e9ef-389">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**Service \_ Status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwwaithint"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("geschätzte Wartezeit")</span><span class="sxs-lookup"><span data-stu-id="4e9ef-389">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwWaitHint"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Estimated Wait Time")</span></span>
</dt> </dl>

<span data-ttu-id="4e9ef-390">Geschätzte benötigte Zeit (in Millisekunden) für einen ausstehenden Start-, anhalte-, Anhaltevorgang-oder continue-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-390">Estimated time required, in milliseconds, for a pending start, stop, pause, or continue operation.</span></span> <span data-ttu-id="4e9ef-391">Nachdem die angegebene Zeit abgelaufen ist, führt der Dienst den nächsten Aufruf der **SetServiceStatus** -Methode mit einem **inkrementierten** Prüf Punkt Wert oder einer Änderung in **CurrentState** aus.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-391">After the specified time has elapsed, the service makes its next call to the **SetServiceStatus** method with either an incremented **CheckPoint** value or a change in **CurrentState**.</span></span> <span data-ttu-id="4e9ef-392">Wenn die von **WaitHint** angegebene Zeitspanne verstrichen **ist und der** Prüfpunkt nicht inkrementiert wurde, oder **CurrentState** nicht geändert wurde, geht der Dienststeuerungs-Manager oder das Dienst Steuerungsprogramm davon aus, dass ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-392">If the amount of time specified by **WaitHint** passes, and **CheckPoint** has not been incremented, or **CurrentState** has not changed, the service control manager or service control program assumes that an error has occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4e9ef-393">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4e9ef-393">Remarks</span></span>

<span data-ttu-id="4e9ef-394">Die **Win32- \_ Dienst** Klasse wird von [**Win32 \_ baseservice**](win32-baseservice.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-394">The **Win32\_Service** class is derived from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

<span data-ttu-id="4e9ef-395">Die Art und Weise, in der Sie einen bestimmten Computer verwalten, hängt stark von der Rolle des Computers ab.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-395">The way in which you manage a specific computer depends greatly on the role that computer plays.</span></span> <span data-ttu-id="4e9ef-396">Beispielsweise überwachen Sie im allgemeinen verschiedene Aspekte eines DNS-Servers als einen DHCP-Server.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-396">For example, you generally monitor different aspects of a DNS server than a DHCP server.</span></span> <span data-ttu-id="4e9ef-397">Obwohl keine einzelne Eigenschaft Aufschluss darüber geben kann, ob es sich bei einem bestimmten Computer um einen Datenbankserver, einen e-Mail-Server oder einen Multimedia-Server handelt, können Sie die Rolle eines Computers häufig ermitteln, indem Sie die installierten Dienste identifizieren.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-397">Although no single property can tell you whether a particular computer is a database server, an e-mail server, or a multimedia server, you can often identify the role a computer plays by identifying the services installed on it.</span></span>

<span data-ttu-id="4e9ef-398">In großen Organisationen ist es wahrscheinlich, dass nur einer der Haupt Dienste (z. b. e-Mail) auf einem einzelnen Computer installiert wird.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-398">In large organizations, only one of the major services (such as e-mail) is likely to be installed on a single computer.</span></span> <span data-ttu-id="4e9ef-399">Es ist nicht ungewöhnlich, dass ein Mailserver auch als Server für Microsoft® Windows Media® Technologies-Technologien Player-Dateien ausführt.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-399">It would be unusual for a mail server to also perform as a server for Microsoft® Windows Media® technologies player files.</span></span> <span data-ttu-id="4e9ef-400">Aus diesem Grund kann das Identifizieren eines auf einem Computer installierten Dienstanbieter helfen, die Rolle des Computers im Netzwerk zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-400">Because of this, identifying a service installed on a computer can help identify the computer's role in the network.</span></span> <span data-ttu-id="4e9ef-401">Wenn der Microsoft® Exchange Server-Dienst installiert ist und auf einem Computer ausgeführt wird, ist es im Allgemeinen sicher, dass dieser Computer als e-Mail-Server fungiert.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-401">If the Microsoft® Exchange Server service is installed and running on a computer, it is generally safe to assume that this computer functions as a mail server.</span></span>

<span data-ttu-id="4e9ef-402">Sie können die WMI- **Win32- \_ Dienst** Klasse verwenden, um die auf einem Computer installierten Dienste aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-402">You can use the WMI **Win32\_Service** class to enumerate the services installed on a computer.</span></span> <span data-ttu-id="4e9ef-403">Außerdem können Sie diese Klasse verwenden, um zu bestimmen, ob diese Dienste derzeit ausgeführt werden, und um alle anderen erforderlichen Informationen zu diesem Dienst und dessen Konfiguration zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-403">In addition, you can use this class to determine whether those services are currently running and to return any other required information about that service and how it has been configured.</span></span>

<span data-ttu-id="4e9ef-404">Eine-Dienst Anwendung entspricht den Schnittstellen Regeln des Dienststeuerungs-Managers (Service Control Manager, SCM) und kann von einem Benutzer automatisch beim Systemstart über das System Steuerungsprogramm "Dienste" oder durch eine Anwendung gestartet werden, die die in der Windows-API enthaltenen Dienstfunktionen verwendet.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-404">A service application conforms to the interface rules of the Service Control Manager (SCM), and can be started by a user automatically at system start through the Services control panel utility, or by an application that uses the service functions included in the Windows API.</span></span> <span data-ttu-id="4e9ef-405">Dienste können gestartet werden, wenn keine Benutzer am Computer angemeldet sind.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-405">Services can start when there are no users logged on to the computer.</span></span>

<span data-ttu-id="4e9ef-406">Ein Benutzer, der eine Verbindung über einen Remote Computer herstellt, muss über die Berechtigung **SC- \_ Manager \_ Connect** verfügen, damit diese Klasse aufgelistet werden kann.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-406">A user connecting from a remote computer must have the **SC\_MANAGER\_CONNECT** privilege enabled to be able to enumerate this class.</span></span> <span data-ttu-id="4e9ef-407">Weitere Informationen finden Sie unter [Dienst Sicherheit und Zugriffsrechte](../services/service-security-and-access-rights.md).</span><span class="sxs-lookup"><span data-stu-id="4e9ef-407">For more information, see [Service Security and Access Rights](../services/service-security-and-access-rights.md).</span></span>

## <a name="examples"></a><span data-ttu-id="4e9ef-408">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4e9ef-408">Examples</span></span>

<span data-ttu-id="4e9ef-409">Die [PS-WMI-Abfrage, die den Dienst "State" für eine Gruppe von Geräten](https://Gallery.TechNet.Microsoft.Com/0f1ab629-d463-4406-be54-ec2c4c23bc1f) PowerShell-Beispiel in der TechNet Gallery zurückgibt, verwendet den **Win32- \_ Dienst** , um eine Liste der Geräte aus Active Directory zu erstellen und anschließend jedes Gerät abzufragen, das mit pingfor einen bestimmten Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-409">The [PS- WMI Query that returns Service 'State' on a group of devices](https://Gallery.TechNet.Microsoft.Com/0f1ab629-d463-4406-be54-ec2c4c23bc1f) PowerShell sample on TechNet Gallery uses **Win32\_Service** to create a list of devices from Active Directory, and then query each device that responds with pingfor a specific service running.</span></span>

<span data-ttu-id="4e9ef-410">Das PowerShell-Beispiel für [Server Berichte](https://Gallery.TechNet.Microsoft.Com/Server-Report-7b4ac2fb) in der TechNet Gallery verwendet den **Win32- \_ Dienst** zum Erfassen von Server Informationen und veröffentlichen im Word-Dokument.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-410">The [Server Report](https://Gallery.TechNet.Microsoft.Com/Server-Report-7b4ac2fb) PowerShell sample on TechNet Gallery uses **Win32\_Service** to gather server information and publish in Word document.</span></span>

<span data-ttu-id="4e9ef-411">Im folgenden VBScript-Codebeispiel werden alle zurzeit installierten Dienste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-411">The following VBScript code sample displays all currently installed services.</span></span>


```VB
for each Service in _ 
    GetObject("winmgmts:").InstancesOf ("Win32_Service")
 WScript.Echo ""
 WScript.Echo Service.Name

 description = Service.Description 
 if IsNull(description) then description = "<No description>"

 pathName = Service.PathName
 if IsNull(pathName) then pathName = "<No path>"

 startName = Service.StartName
 if IsNull(startName) then startName = "<None>"

 WScript.Echo "  Description:  ", description
 WScript.Echo "  Executable:   ", pathName
 WScript.Echo "  Status:       ", Service.Status
 WScript.Echo "  State:        ", Service.State
 WScript.Echo "  Start Mode:   ", Service.StartMode
 Wscript.Echo "  Start Name:   ", startName
next
```



<span data-ttu-id="4e9ef-412">Im folgenden VBScript-Codebeispiel werden die angehaltenen, laufenden und beendeten Dienste auf dem angegebenen Computer beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-412">The following VBScript code sample describes the paused, running, and stopped services on the specified computer.</span></span>


```VB
On Error Resume Next
 StateString = "Paused,Running,Stopped"
 StateArray = Split(StateString, ",", -1, 1) 
 ComputerName = InputBox("Enter the computer name", "List Service", "localhost")

 For x = 0 to Ubound (StateArray)
 Set Services = GetObject("winmgmts:\\" & ComputerName & "\Root\CIMv2").ExecQuery("SELECT * FROM Win32_Service where State='" & StateArray(x) & "'")
 
 For Each Service in Services
  SList = SList & Service.Name & VBlf 
 Next

 WScript.Echo StateArray(x) & " Services: " & VBlf & SList
 SList = ""

Next
```



<span data-ttu-id="4e9ef-413">Das folgende perl-Skript veranschaulicht, wie Sie eine Liste der laufenden Dienste aus Instanzen des **Win32- \_ Diensts** abrufen.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-413">The following Perl script demonstrates how to retrieve a list of running services from instances of **Win32\_Service**.</span></span>


```
use strict;
use Win32::OLE;

my ( $ServiceSet, $Service );

eval { $ServiceSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\Root\\CIMv2")->
 ExecQuery("SELECT * FROM Win32_Service WHERE State=\"Running\""); };
unless ($@)
{
 print "\n";
 foreach $Service (in $ServiceSet) 
 {
  print $Service->{Name}, "\n";
  if( $Service->{Description} ) 
   {
    print "  $Service->{Description}\n";
   }
  else
   {
    print "  <No description>\n";
   }
  print "  Process ID: ", $Service->{ProcessId}, "\n";
  print "  Start Mode: ", $Service->{StartMode}, "\n";
  print "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



<span data-ttu-id="4e9ef-414">Im folgenden c- \# Beispiel wird [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) verwendet, um alle laufenden Dienste auf dem lokalen Computer abzurufen.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-414">The following c\# sample uses [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) to retrieve all the running services on the local machine.</span></span>


```CSharp
static void QueryInstanceFunc()
        {
 
            CimSession session = CimSession.Create("localHost");
            IEnumerable<CimInstance> queryInstance = session.QueryInstances(@"root\cimv2", "WQL", "SELECT * FROM Win32_Service");

            foreach (CimInstance cimObj in queryInstance)
            {
                Console.WriteLine(cimObj.CimInstanceProperties["Name"].ToString());
                Console.WriteLine(cimObj.CimInstanceProperties["State"].ToString());
                Console.WriteLine(cimObj.CimInstanceProperties["Status"].ToString());
                
                //Console.WriteLine(cimObj.CimInstanceProperties["NetworkAddress"].ToString());
                Console.WriteLine();

            }

            Console.ReadLine();
        }
    
```



<span data-ttu-id="4e9ef-415">Im folgenden C- \# Codebeispiel wird der [System. Management](/dotnet/api/system.management) -Namespace verwendet, um alle laufenden Dienste auf dem lokalen Computer abzurufen.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-415">The following C\# code sample uses [System.Management](/dotnet/api/system.management) namespace to retrieve all running services on the local machine.</span></span>

> [!Note]  
> <span data-ttu-id="4e9ef-416">[System. Management](/dotnet/api/system.management) enthält die ursprünglichen Klassen, die für den Zugriff auf WMI verwendet werden. Allerdings gelten Sie als langsamer und werden im Allgemeinen nicht ebenso skaliert wie Ihre [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) -Entsprechungen.</span><span class="sxs-lookup"><span data-stu-id="4e9ef-416">[System.Management](/dotnet/api/system.management) contains the original classes used to access WMI; however, they are considered slower and generally do not scale as well as their [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) counterparts.</span></span>

 


```CSharp
using System.Management;
...
        static void oldSchoolQueryInstanceFunc()
        {

            ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_Service");
            ManagementObjectSearcher searcher = new ManagementObjectSearcher(query);


            ManagementObjectCollection queryCollection = searcher.Get();
            foreach (ManagementObject m in queryCollection)
            {
                Console.WriteLine("ServiceName : {0}", m["Name"]);
                Console.WriteLine("State : {0}", m["State"]);
                Console.WriteLine("Status : {0}", m["Status"]);
                Console.WriteLine();
            }

            Console.ReadLine();


        }
```



## <a name="requirements"></a><span data-ttu-id="4e9ef-417">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4e9ef-417">Requirements</span></span>



| <span data-ttu-id="4e9ef-418">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4e9ef-418">Requirement</span></span> | <span data-ttu-id="4e9ef-419">Wert</span><span class="sxs-lookup"><span data-stu-id="4e9ef-419">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e9ef-420">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4e9ef-420">Minimum supported client</span></span><br/> | <span data-ttu-id="4e9ef-421">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4e9ef-421">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4e9ef-422">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4e9ef-422">Minimum supported server</span></span><br/> | <span data-ttu-id="4e9ef-423">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4e9ef-423">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4e9ef-424">Namespace</span><span class="sxs-lookup"><span data-stu-id="4e9ef-424">Namespace</span></span><br/>                | <span data-ttu-id="4e9ef-425">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4e9ef-425">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4e9ef-426">MOF</span><span class="sxs-lookup"><span data-stu-id="4e9ef-426">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4e9ef-427"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="4e9ef-427"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4e9ef-428">DLL</span><span class="sxs-lookup"><span data-stu-id="4e9ef-428">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e9ef-429"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e9ef-429"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e9ef-430">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4e9ef-430">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e9ef-431">**Win32- \_ baseservice**</span><span class="sxs-lookup"><span data-stu-id="4e9ef-431">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> <dt>

[<span data-ttu-id="4e9ef-432">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="4e9ef-432">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="4e9ef-433">WMI-Tasks: Dienste</span><span class="sxs-lookup"><span data-stu-id="4e9ef-433">WMI Tasks: Services</span></span>](../wmisdk/wmi-tasks--services.md)
</dt> </dl>

 

 
