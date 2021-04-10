---
description: Die CIM \_ controlledby-Beziehung gibt an, welche Geräte von dem logischen Controller Gerät befohlen werden bzw. darauf zugreifen.
ms.assetid: 6aa4e088-32a0-4c88-bb82-341b6ab53b4c
ms.tgt_platform: multiple
title: CIM_ControlledBy-Klasse (cimwin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ControlledBy
- CIM_ControlledBy.NegotiatedDataWidth
- CIM_ControlledBy.NegotiatedSpeed
- CIM_ControlledBy.Dependent
- CIM_ControlledBy.Antecedent
- CIM_ControlledBy.AccessState
- CIM_ControlledBy.NumberOfHardResets
- CIM_ControlledBy.NumberOfSoftResets
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 315eea9fa207a92c3aa1add6fe021127dc3949d5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861032"
---
# <a name="cim_controlledby-class-cimwin32-wmi-providers"></a><span data-ttu-id="94232-103">CIM_ControlledBy-Klasse (cimwin32-WMI-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="94232-103">CIM_ControlledBy class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="94232-104">Die **CIM \_ controlledby** -Beziehung gibt an, welche Geräte von dem logischen Controller Gerät befohlen werden bzw. darauf zugreifen.</span><span class="sxs-lookup"><span data-stu-id="94232-104">The **CIM\_ControlledBy** relationship indicates which devices are commanded by, or accessed through, the controller logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="94232-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="94232-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="94232-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="94232-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="94232-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="94232-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="94232-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="94232-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="94232-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="94232-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C53D-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ControlledBy : CIM_DeviceConnection
{
  uint32                NegotiatedDataWidth;
  uint64                NegotiatedSpeed;
  CIM_LogicalDevice REF Dependent;
  CIM_Controller    REF Antecedent;
  uint16                AccessState;
  uint32                NumberOfHardResets;
  uint32                NumberOfSoftResets;
};
```

## <a name="members"></a><span data-ttu-id="94232-110">Member</span><span class="sxs-lookup"><span data-stu-id="94232-110">Members</span></span>

<span data-ttu-id="94232-111">Die **CIM \_ controlledby** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="94232-111">The **CIM\_ControlledBy** class has these types of members:</span></span>

-   [<span data-ttu-id="94232-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="94232-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="94232-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="94232-113">Properties</span></span>

<span data-ttu-id="94232-114">Die **CIM \_ controlledby** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="94232-114">The **CIM\_ControlledBy** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="94232-115">**Accessstate**</span><span class="sxs-lookup"><span data-stu-id="94232-115">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94232-116">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="94232-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="94232-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="94232-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94232-118">Gibt an, ob der Controller aktiv auf das Gerät zugreift oder darauf zugreift.</span><span class="sxs-lookup"><span data-stu-id="94232-118">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="94232-119">Diese Informationen sind erforderlich, wenn ein logisches Gerät durch mehrere Controller befohlen werden kann oder darauf zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="94232-119">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="94232-120">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="94232-120">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="94232-121">**Aktiv** (1)</span><span class="sxs-lookup"><span data-stu-id="94232-121">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="94232-122">**Inaktiv** (2)</span><span class="sxs-lookup"><span data-stu-id="94232-122">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="94232-123">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="94232-123">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94232-124">Datentyp: **CIM- \_ Controller**</span><span class="sxs-lookup"><span data-stu-id="94232-124">Data type: **CIM\_Controller**</span></span>
</dt> <dt>

<span data-ttu-id="94232-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="94232-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94232-126">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="94232-126">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="94232-127">Ein [**CIM- \_ Controller**](cim-controller.md) , der den Controller darstellt.</span><span class="sxs-lookup"><span data-stu-id="94232-127">A [**CIM\_Controller**](cim-controller.md) that represents the controller.</span></span>

</dd> <dt>

<span data-ttu-id="94232-128">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="94232-128">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94232-129">Datentyp: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="94232-129">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="94232-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="94232-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94232-131">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="94232-131">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="94232-132">Ein [**CIM \_ LogicalDevice**](cim-logicaldevice.md) , das das kontrollierte Gerät darstellt.</span><span class="sxs-lookup"><span data-stu-id="94232-132">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that represents the controlled device.</span></span>

</dd> <dt>

<span data-ttu-id="94232-133">**Aushandateddatawidth**</span><span class="sxs-lookup"><span data-stu-id="94232-133">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94232-134">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="94232-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="94232-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="94232-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94232-136">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits")</span><span class="sxs-lookup"><span data-stu-id="94232-136">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="94232-137">Wenn mehrere Bus-oder Verbindungsdaten breiten möglich sind, definiert diese Eigenschaft die jeweils verwendete Eigenschaft zwischen den Geräten.</span><span class="sxs-lookup"><span data-stu-id="94232-137">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="94232-138">Die Daten Breite wird in Bits angegeben.</span><span class="sxs-lookup"><span data-stu-id="94232-138">Data width is specified in bits.</span></span> <span data-ttu-id="94232-139">Wenn die Daten Breite nicht ausgehandelt wird oder diese Informationen für die Geräteverwaltung nicht verfügbar oder wichtig sind, sollte die-Eigenschaft auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="94232-139">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="94232-140">Diese Eigenschaft wird von CIM-Geräte [**\_ erviceconnetction**](cim-deviceconnection.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="94232-140">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="94232-141">**Aushandatedspeed**</span><span class="sxs-lookup"><span data-stu-id="94232-141">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94232-142">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="94232-142">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="94232-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="94232-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="94232-144">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits pro Sekunde")</span><span class="sxs-lookup"><span data-stu-id="94232-144">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="94232-145">Wenn mehrere Bus-oder Verbindungsgeschwindigkeiten möglich sind, definiert diese Eigenschaft die zwischen den Geräten verwendete.</span><span class="sxs-lookup"><span data-stu-id="94232-145">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="94232-146">Die Geschwindigkeit wird in Bits pro Sekunde angegeben.</span><span class="sxs-lookup"><span data-stu-id="94232-146">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="94232-147">Wenn Verbindungs-oder Busgeschwindigkeiten nicht ausgehandelt werden oder diese Informationen für die Geräteverwaltung nicht verfügbar oder wichtig sind, sollte die-Eigenschaft auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="94232-147">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="94232-148">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="94232-148">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="94232-149">Diese Eigenschaft wird von CIM-Geräte [**\_ erviceconnetction**](cim-deviceconnection.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="94232-149">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="94232-150">**Anzahlersätze**</span><span class="sxs-lookup"><span data-stu-id="94232-150">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94232-151">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="94232-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="94232-152">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="94232-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94232-153">Anzahl von Festplatten, die vom Controller ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="94232-153">Number of hard resets issued by the controller.</span></span> <span data-ttu-id="94232-154">Bei einer festen zurück setzung wird das Gerät wieder in den Initialisierungs-oder Startzustand versetzt.</span><span class="sxs-lookup"><span data-stu-id="94232-154">A hard reset returns the device to its initialization or boot-up state.</span></span> <span data-ttu-id="94232-155">Alle internen Geräte Zustandsinformationen und Daten gehen verloren.</span><span class="sxs-lookup"><span data-stu-id="94232-155">All internal device state information and data are lost.</span></span>

</dd> <dt>

<span data-ttu-id="94232-156">**Anzahlermengen**</span><span class="sxs-lookup"><span data-stu-id="94232-156">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94232-157">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="94232-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="94232-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="94232-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94232-159">Anzahl der vom Controller ausgestellten Soft-zurück Stellungen.</span><span class="sxs-lookup"><span data-stu-id="94232-159">Number of soft resets issued by the controller.</span></span> <span data-ttu-id="94232-160">Eine weiche zurück Setzung löscht den aktuellen Gerätestatus und die Daten nicht vollständig.</span><span class="sxs-lookup"><span data-stu-id="94232-160">A soft reset does not completely clear current device state and data.</span></span> <span data-ttu-id="94232-161">Die genaue Semantik ist abhängig vom Gerät und den Protokollen und Mechanismen, die für die Kommunikation mit dem Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="94232-161">Exact semantics are dependent on the device and on the protocols and mechanisms used to communicate to it.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="94232-162">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="94232-162">Remarks</span></span>

<span data-ttu-id="94232-163">Die **CIM \_ controlledby** -Klasse wird von [**CIM \_ deviceconnetction**](cim-deviceconnection.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="94232-163">The **CIM\_ControlledBy** class is derived from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

<span data-ttu-id="94232-164">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="94232-164">WMI does not implement this class.</span></span> <span data-ttu-id="94232-165">Weitere Informationen zu Klassen, die von **CIM \_ controlledby** abgeleitet sind, finden Sie unter [Win32-Klassen](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="94232-165">For more information about classes derived from **CIM\_ControlledBy**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="94232-166">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="94232-166">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="94232-167">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="94232-167">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="94232-168">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="94232-168">Requirements</span></span>



| <span data-ttu-id="94232-169">Anforderung</span><span class="sxs-lookup"><span data-stu-id="94232-169">Requirement</span></span> | <span data-ttu-id="94232-170">Wert</span><span class="sxs-lookup"><span data-stu-id="94232-170">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="94232-171">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="94232-171">Minimum supported client</span></span><br/> | <span data-ttu-id="94232-172">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="94232-172">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="94232-173">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="94232-173">Minimum supported server</span></span><br/> | <span data-ttu-id="94232-174">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="94232-174">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="94232-175">Namespace</span><span class="sxs-lookup"><span data-stu-id="94232-175">Namespace</span></span><br/>                | <span data-ttu-id="94232-176">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="94232-176">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="94232-177">MOF</span><span class="sxs-lookup"><span data-stu-id="94232-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="94232-178"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="94232-178"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="94232-179">DLL</span><span class="sxs-lookup"><span data-stu-id="94232-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94232-180"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94232-180"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94232-181">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="94232-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94232-182">**CIM-Geräte \_ Steuerung**</span><span class="sxs-lookup"><span data-stu-id="94232-182">**CIM\_DeviceConnection**</span></span>](cim-deviceconnection.md)
</dt> </dl>

 

