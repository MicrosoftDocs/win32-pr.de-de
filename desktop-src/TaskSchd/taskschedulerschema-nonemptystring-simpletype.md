---
title: nonEmptyStringType Simple Type
description: Definiert die Werte, die für eine nicht leere Textzeichenfolge verwendet werden.
ms.assetid: cb3b1ca6-4531-467c-a27a-b27a62233514
keywords:
- 'nonEmptyString: einfache Taskplaner'
topic_type:
- apiref
api_name:
- nonEmptyString
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6359240c2baba14460ab4478c31c490725646130ea2181efdcb8e92a94090d5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758416"
---
# <a name="nonemptystringtype-simple-type"></a>nonEmptyStringType Simple Type

Definiert die Werte, die für eine nicht leere Textzeichenfolge verwendet werden.

``` syntax
<xs:simpleType name="nonEmptyString">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="1"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Enumerationswerte

Der **einfache NonEmptyString-Typ** definiert den folgenden Wert.



| Wert | Beschreibung                                            |
|-------|--------------------------------------------------------|
| 1     | Die Zeichenfolge enthält mindestens ein Zeichen.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





