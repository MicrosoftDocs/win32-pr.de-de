---
description: Die Win32 \_ SerialPort-WMI-Klasse stellt einen seriellen Anschluss auf einem Computersystem dar, auf dem Windows ausgeführt wird.
ms.assetid: f2e5cc5a-a12b-4079-92e1-6bb62fe797a0
ms.tgt_platform: multiple
title: Win32_SerialPort-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SerialPort
- Win32_SerialPort.Reset
- Win32_SerialPort.SetPowerState
- Win32_SerialPort.Availability
- Win32_SerialPort.Binary
- Win32_SerialPort.Capabilities
- Win32_SerialPort.CapabilityDescriptions
- Win32_SerialPort.Caption
- Win32_SerialPort.ConfigManagerErrorCode
- Win32_SerialPort.ConfigManagerUserConfig
- Win32_SerialPort.CreationClassName
- Win32_SerialPort.Description
- Win32_SerialPort.DeviceID
- Win32_SerialPort.ErrorCleared
- Win32_SerialPort.ErrorDescription
- Win32_SerialPort.InstallDate
- Win32_SerialPort.LastErrorCode
- Win32_SerialPort.MaxBaudRate
- Win32_SerialPort.MaximumInputBufferSize
- Win32_SerialPort.MaximumOutputBufferSize
- Win32_SerialPort.MaxNumberControlled
- Win32_SerialPort.Name
- Win32_SerialPort.OSAutoDiscovered
- Win32_SerialPort.PNPDeviceID
- Win32_SerialPort.PowerManagementCapabilities
- Win32_SerialPort.PowerManagementSupported
- Win32_SerialPort.ProtocolSupported
- Win32_SerialPort.ProviderType
- Win32_SerialPort.SettableBaudRate
- Win32_SerialPort.SettableDataBits
- Win32_SerialPort.SettableFlowControl
- Win32_SerialPort.SettableParity
- Win32_SerialPort.SettableParityCheck
- Win32_SerialPort.SettableRLSD
- Win32_SerialPort.SettableStopBits
- Win32_SerialPort.Status
- Win32_SerialPort.StatusInfo
- Win32_SerialPort.Supports16BitMode
- Win32_SerialPort.SupportsDTRDSR
- Win32_SerialPort.SupportsElapsedTimeouts
- Win32_SerialPort.SupportsIntTimeouts
- Win32_SerialPort.SupportsParityCheck
- Win32_SerialPort.SupportsRLSD
- Win32_SerialPort.SupportsRTSCTS
- Win32_SerialPort.SupportsSpecialCharacters
- Win32_SerialPort.SupportsXOnXOff
- Win32_SerialPort.SupportsXOnXOffSet
- Win32_SerialPort.SystemCreationClassName
- Win32_SerialPort.SystemName
- Win32_SerialPort.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b7fc2f25bc88d880ba9b10f10b5efde284a62624
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125989"
---
# <a name="win32_serialport-class"></a><span data-ttu-id="74001-103">Win32- \_ SerialPort-Klasse</span><span class="sxs-lookup"><span data-stu-id="74001-103">Win32\_SerialPort class</span></span>

<span data-ttu-id="74001-104">Die **Win32 \_ SerialPort** - [WMI-Klasse](../wmisdk/retrieving-a-class.md) stellt einen seriellen Anschluss auf einem Computersystem dar, auf dem Windows ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="74001-104">The **Win32\_SerialPort** [WMI class](../wmisdk/retrieving-a-class.md) represents a serial port on a computer system running Windows.</span></span>

<span data-ttu-id="74001-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="74001-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="74001-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="74001-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="74001-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="74001-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4BF-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SerialPort : CIM_SerialController
{
  uint16   Availability;
  boolean  Binary;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint32   MaxBaudRate;
  uint32   MaximumInputBufferSize;
  uint32   MaximumOutputBufferSize;
  uint32   MaxNumberControlled;
  string   Name;
  boolean  OSAutoDiscovered;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   ProtocolSupported;
  string   ProviderType;
  boolean  SettableBaudRate;
  boolean  SettableDataBits;
  boolean  SettableFlowControl;
  boolean  SettableParity;
  boolean  SettableParityCheck;
  boolean  SettableRLSD;
  boolean  SettableStopBits;
  string   Status;
  uint16   StatusInfo;
  boolean  Supports16BitMode;
  boolean  SupportsDTRDSR;
  boolean  SupportsElapsedTimeouts;
  boolean  SupportsIntTimeouts;
  boolean  SupportsParityCheck;
  boolean  SupportsRLSD;
  boolean  SupportsRTSCTS;
  boolean  SupportsSpecialCharacters;
  boolean  SupportsXOnXOff;
  boolean  SupportsXOnXOffSet;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
};
```

## <a name="members"></a><span data-ttu-id="74001-108">Member</span><span class="sxs-lookup"><span data-stu-id="74001-108">Members</span></span>

<span data-ttu-id="74001-109">Die **Win32- \_ SerialPort** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="74001-109">The **Win32\_SerialPort** class has these types of members:</span></span>

-   [<span data-ttu-id="74001-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="74001-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="74001-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="74001-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="74001-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="74001-112">Methods</span></span>

<span data-ttu-id="74001-113">Die **Win32- \_ SerialPort** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="74001-113">The **Win32\_SerialPort** class has these methods.</span></span>



| <span data-ttu-id="74001-114">Methode</span><span class="sxs-lookup"><span data-stu-id="74001-114">Method</span></span>            | <span data-ttu-id="74001-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="74001-115">Description</span></span>                                                                                                                                                                                          |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74001-116">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="74001-116">**Reset**</span></span>         | <span data-ttu-id="74001-117">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="74001-117">Not implemented.</span></span> <span data-ttu-id="74001-118">Informationen zur Implementierung dieser Methode finden Sie unter der [**Reset**](reset-method-in-class-cim-controller.md) -Methode in [**CIM \_ SerialController**](cim-serialcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="74001-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_SerialController**](cim-serialcontroller.md).</span></span><br/>                 |
| <span data-ttu-id="74001-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="74001-119">**SetPowerState**</span></span> | <span data-ttu-id="74001-120">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="74001-120">Not implemented.</span></span> <span data-ttu-id="74001-121">Informationen zur Implementierung dieser Methode finden Sie unter der [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode in [**CIM \_ SerialController**](cim-serialcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="74001-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_SerialController**](cim-serialcontroller.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="74001-122">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="74001-122">Properties</span></span>

<span data-ttu-id="74001-123">Die **Win32- \_ SerialPort** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="74001-123">The **Win32\_SerialPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="74001-124">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="74001-124">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74001-125">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="74001-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="74001-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74001-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74001-127">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="74001-127">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="74001-128">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="74001-128">Availability and status of the device.</span></span>

<span data-ttu-id="74001-129">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="74001-129">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="74001-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="74001-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="74001-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="74001-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="74001-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="74001-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="74001-133">Ausführung oder vollständiger Stromversorgung</span><span class="sxs-lookup"><span data-stu-id="74001-133">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="74001-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="74001-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="74001-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="74001-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="74001-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="74001-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="74001-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="74001-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="74001-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="74001-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="74001-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="74001-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="74001-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="74001-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="74001-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="74001-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="74001-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="74001-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="74001-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="74001-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="74001-144">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="74001-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="74001-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="74001-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="74001-146">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="74001-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="74001-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="74001-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="74001-148">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb gebracht werden.</span><span class="sxs-lookup"><span data-stu-id="74001-148">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="74001-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="74001-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="74001-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="74001-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="74001-151">Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="74001-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="74001-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="74001-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="74001-153">Das Gerät wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="74001-153">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="74001-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="74001-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="74001-155">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="74001-155">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="74001-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="74001-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="74001-157">Das Gerät ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="74001-157">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="74001-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="74001-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="74001-159">Das Gerät ist in Ruhe.</span><span class="sxs-lookup"><span data-stu-id="74001-159">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="74001-160">**Binär (Binary)**</span><span class="sxs-lookup"><span data-stu-id="74001-160">**Binary**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74001-161">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="74001-161">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74001-162">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74001-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74001-163">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| sbinary")</span><span class="sxs-lookup"><span data-stu-id="74001-163">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fBinary")</span></span>
</dt> </dl>

<span data-ttu-id="74001-164">**True** gibt an, dass der serielle Port für die binäre Datenübertragung konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="74001-164">If **TRUE**, the serial port is configured for binary data transfer.</span></span> <span data-ttu-id="74001-165">Da die Windows-API keine Übertragungen im nicht binären Modus unterstützt, muss diese Eigenschaft den Wert " **true**" aufweisen.</span><span class="sxs-lookup"><span data-stu-id="74001-165">Because the Windows API does not support nonbinary mode transfers, this property must be **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="74001-166">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="74001-166">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74001-167">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="74001-167">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="74001-168">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74001-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74001-169">Qualifizierer: [**arrayType**](../wmisdk/standard-qualifiers.md) ("indiziert"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| serielle Ports \| 004,7 "), [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ SerialController**](cim-serialcontroller.md)".**Capabilitybeschreibungen**")</span><span class="sxs-lookup"><span data-stu-id="74001-169">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Serial Ports\|004.7"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_SerialController**](cim-serialcontroller.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="74001-170">Array von Kompatibilitäts auf Chip Ebene für den seriellen Controller.</span><span class="sxs-lookup"><span data-stu-id="74001-170">Array of chip-level compatibility for the serial controller.</span></span> <span data-ttu-id="74001-171">Diese Eigenschaft beschreibt die Pufferung und andere Funktionen des seriellen Controllers, die möglicherweise in der Chip Hardware enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="74001-171">This property describes the buffering and other capabilities of the serial controller that may be inherent in the chip hardware.</span></span> <span data-ttu-id="74001-172">Die-Eigenschaft ist eine enumerierte Ganzzahl.</span><span class="sxs-lookup"><span data-stu-id="74001-172">The property is an enumerated integer.</span></span>

<span data-ttu-id="74001-173">Diese Eigenschaft wird von [**CIM \_ SerialController**](cim-serialcontroller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="74001-173">This property is inherited from [**CIM\_SerialController**](cim-serialcontroller.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="74001-174">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="74001-174">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="74001-175">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="74001-175">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="XT_AT_Compatible"></span><span id="xt_at_compatible"></span><span id="XT_AT_COMPATIBLE"></span>

<span data-ttu-id="74001-176">**XT/kompatibel** (3)</span><span class="sxs-lookup"><span data-stu-id="74001-176">**XT/AT Compatible** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="16450_Compatible"></span><span id="16450_compatible"></span><span id="16450_COMPATIBLE"></span>

<span data-ttu-id="74001-177">**16450 kompatibel** (4)</span><span class="sxs-lookup"><span data-stu-id="74001-177">**16450 Compatible** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="16550_Compatible"></span><span id="16550_compatible"></span><span id="16550_COMPATIBLE"></span>

<span data-ttu-id="74001-178">**16550 kompatibel** (5)</span><span class="sxs-lookup"><span data-stu-id="74001-178">**16550 Compatible** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="16550A_Compatible"></span><span id="16550a_compatible"></span><span id="16550A_COMPATIBLE"></span>

<span data-ttu-id="74001-179">**16550kompatibel** (6)</span><span class="sxs-lookup"><span data-stu-id="74001-179">**16550A Compatible** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="8251_Compatible"></span><span id="8251_compatible"></span><span id="8251_COMPATIBLE"></span>

<span data-ttu-id="74001-180">**8251 kompatibel** (160)</span><span class="sxs-lookup"><span data-stu-id="74001-180">**8251 Compatible** (160)</span></span>


</dt> <dd></dd> <dt>

<span id="8251FIFO_Compatible"></span><span id="8251fifo_compatible"></span><span id="8251FIFO_COMPATIBLE"></span>

<span data-ttu-id="74001-181">**8251FIFO-kompatibel** (161)</span><span class="sxs-lookup"><span data-stu-id="74001-181">**8251FIFO Compatible** (161)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="74001-182">**Capabilitybeschreibungen**</span><span class="sxs-lookup"><span data-stu-id="74001-182">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74001-183">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="74001-183">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="74001-184">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74001-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74001-185">Qualifizierer: [**arrayType**](../wmisdk/standard-qualifiers.md) ("indiziert"), [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ SerialController**](cim-serialcontroller.md).**Funktionen**")</span><span class="sxs-lookup"><span data-stu-id="74001-185">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_SerialController**](cim-serialcontroller.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="74001-186">Ein Array von frei Handzeichen folgen, das Ausführlichere Erläuterungen zu allen seriellen Controller Features bereitstellt, die im **Funktions Array angegeben** sind.</span><span class="sxs-lookup"><span data-stu-id="74001-186">Array of free-form strings providing more detailed explanations for any of the serial controller features indicated in the **Capabilities** array.</span></span> <span data-ttu-id="74001-187">Beachten Sie, dass jeder Eintrag dieses Arrays mit dem Eintrag im **Funktions Array verknüpft ist, der sich** am selben Index befindet.</span><span class="sxs-lookup"><span data-stu-id="74001-187">Note, each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

<span data-ttu-id="74001-188">Diese Eigenschaft wird von [**CIM \_ SerialController**](cim-serialcontroller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="74001-188">This property is inherited from [**CIM\_SerialController**](cim-serialcontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="74001-189">**Caption**</span><span class="sxs-lookup"><span data-stu-id="74001-189">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74001-190">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="74001-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74001-191">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74001-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74001-192">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="74001-192">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="74001-193">Kurze Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="74001-193">Short description of the object.</span></span>

<span data-ttu-id="74001-194">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="74001-194">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="74001-195">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="74001-195">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74001-196">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74001-196">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74001-197">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74001-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74001-198">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="74001-198">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="74001-199">Win32-Configuration Manager Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="74001-199">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="74001-200">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="74001-200">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="74001-201"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="74001-201"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="74001-202"> (0)</span><span class="sxs-lookup"><span data-stu-id="74001-202">(0)</span></span>


</dt> <dd>

<span data-ttu-id="74001-203">Das Gerät funktioniert ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="74001-203">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="74001-204"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="74001-204"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="74001-205">(1)</span><span class="sxs-lookup"><span data-stu-id="74001-205">(1)</span></span>


</dt> <dd>

<span data-ttu-id="74001-206">Das Gerät ist nicht ordnungsgemäß konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="74001-206">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="74001-207"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="74001-207"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="74001-208">(2)</span><span class="sxs-lookup"><span data-stu-id="74001-208">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="74001-209"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="74001-209"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="74001-210">(3)</span><span class="sxs-lookup"><span data-stu-id="74001-210">(3)</span></span>


</dt> <dd>

<span data-ttu-id="74001-211">Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt möglicherweise nicht über genügend Arbeitsspeicher oder andere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="74001-211">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="74001-212"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="74001-212"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="74001-213">(4)</span><span class="sxs-lookup"><span data-stu-id="74001-213">(4)</span></span>


</dt> <dd>

<span data-ttu-id="74001-214">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="74001-214">Device is not working properly.</span></span> <span data-ttu-id="74001-215">Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="74001-215">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="74001-216"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="74001-216"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="74001-217">(5)</span><span class="sxs-lookup"><span data-stu-id="74001-217">(5)</span></span>


</dt> <dd>

<span data-ttu-id="74001-218">Der Treiber für das Gerät erfordert eine Ressource, die von Windows nicht verwaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="74001-218">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="74001-219"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="74001-219"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="74001-220"> (6)</span><span class="sxs-lookup"><span data-stu-id="74001-220">(6)</span></span>


</dt> <dd>

<span data-ttu-id="74001-221">Die Startkonfiguration für das Gerät steht in Konflikt mit anderen Geräten.</span><span class="sxs-lookup"><span data-stu-id="74001-221">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="74001-222"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="74001-222"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="74001-223">(7)</span><span class="sxs-lookup"><span data-stu-id="74001-223">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="74001-224"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="74001-224"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="74001-225">(8)</span><span class="sxs-lookup"><span data-stu-id="74001-225">(8)</span></span>


</dt> <dd>

<span data-ttu-id="74001-226">Das Treiber Lade Modul für das Gerät fehlt.</span><span class="sxs-lookup"><span data-stu-id="74001-226">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="74001-227"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="74001-227"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="74001-228">(9)</span><span class="sxs-lookup"><span data-stu-id="74001-228">(9)</span></span>


</dt> <dd>

<span data-ttu-id="74001-229">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="74001-229">Device is not working properly.</span></span> <span data-ttu-id="74001-230">Die Steuerungs Firmware meldet nicht korrekt die Ressourcen für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="74001-230">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="74001-231"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="74001-231"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="74001-232">(10)</span><span class="sxs-lookup"><span data-stu-id="74001-232">(10)</span></span>


</dt> <dd>

<span data-ttu-id="74001-233">Das Gerät kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="74001-233">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="74001-234"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="74001-234"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="74001-235">(11)</span><span class="sxs-lookup"><span data-stu-id="74001-235">(11)</span></span>


</dt> <dd>

<span data-ttu-id="74001-236">Fehler beim Gerät.</span><span class="sxs-lookup"><span data-stu-id="74001-236">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="74001-237"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="74001-237"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="74001-238">(12)</span><span class="sxs-lookup"><span data-stu-id="74001-238">(12)</span></span>


</dt> <dd>

<span data-ttu-id="74001-239">Das Gerät kann nicht genug freie Ressourcen für die Verwendung finden.</span><span class="sxs-lookup"><span data-stu-id="74001-239">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="74001-240"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="74001-240"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="74001-241">(13)</span><span class="sxs-lookup"><span data-stu-id="74001-241">(13)</span></span>


</dt> <dd>

<span data-ttu-id="74001-242">Die Geräte Ressourcen können nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="74001-242">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="74001-243"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="74001-243"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="74001-244">(14)</span><span class="sxs-lookup"><span data-stu-id="74001-244">(14)</span></span>


</dt> <dd>

<span data-ttu-id="74001-245">Das Gerät kann erst ordnungsgemäß funktionieren, wenn der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="74001-245">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="74001-246"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="74001-246"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="74001-247">(15)</span><span class="sxs-lookup"><span data-stu-id="74001-247">(15)</span></span>


</dt> <dd>

<span data-ttu-id="74001-248">Das Gerät funktioniert aufgrund eines möglichen erneuten Aufzählungs Problems nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="74001-248">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="74001-249"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="74001-249"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="74001-250">(16)</span><span class="sxs-lookup"><span data-stu-id="74001-250">(16)</span></span>


</dt> <dd>

<span data-ttu-id="74001-251">In Windows können nicht alle Ressourcen identifiziert werden, die vom Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="74001-251">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="74001-252"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="74001-252"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="74001-253">(17)</span><span class="sxs-lookup"><span data-stu-id="74001-253">(17)</span></span>


</dt> <dd>

<span data-ttu-id="74001-254">Das Gerät fordert einen unbekannten Ressourcentyp an.</span><span class="sxs-lookup"><span data-stu-id="74001-254">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="74001-255"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="74001-255"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="74001-256">(18)</span><span class="sxs-lookup"><span data-stu-id="74001-256">(18)</span></span>


</dt> <dd>

<span data-ttu-id="74001-257">Gerätetreiber müssen neu installiert werden.</span><span class="sxs-lookup"><span data-stu-id="74001-257">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="74001-258"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="74001-258"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="74001-259">(19)</span><span class="sxs-lookup"><span data-stu-id="74001-259">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="74001-260"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="74001-260"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="74001-261">(20)</span><span class="sxs-lookup"><span data-stu-id="74001-261">(20)</span></span>


</dt> <dd>

<span data-ttu-id="74001-262">Die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="74001-262">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="74001-263"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="74001-263"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="74001-264">(21)</span><span class="sxs-lookup"><span data-stu-id="74001-264">(21)</span></span>


</dt> <dd>

<span data-ttu-id="74001-265">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="74001-265">System failure.</span></span> <span data-ttu-id="74001-266">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="74001-266">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="74001-267">Das Gerät wird von Windows entfernt.</span><span class="sxs-lookup"><span data-stu-id="74001-267">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="74001-268"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="74001-268"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="74001-269">(22)</span><span class="sxs-lookup"><span data-stu-id="74001-269">(22)</span></span>


</dt> <dd>

<span data-ttu-id="74001-270">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="74001-270">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="74001-271"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="74001-271"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="74001-272">(23)</span><span class="sxs-lookup"><span data-stu-id="74001-272">(23)</span></span>


</dt> <dd>

<span data-ttu-id="74001-273">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="74001-273">System failure.</span></span> <span data-ttu-id="74001-274">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="74001-274">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="74001-275"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="74001-275"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="74001-276">(24)</span><span class="sxs-lookup"><span data-stu-id="74001-276">(24)</span></span>


</dt> <dd>

<span data-ttu-id="74001-277">Das Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.</span><span class="sxs-lookup"><span data-stu-id="74001-277">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="74001-278"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="74001-278"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="74001-279">(25)</span><span class="sxs-lookup"><span data-stu-id="74001-279">(25)</span></span>


</dt> <dd>

<span data-ttu-id="74001-280">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="74001-280">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="74001-281"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="74001-281"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="74001-282">(26)</span><span class="sxs-lookup"><span data-stu-id="74001-282">(26)</span></span>


</dt> <dd>

<span data-ttu-id="74001-283">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="74001-283">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="74001-284"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="74001-284"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="74001-285">(27)</span><span class="sxs-lookup"><span data-stu-id="74001-285">(27)</span></span>


</dt> <dd>

<span data-ttu-id="74001-286">Das Gerät verfügt nicht über eine gültige Protokoll Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="74001-286">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="74001-287"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="74001-287"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="74001-288">(28)</span><span class="sxs-lookup"><span data-stu-id="74001-288">(28)</span></span>


</dt> <dd>

<span data-ttu-id="74001-289">Gerätetreiber sind nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="74001-289">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="74001-290"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="74001-290"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="74001-291">(29)</span><span class="sxs-lookup"><span data-stu-id="74001-291">(29)</span></span>


</dt> <dd>

<span data-ttu-id="74001-292">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="74001-292">Device is disabled.</span></span> <span data-ttu-id="74001-293">Die Gerätefirmware hat nicht die erforderlichen Ressourcen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="74001-293">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="74001-294"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="74001-294"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="74001-295">(30)</span><span class="sxs-lookup"><span data-stu-id="74001-295">(30)</span></span>


</dt> <dd>

<span data-ttu-id="74001-296">Das Gerät verwendet eine UNQ-Ressource, die von einem anderen Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="74001-296">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="74001-297"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="74001-297"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="74001-298">31,5</span><span class="sxs-lookup"><span data-stu-id="74001-298">(31)</span></span>


</dt> <dd>

<span data-ttu-id="74001-299">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="74001-299">Device is not working properly.</span></span> <span data-ttu-id="74001-300">Die erforderlichen Gerätetreiber können nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="74001-300">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="74001-301">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="74001-301">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74001-302">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="74001-302">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74001-303">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74001-303">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74001-304">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="74001-304">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="74001-305">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="74001-305">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="74001-306">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="74001-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="74001-307">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="74001-307">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74001-308">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="74001-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74001-309">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74001-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74001-310">Qualifizierer: [ **CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="74001-310">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="74001-311">Der Name der ersten konkreten Klasse, die in der Vererbungs Kette angezeigt werden soll, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="74001-311">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="74001-312">Bei Verwendung mit den anderen Schlüsseleigenschaften der-Klasse ermöglicht die-Eigenschaft, dass alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="74001-312">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="74001-313">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="74001-313">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="74001-314">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="74001-314">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74001-315">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="74001-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74001-316">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74001-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74001-317">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="74001-317">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="74001-318">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="74001-318">Description of the object.</span></span>

<span data-ttu-id="74001-319">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="74001-319">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="74001-320">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="74001-320">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74001-321">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="74001-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74001-322">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74001-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74001-323">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("DeviceID"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| \\ \\ hardcemap \\ \\ SerialComm")</span><span class="sxs-lookup"><span data-stu-id="74001-323">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Hardware\\\\DeviceMap\\\\SerialComm")</span></span>
</dt> </dl>

<span data-ttu-id="74001-324">Eindeutiger Bezeichner des seriellen Anschlusses mit anderen Geräten im System.</span><span class="sxs-lookup"><span data-stu-id="74001-324">Unique identifier of the serial port with other devices on the system.</span></span>

<span data-ttu-id="74001-325">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="74001-325">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="74001-326">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="74001-326">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74001-327">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="74001-327">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74001-328">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74001-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74001-329">**True** gibt an, dass der in **LastErrorCode** gemeldete Fehler jetzt gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="74001-329">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="74001-330">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="74001-330">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="74001-331">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="74001-331">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74001-332">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="74001-332">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74001-333">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74001-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74001-334">Eine frei Form Zeichenfolge, die weitere Informationen über den in **LastErrorCode** aufgezeichneten Fehler sowie Informationen zu eventuell durchzuführenden Korrekturmaßnahmen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="74001-334">Free-form string supplying more information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="74001-335">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="74001-335">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="74001-336">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="74001-336">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74001-337">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="74001-337">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="74001-338">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74001-338">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74001-339">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="74001-339">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="74001-340">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="74001-340">Date and time the object was installed.</span></span> <span data-ttu-id="74001-341">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="74001-341">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="74001-342">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="74001-342">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="74001-343">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="74001-343">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74001-344">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74001-344">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74001-345">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74001-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74001-346">Der letzte vom logischen Gerät gemeldete Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="74001-346">Last error code reported by the logical device.</span></span>

<span data-ttu-id="74001-347">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="74001-347">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="74001-348">**Maxbaudrate**</span><span class="sxs-lookup"><span data-stu-id="74001-348">**MaxBaudRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74001-349">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74001-349">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74001-350">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74001-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74001-351">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| serielle Ports \| 004,6 "), [**Einheiten**](../wmisdk/standard-qualifiers.md) (" Bits pro Sekunde ")</span><span class="sxs-lookup"><span data-stu-id="74001-351">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Serial Ports\|004.6"), [**Units**](../wmisdk/standard-qualifiers.md) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="74001-352">Maximale Baudrate (in Bits pro Sekunde), die vom seriellen Controller unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="74001-352">Maximum baud rate (in bits per second) supported by the serial controller.</span></span>

<span data-ttu-id="74001-353">Diese Eigenschaft wird von [**CIM \_ SerialController**](cim-serialcontroller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="74001-353">This property is inherited from [**CIM\_SerialController**](cim-serialcontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="74001-354">**MaximumInputBufferSize**</span><span class="sxs-lookup"><span data-stu-id="74001-354">**MaximumInputBufferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74001-355">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74001-355">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74001-356">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74001-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74001-357">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**commprop**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwmaxrxqueue"), [**Units**](../wmisdk/standard-qualifiers.md) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="74001-357">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwMaxRxQueue"), [**units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="74001-358">Maximale Größe des internen Eingabe Puffers des seriellen Anschluss Treibers.</span><span class="sxs-lookup"><span data-stu-id="74001-358">Maximum size of the serial port driver's internal input buffer.</span></span> <span data-ttu-id="74001-359">Der Wert 0 (null) gibt an, dass der serielle Anbieter keinen maximalen Wert festgelegt hat.</span><span class="sxs-lookup"><span data-stu-id="74001-359">A value of 0 (zero) indicates that no maximum value is imposed by the serial provider.</span></span>

</dd> <dt>

<span data-ttu-id="74001-360">**Maximumoutputbuffersize**</span><span class="sxs-lookup"><span data-stu-id="74001-360">**MaximumOutputBufferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74001-361">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74001-361">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74001-362">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74001-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74001-363">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**commprop**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwmaxtxqueue"), [**Units**](../wmisdk/standard-qualifiers.md) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="74001-363">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwMaxTxQueue"), [**units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="74001-364">Maximale Größe des internen Ausgabepuffers des seriellen Anschluss Treibers.</span><span class="sxs-lookup"><span data-stu-id="74001-364">Maximum size of the serial port driver's internal output buffer.</span></span> <span data-ttu-id="74001-365">Der Wert 0 (null) gibt an, dass der serielle Anbieter keinen maximalen Wert festgelegt hat.</span><span class="sxs-lookup"><span data-stu-id="74001-365">A value of 0 (zero) indicates that no maximum value is imposed by the serial provider.</span></span>

</dd> <dt>

<span data-ttu-id="74001-366">**Maxnuma**</span><span class="sxs-lookup"><span data-stu-id="74001-366">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74001-367">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74001-367">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74001-368">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74001-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74001-369">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| Bus Port \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="74001-369">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="74001-370">Maximale Anzahl direkt Adressier barer Entitäten, die von diesem Controller unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="74001-370">Maximum number of directly addressable entities supportable by this controller.</span></span> <span data-ttu-id="74001-371">Wenn die Zahl unbekannt ist, sollte ein Wert von 0 (null) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="74001-371">A value of 0 (zero) should be used if the number is unknown.</span></span>

<span data-ttu-id="74001-372">Diese Eigenschaft wird vom [**CIM- \_ Controller**](cim-controller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="74001-372">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="74001-373">**Name**</span><span class="sxs-lookup"><span data-stu-id="74001-373">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74001-374">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="74001-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74001-375">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74001-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74001-376">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="74001-376">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="74001-377">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="74001-377">Label by which the object is known.</span></span> <span data-ttu-id="74001-378">Bei einer Unterklasse kann die Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="74001-378">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="74001-379">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="74001-379">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="74001-380">**Osauum erkannt**</span><span class="sxs-lookup"><span data-stu-id="74001-380">**OSAutoDiscovered**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74001-381">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="74001-381">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74001-382">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74001-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74001-383">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Hardware \\ \\ Description \\ \\ System \\ \\ multifunctionadapter")</span><span class="sxs-lookup"><span data-stu-id="74001-383">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HARDWARE\\\\DESCRIPTION\\\\SYSTEM\\\\MultifunctionAdapter")</span></span>
</dt> </dl>

<span data-ttu-id="74001-384">**True** gibt an, dass die Instanzen dieser Klasse vom Betriebssystem automatisch erkannt wurden.</span><span class="sxs-lookup"><span data-stu-id="74001-384">If **TRUE**, the instances of this class were automatically discovered by the operating system.</span></span> <span data-ttu-id="74001-385">Wenn z. b. Hardware über die Systemsteuerung hinzugefügt wurde, findet das Betriebssystem Instanzen dieser Klasse, indem die Hardware von den Instanzen dieser Klasse abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="74001-385">If, for example, hardware was added through Control Panel, the operating system finds instances of this class by querying hardware from the instances of this class.</span></span>

</dd> <dt>

<span data-ttu-id="74001-386">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="74001-386">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74001-387">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="74001-387">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74001-388">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74001-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74001-389">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="74001-389">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="74001-390">Windows Plug & Play Geräte Bezeichner des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="74001-390">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="74001-391">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="74001-391">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="74001-392">Beispiel: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="74001-392">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="74001-393">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="74001-393">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74001-394">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="74001-394">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="74001-395">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74001-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74001-396">Array der spezifischen energiebezogenen Funktionen eines logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="74001-396">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="74001-397">Diese Eigenschaft wird von **CIM \_ LogicalDevice** geerbt.</span><span class="sxs-lookup"><span data-stu-id="74001-397">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="74001-398"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="74001-398"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="74001-399"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="74001-399"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="74001-400"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="74001-400"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="74001-401"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="74001-401"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="74001-402">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="74001-402">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="74001-403"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="74001-403"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="74001-404">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="74001-404">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="74001-405"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="74001-405"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="74001-406">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="74001-406">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="74001-407">Diese Methode wird in der übergeordneten **CIM \_ LogicalDevice** -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="74001-407">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="74001-408">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="74001-408">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="74001-409"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="74001-409"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="74001-410">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="74001-410">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="74001-411"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="74001-411"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="74001-412">Zeitgesteuerte Power-On unterstützt</span><span class="sxs-lookup"><span data-stu-id="74001-412">Timed Power-On Supported</span></span>

<span data-ttu-id="74001-413">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) und die *Uhrzeit* auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="74001-413">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="74001-414">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="74001-414">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74001-415">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="74001-415">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74001-416">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74001-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74001-417">Wenn der Wert **true** ist, kann das Gerät Energie gesteuert werden (kann in den Unterbrechungs Modus versetzt werden usw.).</span><span class="sxs-lookup"><span data-stu-id="74001-417">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="74001-418">Die-Eigenschaft gibt nicht an, dass die Energie Verwaltungsfunktionen zurzeit aktiviert sind, sondern nur, dass das logische Gerät für die Energie Verwaltung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="74001-418">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="74001-419">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="74001-419">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="74001-420">**Protocolsupported**</span><span class="sxs-lookup"><span data-stu-id="74001-420">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74001-421">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="74001-421">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="74001-422">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74001-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74001-423">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| Bus Port \| 001,2 "," MIF. DMTF-Datenträger \| \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="74001-423">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="74001-424">Protokoll, das vom Controller für den Zugriff auf "gesteuerte" Geräte verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="74001-424">Protocol used by the controller to access "controlled" devices.</span></span>

<span data-ttu-id="74001-425">Diese Eigenschaft wird vom [**CIM- \_ Controller**](cim-controller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="74001-425">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span> <span data-ttu-id="74001-426">In der folgenden Liste werden die möglichen Werte angezeigt.</span><span class="sxs-lookup"><span data-stu-id="74001-426">The following list shows the possible values.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="74001-427"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="74001-427"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="74001-428"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="74001-428"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="74001-429"><span id="EISA"></span><span id="eisa"></span>**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="74001-429"><span id="EISA"></span><span id="eisa"></span>**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="74001-430"><span id="ISA"></span><span id="isa"></span>**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="74001-430"><span id="ISA"></span><span id="isa"></span>**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="74001-431"><span id="PCI"></span><span id="pci"></span>**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="74001-431"><span id="PCI"></span><span id="pci"></span>**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="74001-432"><span id="ATA_ATAPI"></span><span id="ata_atapi"></span>**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="74001-432"><span id="ATA_ATAPI"></span><span id="ata_atapi"></span>**ATA/ATAPI** (6)</span></span>


</dt> <dd>

<span data-ttu-id="74001-433">ATA oder ATAPI</span><span class="sxs-lookup"><span data-stu-id="74001-433">ATA or ATAPI</span></span>

</dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="74001-434"><span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>**Flexible Diskette** (7)</span><span class="sxs-lookup"><span data-stu-id="74001-434"><span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="74001-435"><span id="1496"></span>**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="74001-435"><span id="1496"></span>**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="74001-436"><span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>**SCSI Parallel Interface** (9)</span><span class="sxs-lookup"><span data-stu-id="74001-436"><span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="74001-437"><span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>**SCSI-Fibre Channel Protokoll** (10)</span><span class="sxs-lookup"><span data-stu-id="74001-437"><span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="74001-438"><span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>**SCSI-serielle Busprotokoll** (11)</span><span class="sxs-lookup"><span data-stu-id="74001-438"><span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="74001-439"><span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>**SCSI-serielle Busprotokoll-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="74001-439"><span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="74001-440"><span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>**Architektur des SCSI-seriellen Speichers** (13)</span><span class="sxs-lookup"><span data-stu-id="74001-440"><span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="74001-441"><span id="VESA"></span><span id="vesa"></span>**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="74001-441"><span id="VESA"></span><span id="vesa"></span>**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="74001-442"><span id="PCMCIA"></span><span id="pcmcia"></span>**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="74001-442"><span id="PCMCIA"></span><span id="pcmcia"></span>**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="74001-443"><span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>**Universeller seribus** (16)</span><span class="sxs-lookup"><span data-stu-id="74001-443"><span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="74001-444"><span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>**Paralleles Protokoll** (17)</span><span class="sxs-lookup"><span data-stu-id="74001-444"><span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="74001-445"><span id="ESCON"></span><span id="escon"></span>**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="74001-445"><span id="ESCON"></span><span id="escon"></span>**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="74001-446"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnose** (19)</span><span class="sxs-lookup"><span data-stu-id="74001-446"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="74001-447"><span id="I2C"></span><span id="i2c"></span>**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="74001-447"><span id="I2C"></span><span id="i2c"></span>**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="74001-448"><span id="Power"></span><span id="power"></span><span id="POWER"></span>**Stromversorgung** (21)</span><span class="sxs-lookup"><span data-stu-id="74001-448"><span id="Power"></span><span id="power"></span><span id="POWER"></span>**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="74001-449"><span id="HIPPI"></span><span id="hippi"></span>**HIPPI** (22)</span><span class="sxs-lookup"><span data-stu-id="74001-449"><span id="HIPPI"></span><span id="hippi"></span>**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="74001-450"><span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>**Multibus** (23)</span><span class="sxs-lookup"><span data-stu-id="74001-450"><span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="74001-451"><span id="VME"></span><span id="vme"></span>**VME** (24)</span><span class="sxs-lookup"><span data-stu-id="74001-451"><span id="VME"></span><span id="vme"></span>**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="74001-452"><span id="IPI"></span><span id="ipi"></span>**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="74001-452"><span id="IPI"></span><span id="ipi"></span>**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="74001-453"><span id="IEEE-488"></span><span id="ieee-488"></span>**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="74001-453"><span id="IEEE-488"></span><span id="ieee-488"></span>**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="74001-454"><span id="RS232"></span><span id="rs232"></span>**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="74001-454"><span id="RS232"></span><span id="rs232"></span>**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="74001-455"><span id="ieee_802.3_10base5"></span>**IEEE 802,3 10BASE5** (28)</span><span class="sxs-lookup"><span data-stu-id="74001-455"><span id="ieee_802.3_10base5"></span>**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="74001-456"><span id="ieee_802.3_10base2"></span>**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="74001-456"><span id="ieee_802.3_10base2"></span>**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="74001-457"><span id="ieee_802.3_1base5"></span>**IEEE 802,3 1base5** (30)</span><span class="sxs-lookup"><span data-stu-id="74001-457"><span id="ieee_802.3_1base5"></span>**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="74001-458"><span id="ieee_802.3_10broad36"></span>**IEEE 802,3 10Broad36** (31)</span><span class="sxs-lookup"><span data-stu-id="74001-458"><span id="ieee_802.3_10broad36"></span>**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="74001-459"><span id="ieee_802.3_100basevg"></span>**IEEE 802,3 100BaseVG** (32)</span><span class="sxs-lookup"><span data-stu-id="74001-459"><span id="ieee_802.3_100basevg"></span>**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="74001-460"><span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>**IEEE 802,5-TokenRing** (33)</span><span class="sxs-lookup"><span data-stu-id="74001-460"><span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="74001-461"><span id="ansi_x3t9.5_fddi"></span>**ANSI x3t 9,5, f** (34)</span><span class="sxs-lookup"><span data-stu-id="74001-461"><span id="ansi_x3t9.5_fddi"></span>**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="74001-462"><span id="MCA"></span><span id="mca"></span>**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="74001-462"><span id="MCA"></span><span id="mca"></span>**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="74001-463"><span id="ESDI"></span><span id="esdi"></span>**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="74001-463"><span id="ESDI"></span><span id="esdi"></span>**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="74001-464"><span id="IDE"></span><span id="ide"></span>**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="74001-464"><span id="IDE"></span><span id="ide"></span>**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="74001-465"><span id="CMD"></span><span id="cmd"></span>**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="74001-465"><span id="CMD"></span><span id="cmd"></span>**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="74001-466"><span id="ST506"></span><span id="st506"></span>**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="74001-466"><span id="ST506"></span><span id="st506"></span>**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="74001-467"><span id="DSSI"></span><span id="dssi"></span>**Dssi** (40)</span><span class="sxs-lookup"><span data-stu-id="74001-467"><span id="DSSI"></span><span id="dssi"></span>**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="74001-468"><span id="QIC2"></span><span id="qic2"></span>**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="74001-468"><span id="QIC2"></span><span id="qic2"></span>**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="74001-469"><span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>**Erweiterte ATA/IDE** (42)</span><span class="sxs-lookup"><span data-stu-id="74001-469"><span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="74001-470"><span id="AGP"></span><span id="agp"></span>**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="74001-470"><span id="AGP"></span><span id="agp"></span>**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="74001-471"><span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>**TWIRP (** bidirektionale Infrarot) (44)</span><span class="sxs-lookup"><span data-stu-id="74001-471"><span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="74001-472"><span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>**FIR (schnelles Infrarot)** (45)</span><span class="sxs-lookup"><span data-stu-id="74001-472"><span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="74001-473"><span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>**Sir (serielle Infrarot)** (46)</span><span class="sxs-lookup"><span data-stu-id="74001-473"><span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="74001-474"><span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>" **Iran** " (47)</span><span class="sxs-lookup"><span data-stu-id="74001-474"><span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="74001-475">**ProviderType**</span><span class="sxs-lookup"><span data-stu-id="74001-475">**ProviderType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74001-476">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="74001-476">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74001-477">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74001-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74001-478">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**commprop**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwprovsubtype")</span><span class="sxs-lookup"><span data-stu-id="74001-478">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvSubType")</span></span>
</dt> </dl>

<span data-ttu-id="74001-479">Der Typ des Kommunikations Anbieters.</span><span class="sxs-lookup"><span data-stu-id="74001-479">Communications provider type.</span></span>

<span data-ttu-id="74001-480">Die Werte sind:</span><span class="sxs-lookup"><span data-stu-id="74001-480">The values are:</span></span>

<dl> <dd><span data-ttu-id="74001-481">"Faxgerät"</span><span class="sxs-lookup"><span data-stu-id="74001-481">"FAX Device"</span></span></dd> <dd><span data-ttu-id="74001-482">"Lat-Protokoll"</span><span class="sxs-lookup"><span data-stu-id="74001-482">"LAT Protocol"</span></span></dd> <dd><span data-ttu-id="74001-483">"Modem Gerät"</span><span class="sxs-lookup"><span data-stu-id="74001-483">"Modem Device"</span></span></dd> <dd><span data-ttu-id="74001-484">"Netzwerk Brücke"</span><span class="sxs-lookup"><span data-stu-id="74001-484">"Network Bridge"</span></span></dd> <dd><span data-ttu-id="74001-485">"Paralleler Port"</span><span class="sxs-lookup"><span data-stu-id="74001-485">"Parallel Port"</span></span></dd> <dd><span data-ttu-id="74001-486">"Der serielle anschlussport"</span><span class="sxs-lookup"><span data-stu-id="74001-486">"RS232 Serial Port"</span></span></dd> <dd><span data-ttu-id="74001-487">"RS422-Port"</span><span class="sxs-lookup"><span data-stu-id="74001-487">"RS422 Port"</span></span></dd> <dd><span data-ttu-id="74001-488">"RS423-Port"</span><span class="sxs-lookup"><span data-stu-id="74001-488">"RS423 Port"</span></span></dd> <dd><span data-ttu-id="74001-489">"RS449-Port"</span><span class="sxs-lookup"><span data-stu-id="74001-489">"RS449 Port"</span></span></dd> <dd><span data-ttu-id="74001-490">"Scanner-Gerät"</span><span class="sxs-lookup"><span data-stu-id="74001-490">"Scanner Device"</span></span></dd> <dd><span data-ttu-id="74001-491">"TCP/IP Telnet"</span><span class="sxs-lookup"><span data-stu-id="74001-491">"TCP/IP TelNet"</span></span></dd> <dd><span data-ttu-id="74001-492">"X. 25"</span><span class="sxs-lookup"><span data-stu-id="74001-492">"X.25"</span></span></dd> <dd><span data-ttu-id="74001-493">Nicht angegeben</span><span class="sxs-lookup"><span data-stu-id="74001-493">"Unspecified"</span></span></dd> </dl>

<dt>

<span id="FAX_Device"></span><span id="fax_device"></span><span id="FAX_DEVICE"></span>

<span data-ttu-id="74001-494">**Faxgerät** ("Faxgerät")</span><span class="sxs-lookup"><span data-stu-id="74001-494">**FAX Device** ("FAX Device")</span></span>


</dt> <dd></dd> <dt>

<span id="LAT_Protocol"></span><span id="lat_protocol"></span><span id="LAT_PROTOCOL"></span>

<span data-ttu-id="74001-495">**Lat-Protokoll** ("lat-Protokoll")</span><span class="sxs-lookup"><span data-stu-id="74001-495">**LAT Protocol** ("LAT Protocol")</span></span>


</dt> <dd></dd> <dt>

<span id="Modem_Device"></span><span id="modem_device"></span><span id="MODEM_DEVICE"></span>

<span data-ttu-id="74001-496">**Modem Gerät** ("Modem Gerät")</span><span class="sxs-lookup"><span data-stu-id="74001-496">**Modem Device** ("Modem Device")</span></span>


</dt> <dd></dd> <dt>

<span id="Network_Bridge"></span><span id="network_bridge"></span><span id="NETWORK_BRIDGE"></span>

<span data-ttu-id="74001-497">**Netzwerk Brücke** ("Netzwerk Brücke")</span><span class="sxs-lookup"><span data-stu-id="74001-497">**Network Bridge** ("Network Bridge")</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>

<span data-ttu-id="74001-498">**Paralleler Anschluss** ("paralleler Port")</span><span class="sxs-lookup"><span data-stu-id="74001-498">**Parallel Port** ("Parallel Port")</span></span>


</dt> <dd></dd> <dt>

<span id="RS232_Serial_Port"></span><span id="rs232_serial_port"></span><span id="RS232_SERIAL_PORT"></span>

<span data-ttu-id="74001-499">Gleicher **seriellen Anschluss** ("RS232 Serial Port")</span><span class="sxs-lookup"><span data-stu-id="74001-499">**RS232 Serial Port** ("RS232 Serial Port")</span></span>


</dt> <dd></dd> <dt>

<span id="RS422_Port"></span><span id="rs422_port"></span><span id="RS422_PORT"></span>

<span data-ttu-id="74001-500">**RS422-Port** ("RS422-Port")</span><span class="sxs-lookup"><span data-stu-id="74001-500">**RS422 Port** ("RS422 Port")</span></span>


</dt> <dd></dd> <dt>

<span id="RS423_Port"></span><span id="rs423_port"></span><span id="RS423_PORT"></span>

<span data-ttu-id="74001-501">**RS423-Port** ("RS423-Port")</span><span class="sxs-lookup"><span data-stu-id="74001-501">**RS423 Port** ("RS423 Port")</span></span>


</dt> <dd></dd> <dt>

<span id="RS449_Port"></span><span id="rs449_port"></span><span id="RS449_PORT"></span>

<span data-ttu-id="74001-502">**RS449-Port** ("RS449-Port")</span><span class="sxs-lookup"><span data-stu-id="74001-502">**RS449 Port** ("RS449 Port")</span></span>


</dt> <dd></dd> <dt>

<span id="Scanner_Device"></span><span id="scanner_device"></span><span id="SCANNER_DEVICE"></span>

<span data-ttu-id="74001-503">**Scannergerät** ("Scanner-Gerät")</span><span class="sxs-lookup"><span data-stu-id="74001-503">**Scanner Device** ("Scanner Device")</span></span>


</dt> <dd></dd> <dt>

<span id="TCP_IP_TelNet"></span><span id="tcp_ip_telnet"></span><span id="TCP_IP_TELNET"></span>

<span data-ttu-id="74001-504">**TCP/IP Telnet** ("TCP/IP Telnet")</span><span class="sxs-lookup"><span data-stu-id="74001-504">**TCP/IP TelNet** ("TCP/IP TelNet")</span></span>


</dt> <dd></dd> <dt>

<span id="X.25"></span><span id="x.25"></span>

<span data-ttu-id="74001-505">**X. 25** ("x. 25")</span><span class="sxs-lookup"><span data-stu-id="74001-505">**X.25** ("X.25")</span></span>


</dt> <dd></dd> <dt>

<span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span>

<span data-ttu-id="74001-506">**Nicht angegeben** ("nicht angegeben")</span><span class="sxs-lookup"><span data-stu-id="74001-506">**Unspecified** ("Unspecified")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="74001-507">**SettableBaudRate**</span><span class="sxs-lookup"><span data-stu-id="74001-507">**SettableBaudRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74001-508">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="74001-508">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74001-509">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74001-509">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74001-510">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**commprop**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwsettableparametriams \| SP \_ Baud")</span><span class="sxs-lookup"><span data-stu-id="74001-510">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwSettableParams\|SP\_BAUD")</span></span>
</dt> </dl>

<span data-ttu-id="74001-511">**True** gibt an, dass die Baudrate für diesen seriellen Anschluss geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="74001-511">If **TRUE**, the baud rate can be changed for this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="74001-512">**Settabledatabits**</span><span class="sxs-lookup"><span data-stu-id="74001-512">**SettableDataBits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74001-513">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="74001-513">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74001-514">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74001-514">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74001-515">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**commprop**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwsettableparametriams \| SP \_ DataBits")</span><span class="sxs-lookup"><span data-stu-id="74001-515">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwSettableParams\|SP\_DATABITS")</span></span>
</dt> </dl>

<span data-ttu-id="74001-516">**True** gibt an, dass Datenbits für diesen seriellen Anschluss festgelegt werden können.</span><span class="sxs-lookup"><span data-stu-id="74001-516">If **TRUE**, data bits can be set for this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="74001-517">**SettableFlowControl**</span><span class="sxs-lookup"><span data-stu-id="74001-517">**SettableFlowControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74001-518">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="74001-518">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74001-519">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74001-519">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74001-520">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**commprop**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwsettableparametriams \| SP \_ Handshake")</span><span class="sxs-lookup"><span data-stu-id="74001-520">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwSettableParams\|SP\_HANDSHAKING")</span></span>
</dt> </dl>

<span data-ttu-id="74001-521">**True** gibt an, dass die Fluss Steuerung für diesen seriellen Anschluss festgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="74001-521">If **TRUE**, flow control can be set for this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="74001-522">**SettableParity**</span><span class="sxs-lookup"><span data-stu-id="74001-522">**SettableParity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74001-523">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="74001-523">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74001-524">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74001-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74001-525">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**commprop**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwsettableparams \| SP \_ Parität")</span><span class="sxs-lookup"><span data-stu-id="74001-525">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwSettableParams\|SP\_PARITY")</span></span>
</dt> </dl>

<span data-ttu-id="74001-526">**True** gibt an, dass die Parität für diesen seriellen Anschluss festgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="74001-526">If **TRUE**, parity can be set for this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="74001-527">**Settableparameitycheck**</span><span class="sxs-lookup"><span data-stu-id="74001-527">**SettableParityCheck**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74001-528">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="74001-528">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74001-529">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74001-529">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74001-530">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**commprop**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwsettableparams \| SP \_ Parität \_ Check")</span><span class="sxs-lookup"><span data-stu-id="74001-530">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwSettableParams\|SP\_PARITY\_CHECK")</span></span>
</dt> </dl>

<span data-ttu-id="74001-531">**True** gibt an, dass die Paritäts Überprüfung für diesen seriellen Anschluss festgelegt werden kann (wenn die Paritäts Überprüfung unterstützt wird).</span><span class="sxs-lookup"><span data-stu-id="74001-531">If **TRUE**, parity checking can be set for this serial port (if parity checking is supported).</span></span>

</dd> <dt>

<span data-ttu-id="74001-532">**Settablerlsd**</span><span class="sxs-lookup"><span data-stu-id="74001-532">**SettableRLSD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74001-533">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="74001-533">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74001-534">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74001-534">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74001-535">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**commprop**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwsettableparametriams \| SP \_ RLSD")</span><span class="sxs-lookup"><span data-stu-id="74001-535">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwSettableParams\|SP\_RLSD")</span></span>
</dt> </dl>

<span data-ttu-id="74001-536">**True** gibt an, dass die empfangene Zeilen Signal Erkennung (RLSD) für diesen seriellen Anschluss festgelegt werden kann (wenn "RLSD" unterstützt wird).</span><span class="sxs-lookup"><span data-stu-id="74001-536">If **TRUE**, Received Line Signal Detect (RLSD) can be set for this serial port (if RLSD is supported).</span></span>

</dd> <dt>

<span data-ttu-id="74001-537">**SettableStopBits**</span><span class="sxs-lookup"><span data-stu-id="74001-537">**SettableStopBits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74001-538">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="74001-538">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74001-539">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74001-539">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74001-540">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**commprop**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwsettablebiams \| SP \_ Stopbits")</span><span class="sxs-lookup"><span data-stu-id="74001-540">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwSettableParams\|SP\_STOPBITS")</span></span>
</dt> </dl>

<span data-ttu-id="74001-541">**True** gibt an, dass Stoppbits für diesen seriellen Anschluss festgelegt werden können.</span><span class="sxs-lookup"><span data-stu-id="74001-541">If **TRUE**, stop bits can be set for this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="74001-542">**Status**</span><span class="sxs-lookup"><span data-stu-id="74001-542">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74001-543">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="74001-543">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74001-544">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74001-544">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74001-545">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="74001-545">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="74001-546">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="74001-546">Current status of the object.</span></span> <span data-ttu-id="74001-547">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="74001-547">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="74001-548">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="74001-548">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="74001-549">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="74001-549">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="74001-550">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="74001-550">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="74001-551">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="74001-551">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="74001-552">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="74001-552">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="74001-553">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="74001-553">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="74001-554">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="74001-554">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="74001-555">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="74001-555">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="74001-556">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="74001-556">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="74001-557">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="74001-557">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="74001-558">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="74001-558">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="74001-559">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="74001-559">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="74001-560">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="74001-560">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="74001-561">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="74001-561">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="74001-562">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="74001-562">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="74001-563">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="74001-563">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="74001-564">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="74001-564">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="74001-565">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="74001-565">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="74001-566">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="74001-566">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74001-567">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="74001-567">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="74001-568">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74001-568">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74001-569">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="74001-569">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="74001-570">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="74001-570">State of the logical device.</span></span> <span data-ttu-id="74001-571">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 (nicht zutreffend) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="74001-571">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="74001-572">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="74001-572">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="74001-573">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="74001-573">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="74001-574">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="74001-574">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="74001-575">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="74001-575">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="74001-576">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="74001-576">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="74001-577">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="74001-577">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="74001-578">**Supports16BitMode**</span><span class="sxs-lookup"><span data-stu-id="74001-578">**Supports16BitMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74001-579">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="74001-579">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74001-580">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74001-580">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74001-581">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**commprop**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwprovfunktionalitäten \| PCF \_ 16bitmode")</span><span class="sxs-lookup"><span data-stu-id="74001-581">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_16BITMODE")</span></span>
</dt> </dl>

<span data-ttu-id="74001-582">**True** gibt an, dass der 16-Bit-Modus auf diesem seriellen Anschluss unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="74001-582">If **TRUE**, 16-bit mode is supported on this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="74001-583">**Supportsdtrdsr**</span><span class="sxs-lookup"><span data-stu-id="74001-583">**SupportsDTRDSR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74001-584">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="74001-584">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74001-585">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74001-585">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74001-586">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**commprop**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwprovfunktionalitäten \| PCF \_ dtrdsr")</span><span class="sxs-lookup"><span data-stu-id="74001-586">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_DTRDSR")</span></span>
</dt> </dl>

<span data-ttu-id="74001-587">**True** gibt an, dass Data Terminal Ready (DTR)-und DSR-Signale (Data Set Ready) auf diesem seriellen Port unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="74001-587">If **TRUE**, data terminal ready (DTR) and data set ready (DSR) signals are supported on this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="74001-588">**Supportselapsedtimeouts**</span><span class="sxs-lookup"><span data-stu-id="74001-588">**SupportsElapsedTimeouts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74001-589">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="74001-589">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74001-590">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74001-590">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74001-591">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**commprop**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwprovfunktionalitäten \| PCF \_ totaltimeouts")</span><span class="sxs-lookup"><span data-stu-id="74001-591">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_TOTALTIMEOUTS")</span></span>
</dt> </dl>

<span data-ttu-id="74001-592">**True** gibt an, dass abgelaufene Timeouts auf diesem seriellen Port unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="74001-592">If **TRUE**, elapsed time-outs are supported on this serial port.</span></span> <span data-ttu-id="74001-593">Verstrichene Timeouts verfolgen den Gesamtzeitraum zwischen Datenübertragungen.</span><span class="sxs-lookup"><span data-stu-id="74001-593">Elapsed timeouts track the total amount of time between data transmissions.</span></span>

</dd> <dt>

<span data-ttu-id="74001-594">**SupportsIntTimeouts**</span><span class="sxs-lookup"><span data-stu-id="74001-594">**SupportsIntTimeouts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74001-595">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="74001-595">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74001-596">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74001-596">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74001-597">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**commprop**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwprovfunktionalitäten \| PCF \_ inttimeouts")</span><span class="sxs-lookup"><span data-stu-id="74001-597">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_INTTIMEOUTS")</span></span>
</dt> </dl>

<span data-ttu-id="74001-598">**True** gibt an, dass Intervall Timeouts unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="74001-598">If **TRUE**, interval time-outs are supported.</span></span> <span data-ttu-id="74001-599">Ein Intervall Timeout ist die Zeitspanne, die zwischen dem Eintreffen der einzelnen Daten Daten verlaufen werden darf.</span><span class="sxs-lookup"><span data-stu-id="74001-599">An interval timeout is the amount of time allowed to elapse between the arrival of each piece of data.</span></span>

</dd> <dt>

<span data-ttu-id="74001-600">**SupportsParityCheck**</span><span class="sxs-lookup"><span data-stu-id="74001-600">**SupportsParityCheck**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74001-601">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="74001-601">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74001-602">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74001-602">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74001-603">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**commprop**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwprovfunktionalitäten \| PCF \_ Parity \_ Check")</span><span class="sxs-lookup"><span data-stu-id="74001-603">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_PARITY\_CHECK")</span></span>
</dt> </dl>

<span data-ttu-id="74001-604">**True** gibt an, dass die Paritäts Überprüfung auf diesem seriellen Anschluss unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="74001-604">If **TRUE**, parity checking is supported on this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="74001-605">**SupportsRLSD**</span><span class="sxs-lookup"><span data-stu-id="74001-605">**SupportsRLSD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74001-606">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="74001-606">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74001-607">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74001-607">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74001-608">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**commprop**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwprovfunktionalitäten \| PCF \_ RLSD")</span><span class="sxs-lookup"><span data-stu-id="74001-608">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_RLSD")</span></span>
</dt> </dl>

<span data-ttu-id="74001-609">**True** gibt an, dass die empfangene Zeilen Signal Erkennung (RLSD) auf diesem seriellen Port unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="74001-609">If **TRUE**, Received Line Signal Detect (RLSD) is supported on this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="74001-610">**SupportsRTSCTS**</span><span class="sxs-lookup"><span data-stu-id="74001-610">**SupportsRTSCTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74001-611">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="74001-611">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74001-612">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74001-612">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74001-613">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**commprop**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwprovfunktionalitäten \| PCF \_ RTSCTS")</span><span class="sxs-lookup"><span data-stu-id="74001-613">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_RTSCTS")</span></span>
</dt> </dl>

<span data-ttu-id="74001-614">Wenn " **true**", werden die Signale "bereit zum Senden" (RTS) und "Clear to Send (CTS)" auf diesem seriellen Port unterstützt.</span><span class="sxs-lookup"><span data-stu-id="74001-614">If **TRUE**, ready to send (RTS) and clear to send (CTS) signals are supported on this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="74001-615">**SupportsSpecialCharacters**</span><span class="sxs-lookup"><span data-stu-id="74001-615">**SupportsSpecialCharacters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74001-616">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="74001-616">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74001-617">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74001-617">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74001-618">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**commprop**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwprovfunktionalitäten \| PCF \_ SpecialChars")</span><span class="sxs-lookup"><span data-stu-id="74001-618">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_SPECIALCHARS")</span></span>
</dt> </dl>

<span data-ttu-id="74001-619">**True** gibt an, dass serielle Port Steuerzeichen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="74001-619">If **TRUE**, serial port control characters are supported.</span></span> <span data-ttu-id="74001-620">Diese Zeichen signalisieren Ereignisse anstelle von Daten.</span><span class="sxs-lookup"><span data-stu-id="74001-620">These characters signal events rather than data.</span></span> <span data-ttu-id="74001-621">Diese Zeichen können nicht angezeigt werden und vom Treiber festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="74001-621">These characters are not displayable and are set by the driver.</span></span> <span data-ttu-id="74001-622">Dazu zählen EOF Char, ErrorChar, BreakChar, EventChar, XonChar und XoffChar.</span><span class="sxs-lookup"><span data-stu-id="74001-622">They include EofChar, ErrorChar, BreakChar, EventChar, XonChar, and XoffChar.</span></span>

</dd> <dt>

<span data-ttu-id="74001-623">**SupportsXOnXOff**</span><span class="sxs-lookup"><span data-stu-id="74001-623">**SupportsXOnXOff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74001-624">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="74001-624">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74001-625">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74001-625">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74001-626">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**commprop**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwprovfunktionalitäten \| PCF \_ XOnXOff")</span><span class="sxs-lookup"><span data-stu-id="74001-626">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_XONXOFF")</span></span>
</dt> </dl>

<span data-ttu-id="74001-627">**True** gibt an, dass die Fluss Steuerung von XOn oder XOFF auf diesem seriellen Anschluss unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="74001-627">If **TRUE**, XON or XOFF flow-control is supported on this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="74001-628">**Supportsxonxoffset**</span><span class="sxs-lookup"><span data-stu-id="74001-628">**SupportsXOnXOffSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74001-629">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="74001-629">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74001-630">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74001-630">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74001-631">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**commprop**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwprovfunktionalitäten \| PCF \_ setxchar")</span><span class="sxs-lookup"><span data-stu-id="74001-631">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_SETXCHAR")</span></span>
</dt> </dl>

<span data-ttu-id="74001-632">**True** gibt an, dass der Kommunikationsanbieter die Konfiguration der xonor XOFF-Fluss Steuerungs Einstellung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="74001-632">If **TRUE**, the communications provider supports configuration of the XONor XOFF flow-control setting.</span></span>

</dd> <dt>

<span data-ttu-id="74001-633">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="74001-633">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74001-634">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="74001-634">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74001-635">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74001-635">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74001-636">Qualifizierer [**: weiter**](../wmisdk/standard-qualifiers.md) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="74001-636">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="74001-637">Der Wert der Eigenschaft " **kreationclassname** " des Bereichs Computers.</span><span class="sxs-lookup"><span data-stu-id="74001-637">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="74001-638">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="74001-638">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="74001-639">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="74001-639">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74001-640">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="74001-640">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74001-641">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74001-641">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74001-642">Qualifizierer [**: weiter**](../wmisdk/standard-qualifiers.md) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="74001-642">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="74001-643">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="74001-643">Name of the scoping system.</span></span>

<span data-ttu-id="74001-644">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="74001-644">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="74001-645">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="74001-645">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74001-646">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="74001-646">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="74001-647">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74001-647">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74001-648">Datum und Uhrzeit des letzten zurück Setzens des Controllers.</span><span class="sxs-lookup"><span data-stu-id="74001-648">Date and time this controller was last reset.</span></span> <span data-ttu-id="74001-649">Dies könnte bedeuten, dass der Controller heruntergefahren oder erneut initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="74001-649">This could mean the controller was powered down, or reinitialized.</span></span>

<span data-ttu-id="74001-650">Diese Eigenschaft wird vom [**CIM- \_ Controller**](cim-controller.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="74001-650">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="74001-651">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="74001-651">Remarks</span></span>

<span data-ttu-id="74001-652">Die **Win32- \_ SerialPort** -Klasse wird von [**CIM \_ SerialController**](cim-serialcontroller.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="74001-652">The **Win32\_SerialPort** class is derived from [**CIM\_SerialController**](cim-serialcontroller.md).</span></span>

## <a name="examples"></a><span data-ttu-id="74001-653">Beispiele</span><span class="sxs-lookup"><span data-stu-id="74001-653">Examples</span></span>

<span data-ttu-id="74001-654">Eine alternative Methode zum Abrufen von Informationen zum seriellen Anschluss (aus der Registrierung) finden Sie im Beispiel zum [Aufzählen von Ports](https://Gallery.TechNet.Microsoft.Com/scriptcenter/087b4d73-4a5e-4746-b365-ad682911360e) Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="74001-654">For an alternate method of retrieving serial port information (from the registry), see the [Enumerate Ports](https://Gallery.TechNet.Microsoft.Com/scriptcenter/087b4d73-4a5e-4746-b365-ad682911360e) Visual Basic sample.</span></span>

<span data-ttu-id="74001-655">Das PowerShell-Beispiel " [Eigenschaften von seriellen Anschluss auflisten](https://Gallery.TechNet.Microsoft.Com/42ff8eab-7d2b-4549-b178-835daecf4f12) " gibt Informationen zu den seriellen Anschlüssen zurück, die auf einem Computer installiert sind.</span><span class="sxs-lookup"><span data-stu-id="74001-655">The [List Serial Port Properties](https://Gallery.TechNet.Microsoft.Com/42ff8eab-7d2b-4549-b178-835daecf4f12) PowerShell example returns information about the serial ports installed on a computer.</span></span>

<span data-ttu-id="74001-656">Im folgenden VBScript-Beispiel werden Informationen zu den auf einem Computer installierten seriellen Anschlüssen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="74001-656">The following VBScript sample returns information about the serial ports installed on a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery("Select * from Win32_SerialPort") 
 
For Each objItem in colItems 
    Wscript.Echo "Binary: " & objItem.Binary 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Device ID: " & objItem.DeviceID 
    Wscript.Echo "Maximum Baud Rate: " & objItem.MaxBaudRate 
    Wscript.Echo "Maximum Input Buffer Size: " & objItem.MaximumInputBufferSize 
    Wscript.Echo "Maximum Output Buffer Size: " & _ 
        objItem.MaximumOutputBufferSize 
    Wscript.Echo "Name: " & objItem.Name 
    Wscript.Echo "OS Auto Discovered: " & objItem.OSAutoDiscovered 
    Wscript.Echo "PNP Device ID: " & objItem.PNPDeviceID 
    Wscript.Echo "Provider Type: " & objItem.ProviderType 
    Wscript.Echo "Settable Baud Rate: " & objItem.SettableBaudRate 
    Wscript.Echo "Settable Data Bits: " & objItem.SettableDataBits 
    Wscript.Echo "Settable Flow Control: " & objItem.SettableFlowControl 
    Wscript.Echo "Settable Parity: " & objItem.SettableParity 
    Wscript.Echo "Settable Parity Check: " & objItem.SettableParityCheck 
    Wscript.Echo "Settable RLSD: " & objItem.SettableRLSD 
    Wscript.Echo "Settable Stop Bits: " & objItem.SettableStopBits 
    Wscript.Echo "Supports 16-Bit Mode: " & objItem.Supports16BitMode 
    Wscript.Echo "Supports DTRDSR: " & objItem.SupportsDTRDSR 
    Wscript.Echo "Supports Elapsed Timeouts: " & _ 
        objItem.SupportsElapsedTimeouts 
    Wscript.Echo "Supports Int Timeouts: " & objItem.SupportsIntTimeouts 
    Wscript.Echo "Supports Parity Check: " & objItem.SupportsParityCheck 
    Wscript.Echo "Supports RLSD: " & objItem.SupportsRLSD 
    Wscript.Echo "Supports RTSCTS: " & objItem.SupportsRTSCTS 
    Wscript.Echo "Supports Special Characters: " & _ 
        objItem.SupportsSpecialCharacters 
    Wscript.Echo "Supports XOn XOff: " & objItem.SupportsXOnXOff 
    Wscript.Echo "Supports XOn XOff Setting: " & objItem.SupportsXOnXOffSet 
Next
```



## <a name="requirements"></a><span data-ttu-id="74001-657">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="74001-657">Requirements</span></span>



| <span data-ttu-id="74001-658">Anforderung</span><span class="sxs-lookup"><span data-stu-id="74001-658">Requirement</span></span> | <span data-ttu-id="74001-659">Wert</span><span class="sxs-lookup"><span data-stu-id="74001-659">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="74001-660">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="74001-660">Minimum supported client</span></span><br/> | <span data-ttu-id="74001-661">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="74001-661">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="74001-662">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="74001-662">Minimum supported server</span></span><br/> | <span data-ttu-id="74001-663">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="74001-663">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="74001-664">Namespace</span><span class="sxs-lookup"><span data-stu-id="74001-664">Namespace</span></span><br/>                | <span data-ttu-id="74001-665">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="74001-665">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="74001-666">MOF</span><span class="sxs-lookup"><span data-stu-id="74001-666">MOF</span></span><br/>                      | <dl> <span data-ttu-id="74001-667"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="74001-667"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="74001-668">DLL</span><span class="sxs-lookup"><span data-stu-id="74001-668">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74001-669"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74001-669"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74001-670">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="74001-670">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74001-671">**CIM- \_ SerialController**</span><span class="sxs-lookup"><span data-stu-id="74001-671">**CIM\_SerialController**</span></span>](cim-serialcontroller.md)
</dt> <dt>

[<span data-ttu-id="74001-672">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="74001-672">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
