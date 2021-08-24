---
description: Stellt Informationen zu einer VHD-Satzdatei zur Verfügung.
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
ms.openlocfilehash: d8cef737c02629ac0a1a026a459adf6eb7060e0dbdf8c0f9ecb20c66fce1259e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119789430"
---
# <a name="msvm_vhdsetinformation-class"></a>Msvm \_ VHDSetInformation-Klasse

Stellt Informationen zu einer VHD-Satzdatei zur Verfügung.

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

Die **Msvm \_ VHDSetInformation-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ VHDSetInformation-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**AllPaths**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Liste aller Dateien, die von der VHD-Set-Datei umfasst werden, einschließlich aller dateien, auf die nichtreferenziert wird, und aller der virtuellen Stammfestplatte. Alle Dateien, die nach der virtuellen Stammfestplatte aufgelistet sind, werden von dieser VHD-Satzdatei nicht verwaltet. Dieses Feld ist möglicherweise leer, wenn diese Informationen nicht ausdrücklich angefordert wurden.

</dd> <dt>

**Path**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Pfad der VHD-Set-Datei.

</dd> <dt>

**SnapshotIdList**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Liste von GUIDs, die alle In dieser VHD-Satzdatei enthaltenen Momentaufnahmen darstellen.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

 




