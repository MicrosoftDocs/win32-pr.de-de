---
description: Die \_ WMI-Klasse der WMI-Klasse "Win32 baseservice" stellt ausführbare Objekte dar, die in einer vom Dienststeuerungs-Manager verwalteten Registrierungsdatenbank installiert werden
ms.assetid: 63673df9-3e41-4668-98fe-dc0e048328c1
ms.tgt_platform: multiple
title: Win32_BaseService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService
- Win32_BaseService.AcceptPause
- Win32_BaseService.AcceptStop
- Win32_BaseService.Caption
- Win32_BaseService.CreationClassName
- Win32_BaseService.Description
- Win32_BaseService.DesktopInteract
- Win32_BaseService.DisplayName
- Win32_BaseService.ErrorControl
- Win32_BaseService.ExitCode
- Win32_BaseService.InstallDate
- Win32_BaseService.Name
- Win32_BaseService.PathName
- Win32_BaseService.ServiceSpecificExitCode
- Win32_BaseService.ServiceType
- Win32_BaseService.Started
- Win32_BaseService.StartMode
- Win32_BaseService.StartName
- Win32_BaseService.State
- Win32_BaseService.Status
- Win32_BaseService.SystemCreationClassName
- Win32_BaseService.SystemName
- Win32_BaseService.TagId
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b46f3b4bd37770a5f3a7c1a2d2faa93d49bc079a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127488"
---
# <a name="win32_baseservice-class"></a><span data-ttu-id="d0eb0-103">Win32 \_ baseservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="d0eb0-103">Win32\_BaseService class</span></span>

<span data-ttu-id="d0eb0-104">Die [WMI-Klasse der WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) " **Win32 \_ baseservice** " stellt ausführbare Objekte dar, die in einer vom Dienststeuerungs-Manager verwalteten Registrierungsdatenbank installiert werden</span><span class="sxs-lookup"><span data-stu-id="d0eb0-104">The **Win32\_BaseService** abstract [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents executable objects that are installed in a registry database maintained by the Service Control Manager.</span></span> <span data-ttu-id="d0eb0-105">Die mit einem Dienst verknüpfte ausführbare Datei kann beim Start von einem Start Programm oder vom System gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-105">The executable file associated with a service can be started at boot time by a boot program or by the system.</span></span> <span data-ttu-id="d0eb0-106">Sie kann auch bei Bedarf vom Dienststeuerungs-Manager gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-106">It can also be started on-demand by the Service Control Manager.</span></span> <span data-ttu-id="d0eb0-107">Dienste oder Prozesse, die nicht im Besitz eines bestimmten Benutzers sind und eine Schnittstelle für einige Funktionen bereitstellen, die vom Computersystem unterstützt werden, sind ein Nachfolger (oder Mitglied) dieser Klasse.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-107">Any service or process that is not owned by a specific user, and that provides an interface to some functionality supported by the computer system, is a descendant (or member) of this class.</span></span>

<span data-ttu-id="d0eb0-108">Beispiel: der DHCP-Client Dienst (Dynamic Host Configuration-Protokoll) auf einem Computersystem, auf dem Windows Server ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-108">Example: The dynamic host configuration protocol (DHCP) client service on a computer system running Windows Server.</span></span>

<span data-ttu-id="d0eb0-109">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="d0eb0-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0eb0-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="d0eb0-111">Syntax</span></span>

``` syntax
[SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("DeleteInstance"), Abstract, Provider("CIMWin32"), UUID("{8502C4C4-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("System Drivers and Services"), AMENDMENT]
class Win32_BaseService : CIM_Service
{
  boolean  AcceptPause;
  boolean  AcceptStop;
  string   Caption;
  string   CreationClassName;
  string   Description;
  boolean  DesktopInteract;
  string   DisplayName;
  string   ErrorControl;
  uint32   ExitCode;
  datetime InstallDate;
  string   Name;
  string   PathName;
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
};
```

## <a name="members"></a><span data-ttu-id="d0eb0-112">Member</span><span class="sxs-lookup"><span data-stu-id="d0eb0-112">Members</span></span>

<span data-ttu-id="d0eb0-113">Die **Win32 \_ baseservice** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d0eb0-113">The **Win32\_BaseService** class has these types of members:</span></span>

-   [<span data-ttu-id="d0eb0-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="d0eb0-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="d0eb0-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d0eb0-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d0eb0-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="d0eb0-116">Methods</span></span>

<span data-ttu-id="d0eb0-117">Die **Win32 \_ baseservice** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-117">The **Win32\_BaseService** class has these methods.</span></span>



| <span data-ttu-id="d0eb0-118">Methode</span><span class="sxs-lookup"><span data-stu-id="d0eb0-118">Method</span></span>                                                                             | <span data-ttu-id="d0eb0-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d0eb0-119">Description</span></span>                                                                   |
|:-----------------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="d0eb0-120">**Klima**</span><span class="sxs-lookup"><span data-stu-id="d0eb0-120">**Change**</span></span>](change-method-in-class-win32-baseservice.md)                         | <span data-ttu-id="d0eb0-121">Ändert einen Dienst.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-121">Modifies a service.</span></span><br/>                                                |
| [<span data-ttu-id="d0eb0-122">**ChangeStartMode**</span><span class="sxs-lookup"><span data-stu-id="d0eb0-122">**ChangeStartMode**</span></span>](changestartmode-method-in-class-win32-baseservice.md)       | <span data-ttu-id="d0eb0-123">Ändert den Start Modus eines Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-123">Modifies the start mode of a service.</span></span><br/>                              |
| [<span data-ttu-id="d0eb0-124">**Stelle**</span><span class="sxs-lookup"><span data-stu-id="d0eb0-124">**Create**</span></span>](create-method-in-class-win32-baseservice.md)                         | <span data-ttu-id="d0eb0-125">Erstellt einen neuen Dienst.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-125">Creates a new service.</span></span><br/>                                             |
| [<span data-ttu-id="d0eb0-126">**Lösch**</span><span class="sxs-lookup"><span data-stu-id="d0eb0-126">**Delete**</span></span>](delete-method-in-class-win32-baseservice.md)                         | <span data-ttu-id="d0eb0-127">Löscht einen vorhandenen Dienst.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-127">Deletes an existing service.</span></span><br/>                                       |
| [<span data-ttu-id="d0eb0-128">**"InterrogateService"**</span><span class="sxs-lookup"><span data-stu-id="d0eb0-128">**InterrogateService**</span></span>](interrogateservice-method-in-class-win32-baseservice.md) | <span data-ttu-id="d0eb0-129">Fordert an, dass der Dienst seinen Status an Service Manager aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-129">Requests that the service update its state to the service manager.</span></span><br/> |
| [<span data-ttu-id="d0eb0-130">**PauseService**</span><span class="sxs-lookup"><span data-stu-id="d0eb0-130">**PauseService**</span></span>](pauseservice-method-in-class-win32-baseservice.md)             | <span data-ttu-id="d0eb0-131">Versucht, den Dienst anzuhalten.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-131">Attempts to place the service in the paused state.</span></span><br/>                 |
| [<span data-ttu-id="d0eb0-132">**ResumeService**</span><span class="sxs-lookup"><span data-stu-id="d0eb0-132">**ResumeService**</span></span>](resumeservice-method-in-class-win32-baseservice.md)           | <span data-ttu-id="d0eb0-133">Versucht, den Dienst fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-133">Attempts to place the service in the resumed state.</span></span><br/>                |
| [<span data-ttu-id="d0eb0-134">**Start Service**</span><span class="sxs-lookup"><span data-stu-id="d0eb0-134">**StartService**</span></span>](startservice-method-in-class-win32-baseservice.md)             | <span data-ttu-id="d0eb0-135">Versucht, den Dienst in seinen Startzustand zu versetzen.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-135">Attempts to place the service into its startup state.</span></span><br/>              |
| [<span data-ttu-id="d0eb0-136">**Stop Service**</span><span class="sxs-lookup"><span data-stu-id="d0eb0-136">**StopService**</span></span>](stopservice-method-in-class-win32-baseservice.md)               | <span data-ttu-id="d0eb0-137">Klassenmethode, die den Dienst in den Zustand "beendet" versetzt.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-137">Class method that places the service in the stopped state.</span></span><br/>         |
| [<span data-ttu-id="d0eb0-138">**UserControlService**</span><span class="sxs-lookup"><span data-stu-id="d0eb0-138">**UserControlService**</span></span>](usercontrolservice-method-in-class-win32-baseservice.md) | <span data-ttu-id="d0eb0-139">Versucht, einen benutzerdefinierten Steuerelement Code an einen Dienst zu senden.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-139">Attempts to send a user-defined control code to a service.</span></span><br/>         |



 

### <a name="properties"></a><span data-ttu-id="d0eb0-140">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d0eb0-140">Properties</span></span>

<span data-ttu-id="d0eb0-141">Die **Win32 \_ baseservice** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-141">The **Win32\_BaseService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d0eb0-142">**AcceptPause**</span><span class="sxs-lookup"><span data-stu-id="d0eb0-142">**AcceptPause**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0eb0-143">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="d0eb0-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d0eb0-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d0eb0-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0eb0-145">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API Service \| Structures \| [**Service \_ Status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwcontrolsaccepted \| Service \_ Accept \_ Pause \_ Continue"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Accept Pause")</span><span class="sxs-lookup"><span data-stu-id="d0eb0-145">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwControlsAccepted\|SERVICE\_ACCEPT\_PAUSE\_CONTINUE"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Accepts Pause")</span></span>
</dt> </dl>

<span data-ttu-id="d0eb0-146">Der Dienst kann angehalten werden.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-146">Service can be paused.</span></span>

</dd> <dt>

<span data-ttu-id="d0eb0-147">**AcceptStop**</span><span class="sxs-lookup"><span data-stu-id="d0eb0-147">**AcceptStop**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0eb0-148">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="d0eb0-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d0eb0-149">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d0eb0-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0eb0-150">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API Service \| Structures \| [**Service \_ Status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwcontrolsaccepted \| Service \_ Accept End \_ "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("der Dienst akzeptiert das Ende")</span><span class="sxs-lookup"><span data-stu-id="d0eb0-150">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwControlsAccepted\|SERVICE\_ACCEPT\_STOP"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Accepts Stop")</span></span>
</dt> </dl>

<span data-ttu-id="d0eb0-151">Der Dienst kann angehalten werden.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-151">Service can be stopped.</span></span>

</dd> <dt>

<span data-ttu-id="d0eb0-152">**Caption**</span><span class="sxs-lookup"><span data-stu-id="d0eb0-152">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0eb0-153">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d0eb0-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0eb0-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d0eb0-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0eb0-155">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="d0eb0-155">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="d0eb0-156">Kurze Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-156">Short description of the object.</span></span>

<span data-ttu-id="d0eb0-157">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0eb0-158">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="d0eb0-158">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0eb0-159">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d0eb0-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0eb0-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d0eb0-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0eb0-161">Qualifizierer: [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span><span class="sxs-lookup"><span data-stu-id="d0eb0-161">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="d0eb0-162">Der Name der ersten konkreten Klasse, die in der Vererbungs Kette angezeigt werden soll, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-162">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="d0eb0-163">Bei Verwendung mit den anderen Schlüsseleigenschaften der-Klasse ermöglicht die-Eigenschaft, dass alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-163">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="d0eb0-164">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](cim-service.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-164">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0eb0-165">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d0eb0-165">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0eb0-166">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d0eb0-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0eb0-167">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d0eb0-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0eb0-168">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="d0eb0-168">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="d0eb0-169">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-169">Description of the object.</span></span>

<span data-ttu-id="d0eb0-170">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-170">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0eb0-171">**DesktopInteract**</span><span class="sxs-lookup"><span data-stu-id="d0eb0-171">**DesktopInteract**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0eb0-172">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="d0eb0-172">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d0eb0-173">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d0eb0-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0eb0-174">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwservicetype \| Service \_ Interactive \_ Process"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("interagiert with Desktop")</span><span class="sxs-lookup"><span data-stu-id="d0eb0-174">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|dwServiceType\|SERVICE\_INTERACTIVE\_PROCESS"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Interacts With Desktop")</span></span>
</dt> </dl>

<span data-ttu-id="d0eb0-175">Der Dienst kann Windows auf dem Desktop erstellen oder mit ihm kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-175">Service can create or communicate with windows on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="d0eb0-176">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="d0eb0-176">**DisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0eb0-177">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d0eb0-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0eb0-178">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d0eb0-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0eb0-179">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| lpdisplayname"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Anzeige Name")</span><span class="sxs-lookup"><span data-stu-id="d0eb0-179">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|lpDisplayName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Display Name")</span></span>
</dt> </dl>

<span data-ttu-id="d0eb0-180">Der Anzeige Name des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-180">Display name of the service.</span></span> <span data-ttu-id="d0eb0-181">Die maximale Länge der Zeichenfolge beträgt 256 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-181">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="d0eb0-182">Der Name wird im Dienststeuerungs-Manager nach Groß-/Kleinschreibung beibehalten.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-182">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="d0eb0-183">Bei Vergleichen von **Display Name** wird immer die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-183">Comparisons of **DisplayName** are always case-insensitive.</span></span>

<span data-ttu-id="d0eb0-184">Einschränkungen: akzeptiert denselben Wert wie die **Name** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-184">Constraints: Accepts the same value as the **Name** property.</span></span>

<span data-ttu-id="d0eb0-185">Beispiel: "ATDISK"</span><span class="sxs-lookup"><span data-stu-id="d0eb0-185">Example: "Atdisk"</span></span>

</dd> <dt>

<span data-ttu-id="d0eb0-186">**ErrorControl**</span><span class="sxs-lookup"><span data-stu-id="d0eb0-186">**ErrorControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0eb0-187">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d0eb0-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0eb0-188">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d0eb0-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0eb0-189">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwerrorcontrol"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Schweregrad des Start Fehlers")</span><span class="sxs-lookup"><span data-stu-id="d0eb0-189">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|dwErrorControl"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Severity Of Startup Failure")</span></span>
</dt> </dl>

<span data-ttu-id="d0eb0-190">Der Schweregrad des Fehlers.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-190">Severity of the error.</span></span> <span data-ttu-id="d0eb0-191">Der Dienst kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-191">Service fails to start.</span></span> <span data-ttu-id="d0eb0-192">Der Wert gibt die vom Start Programm ausgeführte Aktion an, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-192">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="d0eb0-193">Alle Fehler werden vom Computersystem protokolliert.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-193">All errors are logged by the computer system.</span></span>

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span data-ttu-id="d0eb0-194"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignorieren** ("ignorieren")</span><span class="sxs-lookup"><span data-stu-id="d0eb0-194"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignore** ("Ignore")</span></span>


</dt> <dd>

<span data-ttu-id="d0eb0-195">Der Benutzer wird nicht benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-195">User is not notified.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="d0eb0-196"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** ("Normal")</span><span class="sxs-lookup"><span data-stu-id="d0eb0-196"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** ("Normal")</span></span>


</dt> <dd>

<span data-ttu-id="d0eb0-197">Der Benutzer wird benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-197">User is notified.</span></span>

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span data-ttu-id="d0eb0-198"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Schwerwiegend** ("schwerwiegend")</span><span class="sxs-lookup"><span data-stu-id="d0eb0-198"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Severe** ("Severe")</span></span>


</dt> <dd>

<span data-ttu-id="d0eb0-199">Das System wurde mit der zuletzt bekannten, guten Konfiguration neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-199">System restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="d0eb0-200"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Kritisch** ("kritisch")</span><span class="sxs-lookup"><span data-stu-id="d0eb0-200"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** ("Critical")</span></span>


</dt> <dd>

<span data-ttu-id="d0eb0-201">Das System versucht, mit einer fehlerfreien Konfiguration zu neu starten.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-201">System attempts to restart with a good configuration.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d0eb0-202"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="d0eb0-202"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** ("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="d0eb0-203">Die ausgeführte Aktion ist nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-203">Action taken is unspecified.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d0eb0-204">**Exitcode**</span><span class="sxs-lookup"><span data-stu-id="d0eb0-204">**ExitCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0eb0-205">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d0eb0-205">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d0eb0-206">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d0eb0-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0eb0-207">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Service \_ Status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwWin32ExitCode"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Exitcode")</span><span class="sxs-lookup"><span data-stu-id="d0eb0-207">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwWin32ExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Exit Code")</span></span>
</dt> </dl>

<span data-ttu-id="d0eb0-208">Definieren von Problemen, die beim Starten oder Beenden des Dienstanbieter aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-208">Defining any problems encountered in starting or stopping the service.</span></span> <span data-ttu-id="d0eb0-209">Diese Eigenschaft ist auf **Fehler \_ Dienst \_ spezifischer \_ Fehler** (1066) festgelegt, wenn der Fehler für den Dienst eindeutig ist, der durch diese Klasse dargestellt wird. Informationen über den Fehler sind in der **ServiceSpecificExitCode** -Eigenschaft verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-209">This property is set to **ERROR\_SERVICE\_SPECIFIC\_ERROR** (1066) when the error is unique to the service represented by this class, and information about the error is available in the **ServiceSpecificExitCode** property.</span></span> <span data-ttu-id="d0eb0-210">Der Dienst legt diesen Wert bei der Ausführung und erneut bei normaler Beendigung auf **keinen \_ Fehler** fest.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-210">The service sets this value to **NO\_ERROR** when running, and again upon normal termination.</span></span>

</dd> <dt>

<span data-ttu-id="d0eb0-211">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d0eb0-211">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0eb0-212">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="d0eb0-212">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d0eb0-213">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d0eb0-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0eb0-214">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="d0eb0-214">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="d0eb0-215">Das Objekt wurde installiert.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-215">Object was installed.</span></span> <span data-ttu-id="d0eb0-216">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-216">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="d0eb0-217">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-217">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0eb0-218">**Name**</span><span class="sxs-lookup"><span data-stu-id="d0eb0-218">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0eb0-219">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d0eb0-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0eb0-220">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d0eb0-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0eb0-221">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d0eb0-221">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d0eb0-222">Eindeutiger Bezeichner für den Dienst, der eine Angabe der verwalteten Funktionalität bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-222">Unique identifier of the service, which provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="d0eb0-223">Diese Funktionalität wird in der **Description** -Eigenschaft des Objekts ausführlicher beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-223">This functionality is described in more detail in the object's **Description** property.</span></span>

<span data-ttu-id="d0eb0-224">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-224">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0eb0-225">**PathName**</span><span class="sxs-lookup"><span data-stu-id="d0eb0-225">**PathName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0eb0-226">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d0eb0-226">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0eb0-227">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d0eb0-227">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0eb0-228">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| lpbinarypathname"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dateipfadname")</span><span class="sxs-lookup"><span data-stu-id="d0eb0-228">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|lpBinaryPathName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Path Name")</span></span>
</dt> </dl>

<span data-ttu-id="d0eb0-229">Der voll qualifizierte Pfad der Dienst Binärdatei, die den Dienst implementiert.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-229">Fully qualified path to the service binary file that implements the service.</span></span>

<span data-ttu-id="d0eb0-230">Beispiel: " \\ systemroot \\ system32 \\ Drivers \\afd.sys"</span><span class="sxs-lookup"><span data-stu-id="d0eb0-230">Example: "\\SystemRoot\\System32\\drivers\\afd.sys"</span></span>

</dd> <dt>

<span data-ttu-id="d0eb0-231">**ServiceSpecificExitCode**</span><span class="sxs-lookup"><span data-stu-id="d0eb0-231">**ServiceSpecificExitCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0eb0-232">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d0eb0-232">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d0eb0-233">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d0eb0-233">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0eb0-234">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Service \_ Status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwservicespecificexitcode"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Server spezifischer Exitcode")</span><span class="sxs-lookup"><span data-stu-id="d0eb0-234">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwServiceSpecificExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Server Specific Exit Code")</span></span>
</dt> </dl>

<span data-ttu-id="d0eb0-235">Dienst spezifischer Fehlercode für Fehler, die auftreten, während der Dienst gestartet oder beendet wird.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-235">Service-specific error code for errors that occur while the service is either starting or stopping.</span></span> <span data-ttu-id="d0eb0-236">Die Exitcodes werden von dem Dienst definiert, der durch diese Klasse dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-236">The exit codes are defined by the service represented by this class.</span></span> <span data-ttu-id="d0eb0-237">Dieser Wert wird nur festgelegt, wenn der **exitcodeproperty** -Wert " **Error \_ Service \_ Specific \_ Error** " (1066) ist.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-237">This value is only set when the **ExitCodeproperty** value is **ERROR\_SERVICE\_SPECIFIC\_ERROR** (1066).</span></span>

</dd> <dt>

<span data-ttu-id="d0eb0-238">**ServiceType**</span><span class="sxs-lookup"><span data-stu-id="d0eb0-238">**ServiceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0eb0-239">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d0eb0-239">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0eb0-240">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d0eb0-240">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0eb0-241">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwservicetype"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Type")</span><span class="sxs-lookup"><span data-stu-id="d0eb0-241">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|dwServiceType"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Type")</span></span>
</dt> </dl>

<span data-ttu-id="d0eb0-242">Der Dienst wurde für aufrufenden Prozesse bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-242">Service provided to calling processes.</span></span>

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

<span data-ttu-id="d0eb0-243">**Kernel Treiber** ("Kernel Treiber")</span><span class="sxs-lookup"><span data-stu-id="d0eb0-243">**Kernel Driver** ("Kernel Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

<span data-ttu-id="d0eb0-244">**Dateisystem Treiber** ("Dateisystem Treiber")</span><span class="sxs-lookup"><span data-stu-id="d0eb0-244">**File System Driver** ("File System Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

<span data-ttu-id="d0eb0-245">**Adapter** ("Adapter")</span><span class="sxs-lookup"><span data-stu-id="d0eb0-245">**Adapter** ("Adapter")</span></span>


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

<span data-ttu-id="d0eb0-246">**Erkennungs Treiber** ("Erkennungs Treiber")</span><span class="sxs-lookup"><span data-stu-id="d0eb0-246">**Recognizer Driver** ("Recognizer Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

<span data-ttu-id="d0eb0-247">**Eigener Prozess** ("eigener Prozess")</span><span class="sxs-lookup"><span data-stu-id="d0eb0-247">**Own Process** ("Own Process")</span></span>


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

<span data-ttu-id="d0eb0-248">**Freigabeprozess** ("Freigabeprozess")</span><span class="sxs-lookup"><span data-stu-id="d0eb0-248">**Share Process** ("Share Process")</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_Process"></span><span id="interactive_process"></span><span id="INTERACTIVE_PROCESS"></span>

<span data-ttu-id="d0eb0-249">**Interaktiver Prozess** ("interaktiver Prozess")</span><span class="sxs-lookup"><span data-stu-id="d0eb0-249">**Interactive Process** ("Interactive Process")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d0eb0-250">**Gestartet**</span><span class="sxs-lookup"><span data-stu-id="d0eb0-250">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0eb0-251">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="d0eb0-251">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d0eb0-252">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d0eb0-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0eb0-253">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")</span><span class="sxs-lookup"><span data-stu-id="d0eb0-253">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")</span></span>
</dt> </dl>

<span data-ttu-id="d0eb0-254">Der Dienst wurde gestartet.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-254">Service has been started.</span></span>

<span data-ttu-id="d0eb0-255">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](cim-service.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-255">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0eb0-256">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="d0eb0-256">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0eb0-257">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d0eb0-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0eb0-258">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d0eb0-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0eb0-259">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("StartMode"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Start Modus")</span><span class="sxs-lookup"><span data-stu-id="d0eb0-259">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("StartMode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Start Mode")</span></span>
</dt> </dl>

<span data-ttu-id="d0eb0-260">Der Start Modus des Windows-Basis Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-260">Start mode of the Windows base service.</span></span>

<span data-ttu-id="d0eb0-261">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](cim-service.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-261">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span data-ttu-id="d0eb0-262"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Start** ("Start")</span><span class="sxs-lookup"><span data-stu-id="d0eb0-262"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Boot** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="d0eb0-263">Der Gerätetreiber wurde vom Betriebssystem Lader gestartet (nur für Treiber Dienste gültig).</span><span class="sxs-lookup"><span data-stu-id="d0eb0-263">Device driver started by the operating system loader (valid only for driver services).</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="d0eb0-264"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ("System")</span><span class="sxs-lookup"><span data-stu-id="d0eb0-264"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="d0eb0-265">Der Gerätetreiber wurde durch den Initialisierungs Prozess des Betriebssystems gestartet.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-265">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="d0eb0-266">Dieses Wert ist nur für Treiberdienste gültig.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-266">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>

<span data-ttu-id="d0eb0-267"><span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Auto** ("Auto")</span><span class="sxs-lookup"><span data-stu-id="d0eb0-267"><span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Auto** ("Auto")</span></span>


</dt> <dd>

<span data-ttu-id="d0eb0-268">Dienst, der vom Dienststeuerungs-Manager beim Systemstart automatisch gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-268">Service to be started automatically by the service control manager during system start up.</span></span>

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="d0eb0-269"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manuell** ("manuell")</span><span class="sxs-lookup"><span data-stu-id="d0eb0-269"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="d0eb0-270">Der Dienst, der vom Dienststeuerungs-Manager gestartet werden soll, wenn ein Prozess die [**StartService**](startservice-method-in-class-win32-baseservice.md) -Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-270">Service to be started by the service control manager when a process calls the [**StartService**](startservice-method-in-class-win32-baseservice.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="d0eb0-271"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** ("deaktiviert")</span><span class="sxs-lookup"><span data-stu-id="d0eb0-271"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="d0eb0-272">Dienst, der nicht mehr gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-272">Service that can no longer be started.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d0eb0-273">**StartName**</span><span class="sxs-lookup"><span data-stu-id="d0eb0-273">**StartName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0eb0-274">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d0eb0-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0eb0-275">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d0eb0-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0eb0-276">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| lpservicestartname"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Starting Account Name")</span><span class="sxs-lookup"><span data-stu-id="d0eb0-276">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|lpServiceStartName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Starting Account Name")</span></span>
</dt> </dl>

<span data-ttu-id="d0eb0-277">Der Kontoname, unter dem der Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-277">Account name under which the service runs.</span></span> <span data-ttu-id="d0eb0-278">Abhängig vom Diensttyp kann der Kontoname die Form "Domänen Name \\ Benutzername" oder das UPN-Format ( Username@DomainName ) aufweisen.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-278">Depending on the service type, the account name may be in the form of "DomainName\\Username" or UPN format (Username@DomainName).</span></span> <span data-ttu-id="d0eb0-279">Der Dienst Prozess wird bei der Ausführung mithilfe einer dieser beiden Formulare protokolliert.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-279">The service process will be logged using one of these two forms when it runs.</span></span> <span data-ttu-id="d0eb0-280">Wenn das Konto zur integrierten Domäne gehört, ". \\ Username "kann angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-280">If the account belongs to the built-in domain, ".\\Username" can be specified.</span></span> <span data-ttu-id="d0eb0-281">Wenn **null** angegeben wird, wird der Dienst als LocalSystem-Konto angemeldet.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-281">If **NULL** is specified, the service will be logged on as the LocalSystem account.</span></span> <span data-ttu-id="d0eb0-282">Bei Kernel-oder System Treibern enthält **StartName** den Treiber Objektnamen ( \\ Dateisystem- \\ rdr oder \\ Treiber- \\ XNS), die vom Eingabe-und Ausgabesystem zum Laden des Gerätetreibers verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-282">For kernel or system-level drivers, **StartName** contains the driver object name (that is, \\FileSystem\\Rdr or \\Driver\\Xns) which the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="d0eb0-283">Wenn **null** angegeben wird, wird der Treiber mit einem Standard Objektnamen ausgeführt, der vom e/a-System basierend auf dem Dienstnamen erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-283">Additionally, if **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name.</span></span> <span data-ttu-id="d0eb0-284">Beispiel: "dwdom \\ Admin".</span><span class="sxs-lookup"><span data-stu-id="d0eb0-284">Example: "DWDOM\\Admin".</span></span>

</dd> <dt>

<span data-ttu-id="d0eb0-285">**State**</span><span class="sxs-lookup"><span data-stu-id="d0eb0-285">**State**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0eb0-286">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d0eb0-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0eb0-287">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d0eb0-287">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d0eb0-288">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Service \_ Status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwcurrentstate"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("State")</span><span class="sxs-lookup"><span data-stu-id="d0eb0-288">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwCurrentState "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("State")</span></span>
</dt> </dl>

<span data-ttu-id="d0eb0-289">Aktueller Status des Basis Dienes.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-289">Current state of the base service.</span></span>

<dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span data-ttu-id="d0eb0-290">**Beendet** ("beendet")</span><span class="sxs-lookup"><span data-stu-id="d0eb0-290">**Stopped** ("Stopped")</span></span>


</dt> <dd></dd> <dt>

<span id="Start_Pending"></span><span id="start_pending"></span><span id="START_PENDING"></span>

<span data-ttu-id="d0eb0-291">**Start steht aus** ("ausstehende Start")</span><span class="sxs-lookup"><span data-stu-id="d0eb0-291">**Start Pending** ("Start Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Stop_Pending"></span><span id="stop_pending"></span><span id="STOP_PENDING"></span>

<span data-ttu-id="d0eb0-292">**Ausstehende Beendigung** ("ausstehenden Vorgang nicht mehr")</span><span class="sxs-lookup"><span data-stu-id="d0eb0-292">**Stop Pending** ("Stop Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="d0eb0-293">Wird **ausgeführt** ("wird ausgeführt")</span><span class="sxs-lookup"><span data-stu-id="d0eb0-293">**Running** ("Running")</span></span>


</dt> <dd></dd> <dt>

<span id="Continue_Pending"></span><span id="continue_pending"></span><span id="CONTINUE_PENDING"></span>

<span data-ttu-id="d0eb0-294">**Ausstehende Fortsetzung** ("ausstehende Fortsetzung")</span><span class="sxs-lookup"><span data-stu-id="d0eb0-294">**Continue Pending** ("Continue Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Pause_Pending"></span><span id="pause_pending"></span><span id="PAUSE_PENDING"></span>

<span data-ttu-id="d0eb0-295">Anhalten steht **aus** ("ausstehende Pause")</span><span class="sxs-lookup"><span data-stu-id="d0eb0-295">**Pause Pending** ("Pause Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="d0eb0-296">**Angeh** alten ("angehalten")</span><span class="sxs-lookup"><span data-stu-id="d0eb0-296">**Paused** ("Paused")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d0eb0-297">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="d0eb0-297">**Unknown** ("Unknown")</span></span>


<span data-ttu-id="d0eb0-298"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="d0eb0-298"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="d0eb0-299">**Windows Server 2008 und Windows Vista:** Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-299">**Windows Server 2008 and Windows Vista:** This property is read-only.</span></span>

</dd> <dt>

<span data-ttu-id="d0eb0-300">**Status**</span><span class="sxs-lookup"><span data-stu-id="d0eb0-300">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0eb0-301">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d0eb0-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0eb0-302">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d0eb0-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0eb0-303">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="d0eb0-303">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="d0eb0-304">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-304">Current status of the object.</span></span> <span data-ttu-id="d0eb0-305">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-305">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="d0eb0-306">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="d0eb0-306">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="d0eb0-307">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="d0eb0-307">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="d0eb0-308">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-308">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="d0eb0-309">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-309">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="d0eb0-310">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-310">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="d0eb0-311">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="d0eb0-311">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="d0eb0-312">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="d0eb0-312">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="d0eb0-313">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="d0eb0-313">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d0eb0-314">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="d0eb0-314">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d0eb0-315">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="d0eb0-315">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="d0eb0-316">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="d0eb0-316">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="d0eb0-317">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="d0eb0-317">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="d0eb0-318">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="d0eb0-318">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="d0eb0-319">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="d0eb0-319">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="d0eb0-320">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="d0eb0-320">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="d0eb0-321">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="d0eb0-321">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="d0eb0-322">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="d0eb0-322">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="d0eb0-323">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="d0eb0-323">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d0eb0-324">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="d0eb0-324">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0eb0-325">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d0eb0-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0eb0-326">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d0eb0-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0eb0-327">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Schlüssel**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Klassenname")</span><span class="sxs-lookup"><span data-stu-id="d0eb0-327">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="d0eb0-328">Der Typname des Systems, das den Dienst hostet.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-328">Type name of the system that hosts this service.</span></span>

<span data-ttu-id="d0eb0-329">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](cim-service.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-329">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0eb0-330">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="d0eb0-330">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0eb0-331">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d0eb0-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0eb0-332">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d0eb0-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0eb0-333">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" System Name ")</span><span class="sxs-lookup"><span data-stu-id="d0eb0-333">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Name")</span></span>
</dt> </dl>

<span data-ttu-id="d0eb0-334">Der Name des Systems, das den Dienst hostet.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-334">Name of the system that hosts this service.</span></span>

<span data-ttu-id="d0eb0-335">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](cim-service.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-335">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0eb0-336">**TagID**</span><span class="sxs-lookup"><span data-stu-id="d0eb0-336">**TagId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0eb0-337">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d0eb0-337">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d0eb0-338">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d0eb0-338">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0eb0-339">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**Query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwtagid"), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tag ID")</span><span class="sxs-lookup"><span data-stu-id="d0eb0-339">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|dwTagId"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tag Id")</span></span>
</dt> </dl>

<span data-ttu-id="d0eb0-340">Eindeutiger Tagwert für diesen Dienst in der Gruppe.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-340">Unique tag value for this service in the group.</span></span> <span data-ttu-id="d0eb0-341">Der Wert 0 (null) gibt an, dass dem Dienst kein Tag zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-341">A value of 0 (zero) indicates that the service has not been assigned a tag.</span></span> <span data-ttu-id="d0eb0-342">Ein-Tag kann verwendet werden, um das Service Star TUP in einer Lade Auftrags Gruppe zu sortieren, indem Sie in der Registrierung unter HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Control \\ grouporderlist einen taganordnungs Vektor angeben.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-342">A tag can be used for ordering service star tup within a load order group by specifying a tag order vector in the registry located at: HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\GroupOrderList.</span></span> <span data-ttu-id="d0eb0-343">Tags werden nur für die Start-und Systemstart Modi des Kernel Treibers und des Datei System-Treibers ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-343">Tags are only evaluated for Kernel Driver and File System Driver start-type services that have Boot or System start modes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d0eb0-344">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d0eb0-344">Remarks</span></span>

<span data-ttu-id="d0eb0-345">Die **Win32 \_ baseservice** -Klasse wird vom [**CIM- \_ Dienst**](cim-service.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="d0eb0-345">The **Win32\_BaseService** class is derived from [**CIM\_Service**](cim-service.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d0eb0-346">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d0eb0-346">Requirements</span></span>



| <span data-ttu-id="d0eb0-347">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d0eb0-347">Requirement</span></span> | <span data-ttu-id="d0eb0-348">Wert</span><span class="sxs-lookup"><span data-stu-id="d0eb0-348">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0eb0-349">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d0eb0-349">Minimum supported client</span></span><br/> | <span data-ttu-id="d0eb0-350">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d0eb0-350">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d0eb0-351">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d0eb0-351">Minimum supported server</span></span><br/> | <span data-ttu-id="d0eb0-352">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d0eb0-352">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d0eb0-353">Namespace</span><span class="sxs-lookup"><span data-stu-id="d0eb0-353">Namespace</span></span><br/>                | <span data-ttu-id="d0eb0-354">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d0eb0-354">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d0eb0-355">MOF</span><span class="sxs-lookup"><span data-stu-id="d0eb0-355">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d0eb0-356"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="d0eb0-356"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d0eb0-357">DLL</span><span class="sxs-lookup"><span data-stu-id="d0eb0-357">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0eb0-358"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0eb0-358"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0eb0-359">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d0eb0-359">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0eb0-360">**CIM- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="d0eb0-360">**CIM\_Service**</span></span>](cim-service.md)
</dt> <dt>

<span data-ttu-id="d0eb0-361">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d0eb0-361">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

