---
title: Komplexer BitMapValueType-Typ
description: Definiert die Zuordnung zwischen einem Bitwert und einem Zeichenfolgenwert. | Komplexer BitMapValueType-Typ
ms.assetid: 2ef9ed89-83cf-4c47-9c6c-64459b6d7198
keywords:
- Komplexer BitMapValueType-Typ EventLog
topic_type:
- apiref
api_name:
- BitMapValueType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6d5f1b254ad4a833c1523f5a139224fc1fed508d4530a056ffdb0f111db5769e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032350"
---
# <a name="bitmapvaluetype-complex-type"></a>Komplexer BitMapValueType-Typ

Definiert die Zuordnung zwischen einem Bitwert und einem Zeichenfolgenwert.

``` syntax
<xs:complexType name="BitMapValueType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="value"
                type="HexInt32Type"
                use="required"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Attributes



| Name    | type                                                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                    |
|---------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| message | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | Der lokalisierte Zeichenfolgenwert, dem der Bitwert zugeordnet wird. Die Meldungszeichenfolge verweist auf eine lokalisierte Zeichenfolge im [**StringTable-Abschnitt**](eventmanifestschema-stringtable-resources-element.md) des Manifests. <br/>                                                                                  |
| Symbol  | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Das Symbol, das verwendet werden soll, um auf die Karte in Ihrer Anwendung zu verweisen. Der [**Nachrichtencompiler (MC.exe)**](message-compiler--mc-exe-.md) verwendet das Symbol, um eine Konstante für die Zuordnung in der Headerdatei zu erstellen, die der Compiler generiert. Wenn Sie kein Symbol angeben, generiert der Compiler ein Symbol für Sie.<br/> |
| value   | [**HexInt32Type**](eventmanifestschema-hex32type-simpletype.md)  | Der Bitwert, der dem Zeichenfolgenwert zugeordnet werden soll. Sie müssen eine Hexadezimalzahl angeben, für die ein einzelnes Bit festgelegt ist.<br/>                                                                                                                                                                                          |



## <a name="remarks"></a>Hinweise

Karten einen Hexadezimalwert (der Zahl muss 0x vorangestellt werden) mit einem einzelnen Bit, das auf einen Namen festgelegt ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





