---
description: Stellt die Konfiguration eines virtuellen Fibre Channel Schalters dar.
ms.assetid: da2918a9-6e7f-4fee-9c13-7e75bbc6821f
title: Msvm_VirtualFcSwitchSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualFcSwitchSettingData
- Msvm_VirtualFcSwitchSettingData.InstanceID
- Msvm_VirtualFcSwitchSettingData.Caption
- Msvm_VirtualFcSwitchSettingData.Description
- Msvm_VirtualFcSwitchSettingData.ElementName
- Msvm_VirtualFcSwitchSettingData.VirtualSystemIdentifier
- Msvm_VirtualFcSwitchSettingData.VirtualSystemType
- Msvm_VirtualFcSwitchSettingData.Notes
- Msvm_VirtualFcSwitchSettingData.CreationTime
- Msvm_VirtualFcSwitchSettingData.ConfigurationID
- Msvm_VirtualFcSwitchSettingData.ConfigurationDataRoot
- Msvm_VirtualFcSwitchSettingData.ConfigurationFile
- Msvm_VirtualFcSwitchSettingData.SnapshotDataRoot
- Msvm_VirtualFcSwitchSettingData.SuspendDataRoot
- Msvm_VirtualFcSwitchSettingData.SwapFileDataRoot
- Msvm_VirtualFcSwitchSettingData.LogDataRoot
- Msvm_VirtualFcSwitchSettingData.AutomaticStartupAction
- Msvm_VirtualFcSwitchSettingData.AutomaticStartupActionDelay
- Msvm_VirtualFcSwitchSettingData.AutomaticStartupActionSequenceNumber
- Msvm_VirtualFcSwitchSettingData.AutomaticShutdownAction
- Msvm_VirtualFcSwitchSettingData.AutomaticRecoveryAction
- Msvm_VirtualFcSwitchSettingData.RecoveryFile
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 67b6008ba1f5ba9849d6fcd9127c1a55c1da8290
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525217"
---
# <a name="msvm_virtualfcswitchsettingdata-class"></a>MSVM \_ virtualfcswitchsettingdata-Klasse

Stellt die Konfiguration eines virtuellen Fibre Channel Schalters dar.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualFcSwitchSettingData : CIM_VirtualSystemSettingData
{
  string   InstanceID;
  string   Caption;
  string   Description;
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
};
```

## <a name="members"></a>Member

Die **MSVM \_ virtualfcswitchsettingdata** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ virtualfcswitchsettingdata** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Automatikrecoveryaction**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die für den virtuellen Computer auszuführende Aktion, wenn die von der virtuellen Maschine ausgeführte Software ausfällt. Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt, wird jedoch nicht verwendet.

</dd> <dt>

**Automaticshutdownaction**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Aktion, die beim Herunterfahren des Hosts für die virtuelle Maschine ausgeführt werden soll. Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt, wird jedoch nicht verwendet.

</dd> <dt>

**Automaticstartupaction**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Aktion, die für den virtuellen Computer ausgeführt werden soll, wenn der Host gestartet wird. Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt, wird jedoch nicht verwendet.

</dd> <dt>

**Automaticstartupactiondelay**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Verzögerungszeit, bevor der virtuelle Computer automatisch gestartet wird. Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt, wird jedoch nicht verwendet.

</dd> <dt>

**Automaticstartupactionsequencenumschlag**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zahl, die die relative Sequenz der Aktivierung virtueller Maschinen angibt, wenn das Host System gestartet wird. Eine niedrigere Zahl deutet auf eine frühere Aktivierung hin. Wenn eine oder mehrere Konfigurationen denselben Wert aufweisen, ist die Sequenz implementierungsabhängig. Der Wert 0 gibt an, dass die Sequenz implementierungsabhängig ist. Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt, wird jedoch nicht verwendet.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine kurze Beschreibung des-Objekts. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**Configurationdataroot**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Pfad eines Verzeichnisses, in dem Informationen zur Konfiguration der virtuellen Maschine gespeichert werden. Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.

</dd> <dt>

**ConfigurationFile**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der relative Pfad und der Dateiname einer Datei, in der Informationen zur Konfiguration der virtuellen Maschine gespeichert werden. Dieser Pfad ist relativ zur **configurationdataroot** -Eigenschaft. Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.

</dd> <dt>

**ConfigurationID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der eindeutige Bezeichner der Konfiguration. Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.

</dd> <dt>

**CreationTime**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Datum und die Uhrzeit der Erstellung der Einstellungen. Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.

Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Anzeige Name für das-Objekt. Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Identifiziert eine Instanz dieser Klasse eindeutig. Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))geerbt.

</dd> <dt>

**Logdataroot**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Pfad eines Verzeichnisses, in dem Protokollinformationen für den virtuellen Computer gespeichert werden. Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt, wird jedoch nicht verwendet.

</dd> <dt>

**Hinweise**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Vom Benutzer bereitgestellte Hinweise zum virtuellen Computer. Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.

</dd> <dt>

**Wiederherstellbare Datei**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der vollständige Pfad einer Datei, in der Wiederherstellungs bezogene Informationen für den virtuellen Computer gespeichert werden. Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt, wird jedoch nicht verwendet.

</dd> <dt>

**Snapshotdataroot**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Pfad eines Verzeichnisses, in dem Informationen zu den Momentaufnahmen der virtuellen Maschine gespeichert werden. Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.

</dd> <dt>

**Suspenddataroot**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Pfad eines Verzeichnisses, in dem Informationen zu den Informationen zum Aussetzen der virtuellen Maschine gespeichert werden. Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.

</dd> <dt>

**Austauschen von Daten**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Pfad eines Verzeichnisses, in dem die Auslagerungs Dateien für den virtuellen Computer gespeichert werden. Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt, wird jedoch nicht verwendet.

</dd> <dt>

**Virtualsystemidentifier**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) -Objekts, zu dem diese Einstellungsdaten gehören. Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.

</dd> <dt>

**Virtualsystemtype**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den Typ der virtuellen Maschine an, die die Einstellungsdaten darstellen. Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))geerbt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

