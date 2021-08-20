---
title: Komplexer StringTableType-Typ
description: Definiert eine Liste lokalisierter Zeichenfolgen, auf die Sie in Ihrem Manifest verweisen können. | Komplexer StringTableType-Typ
ms.assetid: 47a59ff7-aaf6-4200-805b-0a8b5f57f101
keywords:
- Komplexer StringTableType-Typ EventLog
topic_type:
- apiref
api_name:
- StringTableType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f5d52f19ca01a926c82fcc1e13cc7191866722ba5e0e6eef81e916e244744783
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118342984"
---
# <a name="stringtabletype-complex-type"></a>Komplexer StringTableType-Typ

Definiert eine Liste lokalisierter Zeichenfolgen, auf die Sie in Ihrem Manifest verweisen können.

``` syntax
<xs:complexType name="StringTableType">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
        <xs:element name="string">
            <xs:complexType
                mixed="true"
            >
                <xs:attribute name="id"
                    type="string"
                    use="required"
                 />
                <xs:attribute name="value"
                    type="string"
                    use="required"
                 />
                <xs:attribute name="stringType"
                    type="string"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
    </xs:choice>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                              | Typ | Beschreibung                            |
|----------------------------------------------------------------------|------|----------------------------------------|
| [**Schnur**](eventmanifestschema-string-stringtabletype-element.md) |      | Definiert eine lokalisierte Zeichenfolge.<br/> |



## <a name="attributes"></a>Attributes



| Name       | Typ   | BESCHREIBUNG                                                                                                              |
|------------|--------|--------------------------------------------------------------------------------------------------------------------------|
| id         | Zeichenfolge | Ein Bezeichner, der die Zeichenfolge innerhalb der Zeichenfolgentabelle eindeutig identifiziert. Beispiel: "Printer.Connection".<br/> |
| stringType | Zeichenfolge | Wird nicht verwendet.<br/>                                                                                                     |
| value      | Zeichenfolge | Die lokalisierte Zeichenfolge.<br/>                                                                                         |



## <a name="remarks"></a>Hinweise

Sie können auf die Zeichenfolgen eines beliebigen Manifesttyps verweisen, der das Nachrichtenattribut enthält. Verwenden Sie $(string), um auf eine Zeichenfolge mit dem StringType "string" und der ID "Printer.Connection" zu verweisen. Printer.Connection) als Wert des Nachrichtenattributs.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





