---
title: Einfacher CountType-Typ
description: Definiert einen Count-Typ, der verwendet wird, um die Anzahl der Elemente in einem Array anzugeben.
ms.assetid: 84f819d7-5c42-475b-9144-aaa5e2d215c8
keywords:
- CountType simple type EventLog
topic_type:
- apiref
api_name:
- CountType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 63476d70a9bb5b336449a65707664c05c56a20b4c2c9fa4888c0c3125f129d90
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863620"
---
# <a name="counttype-simple-type"></a>Einfacher CountType-Typ

Definiert einen Count-Typ, der verwendet wird, um die Anzahl der Elemente in einem Array anzugeben. Der Wert kann als xs:unsignedShort-Wert oder als Zeichenfolge angegeben werden, die auf den Namen des Datenelementknotens verweist, der den nicht definierten Short-Wert enthält.

``` syntax
<xs:simpleType name="CountType">
    <xs:union
        memberValues="unsignedShort string"
     />
</xs:simpleType>
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





