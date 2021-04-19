---
description: Stellt eine Instanz einer Erweiterungs Komponente dar, die auf einem Host System installiert ist.
ms.assetid: ad24fb08-36af-42a8-a910-63eae54fa5b8
title: Msvm_InstalledEthernetSwitchExtension-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_InstalledEthernetSwitchExtension
- Msvm_InstalledEthernetSwitchExtension.InstanceID
- Msvm_InstalledEthernetSwitchExtension.Caption
- Msvm_InstalledEthernetSwitchExtension.Description
- Msvm_InstalledEthernetSwitchExtension.ElementName
- Msvm_InstalledEthernetSwitchExtension.InstallDate
- Msvm_InstalledEthernetSwitchExtension.Name
- Msvm_InstalledEthernetSwitchExtension.OperationalStatus
- Msvm_InstalledEthernetSwitchExtension.StatusDescriptions
- Msvm_InstalledEthernetSwitchExtension.Status
- Msvm_InstalledEthernetSwitchExtension.HealthState
- Msvm_InstalledEthernetSwitchExtension.CommunicationStatus
- Msvm_InstalledEthernetSwitchExtension.DetailedStatus
- Msvm_InstalledEthernetSwitchExtension.OperatingStatus
- Msvm_InstalledEthernetSwitchExtension.PrimaryStatus
- Msvm_InstalledEthernetSwitchExtension.ExtensionType
- Msvm_InstalledEthernetSwitchExtension.Vendor
- Msvm_InstalledEthernetSwitchExtension.Version
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bfbe0b1996751613c31913447cb0d200d71b8168
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346981"
---
# <a name="msvm_installedethernetswitchextension-class"></a>MSVM \_ installedethernetzwitchextension-Klasse

Stellt eine Instanz einer Erweiterungs Komponente dar, die auf einem Host System installiert ist.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_InstalledEthernetSwitchExtension : CIM_ManagedSystemElement
{
  string   InstanceID;
  string   Caption = " System Virtual Ethernet Switch Extension";
  string   Description = "Microsoft NDIS Packet Capture Filter Driver";
  string   ElementName = "Microsoft NDIS Capture";
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = "OK";
  string   Status = "OK";
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint8    ExtensionType;
  string   Vendor;
  string   Version;
};
```

## <a name="members"></a>Member

Die **MSVM \_ installedethernetzwitchextension** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ installedethernetzwitchextension** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **maxlen** (64)
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

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Anzeige Name für das-Objekt. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**ExtensionType**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den Typ der Erweiterungs Komponente an.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Capture"></span><span id="capture"></span><span id="CAPTURE"></span>

**Erfassung** (1)


</dt> <dd></dd> <dt>

<span id="Filter"></span><span id="filter"></span><span id="FILTER"></span>

**Filter** (2)


</dt> <dd></dd> <dt>

<span id="Forwarding"></span><span id="forwarding"></span><span id="FORWARDING"></span>

**Weiterleitung** (3)


</dt> <dd></dd> <dt>

<span id="Monitoring"></span><span id="monitoring"></span><span id="MONITORING"></span>

**Überwachung** (4)


</dt> <dd></dd> <dt>

<span id="Native"></span><span id="native"></span><span id="NATIVE"></span>

**Native** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der aktuelle Zustand des Elements. Dieses Attribut drückt den Zustand dieses Elements aus, aber nicht notwendigerweise dessen unter Komponenten. Mögliche Werte sind 0 bis 30, wobei 5 bedeutet, dass das Element vollständig fehlerfrei ist und 30 bedeutet, dass das Element vollständig nicht funktionsfähig ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt und ist immer auf 5 (OK) festgelegt.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Datum und die Uhrzeit der Installation des-Objekts. Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

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

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Die Bezeichnung, mit der das-Objekt bekannt ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

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

Die aktuellen Status des-Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, und jedes Array Element ist immer auf 2 (OK) festgelegt.

</dd> <dt>

**Primarystatus**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Stellt Statusinformationen auf hoher Ebene bereit. Diese Eigenschaft sollte in Verbindung mit der **detailedstatus** -Eigenschaft verwendet werden, um allgemeine und ausführliche Integritäts Statusinformationen für das-Element und seine unter Komponenten bereitzustellen. Ein **null** -Wert gibt an, dass diese Eigenschaft nicht implementiert ist. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der aktuelle Status des Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

<dl> <dt>

Okay
</dt> <dt>

<span id="OK"></span><span id="ok"></span>**Okay**
</dt> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Zeit**
</dt> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Zerstört**
</dt> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannter**
</dt> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>**Pred-Fehler**
</dt> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Fahren**
</dt> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Hindern**
</dt> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Leistungs**
</dt> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Gestresst**
</dt> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>**Nicht wiederherstellen**
</dt> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Kein Kontakt**
</dt> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>**Verlorene Kommunikations-**
</dt> </dl>

</dd> <dt>

**Status Beschreibungen**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Zeichen folgen, die die verschiedenen **OperationalStatus** -Array Werte beschreiben. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, und jedes Array Element ist immer auf "OK" festgelegt.

</dd> <dt>

**Hersteller**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den Anbieter an, der die Erweiterung bereitstellt.

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Version der Erweiterung im Format "Major. Minor", z. b. "2,0".

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

