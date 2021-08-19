---
description: Eine Abstraktion oder Emulation einer Hardwareentität, die möglicherweise auf physischer Hardware basiert.
ms.assetid: e31c82ed-2da2-4a18-a55e-16931d74f243
title: CIM_LogicalDevice -Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice
- CIM_LogicalDevice.SystemCreationClassName
- CIM_LogicalDevice.SystemName
- CIM_LogicalDevice.CreationClassName
- CIM_LogicalDevice.DeviceID
- CIM_LogicalDevice.PowerManagementSupported
- CIM_LogicalDevice.PowerManagementCapabilities
- CIM_LogicalDevice.Availability
- CIM_LogicalDevice.StatusInfo
- CIM_LogicalDevice.LastErrorCode
- CIM_LogicalDevice.ErrorDescription
- CIM_LogicalDevice.ErrorCleared
- CIM_LogicalDevice.OtherIdentifyingInfo
- CIM_LogicalDevice.PowerOnHours
- CIM_LogicalDevice.TotalPowerOnHours
- CIM_LogicalDevice.IdentifyingDescriptions
- CIM_LogicalDevice.AdditionalAvailability
- CIM_LogicalDevice.MaxQuiesceTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0831bff996721a170da105c800e670cf10cb4b422869062014ab4df9e2441416
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117812115"
---
# <a name="cim_logicaldevice-class-hyper-v-management"></a>CIM_LogicalDevice -Klasse (Hyper-V-Verwaltung)

Eine Abstraktion oder Emulation einer Hardwareentität, die möglicherweise auf physischer Hardware basiert.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, Version("2.8.0"), UMLPackagePath("CIM::Core::Device"), AMENDMENT]
class CIM_LogicalDevice : CIM_EnabledLogicalElement
{
  string  SystemCreationClassName;
  string  SystemName;
  string  CreationClassName;
  string  DeviceID;
  boolean PowerManagementSupported;
  uint16  PowerManagementCapabilities[];
  uint16  Availability;
  uint16  StatusInfo;
  uint32  LastErrorCode;
  string  ErrorDescription;
  boolean ErrorCleared;
  string  OtherIdentifyingInfo[];
  uint64  PowerOnHours;
  uint64  TotalPowerOnHours;
  string  IdentifyingDescriptions[];
  uint16  AdditionalAvailability[];
  uint64  MaxQuiesceTime;
};
```

## <a name="members"></a>Member

Die **CIM \_ LogicalDevice-Klasse** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **CIM \_ LogicalDevice-Klasse** verfügt über diese Methoden.



| Methode                                                           | Beschreibung                                                                                                                                                                                                                              |
|:-----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnableDevice**](cim-logicaldevice-enabledevice.md)           | Diese Methode ist als veraltet markiert. Verwenden Sie stattdessen die **RequestStateChange-Methode.**<br/> **Veraltete Beschreibung:** Aktiviert oder deaktiviert das logische Gerät.<br/>                                                                     |
| [**OnlineDevice**](cim-logicaldevice-onlinedevice.md)           | Diese Methode ist als veraltet markiert. Verwenden Sie stattdessen die **RequestStateChange-Methode.**<br/> **Veraltete Beschreibung:** Schalten Sie das logische Gerät online, damit es Anforderungen annehmen kann, oder offline, damit es keine Anforderungen mehr akzeptieren kann.<br/> |
| [**QuiesceDevice**](cim-logicaldevice-quiescedevice.md)         | Diese Methode ist als veraltet markiert. Verwenden Sie stattdessen die **RequestStateChange-Methode.**<br/> **Veraltete Beschreibung:** Setzt die Aktivität auf dem logischen Gerät vorübergehend aus oder aktiviert die Aktivität erneut.<br/>                            |
| [**Zurücksetzen**](cim-logicaldevice-reset.md)                         | Setzt das logische Gerät zurück.<br/>                                                                                                                                                                                                    |
| [**RestoreProperties**](cim-logicaldevice-restoreproperties.md) | Stellt eine vorherige Konfiguration und den Zustand des logischen Geräts wieder auf.<br/>                                                                                                                                                            |
| [**SaveProperties**](cim-logicaldevice-saveproperties.md)       | Speichert die Konfiguration und den Status des logischen Geräts.<br/>                                                                                                                                                                      |
| [**SetPowerState**](cim-logicaldevice-setpowerstate.md)         | Diese Methode ist als veraltet markiert. Verwenden Sie stattdessen die **SetPowerState-Eigenschaft** der **CIM \_ PowerManagementService-Klasse.**<br/> **Veraltete Beschreibung:** Legt den Energiezustand des logischen Geräts fest.<br/>                       |



 

### <a name="properties"></a>Eigenschaften

Die **CIM \_ LogicalDevice-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**AdditionalAvailability**
</dt> <dd> <dl> <dt>

Datentyp: **uint16 array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ LogicalDevice**.**Verfügbarkeit**")
</dt> </dl>

Ein Array, das zusätzlich zur Verfügbarkeitseigenschaft Verfügbarkeitsinformationen zum logischen **Gerät** enthält.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (2)


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

**Wird ausgeführt/Vollstrom** (3)


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

**Warnung** (4)


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

**Im Test** (5)


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**Nicht zutreffend** (6)


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

**Ausschalten** (7)


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

**Off Line** (8)


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

**Off-Off-Dienst** (9)


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Heruntergestuft** (10)


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

**Nicht installiert** (11)


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

**Installationsfehler** (12)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

**Energiesparen – Unbekannt** (13)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

**Stromsparen – Modus mit geringer Leistung** (14)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

**Energiesparen – Standby** (15)


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

**Energiezyklus** (16)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

**Energiesparen – Warnung** (17)


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

**Angehalten** (18)


</dt> <dd></dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

**Nicht bereit** (19)


</dt> <dd></dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

**Nicht konfiguriert** (20)


</dt> <dd></dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

**Ruhen** (21)


</dt> <dd></dd> </dl>

</dd> <dt>

**Verfügbarkeit**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Operational State \| 006.5", "MIB. IETF \| HOST-RESOURCES-MIB.hrDeviceStatus", "MIF. DMTF \| Host Device \| 001.5"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ LogicalDevice**.**AdditionalAvailability**")
</dt> </dl>

Enthält die Verfügbarkeit des logischen Geräts.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (2)


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

**Wird ausgeführt/Vollstrom** (3)


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

**Warnung** (4)


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

**Im Test** (5)


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**Nicht zutreffend** (6)


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

**Ausschalten** (7)


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

**Off Line** (8)


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

**Off-Off-Dienst** (9)


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Heruntergestuft** (10)


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

**Nicht installiert** (11)


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

**Installationsfehler** (12)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

**Energiesparen – Unbekannt** (13)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

**Stromsparen – Modus mit geringer Leistung** (14)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

**Energiesparen – Standby** (15)


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

**Energiezyklus** (16)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

**Energiesparen – Warnung** (17)


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

**Angehalten** (18)


</dt> <dd></dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

**Nicht bereit** (19)


</dt> <dd></dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

**Nicht konfiguriert** (20)


</dt> <dd></dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

**Ruhen** (21)


</dt> <dd></dd> </dl>

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Der Klassenname, der zum Erstellen einer Instanz des logischen Geräts verwendet wird. **CreationClassName** wird mit anderen Schlüsseleigenschaften dieser Klasse kombiniert, um Instanzen dieser Klasse und ihrer Unterklassen eindeutig zu identifizieren.

</dd> <dt>

**Deviceid**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Ein eindeutiger Bezeichner des logischen Geräts, z. B. die Adresse.

</dd> <dt>

**ErrorCleared**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).**OperationalStatus**")
</dt> </dl>

Diese Eigenschaft ist veraltet. Verwenden Sie stattdessen die **OperationalStatus-Eigenschaft** aus der **CIM \_ ManagedSystemElement-Klasse.**

**Veraltete Beschreibung:** Gibt an, ob ein von der **LastErrorCode-Eigenschaft** gemeldeter Fehler gelöscht wird.

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ DeviceErrorData.ErrorDescription")
</dt> </dl>

Diese Eigenschaft ist veraltet. Verwenden Sie stattdessen die **ErrorDescription-Eigenschaft** aus der **CIM \_ DeviceErrorData-Klasse.**

**Veraltete Beschreibung:** Zusätzliche Informationen zu dem von der **LastErrorCode-Eigenschaft** gemeldeten Fehler.

</dd> <dt>

**IdentifyingDescriptions**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ LogicalDevice**.**OtherIdentifyingInfo**")
</dt> </dl>

Ein Array von Zeichenfolgen, die die **OtherIdentifyingInfo-Arrayelemente** desselben Indexes beschreiben.

</dd> <dt>

**LastErrorCode**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ DeviceErrorData.LastErrorCode")
</dt> </dl>

Diese Eigenschaft ist veraltet. Stattdessen verwenden wir die **LastErrorCode-Eigenschaft** aus der **CIM \_ DeviceErrorData-Klasse.**

**Veraltete Beschreibung:** Der letzte vom logischen Gerät gemeldete Fehlercode.

</dd> <dt>

**MaxQuiesceTime**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("Kein Wert"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("MilliSeconds")
</dt> </dl>

Diese Eigenschaft ist veraltet und sollte nicht verwendet werden.

**Veraltete Beschreibung:** Die maximale Zeit in Millisekunden, die ein Gerät in einem vorübergehend deaktivierten Zustand verbleiben kann (**Verfügbarkeits-** und **AdditionalAvailability-Eigenschaften** sind auf "21" ruhend) festgelegt. Der Wert "0" gibt an, dass das logische Gerät auf unbestimmte Zeit in einem vorübergehend deaktivierten Zustand verbleiben kann.

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indiziert"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ LogicalDevice**.**IdentifyingDescriptions**")
</dt> </dl>

Informationen, die das logische Gerät außer **DeviceID** identifizieren.

</dd> <dt>

**PowerManagementCapabilities**
</dt> <dd> <dl> <dt>

Datentyp: **uint16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ PowerManagementCapabilities.PowerCapabilities")
</dt> </dl>

Diese Eigenschaft ist veraltet. Verwenden Sie stattdessen die **CIM \_ PowerManagementCapabilities-Klasse.**

**Veraltete Beschreibung:** Ein Array, das die Energieverwaltungsfunktionen des Geräts enthält.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

**Nicht unterstützt** (1)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Deaktiviert** (2)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Aktiviert** (3)


</dt> <dd></dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

**Automatisch eingegebene Energiesparmodi** (4)


</dt> <dd></dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

**Power State Settable** (5)


</dt> <dd></dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

**PowerCycling unterstützt** (6)


</dt> <dd></dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

Timed Power On Supported (7) **(Zeitiertes Einschalten unterstützt** (7)


</dt> <dd></dd> </dl>

</dd> <dt>

**PowerManagementSupported**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ PowerManagementCapabilities")
</dt> </dl>

Diese Eigenschaft ist veraltet. Verwenden Sie stattdessen die **PowerManagementCapabilities-Klasse.**

**Veraltete Beschreibung: TRUE,** wenn das logische Gerät mit Strom verwaltet werden kann. andernfalls **FALSE.**

</dd> <dt>

**PowerOnHours**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Stunden"), **Indikator**
</dt> </dl>

Die Anzahl der aufeinanderfolgenden Stunden, die das logische Gerät seit dem letzten Energiesparzyklus eingeschaltet hat.

</dd> <dt>

**StatusInfo**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md).**EnabledState**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Operational State \| 006.4")
</dt> </dl>

Diese Eigenschaft ist veraltet. Verwenden Sie stattdessen die **CIM \_ PowerManagementCapabilities-Klasse.**

**Veraltete Beschreibung:** Gibt an, ob das logische Gerät aktiviert ist oder sich in einem verknüpften Zustand befindet.

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

Qualifizierer: [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**weitergegeben**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ CIM-System**](cim-system.md).**CreationClassName**")
</dt> </dl>

Der Klassenname, der zum Erstellen einer Instanz des Systems verwendet wird, das das logische Gerät enthält. **SystemCreationClassName** wird mit anderen Schlüsseleigenschaften dieser Klasse kombiniert, um Instanzen dieser Klasse und deren Unterklassen eindeutig zu identifizieren.

</dd> <dt>

**Systemname**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**weitergegeben**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ CIM-System**](cim-system.md).**Name**")
</dt> </dl>

Der Name des Systems, das das logische Gerät enthält.

</dd> <dt>

**TotalPowerOnHours**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Stunden"), **Indikator**
</dt> </dl>

Die Gesamtzahl der Stunden, in der das logische Gerät eingeschaltet wurde.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Root-Virtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md)
</dt> </dl>

 

