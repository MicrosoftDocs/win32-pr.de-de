---
title: strTableRef Simple Type
description: Definiert eine Zeichenfolge, die auf eine Meldungszeichenfolge verweist, die in einer Zeichenfolgentabelle im Manifest oder in einer Meldungsdatei (.mc) definiert ist.
ms.assetid: ecbcefcb-3265-4508-be7d-17a0fe3fe911
keywords:
- strTableRef – einfacher Typ EventLog
topic_type:
- apiref
api_name:
- strTableRef
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 97280b342015338be1cea089f8cb14121e2e51466506e89818501302c3fa891a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117750916"
---
# <a name="strtableref-simple-type"></a>strTableRef Simple Type

Definiert eine Zeichenfolge, die auf eine Meldungszeichenfolge verweist, die in einer Zeichenfolgentabelle im Manifest oder in einer Meldungsdatei (.mc) definiert ist.

``` syntax
<xs:simpleType name="strTableRef">
    <xs:restriction
        base="xs:string"
    >
        <xs:pattern
            value="(\$([Ss]tring\..*))|(\$([Mm][Cc]\..*))"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Muster

Der einfache **strTableRef-Typ** ist eine **xs:string-Zeichenfolge,** die durch das folgende Muster eingeschränkt ist:

-   `(\$([Ss]tring\..*))|(\$([Mm][Cc]\..*))`

    Die Zeichenfolge muss das Format haben, $string. *stringid* oder $mc.*symbolid*. Wenn die Zeichenfolge das Format auf hat, $string. *stringid*, muss im [**StringTable-Abschnitt**](eventmanifestschema-stringtable-resources-element.md) des Manifests auf eine Zeichenfolge verweisen. Wenn die Zeichenfolge das Format hat, $mc.*symbolid*, muss sie auf ein in der Meldungsdatei definiertes Symbol verweisen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/> |



 

 





