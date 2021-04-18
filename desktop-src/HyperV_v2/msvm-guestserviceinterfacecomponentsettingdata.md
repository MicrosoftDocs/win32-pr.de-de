---
description: Stellt den konfigurierten Status der Komponente der Gast Dienst Schnittstelle dar.
ms.assetid: 82B58459-9819-4F51-BEE5-AB57E444CF55
title: Msvm_GuestServiceInterfaceComponentSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestServiceInterfaceComponentSettingData
- Msvm_GuestServiceInterfaceComponentSettingData.ElementName
- Msvm_GuestServiceInterfaceComponentSettingData.InstanceID
- Msvm_GuestServiceInterfaceComponentSettingData.ResourceType
- Msvm_GuestServiceInterfaceComponentSettingData.OtherResourceType
- Msvm_GuestServiceInterfaceComponentSettingData.ResourceSubType
- Msvm_GuestServiceInterfaceComponentSettingData.PoolID
- Msvm_GuestServiceInterfaceComponentSettingData.ConsumerVisibility
- Msvm_GuestServiceInterfaceComponentSettingData.HostResource
- Msvm_GuestServiceInterfaceComponentSettingData.AllocationUnits
- Msvm_GuestServiceInterfaceComponentSettingData.VirtualQuantity
- Msvm_GuestServiceInterfaceComponentSettingData.Reservation
- Msvm_GuestServiceInterfaceComponentSettingData.Limit
- Msvm_GuestServiceInterfaceComponentSettingData.Weight
- Msvm_GuestServiceInterfaceComponentSettingData.AutomaticAllocation
- Msvm_GuestServiceInterfaceComponentSettingData.AutomaticDeallocation
- Msvm_GuestServiceInterfaceComponentSettingData.Parent
- Msvm_GuestServiceInterfaceComponentSettingData.Connection
- Msvm_GuestServiceInterfaceComponentSettingData.Address
- Msvm_GuestServiceInterfaceComponentSettingData.MappingBehavior
- Msvm_GuestServiceInterfaceComponentSettingData.EnabledState
- Msvm_GuestServiceInterfaceComponentSettingData.DefaultEnabledStatePolicy
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0ada39e4428040cf7e6732232ce789f7d837c9c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343649"
---
# <a name="msvm_guestserviceinterfacecomponentsettingdata-class"></a><span data-ttu-id="60e38-103">MSVM- \_ guestserviceinterfacetten componentsettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="60e38-103">Msvm\_GuestServiceInterfaceComponentSettingData class</span></span>

<span data-ttu-id="60e38-104">Stellt den konfigurierten Status der Komponente der Gast Dienst Schnittstelle dar.</span><span class="sxs-lookup"><span data-stu-id="60e38-104">Represents the configured state of the guest service interface component.</span></span> <span data-ttu-id="60e38-105">Diese Klasse wird von der [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) -Klasse abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="60e38-105">This class derives from the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) class.</span></span>

<span data-ttu-id="60e38-106">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="60e38-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="60e38-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="60e38-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestServiceInterfaceComponentSettingData : CIM_ResourceAllocationSettingData
{
  string  ElementName;
  string  InstanceID;
  uint16  ResourceType;
  string  OtherResourceType;
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility;
  string  HostResource[];
  string  AllocationUnits;
  uint64  VirtualQuantity;
  uint64  Reservation;
  uint64  Limit;
  uint32  Weight;
  boolean AutomaticAllocation;
  boolean AutomaticDeallocation;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  uint16  EnabledState = 3;
  uint16  DefaultEnabledStatePolicy = 2;
};
```

## <a name="members"></a><span data-ttu-id="60e38-108">Member</span><span class="sxs-lookup"><span data-stu-id="60e38-108">Members</span></span>

<span data-ttu-id="60e38-109">Die **MSVM \_ guestserviceinterfacecomponentsettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="60e38-109">The **Msvm\_GuestServiceInterfaceComponentSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="60e38-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="60e38-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="60e38-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="60e38-111">Properties</span></span>

<span data-ttu-id="60e38-112">Die **MSVM \_ guestserviceinterfacecomponentsettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="60e38-112">The **Msvm\_GuestServiceInterfaceComponentSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="60e38-113">**Adresse**</span><span class="sxs-lookup"><span data-stu-id="60e38-113">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60e38-114">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60e38-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60e38-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60e38-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60e38-116">Die Adresse der Ressource.</span><span class="sxs-lookup"><span data-stu-id="60e38-116">The address of the resource.</span></span> <span data-ttu-id="60e38-117">Beispielsweise die Mac-Adresse eines Ethernet-Ports.</span><span class="sxs-lookup"><span data-stu-id="60e38-117">For example, the MAC address of a Ethernet port.</span></span>

</dd> <dt>

<span data-ttu-id="60e38-118">**Zuordnung von Einheiten**</span><span class="sxs-lookup"><span data-stu-id="60e38-118">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60e38-119">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60e38-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60e38-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60e38-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60e38-121">Diese Eigenschaft gibt die Zuordnungs Einheiten an, die von den Reservierungs-und Limit-Eigenschaften verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="60e38-121">This property specifies the units of allocation used by the Reservation and Limit properties.</span></span> <span data-ttu-id="60e38-122">Wenn z. b. ResourceType = Processor ist, kann zugcationunits auf MHz festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="60e38-122">For example, when ResourceType=Processor, AllocationUnits may be set to MHz.</span></span> <span data-ttu-id="60e38-123">Wenn ResourceType = Memory, kann ' zugcationunits ' auf ' MB ' festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="60e38-123">When ResourceType=Memory, AllocationUnits may be set to MB</span></span>

</dd> <dt>

<span data-ttu-id="60e38-124">**Automaticallocation**</span><span class="sxs-lookup"><span data-stu-id="60e38-124">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60e38-125">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="60e38-125">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="60e38-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60e38-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60e38-127">Diese Eigenschaft gibt an, ob die Ressource automatisch zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="60e38-127">This property specifies if the resource will be automatically allocated.</span></span> <span data-ttu-id="60e38-128">Wenn z. b. auf true festgelegt ist, wird diese Ressource zugeordnet, wenn das verarbeitende virtuelle Computersystem eingeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="60e38-128">For example when set to true, when the consuming virtual computer system is powered on, this resource would be allocated.</span></span> <span data-ttu-id="60e38-129">Der Wert false gibt an, dass die Ressource explizit zugewiesen werden muss.</span><span class="sxs-lookup"><span data-stu-id="60e38-129">A value of false indicates the resource must be explicitly allocated.</span></span> <span data-ttu-id="60e38-130">Die Einstellung kann z. b. ein Wechselmedium (d. h. Rom oder Disketten) darstellen, bei dem die Medien bei der Stromversorgung nicht vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="60e38-130">For example, the setting may represent removable media (that is, cdrom or floppy) where at power on time, the media is not present.</span></span> <span data-ttu-id="60e38-131">Ein expliziter Vorgang ist erforderlich, um die Ressource zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="60e38-131">An explicit operation is required to allocate the resource.</span></span>

</dd> <dt>

<span data-ttu-id="60e38-132">**Automaticdeallocation**</span><span class="sxs-lookup"><span data-stu-id="60e38-132">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60e38-133">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="60e38-133">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="60e38-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60e38-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60e38-135">Diese Eigenschaft gibt an, ob die Zuordnung der Ressource automatisch aufgehoben wird.</span><span class="sxs-lookup"><span data-stu-id="60e38-135">This property specifies if the resource will be automatically deallocated.</span></span> <span data-ttu-id="60e38-136">Wenn z. b. auf true festgelegt ist, wird die Zuordnung dieser Ressource aufgehoben, wenn das verarbeitende virtuelle Computer ausgeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="60e38-136">For example, when set to true, when the consuming virtual computer system is powered off, this resource would be deallocated.</span></span> <span data-ttu-id="60e38-137">Wenn false festgelegt ist, bleibt die Ressource reserviert, und die Zuordnung muss explizit aufgehoben werden.</span><span class="sxs-lookup"><span data-stu-id="60e38-137">When set to false, the resource will remain allocated and must be explicitly deallocated.</span></span>

</dd> <dt>

<span data-ttu-id="60e38-138">**Connection**</span><span class="sxs-lookup"><span data-stu-id="60e38-138">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60e38-139">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="60e38-139">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="60e38-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60e38-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60e38-141">Das, mit dem diese Ressource verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="60e38-141">The thing to which this resource is connected.</span></span> <span data-ttu-id="60e38-142">Beispielsweise ein benanntes Netzwerk oder ein Switchport.</span><span class="sxs-lookup"><span data-stu-id="60e38-142">For example, a named network or switch port.</span></span>

</dd> <dt>

<span data-ttu-id="60e38-143">**Consumersichtbarkeit**</span><span class="sxs-lookup"><span data-stu-id="60e38-143">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60e38-144">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="60e38-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="60e38-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60e38-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60e38-146">Beschreibt die Benutzer Sichtbarkeit der zugeordneten Ressource.</span><span class="sxs-lookup"><span data-stu-id="60e38-146">Describes the consumers visibility to the allocated resource.</span></span>



| <span data-ttu-id="60e38-147">Wert</span><span class="sxs-lookup"><span data-stu-id="60e38-147">Value</span></span>                                                                                                                                                                                                                                                                  | <span data-ttu-id="60e38-148">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="60e38-148">Meaning</span></span>                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="60e38-149"><dt>**Unbekannter**</dt> Wert <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="60e38-149"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                            | <span data-ttu-id="60e38-150">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="60e38-150">Unknown.</span></span><br/>                                                                                                                                                                                                                                         |
| <span id="Passed-Through"></span><span id="passed-through"></span><span id="PASSED-THROUGH"></span><dl> <span data-ttu-id="60e38-151"><dt>**Durchlaufen**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="60e38-151"><dt>**Passed-Through**</dt> <dt>2</dt></span></span> </dl>                | <span data-ttu-id="60e38-152">Die zugrunde liegende-oder-Host Ressource wird verwendet und an den Consumer übermittelt, möglicherweise mithilfe der Partitionierung.</span><span class="sxs-lookup"><span data-stu-id="60e38-152">The underlying or host resource is utilized and passed through to the consumer, possibly using partitioning.</span></span> <span data-ttu-id="60e38-153">In der Eigenschaft "Eigenschaft" muss mindestens ein Element vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="60e38-153">At least one item shall be present in the DeviceID property.</span></span><br/>                                                                        |
| <span id="Virtualized"></span><span id="virtualized"></span><span id="VIRTUALIZED"></span><dl> <span data-ttu-id="60e38-154"><dt>**Virtualisiert**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="60e38-154"><dt>**Virtualized**</dt> <dt>3</dt></span></span> </dl>                            | <span data-ttu-id="60e38-155">Die Ressource ist virtualisiert und darf nicht direkt einer zugrunde liegenden/Host Ressource zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="60e38-155">The resource is virtualized and may not map directly to an underlying/host resource.</span></span> <span data-ttu-id="60e38-156">Einige Implementierungen unterstützen möglicherweise eine bestimmte Zuweisung für virtualisierte Ressourcen. in diesem Fall werden die Host Ressourcen mithilfe der DeviceID-Eigenschaft verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="60e38-156">Some implementations may support specific assignment for virtualized resources, in which case the host resource(s) are exposed using the DeviceID property.</span></span><br/> |
| <span id="Not_represented"></span><span id="not_represented"></span><span id="NOT_REPRESENTED"></span><dl> <span data-ttu-id="60e38-157"><dt>**Nicht dargestellt**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="60e38-157"><dt>**Not represented**</dt> <dt>4</dt></span></span> </dl>            | <span data-ttu-id="60e38-158">Eine Darstellung der Ressource ist nicht im Kontext des ressourcenconsumers vorhanden.</span><span class="sxs-lookup"><span data-stu-id="60e38-158">A representation of the resource does not exist within the context of the resource consumer.</span></span><br/>                                                                                                                                                     |
| <span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="60e38-159"><dt>**DMTF reserviert**</dt> <dt>..</dt></span><span class="sxs-lookup"><span data-stu-id="60e38-159"><dt>**DMTF reserved**</dt> <dt>..</dt></span></span> </dl>                   |                                                                                                                                                                                                                                                             |
| <span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span><dl> <span data-ttu-id="60e38-160"><dt>**Hersteller reserviert**</dt> <dt>32767.65535</dt></span><span class="sxs-lookup"><span data-stu-id="60e38-160"><dt>**Vendor Reserved**</dt> <dt>32767..65535</dt></span></span> </dl> |                                                                                                                                                                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="60e38-161">**Defaultenabledstatepolicy**</span><span class="sxs-lookup"><span data-stu-id="60e38-161">**DefaultEnabledStatePolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60e38-162">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="60e38-162">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="60e38-163">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60e38-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60e38-164">Der aktivierte und deaktivierte Status der Gast Kommunikationsdienste standardmäßig.</span><span class="sxs-lookup"><span data-stu-id="60e38-164">The enabled and disabled states of guest communication services by default.</span></span>

<span data-ttu-id="60e38-165">Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**modifyresourcesettings**](cim-virtualsystemmanagementservice-modifyresourcesettings.md) -Methode der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="60e38-165">This is a read-only property, but it can be changed using the [**ModifyResourceSettings**](cim-virtualsystemmanagementservice-modifyresourcesettings.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

> [!Note]  
> <span data-ttu-id="60e38-166">In Windows 10 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="60e38-166">Added in Windows 10.</span></span>

 

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="60e38-167">**Aktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="60e38-167">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="60e38-168">**Deaktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="60e38-168">**Disabled** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="60e38-169">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="60e38-169">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60e38-170">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60e38-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60e38-171">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60e38-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60e38-172">Der Anzeige Name für diese Instanz von SettingData.</span><span class="sxs-lookup"><span data-stu-id="60e38-172">The display name for this instance of SettingData.</span></span> <span data-ttu-id="60e38-173">Außerdem kann der Anzeige Name als Index Eigenschaft für eine Suche oder Abfrage verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="60e38-173">In addition, the display name can be used as an index property for a search or query.</span></span> <span data-ttu-id="60e38-174">(Hinweis: der Name muss innerhalb eines Namespace nicht eindeutig sein.)</span><span class="sxs-lookup"><span data-stu-id="60e38-174">(Note: The name does not have to be unique within a namespace.)</span></span>

</dd> <dt>

<span data-ttu-id="60e38-175">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="60e38-175">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60e38-176">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="60e38-176">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="60e38-177">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60e38-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60e38-178">Der aktivierte und deaktivierte Status eines Elements.</span><span class="sxs-lookup"><span data-stu-id="60e38-178">The enabled and disabled states of an element.</span></span>

<span data-ttu-id="60e38-179">Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die jedoch mit der [**modifyvirtualsystemresources**](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice) -Methode (oder mit [**modifyresourcesettings**](cim-virtualsystemmanagementservice-modifyresourcesettings.md) in Windows 10 oder höher) der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="60e38-179">This is a read-only property, but it can be changed by using the [**ModifyVirtualSystemResources**](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice) method (or [**ModifyResourceSettings**](cim-virtualsystemmanagementservice-modifyresourcesettings.md) in Windows 10 or later) of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="60e38-180">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="60e38-180">Valid values are:</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="60e38-181">**Aktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="60e38-181">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="60e38-182">**Deaktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="60e38-182">**Disabled** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="60e38-183">**"Hustresource"**</span><span class="sxs-lookup"><span data-stu-id="60e38-183">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60e38-184">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="60e38-184">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="60e38-185">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60e38-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60e38-186">Diese Eigenschaft macht eine bestimmte Zuweisung zu Host-oder zugrunde liegenden Ressourcen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="60e38-186">This property exposes specific assignment to host or underlying resources.</span></span> <span data-ttu-id="60e38-187">Die eingebetteten Instanzen dürfen nur Schlüsseleigenschaften enthalten und als Objekt Pfade behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="60e38-187">The embedded instances shall contain only key properties and be treated as Object Paths.</span></span> <span data-ttu-id="60e38-188">Wenn die virtuelle Ressource möglicherweise für eine Reihe von zugrunde liegenden Ressourcen geplant ist, sollte diese Eigenschaft **null** bleiben.</span><span class="sxs-lookup"><span data-stu-id="60e38-188">If the virtual resource may be scheduled on a number of underlying resources, this property should remain **NULL**.</span></span> <span data-ttu-id="60e38-189">In diesem Fall können die Zuordnungen devicezugedfrompool oder resourcezucationfrompool verwendet werden, um den Pool von Host Ressourcen zu ermitteln, auf dem diese virtuelle Ressource möglicherweise geplant ist.</span><span class="sxs-lookup"><span data-stu-id="60e38-189">In that case, the DeviceAllocatedFromPool or ResourceAllocationFromPool associations may be used to determine the pool of host resources on which this virtual resource may be scheduled.</span></span> <span data-ttu-id="60e38-190">Wenn eine bestimmte Zuweisung verwendet wird, werden alle zugrunde liegenden Ressourcen, die von dieser virtuellen Ressource verwendet werden, in diesem Array aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="60e38-190">If specific assignment is utilized, all underlying resources used by this virtual resource shall be listed in this array.</span></span> <span data-ttu-id="60e38-191">In der Regel enthält das Array ein Element. für Aggregat Zuordnungen, z. b. mehrere Prozessoren, können jedoch mehrere Host Ressourcen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="60e38-191">Typically, the array will contain one item, however for aggregate allocations, such as multiple processors, multiple host resources may be specified.</span></span>

</dd> <dt>

<span data-ttu-id="60e38-192">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="60e38-192">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60e38-193">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60e38-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60e38-194">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60e38-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60e38-195">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="60e38-195">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="60e38-196">Im Gültigkeitsbereich des instanziierten Namespaces identifiziert InstanceId verdeckt und identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="60e38-196">Within the scope of the instantiating Namespace, InstanceID opaquely and uniquely identifies an instance of this class.</span></span> <span data-ttu-id="60e38-197">Um die Eindeutigkeit innerhalb des Namespaces sicherzustellen, sollte der Wert von InstanceId mit dem folgenden "bevorzugten" Algorithmus erstellt werden: *OrgId*:*localId* , bei der *OrgId* und *localId* durch einen Doppelpunkt (:)) getrennt sind und *OrgId* einen urheberrechtlich geschützten, mit einem Wert gekennzeichneten oder anderweitig eindeutigen Namen enthalten muss, der im Besitz der Geschäfts Entität ist, die die InstanceId erstellt oder definiert, oder bei der es sich um eine registrierte, von einer anerkannten globalen Autorität zugewiesene ID handelt.</span><span class="sxs-lookup"><span data-stu-id="60e38-197">To ensure uniqueness within the NameSpace, the value of InstanceID should be constructed using the following "preferred" algorithm: *OrgID*:*LocalID* Where *OrgID* and *LocalID* are separated by a colon (:), and where *OrgID* must include a copyrighted, trademarked, or otherwise unique name that is owned by the business entity that is creating or defining the InstanceID or that is a registered ID assigned to the business entity by a recognized global authority.</span></span> <span data-ttu-id="60e38-198">(Diese Anforderung ähnelt dem Schema *Name* \_ *ClassName* -Struktur von Schema Klassennamen.) Außerdem darf *OrgId* keinen Doppelpunkt (:) enthalten, um die Eindeutigkeit sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="60e38-198">(This requirement is similar to the *SchemaName*\_*ClassName* structure of Schema class names.) In addition, to ensure uniqueness, *OrgID* must not contain a colon (:).</span></span> <span data-ttu-id="60e38-199">Wenn dieser Algorithmus verwendet wird, muss der erste Doppelpunkt, der in InstanceId angezeigt wird, zwischen *OrgId* und *localId* angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="60e38-199">When using this algorithm, the first colon to appear in InstanceID must appear between *OrgID* and *LocalID*.</span></span> <span data-ttu-id="60e38-200">*LocalId* wird von der Geschäfts Entität ausgewählt und sollte nicht wieder verwendet werden, um verschiedene zugrunde liegende (reale) Elemente zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="60e38-200">*LocalID* is chosen by the business entity and should not be reused to identify different underlying (real-world) elements.</span></span> <span data-ttu-id="60e38-201">Wenn der oben genannte "bevorzugte" Algorithmus nicht verwendet wird, muss die definierende Entität sicherstellen, dass die resultierende InstanceId nicht in allen instanceids wieder verwendet wird, die von diesem oder anderen Anbietern für den Namespace dieser Instanz erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="60e38-201">If the above "preferred" algorithm is not used, the defining entity must assure that the resulting InstanceID is not reused across any InstanceIDs produced by this or other providers for the NameSpace of this instance.</span></span> <span data-ttu-id="60e38-202">Für von DMTF definierte Instanzen muss der "bevorzugte" Algorithmus verwendet werden, wenn die *OrgId* auf CIM festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="60e38-202">For DMTF-defined instances, the "preferred" algorithm must be used with the *OrgID* set to CIM.</span></span>

</dd> <dt>

<span data-ttu-id="60e38-203">**Begrenzung**</span><span class="sxs-lookup"><span data-stu-id="60e38-203">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60e38-204">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="60e38-204">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="60e38-205">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60e38-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60e38-206">Diese Eigenschaft gibt die obere Grenze oder die maximale Menge an Ressourcen an, die für diese Zuweisung gewährt wird.</span><span class="sxs-lookup"><span data-stu-id="60e38-206">This property specifies the upper bound, or maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="60e38-207">Beispielsweise kann ein System, das die Speicher Auslagerung unterstützt, das Festlegen des Limits einer Speicher Belegung unterhalb der virtualmenge unterstützen, wodurch das Paging für diese Zuweisung erzwungen wird.</span><span class="sxs-lookup"><span data-stu-id="60e38-207">For example, a system which supports memory paging may support setting the Limit of a Memory allocation below that of the VirtualQuantity, thus forcing paging to occur for this allocation.</span></span>

</dd> <dt>

<span data-ttu-id="60e38-208">**Mappingbehavior**</span><span class="sxs-lookup"><span data-stu-id="60e38-208">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60e38-209">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="60e38-209">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="60e38-210">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60e38-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60e38-211">Gibt an, wie diese Ressource den zugrunde liegenden Ressourcen zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="60e38-211">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="60e38-212">Wenn das "custresource"-Array Einträge enthält, gibt diese Eigenschaft an, wie die Ressource diesen spezifischen Ressourcen zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="60e38-212">If the HostResource array contains any entries, this property reflects how the resource maps to those specific resources.</span></span>

<dl> <dt>

<span data-ttu-id="60e38-213"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="60e38-213"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="60e38-214"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="60e38-214"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="60e38-215"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dediziert** (2)</span><span class="sxs-lookup"><span data-stu-id="60e38-215"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (2)</span></span>
</dt> <dt>

<span data-ttu-id="60e38-216"><span id="Soft_Affinity"></span><span id="soft_affinity"></span><span id="SOFT_AFFINITY"></span>**Weiche Affinität** (3)</span><span class="sxs-lookup"><span data-stu-id="60e38-216"><span id="Soft_Affinity"></span><span id="soft_affinity"></span><span id="SOFT_AFFINITY"></span>**Soft Affinity** (3)</span></span>
</dt> <dt>

<span data-ttu-id="60e38-217"><span id="Hard_Affinity"></span><span id="hard_affinity"></span><span id="HARD_AFFINITY"></span>**Harte Affinität** (4)</span><span class="sxs-lookup"><span data-stu-id="60e38-217"><span id="Hard_Affinity"></span><span id="hard_affinity"></span><span id="HARD_AFFINITY"></span>**Hard Affinity** (4)</span></span>
</dt> <dt>

<span data-ttu-id="60e38-218"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="60e38-218"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="60e38-219"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Hersteller reserviert** (32767.65535)</span><span class="sxs-lookup"><span data-stu-id="60e38-219"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32767..65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="60e38-220">**Otherresourcetype**</span><span class="sxs-lookup"><span data-stu-id="60e38-220">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60e38-221">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60e38-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60e38-222">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60e38-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60e38-223">Eine Zeichenfolge, die den Ressourcentyp beschreibt, wenn ein klar definierter Wert nicht verfügbar ist und ResourceType den Wert "Other" hat.</span><span class="sxs-lookup"><span data-stu-id="60e38-223">A string that describes the resource type when a well defined value is not available and ResourceType has the value "Other".</span></span>

</dd> <dt>

<span data-ttu-id="60e38-224">**Parent**</span><span class="sxs-lookup"><span data-stu-id="60e38-224">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60e38-225">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60e38-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60e38-226">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60e38-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60e38-227">Das übergeordnete Element der Ressource.</span><span class="sxs-lookup"><span data-stu-id="60e38-227">The Parent of the resource.</span></span> <span data-ttu-id="60e38-228">Beispielsweise ein Controller für die aktuelle Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="60e38-228">For example, a controller for the current allocation.</span></span>

</dd> <dt>

<span data-ttu-id="60e38-229">**Poolid**</span><span class="sxs-lookup"><span data-stu-id="60e38-229">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60e38-230">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60e38-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60e38-231">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60e38-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60e38-232">Diese Eigenschaft gibt an, von welchem resourcepool die Ressource derzeit zugeordnet ist, oder welcher resourcepool die Ressource bei der Zuordnung zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="60e38-232">This property specifies which ResourcePool the resource is currently allocated from, or which ResourcePool the resource will be allocated from when the allocation occurs.</span></span>

</dd> <dt>

<span data-ttu-id="60e38-233">**Reservierung**</span><span class="sxs-lookup"><span data-stu-id="60e38-233">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60e38-234">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="60e38-234">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="60e38-235">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60e38-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60e38-236">Diese Eigenschaft gibt die Menge der Ressourcen an, die für diese Zuordnung garantiert verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="60e38-236">This property specifies the amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="60e38-237">Auf dem System, das eine Überbelegung von Ressourcen unterstützt, wird dieser Wert in der Regel für die Zugangskontrolle verwendet, um zu verhindern, dass eine Zuordnung akzeptiert wird, wodurch Ressourcenmangel verhindert wird.</span><span class="sxs-lookup"><span data-stu-id="60e38-237">On system which support over-commitment of resources, this value is typically used for admission control to prevent an an allocation from being accepted thus preventing resource depletion.</span></span>

</dd> <dt>

<span data-ttu-id="60e38-238">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="60e38-238">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60e38-239">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60e38-239">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60e38-240">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60e38-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60e38-241">Eine Zeichenfolge, die einen Implementierungs spezifischen Untertyp für diese Ressource beschreibt.</span><span class="sxs-lookup"><span data-stu-id="60e38-241">A string describing an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="60e38-242">Dies kann z. b. verwendet werden, um unterschiedliche Modelle desselben Ressourcentyps zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="60e38-242">For example, this may be used to distinguish different models of the same resource type.</span></span>

</dd> <dt>

<span data-ttu-id="60e38-243">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="60e38-243">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60e38-244">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="60e38-244">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="60e38-245">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60e38-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60e38-246">Der Typ der Ressource, die diese Zuordnungs Einstellung darstellt.</span><span class="sxs-lookup"><span data-stu-id="60e38-246">The type of resource this allocation setting represents.</span></span>

<dl> <dt>

<span data-ttu-id="60e38-247"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="60e38-247"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="60e38-248"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span><span class="sxs-lookup"><span data-stu-id="60e38-248"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span></span>
</dt> <dt>

<span data-ttu-id="60e38-249"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Prozessor** (3)</span><span class="sxs-lookup"><span data-stu-id="60e38-249"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processor** (3)</span></span>
</dt> <dt>

<span data-ttu-id="60e38-250"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>Arbeits **Speicher** (4)</span><span class="sxs-lookup"><span data-stu-id="60e38-250"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memory** (4)</span></span>
</dt> <dt>

<span data-ttu-id="60e38-251"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE-Controller** (5)</span><span class="sxs-lookup"><span data-stu-id="60e38-251"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE Controller** (5)</span></span>
</dt> <dt>

<span data-ttu-id="60e38-252"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Paralleler SCSI-HBA** (6)</span><span class="sxs-lookup"><span data-stu-id="60e38-252"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Parallel SCSI HBA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="60e38-253"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC-HBA** (7)</span><span class="sxs-lookup"><span data-stu-id="60e38-253"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7)</span></span>
</dt> <dt>

<span data-ttu-id="60e38-254"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**iSCSI-HBA** (8)</span><span class="sxs-lookup"><span data-stu-id="60e38-254"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**iSCSI HBA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="60e38-255"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span><span class="sxs-lookup"><span data-stu-id="60e38-255"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="60e38-256"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet-Adapter** (10)</span><span class="sxs-lookup"><span data-stu-id="60e38-256"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet Adapter** (10)</span></span>
</dt> <dt>

<span data-ttu-id="60e38-257"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Anderer Netzwerk Adapter** (11)</span><span class="sxs-lookup"><span data-stu-id="60e38-257"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Other Network Adapter** (11)</span></span>
</dt> <dt>

<span data-ttu-id="60e38-258"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>E **/a-Slot** (12)</span><span class="sxs-lookup"><span data-stu-id="60e38-258"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**I/O Slot** (12)</span></span>
</dt> <dt>

<span data-ttu-id="60e38-259"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>E **/a-Gerät** (13)</span><span class="sxs-lookup"><span data-stu-id="60e38-259"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**I/O Device** (13)</span></span>
</dt> <dt>

<span data-ttu-id="60e38-260"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Diskettenlaufwerk** (14)</span><span class="sxs-lookup"><span data-stu-id="60e38-260"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Floppy Drive** (14)</span></span>
</dt> <dt>

<span data-ttu-id="60e38-261"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD-Laufwerk** (15)</span><span class="sxs-lookup"><span data-stu-id="60e38-261"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD Drive** (15)</span></span>
</dt> <dt>

<span data-ttu-id="60e38-262"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD-Laufwerk** (16)</span><span class="sxs-lookup"><span data-stu-id="60e38-262"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD drive** (16)</span></span>
</dt> <dt>

<span data-ttu-id="60e38-263"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Seriellen Anschluss** (17)</span><span class="sxs-lookup"><span data-stu-id="60e38-263"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Serial port** (17)</span></span>
</dt> <dt>

<span data-ttu-id="60e38-264"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Paralleler Anschluss** (18)</span><span class="sxs-lookup"><span data-stu-id="60e38-264"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Parallel port** (18)</span></span>
</dt> <dt>

<span data-ttu-id="60e38-265"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB-Controller** (19)</span><span class="sxs-lookup"><span data-stu-id="60e38-265"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB Controller** (19)</span></span>
</dt> <dt>

<span data-ttu-id="60e38-266"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Grafikcontroller** (20)</span><span class="sxs-lookup"><span data-stu-id="60e38-266"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Graphics controller** (20)</span></span>
</dt> <dt>

<span data-ttu-id="60e38-267"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Speicher** Block (21)</span><span class="sxs-lookup"><span data-stu-id="60e38-267"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Storage Extent** (21)</span></span>
</dt> <dt>

<span data-ttu-id="60e38-268"><span id="Disk"></span><span id="disk"></span><span id="DISK"></span>Daten **Träger (22** )</span><span class="sxs-lookup"><span data-stu-id="60e38-268"><span id="Disk"></span><span id="disk"></span><span id="DISK"></span>**Disk** (22)</span></span>
</dt> <dt>

<span data-ttu-id="60e38-269"><span id="Tape"></span><span id="tape"></span><span id="TAPE"></span>**Band** (23)</span><span class="sxs-lookup"><span data-stu-id="60e38-269"><span id="Tape"></span><span id="tape"></span><span id="TAPE"></span>**Tape** (23)</span></span>
</dt> <dt>

<span data-ttu-id="60e38-270"><span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Anderes Speichergerät** (24)</span><span class="sxs-lookup"><span data-stu-id="60e38-270"><span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Other storage device** (24)</span></span>
</dt> <dt>

<span data-ttu-id="60e38-271"><span id="Firewire_Controller"></span><span id="firewire_controller"></span><span id="FIREWIRE_CONTROLLER"></span>**Firewire-Controller** (25)</span><span class="sxs-lookup"><span data-stu-id="60e38-271"><span id="Firewire_Controller"></span><span id="firewire_controller"></span><span id="FIREWIRE_CONTROLLER"></span>**Firewire Controller** (25)</span></span>
</dt> <dt>

<span data-ttu-id="60e38-272"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Partitionier Bare Einheit** (26)</span><span class="sxs-lookup"><span data-stu-id="60e38-272"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Partitionable Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="60e38-273"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Partitionier bare Basiseinheit** (27)</span><span class="sxs-lookup"><span data-stu-id="60e38-273"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Base Partitionable Unit** (27)</span></span>
</dt> <dt>

<span data-ttu-id="60e38-274"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Netzteil** (28)</span><span class="sxs-lookup"><span data-stu-id="60e38-274"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Power Supply** (28)</span></span>
</dt> <dt>

<span data-ttu-id="60e38-275"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Kühl Gerät** (29)</span><span class="sxs-lookup"><span data-stu-id="60e38-275"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Cooling Device** (29)</span></span>
</dt> <dt>

<span data-ttu-id="60e38-276"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="60e38-276"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="60e38-277"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Hersteller reserviert** (32767.65535)</span><span class="sxs-lookup"><span data-stu-id="60e38-277"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32767..65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="60e38-278">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="60e38-278">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60e38-279">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="60e38-279">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="60e38-280">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60e38-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60e38-281">Diese Eigenschaft gibt die Menge der Ressourcen an, die dem Consumer vorgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="60e38-281">This property specifies the quantity of resources presented to the consumer.</span></span> <span data-ttu-id="60e38-282">Wenn beispielsweise ResourceType = Processor ist, würde diese Eigenschaft die Anzahl der diskreten Prozessoren widerspiegeln, die dem virtuellen Computersystem präsentiert werden.</span><span class="sxs-lookup"><span data-stu-id="60e38-282">For example, when ResourceType=Processor, this property would reflect the number of discrete Processors presented to the virtual computer system.</span></span> <span data-ttu-id="60e38-283">Wenn ResourceType = Arbeitsspeicher vorhanden ist, kann diese Eigenschaft die Anzahl der MB widerspiegeln, die dem virtuellen Computersystem gemeldet wurden.</span><span class="sxs-lookup"><span data-stu-id="60e38-283">When ResourceType=Memory, this property could reflect the number of MB reported to the virtual computer system.</span></span>

</dd> <dt>

<span data-ttu-id="60e38-284">**Weight**</span><span class="sxs-lookup"><span data-stu-id="60e38-284">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60e38-285">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="60e38-285">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="60e38-286">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60e38-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60e38-287">Diese Eigenschaft gibt eine relative Priorität für diese Zuordnung in Bezug auf andere Zuordnungen desselben resourcepools an.</span><span class="sxs-lookup"><span data-stu-id="60e38-287">This property specifies a relative priority for this allocation in relation to other allocations from the same ResourcePool.</span></span> <span data-ttu-id="60e38-288">Diese Eigenschaft hat keine Maßeinheit und ist nur im Vergleich zu anderen Zuordnungen relevant, die für dieselben Host Ressourcen konkurrieren.</span><span class="sxs-lookup"><span data-stu-id="60e38-288">This property has no unit of measure, and is only relevant when compared to other allocations competing for the same host resources.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="60e38-289">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="60e38-289">Requirements</span></span>



| <span data-ttu-id="60e38-290">Anforderung</span><span class="sxs-lookup"><span data-stu-id="60e38-290">Requirement</span></span> | <span data-ttu-id="60e38-291">Wert</span><span class="sxs-lookup"><span data-stu-id="60e38-291">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60e38-292">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="60e38-292">Minimum supported client</span></span><br/> | <span data-ttu-id="60e38-293">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="60e38-293">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="60e38-294">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="60e38-294">Minimum supported server</span></span><br/> | <span data-ttu-id="60e38-295">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="60e38-295">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="60e38-296">Namespace</span><span class="sxs-lookup"><span data-stu-id="60e38-296">Namespace</span></span><br/>                | <span data-ttu-id="60e38-297">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="60e38-297">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="60e38-298">MOF</span><span class="sxs-lookup"><span data-stu-id="60e38-298">MOF</span></span><br/>                      | <dl> <span data-ttu-id="60e38-299"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="60e38-299"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="60e38-300">DLL</span><span class="sxs-lookup"><span data-stu-id="60e38-300">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60e38-301"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="60e38-301"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="60e38-302">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="60e38-302">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60e38-303">**CIM \_ resourcezubesettingdata**</span><span class="sxs-lookup"><span data-stu-id="60e38-303">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="60e38-304">**CIM \_ resourcezubesettingdata**</span><span class="sxs-lookup"><span data-stu-id="60e38-304">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 

