---
description: Die CIM \_ C CIMDrive-Klasse stellt ein CD-ROM-Laufwerk auf dem Computer dar.
ms.assetid: 044c9687-fc25-4a8c-b2ef-bd7ea332af7b
ms.tgt_platform: multiple
title: CIM_CDROMDrive -Klasse (CIMWin32 WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CDROMDrive
- CIM_CDROMDrive.Caption
- CIM_CDROMDrive.Description
- CIM_CDROMDrive.InstallDate
- CIM_CDROMDrive.Name
- CIM_CDROMDrive.Status
- CIM_CDROMDrive.Availability
- CIM_CDROMDrive.ConfigManagerErrorCode
- CIM_CDROMDrive.ConfigManagerUserConfig
- CIM_CDROMDrive.CreationClassName
- CIM_CDROMDrive.DeviceID
- CIM_CDROMDrive.PowerManagementCapabilities
- CIM_CDROMDrive.ErrorCleared
- CIM_CDROMDrive.ErrorDescription
- CIM_CDROMDrive.LastErrorCode
- CIM_CDROMDrive.PNPDeviceID
- CIM_CDROMDrive.PowerManagementSupported
- CIM_CDROMDrive.StatusInfo
- CIM_CDROMDrive.SystemCreationClassName
- CIM_CDROMDrive.SystemName
- CIM_CDROMDrive.Capabilities
- CIM_CDROMDrive.CapabilityDescriptions
- CIM_CDROMDrive.CompressionMethod
- CIM_CDROMDrive.DefaultBlockSize
- CIM_CDROMDrive.ErrorMethodology
- CIM_CDROMDrive.MaxBlockSize
- CIM_CDROMDrive.MaxMediaSize
- CIM_CDROMDrive.MinBlockSize
- CIM_CDROMDrive.NeedsCleaning
- CIM_CDROMDrive.NumberOfMediaSupported
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: be0badd0e3eaaa68b162308f48cda4611ad831a003b2ed51eda0c21010d5ad18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119700970"
---
# <a name="cim_cdromdrive-class-cimwin32-wmi-providers"></a>CIM_CDROMDrive -Klasse (CIMWin32 WMI-Anbieter)

Die **CIM \_ C CIMDrive-Klasse** stellt ein CD-ROM-Laufwerk auf dem Computer dar.

> [!Note]  
> Der Name des Laufwerks entspricht nicht dem Buchstaben des logischen Laufwerks, der dem Gerät zugewiesen ist. Dies ist der Name des logischen Speichergeräts, das vom Laufwerk abhängig ist.

 

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, UUID("{8502C52B-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_CDROMDrive : CIM_MediaAccessDevice
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint16   Availability;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   DeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint32   LastErrorCode;
  string   PNPDeviceID;
  boolean  PowerManagementSupported;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   CompressionMethod;
  uint64   DefaultBlockSize;
  string   ErrorMethodology;
  uint64   MaxBlockSize;
  uint64   MaxMediaSize;
  uint64   MinBlockSize;
  boolean  NeedsCleaning;
  uint32   NumberOfMediaSupported;
};
```

## <a name="members"></a>Member

Die **CIM \_ C CIMDrive-Klasse** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **CIM \_ C CIMDrive-Klasse** verfügt über diese Methoden.



| Methode                                                                | Beschreibung                                                                                                                              |
|:----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [**Zurücksetzen**](reset-method-in-class-cim-cdromdrive.md)                 | Fordert eine Zurücksetzung des logischen Geräts an. Nicht von WMI implementiert.<br/>                                                               |
| [**SetPowerState**](setpowerstate-method-in-class-cim-cdromdrive.md) | Definiert den gewünschten Energiezustand für ein logisches Gerät und wann ein Gerät in diesen Zustand eingedrung werden soll. Nicht von WMI implementiert.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **CIM \_ C CIMDrive-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Verfügbarkeit**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Operational State \| 003.5", "MIB. IETF \| HOST-RESOURCES-MIB.hrDeviceStatus")
</dt> </dl>

Verfügbarkeit und Status des Geräts.

Diese Eigenschaft wird von [**CIM \_ LogicalDevice geerbt.**](cim-logicaldevice.md)

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Wird ausgeführt/Vollstrom** (3)


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Im Test** (5)


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Off-Dienst** (9)


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Heruntergestuft** (10)


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiesparen – Unbekannt** (13)


</dt> <dd>

Es ist bekannt, dass sich das Gerät im Energiesparmodus befindet, aber sein genauer Status ist unbekannt.

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Stromsparen – Modus mit geringer Leistung** (14)


</dt> <dd>

Das Gerät befindet sich in einem Energiesparzustand, funktioniert aber weiterhin und kann eine beeinträchtigte Leistung zeigen.

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparen – Standby** (15)


</dt> <dd>

Das Gerät funktioniert nicht, kann aber schnell voll funktionsfähig sein.

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energiezyklus** (16)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiesparen – Warnung** (17)


</dt> <dd>

Das Gerät befindet sich in einem Warnzustand, jedoch auch im Energiesparmodus.

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angehalten** (18)


</dt> <dd>

Das Gerät wird angehalten.

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

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Ruhen** (21)


</dt> <dd>

Das Gerät ist still.

</dd> </dl>

</dd> <dt>

**Capabilities**
</dt> <dd> <dl> <dt>

Datentyp: **uint16 array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Storage Devices \| 001.9", "MIF. DMTF \| Storage Devices \| 001.11", "MIF. DMTF \| Storage Devices \| 001.12", "MIF. DMTF \| Disks \| 003.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")
</dt> </dl>

Funktionen des Medienzugriffsgeräts.

Diese Eigenschaft wird von [**CIM \_ MediaAccessDevice geerbt.**](cim-mediaaccessdevice.md)

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)


</dt> <dd>

Unbekannt

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)


</dt> <dd>

Sonstiges

</dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequenzieller** Zugriff (2)


</dt> <dd>

Sequenzieller Zugriff.

</dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)


</dt> <dd>

Random-Access.

</dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Unterstützt Das Schreiben** (4)


</dt> <dd>

Schreiben.

</dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Verschlüsselung** (5)


</dt> <dd>

Verschlüsselung:

</dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Komprimierung** (6)


</dt> <dd>

Komprimierung.

</dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Unterstützt entfernbare Medien** (7)


</dt> <dd>

Wechselmedien.

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manuelle Bereinigung** (8)


</dt> <dd>

Manuelle Bereinigung.

</dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatische Bereinigung** (9)


</dt> <dd>

Automatische Bereinigung.

</dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART-Benachrichtigung** (10)


</dt> <dd>

SMART-Benachrichtigung.

</dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Unterstützt duale Medien** (11)


</dt> <dd>

Unterscheidet ein Gerät, das auf beide Seiten von dualseitigen Medien zugreifen kann, von einem Gerät, das nur eine einzige Seite liest und erfordert, dass die Medien umgeschaltet werden.

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)


</dt> <dd>

Gibt an, dass das Medium nicht explizit vom Gerät ausjiziert werden muss, bevor von einem Auswahlelement darauf zugegriffen wird.

</dd> </dl>

</dd> <dt>

**CapabilityDescriptions**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**Funktionen**")
</dt> </dl>

Ein Array von Freiformzeichenfolgen, das ausführliche Erläuterungen zu den im Capabilities-Array angegebenen **Zugriffsgerätefeatures** bietet.

> [!Note]  
> Jeder Eintrag dieses Arrays bezieht sich  auf den Eintrag im Capabilities-Array, der sich am gleichen Index befindet.

 

Diese Eigenschaft wird von [**CIM \_ MediaAccessDevice geerbt.**](cim-mediaaccessdevice.md)

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Eine kurze Textbeschreibung des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**CompressionMethod**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Freiformzeichenfolge, die den Algorithmus oder das Tool zum Komprimieren der logischen Datei angibt. Wenn es nicht möglich ist, das Komprimierungsschema zu beschreiben (da es unbekannt ist), verwenden Sie Folgendes: Wenn , verwenden Sie "Unknown". Wenn , verwenden Sie "Compressed". , verwenden Sie "Not Compressed".

Diese Eigenschaft wird von [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)geerbt.

<dt>



 ("Unbekannt")


</dt> <dd>

Das Komprimierungsschema ist unbekannt oder nicht beschrieben.

</dd> <dt>



 ("Komprimiert")


</dt> <dd>

Die logische Datei ist komprimiert, aber das Komprimierungsschema ist unbekannt oder nicht beschrieben.

</dd> <dt>



 ("Nicht komprimiert")


</dt> <dd>

Wenn die logische Datei nicht komprimiert ist

</dd> </dl>

</dd> <dt>

**ConfigManagerErrorCode**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")
</dt> </dl>

Win32 Konfigurations-Manager Fehlercode.

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

**Dieses Gerät funktioniert ordnungsgemäß.**  (0)


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.** (1)


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

**Windows kann den Treiber für dieses Gerät nicht laden.** (2)


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder ihr System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.** (3)


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder Ihre Registrierung ist möglicherweise beschädigt.** (4)


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

**Der Treiber für dieses Gerät benötigt eine Ressource, die Windows nicht verwalten können.** (5)


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

**Die Startkonfiguration für dieses Gerät ist mit anderen Geräten in Konflikt.**  (6)


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

**Kann nicht gefiltert werden.** (7)


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

**Das Treiberladeprogramm für das Gerät fehlt.** (8)


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

**Dieses Gerät funktioniert nicht ordnungsgemäß, da die steuernde Firmware die Ressourcen für das Gerät falsch meldet.** (9)


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

**Dieses Gerät kann nicht gestartet werden.** (10)


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

**Auf diesem Gerät ist ein Fehler aufgetreten.** (11)


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

**Dieses Gerät kann nicht genügend freie Ressourcen finden, die es verwenden kann.** (12)


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

**Windows können die Ressourcen dieses Geräts nicht überprüfen.** (13)


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

**Dieses Gerät kann erst ordnungsgemäß funktionieren, wenn Sie den Computer neu starten.** (14)


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

**Dieses Gerät funktioniert nicht ordnungsgemäß, da es wahrscheinlich ein Problem mit der erneuten Enumeration gibt.** (15)


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

**Windows können nicht alle Ressourcen identifizieren, die dieses Gerät verwendet.** (16)


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

**Dieses Gerät fordert einen unbekannten Ressourcentyp an.** (17)


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

**Installieren Sie die Treiber für dieses Gerät neu.** (18)


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

**Fehler beim Verwenden des VxD-Ladeprogramm.** (19)


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

**Ihre Registrierung ist möglicherweise beschädigt.** (20)


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

**Systemfehler: Versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardwaredokumentation. Windows entfernt dieses Gerät.** (21)


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

**Dieses Gerät ist deaktiviert.** (22)


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

**Systemfehler: Versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardwaredokumentation.** (23)


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß oder verfügt nicht über alle installierten Treiber.** (24)


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

**Windows richtet dieses Gerät noch ein.** (25)


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

**Windows richtet dieses Gerät noch ein.** (26)


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

**Dieses Gerät verfügt nicht über eine gültige Protokollkonfiguration.** (27)


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

**Die Treiber für dieses Gerät sind nicht installiert.** (28)


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen bereitgestellt hat.** (29)


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

**Dieses Gerät verwendet eine IRQ-Ressource (Interrupt Request), die von einem anderen Gerät verwendet wird.** (30)


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden können.** (31)


</dt> <dd></dd> </dl>

</dd> <dt>

**ConfigManagerUserConfig**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")
</dt> </dl>

**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **\_ CIM-Schlüssel**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird. Bei Verwendung mit anderen Schlüsseleigenschaften der -Klasse ermöglicht diese Eigenschaft, dass alle Instanzen der Klasse und deren Unterklassen eindeutig identifiziert werden.

Diese Eigenschaft wird von [**CIM \_ LogicalDevice geerbt.**](cim-logicaldevice.md)

</dd> <dt>

**DefaultBlockSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")
</dt> </dl>

Standardblockgröße (in Bytes) für das Gerät.

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

Diese Eigenschaft wird von [**CIM \_ MediaAccessDevice geerbt.**](cim-mediaaccessdevice.md)

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")
</dt> </dl>

Eine Textbeschreibung des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**Deviceid**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **\_ CIM-Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.

Diese Eigenschaft wird von [**CIM \_ LogicalDevice geerbt.**](cim-logicaldevice.md)

</dd> <dt>

**ErrorCleared**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

True **gibt an,** dass der in der **LastErrorCode-Eigenschaft** gemeldete Fehler jetzt entfernt wird.

Diese Eigenschaft wird von [**CIM \_ LogicalDevice geerbt.**](cim-logicaldevice.md)

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Freiformzeichenfolge, die Informationen zum In der **LastErrorCode-Eigenschaft** aufgezeichneten Fehler und durchzuführende Korrekturmaßnahmen enthält.

Diese Eigenschaft wird von [**CIM \_ LogicalDevice geerbt.**](cim-logicaldevice.md)

</dd> <dt>

**ErrorMethodology**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Freiformzeichenfolge, die die Typen der vom Gerät unterstützten Fehlererkennung und -korrektur beschreibt.

Diese Eigenschaft wird von [**CIM \_ MediaAccessDevice geerbt.**](cim-mediaaccessdevice.md)

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Installation date")
</dt> </dl>

Gibt an, wann das Objekt installiert wurde. Das Fehlen eines Werts gibt nicht an, dass das Objekt nicht installiert ist.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**LastErrorCode**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Letzter vom logischen Gerät gemeldeter Fehlercode.

Diese Eigenschaft wird von [**CIM \_ LogicalDevice geerbt.**](cim-logicaldevice.md)

</dd> <dt>

**MaxBlockSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")
</dt> </dl>

Maximale Blockgröße (in Bytes) für Medien, auf die vom Gerät zugegriffen wird.

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

Diese Eigenschaft wird von [**CIM \_ MediaAccessDevice geerbt.**](cim-mediaaccessdevice.md)

</dd> <dt>

**MaxMediaSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Sequential Access Devices \| 001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")
</dt> </dl>

Maximale Größe der von diesem Gerät unterstützten Medien in Kilobyte. Kilobytes werden als Anzahl von Bytes multipliziert mit 1000 interpretiert (nicht als Anzahl von Bytes multipliziert mit 1024).

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

Diese Eigenschaft wird von [**CIM \_ MediaAccessDevice geerbt.**](cim-mediaaccessdevice.md)

</dd> <dt>

**MinBlockSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")
</dt> </dl>

Minimale Blockgröße (in Bytes) für Medien, auf die vom Gerät zugegriffen wird.

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

Diese Eigenschaft wird von [**CIM \_ MediaAccessDevice geerbt.**](cim-mediaaccessdevice.md)

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")
</dt> </dl>

Bezeichnung, unter der das Objekt bekannt ist. Bei Unterklassen kann diese Eigenschaft überschrieben werden, um eine Schlüsseleigenschaft zu sein.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

</dd> <dt>

**NeedsCleaning**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

True **gibt an,** dass das Medienzugriffsgerät eine Bereinigung benötigt. Ob eine manuelle oder automatische Bereinigung möglich ist, wird in der **Capabilities-Arrayeigenschaft** angegeben.

Diese Eigenschaft wird von [**CIM \_ MediaAccessDevice geerbt.**](cim-mediaaccessdevice.md)

</dd> <dt>

**NumberOfMediaSupported**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Maximale Anzahl von mehreren einzelnen Medien, die unterstützt oder eingefügt werden können.

Diese Eigenschaft wird von [**CIM \_ MediaAccessDevice geerbt.**](cim-mediaaccessdevice.md)

</dd> <dt>

**PNPDeviceID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")
</dt> </dl>

Gibt die Win32-Plug & Play Geräte-ID des logischen Geräts an.

Beispiel: \* "PNP030b"

Diese Eigenschaft wird von [**CIM \_ LogicalDevice geerbt.**](cim-logicaldevice.md)

</dd> <dt>

**PowerManagementCapabilities**
</dt> <dd> <dl> <dt>

Datentyp: **uint16 array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die spezifischen energiebezogenen Funktionen des logischen Geräts an.

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)


</dt> <dd>

Die energiebezogenen Kapazitäten sind unbekannt.

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)


</dt> <dd>

Energiebezogene Kapazitäten werden für dieses Gerät nicht unterstützt.

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)


</dt> <dd>

Energiebezogene Kapazitäten wurden deaktiviert.

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)


</dt> <dd>

Die Energieverwaltungsfunktionen sind derzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiesparmodi** (4)


</dt> <dd>

Das Gerät kann seinen Energiezustand basierend auf der Nutzung oder anderen Kriterien ändern.

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)


</dt> <dd>

Die **SetPowerState-Methode** wird unterstützt. Diese Methode befindet sich in der übergeordneten [**CIM \_ LogicalDevice-Klasse**](cim-logicaldevice.md) und kann implementiert werden. Weitere Informationen finden Sie unter [Entwerfen von MOF-Klassen (Managed Object Format).](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes)

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**PowerCycling unterstützt** (6)


</dt> <dd>

Die **SetPowerState-Methode** kann aufgerufen werden, wobei der *PowerState-Parameter* auf 5 ("Power Cycle") festgelegt ist.

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Timed Power On Supported (7) **(Zeitiertes Einschalten unterstützt** (7)


</dt> <dd>

Die **SetPowerState-Methode** kann aufgerufen werden, wobei der *PowerState-Parameter* auf 5 ("Power Cycle") und der *Time-Parameter* für das Einschalten auf ein bestimmtes Datum und eine bestimmte Uhrzeit oder ein bestimmtes Intervall festgelegt ist.

</dd> </dl>

</dd> <dt>

**PowerManagementSupported**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

True gibt an, dass das Gerät mit Strom verwaltet werden kann, d.h. in einen Energiesparzustand versetzt werden kann. **False** gibt an, dass der ganzzahlige Wert 1 ("Nicht unterstützt") der einzige Eintrag im **PowerManagementCapabilities-Array** sein sollte.

Diese Eigenschaft gibt nicht an, ob energieverwaltungsfeatures derzeit aktiviert sind oder welche Features unterstützt werden. Weitere Informationen finden Sie im **PowerManagementCapabilities-Array.**

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")
</dt> </dl>

Zeichenfolge, die den aktuellen Status des Objekts angibt. Der Betriebsstatus und der nicht betriebsbereite Status können definiert werden. Der Betriebsstatus kann "OK", "Heruntergestuft" und "Fehler vor dem Fehler" enthalten. "Pred Fail" gibt an, dass ein Element ordnungsgemäß funktioniert, aber einen Fehler vorhersagt (z. B. ein SMART-fähiges Festplattenlaufwerk).

Nicht betriebsbereite Status können "Error", "Starting", "Stopping" und "Service" sein. "Dienst" kann während der Datenträgerspiegelung, beim erneuten Laden einer Benutzerberechtigungsliste oder bei anderen Administrativen Arbeiten angewendet werden. Nicht alle dieser Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.

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

**Heruntergestuft** ("Heruntergestuft")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** ("Unbekannt")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Pred Fail** ("Pred Fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Wird gestartet** ("Wird gestartet")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Beenden** ("Wird beendet")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Dienst** ("Dienst")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Mannslast** ("1000")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**NonRecover** ("NonRecover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Kein Kontakt** ("Kein Kontakt")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Verlorenes Komma** ("Verlorenes Komma")


</dt> <dd></dd> </dl>

</dd> <dt>

**StatusInfo**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Operational State \| 003.3")
</dt> </dl>

Status des logischen Geräts. Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 ("Nicht zutreffend") verwendet werden.

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Andere** (1)


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

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Weitergegeben**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ CIM-System**](cim-system.md).**CreationClassName**"), [**\_ CIM-Schlüssel**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Der Name der Erstellungsklasse des Bereichssystems.

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.

</dd> <dt>

**Systemname**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Weitergegeben**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ CIM-System**](cim-system.md).**Name**"), [**\_ CIM-Schlüssel**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Der Name des Bereichssystems.

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **CIM \_ CREDODrive-Klasse** wird von [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)abgeleitet.

WMI implementiert diese Klasse nicht. Weitere Informationen zu Klassen, die von **CIM \_ CREDODrive** abgeleitet wurden, finden Sie unter [Win32-Klassen.](win32-provider.md)

Diese Dokumentation wird von den CIM-Klassenbeschreibungen abgeleitet, die von dmtf veröffentlicht wurden. Möglicherweise hat Microsoft Änderungen vorgenommen, um kleinere Fehler zu korrigieren, den Dokumentationsstandards des Microsoft SDK zu entsprechen oder weitere Informationen bereitzustellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)
</dt> </dl>

 

