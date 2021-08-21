---
description: Definiert einen Typ für das SimIccID-Element des Mobile Broadband-Profils.
ms.assetid: ce77180e-71e2-4cef-84e0-32397216385f
title: simIccIDType Simple Type
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- simIccIDType
api_type:
- Schema
ms.openlocfilehash: 33a984875e1e6840787d81dc53c8fc13ead54a0328f6610d75c30075066c13c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035758"
---
# <a name="simiccidtype-simple-type"></a>simIccIDType Simple Type

Der **einfache SimIccIDType-Typ** definiert einen Typ für das [**SimIccID-Element**](schema-simiccid-mbnprofile-element.md) des Mobilen Breitbandprofils. Dieser Typ ist eine Sammlung von Ziffern und/oder Groß- und Kleinbuchstaben, mindestens ein Zeichen lang und mindestens 20 Zeichen lang.

``` syntax
<xs:simpleType name="simIccIDType">
    <xs:restriction
        base="token"
    >
        <xs:pattern
            value="[a-zA-Z\d]{1,20}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Muster

Der **einfache SimIccIDType-Typ** ist ein Token, das durch das folgende Muster eingeschränkt wird:

-   `[a-zA-Z\d]{1,20}`

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps \| UWP-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                         |



 

 




