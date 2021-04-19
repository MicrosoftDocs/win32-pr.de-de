---
title: Komplexer localizationtype-Typ
description: Definiert eine Gruppe lokalisierter Ressourcen, auf die im Manifest verwiesen wird. | Komplexer localizationtype-Typ
ms.assetid: fecab4e0-7136-4b13-8c24-bebbad0812e6
keywords:
- EventLog-Typ des komplexen lokalisierationstyp
topic_type:
- apiref
api_name:
- LocalizationType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cbb6911ea606ea30d8e656f20b4c566d4f6d0e08
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106370370"
---
# <a name="localizationtype-complex-type"></a>Komplexer localizationtype-Typ

Definiert eine Gruppe lokalisierter Ressourcen, auf die im Manifest verwiesen wird.

``` syntax
<xs:complexType name="LocalizationType">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
        <xs:element name="resources">
            <xs:complexType>
                <xs:choice
                    minOccurs="0"
                    maxOccurs="unbounded"
                >
                    <xs:element name="stringTable"
                        type="StringTableType"
                     />
                </xs:choice>
                <xs:attribute name="culture"
                    type="string"
                    use="required"
                 />
                <xs:anyAttribute
                    processContents="lax"
                    namespace="##other"
                 />
            </xs:complexType>
        </xs:element>
        <xs:any
            processContents="lax"
            minOccurs="0"
            namespace="##other"
         />
    </xs:choice>
    <xs:attribute name="fallbackCulture"
        type="string"
        default="en-us"
        use="optional"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                         | type                                                                       | BESCHREIBUNG                                                                                                         |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**verfügt**](eventmanifestschema-resources-localizationtype-element.md)     |                                                                            | Definiert eine Gruppe von Zeichen folgen Tabellen, die die lokalisierten Zeichen folgen enthalten, auf die im Manifest verwiesen wird.<br/> |
| [**STRINGTABLE**](eventmanifestschema-stringtable-localizationtype-element.md) | [**Stringtabletype**](eventmanifestschema-stringtabletype-complextype.md) | Definiert eine Liste lokalisierter Zeichen folgen, auf die Sie im Manifest verweisen können.<br/>                             |



## <a name="attributes"></a>Attributes



| Name            | type   | BESCHREIBUNG                                                                                                                                            |
|-----------------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| culture         | Zeichenfolge | Ein Sprachen Name, der die Kultur der lokalisierten Zeichen folgen in der Zeichen folgen Tabelle angibt. Beispiel: "en-US" für Englisch (USA).<br/> |
| fallbackCulture | Zeichenfolge | Nicht verwendet.<br/>                                                                                                                                   |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





