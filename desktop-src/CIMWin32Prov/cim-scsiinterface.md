---
description: Stellt eine CIM \_ controlledby-Beziehung dar, die angibt, auf welche Geräte über einen SCSI-Controller und die Zugriffs Eigenschaften zugegriffen wird.
ms.assetid: a036dbf9-f9ce-4c85-9184-fefcbe4583ba
ms.tgt_platform: multiple
title: CIM_SCSIInterface-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SCSIInterface
- CIM_SCSIInterface.NegotiatedDataWidth
- CIM_SCSIInterface.NegotiatedSpeed
- CIM_SCSIInterface.AccessState
- CIM_SCSIInterface.NumberOfHardResets
- CIM_SCSIInterface.NumberOfSoftResets
- CIM_SCSIInterface.Dependent
- CIM_SCSIInterface.Antecedent
- CIM_SCSIInterface.SCSIRetries
- CIM_SCSIInterface.SCSITimeouts
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1211b142681f15aa8b4d5e61c1d2165a59f5a62c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748593"
---
# <a name="cim_scsiinterface-class"></a><span data-ttu-id="68cc4-103">CIM \_ scsiinterface-Klasse</span><span class="sxs-lookup"><span data-stu-id="68cc4-103">CIM\_SCSIInterface class</span></span>

<span data-ttu-id="68cc4-104">Die **CIM- \_ scsiinterface** -Klasse stellt eine [**CIM- \_ controlledby**](cim-controlledby.md) -Beziehung dar, die angibt, auf welche Geräte über einen SCSI-Controller und die Zugriffs Eigenschaften zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="68cc4-104">The **CIM\_SCSIInterface** class represents a [**CIM\_ControlledBy**](cim-controlledby.md) relationship that indicates which devices are accessed through a SCSI controller and the access characteristics.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="68cc4-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="68cc4-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="68cc4-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="68cc4-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="68cc4-107">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="68cc4-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="68cc4-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="68cc4-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="68cc4-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="68cc4-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{7CE7448E-E3D4-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_SCSIInterface : CIM_ControlledBy
{
  uint32                 NegotiatedDataWidth;
  uint64                 NegotiatedSpeed;
  uint16                 AccessState;
  uint32                 NumberOfHardResets;
  uint32                 NumberOfSoftResets;
  CIM_LogicalDevice  REF Dependent;
  CIM_SCSIController REF Antecedent;
  uint32                 SCSIRetries;
  uint32                 SCSITimeouts;
};
```

## <a name="members"></a><span data-ttu-id="68cc4-110">Member</span><span class="sxs-lookup"><span data-stu-id="68cc4-110">Members</span></span>

<span data-ttu-id="68cc4-111">Die **CIM \_ scsiinterface** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="68cc4-111">The **CIM\_SCSIInterface** class has these types of members:</span></span>

-   [<span data-ttu-id="68cc4-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="68cc4-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="68cc4-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="68cc4-113">Properties</span></span>

<span data-ttu-id="68cc4-114">Die **CIM \_ scsiinterface** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="68cc4-114">The **CIM\_SCSIInterface** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="68cc4-115">**Accessstate**</span><span class="sxs-lookup"><span data-stu-id="68cc4-115">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68cc4-116">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="68cc4-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="68cc4-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="68cc4-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68cc4-118">Gibt an, ob der Controller aktiv auf das Gerät zugreift oder darauf zugreift.</span><span class="sxs-lookup"><span data-stu-id="68cc4-118">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="68cc4-119">Diese Informationen sind erforderlich, wenn ein logisches Gerät durch mehrere Controller befohlen werden kann oder darauf zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="68cc4-119">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<span data-ttu-id="68cc4-120">Diese Eigenschaft wird von [**CIM \_ controlledby**](cim-controlledby.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="68cc4-120">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="68cc4-121">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="68cc4-121">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="68cc4-122">**Aktiv** (1)</span><span class="sxs-lookup"><span data-stu-id="68cc4-122">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="68cc4-123">**Inaktiv** (2)</span><span class="sxs-lookup"><span data-stu-id="68cc4-123">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="68cc4-124">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="68cc4-124">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68cc4-125">Datentyp: **CIM \_ SCSIController**</span><span class="sxs-lookup"><span data-stu-id="68cc4-125">Data type: **CIM\_SCSIController**</span></span>
</dt> <dt>

<span data-ttu-id="68cc4-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="68cc4-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68cc4-127">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="68cc4-127">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="68cc4-128">Ein [**CIM- \_ SCSIController**](cim-scsicontroller.md) , der den SCSI-Controller beschreibt.</span><span class="sxs-lookup"><span data-stu-id="68cc4-128">A [**CIM\_SCSIController**](cim-scsicontroller.md) that describes the SCSI controller.</span></span>

</dd> <dt>

<span data-ttu-id="68cc4-129">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="68cc4-129">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68cc4-130">Datentyp: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="68cc4-130">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="68cc4-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="68cc4-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68cc4-132">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="68cc4-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="68cc4-133">Ein [**CIM \_ LogicalDevice**](cim-logicaldevice.md) , das das logische Gerät beschreibt.</span><span class="sxs-lookup"><span data-stu-id="68cc4-133">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="68cc4-134">**Aushandateddatawidth**</span><span class="sxs-lookup"><span data-stu-id="68cc4-134">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68cc4-135">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="68cc4-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="68cc4-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="68cc4-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68cc4-137">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits")</span><span class="sxs-lookup"><span data-stu-id="68cc4-137">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="68cc4-138">Wenn mehrere Bus-oder Verbindungsdaten breiten möglich sind, definiert diese Eigenschaft die jeweils verwendete Eigenschaft zwischen den Geräten.</span><span class="sxs-lookup"><span data-stu-id="68cc4-138">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="68cc4-139">Die Daten Breite wird in Bits angegeben.</span><span class="sxs-lookup"><span data-stu-id="68cc4-139">Data width is specified in bits.</span></span> <span data-ttu-id="68cc4-140">Wenn die Daten Breite nicht ausgehandelt wird oder diese Informationen für die Geräteverwaltung nicht verfügbar oder wichtig sind, sollte die-Eigenschaft auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="68cc4-140">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="68cc4-141">Diese Eigenschaft wird von CIM-Geräte [**\_ erviceconnetction**](cim-deviceconnection.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="68cc4-141">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="68cc4-142">**Aushandatedspeed**</span><span class="sxs-lookup"><span data-stu-id="68cc4-142">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68cc4-143">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="68cc4-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="68cc4-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="68cc4-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68cc4-145">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits pro Sekunde")</span><span class="sxs-lookup"><span data-stu-id="68cc4-145">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="68cc4-146">Wenn mehrere Bus-oder Verbindungsgeschwindigkeiten möglich sind, definiert diese Eigenschaft die zwischen den Geräten verwendete.</span><span class="sxs-lookup"><span data-stu-id="68cc4-146">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="68cc4-147">Die Geschwindigkeit wird in Bits pro Sekunde angegeben.</span><span class="sxs-lookup"><span data-stu-id="68cc4-147">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="68cc4-148">Wenn Verbindungs-oder Busgeschwindigkeiten nicht ausgehandelt werden oder diese Informationen für die Geräteverwaltung nicht verfügbar oder wichtig sind, sollte die-Eigenschaft auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="68cc4-148">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="68cc4-149">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="68cc4-149">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="68cc4-150">Diese Eigenschaft wird von CIM-Geräte [**\_ erviceconnetction**](cim-deviceconnection.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="68cc4-150">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="68cc4-151">**Anzahlersätze**</span><span class="sxs-lookup"><span data-stu-id="68cc4-151">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68cc4-152">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="68cc4-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="68cc4-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="68cc4-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68cc4-154">Anzahl von Festplatten, die vom Controller ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="68cc4-154">Number of hard resets issued by the controller.</span></span> <span data-ttu-id="68cc4-155">Bei einer festen zurück setzung wird das Gerät wieder in den Initialisierungs-oder Startzustand versetzt.</span><span class="sxs-lookup"><span data-stu-id="68cc4-155">A hard reset returns the device to its initialization or boot-up state.</span></span> <span data-ttu-id="68cc4-156">Alle internen Geräte Zustandsinformationen und Daten gehen verloren.</span><span class="sxs-lookup"><span data-stu-id="68cc4-156">All internal device state information and data are lost.</span></span>

<span data-ttu-id="68cc4-157">Diese Eigenschaft wird von [**CIM \_ controlledby**](cim-controlledby.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="68cc4-157">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="68cc4-158">**Anzahlermengen**</span><span class="sxs-lookup"><span data-stu-id="68cc4-158">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68cc4-159">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="68cc4-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="68cc4-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="68cc4-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68cc4-161">Anzahl der vom Controller ausgestellten Soft-zurück Stellungen.</span><span class="sxs-lookup"><span data-stu-id="68cc4-161">Number of soft resets issued by the controller.</span></span> <span data-ttu-id="68cc4-162">Eine weiche zurück Setzung löscht den aktuellen Gerätestatus und die Daten nicht vollständig.</span><span class="sxs-lookup"><span data-stu-id="68cc4-162">A soft reset does not completely clear current device state and data.</span></span> <span data-ttu-id="68cc4-163">Die genaue Semantik ist abhängig vom Gerät und den Protokollen und Mechanismen, die für die Kommunikation mit dem Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="68cc4-163">Exact semantics are dependent on the device and on the protocols and mechanisms used to communicate to it.</span></span>

<span data-ttu-id="68cc4-164">Diese Eigenschaft wird von [**CIM \_ controlledby**](cim-controlledby.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="68cc4-164">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="68cc4-165">**Scsiretries**</span><span class="sxs-lookup"><span data-stu-id="68cc4-165">**SCSIRetries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68cc4-166">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="68cc4-166">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="68cc4-167">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="68cc4-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68cc4-168">Anzahl der SCSI-Wiederholungen, die seit dem letzten hart oder vorläufig Zurücksetzen des kontrollierten Geräts aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="68cc4-168">Number of SCSI retries that have occurred since the last hard or soft reset related to the controlled device.</span></span> <span data-ttu-id="68cc4-169">Die Zeit der letzten zurück setzung wird in der **timeofdevicereset** -Eigenschaft angegeben, die von der [**CIM \_ controlledby**](cim-controlledby.md) -Zuordnung geerbt wurde.</span><span class="sxs-lookup"><span data-stu-id="68cc4-169">The time of the last reset is indicated in the **TimeOfDeviceReset** property, inherited from the [**CIM\_ControlledBy**](cim-controlledby.md) association.</span></span>

</dd> <dt>

<span data-ttu-id="68cc4-170">**Scsitimeouts**</span><span class="sxs-lookup"><span data-stu-id="68cc4-170">**SCSITimeouts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68cc4-171">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="68cc4-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="68cc4-172">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="68cc4-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68cc4-173">Anzahl der SCSI-Timeouts, die seit der letzten fest-oder Soft-zurück setzung auf das kontrollierte Gerät aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="68cc4-173">Number of SCSI time-outs that occurred since last hard or soft reset related to the controlled device.</span></span> <span data-ttu-id="68cc4-174">Die Zeit der letzten zurück setzung wird in der **timeofdevicereset** -Eigenschaft angegeben, die von der [**CIM \_ controlledby**](cim-controlledby.md) -Zuordnung geerbt wurde.</span><span class="sxs-lookup"><span data-stu-id="68cc4-174">The time of the last reset is indicated in the **TimeOfDeviceReset** property, inherited from the [**CIM\_ControlledBy**](cim-controlledby.md) association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="68cc4-175">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="68cc4-175">Remarks</span></span>

<span data-ttu-id="68cc4-176">Die **CIM- \_ scsiinterface** -Klasse wird von [**CIM \_ controlledby**](cim-controlledby.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="68cc4-176">The **CIM\_SCSIInterface** class is derived from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<span data-ttu-id="68cc4-177">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="68cc4-177">WMI does not implement this class.</span></span>

<span data-ttu-id="68cc4-178">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="68cc4-178">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="68cc4-179">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="68cc4-179">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="68cc4-180">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="68cc4-180">Requirements</span></span>



| <span data-ttu-id="68cc4-181">Anforderung</span><span class="sxs-lookup"><span data-stu-id="68cc4-181">Requirement</span></span> | <span data-ttu-id="68cc4-182">Wert</span><span class="sxs-lookup"><span data-stu-id="68cc4-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="68cc4-183">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="68cc4-183">Minimum supported client</span></span><br/> | <span data-ttu-id="68cc4-184">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="68cc4-184">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="68cc4-185">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="68cc4-185">Minimum supported server</span></span><br/> | <span data-ttu-id="68cc4-186">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="68cc4-186">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="68cc4-187">Namespace</span><span class="sxs-lookup"><span data-stu-id="68cc4-187">Namespace</span></span><br/>                | <span data-ttu-id="68cc4-188">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="68cc4-188">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="68cc4-189">MOF</span><span class="sxs-lookup"><span data-stu-id="68cc4-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="68cc4-190"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="68cc4-190"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="68cc4-191">DLL</span><span class="sxs-lookup"><span data-stu-id="68cc4-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68cc4-192"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68cc4-192"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68cc4-193">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="68cc4-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68cc4-194">**CIM- \_ controlledby**</span><span class="sxs-lookup"><span data-stu-id="68cc4-194">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> </dl>

 

