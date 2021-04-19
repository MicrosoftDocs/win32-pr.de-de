---
description: Stellt Einstellungen für einen synthetischen 3D-Anzeige Controller für einen virtuellen Computer dar.
ms.assetid: 7162AEED-90CB-41C3-BD44-8B552C00F597
title: Msvm_Synthetic3DDisplayControllerSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synthetic3DDisplayControllerSettingData
- Msvm_Synthetic3DDisplayControllerSettingData.InstanceID
- Msvm_Synthetic3DDisplayControllerSettingData.Caption
- Msvm_Synthetic3DDisplayControllerSettingData.Description
- Msvm_Synthetic3DDisplayControllerSettingData.ElementName
- Msvm_Synthetic3DDisplayControllerSettingData.ResourceType
- Msvm_Synthetic3DDisplayControllerSettingData.OtherResourceType
- Msvm_Synthetic3DDisplayControllerSettingData.ResourceSubType
- Msvm_Synthetic3DDisplayControllerSettingData.PoolID
- Msvm_Synthetic3DDisplayControllerSettingData.ConsumerVisibility
- Msvm_Synthetic3DDisplayControllerSettingData.HostResource
- Msvm_Synthetic3DDisplayControllerSettingData.AllocationUnits
- Msvm_Synthetic3DDisplayControllerSettingData.VirtualQuantity
- Msvm_Synthetic3DDisplayControllerSettingData.Reservation
- Msvm_Synthetic3DDisplayControllerSettingData.Limit
- Msvm_Synthetic3DDisplayControllerSettingData.Weight
- Msvm_Synthetic3DDisplayControllerSettingData.AutomaticAllocation
- Msvm_Synthetic3DDisplayControllerSettingData.AutomaticDeallocation
- Msvm_Synthetic3DDisplayControllerSettingData.Parent
- Msvm_Synthetic3DDisplayControllerSettingData.Connection
- Msvm_Synthetic3DDisplayControllerSettingData.Address
- Msvm_Synthetic3DDisplayControllerSettingData.MappingBehavior
- Msvm_Synthetic3DDisplayControllerSettingData.AddressOnParent
- Msvm_Synthetic3DDisplayControllerSettingData.VirtualQuantityUnits
- Msvm_Synthetic3DDisplayControllerSettingData.MaximumScreenResolution
- Msvm_Synthetic3DDisplayControllerSettingData.MaximumMonitors
- Msvm_Synthetic3DDisplayControllerSettingData.VRAMSizeBytes
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c93bb67cd4a66c4ecc5f6820ff2de7cf3816b2b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348895"
---
# <a name="msvm_synthetic3ddisplaycontrollersettingdata-class"></a><span data-ttu-id="ec94c-103">MSVM \_ Synthetic3DDisplayControllerSettingData-Klasse</span><span class="sxs-lookup"><span data-stu-id="ec94c-103">Msvm\_Synthetic3DDisplayControllerSettingData class</span></span>

<span data-ttu-id="ec94c-104">Stellt Einstellungen für einen synthetischen 3D-Anzeige Controller für einen virtuellen Computer dar.</span><span class="sxs-lookup"><span data-stu-id="ec94c-104">Represents settings for a synthetic 3-D display controller for a virtual machine.</span></span> <span data-ttu-id="ec94c-105">Diese Klasse wird nur bei virtuellen Computern verwendet, die remotefx verwenden.</span><span class="sxs-lookup"><span data-stu-id="ec94c-105">This class is only used with virtual machines that use RemoteFX.</span></span>

<span data-ttu-id="ec94c-106">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ec94c-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec94c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec94c-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Synthetic3DDisplayControllerSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "3D Display Controller Default Settings";
  string  Description = "Describes the default settings for the 3D video controller resource pool.";
  string  ElementName;
  uint16  ResourceType = 24;
  string  OtherResourceType;
  string  ResourceSubType = "Microsoft:Hyper-V:Synthetic 3D Display Controller";
  string  PoolID;
  uint16  ConsumerVisibility = 3;
  string  HostResource[];
  string  AllocationUnits = "count";
  uint64  VirtualQuantity = 1;
  uint64  Reservation = 1;
  uint64  Limit = 1;
  uint32  Weight = 0;
  boolean AutomaticAllocation = True;
  boolean AutomaticDeallocation = True;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  string  AddressOnParent;
  string  VirtualQuantityUnits = "count";
  uint8   MaximumScreenResolution;
  uint8   MaximumMonitors;
  uint64  VRAMSizeBytes;
};
```

## <a name="members"></a><span data-ttu-id="ec94c-108">Member</span><span class="sxs-lookup"><span data-stu-id="ec94c-108">Members</span></span>

<span data-ttu-id="ec94c-109">Die **MSVM \_ Synthetic3DDisplayControllerSettingData** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ec94c-109">The **Msvm\_Synthetic3DDisplayControllerSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="ec94c-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ec94c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ec94c-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ec94c-111">Properties</span></span>

<span data-ttu-id="ec94c-112">Die **MSVM- \_ Synthetic3DDisplayControllerSettingData** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ec94c-112">The **Msvm\_Synthetic3DDisplayControllerSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ec94c-113">**Adresse**</span><span class="sxs-lookup"><span data-stu-id="ec94c-113">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec94c-114">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ec94c-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec94c-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ec94c-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec94c-116">Die Adresse der Ressource.</span><span class="sxs-lookup"><span data-stu-id="ec94c-116">The address of the resource.</span></span> <span data-ttu-id="ec94c-117">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ec94c-117">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="ec94c-118">Dabei handelt es sich um eine schreibgeschützte Eigenschaft, wenn die **ResourceType** -Eigenschaft jedoch 20 (Grafikcontroller) ist, kann Sie mithilfe der [**modifyresourcesettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) -Methode der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse geändert werden.</span><span class="sxs-lookup"><span data-stu-id="ec94c-118">This is a read-only property, but if the **ResourceType** property is 20 (Graphics controller), it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="ec94c-119">**Addressonparent**</span><span class="sxs-lookup"><span data-stu-id="ec94c-119">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec94c-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ec94c-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec94c-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ec94c-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec94c-122">Beschreibt die Adresse dieser Ressource im Kontext des übergeordneten Elements.</span><span class="sxs-lookup"><span data-stu-id="ec94c-122">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="ec94c-123">Die über **geordneten** und **addressonparent** -Eigenschaften werden verwendet, um die Controller Beziehung sowie die Reihenfolge von Geräten auf einem Controller zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="ec94c-123">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="ec94c-124">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ec94c-124">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ec94c-125">**Zuordnung von Einheiten**</span><span class="sxs-lookup"><span data-stu-id="ec94c-125">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec94c-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ec94c-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec94c-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ec94c-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec94c-128">Die Zuordnungs Einheiten, die von den **Reservierungs** -und **Limit** -Eigenschaften verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ec94c-128">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="ec94c-129">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ec94c-129">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ec94c-130">**Automaticallocation**</span><span class="sxs-lookup"><span data-stu-id="ec94c-130">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec94c-131">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ec94c-131">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ec94c-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ec94c-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec94c-133">Gibt an, ob die Ressource automatisch zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="ec94c-133">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="ec94c-134">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ec94c-134">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ec94c-135">**Automaticdeallocation**</span><span class="sxs-lookup"><span data-stu-id="ec94c-135">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec94c-136">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ec94c-136">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ec94c-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ec94c-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec94c-138">Gibt an, ob die Zuordnung der Ressource automatisch aufgehoben wird.</span><span class="sxs-lookup"><span data-stu-id="ec94c-138">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="ec94c-139">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ec94c-139">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ec94c-140">**Caption**</span><span class="sxs-lookup"><span data-stu-id="ec94c-140">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec94c-141">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ec94c-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec94c-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ec94c-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec94c-143">Qualifizierer: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="ec94c-143">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="ec94c-144">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="ec94c-144">A short description of the object.</span></span> <span data-ttu-id="ec94c-145">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ec94c-145">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ec94c-146">**Connection**</span><span class="sxs-lookup"><span data-stu-id="ec94c-146">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec94c-147">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="ec94c-147">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ec94c-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ec94c-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec94c-149">Das Gerät, mit dem diese Ressource verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="ec94c-149">The device to which this resource is connected.</span></span> <span data-ttu-id="ec94c-150">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ec94c-150">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="ec94c-151">Dies ist eine schreibgeschützte Eigenschaft, aber wenn 1) lautet die **ResourceType** -Eigenschaft 17 (serieller Port). oder 2) die **ResourceType** -Eigenschaft ist 21 (Speicherblock), und die **resourcesubtype** -Eigenschaft ist "Microsoft Virtual Hard Disk". Sie kann dann mithilfe der [**modifyresourcesettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) -Methode der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse geändert werden.</span><span class="sxs-lookup"><span data-stu-id="ec94c-151">This is a read-only property, but if either 1) the **ResourceType** property is 17 (Serial port), or 2) the **ResourceType** property is 21 (Storage Extent) and the **ResourceSubType** property is "Microsoft Virtual Hard Disk", then it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="ec94c-152">**Consumersichtbarkeit**</span><span class="sxs-lookup"><span data-stu-id="ec94c-152">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec94c-153">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ec94c-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ec94c-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ec94c-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec94c-155">Die Sichtbarkeit des Consumers für die zugeordnete Ressource.</span><span class="sxs-lookup"><span data-stu-id="ec94c-155">The consumer's visibility to the allocated resource.</span></span> <span data-ttu-id="ec94c-156">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ec94c-156">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ec94c-157">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ec94c-157">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec94c-158">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ec94c-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec94c-159">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ec94c-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec94c-160">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="ec94c-160">A description of the object.</span></span> <span data-ttu-id="ec94c-161">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ec94c-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ec94c-162">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="ec94c-162">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec94c-163">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ec94c-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec94c-164">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ec94c-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec94c-165">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="ec94c-165">A display name for the object.</span></span> <span data-ttu-id="ec94c-166">Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="ec94c-166">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span> <span data-ttu-id="ec94c-167">Durch Ändern dieser Eigenschaft wird der Elementname der zugeordneten logischen Geräte Ableitung geändert.</span><span class="sxs-lookup"><span data-stu-id="ec94c-167">Changing this property will change the element name of the associated logical device derivative.</span></span>

</dd> <dt>

<span data-ttu-id="ec94c-168">**"Hustresource"**</span><span class="sxs-lookup"><span data-stu-id="ec94c-168">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec94c-169">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="ec94c-169">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ec94c-170">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ec94c-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec94c-171">Jedem Gerät auf dem virtuellen Computer kann nur eine Host Ressource zugewiesen werden, sodass nur das erste Element dieses Arrays festgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="ec94c-171">Only one host resource can be assigned to each device in the virtual machine, so only the first element of this array can be set.</span></span> <span data-ttu-id="ec94c-172">Legen Sie für Geräte, die diese Funktion unterstützen, das erste Element des **hostresource** -Arrays so fest, dass es einen Verweis auf die zugrunde liegende Host Ressource enthält, die zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="ec94c-172">For devices that support this feature, set the first element of the **HostResource** array to contain a reference to the underlying host resource that is to be assigned.</span></span> <span data-ttu-id="ec94c-173">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ec94c-173">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ec94c-174">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ec94c-174">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec94c-175">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ec94c-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec94c-176">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ec94c-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec94c-177">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="ec94c-177">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="ec94c-178">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ec94c-178">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ec94c-179">**Begrenzung**</span><span class="sxs-lookup"><span data-stu-id="ec94c-179">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec94c-180">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ec94c-180">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ec94c-181">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ec94c-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec94c-182">Die maximale Menge der entsprechenden Host Ressourcen, die von der virtuellen Maschine verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="ec94c-182">The maximum amount of corresponding host resources that can be consumed by the virtual machine.</span></span> <span data-ttu-id="ec94c-183">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ec94c-183">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ec94c-184">**Mappingbehavior**</span><span class="sxs-lookup"><span data-stu-id="ec94c-184">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec94c-185">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ec94c-185">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ec94c-186">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ec94c-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec94c-187">Gibt an, wie diese Ressource den zugrunde liegenden Ressourcen zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="ec94c-187">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="ec94c-188">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ec94c-188">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ec94c-189">**Maximummonitors**</span><span class="sxs-lookup"><span data-stu-id="ec94c-189">**MaximumMonitors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec94c-190">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="ec94c-190">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="ec94c-191">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ec94c-191">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ec94c-192">Die maximale Anzahl der Monitore, die für den 3D-Anzeige Controller verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="ec94c-192">The maximum number of monitors available to the 3-D display controller.</span></span> <span data-ttu-id="ec94c-193">Die Mindestanzahl von Monitoren ist 1, und der Höchstwert hängt von der maximalen Bildschirmauflösung ab.</span><span class="sxs-lookup"><span data-stu-id="ec94c-193">The minimum number of monitors is 1 and the maximum is dependent upon the maximum screen resolution.</span></span> <span data-ttu-id="ec94c-194">In der folgenden Tabelle ist die maximale Anzahl von Monitoren definiert, die für unterschiedliche Auflösungen zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="ec94c-194">The following table defines the maximum number of monitors allowed for different resolutions.</span></span>



| <span data-ttu-id="ec94c-195">Lösung</span><span class="sxs-lookup"><span data-stu-id="ec94c-195">Resolution</span></span>            | <span data-ttu-id="ec94c-196">Maximale Anzahl von Monitoren</span><span class="sxs-lookup"><span data-stu-id="ec94c-196">Maximum monitors</span></span> |
|-----------------------|------------------|
| <span data-ttu-id="ec94c-197">1024 768</span><span class="sxs-lookup"><span data-stu-id="ec94c-197">1024  768</span></span><br/>  | <span data-ttu-id="ec94c-198">4</span><span class="sxs-lookup"><span data-stu-id="ec94c-198">4</span></span><br/>     |
| <span data-ttu-id="ec94c-199">1280 1024</span><span class="sxs-lookup"><span data-stu-id="ec94c-199">1280  1024</span></span><br/> | <span data-ttu-id="ec94c-200">4</span><span class="sxs-lookup"><span data-stu-id="ec94c-200">4</span></span><br/>     |
| <span data-ttu-id="ec94c-201">1600 1200</span><span class="sxs-lookup"><span data-stu-id="ec94c-201">1600  1200</span></span><br/> | <span data-ttu-id="ec94c-202">3</span><span class="sxs-lookup"><span data-stu-id="ec94c-202">3</span></span><br/>     |
| <span data-ttu-id="ec94c-203">1920 1200</span><span class="sxs-lookup"><span data-stu-id="ec94c-203">1920  1200</span></span><br/> | <span data-ttu-id="ec94c-204">2</span><span class="sxs-lookup"><span data-stu-id="ec94c-204">2</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="ec94c-205">**Maximumscreenresolution**</span><span class="sxs-lookup"><span data-stu-id="ec94c-205">**MaximumScreenResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec94c-206">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="ec94c-206">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="ec94c-207">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ec94c-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec94c-208">Gibt die maximale Bildschirmauflösung für den 3D-Anzeige Controller an.</span><span class="sxs-lookup"><span data-stu-id="ec94c-208">Specifies the maximum screen resolution for the 3-D display controller.</span></span> <span data-ttu-id="ec94c-209">Dabei muss es sich um einen der folgenden Werte handeln:</span><span class="sxs-lookup"><span data-stu-id="ec94c-209">This must be one of the following values.</span></span>

<dt>

<span id="1024___768"></span>

<span data-ttu-id="ec94c-210"><span id="1024___768"></span>**1024 \* 768** (0)</span><span class="sxs-lookup"><span data-stu-id="ec94c-210"><span id="1024___768"></span>**1024 \* 768** (0)</span></span>


</dt> <dd>

<span data-ttu-id="ec94c-211">Die maximale Auflösung beträgt 1024 768.</span><span class="sxs-lookup"><span data-stu-id="ec94c-211">The maximum resolution is 1024   768.</span></span>

</dd> <dt>

<span id="1280___1024"></span>

<span data-ttu-id="ec94c-212"><span id="1280___1024"></span>**1280 \* 1024** (1)</span><span class="sxs-lookup"><span data-stu-id="ec94c-212"><span id="1280___1024"></span>**1280 \* 1024** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ec94c-213">Die maximale Auflösung beträgt 1280 1024.</span><span class="sxs-lookup"><span data-stu-id="ec94c-213">The maximum resolution is 1280   1024.</span></span>

</dd> <dt>

<span id="1600___1200"></span>

<span data-ttu-id="ec94c-214"><span id="1600___1200"></span>**1600 \* 1200** (2)</span><span class="sxs-lookup"><span data-stu-id="ec94c-214"><span id="1600___1200"></span>**1600 \* 1200** (2)</span></span>


</dt> <dd>

<span data-ttu-id="ec94c-215">Die maximale Auflösung beträgt 1600 1200.</span><span class="sxs-lookup"><span data-stu-id="ec94c-215">The maximum resolution is 1600   1200.</span></span>

</dd> <dt>

<span id="1920___1200"></span>

<span data-ttu-id="ec94c-216"><span id="1920___1200"></span>**1920 \* 1200** (3)</span><span class="sxs-lookup"><span data-stu-id="ec94c-216"><span id="1920___1200"></span>**1920 \* 1200** (3)</span></span>


</dt> <dd>

<span data-ttu-id="ec94c-217">Die maximale Auflösung beträgt 1920 1200.</span><span class="sxs-lookup"><span data-stu-id="ec94c-217">The maximum resolution is 1920   1200.</span></span>

</dd> <dt>

<span id="2560___1600"></span>

<span data-ttu-id="ec94c-218"><span id="2560___1600"></span>**2560 \* 1600** (4)</span><span class="sxs-lookup"><span data-stu-id="ec94c-218"><span id="2560___1600"></span>**2560 \* 1600** (4)</span></span>


</dt> <dd>

<span data-ttu-id="ec94c-219">Die maximale Auflösung beträgt 2650 1600.</span><span class="sxs-lookup"><span data-stu-id="ec94c-219">The maximum resolution is 2650   1600.</span></span>

</dd> <dt>

<span id="3840___2160"></span>

<span data-ttu-id="ec94c-220"><span id="3840___2160"></span>**3840 \* 2160** (5)</span><span class="sxs-lookup"><span data-stu-id="ec94c-220"><span id="3840___2160"></span>**3840 \* 2160** (5)</span></span>


</dt> <dd>

<span data-ttu-id="ec94c-221">Die maximale Auflösung beträgt 3840 2160.</span><span class="sxs-lookup"><span data-stu-id="ec94c-221">The maximum resolution is 3840   2160.</span></span>

> [!Note]  
> <span data-ttu-id="ec94c-222">Hinzugefügt in Windows 10 und Windows Server 2016. MSVM \_ synte</span><span class="sxs-lookup"><span data-stu-id="ec94c-222">Added in Windows 10 and Windows Server 2016.msvm\_synte</span></span>

 

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ec94c-223">**Otherresourcetype**</span><span class="sxs-lookup"><span data-stu-id="ec94c-223">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec94c-224">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ec94c-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec94c-225">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ec94c-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec94c-226">Eine Zeichenfolge, die den Ressourcentyp beschreibt, wenn ein klar definierter Wert nicht verfügbar ist und [**ResourceType**](msvm-processorsettingdata.md) den Wert 1 (sonstige) aufweist.</span><span class="sxs-lookup"><span data-stu-id="ec94c-226">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorsettingdata.md) has the value 1(Other).</span></span> <span data-ttu-id="ec94c-227">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ec94c-227">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ec94c-228">**Parent**</span><span class="sxs-lookup"><span data-stu-id="ec94c-228">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec94c-229">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ec94c-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec94c-230">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ec94c-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec94c-231">Das übergeordnete Element der Ressource.</span><span class="sxs-lookup"><span data-stu-id="ec94c-231">The parent of the resource.</span></span> <span data-ttu-id="ec94c-232">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ec94c-232">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ec94c-233">**Poolid**</span><span class="sxs-lookup"><span data-stu-id="ec94c-233">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec94c-234">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ec94c-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec94c-235">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ec94c-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec94c-236">Der Bezeichner des Ressourcenpools, von dem diese Ressource zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="ec94c-236">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="ec94c-237">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ec94c-237">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ec94c-238">**Reservierung**</span><span class="sxs-lookup"><span data-stu-id="ec94c-238">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec94c-239">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ec94c-239">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ec94c-240">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ec94c-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec94c-241">Die Menge der CPU-Ressourcen, die für die Verwendung durch den virtuellen Computer reserviert sind.</span><span class="sxs-lookup"><span data-stu-id="ec94c-241">The amount of CPU resources that are reserved for use by the virtual machine.</span></span> <span data-ttu-id="ec94c-242">Diese Ressourcen sind garantiert für den Verbrauch durch den virtuellen Computer verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ec94c-242">These resources are guaranteed to be available for consumption by the virtual machine.</span></span> <span data-ttu-id="ec94c-243">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ec94c-243">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ec94c-244">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="ec94c-244">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec94c-245">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ec94c-245">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec94c-246">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ec94c-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec94c-247">Eine Zeichenfolge, die einen Implementierungs spezifischen Untertyp für diese Ressource beschreibt.</span><span class="sxs-lookup"><span data-stu-id="ec94c-247">A string that describes an implementation specific subtype for this resource.</span></span> <span data-ttu-id="ec94c-248">Dies kann z. b. verwendet werden, um unterschiedliche Modelle desselben Ressourcentyps zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="ec94c-248">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="ec94c-249">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ec94c-249">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ec94c-250">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="ec94c-250">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec94c-251">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ec94c-251">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ec94c-252">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ec94c-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec94c-253">Der Typ der Ressource, die diese Zuordnungs Einstellung darstellt.</span><span class="sxs-lookup"><span data-stu-id="ec94c-253">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="ec94c-254">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ec94c-254">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ec94c-255">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="ec94c-255">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec94c-256">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ec94c-256">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ec94c-257">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ec94c-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec94c-258">Die Gesamtanzahl der Kerne auf dem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="ec94c-258">The total number of cores in the virtual machine.</span></span> <span data-ttu-id="ec94c-259">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ec94c-259">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ec94c-260">**Virtualquantityunits**</span><span class="sxs-lookup"><span data-stu-id="ec94c-260">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec94c-261">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ec94c-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec94c-262">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ec94c-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec94c-263">Gibt die Maßeinheit für die **virtualmenge** -Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="ec94c-263">Specifies the unit of measurement for the **VirtualQuantity** property.</span></span> <span data-ttu-id="ec94c-264">Der Wert dieser Eigenschaft muss ein gültiger Wert des Qualifizierers für programmgesteuerte Einheiten sein, wie in Anhang C. 1 von DSP0004 v 2.5 oder höher definiert.</span><span class="sxs-lookup"><span data-stu-id="ec94c-264">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="ec94c-265">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ec94c-265">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ec94c-266">**Vramsizebytes**</span><span class="sxs-lookup"><span data-stu-id="ec94c-266">**VRAMSizeBytes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec94c-267">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ec94c-267">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ec94c-268">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ec94c-268">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ec94c-269">Die Videospeicher Größe für den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="ec94c-269">The video memory size for the Virtual Machine.</span></span>

> [!Note]  
> <span data-ttu-id="ec94c-270">In Windows 10 und Windows Server 2016 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ec94c-270">Added in Windows 10 and Windows Server 2016.</span></span>

 

<dt>



 <span data-ttu-id="ec94c-271">(67108864)</span><span class="sxs-lookup"><span data-stu-id="ec94c-271">(67108864)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ec94c-272">(134217728)</span><span class="sxs-lookup"><span data-stu-id="ec94c-272">(134217728)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ec94c-273">(268435456)</span><span class="sxs-lookup"><span data-stu-id="ec94c-273">(268435456)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ec94c-274">(536870912)</span><span class="sxs-lookup"><span data-stu-id="ec94c-274">(536870912)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ec94c-275">(1073741824)</span><span class="sxs-lookup"><span data-stu-id="ec94c-275">(1073741824)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ec94c-276">**Weight**</span><span class="sxs-lookup"><span data-stu-id="ec94c-276">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec94c-277">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ec94c-277">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ec94c-278">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ec94c-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec94c-279">Eine ganze Zahl, die die Gewichtung für jeden Prozessor der virtuellen Maschine definiert.</span><span class="sxs-lookup"><span data-stu-id="ec94c-279">An integer that defines the weight for each virtual machine processor.</span></span> <span data-ttu-id="ec94c-280">Nachdem alle Reserven erfüllt wurden, wird die verbleibende physische Prozessor Kapazität der Hostingplattform virtuellen Computern basierend auf ihren relativen Gewichtungen zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="ec94c-280">After all reserves have been met, the remaining physical processor capacity of the hosting platform will be allocated to virtual machines based on their relative weights.</span></span> <span data-ttu-id="ec94c-281">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ec94c-281">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="ec94c-282">0</span><span class="sxs-lookup"><span data-stu-id="ec94c-282">0</span></span>

<span data-ttu-id="ec94c-283">Bereich: 0 1000</span><span class="sxs-lookup"><span data-stu-id="ec94c-283">Range: 0 1000</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ec94c-284">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ec94c-284">Requirements</span></span>



| <span data-ttu-id="ec94c-285">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ec94c-285">Requirement</span></span> | <span data-ttu-id="ec94c-286">Wert</span><span class="sxs-lookup"><span data-stu-id="ec94c-286">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec94c-287">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ec94c-287">Minimum supported client</span></span><br/> | <span data-ttu-id="ec94c-288">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ec94c-288">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ec94c-289">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ec94c-289">Minimum supported server</span></span><br/> | <span data-ttu-id="ec94c-290">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ec94c-290">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ec94c-291">Namespace</span><span class="sxs-lookup"><span data-stu-id="ec94c-291">Namespace</span></span><br/>                | <span data-ttu-id="ec94c-292">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="ec94c-292">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ec94c-293">MOF</span><span class="sxs-lookup"><span data-stu-id="ec94c-293">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ec94c-294"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ec94c-294"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ec94c-295">DLL</span><span class="sxs-lookup"><span data-stu-id="ec94c-295">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec94c-296"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ec94c-296"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

