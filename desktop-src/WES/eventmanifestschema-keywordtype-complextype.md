---
title: Komplexer keywordtype-Typ
description: Definiert ein Schlüsselwort, das eine Kategorie von Ereignissen bezeichnet. | Komplexer keywordtype-Typ
ms.assetid: 6bd41d4a-1d55-4cce-a1f8-136f749fde2a
keywords:
- Keywordtype Complex-Typ EventLog
topic_type:
- apiref
api_name:
- KeywordType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c41a9ad4b1fde0a741a022eb6cfd20823643eeef
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106351878"
---
# <a name="keywordtype-complex-type"></a>Komplexer keywordtype-Typ

Definiert ein Schlüsselwort, das eine Kategorie von Ereignissen bezeichnet. Ein Schlüsselwort ist ein Tag, das Sie an ein Ereignis anfügen, um Ereignisse auf der Grundlage ihrer Verwendung zu gruppieren.

``` syntax
<xs:complexType name="KeywordType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="xs:string"
        >
            <xs:attribute name="name"
                type="QName"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
            <xs:attribute name="mask"
                type="HexInt64Type"
                use="required"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="optional"
             />
            <xs:anyAttribute
                processContents="lax"
                namespace="##other"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Attributes



| Name    | type                                                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                            |
|---------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| mask    | [**HexInt64Type**](eventmanifestschema-hex64type-simpletype.md)  | Eine Bitmaske, für die nur ein einzelnes Bit festgelegt werden muss. Das Bit stellt eine Kategorie von Ereignissen dar (z. b. Lese-oder Schreib Ereignisse). Sie können Bitwerte im Bereich von 0x0000000000000001 bis 0x0000800000000000 (Bits 0 bis 47) angeben.<br/>                                                         |
| message | [**"Strauch"**](eventmanifestschema-strtableref-simpletype.md) | Der lokalisierte Anzeige Name für das Schlüsselwort. Die Meldungs Zeichenfolge verweist auf eine lokalisierte Zeichenfolge im [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) -Abschnitt des Manifests.<br/>                                                                                                       |
| name    | **QName**                                                         | Der Name des Schlüssel Worts. Der Name muss innerhalb der Liste der Schlüsselwörter, die vom Anbieter definiert werden, eindeutig sein.<br/>                                                                                                                                                                                                     |
| Symbol  | [**Csymboltype**](eventmanifestschema-csymboltype-simpletype.md) | Das Symbol, das verwendet wird, um auf das Schlüsselwort in Ihrer Anwendung zu verweisen. Der [**Nachrichten Compiler (MC.exe)**](message-compiler--mc-exe-.md) verwendet das Symbol, um eine Konstante für das Schlüsselwort in der vom Compiler generierten Header Datei zu erstellen. Wenn Sie kein Symbol angeben, generiert der Compiler einen für Sie.<br/> |



## <a name="remarks"></a>Bemerkungen

Die Winmeta.xml-Datei, die in der Windows SDK enthalten ist, enthält eine Liste von Schlüsselwörtern. Diese Schlüsselwörter sind reserviert und sollten nicht verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





