---
description: Dient als Platzhalter für den Dienst innerhalb des Schalters, der Mac-Adressen lernt und als Brücke zwischen den Klassen MSVM \_ virtualethernetstiwitch und MSVM \_ dynamicforwardingentry fungiert.
ms.assetid: E617DBC3-F5DD-4875-B3CC-E120A2218EBE
title: Msvm_TransparentBridgingService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TransparentBridgingService
- Msvm_TransparentBridgingService.InstanceID
- Msvm_TransparentBridgingService.Caption
- Msvm_TransparentBridgingService.Description
- Msvm_TransparentBridgingService.ElementName
- Msvm_TransparentBridgingService.InstallDate
- Msvm_TransparentBridgingService.OperationalStatus
- Msvm_TransparentBridgingService.StatusDescriptions
- Msvm_TransparentBridgingService.Status
- Msvm_TransparentBridgingService.HealthState
- Msvm_TransparentBridgingService.CommunicationStatus
- Msvm_TransparentBridgingService.DetailedStatus
- Msvm_TransparentBridgingService.OperatingStatus
- Msvm_TransparentBridgingService.PrimaryStatus
- Msvm_TransparentBridgingService.EnabledState
- Msvm_TransparentBridgingService.OtherEnabledState
- Msvm_TransparentBridgingService.RequestedState
- Msvm_TransparentBridgingService.EnabledDefault
- Msvm_TransparentBridgingService.TimeOfLastStateChange
- Msvm_TransparentBridgingService.AvailableRequestedStates
- Msvm_TransparentBridgingService.TransitioningToState
- Msvm_TransparentBridgingService.SystemCreationClassName
- Msvm_TransparentBridgingService.SystemName
- Msvm_TransparentBridgingService.CreationClassName
- Msvm_TransparentBridgingService.Name
- Msvm_TransparentBridgingService.PrimaryOwnerName
- Msvm_TransparentBridgingService.PrimaryOwnerContact
- Msvm_TransparentBridgingService.StartMode
- Msvm_TransparentBridgingService.Started
- Msvm_TransparentBridgingService.Keywords
- Msvm_TransparentBridgingService.ServiceURL
- Msvm_TransparentBridgingService.StartupConditions
- Msvm_TransparentBridgingService.StartupParameters
- Msvm_TransparentBridgingService.ProtocolType
- Msvm_TransparentBridgingService.OtherProtocolType
- Msvm_TransparentBridgingService.AgingTime
- Msvm_TransparentBridgingService.FID
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f5daacf42bc221fa98f56d0c5b84140e3784c2ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959185"
---
# <a name="msvm_transparentbridgingservice-class"></a>MSVM- \_ transparentbridgingservice-Klasse

Dient als Platzhalter für den Dienst innerhalb des Schalters, der Mac-Adressen lernt und als Brücke zwischen den Klassen [**MSVM \_ virtualethernetstiwitch**](msvm-virtualethernetswitch.md) und [**MSVM \_ dynamicforwardingentry**](msvm-dynamicforwardingentry.md) fungiert.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TransparentBridgingService : CIM_TransparentBridgingService
{
  string   InstanceID;
  string   Caption = "Virtual Switch Transparent Bridging Service";
  string   Description = "Microsoft Virtual Switch Transparent Bridging Service";
  string   ElementName;
  datetime InstallDate;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = "OK";
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_TransparentBridgingService";
  string   Name;
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode = "Automatic";
  boolean  Started = True;
  string   Keywords[];
  string   ServiceURL;
  string   StartupConditions[];
  string   StartupParameters[];
  uint16   ProtocolType = 15;
  string   OtherProtocolType;
  uint32   AgingTime = 300;
  uint32   FID = 0;
};
```

## <a name="members"></a>Member

Die **MSVM-Klasse " \_ transparentbridgingservice** " verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **MSVM-Klasse " \_ transparentbridgingservice** " verfügt über diese Methoden.



| Methode                                                                           | BESCHREIBUNG                         |
|:---------------------------------------------------------------------------------|:------------------------------------|
| [**RequestStateChange**](msvm-transparentbridgingservice-requeststatechange.md) | Fordert eine Statusänderung an.<br/> |
| [**Start Service**](msvm-transparentbridgingservice-startservice.md)             | Startet den Dienst.<br/>      |
| [**Stop Service**](msvm-transparentbridgingservice-stopservice.md)               | Beendet den Dienst.<br/>       |



 

### <a name="properties"></a>Eigenschaften

Die **MSVM-Klasse " \_ transparentbridgingservice** " verfügt über diese Eigenschaften.

<dl> <dt>

**Agingtime**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Timeout Zeitraum (in Sekunden) für das Auslagern dynamisch erlernter Mac-Adressen. Diese Eigenschaft wird von [**CIM \_ transparentbridgingservice**](/previous-versions/windows/desktop/clushyperv/cim-transparentbridgingservice)geerbt.

</dd> <dt>

**Availablerequestedstates**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die möglichen Werte für den *requestedstate* -Parameter der **requestStateChange** -Methode an. Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine kurze Beschreibung des-Objekts. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer "der virtuelle Switch Transparent Bridging Service".

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
</dt> </dl>

Eine kurze Beschreibung des-Objekts. Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des -Objekts. Diese Eigenschaft wird vom [**CIM- \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Microsoft Virtual Switch Transparent Bridging Service" festgelegt.

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

Ein Anzeige Name für das-Objekt. Mit dieser Eigenschaft kann jede Instanz zusätzlich zu ihren Schlüsseleigenschaften, Identitätsdaten und Beschreibungs Informationen einen anzeigen Amen definieren. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**Enableddefault**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Standard-oder Startkonfiguration eines Administrators für den aktivierten Zustand eines Elements. Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der aktivierte und deaktivierte Status eines Elements. Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.

</dd> <dt>

**Angestrebt**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Bezeichner der Filterungs Datenbank, der von Switches verwendet wird, die VLAN unterstützen und über mehrere Filter Datenbanken verfügen. Diese Eigenschaft wird von [**CIM \_ transparentbridgingservice**](/previous-versions/windows/desktop/clushyperv/cim-transparentbridgingservice)geerbt.

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der aktuelle Zustand des Elements. Dieses Attribut drückt den Zustand dieses Elements aus, aber nicht notwendigerweise dessen unter Komponenten. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die Uhrzeit an, zu der das-Objekt installiert wurde. Ein fehlender Wert weist nicht darauf hin, dass das Objekt nicht installiert ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und wird nicht verwendet.

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

**Schlüsselwörter**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Darf nicht verwendet werden. Ein frei Form Array von Zeichen folgen, die beschreibende Wörter und Ausdrücke bereitstellen, die in Abfragen verwendet werden können. Diese Eigenschaft ist nicht implementiert, da Sie nicht standardisiert ist. Wenn diese Eigenschaft ein erforderliches Abfrage Konstrukt wäre, wäre sie in der Vererbungs Hierarchie höher. Diese Eigenschaft wird vom [**CIM- \_ NetworkService**](/previous-versions//cc136875(v=vs.85))geerbt.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Name, der den Dienst eindeutig identifiziert und eine Angabe der verwalteten Funktionalität bereitstellt. Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.

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

Der aktuelle Status des Elements. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**Otherenabledstate**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der aktivierte oder deaktivierte Status des Elements, wenn die **enabledstate** -Eigenschaft auf 1 (Sonstiges) festgelegt ist. Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und wird nicht verwendet.

</dd> <dt>

**Otherprotocoltype**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Protokolltyp, der weitergeleitet wird, wenn der Wert von **ProtocolType** 1 (Other) ist. Diese Eigenschaft wird von [**CIM \_ forwardingservice**](/previous-versions/windows/desktop/clushyperv/cim-forwardingservice)geerbt.

</dd> <dt>

**PrimaryOwnerContact**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die Informationen darüber bereitstellt, wie der primäre Besitzer des Dienstanbieter erreicht werden kann. Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.

</dd> <dt>

**Primaryownername**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des primären Besitzers für den Dienst, sofern definiert. Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.

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

**ProtocolType**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Protokolltyp, der weitergeleitet wird. Diese Eigenschaft wird von [**CIM \_ forwardingservice**](/previous-versions/windows/desktop/clushyperv/cim-forwardingservice)geerbt.

</dd> <dt>

**RequestedState**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der zuletzt angeforderte oder gewünschte Status für den Verwaltungsdienst. Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.

</dd> <dt>

**ServiceUrl**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Darf nicht verwendet werden. Eine URL, die das Protokoll, den Netzwerk Speicherort und andere Dienst spezifische Informationen bereitstellt, die für den Zugriff auf den Dienst erforderlich sind. Verwenden Sie stattdessen die **serviceaccessuri** -Klasse, die die Semantik des Dienst Zugriffs ordnungsgemäß positioniert und das Format der Informationen verdeutlicht. Diese Eigenschaft wird vom [**CIM- \_ NetworkService**](/previous-versions//cc136875(v=vs.85))geerbt.

</dd> <dt>

**Gestartet**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der Dienst gestartet wurde (**true**) oder beendet (**false**) ist. Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.

</dd> <dt>

**StartMode**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der Dienst automatisch von einem System, einem Betriebssystem usw. gestartet wird oder nur nach Anforderung gestartet wird. Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.

</dd> <dt>

**Startupconditions**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Darf nicht verwendet werden. Ein frei Form Array von Zeichen folgen, die bestimmte Vorbedingungen angeben, die erfüllt sein müssen, damit dieser Dienst ordnungsgemäß gestartet wird. Diese Eigenschaft ist nicht sinnvoll, da Sie nicht standardisiert ist. Wenn diese Eigenschaft ein erforderliches Konstrukt wäre, wäre sie in der Vererbungs Hierarchie höher (für den Dienst). Diese Eigenschaft wird vom [**CIM- \_ NetworkService**](/previous-versions//cc136875(v=vs.85))geerbt.

</dd> <dt>

**StartupParameters**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Darf nicht verwendet werden. Ein frei Form Array von Zeichen folgen, die bestimmte Parameter angeben, die für die Start **Service** -Methode bereitgestellt werden müssen, damit dieser Dienst ordnungsgemäß gestartet wird. Wenn diese Methode optimiert wurde, würden diese Informationen von ihren Parametern eher formal vermittelt werden. Diese Eigenschaft wird vom [**CIM- \_ NetworkService**](/previous-versions//cc136875(v=vs.85))geerbt.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der aktuelle Status des Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**Status Beschreibungen**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**Systemkreationclassname**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name der Erstellungs Klasse des Bereichs Systems. Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.

</dd> <dt>

**Systemname**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der NetBIOS-Name des hostingcomputersystems. Diese Eigenschaft wird vom [**CIM- \_ Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.

</dd> <dt>

**Timeoflaststatechange**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Datum oder die Uhrzeit, zu dem der aktivierte Status des Elements zuletzt geändert wurde. Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt und wird nicht verwendet.

</dd> <dt>

**Transitioningumstate**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den Ziel Status an, in den die-Instanz übergeht. Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Zugriff auf die **MSVM-Klasse " \_ transparentbridgingservice** " kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**CIM- \_ transparentbridgingservice**](cim-transparentbridgingservice.md)
</dt> <dt>

[**CIM- \_ transparentbridgingservice**](/previous-versions/windows/desktop/clushyperv/cim-transparentbridgingservice)
</dt> </dl>

 

