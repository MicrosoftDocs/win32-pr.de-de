---
title: Resources (localizationtype)-Element
description: Definiert eine Gruppe von Zeichen folgen Tabellen, die die lokalisierten Zeichen folgen enthalten, auf die im Manifest verwiesen wird.
ms.assetid: b984894a-0ae8-49be-af93-3acdcce53ee9
keywords:
- Ressourcen Element-Ereignisprotokoll
topic_type:
- apiref
api_name:
- resources
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 55bdfe504da08c754c18b790e282eba6787c3ee3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341580"
---
# <a name="resources-localizationtype-element"></a>Resources (localizationtype)-Element

Definiert eine Gruppe von Zeichen folgen Tabellen, die die lokalisierten Zeichen folgen enthalten, auf die im Manifest verwiesen wird.

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

Das **Resources** -Element wird durch den komplexen Typ [**localizationtype**](eventmanifestschema-localizationtype-complextype.md) definiert.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                  | type                                                                       | BESCHREIBUNG                                                                             |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) | [**Stringtabletype**](eventmanifestschema-stringtabletype-complextype.md) | Definiert eine Liste lokalisierter Zeichen folgen, auf die Sie im Manifest verweisen können.<br/> |



## <a name="attributes"></a>Attributes



| Name    | type   | BESCHREIBUNG                                                                                                                                            |
|---------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| culture | Zeichenfolge | Ein Sprachen Name, der die Kultur der lokalisierten Zeichen folgen in der Zeichen folgen Tabelle angibt. Beispiel: "en-US" für Englisch (USA).<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Übergeordnetes Element**
</dt> <dt>

[**Lokalisierung (instrumentationmanifest)**](eventmanifestschema-localization-instrumentationmanifest-element.md)
</dt> </dl>

 

 





