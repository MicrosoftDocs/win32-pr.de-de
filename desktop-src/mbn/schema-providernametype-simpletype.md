---
description: Definiert einen Zeichen Folgentyp für das ProviderName-Element im mobilen Breitband Profil.
ms.assetid: 1644ded2-f931-4920-848d-e0405d8723e3
title: providernametype simple-Typ
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- providerNameType
api_type:
- Schema
ms.openlocfilehash: df61473358a9ed4453bc28f1b5c7974082e515bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526021"
---
# <a name="providernametype-simple-type"></a>providernametype simple-Typ

Der einfache Typ **providernametype** definiert einen Zeichen Folgentyp für das [**providerName**](schema-providername-providertype-element.md) -Element im mobilen Breitband Profil. Bei dieser Zeichenfolge handelt es sich um mindestens ein Zeichen, das höchstens 20 Zeichen lang ist.

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
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ -Desktop-Apps \| UWP-apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                         |



 

 




