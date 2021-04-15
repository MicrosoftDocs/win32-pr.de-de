---
title: Komplexer FilterType-Typ
description: Definiert einen Daten Filter, den eine Sitzung verwendet, um Ereignisse auf der Grundlage von Ereignisdaten zu filtern.
ms.assetid: f2874b3f-cf3a-4dd9-b914-6adaac33cf7b
keywords:
- "\"FilterType Complex Type Event Log\""
topic_type:
- apiref
api_name:
- FilterType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ef3d80b8cb5347c1adf0e2b21a745e4d4f5fae2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479275"
---
# <a name="filtertype-complex-type"></a>Komplexer FilterType-Typ

Definiert einen Daten Filter, den eine Sitzung verwendet, um Ereignisse auf der Grundlage von Ereignisdaten zu filtern.

``` syntax
<xs:complexType name="FilterType">
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="value"
                type="UInt8Type"
                use="required"
             />
            <xs:attribute name="version"
                type="UInt8Type"
                use="optional"
             />
            <xs:attribute name="name"
                type="QName"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="optional"
             />
            <xs:attribute name="tid"
                type="token"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Attributes



| Name    | type                                                              | BESCHREIBUNG                                                                                                                                                                                                                                      |
|---------|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| message | [**"Strauch"**](eventmanifestschema-strtableref-simpletype.md) | Die lokalisierte Beschreibung für den Filter. Die Meldungs Zeichenfolge verweist auf eine lokalisierte Zeichenfolge im [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) -Abschnitt des Manifests.<br/>                                   |
| name    | **QName**                                                         | Ein Name, der den Filter angibt.<br/>                                                                                                                                                                                                    |
| Symbol  | [**Csymboltype**](eventmanifestschema-csymboltype-simpletype.md) | Das Symbol, das für den Verweis auf den Filter in der Anwendung verwendet werden soll. Der [**Nachrichten Compiler (MC.exe)**](message-compiler--mc-exe-.md) verwendet das Symbol, um eine Konstante für den Filter in der vom Compiler generierten Header Datei zu erstellen.<br/> |
| tid     | token                                                             | Ein Vorlagen Bezeichner, der die Filterdaten beschreibt, die die Sitzung an den Anbieter übergibt, wenn Sie den Anbieter aktiviert.<br/>                                                                                                            |
| value   | [**UInt8Type**](eventmanifestschema-hexint8type-simpletype.md)   | Ein ganzzahliger Wert, der den Filter in der Liste der von Ihnen definierten Filter eindeutig identifiziert.<br/>                                                                                                                                      |
| version | [**UInt8Type**](eventmanifestschema-hexint8type-simpletype.md)   | Ein ganzzahliger Wert, der diese Version des Filters identifiziert. Wenn nicht angegeben, ist der Wert 0 (null).<br/>                                                                                                                                     |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/> |



 

 





