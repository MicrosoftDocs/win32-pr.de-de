---
description: Definiert einen Typ für das ProviderID-Element des mobilen Breitband Profils.
ms.assetid: 84193749-c98d-4313-bf99-3da1c74d7cc4
title: provideridtype simple-Typ
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- providerIdType
api_type:
- Schema
ms.openlocfilehash: ec3c952395be048d18305172e64618fa26313f46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129008"
---
# <a name="provideridtype-simple-type"></a>provideridtype simple-Typ

Der einfache Typ **provideridtype** definiert einen Typ für das [**ProviderID**](schema-providerid-providertype-element.md) -Element des mobilen Breitband Profils. Bei diesem Typ handelt es sich um eine Sammlung von Ziffern, die mindestens eine Ziffer lang und höchstens 6 Ziffern lang sind.

``` syntax
<xs:simpleType name="providerIdType">
    <xs:restriction
        base="token"
    >
        <xs:pattern
            value="\d{1,6}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Muster

Der einfache Typ **provideridtype** ist ein Token, das durch das folgende Muster eingeschränkt wird:

-   `\d{1,6}`

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ -Desktop-Apps \| UWP-apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                         |



 

 




