---
title: Komplexer ProviderType-Typ
description: Definiert einen Anbieter und die Metadaten, die er verwendet, um seine Ereignisse zu definieren. | Komplexer ProviderType-Typ
ms.assetid: 70199cf5-a6d0-4780-9ff1-ed083a5b49ac
keywords:
- Provider Type Complex-Typ EventLog
topic_type:
- apiref
api_name:
- ProviderType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c258b3ff48cdd2f00f632fdce770b58182a531c7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353369"
---
# <a name="providertype-complex-type"></a>Komplexer ProviderType-Typ

Definiert einen Anbieter und die Metadaten, die er verwendet, um seine Ereignisse zu definieren.

``` syntax
<xs:complexType name="ProviderType">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
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
         />
        <xs:element name="keywords"
            type="KeywordListType"
         />
        <xs:element name="maps"
            type="MapType"
         />
        <xs:element name="namedQueries"
            type="NamedQueryType"
         />
        <xs:element name="templates"
            type="TemplateListType"
         />
        <xs:element name="events"
            type="DefinitionType"
         />
        <xs:element name="filters"
            type="FilterListType"
         />
        <xs:any
            processContents="lax"
            namespace="##other"
         />
    </xs:choice>
    <xs:attribute name="name"
        type="anyURI"
        use="required"
     />
    <xs:attribute name="guid"
        type="GUIDType"
        use="required"
     />
    <xs:attribute name="resourceFileName"
        type="filePath"
        use="optional"
     />
    <xs:attribute name="messageFileName"
        type="filePath"
        use="optional"
     />
    <xs:attribute name="parameterFileName"
        type="filePath"
        use="optional"
     />
    <xs:attribute name="helpLink"
        type="anyURI"
        use="optional"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="required"
     />
    <xs:attribute name="message"
        type="strTableRef"
        use="optional"
     />
    <xs:attribute name="source"
        use="optional"
        default="Xml"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="Xml"
                 />
                <xs:enumeration
                    value="Wbem"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="warnOnApplicationCompatibilityError"
        type="xs:boolean"
        use="optional"
        default="false"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                       | type                                                                         | BESCHREIBUNG                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**channels**](eventmanifestschema-channels-providertype-element.md)         | [**Channelellisttype**](eventmanifestschema-channellisttype-complextype.md)   | Definiert eine Liste von Kanälen, zu denen Anbieter Ereignisse protokollieren können.<br/>                                                                                                                                                                                      |
| [**Fall**](eventmanifestschema-events-providertype-element.md)             | [**DefinitionType**](eventmanifestschema-definitiontype-complextype.md)     | Definiert eine Liste der Ereignis Definitionen der Ereignisse, die der Anbieter protokollieren kann.<br/>                                                                                                                                                                       |
| **Filter**                                                                   | [**Filterlisttype**](eventmanifestschema-filterlisttype-complextype.md)     | Definiert eine Liste von Filtern, die Ihr Anbieter unterstützt. Sie können die Filter wie das Level und die Schlüsselwörter verwenden, um zu bestimmen, ob Sie ein Ereignis schreiben möchten. <br/> **Windows Server 2008 und Windows Vista:** Wird bis Windows 7 nicht unterstützt.<br/> |
| [**Keywords**](eventmanifestschema-keywords-providertype-element.md)         | [**Keywordlisttype**](eventmanifestschema-keywordlisttype-complextype.md)   | Definiert eine Liste von Schlüsselwörtern zum Kategorisieren von Ereignissen.<br/>                                                                                                                                                                                                 |
| [**Grad**](eventmanifestschema-levels-providertype-element.md)             | [**Levellisttype**](eventmanifestschema-levellisttype-complextype.md)       | Definiert eine Liste von Ebenen, die den Schweregrad eines Ereignisses angeben.<br/>                                                                                                                                                                                    |
| [**Maps**](eventmanifestschema-maps-providertype-element.md)                 | [**MapType**](eventmanifestschema-maptype-complextype.md)                   | Definiert eine Liste von Name-Wert-Paaren, auf die Sie im Vorlagen Abschnitt des Manifests verweisen können.<br/>                                                                                                                                                 |
| [**namedqueries**](eventmanifestschema-namedqueries-providertype-element.md) | [**Namedquerytype**](eventmanifestschema-namedquerytype-complextype.md)     | Nicht verwendet. Definiert eine Liste benannter Abfragen, die die Ereignis Meldungs Zeichenfolge nach einem Wert Abfragen und eine angegebene Aktion ausführen, sofern gefunden.<br/>                                                                                                                 |
| [**OpCodes**](eventmanifestschema-opcodes-providertype-element.md)           | [**Opcodelisttype**](eventmanifestschema-opcodelisttype-complextype.md)     | Definiert eine Liste von Opcodes, die Sie zum Gruppieren von Ereignissen innerhalb einer Aufgabe verwenden können.<br/>                                                                                                                                                                          |
| [**erfüllen**](eventmanifestschema-tasks-providertype-element.md)               | [**Tasklisttype**](eventmanifestschema-tasklisttype-complextype.md)         | Definiert eine Liste von Aufgaben, die ein Anbieter zum Gruppieren von Ereignissen verwenden kann. In der Regel verwenden Sie Aufgaben, um Ereignisse für ein Feature oder eine Komponente des Anbieters zu gruppieren.<br/>                                                                                              |
| [**betrachtet**](eventmanifestschema-templates-providertype-element.md)       | [**Templatelisttype**](eventmanifestschema-templatelisttype-complextype.md) | Definiert eine Liste von Vorlagen, die die Daten angeben, die in die Ereignisse eingeschlossen werden sollen.<br/>                                                                                                                                                                      |



## <a name="attributes"></a>Attributes



| Name                                | type                                                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| guid                                | [**Guidtype**](eventmanifestschema-guidtype-simpletype.md)       | Eine GUID, die den Anbieter eindeutig identifiziert.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| HelpLink                            | anyURI                                                            | Die URL oder der MS-Link zu Inhalt, der Informationen zu den Ereignissen bereitstellt, die der Anbieter auslöst.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                           |
| message                             | [**"Strauch"**](eventmanifestschema-strtableref-simpletype.md) | Der lokalisierte Anzeige Name für den Anbieter. Die Meldungs Zeichenfolge verweist auf eine lokalisierte Zeichenfolge im [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) -Abschnitt des Manifests. <br/>                                                                                                                                                                                                                                                                                                                           |
| messagefilename                     | [**FilePath**](eventmanifestschema-filepath-simpletype.md)       | Der vollständige Pfad zu der Datei, die die lokalisierten Nachrichten Ressourcen des Anbieters enthält. Die Datei kann eine ausführbare Datei oder eine DLL-Datei sein.<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| name                                | anyURI                                                            | Der Name des Anbieters. Der Name sollte das Format *Company* - *Product* - *Component* aufweisen.<br/> Der Name darf nicht länger als 255 Zeichen sein und darf die folgenden Zeichen nicht enthalten: ' > ', ' < ', ' & ', ' ', ' \| ', ' \\ ', ': ', ' ', '? ', ' \* ' oder Zeichen mit Codes, die kleiner als 31 sind. Außerdem muss der Name den allgemeinen Einschränkungen für Datei-und Registrierungsschlüssel Namen folgen. Diese Einschränkungen finden Sie unter [Benennen einer Datei](/windows/desktop/FileIO/naming-a-file)und [Größenbeschränkungen von Registrierungs Elementen](/windows/desktop/SysInfo/registry-element-size-limits).<br/> |
| parameterfilename                   | [**FilePath**](eventmanifestschema-filepath-simpletype.md)       | Der vollständige Pfad zu der Datei, die die Parameter-Zeichen folgen Ressourcen des Anbieters enthält. Die Datei kann eine ausführbare Datei oder eine DLL-Datei sein. Sie können mehr als eine durch ein Semikolon getrennte Parameterdatei angeben. Die Datei wird durchsucht, wenn die Meldungs Zeichenfolge eines Ereignisses eine Parameter Zeichenfolge enthält. Mit Parametern können lokalisierbare Einfügezeichenfolgen Weitere Informationen finden Sie unter Hinweise.<br/>                                                                                                                                                |
| resourceFileName                    | [**FilePath**](eventmanifestschema-filepath-simpletype.md)       | Der vollständige Pfad zu der Datei, die die Metadatenressourcen des Anbieters enthält. Die Datei kann eine ausführbare Datei oder eine DLL-Datei sein.<br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| source                              |                                                                   | Nur zur internen Verwendung.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Symbol                              | [**Csymboltype**](eventmanifestschema-csymboltype-simpletype.md) | Das Symbol, mit dem auf die GUID des Anbieters in der Anwendung verwiesen werden soll. Der [**Nachrichten Compiler (MC.exe)**](message-compiler--mc-exe-.md) verwendet das Symbol, um eine Konstante für die GUID des Anbieters in der vom Compiler generierten Header Datei zu erstellen.<br/>                                                                                                                                                                                                                                                                           |
| warnonapplicationcompatibilityerror | **xs:boolean**                                                    | Nur zur internen Verwendung.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



## <a name="remarks"></a>Bemerkungen

Der Windows-Ereignisanzeige (Eventvwr.exe) verwendet die lokalisierte Meldungs Zeichenfolge, falls verfügbar. Andernfalls wird die Zeichenfolge aus dem Name-Attribut verwendet.

Die Pfade für "resourceFileName", "messagefilename" und "parameterfilename" können Umgebungsvariablen enthalten. Wenn Sie eine neue Umgebungsvariable definieren, die im Pfad verwendet werden soll, müssen Sie den Computer neu starten, damit der Ereignisprotokoll Dienst die neue Variable abrufen kann. Andernfalls ist der Dienst nicht in der Lage, die Ressourcen des Anbieters zu finden.

Die Meldungs Zeichenfolge eines Ereignisses kann Einfügungs-und Parameter Zeichenfolgen enthalten Eine Einfügezeichenfolge hat das Format%*n*, wobei *n* ein einbasierter Index ist, der ein Datenelement aus der Daten Vorlage des Ereignisses identifiziert, das Sie in die Nachricht einfügen möchten. Eine Parameter Zeichenfolge (siehe das **parameterfilename** -Attribut) hat die Form%%*n*, wobei n der Bezeichner einer Nachricht in der Nachrichten Tabelle ist. Wenn die Meldungs Zeichenfolge des Ereignisses "%1% %11 = %2% %12" enthielt und die Datenelement Werte für "%1" und "%2" jeweils 8 bzw. 2 lauten und die Parameter Zeichenfolgen für% %11 und% %12 "Quarts" bzw

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

