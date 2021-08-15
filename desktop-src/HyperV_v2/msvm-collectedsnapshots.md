---
description: Ordnet die Msvm \_ SnapshotCollection den enthaltenen Msvm \_ VirtualSystemSettingData-Objekten zu.
ms.assetid: 21005e8a-0bc6-4ea7-8f6f-d79803b43bc0
title: Msvm_CollectedSnapshots-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectedSnapshots
- Msvm_CollectedSnapshots.Collection
- Msvm_CollectedSnapshots.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5e5a1007516e5b8b7d827f0a96e1fd7fd5541cba2277111830605971c6d8a101
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119427120"
---
# <a name="msvm_collectedsnapshots-class"></a>Msvm \_ CollectedSnapshots-Klasse

Ordnet die [**Msvm \_ SnapshotCollection**](msvm-snapshotcollection.md) den enthaltenen [**Msvm \_ VirtualSystemSettingData-Objekten**](msvm-virtualsystemsettingdata.md) zu.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectedSnapshots : CIM_CollectedMSEs
{
  Msvm_SnapshotCollection       REF Collection;
  Msvm_VirtualSystemSettingData REF Member;
};
```

## <a name="members"></a>Member

Die **Msvm \_ CollectedSnapshots-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ CollectedSnapshots-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Sammlung**
</dt> <dd> <dl> <dt>

Datentyp: **Msvm \_ SnapshotCollection**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Aggregieren,**](/windows/desktop/WmiSdk/standard-qualifiers) [**Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")
</dt> </dl>

Ein [**Msvm \_ SnapshotCollection-Gruppierungs-**](msvm-snapshotcollection.md) oder Bag-Objekt, das die Auflistung darstellt.

</dd> <dt>

**Member**
</dt> <dd> <dl> <dt>

Datentyp: **Msvm \_ VirtualSystemSettingData**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")
</dt> </dl>

Ein [**Msvm \_ VirtualSystemSettingData-Objekt,**](msvm-virtualsystemsettingdata.md) das die Member der Auflistung enthält.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**CIM \_ CollectedMSEs**](cim-collectedmses.md)
</dt> </dl>

 

