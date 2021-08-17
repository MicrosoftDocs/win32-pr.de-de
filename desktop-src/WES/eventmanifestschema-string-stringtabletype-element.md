---
title: string (StringTableType)-Element
description: Definiert eine lokalisierte Zeichenfolge.
ms.assetid: 845476a9-bcf4-4821-824c-06c9a9f64649
keywords:
- String-Element EventLog
topic_type:
- apiref
api_name:
- string
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 82eae0fa7007790995617b2c26bc5aff2bca720fb689b9ac468ef551d3400e05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136173"
---
# <a name="string-stringtabletype-element"></a>string (StringTableType)-Element

Definiert eine lokalisierte Zeichenfolge.

``` syntax
<xs:element name="string">
    <xs:complexType>
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
```

Das **Zeichenfolgenelement** wird vom komplexen [**StringTableType-Typ**](eventmanifestschema-stringtabletype-complextype.md) definiert.

## <a name="attributes"></a>Attributes



| Name       | type   | BESCHREIBUNG                                                                           |
|------------|--------|---------------------------------------------------------------------------------------|
| id         | Zeichenfolge | Ein Bezeichner, der die Zeichenfolge innerhalb der Zeichenfolgentabelle eindeutig identifiziert.<br/> |
| stringType | Zeichenfolge | Wird nicht verwendet.<br/>                                                                  |
| value      | Zeichenfolge | Die lokalisierte Zeichenfolge.<br/>                                                      |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Übergeordnetes Element**
</dt> <dt>

[**stringTable (LocalizationType)**](eventmanifestschema-stringtable-localizationtype-element.md)
</dt> </dl>

 

 





