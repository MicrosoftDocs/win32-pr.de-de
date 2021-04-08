---
title: Komplexer leveltype-Typ
description: Definiert einen Schweregrad Wert, der die Ausführlichkeit der protokollierten Ereignisse bestimmt.
ms.assetid: c71aedef-7c43-4343-9d6d-94eb45da49b9
keywords:
- "\"Leveltype\"-Ereignisprotokoll Komplex"
topic_type:
- apiref
api_name:
- LevelType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 237b38890283769e9aac20c9b3a3703ff4b72d3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102934"
---
# <a name="leveltype-complex-type"></a>Komplexer leveltype-Typ

Definiert einen Schweregrad Wert, der die Ausführlichkeit der protokollierten Ereignisse bestimmt.

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
| message | [**"Strauch"**](eventmanifestschema-strtableref-simpletype.md) | Der lokalisierte Anzeige Name für die Ebene. Die Meldungs Zeichenfolge verweist auf eine lokalisierte Zeichenfolge im [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) -Abschnitt des Manifests. <br/>                                                                                                    |
| name    | **QName**                                                         | Der Name, der dieser Ebene zugewiesen werden soll. Dieser Name muss innerhalb des Bereichs des Anbieters eindeutig sein.<br/>                                                                                                                                                                                                            |
| Symbol  | [**Csymboltype**](eventmanifestschema-csymboltype-simpletype.md) | Das Symbol, das verwendet werden soll, um auf die Ebene in der Anwendung zu verweisen. Der [**Nachrichten Compiler (MC.exe)**](message-compiler--mc-exe-.md) verwendet das Symbol, um eine Konstante für die Ebene in der vom Compiler generierten Header Datei zu erstellen. Wenn Sie kein Symbol angeben, generiert der Compiler einen für Sie.<br/> |
| value   | [**UInt8Type**](eventmanifestschema-hexint8type-simpletype.md)   | Der Wert der Ebene. Sie können Werte im Bereich von 16 bis 255 angeben. Informationen zu vordefinierten Werten finden Sie unter Hinweise.<br/>                                                                                                                                                                                               |



## <a name="remarks"></a>Bemerkungen

Im folgenden sind die vordefinierten Ebenen-Werte, die Sie verwenden können, fest. Diese Werte werden in der Winmeta.xml-Datei definiert, die in der Windows SDK enthalten ist.



| Name              | Wert | Symbol                    | BESCHREIBUNG                                                             |
|-------------------|-------|---------------------------|-------------------------------------------------------------------------|
| win:Critical      | 1     | WinEvent- \_ Ebene \_ kritisch | Identifiziert ein nicht normales Exit-oder Beendigungs Ereignis.<br/>            |
| win:Error         | 2     | Fehler auf \_ winereignisebene \_    | Identifiziert ein schwerwiegendes Fehler Ereignis.<br/>                             |
| win:Warning       | 3     | Warnung auf \_ winereignisebene \_  | Identifiziert ein Warn Ereignis, z. b. einen Zuordnungs Fehler.<br/>    |
| win:Informational | 4     | Informationen zur WinEvent- \_ Ebene \_     | Identifiziert ein nicht-Fehler Ereignis, z. b. ein Eingabe-oder ein Exit-Ereignis.<br/> |
| win:Verbose       | 5     | Verbose der WinEvent- \_ Ebene \_  | Identifiziert ein ausführliches Ablauf Verfolgungs Ereignis.<br/>                           |



 

Eine höhere Anzahl impliziert, dass Sie auch niedrigere Ebenen erhalten. Wenn Sie z. b. "Win: Warning" angeben, werden alle Warnungen, Fehler und kritischen Ereignisse angezeigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





