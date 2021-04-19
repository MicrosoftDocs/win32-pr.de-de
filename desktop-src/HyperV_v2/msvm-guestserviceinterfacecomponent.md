---
description: Stellt den Status der Komponente der Gast Dienst Schnittstelle dar, die einen Mechanismus zum interagieren mit der virtuellen Maschine über die Verwaltungs Schnittstellen auf dem Host System bereitstellt.
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
ms.openlocfilehash: 4c55417edeee6d9a9fb15c474ba4ee9ca2dd93f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345764"
---
# <a name="msvm_guestserviceinterfacecomponent-class"></a>MSVM \_ guestserviczuterfacecomponent-Klasse

Stellt den Status der Komponente der Gast Dienst Schnittstelle dar, die einen Mechanismus zum interagieren mit der virtuellen Maschine über die Verwaltungs Schnittstellen auf dem Host System bereitstellt. Diese Klasse wird von der [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) -Klasse abgeleitet.

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

Die **MSVM \_ guestserviceinterfacecomponent** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **MSVM \_ guestserviczuterfacecomponent** -Klasse verfügt über diese Methoden.



| Methode                                                                               | BESCHREIBUNG                                                                                                                              |
|:-------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [**RequestStateChange**](requeststatechange-msvm-guestserviceinterfacecomponent.md) | Fordert an, dass der Status der Komponente der Gast Dienst Schnittstelle in den angegebenen Wert geändert wird.<br/>                           |
| [**Zurücksetzen**](/windows/desktop/CIMWin32Prov/reset-method-in-class-cim-logicaldevice)                        | Fordert eine zurück setzung des logischen Geräts an. Wird nicht von WMI implementiert.<br/>                                                               |
| [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-logicaldevice)        | Definiert den gewünschten Energiezustand für ein logisches Gerät und einen Zeitpunkt, zu dem ein Gerät in diesen Zustand versetzt werden soll. Wird nicht von WMI implementiert.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ guestserviczuterfacecomponent** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Verfügbarkeit**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verfügbarkeit und Status des Geräts.



| Wert                                                                                                                                                                                                                                                                                                              | Bedeutung                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <dt>**Sonstige**</dt> <dt>1 (0x1)</dt> </dl>                                                                                          |                                                                                                             |
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Unbekannt**</dt> <dt>2 (0x2)</dt> </dl>                                                                                  |                                                                                                             |
| <span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span><dl> Wird <dt>**ausgeführt/Full Power**</dt> <dt>3 (0x3)</dt> </dl>                                      |                                                                                                             |
| <span id="Warning"></span><span id="warning"></span><span id="WARNING"></span><dl> <dt>**Warnung**</dt> <dt>4 (0x4)</dt> </dl>                                                                                  |                                                                                                             |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <dt>**In Test**</dt> <dt>5 (0x5)</dt> </dl>                                                                                  |                                                                                                             |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <dt>**Nicht zutreffend**</dt> <dt>6 (0x6)</dt> </dl>                                                      |                                                                                                             |
| <span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span><dl> <dt>**Ausschalten von**</dt> <dt>7 (0x7)</dt> </dl>                                                                          |                                                                                                             |
| <span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span><dl> <dt>**Aus Zeile**</dt> <dt>8 (0x8)</dt> </dl>                                                                              |                                                                                                             |
| <span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span><dl> <dt>**Aus Duty**</dt> <dt>9 (0x9)</dt> </dl>                                                                              |                                                                                                             |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <dt></dt> Heruntergestuft <dt>10 (0xa)</dt> </dl>                                                                             |                                                                                                             |
| <span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span><dl> <dt>**Nicht installiert**</dt> <dt>11 (0xB)</dt> </dl>                                                         |                                                                                                             |
| <span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span><dl> <dt>**Installationsfehler**</dt> <dt>12 (0xc)</dt> </dl>                                                         |                                                                                                             |
| <span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span><dl> <dt>**Energie speichern-unbekannt**</dt> <dt>13 (0xD)</dt> </dl>                             | Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.<br/>                 |
| <span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span><dl> <dt>**Energiesparmodus-niedriger Energie Modus**</dt> <dt>14 (0xe)</dt> </dl> | Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch weiterhin und kann eine Beeinträchtigung der Leistung aufweisen.<br/> |
| <span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span><dl> <dt>**Energiesparmodus-Standby**</dt> <dt>15 (0xF)</dt> </dl>                             | Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb versetzt werden.<br/>                        |
| <span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span><dl> <dt>**Power Cycle**</dt> <dt>16 (0x10)</dt> </dl>                                                                |                                                                                                             |
| <span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span><dl> <dt>**Energiespar Speicher-Warnung**</dt> <dt>17 (0x11)</dt> </dl>                            | Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.<br/>                              |



 

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Kurze Textbeschreibung des-Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**Configmanagererrorcode**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Win32-Configuration Manager Fehlercode.



| Wert                                                                                | Bedeutung                                                                                                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl>   | Das Gerät funktioniert ordnungsgemäß.<br/>                                                                                                   |
| <dl> <dt>1 (0x1)</dt> </dl>   | Das Gerät ist nicht ordnungsgemäß konfiguriert.<br/>                                                                                           |
| <dl> <dt>2 (0x2)</dt> </dl>   | Der Treiber für dieses Gerät kann nicht geladen werden.<br/>                                                                               |
| <dl> <dt>3 (0x3)</dt> </dl>   | Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt möglicherweise nicht über genügend Arbeitsspeicher oder andere Ressourcen.<br/>                             |
| <dl> <dt>4 (0x4)</dt> </dl>   | Das Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.<br/>                                        |
| <dl> <dt>5 (0x5)</dt> </dl>   | Der Treiber für das Gerät erfordert eine Ressource, die von Windows nicht verwaltet werden kann.<br/>                                                         |
| <dl> <dt>6 (0x6)</dt> </dl>   | Die Startkonfiguration für das Gerät steht in Konflikt mit anderen Geräten.<br/>                                                               |
| <dl> <dt>7 (0x7)</dt> </dl>   | Kann nicht gefiltert werden.<br/>                                                                                                                |
| <dl> <dt>8 (0x8)</dt> </dl>   | Das Treiber Lade Modul für das Gerät fehlt.<br/>                                                                                      |
| <dl> <dt>9 (0x9)</dt> </dl>   | Das Gerät funktioniert nicht ordnungsgemäß. die Steuerungs Firmware meldet nicht korrekt die Ressourcen für das Gerät.<br/>               |
| <dl> <dt>10 (0xa)</dt> </dl>  | Das Gerät kann nicht gestartet werden.<br/>                                                                                                          |
| <dl> <dt>11 (0xB)</dt> </dl>  | Fehler beim Gerät.<br/>                                                                                                                |
| <dl> <dt>12 (0xc)</dt> </dl>  | Das Gerät kann nicht genug freie Ressourcen für die Verwendung finden.<br/>                                                                              |
| <dl> <dt>13 (0xD)</dt> </dl>  | Die Geräte Ressourcen können nicht überprüft werden.<br/>                                                                                 |
| <dl> <dt>14 (0xe)</dt> </dl>  | Das Gerät kann erst ordnungsgemäß funktionieren, wenn der Computer neu gestartet wird.<br/>                                                                  |
| <dl> <dt>15 (0xF)</dt> </dl>  | Das Gerät funktioniert aufgrund eines möglichen erneuten Aufzählungs Problems nicht ordnungsgemäß.<br/>                                                      |
| <dl> <dt>16 (0x10)</dt> </dl> | In Windows können nicht alle Ressourcen identifiziert werden, die vom Gerät verwendet werden.<br/>                                                            |
| <dl> <dt>17 (0x11)</dt> </dl> | Das Gerät fordert einen unbekannten Ressourcentyp an.<br/>                                                                                |
| <dl> <dt>18 (0x12)</dt> </dl> | Gerätetreiber müssen neu installiert werden.<br/>                                                                                           |
| <dl> <dt>19 (0x13)</dt> </dl> | Fehler bei Verwendung des VXD-Lade Moduls.<br/>                                                                                                 |
| <dl> <dt>20 (0x14)</dt> </dl> | Die Registrierung ist möglicherweise beschädigt.<br/>                                                                                                  |
| <dl> <dt>21 (0x15)</dt> </dl> | System Fehler. Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation. Das Gerät wird von Windows entfernt.<br/> |
| <dl> <dt>22 (0x16)</dt> </dl> | Das Gerät ist deaktiviert.<br/>                                                                                                           |
| <dl> <dt>23 (0x17)</dt> </dl> | System Fehler. Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.<br/>                                 |
| <dl> <dt>24 (0x18)</dt> </dl> | Das Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.<br/>                                   |
| <dl> <dt>25 (0x19)</dt> </dl> | Das Gerät wird weiterhin von Windows eingerichtet.<br/>                                                                                       |
| <dl> <dt>26 (0x1A)</dt> </dl> | Das Gerät wird weiterhin von Windows eingerichtet.<br/>                                                                                       |
| <dl> <dt>27 (0x1B)</dt> </dl> | Das Gerät verfügt nicht über eine gültige Protokoll Konfiguration.<br/>                                                                                 |
| <dl> <dt>28 (0x1C)</dt> </dl> | Gerätetreiber sind nicht installiert.<br/>                                                                                             |
| <dl> <dt>29 (0x1D)</dt> </dl> | Das Gerät ist deaktiviert. die Gerätefirmware hat nicht die erforderlichen Ressourcen bereitgestellt.<br/>                                               |
| <dl> <dt>30 (0x1E)</dt> </dl> | Das Gerät verwendet eine UNQ-Ressource, die von einem anderen Gerät verwendet wird.<br/>                                                                 |
| <dl> <dt>31 (0x1F)</dt> </dl> | Das Gerät funktioniert nicht ordnungsgemäß. Die erforderlichen Gerätetreiber können nicht geladen werden.<br/>                                              |



 

</dd> <dt>

**Configmanageruserconfig**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.

</dd> <dt>

**"Name der Klassenname"**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird. Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Textbeschreibung des Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**DeviceID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Adresse oder andere identifizierende Informationen, um das logische Gerät eindeutig zu benennen.

</dd> <dt>

**Errorgelöscht**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Wenn der Wert **true** ist, wird der in der Eigenschaft **LastErrorCode** gemeldete Fehler nun gelöscht.

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine frei Form Zeichenfolge, die Informationen über den Fehler bereitstellt, der in der **LastErrorCode** -Eigenschaft aufgezeichnet wurde, sowie die auszuführenden Maßnahmen.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Datum und Uhrzeit der Installation des-Objekts. Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**LastErrorCode**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der letzte vom logischen Gerät gemeldete Fehlercode.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Bezeichnung, nach der das-Objekt bekannt ist. Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**PNPDeviceID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den Win32-Plug & Play Geräte Bezeichner des logischen Geräts an.

Beispiel: " \* PNP030b"

</dd> <dt>

**Powermanagementfunktionen**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Array der spezifischen energiebezogenen Funktionen eines logischen Geräts. Diese Eigenschaft wird von **CIM \_ LogicalDevice** geerbt.



| Wert                                                                                                                                                                                                                                                                                                                                                                 | Bedeutung                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Unbekannt**</dt> <dt>0 (0x0)</dt> </dl>                                                                                                                                     |                                                                                                                                                                                                                                                                                                                                      |
| <span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span><dl> <dt>**Nicht unterstützt**</dt> <dt>1 (0x1)</dt> </dl>                                                                                                             |                                                                                                                                                                                                                                                                                                                                      |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <dt>**Deaktiviert**</dt> <dt>2 (0x2)</dt> </dl>                                                                                                                                 |                                                                                                                                                                                                                                                                                                                                      |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <dt>**Aktiviert**</dt> <dt>3 (0x3)</dt> </dl>                                                                                                                                     | Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.<br/>                                                                                                                                                                                               |
| <span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span><dl> Der <dt>**Energiesparmodus wurde automatisch eingegeben**</dt> <dt>4 (0x4)</dt> . </dl> | Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.<br/>                                                                                                                                                                                                                                                   |
| <span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span><dl> <dt>**Energiezustand feststellbar**</dt> <dt>5 (0x5)</dt> </dl>                                                                                 | Die [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) -Methode wird unterstützt. Diese Methode wird in der übergeordneten **CIM \_ LogicalDevice** -Klasse gefunden und kann implementiert werden. Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).<br/> |
| <span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span><dl> <dt>**Unterstützung für Power Cycling**</dt> <dt>6 (0x6)</dt> </dl>                                                                     | Die [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 festgelegt ist ("Power Cycle").<br/>                                                                                                                                                            |
| <span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span><dl> Zeit <dt>**gesteuerte Stromversorgung unterstützt**</dt> <dt>7 (0x7)</dt> </dl>                                                                 | Die [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) -Methode kann aufgerufen werden, wenn der *PowerState*-Parameter auf 5 festgelegt ist ("Power Cycle") und die *Uhrzeit* auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.<br/>                                                                                       |



 

</dd> <dt>

**Powermanagementsupported**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True** gibt an, dass das Gerät Energie verwaltet werden kann, d. h. in einen Energiespar Status versetzt wird. Wenn **false**, sollte der ganzzahlige Wert 1 ("nicht unterstützt") der einzige Eintrag im **powermanagementfunktionalitäten** -Array sein.

Diese Eigenschaft gibt nicht an, ob die Energie Verwaltungsfunktionen derzeit aktiviert sind oder ob Sie aktiviert sind, welche Features unterstützt werden. Weitere Informationen finden Sie im **powermanagementarrays** -Array.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Aktueller Status des Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

Folgende Werte sind gültig:

<dl><span id="OK"></span><span id="ok"></span><dt>

**Okay**
</dt><span id="Error"></span><span id="error"></span><span id="ERROR"></span><dt>

**Zeit**
</dt><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dt>

**Zerstört**
</dt><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dt>

**Unbekannter**
</dt><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span><dt>

**"Pred Fail"**
</dt><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dt>

**Fahren**
</dt><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span><dt>

**Hindern**
</dt><span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dt>

**Leistungs**
</dt><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span><dt>

**Gestresst**
</dt><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span><dt>

**"Nicht wiederherstellen"**
</dt><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dt>

**"Kein Kontakt"**
</dt><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span><dt>

**"Verlorene comm"**
</dt> </dl>

</dd> <dt>

**StatusInfo**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Status des logischen Geräts. Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 ("nicht zutreffend") verwendet werden. Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.

<dl> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1 (0x1))
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

**Systemkreationclassname**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name der Erstellungs Klasse des Bereichs Systems.

</dd> <dt>

**Systemname**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des Bereichs Systems.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                                                 |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ LogicalDevice**](cim-logicaldevice.md)
</dt> <dt>

[**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)
</dt> </dl>

 

