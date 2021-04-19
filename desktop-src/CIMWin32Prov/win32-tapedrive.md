---
description: Die Win32 \_ TapeDrive WMI-Klasse stellt ein Bandlaufwerk auf einem Computersystem dar, auf dem Windows ausgeführt wird. Bandlaufwerke unterscheiden sich in erster Linie durch die Tatsache, dass nur sequenziell auf Sie zugegriffen werden kann.
ms.assetid: ceefec7b-a904-4b2f-a6b6-b84917a33023
ms.tgt_platform: multiple
title: Win32_TapeDrive-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_TapeDrive
- Win32_TapeDrive.Reset
- Win32_TapeDrive.SetPowerState
- Win32_TapeDrive.Availability
- Win32_TapeDrive.Capabilities
- Win32_TapeDrive.CapabilityDescriptions
- Win32_TapeDrive.Caption
- Win32_TapeDrive.Compression
- Win32_TapeDrive.CompressionMethod
- Win32_TapeDrive.ConfigManagerErrorCode
- Win32_TapeDrive.ConfigManagerUserConfig
- Win32_TapeDrive.CreationClassName
- Win32_TapeDrive.DefaultBlockSize
- Win32_TapeDrive.Description
- Win32_TapeDrive.DeviceID
- Win32_TapeDrive.ECC
- Win32_TapeDrive.EOTWarningZoneSize
- Win32_TapeDrive.ErrorCleared
- Win32_TapeDrive.ErrorDescription
- Win32_TapeDrive.ErrorMethodology
- Win32_TapeDrive.FeaturesHigh
- Win32_TapeDrive.FeaturesLow
- Win32_TapeDrive.Id
- Win32_TapeDrive.InstallDate
- Win32_TapeDrive.LastErrorCode
- Win32_TapeDrive.Manufacturer
- Win32_TapeDrive.MaxBlockSize
- Win32_TapeDrive.MaxMediaSize
- Win32_TapeDrive.MaxPartitionCount
- Win32_TapeDrive.MediaType
- Win32_TapeDrive.MinBlockSize
- Win32_TapeDrive.Name
- Win32_TapeDrive.NeedsCleaning
- Win32_TapeDrive.NumberOfMediaSupported
- Win32_TapeDrive.Padding
- Win32_TapeDrive.PNPDeviceID
- Win32_TapeDrive.PowerManagementCapabilities
- Win32_TapeDrive.PowerManagementSupported
- Win32_TapeDrive.ReportSetMarks
- Win32_TapeDrive.Status
- Win32_TapeDrive.StatusInfo
- Win32_TapeDrive.SystemCreationClassName
- Win32_TapeDrive.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6c7e7d3b754a0399acb152dba043da269f67a06f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342991"
---
# <a name="win32_tapedrive-class"></a><span data-ttu-id="c00cc-104">Win32- \_ Klasse "TapeDrive"</span><span class="sxs-lookup"><span data-stu-id="c00cc-104">Win32\_TapeDrive class</span></span>

<span data-ttu-id="c00cc-105">Die **Win32 \_ TapeDrive** [WMI-Klasse](../wmisdk/retrieving-a-class.md) stellt ein Bandlaufwerk auf einem Computersystem dar, auf dem Windows ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c00cc-105">The **Win32\_TapeDrive** [WMI class](../wmisdk/retrieving-a-class.md) represents a tape drive on a computer system running Windows.</span></span> <span data-ttu-id="c00cc-106">Bandlaufwerke unterscheiden sich in erster Linie durch die Tatsache, dass nur sequenziell auf Sie zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="c00cc-106">Tape drives are primarily distinguished by the fact that they can only be accessed sequentially.</span></span>

<span data-ttu-id="c00cc-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c00cc-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="c00cc-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="c00cc-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c00cc-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="c00cc-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4B1-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_TapeDrive : CIM_TapeDrive
{
  uint16   Availability;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   Caption;
  uint32   Compression;
  string   CompressionMethod;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint64   DefaultBlockSize;
  string   Description;
  string   DeviceID;
  uint32   ECC;
  uint32   EOTWarningZoneSize;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  uint32   FeaturesHigh;
  uint32   FeaturesLow;
  string   Id;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Manufacturer;
  uint64   MaxBlockSize;
  uint64   MaxMediaSize;
  uint32   MaxPartitionCount;
  string   MediaType;
  uint64   MinBlockSize;
  string   Name;
  boolean  NeedsCleaning;
  uint32   NumberOfMediaSupported;
  uint32   Padding;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint32   ReportSetMarks;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="c00cc-110">Member</span><span class="sxs-lookup"><span data-stu-id="c00cc-110">Members</span></span>

<span data-ttu-id="c00cc-111">Die **Win32 \_ TapeDrive** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c00cc-111">The **Win32\_TapeDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="c00cc-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="c00cc-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="c00cc-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c00cc-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c00cc-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="c00cc-114">Methods</span></span>

<span data-ttu-id="c00cc-115">Die **Win32 \_ TapeDrive** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="c00cc-115">The **Win32\_TapeDrive** class has these methods.</span></span>



| <span data-ttu-id="c00cc-116">Methode</span><span class="sxs-lookup"><span data-stu-id="c00cc-116">Method</span></span>            | <span data-ttu-id="c00cc-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c00cc-117">Description</span></span>                                                                                                                                                                            |
|:------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c00cc-118">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="c00cc-118">**Reset**</span></span>         | <span data-ttu-id="c00cc-119">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="c00cc-119">Not implemented.</span></span> <span data-ttu-id="c00cc-120">Informationen zur Implementierung dieser Methode finden Sie unter der [**Reset**](reset-method-in-class-cim-controller.md) -Methode in [**CIM \_ TapeDrive**](cim-tapedrive.md).</span><span class="sxs-lookup"><span data-stu-id="c00cc-120">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_TapeDrive**](cim-tapedrive.md).</span></span><br/>                 |
| <span data-ttu-id="c00cc-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="c00cc-121">**SetPowerState**</span></span> | <span data-ttu-id="c00cc-122">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="c00cc-122">Not implemented.</span></span> <span data-ttu-id="c00cc-123">Informationen zur Implementierung dieser Methode finden Sie unter der [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode in [**CIM \_ TapeDrive**](cim-tapedrive.md).</span><span class="sxs-lookup"><span data-stu-id="c00cc-123">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_TapeDrive**](cim-tapedrive.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c00cc-124">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c00cc-124">Properties</span></span>

<span data-ttu-id="c00cc-125">Die **Win32 \_ TapeDrive** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c00cc-125">The **Win32\_TapeDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c00cc-126">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="c00cc-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c00cc-127">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c00cc-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c00cc-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-129">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="c00cc-129">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="c00cc-130">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="c00cc-130">Availability and status of the device.</span></span>

<span data-ttu-id="c00cc-131">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c00cc-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c00cc-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="c00cc-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c00cc-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="c00cc-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="c00cc-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="c00cc-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c00cc-135">Ausführung oder vollständiger Stromversorgung</span><span class="sxs-lookup"><span data-stu-id="c00cc-135">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="c00cc-136"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="c00cc-136"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="c00cc-137"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="c00cc-137"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="c00cc-138"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="c00cc-138"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="c00cc-139"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="c00cc-139"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="c00cc-140"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="c00cc-140"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="c00cc-141"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="c00cc-141"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c00cc-142"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="c00cc-142"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="c00cc-143"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="c00cc-143"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="c00cc-144"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="c00cc-144"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="c00cc-145"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="c00cc-145"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="c00cc-146">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="c00cc-146">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="c00cc-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="c00cc-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="c00cc-148">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="c00cc-148">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="c00cc-149"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="c00cc-149"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="c00cc-150">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb gebracht werden.</span><span class="sxs-lookup"><span data-stu-id="c00cc-150">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="c00cc-151"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="c00cc-151"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="c00cc-152"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="c00cc-152"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="c00cc-153">Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="c00cc-153">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="c00cc-154"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="c00cc-154"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="c00cc-155">Das Gerät wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="c00cc-155">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="c00cc-156"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="c00cc-156"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="c00cc-157">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="c00cc-157">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="c00cc-158"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="c00cc-158"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="c00cc-159">Das Gerät ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="c00cc-159">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="c00cc-160"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="c00cc-160"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="c00cc-161">Das Gerät ist in Ruhe.</span><span class="sxs-lookup"><span data-stu-id="c00cc-161">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c00cc-162">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="c00cc-162">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c00cc-163">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="c00cc-163">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-164">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c00cc-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-165">Qualifizierer: [**arrayType**](../wmisdk/standard-qualifiers.md) ("indiziert"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| Speichergeräte \| 001,9 "," MIF. DMTF- \| Speichergeräte \| 001,11 "," MIF. DMTF- \| Speichergeräte \| 001,12 "," MIF. DMTF-Datenträger \| \| 003,7 "), [**modelkorrespondenz**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md).**Capabilitybeschreibungen**")</span><span class="sxs-lookup"><span data-stu-id="c00cc-165">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="c00cc-166">Array von Funktionen des Medien Zugriffs Geräts.</span><span class="sxs-lookup"><span data-stu-id="c00cc-166">Array of capabilities of the media access device.</span></span> <span data-ttu-id="c00cc-167">Beispielsweise kann das Gerät zufälligen Zugriff, Wechsel Datenträger und Automatisches Bereinigen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="c00cc-167">For example, the device may support Random Access, removable media and Automatic Cleaning.</span></span> <span data-ttu-id="c00cc-168">In diesem Fall werden die Werte 3, 7 und 9 in das Array geschrieben.</span><span class="sxs-lookup"><span data-stu-id="c00cc-168">In this case, the values 3, 7, and 9 would be written to the array.</span></span>

<span data-ttu-id="c00cc-169">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c00cc-169">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c00cc-170"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="c00cc-170"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c00cc-171"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="c00cc-171"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="c00cc-172"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequenzieller Zugriff** (2)</span><span class="sxs-lookup"><span data-stu-id="c00cc-172"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="c00cc-173"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Zufälliger Zugriff** (3)</span><span class="sxs-lookup"><span data-stu-id="c00cc-173"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="c00cc-174"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Unterstützt Schreib** Vorgänge (4)</span><span class="sxs-lookup"><span data-stu-id="c00cc-174"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="c00cc-175"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Verschlüsselung** (5)</span><span class="sxs-lookup"><span data-stu-id="c00cc-175"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="c00cc-176"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Komprimierung** (6)</span><span class="sxs-lookup"><span data-stu-id="c00cc-176"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="c00cc-177"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Unterstützt Removeable Media** (7)</span><span class="sxs-lookup"><span data-stu-id="c00cc-177"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="c00cc-178">Unterstützt Wechselmedien</span><span class="sxs-lookup"><span data-stu-id="c00cc-178">Supports Removable Media</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="c00cc-179"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manuelle Reinigung** (8)</span><span class="sxs-lookup"><span data-stu-id="c00cc-179"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="c00cc-180"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatische Bereinigung** (9)</span><span class="sxs-lookup"><span data-stu-id="c00cc-180"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="c00cc-181"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**Smart Notification** (10)</span><span class="sxs-lookup"><span data-stu-id="c00cc-181"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="c00cc-182"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Unterstützt zweiseitige Medien** (11)</span><span class="sxs-lookup"><span data-stu-id="c00cc-182"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="c00cc-183">Unterstützt Dual-Sided Medien</span><span class="sxs-lookup"><span data-stu-id="c00cc-183">Supports Dual-Sided Media</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="c00cc-184"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount-eject nicht erforderlich** (12)</span><span class="sxs-lookup"><span data-stu-id="c00cc-184"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c00cc-185">**Capabilitybeschreibungen**</span><span class="sxs-lookup"><span data-stu-id="c00cc-185">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c00cc-186">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="c00cc-186">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-187">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c00cc-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-188">Qualifizierer: [**arrayType**](../wmisdk/standard-qualifiers.md) ("indiziert"), [**modelkorrespondenz**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md).**Funktionen**")</span><span class="sxs-lookup"><span data-stu-id="c00cc-188">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="c00cc-189">Ein Array von frei Form Zeichenfolgen, das Ausführlichere Erläuterungen für alle Zugriffsgeräte Funktionen bereitstellt, die im **Funktions Array angegeben** sind.</span><span class="sxs-lookup"><span data-stu-id="c00cc-189">Array of free-form strings providing more detailed explanations for any of the access device features indicated in the **Capabilities** array.</span></span> <span data-ttu-id="c00cc-190">Beachten Sie, dass jeder Eintrag dieses Arrays mit dem Eintrag im **Funktions Array verknüpft ist, der sich** am selben Index befindet.</span><span class="sxs-lookup"><span data-stu-id="c00cc-190">Note that each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

<span data-ttu-id="c00cc-191">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c00cc-191">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c00cc-192">**Caption**</span><span class="sxs-lookup"><span data-stu-id="c00cc-192">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c00cc-193">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c00cc-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-194">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c00cc-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-195">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="c00cc-195">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="c00cc-196">Kurze Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="c00cc-196">Short description of the object.</span></span>

<span data-ttu-id="c00cc-197">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c00cc-197">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c00cc-198">**Komprimierung**</span><span class="sxs-lookup"><span data-stu-id="c00cc-198">**Compression**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c00cc-199">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c00cc-199">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-200">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c00cc-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-201">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Tape Backup Structures \| [**Tape \_ get \_ Drive \_ Parameters**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters) \| Compression")</span><span class="sxs-lookup"><span data-stu-id="c00cc-201">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tape Backup Structures\|[**TAPE\_GET\_DRIVE\_PARAMETERS**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters)\|Compression")</span></span>
</dt> </dl>

<span data-ttu-id="c00cc-202">**True** gibt an, dass die Hardware Datenkomprimierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="c00cc-202">If **TRUE**, hardware data compression is enabled.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="c00cc-203"><span id="0"></span>**1,0**</span><span class="sxs-lookup"><span data-stu-id="c00cc-203"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="c00cc-204">false</span><span class="sxs-lookup"><span data-stu-id="c00cc-204">FALSE</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="c00cc-205"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="c00cc-205"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="c00cc-206">TRUE</span><span class="sxs-lookup"><span data-stu-id="c00cc-206">TRUE</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c00cc-207">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="c00cc-207">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c00cc-208">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c00cc-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-209">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c00cc-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c00cc-210">Frei Form Zeichenfolge, die den Algorithmus oder das Tool angibt, das vom Gerät zur Unterstützung der Komprimierung verwendet</span><span class="sxs-lookup"><span data-stu-id="c00cc-210">Free-form string indicating the algorithm or tool used by the device to support compression.</span></span> <span data-ttu-id="c00cc-211">Wenn es nicht möglich oder nicht erwünscht ist, das Komprimierungs Schema zu beschreiben (weil es möglicherweise nicht bekannt ist), verwenden Sie die folgenden Wörter: "unknown", um darzustellen, dass das Gerät Komprimierungs Funktionen unterstützt oder nicht. "Komprimiert", um darzustellen, dass das Gerät Komprimierungs Funktionen unterstützt, aber entweder das zugehörige Komprimierungs Schema nicht bekannt oder nicht offengelegt ist. und "nicht komprimiert", um darzustellen, dass das Gerät keine Komprimierungs Funktionen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c00cc-211">If it is not possible or not desired to describe the compression scheme (perhaps because it is not known), use the following words: "Unknown" to represent that it is not known whether the device supports compression capabilities or not; "Compressed" to represent that the device supports compression capabilities but either its compression scheme is not known or not disclosed; and "Not Compressed" to represent that the device does not support compression capabilities.</span></span>

<span data-ttu-id="c00cc-212">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c00cc-212">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>



 <span data-ttu-id="c00cc-213">("Unbekannt")</span><span class="sxs-lookup"><span data-stu-id="c00cc-213">("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="c00cc-214">Das Komprimierungs Schema ist unbekannt oder nicht beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c00cc-214">The compression scheme is unknown or not described.</span></span>

</dd> <dt>



 <span data-ttu-id="c00cc-215">("Komprimiert")</span><span class="sxs-lookup"><span data-stu-id="c00cc-215">("Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="c00cc-216">Die logische Datei ist komprimiert, das Komprimierungs Schema ist jedoch unbekannt oder nicht beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c00cc-216">The logical file is compressed, but the compression scheme is unknown or not described</span></span>

</dd> <dt>



 <span data-ttu-id="c00cc-217">("Nicht komprimiert")</span><span class="sxs-lookup"><span data-stu-id="c00cc-217">("Not Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="c00cc-218">Wenn die logische Datei nicht komprimiert ist</span><span class="sxs-lookup"><span data-stu-id="c00cc-218">If the logical file is not compressed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c00cc-219">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="c00cc-219">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c00cc-220">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c00cc-220">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-221">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c00cc-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-222">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="c00cc-222">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c00cc-223">Win32-Configuration Manager Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="c00cc-223">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="c00cc-224">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c00cc-224">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="c00cc-225"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="c00cc-225"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="c00cc-226"> (0)</span><span class="sxs-lookup"><span data-stu-id="c00cc-226">(0)</span></span>


</dt> <dd>

<span data-ttu-id="c00cc-227">Das Gerät funktioniert ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="c00cc-227">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="c00cc-228"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="c00cc-228"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="c00cc-229">(1)</span><span class="sxs-lookup"><span data-stu-id="c00cc-229">(1)</span></span>


</dt> <dd>

<span data-ttu-id="c00cc-230">Das Gerät ist nicht ordnungsgemäß konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="c00cc-230">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c00cc-231"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="c00cc-231"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="c00cc-232">(2)</span><span class="sxs-lookup"><span data-stu-id="c00cc-232">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="c00cc-233"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="c00cc-233"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="c00cc-234">(3)</span><span class="sxs-lookup"><span data-stu-id="c00cc-234">(3)</span></span>


</dt> <dd>

<span data-ttu-id="c00cc-235">Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt möglicherweise nicht über genügend Arbeitsspeicher oder andere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="c00cc-235">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="c00cc-236"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="c00cc-236"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="c00cc-237">(4)</span><span class="sxs-lookup"><span data-stu-id="c00cc-237">(4)</span></span>


</dt> <dd>

<span data-ttu-id="c00cc-238">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="c00cc-238">Device is not working properly.</span></span> <span data-ttu-id="c00cc-239">Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="c00cc-239">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="c00cc-240"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="c00cc-240"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="c00cc-241">(5)</span><span class="sxs-lookup"><span data-stu-id="c00cc-241">(5)</span></span>


</dt> <dd>

<span data-ttu-id="c00cc-242">Der Treiber für das Gerät erfordert eine Ressource, die von Windows nicht verwaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c00cc-242">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="c00cc-243"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="c00cc-243"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="c00cc-244"> (6)</span><span class="sxs-lookup"><span data-stu-id="c00cc-244">(6)</span></span>


</dt> <dd>

<span data-ttu-id="c00cc-245">Die Startkonfiguration für das Gerät steht in Konflikt mit anderen Geräten.</span><span class="sxs-lookup"><span data-stu-id="c00cc-245">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="c00cc-246"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="c00cc-246"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="c00cc-247">(7)</span><span class="sxs-lookup"><span data-stu-id="c00cc-247">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="c00cc-248"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="c00cc-248"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="c00cc-249">(8)</span><span class="sxs-lookup"><span data-stu-id="c00cc-249">(8)</span></span>


</dt> <dd>

<span data-ttu-id="c00cc-250">Das Treiber Lade Modul für das Gerät fehlt.</span><span class="sxs-lookup"><span data-stu-id="c00cc-250">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="c00cc-251"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="c00cc-251"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="c00cc-252">(9)</span><span class="sxs-lookup"><span data-stu-id="c00cc-252">(9)</span></span>


</dt> <dd>

<span data-ttu-id="c00cc-253">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="c00cc-253">Device is not working properly.</span></span> <span data-ttu-id="c00cc-254">Die Steuerungs Firmware meldet nicht korrekt die Ressourcen für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="c00cc-254">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="c00cc-255"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="c00cc-255"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="c00cc-256">(10)</span><span class="sxs-lookup"><span data-stu-id="c00cc-256">(10)</span></span>


</dt> <dd>

<span data-ttu-id="c00cc-257">Das Gerät kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="c00cc-257">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="c00cc-258"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="c00cc-258"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="c00cc-259">(11)</span><span class="sxs-lookup"><span data-stu-id="c00cc-259">(11)</span></span>


</dt> <dd>

<span data-ttu-id="c00cc-260">Fehler beim Gerät.</span><span class="sxs-lookup"><span data-stu-id="c00cc-260">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="c00cc-261"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="c00cc-261"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="c00cc-262">(12)</span><span class="sxs-lookup"><span data-stu-id="c00cc-262">(12)</span></span>


</dt> <dd>

<span data-ttu-id="c00cc-263">Das Gerät kann nicht genug freie Ressourcen für die Verwendung finden.</span><span class="sxs-lookup"><span data-stu-id="c00cc-263">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="c00cc-264"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="c00cc-264"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="c00cc-265">(13)</span><span class="sxs-lookup"><span data-stu-id="c00cc-265">(13)</span></span>


</dt> <dd>

<span data-ttu-id="c00cc-266">Die Geräte Ressourcen können nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="c00cc-266">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="c00cc-267"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="c00cc-267"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="c00cc-268">(14)</span><span class="sxs-lookup"><span data-stu-id="c00cc-268">(14)</span></span>


</dt> <dd>

<span data-ttu-id="c00cc-269">Das Gerät kann erst ordnungsgemäß funktionieren, wenn der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="c00cc-269">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="c00cc-270"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="c00cc-270"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="c00cc-271">(15)</span><span class="sxs-lookup"><span data-stu-id="c00cc-271">(15)</span></span>


</dt> <dd>

<span data-ttu-id="c00cc-272">Das Gerät funktioniert aufgrund eines möglichen erneuten Aufzählungs Problems nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="c00cc-272">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="c00cc-273"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="c00cc-273"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="c00cc-274">(16)</span><span class="sxs-lookup"><span data-stu-id="c00cc-274">(16)</span></span>


</dt> <dd>

<span data-ttu-id="c00cc-275">In Windows können nicht alle Ressourcen identifiziert werden, die vom Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c00cc-275">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="c00cc-276"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="c00cc-276"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="c00cc-277">(17)</span><span class="sxs-lookup"><span data-stu-id="c00cc-277">(17)</span></span>


</dt> <dd>

<span data-ttu-id="c00cc-278">Das Gerät fordert einen unbekannten Ressourcentyp an.</span><span class="sxs-lookup"><span data-stu-id="c00cc-278">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c00cc-279"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="c00cc-279"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="c00cc-280">(18)</span><span class="sxs-lookup"><span data-stu-id="c00cc-280">(18)</span></span>


</dt> <dd>

<span data-ttu-id="c00cc-281">Gerätetreiber müssen neu installiert werden.</span><span class="sxs-lookup"><span data-stu-id="c00cc-281">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="c00cc-282"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="c00cc-282"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="c00cc-283">(19)</span><span class="sxs-lookup"><span data-stu-id="c00cc-283">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="c00cc-284"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="c00cc-284"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="c00cc-285">(20)</span><span class="sxs-lookup"><span data-stu-id="c00cc-285">(20)</span></span>


</dt> <dd>

<span data-ttu-id="c00cc-286">Die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="c00cc-286">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="c00cc-287"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="c00cc-287"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="c00cc-288">(21)</span><span class="sxs-lookup"><span data-stu-id="c00cc-288">(21)</span></span>


</dt> <dd>

<span data-ttu-id="c00cc-289">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="c00cc-289">System failure.</span></span> <span data-ttu-id="c00cc-290">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="c00cc-290">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="c00cc-291">Das Gerät wird von Windows entfernt.</span><span class="sxs-lookup"><span data-stu-id="c00cc-291">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="c00cc-292"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="c00cc-292"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="c00cc-293">(22)</span><span class="sxs-lookup"><span data-stu-id="c00cc-293">(22)</span></span>


</dt> <dd>

<span data-ttu-id="c00cc-294">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="c00cc-294">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="c00cc-295"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="c00cc-295"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="c00cc-296">(23)</span><span class="sxs-lookup"><span data-stu-id="c00cc-296">(23)</span></span>


</dt> <dd>

<span data-ttu-id="c00cc-297">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="c00cc-297">System failure.</span></span> <span data-ttu-id="c00cc-298">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="c00cc-298">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="c00cc-299"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="c00cc-299"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="c00cc-300">(24)</span><span class="sxs-lookup"><span data-stu-id="c00cc-300">(24)</span></span>


</dt> <dd>

<span data-ttu-id="c00cc-301">Das Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.</span><span class="sxs-lookup"><span data-stu-id="c00cc-301">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="c00cc-302"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="c00cc-302"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="c00cc-303">(25)</span><span class="sxs-lookup"><span data-stu-id="c00cc-303">(25)</span></span>


</dt> <dd>

<span data-ttu-id="c00cc-304">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="c00cc-304">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="c00cc-305"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="c00cc-305"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="c00cc-306">(26)</span><span class="sxs-lookup"><span data-stu-id="c00cc-306">(26)</span></span>


</dt> <dd>

<span data-ttu-id="c00cc-307">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="c00cc-307">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="c00cc-308"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="c00cc-308"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="c00cc-309">(27)</span><span class="sxs-lookup"><span data-stu-id="c00cc-309">(27)</span></span>


</dt> <dd>

<span data-ttu-id="c00cc-310">Das Gerät verfügt nicht über eine gültige Protokoll Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="c00cc-310">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="c00cc-311"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="c00cc-311"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="c00cc-312">(28)</span><span class="sxs-lookup"><span data-stu-id="c00cc-312">(28)</span></span>


</dt> <dd>

<span data-ttu-id="c00cc-313">Gerätetreiber sind nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="c00cc-313">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="c00cc-314"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="c00cc-314"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="c00cc-315">(29)</span><span class="sxs-lookup"><span data-stu-id="c00cc-315">(29)</span></span>


</dt> <dd>

<span data-ttu-id="c00cc-316">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="c00cc-316">Device is disabled.</span></span> <span data-ttu-id="c00cc-317">Die Gerätefirmware hat nicht die erforderlichen Ressourcen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="c00cc-317">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="c00cc-318"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="c00cc-318"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="c00cc-319">(30)</span><span class="sxs-lookup"><span data-stu-id="c00cc-319">(30)</span></span>


</dt> <dd>

<span data-ttu-id="c00cc-320">Das Gerät verwendet eine UNQ-Ressource, die von einem anderen Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c00cc-320">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c00cc-321"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="c00cc-321"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="c00cc-322">31,5</span><span class="sxs-lookup"><span data-stu-id="c00cc-322">(31)</span></span>


</dt> <dd>

<span data-ttu-id="c00cc-323">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="c00cc-323">Device is not working properly.</span></span> <span data-ttu-id="c00cc-324">Die erforderlichen Gerätetreiber können nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="c00cc-324">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c00cc-325">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="c00cc-325">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c00cc-326">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="c00cc-326">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-327">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c00cc-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-328">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="c00cc-328">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c00cc-329">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="c00cc-329">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="c00cc-330">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c00cc-330">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c00cc-331">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="c00cc-331">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c00cc-332">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c00cc-332">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-333">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c00cc-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-334">Qualifizierer: [ **CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="c00cc-334">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="c00cc-335">Der Name der ersten konkreten Klasse, die in der Vererbungs Kette angezeigt werden soll, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c00cc-335">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="c00cc-336">Wenn diese Eigenschaft mit den anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="c00cc-336">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="c00cc-337">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c00cc-337">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c00cc-338">**Defaultblocksize**</span><span class="sxs-lookup"><span data-stu-id="c00cc-338">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c00cc-339">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c00cc-339">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-340">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c00cc-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-341">Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="c00cc-341">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="c00cc-342">Standard Blockgröße (in Bytes) für dieses Gerät.</span><span class="sxs-lookup"><span data-stu-id="c00cc-342">Default block size, in bytes, for this device.</span></span>

<span data-ttu-id="c00cc-343">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c00cc-343">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="c00cc-344">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="c00cc-344">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="c00cc-345">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c00cc-345">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c00cc-346">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c00cc-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-347">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c00cc-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-348">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="c00cc-348">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="c00cc-349">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="c00cc-349">Description of the object.</span></span>

<span data-ttu-id="c00cc-350">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c00cc-350">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c00cc-351">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="c00cc-351">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c00cc-352">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c00cc-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-353">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c00cc-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-354">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("DeviceID"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| File Functions | \| atefile")</span><span class="sxs-lookup"><span data-stu-id="c00cc-354">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|File Functions\|CreateFile")</span></span>
</dt> </dl>

<span data-ttu-id="c00cc-355">Eindeutiger Bezeichner des Band Laufwerks mit anderen Geräten im System.</span><span class="sxs-lookup"><span data-stu-id="c00cc-355">Unique identifier of the tape drive with other devices on the system.</span></span>

<span data-ttu-id="c00cc-356">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c00cc-356">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c00cc-357">**ECC**</span><span class="sxs-lookup"><span data-stu-id="c00cc-357">**ECC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c00cc-358">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c00cc-358">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-359">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c00cc-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-360">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Tape Backup Structures \| [**Tape \_ get \_ Drive \_ Parameters**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters) \| ECC")</span><span class="sxs-lookup"><span data-stu-id="c00cc-360">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tape Backup Structures\|[**TAPE\_GET\_DRIVE\_PARAMETERS**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters)\|ECC")</span></span>
</dt> </dl>

<span data-ttu-id="c00cc-361">**True** gibt an, dass das Gerät die Hardwarefehler Korrektur unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c00cc-361">If **TRUE**, the device supports hardware error correction.</span></span>

<dt>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>

<span data-ttu-id="c00cc-362">**False** (0)</span><span class="sxs-lookup"><span data-stu-id="c00cc-362">**False** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>

<span data-ttu-id="c00cc-363">**True** (1)</span><span class="sxs-lookup"><span data-stu-id="c00cc-363">**True** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c00cc-364">**EOTWarningZoneSize**</span><span class="sxs-lookup"><span data-stu-id="c00cc-364">**EOTWarningZoneSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c00cc-365">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c00cc-365">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-366">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c00cc-366">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-367">Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="c00cc-367">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="c00cc-368">Die Zonen Größe für das Ende der Band Warnung (EOT).</span><span class="sxs-lookup"><span data-stu-id="c00cc-368">Zone size for the end of tape (EOT) warning.</span></span>

<span data-ttu-id="c00cc-369">Diese Eigenschaft wird von [**CIM \_ TapeDrive**](cim-tapedrive.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c00cc-369">This property is inherited from [**CIM\_TapeDrive**](cim-tapedrive.md).</span></span>

</dd> <dt>

<span data-ttu-id="c00cc-370">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="c00cc-370">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c00cc-371">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="c00cc-371">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-372">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c00cc-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c00cc-373">**True** gibt an, dass der in **LastErrorCode** gemeldete Fehler jetzt gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="c00cc-373">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="c00cc-374">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c00cc-374">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c00cc-375">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="c00cc-375">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c00cc-376">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c00cc-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-377">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c00cc-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c00cc-378">Eine frei Form Zeichenfolge, die weitere Informationen über den in **LastErrorCode** aufgezeichneten Fehler sowie Informationen zu eventuell durchzuführenden Korrekturmaßnahmen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="c00cc-378">Free-form string supplying more information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="c00cc-379">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c00cc-379">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c00cc-380">**Errormethodmethodologie**</span><span class="sxs-lookup"><span data-stu-id="c00cc-380">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c00cc-381">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c00cc-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-382">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c00cc-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c00cc-383">Frei Form Zeichenfolge, die den Typ der von diesem Gerät unterstützten Fehlererkennung und-Korrektur beschreibt.</span><span class="sxs-lookup"><span data-stu-id="c00cc-383">Free-form string describing the type of error detection and correction supported by this device.</span></span>

<span data-ttu-id="c00cc-384">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c00cc-384">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c00cc-385">**Featureshigh**</span><span class="sxs-lookup"><span data-stu-id="c00cc-385">**FeaturesHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c00cc-386">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c00cc-386">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-387">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c00cc-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-388">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Tape Backup Structures \| [**Tape \_ get \_ Drive \_ Parameters**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters) \| featureshigh")</span><span class="sxs-lookup"><span data-stu-id="c00cc-388">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tape Backup Structures\|[**TAPE\_GET\_DRIVE\_PARAMETERS**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters)\|FeaturesHigh")</span></span>
</dt> </dl>

<span data-ttu-id="c00cc-389">Hohe Reihenfolge 32 Bits des Device Features-Flags.</span><span class="sxs-lookup"><span data-stu-id="c00cc-389">High-order 32 bits of the device features flag.</span></span>

</dd> <dt>

<span data-ttu-id="c00cc-390">**Featurelangsam**</span><span class="sxs-lookup"><span data-stu-id="c00cc-390">**FeaturesLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c00cc-391">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c00cc-391">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-392">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c00cc-392">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-393">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Tape Backup Structures \| [**Tape \_ get \_ Drive \_ Parameters**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters) \| featureslow")</span><span class="sxs-lookup"><span data-stu-id="c00cc-393">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tape Backup Structures\|[**TAPE\_GET\_DRIVE\_PARAMETERS**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters)\|FeaturesLow")</span></span>
</dt> </dl>

<span data-ttu-id="c00cc-394">32 Bits der Geräte Features in niedriger Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="c00cc-394">Low-order 32 bits of the device features flag.</span></span>

</dd> <dt>

<span data-ttu-id="c00cc-395">**Id**</span><span class="sxs-lookup"><span data-stu-id="c00cc-395">**Id**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c00cc-396">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c00cc-396">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-397">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c00cc-397">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-398">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| File Functions")</span><span class="sxs-lookup"><span data-stu-id="c00cc-398">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|File Functions")</span></span>
</dt> </dl>

<span data-ttu-id="c00cc-399">Der Hersteller identifiziert den Namen des Windows CD ROM-Laufwerks.</span><span class="sxs-lookup"><span data-stu-id="c00cc-399">Manufacturer's identifying name of the Windows CD ROM drive.</span></span>

<span data-ttu-id="c00cc-400">Beispiel: "Plextor CD-ROM px-12CS 1,01"</span><span class="sxs-lookup"><span data-stu-id="c00cc-400">Example: "PLEXTOR CD-ROM PX-12CS 1.01"</span></span>

</dd> <dt>

<span data-ttu-id="c00cc-401">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c00cc-401">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c00cc-402">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="c00cc-402">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-403">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c00cc-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-404">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="c00cc-404">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="c00cc-405">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="c00cc-405">Date and time the object was installed.</span></span> <span data-ttu-id="c00cc-406">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="c00cc-406">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="c00cc-407">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c00cc-407">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c00cc-408">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="c00cc-408">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c00cc-409">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c00cc-409">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-410">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c00cc-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c00cc-411">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="c00cc-411">Last error code reported by the logical device.</span></span>

<span data-ttu-id="c00cc-412">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c00cc-412">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c00cc-413">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="c00cc-413">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c00cc-414">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c00cc-414">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-415">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c00cc-415">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-416">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry")</span><span class="sxs-lookup"><span data-stu-id="c00cc-416">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry")</span></span>
</dt> </dl>

<span data-ttu-id="c00cc-417">Hersteller des Windows-CD-ROM-Laufwerks.</span><span class="sxs-lookup"><span data-stu-id="c00cc-417">Manufacturer of the Windows CD-ROM drive.</span></span>

<span data-ttu-id="c00cc-418">Beispiel: "Plextor"</span><span class="sxs-lookup"><span data-stu-id="c00cc-418">Example: "PLEXTOR"</span></span>

</dd> <dt>

<span data-ttu-id="c00cc-419">**Maxblocksize**</span><span class="sxs-lookup"><span data-stu-id="c00cc-419">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c00cc-420">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c00cc-420">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-421">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c00cc-421">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-422">Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="c00cc-422">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="c00cc-423">Maximale Blockgröße (in Bytes) für Medien, auf die dieses Gerät zugreift.</span><span class="sxs-lookup"><span data-stu-id="c00cc-423">Maximum block size, in bytes, for media accessed by this device.</span></span>

<span data-ttu-id="c00cc-424">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c00cc-424">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="c00cc-425">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="c00cc-425">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="c00cc-426">**Maxmediasize**</span><span class="sxs-lookup"><span data-stu-id="c00cc-426">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c00cc-427">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c00cc-427">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-428">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c00cc-428">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-429">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| sequenzielle Zugriffsgeräte \| 001,2 "), [**Einheiten**](../wmisdk/standard-qualifiers.md) (" Kilobyte ")</span><span class="sxs-lookup"><span data-stu-id="c00cc-429">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="c00cc-430">Maximale Größe des von diesem Gerät unterstützten Mediums in Kilobyte.</span><span class="sxs-lookup"><span data-stu-id="c00cc-430">Maximum size, in kilobytes, of media supported by this device.</span></span>

<span data-ttu-id="c00cc-431">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c00cc-431">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="c00cc-432">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="c00cc-432">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="c00cc-433">**MaxPartitionCount**</span><span class="sxs-lookup"><span data-stu-id="c00cc-433">**MaxPartitionCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c00cc-434">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c00cc-434">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-435">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c00cc-435">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c00cc-436">Maximale Anzahl von Partitionen für das Bandlaufwerk.</span><span class="sxs-lookup"><span data-stu-id="c00cc-436">Maximum partition count for the tape drive.</span></span>

<span data-ttu-id="c00cc-437">Diese Eigenschaft wird von [**CIM \_ TapeDrive**](cim-tapedrive.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c00cc-437">This property is inherited from [**CIM\_TapeDrive**](cim-tapedrive.md).</span></span>

</dd> <dt>

<span data-ttu-id="c00cc-438">**MediaType**</span><span class="sxs-lookup"><span data-stu-id="c00cc-438">**MediaType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c00cc-439">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c00cc-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-440">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c00cc-440">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-441">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32 \_ TapeDrive \| mediaType \| Tape Drive")</span><span class="sxs-lookup"><span data-stu-id="c00cc-441">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_TapeDrive\|MediaType\|Tape Drive")</span></span>
</dt> </dl>

<span data-ttu-id="c00cc-442">Medientyp, der von diesem Gerät verwendet wird (oder auf das von zugegriffen wird).</span><span class="sxs-lookup"><span data-stu-id="c00cc-442">Media type used by (or accessed by) this device.</span></span> <span data-ttu-id="c00cc-443">In diesem Fall ist es auf "Bandlaufwerk" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c00cc-443">In this case, it is set to "Tape Drive".</span></span>

</dd> <dt>

<span data-ttu-id="c00cc-444">**Minblocksize**</span><span class="sxs-lookup"><span data-stu-id="c00cc-444">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c00cc-445">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c00cc-445">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-446">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c00cc-446">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-447">Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="c00cc-447">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="c00cc-448">Minimale Blockgröße (in Bytes) für Medien, auf die dieses Gerät zugreift.</span><span class="sxs-lookup"><span data-stu-id="c00cc-448">Minimum block size, in bytes, for media accessed by this device.</span></span>

<span data-ttu-id="c00cc-449">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c00cc-449">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="c00cc-450">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="c00cc-450">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="c00cc-451">**Name**</span><span class="sxs-lookup"><span data-stu-id="c00cc-451">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c00cc-452">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c00cc-452">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-453">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c00cc-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-454">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="c00cc-454">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="c00cc-455">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="c00cc-455">Label by which the object is known.</span></span> <span data-ttu-id="c00cc-456">Bei einer Unterklasse kann die Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="c00cc-456">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="c00cc-457">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c00cc-457">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c00cc-458">**Unnötig**</span><span class="sxs-lookup"><span data-stu-id="c00cc-458">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c00cc-459">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="c00cc-459">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-460">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c00cc-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c00cc-461">**True** gibt an, dass das Medien Zugriffsgerät bereinigt werden muss.</span><span class="sxs-lookup"><span data-stu-id="c00cc-461">If **TRUE**, the media access device needs cleaning.</span></span> <span data-ttu-id="c00cc-462">Ob manuelle oder automatische Bereinigung möglich ist, wird in der Eigenschaft **Funktionen** angegeben.</span><span class="sxs-lookup"><span data-stu-id="c00cc-462">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** property.</span></span>

<span data-ttu-id="c00cc-463">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c00cc-463">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c00cc-464">**"Numofmediasupportiert"**</span><span class="sxs-lookup"><span data-stu-id="c00cc-464">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c00cc-465">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c00cc-465">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-466">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c00cc-466">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c00cc-467">Maximale Anzahl einzelner Medien, die auf dem Medien Zugriffsgerät unterstützt oder eingefügt werden können (sofern unterstützt).</span><span class="sxs-lookup"><span data-stu-id="c00cc-467">Maximum number of individual media which can be supported or inserted in the media access device (when supported).</span></span>

<span data-ttu-id="c00cc-468">Diese Eigenschaft wird von [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c00cc-468">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c00cc-469">**Auffüllen**</span><span class="sxs-lookup"><span data-stu-id="c00cc-469">**Padding**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c00cc-470">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c00cc-470">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-471">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c00cc-471">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-472">Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="c00cc-472">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="c00cc-473">Anzahl von Bytes, die zwischen Blöcken auf einem Band Medium eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="c00cc-473">Number of bytes inserted between blocks on a tape media.</span></span>

<span data-ttu-id="c00cc-474">Diese Eigenschaft wird von [**CIM \_ TapeDrive**](cim-tapedrive.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c00cc-474">This property is inherited from [**CIM\_TapeDrive**](cim-tapedrive.md).</span></span>

</dd> <dt>

<span data-ttu-id="c00cc-475">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="c00cc-475">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c00cc-476">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c00cc-476">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-477">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c00cc-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-478">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="c00cc-478">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c00cc-479">Windows Plug & Play Geräte Bezeichner des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="c00cc-479">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="c00cc-480">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c00cc-480">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="c00cc-481">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="c00cc-481">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="c00cc-482">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="c00cc-482">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c00cc-483">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="c00cc-483">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-484">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c00cc-484">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c00cc-485">Array der spezifischen energiebezogenen Funktionen eines logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="c00cc-485">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="c00cc-486">Diese Eigenschaft wird von **CIM \_ LogicalDevice** geerbt.</span><span class="sxs-lookup"><span data-stu-id="c00cc-486">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c00cc-487"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="c00cc-487"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="c00cc-488"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="c00cc-488"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="c00cc-489">Energiebezogene Kapazitäten werden für dieses Gerät nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c00cc-489">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c00cc-490"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="c00cc-490"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="c00cc-491"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="c00cc-491"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c00cc-492">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c00cc-492">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="c00cc-493"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="c00cc-493"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="c00cc-494">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="c00cc-494">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="c00cc-495"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="c00cc-495"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="c00cc-496">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c00cc-496">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="c00cc-497">Diese Methode wird in der übergeordneten **CIM \_ LogicalDevice** -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="c00cc-497">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="c00cc-498">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="c00cc-498">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="c00cc-499"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="c00cc-499"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="c00cc-500">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c00cc-500">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="c00cc-501"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="c00cc-501"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="c00cc-502">Zeitgesteuerte Power-On unterstützt</span><span class="sxs-lookup"><span data-stu-id="c00cc-502">Timed Power-On Supported</span></span>

<span data-ttu-id="c00cc-503">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) und die *Uhrzeit* auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c00cc-503">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c00cc-504">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="c00cc-504">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c00cc-505">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="c00cc-505">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-506">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c00cc-506">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c00cc-507">Wenn der Wert **true** ist, kann das Gerät Energie gesteuert werden (kann in den Unterbrechungs Modus versetzt werden usw.).</span><span class="sxs-lookup"><span data-stu-id="c00cc-507">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="c00cc-508">Die-Eigenschaft gibt nicht an, dass die Energie Verwaltungsfunktionen zurzeit aktiviert sind, sondern nur, dass das logische Gerät für die Energie Verwaltung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="c00cc-508">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="c00cc-509">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c00cc-509">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c00cc-510">**Report Setmarks**</span><span class="sxs-lookup"><span data-stu-id="c00cc-510">**ReportSetMarks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c00cc-511">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c00cc-511">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-512">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c00cc-512">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-513">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Tape Backup Structures \| [**Tape \_ get \_ Drive \_ Parameters**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters) \| reportsetmarks")</span><span class="sxs-lookup"><span data-stu-id="c00cc-513">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tape Backup Structures\|[**TAPE\_GET\_DRIVE\_PARAMETERS**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters)\|ReportSetmarks")</span></span>
</dt> </dl>

<span data-ttu-id="c00cc-514">**True** gibt an, dass die setmark-Berichterstellung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="c00cc-514">If **TRUE**, setmark reporting is enabled.</span></span> <span data-ttu-id="c00cc-515">Die setmark-Berichterstellung verwendet ein spezielles aufgenommenes Element, das keine Benutzerdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="c00cc-515">Setmark reporting makes use of a specialized recorded element that does not contain user data.</span></span> <span data-ttu-id="c00cc-516">Dieses aufgezeichnete Element wird verwendet, um ein Segmentierungs Schema bereitzustellen, das Datei Markierungen hierarchisch überlegen ist.</span><span class="sxs-lookup"><span data-stu-id="c00cc-516">This recorded element is used to provide a segmentation scheme that is hierarchically superior to filemarks.</span></span> <span data-ttu-id="c00cc-517">Mit Setmarks wird eine schnellere Positionierung bei Bändern mit hoher Kapazität ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="c00cc-517">Setmarks provide faster positioning on high-capacity tapes.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="c00cc-518"><span id="0"></span>**1,0**</span><span class="sxs-lookup"><span data-stu-id="c00cc-518"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="c00cc-519">false</span><span class="sxs-lookup"><span data-stu-id="c00cc-519">FALSE</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="c00cc-520"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="c00cc-520"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="c00cc-521">TRUE</span><span class="sxs-lookup"><span data-stu-id="c00cc-521">TRUE</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c00cc-522">**Status**</span><span class="sxs-lookup"><span data-stu-id="c00cc-522">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c00cc-523">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c00cc-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-524">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c00cc-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-525">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="c00cc-525">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="c00cc-526">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="c00cc-526">Current status of the object.</span></span> <span data-ttu-id="c00cc-527">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="c00cc-527">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="c00cc-528">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="c00cc-528">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="c00cc-529">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="c00cc-529">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="c00cc-530">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="c00cc-530">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="c00cc-531">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="c00cc-531">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="c00cc-532">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c00cc-532">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="c00cc-533">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="c00cc-533">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="c00cc-534">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="c00cc-534">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="c00cc-535">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="c00cc-535">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c00cc-536">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="c00cc-536">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c00cc-537">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="c00cc-537">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="c00cc-538">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="c00cc-538">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="c00cc-539">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="c00cc-539">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="c00cc-540">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="c00cc-540">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="c00cc-541">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="c00cc-541">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="c00cc-542">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="c00cc-542">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="c00cc-543">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="c00cc-543">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="c00cc-544">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="c00cc-544">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="c00cc-545">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="c00cc-545">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c00cc-546">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="c00cc-546">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c00cc-547">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c00cc-547">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-548">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c00cc-548">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-549">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="c00cc-549">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="c00cc-550">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="c00cc-550">State of the logical device.</span></span> <span data-ttu-id="c00cc-551">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 (nicht zutreffend) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c00cc-551">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="c00cc-552">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c00cc-552">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c00cc-553">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="c00cc-553">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c00cc-554">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="c00cc-554">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="c00cc-555">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="c00cc-555">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c00cc-556">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="c00cc-556">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="c00cc-557">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="c00cc-557">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c00cc-558">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="c00cc-558">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c00cc-559">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c00cc-559">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-560">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c00cc-560">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-561">Qualifizierer [**: weiter**](../wmisdk/standard-qualifiers.md) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="c00cc-561">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="c00cc-562">Der Wert der Eigenschaft " **kreationclassname** " des Bereichs Computers.</span><span class="sxs-lookup"><span data-stu-id="c00cc-562">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="c00cc-563">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c00cc-563">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c00cc-564">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="c00cc-564">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c00cc-565">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c00cc-565">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-566">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c00cc-566">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c00cc-567">Qualifizierer [**: weiter**](../wmisdk/standard-qualifiers.md) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="c00cc-567">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="c00cc-568">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="c00cc-568">Name of the scoping system.</span></span>

<span data-ttu-id="c00cc-569">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="c00cc-569">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c00cc-570">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c00cc-570">Remarks</span></span>

<span data-ttu-id="c00cc-571">Die **Win32 \_ TapeDrive** -Klasse wird von [**CIM \_ TapeDrive**](cim-tapedrive.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="c00cc-571">The **Win32\_TapeDrive** class is derived from [**CIM\_TapeDrive**](cim-tapedrive.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c00cc-572">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c00cc-572">Requirements</span></span>



| <span data-ttu-id="c00cc-573">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c00cc-573">Requirement</span></span> | <span data-ttu-id="c00cc-574">Wert</span><span class="sxs-lookup"><span data-stu-id="c00cc-574">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c00cc-575">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c00cc-575">Minimum supported client</span></span><br/> | <span data-ttu-id="c00cc-576">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c00cc-576">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c00cc-577">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c00cc-577">Minimum supported server</span></span><br/> | <span data-ttu-id="c00cc-578">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c00cc-578">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c00cc-579">Namespace</span><span class="sxs-lookup"><span data-stu-id="c00cc-579">Namespace</span></span><br/>                | <span data-ttu-id="c00cc-580">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c00cc-580">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c00cc-581">MOF</span><span class="sxs-lookup"><span data-stu-id="c00cc-581">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c00cc-582"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c00cc-582"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c00cc-583">DLL</span><span class="sxs-lookup"><span data-stu-id="c00cc-583">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c00cc-584"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c00cc-584"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c00cc-585">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c00cc-585">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c00cc-586">**CIM- \_ TapeDrive**</span><span class="sxs-lookup"><span data-stu-id="c00cc-586">**CIM\_TapeDrive**</span></span>](cim-tapedrive.md)
</dt> <dt>

[<span data-ttu-id="c00cc-587">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="c00cc-587">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
