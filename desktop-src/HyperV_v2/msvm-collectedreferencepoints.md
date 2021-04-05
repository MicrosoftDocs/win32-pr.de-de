---
description: Ordnet die MSVM \_ referencepointcollection den enthaltenen MSVM \_ virtualsystemreferencepoint-Objekten zu.
ms.assetid: 826125c3-0a89-4573-ac28-88588eac248d
title: Msvm_CollectedReferencePoints-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectedReferencePoints
- Msvm_CollectedReferencePoints.Collection
- Msvm_CollectedReferencePoints.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4891d4ec4c613c92c3b5d5a090f2683bfc77dc5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753024"
---
# <a name="msvm_collectedreferencepoints-class"></a>MSVM \_ collectedreferencepoints-Klasse

Ordnet die [**MSVM \_ referencepointcollection**](msvm-referencepointcollection.md) den enthaltenen [**MSVM \_ virtualsystemreferencepoint**](msvm-virtualsystemreferencepoint.md) -Objekten zu.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectedReferencePoints : CIM_CollectedMSEs
{
  Msvm_ReferencePointCollection    REF Collection;
  Msvm_VirtualSystemReferencePoint REF Member;
};
```

## <a name="members"></a>Member

Die **MSVM \_ collectedreferencepoints** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ collectedreferencepoints** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Sammlung**
</dt> <dd> <dl> <dt>

Datentyp: **MSVM \_ referencepointcollection**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")
</dt> </dl>

Eine [**MSVM- \_ referencepointcollection**](msvm-referencepointcollection.md) -Gruppierung oder ein "Bag"-Objekt, das die Auflistung darstellt.

</dd> <dt>

**Member**
</dt> <dd> <dl> <dt>

Datentyp: **MSVM \_ virtualsystemreferencepoint**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")
</dt> </dl>

Ein [**MSVM \_ virtualsystemreferencepoint**](msvm-virtualsystemreferencepoint.md) , der die Member der Auflistung enthält.

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

 

