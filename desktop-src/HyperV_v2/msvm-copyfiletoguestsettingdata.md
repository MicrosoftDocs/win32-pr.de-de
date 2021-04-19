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
ms.openlocfilehash: 05e27340acc9dd341bec7857c164f50344abc36f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355348"
---
# <a name="msvm_copyfiletoguestsettingdata-class"></a>MSVM \_ copyfiledeguestsettingdata-Klasse

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

Die **MSVM \_ copyfiletoguestsettingdata** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ copyfiledeguestsettingdata** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

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

**"Kreatefullpath"**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob fehlende Verzeichnisse im Pfad der Zieldatei vor dem Kopieren der Datei erstellt werden müssen.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Textbeschreibung des-Objekts.

</dd> <dt>

**DestinationPath**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der komplette Pfad der Zieldatei, die kopiert werden soll. Diese Zieldatei muss für den Gast zugänglich sein und Umgebungsvariablen enthalten können, die vom Gast erweitert werden. Wenn es sich bei dem angegebenen Pfad um ein vorhandenes Verzeichnis im Gast Verzeichnis handelt, wird die Zieldatei in diesem Verzeichnis erstellt. In diesem Fall wird der Dateiname aus **SourcePath** als Ziel Dateiname verwendet.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Anzeige Name für diese Instanz von SettingData. Außerdem kann der Anzeige Name als Index Eigenschaft für eine Suche oder Abfrage verwendet werden. (Hinweis: der Name muss innerhalb eines Namespace nicht eindeutig sein.)

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

**Überschreiben vorhanden**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob eine vorhandene Zieldatei überschrieben werden muss.

</dd> <dt>

**SourcePath**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der gesamte Pfad der Quelldatei, die kopiert werden soll. Auf diese Quelldatei muss der Hyper-v-Host zugreifen können, und Sie kann Umgebungsvariablen enthalten, die vom Hyper-v-Host erweitert werden.

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

 

