---
description: Stellt den konfigurierten Status eines emulierten Ethernet-Adapters dar.
ms.assetid: 8BFD69D8-65B6-4C6F-9972-BD2F3C4FB5B8
title: Msvm_EmulatedEthernetPortSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EmulatedEthernetPortSettingData
- Msvm_EmulatedEthernetPortSettingData.Caption
- Msvm_EmulatedEthernetPortSettingData.Description
- Msvm_EmulatedEthernetPortSettingData.InstanceID
- Msvm_EmulatedEthernetPortSettingData.ElementName
- Msvm_EmulatedEthernetPortSettingData.ResourceType
- Msvm_EmulatedEthernetPortSettingData.OtherResourceType
- Msvm_EmulatedEthernetPortSettingData.ResourceSubType
- Msvm_EmulatedEthernetPortSettingData.PoolID
- Msvm_EmulatedEthernetPortSettingData.ConsumerVisibility
- Msvm_EmulatedEthernetPortSettingData.HostResource
- Msvm_EmulatedEthernetPortSettingData.AllocationUnits
- Msvm_EmulatedEthernetPortSettingData.VirtualQuantity
- Msvm_EmulatedEthernetPortSettingData.Reservation
- Msvm_EmulatedEthernetPortSettingData.Limit
- Msvm_EmulatedEthernetPortSettingData.Weight
- Msvm_EmulatedEthernetPortSettingData.AutomaticAllocation
- Msvm_EmulatedEthernetPortSettingData.AutomaticDeallocation
- Msvm_EmulatedEthernetPortSettingData.Parent
- Msvm_EmulatedEthernetPortSettingData.Connection
- Msvm_EmulatedEthernetPortSettingData.Address
- Msvm_EmulatedEthernetPortSettingData.MappingBehavior
- Msvm_EmulatedEthernetPortSettingData.AddressOnParent
- Msvm_EmulatedEthernetPortSettingData.VirtualQuantityUnits
- Msvm_EmulatedEthernetPortSettingData.DesiredVLANEndpointMode
- Msvm_EmulatedEthernetPortSettingData.OtherEndpointMode
- Msvm_EmulatedEthernetPortSettingData.StaticMacAddress
- Msvm_EmulatedEthernetPortSettingData.ClusterMonitored
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f80a1f14f7a5bd388aec747f19ef84ecf0a32b1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863879"
---
# <a name="msvm_emulatedethernetportsettingdata-class"></a><span data-ttu-id="4575d-103">MSVM \_ emuatedethernetportsettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="4575d-103">Msvm\_EmulatedEthernetPortSettingData class</span></span>

<span data-ttu-id="4575d-104">Stellt den konfigurierten Status eines emulierten Ethernet-Adapters dar.</span><span class="sxs-lookup"><span data-stu-id="4575d-104">Represents the configured state of an emulated Ethernet adapter.</span></span>

<span data-ttu-id="4575d-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4575d-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4575d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="4575d-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EmulatedEthernetPortSettingData : CIM_EthernetPortAllocationSettingData
{
  string  Caption = "Ethernet Port";
  string  Description = "Settings for the Microsoft Emulated Ethernet Port";
  string  InstanceID = "Microsoft:VMID\VDID\device-specific-data";
  string  ElementName = "Ethernet Port";
  uint16  ResourceType = 10;
  string  OtherResourceType;
  string  ResourceSubType = "Microsoft Emulated Ethernet Port";
  string  PoolID;
  uint16  ConsumerVisibility = 3;
  string  HostResource[];
  string  AllocationUnits = "Ports";
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
  boolean StaticMacAddress = TRUE;
  boolean ClusterMonitored = TRUE;
};
```

## <a name="members"></a><span data-ttu-id="4575d-107">Member</span><span class="sxs-lookup"><span data-stu-id="4575d-107">Members</span></span>

<span data-ttu-id="4575d-108">Die **MSVM- \_ emulatedethernetportsettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="4575d-108">The **Msvm\_EmulatedEthernetPortSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="4575d-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4575d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4575d-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4575d-110">Properties</span></span>

<span data-ttu-id="4575d-111">Die **MSVM- \_ emulatedethernetportsettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4575d-111">The **Msvm\_EmulatedEthernetPortSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4575d-112">**Adresse**</span><span class="sxs-lookup"><span data-stu-id="4575d-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4575d-113">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4575d-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4575d-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4575d-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4575d-115">Die Adresse der Ressource.</span><span class="sxs-lookup"><span data-stu-id="4575d-115">The address of the resource.</span></span> <span data-ttu-id="4575d-116">Beispielsweise die Mac-Adresse eines Ethernet-Ports.</span><span class="sxs-lookup"><span data-stu-id="4575d-116">For example, the MAC address of a Ethernet port.</span></span> <span data-ttu-id="4575d-117">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4575d-117">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="4575d-118">Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**modifyresourcesettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) -Methode der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="4575d-118">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="4575d-119">**Addressonparent**</span><span class="sxs-lookup"><span data-stu-id="4575d-119">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4575d-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4575d-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4575d-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4575d-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4575d-122">Beschreibt die Adresse dieser Ressource im Kontext des übergeordneten Elements.</span><span class="sxs-lookup"><span data-stu-id="4575d-122">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="4575d-123">Die über **geordneten** und **addressonparent** -Eigenschaften werden verwendet, um die Controller Beziehung sowie die Reihenfolge von Geräten auf einem Controller zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="4575d-123">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="4575d-124">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4575d-124">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="4575d-125">**Zuordnung von Einheiten**</span><span class="sxs-lookup"><span data-stu-id="4575d-125">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4575d-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4575d-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4575d-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4575d-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4575d-128">Die Zuordnungs Einheiten, die von den **Reservierungs** -und **Limit** -Eigenschaften verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4575d-128">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="4575d-129">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt und ist immer auf "Ports" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4575d-129">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to "Ports".</span></span>

</dd> <dt>

<span data-ttu-id="4575d-130">**Automaticallocation**</span><span class="sxs-lookup"><span data-stu-id="4575d-130">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4575d-131">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="4575d-131">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4575d-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4575d-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4575d-133">Gibt an, ob die Ressource automatisch zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="4575d-133">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="4575d-134">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt und ist immer auf " **true**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4575d-134">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="4575d-135">**Automaticdeallocation**</span><span class="sxs-lookup"><span data-stu-id="4575d-135">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4575d-136">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="4575d-136">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4575d-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4575d-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4575d-138">Gibt an, ob die Zuordnung der Ressource automatisch aufgehoben wird.</span><span class="sxs-lookup"><span data-stu-id="4575d-138">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="4575d-139">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt und ist immer auf " **true**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4575d-139">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="4575d-140">**Caption**</span><span class="sxs-lookup"><span data-stu-id="4575d-140">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4575d-141">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4575d-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4575d-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4575d-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4575d-143">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="4575d-143">A short description of the object.</span></span> <span data-ttu-id="4575d-144">Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Ethernet-Port" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4575d-144">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="4575d-145">**Clusterüberwacht**</span><span class="sxs-lookup"><span data-stu-id="4575d-145">**ClusterMonitored**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4575d-146">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="4575d-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4575d-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4575d-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4575d-148">Gibt an, ob dieser Ethernet-Adapter von einem Cluster überwacht wird.</span><span class="sxs-lookup"><span data-stu-id="4575d-148">Indicates whether this ethernet adapter is monitored by a cluster.</span></span> <span data-ttu-id="4575d-149">Diese Eigenschaft ist standardmäßig auf true, wenn Sie nicht konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="4575d-149">This property defaults to true if not configured.</span></span>

<span data-ttu-id="4575d-150">Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**modifyresourcesettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) -Methode der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="4575d-150">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="4575d-151">**Windows 8.1:** Dieser Wert wird bis Windows 8.1 und Windows Server 2012 R2 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4575d-151">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="4575d-152">**Connection**</span><span class="sxs-lookup"><span data-stu-id="4575d-152">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4575d-153">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="4575d-153">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4575d-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4575d-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4575d-155">Das, mit dem diese Ressource verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="4575d-155">The thing to which this resource is connected.</span></span> <span data-ttu-id="4575d-156">Beispielsweise ein benanntes Netzwerk oder ein Switchport.</span><span class="sxs-lookup"><span data-stu-id="4575d-156">For example, a named network or switch port.</span></span> <span data-ttu-id="4575d-157">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4575d-157">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="4575d-158">Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**modifyresourcesettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) -Methode der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="4575d-158">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="4575d-159">**Consumersichtbarkeit**</span><span class="sxs-lookup"><span data-stu-id="4575d-159">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4575d-160">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4575d-160">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4575d-161">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4575d-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4575d-162">Beschreibt die Benutzer Sichtbarkeit der zugeordneten Ressource.</span><span class="sxs-lookup"><span data-stu-id="4575d-162">Describes the consumers visibility to the allocated resource.</span></span> <span data-ttu-id="4575d-163">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt und ist immer auf 3 (virtualisiert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4575d-163">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 3 (Virtualized).</span></span>

</dd> <dt>

<span data-ttu-id="4575d-164">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4575d-164">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4575d-165">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4575d-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4575d-166">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4575d-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4575d-167">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="4575d-167">A description of the object.</span></span> <span data-ttu-id="4575d-168">Diese Eigenschaft wird vom [**CIM \_ managedelta-Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Settings for the Microsoft emuated Ethernet Port" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4575d-168">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Settings for the Microsoft Emulated Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="4575d-169">**Desiredvlanendpointmode**</span><span class="sxs-lookup"><span data-stu-id="4575d-169">**DesiredVLANEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4575d-170">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4575d-170">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4575d-171">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4575d-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4575d-172">Der gewünschte Konfigurations Modus für den VLAN-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="4575d-172">The desired configuration mode for the VLAN endpoint.</span></span> <span data-ttu-id="4575d-173">Diese Eigenschaft wird verwendet, um den ursprünglichen **operationalendpointmode** -Eigenschafts Wert in der Instanz der [**MSVM \_ vlanendpoint**](msvm-vlanendpoint.md) -Klasse festzulegen, die dem zielethernet-Port zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="4575d-173">This property is used to set the initial **OperationalEndpointMode** property value in the instance of [**Msvm\_VLANEndpoint**](msvm-vlanendpoint.md) class associated with the targeted Ethernet port.</span></span> <span data-ttu-id="4575d-174">Mögliche Werte finden Sie unter der **operationalendpointmode** -Eigenschaft der **MSVM \_ vlanendpoint** -Klasse.</span><span class="sxs-lookup"><span data-stu-id="4575d-174">See the **OperationalEndpointMode** property of the **Msvm\_VLANEndpoint** class for possible values.</span></span> <span data-ttu-id="4575d-175">Diese Eigenschaft wird von **CIM \_ ethernetportaccesscationsettingdata** geerbt.</span><span class="sxs-lookup"><span data-stu-id="4575d-175">This property is inherited from **CIM\_EthernetPortAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="4575d-176">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="4575d-176">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4575d-177">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4575d-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4575d-178">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4575d-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4575d-179">Der vom benutzerkonfigurierbare Anzeige Name für das Gerät, dem diese rasd-Instanz zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="4575d-179">The user-configurable display name for the device this RASD instance is associated with.</span></span> <span data-ttu-id="4575d-180">Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))geerbt und ist auf "Ethernet-Port" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4575d-180">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is set to "Ethernet Port".</span></span> <span data-ttu-id="4575d-181">Durch Ändern dieser Eigenschaft wird der Elementname der zugeordneten logischen Geräte Ableitung geändert.</span><span class="sxs-lookup"><span data-stu-id="4575d-181">Changing this property will change the element name of the associated logical device derivative.</span></span>

<span data-ttu-id="4575d-182">Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**modifyresourcesettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) -Methode der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="4575d-182">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="4575d-183">**"Hustresource"**</span><span class="sxs-lookup"><span data-stu-id="4575d-183">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4575d-184">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="4575d-184">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4575d-185">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4575d-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4575d-186">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4575d-186">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="4575d-187">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="4575d-187">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4575d-188">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4575d-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4575d-189">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4575d-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4575d-190">Im Gültigkeitsbereich des instanziierten Namespaces identifiziert **InstanceId** verdeckt und identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="4575d-190">Within the scope of the instantiating namespace, **InstanceID** opaquely and uniquely identifies an instance of this class.</span></span> <span data-ttu-id="4575d-191">Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))geerbt und ist immer auf "Microsoft:*VMID* \\ *VDID* \\ *Device-Specific-Data*" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4575d-191">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to "Microsoft:*VMID*\\*VDID*\\*device-specific-data*".</span></span>

</dd> <dt>

<span data-ttu-id="4575d-192">**Begrenzung**</span><span class="sxs-lookup"><span data-stu-id="4575d-192">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4575d-193">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4575d-193">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4575d-194">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4575d-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4575d-195">Die obere Grenze oder die maximale Ressourcen Menge, die für diese Zuweisung gewährt wird.</span><span class="sxs-lookup"><span data-stu-id="4575d-195">The upper bound, or maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="4575d-196">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt und ist immer auf 1 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4575d-196">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="4575d-197">**Mappingbehavior**</span><span class="sxs-lookup"><span data-stu-id="4575d-197">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4575d-198">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4575d-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4575d-199">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4575d-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4575d-200">Gibt an, wie diese Ressource den zugrunde liegenden Ressourcen zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="4575d-200">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="4575d-201">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4575d-201">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="4575d-202">**Otherendpointmode**</span><span class="sxs-lookup"><span data-stu-id="4575d-202">**OtherEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4575d-203">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4575d-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4575d-204">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4575d-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4575d-205">Eine Zeichenfolge, die den Typ des VLAN-Endpunkt Modells beschreibt, das von diesem VLAN-Endpunkt unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="4575d-205">A string that describes the type of VLAN endpoint model that is supported by this VLAN endpoint.</span></span> <span data-ttu-id="4575d-206">Diese Eigenschaft wird nur verwendet, wenn die **desiredvlanendpointmode** -Eigenschaft auf 1 (sonstige) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="4575d-206">This property is only used when the **DesiredVLANEndpointMode** property is set to 1 (Other).</span></span> <span data-ttu-id="4575d-207">Diese Eigenschaft sollte auf **null** festgelegt werden, wenn die **desiredvlanendpointmode** -Eigenschaft einen anderen Wert als 1 hat.</span><span class="sxs-lookup"><span data-stu-id="4575d-207">This property should be set to **Null** when the **DesiredVLANEndpointMode** property is any value other than 1.</span></span> <span data-ttu-id="4575d-208">Diese Eigenschaft wird von **CIM \_ ethernetportaccesscationsettingdata** geerbt.</span><span class="sxs-lookup"><span data-stu-id="4575d-208">This property is inherited from **CIM\_EthernetPortAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="4575d-209">**Otherresourcetype**</span><span class="sxs-lookup"><span data-stu-id="4575d-209">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4575d-210">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4575d-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4575d-211">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4575d-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4575d-212">Eine Zeichenfolge, die den Ressourcentyp beschreibt, wenn ein klar definierter Wert nicht verfügbar ist und ResourceType auf 0 ("Other") festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="4575d-212">A string that describes the resource type when a well-defined value is not available and ResourceType is set to 0 ("Other").</span></span> <span data-ttu-id="4575d-213">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="4575d-213">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4575d-214">**Parent**</span><span class="sxs-lookup"><span data-stu-id="4575d-214">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4575d-215">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4575d-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4575d-216">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4575d-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4575d-217">Das übergeordnete Element der Ressource.</span><span class="sxs-lookup"><span data-stu-id="4575d-217">The parent of the resource.</span></span> <span data-ttu-id="4575d-218">Beispielsweise ein Controller für die aktuelle Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="4575d-218">For example, a controller for the current allocation.</span></span> <span data-ttu-id="4575d-219">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4575d-219">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="4575d-220">**Poolid**</span><span class="sxs-lookup"><span data-stu-id="4575d-220">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4575d-221">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4575d-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4575d-222">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4575d-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4575d-223">Der Pool, aus dem die Ressource aktuell zugewiesen ist, oder der Pool, von dem die Ressource zugeordnet wird, wenn die Zuordnung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="4575d-223">The pool the resource is currently allocated from, or the pool the resource will be allocated from when the allocation occurs.</span></span> <span data-ttu-id="4575d-224">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4575d-224">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="4575d-225">**Reservierung**</span><span class="sxs-lookup"><span data-stu-id="4575d-225">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4575d-226">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4575d-226">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4575d-227">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4575d-227">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4575d-228">Die Menge der Ressource, die für diese Zuordnung garantiert verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="4575d-228">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="4575d-229">Auf Systemen, die eine über-und Ressourcen Belegung unterstützen, wird dieser Wert in der Regel für die Zugangskontrolle verwendet, um zu verhindern, dass eine Zuordnung akzeptiert wird.</span><span class="sxs-lookup"><span data-stu-id="4575d-229">On systems that support over-commitment of resources, this value is typically used for admission control to prevent an allocation from being accepted.</span></span> <span data-ttu-id="4575d-230">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt und ist immer auf 1 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4575d-230">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="4575d-231">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="4575d-231">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4575d-232">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4575d-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4575d-233">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4575d-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4575d-234">Eine Zeichenfolge, die einen Implementierungs spezifischen Untertyp für diese Ressource beschreibt.</span><span class="sxs-lookup"><span data-stu-id="4575d-234">A string that describes an implementation specific subtype for this resource.</span></span> <span data-ttu-id="4575d-235">Dies kann z. b. verwendet werden, um unterschiedliche Modelle desselben Ressourcentyps zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="4575d-235">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="4575d-236">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt und ist immer auf "Microsoft emulierten Ethernet-Port" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4575d-236">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to "Microsoft Emulated Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="4575d-237">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="4575d-237">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4575d-238">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4575d-238">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4575d-239">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4575d-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4575d-240">Der Typ der Ressource, für die diese Einstellung gilt.</span><span class="sxs-lookup"><span data-stu-id="4575d-240">The type of resource this setting applies to.</span></span> <span data-ttu-id="4575d-241">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt und ist immer auf 10 (Ethernet-Adapter) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4575d-241">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 10 (Ethernet Adapter).</span></span>

</dd> <dt>

<span data-ttu-id="4575d-242">**Staticmacaddress**</span><span class="sxs-lookup"><span data-stu-id="4575d-242">**StaticMacAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4575d-243">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="4575d-243">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4575d-244">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4575d-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4575d-245">Gibt an, ob eine statische MAC-Adresse verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4575d-245">Indicates whether to use a static MAC address.</span></span>

<span data-ttu-id="4575d-246">Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**modifyresourcesettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) -Methode der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="4575d-246">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="4575d-247">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="4575d-247">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4575d-248">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4575d-248">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4575d-249">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4575d-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4575d-250">Die Menge der Ressourcen, die dem Consumer vorgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="4575d-250">The quantity of resources presented to the consumer.</span></span> <span data-ttu-id="4575d-251">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt und ist immer auf 1 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4575d-251">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="4575d-252">**Virtualquantityunits**</span><span class="sxs-lookup"><span data-stu-id="4575d-252">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4575d-253">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4575d-253">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4575d-254">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4575d-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4575d-255">Gibt die Maßeinheit für diese Ressourcenzuweisung an.</span><span class="sxs-lookup"><span data-stu-id="4575d-255">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="4575d-256">Der Wert dieser Eigenschaft muss ein gültiger Wert des Qualifizierers für programmgesteuerte Einheiten sein, wie in Anhang C. 1 von DSP0004 v 2.5 oder höher definiert.</span><span class="sxs-lookup"><span data-stu-id="4575d-256">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="4575d-257">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4575d-257">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="4575d-258">**Weight**</span><span class="sxs-lookup"><span data-stu-id="4575d-258">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4575d-259">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4575d-259">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4575d-260">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4575d-260">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4575d-261">Eine relative Priorität für diese Zuordnung in Bezug auf andere Zuordnungen desselben resourcepools.</span><span class="sxs-lookup"><span data-stu-id="4575d-261">A relative priority for this allocation in relation to other allocations from the same ResourcePool.</span></span> <span data-ttu-id="4575d-262">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt und ist immer auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4575d-262">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 0.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4575d-263">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4575d-263">Remarks</span></span>

<span data-ttu-id="4575d-264">Der Zugriff auf die **MSVM- \_ emulatedethernetportsettingdata** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="4575d-264">Access to the **Msvm\_EmulatedEthernetPortSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="4575d-265">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="4575d-265">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="4575d-266">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4575d-266">Examples</span></span>

<span data-ttu-id="4575d-267">Weitere Informationen finden Sie unter [Abfragen von Netzwerk Objekten](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="4575d-267">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4575d-268">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4575d-268">Requirements</span></span>



| <span data-ttu-id="4575d-269">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4575d-269">Requirement</span></span> | <span data-ttu-id="4575d-270">Wert</span><span class="sxs-lookup"><span data-stu-id="4575d-270">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4575d-271">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4575d-271">Minimum supported client</span></span><br/> | <span data-ttu-id="4575d-272">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4575d-272">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4575d-273">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4575d-273">Minimum supported server</span></span><br/> | <span data-ttu-id="4575d-274">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4575d-274">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4575d-275">Namespace</span><span class="sxs-lookup"><span data-stu-id="4575d-275">Namespace</span></span><br/>                | <span data-ttu-id="4575d-276">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="4575d-276">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4575d-277">MOF</span><span class="sxs-lookup"><span data-stu-id="4575d-277">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4575d-278"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="4575d-278"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4575d-279">DLL</span><span class="sxs-lookup"><span data-stu-id="4575d-279">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4575d-280"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4575d-280"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4575d-281">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4575d-281">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4575d-282">**CIM \_ ethernetportzuweisung-Daten**</span><span class="sxs-lookup"><span data-stu-id="4575d-282">**CIM\_EthernetPortAllocationSettingData**</span></span>](cim-ethernetportallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="4575d-283">**CIM \_ resourcezubesettingdata**</span><span class="sxs-lookup"><span data-stu-id="4575d-283">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 

