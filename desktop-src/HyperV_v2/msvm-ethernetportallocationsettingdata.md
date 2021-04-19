---
description: Stellt eine Zuordnungs Anforderung für einen statischen oder dynamischen Switchport dar oder stellt die aktive Konfiguration eines derzeit zugeordneten statischen oder dynamischen Switchports dar.
ms.assetid: ef70b72f-75a0-448e-a648-6a28c12f0da1
title: Msvm_EthernetPortAllocationSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetPortAllocationSettingData
- Msvm_EthernetPortAllocationSettingData.InstanceID
- Msvm_EthernetPortAllocationSettingData.Caption
- Msvm_EthernetPortAllocationSettingData.Description
- Msvm_EthernetPortAllocationSettingData.ElementName
- Msvm_EthernetPortAllocationSettingData.ResourceType
- Msvm_EthernetPortAllocationSettingData.OtherResourceType
- Msvm_EthernetPortAllocationSettingData.ResourceSubType
- Msvm_EthernetPortAllocationSettingData.PoolID
- Msvm_EthernetPortAllocationSettingData.ConsumerVisibility
- Msvm_EthernetPortAllocationSettingData.HostResource
- Msvm_EthernetPortAllocationSettingData.AllocationUnits
- Msvm_EthernetPortAllocationSettingData.VirtualQuantity
- Msvm_EthernetPortAllocationSettingData.Reservation
- Msvm_EthernetPortAllocationSettingData.Limit
- Msvm_EthernetPortAllocationSettingData.Weight
- Msvm_EthernetPortAllocationSettingData.AutomaticAllocation
- Msvm_EthernetPortAllocationSettingData.AutomaticDeallocation
- Msvm_EthernetPortAllocationSettingData.Parent
- Msvm_EthernetPortAllocationSettingData.Connection
- Msvm_EthernetPortAllocationSettingData.Address
- Msvm_EthernetPortAllocationSettingData.MappingBehavior
- Msvm_EthernetPortAllocationSettingData.AddressOnParent
- Msvm_EthernetPortAllocationSettingData.VirtualQuantityUnits
- Msvm_EthernetPortAllocationSettingData.DesiredVLANEndpointMode
- Msvm_EthernetPortAllocationSettingData.OtherEndpointMode
- Msvm_EthernetPortAllocationSettingData.EnabledState
- Msvm_EthernetPortAllocationSettingData.LastKnownSwitchName
- Msvm_EthernetPortAllocationSettingData.RequiredFeatures
- Msvm_EthernetPortAllocationSettingData.RequiredFeatureHints
- Msvm_EthernetPortAllocationSettingData.TestReplicaPoolID
- Msvm_EthernetPortAllocationSettingData.TestReplicaSwitchName
- Msvm_EthernetPortAllocationSettingData.CompartmentGuid
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a310daf30127aec5069efcf7ca4fd5ead9277e6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349260"
---
# <a name="msvm_ethernetportallocationsettingdata-class"></a><span data-ttu-id="ce757-103">MSVM- \_ Klasse "ethernetportzugegenssettingdata"</span><span class="sxs-lookup"><span data-stu-id="ce757-103">Msvm\_EthernetPortAllocationSettingData class</span></span>

<span data-ttu-id="ce757-104">Stellt eine Zuordnungs Anforderung für einen statischen oder dynamischen Switchport dar oder stellt die aktive Konfiguration eines derzeit zugeordneten statischen oder dynamischen Switchports dar.</span><span class="sxs-lookup"><span data-stu-id="ce757-104">Represents an allocation request for a static or dynamic switch port, or represents the active configuration of a currently allocated static or dynamic switch port.</span></span> <span data-ttu-id="ce757-105">Eine Zuordnungs Anforderung für einen dynamischen Switchport wird auch als Verbindungsanforderung bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="ce757-105">An allocation request for a dynamic switch port is also known as a connection request.</span></span>

<span data-ttu-id="ce757-106">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ce757-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce757-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce757-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetPortAllocationSettingData : CIM_EthernetPortAllocationSettingData
{
  string  InstanceID = "Microsoft:GUID\DeviceSpecificData";
  string  Caption = "Ethernet Switch Port Settings";
  string  Description = "Ethernet Switch Port Settings";
  string  ElementName;
  uint16  ResourceType = 33;
  string  OtherResourceType;
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility = 3;
  string  HostResource[];
  string  AllocationUnits;
  uint64  VirtualQuantity;
  uint64  Reservation;
  uint64  Limit;
  uint32  Weight = 0;
  boolean AutomaticAllocation;
  boolean AutomaticDeallocation;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  string  AddressOnParent;
  string  VirtualQuantityUnits = "count";
  uint16  DesiredVLANEndpointMode;
  string  OtherEndpointMode;
  uint16  EnabledState;
  string  LastKnownSwitchName;
  string  RequiredFeatures[];
  string  RequiredFeatureHints[];
  string  TestReplicaPoolID;
  string  TestReplicaSwitchName;
  string  CompartmentGuid;
};
```

## <a name="members"></a><span data-ttu-id="ce757-108">Member</span><span class="sxs-lookup"><span data-stu-id="ce757-108">Members</span></span>

<span data-ttu-id="ce757-109">Die **MSVM-Klasse " \_ ethernetportzuweisung** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ce757-109">The **Msvm\_EthernetPortAllocationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="ce757-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ce757-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ce757-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ce757-111">Properties</span></span>

<span data-ttu-id="ce757-112">Die **MSVM-Klasse " \_ ethernetportzuweisung** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ce757-112">The **Msvm\_EthernetPortAllocationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ce757-113">**Adresse**</span><span class="sxs-lookup"><span data-stu-id="ce757-113">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce757-114">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ce757-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce757-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ce757-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ce757-116">Die Adresse der Ressource.</span><span class="sxs-lookup"><span data-stu-id="ce757-116">The address of the resource.</span></span> <span data-ttu-id="ce757-117">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ce757-117">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ce757-118">**Addressonparent**</span><span class="sxs-lookup"><span data-stu-id="ce757-118">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce757-119">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ce757-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce757-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ce757-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ce757-121">Beschreibt die Adresse dieser Ressource im Kontext des übergeordneten Elements.</span><span class="sxs-lookup"><span data-stu-id="ce757-121">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="ce757-122">Die über **geordneten** und **addressonparent** -Eigenschaften werden verwendet, um die Controller Beziehung sowie die Reihenfolge von Geräten auf einem Controller zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="ce757-122">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="ce757-123">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ce757-123">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ce757-124">**Zuordnung von Einheiten**</span><span class="sxs-lookup"><span data-stu-id="ce757-124">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce757-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ce757-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce757-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ce757-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ce757-127">Die Zuordnungs Einheit, die von den **Reservierungs** -und **Limit** -Eigenschaften verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ce757-127">The unit of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="ce757-128">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ce757-128">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ce757-129">**Automaticallocation**</span><span class="sxs-lookup"><span data-stu-id="ce757-129">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce757-130">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ce757-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ce757-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ce757-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ce757-132">Gibt an, ob die Ressource automatisch zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="ce757-132">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="ce757-133">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ce757-133">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ce757-134">**Automaticdeallocation**</span><span class="sxs-lookup"><span data-stu-id="ce757-134">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce757-135">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ce757-135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ce757-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ce757-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ce757-137">Gibt an, ob die Zuordnung der Ressource automatisch aufgehoben wird.</span><span class="sxs-lookup"><span data-stu-id="ce757-137">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="ce757-138">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ce757-138">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ce757-139">**Caption**</span><span class="sxs-lookup"><span data-stu-id="ce757-139">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce757-140">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ce757-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce757-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ce757-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce757-142">Qualifizierer: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="ce757-142">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="ce757-143">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="ce757-143">A short description of the object.</span></span> <span data-ttu-id="ce757-144">Diese Eigenschaft wird vom [**CIM \_ managedelta-Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Ethernet-switchporteinstellungen" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ce757-144">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Settings".</span></span>

</dd> <dt>

<span data-ttu-id="ce757-145">**Abteilungs-GUID**</span><span class="sxs-lookup"><span data-stu-id="ce757-145">**CompartmentGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce757-146">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ce757-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce757-147">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ce757-147">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ce757-148">Diese Eigenschaft gibt das Zielnetzwerk Depot für den Port an.</span><span class="sxs-lookup"><span data-stu-id="ce757-148">This property specifies the target network compartment for the port.</span></span> <span data-ttu-id="ce757-149">Sie wird nur bei internen Adaptern unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ce757-149">It is only supported for internal adapters.</span></span>

> [!Note]  
> <span data-ttu-id="ce757-150">Die Eigenschaft wurde in Windows 10 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ce757-150">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="ce757-151">**Connection**</span><span class="sxs-lookup"><span data-stu-id="ce757-151">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce757-152">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="ce757-152">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ce757-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ce757-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ce757-154">Das Gerät, mit dem diese Ressource verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="ce757-154">The device to which this resource is connected.</span></span> <span data-ttu-id="ce757-155">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ce757-155">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ce757-156">**Consumersichtbarkeit**</span><span class="sxs-lookup"><span data-stu-id="ce757-156">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce757-157">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ce757-157">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ce757-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ce757-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ce757-159">Die Sichtbarkeit des Consumers für die zugeordnete Ressource.</span><span class="sxs-lookup"><span data-stu-id="ce757-159">The consumer's visibility to the allocated resource.</span></span> <span data-ttu-id="ce757-160">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt und ist immer auf 3 (virtualisiert) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ce757-160">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 3 (Virtualized).</span></span>

</dd> <dt>

<span data-ttu-id="ce757-161">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ce757-161">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce757-162">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ce757-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce757-163">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ce757-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ce757-164">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="ce757-164">A description of the object.</span></span> <span data-ttu-id="ce757-165">Diese Eigenschaft wird vom [**CIM \_ managedelta-Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Ethernet-switchporteinstellungen" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ce757-165">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Settings".</span></span>

</dd> <dt>

<span data-ttu-id="ce757-166">**Desiredvlanendpointmode**</span><span class="sxs-lookup"><span data-stu-id="ce757-166">**DesiredVLANEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce757-167">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ce757-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ce757-168">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ce757-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ce757-169">Der gewünschte Konfigurations Modus für den VLAN-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="ce757-169">The desired configuration mode for the VLAN endpoint.</span></span> <span data-ttu-id="ce757-170">Diese Eigenschaft wird verwendet, um den ursprünglichen **operationalendpointmode** -Eigenschafts Wert in der Instanz der [**MSVM \_ vlanendpoint**](msvm-vlanendpoint.md) -Klasse festzulegen, die dem zielethernet-Port zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ce757-170">This property is used to set the initial **OperationalEndpointMode** property value in the instance of [**Msvm\_VLANEndpoint**](msvm-vlanendpoint.md) class associated with the targeted Ethernet port.</span></span> <span data-ttu-id="ce757-171">Mögliche Werte finden Sie unter der **operationalendpointmode** -Eigenschaft der **MSVM \_ vlanendpoint** -Klasse.</span><span class="sxs-lookup"><span data-stu-id="ce757-171">See the **OperationalEndpointMode** property of the **Msvm\_VLANEndpoint** class for possible values.</span></span> <span data-ttu-id="ce757-172">Diese Eigenschaft wird von **CIM \_ ethernetportaccesscationsettingdata** geerbt.</span><span class="sxs-lookup"><span data-stu-id="ce757-172">This property is inherited from **CIM\_EthernetPortAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="ce757-173">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="ce757-173">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce757-174">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ce757-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce757-175">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ce757-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ce757-176">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="ce757-176">A display name for the object.</span></span> <span data-ttu-id="ce757-177">Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="ce757-177">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span> <span data-ttu-id="ce757-178">Durch Ändern dieser Eigenschaft wird der Elementname der zugeordneten logischen Geräte Ableitung geändert.</span><span class="sxs-lookup"><span data-stu-id="ce757-178">Changing this property will change the element name of the associated logical device derivative.</span></span>

</dd> <dt>

<span data-ttu-id="ce757-179">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="ce757-179">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce757-180">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ce757-180">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ce757-181">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ce757-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ce757-182">Gibt an, ob die Zuordnungs Anforderung aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="ce757-182">Indicates whether the allocation request is enabled or disabled.</span></span> <span data-ttu-id="ce757-183">Wenn eine Zuordnungs Anforderung als deaktiviert markiert ist (3), wird die Zuordnung nicht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="ce757-183">When an allocation request is marked as Disabled (3), then the allocation is not processed.</span></span> <span data-ttu-id="ce757-184">Der **enabledstate** für eine aktive Konfiguration wird immer als aktiviert markiert (2).</span><span class="sxs-lookup"><span data-stu-id="ce757-184">The **EnabledState** for an active configuration is always marked as Enabled (2).</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="ce757-185">**Aktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="ce757-185">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="ce757-186">**Deaktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="ce757-186">**Disabled** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ce757-187">**"Hustresource"**</span><span class="sxs-lookup"><span data-stu-id="ce757-187">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce757-188">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="ce757-188">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ce757-189">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ce757-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ce757-190">Jedem Gerät im virtuellen Switch kann nur eine Host Ressource zugewiesen werden, sodass nur das erste Element dieses Arrays festgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="ce757-190">Only one host resource can be assigned to each device in the virtual switch, so only the first element of this array can be set.</span></span> <span data-ttu-id="ce757-191">Legen Sie für Geräte, die diese Funktion unterstützen, das erste Element des **hostresource** -Arrays so fest, dass es einen Verweis auf die zugrunde liegende Host Ressource enthält, die zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="ce757-191">For devices that support this feature, set the first element of the **HostResource** array to contain a reference to the underlying host resource to be assigned.</span></span> <span data-ttu-id="ce757-192">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ce757-192">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ce757-193">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ce757-193">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce757-194">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ce757-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce757-195">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ce757-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce757-196">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="ce757-196">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="ce757-197">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="ce757-197">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="ce757-198">Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))geerbt und ist immer auf "Microsoft:*GUID* Geräte-ID- \\ *Daten*" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ce757-198">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to "Microsoft:*GUID*\\*DeviceSpecificData*".</span></span>

</dd> <dt>

<span data-ttu-id="ce757-199">**Lastknownswitchname**</span><span class="sxs-lookup"><span data-stu-id="ce757-199">**LastKnownSwitchName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce757-200">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ce757-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce757-201">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ce757-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ce757-202">Der letzte bekannte Anzeige Name des Schalters, der für diesen Port eine harte Affinität enthielt, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ce757-202">The last known friendly name of the switch this port had a hard affinity to, if any.</span></span>

> [!Note]  
> <span data-ttu-id="ce757-203">Die Eigenschaft wurde in Windows 10 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ce757-203">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="ce757-204">**Begrenzung**</span><span class="sxs-lookup"><span data-stu-id="ce757-204">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce757-205">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ce757-205">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ce757-206">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ce757-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ce757-207">Die maximale Menge der entsprechenden Host Ressourcen, die vom virtuellen Switch genutzt werden können.</span><span class="sxs-lookup"><span data-stu-id="ce757-207">The maximum amount of corresponding host resources that can be consumed by the virtual switch.</span></span> <span data-ttu-id="ce757-208">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ce757-208">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ce757-209">**Mappingbehavior**</span><span class="sxs-lookup"><span data-stu-id="ce757-209">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce757-210">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ce757-210">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ce757-211">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ce757-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ce757-212">Gibt an, wie diese Ressource den zugrunde liegenden Ressourcen zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="ce757-212">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="ce757-213">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ce757-213">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ce757-214">**Otherendpointmode**</span><span class="sxs-lookup"><span data-stu-id="ce757-214">**OtherEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce757-215">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ce757-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce757-216">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ce757-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ce757-217">Eine Zeichenfolge, die den Typ des VLAN-Endpunkt Modells beschreibt, das von diesem VLAN-Endpunkt unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="ce757-217">A string that describes the type of VLAN endpoint model that is supported by this VLAN endpoint.</span></span> <span data-ttu-id="ce757-218">Diese Eigenschaft wird nur verwendet, wenn die **desiredvlanendpointmode** -Eigenschaft auf 1 (sonstige) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ce757-218">This property is only used when the **DesiredVLANEndpointMode** property is set to 1 (Other).</span></span> <span data-ttu-id="ce757-219">Diese Eigenschaft sollte auf **null** festgelegt werden, wenn die **desiredvlanendpointmode** -Eigenschaft einen anderen Wert als 1 hat.</span><span class="sxs-lookup"><span data-stu-id="ce757-219">This property should be set to **Null** when the **DesiredVLANEndpointMode** property is any value other than 1.</span></span> <span data-ttu-id="ce757-220">Diese Eigenschaft wird von **CIM \_ ethernetportaccesscationsettingdata** geerbt.</span><span class="sxs-lookup"><span data-stu-id="ce757-220">This property is inherited from **CIM\_EthernetPortAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="ce757-221">**Otherresourcetype**</span><span class="sxs-lookup"><span data-stu-id="ce757-221">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce757-222">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ce757-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce757-223">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ce757-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ce757-224">Eine Zeichenfolge, die den Ressourcentyp beschreibt, wenn ein klar definierter Wert nicht verfügbar ist und [**ResourceType**](msvm-processorsettingdata.md) den Wert 1 (sonstige) aufweist.</span><span class="sxs-lookup"><span data-stu-id="ce757-224">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorsettingdata.md) has the value 1 (Other).</span></span> <span data-ttu-id="ce757-225">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt und wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="ce757-225">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ce757-226">**Parent**</span><span class="sxs-lookup"><span data-stu-id="ce757-226">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce757-227">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ce757-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce757-228">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ce757-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ce757-229">Das übergeordnete Element der Ressource.</span><span class="sxs-lookup"><span data-stu-id="ce757-229">The parent of the resource.</span></span> <span data-ttu-id="ce757-230">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ce757-230">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ce757-231">**Poolid**</span><span class="sxs-lookup"><span data-stu-id="ce757-231">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce757-232">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ce757-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce757-233">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ce757-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ce757-234">Der Bezeichner des Ressourcenpools, von dem diese Ressource zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="ce757-234">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="ce757-235">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ce757-235">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ce757-236">**Requirements dfeaturehints**</span><span class="sxs-lookup"><span data-stu-id="ce757-236">**RequiredFeatureHints**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce757-237">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="ce757-237">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ce757-238">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ce757-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ce757-239">Die Liste der anzeigen Amen, die jedem Eintrag im "Requirements **dfeatures** "-Array entsprechen.</span><span class="sxs-lookup"><span data-stu-id="ce757-239">The list of display names that correspond to each entry in the **RequiredFeatures** array.</span></span>

</dd> <dt>

<span data-ttu-id="ce757-240">**Requirements-Features**</span><span class="sxs-lookup"><span data-stu-id="ce757-240">**RequiredFeatures**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce757-241">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="ce757-241">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ce757-242">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ce757-242">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ce757-243">Die Liste von Featurebezeichner, die alle für einen Port erforderlichen Features darstellen.</span><span class="sxs-lookup"><span data-stu-id="ce757-243">The list of feature identifiers that represent all the features that are required for a port.</span></span>

</dd> <dt>

<span data-ttu-id="ce757-244">**Reservierung**</span><span class="sxs-lookup"><span data-stu-id="ce757-244">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce757-245">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ce757-245">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ce757-246">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ce757-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ce757-247">Die Menge der Ressourcen, die für die Verwendung durch den virtuellen Switch reserviert sind.</span><span class="sxs-lookup"><span data-stu-id="ce757-247">The amount of resources that are reserved for use by the virtual switch.</span></span> <span data-ttu-id="ce757-248">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ce757-248">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ce757-249">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="ce757-249">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce757-250">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ce757-250">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce757-251">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ce757-251">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ce757-252">Eine Zeichenfolge, die einen Implementierungs spezifischen Untertyp für diese Ressource beschreibt.</span><span class="sxs-lookup"><span data-stu-id="ce757-252">A string that describes an implementation specific subtype for this resource.</span></span> <span data-ttu-id="ce757-253">Dies kann z. b. verwendet werden, um unterschiedliche Modelle desselben Ressourcentyps zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="ce757-253">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="ce757-254">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ce757-254">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ce757-255">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="ce757-255">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce757-256">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ce757-256">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ce757-257">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ce757-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ce757-258">Der Typ der Ressource, die diese Zuordnungs Einstellung darstellt.</span><span class="sxs-lookup"><span data-stu-id="ce757-258">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="ce757-259">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt und ist immer auf 33 (Ethernet-Verbindung) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ce757-259">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 33 (Ethernet connection).</span></span>

</dd> <dt>

<span data-ttu-id="ce757-260">**Testreplicapoolid**</span><span class="sxs-lookup"><span data-stu-id="ce757-260">**TestReplicaPoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce757-261">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ce757-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce757-262">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ce757-262">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ce757-263">Gibt den Netzwerkressourcen Pool an, aus dem beim Erstellen eine Verbindung zum Test Replikat System zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="ce757-263">Specifies the network resource pool from which a connection will be allocated to the test replica system when it is created.</span></span>

</dd> <dt>

<span data-ttu-id="ce757-264">**Testreplicaswitchname**</span><span class="sxs-lookup"><span data-stu-id="ce757-264">**TestReplicaSwitchName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce757-265">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ce757-265">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce757-266">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ce757-266">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ce757-267">Gibt den anzeigen amen des virtuellen Netzwerk Switches an, dem bei der Erstellung eine Verbindung für das Test Replikat System zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="ce757-267">Specifies the display name of the virtual network switch to which a connection will be allocated for the test replica system when it is created.</span></span>

</dd> <dt>

<span data-ttu-id="ce757-268">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="ce757-268">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce757-269">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ce757-269">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ce757-270">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ce757-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ce757-271">Die Gesamtanzahl der Ports im virtuellen Switch.</span><span class="sxs-lookup"><span data-stu-id="ce757-271">The total number of ports in the virtual switch.</span></span> <span data-ttu-id="ce757-272">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ce757-272">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ce757-273">**Virtualquantityunits**</span><span class="sxs-lookup"><span data-stu-id="ce757-273">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce757-274">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ce757-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce757-275">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ce757-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ce757-276">Gibt die Maßeinheit für die **virtualmenge** -Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="ce757-276">Specifies the unit of measurement for the **VirtualQuantity** property.</span></span> <span data-ttu-id="ce757-277">Der Wert dieser Eigenschaft muss ein gültiger Wert des Qualifizierers für programmgesteuerte Einheiten sein, wie in Anhang C. 1 von DSP0004 v 2.5 oder höher definiert.</span><span class="sxs-lookup"><span data-stu-id="ce757-277">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="ce757-278">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ce757-278">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ce757-279">**Weight**</span><span class="sxs-lookup"><span data-stu-id="ce757-279">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce757-280">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ce757-280">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ce757-281">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ce757-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ce757-282">Eine ganze Zahl, die die Gewichtung für jeden virtuellen Switch definiert.</span><span class="sxs-lookup"><span data-stu-id="ce757-282">An integer that defines the weight for each virtual switch.</span></span> <span data-ttu-id="ce757-283">Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ce757-283">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="ce757-284">Bereich: 0 1000</span><span class="sxs-lookup"><span data-stu-id="ce757-284">Range: 0 1000</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ce757-285">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ce757-285">Requirements</span></span>



| <span data-ttu-id="ce757-286">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ce757-286">Requirement</span></span> | <span data-ttu-id="ce757-287">Wert</span><span class="sxs-lookup"><span data-stu-id="ce757-287">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce757-288">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ce757-288">Minimum supported client</span></span><br/> | <span data-ttu-id="ce757-289">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ce757-289">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ce757-290">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ce757-290">Minimum supported server</span></span><br/> | <span data-ttu-id="ce757-291">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ce757-291">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ce757-292">Namespace</span><span class="sxs-lookup"><span data-stu-id="ce757-292">Namespace</span></span><br/>                | <span data-ttu-id="ce757-293">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="ce757-293">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ce757-294">MOF</span><span class="sxs-lookup"><span data-stu-id="ce757-294">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ce757-295"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ce757-295"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ce757-296">DLL</span><span class="sxs-lookup"><span data-stu-id="ce757-296">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce757-297"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ce757-297"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

