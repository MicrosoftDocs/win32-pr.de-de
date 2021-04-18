---
title: Einfacher csymboltype-Typ (Windows-Ereignisprotokoll)
description: Definiert einen gültigen C/C++-Symbolnamen.
ms.assetid: d19827b6-2b61-4d75-ac9d-56a384b0cc4b
keywords:
- Csymboltype Simple Event Log-Typ
topic_type:
- apiref
api_name:
- CSymbolType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 67b0ccb7c573aa4d71c038f9133cea7c95cdfbd3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340328"
---
# <a name="csymboltype-simple-type-windows-event-log"></a>Einfacher csymboltype-Typ (Windows-Ereignisprotokoll)

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

    Der Symbol Name kann leer sein oder alphanumerische Zeichen und Unterstriche enthalten. Wenn der Name leer ist, generiert der Nachrichten Compiler den Symbolnamen. Wenn Sie einen Namen angeben, muss der Name mit einem Unterstrich ( \_ ) oder einem alphabetischen Zeichen beginnen.

## <a name="remarks"></a>Bemerkungen

Wenn der Symbol Name leer ist, verwendet der Nachrichten Compiler das **Name** -Attribut des-Elements, das Sie definieren, um den Symbolnamen zu generieren. Der Compiler ersetzt alle nicht alphanumerischen Zeichen und vorangestellten Ziffern durch Unterstriche. Wenn das **Name** -Attribut des Kanals z. b. Microsoft-Windows-SampleProvider/Operational ist, verwendet der Compiler Microsoft \_ Windows \_ Sample Provider \_ Operational als Symbolnamen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/> |



 

 





