---
title: Komplexer eventstype-Typ
description: Enthält eine Liste von Anbietern, die im Manifest definiert sind. | Komplexer eventstype-Typ
ms.assetid: 43f9f577-eae0-45c5-aaf0-5a6df28d3b79
keywords:
- Ereignisprotokoll für komplexen eventstype-Typ
topic_type:
- apiref
api_name:
- EventsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 36500aa037c8e33a48b4f9dd6e38e46eaac58da2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106350625"
---
# <a name="eventstype-complex-type"></a>Komplexer eventstype-Typ

Enthält eine Liste von Anbietern, die im Manifest definiert sind.

``` syntax
<xs:complexType name="EventsType">
    <xs:choice
        maxOccurs="unbounded"
    >
        <xs:element name="provider"
            type="ProviderType"
            maxOccurs="unbounded"
         />
        <xs:element name="messageTable"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:sequence>
                    <xs:element name="message"
                        minOccurs="0"
                        maxOccurs="unbounded"
                    >
                        <xs:complexType>
                            <xs:attribute name="value"
                                type="UInt32Type"
                                use="required"
                             />
                            <xs:attribute name="mid"
                                type="xs:string"
                                use="optional"
                             />
                            <xs:attribute name="message"
                                type="strTableRef"
                                use="required"
                             />
                            <xs:attribute name="symbol"
                                type="CSymbolType"
                                use="optional"
                             />
                        </xs:complexType>
                    </xs:element>
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:choice>
    <xs:anyAttribute
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente

| Element | type | BESCHREIBUNG |
|---------|------|-------------|
| message |      | Definiert eine Meldungs Zeichenfolge. |
| messagetable | | Definiert eine Liste von Meldungs Zeichenfolgen. Sie sollten keine Nachrichten Tabelle verwenden, außer in den folgenden Fällen, in denen Sie eine Nachrichten Tabelle definieren müssen, um Nachrichten Zeichenfolgen explizit Ressourcen Nummern zuzuweisen. <ul><li>Sie Migrieren von einer nachrichtentexttextdatei (. MC) zu einem Manifest, schreiben aber immer noch Ereignisse in die Anwendungs-und System Kanäle, damit Legacy Consumer die Ereignisse weiterhin nutzen können. Um dies zu ermöglichen, müssen die Ressourcen Bezeichner für die im Manifest definierten Nachrichten Zeichenfolgen mit den Ereignis bezeichlern identisch sein. Der Nachrichten Compiler weist den Meldungs Zeichenfolgen jedoch automatisch Ressourcen Bezeichner zu. Um den Compiler zu überschreiben, verwenden Sie die Message-Tabelle, und legen Sie das value-Attribut auf den Ereignis Bezeichner und das Message-Attribut fest, um auf eine Zeichenfolge in der Zeichen folgen Tabelle im Lokalisierungs Abschnitt des Manifests zu verweisen.</li><li>Wenn Sie mehr als 16 Anbieter identifizieren möchten, müssen Sie die Nachrichten Tabelle einschließen, mit der die-und-Anbieter Ressourcen Werte für die von Ihnen definierten Nachrichten Zeichenfolgen zuweisen müssen. Wenn der Anbieter auf Meldungs Zeichenfolgen verweist, die von den Anbietern 1 bis 16 definiert wurden, schließen Sie diese Nachrichten Zeichenfolgen nicht in die Nachrichten Tabelle ein</li></ul>|
| [**ab**](eventmanifestschema-provider-eventstype-element.md) | [**ProviderType**](eventmanifestschema-providertype-complextype.md) | Eine Liste von Anbietern, die Sie definieren möchten. |

## <a name="attributes"></a>Attributes

| Name    | type                                                             | BESCHREIBUNG                                                                            |
|---------|------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| message | [**"Strauch"**](eventmanifestschema-strtableref-simpletype.md) | Ein Verweis auf die lokalisierte Zeichenfolge in der Zeichen folgen Tabelle.                               |
| mId     | xs:string                                                        | Nicht verwendet.                                                                              |
| Symbol  | [**Csymboltype**](eventmanifestschema-csymboltype-simpletype.md) | Der symbolische Name, den der Nachrichten Compiler für diese Meldungs Zeichenfolge erstellen soll.|
| value   | [**UInt32Type**](eventmanifestschema-hexint32type-simpletype.md) | Die Zahl, die als Nachrichten-ID für diese Nachricht verwendet werden soll.                          |


## <a name="remarks"></a>Bemerkungen

Der praktische Grenzwert für die Anzahl von Anbietern, die Sie in einem Manifest definieren können, sind 16 Anbieter. Wenn Sie mehr als 16 Anbieter angeben, müssen Sie eine Nachrichten Tabelle zum expliziten Zuweisen von Ressourcen Nummern zu den Nachrichten Zeichenfolgen verwenden, auf die der Anbieter verweist. Weitere Informationen finden Sie im obigen Nachrichten Element.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|--------------------------|-------------------------------------------|
| Unterstützte Mindestversion (Client) | Nur Windows Vista \[ -Desktop-Apps\]       |
| Unterstützte Mindestversion (Server) | Nur Windows Server 2008 \[ -Desktop-Apps\] |
