---
title: resources (LocalizationType)-Element
description: Definiert eine Gruppe von Zeichenfolgentabellen, die die lokalisierten Zeichenfolgen enthalten, auf die Sie im Manifest verweisen.
ms.assetid: b984894a-0ae8-49be-af93-3acdcce53ee9
keywords:
- resources-Element EventLog
topic_type:
- apiref
api_name:
- resources
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3075b2b1741079f80c34e5acf9783b13b74b6973c1d16f2cd323890bcea5d0d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118120577"
---
# <a name="resources-localizationtype-element"></a>resources (LocalizationType)-Element

Definiert eine Gruppe von Zeichenfolgentabellen, die die lokalisierten Zeichenfolgen enthalten, auf die Sie im Manifest verweisen.

``` syntax
<xs:element name="resources">
    <xs:complexType>
        <xs:choice
            minOccurs="0"
            maxOccurs="unbounded"
        >
            <xs:element name="stringTable"
                type="StringTableType"
             />
            <xs:any
                processContents="lax"
                minOccurs="0"
                namespace="##other"
             />
        </xs:choice>
        <xs:attribute name="culture"
            type="string"
            default="##fallback"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

Das **resources-Element** wird durch den komplexen [**LocalizationType-Typ**](eventmanifestschema-localizationtype-complextype.md) definiert.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                  | type                                                                       | Beschreibung                                                                             |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**Stringtable**](eventmanifestschema-stringtable-resources-element.md) | [**StringTableType**](eventmanifestschema-stringtabletype-complextype.md) | Definiert eine Liste lokalisierter Zeichenfolgen, auf die Sie in Ihrem Manifest verweisen können.<br/> |



## <a name="attributes"></a>Attributes



| Name    | type   | Beschreibung                                                                                                                                            |
|---------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kultur | Zeichenfolge | Ein Sprachname, der die Kultur der lokalisierten Zeichenfolgen in der Zeichenfolgentabelle identifiziert. Beispiel: "en-US" für Englisch (USA).<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Übergeordnetes Element**
</dt> <dt>

[**Lokalisierung (instrumentationManifest)**](eventmanifestschema-localization-instrumentationmanifest-element.md)
</dt> </dl>

 

 





