---
description: Stellt die Parameter zum Festlegen der Start Quelle eines virtuellen Computers dar.
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
ms.openlocfilehash: 0403846e10df4c9bd54146eea44e8e91c06d01c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348822"
---
# <a name="msvm_bootsourcesettingdata-class"></a>MSVM \_ bootsourcesettingdata-Klasse

Stellt die Parameter zum Festlegen der Start Quelle eines virtuellen Computers dar. Diese Klasse wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))abgeleitet.

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

Die **MSVM \_ bootsourcesettingdata** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ bootsourcesettingdata** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Bootsourcedescription**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Beschreibung der von der Firmware bereitgestellten Start Quelle.

</dd> <dt>

**Bootsourcetype**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein-Enumerationswert, der den Typ der Start Quelle angibt.

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

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **maxlen** (64)
</dt> </dl>

Eine kurze Textbeschreibung des-Objekts.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Textbeschreibung des-Objekts.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Anzeige Name für diese Instanz von SettingData. Außerdem kann der Anzeige Name als Index Eigenschaft für eine Suche oder Abfrage verwendet werden. (Hinweis: der Name muss innerhalb eines Namespace nicht eindeutig sein.)

</dd> <dt>

**Firmwaredevicepath**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Native Pfad, den die Firmware verwendet, um das Gerät zu beschreiben.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Im Gültigkeitsbereich des instanziierten Namespaces identifiziert InstanceId verdeckt und identifiziert eine Instanz dieser Klasse eindeutig. Um die Eindeutigkeit innerhalb des Namespaces sicherzustellen, sollte der Wert von InstanceId mit dem folgenden "bevorzugten" Algorithmus erstellt werden: *OrgId*:*localId* , bei der *OrgId* und *localId* durch einen Doppelpunkt (:)) getrennt sind und *OrgId* einen urheberrechtlich geschützten, mit einem Wert gekennzeichneten oder anderweitig eindeutigen Namen enthalten muss, der im Besitz der Geschäfts Entität ist, die die InstanceId erstellt oder definiert, oder bei der es sich um eine registrierte, von einer anerkannten globalen Autorität zugewiesene ID handelt. (Diese Anforderung ähnelt dem Schema *Name* \_ *ClassName* -Struktur von Schema Klassennamen.) Außerdem darf *OrgId* keinen Doppelpunkt (:) enthalten, um die Eindeutigkeit sicherzustellen. Wenn dieser Algorithmus verwendet wird, muss der erste Doppelpunkt, der in InstanceId angezeigt wird, zwischen *OrgId* und *localId* angezeigt werden. *LocalId* wird von der Geschäfts Entität ausgewählt und sollte nicht wieder verwendet werden, um verschiedene zugrunde liegende (reale) Elemente zu identifizieren. Wenn der oben genannte bevorzugte Algorithmus nicht verwendet wird, muss die definierende Entität sicherstellen, dass die resultierende InstanceId nicht für instanceids wieder verwendet wird, die von diesem oder anderen Anbietern für den Namespace dieser Instanz erstellt werden. Für von DMTF definierte Instanzen muss der "bevorzugte" Algorithmus verwendet werden, wenn die *OrgId* auf CIM festgelegt ist.

</dd> <dt>

**OptionalData**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

**Qualifizierer: octetstring**, [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")
</dt> </dl>

Optionale Daten, die von der Firmware bereitgestellt werden.

> [!Note]  
> Die Eigenschaft wurde in Windows 10 hinzugefügt.

 

</dd> <dt>

**Otherlocation**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die anderen Standortinformationen, sofern vorhanden, die die Firmware zur weiteren eindeutigen Identifizierung der Start Quelle verwendet.

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

[**CIM- \_ SettingData**](cim-settingdata.md)
</dt> <dt>

[**CIM- \_ SettingData**](/previous-versions//cc136911(v=vs.85))
</dt> </dl>

 

