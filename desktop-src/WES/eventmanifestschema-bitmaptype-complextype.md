---
title: Komplexer bitmaptype-Typ
description: Definiert eine Liste von Name-Wert-Zuordnungen zwischen Bitwerten und Zeichen folgen Werten.
ms.assetid: 65dc6a48-878c-415c-872c-41dc27691b7f
keywords:
- Bitmaptype komplexer Typ EventLog
topic_type:
- apiref
api_name:
- BitMapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ef3a48b102b9ab36ef492fcd38c4bb8b2560d5fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479215"
---
# <a name="bitmaptype-complex-type"></a>Komplexer bitmaptype-Typ

Definiert eine Liste von Name-Wert-Zuordnungen zwischen Bitwerten und Zeichen folgen Werten.

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



| Element                                                   | type                                                                       | BESCHREIBUNG                                                            |
|-----------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**bilden**](eventmanifestschema-map-bitmaptype-element.md) | [**Bitmapvaluetype**](eventmanifestschema-bitmapvaluetype-complextype.md) | Definiert die Zuordnung zwischen einem Bitwert und einem Zeichen folgen Wert.<br/> |



## <a name="attributes"></a>Attributes



| Name   | type                                                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                         |
|--------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name   | Zeichenfolge                                                            | Der Name der Bitmap.<br/>                                                                                                                                                                                                                                                                                  |
| Symbol | [**Csymboltype**](eventmanifestschema-csymboltype-simpletype.md) | Das Symbol, das verwendet werden soll, um auf die Zuordnungen in der Anwendung zu verweisen. Der [**Nachrichten Compiler (MC.exe)**](message-compiler--mc-exe-.md) verwendet das Symbol, um eine Konstante für die Zuordnung in der vom Compiler generierten Header Datei zu erstellen. Wenn Sie kein Symbol angeben, generiert der Compiler einen für Sie.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





