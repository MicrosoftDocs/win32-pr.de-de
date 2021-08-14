---
title: Einfacher CSymbolType-Typ (Windows Ereignisprotokoll)
description: 'CSymbolType Simple Type (Windows Ereignisprotokoll): Definiert einen gültigen C/C++-Symbolnamen.'
ms.assetid: d19827b6-2b61-4d75-ac9d-56a384b0cc4b
keywords:
- 'CSymbolType: Einfacher Typ EventLog'
topic_type:
- apiref
api_name:
- CSymbolType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5e51438a49a45c167b247882f0976b27a4ad8d4da048437f385ccff545663b4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118589893"
---
# <a name="csymboltype-simple-type-windows-event-log"></a>Einfacher CSymbolType-Typ (Windows Ereignisprotokoll)

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

    Der Symbolname kann leer sein oder alphanumerische Zeichen und Unterstriche enthalten. Wenn der Name leer ist, generiert der Nachrichtencompiler den Symbolnamen. Wenn Sie einen Namen angeben, muss der Name mit einem Unterstrich \_ () oder einem alphabetischen Zeichen beginnen.

## <a name="remarks"></a>Bemerkungen

Wenn der Symbolname leer ist, verwendet der Nachrichtencompiler das **Name-Attribut** des Elements, das Sie definieren, um den Symbolnamen zu generieren. Der Compiler ersetzt alle nicht alphanumerischen Zeichen und führenden Ziffern durch Unterstriche. Wenn das Namensattribut  des Kanals beispielsweise Microsoft-Windows-SampleProvider/Operational lautet, verwendet der Compiler Microsoft \_ Windows \_ SampleProvider Operational \_ als Symbolnamen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/> |



 

 





