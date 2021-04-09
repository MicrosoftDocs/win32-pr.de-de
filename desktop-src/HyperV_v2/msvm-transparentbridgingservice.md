---
description: Dient als Platzhalter für den Dienst innerhalb des Schalters, der Mac-Adressen lernt und als Brücke zwischen den Klassen MSVM \_ virtualethernetstiwitch und MSVM \_ dynamicforwardingentry fungiert.
ms.assetid: E617DBC3-F5DD-4875-B3CC-E120A2218EBE
title: Msvm_TransparentBridgingService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TransparentBridgingService
- Msvm_TransparentBridgingService.InstanceID
- Msvm_TransparentBridgingService.Caption
- Msvm_TransparentBridgingService.Description
- Msvm_TransparentBridgingService.ElementName
- Msvm_TransparentBridgingService.InstallDate
- Msvm_TransparentBridgingService.OperationalStatus
- Msvm_TransparentBridgingService.StatusDescriptions
- Msvm_TransparentBridgingService.Status
- Msvm_TransparentBridgingService.HealthState
- Msvm_TransparentBridgingService.CommunicationStatus
- Msvm_TransparentBridgingService.DetailedStatus
- Msvm_TransparentBridgingService.OperatingStatus
- Msvm_TransparentBridgingService.PrimaryStatus
- Msvm_TransparentBridgingService.EnabledState
- Msvm_TransparentBridgingService.OtherEnabledState
- Msvm_TransparentBridgingService.RequestedState
- Msvm_TransparentBridgingService.EnabledDefault
- Msvm_TransparentBridgingService.TimeOfLastStateChange
- Msvm_TransparentBridgingService.AvailableRequestedStates
- Msvm_TransparentBridgingService.TransitioningToState
- Msvm_TransparentBridgingService.SystemCreationClassName
- Msvm_TransparentBridgingService.SystemName
- Msvm_TransparentBridgingService.CreationClassName
- Msvm_TransparentBridgingService.Name
- Msvm_TransparentBridgingService.PrimaryOwnerName
- Msvm_TransparentBridgingService.PrimaryOwnerContact
- Msvm_TransparentBridgingService.StartMode
- Msvm_TransparentBridgingService.Started
- Msvm_TransparentBridgingService.Keywords
- Msvm_TransparentBridgingService.ServiceURL
- Msvm_TransparentBridgingService.StartupConditions
- Msvm_TransparentBridgingService.StartupParameters
- Msvm_TransparentBridgingService.ProtocolType
- Msvm_TransparentBridgingService.OtherProtocolType
- Msvm_TransparentBridgingService.AgingTime
- Msvm_TransparentBridgingService.FID
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f5daacf42bc221fa98f56d0c5b84140e3784c2ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959185"
---
# <a name="msvm_transparentbridgingservice-class"></a><span data-ttu-id="194d3-103">MSVM- \_ transparentbridgingservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="194d3-103">Msvm\_TransparentBridgingService class</span></span>

<span data-ttu-id="194d3-104">Dient als Platzhalter für den Dienst innerhalb des Schalters, der Mac-Adressen lernt und als Brücke zwischen den Klassen [**MSVM \_ virtualethernetstiwitch**](msvm-virtualethernetswitch.md) und [**MSVM \_ dynamicforwardingentry**](msvm-dynamicforwardingentry.md) fungiert.</span><span class="sxs-lookup"><span data-stu-id="194d3-104">Serves as a placeholder for the service inside the switch that learns MAC addresses and serves as a bridge between the [**Msvm\_VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) and [**Msvm\_DynamicForwardingEntry**](msvm-dynamicforwardingentry.md) classes.</span></span>

<span data-ttu-id="194d3-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="194d3-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="194d3-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="194d3-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TransparentBridgingService : CIM_TransparentBridgingService
{
  string   InstanceID;
  string   Caption = "Virtual Switch Transparent Bridging Service";
  string   Description = "Microsoft Virtual Switch Transparent Bridging Service";
  string   ElementName;
  datetime InstallDate;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = "OK";
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_TransparentBridgingService";
  string   Name;
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode = "Automatic";
  boolean  Started = True;
  string   Keywords[];
  string   ServiceURL;
  string   StartupConditions[];
  string   StartupParameters[];
  uint16   ProtocolType = 15;
  string   OtherProtocolType;
  uint32   AgingTime = 300;
  uint32   FID = 0;
};
```

## <a name="members"></a><span data-ttu-id="194d3-107">Member</span><span class="sxs-lookup"><span data-stu-id="194d3-107">Members</span></span>

<span data-ttu-id="194d3-108">Die **MSVM-Klasse " \_ transparentbridgingservice** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="194d3-108">The **Msvm\_TransparentBridgingService** class has these types of members:</span></span>

-   [<span data-ttu-id="194d3-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="194d3-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="194d3-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="194d3-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="194d3-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="194d3-111">Methods</span></span>

<span data-ttu-id="194d3-112">Die **MSVM-Klasse " \_ transparentbridgingservice** " verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="194d3-112">The **Msvm\_TransparentBridgingService** class has these methods.</span></span>



| <span data-ttu-id="194d3-113">Methode</span><span class="sxs-lookup"><span data-stu-id="194d3-113">Method</span></span>                                                                           | <span data-ttu-id="194d3-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="194d3-114">Description</span></span>                         |
|:---------------------------------------------------------------------------------|:------------------------------------|
| [<span data-ttu-id="194d3-115">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="194d3-115">**RequestStateChange**</span></span>](msvm-transparentbridgingservice-requeststatechange.md) | <span data-ttu-id="194d3-116">Fordert eine Statusänderung an.</span><span class="sxs-lookup"><span data-stu-id="194d3-116">Requests a state change.</span></span><br/> |
| [<span data-ttu-id="194d3-117">**Start Service**</span><span class="sxs-lookup"><span data-stu-id="194d3-117">**StartService**</span></span>](msvm-transparentbridgingservice-startservice.md)             | <span data-ttu-id="194d3-118">Startet den Dienst.</span><span class="sxs-lookup"><span data-stu-id="194d3-118">Starts the service.</span></span><br/>      |
| [<span data-ttu-id="194d3-119">**Stop Service**</span><span class="sxs-lookup"><span data-stu-id="194d3-119">**StopService**</span></span>](msvm-transparentbridgingservice-stopservice.md)               | <span data-ttu-id="194d3-120">Beendet den Dienst.</span><span class="sxs-lookup"><span data-stu-id="194d3-120">Stops the service.</span></span><br/>       |



 

### <a name="properties"></a><span data-ttu-id="194d3-121">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="194d3-121">Properties</span></span>

<span data-ttu-id="194d3-122">Die **MSVM-Klasse " \_ transparentbridgingservice** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="194d3-122">The **Msvm\_TransparentBridgingService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="194d3-123">**Agingtime**</span><span class="sxs-lookup"><span data-stu-id="194d3-123">**AgingTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="194d3-124">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="194d3-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="194d3-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="194d3-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="194d3-126">Der Timeout Zeitraum (in Sekunden) für das Auslagern dynamisch erlernter Mac-Adressen.</span><span class="sxs-lookup"><span data-stu-id="194d3-126">The time-out period, in seconds, for aging out dynamically learned MAC addresses.</span></span> <span data-ttu-id="194d3-127">Diese Eigenschaft wird von [**CIM \_ transparentbridgingservice**](/previous-versions/windows/desktop/clushyperv/cim-transparentbridgingservice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="194d3-127">This property is inherited from [**CIM\_TransparentBridgingService**](/previous-versions/windows/desktop/clushyperv/cim-transparentbridgingservice).</span></span>

</dd> <dt>

<span data-ttu-id="194d3-128">**Availablerequestedstates**</span><span class="sxs-lookup"><span data-stu-id="194d3-128">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="194d3-129">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="194d3-129">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="194d3-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="194d3-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="194d3-131">Gibt die möglichen Werte für den *requestedstate* -Parameter der **requestStateChange** -Methode an.</span><span class="sxs-lookup"><span data-stu-id="194d3-131">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="194d3-132">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="194d3-132">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="194d3-133">**Caption**</span><span class="sxs-lookup"><span data-stu-id="194d3-133">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="194d3-134">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="194d3-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="194d3-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="194d3-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="194d3-136">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="194d3-136">A short description of the object.</span></span> <span data-ttu-id="194d3-137">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer "der virtuelle Switch Transparent Bridging Service".</span><span class="sxs-lookup"><span data-stu-id="194d3-137">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always "Virtual Switch Transparent Bridging Service".</span></span>

</dd> <dt>

<span data-ttu-id="194d3-138">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="194d3-138">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="194d3-139">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="194d3-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="194d3-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="194d3-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="194d3-141">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="194d3-141">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="194d3-142">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="194d3-142">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="194d3-143">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="194d3-143">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="194d3-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="194d3-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="194d3-145"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="194d3-145"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="194d3-146"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Kommunikation OK** (2)</span><span class="sxs-lookup"><span data-stu-id="194d3-146"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="194d3-147"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Verlorene Kommunikation** (3)</span><span class="sxs-lookup"><span data-stu-id="194d3-147"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="194d3-148"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Kein Kontakt** (4)</span><span class="sxs-lookup"><span data-stu-id="194d3-148"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="194d3-149"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="194d3-149"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="194d3-150"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="194d3-150"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="194d3-151">)</span><span class="sxs-lookup"><span data-stu-id="194d3-151">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="194d3-152">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="194d3-152">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="194d3-153">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="194d3-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="194d3-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="194d3-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="194d3-155">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="194d3-155">A short description of the object.</span></span> <span data-ttu-id="194d3-156">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.</span><span class="sxs-lookup"><span data-stu-id="194d3-156">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="194d3-157">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="194d3-157">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="194d3-158">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="194d3-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="194d3-159">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="194d3-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="194d3-160">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="194d3-160">A description of the object.</span></span> <span data-ttu-id="194d3-161">Diese Eigenschaft wird vom [**CIM- \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Microsoft Virtual Switch Transparent Bridging Service" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="194d3-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Virtual Switch Transparent Bridging Service".</span></span>

</dd> <dt>

<span data-ttu-id="194d3-162">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="194d3-162">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="194d3-163">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="194d3-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="194d3-164">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="194d3-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="194d3-165">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="194d3-165">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="194d3-166">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="194d3-166">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="194d3-167">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="194d3-167">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="194d3-168"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (0)</span><span class="sxs-lookup"><span data-stu-id="194d3-168"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="194d3-169"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Keine zusätzlichen Informationen** (1)</span><span class="sxs-lookup"><span data-stu-id="194d3-169"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="194d3-170"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Betont** (2)</span><span class="sxs-lookup"><span data-stu-id="194d3-170"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="194d3-171"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Vorhersagefehler** (3)</span><span class="sxs-lookup"><span data-stu-id="194d3-171"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="194d3-172"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Nicht BEHEB barer Fehler** (4)</span><span class="sxs-lookup"><span data-stu-id="194d3-172"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="194d3-173"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Unterstützende Entität in Error** (5)</span><span class="sxs-lookup"><span data-stu-id="194d3-173"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="194d3-174"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="194d3-174"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="194d3-175"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="194d3-175"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="194d3-176">)</span><span class="sxs-lookup"><span data-stu-id="194d3-176">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="194d3-177">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="194d3-177">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="194d3-178">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="194d3-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="194d3-179">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="194d3-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="194d3-180">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="194d3-180">A display name for the object.</span></span> <span data-ttu-id="194d3-181">Mit dieser Eigenschaft kann jede Instanz zusätzlich zu ihren Schlüsseleigenschaften, Identitätsdaten und Beschreibungs Informationen einen anzeigen Amen definieren.</span><span class="sxs-lookup"><span data-stu-id="194d3-181">This property allows each instance to define a display name in addition to its key properties, identity data, and description information.</span></span> <span data-ttu-id="194d3-182">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="194d3-182">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="194d3-183">**Enableddefault**</span><span class="sxs-lookup"><span data-stu-id="194d3-183">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="194d3-184">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="194d3-184">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="194d3-185">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="194d3-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="194d3-186">Die Standard-oder Startkonfiguration eines Administrators für den aktivierten Zustand eines Elements.</span><span class="sxs-lookup"><span data-stu-id="194d3-186">An administrator's default or startup configuration for the Enabled State of an element.</span></span> <span data-ttu-id="194d3-187">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="194d3-187">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="194d3-188">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="194d3-188">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="194d3-189">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="194d3-189">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="194d3-190">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="194d3-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="194d3-191">Der aktivierte und deaktivierte Status eines Elements.</span><span class="sxs-lookup"><span data-stu-id="194d3-191">The enabled and disabled states of an element.</span></span> <span data-ttu-id="194d3-192">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="194d3-192">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="194d3-193">**Angestrebt**</span><span class="sxs-lookup"><span data-stu-id="194d3-193">**FID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="194d3-194">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="194d3-194">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="194d3-195">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="194d3-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="194d3-196">Der Bezeichner der Filterungs Datenbank, der von Switches verwendet wird, die VLAN unterstützen und über mehrere Filter Datenbanken verfügen.</span><span class="sxs-lookup"><span data-stu-id="194d3-196">The filtering database identifier used by switches that support VLAN and that have more than one filtering database.</span></span> <span data-ttu-id="194d3-197">Diese Eigenschaft wird von [**CIM \_ transparentbridgingservice**](/previous-versions/windows/desktop/clushyperv/cim-transparentbridgingservice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="194d3-197">This property is inherited from [**CIM\_TransparentBridgingService**](/previous-versions/windows/desktop/clushyperv/cim-transparentbridgingservice).</span></span>

</dd> <dt>

<span data-ttu-id="194d3-198">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="194d3-198">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="194d3-199">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="194d3-199">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="194d3-200">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="194d3-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="194d3-201">Der aktuelle Zustand des Elements.</span><span class="sxs-lookup"><span data-stu-id="194d3-201">The current health of the element.</span></span> <span data-ttu-id="194d3-202">Dieses Attribut drückt den Zustand dieses Elements aus, aber nicht notwendigerweise dessen unter Komponenten.</span><span class="sxs-lookup"><span data-stu-id="194d3-202">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="194d3-203">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="194d3-203">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="194d3-204">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="194d3-204">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="194d3-205">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="194d3-205">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="194d3-206">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="194d3-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="194d3-207">Gibt die Uhrzeit an, zu der das-Objekt installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="194d3-207">Specifies the time when the object was installed.</span></span> <span data-ttu-id="194d3-208">Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="194d3-208">Lack of a value does not indicate that the object is not installed.</span></span> <span data-ttu-id="194d3-209">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="194d3-209">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="194d3-210">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="194d3-210">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="194d3-211">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="194d3-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="194d3-212">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="194d3-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="194d3-213">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="194d3-213">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="194d3-214">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="194d3-214">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="194d3-215">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="194d3-215">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="194d3-216">**Schlüsselwörter**</span><span class="sxs-lookup"><span data-stu-id="194d3-216">**Keywords**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="194d3-217">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="194d3-217">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="194d3-218">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="194d3-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="194d3-219">Darf nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="194d3-219">Do not use.</span></span> <span data-ttu-id="194d3-220">Ein frei Form Array von Zeichen folgen, die beschreibende Wörter und Ausdrücke bereitstellen, die in Abfragen verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="194d3-220">A free-form array of strings that provide descriptive words and phrases that can be used in queries.</span></span> <span data-ttu-id="194d3-221">Diese Eigenschaft ist nicht implementiert, da Sie nicht standardisiert ist.</span><span class="sxs-lookup"><span data-stu-id="194d3-221">This property is not implemented because it is not standardized.</span></span> <span data-ttu-id="194d3-222">Wenn diese Eigenschaft ein erforderliches Abfrage Konstrukt wäre, wäre sie in der Vererbungs Hierarchie höher.</span><span class="sxs-lookup"><span data-stu-id="194d3-222">If this property were a necessary query construct, then it would be required higher in the inheritance hierarchy.</span></span> <span data-ttu-id="194d3-223">Diese Eigenschaft wird vom [**CIM- \_ NetworkService**](/previous-versions//cc136875(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="194d3-223">This property is inherited from [**CIM\_NetworkService**](/previous-versions//cc136875(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="194d3-224">**Name**</span><span class="sxs-lookup"><span data-stu-id="194d3-224">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="194d3-225">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="194d3-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="194d3-226">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="194d3-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="194d3-227">Ein Name, der den Dienst eindeutig identifiziert und eine Angabe der verwalteten Funktionalität bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="194d3-227">A name that uniquely identifies the service and provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="194d3-228">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.</span><span class="sxs-lookup"><span data-stu-id="194d3-228">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="194d3-229">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="194d3-229">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="194d3-230">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="194d3-230">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="194d3-231">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="194d3-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="194d3-232">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="194d3-232">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="194d3-233">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="194d3-233">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="194d3-234">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="194d3-234">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="194d3-235"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="194d3-235"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="194d3-236"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="194d3-236"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="194d3-237"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Wartung** (2)</span><span class="sxs-lookup"><span data-stu-id="194d3-237"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="194d3-238"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>Wird **gestartet** (3)</span><span class="sxs-lookup"><span data-stu-id="194d3-238"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="194d3-239"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>Wird **beendet (4** )</span><span class="sxs-lookup"><span data-stu-id="194d3-239"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="194d3-240"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Beendet** (5)</span><span class="sxs-lookup"><span data-stu-id="194d3-240"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="194d3-241"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abgebrochen** (6)</span><span class="sxs-lookup"><span data-stu-id="194d3-241"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="194d3-242"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Ruhende** (7)</span><span class="sxs-lookup"><span data-stu-id="194d3-242"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="194d3-243"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Abgeschlossen** (8)</span><span class="sxs-lookup"><span data-stu-id="194d3-243"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="194d3-244"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrieren** (9)</span><span class="sxs-lookup"><span data-stu-id="194d3-244"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="194d3-245"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Migration** (10)</span><span class="sxs-lookup"><span data-stu-id="194d3-245"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="194d3-246"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migration** (11)</span><span class="sxs-lookup"><span data-stu-id="194d3-246"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="194d3-247"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotts** (12)</span><span class="sxs-lookup"><span data-stu-id="194d3-247"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="194d3-248"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Herunter** fahren (13)</span><span class="sxs-lookup"><span data-stu-id="194d3-248"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="194d3-249"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span><span class="sxs-lookup"><span data-stu-id="194d3-249"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="194d3-250"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Übergang** (15)</span><span class="sxs-lookup"><span data-stu-id="194d3-250"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="194d3-251"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Dienst** (16)</span><span class="sxs-lookup"><span data-stu-id="194d3-251"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="194d3-252"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="194d3-252"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="194d3-253"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="194d3-253"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="194d3-254">)</span><span class="sxs-lookup"><span data-stu-id="194d3-254">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="194d3-255">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="194d3-255">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="194d3-256">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="194d3-256">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="194d3-257">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="194d3-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="194d3-258">Der aktuelle Status des Elements.</span><span class="sxs-lookup"><span data-stu-id="194d3-258">The current status of the element.</span></span> <span data-ttu-id="194d3-259">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="194d3-259">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="194d3-260">**Otherenabledstate**</span><span class="sxs-lookup"><span data-stu-id="194d3-260">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="194d3-261">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="194d3-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="194d3-262">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="194d3-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="194d3-263">Der aktivierte oder deaktivierte Status des Elements, wenn die **enabledstate** -Eigenschaft auf 1 (Sonstiges) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="194d3-263">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="194d3-264">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="194d3-264">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="194d3-265">**Otherprotocoltype**</span><span class="sxs-lookup"><span data-stu-id="194d3-265">**OtherProtocolType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="194d3-266">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="194d3-266">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="194d3-267">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="194d3-267">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="194d3-268">Der Protokolltyp, der weitergeleitet wird, wenn der Wert von **ProtocolType** 1 (Other) ist.</span><span class="sxs-lookup"><span data-stu-id="194d3-268">The type of protocol that is being forwarded when the value of **ProtocolType** is 1 (Other).</span></span> <span data-ttu-id="194d3-269">Diese Eigenschaft wird von [**CIM \_ forwardingservice**](/previous-versions/windows/desktop/clushyperv/cim-forwardingservice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="194d3-269">This property is inherited from [**CIM\_ForwardingService**](/previous-versions/windows/desktop/clushyperv/cim-forwardingservice).</span></span>

</dd> <dt>

<span data-ttu-id="194d3-270">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="194d3-270">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="194d3-271">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="194d3-271">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="194d3-272">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="194d3-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="194d3-273">Eine Zeichenfolge, die Informationen darüber bereitstellt, wie der primäre Besitzer des Dienstanbieter erreicht werden kann.</span><span class="sxs-lookup"><span data-stu-id="194d3-273">A string that provides information about how the primary owner of the Service can be reached.</span></span> <span data-ttu-id="194d3-274">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.</span><span class="sxs-lookup"><span data-stu-id="194d3-274">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="194d3-275">**Primaryownername**</span><span class="sxs-lookup"><span data-stu-id="194d3-275">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="194d3-276">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="194d3-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="194d3-277">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="194d3-277">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="194d3-278">Der Name des primären Besitzers für den Dienst, sofern definiert.</span><span class="sxs-lookup"><span data-stu-id="194d3-278">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="194d3-279">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.</span><span class="sxs-lookup"><span data-stu-id="194d3-279">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="194d3-280">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="194d3-280">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="194d3-281">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="194d3-281">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="194d3-282">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="194d3-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="194d3-283">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="194d3-283">Provides high level status information.</span></span> <span data-ttu-id="194d3-284">Diese Eigenschaft sollte in Verbindung mit der Eigenschaft **detailedstatus** verwendet werden, um einen hohen und detaillierten Integritäts Status des Elements und seiner unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="194d3-284">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="194d3-285">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="194d3-285">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="194d3-286">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="194d3-286">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="194d3-287"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="194d3-287"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="194d3-288"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="194d3-288"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="194d3-289"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (2** )</span><span class="sxs-lookup"><span data-stu-id="194d3-289"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="194d3-290"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Fehler** (3)</span><span class="sxs-lookup"><span data-stu-id="194d3-290"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="194d3-291"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="194d3-291"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="194d3-292"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="194d3-292"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="194d3-293">)</span><span class="sxs-lookup"><span data-stu-id="194d3-293">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="194d3-294">**ProtocolType**</span><span class="sxs-lookup"><span data-stu-id="194d3-294">**ProtocolType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="194d3-295">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="194d3-295">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="194d3-296">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="194d3-296">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="194d3-297">Der Protokolltyp, der weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="194d3-297">The type of protocol that is being forwarded.</span></span> <span data-ttu-id="194d3-298">Diese Eigenschaft wird von [**CIM \_ forwardingservice**](/previous-versions/windows/desktop/clushyperv/cim-forwardingservice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="194d3-298">This property is inherited from [**CIM\_ForwardingService**](/previous-versions/windows/desktop/clushyperv/cim-forwardingservice).</span></span>

</dd> <dt>

<span data-ttu-id="194d3-299">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="194d3-299">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="194d3-300">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="194d3-300">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="194d3-301">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="194d3-301">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="194d3-302">Der zuletzt angeforderte oder gewünschte Status für den Verwaltungsdienst.</span><span class="sxs-lookup"><span data-stu-id="194d3-302">The last requested or desired state for the management service.</span></span> <span data-ttu-id="194d3-303">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="194d3-303">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="194d3-304">**ServiceUrl**</span><span class="sxs-lookup"><span data-stu-id="194d3-304">**ServiceURL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="194d3-305">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="194d3-305">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="194d3-306">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="194d3-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="194d3-307">Darf nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="194d3-307">Do not use.</span></span> <span data-ttu-id="194d3-308">Eine URL, die das Protokoll, den Netzwerk Speicherort und andere Dienst spezifische Informationen bereitstellt, die für den Zugriff auf den Dienst erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="194d3-308">A URL that provides the protocol, network location, and other service-specific information required to access the service.</span></span> <span data-ttu-id="194d3-309">Verwenden Sie stattdessen die **serviceaccessuri** -Klasse, die die Semantik des Dienst Zugriffs ordnungsgemäß positioniert und das Format der Informationen verdeutlicht.</span><span class="sxs-lookup"><span data-stu-id="194d3-309">Instead, use the **ServiceAccessURI** class, which correctly positions the semantics of the service access, and clarifies the format of the information.</span></span> <span data-ttu-id="194d3-310">Diese Eigenschaft wird vom [**CIM- \_ NetworkService**](/previous-versions//cc136875(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="194d3-310">This property is inherited from [**CIM\_NetworkService**](/previous-versions//cc136875(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="194d3-311">**Gestartet**</span><span class="sxs-lookup"><span data-stu-id="194d3-311">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="194d3-312">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="194d3-312">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="194d3-313">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="194d3-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="194d3-314">Gibt an, ob der Dienst gestartet wurde (**true**) oder beendet (**false**) ist.</span><span class="sxs-lookup"><span data-stu-id="194d3-314">Indicates whether the service has been started (**True**), or stopped (**False**).</span></span> <span data-ttu-id="194d3-315">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.</span><span class="sxs-lookup"><span data-stu-id="194d3-315">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="194d3-316">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="194d3-316">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="194d3-317">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="194d3-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="194d3-318">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="194d3-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="194d3-319">Gibt an, ob der Dienst automatisch von einem System, einem Betriebssystem usw. gestartet wird oder nur nach Anforderung gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="194d3-319">Indicates whether the service is automatically started by a system, an operating system, and so on, or is started only upon request.</span></span> <span data-ttu-id="194d3-320">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.</span><span class="sxs-lookup"><span data-stu-id="194d3-320">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="194d3-321">**Startupconditions**</span><span class="sxs-lookup"><span data-stu-id="194d3-321">**StartupConditions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="194d3-322">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="194d3-322">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="194d3-323">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="194d3-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="194d3-324">Darf nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="194d3-324">Do not use.</span></span> <span data-ttu-id="194d3-325">Ein frei Form Array von Zeichen folgen, die bestimmte Vorbedingungen angeben, die erfüllt sein müssen, damit dieser Dienst ordnungsgemäß gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="194d3-325">A free-form array of strings that specify any specific preconditions that must be met for this service to start correctly.</span></span> <span data-ttu-id="194d3-326">Diese Eigenschaft ist nicht sinnvoll, da Sie nicht standardisiert ist.</span><span class="sxs-lookup"><span data-stu-id="194d3-326">This property is not useful because it is not standardized.</span></span> <span data-ttu-id="194d3-327">Wenn diese Eigenschaft ein erforderliches Konstrukt wäre, wäre sie in der Vererbungs Hierarchie höher (für den Dienst).</span><span class="sxs-lookup"><span data-stu-id="194d3-327">If this property were a necessary construct, then it would be required higher in the inheritance hierarchy (on Service).</span></span> <span data-ttu-id="194d3-328">Diese Eigenschaft wird vom [**CIM- \_ NetworkService**](/previous-versions//cc136875(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="194d3-328">This property is inherited from [**CIM\_NetworkService**](/previous-versions//cc136875(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="194d3-329">**StartupParameters**</span><span class="sxs-lookup"><span data-stu-id="194d3-329">**StartupParameters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="194d3-330">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="194d3-330">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="194d3-331">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="194d3-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="194d3-332">Darf nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="194d3-332">Do not use.</span></span> <span data-ttu-id="194d3-333">Ein frei Form Array von Zeichen folgen, die bestimmte Parameter angeben, die für die Start **Service** -Methode bereitgestellt werden müssen, damit dieser Dienst ordnungsgemäß gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="194d3-333">A free-form array of strings that specify any specific parameters that must be supplied to the **StartService** method for this service to start correctly.</span></span> <span data-ttu-id="194d3-334">Wenn diese Methode optimiert wurde, würden diese Informationen von ihren Parametern eher formal vermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="194d3-334">If this method were refined, then its parameters would more formally convey this information.</span></span> <span data-ttu-id="194d3-335">Diese Eigenschaft wird vom [**CIM- \_ NetworkService**](/previous-versions//cc136875(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="194d3-335">This property is inherited from [**CIM\_NetworkService**](/previous-versions//cc136875(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="194d3-336">**Status**</span><span class="sxs-lookup"><span data-stu-id="194d3-336">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="194d3-337">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="194d3-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="194d3-338">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="194d3-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="194d3-339">Der aktuelle Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="194d3-339">The current status of the object.</span></span> <span data-ttu-id="194d3-340">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="194d3-340">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="194d3-341">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="194d3-341">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="194d3-342">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="194d3-342">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="194d3-343">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="194d3-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="194d3-344">Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="194d3-344">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="194d3-345">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="194d3-345">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="194d3-346">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="194d3-346">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="194d3-347">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="194d3-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="194d3-348">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="194d3-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="194d3-349">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="194d3-349">The creation class name of the scoping system.</span></span> <span data-ttu-id="194d3-350">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.</span><span class="sxs-lookup"><span data-stu-id="194d3-350">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="194d3-351">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="194d3-351">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="194d3-352">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="194d3-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="194d3-353">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="194d3-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="194d3-354">Der NetBIOS-Name des hostingcomputersystems.</span><span class="sxs-lookup"><span data-stu-id="194d3-354">The NetBIOS name of the hosting computer system.</span></span> <span data-ttu-id="194d3-355">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.</span><span class="sxs-lookup"><span data-stu-id="194d3-355">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="194d3-356">**Timeoflaststatechange**</span><span class="sxs-lookup"><span data-stu-id="194d3-356">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="194d3-357">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="194d3-357">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="194d3-358">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="194d3-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="194d3-359">Das Datum oder die Uhrzeit, zu dem der aktivierte Status des Elements zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="194d3-359">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="194d3-360">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="194d3-360">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="194d3-361">**Transitioningumstate**</span><span class="sxs-lookup"><span data-stu-id="194d3-361">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="194d3-362">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="194d3-362">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="194d3-363">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="194d3-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="194d3-364">Gibt den Ziel Status an, in den die-Instanz übergeht.</span><span class="sxs-lookup"><span data-stu-id="194d3-364">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="194d3-365">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="194d3-365">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="194d3-366">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="194d3-366">Remarks</span></span>

<span data-ttu-id="194d3-367">Der Zugriff auf die **MSVM-Klasse " \_ transparentbridgingservice** " kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="194d3-367">Access to the **Msvm\_TransparentBridgingService** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="194d3-368">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="194d3-368">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="194d3-369">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="194d3-369">Requirements</span></span>



| <span data-ttu-id="194d3-370">Anforderung</span><span class="sxs-lookup"><span data-stu-id="194d3-370">Requirement</span></span> | <span data-ttu-id="194d3-371">Wert</span><span class="sxs-lookup"><span data-stu-id="194d3-371">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="194d3-372">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="194d3-372">Minimum supported client</span></span><br/> | <span data-ttu-id="194d3-373">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="194d3-373">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="194d3-374">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="194d3-374">Minimum supported server</span></span><br/> | <span data-ttu-id="194d3-375">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="194d3-375">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="194d3-376">Namespace</span><span class="sxs-lookup"><span data-stu-id="194d3-376">Namespace</span></span><br/>                | <span data-ttu-id="194d3-377">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="194d3-377">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="194d3-378">MOF</span><span class="sxs-lookup"><span data-stu-id="194d3-378">MOF</span></span><br/>                      | <dl> <span data-ttu-id="194d3-379"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="194d3-379"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="194d3-380">DLL</span><span class="sxs-lookup"><span data-stu-id="194d3-380">DLL</span></span><br/>                      | <dl> <span data-ttu-id="194d3-381"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="194d3-381"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="194d3-382">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="194d3-382">See also</span></span>

<dl> <dt>

[<span data-ttu-id="194d3-383">**CIM- \_ transparentbridgingservice**</span><span class="sxs-lookup"><span data-stu-id="194d3-383">**CIM\_TransparentBridgingService**</span></span>](cim-transparentbridgingservice.md)
</dt> <dt>

[<span data-ttu-id="194d3-384">**CIM- \_ transparentbridgingservice**</span><span class="sxs-lookup"><span data-stu-id="194d3-384">**CIM\_TransparentBridgingService**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-transparentbridgingservice)
</dt> </dl>

 

