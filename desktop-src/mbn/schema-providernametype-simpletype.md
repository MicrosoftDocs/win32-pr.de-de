---
description: Definiert einen Zeichenfolgentyp für das ProviderName-Element im Mobile Broadband-Profil.
ms.assetid: 1644ded2-f931-4920-848d-e0405d8723e3
title: providerNameType Simple Type
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- providerNameType
api_type:
- Schema
ms.openlocfilehash: e0a1a0c999eebe8d4ac9922564a28f3b8abce90397fbbda3556bf7726c7355cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118744389"
---
# <a name="providernametype-simple-type"></a>providerNameType Simple Type

Der **einfache Typ providerNameType** definiert einen Zeichenfolgentyp für das [**ProviderName-Element**](schema-providername-providertype-element.md) im Mobile Broadband-Profil. Diese Zeichenfolge ist mindestens ein Zeichen lang und mindestens 20 Zeichen lang.

``` syntax
<xs:simpleType name="providerNameType">
    <xs:restriction
        base="normalizedString"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="20"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps \| UWP-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                         |



 

 




