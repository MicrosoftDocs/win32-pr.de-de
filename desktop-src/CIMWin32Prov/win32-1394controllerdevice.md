---
description: Die \_ WMI-Klasse für die Win32-Klasse "1394controllerdevice" verknüpft den Hochleistungs Controller (IEEE 1394 FireWire) und die Verbindung mit der CIM \_ LogicalDevice-Instanz.
ms.assetid: 327fbced-4637-4402-a06f-6ac352da920c
ms.tgt_platform: multiple
title: Win32_1394ControllerDevice-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_1394ControllerDevice
- Win32_1394ControllerDevice.NegotiatedDataWidth
- Win32_1394ControllerDevice.NegotiatedSpeed
- Win32_1394ControllerDevice.AccessState
- Win32_1394ControllerDevice.NumberOfHardResets
- Win32_1394ControllerDevice.NumberOfSoftResets
- Win32_1394ControllerDevice.Antecedent
- Win32_1394ControllerDevice.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: af3a54db81a388184da148cd411895ebb910de7d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861595"
---
# <a name="win32_1394controllerdevice-class"></a><span data-ttu-id="44818-103">Win32- \_ Klasse "1394controllerdevice"</span><span class="sxs-lookup"><span data-stu-id="44818-103">Win32\_1394ControllerDevice class</span></span>

<span data-ttu-id="44818-104">Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) für die Win32-Klasse " **\_ 1394controllerdevice** " verknüpft den Hochleistungs Controller (IEEE 1394 FireWire) und die Verbindung mit der [**CIM \_ LogicalDevice**](cim-logicaldevice.md) -Instanz.</span><span class="sxs-lookup"><span data-stu-id="44818-104">The **Win32\_1394ControllerDevice** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates the high-speed serial bus (IEEE 1394 Firewire) Controller and the [**CIM\_LogicalDevice**](cim-logicaldevice.md) instance connected to it.</span></span> <span data-ttu-id="44818-105">Dieser serielle Bus bietet eine verbesserte Konnektivität für eine große Bandbreite von Geräten, einschließlich Consumer-Audiodaten oder Videokomponenten, Speicher Peripheriegeräte, andere Computer und tragbare Geräte.</span><span class="sxs-lookup"><span data-stu-id="44818-105">This serial bus provides enhanced connectivity for a wide range of devices, including consumer audio or video components, storage peripherals, other computers, and portable devices.</span></span> <span data-ttu-id="44818-106">IEEE 1394 wurde von der Consumer Electronics Industry übernommen und bietet eine Plug & Play kompatible Erweiterungsschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="44818-106">IEEE 1394 has been adopted by the consumer electronics industry and provides a Plug and Play-compatible expansion interface.</span></span>

<span data-ttu-id="44818-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="44818-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="44818-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="44818-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="44818-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="44818-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8835CFC9-BAEF-11d2-85E5-0000F8102E5F}"), AMENDMENT]
class Win32_1394ControllerDevice : CIM_ControlledBy
{
  uint32                   NegotiatedDataWidth;
  uint64                   NegotiatedSpeed;
  uint16                   AccessState;
  uint32                   NumberOfHardResets;
  uint32                   NumberOfSoftResets;
  Win32_1394Controller REF Antecedent;
  CIM_LogicalDevice    REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="44818-110">Member</span><span class="sxs-lookup"><span data-stu-id="44818-110">Members</span></span>

<span data-ttu-id="44818-111">Die Win32-Klasse " **\_ 1394controllerdevice** " enthält diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="44818-111">The **Win32\_1394ControllerDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="44818-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="44818-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="44818-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="44818-113">Properties</span></span>

<span data-ttu-id="44818-114">Die Win32-Klasse " **\_ 1394controllerdevice** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="44818-114">The **Win32\_1394ControllerDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="44818-115">**Accessstate**</span><span class="sxs-lookup"><span data-stu-id="44818-115">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44818-116">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="44818-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="44818-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="44818-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44818-118">Gibt an, ob der Controller aktiv auf das Gerät zugreift oder darauf zugreift.</span><span class="sxs-lookup"><span data-stu-id="44818-118">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="44818-119">Diese Informationen sind erforderlich, wenn ein logisches Gerät durch mehrere Controller befohlen werden kann oder darauf zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="44818-119">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<span data-ttu-id="44818-120">Diese Eigenschaft wird von [**CIM \_ controlledby**](cim-controlledby.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="44818-120">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="44818-121">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="44818-121">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="44818-122">**Aktiv** (1)</span><span class="sxs-lookup"><span data-stu-id="44818-122">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="44818-123">**Inaktiv** (2)</span><span class="sxs-lookup"><span data-stu-id="44818-123">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="44818-124">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="44818-124">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44818-125">Datentyp: **Win32 \_** -Wert Controller</span><span class="sxs-lookup"><span data-stu-id="44818-125">Data type: **Win32\_1394Controller**</span></span>
</dt> <dt>

<span data-ttu-id="44818-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="44818-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44818-127">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorgänger"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ 1394controller")</span><span class="sxs-lookup"><span data-stu-id="44818-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_1394Controller")</span></span>
</dt> </dl>

<span data-ttu-id="44818-128">Die Win32-Referenz für den " \_ 1394controller Vorgänger" stellt den 1394-Controller dar, der diesem Gerät zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="44818-128">The Win32\_1394Controller antecedent reference represents the 1394 controller associated with this device.</span></span>

</dd> <dt>

<span data-ttu-id="44818-129">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="44818-129">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44818-130">Datentyp: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="44818-130">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="44818-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="44818-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44818-132">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM \_ LogicalDevice")</span><span class="sxs-lookup"><span data-stu-id="44818-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="44818-133">Der \_ von CIM LogicalDevice abhängige Verweis stellt das CIM \_ LogicalDevice dar, das mit dem 1394-Controller verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="44818-133">The CIM\_LogicalDevice dependent reference represents the CIM\_LogicalDevice connected to the 1394 controller.</span></span>

</dd> <dt>

<span data-ttu-id="44818-134">**Aushandateddatawidth**</span><span class="sxs-lookup"><span data-stu-id="44818-134">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44818-135">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="44818-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="44818-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="44818-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44818-137">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits")</span><span class="sxs-lookup"><span data-stu-id="44818-137">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="44818-138">Wenn mehrere Bus-oder Verbindungsdaten breiten möglich sind, definiert diese Eigenschaft die jeweils verwendete Eigenschaft zwischen den Geräten.</span><span class="sxs-lookup"><span data-stu-id="44818-138">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="44818-139">Die Daten Breite wird in Bits angegeben.</span><span class="sxs-lookup"><span data-stu-id="44818-139">Data width is specified in bits.</span></span> <span data-ttu-id="44818-140">Wenn die Daten Breite nicht ausgehandelt wird oder diese Informationen für die Geräteverwaltung nicht verfügbar oder wichtig sind, sollte die-Eigenschaft auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="44818-140">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="44818-141">Diese Eigenschaft wird von CIM-Geräte [**\_ erviceconnetction**](cim-deviceconnection.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="44818-141">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="44818-142">**Aushandatedspeed**</span><span class="sxs-lookup"><span data-stu-id="44818-142">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44818-143">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="44818-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="44818-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="44818-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44818-145">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits pro Sekunde")</span><span class="sxs-lookup"><span data-stu-id="44818-145">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="44818-146">Wenn mehrere Bus-oder Verbindungsgeschwindigkeiten möglich sind, definiert diese Eigenschaft die zwischen den Geräten verwendete.</span><span class="sxs-lookup"><span data-stu-id="44818-146">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="44818-147">Die Geschwindigkeit wird in Bits pro Sekunde angegeben.</span><span class="sxs-lookup"><span data-stu-id="44818-147">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="44818-148">Wenn Verbindungs-oder Busgeschwindigkeiten nicht ausgehandelt werden oder diese Informationen für die Geräteverwaltung nicht verfügbar oder wichtig sind, sollte die-Eigenschaft auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="44818-148">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="44818-149">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="44818-149">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="44818-150">Diese Eigenschaft wird von CIM-Geräte [**\_ erviceconnetction**](cim-deviceconnection.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="44818-150">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="44818-151">**Anzahlersätze**</span><span class="sxs-lookup"><span data-stu-id="44818-151">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44818-152">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="44818-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="44818-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="44818-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44818-154">Anzahl von Festplatten, die vom Controller ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="44818-154">Number of hard resets issued by the controller.</span></span> <span data-ttu-id="44818-155">Bei einer festen zurück setzung wird das Gerät wieder in den Initialisierungs-oder Startzustand versetzt.</span><span class="sxs-lookup"><span data-stu-id="44818-155">A hard reset returns the device to its initialization or boot-up state.</span></span> <span data-ttu-id="44818-156">Alle internen Geräte Zustandsinformationen und Daten gehen verloren.</span><span class="sxs-lookup"><span data-stu-id="44818-156">All internal device state information and data are lost.</span></span>

<span data-ttu-id="44818-157">Diese Eigenschaft wird von [**CIM \_ controlledby**](cim-controlledby.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="44818-157">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="44818-158">**Anzahlermengen**</span><span class="sxs-lookup"><span data-stu-id="44818-158">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44818-159">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="44818-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="44818-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="44818-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44818-161">Anzahl der vom Controller ausgestellten Soft-zurück Stellungen.</span><span class="sxs-lookup"><span data-stu-id="44818-161">Number of soft resets issued by the controller.</span></span> <span data-ttu-id="44818-162">Eine weiche zurück Setzung löscht den aktuellen Gerätestatus und die Daten nicht vollständig.</span><span class="sxs-lookup"><span data-stu-id="44818-162">A soft reset does not completely clear current device state and data.</span></span> <span data-ttu-id="44818-163">Die genaue Semantik ist abhängig vom Gerät und den Protokollen und Mechanismen, die für die Kommunikation mit dem Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="44818-163">Exact semantics are dependent on the device and on the protocols and mechanisms used to communicate to it.</span></span>

<span data-ttu-id="44818-164">Diese Eigenschaft wird von [**CIM \_ controlledby**](cim-controlledby.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="44818-164">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="44818-165">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="44818-165">Remarks</span></span>

<span data-ttu-id="44818-166">Die Win32-Klasse " **\_ 1394controllerdevice** " ist von [**CIM \_ controlledby**](cim-controlledby.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="44818-166">The **Win32\_1394ControllerDevice** class is derived from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

## <a name="examples"></a><span data-ttu-id="44818-167">Beispiele</span><span class="sxs-lookup"><span data-stu-id="44818-167">Examples</span></span>

<span data-ttu-id="44818-168">Das folgende PowerShell-Codebeispiel ruft 1394 Controller-Geräteinformationen ab.</span><span class="sxs-lookup"><span data-stu-id="44818-168">The following PowerShell code sample retrieves 1394 controller device information.</span></span>


```PowerShell
# Helper function to return AccessState

function get-WmiAccessState {
param ([uint16] $char)

# parse and return values

If ($char -le 2 -and $char -ge 0) {

switch ($char) {
0 {"00-Reserved"}
1 {"01-Reserved"}
2 {"02-Unknown"}
}
}

Else {
"$char - unknown value"
}
}

# Get 1394 Controller Device information from WMI
$1394Cont = Get-WMIObject Win32_1394ControllerDevice

# Display Details
"Win32_1394ControllerDevice WMI Information"
"=========================================="

foreach ($device in $1394Cont) {

"Device Characteristics - Device {0}" -f ++$i

"Access State : {0}" -f (Get-WmiAccessState($ch))
"Antecedent : {0}" -f $device.Antecedent
"Negotiated Data Width : {0}" -f $device.NegotiatedDataWidth
"Negotiated Speed : {0}" -f $device.NegotiatedSpeed
"Number of Hard Resets : {0}" -f $device.NumberofHardResets
"Number of Soft Resets : {0}" -f $device.NumberofSoftResets
} 
```



<span data-ttu-id="44818-169">Im vorherigen Codebeispiel werden die folgenden Informationen zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="44818-169">The previous code sample returns the following information:</span></span>

``` syntax
# Win32_1394ControllerDevice WMI Information

Device Characteristics -Device 1
Access State : 00-Reserved
Antecedent : \\UK0N055\root\CIMV2:Win32_1394Controller.DeviceID="PCI\\VEN_1217&DEV_00F7&SUBSYS_01CC1028
&REV_02\\4&2FE911E8&0&0CF0"
Negotiated Data Width :
Negotiated Speed :
Number of Hard Resets :
Number of Soft Resets :
```

## <a name="requirements"></a><span data-ttu-id="44818-170">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="44818-170">Requirements</span></span>



| <span data-ttu-id="44818-171">Anforderung</span><span class="sxs-lookup"><span data-stu-id="44818-171">Requirement</span></span> | <span data-ttu-id="44818-172">Wert</span><span class="sxs-lookup"><span data-stu-id="44818-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="44818-173">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="44818-173">Minimum supported client</span></span><br/> | <span data-ttu-id="44818-174">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="44818-174">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="44818-175">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="44818-175">Minimum supported server</span></span><br/> | <span data-ttu-id="44818-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="44818-176">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="44818-177">Namespace</span><span class="sxs-lookup"><span data-stu-id="44818-177">Namespace</span></span><br/>                | <span data-ttu-id="44818-178">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="44818-178">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="44818-179">MOF</span><span class="sxs-lookup"><span data-stu-id="44818-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="44818-180"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="44818-180"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="44818-181">DLL</span><span class="sxs-lookup"><span data-stu-id="44818-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44818-182"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44818-182"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44818-183">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="44818-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44818-184">**CIM- \_ controlledby**</span><span class="sxs-lookup"><span data-stu-id="44818-184">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> <dt>

[<span data-ttu-id="44818-185">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="44818-185">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

