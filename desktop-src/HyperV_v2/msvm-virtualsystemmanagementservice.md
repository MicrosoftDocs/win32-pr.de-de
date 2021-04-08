---
description: Stellt den virtualisierungdienst dar, der auf einem einzelnen Host System vorhanden ist.
ms.assetid: 7f4bd9e0-b034-4882-ad01-f7df740939ae
title: Msvm_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService
- Msvm_VirtualSystemManagementService.InstanceID
- Msvm_VirtualSystemManagementService.Caption
- Msvm_VirtualSystemManagementService.Description
- Msvm_VirtualSystemManagementService.ElementName
- Msvm_VirtualSystemManagementService.InstallDate
- Msvm_VirtualSystemManagementService.Name
- Msvm_VirtualSystemManagementService.OperationalStatus
- Msvm_VirtualSystemManagementService.StatusDescriptions
- Msvm_VirtualSystemManagementService.Status
- Msvm_VirtualSystemManagementService.HealthState
- Msvm_VirtualSystemManagementService.CommunicationStatus
- Msvm_VirtualSystemManagementService.DetailedStatus
- Msvm_VirtualSystemManagementService.OperatingStatus
- Msvm_VirtualSystemManagementService.PrimaryStatus
- Msvm_VirtualSystemManagementService.EnabledState
- Msvm_VirtualSystemManagementService.OtherEnabledState
- Msvm_VirtualSystemManagementService.RequestedState
- Msvm_VirtualSystemManagementService.EnabledDefault
- Msvm_VirtualSystemManagementService.TimeOfLastStateChange
- Msvm_VirtualSystemManagementService.AvailableRequestedStates
- Msvm_VirtualSystemManagementService.TransitioningToState
- Msvm_VirtualSystemManagementService.SystemCreationClassName
- Msvm_VirtualSystemManagementService.SystemName
- Msvm_VirtualSystemManagementService.CreationClassName
- Msvm_VirtualSystemManagementService.PrimaryOwnerName
- Msvm_VirtualSystemManagementService.PrimaryOwnerContact
- Msvm_VirtualSystemManagementService.StartMode
- Msvm_VirtualSystemManagementService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7ee79b9690f1eacdf7dc57a2ebfc2133091a1d55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750169"
---
# <a name="msvm_virtualsystemmanagementservice-class"></a>MSVM \_ virtualsystemmanagementservice-Klasse

Stellt den virtualisierungdienst dar, der auf einem einzelnen Host System vorhanden ist. **MSVM \_ Virtualsystemmanagementservice** wird verwendet, um die Definition, Änderung und Löschung von virtuellen Computern zu steuern. Außerdem gibt es Methoden zum Ausführen von Vorgängen auf virtuellen Computern, z. b. zum Klonen, snapshoten und zum Importieren oder Exportieren virtueller Maschinen. Verwenden Sie [**MSVM \_ Computersystem**](msvm-computersystem.md), um Informationen zu virtuellen Computern abzurufen.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemManagementService : CIM_VirtualSystemManagementService
{
  string   InstanceID;
  string   Caption = "Virtual System Management Service";
  string   Description = "Service for creating, manipulating, and managing virtual machines";
  string   ElementName = "Hyper-V Virtual System Management Service";
  datetime InstallDate;
  string   Name = "vmms";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "The service is running normally" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_VirtualSystemManagementService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started = True;
};
```

## <a name="members"></a>Member

Die **MSVM \_ virtualsystemmanagementservice** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **MSVM \_ virtualsystemmanagementservice** -Klasse verfügt über diese Methoden.



| Methode                                                                                                                 | BESCHREIBUNG                                                                                                                                                                                                                                        |
|:-----------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Addbootsourcesettings**](msvm-virtualsystemmanagementservice-addbootsourcesettings.md)                             | Fügt einer virtuellen Systemkonfiguration Start Quellen hinzu, wenn diese auf eine virtuelle Systemkonfiguration vom Typ "State" angewendet werden.<br/>                                                                                                                             |
| [**Addfeaturesettings**](addfeaturesettings-msvm-virtualsystemmanagementservice.md)                                   | Fügt der Konfiguration einer Ethernet-Verbindung mit einem virtuellen Computer Ethernet-Funktionseinstellungen hinzu.<br/>                                                                                                                                           |
| [**Addspbrechannelchap**](addfibrechannelchap-msvm-virtualsystemmanagementservice.md)                                 | Fügt einem synthetischen Fibre Channel-Port auf einem virtuellen Computer dh-CHAP-Parameter hinzu.<br/>                                                                                                                                                         |
| [**Addguestservicesettings**](msvm-virtualsystemmanagementservice-addguestservicesettings.md)                         | Fügt einer virtuellen Systemkonfiguration Gast Dienst Einstellungen hinzu.<br/> Wenn Sie auf Teile einer "aktuellen" virtuellen Systemkonfiguration angewendet werden, können die Gast Dienste des aktiven virtuellen Systems als Nebeneffekt geändert werden.<br/>              |
| [**Addkvpitems**](addkvpitems-msvm-virtualsystemmanagementservice.md)                                                 | Fügt einem virtuellen Computer Schlüssel-Wert-Paare hinzu.<br/>                                                                                                                                                                                              |
| [**Adresssourcesettings**](addresourcesettings-msvm-virtualsystemmanagementservice.md)                                 | Fügt der Konfiguration einer virtuellen Maschine Ressourcen hinzu.<br/>                                                                                                                                                                                      |
| [**Addsystemcomponentsettings**](msvm-virtualsystemmanagementservice-addsystemcomponentsettings.md)                   | Fügt der Konfiguration eines virtuellen Systems generische Einstellungen hinzu.<br/>                                                                                                                                                                                |
| [**Defineplannedsystem**](msvm-virtualsystemmanagementservice-defineplannedsystem.md)                                 | Definiert ein geplantes virtuelles System.<br/> Eingaben, die nicht vollständig angegeben sind, können mit Standardwerten aufgefüllt werden.<br/>                                                                                                              |
| [**Definesystem**](definesystem-msvm-virtualsystemmanagementservice.md)                                               | Erstellt eine neue Definition für virtuelle Maschinen.<br/>                                                                                                                                                                                               |
| [**Destroysystem**](destroysystem-msvm-virtualsystemmanagementservice.md)                                             | Löscht die Definition einer vorhandenen virtuellen Maschine.<br/>                                                                                                                                                                                         |
| [**Diagnosenetworkconnection**](msvm-virtualsystemmanagementservice-diagnosenetworkconnection.md)                     | Diagnostizieren der Netzwerk Konnektivität eines virtuellen Computers in einer Windows-netzwerkvirtualisierungsumgebung.<br/>                                                                                                                                             |
| [**Exportsystemdefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)                           | Exportiert einen virtuellen Computer oder eine Momentaufnahme eines virtuellen Computers in eine Datei.<br/>                                                                                                                                                               |
| [**FormatError**](formaterror-msvm-virtualsystemmanagementservice.md)                                                 | Gibt eine formatierte Fehlermeldungs Zeichenfolge für das angegebene Array von eingebetteten [**MSVM- \_ Fehler**](msvm-error.md) Instanzen zurück.<br/>                                                                                                               |
| [**Generatewwpn**](generatewwpn-msvm-virtualsystemmanagementservice.md)                                               | Generiert einen Satz von World Wide Port Names (WWPNs).<br/>                                                                                                                                                                                       |
| [**Getcurrentwwpnfromgenerator**](getcurrentwwpnfromgenerator-msvm-virtualsystemmanagementservice.md)                 | Bietet die Möglichkeit, den aktuellen World Wide Port Name (WWPN) anzuzeigen, ohne dass der WWPN reserviert ist.<br/>                                                                                                                                |
| [**GetDefinitionFileSummaryInformation**](getdefinitionfilesummaryinformation-msvm-virtualsystemmanagementservice.md) | Gibt Informationen zur Zusammenfassung der virtuellen Computer für die angegebenen Definitions Dateien der virtuellen Maschine zurück.<br/>                                                                                                                                         |
| [**Getsizeofsystemfiles**](getsizeofsystemfiles-msvm-virtualsystemmanagementservice.md)                               | Ruft die Gesamtgröße der Systemdateien des virtuellen Computers ab.<br/>                                                                                                                                                                        |
| [**Getsummaryinformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md)                             | Gibt Zusammenfassungs Informationen für virtuelle Computer zurück.<br/>                                                                                                                                                                                            |
| [**Getvirtualsystemthumbnailimage**](getvirtualsystemthumbnailimage-msvm-virtualsystemmanagementservice.md)           | Ruft ein Miniaturbild eines vorhandenen virtuellen Computers ab.<br/>                                                                                                                                                                             |
| [**Importsnapshotdefinitions**](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md)                     | Durchsucht den angegebenen Ordner nach allen Momentaufnahme Definitions Dateien, die dem angegebenen geplanten Computersystem zugeordnet sind, und erstellt eine neue Momentaufnahme auf dem geplanten Computersystem für jede zugeordnete Definitionsdatei an diesem Speicherort.<br/> |
| [**Importsystemdefinition**](importsystemdefinition-msvm-virtualsystemmanagementservice.md)                           | Erstellt ein neues geplantes Computersystem basierend auf der angegebenen Definition der virtuellen Maschine.<br/>                                                                                                                                                |
| [**Modifydiskmergesettings**](modifydiskmergesettings-msvm-virtualsystemmanagementservice.md)                         | Ändert die Daten der Datenträger zusammenlaufseinstellung.<br/>                                                                                                                                                                                                   |
| [**Modifyfeaturesettings**](modifyfeaturesettings-msvm-virtualsystemmanagementservice.md)                             | Ändert die aktuellen Featureeinstellungen einer Ethernet-Verbindung einer virtuellen Maschine.<br/>                                                                                                                                                         |
| [**Modifyguestservicesettings**](msvm-virtualsystemmanagementservice-modifyguestservicesettings.md)                   | Ändert die Einstellungen des Gast Diensts.<br/> Wenn Sie auf Teile einer "aktuellen" virtuellen Systemkonfiguration angewendet werden, können die Gast Dienste des aktiven virtuellen Systems als Nebeneffekt geändert werden.<br/>                                            |
| [**Modifykvpitems**](modifykvpitems-msvm-virtualsystemmanagementservice.md)                                           | Ändert vorhandene Schlüssel-Wert-Paare auf einem virtuellen Computer.<br/>                                                                                                                                                                                 |
| [**Modifyresourcesettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md)                           | Ändert die Einstellungen der virtuellen Ressource.<br/>                                                                                                                                                                                                     |
| [**Modifyservicesettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)                             | Ändert die Einstellungsdaten des dienstanders.<br/>                                                                                                                                                                                                    |
| [**Modifysystemcomponentsettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md)             | Ändert die generischen Systemkomponenten Einstellungen.<br/>                                                                                                                                                                                             |
| [**Modifysystemsettings**](modifysystemsettings-msvm-virtualsystemmanagementservice.md)                               | Ändert die Einstellungen der virtuellen Maschine.<br/>                                                                                                                                                                                                      |
| [**Realizeplannedsystem**](realizeplannedsystem-msvm-virtualsystemmanagementservice.md)                               | Überprüft die Konfiguration einer geplanten virtuellen Maschine und konvertiert sie in eine erkannte virtuelle Maschine.<br/>                                                                                                                                 |
| [**Removebootsourcesettings**](msvm-virtualsystemmanagementservice-removebootsourcesettings.md)                       | Entfernt die Einstellungen virtueller Ressourcen aus einer Konfiguration des virtuellen Systems.<br/> Wenn Sie auf Teile einer "aktuellen" virtuellen Systemkonfiguration angewendet werden, werden möglicherweise als Nebeneffekt Ressourcen des aktiven virtuellen Systems entfernt.<br/>            |
| [**Removefeaturesettings**](removefeaturesettings-msvm-virtualsystemmanagementservice.md)                             | Entfernt Funktionseinstellungen aus einer Ethernet-Verbindung eines virtuellen Computers.<br/>                                                                                                                                                                    |
| [**Removefbrechannelchap**](removefibrechannelchap-msvm-virtualsystemmanagementservice.md)                           | Entfernt die dh-CHAP-Parameter aus einem synthetischen Fibre Channel-Port auf einem virtuellen Computer.<br/>                                                                                                                                                    |
| [**Removeguestservicesettings**](msvm-virtualsystemmanagementservice-removeguestservicesettings.md)                   | Entfernt Gast Dienst Einstellungen aus einer Konfiguration des virtuellen Systems.<br/> Wenn Sie auf Teile einer "aktuellen" virtuellen Systemkonfiguration angewendet werden, können die Gast Dienste des aktiven virtuellen Systems als Nebeneffekt geändert werden.<br/>         |
| [**Removekvpitems**](removekvpitems-msvm-virtualsystemmanagementservice.md)                                           | Entfernt vorhandene Schlüssel-Wert-Paare aus einer virtuellen Maschine.<br/>                                                                                                                                                                                |
| [**Removeresourcesettings**](removeresourcesettings-msvm-virtualsystemmanagementservice.md)                           | Entfernt die Einstellungen der virtuellen Ressource aus der Konfiguration einer virtuellen Maschine.<br/>                                                                                                                                                                 |
| [**Removesystemcomponentsettings**](msvm-virtualsystemmanagementservice-removesystemcomponentsettings.md)             | Entfernt generische Komponenten Einstellungen aus einer virtuellen Systemkonfiguration.<br/>                                                                                                                                                                 |
| [**RequestStateChange**](msvm-virtualsystemmanagementservice-requeststatechange.md)                                   | Diese Methode wird nicht unterstützt.<br/>                                                                                                                                                                                                           |
| [**Setguestnetworkadapterconfiguration**](setguestnetworkadapterconfiguration-msvm-virtualsystemmanagementservice.md) | Konfiguriert die Netzwerkadapter innerhalb des Gast Betriebssystems.<br/>                                                                                                                                                                      |
| [**Setinitialmachineconfigurationdata**](msvm-virtualsystemmanagementservice-setinitialmachineconfigurationdata.md)   | Legt die anfänglichen Computer Konfigurationsdaten eines virtuellen Computers fest.<br/>                                                                                                                                                                                         |
| [**Start Service**](msvm-virtualsystemmanagementservice-startservice.md)                                               | Diese Methode wird nicht unterstützt.<br/>                                                                                                                                                                                                           |
| [**Stop Service**](msvm-virtualsystemmanagementservice-stopservice.md)                                                 | Diese Methode wird nicht unterstützt.<br/>                                                                                                                                                                                                           |
| [**Testnetworkconnection**](msvm-virtualsystemmanagementservice-testnetworkconnection.md)                             | Testet die Netzwerk Konnektivität eines virtuellen Computers in einer Windows-netzwerkvirtualisierungsumgebung.<br/>                                                                                                                                                 |
| [**Upgradesystemversion**](msvm-virtualsystemmanagementservice-upgradesystemversion.md)                               | Führt ein Upgrade des virtuellen Systems durch.<br/> Bei Anwendung auf die Systemeinstellungen einer "aktuellen" virtuellen Systemkonfiguration<br/>                                                                                                                 |
| [**Validateplannedsystem**](validateplannedsystem-msvm-virtualsystemmanagementservice.md)                             | Überprüft das angegebene geplante System.<br/>                                                                                                                                                                                                 |



 

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ virtualsystemmanagementservice** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

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

Eine kurze Beschreibung des-Objekts. Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Hyper-V Virtual System Management Service" festgelegt.

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

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Key**, **maxlen** (256)
</dt> </dl>

Der Name der Klasse oder Unterklasse, die bei der Erstellung einer-Instanz verwendet wird. Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt und ist immer auf "MSVM \_ virtualsystemmanagementservice" festgelegt.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des -Objekts. Diese Eigenschaft wird vom [**CIM- \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Service zum Erstellen, bearbeiten und Verwalten virtueller Maschinen" festgelegt.

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

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Anzeige Name für das-Objekt. Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Hyper-V Virtual System Management Service" festgelegt.

</dd> <dt>

**Enableddefault**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Standard-oder Startkonfiguration eines Administrators für den aktivierten Zustand eines Elements. Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf 2 (aktiviert) festgelegt.



| Wert                                                                        | Bedeutung            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <dt>2</dt> </dl> | Aktiviert<br/> |



 

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der aktivierte und deaktivierte Status eines Elements. Diese Eigenschaft kann auch die Übergänge zwischen diesen angeforderten Zuständen angeben. Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf 2 (aktiviert) festgelegt.



| Wert                                                                        | Bedeutung            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <dt>2</dt> </dl> | Aktiviert<br/> |



 

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der aktuelle Zustand des Elements. Dieses Attribut drückt den Zustand dieses Elements aus, aber nicht notwendigerweise dessen unter Komponenten. Mögliche Werte sind 0 bis 30, wobei 5 bedeutet, dass das Element vollständig fehlerfrei ist und 30 bedeutet, dass das Element vollständig nicht funktionsfähig ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und ist immer auf 5 (OK) festgelegt.



| Wert                                                                        | Bedeutung                                 |
|------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>5</dt> </dl> | Der Integritäts Status ist "Normal".<br/> |



 

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

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Key**, **maxlen** (256)
</dt> </dl>

Die Bezeichnung, mit der das-Objekt bekannt ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und ist immer auf "VMMS" festgelegt.

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

Die aktuellen Status des-Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, und jedes Array Element ist immer auf 2 (OK) festgelegt.

</dd> <dt>

**Otherenabledstate**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die den aktivierten oder deaktivierten Status des Elements beschreibt, wenn die **enabledstate** -Eigenschaft auf 1 ("Other") festgelegt ist. Diese Eigenschaft muss auf **null** festgelegt werden, wenn **enabledstate** ein anderer Wert als 1 ist. Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.

</dd> <dt>

**PrimaryOwnerContact**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **maxlen** (256)
</dt> </dl>

Alle Informationen dazu, wie der primäre Besitzer des Dienstanbieter erreicht werden kann (z. b. Telefonnummer, e-Mail-Adresse usw.). Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt und ist immer auf **null** festgelegt.

</dd> <dt>

**Primaryownername**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **maxlen** (64)
</dt> </dl>

Der Name des primären Besitzers für den Dienst, sofern definiert. Der primäre Besitzer ist der erste Support Kontakt für den Dienst. Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt und ist immer auf **null** festgelegt.

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

Der zuletzt angeforderte oder gewünschte Zustand für das Element. Der tatsächliche Zustand des Elements wird durch **enabledstate** dargestellt. Diese Eigenschaft wird bereitgestellt, um die zuletzt angeforderten und aktuellen Zustände für ein Element zu vergleichen. Eine bestimmte Instanz der [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85)) -Klasse unterstützt die **requestedstate** -Eigenschaft möglicherweise nicht. Wenn dies auftritt, wird der Wert 12 ("nicht zutreffend") verwendet. Diese Eigenschaft wird von **CIM \_ enabledlogicalelement** geerbt und ist immer auf 12 (nicht zutreffend) festgelegt.



| Wert                                                                         | Bedeutung                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>12</dt> </dl> | Nicht zutreffend<br/> |



 

</dd> <dt>

**Gestartet**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der Dienst gerade ausgeführt wird. Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt und ist immer auf " **true**" festgelegt.

</dd> <dt>

**StartMode**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **maxlen** (10)
</dt> </dl>

Ein Zeichen folgen Wert, der angibt, ob der Dienst automatisch von einem System oder einem Betriebssystem gestartet oder nur nach Anforderung gestartet wird. Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt und ist immer auf **null** festgelegt.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, aber nicht verwendet.

</dd> <dt>

**Status Beschreibungen**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, und jedes Array Element ist immer auf "der Dienst wird normal ausgeführt" festgelegt.

</dd> <dt>

**Systemkreationclassname**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Key**, **maxlen** (256)
</dt> </dl>

Der Name der Erstellungs Klasse des Bereichs Systems. Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt und ist immer auf "MSVM \_ Computersystem" festgelegt.

</dd> <dt>

**Systemname**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Key**, **maxlen** (256)
</dt> </dl>

Der NetBIOS-Name des hostingcomputersystems. Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.

</dd> <dt>

**Timeoflaststatechange**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Datum oder die Uhrzeit, zu dem der aktivierte Status des Elements zuletzt geändert wurde. Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.

</dd> <dt>

**Transitioningumstate**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den Ziel Status an, in den die-Instanz übergeht. Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und ist immer auf **null** festgelegt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Zugriff auf die **MSVM \_ virtualsystemmanagementservice** -Klasse kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**CIM \_ virtualsystemmanagementservice**](cim-virtualsystemmanagementservice.md)
</dt> <dt>

[**CIM \_ virtualsystemmanagementservice**](/previous-versions//cc136952(v=vs.85))
</dt> <dt>

[**MSVM \_ virtualsystemmanagementservice (v1)**](/previous-versions/windows/desktop/legacy/cc136940(v=vs.85))
</dt> <dt>

[Verwaltungs Klassen für virtuelle Systeme](virtual-system-management-classes.md)
</dt> </dl>

 

