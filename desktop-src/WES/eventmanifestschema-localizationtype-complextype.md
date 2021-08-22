---
title: LocalizationType Complex Type
description: Definiert eine Gruppe lokalisierter Ressourcen, auf die Sie im Manifest verweisen. | LocalizationType Complex Type
ms.assetid: fecab4e0-7136-4b13-8c24-bebbad0812e6
keywords:
- LocalizationType complex type EventLog
topic_type:
- apiref
api_name:
- LocalizationType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 09a596ff981944943c193fb158f14aa04eafb0b0b3d4df660d2034c5b5d281be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055948"
---
# <a name="localizationtype-complex-type"></a>LocalizationType Complex Type

Definiert eine Gruppe lokalisierter Ressourcen, auf die Sie im Manifest verweisen.

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



| Element                                                                         | Typ                                                                       | Beschreibung                                                                                                         |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**Ressourcen**](eventmanifestschema-resources-localizationtype-element.md)     |                                                                            | Definiert eine Gruppe von Zeichenfolgentabellen, die die lokalisierten Zeichenfolgen enthalten, auf die Sie im Manifest verweisen.<br/> |
| [**Stringtable**](eventmanifestschema-stringtable-localizationtype-element.md) | [**StringTableType**](eventmanifestschema-stringtabletype-complextype.md) | Definiert eine Liste lokalisierter Zeichenfolgen, auf die Sie im Manifest verweisen können.<br/>                             |



## <a name="attributes"></a>Attributes



| Name            | Typ   | Beschreibung                                                                                                                                            |
|-----------------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kultur         | Zeichenfolge | Ein Sprachname, der die Kultur der lokalisierten Zeichenfolgen in der Zeichenfolgentabelle identifiziert. Beispiel: "en-US" für Englisch (USA).<br/> |
| fallbackCulture | Zeichenfolge | Wird nicht verwendet.<br/>                                                                                                                                   |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





