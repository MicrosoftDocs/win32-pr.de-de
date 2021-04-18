---
description: Definiert eine Zuordnung eines Ressourcentyps zu seinen Implementierungsklassen.
ms.assetid: 0911454D-2494-49D5-8480-212E9ADD1B45
title: Msvm_ResourceTypeDefinition-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourceTypeDefinition
- Msvm_ResourceTypeDefinition.ResourceType
- Msvm_ResourceTypeDefinition.OtherResourceType
- Msvm_ResourceTypeDefinition.ResourceSubType
- Msvm_ResourceTypeDefinition.LogicalDeviceClassName
- Msvm_ResourceTypeDefinition.SettingDataClassName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: edfbf2ec9772fa710df5fc0d024abfcad6d826d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368046"
---
# <a name="msvm_resourcetypedefinition-class"></a><span data-ttu-id="ca2a7-103">MSVM \_ resourcetypeer Definition-Klasse</span><span class="sxs-lookup"><span data-stu-id="ca2a7-103">Msvm\_ResourceTypeDefinition class</span></span>

<span data-ttu-id="ca2a7-104">Definiert eine Zuordnung eines Ressourcentyps zu seinen Implementierungsklassen.</span><span class="sxs-lookup"><span data-stu-id="ca2a7-104">Defines a mapping of a resource type to its implementation classes.</span></span>

<span data-ttu-id="ca2a7-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="ca2a7-105">The following syntax is simplified Managed Object Format (MOF) code.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca2a7-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca2a7-106">Syntax</span></span>

``` syntax
class Msvm_ResourceTypeDefinition
{
  uint16 ResourceType;
  string OtherResourceType;
  string ResourceSubType;
  string LogicalDeviceClassName;
  string SettingDataClassName;
};
```

## <a name="members"></a><span data-ttu-id="ca2a7-107">Member</span><span class="sxs-lookup"><span data-stu-id="ca2a7-107">Members</span></span>

<span data-ttu-id="ca2a7-108">Die **MSVM \_ resourcetypeer Definition** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ca2a7-108">The **Msvm\_ResourceTypeDefinition** class has these types of members:</span></span>

-   [<span data-ttu-id="ca2a7-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ca2a7-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ca2a7-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ca2a7-110">Properties</span></span>

<span data-ttu-id="ca2a7-111">Die **MSVM \_ resourcetypeer Definition** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ca2a7-111">The **Msvm\_ResourceTypeDefinition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ca2a7-112">**Logicalenviceclassname**</span><span class="sxs-lookup"><span data-stu-id="ca2a7-112">**LogicalDeviceClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca2a7-113">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ca2a7-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca2a7-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ca2a7-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca2a7-115">Der Name der Klasse, die vom [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) abgeleitet wurde, das das logische Gerät für diesen Ressourcentyp implementiert.</span><span class="sxs-lookup"><span data-stu-id="ca2a7-115">The name of the class derived from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) that implements the logical device for this resource type.</span></span>

</dd> <dt>

<span data-ttu-id="ca2a7-116">**Otherresourcetype**</span><span class="sxs-lookup"><span data-stu-id="ca2a7-116">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca2a7-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ca2a7-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca2a7-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ca2a7-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca2a7-119">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="ca2a7-119">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="ca2a7-120">Eine Zeichenfolge, die den Ressourcentyp beschreibt, wenn ein klar definierter Wert nicht verfügbar ist und **ResourceType** den Wert 1 (sonstige) aufweist.</span><span class="sxs-lookup"><span data-stu-id="ca2a7-120">A string that describes the resource type when a well-defined value is not available and **ResourceType** has the value 1 (Other).</span></span> <span data-ttu-id="ca2a7-121">Es gibt eine Entsprechung zur **otherresourcetype** -Eigenschaft von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ca2a7-121">There is a correspondence with the **OtherResourceType** property of [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ca2a7-122">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="ca2a7-122">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca2a7-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ca2a7-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca2a7-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ca2a7-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca2a7-125">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="ca2a7-125">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="ca2a7-126">Eine Zeichenfolge, die einen Implementierungs spezifischen Untertyp für diese Ressource beschreibt.</span><span class="sxs-lookup"><span data-stu-id="ca2a7-126">A string that describes an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="ca2a7-127">Dies kann z. b. verwendet werden, um unterschiedliche Modelle desselben Ressourcentyps zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="ca2a7-127">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="ca2a7-128">Es gibt eine Entsprechung zur **resourcesubtype** -Eigenschaft von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ca2a7-128">There is a correspondence with the **ResourceSubType** property of [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ca2a7-129">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="ca2a7-129">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca2a7-130">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ca2a7-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ca2a7-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ca2a7-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca2a7-132">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="ca2a7-132">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="ca2a7-133">Der Typ der Ressource, die diese Zuordnungs Einstellung darstellt.</span><span class="sxs-lookup"><span data-stu-id="ca2a7-133">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="ca2a7-134">Es gibt eine Entsprechung zur **ResourceType** -Eigenschaft von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ca2a7-134">There is a correspondence with the **ResourceType** property of [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<dl> <dt>

<span data-ttu-id="ca2a7-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="ca2a7-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ca2a7-136"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span><span class="sxs-lookup"><span data-stu-id="ca2a7-136"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ca2a7-137"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Prozessor** (3)</span><span class="sxs-lookup"><span data-stu-id="ca2a7-137"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processor** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ca2a7-138"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>Arbeits **Speicher** (4)</span><span class="sxs-lookup"><span data-stu-id="ca2a7-138"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memory** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ca2a7-139"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE-Controller** (5)</span><span class="sxs-lookup"><span data-stu-id="ca2a7-139"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE Controller** (5)</span></span>
</dt> <dt>

<span data-ttu-id="ca2a7-140"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Paralleler SCSI-HBA** (6)</span><span class="sxs-lookup"><span data-stu-id="ca2a7-140"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Parallel SCSI HBA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="ca2a7-141"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC-HBA** (7)</span><span class="sxs-lookup"><span data-stu-id="ca2a7-141"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7)</span></span>
</dt> <dt>

<span data-ttu-id="ca2a7-142"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**iSCSI-HBA** (8)</span><span class="sxs-lookup"><span data-stu-id="ca2a7-142"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**iSCSI HBA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="ca2a7-143"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span><span class="sxs-lookup"><span data-stu-id="ca2a7-143"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="ca2a7-144"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet-Adapter** (10)</span><span class="sxs-lookup"><span data-stu-id="ca2a7-144"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet Adapter** (10)</span></span>
</dt> <dt>

<span data-ttu-id="ca2a7-145"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Anderer Netzwerk Adapter** (11)</span><span class="sxs-lookup"><span data-stu-id="ca2a7-145"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Other Network Adapter** (11)</span></span>
</dt> <dt>

<span data-ttu-id="ca2a7-146"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>E **/a-Slot** (12)</span><span class="sxs-lookup"><span data-stu-id="ca2a7-146"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**I/O Slot** (12)</span></span>
</dt> <dt>

<span data-ttu-id="ca2a7-147"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>E **/a-Gerät** (13)</span><span class="sxs-lookup"><span data-stu-id="ca2a7-147"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**I/O Device** (13)</span></span>
</dt> <dt>

<span data-ttu-id="ca2a7-148"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Diskettenlaufwerk** (14)</span><span class="sxs-lookup"><span data-stu-id="ca2a7-148"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Floppy Drive** (14)</span></span>
</dt> <dt>

<span data-ttu-id="ca2a7-149"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD-Laufwerk** (15)</span><span class="sxs-lookup"><span data-stu-id="ca2a7-149"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD Drive** (15)</span></span>
</dt> <dt>

<span data-ttu-id="ca2a7-150"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD-Laufwerk** (16)</span><span class="sxs-lookup"><span data-stu-id="ca2a7-150"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD drive** (16)</span></span>
</dt> <dt>

<span data-ttu-id="ca2a7-151"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Seriellen Anschluss** (17)</span><span class="sxs-lookup"><span data-stu-id="ca2a7-151"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Serial port** (17)</span></span>
</dt> <dt>

<span data-ttu-id="ca2a7-152"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Paralleler Anschluss** (18)</span><span class="sxs-lookup"><span data-stu-id="ca2a7-152"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Parallel port** (18)</span></span>
</dt> <dt>

<span data-ttu-id="ca2a7-153"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB-Controller** (19)</span><span class="sxs-lookup"><span data-stu-id="ca2a7-153"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB Controller** (19)</span></span>
</dt> <dt>

<span data-ttu-id="ca2a7-154"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Grafikcontroller** (20)</span><span class="sxs-lookup"><span data-stu-id="ca2a7-154"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Graphics controller** (20)</span></span>
</dt> <dt>

<span data-ttu-id="ca2a7-155"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Speicher** Block (21)</span><span class="sxs-lookup"><span data-stu-id="ca2a7-155"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Storage Extent** (21)</span></span>
</dt> <dt>

<span data-ttu-id="ca2a7-156"><span id="Disk"></span><span id="disk"></span><span id="DISK"></span>Daten **Träger (22** )</span><span class="sxs-lookup"><span data-stu-id="ca2a7-156"><span id="Disk"></span><span id="disk"></span><span id="DISK"></span>**Disk** (22)</span></span>
</dt> <dt>

<span data-ttu-id="ca2a7-157"><span id="Tape"></span><span id="tape"></span><span id="TAPE"></span>**Band** (23)</span><span class="sxs-lookup"><span data-stu-id="ca2a7-157"><span id="Tape"></span><span id="tape"></span><span id="TAPE"></span>**Tape** (23)</span></span>
</dt> <dt>

<span data-ttu-id="ca2a7-158"><span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Anderes Speichergerät** (24)</span><span class="sxs-lookup"><span data-stu-id="ca2a7-158"><span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Other storage device** (24)</span></span>
</dt> <dt>

<span data-ttu-id="ca2a7-159"><span id="Firewire_Controller"></span><span id="firewire_controller"></span><span id="FIREWIRE_CONTROLLER"></span>**Firewire-Controller** (25)</span><span class="sxs-lookup"><span data-stu-id="ca2a7-159"><span id="Firewire_Controller"></span><span id="firewire_controller"></span><span id="FIREWIRE_CONTROLLER"></span>**Firewire Controller** (25)</span></span>
</dt> <dt>

<span data-ttu-id="ca2a7-160"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Partitionier Bare Einheit** (26)</span><span class="sxs-lookup"><span data-stu-id="ca2a7-160"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Partitionable Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="ca2a7-161"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Partitionier bare Basiseinheit** (27)</span><span class="sxs-lookup"><span data-stu-id="ca2a7-161"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Base Partitionable Unit** (27)</span></span>
</dt> <dt>

<span data-ttu-id="ca2a7-162"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Netzteil** (28)</span><span class="sxs-lookup"><span data-stu-id="ca2a7-162"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Power Supply** (28)</span></span>
</dt> <dt>

<span data-ttu-id="ca2a7-163"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Kühl Gerät** (29)</span><span class="sxs-lookup"><span data-stu-id="ca2a7-163"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Cooling Device** (29)</span></span>
</dt> <dt>

<span data-ttu-id="ca2a7-164"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (30 32767)</span><span class="sxs-lookup"><span data-stu-id="ca2a7-164"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (30 32767)</span></span>
</dt> <dt>

<span data-ttu-id="ca2a7-165"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Anbieter reserviert** (32768 65535)</span><span class="sxs-lookup"><span data-stu-id="ca2a7-165"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768 65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ca2a7-166">**Settingdataclassname**</span><span class="sxs-lookup"><span data-stu-id="ca2a7-166">**SettingDataClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca2a7-167">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ca2a7-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca2a7-168">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ca2a7-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca2a7-169">Der Name der Klasse, die aus [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) abgeleitet ist und die Einstellungen für diesen Ressourcentyp implementiert.</span><span class="sxs-lookup"><span data-stu-id="ca2a7-169">The name of the class derived from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) that implements the settings for this resource type.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ca2a7-170">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ca2a7-170">Remarks</span></span>

<span data-ttu-id="ca2a7-171">Der Zugriff auf die **MSVM \_ resourcetypeer Definition** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="ca2a7-171">Access to the **Msvm\_ResourceTypeDefinition** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="ca2a7-172">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="ca2a7-172">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="ca2a7-173">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ca2a7-173">Requirements</span></span>



| <span data-ttu-id="ca2a7-174">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ca2a7-174">Requirement</span></span> | <span data-ttu-id="ca2a7-175">Wert</span><span class="sxs-lookup"><span data-stu-id="ca2a7-175">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca2a7-176">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ca2a7-176">Minimum supported client</span></span><br/> | <span data-ttu-id="ca2a7-177">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ca2a7-177">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ca2a7-178">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ca2a7-178">Minimum supported server</span></span><br/> | <span data-ttu-id="ca2a7-179">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ca2a7-179">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ca2a7-180">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="ca2a7-180">End of client support</span></span><br/>    | <span data-ttu-id="ca2a7-181">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="ca2a7-181">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="ca2a7-182">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="ca2a7-182">End of server support</span></span><br/>    | <span data-ttu-id="ca2a7-183">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="ca2a7-183">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="ca2a7-184">Namespace</span><span class="sxs-lookup"><span data-stu-id="ca2a7-184">Namespace</span></span><br/>                | <span data-ttu-id="ca2a7-185">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="ca2a7-185">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ca2a7-186">MOF</span><span class="sxs-lookup"><span data-stu-id="ca2a7-186">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ca2a7-187"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ca2a7-187"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ca2a7-188">DLL</span><span class="sxs-lookup"><span data-stu-id="ca2a7-188">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca2a7-189"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ca2a7-189"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

