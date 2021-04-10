---
title: String (stringtabletype)-Element
description: Definiert eine lokalisierte Zeichenfolge.
ms.assetid: 845476a9-bcf4-4821-824c-06c9a9f64649
keywords:
- Zeichen folgen Element-Ereignisprotokoll
topic_type:
- apiref
api_name:
- string
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c46fc43366d6472e8047b529d847eefd5369c263
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956655"
---
# <a name="string-stringtabletype-element"></a>String (stringtabletype)-Element

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

Das **String** -Element wird durch den komplexen [**stringtabletype**](eventmanifestschema-stringtabletype-complextype.md) -Typ definiert.

## <a name="attributes"></a>Attributes



| Name       | type   | BESCHREIBUNG                                                                           |
|------------|--------|---------------------------------------------------------------------------------------|
| id         | Zeichenfolge | Ein Bezeichner, der die Zeichenfolge innerhalb der Zeichen folgen Tabelle eindeutig identifiziert.<br/> |
| StringType | Zeichenfolge | Nicht verwendet.<br/>                                                                  |
| value      | Zeichenfolge | Die lokalisierte Zeichenfolge.<br/>                                                      |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Übergeordnetes Element**
</dt> <dt>

[**STRINGTABLE (localizationtype)**](eventmanifestschema-stringtable-localizationtype-element.md)
</dt> </dl>

 

 





