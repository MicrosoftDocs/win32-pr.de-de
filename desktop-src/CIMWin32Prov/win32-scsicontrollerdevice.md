---
description: Die Win32 \_ -WMI-Klasse scsicontrollerdevice Association bezieht sich auf einen SCSI-Controller (Small Computersystem Interface) und das logische Gerät (Laufwerk), das mit ihm verbunden ist.
ms.assetid: 0334829c-3625-4acf-8ef3-da934c51e9bf
ms.tgt_platform: multiple
title: Win32_SCSIControllerDevice-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SCSIControllerDevice
- Win32_SCSIControllerDevice.NegotiatedDataWidth
- Win32_SCSIControllerDevice.NegotiatedSpeed
- Win32_SCSIControllerDevice.AccessState
- Win32_SCSIControllerDevice.NumberOfHardResets
- Win32_SCSIControllerDevice.NumberOfSoftResets
- Win32_SCSIControllerDevice.Antecedent
- Win32_SCSIControllerDevice.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7a3189f9d9b75321df7c69214e68779864953f6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524259"
---
# <a name="win32_scsicontrollerdevice-class"></a><span data-ttu-id="5dc25-103">Win32 \_ scsicontrollerdevice-Klasse</span><span class="sxs-lookup"><span data-stu-id="5dc25-103">Win32\_SCSIControllerDevice class</span></span>

<span data-ttu-id="5dc25-104">Die Win32- [WMI-Klasse](../wmisdk/retrieving-a-class.md) **\_ scsicontrollerdevice** Association bezieht sich auf einen SCSI-Controller (Small Computersystem Interface) und das logische Gerät (Laufwerk), das mit ihm verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="5dc25-104">The **Win32\_SCSIControllerDevice** association [WMI class](../wmisdk/retrieving-a-class.md) relates a small computer system interface (SCSI) controller and the logical device (disk drive) connected to it.</span></span>

<span data-ttu-id="5dc25-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5dc25-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="5dc25-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="5dc25-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5dc25-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5dc25-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{CC0F48D2-C847-11d2-911E-0060081A46FD}"), AMENDMENT]
class Win32_SCSIControllerDevice : CIM_ControlledBy
{
  uint32                   NegotiatedDataWidth;
  uint64                   NegotiatedSpeed;
  uint16                   AccessState;
  uint32                   NumberOfHardResets;
  uint32                   NumberOfSoftResets;
  Win32_SCSIController REF Antecedent;
  CIM_LogicalDevice    REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="5dc25-108">Member</span><span class="sxs-lookup"><span data-stu-id="5dc25-108">Members</span></span>

<span data-ttu-id="5dc25-109">Die **Win32 \_ scsicontrollerdevice** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="5dc25-109">The **Win32\_SCSIControllerDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="5dc25-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5dc25-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5dc25-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5dc25-111">Properties</span></span>

<span data-ttu-id="5dc25-112">Die **Win32 \_ scsicontrollerdevice** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5dc25-112">The **Win32\_SCSIControllerDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5dc25-113">**Accessstate**</span><span class="sxs-lookup"><span data-stu-id="5dc25-113">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5dc25-114">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5dc25-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5dc25-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5dc25-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5dc25-116">Gibt an, ob der Controller aktiv auf das Gerät zugreift oder darauf zugreift.</span><span class="sxs-lookup"><span data-stu-id="5dc25-116">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="5dc25-117">Diese Informationen sind erforderlich, wenn ein logisches Gerät durch mehrere Controller befohlen werden kann oder darauf zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="5dc25-117">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<span data-ttu-id="5dc25-118">Diese Eigenschaft wird von [**CIM \_ controlledby**](cim-controlledby.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5dc25-118">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5dc25-119">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="5dc25-119">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="5dc25-120">**Aktiv** (1)</span><span class="sxs-lookup"><span data-stu-id="5dc25-120">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="5dc25-121">**Inaktiv** (2)</span><span class="sxs-lookup"><span data-stu-id="5dc25-121">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5dc25-122">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="5dc25-122">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5dc25-123">Datentyp: **Win32 \_ SCSIController**</span><span class="sxs-lookup"><span data-stu-id="5dc25-123">Data type: **Win32\_SCSIController**</span></span>
</dt> <dt>

<span data-ttu-id="5dc25-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5dc25-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5dc25-125">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Vorgänger"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("CIM \| Win32 \_ SCSIController")</span><span class="sxs-lookup"><span data-stu-id="5dc25-125">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|Win32\_SCSIController")</span></span>
</dt> </dl>

<span data-ttu-id="5dc25-126">Die [**Win32 \_ SCSIController**](win32-scsicontroller.md) Vorgänger-Referenz stellt den SCSI-Controller dar, der diesem Gerät zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="5dc25-126">The [**Win32\_SCSIController**](win32-scsicontroller.md) antecedent reference represents the SCSI controller associated with this device.</span></span>

</dd> <dt>

<span data-ttu-id="5dc25-127">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="5dc25-127">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5dc25-128">Datentyp: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="5dc25-128">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="5dc25-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5dc25-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5dc25-130">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ LogicalDevice")</span><span class="sxs-lookup"><span data-stu-id="5dc25-130">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="5dc25-131">Der von [**CIM \_ LogicalDevice**](cim-logicaldevice.md) abhängige Verweis stellt das logische Gerät dar, das mit dem SCSI-Controller verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="5dc25-131">The [**CIM\_LogicalDevice**](cim-logicaldevice.md) dependent reference represents the logical device connected to the SCSI controller.</span></span>

</dd> <dt>

<span data-ttu-id="5dc25-132">**Aushandateddatawidth**</span><span class="sxs-lookup"><span data-stu-id="5dc25-132">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5dc25-133">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5dc25-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5dc25-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5dc25-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5dc25-135">Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Bits")</span><span class="sxs-lookup"><span data-stu-id="5dc25-135">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="5dc25-136">Wenn mehrere Bus-oder Verbindungsdaten breiten möglich sind, definiert diese Eigenschaft die jeweils verwendete Eigenschaft zwischen den Geräten.</span><span class="sxs-lookup"><span data-stu-id="5dc25-136">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="5dc25-137">Die Daten Breite wird in Bits angegeben.</span><span class="sxs-lookup"><span data-stu-id="5dc25-137">Data width is specified in bits.</span></span> <span data-ttu-id="5dc25-138">Wenn die Daten Breite nicht ausgehandelt wird oder diese Informationen für die Geräteverwaltung nicht verfügbar oder wichtig sind, sollte die-Eigenschaft auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="5dc25-138">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="5dc25-139">Diese Eigenschaft wird von CIM-Geräte [**\_ erviceconnetction**](cim-deviceconnection.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5dc25-139">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="5dc25-140">**Aushandatedspeed**</span><span class="sxs-lookup"><span data-stu-id="5dc25-140">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5dc25-141">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5dc25-141">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5dc25-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5dc25-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5dc25-143">Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Bits pro Sekunde")</span><span class="sxs-lookup"><span data-stu-id="5dc25-143">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="5dc25-144">Wenn mehrere Bus-oder Verbindungsgeschwindigkeiten möglich sind, definiert diese Eigenschaft die zwischen den Geräten verwendete.</span><span class="sxs-lookup"><span data-stu-id="5dc25-144">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="5dc25-145">Die Geschwindigkeit wird in Bits pro Sekunde angegeben.</span><span class="sxs-lookup"><span data-stu-id="5dc25-145">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="5dc25-146">Wenn Verbindungs-oder Busgeschwindigkeiten nicht ausgehandelt werden oder diese Informationen für die Geräteverwaltung nicht verfügbar oder wichtig sind, sollte die-Eigenschaft auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="5dc25-146">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="5dc25-147">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="5dc25-147">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="5dc25-148">Diese Eigenschaft wird von CIM-Geräte [**\_ erviceconnetction**](cim-deviceconnection.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5dc25-148">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="5dc25-149">**Anzahlersätze**</span><span class="sxs-lookup"><span data-stu-id="5dc25-149">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5dc25-150">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5dc25-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5dc25-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5dc25-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5dc25-152">Anzahl von Festplatten, die vom Controller ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5dc25-152">Number of hard resets issued by the controller.</span></span> <span data-ttu-id="5dc25-153">Bei einer festen zurück setzung wird das Gerät wieder in den Initialisierungs-oder Startzustand versetzt.</span><span class="sxs-lookup"><span data-stu-id="5dc25-153">A hard reset returns the device to its initialization or boot-up state.</span></span> <span data-ttu-id="5dc25-154">Alle internen Geräte Zustandsinformationen und Daten gehen verloren.</span><span class="sxs-lookup"><span data-stu-id="5dc25-154">All internal device state information and data are lost.</span></span>

<span data-ttu-id="5dc25-155">Diese Eigenschaft wird von [**CIM \_ controlledby**](cim-controlledby.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5dc25-155">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="5dc25-156">**Anzahlermengen**</span><span class="sxs-lookup"><span data-stu-id="5dc25-156">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5dc25-157">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5dc25-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5dc25-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5dc25-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5dc25-159">Anzahl der vom Controller ausgestellten Soft-zurück Stellungen.</span><span class="sxs-lookup"><span data-stu-id="5dc25-159">Number of soft resets issued by the controller.</span></span> <span data-ttu-id="5dc25-160">Eine weiche zurück Setzung löscht den aktuellen Gerätestatus und die Daten nicht vollständig.</span><span class="sxs-lookup"><span data-stu-id="5dc25-160">A soft reset does not completely clear current device state and data.</span></span> <span data-ttu-id="5dc25-161">Die genaue Semantik ist abhängig vom Gerät und den Protokollen und Mechanismen, die für die Kommunikation mit dem Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5dc25-161">Exact semantics are dependent on the device and on the protocols and mechanisms used to communicate to it.</span></span>

<span data-ttu-id="5dc25-162">Diese Eigenschaft wird von [**CIM \_ controlledby**](cim-controlledby.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="5dc25-162">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5dc25-163">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5dc25-163">Remarks</span></span>

<span data-ttu-id="5dc25-164">Die **Win32-Klasse \_ scsicontrollerdevice** ist von [**CIM \_ controlledby**](cim-controlledby.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="5dc25-164">The **Win32\_SCSIControllerDevice** class is derived from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5dc25-165">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5dc25-165">Requirements</span></span>



| <span data-ttu-id="5dc25-166">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5dc25-166">Requirement</span></span> | <span data-ttu-id="5dc25-167">Wert</span><span class="sxs-lookup"><span data-stu-id="5dc25-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5dc25-168">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5dc25-168">Minimum supported client</span></span><br/> | <span data-ttu-id="5dc25-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5dc25-169">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5dc25-170">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5dc25-170">Minimum supported server</span></span><br/> | <span data-ttu-id="5dc25-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5dc25-171">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5dc25-172">Namespace</span><span class="sxs-lookup"><span data-stu-id="5dc25-172">Namespace</span></span><br/>                | <span data-ttu-id="5dc25-173">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="5dc25-173">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5dc25-174">MOF</span><span class="sxs-lookup"><span data-stu-id="5dc25-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5dc25-175"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5dc25-175"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5dc25-176">DLL</span><span class="sxs-lookup"><span data-stu-id="5dc25-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5dc25-177"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5dc25-177"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5dc25-178">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5dc25-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5dc25-179">**CIM- \_ controlledby**</span><span class="sxs-lookup"><span data-stu-id="5dc25-179">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> <dt>

[<span data-ttu-id="5dc25-180">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="5dc25-180">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
