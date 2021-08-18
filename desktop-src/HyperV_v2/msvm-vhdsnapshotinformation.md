---
description: Stellt Informationen zu einer Momentaufnahme in einer VHD-Set-Datei bereit.
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
ms.openlocfilehash: c256ee2d3fb277fc98fa440403cf385377d7f64160267ff39a2d905c59f9d3ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068450"
---
# <a name="msvm_vhdsnapshotinformation-class"></a>Msvm \_ VHDSnapshotInformation-Klasse

Stellt Informationen zu einer Momentaufnahme in einer VHD-Set-Datei bereit.

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

Die **\_ Msvm-VHDSnapshotInformation-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ VHDSnapshotInformation-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Creationtime**
</dt> <dd> <dl> <dt>

Datentyp: **DATETIME**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Datum und Uhrzeit der Erstellung dieser Momentaufnahme.

</dd> <dt>

**Filepath**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Pfad der VHD-Set-Datei.

</dd> <dt>

**ParentPathsList**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Liste von Dateipfaden, die alle Dateien darstellen, von denen diese Momentaufnahme abhängt. Dieses Feld ist leer, sofern nicht ausdrücklich angefordert. Der erste Eintrag ist das unmittelbar übergeordnete Element der Datei, wobei der letzte Eintrag der Stamm ist.

</dd> <dt>

**ResilientChangeTrackingId**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die robuste Änderungsnachverfolgungs-ID, sofern vorhanden, die dieser Momentaufnahme zugeordnet ist.

</dd> <dt>

**SnapshotId**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine GUID, die diese Momentaufnahme innerhalb der VHD-Set-Datei eindeutig identifiziert.

</dd> <dt>

**SnapshotPath**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Pfad der durch diese Momentaufnahme dargestellten Datei. Dieses Feld ist möglicherweise leer, wenn dieser Momentaufnahme keine Datei zugeordnet ist.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Root-Virtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

 




