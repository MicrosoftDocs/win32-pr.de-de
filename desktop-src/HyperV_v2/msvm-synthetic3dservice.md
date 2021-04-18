---
description: Beschreibt den synthetischen 3D-GPU-Dienst.
ms.assetid: fe3d6105-3def-453a-ad81-97cd0bb4613f
title: Msvm_Synthetic3DService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synthetic3DService
- Msvm_Synthetic3DService.RequestStateChange
- Msvm_Synthetic3DService.StartService
- Msvm_Synthetic3DService.StopService
- Msvm_Synthetic3DService.InstanceID
- Msvm_Synthetic3DService.Caption
- Msvm_Synthetic3DService.Description
- Msvm_Synthetic3DService.ElementName
- Msvm_Synthetic3DService.InstallDate
- Msvm_Synthetic3DService.OperationalStatus
- Msvm_Synthetic3DService.StatusDescriptions
- Msvm_Synthetic3DService.Status
- Msvm_Synthetic3DService.HealthState
- Msvm_Synthetic3DService.CommunicationStatus
- Msvm_Synthetic3DService.DetailedStatus
- Msvm_Synthetic3DService.OperatingStatus
- Msvm_Synthetic3DService.PrimaryStatus
- Msvm_Synthetic3DService.EnabledState
- Msvm_Synthetic3DService.OtherEnabledState
- Msvm_Synthetic3DService.RequestedState
- Msvm_Synthetic3DService.EnabledDefault
- Msvm_Synthetic3DService.TimeOfLastStateChange
- Msvm_Synthetic3DService.AvailableRequestedStates
- Msvm_Synthetic3DService.TransitioningToState
- Msvm_Synthetic3DService.SystemCreationClassName
- Msvm_Synthetic3DService.SystemName
- Msvm_Synthetic3DService.Name
- Msvm_Synthetic3DService.CreationClassName
- Msvm_Synthetic3DService.PrimaryOwnerName
- Msvm_Synthetic3DService.PrimaryOwnerContact
- Msvm_Synthetic3DService.StartMode
- Msvm_Synthetic3DService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e5bdacb764051f4bee2c9a646a00b09615ee5c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343763"
---
# <a name="msvm_synthetic3dservice-class"></a><span data-ttu-id="687a8-103">MSVM \_ Synthetic3DService-Klasse</span><span class="sxs-lookup"><span data-stu-id="687a8-103">Msvm\_Synthetic3DService class</span></span>

<span data-ttu-id="687a8-104">Beschreibt den synthetischen 3D-GPU-Dienst.</span><span class="sxs-lookup"><span data-stu-id="687a8-104">Describes the synthetic 3-D GPU service.</span></span>

> [!Note]  
> <span data-ttu-id="687a8-105">Diese Klasse ist für virtuelle Maschinen der Generation 2 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="687a8-105">This class is not available to generation 2 virtual machines.</span></span>

 

<span data-ttu-id="687a8-106">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="687a8-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="687a8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="687a8-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Synthetic3DService : CIM_Service
{
  string   InstanceID;
  string   Caption = "Synthetic3D Service";
  string   Description = "Microsoft Synthetic3D Service";
  string   ElementName = "Synthetic3D Service";
  datetime InstallDate;
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "The Synthetic 3D service is fully operational." };
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
  string   Name = "synth3d";
  string   CreationClassName = "Msvm_Synthetic3DService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started;
};
```

## <a name="members"></a><span data-ttu-id="687a8-108">Member</span><span class="sxs-lookup"><span data-stu-id="687a8-108">Members</span></span>

<span data-ttu-id="687a8-109">Die **MSVM \_ Synthetic3DService** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="687a8-109">The **Msvm\_Synthetic3DService** class has these types of members:</span></span>

-   [<span data-ttu-id="687a8-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="687a8-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="687a8-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="687a8-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="687a8-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="687a8-112">Methods</span></span>

<span data-ttu-id="687a8-113">Die **MSVM- \_ Synthetic3DService** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="687a8-113">The **Msvm\_Synthetic3DService** class has these methods.</span></span>



| <span data-ttu-id="687a8-114">Methode</span><span class="sxs-lookup"><span data-stu-id="687a8-114">Method</span></span>                                                                                     | <span data-ttu-id="687a8-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="687a8-115">Description</span></span>                                                         |
|:-------------------------------------------------------------------------------------------|:--------------------------------------------------------------------|
| [<span data-ttu-id="687a8-116">**Disablegpuforvirtualization**</span><span class="sxs-lookup"><span data-stu-id="687a8-116">**DisableGPUForVirtualization**</span></span>](disablegpuforvirtualization-msvm-synthetic3dservice.md) | <span data-ttu-id="687a8-117">Deaktiviert eine physische GPU für die Virtualisierung.</span><span class="sxs-lookup"><span data-stu-id="687a8-117">Disables a physical GPU for virtualization.</span></span><br/>              |
| [<span data-ttu-id="687a8-118">**Enablegpuforvirtualization**</span><span class="sxs-lookup"><span data-stu-id="687a8-118">**EnableGPUForVirtualization**</span></span>](enablegpuforvirtualization-msvm-synthetic3dservice.md)   | <span data-ttu-id="687a8-119">Aktiviert eine physische GPU für die Virtualisierung.</span><span class="sxs-lookup"><span data-stu-id="687a8-119">Enables a physical GPU for virtualization.</span></span><br/>               |
| [<span data-ttu-id="687a8-120">**Modifyservicesettings**</span><span class="sxs-lookup"><span data-stu-id="687a8-120">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-synthetic3dservice.md)             | <span data-ttu-id="687a8-121">Ändert die Einstellungsdaten für den synthetischen 3D-Dienst.</span><span class="sxs-lookup"><span data-stu-id="687a8-121">Modifies the setting data for the synthetic 3-D service.</span></span><br/> |
| <span data-ttu-id="687a8-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="687a8-122">**RequestStateChange**</span></span>                                                                     | <span data-ttu-id="687a8-123">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="687a8-123">This method is not supported.</span></span><br/>                            |
| <span data-ttu-id="687a8-124">**Start Service**</span><span class="sxs-lookup"><span data-stu-id="687a8-124">**StartService**</span></span>                                                                           | <span data-ttu-id="687a8-125">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="687a8-125">This method is not supported.</span></span><br/>                            |
| <span data-ttu-id="687a8-126">**Stop Service**</span><span class="sxs-lookup"><span data-stu-id="687a8-126">**StopService**</span></span>                                                                            | <span data-ttu-id="687a8-127">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="687a8-127">This method is not supported.</span></span><br/>                            |



 

### <a name="properties"></a><span data-ttu-id="687a8-128">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="687a8-128">Properties</span></span>

<span data-ttu-id="687a8-129">Die **MSVM- \_ Synthetic3DService** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="687a8-129">The **Msvm\_Synthetic3DService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="687a8-130">**Availablerequestedstates**</span><span class="sxs-lookup"><span data-stu-id="687a8-130">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="687a8-131">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="687a8-131">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="687a8-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="687a8-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="687a8-133">Gibt die möglichen Werte für den *requestedstate* -Parameter der **requestStateChange** -Methode an.</span><span class="sxs-lookup"><span data-stu-id="687a8-133">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="687a8-134">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="687a8-134">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="687a8-135">**Caption**</span><span class="sxs-lookup"><span data-stu-id="687a8-135">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="687a8-136">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="687a8-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="687a8-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="687a8-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="687a8-138">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="687a8-138">A short description of the object.</span></span> <span data-ttu-id="687a8-139">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="687a8-139">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="687a8-140">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="687a8-140">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="687a8-141">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="687a8-141">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="687a8-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="687a8-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="687a8-143">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="687a8-143">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="687a8-144">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="687a8-144">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="687a8-145">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="687a8-145">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="687a8-146"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="687a8-146"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="687a8-147"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="687a8-147"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="687a8-148"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Kommunikation OK** (2)</span><span class="sxs-lookup"><span data-stu-id="687a8-148"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="687a8-149"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Verlorene Kommunikation** (3)</span><span class="sxs-lookup"><span data-stu-id="687a8-149"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="687a8-150"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Kein Kontakt** (4)</span><span class="sxs-lookup"><span data-stu-id="687a8-150"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="687a8-151"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="687a8-151"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="687a8-152"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="687a8-152"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="687a8-153">)</span><span class="sxs-lookup"><span data-stu-id="687a8-153">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="687a8-154">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="687a8-154">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="687a8-155">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="687a8-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="687a8-156">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="687a8-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="687a8-157">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer-Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="687a8-157">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="687a8-158">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.</span><span class="sxs-lookup"><span data-stu-id="687a8-158">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="687a8-159">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="687a8-159">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="687a8-160">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="687a8-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="687a8-161">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="687a8-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="687a8-162">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="687a8-162">A description of the object.</span></span> <span data-ttu-id="687a8-163">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="687a8-163">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="687a8-164">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="687a8-164">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="687a8-165">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="687a8-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="687a8-166">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="687a8-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="687a8-167">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="687a8-167">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="687a8-168">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="687a8-168">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="687a8-169">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="687a8-169">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="687a8-170"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (0)</span><span class="sxs-lookup"><span data-stu-id="687a8-170"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="687a8-171"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Keine zusätzlichen Informationen** (1)</span><span class="sxs-lookup"><span data-stu-id="687a8-171"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="687a8-172"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Betont** (2)</span><span class="sxs-lookup"><span data-stu-id="687a8-172"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="687a8-173"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Vorhersagefehler** (3)</span><span class="sxs-lookup"><span data-stu-id="687a8-173"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="687a8-174"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Nicht BEHEB barer Fehler** (4)</span><span class="sxs-lookup"><span data-stu-id="687a8-174"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="687a8-175"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Unterstützende Entität in Error** (5)</span><span class="sxs-lookup"><span data-stu-id="687a8-175"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="687a8-176"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="687a8-176"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="687a8-177"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="687a8-177"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="687a8-178">)</span><span class="sxs-lookup"><span data-stu-id="687a8-178">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="687a8-179">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="687a8-179">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="687a8-180">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="687a8-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="687a8-181">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="687a8-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="687a8-182">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="687a8-182">A display name for the object.</span></span> <span data-ttu-id="687a8-183">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="687a8-183">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="687a8-184">**Enableddefault**</span><span class="sxs-lookup"><span data-stu-id="687a8-184">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="687a8-185">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="687a8-185">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="687a8-186">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="687a8-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="687a8-187">Die Standard-oder Startkonfiguration eines Administrators für den aktivierten Zustand eines Elements.</span><span class="sxs-lookup"><span data-stu-id="687a8-187">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="687a8-188">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="687a8-188">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="687a8-189">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="687a8-189">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="687a8-190">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="687a8-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="687a8-191">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="687a8-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="687a8-192">Der aktivierte und deaktivierte Status eines Elements.</span><span class="sxs-lookup"><span data-stu-id="687a8-192">The enabled and disabled states of an element.</span></span> <span data-ttu-id="687a8-193">Sie kann auch die Übergänge zwischen diesen angeforderten Zuständen angeben.</span><span class="sxs-lookup"><span data-stu-id="687a8-193">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="687a8-194">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="687a8-194">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="687a8-195">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="687a8-195">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="687a8-196">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="687a8-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="687a8-197">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="687a8-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="687a8-198">Der aktuelle Zustand des Elements.</span><span class="sxs-lookup"><span data-stu-id="687a8-198">The current health of the element.</span></span> <span data-ttu-id="687a8-199">Dieses Attribut drückt den Zustand dieses Elements aus, aber nicht notwendigerweise dessen unter Komponenten.</span><span class="sxs-lookup"><span data-stu-id="687a8-199">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="687a8-200">Mögliche Werte sind 0 bis 30, wobei 5 bedeutet, dass das Element vollständig fehlerfrei ist und 30 bedeutet, dass das Element vollständig nicht funktionsfähig ist.</span><span class="sxs-lookup"><span data-stu-id="687a8-200">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="687a8-201">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="687a8-201">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="687a8-202">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="687a8-202">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="687a8-203">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="687a8-203">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="687a8-204">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="687a8-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="687a8-205">Das Datum und die Uhrzeit der Erstellung der Konfiguration der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="687a8-205">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="687a8-206">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="687a8-206">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="687a8-207">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="687a8-207">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="687a8-208">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="687a8-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="687a8-209">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="687a8-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="687a8-210">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="687a8-210">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="687a8-211">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="687a8-211">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="687a8-212">Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="687a8-212">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="687a8-213">**Name**</span><span class="sxs-lookup"><span data-stu-id="687a8-213">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="687a8-214">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="687a8-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="687a8-215">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="687a8-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="687a8-216">Die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="687a8-216">The label by which the object is known.</span></span> <span data-ttu-id="687a8-217">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.</span><span class="sxs-lookup"><span data-stu-id="687a8-217">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="687a8-218">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="687a8-218">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="687a8-219">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="687a8-219">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="687a8-220">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="687a8-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="687a8-221">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="687a8-221">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="687a8-222">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="687a8-222">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="687a8-223">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="687a8-223">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="687a8-224"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="687a8-224"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="687a8-225"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="687a8-225"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="687a8-226"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Wartung** (2)</span><span class="sxs-lookup"><span data-stu-id="687a8-226"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="687a8-227"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>Wird **gestartet** (3)</span><span class="sxs-lookup"><span data-stu-id="687a8-227"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="687a8-228"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>Wird **beendet (4** )</span><span class="sxs-lookup"><span data-stu-id="687a8-228"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="687a8-229"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Beendet** (5)</span><span class="sxs-lookup"><span data-stu-id="687a8-229"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="687a8-230"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abgebrochen** (6)</span><span class="sxs-lookup"><span data-stu-id="687a8-230"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="687a8-231"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Ruhende** (7)</span><span class="sxs-lookup"><span data-stu-id="687a8-231"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="687a8-232"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Abgeschlossen** (8)</span><span class="sxs-lookup"><span data-stu-id="687a8-232"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="687a8-233"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrieren** (9)</span><span class="sxs-lookup"><span data-stu-id="687a8-233"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="687a8-234"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Migration** (10)</span><span class="sxs-lookup"><span data-stu-id="687a8-234"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="687a8-235"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migration** (11)</span><span class="sxs-lookup"><span data-stu-id="687a8-235"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="687a8-236"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotts** (12)</span><span class="sxs-lookup"><span data-stu-id="687a8-236"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="687a8-237"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Herunter** fahren (13)</span><span class="sxs-lookup"><span data-stu-id="687a8-237"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="687a8-238"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span><span class="sxs-lookup"><span data-stu-id="687a8-238"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="687a8-239"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Übergang** (15)</span><span class="sxs-lookup"><span data-stu-id="687a8-239"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="687a8-240"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Dienst** (16)</span><span class="sxs-lookup"><span data-stu-id="687a8-240"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="687a8-241"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="687a8-241"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="687a8-242"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="687a8-242"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="687a8-243">)</span><span class="sxs-lookup"><span data-stu-id="687a8-243">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="687a8-244">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="687a8-244">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="687a8-245">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="687a8-245">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="687a8-246">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="687a8-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="687a8-247">Die aktuellen Status des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="687a8-247">The current statuses of the object.</span></span> <span data-ttu-id="687a8-248">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="687a8-248">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="687a8-249">**Otherenabledstate**</span><span class="sxs-lookup"><span data-stu-id="687a8-249">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="687a8-250">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="687a8-250">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="687a8-251">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="687a8-251">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="687a8-252">Eine Zeichenfolge, die den aktivierten oder deaktivierten Status des Elements beschreibt, wenn die **enabledstate** -Eigenschaft auf 1 (Sonstiges) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="687a8-252">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="687a8-253">Diese Eigenschaft muss auf **null** festgelegt werden, wenn **enabledstate** ein anderer Wert als 1 ist.</span><span class="sxs-lookup"><span data-stu-id="687a8-253">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="687a8-254">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="687a8-254">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="687a8-255">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="687a8-255">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="687a8-256">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="687a8-256">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="687a8-257">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="687a8-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="687a8-258">Ein Wert, der Informationen darüber bereitstellt, wie der primäre Besitzer des Dienstanbieter erreicht werden kann (z. b. Telefonnummer, e-Mail-Adresse usw.).</span><span class="sxs-lookup"><span data-stu-id="687a8-258">A value that provides information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="687a8-259">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.</span><span class="sxs-lookup"><span data-stu-id="687a8-259">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="687a8-260">**Primaryownername**</span><span class="sxs-lookup"><span data-stu-id="687a8-260">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="687a8-261">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="687a8-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="687a8-262">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="687a8-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="687a8-263">Der Name des primären Besitzers für den Dienst, sofern definiert.</span><span class="sxs-lookup"><span data-stu-id="687a8-263">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="687a8-264">Der primäre Besitzer ist der erste Support Kontakt für den Dienst.</span><span class="sxs-lookup"><span data-stu-id="687a8-264">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="687a8-265">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.</span><span class="sxs-lookup"><span data-stu-id="687a8-265">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="687a8-266">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="687a8-266">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="687a8-267">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="687a8-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="687a8-268">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="687a8-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="687a8-269">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="687a8-269">Provides high level status information.</span></span> <span data-ttu-id="687a8-270">Diese Eigenschaft sollte in Verbindung mit der Eigenschaft **detailedstatus** verwendet werden, um einen hohen und detaillierten Integritäts Status des Elements und seiner unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="687a8-270">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="687a8-271">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="687a8-271">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="687a8-272">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="687a8-272">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="687a8-273"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="687a8-273"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="687a8-274"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="687a8-274"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="687a8-275"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (2** )</span><span class="sxs-lookup"><span data-stu-id="687a8-275"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="687a8-276"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Fehler** (3)</span><span class="sxs-lookup"><span data-stu-id="687a8-276"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="687a8-277"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="687a8-277"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="687a8-278"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="687a8-278"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="687a8-279">)</span><span class="sxs-lookup"><span data-stu-id="687a8-279">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="687a8-280">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="687a8-280">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="687a8-281">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="687a8-281">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="687a8-282">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="687a8-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="687a8-283">Der zuletzt angeforderte oder gewünschte Zustand für das Element.</span><span class="sxs-lookup"><span data-stu-id="687a8-283">The last requested or desired state for the element.</span></span> <span data-ttu-id="687a8-284">Der tatsächliche Zustand des Elements wird durch **enabledstate** dargestellt.</span><span class="sxs-lookup"><span data-stu-id="687a8-284">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="687a8-285">Diese Eigenschaft wird bereitgestellt, um die zuletzt angeforderten und aktuell aktivierten oder deaktivierten Zustände zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="687a8-285">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="687a8-286">Eine bestimmte Instanz der [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85)) -Klasse unterstützt möglicherweise nicht die **requestStateChange** -Methode.</span><span class="sxs-lookup"><span data-stu-id="687a8-286">A particular instance of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) class might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="687a8-287">Wenn dies auftritt, wird der Wert 12 (nicht zutreffend) verwendet.</span><span class="sxs-lookup"><span data-stu-id="687a8-287">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="687a8-288">Diese Eigenschaft wird von **CIM \_ enabledlogicalelement** geerbt.</span><span class="sxs-lookup"><span data-stu-id="687a8-288">This property is inherited from **CIM\_EnabledLogicalElement**.</span></span>

</dd> <dt>

<span data-ttu-id="687a8-289">**Gestartet**</span><span class="sxs-lookup"><span data-stu-id="687a8-289">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="687a8-290">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="687a8-290">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="687a8-291">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="687a8-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="687a8-292">Gibt an, ob der Dienst gerade ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="687a8-292">Indicates whether the service is currently running.</span></span> <span data-ttu-id="687a8-293">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.</span><span class="sxs-lookup"><span data-stu-id="687a8-293">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="687a8-294">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="687a8-294">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="687a8-295">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="687a8-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="687a8-296">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="687a8-296">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="687a8-297">Ein Zeichen folgen Wert, der angibt, ob der Dienst automatisch von einem System oder einem Betriebssystem gestartet oder nur nach Anforderung gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="687a8-297">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="687a8-298">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.</span><span class="sxs-lookup"><span data-stu-id="687a8-298">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="687a8-299">**Status**</span><span class="sxs-lookup"><span data-stu-id="687a8-299">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="687a8-300">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="687a8-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="687a8-301">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="687a8-301">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="687a8-302">Der Status des Elements.</span><span class="sxs-lookup"><span data-stu-id="687a8-302">The status of the element.</span></span> <span data-ttu-id="687a8-303">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="687a8-303">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="687a8-304">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="687a8-304">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="687a8-305">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="687a8-305">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="687a8-306">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="687a8-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="687a8-307">Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="687a8-307">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="687a8-308">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="687a8-308">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="687a8-309">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="687a8-309">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="687a8-310">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="687a8-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="687a8-311">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="687a8-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="687a8-312">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="687a8-312">The scoping system's creation class name.</span></span> <span data-ttu-id="687a8-313">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.</span><span class="sxs-lookup"><span data-stu-id="687a8-313">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="687a8-314">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="687a8-314">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="687a8-315">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="687a8-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="687a8-316">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="687a8-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="687a8-317">Der Name des hostingcomputersystems.</span><span class="sxs-lookup"><span data-stu-id="687a8-317">The name of the hosting computer system.</span></span> <span data-ttu-id="687a8-318">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.</span><span class="sxs-lookup"><span data-stu-id="687a8-318">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="687a8-319">**Timeoflaststatechange**</span><span class="sxs-lookup"><span data-stu-id="687a8-319">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="687a8-320">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="687a8-320">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="687a8-321">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="687a8-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="687a8-322">Das Datum oder die Uhrzeit, zu dem der aktivierte Status des Elements zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="687a8-322">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="687a8-323">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="687a8-323">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="687a8-324">**Transitioningumstate**</span><span class="sxs-lookup"><span data-stu-id="687a8-324">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="687a8-325">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="687a8-325">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="687a8-326">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="687a8-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="687a8-327">Gibt den Ziel Status an, in den die-Instanz übergeht.</span><span class="sxs-lookup"><span data-stu-id="687a8-327">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="687a8-328">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="687a8-328">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="687a8-329">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="687a8-329">Requirements</span></span>



| <span data-ttu-id="687a8-330">Anforderung</span><span class="sxs-lookup"><span data-stu-id="687a8-330">Requirement</span></span> | <span data-ttu-id="687a8-331">Wert</span><span class="sxs-lookup"><span data-stu-id="687a8-331">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="687a8-332">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="687a8-332">Minimum supported client</span></span><br/> | <span data-ttu-id="687a8-333">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="687a8-333">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="687a8-334">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="687a8-334">Minimum supported server</span></span><br/> | <span data-ttu-id="687a8-335">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="687a8-335">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="687a8-336">Namespace</span><span class="sxs-lookup"><span data-stu-id="687a8-336">Namespace</span></span><br/>                | <span data-ttu-id="687a8-337">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="687a8-337">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="687a8-338">MOF</span><span class="sxs-lookup"><span data-stu-id="687a8-338">MOF</span></span><br/>                      | <dl> <span data-ttu-id="687a8-339"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="687a8-339"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="687a8-340">DLL</span><span class="sxs-lookup"><span data-stu-id="687a8-340">DLL</span></span><br/>                      | <dl> <span data-ttu-id="687a8-341"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="687a8-341"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

