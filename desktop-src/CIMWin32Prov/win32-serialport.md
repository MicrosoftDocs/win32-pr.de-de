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
# <a name="win32_serialport-class"></a>Win32- \_ SerialPort-Klasse

Die **Win32 \_ SerialPort** - [WMI-Klasse](../wmisdk/retrieving-a-class.md) stellt einen seriellen Anschluss auf einem Computersystem dar, auf dem Windows ausgeführt wird.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

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

## <a name="members"></a>Member

Die **Win32- \_ SerialPort** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32- \_ SerialPort** -Klasse verfügt über diese Methoden.



| Methode            | BESCHREIBUNG                                                                                                                                                                                          |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Zurücksetzen**         | Nicht implementiert. Informationen zur Implementierung dieser Methode finden Sie unter der [**Reset**](reset-method-in-class-cim-controller.md) -Methode in [**CIM \_ SerialController**](cim-serialcontroller.md).<br/>                 |
| **SetPowerState** | Nicht implementiert. Informationen zur Implementierung dieser Methode finden Sie unter der [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode in [**CIM \_ SerialController**](cim-serialcontroller.md).<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **Win32- \_ SerialPort** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Verfügbarkeit**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")
</dt> </dl>

Verfügbarkeit und Status des Geräts.

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)


</dt> <dd>

Ausführung oder vollständiger Stromversorgung

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)


</dt> <dd>

Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)


</dt> <dd>

Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)


</dt> <dd>

Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb gebracht werden.

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)


</dt> <dd>

Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)


</dt> <dd>

Das Gerät wurde angehalten.

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)


</dt> <dd>

Das Gerät ist nicht bereit.

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)


</dt> <dd>

Das Gerät ist nicht konfiguriert.

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )


</dt> <dd>

Das Gerät ist in Ruhe.

</dd> </dl>

</dd> <dt>

**Binär (Binary)**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| sbinary")
</dt> </dl>

**True** gibt an, dass der serielle Port für die binäre Datenübertragung konfiguriert ist. Da die Windows-API keine Übertragungen im nicht binären Modus unterstützt, muss diese Eigenschaft den Wert " **true**" aufweisen.

</dd> <dt>

**Capabilities**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**arrayType**](../wmisdk/standard-qualifiers.md) ("indiziert"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| serielle Ports \| 004,7 "), [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ SerialController**](cim-serialcontroller.md)".**Capabilitybeschreibungen**")
</dt> </dl>

Array von Kompatibilitäts auf Chip Ebene für den seriellen Controller. Diese Eigenschaft beschreibt die Pufferung und andere Funktionen des seriellen Controllers, die möglicherweise in der Chip Hardware enthalten sind. Die-Eigenschaft ist eine enumerierte Ganzzahl.

Diese Eigenschaft wird von [**CIM \_ SerialController**](cim-serialcontroller.md)geerbt.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (2)


</dt> <dd></dd> <dt>

<span id="XT_AT_Compatible"></span><span id="xt_at_compatible"></span><span id="XT_AT_COMPATIBLE"></span>

**XT/kompatibel** (3)


</dt> <dd></dd> <dt>

<span id="16450_Compatible"></span><span id="16450_compatible"></span><span id="16450_COMPATIBLE"></span>

**16450 kompatibel** (4)


</dt> <dd></dd> <dt>

<span id="16550_Compatible"></span><span id="16550_compatible"></span><span id="16550_COMPATIBLE"></span>

**16550 kompatibel** (5)


</dt> <dd></dd> <dt>

<span id="16550A_Compatible"></span><span id="16550a_compatible"></span><span id="16550A_COMPATIBLE"></span>

**16550kompatibel** (6)


</dt> <dd></dd> <dt>

<span id="8251_Compatible"></span><span id="8251_compatible"></span><span id="8251_COMPATIBLE"></span>

**8251 kompatibel** (160)


</dt> <dd></dd> <dt>

<span id="8251FIFO_Compatible"></span><span id="8251fifo_compatible"></span><span id="8251FIFO_COMPATIBLE"></span>

**8251FIFO-kompatibel** (161)


</dt> <dd></dd> </dl>

</dd> <dt>

**Capabilitybeschreibungen**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**arrayType**](../wmisdk/standard-qualifiers.md) ("indiziert"), [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ SerialController**](cim-serialcontroller.md).**Funktionen**")
</dt> </dl>

Ein Array von frei Handzeichen folgen, das Ausführlichere Erläuterungen zu allen seriellen Controller Features bereitstellt, die im **Funktions Array angegeben** sind. Beachten Sie, dass jeder Eintrag dieses Arrays mit dem Eintrag im **Funktions Array verknüpft ist, der sich** am selben Index befindet.

Diese Eigenschaft wird von [**CIM \_ SerialController**](cim-serialcontroller.md)geerbt.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Kurze Beschreibung des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**Configmanagererrorcode**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")
</dt> </dl>

Win32-Configuration Manager Fehlercode.

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Dieses Gerät funktioniert ordnungsgemäß.**  (0)


</dt> <dd>

Das Gerät funktioniert ordnungsgemäß.

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.** (1)


</dt> <dd>

Das Gerät ist nicht ordnungsgemäß konfiguriert.

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Der Treiber für dieses Gerät kann nicht geladen werden.** (2)


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.** (3)


</dt> <dd>

Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt möglicherweise nicht über genügend Arbeitsspeicher oder andere Ressourcen.

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.** (4)


</dt> <dd>

Das Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.** (5)


</dt> <dd>

Der Treiber für das Gerät erfordert eine Ressource, die von Windows nicht verwaltet werden kann.

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**  (6)


</dt> <dd>

Die Startkonfiguration für das Gerät steht in Konflikt mit anderen Geräten.

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Kann nicht gefiltert werden.** (7)


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Das Treiber Lade Modul für das Gerät fehlt.** (8)


</dt> <dd>

Das Treiber Lade Modul für das Gerät fehlt.

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.** (9)


</dt> <dd>

Das Gerät funktioniert nicht ordnungsgemäß. Die Steuerungs Firmware meldet nicht korrekt die Ressourcen für das Gerät.

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Dieses Gerät kann nicht gestartet werden.** (10)


</dt> <dd>

Das Gerät kann nicht gestartet werden.

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Dieses Gerät ist fehlgeschlagen.** (11)


</dt> <dd>

Fehler beim Gerät.

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.** (12)


</dt> <dd>

Das Gerät kann nicht genug freie Ressourcen für die Verwendung finden.

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.** (13)


</dt> <dd>

Die Geräte Ressourcen können nicht überprüft werden.

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.** (14)


</dt> <dd>

Das Gerät kann erst ordnungsgemäß funktionieren, wenn der Computer neu gestartet wird.

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.** (15)


</dt> <dd>

Das Gerät funktioniert aufgrund eines möglichen erneuten Aufzählungs Problems nicht ordnungsgemäß.

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.** (16)


</dt> <dd>

In Windows können nicht alle Ressourcen identifiziert werden, die vom Gerät verwendet werden.

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.** (17)


</dt> <dd>

Das Gerät fordert einen unbekannten Ressourcentyp an.

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Installieren Sie die Treiber für dieses Gerät neu.** (18)


</dt> <dd>

Gerätetreiber müssen neu installiert werden.

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Fehler bei Verwendung des VXD-Lade Moduls.** (19)


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Möglicherweise ist die Registrierung beschädigt.** (20)


</dt> <dd>

Die Registrierung ist möglicherweise beschädigt.

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.** (21)


</dt> <dd>

System Fehler. Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation. Das Gerät wird von Windows entfernt.

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Dieses Gerät ist deaktiviert.** (22)


</dt> <dd>

Das Gerät ist deaktiviert.

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.** (23)


</dt> <dd>

System Fehler. Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.** (24)


</dt> <dd>

Das Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.** (25)


</dt> <dd>

Das Gerät wird weiterhin von Windows eingerichtet.

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.** (26)


</dt> <dd>

Das Gerät wird weiterhin von Windows eingerichtet.

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.** (27)


</dt> <dd>

Das Gerät verfügt nicht über eine gültige Protokoll Konfiguration.

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Die Treiber für dieses Gerät sind nicht installiert.** (28)


</dt> <dd>

Gerätetreiber sind nicht installiert.

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.** (29)


</dt> <dd>

Das Gerät ist deaktiviert. Die Gerätefirmware hat nicht die erforderlichen Ressourcen bereitgestellt.

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.** (30)


</dt> <dd>

Das Gerät verwendet eine UNQ-Ressource, die von einem anderen Gerät verwendet wird.

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.** 31,5


</dt> <dd>

Das Gerät funktioniert nicht ordnungsgemäß. Die erforderlichen Gerätetreiber können nicht geladen werden.

</dd> </dl>

</dd> <dt>

**Configmanageruserconfig**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")
</dt> </dl>

**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.

</dd> <dt>

**"Name der Klassenname"**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Der Name der ersten konkreten Klasse, die in der Vererbungs Kette angezeigt werden soll, die bei der Erstellung einer Instanz verwendet wird. Bei Verwendung mit den anderen Schlüsseleigenschaften der-Klasse ermöglicht die-Eigenschaft, dass alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Description")
</dt> </dl>

Eine Beschreibung des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**DeviceID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("DeviceID"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| \\ \\ hardcemap \\ \\ SerialComm")
</dt> </dl>

Eindeutiger Bezeichner des seriellen Anschlusses mit anderen Geräten im System.

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.

</dd> <dt>

**Errorgelöscht**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True** gibt an, dass der in **LastErrorCode** gemeldete Fehler jetzt gelöscht wird.

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine frei Form Zeichenfolge, die weitere Informationen über den in **LastErrorCode** aufgezeichneten Fehler sowie Informationen zu eventuell durchzuführenden Korrekturmaßnahmen bereitstellt.

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Install Date ")
</dt> </dl>

Datum und Uhrzeit der Installation des-Objekts. Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**LastErrorCode**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der letzte vom logischen Gerät gemeldete Fehlercode.

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.

</dd> <dt>

**Maxbaudrate**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| serielle Ports \| 004,6 "), [**Einheiten**](../wmisdk/standard-qualifiers.md) (" Bits pro Sekunde ")
</dt> </dl>

Maximale Baudrate (in Bits pro Sekunde), die vom seriellen Controller unterstützt werden.

Diese Eigenschaft wird von [**CIM \_ SerialController**](cim-serialcontroller.md)geerbt.

</dd> <dt>

**MaximumInputBufferSize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**commprop**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwmaxrxqueue"), [**Units**](../wmisdk/standard-qualifiers.md) ("Bytes")
</dt> </dl>

Maximale Größe des internen Eingabe Puffers des seriellen Anschluss Treibers. Der Wert 0 (null) gibt an, dass der serielle Anbieter keinen maximalen Wert festgelegt hat.

</dd> <dt>

**Maximumoutputbuffersize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**commprop**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwmaxtxqueue"), [**Units**](../wmisdk/standard-qualifiers.md) ("Bytes")
</dt> </dl>

Maximale Größe des internen Ausgabepuffers des seriellen Anschluss Treibers. Der Wert 0 (null) gibt an, dass der serielle Anbieter keinen maximalen Wert festgelegt hat.

</dd> <dt>

**Maxnuma**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| Bus Port \| 001,9 ")
</dt> </dl>

Maximale Anzahl direkt Adressier barer Entitäten, die von diesem Controller unterstützt werden. Wenn die Zahl unbekannt ist, sollte ein Wert von 0 (null) verwendet werden.

Diese Eigenschaft wird vom [**CIM- \_ Controller**](cim-controller.md)geerbt.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Name")
</dt> </dl>

Die Bezeichnung, nach der das-Objekt bekannt ist. Bei einer Unterklasse kann die Eigenschaft als Schlüsseleigenschaft überschrieben werden.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**Osauum erkannt**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Hardware \\ \\ Description \\ \\ System \\ \\ multifunctionadapter")
</dt> </dl>

**True** gibt an, dass die Instanzen dieser Klasse vom Betriebssystem automatisch erkannt wurden. Wenn z. b. Hardware über die Systemsteuerung hinzugefügt wurde, findet das Betriebssystem Instanzen dieser Klasse, indem die Hardware von den Instanzen dieser Klasse abgefragt wird.

</dd> <dt>

**PNPDeviceID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")
</dt> </dl>

Windows Plug & Play Geräte Bezeichner des logischen Geräts.

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.

Beispiel: " \* PNP030b"

</dd> <dt>

**Powermanagementfunktionen**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Array der spezifischen energiebezogenen Funktionen eines logischen Geräts.

Diese Eigenschaft wird von **CIM \_ LogicalDevice** geerbt.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)


</dt> <dd>

Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)


</dt> <dd>

Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)


</dt> <dd>

Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode wird unterstützt. Diese Methode wird in der übergeordneten **CIM \_ LogicalDevice** -Klasse gefunden und kann implementiert werden. Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)


</dt> <dd>

Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) festgelegt ist.

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)


</dt> <dd>

Zeitgesteuerte Power-On unterstützt

Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) und die *Uhrzeit* auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.

</dd> </dl>

</dd> <dt>

**Powermanagementsupported**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Wenn der Wert **true** ist, kann das Gerät Energie gesteuert werden (kann in den Unterbrechungs Modus versetzt werden usw.). Die-Eigenschaft gibt nicht an, dass die Energie Verwaltungsfunktionen zurzeit aktiviert sind, sondern nur, dass das logische Gerät für die Energie Verwaltung geeignet ist.

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.

</dd> <dt>

**Protocolsupported**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| Bus Port \| 001,2 "," MIF. DMTF-Datenträger \| \| 003,3 ")
</dt> </dl>

Protokoll, das vom Controller für den Zugriff auf "gesteuerte" Geräte verwendet wird.

Diese Eigenschaft wird vom [**CIM- \_ Controller**](cim-controller.md)geerbt. In der folgenden Liste werden die möglichen Werte angezeigt.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span id="EISA"></span><span id="eisa"></span>**EISA** (3)


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span id="ISA"></span><span id="isa"></span>**ISA** (4)


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span id="PCI"></span><span id="pci"></span>**PCI** (5)


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>**ATA/ATAPI** (6)


</dt> <dd>

ATA oder ATAPI

</dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>**Flexible Diskette** (7)


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span id="1496"></span>**1496** (8)


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>**SCSI Parallel Interface** (9)


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>**SCSI-Fibre Channel Protokoll** (10)


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>**SCSI-serielle Busprotokoll** (11)


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>**SCSI-serielle Busprotokoll-2 (1394)** (12)


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>**Architektur des SCSI-seriellen Speichers** (13)


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span id="VESA"></span><span id="vesa"></span>**VESA** (14)


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span id="PCMCIA"></span><span id="pcmcia"></span>**PCMCIA** (15)


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>**Universeller seribus** (16)


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>**Paralleles Protokoll** (17)


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span id="ESCON"></span><span id="escon"></span>**ESCON** (18)


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnose** (19)


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span id="I2C"></span><span id="i2c"></span>**I2C** (20)


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>**Stromversorgung** (21)


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span id="HIPPI"></span><span id="hippi"></span>**HIPPI** (22)


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>**Multibus** (23)


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span id="VME"></span><span id="vme"></span>**VME** (24)


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span id="IPI"></span><span id="ipi"></span>**IPI** (25)


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span id="IEEE-488"></span><span id="ieee-488"></span>**IEEE-488** (26)


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span id="RS232"></span><span id="rs232"></span>**RS232** (27)


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span id="ieee_802.3_10base5"></span>**IEEE 802,3 10BASE5** (28)


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span id="ieee_802.3_10base2"></span>**IEEE 802,3 10Base2** (29)


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span id="ieee_802.3_1base5"></span>**IEEE 802,3 1base5** (30)


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span id="ieee_802.3_10broad36"></span>**IEEE 802,3 10Broad36** (31)


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span id="ieee_802.3_100basevg"></span>**IEEE 802,3 100BaseVG** (32)


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>**IEEE 802,5-TokenRing** (33)


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span id="ansi_x3t9.5_fddi"></span>**ANSI x3t 9,5, f** (34)


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span id="MCA"></span><span id="mca"></span>**MCA** (35)


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span id="ESDI"></span><span id="esdi"></span>**ESDI** (36)


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span id="IDE"></span><span id="ide"></span>**IDE** (37)


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span id="CMD"></span><span id="cmd"></span>**Cmd** (38)


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span id="ST506"></span><span id="st506"></span>**ST506** (39)


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span id="DSSI"></span><span id="dssi"></span>**Dssi** (40)


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span id="QIC2"></span><span id="qic2"></span>**QIC2** (41)


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>**Erweiterte ATA/IDE** (42)


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span id="AGP"></span><span id="agp"></span>**AGP** (43)


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>**TWIRP (** bidirektionale Infrarot) (44)


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>**FIR (schnelles Infrarot)** (45)


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>**Sir (serielle Infrarot)** (46)


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>" **Iran** " (47)


</dt> <dd></dd> </dl>

</dd> <dt>

**ProviderType**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**commprop**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwprovsubtype")
</dt> </dl>

Der Typ des Kommunikations Anbieters.

Die Werte sind:

<dl> <dd>"Faxgerät"</dd> <dd>"Lat-Protokoll"</dd> <dd>"Modem Gerät"</dd> <dd>"Netzwerk Brücke"</dd> <dd>"Paralleler Port"</dd> <dd>"Der serielle anschlussport"</dd> <dd>"RS422-Port"</dd> <dd>"RS423-Port"</dd> <dd>"RS449-Port"</dd> <dd>"Scanner-Gerät"</dd> <dd>"TCP/IP Telnet"</dd> <dd>"X. 25"</dd> <dd>Nicht angegeben</dd> </dl>

<dt>

<span id="FAX_Device"></span><span id="fax_device"></span><span id="FAX_DEVICE"></span>

**Faxgerät** ("Faxgerät")


</dt> <dd></dd> <dt>

<span id="LAT_Protocol"></span><span id="lat_protocol"></span><span id="LAT_PROTOCOL"></span>

**Lat-Protokoll** ("lat-Protokoll")


</dt> <dd></dd> <dt>

<span id="Modem_Device"></span><span id="modem_device"></span><span id="MODEM_DEVICE"></span>

**Modem Gerät** ("Modem Gerät")


</dt> <dd></dd> <dt>

<span id="Network_Bridge"></span><span id="network_bridge"></span><span id="NETWORK_BRIDGE"></span>

**Netzwerk Brücke** ("Netzwerk Brücke")


</dt> <dd></dd> <dt>

<span id="Parallel_Port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>

**Paralleler Anschluss** ("paralleler Port")


</dt> <dd></dd> <dt>

<span id="RS232_Serial_Port"></span><span id="rs232_serial_port"></span><span id="RS232_SERIAL_PORT"></span>

Gleicher **seriellen Anschluss** ("RS232 Serial Port")


</dt> <dd></dd> <dt>

<span id="RS422_Port"></span><span id="rs422_port"></span><span id="RS422_PORT"></span>

**RS422-Port** ("RS422-Port")


</dt> <dd></dd> <dt>

<span id="RS423_Port"></span><span id="rs423_port"></span><span id="RS423_PORT"></span>

**RS423-Port** ("RS423-Port")


</dt> <dd></dd> <dt>

<span id="RS449_Port"></span><span id="rs449_port"></span><span id="RS449_PORT"></span>

**RS449-Port** ("RS449-Port")


</dt> <dd></dd> <dt>

<span id="Scanner_Device"></span><span id="scanner_device"></span><span id="SCANNER_DEVICE"></span>

**Scannergerät** ("Scanner-Gerät")


</dt> <dd></dd> <dt>

<span id="TCP_IP_TelNet"></span><span id="tcp_ip_telnet"></span><span id="TCP_IP_TELNET"></span>

**TCP/IP Telnet** ("TCP/IP Telnet")


</dt> <dd></dd> <dt>

<span id="X.25"></span><span id="x.25"></span>

**X. 25** ("x. 25")


</dt> <dd></dd> <dt>

<span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span>

**Nicht angegeben** ("nicht angegeben")


</dt> <dd></dd> </dl>

</dd> <dt>

**SettableBaudRate**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**commprop**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwsettableparametriams \| SP \_ Baud")
</dt> </dl>

**True** gibt an, dass die Baudrate für diesen seriellen Anschluss geändert werden kann.

</dd> <dt>

**Settabledatabits**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**commprop**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwsettableparametriams \| SP \_ DataBits")
</dt> </dl>

**True** gibt an, dass Datenbits für diesen seriellen Anschluss festgelegt werden können.

</dd> <dt>

**SettableFlowControl**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**commprop**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwsettableparametriams \| SP \_ Handshake")
</dt> </dl>

**True** gibt an, dass die Fluss Steuerung für diesen seriellen Anschluss festgelegt werden kann.

</dd> <dt>

**SettableParity**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**commprop**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwsettableparams \| SP \_ Parität")
</dt> </dl>

**True** gibt an, dass die Parität für diesen seriellen Anschluss festgelegt werden kann.

</dd> <dt>

**Settableparameitycheck**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**commprop**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwsettableparams \| SP \_ Parität \_ Check")
</dt> </dl>

**True** gibt an, dass die Paritäts Überprüfung für diesen seriellen Anschluss festgelegt werden kann (wenn die Paritäts Überprüfung unterstützt wird).

</dd> <dt>

**Settablerlsd**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**commprop**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwsettableparametriams \| SP \_ RLSD")
</dt> </dl>

**True** gibt an, dass die empfangene Zeilen Signal Erkennung (RLSD) für diesen seriellen Anschluss festgelegt werden kann (wenn "RLSD" unterstützt wird).

</dd> <dt>

**SettableStopBits**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**commprop**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwsettablebiams \| SP \_ Stopbits")
</dt> </dl>

**True** gibt an, dass Stoppbits für diesen seriellen Anschluss festgelegt werden können.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Status")
</dt> </dl>

Aktueller Status des Objekts. Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden. Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen). Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service". Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden. Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

Folgende Werte sind gültig:

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** ("OK")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Fehler** ("Fehler")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

Herunter **gestuft ("** heruntergestuft")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** ("unbekannt")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Pred-** Fehler ("pred Fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

Wird **gestartet** ("wird gestartet")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

Wird **beendet ("wird angehalten** ")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Dienst** ("Dienst")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Betont** ("gestresst")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**Nicht wiederherstellen** ("nicht wiederherstellen")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Kein Kontakt** ("kein Kontakt")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Verlorene** Kommunikations ("verlorene Kommunikations-")


</dt> <dd></dd> </dl>

</dd> <dt>

**StatusInfo**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")
</dt> </dl>

Der Status des logischen Geräts. Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 (nicht zutreffend) verwendet werden.

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (2)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Aktiviert** (3)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Deaktiviert** (4)


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**Nicht zutreffend** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**Supports16BitMode**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**commprop**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwprovfunktionalitäten \| PCF \_ 16bitmode")
</dt> </dl>

**True** gibt an, dass der 16-Bit-Modus auf diesem seriellen Anschluss unterstützt wird.

</dd> <dt>

**Supportsdtrdsr**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**commprop**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwprovfunktionalitäten \| PCF \_ dtrdsr")
</dt> </dl>

**True** gibt an, dass Data Terminal Ready (DTR)-und DSR-Signale (Data Set Ready) auf diesem seriellen Port unterstützt werden.

</dd> <dt>

**Supportselapsedtimeouts**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**commprop**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwprovfunktionalitäten \| PCF \_ totaltimeouts")
</dt> </dl>

**True** gibt an, dass abgelaufene Timeouts auf diesem seriellen Port unterstützt werden. Verstrichene Timeouts verfolgen den Gesamtzeitraum zwischen Datenübertragungen.

</dd> <dt>

**SupportsIntTimeouts**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**commprop**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwprovfunktionalitäten \| PCF \_ inttimeouts")
</dt> </dl>

**True** gibt an, dass Intervall Timeouts unterstützt werden. Ein Intervall Timeout ist die Zeitspanne, die zwischen dem Eintreffen der einzelnen Daten Daten verlaufen werden darf.

</dd> <dt>

**SupportsParityCheck**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**commprop**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwprovfunktionalitäten \| PCF \_ Parity \_ Check")
</dt> </dl>

**True** gibt an, dass die Paritäts Überprüfung auf diesem seriellen Anschluss unterstützt wird.

</dd> <dt>

**SupportsRLSD**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**commprop**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwprovfunktionalitäten \| PCF \_ RLSD")
</dt> </dl>

**True** gibt an, dass die empfangene Zeilen Signal Erkennung (RLSD) auf diesem seriellen Port unterstützt wird.

</dd> <dt>

**SupportsRTSCTS**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**commprop**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwprovfunktionalitäten \| PCF \_ RTSCTS")
</dt> </dl>

Wenn " **true**", werden die Signale "bereit zum Senden" (RTS) und "Clear to Send (CTS)" auf diesem seriellen Port unterstützt.

</dd> <dt>

**SupportsSpecialCharacters**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**commprop**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwprovfunktionalitäten \| PCF \_ SpecialChars")
</dt> </dl>

**True** gibt an, dass serielle Port Steuerzeichen unterstützt werden. Diese Zeichen signalisieren Ereignisse anstelle von Daten. Diese Zeichen können nicht angezeigt werden und vom Treiber festgelegt werden. Dazu zählen EOF Char, ErrorChar, BreakChar, EventChar, XonChar und XoffChar.

</dd> <dt>

**SupportsXOnXOff**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**commprop**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwprovfunktionalitäten \| PCF \_ XOnXOff")
</dt> </dl>

**True** gibt an, dass die Fluss Steuerung von XOn oder XOFF auf diesem seriellen Anschluss unterstützt wird.

</dd> <dt>

**Supportsxonxoffset**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**commprop**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwprovfunktionalitäten \| PCF \_ setxchar")
</dt> </dl>

**True** gibt an, dass der Kommunikationsanbieter die Konfiguration der xonor XOFF-Fluss Steuerungs Einstellung unterstützt.

</dd> <dt>

**Systemkreationclassname**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer [**: weiter**](../wmisdk/standard-qualifiers.md) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Der Wert der Eigenschaft " **kreationclassname** " des Bereichs Computers.

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.

</dd> <dt>

**Systemname**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer [**: weiter**](../wmisdk/standard-qualifiers.md) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Der Name des Bereichs Systems.

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.

</dd> <dt>

**TimeOfLastReset**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Datum und Uhrzeit des letzten zurück Setzens des Controllers. Dies könnte bedeuten, dass der Controller heruntergefahren oder erneut initialisiert wurde.

Diese Eigenschaft wird vom [**CIM- \_ Controller**](cim-controller.md)geerbt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **Win32- \_ SerialPort** -Klasse wird von [**CIM \_ SerialController**](cim-serialcontroller.md)abgeleitet.

## <a name="examples"></a>Beispiele

Eine alternative Methode zum Abrufen von Informationen zum seriellen Anschluss (aus der Registrierung) finden Sie im Beispiel zum [Aufzählen von Ports](https://Gallery.TechNet.Microsoft.Com/scriptcenter/087b4d73-4a5e-4746-b365-ad682911360e) Visual Basic.

Das PowerShell-Beispiel " [Eigenschaften von seriellen Anschluss auflisten](https://Gallery.TechNet.Microsoft.Com/42ff8eab-7d2b-4549-b178-835daecf4f12) " gibt Informationen zu den seriellen Anschlüssen zurück, die auf einem Computer installiert sind.

Im folgenden VBScript-Beispiel werden Informationen zu den auf einem Computer installierten seriellen Anschlüssen zurückgegeben.


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



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ SerialController**](cim-serialcontroller.md)
</dt> <dt>

[Computer System-Hardware Klassen](computer-system-hardware-classes.md)
</dt> </dl>

 

 
