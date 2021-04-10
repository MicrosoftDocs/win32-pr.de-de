---
description: Win32 \_ mappedlogicaldisk &\# 32; Die WMI-Klasse stellt Netzwerkspeicher Geräte dar, die auf dem Computersystem als logische Datenträger zugeordnet sind.
ms.assetid: 5dd4b0eb-7872-4f2d-9c8b-ea03f7e2c16d
ms.tgt_platform: multiple
title: Win32_MappedLogicalDisk-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_MappedLogicalDisk
- Win32_MappedLogicalDisk.Reset
- Win32_MappedLogicalDisk.SetPowerState
- Win32_MappedLogicalDisk.Access
- Win32_MappedLogicalDisk.Availability
- Win32_MappedLogicalDisk.BlockSize
- Win32_MappedLogicalDisk.Caption
- Win32_MappedLogicalDisk.Compressed
- Win32_MappedLogicalDisk.ConfigManagerErrorCode
- Win32_MappedLogicalDisk.ConfigManagerUserConfig
- Win32_MappedLogicalDisk.CreationClassName
- Win32_MappedLogicalDisk.Description
- Win32_MappedLogicalDisk.DeviceID
- Win32_MappedLogicalDisk.ErrorCleared
- Win32_MappedLogicalDisk.ErrorDescription
- Win32_MappedLogicalDisk.ErrorMethodology
- Win32_MappedLogicalDisk.FileSystem
- Win32_MappedLogicalDisk.FreeSpace
- Win32_MappedLogicalDisk.InstallDate
- Win32_MappedLogicalDisk.LastErrorCode
- Win32_MappedLogicalDisk.MaximumComponentLength
- Win32_MappedLogicalDisk.Name
- Win32_MappedLogicalDisk.NumberOfBlocks
- Win32_MappedLogicalDisk.PNPDeviceID
- Win32_MappedLogicalDisk.PowerManagementCapabilities
- Win32_MappedLogicalDisk.PowerManagementSupported
- Win32_MappedLogicalDisk.ProviderName
- Win32_MappedLogicalDisk.Purpose
- Win32_MappedLogicalDisk.QuotasDisabled
- Win32_MappedLogicalDisk.QuotasIncomplete
- Win32_MappedLogicalDisk.QuotasRebuilding
- Win32_MappedLogicalDisk.SessionID
- Win32_MappedLogicalDisk.Size
- Win32_MappedLogicalDisk.Status
- Win32_MappedLogicalDisk.StatusInfo
- Win32_MappedLogicalDisk.SupportsDiskQuotas
- Win32_MappedLogicalDisk.SupportsFileBasedCompression
- Win32_MappedLogicalDisk.SystemCreationClassName
- Win32_MappedLogicalDisk.SystemName
- Win32_MappedLogicalDisk.VolumeName
- Win32_MappedLogicalDisk.VolumeSerialNumber
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 75c3dfee876c34f36fd0b4cf0b59d3a61afcd75c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127604"
---
# <a name="win32_mappedlogicaldisk-class"></a><span data-ttu-id="1f3bf-103">Win32 \_ mappedlogicaldisk-Klasse</span><span class="sxs-lookup"><span data-stu-id="1f3bf-103">Win32\_MappedLogicalDisk class</span></span>

<span data-ttu-id="1f3bf-104">Die **Win32 \_ mappedlogicaldisk** - [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) stellt Netzwerkspeicher Geräte dar, die auf dem Computersystem als logische Datenträger zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-104">The **Win32\_MappedLogicalDisk** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents network storage devices that are mapped as logical disks on the computer system.</span></span>

<span data-ttu-id="1f3bf-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="1f3bf-106">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f3bf-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f3bf-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{BCF02FFE-5560-4de2-B419-272918693426}"), AMENDMENT]
class Win32_MappedLogicalDisk : CIM_LogicalDisk
{
  uint16   Access;
  uint16   Availability;
  uint64   BlockSize;
  string   Caption;
  boolean  Compressed;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  string   FileSystem;
  uint64   FreeSpace;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint32   MaximumComponentLength;
  string   Name;
  uint64   NumberOfBlocks;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   ProviderName;
  string   Purpose;
  boolean  QuotasDisabled;
  boolean  QuotasIncomplete;
  boolean  QuotasRebuilding;
  string   SessionID;
  uint64   Size;
  string   Status;
  uint16   StatusInfo;
  boolean  SupportsDiskQuotas;
  boolean  SupportsFileBasedCompression;
  string   SystemCreationClassName;
  string   SystemName;
  string   VolumeName;
  string   VolumeSerialNumber;
};
```

## <a name="members"></a><span data-ttu-id="1f3bf-108">Member</span><span class="sxs-lookup"><span data-stu-id="1f3bf-108">Members</span></span>

<span data-ttu-id="1f3bf-109">Die **Win32 \_ mappedlogicaldisk** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1f3bf-109">The **Win32\_MappedLogicalDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="1f3bf-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="1f3bf-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="1f3bf-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1f3bf-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1f3bf-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="1f3bf-112">Methods</span></span>

<span data-ttu-id="1f3bf-113">Die **Win32 \_ mappedlogicaldisk** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-113">The **Win32\_MappedLogicalDisk** class has these methods.</span></span>



| <span data-ttu-id="1f3bf-114">Methode</span><span class="sxs-lookup"><span data-stu-id="1f3bf-114">Method</span></span>            | <span data-ttu-id="1f3bf-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1f3bf-115">Description</span></span>                                                                                                                                                                                |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f3bf-116">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-116">**Reset**</span></span>         | <span data-ttu-id="1f3bf-117">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-117">Not implemented.</span></span> <span data-ttu-id="1f3bf-118">Informationen zur Implementierung dieser Methode finden Sie unter der [**Reset**](reset-method-in-class-cim-controller.md) -Methode in [**CIM \_ LogicalDisk**](cim-logicaldisk.md).</span><span class="sxs-lookup"><span data-stu-id="1f3bf-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_LogicalDisk**](cim-logicaldisk.md).</span></span><br/>                 |
| <span data-ttu-id="1f3bf-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-119">**SetPowerState**</span></span> | <span data-ttu-id="1f3bf-120">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-120">Not implemented.</span></span> <span data-ttu-id="1f3bf-121">Informationen zur Implementierung dieser Methode finden Sie unter der [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode in [**CIM \_ LogicalDisk**](cim-logicaldisk.md).</span><span class="sxs-lookup"><span data-stu-id="1f3bf-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_LogicalDisk**](cim-logicaldisk.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="1f3bf-122">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1f3bf-122">Properties</span></span>

<span data-ttu-id="1f3bf-123">Die **Win32 \_ mappedlogicaldisk** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-123">The **Win32\_MappedLogicalDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1f3bf-124">**zugreifen**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-124">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f3bf-125">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1f3bf-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f3bf-127">Geräte Zugriffsstatus.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-127">Device access state.</span></span>

<span data-ttu-id="1f3bf-128">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-128">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1f3bf-129">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-129">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="1f3bf-130">**Lesbar** (1)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-130">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="1f3bf-131">**Beschreibbar** (2)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-131">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="1f3bf-132">**Lese-/Schreibzugriff unterstützt** (3)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-132">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="1f3bf-133">**Einmal schreiben** (4)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-133">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1f3bf-134">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-134">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f3bf-135">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1f3bf-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-137">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="1f3bf-137">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="1f3bf-138">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-138">Availability and status of the device.</span></span>

<span data-ttu-id="1f3bf-139">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-139">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1f3bf-140"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-140"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1f3bf-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="1f3bf-142"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-142"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="1f3bf-143">Ausführung oder vollständiger Stromversorgung</span><span class="sxs-lookup"><span data-stu-id="1f3bf-143">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="1f3bf-144"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-144"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="1f3bf-145"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-145"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="1f3bf-146"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-146"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="1f3bf-147"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-147"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="1f3bf-148"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-148"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd>

<span data-ttu-id="1f3bf-149">Offline</span><span class="sxs-lookup"><span data-stu-id="1f3bf-149">Offline</span></span>

</dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="1f3bf-150"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-150"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="1f3bf-151"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="1f3bf-151"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="1f3bf-152"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-152"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="1f3bf-153"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-153"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="1f3bf-154"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-154"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="1f3bf-155">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-155">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="1f3bf-156"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-156"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="1f3bf-157">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-157">The device is in a power save state but still functioning and can exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="1f3bf-158"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-158"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="1f3bf-159">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb versetzt werden.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-159">The device is not functioning, but can be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="1f3bf-160"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-160"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="1f3bf-161"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-161"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="1f3bf-162">Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-162">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="1f3bf-163"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-163"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="1f3bf-164">Das Gerät wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-164">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="1f3bf-165"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-165"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="1f3bf-166">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-166">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="1f3bf-167"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-167"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="1f3bf-168">Das Gerät ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-168">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="1f3bf-169"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="1f3bf-169"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="1f3bf-170">Das Gerät ist in Ruhe.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-170">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1f3bf-171">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-171">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f3bf-172">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-172">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-173">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1f3bf-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-174">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. hrstorageallocationunits "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Bytes ")</span><span class="sxs-lookup"><span data-stu-id="1f3bf-174">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="1f3bf-175">Größe (in Bytes) der Blöcke, die diesen Speicherblock bilden.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-175">Size, in bytes, of the blocks that form this storage extent.</span></span> <span data-ttu-id="1f3bf-176">Wenn dieses Konzept für den Gerätetyp nicht gültig ist, ist der Wert 1.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-176">If this concept is not valid for the device type, the value is 1.</span></span>

<span data-ttu-id="1f3bf-177">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-177">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="1f3bf-178">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="1f3bf-178">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="1f3bf-179">**Caption**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-179">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f3bf-180">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-181">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1f3bf-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-182">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="1f3bf-182">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="1f3bf-183">Kurze Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-183">Short description of the object.</span></span>

<span data-ttu-id="1f3bf-184">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-184">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1f3bf-185">**Compressed**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-185">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f3bf-186">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1f3bf-186">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-187">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1f3bf-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-188">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| File System Functions \| [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa) \| FS \_ Vol \_ ist \_ komprimiert")</span><span class="sxs-lookup"><span data-stu-id="1f3bf-188">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)\|FS\_VOL\_IS\_COMPRESSED")</span></span>
</dt> </dl>

<span data-ttu-id="1f3bf-189">**True** gibt an, dass die Datei komprimiert wird.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-189">If **True**, the file is compressed.</span></span>

</dd> <dt>

<span data-ttu-id="1f3bf-190">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-190">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f3bf-191">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-191">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-192">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1f3bf-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-193">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="1f3bf-193">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="1f3bf-194">Windows Configuration Manager-Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-194">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="1f3bf-195">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-195">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="1f3bf-196"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-196"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="1f3bf-197"> (0)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-197">(0)</span></span>


</dt> <dd>

<span data-ttu-id="1f3bf-198">Das Gerät funktioniert ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-198">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="1f3bf-199"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-199"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="1f3bf-200">(1)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-200">(1)</span></span>


</dt> <dd>

<span data-ttu-id="1f3bf-201">Das Gerät ist nicht ordnungsgemäß konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-201">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="1f3bf-202"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-202"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="1f3bf-203">(2)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-203">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="1f3bf-204"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-204"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="1f3bf-205">(3)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-205">(3)</span></span>


</dt> <dd>

<span data-ttu-id="1f3bf-206">Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt möglicherweise nicht über genügend Arbeitsspeicher oder andere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-206">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="1f3bf-207"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-207"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="1f3bf-208">(4)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-208">(4)</span></span>


</dt> <dd>

<span data-ttu-id="1f3bf-209">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-209">Device is not working properly.</span></span> <span data-ttu-id="1f3bf-210">Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-210">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="1f3bf-211"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-211"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="1f3bf-212">(5)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-212">(5)</span></span>


</dt> <dd>

<span data-ttu-id="1f3bf-213">Der Treiber für das Gerät erfordert eine Ressource, die von Windows nicht verwaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-213">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="1f3bf-214"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-214"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="1f3bf-215"> (6)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-215">(6)</span></span>


</dt> <dd>

<span data-ttu-id="1f3bf-216">Die Startkonfiguration für das Gerät steht in Konflikt mit anderen Geräten.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-216">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="1f3bf-217"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-217"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="1f3bf-218">(7)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-218">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="1f3bf-219"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-219"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="1f3bf-220">(8)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-220">(8)</span></span>


</dt> <dd>

<span data-ttu-id="1f3bf-221">Das Treiber Lade Modul für das Gerät fehlt.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-221">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="1f3bf-222"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-222"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="1f3bf-223">(9)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-223">(9)</span></span>


</dt> <dd>

<span data-ttu-id="1f3bf-224">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-224">Device is not working properly.</span></span> <span data-ttu-id="1f3bf-225">Die Steuerungs Firmware meldet nicht korrekt die Ressourcen für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-225">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="1f3bf-226"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-226"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="1f3bf-227">(10)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-227">(10)</span></span>


</dt> <dd>

<span data-ttu-id="1f3bf-228">Das Gerät kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-228">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="1f3bf-229"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-229"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="1f3bf-230">(11)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-230">(11)</span></span>


</dt> <dd>

<span data-ttu-id="1f3bf-231">Fehler beim Gerät.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-231">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="1f3bf-232"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-232"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="1f3bf-233">(12)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-233">(12)</span></span>


</dt> <dd>

<span data-ttu-id="1f3bf-234">Das Gerät kann nicht genug freie Ressourcen für die Verwendung finden.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-234">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="1f3bf-235"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-235"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="1f3bf-236">(13)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-236">(13)</span></span>


</dt> <dd>

<span data-ttu-id="1f3bf-237">Die Geräte Ressourcen können nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-237">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="1f3bf-238"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-238"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="1f3bf-239">(14)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-239">(14)</span></span>


</dt> <dd>

<span data-ttu-id="1f3bf-240">Das Gerät kann erst ordnungsgemäß funktionieren, wenn der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-240">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="1f3bf-241"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-241"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="1f3bf-242">(15)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-242">(15)</span></span>


</dt> <dd>

<span data-ttu-id="1f3bf-243">Das Gerät funktioniert aufgrund eines möglichen erneuten Aufzählungs Problems nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-243">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="1f3bf-244"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-244"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="1f3bf-245">(16)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-245">(16)</span></span>


</dt> <dd>

<span data-ttu-id="1f3bf-246">In Windows können nicht alle Ressourcen identifiziert werden, die vom Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-246">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="1f3bf-247"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-247"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="1f3bf-248">(17)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-248">(17)</span></span>


</dt> <dd>

<span data-ttu-id="1f3bf-249">Das Gerät fordert einen unbekannten Ressourcentyp an.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-249">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="1f3bf-250"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-250"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="1f3bf-251">(18)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-251">(18)</span></span>


</dt> <dd>

<span data-ttu-id="1f3bf-252">Gerätetreiber müssen neu installiert werden.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-252">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="1f3bf-253"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-253"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="1f3bf-254">(19)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-254">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="1f3bf-255"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-255"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="1f3bf-256">(20)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-256">(20)</span></span>


</dt> <dd>

<span data-ttu-id="1f3bf-257">Die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-257">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="1f3bf-258"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-258"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="1f3bf-259">(21)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-259">(21)</span></span>


</dt> <dd>

<span data-ttu-id="1f3bf-260">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-260">System failure.</span></span> <span data-ttu-id="1f3bf-261">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-261">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="1f3bf-262">Das Gerät wird von Windows entfernt.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-262">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="1f3bf-263"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-263"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="1f3bf-264">(22)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-264">(22)</span></span>


</dt> <dd>

<span data-ttu-id="1f3bf-265">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-265">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="1f3bf-266"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-266"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="1f3bf-267">(23)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-267">(23)</span></span>


</dt> <dd>

<span data-ttu-id="1f3bf-268">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-268">System failure.</span></span> <span data-ttu-id="1f3bf-269">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-269">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="1f3bf-270"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-270"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="1f3bf-271">(24)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-271">(24)</span></span>


</dt> <dd>

<span data-ttu-id="1f3bf-272">Das Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-272">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="1f3bf-273"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-273"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="1f3bf-274">(25)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-274">(25)</span></span>


</dt> <dd>

<span data-ttu-id="1f3bf-275">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-275">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="1f3bf-276"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-276"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="1f3bf-277">(26)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-277">(26)</span></span>


</dt> <dd>

<span data-ttu-id="1f3bf-278">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-278">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="1f3bf-279"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-279"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="1f3bf-280">(27)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-280">(27)</span></span>


</dt> <dd>

<span data-ttu-id="1f3bf-281">Das Gerät verfügt nicht über eine gültige Protokoll Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-281">Device does not have a valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="1f3bf-282"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-282"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="1f3bf-283">(28)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-283">(28)</span></span>


</dt> <dd>

<span data-ttu-id="1f3bf-284">Gerätetreiber sind nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-284">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="1f3bf-285"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-285"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="1f3bf-286">(29)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-286">(29)</span></span>


</dt> <dd>

<span data-ttu-id="1f3bf-287">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-287">Device is disabled.</span></span> <span data-ttu-id="1f3bf-288">Die Gerätefirmware hat nicht die erforderlichen Ressourcen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-288">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="1f3bf-289"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-289"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="1f3bf-290">(30)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-290">(30)</span></span>


</dt> <dd>

<span data-ttu-id="1f3bf-291">Das Gerät verwendet eine UNQ-Ressource, die von einem anderen Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-291">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="1f3bf-292"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-292"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="1f3bf-293">31,5</span><span class="sxs-lookup"><span data-stu-id="1f3bf-293">(31)</span></span>


</dt> <dd>

<span data-ttu-id="1f3bf-294">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-294">Device is not working properly.</span></span> <span data-ttu-id="1f3bf-295">Die erforderlichen Gerätetreiber können nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-295">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1f3bf-296">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-296">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f3bf-297">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1f3bf-297">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-298">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1f3bf-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-299">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="1f3bf-299">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="1f3bf-300">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-300">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="1f3bf-301">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-301">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1f3bf-302">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-302">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f3bf-303">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-304">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1f3bf-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-305">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-305">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1f3bf-306">Der Name der ersten konkreten Klasse, die in der Vererbungs Kette angezeigt werden soll, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-306">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="1f3bf-307">Wenn diese Eigenschaft mit den anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-307">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="1f3bf-308">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-308">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1f3bf-309">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-309">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f3bf-310">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-311">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1f3bf-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-312">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="1f3bf-312">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="1f3bf-313">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-313">Description of the object.</span></span>

<span data-ttu-id="1f3bf-314">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-314">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1f3bf-315">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-315">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f3bf-316">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-317">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1f3bf-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-318">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("toviceid"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="1f3bf-318">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="1f3bf-319">Eindeutiger Bezeichner des Speicherarrays.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-319">Unique identifier of the memory array.</span></span>

<span data-ttu-id="1f3bf-320">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="1f3bf-321">Beispiel: "Arbeitsspeicher Array 1"</span><span class="sxs-lookup"><span data-stu-id="1f3bf-321">Example: "Memory Array 1"</span></span>

</dd> <dt>

<span data-ttu-id="1f3bf-322">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-322">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f3bf-323">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1f3bf-323">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-324">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1f3bf-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f3bf-325">**True** gibt an, dass der in **LastErrorCode** gemeldete Fehler jetzt gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-325">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="1f3bf-326">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-326">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1f3bf-327">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-327">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f3bf-328">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-329">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1f3bf-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f3bf-330">Weitere Informationen zu dem Fehler, der in **LastErrorCode** aufgezeichnet wurde, sowie Informationen zu den Maßnahmen, die ausgeführt werden können, finden Sie unter.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-330">More information about the error recorded in **LastErrorCode**, and information on any corrective actions that can be taken.</span></span>

<span data-ttu-id="1f3bf-331">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-331">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1f3bf-332">**Errormethodmethodologie**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-332">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f3bf-333">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-334">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1f3bf-334">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f3bf-335">Typen von Fehlerüberprüfungen, die von der Hardware verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-335">Types of error checking used by the hardware.</span></span>

<span data-ttu-id="1f3bf-336">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-336">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="1f3bf-337">**Verwendet**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-337">**FileSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f3bf-338">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-339">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1f3bf-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-340">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span><span class="sxs-lookup"><span data-stu-id="1f3bf-340">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span></span>
</dt> </dl>

<span data-ttu-id="1f3bf-341">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1f3bf-341">Access type: Read-only</span></span>

<span data-ttu-id="1f3bf-342">Dateisystem auf dem logischen Datenträger.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-342">File system on the logical disk.</span></span>

<span data-ttu-id="1f3bf-343">Beispiel: "NTFS"</span><span class="sxs-lookup"><span data-stu-id="1f3bf-343">Example: "NTFS"</span></span>

</dd> <dt>

<span data-ttu-id="1f3bf-344">**FreeSpace**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-344">**FreeSpace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f3bf-345">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-345">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-346">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1f3bf-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-347">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="1f3bf-347">Qualifiers: [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="1f3bf-348">Auf dem logischen Datenträger verfügbarer Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-348">Space available on the logical disk.</span></span>

<span data-ttu-id="1f3bf-349">Diese Eigenschaft wird von [**CIM \_ LogicalDisk**](cim-logicaldisk.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-349">This property is inherited from [**CIM\_LogicalDisk**](cim-logicaldisk.md).</span></span>

<span data-ttu-id="1f3bf-350">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="1f3bf-350">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="1f3bf-351">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-351">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f3bf-352">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-352">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-353">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1f3bf-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-354">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="1f3bf-354">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="1f3bf-355">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1f3bf-355">Access type: Read-only</span></span>

<span data-ttu-id="1f3bf-356">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-356">Date and time the object was installed.</span></span> <span data-ttu-id="1f3bf-357">Diese Eigenschaft erfordert keinen Wert, um anzugeben, dass das-Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-357">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="1f3bf-358">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-358">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1f3bf-359">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-359">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f3bf-360">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-360">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-361">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1f3bf-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f3bf-362">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-362">Last error code reported by the logical device.</span></span>

<span data-ttu-id="1f3bf-363">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-363">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1f3bf-364">**MaximumComponentLength**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-364">**MaximumComponentLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f3bf-365">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-365">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-366">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1f3bf-366">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-367">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span><span class="sxs-lookup"><span data-stu-id="1f3bf-367">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span></span>
</dt> </dl>

<span data-ttu-id="1f3bf-368">Enthält die maximale Länge einer Dateinamen Komponente, die vom Windows-Laufwerk unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-368">Contains the maximum length of a file-name component supported by the Windows drive.</span></span>

<span data-ttu-id="1f3bf-369">Beispiel: 255</span><span class="sxs-lookup"><span data-stu-id="1f3bf-369">Example: 255</span></span>

</dd> <dt>

<span data-ttu-id="1f3bf-370">**Name**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-370">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f3bf-371">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-371">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-372">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1f3bf-372">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-373">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="1f3bf-373">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="1f3bf-374">Objekt Bezeichnung.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-374">Object label.</span></span>

<span data-ttu-id="1f3bf-375">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-375">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1f3bf-376">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-376">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f3bf-377">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-377">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-378">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1f3bf-378">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-379">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. hrstoragesize ")</span><span class="sxs-lookup"><span data-stu-id="1f3bf-379">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="1f3bf-380">Gesamtanzahl der aufeinander folgenden Blöcke, die jeweils die Größe des in der **BLOCKSIZE** -Eigenschaft enthaltenen Werts blockieren, die diesen Speicherblock bilden.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-380">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="1f3bf-381">Die Gesamtgröße des Speicherbereichs kann berechnet werden, indem der Wert der **BLOCKSIZE** -Eigenschaft mit dem Wert dieser Eigenschaft multipliziert wird.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-381">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="1f3bf-382">Wenn der Wert von **BLOCKSIZE** 1 ist, entspricht diese Eigenschaft der Gesamtgröße des Speicherblocks.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-382">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="1f3bf-383">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-383">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="1f3bf-384">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="1f3bf-384">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="1f3bf-385">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-385">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f3bf-386">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-386">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-387">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1f3bf-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-388">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="1f3bf-388">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="1f3bf-389">Windows Plug & Play Geräte Bezeichner des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-389">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="1f3bf-390">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-390">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="1f3bf-391">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="1f3bf-391">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="1f3bf-392">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-392">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f3bf-393">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="1f3bf-393">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-394">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1f3bf-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f3bf-395">Array der spezifischen energiebezogenen Funktionen eines logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-395">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="1f3bf-396">Diese Eigenschaft wird von **CIM \_ LogicalDevice** geerbt.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-396">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1f3bf-397"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-397"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="1f3bf-398"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-398"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="1f3bf-399"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-399"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="1f3bf-400"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-400"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="1f3bf-401">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-401">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="1f3bf-402"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-402"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="1f3bf-403">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-403">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="1f3bf-404"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-404"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="1f3bf-405">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-405">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="1f3bf-406">Diese Methode wird in der übergeordneten **CIM \_ LogicalDevice** -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-406">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="1f3bf-407">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="1f3bf-407">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="1f3bf-408"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-408"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="1f3bf-409">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-409">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="1f3bf-410"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-410"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="1f3bf-411">Zeitgesteuerte Power-On unterstützt</span><span class="sxs-lookup"><span data-stu-id="1f3bf-411">Timed Power-On Supported</span></span>

<span data-ttu-id="1f3bf-412">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) und die *Uhrzeit* auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-412">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1f3bf-413">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-413">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f3bf-414">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1f3bf-414">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-415">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1f3bf-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f3bf-416">Wenn der Wert **true** ist, kann das Gerät Energie gesteuert werden (kann in den Unterbrechungs Modus versetzt werden usw.).</span><span class="sxs-lookup"><span data-stu-id="1f3bf-416">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="1f3bf-417">Die-Eigenschaft gibt nicht an, dass die Energie Verwaltungsfunktionen zurzeit aktiviert sind, sondern nur, dass das logische Gerät für die Energie Verwaltung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-417">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="1f3bf-418">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-418">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1f3bf-419">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-419">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f3bf-420">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-420">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-421">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1f3bf-421">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-422">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Windows Networking Functions \| WNetGetConnection")</span><span class="sxs-lookup"><span data-stu-id="1f3bf-422">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Windows Networking Functions\|WNetGetConnection")</span></span>
</dt> </dl>

<span data-ttu-id="1f3bf-423">Der Netzwerk Pfadname für das logische Gerät.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-423">Network path name to the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="1f3bf-424">**Zweck**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-424">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f3bf-425">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-425">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-426">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1f3bf-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f3bf-427">Frei Form Zeichenfolge, die die Medien und deren Verwendung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-427">Free-form string that describes the media and its use.</span></span>

<span data-ttu-id="1f3bf-428">Diese Eigenschaft wird von [**CIM \_ storageblock**](cim-storageextent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-428">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="1f3bf-429">**Quotasdeaktiviert**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-429">**QuotasDisabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f3bf-430">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1f3bf-430">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-431">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1f3bf-431">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f3bf-432">**True** gibt an, dass die Kontingent Verwaltung für dieses Volume nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-432">If **True**, quota management is not enabled for this volume.</span></span>

</dd> <dt>

<span data-ttu-id="1f3bf-433">**Quotasunvollständig**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-433">**QuotasIncomplete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f3bf-434">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1f3bf-434">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-435">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1f3bf-435">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f3bf-436">**True** gibt an, dass die Kontingent Verwaltung verwendet, aber deaktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-436">If **True**, quota management was used but has been disabled.</span></span> <span data-ttu-id="1f3bf-437">Unvollständig bezieht sich auf die im Dateisystem verbleibenden Informationen, nachdem die Kontingent Verwaltung deaktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-437">Incomplete refers to the information left in the file system after quota management has been disabled.</span></span>

</dd> <dt>

<span data-ttu-id="1f3bf-438">**Quotasrebuild**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-438">**QuotasRebuilding**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f3bf-439">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1f3bf-439">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-440">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1f3bf-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f3bf-441">**True** gibt an, dass das Dateisystem für die Kontingent Verwaltung eingerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-441">If **True**, the file system is setting up for quota management.</span></span>

</dd> <dt>

<span data-ttu-id="1f3bf-442">**SessionID**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-442">**SessionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f3bf-443">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-443">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-444">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1f3bf-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-445">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-445">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1f3bf-446">Die ID der Sitzung des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-446">ID of the user's session.</span></span> <span data-ttu-id="1f3bf-447">Der Benutzer kann mit einer lokalen Anmeldung oder einer Terminalsitzung verbunden sein.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-447">The user may be connected using a local login or a terminal session.</span></span>

</dd> <dt>

<span data-ttu-id="1f3bf-448">**Größe**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-448">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f3bf-449">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-449">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-450">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1f3bf-450">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-451">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="1f3bf-451">Qualifiers: [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="1f3bf-452">Größe des logischen Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-452">Size of the logical disk.</span></span>

<span data-ttu-id="1f3bf-453">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="1f3bf-453">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="1f3bf-454">Diese Eigenschaft wird von [**CIM \_ LogicalDisk**](cim-logicaldisk.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-454">This property is inherited from [**CIM\_LogicalDisk**](cim-logicaldisk.md).</span></span>

</dd> <dt>

<span data-ttu-id="1f3bf-455">**Status**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-455">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f3bf-456">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-456">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-457">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1f3bf-457">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-458">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="1f3bf-458">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="1f3bf-459">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-459">Current status of the object.</span></span> <span data-ttu-id="1f3bf-460">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-460">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="1f3bf-461">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein intelligent-fähiges Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber prognostiziert einen Fehler in naher Zukunft).</span><span class="sxs-lookup"><span data-stu-id="1f3bf-461">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive may function properly, but predicts a failure in the near future).</span></span> <span data-ttu-id="1f3bf-462">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="1f3bf-462">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="1f3bf-463">Der Dienststatus gilt für administrative Aufgaben, z. b. die Spiegelung eines Datenträgers, das erneute Laden einer Benutzer Berechtigungs Liste oder andere administrative Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-463">The Service status applies to administrative work, such as mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="1f3bf-464">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-464">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="1f3bf-465">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-465">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="1f3bf-466">Die Werte sind:</span><span class="sxs-lookup"><span data-stu-id="1f3bf-466">The values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="1f3bf-467">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="1f3bf-467">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="1f3bf-468">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="1f3bf-468">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="1f3bf-469">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="1f3bf-469">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1f3bf-470">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="1f3bf-470">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="1f3bf-471">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="1f3bf-471">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="1f3bf-472">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="1f3bf-472">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="1f3bf-473">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="1f3bf-473">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="1f3bf-474">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="1f3bf-474">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="1f3bf-475">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="1f3bf-475">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="1f3bf-476">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="1f3bf-476">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="1f3bf-477">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="1f3bf-477">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="1f3bf-478">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="1f3bf-478">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1f3bf-479">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-479">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f3bf-480">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-480">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-481">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1f3bf-481">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-482">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="1f3bf-482">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="1f3bf-483">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-483">State of the logical device.</span></span> <span data-ttu-id="1f3bf-484">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 (nicht zutreffend) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-484">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="1f3bf-485">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-485">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1f3bf-486">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-486">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1f3bf-487">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-487">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="1f3bf-488">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-488">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="1f3bf-489">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-489">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="1f3bf-490">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-490">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1f3bf-491">**Supportsdiskkontingenten**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-491">**SupportsDiskQuotas**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f3bf-492">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1f3bf-492">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-493">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1f3bf-493">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f3bf-494">**True** gibt an, dass das Dateisystem, dem dieses Netzwerklaufwerk zugeordnet ist, Datenträger Kontingente unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-494">If **True**, then the file system on which this network drive is mapped supports disk quotas.</span></span>

</dd> <dt>

<span data-ttu-id="1f3bf-495">**SupportsFileBasedCompression**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-495">**SupportsFileBasedCompression**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f3bf-496">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="1f3bf-496">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-497">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1f3bf-497">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-498">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| File System Functions \| [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa) \| FS \_ file \_ Compression")</span><span class="sxs-lookup"><span data-stu-id="1f3bf-498">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)\|FS\_FILE\_COMPRESSION")</span></span>
</dt> </dl>

<span data-ttu-id="1f3bf-499">**True** gibt an, dass die logische Datenträger Partition dateibasierte Komprimierung unterstützt, wie z. b. bei NTFS.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-499">If **True**, the logical disk partition supports file-based compression, such as is the case with NTFS.</span></span> <span data-ttu-id="1f3bf-500">Diese Eigenschaft ist **false**, wenn die **komprimierte** Eigenschaft den Wert **true** hat.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-500">This property is **False**, when the **Compressed** property is **True**.</span></span>

</dd> <dt>

<span data-ttu-id="1f3bf-501">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-501">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f3bf-502">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-502">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-503">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1f3bf-503">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-504">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-504">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1f3bf-505">Der Wert der Eigenschaft " **kreationclassname** " des Bereichs Computers.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-505">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="1f3bf-506">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-506">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1f3bf-507">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-507">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f3bf-508">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-508">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-509">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1f3bf-509">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-510">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-510">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1f3bf-511">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-511">Name of the scoping system.</span></span>

<span data-ttu-id="1f3bf-512">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-512">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1f3bf-513">**Volumename**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-513">**VolumeName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f3bf-514">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-514">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-515">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1f3bf-515">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-516">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span><span class="sxs-lookup"><span data-stu-id="1f3bf-516">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span></span>
</dt> </dl>

<span data-ttu-id="1f3bf-517">Der Volumename des logischen Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-517">Volume name of the logical disk.</span></span> <span data-ttu-id="1f3bf-518">Dieser Eigenschafts Wert kann maximal 32 Zeichen umfassen.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-518">This property value can have a maximum of 32 characters.</span></span>

</dd> <dt>

<span data-ttu-id="1f3bf-519">**VolumeSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-519">**VolumeSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f3bf-520">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-520">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-521">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1f3bf-521">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1f3bf-522">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span><span class="sxs-lookup"><span data-stu-id="1f3bf-522">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span></span>
</dt> </dl>

<span data-ttu-id="1f3bf-523">Seriennummer des logischen Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-523">Volume serial number of the logical disk.</span></span> <span data-ttu-id="1f3bf-524">Dieser Eigenschafts Wert kann maximal 11 Zeichen umfassen.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-524">This property value can have a maximum of 11 characters.</span></span>

<span data-ttu-id="1f3bf-525">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-525">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="1f3bf-526">Beispiel: "A8C3-D032"</span><span class="sxs-lookup"><span data-stu-id="1f3bf-526">Example: "A8C3-D032"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1f3bf-527">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1f3bf-527">Remarks</span></span>

<span data-ttu-id="1f3bf-528">Die für diese Klasse zurückgegebenen Instanzen lauten wie folgt, um zu untersuchen, dass Benutzer A die-Instanzen auflistet:</span><span class="sxs-lookup"><span data-stu-id="1f3bf-528">The instances returned for this class are as follows, supposing that user A is enumerating the instances:</span></span>

-   <span data-ttu-id="1f3bf-529">Der Anbieter sucht eine Anmelde Sitzung von Benutzer a auf diesem Computer:</span><span class="sxs-lookup"><span data-stu-id="1f3bf-529">The provider looks for a logon session of user A on that machine:</span></span>

    -   <span data-ttu-id="1f3bf-530">Wenn eine solche Anmelde Sitzung (und nur eine) vorhanden ist, gibt der Anbieter die zugeordneten Laufwerke dieser Sitzung zurück.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-530">If there is one (and only one) such logon session, then the provider returns the mapped drives of that session.</span></span>
    -   <span data-ttu-id="1f3bf-531">Wenn für Benutzer A auf dem Computer mehr als eine Sitzung vorhanden ist, werden keine zugeordneten Laufwerks Instanzen zurückgegeben (weil der Anbieter keine angemessene Methode zur Entscheidung über die zu verwendende Sitzung hat).</span><span class="sxs-lookup"><span data-stu-id="1f3bf-531">If there is more than one session for user A on the machine, then no mapped drive instances are returned (because the provider has no reasonable way of deciding which session to use).</span></span>

-   <span data-ttu-id="1f3bf-532">Wenn keine Sitzungen von Benutzer a ausgeführt werden und ein lokal angemeldeter Benutzer B vorhanden ist:</span><span class="sxs-lookup"><span data-stu-id="1f3bf-532">If there are no sessions of user A running, and there is a locally logged on user B:</span></span>

    -   <span data-ttu-id="1f3bf-533">Wenn eine einzelne Sitzung für Benutzer b vorhanden ist, nimmt der Anbieter einen Identitätswechsel vor und gibt die zugeordneten Laufwerke von Benutzer b zurück. In diesem Fall wird das Szenario des Helpdesk unterstützt, in dem die Instanzen eines lokal angemeldeten Benutzers angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-533">If there is a single session for user B, then the provider impersonates A and returns the mapped drives of user B. This case supports the scenario of Helpdesk wanting to see the instances of a locally logged on user.</span></span> <span data-ttu-id="1f3bf-534">Ob Instanzen zurückgegeben werden, hängt jedoch von den Einstellungen der lokalen Sicherheitsrichtlinie in der Systemsteuerung Verwaltungs Tools ab.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-534">However, whether instances are returned depends on the Local Security Policy settings in the Control Panel Administrative Tools.</span></span> <span data-ttu-id="1f3bf-535">Wenn die folgende Richtlinie auf "Objekt Ersteller" festgelegt ist, werden keine zugeordneten Laufwerks Instanzen zurückgegeben, selbst wenn ein Mitglied der Gruppe "Administratoren" ist:</span><span class="sxs-lookup"><span data-stu-id="1f3bf-535">If the following policy is set to "Object Creator", then no mapped drive instances are returned, even if A is a member of the Administrators group:</span></span>

        <span data-ttu-id="1f3bf-536">"System Objekt: Standard Besitzer für Objekte, die von Mitgliedern der Gruppe" Administratoren "erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-536">"System object: default owner for objects created by members of the administrators group."</span></span>

    -   <span data-ttu-id="1f3bf-537">Wenn mehr als eine Sitzung von Benutzer B auf dem Computer ausgeführt wird, hat der Anbieter keine Möglichkeit, zu entscheiden, welche verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-537">Again, if there is more than one session of user B running on the machine, then the provider has no way of deciding which to use.</span></span> <span data-ttu-id="1f3bf-538">In diesem Fall werden keine zugeordneten Laufwerks Instanzen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-538">In this case, no mapped drive instances are returned.</span></span>

<span data-ttu-id="1f3bf-539">Weitere Informationen zur Verwendung von **Win32 \_ mappedlogicaldisk** finden Sie unter [wie kann ich ermitteln, welche Laufwerke Netzwerkfreigaben zugeordnet sind?](https://blogs.technet.com/b/heyscriptingguy/archive/2005/10/27/how-can-i-determine-which-drives-are-mapped-to-network-shares.aspx)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-539">For more information on using **Win32\_MappedLogicalDisk**, see [How Can I Determine Which Drives are Mapped to Network Shares?](https://blogs.technet.com/b/heyscriptingguy/archive/2005/10/27/how-can-i-determine-which-drives-are-mapped-to-network-shares.aspx)</span></span>

## <a name="examples"></a><span data-ttu-id="1f3bf-540">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1f3bf-540">Examples</span></span>

<span data-ttu-id="1f3bf-541">Der folgende PowerShell-Code Ausschnitt zeigt zugeordnete Laufwerke.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-541">The following PowerShell snippet shows mapped drives.</span></span>


```PowerShell
Get-WmiObject Win32_MappedLogicalDisk | Select Name, ProviderName, FileSystem, Size, FreeSpace | Format-Table
```



## <a name="requirements"></a><span data-ttu-id="1f3bf-542">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1f3bf-542">Requirements</span></span>



| <span data-ttu-id="1f3bf-543">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1f3bf-543">Requirement</span></span> | <span data-ttu-id="1f3bf-544">Wert</span><span class="sxs-lookup"><span data-stu-id="1f3bf-544">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f3bf-545">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-545">Minimum supported client</span></span><br/> | <span data-ttu-id="1f3bf-546">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1f3bf-546">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1f3bf-547">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1f3bf-547">Minimum supported server</span></span><br/> | <span data-ttu-id="1f3bf-548">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1f3bf-548">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1f3bf-549">Namespace</span><span class="sxs-lookup"><span data-stu-id="1f3bf-549">Namespace</span></span><br/>                | <span data-ttu-id="1f3bf-550">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="1f3bf-550">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1f3bf-551">MOF</span><span class="sxs-lookup"><span data-stu-id="1f3bf-551">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1f3bf-552"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1f3bf-552"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1f3bf-553">DLL</span><span class="sxs-lookup"><span data-stu-id="1f3bf-553">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f3bf-554"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f3bf-554"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f3bf-555">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1f3bf-555">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f3bf-556">**CIM \_ LogicalDisk**</span><span class="sxs-lookup"><span data-stu-id="1f3bf-556">**CIM\_LogicalDisk**</span></span>](cim-logicaldisk.md)
</dt> <dt>

[<span data-ttu-id="1f3bf-557">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="1f3bf-557">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="1f3bf-558">WMI-Tasks: Datenträger und Dateisysteme</span><span class="sxs-lookup"><span data-stu-id="1f3bf-558">WMI Tasks: Disks and File Systems</span></span>](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems)
</dt> </dl>

 

