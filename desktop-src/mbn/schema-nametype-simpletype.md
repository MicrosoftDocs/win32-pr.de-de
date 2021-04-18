---
description: Definiert einen Zeichen Folgentyp für das mobile Breitband Profil.
ms.assetid: a5c14c39-2731-44f0-9fd2-e78d900b66f0
title: einfacher nametype-Typ (mobiles Breitband)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- nameType
api_type:
- Schema
ms.openlocfilehash: d8c6032e17eaf2d067dc23030a7a6279bd41eafa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347788"
---
# <a name="nametype-simple-type-mobile-broadband"></a>einfacher nametype-Typ (mobiles Breitband)

Der einfache **nametype** -Typ definiert einen Zeichen Folgentyp für das mobile Breitband Profil. Bei dieser Zeichenfolge handelt es sich um mindestens ein Zeichen, das höchstens 255 Zeichen lang ist.

``` syntax
<xs:simpleType name="nameType">
    <xs:restriction
        base="normalizedString"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="255"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ -Desktop-Apps \| UWP-apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                         |



 

 




