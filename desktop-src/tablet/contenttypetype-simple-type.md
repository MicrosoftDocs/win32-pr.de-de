---
description: Definiert den Typ, der gültige Werte für das Type-Attribut des Inhalts Element- \[ Journal Readers definiert \] .
ms.assetid: f38f7a7e-a517-4156-9c60-e1b6d35baa07
title: Einfacher contenttypetype-Typ
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
ms.openlocfilehash: 55297be38dfd75f9ca11bfb6213cd99d52d2a7e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042414"
---
# <a name="contenttypetype-simple-type"></a>Einfacher contenttypetype-Typ

Definiert den Typ, der gültige Werte für das *Type* -Attribut des [Inhalts Element- \[ Journal \] Readers](content-element--journal-reader.md)definiert.

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

Der einfache **contenttypetype** -Typ ist eine Zeichenfolge, die durch das folgende Muster eingeschränkt ist:

-   `Normal|Inert`

## <a name="remarks"></a>Bemerkungen

Gültige Werte sind "Normal" und "inert".

Wenn der Typ "inert" ist, ist der enthaltene Inhalt eine Journal Seite, bei der es sich um den schreibgeschützten/nicht bearbeitbaren "Hintergrund" für das Dokument handelt. Dieser Fehler tritt auf, wenn ein Dokument mithilfe des Druckertreibers für den Journal Hinweis Writer erstellt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                     |



 

 




