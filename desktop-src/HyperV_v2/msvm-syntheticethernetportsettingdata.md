---
description: Stellt den konfigurierten Status eines synthetischen Ethernet-Adapters dar.
ms.assetid: BE895BAF-7766-43A2-9659-3ABA97A16134
title: Msvm_SyntheticEthernetPortSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticEthernetPortSettingData
- Msvm_SyntheticEthernetPortSettingData.InstanceID
- Msvm_SyntheticEthernetPortSettingData.Caption
- Msvm_SyntheticEthernetPortSettingData.Description
- Msvm_SyntheticEthernetPortSettingData.ElementName
- Msvm_SyntheticEthernetPortSettingData.ResourceType
- Msvm_SyntheticEthernetPortSettingData.OtherResourceType
- Msvm_SyntheticEthernetPortSettingData.ResourceSubType
- Msvm_SyntheticEthernetPortSettingData.PoolID
- Msvm_SyntheticEthernetPortSettingData.ConsumerVisibility
- Msvm_SyntheticEthernetPortSettingData.HostResource
- Msvm_SyntheticEthernetPortSettingData.AllocationUnits
- Msvm_SyntheticEthernetPortSettingData.VirtualQuantity
- Msvm_SyntheticEthernetPortSettingData.Reservation
- Msvm_SyntheticEthernetPortSettingData.Limit
- Msvm_SyntheticEthernetPortSettingData.Weight
- Msvm_SyntheticEthernetPortSettingData.AutomaticAllocation
- Msvm_SyntheticEthernetPortSettingData.AutomaticDeallocation
- Msvm_SyntheticEthernetPortSettingData.Parent
- Msvm_SyntheticEthernetPortSettingData.Connection
- Msvm_SyntheticEthernetPortSettingData.Address
- Msvm_SyntheticEthernetPortSettingData.MappingBehavior
- Msvm_SyntheticEthernetPortSettingData.AddressOnParent
- Msvm_SyntheticEthernetPortSettingData.VirtualQuantityUnits
- Msvm_SyntheticEthernetPortSettingData.DesiredVLANEndpointMode
- Msvm_SyntheticEthernetPortSettingData.OtherEndpointMode
- Msvm_SyntheticEthernetPortSettingData.VirtualSystemIdentifiers
- Msvm_SyntheticEthernetPortSettingData.DeviceNamingEnabled
- Msvm_SyntheticEthernetPortSettingData.AllowPacketDirect
- Msvm_SyntheticEthernetPortSettingData.StaticMacAddress
- Msvm_SyntheticEthernetPortSettingData.ClusterMonitored
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5b31b02782c0f215f70f3bb5d2767b01294c7261
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344878"
---
# <a name="msvm_syntheticethernetportsettingdata-class"></a><span data-ttu-id="62a9b-103">MSVM \_ syntheticethernetportsettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="62a9b-103">Msvm\_SyntheticEthernetPortSettingData class</span></span>

<span data-ttu-id="62a9b-104">Stellt den konfigurierten Status eines synthetischen Ethernet-Adapters dar.</span><span class="sxs-lookup"><span data-stu-id="62a9b-104">Represents the configured state of a synthetic Ethernet adapter.</span></span>

<span data-ttu-id="62a9b-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="62a9b-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="62a9b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="62a9b-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticEthernetPortSettingData : CIM_EthernetPortAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Virtual Ethernet Port Default Settings";
  string  Description = "Describes the default settings for the virtual Ethernet port resources.";
  string  ElementName;
  uint16  ResourceType = 10;
  string  OtherResourceType;
  string  ResourceSubType = "Microsoft:Hyper-V:Synthetic Ethernet Port";
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
  uint16  DesiredVLANEndpointMode;
  string  OtherEndpointMode;
  string  VirtualSystemIdentifiers[];
  boolean DeviceNamingEnabled = FALSE;
  boolean AllowPacketDirect = FALSE;
  boolean StaticMacAddress = False;
  boolean ClusterMonitored = TRUE;
};
```

## <a name="members"></a><span data-ttu-id="62a9b-107">Member</span><span class="sxs-lookup"><span data-stu-id="62a9b-107">Members</span></span>

<span data-ttu-id="62a9b-108">Die **MSVM \_ syntheticethernetportsettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="62a9b-108">The **Msvm\_SyntheticEthernetPortSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="62a9b-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="62a9b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="62a9b-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="62a9b-110">Properties</span></span>

<span data-ttu-id="62a9b-111">Die **MSVM \_ syntheticethernetportsettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="62a9b-111">The **Msvm\_SyntheticEthernetPortSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="62a9b-112">**Adresse**</span><span class="sxs-lookup"><span data-stu-id="62a9b-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62a9b-113">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="62a9b-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62a9b-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62a9b-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62a9b-115">Die Adresse der Ressource.</span><span class="sxs-lookup"><span data-stu-id="62a9b-115">The address of the resource.</span></span> <span data-ttu-id="62a9b-116">Beispielsweise die Mac-Adresse eines Ethernet-Ports.</span><span class="sxs-lookup"><span data-stu-id="62a9b-116">For example, the MAC address of a Ethernet port.</span></span> <span data-ttu-id="62a9b-117">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="62a9b-117">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="62a9b-118">**Addressonparent**</span><span class="sxs-lookup"><span data-stu-id="62a9b-118">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62a9b-119">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="62a9b-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62a9b-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62a9b-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62a9b-121">Beschreibt die Adresse dieser Ressource im Kontext des übergeordneten Elements.</span><span class="sxs-lookup"><span data-stu-id="62a9b-121">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="62a9b-122">Die über **geordneten** und **addressonparent** -Eigenschaften werden verwendet, um die Controller Beziehung sowie die Reihenfolge von Geräten auf einem Controller zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="62a9b-122">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="62a9b-123">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="62a9b-123">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="62a9b-124">**Zuordnung von Einheiten**</span><span class="sxs-lookup"><span data-stu-id="62a9b-124">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62a9b-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="62a9b-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62a9b-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62a9b-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62a9b-127">Die Zuordnungs Einheiten, die von den **Reservierungs** -und **Limit** -Eigenschaften verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="62a9b-127">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="62a9b-128">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="62a9b-128">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="62a9b-129">**Allowpacketdirect**</span><span class="sxs-lookup"><span data-stu-id="62a9b-129">**AllowPacketDirect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62a9b-130">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="62a9b-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="62a9b-131">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="62a9b-131">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="62a9b-132">Gibt an, ob die packetdirect-Projektion für die VM aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="62a9b-132">Indicates if PacketDirect projection is enabled for the VM.</span></span>

> [!Note]  
> <span data-ttu-id="62a9b-133">In Windows 10, Version 1703 und Windows Server 2016 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="62a9b-133">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="62a9b-134">**Automaticallocation**</span><span class="sxs-lookup"><span data-stu-id="62a9b-134">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62a9b-135">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="62a9b-135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="62a9b-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62a9b-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62a9b-137">Gibt an, ob die Ressource automatisch zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="62a9b-137">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="62a9b-138">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="62a9b-138">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="62a9b-139">**Automaticdeallocation**</span><span class="sxs-lookup"><span data-stu-id="62a9b-139">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62a9b-140">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="62a9b-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="62a9b-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62a9b-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62a9b-142">Gibt an, ob die Zuordnung der Ressource automatisch aufgehoben wird.</span><span class="sxs-lookup"><span data-stu-id="62a9b-142">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="62a9b-143">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="62a9b-143">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="62a9b-144">**Caption**</span><span class="sxs-lookup"><span data-stu-id="62a9b-144">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62a9b-145">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="62a9b-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62a9b-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62a9b-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62a9b-147">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="62a9b-147">A short description of the object.</span></span> <span data-ttu-id="62a9b-148">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="62a9b-148">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="62a9b-149">**Clusterüberwacht**</span><span class="sxs-lookup"><span data-stu-id="62a9b-149">**ClusterMonitored**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62a9b-150">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="62a9b-150">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="62a9b-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62a9b-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62a9b-152">Gibt an, ob dieser Ethernet-Adapter von einem Cluster überwacht wird.</span><span class="sxs-lookup"><span data-stu-id="62a9b-152">Indicates whether this ethernet adapter is monitored by a cluster.</span></span> <span data-ttu-id="62a9b-153">Diese Eigenschaft ist standardmäßig auf true, wenn Sie nicht konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="62a9b-153">This property defaults to true if not configured.</span></span>

<span data-ttu-id="62a9b-154">Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**modifyresourcesettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) -Methode der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="62a9b-154">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="62a9b-155">**Windows 8.1:** Dieser Wert wird bis Windows 8.1 und Windows Server 2012 R2 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="62a9b-155">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="62a9b-156">**Connection**</span><span class="sxs-lookup"><span data-stu-id="62a9b-156">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62a9b-157">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="62a9b-157">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="62a9b-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62a9b-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62a9b-159">Das, mit dem diese Ressource verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="62a9b-159">The thing to which this resource is connected.</span></span> <span data-ttu-id="62a9b-160">Beispielsweise ein benanntes Netzwerk oder ein Switchport.</span><span class="sxs-lookup"><span data-stu-id="62a9b-160">For example, a named network or switch port.</span></span> <span data-ttu-id="62a9b-161">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="62a9b-161">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="62a9b-162">**Consumersichtbarkeit**</span><span class="sxs-lookup"><span data-stu-id="62a9b-162">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62a9b-163">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="62a9b-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="62a9b-164">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62a9b-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62a9b-165">Die Consumer, die für die zugeordnete Ressource sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="62a9b-165">The consumers visibility to the allocated resource.</span></span> <span data-ttu-id="62a9b-166">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt und ist immer auf 3 (virtualisiert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="62a9b-166">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 3 (Virtualized).</span></span>

</dd> <dt>

<span data-ttu-id="62a9b-167">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="62a9b-167">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62a9b-168">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="62a9b-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62a9b-169">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62a9b-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62a9b-170">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="62a9b-170">A description of the object.</span></span> <span data-ttu-id="62a9b-171">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="62a9b-171">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="62a9b-172">**Desiredvlanendpointmode**</span><span class="sxs-lookup"><span data-stu-id="62a9b-172">**DesiredVLANEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62a9b-173">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="62a9b-173">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="62a9b-174">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62a9b-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62a9b-175">Der gewünschte Konfigurations Modus für den VLAN-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="62a9b-175">The desired configuration mode for the VLAN endpoint.</span></span> <span data-ttu-id="62a9b-176">Diese Eigenschaft wird verwendet, um den ursprünglichen **operationalendpointmode** -Eigenschafts Wert in der Instanz der [**MSVM \_ vlanendpoint**](msvm-vlanendpoint.md) -Klasse festzulegen, die dem zielethernet-Port zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="62a9b-176">This property is used to set the initial **OperationalEndpointMode** property value in the instance of the [**Msvm\_VLANEndpoint**](msvm-vlanendpoint.md) class associated with the targeted Ethernet port.</span></span> <span data-ttu-id="62a9b-177">Mögliche Werte finden Sie unter der **operationalendpointmode** -Eigenschaft der **MSVM \_ vlanendpoint** -Klasse.</span><span class="sxs-lookup"><span data-stu-id="62a9b-177">See the **OperationalEndpointMode** property of the **Msvm\_VLANEndpoint** class for possible values.</span></span> <span data-ttu-id="62a9b-178">Diese Eigenschaft wird von **CIM \_ ethernetportaccesscationsettingdata** geerbt.</span><span class="sxs-lookup"><span data-stu-id="62a9b-178">This property is inherited from **CIM\_EthernetPortAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="62a9b-179">**Devicenamingenabled**</span><span class="sxs-lookup"><span data-stu-id="62a9b-179">**DeviceNamingEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62a9b-180">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="62a9b-180">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="62a9b-181">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62a9b-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62a9b-182">Gibt an, ob dieser Ethernet-Adapter die Gerätebenennung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="62a9b-182">Indicates whether this ethernet adapter supports device naming.</span></span>

<span data-ttu-id="62a9b-183">Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**modifyvirtualsystemresources**](https://www.bing.com/search?q=**ModifyVirtualSystemResources**) -Methode der Klasse " [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) " geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="62a9b-183">This is a read-only property, but it can be changed using the [**ModifyVirtualSystemResources**](https://www.bing.com/search?q=**ModifyVirtualSystemResources**) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

> [!Note]  
> <span data-ttu-id="62a9b-184">In Windows 10 und Windows Server 2016 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="62a9b-184">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="62a9b-185">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="62a9b-185">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62a9b-186">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="62a9b-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62a9b-187">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62a9b-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62a9b-188">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="62a9b-188">A short description of the object.</span></span> <span data-ttu-id="62a9b-189">Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="62a9b-189">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="62a9b-190">**"Hustresource"**</span><span class="sxs-lookup"><span data-stu-id="62a9b-190">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62a9b-191">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="62a9b-191">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="62a9b-192">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62a9b-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62a9b-193">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="62a9b-193">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="62a9b-194">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="62a9b-194">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62a9b-195">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="62a9b-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62a9b-196">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62a9b-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62a9b-197">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="62a9b-197">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="62a9b-198">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="62a9b-198">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="62a9b-199">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="62a9b-199">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="62a9b-200">**Begrenzung**</span><span class="sxs-lookup"><span data-stu-id="62a9b-200">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62a9b-201">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="62a9b-201">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="62a9b-202">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62a9b-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62a9b-203">Die obere Grenze oder die maximale Ressourcen Menge, die für diese Zuweisung gewährt wird.</span><span class="sxs-lookup"><span data-stu-id="62a9b-203">The upper bound, or maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="62a9b-204">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="62a9b-204">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="62a9b-205">**Mappingbehavior**</span><span class="sxs-lookup"><span data-stu-id="62a9b-205">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62a9b-206">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="62a9b-206">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="62a9b-207">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62a9b-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62a9b-208">Gibt an, wie diese Ressource den zugrunde liegenden Ressourcen zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="62a9b-208">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="62a9b-209">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="62a9b-209">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="62a9b-210">**Otherendpointmode**</span><span class="sxs-lookup"><span data-stu-id="62a9b-210">**OtherEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62a9b-211">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="62a9b-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62a9b-212">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62a9b-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62a9b-213">Eine Zeichenfolge, die den Typ des VLAN-Endpunkt Modells beschreibt, das von diesem VLAN-Endpunkt unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="62a9b-213">A string that describes the type of VLAN endpoint model that is supported by this VLAN endpoint.</span></span> <span data-ttu-id="62a9b-214">Diese Eigenschaft wird nur verwendet, wenn die **desiredvlanendpointmode** -Eigenschaft auf 1 (sonstige) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="62a9b-214">This property is only used when the **DesiredVLANEndpointMode** property is set to 1 (Other).</span></span> <span data-ttu-id="62a9b-215">Diese Eigenschaft sollte auf **null** festgelegt werden, wenn die **desiredvlanendpointmode** -Eigenschaft einen anderen Wert als 1 hat.</span><span class="sxs-lookup"><span data-stu-id="62a9b-215">This property should be set to **Null** when the **DesiredVLANEndpointMode** property is any value other than 1.</span></span> <span data-ttu-id="62a9b-216">Diese Eigenschaft wird von **CIM \_ ethernetportaccesscationsettingdata** geerbt.</span><span class="sxs-lookup"><span data-stu-id="62a9b-216">This property is inherited from **CIM\_EthernetPortAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="62a9b-217">**Otherresourcetype**</span><span class="sxs-lookup"><span data-stu-id="62a9b-217">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62a9b-218">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="62a9b-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62a9b-219">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62a9b-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62a9b-220">Eine Zeichenfolge, die den Ressourcentyp beschreibt, wenn ein klar definierter Wert nicht verfügbar ist und **ResourceType** auf "Other" (0) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="62a9b-220">A string that describes the resource type when a well-defined value is not available and **ResourceType** is set to "Other" (0).</span></span> <span data-ttu-id="62a9b-221">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="62a9b-221">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="62a9b-222">**Parent**</span><span class="sxs-lookup"><span data-stu-id="62a9b-222">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62a9b-223">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="62a9b-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62a9b-224">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62a9b-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62a9b-225">Das übergeordnete Element der Ressource.</span><span class="sxs-lookup"><span data-stu-id="62a9b-225">The parent of the resource.</span></span> <span data-ttu-id="62a9b-226">Beispielsweise ein Controller für die aktuelle Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="62a9b-226">For example, a controller for the current allocation.</span></span> <span data-ttu-id="62a9b-227">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="62a9b-227">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="62a9b-228">**Poolid**</span><span class="sxs-lookup"><span data-stu-id="62a9b-228">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62a9b-229">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="62a9b-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62a9b-230">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62a9b-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62a9b-231">Der Pool, aus dem die Ressource aktuell zugewiesen ist, oder der Pool, von dem die Ressource zugeordnet wird, wenn die Zuordnung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="62a9b-231">The pool the resource is currently allocated from, or which pool the resource will be allocated from when the allocation occurs.</span></span> <span data-ttu-id="62a9b-232">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="62a9b-232">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="62a9b-233">**Reservierung**</span><span class="sxs-lookup"><span data-stu-id="62a9b-233">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62a9b-234">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="62a9b-234">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="62a9b-235">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62a9b-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62a9b-236">Die Menge der Ressource, die für diese Zuordnung garantiert verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="62a9b-236">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="62a9b-237">Auf Systemen, die eine über-und Ressourcen Belegung unterstützen, wird dieser Wert in der Regel für die Zugangskontrolle verwendet, um zu verhindern, dass eine Zuordnung akzeptiert wird.</span><span class="sxs-lookup"><span data-stu-id="62a9b-237">On systems that support over-commitment of resources, this value is typically used for admission control to prevent an allocation from being accepted.</span></span> <span data-ttu-id="62a9b-238">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="62a9b-238">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="62a9b-239">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="62a9b-239">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62a9b-240">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="62a9b-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62a9b-241">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62a9b-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62a9b-242">Eine Zeichenfolge, die einen Implementierungs spezifischen Untertyp für diese Ressource beschreibt.</span><span class="sxs-lookup"><span data-stu-id="62a9b-242">A string that describes an implementation specific subtype for this resource.</span></span> <span data-ttu-id="62a9b-243">Dies kann z. b. verwendet werden, um unterschiedliche Modelle desselben Ressourcentyps zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="62a9b-243">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="62a9b-244">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="62a9b-244">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="62a9b-245">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="62a9b-245">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62a9b-246">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="62a9b-246">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="62a9b-247">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62a9b-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62a9b-248">Der Typ der Ressource, für die diese Einstellung gilt.</span><span class="sxs-lookup"><span data-stu-id="62a9b-248">The type of resource this setting applies to.</span></span> <span data-ttu-id="62a9b-249">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt und ist immer auf 10 (Ethernet-Adapter) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="62a9b-249">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 10 (Ethernet Adapter).</span></span>

</dd> <dt>

<span data-ttu-id="62a9b-250">**Staticmacaddress**</span><span class="sxs-lookup"><span data-stu-id="62a9b-250">**StaticMacAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62a9b-251">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="62a9b-251">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="62a9b-252">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62a9b-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62a9b-253">Gibt an, ob die Mac-Adresse statisch ist.</span><span class="sxs-lookup"><span data-stu-id="62a9b-253">Specifies if the MAC address is static.</span></span>

</dd> <dt>

<span data-ttu-id="62a9b-254">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="62a9b-254">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62a9b-255">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="62a9b-255">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="62a9b-256">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62a9b-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62a9b-257">Die Menge der Ressourcen, die dem Consumer vorgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="62a9b-257">The quantity of resources presented to the consumer.</span></span> <span data-ttu-id="62a9b-258">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="62a9b-258">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="62a9b-259">**Virtualquantityunits**</span><span class="sxs-lookup"><span data-stu-id="62a9b-259">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62a9b-260">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="62a9b-260">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62a9b-261">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62a9b-261">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62a9b-262">Gibt die Maßeinheit für die **virtualmenge** -Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="62a9b-262">Specifies the unit of measurement for the **VirtualQuantity** property.</span></span> <span data-ttu-id="62a9b-263">Der Wert dieser Eigenschaft muss ein gültiger Wert des Qualifizierers für programmgesteuerte Einheiten sein, wie in Anhang C. 1 von DSP0004 v 2.5 oder höher definiert.</span><span class="sxs-lookup"><span data-stu-id="62a9b-263">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="62a9b-264">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="62a9b-264">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="62a9b-265">**Virtualsystemidentifier**</span><span class="sxs-lookup"><span data-stu-id="62a9b-265">**VirtualSystemIdentifiers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62a9b-266">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="62a9b-266">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="62a9b-267">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62a9b-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62a9b-268">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")</span><span class="sxs-lookup"><span data-stu-id="62a9b-268">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="62a9b-269">Ein Zeichen folgen Array mit Bezeichners dieser Ressource, die dem Betriebssystem des virtuellen Computers vorgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="62a9b-269">A string array of identifiers of this resource presented to the virtual machine's operating system.</span></span> <span data-ttu-id="62a9b-270">Die Indizes und Werte pro Index werden pro Ressource definiert (d. h. für jeden enumerierten **ResourceType** -Eigenschafts Wert).</span><span class="sxs-lookup"><span data-stu-id="62a9b-270">The indexes and values per index are defined on a per resource basis (that is, for each enumerated **ResourceType** property value).</span></span>

</dd> <dt>

<span data-ttu-id="62a9b-271">**Weight**</span><span class="sxs-lookup"><span data-stu-id="62a9b-271">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62a9b-272">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="62a9b-272">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="62a9b-273">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="62a9b-273">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62a9b-274">Eine relative Priorität für diese Zuordnung in Bezug auf andere Zuordnungen desselben Ressourcenpools.</span><span class="sxs-lookup"><span data-stu-id="62a9b-274">A relative priority for this allocation in relation to other allocations from the same resource pool.</span></span> <span data-ttu-id="62a9b-275">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="62a9b-275">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="62a9b-276">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="62a9b-276">Remarks</span></span>

<span data-ttu-id="62a9b-277">Der Zugriff auf die **MSVM \_ syntheticethernetportsettingdata** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="62a9b-277">Access to the **Msvm\_SyntheticEthernetPortSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="62a9b-278">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="62a9b-278">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="62a9b-279">Beispiele</span><span class="sxs-lookup"><span data-stu-id="62a9b-279">Examples</span></span>

<span data-ttu-id="62a9b-280">Weitere Informationen finden Sie unter [Abfragen von Netzwerk Objekten](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="62a9b-280">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="62a9b-281">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="62a9b-281">Requirements</span></span>



| <span data-ttu-id="62a9b-282">Anforderung</span><span class="sxs-lookup"><span data-stu-id="62a9b-282">Requirement</span></span> | <span data-ttu-id="62a9b-283">Wert</span><span class="sxs-lookup"><span data-stu-id="62a9b-283">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62a9b-284">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="62a9b-284">Minimum supported client</span></span><br/> | <span data-ttu-id="62a9b-285">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="62a9b-285">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="62a9b-286">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="62a9b-286">Minimum supported server</span></span><br/> | <span data-ttu-id="62a9b-287">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="62a9b-287">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="62a9b-288">Namespace</span><span class="sxs-lookup"><span data-stu-id="62a9b-288">Namespace</span></span><br/>                | <span data-ttu-id="62a9b-289">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="62a9b-289">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="62a9b-290">MOF</span><span class="sxs-lookup"><span data-stu-id="62a9b-290">MOF</span></span><br/>                      | <dl> <span data-ttu-id="62a9b-291"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="62a9b-291"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="62a9b-292">DLL</span><span class="sxs-lookup"><span data-stu-id="62a9b-292">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62a9b-293"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="62a9b-293"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="62a9b-294">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="62a9b-294">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62a9b-295">**CIM \_ ethernetportzuweisung-Daten**</span><span class="sxs-lookup"><span data-stu-id="62a9b-295">**CIM\_EthernetPortAllocationSettingData**</span></span>](cim-ethernetportallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="62a9b-296">**CIM \_ resourcezubesettingdata**</span><span class="sxs-lookup"><span data-stu-id="62a9b-296">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 

