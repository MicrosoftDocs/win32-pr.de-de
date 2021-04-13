---
title: versiontype simple-Typ
description: Definiert ein Muster, das eine Version eines Tasks angibt.
ms.assetid: e9eebbc1-5465-4af6-8b97-f1fd5827442e
keywords:
- versiontype Simple Type Taskplaner
topic_type:
- apiref
api_name:
- versionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: df7010c6ecba29ad0ade80ce403018dd626d01cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340487"
---
# <a name="versiontype-simple-type"></a>versiontype simple-Typ

Definiert ein Muster, das eine Version eines Tasks angibt.

``` syntax
<xs:simpleType name="versionType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="\d+(\.\d+){1,3}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Muster

Der einfache **versiontype** -Typ ist eine **Zeichenfolge** , die durch das folgende Muster eingeschränkt ist:

-   `\d+(\.\d+){1,3}`

    Ein Double, auf das ein, zwei oder drei Doubles folgt. Beispielsweise 1,2 oder 1.2.3.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





