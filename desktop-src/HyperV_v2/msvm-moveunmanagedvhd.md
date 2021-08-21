---
description: Verschiebt eine virtuelle Festplatte von der Quelle in den Zielpfad.
ms.assetid: f51f7bf3-585a-442d-b84d-51d633c38dea
title: Msvm_MoveUnmanagedVhd-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MoveUnmanagedVhd
- Msvm_MoveUnmanagedVhd.VhdSourcePath
- Msvm_MoveUnmanagedVhd.VhdDestinationPath
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e631b95c9961262df288b76cf83f953589780c2feb294e940314d08975bcfd57
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119521120"
---
# <a name="msvm_moveunmanagedvhd-class"></a>Msvm \_ MoveUnmanagedVhd-Klasse

Verschiebt eine virtuelle Festplatte von der Quelle in den Zielpfad.

Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_MoveUnmanagedVhd : CIM_ManagedElement
{
  string VhdSourcePath;
  string VhdDestinationPath;
};
```

## <a name="members"></a>Member

Die **Msvm \_ MoveUnmanagedVhd-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ MoveUnmanagedVhd-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**VhdDestinationPath**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Zielpfad.

</dd> <dt>

**VhdSourcePath**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Quellpfad der virtuellen Festplatte, die verschoben werden soll.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Root-Virtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ ManagedElement**](cim-managedelement.md)
</dt> </dl>

 

 




