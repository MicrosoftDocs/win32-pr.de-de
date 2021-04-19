---
description: Verwaltet alle Remote-Terminal Verbindungen mit einem bestimmten Host.
ms.assetid: 7eacb8a6-cb8d-4a2a-951e-f5286cf484e7
title: Msvm_TerminalService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalService
- Msvm_TerminalService.InstanceID
- Msvm_TerminalService.Caption
- Msvm_TerminalService.Description
- Msvm_TerminalService.ElementName
- Msvm_TerminalService.InstallDate
- Msvm_TerminalService.OperationalStatus
- Msvm_TerminalService.StatusDescriptions
- Msvm_TerminalService.Status
- Msvm_TerminalService.HealthState
- Msvm_TerminalService.CommunicationStatus
- Msvm_TerminalService.DetailedStatus
- Msvm_TerminalService.OperatingStatus
- Msvm_TerminalService.PrimaryStatus
- Msvm_TerminalService.EnabledState
- Msvm_TerminalService.OtherEnabledState
- Msvm_TerminalService.RequestedState
- Msvm_TerminalService.EnabledDefault
- Msvm_TerminalService.TimeOfLastStateChange
- Msvm_TerminalService.AvailableRequestedStates
- Msvm_TerminalService.TransitioningToState
- Msvm_TerminalService.SystemCreationClassName
- Msvm_TerminalService.SystemName
- Msvm_TerminalService.Name
- Msvm_TerminalService.CreationClassName
- Msvm_TerminalService.PrimaryOwnerName
- Msvm_TerminalService.PrimaryOwnerContact
- Msvm_TerminalService.StartMode
- Msvm_TerminalService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 76b12bb49391909638d20df817a3693938c3222c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355549"
---
# <a name="msvm_terminalservice-class"></a><span data-ttu-id="30035-103">MSVM \_ Terminalservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="30035-103">Msvm\_TerminalService class</span></span>

<span data-ttu-id="30035-104">Verwaltet alle Remote-Terminal Verbindungen mit einem bestimmten Host.</span><span class="sxs-lookup"><span data-stu-id="30035-104">Manages all remote terminal connections to a particular host.</span></span> <span data-ttu-id="30035-105">Der Dienst verwendet einen konfigurierbaren Port, um alle Terminal Verbindungen zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="30035-105">The service uses a configurable port to initiate all terminal connections.</span></span>

<span data-ttu-id="30035-106">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="30035-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="30035-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="30035-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TerminalService : CIM_Service
{
  string   InstanceID;
  string   Caption = "Hyper-V Terminal Service";
  string   Description = "Microsoft Virtual Terminal Service";
  string   ElementName = "Hyper-V Terminal Service";
  datetime InstallDate;
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "The virtual terminal connection management service is fully operational" };
  string   Status = "OK";
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   Name = "termsvc";
  string   CreationClassName = "Msvm_TerminalService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started;
};
```

## <a name="members"></a><span data-ttu-id="30035-108">Member</span><span class="sxs-lookup"><span data-stu-id="30035-108">Members</span></span>

<span data-ttu-id="30035-109">Die **MSVM \_ Terminalservice** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="30035-109">The **Msvm\_TerminalService** class has these types of members:</span></span>

-   [<span data-ttu-id="30035-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="30035-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="30035-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="30035-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="30035-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="30035-112">Methods</span></span>

<span data-ttu-id="30035-113">Die **MSVM \_ Terminalservice** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="30035-113">The **Msvm\_TerminalService** class has these methods.</span></span>



| <span data-ttu-id="30035-114">Methode</span><span class="sxs-lookup"><span data-stu-id="30035-114">Method</span></span>                                                                                        | <span data-ttu-id="30035-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="30035-115">Description</span></span>                                                                                                      |
|:----------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="30035-116">**Getinteractivesessionacl**</span><span class="sxs-lookup"><span data-stu-id="30035-116">**GetInteractiveSessionACL**</span></span>](getinteractivesessionacl-msvm-terminalservice.md)             | <span data-ttu-id="30035-117">Ruft die aktuelle DACL ab, mit der der Zugriff auf die interaktive Sitzung eines virtuellen Computers gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="30035-117">Retrieves the current DACL that controls access to the interactive session of a virtual machine.</span></span><br/>      |
| [<span data-ttu-id="30035-118">**Grantinteractivesessionaccess**</span><span class="sxs-lookup"><span data-stu-id="30035-118">**GrantInteractiveSessionAccess**</span></span>](grantinteractivesessionaccess-msvm-terminalservice.md)   | <span data-ttu-id="30035-119">Ermöglicht den Zugriff auf die interaktive Sitzung des virtuellen Computers auf die angegebene Liste von Treuhändern.</span><span class="sxs-lookup"><span data-stu-id="30035-119">Grants access to the interactive session of the virtual machine to the specified list of trustees.</span></span><br/>    |
| [<span data-ttu-id="30035-120">**Modifyservicesettings**</span><span class="sxs-lookup"><span data-stu-id="30035-120">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-terminalservice.md)                   | <span data-ttu-id="30035-121">Ändert die Einstellungsdaten für den Dienst.</span><span class="sxs-lookup"><span data-stu-id="30035-121">Modifies the setting data for the service.</span></span><br/>                                                            |
| [<span data-ttu-id="30035-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="30035-122">**RequestStateChange**</span></span>](msvm-terminalservice-requeststatechange.md)                         | <span data-ttu-id="30035-123">Fordert eine Statusänderung an.</span><span class="sxs-lookup"><span data-stu-id="30035-123">Requests a state change.</span></span><br/>                                                                              |
| [<span data-ttu-id="30035-124">**Revokeinteractivesessionaccess**</span><span class="sxs-lookup"><span data-stu-id="30035-124">**RevokeInteractiveSessionAccess**</span></span>](revokeinteractivesessionaccess-msvm-terminalservice.md) | <span data-ttu-id="30035-125">Widerruft den Zugriff auf die interaktive Sitzung der virtuellen Maschine aus der angegebenen Liste von Treuhändern.</span><span class="sxs-lookup"><span data-stu-id="30035-125">Revokes access to the interactive session of the virtual machine from the specified list of trustees.</span></span><br/> |
| [<span data-ttu-id="30035-126">**Start Service**</span><span class="sxs-lookup"><span data-stu-id="30035-126">**StartService**</span></span>](msvm-terminalservice-startservice.md)                                     | <span data-ttu-id="30035-127">Startet den Dienst.</span><span class="sxs-lookup"><span data-stu-id="30035-127">Starts the service.</span></span><br/>                                                                                   |
| [<span data-ttu-id="30035-128">**Stop Service**</span><span class="sxs-lookup"><span data-stu-id="30035-128">**StopService**</span></span>](msvm-terminalservice-stopservice.md)                                       | <span data-ttu-id="30035-129">Beendet den Dienst.</span><span class="sxs-lookup"><span data-stu-id="30035-129">Stops the service.</span></span><br/>                                                                                    |



 

### <a name="properties"></a><span data-ttu-id="30035-130">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="30035-130">Properties</span></span>

<span data-ttu-id="30035-131">Die **MSVM \_ Terminalservice** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="30035-131">The **Msvm\_TerminalService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="30035-132">**Availablerequestedstates**</span><span class="sxs-lookup"><span data-stu-id="30035-132">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30035-133">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="30035-133">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="30035-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="30035-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="30035-135">Gibt die möglichen Werte für den *requestedstate* -Parameter der **requestStateChange** -Methode an.</span><span class="sxs-lookup"><span data-stu-id="30035-135">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="30035-136">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="30035-136">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="30035-137">**Caption**</span><span class="sxs-lookup"><span data-stu-id="30035-137">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30035-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="30035-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30035-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="30035-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="30035-140">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="30035-140">A short description of the object.</span></span> <span data-ttu-id="30035-141">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="30035-141">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="30035-142">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="30035-142">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30035-143">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="30035-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="30035-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="30035-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="30035-145">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="30035-145">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="30035-146">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="30035-146">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="30035-147">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="30035-147">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="30035-148"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="30035-148"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="30035-149"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="30035-149"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="30035-150"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Kommunikation OK** (2)</span><span class="sxs-lookup"><span data-stu-id="30035-150"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="30035-151"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Verlorene Kommunikation** (3)</span><span class="sxs-lookup"><span data-stu-id="30035-151"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="30035-152"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Kein Kontakt** (4)</span><span class="sxs-lookup"><span data-stu-id="30035-152"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="30035-153"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="30035-153"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="30035-154"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="30035-154"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="30035-155">)</span><span class="sxs-lookup"><span data-stu-id="30035-155">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="30035-156">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="30035-156">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30035-157">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="30035-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30035-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="30035-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="30035-159">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer-Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="30035-159">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="30035-160">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.</span><span class="sxs-lookup"><span data-stu-id="30035-160">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="30035-161">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="30035-161">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30035-162">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="30035-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30035-163">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="30035-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="30035-164">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="30035-164">A description of the object.</span></span> <span data-ttu-id="30035-165">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="30035-165">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="30035-166">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="30035-166">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30035-167">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="30035-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="30035-168">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="30035-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="30035-169">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="30035-169">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="30035-170">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="30035-170">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="30035-171">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="30035-171">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="30035-172"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (0)</span><span class="sxs-lookup"><span data-stu-id="30035-172"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="30035-173"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Keine zusätzlichen Informationen** (1)</span><span class="sxs-lookup"><span data-stu-id="30035-173"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="30035-174"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Betont** (2)</span><span class="sxs-lookup"><span data-stu-id="30035-174"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="30035-175"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Vorhersagefehler** (3)</span><span class="sxs-lookup"><span data-stu-id="30035-175"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="30035-176"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Nicht BEHEB barer Fehler** (4)</span><span class="sxs-lookup"><span data-stu-id="30035-176"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="30035-177"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Unterstützende Entität in Error** (5)</span><span class="sxs-lookup"><span data-stu-id="30035-177"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="30035-178"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="30035-178"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="30035-179"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="30035-179"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="30035-180">)</span><span class="sxs-lookup"><span data-stu-id="30035-180">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="30035-181">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="30035-181">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30035-182">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="30035-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30035-183">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="30035-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="30035-184">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="30035-184">A display name for the object.</span></span> <span data-ttu-id="30035-185">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="30035-185">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="30035-186">**Enableddefault**</span><span class="sxs-lookup"><span data-stu-id="30035-186">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30035-187">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="30035-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="30035-188">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="30035-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="30035-189">Die Standard-oder Startkonfiguration eines Administrators für den aktivierten Zustand eines Elements.</span><span class="sxs-lookup"><span data-stu-id="30035-189">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="30035-190">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="30035-190">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="30035-191">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="30035-191">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30035-192">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="30035-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30035-193">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="30035-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="30035-194">Der aktivierte und deaktivierte Status eines Elements.</span><span class="sxs-lookup"><span data-stu-id="30035-194">The enabled and disabled states of an element.</span></span> <span data-ttu-id="30035-195">Sie kann auch die Übergänge zwischen diesen angeforderten Zuständen angeben.</span><span class="sxs-lookup"><span data-stu-id="30035-195">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="30035-196">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="30035-196">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="30035-197">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="30035-197">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30035-198">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="30035-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="30035-199">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="30035-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="30035-200">Der aktuelle Zustand des Elements.</span><span class="sxs-lookup"><span data-stu-id="30035-200">The current health of the element.</span></span> <span data-ttu-id="30035-201">Dieses Attribut drückt den Zustand dieses Elements aus, aber nicht notwendigerweise dessen unter Komponenten.</span><span class="sxs-lookup"><span data-stu-id="30035-201">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="30035-202">Mögliche Werte sind 0 bis 30, wobei 5 bedeutet, dass das Element vollständig fehlerfrei ist und 30 bedeutet, dass das Element vollständig nicht funktionsfähig ist.</span><span class="sxs-lookup"><span data-stu-id="30035-202">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="30035-203">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="30035-203">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="30035-204">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="30035-204">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30035-205">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="30035-205">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="30035-206">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="30035-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="30035-207">Das Datum und die Uhrzeit der Erstellung der Konfiguration der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="30035-207">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="30035-208">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="30035-208">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="30035-209">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="30035-209">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30035-210">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="30035-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30035-211">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="30035-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="30035-212">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="30035-212">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="30035-213">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="30035-213">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="30035-214">Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="30035-214">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="30035-215">**Name**</span><span class="sxs-lookup"><span data-stu-id="30035-215">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30035-216">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="30035-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30035-217">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="30035-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="30035-218">Die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="30035-218">The label by which the object is known.</span></span> <span data-ttu-id="30035-219">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.</span><span class="sxs-lookup"><span data-stu-id="30035-219">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="30035-220">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="30035-220">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30035-221">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="30035-221">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="30035-222">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="30035-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="30035-223">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="30035-223">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="30035-224">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="30035-224">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="30035-225">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="30035-225">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="30035-226"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="30035-226"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="30035-227"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="30035-227"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="30035-228"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Wartung** (2)</span><span class="sxs-lookup"><span data-stu-id="30035-228"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="30035-229"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>Wird **gestartet** (3)</span><span class="sxs-lookup"><span data-stu-id="30035-229"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="30035-230"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>Wird **beendet (4** )</span><span class="sxs-lookup"><span data-stu-id="30035-230"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="30035-231"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Beendet** (5)</span><span class="sxs-lookup"><span data-stu-id="30035-231"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="30035-232"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abgebrochen** (6)</span><span class="sxs-lookup"><span data-stu-id="30035-232"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="30035-233"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Ruhende** (7)</span><span class="sxs-lookup"><span data-stu-id="30035-233"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="30035-234"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Abgeschlossen** (8)</span><span class="sxs-lookup"><span data-stu-id="30035-234"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="30035-235"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrieren** (9)</span><span class="sxs-lookup"><span data-stu-id="30035-235"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="30035-236"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Migration** (10)</span><span class="sxs-lookup"><span data-stu-id="30035-236"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="30035-237"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migration** (11)</span><span class="sxs-lookup"><span data-stu-id="30035-237"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="30035-238"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotts** (12)</span><span class="sxs-lookup"><span data-stu-id="30035-238"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="30035-239"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Herunter** fahren (13)</span><span class="sxs-lookup"><span data-stu-id="30035-239"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="30035-240"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span><span class="sxs-lookup"><span data-stu-id="30035-240"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="30035-241"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Übergang** (15)</span><span class="sxs-lookup"><span data-stu-id="30035-241"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="30035-242"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Dienst** (16)</span><span class="sxs-lookup"><span data-stu-id="30035-242"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="30035-243"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="30035-243"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="30035-244"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="30035-244"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="30035-245">)</span><span class="sxs-lookup"><span data-stu-id="30035-245">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="30035-246">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="30035-246">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30035-247">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="30035-247">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="30035-248">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="30035-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="30035-249">Die aktuellen Status des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="30035-249">The current statuses of the object.</span></span> <span data-ttu-id="30035-250">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="30035-250">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="30035-251">**Otherenabledstate**</span><span class="sxs-lookup"><span data-stu-id="30035-251">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30035-252">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="30035-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30035-253">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="30035-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="30035-254">Eine Zeichenfolge, die den aktivierten oder deaktivierten Status des Elements beschreibt, wenn die **enabledstate** -Eigenschaft auf 1 (Sonstiges) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="30035-254">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="30035-255">Diese Eigenschaft muss auf **null** festgelegt werden, wenn **enabledstate** ein anderer Wert als 1 ist.</span><span class="sxs-lookup"><span data-stu-id="30035-255">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="30035-256">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="30035-256">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="30035-257">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="30035-257">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30035-258">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="30035-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30035-259">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="30035-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="30035-260">Ein Wert, der Informationen darüber bereitstellt, wie der primäre Besitzer des Dienstanbieter erreicht werden kann (z. b. Telefonnummer, e-Mail-Adresse usw.).</span><span class="sxs-lookup"><span data-stu-id="30035-260">A value that provides information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="30035-261">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.</span><span class="sxs-lookup"><span data-stu-id="30035-261">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="30035-262">**Primaryownername**</span><span class="sxs-lookup"><span data-stu-id="30035-262">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30035-263">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="30035-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30035-264">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="30035-264">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="30035-265">Der Name des primären Besitzers für den Dienst, sofern definiert.</span><span class="sxs-lookup"><span data-stu-id="30035-265">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="30035-266">Der primäre Besitzer ist der erste Support Kontakt für den Dienst.</span><span class="sxs-lookup"><span data-stu-id="30035-266">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="30035-267">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.</span><span class="sxs-lookup"><span data-stu-id="30035-267">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="30035-268">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="30035-268">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30035-269">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="30035-269">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="30035-270">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="30035-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="30035-271">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="30035-271">Provides high level status information.</span></span> <span data-ttu-id="30035-272">Diese Eigenschaft sollte in Verbindung mit der Eigenschaft **detailedstatus** verwendet werden, um einen hohen und detaillierten Integritäts Status des Elements und seiner unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="30035-272">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="30035-273">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="30035-273">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="30035-274">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="30035-274">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="30035-275"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="30035-275"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="30035-276"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="30035-276"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="30035-277"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (2** )</span><span class="sxs-lookup"><span data-stu-id="30035-277"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="30035-278"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Fehler** (3)</span><span class="sxs-lookup"><span data-stu-id="30035-278"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="30035-279"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="30035-279"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="30035-280"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="30035-280"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="30035-281">)</span><span class="sxs-lookup"><span data-stu-id="30035-281">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="30035-282">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="30035-282">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30035-283">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="30035-283">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="30035-284">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="30035-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="30035-285">Der zuletzt angeforderte oder gewünschte Zustand für das Element.</span><span class="sxs-lookup"><span data-stu-id="30035-285">The last requested or desired state for the element.</span></span> <span data-ttu-id="30035-286">Der tatsächliche Zustand des Elements wird durch **enabledstate** dargestellt.</span><span class="sxs-lookup"><span data-stu-id="30035-286">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="30035-287">Diese Eigenschaft wird bereitgestellt, um die zuletzt angeforderten und aktuell aktivierten oder deaktivierten Zustände zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="30035-287">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="30035-288">Eine bestimmte Instanz von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85)) unterstützt möglicherweise nicht die **requestStateChange** -Methode.</span><span class="sxs-lookup"><span data-stu-id="30035-288">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="30035-289">Wenn dies auftritt, wird der Wert 12 (nicht zutreffend) verwendet.</span><span class="sxs-lookup"><span data-stu-id="30035-289">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="30035-290">Diese Eigenschaft wird von **CIM \_ enabledlogicalelement** geerbt.</span><span class="sxs-lookup"><span data-stu-id="30035-290">This property is inherited from **CIM\_EnabledLogicalElement**.</span></span>

</dd> <dt>

<span data-ttu-id="30035-291">**Gestartet**</span><span class="sxs-lookup"><span data-stu-id="30035-291">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30035-292">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="30035-292">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="30035-293">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="30035-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="30035-294">Gibt an, ob der Dienst gerade ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="30035-294">Indicates whether the service is currently running.</span></span> <span data-ttu-id="30035-295">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.</span><span class="sxs-lookup"><span data-stu-id="30035-295">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="30035-296">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="30035-296">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30035-297">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="30035-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30035-298">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="30035-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="30035-299">Ein Zeichen folgen Wert, der angibt, ob der Dienst automatisch von einem System oder einem Betriebssystem gestartet oder nur nach Anforderung gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="30035-299">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="30035-300">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.</span><span class="sxs-lookup"><span data-stu-id="30035-300">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="30035-301">**Status**</span><span class="sxs-lookup"><span data-stu-id="30035-301">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30035-302">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="30035-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30035-303">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="30035-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="30035-304">Der Status des Elements.</span><span class="sxs-lookup"><span data-stu-id="30035-304">The status of the element.</span></span> <span data-ttu-id="30035-305">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="30035-305">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="30035-306">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="30035-306">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30035-307">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="30035-307">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="30035-308">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="30035-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="30035-309">Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="30035-309">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="30035-310">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="30035-310">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="30035-311">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="30035-311">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30035-312">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="30035-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30035-313">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="30035-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="30035-314">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="30035-314">The scoping system's creation class name.</span></span> <span data-ttu-id="30035-315">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.</span><span class="sxs-lookup"><span data-stu-id="30035-315">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="30035-316">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="30035-316">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30035-317">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="30035-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30035-318">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="30035-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="30035-319">Der Name des hostingcomputersystems.</span><span class="sxs-lookup"><span data-stu-id="30035-319">The name of the hosting computer system.</span></span> <span data-ttu-id="30035-320">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.</span><span class="sxs-lookup"><span data-stu-id="30035-320">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="30035-321">**Timeoflaststatechange**</span><span class="sxs-lookup"><span data-stu-id="30035-321">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30035-322">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="30035-322">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="30035-323">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="30035-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="30035-324">Das Datum oder die Uhrzeit, zu dem der aktivierte Status des Elements zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="30035-324">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="30035-325">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="30035-325">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="30035-326">**Transitioningumstate**</span><span class="sxs-lookup"><span data-stu-id="30035-326">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30035-327">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="30035-327">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="30035-328">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="30035-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="30035-329">Gibt den Ziel Status an, in den die-Instanz übergeht.</span><span class="sxs-lookup"><span data-stu-id="30035-329">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="30035-330">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="30035-330">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="30035-331">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="30035-331">Remarks</span></span>

<span data-ttu-id="30035-332">Der Zugriff auf die **MSVM \_ Terminalservice** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="30035-332">Access to the **Msvm\_TerminalService** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="30035-333">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="30035-333">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="30035-334">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="30035-334">Requirements</span></span>



| <span data-ttu-id="30035-335">Anforderung</span><span class="sxs-lookup"><span data-stu-id="30035-335">Requirement</span></span> | <span data-ttu-id="30035-336">Wert</span><span class="sxs-lookup"><span data-stu-id="30035-336">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30035-337">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="30035-337">Minimum supported client</span></span><br/> | <span data-ttu-id="30035-338">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="30035-338">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="30035-339">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="30035-339">Minimum supported server</span></span><br/> | <span data-ttu-id="30035-340">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="30035-340">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="30035-341">Namespace</span><span class="sxs-lookup"><span data-stu-id="30035-341">Namespace</span></span><br/>                | <span data-ttu-id="30035-342">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="30035-342">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="30035-343">MOF</span><span class="sxs-lookup"><span data-stu-id="30035-343">MOF</span></span><br/>                      | <dl> <span data-ttu-id="30035-344"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="30035-344"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="30035-345">DLL</span><span class="sxs-lookup"><span data-stu-id="30035-345">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30035-346"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="30035-346"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="30035-347">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30035-347">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30035-348">**CIM- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="30035-348">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

