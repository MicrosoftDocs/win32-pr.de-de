---
title: Komplexer MetadataType-Typ
description: Definiert die Metadatentypen, die Sie im Metadatenabschnitt des Manifests definieren können.
ms.assetid: 602bafe7-940e-4313-9da5-54c6aa7f60a2
keywords:
- Komplexer MetadataType-Typ EventLog
topic_type:
- apiref
api_name:
- MetadataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 392e0bb2940c36b541f63f55dac418312489f231d785f82014ade82c20602fbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118343602"
---
# <a name="metadatatype-complex-type"></a>Komplexer MetadataType-Typ

Definiert die Metadatentypen, die Sie im Metadatenabschnitt des Manifests definieren können.

``` syntax
<xs:complexType name="MetadataType">
    <xs:sequence>
        <xs:element name="channels"
            type="ChannelListType"
         />
        <xs:element name="levels"
            type="LevelListType"
         />
        <xs:element name="tasks"
            type="TaskListType"
         />
        <xs:element name="opcodes"
            type="OpcodeListType"
            minOccurs="0"
         />
        <xs:element name="keywords"
            type="KeywordListType"
            minOccurs="0"
         />
        <xs:element name="types"
            type="TypeListType"
            minOccurs="0"
         />
        <xs:element name="namedQueries"
            type="NamedQueryType"
            minOccurs="0"
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
    </xs:sequence>
    <xs:attribute name="name"
        type="anyURI"
        use="required"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                       | Typ                                                                       | Beschreibung                                                                                                                                                      |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Kanäle**](eventmanifestschema-channels-metadatatype-element.md)         | [**ChannelListType**](eventmanifestschema-channellisttype-complextype.md) | Definiert eine Liste von Kanälen, für die Anbieter Ereignisse protokollieren können. Ein Anbieter kann dann einen oder mehrere Kanäle in sein Manifest importieren.<br/>               |
| [**Schlüsselwörter**](eventmanifestschema-keywords-metadatatype-element.md)         | [**KeywordListType**](eventmanifestschema-keywordlisttype-complextype.md) | Definiert eine Liste von Schlüsselwörtern, die die Kategorie der Ereignisse bestimmen, die der Anbieter schreibt.<br/>                                                            |
| [**Ebenen**](eventmanifestschema-levels-metadatatype-element.md)             | [**LevelListType**](eventmanifestschema-levellisttype-complextype.md)     | Definiert eine Liste von Ebenen, die den Schweregrad eines Ereignisses angeben.<br/>                                                                                       |
| **Nachricht**                                                                   |                                                                            | Definiert eine Meldungszeichenfolge.<br/>                                                                                                                             |
| **messageTable**                                                              |                                                                            | Definiert eine Liste von Nachrichtenzeichenfolgen.<br/>                                                                                                                    |
| [**namedQueries**](eventmanifestschema-namedqueries-metadatatype-element.md) | [**NamedQueryType**](eventmanifestschema-namedquerytype-complextype.md)   | Definiert eine Liste benannter Abfragen, die reguläre Ausdrücke verwenden, um Such- und Ersetzungsaktionen für die Nachrichtenzeichenfolge eines Ereignisses auszuführen.<br/>                        |
| [**Opcodes**](eventmanifestschema-opcodes-metadatatype-element.md)           | [**OpcodeListType**](eventmanifestschema-opcodelisttype-complextype.md)   | Definiert eine Liste von Opcodes, die Sie zum Gruppieren von Ereignissen innerhalb einer Aufgabe verwenden können.<br/>                                                                             |
| **tasks**                                                                     | [**TaskListType**](eventmanifestschema-tasklisttype-complextype.md)       | Definiert eine Liste von Aufgaben, die ein Anbieter zum Gruppieren von Ereignissen verwenden kann. In der Regel verwenden Sie Aufgaben, um Ereignisse für ein Feature oder eine Komponente des Anbieters zu gruppieren.<br/> |
| [**Typen**](eventmanifestschema-types-metadatatype-element.md)               | [**TypeListType**](eventmanifestschema-typelisttype-complextype.md)       | Definiert eine Liste von XML-Typen.<br/>                                                                                                                          |



## <a name="attributes"></a>Attributes



| Name    | Typ                                                              | Beschreibung                                                                                        |
|---------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| message | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | Ein Verweis auf die lokalisierte Zeichenfolge in der Zeichenfolgentabelle.<br/>                                |
| mId     | xs:string                                                         | Wird nicht verwendet.<br/>                                                                               |
| name    | anyURI                                                            | Der URI der Metadatei. <br/>                                                              |
| Symbol  | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Der symbolische Name, den der Nachrichtencompiler für diese Meldungszeichenfolge erstellen soll.<br/> |
| Wert   | [**UInt32Type**](eventmanifestschema-hexint32type-simpletype.md) | Die Zahl, die als Nachrichtenbezeichner für diese Nachricht verwendet werden soll.<br/>                           |



## <a name="remarks"></a>Hinweise

Obwohl Sie ein Manifest erstellen können, das einen Metadatenabschnitt enthält, wird es vom Dienst nicht verwendet. Die einzigen Metadaten, die der Dienst erkennt, sind die Metadaten, die in der datei Winmeta.xml gefunden werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





