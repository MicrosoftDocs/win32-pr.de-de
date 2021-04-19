---
description: Ordnet die MSVM \_ virtualsystemcollection den enthaltenen MSVM \_ Computersystem-Objekten zu.
ms.assetid: ad783188-b60a-4271-aa2d-8050c36e70eb
title: Msvm_CollectedVirtualSystems-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectedVirtualSystems
- Msvm_CollectedVirtualSystems.Collection
- Msvm_CollectedVirtualSystems.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0803eda14ffbaf21ee2bf4491bd835123b7191e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366141"
---
# <a name="msvm_collectedvirtualsystems-class"></a>MSVM \_ collectedvirtualsystems-Klasse

Ordnet die [**MSVM \_ virtualsystemcollection**](msvm-virtualsystemcollection.md) den enthaltenen [**MSVM \_ Computersystem**](msvm-computersystem.md) -Objekten zu.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectedVirtualSystems : CIM_CollectedMSEs
{
  Msvm_VirtualSystemCollection REF Collection;
  Msvm_ComputerSystem          REF Member;
};
```

## <a name="members"></a>Member

Die **MSVM \_ collectedvirtualsystems** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ collectedvirtualsystems** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Sammlung**
</dt> <dd> <dl> <dt>

Datentyp: **MSVM \_ virtualsystemcollection**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")
</dt> </dl>

Eine [**MSVM- \_ virtualsystemcollection**](msvm-virtualsystemcollection.md) -Gruppierung oder ein "Bag"-Objekt, das die Auflistung darstellt.

</dd> <dt>

**Member**
</dt> <dd> <dl> <dt>

Datentyp: **MSVM \_ Computersystem**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")
</dt> </dl>

Ein [**MSVM \_ Computersystem**](msvm-computersystem.md) -Objekt, das die Member der Auflistung enthält.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ collectedmses**](cim-collectedmses.md)
</dt> </dl>

 

