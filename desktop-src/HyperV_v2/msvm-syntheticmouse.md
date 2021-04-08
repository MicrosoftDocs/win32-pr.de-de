---
description: Stellt ein synthetisches Mausgerät dar.
ms.assetid: c04b7aa1-44fe-41f5-943f-ff49ce64be96
title: Msvm_SyntheticMouse-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticMouse
- Msvm_SyntheticMouse.SetPowerState
- Msvm_SyntheticMouse.EnableDevice
- Msvm_SyntheticMouse.OnlineDevice
- Msvm_SyntheticMouse.QuiesceDevice
- Msvm_SyntheticMouse.SaveProperties
- Msvm_SyntheticMouse.RestoreProperties
- Msvm_SyntheticMouse.InstanceID
- Msvm_SyntheticMouse.Caption
- Msvm_SyntheticMouse.Description
- Msvm_SyntheticMouse.ElementName
- Msvm_SyntheticMouse.InstallDate
- Msvm_SyntheticMouse.Name
- Msvm_SyntheticMouse.OperationalStatus
- Msvm_SyntheticMouse.StatusDescriptions
- Msvm_SyntheticMouse.Status
- Msvm_SyntheticMouse.HealthState
- Msvm_SyntheticMouse.CommunicationStatus
- Msvm_SyntheticMouse.DetailedStatus
- Msvm_SyntheticMouse.OperatingStatus
- Msvm_SyntheticMouse.PrimaryStatus
- Msvm_SyntheticMouse.EnabledState
- Msvm_SyntheticMouse.OtherEnabledState
- Msvm_SyntheticMouse.RequestedState
- Msvm_SyntheticMouse.EnabledDefault
- Msvm_SyntheticMouse.TimeOfLastStateChange
- Msvm_SyntheticMouse.AvailableRequestedStates
- Msvm_SyntheticMouse.TransitioningToState
- Msvm_SyntheticMouse.SystemCreationClassName
- Msvm_SyntheticMouse.SystemName
- Msvm_SyntheticMouse.CreationClassName
- Msvm_SyntheticMouse.DeviceID
- Msvm_SyntheticMouse.PowerManagementSupported
- Msvm_SyntheticMouse.PowerManagementCapabilities
- Msvm_SyntheticMouse.Availability
- Msvm_SyntheticMouse.StatusInfo
- Msvm_SyntheticMouse.LastErrorCode
- Msvm_SyntheticMouse.ErrorDescription
- Msvm_SyntheticMouse.ErrorCleared
- Msvm_SyntheticMouse.OtherIdentifyingInfo
- Msvm_SyntheticMouse.PowerOnHours
- Msvm_SyntheticMouse.TotalPowerOnHours
- Msvm_SyntheticMouse.IdentifyingDescriptions
- Msvm_SyntheticMouse.AdditionalAvailability
- Msvm_SyntheticMouse.MaxQuiesceTime
- Msvm_SyntheticMouse.IsLocked
- Msvm_SyntheticMouse.PointingType
- Msvm_SyntheticMouse.NumberOfButtons
- Msvm_SyntheticMouse.Handedness
- Msvm_SyntheticMouse.Resolution
- Msvm_SyntheticMouse.AbsoluteCoordinates
- Msvm_SyntheticMouse.HorizontalPosition
- Msvm_SyntheticMouse.VerticalPosition
- Msvm_SyntheticMouse.ScrollPosition
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1c5be44637c91ebd57867c5062eba6f9e57ee543
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750193"
---
# <a name="msvm_syntheticmouse-class"></a><span data-ttu-id="1fe4b-103">MSVM- \_ syntheticmouse-Klasse</span><span class="sxs-lookup"><span data-stu-id="1fe4b-103">Msvm\_SyntheticMouse class</span></span>

<span data-ttu-id="1fe4b-104">Stellt ein synthetisches Mausgerät dar.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-104">Represents a synthetic mouse device.</span></span>

<span data-ttu-id="1fe4b-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fe4b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="1fe4b-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticMouse : CIM_PointingDevice
{
  string   InstanceID;
  string   Caption = "Mouse";
  string   Description = "Microsoft Synthetic Mouse";
  string   ElementName = "Mouse";
  datetime InstallDate;
  string   Name = "Mouse";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = {
                "OK"
              };
  string   Status;
  uint16   HealthState = 5;
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
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_SyntheticMouse";
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
  uint16   AdditionalAvailability[] = {6};
  uint64   MaxQuiesceTime;
  boolean  IsLocked = False;
  uint16   PointingType = 3;
  uint8    NumberOfButtons = 5;
  uint16   Handedness = 2;
  uint32   Resolution;
  boolean  AbsoluteCoordinates = True;
  sint32   HorizontalPosition;
  sint32   VerticalPosition;
  sint32   ScrollPosition;
};
```

## <a name="members"></a><span data-ttu-id="1fe4b-107">Member</span><span class="sxs-lookup"><span data-stu-id="1fe4b-107">Members</span></span>

<span data-ttu-id="1fe4b-108">Die **MSVM \_ syntheticmouse** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1fe4b-108">The **Msvm\_SyntheticMouse** class has these types of members:</span></span>

-   [<span data-ttu-id="1fe4b-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="1fe4b-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="1fe4b-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1fe4b-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1fe4b-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="1fe4b-111">Methods</span></span>

<span data-ttu-id="1fe4b-112">Die **MSVM \_ syntheticmouse** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-112">The **Msvm\_SyntheticMouse** class has these methods.</span></span>



| <span data-ttu-id="1fe4b-113">Methode</span><span class="sxs-lookup"><span data-stu-id="1fe4b-113">Method</span></span>                                                                 | <span data-ttu-id="1fe4b-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1fe4b-114">Description</span></span>                                                                   |
|:-----------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="1fe4b-115">**ClickButton**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-115">**ClickButton**</span></span>](clickbutton-msvm-syntheticmouse.md)                 | <span data-ttu-id="1fe4b-116">Simuliert einen Klick auf die Schaltfläche der angegebenen Geräte Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-116">Simulates a button click of the specified device button.</span></span><br/>           |
| <span data-ttu-id="1fe4b-117">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-117">**EnableDevice**</span></span>                                                       | <span data-ttu-id="1fe4b-118">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-118">This method is not supported.</span></span><br/>                                      |
| [<span data-ttu-id="1fe4b-119">**GetButtonState**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-119">**GetButtonState**</span></span>](getbuttonstate-msvm-syntheticmouse.md)           | <span data-ttu-id="1fe4b-120">Ruft den aktuellen Zustand der angegebenen Geräte Schaltfläche ab.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-120">Retrieves the current state of the specified device button.</span></span><br/>        |
| <span data-ttu-id="1fe4b-121">**Onlinedevice**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-121">**OnlineDevice**</span></span>                                                       | <span data-ttu-id="1fe4b-122">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-122">This method is not supported.</span></span><br/>                                      |
| <span data-ttu-id="1fe4b-123">**Inaktiven Geräte**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-123">**QuiesceDevice**</span></span>                                                      | <span data-ttu-id="1fe4b-124">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-124">This method is not supported.</span></span><br/>                                      |
| [<span data-ttu-id="1fe4b-125">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-125">**RequestStateChange**</span></span>](msvm-syntheticmouse-requeststatechange.md)   | <span data-ttu-id="1fe4b-126">Fordert eine Statusänderung an.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-126">Requests a state change</span></span><br/>                                            |
| [<span data-ttu-id="1fe4b-127">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-127">**Reset**</span></span>](msvm-syntheticmouse-reset.md)                             | <span data-ttu-id="1fe4b-128">Setzt das Gerät zurück.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-128">Resets the device.</span></span><br/>                                                 |
| <span data-ttu-id="1fe4b-129">**Restoreproperties**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-129">**RestoreProperties**</span></span>                                                  | <span data-ttu-id="1fe4b-130">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-130">This method is not supported.</span></span><br/>                                      |
| <span data-ttu-id="1fe4b-131">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-131">**SaveProperties**</span></span>                                                     | <span data-ttu-id="1fe4b-132">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-132">This method is not supported.</span></span><br/>                                      |
| [<span data-ttu-id="1fe4b-133">**"Settabsoluteposition"**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-133">**SetAbsolutePosition**</span></span>](setabsoluteposition-msvm-syntheticmouse.md) | <span data-ttu-id="1fe4b-134">Legt die horizontale und vertikale Position des Mauszeigers fest.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-134">Sets the horizontal and vertical position of the mouse cursor.</span></span><br/>     |
| [<span data-ttu-id="1fe4b-135">**SetButtonState**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-135">**SetButtonState**</span></span>](setbuttonstate-msvm-syntheticmouse.md)           | <span data-ttu-id="1fe4b-136">Legt den aktuellen Zustand der angegebenen Geräte Schaltfläche fest.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-136">Sets the current state of the specified device button.</span></span><br/>             |
| <span data-ttu-id="1fe4b-137">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-137">**SetPowerState**</span></span>                                                      | <span data-ttu-id="1fe4b-138">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-138">This method is not supported.</span></span><br/>                                      |
| [<span data-ttu-id="1fe4b-139">**Setscrollposition**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-139">**SetScrollPosition**</span></span>](setscrollposition-msvm-syntheticmouse.md)     | <span data-ttu-id="1fe4b-140">Legt die z-Koordinate des Steuer Elements für das Mausrad fest.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-140">Sets the z-coordinate of the wheel control of the pointing device.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="1fe4b-141">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1fe4b-141">Properties</span></span>

<span data-ttu-id="1fe4b-142">Die **MSVM- \_ syntheticmouse** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-142">The **Msvm\_SyntheticMouse** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1fe4b-143">**Absolutekoordinaten**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-143">**AbsoluteCoordinates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fe4b-144">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1fe4b-144">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1fe4b-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fe4b-146">Gibt an, ob das Gerät mit absoluten oder relativen Koordinaten arbeitet.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-146">Indicates whether the device operates on absolute or relative coordinates.</span></span>



| <span data-ttu-id="1fe4b-147">Wert</span><span class="sxs-lookup"><span data-stu-id="1fe4b-147">Value</span></span>                                                                                | <span data-ttu-id="1fe4b-148">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="1fe4b-148">Meaning</span></span>                                           |
|--------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="1fe4b-149"><dt>**Fall**</dt></span><span class="sxs-lookup"><span data-stu-id="1fe4b-149"><dt>**True**</dt></span></span> </dl>  | <span data-ttu-id="1fe4b-150">Die Koordinaten des Geräts sind absolut.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-150">The device's coordinates are absolute.</span></span><br/> |
| <dl> <span data-ttu-id="1fe4b-151"><dt>**False**</dt></span><span class="sxs-lookup"><span data-stu-id="1fe4b-151"><dt>**False**</dt></span></span> </dl> | <span data-ttu-id="1fe4b-152">Die Koordinaten des Geräts sind relativ.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-152">The device's coordinates are relative.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1fe4b-153">**Additionalavailability**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-153">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fe4b-154">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="1fe4b-154">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-155">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1fe4b-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fe4b-156">Alle zusätzlichen Verfügbarkeit und den Status des Geräts, außer den in der **Availability** -Eigenschaft angegebenen.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-156">Any additional availability and status of the device, beyond that specified in the **Availability** property.</span></span> <span data-ttu-id="1fe4b-157">Die **Availability** -Eigenschaft gibt den primären Status und die Verfügbarkeit des Geräts an.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-157">The **Availability** property denotes the primary status and availability of the device.</span></span> <span data-ttu-id="1fe4b-158">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-158">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="1fe4b-159">Wert</span><span class="sxs-lookup"><span data-stu-id="1fe4b-159">Value</span></span>                                                                          | <span data-ttu-id="1fe4b-160">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="1fe4b-160">Meaning</span></span>                   |
|--------------------------------------------------------------------------------|---------------------------|
| <dl> <dt>{6}</dt> </dl> | <span data-ttu-id="1fe4b-161">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="1fe4b-161">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1fe4b-162">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-162">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fe4b-163">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-164">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1fe4b-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fe4b-165">Die primäre Verfügbarkeit und den Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-165">The primary availability and status of the device.</span></span> <span data-ttu-id="1fe4b-166">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-166">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="1fe4b-167">Wert</span><span class="sxs-lookup"><span data-stu-id="1fe4b-167">Value</span></span>                                                                        | <span data-ttu-id="1fe4b-168">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="1fe4b-168">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="1fe4b-169"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="1fe4b-169"><dt>6</dt></span></span> </dl> | <span data-ttu-id="1fe4b-170">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="1fe4b-170">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1fe4b-171">**Availablerequestedstates**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-171">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fe4b-172">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="1fe4b-172">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-173">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1fe4b-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fe4b-174">Gibt die möglichen Werte für den *requestedstate* -Parameter der **requestStateChange** -Methode an.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-174">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="1fe4b-175">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-175">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="1fe4b-176">**Caption**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-176">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fe4b-177">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-178">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1fe4b-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fe4b-179">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-179">A short description of the object.</span></span> <span data-ttu-id="1fe4b-180">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-180">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1fe4b-181">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-181">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fe4b-182">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-183">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1fe4b-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fe4b-184">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-184">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="1fe4b-185">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-185">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="1fe4b-186">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-186">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="1fe4b-187"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="1fe4b-187"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-188"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="1fe4b-188"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-189"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Kommunikation OK** (2)</span><span class="sxs-lookup"><span data-stu-id="1fe4b-189"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-190"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Verlorene Kommunikation** (3)</span><span class="sxs-lookup"><span data-stu-id="1fe4b-190"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-191"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Kein Kontakt** (4)</span><span class="sxs-lookup"><span data-stu-id="1fe4b-191"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-192"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="1fe4b-192"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-193"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="1fe4b-193"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="1fe4b-194">)</span><span class="sxs-lookup"><span data-stu-id="1fe4b-194">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1fe4b-195">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-195">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fe4b-196">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-197">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1fe4b-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-198">Qualifizierer: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="1fe4b-198">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="1fe4b-199">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer-Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-199">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="1fe4b-200">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-200">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span> <span data-ttu-id="1fe4b-201">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-201">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="1fe4b-202">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-202">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fe4b-203">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-204">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1fe4b-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fe4b-205">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-205">A description of the object.</span></span> <span data-ttu-id="1fe4b-206">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-206">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1fe4b-207">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-207">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fe4b-208">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-209">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1fe4b-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fe4b-210">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-210">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="1fe4b-211">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-211">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="1fe4b-212">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-212">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="1fe4b-213"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (0)</span><span class="sxs-lookup"><span data-stu-id="1fe4b-213"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-214"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Keine zusätzlichen Informationen** (1)</span><span class="sxs-lookup"><span data-stu-id="1fe4b-214"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-215"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Betont** (2)</span><span class="sxs-lookup"><span data-stu-id="1fe4b-215"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-216"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Vorhersagefehler** (3)</span><span class="sxs-lookup"><span data-stu-id="1fe4b-216"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-217"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Nicht BEHEB barer Fehler** (4)</span><span class="sxs-lookup"><span data-stu-id="1fe4b-217"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-218"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Unterstützende Entität in Error** (5)</span><span class="sxs-lookup"><span data-stu-id="1fe4b-218"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-219"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="1fe4b-219"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-220"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="1fe4b-220"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="1fe4b-221">)</span><span class="sxs-lookup"><span data-stu-id="1fe4b-221">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1fe4b-222">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-222">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fe4b-223">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-224">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1fe4b-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-225">Qualifizierer: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="1fe4b-225">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="1fe4b-226">Eine Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-226">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="1fe4b-227">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist immer auf "Microsoft:*GUID*" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-227">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*GUID*".</span></span>

</dd> <dt>

<span data-ttu-id="1fe4b-228">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-228">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fe4b-229">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-230">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1fe4b-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fe4b-231">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-231">A display name for the object.</span></span> <span data-ttu-id="1fe4b-232">Mit dieser Eigenschaft kann jede Instanz zusätzlich zu ihren Schlüsseleigenschaften, Identitätsdaten und Beschreibungs Informationen einen anzeigen Amen definieren.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-232">This property allows each instance to define a display name in addition to its key properties, identity data, and description information.</span></span> <span data-ttu-id="1fe4b-233">Die [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) -Eigenschaft der **CIM \_ ManagedSystemElement** -Klasse wird auch als Anzeige Name definiert.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-233">The [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) property of the **CIM\_ManagedSystemElement** class is also defined as a display name.</span></span> <span data-ttu-id="1fe4b-234">Sie wird jedoch häufig als Schlüssel untergeordnet eingestuft.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-234">But, it is often subclassed to be a Key.</span></span> <span data-ttu-id="1fe4b-235">Es ist nicht sinnvoll, dass dieselbe Eigenschaft ohne Inkonsistenzen sowohl Identität als auch einen anzeigen Amen vermitteln kann.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-235">It is not reasonable that the same property can convey both identity and a display name, without inconsistencies.</span></span> <span data-ttu-id="1fe4b-236">Wenn [**Name**](msvm-keyboard.md) vorhanden und kein Schlüssel ist (z. b. für Instanzen von LogicalDevice), können dieselben Informationen in den Eigenschaften **Name** und **ElementName** vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-236">Where [**Name**](msvm-keyboard.md) exists and is not a Key (such as for instances of LogicalDevice), the same information can be present in both the **Name** and **ElementName** properties.</span></span> <span data-ttu-id="1fe4b-237">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-237">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1fe4b-238">**Enableddefault**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-238">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fe4b-239">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-239">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-240">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1fe4b-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fe4b-241">Die Standard-oder Startkonfiguration eines Administrators für den **enabledstate** eines Elements.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-241">An administrator's default or startup configuration for the **EnabledState** of an element.</span></span> <span data-ttu-id="1fe4b-242">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-242">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1fe4b-243">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-243">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fe4b-244">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-244">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-245">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1fe4b-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fe4b-246">Der aktivierte und deaktivierte Status eines Elements.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-246">The enabled and disabled states of an element.</span></span> <span data-ttu-id="1fe4b-247">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-247">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="1fe4b-248">Wert</span><span class="sxs-lookup"><span data-stu-id="1fe4b-248">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="1fe4b-249">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="1fe4b-249">Meaning</span></span>                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="1fe4b-250"><dt>**Aktiviert**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="1fe4b-250"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="1fe4b-251">Der virtuelle Gastcomputer unterstützt eine synthetische Maus.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-251">The guest virtual machine supports a synthetic mouse.</span></span><br/>         |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="1fe4b-252"><dt>**Deaktiviert**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="1fe4b-252"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="1fe4b-253">Der virtuelle Gastcomputer unterstützt keine synthetische Maus.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-253">The guest virtual machine does not support a synthetic mouse.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1fe4b-254">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-254">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fe4b-255">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1fe4b-255">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-256">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1fe4b-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fe4b-257">Gibt an, ob der in **LastErrorCode** gemeldete Fehler jetzt gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-257">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="1fe4b-258">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-258">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1fe4b-259">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-259">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fe4b-260">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-260">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-261">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1fe4b-261">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fe4b-262">Eine Zeichenfolge, die weitere Informationen über den Fehler enthält, der in **LastErrorCode** aufgezeichnet wurde, sowie Informationen über alle Maßnahmen, die ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-262">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="1fe4b-263">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-263">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1fe4b-264">**Händigkeit**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-264">**Handedness**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fe4b-265">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-265">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-266">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1fe4b-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fe4b-267">Die Konfiguration des Zeige Geräts für den rechten oder linken Vorgang.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-267">The configuration of the pointing device for right-hand or left-hand operation.</span></span> <span data-ttu-id="1fe4b-268">Diese Eigenschaft wird von [**CIM \_ pointingdevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-268">This property is inherited from [**CIM\_PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span></span>



| <span data-ttu-id="1fe4b-269">Wert</span><span class="sxs-lookup"><span data-stu-id="1fe4b-269">Value</span></span>                                                                        | <span data-ttu-id="1fe4b-270">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="1fe4b-270">Meaning</span></span>                            |
|------------------------------------------------------------------------------|------------------------------------|
| <dl> <span data-ttu-id="1fe4b-271"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="1fe4b-271"><dt>0</dt></span></span> </dl> | <span data-ttu-id="1fe4b-272">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="1fe4b-272">Unknown</span></span><br/>                 |
| <dl> <span data-ttu-id="1fe4b-273"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="1fe4b-273"><dt>1</dt></span></span> </dl> | <span data-ttu-id="1fe4b-274">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="1fe4b-274">Not applicable.</span></span><br/>         |
| <dl> <span data-ttu-id="1fe4b-275"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="1fe4b-275"><dt>2</dt></span></span> </dl> | <span data-ttu-id="1fe4b-276">Rechter übergebenen Vorgang.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-276">Right handed operation.</span></span><br/> |
| <dl> <span data-ttu-id="1fe4b-277"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="1fe4b-277"><dt>3</dt></span></span> </dl> | <span data-ttu-id="1fe4b-278">Links übergebenen Vorgang.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-278">Left handed operation.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="1fe4b-279">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-279">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fe4b-280">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-280">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-281">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1fe4b-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fe4b-282">Der aktuelle Zustand des Elements.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-282">The current health of the element.</span></span> <span data-ttu-id="1fe4b-283">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-283">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1fe4b-284">**HorizontalPosition**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-284">**HorizontalPosition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fe4b-285">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-285">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-286">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1fe4b-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fe4b-287">Die absolute x-Koordinate des Zeige Geräts.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-287">The absolute x-coordinate of the pointing device.</span></span>

</dd> <dt>

<span data-ttu-id="1fe4b-288">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-288">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fe4b-289">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="1fe4b-289">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-290">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1fe4b-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fe4b-291">Ein Array von Freiform-Zeichen folgen, die Erklärungen und Details hinter den Einträgen im " [**OtherIdentifyingInfo**](msvm-keyboard.md) "-Array bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-291">An array of free-form strings that provide explanations and details behind the entries in the [**OtherIdentifyingInfo**](msvm-keyboard.md) array.</span></span> <span data-ttu-id="1fe4b-292">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-292">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="1fe4b-293">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-293">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fe4b-294">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-294">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-295">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1fe4b-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fe4b-296">Das Datum und die Uhrzeit der Erstellung der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-296">The date and time at which the virtual machine was created.</span></span> <span data-ttu-id="1fe4b-297">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-297">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1fe4b-298">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-298">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fe4b-299">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-300">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1fe4b-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-301">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-301">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="1fe4b-302">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-302">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="1fe4b-303">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-303">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1fe4b-304">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-304">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fe4b-305">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1fe4b-305">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-306">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1fe4b-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fe4b-307">Gibt an, ob das Gerät gesperrt ist, und verhindert Benutzereingaben oder-Ausgaben.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-307">Indicates whether the device is locked, preventing user input or output.</span></span> <span data-ttu-id="1fe4b-308">Diese Eigenschaft wird von [**CIM \_ userdevice**](/windows/desktop/CIMWin32Prov/cim-userdevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-308">This property is inherited from [**CIM\_UserDevice**](/windows/desktop/CIMWin32Prov/cim-userdevice).</span></span>

</dd> <dt>

<span data-ttu-id="1fe4b-309">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-309">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fe4b-310">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-310">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-311">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1fe4b-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fe4b-312">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-312">The last error code reported by the logical device.</span></span> <span data-ttu-id="1fe4b-313">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-313">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1fe4b-314">**Maxquiescetime**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-314">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fe4b-315">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-315">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-316">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1fe4b-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fe4b-317">Diese Eigenschaft ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-317">This property has been deprecated.</span></span> <span data-ttu-id="1fe4b-318">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-318">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="1fe4b-319">**Name**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-319">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fe4b-320">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-321">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1fe4b-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-322">Qualifizierer: **maxlen** (1024)</span><span class="sxs-lookup"><span data-stu-id="1fe4b-322">Qualifiers: **MaxLen** (1024)</span></span>
</dt> </dl>

<span data-ttu-id="1fe4b-323">Die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-323">The label by which the object is known.</span></span> <span data-ttu-id="1fe4b-324">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-324">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="1fe4b-325">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-325">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1fe4b-326">**Anzahl von Schaltflächen**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-326">**NumberOfButtons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fe4b-327">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-327">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-328">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1fe4b-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fe4b-329">Die Anzahl der Schaltflächen auf dem Zeigegerät.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-329">The number of buttons on the pointing device.</span></span> <span data-ttu-id="1fe4b-330">Diese Eigenschaft wird von [**CIM \_ pointingdevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-330">This property is inherited from [**CIM\_PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span></span>

</dd> <dt>

<span data-ttu-id="1fe4b-331">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-331">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fe4b-332">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-332">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-333">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1fe4b-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fe4b-334">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-334">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="1fe4b-335">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-335">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="1fe4b-336">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-336">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="1fe4b-337"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="1fe4b-337"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-338"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="1fe4b-338"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-339"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Wartung** (2)</span><span class="sxs-lookup"><span data-stu-id="1fe4b-339"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-340"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>Wird **gestartet** (3)</span><span class="sxs-lookup"><span data-stu-id="1fe4b-340"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-341"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>Wird **beendet (4** )</span><span class="sxs-lookup"><span data-stu-id="1fe4b-341"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-342"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Beendet** (5)</span><span class="sxs-lookup"><span data-stu-id="1fe4b-342"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-343"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abgebrochen** (6)</span><span class="sxs-lookup"><span data-stu-id="1fe4b-343"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-344"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Ruhende** (7)</span><span class="sxs-lookup"><span data-stu-id="1fe4b-344"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-345"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Abgeschlossen** (8)</span><span class="sxs-lookup"><span data-stu-id="1fe4b-345"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-346"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrieren** (9)</span><span class="sxs-lookup"><span data-stu-id="1fe4b-346"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-347"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Migration** (10)</span><span class="sxs-lookup"><span data-stu-id="1fe4b-347"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-348"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migration** (11)</span><span class="sxs-lookup"><span data-stu-id="1fe4b-348"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-349"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotts** (12)</span><span class="sxs-lookup"><span data-stu-id="1fe4b-349"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-350"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Herunter** fahren (13)</span><span class="sxs-lookup"><span data-stu-id="1fe4b-350"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-351"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span><span class="sxs-lookup"><span data-stu-id="1fe4b-351"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-352"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Übergang** (15)</span><span class="sxs-lookup"><span data-stu-id="1fe4b-352"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-353"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Dienst** (16)</span><span class="sxs-lookup"><span data-stu-id="1fe4b-353"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-354"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="1fe4b-354"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-355"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="1fe4b-355"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="1fe4b-356">)</span><span class="sxs-lookup"><span data-stu-id="1fe4b-356">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1fe4b-357">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-357">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fe4b-358">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="1fe4b-358">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-359">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1fe4b-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fe4b-360">Der aktuelle Status des Elements.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-360">The current status of the element.</span></span> <span data-ttu-id="1fe4b-361">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-361">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1fe4b-362">**Otherenabledstate**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-362">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fe4b-363">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-363">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-364">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1fe4b-364">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fe4b-365">Der aktivierte oder deaktivierte Status des Elements, wenn die **enabledstate** -Eigenschaft auf 1 (Sonstiges) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-365">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="1fe4b-366">Diese Eigenschaft muss auf **null** festgelegt werden, wenn **enabledstate** ein anderer Wert als 1 ist.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-366">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="1fe4b-367">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-367">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1fe4b-368">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-368">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fe4b-369">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="1fe4b-369">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-370">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1fe4b-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fe4b-371">Alle zusätzlichen Daten über Geräte-ID-Informationen, die zur Identifizierung eines logischen Geräts verwendet werden könnten.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-371">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="1fe4b-372">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-372">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="1fe4b-373">**Pointingtype**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-373">**PointingType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fe4b-374">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-374">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-375">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1fe4b-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fe4b-376">Der Typ des Zeige Geräts.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-376">The type of pointing device.</span></span> <span data-ttu-id="1fe4b-377">Diese Eigenschaft wird von [**CIM \_ pointingdevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-377">This property is inherited from [**CIM\_PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span></span>



| <span data-ttu-id="1fe4b-378">Wert</span><span class="sxs-lookup"><span data-stu-id="1fe4b-378">Value</span></span>                                                                        | <span data-ttu-id="1fe4b-379">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="1fe4b-379">Meaning</span></span>          |
|------------------------------------------------------------------------------|------------------|
| <dl> <span data-ttu-id="1fe4b-380"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="1fe4b-380"><dt>3</dt></span></span> </dl> | <span data-ttu-id="1fe4b-381">Maus</span><span class="sxs-lookup"><span data-stu-id="1fe4b-381">Mouse</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1fe4b-382">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-382">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fe4b-383">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="1fe4b-383">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-384">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1fe4b-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fe4b-385">Die Energie Verwaltungsfunktionen des Geräts.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-385">The power management capabilities of the device.</span></span> <span data-ttu-id="1fe4b-386">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-386">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1fe4b-387">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-387">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fe4b-388">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1fe4b-388">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-389">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1fe4b-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fe4b-390">Gibt an, ob das Gerät Energie gesteuert werden kann.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-390">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="1fe4b-391">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-391">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1fe4b-392">**Poweronhours**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-392">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fe4b-393">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-393">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-394">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1fe4b-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fe4b-395">Gibt an, wie viele aufeinanderfolgende Stunden dieses Gerät seit dem letzten Strom Umgebung eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-395">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="1fe4b-396">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-396">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1fe4b-397">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-397">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fe4b-398">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-398">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-399">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1fe4b-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fe4b-400">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-400">Provides high level status information.</span></span> <span data-ttu-id="1fe4b-401">Diese Eigenschaft sollte in Verbindung mit der Eigenschaft **detailedstatus** verwendet werden, um einen hohen und detaillierten Integritäts Status des Elements und seiner unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-401">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="1fe4b-402">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-402">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="1fe4b-403">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-403">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="1fe4b-404"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="1fe4b-404"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-405"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="1fe4b-405"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-406"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (2** )</span><span class="sxs-lookup"><span data-stu-id="1fe4b-406"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-407"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Fehler** (3)</span><span class="sxs-lookup"><span data-stu-id="1fe4b-407"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-408"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="1fe4b-408"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-409"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="1fe4b-409"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="1fe4b-410">)</span><span class="sxs-lookup"><span data-stu-id="1fe4b-410">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1fe4b-411">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-411">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fe4b-412">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-412">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-413">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1fe4b-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fe4b-414">Der zuletzt angeforderte oder gewünschte Zustand für das Element.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-414">The last requested or desired state for the element.</span></span> <span data-ttu-id="1fe4b-415">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-415">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="1fe4b-416">Wert</span><span class="sxs-lookup"><span data-stu-id="1fe4b-416">Value</span></span>                                                                         | <span data-ttu-id="1fe4b-417">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="1fe4b-417">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="1fe4b-418"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="1fe4b-418"><dt>12</dt></span></span> </dl> | <span data-ttu-id="1fe4b-419">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="1fe4b-419">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1fe4b-420">**Auflösung**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-420">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fe4b-421">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-421">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-422">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1fe4b-422">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fe4b-423">Die nach Verfolgungs Auflösung des Zeige Geräts in Zählungen pro Zoll.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-423">The tracking resolution of the pointing device, in counts per inch.</span></span> <span data-ttu-id="1fe4b-424">Diese Eigenschaft wird von [**CIM \_ pointingdevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-424">This property is inherited from [**CIM\_PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span></span>

</dd> <dt>

<span data-ttu-id="1fe4b-425">**Scrollposition**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-425">**ScrollPosition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fe4b-426">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-426">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-427">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1fe4b-427">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-428">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Mickeys")</span><span class="sxs-lookup"><span data-stu-id="1fe4b-428">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Mickeys")</span></span>
</dt> </dl>

<span data-ttu-id="1fe4b-429">Die z-Koordinaten Position des Maus Geräts.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-429">The z-coordinate position of the mouse device.</span></span>

</dd> <dt>

<span data-ttu-id="1fe4b-430">**Status**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-430">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fe4b-431">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-431">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-432">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1fe4b-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fe4b-433">Der aktuelle Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-433">The current status of the object.</span></span> <span data-ttu-id="1fe4b-434">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-434">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1fe4b-435">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-435">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fe4b-436">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="1fe4b-436">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-437">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1fe4b-437">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fe4b-438">Zeichen folgen, die die verschiedenen [**OperationalStatus**](msvm-bioselement.md) -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-438">Strings that describe the various [**OperationalStatus**](msvm-bioselement.md) array values.</span></span> <span data-ttu-id="1fe4b-439">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-439">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1fe4b-440">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-440">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fe4b-441">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-441">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-442">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1fe4b-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fe4b-443">Der aktuelle Zustand des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-443">The current state of the logical device.</span></span> <span data-ttu-id="1fe4b-444">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-444">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1fe4b-445">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-445">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fe4b-446">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-446">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-447">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1fe4b-447">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-448">Qualifizierer: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="1fe4b-448">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="1fe4b-449">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-449">The creation class name of the scoping system.</span></span> <span data-ttu-id="1fe4b-450">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-450">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="1fe4b-451">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-451">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fe4b-452">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-452">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-453">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1fe4b-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-454">Qualifizierer: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="1fe4b-454">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="1fe4b-455">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-455">The name of the scoping system.</span></span> <span data-ttu-id="1fe4b-456">Dieser Wert entspricht dem Wert der [**Name**](msvm-computersystem.md) -Eigenschaft der **MSVM \_ Computersystem** -Klasse für die Bereichs bezogene virtuelle Maschine.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-456">This value corresponds to the value of the [**Name**](msvm-computersystem.md) property of the **Msvm\_ComputerSystem** class for the scoping virtual machine.</span></span> <span data-ttu-id="1fe4b-457">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-457">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="1fe4b-458">**Timeoflaststatechange**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-458">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fe4b-459">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-459">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-460">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1fe4b-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fe4b-461">Das Datum oder die Uhrzeit, zu dem der aktivierte Status des Elements zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-461">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="1fe4b-462">Wenn der Zustand des Elements nicht geändert wurde und diese Eigenschaft aufgefüllt ist, muss Sie auf einen Wert von 0 Intervall festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-462">If the state of the element has not changed and this property is populated, then it must be set to a 0 interval value.</span></span> <span data-ttu-id="1fe4b-463">Wenn eine Zustandsänderung angefordert, aber abgelehnt oder noch nicht verarbeitet wurde, darf die Eigenschaft nicht aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-463">If a state change was requested, but rejected or not yet processed, the property must not be updated.</span></span> <span data-ttu-id="1fe4b-464">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-464">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="1fe4b-465">**Totalpoweronhours**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-465">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fe4b-466">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-466">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-467">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1fe4b-467">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fe4b-468">Die Gesamtanzahl der Stunden, für die dieses Gerät eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-468">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="1fe4b-469">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-469">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1fe4b-470">**Transitioningumstate**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-470">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fe4b-471">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-471">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-472">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1fe4b-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fe4b-473">Gibt den Ziel Status an, in den die-Instanz übergeht.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-473">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="1fe4b-474">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-474">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="1fe4b-475">**VerticalPosition**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-475">**VerticalPosition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fe4b-476">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-476">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1fe4b-477">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1fe4b-477">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1fe4b-478">Die absolute y-Koordinate des Zeige Geräts.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-478">The absolute y-coordinate of the pointing device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1fe4b-479">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1fe4b-479">Remarks</span></span>

<span data-ttu-id="1fe4b-480">Der Zugriff auf die **MSVM \_ syntheticmouse** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="1fe4b-480">Access to the **Msvm\_SyntheticMouse** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="1fe4b-481">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="1fe4b-481">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="1fe4b-482">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1fe4b-482">Requirements</span></span>



| <span data-ttu-id="1fe4b-483">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1fe4b-483">Requirement</span></span> | <span data-ttu-id="1fe4b-484">Wert</span><span class="sxs-lookup"><span data-stu-id="1fe4b-484">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fe4b-485">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1fe4b-485">Minimum supported client</span></span><br/> | <span data-ttu-id="1fe4b-486">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1fe4b-486">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1fe4b-487">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1fe4b-487">Minimum supported server</span></span><br/> | <span data-ttu-id="1fe4b-488">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1fe4b-488">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1fe4b-489">Namespace</span><span class="sxs-lookup"><span data-stu-id="1fe4b-489">Namespace</span></span><br/>                | <span data-ttu-id="1fe4b-490">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="1fe4b-490">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1fe4b-491">MOF</span><span class="sxs-lookup"><span data-stu-id="1fe4b-491">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1fe4b-492"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1fe4b-492"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1fe4b-493">DLL</span><span class="sxs-lookup"><span data-stu-id="1fe4b-493">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1fe4b-494"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1fe4b-494"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1fe4b-495">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1fe4b-495">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fe4b-496">**CIM- \_ pointingdevice**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-496">**CIM\_PointingDevice**</span></span>](cim-pointingdevice.md)
</dt> <dt>

[<span data-ttu-id="1fe4b-497">**CIM- \_ pointingdevice**</span><span class="sxs-lookup"><span data-stu-id="1fe4b-497">**CIM\_PointingDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-pointingdevice)
</dt> <dt>

[<span data-ttu-id="1fe4b-498">Eingabe Klassen</span><span class="sxs-lookup"><span data-stu-id="1fe4b-498">Input Classes</span></span>](input-classes.md)
</dt> </dl>

 

