---
description: Stellt die Ressourcen Zuordnungs Einstellungen eines verwalteten Elements für einen bestimmten Ressourcentyp dar.
ms.assetid: f27910c7-a88a-4694-80fe-7761945782e0
title: CIM_AllocationCapabilities-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AllocationCapabilities
- CIM_AllocationCapabilities.ResourceType
- CIM_AllocationCapabilities.OtherResourceType
- CIM_AllocationCapabilities.ResourceSubType
- CIM_AllocationCapabilities.RequestTypesSupported
- CIM_AllocationCapabilities.SharingMode
- CIM_AllocationCapabilities.SupportedAddStates
- CIM_AllocationCapabilities.SupportedRemoveStates
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d022023142b38905067e30a4c1be3b133e49a86f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342632"
---
# <a name="cim_allocationcapabilities-class"></a><span data-ttu-id="ac6c5-103">CIM- \_ Klasse "Zuordnung"</span><span class="sxs-lookup"><span data-stu-id="ac6c5-103">CIM\_AllocationCapabilities class</span></span>

<span data-ttu-id="ac6c5-104">Stellt die Ressourcen Zuordnungs Einstellungen eines verwalteten Elements für einen bestimmten Ressourcentyp dar.</span><span class="sxs-lookup"><span data-stu-id="ac6c5-104">Represents the resource allocation settings of a managed element for a specific resource type.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac6c5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac6c5-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Capabilities"), AMENDMENT]
class CIM_AllocationCapabilities : CIM_Capabilities
{
  uint16 ResourceType;
  string OtherResourceType;
  string ResourceSubType;
  uint16 RequestTypesSupported;
  uint16 SharingMode;
  uint16 SupportedAddStates[];
  uint16 SupportedRemoveStates[];
};
```

## <a name="members"></a><span data-ttu-id="ac6c5-106">Member</span><span class="sxs-lookup"><span data-stu-id="ac6c5-106">Members</span></span>

<span data-ttu-id="ac6c5-107">Die **CIM \_** -Klasse "-Zuordnung" weist die folgenden Typen von Membern auf:</span><span class="sxs-lookup"><span data-stu-id="ac6c5-107">The **CIM\_AllocationCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="ac6c5-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ac6c5-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ac6c5-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ac6c5-109">Properties</span></span>

<span data-ttu-id="ac6c5-110">Die **CIM \_** -Klasse "Zuweisung von Klassen" verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ac6c5-110">The **CIM\_AllocationCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ac6c5-111">**Otherresourcetype**</span><span class="sxs-lookup"><span data-stu-id="ac6c5-111">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac6c5-112">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ac6c5-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac6c5-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ac6c5-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac6c5-114">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ resourcezucationsettingdata**](cim-resourceallocationsettingdata.md)".**ResourceType**")</span><span class="sxs-lookup"><span data-stu-id="ac6c5-114">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md).**ResourceType**")</span></span>
</dt> </dl>

<span data-ttu-id="ac6c5-115">Der Ressourcentyp für diese Zuordnungs Einstellung, wenn die **ResourceType** -Eigenschaft auf "1" (sonstige) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ac6c5-115">The resource type for this allocation setting when the **ResourceType** property is set to "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="ac6c5-116">**Requesttypessupported**</span><span class="sxs-lookup"><span data-stu-id="ac6c5-116">**RequestTypesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac6c5-117">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ac6c5-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ac6c5-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ac6c5-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac6c5-119">Gibt an, ob die Anforderung einer bestimmten Ressource unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="ac6c5-119">Indicates whether requesting a specific resource is supported.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ac6c5-120"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-120"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Specific"></span><span id="specific"></span><span id="SPECIFIC"></span>

<span data-ttu-id="ac6c5-121"><span id="Specific"></span><span id="specific"></span><span id="SPECIFIC"></span>**Spezifisch** (2)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-121"><span id="Specific"></span><span id="specific"></span><span id="SPECIFIC"></span>**Specific** (2)</span></span>


</dt> <dd>

<span data-ttu-id="ac6c5-122">Die Anforderung kann eine Anforderung für eine bestimmte Ressource enthalten.</span><span class="sxs-lookup"><span data-stu-id="ac6c5-122">Request can include a request for specific resource.</span></span>

</dd> <dt>

<span id="General"></span><span id="general"></span><span id="GENERAL"></span>

<span data-ttu-id="ac6c5-123"><span id="General"></span><span id="general"></span><span id="GENERAL"></span>**Allgemein** (3)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-123"><span id="General"></span><span id="general"></span><span id="GENERAL"></span>**General** (3)</span></span>


</dt> <dd>

<span data-ttu-id="ac6c5-124">Die Anforderung enthält keine bestimmte Ressource.</span><span class="sxs-lookup"><span data-stu-id="ac6c5-124">Request does not include specific resource.</span></span>

</dd> <dt>

<span id="Both"></span><span id="both"></span><span id="BOTH"></span>

<span data-ttu-id="ac6c5-125"><span id="Both"></span><span id="both"></span><span id="BOTH"></span>**Beides** (4)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-125"><span id="Both"></span><span id="both"></span><span id="BOTH"></span>**Both** (4)</span></span>


</dt> <dd>

<span data-ttu-id="ac6c5-126">Sowohl spezifische als auch allgemeine Anforderungen werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ac6c5-126">Both specific and general requests are supported.</span></span>

</dd> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="ac6c5-127"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-127"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="ac6c5-128"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Anbieter reserviert** (0X8000.. 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="ac6c5-128"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (0x8000..0xFFFF)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ac6c5-129">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="ac6c5-129">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac6c5-130">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ac6c5-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac6c5-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ac6c5-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac6c5-132">Eine Beschreibung eines Implementierungs spezifischen unter Typs für diese Ressource.</span><span class="sxs-lookup"><span data-stu-id="ac6c5-132">A description of an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="ac6c5-133">Dies kann z. b. verwendet werden, um unterschiedliche Modelle desselben Ressourcentyps zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="ac6c5-133">For example, this may be used to distinguish different models of the same resource type.</span></span>

</dd> <dt>

<span data-ttu-id="ac6c5-134">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="ac6c5-134">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac6c5-135">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ac6c5-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ac6c5-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ac6c5-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac6c5-137">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM-Zuweisung- \_ Funktionen**".**Otherresourcetype**","[**CIM \_ resourcezucationsettingdata**](cim-resourceallocationsettingdata.md).**ResourceType**")</span><span class="sxs-lookup"><span data-stu-id="ac6c5-137">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AllocationCapabilities**.**OtherResourceType**", "[**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md).**ResourceType**")</span></span>
</dt> </dl>

<span data-ttu-id="ac6c5-138">Der Typ der Ressource, die dieser Zuordnungs Einstellung zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="ac6c5-138">The type of resource that is assigned to this allocation setting.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ac6c5-139">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-139">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>

<span data-ttu-id="ac6c5-140">**Computer System** (2)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-140">**Computer System** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>

<span data-ttu-id="ac6c5-141">**Prozessor** (3)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-141">**Processor** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>

<span data-ttu-id="ac6c5-142">Arbeits **Speicher** (4)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-142">**Memory** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>

<span data-ttu-id="ac6c5-143">**IDE-Controller** (5)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-143">**IDE Controller** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>

<span data-ttu-id="ac6c5-144">**Paralleler SCSI-HBA** (6)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-144">**Parallel SCSI HBA** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_HBA"></span><span id="fc_hba"></span>

<span data-ttu-id="ac6c5-145">**FC-HBA** (7)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-145">**FC HBA** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>

<span data-ttu-id="ac6c5-146">**iSCSI-HBA** (8)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-146">**iSCSI HBA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="IB_HCA"></span><span id="ib_hca"></span>

<span data-ttu-id="ac6c5-147">**IB HCA** (9)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-147">**IB HCA** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>

<span data-ttu-id="ac6c5-148">**Ethernet-Adapter** (10)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-148">**Ethernet Adapter** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>

<span data-ttu-id="ac6c5-149">**Anderer Netzwerk Adapter** (11)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-149">**Other Network Adapter** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>

<span data-ttu-id="ac6c5-150">E **/a-Slot** (12)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-150">**I/O Slot** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>

<span data-ttu-id="ac6c5-151">E **/a-Gerät** (13)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-151">**I/O Device** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>

<span data-ttu-id="ac6c5-152">**Diskettenlaufwerk** (14)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-152">**Floppy Drive** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>

<span data-ttu-id="ac6c5-153">**CD-Laufwerk** (15)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-153">**CD Drive** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>

<span data-ttu-id="ac6c5-154">**DVD-Laufwerk** (16)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-154">**DVD drive** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

<span data-ttu-id="ac6c5-155">**Laufwerk (17** )</span><span class="sxs-lookup"><span data-stu-id="ac6c5-155">**Disk Drive** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>

<span data-ttu-id="ac6c5-156">**Bandlaufwerk** (18)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-156">**Tape Drive** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>

<span data-ttu-id="ac6c5-157">**Speicher** Block (19)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-157">**Storage Extent** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_Storage_Device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>

<span data-ttu-id="ac6c5-158">**Anderes Speichergerät** (20)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-158">**Other Storage Device** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>

<span data-ttu-id="ac6c5-159">**Seriellen Anschluss** (21)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-159">**Serial port** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>

<span data-ttu-id="ac6c5-160">**Paralleler Anschluss** (22)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-160">**Parallel port** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>

<span data-ttu-id="ac6c5-161">**USB-Controller** (23)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-161">**USB Controller** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>

<span data-ttu-id="ac6c5-162">**Grafikcontroller** (24)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-162">**Graphics controller** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>

<span data-ttu-id="ac6c5-163">**IEEE 1394-Controller** (25)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-163">**IEEE 1394 Controller** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>

<span data-ttu-id="ac6c5-164">**Partitionier Bare Einheit** (26)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-164">**Partitionable Unit** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>

<span data-ttu-id="ac6c5-165">**Partitionier bare Basiseinheit** (27)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-165">**Base Partitionable Unit** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="ac6c5-166">**Energie** (28)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-166">**Power** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>

<span data-ttu-id="ac6c5-167">**Kühlkapazität** (29)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-167">**Cooling Capacity** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>

<span data-ttu-id="ac6c5-168">**Ethernet-Switchport** (30)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-168">**Ethernet Switch Port** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>

<span data-ttu-id="ac6c5-169">**Logischer** Datenträger (31)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-169">**Logical Disk** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>

<span data-ttu-id="ac6c5-170">**Speicher Volume** (32)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-170">**Storage Volume** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>

<span data-ttu-id="ac6c5-171">**Ethernet-Verbindung** (33)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-171">**Ethernet Connection** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="ac6c5-172">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-172">**DMTF reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="ac6c5-173">**Anbieter reserviert** (0X8000.. 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="ac6c5-173">**Vendor Reserved** (0x8000..0xFFFF)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ac6c5-174">**Sharingmode**</span><span class="sxs-lookup"><span data-stu-id="ac6c5-174">**SharingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac6c5-175">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ac6c5-175">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ac6c5-176">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ac6c5-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac6c5-177">Gibt an, wie der Zugriff auf die zugrunde liegende Ressource gewährt wird.</span><span class="sxs-lookup"><span data-stu-id="ac6c5-177">Indicates how access to the underlying resource is granted.</span></span>

<span data-ttu-id="ac6c5-178">Die tatsächliche Menge wird durch min, maximale Größe, Gewichtungen usw. gesteuert.</span><span class="sxs-lookup"><span data-stu-id="ac6c5-178">Actual quantity is controlled by min, max size, weights, etc.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ac6c5-179"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-179"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="ac6c5-180"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dediziert** (2)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-180"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (2)</span></span>


</dt> <dd>

<span data-ttu-id="ac6c5-181">Exklusiver Zugriff auf die zugrunde liegende Ressource.</span><span class="sxs-lookup"><span data-stu-id="ac6c5-181">Exclusive access to underlying resource.</span></span>

</dd> <dt>

<span id="Shared"></span><span id="shared"></span><span id="SHARED"></span>

<span data-ttu-id="ac6c5-182"><span id="Shared"></span><span id="shared"></span><span id="SHARED"></span>Frei **gegeben** (3)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-182"><span id="Shared"></span><span id="shared"></span><span id="SHARED"></span>**Shared** (3)</span></span>


</dt> <dd>

<span data-ttu-id="ac6c5-183">Freigegebene Verwendung der zugrunde liegenden Ressource.</span><span class="sxs-lookup"><span data-stu-id="ac6c5-183">Shared use of underlying resource.</span></span>

</dd> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="ac6c5-184"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-184"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="ac6c5-185"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Anbieter reserviert** (0X8000.. 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="ac6c5-185"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (0x8000..0xFFFF)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ac6c5-186">**Supportedaddstates**</span><span class="sxs-lookup"><span data-stu-id="ac6c5-186">**SupportedAddStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac6c5-187">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="ac6c5-187">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ac6c5-188">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ac6c5-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac6c5-189">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ enabledlogicalelement**](cim-enabledlogicalelement.md)".**Enabledstate**")</span><span class="sxs-lookup"><span data-stu-id="ac6c5-189">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).**EnabledState**")</span></span>
</dt> </dl>

<span data-ttu-id="ac6c5-190">Der Systemstatus, der beim Erstellen einer neuen Ressource unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="ac6c5-190">The system states that are supported when a new resource is created.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ac6c5-191">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-191">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="ac6c5-192">**Aktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-192">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="ac6c5-193">**Deaktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-193">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>

<span data-ttu-id="ac6c5-194">**Herunter** fahren (4)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-194">**Shutting Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="ac6c5-195">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-195">**Not Applicable** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>

<span data-ttu-id="ac6c5-196">**Aktiviert, aber offline** (6)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-196">**Enabled but Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="ac6c5-197">**In Test** (7)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-197">**In Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>

<span data-ttu-id="ac6c5-198">Verzögert **(8** )</span><span class="sxs-lookup"><span data-stu-id="ac6c5-198">**Deferred** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="ac6c5-199">Still **legung (9** )</span><span class="sxs-lookup"><span data-stu-id="ac6c5-199">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="ac6c5-200">Wird **gestartet** (10)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-200">**Starting** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="ac6c5-201">**Angeh** alten (11)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-201">**Paused** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="ac6c5-202">Angeh **alten (12** )</span><span class="sxs-lookup"><span data-stu-id="ac6c5-202">**Suspended** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="ac6c5-203">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-203">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="ac6c5-204">**Anbieter reserviert** (0X8000.. 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="ac6c5-204">**Vendor Reserved** (0x8000..0xFFFF)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ac6c5-205">**Supportedremuvestates**</span><span class="sxs-lookup"><span data-stu-id="ac6c5-205">**SupportedRemoveStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac6c5-206">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="ac6c5-206">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ac6c5-207">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ac6c5-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac6c5-208">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ enabledlogicalelement**](cim-enabledlogicalelement.md)".**Enabledstate**")</span><span class="sxs-lookup"><span data-stu-id="ac6c5-208">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).**EnabledState**")</span></span>
</dt> </dl>

<span data-ttu-id="ac6c5-209">Der Systemstatus, der beim Entfernen einer Ressource unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="ac6c5-209">The system states that are supported when a resource is removed.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ac6c5-210">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-210">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="ac6c5-211">**Aktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-211">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="ac6c5-212">**Deaktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-212">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>

<span data-ttu-id="ac6c5-213">**Herunter** fahren (4)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-213">**Shutting Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="ac6c5-214">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-214">**Not Applicable** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>

<span data-ttu-id="ac6c5-215">**Aktiviert, aber offline** (6)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-215">**Enabled but Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="ac6c5-216">**In Test** (7)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-216">**In Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>

<span data-ttu-id="ac6c5-217">Verzögert **(8** )</span><span class="sxs-lookup"><span data-stu-id="ac6c5-217">**Deferred** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="ac6c5-218">Still **legung (9** )</span><span class="sxs-lookup"><span data-stu-id="ac6c5-218">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="ac6c5-219">Wird **gestartet** (10)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-219">**Starting** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="ac6c5-220">**Angeh** alten (11)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-220">**Paused** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="ac6c5-221">Angeh **alten (12** )</span><span class="sxs-lookup"><span data-stu-id="ac6c5-221">**Suspended** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="ac6c5-222">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-222">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="ac6c5-223">**Anbieter reserviert** (0X8000.. 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="ac6c5-223">**Vendor Reserved** (0x8000..0xFFFF)</span></span>


<span data-ttu-id="ac6c5-224"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="ac6c5-224"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="ac6c5-225">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ac6c5-225">Requirements</span></span>



| <span data-ttu-id="ac6c5-226">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ac6c5-226">Requirement</span></span> | <span data-ttu-id="ac6c5-227">Wert</span><span class="sxs-lookup"><span data-stu-id="ac6c5-227">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac6c5-228">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-228">Minimum supported client</span></span><br/> | <span data-ttu-id="ac6c5-229">Windows 8</span><span class="sxs-lookup"><span data-stu-id="ac6c5-229">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="ac6c5-230">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ac6c5-230">Minimum supported server</span></span><br/> | <span data-ttu-id="ac6c5-231">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ac6c5-231">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="ac6c5-232">Namespace</span><span class="sxs-lookup"><span data-stu-id="ac6c5-232">Namespace</span></span><br/>                | <span data-ttu-id="ac6c5-233">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="ac6c5-233">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ac6c5-234">MOF</span><span class="sxs-lookup"><span data-stu-id="ac6c5-234">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ac6c5-235"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ac6c5-235"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ac6c5-236">DLL</span><span class="sxs-lookup"><span data-stu-id="ac6c5-236">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac6c5-237"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ac6c5-237"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ac6c5-238">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ac6c5-238">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac6c5-239">**CIM- \_ Funktionen**</span><span class="sxs-lookup"><span data-stu-id="ac6c5-239">**CIM\_Capabilities**</span></span>](cim-capabilities.md)
</dt> </dl>

 

