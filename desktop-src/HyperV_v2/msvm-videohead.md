---
description: Beschreibt die primäre Zeichen Oberfläche auf einem Anzeige Controller.
ms.assetid: 280ABAD0-D91B-4683-9F12-32563D7FE6BF
title: Msvm_VideoHead-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VideoHead
- Msvm_VideoHead.SetPowerState
- Msvm_VideoHead.EnableDevice
- Msvm_VideoHead.OnlineDevice
- Msvm_VideoHead.QuiesceDevice
- Msvm_VideoHead.SaveProperties
- Msvm_VideoHead.RestoreProperties
- Msvm_VideoHead.InstanceID
- Msvm_VideoHead.Caption
- Msvm_VideoHead.Description
- Msvm_VideoHead.ElementName
- Msvm_VideoHead.InstallDate
- Msvm_VideoHead.Name
- Msvm_VideoHead.OperationalStatus
- Msvm_VideoHead.StatusDescriptions
- Msvm_VideoHead.Status
- Msvm_VideoHead.HealthState
- Msvm_VideoHead.CommunicationStatus
- Msvm_VideoHead.DetailedStatus
- Msvm_VideoHead.OperatingStatus
- Msvm_VideoHead.PrimaryStatus
- Msvm_VideoHead.EnabledState
- Msvm_VideoHead.OtherEnabledState
- Msvm_VideoHead.RequestedState
- Msvm_VideoHead.EnabledDefault
- Msvm_VideoHead.TimeOfLastStateChange
- Msvm_VideoHead.AvailableRequestedStates
- Msvm_VideoHead.TransitioningToState
- Msvm_VideoHead.SystemCreationClassName
- Msvm_VideoHead.SystemName
- Msvm_VideoHead.CreationClassName
- Msvm_VideoHead.DeviceID
- Msvm_VideoHead.PowerManagementSupported
- Msvm_VideoHead.PowerManagementCapabilities
- Msvm_VideoHead.Availability
- Msvm_VideoHead.StatusInfo
- Msvm_VideoHead.LastErrorCode
- Msvm_VideoHead.ErrorDescription
- Msvm_VideoHead.ErrorCleared
- Msvm_VideoHead.OtherIdentifyingInfo
- Msvm_VideoHead.PowerOnHours
- Msvm_VideoHead.TotalPowerOnHours
- Msvm_VideoHead.IdentifyingDescriptions
- Msvm_VideoHead.AdditionalAvailability
- Msvm_VideoHead.MaxQuiesceTime
- Msvm_VideoHead.CurrentBitsPerPixel
- Msvm_VideoHead.CurrentHorizontalResolution
- Msvm_VideoHead.CurrentVerticalResolution
- Msvm_VideoHead.MaxRefreshRate
- Msvm_VideoHead.MinRefreshRate
- Msvm_VideoHead.CurrentRefreshRate
- Msvm_VideoHead.CurrentScanMode
- Msvm_VideoHead.OtherCurrentScanMode
- Msvm_VideoHead.CurrentNumberOfRows
- Msvm_VideoHead.CurrentNumberOfColumns
- Msvm_VideoHead.CurrentNumberOfColors
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9f40e0386fe42177484fc07296a2f4567f1ee47a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130320"
---
# <a name="msvm_videohead-class"></a>MSVM- \_ videoheadklasse

Beschreibt die primäre Zeichen Oberfläche auf einem Anzeige Controller.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VideoHead : CIM_VideoHead
{
  string   InstanceID;
  string   Caption = "Video Head";
  string   Description = "Microsoft Virtual Video Head";
  string   ElementName = "Video Head";
  datetime InstallDate;
  string   Name = "Video Head";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   EnabledState = 3;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState = 12;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  uint16   CreationClassName = "Msvm_VideoHead";
  string   DeviceID;
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability = 6;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  string   OtherIdentifyingInfo[];
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[] = { 6 };
  uint64   MaxQuiesceTime;
  uint32   CurrentBitsPerPixel;
  uint32   CurrentHorizontalResolution;
  uint32   CurrentVerticalResolution;
  uint32   MaxRefreshRate;
  uint32   MinRefreshRate;
  uint32   CurrentRefreshRate;
  uint16   CurrentScanMode;
  string   OtherCurrentScanMode;
  uint32   CurrentNumberOfRows;
  uint32   CurrentNumberOfColumns;
  uint64   CurrentNumberOfColors;
};
```

## <a name="members"></a>Member

Die **MSVM- \_ videoheadklasse** verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **MSVM- \_ videohead** -Klasse verfügt über diese Methoden.



| Methode                                                          | BESCHREIBUNG                              |
|:----------------------------------------------------------------|:-----------------------------------------|
| **EnableDevice**                                                | Diese Methode wird nicht unterstützt.<br/> |
| **Onlinedevice**                                                | Diese Methode wird nicht unterstützt.<br/> |
| **Inaktiven Geräte**                                               | Diese Methode wird nicht unterstützt.<br/> |
| [**RequestStateChange**](msvm-videohead-requeststatechange.md) | Fordert eine Statusänderung an.<br/>      |
| [**Zurücksetzen**](msvm-videohead-reset.md)                           | Setzt das virtuelle Gerät zurück.<br/>    |
| **Restoreproperties**                                           | Diese Methode wird nicht unterstützt.<br/> |
| **SaveProperties**                                              | Diese Methode wird nicht unterstützt.<br/> |
| **SetPowerState**                                               | Diese Methode wird nicht unterstützt.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **MSVM- \_ videohead** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Additionalavailability**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Alle zusätzlichen Verfügbarkeit und der Status des Geräts. Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist auf 6 festgelegt (nicht zutreffend).

</dd> <dt>

**Verfügbarkeit**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die primäre Verfügbarkeit und den Status des Geräts. Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.



| Wert                                                                        | Bedeutung                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <dt>6</dt> </dl> | Nicht zutreffend<br/> |



 

</dd> <dt>

**Availablerequestedstates**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die möglichen Werte für den *requestedstate* -Parameter der **requestStateChange** -Methode an. Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine kurze Beschreibung des-Objekts. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**Communicationstatus**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren. Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)
</dt> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)
</dt> <dt>

<span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Kommunikation OK** (2)
</dt> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Verlorene Kommunikation** (3)
</dt> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Kein Kontakt** (4)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000.. )
</dt> </dl>

</dd> <dt>

**"Name der Klassenname"**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name der Klasse oder Unterklasse, die bei der Erstellung einer-Instanz verwendet wird. Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.

</dd> <dt>

**Currentbitsperpixel**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Einheiten** ("Bits")
</dt> </dl>

Die Anzahl der Bits, die zum Anzeigen der einzelnen Pixel verwendet werden. Diese Eigenschaft wird vom [**CIM- \_ videohead**](/previous-versions//cc136948(v=vs.85))geerbt.

</dd> <dt>

**Ereignis Auflösung**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Einheiten** ("Pixel")
</dt> </dl>

Die aktuelle Anzahl von horizontalen Pixeln. Diese Eigenschaft wird vom [**CIM- \_ videohead**](/previous-versions//cc136948(v=vs.85))geerbt.

</dd> <dt>

**Currentzahlofcolors**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Anzahl von Farben, die in den aktuellen Auflösungen unterstützt werden. Diese Eigenschaft wird vom [**CIM- \_ videohead**](/previous-versions//cc136948(v=vs.85))geerbt.

</dd> <dt>

**Currentzahlofcolumns**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Im Zeichenmodus die Anzahl der Spalten für diesen Anzeige Controller. Andernfalls ist es 0. Diese Eigenschaft wird vom [**CIM- \_ videohead**](/previous-versions//cc136948(v=vs.85))geerbt.

</dd> <dt>

**Currentnumofrows**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Im Zeichenmodus die Anzahl der Zeilen für diesen Videocontroller. Andernfalls ist es 0. Diese Eigenschaft wird vom [**CIM- \_ videohead**](/previous-versions//cc136948(v=vs.85))geerbt.

</dd> <dt>

**CurrentRefreshRate**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Einheiten** ("Hertz")
</dt> </dl>

Die aktuelle Aktualisierungsrate in Hertz. Diese Eigenschaft wird vom [**CIM- \_ videohead**](/previous-versions//cc136948(v=vs.85))geerbt.

</dd> <dt>

**Currentscanmode**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der aktuelle Scanmodus. Diese Eigenschaft wird vom [**CIM- \_ videohead**](/previous-versions//cc136948(v=vs.85))geerbt.

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)
</dt> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (2)
</dt> <dt>

<span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>**Nicht-Interlacing-Vorgang** (3)
</dt> <dt>

<span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>Zeilen Sprung **Vorgang** (4)
</dt> </dl>

</dd> <dt>

**Currentverticalresolution**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Einheiten** ("Pixel")
</dt> </dl>

Die aktuelle Anzahl vertikaler Pixel. Diese Eigenschaft wird vom [**CIM- \_ videohead**](/previous-versions//cc136948(v=vs.85))geerbt.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**DetailedStatus**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ergänzt die **primarystatus** -Eigenschaft mit zusätzlichen Status Details. Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

<dl> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (0)
</dt> <dt>

<span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Keine zusätzlichen Informationen** (1)
</dt> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Betont** (2)
</dt> <dt>

<span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Vorhersagefehler** (3)
</dt> <dt>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Nicht BEHEB barer Fehler** (4)
</dt> <dt>

<span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Unterstützende Entität in Error** (5)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000.. )
</dt> </dl>

</dd> <dt>

**DeviceID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und auf "Microsoft:*GUID* \\ Head \\ *Index*" festgelegt.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Anzeige Name für das-Objekt. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**Enableddefault**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Standard-oder Startkonfiguration eines Administrators für den aktivierten Zustand eines Elements. Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf 2 (aktiviert) festgelegt.



| Wert                                                                        | Bedeutung             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <dt>2</dt> </dl> | Aktiviert<br/>  |
| <dl> <dt>3</dt> </dl> | Disabled<br/> |



 

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der aktivierte und deaktivierte Status eines Elements. Sie kann auch die Übergänge zwischen diesen angeforderten Zuständen angeben. Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.



| Wert                                                                        | Bedeutung             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <dt>2</dt> </dl> | Aktiviert<br/>  |
| <dl> <dt>3</dt> </dl> | Disabled<br/> |



 

</dd> <dt>

**Errorgelöscht**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der in **LastErrorCode** gemeldete Fehler jetzt gelöscht wird. Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die weitere Informationen über den Fehler enthält, der in **LastErrorCode** aufgezeichnet wurde, sowie Informationen über alle Maßnahmen, die ausgeführt werden können. Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der aktuelle Zustand des Elements. Dieses Attribut drückt den Zustand dieses Elements aus, aber nicht notwendigerweise dessen unter Komponenten. Mögliche Werte sind 0 bis 30, wobei 5 bedeutet, dass das Element vollständig fehlerfrei ist und 30 bedeutet, dass das Element vollständig nicht funktionsfähig ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.



| Wert                                                                        | Bedeutung       |
|------------------------------------------------------------------------------|---------------|
| <dl> <dt>5</dt> </dl> | OK<br/> |



 

</dd> <dt>

**IdentifyingDescriptions**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Array von Freiform-Zeichen folgen, die Erklärungen und Details hinter den Einträgen im Eigenschafts Array " **OtherIdentifyingInfo** " bereitstellen. Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist auf **null** festgelegt.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Datum und die Uhrzeit der Erstellung der Konfiguration der virtuellen Maschine. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Identifiziert eine Instanz dieser Klasse eindeutig. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**LastErrorCode**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der letzte vom logischen Gerät gemeldete Fehlercode. Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.

</dd> <dt>

**Maxquiescetime**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft ist veraltet. Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.

</dd> <dt>

**Maxfreshshrate**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Einheiten** ("Hertz")
</dt> </dl>

Die maximale Aktualisierungsrate des Anzeige Controllers in Hertz. Diese Eigenschaft wird vom [**CIM- \_ videohead**](/previous-versions//cc136948(v=vs.85))geerbt.

</dd> <dt>

**Minfreshshrate**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Einheiten** ("Hertz")
</dt> </dl>

Die minimale Aktualisierungsrate des Video Controllers in Hertz. Diese Eigenschaft wird vom [**CIM- \_ videohead**](/previous-versions//cc136948(v=vs.85))geerbt.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Bezeichnung, mit der das-Objekt bekannt ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und entspricht der Element **Name** -Eigenschaft.

</dd> <dt>

**Operatingstatus**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen. Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)
</dt> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (1)
</dt> <dt>

<span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Wartung** (2)
</dt> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>Wird **gestartet** (3)
</dt> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>Wird **beendet (4** )
</dt> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Beendet** (5)
</dt> <dt>

<span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Abgebrochen** (6)
</dt> <dt>

<span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Ruhende** (7)
</dt> <dt>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Abgeschlossen** (8)
</dt> <dt>

<span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrieren** (9)
</dt> <dt>

<span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Migration** (10)
</dt> <dt>

<span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migration** (11)
</dt> <dt>

<span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotts** (12)
</dt> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Herunter** fahren (13)
</dt> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)
</dt> <dt>

<span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Übergang** (15)
</dt> <dt>

<span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Dienst** (16)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000.. )
</dt> </dl>

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die aktuellen Status des-Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**Othercurrentscanmode**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der aktuelle Scanmodus, wenn die **currentscanmode** -Eigenschaft der Instanz 1 (Other) ist. Diese Eigenschaft wird von [**CIM \_ videohead**](/previous-versions//cc136948(v=vs.85)) geerbt und ist auf **null** festgelegt.

</dd> <dt>

**Otherenabledstate**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die den aktivierten oder deaktivierten Status des Elements beschreibt, wenn die **enabledstate** -Eigenschaft auf 1 (Sonstiges) festgelegt ist. Diese Eigenschaft muss auf **null** festgelegt werden, wenn **enabledstate** ein anderer Wert als 1 ist. Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Alle zusätzlichen Daten über Geräte-ID-Informationen, die zur Identifizierung eines logischen Geräts verwendet werden könnten. Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist auf **null** festgelegt.

</dd> <dt>

**Powermanagementfunktionen**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Energie Verwaltungsfunktionen des Geräts. Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.

</dd> <dt>

**Powermanagementsupported**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob das Gerät Energie gesteuert werden kann. Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.

</dd> <dt>

**Poweronhours**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, wie viele aufeinanderfolgende Stunden dieses Gerät seit dem letzten Strom Umgebung eingeschaltet wurde. Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.

</dd> <dt>

**Primarystatus**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Stellt Statusinformationen auf hoher Ebene bereit. Diese Eigenschaft sollte in Verbindung mit der Eigenschaft **detailedstatus** verwendet werden, um einen hohen und detaillierten Integritäts Status des Elements und seiner unter Komponenten bereitzustellen. Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)
</dt> <dt>

<span id="OK"></span><span id="ok"></span>**OK** (1)
</dt> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (2** )
</dt> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Fehler** (3)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (0X8000.. )
</dt> </dl>

</dd> <dt>

**RequestedState**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der zuletzt angeforderte oder gewünschte Zustand für das Element. Der tatsächliche Zustand des Elements wird durch **enabledstate** dargestellt. Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.



| Wert                                                                         | Bedeutung                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <dt>12</dt> </dl> | Nicht zutreffend<br/> |



 

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die den aktuellen Status des-Objekts angibt. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, aber nicht verwendet.

</dd> <dt>

**Status Beschreibungen**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**StatusInfo**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der aktuelle Zustand des logischen Geräts. Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.

</dd> <dt>

**Systemkreationclassname**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name der Erstellungs Klasse des Bereichs Systems. Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.

</dd> <dt>

**Systemname**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der eindeutige Bezeichner für die Bereichs bezogene virtuelle Maschine. Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.

</dd> <dt>

**Timeoflaststatechange**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Datum oder die Uhrzeit, zu dem der aktivierte Status des Elements zuletzt geändert wurde. Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.

</dd> <dt>

**Totalpoweronhours**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Gesamtanzahl der Stunden, für die dieses Gerät eingeschaltet wurde. Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.

</dd> <dt>

**Transitioningumstate**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den Ziel Status an, in den die-Instanz übergeht. Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.



| Wert                                                                         | Bedeutung                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <dt>12</dt> </dl> | Nicht zutreffend<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Zugriff auf die **MSVM- \_ videoheadklasse** kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ videohead**](cim-videohead.md)
</dt> <dt>

[**CIM- \_ videohead**](/previous-versions//cc136948(v=vs.85))
</dt> <dt>

[Video Klassen](video-classes.md)
</dt> </dl>

 

