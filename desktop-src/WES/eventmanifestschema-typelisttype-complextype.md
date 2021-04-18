---
title: Komplexer typelisttype-Typ
description: Definiert die Typen, die im Manifest verwendet werden.
ms.assetid: e7ce0ecf-3bd0-49ab-82c7-dc28fd0e59a2
keywords:
- Typelisttype komplexer Typ EventLog
topic_type:
- apiref
api_name:
- TypeListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 61cec902684d7426a5951c12c4b319ae1ce29923
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344695"
---
# <a name="typelisttype-complex-type"></a>Komplexer typelisttype-Typ

Definiert die Typen, die im Manifest verwendet werden.

``` syntax
<xs:complexType name="TypeListType">
    <xs:choice
        maxOccurs="unbounded"
    >
        <xs:element name="xmlTypes"
            type="XmlTypeListType"
         />
        <xs:element name="inTypes"
            type="InputTypeListType"
         />
        <xs:any
            processContents="lax"
            namespace="##other"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                               | type                                                                           | BESCHREIBUNG                                                                                                 |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**Intypes**](eventmanifestschema-intypes-typelisttype-element.md)   | [**Inputtypelisttype**](eventmanifestschema-inputtypelisttype-complextype.md) | Definiert eine Liste von Eingabe Datentypen.<br/>                                                              |
| [**xmltypes**](eventmanifestschema-xmltypes-typelisttype-element.md) | [**Xmltypelisttype**](eventmanifestschema-xmltypelisttype-complextype.md)     | Definiert einen Listen Ausgabetyp, den der Dienst verwendet, um zu bestimmen, wie ein Eingabe Datentyp dargestellt werden soll.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





