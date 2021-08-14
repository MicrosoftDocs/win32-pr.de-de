---
description: Definiert einen Typ für das SubscriberID-Element des Mobile Broadband-Profils.
ms.assetid: b36df4d3-f558-4af8-8f63-e4991c34990f
title: subscriberIdType Simple Type
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- subscriberIdType
api_type:
- Schema
ms.openlocfilehash: aac83be84ae313f572d82e6b4c9a2afb14beeb7e15c531eaae7efd67bcc90464
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117881364"
---
# <a name="subscriberidtype-simple-type"></a>subscriberIdType Simple Type

Der **einfache Typ subscriberIdType** definiert einen Typ für das [**SubscriberID-Element**](schema-subscriberid-mbnprofile-element.md) des Mobile Broadband-Profils. Dieser Typ ist eine Auflistung von mindestens einem Zeichen.

``` syntax
<xs:simpleType name="subscriberIdType">
    <xs:restriction
        base="token"
    >
        <xs:minLength
            value="1"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps \| UWP-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                         |



 

 




