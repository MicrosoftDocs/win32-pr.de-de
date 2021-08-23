---
description: Stellt die aktuelle Konfiguration eines virtuellen Ethernet-Switches dar.
ms.assetid: a7c03517-332d-47ce-8e04-c2187bcb2977
title: Msvm_VirtualEthernetSwitchSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchSettingData
- Msvm_VirtualEthernetSwitchSettingData.InstanceID
- Msvm_VirtualEthernetSwitchSettingData.Caption
- Msvm_VirtualEthernetSwitchSettingData.Description
- Msvm_VirtualEthernetSwitchSettingData.ElementName
- Msvm_VirtualEthernetSwitchSettingData.VirtualSystemIdentifier
- Msvm_VirtualEthernetSwitchSettingData.VirtualSystemType
- Msvm_VirtualEthernetSwitchSettingData.Notes
- Msvm_VirtualEthernetSwitchSettingData.CreationTime
- Msvm_VirtualEthernetSwitchSettingData.ConfigurationID
- Msvm_VirtualEthernetSwitchSettingData.ConfigurationDataRoot
- Msvm_VirtualEthernetSwitchSettingData.ConfigurationFile
- Msvm_VirtualEthernetSwitchSettingData.SnapshotDataRoot
- Msvm_VirtualEthernetSwitchSettingData.SuspendDataRoot
- Msvm_VirtualEthernetSwitchSettingData.SwapFileDataRoot
- Msvm_VirtualEthernetSwitchSettingData.LogDataRoot
- Msvm_VirtualEthernetSwitchSettingData.AutomaticStartupAction
- Msvm_VirtualEthernetSwitchSettingData.AutomaticStartupActionDelay
- Msvm_VirtualEthernetSwitchSettingData.AutomaticStartupActionSequenceNumber
- Msvm_VirtualEthernetSwitchSettingData.AutomaticShutdownAction
- Msvm_VirtualEthernetSwitchSettingData.AutomaticRecoveryAction
- Msvm_VirtualEthernetSwitchSettingData.RecoveryFile
- Msvm_VirtualEthernetSwitchSettingData.VLANConnection
- Msvm_VirtualEthernetSwitchSettingData.AssociatedResourcePool
- Msvm_VirtualEthernetSwitchSettingData.MaxNumMACAddress
- Msvm_VirtualEthernetSwitchSettingData.IOVPreferred
- Msvm_VirtualEthernetSwitchSettingData.ExtensionOrder
- Msvm_VirtualEthernetSwitchSettingData.BandwidthReservationMode
- Msvm_VirtualEthernetSwitchSettingData.TeamingEnabled
- Msvm_VirtualEthernetSwitchSettingData.PacketDirectEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bbd8cd77a96301187e9b5c9f8544a23b616bf9db78af6560296660b0a3995bed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681240"
---
# <a name="msvm_virtualethernetswitchsettingdata-class"></a>Msvm \_ VirtualEthernetSwitchSettingData-Klasse

Stellt die aktuelle Konfiguration eines virtuellen Ethernet-Switches dar.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualEthernetSwitchSettingData : CIM_VirtualEthernetSwitchSettingData
{
  string   InstanceID = "Microsoft:GUID\DeviceSpecificData";
  string   Caption = "Virtual Ethernet Switch Settings";
  string   Description = "Active settings for the virtual Ethernet switch";
  string   ElementName;
  string   VirtualSystemIdentifier;
  string   VirtualSystemType;
  string   Notes[];
  datetime CreationTime;
  string   ConfigurationID;
  string   ConfigurationDataRoot;
  string   ConfigurationFile;
  string   SnapshotDataRoot;
  string   SuspendDataRoot;
  string   SwapFileDataRoot;
  string   LogDataRoot;
  uint16   AutomaticStartupAction;
  datetime AutomaticStartupActionDelay;
  uint16   AutomaticStartupActionSequenceNumber;
  uint16   AutomaticShutdownAction;
  uint16   AutomaticRecoveryAction;
  string   RecoveryFile;
  string   VLANConnection[];
  string   AssociatedResourcePool[];
  uint32   MaxNumMACAddress;
  boolean  IOVPreferred = FALSE;
  string   ExtensionOrder[];
  uint32   BandwidthReservationMode = 0;
  boolean  TeamingEnabled = FALSE;
  boolean  PacketDirectEnabled = FALSE;
};
```

## <a name="members"></a>Member

Die **Msvm \_ VirtualEthernetSwitchSettingData-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ VirtualEthernetSwitchSettingData-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**AssociatedResourcePool**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Liste der Hostressourcenpools, die zugeordnet werden sollen oder die derzeit dem Ethernet-Switch zugeordnet sind, um Ethernetverbindungen zwischen einem virtuellen Computer und einem Ethernet-Switch zu erstellen. Jeder Wert muss dem WBEM-Produktions-URI \_ \_ UntypedInstancePath entsprechen, wie in DSP0207 definiert. Diese Eigenschaft wird von **CIM \_ VirtualEthernetSwitchSettingData geerbt.**

</dd> <dt>

**AutomaticRecoveryAction**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Aktion, die für den virtuellen Computer ausgeführt werden soll, wenn die vom virtuellen Computer ausgeführte Software ausfällt. Fehler sind in diesem Fall ein Fehler, der von der Hostplattform erkannt werden kann, z. B. eine nicht unterbrechbare Wartezustandsbedingung. Diese Eigenschaft wird von [**CIM \_ VirtualSystemSettingData geerbt**](/previous-versions//cc136954(v=vs.85))und nicht verwendet.

</dd> <dt>

**AutomaticShutdownAction**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Aktion, die für den virtuellen Computer ausgeführt werden soll, wenn der Host heruntergefahren wird. Diese Eigenschaft wird von [**CIM \_ VirtualSystemSettingData geerbt**](/previous-versions//cc136954(v=vs.85))und nicht verwendet.

</dd> <dt>

**AutomaticStartupAction**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Aktion, die für den virtuellen Computer ausgeführt werden soll, wenn der Host gestartet wird. Diese Eigenschaft wird von [**CIM \_ VirtualSystemSettingData geerbt**](/previous-versions//cc136954(v=vs.85))und nicht verwendet.

</dd> <dt>

**AutomaticStartupActionDelay**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Verzögerung bis zum automatischen Start des virtuellen Computers. Diese Eigenschaft wird von [**CIM \_ VirtualSystemSettingData geerbt**](/previous-versions//cc136954(v=vs.85))und nicht verwendet.

</dd> <dt>

**AutomaticStartupActionSequenceNumber**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zahl, die die relative Sequenz der Aktivierung virtueller Computer angibt, wenn das Hostsystem gestartet wird. Eine niedrigere Zahl gibt eine frühere Aktivierung an. Diese Eigenschaft wird von [**CIM \_ VirtualSystemSettingData geerbt**](/previous-versions//cc136954(v=vs.85))und nicht verwendet.

</dd> <dt>

**BandwidthReservationMode**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Der Bandbreitenreservierungsmodus.

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

**Standard** (0)


</dt> <dd></dd> <dt>

<span id="Weight"></span><span id="weight"></span><span id="WEIGHT"></span>

**Gewichtung** (1)


</dt> <dd></dd> <dt>

<span id="Absolute"></span><span id="absolute"></span><span id="ABSOLUTE"></span>

**Absolut** (2)


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Keine** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine kurze Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedElement geerbt**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)und immer auf "Virtual Ethernet Switch Einstellungen" festgelegt.

</dd> <dt>

**ConfigurationDataRoot**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Pfad eines Verzeichnisses, in dem Informationen zur Konfiguration des virtuellen Computers gespeichert werden. Diese Eigenschaft wird von [**CIM \_ VirtualSystemSettingData geerbt**](/previous-versions//cc136954(v=vs.85))und nicht verwendet.

</dd> <dt>

**ConfigurationFile**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der relative Pfad und Dateiname einer Datei, in der Informationen zur Konfiguration des virtuellen Computers gespeichert werden. Dieser Pfad ist relativ zur **ConfigurationDataRoot-Eigenschaft.** Diese Eigenschaft wird von [**CIM \_ VirtualSystemSettingData geerbt**](/previous-versions//cc136954(v=vs.85))und nicht verwendet.

</dd> <dt>

**ConfigurationID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der eindeutige Bezeichner der Konfiguration des virtuellen Computers. Diese Eigenschaft wird von [**CIM \_ VirtualSystemSettingData geerbt**](/previous-versions//cc136954(v=vs.85))und nicht verwendet.

</dd> <dt>

**Creationtime**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Datum und die Uhrzeit der Erstellung der Einstellungen. Diese Eigenschaft wird von [**CIM \_ VirtualSystemSettingData geerbt.**](/previous-versions//cc136954(v=vs.85))

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedElement geerbt**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)und immer auf "Aktive Einstellungen für den virtuellen Ethernet-Switch" festgelegt.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Anzeigename für das Objekt. Diese Eigenschaft wird von [**CIM \_ VirtualSystemSettingData geerbt.**](/previous-versions//cc136954(v=vs.85))

</dd> <dt>

**ExtensionOrder**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Ein Array eingebetteter Instanzen der [**Msvm \_ EthernetSwitchExtension-Klasse,**](msvm-ethernetswitchextension.md) die die an diesen Switch gebundenen Switcherweiterungen in der Reihenfolge darstellen, in der sie angewendet werden.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Identifiziert eine Instanz dieser Klasse eindeutig. Diese Eigenschaft wird von [**CIM \_ SettingData geerbt**](/previous-versions//cc136911(v=vs.85)) und immer auf "Microsoft:*GUID* \\ *DeviceSpecificData"* festgelegt.

</dd> <dt>

**IOVPreferred**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob die E/A-Virtualisierung mit einem Stamm (SINGLE Root IO Virtualization, SR-IOV) auf dem zugrunde liegenden Adapter bevorzugt wird, sofern verfügbar.

</dd> <dt>

**LogDataRoot**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Pfad eines Verzeichnisses, in dem Protokollinformationen für den virtuellen Computer gespeichert werden. Diese Eigenschaft wird von [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))geerbt und nicht verwendet.

</dd> <dt>

**MaxNumMACAddress**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die maximale Anzahl eindeutiger MAC-Adressen an, die durch den Schalter zur Unterstützung von MAC-Adress-Learning erlernt werden können, wie im IEEE 802.1-Standard definiert. Diese Eigenschaft wird von **CIM \_ VirtualEthernetSwitchSettingData** geerbt.

</dd> <dt>

**Notizen**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Vom Benutzer bereitgestellte Hinweise, die sich auf den virtuellen Computer beziehen. Diese Eigenschaft wird von [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))geerbt.

</dd> <dt>

**PacketDirectEnabled**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob PacketDirect verwendet werden soll, falls verfügbar. Der Standardwert ist **false**.

> [!Note]  
> Diese Eigenschaft wurde in Windows 10 und Windows Server 2016 hinzugefügt.

 

</dd> <dt>

**RecoveryFile**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der vollständige Pfad einer Datei, in der wiederherstellungsbezogene Informationen für den virtuellen Computer gespeichert werden. Diese Eigenschaft wird von [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))geerbt und nicht verwendet.

</dd> <dt>

**SnapshotDataRoot**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Pfad eines Verzeichnisses, in dem Informationen zu den Momentaufnahmen des virtuellen Computers gespeichert werden. Diese Eigenschaft wird von [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))geerbt und nicht verwendet.

</dd> <dt>

**SuspendDataRoot**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Pfad eines Verzeichnisses, in dem Informationen zu den Informationen zum virtuellen Computer gespeichert werden, die sich auf das Anhalten beziehen. Diese Eigenschaft wird von [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))geerbt und nicht verwendet.

</dd> <dt>

**SwapFileDataRoot**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Pfad eines Verzeichnisses, in dem Auslagerungsdateien für den virtuellen Computer gespeichert werden. Diese Eigenschaft wird von [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))geerbt und nicht verwendet.

</dd> <dt>

**TeamingEnabled**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob NIC-Teaming verwendet werden soll. Der Standardwert ist **false**.

> [!Note]  
> Diese Eigenschaft wurde inWindows 10 und Windows Server 2016 hinzugefügt.

 

</dd> <dt>

**VirtualSystemIdentifier**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des [**CIM \_ ComputerSystem-Objekts,**](/windows/desktop/CIMWin32Prov/cim-computersystem) zu dem diese Einstellungsdaten gehören. Diese Eigenschaft ist eine Außerkraftsetzung von [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).

</dd> <dt>

**VirtualSystemType**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den Typ des virtuellen Computers an, den die Einstellungsdaten darstellen. Diese Eigenschaft wird von [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))geerbt.

</dd> <dt>

**VLANConnection**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Liste der VLAN-Bezeichner, auf die dieser Switch zugreifen kann. Diese Eigenschaft wird von **CIM \_ VirtualEthernetSwitchSettingData** geerbt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

