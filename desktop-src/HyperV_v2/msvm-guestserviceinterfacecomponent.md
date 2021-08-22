---
description: Stellt den Zustand der Gastdienstschnittstellenkomponente dar, die einen Mechanismus für die Interaktion mit dem virtuellen Computer über die Verwaltungsschnittstellen auf dem Hostsystem bereitstellt.
ms.assetid: 9A158B42-052B-42B3-8539-00927056306D
title: Msvm_GuestServiceInterfaceComponent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestServiceInterfaceComponent
- Msvm_GuestServiceInterfaceComponent.Availability
- Msvm_GuestServiceInterfaceComponent.Caption
- Msvm_GuestServiceInterfaceComponent.ConfigManagerErrorCode
- Msvm_GuestServiceInterfaceComponent.ConfigManagerUserConfig
- Msvm_GuestServiceInterfaceComponent.CreationClassName
- Msvm_GuestServiceInterfaceComponent.Description
- Msvm_GuestServiceInterfaceComponent.DeviceID
- Msvm_GuestServiceInterfaceComponent.ErrorCleared
- Msvm_GuestServiceInterfaceComponent.ErrorDescription
- Msvm_GuestServiceInterfaceComponent.InstallDate
- Msvm_GuestServiceInterfaceComponent.LastErrorCode
- Msvm_GuestServiceInterfaceComponent.Name
- Msvm_GuestServiceInterfaceComponent.PNPDeviceID
- Msvm_GuestServiceInterfaceComponent.PowerManagementCapabilities
- Msvm_GuestServiceInterfaceComponent.PowerManagementSupported
- Msvm_GuestServiceInterfaceComponent.Status
- Msvm_GuestServiceInterfaceComponent.StatusInfo
- Msvm_GuestServiceInterfaceComponent.SystemCreationClassName
- Msvm_GuestServiceInterfaceComponent.SystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c7e404a1195332b508de22fc0a26dfebb96eba29f487f08505987edcc72b6cec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119523020"
---
# <a name="msvm_guestserviceinterfacecomponent-class"></a>Msvm \_ GuestServiceInterfaceComponent-Klasse

Stellt den Zustand der Gastdienstschnittstellenkomponente dar, die einen Mechanismus für die Interaktion mit dem virtuellen Computer über die Verwaltungsschnittstellen auf dem Hostsystem bereitstellt. Diese Klasse wird von der [**CIM \_ LogicalDevice-Klasse**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) abgeleitet.

Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestServiceInterfaceComponent : CIM_LogicalDevice
{
  uint16   Availability;
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
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a>Member

Die **Msvm \_ GuestServiceInterfaceComponent-Klasse** verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Msvm \_ GuestServiceInterfaceComponent-Klasse** verfügt über diese Methoden.



| Methode                                                                               | Beschreibung                                                                                                                              |
|:-------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [**RequestStateChange**](requeststatechange-msvm-guestserviceinterfacecomponent.md) | Fordert an, dass der Zustand der Gastdienstschnittstellenkomponente in den angegebenen Wert geändert wird.<br/>                           |
| [**Zurücksetzen**](/windows/desktop/CIMWin32Prov/reset-method-in-class-cim-logicaldevice)                        | Fordert eine Zurücksetzung des logischen Geräts an. Nicht von WMI implementiert.<br/>                                                               |
| [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-logicaldevice)        | Definiert den gewünschten Energiezustand für ein logisches Gerät und wann ein Gerät in diesen Zustand versetzt werden soll. Nicht von WMI implementiert.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ GuestServiceInterfaceComponent-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Verfügbarkeit**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verfügbarkeit und Status des Geräts.



| Wert                                                                                                                                                                                                                                                                                                              | Bedeutung                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <dt>**Andere**</dt> <dt>1 (0x1)</dt> </dl>                                                                                          |                                                                                                             |
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Unbekannt**</dt> <dt>2 (0x2)</dt> </dl>                                                                                  |                                                                                                             |
| <span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span><dl> <dt>**Running/Full Power 3 (0x3) (Ausführen/Vollständiges Power**</dt> <dt>3(0x3))</dt> </dl>                                      |                                                                                                             |
| <span id="Warning"></span><span id="warning"></span><span id="WARNING"></span><dl> <dt>**Warnung**</dt> <dt>4 (0x4)</dt> </dl>                                                                                  |                                                                                                             |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <dt>**In Test**</dt> <dt>5 (0x5)</dt> </dl>                                                                                  |                                                                                                             |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <dt>**Nicht zutreffend**</dt> <dt>6 (0x6)</dt> </dl>                                                      |                                                                                                             |
| <span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span><dl> <dt>**Ausschalten**</dt> <dt>7 (0x7)</dt> </dl>                                                                          |                                                                                                             |
| <span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span><dl> <dt>**Off Line**</dt> <dt>8 (0x8)</dt> </dl>                                                                              |                                                                                                             |
| <span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span><dl> <dt>**Off Duty**</dt> <dt>9 (0x9)</dt> </dl>                                                                              |                                                                                                             |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <dt>**Heruntergestuft**</dt> <dt>10 (0xA)</dt> </dl>                                                                             |                                                                                                             |
| <span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span><dl> <dt>**Nicht installiert**</dt> <dt>11 (0xB)</dt> </dl>                                                         |                                                                                                             |
| <span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span><dl> <dt>**Installationsfehler**</dt> <dt>12 (0xC)</dt> </dl>                                                         |                                                                                                             |
| <span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span><dl> <dt>**Energiesparen – Unbekannt**</dt> <dt>13 (0xD)</dt> </dl>                             | Das Gerät befindet sich bekanntermaßen im Energiesparmodus, aber sein genauer Status ist unbekannt.<br/>                 |
| <span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span><dl> <dt>**Energiesparmodus**</dt> <dt>14 (0xE)</dt> </dl> | Das Gerät befindet sich im Energiesparzustand, funktioniert aber weiterhin und kann eine beeinträchtigte Leistung aufweisen.<br/> |
| <span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span><dl> <dt>**Energiesparmodus**</dt> – Standby <dt>15 (0xF)</dt> </dl>                             | Das Gerät funktioniert nicht, kann aber schnell voll ausgepowert werden.<br/>                        |
| <span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span><dl> <dt>**Leistungszyklus**</dt> <dt>16 (0x10)</dt> </dl>                                                                |                                                                                                             |
| <span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span><dl> <dt>**Energiesparen – Warnung**</dt> <dt>17 (0x11)</dt> </dl>                            | Das Gerät befindet sich in einem Warnungszustand, aber auch im Energiesparmodus.<br/>                              |



 

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Kurze Textbeschreibung des Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**ConfigManagerErrorCode**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Win32 Konfigurations-Manager Fehlercode.



| Wert                                                                                | Bedeutung                                                                                                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl>   | Das Gerät funktioniert ordnungsgemäß.<br/>                                                                                                   |
| <dl> <dt>1 (0x1)</dt> </dl>   | Das Gerät ist nicht ordnungsgemäß konfiguriert.<br/>                                                                                           |
| <dl> <dt>2 (0x2)</dt> </dl>   | Windows kann den Treiber für dieses Gerät nicht laden.<br/>                                                                               |
| <dl> <dt>3 (0x3)</dt> </dl>   | Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.<br/>                             |
| <dl> <dt>4 (0x4)</dt> </dl>   | Das Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.<br/>                                        |
| <dl> <dt>5 (0x5)</dt> </dl>   | Der Treiber für das Gerät erfordert eine Ressource, die Windows nicht verwalten können.<br/>                                                         |
| <dl> <dt>6 (0x6)</dt> </dl>   | Bei der Startkonfiguration für das Gerät tritt ein Konflikt mit anderen Geräten auf.<br/>                                                               |
| <dl> <dt>7 (0x7)</dt> </dl>   | Kann nicht gefiltert werden.<br/>                                                                                                                |
| <dl> <dt>8 (0x8)</dt> </dl>   | Das Treiberladeprogramm für das Gerät fehlt.<br/>                                                                                      |
| <dl> <dt>9 (0x9)</dt> </dl>   | Das Gerät funktioniert nicht ordnungsgemäß. die steuernde Firmware meldet fälschlicherweise die Ressourcen für das Gerät.<br/>               |
| <dl> <dt>10 (0xA)</dt> </dl>  | Das Gerät kann nicht gestartet werden.<br/>                                                                                                          |
| <dl> <dt>11 (0xB)</dt> </dl>  | Fehler beim Gerät.<br/>                                                                                                                |
| <dl> <dt>12 (0xC)</dt> </dl>  | Das Gerät kann nicht genügend freie Ressourcen für die Verwendung finden.<br/>                                                                              |
| <dl> <dt>13 (0xD)</dt> </dl>  | Windows können die Ressourcen des Geräts nicht überprüfen.<br/>                                                                                 |
| <dl> <dt>14 (0xE)</dt> </dl>  | Das Gerät kann erst ordnungsgemäß funktionieren, wenn der Computer neu gestartet wurde.<br/>                                                                  |
| <dl> <dt>15 (0xF)</dt> </dl>  | Das Gerät funktioniert aufgrund eines möglichen Problems mit der erneuten Enumeration nicht ordnungsgemäß.<br/>                                                      |
| <dl> <dt>16 (0x10)</dt> </dl> | Windows können nicht alle Ressourcen identifizieren, die das Gerät verwendet.<br/>                                                            |
| <dl> <dt>17 (0x11)</dt> </dl> | Das Gerät fordert einen unbekannten Ressourcentyp an.<br/>                                                                                |
| <dl> <dt>18 (0x12)</dt> </dl> | Gerätetreiber müssen neu installiert werden.<br/>                                                                                           |
| <dl> <dt>19 (0x13)</dt> </dl> | Fehler beim Verwenden des VxD-Ladeprogramm.<br/>                                                                                                 |
| <dl> <dt>20 (0x14)</dt> </dl> | Die Registrierung ist möglicherweise beschädigt.<br/>                                                                                                  |
| <dl> <dt>21 (0x15)</dt> </dl> | Systemfehler. Wenn das Ändern des Gerätetreibers ineffektiv ist, lesen Sie die Hardwaredokumentation. Windows entfernt das Gerät.<br/> |
| <dl> <dt>22 (0x16)</dt> </dl> | Das Gerät ist deaktiviert.<br/>                                                                                                           |
| <dl> <dt>23 (0x17)</dt> </dl> | Systemfehler. Wenn das Ändern des Gerätetreibers ineffektiv ist, lesen Sie die Hardwaredokumentation.<br/>                                 |
| <dl> <dt>24 (0x18)</dt> </dl> | Das Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß oder verfügt nicht über alle installierten Treiber.<br/>                                   |
| <dl> <dt>25 (0x19)</dt> </dl> | Windows richtet das Gerät noch ein.<br/>                                                                                       |
| <dl> <dt>26 (0x1A)</dt> </dl> | Windows richtet das Gerät noch ein.<br/>                                                                                       |
| <dl> <dt>27 (0x1B)</dt> </dl> | Das Gerät verfügt nicht über eine gültige Protokollkonfiguration.<br/>                                                                                 |
| <dl> <dt>28 (0x1C)</dt> </dl> | Gerätetreiber sind nicht installiert.<br/>                                                                                             |
| <dl> <dt>29 (0x1D)</dt> </dl> | Das Gerät ist deaktiviert. Die Gerätefirmware hat nicht die erforderlichen Ressourcen bereitgestellt.<br/>                                               |
| <dl> <dt>30 (0x1E)</dt> </dl> | Das Gerät verwendet eine IRQ-Ressource, die von einem anderen Gerät verwendet wird.<br/>                                                                 |
| <dl> <dt>31 (0x1F)</dt> </dl> | Das Gerät funktioniert nicht ordnungsgemäß. Windows können die erforderlichen Gerätetreiber nicht laden.<br/>                                              |



 

</dd> <dt>

**ConfigManagerUserConfig**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird. Bei Verwendung mit anderen Schlüsseleigenschaften der -Klasse ermöglicht diese Eigenschaft die eindeutige Identifizierung aller Instanzen der -Klasse und ihrer Unterklassen.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Textbeschreibung des Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**Deviceid**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Adresse oder andere identifizierende Informationen, um dem logischen Gerät einen eindeutigen Namen zu geben.

</dd> <dt>

**ErrorCleared**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

True gibt an, dass der in der **LastErrorCode-Eigenschaft** gemeldete Fehler jetzt gelöscht wird.

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Freiformzeichenfolge, die Informationen über den in der **LastErrorCode-Eigenschaft** aufgezeichneten Fehler und die auszuführenden Korrekturmaßnahmen enthält.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Datum und Uhrzeit der Installation des Objekts. Diese Eigenschaft benötigt keinen Wert, um anzugeben, dass das Objekt installiert ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**LastErrorCode**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der letzte vom logischen Gerät gemeldete Fehlercode.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Bezeichnung, mit der das Objekt bekannt ist. Bei Einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**PNPDeviceID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den Win32-Plug & Play Gerätebezeichner des logischen Geräts an.

Beispiel: \* "PNP030b"

</dd> <dt>

**PowerManagementCapabilities**
</dt> <dd> <dl> <dt>

Datentyp: **uint16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Array der spezifischen energiebezogenen Funktionen eines logischen Geräts. Diese Eigenschaft wird von **CIM \_ LogicalDevice** geerbt.



| Wert                                                                                                                                                                                                                                                                                                                                                                 | Bedeutung                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Unbekannt**</dt> <dt>0 (0x0)</dt> </dl>                                                                                                                                     |                                                                                                                                                                                                                                                                                                                                      |
| <span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span><dl> <dt>**Nicht unterstützt**</dt> <dt>1 (0x1)</dt> </dl>                                                                                                             |                                                                                                                                                                                                                                                                                                                                      |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <dt>**Deaktiviert**</dt> <dt>2 (0x2)</dt> </dl>                                                                                                                                 |                                                                                                                                                                                                                                                                                                                                      |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <dt>**Aktiviert**</dt> <dt>3 (0x3)</dt> </dl>                                                                                                                                     | Die Energieverwaltungsfunktionen sind derzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.<br/>                                                                                                                                                                                               |
| <span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span><dl> <dt>**Automatisch eingegebene Energiesparmodi**</dt> <dt>4 (0x4)</dt> </dl> | Das Gerät kann seinen Energiezustand basierend auf der Nutzung oder anderen Kriterien ändern.<br/>                                                                                                                                                                                                                                                   |
| <span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span><dl> <dt>**Power State Settable**</dt> <dt>5 (0x5)</dt> </dl>                                                                                 | Die [**SetPowerState-Methode**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) wird unterstützt. Diese Methode befindet sich in der übergeordneten **CIM \_ LogicalDevice-Klasse** und kann implementiert werden. Weitere Informationen finden Sie unter [Entwerfen von MOF-Klassen (Managed Object Format).](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes)<br/> |
| <span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span><dl> <dt>**PowerCycling unterstützt**</dt> <dt>6 (0x6)</dt> </dl>                                                                     | Die [**SetPowerState-Methode**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) kann aufgerufen werden, wobei der *PowerState-Parameter* auf 5 ("Power Cycle") festgelegt ist.<br/>                                                                                                                                                            |
| <span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span><dl> <dt>**Timed Power On Supported**</dt> <dt>7 (0x7)</dt> </dl>                                                                 | Die [**SetPowerState-Methode**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) kann aufgerufen werden, wobei der *PowerState-Parameter* auf 5 ("Power Cycle") und *time* für das Einschalten auf ein bestimmtes Datum und eine bestimmte Uhrzeit oder ein bestimmtes Intervall festgelegt ist.<br/>                                                                                       |



 

</dd> <dt>

**PowerManagementSupported**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

True gibt an, dass das Gerät mit Strom verwaltet werden kann, d.h. in einen Energiesparzustand versetzt werden kann. **False** gibt an, dass der ganzzahlige Wert 1 ("Nicht unterstützt") der einzige Eintrag im **PowerManagementCapabilities-Array** sein sollte.

Diese Eigenschaft gibt nicht an, ob energieverwaltungsfeatures derzeit aktiviert sind oder welche Features unterstützt werden. Weitere Informationen finden Sie im **PowerManagementCapabilities-Array.**

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Aktueller Status des Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

Folgende Werte sind gültig:

<dl><span id="OK"></span><span id="ok"></span><dt>

**"OK"**
</dt><span id="Error"></span><span id="error"></span><span id="ERROR"></span><dt>

**"Fehler"**
</dt><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dt>

**"Heruntergestuft"**
</dt><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dt>

**"Unbekannt"**
</dt><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span><dt>

**"Pred Fail" (Fehler vor dem Fehler)**
</dt><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dt>

**"Starting" (Wird gestartet)**
</dt><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span><dt>

**"Wird beendet"**
</dt><span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dt>

**"Dienst"**
</dt><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span><dt>

**"100"**
</dt><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span><dt>

**"NonRecover"**
</dt><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dt>

**"Kein Kontakt"**
</dt><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span><dt>

**"Lost Comm"**
</dt> </dl>

</dd> <dt>

**StatusInfo**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Status des logischen Geräts. Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 ("Nicht zutreffend") verwendet werden. Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.

<dl> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1 (0x1))
</dt> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2 (0x2))
</dt> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3 (0x3))
</dt> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (4 (0x4))
</dt> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (5 (0x5))
</dt> </dl>

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name der Erstellungsklasse des Bereichssystems.

</dd> <dt>

**Systemname**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Bereichsname des Systems.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Nur Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 Nur \[ R2-Desktop-Apps\]<br/>                                                 |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ LogicalDevice**](cim-logicaldevice.md)
</dt> <dt>

[**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)
</dt> </dl>

 

