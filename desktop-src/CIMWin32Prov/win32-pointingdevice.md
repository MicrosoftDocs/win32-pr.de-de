---
description: Die \_ WMI-Klasse von Win32 pointingdevice stellt ein Eingabegerät dar, das verwendet wird, um auf die Anzeige eines Computer Systems, auf dem Windows ausgeführt wird, zu zeigen und diese auszuwählen
ms.assetid: ed81abe3-3d8f-48aa-ab64-9e6c87e44f64
ms.tgt_platform: multiple
title: Win32_PointingDevice-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PointingDevice
- Win32_PointingDevice.Reset
- Win32_PointingDevice.SetPowerState
- Win32_PointingDevice.Availability
- Win32_PointingDevice.Caption
- Win32_PointingDevice.ConfigManagerErrorCode
- Win32_PointingDevice.ConfigManagerUserConfig
- Win32_PointingDevice.CreationClassName
- Win32_PointingDevice.Description
- Win32_PointingDevice.DeviceID
- Win32_PointingDevice.DeviceInterface
- Win32_PointingDevice.DoubleSpeedThreshold
- Win32_PointingDevice.ErrorCleared
- Win32_PointingDevice.ErrorDescription
- Win32_PointingDevice.Handedness
- Win32_PointingDevice.HardwareType
- Win32_PointingDevice.InfFileName
- Win32_PointingDevice.InfSection
- Win32_PointingDevice.InstallDate
- Win32_PointingDevice.IsLocked
- Win32_PointingDevice.LastErrorCode
- Win32_PointingDevice.Manufacturer
- Win32_PointingDevice.Name
- Win32_PointingDevice.NumberOfButtons
- Win32_PointingDevice.PNPDeviceID
- Win32_PointingDevice.PointingType
- Win32_PointingDevice.PowerManagementCapabilities
- Win32_PointingDevice.PowerManagementSupported
- Win32_PointingDevice.QuadSpeedThreshold
- Win32_PointingDevice.Resolution
- Win32_PointingDevice.SampleRate
- Win32_PointingDevice.Status
- Win32_PointingDevice.StatusInfo
- Win32_PointingDevice.Synch
- Win32_PointingDevice.SystemCreationClassName
- Win32_PointingDevice.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3e4f2359e19476dfae111fc361f48e6f73d8cfac
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106338890"
---
# <a name="win32_pointingdevice-class"></a><span data-ttu-id="7f086-103">Win32- \_ pointingdevice-Klasse</span><span class="sxs-lookup"><span data-stu-id="7f086-103">Win32\_PointingDevice class</span></span>

<span data-ttu-id="7f086-104">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) von **Win32 \_ pointingdevice** stellt ein Eingabegerät dar, das verwendet wird, um auf die Anzeige eines Computer Systems, auf dem Windows ausgeführt wird, zu zeigen und diese auszuwählen</span><span class="sxs-lookup"><span data-stu-id="7f086-104">The **Win32\_PointingDevice** [WMI class](../wmisdk/retrieving-a-class.md) represents an input device used to point to and select regions on the display of a computer system running Windows.</span></span> <span data-ttu-id="7f086-105">Alle Geräte, die zur Bearbeitung eines Zeigers verwendet werden, oder zeigen auf die Anzeige auf einem Computersystem, auf dem Windows ausgeführt wird, sind ein Mitglied dieser Klasse.</span><span class="sxs-lookup"><span data-stu-id="7f086-105">Any device used to manipulate a pointer, or point to the display on a computer system running Windows is a member of this class.</span></span>

<span data-ttu-id="7f086-106">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7f086-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="7f086-107">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="7f086-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f086-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f086-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4B4-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_PointingDevice : CIM_PointingDevice
{
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  uint16   DeviceInterface;
  uint32   DoubleSpeedThreshold;
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint16   Handedness;
  string   HardwareType;
  string   InfFileName;
  string   InfSection;
  datetime InstallDate;
  boolean  IsLocked;
  uint32   LastErrorCode;
  string   Manufacturer;
  string   Name;
  uint8    NumberOfButtons;
  string   PNPDeviceID;
  uint16   PointingType;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint32   QuadSpeedThreshold;
  uint32   Resolution;
  uint32   SampleRate;
  string   Status;
  uint16   StatusInfo;
  uint32   Synch;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="7f086-109">Member</span><span class="sxs-lookup"><span data-stu-id="7f086-109">Members</span></span>

<span data-ttu-id="7f086-110">Die **Win32 \_ pointingdevice** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="7f086-110">The **Win32\_PointingDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="7f086-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="7f086-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="7f086-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7f086-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7f086-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="7f086-113">Methods</span></span>

<span data-ttu-id="7f086-114">Die **Win32 \_ pointingdevice** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="7f086-114">The **Win32\_PointingDevice** class has these methods.</span></span>



| <span data-ttu-id="7f086-115">Methode</span><span class="sxs-lookup"><span data-stu-id="7f086-115">Method</span></span>            | <span data-ttu-id="7f086-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7f086-116">Description</span></span>                                                                                                                                                                                      |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f086-117">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="7f086-117">**Reset**</span></span>         | <span data-ttu-id="7f086-118">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="7f086-118">Not implemented.</span></span> <span data-ttu-id="7f086-119">Informationen zur Implementierung dieser Methode finden Sie unter der [**Reset**](reset-method-in-class-cim-controller.md) -Methode in [**CIM \_ pointingdevice**](cim-pointingdevice.md).</span><span class="sxs-lookup"><span data-stu-id="7f086-119">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_PointingDevice**](cim-pointingdevice.md).</span></span><br/>                 |
| <span data-ttu-id="7f086-120">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="7f086-120">**SetPowerState**</span></span> | <span data-ttu-id="7f086-121">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="7f086-121">Not implemented.</span></span> <span data-ttu-id="7f086-122">Informationen zur Implementierung dieser Methode finden Sie unter der [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode in [**CIM \_ pointingdevice**](cim-pointingdevice.md).</span><span class="sxs-lookup"><span data-stu-id="7f086-122">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_PointingDevice**](cim-pointingdevice.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="7f086-123">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7f086-123">Properties</span></span>

<span data-ttu-id="7f086-124">Die **Win32 \_ pointingdevice** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7f086-124">The **Win32\_PointingDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7f086-125">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="7f086-125">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f086-126">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7f086-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7f086-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7f086-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f086-128">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="7f086-128">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="7f086-129">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="7f086-129">Availability and status of the device.</span></span>

<span data-ttu-id="7f086-130">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7f086-130">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7f086-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="7f086-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7f086-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="7f086-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="7f086-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="7f086-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="7f086-134">Ausführung oder vollständiger Stromversorgung</span><span class="sxs-lookup"><span data-stu-id="7f086-134">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="7f086-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="7f086-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="7f086-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="7f086-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="7f086-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="7f086-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="7f086-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="7f086-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="7f086-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="7f086-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="7f086-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="7f086-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="7f086-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="7f086-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="7f086-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="7f086-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="7f086-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="7f086-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="7f086-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="7f086-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="7f086-145">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="7f086-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="7f086-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="7f086-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="7f086-147">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="7f086-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="7f086-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="7f086-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="7f086-149">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb gebracht werden.</span><span class="sxs-lookup"><span data-stu-id="7f086-149">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="7f086-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="7f086-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="7f086-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="7f086-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="7f086-152">Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="7f086-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="7f086-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="7f086-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="7f086-154">Das Gerät wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="7f086-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="7f086-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="7f086-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="7f086-156">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="7f086-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="7f086-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="7f086-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="7f086-158">Das Gerät ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="7f086-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="7f086-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="7f086-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="7f086-160">Das Gerät ist in Ruhe.</span><span class="sxs-lookup"><span data-stu-id="7f086-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7f086-161">**Caption**</span><span class="sxs-lookup"><span data-stu-id="7f086-161">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f086-162">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7f086-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f086-163">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7f086-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f086-164">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="7f086-164">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="7f086-165">Kurze Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="7f086-165">Short description of the object.</span></span>

<span data-ttu-id="7f086-166">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7f086-166">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f086-167">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="7f086-167">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f086-168">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7f086-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7f086-169">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7f086-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f086-170">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="7f086-170">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="7f086-171">Win32-Configuration Manager Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="7f086-171">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="7f086-172">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7f086-172">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="7f086-173"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="7f086-173"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="7f086-174"> (0)</span><span class="sxs-lookup"><span data-stu-id="7f086-174">(0)</span></span>


</dt> <dd>

<span data-ttu-id="7f086-175">Das Gerät funktioniert ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="7f086-175">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="7f086-176"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="7f086-176"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="7f086-177">(1)</span><span class="sxs-lookup"><span data-stu-id="7f086-177">(1)</span></span>


</dt> <dd>

<span data-ttu-id="7f086-178">Das Gerät ist nicht ordnungsgemäß konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="7f086-178">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="7f086-179"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="7f086-179"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="7f086-180">(2)</span><span class="sxs-lookup"><span data-stu-id="7f086-180">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="7f086-181"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="7f086-181"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="7f086-182">(3)</span><span class="sxs-lookup"><span data-stu-id="7f086-182">(3)</span></span>


</dt> <dd>

<span data-ttu-id="7f086-183">Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt möglicherweise nicht über genügend Arbeitsspeicher oder andere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="7f086-183">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="7f086-184"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="7f086-184"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="7f086-185">(4)</span><span class="sxs-lookup"><span data-stu-id="7f086-185">(4)</span></span>


</dt> <dd>

<span data-ttu-id="7f086-186">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="7f086-186">Device is not working properly.</span></span> <span data-ttu-id="7f086-187">Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="7f086-187">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="7f086-188"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="7f086-188"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="7f086-189">(5)</span><span class="sxs-lookup"><span data-stu-id="7f086-189">(5)</span></span>


</dt> <dd>

<span data-ttu-id="7f086-190">Der Treiber für das Gerät erfordert eine Ressource, die von Windows nicht verwaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="7f086-190">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="7f086-191"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="7f086-191"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="7f086-192"> (6)</span><span class="sxs-lookup"><span data-stu-id="7f086-192">(6)</span></span>


</dt> <dd>

<span data-ttu-id="7f086-193">Die Startkonfiguration für das Gerät steht in Konflikt mit anderen Geräten.</span><span class="sxs-lookup"><span data-stu-id="7f086-193">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="7f086-194"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="7f086-194"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="7f086-195">(7)</span><span class="sxs-lookup"><span data-stu-id="7f086-195">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="7f086-196"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="7f086-196"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="7f086-197">(8)</span><span class="sxs-lookup"><span data-stu-id="7f086-197">(8)</span></span>


</dt> <dd>

<span data-ttu-id="7f086-198">Das Treiber Lade Modul für das Gerät fehlt.</span><span class="sxs-lookup"><span data-stu-id="7f086-198">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="7f086-199"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="7f086-199"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="7f086-200">(9)</span><span class="sxs-lookup"><span data-stu-id="7f086-200">(9)</span></span>


</dt> <dd>

<span data-ttu-id="7f086-201">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="7f086-201">Device is not working properly.</span></span> <span data-ttu-id="7f086-202">Die Steuerungs Firmware meldet nicht korrekt die Ressourcen für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="7f086-202">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="7f086-203"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="7f086-203"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="7f086-204">(10)</span><span class="sxs-lookup"><span data-stu-id="7f086-204">(10)</span></span>


</dt> <dd>

<span data-ttu-id="7f086-205">Das Gerät kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="7f086-205">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="7f086-206"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="7f086-206"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="7f086-207">(11)</span><span class="sxs-lookup"><span data-stu-id="7f086-207">(11)</span></span>


</dt> <dd>

<span data-ttu-id="7f086-208">Fehler beim Gerät.</span><span class="sxs-lookup"><span data-stu-id="7f086-208">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="7f086-209"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="7f086-209"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="7f086-210">(12)</span><span class="sxs-lookup"><span data-stu-id="7f086-210">(12)</span></span>


</dt> <dd>

<span data-ttu-id="7f086-211">Das Gerät kann nicht genug freie Ressourcen für die Verwendung finden.</span><span class="sxs-lookup"><span data-stu-id="7f086-211">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="7f086-212"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="7f086-212"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="7f086-213">(13)</span><span class="sxs-lookup"><span data-stu-id="7f086-213">(13)</span></span>


</dt> <dd>

<span data-ttu-id="7f086-214">Die Geräte Ressourcen können nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="7f086-214">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="7f086-215"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="7f086-215"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="7f086-216">(14)</span><span class="sxs-lookup"><span data-stu-id="7f086-216">(14)</span></span>


</dt> <dd>

<span data-ttu-id="7f086-217">Das Gerät kann erst ordnungsgemäß funktionieren, wenn der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="7f086-217">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="7f086-218"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="7f086-218"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="7f086-219">(15)</span><span class="sxs-lookup"><span data-stu-id="7f086-219">(15)</span></span>


</dt> <dd>

<span data-ttu-id="7f086-220">Das Gerät funktioniert aufgrund eines möglichen erneuten Aufzählungs Problems nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="7f086-220">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="7f086-221"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="7f086-221"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="7f086-222">(16)</span><span class="sxs-lookup"><span data-stu-id="7f086-222">(16)</span></span>


</dt> <dd>

<span data-ttu-id="7f086-223">In Windows können nicht alle Ressourcen identifiziert werden, die vom Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7f086-223">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="7f086-224"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="7f086-224"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="7f086-225">(17)</span><span class="sxs-lookup"><span data-stu-id="7f086-225">(17)</span></span>


</dt> <dd>

<span data-ttu-id="7f086-226">Das Gerät fordert einen unbekannten Ressourcentyp an.</span><span class="sxs-lookup"><span data-stu-id="7f086-226">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="7f086-227"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="7f086-227"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="7f086-228">(18)</span><span class="sxs-lookup"><span data-stu-id="7f086-228">(18)</span></span>


</dt> <dd>

<span data-ttu-id="7f086-229">Gerätetreiber müssen neu installiert werden.</span><span class="sxs-lookup"><span data-stu-id="7f086-229">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="7f086-230"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="7f086-230"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="7f086-231">(19)</span><span class="sxs-lookup"><span data-stu-id="7f086-231">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="7f086-232"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="7f086-232"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="7f086-233">(20)</span><span class="sxs-lookup"><span data-stu-id="7f086-233">(20)</span></span>


</dt> <dd>

<span data-ttu-id="7f086-234">Die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="7f086-234">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="7f086-235"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="7f086-235"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="7f086-236">(21)</span><span class="sxs-lookup"><span data-stu-id="7f086-236">(21)</span></span>


</dt> <dd>

<span data-ttu-id="7f086-237">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="7f086-237">System failure.</span></span> <span data-ttu-id="7f086-238">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="7f086-238">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="7f086-239">Das Gerät wird von Windows entfernt.</span><span class="sxs-lookup"><span data-stu-id="7f086-239">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="7f086-240"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="7f086-240"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="7f086-241">(22)</span><span class="sxs-lookup"><span data-stu-id="7f086-241">(22)</span></span>


</dt> <dd>

<span data-ttu-id="7f086-242">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="7f086-242">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="7f086-243"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="7f086-243"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="7f086-244">(23)</span><span class="sxs-lookup"><span data-stu-id="7f086-244">(23)</span></span>


</dt> <dd>

<span data-ttu-id="7f086-245">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="7f086-245">System failure.</span></span> <span data-ttu-id="7f086-246">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="7f086-246">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="7f086-247"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="7f086-247"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="7f086-248">(24)</span><span class="sxs-lookup"><span data-stu-id="7f086-248">(24)</span></span>


</dt> <dd>

<span data-ttu-id="7f086-249">Das Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.</span><span class="sxs-lookup"><span data-stu-id="7f086-249">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="7f086-250"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="7f086-250"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="7f086-251">(25)</span><span class="sxs-lookup"><span data-stu-id="7f086-251">(25)</span></span>


</dt> <dd>

<span data-ttu-id="7f086-252">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="7f086-252">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="7f086-253"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="7f086-253"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="7f086-254">(26)</span><span class="sxs-lookup"><span data-stu-id="7f086-254">(26)</span></span>


</dt> <dd>

<span data-ttu-id="7f086-255">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="7f086-255">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="7f086-256"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="7f086-256"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="7f086-257">(27)</span><span class="sxs-lookup"><span data-stu-id="7f086-257">(27)</span></span>


</dt> <dd>

<span data-ttu-id="7f086-258">Das Gerät verfügt nicht über eine gültige Protokoll Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="7f086-258">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="7f086-259"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="7f086-259"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="7f086-260">(28)</span><span class="sxs-lookup"><span data-stu-id="7f086-260">(28)</span></span>


</dt> <dd>

<span data-ttu-id="7f086-261">Gerätetreiber sind nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="7f086-261">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="7f086-262"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="7f086-262"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="7f086-263">(29)</span><span class="sxs-lookup"><span data-stu-id="7f086-263">(29)</span></span>


</dt> <dd>

<span data-ttu-id="7f086-264">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="7f086-264">Device is disabled.</span></span> <span data-ttu-id="7f086-265">Die Gerätefirmware hat nicht die erforderlichen Ressourcen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="7f086-265">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="7f086-266"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="7f086-266"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="7f086-267">(30)</span><span class="sxs-lookup"><span data-stu-id="7f086-267">(30)</span></span>


</dt> <dd>

<span data-ttu-id="7f086-268">Das Gerät verwendet eine UNQ-Ressource, die von einem anderen Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7f086-268">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="7f086-269"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="7f086-269"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="7f086-270">31,5</span><span class="sxs-lookup"><span data-stu-id="7f086-270">(31)</span></span>


</dt> <dd>

<span data-ttu-id="7f086-271">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="7f086-271">Device is not working properly.</span></span> <span data-ttu-id="7f086-272">Die erforderlichen Gerätetreiber können nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="7f086-272">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7f086-273">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="7f086-273">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f086-274">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="7f086-274">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7f086-275">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7f086-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f086-276">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="7f086-276">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="7f086-277">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="7f086-277">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="7f086-278">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7f086-278">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f086-279">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="7f086-279">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f086-280">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7f086-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f086-281">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7f086-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f086-282">Qualifizierer: [ **CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="7f086-282">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="7f086-283">Der Name der ersten konkreten Klasse, die in der Vererbungs Kette angezeigt werden soll, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7f086-283">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="7f086-284">Bei Verwendung mit den anderen Schlüsseleigenschaften der-Klasse ermöglicht die-Eigenschaft, dass alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="7f086-284">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="7f086-285">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7f086-285">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f086-286">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7f086-286">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f086-287">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7f086-287">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f086-288">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7f086-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f086-289">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="7f086-289">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="7f086-290">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="7f086-290">Description of the object.</span></span>

<span data-ttu-id="7f086-291">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7f086-291">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f086-292">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="7f086-292">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f086-293">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7f086-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f086-294">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7f086-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f086-295">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("toviceid"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="7f086-295">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="7f086-296">Eindeutiger Bezeichner des Zeige Geräts mit anderen Geräten im System.</span><span class="sxs-lookup"><span data-stu-id="7f086-296">Unique identifier of the pointing device with other devices on the system.</span></span>

<span data-ttu-id="7f086-297">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7f086-297">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f086-298">**Geräte-tergesicht**</span><span class="sxs-lookup"><span data-stu-id="7f086-298">**DeviceInterface**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f086-299">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7f086-299">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7f086-300">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7f086-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f086-301">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS- \| Typ 21- \| Schnittstelle")</span><span class="sxs-lookup"><span data-stu-id="7f086-301">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 21\|Interface")</span></span>
</dt> </dl>

<span data-ttu-id="7f086-302">Der Typ der Schnittstelle, die für das Zeigegerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7f086-302">Type of interface used for the pointing device.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7f086-303">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="7f086-303">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7f086-304">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="7f086-304">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial"></span><span id="serial"></span><span id="SERIAL"></span>

<span data-ttu-id="7f086-305">**Seriell** (3)</span><span class="sxs-lookup"><span data-stu-id="7f086-305">**Serial** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="PS_2"></span><span id="ps_2"></span>

<span data-ttu-id="7f086-306">**PS/2** (4)</span><span class="sxs-lookup"><span data-stu-id="7f086-306">**PS/2** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>

<span data-ttu-id="7f086-307">**Infrarot** (5)</span><span class="sxs-lookup"><span data-stu-id="7f086-307">**Infrared** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="HP-HIL"></span><span id="hp-hil"></span>

<span data-ttu-id="7f086-308">**HP-HIL** (6)</span><span class="sxs-lookup"><span data-stu-id="7f086-308">**HP-HIL** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Bus_mouse"></span><span id="bus_mouse"></span><span id="BUS_MOUSE"></span>

<span data-ttu-id="7f086-309">**Busmaus** (7)</span><span class="sxs-lookup"><span data-stu-id="7f086-309">**Bus mouse** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="ADB__Apple_Desktop_Bus_"></span><span id="adb__apple_desktop_bus_"></span><span id="ADB__APPLE_DESKTOP_BUS_"></span>

<span data-ttu-id="7f086-310">**ADB (Apple-desktopbus)** (8)</span><span class="sxs-lookup"><span data-stu-id="7f086-310">**ADB (Apple Desktop Bus)** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Bus_mouse_DB-9"></span><span id="bus_mouse_db-9"></span><span id="BUS_MOUSE_DB-9"></span>

<span data-ttu-id="7f086-311">**Bus Mouse DB-9** (160)</span><span class="sxs-lookup"><span data-stu-id="7f086-311">**Bus mouse DB-9** (160)</span></span>


</dt> <dd></dd> <dt>

<span id="Bus_mouse_micro-DIN"></span><span id="bus_mouse_micro-din"></span><span id="BUS_MOUSE_MICRO-DIN"></span>

<span data-ttu-id="7f086-312">**Busmaus Mikro-DIN** (161)</span><span class="sxs-lookup"><span data-stu-id="7f086-312">**Bus mouse micro-DIN** (161)</span></span>


</dt> <dd></dd> <dt>

<span id="USB"></span><span id="usb"></span>

<span data-ttu-id="7f086-313">**USB** (162)</span><span class="sxs-lookup"><span data-stu-id="7f086-313">**USB** (162)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7f086-314">**DoubleSpeedThreshold**</span><span class="sxs-lookup"><span data-stu-id="7f086-314">**DoubleSpeedThreshold**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f086-315">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7f086-315">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7f086-316">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7f086-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f086-317">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| System Information Functions \| SystemParametersInfo"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Mickeys")</span><span class="sxs-lookup"><span data-stu-id="7f086-317">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Functions\|SystemParametersInfo"), [**Units**](../wmisdk/standard-qualifiers.md) ("mickeys")</span></span>
</dt> </dl>

<span data-ttu-id="7f086-318">Einer von zwei Beschleunigungswerten.</span><span class="sxs-lookup"><span data-stu-id="7f086-318">One of two acceleration values.</span></span> <span data-ttu-id="7f086-319">Die Empfindlichkeit der Zeigegeräte verdoppelt sich (wechselt vom ersten zum zweiten Wert), wenn das Zeigegerät einen Abstand über diesem Schwellenwert erreicht.</span><span class="sxs-lookup"><span data-stu-id="7f086-319">The sensitivity of the pointing device doubles (toggles from the first to the second value) when the pointing device moves a distance greater than this threshold value.</span></span>

</dd> <dt>

<span data-ttu-id="7f086-320">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="7f086-320">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f086-321">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="7f086-321">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7f086-322">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7f086-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f086-323">**True** gibt an, dass der in **LastErrorCode** gemeldete Fehler jetzt gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="7f086-323">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="7f086-324">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7f086-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f086-325">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="7f086-325">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f086-326">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7f086-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f086-327">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7f086-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f086-328">Weitere Informationen zu dem Fehler, der in " **LastErrorCode**" aufgezeichnet wurde, sowie Informationen zu ggf. getroffenen Korrekturmaßnahmen.</span><span class="sxs-lookup"><span data-stu-id="7f086-328">More information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="7f086-329">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7f086-329">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f086-330">**Händigkeit**</span><span class="sxs-lookup"><span data-stu-id="7f086-330">**Handedness**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f086-331">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7f086-331">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7f086-332">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7f086-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f086-333">Konfiguration des Zeige Geräts für den linken oder rechten Vorgang.</span><span class="sxs-lookup"><span data-stu-id="7f086-333">Configuration of the pointing device for left-hand or right-hand operation.</span></span>

<span data-ttu-id="7f086-334">Diese Eigenschaft wird von [**CIM \_ pointingdevice**](cim-pointingdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7f086-334">This property is inherited from [**CIM\_PointingDevice**](cim-pointingdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7f086-335"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="7f086-335"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="7f086-336"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (1)</span><span class="sxs-lookup"><span data-stu-id="7f086-336"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Right_Handed_Operation"></span><span id="right_handed_operation"></span><span id="RIGHT_HANDED_OPERATION"></span>

<span data-ttu-id="7f086-337"><span id="Right_Handed_Operation"></span><span id="right_handed_operation"></span><span id="RIGHT_HANDED_OPERATION"></span>**Rechter übergebenen Vorgang** (2)</span><span class="sxs-lookup"><span data-stu-id="7f086-337"><span id="Right_Handed_Operation"></span><span id="right_handed_operation"></span><span id="RIGHT_HANDED_OPERATION"></span>**Right Handed Operation** (2)</span></span>


</dt> <dd>

<span data-ttu-id="7f086-338">Right-Handed Vorgang</span><span class="sxs-lookup"><span data-stu-id="7f086-338">Right-Handed Operation</span></span>

</dd> <dt>

<span id="Left_Handed_Operation"></span><span id="left_handed_operation"></span><span id="LEFT_HANDED_OPERATION"></span>

<span data-ttu-id="7f086-339"><span id="Left_Handed_Operation"></span><span id="left_handed_operation"></span><span id="LEFT_HANDED_OPERATION"></span>**Linker Vorgang** (3)</span><span class="sxs-lookup"><span data-stu-id="7f086-339"><span id="Left_Handed_Operation"></span><span id="left_handed_operation"></span><span id="LEFT_HANDED_OPERATION"></span>**Left Handed Operation** (3)</span></span>


</dt> <dd>

<span data-ttu-id="7f086-340">Left-Handed Vorgang</span><span class="sxs-lookup"><span data-stu-id="7f086-340">Left-Handed Operation</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7f086-341">**Hardwaretype**</span><span class="sxs-lookup"><span data-stu-id="7f086-341">**HardwareType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f086-342">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7f086-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f086-343">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7f086-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f086-344">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ System \\ \\ ControlSet001 \\ \\ Control \\ \\ Class \| DriverDesc")</span><span class="sxs-lookup"><span data-stu-id="7f086-344">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SYSTEM\\\\ControlSet001\\\\Control\\\\Class\|DriverDesc")</span></span>
</dt> </dl>

<span data-ttu-id="7f086-345">Der Typ der Hardware, die für das Windows-Zeigegerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7f086-345">Type of hardware used for the Windows pointing device.</span></span>

<span data-ttu-id="7f086-346">Beispiel: "Microsoft PS2 Mouse"</span><span class="sxs-lookup"><span data-stu-id="7f086-346">Example: "MICROSOFT PS2 MOUSE"</span></span>

</dd> <dt>

<span data-ttu-id="7f086-347">**INFFILENAME**</span><span class="sxs-lookup"><span data-stu-id="7f086-347">**InfFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f086-348">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7f086-348">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f086-349">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7f086-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f086-350">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| INFPath")</span><span class="sxs-lookup"><span data-stu-id="7f086-350">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|InfPath")</span></span>
</dt> </dl>

<span data-ttu-id="7f086-351">Der Name der INF-Datei für das Windows-Zeigegerät.</span><span class="sxs-lookup"><span data-stu-id="7f086-351">Name of the .inf file for the Windows pointing device.</span></span>

<span data-ttu-id="7f086-352">Beispiel: "ab. inf"</span><span class="sxs-lookup"><span data-stu-id="7f086-352">Example: "ab.inf"</span></span>

</dd> <dt>

<span data-ttu-id="7f086-353">**InfSection**</span><span class="sxs-lookup"><span data-stu-id="7f086-353">**InfSection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f086-354">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7f086-354">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f086-355">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7f086-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f086-356">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| InfSection")</span><span class="sxs-lookup"><span data-stu-id="7f086-356">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|InfSection")</span></span>
</dt> </dl>

<span data-ttu-id="7f086-357">Abschnitt der INF-Datei, die Konfigurationsinformationen für das Windows-Zeigegerät enthält.</span><span class="sxs-lookup"><span data-stu-id="7f086-357">Section of the .inf file that holds configuration information for the Windows pointing device.</span></span>

</dd> <dt>

<span data-ttu-id="7f086-358">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="7f086-358">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f086-359">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="7f086-359">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7f086-360">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7f086-360">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f086-361">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="7f086-361">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="7f086-362">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="7f086-362">Date and time the object was installed.</span></span> <span data-ttu-id="7f086-363">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="7f086-363">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="7f086-364">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7f086-364">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f086-365">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="7f086-365">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f086-366">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="7f086-366">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7f086-367">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7f086-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f086-368">**True** gibt an, dass das Gerät gesperrt ist und Benutzereingaben oder-Ausgaben verhindert.</span><span class="sxs-lookup"><span data-stu-id="7f086-368">If **TRUE**, the device is locked, preventing user input or output.</span></span>

<span data-ttu-id="7f086-369">Diese Eigenschaft wird von [**CIM \_ userdevice**](cim-userdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7f086-369">This property is inherited from [**CIM\_UserDevice**](cim-userdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f086-370">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="7f086-370">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f086-371">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7f086-371">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7f086-372">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7f086-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f086-373">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="7f086-373">Last error code reported by the logical device.</span></span>

<span data-ttu-id="7f086-374">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7f086-374">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f086-375">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="7f086-375">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f086-376">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7f086-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f086-377">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7f086-377">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f086-378">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="7f086-378">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="7f086-379">Der Name des Herstellers des Prozessors.</span><span class="sxs-lookup"><span data-stu-id="7f086-379">Name of the processor's manufacturer.</span></span>

<span data-ttu-id="7f086-380">Beispiel: "GenuineSilicon"</span><span class="sxs-lookup"><span data-stu-id="7f086-380">Example: "GenuineSilicon"</span></span>

</dd> <dt>

<span data-ttu-id="7f086-381">**Name**</span><span class="sxs-lookup"><span data-stu-id="7f086-381">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f086-382">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7f086-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f086-383">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7f086-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f086-384">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="7f086-384">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="7f086-385">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="7f086-385">Label by which the object is known.</span></span> <span data-ttu-id="7f086-386">Bei einer Unterklasse kann die Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="7f086-386">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="7f086-387">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7f086-387">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f086-388">**Anzahl von Schaltflächen**</span><span class="sxs-lookup"><span data-stu-id="7f086-388">**NumberOfButtons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f086-389">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="7f086-389">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="7f086-390">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7f086-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f086-391">Anzahl der Schaltflächen auf dem Zeigegerät.</span><span class="sxs-lookup"><span data-stu-id="7f086-391">Number of buttons on the pointing device.</span></span>

<span data-ttu-id="7f086-392">Diese Eigenschaft wird von [**CIM \_ pointingdevice**](cim-pointingdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7f086-392">This property is inherited from [**CIM\_PointingDevice**](cim-pointingdevice.md).</span></span>

<span data-ttu-id="7f086-393">Beispiel: 2</span><span class="sxs-lookup"><span data-stu-id="7f086-393">Example: 2</span></span>

</dd> <dt>

<span data-ttu-id="7f086-394">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="7f086-394">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f086-395">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7f086-395">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f086-396">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7f086-396">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f086-397">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="7f086-397">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="7f086-398">Windows Plug & Play Geräte Bezeichner des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="7f086-398">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="7f086-399">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7f086-399">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="7f086-400">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="7f086-400">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="7f086-401">**Pointingtype**</span><span class="sxs-lookup"><span data-stu-id="7f086-401">**PointingType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f086-402">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7f086-402">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7f086-403">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7f086-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f086-404">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| zeigt Gerät \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="7f086-404">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Pointing Device\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="7f086-405">Typ des Zeige Geräts.</span><span class="sxs-lookup"><span data-stu-id="7f086-405">Type of pointing device.</span></span>

<span data-ttu-id="7f086-406">Diese Eigenschaft wird von [**CIM \_ pointingdevice**](cim-pointingdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7f086-406">This property is inherited from [**CIM\_PointingDevice**](cim-pointingdevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7f086-407"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="7f086-407"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7f086-408"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="7f086-408"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Mouse"></span><span id="mouse"></span><span id="MOUSE"></span>

<span data-ttu-id="7f086-409"><span id="Mouse"></span><span id="mouse"></span><span id="MOUSE"></span>**Maus** (3)</span><span class="sxs-lookup"><span data-stu-id="7f086-409"><span id="Mouse"></span><span id="mouse"></span><span id="MOUSE"></span>**Mouse** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Track_Ball"></span><span id="track_ball"></span><span id="TRACK_BALL"></span>

<span data-ttu-id="7f086-410"><span id="Track_Ball"></span><span id="track_ball"></span><span id="TRACK_BALL"></span>**Ball verfolgen** (4)</span><span class="sxs-lookup"><span data-stu-id="7f086-410"><span id="Track_Ball"></span><span id="track_ball"></span><span id="TRACK_BALL"></span>**Track Ball** (4)</span></span>


</dt> <dd>

<span data-ttu-id="7f086-411">Trackballunterstützung</span><span class="sxs-lookup"><span data-stu-id="7f086-411">Trackball</span></span>

</dd> <dt>

<span id="Track_Point"></span><span id="track_point"></span><span id="TRACK_POINT"></span>

<span data-ttu-id="7f086-412"><span id="Track_Point"></span><span id="track_point"></span><span id="TRACK_POINT"></span>Verfolgungs **Punkt** (5)</span><span class="sxs-lookup"><span data-stu-id="7f086-412"><span id="Track_Point"></span><span id="track_point"></span><span id="TRACK_POINT"></span>**Track Point** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Glide_Point"></span><span id="glide_point"></span><span id="GLIDE_POINT"></span>

<span data-ttu-id="7f086-413"><span id="Glide_Point"></span><span id="glide_point"></span><span id="GLIDE_POINT"></span>**Gleitspunkt** (6)</span><span class="sxs-lookup"><span data-stu-id="7f086-413"><span id="Glide_Point"></span><span id="glide_point"></span><span id="GLIDE_POINT"></span>**Glide Point** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Touch_Pad"></span><span id="touch_pad"></span><span id="TOUCH_PAD"></span>

<span data-ttu-id="7f086-414"><span id="Touch_Pad"></span><span id="touch_pad"></span><span id="TOUCH_PAD"></span>**Touchpad** (7)</span><span class="sxs-lookup"><span data-stu-id="7f086-414"><span id="Touch_Pad"></span><span id="touch_pad"></span><span id="TOUCH_PAD"></span>**Touch Pad** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Touch_Screen"></span><span id="touch_screen"></span><span id="TOUCH_SCREEN"></span>

<span data-ttu-id="7f086-415"><span id="Touch_Screen"></span><span id="touch_screen"></span><span id="TOUCH_SCREEN"></span>**Touchscreen** (8)</span><span class="sxs-lookup"><span data-stu-id="7f086-415"><span id="Touch_Screen"></span><span id="touch_screen"></span><span id="TOUCH_SCREEN"></span>**Touch Screen** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Mouse_-_Optical_Sensor"></span><span id="mouse_-_optical_sensor"></span><span id="MOUSE_-_OPTICAL_SENSOR"></span>

<span data-ttu-id="7f086-416"><span id="Mouse_-_Optical_Sensor"></span><span id="mouse_-_optical_sensor"></span><span id="MOUSE_-_OPTICAL_SENSOR"></span>**Maus optischer Sensor** (9)</span><span class="sxs-lookup"><span data-stu-id="7f086-416"><span id="Mouse_-_Optical_Sensor"></span><span id="mouse_-_optical_sensor"></span><span id="MOUSE_-_OPTICAL_SENSOR"></span>**Mouse - Optical Sensor** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7f086-417">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="7f086-417">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f086-418">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="7f086-418">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7f086-419">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7f086-419">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f086-420">Array der spezifischen energiebezogenen Funktionen eines logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="7f086-420">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="7f086-421">Diese Eigenschaft wird von **CIM \_ LogicalDevice** geerbt.</span><span class="sxs-lookup"><span data-stu-id="7f086-421">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7f086-422"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="7f086-422"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="7f086-423"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="7f086-423"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="7f086-424"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="7f086-424"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="7f086-425"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="7f086-425"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="7f086-426">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7f086-426">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="7f086-427"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="7f086-427"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="7f086-428">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="7f086-428">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="7f086-429"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="7f086-429"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="7f086-430">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7f086-430">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="7f086-431">Diese Methode wird in der übergeordneten **CIM \_ LogicalDevice** -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="7f086-431">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="7f086-432">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="7f086-432">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="7f086-433"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="7f086-433"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="7f086-434">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7f086-434">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="7f086-435"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="7f086-435"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="7f086-436">Zeitgesteuerte Power-On unterstützt</span><span class="sxs-lookup"><span data-stu-id="7f086-436">Timed Power-On Supported</span></span>

<span data-ttu-id="7f086-437">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) und die *Uhrzeit* auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7f086-437">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7f086-438">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="7f086-438">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f086-439">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="7f086-439">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7f086-440">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7f086-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f086-441">Wenn der Wert **true** ist, kann das Gerät Energie gesteuert werden (kann in den Unterbrechungs Modus versetzt werden usw.).</span><span class="sxs-lookup"><span data-stu-id="7f086-441">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="7f086-442">Die-Eigenschaft gibt nicht an, dass die Energie Verwaltungsfunktionen zurzeit aktiviert sind, sondern nur, dass das logische Gerät für die Energie Verwaltung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="7f086-442">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="7f086-443">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7f086-443">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f086-444">**Quadspeedthreshold**</span><span class="sxs-lookup"><span data-stu-id="7f086-444">**QuadSpeedThreshold**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f086-445">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7f086-445">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7f086-446">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7f086-446">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f086-447">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| System Information Functions \| SystemParametersInfo"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Mickeys")</span><span class="sxs-lookup"><span data-stu-id="7f086-447">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Functions\|SystemParametersInfo"), [**Units**](../wmisdk/standard-qualifiers.md) ("mickeys")</span></span>
</dt> </dl>

<span data-ttu-id="7f086-448">Einer von zwei Beschleunigungs Schwellenwerten.</span><span class="sxs-lookup"><span data-stu-id="7f086-448">One of two acceleration threshold values.</span></span> <span data-ttu-id="7f086-449">Das System verdoppelt die Geschwindigkeit der Zeiger Bewegung, wenn das Zeiger Gerät einen Abstand bewegt, der größer ist als dieser Wert.</span><span class="sxs-lookup"><span data-stu-id="7f086-449">The system doubles the speed of the pointer movement when the pointer device moves a distance greater than this value.</span></span> <span data-ttu-id="7f086-450">Da diese Geschwindigkeitssteigerung erreicht wird, nachdem der **Double-Threshold** -Wert erreicht wurde, wird der Zeiger um das Vierfache der ursprünglichen Geschwindigkeit verschoben.</span><span class="sxs-lookup"><span data-stu-id="7f086-450">Because this speed increase occurs after the **DoubleSpeedThreshold** value has been met, the pointer effectively moves at four times its original speed.</span></span>

</dd> <dt>

<span data-ttu-id="7f086-451">**Auflösung**</span><span class="sxs-lookup"><span data-stu-id="7f086-451">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f086-452">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7f086-452">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7f086-453">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7f086-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f086-454">Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Zählungen pro Zoll")</span><span class="sxs-lookup"><span data-stu-id="7f086-454">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("counts per inch")</span></span>
</dt> </dl>

<span data-ttu-id="7f086-455">Nach Verfolgungs Auflösung.</span><span class="sxs-lookup"><span data-stu-id="7f086-455">Tracking resolution.</span></span>

<span data-ttu-id="7f086-456">Diese Eigenschaft wird von [**CIM \_ pointingdevice**](cim-pointingdevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7f086-456">This property is inherited from [**CIM\_PointingDevice**](cim-pointingdevice.md).</span></span>

<span data-ttu-id="7f086-457">Beispiel: 0</span><span class="sxs-lookup"><span data-stu-id="7f086-457">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="7f086-458">**Sample Rate**</span><span class="sxs-lookup"><span data-stu-id="7f086-458">**SampleRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f086-459">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7f086-459">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7f086-460">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7f086-460">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f086-461">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Samplerate"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Hertz")</span><span class="sxs-lookup"><span data-stu-id="7f086-461">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SampleRate"), [**Units**](../wmisdk/standard-qualifiers.md) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="7f086-462">Rate, mit der das Zeigegerät nach Eingabeinformationen abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="7f086-462">Rate at which the pointing device is polled for input information.</span></span>

</dd> <dt>

<span data-ttu-id="7f086-463">**Status**</span><span class="sxs-lookup"><span data-stu-id="7f086-463">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f086-464">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7f086-464">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f086-465">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7f086-465">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f086-466">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="7f086-466">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="7f086-467">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="7f086-467">Current status of the object.</span></span> <span data-ttu-id="7f086-468">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="7f086-468">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="7f086-469">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="7f086-469">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="7f086-470">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="7f086-470">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="7f086-471">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="7f086-471">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="7f086-472">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="7f086-472">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="7f086-473">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7f086-473">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="7f086-474">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="7f086-474">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="7f086-475">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="7f086-475">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="7f086-476">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="7f086-476">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="7f086-477">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="7f086-477">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7f086-478">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="7f086-478">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="7f086-479">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="7f086-479">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="7f086-480">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="7f086-480">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="7f086-481">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="7f086-481">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="7f086-482">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="7f086-482">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="7f086-483">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="7f086-483">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="7f086-484">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="7f086-484">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="7f086-485">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="7f086-485">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="7f086-486">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="7f086-486">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7f086-487">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="7f086-487">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f086-488">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7f086-488">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7f086-489">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7f086-489">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f086-490">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="7f086-490">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="7f086-491">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="7f086-491">State of the logical device.</span></span> <span data-ttu-id="7f086-492">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 (nicht zutreffend) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7f086-492">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="7f086-493">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7f086-493">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7f086-494">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="7f086-494">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7f086-495">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="7f086-495">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="7f086-496">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="7f086-496">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="7f086-497">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="7f086-497">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="7f086-498">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="7f086-498">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7f086-499">**Synchronisieren**</span><span class="sxs-lookup"><span data-stu-id="7f086-499">**Synch**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f086-500">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7f086-500">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7f086-501">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7f086-501">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f086-502">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| MouseSynchIn100ns"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("100 nanoseconds")</span><span class="sxs-lookup"><span data-stu-id="7f086-502">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|MouseSynchIn100ns"), [**Units**](../wmisdk/standard-qualifiers.md) ("100 nanoseconds")</span></span>
</dt> </dl>

<span data-ttu-id="7f086-503">Die Zeitspanne, nach der der nächste Interruptzeit angenommen wird, dass der Start eines neuen gerätepakets angegeben wird (Teil Pakete werden verworfen).</span><span class="sxs-lookup"><span data-stu-id="7f086-503">Length of time after which the next interrupt is assumed to indicate the start of a new device packet (partial packets are discarded).</span></span> <span data-ttu-id="7f086-504">Wenn eine Unterbrechung verloren geht, kann der Gerätetreiber auf diese Weise die interne Darstellung des Paketstatus mit dem Hardware Status synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="7f086-504">In the event that an interrupt is lost, this allows the pointing device driver to synchronize its internal representation of the packet state with the hardware state.</span></span>

</dd> <dt>

<span data-ttu-id="7f086-505">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="7f086-505">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f086-506">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7f086-506">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f086-507">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7f086-507">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f086-508">Qualifizierer [**: weiter**](../wmisdk/standard-qualifiers.md) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="7f086-508">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="7f086-509">Der Wert der Eigenschaft " **kreationclassname** " des Bereichs Computers.</span><span class="sxs-lookup"><span data-stu-id="7f086-509">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="7f086-510">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7f086-510">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f086-511">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="7f086-511">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f086-512">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7f086-512">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f086-513">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7f086-513">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f086-514">Qualifizierer [**: weiter**](../wmisdk/standard-qualifiers.md) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="7f086-514">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="7f086-515">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="7f086-515">Name of the scoping system.</span></span>

<span data-ttu-id="7f086-516">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7f086-516">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7f086-517">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7f086-517">Remarks</span></span>

<span data-ttu-id="7f086-518">Die **Win32 \_ pointingdevice** -Klasse wird von [**CIM \_ pointingdevice**](cim-pointingdevice.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="7f086-518">The **Win32\_PointingDevice** class is derived from [**CIM\_PointingDevice**](cim-pointingdevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7f086-519">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7f086-519">Requirements</span></span>



| <span data-ttu-id="7f086-520">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7f086-520">Requirement</span></span> | <span data-ttu-id="7f086-521">Wert</span><span class="sxs-lookup"><span data-stu-id="7f086-521">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f086-522">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7f086-522">Minimum supported client</span></span><br/> | <span data-ttu-id="7f086-523">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7f086-523">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7f086-524">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7f086-524">Minimum supported server</span></span><br/> | <span data-ttu-id="7f086-525">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7f086-525">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7f086-526">Namespace</span><span class="sxs-lookup"><span data-stu-id="7f086-526">Namespace</span></span><br/>                | <span data-ttu-id="7f086-527">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7f086-527">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7f086-528">MOF</span><span class="sxs-lookup"><span data-stu-id="7f086-528">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7f086-529"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7f086-529"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7f086-530">DLL</span><span class="sxs-lookup"><span data-stu-id="7f086-530">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f086-531"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f086-531"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f086-532">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7f086-532">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f086-533">**CIM- \_ pointingdevice**</span><span class="sxs-lookup"><span data-stu-id="7f086-533">**CIM\_PointingDevice**</span></span>](cim-pointingdevice.md)
</dt> <dt>

[<span data-ttu-id="7f086-534">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="7f086-534">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
