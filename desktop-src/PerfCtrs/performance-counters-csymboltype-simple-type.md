---
description: 'Einfacher CSymbolType-Typ (Leistungsindikatoren): Definiert einen gültigen C/C++-Symbolnamen.'
ms.assetid: 75f74a16-0be4-466b-a88d-247c8c94f4ce
title: Einfacher CSymbolType-Typ (Leistungsindikatoren)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0771bb1dffc006abf8e02e6c391278f7d0b03f11
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084228"
---
# <a name="csymboltype-simple-type-performance-counters"></a>Einfacher CSymbolType-Typ (Leistungsindikatoren)

Definiert einen gültigen C/C++-Symbolnamen.

``` syntax
<xs:simpleType name="CSymbolType">
    <xs:restriction
        base="xs:string"
    >
        <xs:pattern
            value="()|([_a-zA-Z][_0-9a-zA-Z]*)"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Muster

Der einfache **CSymbolType-Typ** ist eine **xs:string-Zeichenfolge,** die durch das folgende Muster eingeschränkt ist:

-   `()|([_a-zA-Z][_0-9a-zA-Z]*)`

    Der Symbolname kann leer sein oder alphanumerische Zeichen und Unterstriche enthalten. Wenn Sie einen Namen angeben, muss der Name mit einem Unterstrich \_ () oder einem alphabetischen Zeichen beginnen.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2008-Desktop-Apps\]<br/> |



 

 




