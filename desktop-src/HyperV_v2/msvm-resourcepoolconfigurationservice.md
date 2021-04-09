---
description: Ermöglicht die aktive Verwaltung von Ressourcenpools.
ms.assetid: 34ee3189-cb89-4d36-b12f-333449103968
title: Msvm_ResourcePoolConfigurationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationService
- Msvm_ResourcePoolConfigurationService.RequestStateChange
- Msvm_ResourcePoolConfigurationService.StartService
- Msvm_ResourcePoolConfigurationService.StopService
- Msvm_ResourcePoolConfigurationService.InstanceID
- Msvm_ResourcePoolConfigurationService.Caption
- Msvm_ResourcePoolConfigurationService.Description
- Msvm_ResourcePoolConfigurationService.ElementName
- Msvm_ResourcePoolConfigurationService.InstallDate
- Msvm_ResourcePoolConfigurationService.Name
- Msvm_ResourcePoolConfigurationService.OperationalStatus
- Msvm_ResourcePoolConfigurationService.StatusDescriptions
- Msvm_ResourcePoolConfigurationService.Status
- Msvm_ResourcePoolConfigurationService.HealthState
- Msvm_ResourcePoolConfigurationService.CommunicationStatus
- Msvm_ResourcePoolConfigurationService.DetailedStatus
- Msvm_ResourcePoolConfigurationService.OperatingStatus
- Msvm_ResourcePoolConfigurationService.PrimaryStatus
- Msvm_ResourcePoolConfigurationService.EnabledState
- Msvm_ResourcePoolConfigurationService.OtherEnabledState
- Msvm_ResourcePoolConfigurationService.RequestedState
- Msvm_ResourcePoolConfigurationService.EnabledDefault
- Msvm_ResourcePoolConfigurationService.TimeOfLastStateChange
- Msvm_ResourcePoolConfigurationService.AvailableRequestedStates
- Msvm_ResourcePoolConfigurationService.TransitioningToState
- Msvm_ResourcePoolConfigurationService.SystemCreationClassName
- Msvm_ResourcePoolConfigurationService.SystemName
- Msvm_ResourcePoolConfigurationService.CreationClassName
- Msvm_ResourcePoolConfigurationService.PrimaryOwnerName
- Msvm_ResourcePoolConfigurationService.PrimaryOwnerContact
- Msvm_ResourcePoolConfigurationService.StartMode
- Msvm_ResourcePoolConfigurationService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3160e8ac9ba011db70a5d7118e4d1f72733ff23f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868491"
---
# <a name="msvm_resourcepoolconfigurationservice-class"></a><span data-ttu-id="e1331-103">MSVM \_ resourcepoolconfigurationservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="e1331-103">Msvm\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="e1331-104">Ermöglicht die aktive Verwaltung von Ressourcenpools.</span><span class="sxs-lookup"><span data-stu-id="e1331-104">Provides for active management of resource pools.</span></span>

<span data-ttu-id="e1331-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e1331-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1331-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e1331-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_ResourcePoolConfigurationService : CIM_Service
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  string   CreationClassName;
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started;
};
```

## <a name="members"></a><span data-ttu-id="e1331-107">Member</span><span class="sxs-lookup"><span data-stu-id="e1331-107">Members</span></span>

<span data-ttu-id="e1331-108">Die **MSVM \_ resourcepoolconfigurationservice** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e1331-108">The **Msvm\_ResourcePoolConfigurationService** class has these types of members:</span></span>

-   [<span data-ttu-id="e1331-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="e1331-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="e1331-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e1331-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e1331-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="e1331-111">Methods</span></span>

<span data-ttu-id="e1331-112">Die **MSVM \_ resourcepoolconfigurationservice** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="e1331-112">The **Msvm\_ResourcePoolConfigurationService** class has these methods.</span></span>



| <span data-ttu-id="e1331-113">Methode</span><span class="sxs-lookup"><span data-stu-id="e1331-113">Method</span></span>                                                                                   | <span data-ttu-id="e1331-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e1331-114">Description</span></span>                                                                                  |
|:-----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e1331-115">**CreatePool**</span><span class="sxs-lookup"><span data-stu-id="e1331-115">**CreatePool**</span></span>](createpool-msvm-resourcepoolconfigurationservice.md)                   | <span data-ttu-id="e1331-116">Erstellt einen untergeordneten Ressourcenpool.</span><span class="sxs-lookup"><span data-stu-id="e1331-116">Creates a child resource pool.</span></span><br/>                                                    |
| [<span data-ttu-id="e1331-117">**DeletePool**</span><span class="sxs-lookup"><span data-stu-id="e1331-117">**DeletePool**</span></span>](deletepool-msvm-resourcepoolconfigurationservice.md)                   | <span data-ttu-id="e1331-118">Löscht einen Ressourcenpool.</span><span class="sxs-lookup"><span data-stu-id="e1331-118">Deletes a resource pool.</span></span><br/>                                                          |
| [<span data-ttu-id="e1331-119">**Modifypoolresources**</span><span class="sxs-lookup"><span data-stu-id="e1331-119">**ModifyPoolResources**</span></span>](modifypoolresources-msvm-resourcepoolconfigurationservice.md) | <span data-ttu-id="e1331-120">Ändert die Ressourcen Einstellungen des übergeordneten Pools für Ressourcen, die einem untergeordneten Pool zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="e1331-120">Changes the parent pool resource settings for resources assigned to a child pool.</span></span><br/> |
| [<span data-ttu-id="e1331-121">**Modifypoolsettings**</span><span class="sxs-lookup"><span data-stu-id="e1331-121">**ModifyPoolSettings**</span></span>](modifypoolsettings-msvm-resourcepoolconfigurationservice.md)   | <span data-ttu-id="e1331-122">Ändert die Einstellungen eines untergeordneten Pools, die nicht zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="e1331-122">Changes the settings of a child pool that are not allocation related.</span></span><br/>             |
| <span data-ttu-id="e1331-123">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="e1331-123">**RequestStateChange**</span></span>                                                                   | <span data-ttu-id="e1331-124">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e1331-124">This method is not supported.</span></span><br/>                                                     |
| <span data-ttu-id="e1331-125">**Start Service**</span><span class="sxs-lookup"><span data-stu-id="e1331-125">**StartService**</span></span>                                                                         | <span data-ttu-id="e1331-126">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e1331-126">This method is not supported.</span></span><br/>                                                     |
| <span data-ttu-id="e1331-127">**Stop Service**</span><span class="sxs-lookup"><span data-stu-id="e1331-127">**StopService**</span></span>                                                                          | <span data-ttu-id="e1331-128">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e1331-128">This method is not supported.</span></span><br/>                                                     |



 

### <a name="properties"></a><span data-ttu-id="e1331-129">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e1331-129">Properties</span></span>

<span data-ttu-id="e1331-130">Die **MSVM \_ resourcepoolconfigurationservice** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e1331-130">The **Msvm\_ResourcePoolConfigurationService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e1331-131">**Availablerequestedstates**</span><span class="sxs-lookup"><span data-stu-id="e1331-131">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1331-132">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="e1331-132">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e1331-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e1331-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1331-134">Gibt die möglichen Werte für den *requestedstate* -Parameter der **requestStateChange** -Methode an.</span><span class="sxs-lookup"><span data-stu-id="e1331-134">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="e1331-135">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e1331-135">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e1331-136">**Caption**</span><span class="sxs-lookup"><span data-stu-id="e1331-136">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1331-137">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e1331-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e1331-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e1331-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1331-139">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="e1331-139">A short description of the object.</span></span> <span data-ttu-id="e1331-140">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e1331-140">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e1331-141">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="e1331-141">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1331-142">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e1331-142">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e1331-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e1331-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1331-144">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="e1331-144">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="e1331-145">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="e1331-145">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e1331-146">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e1331-146">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="e1331-147"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="e1331-147"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e1331-148"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="e1331-148"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e1331-149"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Kommunikation OK** (2)</span><span class="sxs-lookup"><span data-stu-id="e1331-149"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e1331-150"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Verlorene Kommunikation** (3)</span><span class="sxs-lookup"><span data-stu-id="e1331-150"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e1331-151"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Kein Kontakt** (4)</span><span class="sxs-lookup"><span data-stu-id="e1331-151"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="e1331-152"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="e1331-152"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="e1331-153"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="e1331-153"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="e1331-154">)</span><span class="sxs-lookup"><span data-stu-id="e1331-154">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e1331-155">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="e1331-155">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1331-156">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e1331-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e1331-157">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e1331-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e1331-158">Qualifizierer: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="e1331-158">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="e1331-159">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer-Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e1331-159">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="e1331-160">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e1331-160">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="e1331-161">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e1331-161">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1331-162">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e1331-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e1331-163">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e1331-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1331-164">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="e1331-164">A description of the object.</span></span> <span data-ttu-id="e1331-165">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e1331-165">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e1331-166">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="e1331-166">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1331-167">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e1331-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e1331-168">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e1331-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1331-169">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="e1331-169">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="e1331-170">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="e1331-170">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e1331-171">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e1331-171">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="e1331-172"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (0)</span><span class="sxs-lookup"><span data-stu-id="e1331-172"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e1331-173"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Keine zusätzlichen Informationen** (1)</span><span class="sxs-lookup"><span data-stu-id="e1331-173"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e1331-174"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Betont** (2)</span><span class="sxs-lookup"><span data-stu-id="e1331-174"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e1331-175"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Vorhersagefehler** (3)</span><span class="sxs-lookup"><span data-stu-id="e1331-175"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e1331-176"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Nicht BEHEB barer Fehler** (4)</span><span class="sxs-lookup"><span data-stu-id="e1331-176"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="e1331-177"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Unterstützende Entität in Error** (5)</span><span class="sxs-lookup"><span data-stu-id="e1331-177"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="e1331-178"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="e1331-178"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="e1331-179"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="e1331-179"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="e1331-180">)</span><span class="sxs-lookup"><span data-stu-id="e1331-180">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e1331-181">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="e1331-181">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1331-182">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e1331-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e1331-183">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e1331-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1331-184">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="e1331-184">A display name for the object.</span></span> <span data-ttu-id="e1331-185">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e1331-185">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e1331-186">**Enableddefault**</span><span class="sxs-lookup"><span data-stu-id="e1331-186">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1331-187">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e1331-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e1331-188">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e1331-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1331-189">Die Standard-oder Startkonfiguration eines Administrators für den aktivierten Zustand eines Elements.</span><span class="sxs-lookup"><span data-stu-id="e1331-189">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="e1331-190">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf 2 (aktiviert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e1331-190">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="e1331-191">Wert</span><span class="sxs-lookup"><span data-stu-id="e1331-191">Value</span></span>                                                                        | <span data-ttu-id="e1331-192">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e1331-192">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="e1331-193"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e1331-193"><dt>2</dt></span></span> </dl> | <span data-ttu-id="e1331-194">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="e1331-194">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e1331-195">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="e1331-195">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1331-196">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e1331-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e1331-197">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e1331-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1331-198">Der aktivierte und deaktivierte Status eines Elements.</span><span class="sxs-lookup"><span data-stu-id="e1331-198">The enabled and disabled states of an element.</span></span> <span data-ttu-id="e1331-199">Diese Eigenschaft kann auch die Übergänge zwischen diesen angeforderten Zuständen angeben.</span><span class="sxs-lookup"><span data-stu-id="e1331-199">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="e1331-200">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf 2 (aktiviert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e1331-200">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="e1331-201">Wert</span><span class="sxs-lookup"><span data-stu-id="e1331-201">Value</span></span>                                                                        | <span data-ttu-id="e1331-202">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e1331-202">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="e1331-203"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e1331-203"><dt>2</dt></span></span> </dl> | <span data-ttu-id="e1331-204">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="e1331-204">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e1331-205">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="e1331-205">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1331-206">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e1331-206">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e1331-207">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e1331-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1331-208">Der aktuelle Zustand des Elements.</span><span class="sxs-lookup"><span data-stu-id="e1331-208">The current health of the element.</span></span> <span data-ttu-id="e1331-209">Dieses Attribut drückt den Zustand dieses Elements aus, aber nicht notwendigerweise dessen unter Komponenten.</span><span class="sxs-lookup"><span data-stu-id="e1331-209">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="e1331-210">Mögliche Werte sind 0 bis 30, wobei 5 bedeutet, dass das Element vollständig fehlerfrei ist und 30 bedeutet, dass das Element vollständig nicht funktionsfähig ist.</span><span class="sxs-lookup"><span data-stu-id="e1331-210">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="e1331-211">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e1331-211">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e1331-212">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e1331-212">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1331-213">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="e1331-213">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e1331-214">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e1331-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1331-215">Das Datum und die Uhrzeit der Erstellung der Konfiguration der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="e1331-215">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="e1331-216">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e1331-216">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e1331-217">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e1331-217">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1331-218">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e1331-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e1331-219">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e1331-219">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e1331-220">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="e1331-220">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="e1331-221">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="e1331-221">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="e1331-222">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e1331-222">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e1331-223">**Name**</span><span class="sxs-lookup"><span data-stu-id="e1331-223">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1331-224">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e1331-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e1331-225">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e1331-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e1331-226">Qualifizierer: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="e1331-226">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="e1331-227">Die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="e1331-227">The label by which the object is known.</span></span> <span data-ttu-id="e1331-228">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e1331-228">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e1331-229">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="e1331-229">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1331-230">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e1331-230">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e1331-231">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e1331-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1331-232">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="e1331-232">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="e1331-233">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="e1331-233">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e1331-234">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e1331-234">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="e1331-235"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="e1331-235"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e1331-236"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="e1331-236"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e1331-237"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Wartung** (2)</span><span class="sxs-lookup"><span data-stu-id="e1331-237"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e1331-238"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>Wird **gestartet** (3)</span><span class="sxs-lookup"><span data-stu-id="e1331-238"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e1331-239"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>Wird **beendet (4** )</span><span class="sxs-lookup"><span data-stu-id="e1331-239"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="e1331-240"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Beendet** (5)</span><span class="sxs-lookup"><span data-stu-id="e1331-240"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="e1331-241"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abgebrochen** (6)</span><span class="sxs-lookup"><span data-stu-id="e1331-241"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="e1331-242"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Ruhende** (7)</span><span class="sxs-lookup"><span data-stu-id="e1331-242"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="e1331-243"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Abgeschlossen** (8)</span><span class="sxs-lookup"><span data-stu-id="e1331-243"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="e1331-244"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrieren** (9)</span><span class="sxs-lookup"><span data-stu-id="e1331-244"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="e1331-245"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Migration** (10)</span><span class="sxs-lookup"><span data-stu-id="e1331-245"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="e1331-246"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migration** (11)</span><span class="sxs-lookup"><span data-stu-id="e1331-246"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="e1331-247"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotts** (12)</span><span class="sxs-lookup"><span data-stu-id="e1331-247"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="e1331-248"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Herunter** fahren (13)</span><span class="sxs-lookup"><span data-stu-id="e1331-248"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="e1331-249"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span><span class="sxs-lookup"><span data-stu-id="e1331-249"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="e1331-250"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Übergang** (15)</span><span class="sxs-lookup"><span data-stu-id="e1331-250"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="e1331-251"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Dienst** (16)</span><span class="sxs-lookup"><span data-stu-id="e1331-251"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="e1331-252"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="e1331-252"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="e1331-253"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="e1331-253"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="e1331-254">)</span><span class="sxs-lookup"><span data-stu-id="e1331-254">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e1331-255">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="e1331-255">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1331-256">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="e1331-256">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e1331-257">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e1331-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1331-258">Die aktuellen Status des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="e1331-258">The current statuses of the object.</span></span> <span data-ttu-id="e1331-259">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e1331-259">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e1331-260">**Otherenabledstate**</span><span class="sxs-lookup"><span data-stu-id="e1331-260">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1331-261">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e1331-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e1331-262">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e1331-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1331-263">Eine Zeichenfolge, die den aktivierten oder deaktivierten Status des Elements beschreibt, wenn die **enabledstate** -Eigenschaft auf 1 ("Other") festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e1331-263">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="e1331-264">Diese Eigenschaft muss auf **null** festgelegt werden, wenn **enabledstate** ein anderer Wert als 1 ist.</span><span class="sxs-lookup"><span data-stu-id="e1331-264">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="e1331-265">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e1331-265">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e1331-266">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="e1331-266">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1331-267">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e1331-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e1331-268">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e1331-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e1331-269">Qualifizierer: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="e1331-269">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="e1331-270">Alle Informationen dazu, wie der primäre Besitzer des Dienstanbieter erreicht werden kann (z. b. Telefonnummer, e-Mail-Adresse usw.).</span><span class="sxs-lookup"><span data-stu-id="e1331-270">Any information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="e1331-271">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e1331-271">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e1331-272">**Primaryownername**</span><span class="sxs-lookup"><span data-stu-id="e1331-272">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1331-273">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e1331-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e1331-274">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e1331-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e1331-275">Qualifizierer: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="e1331-275">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="e1331-276">Der Name des primären Besitzers für den Dienst, sofern definiert.</span><span class="sxs-lookup"><span data-stu-id="e1331-276">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="e1331-277">Der primäre Besitzer ist der erste Support Kontakt für den Dienst.</span><span class="sxs-lookup"><span data-stu-id="e1331-277">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="e1331-278">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e1331-278">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e1331-279">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="e1331-279">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1331-280">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e1331-280">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e1331-281">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e1331-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1331-282">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="e1331-282">Provides high level status information.</span></span> <span data-ttu-id="e1331-283">Diese Eigenschaft sollte in Verbindung mit der Eigenschaft **detailedstatus** verwendet werden, um einen hohen und detaillierten Integritäts Status des Elements und seiner unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="e1331-283">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="e1331-284">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="e1331-284">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e1331-285">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e1331-285">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="e1331-286"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="e1331-286"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e1331-287"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="e1331-287"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e1331-288"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (2** )</span><span class="sxs-lookup"><span data-stu-id="e1331-288"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e1331-289"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Fehler** (3)</span><span class="sxs-lookup"><span data-stu-id="e1331-289"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e1331-290"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="e1331-290"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="e1331-291"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="e1331-291"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="e1331-292">)</span><span class="sxs-lookup"><span data-stu-id="e1331-292">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e1331-293">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="e1331-293">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1331-294">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e1331-294">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e1331-295">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e1331-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1331-296">Der zuletzt angeforderte oder gewünschte Zustand für das Element.</span><span class="sxs-lookup"><span data-stu-id="e1331-296">The last requested or desired state for the element.</span></span> <span data-ttu-id="e1331-297">Der tatsächliche Zustand des Elements wird durch **enabledstate** dargestellt.</span><span class="sxs-lookup"><span data-stu-id="e1331-297">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="e1331-298">Diese Eigenschaft wird bereitgestellt, um die zuletzt angeforderten und aktuellen Zustände für ein Element zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="e1331-298">This property is provided to compare the last requested and current states for an element.</span></span> <span data-ttu-id="e1331-299">Eine bestimmte Instanz der [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85)) -Klasse unterstützt die **requestedstate** -Eigenschaft möglicherweise nicht.</span><span class="sxs-lookup"><span data-stu-id="e1331-299">A particular instance of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) class might not support the **RequestedState** property.</span></span> <span data-ttu-id="e1331-300">Wenn dies auftritt, wird der Wert 12 ("nicht zutreffend") verwendet.</span><span class="sxs-lookup"><span data-stu-id="e1331-300">If this occurs, the value 12 ("Not Applicable") is used.</span></span> <span data-ttu-id="e1331-301">Diese Eigenschaft wird von **CIM \_ enabledlogicalelement** geerbt und ist immer auf 12 (nicht zutreffend) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e1331-301">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="e1331-302">Wert</span><span class="sxs-lookup"><span data-stu-id="e1331-302">Value</span></span>                                                                         | <span data-ttu-id="e1331-303">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e1331-303">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="e1331-304"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="e1331-304"><dt>12</dt></span></span> </dl> | <span data-ttu-id="e1331-305">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="e1331-305">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e1331-306">**Gestartet**</span><span class="sxs-lookup"><span data-stu-id="e1331-306">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1331-307">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="e1331-307">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e1331-308">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e1331-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1331-309">Gibt an, ob der Dienst gerade ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e1331-309">Indicates whether the service is currently running.</span></span> <span data-ttu-id="e1331-310">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e1331-310">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="e1331-311">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="e1331-311">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1331-312">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e1331-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e1331-313">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e1331-313">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e1331-314">Qualifizierer: **maxlen** (10)</span><span class="sxs-lookup"><span data-stu-id="e1331-314">Qualifiers: **MaxLen** ( 10 )</span></span>
</dt> </dl>

<span data-ttu-id="e1331-315">Ein Zeichen folgen Wert, der angibt, ob der Dienst automatisch von einem System oder einem Betriebssystem gestartet oder nur nach Anforderung gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="e1331-315">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="e1331-316">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e1331-316">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e1331-317">**Status**</span><span class="sxs-lookup"><span data-stu-id="e1331-317">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1331-318">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e1331-318">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e1331-319">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e1331-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1331-320">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="e1331-320">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e1331-321">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="e1331-321">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1331-322">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="e1331-322">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e1331-323">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e1331-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1331-324">Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="e1331-324">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="e1331-325">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e1331-325">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e1331-326">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="e1331-326">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1331-327">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e1331-327">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e1331-328">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e1331-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e1331-329">Qualifizierer: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="e1331-329">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="e1331-330">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="e1331-330">The scoping system's creation class name.</span></span> <span data-ttu-id="e1331-331">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e1331-331">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="e1331-332">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="e1331-332">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1331-333">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e1331-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e1331-334">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e1331-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e1331-335">Qualifizierer: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="e1331-335">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="e1331-336">Der NetBIOS-Name des hostingcomputersystems.</span><span class="sxs-lookup"><span data-stu-id="e1331-336">The NetBIOS name of the hosting computer system.</span></span> <span data-ttu-id="e1331-337">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e1331-337">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="e1331-338">**Timeoflaststatechange**</span><span class="sxs-lookup"><span data-stu-id="e1331-338">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1331-339">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="e1331-339">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e1331-340">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e1331-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1331-341">Das Datum oder die Uhrzeit, zu dem der aktivierte Status des Elements zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="e1331-341">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="e1331-342">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="e1331-342">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e1331-343">**Transitioningumstate**</span><span class="sxs-lookup"><span data-stu-id="e1331-343">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1331-344">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e1331-344">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e1331-345">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e1331-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1331-346">Gibt den Ziel Status an, in den die-Instanz übergeht.</span><span class="sxs-lookup"><span data-stu-id="e1331-346">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="e1331-347">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e1331-347">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e1331-348">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e1331-348">Requirements</span></span>



| <span data-ttu-id="e1331-349">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e1331-349">Requirement</span></span> | <span data-ttu-id="e1331-350">Wert</span><span class="sxs-lookup"><span data-stu-id="e1331-350">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1331-351">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e1331-351">Minimum supported client</span></span><br/> | <span data-ttu-id="e1331-352">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="e1331-352">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="e1331-353">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e1331-353">Minimum supported server</span></span><br/> | <span data-ttu-id="e1331-354">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e1331-354">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e1331-355">Namespace</span><span class="sxs-lookup"><span data-stu-id="e1331-355">Namespace</span></span><br/>                | <span data-ttu-id="e1331-356">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="e1331-356">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e1331-357">MOF</span><span class="sxs-lookup"><span data-stu-id="e1331-357">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e1331-358"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e1331-358"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e1331-359">DLL</span><span class="sxs-lookup"><span data-stu-id="e1331-359">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1331-360"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e1331-360"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

