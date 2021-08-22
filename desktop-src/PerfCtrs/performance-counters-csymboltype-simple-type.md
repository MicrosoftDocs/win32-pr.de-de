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
ms.openlocfilehash: e4ebba4d72b7bc79f2aaefccfa2d71e57abd82aa06efb09abc2e83cebdb513f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033530"
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

Der **einfache CSymbolType-Typ** ist ein **xs:string-Objekt,** das durch das folgende Muster eingeschränkt ist:

-   `()|([_a-zA-Z][_0-9a-zA-Z]*)`

    Der Symbolname kann leer sein oder alphanumerische Zeichen und Unterstriche enthalten. Wenn Sie einen Namen angeben, muss der Name mit einem Unterstrich ( ) oder einem \_ alphabetischen Zeichen beginnen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 




