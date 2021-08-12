---
description: Stellt ein physisches Laufwerk dar, das von einem Computer angezeigt wird, auf dem das Windows Betriebssystem ausgeführt wird.
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
ms.openlocfilehash: 94d9afa6fb4c38c4286f705b50011f5378057004cbe7fe5a4b2b700a0385c10f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118675236"
---
# <a name="win32_diskdrive-class"></a>Win32 \_ DiskDrive-Klasse

Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) **"Win32 \_ DiskDrive"** stellt ein physisches Laufwerk dar, das von einem Computer mit dem betriebssystem Windows erkannt wird.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

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

## <a name="members"></a>Member

Die **Win32 \_ DiskDrive-Klasse** verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32 \_ DiskDrive-Klasse** verfügt über diese Methoden.



| Methode            | Beschreibung                                                                                                                                                                                              |
|:------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Zurücksetzen**         | Nicht implementiert. Informationen zum Implementieren dieser Methode finden Sie in der Dokumentation zur [**Reset-Methode**](reset-method-in-class-cim-controller.md) in [**CIM \_ DiskDrive.**](cim-diskdrive.md)<br/>                 |
| **SetPowerState** | Nicht implementiert. Informationen zum Implementieren dieser Methode finden Sie in der Dokumentation zur [**SetPowerState-Methode**](setpowerstate-method-in-class-cim-controller.md) in [**CIM \_ DiskDrive.**](cim-diskdrive.md)<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ DiskDrive-Klasse** verfügt über diese Eigenschaften.

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

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Andere** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>Running/Full Power (3) **(Ausführen/Vollbetrieb** (3))


</dt> <dd>

Running or Full Power

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

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)


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

Das Gerät befindet sich bekanntermaßen im Energiesparmodus, aber sein genauer Status ist unbekannt.

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus – Energiesparmodus** (14)


</dt> <dd>

Das Gerät befindet sich im Energiesparzustand, funktioniert aber weiterhin und kann eine beeinträchtigte Leistung aufweisen.

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus – Standby** (15)


</dt> <dd>

Das Gerät funktioniert nicht, kann aber schnell voll ausgepowert werden.

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Stromzyklus** (16)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiesparen – Warnung** (17)


</dt> <dd>

Das Gerät befindet sich in einem Warnungszustand, aber auch im Energiesparmodus.

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angehalten** (18)


</dt> <dd></dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)


</dt> <dd></dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)


</dt> <dd></dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Still** (21)


</dt> <dd>

Das Laufwerk ist nicht verfügbar.

</dd> </dl>

</dd> <dt>

**BytesPerSector**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API-Geräteeingabe- \| und -ausgabestrukturen \| [**DISK \_ GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| BytesPerSector"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")
</dt> </dl>

Anzahl der Bytes in jedem Sektor für das physische Laufwerk.

Beispiel: 512

</dd> <dt>

**Capabilities**
</dt> <dd> <dl> <dt>

Datentyp: **uint16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indiziert"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Storage Devices \| 001.9", "MIF. DMTF \| Storage Devices \| 001.11", "MIF. DMTF \| Storage Devices \| 001.12", "MIF. DMTF \| Disks \| 003.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")
</dt> </dl>

Array von Funktionen des Medienzugriffsgeräts. Das Gerät unterstützt beispielsweise zufälligen Zugriff (3), Wechselmedien (7) und automatische Bereinigung (9).

Diese Eigenschaft wird von [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)geerbt.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Andere** (1)


</dt> <dd></dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequenzieller Zugriff** (2)


</dt> <dd></dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Zufälliger Zugriff** (3)


</dt> <dd></dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Unterstützt das Schreiben** (4)


</dt> <dd></dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Verschlüsselung** (5)


</dt> <dd></dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Komprimierung** (6)


</dt> <dd></dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Unterstützt entfernbare Medien** (7)


</dt> <dd>

Unterstützt Wechselmedien

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manuelle Bereinigung** (8)


</dt> <dd></dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatische Bereinigung** (9)


</dt> <dd></dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART-Benachrichtigung** (10)


</dt> <dd></dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Unterstützt doppelseitige Medien** (11)


</dt> <dd>

Unterstützt Dual-Sided Medien

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required (12) (Bereitstellung vorab** aufheben nicht erforderlich (12)


</dt> <dd>

Ejection vor der Bereitstellung des Laufwerks nicht erforderlich

</dd> </dl>

</dd> <dt>

**CapabilityDescriptions**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indiziert"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**Funktionen**")
</dt> </dl>

Liste ausführlicherer Erklärungen für alle Im **Capabilities-Array** angegebenen Zugriffsgerätefeatures. Beachten Sie, dass jeder Eintrag dieses Arrays mit dem Eintrag im **Capabilities-Array** verknüpft ist, das sich am gleichen Index befindet.

Diese Eigenschaft wird von [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)geerbt.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Kurze Beschreibung des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**CompressionMethod**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Algorithmus oder Tool, der vom Gerät zur Unterstützung der Komprimierung verwendet wird. Diese Eigenschaft wird von [**CIM \_ MediaAccessDevice geerbt.**](cim-mediaaccessdevice.md)

Der Name des Komprimierungsalgorithmus oder einer der folgenden Werte.

<dt>



 ("Unbekannt")


</dt> <dd>

Ob das Gerät Komprimierungsfunktionen unterstützt, ist nicht bekannt.

</dd> <dt>



 ("Komprimiert")


</dt> <dd>

Das Gerät unterstützt Komprimierungsfunktionen, aber sein Komprimierungsschema ist nicht bekannt oder nicht offengelegt.

</dd> <dt>



 ("Nicht komprimiert")


</dt> <dd>

Das Gerät unterstützt keine Komprimierung.

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

Windows Konfigurations-Manager Fehlercode.

Diese Eigenschaft wird von [**CIM \_ LogicalDevice geerbt.**](cim-logicaldevice.md)

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

<span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows kann den Treiber für dieses Gerät nicht laden.** (2)


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder ihr System hat möglicherweise nicht genügend Arbeitsspeicher oder andere Ressourcen.** (3)


</dt> <dd>

Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System hat möglicherweise wenig Arbeitsspeicher oder andere Ressourcen.

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder Ihre Registrierung ist möglicherweise beschädigt.** (4)


</dt> <dd>

Das Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Der Treiber für dieses Gerät benötigt eine Ressource, die Windows verwaltet werden kann.** (5)


</dt> <dd>

Der Treiber für das Gerät erfordert eine Ressource, die Windows verwaltet werden kann.

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

<span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Das Treiberlader für das Gerät fehlt.** (8)


</dt> <dd>

Das Treiberlader für das Gerät fehlt.

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da die steuernde Firmware die Ressourcen für das Gerät falsch berichtet.** (9)


</dt> <dd>

Das Gerät funktioniert nicht ordnungsgemäß. Die steuernde Firmware berichtet falsch über die Ressourcen für das Gerät.

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Dieses Gerät kann nicht gestartet werden.** (10)


</dt> <dd>

Das Gerät kann nicht gestartet werden.

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Fehler bei diesem Gerät.** (11)


</dt> <dd>

Fehler beim Gerät.

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Dieses Gerät kann nicht genügend freie Ressourcen finden, die es verwenden kann.** (12)


</dt> <dd>

Das Gerät kann nicht genügend freie Ressourcen für die Verwendung finden.

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows können die Ressourcen dieses Geräts nicht überprüfen.** (13)


</dt> <dd>

Windows können die Ressourcen des Geräts nicht überprüfen.

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Dieses Gerät funktioniert erst dann ordnungsgemäß, wenn Sie Ihren Computer neu starten.** (14)


</dt> <dd>

Das Gerät funktioniert erst dann ordnungsgemäß, wenn der Computer neu gestartet wird.

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Enumeration vor liegt.** (15)


</dt> <dd>

Das Gerät funktioniert aufgrund eines möglichen Problems mit der erneuten Enumeration nicht ordnungsgemäß.

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows können nicht alle Ressourcen identifizieren, die dieses Gerät verwendet.** (16)


</dt> <dd>

Windows können nicht alle Ressourcen identifizieren, die das Gerät verwendet.

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

<span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Fehler beim Verwenden des VxD-Ladeers.** (19)


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Ihre Registrierung ist möglicherweise beschädigt.** (20)


</dt> <dd>

Die Registrierung ist möglicherweise beschädigt.

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Systemfehler: Versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, lesen Sie ihre Hardwaredokumentation. Windows entfernt dieses Gerät.** (21)


</dt> <dd>

Systemfehler. Wenn das Ändern des Gerätetreibers ineffektiv ist, lesen Sie die Hardwaredokumentation. Windows entfernt das Gerät.

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Dieses Gerät ist deaktiviert.** (22)


</dt> <dd>

Das Gerät ist deaktiviert.

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Systemfehler: Versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, lesen Sie Ihre Hardwaredokumentation.** (23)


</dt> <dd>

Systemfehler. Wenn das Ändern des Gerätetreibers ineffektiv ist, lesen Sie die Hardwaredokumentation.

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß oder verfügt nicht über alle installierten Treiber.** (24)


</dt> <dd>

Das Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß oder verfügt nicht über alle installierten Treiber.

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows wird dieses Gerät weiterhin eingerichtet.** (25)


</dt> <dd>

Windows wird das Gerät weiterhin eingerichtet.

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows wird dieses Gerät weiterhin eingerichtet.** (26)


</dt> <dd>

Windows wird das Gerät weiterhin eingerichtet.

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Dieses Gerät verfügt nicht über eine gültige Protokollkonfiguration.** (27)


</dt> <dd>

Das Gerät verfügt nicht über eine gültige Protokollkonfiguration.

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Die Treiber für dieses Gerät sind nicht installiert.** (28)


</dt> <dd>

Gerätetreiber sind nicht installiert.

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen bereitgestellt hat.** (29)


</dt> <dd>

Das Gerät ist deaktiviert. Die Gerätefirmware hat nicht die erforderlichen Ressourcen bereitgestellt.

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Dieses Gerät verwendet eine IRQ-Ressource (Interrupt Request), die von einem anderen Gerät verwendet wird.** (30)


</dt> <dd>

Das Gerät verwendet eine IRQ-Ressource, die von einem anderen Gerät verwendet wird.

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden können.** (31)


</dt> <dd>

Das Gerät funktioniert nicht ordnungsgemäß. Windows können die erforderlichen Gerätetreiber nicht laden.

</dd> </dl>

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

Name der ersten konkreten Klasse, die in der Vererbungskette angezeigt wird, die bei der Erstellung einer Instanz verwendet wird. Bei Verwendung mit den anderen Schlüsseleigenschaften der -Klasse ermöglicht die -Eigenschaft, dass alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.

</dd> <dt>

**DefaultBlockSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")
</dt> </dl>

Standardblockgröße in Bytes für dieses Gerät.

Diese Eigenschaft wird von [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)geerbt.

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Beschreibung")
</dt> </dl>

Eine Beschreibung des Objekts.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**Deviceid**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schlüssel,**](/windows/desktop/WmiSdk/key-qualifier) [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

Eindeutiger Bezeichner des Laufwerks mit anderen Geräten auf dem System.

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.

</dd> <dt>

**ErrorCleared**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True** gibt an, dass der in **LastErrorCode** gemeldete Fehler jetzt gelöscht wird.

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Weitere Informationen zu dem in **LastErrorCode** aufgezeichneten Fehler sowie Informationen zu ggf. ergriffenen Korrekturmaßnahmen.

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.

</dd> <dt>

**ErrorMethodology**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Typ der von diesem Gerät unterstützten Fehlererkennung und -korrektur.

Diese Eigenschaft wird von [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)geerbt.

</dd> <dt>

**FirmwareRevision**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API-Geräteeingabe- \| und -ausgabestrukturen \| [**STORAGE DEVICE \_ \_ DESCRIPTOR**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor) \| ProductRevisionOffset")
</dt> </dl>

Revision für die Datenträgerlaufwerkfirmware, die vom Hersteller zugewiesen wird.

</dd> <dt>

**Index**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Windows 95/98 Functions \| DRIVE MAP INFO \_ \_ \| btInt13Unit")
</dt> </dl>

Nummer des physischen Laufwerks des angegebenen Laufwerks. Diese Eigenschaft wird durch die [**\_ \_ SPEICHERGERÄTENUMMER-Struktur**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_number) gefüllt, die vom [**IOCTL \_ STORAGE GET DEVICE \_ \_ NUMBER-Steuerungscode \_**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_get_device_number) zurückgegeben wird. Der Wert 0xffffffff gibt an, dass das angegebene Laufwerk keinem physischen Laufwerk zugeordnet wird.

Beispiel: 1

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Installationsdatum")
</dt> </dl>

Datum und Uhrzeit der Installation des Objekts. Diese Eigenschaft benötigt keinen Wert, um anzugeben, dass das Objekt installiert ist.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**InterfaceType**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API-Geräteeingabe- \| und -ausgabefunktionen \| [**DeviceIoControl")**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> </dl>

Schnittstellentyp des physischen Laufwerks.

Die Werte sind:

SCSI

Hdc

IDE

USB

1394

</dd> <dt>

**LastErrorCode**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der letzte vom logischen Gerät gemeldete Fehlercode.

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.

</dd> <dt>

**Manufacturer**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE \_ HARDWARE \\ \\ \\ \\ DEVICEMAP \\ \\ \\ \\ Scsi Port \\ \\ Scsi Bus Target ID Logical Unit ID \\ \\ \\ \\ \\ \\ Identifier", "Win32Registry \| Manufacturer")
</dt> </dl>

Name des Laufwerkherstellers.

Beispiel: "Seagate"

</dd> <dt>

**MaxBlockSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")
</dt> </dl>

Maximale Blockgröße (in Bytes) für Medien, auf die von diesem Gerät zugegriffen wird.

Diese Eigenschaft wird von [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)geerbt.

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

</dd> <dt>

**MaxMediaSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Sequential Access Devices \| 001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")
</dt> </dl>

Maximale Mediengröße in Kilobyte von Medien, die von diesem Gerät unterstützt werden.

Diese Eigenschaft wird von [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)geerbt.

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

</dd> <dt>

**MediaLoaded**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API-Geräteeingabe- \| und -ausgabestrukturen \| [**DISK \_ GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| MediaType \| FixedMedia")
</dt> </dl>

**True** gibt an, dass die Medien für ein Laufwerk geladen werden. Dies bedeutet, dass das Gerät über ein lesbares Dateisystem verfügt und darauf zugegriffen werden kann. Bei Festplattenlaufwerken ist diese Eigenschaft immer **TRUE.**

</dd> <dt>

**MediaType**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API-Geräteeingabe- \| und -ausgabestrukturen \| [**DISK \_ GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| MediaType")
</dt> </dl>

Typ des Mediums, das von diesem Gerät verwendet wird oder auf das zugegriffen wird.

Mögliche Werte:

<dt>

<span id="External_hard_disk_media"></span><span id="external_hard_disk_media"></span><span id="EXTERNAL_HARD_DISK_MEDIA"></span>

**Externe Festplattenmedien**


</dt> <dd></dd> <dt>

<span id="Removable_media"></span><span id="removable_media"></span><span id="REMOVABLE_MEDIA"></span>

**Wechselmedien** ("Wechselmedien außer Disketten")


</dt> <dd></dd> <dt>

<span id="Fixed_hard_disk"></span><span id="fixed_hard_disk"></span><span id="FIXED_HARD_DISK"></span>

**Feste Festplatte** ("Festes Festplattenmedium")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** ("Format ist unbekannt")


</dt> <dd></dd> </dl>

</dd> <dt>

**MinBlockSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes")
</dt> </dl>

Minimale Blockgröße in Bytes für Medien, auf die von diesem Gerät zugegriffen wird.

Diese Eigenschaft wird von [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)geerbt.

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

</dd> <dt>

**Modell**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE \_ HARDWARE \\ \\ \\ \\ DEVICEMAP \\ \\ \\ \\ Scsi Port \\ \\ Scsi Bus Target ID Logical Unit ID \\ \\ \\ \\ \\ \\ Identifier", "Win32Registry \| ProductId")
</dt> </dl>

Die Modellnummer des Laufwerks des Herstellers.

Beispiel: "ST32171W"

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")
</dt> </dl>

Bezeichnung, mit der das Objekt bekannt ist. Bei einer Unterklasse kann die Eigenschaft als Schlüsseleigenschaft überschrieben werden.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.

</dd> <dt>

**NeedsCleaning**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True** gibt an, dass das Medienzugriffsgerät bereinigungs erforderlich ist. Ob eine manuelle oder automatische Bereinigung möglich ist, wird in der **Capabilities-Eigenschaft** angegeben.

Diese Eigenschaft wird von [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)geerbt.

</dd> <dt>

**NumberOfMediaSupported**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Maximale Anzahl von Medien, die unterstützt oder eingefügt werden können (wenn das Medienzugriffsgerät mehrere einzelne Medien unterstützt).

Diese Eigenschaft wird von [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)geerbt.

</dd> <dt>

**Partitionen**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API-Geräteeingabe- \| und -ausgabestrukturen \| [**PARTITION \_ INFORMATION**](/windows/desktop/api/winioctl/ns-winioctl-partition_information) \| RecognizedPartition")
</dt> </dl>

Anzahl der Partitionen auf diesem physischen Laufwerk, die vom Betriebssystem erkannt werden.

Beispiel: 2

</dd> <dt>

**PNPDeviceID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")
</dt> </dl>

Windows Plug & Play Gerätebezeichner des logischen Geräts.

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.

Beispiel: \* "PNP030b"

</dd> <dt>

**PowerManagementCapabilities**
</dt> <dd> <dl> <dt>

Datentyp: **uint16-Array**
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


</dt> <dd>

Energiebezogene Kapazitäten werden für dieses Gerät nicht unterstützt.

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)


</dt> <dd></dd> <dt>

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

Die [**SetPowerState-Methode**](setpowerstate-method-in-class-cim-controller.md) wird unterstützt. Diese Methode befindet sich in der übergeordneten [**CIM \_ LogicalDevice-Klasse**](cim-logicaldevice.md) und kann implementiert werden. Weitere Informationen finden Sie unter [Entwerfen von MOF-Klassen (Managed Object Format).](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes)

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**PowerCycling unterstützt** (6)


</dt> <dd>

Die [**SetPowerState-Methode**](setpowerstate-method-in-class-cim-controller.md) kann aufgerufen werden, wobei der *PowerState-Parameter* auf 5 (Power Cycle) festgelegt ist.

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Timed Power On Supported (7) **(Zeitiertes Einschalten unterstützt** (7)


</dt> <dd>

Timed Power-On Supported

Die [**SetPowerState-Methode**](setpowerstate-method-in-class-cim-controller.md) kann aufgerufen werden, wenn der *PowerState-Parameter* auf 5 (Power Cycle) und *Time* auf ein bestimmtes Datum und eine bestimmte Uhrzeit oder ein bestimmtes Intervall für das Ein-/Aus-Setzen festgelegt ist.

</dd> </dl>

</dd> <dt>

**PowerManagementSupported**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

True **gibt an,** dass das Gerät energieverwendt verwaltet werden kann (kann in den Suspend-Modus wechseln und so weiter). Die -Eigenschaft gibt nicht an, dass energieverwaltungsfeatures derzeit aktiviert sind, sondern nur, dass das logische Gerät energieverwaltungsfähig ist.

Diese Eigenschaft wird von [**CIM \_ LogicalDevice geerbt.**](cim-logicaldevice.md)

</dd> <dt>

**SCSIBus**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Input and Output Structures \| [**SCSI \_ ADDRESS**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address) \| PathId")
</dt> </dl>

SCSI-Busnummer des Laufwerks.

Beispiel: 0

</dd> <dt>

**SCSILogicalUnit**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Input and Output Structures \| [**SCSI \_ ADDRESS**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address) \| Lun")
</dt> </dl>

SCSI-LUN (Logical Unit Number) des Laufwerks.

Beispiel: 0

</dd> <dt>

**SCSIPort**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Input and Output Structures \| [**SCSI \_ ADDRESS**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address) \| PortNumber")
</dt> </dl>

SCSI-Portnummer des Laufwerks.

Beispiel: 0

</dd> <dt>

**SCSITargetId**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Input and Output Structures \| [**SCSI \_ ADDRESS**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address) \| TargetId")
</dt> </dl>

SCSI-IdNr. des Laufwerks.

Beispiel: 0

</dd> <dt>

**SectorsPerTrack**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Input and Output Structures DISK \| [**\_ GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| SectorsPerTrack")
</dt> </dl>

Anzahl der Sektoren in jeder Spur für dieses physische Laufwerk.

Beispiel: 63

</dd> <dt>

**Serialnumber**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Input and Output Structures STORAGE DEVICE \| [**\_ \_ DESCRIPTOR**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor) \| SerialNumberOffset")
</dt> </dl>

Nummer, die vom Hersteller zugeordnet wird, um die physischen Medien zu identifizieren.

Beispiel: WD-WM3493798728

</dd> <dt>

**Signature**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Input and Output Structures DRIVE LAYOUT \| [**\_ \_ INFORMATION**](/windows/desktop/api/winioctl/ns-winioctl-drive_layout_information) \| Signature")
</dt> </dl>

Datenträgeridentifikation. Diese Eigenschaft kann verwendet werden, um eine freigegebene Ressource zu identifizieren.

</dd> <dt>

**Größe**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Input and Output Structures DISK \| [**\_ GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)"), [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")
</dt> </dl>

Größe des Laufwerks. Sie wird berechnet, indem die Gesamtzahl der Zylinder, Spuren in jedem Zylinder, Sektoren auf jeder Spur und Bytes in jedem Sektor multipliziert werden.

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")
</dt> </dl>

Aktueller Status des Objekts. Es können verschiedene betriebsbereite und nicht betriebsbereite Status definiert werden. Folgende Betriebsstatus sind möglich: "OK", "Heruntergestuft" und "Fehler vor dem Ausfall" (ein Element, z. B. eine SMART-fähige Festplatte, funktioniert möglicherweise ordnungsgemäß, aber es wird in naher Zukunft ein Fehler vorhergesagt). Nicht operative Status sind: "Error", "Starting", "Stopping" und "Service". Letzteres, "Dienst", kann während der Spiegelung eines Datenträgers, beim erneuten Laden einer Benutzerberechtigungsliste oder bei anderen administrativen Aufgaben angewendet werden. Nicht alle derartigen Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](cim-managedsystemelement.md)

Gültige Werte:

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

**Wird** gestartet ("Wird gestartet")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Wird beendet** ("Wird beendet")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Dienst** ("Dienst")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Striche** ("Strich")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**NonRecover** ("NonRecover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Kein Kontakt** ("Kein Kontakt")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Lost Comm** ("Lost Comm")


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

Status des logischen Geräts. Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 (Nicht zutreffend) verwendet werden.

Diese Eigenschaft wird von [**CIM \_ LogicalDevice geerbt.**](cim-logicaldevice.md)

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

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ CIM-System**](cim-system.md).**CreationClassName**"), [**\_ CIM-Schlüssel**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Der Wert der **CreationClassName-Eigenschaft** des Bereichscomputers.

Diese Eigenschaft wird von [**CIM \_ LogicalDevice geerbt.**](cim-logicaldevice.md)

</dd> <dt>

**Systemname**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ CIM-System**](cim-system.md).**Name**"), [**\_ CIM-Schlüssel**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Name des Bereichssystems.

Diese Eigenschaft wird von [**CIM \_ LogicalDevice geerbt.**](cim-logicaldevice.md)

</dd> <dt>

**TotalCylinders**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Input and Output Structures DISK \| [**\_ GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| Cylinders")
</dt> </dl>

Gesamtanzahl der Zylinder auf dem physischen Laufwerk. Hinweis: Der Wert für diese Eigenschaft wird über erweiterte Funktionen des BIOS-Interrupts 13h ermittelt. Der Wert kann ungenau sein, wenn das Laufwerk ein Übersetzungsschema verwendet, um Datenträgergrößen mit hoher Kapazität zu unterstützen. Wenden Sie sich an den Hersteller, um genaue Laufwerkspezifikationen zu erhalten.

Beispiel: 657

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

</dd> <dt>

**TotalHeads**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Input and Output Structures DISK \| [**\_ GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| TracksPerCylinder")
</dt> </dl>

Gesamtanzahl der Kopfköpfe auf dem Laufwerk. Hinweis: Der Wert für diese Eigenschaft wird über erweiterte Funktionen des BIOS-Interrupts 13h ermittelt. Der Wert kann ungenau sein, wenn das Laufwerk ein Übersetzungsschema verwendet, um Datenträgergrößen mit hoher Kapazität zu unterstützen. Wenden Sie sich an den Hersteller, um genaue Laufwerkspezifikationen zu erhalten.

</dd> <dt>

**TotalSectors**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Input and Output Structures DISK \| [**\_ GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| SectorsPerTrack")
</dt> </dl>

Gesamtzahl der Sektoren auf dem physischen Laufwerk. Hinweis: Der Wert für diese Eigenschaft wird über erweiterte Funktionen des BIOS-Interrupts 13h ermittelt. Der Wert kann ungenau sein, wenn das Laufwerk ein Übersetzungsschema verwendet, um Datenträgergrößen mit hoher Kapazität zu unterstützen. Wenden Sie sich an den Hersteller, um genaue Laufwerkspezifikationen zu erhalten.

Beispiel: 2649024

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

</dd> <dt>

**TotalTracks**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Input and Output Structures DISK \| [**\_ GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| TracksPerCylinder")
</dt> </dl>

Gesamtanzahl der Spuren auf dem physischen Laufwerk. Hinweis: Der Wert für diese Eigenschaft wird über erweiterte Funktionen des BIOS-Interrupts 13h ermittelt. Der Wert kann ungenau sein, wenn das Laufwerk ein Übersetzungsschema verwendet, um Datenträgergrößen mit hoher Kapazität zu unterstützen. Wenden Sie sich an den Hersteller, um genaue Laufwerkspezifikationen zu erhalten.

Beispiel: 42048

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

</dd> <dt>

**TracksPerCylinder**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Device Input and Output Structures DISK \| [**\_ GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| TracksPerCylinder")
</dt> </dl>

Anzahl der Spuren in jedem Zylinder auf dem physischen Laufwerk. Hinweis: Der Wert für diese Eigenschaft wird über erweiterte Funktionen des BIOS-Interrupts 13h ermittelt. Der Wert kann ungenau sein, wenn das Laufwerk ein Übersetzungsschema verwendet, um Datenträgergrößen mit hoher Kapazität zu unterstützen. Wenden Sie sich an den Hersteller, um genaue Laufwerkspezifikationen zu erhalten.

Beispiel: 64

</dd> </dl>

## <a name="remarks"></a>Hinweise

Physische Festplattenlaufwerke sind das primäre Speichermedium für Informationen in jeder Computerumgebung. Obwohl Organisationen häufig Geräte wie Bandlaufwerke und Compact Disk-Laufwerke zum Archivieren von Daten verwenden, eignen sich diese Geräte nicht für die täglichen Speicherung von Benutzerdaten. Nur physische Festplatten bieten die Geschwindigkeit und Benutzerfreundlichkeit, die zum Speichern von Daten und zum Ausführen von Anwendungen und des Betriebssystems erforderlich sind.

Um Daten effizient zu verwalten, ist es wichtig, über eine detaillierte Inventur aller physischen Datenträger, deren Funktionen und kapazitäten zu verfügen. Sie können die **Win32 \_ DiskDrive-Klasse** verwenden, um diesen Inventurtyp zu leiten.

Jede Schnittstelle zu einem Windows physischen Laufwerk ist ein Nachfolger (oder Member) dieser Klasse. Die Features des Datenträgerlaufwerks, die über dieses Objekt zu sehen sind, entsprechen den logischen und Verwaltungsmerkmalen des Laufwerks. In einigen Fällen spiegelt dies möglicherweise nicht die tatsächlichen physischen Merkmale des Geräts wider. Jedes Objekt, das auf einem anderen logischen Gerät basiert, wäre kein Member dieser Klasse.

Aus Sicherheitsgründen muss für einen Benutzer, der eine Verbindung von einem Remotecomputer aus herstellen, die **SC \_ MANAGER \_ CONNECT-Berechtigung** aktiviert sein, um diese Klasse aufzählen zu können. Weitere Informationen finden Sie unter [Dienstsicherheit und Zugriffsrechte.](/windows/desktop/Services/service-security-and-access-rights)

Die **Win32 \_ DiskDrive-Klasse** wird von [**CIM \_ DiskDrive**](cim-diskdrive.md) abgeleitet, das von [**CIM \_ MediaAccessDevice abgeleitet wird.**](cim-mediaaccessdevice.md) Die **CIM \_ MediaAccessDevice-Klasse** wird von [**CIM \_ LogicalDevice ableiten.**](cim-logicaldevice.md)

## <a name="examples"></a>Beispiele

Das [Codebeispiel server inventory report-WMI & CIM](https://Gallery.TechNet.Microsoft.Com/Servers-Inventory-report-e79e2b24) PowerShell im TechNet-Katalog verwendet eine Reihe von Klassen, einschließlich **Win32 \_ DiskDrive,** um Informationen zum Serverstatus zurück zu geben.

Das PowerShell-Codebeispiel Map [Drive to Drive Letter Using the Win32 \_ DiskDrive Interface Type Property](https://Gallery.TechNet.Microsoft.Com/Map-Drive-to-Drive-Letter-1fff91ad) ordnet ein Laufwerk einem Laufwerkbuchstaben zu.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**CIM \_ DiskDrive**](cim-diskdrive.md)
</dt> <dt>

[Hardwareklassen des Computersystems](computer-system-hardware-classes.md)
</dt> <dt>

[WMI-Aufgaben: Datenträger und Dateisysteme](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems)
</dt> </dl>

 

