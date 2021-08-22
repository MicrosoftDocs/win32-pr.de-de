---
title: Komplexer XmlTypeListType-Typ
description: Definiert listenausgabetypen, die der Dienst verwendet, um zu bestimmen, wie ein Eingabedatentyp gerendert wird.
ms.assetid: d90b32cc-a0b5-44d1-8083-781aa5e10783
keywords:
- Komplexer XmlTypeListType-Typ EventLog
topic_type:
- apiref
api_name:
- XmlTypeListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e30ca23a0e4ab0168ff7479a5246acfb4b34e3a43bc62886d988d5f54549672b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119620320"
---
# <a name="xmltypelisttype-complex-type"></a>Komplexer XmlTypeListType-Typ

Definiert listenausgabetypen, die der Dienst verwendet, um zu bestimmen, wie ein Eingabedatentyp gerendert wird.

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



| Element                                                                | Typ | Beschreibung                      |
|------------------------------------------------------------------------|------|----------------------------------|
| [**Xmltype**](eventmanifestschema-xmltype-xmltypelisttype-element.md) |      | Definiert einen XML-Typ. <br/> |



## <a name="attributes"></a>Attributes



| Name   | Typ                                                              | Beschreibung                                                                                                                                                                                                                                                |
|--------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name   | **QName**                                                         | Der Name des Ausgabetyps.<br/>                                                                                                                                                                                                                    |
| Symbol | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Das Symbol, das verwendet werden soll, um auf den Ausgabetyp in Ihrer Anwendung zu verweisen. Der [**Nachrichtencompiler (MC.exe)**](message-compiler--mc-exe-.md) verwendet das -Symbol, um eine Konstante für den Ausgabetyp in der Headerdatei zu erstellen, die der Compiler generiert.<br/> |
| value  | Zeichenfolge                                                            | Ein ganzzahliger Wert, der den Ausgabetyp in der Liste der von Ihnen definierten Ausgabetypen eindeutig identifiziert.<br/>                                                                                                                                          |



## <a name="remarks"></a>Hinweise

Die IncludeWinmeta.xml datei, die im Windows SDK enthalten ist, enthält eine Liste \\ \\ vordefinierter Ausgabetypen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





