---
title: Komplexer metadataType-Typ
description: Definiert die Metadatentypen, die Sie im Metadatenabschnitt des Manifests definieren können.
ms.assetid: 602bafe7-940e-4313-9da5-54c6aa7f60a2
keywords:
- MetadataType komplexer Typ (Ereignisprotokoll)
topic_type:
- apiref
api_name:
- MetadataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 69b140a2b65d47d563fd88f49d6818efc13613f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040965"
---
# <a name="metadatatype-complex-type"></a>Komplexer metadataType-Typ

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



| Element                                                                       | type                                                                       | BESCHREIBUNG                                                                                                                                                      |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**channels**](eventmanifestschema-channels-metadatatype-element.md)         | [**Channelellisttype**](eventmanifestschema-channellisttype-complextype.md) | Definiert eine Liste von Kanälen, zu denen Anbieter Ereignisse protokollieren können. Ein Anbieter kann dann einen oder mehrere der Kanäle in seinem Manifest importieren.<br/>               |
| [**Keywords**](eventmanifestschema-keywords-metadatatype-element.md)         | [**Keywordlisttype**](eventmanifestschema-keywordlisttype-complextype.md) | Definiert eine Liste von Schlüsselwörtern, die die Kategorie der vom Anbieter schreibenden Ereignisse bestimmen.<br/>                                                            |
| [**Grad**](eventmanifestschema-levels-metadatatype-element.md)             | [**Levellisttype**](eventmanifestschema-levellisttype-complextype.md)     | Definiert eine Liste von Ebenen, die den Schweregrad eines Ereignisses angeben.<br/>                                                                                       |
| **Nachricht**                                                                   |                                                                            | Definiert eine Meldungs Zeichenfolge.<br/>                                                                                                                             |
| **messagetable**                                                              |                                                                            | Definiert eine Liste von Meldungs Zeichenfolgen.<br/>                                                                                                                    |
| [**namedqueries**](eventmanifestschema-namedqueries-metadatatype-element.md) | [**Namedquerytype**](eventmanifestschema-namedquerytype-complextype.md)   | Definiert eine Liste benannter Abfragen, die reguläre Ausdrücke verwenden, um Aktionen zum Suchen und ersetzen in der Meldungs Zeichenfolge eines Ereignisses auszuführen.<br/>                        |
| [**OpCodes**](eventmanifestschema-opcodes-metadatatype-element.md)           | [**Opcodelisttype**](eventmanifestschema-opcodelisttype-complextype.md)   | Definiert eine Liste von Opcodes, die Sie zum Gruppieren von Ereignissen innerhalb einer Aufgabe verwenden können.<br/>                                                                             |
| **tasks**                                                                     | [**Tasklisttype**](eventmanifestschema-tasklisttype-complextype.md)       | Definiert eine Liste von Aufgaben, die ein Anbieter zum Gruppieren von Ereignissen verwenden kann. In der Regel verwenden Sie Aufgaben, um Ereignisse für ein Feature oder eine Komponente des Anbieters zu gruppieren.<br/> |
| [**solche**](eventmanifestschema-types-metadatatype-element.md)               | [**Typelisttype**](eventmanifestschema-typelisttype-complextype.md)       | Definiert eine Liste von XML-Typen.<br/>                                                                                                                          |



## <a name="attributes"></a>Attributes



| Name    | type                                                              | BESCHREIBUNG                                                                                        |
|---------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| message | [**"Strauch"**](eventmanifestschema-strtableref-simpletype.md) | Ein Verweis auf die lokalisierte Zeichenfolge in der Zeichen folgen Tabelle.<br/>                                |
| mId     | xs:string                                                         | Nicht verwendet.<br/>                                                                               |
| name    | anyURI                                                            | Der URI der Metadatendatei. <br/>                                                              |
| Symbol  | [**Csymboltype**](eventmanifestschema-csymboltype-simpletype.md) | Der symbolische Name, den der Nachrichten Compiler für diese Meldungs Zeichenfolge erstellen soll.<br/> |
| value   | [**UInt32Type**](eventmanifestschema-hexint32type-simpletype.md) | Die Zahl, die als Nachrichten-ID für diese Nachricht verwendet werden soll.<br/>                           |



## <a name="remarks"></a>Bemerkungen

Obwohl Sie ein Manifest erstellen können, das einen Metadatenabschnitt enthält, wird es vom Dienst nicht verwendet. die einzigen Metadaten, die der Dienst erkennt, sind die Metadaten, die in der Winmeta.xml-Datei gefunden werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





