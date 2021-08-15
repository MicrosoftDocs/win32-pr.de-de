---
title: Komplexer LevelType-Typ
description: Definiert einen Schweregrad, der die Ausführlichkeit der protokollierten Ereignisse bestimmt.
ms.assetid: c71aedef-7c43-4343-9d6d-94eb45da49b9
keywords:
- Komplexer LevelType-Typ EventLog
topic_type:
- apiref
api_name:
- LevelType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b80e034f6b77f869207ecb785edbb935841eed2dba6bde73ad88c441dabf15cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055938"
---
# <a name="leveltype-complex-type"></a>Komplexer LevelType-Typ

Definiert einen Schweregrad, der die Ausführlichkeit der protokollierten Ereignisse bestimmt.

``` syntax
<xs:complexType name="LevelType"
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
            <xs:attribute name="value"
                type="UInt8Type"
                use="required"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Attributes



| Name    | type                                                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                        |
|---------|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| message | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | Der lokalisierte Anzeigename für die Ebene. Die Meldungszeichenfolge verweist auf eine lokalisierte Zeichenfolge im [**StringTable-Abschnitt**](eventmanifestschema-stringtable-resources-element.md) des Manifests. <br/>                                                                                                    |
| name    | **QName**                                                         | Der Name, der dieser Ebene zugewiesen werden soll. Dieser Name muss innerhalb des Bereichs des Anbieters eindeutig sein.<br/>                                                                                                                                                                                                            |
| Symbol  | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Das Symbol, das verwendet werden soll, um auf die Ebene in Ihrer Anwendung zu verweisen. Der [**Nachrichtencompiler (MC.exe)**](message-compiler--mc-exe-.md) verwendet das -Symbol, um eine Konstante für die Ebene in der Headerdatei zu erstellen, die der Compiler generiert. Wenn Sie kein Symbol angeben, generiert der Compiler ein Symbol für Sie.<br/> |
| value   | [**UInt8Type**](eventmanifestschema-hexint8type-simpletype.md)   | Der Wert der Ebene. Sie können Werte im Bereich von 16 bis 255 angeben. Vordefinierte Werte finden Sie unter Hinweise.<br/>                                                                                                                                                                                               |



## <a name="remarks"></a>Hinweise

Im Folgenden finden Sie die vordefinierten Levelwerte, die Sie verwenden können. Diese Werte werden in der Winmeta.xml definiert, die im Windows SDK enthalten ist.



| Name              | Wert | Symbol                    | BESCHREIBUNG                                                             |
|-------------------|-------|---------------------------|-------------------------------------------------------------------------|
| win:Critical      | 1     | WINEVENT \_ LEVEL \_ CRITICAL | Identifiziert ein ungewöhnliches Beendigungs- oder Beendigungsereignis.<br/>            |
| win:Error         | 2     | WINEVENT \_ LEVEL \_ ERROR    | Identifiziert ein schwerwiegendes Fehlerereignis.<br/>                             |
| win:Warning       | 3     | WINEVENT \_ LEVEL \_ WARNING  | Identifiziert ein Warnungsereignis, z. B. einen Zuordnungsfehler.<br/>    |
| win:Informational | 4     | INFORMATIONEN ZUM \_ \_ WINEVENT-LEVEL     | Identifiziert ein Nicht-Fehlerereignis, z. B. ein Einstiegs- oder Beendigungsereignis.<br/> |
| win:Verbose       | 5     | WINEVENT \_ LEVEL \_ VERBOSE  | Identifiziert ein detailliertes Ablaufverfolgungsereignis.<br/>                           |



 

Höhere Zahlen implizieren, dass Sie auch niedrigere Ebenen erhalten. Wenn Sie beispielsweise win:Warning angeben, erhalten Sie alle Warnungs-, Fehler- und kritischen Ereignisse.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





