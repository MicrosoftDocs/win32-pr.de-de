---
description: Stellt eine Beziehung dar, in der ein verwaltetes Element ein Member von ist und durch eine Auflistung aggregiert wird.
ms.assetid: 324284fa-ece6-41df-9891-040a7561dce4
title: CIM_MemberOfCollection-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MemberOfCollection
- CIM_MemberOfCollection.Collection
- CIM_MemberOfCollection.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9bcebfb08cbbc0cb18e00f1b0e5e2646ca086faf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042551"
---
# <a name="cim_memberofcollection-class"></a>CIM- \_ mitgliedfassungs Klasse

Stellt eine Beziehung dar, in der ein verwaltetes Element ein Member von ist und durch eine Auflistung aggregiert wird.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Aggregation, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Core::Collection"), AMENDMENT]
class CIM_MemberOfCollection
{
  CIM_Collection     REF Collection;
  CIM_ManagedElement REF Member;
};
```

## <a name="members"></a>Member

Die **CIM- \_ mitgliedfassungs** Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM- \_ Mitgliedschafts** Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Sammlung**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_** -Auflistung
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier), [**Aggregat**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Die Auflistung, die Elemente aggregiert.

</dd> <dt>

**Member**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ managedelta**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Der Member der Auflistung.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

