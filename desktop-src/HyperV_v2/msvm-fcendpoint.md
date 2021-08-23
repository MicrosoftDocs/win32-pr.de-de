---
description: Stellt den logischen Verbindungspunkt für einen Fibre Channel dar.
ms.assetid: 54e9cb76-04f2-417b-b250-1b3156772694
title: Msvm_FcEndpoint-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FcEndpoint
- Msvm_FcEndpoint.InstanceID
- Msvm_FcEndpoint.Caption
- Msvm_FcEndpoint.Description
- Msvm_FcEndpoint.ElementName
- Msvm_FcEndpoint.InstallDate
- Msvm_FcEndpoint.Name
- Msvm_FcEndpoint.OperationalStatus
- Msvm_FcEndpoint.StatusDescriptions
- Msvm_FcEndpoint.Status
- Msvm_FcEndpoint.HealthState
- Msvm_FcEndpoint.CommunicationStatus
- Msvm_FcEndpoint.DetailedStatus
- Msvm_FcEndpoint.OperatingStatus
- Msvm_FcEndpoint.PrimaryStatus
- Msvm_FcEndpoint.EnabledState
- Msvm_FcEndpoint.OtherEnabledState
- Msvm_FcEndpoint.RequestedState
- Msvm_FcEndpoint.EnabledDefault
- Msvm_FcEndpoint.TimeOfLastStateChange
- Msvm_FcEndpoint.AvailableRequestedStates
- Msvm_FcEndpoint.TransitioningToState
- Msvm_FcEndpoint.SystemCreationClassName
- Msvm_FcEndpoint.SystemName
- Msvm_FcEndpoint.CreationClassName
- Msvm_FcEndpoint.NameFormat
- Msvm_FcEndpoint.ProtocolType
- Msvm_FcEndpoint.ProtocolIFType
- Msvm_FcEndpoint.OtherTypeDescription
- Msvm_FcEndpoint.Connected
- Msvm_FcEndpoint.WWPN
- Msvm_FcEndpoint.WWNN
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a49440158beffb159b2f931283cf902a21ca5c9de1addac462b494c30eec2100
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119523390"
---
# <a name="msvm_fcendpoint-class"></a>Msvm \_ FcEndpoint-Klasse

Stellt den logischen Verbindungspunkt für einen Fibre Channel dar. Wenn der Fibre Channel-Endpunkt mit einem Switchport verbunden ist, verfügt Fibre Channel port, der mit dem Fibre Channel-Endpunkt verbunden ist, über Fibre Channel Konnektivität.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FcEndpoint : CIM_ProtocolEndpoint
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  string   CreationClassName;
  string   NameFormat;
  uint16   ProtocolType;
  uint16   ProtocolIFType;
  string   OtherTypeDescription;
  boolean  Connected;
  string   WWPN;
  string   WWNN;
};
```

## <a name="members"></a>Member

Die **Msvm \_ FcEndpoint-Klasse** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Msvm \_ FcEndpoint-Klasse** verfügt über diese Methoden.



| Methode                                                           | Beschreibung                         |
|:-----------------------------------------------------------------|:------------------------------------|
| [**RequestStateChange**](msvm-fcendpoint-requeststatechange.md) | Fordert eine Zustandsänderung an.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ FcEndpoint-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**AvailableRequestedStates**
</dt> <dd> <dl> <dt>

Datentyp: **uint16 array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die möglichen Werte für den *RequestedState-Parameter* der [**RequestStateChange-Methode**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) an, die zum Initiieren einer Zustandsänderung verwendet wird. Die aufgeführten Werte sind eine Teilmenge der Werte, die in der **RequestedStatesSupported-Eigenschaft** der zugeordneten Instanz von **CIM \_ EnabledLogicalElementCapabilities** enthalten sind, wobei die ausgewählten Werte eine Funktion des aktuellen Zustands der [**CIM \_ EnabledLogicalElement-Klasse**](/previous-versions//cc136818(v=vs.85)) sind. Diese Eigenschaft kann nicht NULL sein, wenn eine Implementierung den Satz möglicher Werte als Funktion des aktuellen Zustands anknullen kann. Diese Eigenschaft ist **NULL,** wenn eine Implementierung den Satz möglicher Werte nicht als Funktion des aktuellen Zustands bestimmen kann.

Diese Eigenschaft wird von [**CIM \_ EnabledLogicalElement geerbt.**](/previous-versions//cc136818(v=vs.85))

<dl> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (2)
</dt> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (3)
</dt> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Herunterfahren** (4)
</dt> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)
</dt> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)
</dt> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Zurückern** (8)
</dt> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Ruhe** (9)
</dt> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Neustart** (10)
</dt> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Zurücksetzen** (11)
</dt> <dt>

<span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (.. )
</dt> </dl>

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine kurze Beschreibung des Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedElement geerbt.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**CommunicationStatus**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die Fähigkeit der Instrumentierung an, mit dem zugrunde liegenden verwalteten Element zu kommunizieren. Ein **NULL-Wert** gibt an, dass diese Eigenschaft nicht implementiert ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**Verbunden**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird auf True **festgelegt,** wenn Fibre Channel Endpunkt aktiv mit einem anderen Endpunkt Fibre Channel ist.

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Key**, **MaxLen** ( 256 )
</dt> </dl>

Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird. Diese Eigenschaft wird von [**CIM \_ ServiceAccessPoint geerbt.**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedElement geerbt.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**DetailedStatus**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ergänzt die **PrimaryStatus-Eigenschaft** durch zusätzliche Statusdetails. Ein **NULL-Wert** gibt an, dass diese Eigenschaft nicht implementiert ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Anzeigename für das Objekt. Diese Eigenschaft wird von [**CIM \_ ManagedElement geerbt.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**EnabledDefault**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Standard- oder Startkonfiguration eines Administrators für den aktivierten Zustand eines Elements. Diese Eigenschaft wird von [**CIM \_ EnabledLogicalElement geerbt**](/previous-versions//cc136818(v=vs.85))und ist einer der folgenden Werte.

<dl> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (2)
</dt> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (3)
</dt> <dt>

<span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Aktiviert, aber offline** (6)
</dt> </dl>

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den aktivierten Zustand des geplanten Systems an. Diese Eigenschaft wird von [**CIM \_ EnabledLogicalElement geerbt**](/previous-versions//cc136818(v=vs.85))und kann einer der folgenden Werte sein.



| Wert                                                                                                                                                                                                                                                                       | Bedeutung                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <dt>**Deaktiviert**</dt> <dt>3</dt> </dl>                                             | Das System ist deaktiviert.<br/>                                             |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <dt>**Nicht zutreffend**</dt> <dt>5</dt> </dl>                     | Das -Element unterstützt nicht das Aktivieren oder Deaktivieren.<br/>               |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <dt>**Aktiviert, aber offline**</dt> <dt>6</dt> </dl> | Das System ist aktiviert, aber offline. Alle neuen Anforderungen werden gelöscht.<br/> |



 

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die aktuelle Integrität des Elements. Diese Eigenschaft drückt die Integrität dieses Elements aus, jedoch nicht notwendigerweise die Integrität seiner Unterkomponenten. Die möglichen Werte sind 0 bis 30, wobei 5 bedeutet, dass das Element vollständig fehlerfrei ist und 30 bedeutet, dass das Element vollständig nicht funktionslos ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Datum und die Uhrzeit der Erstellung der Konfiguration des virtuellen Computers. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Identifiziert eine Instanz dieser Klasse eindeutig. Diese Eigenschaft wird von [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Bezeichnung, mit der das Objekt bekannt ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**NameFormat**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **MaxLen** ( 256 )
</dt> </dl>

Enthält die Namensheuristik, die ausgewählt wird, um sicherzustellen, dass der Wert der **Name-Eigenschaft** eindeutig ist. Diese Eigenschaft wird von [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint)geerbt.

</dd> <dt>

**OperatingStatus**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Stellt aktuelle Statusinformationen für die Betriebsbedingung des Elements bereit und kann zum Bereitstellen weiterer Details in Bezug auf den Wert der **EnabledState-Eigenschaft** verwendet werden. Ein **NULL-Wert** gibt an, dass diese Eigenschaft nicht implementiert ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Datentyp: **uint16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die aktuellen Status des -Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**OtherEnabledState**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die den aktivierten oder deaktivierten Zustand des Elements beschreibt, wenn die **EnabledState-Eigenschaft** auf 1 ("Other") festgelegt ist. Diese Eigenschaft muss auf **NULL** festgelegt werden, wenn **EnabledState** ein anderer Wert als 1 ist. Diese Eigenschaft wird von [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))geerbt und immer auf **NULL** festgelegt.

</dd> <dt>

**OtherTypeDescription**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **MaxLen** ( 64 )
</dt> </dl>

Eine Zeichenfolge, die den Typ des Protokollendpunkts beschreibt, wenn die **ProtocolIFType-Eigenschaft** dieser Klasse (oder einer ihrer Unterklassen) auf 1 (Sonstige) festgelegt ist. Diese Eigenschaft sollte auf **NULL** festgelegt werden, wenn die **ProtocolIFType-Eigenschaft** ein anderer Wert als 1 ist. Diese Eigenschaft wird von [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint)geerbt.

</dd> <dt>

**PrimaryStatus**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Stellt statusinformationen auf hoher Ebene bereit. Diese Eigenschaft sollte in Verbindung mit der **DetailedStatus-Eigenschaft** verwendet werden, um detaillierte und detaillierte Integritätsstatusinformationen für das Element und seine Unterkomponenten bereitzustellen. Ein **NULL-Wert** gibt an, dass diese Eigenschaft nicht implementiert ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**ProtocolIFType**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die -Eigenschaft wird verwendet, um Instanzen dieser Klasse zu kategorisieren und zu klassifizieren. Wenn **ProtocolIFType** auf 1 (Other) festgelegt ist, sollten die Typinformationen in der **OtherTypeDescription-Eigenschaft** bereitgestellt werden. Diese Eigenschaft wird von [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint)geerbt.

> [!Note]  
> **ProtocolIFType** ist eine Enumeration, die mit dem [IANA ifType MIB](https://www.iana.org/assignments/ianaiftype-mib)synchronisiert wird. Zusätzliche Werte, die von dmtf definiert werden, sind ebenfalls enthalten.

 

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Andere** (1)
</dt> <dt>

<span id="Regular_1822"></span><span id="regular_1822"></span><span id="REGULAR_1822"></span>**Regular 1822** (2)
</dt> <dt>

<span id="HDH_1822"></span><span id="hdh_1822"></span>**HDH 1822** (3)
</dt> <dt>

<span id="DDN_X.25"></span><span id="ddn_x.25"></span>**DDN X.25** (4)
</dt> <dt>

<span id="RFC877_X.25"></span><span id="rfc877_x.25"></span>**RFC877 X.25** (5)
</dt> <dt>

<span id="Ethernet_CSMA_CD"></span><span id="ethernet_csma_cd"></span><span id="ETHERNET_CSMA_CD"></span>**Ethernet CSMA/CD** (6)
</dt> <dt>

<span id="ISO_802.3_CSMA_CD"></span><span id="iso_802.3_csma_cd"></span>**ISO 802.3 CSMA/CD** (7)
</dt> <dt>

<span id="ISO_802.4_Token_Bus"></span><span id="iso_802.4_token_bus"></span><span id="ISO_802.4_TOKEN_BUS"></span>**ISO 802.4 Token Bus** (8)
</dt> <dt>

<span id="ISO_802.5_Token_Ring"></span><span id="iso_802.5_token_ring"></span><span id="ISO_802.5_TOKEN_RING"></span>**ISO 802.5-Tokenring** (9)
</dt> <dt>

<span id="ISO_802.6_MAN"></span><span id="iso_802.6_man"></span>**ISO 802.6 MAN** (10)
</dt> <dt>

<span id="StarLAN"></span><span id="starlan"></span><span id="STARLAN"></span>**StarLAN** (11)
</dt> <dt>

<span id="Proteon_10Mbit"></span><span id="proteon_10mbit"></span><span id="PROTEON_10MBIT"></span>**Sollon 10Mbit** (12)
</dt> <dt>

<span id="Proteon_80Mbit"></span><span id="proteon_80mbit"></span><span id="PROTEON_80MBIT"></span>**Sollon 80Mbit** (13)
</dt> <dt>

<span id="HyperChannel"></span><span id="hyperchannel"></span><span id="HYPERCHANNEL"></span>**HyperChannel** (14)
</dt> <dt>

<span id="FDDI"></span><span id="fddi"></span>**FDDI** (15)
</dt> <dt>

<span id="LAP-B"></span><span id="lap-b"></span>**LAP-B** (16)
</dt> <dt>

<span id="SDLC"></span><span id="sdlc"></span>**SDLC** (17)
</dt> <dt>

<span id="DS1"></span><span id="ds1"></span>**DS1** (18)
</dt> <dt>

<span id="E1"></span><span id="e1"></span>**E1** (19)
</dt> <dt>

<span id="Basic_ISDN"></span><span id="basic_isdn"></span><span id="BASIC_ISDN"></span>**Standard-ISDN** (20)
</dt> <dt>

<span id="Primary_ISDN"></span><span id="primary_isdn"></span><span id="PRIMARY_ISDN"></span>**Primärer ISDN** (21)
</dt> <dt>

<span id="Proprietary_Point-to-Point_Serial"></span><span id="proprietary_point-to-point_serial"></span><span id="PROPRIETARY_POINT-TO-POINT_SERIAL"></span>**Proprietäre Point-to-Point-Serie** (22)
</dt> <dt>

<span id="PPP"></span><span id="ppp"></span>**PPP** (23)
</dt> <dt>

<span id="Software_Loopback"></span><span id="software_loopback"></span><span id="SOFTWARE_LOOPBACK"></span>**Software-Loopback** (24)
</dt> <dt>

<span id="EON"></span><span id="eon"></span>**EON** (25)
</dt> <dt>

<span id="Ethernet_3Mbit"></span><span id="ethernet_3mbit"></span><span id="ETHERNET_3MBIT"></span>**Ethernet 3Mbit** (26)
</dt> <dt>

<span id="NSIP"></span><span id="nsip"></span>**NSIP** (27)
</dt> <dt>

<span id="SLIP"></span><span id="slip"></span>**SLIP** (28)
</dt> <dt>

<span id="Ultra"></span><span id="ultra"></span><span id="ULTRA"></span>**Ultra** (29)
</dt> <dt>

<span id="DS3"></span><span id="ds3"></span>**DS3** (30)
</dt> <dt>

<span id="SIP"></span><span id="sip"></span>**SIP** (31)
</dt> <dt>

<span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (32)
</dt> <dt>

<span id="RS-232"></span><span id="rs-232"></span>**RS-232** (33)
</dt> <dt>

<span id="Parallel"></span><span id="parallel"></span><span id="PARALLEL"></span>**Parallel** (34)
</dt> <dt>

<span id="ARCNet"></span><span id="arcnet"></span><span id="ARCNET"></span>**ARCNet** (35)
</dt> <dt>

<span id="ARCNet_Plus"></span><span id="arcnet_plus"></span><span id="ARCNET_PLUS"></span>**ARCNet Plus** (36)
</dt> <dt>

<span id="ATM"></span><span id="atm"></span>**GELDAUTOMATEN** (37)
</dt> <dt>

<span id="MIO_X.25"></span><span id="mio_x.25"></span>**MIO X.25** (38)
</dt> <dt>

<span id="SONET"></span><span id="sonet"></span>**SONET** (39)
</dt> <dt>

<span id="X.25_PLE"></span><span id="x.25_ple"></span>**X.25 XI** (40)
</dt> <dt>

<span id="ISO_802.211c"></span><span id="iso_802.211c"></span><span id="ISO_802.211C"></span>**ISO 802.211c** (41)
</dt> <dt>

<span id="LocalTalk"></span><span id="localtalk"></span><span id="LOCALTALK"></span>**LocalTalk** (42)
</dt> <dt>

<span id="SMDS_DXI"></span><span id="smds_dxi"></span>**SMDS DXI** (43)
</dt> <dt>

<span id="Frame_Relay_Service"></span><span id="frame_relay_service"></span><span id="FRAME_RELAY_SERVICE"></span>**Frame Relay-Dienst** (44)
</dt> <dt>

<span id="V.35"></span><span id="v.35"></span>**V.35** (45)
</dt> <dt>

<span id="HSSI"></span><span id="hssi"></span>**HSSI** (46)
</dt> <dt>

<span id="HIPPI"></span><span id="hippi"></span>**HIPI** (47)
</dt> <dt>

<span id="Modem"></span><span id="modem"></span><span id="MODEM"></span>**Modem** (48)
</dt> <dt>

<span id="AAL5"></span><span id="aal5"></span>**AAL5** (49)
</dt> <dt>

<span id="SONET_Path"></span><span id="sonet_path"></span><span id="SONET_PATH"></span>**SONET-Pfad** (50)
</dt> <dt>

<span id="SONET_VT"></span><span id="sonet_vt"></span>**SONET VT** (51)
</dt> <dt>

<span id="SMDS_ICIP"></span><span id="smds_icip"></span>**SMDS ICIP** (52)
</dt> <dt>

<span id="Proprietary_Virtual_Internal"></span><span id="proprietary_virtual_internal"></span><span id="PROPRIETARY_VIRTUAL_INTERNAL"></span>**Proprietäre virtuelle/interne** (53)
</dt> <dt>

<span id="Proprietary_Multiplexor"></span><span id="proprietary_multiplexor"></span><span id="PROPRIETARY_MULTIPLEXOR"></span>**Proprietärer Multiplexor** (54)
</dt> <dt>

<span id="IEEE_802.12"></span><span id="ieee_802.12"></span>**IEEE 802.12** (55)
</dt> <dt>

<span id="Fibre_Channel"></span><span id="fibre_channel"></span><span id="FIBRE_CHANNEL"></span>**Fibre Channel** (56)
</dt> <dt>

<span id="HIPPI_Interface"></span><span id="hippi_interface"></span><span id="HIPPI_INTERFACE"></span>**FÜHRUNGI-Schnittstelle** (57)
</dt> <dt>

<span id="Frame_Relay_Interconnect"></span><span id="frame_relay_interconnect"></span><span id="FRAME_RELAY_INTERCONNECT"></span>**Frame Relay Interconnect** (58)
</dt> <dt>

<span id="ATM_Emulated_LAN_for_802.3"></span><span id="atm_emulated_lan_for_802.3"></span><span id="ATM_EMULATED_LAN_FOR_802.3"></span>**EMULIERTES LAN für 802.3** (59)
</dt> <dt>

<span id="ATM_Emulated_LAN_for_802.5"></span><span id="atm_emulated_lan_for_802.5"></span><span id="ATM_EMULATED_LAN_FOR_802.5"></span>**ATM Emulated LAN for 802.5 (60) (EMULATED LAN für 802.5** (60))
</dt> <dt>

<span id="ATM_Emulated_Circuit"></span><span id="atm_emulated_circuit"></span><span id="ATM_EMULATED_CIRCUIT"></span>**Emulierte ATM-Leitung** (61)
</dt> <dt>

<span id="Fast_Ethernet__100BaseT_"></span><span id="fast_ethernet__100baset_"></span><span id="FAST_ETHERNET__100BASET_"></span>**Fast Ethernet (100BaseT)** (62)
</dt> <dt>

<span id="ISDN"></span><span id="isdn"></span>**ISDN** (63)
</dt> <dt>

<span id="V.11"></span><span id="v.11"></span>**V.11** (64)
</dt> <dt>

<span id="V.36"></span><span id="v.36"></span>**V.36** (65)
</dt> <dt>

<span id="G703_at_64K"></span><span id="g703_at_64k"></span><span id="G703_AT_64K"></span>**G703 bei 64K** (66)
</dt> <dt>

<span id="G703_at_2Mb"></span><span id="g703_at_2mb"></span><span id="G703_AT_2MB"></span>**G703 bei 2 MB** (67)
</dt> <dt>

<span id="QLLC"></span><span id="qllc"></span>**QLLC** (68)
</dt> <dt>

<span id="Fast_Ethernet_100BaseFX"></span><span id="fast_ethernet_100basefx"></span><span id="FAST_ETHERNET_100BASEFX"></span>**Fast Ethernet 100BaseFX** (69)
</dt> <dt>

<span id="Channel"></span><span id="channel"></span><span id="CHANNEL"></span>**Kanal** (70)
</dt> <dt>

<span id="IEEE_802.11"></span><span id="ieee_802.11"></span>**IEEE 802.11** (71)
</dt> <dt>

<span id="IBM_260_370_OEMI_Channel"></span><span id="ibm_260_370_oemi_channel"></span><span id="IBM_260_370_OEMI_CHANNEL"></span>**IBM 260/370 OEMI-Kanal** (72)
</dt> <dt>

<span id="ESCON"></span><span id="escon"></span>**ESCON** (73)
</dt> <dt>

<span id="Data_Link_Switching"></span><span id="data_link_switching"></span><span id="DATA_LINK_SWITCHING"></span>**Datenlinkwechsel** (74)
</dt> <dt>

<span id="ISDN_S_T_Interface"></span><span id="isdn_s_t_interface"></span><span id="ISDN_S_T_INTERFACE"></span>**ISDN-S/T-Schnittstelle** (75)
</dt> <dt>

<span id="ISDN_U_Interface"></span><span id="isdn_u_interface"></span><span id="ISDN_U_INTERFACE"></span>**ISDN U-Schnittstelle** (76)
</dt> <dt>

<span id="LAP-D"></span><span id="lap-d"></span>**LAP-D** (77)
</dt> <dt>

<span id="IP_Switch"></span><span id="ip_switch"></span><span id="IP_SWITCH"></span>**IP-Switch** (78)
</dt> <dt>

<span id="Remote_Source_Route_Bridging"></span><span id="remote_source_route_bridging"></span><span id="REMOTE_SOURCE_ROUTE_BRIDGING"></span>**Remote Source Route Bridging** (79)
</dt> <dt>

<span id="ATM_Logical"></span><span id="atm_logical"></span><span id="ATM_LOGICAL"></span>**ATM Logical** (80)
</dt> <dt>

<span id="DS0"></span><span id="ds0"></span>**DS0** (81)
</dt> <dt>

<span id="DS0_Bundle"></span><span id="ds0_bundle"></span><span id="DS0_BUNDLE"></span>**DS0 Bundle** (82)
</dt> <dt>

<span id="BSC"></span><span id="bsc"></span>**BSC** (83)
</dt> <dt>

<span id="Async"></span><span id="async"></span><span id="ASYNC"></span>**Async** (84)
</dt> <dt>

<span id="Combat_Net_Radio"></span><span id="combat_net_radio"></span><span id="COMBAT_NET_RADIO"></span>**Netz radio** (85)
</dt> <dt>

<span id="ISO_802.5r_DTR"></span><span id="iso_802.5r_dtr"></span><span id="ISO_802.5R_DTR"></span>**ISO 802.5r DTR** (86)
</dt> <dt>

<span id="Ext_Pos_Loc_Report_System"></span><span id="ext_pos_loc_report_system"></span><span id="EXT_POS_LOC_REPORT_SYSTEM"></span>**Ext Pos Loc Report System** (87)
</dt> <dt>

<span id="AppleTalk_Remote_Access_Protocol"></span><span id="appletalk_remote_access_protocol"></span><span id="APPLETALK_REMOTE_ACCESS_PROTOCOL"></span>**AppleTalk-Remotezugriffsprotokoll** (88)
</dt> <dt>

<span id="Proprietary_Connectionless"></span><span id="proprietary_connectionless"></span><span id="PROPRIETARY_CONNECTIONLESS"></span>**Proprietäres verbindungsloses** (89)
</dt> <dt>

<span id="ITU_X.29_Host_PAD"></span><span id="itu_x.29_host_pad"></span><span id="ITU_X.29_HOST_PAD"></span>**ITU X.29 Host PAD** (90)
</dt> <dt>

<span id="ITU_X.3_Terminal_PAD"></span><span id="itu_x.3_terminal_pad"></span><span id="ITU_X.3_TERMINAL_PAD"></span>**ITU X.3 Terminal PAD** (91)
</dt> <dt>

<span id="Frame_Relay_MPI"></span><span id="frame_relay_mpi"></span><span id="FRAME_RELAY_MPI"></span>**Frame Relay MPI** (92)
</dt> <dt>

<span id="ITU_X.213"></span><span id="itu_x.213"></span>**ITU X.213** (93)
</dt> <dt>

<span id="ADSL"></span><span id="adsl"></span>**ADSL** (94)
</dt> <dt>

<span id="RADSL"></span><span id="radsl"></span>**RADSL** (95)
</dt> <dt>

<span id="SDSL"></span><span id="sdsl"></span>**SDSL** (96)
</dt> <dt>

<span id="VDSL"></span><span id="vdsl"></span>**VDSL** (97)
</dt> <dt>

<span id="ISO_802.5_CRFP"></span><span id="iso_802.5_crfp"></span>**ISO 802.5 CRFP** (98)
</dt> <dt>

<span id="Myrinet"></span><span id="myrinet"></span><span id="MYRINET"></span>**Myolet** (99)
</dt> <dt>

<span id="Voice_Receive_and_Transmit"></span><span id="voice_receive_and_transmit"></span><span id="VOICE_RECEIVE_AND_TRANSMIT"></span>**Empfangen und Übertragen von Stimmen** (100)
</dt> <dt>

<span id="Voice_Foreign_Exchange_Office"></span><span id="voice_foreign_exchange_office"></span><span id="VOICE_FOREIGN_EXCHANGE_OFFICE"></span>**Voice Foreign Exchange Office** (101)
</dt> <dt>

<span id="Voice_Foreign_Exchange_Service"></span><span id="voice_foreign_exchange_service"></span><span id="VOICE_FOREIGN_EXCHANGE_SERVICE"></span>**Voice Foreign Exchange Service** (102)
</dt> <dt>

<span id="Voice_Encapsulation"></span><span id="voice_encapsulation"></span><span id="VOICE_ENCAPSULATION"></span>**Sprachkapselung** (103)
</dt> <dt>

<span id="Voice_over_IP"></span><span id="voice_over_ip"></span><span id="VOICE_OVER_IP"></span>**Voice over IP** (104)
</dt> <dt>

<span id="ATM_DXI"></span><span id="atm_dxi"></span>**ATM DXI** (105)
</dt> <dt>

<span id="ATM_FUNI"></span><span id="atm_funi"></span>**ATM FUNI** (106)
</dt> <dt>

<span id="ATM_IMA"></span><span id="atm_ima"></span>**ATM IMA** (107)
</dt> <dt>

<span id="PPP_Multilink_Bundle"></span><span id="ppp_multilink_bundle"></span><span id="PPP_MULTILINK_BUNDLE"></span>**PPP Multilink Bundle** (108)
</dt> <dt>

<span id="IP_over_CDLC"></span><span id="ip_over_cdlc"></span><span id="IP_OVER_CDLC"></span>**IP über CDLC** (109)
</dt> <dt>

<span id="IP_over_CLAW"></span><span id="ip_over_claw"></span><span id="IP_OVER_CLAW"></span>**IP über CLAW** (110)
</dt> <dt>

<span id="Stack_to_Stack"></span><span id="stack_to_stack"></span><span id="STACK_TO_STACK"></span>**Stack to Stack** (111)
</dt> <dt>

<span id="Virtual_IP_Address"></span><span id="virtual_ip_address"></span><span id="VIRTUAL_IP_ADDRESS"></span>**Virtuelle IP-Adresse** (112)
</dt> <dt>

<span id="MPC"></span><span id="mpc"></span>**MPC** (113)
</dt> <dt>

<span id="IP_over_ATM"></span><span id="ip_over_atm"></span><span id="IP_OVER_ATM"></span>**IP über Geldautomaten** (114)
</dt> <dt>

<span id="ISO_802.5j_Fibre_Token_Ring"></span><span id="iso_802.5j_fibre_token_ring"></span><span id="ISO_802.5J_FIBRE_TOKEN_RING"></span>**ISO 802.5j Fibre Token Ring** (115)
</dt> <dt>

<span id="TDLC"></span><span id="tdlc"></span>**TDLC** (116)
</dt> <dt>

<span id="Gigabit_Ethernet"></span><span id="gigabit_ethernet"></span><span id="GIGABIT_ETHERNET"></span>**Gigabit-Ethernet** (117)
</dt> <dt>

<span id="HDLC"></span><span id="hdlc"></span>**HDLC** (118)
</dt> <dt>

<span id="LAP-F"></span><span id="lap-f"></span>**LAP-F** (119)
</dt> <dt>

<span id="V.37"></span><span id="v.37"></span>**V.37** (120)
</dt> <dt>

<span id="X.25_MLP"></span><span id="x.25_mlp"></span>**X.25 MLP** (121)
</dt> <dt>

<span id="X.25_Hunt_Group"></span><span id="x.25_hunt_group"></span><span id="X.25_HUNT_GROUP"></span>**X.25-Suche-Gruppe** (122)
</dt> <dt>

<span id="Transp_HDLC"></span><span id="transp_hdlc"></span><span id="TRANSP_HDLC"></span>**Transp HDLC** (123)
</dt> <dt>

<span id="Interleave_Channel"></span><span id="interleave_channel"></span><span id="INTERLEAVE_CHANNEL"></span>**Interleave Channel** (124)
</dt> <dt>

<span id="FAST_Channel"></span><span id="fast_channel"></span><span id="FAST_CHANNEL"></span>**FAST Channel** (125)
</dt> <dt>

<span id="IP__for_APPN_HPR_in_IP_Networks_"></span><span id="ip__for_appn_hpr_in_ip_networks_"></span><span id="IP__FOR_APPN_HPR_IN_IP_NETWORKS_"></span>**IP (für APPN HPR in IP-Netzwerken)** (126)
</dt> <dt>

<span id="CATV_MAC_Layer"></span><span id="catv_mac_layer"></span><span id="CATV_MAC_LAYER"></span>**CATV MAC Layer** (127)
</dt> <dt>

<span id="CATV_Downstream"></span><span id="catv_downstream"></span><span id="CATV_DOWNSTREAM"></span>**CATV Downstream** (128)
</dt> <dt>

<span id="CATV_Upstream"></span><span id="catv_upstream"></span><span id="CATV_UPSTREAM"></span>**CATV Upstream** (129)
</dt> <dt>

<span id="Avalon_12MPP_Switch"></span><span id="avalon_12mpp_switch"></span><span id="AVALON_12MPP_SWITCH"></span>**Automatischer 12-MPP-Switch** (130)
</dt> <dt>

<span id="Tunnel"></span><span id="tunnel"></span><span id="TUNNEL"></span>**Tunnel** (131)
</dt> <dt>

<span id="Coffee"></span><span id="coffee"></span><span id="COFFEE"></span>**Coffee** (132)
</dt> <dt>

<span id="Circuit_Emulation_Service"></span><span id="circuit_emulation_service"></span><span id="CIRCUIT_EMULATION_SERVICE"></span>**Circuit Emulation Service** (133)
</dt> <dt>

<span id="ATM_SubInterface"></span><span id="atm_subinterface"></span><span id="ATM_SUBINTERFACE"></span>**ATM SubInterface** (134)
</dt> <dt>

<span id="Layer_2_VLAN_using_802.1Q"></span><span id="layer_2_vlan_using_802.1q"></span><span id="LAYER_2_VLAN_USING_802.1Q"></span>**Layer 2-VLAN mit 802.1Q** (135)
</dt> <dt>

<span id="Layer_3_VLAN_using_IP"></span><span id="layer_3_vlan_using_ip"></span><span id="LAYER_3_VLAN_USING_IP"></span>**Layer 3-VLAN mit IP** (136)
</dt> <dt>

<span id="Layer_3_VLAN_using_IPX"></span><span id="layer_3_vlan_using_ipx"></span><span id="LAYER_3_VLAN_USING_IPX"></span>**Layer 3-VLAN mit IPX** (137)
</dt> <dt>

<span id="Digital_Power_Line"></span><span id="digital_power_line"></span><span id="DIGITAL_POWER_LINE"></span>**Digital Power Line** (138)
</dt> <dt>

<span id="Multimedia_Mail_over_IP"></span><span id="multimedia_mail_over_ip"></span><span id="MULTIMEDIA_MAIL_OVER_IP"></span>**Multimedia-E-Mail über IP** (139)
</dt> <dt>

<span id="DTM"></span><span id="dtm"></span>**DG** (140)
</dt> <dt>

<span id="DCN"></span><span id="dcn"></span>**DCN** (141)
</dt> <dt>

<span id="IP_Forwarding"></span><span id="ip_forwarding"></span><span id="IP_FORWARDING"></span>**IP-Weiterleitung** (142)
</dt> <dt>

<span id="MSDSL"></span><span id="msdsl"></span>**MSDSL** (143)
</dt> <dt>

<span id="IEEE_1394"></span><span id="ieee_1394"></span>**IEEE 1394** (144)
</dt> <dt>

<span id="IF-GSN_HIPPI-6400"></span><span id="if-gsn_hippi-6400"></span>**IF-GSN/NAGI-6400** (145)
</dt> <dt>

<span id="DVB-RCC_MAC_Layer"></span><span id="dvb-rcc_mac_layer"></span><span id="DVB-RCC_MAC_LAYER"></span>**RATES-RCC MAC Layer** (146)
</dt> <dt>

<span id="DVB-RCC_Downstream"></span><span id="dvb-rcc_downstream"></span><span id="DVB-RCC_DOWNSTREAM"></span>**RATES-RCC Downstream** (147)
</dt> <dt>

<span id="DVB-RCC_Upstream"></span><span id="dvb-rcc_upstream"></span><span id="DVB-RCC_UPSTREAM"></span>**UPSTREAM-RCC Upstream** (148)
</dt> <dt>

<span id="ATM_Virtual"></span><span id="atm_virtual"></span><span id="ATM_VIRTUAL"></span>**Virtueller Geldautomaten** (149)
</dt> <dt>

<span id="MPLS_Tunnel"></span><span id="mpls_tunnel"></span><span id="MPLS_TUNNEL"></span>**MPLS Tunnel** (150)
</dt> <dt>

<span id="SRP"></span><span id="srp"></span>**SRP** (151)
</dt> <dt>

<span id="Voice_over_ATM"></span><span id="voice_over_atm"></span><span id="VOICE_OVER_ATM"></span>**Voice over ATM** (152)
</dt> <dt>

<span id="Voice_over_Frame_Relay"></span><span id="voice_over_frame_relay"></span><span id="VOICE_OVER_FRAME_RELAY"></span>**Voice over Frame Relay** (153)
</dt> <dt>

<span id="ISDL"></span><span id="isdl"></span>**ISDL** (154)
</dt> <dt>

<span id="Composite_Link"></span><span id="composite_link"></span><span id="COMPOSITE_LINK"></span>**Zusammengesetzter Link** (155)
</dt> <dt>

<span id="SS7_Signaling_Link"></span><span id="ss7_signaling_link"></span><span id="SS7_SIGNALING_LINK"></span>**SS7 Signaling Link** (156)
</dt> <dt>

<span id="Proprietary_P2P_Wireless"></span><span id="proprietary_p2p_wireless"></span><span id="PROPRIETARY_P2P_WIRELESS"></span>**Proprietäres P2P Wireless** (157)
</dt> <dt>

<span id="Frame_Forward"></span><span id="frame_forward"></span><span id="FRAME_FORWARD"></span>**Frame Forward** (158)
</dt> <dt>

<span id="RFC1483_Multiprotocol_over_ATM"></span><span id="rfc1483_multiprotocol_over_atm"></span><span id="RFC1483_MULTIPROTOCOL_OVER_ATM"></span>**RFC1483 Multiprotokoll über ATM** (159)
</dt> <dt>

<span id="USB"></span><span id="usb"></span>**USB** (160)
</dt> <dt>

<span id="IEEE_802.3ad_Link_Aggregate"></span><span id="ieee_802.3ad_link_aggregate"></span><span id="IEEE_802.3AD_LINK_AGGREGATE"></span>**IEEE 802.3ad Link Aggregate** (161)
</dt> <dt>

<span id="BGP_Policy_Accounting"></span><span id="bgp_policy_accounting"></span><span id="BGP_POLICY_ACCOUNTING"></span>**BGP-Richtlinienbuchhaltung** (162)
</dt> <dt>

<span id="FRF_.16_Multilink_FR"></span><span id="frf_.16_multilink_fr"></span><span id="FRF_.16_MULTILINK_FR"></span>**FRF .16 Multilink FR** (163)
</dt> <dt>

<span id="H.323_Gatekeeper"></span><span id="h.323_gatekeeper"></span><span id="H.323_GATEKEEPER"></span>**H.323 Gatekeeper** (164)
</dt> <dt>

<span id="H.323_Proxy"></span><span id="h.323_proxy"></span><span id="H.323_PROXY"></span>**H.323-Proxy** (165)
</dt> <dt>

<span id="MPLS"></span><span id="mpls"></span>**MPLS** (166)
</dt> <dt>

<span id="Multi-Frequency_Signaling_Link"></span><span id="multi-frequency_signaling_link"></span><span id="MULTI-FREQUENCY_SIGNALING_LINK"></span>**Multi-Frequency Signaling Link** (167)
</dt> <dt>

<span id="HDSL-2"></span><span id="hdsl-2"></span>**HDSL-2** (168)
</dt> <dt>

<span id="S-HDSL"></span><span id="s-hdsl"></span>**S-HDSL** (169)
</dt> <dt>

<span id="DS1_Facility_Data_Link"></span><span id="ds1_facility_data_link"></span><span id="DS1_FACILITY_DATA_LINK"></span>**DS1 Facility Data Link** (170)
</dt> <dt>

<span id="Packet_over_SONET_SDH"></span><span id="packet_over_sonet_sdh"></span><span id="PACKET_OVER_SONET_SDH"></span>**Paket über SONET/SDH** (171)
</dt> <dt>

<span id="DVB-ASI_Input"></span><span id="dvb-asi_input"></span><span id="DVB-ASI_INPUT"></span>**EINGANGS-ASI-Eingabe** (172)
</dt> <dt>

<span id="DVB-ASI_Output"></span><span id="dvb-asi_output"></span><span id="DVB-ASI_OUTPUT"></span>**FORMAT-ASI-Ausgabe** (173)
</dt> <dt>

<span id="Power_Line"></span><span id="power_line"></span><span id="POWER_LINE"></span>**Power Line** (174)
</dt> <dt>

<span id="Non_Facility_Associated_Signaling"></span><span id="non_facility_associated_signaling"></span><span id="NON_FACILITY_ASSOCIATED_SIGNALING"></span>**Nicht-Facility Associated Signaling** (175)
</dt> <dt>

<span id="TR008"></span><span id="tr008"></span>**TR008** (176)
</dt> <dt>

<span id="GR303_RDT"></span><span id="gr303_rdt"></span>**GR303 RDT** (177)
</dt> <dt>

<span id="GR303_IDT"></span><span id="gr303_idt"></span>**GR303 IDT** (178)
</dt> <dt>

<span id="ISUP"></span><span id="isup"></span>**ISUP** (179)
</dt> <dt>

<span id="Proprietary_Wireless_MAC_Layer"></span><span id="proprietary_wireless_mac_layer"></span><span id="PROPRIETARY_WIRELESS_MAC_LAYER"></span>**Proprietäre drahtlose MAC-Schicht** (180)
</dt> <dt>

<span id="Proprietary_Wireless_Downstream"></span><span id="proprietary_wireless_downstream"></span><span id="PROPRIETARY_WIRELESS_DOWNSTREAM"></span>**Proprietary Wireless Downstream** (181)
</dt> <dt>

<span id="Proprietary_Wireless_Upstream"></span><span id="proprietary_wireless_upstream"></span><span id="PROPRIETARY_WIRELESS_UPSTREAM"></span>**Proprietäres drahtloses Upstream** (182)
</dt> <dt>

<span id="HIPERLAN_Type_2"></span><span id="hiperlan_type_2"></span><span id="HIPERLAN_TYPE_2"></span>**HIPERLAN-Typ 2** (183)
</dt> <dt>

<span id="Proprietary_Broadband_Wireless_Access_Point_to_Multipoint"></span><span id="proprietary_broadband_wireless_access_point_to_multipoint"></span><span id="PROPRIETARY_BROADBAND_WIRELESS_ACCESS_POINT_TO_MULTIPOINT"></span>**Proprietärer drahtloser Breitbandzugriffspunkt auf Multipoint** (184)
</dt> <dt>

<span id="SONET_Overhead_Channel"></span><span id="sonet_overhead_channel"></span><span id="SONET_OVERHEAD_CHANNEL"></span>**SONET-Overheadkanal** (185)
</dt> <dt>

<span id="Digital_Wrapper_Overhead_Channel"></span><span id="digital_wrapper_overhead_channel"></span><span id="DIGITAL_WRAPPER_OVERHEAD_CHANNEL"></span>**Digital Wrapper Overhead Channel** (186)
</dt> <dt>

<span id="ATM_Adaptation_Layer_2"></span><span id="atm_adaptation_layer_2"></span><span id="ATM_ADAPTATION_LAYER_2"></span>**ATM-Anpassungsebene 2** (187)
</dt> <dt>

<span id="Radio_MAC"></span><span id="radio_mac"></span><span id="RADIO_MAC"></span>**Radio MAC** (188)
</dt> <dt>

<span id="ATM_Radio"></span><span id="atm_radio"></span><span id="ATM_RADIO"></span>**ATM Radio** (189)
</dt> <dt>

<span id="Inter_Machine_Trunk"></span><span id="inter_machine_trunk"></span><span id="INTER_MACHINE_TRUNK"></span>**Inter Machine Trunk** (190)
</dt> <dt>

<span id="MVL_DSL"></span><span id="mvl_dsl"></span>**MVL DSL** (191)
</dt> <dt>

<span id="Long_Read_DSL"></span><span id="long_read_dsl"></span><span id="LONG_READ_DSL"></span>**LANGE LESE-DSL** (192)
</dt> <dt>

<span id="Frame_Relay_DLCI_Endpoint"></span><span id="frame_relay_dlci_endpoint"></span><span id="FRAME_RELAY_DLCI_ENDPOINT"></span>**Frame Relay-DLCI-Endpunkt** (193)
</dt> <dt>

<span id="ATM_VCI_Endpoint"></span><span id="atm_vci_endpoint"></span><span id="ATM_VCI_ENDPOINT"></span>**ATM VCI-Endpunkt** (194)
</dt> <dt>

<span id="Optical_Channel"></span><span id="optical_channel"></span><span id="OPTICAL_CHANNEL"></span>**Optical Channel** (195)
</dt> <dt>

<span id="Optical_Transport"></span><span id="optical_transport"></span><span id="OPTICAL_TRANSPORT"></span>**Optischer Transport** (196)
</dt> <dt>

<span id="Proprietary_ATM"></span><span id="proprietary_atm"></span><span id="PROPRIETARY_ATM"></span>**Proprietäres Geldautomaten** (197)
</dt> <dt>

<span id="Voice_over_Cable"></span><span id="voice_over_cable"></span><span id="VOICE_OVER_CABLE"></span>**Voice over Cable** (198)
</dt> <dt>

<span id="Infiniband"></span><span id="infiniband"></span><span id="INFINIBAND"></span>**Infiniband** (199)
</dt> <dt>

<span id="TE_Link"></span><span id="te_link"></span><span id="TE_LINK"></span>**TE Link** (200)
</dt> <dt>

<span id="Q.2931"></span><span id="q.2931"></span>**Q.2931** (201)
</dt> <dt>

<span id="Virtual_Trunk_Group"></span><span id="virtual_trunk_group"></span><span id="VIRTUAL_TRUNK_GROUP"></span>**Virtual Trunk Group** (202)
</dt> <dt>

<span id="SIP_Trunk_Group"></span><span id="sip_trunk_group"></span><span id="SIP_TRUNK_GROUP"></span>**SIP Trunk Group** (203)
</dt> <dt>

<span id="SIP_Signaling"></span><span id="sip_signaling"></span><span id="SIP_SIGNALING"></span>**SIP-Signalisierung** (204)
</dt> <dt>

<span id="CATV_Upstream_Channel"></span><span id="catv_upstream_channel"></span><span id="CATV_UPSTREAM_CHANNEL"></span>**CATV-Upstreamkanal** (205)
</dt> <dt>

<span id="Econet"></span><span id="econet"></span><span id="ECONET"></span>**Econet** (206)
</dt> <dt>

<span id="FSAN_155Mb_PON"></span><span id="fsan_155mb_pon"></span><span id="FSAN_155MB_PON"></span>**FSAN 155Mb WIES** (207)
</dt> <dt>

<span id="FSAN_622Mb_PON"></span><span id="fsan_622mb_pon"></span><span id="FSAN_622MB_PON"></span>**FSAN 622Mb WIES** (208)
</dt> <dt>

<span id="Transparent_Bridge"></span><span id="transparent_bridge"></span><span id="TRANSPARENT_BRIDGE"></span>**Transparent Bridge** (209)
</dt> <dt>

<span id="Line_Group"></span><span id="line_group"></span><span id="LINE_GROUP"></span>**Zeilengruppe** (210)
</dt> <dt>

<span id="Voice___Feature_Group"></span><span id="voice___feature_group"></span><span id="VOICE___FEATURE_GROUP"></span>**Voice & Feature Group** (211)
</dt> <dt>

<span id="Voice_FGD_EANA"></span><span id="voice_fgd_eana"></span><span id="VOICE_FGD_EANA"></span>**Voice FGD EANA** (212)
</dt> <dt>

<span id="Voice_DID"></span><span id="voice_did"></span><span id="VOICE_DID"></span>**Voice DID** (213)
</dt> <dt>

<span id="MPEG_Transport"></span><span id="mpeg_transport"></span><span id="MPEG_TRANSPORT"></span>**MPEG-Transport** (214)
</dt> <dt>

<span id="6To4"></span><span id="6to4"></span><span id="6TO4"></span>**6To4** (215)
</dt> <dt>

<span id="GTP"></span><span id="gtp"></span>**GTP** (216)
</dt> <dt>

<span id="Paradyne_EtherLoop_1"></span><span id="paradyne_etherloop_1"></span><span id="PARADYNE_ETHERLOOP_1"></span>**Paradsai EtherLoop 1** (217)
</dt> <dt>

<span id="Paradyne_EtherLoop_2"></span><span id="paradyne_etherloop_2"></span><span id="PARADYNE_ETHERLOOP_2"></span>**Paradsai EtherLoop 2** (218)
</dt> <dt>

<span id="Optical_Channel_Group"></span><span id="optical_channel_group"></span><span id="OPTICAL_CHANNEL_GROUP"></span>**Optical Channel Group** (219)
</dt> <dt>

<span id="HomePNA"></span><span id="homepna"></span><span id="HOMEPNA"></span>**HomePNA** (220)
</dt> <dt>

<span id="GFP"></span><span id="gfp"></span>**LP** (221)
</dt> <dt>

<span id="ciscoISLvlan"></span><span id="ciscoislvlan"></span><span id="CISCOISLVLAN"></span>**ciscoISLvlan** (222)
</dt> <dt>

<span id="actelisMetaLOOP"></span><span id="actelismetaloop"></span><span id="ACTELISMETALOOP"></span>**actelisMetaLOOP** (223)
</dt> <dt>

<span id="Fcip"></span><span id="fcip"></span><span id="FCIP"></span>**Fcip** (224)
</dt> <dt>

<span id="IANA_Reserved"></span><span id="iana_reserved"></span><span id="IANA_RESERVED"></span>**IANA Reserved** (225..4095)
</dt> <dt>

<span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>**IPv4** (4096)
</dt> <dt>

<span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>**IPv6** (4097)
</dt> <dt>

<span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>**IPv4/v6** (4098)
</dt> <dt>

<span id="IPX"></span><span id="ipx"></span>**IPX** (4099)
</dt> <dt>

<span id="DECnet"></span><span id="decnet"></span><span id="DECNET"></span>**DECnet** (4100)
</dt> <dt>

<span id="SNA"></span><span id="sna"></span>**SNA** (4101)
</dt> <dt>

<span id="CONP"></span><span id="conp"></span>**CONP** (4102)
</dt> <dt>

<span id="CLNP"></span><span id="clnp"></span>**CLNP** (4103)
</dt> <dt>

<span id="VINES"></span><span id="vines"></span>**VINES** (4104)
</dt> <dt>

<span id="XNS"></span><span id="xns"></span>**XNS** (4105)
</dt> <dt>

<span id="ISDN_B_Channel_Endpoint"></span><span id="isdn_b_channel_endpoint"></span><span id="ISDN_B_CHANNEL_ENDPOINT"></span>**ISDN B-Kanalendpunkt** (4106)
</dt> <dt>

<span id="ISDN_D_Channel_Endpoint"></span><span id="isdn_d_channel_endpoint"></span><span id="ISDN_D_CHANNEL_ENDPOINT"></span>**ISDN D-Kanalendpunkt** (4107)
</dt> <dt>

<span id="BGP"></span><span id="bgp"></span>**BGP** (4108)
</dt> <dt>

<span id="OSPF"></span><span id="ospf"></span>**OSPF** (4109)
</dt> <dt>

<span id="UDP"></span><span id="udp"></span>**UDP** (4110)
</dt> <dt>

<span id="TCP"></span><span id="tcp"></span>**TCP** (4111)
</dt> <dt>

<span id="802.11a"></span><span id="802.11A"></span>**802.11a** (4112)
</dt> <dt>

<span id="802.11b"></span><span id="802.11B"></span>**802.11b** (4113)
</dt> <dt>

<span id="802.11g"></span><span id="802.11G"></span>**802,11 g** (4114)
</dt> <dt>

<span id="802.11h"></span><span id="802.11H"></span>**802.11h** (4115)
</dt> <dt>

<span id="NFS"></span><span id="nfs"></span>**NFS** (4200)
</dt> <dt>

<span id="CIFS"></span><span id="cifs"></span>**CIFS** (4201)
</dt> <dt>

<span id="DAFS"></span><span id="dafs"></span>**DAFS** (4202)
</dt> <dt>

<span id="WebDAV"></span><span id="webdav"></span><span id="WEBDAV"></span>**WebDAV** (4203)
</dt> <dt>

<span id="HTTP"></span><span id="http"></span>**HTTP** (4204)
</dt> <dt>

<span id="FTP"></span><span id="ftp"></span>**FTP** (4205)
</dt> <dt>

<span id="NDMP"></span><span id="ndmp"></span>**NDMP** (4300)
</dt> <dt>

<span id="Telnet"></span><span id="telnet"></span><span id="TELNET"></span>**Telnet** (4400)
</dt> <dt>

<span id="SSH"></span><span id="ssh"></span>**SSH** (4401)
</dt> <dt>

<span id="SM_CLP"></span><span id="sm_clp"></span>**SM CLP** (4402)
</dt> <dt>

<span id="SMTP"></span><span id="smtp"></span>**SMTP** (4403)
</dt> <dt>

<span id="LDAP"></span><span id="ldap"></span>**LDAP** (4404)
</dt> <dt>

<span id="RDP"></span><span id="rdp"></span>**RDP** (4405)
</dt> <dt>

<span id="HTTPS"></span><span id="https"></span>**HTTPS** (4406)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Anbieter reserviert** (32768.. )
</dt> </dl>

</dd> <dt>

**Protocoltype**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft ist veraltet statt der **ProtocolIFType-Eigenschaft.** Diese Eigenschaft wird von [**CIM \_ ProtocolEndpoint geerbt.**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint)

</dd> <dt>

**RequestedState**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der zuletzt angeforderte oder gewünschte Zustand für den Verwaltungsdienst. Diese Eigenschaft wird von [**CIM \_ EnabledLogicalElement geerbt**](/previous-versions//cc136818(v=vs.85))und immer auf 12 (Nicht zutreffend) festgelegt.



| Wert                                                                         | Bedeutung                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>12</dt> </dl> | Nicht zutreffend<br/> |



 

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Beschreibt den Status des Elements. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

"OK"

"Error" (Fehler)

"Heruntergestuft"

"Unbekannt"

"Pred Fail"

"Wird gestartet"

"Wird beendet"

"Dienst"

"Striche"

"NonRecover"

"Kein Kontakt"

"Lost Comm"

</dd> <dt>

**StatusDescriptions**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Zeichenfolgen, die die verschiedenen **OperationalStatus-Arraywerte** beschreiben. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement geerbt.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name der Erstellungsklasse des Hostsystems. Diese Eigenschaft wird von [**CIM \_ ServiceAccessPoint geerbt.**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)

</dd> <dt>

**Systemname**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Key**, **MaxLen** ( 256 )
</dt> </dl>

Der Name des Hostsystems. Diese Eigenschaft wird von [**CIM \_ ServiceAccessPoint geerbt.**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)

</dd> <dt>

**TimeOfLastStateChange**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Datum und die Uhrzeit der letzten Änderung des aktivierten Zustands des Elements. Diese Eigenschaft wird von [**CIM \_ EnabledLogicalElement geerbt,**](/previous-versions//cc136818(v=vs.85))wird jedoch nicht unterstützt.

</dd> <dt>

**TransitioningToState**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den Zielzustand an, in den die Instanz übergibt. Diese Eigenschaft wird von [**CIM \_ EnabledLogicalElement geerbt,**](/previous-versions//cc136818(v=vs.85))aber nicht verwendet.

</dd> <dt>

**WWNN**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der name des weltweiten Knotens des Fibre Channel, mit dem dieser Endpunkt verbunden ist.

</dd> <dt>

**WWPN**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der name des weltweiten Ports des Fibre Channel, mit dem dieser Endpunkt verbunden ist.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

