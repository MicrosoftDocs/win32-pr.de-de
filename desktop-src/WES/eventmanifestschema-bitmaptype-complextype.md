---
title: Komplexer BitMapType-Typ
description: Definiert eine Liste von Name-Wert-Zuordnungen zwischen Bitwerten und Zeichenfolgenwerten.
ms.assetid: 65dc6a48-878c-415c-872c-41dc27691b7f
keywords:
- Komplexer BitMapType-Typ EventLog
topic_type:
- apiref
api_name:
- BitMapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c899718cd28e337bbc5d34301b7bb49446fde51f21db5b742e98dd95c5092c23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118590410"
---
# <a name="bitmaptype-complex-type"></a>Komplexer BitMapType-Typ

Definiert eine Liste von Name-Wert-Zuordnungen zwischen Bitwerten und Zeichenfolgenwerten.

``` syntax
<xs:complexType name="BitMapType">
    <xs:sequence>
        <xs:element name="map"
            type="BitMapValueType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="string"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                   | Typ                                                                       | BESCHREIBUNG                                                            |
|-----------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**Karte**](eventmanifestschema-map-bitmaptype-element.md) | [**BitMapValueType**](eventmanifestschema-bitmapvaluetype-complextype.md) | Definiert die Zuordnung zwischen einem Bitwert und einem Zeichenfolgenwert.<br/> |



## <a name="attributes"></a>Attributes



| Name   | Typ                                                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                         |
|--------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name   | Zeichenfolge                                                            | Der Name der Bitmap.<br/>                                                                                                                                                                                                                                                                                  |
| Symbol | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Das Symbol, das verwendet werden soll, um auf die Zuordnungen in Ihrer Anwendung zu verweisen. Der [**Nachrichtencompiler (MC.exe)**](message-compiler--mc-exe-.md) verwendet das -Symbol, um eine Konstante für die Zuordnung in der Headerdatei zu erstellen, die der Compiler generiert. Wenn Sie kein Symbol angeben, generiert der Compiler ein Symbol für Sie.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





