---
description: Ordnet dem Speichercontroller, der das Gerät besitzt, ein Speichergerät zu.
ms.assetid: 3DE05EDC-C54A-4C3C-9057-4418246037D5
title: Msvm_ControlledBy-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ControlledBy
- Msvm_ControlledBy.NegotiatedSpeed
- Msvm_ControlledBy.NegotiatedDataWidth
- Msvm_ControlledBy.Antecedent
- Msvm_ControlledBy.Dependent
- Msvm_ControlledBy.AccessState
- Msvm_ControlledBy.TimeOfDeviceReset
- Msvm_ControlledBy.NumberOfHardResets
- Msvm_ControlledBy.NumberOfSoftResets
- Msvm_ControlledBy.DeviceNumber
- Msvm_ControlledBy.AccessMode
- Msvm_ControlledBy.AccessPriority
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7986ffb842f7a1a104a0a8d846c1b6ee47a21523
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373276"
---
# <a name="msvm_controlledby-class"></a><span data-ttu-id="dd80b-103">MSVM \_ controlledby-Klasse</span><span class="sxs-lookup"><span data-stu-id="dd80b-103">Msvm\_ControlledBy class</span></span>

<span data-ttu-id="dd80b-104">Ordnet dem Speichercontroller, der das Gerät besitzt, ein Speichergerät zu.</span><span class="sxs-lookup"><span data-stu-id="dd80b-104">Associates a storage device with the storage controller that owns the device.</span></span> <span data-ttu-id="dd80b-105">Diese Zuordnung wird sowohl für IDE als auch für Disketten Controller verwendet.</span><span class="sxs-lookup"><span data-stu-id="dd80b-105">This association is used with both IDE and floppy controllers.</span></span>

<span data-ttu-id="dd80b-106">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="dd80b-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd80b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd80b-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ControlledBy : CIM_ControlledBy
{
  uint64                NegotiatedSpeed = 0;
  uint32                NegotiatedDataWidth = 0;
  CIM_Controller    REF Antecedent;
  CIM_LogicalDevice REF Dependent;
  uint16                AccessState = 1;
  datetime              TimeOfDeviceReset;
  uint32                NumberOfHardResets;
  uint32                NumberOfSoftResets;
  string                DeviceNumber;
  uint16                AccessMode = 2;
  uint16                AccessPriority = 0;
};
```

## <a name="members"></a><span data-ttu-id="dd80b-108">Member</span><span class="sxs-lookup"><span data-stu-id="dd80b-108">Members</span></span>

<span data-ttu-id="dd80b-109">Die **MSVM \_ controlledby** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="dd80b-109">The **Msvm\_ControlledBy** class has these types of members:</span></span>

-   [<span data-ttu-id="dd80b-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dd80b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dd80b-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dd80b-111">Properties</span></span>

<span data-ttu-id="dd80b-112">Die **MSVM \_ controlledby** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="dd80b-112">The **Msvm\_ControlledBy** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dd80b-113">**AccessMode**</span><span class="sxs-lookup"><span data-stu-id="dd80b-113">**AccessMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd80b-114">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dd80b-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dd80b-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd80b-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd80b-116">Der Zugriff auf das Gerät über den Vorgänger Controller.</span><span class="sxs-lookup"><span data-stu-id="dd80b-116">The accessibility of the device through the antecedent controller.</span></span> <span data-ttu-id="dd80b-117">Diese Eigenschaft wird von [**CIM \_ controlledby**](/windows/desktop/CIMWin32Prov/cim-controlledby)geerbt und ist immer auf 2 festgelegt (Lese-/Schreibzugriff).</span><span class="sxs-lookup"><span data-stu-id="dd80b-117">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), and it is always set to 2 (read/write).</span></span>

</dd> <dt>

<span data-ttu-id="dd80b-118">**Accesspriority**</span><span class="sxs-lookup"><span data-stu-id="dd80b-118">**AccessPriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd80b-119">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dd80b-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dd80b-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd80b-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd80b-121">Die Priorität, die für den Zugriff auf das Gerät über diesen Controller eingeräumt wird.</span><span class="sxs-lookup"><span data-stu-id="dd80b-121">The priority given to accesses of the device through this controller.</span></span> <span data-ttu-id="dd80b-122">Der Pfad mit der höchsten Priorität hat den niedrigsten Wert.</span><span class="sxs-lookup"><span data-stu-id="dd80b-122">The highest priority path will have the lowest value.</span></span> <span data-ttu-id="dd80b-123">Diese Eigenschaft wird von [**CIM \_ controlledby**](/windows/desktop/CIMWin32Prov/cim-controlledby)geerbt und ist immer auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="dd80b-123">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="dd80b-124">**Accessstate**</span><span class="sxs-lookup"><span data-stu-id="dd80b-124">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd80b-125">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dd80b-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dd80b-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd80b-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd80b-127">Gibt an, ob der Controller aktiv auf das Gerät zugreift oder darauf zugreift.</span><span class="sxs-lookup"><span data-stu-id="dd80b-127">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="dd80b-128">Diese Eigenschaft wird von [**CIM \_ controlledby**](/windows/desktop/CIMWin32Prov/cim-controlledby)geerbt und ist immer auf 1 (aktiv) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="dd80b-128">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), and it is always set to 1 (Active).</span></span>

</dd> <dt>

<span data-ttu-id="dd80b-129">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="dd80b-129">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd80b-130">Datentyp: **[ **CIM- \_ Controller**](/windows/desktop/CIMWin32Prov/cim-controller)**</span><span class="sxs-lookup"><span data-stu-id="dd80b-130">Data type: **[**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller)**</span></span>
</dt> <dt>

<span data-ttu-id="dd80b-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd80b-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd80b-132">Ein Verweis auf den Controller.</span><span class="sxs-lookup"><span data-stu-id="dd80b-132">A reference to the controller.</span></span> <span data-ttu-id="dd80b-133">Diese Eigenschaft wird von [**CIM \_ controlledby**](/windows/desktop/CIMWin32Prov/cim-controlledby)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dd80b-133">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby).</span></span>

</dd> <dt>

<span data-ttu-id="dd80b-134">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="dd80b-134">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd80b-135">Datentyp: **[ **CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span><span class="sxs-lookup"><span data-stu-id="dd80b-135">Data type: **[**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span></span>
</dt> <dt>

<span data-ttu-id="dd80b-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd80b-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd80b-137">Ein Verweis auf das kontrollierte Gerät.</span><span class="sxs-lookup"><span data-stu-id="dd80b-137">A reference to the controlled device.</span></span> <span data-ttu-id="dd80b-138">Diese Eigenschaft wird von [**CIM \_ controlledby**](/windows/desktop/CIMWin32Prov/cim-controlledby)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dd80b-138">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby).</span></span>

</dd> <dt>

<span data-ttu-id="dd80b-139">**Devicengegen ber**</span><span class="sxs-lookup"><span data-stu-id="dd80b-139">**DeviceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd80b-140">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dd80b-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd80b-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd80b-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd80b-142">Die Adresse des zugeordneten Geräts im Zusammenhang mit dem Vorgänger Controller.</span><span class="sxs-lookup"><span data-stu-id="dd80b-142">The address of the associated device in the context of the antecedent controller.</span></span> <span data-ttu-id="dd80b-143">Diese Eigenschaft wird von [**CIM \_ controlledby**](/windows/desktop/CIMWin32Prov/cim-controlledby)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dd80b-143">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby).</span></span>

</dd> <dt>

<span data-ttu-id="dd80b-144">**Aushandateddatawidth**</span><span class="sxs-lookup"><span data-stu-id="dd80b-144">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd80b-145">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dd80b-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd80b-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd80b-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd80b-147">Diese Eigenschaft wird von CIM-Geräte [**\_ Bindung**](/windows/desktop/CIMWin32Prov/cim-deviceconnection)geerbt und immer auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="dd80b-147">This property is inherited from [**CIM\_DeviceConnection**](/windows/desktop/CIMWin32Prov/cim-deviceconnection), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="dd80b-148">**Aushandatedspeed**</span><span class="sxs-lookup"><span data-stu-id="dd80b-148">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd80b-149">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="dd80b-149">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dd80b-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd80b-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd80b-151">Diese Eigenschaft wird von CIM-Geräte [**\_ Bindung**](/windows/desktop/CIMWin32Prov/cim-deviceconnection)geerbt und immer auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="dd80b-151">This property is inherited from [**CIM\_DeviceConnection**](/windows/desktop/CIMWin32Prov/cim-deviceconnection), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="dd80b-152">**Anzahlersätze**</span><span class="sxs-lookup"><span data-stu-id="dd80b-152">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd80b-153">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dd80b-153">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd80b-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd80b-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd80b-155">Diese Eigenschaft wird von [**CIM \_ controlledby**](/windows/desktop/CIMWin32Prov/cim-controlledby)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="dd80b-155">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="dd80b-156">**Anzahlermengen**</span><span class="sxs-lookup"><span data-stu-id="dd80b-156">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd80b-157">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dd80b-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd80b-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd80b-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd80b-159">Diese Eigenschaft wird von [**CIM \_ controlledby**](/windows/desktop/CIMWin32Prov/cim-controlledby)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="dd80b-159">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="dd80b-160">**Timeofdevicereset**</span><span class="sxs-lookup"><span data-stu-id="dd80b-160">**TimeOfDeviceReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd80b-161">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="dd80b-161">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="dd80b-162">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd80b-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd80b-163">Diese Eigenschaft wird von [**CIM \_ controlledby**](/windows/desktop/CIMWin32Prov/cim-controlledby)geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="dd80b-163">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dd80b-164">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dd80b-164">Remarks</span></span>

<span data-ttu-id="dd80b-165">Der Zugriff auf die **MSVM \_ controlledby** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="dd80b-165">Access to the **Msvm\_ControlledBy** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="dd80b-166">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="dd80b-166">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="dd80b-167">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dd80b-167">Requirements</span></span>



| <span data-ttu-id="dd80b-168">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dd80b-168">Requirement</span></span> | <span data-ttu-id="dd80b-169">Wert</span><span class="sxs-lookup"><span data-stu-id="dd80b-169">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd80b-170">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dd80b-170">Minimum supported client</span></span><br/> | <span data-ttu-id="dd80b-171">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dd80b-171">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="dd80b-172">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dd80b-172">Minimum supported server</span></span><br/> | <span data-ttu-id="dd80b-173">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dd80b-173">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dd80b-174">Namespace</span><span class="sxs-lookup"><span data-stu-id="dd80b-174">Namespace</span></span><br/>                | <span data-ttu-id="dd80b-175">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="dd80b-175">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="dd80b-176">MOF</span><span class="sxs-lookup"><span data-stu-id="dd80b-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dd80b-177"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="dd80b-177"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dd80b-178">DLL</span><span class="sxs-lookup"><span data-stu-id="dd80b-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd80b-179"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dd80b-179"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="dd80b-180">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dd80b-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd80b-181">**CIM- \_ controlledby**</span><span class="sxs-lookup"><span data-stu-id="dd80b-181">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> <dt>

[<span data-ttu-id="dd80b-182">**CIM- \_ controlledby**</span><span class="sxs-lookup"><span data-stu-id="dd80b-182">**CIM\_ControlledBy**</span></span>](/windows/desktop/CIMWin32Prov/cim-controlledby)
</dt> <dt>

[<span data-ttu-id="dd80b-183">Speicher Klassen</span><span class="sxs-lookup"><span data-stu-id="dd80b-183">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

