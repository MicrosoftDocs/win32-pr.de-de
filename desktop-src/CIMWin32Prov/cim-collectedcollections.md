---
description: Die CIM \_ collectedcollections-Klasse ist eine Aggregations Zuordnung, die eine Auflistung verwalteter System Elemente (MSE) darstellt, die in einer Auflistung von MSES enthalten sind.
ms.assetid: 7baaf429-1211-4545-ace2-c6312d53c0f6
ms.tgt_platform: multiple
title: CIM_CollectedCollections-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectedCollections
- CIM_CollectedCollections.Collection
- CIM_CollectedCollections.CollectionInCollection
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e592c7799efc8c280d4cd64c2b54ed8a3ea328f6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958453"
---
# <a name="cim_collectedcollections-class"></a>CIM \_ collectedcollections-Klasse

Die **CIM \_ collectedcollections** -Klasse ist eine Aggregations Zuordnung, die eine Auflistung verwalteter System Elemente (MSE) darstellt, die in einer Auflistung von MSES enthalten sind.

> [!IMPORTANT]
> Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).

 

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
class CIM_CollectedCollections
{
  CIM_CollectionOfMSEs REF Collection;
  CIM_CollectionOfMSEs REF CollectionInCollection;
};
```

## <a name="members"></a>Member

Die **CIM \_ collectedcollections** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ collectedcollections** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Sammlung**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ CollectionOfMSEs**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verweis auf die "höhere Ebene" oder das übergeordnete Element in der Aggregation.

</dd> <dt>

**Collectionincollection**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ CollectionOfMSEs**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verweis auf die **Sammlung**"gesammelt".

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Klasse wird von WMI nicht implementiert.

Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet. Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

 




