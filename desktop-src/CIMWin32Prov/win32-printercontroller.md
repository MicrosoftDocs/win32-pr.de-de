---
description: Die \_ WMI-Klasse für die Win32 printercontroller-Zuordnung bezieht sich auf einen Drucker und das lokale Gerät, mit dem der Drucker verbunden ist. Beachten Sie, dass diese Klasse nur Instanzen für lokale Drucker zurückgibt.
ms.assetid: fb483b28-11f1-4153-893e-492f71763712
ms.tgt_platform: multiple
title: Win32_PrinterController-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterController
- Win32_PrinterController.AccessState
- Win32_PrinterController.Antecedent
- Win32_PrinterController.Dependent
- Win32_PrinterController.NegotiatedDataWidth
- Win32_PrinterController.NegotiatedSpeed
- Win32_PrinterController.NumberOfHardResets
- Win32_PrinterController.NumberOfSoftResets
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1ee38b827aed2dfffe1e7ef4f5049b16eee50791
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861179"
---
# <a name="win32_printercontroller-class"></a><span data-ttu-id="971b0-104">Win32 \_ printercontroller-Klasse</span><span class="sxs-lookup"><span data-stu-id="971b0-104">Win32\_PrinterController class</span></span>

<span data-ttu-id="971b0-105">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) für die **Win32 \_ printercontroller** -Zuordnung bezieht sich auf einen Drucker und das lokale Gerät, mit dem der Drucker verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="971b0-105">The **Win32\_PrinterController** association [WMI class](../wmisdk/retrieving-a-class.md) relates a printer and the local device to which the printer is connected.</span></span> <span data-ttu-id="971b0-106">Beachten Sie, dass diese Klasse nur Instanzen für lokale Drucker zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="971b0-106">Note that this class only returns instances for local printers.</span></span>

<span data-ttu-id="971b0-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="971b0-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="971b0-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="971b0-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="971b0-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="971b0-109">Syntax</span></span>

``` syntax
class Win32_PrinterController : CIM_ControlledBy
{
  uint16             AccessState;
  CIM_Controller REF Antecedent;
  Win32_Printer  REF Dependent;
  uint32             NegotiatedDataWidth;
  uint64             NegotiatedSpeed;
  uint32             NumberOfHardResets;
  uint32             NumberOfSoftResets;
};
```

## <a name="members"></a><span data-ttu-id="971b0-110">Member</span><span class="sxs-lookup"><span data-stu-id="971b0-110">Members</span></span>

<span data-ttu-id="971b0-111">Die **Win32 \_ printercontroller** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="971b0-111">The **Win32\_PrinterController** class has these types of members:</span></span>

-   [<span data-ttu-id="971b0-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="971b0-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="971b0-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="971b0-113">Properties</span></span>

<span data-ttu-id="971b0-114">Die **Win32 \_ printercontroller** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="971b0-114">The **Win32\_PrinterController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="971b0-115">**Accessstate**</span><span class="sxs-lookup"><span data-stu-id="971b0-115">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="971b0-116">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="971b0-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="971b0-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="971b0-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="971b0-118">Status des Controller Zugriffs auf das Gerät.</span><span class="sxs-lookup"><span data-stu-id="971b0-118">State of the controller access to the device.</span></span> <span data-ttu-id="971b0-119">Diese Informationen sind erforderlich, wenn ein logisches Gerät durch mehrere Controller befohlen werden kann oder darauf zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="971b0-119">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<span data-ttu-id="971b0-120">Diese Eigenschaft wird von [**CIM \_ controlledby**](cim-controlledby.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="971b0-120">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="971b0-121"><span id="0"></span>**1,0**</span><span class="sxs-lookup"><span data-stu-id="971b0-121"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="971b0-122">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="971b0-122">Unknown</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="971b0-123"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="971b0-123"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="971b0-124">Aktiv</span><span class="sxs-lookup"><span data-stu-id="971b0-124">Active</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="971b0-125"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="971b0-125"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="971b0-126">Inaktiv</span><span class="sxs-lookup"><span data-stu-id="971b0-126">Inactive</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="971b0-127">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="971b0-127">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="971b0-128">Datentyp: **CIM- \_ Controller**</span><span class="sxs-lookup"><span data-stu-id="971b0-128">Data type: **CIM\_Controller**</span></span>
</dt> <dt>

<span data-ttu-id="971b0-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="971b0-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="971b0-130">Qualifizierer: [ **Schlüssel**](../wmisdk/standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="971b0-130">Qualifiers: [**Key**](../wmisdk/standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="971b0-131">Verweis auf die [**CIM- \_ Controller**](cim-controller.md) Instanz, die das diesem Drucker zugeordnete lokale Gerät darstellt.</span><span class="sxs-lookup"><span data-stu-id="971b0-131">Reference to the [**CIM\_Controller**](cim-controller.md) instance representing the local device associated with this printer.</span></span>

<span data-ttu-id="971b0-132">Diese Eigenschaft wird von der [**CIM- \_ Abhängigkeit**](cim-dependency.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="971b0-132">This property is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

</dd> <dt>

<span data-ttu-id="971b0-133">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="971b0-133">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="971b0-134">Datentyp: **Win32- \_ Drucker**</span><span class="sxs-lookup"><span data-stu-id="971b0-134">Data type: **Win32\_Printer**</span></span>
</dt> <dt>

<span data-ttu-id="971b0-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="971b0-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="971b0-136">Qualifizierer: [ **Schlüssel**](../wmisdk/standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="971b0-136">Qualifiers: [**Key**](../wmisdk/standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="971b0-137">Verweis auf die [**Win32- \_ Drucker**](win32-printer.md) Instanz, die den Drucker darstellt, der dem lokalen Gerät zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="971b0-137">Reference to the [**Win32\_Printer**](win32-printer.md) instance representing the printer associated with the local device.</span></span>

<span data-ttu-id="971b0-138">Diese Eigenschaft wird von der [**CIM- \_ Abhängigkeit**](cim-dependency.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="971b0-138">This property is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

</dd> <dt>

<span data-ttu-id="971b0-139">**Aushandateddatawidth**</span><span class="sxs-lookup"><span data-stu-id="971b0-139">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="971b0-140">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="971b0-140">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="971b0-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="971b0-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="971b0-142">Zwischen Geräten verwendete Daten Breite (wenn mehrere Bus-oder Verbindungsdaten breiten möglich sind).</span><span class="sxs-lookup"><span data-stu-id="971b0-142">Data width in use between devices (when several bus or connection data widths are possible).</span></span> <span data-ttu-id="971b0-143">Die Daten Breite wird in Bits angegeben.</span><span class="sxs-lookup"><span data-stu-id="971b0-143">Data width is specified in bits.</span></span> <span data-ttu-id="971b0-144">Wenn die Daten Breite nicht ausgehandelt wird oder diese Informationen für die Geräteverwaltung nicht verfügbar oder wichtig sind, sollte die-Eigenschaft auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="971b0-144">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="971b0-145">Diese Eigenschaft wird von CIM-Geräte [**\_ erviceconnetction**](cim-deviceconnection.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="971b0-145">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="971b0-146">**Aushandatedspeed**</span><span class="sxs-lookup"><span data-stu-id="971b0-146">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="971b0-147">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="971b0-147">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="971b0-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="971b0-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="971b0-149">Verwendungs Geschwindigkeit zwischen Geräten (wenn mehrere Bus-oder Verbindungsgeschwindigkeiten möglich sind).</span><span class="sxs-lookup"><span data-stu-id="971b0-149">Speed in use between devices (when several bus or connection speeds are possible).</span></span> <span data-ttu-id="971b0-150">Die Geschwindigkeit wird in Bits pro Sekunde angegeben.</span><span class="sxs-lookup"><span data-stu-id="971b0-150">Speed is specified in bits per second.</span></span> <span data-ttu-id="971b0-151">Wenn Verbindungs-oder Busgeschwindigkeiten nicht ausgehandelt werden oder diese Informationen für die Geräteverwaltung nicht verfügbar oder wichtig sind, sollte die-Eigenschaft auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="971b0-151">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="971b0-152">Diese Eigenschaft wird von CIM-Geräte [**\_ erviceconnetction**](cim-deviceconnection.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="971b0-152">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

<span data-ttu-id="971b0-153">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="971b0-153">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="971b0-154">**Anzahlersätze**</span><span class="sxs-lookup"><span data-stu-id="971b0-154">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="971b0-155">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="971b0-155">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="971b0-156">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="971b0-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="971b0-157">Anzahl von Festplatten, die vom Controller ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="971b0-157">Number of hard resets issued by the controller.</span></span>

<span data-ttu-id="971b0-158">Diese Eigenschaft wird von [**CIM \_ controlledby**](cim-controlledby.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="971b0-158">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="971b0-159">**Anzahlermengen**</span><span class="sxs-lookup"><span data-stu-id="971b0-159">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="971b0-160">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="971b0-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="971b0-161">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="971b0-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="971b0-162">Anzahl der vom Controller ausgestellten Soft-zurück Stellungen.</span><span class="sxs-lookup"><span data-stu-id="971b0-162">Number of soft resets issued by the controller.</span></span>

<span data-ttu-id="971b0-163">Diese Eigenschaft wird von [**CIM \_ controlledby**](cim-controlledby.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="971b0-163">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="971b0-164">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="971b0-164">Remarks</span></span>

<span data-ttu-id="971b0-165">Die **Win32 \_ printercontroller** -Klasse wird von [**CIM \_ controlledby**](cim-controlledby.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="971b0-165">The **Win32\_PrinterController** class is derived from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="971b0-166">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="971b0-166">Requirements</span></span>



| <span data-ttu-id="971b0-167">Anforderung</span><span class="sxs-lookup"><span data-stu-id="971b0-167">Requirement</span></span> | <span data-ttu-id="971b0-168">Wert</span><span class="sxs-lookup"><span data-stu-id="971b0-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="971b0-169">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="971b0-169">Minimum supported client</span></span><br/> | <span data-ttu-id="971b0-170">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="971b0-170">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="971b0-171">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="971b0-171">Minimum supported server</span></span><br/> | <span data-ttu-id="971b0-172">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="971b0-172">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="971b0-173">Namespace</span><span class="sxs-lookup"><span data-stu-id="971b0-173">Namespace</span></span><br/>                | <span data-ttu-id="971b0-174">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="971b0-174">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="971b0-175">MOF</span><span class="sxs-lookup"><span data-stu-id="971b0-175">MOF</span></span><br/>                      | <dl> <span data-ttu-id="971b0-176"><dt>Win32 \_ Printer. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="971b0-176"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="971b0-177">DLL</span><span class="sxs-lookup"><span data-stu-id="971b0-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="971b0-178"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="971b0-178"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="971b0-179">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="971b0-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="971b0-180">**CIM- \_ controlledby**</span><span class="sxs-lookup"><span data-stu-id="971b0-180">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> <dt>

[<span data-ttu-id="971b0-181">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="971b0-181">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
