---
description: Stellt die Parameter zum Kopieren einer Datei vom Host in den Gast dar.
ms.assetid: 255F4132-C212-4A3B-A9B8-3F531E7D1CF9
title: Msvm_CopyFileToGuestSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestSettingData
- Msvm_CopyFileToGuestSettingData.Description
- Msvm_CopyFileToGuestSettingData.Caption
- Msvm_CopyFileToGuestSettingData.InstanceID
- Msvm_CopyFileToGuestSettingData.ElementName
- Msvm_CopyFileToGuestSettingData.OverwriteExisting
- Msvm_CopyFileToGuestSettingData.CreateFullPath
- Msvm_CopyFileToGuestSettingData.SourcePath
- Msvm_CopyFileToGuestSettingData.DestinationPath
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6eb011ec8d03153bd5f1b7d956775327d2582410e9ca12591e19a39ddb4af5fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118148839"
---
# <a name="msvm_copyfiletoguestsettingdata-class"></a>Msvm \_ CopyFileToGuestSettingData-Klasse

Stellt die Parameter zum Kopieren einer Datei vom Host in den Gast dar. Diese Klasse wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))abgeleitet.

Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.

## <a name="syntax"></a>Syntax

``` syntax
[AMENDMENT]
class Msvm_CopyFileToGuestSettingData : CIM_SettingData
{
  string  Description;
  string  Caption;
  string  InstanceID;
  string  ElementName;
  boolean OverwriteExisting;
  boolean CreateFullPath;
  string  SourcePath;
  string  DestinationPath;
};
```

## <a name="members"></a>Member

Die **Msvm \_ CopyFileToGuestSettingData-Klasse** verfügt über folgende Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ CopyFileToGuestSettingData-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

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

**CreateFullPath**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob fehlende Verzeichnisse im Pfad der Zieldatei vor dem Kopieren der Datei erstellt werden müssen.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Textbeschreibung des Objekts.

</dd> <dt>

**DestinationPath**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der vollständige Pfad der zu kopierenden Zieldatei. Diese Zieldatei muss für den Gast zugänglich sein und kann Umgebungsvariablen enthalten, die vom Gast erweitert werden. Wenn der angegebene Pfad ein vorhandenes Verzeichnis im Gast ist, wird die Zieldatei in diesem Verzeichnis erstellt. In diesem Fall wird der Dateiname aus **SourcePath** als Zieldateiname verwendet.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Anzeigename für diese Instanz von SettingData. Darüber hinaus kann der Anzeigename als Indexeigenschaft für eine Suche oder Abfrage verwendet werden. (Hinweis: Der Name muss innerhalb eines Namespace nicht eindeutig sein.)

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

**OverwriteExisting**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob eine vorhandene Zieldatei überschrieben werden muss.

</dd> <dt>

**Sourcepath**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der vollständige Pfad der zu kopierenden Quelldatei. Diese Quelldatei muss für den Hyper-V-Host zugänglich sein und kann Umgebungsvariablen enthalten, die durch den Hyper-V-Host erweitert werden.

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

 

