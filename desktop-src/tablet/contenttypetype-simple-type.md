---
description: Definiert den Typ, der gültige Werte für das Type-Attribut des Content-Elements \[ Journal Reader \] definiert.
ms.assetid: f38f7a7e-a517-4156-9c60-e1b6d35baa07
title: Einfacher ContentTypeType-Typ
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ContentTypeType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 83b49427e65bb5190554a0c995bec119de1230f0baab869ea4c5ce48dc5616f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008970"
---
# <a name="contenttypetype-simple-type"></a>Einfacher ContentTypeType-Typ

Definiert den Typ, der gültige Werte für das *Type-Attribut* des [Content-Elements \[ Journal Reader definiert. \]](content-element--journal-reader.md)

``` syntax
<xs:simpleType name="ContentTypeType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="Normal|Inert"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Muster

Der **einfache ContentTypeType-Typ** ist eine Zeichenfolge, die durch das folgende Muster eingeschränkt ist:

-   `Normal|Inert`

## <a name="remarks"></a>Hinweise

Gültige Werte sind "Normal" und "Inert".

Wenn der Typ "Inert" ist, ist der enthaltene Inhalt eine Journalseite, die der schreibgeschützte/nicht bearbeitbare "Hintergrund" für das Dokument ist. Dies tritt auf, wenn ein Dokument mit dem Druckertreiber Journal Note Writer erstellt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                     |



 

 




