---
description: Gibt den Status einer aktiven Remote Sitzung an, die mit einer virtuellen Maschine interagiert.
ms.assetid: EAE6082F-A0CB-4E75-8029-51E20649C0A8
title: Msvm_TerminalConnection-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalConnection
- Msvm_TerminalConnection.InstanceID
- Msvm_TerminalConnection.Caption
- Msvm_TerminalConnection.Description
- Msvm_TerminalConnection.ElementName
- Msvm_TerminalConnection.InstallDate
- Msvm_TerminalConnection.Name
- Msvm_TerminalConnection.OperationalStatus
- Msvm_TerminalConnection.StatusDescriptions
- Msvm_TerminalConnection.Status
- Msvm_TerminalConnection.HealthState
- Msvm_TerminalConnection.CommunicationStatus
- Msvm_TerminalConnection.DetailedStatus
- Msvm_TerminalConnection.OperatingStatus
- Msvm_TerminalConnection.PrimaryStatus
- Msvm_TerminalConnection.EnabledState
- Msvm_TerminalConnection.OtherEnabledState
- Msvm_TerminalConnection.RequestedState
- Msvm_TerminalConnection.EnabledDefault
- Msvm_TerminalConnection.TimeOfLastStateChange
- Msvm_TerminalConnection.AvailableRequestedStates
- Msvm_TerminalConnection.TransitioningToState
- Msvm_TerminalConnection.ConnectionID
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 66be5000fb7fdd4404e07c87673e3359065af6bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759054"
---
# <a name="msvm_terminalconnection-class"></a><span data-ttu-id="0afec-103">MSVM \_ terminalconnection-Klasse</span><span class="sxs-lookup"><span data-stu-id="0afec-103">Msvm\_TerminalConnection class</span></span>

<span data-ttu-id="0afec-104">Gibt den Status einer aktiven Remote Sitzung an, die mit einer virtuellen Maschine interagiert.</span><span class="sxs-lookup"><span data-stu-id="0afec-104">Indicates the state of an active remote session interacting with a virtual machine.</span></span> <span data-ttu-id="0afec-105">Es kann jeweils nur eine Verbindung vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="0afec-105">There can only be one connection at a time.</span></span>

<span data-ttu-id="0afec-106">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0afec-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0afec-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0afec-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TerminalConnection : CIM_EnabledLogicalElement
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
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
  uint16   TransitioningToState = 12;
  string   ConnectionID;
};
```

## <a name="members"></a><span data-ttu-id="0afec-108">Member</span><span class="sxs-lookup"><span data-stu-id="0afec-108">Members</span></span>

<span data-ttu-id="0afec-109">Die **MSVM \_ terminalconnection** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0afec-109">The **Msvm\_TerminalConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="0afec-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="0afec-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="0afec-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0afec-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0afec-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="0afec-112">Methods</span></span>

<span data-ttu-id="0afec-113">Die **MSVM \_ terminalconnection** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="0afec-113">The **Msvm\_TerminalConnection** class has these methods.</span></span>



| <span data-ttu-id="0afec-114">Methode</span><span class="sxs-lookup"><span data-stu-id="0afec-114">Method</span></span>                                                                   | <span data-ttu-id="0afec-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0afec-115">Description</span></span>                         |
|:-------------------------------------------------------------------------|:------------------------------------|
| [<span data-ttu-id="0afec-116">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="0afec-116">**RequestStateChange**</span></span>](msvm-terminalconnection-requeststatechange.md) | <span data-ttu-id="0afec-117">Fordert eine Statusänderung an.</span><span class="sxs-lookup"><span data-stu-id="0afec-117">Requests a state change.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="0afec-118">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0afec-118">Properties</span></span>

<span data-ttu-id="0afec-119">Die **MSVM \_ terminalconnection** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0afec-119">The **Msvm\_TerminalConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0afec-120">**Availablerequestedstates**</span><span class="sxs-lookup"><span data-stu-id="0afec-120">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0afec-121">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="0afec-121">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0afec-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0afec-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0afec-123">Gibt die möglichen Werte für den *requestedstate* -Parameter der **requestStateChange** -Methode an.</span><span class="sxs-lookup"><span data-stu-id="0afec-123">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="0afec-124">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0afec-124">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0afec-125">**Caption**</span><span class="sxs-lookup"><span data-stu-id="0afec-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0afec-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0afec-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0afec-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0afec-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0afec-128">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="0afec-128">A short description of the object.</span></span> <span data-ttu-id="0afec-129">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0afec-129">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0afec-130">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="0afec-130">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0afec-131">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0afec-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0afec-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0afec-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0afec-133">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="0afec-133">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="0afec-134">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="0afec-134">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0afec-135">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0afec-135">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="0afec-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="0afec-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0afec-137"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="0afec-137"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0afec-138"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Kommunikation OK** (2)</span><span class="sxs-lookup"><span data-stu-id="0afec-138"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0afec-139"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Verlorene Kommunikation** (3)</span><span class="sxs-lookup"><span data-stu-id="0afec-139"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0afec-140"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Kein Kontakt** (4)</span><span class="sxs-lookup"><span data-stu-id="0afec-140"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="0afec-141"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="0afec-141"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0afec-142"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="0afec-142"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="0afec-143">)</span><span class="sxs-lookup"><span data-stu-id="0afec-143">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0afec-144">**ConnectionID**</span><span class="sxs-lookup"><span data-stu-id="0afec-144">**ConnectionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0afec-145">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0afec-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0afec-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0afec-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0afec-147">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0afec-147">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0afec-148">Der eindeutige Bezeichner für eine Instanz des Terminal Verbindungs Objekts.</span><span class="sxs-lookup"><span data-stu-id="0afec-148">The unique identifier for an instance of the terminal connection object.</span></span> <span data-ttu-id="0afec-149">Der Bezeichner hat das Format "Microsoft:*VMID* \\ *Index*".</span><span class="sxs-lookup"><span data-stu-id="0afec-149">The identifier is of the form "Microsoft:*VMID*\\*Index*".</span></span> <span data-ttu-id="0afec-150">Beispiel: "Microsoft: 67a5d397-a02d-11dB-AC13-001676aa34f 0 \\ ".</span><span class="sxs-lookup"><span data-stu-id="0afec-150">For example, "Microsoft:67A5D397-A02D-11DB-AC13-001676AA34F0\\0".</span></span>

</dd> <dt>

<span data-ttu-id="0afec-151">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0afec-151">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0afec-152">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0afec-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0afec-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0afec-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0afec-154">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="0afec-154">A description of the object.</span></span> <span data-ttu-id="0afec-155">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0afec-155">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0afec-156">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="0afec-156">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0afec-157">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0afec-157">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0afec-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0afec-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0afec-159">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="0afec-159">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="0afec-160">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="0afec-160">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0afec-161">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0afec-161">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="0afec-162"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (0)</span><span class="sxs-lookup"><span data-stu-id="0afec-162"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0afec-163"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Keine zusätzlichen Informationen** (1)</span><span class="sxs-lookup"><span data-stu-id="0afec-163"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0afec-164"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Betont** (2)</span><span class="sxs-lookup"><span data-stu-id="0afec-164"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0afec-165"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Vorhersagefehler** (3)</span><span class="sxs-lookup"><span data-stu-id="0afec-165"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0afec-166"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Nicht BEHEB barer Fehler** (4)</span><span class="sxs-lookup"><span data-stu-id="0afec-166"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="0afec-167"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Unterstützende Entität in Error** (5)</span><span class="sxs-lookup"><span data-stu-id="0afec-167"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="0afec-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="0afec-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0afec-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="0afec-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="0afec-170">)</span><span class="sxs-lookup"><span data-stu-id="0afec-170">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0afec-171">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="0afec-171">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0afec-172">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0afec-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0afec-173">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0afec-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0afec-174">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="0afec-174">A display name for the object.</span></span> <span data-ttu-id="0afec-175">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0afec-175">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0afec-176">**Enableddefault**</span><span class="sxs-lookup"><span data-stu-id="0afec-176">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0afec-177">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0afec-177">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0afec-178">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0afec-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0afec-179">Die Standard-oder Startkonfiguration eines Administrators für den aktivierten Zustand eines Elements.</span><span class="sxs-lookup"><span data-stu-id="0afec-179">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="0afec-180">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="0afec-180">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="0afec-181">Wert</span><span class="sxs-lookup"><span data-stu-id="0afec-181">Value</span></span>                                                                        | <span data-ttu-id="0afec-182">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0afec-182">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="0afec-183"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="0afec-183"><dt>2</dt></span></span> </dl> | <span data-ttu-id="0afec-184">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="0afec-184">Enabled</span></span><br/>  |
| <dl> <span data-ttu-id="0afec-185"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="0afec-185"><dt>3</dt></span></span> </dl> | <span data-ttu-id="0afec-186">Disabled</span><span class="sxs-lookup"><span data-stu-id="0afec-186">Disabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0afec-187">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="0afec-187">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0afec-188">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0afec-188">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0afec-189">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0afec-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0afec-190">Der aktivierte und deaktivierte Status eines Elements.</span><span class="sxs-lookup"><span data-stu-id="0afec-190">The enabled and disabled states of an element.</span></span> <span data-ttu-id="0afec-191">Sie kann auch die Übergänge zwischen diesen angeforderten Zuständen angeben.</span><span class="sxs-lookup"><span data-stu-id="0afec-191">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="0afec-192">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="0afec-192">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="0afec-193">Wert</span><span class="sxs-lookup"><span data-stu-id="0afec-193">Value</span></span>                                                                        | <span data-ttu-id="0afec-194">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0afec-194">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="0afec-195"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="0afec-195"><dt>2</dt></span></span> </dl> | <span data-ttu-id="0afec-196">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="0afec-196">Enabled</span></span><br/>        |
| <dl> <span data-ttu-id="0afec-197"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="0afec-197"><dt>3</dt></span></span> </dl> | <span data-ttu-id="0afec-198">Disabled</span><span class="sxs-lookup"><span data-stu-id="0afec-198">Disabled</span></span><br/>       |
| <dl> <span data-ttu-id="0afec-199"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="0afec-199"><dt>5</dt></span></span> </dl> | <span data-ttu-id="0afec-200">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="0afec-200">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0afec-201">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="0afec-201">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0afec-202">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0afec-202">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0afec-203">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0afec-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0afec-204">Der aktuelle Zustand des Elements.</span><span class="sxs-lookup"><span data-stu-id="0afec-204">The current health of the element.</span></span> <span data-ttu-id="0afec-205">Dieses Attribut drückt den Zustand dieses Elements aus, aber nicht notwendigerweise dessen unter Komponenten.</span><span class="sxs-lookup"><span data-stu-id="0afec-205">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="0afec-206">Mögliche Werte sind 0 bis 30, wobei 5 bedeutet, dass das Element vollständig fehlerfrei ist und 30 bedeutet, dass das Element vollständig nicht funktionsfähig ist.</span><span class="sxs-lookup"><span data-stu-id="0afec-206">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="0afec-207">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und ist immer auf 5 (OK) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0afec-207">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="0afec-208">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0afec-208">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0afec-209">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="0afec-209">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0afec-210">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0afec-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0afec-211">Das Datum und die Uhrzeit der Erstellung der Konfiguration der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="0afec-211">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="0afec-212">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0afec-212">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0afec-213">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0afec-213">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0afec-214">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0afec-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0afec-215">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0afec-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0afec-216">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="0afec-216">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="0afec-217">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="0afec-217">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="0afec-218">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0afec-218">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0afec-219">**Name**</span><span class="sxs-lookup"><span data-stu-id="0afec-219">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0afec-220">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0afec-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0afec-221">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0afec-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0afec-222">Die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="0afec-222">The label by which the object is known.</span></span> <span data-ttu-id="0afec-223">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und entspricht der Element **Name** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="0afec-223">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="0afec-224">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="0afec-224">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0afec-225">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0afec-225">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0afec-226">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0afec-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0afec-227">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="0afec-227">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="0afec-228">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="0afec-228">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0afec-229">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0afec-229">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="0afec-230"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="0afec-230"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0afec-231"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="0afec-231"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0afec-232"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Wartung** (2)</span><span class="sxs-lookup"><span data-stu-id="0afec-232"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0afec-233"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>Wird **gestartet** (3)</span><span class="sxs-lookup"><span data-stu-id="0afec-233"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0afec-234"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>Wird **beendet (4** )</span><span class="sxs-lookup"><span data-stu-id="0afec-234"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="0afec-235"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Beendet** (5)</span><span class="sxs-lookup"><span data-stu-id="0afec-235"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="0afec-236"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abgebrochen** (6)</span><span class="sxs-lookup"><span data-stu-id="0afec-236"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="0afec-237"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Ruhende** (7)</span><span class="sxs-lookup"><span data-stu-id="0afec-237"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="0afec-238"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Abgeschlossen** (8)</span><span class="sxs-lookup"><span data-stu-id="0afec-238"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="0afec-239"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrieren** (9)</span><span class="sxs-lookup"><span data-stu-id="0afec-239"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="0afec-240"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Migration** (10)</span><span class="sxs-lookup"><span data-stu-id="0afec-240"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="0afec-241"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migration** (11)</span><span class="sxs-lookup"><span data-stu-id="0afec-241"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="0afec-242"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotts** (12)</span><span class="sxs-lookup"><span data-stu-id="0afec-242"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="0afec-243"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Herunter** fahren (13)</span><span class="sxs-lookup"><span data-stu-id="0afec-243"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="0afec-244"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span><span class="sxs-lookup"><span data-stu-id="0afec-244"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="0afec-245"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Übergang** (15)</span><span class="sxs-lookup"><span data-stu-id="0afec-245"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="0afec-246"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Dienst** (16)</span><span class="sxs-lookup"><span data-stu-id="0afec-246"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="0afec-247"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="0afec-247"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0afec-248"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="0afec-248"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="0afec-249">)</span><span class="sxs-lookup"><span data-stu-id="0afec-249">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0afec-250">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="0afec-250">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0afec-251">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="0afec-251">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0afec-252">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0afec-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0afec-253">Die aktuellen Status des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="0afec-253">The current statuses of the object.</span></span> <span data-ttu-id="0afec-254">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0afec-254">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0afec-255">**Otherenabledstate**</span><span class="sxs-lookup"><span data-stu-id="0afec-255">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0afec-256">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0afec-256">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0afec-257">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0afec-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0afec-258">Eine Zeichenfolge, die den aktivierten oder deaktivierten Status des Elements beschreibt, wenn die **enabledstate** -Eigenschaft auf 1 (Sonstiges) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="0afec-258">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="0afec-259">Diese Eigenschaft muss auf **null** festgelegt werden, wenn **enabledstate** ein anderer Wert als 1 ist.</span><span class="sxs-lookup"><span data-stu-id="0afec-259">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="0afec-260">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0afec-260">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0afec-261">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="0afec-261">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0afec-262">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0afec-262">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0afec-263">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0afec-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0afec-264">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="0afec-264">Provides high level status information.</span></span> <span data-ttu-id="0afec-265">Diese Eigenschaft sollte in Verbindung mit der Eigenschaft **detailedstatus** verwendet werden, um einen hohen und detaillierten Integritäts Status des Elements und seiner unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="0afec-265">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="0afec-266">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="0afec-266">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="0afec-267">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0afec-267">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="0afec-268"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="0afec-268"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0afec-269"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="0afec-269"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0afec-270"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (2** )</span><span class="sxs-lookup"><span data-stu-id="0afec-270"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0afec-271"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Fehler** (3)</span><span class="sxs-lookup"><span data-stu-id="0afec-271"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0afec-272"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="0afec-272"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0afec-273"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="0afec-273"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="0afec-274">)</span><span class="sxs-lookup"><span data-stu-id="0afec-274">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0afec-275">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="0afec-275">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0afec-276">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0afec-276">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0afec-277">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0afec-277">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0afec-278">Der zuletzt angeforderte oder gewünschte Zustand für das Element.</span><span class="sxs-lookup"><span data-stu-id="0afec-278">The last requested or desired state for the element.</span></span> <span data-ttu-id="0afec-279">Der tatsächliche Zustand des Elements wird durch **enabledstate** dargestellt.</span><span class="sxs-lookup"><span data-stu-id="0afec-279">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="0afec-280">Diese Eigenschaft wird bereitgestellt, um die zuletzt angeforderten und aktuell aktivierten oder deaktivierten Zustände zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="0afec-280">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="0afec-281">**RequestStateChange** kann von einer bestimmten Instanz von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85)) nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="0afec-281">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support **RequestStateChange**.</span></span> <span data-ttu-id="0afec-282">Wenn dies auftritt, wird der Wert 12 verwendet.</span><span class="sxs-lookup"><span data-stu-id="0afec-282">If this occurs, the value 12 is used.</span></span> <span data-ttu-id="0afec-283">Diese Eigenschaft wird von **CIM \_ enabledlogicalelement** geerbt.</span><span class="sxs-lookup"><span data-stu-id="0afec-283">This property is inherited from **CIM\_EnabledLogicalElement**.</span></span>



| <span data-ttu-id="0afec-284">Wert</span><span class="sxs-lookup"><span data-stu-id="0afec-284">Value</span></span>                                                                         | <span data-ttu-id="0afec-285">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0afec-285">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="0afec-286"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="0afec-286"><dt>12</dt></span></span> </dl> | <span data-ttu-id="0afec-287">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="0afec-287">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0afec-288">**Status**</span><span class="sxs-lookup"><span data-stu-id="0afec-288">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0afec-289">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0afec-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0afec-290">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0afec-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0afec-291">Der aktuelle Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="0afec-291">The current status of the object.</span></span> <span data-ttu-id="0afec-292">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="0afec-292">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0afec-293">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="0afec-293">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0afec-294">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="0afec-294">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0afec-295">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0afec-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0afec-296">Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="0afec-296">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="0afec-297">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="0afec-297">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="0afec-298">**Timeoflaststatechange**</span><span class="sxs-lookup"><span data-stu-id="0afec-298">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0afec-299">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="0afec-299">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0afec-300">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0afec-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0afec-301">Das Datum oder die Uhrzeit, zu dem der aktivierte Status des Elements zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="0afec-301">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="0afec-302">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0afec-302">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="0afec-303">**Transitioningumstate**</span><span class="sxs-lookup"><span data-stu-id="0afec-303">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0afec-304">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0afec-304">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0afec-305">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0afec-305">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0afec-306">Gibt den Ziel Status an, in den die-Instanz übergeht.</span><span class="sxs-lookup"><span data-stu-id="0afec-306">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="0afec-307">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="0afec-307">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="0afec-308">Wert</span><span class="sxs-lookup"><span data-stu-id="0afec-308">Value</span></span>                                                                         | <span data-ttu-id="0afec-309">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0afec-309">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="0afec-310"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="0afec-310"><dt>12</dt></span></span> </dl> | <span data-ttu-id="0afec-311">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="0afec-311">Not Applicable</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0afec-312">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0afec-312">Remarks</span></span>

<span data-ttu-id="0afec-313">Der Zugriff auf die **MSVM \_ terminalconnection** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="0afec-313">Access to the **Msvm\_TerminalConnection** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="0afec-314">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="0afec-314">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="0afec-315">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0afec-315">Requirements</span></span>



| <span data-ttu-id="0afec-316">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0afec-316">Requirement</span></span> | <span data-ttu-id="0afec-317">Wert</span><span class="sxs-lookup"><span data-stu-id="0afec-317">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0afec-318">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0afec-318">Minimum supported client</span></span><br/> | <span data-ttu-id="0afec-319">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0afec-319">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0afec-320">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0afec-320">Minimum supported server</span></span><br/> | <span data-ttu-id="0afec-321">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0afec-321">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0afec-322">Namespace</span><span class="sxs-lookup"><span data-stu-id="0afec-322">Namespace</span></span><br/>                | <span data-ttu-id="0afec-323">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="0afec-323">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0afec-324">MOF</span><span class="sxs-lookup"><span data-stu-id="0afec-324">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0afec-325"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0afec-325"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0afec-326">DLL</span><span class="sxs-lookup"><span data-stu-id="0afec-326">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0afec-327"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0afec-327"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0afec-328">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0afec-328">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0afec-329">**CIM \_ enabledlogicalelement**</span><span class="sxs-lookup"><span data-stu-id="0afec-329">**CIM\_EnabledLogicalElement**</span></span>](cim-enabledlogicalelement.md)
</dt> <dt>

<span data-ttu-id="0afec-330">[**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0afec-330">[**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="0afec-331">Video Klassen</span><span class="sxs-lookup"><span data-stu-id="0afec-331">Video Classes</span></span>](video-classes.md)
</dt> </dl>

 

