---
description: Stellt Informationen zu einer VHD-Datei bereit.
ms.assetid: a975c131-d3f3-4be3-bc69-e277e3ce4d28
title: Msvm_VHDSetInformation-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VHDSetInformation
- Msvm_VHDSetInformation.Path
- Msvm_VHDSetInformation.SnapshotIdList
- Msvm_VHDSetInformation.AllPaths
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 51f1371baea902627160c2c7a1fb31d156be8951
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349071"
---
# <a name="msvm_vhdsetinformation-class"></a>MSVM \_ vhdsetinformation-Klasse

Stellt Informationen zu einer VHD-Datei bereit.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[AMENDMENT]
class Msvm_VHDSetInformation
{
  string Path;
  string SnapshotIdList[];
  string AllPaths[];
};
```

## <a name="members"></a>Member

Die **MSVM \_ vhdsetinformation** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ vhdsetinformation** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Allpath**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Liste aller Dateien, die von der VHD-Set-Datei eingeschlossen werden, einschließlich aller Dateien, auf die nicht verwiesen wird, und aller übergeordneten Elemente der virtuellen Stamm Festplatte. Alle Dateien, die nach der virtuellen Stamm Festplatte aufgeführt sind, werden von dieser VHD-Datei nicht mehr verwaltet. Dieses Feld ist möglicherweise leer, wenn diese Informationen nicht ausdrücklich angefordert wurden.

</dd> <dt>

**Pfad**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Pfad der VHD-Satz Datei.

</dd> <dt>

**Snapshotidlist**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Liste von GUIDs, die alle in dieser VHD-Satz Datei enthaltenen Momentaufnahmen darstellen.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

 




