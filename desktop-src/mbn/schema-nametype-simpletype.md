---
description: Definiert einen Zeichenfolgentyp für das Mobile Breitbandprofil.
ms.assetid: a5c14c39-2731-44f0-9fd2-e78d900b66f0
title: 'nameType : einfacher Typ (mobiles Breitband)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- nameType
api_type:
- Schema
ms.openlocfilehash: 9b07bfb62e23b0c82ef69bc924147675caad10d61258a5c49edc906c4b6bf2a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117881404"
---
# <a name="nametype-simple-type-mobile-broadband"></a>nameType : einfacher Typ (mobiles Breitband)

Der einfache **NameType-Typ** definiert einen Zeichenfolgentyp für das Mobile Breitbandprofil. Diese Zeichenfolge ist mindestens ein Zeichen lang und höchstens 255 Zeichen lang.

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
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps \| UWP-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                         |



 

 




