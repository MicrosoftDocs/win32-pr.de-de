---
description: Stellt den virtualisierungdienst dar, der auf einem einzelnen Host System vorhanden ist. MSVM \_ virtualethernetswitchmanagementservice wird verwendet, um die Definition, Änderung und Löschung von virtuellen Ethernet-Switches zu steuern.
ms.assetid: d29935d3-3a88-4186-97e9-b27c0c0d07d0
title: Msvm_VirtualEthernetSwitchManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService
- Msvm_VirtualEthernetSwitchManagementService.InstanceID
- Msvm_VirtualEthernetSwitchManagementService.Caption
- Msvm_VirtualEthernetSwitchManagementService.Description
- Msvm_VirtualEthernetSwitchManagementService.ElementName
- Msvm_VirtualEthernetSwitchManagementService.InstallDate
- Msvm_VirtualEthernetSwitchManagementService.Name
- Msvm_VirtualEthernetSwitchManagementService.OperationalStatus
- Msvm_VirtualEthernetSwitchManagementService.StatusDescriptions
- Msvm_VirtualEthernetSwitchManagementService.Status
- Msvm_VirtualEthernetSwitchManagementService.HealthState
- Msvm_VirtualEthernetSwitchManagementService.CommunicationStatus
- Msvm_VirtualEthernetSwitchManagementService.DetailedStatus
- Msvm_VirtualEthernetSwitchManagementService.OperatingStatus
- Msvm_VirtualEthernetSwitchManagementService.PrimaryStatus
- Msvm_VirtualEthernetSwitchManagementService.EnabledState
- Msvm_VirtualEthernetSwitchManagementService.OtherEnabledState
- Msvm_VirtualEthernetSwitchManagementService.RequestedState
- Msvm_VirtualEthernetSwitchManagementService.EnabledDefault
- Msvm_VirtualEthernetSwitchManagementService.TimeOfLastStateChange
- Msvm_VirtualEthernetSwitchManagementService.AvailableRequestedStates
- Msvm_VirtualEthernetSwitchManagementService.TransitioningToState
- Msvm_VirtualEthernetSwitchManagementService.SystemCreationClassName
- Msvm_VirtualEthernetSwitchManagementService.SystemName
- Msvm_VirtualEthernetSwitchManagementService.CreationClassName
- Msvm_VirtualEthernetSwitchManagementService.PrimaryOwnerName
- Msvm_VirtualEthernetSwitchManagementService.PrimaryOwnerContact
- Msvm_VirtualEthernetSwitchManagementService.StartMode
- Msvm_VirtualEthernetSwitchManagementService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1e6c1d4dee775dc6fabbb5fb3c96c987d1f6bda5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366341"
---
# <a name="msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="eeb96-104">MSVM \_ virtualethernetzwitchmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="eeb96-104">Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="eeb96-105">Stellt den virtualisierungdienst dar, der auf einem einzelnen Host System vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="eeb96-105">Represents the virtualization service present on a single host system.</span></span> <span data-ttu-id="eeb96-106">MSVM \_ virtualethernetswitchmanagementservice wird verwendet, um die Definition, Änderung und Löschung von virtuellen Ethernet-Switches zu steuern.</span><span class="sxs-lookup"><span data-stu-id="eeb96-106">Msvm\_VirtualEthernetSwitchManagementService is used to control the definition, modification, and deletion of virtual Ethernet switches.</span></span>

<span data-ttu-id="eeb96-107">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="eeb96-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="eeb96-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="eeb96-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualEthernetSwitchManagementService : CIM_VirtualSystemManagementService
{
  string   InstanceID;
  string   Caption = "Virtual Networking Management Service";
  string   Description = "Provides Hyper-V Networking WMI management";
  string   ElementName = "Hyper-V Networking Management Service";
  datetime InstallDate;
  string   Name = "nvspwmi";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status = { "OK" };
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
  string   CreationClassName = "Msvm_VirtualEthernetSwitchManagementService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started = True;
};
```

## <a name="members"></a><span data-ttu-id="eeb96-109">Member</span><span class="sxs-lookup"><span data-stu-id="eeb96-109">Members</span></span>

<span data-ttu-id="eeb96-110">Die **MSVM \_ virtualethernettwitchmanagementservice** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="eeb96-110">The **Msvm\_VirtualEthernetSwitchManagementService** class has these types of members:</span></span>

-   [<span data-ttu-id="eeb96-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="eeb96-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="eeb96-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="eeb96-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="eeb96-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="eeb96-113">Methods</span></span>

<span data-ttu-id="eeb96-114">Die **MSVM \_ virtualethernettwitchmanagementservice** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="eeb96-114">The **Msvm\_VirtualEthernetSwitchManagementService** class has these methods.</span></span>



| <span data-ttu-id="eeb96-115">Methode</span><span class="sxs-lookup"><span data-stu-id="eeb96-115">Method</span></span>                                                                                               | <span data-ttu-id="eeb96-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eeb96-116">Description</span></span>                                                                       |
|:-----------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [<span data-ttu-id="eeb96-117">**Addfeaturesettings**</span><span class="sxs-lookup"><span data-stu-id="eeb96-117">**AddFeatureSettings**</span></span>](addfeaturesettings-msvm-virtualethernetswitchmanagementservice.md)         | <span data-ttu-id="eeb96-118">Fügt der Konfiguration eines Ethernet-Switchports Funktionseinstellungen hinzu.</span><span class="sxs-lookup"><span data-stu-id="eeb96-118">Adds feature settings to the configuration of an Ethernet switch port.</span></span><br/> |
| [<span data-ttu-id="eeb96-119">**Adresssourcesettings**</span><span class="sxs-lookup"><span data-stu-id="eeb96-119">**AddResourceSettings**</span></span>](addresourcesettings-msvm-virtualethernetswitchmanagementservice.md)       | <span data-ttu-id="eeb96-120">Fügt einer Konfiguration des virtuellen Switches Ressourcen hinzu.</span><span class="sxs-lookup"><span data-stu-id="eeb96-120">Adds resources to a virtual switch configuration.</span></span><br/>                      |
| [<span data-ttu-id="eeb96-121">**Definesystem**</span><span class="sxs-lookup"><span data-stu-id="eeb96-121">**DefineSystem**</span></span>](definesystem-msvm-virtualethernetswitchmanagementservice.md)                     | <span data-ttu-id="eeb96-122">Erstellt einen neuen virtuellen Switch.</span><span class="sxs-lookup"><span data-stu-id="eeb96-122">Creates a new virtual switch.</span></span><br/>                                          |
| [<span data-ttu-id="eeb96-123">**Destroysystem**</span><span class="sxs-lookup"><span data-stu-id="eeb96-123">**DestroySystem**</span></span>](destroysystem-msvm-virtualethernetswitchmanagementservice.md)                   | <span data-ttu-id="eeb96-124">Zerstört einen virtuellen Switch.</span><span class="sxs-lookup"><span data-stu-id="eeb96-124">Destroys a virtual switch.</span></span><br/>                                             |
| [<span data-ttu-id="eeb96-125">**Modifyfeaturesettings**</span><span class="sxs-lookup"><span data-stu-id="eeb96-125">**ModifyFeatureSettings**</span></span>](modifyfeaturesettings-msvm-virtualethernetswitchmanagementservice.md)   | <span data-ttu-id="eeb96-126">Ändert die Funktionseinstellungen eines Ethernet-Switchports.</span><span class="sxs-lookup"><span data-stu-id="eeb96-126">Modifies the feature settings of an Ethernet switch port.</span></span><br/>              |
| [<span data-ttu-id="eeb96-127">**Modifyresourcesettings**</span><span class="sxs-lookup"><span data-stu-id="eeb96-127">**ModifyResourceSettings**</span></span>](modifyresourcesettings-msvm-virtualethernetswitchmanagementservice.md) | <span data-ttu-id="eeb96-128">Ändert die Ressourcen Einstellungen für einen virtuellen Switch.</span><span class="sxs-lookup"><span data-stu-id="eeb96-128">Modifies resource settings for a virtual switch.</span></span><br/>                       |
| [<span data-ttu-id="eeb96-129">**Modifysystemsettings**</span><span class="sxs-lookup"><span data-stu-id="eeb96-129">**ModifySystemSettings**</span></span>](modifysystemsettings-msvm-virtualethernetswitchmanagementservice.md)     | <span data-ttu-id="eeb96-130">Ändert Einstellungen für virtuelle Switches.</span><span class="sxs-lookup"><span data-stu-id="eeb96-130">Modifies virtual switch settings.</span></span><br/>                                      |
| [<span data-ttu-id="eeb96-131">**Removefeaturesettings**</span><span class="sxs-lookup"><span data-stu-id="eeb96-131">**RemoveFeatureSettings**</span></span>](removefeaturesettings-msvm-virtualethernetswitchmanagementservice.md)   | <span data-ttu-id="eeb96-132">Entfernt die Funktionseinstellungen von einem Ethernet-Switchport.</span><span class="sxs-lookup"><span data-stu-id="eeb96-132">Removes feature settings from an Ethernet switch port.</span></span><br/>                 |
| [<span data-ttu-id="eeb96-133">**Removeresourcesettings**</span><span class="sxs-lookup"><span data-stu-id="eeb96-133">**RemoveResourceSettings**</span></span>](removeresourcesettings-msvm-virtualethernetswitchmanagementservice.md) | <span data-ttu-id="eeb96-134">Entfernt die Einstellungen virtueller Ressourcen aus einer Konfiguration des virtuellen Switches.</span><span class="sxs-lookup"><span data-stu-id="eeb96-134">Removes virtual resource settings from a virtual switch configuration.</span></span><br/> |
| [<span data-ttu-id="eeb96-135">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="eeb96-135">**RequestStateChange**</span></span>](msvm-virtualethernetswitchmanagementservice-requeststatechange.md)         | <span data-ttu-id="eeb96-136">Fordert eine Statusänderung an.</span><span class="sxs-lookup"><span data-stu-id="eeb96-136">Requests a state change.</span></span><br/>                                               |
| [<span data-ttu-id="eeb96-137">**Start Service**</span><span class="sxs-lookup"><span data-stu-id="eeb96-137">**StartService**</span></span>](msvm-virtualethernetswitchmanagementservice-startservice.md)                     | <span data-ttu-id="eeb96-138">Startet den Dienst.</span><span class="sxs-lookup"><span data-stu-id="eeb96-138">Starts the service.</span></span><br/>                                                    |
| [<span data-ttu-id="eeb96-139">**Stop Service**</span><span class="sxs-lookup"><span data-stu-id="eeb96-139">**StopService**</span></span>](msvm-virtualethernetswitchmanagementservice-stopservice.md)                       | <span data-ttu-id="eeb96-140">Beendet den Dienst.</span><span class="sxs-lookup"><span data-stu-id="eeb96-140">Stops the service.</span></span><br/>                                                     |



 

### <a name="properties"></a><span data-ttu-id="eeb96-141">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="eeb96-141">Properties</span></span>

<span data-ttu-id="eeb96-142">Die **MSVM \_ virtualethernettwitchmanagementservice** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="eeb96-142">The **Msvm\_VirtualEthernetSwitchManagementService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="eeb96-143">**Availablerequestedstates**</span><span class="sxs-lookup"><span data-stu-id="eeb96-143">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eeb96-144">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="eeb96-144">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eeb96-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eeb96-146">Gibt die möglichen Werte für den *requestedstate* -Parameter der **requestStateChange** -Methode an.</span><span class="sxs-lookup"><span data-stu-id="eeb96-146">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="eeb96-147">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="eeb96-147">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="eeb96-148">**Caption**</span><span class="sxs-lookup"><span data-stu-id="eeb96-148">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eeb96-149">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eeb96-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eeb96-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eeb96-151">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="eeb96-151">A short description of the object.</span></span> <span data-ttu-id="eeb96-152">Diese Eigenschaft wird vom [**CIM \_ managedelta-Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Hyper-V-Verwaltungsdienst für virtuelle Netzwerke" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="eeb96-152">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Virtual Networking Management Service".</span></span>

</dd> <dt>

<span data-ttu-id="eeb96-153">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="eeb96-153">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eeb96-154">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eeb96-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-155">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eeb96-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eeb96-156">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="eeb96-156">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="eeb96-157">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="eeb96-157">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="eeb96-158">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="eeb96-158">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="eeb96-159"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="eeb96-159"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-160"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="eeb96-160"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-161"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Kommunikation OK** (2)</span><span class="sxs-lookup"><span data-stu-id="eeb96-161"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-162"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Verlorene Kommunikation** (3)</span><span class="sxs-lookup"><span data-stu-id="eeb96-162"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-163"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Kein Kontakt** (4)</span><span class="sxs-lookup"><span data-stu-id="eeb96-163"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-164"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="eeb96-164"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-165"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="eeb96-165"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="eeb96-166">)</span><span class="sxs-lookup"><span data-stu-id="eeb96-166">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="eeb96-167">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="eeb96-167">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eeb96-168">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eeb96-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-169">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eeb96-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-170">Qualifizierer: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="eeb96-170">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="eeb96-171">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer-Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="eeb96-171">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="eeb96-172">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt und ist immer auf "MSVM \_ virtualethernetzwitchmanagementservice" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="eeb96-172">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_VirtualEthernetSwitchManagementService".</span></span>

</dd> <dt>

<span data-ttu-id="eeb96-173">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="eeb96-173">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eeb96-174">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eeb96-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-175">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eeb96-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eeb96-176">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="eeb96-176">A description of the object.</span></span> <span data-ttu-id="eeb96-177">Diese Eigenschaft wird vom [**CIM- \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Bereitstellen der WMI-Verwaltung für Hyper-V-Netzwerke" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="eeb96-177">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Provides Hyper-V Networking WMI management".</span></span>

</dd> <dt>

<span data-ttu-id="eeb96-178">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="eeb96-178">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eeb96-179">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eeb96-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-180">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eeb96-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eeb96-181">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="eeb96-181">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="eeb96-182">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="eeb96-182">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="eeb96-183">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="eeb96-183">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="eeb96-184"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (0)</span><span class="sxs-lookup"><span data-stu-id="eeb96-184"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-185"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Keine zusätzlichen Informationen** (1)</span><span class="sxs-lookup"><span data-stu-id="eeb96-185"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-186"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Betont** (2)</span><span class="sxs-lookup"><span data-stu-id="eeb96-186"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-187"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Vorhersagefehler** (3)</span><span class="sxs-lookup"><span data-stu-id="eeb96-187"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-188"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Nicht BEHEB barer Fehler** (4)</span><span class="sxs-lookup"><span data-stu-id="eeb96-188"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-189"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Unterstützende Entität in Error** (5)</span><span class="sxs-lookup"><span data-stu-id="eeb96-189"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-190"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="eeb96-190"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-191"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="eeb96-191"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="eeb96-192">)</span><span class="sxs-lookup"><span data-stu-id="eeb96-192">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="eeb96-193">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="eeb96-193">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eeb96-194">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eeb96-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-195">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eeb96-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eeb96-196">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="eeb96-196">A display name for the object.</span></span> <span data-ttu-id="eeb96-197">Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Hyper-V-Netzwerk Verwaltungsdienst" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="eeb96-197">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Networking Management Service".</span></span>

</dd> <dt>

<span data-ttu-id="eeb96-198">**Enableddefault**</span><span class="sxs-lookup"><span data-stu-id="eeb96-198">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eeb96-199">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eeb96-199">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-200">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eeb96-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eeb96-201">Die Standard-oder Startkonfiguration eines Administrators für den aktivierten Zustand eines Elements.</span><span class="sxs-lookup"><span data-stu-id="eeb96-201">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="eeb96-202">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf 2 (aktiviert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="eeb96-202">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="eeb96-203">Wert</span><span class="sxs-lookup"><span data-stu-id="eeb96-203">Value</span></span>                                                                        | <span data-ttu-id="eeb96-204">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="eeb96-204">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="eeb96-205"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="eeb96-205"><dt>2</dt></span></span> </dl> | <span data-ttu-id="eeb96-206">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="eeb96-206">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="eeb96-207">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="eeb96-207">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eeb96-208">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eeb96-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-209">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eeb96-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eeb96-210">Der aktivierte und deaktivierte Status eines Elements.</span><span class="sxs-lookup"><span data-stu-id="eeb96-210">The enabled and disabled states of an element.</span></span> <span data-ttu-id="eeb96-211">Diese Eigenschaft kann auch die Übergänge zwischen diesen angeforderten Zuständen angeben.</span><span class="sxs-lookup"><span data-stu-id="eeb96-211">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="eeb96-212">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf 5 festgelegt (nicht zutreffend).</span><span class="sxs-lookup"><span data-stu-id="eeb96-212">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 5 (Not applicable).</span></span>

</dd> <dt>

<span data-ttu-id="eeb96-213">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="eeb96-213">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eeb96-214">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eeb96-214">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-215">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eeb96-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eeb96-216">Der aktuelle Zustand des Elements.</span><span class="sxs-lookup"><span data-stu-id="eeb96-216">The current health of the element.</span></span> <span data-ttu-id="eeb96-217">Dieses Attribut drückt den Zustand dieses Elements aus, aber nicht notwendigerweise dessen unter Komponenten.</span><span class="sxs-lookup"><span data-stu-id="eeb96-217">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="eeb96-218">Mögliche Werte sind 0 bis 30, wobei 5 bedeutet, dass das Element vollständig fehlerfrei ist und 30 bedeutet, dass das Element vollständig nicht funktionsfähig ist.</span><span class="sxs-lookup"><span data-stu-id="eeb96-218">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="eeb96-219">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und ist immer auf 5 (OK) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="eeb96-219">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>



| <span data-ttu-id="eeb96-220">Wert</span><span class="sxs-lookup"><span data-stu-id="eeb96-220">Value</span></span>                                                                        | <span data-ttu-id="eeb96-221">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="eeb96-221">Meaning</span></span>                                 |
|------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="eeb96-222"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="eeb96-222"><dt>5</dt></span></span> </dl> | <span data-ttu-id="eeb96-223">Der Integritäts Status ist "Normal".</span><span class="sxs-lookup"><span data-stu-id="eeb96-223">The health status is normal.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="eeb96-224">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="eeb96-224">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eeb96-225">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="eeb96-225">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-226">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eeb96-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eeb96-227">Das Datum und die Uhrzeit der Erstellung der Konfiguration der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="eeb96-227">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="eeb96-228">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="eeb96-228">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="eeb96-229">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="eeb96-229">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eeb96-230">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eeb96-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-231">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eeb96-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-232">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="eeb96-232">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="eeb96-233">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="eeb96-233">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="eeb96-234">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="eeb96-234">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="eeb96-235">**Name**</span><span class="sxs-lookup"><span data-stu-id="eeb96-235">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eeb96-236">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eeb96-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-237">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eeb96-237">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-238">Qualifizierer: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="eeb96-238">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="eeb96-239">Die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="eeb96-239">The label by which the object is known.</span></span> <span data-ttu-id="eeb96-240">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und ist immer auf "VMMS" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="eeb96-240">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "vmms".</span></span>

</dd> <dt>

<span data-ttu-id="eeb96-241">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="eeb96-241">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eeb96-242">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eeb96-242">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-243">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eeb96-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eeb96-244">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="eeb96-244">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="eeb96-245">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="eeb96-245">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="eeb96-246">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="eeb96-246">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="eeb96-247"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="eeb96-247"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-248"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="eeb96-248"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-249"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Wartung** (2)</span><span class="sxs-lookup"><span data-stu-id="eeb96-249"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-250"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>Wird **gestartet** (3)</span><span class="sxs-lookup"><span data-stu-id="eeb96-250"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-251"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>Wird **beendet (4** )</span><span class="sxs-lookup"><span data-stu-id="eeb96-251"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-252"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Beendet** (5)</span><span class="sxs-lookup"><span data-stu-id="eeb96-252"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-253"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abgebrochen** (6)</span><span class="sxs-lookup"><span data-stu-id="eeb96-253"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-254"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Ruhende** (7)</span><span class="sxs-lookup"><span data-stu-id="eeb96-254"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-255"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Abgeschlossen** (8)</span><span class="sxs-lookup"><span data-stu-id="eeb96-255"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-256"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrieren** (9)</span><span class="sxs-lookup"><span data-stu-id="eeb96-256"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-257"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Migration** (10)</span><span class="sxs-lookup"><span data-stu-id="eeb96-257"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-258"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migration** (11)</span><span class="sxs-lookup"><span data-stu-id="eeb96-258"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-259"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotts** (12)</span><span class="sxs-lookup"><span data-stu-id="eeb96-259"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-260"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Herunter** fahren (13)</span><span class="sxs-lookup"><span data-stu-id="eeb96-260"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-261"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span><span class="sxs-lookup"><span data-stu-id="eeb96-261"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-262"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Übergang** (15)</span><span class="sxs-lookup"><span data-stu-id="eeb96-262"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-263"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Dienst** (16)</span><span class="sxs-lookup"><span data-stu-id="eeb96-263"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-264"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="eeb96-264"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-265"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="eeb96-265"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="eeb96-266">)</span><span class="sxs-lookup"><span data-stu-id="eeb96-266">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="eeb96-267">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="eeb96-267">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eeb96-268">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="eeb96-268">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-269">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eeb96-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eeb96-270">Die aktuellen Status des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="eeb96-270">The current statuses of the object.</span></span> <span data-ttu-id="eeb96-271">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, und jedes Array Element ist immer auf 2 (OK) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="eeb96-271">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="eeb96-272">**Otherenabledstate**</span><span class="sxs-lookup"><span data-stu-id="eeb96-272">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eeb96-273">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eeb96-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-274">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eeb96-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eeb96-275">Eine Zeichenfolge, die den aktivierten oder deaktivierten Status des Elements beschreibt, wenn die **enabledstate** -Eigenschaft auf 1 ("Other") festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="eeb96-275">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="eeb96-276">Diese Eigenschaft muss auf **null** festgelegt werden, wenn **enabledstate** ein anderer Wert als 1 ist.</span><span class="sxs-lookup"><span data-stu-id="eeb96-276">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="eeb96-277">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="eeb96-277">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="eeb96-278">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="eeb96-278">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eeb96-279">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eeb96-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-280">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eeb96-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-281">Qualifizierer: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="eeb96-281">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="eeb96-282">Alle Informationen dazu, wie der primäre Besitzer des Dienstanbieter erreicht werden kann (z. b. Telefonnummer, e-Mail-Adresse usw.).</span><span class="sxs-lookup"><span data-stu-id="eeb96-282">Any information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="eeb96-283">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="eeb96-283">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="eeb96-284">**Primaryownername**</span><span class="sxs-lookup"><span data-stu-id="eeb96-284">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eeb96-285">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eeb96-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-286">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eeb96-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-287">Qualifizierer: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="eeb96-287">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="eeb96-288">Der Name des primären Besitzers für den Dienst, sofern definiert.</span><span class="sxs-lookup"><span data-stu-id="eeb96-288">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="eeb96-289">Der primäre Besitzer ist der erste Support Kontakt für den Dienst.</span><span class="sxs-lookup"><span data-stu-id="eeb96-289">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="eeb96-290">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="eeb96-290">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="eeb96-291">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="eeb96-291">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eeb96-292">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eeb96-292">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-293">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eeb96-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eeb96-294">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="eeb96-294">Provides high level status information.</span></span> <span data-ttu-id="eeb96-295">Diese Eigenschaft sollte in Verbindung mit der Eigenschaft **detailedstatus** verwendet werden, um einen hohen und detaillierten Integritäts Status des Elements und seiner unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="eeb96-295">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="eeb96-296">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="eeb96-296">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="eeb96-297">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="eeb96-297">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="eeb96-298"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="eeb96-298"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-299"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="eeb96-299"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-300"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (2** )</span><span class="sxs-lookup"><span data-stu-id="eeb96-300"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-301"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Fehler** (3)</span><span class="sxs-lookup"><span data-stu-id="eeb96-301"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-302"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="eeb96-302"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-303"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="eeb96-303"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="eeb96-304">)</span><span class="sxs-lookup"><span data-stu-id="eeb96-304">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="eeb96-305">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="eeb96-305">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eeb96-306">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eeb96-306">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-307">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eeb96-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eeb96-308">Der zuletzt angeforderte oder gewünschte Zustand für das Element.</span><span class="sxs-lookup"><span data-stu-id="eeb96-308">The last requested or desired state for the element.</span></span> <span data-ttu-id="eeb96-309">Der tatsächliche Zustand des Elements wird durch **enabledstate** dargestellt.</span><span class="sxs-lookup"><span data-stu-id="eeb96-309">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="eeb96-310">Diese Eigenschaft wird bereitgestellt, um die zuletzt angeforderten und aktuellen Zustände für ein Element zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="eeb96-310">This property is provided to compare the last requested and current states for an element.</span></span> <span data-ttu-id="eeb96-311">Eine bestimmte Instanz der [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85)) -Klasse unterstützt die **requestedstate** -Eigenschaft möglicherweise nicht.</span><span class="sxs-lookup"><span data-stu-id="eeb96-311">A particular instance of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) class might not support the **RequestedState** property.</span></span> <span data-ttu-id="eeb96-312">Wenn dies auftritt, wird der Wert 12 ("nicht zutreffend") verwendet.</span><span class="sxs-lookup"><span data-stu-id="eeb96-312">If this occurs, the value 12 ("Not Applicable") is used.</span></span> <span data-ttu-id="eeb96-313">Diese Eigenschaft wird von **CIM \_ enabledlogicalelement** geerbt und ist immer auf 12 (nicht zutreffend) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="eeb96-313">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="eeb96-314">Wert</span><span class="sxs-lookup"><span data-stu-id="eeb96-314">Value</span></span>                                                                         | <span data-ttu-id="eeb96-315">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="eeb96-315">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="eeb96-316"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="eeb96-316"><dt>12</dt></span></span> </dl> | <span data-ttu-id="eeb96-317">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="eeb96-317">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="eeb96-318">**Gestartet**</span><span class="sxs-lookup"><span data-stu-id="eeb96-318">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eeb96-319">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="eeb96-319">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-320">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eeb96-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eeb96-321">Gibt an, ob der Dienst gerade ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="eeb96-321">Indicates whether the service is currently running.</span></span> <span data-ttu-id="eeb96-322">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt und ist immer auf " **true**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="eeb96-322">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="eeb96-323">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="eeb96-323">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eeb96-324">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eeb96-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-325">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eeb96-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-326">Qualifizierer: **maxlen** (10)</span><span class="sxs-lookup"><span data-stu-id="eeb96-326">Qualifiers: **MaxLen** ( 10 )</span></span>
</dt> </dl>

<span data-ttu-id="eeb96-327">Ein Zeichen folgen Wert, der angibt, ob der Dienst automatisch von einem System oder einem Betriebssystem gestartet oder nur nach Anforderung gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="eeb96-327">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="eeb96-328">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="eeb96-328">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="eeb96-329">**Status**</span><span class="sxs-lookup"><span data-stu-id="eeb96-329">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eeb96-330">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eeb96-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-331">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eeb96-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eeb96-332">Beschreibt den aktuellen Status des Diensts.</span><span class="sxs-lookup"><span data-stu-id="eeb96-332">Describes the current status of the service.</span></span> <span data-ttu-id="eeb96-333">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und ist immer auf "OK" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="eeb96-333">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="eeb96-334">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="eeb96-334">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eeb96-335">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="eeb96-335">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-336">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eeb96-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eeb96-337">Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="eeb96-337">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="eeb96-338">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, und jedes Array Element ist immer auf "OK" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="eeb96-338">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="eeb96-339">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="eeb96-339">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eeb96-340">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eeb96-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-341">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eeb96-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-342">Qualifizierer: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="eeb96-342">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="eeb96-343">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="eeb96-343">The scoping system's creation class name.</span></span> <span data-ttu-id="eeb96-344">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt und ist immer auf "MSVM \_ Computersystem" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="eeb96-344">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="eeb96-345">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="eeb96-345">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eeb96-346">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eeb96-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-347">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eeb96-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-348">Qualifizierer: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="eeb96-348">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="eeb96-349">Der NetBIOS-Name des hostingcomputersystems.</span><span class="sxs-lookup"><span data-stu-id="eeb96-349">The NetBIOS name of the hosting computer system.</span></span> <span data-ttu-id="eeb96-350">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.</span><span class="sxs-lookup"><span data-stu-id="eeb96-350">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="eeb96-351">**Timeoflaststatechange**</span><span class="sxs-lookup"><span data-stu-id="eeb96-351">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eeb96-352">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="eeb96-352">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-353">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eeb96-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eeb96-354">Das Datum oder die Uhrzeit, zu dem der aktivierte Status des Elements zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="eeb96-354">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="eeb96-355">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="eeb96-355">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="eeb96-356">**Transitioningumstate**</span><span class="sxs-lookup"><span data-stu-id="eeb96-356">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eeb96-357">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eeb96-357">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eeb96-358">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eeb96-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eeb96-359">Gibt den Ziel Status an, in den die-Instanz übergeht.</span><span class="sxs-lookup"><span data-stu-id="eeb96-359">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="eeb96-360">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="eeb96-360">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="eeb96-361">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eeb96-361">Requirements</span></span>



| <span data-ttu-id="eeb96-362">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eeb96-362">Requirement</span></span> | <span data-ttu-id="eeb96-363">Wert</span><span class="sxs-lookup"><span data-stu-id="eeb96-363">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eeb96-364">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eeb96-364">Minimum supported client</span></span><br/> | <span data-ttu-id="eeb96-365">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eeb96-365">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="eeb96-366">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eeb96-366">Minimum supported server</span></span><br/> | <span data-ttu-id="eeb96-367">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eeb96-367">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="eeb96-368">Namespace</span><span class="sxs-lookup"><span data-stu-id="eeb96-368">Namespace</span></span><br/>                | <span data-ttu-id="eeb96-369">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="eeb96-369">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="eeb96-370">MOF</span><span class="sxs-lookup"><span data-stu-id="eeb96-370">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eeb96-371"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="eeb96-371"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="eeb96-372">DLL</span><span class="sxs-lookup"><span data-stu-id="eeb96-372">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eeb96-373"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="eeb96-373"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

