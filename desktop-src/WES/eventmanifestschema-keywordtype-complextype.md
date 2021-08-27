---
title: Komplexer KeywordType-Typ
description: Definiert ein Schlüsselwort, das eine Kategorie von Ereignissen identifiziert. | Komplexer KeywordType-Typ
ms.assetid: 6bd41d4a-1d55-4cce-a1f8-136f749fde2a
keywords:
- Komplexer KeywordType-Typ EventLog
topic_type:
- apiref
api_name:
- KeywordType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3d444c39796f741cd800fb393527e5adca6e50cef05de0c55c1def2bb40142a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124380"
---
# <a name="keywordtype-complex-type"></a>Komplexer KeywordType-Typ

Definiert ein Schlüsselwort, das eine Kategorie von Ereignissen identifiziert. Ein Schlüsselwort ist ein Tag, das Sie an ein Ereignis anfügen, um Ereignisse basierend auf ihrer Verwendung zu gruppieren.

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



| Name    | type                                                              | Beschreibung                                                                                                                                                                                                                                                                                                            |
|---------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| mask    | [**HexInt64Type**](eventmanifestschema-hex64type-simpletype.md)  | Eine Bitmaske, die nur ein einzelnes Bit aufweisen darf. Das Bit stellt eine Kategorie von Ereignissen dar (z. B. Lesen von Ereignissen oder Schreiben von Ereignissen). Sie können Bitwerte im Bereich von 0x0000000000000001 bis 0x0000800000000000 (Bits 0 bis 47) angeben.<br/>                                                         |
| message | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | Der lokalisierte Anzeigename für das Schlüsselwort. Die Meldungszeichenfolge verweist auf eine lokalisierte Zeichenfolge im [**StringTable-Abschnitt**](eventmanifestschema-stringtable-resources-element.md) des Manifests.<br/>                                                                                                       |
| name    | **QName**                                                         | Der Name des Schlüsselworts. Der Name muss innerhalb der Liste der Schlüsselwörter, die der Anbieter definiert, eindeutig sein.<br/>                                                                                                                                                                                                     |
| Symbol  | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Das Symbol, das verwendet werden soll, um auf das Schlüsselwort in Ihrer Anwendung zu verweisen. Der [**Nachrichtencompiler (MC.exe)**](message-compiler--mc-exe-.md) verwendet das Symbol, um eine Konstante für das Schlüsselwort in der Headerdatei zu erstellen, die der Compiler generiert. Wenn Sie kein Symbol angeben, generiert der Compiler ein Symbol für Sie.<br/> |



## <a name="remarks"></a>Hinweise

Die Winmeta.xml-Datei, die im Windows SDK enthalten ist, enthält eine Liste mit Schlüsselwörtern. Diese Schlüsselwörter sind reserviert und sollten nicht verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





