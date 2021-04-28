---
title: Einfacher CSymbolType-Typ (Windows-Ereignisprotokoll)
description: 'Einfacher CSymbolType-Typ (Windows-Ereignisprotokoll): Definiert einen gültigen C/C++-Symbolnamen.'
ms.assetid: d19827b6-2b61-4d75-ac9d-56a384b0cc4b
keywords:
- Einfacher CSymbolType-Typ EventLog
topic_type:
- apiref
api_name:
- CSymbolType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e0c8c17a9f4bb7e86b573d60187ffffd55c6cb96
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090618"
---
# <a name="csymboltype-simple-type-windows-event-log"></a>Einfacher CSymbolType-Typ (Windows-Ereignisprotokoll)

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

    Der Symbolname kann leer sein oder alphanumerische Zeichen und Unterstriche enthalten. Wenn der Name leer ist, generiert der Nachrichtencompiler den Symbolnamen. Wenn Sie einen Namen angeben, muss der Name mit einem Unterstrich ( ) oder einem \_ alphabetischen Zeichen beginnen.

## <a name="remarks"></a>Bemerkungen

Wenn der Symbolname leer ist, verwendet der Nachrichtencompiler das **Name-Attribut** des Elements, das Sie definieren, um den Symbolnamen zu generieren. Der Compiler ersetzt alle nicht alphanumerischen Zeichen und führenden Ziffern durch Unterstriche. Wenn das Name-Attribut  des Kanals beispielsweise Microsoft-Windows-SampleProvider/Operational ist, verwendet der Compiler Microsoft Windows SampleProvider Operational als \_ \_ \_ Symbolnamen.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ 7-Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ R2-Desktop-Apps\]<br/> |



 

 





