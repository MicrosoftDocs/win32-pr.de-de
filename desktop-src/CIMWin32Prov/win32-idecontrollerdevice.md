---
description: Die \_ WMI-Klasse der Win32-idecontrollerdevice-Zuordnung bezieht einen IDE-Controller (Integrated Drive Electronics) und das mit verbundene logische Gerät (z. b. ein Laufwerk) in Beziehung.
ms.assetid: 1b0a551c-d836-4147-91ed-a0a7d97f4a5b
ms.tgt_platform: multiple
title: Win32_IDEControllerDevice-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_IDEControllerDevice
- Win32_IDEControllerDevice.NegotiatedDataWidth
- Win32_IDEControllerDevice.NegotiatedSpeed
- Win32_IDEControllerDevice.AccessState
- Win32_IDEControllerDevice.NumberOfHardResets
- Win32_IDEControllerDevice.NumberOfSoftResets
- Win32_IDEControllerDevice.Antecedent
- Win32_IDEControllerDevice.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bc690aadd442d656132b2d9e4539cc27961c3ef9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393198"
---
# <a name="win32_idecontrollerdevice-class"></a><span data-ttu-id="2f3e3-103">Win32- \_ idecontrollerdevice-Klasse</span><span class="sxs-lookup"><span data-stu-id="2f3e3-103">Win32\_IDEControllerDevice class</span></span>

<span data-ttu-id="2f3e3-104">Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) der **Win32- \_ idecontrollerdevice** -Zuordnung bezieht einen IDE-Controller (Integrated Drive Electronics) und das mit verbundene logische Gerät (z. b. ein Laufwerk) in Beziehung.</span><span class="sxs-lookup"><span data-stu-id="2f3e3-104">The **Win32\_IDEControllerDevice** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates an Integrated Drive Electronics (IDE) controller and the logical device connected to, for example, a disk drive.</span></span>

<span data-ttu-id="2f3e3-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2f3e3-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="2f3e3-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="2f3e3-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f3e3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f3e3-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{5BC42B62-C7A1-11d2-911D-0060081A46FD}"), AMENDMENT]
class Win32_IDEControllerDevice : CIM_ControlledBy
{
  uint32                  NegotiatedDataWidth;
  uint64                  NegotiatedSpeed;
  uint16                  AccessState;
  uint32                  NumberOfHardResets;
  uint32                  NumberOfSoftResets;
  Win32_IDEController REF Antecedent;
  CIM_LogicalDevice   REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="2f3e3-108">Member</span><span class="sxs-lookup"><span data-stu-id="2f3e3-108">Members</span></span>

<span data-ttu-id="2f3e3-109">Die **Win32- \_ idecontrollerdevice** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2f3e3-109">The **Win32\_IDEControllerDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="2f3e3-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2f3e3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2f3e3-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2f3e3-111">Properties</span></span>

<span data-ttu-id="2f3e3-112">Die **Win32- \_ idecontrollerdevice** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2f3e3-112">The **Win32\_IDEControllerDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2f3e3-113">**Accessstate**</span><span class="sxs-lookup"><span data-stu-id="2f3e3-113">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f3e3-114">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2f3e3-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2f3e3-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2f3e3-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f3e3-116">Gibt an, ob der Controller aktiv auf das Gerät zugreift oder darauf zugreift.</span><span class="sxs-lookup"><span data-stu-id="2f3e3-116">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="2f3e3-117">Diese Informationen sind erforderlich, wenn ein logisches Gerät durch mehrere Controller befohlen werden kann oder darauf zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="2f3e3-117">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<span data-ttu-id="2f3e3-118">Diese Eigenschaft wird von [**CIM \_ controlledby**](cim-controlledby.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2f3e3-118">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2f3e3-119">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="2f3e3-119">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="2f3e3-120">**Aktiv** (1)</span><span class="sxs-lookup"><span data-stu-id="2f3e3-120">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="2f3e3-121">**Inaktiv** (2)</span><span class="sxs-lookup"><span data-stu-id="2f3e3-121">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2f3e3-122">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="2f3e3-122">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f3e3-123">Datentyp: **Win32- \_ idecontroller**</span><span class="sxs-lookup"><span data-stu-id="2f3e3-123">Data type: **Win32\_IDEController**</span></span>
</dt> <dt>

<span data-ttu-id="2f3e3-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2f3e3-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f3e3-125">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorgänger"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| Win32 \_ idecontroller")</span><span class="sxs-lookup"><span data-stu-id="2f3e3-125">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|Win32\_IDEController")</span></span>
</dt> </dl>

<span data-ttu-id="2f3e3-126">Ein [**Win32- \_ idecontroller**](win32-idecontroller.md) , der den IDE-Controller darstellt, der diesem Gerät zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="2f3e3-126">A [**Win32\_IDEController**](win32-idecontroller.md) that represents the IDE controller associated with this device.</span></span>

</dd> <dt>

<span data-ttu-id="2f3e3-127">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="2f3e3-127">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f3e3-128">Datentyp: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="2f3e3-128">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="2f3e3-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2f3e3-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f3e3-130">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM \_ LogicalDevice")</span><span class="sxs-lookup"><span data-stu-id="2f3e3-130">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="2f3e3-131">Ein [**CIM \_ LogicalDevice**](cim-logicaldevice.md) , das das logische Gerät darstellt, das mit dem IDE-Controller verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="2f3e3-131">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that represents the logical device connected to the IDE controller.</span></span>

</dd> <dt>

<span data-ttu-id="2f3e3-132">**Aushandateddatawidth**</span><span class="sxs-lookup"><span data-stu-id="2f3e3-132">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f3e3-133">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2f3e3-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2f3e3-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2f3e3-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f3e3-135">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits")</span><span class="sxs-lookup"><span data-stu-id="2f3e3-135">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="2f3e3-136">Wenn mehrere Bus-oder Verbindungsdaten breiten möglich sind, definiert diese Eigenschaft die jeweils verwendete Eigenschaft zwischen den Geräten.</span><span class="sxs-lookup"><span data-stu-id="2f3e3-136">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="2f3e3-137">Die Daten Breite wird in Bits angegeben.</span><span class="sxs-lookup"><span data-stu-id="2f3e3-137">Data width is specified in bits.</span></span> <span data-ttu-id="2f3e3-138">Wenn die Daten Breite nicht ausgehandelt wird oder diese Informationen für die Geräteverwaltung nicht verfügbar oder wichtig sind, sollte die-Eigenschaft auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="2f3e3-138">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="2f3e3-139">Diese Eigenschaft wird von CIM-Geräte [**\_ erviceconnetction**](cim-deviceconnection.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2f3e3-139">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f3e3-140">**Aushandatedspeed**</span><span class="sxs-lookup"><span data-stu-id="2f3e3-140">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f3e3-141">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2f3e3-141">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2f3e3-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2f3e3-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f3e3-143">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits pro Sekunde")</span><span class="sxs-lookup"><span data-stu-id="2f3e3-143">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="2f3e3-144">Wenn mehrere Bus-oder Verbindungsgeschwindigkeiten möglich sind, definiert diese Eigenschaft die zwischen den Geräten verwendete.</span><span class="sxs-lookup"><span data-stu-id="2f3e3-144">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="2f3e3-145">Die Geschwindigkeit wird in Bits pro Sekunde angegeben.</span><span class="sxs-lookup"><span data-stu-id="2f3e3-145">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="2f3e3-146">Wenn Verbindungs-oder Busgeschwindigkeiten nicht ausgehandelt werden oder diese Informationen für die Geräteverwaltung nicht verfügbar oder wichtig sind, sollte die-Eigenschaft auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="2f3e3-146">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="2f3e3-147">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="2f3e3-147">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="2f3e3-148">Diese Eigenschaft wird von CIM-Geräte [**\_ erviceconnetction**](cim-deviceconnection.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2f3e3-148">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f3e3-149">**Anzahlersätze**</span><span class="sxs-lookup"><span data-stu-id="2f3e3-149">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f3e3-150">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2f3e3-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2f3e3-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2f3e3-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f3e3-152">Anzahl von Festplatten, die vom Controller ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2f3e3-152">Number of hard resets issued by the controller.</span></span> <span data-ttu-id="2f3e3-153">Bei einer festen zurück setzung wird das Gerät wieder in den Initialisierungs-oder Startzustand versetzt.</span><span class="sxs-lookup"><span data-stu-id="2f3e3-153">A hard reset returns the device to its initialization or boot-up state.</span></span> <span data-ttu-id="2f3e3-154">Alle internen Geräte Zustandsinformationen und Daten gehen verloren.</span><span class="sxs-lookup"><span data-stu-id="2f3e3-154">All internal device state information and data are lost.</span></span>

<span data-ttu-id="2f3e3-155">Diese Eigenschaft wird von [**CIM \_ controlledby**](cim-controlledby.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2f3e3-155">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f3e3-156">**Anzahlermengen**</span><span class="sxs-lookup"><span data-stu-id="2f3e3-156">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f3e3-157">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2f3e3-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2f3e3-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2f3e3-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f3e3-159">Anzahl der vom Controller ausgestellten Soft-zurück Stellungen.</span><span class="sxs-lookup"><span data-stu-id="2f3e3-159">Number of soft resets issued by the controller.</span></span> <span data-ttu-id="2f3e3-160">Eine weiche zurück Setzung löscht den aktuellen Gerätestatus und die Daten nicht vollständig.</span><span class="sxs-lookup"><span data-stu-id="2f3e3-160">A soft reset does not completely clear current device state and data.</span></span> <span data-ttu-id="2f3e3-161">Die genaue Semantik ist abhängig vom Gerät und den Protokollen und Mechanismen, die für die Kommunikation mit dem Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2f3e3-161">Exact semantics are dependent on the device and on the protocols and mechanisms used to communicate to it.</span></span>

<span data-ttu-id="2f3e3-162">Diese Eigenschaft wird von [**CIM \_ controlledby**](cim-controlledby.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2f3e3-162">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2f3e3-163">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2f3e3-163">Remarks</span></span>

<span data-ttu-id="2f3e3-164">Die **Win32- \_ idecontrollerdevice** -Klasse wird von [**CIM \_ controlledby**](cim-controlledby.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="2f3e3-164">The **Win32\_IDEControllerDevice** class is derived from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2f3e3-165">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2f3e3-165">Requirements</span></span>



| <span data-ttu-id="2f3e3-166">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2f3e3-166">Requirement</span></span> | <span data-ttu-id="2f3e3-167">Wert</span><span class="sxs-lookup"><span data-stu-id="2f3e3-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f3e3-168">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2f3e3-168">Minimum supported client</span></span><br/> | <span data-ttu-id="2f3e3-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2f3e3-169">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2f3e3-170">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2f3e3-170">Minimum supported server</span></span><br/> | <span data-ttu-id="2f3e3-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2f3e3-171">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2f3e3-172">Namespace</span><span class="sxs-lookup"><span data-stu-id="2f3e3-172">Namespace</span></span><br/>                | <span data-ttu-id="2f3e3-173">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="2f3e3-173">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2f3e3-174">MOF</span><span class="sxs-lookup"><span data-stu-id="2f3e3-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2f3e3-175"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2f3e3-175"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2f3e3-176">DLL</span><span class="sxs-lookup"><span data-stu-id="2f3e3-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f3e3-177"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f3e3-177"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f3e3-178">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2f3e3-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f3e3-179">**CIM- \_ controlledby**</span><span class="sxs-lookup"><span data-stu-id="2f3e3-179">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> <dt>

[<span data-ttu-id="2f3e3-180">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="2f3e3-180">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

