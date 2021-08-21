---
title: xmlType (XmlTypeListType) -Element
description: Definiert einen XML-Typ.
ms.assetid: 4443963f-f47a-4371-87d8-58f508ba15d6
keywords:
- xmlType-Element EventLog
topic_type:
- apiref
api_name:
- xmlType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 119ebe7f09f86aa46d9e80380670309fe8734fa818b48049d5dffc29e6a2ebb0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863280"
---
# <a name="xmltype-xmltypelisttype-element"></a>xmlType (XmlTypeListType) -Element

Definiert einen XML-Typ.

``` syntax
<xs:element name="xmlType">
    <xs:complexType>
        <xs:complexContent>
            <xs:extension
                base="XmlType"
            >
                <xs:attribute name="name"
                    type="QName"
                    use="required"
                 />
                <xs:attribute name="value"
                    type="string"
                    use="required"
                 />
                <xs:attribute name="symbol"
                    type="string"
                    use="required"
                 />
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

Das **xmlType-Element** wird durch den komplexen [**XmlTypeListType-Typ**](eventmanifestschema-xmltypelisttype-complextype.md) definiert.

## <a name="attributes"></a>Attributes



| Name   | type      | BESCHREIBUNG                                                                                                                                                                                                                                                |
|--------|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name   | **QName** | Der Name des Ausgabetyps.<br/>                                                                                                                                                                                                                    |
| Symbol | Zeichenfolge    | Das Symbol, das verwendet werden soll, um auf den Ausgabetyp in Ihrer Anwendung zu verweisen. Der [**Nachrichtencompiler (MC.exe)**](message-compiler--mc-exe-.md) verwendet das -Symbol, um eine Konstante für den Ausgabetyp in der Headerdatei zu erstellen, die der Compiler generiert.<br/> |
| value  | Zeichenfolge    | Ein ganzzahliger Wert, der den Ausgabetyp in der Liste der von Ihnen definierten Ausgabetypen eindeutig identifiziert.<br/>                                                                                                                                          |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Übergeordnetes Element**
</dt> <dt>

[**xmlTypes (TypeListType)**](eventmanifestschema-xmltypes-typelisttype-element.md)
</dt> </dl>

 

 





