---
description: Bietet die Möglichkeit zum Verwalten von Metriken.
ms.assetid: 39dee432-995d-472a-84c3-eede95dccb43
title: Msvm_MetricService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService
- Msvm_MetricService.InstanceID
- Msvm_MetricService.Caption
- Msvm_MetricService.Description
- Msvm_MetricService.ElementName
- Msvm_MetricService.InstallDate
- Msvm_MetricService.OperationalStatus
- Msvm_MetricService.StatusDescriptions
- Msvm_MetricService.Status
- Msvm_MetricService.HealthState
- Msvm_MetricService.CommunicationStatus
- Msvm_MetricService.DetailedStatus
- Msvm_MetricService.OperatingStatus
- Msvm_MetricService.PrimaryStatus
- Msvm_MetricService.EnabledState
- Msvm_MetricService.OtherEnabledState
- Msvm_MetricService.RequestedState
- Msvm_MetricService.EnabledDefault
- Msvm_MetricService.TimeOfLastStateChange
- Msvm_MetricService.AvailableRequestedStates
- Msvm_MetricService.TransitioningToState
- Msvm_MetricService.SystemCreationClassName
- Msvm_MetricService.SystemName
- Msvm_MetricService.Name
- Msvm_MetricService.CreationClassName
- Msvm_MetricService.PrimaryOwnerName
- Msvm_MetricService.PrimaryOwnerContact
- Msvm_MetricService.StartMode
- Msvm_MetricService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c4117e3adf3db5a2b0073615ae999b9f85bb9b18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351545"
---
# <a name="msvm_metricservice-class"></a><span data-ttu-id="0c660-103">MSVM- \_ metricservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="0c660-103">Msvm\_MetricService class</span></span>

<span data-ttu-id="0c660-104">Bietet die Möglichkeit zum Verwalten von Metriken.</span><span class="sxs-lookup"><span data-stu-id="0c660-104">Provides the ability to manage metrics.</span></span>

<span data-ttu-id="0c660-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0c660-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c660-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c660-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricService : CIM_MetricService
{
  string   InstanceID;
  string   Caption = "Hyper-V Metric Service";
  string   Description = "Provides Hyper-V Metric WMI management";
  string   ElementName = "Hyper-V Metric Service";
  datetime InstallDate;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = "OK";
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
  string   Name = "metricsvc";
  string   CreationClassName = "Msvm_MetricService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started;
};
```

## <a name="members"></a><span data-ttu-id="0c660-107">Member</span><span class="sxs-lookup"><span data-stu-id="0c660-107">Members</span></span>

<span data-ttu-id="0c660-108">Die **MSVM \_ metricservice** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0c660-108">The **Msvm\_MetricService** class has these types of members:</span></span>

-   [<span data-ttu-id="0c660-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="0c660-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="0c660-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0c660-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0c660-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="0c660-111">Methods</span></span>

<span data-ttu-id="0c660-112">Die **MSVM \_ metricservice** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="0c660-112">The **Msvm\_MetricService** class has these methods.</span></span>



| <span data-ttu-id="0c660-113">Methode</span><span class="sxs-lookup"><span data-stu-id="0c660-113">Method</span></span>                                                                    | <span data-ttu-id="0c660-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0c660-114">Description</span></span>                                                                             |
|:--------------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [<span data-ttu-id="0c660-115">**Controlmetrics**</span><span class="sxs-lookup"><span data-stu-id="0c660-115">**ControlMetrics**</span></span>](controlmetrics-msvm-metricservice.md)               | <span data-ttu-id="0c660-116">Wird verwendet, um die Sammlung von Metriken für ein verwaltetes Element oder Elemente zu steuern.</span><span class="sxs-lookup"><span data-stu-id="0c660-116">Used to control the collection of metrics for a managed element or elements.</span></span><br/> |
| [<span data-ttu-id="0c660-117">**Controlmetricsbyclass**</span><span class="sxs-lookup"><span data-stu-id="0c660-117">**ControlMetricsByClass**</span></span>](msvm-metricservice-controlmetricsbyclass.md) | <span data-ttu-id="0c660-118">Steuert die Metriken nach Klasse.</span><span class="sxs-lookup"><span data-stu-id="0c660-118">Controls the metrics by class.</span></span><br/>                                               |
| [<span data-ttu-id="0c660-119">**Controlsampletimes**</span><span class="sxs-lookup"><span data-stu-id="0c660-119">**ControlSampleTimes**</span></span>](msvm-metricservice-controlsampletimes.md)       | <span data-ttu-id="0c660-120">Legt die Beispiel Zeiten für das Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="0c660-120">Sets the control sample times.</span></span><br/>                                               |
| [<span data-ttu-id="0c660-121">**Getmetricvalues**</span><span class="sxs-lookup"><span data-stu-id="0c660-121">**GetMetricValues**</span></span>](msvm-metricservice-getmetricvalues.md)             | <span data-ttu-id="0c660-122">Ruft die Metrikwerte ab.</span><span class="sxs-lookup"><span data-stu-id="0c660-122">Retrieves the metric values.</span></span><br/>                                                 |
| [<span data-ttu-id="0c660-123">**Modifyservicesettings**</span><span class="sxs-lookup"><span data-stu-id="0c660-123">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-metricservice.md) | <span data-ttu-id="0c660-124">Ändert die Einstellungsdaten für den Dienst.</span><span class="sxs-lookup"><span data-stu-id="0c660-124">Modifies the setting data for the service.</span></span><br/>                                   |
| [<span data-ttu-id="0c660-125">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="0c660-125">**RequestStateChange**</span></span>](msvm-metricservice-requeststatechange.md)       | <span data-ttu-id="0c660-126">Fordert eine Statusänderung an.</span><span class="sxs-lookup"><span data-stu-id="0c660-126">Requests a state change.</span></span><br/>                                                     |
| [<span data-ttu-id="0c660-127">**Showmetrics**</span><span class="sxs-lookup"><span data-stu-id="0c660-127">**ShowMetrics**</span></span>](msvm-metricservice-showmetrics.md)                     | <span data-ttu-id="0c660-128">Zeigt die angegebenen Metriken an.</span><span class="sxs-lookup"><span data-stu-id="0c660-128">Shows the specified metrics.</span></span><br/>                                                 |
| [<span data-ttu-id="0c660-129">**Showmetricsbyclass**</span><span class="sxs-lookup"><span data-stu-id="0c660-129">**ShowMetricsByClass**</span></span>](msvm-metricservice-showmetricsbyclass.md)       | <span data-ttu-id="0c660-130">Zeigt die Metriken nach Klasse an.</span><span class="sxs-lookup"><span data-stu-id="0c660-130">Shows the metrics by class.</span></span><br/>                                                  |
| [<span data-ttu-id="0c660-131">**Start Service**</span><span class="sxs-lookup"><span data-stu-id="0c660-131">**StartService**</span></span>](msvm-metricservice-startservice.md)                   | <span data-ttu-id="0c660-132">Startet den Dienst.</span><span class="sxs-lookup"><span data-stu-id="0c660-132">Starts the service.</span></span><br/>                                                          |
| [<span data-ttu-id="0c660-133">**Stop Service**</span><span class="sxs-lookup"><span data-stu-id="0c660-133">**StopService**</span></span>](msvm-metricservice-stopservice.md)                     | <span data-ttu-id="0c660-134">Beendet den Dienst.</span><span class="sxs-lookup"><span data-stu-id="0c660-134">Stops the service.</span></span><br/>                                                           |



 

### <a name="properties"></a><span data-ttu-id="0c660-135">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0c660-135">Properties</span></span>

<span data-ttu-id="0c660-136">Die **MSVM \_ metricservice** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0c660-136">The **Msvm\_MetricService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0c660-137">**Availablerequestedstates**</span><span class="sxs-lookup"><span data-stu-id="0c660-137">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c660-138">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="0c660-138">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0c660-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0c660-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c660-140">Gibt die möglichen Werte für den *requestedstate* -Parameter der **requestStateChange** -Methode an.</span><span class="sxs-lookup"><span data-stu-id="0c660-140">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="0c660-141">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="0c660-141">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0c660-142">**Caption**</span><span class="sxs-lookup"><span data-stu-id="0c660-142">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c660-143">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0c660-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c660-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0c660-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c660-145">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="0c660-145">A short description of the object.</span></span> <span data-ttu-id="0c660-146">Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Hyper-V Metric Service" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0c660-146">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Metric Service".</span></span>

</dd> <dt>

<span data-ttu-id="0c660-147">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="0c660-147">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c660-148">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0c660-148">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0c660-149">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0c660-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c660-150">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="0c660-150">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="0c660-151">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="0c660-151">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0c660-152">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0c660-152">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="0c660-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="0c660-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0c660-154"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="0c660-154"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0c660-155"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Kommunikation OK** (2)</span><span class="sxs-lookup"><span data-stu-id="0c660-155"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0c660-156"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Verlorene Kommunikation** (3)</span><span class="sxs-lookup"><span data-stu-id="0c660-156"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0c660-157"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Kein Kontakt** (4)</span><span class="sxs-lookup"><span data-stu-id="0c660-157"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="0c660-158"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="0c660-158"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0c660-159"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="0c660-159"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="0c660-160">)</span><span class="sxs-lookup"><span data-stu-id="0c660-160">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0c660-161">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="0c660-161">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c660-162">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0c660-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c660-163">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0c660-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c660-164">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer-Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0c660-164">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="0c660-165">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt und ist immer auf "MSVM \_ metricservice" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0c660-165">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_MetricService".</span></span>

</dd> <dt>

<span data-ttu-id="0c660-166">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0c660-166">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c660-167">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0c660-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c660-168">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0c660-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c660-169">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="0c660-169">A description of the object.</span></span> <span data-ttu-id="0c660-170">Diese Eigenschaft wird vom [**CIM- \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "stellt die WMI-Verwaltung für Hyper-V-Metriken" fest.</span><span class="sxs-lookup"><span data-stu-id="0c660-170">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Provides Hyper-V Metric WMI management".</span></span>

</dd> <dt>

<span data-ttu-id="0c660-171">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="0c660-171">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c660-172">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0c660-172">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0c660-173">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0c660-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c660-174">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="0c660-174">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="0c660-175">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="0c660-175">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0c660-176">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0c660-176">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="0c660-177"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (0)</span><span class="sxs-lookup"><span data-stu-id="0c660-177"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0c660-178"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Keine zusätzlichen Informationen** (1)</span><span class="sxs-lookup"><span data-stu-id="0c660-178"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0c660-179"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Betont** (2)</span><span class="sxs-lookup"><span data-stu-id="0c660-179"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0c660-180"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Vorhersagefehler** (3)</span><span class="sxs-lookup"><span data-stu-id="0c660-180"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0c660-181"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Nicht BEHEB barer Fehler** (4)</span><span class="sxs-lookup"><span data-stu-id="0c660-181"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="0c660-182"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Unterstützende Entität in Error** (5)</span><span class="sxs-lookup"><span data-stu-id="0c660-182"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="0c660-183"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="0c660-183"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0c660-184"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="0c660-184"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="0c660-185">)</span><span class="sxs-lookup"><span data-stu-id="0c660-185">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0c660-186">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="0c660-186">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c660-187">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0c660-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c660-188">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0c660-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c660-189">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="0c660-189">A display name for the object.</span></span> <span data-ttu-id="0c660-190">Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Hyper-V Metric Service" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0c660-190">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Metric Service".</span></span>

</dd> <dt>

<span data-ttu-id="0c660-191">**Enableddefault**</span><span class="sxs-lookup"><span data-stu-id="0c660-191">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c660-192">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0c660-192">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0c660-193">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0c660-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c660-194">Die Standard-oder Startkonfiguration eines Administrators für den aktivierten Zustand eines Elements.</span><span class="sxs-lookup"><span data-stu-id="0c660-194">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="0c660-195">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf 2 (aktiviert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0c660-195">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="0c660-196">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="0c660-196">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c660-197">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0c660-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c660-198">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0c660-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c660-199">Der aktivierte und deaktivierte Status eines Elements.</span><span class="sxs-lookup"><span data-stu-id="0c660-199">The enabled and disabled states of an element.</span></span> <span data-ttu-id="0c660-200">Diese Eigenschaft kann auch die Übergänge zwischen diesen angeforderten Zuständen angeben.</span><span class="sxs-lookup"><span data-stu-id="0c660-200">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="0c660-201">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf 2 (aktiviert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0c660-201">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="0c660-202">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="0c660-202">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c660-203">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0c660-203">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0c660-204">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0c660-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c660-205">Der aktuelle Zustand des Elements.</span><span class="sxs-lookup"><span data-stu-id="0c660-205">The current health of the element.</span></span> <span data-ttu-id="0c660-206">Dieses Attribut drückt den Zustand dieses Elements aus, aber nicht notwendigerweise dessen unter Komponenten.</span><span class="sxs-lookup"><span data-stu-id="0c660-206">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="0c660-207">Mögliche Werte sind 0 bis 30, wobei 5 bedeutet, dass das Element vollständig fehlerfrei ist und 30 bedeutet, dass das Element vollständig nicht funktionsfähig ist.</span><span class="sxs-lookup"><span data-stu-id="0c660-207">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="0c660-208">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und ist immer auf 5 (OK) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0c660-208">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="0c660-209">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0c660-209">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c660-210">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="0c660-210">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0c660-211">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0c660-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c660-212">Das Datum und die Uhrzeit der Erstellung der Konfiguration der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="0c660-212">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="0c660-213">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0c660-213">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0c660-214">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0c660-214">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c660-215">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0c660-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c660-216">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0c660-216">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c660-217">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="0c660-217">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="0c660-218">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="0c660-218">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="0c660-219">Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0c660-219">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0c660-220">**Name**</span><span class="sxs-lookup"><span data-stu-id="0c660-220">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c660-221">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0c660-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c660-222">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0c660-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c660-223">Die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="0c660-223">The label by which the object is known.</span></span> <span data-ttu-id="0c660-224">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt und ist immer auf "metricsvc" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0c660-224">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "metricsvc".</span></span>

</dd> <dt>

<span data-ttu-id="0c660-225">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="0c660-225">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c660-226">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0c660-226">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0c660-227">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0c660-227">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c660-228">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="0c660-228">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="0c660-229">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="0c660-229">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0c660-230">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0c660-230">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="0c660-231"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="0c660-231"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0c660-232"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="0c660-232"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0c660-233"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Wartung** (2)</span><span class="sxs-lookup"><span data-stu-id="0c660-233"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0c660-234"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>Wird **gestartet** (3)</span><span class="sxs-lookup"><span data-stu-id="0c660-234"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0c660-235"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>Wird **beendet (4** )</span><span class="sxs-lookup"><span data-stu-id="0c660-235"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="0c660-236"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Beendet** (5)</span><span class="sxs-lookup"><span data-stu-id="0c660-236"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="0c660-237"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abgebrochen** (6)</span><span class="sxs-lookup"><span data-stu-id="0c660-237"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="0c660-238"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Ruhende** (7)</span><span class="sxs-lookup"><span data-stu-id="0c660-238"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="0c660-239"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Abgeschlossen** (8)</span><span class="sxs-lookup"><span data-stu-id="0c660-239"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="0c660-240"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrieren** (9)</span><span class="sxs-lookup"><span data-stu-id="0c660-240"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="0c660-241"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Migration** (10)</span><span class="sxs-lookup"><span data-stu-id="0c660-241"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="0c660-242"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migration** (11)</span><span class="sxs-lookup"><span data-stu-id="0c660-242"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="0c660-243"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotts** (12)</span><span class="sxs-lookup"><span data-stu-id="0c660-243"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="0c660-244"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Herunter** fahren (13)</span><span class="sxs-lookup"><span data-stu-id="0c660-244"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="0c660-245"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span><span class="sxs-lookup"><span data-stu-id="0c660-245"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="0c660-246"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Übergang** (15)</span><span class="sxs-lookup"><span data-stu-id="0c660-246"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="0c660-247"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Dienst** (16)</span><span class="sxs-lookup"><span data-stu-id="0c660-247"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="0c660-248"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="0c660-248"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0c660-249"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="0c660-249"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="0c660-250">)</span><span class="sxs-lookup"><span data-stu-id="0c660-250">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0c660-251">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="0c660-251">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c660-252">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="0c660-252">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0c660-253">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0c660-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c660-254">Die aktuellen Status des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="0c660-254">The current statuses of the object.</span></span> <span data-ttu-id="0c660-255">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, und jedes Array Element ist immer auf 2 (OK) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0c660-255">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="0c660-256">**Otherenabledstate**</span><span class="sxs-lookup"><span data-stu-id="0c660-256">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c660-257">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0c660-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c660-258">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0c660-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c660-259">Eine Zeichenfolge, die den aktivierten oder deaktivierten Status des Elements beschreibt, wenn die **enabledstate** -Eigenschaft auf 1 (Sonstiges) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="0c660-259">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="0c660-260">Diese Eigenschaft muss auf **null** festgelegt werden, wenn **enabledstate** ein anderer Wert als 1 ist.</span><span class="sxs-lookup"><span data-stu-id="0c660-260">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="0c660-261">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0c660-261">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0c660-262">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="0c660-262">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c660-263">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0c660-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c660-264">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0c660-264">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c660-265">Ein Wert, der Informationen darüber bereitstellt, wie der primäre Besitzer des Dienstanbieter erreicht werden kann (z. b. Telefonnummer, e-Mail-Adresse usw.).</span><span class="sxs-lookup"><span data-stu-id="0c660-265">A value that provides information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="0c660-266">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0c660-266">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0c660-267">**Primaryownername**</span><span class="sxs-lookup"><span data-stu-id="0c660-267">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c660-268">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0c660-268">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c660-269">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0c660-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c660-270">Der Name des primären Besitzers für den Dienst, sofern definiert.</span><span class="sxs-lookup"><span data-stu-id="0c660-270">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="0c660-271">Der primäre Besitzer ist der erste Support Kontakt für den Dienst.</span><span class="sxs-lookup"><span data-stu-id="0c660-271">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="0c660-272">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0c660-272">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0c660-273">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="0c660-273">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c660-274">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0c660-274">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0c660-275">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0c660-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c660-276">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="0c660-276">Provides high level status information.</span></span> <span data-ttu-id="0c660-277">Diese Eigenschaft sollte in Verbindung mit der Eigenschaft **detailedstatus** verwendet werden, um einen hohen und detaillierten Integritäts Status des Elements und seiner unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="0c660-277">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="0c660-278">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="0c660-278">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0c660-279">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0c660-279">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="0c660-280"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="0c660-280"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0c660-281"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="0c660-281"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0c660-282"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (2** )</span><span class="sxs-lookup"><span data-stu-id="0c660-282"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0c660-283"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Fehler** (3)</span><span class="sxs-lookup"><span data-stu-id="0c660-283"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0c660-284"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="0c660-284"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0c660-285"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="0c660-285"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="0c660-286">)</span><span class="sxs-lookup"><span data-stu-id="0c660-286">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0c660-287">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="0c660-287">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c660-288">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0c660-288">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0c660-289">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0c660-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c660-290">Der zuletzt angeforderte oder gewünschte Zustand für das Element.</span><span class="sxs-lookup"><span data-stu-id="0c660-290">The last requested or desired state for the element.</span></span> <span data-ttu-id="0c660-291">Der tatsächliche Zustand des Elements wird durch **enabledstate** dargestellt.</span><span class="sxs-lookup"><span data-stu-id="0c660-291">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="0c660-292">Diese Eigenschaft wird bereitgestellt, um die zuletzt angeforderten und aktuell aktivierten oder deaktivierten Zustände zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="0c660-292">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="0c660-293">Eine bestimmte Instanz von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85)) unterstützt möglicherweise nicht die **requestStateChange** -Methode.</span><span class="sxs-lookup"><span data-stu-id="0c660-293">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="0c660-294">Wenn dies auftritt, wird der Wert 12 (nicht zutreffend) verwendet.</span><span class="sxs-lookup"><span data-stu-id="0c660-294">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="0c660-295">Diese Eigenschaft wird von **CIM \_ enabledlogicalelement** geerbt und ist immer auf 12 (nicht zutreffend) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0c660-295">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="0c660-296">**Gestartet**</span><span class="sxs-lookup"><span data-stu-id="0c660-296">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c660-297">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="0c660-297">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0c660-298">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0c660-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c660-299">Gibt an, ob der Dienst gerade ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0c660-299">Indicates whether the service is currently running.</span></span> <span data-ttu-id="0c660-300">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0c660-300">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="0c660-301">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="0c660-301">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c660-302">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0c660-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c660-303">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0c660-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c660-304">Ein Zeichen folgen Wert, der angibt, ob der Dienst automatisch von einem System oder einem Betriebssystem gestartet oder nur nach Anforderung gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="0c660-304">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="0c660-305">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0c660-305">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0c660-306">**Status**</span><span class="sxs-lookup"><span data-stu-id="0c660-306">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c660-307">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0c660-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c660-308">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0c660-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c660-309">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und ist immer auf "OK" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0c660-309">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="0c660-310">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="0c660-310">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c660-311">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="0c660-311">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0c660-312">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0c660-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c660-313">Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="0c660-313">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="0c660-314">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, und die Zeichen folgen sind immer auf "OK" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0c660-314">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and the strings are always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="0c660-315">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="0c660-315">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c660-316">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0c660-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c660-317">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0c660-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c660-318">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="0c660-318">The scoping system's creation class name.</span></span> <span data-ttu-id="0c660-319">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt und ist immer auf "MSVM \_ Computersystem" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0c660-319">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="0c660-320">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="0c660-320">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c660-321">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0c660-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c660-322">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0c660-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c660-323">Der Name des hostingcomputersystems.</span><span class="sxs-lookup"><span data-stu-id="0c660-323">The name of the hosting computer system.</span></span> <span data-ttu-id="0c660-324">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0c660-324">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="0c660-325">**Timeoflaststatechange**</span><span class="sxs-lookup"><span data-stu-id="0c660-325">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c660-326">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="0c660-326">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0c660-327">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0c660-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c660-328">Das Datum oder die Uhrzeit, zu dem der aktivierte Status des Elements zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="0c660-328">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="0c660-329">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="0c660-329">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0c660-330">**Transitioningumstate**</span><span class="sxs-lookup"><span data-stu-id="0c660-330">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c660-331">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0c660-331">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0c660-332">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0c660-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c660-333">Gibt den Ziel Status an, in den die-Instanz übergeht.</span><span class="sxs-lookup"><span data-stu-id="0c660-333">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="0c660-334">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="0c660-334">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0c660-335">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0c660-335">Requirements</span></span>



| <span data-ttu-id="0c660-336">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0c660-336">Requirement</span></span> | <span data-ttu-id="0c660-337">Wert</span><span class="sxs-lookup"><span data-stu-id="0c660-337">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c660-338">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0c660-338">Minimum supported client</span></span><br/> | <span data-ttu-id="0c660-339">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0c660-339">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0c660-340">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0c660-340">Minimum supported server</span></span><br/> | <span data-ttu-id="0c660-341">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0c660-341">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0c660-342">Namespace</span><span class="sxs-lookup"><span data-stu-id="0c660-342">Namespace</span></span><br/>                | <span data-ttu-id="0c660-343">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="0c660-343">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0c660-344">MOF</span><span class="sxs-lookup"><span data-stu-id="0c660-344">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0c660-345"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0c660-345"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0c660-346">DLL</span><span class="sxs-lookup"><span data-stu-id="0c660-346">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c660-347"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0c660-347"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

