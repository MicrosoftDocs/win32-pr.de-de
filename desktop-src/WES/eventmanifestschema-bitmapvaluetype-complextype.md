---
title: Komplexer bitmapvaluetype-Typ
description: Definiert die Zuordnung zwischen einem Bitwert und einem Zeichen folgen Wert. | Komplexer bitmapvaluetype-Typ
ms.assetid: 2ef9ed89-83cf-4c47-9c6c-64459b6d7198
keywords:
- Bitmapvaluetype komplexer Typ EventLog
topic_type:
- apiref
api_name:
- BitMapValueType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f2da7e0576579b0f0c509de7a8318e46e5dd955d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103961398"
---
# <a name="bitmapvaluetype-complex-type"></a>Komplexer bitmapvaluetype-Typ

Definiert die Zuordnung zwischen einem Bitwert und einem Zeichen folgen Wert.

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
| message | [**"Strauch"**](eventmanifestschema-strtableref-simpletype.md) | Der lokalisierte Zeichen folgen Wert, dem der Bitwert zugeordnet ist. Die Meldungs Zeichenfolge verweist auf eine lokalisierte Zeichenfolge im [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) -Abschnitt des Manifests. <br/>                                                                                  |
| Symbol  | [**Csymboltype**](eventmanifestschema-csymboltype-simpletype.md) | Das Symbol, das für den Verweis auf die Karte in der Anwendung verwendet werden soll. Der [**Nachrichten Compiler (MC.exe)**](message-compiler--mc-exe-.md) verwendet das Symbol, um eine Konstante für die Zuordnung in der vom Compiler generierten Header Datei zu erstellen. Wenn Sie kein Symbol angeben, generiert der Compiler einen für Sie.<br/> |
| value   | [**HexInt32Type**](eventmanifestschema-hex32type-simpletype.md)  | Der Bitwert, der dem Zeichen folgen Wert zugeordnet werden soll. Sie müssen eine hexadezimale Zahl angeben, für die ein einzelnes Bit festgelegt ist.<br/>                                                                                                                                                                                          |



## <a name="remarks"></a>Bemerkungen

Ordnet einen hexadezimalen Wert zu (die Zahl muss 0x vorangestellt sein), wobei ein einzelnes Bit auf einen Namen festgelegt ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





