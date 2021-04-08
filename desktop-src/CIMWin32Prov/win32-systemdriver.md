---
description: Stellt den System Treiber für einen Basis Dienst dar.
ms.assetid: 67dc6e14-c8c1-4168-8f99-b04c6ecd4ad2
ms.tgt_platform: multiple
title: Win32_SystemDriver-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver
- Win32_SystemDriver.AcceptPause
- Win32_SystemDriver.AcceptStop
- Win32_SystemDriver.Caption
- Win32_SystemDriver.CreationClassName
- Win32_SystemDriver.Description
- Win32_SystemDriver.DesktopInteract
- Win32_SystemDriver.DisplayName
- Win32_SystemDriver.ErrorControl
- Win32_SystemDriver.ExitCode
- Win32_SystemDriver.InstallDate
- Win32_SystemDriver.Name
- Win32_SystemDriver.PathName
- Win32_SystemDriver.ServiceSpecificExitCode
- Win32_SystemDriver.ServiceType
- Win32_SystemDriver.Started
- Win32_SystemDriver.StartMode
- Win32_SystemDriver.StartName
- Win32_SystemDriver.State
- Win32_SystemDriver.Status
- Win32_SystemDriver.SystemCreationClassName
- Win32_SystemDriver.SystemName
- Win32_SystemDriver.TagId
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 15be9b176680e8abb259d3d011da9d6cec0c2fa8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748401"
---
# <a name="win32_systemdriver-class"></a><span data-ttu-id="f188e-103">Win32 \_ systemdriver-Klasse</span><span class="sxs-lookup"><span data-stu-id="f188e-103">Win32\_SystemDriver class</span></span>

<span data-ttu-id="f188e-104">Die  [WMI-Klasse](../wmisdk/retrieving-a-class.md) des Win32-System **\_ Treibers** stellt den System Treiber für einen Basis Dienst dar.</span><span class="sxs-lookup"><span data-stu-id="f188e-104">The **Win32\_SystemDriver** [WMI class](../wmisdk/retrieving-a-class.md) represents the system driver for a base service.</span></span>

<span data-ttu-id="f188e-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f188e-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="f188e-106">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="f188e-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f188e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f188e-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4C5-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemDriver : Win32_BaseService
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

## <a name="members"></a><span data-ttu-id="f188e-108">Member</span><span class="sxs-lookup"><span data-stu-id="f188e-108">Members</span></span>

<span data-ttu-id="f188e-109">Die **Win32 \_ System Driver** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f188e-109">The **Win32\_SystemDriver** class has these types of members:</span></span>

-   [<span data-ttu-id="f188e-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="f188e-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="f188e-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f188e-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f188e-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="f188e-112">Methods</span></span>

<span data-ttu-id="f188e-113">Die **Win32 \_ System Driver** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="f188e-113">The **Win32\_SystemDriver** class has these methods.</span></span>



| <span data-ttu-id="f188e-114">Methode</span><span class="sxs-lookup"><span data-stu-id="f188e-114">Method</span></span>                                                                              | <span data-ttu-id="f188e-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f188e-115">Description</span></span>                                                                                     |
|:------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f188e-116">**Klima**</span><span class="sxs-lookup"><span data-stu-id="f188e-116">**Change**</span></span>](change-method-in-class-win32-systemdriver.md)                         | <span data-ttu-id="f188e-117">Klassenmethode, die einen Dienst ändert.</span><span class="sxs-lookup"><span data-stu-id="f188e-117">Class method that modifies a service.</span></span><br/>                                                |
| [<span data-ttu-id="f188e-118">**ChangeStartMode**</span><span class="sxs-lookup"><span data-stu-id="f188e-118">**ChangeStartMode**</span></span>](changestartmode-method-in-class-win32-systemdriver.md)       | <span data-ttu-id="f188e-119">Klassenmethode, mit der der Start Modus eines Dienstanbieter geändert wird.</span><span class="sxs-lookup"><span data-stu-id="f188e-119">Class method that modifies the start mode of a service.</span></span><br/>                              |
| [<span data-ttu-id="f188e-120">**Stelle**</span><span class="sxs-lookup"><span data-stu-id="f188e-120">**Create**</span></span>](create-method-in-class-win32-systemdriver.md)                         | <span data-ttu-id="f188e-121">Klassenmethode, mit der ein neuer Dienst erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="f188e-121">Class method that creates a new service.</span></span><br/>                                             |
| [<span data-ttu-id="f188e-122">**Lösch**</span><span class="sxs-lookup"><span data-stu-id="f188e-122">**Delete**</span></span>](delete-method-in-class-win32-systemdriver.md)                         | <span data-ttu-id="f188e-123">Klassenmethode, mit der ein vorhandener Dienst gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="f188e-123">Class method that deletes an existing service.</span></span><br/>                                       |
| [<span data-ttu-id="f188e-124">**"InterrogateService"**</span><span class="sxs-lookup"><span data-stu-id="f188e-124">**InterrogateService**</span></span>](interrogateservice-method-in-class-win32-systemdriver.md) | <span data-ttu-id="f188e-125">Class-Methode, die anfordert, dass der Dienst seinen Status an den Dienst-Manager aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="f188e-125">Class method that requests that the service update its state to the service manager.</span></span><br/> |
| [<span data-ttu-id="f188e-126">**PauseService**</span><span class="sxs-lookup"><span data-stu-id="f188e-126">**PauseService**</span></span>](pauseservice-method-in-class-win32-systemdriver.md)             | <span data-ttu-id="f188e-127">Klassenmethode, die versucht, den Dienst in den angehaltenen Zustand zu versetzen.</span><span class="sxs-lookup"><span data-stu-id="f188e-127">Class method that attempts to place the service in the paused state.</span></span><br/>                 |
| [<span data-ttu-id="f188e-128">**ResumeService**</span><span class="sxs-lookup"><span data-stu-id="f188e-128">**ResumeService**</span></span>](resumeservice-method-in-class-win32-systemdriver.md)           | <span data-ttu-id="f188e-129">Klassenmethode, die versucht, den Dienst in den Status "wieder aufgenommen" zu versetzen.</span><span class="sxs-lookup"><span data-stu-id="f188e-129">Class method that attempts to place the service in the resumed state.</span></span><br/>                |
| [<span data-ttu-id="f188e-130">**Start Service**</span><span class="sxs-lookup"><span data-stu-id="f188e-130">**StartService**</span></span>](startservice-method-in-class-win32-systemdriver.md)             | <span data-ttu-id="f188e-131">Klassenmethode, die versucht, den Dienst in seinen Startzustand zu versetzen.</span><span class="sxs-lookup"><span data-stu-id="f188e-131">Class method that attempts to place the service into its startup state.</span></span><br/>              |
| [<span data-ttu-id="f188e-132">**Stop Service**</span><span class="sxs-lookup"><span data-stu-id="f188e-132">**StopService**</span></span>](stopservice-method-in-class-win32-systemdriver.md)               | <span data-ttu-id="f188e-133">Klassenmethode, die den Dienst in den Zustand "beendet" versetzt.</span><span class="sxs-lookup"><span data-stu-id="f188e-133">Class method that places the service in the stopped state.</span></span><br/>                           |
| [<span data-ttu-id="f188e-134">**UserControlService**</span><span class="sxs-lookup"><span data-stu-id="f188e-134">**UserControlService**</span></span>](usercontrolservice-method-in-class-win32-systemdriver.md) | <span data-ttu-id="f188e-135">Klassenmethode, die versucht, einen benutzerdefinierten Steuerelement Code an einen Dienst zu senden.</span><span class="sxs-lookup"><span data-stu-id="f188e-135">Class method that attempts to send a user-defined control code to a service.</span></span><br/>         |



 

### <a name="properties"></a><span data-ttu-id="f188e-136">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f188e-136">Properties</span></span>

<span data-ttu-id="f188e-137">Die **Win32 \_ System Driver** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f188e-137">The **Win32\_SystemDriver** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f188e-138">**AcceptPause**</span><span class="sxs-lookup"><span data-stu-id="f188e-138">**AcceptPause**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f188e-139">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f188e-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f188e-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f188e-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f188e-141">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API Service \| Structures \| [**Service \_ Status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwcontrolsaccepted \| Service \_ Accept \_ Pause \_ Continue"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Service Accept Pause")</span><span class="sxs-lookup"><span data-stu-id="f188e-141">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwControlsAccepted\|SERVICE\_ACCEPT\_PAUSE\_CONTINUE"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Service Accepts Pause")</span></span>
</dt> </dl>

<span data-ttu-id="f188e-142">Der Dienst kann angehalten werden.</span><span class="sxs-lookup"><span data-stu-id="f188e-142">Service can be paused.</span></span>

<span data-ttu-id="f188e-143">Diese Eigenschaft wird von [**Win32 \_ baseservice**](win32-baseservice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f188e-143">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f188e-144">**AcceptStop**</span><span class="sxs-lookup"><span data-stu-id="f188e-144">**AcceptStop**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f188e-145">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f188e-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f188e-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f188e-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f188e-147">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API Service \| Structures \| [**Service \_ Status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwcontrolsaccepted \| Service \_ Accept End \_ "), [**Display Name**](../wmisdk/standard-qualifiers.md) ("der Dienst akzeptiert das Ende")</span><span class="sxs-lookup"><span data-stu-id="f188e-147">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwControlsAccepted\|SERVICE\_ACCEPT\_STOP"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Service Accepts Stop")</span></span>
</dt> </dl>

<span data-ttu-id="f188e-148">Der Dienst kann angehalten werden.</span><span class="sxs-lookup"><span data-stu-id="f188e-148">Service can be stopped.</span></span>

<span data-ttu-id="f188e-149">Diese Eigenschaft wird von [**Win32 \_ baseservice**](win32-baseservice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f188e-149">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f188e-150">**Caption**</span><span class="sxs-lookup"><span data-stu-id="f188e-150">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f188e-151">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f188e-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f188e-152">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f188e-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f188e-153">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="f188e-153">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="f188e-154">Kurze Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="f188e-154">Short description of the object.</span></span>

<span data-ttu-id="f188e-155">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f188e-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f188e-156">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="f188e-156">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f188e-157">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f188e-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f188e-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f188e-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f188e-159">Qualifizierer: [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Class Name")</span><span class="sxs-lookup"><span data-stu-id="f188e-159">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="f188e-160">Der Name der ersten konkreten Klasse, die in der Vererbungs Kette angezeigt werden soll, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f188e-160">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="f188e-161">Wenn diese Eigenschaft mit den anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="f188e-161">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="f188e-162">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](cim-service.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f188e-162">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="f188e-163">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f188e-163">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f188e-164">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f188e-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f188e-165">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f188e-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f188e-166">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="f188e-166">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="f188e-167">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="f188e-167">Description of the object.</span></span>

<span data-ttu-id="f188e-168">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f188e-168">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f188e-169">**DesktopInteract**</span><span class="sxs-lookup"><span data-stu-id="f188e-169">**DesktopInteract**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f188e-170">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f188e-170">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f188e-171">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f188e-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f188e-172">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**Query \_ Service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| dwservicetype \| Service \_ Interactive \_ Process"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("interagiert with Desktop")</span><span class="sxs-lookup"><span data-stu-id="f188e-172">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|dwServiceType\|SERVICE\_INTERACTIVE\_PROCESS"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Interacts With Desktop")</span></span>
</dt> </dl>

<span data-ttu-id="f188e-173">Dieser Dienst kann Windows auf dem Desktop erstellen oder mit ihm kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="f188e-173">This service can create or communicate with windows on the desktop.</span></span>

<span data-ttu-id="f188e-174">Diese Eigenschaft wird von [**Win32 \_ baseservice**](win32-baseservice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f188e-174">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f188e-175">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="f188e-175">**DisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f188e-176">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f188e-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f188e-177">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f188e-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f188e-178">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**Query \_ Service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| lpdisplayname"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Anzeige Name")</span><span class="sxs-lookup"><span data-stu-id="f188e-178">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|lpDisplayName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Display Name")</span></span>
</dt> </dl>

<span data-ttu-id="f188e-179">Der Anzeige Name des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="f188e-179">Display name of the service.</span></span> <span data-ttu-id="f188e-180">Die maximale Länge der Zeichenfolge beträgt 256 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="f188e-180">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="f188e-181">Der Name wird im Dienststeuerungs-Manager nach Groß-/Kleinschreibung beibehalten.</span><span class="sxs-lookup"><span data-stu-id="f188e-181">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="f188e-182">Bei **Display Name** -vergleichen wird immer die Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="f188e-182">**DisplayName** comparisons are always case-insensitive.</span></span>

<span data-ttu-id="f188e-183">Einschränkungen: akzeptiert denselben Wert wie die **Name** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="f188e-183">Constraints: Accepts the same value as the **Name** property.</span></span>

<span data-ttu-id="f188e-184">Beispiel: "ATDISK"</span><span class="sxs-lookup"><span data-stu-id="f188e-184">Example: "Atdisk"</span></span>

<span data-ttu-id="f188e-185">Diese Eigenschaft wird von [**Win32 \_ baseservice**](win32-baseservice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f188e-185">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f188e-186">**ErrorControl**</span><span class="sxs-lookup"><span data-stu-id="f188e-186">**ErrorControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f188e-187">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f188e-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f188e-188">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f188e-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f188e-189">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**Query \_ Service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| dwerrorcontrol"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Schweregrad des Start Fehlers")</span><span class="sxs-lookup"><span data-stu-id="f188e-189">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|dwErrorControl"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Severity Of Startup Failure")</span></span>
</dt> </dl>

<span data-ttu-id="f188e-190">Der Schweregrad des Fehlers, wenn dieser Dienst während des Starts nicht gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="f188e-190">Severity of the error if this service fails to start during startup.</span></span> <span data-ttu-id="f188e-191">Dieser Wert gibt die vom Start Programm ausgeführte Aktion an, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="f188e-191">This value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="f188e-192">Alle Fehler werden vom Computersystem protokolliert.</span><span class="sxs-lookup"><span data-stu-id="f188e-192">All errors are logged by the computer system.</span></span>

<span data-ttu-id="f188e-193">Diese Eigenschaft wird von [**Win32 \_ baseservice**](win32-baseservice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f188e-193">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span data-ttu-id="f188e-194"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignorieren** ("ignorieren")</span><span class="sxs-lookup"><span data-stu-id="f188e-194"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignore** ("Ignore")</span></span>


</dt> <dd>

<span data-ttu-id="f188e-195">Der Benutzer wird nicht benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="f188e-195">User is not notified.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="f188e-196"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** ("Normal")</span><span class="sxs-lookup"><span data-stu-id="f188e-196"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** ("Normal")</span></span>


</dt> <dd>

<span data-ttu-id="f188e-197">Der Benutzer wird benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="f188e-197">User is notified.</span></span>

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span data-ttu-id="f188e-198"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Schwerwiegend** ("schwerwiegend")</span><span class="sxs-lookup"><span data-stu-id="f188e-198"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Severe** ("Severe")</span></span>


</dt> <dd>

<span data-ttu-id="f188e-199">Das System wird mit der letzten bekannten, fehlerfreien Konfiguration neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="f188e-199">System is restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="f188e-200"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Kritisch** ("kritisch")</span><span class="sxs-lookup"><span data-stu-id="f188e-200"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** ("Critical")</span></span>


</dt> <dd>

<span data-ttu-id="f188e-201">Das System versucht, mit einer fehlerfreien Konfiguration zu neu starten.</span><span class="sxs-lookup"><span data-stu-id="f188e-201">System attempts to restart with a good configuration.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f188e-202"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="f188e-202"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** ("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="f188e-203">Die Ursache des Fehlers ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="f188e-203">Cause of the failure is unknown.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f188e-204">**Exitcode**</span><span class="sxs-lookup"><span data-stu-id="f188e-204">**ExitCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f188e-205">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f188e-205">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f188e-206">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f188e-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f188e-207">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**Service \_ Status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwWin32ExitCode"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Exitcode")</span><span class="sxs-lookup"><span data-stu-id="f188e-207">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwWin32ExitCode"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Exit Code")</span></span>
</dt> </dl>

<span data-ttu-id="f188e-208">Windows-Fehlercode, der Probleme definiert, die beim Starten oder Beenden des Dienstes aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="f188e-208">Windows error code defining any problems encountered in starting or stopping the service.</span></span> <span data-ttu-id="f188e-209">Diese Eigenschaft ist auf **Fehler \_ Dienst \_ spezifischer \_ Fehler** (1066) festgelegt, wenn der Fehler für den Dienst eindeutig ist, der durch diese Klasse dargestellt wird. Informationen über den Fehler sind in der **ServiceSpecificExitCode** -Eigenschaft verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f188e-209">This property is set to **ERROR\_SERVICE\_SPECIFIC\_ERROR** (1066) when the error is unique to the service represented by this class, and information about the error is available in the **ServiceSpecificExitCode** property.</span></span> <span data-ttu-id="f188e-210">Der Dienst legt diesen Wert bei der Ausführung und erneut bei normaler Beendigung auf **keinen \_ Fehler** fest.</span><span class="sxs-lookup"><span data-stu-id="f188e-210">The service sets this value to **NO\_ERROR** when running, and again upon normal termination.</span></span>

<span data-ttu-id="f188e-211">Diese Eigenschaft wird von [**Win32 \_ baseservice**](win32-baseservice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f188e-211">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f188e-212">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f188e-212">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f188e-213">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="f188e-213">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f188e-214">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f188e-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f188e-215">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="f188e-215">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="f188e-216">Das Objekt wurde installiert.</span><span class="sxs-lookup"><span data-stu-id="f188e-216">Object was installed.</span></span> <span data-ttu-id="f188e-217">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="f188e-217">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="f188e-218">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f188e-218">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f188e-219">**Name**</span><span class="sxs-lookup"><span data-stu-id="f188e-219">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f188e-220">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f188e-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f188e-221">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f188e-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f188e-222">Qualifizierer: [ **Schlüssel**](../wmisdk/key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="f188e-222">Qualifiers: [**Key**](../wmisdk/key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="f188e-223">Eindeutiger Bezeichner für den Dienst, der eine Angabe der verwalteten Funktionalität bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="f188e-223">Unique identifier for the service which provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="f188e-224">Diese Funktionalität wird in der Objekt **Beschreibungs** Eigenschaft ausführlicher beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f188e-224">This functionality is described in more detail in the object **Description** property.</span></span>

<span data-ttu-id="f188e-225">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](cim-service.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f188e-225">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="f188e-226">**PathName**</span><span class="sxs-lookup"><span data-stu-id="f188e-226">**PathName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f188e-227">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f188e-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f188e-228">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f188e-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f188e-229">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**Query \_ Service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| lpbinarypathname"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Dateipfadname")</span><span class="sxs-lookup"><span data-stu-id="f188e-229">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|lpBinaryPathName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File Path Name")</span></span>
</dt> </dl>

<span data-ttu-id="f188e-230">Der voll qualifizierte Pfad der Dienst Binärdatei, die den Dienst implementiert.</span><span class="sxs-lookup"><span data-stu-id="f188e-230">Fully qualified path to the service binary file that implements the service.</span></span>

<span data-ttu-id="f188e-231">Beispiel: " \\ systemroot \\ system32 \\ Drivers \\afd.sys"</span><span class="sxs-lookup"><span data-stu-id="f188e-231">Example: "\\SystemRoot\\System32\\drivers\\afd.sys"</span></span>

<span data-ttu-id="f188e-232">Diese Eigenschaft wird von [**Win32 \_ baseservice**](win32-baseservice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f188e-232">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f188e-233">**ServiceSpecificExitCode**</span><span class="sxs-lookup"><span data-stu-id="f188e-233">**ServiceSpecificExitCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f188e-234">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f188e-234">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f188e-235">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f188e-235">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f188e-236">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**Service \_ Status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwservicespecificexitcode"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Server spezifischer Exitcode")</span><span class="sxs-lookup"><span data-stu-id="f188e-236">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwServiceSpecificExitCode"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Server Specific Exit Code")</span></span>
</dt> </dl>

<span data-ttu-id="f188e-237">Dienst spezifischer Fehlercode für Fehler, die auftreten, während der Dienst gestartet oder beendet wird.</span><span class="sxs-lookup"><span data-stu-id="f188e-237">Service-specific error code for errors that occur while the service is either starting or stopping.</span></span> <span data-ttu-id="f188e-238">Die Exitcodes werden von dem Dienst definiert, der durch diese Klasse dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="f188e-238">The exit codes are defined by the service represented by this class.</span></span> <span data-ttu-id="f188e-239">Dieser Wert wird nur festgelegt, wenn der **Exitcode** -Eigenschafts Wert **Fehler \_ Dienst \_ spezifisch \_** ist (1066).</span><span class="sxs-lookup"><span data-stu-id="f188e-239">This value is only set when the **ExitCode** property value is **ERROR\_SERVICE\_SPECIFIC\_ERROR** (1066).</span></span>

<span data-ttu-id="f188e-240">Diese Eigenschaft wird von [**Win32 \_ baseservice**](win32-baseservice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f188e-240">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f188e-241">**ServiceType**</span><span class="sxs-lookup"><span data-stu-id="f188e-241">**ServiceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f188e-242">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f188e-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f188e-243">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f188e-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f188e-244">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**Query \_ Service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| dwservicetype"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Service Type")</span><span class="sxs-lookup"><span data-stu-id="f188e-244">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|dwServiceType"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Service Type")</span></span>
</dt> </dl>

<span data-ttu-id="f188e-245">Der für aufrufende Prozesse bereitgestellte Diensttyp.</span><span class="sxs-lookup"><span data-stu-id="f188e-245">Type of service provided to calling processes.</span></span>

<span data-ttu-id="f188e-246">Diese Eigenschaft wird von [**Win32 \_ baseservice**](win32-baseservice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f188e-246">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

<span data-ttu-id="f188e-247">Die Werte sind:</span><span class="sxs-lookup"><span data-stu-id="f188e-247">The values are:</span></span>

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

<span data-ttu-id="f188e-248">**Kernel Treiber** ("Kernel Treiber")</span><span class="sxs-lookup"><span data-stu-id="f188e-248">**Kernel Driver** ("Kernel Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

<span data-ttu-id="f188e-249">**Dateisystem Treiber** ("Dateisystem Treiber")</span><span class="sxs-lookup"><span data-stu-id="f188e-249">**File System Driver** ("File System Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

<span data-ttu-id="f188e-250">**Adapter** ("Adapter")</span><span class="sxs-lookup"><span data-stu-id="f188e-250">**Adapter** ("Adapter")</span></span>


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

<span data-ttu-id="f188e-251">**Erkennungs Treiber** ("Erkennungs Treiber")</span><span class="sxs-lookup"><span data-stu-id="f188e-251">**Recognizer Driver** ("Recognizer Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

<span data-ttu-id="f188e-252">**Eigener Prozess** ("eigener Prozess")</span><span class="sxs-lookup"><span data-stu-id="f188e-252">**Own Process** ("Own Process")</span></span>


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

<span data-ttu-id="f188e-253">**Freigabeprozess** ("Freigabeprozess")</span><span class="sxs-lookup"><span data-stu-id="f188e-253">**Share Process** ("Share Process")</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_Process"></span><span id="interactive_process"></span><span id="INTERACTIVE_PROCESS"></span>

<span data-ttu-id="f188e-254">**Interaktiver Prozess** ("interaktiver Prozess")</span><span class="sxs-lookup"><span data-stu-id="f188e-254">**Interactive Process** ("Interactive Process")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f188e-255">**Gestartet**</span><span class="sxs-lookup"><span data-stu-id="f188e-255">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f188e-256">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f188e-256">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f188e-257">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f188e-257">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f188e-258">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Started")</span><span class="sxs-lookup"><span data-stu-id="f188e-258">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Started")</span></span>
</dt> </dl>

<span data-ttu-id="f188e-259">Der Dienst wurde gestartet.</span><span class="sxs-lookup"><span data-stu-id="f188e-259">Service has been started.</span></span>

<span data-ttu-id="f188e-260">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](cim-service.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f188e-260">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="f188e-261">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="f188e-261">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f188e-262">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f188e-262">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f188e-263">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f188e-263">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f188e-264">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Start Modus")</span><span class="sxs-lookup"><span data-stu-id="f188e-264">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Start Mode")</span></span>
</dt> </dl>

<span data-ttu-id="f188e-265">Der Start Modus des System Treibers.</span><span class="sxs-lookup"><span data-stu-id="f188e-265">Start mode of the system driver.</span></span>

<span data-ttu-id="f188e-266">Diese Eigenschaft wird von [**Win32 \_ baseservice**](win32-baseservice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f188e-266">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span data-ttu-id="f188e-267"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Start** ("Start")</span><span class="sxs-lookup"><span data-stu-id="f188e-267"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Boot** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="f188e-268">Der Gerätetreiber wurde vom Betriebssystem Lader gestartet (nur für Treiber Dienste gültig).</span><span class="sxs-lookup"><span data-stu-id="f188e-268">Device driver started by the operating system loader (valid only for driver services).</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="f188e-269"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ("System")</span><span class="sxs-lookup"><span data-stu-id="f188e-269"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="f188e-270">Der Gerätetreiber wurde durch den Initialisierungs Prozess des Betriebssystems gestartet.</span><span class="sxs-lookup"><span data-stu-id="f188e-270">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="f188e-271">Dieses Wert ist nur für Treiberdienste gültig.</span><span class="sxs-lookup"><span data-stu-id="f188e-271">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>

<span data-ttu-id="f188e-272"><span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Auto** ("Auto")</span><span class="sxs-lookup"><span data-stu-id="f188e-272"><span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Auto** ("Auto")</span></span>


</dt> <dd>

<span data-ttu-id="f188e-273">Dienst, der vom Dienststeuerungs-Manager beim Systemstart automatisch gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="f188e-273">Service to be started automatically by the service control manager during system start up.</span></span>

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="f188e-274"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manuell** ("manuell")</span><span class="sxs-lookup"><span data-stu-id="f188e-274"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="f188e-275">Der Dienst, der vom Dienststeuerungs-Manager gestartet werden soll, wenn ein Prozess die [**StartService**](startservice-method-in-class-win32-systemdriver.md) -Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="f188e-275">Service to be started by the service control manager when a process calls the [**StartService**](startservice-method-in-class-win32-systemdriver.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="f188e-276"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** ("deaktiviert")</span><span class="sxs-lookup"><span data-stu-id="f188e-276"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="f188e-277">Dienst, der nicht mehr gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="f188e-277">Service that can no longer be started.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f188e-278">**StartName**</span><span class="sxs-lookup"><span data-stu-id="f188e-278">**StartName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f188e-279">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f188e-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f188e-280">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f188e-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f188e-281">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**Query \_ Service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| lpservicestartname"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Starting Account Name")</span><span class="sxs-lookup"><span data-stu-id="f188e-281">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|lpServiceStartName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Starting Account Name")</span></span>
</dt> </dl>

<span data-ttu-id="f188e-282">Der Kontoname, unter dem der Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f188e-282">Account name under which the service runs.</span></span> <span data-ttu-id="f188e-283">Abhängig vom Diensttyp kann der Kontoname die Form "Domänen Name \\ Benutzername" aufweisen.</span><span class="sxs-lookup"><span data-stu-id="f188e-283">Depending on the service type, the account name may be in the form of DomainName\\Username.</span></span> <span data-ttu-id="f188e-284">Der Dienst Prozess wird bei der Ausführung mithilfe einer dieser beiden Formulare protokolliert.</span><span class="sxs-lookup"><span data-stu-id="f188e-284">The service process will be logged using one of these two forms when it runs.</span></span> <span data-ttu-id="f188e-285">, Wenn das Konto zur integrierten Domäne gehört. \\ Der Benutzername kann angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f188e-285">If the account belongs to the built-in domain, .\\Username can be specified.</span></span> <span data-ttu-id="f188e-286">Wenn **null** angegeben wird, wird der Dienst als LocalSystem-Konto angemeldet.</span><span class="sxs-lookup"><span data-stu-id="f188e-286">If **NULL** is specified, the service will be logged on as the LocalSystem account.</span></span> <span data-ttu-id="f188e-287">Bei Kernel-oder System Treibern enthält **StartName** den Treiber Objektnamen ( \\ Dateisystem- \\ rdr oder \\ Treiber- \\ XNS), die vom Eingabe-und Ausgabesystem zum Laden des Gerätetreibers verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f188e-287">For kernel or system-level drivers, **StartName** contains the driver object name (that is, \\FileSystem\\Rdr or \\Driver\\Xns) which the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="f188e-288">Wenn **null** angegeben wird, wird der Treiber mit einem Standard Objektnamen ausgeführt, der vom e/a-System basierend auf dem Dienstnamen erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="f188e-288">Additionally, if **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name.</span></span>

<span data-ttu-id="f188e-289">Beispiel: "dwdom \\ Admin"</span><span class="sxs-lookup"><span data-stu-id="f188e-289">Example: "DWDOM\\Admin"</span></span>

<span data-ttu-id="f188e-290">Diese Eigenschaft wird von [**Win32 \_ baseservice**](win32-baseservice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f188e-290">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f188e-291">**State**</span><span class="sxs-lookup"><span data-stu-id="f188e-291">**State**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f188e-292">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f188e-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f188e-293">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f188e-293">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f188e-294">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**Service \_ Status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwcurrentstate"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("State")</span><span class="sxs-lookup"><span data-stu-id="f188e-294">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwCurrentState "), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("State")</span></span>
</dt> </dl>

<span data-ttu-id="f188e-295">Aktueller Status des Basis Dienes.</span><span class="sxs-lookup"><span data-stu-id="f188e-295">Current state of the base service.</span></span>

<span data-ttu-id="f188e-296">Diese Eigenschaft wird von [**Win32 \_ baseservice**](win32-baseservice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f188e-296">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

<span data-ttu-id="f188e-297">Die Werte sind:</span><span class="sxs-lookup"><span data-stu-id="f188e-297">The values are:</span></span>

<dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span data-ttu-id="f188e-298">**Beendet** ("beendet")</span><span class="sxs-lookup"><span data-stu-id="f188e-298">**Stopped** ("Stopped")</span></span>


</dt> <dd></dd> <dt>

<span id="Start_Pending"></span><span id="start_pending"></span><span id="START_PENDING"></span>

<span data-ttu-id="f188e-299">**Start steht aus** ("ausstehende Start")</span><span class="sxs-lookup"><span data-stu-id="f188e-299">**Start Pending** ("Start Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Stop_Pending"></span><span id="stop_pending"></span><span id="STOP_PENDING"></span>

<span data-ttu-id="f188e-300">**Ausstehende Beendigung** ("ausstehenden Vorgang nicht mehr")</span><span class="sxs-lookup"><span data-stu-id="f188e-300">**Stop Pending** ("Stop Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="f188e-301">Wird **ausgeführt** ("wird ausgeführt")</span><span class="sxs-lookup"><span data-stu-id="f188e-301">**Running** ("Running")</span></span>


</dt> <dd></dd> <dt>

<span id="Continue_Pending"></span><span id="continue_pending"></span><span id="CONTINUE_PENDING"></span>

<span data-ttu-id="f188e-302">**Ausstehende Fortsetzung** ("ausstehende Fortsetzung")</span><span class="sxs-lookup"><span data-stu-id="f188e-302">**Continue Pending** ("Continue Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Pause_Pending"></span><span id="pause_pending"></span><span id="PAUSE_PENDING"></span>

<span data-ttu-id="f188e-303">Anhalten steht **aus** ("ausstehende Pause")</span><span class="sxs-lookup"><span data-stu-id="f188e-303">**Pause Pending** ("Pause Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="f188e-304">**Angeh** alten ("angehalten")</span><span class="sxs-lookup"><span data-stu-id="f188e-304">**Paused** ("Paused")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f188e-305">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="f188e-305">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f188e-306">**Status**</span><span class="sxs-lookup"><span data-stu-id="f188e-306">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f188e-307">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f188e-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f188e-308">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f188e-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f188e-309">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="f188e-309">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="f188e-310">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="f188e-310">Current status of the object.</span></span> <span data-ttu-id="f188e-311">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="f188e-311">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="f188e-312">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="f188e-312">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="f188e-313">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="f188e-313">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="f188e-314">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="f188e-314">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="f188e-315">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="f188e-315">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="f188e-316">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f188e-316">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="f188e-317">Die Werte sind:</span><span class="sxs-lookup"><span data-stu-id="f188e-317">The values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="f188e-318">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="f188e-318">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="f188e-319">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="f188e-319">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f188e-320">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="f188e-320">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f188e-321">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="f188e-321">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="f188e-322">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="f188e-322">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="f188e-323">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="f188e-323">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="f188e-324">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="f188e-324">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="f188e-325">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="f188e-325">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="f188e-326">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="f188e-326">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="f188e-327">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="f188e-327">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="f188e-328">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="f188e-328">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="f188e-329">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="f188e-329">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f188e-330">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="f188e-330">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f188e-331">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f188e-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f188e-332">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f188e-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f188e-333">Qualifizierer [**: weiter**](../wmisdk/standard-qualifiers.md) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Schlüssel**](../wmisdk/standard-wmi-qualifiers.md), [**Display Name**](../wmisdk/standard-qualifiers.md) ("System Klassenname")</span><span class="sxs-lookup"><span data-stu-id="f188e-333">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="f188e-334">Der Typname des Systems, das den Dienst hostet.</span><span class="sxs-lookup"><span data-stu-id="f188e-334">Type name of the system that hosts this service.</span></span>

<span data-ttu-id="f188e-335">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](cim-service.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f188e-335">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="f188e-336">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="f188e-336">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f188e-337">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f188e-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f188e-338">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f188e-338">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f188e-339">Qualifizierer [**: weiter**](../wmisdk/standard-qualifiers.md) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md), [**Display Name**](../wmisdk/standard-qualifiers.md) (" System Name ")</span><span class="sxs-lookup"><span data-stu-id="f188e-339">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("System Name")</span></span>
</dt> </dl>

<span data-ttu-id="f188e-340">Der Name des Systems, das den Dienst hostet.</span><span class="sxs-lookup"><span data-stu-id="f188e-340">Name of the system that hosts this service.</span></span>

<span data-ttu-id="f188e-341">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](cim-service.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f188e-341">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="f188e-342">**TagID**</span><span class="sxs-lookup"><span data-stu-id="f188e-342">**TagId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f188e-343">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f188e-343">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f188e-344">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f188e-344">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f188e-345">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**Query \_ Service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| dwtagid"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Tag ID")</span><span class="sxs-lookup"><span data-stu-id="f188e-345">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|dwTagId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Tag Id")</span></span>
</dt> </dl>

<span data-ttu-id="f188e-346">Eindeutiger Tagwert für diesen Dienst in der Gruppe.</span><span class="sxs-lookup"><span data-stu-id="f188e-346">Unique tag value for this service in the group.</span></span> <span data-ttu-id="f188e-347">Der Wert 0 (null) gibt an, dass dem Dienst kein Tag zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="f188e-347">A value of 0 (zero) indicates that the service has not been assigned a tag.</span></span> <span data-ttu-id="f188e-348">Ein Tag kann zum Sortieren des Dienst Starts innerhalb einer Gruppe von Lade Reihenfolgen verwendet werden, indem ein taganordnungs Vektor in der Registrierung unter angegeben wird:</span><span class="sxs-lookup"><span data-stu-id="f188e-348">A tag can be used for ordering service startup within a load order group by specifying a tag order vector in the registry located at:</span></span>

<span data-ttu-id="f188e-349">Diese Eigenschaft wird von [**Win32 \_ baseservice**](win32-baseservice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f188e-349">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

<span data-ttu-id="f188e-350">**HKEY \_ Lokales \_ Computer \\ System \\ CurrentControlSet \\ Steuerelement \\ grouporderlist**.</span><span class="sxs-lookup"><span data-stu-id="f188e-350">**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\GroupOrderList**.</span></span>

<span data-ttu-id="f188e-351">Tags werden nur für die Start-und Systemstart Modi des Kernel Treibers und des Datei System-Treibers ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="f188e-351">Tags are only evaluated for Kernel Driver and File System Driver start-type services that have Boot or System start modes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f188e-352">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f188e-352">Remarks</span></span>

<span data-ttu-id="f188e-353">Die **Win32 \_ System Driver** -Klasse wird von [**Win32 \_ baseservice**](win32-baseservice.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="f188e-353">The **Win32\_SystemDriver** class is derived from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

## <a name="examples"></a><span data-ttu-id="f188e-354">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f188e-354">Examples</span></span>

<span data-ttu-id="f188e-355">Im Beispiel " [List System Drivers](https://Gallery.TechNet.Microsoft.Com/5629cc13-cefc-4e51-a24f-aac6db23d141) VBScript" werden installierte System Treiber in einer HTML-Datei angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f188e-355">The [List System Drivers](https://Gallery.TechNet.Microsoft.Com/5629cc13-cefc-4e51-a24f-aac6db23d141) VBScript sample Displays installed system drivers in an HTML file.</span></span>

<span data-ttu-id="f188e-356">Das folgende PowerShell-Beispiel ruft eine Reihe von Eigenschaften aus den System Treibern auf einem Computer ab.</span><span class="sxs-lookup"><span data-stu-id="f188e-356">The following PowerShell example retrieves a number of properties from the running system drivers on a computer.</span></span>


```PowerShell
Get-WmiObject -Class Win32_SystemDriver | Where-Object -FilterScript {$_.State -eq "Running"} | Where-Object -FilterScript {$_.StartMode -eq "Manual"} | Format-Table -Property Name,DisplayName
```



## <a name="requirements"></a><span data-ttu-id="f188e-357">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f188e-357">Requirements</span></span>



| <span data-ttu-id="f188e-358">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f188e-358">Requirement</span></span> | <span data-ttu-id="f188e-359">Wert</span><span class="sxs-lookup"><span data-stu-id="f188e-359">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f188e-360">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f188e-360">Minimum supported client</span></span><br/> | <span data-ttu-id="f188e-361">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f188e-361">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f188e-362">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f188e-362">Minimum supported server</span></span><br/> | <span data-ttu-id="f188e-363">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f188e-363">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f188e-364">Namespace</span><span class="sxs-lookup"><span data-stu-id="f188e-364">Namespace</span></span><br/>                | <span data-ttu-id="f188e-365">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f188e-365">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f188e-366">MOF</span><span class="sxs-lookup"><span data-stu-id="f188e-366">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f188e-367"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f188e-367"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f188e-368">DLL</span><span class="sxs-lookup"><span data-stu-id="f188e-368">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f188e-369"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f188e-369"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f188e-370">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f188e-370">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f188e-371">**Win32- \_ baseservice**</span><span class="sxs-lookup"><span data-stu-id="f188e-371">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> <dt>

[<span data-ttu-id="f188e-372">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="f188e-372">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
