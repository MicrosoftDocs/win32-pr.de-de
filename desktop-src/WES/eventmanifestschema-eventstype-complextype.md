---
title: Komplexer Ereignistyp
description: Enthält eine Liste von Anbietern, die im Manifest definiert sind. | Komplexer Ereignistyp
ms.assetid: 43f9f577-eae0-45c5-aaf0-5a6df28d3b79
keywords:
- EventLog vom komplexen Ereignistyp "EventsType"
topic_type:
- apiref
api_name:
- EventsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8d0cee50c0332d283c439448fd80c7abe319fec5065f39dcad4e053baf600bd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055988"
---
# <a name="eventstype-complex-type"></a>Komplexer Ereignistyp

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

| Element | Typ | Beschreibung |
|---------|------|-------------|
| message |      | Definiert eine Meldungszeichenfolge. |
| messageTable | | Definiert eine Liste von Nachrichtenzeichenfolgen. Sie sollten keine Meldungstabelle verwenden müssen, außer in den folgenden Fällen, in denen Sie eine Meldungstabelle definieren müssen, um Nachrichtenzeichenfolgen explizit Ressourcennummern zuzuweisen. <ul><li>Sie migrieren von einer Nachrichtentextdatei (MC)-Datei zu einem Manifest, schreiben aber weiterhin Ereignisse in die Anwendungs- und Systemkanäle, sodass Legacy-Consumer die Ereignisse weiterhin nutzen können. Damit dies funktioniert, müssen die Ressourcenbezeichner für die im Manifest definierten Meldungszeichenfolgen mit den Ereignisbezeichnern identisch sein. Der Nachrichtencompiler weist den Nachrichtenzeichenfolgen jedoch automatisch Ressourcenbezeichner zu. Verwenden Sie zum Überschreiben des Compilers die Meldungstabelle, und legen Sie das Value-Attribut auf den Ereignisbezeichner und das Nachrichtenattribut fest, um auf eine Zeichenfolge in der Zeichenfolgentabelle im Lokalisierungsabschnitt des Manifests zu verweisen.</li><li>Wenn Sie mehr als 16 Anbieter identifizieren möchten, müssen Sie die Meldungstabelle einschließen, die der Siebzehnte und der Anbieter verwenden müssen, um Ressourcenwerte für die von ihnen definierten Nachrichtenzeichenfolgen zuzuweisen. Wenn der Anbieter auf Nachrichtenzeichenfolgen verweist, die von den Anbietern 1 bis 16 definiert sind, schließen Sie diese Nachrichtenzeichenfolgen nicht in die Meldungstabelle ein.</li></ul>|
| [**Anbieter**](eventmanifestschema-provider-eventstype-element.md) | [**ProviderType**](eventmanifestschema-providertype-complextype.md) | Eine Liste der Anbieter, die Sie definieren möchten. |

## <a name="attributes"></a>Attributes

| Name    | Typ                                                             | Beschreibung                                                                            |
|---------|------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| message | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | Ein Verweis auf die lokalisierte Zeichenfolge in der Zeichenfolgentabelle.                               |
| mId     | xs:string                                                        | Wird nicht verwendet.                                                                              |
| Symbol  | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Der symbolische Name, den der Nachrichtencompiler für diese Meldungszeichenfolge erstellen soll.|
| Wert   | [**UInt32Type**](eventmanifestschema-hexint32type-simpletype.md) | Die Zahl, die als Nachrichtenbezeichner für diese Nachricht verwendet werden soll.                          |


## <a name="remarks"></a>Hinweise

Die praktische Beschränkung der Anzahl von Anbietern, die Sie in einem Manifest definieren können, beträgt 16 Anbieter. Wenn Sie mehr als 16 Anbieter angeben, müssen Sie den Meldungszeichenfolgen, auf die der Anbieter verweist, explizit Ressourcennummern zuweisen. Weitere Informationen finden Sie im obigen Meldungselement.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|--------------------------|-------------------------------------------|
| Unterstützte Mindestversion (Client) | Windows \[Nur Vista-Desktop-Apps\]       |
| Unterstützte Mindestversion (Server) | Windows Nur Server \[ 2008-Desktop-Apps\] |
