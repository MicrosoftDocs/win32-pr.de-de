---
description: Die CIM \_ Diskpartition-Klasse stellt einen zusammenhängenden Bereich logischer Blöcke dar, der vom Betriebssystem mithilfe der Felder Typ und Untertyp der Partition identifiziert werden kann.
ms.assetid: 22a0e5be-c66b-40a2-9a7a-047d2edc0278
ms.tgt_platform: multiple
title: CIM_DiskPartition-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DiskPartition
- CIM_DiskPartition.Access
- CIM_DiskPartition.Availability
- CIM_DiskPartition.BlockSize
- CIM_DiskPartition.Bootable
- CIM_DiskPartition.Caption
- CIM_DiskPartition.ConfigManagerErrorCode
- CIM_DiskPartition.ConfigManagerUserConfig
- CIM_DiskPartition.CreationClassName
- CIM_DiskPartition.Description
- CIM_DiskPartition.DeviceID
- CIM_DiskPartition.ErrorCleared
- CIM_DiskPartition.ErrorDescription
- CIM_DiskPartition.ErrorMethodology
- CIM_DiskPartition.InstallDate
- CIM_DiskPartition.LastErrorCode
- CIM_DiskPartition.Name
- CIM_DiskPartition.NumberOfBlocks
- CIM_DiskPartition.PNPDeviceID
- CIM_DiskPartition.PowerManagementCapabilities
- CIM_DiskPartition.PowerManagementSupported
- CIM_DiskPartition.PrimaryPartition
- CIM_DiskPartition.Purpose
- CIM_DiskPartition.Status
- CIM_DiskPartition.StatusInfo
- CIM_DiskPartition.SystemCreationClassName
- CIM_DiskPartition.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d1761e140813c26e67594872df5a8d2f7361768b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861396"
---
# <a name="cim_diskpartition-class"></a><span data-ttu-id="e706a-103">CIM \_ Diskpartition-Klasse</span><span class="sxs-lookup"><span data-stu-id="e706a-103">CIM\_DiskPartition class</span></span>

<span data-ttu-id="e706a-104">Die **CIM \_ Diskpartition** -Klasse stellt einen zusammenhängenden Bereich logischer Blöcke dar, der vom Betriebssystem mithilfe der Felder Typ und Untertyp der Partition identifiziert werden kann.</span><span class="sxs-lookup"><span data-stu-id="e706a-104">The **CIM\_DiskPartition** class represents a contiguous range of logical blocks that is identifiable by the operating system by way of the partition's type and subtype fields.</span></span> <span data-ttu-id="e706a-105">Datenträger Partitionen sollten direkt durch physische Medien (angegeben durch die [**CIM- \_**](cim-realizesdiskpartition.md) Neuzuordnung) oder auf Speichervolumes erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="e706a-105">Disk partitions should be directly realized by physical media (indicated by the [**CIM\_RealizesDiskPartition**](cim-realizesdiskpartition.md) association) or built on storage volumes.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e706a-106">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="e706a-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e706a-107">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e706a-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e706a-108">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="e706a-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="e706a-109">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="e706a-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e706a-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="e706a-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C541-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_DiskPartition : CIM_StorageExtent
{
  uint16   Access;
  uint16   Availability;
  uint64   BlockSize;
  boolean  Bootable;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  uint64   NumberOfBlocks;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  boolean  PrimaryPartition;
  string   Purpose;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="e706a-111">Member</span><span class="sxs-lookup"><span data-stu-id="e706a-111">Members</span></span>

<span data-ttu-id="e706a-112">Die **CIM \_ Diskpartition** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e706a-112">The **CIM\_DiskPartition** class has these types of members:</span></span>

-   [<span data-ttu-id="e706a-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="e706a-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="e706a-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e706a-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e706a-115">Methoden</span><span class="sxs-lookup"><span data-stu-id="e706a-115">Methods</span></span>

<span data-ttu-id="e706a-116">Die **CIM \_ Diskpartition** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="e706a-116">The **CIM\_DiskPartition** class has these methods.</span></span>



| <span data-ttu-id="e706a-117">Methode</span><span class="sxs-lookup"><span data-stu-id="e706a-117">Method</span></span>                                                                   | <span data-ttu-id="e706a-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e706a-118">Description</span></span>                                                                                                                              |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e706a-119">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="e706a-119">**Reset**</span></span>](reset-method-in-class-cim-diskpartition.md)                 | <span data-ttu-id="e706a-120">Fordert eine zurück setzung des logischen Geräts an.</span><span class="sxs-lookup"><span data-stu-id="e706a-120">Requests a reset of the logical device.</span></span> <span data-ttu-id="e706a-121">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="e706a-121">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="e706a-122">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="e706a-122">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-diskpartition.md) | <span data-ttu-id="e706a-123">Definiert den gewünschten Energiezustand für ein logisches Gerät und einen Zeitpunkt, zu dem ein Gerät in diesen Zustand versetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e706a-123">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="e706a-124">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="e706a-124">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="e706a-125">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e706a-125">Properties</span></span>

<span data-ttu-id="e706a-126">Die **CIM \_ Diskpartition** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e706a-126">The **CIM\_DiskPartition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e706a-127">**zugreifen**</span><span class="sxs-lookup"><span data-stu-id="e706a-127">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e706a-128">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e706a-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e706a-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e706a-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e706a-130">Gibt an, ob die Medien lesbar, beschreibbar oder beides sind, z. b..</span><span class="sxs-lookup"><span data-stu-id="e706a-130">Specifies whether the media is readable, writeable, or both, for example.</span></span> <span data-ttu-id="e706a-131">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e706a-131">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e706a-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="e706a-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="e706a-133">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="e706a-133">Unknown.</span></span>

</dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="e706a-134"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Lesbar** (1)</span><span class="sxs-lookup"><span data-stu-id="e706a-134"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Readable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="e706a-135">Lesbare.</span><span class="sxs-lookup"><span data-stu-id="e706a-135">Readable.</span></span>

</dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="e706a-136"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Beschreibbar** (2)</span><span class="sxs-lookup"><span data-stu-id="e706a-136"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Writeable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="e706a-137">Beschreibbaren.</span><span class="sxs-lookup"><span data-stu-id="e706a-137">Writeable.</span></span>

</dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="e706a-138"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Lese-/Schreibzugriff unterstützt** (3)</span><span class="sxs-lookup"><span data-stu-id="e706a-138"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Read/Write Supported** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e706a-139">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="e706a-139">Read/write supported.</span></span>

</dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="e706a-140"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Einmal schreiben** (4)</span><span class="sxs-lookup"><span data-stu-id="e706a-140"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Write Once** (4)</span></span>


</dt> <dd>

<span data-ttu-id="e706a-141">Einmal schreiben.</span><span class="sxs-lookup"><span data-stu-id="e706a-141">Write once.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e706a-142">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="e706a-142">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e706a-143">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e706a-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e706a-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e706a-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e706a-145">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="e706a-145">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="e706a-146">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="e706a-146">Availability and status of the device.</span></span>

<span data-ttu-id="e706a-147">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e706a-147">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e706a-148"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="e706a-148"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e706a-149"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="e706a-149"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="e706a-150"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="e706a-150"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="e706a-151"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="e706a-151"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="e706a-152"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="e706a-152"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="e706a-153"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="e706a-153"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="e706a-154"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="e706a-154"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="e706a-155"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="e706a-155"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="e706a-156"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="e706a-156"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="e706a-157"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="e706a-157"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="e706a-158"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="e706a-158"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="e706a-159"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="e706a-159"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="e706a-160"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="e706a-160"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="e706a-161">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="e706a-161">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="e706a-162"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="e706a-162"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="e706a-163">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="e706a-163">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="e706a-164"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="e706a-164"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="e706a-165">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb versetzt werden.</span><span class="sxs-lookup"><span data-stu-id="e706a-165">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="e706a-166"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="e706a-166"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="e706a-167"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="e706a-167"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="e706a-168">Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="e706a-168">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="e706a-169"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="e706a-169"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="e706a-170">Das Gerät wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="e706a-170">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="e706a-171"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="e706a-171"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="e706a-172">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="e706a-172">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="e706a-173"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="e706a-173"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="e706a-174">Das Gerät ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="e706a-174">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="e706a-175"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="e706a-175"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="e706a-176">Das Gerät ist in Ruhe.</span><span class="sxs-lookup"><span data-stu-id="e706a-176">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e706a-177">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="e706a-177">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e706a-178">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e706a-178">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e706a-179">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e706a-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e706a-180">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. hrstorageallocationunits "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Bytes ")</span><span class="sxs-lookup"><span data-stu-id="e706a-180">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="e706a-181">Größe (in Bytes) der Blöcke, die den Speicherblock bilden.</span><span class="sxs-lookup"><span data-stu-id="e706a-181">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="e706a-182">Wenn es sich um eine Variable Blockgröße handelt, muss die maximale Blockgröße in Bytes angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e706a-182">If it is a variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="e706a-183">Wenn die Blockgröße unbekannt ist oder ein Block Konzept nicht gültig ist (z. b. für Aggregat Blöcke, Arbeitsspeicher oder logische Datenträger), geben Sie den Wert 1 ein.</span><span class="sxs-lookup"><span data-stu-id="e706a-183">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter the value 1.</span></span>

<span data-ttu-id="e706a-184">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e706a-184">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="e706a-185">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="e706a-185">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="e706a-186">**Startbare**</span><span class="sxs-lookup"><span data-stu-id="e706a-186">**Bootable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e706a-187">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="e706a-187">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e706a-188">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e706a-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e706a-189">Wenn der Wert **true** ist, wird die Datenträger Partition als Start fähige Bezeichnung bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="e706a-189">If **TRUE**, the disk partition is labeled as bootable.</span></span> <span data-ttu-id="e706a-190">Dies bedeutet nicht, dass ein Betriebssystem auf der Partition geladen wird.</span><span class="sxs-lookup"><span data-stu-id="e706a-190">This does not mean that an operating system is loaded on the partition.</span></span>

</dd> <dt>

<span data-ttu-id="e706a-191">**Caption**</span><span class="sxs-lookup"><span data-stu-id="e706a-191">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e706a-192">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e706a-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e706a-193">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e706a-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e706a-194">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="e706a-194">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="e706a-195">Kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="e706a-195">Short textual description of the object.</span></span>

<span data-ttu-id="e706a-196">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e706a-196">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e706a-197">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="e706a-197">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e706a-198">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e706a-198">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e706a-199">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e706a-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e706a-200">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="e706a-200">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="e706a-201">Windows Configuration Manager-Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="e706a-201">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="e706a-202">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e706a-202">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="e706a-203"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="e706a-203"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="e706a-204"> (0)</span><span class="sxs-lookup"><span data-stu-id="e706a-204">(0)</span></span>


</dt> <dd>

<span data-ttu-id="e706a-205">Das Gerät funktioniert ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="e706a-205">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="e706a-206"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="e706a-206"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="e706a-207">(1)</span><span class="sxs-lookup"><span data-stu-id="e706a-207">(1)</span></span>


</dt> <dd>

<span data-ttu-id="e706a-208">Das Gerät ist nicht ordnungsgemäß konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="e706a-208">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="e706a-209"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="e706a-209"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="e706a-210">(2)</span><span class="sxs-lookup"><span data-stu-id="e706a-210">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="e706a-211"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="e706a-211"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="e706a-212">(3)</span><span class="sxs-lookup"><span data-stu-id="e706a-212">(3)</span></span>


</dt> <dd>

<span data-ttu-id="e706a-213">Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt möglicherweise nicht über genügend Arbeitsspeicher oder andere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="e706a-213">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="e706a-214"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="e706a-214"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="e706a-215">(4)</span><span class="sxs-lookup"><span data-stu-id="e706a-215">(4)</span></span>


</dt> <dd>

<span data-ttu-id="e706a-216">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="e706a-216">Device is not working properly.</span></span> <span data-ttu-id="e706a-217">Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="e706a-217">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="e706a-218"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="e706a-218"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="e706a-219">(5)</span><span class="sxs-lookup"><span data-stu-id="e706a-219">(5)</span></span>


</dt> <dd>

<span data-ttu-id="e706a-220">Der Treiber für das Gerät erfordert eine Ressource, die von Windows nicht verwaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="e706a-220">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="e706a-221"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="e706a-221"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="e706a-222"> (6)</span><span class="sxs-lookup"><span data-stu-id="e706a-222">(6)</span></span>


</dt> <dd>

<span data-ttu-id="e706a-223">Die Startkonfiguration für das Gerät steht in Konflikt mit anderen Geräten.</span><span class="sxs-lookup"><span data-stu-id="e706a-223">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="e706a-224"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="e706a-224"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="e706a-225">(7)</span><span class="sxs-lookup"><span data-stu-id="e706a-225">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="e706a-226"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="e706a-226"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="e706a-227">(8)</span><span class="sxs-lookup"><span data-stu-id="e706a-227">(8)</span></span>


</dt> <dd>

<span data-ttu-id="e706a-228">Das Treiber Lade Modul für das Gerät fehlt.</span><span class="sxs-lookup"><span data-stu-id="e706a-228">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="e706a-229"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="e706a-229"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="e706a-230">(9)</span><span class="sxs-lookup"><span data-stu-id="e706a-230">(9)</span></span>


</dt> <dd>

<span data-ttu-id="e706a-231">Das Gerät funktioniert nicht ordnungsgemäß. die Steuerungs Firmware meldet nicht korrekt die Ressourcen für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="e706a-231">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="e706a-232"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="e706a-232"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="e706a-233">(10)</span><span class="sxs-lookup"><span data-stu-id="e706a-233">(10)</span></span>


</dt> <dd>

<span data-ttu-id="e706a-234">Das Gerät kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="e706a-234">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="e706a-235"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="e706a-235"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="e706a-236">(11)</span><span class="sxs-lookup"><span data-stu-id="e706a-236">(11)</span></span>


</dt> <dd>

<span data-ttu-id="e706a-237">Fehler beim Gerät.</span><span class="sxs-lookup"><span data-stu-id="e706a-237">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="e706a-238"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="e706a-238"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="e706a-239">(12)</span><span class="sxs-lookup"><span data-stu-id="e706a-239">(12)</span></span>


</dt> <dd>

<span data-ttu-id="e706a-240">Das Gerät kann nicht genug freie Ressourcen für die Verwendung finden.</span><span class="sxs-lookup"><span data-stu-id="e706a-240">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="e706a-241"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="e706a-241"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="e706a-242">(13)</span><span class="sxs-lookup"><span data-stu-id="e706a-242">(13)</span></span>


</dt> <dd>

<span data-ttu-id="e706a-243">Die Geräte Ressourcen können nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="e706a-243">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="e706a-244"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="e706a-244"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="e706a-245">(14)</span><span class="sxs-lookup"><span data-stu-id="e706a-245">(14)</span></span>


</dt> <dd>

<span data-ttu-id="e706a-246">Das Gerät kann erst ordnungsgemäß funktionieren, wenn der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="e706a-246">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="e706a-247"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="e706a-247"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="e706a-248">(15)</span><span class="sxs-lookup"><span data-stu-id="e706a-248">(15)</span></span>


</dt> <dd>

<span data-ttu-id="e706a-249">Das Gerät funktioniert aufgrund eines möglichen erneuten Aufzählungs Problems nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="e706a-249">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="e706a-250"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="e706a-250"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="e706a-251">(16)</span><span class="sxs-lookup"><span data-stu-id="e706a-251">(16)</span></span>


</dt> <dd>

<span data-ttu-id="e706a-252">In Windows können nicht alle Ressourcen identifiziert werden, die vom Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e706a-252">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="e706a-253"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="e706a-253"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="e706a-254">(17)</span><span class="sxs-lookup"><span data-stu-id="e706a-254">(17)</span></span>


</dt> <dd>

<span data-ttu-id="e706a-255">Das Gerät fordert einen unbekannten Ressourcentyp an.</span><span class="sxs-lookup"><span data-stu-id="e706a-255">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="e706a-256"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="e706a-256"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="e706a-257">(18)</span><span class="sxs-lookup"><span data-stu-id="e706a-257">(18)</span></span>


</dt> <dd>

<span data-ttu-id="e706a-258">Gerätetreiber müssen neu installiert werden.</span><span class="sxs-lookup"><span data-stu-id="e706a-258">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="e706a-259"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="e706a-259"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="e706a-260">(19)</span><span class="sxs-lookup"><span data-stu-id="e706a-260">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="e706a-261"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="e706a-261"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="e706a-262">(20)</span><span class="sxs-lookup"><span data-stu-id="e706a-262">(20)</span></span>


</dt> <dd>

<span data-ttu-id="e706a-263">Die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="e706a-263">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="e706a-264"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="e706a-264"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="e706a-265">(21)</span><span class="sxs-lookup"><span data-stu-id="e706a-265">(21)</span></span>


</dt> <dd>

<span data-ttu-id="e706a-266">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="e706a-266">System failure.</span></span> <span data-ttu-id="e706a-267">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="e706a-267">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="e706a-268">Das Gerät wird von Windows entfernt.</span><span class="sxs-lookup"><span data-stu-id="e706a-268">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="e706a-269"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="e706a-269"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="e706a-270">(22)</span><span class="sxs-lookup"><span data-stu-id="e706a-270">(22)</span></span>


</dt> <dd>

<span data-ttu-id="e706a-271">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="e706a-271">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="e706a-272"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="e706a-272"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="e706a-273">(23)</span><span class="sxs-lookup"><span data-stu-id="e706a-273">(23)</span></span>


</dt> <dd>

<span data-ttu-id="e706a-274">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="e706a-274">System failure.</span></span> <span data-ttu-id="e706a-275">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="e706a-275">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="e706a-276"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="e706a-276"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="e706a-277">(24)</span><span class="sxs-lookup"><span data-stu-id="e706a-277">(24)</span></span>


</dt> <dd>

<span data-ttu-id="e706a-278">Das Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.</span><span class="sxs-lookup"><span data-stu-id="e706a-278">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="e706a-279"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="e706a-279"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="e706a-280">(25)</span><span class="sxs-lookup"><span data-stu-id="e706a-280">(25)</span></span>


</dt> <dd>

<span data-ttu-id="e706a-281">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="e706a-281">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="e706a-282"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="e706a-282"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="e706a-283">(26)</span><span class="sxs-lookup"><span data-stu-id="e706a-283">(26)</span></span>


</dt> <dd>

<span data-ttu-id="e706a-284">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="e706a-284">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="e706a-285"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="e706a-285"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="e706a-286">(27)</span><span class="sxs-lookup"><span data-stu-id="e706a-286">(27)</span></span>


</dt> <dd>

<span data-ttu-id="e706a-287">Das Gerät verfügt nicht über eine gültige Protokoll Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="e706a-287">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="e706a-288"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="e706a-288"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="e706a-289">(28)</span><span class="sxs-lookup"><span data-stu-id="e706a-289">(28)</span></span>


</dt> <dd>

<span data-ttu-id="e706a-290">Gerätetreiber sind nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="e706a-290">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="e706a-291"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="e706a-291"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="e706a-292">(29)</span><span class="sxs-lookup"><span data-stu-id="e706a-292">(29)</span></span>


</dt> <dd>

<span data-ttu-id="e706a-293">Das Gerät ist deaktiviert. die Gerätefirmware hat nicht die erforderlichen Ressourcen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="e706a-293">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="e706a-294"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="e706a-294"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="e706a-295">(30)</span><span class="sxs-lookup"><span data-stu-id="e706a-295">(30)</span></span>


</dt> <dd>

<span data-ttu-id="e706a-296">Das Gerät verwendet eine UNQ-Ressource, die von einem anderen Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e706a-296">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="e706a-297"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="e706a-297"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="e706a-298">31,5</span><span class="sxs-lookup"><span data-stu-id="e706a-298">(31)</span></span>


</dt> <dd>

<span data-ttu-id="e706a-299">Das Gerät funktioniert nicht ordnungsgemäß. Die erforderlichen Gerätetreiber können nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="e706a-299">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e706a-300">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="e706a-300">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e706a-301">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="e706a-301">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e706a-302">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e706a-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e706a-303">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="e706a-303">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="e706a-304">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="e706a-304">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="e706a-305">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e706a-305">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e706a-306">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="e706a-306">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e706a-307">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e706a-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e706a-308">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e706a-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e706a-309">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e706a-309">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e706a-310">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e706a-310">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="e706a-311">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="e706a-311">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="e706a-312">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e706a-312">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e706a-313">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e706a-313">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e706a-314">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e706a-314">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e706a-315">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e706a-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e706a-316">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="e706a-316">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="e706a-317">Die Textbeschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="e706a-317">Textual description of the object.</span></span>

<span data-ttu-id="e706a-318">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e706a-318">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e706a-319">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="e706a-319">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e706a-320">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e706a-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e706a-321">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e706a-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e706a-322">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e706a-322">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e706a-323">Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.</span><span class="sxs-lookup"><span data-stu-id="e706a-323">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="e706a-324">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e706a-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e706a-325">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="e706a-325">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e706a-326">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="e706a-326">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e706a-327">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e706a-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e706a-328">Wenn der Wert **true** ist, wird der in der Eigenschaft **LastErrorCode** gemeldete Fehler nun gelöscht.</span><span class="sxs-lookup"><span data-stu-id="e706a-328">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="e706a-329">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e706a-329">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e706a-330">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="e706a-330">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e706a-331">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e706a-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e706a-332">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e706a-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e706a-333">Eine frei Form Zeichenfolge, die weitere Informationen über den Fehler bereitstellt, der in der **LastErrorCode** -Eigenschaft aufgezeichnet wurde, sowie die auszuführenden Maßnahmen.</span><span class="sxs-lookup"><span data-stu-id="e706a-333">Free-form string that supplies more information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="e706a-334">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e706a-334">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e706a-335">**Errormethodmethodologie**</span><span class="sxs-lookup"><span data-stu-id="e706a-335">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e706a-336">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e706a-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e706a-337">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e706a-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e706a-338">Eine frei Form Zeichenfolge, die den Typ der Fehlererkennung und-Korrektur beschreibt, der vom Speicherblock unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="e706a-338">Free-form string that describes the type of error detection and correction supported by the storage extent.</span></span>

<span data-ttu-id="e706a-339">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e706a-339">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="e706a-340">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e706a-340">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e706a-341">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="e706a-341">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e706a-342">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e706a-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e706a-343">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="e706a-343">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="e706a-344">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="e706a-344">Date and time the object was installed.</span></span> <span data-ttu-id="e706a-345">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="e706a-345">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="e706a-346">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e706a-346">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e706a-347">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="e706a-347">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e706a-348">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e706a-348">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e706a-349">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e706a-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e706a-350">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="e706a-350">Last error code reported by the logical device.</span></span>

<span data-ttu-id="e706a-351">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e706a-351">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e706a-352">**Name**</span><span class="sxs-lookup"><span data-stu-id="e706a-352">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e706a-353">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e706a-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e706a-354">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e706a-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e706a-355">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="e706a-355">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="e706a-356">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="e706a-356">Label by which the object is known.</span></span> <span data-ttu-id="e706a-357">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="e706a-357">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="e706a-358">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e706a-358">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e706a-359">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="e706a-359">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e706a-360">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e706a-360">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e706a-361">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e706a-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e706a-362">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. hrstoragesize ")</span><span class="sxs-lookup"><span data-stu-id="e706a-362">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="e706a-363">Anzahl der aufeinanderfolgenden Blöcke, die jeweils die Größe des in der **BLOCKSIZE** -Eigenschaft enthaltenen Werts blockieren, der den Speicherblock bildet.</span><span class="sxs-lookup"><span data-stu-id="e706a-363">Number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which forms the storage extent.</span></span> <span data-ttu-id="e706a-364">Die Gesamtgröße des Speicherbereichs kann berechnet werden, indem der Wert der **BLOCKSIZE** -Eigenschaft mit dem Wert dieser Eigenschaft multipliziert wird.</span><span class="sxs-lookup"><span data-stu-id="e706a-364">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="e706a-365">Wenn der Wert von **BLOCKSIZE** 1 ist, entspricht diese Eigenschaft der Gesamtgröße des Speicherblocks.</span><span class="sxs-lookup"><span data-stu-id="e706a-365">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="e706a-366">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e706a-366">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="e706a-367">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="e706a-367">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="e706a-368">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="e706a-368">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e706a-369">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e706a-369">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e706a-370">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e706a-370">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e706a-371">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="e706a-371">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="e706a-372">Win32-Plug & Play Geräte Bezeichner des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="e706a-372">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="e706a-373">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e706a-373">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="e706a-374">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="e706a-374">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="e706a-375">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="e706a-375">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e706a-376">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="e706a-376">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e706a-377">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e706a-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e706a-378">Array der spezifischen energiebezogenen Funktionen eines logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="e706a-378">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="e706a-379">Diese Eigenschaft wird von **CIM \_ LogicalDevice** geerbt.</span><span class="sxs-lookup"><span data-stu-id="e706a-379">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e706a-380"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="e706a-380"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="e706a-381"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="e706a-381"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="e706a-382"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="e706a-382"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="e706a-383"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="e706a-383"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e706a-384">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e706a-384">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="e706a-385"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="e706a-385"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="e706a-386">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="e706a-386">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="e706a-387"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="e706a-387"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="e706a-388">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e706a-388">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="e706a-389">Diese Methode wird in der übergeordneten **CIM \_ LogicalDevice** -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="e706a-389">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="e706a-390">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="e706a-390">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="e706a-391"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="e706a-391"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="e706a-392">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e706a-392">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="e706a-393"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="e706a-393"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="e706a-394">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) und die *Uhrzeit* auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e706a-394">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e706a-395">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="e706a-395">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e706a-396">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="e706a-396">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e706a-397">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e706a-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e706a-398">**True** gibt an, dass das Gerät Energie verwaltet werden kann, d. h. in einen Energiespar Status versetzt wird.</span><span class="sxs-lookup"><span data-stu-id="e706a-398">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="e706a-399">Wenn **false**, sollte der ganzzahlige Wert 1 ("nicht unterstützt") der einzige Eintrag im **powermanagementfunktionalitäten** -Array sein.</span><span class="sxs-lookup"><span data-stu-id="e706a-399">If **False**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="e706a-400">Diese Eigenschaft gibt nicht an, ob die Energie Verwaltungsfunktionen derzeit aktiviert sind oder ob Sie aktiviert sind, welche Features unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="e706a-400">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="e706a-401">Weitere Informationen finden Sie im **powermanagementarrays** -Array.</span><span class="sxs-lookup"><span data-stu-id="e706a-401">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="e706a-402">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e706a-402">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e706a-403">**Primäre Partition**</span><span class="sxs-lookup"><span data-stu-id="e706a-403">**PrimaryPartition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e706a-404">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="e706a-404">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e706a-405">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e706a-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e706a-406">Wenn der Wert **true** ist, wird die Datenträger Partition als primäre Partition für ein Computersystem bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="e706a-406">If **TRUE**, the disk partition is labeled as the primary partition for a computer system.</span></span>

</dd> <dt>

<span data-ttu-id="e706a-407">**Zweck**</span><span class="sxs-lookup"><span data-stu-id="e706a-407">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e706a-408">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e706a-408">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e706a-409">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e706a-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e706a-410">Beschreibt die Medien und deren Verwendung.</span><span class="sxs-lookup"><span data-stu-id="e706a-410">Describes the media and its use.</span></span>

<span data-ttu-id="e706a-411">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e706a-411">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="e706a-412">**Status**</span><span class="sxs-lookup"><span data-stu-id="e706a-412">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e706a-413">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e706a-413">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e706a-414">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e706a-414">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e706a-415">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="e706a-415">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="e706a-416">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="e706a-416">Current status of the object.</span></span>

<span data-ttu-id="e706a-417">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e706a-417">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="e706a-418">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="e706a-418">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="e706a-419">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="e706a-419">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="e706a-420">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="e706a-420">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="e706a-421">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="e706a-421">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e706a-422">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="e706a-422">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="e706a-423">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="e706a-423">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="e706a-424">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="e706a-424">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="e706a-425">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="e706a-425">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="e706a-426">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="e706a-426">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="e706a-427">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="e706a-427">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="e706a-428">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="e706a-428">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="e706a-429">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="e706a-429">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="e706a-430">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="e706a-430">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e706a-431">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="e706a-431">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e706a-432">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e706a-432">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e706a-433">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e706a-433">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e706a-434">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="e706a-434">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="e706a-435">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="e706a-435">State of the logical device.</span></span> <span data-ttu-id="e706a-436">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 (nicht zutreffend) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e706a-436">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="e706a-437">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e706a-437">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e706a-438">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="e706a-438">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e706a-439">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="e706a-439">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="e706a-440">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="e706a-440">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="e706a-441">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="e706a-441">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="e706a-442">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="e706a-442">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e706a-443">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="e706a-443">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e706a-444">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e706a-444">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e706a-445">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e706a-445">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e706a-446">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e706a-446">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e706a-447">Die Eigenschaft " **kreationclassname** " des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="e706a-447">Scoping system's **CreationClassName** property.</span></span>

<span data-ttu-id="e706a-448">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e706a-448">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e706a-449">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="e706a-449">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e706a-450">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e706a-450">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e706a-451">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e706a-451">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e706a-452">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e706a-452">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e706a-453">Die **Name** -Eigenschaft des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="e706a-453">Scoping system's **Name** property.</span></span>

<span data-ttu-id="e706a-454">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e706a-454">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e706a-455">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e706a-455">Remarks</span></span>

<span data-ttu-id="e706a-456">Die **CIM \_ Diskpartition** -Klasse wird von [**CIM \_ storageblock**](cim-storageextent.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="e706a-456">The **CIM\_DiskPartition** class is derived from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="e706a-457">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="e706a-457">WMI does not implement this class.</span></span> <span data-ttu-id="e706a-458">Informationen zu von **CIM \_ Diskpartition** abgeleiteten Klassen finden Sie unter [Win32-Klassen](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="e706a-458">For classes derived from **CIM\_DiskPartition**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="e706a-459">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="e706a-459">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e706a-460">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="e706a-460">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e706a-461">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e706a-461">Requirements</span></span>



| <span data-ttu-id="e706a-462">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e706a-462">Requirement</span></span> | <span data-ttu-id="e706a-463">Wert</span><span class="sxs-lookup"><span data-stu-id="e706a-463">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e706a-464">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e706a-464">Minimum supported client</span></span><br/> | <span data-ttu-id="e706a-465">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e706a-465">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e706a-466">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e706a-466">Minimum supported server</span></span><br/> | <span data-ttu-id="e706a-467">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e706a-467">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e706a-468">Namespace</span><span class="sxs-lookup"><span data-stu-id="e706a-468">Namespace</span></span><br/>                | <span data-ttu-id="e706a-469">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e706a-469">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e706a-470">MOF</span><span class="sxs-lookup"><span data-stu-id="e706a-470">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e706a-471"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e706a-471"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e706a-472">DLL</span><span class="sxs-lookup"><span data-stu-id="e706a-472">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e706a-473"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e706a-473"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e706a-474">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e706a-474">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e706a-475">**CIM- \_ storageblock**</span><span class="sxs-lookup"><span data-stu-id="e706a-475">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> </dl>

 

