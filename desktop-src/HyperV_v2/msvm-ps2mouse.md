---
description: Stellt ein PS2-Mausgerät dar.
ms.assetid: 5e02ec15-95e6-4d82-833e-a48ca117a890
title: Msvm_Ps2Mouse-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Ps2Mouse
- Msvm_Ps2Mouse.SetPowerState
- Msvm_Ps2Mouse.EnableDevice
- Msvm_Ps2Mouse.OnlineDevice
- Msvm_Ps2Mouse.QuiesceDevice
- Msvm_Ps2Mouse.SaveProperties
- Msvm_Ps2Mouse.RestoreProperties
- Msvm_Ps2Mouse.InstanceID
- Msvm_Ps2Mouse.Caption
- Msvm_Ps2Mouse.Description
- Msvm_Ps2Mouse.ElementName
- Msvm_Ps2Mouse.InstallDate
- Msvm_Ps2Mouse.Name
- Msvm_Ps2Mouse.OperationalStatus
- Msvm_Ps2Mouse.StatusDescriptions
- Msvm_Ps2Mouse.Status
- Msvm_Ps2Mouse.HealthState
- Msvm_Ps2Mouse.CommunicationStatus
- Msvm_Ps2Mouse.DetailedStatus
- Msvm_Ps2Mouse.OperatingStatus
- Msvm_Ps2Mouse.PrimaryStatus
- Msvm_Ps2Mouse.EnabledState
- Msvm_Ps2Mouse.OtherEnabledState
- Msvm_Ps2Mouse.RequestedState
- Msvm_Ps2Mouse.EnabledDefault
- Msvm_Ps2Mouse.TimeOfLastStateChange
- Msvm_Ps2Mouse.AvailableRequestedStates
- Msvm_Ps2Mouse.TransitioningToState
- Msvm_Ps2Mouse.SystemCreationClassName
- Msvm_Ps2Mouse.SystemName
- Msvm_Ps2Mouse.CreationClassName
- Msvm_Ps2Mouse.DeviceID
- Msvm_Ps2Mouse.PowerManagementSupported
- Msvm_Ps2Mouse.PowerManagementCapabilities
- Msvm_Ps2Mouse.Availability
- Msvm_Ps2Mouse.StatusInfo
- Msvm_Ps2Mouse.LastErrorCode
- Msvm_Ps2Mouse.ErrorDescription
- Msvm_Ps2Mouse.ErrorCleared
- Msvm_Ps2Mouse.OtherIdentifyingInfo
- Msvm_Ps2Mouse.PowerOnHours
- Msvm_Ps2Mouse.TotalPowerOnHours
- Msvm_Ps2Mouse.IdentifyingDescriptions
- Msvm_Ps2Mouse.AdditionalAvailability
- Msvm_Ps2Mouse.MaxQuiesceTime
- Msvm_Ps2Mouse.IsLocked
- Msvm_Ps2Mouse.PointingType
- Msvm_Ps2Mouse.NumberOfButtons
- Msvm_Ps2Mouse.Handedness
- Msvm_Ps2Mouse.Resolution
- Msvm_Ps2Mouse.AbsoluteCoordinates
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d25d168b85a79c5212afc719ce6ec83ca9780395
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345778"
---
# <a name="msvm_ps2mouse-class"></a><span data-ttu-id="c6f8c-103">MSVM \_ Ps2Mouse-Klasse</span><span class="sxs-lookup"><span data-stu-id="c6f8c-103">Msvm\_Ps2Mouse class</span></span>

<span data-ttu-id="c6f8c-104">Stellt ein PS2-Mausgerät dar.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-104">Represents a PS2 mouse device.</span></span> <span data-ttu-id="c6f8c-105">Instanzen dieser Klasse sind logische Geräte, die immer auf einem virtuellen Computer vorhanden sind und daher nicht über einen Ressourcenpool zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-105">Instances of this class are logical devices that are always present in a virtual machine, and thus are not allocated through a resource pool.</span></span> <span data-ttu-id="c6f8c-106">Eine Instanz ist immer auf einem virtuellen Computer vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-106">One instance is always present in a virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="c6f8c-107">Diese Klasse ist für virtuelle Maschinen der Generation 2 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-107">This class is not available to generation 2 virtual machines.</span></span>

 

<span data-ttu-id="c6f8c-108">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6f8c-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6f8c-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Ps2Mouse : CIM_PointingDevice
{
  string   InstanceID;
  string   Caption = "Mouse";
  string   Description = "Microsoft Emulated Mouse";
  string   ElementName = "Mouse";
  datetime InstallDate;
  string   Name = "Mouse";
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = "OK";
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
  string   CreationClassName = "Msvm_PS2Mouse";
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
  uint16   AdditionalAvailability[] = 6;
  uint64   MaxQuiesceTime;
  boolean  IsLocked = False;
  uint16   PointingType = 3;
  uint8    NumberOfButtons = 5;
  uint16   Handedness = 2;
  uint32   Resolution;
  boolean  AbsoluteCoordinates = False;
};
```

## <a name="members"></a><span data-ttu-id="c6f8c-110">Member</span><span class="sxs-lookup"><span data-stu-id="c6f8c-110">Members</span></span>

<span data-ttu-id="c6f8c-111">Die **MSVM \_ Ps2Mouse** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c6f8c-111">The **Msvm\_Ps2Mouse** class has these types of members:</span></span>

-   [<span data-ttu-id="c6f8c-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="c6f8c-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="c6f8c-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c6f8c-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c6f8c-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="c6f8c-114">Methods</span></span>

<span data-ttu-id="c6f8c-115">Die **MSVM- \_ Ps2Mouse** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-115">The **Msvm\_Ps2Mouse** class has these methods.</span></span>



| <span data-ttu-id="c6f8c-116">Methode</span><span class="sxs-lookup"><span data-stu-id="c6f8c-116">Method</span></span>                                                           | <span data-ttu-id="c6f8c-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c6f8c-117">Description</span></span>                                                                                           |
|:-----------------------------------------------------------------|:------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c6f8c-118">**ClickButton**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-118">**ClickButton**</span></span>](clickbutton-msvm-ps2mouse.md)                 | <span data-ttu-id="c6f8c-119">Simuliert einen Schaltflächen Klick, eine aufgeschselnde Sequenz auf der angegebenen Geräte Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-119">Simulates a button click, a down-up sequence, on the specified device button.</span></span><br/>              |
| <span data-ttu-id="c6f8c-120">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-120">**EnableDevice**</span></span>                                                 | <span data-ttu-id="c6f8c-121">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-121">This method is not supported.</span></span><br/>                                                              |
| [<span data-ttu-id="c6f8c-122">**GetButtonState**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-122">**GetButtonState**</span></span>](getbuttonstate-msvm-ps2mouse.md)           | <span data-ttu-id="c6f8c-123">Ruft den aktuellen Zustand der angegebenen Geräte Schaltfläche ab.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-123">Retrieves the current state of the specified device button.</span></span><br/>                                |
| <span data-ttu-id="c6f8c-124">**Onlinedevice**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-124">**OnlineDevice**</span></span>                                                 | <span data-ttu-id="c6f8c-125">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-125">This method is not supported.</span></span><br/>                                                              |
| <span data-ttu-id="c6f8c-126">**Inaktiven Geräte**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-126">**QuiesceDevice**</span></span>                                                | <span data-ttu-id="c6f8c-127">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-127">This method is not supported.</span></span><br/>                                                              |
| [<span data-ttu-id="c6f8c-128">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-128">**RequestStateChange**</span></span>](msvm-ps2mouse-requeststatechange.md)   | <span data-ttu-id="c6f8c-129">Fordert eine Statusänderung an.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-129">Requests a state change.</span></span><br/>                                                                   |
| [<span data-ttu-id="c6f8c-130">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-130">**Reset**</span></span>](msvm-ps2mouse-reset.md)                             | <span data-ttu-id="c6f8c-131">Setzt das Gerät zurück.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-131">Resets the device.</span></span><br/>                                                                         |
| <span data-ttu-id="c6f8c-132">**Restoreproperties**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-132">**RestoreProperties**</span></span>                                            | <span data-ttu-id="c6f8c-133">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-133">This method is not supported.</span></span><br/>                                                              |
| <span data-ttu-id="c6f8c-134">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-134">**SaveProperties**</span></span>                                               | <span data-ttu-id="c6f8c-135">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-135">This method is not supported.</span></span><br/>                                                              |
| [<span data-ttu-id="c6f8c-136">**SetButtonState**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-136">**SetButtonState**</span></span>](setbuttonstate-msvm-ps2mouse.md)           | <span data-ttu-id="c6f8c-137">Legt den aktuellen Zustand der angegebenen Geräte Schaltfläche fest.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-137">Sets the current state of the specified device button.</span></span><br/>                                     |
| <span data-ttu-id="c6f8c-138">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-138">**SetPowerState**</span></span>                                                | <span data-ttu-id="c6f8c-139">Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-139">This method is not supported.</span></span><br/>                                                              |
| [<span data-ttu-id="c6f8c-140">**"Settrelativeposition"**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-140">**SetRelativePosition**</span></span>](setrelativeposition-msvm-ps2mouse.md) | <span data-ttu-id="c6f8c-141">Versetzt die Position des Mauszeigers um das angegebene horizontale und vertikale Delta.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-141">Offsets the position of the mouse pointer by the specified horizontal and vertical deltas.</span></span><br/> |
| [<span data-ttu-id="c6f8c-142">**Setscrollposition**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-142">**SetScrollPosition**</span></span>](setscrollposition-msvm-ps2mouse.md)     | <span data-ttu-id="c6f8c-143">Passt die z-Koordinate des Rad-Steuer Elements des Zeige Geräts an.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-143">Adjusts the z-coordinate of the wheel control of the pointing device.</span></span><br/>                      |



 

### <a name="properties"></a><span data-ttu-id="c6f8c-144">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c6f8c-144">Properties</span></span>

<span data-ttu-id="c6f8c-145">Die **MSVM- \_ Ps2Mouse** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-145">The **Msvm\_Ps2Mouse** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c6f8c-146">**Absolutekoordinaten**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-146">**AbsoluteCoordinates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6f8c-147">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="c6f8c-147">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6f8c-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c6f8c-149">Gibt an, ob das Gerät mit absoluten Koordinaten arbeitet.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-149">Indicates whether the device operates on absolute coordinates.</span></span> <span data-ttu-id="c6f8c-150">Wenn nicht festgelegt, sind die Koordinaten des Geräts relativ.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-150">If not set, the device's coordinates are relative.</span></span>

</dd> <dt>

<span data-ttu-id="c6f8c-151">**Additionalavailability**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-151">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6f8c-152">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="c6f8c-152">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6f8c-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c6f8c-154">Alle zusätzlichen Verfügbarkeit und den Status des Geräts, außer den in der **Availability** -Eigenschaft angegebenen.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-154">Any additional availability and status of the device, beyond that specified in the **Availability** property.</span></span> <span data-ttu-id="c6f8c-155">Die **Availability** -Eigenschaft gibt den primären Status und die Verfügbarkeit des Geräts an.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-155">The **Availability** property denotes the primary status and availability of the device.</span></span> <span data-ttu-id="c6f8c-156">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-156">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="c6f8c-157">Wert</span><span class="sxs-lookup"><span data-stu-id="c6f8c-157">Value</span></span>                                                                        | <span data-ttu-id="c6f8c-158">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c6f8c-158">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="c6f8c-159"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="c6f8c-159"><dt>6</dt></span></span> </dl> | <span data-ttu-id="c6f8c-160">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="c6f8c-160">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c6f8c-161">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-161">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6f8c-162">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-162">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-163">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6f8c-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c6f8c-164">Die primäre Verfügbarkeit und den Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-164">The primary availability and status of the device.</span></span> <span data-ttu-id="c6f8c-165">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-165">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="c6f8c-166">Wert</span><span class="sxs-lookup"><span data-stu-id="c6f8c-166">Value</span></span>                                                                        | <span data-ttu-id="c6f8c-167">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c6f8c-167">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="c6f8c-168"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="c6f8c-168"><dt>6</dt></span></span> </dl> | <span data-ttu-id="c6f8c-169">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="c6f8c-169">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c6f8c-170">**Availablerequestedstates**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-170">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6f8c-171">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="c6f8c-171">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-172">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6f8c-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c6f8c-173">Gibt die möglichen Werte für den *requestedstate* -Parameter der **requestStateChange** -Methode an.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-173">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="c6f8c-174">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-174">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c6f8c-175">**Caption**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-175">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6f8c-176">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-177">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6f8c-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c6f8c-178">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-178">A short description of the object.</span></span> <span data-ttu-id="c6f8c-179">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-179">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c6f8c-180">**Communicationstatus**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-180">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6f8c-181">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-181">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-182">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6f8c-182">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c6f8c-183">Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-183">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="c6f8c-184">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-184">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c6f8c-185">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-185">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="c6f8c-186"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="c6f8c-186"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-187"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="c6f8c-187"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-188"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Kommunikation OK** (2)</span><span class="sxs-lookup"><span data-stu-id="c6f8c-188"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-189"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Verlorene Kommunikation** (3)</span><span class="sxs-lookup"><span data-stu-id="c6f8c-189"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-190"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Kein Kontakt** (4)</span><span class="sxs-lookup"><span data-stu-id="c6f8c-190"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-191"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="c6f8c-191"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-192"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="c6f8c-192"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="c6f8c-193">)</span><span class="sxs-lookup"><span data-stu-id="c6f8c-193">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c6f8c-194">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-194">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6f8c-195">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-196">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6f8c-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-197">Qualifizierer: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="c6f8c-197">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="c6f8c-198">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer-Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-198">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="c6f8c-199">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-199">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span> <span data-ttu-id="c6f8c-200">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-200">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="c6f8c-201">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-201">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6f8c-202">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-203">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6f8c-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c6f8c-204">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-204">A description of the object.</span></span> <span data-ttu-id="c6f8c-205">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-205">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c6f8c-206">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-206">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6f8c-207">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-207">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-208">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6f8c-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c6f8c-209">Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-209">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="c6f8c-210">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-210">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c6f8c-211">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-211">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="c6f8c-212"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (0)</span><span class="sxs-lookup"><span data-stu-id="c6f8c-212"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-213"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Keine zusätzlichen Informationen** (1)</span><span class="sxs-lookup"><span data-stu-id="c6f8c-213"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-214"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Betont** (2)</span><span class="sxs-lookup"><span data-stu-id="c6f8c-214"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-215"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Vorhersagefehler** (3)</span><span class="sxs-lookup"><span data-stu-id="c6f8c-215"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-216"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Nicht BEHEB barer Fehler** (4)</span><span class="sxs-lookup"><span data-stu-id="c6f8c-216"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-217"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Unterstützende Entität in Error** (5)</span><span class="sxs-lookup"><span data-stu-id="c6f8c-217"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-218"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="c6f8c-218"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-219"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="c6f8c-219"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="c6f8c-220">)</span><span class="sxs-lookup"><span data-stu-id="c6f8c-220">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c6f8c-221">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-221">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6f8c-222">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-223">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6f8c-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-224">Qualifizierer: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="c6f8c-224">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="c6f8c-225">Eine Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-225">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="c6f8c-226">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist immer auf "Microsoft:*GUID*" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-226">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*GUID*".</span></span>

</dd> <dt>

<span data-ttu-id="c6f8c-227">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-227">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6f8c-228">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-229">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6f8c-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c6f8c-230">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-230">A display name for the object.</span></span> <span data-ttu-id="c6f8c-231">Mit dieser Eigenschaft kann jede Instanz zusätzlich zu ihren Schlüsseleigenschaften, Identitätsdaten und Beschreibungs Informationen einen anzeigen Amen definieren.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-231">This property allows each instance to define a display name in addition to its key properties, identity data, and description information.</span></span> <span data-ttu-id="c6f8c-232">Die [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) -Eigenschaft der **CIM \_ ManagedSystemElement** -Klasse wird auch als Anzeige Name definiert.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-232">The [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) property of the **CIM\_ManagedSystemElement** class is also defined as a display name.</span></span> <span data-ttu-id="c6f8c-233">Sie wird jedoch häufig als Schlüssel untergeordnet eingestuft.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-233">But, it is often subclassed to be a Key.</span></span> <span data-ttu-id="c6f8c-234">Es ist nicht sinnvoll, dass dieselbe Eigenschaft ohne Inkonsistenzen sowohl Identität als auch einen anzeigen Amen vermitteln kann.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-234">It is not reasonable that the same property can convey both identity and a display name, without inconsistencies.</span></span> <span data-ttu-id="c6f8c-235">Wenn [**Name**](msvm-keyboard.md) vorhanden und kein Schlüssel ist (z. b. für Instanzen von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)), können dieselben Informationen in den Eigenschaften **Name** und **ElementName** vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-235">Where [**Name**](msvm-keyboard.md) exists and is not a Key (such as for instances of [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)), the same information can be present in both the **Name** and **ElementName** properties.</span></span> <span data-ttu-id="c6f8c-236">Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Mouse" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-236">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Mouse".</span></span>

</dd> <dt>

<span data-ttu-id="c6f8c-237">**Enableddefault**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-237">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6f8c-238">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-238">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-239">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6f8c-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c6f8c-240">Die Standard-oder Startkonfiguration eines Administrators für den aktivierten Zustand eines Elements.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-240">An administrator's default or startup configuration for the Enabled State of an element.</span></span> <span data-ttu-id="c6f8c-241">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-241">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c6f8c-242">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-242">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6f8c-243">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-243">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-244">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6f8c-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c6f8c-245">Der aktivierte und deaktivierte Status eines Elements.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-245">The enabled and disabled states of an element.</span></span> <span data-ttu-id="c6f8c-246">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-246">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c6f8c-247">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-247">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6f8c-248">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="c6f8c-248">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-249">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6f8c-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c6f8c-250">Gibt an, ob der in **LastErrorCode** gemeldete Fehler jetzt gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-250">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="c6f8c-251">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-251">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c6f8c-252">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-252">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6f8c-253">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-253">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-254">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6f8c-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c6f8c-255">Eine Zeichenfolge, die weitere Informationen über den Fehler enthält, der in **LastErrorCode** aufgezeichnet wurde, sowie Informationen über alle Maßnahmen, die ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-255">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="c6f8c-256">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-256">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c6f8c-257">**Händigkeit**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-257">**Handedness**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6f8c-258">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-258">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-259">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6f8c-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c6f8c-260">Die Konfiguration des Zeige Geräts für den rechten oder linken Vorgang.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-260">The configuration of the pointing device for right-hand or left-hand operation.</span></span> <span data-ttu-id="c6f8c-261">Diese Eigenschaft wird von [**CIM \_ pointingdevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-261">This property is inherited from [**CIM\_PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span></span>



| <span data-ttu-id="c6f8c-262">Wert</span><span class="sxs-lookup"><span data-stu-id="c6f8c-262">Value</span></span>                                                                        | <span data-ttu-id="c6f8c-263">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c6f8c-263">Meaning</span></span>                            |
|------------------------------------------------------------------------------|------------------------------------|
| <dl> <span data-ttu-id="c6f8c-264"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c6f8c-264"><dt>0</dt></span></span> </dl> | <span data-ttu-id="c6f8c-265">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="c6f8c-265">Unknown</span></span><br/>                 |
| <dl> <span data-ttu-id="c6f8c-266"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="c6f8c-266"><dt>1</dt></span></span> </dl> | <span data-ttu-id="c6f8c-267">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="c6f8c-267">Not applicable.</span></span><br/>         |
| <dl> <span data-ttu-id="c6f8c-268"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="c6f8c-268"><dt>2</dt></span></span> </dl> | <span data-ttu-id="c6f8c-269">Rechter übergebenen Vorgang.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-269">Right handed operation.</span></span><br/> |
| <dl> <span data-ttu-id="c6f8c-270"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="c6f8c-270"><dt>3</dt></span></span> </dl> | <span data-ttu-id="c6f8c-271">Links übergebenen Vorgang.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-271">Left handed operation.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="c6f8c-272">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-272">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6f8c-273">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-273">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-274">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6f8c-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c6f8c-275">Der aktuelle Zustand des Elements.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-275">The current health of the element.</span></span> <span data-ttu-id="c6f8c-276">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und ist immer auf 5 (OK) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-276">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK)</span></span>

</dd> <dt>

<span data-ttu-id="c6f8c-277">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-277">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6f8c-278">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="c6f8c-278">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-279">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6f8c-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c6f8c-280">Ein Array von Freiform-Zeichen folgen, die Erklärungen und Details hinter den Einträgen im " [**OtherIdentifyingInfo**](msvm-keyboard.md) "-Array bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-280">An array of free-form strings that provide explanations and details behind the entries in the [**OtherIdentifyingInfo**](msvm-keyboard.md) array.</span></span> <span data-ttu-id="c6f8c-281">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-281">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="c6f8c-282">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-282">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6f8c-283">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-283">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-284">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6f8c-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c6f8c-285">Das Datum und die Uhrzeit der Erstellung der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-285">The date and time at which the virtual machine was created.</span></span> <span data-ttu-id="c6f8c-286">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-286">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c6f8c-287">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-287">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6f8c-288">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-289">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6f8c-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-290">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-290">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="c6f8c-291">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-291">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="c6f8c-292">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-292">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c6f8c-293">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-293">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6f8c-294">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="c6f8c-294">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-295">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6f8c-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c6f8c-296">Gibt an, ob das Gerät gesperrt ist, und verhindert Benutzereingaben oder-Ausgaben.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-296">Indicates whether the device is locked, preventing user input or output.</span></span> <span data-ttu-id="c6f8c-297">Diese Eigenschaft wird von [**CIM \_ userdevice**](/windows/desktop/CIMWin32Prov/cim-userdevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-297">This property is inherited from [**CIM\_UserDevice**](/windows/desktop/CIMWin32Prov/cim-userdevice).</span></span>

</dd> <dt>

<span data-ttu-id="c6f8c-298">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-298">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6f8c-299">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-299">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-300">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6f8c-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c6f8c-301">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-301">The last error code reported by the logical device.</span></span> <span data-ttu-id="c6f8c-302">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-302">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c6f8c-303">**Maxquiescetime**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-303">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6f8c-304">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-304">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-305">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6f8c-305">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c6f8c-306">Diese Eigenschaft ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-306">This property has been deprecated.</span></span> <span data-ttu-id="c6f8c-307">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-307">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="c6f8c-308">**Name**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-308">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6f8c-309">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-310">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6f8c-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-311">Qualifizierer: **maxlen** (1024)</span><span class="sxs-lookup"><span data-stu-id="c6f8c-311">Qualifiers: **MaxLen** (1024)</span></span>
</dt> </dl>

<span data-ttu-id="c6f8c-312">Die Bezeichnung, mit der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-312">The label by which the object is known.</span></span> <span data-ttu-id="c6f8c-313">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-313">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="c6f8c-314">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-314">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c6f8c-315">**Anzahl von Schaltflächen**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-315">**NumberOfButtons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6f8c-316">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-316">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-317">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6f8c-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c6f8c-318">Die Anzahl der Schaltflächen auf dem Zeigegerät.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-318">The number of buttons on the pointing device.</span></span> <span data-ttu-id="c6f8c-319">Diese Eigenschaft wird von [**CIM \_ pointingdevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-319">This property is inherited from [**CIM\_PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span></span>

</dd> <dt>

<span data-ttu-id="c6f8c-320">**Operatingstatus**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-320">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6f8c-321">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-321">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-322">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6f8c-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c6f8c-323">Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-323">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="c6f8c-324">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-324">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c6f8c-325">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-325">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="c6f8c-326"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="c6f8c-326"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-327"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)</span><span class="sxs-lookup"><span data-stu-id="c6f8c-327"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-328"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Wartung** (2)</span><span class="sxs-lookup"><span data-stu-id="c6f8c-328"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-329"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>Wird **gestartet** (3)</span><span class="sxs-lookup"><span data-stu-id="c6f8c-329"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-330"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>Wird **beendet (4** )</span><span class="sxs-lookup"><span data-stu-id="c6f8c-330"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-331"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Beendet** (5)</span><span class="sxs-lookup"><span data-stu-id="c6f8c-331"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-332"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abgebrochen** (6)</span><span class="sxs-lookup"><span data-stu-id="c6f8c-332"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-333"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Ruhende** (7)</span><span class="sxs-lookup"><span data-stu-id="c6f8c-333"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-334"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Abgeschlossen** (8)</span><span class="sxs-lookup"><span data-stu-id="c6f8c-334"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-335"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrieren** (9)</span><span class="sxs-lookup"><span data-stu-id="c6f8c-335"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-336"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Migration** (10)</span><span class="sxs-lookup"><span data-stu-id="c6f8c-336"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-337"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migration** (11)</span><span class="sxs-lookup"><span data-stu-id="c6f8c-337"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-338"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotts** (12)</span><span class="sxs-lookup"><span data-stu-id="c6f8c-338"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-339"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Herunter** fahren (13)</span><span class="sxs-lookup"><span data-stu-id="c6f8c-339"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-340"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span><span class="sxs-lookup"><span data-stu-id="c6f8c-340"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-341"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Übergang** (15)</span><span class="sxs-lookup"><span data-stu-id="c6f8c-341"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-342"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Dienst** (16)</span><span class="sxs-lookup"><span data-stu-id="c6f8c-342"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-343"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="c6f8c-343"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-344"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="c6f8c-344"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="c6f8c-345">)</span><span class="sxs-lookup"><span data-stu-id="c6f8c-345">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c6f8c-346">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-346">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6f8c-347">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="c6f8c-347">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-348">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6f8c-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c6f8c-349">Der aktuelle Status des Elements.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-349">The current status of the element.</span></span> <span data-ttu-id="c6f8c-350">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und ist immer auf 2 (OK) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-350">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="c6f8c-351">**Otherenabledstate**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-351">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6f8c-352">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-353">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6f8c-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c6f8c-354">Der aktivierte oder deaktivierte Status des Elements, wenn die [**enabledstate**](msvm-keyboard.md) -Eigenschaft auf 1 (Sonstiges) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-354">The enabled or disabled state of the element when the [**EnabledState**](msvm-keyboard.md) property is set to 1 (Other).</span></span> <span data-ttu-id="c6f8c-355">Diese Eigenschaft muss auf **null** festgelegt werden, wenn **enabledstate** ein anderer Wert als 1 ist.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-355">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="c6f8c-356">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-356">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c6f8c-357">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-357">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6f8c-358">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="c6f8c-358">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-359">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6f8c-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c6f8c-360">Alle zusätzlichen Daten über Geräte-ID-Informationen, die zur Identifizierung eines logischen Geräts verwendet werden könnten.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-360">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="c6f8c-361">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-361">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="c6f8c-362">**Pointingtype**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-362">**PointingType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6f8c-363">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-363">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-364">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6f8c-364">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c6f8c-365">Der Typ des Zeige Geräts.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-365">The type of the pointing device.</span></span> <span data-ttu-id="c6f8c-366">Diese Eigenschaft wird von [**CIM \_ pointingdevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-366">This property is inherited from [**CIM\_PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span></span>



| <span data-ttu-id="c6f8c-367">Wert</span><span class="sxs-lookup"><span data-stu-id="c6f8c-367">Value</span></span>                                                                        | <span data-ttu-id="c6f8c-368">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c6f8c-368">Meaning</span></span>          |
|------------------------------------------------------------------------------|------------------|
| <dl> <span data-ttu-id="c6f8c-369"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="c6f8c-369"><dt>3</dt></span></span> </dl> | <span data-ttu-id="c6f8c-370">Maus</span><span class="sxs-lookup"><span data-stu-id="c6f8c-370">Mouse</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c6f8c-371">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-371">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6f8c-372">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="c6f8c-372">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-373">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6f8c-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c6f8c-374">Die Energie Verwaltungsfunktionen des Geräts.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-374">The power management capabilities of the device.</span></span> <span data-ttu-id="c6f8c-375">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-375">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c6f8c-376">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-376">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6f8c-377">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="c6f8c-377">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-378">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6f8c-378">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c6f8c-379">Gibt an, ob das Gerät Energie gesteuert werden kann.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-379">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="c6f8c-380">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-380">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c6f8c-381">**Poweronhours**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-381">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6f8c-382">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-382">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-383">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6f8c-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c6f8c-384">Gibt an, wie viele aufeinanderfolgende Stunden dieses Gerät seit dem letzten Strom Umgebung eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-384">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="c6f8c-385">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-385">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c6f8c-386">**Primarystatus**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-386">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6f8c-387">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-387">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-388">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6f8c-388">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c6f8c-389">Stellt Statusinformationen auf hoher Ebene bereit.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-389">Provides high level status information.</span></span> <span data-ttu-id="c6f8c-390">Diese Eigenschaft sollte in Verbindung mit der Eigenschaft **detailedstatus** verwendet werden, um einen hohen und detaillierten Integritäts Status des Elements und seiner unter Komponenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-390">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="c6f8c-391">Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-391">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c6f8c-392">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-392">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="c6f8c-393"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="c6f8c-393"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-394"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="c6f8c-394"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-395"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (2** )</span><span class="sxs-lookup"><span data-stu-id="c6f8c-395"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-396"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Fehler** (3)</span><span class="sxs-lookup"><span data-stu-id="c6f8c-396"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-397"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="c6f8c-397"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-398"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000..</span><span class="sxs-lookup"><span data-stu-id="c6f8c-398"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="c6f8c-399">)</span><span class="sxs-lookup"><span data-stu-id="c6f8c-399">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c6f8c-400">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-400">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6f8c-401">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-401">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-402">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6f8c-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c6f8c-403">Der zuletzt angeforderte oder gewünschte Zustand für das Element.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-403">The last requested or desired state for the element.</span></span> <span data-ttu-id="c6f8c-404">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-404">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="c6f8c-405">Wert</span><span class="sxs-lookup"><span data-stu-id="c6f8c-405">Value</span></span>                                                                         | <span data-ttu-id="c6f8c-406">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c6f8c-406">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="c6f8c-407"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="c6f8c-407"><dt>12</dt></span></span> </dl> | <span data-ttu-id="c6f8c-408">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="c6f8c-408">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c6f8c-409">**Auflösung**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-409">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6f8c-410">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-410">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-411">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6f8c-411">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c6f8c-412">Die nach Verfolgungs Auflösung des Zeige Geräts in Zählungen pro Zoll.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-412">The tracking resolution of the pointing device, in counts per inch.</span></span> <span data-ttu-id="c6f8c-413">Diese Eigenschaft wird von [**CIM \_ pointingdevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-413">This property is inherited from [**CIM\_PointingDevice**](/windows/desktop/CIMWin32Prov/cim-pointingdevice).</span></span>

</dd> <dt>

<span data-ttu-id="c6f8c-414">**Status**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-414">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6f8c-415">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-416">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6f8c-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c6f8c-417">Der aktuelle Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-417">The current status of the object.</span></span> <span data-ttu-id="c6f8c-418">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-418">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c6f8c-419">**Status Beschreibungen**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-419">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6f8c-420">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="c6f8c-420">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-421">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6f8c-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c6f8c-422">Zeichen folgen, die die verschiedenen [**OperationalStatus**](msvm-bioselement.md) -Array Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-422">Strings that describe the various [**OperationalStatus**](msvm-bioselement.md) array values.</span></span> <span data-ttu-id="c6f8c-423">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) geerbt und ist immer auf "OK" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-423">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) and it is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="c6f8c-424">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-424">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6f8c-425">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-425">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-426">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6f8c-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c6f8c-427">Der aktuelle Zustand des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-427">The current state of the logical device.</span></span> <span data-ttu-id="c6f8c-428">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-428">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c6f8c-429">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-429">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6f8c-430">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-431">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6f8c-431">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-432">Qualifizierer: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="c6f8c-432">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="c6f8c-433">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-433">The scoping system's creation class name.</span></span> <span data-ttu-id="c6f8c-434">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-434">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="c6f8c-435">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-435">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6f8c-436">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-437">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6f8c-437">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-438">Qualifizierer: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="c6f8c-438">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="c6f8c-439">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-439">The scoping system's name.</span></span> <span data-ttu-id="c6f8c-440">Dieser Wert entspricht dem Wert der [**Name**](msvm-computersystem.md) -Eigenschaft der **MSVM \_ Computersystem** -Klasse für die Bereichs bezogene virtuelle Maschine.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-440">This value corresponds to the value of the [**Name**](msvm-computersystem.md) property of the **Msvm\_ComputerSystem** class for the scoping virtual machine.</span></span> <span data-ttu-id="c6f8c-441">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-441">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="c6f8c-442">**Timeoflaststatechange**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-442">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6f8c-443">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-443">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-444">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6f8c-444">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c6f8c-445">Das Datum oder die Uhrzeit, zu dem der aktivierte Status des Elements zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-445">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="c6f8c-446">Wenn der Zustand des Elements nicht geändert wurde und diese Eigenschaft aufgefüllt ist, muss Sie auf einen Wert von 0 Intervall festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-446">If the state of the element has not changed and this property is populated, then it must be set to a 0 interval value.</span></span> <span data-ttu-id="c6f8c-447">Wenn eine Zustandsänderung angefordert, aber abgelehnt oder noch nicht verarbeitet wurde, darf die Eigenschaft nicht aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-447">If a state change was requested, but rejected or not yet processed, the property must not be updated.</span></span> <span data-ttu-id="c6f8c-448">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-448">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c6f8c-449">**Totalpoweronhours**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-449">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6f8c-450">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-450">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-451">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6f8c-451">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c6f8c-452">Die Gesamtanzahl der Stunden, für die dieses Gerät eingeschaltet wurde.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-452">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="c6f8c-453">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-453">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c6f8c-454">**Transitioningumstate**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-454">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6f8c-455">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-455">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c6f8c-456">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6f8c-456">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c6f8c-457">Gibt den Ziel Status an, in den die-Instanz übergeht.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-457">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="c6f8c-458">Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-458">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c6f8c-459">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c6f8c-459">Remarks</span></span>

<span data-ttu-id="c6f8c-460">Der Zugriff auf die **MSVM- \_ Ps2Mouse** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="c6f8c-460">Access to the **Msvm\_Ps2Mouse** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="c6f8c-461">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="c6f8c-461">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="c6f8c-462">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c6f8c-462">Requirements</span></span>



| <span data-ttu-id="c6f8c-463">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c6f8c-463">Requirement</span></span> | <span data-ttu-id="c6f8c-464">Wert</span><span class="sxs-lookup"><span data-stu-id="c6f8c-464">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6f8c-465">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c6f8c-465">Minimum supported client</span></span><br/> | <span data-ttu-id="c6f8c-466">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c6f8c-466">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c6f8c-467">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c6f8c-467">Minimum supported server</span></span><br/> | <span data-ttu-id="c6f8c-468">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c6f8c-468">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c6f8c-469">Namespace</span><span class="sxs-lookup"><span data-stu-id="c6f8c-469">Namespace</span></span><br/>                | <span data-ttu-id="c6f8c-470">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="c6f8c-470">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c6f8c-471">MOF</span><span class="sxs-lookup"><span data-stu-id="c6f8c-471">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c6f8c-472"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c6f8c-472"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c6f8c-473">DLL</span><span class="sxs-lookup"><span data-stu-id="c6f8c-473">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6f8c-474"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c6f8c-474"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c6f8c-475">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c6f8c-475">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6f8c-476">**CIM- \_ pointingdevice**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-476">**CIM\_PointingDevice**</span></span>](cim-pointingdevice.md)
</dt> <dt>

[<span data-ttu-id="c6f8c-477">**CIM- \_ pointingdevice**</span><span class="sxs-lookup"><span data-stu-id="c6f8c-477">**CIM\_PointingDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-pointingdevice)
</dt> <dt>

[<span data-ttu-id="c6f8c-478">Eingabe Klassen</span><span class="sxs-lookup"><span data-stu-id="c6f8c-478">Input Classes</span></span>](input-classes.md)
</dt> </dl>

 

