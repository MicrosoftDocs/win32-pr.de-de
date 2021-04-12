---
description: Stellt Einstellungen dar, die sich speziell auf die Zuordnung des virtuellen Speichers beziehen.
ms.assetid: de6787c0-9998-4f1d-9715-f0dfa0ff70c6
title: Msvm_StorageAllocationSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageAllocationSettingData
- Msvm_StorageAllocationSettingData.InstanceID
- Msvm_StorageAllocationSettingData.Caption
- Msvm_StorageAllocationSettingData.Description
- Msvm_StorageAllocationSettingData.ElementName
- Msvm_StorageAllocationSettingData.ResourceType
- Msvm_StorageAllocationSettingData.OtherResourceType
- Msvm_StorageAllocationSettingData.ResourceSubType
- Msvm_StorageAllocationSettingData.PoolID
- Msvm_StorageAllocationSettingData.ConsumerVisibility
- Msvm_StorageAllocationSettingData.HostResource
- Msvm_StorageAllocationSettingData.AllocationUnits
- Msvm_StorageAllocationSettingData.VirtualQuantity
- Msvm_StorageAllocationSettingData.Limit
- Msvm_StorageAllocationSettingData.Weight
- Msvm_StorageAllocationSettingData.StorageQoSPolicyID
- Msvm_StorageAllocationSettingData.AutomaticAllocation
- Msvm_StorageAllocationSettingData.AutomaticDeallocation
- Msvm_StorageAllocationSettingData.Parent
- Msvm_StorageAllocationSettingData.Connection
- Msvm_StorageAllocationSettingData.Address
- Msvm_StorageAllocationSettingData.MappingBehavior
- Msvm_StorageAllocationSettingData.AddressOnParent
- Msvm_StorageAllocationSettingData.VirtualResourceBlockSize
- Msvm_StorageAllocationSettingData.VirtualQuantityUnits
- Msvm_StorageAllocationSettingData.Access
- Msvm_StorageAllocationSettingData.HostResourceBlockSize
- Msvm_StorageAllocationSettingData.Reservation
- Msvm_StorageAllocationSettingData.HostExtentStartingAddress
- Msvm_StorageAllocationSettingData.HostExtentName
- Msvm_StorageAllocationSettingData.HostExtentNameFormat
- Msvm_StorageAllocationSettingData.OtherHostExtentNameFormat
- Msvm_StorageAllocationSettingData.HostExtentNameNamespace
- Msvm_StorageAllocationSettingData.OtherHostExtentNameNamespace
- Msvm_StorageAllocationSettingData.IOPSLimit
- Msvm_StorageAllocationSettingData.IOPSReservation
- Msvm_StorageAllocationSettingData.IOPSAllocationUnits
- Msvm_StorageAllocationSettingData.PersistentReservationsSupported
- Msvm_StorageAllocationSettingData.CachingMode
- Msvm_StorageAllocationSettingData.SnapshotId
- Msvm_StorageAllocationSettingData.IgnoreFlushes
- Msvm_StorageAllocationSettingData.WriteHardeningMethod
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d889c262eee9d827a02547ddbfdff2cb121cb337
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216761"
---
# <a name="msvm_storageallocationsettingdata-class"></a><span data-ttu-id="c2f3c-103">MSVM \_ storagezugecationsettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="c2f3c-103">Msvm\_StorageAllocationSettingData class</span></span>

<span data-ttu-id="c2f3c-104">Stellt Einstellungen dar, die sich speziell auf die Zuordnung des virtuellen Speichers beziehen.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-104">Represents settings specifically related to the allocation of virtual storage.</span></span>

<span data-ttu-id="c2f3c-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2f3c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2f3c-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_StorageAllocationSettingData : CIM_StorageAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Hard Disk Image Default Settings";
  string  Description = "Describes the default settings for the hard disk image resources";
  string  ElementName;
  uint16  ResourceType;
  string  OtherResourceType;
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility;
  string  HostResource[];
  string  AllocationUnits;
  uint64  VirtualQuantity;
  uint64  Limit = 1;
  uint32  Weight;
  string  StorageQoSPolicyID;
  boolean AutomaticAllocation;
  boolean AutomaticDeallocation;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  string  AddressOnParent;
  uint64  VirtualResourceBlockSize;
  string  VirtualQuantityUnits = "count(fixed size block)";
  uint16  Access;
  uint64  HostResourceBlockSize;
  uint64  Reservation;
  uint64  HostExtentStartingAddress;
  string  HostExtentName;
  uint16  HostExtentNameFormat;
  string  OtherHostExtentNameFormat;
  uint16  HostExtentNameNamespace;
  string  OtherHostExtentNameNamespace;
  uint64  IOPSLimit;
  uint64  IOPSReservation;
  string  IOPSAllocationUnits;
  boolean PersistentReservationsSupported;
  uint16  CachingMode;
  string  SnapshotId = "";
  boolean IgnoreFlushes;
  uint16  WriteHardeningMethod;
};
```

## <a name="members"></a><span data-ttu-id="c2f3c-107">Member</span><span class="sxs-lookup"><span data-stu-id="c2f3c-107">Members</span></span>

<span data-ttu-id="c2f3c-108">Die Klasse " **MSVM \_ storagezugecationsettingdata** " enthält diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c2f3c-108">The **Msvm\_StorageAllocationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="c2f3c-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c2f3c-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c2f3c-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c2f3c-110">Properties</span></span>

<span data-ttu-id="c2f3c-111">Die **MSVM-Klasse \_ storagezuweisung** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-111">The **Msvm\_StorageAllocationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c2f3c-112">**zugreifen**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-112">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2f3c-113">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2f3c-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2f3c-115">Gibt den Speicherzugriff an.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-115">Specifies the storage access.</span></span> <span data-ttu-id="c2f3c-116">Diese Eigenschaft wird von **CIM \_ storagezugecationsettingdata** geerbt.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-116">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

<dl> <dt>

<span data-ttu-id="c2f3c-117"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-117"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-118"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Lesbar** (1)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-118"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Readable** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-119"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Beschreibbar** (2)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-119"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Writeable** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-120"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Lese-/Schreibzugriff unterstützt** (3)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-120"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Read/Write Supported** (3)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c2f3c-121">**Adresse**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-121">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2f3c-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2f3c-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2f3c-124">Die Adresse der Ressource.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-124">The address of the resource.</span></span> <span data-ttu-id="c2f3c-125">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-125">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c2f3c-126">**Addressonparent**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-126">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2f3c-127">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2f3c-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2f3c-129">Beschreibt die Adresse dieser Ressource im Kontext des übergeordneten Elements.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-129">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="c2f3c-130">Die über **geordneten** und **addressonparent** -Eigenschaften werden verwendet, um die Controller Beziehung sowie die Reihenfolge von Geräten auf einem Controller zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-130">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="c2f3c-131">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-131">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c2f3c-132">**Zuordnung von Einheiten**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-132">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2f3c-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2f3c-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2f3c-135">Die Zuordnungs Einheiten, die von den **Reservierungs** -und **Limit** -Eigenschaften verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-135">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="c2f3c-136">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-136">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c2f3c-137">**Automaticallocation**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-137">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2f3c-138">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="c2f3c-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2f3c-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2f3c-140">Gibt an, ob die Ressource automatisch zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-140">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="c2f3c-141">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-141">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c2f3c-142">**Automaticdeallocation**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-142">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2f3c-143">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="c2f3c-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2f3c-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2f3c-145">Gibt an, ob die Zuordnung der Ressource automatisch aufgehoben wird.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-145">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="c2f3c-146">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-146">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c2f3c-147">**CachingMode**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-147">**CachingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2f3c-148">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-148">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-149">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2f3c-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2f3c-150">Gibt an, ob und wie die Zwischenspeicherung im Arbeitsspeicher für diese VHD verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-150">Indicates whether and how in-memory file caching should be used for this VHD.</span></span> <span data-ttu-id="c2f3c-151">Die Standard Richtlinie wird im Feld **defaultvirtualharddiskcachingmode** der [**MSVM \_ virtualsystemmanagementservicesettingdata**](msvm-virtualsystemmanagementservicesettingdata.md) -Klasse festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-151">The default policy is set in the **DefaultVirtualHardDiskCachingMode** field of the [**Msvm\_VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md) class.</span></span>

> [!Note]  
> <span data-ttu-id="c2f3c-152">In Windows 10 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-152">Added in Windows 10.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c2f3c-153">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-153">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="c2f3c-154">**Standard** (2)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-154">**Default** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Caching"></span><span id="no_caching"></span><span id="NO_CACHING"></span>

<span data-ttu-id="c2f3c-155">**Kein Caching** (3)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-155">**No Caching** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cache_Sharable_Parents"></span><span id="cache_sharable_parents"></span><span id="CACHE_SHARABLE_PARENTS"></span>

<span data-ttu-id="c2f3c-156">Zwischen **Speichern** von freigegebenen übergeordneten Elementen (4)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-156">**Cache Sharable Parents** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c2f3c-157">**Caption**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-157">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2f3c-158">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-159">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2f3c-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-160">Qualifizierer: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-160">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="c2f3c-161">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-161">A short description of the object.</span></span> <span data-ttu-id="c2f3c-162">Diese Eigenschaft wird vom [**CIM- \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf die Standardeinstellungen Festplatte Image festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-162">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hard Disk Image Default Settings".</span></span>

</dd> <dt>

<span data-ttu-id="c2f3c-163">**Connection**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-163">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2f3c-164">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="c2f3c-164">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-165">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2f3c-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2f3c-166">Das Gerät, mit dem diese Ressource verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-166">The device to which this resource is connected.</span></span> <span data-ttu-id="c2f3c-167">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-167">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c2f3c-168">**Consumersichtbarkeit**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-168">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2f3c-169">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-169">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-170">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2f3c-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2f3c-171">Die Sichtbarkeit des Consumers für die zugeordnete Ressource.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-171">The consumer's visibility to the allocated resource.</span></span> <span data-ttu-id="c2f3c-172">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-172">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<dl> <dt>

<span data-ttu-id="c2f3c-173"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-173"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-174"><span id="Passed-Through"></span><span id="passed-through"></span><span id="PASSED-THROUGH"></span>Pass **-through** (2)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-174"><span id="Passed-Through"></span><span id="passed-through"></span><span id="PASSED-THROUGH"></span>**Passed-Through** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-175"><span id="Virtualized"></span><span id="virtualized"></span><span id="VIRTUALIZED"></span>**Virtualisiert** (3)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-175"><span id="Virtualized"></span><span id="virtualized"></span><span id="VIRTUALIZED"></span>**Virtualized** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-176"><span id="Not_represented"></span><span id="not_represented"></span><span id="NOT_REPRESENTED"></span>**Nicht dargestellt** (4)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-176"><span id="Not_represented"></span><span id="not_represented"></span><span id="NOT_REPRESENTED"></span>**Not represented** (4)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c2f3c-177">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-177">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2f3c-178">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-179">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2f3c-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2f3c-180">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-180">A description of the object.</span></span> <span data-ttu-id="c2f3c-181">Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "beschreibt die Standardeinstellungen für die Festplatten Abbild Ressourcen".</span><span class="sxs-lookup"><span data-stu-id="c2f3c-181">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Describes the default settings for the hard disk image resources".</span></span>

</dd> <dt>

<span data-ttu-id="c2f3c-182">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-182">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2f3c-183">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-184">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2f3c-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2f3c-185">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-185">A display name for the object.</span></span> <span data-ttu-id="c2f3c-186">Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-186">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c2f3c-187">**Hostextentname**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-187">**HostExtentName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2f3c-188">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-189">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2f3c-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2f3c-190">Ein eindeutiger Bezeichner für den Host Block.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-190">A unique identifier for the host extent.</span></span> <span data-ttu-id="c2f3c-191">Der identifizierte Host Block wird für die Speicherressourcen Zuordnung verwendet.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-191">The identified host extent is used for the storage resource allocation.</span></span> <span data-ttu-id="c2f3c-192">Diese Eigenschaft wird von **CIM \_ storagezugecationsettingdata** geerbt.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-192">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="c2f3c-193">**Hostextentnameformat**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-193">**HostExtentNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2f3c-194">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-194">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-195">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2f3c-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2f3c-196">Gibt das Format an, das für die **hostextentname** -Eigenschaft verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-196">Identifies the format that is used for the **HostExtentName** property.</span></span> <span data-ttu-id="c2f3c-197">Diese Eigenschaft wird von **CIM \_ storagezugecationsettingdata** geerbt.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-197">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

<dl> <dt>

<span data-ttu-id="c2f3c-198"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-198"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-199"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-199"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-200"><span id="SNVM"></span><span id="snvm"></span>**Snvm** (7)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-200"><span id="SNVM"></span><span id="snvm"></span>**SNVM** (7)</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-201"><span id="NAA"></span><span id="naa"></span>**Naa** (9)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-201"><span id="NAA"></span><span id="naa"></span>**NAA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-202"><span id="EUI64"></span><span id="eui64"></span>**EUI64** (10)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-202"><span id="EUI64"></span><span id="eui64"></span>**EUI64** (10)</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-203"><span id="T10VID"></span><span id="t10vid"></span>**T10VID** (11)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-203"><span id="T10VID"></span><span id="t10vid"></span>**T10VID** (11)</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-204"><span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>**Betriebssystem-Geräte Name** (12)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-204"><span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>**OS Device Name** (12)</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-205"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reserviert** (..</span><span class="sxs-lookup"><span data-stu-id="c2f3c-205"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="c2f3c-206">)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-206">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c2f3c-207">**Hostextentnamenamespace**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-207">**HostExtentNameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2f3c-208">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-209">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2f3c-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2f3c-210">Wenn der Host Block ein SCSI-Volume ist, ist die bevorzugte Quelle für SCSI-Volumenamen SCSI VPD Page 83-Antworten.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-210">If the host extent is a SCSI volume, then the preferred source for SCSI volume names is SCSI VPD Page 83 responses.</span></span> <span data-ttu-id="c2f3c-211">Diese Eigenschaft wird von **CIM \_ storagezugecationsettingdata** geerbt.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-211">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

<dl> <dt>

<span data-ttu-id="c2f3c-212"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-212"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-213"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-213"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-214"><span id="VPD83Type3"></span><span id="vpd83type3"></span><span id="VPD83TYPE3"></span>**VPD83Type3** (2)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-214"><span id="VPD83Type3"></span><span id="vpd83type3"></span><span id="VPD83TYPE3"></span>**VPD83Type3** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-215"><span id="VPD83Type2"></span><span id="vpd83type2"></span><span id="VPD83TYPE2"></span>**VPD83Type2** (3)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-215"><span id="VPD83Type2"></span><span id="vpd83type2"></span><span id="VPD83TYPE2"></span>**VPD83Type2** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-216"><span id="VPD83Type1"></span><span id="vpd83type1"></span><span id="VPD83TYPE1"></span>**VPD83Type1** (4)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-216"><span id="VPD83Type1"></span><span id="vpd83type1"></span><span id="VPD83TYPE1"></span>**VPD83Type1** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-217"><span id="VPD80"></span><span id="vpd80"></span>**VPD80** (5)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-217"><span id="VPD80"></span><span id="vpd80"></span>**VPD80** (5)</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-218"><span id="NodeWWN"></span><span id="nodewwn"></span><span id="NODEWWN"></span>**NoDebug** (6)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-218"><span id="NodeWWN"></span><span id="nodewwn"></span><span id="NODEWWN"></span>**NodeWWN** (6)</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-219"><span id="SNVM"></span><span id="snvm"></span>**Snvm** (7)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-219"><span id="SNVM"></span><span id="snvm"></span>**SNVM** (7)</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-220"><span id="OS_Device_Namespace"></span><span id="os_device_namespace"></span><span id="OS_DEVICE_NAMESPACE"></span>**Betriebssystem-Geräte Namespace** (8)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-220"><span id="OS_Device_Namespace"></span><span id="os_device_namespace"></span><span id="OS_DEVICE_NAMESPACE"></span>**OS Device Namespace** (8)</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-221"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reserviert** (..</span><span class="sxs-lookup"><span data-stu-id="c2f3c-221"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="c2f3c-222">)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-222">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c2f3c-223">**Hostextentstartingaddress**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-223">**HostExtentStartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2f3c-224">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-224">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-225">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2f3c-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2f3c-226">Gibt die Anfangsadresse für den von der **hostextentname** -Eigenschaft identifizierten Host Speicherblock an, der für die Zuordnung des virtuellen Speicherbereichs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-226">Identifies the starting address on the host storage extent, identified by the **HostExtentName** property, that is used for the allocation of the virtual storage extent.</span></span> <span data-ttu-id="c2f3c-227">Ein **null** -Wert gibt an, dass es keine direkte Zuordnung des virtuellen Speicherbereichs zum Host Speicherblock gibt, auf den verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-227">A **Null** value indicates that there is no direct mapping of the virtual storage extent to the referenced host storage extent.</span></span> <span data-ttu-id="c2f3c-228">Diese Eigenschaft wird von **CIM \_ storagezugecationsettingdata** geerbt.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-228">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="c2f3c-229">**"Hustresource"**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-229">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2f3c-230">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="c2f3c-230">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-231">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2f3c-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2f3c-232">Jedem Gerät auf dem virtuellen Computer kann nur eine Host Ressource zugewiesen werden, sodass nur das erste Element dieses Arrays festgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-232">Only one host resource can be assigned to each device in the virtual machine, so only the first element of this array can be set.</span></span> <span data-ttu-id="c2f3c-233">Legen Sie für Geräte, die diese Funktion unterstützen, das erste Element des **hostresource** -Arrays so fest, dass es einen Verweis auf die zugrunde liegende Host Ressource enthält, die zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-233">For devices that support this feature, set the first element of the **HostResource** array to contain a reference to the underlying host resource to be assigned.</span></span> <span data-ttu-id="c2f3c-234">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-234">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="c2f3c-235">Dies ist eine schreibgeschützte Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-235">This is a read-only property.</span></span> <span data-ttu-id="c2f3c-236">Wenn die **ResourceType** -Eigenschaft jedoch 31 (logischer Datenträger) und die **resourcesubtype** -Eigenschaft "Microsoft: Hyper-V: virtuelle Festplatte", "Microsoft: Hyper-v: Virtual CD/DVD Disk" oder "Microsoft: Hyper-v: Virtual Diskette". die Eigenschaft " **hoststresource** " kann mithilfe der [**modifyresourcesettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) -Methode der Klasse " [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) " geändert werden.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-236">But if the **ResourceType** property is 31 (Logical Disk) and the **ResourceSubType** property is "Microsoft:Hyper-V:Virtual Hard Disk", "Microsoft:Hyper-V:Virtual CD/DVD Disk", or "Microsoft:Hyper-V:Virtual Floppy Disk", the **HostResource** property can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="c2f3c-237">**"Hastresourceblocksize"**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-237">**HostResourceBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2f3c-238">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-238">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-239">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2f3c-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2f3c-240">Die Größe (in Bytes) der Blöcke, die auf dem Host als Ergebnis dieser Speicherressourcen Zuordnung oder Speicherressourcen Zuordnungs Anforderung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-240">The size, in bytes, of the blocks that are allocated at the host as the result of this storage resource allocation or storage resource allocation request.</span></span> <span data-ttu-id="c2f3c-241">Wenn die Blockgröße variabel ist, wird die maximale Blockgröße in Bytes angegeben.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-241">If the block size is variable, then the maximum block size, in bytes, will be specified.</span></span> <span data-ttu-id="c2f3c-242">Wenn die Blockgröße unbekannt ist oder ein Block Konzept nicht zutrifft, wird der Wert 1 verwendet.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-242">If the block size is unknown or if a block concept does not apply, then the value 1 will be used.</span></span> <span data-ttu-id="c2f3c-243">Diese Eigenschaft wird von **CIM \_ storagezugecationsettingdata** geerbt.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-243">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="c2f3c-244">**Ignoreflushes**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-244">**IgnoreFlushes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2f3c-245">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="c2f3c-245">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-246">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2f3c-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2f3c-247">Wenn diese Einstellung auf "true" festgelegt ist, ignoriert Hyper-V das Leeren des Rück Schreibens für diesen bestimmten virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-247">If set to true, Hyper-V will ignore write back flushing for that particular virtual machine.</span></span> <span data-ttu-id="c2f3c-248">Wenn diese Einstellung auf "false" festgelegt ist, schreibt Hyper-V bei jedem leeren Vorgang weiterhin auf den Datenträger zurück.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-248">If set to false, Hyper-V will continue to write back to the disk on every flush.</span></span> <span data-ttu-id="c2f3c-249">Die Standardeinstellung ist false.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-249">The default setting is false.</span></span>

<span data-ttu-id="c2f3c-250">**Windows 10:** Dieser Wert wird bis Windows 10 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-250">**Windows 10:** This value is not supported until Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="c2f3c-251">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-251">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2f3c-252">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-253">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2f3c-253">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-254">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-254">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="c2f3c-255">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-255">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="c2f3c-256">Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-256">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c2f3c-257">**Iopsallocationunits**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-257">**IOPSAllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2f3c-258">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-259">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2f3c-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2f3c-260">Gibt die Zuordnungs Einheiten an, die von den Eigenschaften **iopslimit** und **iopsreservierung** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-260">Specifies the allocation units used by the **IOPSLimit** and **IOPSReservation** properties.</span></span> <span data-ttu-id="c2f3c-261">Diese Eigenschaft hat immer den Wert:</span><span class="sxs-lookup"><span data-stu-id="c2f3c-261">This property always has the value:</span></span>

<span data-ttu-id="c2f3c-262">"count (Normalized I/O)/Second"</span><span class="sxs-lookup"><span data-stu-id="c2f3c-262">"count(normalized I/O) / second"</span></span>

<span data-ttu-id="c2f3c-263">Der Durchsatz wird in normalisierten e/a-Vorgängen pro Sekunde (IOPS) anstelle von unformatiertem IOPS gemessen.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-263">Throughput is measured in normalized I/O operations per second (IOPS) instead of raw IOPS.</span></span> <span data-ttu-id="c2f3c-264">Bei der Verwendung von normalisierten IOPS werden alle e/a-Anforderungen als 1 normalisierte e/a-Vorgänge angesehen, wenn die Anforderungs Größe kleiner oder gleich einer vordefinierten Basis Größe (8 KB) ist.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-264">When using normalized IOPS, each I/O request is accounted for as 1 normalized I/O if the size of the request is less than or equal to a predefined base size (8 KB).</span></span> <span data-ttu-id="c2f3c-265">Anforderungen, die größer als die Basis Größe sind, werden als N e/a-Vorgänge berücksichtigt, wobei n der aufgerundete Wert der Anforderungs Größe dividiert durch die Basis Größe ist.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-265">Requests that are larger than the base size are accounted for as N I/O operations, where N is the rounded-up value of the request size divided by the base size.</span></span> <span data-ttu-id="c2f3c-266">Wenn die Basis Größe z. b. 8 KB beträgt, wird eine 16-KB-Anforderung als 2 normalisierte e/a-Vorgänge gezählt, eine 32-KB-Anforderung als vier normalisierte e/a-Vorgänge usw.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-266">For example, if the base size is 8 KB, a 16-KB request is counted as 2 normalized I/O operations, a 32-KB request as 4 normalized I/O operations, and so on.</span></span>

<span data-ttu-id="c2f3c-267">**Windows 8.1:** Dieser Wert wird bis Windows 8.1 und Windows Server 2012 R2 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-267">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="c2f3c-268">**Iopslimit**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-268">**IOPSLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2f3c-269">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-269">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-270">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2f3c-270">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-271">Qualifizierer: [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1 Milliarde)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-271">Qualifiers: [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1000000000)</span></span>
</dt> </dl>

<span data-ttu-id="c2f3c-272">Die maximale Anzahl von e/a-Vorgängen pro Sekunde (IOPS), die für diesen virtuellen Speicherbereich gewartet werden.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-272">The maximum number of I/O operations per second (IOPS) that will be serviced for this virtual storage extent.</span></span> <span data-ttu-id="c2f3c-273">Wenn der Wert nicht definiert oder NULL ist, gibt es keine Beschränkung für die Anzahl der IOPS, die das Gerät ausgeben kann.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-273">If the value isn't defined or is zero, there is no limit to the number of IOPS that the device can issue.</span></span>

> [!Note]  
> <span data-ttu-id="c2f3c-274">Sie können den Wert dieser Eigenschaft mit der [**modifyresourcesettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) -Methode der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse ändern.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-274">You can use the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class to modify the value of this property.</span></span> <span data-ttu-id="c2f3c-275">Diese Eigenschaft ist nur für **MSVM- \_ storageallocationsettingdata** -Instanzen von Bedeutung, die Ressourcen Zuordnungen für virtuelle Maschinen anfordern.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-275">This property is meaningful only for **Msvm\_StorageAllocationSettingData** instances that request resource allocations for virtual machines.</span></span> <span data-ttu-id="c2f3c-276">Beim Zuordnen von Ressourcen zu einem untergeordneten Pool wird dies ignoriert.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-276">It's ignored when allocating resources to a child pool.</span></span>

 

<span data-ttu-id="c2f3c-277">**Windows 8.1:** Dieser Wert wird bis Windows 8.1 und Windows Server 2012 R2 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-277">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="c2f3c-278">**Iopsreservierung**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-278">**IOPSReservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2f3c-279">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-279">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-280">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2f3c-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-281">Qualifizierer: [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1 Milliarde)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-281">Qualifiers: [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1000000000)</span></span>
</dt> </dl>

<span data-ttu-id="c2f3c-282">Die Mindestanzahl von e/a-Vorgängen pro Sekunde (IOPS), die für diesen virtuellen Speicherbereich gewartet werden.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-282">The minimum number of I/O operations per second (IOPS) that will be serviced for this virtual storage extent.</span></span>

<span data-ttu-id="c2f3c-283">Wenn sowohl **iopslimit** als auch **iopsreservierung** definiert sind, muss der Wert von **iopslimit** größer oder gleich dem Wert von **iopsreservierung** sein.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-283">If both **IOPSLimit** and **IOPSReservation** are defined, the value of **IOPSLimit** must be greater than or equal to the value of **IOPSReservation**.</span></span>

> [!Note]  
> <span data-ttu-id="c2f3c-284">Sie können den Wert dieser Eigenschaft mit der [**modifyresourcesettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) -Methode der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse ändern.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-284">You can use the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class to modify the value of this property.</span></span> <span data-ttu-id="c2f3c-285">Diese Eigenschaft ist nur für **MSVM- \_ storageallocationsettingdata** -Instanzen von Bedeutung, die Ressourcen Zuordnungen für virtuelle Maschinen anfordern.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-285">This property is meaningful only for **Msvm\_StorageAllocationSettingData** instances that request resource allocations for virtual machines.</span></span> <span data-ttu-id="c2f3c-286">Beim Zuordnen von Ressourcen zu einem untergeordneten Pool wird dies ignoriert.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-286">It's ignored when allocating resources to a child pool.</span></span>

 

<span data-ttu-id="c2f3c-287">**Windows 8.1:** Dieser Wert wird bis Windows 8.1 und Windows Server 2012 R2 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-287">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="c2f3c-288">**Begrenzung**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-288">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2f3c-289">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-289">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-290">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2f3c-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2f3c-291">Die maximale Anzahl von Blöcken, die für diese Speicherressourcen Zuweisung auf dem Host erteilt werden.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-291">The maximum number of blocks that will be granted for this storage resource allocation at the host.</span></span> <span data-ttu-id="c2f3c-292">Die Blockgröße wird durch die Eigenschaft " **hustresourceblocksize** " angegeben.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-292">The block size is specified by the **HostResourceBlockSize** property.</span></span> <span data-ttu-id="c2f3c-293">Normalerweise würde der Wert dieser Eigenschaft eine maximale Größe für den zugewiesenen hostblock widerspiegeln, der der Größe des dem Consumer dargestellten virtuellen Speicherbereichs entspricht.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-293">Usually the value of this property would reflect a maximum size for the allocated host extent that matches the size of the virtual storage extent presented to the consumer.</span></span> <span data-ttu-id="c2f3c-294">Ein Wert, der kleiner als ist, würde auf eine Situation hindeuten, in der ein dünn aufgefüllter virtueller Speicherblock erwartet wird, wobei die Füllrate durch den Wert der Eigenschaft Limit beschränkt wird.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-294">A value less than that would indicate a situation where a sparsely populated virtual storage extent is expected, where the fill rate is limited by the value of the Limit property.</span></span> <span data-ttu-id="c2f3c-295">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-295">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c2f3c-296">**Mappingbehavior**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-296">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2f3c-297">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-297">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-298">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2f3c-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2f3c-299">Gibt an, wie diese Ressource den zugrunde liegenden Ressourcen zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-299">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="c2f3c-300">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-300">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c2f3c-301">**Otherhostextentnameformat**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-301">**OtherHostExtentNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2f3c-302">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-303">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2f3c-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2f3c-304">Eine Zeichenfolge, die das Format der **hostextentname** -Eigenschaft beschreibt, wenn die **hostextentnameformat** -Eigenschaft 1 (Sonstiges) ist.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-304">A string that describes the format of the **HostExtentName** property if the **HostExtentNameFormat** property is 1 (Other).</span></span> <span data-ttu-id="c2f3c-305">Diese Eigenschaft wird von **CIM \_ storagezugecationsettingdata** geerbt.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-305">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="c2f3c-306">**Otherhostextentnamenamespace**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-306">**OtherHostExtentNameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2f3c-307">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-308">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2f3c-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2f3c-309">Eine Zeichenfolge, die den Namespace der **hostextentname** -Eigenschaft beschreibt, wenn die **hostextentnamenamespace** -Eigenschaft 1 (Sonstiges) enthält.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-309">A string that describes the namespace of the **HostExtentName** property if the **HostExtentNameNamespace** property contains 1 (Other).</span></span> <span data-ttu-id="c2f3c-310">Diese Eigenschaft wird von **CIM \_ storagezugecationsettingdata** geerbt.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-310">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="c2f3c-311">**Otherresourcetype**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-311">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2f3c-312">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-313">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2f3c-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2f3c-314">Eine Zeichenfolge, die den Ressourcentyp beschreibt, wenn ein klar definierter Wert nicht verfügbar ist und [**ResourceType**](msvm-processorsettingdata.md) den Wert 1 (sonstige) aufweist.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-314">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorsettingdata.md) has the value 1(Other).</span></span> <span data-ttu-id="c2f3c-315">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-315">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c2f3c-316">**Parent**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-316">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2f3c-317">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-318">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2f3c-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2f3c-319">Das übergeordnete Element der Ressource.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-319">The parent of the resource.</span></span> <span data-ttu-id="c2f3c-320">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-320">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c2f3c-321">**Persistentreservationssupported**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-321">**PersistentReservationsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2f3c-322">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="c2f3c-322">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-323">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2f3c-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2f3c-324">Gibt an, ob die virtuelle Festplatte permanente SCSI-3-Reservierungen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-324">Indicates whether the virtual hard disk supports SCSI-3 persistent reservations.</span></span>

<span data-ttu-id="c2f3c-325">**Windows 8.1:** Dieser Wert wird bis Windows 8.1 und Windows Server 2012 R2 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-325">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="c2f3c-326">**Poolid**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-326">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2f3c-327">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-327">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-328">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2f3c-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2f3c-329">Der Bezeichner des Ressourcenpools, von dem diese Ressource zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-329">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="c2f3c-330">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-330">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c2f3c-331">**Reservierung**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-331">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2f3c-332">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-332">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-333">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2f3c-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-334">Qualifizierer: **außer Kraft** Setzung ("Reservierung"), **modelcorrespondence** ("CIM \_ storagezucationsettingdata. hostresourceblocksize")</span><span class="sxs-lookup"><span data-stu-id="c2f3c-334">Qualifiers: **Override** ("Reservation"), **ModelCorrespondence** ("CIM\_StorageAllocationSettingData.HostResourceBlockSize")</span></span>
</dt> </dl>

<span data-ttu-id="c2f3c-335">Die Anzahl der Blöcke, die für diese Speicherressourcen Zuordnung auf dem Host garantiert verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-335">The number of blocks that are guaranteed to be available for this storage resource allocation at the host.</span></span> <span data-ttu-id="c2f3c-336">Die Blockgröße wird durch die Eigenschaft " **hustresourceblocksize** " angegeben.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-336">The block size is specified by the **HostResourceBlockSize** property.</span></span> <span data-ttu-id="c2f3c-337">Diese Eigenschaft wird von **CIM \_ storagezugecationsettingdata** geerbt.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-337">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="c2f3c-338">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-338">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2f3c-339">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-339">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-340">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2f3c-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2f3c-341">Eine Zeichenfolge, die einen Implementierungs spezifischen Untertyp für diese Ressource beschreibt.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-341">A string that describes an implementation-specific subtype for this resource.</span></span> <span data-ttu-id="c2f3c-342">Dies kann z. b. verwendet werden, um unterschiedliche Modelle desselben Ressourcentyps zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-342">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="c2f3c-343">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-343">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c2f3c-344">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-344">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2f3c-345">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-345">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-346">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2f3c-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2f3c-347">Der Typ der Ressource, die diese Zuordnungs Einstellung darstellt.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-347">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="c2f3c-348">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-348">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<dl> <dt>

<span data-ttu-id="c2f3c-349"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-349"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-350"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-350"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-351"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Prozessor** (3)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-351"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processor** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-352"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>Arbeits **Speicher** (4)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-352"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memory** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-353"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE-Controller** (5)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-353"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE Controller** (5)</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-354"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Paralleler SCSI-HBA** (6)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-354"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Parallel SCSI HBA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-355"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC-HBA** (7)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-355"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7)</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-356"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**iSCSI-HBA** (8)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-356"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**iSCSI HBA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-357"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-357"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-358"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet-Adapter** (10)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-358"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet Adapter** (10)</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-359"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Anderer Netzwerk Adapter** (11)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-359"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Other Network Adapter** (11)</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-360"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>E **/a-Slot** (12)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-360"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**I/O Slot** (12)</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-361"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>E **/a-Gerät** (13)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-361"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**I/O Device** (13)</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-362"><span id="Diskette_Drive"></span><span id="diskette_drive"></span><span id="DISKETTE_DRIVE"></span>**Diskettenlaufwerk** (14)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-362"><span id="Diskette_Drive"></span><span id="diskette_drive"></span><span id="DISKETTE_DRIVE"></span>**Diskette Drive** (14)</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-363"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD-Laufwerk** (15)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-363"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD Drive** (15)</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-364"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD-Laufwerk** (16)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-364"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD drive** (16)</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-365"><span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**Laufwerk (17** )</span><span class="sxs-lookup"><span data-stu-id="c2f3c-365"><span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**Disk Drive** (17)</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-366"><span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**Bandlaufwerk** (18)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-366"><span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**Tape Drive** (18)</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-367"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Speicher** Block (19)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-367"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Storage Extent** (19)</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-368"><span id="Other_Storage_Device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Anderes Speichergerät** (20)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-368"><span id="Other_Storage_Device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Other Storage Device** (20)</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-369"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Seriellen Anschluss** (21)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-369"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Serial port** (21)</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-370"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Paralleler Anschluss** (22)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-370"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Parallel port** (22)</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-371"><span id="USB_controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB-Controller** (23)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-371"><span id="USB_controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB controller** (23)</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-372"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Grafikcontroller** (24)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-372"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Graphics controller** (24)</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-373"><span id="IEEE_1394_controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**IEEE 1394-Controller** (25)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-373"><span id="IEEE_1394_controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**IEEE 1394 controller** (25)</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-374"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Partitionier Bare Einheit** (26)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-374"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Partitionable Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-375"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Partitionier bare Basiseinheit** (27)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-375"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Base Partitionable Unit** (27)</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-376"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Netzteil** (28)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-376"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Power Supply** (28)</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-377"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Kühl Gerät** (29)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-377"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Cooling Device** (29)</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-378"><span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**Ethernet-Switchport** (30)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-378"><span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**Ethernet Switch Port** (30)</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-379"><span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**Logischer** Datenträger (31)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-379"><span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**Logical Disk** (31)</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-380"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**Speicher Volume** (32)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-380"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**Storage Volume** (32)</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-381"><span id="Ethernet_connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Ethernet-Verbindung** (33)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-381"><span id="Ethernet_connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Ethernet connection** (33)</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-382"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (30 32767)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-382"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (30 32767)</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-383"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Anbieter reserviert** (32768 65535)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-383"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768 65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c2f3c-384">**SnapshotId**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-384">**SnapshotId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2f3c-385">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-385">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-386">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2f3c-386">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2f3c-387">Eine GUID, die angibt, welche Momentaufnahme in der VHD-Satz Datei angefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-387">A GUID representing which snapshot within the VHD Set file is to be attached.</span></span>

> [!Note]  
> <span data-ttu-id="c2f3c-388">In Windows 10 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-388">Added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="c2f3c-389">**Storageqospolicyid**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-389">**StorageQoSPolicyID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2f3c-390">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-390">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-391">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2f3c-391">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2f3c-392">Gibt den eindeutigen Bezeichner der Speicher-QoS-Richtlinie an, die auf diesen virtuellen Speicherbereich angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-392">Specifies the unique identifier of the Storage QoS Policy to be applied to this virtual storage extent.</span></span>

> [!Note]  
> <span data-ttu-id="c2f3c-393">In Windows 10 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-393">Added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="c2f3c-394">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-394">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2f3c-395">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-395">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-396">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2f3c-396">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2f3c-397">Die Anzahl der Blöcke, die dem Consumer angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-397">The number of blocks that are presented to the consumer.</span></span> <span data-ttu-id="c2f3c-398">Die Blockgröße wird von der **virtualresourceblocksize** -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-398">The block size is specified by the **VirtualResourceBlockSize** property.</span></span> <span data-ttu-id="c2f3c-399">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-399">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c2f3c-400">**Virtualquantityunits**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-400">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2f3c-401">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-401">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-402">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2f3c-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2f3c-403">Gibt die Einheiten an, die von der **virtualmenge** -Eigenschaft verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-403">Specifies the units used by the **VirtualQuantity** property.</span></span> <span data-ttu-id="c2f3c-404">Diese Eigenschaft wird von **CIM \_ storagezugecationsettingdata** geerbt.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-404">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>



| <span data-ttu-id="c2f3c-405">Wert</span><span class="sxs-lookup"><span data-stu-id="c2f3c-405">Value</span></span>                                                                                                | <span data-ttu-id="c2f3c-406">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c2f3c-406">Meaning</span></span>                                                                                    |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c2f3c-407"><dt>"count (Block fester Größe)"</dt></span><span class="sxs-lookup"><span data-stu-id="c2f3c-407"><dt>"count(fixed size block)"</dt></span></span> </dl> | <span data-ttu-id="c2f3c-408">Die festgelegte Blockgröße ist in der **virtualresourceblocksize** -Eigenschaft enthalten.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-408">The fixed block size is contained in the **VirtualResourceBlockSize** property.</span></span><br/> |
| <dl> <span data-ttu-id="c2f3c-409"><dt>Hobby</dt></span><span class="sxs-lookup"><span data-stu-id="c2f3c-409"><dt>"byte"</dt></span></span> </dl>                    | <span data-ttu-id="c2f3c-410">Die **virtualmenge** -Eigenschaft wird in Bytes gemessen.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-410">The **VirtualQuantity** property is measured in bytes.</span></span><br/>                          |



 

</dd> <dt>

<span data-ttu-id="c2f3c-411">**Virtualresourceblocksize**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-411">**VirtualResourceBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2f3c-412">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-412">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-413">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2f3c-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2f3c-414">Die Größe (in Bytes) der Blöcke, die dem Consumer als Ergebnis dieser Speicherressourcen Zuordnung oder Speicherressourcen Zuordnungs Anforderung angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-414">The size, in bytes, of the blocks that are presented to the consumer as the result of this storage resource allocation or storage resource allocation request.</span></span> <span data-ttu-id="c2f3c-415">Wenn die Blockgröße variabel ist, wird die maximale Blockgröße in Bytes angegeben.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-415">If the block size is variable, then the maximum block size, in bytes, will be specified.</span></span> <span data-ttu-id="c2f3c-416">Wenn die Blockgröße unbekannt ist oder ein Block Konzept nicht zutrifft, wird der Wert 1 verwendet.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-416">If the block size is unknown or if a block concept does not apply, then the value 1 will be used.</span></span> <span data-ttu-id="c2f3c-417">Diese Eigenschaft wird von **CIM \_ storagezugecationsettingdata** geerbt.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-417">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="c2f3c-418">**Weight**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-418">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2f3c-419">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-419">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-420">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2f3c-420">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-421">Qualifizierer: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Weight"), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (10000)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-421">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Weight"), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (10000)</span></span>
</dt> </dl>

<span data-ttu-id="c2f3c-422">Gibt eine relative Priorität für diese Zuordnung in Bezug auf andere Zuordnungen aus demselben Ressourcenpool an.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-422">Specifies a relative priority for this allocation in relation to other allocations from the same resource pool.</span></span> <span data-ttu-id="c2f3c-423">Diese Eigenschaft hat keine Maßeinheit und ist nur im Vergleich zu anderen Zuordnungs-vying für dieselben Host Ressourcen relevant.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-423">This property has no unit of measure and is only relevant when compared to other allocations vying for the same host resources.</span></span> <span data-ttu-id="c2f3c-424">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-424">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="c2f3c-425">Bereich: 1 10000</span><span class="sxs-lookup"><span data-stu-id="c2f3c-425">Range: 1 10000</span></span>

</dd> <dt>

<span data-ttu-id="c2f3c-426">**Write-hardeningmethod**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-426">**WriteHardeningMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2f3c-427">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c2f3c-427">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c2f3c-428">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c2f3c-428">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2f3c-429">Gibt an, welche Schreib Härtungs Methode von der Festplatte unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-429">Indicates what write hardening method is supported by the disk.</span></span>

> [!Note]  
> <span data-ttu-id="c2f3c-430">Diese Eigenschaft wurde in Windows 10, Version 1703, hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c2f3c-430">This property was added in Windows 10, version 1703.</span></span>

 

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="c2f3c-431">**Standard** (0)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-431">**Default** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="WriteCacheEnabled"></span><span id="writecacheenabled"></span><span id="WRITECACHEENABLED"></span>

<span data-ttu-id="c2f3c-432">**Schreibzugriff aktiviert** (1)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-432">**WriteCacheEnabled** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="WriteCacheandFUAEnabled"></span><span id="writecacheandfuaenabled"></span><span id="WRITECACHEANDFUAENABLED"></span>

<span data-ttu-id="c2f3c-433">**Schreibaktivierte Schreib-andfuaaktivierte** (2)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-433">**WriteCacheandFUAEnabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="WriteCacheDisabled"></span><span id="writecachedisabled"></span><span id="WRITECACHEDISABLED"></span>

<span data-ttu-id="c2f3c-434">**Schreibwaredeaktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-434">**WriteCacheDisabled** (3)</span></span>


<span data-ttu-id="c2f3c-435"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="c2f3c-435"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="c2f3c-436">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c2f3c-436">Requirements</span></span>



| <span data-ttu-id="c2f3c-437">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c2f3c-437">Requirement</span></span> | <span data-ttu-id="c2f3c-438">Wert</span><span class="sxs-lookup"><span data-stu-id="c2f3c-438">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2f3c-439">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-439">Minimum supported client</span></span><br/> | <span data-ttu-id="c2f3c-440">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c2f3c-440">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c2f3c-441">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c2f3c-441">Minimum supported server</span></span><br/> | <span data-ttu-id="c2f3c-442">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c2f3c-442">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c2f3c-443">Namespace</span><span class="sxs-lookup"><span data-stu-id="c2f3c-443">Namespace</span></span><br/>                | <span data-ttu-id="c2f3c-444">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="c2f3c-444">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c2f3c-445">MOF</span><span class="sxs-lookup"><span data-stu-id="c2f3c-445">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c2f3c-446"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c2f3c-446"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c2f3c-447">DLL</span><span class="sxs-lookup"><span data-stu-id="c2f3c-447">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2f3c-448"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c2f3c-448"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

