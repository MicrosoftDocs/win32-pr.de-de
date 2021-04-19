---
description: Die \_ WMI-Klasse "Win32 potsmodemtoserialport Association" verknüpft ein Modem mit dem seriellen Anschluss, den das Modem verwendet.
ms.assetid: 4dbde5ae-f785-4d2d-80d9-508effd72cf2
ms.tgt_platform: multiple
title: Win32_POTSModemToSerialPort-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_POTSModemToSerialPort
- Win32_POTSModemToSerialPort.NegotiatedDataWidth
- Win32_POTSModemToSerialPort.NegotiatedSpeed
- Win32_POTSModemToSerialPort.AccessState
- Win32_POTSModemToSerialPort.NumberOfHardResets
- Win32_POTSModemToSerialPort.NumberOfSoftResets
- Win32_POTSModemToSerialPort.Dependent
- Win32_POTSModemToSerialPort.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0a1e6128ffde7afce0132dd4415e4eca1f06b5cb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342598"
---
# <a name="win32_potsmodemtoserialport-class"></a><span data-ttu-id="d52f5-103">Win32- \_ Klasse "potsmudemtoserialport"</span><span class="sxs-lookup"><span data-stu-id="d52f5-103">Win32\_POTSModemToSerialPort class</span></span>

<span data-ttu-id="d52f5-104">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) " **Win32 \_ potsmodemtoserialport** Association" verknüpft ein Modem mit dem seriellen Anschluss, den das Modem verwendet.</span><span class="sxs-lookup"><span data-stu-id="d52f5-104">The **Win32\_POTSModemToSerialPort** association [WMI class](../wmisdk/retrieving-a-class.md) relates a modem to the serial port the modem uses.</span></span>

<span data-ttu-id="d52f5-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d52f5-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="d52f5-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="d52f5-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d52f5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d52f5-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4B6-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_POTSModemToSerialPort : CIM_ControlledBy
{
  uint32               NegotiatedDataWidth;
  uint64               NegotiatedSpeed;
  uint16               AccessState;
  uint32               NumberOfHardResets;
  uint32               NumberOfSoftResets;
  Win32_POTSModem  REF Dependent;
  Win32_SerialPort REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="d52f5-108">Member</span><span class="sxs-lookup"><span data-stu-id="d52f5-108">Members</span></span>

<span data-ttu-id="d52f5-109">Die Win32-Klasse " **\_ potspordemtoserialport** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d52f5-109">The **Win32\_POTSModemToSerialPort** class has these types of members:</span></span>

-   [<span data-ttu-id="d52f5-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d52f5-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d52f5-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d52f5-111">Properties</span></span>

<span data-ttu-id="d52f5-112">Die Win32-Klasse " **\_ potspordemtoserialport** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d52f5-112">The **Win32\_POTSModemToSerialPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d52f5-113">**Accessstate**</span><span class="sxs-lookup"><span data-stu-id="d52f5-113">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d52f5-114">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d52f5-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d52f5-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d52f5-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d52f5-116">Gibt an, ob der Controller aktiv auf das Gerät zugreift oder darauf zugreift.</span><span class="sxs-lookup"><span data-stu-id="d52f5-116">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="d52f5-117">Diese Informationen sind erforderlich, wenn ein logisches Gerät durch mehrere Controller befohlen werden kann oder darauf zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="d52f5-117">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<span data-ttu-id="d52f5-118">Diese Eigenschaft wird von [**CIM \_ controlledby**](cim-controlledby.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d52f5-118">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d52f5-119">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="d52f5-119">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="d52f5-120">**Aktiv** (1)</span><span class="sxs-lookup"><span data-stu-id="d52f5-120">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="d52f5-121">**Inaktiv** (2)</span><span class="sxs-lookup"><span data-stu-id="d52f5-121">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d52f5-122">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="d52f5-122">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d52f5-123">Datentyp: **Win32- \_ SerialPort**</span><span class="sxs-lookup"><span data-stu-id="d52f5-123">Data type: **Win32\_SerialPort**</span></span>
</dt> <dt>

<span data-ttu-id="d52f5-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d52f5-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d52f5-125">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Vorgänger"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ SerialPort")</span><span class="sxs-lookup"><span data-stu-id="d52f5-125">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_SerialPort")</span></span>
</dt> </dl>

<span data-ttu-id="d52f5-126">Ein [**Win32- \_ SerialPort**](win32-serialport.md) , der den vom Modem verwendeten seriellen Anschluss darstellt.</span><span class="sxs-lookup"><span data-stu-id="d52f5-126">A [**Win32\_SerialPort**](win32-serialport.md) that represents the serial port used by the modem.</span></span>

</dd> <dt>

<span data-ttu-id="d52f5-127">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="d52f5-127">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d52f5-128">Datentyp: **Win32- \_ potsmodem**</span><span class="sxs-lookup"><span data-stu-id="d52f5-128">Data type: **Win32\_POTSModem**</span></span>
</dt> <dt>

<span data-ttu-id="d52f5-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d52f5-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d52f5-130">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ potsmodem")</span><span class="sxs-lookup"><span data-stu-id="d52f5-130">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_POTSModem")</span></span>
</dt> </dl>

<span data-ttu-id="d52f5-131">Ein [**Win32- \_ Modem Modem**](win32-potsmodem.md) , das das POTS-Modem mit dem seriellen Anschluss darstellt.</span><span class="sxs-lookup"><span data-stu-id="d52f5-131">A [**Win32\_POTSModem**](win32-potsmodem.md) that represents the POTS modem using the serial port.</span></span>

</dd> <dt>

<span data-ttu-id="d52f5-132">**Aushandateddatawidth**</span><span class="sxs-lookup"><span data-stu-id="d52f5-132">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d52f5-133">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d52f5-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d52f5-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d52f5-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d52f5-135">Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Bits")</span><span class="sxs-lookup"><span data-stu-id="d52f5-135">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="d52f5-136">Wenn mehrere Bus-oder Verbindungsdaten breiten möglich sind, definiert diese Eigenschaft die jeweils verwendete Eigenschaft zwischen den Geräten.</span><span class="sxs-lookup"><span data-stu-id="d52f5-136">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="d52f5-137">Die Daten Breite wird in Bits angegeben.</span><span class="sxs-lookup"><span data-stu-id="d52f5-137">Data width is specified in bits.</span></span> <span data-ttu-id="d52f5-138">Wenn die Daten Breite nicht ausgehandelt wird oder diese Informationen für die Geräteverwaltung nicht verfügbar oder wichtig sind, sollte die-Eigenschaft auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="d52f5-138">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="d52f5-139">Diese Eigenschaft wird von CIM-Geräte [**\_ erviceconnetction**](cim-deviceconnection.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d52f5-139">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="d52f5-140">**Aushandatedspeed**</span><span class="sxs-lookup"><span data-stu-id="d52f5-140">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d52f5-141">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d52f5-141">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d52f5-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d52f5-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d52f5-143">Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Bits pro Sekunde")</span><span class="sxs-lookup"><span data-stu-id="d52f5-143">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="d52f5-144">Wenn mehrere Bus-oder Verbindungsgeschwindigkeiten möglich sind, definiert diese Eigenschaft die zwischen den Geräten verwendete.</span><span class="sxs-lookup"><span data-stu-id="d52f5-144">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="d52f5-145">Die Geschwindigkeit wird in Bits pro Sekunde angegeben.</span><span class="sxs-lookup"><span data-stu-id="d52f5-145">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="d52f5-146">Wenn Verbindungs-oder Busgeschwindigkeiten nicht ausgehandelt werden oder diese Informationen für die Geräteverwaltung nicht verfügbar oder wichtig sind, sollte die-Eigenschaft auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="d52f5-146">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="d52f5-147">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="d52f5-147">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="d52f5-148">Diese Eigenschaft wird von CIM-Geräte [**\_ erviceconnetction**](cim-deviceconnection.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d52f5-148">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="d52f5-149">**Anzahlersätze**</span><span class="sxs-lookup"><span data-stu-id="d52f5-149">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d52f5-150">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d52f5-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d52f5-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d52f5-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d52f5-152">Anzahl von Festplatten, die vom Controller ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d52f5-152">Number of hard resets issued by the controller.</span></span> <span data-ttu-id="d52f5-153">Bei einer festen zurück setzung wird das Gerät wieder in den Initialisierungs-oder Startzustand versetzt.</span><span class="sxs-lookup"><span data-stu-id="d52f5-153">A hard reset returns the device to its initialization or boot-up state.</span></span> <span data-ttu-id="d52f5-154">Alle internen Geräte Zustandsinformationen und Daten gehen verloren.</span><span class="sxs-lookup"><span data-stu-id="d52f5-154">All internal device state information and data are lost.</span></span>

<span data-ttu-id="d52f5-155">Diese Eigenschaft wird von [**CIM \_ controlledby**](cim-controlledby.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d52f5-155">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="d52f5-156">**Anzahlermengen**</span><span class="sxs-lookup"><span data-stu-id="d52f5-156">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d52f5-157">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d52f5-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d52f5-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d52f5-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d52f5-159">Anzahl der vom Controller ausgestellten Soft-zurück Stellungen.</span><span class="sxs-lookup"><span data-stu-id="d52f5-159">Number of soft resets issued by the controller.</span></span> <span data-ttu-id="d52f5-160">Eine weiche zurück Setzung löscht den aktuellen Gerätestatus und die Daten nicht vollständig.</span><span class="sxs-lookup"><span data-stu-id="d52f5-160">A soft reset does not completely clear current device state and data.</span></span> <span data-ttu-id="d52f5-161">Die genaue Semantik ist abhängig vom Gerät und den Protokollen und Mechanismen, die für die Kommunikation mit dem Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d52f5-161">Exact semantics are dependent on the device and on the protocols and mechanisms used to communicate to it.</span></span>

<span data-ttu-id="d52f5-162">Diese Eigenschaft wird von [**CIM \_ controlledby**](cim-controlledby.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d52f5-162">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d52f5-163">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d52f5-163">Remarks</span></span>

<span data-ttu-id="d52f5-164">Die Win32-Klasse " **\_ potsmudemtoserialport** " ist von [**CIM \_ controlledby**](cim-controlledby.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="d52f5-164">The **Win32\_POTSModemToSerialPort** class is derived from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d52f5-165">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d52f5-165">Requirements</span></span>



| <span data-ttu-id="d52f5-166">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d52f5-166">Requirement</span></span> | <span data-ttu-id="d52f5-167">Wert</span><span class="sxs-lookup"><span data-stu-id="d52f5-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d52f5-168">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d52f5-168">Minimum supported client</span></span><br/> | <span data-ttu-id="d52f5-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d52f5-169">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d52f5-170">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d52f5-170">Minimum supported server</span></span><br/> | <span data-ttu-id="d52f5-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d52f5-171">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d52f5-172">Namespace</span><span class="sxs-lookup"><span data-stu-id="d52f5-172">Namespace</span></span><br/>                | <span data-ttu-id="d52f5-173">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d52f5-173">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d52f5-174">MOF</span><span class="sxs-lookup"><span data-stu-id="d52f5-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d52f5-175"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="d52f5-175"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d52f5-176">DLL</span><span class="sxs-lookup"><span data-stu-id="d52f5-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d52f5-177"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d52f5-177"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d52f5-178">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d52f5-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d52f5-179">**CIM- \_ controlledby**</span><span class="sxs-lookup"><span data-stu-id="d52f5-179">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> <dt>

[<span data-ttu-id="d52f5-180">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="d52f5-180">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
