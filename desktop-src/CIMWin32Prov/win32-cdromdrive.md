---
description: Stellt ein CD-ROM-Laufwerk auf einem Computersystem dar, auf dem Windows ausgeführt wird.
ms.assetid: 08087976-ca88-4ac8-9456-0d8bd799e66c
ms.tgt_platform: multiple
title: Win32_CDROMDrive-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CDROMDrive
- Win32_CDROMDrive.Reset
- Win32_CDROMDrive.SetPowerState
- Win32_CDROMDrive.Availability
- Win32_CDROMDrive.Capabilities
- Win32_CDROMDrive.CapabilityDescriptions
- Win32_CDROMDrive.Caption
- Win32_CDROMDrive.CompressionMethod
- Win32_CDROMDrive.ConfigManagerErrorCode
- Win32_CDROMDrive.ConfigManagerUserConfig
- Win32_CDROMDrive.CreationClassName
- Win32_CDROMDrive.DefaultBlockSize
- Win32_CDROMDrive.Description
- Win32_CDROMDrive.DeviceID
- Win32_CDROMDrive.Drive
- Win32_CDROMDrive.DriveIntegrity
- Win32_CDROMDrive.ErrorCleared
- Win32_CDROMDrive.ErrorDescription
- Win32_CDROMDrive.ErrorMethodology
- Win32_CDROMDrive.FileSystemFlags
- Win32_CDROMDrive.FileSystemFlagsEx
- Win32_CDROMDrive.Id
- Win32_CDROMDrive.InstallDate
- Win32_CDROMDrive.LastErrorCode
- Win32_CDROMDrive.Manufacturer
- Win32_CDROMDrive.MaxBlockSize
- Win32_CDROMDrive.MaximumComponentLength
- Win32_CDROMDrive.MaxMediaSize
- Win32_CDROMDrive.MediaLoaded
- Win32_CDROMDrive.MediaType
- Win32_CDROMDrive.MfrAssignedRevisionLevel
- Win32_CDROMDrive.MinBlockSize
- Win32_CDROMDrive.Name
- Win32_CDROMDrive.NeedsCleaning
- Win32_CDROMDrive.NumberOfMediaSupported
- Win32_CDROMDrive.PNPDeviceID
- Win32_CDROMDrive.PowerManagementCapabilities
- Win32_CDROMDrive.PowerManagementSupported
- Win32_CDROMDrive.RevisionLevel
- Win32_CDROMDrive.SCSIBus
- Win32_CDROMDrive.SCSILogicalUnit
- Win32_CDROMDrive.SCSIPort
- Win32_CDROMDrive.SCSITargetId
- Win32_CDROMDrive.SerialNumber
- Win32_CDROMDrive.Size
- Win32_CDROMDrive.Status
- Win32_CDROMDrive.StatusInfo
- Win32_CDROMDrive.SystemCreationClassName
- Win32_CDROMDrive.SystemName
- Win32_CDROMDrive.TransferRate
- Win32_CDROMDrive.VolumeName
- Win32_CDROMDrive.VolumeSerialNumber
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6c352d2ee717f5eb888b49d6e5e8ff456cc5a85f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958521"
---
# <a name="win32_cdromdrive-class"></a><span data-ttu-id="dd060-103">Win32 \_ cdromdrive-Klasse</span><span class="sxs-lookup"><span data-stu-id="dd060-103">Win32\_CDROMDrive class</span></span>

<span data-ttu-id="dd060-104">Die **Win32 \_ cdromdrive** - [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) stellt ein CD-ROM-Laufwerk auf einem Computersystem dar, auf dem Windows ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dd060-104">The **Win32\_CDROMDrive** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a CD-ROM drive on a computer system running Windows.</span></span>

> [!Note]  
> <span data-ttu-id="dd060-105">Beachten Sie, dass der Name des Laufwerks nicht dem Buchstaben des logischen Laufwerks entspricht, das dem Gerät zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="dd060-105">Be aware that the name of the drive does not correspond to the logical drive letter assigned to the device.</span></span>

 

<span data-ttu-id="dd060-106">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="dd060-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="dd060-107">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="dd060-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd060-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd060-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4B3-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_CDROMDrive : CIM_CDROMDrive
{
  uint16   Availability;
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
  string   Drive;
  boolean  DriveIntegrity;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  uint16   FileSystemFlags;
  uint32   FileSystemFlagsEx;
  string   Id;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Manufacturer;
  uint64   MaxBlockSize;
  uint32   MaximumComponentLength;
  uint64   MaxMediaSize;
  boolean  MediaLoaded;
  string   MediaType;
  string   MfrAssignedRevisionLevel;
  uint64   MinBlockSize;
  string   Name;
  boolean  NeedsCleaning;
  uint32   NumberOfMediaSupported;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   RevisionLevel;
  uint32   SCSIBus;
  uint16   SCSILogicalUnit;
  uint16   SCSIPort;
  uint16   SCSITargetId;
  string   SerialNumber;
  uint64   Size;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  real64   TransferRate;
  string   VolumeName;
  string   VolumeSerialNumber;
};
```

## <a name="members"></a><span data-ttu-id="dd060-109">Member</span><span class="sxs-lookup"><span data-stu-id="dd060-109">Members</span></span>

<span data-ttu-id="dd060-110">Die **Win32 \_ cdromdrive** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="dd060-110">The **Win32\_CDROMDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="dd060-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="dd060-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="dd060-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dd060-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="dd060-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="dd060-113">Methods</span></span>

<span data-ttu-id="dd060-114">Die **Win32 \_ cdromdrive** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="dd060-114">The **Win32\_CDROMDrive** class has these methods.</span></span>



| <span data-ttu-id="dd060-115">Methode</span><span class="sxs-lookup"><span data-stu-id="dd060-115">Method</span></span>            | <span data-ttu-id="dd060-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dd060-116">Description</span></span>                                                                                                                                                                                                |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd060-117">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="dd060-117">**Reset**</span></span>         | <span data-ttu-id="dd060-118">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="dd060-118">Not implemented.</span></span> <span data-ttu-id="dd060-119">Informationen zur Implementierung dieser Methode finden Sie unter der [**Reset**](reset-method-in-class-cim-controller.md) -Methode in [**CIM \_ cdromdrive**](cim-cdromdrive.md) .</span><span class="sxs-lookup"><span data-stu-id="dd060-119">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_CDROMDrive**](cim-cdromdrive.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="dd060-120">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="dd060-120">**SetPowerState**</span></span> | <span data-ttu-id="dd060-121">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="dd060-121">Not implemented.</span></span> <span data-ttu-id="dd060-122">Informationen zur Implementierung dieser Methode finden Sie in der [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode in [**CIM \_ cdromdrive**](cim-cdromdrive.md) .</span><span class="sxs-lookup"><span data-stu-id="dd060-122">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_CDROMDrive**](cim-cdromdrive.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="dd060-123">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dd060-123">Properties</span></span>

<span data-ttu-id="dd060-124">Die **Win32 \_ cdromdrive** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="dd060-124">The **Win32\_CDROMDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dd060-125">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="dd060-125">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd060-126">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dd060-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dd060-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd060-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd060-128">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="dd060-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="dd060-129">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="dd060-129">Availability and status of the device.</span></span>

<span data-ttu-id="dd060-130">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dd060-130">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dd060-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="dd060-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dd060-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="dd060-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="dd060-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="dd060-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-134">Ausführung oder vollständiger Stromversorgung</span><span class="sxs-lookup"><span data-stu-id="dd060-134">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="dd060-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="dd060-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="dd060-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="dd060-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="dd060-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="dd060-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="dd060-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="dd060-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="dd060-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="dd060-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="dd060-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="dd060-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="dd060-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="dd060-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="dd060-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="dd060-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="dd060-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="dd060-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="dd060-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="dd060-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-145">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="dd060-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="dd060-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="dd060-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-147">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="dd060-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="dd060-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="dd060-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-149">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb gebracht werden.</span><span class="sxs-lookup"><span data-stu-id="dd060-149">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="dd060-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="dd060-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="dd060-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="dd060-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-152">Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="dd060-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="dd060-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="dd060-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-154">Das Gerät wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="dd060-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="dd060-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="dd060-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-156">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="dd060-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="dd060-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="dd060-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-158">Das Gerät ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="dd060-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="dd060-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="dd060-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-160">Das Gerät ist in Ruhe.</span><span class="sxs-lookup"><span data-stu-id="dd060-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="dd060-161">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="dd060-161">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd060-162">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="dd060-162">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="dd060-163">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd060-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd060-164">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergeräte \| 001,9 "," MIF. DMTF- \| Speichergeräte \| 001,11 "," MIF. DMTF- \| Speichergeräte \| 001,12 "," MIF. DMTF-Datenträger \| \| 003,7 "), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md).**Capabilitybeschreibungen**")</span><span class="sxs-lookup"><span data-stu-id="dd060-164">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="dd060-165">Array von Funktionen des Medien Zugriffs Geräts.</span><span class="sxs-lookup"><span data-stu-id="dd060-165">Array of capabilities of the media access device.</span></span> <span data-ttu-id="dd060-166">Beispielsweise kann das Gerät zufälligen Zugriff (3), Wechselmedien (7) und automatische Bereinigung (9) unterstützen.</span><span class="sxs-lookup"><span data-stu-id="dd060-166">For example, the device may support random access (3), removable media (7), and automatic cleaning (9).</span></span>

<span data-ttu-id="dd060-167">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dd060-167">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dd060-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="dd060-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dd060-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="dd060-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="dd060-170"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequenzieller Zugriff** (2)</span><span class="sxs-lookup"><span data-stu-id="dd060-170"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="dd060-171"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Zufälliger Zugriff** (3)</span><span class="sxs-lookup"><span data-stu-id="dd060-171"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="dd060-172"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Unterstützt Schreib** Vorgänge (4)</span><span class="sxs-lookup"><span data-stu-id="dd060-172"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="dd060-173"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Verschlüsselung** (5)</span><span class="sxs-lookup"><span data-stu-id="dd060-173"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="dd060-174"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Komprimierung** (6)</span><span class="sxs-lookup"><span data-stu-id="dd060-174"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="dd060-175"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Unterstützt Removeable Media** (7)</span><span class="sxs-lookup"><span data-stu-id="dd060-175"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-176">Unterstützt Wechselmedien</span><span class="sxs-lookup"><span data-stu-id="dd060-176">Supports Removable Media</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="dd060-177"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manuelle Reinigung** (8)</span><span class="sxs-lookup"><span data-stu-id="dd060-177"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="dd060-178"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatische Bereinigung** (9)</span><span class="sxs-lookup"><span data-stu-id="dd060-178"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="dd060-179"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**Smart Notification** (10)</span><span class="sxs-lookup"><span data-stu-id="dd060-179"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="dd060-180"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Unterstützt zweiseitige Medien** (11)</span><span class="sxs-lookup"><span data-stu-id="dd060-180"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-181">Unterstützt Dual-Sided Medien</span><span class="sxs-lookup"><span data-stu-id="dd060-181">Supports Dual-Sided Media</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="dd060-182"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount-eject nicht erforderlich** (12)</span><span class="sxs-lookup"><span data-stu-id="dd060-182"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dd060-183">**Capabilitybeschreibungen**</span><span class="sxs-lookup"><span data-stu-id="dd060-183">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd060-184">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="dd060-184">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="dd060-185">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd060-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd060-186">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md).**Funktionen**")</span><span class="sxs-lookup"><span data-stu-id="dd060-186">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="dd060-187">Array ausführlicher Erläuterungen für alle Zugriffsgeräte Funktionen, die im **Funktions Array angegeben** sind.</span><span class="sxs-lookup"><span data-stu-id="dd060-187">Array of more detailed explanations for any of the access device features indicated in the **Capabilities** array.</span></span> <span data-ttu-id="dd060-188">Jeder Eintrag dieses Arrays bezieht sich auf den Eintrag im **Funktions Array, der sich** am selben Index befindet.</span><span class="sxs-lookup"><span data-stu-id="dd060-188">Each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

<span data-ttu-id="dd060-189">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dd060-189">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd060-190">**Caption**</span><span class="sxs-lookup"><span data-stu-id="dd060-190">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd060-191">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dd060-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd060-192">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd060-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd060-193">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="dd060-193">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="dd060-194">Kurze Beschreibung des Objekts eine einzeilige Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="dd060-194">Short description of the object a one-line string.</span></span>

<span data-ttu-id="dd060-195">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dd060-195">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd060-196">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="dd060-196">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd060-197">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dd060-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd060-198">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd060-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd060-199">Der Algorithmus oder das Tool, mit dem das Gerät die Komprimierung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dd060-199">Algorithm or tool used by the device to support compression.</span></span> <span data-ttu-id="dd060-200">Wenn es nicht möglich oder nicht erwünscht ist, das Komprimierungs Schema zu beschreiben (weil es möglicherweise nicht bekannt ist), verwenden Sie die folgenden Wörter: "unknown", um darzustellen, dass das Gerät Komprimierungs Funktionen unterstützt. "Komprimiert", um darzustellen, dass das Gerät Komprimierungs Funktionen unterstützt, aber entweder das zugehörige Komprimierungs Schema nicht bekannt oder nicht offengelegt ist. und "nicht komprimiert", um darzustellen, dass das Gerät keine Komprimierungs Funktionen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dd060-200">If it is not possible or not desired to describe the compression scheme (perhaps because it is not known), use the following words: "Unknown" to represent that it is not known whether the device supports compression capabilities; "Compressed" to represent that the device supports compression capabilities but either its compression scheme is not known or not disclosed; and "Not Compressed" to represent that the device does not support compression capabilities.</span></span>

<span data-ttu-id="dd060-201">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dd060-201">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>



 <span data-ttu-id="dd060-202">("Unbekannt")</span><span class="sxs-lookup"><span data-stu-id="dd060-202">("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="dd060-203">Das Komprimierungs Schema ist unbekannt oder nicht beschrieben.</span><span class="sxs-lookup"><span data-stu-id="dd060-203">The compression scheme is unknown or not described.</span></span>

</dd> <dt>



 <span data-ttu-id="dd060-204">("Komprimiert")</span><span class="sxs-lookup"><span data-stu-id="dd060-204">("Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="dd060-205">Die logische Datei ist komprimiert, das Komprimierungs Schema ist jedoch unbekannt oder nicht beschrieben.</span><span class="sxs-lookup"><span data-stu-id="dd060-205">The logical file is compressed, but the compression scheme is unknown or not described</span></span>

</dd> <dt>



 <span data-ttu-id="dd060-206">("Nicht komprimiert")</span><span class="sxs-lookup"><span data-stu-id="dd060-206">("Not Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="dd060-207">Wenn die logische Datei nicht komprimiert ist</span><span class="sxs-lookup"><span data-stu-id="dd060-207">If the logical file is not compressed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="dd060-208">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="dd060-208">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd060-209">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dd060-209">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd060-210">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd060-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd060-211">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="dd060-211">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="dd060-212">Windows Configuration Manager-Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="dd060-212">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="dd060-213">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dd060-213">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="dd060-214"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="dd060-214"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="dd060-215"> (0)</span><span class="sxs-lookup"><span data-stu-id="dd060-215">(0)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-216">Das Gerät funktioniert ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="dd060-216">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="dd060-217"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="dd060-217"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="dd060-218">(1)</span><span class="sxs-lookup"><span data-stu-id="dd060-218">(1)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-219">Das Gerät ist nicht ordnungsgemäß konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="dd060-219">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="dd060-220"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="dd060-220"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="dd060-221">(2)</span><span class="sxs-lookup"><span data-stu-id="dd060-221">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="dd060-222"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="dd060-222"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="dd060-223">(3)</span><span class="sxs-lookup"><span data-stu-id="dd060-223">(3)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-224">Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt möglicherweise nicht über genügend Arbeitsspeicher oder andere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="dd060-224">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="dd060-225"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="dd060-225"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="dd060-226">(4)</span><span class="sxs-lookup"><span data-stu-id="dd060-226">(4)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-227">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="dd060-227">Device is not working properly.</span></span> <span data-ttu-id="dd060-228">Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="dd060-228">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="dd060-229"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="dd060-229"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="dd060-230">(5)</span><span class="sxs-lookup"><span data-stu-id="dd060-230">(5)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-231">Der Treiber für das Gerät erfordert eine Ressource, die von Windows nicht verwaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="dd060-231">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="dd060-232"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="dd060-232"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="dd060-233"> (6)</span><span class="sxs-lookup"><span data-stu-id="dd060-233">(6)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-234">Die Startkonfiguration für das Gerät steht in Konflikt mit anderen Geräten.</span><span class="sxs-lookup"><span data-stu-id="dd060-234">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="dd060-235"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="dd060-235"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="dd060-236">(7)</span><span class="sxs-lookup"><span data-stu-id="dd060-236">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="dd060-237"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="dd060-237"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="dd060-238">(8)</span><span class="sxs-lookup"><span data-stu-id="dd060-238">(8)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-239">Das Treiber Lade Modul für das Gerät fehlt.</span><span class="sxs-lookup"><span data-stu-id="dd060-239">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="dd060-240"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="dd060-240"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="dd060-241">(9)</span><span class="sxs-lookup"><span data-stu-id="dd060-241">(9)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-242">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="dd060-242">Device is not working properly.</span></span> <span data-ttu-id="dd060-243">Die Steuerungs Firmware meldet nicht korrekt die Ressourcen für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="dd060-243">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="dd060-244"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="dd060-244"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="dd060-245">(10)</span><span class="sxs-lookup"><span data-stu-id="dd060-245">(10)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-246">Das Gerät kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="dd060-246">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="dd060-247"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="dd060-247"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="dd060-248">(11)</span><span class="sxs-lookup"><span data-stu-id="dd060-248">(11)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-249">Fehler beim Gerät.</span><span class="sxs-lookup"><span data-stu-id="dd060-249">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="dd060-250"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="dd060-250"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="dd060-251">(12)</span><span class="sxs-lookup"><span data-stu-id="dd060-251">(12)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-252">Das Gerät kann nicht genug freie Ressourcen für die Verwendung finden.</span><span class="sxs-lookup"><span data-stu-id="dd060-252">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="dd060-253"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="dd060-253"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="dd060-254">(13)</span><span class="sxs-lookup"><span data-stu-id="dd060-254">(13)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-255">Die Geräte Ressourcen können nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="dd060-255">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="dd060-256"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="dd060-256"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="dd060-257">(14)</span><span class="sxs-lookup"><span data-stu-id="dd060-257">(14)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-258">Das Gerät kann erst ordnungsgemäß funktionieren, wenn der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="dd060-258">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="dd060-259"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="dd060-259"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="dd060-260">(15)</span><span class="sxs-lookup"><span data-stu-id="dd060-260">(15)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-261">Das Gerät funktioniert aufgrund eines möglichen erneuten Aufzählungs Problems nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="dd060-261">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="dd060-262"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="dd060-262"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="dd060-263">(16)</span><span class="sxs-lookup"><span data-stu-id="dd060-263">(16)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-264">In Windows können nicht alle Ressourcen identifiziert werden, die vom Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dd060-264">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="dd060-265"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="dd060-265"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="dd060-266">(17)</span><span class="sxs-lookup"><span data-stu-id="dd060-266">(17)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-267">Das Gerät fordert einen unbekannten Ressourcentyp an.</span><span class="sxs-lookup"><span data-stu-id="dd060-267">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="dd060-268"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="dd060-268"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="dd060-269">(18)</span><span class="sxs-lookup"><span data-stu-id="dd060-269">(18)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-270">Gerätetreiber müssen neu installiert werden.</span><span class="sxs-lookup"><span data-stu-id="dd060-270">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="dd060-271"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="dd060-271"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="dd060-272">(19)</span><span class="sxs-lookup"><span data-stu-id="dd060-272">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="dd060-273"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="dd060-273"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="dd060-274">(20)</span><span class="sxs-lookup"><span data-stu-id="dd060-274">(20)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-275">Die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="dd060-275">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="dd060-276"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="dd060-276"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="dd060-277">(21)</span><span class="sxs-lookup"><span data-stu-id="dd060-277">(21)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-278">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="dd060-278">System failure.</span></span> <span data-ttu-id="dd060-279">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="dd060-279">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="dd060-280">Das Gerät wird von Windows entfernt.</span><span class="sxs-lookup"><span data-stu-id="dd060-280">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="dd060-281"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="dd060-281"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="dd060-282">(22)</span><span class="sxs-lookup"><span data-stu-id="dd060-282">(22)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-283">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="dd060-283">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="dd060-284"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="dd060-284"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="dd060-285">(23)</span><span class="sxs-lookup"><span data-stu-id="dd060-285">(23)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-286">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="dd060-286">System failure.</span></span> <span data-ttu-id="dd060-287">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="dd060-287">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="dd060-288"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="dd060-288"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="dd060-289">(24)</span><span class="sxs-lookup"><span data-stu-id="dd060-289">(24)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-290">Das Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.</span><span class="sxs-lookup"><span data-stu-id="dd060-290">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="dd060-291"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="dd060-291"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="dd060-292">(25)</span><span class="sxs-lookup"><span data-stu-id="dd060-292">(25)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-293">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="dd060-293">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="dd060-294"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="dd060-294"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="dd060-295">(26)</span><span class="sxs-lookup"><span data-stu-id="dd060-295">(26)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-296">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="dd060-296">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="dd060-297"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="dd060-297"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="dd060-298">(27)</span><span class="sxs-lookup"><span data-stu-id="dd060-298">(27)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-299">Das Gerät verfügt nicht über eine gültige Protokoll Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="dd060-299">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="dd060-300"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="dd060-300"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="dd060-301">(28)</span><span class="sxs-lookup"><span data-stu-id="dd060-301">(28)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-302">Gerätetreiber sind nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="dd060-302">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="dd060-303"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="dd060-303"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="dd060-304">(29)</span><span class="sxs-lookup"><span data-stu-id="dd060-304">(29)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-305">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="dd060-305">Device is disabled.</span></span> <span data-ttu-id="dd060-306">Die Gerätefirmware hat nicht die erforderlichen Ressourcen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="dd060-306">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="dd060-307"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="dd060-307"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="dd060-308">(30)</span><span class="sxs-lookup"><span data-stu-id="dd060-308">(30)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-309">Das Gerät verwendet eine UNQ-Ressource, die von einem anderen Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dd060-309">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="dd060-310"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="dd060-310"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="dd060-311">31,5</span><span class="sxs-lookup"><span data-stu-id="dd060-311">(31)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-312">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="dd060-312">Device is not working properly.</span></span> <span data-ttu-id="dd060-313">Die erforderlichen Gerätetreiber können nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="dd060-313">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="dd060-314">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="dd060-314">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd060-315">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="dd060-315">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dd060-316">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd060-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd060-317">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="dd060-317">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="dd060-318">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="dd060-318">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="dd060-319">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dd060-319">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd060-320">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="dd060-320">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd060-321">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dd060-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd060-322">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd060-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd060-323">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="dd060-323">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="dd060-324">Der Name der ersten konkreten Klasse, die in der Vererbungs Kette angezeigt wird, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dd060-324">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="dd060-325">Bei Verwendung mit den anderen Schlüsseleigenschaften der-Klasse ermöglicht die-Eigenschaft, dass alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="dd060-325">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="dd060-326">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dd060-326">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd060-327">**Defaultblocksize**</span><span class="sxs-lookup"><span data-stu-id="dd060-327">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd060-328">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="dd060-328">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dd060-329">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd060-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd060-330">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="dd060-330">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="dd060-331">Standard Blockgröße (in Bytes) für dieses Gerät.</span><span class="sxs-lookup"><span data-stu-id="dd060-331">Default block size, in bytes, for this device.</span></span>

<span data-ttu-id="dd060-332">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dd060-332">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="dd060-333">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="dd060-333">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="dd060-334">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dd060-334">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd060-335">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dd060-335">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd060-336">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd060-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd060-337">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="dd060-337">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="dd060-338">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="dd060-338">Description of the object.</span></span>

<span data-ttu-id="dd060-339">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dd060-339">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd060-340">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="dd060-340">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd060-341">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dd060-341">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd060-342">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd060-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd060-343">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceID"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| File Functions \| getlogicaldrivestrings")</span><span class="sxs-lookup"><span data-stu-id="dd060-343">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|GetLogicalDriveStrings")</span></span>
</dt> </dl>

<span data-ttu-id="dd060-344">Eindeutiger Bezeichner für ein CD-ROM-Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="dd060-344">Unique identifier for a CD-ROM drive.</span></span>

<span data-ttu-id="dd060-345">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dd060-345">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd060-346">**Laufwerk**</span><span class="sxs-lookup"><span data-stu-id="dd060-346">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd060-347">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dd060-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd060-348">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd060-348">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd060-349">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| File Functions \| GetDriveType")</span><span class="sxs-lookup"><span data-stu-id="dd060-349">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|GetDriveType")</span></span>
</dt> </dl>

<span data-ttu-id="dd060-350">Laufwerk Buchstabe des CD-ROM-Laufwerks.</span><span class="sxs-lookup"><span data-stu-id="dd060-350">Drive letter of the CD-ROM drive.</span></span>

<span data-ttu-id="dd060-351">Beispiel: "d: \\ "</span><span class="sxs-lookup"><span data-stu-id="dd060-351">Example: "d:\\"</span></span>

</dd> <dt>

<span data-ttu-id="dd060-352">**Driveitegrity**</span><span class="sxs-lookup"><span data-stu-id="dd060-352">**DriveIntegrity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd060-353">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="dd060-353">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dd060-354">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd060-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd060-355">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="dd060-355">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="dd060-356">Wenn der Wert **true** ist, können Dateien vom CD-Gerät korrekt gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="dd060-356">If **True**, files can be accurately read from the CD device.</span></span> <span data-ttu-id="dd060-357">Dies wird erreicht, indem ein Datenblock zweimal gelesen und die Daten mit sich selbst verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="dd060-357">This is achieved by reading a block of data twice and comparing the data against itself.</span></span>

</dd> <dt>

<span data-ttu-id="dd060-358">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="dd060-358">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd060-359">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="dd060-359">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dd060-360">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd060-360">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd060-361">**True** gibt an, dass der in **LastErrorCode** gemeldete Fehler jetzt gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="dd060-361">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="dd060-362">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dd060-362">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd060-363">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="dd060-363">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd060-364">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dd060-364">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd060-365">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd060-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd060-366">Weitere Informationen zu dem Fehler, der in " **LastErrorCode**" aufgezeichnet wurde, sowie Informationen zu Korrekturmaßnahmen, die durchgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="dd060-366">More information about the error recorded in **LastErrorCode**, and information about corrective actions that can be taken.</span></span>

<span data-ttu-id="dd060-367">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dd060-367">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd060-368">**Errormethodmethodologie**</span><span class="sxs-lookup"><span data-stu-id="dd060-368">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd060-369">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dd060-369">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd060-370">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd060-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd060-371">Typ der Fehlererkennung und-Korrektur, die von diesem Gerät unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="dd060-371">Type of error detection and correction supported by this device.</span></span>

<span data-ttu-id="dd060-372">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dd060-372">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd060-373">**FileSystemFlags**</span><span class="sxs-lookup"><span data-stu-id="dd060-373">**FileSystemFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd060-374">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dd060-374">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dd060-375">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd060-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd060-376">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| File System Functions \| [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span><span class="sxs-lookup"><span data-stu-id="dd060-376">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span></span>
</dt> </dl>

<span data-ttu-id="dd060-377">Diese Eigenschaft ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="dd060-377">This property is obsolete.</span></span> <span data-ttu-id="dd060-378">Verwenden Sie anstelle dieser Eigenschaft **FileSystemFlagsEx**.</span><span class="sxs-lookup"><span data-stu-id="dd060-378">In place of this property, use **FileSystemFlagsEx**.</span></span>

</dd> <dt>

<span data-ttu-id="dd060-379">**FileSystemFlagsEx**</span><span class="sxs-lookup"><span data-stu-id="dd060-379">**FileSystemFlagsEx**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd060-380">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dd060-380">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd060-381">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd060-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd060-382">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| File System Functions \| [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span><span class="sxs-lookup"><span data-stu-id="dd060-382">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span></span>
</dt> </dl>

<span data-ttu-id="dd060-383">Dateisystemflags, die dem Windows-CD-ROM-Laufwerk zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="dd060-383">File system flags associated with the Windows CD-ROM drive.</span></span> <span data-ttu-id="dd060-384">Dieser Parameter kann eine beliebige Kombination von Flags sein, aber die **FS- \_ Datei \_ Komprimierung** und das **FS- \_ Vol \_ \_** werden sich gegenseitig ausschließen.</span><span class="sxs-lookup"><span data-stu-id="dd060-384">This parameter can be any combination of flags, but **FS\_FILE\_COMPRESSION** and **FS\_VOL\_IS\_COMPRESSED** are mutually exclusive.</span></span>

<dt>

<span id="Case_Sensitive_Search"></span><span id="case_sensitive_search"></span><span id="CASE_SENSITIVE_SEARCH"></span>

<span data-ttu-id="dd060-385"><span id="Case_Sensitive_Search"></span><span id="case_sensitive_search"></span><span id="CASE_SENSITIVE_SEARCH"></span>**Suche nach Groß-/Kleinschreibung** (1)</span><span class="sxs-lookup"><span data-stu-id="dd060-385"><span id="Case_Sensitive_Search"></span><span id="case_sensitive_search"></span><span id="CASE_SENSITIVE_SEARCH"></span>**Case Sensitive Search** (1)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-386">Das Dateisystem unterstützt Dateinamen mit Beachtung der Groß-/Kleinschreibung</span><span class="sxs-lookup"><span data-stu-id="dd060-386">The file system supports case-sensitive file names.</span></span>

</dd> <dt>

<span id="Case_Preserved_Names"></span><span id="case_preserved_names"></span><span id="CASE_PRESERVED_NAMES"></span>

<span data-ttu-id="dd060-387"><span id="Case_Preserved_Names"></span><span id="case_preserved_names"></span><span id="CASE_PRESERVED_NAMES"></span>Beibehaltene **Namen** (2)</span><span class="sxs-lookup"><span data-stu-id="dd060-387"><span id="Case_Preserved_Names"></span><span id="case_preserved_names"></span><span id="CASE_PRESERVED_NAMES"></span>**Case Preserved Names** (2)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-388">Das Dateisystem behält die Groß-/Kleinschreibung von Dateinamen bei, wenn ein Name auf einem Datenträger platziert wird.</span><span class="sxs-lookup"><span data-stu-id="dd060-388">The file system preserves the case of file names when it places a name on a disk.</span></span>

</dd> <dt>

<span id="Unicode_On_Disk"></span><span id="unicode_on_disk"></span><span id="UNICODE_ON_DISK"></span>

<span data-ttu-id="dd060-389"><span id="Unicode_On_Disk"></span><span id="unicode_on_disk"></span><span id="UNICODE_ON_DISK"></span>**Unicode auf** Datenträger (4)</span><span class="sxs-lookup"><span data-stu-id="dd060-389"><span id="Unicode_On_Disk"></span><span id="unicode_on_disk"></span><span id="UNICODE_ON_DISK"></span>**Unicode On Disk** (4)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-390">Das Dateisystem unterstützt Unicode in Dateinamen, so wie Sie auf dem Datenträger angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="dd060-390">The file system supports Unicode in file names as they appear on the disk.</span></span>

</dd> <dt>

<span id="Persistent_ACLs"></span><span id="persistent_acls"></span><span id="PERSISTENT_ACLS"></span>

<span data-ttu-id="dd060-391"><span id="Persistent_ACLs"></span><span id="persistent_acls"></span><span id="PERSISTENT_ACLS"></span>**Persistente ACLs** (8)</span><span class="sxs-lookup"><span data-stu-id="dd060-391"><span id="Persistent_ACLs"></span><span id="persistent_acls"></span><span id="PERSISTENT_ACLS"></span>**Persistent ACLs** (8)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-392">Das Dateisystem behält Zugriffs Steuerungs Listen (ACLs) bei und erzwingt Sie.</span><span class="sxs-lookup"><span data-stu-id="dd060-392">The file system preserves and enforces access control lists (ACLs).</span></span> <span data-ttu-id="dd060-393">Das NTFS-Dateisystem behält z. b. ACLs bei und erzwingt Sie, und das FAT-Dateisystem wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dd060-393">For example, the NTFS file system preserves and enforces ACLs and the FAT file system does not.</span></span>

</dd> <dt>

<span id="File_Compression"></span><span id="file_compression"></span><span id="FILE_COMPRESSION"></span>

<span data-ttu-id="dd060-394"><span id="File_Compression"></span><span id="file_compression"></span><span id="FILE_COMPRESSION"></span>**Dateikomprimierung** (16)</span><span class="sxs-lookup"><span data-stu-id="dd060-394"><span id="File_Compression"></span><span id="file_compression"></span><span id="FILE_COMPRESSION"></span>**File Compression** (16)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-395">Das Dateisystem unterstützt dateibasierte Komprimierung.</span><span class="sxs-lookup"><span data-stu-id="dd060-395">The file system supports file-based compression.</span></span>

</dd> <dt>

<span id="Volume_Quotas"></span><span id="volume_quotas"></span><span id="VOLUME_QUOTAS"></span>

<span data-ttu-id="dd060-396"><span id="Volume_Quotas"></span><span id="volume_quotas"></span><span id="VOLUME_QUOTAS"></span>**Volumekontingente** (32)</span><span class="sxs-lookup"><span data-stu-id="dd060-396"><span id="Volume_Quotas"></span><span id="volume_quotas"></span><span id="VOLUME_QUOTAS"></span>**Volume Quotas** (32)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-397">Das Dateisystem unterstützt Datenträger Kontingente.</span><span class="sxs-lookup"><span data-stu-id="dd060-397">The file system supports disk quotas.</span></span>

</dd> <dt>

<span id="Supports_Sparse_Files"></span><span id="supports_sparse_files"></span><span id="SUPPORTS_SPARSE_FILES"></span>

<span data-ttu-id="dd060-398"><span id="Supports_Sparse_Files"></span><span id="supports_sparse_files"></span><span id="SUPPORTS_SPARSE_FILES"></span>**Unterstützt sparsesdateien** (64)</span><span class="sxs-lookup"><span data-stu-id="dd060-398"><span id="Supports_Sparse_Files"></span><span id="supports_sparse_files"></span><span id="SUPPORTS_SPARSE_FILES"></span>**Supports Sparse Files** (64)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-399">Das Dateisystem unterstützt Ersatz Dateien.</span><span class="sxs-lookup"><span data-stu-id="dd060-399">The file system supports spare files.</span></span>

</dd> <dt>

<span id="Supports_Reparse_Points"></span><span id="supports_reparse_points"></span><span id="SUPPORTS_REPARSE_POINTS"></span>

<span data-ttu-id="dd060-400"><span id="Supports_Reparse_Points"></span><span id="supports_reparse_points"></span><span id="SUPPORTS_REPARSE_POINTS"></span>**Unterstützt Analyse Punkte** (128)</span><span class="sxs-lookup"><span data-stu-id="dd060-400"><span id="Supports_Reparse_Points"></span><span id="supports_reparse_points"></span><span id="SUPPORTS_REPARSE_POINTS"></span>**Supports Reparse Points** (128)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-401">Das Dateisystem unterstützt Analyse Punkte.</span><span class="sxs-lookup"><span data-stu-id="dd060-401">The file system supports reparse points.</span></span>

</dd> <dt>

<span id="Supports_Remote_Storage"></span><span id="supports_remote_storage"></span><span id="SUPPORTS_REMOTE_STORAGE"></span>

<span data-ttu-id="dd060-402"><span id="Supports_Remote_Storage"></span><span id="supports_remote_storage"></span><span id="SUPPORTS_REMOTE_STORAGE"></span>**Unterstützt Remote Speicher** (256)</span><span class="sxs-lookup"><span data-stu-id="dd060-402"><span id="Supports_Remote_Storage"></span><span id="supports_remote_storage"></span><span id="SUPPORTS_REMOTE_STORAGE"></span>**Supports Remote Storage** (256)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-403">Das Dateisystem unterstützt die Remote Speicherung von Dateien.</span><span class="sxs-lookup"><span data-stu-id="dd060-403">The file system supports the remote storage of files.</span></span>

</dd> <dt>

<span id="Supports_Long_Names"></span><span id="supports_long_names"></span><span id="SUPPORTS_LONG_NAMES"></span>

<span data-ttu-id="dd060-404"><span id="Supports_Long_Names"></span><span id="supports_long_names"></span><span id="SUPPORTS_LONG_NAMES"></span>**Unterstützt lange Namen** (16384)</span><span class="sxs-lookup"><span data-stu-id="dd060-404"><span id="Supports_Long_Names"></span><span id="supports_long_names"></span><span id="SUPPORTS_LONG_NAMES"></span>**Supports Long Names** (16384)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-405">Das Dateisystem unterstützt Dateinamen, die länger als acht Zeichen sind.</span><span class="sxs-lookup"><span data-stu-id="dd060-405">The file system supports file names that are longer than eight characters.</span></span>

</dd> <dt>

<span id="Volume_Is_Compressed"></span><span id="volume_is_compressed"></span><span id="VOLUME_IS_COMPRESSED"></span>

<span data-ttu-id="dd060-406"><span id="Volume_Is_Compressed"></span><span id="volume_is_compressed"></span><span id="VOLUME_IS_COMPRESSED"></span>**Volume ist komprimiert** (32768)</span><span class="sxs-lookup"><span data-stu-id="dd060-406"><span id="Volume_Is_Compressed"></span><span id="volume_is_compressed"></span><span id="VOLUME_IS_COMPRESSED"></span>**Volume Is Compressed** (32768)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-407">Das angegebene Datenträger Volume ist ein komprimiertes Volume, z. b. ein Double Space-Volume.</span><span class="sxs-lookup"><span data-stu-id="dd060-407">The specified disk volume is a compressed volume, for example, a DoubleSpace volume.</span></span>

</dd> <dt>

<span id="Read_Only_Volume"></span><span id="read_only_volume"></span><span id="READ_ONLY_VOLUME"></span>

<span data-ttu-id="dd060-408"><span id="Read_Only_Volume"></span><span id="read_only_volume"></span><span id="READ_ONLY_VOLUME"></span>Schreib geschütztes **Volume** (524289)</span><span class="sxs-lookup"><span data-stu-id="dd060-408"><span id="Read_Only_Volume"></span><span id="read_only_volume"></span><span id="READ_ONLY_VOLUME"></span>**Read Only Volume** (524289)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-409">Das angegebene Volume ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="dd060-409">The specified volume is read-only.</span></span>

</dd> <dt>

<span id="Supports_Object_IDS"></span><span id="supports_object_ids"></span><span id="SUPPORTS_OBJECT_IDS"></span>

<span data-ttu-id="dd060-410"><span id="Supports_Object_IDS"></span><span id="supports_object_ids"></span><span id="SUPPORTS_OBJECT_IDS"></span>**Unterstützung von Objekt-IDs** (65536)</span><span class="sxs-lookup"><span data-stu-id="dd060-410"><span id="Supports_Object_IDS"></span><span id="supports_object_ids"></span><span id="SUPPORTS_OBJECT_IDS"></span>**Supports Object IDS** (65536)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-411">Das Dateisystem unterstützt Objekt Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="dd060-411">The file system supports object identifiers.</span></span>

</dd> <dt>

<span id="Supports_Encryption"></span><span id="supports_encryption"></span><span id="SUPPORTS_ENCRYPTION"></span>

<span data-ttu-id="dd060-412"><span id="Supports_Encryption"></span><span id="supports_encryption"></span><span id="SUPPORTS_ENCRYPTION"></span>**Unterstützt Verschlüsselung** (131072)</span><span class="sxs-lookup"><span data-stu-id="dd060-412"><span id="Supports_Encryption"></span><span id="supports_encryption"></span><span id="SUPPORTS_ENCRYPTION"></span>**Supports Encryption** (131072)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-413">Das Dateisystem unterstützt das verschlüsselte Dateisystem (EFS).</span><span class="sxs-lookup"><span data-stu-id="dd060-413">The file system supports the Encrypted File System (EFS).</span></span>

</dd> <dt>

<span id="Supports_Named_Streams"></span><span id="supports_named_streams"></span><span id="SUPPORTS_NAMED_STREAMS"></span>

<span data-ttu-id="dd060-414"><span id="Supports_Named_Streams"></span><span id="supports_named_streams"></span><span id="SUPPORTS_NAMED_STREAMS"></span>**Unterstützt benannte Streams** (262144)</span><span class="sxs-lookup"><span data-stu-id="dd060-414"><span id="Supports_Named_Streams"></span><span id="supports_named_streams"></span><span id="SUPPORTS_NAMED_STREAMS"></span>**Supports Named Streams** (262144)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-415">Das Dateisystem unterstützt benannte Datenströme.</span><span class="sxs-lookup"><span data-stu-id="dd060-415">The file system supports named streams.</span></span>

</dd> </dl>

<span data-ttu-id="dd060-416">Beispiel: 0</span><span class="sxs-lookup"><span data-stu-id="dd060-416">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="dd060-417">**Id**</span><span class="sxs-lookup"><span data-stu-id="dd060-417">**Id**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd060-418">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dd060-418">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd060-419">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd060-419">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd060-420">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| File Functions \| GetDriveType")</span><span class="sxs-lookup"><span data-stu-id="dd060-420">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|GetDriveType")</span></span>
</dt> </dl>

<span data-ttu-id="dd060-421">Laufwerk Buchstabe, der dieses CD-ROM-Laufwerk eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="dd060-421">Drive letter that uniquely identifies this CD-ROM drive.</span></span>

<span data-ttu-id="dd060-422">Beispiel: "d: \\ "</span><span class="sxs-lookup"><span data-stu-id="dd060-422">Example: "d:\\"</span></span>

</dd> <dt>

<span data-ttu-id="dd060-423">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="dd060-423">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd060-424">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="dd060-424">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="dd060-425">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd060-425">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd060-426">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="dd060-426">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="dd060-427">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="dd060-427">Date and time the object is installed.</span></span> <span data-ttu-id="dd060-428">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="dd060-428">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="dd060-429">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dd060-429">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd060-430">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="dd060-430">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd060-431">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dd060-431">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd060-432">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd060-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd060-433">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="dd060-433">Last error code reported by the logical device.</span></span>

<span data-ttu-id="dd060-434">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dd060-434">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd060-435">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="dd060-435">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd060-436">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dd060-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd060-437">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd060-437">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd060-438">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span><span class="sxs-lookup"><span data-stu-id="dd060-438">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span></span>
</dt> </dl>

<span data-ttu-id="dd060-439">Hersteller des Windows-CD-ROM-Laufwerks.</span><span class="sxs-lookup"><span data-stu-id="dd060-439">Manufacturer of the Windows CD-ROM drive.</span></span>

<span data-ttu-id="dd060-440">Beispiel: "Plextor"</span><span class="sxs-lookup"><span data-stu-id="dd060-440">Example: "PLEXTOR"</span></span>

</dd> <dt>

<span data-ttu-id="dd060-441">**Maxblocksize**</span><span class="sxs-lookup"><span data-stu-id="dd060-441">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd060-442">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="dd060-442">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dd060-443">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd060-443">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd060-444">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="dd060-444">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="dd060-445">Maximale Blockgröße (in Bytes) für Medien, auf die dieses Gerät zugreift.</span><span class="sxs-lookup"><span data-stu-id="dd060-445">Maximum block size, in bytes, for media accessed by this device.</span></span>

<span data-ttu-id="dd060-446">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dd060-446">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="dd060-447">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="dd060-447">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="dd060-448">**MaximumComponentLength**</span><span class="sxs-lookup"><span data-stu-id="dd060-448">**MaximumComponentLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd060-449">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dd060-449">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd060-450">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd060-450">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd060-451">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| File System Functions \| [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span><span class="sxs-lookup"><span data-stu-id="dd060-451">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span></span>
</dt> </dl>

<span data-ttu-id="dd060-452">Maximale Länge einer vom Windows-CD-ROM-Laufwerk unterstützten Dateinamen Komponente.</span><span class="sxs-lookup"><span data-stu-id="dd060-452">Maximum length of a filename component supported by the Windows CD-ROM drive.</span></span> <span data-ttu-id="dd060-453">Eine Dateinamen Komponente der Teil eines Datei namens zwischen umgekehrten Schrägstrichen.</span><span class="sxs-lookup"><span data-stu-id="dd060-453">A file name component the portion of a file name between backslashes.</span></span> <span data-ttu-id="dd060-454">Der Wert kann verwendet werden, um anzugeben, dass lange Namen vom angegebenen Dateisystem unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="dd060-454">The value can be used to indicate that long names are supported by the specified file system.</span></span> <span data-ttu-id="dd060-455">Beispielsweise speichert die Funktion für ein FAT-Dateisystem, das lange Namen unterstützt, den Wert 255 und nicht den vorherigen 8,3-Indikator.</span><span class="sxs-lookup"><span data-stu-id="dd060-455">For example, for a FAT file system supporting long names, the function stores the value 255, rather than the previous 8.3 indicator.</span></span> <span data-ttu-id="dd060-456">Lange Namen können auch auf Systemen unterstützt werden, die das NTFS-Dateisystem verwenden.</span><span class="sxs-lookup"><span data-stu-id="dd060-456">Long names can also be supported on systems that use the NTFS file system.</span></span>

<span data-ttu-id="dd060-457">Beispiel: 255</span><span class="sxs-lookup"><span data-stu-id="dd060-457">Example: 255</span></span>

</dd> <dt>

<span data-ttu-id="dd060-458">**Maxmediasize**</span><span class="sxs-lookup"><span data-stu-id="dd060-458">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd060-459">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="dd060-459">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dd060-460">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd060-460">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd060-461">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| sequenzielle Zugriffsgeräte \| 001,2 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Kilobyte ")</span><span class="sxs-lookup"><span data-stu-id="dd060-461">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="dd060-462">Maximale Größe des von diesem Gerät unterstützten Mediums in Kilobyte.</span><span class="sxs-lookup"><span data-stu-id="dd060-462">Maximum size, in kilobytes, of media supported by this device.</span></span>

<span data-ttu-id="dd060-463">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dd060-463">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="dd060-464">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="dd060-464">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="dd060-465">**MediaLoaded**</span><span class="sxs-lookup"><span data-stu-id="dd060-465">**MediaLoaded**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd060-466">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="dd060-466">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dd060-467">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd060-467">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd060-468">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| File System Functions \| [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span><span class="sxs-lookup"><span data-stu-id="dd060-468">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span></span>
</dt> </dl>

<span data-ttu-id="dd060-469">**True** gibt an, dass sich eine CD-ROM auf dem Laufwerk befindet.</span><span class="sxs-lookup"><span data-stu-id="dd060-469">If **True**, a CD-ROM is in the drive.</span></span>

</dd> <dt>

<span data-ttu-id="dd060-470">**MediaType**</span><span class="sxs-lookup"><span data-stu-id="dd060-470">**MediaType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd060-471">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dd060-471">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd060-472">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd060-472">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd060-473">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| GetDriveType")</span><span class="sxs-lookup"><span data-stu-id="dd060-473">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|GetDriveType")</span></span>
</dt> </dl>

<span data-ttu-id="dd060-474">Typ des Mediums, das von diesem Gerät verwendet werden kann oder auf das zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="dd060-474">Type of media that can be used or accessed by this device.</span></span> <span data-ttu-id="dd060-475">Dabei sind folgende Werte möglich:</span><span class="sxs-lookup"><span data-stu-id="dd060-475">Possible values are:</span></span>

<dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="dd060-476">**Zufälliger Zugriff** ("zufälliger Zugriff")</span><span class="sxs-lookup"><span data-stu-id="dd060-476">**Random Access** ("Random Access")</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="dd060-477">**Unterstützt das Schreiben** ("unterstützt Schreibvorgänge")</span><span class="sxs-lookup"><span data-stu-id="dd060-477">**Supports Writing** ("Supports Writing")</span></span>


</dt> <dd></dd> <dt>

<span id="Removable_Media"></span><span id="removable_media"></span><span id="REMOVABLE_MEDIA"></span>

<span data-ttu-id="dd060-478">Wechsel **Medien** ("Wechselmedien")</span><span class="sxs-lookup"><span data-stu-id="dd060-478">**Removable Media** ("Removable Media")</span></span>


</dt> <dd></dd> <dt>

<span id="CD-ROM"></span><span id="cd-rom"></span>

<span data-ttu-id="dd060-479">**CD-ROM** ("CD-ROM")</span><span class="sxs-lookup"><span data-stu-id="dd060-479">**CD-ROM** ("CD-ROM")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dd060-480">**MfrAssignedRevisionLevel**</span><span class="sxs-lookup"><span data-stu-id="dd060-480">**MfrAssignedRevisionLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd060-481">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dd060-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd060-482">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd060-482">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd060-483">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win2000DDK \| kernelmodedrivers \| [**Storage \_ Device \_ Descriptor**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor) \| productrevisionoffset")</span><span class="sxs-lookup"><span data-stu-id="dd060-483">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win2000DDK\|KernelModeDrivers\|[**STORAGE\_DEVICE\_DESCRIPTOR**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor)\|ProductRevisionOffset")</span></span>
</dt> </dl>

<span data-ttu-id="dd060-484">Die firmwarerevisions-Ebene, die vom Hersteller zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="dd060-484">Firmware revision level that is assigned by the manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="dd060-485">**Minblocksize**</span><span class="sxs-lookup"><span data-stu-id="dd060-485">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd060-486">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="dd060-486">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dd060-487">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd060-487">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd060-488">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="dd060-488">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="dd060-489">Minimale Blockgröße (in Bytes) für Medien, auf die dieses Gerät zugreift.</span><span class="sxs-lookup"><span data-stu-id="dd060-489">Minimum block size, in bytes, for media accessed by this device.</span></span>

<span data-ttu-id="dd060-490">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dd060-490">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="dd060-491">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="dd060-491">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="dd060-492">**Name**</span><span class="sxs-lookup"><span data-stu-id="dd060-492">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd060-493">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dd060-493">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd060-494">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd060-494">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd060-495">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="dd060-495">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="dd060-496">Die Bezeichnung für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="dd060-496">Label for the object.</span></span> <span data-ttu-id="dd060-497">Bei einer Unterklasse kann die Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="dd060-497">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="dd060-498">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dd060-498">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd060-499">**Unnötig**</span><span class="sxs-lookup"><span data-stu-id="dd060-499">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd060-500">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="dd060-500">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dd060-501">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd060-501">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd060-502">**True** gibt an, dass das Medien Zugriffsgerät bereinigt werden muss.</span><span class="sxs-lookup"><span data-stu-id="dd060-502">If **True**, the media access device needs cleaning.</span></span> <span data-ttu-id="dd060-503">Ob manuelle oder automatische Bereinigung möglich ist, wird in der Eigenschaft **Funktionen** angegeben.</span><span class="sxs-lookup"><span data-stu-id="dd060-503">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** property.</span></span>

<span data-ttu-id="dd060-504">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dd060-504">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd060-505">**"Numofmediasupportiert"**</span><span class="sxs-lookup"><span data-stu-id="dd060-505">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd060-506">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dd060-506">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd060-507">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd060-507">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd060-508">Maximale Anzahl von Medien, die unterstützt oder eingefügt werden können, wenn das Medien Zugriffsgerät mehrere einzelne Medien unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dd060-508">Maximum number of media that can be supported or inserted, when the media access device supports multiple individual media.</span></span>

<span data-ttu-id="dd060-509">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dd060-509">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd060-510">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="dd060-510">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd060-511">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dd060-511">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd060-512">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd060-512">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd060-513">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="dd060-513">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="dd060-514">Windows Plug & Play Geräte Bezeichner des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="dd060-514">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="dd060-515">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dd060-515">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="dd060-516">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="dd060-516">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="dd060-517">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="dd060-517">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd060-518">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="dd060-518">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="dd060-519">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd060-519">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd060-520">Array der spezifischen energiebezogenen Funktionen eines logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="dd060-520">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="dd060-521">Diese Eigenschaft wird von **CIM \_ LogicalDevice** geerbt.</span><span class="sxs-lookup"><span data-stu-id="dd060-521">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dd060-522"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="dd060-522"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="dd060-523"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="dd060-523"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-524">Energiebezogene Kapazitäten werden für dieses Gerät nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dd060-524">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="dd060-525"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="dd060-525"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="dd060-526"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="dd060-526"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-527">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="dd060-527">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="dd060-528"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="dd060-528"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-529">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="dd060-529">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="dd060-530"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="dd060-530"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-531">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dd060-531">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="dd060-532">Diese Methode wird in der übergeordneten **CIM \_ LogicalDevice** -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="dd060-532">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="dd060-533">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="dd060-533">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="dd060-534"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="dd060-534"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-535">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState*-Parameter auf 5 (Power Cycle) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="dd060-535">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="dd060-536"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="dd060-536"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="dd060-537">Zeitgesteuerte Power-On unterstützt</span><span class="sxs-lookup"><span data-stu-id="dd060-537">Timed Power-On Supported</span></span>

<span data-ttu-id="dd060-538">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) und die *Uhrzeit* auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="dd060-538">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="dd060-539">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="dd060-539">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd060-540">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="dd060-540">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dd060-541">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd060-541">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd060-542">**True** gibt an, dass das Gerät Energie gesteuert werden kann. Dies bedeutet, dass es in den Unterbrechungs Modus versetzt werden kann usw.</span><span class="sxs-lookup"><span data-stu-id="dd060-542">If **True**, the device can be power-managed, which means that it can be put into suspend mode, and so on.</span></span> <span data-ttu-id="dd060-543">Die-Eigenschaft gibt nicht an, dass die Energie Verwaltungsfunktionen zurzeit aktiviert sind, sondern nur, dass das logische Gerät für die Energie Verwaltung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="dd060-543">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="dd060-544">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dd060-544">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd060-545">**Revisions Ebene**</span><span class="sxs-lookup"><span data-stu-id="dd060-545">**RevisionLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd060-546">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dd060-546">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd060-547">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd060-547">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd060-548">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| Revisions Level")</span><span class="sxs-lookup"><span data-stu-id="dd060-548">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|RevisionLevel")</span></span>
</dt> </dl>

<span data-ttu-id="dd060-549">Firmwarerevisions-Ebene des Windows-CD-ROM-Laufwerks.</span><span class="sxs-lookup"><span data-stu-id="dd060-549">Firmware revision level of the Windows CD-ROM drive.</span></span>

</dd> <dt>

<span data-ttu-id="dd060-550">**SCSIBus**</span><span class="sxs-lookup"><span data-stu-id="dd060-550">**SCSIBus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd060-551">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dd060-551">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd060-552">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd060-552">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd060-553">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| SCSI Structures \| [**SCSI \_ Request \_ Block**](/windows-hardware/drivers/ddi/content/srb/ns-srb-_scsi_request_block) \| pathid")</span><span class="sxs-lookup"><span data-stu-id="dd060-553">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|SCSI Structures\|[**SCSI\_REQUEST\_BLOCK**](/windows-hardware/drivers/ddi/content/srb/ns-srb-_scsi_request_block)\|PathId")</span></span>
</dt> </dl>

<span data-ttu-id="dd060-554">SCSI-Busnummer für das Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="dd060-554">SCSI bus number for the disk drive.</span></span>

<span data-ttu-id="dd060-555">Beispiel: 0</span><span class="sxs-lookup"><span data-stu-id="dd060-555">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="dd060-556">**SCSILogicalUnit**</span><span class="sxs-lookup"><span data-stu-id="dd060-556">**SCSILogicalUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd060-557">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dd060-557">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dd060-558">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd060-558">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd060-559">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| SCSI-Strukturen \| [**SCSI- \_ Anforderungs \_ Block**](/windows-hardware/drivers/ddi/content/srb/ns-srb-_scsi_request_block)- \| LUN")</span><span class="sxs-lookup"><span data-stu-id="dd060-559">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|SCSI Structures\|[**SCSI\_REQUEST\_BLOCK**](/windows-hardware/drivers/ddi/content/srb/ns-srb-_scsi_request_block)\|Lun")</span></span>
</dt> </dl>

<span data-ttu-id="dd060-560">Die SCSI-logische Gerätenummer (LUN) des Laufwerks.</span><span class="sxs-lookup"><span data-stu-id="dd060-560">SCSI logical unit number (LUN) of the disk drive.</span></span> <span data-ttu-id="dd060-561">Die LUN wird verwendet, um anzugeben, auf welchen SCSI-Controller in einem System zugegriffen wird, auf dem mehr als ein Controller verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dd060-561">The LUN is used to designate which SCSI controller is being accessed in a system with more than one controller being used.</span></span> <span data-ttu-id="dd060-562">Der SCSI-Geräte Bezeichner ist ähnlich, aber er ist die Bezeichnung für mehrere Geräte auf einem Controller.</span><span class="sxs-lookup"><span data-stu-id="dd060-562">The SCSI device identifier is similar, but is the designation for multiple devices on one controller.</span></span>

<span data-ttu-id="dd060-563">Beispiel: 0</span><span class="sxs-lookup"><span data-stu-id="dd060-563">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="dd060-564">**SCSIPort**</span><span class="sxs-lookup"><span data-stu-id="dd060-564">**SCSIPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd060-565">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dd060-565">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dd060-566">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd060-566">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd060-567">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| SCSI Structures \| [**SCSI \_ Request \_ Block**](/windows-hardware/drivers/ddi/content/srb/ns-srb-_scsi_request_block) \| ScsiStatus")</span><span class="sxs-lookup"><span data-stu-id="dd060-567">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|SCSI Structures\|[**SCSI\_REQUEST\_BLOCK**](/windows-hardware/drivers/ddi/content/srb/ns-srb-_scsi_request_block)\|ScsiStatus")</span></span>
</dt> </dl>

<span data-ttu-id="dd060-568">SCSI-Portnummer des Laufwerks.</span><span class="sxs-lookup"><span data-stu-id="dd060-568">SCSI port number of the disk drive.</span></span>

<span data-ttu-id="dd060-569">Beispiel: 1</span><span class="sxs-lookup"><span data-stu-id="dd060-569">Example: 1</span></span>

</dd> <dt>

<span data-ttu-id="dd060-570">**SCSITargetId**</span><span class="sxs-lookup"><span data-stu-id="dd060-570">**SCSITargetId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd060-571">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dd060-571">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dd060-572">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd060-572">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd060-573">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| enviceiocontrol \| IOCTL \_ SCSI \_ get \_ Address")</span><span class="sxs-lookup"><span data-stu-id="dd060-573">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|DeviceIoControl\|IOCTL\_SCSI\_GET\_ADDRESS")</span></span>
</dt> </dl>

<span data-ttu-id="dd060-574">SCSI-Bezeichnernummer des Windows-CD-ROM-Laufwerks.</span><span class="sxs-lookup"><span data-stu-id="dd060-574">SCSI identifier number of the Windows CD-ROM drive.</span></span>

<span data-ttu-id="dd060-575">Beispiel: 0</span><span class="sxs-lookup"><span data-stu-id="dd060-575">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="dd060-576">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="dd060-576">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd060-577">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dd060-577">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd060-578">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd060-578">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd060-579">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Input and Output Structures \| [**Storage \_ Device \_ Descriptor**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor) \| serialnummerioffset")</span><span class="sxs-lookup"><span data-stu-id="dd060-579">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**STORAGE\_DEVICE\_DESCRIPTOR**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor)\|SerialNumberOffset")</span></span>
</dt> </dl>

<span data-ttu-id="dd060-580">Die Nummer, die vom Hersteller zur Identifizierung der physischen Medien angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="dd060-580">Number supplied by the manufacturer that identifies the physical media.</span></span> <span data-ttu-id="dd060-581">Beispiel: WD-WM3493798728.</span><span class="sxs-lookup"><span data-stu-id="dd060-581">Example: WD-WM3493798728.</span></span>

</dd> <dt>

<span data-ttu-id="dd060-582">**Größe**</span><span class="sxs-lookup"><span data-stu-id="dd060-582">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd060-583">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="dd060-583">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dd060-584">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd060-584">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd060-585">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| File Functions \| GetDiskFreeSpace"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="dd060-585">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|GetDiskFreeSpace"), [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="dd060-586">Größe des Laufwerks.</span><span class="sxs-lookup"><span data-stu-id="dd060-586">Size of the disk drive.</span></span>

<span data-ttu-id="dd060-587">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="dd060-587">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="dd060-588">**Status**</span><span class="sxs-lookup"><span data-stu-id="dd060-588">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd060-589">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dd060-589">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd060-590">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd060-590">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd060-591">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="dd060-591">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="dd060-592">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="dd060-592">Current status of the object.</span></span> <span data-ttu-id="dd060-593">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="dd060-593">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="dd060-594">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="dd060-594">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="dd060-595">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="dd060-595">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="dd060-596">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="dd060-596">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="dd060-597">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="dd060-597">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="dd060-598">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dd060-598">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="dd060-599">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="dd060-599">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="dd060-600">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="dd060-600">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="dd060-601">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="dd060-601">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="dd060-602">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="dd060-602">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dd060-603">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="dd060-603">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="dd060-604">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="dd060-604">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="dd060-605">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="dd060-605">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="dd060-606">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="dd060-606">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="dd060-607">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="dd060-607">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="dd060-608">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="dd060-608">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="dd060-609">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="dd060-609">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="dd060-610">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="dd060-610">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="dd060-611">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="dd060-611">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dd060-612">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="dd060-612">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd060-613">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dd060-613">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dd060-614">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd060-614">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd060-615">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="dd060-615">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="dd060-616">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="dd060-616">State of the logical device.</span></span> <span data-ttu-id="dd060-617">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 (nicht zutreffend) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dd060-617">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="dd060-618">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dd060-618">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dd060-619">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="dd060-619">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dd060-620">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="dd060-620">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="dd060-621">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="dd060-621">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="dd060-622">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="dd060-622">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="dd060-623">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="dd060-623">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dd060-624">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="dd060-624">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd060-625">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dd060-625">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd060-626">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd060-626">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd060-627">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="dd060-627">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="dd060-628">Der Wert der Eigenschaft " **kreationclassname** " des Bereichs Computers.</span><span class="sxs-lookup"><span data-stu-id="dd060-628">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="dd060-629">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dd060-629">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd060-630">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="dd060-630">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd060-631">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dd060-631">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd060-632">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd060-632">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd060-633">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="dd060-633">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="dd060-634">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="dd060-634">Name of the scoping system.</span></span>

<span data-ttu-id="dd060-635">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dd060-635">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dd060-636">**Übertragungsrate**</span><span class="sxs-lookup"><span data-stu-id="dd060-636">**TransferRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd060-637">Datentyp: **real64**</span><span class="sxs-lookup"><span data-stu-id="dd060-637">Data type: **real64**</span></span>
</dt> <dt>

<span data-ttu-id="dd060-638">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd060-638">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd060-639">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| Verweis-und Uhrzeit Referenz für Win32API"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Kilobyte pro Sekunde")</span><span class="sxs-lookup"><span data-stu-id="dd060-639">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Reference and Time Reference"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes per second")</span></span>
</dt> </dl>

<span data-ttu-id="dd060-640">Übertragungsrate des CD-ROM-Laufwerks.</span><span class="sxs-lookup"><span data-stu-id="dd060-640">Transfer rate of the CD-ROM drive.</span></span> <span data-ttu-id="dd060-641">Der Wert-1 gibt an, dass die Rate nicht bestimmt werden kann.</span><span class="sxs-lookup"><span data-stu-id="dd060-641">A value of -1 indicates that the rate cannot be determined.</span></span> <span data-ttu-id="dd060-642">In diesem Fall befindet sich die CD nicht auf dem Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="dd060-642">When this happens, the CD is not in the drive.</span></span>

</dd> <dt>

<span data-ttu-id="dd060-643">**Volumename**</span><span class="sxs-lookup"><span data-stu-id="dd060-643">**VolumeName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd060-644">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dd060-644">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd060-645">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd060-645">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd060-646">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| File System Functions \| [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span><span class="sxs-lookup"><span data-stu-id="dd060-646">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span></span>
</dt> </dl>

<span data-ttu-id="dd060-647">Der Volumename des Windows-CD-ROM-Laufwerks.</span><span class="sxs-lookup"><span data-stu-id="dd060-647">Volume name of the Windows CD-ROM drive.</span></span>

</dd> <dt>

<span data-ttu-id="dd060-648">**VolumeSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="dd060-648">**VolumeSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd060-649">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dd060-649">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd060-650">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dd060-650">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd060-651">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| File System Functions \| [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span><span class="sxs-lookup"><span data-stu-id="dd060-651">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span></span>
</dt> </dl>

<span data-ttu-id="dd060-652">Seriennummer des Mediums auf dem CD-ROM-Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="dd060-652">Volume serial number of the media in the CD-ROM drive.</span></span>

<span data-ttu-id="dd060-653">Beispiel: A8C3-D032</span><span class="sxs-lookup"><span data-stu-id="dd060-653">Example: A8C3-D032</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dd060-654">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dd060-654">Remarks</span></span>

<span data-ttu-id="dd060-655">Die **Win32 \_ cdromdrive** -Klasse wird von [**CIM \_ cdromdrive**](cim-cdromdrive.md) abgeleitet, das von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="dd060-655">The **Win32\_CDROMDrive** class is derived from [**CIM\_CDROMDrive**](cim-cdromdrive.md) which derives from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span> <span data-ttu-id="dd060-656">Die **CIM \_ mediaaccessdevice** -Klasse wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="dd060-656">The **CIM\_MediaAccessDevice** class derives from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="examples"></a><span data-ttu-id="dd060-657">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dd060-657">Examples</span></span>

<span data-ttu-id="dd060-658">Das folgende VBScript-Beispiel bestimmt, ob sich eine CD in einem Crom-Laufwerk befindet.</span><span class="sxs-lookup"><span data-stu-id="dd060-658">The following VBScript example determines if a CD is in a CDROM drive.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject(_
    "winmgmts:\\" & strComputer & "\root\cimv2")
Set colItems = objWMIService.ExecQuery( _
    "Select * from Win32_CDROMDrive")
For Each objItem in colItems
    Wscript.Echo "Device ID: " _
        & objItem.DeviceID
    Wscript.Echo "Media Loaded: " _
        & objItem.MediaLoaded
Next
```



## <a name="requirements"></a><span data-ttu-id="dd060-659">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dd060-659">Requirements</span></span>



| <span data-ttu-id="dd060-660">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dd060-660">Requirement</span></span> | <span data-ttu-id="dd060-661">Wert</span><span class="sxs-lookup"><span data-stu-id="dd060-661">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dd060-662">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dd060-662">Minimum supported client</span></span><br/> | <span data-ttu-id="dd060-663">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dd060-663">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dd060-664">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dd060-664">Minimum supported server</span></span><br/> | <span data-ttu-id="dd060-665">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dd060-665">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dd060-666">Namespace</span><span class="sxs-lookup"><span data-stu-id="dd060-666">Namespace</span></span><br/>                | <span data-ttu-id="dd060-667">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="dd060-667">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="dd060-668">MOF</span><span class="sxs-lookup"><span data-stu-id="dd060-668">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dd060-669"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="dd060-669"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="dd060-670">DLL</span><span class="sxs-lookup"><span data-stu-id="dd060-670">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd060-671"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd060-671"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd060-672">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dd060-672">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd060-673">**CIM- \_ cdromdrive**</span><span class="sxs-lookup"><span data-stu-id="dd060-673">**CIM\_CDROMDrive**</span></span>](cim-cdromdrive.md)
</dt> <dt>

[<span data-ttu-id="dd060-674">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="dd060-674">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="dd060-675">WMI-Tasks: Computer Hardware</span><span class="sxs-lookup"><span data-stu-id="dd060-675">WMI Tasks: Computer Hardware</span></span>](/windows/desktop/WmiSdk/wmi-tasks--computer-hardware)
</dt> <dt>

[<span data-ttu-id="dd060-676">WMI-Tasks: Datenträger und Dateisysteme</span><span class="sxs-lookup"><span data-stu-id="dd060-676">WMI Tasks: Disks and File Systems</span></span>](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems)
</dt> </dl>

 

