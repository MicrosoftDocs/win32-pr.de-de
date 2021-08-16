---
title: Komplexer PatternMapType-Typ
description: Wird nicht verwendet. Definiert eine Zuordnung zwischen zwei regulären Ausdrücken. Ein Ausdruck wird verwendet, um eine übereinstimmende Zeichenfolge in der Meldungszeichenfolge zu finden, und der andere wird verwendet, um die Zeichenfolge zu ändern, bevor der Dienst sie wieder in die Meldungszeichenfolge eingibt.
ms.assetid: 184b6aeb-a554-4a92-b19e-1849c711d33b
keywords:
- Komplexer PatternMapType-Typ EventLog
topic_type:
- apiref
api_name:
- PatternMapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d4ba0c404220023a124c082ea448cbb7bdcab192b611bf35a2afc90df82e9e63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136192"
---
# <a name="patternmaptype-complex-type"></a>Komplexer PatternMapType-Typ

Wird nicht verwendet. Definiert eine Zuordnung zwischen zwei regulären Ausdrücken. Ein Ausdruck wird verwendet, um eine übereinstimmende Zeichenfolge in der Meldungszeichenfolge zu finden, und der andere wird verwendet, um die Zeichenfolge zu ändern, bevor der Dienst sie wieder in die Meldungszeichenfolge eingibt.

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



| Element                                                       | type                                                                               | Beschreibung                                                                                                   |
|---------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [**Karte**](eventmanifestschema-map-patternmaptype-element.md) | [**PatternMapValueType**](eventmanifestschema-patternmapvaluetype-complextype.md) | Definiert die regulären Ausdrücke, die verwendet werden, um eine übereinstimmende Zeichenfolge in der Meldungszeichenfolge zu suchen und zu ändern.<br/> |



## <a name="attributes"></a>Attributes



| Name   | type                                                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                         |
|--------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| format | anyURI                                                            | Die zu verwendende Engine für reguläre Ausdrücke.<br/>                                                                                                                                                                                                                                                                    |
| name   | **QName**                                                         | Der Name der Musterzuordnung. Verwenden Sie den Namen in einem Datenelement, um auf die Zuordnungen zu verweisen.<br/>                                                                                                                                                                                                                   |
| Symbol | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Das Symbol, das verwendet werden soll, um auf die Zuordnungen in Ihrer Anwendung zu verweisen. Der [**Nachrichtencompiler (MC.exe)**](message-compiler--mc-exe-.md) verwendet das -Symbol, um eine Konstante für die Zuordnung in der Headerdatei zu erstellen, die der Compiler generiert. Wenn Sie kein Symbol angeben, generiert der Compiler ein Symbol für Sie.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





