---
description: Die WMI-Klasse für die Win32-Methode für die \_ WMI-Zuordnung bezieht einen USB-Controller (Universal Serial Bus) und die Verbindung mit der CIM \_ LogicalDevice-Instanz ein.
ms.assetid: a0c64984-9116-4cb8-86e0-38c897cb7119
ms.tgt_platform: multiple
title: Win32_USBControllerDevice-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_USBControllerDevice
- Win32_USBControllerDevice.NegotiatedDataWidth
- Win32_USBControllerDevice.NegotiatedSpeed
- Win32_USBControllerDevice.AccessState
- Win32_USBControllerDevice.NumberOfHardResets
- Win32_USBControllerDevice.NumberOfSoftResets
- Win32_USBControllerDevice.Antecedent
- Win32_USBControllerDevice.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9bf72c92a4ae23ac7750cdd52914e86f5dbcdd01
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342977"
---
# <a name="win32_usbcontrollerdevice-class"></a><span data-ttu-id="ea392-103">Win32-Klasse "- \_ bcontrollerdevice"</span><span class="sxs-lookup"><span data-stu-id="ea392-103">Win32\_USBControllerDevice class</span></span>

<span data-ttu-id="ea392-104">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) für die Win32-Methode für die WMI-Zuordnung bezieht einen USB-Controller (Universal Serial Bus) und die Verbindung mit der [**CIM \_ LogicalDevice**](cim-logicaldevice.md) -Instanz ein. **\_**</span><span class="sxs-lookup"><span data-stu-id="ea392-104">The **Win32\_USBControllerDevice** association [WMI class](../wmisdk/retrieving-a-class.md) relates a universal serial bus (USB) controller and the [**CIM\_LogicalDevice**](cim-logicaldevice.md) instance connected to it.</span></span>

<span data-ttu-id="ea392-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ea392-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="ea392-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="ea392-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea392-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ea392-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{DE57D792-A032-11D2-90F0-0060081A46FD}"), AMENDMENT]
class Win32_USBControllerDevice : CIM_ControlledBy
{
  uint32                NegotiatedDataWidth;
  uint64                NegotiatedSpeed;
  uint16                AccessState;
  uint32                NumberOfHardResets;
  uint32                NumberOfSoftResets;
  CIM_USBController REF Antecedent;
  CIM_LogicalDevice REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="ea392-108">Member</span><span class="sxs-lookup"><span data-stu-id="ea392-108">Members</span></span>

<span data-ttu-id="ea392-109">Die **Win32 \_** -Klasse "-Klasse":</span><span class="sxs-lookup"><span data-stu-id="ea392-109">The **Win32\_USBControllerDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="ea392-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ea392-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ea392-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ea392-111">Properties</span></span>

<span data-ttu-id="ea392-112">Die **Win32 \_** -Klasse "-Klasse" hat diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ea392-112">The **Win32\_USBControllerDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ea392-113">**Accessstate**</span><span class="sxs-lookup"><span data-stu-id="ea392-113">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea392-114">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ea392-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ea392-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ea392-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea392-116">Gibt an, ob der Controller aktiv auf das Gerät zugreift oder darauf zugreift.</span><span class="sxs-lookup"><span data-stu-id="ea392-116">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="ea392-117">Diese Informationen sind erforderlich, wenn ein logisches Gerät durch mehrere Controller befohlen werden kann oder darauf zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="ea392-117">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<span data-ttu-id="ea392-118">Diese Eigenschaft wird von [**CIM \_ controlledby**](cim-controlledby.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ea392-118">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ea392-119">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="ea392-119">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="ea392-120">**Aktiv** (1)</span><span class="sxs-lookup"><span data-stu-id="ea392-120">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="ea392-121">**Inaktiv** (2)</span><span class="sxs-lookup"><span data-stu-id="ea392-121">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ea392-122">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="ea392-122">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea392-123">Datentyp: **CIM \_** -Start Controller</span><span class="sxs-lookup"><span data-stu-id="ea392-123">Data type: **CIM\_USBController**</span></span>
</dt> <dt>

<span data-ttu-id="ea392-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ea392-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea392-125">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Vorgänger"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM-Start \_ Controller")</span><span class="sxs-lookup"><span data-stu-id="ea392-125">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_USBController")</span></span>
</dt> </dl>

<span data-ttu-id="ea392-126">Ein [**CIM \_**](cim-usbcontroller.md) -Start Controller, der den diesem Gerät zugeordneten USB-Controller (Universal Serial Bus) darstellt.</span><span class="sxs-lookup"><span data-stu-id="ea392-126">A [**CIM\_USBController**](cim-usbcontroller.md) representing the Universal Serial Bus (USB) controller associated with this device.</span></span>

</dd> <dt>

<span data-ttu-id="ea392-127">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="ea392-127">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea392-128">Datentyp: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="ea392-128">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="ea392-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ea392-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea392-130">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ LogicalDevice")</span><span class="sxs-lookup"><span data-stu-id="ea392-130">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="ea392-131">Ein [**CIM \_ LogicalDevice**](cim-logicaldevice.md) , das das logische Gerät beschreibt, das mit dem USB-Controller (Universal Serial Bus) verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="ea392-131">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) describing the logical device connected to the Universal Serial Bus (USB) controller.</span></span>

</dd> <dt>

<span data-ttu-id="ea392-132">**Aushandateddatawidth**</span><span class="sxs-lookup"><span data-stu-id="ea392-132">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea392-133">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ea392-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ea392-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ea392-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea392-135">Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Bits")</span><span class="sxs-lookup"><span data-stu-id="ea392-135">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="ea392-136">Wenn mehrere Bus-oder Verbindungsdaten breiten möglich sind, definiert diese Eigenschaft die jeweils verwendete Eigenschaft zwischen den Geräten.</span><span class="sxs-lookup"><span data-stu-id="ea392-136">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="ea392-137">Die Daten Breite wird in Bits angegeben.</span><span class="sxs-lookup"><span data-stu-id="ea392-137">Data width is specified in bits.</span></span> <span data-ttu-id="ea392-138">Wenn die Daten Breite nicht ausgehandelt wird oder diese Informationen für die Geräteverwaltung nicht verfügbar oder wichtig sind, sollte die-Eigenschaft auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="ea392-138">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="ea392-139">Diese Eigenschaft wird von CIM-Geräte [**\_ erviceconnetction**](cim-deviceconnection.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ea392-139">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="ea392-140">**Aushandatedspeed**</span><span class="sxs-lookup"><span data-stu-id="ea392-140">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea392-141">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ea392-141">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ea392-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ea392-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea392-143">Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Bits pro Sekunde")</span><span class="sxs-lookup"><span data-stu-id="ea392-143">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="ea392-144">Wenn mehrere Bus-oder Verbindungsgeschwindigkeiten möglich sind, definiert diese Eigenschaft die zwischen den Geräten verwendete.</span><span class="sxs-lookup"><span data-stu-id="ea392-144">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="ea392-145">Die Geschwindigkeit wird in Bits pro Sekunde angegeben.</span><span class="sxs-lookup"><span data-stu-id="ea392-145">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="ea392-146">Wenn Verbindungs-oder Busgeschwindigkeiten nicht ausgehandelt werden oder diese Informationen für die Geräteverwaltung nicht verfügbar oder wichtig sind, sollte die-Eigenschaft auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="ea392-146">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="ea392-147">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="ea392-147">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="ea392-148">Diese Eigenschaft wird von CIM-Geräte [**\_ erviceconnetction**](cim-deviceconnection.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ea392-148">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="ea392-149">**Anzahlersätze**</span><span class="sxs-lookup"><span data-stu-id="ea392-149">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea392-150">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ea392-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ea392-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ea392-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea392-152">Anzahl von Festplatten, die vom Controller ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ea392-152">Number of hard resets issued by the controller.</span></span> <span data-ttu-id="ea392-153">Bei einer festen zurück setzung wird das Gerät wieder in den Initialisierungs-oder Startzustand versetzt.</span><span class="sxs-lookup"><span data-stu-id="ea392-153">A hard reset returns the device to its initialization or boot-up state.</span></span> <span data-ttu-id="ea392-154">Alle internen Geräte Zustandsinformationen und Daten gehen verloren.</span><span class="sxs-lookup"><span data-stu-id="ea392-154">All internal device state information and data are lost.</span></span>

<span data-ttu-id="ea392-155">Diese Eigenschaft wird von [**CIM \_ controlledby**](cim-controlledby.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ea392-155">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="ea392-156">**Anzahlermengen**</span><span class="sxs-lookup"><span data-stu-id="ea392-156">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea392-157">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ea392-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ea392-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ea392-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ea392-159">Anzahl der vom Controller ausgestellten Soft-zurück Stellungen.</span><span class="sxs-lookup"><span data-stu-id="ea392-159">Number of soft resets issued by the controller.</span></span> <span data-ttu-id="ea392-160">Eine weiche zurück Setzung löscht den aktuellen Gerätestatus und die Daten nicht vollständig.</span><span class="sxs-lookup"><span data-stu-id="ea392-160">A soft reset does not completely clear current device state and data.</span></span> <span data-ttu-id="ea392-161">Die genaue Semantik ist abhängig vom Gerät und den Protokollen und Mechanismen, die für die Kommunikation mit dem Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ea392-161">Exact semantics are dependent on the device and on the protocols and mechanisms used to communicate to it.</span></span>

<span data-ttu-id="ea392-162">Diese Eigenschaft wird von [**CIM \_ controlledby**](cim-controlledby.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ea392-162">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ea392-163">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ea392-163">Remarks</span></span>

<span data-ttu-id="ea392-164">Die **Win32 \_** -Klasse "-Klasse" wird von [**CIM \_ controlledby**](cim-controlledby.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="ea392-164">The **Win32\_USBControllerDevice** class is derived from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<span data-ttu-id="ea392-165">Eine Erläuterung zur Verwendung von finden Sie im Artikel [Anzeigen von USB-Geräten mithilfe des WMI-](https://devblogs.microsoft.com/powershell/displaying-usb-devices-using-wmi/) Blogs.</span><span class="sxs-lookup"><span data-stu-id="ea392-165">For a discussion on using, see the [Displaying USB Devices using WMI](https://devblogs.microsoft.com/powershell/displaying-usb-devices-using-wmi/) blog article.</span></span> <span data-ttu-id="ea392-166">Eine Erörterung der Verwendung von Zuordnungs Klassen finden Sie [im Artikel Get-USB – Using WMI Association classes in PowerShell](https://devblogs.microsoft.com/powershell/get-usb-using-wmi-association-classes-in-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="ea392-166">For a discussion of using association classes, see the [Get-USB – Using WMI Association Classes in PowerShell](https://devblogs.microsoft.com/powershell/get-usb-using-wmi-association-classes-in-powershell/) article.</span></span>

## <a name="examples"></a><span data-ttu-id="ea392-167">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ea392-167">Examples</span></span>

<span data-ttu-id="ea392-168">Das folgende PowerShell-Beispiel ruft das abhängige logische Gerät ab und zeigt die relevanten Informationen an.</span><span class="sxs-lookup"><span data-stu-id="ea392-168">The following PowerShell example retrieves the dependent logical device and displays the relevant information.</span></span>


```PowerShell
gwmi Win32_USBControllerDevice |%{[wmi]($_.Dependent)} | Sort Manufacturer,Description,DeviceID | Ft -GroupBy Manufacturer Description,Service,DeviceID
```



## <a name="requirements"></a><span data-ttu-id="ea392-169">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ea392-169">Requirements</span></span>



| <span data-ttu-id="ea392-170">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ea392-170">Requirement</span></span> | <span data-ttu-id="ea392-171">Wert</span><span class="sxs-lookup"><span data-stu-id="ea392-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea392-172">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ea392-172">Minimum supported client</span></span><br/> | <span data-ttu-id="ea392-173">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ea392-173">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ea392-174">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ea392-174">Minimum supported server</span></span><br/> | <span data-ttu-id="ea392-175">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ea392-175">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ea392-176">Namespace</span><span class="sxs-lookup"><span data-stu-id="ea392-176">Namespace</span></span><br/>                | <span data-ttu-id="ea392-177">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ea392-177">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ea392-178">MOF</span><span class="sxs-lookup"><span data-stu-id="ea392-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ea392-179"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ea392-179"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ea392-180">DLL</span><span class="sxs-lookup"><span data-stu-id="ea392-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea392-181"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea392-181"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea392-182">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ea392-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea392-183">**CIM- \_ controlledby**</span><span class="sxs-lookup"><span data-stu-id="ea392-183">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> <dt>

[<span data-ttu-id="ea392-184">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="ea392-184">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
