---
description: 'Msvm_CollectedCollections -Klasse: Ordnet die Msvm \_ VirtualSystemCollection den enthaltenen Msvm \_ ComputerSystem-Objekten zu.'
ms.assetid: bbf7713a-b331-4b40-bcb4-3545c26c6f3a
title: Msvm_CollectedCollections-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectedCollections
- Msvm_CollectedCollections.Collection
- Msvm_CollectedCollections.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c645bc4c6dbf7cf6f7b3fb43cc229af3ef744b264b088356d192e4ad58e68a88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790180"
---
# <a name="msvm_collectedcollections-class"></a>Msvm \_ CollectedCollections-Klasse

Ordnet die [**Msvm \_ VirtualSystemCollection**](msvm-virtualsystemcollection.md) den enthaltenen [**Msvm \_ ComputerSystem-Objekten**](msvm-computersystem.md) zu.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectedCollections : CIM_CollectedMSEs
{
  Msvm_ManagementCollection REF Collection;
  CIM_CollectionOfMSEs      REF Member;
};
```

## <a name="members"></a>Member

Die **Msvm \_ CollectedCollections-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ CollectedCollections-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Sammlung**
</dt> <dd> <dl> <dt>

Datentyp: **Msvm \_ ManagementCollection**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Aggregieren,**](/windows/desktop/WmiSdk/standard-qualifiers) [**Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")
</dt> </dl>

Ein [**Msvm \_ ManagementCollection-Gruppierungsobjekt**](msvm-managementcollection.md) oder ein Bag-Objekt, das die Auflistung darstellt.

</dd> <dt>

**Member**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ CollectionOfMSEs**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")
</dt> </dl>

Eine [**\_ CIM-CollectionOfMSEs,**](cim-collectionofmses.md) die die Elemente der Auflistung enthält.

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

[**CIM \_ CollectedMSEs**](cim-collectedmses.md)
</dt> </dl>

 

