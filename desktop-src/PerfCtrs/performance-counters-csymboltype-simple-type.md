---
description: Definiert einen gültigen C/C++-Symbolnamen.
ms.assetid: 75f74a16-0be4-466b-a88d-247c8c94f4ce
title: Einfacher csymboltype-Typ (Leistungsindikatoren)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 418b5119046a89d93814ed8ac8bd427dc554bf26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959754"
---
# <a name="csymboltype-simple-type-performance-counters"></a>Einfacher csymboltype-Typ (Leistungsindikatoren)

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

Der einfache **csymboltype** -Typ ist eine **xs: String** , die durch das folgende Muster eingeschränkt ist:

-   `()|([_a-zA-Z][_0-9a-zA-Z]*)`

    Der Symbol Name kann leer sein oder alphanumerische Zeichen und Unterstriche enthalten. Wenn Sie einen Namen angeben, muss der Name mit einem Unterstrich ( \_ ) oder einem alphabetischen Zeichen beginnen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 




