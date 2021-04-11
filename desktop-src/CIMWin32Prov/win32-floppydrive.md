---
description: Die \_ WMI-Klasse von Win32 floppydrive verwaltet die Funktionen eines Disketten Laufwerks.
ms.assetid: 41823eeb-4831-4deb-a798-7b3589ebf3e2
ms.tgt_platform: multiple
title: Win32_FloppyDrive-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_FloppyDrive
- Win32_FloppyDrive.Reset
- Win32_FloppyDrive.SetPowerState
- Win32_FloppyDrive.Availability
- Win32_FloppyDrive.Capabilities
- Win32_FloppyDrive.CapabilityDescriptions
- Win32_FloppyDrive.Caption
- Win32_FloppyDrive.CompressionMethod
- Win32_FloppyDrive.ConfigManagerErrorCode
- Win32_FloppyDrive.ConfigManagerUserConfig
- Win32_FloppyDrive.CreationClassName
- Win32_FloppyDrive.DefaultBlockSize
- Win32_FloppyDrive.Description
- Win32_FloppyDrive.DeviceID
- Win32_FloppyDrive.ErrorCleared
- Win32_FloppyDrive.ErrorDescription
- Win32_FloppyDrive.ErrorMethodology
- Win32_FloppyDrive.InstallDate
- Win32_FloppyDrive.LastErrorCode
- Win32_FloppyDrive.Manufacturer
- Win32_FloppyDrive.MaxBlockSize
- Win32_FloppyDrive.MaxMediaSize
- Win32_FloppyDrive.MinBlockSize
- Win32_FloppyDrive.Name
- Win32_FloppyDrive.NeedsCleaning
- Win32_FloppyDrive.NumberOfMediaSupported
- Win32_FloppyDrive.PNPDeviceID
- Win32_FloppyDrive.PowerManagementCapabilities
- Win32_FloppyDrive.PowerManagementSupported
- Win32_FloppyDrive.Status
- Win32_FloppyDrive.StatusInfo
- Win32_FloppyDrive.SystemCreationClassName
- Win32_FloppyDrive.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 832b5fad0ce54d1436fd6b2e47765af0fabfd2bb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127332"
---
# <a name="win32_floppydrive-class"></a><span data-ttu-id="9f400-103">Win32 \_ floppydrive-Klasse</span><span class="sxs-lookup"><span data-stu-id="9f400-103">Win32\_FloppyDrive class</span></span>

<span data-ttu-id="9f400-104">\[**Win32 \_ Floppydrive** ist nicht mehr für die Verwendung ab Windows 10 und Windows Server 2016 verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="9f400-104">\[**Win32\_FloppyDrive** is no longer available for use as of Windows 10 and Windows Server 2016.\]</span></span>

<span data-ttu-id="9f400-105">Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) von **Win32 \_ floppydrive** verwaltet die Funktionen eines Disketten Laufwerks.</span><span class="sxs-lookup"><span data-stu-id="9f400-105">The **Win32\_FloppyDrive** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) manages the functions of a floppy disk drive.</span></span>

<span data-ttu-id="9f400-106">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9f400-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="9f400-107">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="9f400-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f400-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9f400-108">Syntax</span></span>

``` syntax
[Dynamic, provider("CIMWin32"), UUID("{FB1F3A64-BBAC-11d2-85E5-0000F8102E5F}"), AMENDMENT]
class Win32_FloppyDrive : CIM_DisketteDrive
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
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Manufacturer;
  uint64   MaxBlockSize;
  uint64   MaxMediaSize;
  uint64   MinBlockSize;
  string   Name;
  boolean  NeedsCleaning;
  uint32   NumberOfMediaSupported;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="9f400-109">Member</span><span class="sxs-lookup"><span data-stu-id="9f400-109">Members</span></span>

<span data-ttu-id="9f400-110">Die **Win32 \_ floppydrive** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="9f400-110">The **Win32\_FloppyDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="9f400-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="9f400-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="9f400-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9f400-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9f400-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="9f400-113">Methods</span></span>

<span data-ttu-id="9f400-114">Die **Win32 \_ floppydrive** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="9f400-114">The **Win32\_FloppyDrive** class has these methods.</span></span>



| <span data-ttu-id="9f400-115">Methode</span><span class="sxs-lookup"><span data-stu-id="9f400-115">Method</span></span>            | <span data-ttu-id="9f400-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9f400-116">Description</span></span>                                                                                                                                                                                                                   |
|:------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f400-117">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="9f400-117">**Reset**</span></span>         | <span data-ttu-id="9f400-118">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="9f400-118">Not implemented.</span></span> <span data-ttu-id="9f400-119">Weitere Informationen zur Implementierung dieser Methode finden Sie unter der [**Reset**](reset-method-in-class-cim-controller.md) -Methode in [**CIM \_ diskettedrive**](cim-diskettedrive.md).</span><span class="sxs-lookup"><span data-stu-id="9f400-119">For more information about how to implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_DisketteDrive**](cim-diskettedrive.md).</span></span><br/>                 |
| <span data-ttu-id="9f400-120">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="9f400-120">**SetPowerState**</span></span> | <span data-ttu-id="9f400-121">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="9f400-121">Not implemented.</span></span> <span data-ttu-id="9f400-122">Weitere Informationen zur Implementierung dieser Methode finden Sie unter der [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode in [**CIM \_ diskettedrive**](cim-diskettedrive.md).</span><span class="sxs-lookup"><span data-stu-id="9f400-122">For more information about how to implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_DisketteDrive**](cim-diskettedrive.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="9f400-123">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9f400-123">Properties</span></span>

<span data-ttu-id="9f400-124">Die **Win32 \_ floppydrive** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9f400-124">The **Win32\_FloppyDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9f400-125">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="9f400-125">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f400-126">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9f400-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9f400-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f400-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f400-128">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="9f400-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="9f400-129">Der Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="9f400-129">Status of the device.</span></span>

<span data-ttu-id="9f400-130">Diese Eigenschaft wird von [ **CIM \_ LogicalDevice** geerbt.](cim-logicaldevice.md)</span><span class="sxs-lookup"><span data-stu-id="9f400-130">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md)</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9f400-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="9f400-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9f400-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="9f400-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="9f400-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="9f400-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="9f400-134">Ausführung oder vollständiger Stromversorgung</span><span class="sxs-lookup"><span data-stu-id="9f400-134">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="9f400-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="9f400-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="9f400-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="9f400-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="9f400-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="9f400-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="9f400-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="9f400-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="9f400-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="9f400-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="9f400-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="9f400-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="9f400-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="9f400-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="9f400-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="9f400-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="9f400-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="9f400-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="9f400-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="9f400-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="9f400-145">Energiespeicher-unbekannt</span><span class="sxs-lookup"><span data-stu-id="9f400-145">Power Save - Unknown</span></span>

<span data-ttu-id="9f400-146">Das Gerät befindet sich im Energiesparmodus, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="9f400-146">The device in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="9f400-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="9f400-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="9f400-148">Energiesparmodus-niedriger Energie Modus</span><span class="sxs-lookup"><span data-stu-id="9f400-148">Power Save - Low Power Mode</span></span>

<span data-ttu-id="9f400-149">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="9f400-149">The device is in a power save state, but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="9f400-150"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="9f400-150"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="9f400-151">Energiesparmodus-Standby</span><span class="sxs-lookup"><span data-stu-id="9f400-151">Power Save - Standby</span></span>

<span data-ttu-id="9f400-152">Das Gerät funktioniert nicht, kann jedoch schnell wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="9f400-152">The device is not functioning, but can be quickly restored to full-power.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="9f400-153"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="9f400-153"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="9f400-154"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="9f400-154"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="9f400-155">Energiespeicher-Warnung</span><span class="sxs-lookup"><span data-stu-id="9f400-155">Power Save - Warning</span></span>

<span data-ttu-id="9f400-156">Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="9f400-156">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="9f400-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="9f400-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="9f400-158">Das Gerät wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="9f400-158">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="9f400-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="9f400-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="9f400-160">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="9f400-160">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="9f400-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="9f400-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="9f400-162">Das Gerät ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="9f400-162">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="9f400-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="9f400-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="9f400-164">Das Gerät ist in Ruhe.</span><span class="sxs-lookup"><span data-stu-id="9f400-164">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9f400-165">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="9f400-165">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f400-166">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="9f400-166">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9f400-167">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f400-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f400-168">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergeräte \| 001,9 "," MIF. DMTF- \| Speichergeräte \| 001,11 "," MIF. DMTF- \| Speichergeräte \| 001,12 "," MIF. DMTF-Datenträger \| \| 003,7 "), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md).**Capabilitybeschreibungen**")</span><span class="sxs-lookup"><span data-stu-id="9f400-168">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="9f400-169">Array von Funktionen des Medien Zugriffs Geräts.</span><span class="sxs-lookup"><span data-stu-id="9f400-169">Array of capabilities of the media access device.</span></span> <span data-ttu-id="9f400-170">Beispielsweise kann das Gerät zufälligen Zugriff, Wechsel Datenträger und Automatisches Bereinigen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="9f400-170">For example, the device may support Random Access, Removable Media, and Automatic Cleaning.</span></span> <span data-ttu-id="9f400-171">In diesem Fall werden die Werte 3, 7 und 9 in das Array geschrieben.</span><span class="sxs-lookup"><span data-stu-id="9f400-171">In this case, the values 3, 7, and 9 would be written to the array.</span></span>

<span data-ttu-id="9f400-172">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9f400-172">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9f400-173"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="9f400-173"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9f400-174"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="9f400-174"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="9f400-175"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequenzieller Zugriff** (2)</span><span class="sxs-lookup"><span data-stu-id="9f400-175"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="9f400-176"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Zufälliger Zugriff** (3)</span><span class="sxs-lookup"><span data-stu-id="9f400-176"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="9f400-177"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Unterstützt Schreib** Vorgänge (4)</span><span class="sxs-lookup"><span data-stu-id="9f400-177"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="9f400-178"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Verschlüsselung** (5)</span><span class="sxs-lookup"><span data-stu-id="9f400-178"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="9f400-179"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Komprimierung** (6)</span><span class="sxs-lookup"><span data-stu-id="9f400-179"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="9f400-180"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Unterstützt Removeable Media** (7)</span><span class="sxs-lookup"><span data-stu-id="9f400-180"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="9f400-181">Unterstützt Wechselmedien</span><span class="sxs-lookup"><span data-stu-id="9f400-181">Supports Removable Media</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="9f400-182"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manuelle Reinigung** (8)</span><span class="sxs-lookup"><span data-stu-id="9f400-182"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="9f400-183"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatische Bereinigung** (9)</span><span class="sxs-lookup"><span data-stu-id="9f400-183"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="9f400-184"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**Smart Notification** (10)</span><span class="sxs-lookup"><span data-stu-id="9f400-184"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="9f400-185"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Unterstützt zweiseitige Medien** (11)</span><span class="sxs-lookup"><span data-stu-id="9f400-185"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="9f400-186">Unterstützt Dual-Sided Medien</span><span class="sxs-lookup"><span data-stu-id="9f400-186">Supports Dual-Sided Media</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="9f400-187"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount-eject nicht erforderlich** (12)</span><span class="sxs-lookup"><span data-stu-id="9f400-187"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9f400-188">**Capabilitybeschreibungen**</span><span class="sxs-lookup"><span data-stu-id="9f400-188">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f400-189">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="9f400-189">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9f400-190">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f400-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f400-191">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md).**Funktionen**")</span><span class="sxs-lookup"><span data-stu-id="9f400-191">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="9f400-192">Ein Array von frei Handzeichen folgen, das Ausführlichere Erläuterungen zu allen seriellen Controller Features bereitstellt, die im **Funktions Array angegeben** sind.</span><span class="sxs-lookup"><span data-stu-id="9f400-192">Array of free-form strings providing more detailed explanations for any of the serial controller features indicated in the **Capabilities** array.</span></span> <span data-ttu-id="9f400-193">Beachten Sie, dass jeder Eintrag dieses Arrays mit dem Eintrag im **Funktions Array verknüpft ist, der sich** am selben Index befindet.</span><span class="sxs-lookup"><span data-stu-id="9f400-193">Note, each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

<span data-ttu-id="9f400-194">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9f400-194">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f400-195">**Caption**</span><span class="sxs-lookup"><span data-stu-id="9f400-195">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f400-196">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9f400-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f400-197">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f400-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f400-198">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="9f400-198">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="9f400-199">Kurze Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="9f400-199">Short description of the object.</span></span>

<span data-ttu-id="9f400-200">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9f400-200">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f400-201">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="9f400-201">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f400-202">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9f400-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f400-203">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f400-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f400-204">Freie Formular Zeichenfolge, die den Algorithmus oder das Tool angibt, mit dem das Gerät die Komprimierung unterstützt</span><span class="sxs-lookup"><span data-stu-id="9f400-204">Free form string indicating the algorithm or tool used by the device to support compression.</span></span> <span data-ttu-id="9f400-205">Wenn es nicht möglich oder nicht erwünscht ist, das Komprimierungs Schema zu beschreiben (weil es möglicherweise nicht bekannt ist), verwenden Sie "unknown", um darzustellen, dass es nicht bekannt ist, ob das Gerät Komprimierungs Funktionen unterstützt. "Komprimiert", um darzustellen, dass das Gerät Komprimierungs Funktionen unterstützt, aber entweder ist das Komprimierungs Schema nicht bekannt oder nicht offengelegt. und "nicht komprimiert", um darzustellen, dass das Gerät keine Komprimierungs Funktionen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9f400-205">If it is not possible or not desired to describe the compression scheme (perhaps because it is not known), use "Unknown" to represent that it is not known whether the device supports compression capabilities or not; "Compressed" to represent that the device supports compression capabilities, but either its compression scheme is not known or not disclosed; and "Not Compressed" to represent that the device does not support compression capabilities.</span></span>

<span data-ttu-id="9f400-206">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9f400-206">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>



 <span data-ttu-id="9f400-207">("Unbekannt")</span><span class="sxs-lookup"><span data-stu-id="9f400-207">("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="9f400-208">Das Komprimierungs Schema ist unbekannt oder nicht beschrieben.</span><span class="sxs-lookup"><span data-stu-id="9f400-208">The compression scheme is unknown or not described.</span></span>

</dd> <dt>



 <span data-ttu-id="9f400-209">("Komprimiert")</span><span class="sxs-lookup"><span data-stu-id="9f400-209">("Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="9f400-210">Die logische Datei ist komprimiert, das Komprimierungs Schema ist jedoch unbekannt oder nicht beschrieben.</span><span class="sxs-lookup"><span data-stu-id="9f400-210">The logical file is compressed, but the compression scheme is unknown or not described</span></span>

</dd> <dt>



 <span data-ttu-id="9f400-211">("Nicht komprimiert")</span><span class="sxs-lookup"><span data-stu-id="9f400-211">("Not Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="9f400-212">Wenn die logische Datei nicht komprimiert ist</span><span class="sxs-lookup"><span data-stu-id="9f400-212">If the logical file is not compressed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9f400-213">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="9f400-213">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f400-214">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9f400-214">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f400-215">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f400-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f400-216">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="9f400-216">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="9f400-217">Windows Configuration Manager-Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="9f400-217">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="9f400-218">Diese Eigenschaft wird von [ **CIM \_ LogicalDevice** geerbt.](cim-logicaldevice.md)</span><span class="sxs-lookup"><span data-stu-id="9f400-218">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md)</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="9f400-219"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="9f400-219"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="9f400-220"> (0)</span><span class="sxs-lookup"><span data-stu-id="9f400-220">(0)</span></span>


</dt> <dd>

<span data-ttu-id="9f400-221">Das Gerät funktioniert ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="9f400-221">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="9f400-222"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="9f400-222"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="9f400-223">(1)</span><span class="sxs-lookup"><span data-stu-id="9f400-223">(1)</span></span>


</dt> <dd>

<span data-ttu-id="9f400-224">Das Gerät ist nicht ordnungsgemäß konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="9f400-224">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="9f400-225"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="9f400-225"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="9f400-226">(2)</span><span class="sxs-lookup"><span data-stu-id="9f400-226">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="9f400-227"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="9f400-227"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="9f400-228">(3)</span><span class="sxs-lookup"><span data-stu-id="9f400-228">(3)</span></span>


</dt> <dd>

<span data-ttu-id="9f400-229">Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt möglicherweise nicht über genügend Arbeitsspeicher oder andere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="9f400-229">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="9f400-230"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="9f400-230"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="9f400-231">(4)</span><span class="sxs-lookup"><span data-stu-id="9f400-231">(4)</span></span>


</dt> <dd>

<span data-ttu-id="9f400-232">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="9f400-232">Device is not working properly.</span></span> <span data-ttu-id="9f400-233">Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="9f400-233">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="9f400-234"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="9f400-234"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="9f400-235">(5)</span><span class="sxs-lookup"><span data-stu-id="9f400-235">(5)</span></span>


</dt> <dd>

<span data-ttu-id="9f400-236">Der Treiber für das Gerät erfordert eine Ressource, die von Windows nicht verwaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="9f400-236">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="9f400-237"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="9f400-237"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="9f400-238"> (6)</span><span class="sxs-lookup"><span data-stu-id="9f400-238">(6)</span></span>


</dt> <dd>

<span data-ttu-id="9f400-239">Die Startkonfiguration für das Gerät steht in Konflikt mit anderen Geräten.</span><span class="sxs-lookup"><span data-stu-id="9f400-239">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="9f400-240"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="9f400-240"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="9f400-241">(7)</span><span class="sxs-lookup"><span data-stu-id="9f400-241">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="9f400-242"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="9f400-242"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="9f400-243">(8)</span><span class="sxs-lookup"><span data-stu-id="9f400-243">(8)</span></span>


</dt> <dd>

<span data-ttu-id="9f400-244">Das Treiber Lade Modul für das Gerät fehlt.</span><span class="sxs-lookup"><span data-stu-id="9f400-244">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="9f400-245"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="9f400-245"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="9f400-246">(9)</span><span class="sxs-lookup"><span data-stu-id="9f400-246">(9)</span></span>


</dt> <dd>

<span data-ttu-id="9f400-247">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="9f400-247">Device is not working properly.</span></span> <span data-ttu-id="9f400-248">Die Steuerungs Firmware meldet nicht korrekt die Ressourcen für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="9f400-248">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="9f400-249"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="9f400-249"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="9f400-250">(10)</span><span class="sxs-lookup"><span data-stu-id="9f400-250">(10)</span></span>


</dt> <dd>

<span data-ttu-id="9f400-251">Das Gerät kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="9f400-251">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="9f400-252"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="9f400-252"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="9f400-253">(11)</span><span class="sxs-lookup"><span data-stu-id="9f400-253">(11)</span></span>


</dt> <dd>

<span data-ttu-id="9f400-254">Fehler beim Gerät.</span><span class="sxs-lookup"><span data-stu-id="9f400-254">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="9f400-255"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="9f400-255"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="9f400-256">(12)</span><span class="sxs-lookup"><span data-stu-id="9f400-256">(12)</span></span>


</dt> <dd>

<span data-ttu-id="9f400-257">Das Gerät kann nicht genug freie Ressourcen für die Verwendung finden.</span><span class="sxs-lookup"><span data-stu-id="9f400-257">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="9f400-258"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="9f400-258"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="9f400-259">(13)</span><span class="sxs-lookup"><span data-stu-id="9f400-259">(13)</span></span>


</dt> <dd>

<span data-ttu-id="9f400-260">Die Geräte Ressourcen können nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="9f400-260">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="9f400-261"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="9f400-261"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="9f400-262">(14)</span><span class="sxs-lookup"><span data-stu-id="9f400-262">(14)</span></span>


</dt> <dd>

<span data-ttu-id="9f400-263">Das Gerät kann erst ordnungsgemäß funktionieren, wenn der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="9f400-263">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="9f400-264"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="9f400-264"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="9f400-265">(15)</span><span class="sxs-lookup"><span data-stu-id="9f400-265">(15)</span></span>


</dt> <dd>

<span data-ttu-id="9f400-266">Das Gerät funktioniert aufgrund eines möglichen erneuten Aufzählungs Problems nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="9f400-266">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="9f400-267"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="9f400-267"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="9f400-268">(16)</span><span class="sxs-lookup"><span data-stu-id="9f400-268">(16)</span></span>


</dt> <dd>

<span data-ttu-id="9f400-269">In Windows können nicht alle Ressourcen identifiziert werden, die vom Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9f400-269">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="9f400-270"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="9f400-270"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="9f400-271">(17)</span><span class="sxs-lookup"><span data-stu-id="9f400-271">(17)</span></span>


</dt> <dd>

<span data-ttu-id="9f400-272">Das Gerät fordert einen unbekannten Ressourcentyp an.</span><span class="sxs-lookup"><span data-stu-id="9f400-272">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="9f400-273"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="9f400-273"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="9f400-274">(18)</span><span class="sxs-lookup"><span data-stu-id="9f400-274">(18)</span></span>


</dt> <dd>

<span data-ttu-id="9f400-275">Gerätetreiber müssen neu installiert werden.</span><span class="sxs-lookup"><span data-stu-id="9f400-275">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="9f400-276"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="9f400-276"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="9f400-277">(19)</span><span class="sxs-lookup"><span data-stu-id="9f400-277">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="9f400-278"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="9f400-278"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="9f400-279">(20)</span><span class="sxs-lookup"><span data-stu-id="9f400-279">(20)</span></span>


</dt> <dd>

<span data-ttu-id="9f400-280">Die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="9f400-280">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="9f400-281"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="9f400-281"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="9f400-282">(21)</span><span class="sxs-lookup"><span data-stu-id="9f400-282">(21)</span></span>


</dt> <dd>

<span data-ttu-id="9f400-283">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="9f400-283">System failure.</span></span> <span data-ttu-id="9f400-284">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="9f400-284">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="9f400-285">Das Gerät wird von Windows entfernt.</span><span class="sxs-lookup"><span data-stu-id="9f400-285">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="9f400-286"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="9f400-286"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="9f400-287">(22)</span><span class="sxs-lookup"><span data-stu-id="9f400-287">(22)</span></span>


</dt> <dd>

<span data-ttu-id="9f400-288">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="9f400-288">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="9f400-289"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="9f400-289"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="9f400-290">(23)</span><span class="sxs-lookup"><span data-stu-id="9f400-290">(23)</span></span>


</dt> <dd>

<span data-ttu-id="9f400-291">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="9f400-291">System failure.</span></span> <span data-ttu-id="9f400-292">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="9f400-292">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="9f400-293"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="9f400-293"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="9f400-294">(24)</span><span class="sxs-lookup"><span data-stu-id="9f400-294">(24)</span></span>


</dt> <dd>

<span data-ttu-id="9f400-295">Das Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.</span><span class="sxs-lookup"><span data-stu-id="9f400-295">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="9f400-296"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="9f400-296"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="9f400-297">(25)</span><span class="sxs-lookup"><span data-stu-id="9f400-297">(25)</span></span>


</dt> <dd>

<span data-ttu-id="9f400-298">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="9f400-298">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="9f400-299"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="9f400-299"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="9f400-300">(26)</span><span class="sxs-lookup"><span data-stu-id="9f400-300">(26)</span></span>


</dt> <dd>

<span data-ttu-id="9f400-301">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="9f400-301">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="9f400-302"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="9f400-302"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="9f400-303">(27)</span><span class="sxs-lookup"><span data-stu-id="9f400-303">(27)</span></span>


</dt> <dd>

<span data-ttu-id="9f400-304">Das Gerät verfügt nicht über eine gültige Protokoll Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="9f400-304">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="9f400-305"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="9f400-305"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="9f400-306">(28)</span><span class="sxs-lookup"><span data-stu-id="9f400-306">(28)</span></span>


</dt> <dd>

<span data-ttu-id="9f400-307">Gerätetreiber sind nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="9f400-307">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="9f400-308"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="9f400-308"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="9f400-309">(29)</span><span class="sxs-lookup"><span data-stu-id="9f400-309">(29)</span></span>


</dt> <dd>

<span data-ttu-id="9f400-310">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="9f400-310">Device is disabled.</span></span> <span data-ttu-id="9f400-311">Die Gerätefirmware hat nicht die erforderlichen Ressourcen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="9f400-311">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="9f400-312"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="9f400-312"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="9f400-313">(30)</span><span class="sxs-lookup"><span data-stu-id="9f400-313">(30)</span></span>


</dt> <dd>

<span data-ttu-id="9f400-314">Das Gerät verwendet eine UNQ-Ressource, die von einem anderen Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9f400-314">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="9f400-315"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="9f400-315"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="9f400-316">31,5</span><span class="sxs-lookup"><span data-stu-id="9f400-316">(31)</span></span>


</dt> <dd>

<span data-ttu-id="9f400-317">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="9f400-317">Device is not working properly.</span></span> <span data-ttu-id="9f400-318">Die erforderlichen Gerätetreiber können nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="9f400-318">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9f400-319">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="9f400-319">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f400-320">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="9f400-320">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9f400-321">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f400-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f400-322">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="9f400-322">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="9f400-323">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="9f400-323">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="9f400-324">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9f400-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f400-325">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="9f400-325">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f400-326">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9f400-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f400-327">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f400-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f400-328">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9f400-328">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9f400-329">Der Name der ersten konkreten Klasse, die in der Vererbungs Kette angezeigt werden soll, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9f400-329">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="9f400-330">Bei Verwendung mit den anderen Schlüsseleigenschaften der-Klasse ermöglicht die-Eigenschaft, dass alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="9f400-330">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="9f400-331">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9f400-331">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f400-332">**Defaultblocksize**</span><span class="sxs-lookup"><span data-stu-id="9f400-332">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f400-333">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9f400-333">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9f400-334">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f400-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f400-335">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="9f400-335">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="9f400-336">Standard Blockgröße (in Bytes) für dieses Gerät.</span><span class="sxs-lookup"><span data-stu-id="9f400-336">Default block size, in bytes, for this device.</span></span>

<span data-ttu-id="9f400-337">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9f400-337">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="9f400-338">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="9f400-338">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="9f400-339">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9f400-339">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f400-340">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9f400-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f400-341">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f400-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f400-342">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="9f400-342">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="9f400-343">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="9f400-343">Description of the object.</span></span>

<span data-ttu-id="9f400-344">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9f400-344">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f400-345">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="9f400-345">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f400-346">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9f400-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f400-347">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f400-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f400-348">Qualifizierer: [ **CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9f400-348">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9f400-349">Eindeutiger Bezeichner des Disketten Laufwerks mit anderen Geräten im System.</span><span class="sxs-lookup"><span data-stu-id="9f400-349">Unique identifier of the floppy disk drive with other devices on the system.</span></span>

<span data-ttu-id="9f400-350">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9f400-350">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f400-351">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="9f400-351">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f400-352">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="9f400-352">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9f400-353">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f400-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f400-354">**True** gibt an, dass der in **LastErrorCode** gemeldete Fehler jetzt gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="9f400-354">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="9f400-355">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9f400-355">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f400-356">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="9f400-356">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f400-357">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9f400-357">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f400-358">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f400-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f400-359">Eine frei Form Zeichenfolge, die weitere Informationen über den in **LastErrorCode** aufgezeichneten Fehler sowie Informationen zu eventuell durchzuführenden Korrekturmaßnahmen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="9f400-359">Free-form string that supplies more information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="9f400-360">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9f400-360">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f400-361">**Errormethodmethodologie**</span><span class="sxs-lookup"><span data-stu-id="9f400-361">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f400-362">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9f400-362">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f400-363">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f400-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f400-364">Eine frei Form Zeichenfolge, die den Typ der von diesem Gerät unterstützten Fehlererkennung und-Korrektur beschreibt.</span><span class="sxs-lookup"><span data-stu-id="9f400-364">Free-form string that describes the type of error detection and correction supported by this device.</span></span>

<span data-ttu-id="9f400-365">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9f400-365">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f400-366">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9f400-366">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f400-367">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="9f400-367">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9f400-368">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f400-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f400-369">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="9f400-369">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="9f400-370">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="9f400-370">Date and time the object was installed.</span></span> <span data-ttu-id="9f400-371">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="9f400-371">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="9f400-372">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9f400-372">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f400-373">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="9f400-373">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f400-374">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9f400-374">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f400-375">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f400-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f400-376">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="9f400-376">Last error code reported by the logical device.</span></span>

<span data-ttu-id="9f400-377">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9f400-377">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f400-378">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="9f400-378">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f400-379">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9f400-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f400-380">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f400-380">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f400-381">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span><span class="sxs-lookup"><span data-stu-id="9f400-381">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span></span>
</dt> </dl>

<span data-ttu-id="9f400-382">Der Name des Herstellers des Disketten Laufwerks.</span><span class="sxs-lookup"><span data-stu-id="9f400-382">Name of the manufacturer of the floppy disk drive.</span></span>

<span data-ttu-id="9f400-383">Beispiel: "Acme"</span><span class="sxs-lookup"><span data-stu-id="9f400-383">Example: "Acme"</span></span>

</dd> <dt>

<span data-ttu-id="9f400-384">**Maxblocksize**</span><span class="sxs-lookup"><span data-stu-id="9f400-384">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f400-385">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9f400-385">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9f400-386">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f400-386">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f400-387">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="9f400-387">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="9f400-388">Maximale Blockgröße (in Bytes) für Medien, auf die dieses Gerät zugreift.</span><span class="sxs-lookup"><span data-stu-id="9f400-388">Maximum block size, in bytes, for media accessed by this device.</span></span>

<span data-ttu-id="9f400-389">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9f400-389">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="9f400-390">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="9f400-390">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="9f400-391">**Maxmediasize**</span><span class="sxs-lookup"><span data-stu-id="9f400-391">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f400-392">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9f400-392">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9f400-393">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f400-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f400-394">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| sequenzielle Zugriffsgeräte \| 001,2 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Kilobyte ")</span><span class="sxs-lookup"><span data-stu-id="9f400-394">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="9f400-395">Maximale Größe des von diesem Gerät unterstützten Mediums in Kilobyte.</span><span class="sxs-lookup"><span data-stu-id="9f400-395">Maximum size, in kilobytes, of media supported by this device.</span></span>

<span data-ttu-id="9f400-396">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9f400-396">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="9f400-397">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="9f400-397">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="9f400-398">**Minblocksize**</span><span class="sxs-lookup"><span data-stu-id="9f400-398">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f400-399">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9f400-399">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9f400-400">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f400-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f400-401">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="9f400-401">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="9f400-402">Minimale Blockgröße (in Bytes) für Medien, auf die dieses Gerät zugreift.</span><span class="sxs-lookup"><span data-stu-id="9f400-402">Minimum block size, in bytes, for media accessed by this device.</span></span>

<span data-ttu-id="9f400-403">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9f400-403">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="9f400-404">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="9f400-404">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="9f400-405">**Name**</span><span class="sxs-lookup"><span data-stu-id="9f400-405">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f400-406">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9f400-406">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f400-407">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f400-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f400-408">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="9f400-408">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="9f400-409">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="9f400-409">Label by which the object is known.</span></span> <span data-ttu-id="9f400-410">Bei einer Unterklasse kann die Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="9f400-410">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="9f400-411">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9f400-411">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f400-412">**Unnötig**</span><span class="sxs-lookup"><span data-stu-id="9f400-412">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f400-413">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="9f400-413">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9f400-414">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f400-414">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f400-415">**True** gibt an, dass das Medien Zugriffsgerät bereinigt werden muss.</span><span class="sxs-lookup"><span data-stu-id="9f400-415">If **True**, the media access device requires cleaning.</span></span> <span data-ttu-id="9f400-416">Ob manuelle oder automatische Bereinigung möglich ist, wird in der Eigenschaft **Funktionen** angegeben.</span><span class="sxs-lookup"><span data-stu-id="9f400-416">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** property.</span></span>

<span data-ttu-id="9f400-417">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9f400-417">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f400-418">**"Numofmediasupportiert"**</span><span class="sxs-lookup"><span data-stu-id="9f400-418">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f400-419">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9f400-419">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f400-420">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f400-420">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f400-421">Maximale Anzahl einzelner Medien, die auf dem Medien Zugriffsgerät unterstützt oder eingefügt werden können (sofern unterstützt).</span><span class="sxs-lookup"><span data-stu-id="9f400-421">Maximum number of individual media which can be supported or inserted in the media access device (when supported).</span></span>

<span data-ttu-id="9f400-422">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9f400-422">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f400-423">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="9f400-423">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f400-424">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9f400-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f400-425">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f400-425">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f400-426">Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="9f400-426">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="9f400-427">Windows Plug & Play Geräte Bezeichner des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="9f400-427">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="9f400-428">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9f400-428">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="9f400-429">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="9f400-429">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="9f400-430">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="9f400-430">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f400-431">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="9f400-431">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9f400-432">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f400-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f400-433">Array der spezifischen energiebezogenen Funktionen eines logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="9f400-433">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="9f400-434">Diese Eigenschaft wird von **CIM \_ LogicalDevice** geerbt.</span><span class="sxs-lookup"><span data-stu-id="9f400-434">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9f400-435"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="9f400-435"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="9f400-436"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="9f400-436"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="9f400-437"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="9f400-437"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="9f400-438"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="9f400-438"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="9f400-439">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="9f400-439">Enabled</span></span>

<span data-ttu-id="9f400-440">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9f400-440">The power management features are currently enabled, but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="9f400-441"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="9f400-441"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="9f400-442">Automatisch eingegebene Energiespar Modi</span><span class="sxs-lookup"><span data-stu-id="9f400-442">Power Saving Modes Entered Automatically</span></span>

<span data-ttu-id="9f400-443">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="9f400-443">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="9f400-444"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="9f400-444"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="9f400-445">Energiezustand kann festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="9f400-445">Power State Settable</span></span>

<span data-ttu-id="9f400-446">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9f400-446">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="9f400-447">Diese Methode wird in der übergeordneten **CIM \_ LogicalDevice** -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="9f400-447">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="9f400-448">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="9f400-448">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="9f400-449"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="9f400-449"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="9f400-450">Unterstützung von Power Cycling</span><span class="sxs-lookup"><span data-stu-id="9f400-450">Power Cycling Supported</span></span>

<span data-ttu-id="9f400-451">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="9f400-451">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="9f400-452"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="9f400-452"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="9f400-453">Zeitgesteuerte Power-On unterstützt</span><span class="sxs-lookup"><span data-stu-id="9f400-453">Timed Power-On Supported</span></span>

<span data-ttu-id="9f400-454">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) und die *Uhrzeit* auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="9f400-454">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9f400-455">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="9f400-455">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f400-456">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="9f400-456">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9f400-457">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f400-457">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f400-458">Wenn der Wert **true** ist, kann das Gerät Energie gesteuert werden (kann in den Unterbrechungs Modus versetzt werden usw.).</span><span class="sxs-lookup"><span data-stu-id="9f400-458">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="9f400-459">Die-Eigenschaft gibt nicht an, dass die Energie Verwaltungsfunktionen zurzeit aktiviert sind, sondern nur, dass das logische Gerät für die Energie Verwaltung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="9f400-459">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="9f400-460">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9f400-460">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f400-461">**Status**</span><span class="sxs-lookup"><span data-stu-id="9f400-461">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f400-462">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9f400-462">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f400-463">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f400-463">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f400-464">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="9f400-464">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="9f400-465">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="9f400-465">Current status of the object.</span></span> <span data-ttu-id="9f400-466">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="9f400-466">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="9f400-467">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein intelligent-fähiges Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber Vorhersagen eines Fehlers in naher Zukunft).</span><span class="sxs-lookup"><span data-stu-id="9f400-467">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly, but predicting a failure in the near future).</span></span> <span data-ttu-id="9f400-468">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="9f400-468">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="9f400-469">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="9f400-469">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="9f400-470">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="9f400-470">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="9f400-471">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9f400-471">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="9f400-472">Die Werte sind:</span><span class="sxs-lookup"><span data-stu-id="9f400-472">The values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="9f400-473">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="9f400-473">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="9f400-474">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="9f400-474">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="9f400-475">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="9f400-475">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9f400-476">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="9f400-476">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="9f400-477">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="9f400-477">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="9f400-478">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="9f400-478">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="9f400-479">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="9f400-479">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="9f400-480">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="9f400-480">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="9f400-481">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="9f400-481">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="9f400-482">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="9f400-482">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="9f400-483">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="9f400-483">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="9f400-484">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="9f400-484">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9f400-485">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="9f400-485">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f400-486">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9f400-486">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9f400-487">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f400-487">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f400-488">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="9f400-488">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="9f400-489">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="9f400-489">State of the logical device.</span></span> <span data-ttu-id="9f400-490">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 ("nicht zutreffend") verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9f400-490">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="9f400-491">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9f400-491">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9f400-492">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="9f400-492">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9f400-493">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="9f400-493">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="9f400-494">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="9f400-494">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="9f400-495">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="9f400-495">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="9f400-496">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="9f400-496">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9f400-497">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="9f400-497">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f400-498">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9f400-498">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f400-499">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f400-499">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f400-500">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9f400-500">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9f400-501">Der Wert **der Eigenschaft "** Eigenschaft des Bereichs Computers".</span><span class="sxs-lookup"><span data-stu-id="9f400-501">Value of the scoping computer **CreationClassName** property.</span></span> <span data-ttu-id="9f400-502">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9f400-502">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="9f400-503">Diese Eigenschaft wird von [ **CIM \_ LogicalDevice** geerbt.](cim-logicaldevice.md)</span><span class="sxs-lookup"><span data-stu-id="9f400-503">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md)</span></span>

</dd> <dt>

<span data-ttu-id="9f400-504">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="9f400-504">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f400-505">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9f400-505">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f400-506">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9f400-506">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f400-507">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9f400-507">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9f400-508">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="9f400-508">Name of the scoping system.</span></span>

<span data-ttu-id="9f400-509">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9f400-509">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9f400-510">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9f400-510">Remarks</span></span>

<span data-ttu-id="9f400-511">Die **Win32 \_ floppydrive** -Klasse wird von [**CIM \_ diskettedrive**](cim-diskettedrive.md) abgeleitet, das von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="9f400-511">The **Win32\_FloppyDrive** class is derived from [**CIM\_DisketteDrive**](cim-diskettedrive.md) which derives from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span> <span data-ttu-id="9f400-512">Die **CIM \_ mediaaccessdevice** -Klasse wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="9f400-512">The **CIM\_MediaAccessDevice** class derives from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9f400-513">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9f400-513">Requirements</span></span>



| <span data-ttu-id="9f400-514">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9f400-514">Requirement</span></span> | <span data-ttu-id="9f400-515">Wert</span><span class="sxs-lookup"><span data-stu-id="9f400-515">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f400-516">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9f400-516">Minimum supported client</span></span><br/> | <span data-ttu-id="9f400-517">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9f400-517">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9f400-518">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9f400-518">Minimum supported server</span></span><br/> | <span data-ttu-id="9f400-519">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9f400-519">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9f400-520">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="9f400-520">End of client support</span></span><br/>    | <span data-ttu-id="9f400-521">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="9f400-521">Windows 8.1</span></span><br/>                                                                  |
| <span data-ttu-id="9f400-522">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="9f400-522">End of server support</span></span><br/>    | <span data-ttu-id="9f400-523">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="9f400-523">Windows Server 2012 R2</span></span><br/>                                                       |
| <span data-ttu-id="9f400-524">Namespace</span><span class="sxs-lookup"><span data-stu-id="9f400-524">Namespace</span></span><br/>                | <span data-ttu-id="9f400-525">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="9f400-525">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9f400-526">MOF</span><span class="sxs-lookup"><span data-stu-id="9f400-526">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9f400-527"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9f400-527"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9f400-528">DLL</span><span class="sxs-lookup"><span data-stu-id="9f400-528">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f400-529"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f400-529"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f400-530">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f400-530">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f400-531">**CIM- \_ Diskettelaufwerk**</span><span class="sxs-lookup"><span data-stu-id="9f400-531">**CIM\_DisketteDrive**</span></span>](cim-diskettedrive.md)
</dt> <dt>

[<span data-ttu-id="9f400-532">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="9f400-532">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

