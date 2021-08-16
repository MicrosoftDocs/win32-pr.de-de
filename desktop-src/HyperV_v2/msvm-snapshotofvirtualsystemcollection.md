---
description: Ordnet die Msvm \_ SnapshotCollection den entsprechenden Msvm \_ VirtualSystemCollection-Objekten zu.
ms.assetid: 4dbfe21f-e700-4266-aedb-236c57c424f6
title: Msvm_SnapshotOfVirtualSystemCollection-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SnapshotOfVirtualSystemCollection
- Msvm_SnapshotOfVirtualSystemCollection.Antecedent
- Msvm_SnapshotOfVirtualSystemCollection.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 151a54c99376cdf7d9e5f2e14fa0fd3c903d3659c12310212304a1a2b2f2e339
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950249"
---
# <a name="msvm_snapshotofvirtualsystemcollection-class"></a>Msvm \_ SnapshotOfVirtualSystemCollection-Klasse

Ordnet die [**Msvm \_ SnapshotCollection**](msvm-snapshotcollection.md) den entsprechenden [**Msvm \_ VirtualSystemCollection-Objekten**](msvm-virtualsystemcollection.md) zu.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SnapshotOfVirtualSystemCollection : CIM_Dependency
{
  CIM_CollectionOfMSEs REF Antecedent;
  CIM_Collection       REF Dependent;
};
```

## <a name="members"></a>Member

Die **Msvm \_ SnapshotOfVirtualSystemCollection-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ SnapshotOfVirtualSystemCollection-Klasse** verfügt über diese Eigenschaften.

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

Eine [**\_ CIM-Auflistung,**](cim-collection.md) die das Objekt darstellt, das vom **Vordenten abhängig ist.**

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_CIM-Abhängigkeit**](cim-dependency.md)
</dt> </dl>

 

