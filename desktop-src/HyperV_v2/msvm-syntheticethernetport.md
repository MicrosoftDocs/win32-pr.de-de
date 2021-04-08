---
description: Stellt einen synthetischen Ethernet-Adapter dar.
ms.assetid: B5CB86A9-015B-42E8-ADF4-2F61970D8437
title: Msvm_SyntheticEthernetPort-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticEthernetPort
- Msvm_SyntheticEthernetPort.SetPowerState
- Msvm_SyntheticEthernetPort.EnableDevice
- Msvm_SyntheticEthernetPort.OnlineDevice
- Msvm_SyntheticEthernetPort.QuiesceDevice
- Msvm_SyntheticEthernetPort.SaveProperties
- Msvm_SyntheticEthernetPort.RestoreProperties
- Msvm_SyntheticEthernetPort.InstanceID
- Msvm_SyntheticEthernetPort.Caption
- Msvm_SyntheticEthernetPort.Description
- Msvm_SyntheticEthernetPort.ElementName
- Msvm_SyntheticEthernetPort.InstallDate
- Msvm_SyntheticEthernetPort.Name
- Msvm_SyntheticEthernetPort.OperationalStatus
- Msvm_SyntheticEthernetPort.StatusDescriptions
- Msvm_SyntheticEthernetPort.Status
- Msvm_SyntheticEthernetPort.HealthState
- Msvm_SyntheticEthernetPort.CommunicationStatus
- Msvm_SyntheticEthernetPort.DetailedStatus
- Msvm_SyntheticEthernetPort.OperatingStatus
- Msvm_SyntheticEthernetPort.PrimaryStatus
- Msvm_SyntheticEthernetPort.EnabledState
- Msvm_SyntheticEthernetPort.OtherEnabledState
- Msvm_SyntheticEthernetPort.RequestedState
- Msvm_SyntheticEthernetPort.EnabledDefault
- Msvm_SyntheticEthernetPort.TimeOfLastStateChange
- Msvm_SyntheticEthernetPort.AvailableRequestedStates
- Msvm_SyntheticEthernetPort.TransitioningToState
- Msvm_SyntheticEthernetPort.SystemCreationClassName
- Msvm_SyntheticEthernetPort.SystemName
- Msvm_SyntheticEthernetPort.CreationClassName
- Msvm_SyntheticEthernetPort.DeviceID
- Msvm_SyntheticEthernetPort.PowerManagementSupported
- Msvm_SyntheticEthernetPort.PowerManagementCapabilities
- Msvm_SyntheticEthernetPort.Availability
- Msvm_SyntheticEthernetPort.StatusInfo
- Msvm_SyntheticEthernetPort.LastErrorCode
- Msvm_SyntheticEthernetPort.ErrorDescription
- Msvm_SyntheticEthernetPort.ErrorCleared
- Msvm_SyntheticEthernetPort.OtherIdentifyingInfo
- Msvm_SyntheticEthernetPort.PowerOnHours
- Msvm_SyntheticEthernetPort.TotalPowerOnHours
- Msvm_SyntheticEthernetPort.IdentifyingDescriptions
- Msvm_SyntheticEthernetPort.AdditionalAvailability
- Msvm_SyntheticEthernetPort.MaxQuiesceTime
- Msvm_SyntheticEthernetPort.Speed
- Msvm_SyntheticEthernetPort.MaxSpeed
- Msvm_SyntheticEthernetPort.RequestedSpeed
- Msvm_SyntheticEthernetPort.UsageRestriction
- Msvm_SyntheticEthernetPort.PortType
- Msvm_SyntheticEthernetPort.OtherPortType
- Msvm_SyntheticEthernetPort.OtherNetworkPortType
- Msvm_SyntheticEthernetPort.PortNumber
- Msvm_SyntheticEthernetPort.LinkTechnology
- Msvm_SyntheticEthernetPort.OtherLinkTechnology
- Msvm_SyntheticEthernetPort.PermanentAddress
- Msvm_SyntheticEthernetPort.NetworkAddresses
- Msvm_SyntheticEthernetPort.FullDuplex
- Msvm_SyntheticEthernetPort.AutoSense
- Msvm_SyntheticEthernetPort.SupportedMaximumTransmissionUnit
- Msvm_SyntheticEthernetPort.ActiveMaximumTransmissionUnit
- Msvm_SyntheticEthernetPort.MaxDataSize
- Msvm_SyntheticEthernetPort.Capabilities
- Msvm_SyntheticEthernetPort.CapabilityDescriptions
- Msvm_SyntheticEthernetPort.EnabledCapabilities
- Msvm_SyntheticEthernetPort.OtherEnabledCapabilities
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c8e2a8c2207e410878a4f5c498ea71a1ce67cd8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863875"
---
# <a name="msvm_syntheticethernetport-class"></a>MSVM \_ syntheticethernetport-Klasse

Stellt einen synthetischen Ethernet-Adapter dar. Dieser Adapter ist der bevorzugte Netzwerkadapter aufgrund seiner Leistung und, da Änderungen an der IT sofort wirksam werden können, während Sie verwendet werden (Hot Configurability).

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticEthernetPort : CIM_EthernetPort
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  string   CreationClassName;
  string   DeviceID;
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  string   OtherIdentifyingInfo[];
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[] = 6;
  uint64   MaxQuiesceTime;
  uint64   Speed;
  uint64   MaxSpeed;
  uint64   RequestedSpeed;
  uint16   UsageRestriction;
  uint16   PortType;
  string   OtherPortType;
  string   OtherNetworkPortType;
  uint16   PortNumber;
  uint16   LinkTechnology;
  string   OtherLinkTechnology;
  string   PermanentAddress;
  string   NetworkAddresses[];
  boolean  FullDuplex;
  boolean  AutoSense;
  uint64   SupportedMaximumTransmissionUnit;
  uint64   ActiveMaximumTransmissionUnit;
  uint32   MaxDataSize;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  uint16   EnabledCapabilities[];
  string   OtherEnabledCapabilities[];
};
```

## <a name="members"></a>Member

Die **MSVM \_ syntheticethernetport** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **MSVM \_ syntheticethernetport** -Klasse verfügt über diese Methoden.



| Methode                                                                      | BESCHREIBUNG                              |
|:----------------------------------------------------------------------------|:-----------------------------------------|
| **EnableDevice**                                                            | Diese Methode wird nicht unterstützt.<br/> |
| **Onlinedevice**                                                            | Diese Methode wird nicht unterstützt.<br/> |
| **Inaktiven Geräte**                                                           | Diese Methode wird nicht unterstützt.<br/> |
| [**RequestStateChange**](msvm-syntheticethernetport-requeststatechange.md) | Fordert eine Statusänderung an.<br/>      |
| [**Zurücksetzen**](msvm-syntheticethernetport-reset.md)                           | Setzt das Gerät zurück.<br/>            |
| **Restoreproperties**                                                       | Diese Methode wird nicht unterstützt.<br/> |
| **SaveProperties**                                                          | Diese Methode wird nicht unterstützt.<br/> |
| **SetPowerState**                                                           | Diese Methode wird nicht unterstützt.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ syntheticethernetport** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Activemaximumtransmissionunit**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Einheiten** ("Bytes")
</dt> </dl>

Die aktive oder ausgehandelte maximale Übertragungseinheit (Maximum Transmission Unit, MTU), die unterstützt werden kann. Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.

</dd> <dt>

**Additionalavailability**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Zusätzliche Verfügbarkeit und Status des Geräts, über das hinaus, das in der **Availability** -Eigenschaft angegeben ist. Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt und ist immer auf 6 festgelegt (nicht zutreffend).

</dd> <dt>

**AutoSense**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der Netzwerkport die Geschwindigkeit oder andere Kommunikationsmerkmale der angeschlossenen Netzwerk Medien automatisch bestimmen kann. Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.

</dd> <dt>

**Verfügbarkeit**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die primäre Verfügbarkeit und den Status des Geräts. Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.

</dd> <dt>

**Availablerequestedstates**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die möglichen Werte für den *requestedstate* -Parameter der [**requestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) -Methode an, die zum Initiieren einer Zustandsänderung verwendet wird. Bei den aufgelisteten Werten handelt es sich um eine Teilmenge der Werte in der **requestedstaatsupported** -Eigenschaft der zugeordneten Instanz von **CIM \_ enabledlogicalelementfunctions**, bei der die ausgewählten Werte eine Funktion des aktuellen Zustands des [**CIM- \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))sind. Diese Eigenschaft darf nicht **null** sein, wenn eine Implementierung den Satz möglicher Werte als Funktion des aktuellen Zustands ankündigen kann. Diese Eigenschaft ist **null** , wenn eine Implementierung den Satz möglicher Werte nicht als Funktion des aktuellen Zustands bestimmen kann.

Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.

<dl> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (2)
</dt> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (3)
</dt> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Herunter** fahren (4)
</dt> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)
</dt> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)
</dt> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>Zurück **stellen (8** )
</dt> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>Still **legung (9** )
</dt> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Neustart** (10)
</dt> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Zurücksetzen** (11)
</dt> <dt>

<span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reserviert** (.. )
</dt> </dl>

</dd> <dt>

**Capabilities**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Funktionen des Ethernet-Ports. Das Gerät unterstützt z. b. alertonlan, wakeonlan, Lastenausgleich oder Failover. Wenn Failover-oder Lasten Ausgleichs Funktionen aufgelistet werden, sollte auch eine SpareGroup (Failover) oder extracapacitygroup (Lastenausgleich) definiert werden, um die Funktion vollständig zu beschreiben. Diese Eigenschaft wird vom [**CIM- \_ Ethernetport**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) geerbt und wird nicht verwendet.

</dd> <dt>

**Capabilitybeschreibungen**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Array von Freiform-Zeichen folgen, das Ausführlichere Erläuterungen für alle Ethernetport-Funktionen bereitstellt, die im Eigenschafts Array der **Funktionen** angegeben sind. Beachten Sie, dass jeder Eintrag dieses Arrays mit dem Eintrag im Eigenschafts Array " **Funktionen** " verknüpft ist, der sich am selben Index befindet. Diese Eigenschaft wird vom [**CIM- \_ Ethernetport**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) geerbt und wird nicht verwendet.

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

</dd> <dt>

**"Name der Klassenname"**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name der Klasse oder der Unterklasse, die bei der Erstellung einer-Instanz verwendet wird. Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.

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

</dd> <dt>

**DeviceID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Adresse oder andere identifizierende Informationen, die verwendet werden, um das logische Gerät eindeutig zu benennen. Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Anzeige Name für das-Objekt. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**Enabled-Funktionen**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Funktionen, die in der Liste aller unterstützten Funktionen aktiviert sind, die im Eigenschafts Array " **Funktionen** " definiert sind. Diese Eigenschaft wird vom [**CIM- \_ Ethernetport**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)geerbt, aber nicht verwendet.

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

Der aktivierte und deaktivierte Status dieses Elements. Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.

</dd> <dt>

**Errorgelöscht**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.

</dd> <dt>

**Vollduplex**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der Port im Vollduplex Modus betrieben wird. Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der aktuelle Zustand des Elements. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**IdentifyingDescriptions**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Array von Freiform-Zeichen folgen, die Erklärungen und Details hinter den Einträgen im " **OtherIdentifyingInfo** "-Array bereitstellen. Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) geerbt und wird nicht verwendet.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Datum, an dem der Ethernet-Port dem virtuellen Computer hinzugefügt wurde. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

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

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.

</dd> <dt>

**Linktechnology**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Enumeration der Linktypen. Wenn der Wert auf 1 (Other) festgelegt ist, enthält die zugehörige Eigenschaft **otherlinktechnology** eine Zeichen folgen Beschreibung des linktyps. Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.

<dl> <dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)
</dt> </dl>

</dd> <dt>

**Maxdatasize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die maximale Größe des Felds Info (nicht-Mac), das empfangen oder übertragen wird. Diese Eigenschaft wird vom [**CIM- \_ Ethernetport**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)geerbt.

</dd> <dt>

**Maxquiescetime**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.

</dd> <dt>

**MAXSPEED**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Einheiten** ("Bits pro Sekunde")
</dt> </dl>

Die maximale Bandbreite des Ports in Bits pro Sekunde. Diese Eigenschaft wird von [**CIM \_ logicalport**](/previous-versions//cc136869(v=vs.85))geerbt.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Anzeige Name für das-Objekt. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**"Networkaddresses"**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ethernet/802.3-Mac-Adressen, die als zwölf hexadezimal Ziffern formatiert sind (z. b. "010203040506"), wobei jedes Paar eines der sechs Oktette der Mac-Adresse in kanonischer bidirektionalen Reihenfolge darstellt (das Gruppen Adressbit befindet sich im niedrig wertigen Bit des ersten Zeichens der Zeichenfolge). Diese Eigenschaft wird vom [**CIM- \_ Ethernetport**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)geerbt und wird nicht verwendet.

</dd> <dt>

**Operatingstatus**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Stellt aktuelle Statusinformationen für den Betriebszustand des-Elements bereit und kann verwendet werden, um weitere Details in Bezug auf den Wert der **enabledstate** -Eigenschaft bereitzustellen. Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der aktuelle Status des Elements. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und ist immer auf 2 (OK) festgelegt.

</dd> <dt>

**Otherenabled-Funktionen**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Array von Freiform-Zeichen folgen, das Ausführlichere Erläuterungen für jede der aktivierten Funktionen bereitstellt, die als "Other" angegeben sind. Diese Eigenschaft wird vom [**CIM- \_ Ethernetport**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) geerbt und wird nicht verwendet.

</dd> <dt>

**Otherenabledstate**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der aktivierte oder deaktivierte Status des Elements, wenn die **enabledstate** -Eigenschaft auf 1 (Sonstiges) festgelegt ist. Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Alle Daten, zusätzlich zu den Informationen zur Geräte-ID, die zum Identifizieren eines logischen Geräts verwendet werden könnten. Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) geerbt und wird nicht verwendet.

</dd> <dt>

**Otherlinktechnology**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Zeichen folgen Wert, der **linktechnology** beschreibt, wenn es auf 1 (Sonstiges) festgelegt ist. Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.

</dd> <dt>

**Othernetworkporttype**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport) geerbt und auf **null** festgelegt.

</dd> <dt>

**Otherporttype**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Modultyp, wenn **portType** auf 1 (Other) festgelegt ist. Diese Eigenschaft wird von [**CIM \_ logicalport**](/previous-versions//cc136869(v=vs.85))geerbt.

</dd> <dt>

**Permanent Address**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Netzwerkadresse, die in den Port hart codiert ist. Diese hart codierte Adresse kann mithilfe eines Firmwareupdates oder einer Softwarekonfiguration geändert werden. Wenn diese Änderung vorgenommen wird, sollte das Feld gleichzeitig aktualisiert werden. Die **permanentaddress** -Eigenschaft sollte leer gelassen werden, wenn keine hart codierte Adresse für den Netzwerkadapter vorhanden ist. Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.

</dd> <dt>

**PortNumber**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Netzwerkports sind häufig in Bezug auf ein logisches Modul oder ein Netzwerkelement nummeriert. Dieser Wert ist 1 für emulierten NICs, 0 für alle anderen. Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.

</dd> <dt>

**PortType**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der bestimmte Modus, der derzeit für den Port aktiviert ist. Wenn der Wert auf 1 (Sonstiges) festgelegt ist, enthält die zugehörige Eigenschaft **otherporttype** eine Zeichen folgen Beschreibung für den Porttyp. Diese Eigenschaft wird vom [**CIM- \_ Ethernetport**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)geerbt.

</dd> <dt>

**Powermanagementfunktionen**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.

</dd> <dt>

**Powermanagementsupported**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.

</dd> <dt>

**Poweronhours**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.

</dd> <dt>

**Primarystatus**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Stellt Statusinformationen auf hoher Ebene bereit. Diese Eigenschaft sollte in Verbindung mit der **detailedstatus** -Eigenschaft verwendet werden, um allgemeine und ausführliche Integritäts Statusinformationen für das-Element und seine unter Komponenten bereitzustellen. Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**RequestedSpeed**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Einheiten** ("Bits pro Sekunde")
</dt> </dl>

Die angeforderte Bandbreite des Ports (in Bits pro Sekunde). Die tatsächliche Bandbreite wird in der Eigenschaft **Geschwindigkeit** gemeldet. Diese Eigenschaft wird von [**CIM \_ logicalport**](/previous-versions//cc136869(v=vs.85))geerbt.

</dd> <dt>

**RequestedState**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der zuletzt angeforderte oder gewünschte Status für den Verwaltungsdienst. Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.

</dd> <dt>

**Geschwindigkeit**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Einheiten** ("Bits pro Sekunde")
</dt> </dl>

Die aktuelle Bandbreite des Ports (in Bits pro Sekunde). Für Ports, die die Bandbreite variieren, oder für diejenigen, bei denen keine genaue Schätzung vorgenommen werden kann, sollte diese Eigenschaft die nominale Bandbreite enthalten. Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der aktuelle Status des Elements. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

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

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.

</dd> <dt>

**Supportedmaximumtransmissionunit**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Einheiten** ("Bytes")
</dt> </dl>

Die maximale Übertragungseinheit (MTU), die unterstützt werden kann. Diese Eigenschaft wird vom [**CIM- \_ Netzwerkport**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)geerbt.

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

Der NetBIOS-Name des hostingcomputersystems. Diese Eigenschaft enthält die ID der virtuellen Maschine im **GUID** -Format. Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt.

</dd> <dt>

**Timeoflaststatechange**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Datum oder die Uhrzeit, zu dem der aktivierte Status des Elements zuletzt geändert wurde. Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.

</dd> <dt>

**Totalpoweronhours**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)geerbt, aber nicht verwendet.

</dd> <dt>

**Transitioningumstate**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den Ziel Status an, in den die-Instanz übergeht. Diese Eigenschaft wird von [**CIM \_ enabledlogicalelement**](/previous-versions//cc136818(v=vs.85))geerbt.

</dd> <dt>

**Einsatz Einschränkung**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Unter bestimmten Umständen kann ein logischer Port als Front-End-oder Back-End-Port identifiziert werden. Wenn keine Einschränkung für die Verwendung des Ports vorliegt, sollte der Wert auf 4 (nicht eingeschränkt) festgelegt werden. Diese Eigenschaft wird von [**CIM \_ logicalport**](/previous-versions//cc136869(v=vs.85))geerbt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Zugriff auf die **MSVM \_ syntheticethernetport** -Klasse kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="examples"></a>Beispiele

Weitere Informationen finden Sie unter [Abfragen von Netzwerk Objekten](querying-networking-objects.md).

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

[**CIM- \_ Ethernetport**](cim-ethernetport.md)
</dt> <dt>

[**CIM- \_ Ethernetport**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)
</dt> </dl>

 

