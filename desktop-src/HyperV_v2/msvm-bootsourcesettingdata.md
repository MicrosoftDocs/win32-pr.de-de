---
description: Stellt die Parameter zum Festlegen der Startquelle eines virtuellen Computers dar.
ms.assetid: 21CD4B71-3D05-469E-89BB-DC2C65F5AB10
title: Msvm_BootSourceSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BootSourceSettingData
- Msvm_BootSourceSettingData.Description
- Msvm_BootSourceSettingData.Caption
- Msvm_BootSourceSettingData.InstanceID
- Msvm_BootSourceSettingData.ElementName
- Msvm_BootSourceSettingData.BootSourceType
- Msvm_BootSourceSettingData.OtherLocation
- Msvm_BootSourceSettingData.FirmwareDevicePath
- Msvm_BootSourceSettingData.BootSourceDescription
- Msvm_BootSourceSettingData.OptionalData
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d7319c8df8c8f9b98ae39ed94f620445d4cc80b32f2c7b45189ce636c1c020dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117995037"
---
# <a name="msvm_bootsourcesettingdata-class"></a>Msvm \_ BootSourceSettingData-Klasse

Stellt die Parameter zum Festlegen der Startquelle eines virtuellen Computers dar. Diese Klasse wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))abgeleitet.

Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BootSourceSettingData : CIM_SettingData
{
  string Description;
  string Caption;
  string InstanceID;
  string ElementName;
  uint32 BootSourceType;
  string OtherLocation;
  string FirmwareDevicePath;
  string BootSourceDescription;
  uint8  OptionalData[];
};
```

## <a name="members"></a>Member

Die **Msvm \_ BootSourceSettingData-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ BootSourceSettingData-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**BootSourceDescription**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Beschreibung der von der Firmware bereitgestellten Startquelle.

</dd> <dt>

**BootSourceType**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein -Enumerationswert, der den Typ der Startquelle angibt.

Dies sind gültige Werte:

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Drive"></span><span id="drive"></span><span id="DRIVE"></span>

**Laufwerk** (1)


</dt> <dd></dd> <dt>

<span id="Network"></span><span id="network"></span><span id="NETWORK"></span>

**Netzwerk** (2)


</dt> <dd></dd> <dt>

<span id="File"></span><span id="file"></span><span id="FILE"></span>

**Datei** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **MaxLen** ( 64 )
</dt> </dl>

Eine kurze Textbeschreibung des Objekts.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Textbeschreibung des Objekts.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Anzeigename für diese Instanz von SettingData. Darüber hinaus kann der Anzeigename als Indexeigenschaft für eine Suche oder Abfrage verwendet werden. (Hinweis: Der Name muss innerhalb eines Namespace nicht eindeutig sein.)

</dd> <dt>

**FirmwareDevicePath**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der native Pfad, den die Firmware zum Beschreiben des Geräts verwendet.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Innerhalb des Bereichs des instanziierenden Namespace identifiziert InstanceID eine Instanz dieser Klasse nicht transparent und eindeutig. Um die Eindeutigkeit innerhalb des NameSpace zu gewährleisten, sollte der Wert von InstanceID mit dem folgenden "bevorzugten" Algorithmus erstellt werden: *OrgID: LocalID.**Dabei* werden *OrgID* und *LocalID* durch einen Doppelpunkt getrennt (:), und *orgID* muss einen urheberrechtlich geschützten, geschützten oder anderweitig eindeutigen Namen enthalten, der sich im Besitz der Geschäftsentität befindet, die die Instanz-ID erstellt oder definiert oder eine registrierte ID ist, die der Geschäftseinheit von einer anerkannten globalen Autorität zugewiesen wird. (Diese Anforderung ähnelt *schemaname.* \_ *ClassName-Struktur* von Schemaklassennamen.) Darüber hinaus darf *OrgID* keinen Doppelpunkt (:) enthalten, um eindeutig zu sein. Wenn Sie diesen Algorithmus verwenden, muss der erste Doppelpunkt, der in InstanceID angezeigt wird, zwischen *OrgID* und *LocalID* angezeigt werden. *LocalID* wird von der Geschäftsentität ausgewählt und sollte nicht wiederverwendet werden, um verschiedene zugrunde liegende (reale) Elemente zu identifizieren. Wenn der oben bevorzugte Algorithmus nicht verwendet wird, muss die definierende Entität sicherstellen, dass die resultierende Instanz-ID nicht für alle InstanceIDs wiederverwendet wird, die von diesem oder anderen Anbietern für den NameSpace dieser Instanz erstellt wurden. Für DMTF-definierte Instanzen muss der "bevorzugte" Algorithmus verwendet werden, wobei die *OrgID* auf CIM festgelegt ist.

</dd> <dt>

**OptionalData**
</dt> <dd> <dl> <dt>

Datentyp: **uint8-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **OctetString**, [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Optionale Daten, die von der Firmware bereitgestellt werden.

> [!Note]  
> In Windows 10 hinzugefügte Eigenschaft.

 

</dd> <dt>

**OtherLocation**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die anderen Standortinformationen, sofern vorhanden, die von der Firmware verwendet werden, um die Startquelle weiter eindeutig zu identifizieren.

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

[**CIM \_ SettingData**](cim-settingdata.md)
</dt> <dt>

[**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))
</dt> </dl>

 

