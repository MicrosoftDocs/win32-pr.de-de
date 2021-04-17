---
title: Komplexer Typ von patternmaptype
description: Nicht verwendet. Definiert eine Zuordnung zwischen zwei regulären Ausdrücken. Ein Ausdruck wird verwendet, um nach einer übereinstimmenden Zeichenfolge in der Meldungs Zeichenfolge zu suchen, und die andere wird verwendet, um die Zeichenfolge zu ändern
ms.assetid: 184b6aeb-a554-4a92-b19e-1849c711d33b
keywords:
- "\"Patternmaptype Complex Type Event Log\""
topic_type:
- apiref
api_name:
- PatternMapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e39ca30520f4f595bfc73a4d80b9bc191793859a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477391"
---
# <a name="patternmaptype-complex-type"></a>Komplexer Typ von patternmaptype

Nicht verwendet. Definiert eine Zuordnung zwischen zwei regulären Ausdrücken. Ein Ausdruck wird verwendet, um nach einer übereinstimmenden Zeichenfolge in der Meldungs Zeichenfolge zu suchen, und die andere wird verwendet, um die Zeichenfolge zu ändern

``` syntax
<xs:complexType name="PatternMapType">
    <xs:sequence>
        <xs:element name="map"
            type="PatternMapValueType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="QName"
        use="required"
     />
    <xs:attribute name="format"
        type="anyURI"
        use="required"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                       | type                                                                               | BESCHREIBUNG                                                                                                   |
|---------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [**bilden**](eventmanifestschema-map-patternmaptype-element.md) | [**Patternmapvaluetype**](eventmanifestschema-patternmapvaluetype-complextype.md) | Definiert die regulären Ausdrücke, mit denen eine übereinstimmende Zeichenfolge in der Meldungs Zeichenfolge gesucht und geändert wird.<br/> |



## <a name="attributes"></a>Attributes



| Name   | type                                                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                         |
|--------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| format | anyURI                                                            | Die zu verwendende Engine für reguläre Ausdrücke.<br/>                                                                                                                                                                                                                                                                    |
| name   | **QName**                                                         | Der Name der Musterzuordnung. Verwenden Sie den Namen in einem Datenelement, um auf die Zuordnungen zu verweisen.<br/>                                                                                                                                                                                                                   |
| Symbol | [**Csymboltype**](eventmanifestschema-csymboltype-simpletype.md) | Das Symbol, das verwendet werden soll, um auf die Zuordnungen in der Anwendung zu verweisen. Der [**Nachrichten Compiler (MC.exe)**](message-compiler--mc-exe-.md) verwendet das Symbol, um eine Konstante für die Zuordnung in der vom Compiler generierten Header Datei zu erstellen. Wenn Sie kein Symbol angeben, generiert der Compiler einen für Sie.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





