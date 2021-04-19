---
title: XmlType (xmltypelisttype)-Element
description: Definiert einen XML-Typ.
ms.assetid: 4443963f-f47a-4371-87d8-58f508ba15d6
keywords:
- XmlType-Element EventLog
topic_type:
- apiref
api_name:
- xmlType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5aa37214c5efc0dee9e788ad10ed2f437e3df19f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342207"
---
# <a name="xmltype-xmltypelisttype-element"></a>XmlType (xmltypelisttype)-Element

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

Das **XmlType** -Element wird durch den komplexen [**xmltypelisttype**](eventmanifestschema-xmltypelisttype-complextype.md) -Typ definiert.

## <a name="attributes"></a>Attributes



| Name   | type      | BESCHREIBUNG                                                                                                                                                                                                                                                |
|--------|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name   | **QName** | Der Name des Ausgabe Typs.<br/>                                                                                                                                                                                                                    |
| Symbol | Zeichenfolge    | Das Symbol, mit dem auf den Ausgabetyp in der Anwendung verwiesen werden soll. Der [**Nachrichten Compiler (MC.exe)**](message-compiler--mc-exe-.md) verwendet das Symbol, um eine Konstante für den Ausgabetyp in der vom Compiler generierten Header Datei zu erstellen.<br/> |
| value  | Zeichenfolge    | Ein ganzzahliger Wert, der den Ausgabetyp in der Liste der von Ihnen definierten Ausgabetypen eindeutig identifiziert.<br/>                                                                                                                                          |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Übergeordnetes Element**
</dt> <dt>

[**xmltypes (typelisttype)**](eventmanifestschema-xmltypes-typelisttype-element.md)
</dt> </dl>

 

 





