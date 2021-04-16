---
description: Stellt ein physisches Laufwerk dar, das auf einem Computer mit dem Windows-Betriebssystem angezeigt wird.
ms.assetid: c1fc6a1e-e725-484b-aacf-279f777e9b19
ms.tgt_platform: multiple
title: Win32_DiskDrive-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DiskDrive
- Win32_DiskDrive.Reset
- Win32_DiskDrive.SetPowerState
- Win32_DiskDrive.Availability
- Win32_DiskDrive.BytesPerSector
- Win32_DiskDrive.Capabilities
- Win32_DiskDrive.CapabilityDescriptions
- Win32_DiskDrive.Caption
- Win32_DiskDrive.CompressionMethod
- Win32_DiskDrive.ConfigManagerErrorCode
- Win32_DiskDrive.ConfigManagerUserConfig
- Win32_DiskDrive.CreationClassName
- Win32_DiskDrive.DefaultBlockSize
- Win32_DiskDrive.Description
- Win32_DiskDrive.DeviceID
- Win32_DiskDrive.ErrorCleared
- Win32_DiskDrive.ErrorDescription
- Win32_DiskDrive.ErrorMethodology
- Win32_DiskDrive.FirmwareRevision
- Win32_DiskDrive.Index
- Win32_DiskDrive.InstallDate
- Win32_DiskDrive.InterfaceType
- Win32_DiskDrive.LastErrorCode
- Win32_DiskDrive.Manufacturer
- Win32_DiskDrive.MaxBlockSize
- Win32_DiskDrive.MaxMediaSize
- Win32_DiskDrive.MediaLoaded
- Win32_DiskDrive.MediaType
- Win32_DiskDrive.MinBlockSize
- Win32_DiskDrive.Model
- Win32_DiskDrive.Name
- Win32_DiskDrive.NeedsCleaning
- Win32_DiskDrive.NumberOfMediaSupported
- Win32_DiskDrive.Partitions
- Win32_DiskDrive.PNPDeviceID
- Win32_DiskDrive.PowerManagementCapabilities
- Win32_DiskDrive.PowerManagementSupported
- Win32_DiskDrive.SCSIBus
- Win32_DiskDrive.SCSILogicalUnit
- Win32_DiskDrive.SCSIPort
- Win32_DiskDrive.SCSITargetId
- Win32_DiskDrive.SectorsPerTrack
- Win32_DiskDrive.SerialNumber
- Win32_DiskDrive.Signature
- Win32_DiskDrive.Size
- Win32_DiskDrive.Status
- Win32_DiskDrive.StatusInfo
- Win32_DiskDrive.SystemCreationClassName
- Win32_DiskDrive.SystemName
- Win32_DiskDrive.TotalCylinders
- Win32_DiskDrive.TotalHeads
- Win32_DiskDrive.TotalSectors
- Win32_DiskDrive.TotalTracks
- Win32_DiskDrive.TracksPerCylinder
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 751dee053574be417cb312f6b046ae6b7703d543
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523984"
---
# <a name="win32_diskdrive-class"></a><span data-ttu-id="3a9da-103">Win32 \_ diskdrive-Klasse</span><span class="sxs-lookup"><span data-stu-id="3a9da-103">Win32\_DiskDrive class</span></span>

<span data-ttu-id="3a9da-104">Die **Win32 \_ diskdrive** [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) stellt ein physisches Laufwerk dar, das auf einem Computer mit dem Windows-Betriebssystem angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="3a9da-104">The **Win32\_DiskDrive** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a physical disk drive as seen by a computer running the Windows operating system.</span></span>

<span data-ttu-id="3a9da-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3a9da-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="3a9da-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="3a9da-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a9da-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a9da-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4B2-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DiskDrive : CIM_DiskDrive
{
  uint16   Availability;
  uint32   BytesPerSector;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   Caption;
  string   CompressionMethod;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint64   DefaultBlockSize;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  string   FirmwareRevision;
  uint32   Index;
  datetime InstallDate;
  string   InterfaceType;
  uint32   LastErrorCode;
  string   Manufacturer;
  uint64   MaxBlockSize;
  uint64   MaxMediaSize;
  boolean  MediaLoaded;
  string   MediaType;
  uint64   MinBlockSize;
  string   Model;
  string   Name;
  boolean  NeedsCleaning;
  uint32   NumberOfMediaSupported;
  uint32   Partitions;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint32   SCSIBus;
  uint16   SCSILogicalUnit;
  uint16   SCSIPort;
  uint16   SCSITargetId;
  uint32   SectorsPerTrack;
  string   SerialNumber;
  uint32   Signature;
  uint64   Size;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint64   TotalCylinders;
  uint32   TotalHeads;
  uint64   TotalSectors;
  uint64   TotalTracks;
  uint32   TracksPerCylinder;
};
```

## <a name="members"></a><span data-ttu-id="3a9da-108">Member</span><span class="sxs-lookup"><span data-stu-id="3a9da-108">Members</span></span>

<span data-ttu-id="3a9da-109">Die **Win32 \_ diskdrive** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="3a9da-109">The **Win32\_DiskDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="3a9da-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="3a9da-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="3a9da-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3a9da-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3a9da-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="3a9da-112">Methods</span></span>

<span data-ttu-id="3a9da-113">Die **Win32 \_ diskdrive** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="3a9da-113">The **Win32\_DiskDrive** class has these methods.</span></span>



| <span data-ttu-id="3a9da-114">Methode</span><span class="sxs-lookup"><span data-stu-id="3a9da-114">Method</span></span>            | <span data-ttu-id="3a9da-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3a9da-115">Description</span></span>                                                                                                                                                                                              |
|:------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a9da-116">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="3a9da-116">**Reset**</span></span>         | <span data-ttu-id="3a9da-117">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="3a9da-117">Not implemented.</span></span> <span data-ttu-id="3a9da-118">Informationen zur Implementierung dieser Methode finden Sie unter der [**Reset**](reset-method-in-class-cim-controller.md) -Methode in [**CIM \_ diskdrive**](cim-diskdrive.md) .</span><span class="sxs-lookup"><span data-stu-id="3a9da-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_DiskDrive**](cim-diskdrive.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="3a9da-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="3a9da-119">**SetPowerState**</span></span> | <span data-ttu-id="3a9da-120">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="3a9da-120">Not implemented.</span></span> <span data-ttu-id="3a9da-121">Informationen zur Implementierung dieser Methode finden Sie in der [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode in [**CIM \_ diskdrive**](cim-diskdrive.md) .</span><span class="sxs-lookup"><span data-stu-id="3a9da-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_DiskDrive**](cim-diskdrive.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="3a9da-122">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3a9da-122">Properties</span></span>

<span data-ttu-id="3a9da-123">Die **Win32 \_ diskdrive** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3a9da-123">The **Win32\_DiskDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3a9da-124">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="3a9da-124">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a9da-125">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a9da-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a9da-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-127">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="3a9da-127">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="3a9da-128">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="3a9da-128">Availability and status of the device.</span></span>

<span data-ttu-id="3a9da-129">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3a9da-129">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3a9da-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="3a9da-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3a9da-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="3a9da-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="3a9da-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="3a9da-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="3a9da-133">Ausführung oder vollständiger Stromversorgung</span><span class="sxs-lookup"><span data-stu-id="3a9da-133">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="3a9da-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="3a9da-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="3a9da-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="3a9da-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="3a9da-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="3a9da-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="3a9da-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="3a9da-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="3a9da-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="3a9da-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="3a9da-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="3a9da-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="3a9da-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="3a9da-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="3a9da-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="3a9da-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="3a9da-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="3a9da-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="3a9da-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="3a9da-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="3a9da-144">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="3a9da-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="3a9da-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="3a9da-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="3a9da-146">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="3a9da-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="3a9da-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="3a9da-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="3a9da-148">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb gebracht werden.</span><span class="sxs-lookup"><span data-stu-id="3a9da-148">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="3a9da-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="3a9da-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="3a9da-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="3a9da-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="3a9da-151">Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="3a9da-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="3a9da-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="3a9da-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="3a9da-153"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="3a9da-153"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="3a9da-154"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="3a9da-154"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="3a9da-155"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="3a9da-155"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="3a9da-156">Das Laufwerk ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3a9da-156">The disk drive is unavailable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3a9da-157">**Bytespersektor**</span><span class="sxs-lookup"><span data-stu-id="3a9da-157">**BytesPerSector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a9da-158">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3a9da-158">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-159">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a9da-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-160">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Input and Output Structures \| [**Disk \_ Geometry**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| bytespersektor"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="3a9da-160">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|BytesPerSector"), [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="3a9da-161">Anzahl von Bytes in den einzelnen Sektoren für das physische Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="3a9da-161">Number of bytes in each sector for the physical disk drive.</span></span>

<span data-ttu-id="3a9da-162">Beispiel: 512</span><span class="sxs-lookup"><span data-stu-id="3a9da-162">Example: 512</span></span>

</dd> <dt>

<span data-ttu-id="3a9da-163">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="3a9da-163">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a9da-164">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="3a9da-164">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-165">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a9da-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-166">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergeräte \| 001,9 "," MIF. DMTF- \| Speichergeräte \| 001,11 "," MIF. DMTF- \| Speichergeräte \| 001,12 "," MIF. DMTF-Datenträger \| \| 003,7 "), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md).**Capabilitybeschreibungen**")</span><span class="sxs-lookup"><span data-stu-id="3a9da-166">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="3a9da-167">Array von Funktionen des Medien Zugriffs Geräts.</span><span class="sxs-lookup"><span data-stu-id="3a9da-167">Array of capabilities of the media access device.</span></span> <span data-ttu-id="3a9da-168">Beispielsweise kann das Gerät zufälligen Zugriff (3), Wechselmedien (7) und automatische Bereinigung (9) unterstützen.</span><span class="sxs-lookup"><span data-stu-id="3a9da-168">For example, the device may support random access (3), removable media (7), and automatic cleaning (9).</span></span>

<span data-ttu-id="3a9da-169">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3a9da-169">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3a9da-170"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="3a9da-170"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3a9da-171"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="3a9da-171"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="3a9da-172"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequenzieller Zugriff** (2)</span><span class="sxs-lookup"><span data-stu-id="3a9da-172"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="3a9da-173"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Zufälliger Zugriff** (3)</span><span class="sxs-lookup"><span data-stu-id="3a9da-173"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="3a9da-174"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Unterstützt Schreib** Vorgänge (4)</span><span class="sxs-lookup"><span data-stu-id="3a9da-174"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="3a9da-175"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Verschlüsselung** (5)</span><span class="sxs-lookup"><span data-stu-id="3a9da-175"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="3a9da-176"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Komprimierung** (6)</span><span class="sxs-lookup"><span data-stu-id="3a9da-176"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="3a9da-177"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Unterstützt Removeable Media** (7)</span><span class="sxs-lookup"><span data-stu-id="3a9da-177"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="3a9da-178">Unterstützt Wechselmedien</span><span class="sxs-lookup"><span data-stu-id="3a9da-178">Supports Removable Media</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="3a9da-179"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manuelle Reinigung** (8)</span><span class="sxs-lookup"><span data-stu-id="3a9da-179"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="3a9da-180"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatische Bereinigung** (9)</span><span class="sxs-lookup"><span data-stu-id="3a9da-180"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="3a9da-181"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**Smart Notification** (10)</span><span class="sxs-lookup"><span data-stu-id="3a9da-181"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="3a9da-182"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Unterstützt zweiseitige Medien** (11)</span><span class="sxs-lookup"><span data-stu-id="3a9da-182"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="3a9da-183">Unterstützt Dual-Sided Medien</span><span class="sxs-lookup"><span data-stu-id="3a9da-183">Supports Dual-Sided Media</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="3a9da-184"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount-eject nicht erforderlich** (12)</span><span class="sxs-lookup"><span data-stu-id="3a9da-184"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd>

<span data-ttu-id="3a9da-185">Der Ejection vor der Aufhebung der Laufwerk Aufhebung ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3a9da-185">Ejection Prior to Drive Dismount Not Required</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3a9da-186">**Capabilitybeschreibungen**</span><span class="sxs-lookup"><span data-stu-id="3a9da-186">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a9da-187">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="3a9da-187">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-188">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a9da-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-189">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md).**Funktionen**")</span><span class="sxs-lookup"><span data-stu-id="3a9da-189">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="3a9da-190">Liste der detaillierteren Erläuterungen für alle Zugriffsgeräte Funktionen, die im **Funktions Array angegeben** sind.</span><span class="sxs-lookup"><span data-stu-id="3a9da-190">List of more detailed explanations for any of the access device features indicated in the **Capabilities** array.</span></span> <span data-ttu-id="3a9da-191">Beachten Sie, dass jeder Eintrag dieses Arrays mit dem Eintrag im **Funktions Array verknüpft ist, der sich** am selben Index befindet.</span><span class="sxs-lookup"><span data-stu-id="3a9da-191">Note, each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

<span data-ttu-id="3a9da-192">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3a9da-192">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a9da-193">**Caption**</span><span class="sxs-lookup"><span data-stu-id="3a9da-193">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a9da-194">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3a9da-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-195">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a9da-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-196">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="3a9da-196">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="3a9da-197">Kurze Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="3a9da-197">Short description of the object.</span></span>

<span data-ttu-id="3a9da-198">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3a9da-198">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a9da-199">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="3a9da-199">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a9da-200">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3a9da-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-201">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a9da-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a9da-202">Der Algorithmus oder das Tool, mit dem das Gerät die Komprimierung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3a9da-202">Algorithm or tool used by the device to support compression.</span></span> <span data-ttu-id="3a9da-203">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3a9da-203">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="3a9da-204">Der Name des Komprimierungs Algorithmus oder eines der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="3a9da-204">The name of the compression algorithm or one of the following values.</span></span>

<dt>



 <span data-ttu-id="3a9da-205">("Unbekannt")</span><span class="sxs-lookup"><span data-stu-id="3a9da-205">("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="3a9da-206">Ob das Gerät Komprimierungs Funktionen unterstützt oder nicht, ist nicht bekannt.</span><span class="sxs-lookup"><span data-stu-id="3a9da-206">Whether the device supports compression capabilities or not is not known.</span></span>

</dd> <dt>



 <span data-ttu-id="3a9da-207">("Komprimiert")</span><span class="sxs-lookup"><span data-stu-id="3a9da-207">("Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="3a9da-208">Das Gerät unterstützt Komprimierungs Funktionen, das zugehörige Komprimierungs Schema ist jedoch nicht bekannt oder nicht offengelegt.</span><span class="sxs-lookup"><span data-stu-id="3a9da-208">The device supports compression capabilities but its compression scheme is not known or not disclosed.</span></span>

</dd> <dt>



 <span data-ttu-id="3a9da-209">("Nicht komprimiert")</span><span class="sxs-lookup"><span data-stu-id="3a9da-209">("Not Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="3a9da-210">Das Gerät unterstützt keine Komprimierung.</span><span class="sxs-lookup"><span data-stu-id="3a9da-210">The device does not support compression.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3a9da-211">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="3a9da-211">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a9da-212">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3a9da-212">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-213">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a9da-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-214">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="3a9da-214">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="3a9da-215">Windows Configuration Manager-Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="3a9da-215">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="3a9da-216">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3a9da-216">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="3a9da-217"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="3a9da-217"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="3a9da-218"> (0)</span><span class="sxs-lookup"><span data-stu-id="3a9da-218">(0)</span></span>


</dt> <dd>

<span data-ttu-id="3a9da-219">Das Gerät funktioniert ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="3a9da-219">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="3a9da-220"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="3a9da-220"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="3a9da-221">(1)</span><span class="sxs-lookup"><span data-stu-id="3a9da-221">(1)</span></span>


</dt> <dd>

<span data-ttu-id="3a9da-222">Das Gerät ist nicht ordnungsgemäß konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="3a9da-222">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="3a9da-223"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="3a9da-223"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="3a9da-224">(2)</span><span class="sxs-lookup"><span data-stu-id="3a9da-224">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="3a9da-225"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="3a9da-225"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="3a9da-226">(3)</span><span class="sxs-lookup"><span data-stu-id="3a9da-226">(3)</span></span>


</dt> <dd>

<span data-ttu-id="3a9da-227">Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt möglicherweise nicht über genügend Arbeitsspeicher oder andere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="3a9da-227">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="3a9da-228"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="3a9da-228"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="3a9da-229">(4)</span><span class="sxs-lookup"><span data-stu-id="3a9da-229">(4)</span></span>


</dt> <dd>

<span data-ttu-id="3a9da-230">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="3a9da-230">Device is not working properly.</span></span> <span data-ttu-id="3a9da-231">Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="3a9da-231">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="3a9da-232"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="3a9da-232"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="3a9da-233">(5)</span><span class="sxs-lookup"><span data-stu-id="3a9da-233">(5)</span></span>


</dt> <dd>

<span data-ttu-id="3a9da-234">Der Treiber für das Gerät erfordert eine Ressource, die von Windows nicht verwaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="3a9da-234">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="3a9da-235"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="3a9da-235"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="3a9da-236"> (6)</span><span class="sxs-lookup"><span data-stu-id="3a9da-236">(6)</span></span>


</dt> <dd>

<span data-ttu-id="3a9da-237">Die Startkonfiguration für das Gerät steht in Konflikt mit anderen Geräten.</span><span class="sxs-lookup"><span data-stu-id="3a9da-237">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="3a9da-238"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="3a9da-238"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="3a9da-239">(7)</span><span class="sxs-lookup"><span data-stu-id="3a9da-239">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="3a9da-240"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="3a9da-240"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="3a9da-241">(8)</span><span class="sxs-lookup"><span data-stu-id="3a9da-241">(8)</span></span>


</dt> <dd>

<span data-ttu-id="3a9da-242">Das Treiber Lade Modul für das Gerät fehlt.</span><span class="sxs-lookup"><span data-stu-id="3a9da-242">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="3a9da-243"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="3a9da-243"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="3a9da-244">(9)</span><span class="sxs-lookup"><span data-stu-id="3a9da-244">(9)</span></span>


</dt> <dd>

<span data-ttu-id="3a9da-245">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="3a9da-245">Device is not working properly.</span></span> <span data-ttu-id="3a9da-246">Die Steuerungs Firmware meldet nicht korrekt die Ressourcen für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="3a9da-246">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="3a9da-247"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="3a9da-247"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="3a9da-248">(10)</span><span class="sxs-lookup"><span data-stu-id="3a9da-248">(10)</span></span>


</dt> <dd>

<span data-ttu-id="3a9da-249">Das Gerät kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="3a9da-249">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="3a9da-250"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="3a9da-250"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="3a9da-251">(11)</span><span class="sxs-lookup"><span data-stu-id="3a9da-251">(11)</span></span>


</dt> <dd>

<span data-ttu-id="3a9da-252">Fehler beim Gerät.</span><span class="sxs-lookup"><span data-stu-id="3a9da-252">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="3a9da-253"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="3a9da-253"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="3a9da-254">(12)</span><span class="sxs-lookup"><span data-stu-id="3a9da-254">(12)</span></span>


</dt> <dd>

<span data-ttu-id="3a9da-255">Das Gerät kann nicht genug freie Ressourcen für die Verwendung finden.</span><span class="sxs-lookup"><span data-stu-id="3a9da-255">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="3a9da-256"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="3a9da-256"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="3a9da-257">(13)</span><span class="sxs-lookup"><span data-stu-id="3a9da-257">(13)</span></span>


</dt> <dd>

<span data-ttu-id="3a9da-258">Die Geräte Ressourcen können nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="3a9da-258">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="3a9da-259"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="3a9da-259"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="3a9da-260">(14)</span><span class="sxs-lookup"><span data-stu-id="3a9da-260">(14)</span></span>


</dt> <dd>

<span data-ttu-id="3a9da-261">Das Gerät kann erst ordnungsgemäß funktionieren, wenn der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="3a9da-261">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="3a9da-262"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="3a9da-262"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="3a9da-263">(15)</span><span class="sxs-lookup"><span data-stu-id="3a9da-263">(15)</span></span>


</dt> <dd>

<span data-ttu-id="3a9da-264">Das Gerät funktioniert aufgrund eines möglichen erneuten Aufzählungs Problems nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="3a9da-264">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="3a9da-265"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="3a9da-265"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="3a9da-266">(16)</span><span class="sxs-lookup"><span data-stu-id="3a9da-266">(16)</span></span>


</dt> <dd>

<span data-ttu-id="3a9da-267">In Windows können nicht alle Ressourcen identifiziert werden, die vom Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3a9da-267">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="3a9da-268"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="3a9da-268"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="3a9da-269">(17)</span><span class="sxs-lookup"><span data-stu-id="3a9da-269">(17)</span></span>


</dt> <dd>

<span data-ttu-id="3a9da-270">Das Gerät fordert einen unbekannten Ressourcentyp an.</span><span class="sxs-lookup"><span data-stu-id="3a9da-270">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="3a9da-271"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="3a9da-271"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="3a9da-272">(18)</span><span class="sxs-lookup"><span data-stu-id="3a9da-272">(18)</span></span>


</dt> <dd>

<span data-ttu-id="3a9da-273">Gerätetreiber müssen neu installiert werden.</span><span class="sxs-lookup"><span data-stu-id="3a9da-273">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="3a9da-274"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="3a9da-274"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="3a9da-275">(19)</span><span class="sxs-lookup"><span data-stu-id="3a9da-275">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="3a9da-276"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="3a9da-276"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="3a9da-277">(20)</span><span class="sxs-lookup"><span data-stu-id="3a9da-277">(20)</span></span>


</dt> <dd>

<span data-ttu-id="3a9da-278">Die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="3a9da-278">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="3a9da-279"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="3a9da-279"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="3a9da-280">(21)</span><span class="sxs-lookup"><span data-stu-id="3a9da-280">(21)</span></span>


</dt> <dd>

<span data-ttu-id="3a9da-281">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="3a9da-281">System failure.</span></span> <span data-ttu-id="3a9da-282">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="3a9da-282">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="3a9da-283">Das Gerät wird von Windows entfernt.</span><span class="sxs-lookup"><span data-stu-id="3a9da-283">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="3a9da-284"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="3a9da-284"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="3a9da-285">(22)</span><span class="sxs-lookup"><span data-stu-id="3a9da-285">(22)</span></span>


</dt> <dd>

<span data-ttu-id="3a9da-286">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="3a9da-286">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="3a9da-287"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="3a9da-287"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="3a9da-288">(23)</span><span class="sxs-lookup"><span data-stu-id="3a9da-288">(23)</span></span>


</dt> <dd>

<span data-ttu-id="3a9da-289">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="3a9da-289">System failure.</span></span> <span data-ttu-id="3a9da-290">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="3a9da-290">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="3a9da-291"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="3a9da-291"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="3a9da-292">(24)</span><span class="sxs-lookup"><span data-stu-id="3a9da-292">(24)</span></span>


</dt> <dd>

<span data-ttu-id="3a9da-293">Das Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.</span><span class="sxs-lookup"><span data-stu-id="3a9da-293">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="3a9da-294"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="3a9da-294"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="3a9da-295">(25)</span><span class="sxs-lookup"><span data-stu-id="3a9da-295">(25)</span></span>


</dt> <dd>

<span data-ttu-id="3a9da-296">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="3a9da-296">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="3a9da-297"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="3a9da-297"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="3a9da-298">(26)</span><span class="sxs-lookup"><span data-stu-id="3a9da-298">(26)</span></span>


</dt> <dd>

<span data-ttu-id="3a9da-299">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="3a9da-299">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="3a9da-300"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="3a9da-300"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="3a9da-301">(27)</span><span class="sxs-lookup"><span data-stu-id="3a9da-301">(27)</span></span>


</dt> <dd>

<span data-ttu-id="3a9da-302">Das Gerät verfügt nicht über eine gültige Protokoll Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="3a9da-302">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="3a9da-303"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="3a9da-303"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="3a9da-304">(28)</span><span class="sxs-lookup"><span data-stu-id="3a9da-304">(28)</span></span>


</dt> <dd>

<span data-ttu-id="3a9da-305">Gerätetreiber sind nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="3a9da-305">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="3a9da-306"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="3a9da-306"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="3a9da-307">(29)</span><span class="sxs-lookup"><span data-stu-id="3a9da-307">(29)</span></span>


</dt> <dd>

<span data-ttu-id="3a9da-308">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="3a9da-308">Device is disabled.</span></span> <span data-ttu-id="3a9da-309">Die Gerätefirmware hat nicht die erforderlichen Ressourcen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="3a9da-309">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="3a9da-310"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="3a9da-310"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="3a9da-311">(30)</span><span class="sxs-lookup"><span data-stu-id="3a9da-311">(30)</span></span>


</dt> <dd>

<span data-ttu-id="3a9da-312">Das Gerät verwendet eine UNQ-Ressource, die von einem anderen Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3a9da-312">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="3a9da-313"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="3a9da-313"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="3a9da-314">31,5</span><span class="sxs-lookup"><span data-stu-id="3a9da-314">(31)</span></span>


</dt> <dd>

<span data-ttu-id="3a9da-315">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="3a9da-315">Device is not working properly.</span></span> <span data-ttu-id="3a9da-316">Die erforderlichen Gerätetreiber können nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="3a9da-316">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3a9da-317">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="3a9da-317">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a9da-318">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="3a9da-318">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-319">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a9da-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-320">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="3a9da-320">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="3a9da-321">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="3a9da-321">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="3a9da-322">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3a9da-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a9da-323">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="3a9da-323">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a9da-324">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3a9da-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-325">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a9da-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-326">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3a9da-326">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3a9da-327">Der Name der ersten konkreten Klasse, die in der Vererbungs Kette angezeigt werden soll, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3a9da-327">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="3a9da-328">Bei Verwendung mit den anderen Schlüsseleigenschaften der-Klasse ermöglicht die-Eigenschaft, dass alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="3a9da-328">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="3a9da-329">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3a9da-329">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a9da-330">**Defaultblocksize**</span><span class="sxs-lookup"><span data-stu-id="3a9da-330">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a9da-331">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3a9da-331">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-332">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a9da-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-333">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="3a9da-333">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="3a9da-334">Standard Blockgröße (in Bytes) für dieses Gerät.</span><span class="sxs-lookup"><span data-stu-id="3a9da-334">Default block size, in bytes, for this device.</span></span>

<span data-ttu-id="3a9da-335">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3a9da-335">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="3a9da-336">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="3a9da-336">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="3a9da-337">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3a9da-337">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a9da-338">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3a9da-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-339">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a9da-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-340">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="3a9da-340">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="3a9da-341">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="3a9da-341">Description of the object.</span></span>

<span data-ttu-id="3a9da-342">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3a9da-342">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a9da-343">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="3a9da-343">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a9da-344">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3a9da-344">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-345">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a9da-345">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-346">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("toviceid"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="3a9da-346">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="3a9da-347">Eindeutiger Bezeichner des Laufwerks mit anderen Geräten im System.</span><span class="sxs-lookup"><span data-stu-id="3a9da-347">Unique identifier of the disk drive with other devices on the system.</span></span>

<span data-ttu-id="3a9da-348">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3a9da-348">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a9da-349">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="3a9da-349">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a9da-350">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="3a9da-350">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-351">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a9da-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a9da-352">**True** gibt an, dass der in **LastErrorCode** gemeldete Fehler jetzt gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="3a9da-352">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="3a9da-353">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3a9da-353">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a9da-354">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="3a9da-354">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a9da-355">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3a9da-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-356">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a9da-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a9da-357">Weitere Informationen zu dem Fehler, der in " **LastErrorCode**" aufgezeichnet wurde, sowie Informationen zu ggf. getroffenen Korrekturmaßnahmen.</span><span class="sxs-lookup"><span data-stu-id="3a9da-357">More information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="3a9da-358">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3a9da-358">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a9da-359">**Errormethodmethodologie**</span><span class="sxs-lookup"><span data-stu-id="3a9da-359">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a9da-360">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3a9da-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-361">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a9da-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a9da-362">Typ der Fehlererkennung und-Korrektur, die von diesem Gerät unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="3a9da-362">Type of error detection and correction supported by this device.</span></span>

<span data-ttu-id="3a9da-363">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3a9da-363">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a9da-364">**Firmwarerevision**</span><span class="sxs-lookup"><span data-stu-id="3a9da-364">**FirmwareRevision**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a9da-365">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3a9da-365">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-366">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a9da-366">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-367">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Input and Output Structures \| [**Storage \_ Device \_ Descriptor**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor) \| productrevisionoffset")</span><span class="sxs-lookup"><span data-stu-id="3a9da-367">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**STORAGE\_DEVICE\_DESCRIPTOR**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor)\|ProductRevisionOffset")</span></span>
</dt> </dl>

<span data-ttu-id="3a9da-368">Revision der Laufwerks Firmware, die vom Hersteller zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="3a9da-368">Revision for the disk drive firmware that is assigned by the manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="3a9da-369">**Index**</span><span class="sxs-lookup"><span data-stu-id="3a9da-369">**Index**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a9da-370">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3a9da-370">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-371">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a9da-371">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-372">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Windows 95/98 Functions \| Drive \_ map \_ Info \| btInt13Unit")</span><span class="sxs-lookup"><span data-stu-id="3a9da-372">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Windows 95/98 Functions\|DRIVE\_MAP\_INFO\|btInt13Unit")</span></span>
</dt> </dl>

<span data-ttu-id="3a9da-373">Die Nummer des physischen Laufwerks des angegebenen Laufwerks.</span><span class="sxs-lookup"><span data-stu-id="3a9da-373">Physical drive number of the given drive.</span></span> <span data-ttu-id="3a9da-374">Diese Eigenschaft wird von der Struktur der [**Speicher \_ Geräte \_ Nummer**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_number) aufgefüllt, die aus dem IOCTL-Speicher Ablaufsteuerungs-Code für [**\_ \_ \_ Geräte \_ Nummern**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_get_device_number) zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="3a9da-374">This property is filled by the [**STORAGE\_DEVICE\_NUMBER**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_number) structure returned from the [**IOCTL\_STORAGE\_GET\_DEVICE\_NUMBER**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_get_device_number) control code.</span></span> <span data-ttu-id="3a9da-375">Der Wert 0xFFFFFFFF gibt an, dass das angegebene Laufwerk keinem physischen Laufwerk zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3a9da-375">A value of 0xffffffff indicates that the given drive does not map to a physical drive.</span></span>

<span data-ttu-id="3a9da-376">Beispiel: 1</span><span class="sxs-lookup"><span data-stu-id="3a9da-376">Example: 1</span></span>

</dd> <dt>

<span data-ttu-id="3a9da-377">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="3a9da-377">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a9da-378">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="3a9da-378">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-379">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a9da-379">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-380">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="3a9da-380">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="3a9da-381">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="3a9da-381">Date and time the object was installed.</span></span> <span data-ttu-id="3a9da-382">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="3a9da-382">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="3a9da-383">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3a9da-383">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a9da-384">**InterfaceType**</span><span class="sxs-lookup"><span data-stu-id="3a9da-384">**InterfaceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a9da-385">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3a9da-385">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-386">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a9da-386">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-387">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Input and Output Functions \| [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)")</span><span class="sxs-lookup"><span data-stu-id="3a9da-387">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Functions\|[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)")</span></span>
</dt> </dl>

<span data-ttu-id="3a9da-388">Der Schnittstellentyp des physischen Laufwerks.</span><span class="sxs-lookup"><span data-stu-id="3a9da-388">Interface type of physical disk drive.</span></span>

<span data-ttu-id="3a9da-389">Die Werte sind:</span><span class="sxs-lookup"><span data-stu-id="3a9da-389">The values are:</span></span>

<span data-ttu-id="3a9da-390">SCSI</span><span class="sxs-lookup"><span data-stu-id="3a9da-390">SCSI</span></span>

<span data-ttu-id="3a9da-391">HDC</span><span class="sxs-lookup"><span data-stu-id="3a9da-391">HDC</span></span>

<span data-ttu-id="3a9da-392">IDE</span><span class="sxs-lookup"><span data-stu-id="3a9da-392">IDE</span></span>

<span data-ttu-id="3a9da-393">USB</span><span class="sxs-lookup"><span data-stu-id="3a9da-393">USB</span></span>

<span data-ttu-id="3a9da-394">1394</span><span class="sxs-lookup"><span data-stu-id="3a9da-394">1394</span></span>

</dd> <dt>

<span data-ttu-id="3a9da-395">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="3a9da-395">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a9da-396">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3a9da-396">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-397">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a9da-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a9da-398">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="3a9da-398">Last error code reported by the logical device.</span></span>

<span data-ttu-id="3a9da-399">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3a9da-399">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a9da-400">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="3a9da-400">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a9da-401">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3a9da-401">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-402">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a9da-402">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-403">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ Hardware \\ \\ DeviceMap \\ \\ SCSI \\ \\ SCSI Port \\ \\ SCSI Bus \\ \\ Target ID \\ \\ Logical Unit ID \\ \\ Identifier", "Win32Registry \| Manufacturer")</span><span class="sxs-lookup"><span data-stu-id="3a9da-403">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\HARDWARE\\\\DEVICEMAP\\\\Scsi\\\\Scsi Port\\\\Scsi Bus\\\\Target Id\\\\Logical Unit Id\\\\Identifier", "Win32Registry\|Manufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="3a9da-404">Der Name des Laufwerks Herstellers.</span><span class="sxs-lookup"><span data-stu-id="3a9da-404">Name of the disk drive manufacturer.</span></span>

<span data-ttu-id="3a9da-405">Beispiel: "abachat"</span><span class="sxs-lookup"><span data-stu-id="3a9da-405">Example: "Seagate"</span></span>

</dd> <dt>

<span data-ttu-id="3a9da-406">**Maxblocksize**</span><span class="sxs-lookup"><span data-stu-id="3a9da-406">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a9da-407">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3a9da-407">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-408">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a9da-408">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-409">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="3a9da-409">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="3a9da-410">Maximale Blockgröße (in Bytes) für Medien, auf die dieses Gerät zugreift.</span><span class="sxs-lookup"><span data-stu-id="3a9da-410">Maximum block size, in bytes, for media accessed by this device.</span></span>

<span data-ttu-id="3a9da-411">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3a9da-411">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="3a9da-412">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="3a9da-412">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="3a9da-413">**Maxmediasize**</span><span class="sxs-lookup"><span data-stu-id="3a9da-413">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a9da-414">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3a9da-414">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-415">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a9da-415">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-416">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| sequenzielle Zugriffsgeräte \| 001,2 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Kilobyte ")</span><span class="sxs-lookup"><span data-stu-id="3a9da-416">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="3a9da-417">Maximale Mediengröße der von diesem Gerät unterstützten Medien in Kilobyte.</span><span class="sxs-lookup"><span data-stu-id="3a9da-417">Maximum media size, in kilobytes, of media supported by this device.</span></span>

<span data-ttu-id="3a9da-418">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3a9da-418">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="3a9da-419">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="3a9da-419">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="3a9da-420">**MediaLoaded**</span><span class="sxs-lookup"><span data-stu-id="3a9da-420">**MediaLoaded**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a9da-421">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="3a9da-421">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-422">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a9da-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-423">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Input and Output Structures \| [**Disk \_ Geometry**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| mediaType \| fixedmedia")</span><span class="sxs-lookup"><span data-stu-id="3a9da-423">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|MediaType\|FixedMedia")</span></span>
</dt> </dl>

<span data-ttu-id="3a9da-424">Wenn der Wert **true** ist, werden die Medien für ein Laufwerk geladen, was bedeutet, dass das Gerät über ein lesbares Dateisystem verfügt und darauf zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="3a9da-424">If **True**, the media for a disk drive is loaded, which means that the device has a readable file system and is accessible.</span></span> <span data-ttu-id="3a9da-425">Bei Festplatten Laufwerken ist diese Eigenschaft immer " **true**".</span><span class="sxs-lookup"><span data-stu-id="3a9da-425">For fixed disk drives, this property will always be **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="3a9da-426">**MediaType**</span><span class="sxs-lookup"><span data-stu-id="3a9da-426">**MediaType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a9da-427">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3a9da-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-428">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a9da-428">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-429">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Input and Output Structures \| [**Disk \_ Geometry**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| MediaType")</span><span class="sxs-lookup"><span data-stu-id="3a9da-429">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|MediaType")</span></span>
</dt> </dl>

<span data-ttu-id="3a9da-430">Typ des Mediums, das von diesem Gerät verwendet oder aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="3a9da-430">Type of media used or accessed by this device.</span></span>

<span data-ttu-id="3a9da-431">Dabei sind folgende Werte möglich:</span><span class="sxs-lookup"><span data-stu-id="3a9da-431">Possible values are:</span></span>

<dt>

<span id="External_hard_disk_media"></span><span id="external_hard_disk_media"></span><span id="EXTERNAL_HARD_DISK_MEDIA"></span>

<span data-ttu-id="3a9da-432">**Externes Festplatten Medium**</span><span class="sxs-lookup"><span data-stu-id="3a9da-432">**External hard disk media**</span></span>


</dt> <dd></dd> <dt>

<span id="Removable_media"></span><span id="removable_media"></span><span id="REMOVABLE_MEDIA"></span>

<span data-ttu-id="3a9da-433">Wechsel **Medium** ("Wechsel Datenträger als Disketten")</span><span class="sxs-lookup"><span data-stu-id="3a9da-433">**Removable media** ("Removable media other than floppy")</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed_hard_disk"></span><span id="fixed_hard_disk"></span><span id="FIXED_HARD_DISK"></span>

<span data-ttu-id="3a9da-434">Fest **Platte Festplatte** ("Festplatten Medium")</span><span class="sxs-lookup"><span data-stu-id="3a9da-434">**Fixed hard disk** ("Fixed hard disk media")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3a9da-435">**Unknown** ("Format ist unbekannt")</span><span class="sxs-lookup"><span data-stu-id="3a9da-435">**Unknown** ("Format is unknown")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3a9da-436">**Minblocksize**</span><span class="sxs-lookup"><span data-stu-id="3a9da-436">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a9da-437">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3a9da-437">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-438">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a9da-438">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-439">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="3a9da-439">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="3a9da-440">Minimale Blockgröße (in Bytes) für Medien, auf die dieses Gerät zugreift.</span><span class="sxs-lookup"><span data-stu-id="3a9da-440">Minimum block size, in bytes, for media accessed by this device.</span></span>

<span data-ttu-id="3a9da-441">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3a9da-441">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="3a9da-442">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="3a9da-442">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="3a9da-443">**Modell**</span><span class="sxs-lookup"><span data-stu-id="3a9da-443">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a9da-444">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3a9da-444">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-445">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a9da-445">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-446">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ Hardware \\ \\ DeviceMap \\ \\ SCSI \\ \\ SCSI Port \\ \\ SCSI Bus \\ \\ Target ID \\ \\ Logical Unit ID \\ \\ Identifier", "Win32Registry \| ProductID")</span><span class="sxs-lookup"><span data-stu-id="3a9da-446">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\HARDWARE\\\\DEVICEMAP\\\\Scsi\\\\Scsi Port\\\\Scsi Bus\\\\Target Id\\\\Logical Unit Id\\\\Identifier", "Win32Registry\|ProductId")</span></span>
</dt> </dl>

<span data-ttu-id="3a9da-447">Die Modellnummer des Herstellers des Laufwerks.</span><span class="sxs-lookup"><span data-stu-id="3a9da-447">Manufacturer's model number of the disk drive.</span></span>

<span data-ttu-id="3a9da-448">Beispiel: "ST32171W"</span><span class="sxs-lookup"><span data-stu-id="3a9da-448">Example: "ST32171W"</span></span>

</dd> <dt>

<span data-ttu-id="3a9da-449">**Name**</span><span class="sxs-lookup"><span data-stu-id="3a9da-449">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a9da-450">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3a9da-450">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-451">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a9da-451">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-452">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="3a9da-452">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="3a9da-453">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="3a9da-453">Label by which the object is known.</span></span> <span data-ttu-id="3a9da-454">Bei einer Unterklasse kann die Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="3a9da-454">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="3a9da-455">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3a9da-455">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a9da-456">**Unnötig**</span><span class="sxs-lookup"><span data-stu-id="3a9da-456">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a9da-457">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="3a9da-457">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-458">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a9da-458">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a9da-459">**True** gibt an, dass das Medien Zugriffsgerät bereinigt werden muss.</span><span class="sxs-lookup"><span data-stu-id="3a9da-459">If **True**, the media access device needs cleaning.</span></span> <span data-ttu-id="3a9da-460">Ob manuelle oder automatische Bereinigung möglich ist, wird in der Eigenschaft **Funktionen** angegeben.</span><span class="sxs-lookup"><span data-stu-id="3a9da-460">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** property.</span></span>

<span data-ttu-id="3a9da-461">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3a9da-461">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a9da-462">**"Numofmediasupportiert"**</span><span class="sxs-lookup"><span data-stu-id="3a9da-462">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a9da-463">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3a9da-463">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-464">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a9da-464">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a9da-465">Maximale Anzahl von Medien, die unterstützt oder eingefügt werden können (wenn das Medien Zugriffsgerät mehrere einzelne Medien unterstützt).</span><span class="sxs-lookup"><span data-stu-id="3a9da-465">Maximum number of media which can be supported or inserted (when the media access device supports multiple individual media).</span></span>

<span data-ttu-id="3a9da-466">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3a9da-466">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a9da-467">**Partitionen**</span><span class="sxs-lookup"><span data-stu-id="3a9da-467">**Partitions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a9da-468">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3a9da-468">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-469">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a9da-469">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-470">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Input and Output Structures \| [**Partition \_ Information**](/windows/desktop/api/winioctl/ns-winioctl-partition_information) \| erkenzedpartition")</span><span class="sxs-lookup"><span data-stu-id="3a9da-470">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**PARTITION\_INFORMATION**](/windows/desktop/api/winioctl/ns-winioctl-partition_information)\|RecognizedPartition")</span></span>
</dt> </dl>

<span data-ttu-id="3a9da-471">Anzahl der Partitionen auf diesem physischen Laufwerk, die vom Betriebssystem erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="3a9da-471">Number of partitions on this physical disk drive that are recognized by the operating system.</span></span>

<span data-ttu-id="3a9da-472">Beispiel: 2</span><span class="sxs-lookup"><span data-stu-id="3a9da-472">Example: 2</span></span>

</dd> <dt>

<span data-ttu-id="3a9da-473">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="3a9da-473">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a9da-474">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3a9da-474">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-475">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a9da-475">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-476">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="3a9da-476">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="3a9da-477">Windows Plug & Play Geräte Bezeichner des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="3a9da-477">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="3a9da-478">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3a9da-478">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="3a9da-479">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="3a9da-479">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="3a9da-480">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="3a9da-480">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a9da-481">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="3a9da-481">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-482">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a9da-482">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a9da-483">Array der spezifischen energiebezogenen Funktionen eines logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="3a9da-483">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="3a9da-484">Diese Eigenschaft wird von **CIM \_ LogicalDevice** geerbt.</span><span class="sxs-lookup"><span data-stu-id="3a9da-484">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3a9da-485"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="3a9da-485"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="3a9da-486"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="3a9da-486"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="3a9da-487">Energiebezogene Kapazitäten werden für dieses Gerät nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3a9da-487">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="3a9da-488"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="3a9da-488"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="3a9da-489"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="3a9da-489"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="3a9da-490">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3a9da-490">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="3a9da-491"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="3a9da-491"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="3a9da-492">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="3a9da-492">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="3a9da-493"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="3a9da-493"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="3a9da-494">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3a9da-494">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="3a9da-495">Diese Methode wird in der übergeordneten [**CIM \_ LogicalDevice**](cim-logicaldevice.md) -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="3a9da-495">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="3a9da-496">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="3a9da-496">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="3a9da-497"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="3a9da-497"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="3a9da-498">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="3a9da-498">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="3a9da-499"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="3a9da-499"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="3a9da-500">Zeitgesteuerte Power-On unterstützt</span><span class="sxs-lookup"><span data-stu-id="3a9da-500">Timed Power-On Supported</span></span>

<span data-ttu-id="3a9da-501">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) und die *Uhrzeit* auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="3a9da-501">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3a9da-502">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="3a9da-502">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a9da-503">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="3a9da-503">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-504">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a9da-504">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a9da-505">Wenn der Wert **true** ist, kann das Gerät Energie gesteuert werden (kann in den Unterbrechungs Modus versetzt werden usw.).</span><span class="sxs-lookup"><span data-stu-id="3a9da-505">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="3a9da-506">Die-Eigenschaft gibt nicht an, dass die Energie Verwaltungsfunktionen zurzeit aktiviert sind, sondern nur, dass das logische Gerät für die Energie Verwaltung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="3a9da-506">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="3a9da-507">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3a9da-507">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a9da-508">**SCSIBus**</span><span class="sxs-lookup"><span data-stu-id="3a9da-508">**SCSIBus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a9da-509">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3a9da-509">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-510">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a9da-510">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-511">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Input and Output Structures \| [**SCSI \_ Address**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address) \| pathid")</span><span class="sxs-lookup"><span data-stu-id="3a9da-511">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**SCSI\_ADDRESS**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address)\|PathId")</span></span>
</dt> </dl>

<span data-ttu-id="3a9da-512">SCSI-Bus-Nummer des Laufwerks.</span><span class="sxs-lookup"><span data-stu-id="3a9da-512">SCSI bus number of the disk drive.</span></span>

<span data-ttu-id="3a9da-513">Beispiel: 0</span><span class="sxs-lookup"><span data-stu-id="3a9da-513">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="3a9da-514">**SCSILogicalUnit**</span><span class="sxs-lookup"><span data-stu-id="3a9da-514">**SCSILogicalUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a9da-515">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a9da-515">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-516">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a9da-516">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-517">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Input and Output Structures \| [**SCSI \_ Address**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address) \| LUN")</span><span class="sxs-lookup"><span data-stu-id="3a9da-517">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**SCSI\_ADDRESS**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address)\|Lun")</span></span>
</dt> </dl>

<span data-ttu-id="3a9da-518">Die SCSI-logische Gerätenummer (LUN) des Laufwerks.</span><span class="sxs-lookup"><span data-stu-id="3a9da-518">SCSI logical unit number (LUN) of the disk drive.</span></span>

<span data-ttu-id="3a9da-519">Beispiel: 0</span><span class="sxs-lookup"><span data-stu-id="3a9da-519">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="3a9da-520">**SCSIPort**</span><span class="sxs-lookup"><span data-stu-id="3a9da-520">**SCSIPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a9da-521">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a9da-521">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-522">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a9da-522">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-523">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Input and Output Structures \| [**SCSI \_ Address**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address) \| PortNumber")</span><span class="sxs-lookup"><span data-stu-id="3a9da-523">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**SCSI\_ADDRESS**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address)\|PortNumber")</span></span>
</dt> </dl>

<span data-ttu-id="3a9da-524">SCSI-Portnummer des Laufwerks.</span><span class="sxs-lookup"><span data-stu-id="3a9da-524">SCSI port number of the disk drive.</span></span>

<span data-ttu-id="3a9da-525">Beispiel: 0</span><span class="sxs-lookup"><span data-stu-id="3a9da-525">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="3a9da-526">**SCSITargetId**</span><span class="sxs-lookup"><span data-stu-id="3a9da-526">**SCSITargetId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a9da-527">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a9da-527">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-528">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a9da-528">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-529">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Input and Output Structures \| [**SCSI \_ Address**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address) \| targetID")</span><span class="sxs-lookup"><span data-stu-id="3a9da-529">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**SCSI\_ADDRESS**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address)\|TargetId")</span></span>
</dt> </dl>

<span data-ttu-id="3a9da-530">SCSI-Bezeichnernummer des Laufwerks.</span><span class="sxs-lookup"><span data-stu-id="3a9da-530">SCSI identifier number of the disk drive.</span></span>

<span data-ttu-id="3a9da-531">Beispiel: 0</span><span class="sxs-lookup"><span data-stu-id="3a9da-531">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="3a9da-532">**Sector-Spur**</span><span class="sxs-lookup"><span data-stu-id="3a9da-532">**SectorsPerTrack**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a9da-533">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3a9da-533">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-534">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a9da-534">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-535">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Input and Output Structures \| [**Disk \_ Geometry**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| Sector spertrack")</span><span class="sxs-lookup"><span data-stu-id="3a9da-535">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|SectorsPerTrack")</span></span>
</dt> </dl>

<span data-ttu-id="3a9da-536">Anzahl der Sektoren in jeder Spur für dieses physische Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="3a9da-536">Number of sectors in each track for this physical disk drive.</span></span>

<span data-ttu-id="3a9da-537">Beispiel: 63</span><span class="sxs-lookup"><span data-stu-id="3a9da-537">Example: 63</span></span>

</dd> <dt>

<span data-ttu-id="3a9da-538">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="3a9da-538">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a9da-539">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3a9da-539">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-540">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a9da-540">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-541">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Input and Output Structures \| [**Storage \_ Device \_ Descriptor**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor) \| serialnummerioffset")</span><span class="sxs-lookup"><span data-stu-id="3a9da-541">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**STORAGE\_DEVICE\_DESCRIPTOR**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor)\|SerialNumberOffset")</span></span>
</dt> </dl>

<span data-ttu-id="3a9da-542">Die Nummer, die vom Hersteller zum Identifizieren der physischen Medien zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="3a9da-542">Number allocated by the manufacturer to identify the physical media.</span></span>

<span data-ttu-id="3a9da-543">Beispiel: WD-WM3493798728</span><span class="sxs-lookup"><span data-stu-id="3a9da-543">Example: WD-WM3493798728</span></span>

</dd> <dt>

<span data-ttu-id="3a9da-544">**Signature**</span><span class="sxs-lookup"><span data-stu-id="3a9da-544">**Signature**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a9da-545">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3a9da-545">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-546">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a9da-546">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-547">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Input and Output Structures \| [**Laufwerk \_ \_ Layoutinformationen**](/windows/desktop/api/winioctl/ns-winioctl-drive_layout_information) \| Signature")</span><span class="sxs-lookup"><span data-stu-id="3a9da-547">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DRIVE\_LAYOUT\_INFORMATION**](/windows/desktop/api/winioctl/ns-winioctl-drive_layout_information)\|Signature")</span></span>
</dt> </dl>

<span data-ttu-id="3a9da-548">Datenträger Identifikation.</span><span class="sxs-lookup"><span data-stu-id="3a9da-548">Disk identification.</span></span> <span data-ttu-id="3a9da-549">Diese Eigenschaft kann verwendet werden, um eine freigegebene Ressource zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="3a9da-549">This property can be used to identify a shared resource.</span></span>

</dd> <dt>

<span data-ttu-id="3a9da-550">**Größe**</span><span class="sxs-lookup"><span data-stu-id="3a9da-550">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a9da-551">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3a9da-551">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-552">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a9da-552">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-553">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Input and Output Structures \| [**Disk \_ Geometry**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="3a9da-553">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)"), [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="3a9da-554">Größe des Laufwerks.</span><span class="sxs-lookup"><span data-stu-id="3a9da-554">Size of the disk drive.</span></span> <span data-ttu-id="3a9da-555">Er wird berechnet, indem die Gesamtzahl der Zylinder, die Spuren in den einzelnen Zylinder, die Sektoren in den einzelnen Spuren und die Bytes in den einzelnen Sektoren multipliziert werden.</span><span class="sxs-lookup"><span data-stu-id="3a9da-555">It is calculated by multiplying the total number of cylinders, tracks in each cylinder, sectors in each track, and bytes in each sector.</span></span>

<span data-ttu-id="3a9da-556">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="3a9da-556">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="3a9da-557">**Status**</span><span class="sxs-lookup"><span data-stu-id="3a9da-557">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a9da-558">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3a9da-558">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-559">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a9da-559">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-560">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="3a9da-560">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="3a9da-561">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="3a9da-561">Current status of the object.</span></span> <span data-ttu-id="3a9da-562">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="3a9da-562">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="3a9da-563">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="3a9da-563">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="3a9da-564">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="3a9da-564">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="3a9da-565">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="3a9da-565">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="3a9da-566">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="3a9da-566">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="3a9da-567">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3a9da-567">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="3a9da-568">Gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="3a9da-568">Values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="3a9da-569">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="3a9da-569">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="3a9da-570">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="3a9da-570">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="3a9da-571">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="3a9da-571">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3a9da-572">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="3a9da-572">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="3a9da-573">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="3a9da-573">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="3a9da-574">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="3a9da-574">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="3a9da-575">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="3a9da-575">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="3a9da-576">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="3a9da-576">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="3a9da-577">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="3a9da-577">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="3a9da-578">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="3a9da-578">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="3a9da-579">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="3a9da-579">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="3a9da-580">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="3a9da-580">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3a9da-581">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="3a9da-581">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a9da-582">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a9da-582">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-583">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a9da-583">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-584">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="3a9da-584">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="3a9da-585">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="3a9da-585">State of the logical device.</span></span> <span data-ttu-id="3a9da-586">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 (nicht zutreffend) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3a9da-586">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="3a9da-587">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3a9da-587">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3a9da-588">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="3a9da-588">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3a9da-589">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="3a9da-589">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="3a9da-590">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="3a9da-590">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="3a9da-591">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="3a9da-591">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="3a9da-592">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="3a9da-592">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3a9da-593">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="3a9da-593">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a9da-594">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3a9da-594">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-595">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a9da-595">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-596">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3a9da-596">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3a9da-597">Der Wert der Eigenschaft " **kreationclassname** " des Bereichs Computers.</span><span class="sxs-lookup"><span data-stu-id="3a9da-597">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="3a9da-598">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3a9da-598">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a9da-599">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="3a9da-599">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a9da-600">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3a9da-600">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-601">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a9da-601">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-602">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3a9da-602">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3a9da-603">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="3a9da-603">Name of the scoping system.</span></span>

<span data-ttu-id="3a9da-604">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="3a9da-604">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a9da-605">**TotalCylinders**</span><span class="sxs-lookup"><span data-stu-id="3a9da-605">**TotalCylinders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a9da-606">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3a9da-606">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-607">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a9da-607">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-608">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Input and Output Structures \| [**Disk \_ Geometry**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| Zylinder")</span><span class="sxs-lookup"><span data-stu-id="3a9da-608">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|Cylinders")</span></span>
</dt> </dl>

<span data-ttu-id="3a9da-609">Die Gesamtanzahl der Zylinder auf dem physischen Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="3a9da-609">Total number of cylinders on the physical disk drive.</span></span> <span data-ttu-id="3a9da-610">Hinweis: der Wert für diese Eigenschaft wird durch erweiterte Funktionen der BIOS-Interruptzeit 13 h abgerufen.</span><span class="sxs-lookup"><span data-stu-id="3a9da-610">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="3a9da-611">Der Wert kann ungenau sein, wenn das Laufwerk ein Übersetzungs Schema verwendet, um Festplattengrößen mit hoher Kapazität zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="3a9da-611">The value may be inaccurate if the drive uses a translation scheme to support high-capacity disk sizes.</span></span> <span data-ttu-id="3a9da-612">Informieren Sie sich beim Hersteller über genaue Laufwerk Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="3a9da-612">Consult the manufacturer for accurate drive specifications.</span></span>

<span data-ttu-id="3a9da-613">Beispiel: 657</span><span class="sxs-lookup"><span data-stu-id="3a9da-613">Example: 657</span></span>

<span data-ttu-id="3a9da-614">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="3a9da-614">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="3a9da-615">**TotalHeads**</span><span class="sxs-lookup"><span data-stu-id="3a9da-615">**TotalHeads**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a9da-616">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3a9da-616">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-617">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a9da-617">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-618">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Input and Output Structures \| [**Disk \_ Geometry**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| tracksperzylinder")</span><span class="sxs-lookup"><span data-stu-id="3a9da-618">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|TracksPerCylinder")</span></span>
</dt> </dl>

<span data-ttu-id="3a9da-619">Die Gesamtanzahl der Köpfe auf dem Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="3a9da-619">Total number of heads on the disk drive.</span></span> <span data-ttu-id="3a9da-620">Hinweis: der Wert für diese Eigenschaft wird durch erweiterte Funktionen der BIOS-Interruptzeit 13 h abgerufen.</span><span class="sxs-lookup"><span data-stu-id="3a9da-620">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="3a9da-621">Der Wert kann ungenau sein, wenn das Laufwerk ein Übersetzungs Schema verwendet, um Festplattengrößen mit hoher Kapazität zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="3a9da-621">The value may be inaccurate if the drive uses a translation scheme to support high-capacity disk sizes.</span></span> <span data-ttu-id="3a9da-622">Informieren Sie sich beim Hersteller über genaue Laufwerk Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="3a9da-622">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> <dt>

<span data-ttu-id="3a9da-623">**TotalSectors**</span><span class="sxs-lookup"><span data-stu-id="3a9da-623">**TotalSectors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a9da-624">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3a9da-624">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-625">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a9da-625">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-626">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Input and Output Structures \| [**Disk \_ Geometry**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| Sector spertrack")</span><span class="sxs-lookup"><span data-stu-id="3a9da-626">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|SectorsPerTrack")</span></span>
</dt> </dl>

<span data-ttu-id="3a9da-627">Gesamtanzahl der Sektoren auf dem physischen Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="3a9da-627">Total number of sectors on the physical disk drive.</span></span> <span data-ttu-id="3a9da-628">Hinweis: der Wert für diese Eigenschaft wird durch erweiterte Funktionen der BIOS-Interruptzeit 13 h abgerufen.</span><span class="sxs-lookup"><span data-stu-id="3a9da-628">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="3a9da-629">Der Wert kann ungenau sein, wenn das Laufwerk ein Übersetzungs Schema verwendet, um Festplattengrößen mit hoher Kapazität zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="3a9da-629">The value may be inaccurate if the drive uses a translation scheme to support high-capacity disk sizes.</span></span> <span data-ttu-id="3a9da-630">Informieren Sie sich beim Hersteller über genaue Laufwerk Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="3a9da-630">Consult the manufacturer for accurate drive specifications.</span></span>

<span data-ttu-id="3a9da-631">Beispiel: 2649024</span><span class="sxs-lookup"><span data-stu-id="3a9da-631">Example: 2649024</span></span>

<span data-ttu-id="3a9da-632">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="3a9da-632">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="3a9da-633">**TotalTracks**</span><span class="sxs-lookup"><span data-stu-id="3a9da-633">**TotalTracks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a9da-634">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3a9da-634">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-635">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a9da-635">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-636">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Input and Output Structures \| [**Disk \_ Geometry**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| tracksperzylinder")</span><span class="sxs-lookup"><span data-stu-id="3a9da-636">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|TracksPerCylinder")</span></span>
</dt> </dl>

<span data-ttu-id="3a9da-637">Gesamtanzahl der Spuren auf dem physischen Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="3a9da-637">Total number of tracks on the physical disk drive.</span></span> <span data-ttu-id="3a9da-638">Hinweis: der Wert für diese Eigenschaft wird durch erweiterte Funktionen der BIOS-Interruptzeit 13 h abgerufen.</span><span class="sxs-lookup"><span data-stu-id="3a9da-638">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="3a9da-639">Der Wert kann ungenau sein, wenn das Laufwerk ein Übersetzungs Schema verwendet, um Festplattengrößen mit hoher Kapazität zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="3a9da-639">The value may be inaccurate if the drive uses a translation scheme to support high-capacity disk sizes.</span></span> <span data-ttu-id="3a9da-640">Informieren Sie sich beim Hersteller über genaue Laufwerk Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="3a9da-640">Consult the manufacturer for accurate drive specifications.</span></span>

<span data-ttu-id="3a9da-641">Beispiel: 42048</span><span class="sxs-lookup"><span data-stu-id="3a9da-641">Example: 42048</span></span>

<span data-ttu-id="3a9da-642">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="3a9da-642">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="3a9da-643">**TracksPerCylinder**</span><span class="sxs-lookup"><span data-stu-id="3a9da-643">**TracksPerCylinder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a9da-644">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3a9da-644">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-645">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3a9da-645">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a9da-646">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Input and Output Structures \| [**Disk \_ Geometry**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| tracksperzylinder")</span><span class="sxs-lookup"><span data-stu-id="3a9da-646">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|TracksPerCylinder")</span></span>
</dt> </dl>

<span data-ttu-id="3a9da-647">Anzahl der Spuren in jedem Zylinder auf dem physischen Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="3a9da-647">Number of tracks in each cylinder on the physical disk drive.</span></span> <span data-ttu-id="3a9da-648">Hinweis: der Wert für diese Eigenschaft wird durch erweiterte Funktionen der BIOS-Interruptzeit 13 h abgerufen.</span><span class="sxs-lookup"><span data-stu-id="3a9da-648">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="3a9da-649">Der Wert kann ungenau sein, wenn das Laufwerk ein Übersetzungs Schema verwendet, um Festplattengrößen mit hoher Kapazität zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="3a9da-649">The value may be inaccurate if the drive uses a translation scheme to support high-capacity disk sizes.</span></span> <span data-ttu-id="3a9da-650">Informieren Sie sich beim Hersteller über genaue Laufwerk Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="3a9da-650">Consult the manufacturer for accurate drive specifications.</span></span>

<span data-ttu-id="3a9da-651">Beispiel: 64</span><span class="sxs-lookup"><span data-stu-id="3a9da-651">Example: 64</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3a9da-652">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3a9da-652">Remarks</span></span>

<span data-ttu-id="3a9da-653">Physische Festplattenlaufwerke sind das primäre Speichermedium für Informationen in jeder Computerumgebung.</span><span class="sxs-lookup"><span data-stu-id="3a9da-653">Physical hard disk drives are the primary storage medium for information in any computing environment.</span></span> <span data-ttu-id="3a9da-654">Obwohl Organisationen häufig Geräte wie Bandlaufwerke und CD-Laufwerke zum Archivieren von Daten verwenden, sind diese Geräte nicht für die alltägliche Speicherung von Benutzerdaten geeignet.</span><span class="sxs-lookup"><span data-stu-id="3a9da-654">Although organizations often use devices such as tape drives and compact disc drives for archiving data, these devices are not suited for day-to-day storage of user data.</span></span> <span data-ttu-id="3a9da-655">Nur physische Festplatten bieten die Geschwindigkeit und Benutzerfreundlichkeit, die zum Speichern von Daten und zum Ausführen von Anwendungen und des Betriebssystems erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="3a9da-655">Only physical hard disks offer the speed and ease of use required for storing data and for running applications and the operating system.</span></span>

<span data-ttu-id="3a9da-656">Zur effizienten Verwaltung von Daten ist es wichtig, dass Sie über eine ausführliche Inventur aller physischen Datenträger, ihrer Fähigkeiten und ihrer Kapazitäten verfügen.</span><span class="sxs-lookup"><span data-stu-id="3a9da-656">To efficiently manage data, it is important to have a detailed inventory of all your physical disks, their capabilities, and their capacities.</span></span> <span data-ttu-id="3a9da-657">Sie können diese Art von Inventur mithilfe der Win32-Klasse **\_ diskdrive** ableiten.</span><span class="sxs-lookup"><span data-stu-id="3a9da-657">You can use the **Win32\_DiskDrive** class to derive this type of inventory.</span></span>

<span data-ttu-id="3a9da-658">Jede Schnittstelle zu einem physischen Windows-Laufwerk ist ein Nachfolger (oder Mitglied) dieser Klasse.</span><span class="sxs-lookup"><span data-stu-id="3a9da-658">Any interface to a Windows physical disk drive is a descendant (or member) of this class.</span></span> <span data-ttu-id="3a9da-659">Die Funktionen des Laufwerks, das über dieses Objekt angezeigt wird, entsprechen den logischen und Verwaltungs Merkmalen des Laufwerks.</span><span class="sxs-lookup"><span data-stu-id="3a9da-659">The features of the disk drive seen through this object correspond to the logical and management characteristics of the drive.</span></span> <span data-ttu-id="3a9da-660">In einigen Fällen wird dies möglicherweise nicht die tatsächlichen physischen Eigenschaften des Geräts widerspiegeln.</span><span class="sxs-lookup"><span data-stu-id="3a9da-660">In some cases, this may not reflect the actual physical characteristics of the device.</span></span> <span data-ttu-id="3a9da-661">Jedes Objekt, das auf einem anderen logischen Gerät basiert, ist kein Member dieser Klasse.</span><span class="sxs-lookup"><span data-stu-id="3a9da-661">Any object based on another logical device would not be a member of this class.</span></span>

<span data-ttu-id="3a9da-662">Aus Sicherheitsgründen muss ein Benutzer, der von einem Remote Computer aus eine Verbindung herstellt, die **SC- \_ Manager \_ Connect** -Berechtigung aktivieren, damit diese Klasse aufgelistet werden kann.</span><span class="sxs-lookup"><span data-stu-id="3a9da-662">For security reasons, a user connecting from a remote computer must have the **SC\_MANAGER\_CONNECT** privilege enabled to be able to enumerate this class.</span></span> <span data-ttu-id="3a9da-663">Weitere Informationen finden Sie unter [Dienst Sicherheit und Zugriffsrechte](/windows/desktop/Services/service-security-and-access-rights).</span><span class="sxs-lookup"><span data-stu-id="3a9da-663">For more information, see [Service Security and Access Rights](/windows/desktop/Services/service-security-and-access-rights).</span></span>

<span data-ttu-id="3a9da-664">Die **Win32- \_ diskdrive** -Klasse wird von CIM-Datenträger [**\_ Laufwerk**](cim-diskdrive.md) abgeleitet, das von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="3a9da-664">The **Win32\_DiskDrive** class is derived from [**CIM\_DiskDrive**](cim-diskdrive.md) which derives from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span> <span data-ttu-id="3a9da-665">Die **CIM \_ mediaaccessdevice** -Klasse wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="3a9da-665">The **CIM\_MediaAccessDevice** class derives from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="examples"></a><span data-ttu-id="3a9da-666">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3a9da-666">Examples</span></span>

<span data-ttu-id="3a9da-667">Der [Server Inventur Bericht-WMI & CIM](https://Gallery.TechNet.Microsoft.Com/Servers-Inventory-report-e79e2b24) PowerShell-Codebeispiel in der TechNet Gallery verwendet eine Reihe von Klassen, einschließlich **Win32 \_ diskdrive**, um Informationen zum Serverstatus zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="3a9da-667">The [Servers Inventory report-WMI & CIM](https://Gallery.TechNet.Microsoft.Com/Servers-Inventory-report-e79e2b24) PowerShell code example on TechNet Gallery uses a number of classes, including **Win32\_DiskDrive**, to return information about server status.</span></span>

<span data-ttu-id="3a9da-668">Mithilfe des PowerShell-Code Beispiels für das Laufwerk [Laufwerk to Laufwerk Letter using the Win32 \_ diskdrive Interface Type](https://Gallery.TechNet.Microsoft.Com/Map-Drive-to-Drive-Letter-1fff91ad) wird ein Laufwerk einem Laufwerk Buchstaben zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="3a9da-668">The [Map Drive to Drive Letter Using the Win32\_DiskDrive Interface Type Property](https://Gallery.TechNet.Microsoft.Com/Map-Drive-to-Drive-Letter-1fff91ad) PowerShell code sample maps a drive to a drive letter.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a9da-669">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3a9da-669">Requirements</span></span>



| <span data-ttu-id="3a9da-670">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3a9da-670">Requirement</span></span> | <span data-ttu-id="3a9da-671">Wert</span><span class="sxs-lookup"><span data-stu-id="3a9da-671">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3a9da-672">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3a9da-672">Minimum supported client</span></span><br/> | <span data-ttu-id="3a9da-673">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3a9da-673">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3a9da-674">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3a9da-674">Minimum supported server</span></span><br/> | <span data-ttu-id="3a9da-675">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3a9da-675">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3a9da-676">Namespace</span><span class="sxs-lookup"><span data-stu-id="3a9da-676">Namespace</span></span><br/>                | <span data-ttu-id="3a9da-677">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="3a9da-677">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3a9da-678">MOF</span><span class="sxs-lookup"><span data-stu-id="3a9da-678">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3a9da-679"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3a9da-679"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3a9da-680">DLL</span><span class="sxs-lookup"><span data-stu-id="3a9da-680">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a9da-681"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a9da-681"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a9da-682">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3a9da-682">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a9da-683">**CIM- \_ diskdrive**</span><span class="sxs-lookup"><span data-stu-id="3a9da-683">**CIM\_DiskDrive**</span></span>](cim-diskdrive.md)
</dt> <dt>

[<span data-ttu-id="3a9da-684">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="3a9da-684">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="3a9da-685">WMI-Tasks: Datenträger und Dateisysteme</span><span class="sxs-lookup"><span data-stu-id="3a9da-685">WMI Tasks: Disks and File Systems</span></span>](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems)
</dt> </dl>

 

