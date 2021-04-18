---
title: Komplexer stringtabletype-Typ
description: Definiert eine Liste lokalisierter Zeichen folgen, auf die Sie im Manifest verweisen können. | Komplexer stringtabletype-Typ
ms.assetid: 47a59ff7-aaf6-4200-805b-0a8b5f57f101
keywords:
- Stringtabletype Complex-Typ EventLog
topic_type:
- apiref
api_name:
- StringTableType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a9964c51524f7401afdfdd8a2da10cf43326bcae
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106365266"
---
# <a name="stringtabletype-complex-type"></a>Komplexer stringtabletype-Typ

Definiert eine Liste lokalisierter Zeichen folgen, auf die Sie im Manifest verweisen können.

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



| Element                                                              | type | BESCHREIBUNG                            |
|----------------------------------------------------------------------|------|----------------------------------------|
| [**Zeichenfolge**](eventmanifestschema-string-stringtabletype-element.md) |      | Definiert eine lokalisierte Zeichenfolge.<br/> |



## <a name="attributes"></a>Attributes



| Name       | type   | BESCHREIBUNG                                                                                                              |
|------------|--------|--------------------------------------------------------------------------------------------------------------------------|
| id         | Zeichenfolge | Ein Bezeichner, der die Zeichenfolge innerhalb der Zeichen folgen Tabelle eindeutig identifiziert. Beispiel: "Printer. Connection".<br/> |
| StringType | Zeichenfolge | Nicht verwendet.<br/>                                                                                                     |
| value      | Zeichenfolge | Die lokalisierte Zeichenfolge.<br/>                                                                                         |



## <a name="remarks"></a>Bemerkungen

Sie können auf die Zeichen Folgen eines beliebigen manifestressyps verweisen, der das Message-Attribut enthält. Um auf eine Zeichenfolge mit dem StringType-Zeichensatz "String" und der ID "Printer. Connection" zu verweisen, verwenden Sie $ (String. Printer. Connection) als Wert für das Message-Attribut.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





