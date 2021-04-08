---
description: Eine Abstraktion oder Emulation einer Hardware Entität, die auf physischer Hardware basieren kann oder nicht.
ms.assetid: e31c82ed-2da2-4a18-a55e-16931d74f243
title: CIM_LogicalDevice-Klasse (Hyper-V-Verwaltung)
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
ms.openlocfilehash: 471b10f8d3c8640cfcc4277d0151bdd46d59db86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749656"
---
# <a name="cim_logicaldevice-class-hyper-v-management"></a>CIM_LogicalDevice-Klasse (Hyper-V-Verwaltung)

Eine Abstraktion oder Emulation einer Hardware Entität, die auf physischer Hardware basieren kann oder nicht.

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

Die **CIM \_ LogicalDevice** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **CIM \_ LogicalDevice** -Klasse verfügt über diese Methoden.



| Methode                                                           | BESCHREIBUNG                                                                                                                                                                                                                              |
|:-----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnableDevice**](cim-logicaldevice-enabledevice.md)           | Diese Methode ist als veraltet markiert. Verwenden Sie stattdessen die **requestStateChange** -Methode.<br/> **Veraltete Beschreibung:** Aktiviert oder deaktiviert das logische Gerät.<br/>                                                                     |
| [**Onlinedevice**](cim-logicaldevice-onlinedevice.md)           | Diese Methode ist als veraltet markiert. Verwenden Sie stattdessen die **requestStateChange** -Methode.<br/> **Veraltete Beschreibung:** Schaltet das logische Gerät online, damit es Anforderungen akzeptieren oder offline schalten kann, sodass keine Anforderungen mehr akzeptiert werden können.<br/> |
| [**Inaktiven Geräte**](cim-logicaldevice-quiescedevice.md)         | Diese Methode ist als veraltet markiert. Verwenden Sie stattdessen die **requestStateChange** -Methode.<br/> **Veraltete Beschreibung:** Hält die Aktivität vorübergehend auf dem logischen Gerät an oder aktiviert die Aktivität erneut.<br/>                            |
| [**Zurücksetzen**](cim-logicaldevice-reset.md)                         | Setzt das logische Gerät zurück.<br/>                                                                                                                                                                                                    |
| [**Restoreproperties**](cim-logicaldevice-restoreproperties.md) | Stellt eine vorherige Konfiguration und den Status des logischen Geräts wieder her.<br/>                                                                                                                                                            |
| [**SaveProperties**](cim-logicaldevice-saveproperties.md)       | Speichert die Konfiguration und den Status des logischen Geräts.<br/>                                                                                                                                                                      |
| [**SetPowerState**](cim-logicaldevice-setpowerstate.md)         | Diese Methode ist als veraltet markiert. Verwenden Sie stattdessen die **SetPowerState** -Eigenschaft der **CIM- \_ powermanagementservice** -Klasse.<br/> **Veraltete Beschreibung:** Legt den Energiezustand des logischen Geräts fest.<br/>                       |



 

### <a name="properties"></a>Eigenschaften

Die **CIM \_ LogicalDevice** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Additionalavailability**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ LogicalDevice**.**Verfügbarkeit**")
</dt> </dl>

Ein Array, das neben dem der **Verfügbarkeits** Eigenschaft Verfügbarkeitsinformationen über das logische Gerät enthält.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (2)


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

**Running/Full Power** (3)


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

**Warnung** (4)


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

**In Test** (5)


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**Nicht zutreffend** (6)


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

**Ausschalten** (7)


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

**Offline** (8)


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

**Off-Duty** (9)


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

Herunter **gestuft (10** )


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

**Nicht installiert** (11)


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

**Installationsfehler** (12)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

**Energiespeicher-unbekannt** (13)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

**Energiesparmodus-niedriger Energie Modus** (14)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

**Energiesparmodus-Standby** (15)


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

**Energie Zyklen** (16)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

**Energiespar Speicher-Warnung** (17)


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

**Angeh** alten (18)


</dt> <dd></dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

**Nicht bereit** (19)


</dt> <dd></dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

**Nicht konfiguriert** (20)


</dt> <dd></dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

Inaktiven **Status (21** )


</dt> <dd></dd> </dl>

</dd> <dt>

**Verfügbarkeit**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Betriebsstatus \| 006,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus "," MIF. DMTF- \| Host Gerät \| 001,5 "), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ LogicalDevice**.**Additionalavailability**")
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

**Running/Full Power** (3)


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

**Warnung** (4)


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

**In Test** (5)


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**Nicht zutreffend** (6)


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

**Ausschalten** (7)


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

**Offline** (8)


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

**Off-Duty** (9)


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

Herunter **gestuft (10** )


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

**Nicht installiert** (11)


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

**Installationsfehler** (12)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

**Energiespeicher-unbekannt** (13)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

**Energiesparmodus-niedriger Energie Modus** (14)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

**Energiesparmodus-Standby** (15)


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

**Energie Zyklen** (16)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

**Energiespar Speicher-Warnung** (17)


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

**Angeh** alten (18)


</dt> <dd></dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

**Nicht bereit** (19)


</dt> <dd></dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

**Nicht konfiguriert** (20)


</dt> <dd></dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

Inaktiven **Status (21** )


</dt> <dd></dd> </dl>

</dd> <dt>

**"Name der Klassenname"**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Der Klassenname, der zum Erstellen einer Instanz des logischen Geräts verwendet wird. " **Kreationclassname** " wird mit anderen Schlüsseleigenschaften dieser Klasse kombiniert, um Instanzen dieser Klasse und ihrer Unterklassen eindeutig zu identifizieren.

</dd> <dt>

**DeviceID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Ein eindeutiger Bezeichner des logischen Geräts, z. b. die Adresse.

</dd> <dt>

**Errorgelöscht**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)".**OperationalStatus**")
</dt> </dl>

Diese Eigenschaft ist veraltet. Verwenden Sie stattdessen die Eigenschaft **OperationalStatus** aus der **CIM \_ ManagedSystemElement** -Klasse.

**Veraltete Beschreibung:** Gibt an, ob ein von der **LastErrorCode** -Eigenschaft gemeldeter Fehler gelöscht wird.

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ deviceerrordata. ErrorDescription")
</dt> </dl>

Diese Eigenschaft ist veraltet. Verwenden Sie stattdessen die **ErrorDescription** -Eigenschaft aus der **CIM \_ deviceerrordata** -Klasse.

**Veraltete Beschreibung:** Zusätzliche Informationen über den Fehler, der von der **LastErrorCode** -Eigenschaft gemeldet wird.

</dd> <dt>

**IdentifyingDescriptions**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ LogicalDevice**.**"OtherIdentifyingInfo**")
</dt> </dl>

Ein Array von Zeichen folgen, die die " **OtherIdentifyingInfo** "-Array Elemente desselben Indexes beschreiben.

</dd> <dt>

**LastErrorCode**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ deviceerrordata. LastErrorCode")
</dt> </dl>

Diese Eigenschaft ist veraltet. Stattdessen verwenden wir die Eigenschaft " **LastErrorCode** " aus der **CIM \_ deviceerrordata** -Klasse.

**Veraltete Beschreibung:** Der letzte vom logischen Gerät gemeldete Fehlercode.

</dd> <dt>

**Maxquiescetime**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("kein Wert"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Millisekunden")
</dt> </dl>

Diese Eigenschaft ist veraltet und sollte nicht verwendet werden.

**Veraltete Beschreibung:** Die maximale Zeit in Millisekunden, die ein Gerät in einem temporär deaktivierten Zustand verbleiben kann (**Availability** und **additionalavailability** -Eigenschaften sind auf "21" festgelegt). Der Wert "0" gibt an, dass das logische Gerät unbegrenzt in einem temporär deaktivierten Zustand bleiben kann.

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ LogicalDevice**.**Identifyingbeschreibungen**")
</dt> </dl>

Informationen, die das logische Gerät außer der **DeviceID** identifizieren.

</dd> <dt>

**Powermanagementfunktionen**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ powermanagementfunktionalitäten. Power-Funktionen")
</dt> </dl>

Diese Eigenschaft ist veraltet. Verwenden Sie stattdessen die **CIM- \_ powermanagementfunktionalitäten** -Klasse.

**Veraltete Beschreibung:** Ein Array, das die Energie Verwaltungsfunktionen des Geräts enthält.

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

**Automatisch eingegebene Energiespar Modi** (4)


</dt> <dd></dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

**Einsetzbaren Energiezustand** (5)


</dt> <dd></dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

**Unterstützung für Power Cycling** (6)


</dt> <dd></dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

**Unterstützte Unterstützung** (7)


</dt> <dd></dd> </dl>

</dd> <dt>

**Powermanagementsupported**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ powermanagementfunktionalitäten")
</dt> </dl>

Diese Eigenschaft ist veraltet. Verwenden Sie stattdessen die **powermanagementfunktionalitäten** -Klasse.

**Veraltete Beschreibung: true** , wenn das logische Gerät Energie gesteuert werden kann. andernfalls **false**.

</dd> <dt>

**Poweronhours**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Stunden"), **Counter**
</dt> </dl>

Die Anzahl der aufeinanderfolgenden Stunden, die das logische Gerät seit dem letzten Strom Umgebung eingeschaltet wurde.

</dd> <dt>

**StatusInfo**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM \_ enabledlogicalelement**](cim-enabledlogicalelement.md).**Enabledstate**"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF ". \|Betriebsstatus DMTF \| 006,4 ")
</dt> </dl>

Diese Eigenschaft ist veraltet. Verwenden Sie stattdessen die **CIM- \_ powermanagementfunktionalitäten** -Klasse.

**Veraltete Beschreibung:** Gibt an, ob das logische Gerät aktiviert ist oder sich in einem verknüpften Zustand befindet.

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

**Systemkreationclassname**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagierter**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**")
</dt> </dl>

Der Klassenname, der zum Erstellen einer Instanz des Systems verwendet wird, das das logische Gerät enthält. **Systemkreationclassname** wird mit anderen Schlüsseleigenschaften dieser Klasse kombiniert, um Instanzen dieser Klasse und ihrer Unterklassen eindeutig zu identifizieren.

</dd> <dt>

**Systemname**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagierter**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM- \_ System**](cim-system.md).**Name**")
</dt> </dl>

Der Name des Systems, das das logische Gerät enthält.

</dd> <dt>

**Totalpoweronhours**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Stunden"), **Counter**
</dt> </dl>

Die Gesamtzahl der Stunden, die das logische Gerät eingeschaltet wurde.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ enabledlogicalelement**](cim-enabledlogicalelement.md)
</dt> </dl>

 

