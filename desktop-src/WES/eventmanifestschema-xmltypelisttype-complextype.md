---
title: Komplexer xmltypelisttype-Typ
description: Definiert einen Listen Ausgabetyp, den der Dienst verwendet, um zu bestimmen, wie ein Eingabe Datentyp dargestellt werden soll.
ms.assetid: d90b32cc-a0b5-44d1-8083-781aa5e10783
keywords:
- Xmltypelisttype Complex-Typ EventLog
topic_type:
- apiref
api_name:
- XmlTypeListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 388161572ec9c84ed46d5b40987df5fb8d1ed077
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340797"
---
# <a name="xmltypelisttype-complex-type"></a>Komplexer xmltypelisttype-Typ

Definiert einen Listen Ausgabetyp, den der Dienst verwendet, um zu bestimmen, wie ein Eingabe Datentyp dargestellt werden soll.

``` syntax
<xs:complexType name="XmlTypeListType">
    <xs:sequence>
        <xs:element name="xmlType"
            minOccurs="0"
            maxOccurs="unbounded"
        >
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
                            type="CSymbolType"
                            use="required"
                         />
                    </xs:extension>
                </xs:complexContent>
            </xs:complexType>
        </xs:element>
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                | type | BESCHREIBUNG                      |
|------------------------------------------------------------------------|------|----------------------------------|
| [**xmlType**](eventmanifestschema-xmltype-xmltypelisttype-element.md) |      | Definiert einen XML-Typ. <br/> |



## <a name="attributes"></a>Attributes



| Name   | type                                                              | BESCHREIBUNG                                                                                                                                                                                                                                                |
|--------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name   | **QName**                                                         | Der Name des Ausgabe Typs.<br/>                                                                                                                                                                                                                    |
| Symbol | [**Csymboltype**](eventmanifestschema-csymboltype-simpletype.md) | Das Symbol, mit dem auf den Ausgabetyp in der Anwendung verwiesen werden soll. Der [**Nachrichten Compiler (MC.exe)**](message-compiler--mc-exe-.md) verwendet das Symbol, um eine Konstante für den Ausgabetyp in der vom Compiler generierten Header Datei zu erstellen.<br/> |
| value  | Zeichenfolge                                                            | Ein ganzzahliger Wert, der den Ausgabetyp in der Liste der von Ihnen definierten Ausgabetypen eindeutig identifiziert.<br/>                                                                                                                                          |



## <a name="remarks"></a>Bemerkungen

Die \\ include \\Winmeta.xml-Datei, die im Windows SDK enthalten ist, enthält eine Liste vordefinierter Ausgabetypen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





