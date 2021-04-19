---
description: Ordnet die MSVM \_ referencepointcollection den entsprechenden MSVM \_ virtualsystemcollection-Objekten zu.
ms.assetid: 847f1f46-364f-4c91-b9e8-4740d3da1947
title: Msvm_ReferencePointOfVirtualSystemCollection-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReferencePointOfVirtualSystemCollection
- Msvm_ReferencePointOfVirtualSystemCollection.Antecedent
- Msvm_ReferencePointOfVirtualSystemCollection.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0919b8666915817d8475908b0305e90ea39e60f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349883"
---
# <a name="msvm_referencepointofvirtualsystemcollection-class"></a>MSVM \_ referencepoinpofvirtualsystemcollection-Klasse

Ordnet die [**MSVM \_ referencepointcollection**](msvm-referencepointcollection.md) den entsprechenden [**MSVM \_ virtualsystemcollection**](msvm-virtualsystemcollection.md) -Objekten zu.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReferencePointOfVirtualSystemCollection : CIM_Dependency
{
  CIM_CollectionOfMSEs REF Antecedent;
  CIM_Collection       REF Dependent;
};
```

## <a name="members"></a>Member

Die **MSVM \_ referencepointofvirtualsystemcollection** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ referencepoinpofvirtualsystemcollection** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Vorgänger**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ CollectionOfMSEs**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorgänger")
</dt> </dl>

Ein [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) , das das unabhängige Objekt in dieser Zuordnung darstellt.

</dd> <dt>

**Dependent**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_** -Auflistung
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")
</dt> </dl>

Eine [**CIM \_**](cim-collection.md) -Auflistung, die das Objekt darstellt, das von dem **Vorgänger** abhängig ist.

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

[**CIM- \_ Abhängigkeit**](cim-dependency.md)
</dt> </dl>

 

