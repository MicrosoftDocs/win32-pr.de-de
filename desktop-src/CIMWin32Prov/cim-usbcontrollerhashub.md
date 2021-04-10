---
description: Die CIM- \_ Klasse "-Klasse" definiert die Hubs, die dem USB-Controller nachgelagert werden.
ms.assetid: 38bc0342-3ff0-42c8-9c1e-ea5a5822e1d3
ms.tgt_platform: multiple
title: CIM_USBControllerHasHub-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_USBControllerHasHub
- CIM_USBControllerHasHub.NegotiatedDataWidth
- CIM_USBControllerHasHub.NegotiatedSpeed
- CIM_USBControllerHasHub.AccessState
- CIM_USBControllerHasHub.NumberOfHardResets
- CIM_USBControllerHasHub.NumberOfSoftResets
- CIM_USBControllerHasHub.Dependent
- CIM_USBControllerHasHub.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ba0f6d9a618a194faa8d16f9b2f53c6ce10653cf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125827"
---
# <a name="cim_usbcontrollerhashub-class"></a><span data-ttu-id="6250b-103">CIM-Klasse "-Start \_ Controller Controller hashub"</span><span class="sxs-lookup"><span data-stu-id="6250b-103">CIM\_USBControllerHasHub class</span></span>

<span data-ttu-id="6250b-104">Die **CIM \_** -Klasse "-Klasse" definiert die Hubs, die dem USB-Controller nachgelagert werden.</span><span class="sxs-lookup"><span data-stu-id="6250b-104">The **CIM\_USBControllerHasHub** class defines the hubs that are downstream of the USB controller.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6250b-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="6250b-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6250b-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6250b-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6250b-107">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6250b-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="6250b-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="6250b-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6250b-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="6250b-109">Syntax</span></span>

``` syntax
[AMENDMENT]
class CIM_USBControllerHasHub : CIM_ControlledBy
{
  uint32                NegotiatedDataWidth;
  uint64                NegotiatedSpeed;
  uint16                AccessState;
  uint32                NumberOfHardResets;
  uint32                NumberOfSoftResets;
  CIM_USBHub        REF Dependent;
  CIM_USBController REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="6250b-110">Member</span><span class="sxs-lookup"><span data-stu-id="6250b-110">Members</span></span>

<span data-ttu-id="6250b-111">Die **CIM \_** -Klasse "-Klasse":</span><span class="sxs-lookup"><span data-stu-id="6250b-111">The **CIM\_USBControllerHasHub** class has these types of members:</span></span>

-   [<span data-ttu-id="6250b-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6250b-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6250b-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6250b-113">Properties</span></span>

<span data-ttu-id="6250b-114">Die **CIM \_** -Klasse "-Klasse" hat diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6250b-114">The **CIM\_USBControllerHasHub** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6250b-115">**Accessstate**</span><span class="sxs-lookup"><span data-stu-id="6250b-115">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6250b-116">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6250b-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6250b-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6250b-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6250b-118">Gibt an, ob der Controller aktiv auf das Gerät zugreift oder darauf zugreift.</span><span class="sxs-lookup"><span data-stu-id="6250b-118">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="6250b-119">Diese Informationen sind erforderlich, wenn ein logisches Gerät durch mehrere Controller befohlen werden kann oder darauf zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="6250b-119">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<span data-ttu-id="6250b-120">Diese Eigenschaft wird von [**CIM \_ controlledby**](cim-controlledby.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6250b-120">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6250b-121">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="6250b-121">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="6250b-122">**Aktiv** (1)</span><span class="sxs-lookup"><span data-stu-id="6250b-122">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="6250b-123">**Inaktiv** (2)</span><span class="sxs-lookup"><span data-stu-id="6250b-123">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6250b-124">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="6250b-124">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6250b-125">Datentyp: **CIM \_** -Start Controller</span><span class="sxs-lookup"><span data-stu-id="6250b-125">Data type: **CIM\_USBController**</span></span>
</dt> <dt>

<span data-ttu-id="6250b-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6250b-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6250b-127">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="6250b-127">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="6250b-128">Ein [**CIM \_**](cim-usbcontroller.md) -Start Controller, der den "Start Controller" beschreibt.</span><span class="sxs-lookup"><span data-stu-id="6250b-128">A [**CIM\_USBController**](cim-usbcontroller.md) describing the USBController.</span></span>

</dd> <dt>

<span data-ttu-id="6250b-129">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="6250b-129">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6250b-130">Datentyp: **CIM \_** -Startseite</span><span class="sxs-lookup"><span data-stu-id="6250b-130">Data type: **CIM\_USBHub**</span></span>
</dt> <dt>

<span data-ttu-id="6250b-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6250b-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6250b-132">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="6250b-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="6250b-133">Ein [**CIM \_**](cim-usbhub.md) -Befehl, der den dem Controller zugeordneten "dem Controller" zugeordneten "Start" beschreibt.</span><span class="sxs-lookup"><span data-stu-id="6250b-133">A [**CIM\_USBHub**](cim-usbhub.md) describing the USBHub that is associated with the Controller.</span></span>

</dd> <dt>

<span data-ttu-id="6250b-134">**Aushandateddatawidth**</span><span class="sxs-lookup"><span data-stu-id="6250b-134">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6250b-135">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6250b-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6250b-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6250b-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6250b-137">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits")</span><span class="sxs-lookup"><span data-stu-id="6250b-137">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="6250b-138">Wenn mehrere Bus-oder Verbindungsdaten breiten möglich sind, definiert diese Eigenschaft die jeweils verwendete Eigenschaft zwischen den Geräten.</span><span class="sxs-lookup"><span data-stu-id="6250b-138">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="6250b-139">Die Daten Breite wird in Bits angegeben.</span><span class="sxs-lookup"><span data-stu-id="6250b-139">Data width is specified in bits.</span></span> <span data-ttu-id="6250b-140">Wenn die Daten Breite nicht ausgehandelt wird oder diese Informationen für die Geräteverwaltung nicht verfügbar oder wichtig sind, sollte die-Eigenschaft auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="6250b-140">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="6250b-141">Diese Eigenschaft wird von CIM-Geräte [**\_ erviceconnetction**](cim-deviceconnection.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6250b-141">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="6250b-142">**Aushandatedspeed**</span><span class="sxs-lookup"><span data-stu-id="6250b-142">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6250b-143">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6250b-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6250b-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6250b-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6250b-145">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits pro Sekunde")</span><span class="sxs-lookup"><span data-stu-id="6250b-145">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="6250b-146">Wenn mehrere Bus-oder Verbindungsgeschwindigkeiten möglich sind, definiert diese Eigenschaft die zwischen den Geräten verwendete.</span><span class="sxs-lookup"><span data-stu-id="6250b-146">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="6250b-147">Die Geschwindigkeit wird in Bits pro Sekunde angegeben.</span><span class="sxs-lookup"><span data-stu-id="6250b-147">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="6250b-148">Wenn Verbindungs-oder Busgeschwindigkeiten nicht ausgehandelt werden oder diese Informationen für die Geräteverwaltung nicht verfügbar oder wichtig sind, sollte die-Eigenschaft auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="6250b-148">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="6250b-149">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="6250b-149">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="6250b-150">Diese Eigenschaft wird von CIM-Geräte [**\_ erviceconnetction**](cim-deviceconnection.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6250b-150">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="6250b-151">**Anzahlersätze**</span><span class="sxs-lookup"><span data-stu-id="6250b-151">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6250b-152">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6250b-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6250b-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6250b-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6250b-154">Anzahl von Festplatten, die vom Controller ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6250b-154">Number of hard resets issued by the controller.</span></span> <span data-ttu-id="6250b-155">Bei einer festen zurück setzung wird das Gerät wieder in den Initialisierungs-oder Startzustand versetzt.</span><span class="sxs-lookup"><span data-stu-id="6250b-155">A hard reset returns the device to its initialization or boot-up state.</span></span> <span data-ttu-id="6250b-156">Alle internen Geräte Zustandsinformationen und Daten gehen verloren.</span><span class="sxs-lookup"><span data-stu-id="6250b-156">All internal device state information and data are lost.</span></span>

<span data-ttu-id="6250b-157">Diese Eigenschaft wird von [**CIM \_ controlledby**](cim-controlledby.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6250b-157">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="6250b-158">**Anzahlermengen**</span><span class="sxs-lookup"><span data-stu-id="6250b-158">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6250b-159">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6250b-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6250b-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6250b-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6250b-161">Anzahl der vom Controller ausgestellten Soft-zurück Stellungen.</span><span class="sxs-lookup"><span data-stu-id="6250b-161">Number of soft resets issued by the controller.</span></span> <span data-ttu-id="6250b-162">Eine weiche zurück Setzung löscht den aktuellen Gerätestatus und die Daten nicht vollständig.</span><span class="sxs-lookup"><span data-stu-id="6250b-162">A soft reset does not completely clear current device state and data.</span></span> <span data-ttu-id="6250b-163">Die genaue Semantik ist abhängig vom Gerät und den Protokollen und Mechanismen, die für die Kommunikation mit dem Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6250b-163">Exact semantics are dependent on the device and on the protocols and mechanisms used to communicate to it.</span></span>

<span data-ttu-id="6250b-164">Diese Eigenschaft wird von [**CIM \_ controlledby**](cim-controlledby.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6250b-164">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6250b-165">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6250b-165">Remarks</span></span>

<span data-ttu-id="6250b-166">Die CIM-Klasse "-Start **\_ Controller Controller Hash** " ist von [**CIM \_ controlledby**](cim-controlledby.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="6250b-166">The **CIM\_USBControllerHasHub** class is derived from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<span data-ttu-id="6250b-167">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="6250b-167">WMI does not implement this class.</span></span> <span data-ttu-id="6250b-168">Informationen zu WMI-Klassen, die von **\_ CIM**-Methode "-Methode" erstellt wurden, finden Sie unter [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="6250b-168">For WMI classes derived from **CIM\_USBControllerHasHub**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="6250b-169">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="6250b-169">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6250b-170">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="6250b-170">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6250b-171">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6250b-171">Requirements</span></span>



| <span data-ttu-id="6250b-172">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6250b-172">Requirement</span></span> | <span data-ttu-id="6250b-173">Wert</span><span class="sxs-lookup"><span data-stu-id="6250b-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6250b-174">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6250b-174">Minimum supported client</span></span><br/> | <span data-ttu-id="6250b-175">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6250b-175">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6250b-176">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6250b-176">Minimum supported server</span></span><br/> | <span data-ttu-id="6250b-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6250b-177">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6250b-178">Namespace</span><span class="sxs-lookup"><span data-stu-id="6250b-178">Namespace</span></span><br/>                | <span data-ttu-id="6250b-179">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="6250b-179">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6250b-180">MOF</span><span class="sxs-lookup"><span data-stu-id="6250b-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6250b-181"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="6250b-181"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6250b-182">DLL</span><span class="sxs-lookup"><span data-stu-id="6250b-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6250b-183"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6250b-183"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6250b-184">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6250b-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6250b-185">**CIM- \_ controlledby**</span><span class="sxs-lookup"><span data-stu-id="6250b-185">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> </dl>

 

