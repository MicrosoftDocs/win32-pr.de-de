---
description: Definiert einen Typ für das abonniert-Element des mobilen Breitband Profils.
ms.assetid: b36df4d3-f558-4af8-8f63-e4991c34990f
title: einfacher Typ des abonniert-Typs
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- subscriberIdType
api_type:
- Schema
ms.openlocfilehash: c3c776bbd721bbb03b4f5549f87d48248a35206b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041707"
---
# <a name="subscriberidtype-simple-type"></a>einfacher Typ des abonniert-Typs

Der einfache Typ " **abonniert Type** " definiert einen Typ für das " [**abonniert**](schema-subscriberid-mbnprofile-element.md) "-Element des mobilen Breitband Profils. Dieser Typ ist eine Auflistung von einem oder mehreren Zeichen.

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
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ -Desktop-Apps \| UWP-apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                         |



 

 




