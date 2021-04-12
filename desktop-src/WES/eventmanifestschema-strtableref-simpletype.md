---
title: der einfache Typ "strautableref"
description: Definiert eine Zeichenfolge, die auf eine Meldungs Zeichenfolge verweist, die in einer Zeichen folgen Tabelle im Manifest oder in einer Nachrichtendatei (. MC) definiert ist.
ms.assetid: ecbcefcb-3265-4508-be7d-17a0fe3fe911
keywords:
- "\"\" \"\"."
topic_type:
- apiref
api_name:
- strTableRef
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 95b7db446af056987e2aa25cd1483e9e53c01d39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517999"
---
# <a name="strtableref-simple-type"></a>der einfache Typ "strautableref"

Definiert eine Zeichenfolge, die auf eine Meldungs Zeichenfolge verweist, die in einer Zeichen folgen Tabelle im Manifest oder in einer Nachrichtendatei (. MC) definiert ist.

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

Der einfache Typ " **strautableref** " ist eine " **xs: String** ", die durch das folgende Muster eingeschränkt ist:

-   `(\$([Ss]tring\..*))|(\$([Mm][Cc]\..*))`

    Die Zeichenfolge muss das Format haben, $String. *stringID* oder $MC.*symbolid*. Wenn die Zeichenfolge das Formular ist, $String. *stringID* muss im [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) -Abschnitt des Manifests auf eine Zeichenfolge verweisen. Wenn die Zeichenfolge das Format $MC.*symbolid* hat, muss Sie auf ein Symbol verweisen, das in der Nachrichtendatei definiert ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/> |



 

 





