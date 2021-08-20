---
description: Ordnet die Msvm \_ ReferencePointCollection den entsprechenden Msvm \_ VirtualSystemCollection-Objekten zu.
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
ms.openlocfilehash: 4dfa8e8ab6c0d46f020116d4b9e9d0c1ea07b2e67d334896462950b371d368c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119789600"
---
# <a name="msvm_referencepointofvirtualsystemcollection-class"></a>Msvm \_ ReferencePointOfVirtualSystemCollection-Klasse

Ordnet die [**Msvm \_ ReferencePointCollection**](msvm-referencepointcollection.md) den entsprechenden [**Msvm \_ VirtualSystemCollection-Objekten**](msvm-virtualsystemcollection.md) zu.

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

Die **Msvm \_ ReferencePointOfVirtualSystemCollection-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ ReferencePointOfVirtualSystemCollection-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Vorläufer**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ CollectionOfMSEs**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Eine [**\_ CIM-CollectionOfMSEs,**](cim-collectionofmses.md) die das unabhängige Objekt in dieser Zuordnung darstellt.

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **\_ CIM-Sammlung**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")
</dt> </dl>

Eine [**\_ CIM-Auflistung,**](cim-collection.md) die das Objekt darstellt, das von der **-Klasse abhängig ist.**

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_CIM-Abhängigkeit**](cim-dependency.md)
</dt> </dl>

 

