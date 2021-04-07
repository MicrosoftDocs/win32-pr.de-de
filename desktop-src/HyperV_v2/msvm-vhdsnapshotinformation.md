---
description: Stellt Informationen zu einer Momentaufnahme in einer VHD-Datei bereit.
ms.assetid: 922bf0b8-523d-488e-9a41-1a27594e2e44
title: Msvm_VHDSnapshotInformation-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VHDSnapshotInformation
- Msvm_VHDSnapshotInformation.FilePath
- Msvm_VHDSnapshotInformation.SnapshotId
- Msvm_VHDSnapshotInformation.SnapshotPath
- Msvm_VHDSnapshotInformation.ParentPathsList
- Msvm_VHDSnapshotInformation.CreationTime
- Msvm_VHDSnapshotInformation.ResilientChangeTrackingId
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1a1e2a573546d62d79170f15abddd8d5c17e30f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863287"
---
# <a name="msvm_vhdsnapshotinformation-class"></a>MSVM \_ vhdsnapshotinformation-Klasse

Stellt Informationen zu einer Momentaufnahme in einer VHD-Datei fest.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[AMENDMENT]
class Msvm_VHDSnapshotInformation
{
  string   FilePath;
  string   SnapshotId;
  string   SnapshotPath;
  string   ParentPathsList[];
  DATETIME CreationTime;
  string   ResilientChangeTrackingId;
};
```

## <a name="members"></a>Member

Die **MSVM \_ vhdsnapshotinformation** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ vhdsnapshotinformation** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**CreationTime**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Datum und die Uhrzeit der Erstellung der Momentaufnahme.

</dd> <dt>

**FilePath**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Pfad der VHD-Satz Datei.

</dd> <dt>

**"Parametripathslist"**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Liste der Dateipfade, die alle Dateien darstellen, von denen diese Momentaufnahme abhängt. Dieses Feld ist leer, es sei denn, es wird ausdrücklich angefordert. Der erste Eintrag ist das unmittelbar übergeordnete Element der Datei, wobei der letzte Eintrag der Stamm ist.

</dd> <dt>

**Resilientchangetrackingid**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die robuste Änderungsnachverfolgungs-ID, die dieser Momentaufnahme zugeordnet ist, sofern vorhanden.

</dd> <dt>

**SnapshotId**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine GUID, die diese Momentaufnahme innerhalb der VHD-Satz Datei eindeutig identifiziert.

</dd> <dt>

**SnapshotPath**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Pfad der Datei, die durch diese Momentaufnahme dargestellt wird. Dieses Feld ist möglicherweise leer, wenn dieser Momentaufnahme keine Datei zugeordnet ist.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

 




