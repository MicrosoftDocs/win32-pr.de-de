---
description: Stellt ein Tastatur Gerät dar.
ms.assetid: 2a59fe90-12e2-471c-b49e-dfb4f4a31e0c
title: Msvm_Keyboard-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard
- Msvm_Keyboard.SetPowerState
- Msvm_Keyboard.EnableDevice
- Msvm_Keyboard.OnlineDevice
- Msvm_Keyboard.QuiesceDevice
- Msvm_Keyboard.SaveProperties
- Msvm_Keyboard.RestoreProperties
- Msvm_Keyboard.InstanceID
- Msvm_Keyboard.Caption
- Msvm_Keyboard.Description
- Msvm_Keyboard.ElementName
- Msvm_Keyboard.InstallDate
- Msvm_Keyboard.Name
- Msvm_Keyboard.OperationalStatus
- Msvm_Keyboard.StatusDescriptions
- Msvm_Keyboard.Status
- Msvm_Keyboard.HealthState
- Msvm_Keyboard.CommunicationStatus
- Msvm_Keyboard.DetailedStatus
- Msvm_Keyboard.OperatingStatus
- Msvm_Keyboard.PrimaryStatus
- Msvm_Keyboard.EnabledState
- Msvm_Keyboard.OtherEnabledState
- Msvm_Keyboard.RequestedState
- Msvm_Keyboard.EnabledDefault
- Msvm_Keyboard.TimeOfLastStateChange
- Msvm_Keyboard.AvailableRequestedStates
- Msvm_Keyboard.TransitioningToState
- Msvm_Keyboard.SystemCreationClassName
- Msvm_Keyboard.SystemName
- Msvm_Keyboard.CreationClassName
- Msvm_Keyboard.DeviceID
- Msvm_Keyboard.PowerManagementSupported
- Msvm_Keyboard.PowerManagementCapabilities
- Msvm_Keyboard.Availability
- Msvm_Keyboard.StatusInfo
- Msvm_Keyboard.LastErrorCode
- Msvm_Keyboard.ErrorDescription
- Msvm_Keyboard.ErrorCleared
- Msvm_Keyboard.OtherIdentifyingInfo
- Msvm_Keyboard.PowerOnHours
- Msvm_Keyboard.TotalPowerOnHours
- Msvm_Keyboard.IdentifyingDescriptions
- Msvm_Keyboard.AdditionalAvailability
- Msvm_Keyboard.MaxQuiesceTime
- Msvm_Keyboard.IsLocked
- Msvm_Keyboard.Layout
- Msvm_Keyboard.NumberOfFunctionKeys
- Msvm_Keyboard.Password
- Msvm_Keyboard.UnicodeSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 37c4faceb9072c1851868eb23c031e715cb6e1c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042240"
---
# <a name="msvm_keyboard-class"></a><span data-ttu-id="159ac-103">MSVM- \_ Tastatur Klasse</span><span class="sxs-lookup"><span data-stu-id="159ac-103">Msvm\_Keyboard class</span></span>

<span data-ttu-id="159ac-104">Stellt ein Tastatur Gerät dar.</span><span class="sxs-lookup"><span data-stu-id="159ac-104">Represents a keyboard device.</span></span> <span data-ttu-id="159ac-105">Tastaturen sind logische Geräte, die immer auf einem virtuellen Computer vorhanden sind und daher nicht über einen Ressourcenpool zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="159ac-105">Keyboards are logical devices that are always present in a virtual machine, and thus are not allocated through a resource pool.</span></span> <span data-ttu-id="159ac-106">Eine Instanz ist immer in einem virtuellen Computersystem vorhanden.</span><span class="sxs-lookup"><span data-stu-id="159ac-106">One instance is always present in a virtual computer system.</span></span>

<span data-ttu-id="159ac-107">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="159ac-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="159ac-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="159ac-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Keyboard : CIM_UserDevice
{
  string   InstanceID;
  string   Caption = "Keyboard";
  string   Description = "Microsoft Virtual Keyboard";
  string   ElementName = "Keyboard";
  datetime InstallDate;
  string   Name = "Keyboard";
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
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_Keyboard";
  string   DeviceID;
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability = 6;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  string   OtherIdentifyingInfo[];
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[] = { 6 };
  uint64   MaxQuiesceTime;
  boolean  IsLocked = False;
  string   Layout = "00000409";
  uint16   NumberOfFunctionKeys = 12;
  uint16   Password = 5;
  boolean  UnicodeSupported;
};
```

## <a name="members"></a><span data-ttu-id="159ac-109">Member</span><span class="sxs-lookup"><span data-stu-id="159ac-109">Members</span></span>

<span data-ttu-id="159ac-110">Die **MSVM- \_ Tastatur** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="159ac-110">The **Msvm\_Keyboard** class has these types of members:</span></span>

-   [<span data-ttu-id="159ac-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="159ac-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="159ac-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="159ac-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="159ac-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="159ac-113">Methods</span></span>

<span data-ttu-id="159ac-114">Die **MSVM- \_ Tastatur** Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="159ac-114">The **Msvm\_Keyboard** class has these methods.</span></span>



| <span data-ttu-id="159ac-115">Methode</span><span class="sxs-lookup"><span data-stu-id="159ac-115">Method</span></span>                                                         | <span data-ttu-id="159ac-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="159ac-116">Description</span></span>                                                   |
|:---------------------------------------------------------------|:--------------------------------------------------------------|
| <span data-ttu-id="159ac-117">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="159ac-117">**EnableDevice**</span></span>                                               | <span data-ttu-id="159ac-118">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="159ac-118">This method is not supported.</span></span><br/>                      |
| [<span data-ttu-id="159ac-119">**Iskeypressed**</span><span class="sxs-lookup"><span data-stu-id="159ac-119">**IsKeyPressed**</span></span>](iskeypressed-msvm-keyboard.md)             | <span data-ttu-id="159ac-120">Ruft den Schlüssel Zustand eines Schlüssels ab.</span><span class="sxs-lookup"><span data-stu-id="159ac-120">Retrieves the key state of a key.</span></span><br/>                  |
| <span data-ttu-id="159ac-121">**Onlinedevice**</span><span class="sxs-lookup"><span data-stu-id="159ac-121">**OnlineDevice**</span></span>                                               | <span data-ttu-id="159ac-122">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="159ac-122">This method is not supported.</span></span><br/>                      |
| [<span data-ttu-id="159ac-123">**PressKey**</span><span class="sxs-lookup"><span data-stu-id="159ac-123">**PressKey**</span></span>](presskey-msvm-keyboard.md)                     | <span data-ttu-id="159ac-124">Simuliert einen Tastendruck.</span><span class="sxs-lookup"><span data-stu-id="159ac-124">Simulates a key press.</span></span><br/>                             |
| <span data-ttu-id="159ac-125">**Inaktiven Geräte**</span><span class="sxs-lookup"><span data-stu-id="159ac-125">**QuiesceDevice**</span></span>                                              | <span data-ttu-id="159ac-126">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="159ac-126">This method is not supported.</span></span><br/>                      |
| [<span data-ttu-id="159ac-127">**Releasekey**</span><span class="sxs-lookup"><span data-stu-id="159ac-127">**ReleaseKey**</span></span>](releasekey-msvm-keyboard.md)                 | <span data-ttu-id="159ac-128">Simuliert eine Schlüssel Version.</span><span class="sxs-lookup"><span data-stu-id="159ac-128">Simulates a key release.</span></span><br/>                           |
| [<span data-ttu-id="159ac-129">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="159ac-129">**RequestStateChange**</span></span>](msvm-keyboard-requeststatechange.md) | <span data-ttu-id="159ac-130">Fordert an, dass der Zustand des Elements geändert wird.</span><span class="sxs-lookup"><span data-stu-id="159ac-130">Requests that the state of the element be changed.</span></span><br/> |
| [<span data-ttu-id="159ac-131">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="159ac-131">**Reset**</span></span>](msvm-keyboard-reset.md)                           | <span data-ttu-id="159ac-132">Setzt die virtuelle Tastatur zurück.</span><span class="sxs-lookup"><span data-stu-id="159ac-132">Resets the virtual keyboard.</span></span><br/>                       |
| <span data-ttu-id="159ac-133">**Restoreproperties**</span><span class="sxs-lookup"><span data-stu-id="159ac-133">**RestoreProperties**</span></span>                                          | <span data-ttu-id="159ac-134">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="159ac-134">This method is not supported.</span></span><br/>                      |
| <span data-ttu-id="159ac-135">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="159ac-135">**SaveProperties**</span></span>                                             | <span data-ttu-id="159ac-136">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="159ac-136">This method is not supported.</span></span><br/>                      |
| <span data-ttu-id="159ac-137">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="159ac-137">**SetPowerState**</span></span>                                              | <span data-ttu-id="159ac-138">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="159ac-138">This method is not supported.</span></span><br/>                      |
| [<span data-ttu-id="159ac-139">**Typectrlaltdel**</span><span class="sxs-lookup"><span data-stu-id="159ac-139">**TypeCtrlAltDel**</span></span>](typectrlaltdel-msvm-keyboard.md)         | <span data-ttu-id="159ac-140">Simuliert eine Tastenkombination STRG + ALT + ENTF.</span><span class="sxs-lookup"><span data-stu-id="159ac-140">Simulates a Ctrl+Alt+Del key sequence.</span></span><br/>             |
| [<span data-ttu-id="159ac-141">**Typekey**</span><span class="sxs-lookup"><span data-stu-id="159ac-141">**TypeKey**</span></span>](typekey-msvm-keyboard.md)                       | <span data-ttu-id="159ac-142">Simuliert eine Tastenkombination für die Tastenkombination.</span><span class="sxs-lookup"><span data-stu-id="159ac-142">Simulates a press-release key sequence.</span></span><br/>            |
| [<span data-ttu-id="159ac-143">**Typescancodes**</span><span class="sxs-lookup"><span data-stu-id="159ac-143">**TypeScancodes**</span></span>](msvm-keyboard-typescancodes.md)           | <span data-ttu-id="159ac-144">Simuliert eine Schlüssel Sequenz mithilfe von Scan Codes.</span><span class="sxs-lookup"><span data-stu-id="159ac-144">Simulates a key sequence using scan codes.</span></span><br/>         |
| [<span data-ttu-id="159ac-145">**TypeText**</span><span class="sxs-lookup"><span data-stu-id="159ac-145">**TypeText**</span></span>](typetext-msvm-keyboard.md)                     | <span data-ttu-id="159ac-146">Simuliert eine Reihe von typisierten Zeichen.</span><span class="sxs-lookup"><span data-stu-id="159ac-146">Simulates a series of typed characters.</span></span><br/>            |



 

### <a name="properties"></a><span data-ttu-id="159ac-147">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="159ac-147">Properties</span></span>

<span data-ttu-id="159ac-148">Die **MSVM- \_ Tastatur** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="159ac-148">The **Msvm\_Keyboard** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="159ac-149">**Additionalavailability**</span><span class="sxs-lookup"><span data-stu-id="159ac-149">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="159ac-150">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="159ac-150">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="159ac-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="159ac-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="159ac-152">Alle zusätzlichen Verfügbarkeit und den Status des Geräts, außer den in der **Availability** -Eigenschaft angegebenen.</span><span class="sxs-lookup"><span data-stu-id="159ac-152">Any additional availability and status of the device, beyond that specified in the **Availability** property.</span></span> <span data-ttu-id="159ac-153">Die **Availability** -Eigenschaft gibt den primären Status und die Verfügbarkeit des Geräts an.</span><span class="sxs-lookup"><span data-stu-id="159ac-153">The **Availability** property denotes the primary status and availability of the device.</span></span> <span data-ttu-id="159ac-154">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="159ac-154">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="159ac-155">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="159ac-155">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="159ac-156">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="159ac-156">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="159ac-157">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="159ac-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="159ac-158">Die primäre Verfügbarkeit und den Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="159ac-158">The primary availability and status of the device.</span></span> <span data-ttu-id="159ac-159">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="159ac-159">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="159ac-160">**Availablerequestedstates**</span><span class="sxs-lookup"><span data-stu-id="159ac-160">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="159ac-161">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="159ac-161">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="159ac-162">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="159ac-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="159ac-163">Gibt die möglichen Werte für den *requestedstate* -Parameter der **requestStateChange** -Methode an.</span><span class="sxs-lookup"><span data-stu-id="159ac-163">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="159ac-164">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="159ac-164">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="159ac-165">**Caption**</span><span class="sxs-lookup"><span data-stu-id="159ac-165">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="159ac-166">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="159ac-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="159ac-167">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="159ac-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="159ac-168">Qualifizierer: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="159ac-168">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="159ac-169">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="159ac-169">A short description of the object.</span></span> <span data-ttu-id="159ac-170">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="159ac-170">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="159ac-171">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="159ac-171">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="159ac-172">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="159ac-172">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="159ac-173">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="159ac-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="159ac-174">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="159ac-174">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="159ac-175">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="159ac-175">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="159ac-176">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="159ac-176">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="159ac-177"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="159ac-177"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="159ac-178"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="159ac-178"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="159ac-179"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Kommunikation OK** (2)</span><span class="sxs-lookup"><span data-stu-id="159ac-179"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="159ac-180"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Verlorene Kommunikation** (3)</span><span class="sxs-lookup"><span data-stu-id="159ac-180"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="159ac-181"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Kein Kontakt** (4)</span><span class="sxs-lookup"><span data-stu-id="159ac-181"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="159ac-182"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="159ac-182"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="159ac-183"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="159ac-183"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="159ac-184">)</span><span class="sxs-lookup"><span data-stu-id="159ac-184">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="159ac-185">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="159ac-185">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="159ac-186">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="159ac-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="159ac-187">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="159ac-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="159ac-188">Qualifizierer: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="159ac-188">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="159ac-189">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer-Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="159ac-189">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="159ac-190">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="159ac-190">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span> <span data-ttu-id="159ac-191">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="159ac-191">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="159ac-192">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="159ac-192">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="159ac-193">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="159ac-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="159ac-194">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="159ac-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="159ac-195">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="159ac-195">A description of the object.</span></span> <span data-ttu-id="159ac-196">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="159ac-196">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="159ac-197">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="159ac-197">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="159ac-198">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="159ac-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="159ac-199">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="159ac-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="159ac-200">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="159ac-200">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="159ac-201">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="159ac-201">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="159ac-202">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="159ac-202">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="159ac-203"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (0)</span><span class="sxs-lookup"><span data-stu-id="159ac-203"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="159ac-204"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Keine zusätzlichen Informationen** (1)</span><span class="sxs-lookup"><span data-stu-id="159ac-204"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="159ac-205"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Betont** (2)</span><span class="sxs-lookup"><span data-stu-id="159ac-205"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="159ac-206"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Vorhersagefehler** (3)</span><span class="sxs-lookup"><span data-stu-id="159ac-206"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="159ac-207"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Nicht BEHEB barer Fehler** (4)</span><span class="sxs-lookup"><span data-stu-id="159ac-207"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="159ac-208"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Unterstützende Entität in Error** (5)</span><span class="sxs-lookup"><span data-stu-id="159ac-208"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="159ac-209"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="159ac-209"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="159ac-210"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="159ac-210"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="159ac-211">)</span><span class="sxs-lookup"><span data-stu-id="159ac-211">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="159ac-212">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="159ac-212">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="159ac-213">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="159ac-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="159ac-214">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="159ac-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="159ac-215">Eine Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="159ac-215">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="159ac-216">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist immer auf "Microsoft:*GUID*" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="159ac-216">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*GUID*".</span></span>

</dd> <dt>

<span data-ttu-id="159ac-217">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="159ac-217">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="159ac-218">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="159ac-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="159ac-219">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="159ac-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="159ac-220">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="159ac-220">A display name for the object.</span></span> <span data-ttu-id="159ac-221">Mit dieser Eigenschaft kann jede Instanz zusätzlich zu ihren Schlüsseleigenschaften, Identitätsdaten und Beschreibungs Informationen einen anzeigen Amen definieren.</span><span class="sxs-lookup"><span data-stu-id="159ac-221">This property allows each instance to define a display name in addition to its key properties, identity data, and description information.</span></span> <span data-ttu-id="159ac-222">Die [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) -Eigenschaft der **CIM \_ ManagedSystemElement** -Klasse wird auch als Anzeige Name definiert.</span><span class="sxs-lookup"><span data-stu-id="159ac-222">The [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) property of the **CIM\_ManagedSystemElement** class is also defined as a display name.</span></span> <span data-ttu-id="159ac-223">Sie wird jedoch häufig als Schlüssel untergeordnet eingestuft.</span><span class="sxs-lookup"><span data-stu-id="159ac-223">But, it is often subclassed to be a Key.</span></span> <span data-ttu-id="159ac-224">Es ist nicht sinnvoll, dass dieselbe Eigenschaft ohne Inkonsistenzen sowohl Identität als auch einen anzeigen Amen vermitteln kann.</span><span class="sxs-lookup"><span data-stu-id="159ac-224">It is not reasonable that the same property can convey both identity and a display name, without inconsistencies.</span></span> <span data-ttu-id="159ac-225">Wenn **Name** vorhanden und kein Schlüssel ist (z. b. für Instanzen von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)), können dieselben Informationen in den Eigenschaften **Name** und **ElementName** vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="159ac-225">Where **Name** exists and is not a Key (such as for instances of [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)), the same information can be present in both the **Name** and **ElementName** properties.</span></span> <span data-ttu-id="159ac-226">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="159ac-226">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="159ac-227">**Enableddefault**</span><span class="sxs-lookup"><span data-stu-id="159ac-227">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="159ac-228">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="159ac-228">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="159ac-229">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="159ac-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="159ac-230">Die Standard-oder Startkonfiguration eines Administrators für den aktivierten Zustand eines Elements.</span><span class="sxs-lookup"><span data-stu-id="159ac-230">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="159ac-231">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="159ac-231">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="159ac-232">Wert</span><span class="sxs-lookup"><span data-stu-id="159ac-232">Value</span></span>                                                                        | <span data-ttu-id="159ac-233">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="159ac-233">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="159ac-234"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="159ac-234"><dt>2</dt></span></span> </dl> | <span data-ttu-id="159ac-235">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="159ac-235">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="159ac-236">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="159ac-236">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="159ac-237">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="159ac-237">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="159ac-238">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="159ac-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="159ac-239">Gibt den aktivierten und deaktivierten Status eines Elements an.</span><span class="sxs-lookup"><span data-stu-id="159ac-239">Indicates the enabled and disabled states of an element.</span></span> <span data-ttu-id="159ac-240">Sie kann auch die Übergänge zwischen diesen angeforderten Zuständen angeben.</span><span class="sxs-lookup"><span data-stu-id="159ac-240">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="159ac-241">Beispielsweise sind das Herunterfahren (Wert = 4) und das Starten (Wert = 10) vorübergehende Zustände zwischen aktiviert und deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="159ac-241">For example, shutting down (value=4) and starting (value=10) are transient states between enabled and disabled.</span></span>



| <span data-ttu-id="159ac-242">Wert</span><span class="sxs-lookup"><span data-stu-id="159ac-242">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="159ac-243">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="159ac-243">Meaning</span></span>                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="159ac-244"><dt>**Unbekannter**</dt> Wert <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="159ac-244"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="159ac-245">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="159ac-245">Unknown</span></span><br/>                                                                                                                                                                                              |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="159ac-246"><dt>**Sonstige**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="159ac-246"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         | <span data-ttu-id="159ac-247">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="159ac-247">Other</span></span><br/>                                                                                                                                                                                                |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="159ac-248"><dt>**Aktiviert**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="159ac-248"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="159ac-249">Das-Element ist oder kann Befehle ausführen, verarbeitet alle in der Warteschlange befindlichen Befehle und fügt neue Anforderungen in die Warteschlange ein.</span><span class="sxs-lookup"><span data-stu-id="159ac-249">The element is or could be executing commands, will process any queued commands, and queues new requests.</span></span><br/>                                                                                            |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="159ac-250"><dt>**Deaktiviert**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="159ac-250"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="159ac-251">Das-Element führt keine Befehle aus und löscht alle neuen Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="159ac-251">The element will not execute commands and will drop any new requests.</span></span><br/>                                                                                                                                |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="159ac-252"><dt>4</dt> wird <dt>**heruntergefahren**</dt></span><span class="sxs-lookup"><span data-stu-id="159ac-252"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="159ac-253">Das Element wird gerade in den deaktivierten Zustand versetzt.</span><span class="sxs-lookup"><span data-stu-id="159ac-253">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                          |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="159ac-254"><dt>**Nicht zutreffend**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="159ac-254"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="159ac-255">Das Element unterstützt das Aktivieren oder Deaktivieren des Elements nicht.</span><span class="sxs-lookup"><span data-stu-id="159ac-255">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                              |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="159ac-256"><dt>**Aktiviert, aber offline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="159ac-256"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="159ac-257">Das-Element kann Befehle abschließen und alle neuen Anforderungen löschen.</span><span class="sxs-lookup"><span data-stu-id="159ac-257">The element might be completing commands and will drop any new requests.</span></span><br/>                                                                                                                             |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="159ac-258"><dt>**In Test**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="159ac-258"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="159ac-259">Das-Element befindet sich in einem Testzustand.</span><span class="sxs-lookup"><span data-stu-id="159ac-259">The element is in a test state.</span></span><br/>                                                                                                                                                                      |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="159ac-260"><dt></dt> Verzögert <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="159ac-260"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="159ac-261">Das Element kann Befehle abschließen, aber alle neuen Anforderungen werden in die Warteschlange eingereiht.</span><span class="sxs-lookup"><span data-stu-id="159ac-261">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                        |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="159ac-262"><dt>**Inesce**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="159ac-262"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="159ac-263">Das Element ist aktiviert, jedoch in einem eingeschränkten Modus.</span><span class="sxs-lookup"><span data-stu-id="159ac-263">The element is enabled but in a restricted mode.</span></span> <span data-ttu-id="159ac-264">Das Verhalten des-Elements ähnelt dem aktivierten Status (2), aber es verarbeitet nur einen eingeschränkten Satz von Befehlen.</span><span class="sxs-lookup"><span data-stu-id="159ac-264">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="159ac-265">Alle anderen Anforderungen werden in die Warteschlange eingereiht.</span><span class="sxs-lookup"><span data-stu-id="159ac-265">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="159ac-266"><dt>**Start**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="159ac-266"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="159ac-267">Das Element wechselt in den Zustand "aktiviert" (2).</span><span class="sxs-lookup"><span data-stu-id="159ac-267">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="159ac-268">Neue Anforderungen werden in die Warteschlange eingereiht.</span><span class="sxs-lookup"><span data-stu-id="159ac-268">New requests are queued.</span></span><br/>                                                                                                             |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="159ac-269"><dt>**DMTF reserviert**</dt> <dt>11 32767</dt></span><span class="sxs-lookup"><span data-stu-id="159ac-269"><dt>**DMTF Reserved**</dt> <dt>11 32767</dt></span></span> </dl>                  | <span data-ttu-id="159ac-270">Dieser Wert ist reserviert.</span><span class="sxs-lookup"><span data-stu-id="159ac-270">This value is reserved.</span></span><br/>                                                                                                                                                                              |
| <span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span><dl> <span data-ttu-id="159ac-271"><dt>**Anbieter reserviert**</dt> <dt>32768 65535</dt></span><span class="sxs-lookup"><span data-stu-id="159ac-271"><dt>**Vendor Reserved**</dt> <dt>32768 65535</dt></span></span> </dl>       | <span data-ttu-id="159ac-272">Dieser Wert ist reserviert.</span><span class="sxs-lookup"><span data-stu-id="159ac-272">This value is reserved.</span></span><br/>                                                                                                                                                                              |



 

</dd> <dt>

<span data-ttu-id="159ac-273">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="159ac-273">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="159ac-274">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="159ac-274">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="159ac-275">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="159ac-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="159ac-276">Gibt an, ob der in **LastErrorCode** gemeldete Fehler jetzt gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="159ac-276">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="159ac-277">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="159ac-277">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="159ac-278">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="159ac-278">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="159ac-279">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="159ac-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="159ac-280">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="159ac-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="159ac-281">Eine Zeichenfolge, die weitere Informationen über den Fehler enthält, der in **LastErrorCode** aufgezeichnet wurde, sowie Informationen über alle Maßnahmen, die ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="159ac-281">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="159ac-282">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="159ac-282">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="159ac-283">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="159ac-283">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="159ac-284">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="159ac-284">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="159ac-285">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="159ac-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="159ac-286">Der aktuelle Zustand des Elements.</span><span class="sxs-lookup"><span data-stu-id="159ac-286">The current health of the element.</span></span> <span data-ttu-id="159ac-287">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und ist immer auf 5 (OK) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="159ac-287">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="159ac-288">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="159ac-288">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="159ac-289">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="159ac-289">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="159ac-290">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="159ac-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="159ac-291">Ein Array von Freiform-Zeichen folgen, die Erklärungen und Details hinter den Einträgen im " **OtherIdentifyingInfo** "-Array bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="159ac-291">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** array.</span></span> <span data-ttu-id="159ac-292">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="159ac-292">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="159ac-293">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="159ac-293">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="159ac-294">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="159ac-294">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="159ac-295">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="159ac-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="159ac-296">Das Datum und die Uhrzeit der Erstellung der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="159ac-296">The date and time when the virtual machine was created.</span></span> <span data-ttu-id="159ac-297">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="159ac-297">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="159ac-298">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="159ac-298">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="159ac-299">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="159ac-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="159ac-300">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="159ac-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="159ac-301">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="159ac-301">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="159ac-302">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="159ac-302">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="159ac-303">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="159ac-303">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="159ac-304">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="159ac-304">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="159ac-305">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="159ac-305">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="159ac-306">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="159ac-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="159ac-307">Gibt an, ob das Gerät gesperrt ist, und verhindert Benutzereingaben oder-Ausgaben.</span><span class="sxs-lookup"><span data-stu-id="159ac-307">Indicates whether the device is locked, preventing user input or output.</span></span> <span data-ttu-id="159ac-308">Diese Eigenschaft wird von [**CIM \_ userdevice**](/windows/desktop/CIMWin32Prov/cim-userdevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="159ac-308">This property is inherited from [**CIM\_UserDevice**](/windows/desktop/CIMWin32Prov/cim-userdevice).</span></span>

</dd> <dt>

<span data-ttu-id="159ac-309">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="159ac-309">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="159ac-310">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="159ac-310">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="159ac-311">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="159ac-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="159ac-312">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="159ac-312">The last error code reported by the logical device.</span></span> <span data-ttu-id="159ac-313">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="159ac-313">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="159ac-314">**Layout**</span><span class="sxs-lookup"><span data-stu-id="159ac-314">**Layout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="159ac-315">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="159ac-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="159ac-316">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="159ac-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="159ac-317">Eine Zeichenfolge, die das Format und das Layout der Tastatur angibt.</span><span class="sxs-lookup"><span data-stu-id="159ac-317">A string indicating the format and layout of the keyboard.</span></span>

</dd> <dt>

<span data-ttu-id="159ac-318">**Maxquiescetime**</span><span class="sxs-lookup"><span data-stu-id="159ac-318">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="159ac-319">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="159ac-319">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="159ac-320">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="159ac-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="159ac-321">Diese Eigenschaft ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="159ac-321">This property has been deprecated.</span></span> <span data-ttu-id="159ac-322">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="159ac-322">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="159ac-323">**Name**</span><span class="sxs-lookup"><span data-stu-id="159ac-323">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="159ac-324">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="159ac-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="159ac-325">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="159ac-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="159ac-326">Qualifizierer: **maxlen** (1024)</span><span class="sxs-lookup"><span data-stu-id="159ac-326">Qualifiers: **MaxLen** (1024)</span></span>
</dt> </dl>

<span data-ttu-id="159ac-327">Die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="159ac-327">The label by which the object is known.</span></span> <span data-ttu-id="159ac-328">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="159ac-328">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="159ac-329">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="159ac-329">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="159ac-330">**"Numoffunctionkeys"**</span><span class="sxs-lookup"><span data-stu-id="159ac-330">**NumberOfFunctionKeys**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="159ac-331">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="159ac-331">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="159ac-332">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="159ac-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="159ac-333">Die Anzahl der Funktionstasten auf der Tastatur.</span><span class="sxs-lookup"><span data-stu-id="159ac-333">The number of function keys on the keyboard.</span></span>

</dd> <dt>

<span data-ttu-id="159ac-334">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="159ac-334">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="159ac-335">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="159ac-335">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="159ac-336">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="159ac-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="159ac-337">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="159ac-337">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="159ac-338">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="159ac-338">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="159ac-339">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="159ac-339">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="159ac-340"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="159ac-340"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="159ac-341"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="159ac-341"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="159ac-342"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Wartung** (2)</span><span class="sxs-lookup"><span data-stu-id="159ac-342"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="159ac-343"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>Wird **gestartet** (3)</span><span class="sxs-lookup"><span data-stu-id="159ac-343"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="159ac-344"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>Wird **beendet (4** )</span><span class="sxs-lookup"><span data-stu-id="159ac-344"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="159ac-345"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Beendet** (5)</span><span class="sxs-lookup"><span data-stu-id="159ac-345"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="159ac-346"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abgebrochen** (6)</span><span class="sxs-lookup"><span data-stu-id="159ac-346"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="159ac-347"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Ruhende** (7)</span><span class="sxs-lookup"><span data-stu-id="159ac-347"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="159ac-348"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Abgeschlossen** (8)</span><span class="sxs-lookup"><span data-stu-id="159ac-348"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="159ac-349"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrieren** (9)</span><span class="sxs-lookup"><span data-stu-id="159ac-349"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="159ac-350"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Migration** (10)</span><span class="sxs-lookup"><span data-stu-id="159ac-350"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="159ac-351"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migration** (11)</span><span class="sxs-lookup"><span data-stu-id="159ac-351"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="159ac-352"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotts** (12)</span><span class="sxs-lookup"><span data-stu-id="159ac-352"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="159ac-353"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Herunter** fahren (13)</span><span class="sxs-lookup"><span data-stu-id="159ac-353"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="159ac-354"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span><span class="sxs-lookup"><span data-stu-id="159ac-354"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="159ac-355"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Übergang** (15)</span><span class="sxs-lookup"><span data-stu-id="159ac-355"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="159ac-356"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Dienst** (16)</span><span class="sxs-lookup"><span data-stu-id="159ac-356"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="159ac-357"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="159ac-357"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="159ac-358"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="159ac-358"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="159ac-359">)</span><span class="sxs-lookup"><span data-stu-id="159ac-359">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="159ac-360">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="159ac-360">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="159ac-361">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="159ac-361">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="159ac-362">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="159ac-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="159ac-363">Der aktuelle Status des Elements.</span><span class="sxs-lookup"><span data-stu-id="159ac-363">The current status of the element.</span></span> <span data-ttu-id="159ac-364">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und ist immer auf 2 (OK) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="159ac-364">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="159ac-365">**Otherenabledstate**</span><span class="sxs-lookup"><span data-stu-id="159ac-365">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="159ac-366">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="159ac-366">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="159ac-367">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="159ac-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="159ac-368">Eine Zeichenfolge, die den aktivierten oder deaktivierten Status des Elements beschreibt, wenn die **enabledstate** -Eigenschaft auf 1 (Sonstiges) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="159ac-368">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="159ac-369">Diese Eigenschaft muss auf **null** festgelegt werden, wenn **enabledstate** ein anderer Wert als 1 ist.</span><span class="sxs-lookup"><span data-stu-id="159ac-369">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="159ac-370">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="159ac-370">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="159ac-371">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="159ac-371">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="159ac-372">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="159ac-372">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="159ac-373">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="159ac-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="159ac-374">Alle zusätzlichen Daten über Geräte-ID-Informationen, die zur Identifizierung eines logischen Geräts verwendet werden könnten.</span><span class="sxs-lookup"><span data-stu-id="159ac-374">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="159ac-375">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="159ac-375">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="159ac-376">**Kennwort**</span><span class="sxs-lookup"><span data-stu-id="159ac-376">**Password**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="159ac-377">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="159ac-377">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="159ac-378">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="159ac-378">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="159ac-379">Gibt an, ob ein Kennwort auf Hardwareebene auf der Tastatur aktiviert ist, wodurch lokale Eingaben verhindert werden.</span><span class="sxs-lookup"><span data-stu-id="159ac-379">Indicates whether a hardware-level password is enabled at the keyboard, preventing local input.</span></span>

<dt>

<span data-ttu-id="159ac-380">5</span><span class="sxs-lookup"><span data-stu-id="159ac-380">5</span></span>
</dt> <dd>

<span data-ttu-id="159ac-381">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="159ac-381">Not implemented.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="159ac-382">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="159ac-382">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="159ac-383">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="159ac-383">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="159ac-384">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="159ac-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="159ac-385">Die Energie Verwaltungsfunktionen des Geräts.</span><span class="sxs-lookup"><span data-stu-id="159ac-385">The power management capabilities of the device.</span></span> <span data-ttu-id="159ac-386">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="159ac-386">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="159ac-387">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="159ac-387">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="159ac-388">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="159ac-388">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="159ac-389">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="159ac-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="159ac-390">Gibt an, ob das Gerät Energie gesteuert werden kann.</span><span class="sxs-lookup"><span data-stu-id="159ac-390">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="159ac-391">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="159ac-391">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="159ac-392">**Poweronhours**</span><span class="sxs-lookup"><span data-stu-id="159ac-392">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="159ac-393">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="159ac-393">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="159ac-394">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="159ac-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="159ac-395">Gibt an, wie viele aufeinanderfolgende Stunden dieses Gerät seit dem letzten Strom Umgebung eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="159ac-395">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="159ac-396">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="159ac-396">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="159ac-397">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="159ac-397">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="159ac-398">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="159ac-398">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="159ac-399">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="159ac-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="159ac-400">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="159ac-400">Provides high level status information.</span></span> <span data-ttu-id="159ac-401">Diese Eigenschaft sollte in Verbindung mit der Eigenschaft **detailedstatus** verwendet werden, um einen hohen und detaillierten Integritäts Status des Elements und seiner unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="159ac-401">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="159ac-402">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="159ac-402">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="159ac-403">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="159ac-403">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="159ac-404"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="159ac-404"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="159ac-405"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="159ac-405"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="159ac-406"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (2** )</span><span class="sxs-lookup"><span data-stu-id="159ac-406"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="159ac-407"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Fehler** (3)</span><span class="sxs-lookup"><span data-stu-id="159ac-407"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="159ac-408"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="159ac-408"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="159ac-409"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="159ac-409"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="159ac-410">)</span><span class="sxs-lookup"><span data-stu-id="159ac-410">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="159ac-411">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="159ac-411">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="159ac-412">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="159ac-412">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="159ac-413">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="159ac-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="159ac-414">Der zuletzt angeforderte Zustand für das Element.</span><span class="sxs-lookup"><span data-stu-id="159ac-414">The last requested state for the element.</span></span>



| <span data-ttu-id="159ac-415">Wert</span><span class="sxs-lookup"><span data-stu-id="159ac-415">Value</span></span>                                                                                                                                                                                                                                                    | <span data-ttu-id="159ac-416">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="159ac-416">Meaning</span></span>                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="159ac-417"><dt>**Nicht zutreffend**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="159ac-417"><dt>**Not Applicable**</dt> <dt>12</dt></span></span> </dl> | <span data-ttu-id="159ac-418">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="159ac-418">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="159ac-419">**Status**</span><span class="sxs-lookup"><span data-stu-id="159ac-419">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="159ac-420">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="159ac-420">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="159ac-421">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="159ac-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="159ac-422">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="159ac-422">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="159ac-423">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="159ac-423">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="159ac-424">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="159ac-424">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="159ac-425">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="159ac-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="159ac-426">Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="159ac-426">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="159ac-427">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und ist immer auf "OK" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="159ac-427">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="159ac-428">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="159ac-428">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="159ac-429">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="159ac-429">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="159ac-430">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="159ac-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="159ac-431">Der aktuelle Zustand des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="159ac-431">The current state of the logical device.</span></span> <span data-ttu-id="159ac-432">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="159ac-432">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="159ac-433">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="159ac-433">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="159ac-434">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="159ac-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="159ac-435">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="159ac-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="159ac-436">Qualifizierer: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="159ac-436">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="159ac-437">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="159ac-437">The scoping system's creation class name.</span></span> <span data-ttu-id="159ac-438">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist auf "MSVM \_ Computersystem" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="159ac-438">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="159ac-439">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="159ac-439">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="159ac-440">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="159ac-440">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="159ac-441">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="159ac-441">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="159ac-442">Qualifizierer: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="159ac-442">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="159ac-443">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="159ac-443">The scoping system's name.</span></span> <span data-ttu-id="159ac-444">Dieser Wert entspricht dem Wert der **Name** -Eigenschaft der [**MSVM \_ Computersystem**](msvm-computersystem.md) -Klasse für die Bereichs bezogene virtuelle Maschine.</span><span class="sxs-lookup"><span data-stu-id="159ac-444">This value corresponds to the value of the **Name** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class for the scoping virtual machine.</span></span> <span data-ttu-id="159ac-445">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="159ac-445">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="159ac-446">**Timeoflaststatechange**</span><span class="sxs-lookup"><span data-stu-id="159ac-446">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="159ac-447">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="159ac-447">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="159ac-448">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="159ac-448">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="159ac-449">Das Datum und die Uhrzeit der letzten Änderung des aktivierten Zustands des Elements.</span><span class="sxs-lookup"><span data-stu-id="159ac-449">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="159ac-450">Wenn der Zustand des Elements nicht geändert wurde und diese Eigenschaft aufgefüllt ist, muss Sie auf einen Wert von 0 Intervall festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="159ac-450">If the state of the element has not changed and this property is populated, then it must be set to a 0 interval value.</span></span> <span data-ttu-id="159ac-451">Wenn eine Zustandsänderung angefordert, aber abgelehnt oder noch nicht verarbeitet wurde, darf die Eigenschaft nicht aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="159ac-451">If a state change was requested, but rejected or not yet processed, the property must not be updated.</span></span> <span data-ttu-id="159ac-452">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="159ac-452">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="159ac-453">**Totalpoweronhours**</span><span class="sxs-lookup"><span data-stu-id="159ac-453">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="159ac-454">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="159ac-454">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="159ac-455">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="159ac-455">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="159ac-456">Die Gesamtanzahl der Stunden, für die dieses Gerät eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="159ac-456">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="159ac-457">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="159ac-457">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="159ac-458">**Transitioningumstate**</span><span class="sxs-lookup"><span data-stu-id="159ac-458">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="159ac-459">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="159ac-459">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="159ac-460">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="159ac-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="159ac-461">Gibt den Ziel Status an, in den die-Instanz übergeht.</span><span class="sxs-lookup"><span data-stu-id="159ac-461">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="159ac-462">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="159ac-462">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="159ac-463">**Unicodesupported**</span><span class="sxs-lookup"><span data-stu-id="159ac-463">**UnicodeSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="159ac-464">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="159ac-464">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="159ac-465">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="159ac-465">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="159ac-466">Gibt an, ob die virtuelle Tastatur Unicode-Zeichen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="159ac-466">Indicates if the virtual keyboard supports Unicode characters.</span></span> <span data-ttu-id="159ac-467">Dies kann einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="159ac-467">This can be one of the following values.</span></span>



| <span data-ttu-id="159ac-468">Wert</span><span class="sxs-lookup"><span data-stu-id="159ac-468">Value</span></span>                                                                            | <span data-ttu-id="159ac-469">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="159ac-469">Meaning</span></span>                                                              |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="159ac-470"><dt>True</dt></span><span class="sxs-lookup"><span data-stu-id="159ac-470"><dt>True</dt></span></span> </dl>  | <span data-ttu-id="159ac-471">Die virtuelle Tastatur unterstützt Unicode-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="159ac-471">The virtual keyboard supports Unicode characters.</span></span><br/>         |
| <dl> <span data-ttu-id="159ac-472"><dt>False</dt></span><span class="sxs-lookup"><span data-stu-id="159ac-472"><dt>False</dt></span></span> </dl> | <span data-ttu-id="159ac-473">Die virtuelle Tastatur unterstützt keine Unicode-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="159ac-473">The virtual keyboard does not support Unicode characters.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="159ac-474">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="159ac-474">Remarks</span></span>

<span data-ttu-id="159ac-475">Der Zugriff auf die **MSVM- \_ Tastatur** Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="159ac-475">Access to the **Msvm\_Keyboard** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="159ac-476">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="159ac-476">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="159ac-477">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="159ac-477">Requirements</span></span>



| <span data-ttu-id="159ac-478">Anforderung</span><span class="sxs-lookup"><span data-stu-id="159ac-478">Requirement</span></span> | <span data-ttu-id="159ac-479">Wert</span><span class="sxs-lookup"><span data-stu-id="159ac-479">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="159ac-480">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="159ac-480">Minimum supported client</span></span><br/> | <span data-ttu-id="159ac-481">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="159ac-481">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="159ac-482">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="159ac-482">Minimum supported server</span></span><br/> | <span data-ttu-id="159ac-483">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="159ac-483">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="159ac-484">Namespace</span><span class="sxs-lookup"><span data-stu-id="159ac-484">Namespace</span></span><br/>                | <span data-ttu-id="159ac-485">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="159ac-485">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="159ac-486">MOF</span><span class="sxs-lookup"><span data-stu-id="159ac-486">MOF</span></span><br/>                      | <dl> <span data-ttu-id="159ac-487"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="159ac-487"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="159ac-488">DLL</span><span class="sxs-lookup"><span data-stu-id="159ac-488">DLL</span></span><br/>                      | <dl> <span data-ttu-id="159ac-489"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="159ac-489"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="159ac-490">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="159ac-490">See also</span></span>

<dl> <dt>

[<span data-ttu-id="159ac-491">**CIM- \_ userdevice**</span><span class="sxs-lookup"><span data-stu-id="159ac-491">**CIM\_UserDevice**</span></span>](cim-userdevice.md)
</dt> <dt>

[<span data-ttu-id="159ac-492">**CIM- \_ userdevice**</span><span class="sxs-lookup"><span data-stu-id="159ac-492">**CIM\_UserDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-userdevice)
</dt> <dt>

[<span data-ttu-id="159ac-493">Eingabe Klassen</span><span class="sxs-lookup"><span data-stu-id="159ac-493">Input Classes</span></span>](input-classes.md)
</dt> </dl>

 

