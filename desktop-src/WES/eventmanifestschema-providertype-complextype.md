---
title: Komplexer ProviderType-Typ
description: Definiert einen Anbieter und die Metadaten, die er zum Definieren seiner Ereignisse verwendet. | Komplexer ProviderType-Typ
ms.assetid: 70199cf5-a6d0-4780-9ff1-ed083a5b49ac
keywords:
- Komplexer ProviderType-Typ EventLog
topic_type:
- apiref
api_name:
- ProviderType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e48edd19d6ff9a547ce1698f81c89f780ffaa48f6312a656ef18664b39e78410
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119511270"
---
# <a name="providertype-complex-type"></a>Komplexer ProviderType-Typ

Definiert einen Anbieter und die Metadaten, die er zum Definieren seiner Ereignisse verwendet.

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



| Element                                                                       | Typ                                                                         | Beschreibung                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Kanäle**](eventmanifestschema-channels-providertype-element.md)         | [**ChannelListType**](eventmanifestschema-channellisttype-complextype.md)   | Definiert eine Liste von Kanälen, an die Anbieter Ereignisse protokollieren können.<br/>                                                                                                                                                                                      |
| [**Ereignisse**](eventmanifestschema-events-providertype-element.md)             | [**DefinitionType**](eventmanifestschema-definitiontype-complextype.md)     | Definiert eine Liste von Ereignisdefinitionen der Ereignisse, die der Anbieter protokollieren kann.<br/>                                                                                                                                                                       |
| **Filter**                                                                   | [**FilterListType**](eventmanifestschema-filterlisttype-complextype.md)     | Definiert eine Liste von Filtern, die ihr Anbieter unterstützt. Sie können die Filter wie bei den Schlüsselwörtern und verwenden, um zu bestimmen, ob Sie ein Ereignis schreiben möchten. <br/> **Windows Server 2008 und Windows Vista:** Wird erst ab Windows 7 unterstützt.<br/> |
| [**Schlüsselwörter**](eventmanifestschema-keywords-providertype-element.md)         | [**KeywordListType**](eventmanifestschema-keywordlisttype-complextype.md)   | Definiert eine Liste von Schlüsselwörtern, die Ereignisse kategorisieren.<br/>                                                                                                                                                                                                 |
| [**Ebenen**](eventmanifestschema-levels-providertype-element.md)             | [**LevelListType**](eventmanifestschema-levellisttype-complextype.md)       | Definiert eine Liste von Ebenen, die den Schweregrad eines Ereignisses angeben.<br/>                                                                                                                                                                                    |
| [**Karten**](eventmanifestschema-maps-providertype-element.md)                 | [**MapType**](eventmanifestschema-maptype-complextype.md)                   | Definiert eine Liste von Name-Wert-Paaren, auf die Sie im Vorlagenabschnitt des Manifests verweisen können.<br/>                                                                                                                                                 |
| [**namedQueries**](eventmanifestschema-namedqueries-providertype-element.md) | [**NamedQueryType**](eventmanifestschema-namedquerytype-complextype.md)     | Wird nicht verwendet. Definiert eine Liste benannter Abfragen, die die Ereignismeldungszeichenfolge nach einem Wert abfragen und eine angegebene Aktion ausführen, falls gefunden.<br/>                                                                                                                 |
| [**Opcodes**](eventmanifestschema-opcodes-providertype-element.md)           | [**OpcodeListType**](eventmanifestschema-opcodelisttype-complextype.md)     | Definiert eine Liste von Opcodes, die Sie zum Gruppieren von Ereignissen innerhalb einer Aufgabe verwenden können.<br/>                                                                                                                                                                          |
| [**Aufgaben**](eventmanifestschema-tasks-providertype-element.md)               | [**TaskListType**](eventmanifestschema-tasklisttype-complextype.md)         | Definiert eine Liste von Aufgaben, die ein Anbieter zum Gruppen von Ereignissen verwenden kann. In der Regel verwenden Sie Aufgaben, um Ereignisse für ein Feature oder eine Komponente des Anbieters zu gruppen.<br/>                                                                                              |
| [**Vorlagen**](eventmanifestschema-templates-providertype-element.md)       | [**TemplateListType**](eventmanifestschema-templatelisttype-complextype.md) | Definiert eine Liste von Vorlagen, die die Daten angeben, die in die Ereignisse aufgenommen werden.<br/>                                                                                                                                                                      |



## <a name="attributes"></a>Attributes



| Name                                | Typ                                                              | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| guid                                | [**GUIDType**](eventmanifestschema-guidtype-simpletype.md)       | Eine GUID, die den Anbieter eindeutig identifiziert.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Helplink                            | anyURI                                                            | Die URL oder ms help link to content that provides information about the events that the provider raises.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                           |
| message                             | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | Der lokalisierte Anzeigename für den Anbieter. Die Meldungszeichenfolge verweist auf eine lokalisierte Zeichenfolge im [**StringTable-Abschnitt**](eventmanifestschema-stringtable-resources-element.md) des Manifests. <br/>                                                                                                                                                                                                                                                                                                                           |
| messageFileName                     | [**Filepath**](eventmanifestschema-filepath-simpletype.md)       | Der vollständige Pfad zu der Datei, die die lokalisierten Nachrichtenressourcen des Anbieters enthält. Die Datei kann eine ausführbare Datei oder DLL-Datei sein.<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| name                                | anyURI                                                            | Der Name des Anbieters. Der Name sollte das Formular Company Product Component  -  - *(Unternehmensproduktkomponente) haben.*<br/> Der Name darf nicht länger als 255 Zeichen sein und darf nicht die folgenden Zeichen enthalten: ">", "<", "&", ", " \| ", \\ ", ":", "", "?", " " oder Zeichen mit Codes kleiner \* als 31. Darüber hinaus muss der Name den allgemeinen Einschränkungen für Datei- und Registrierungsschlüsselnamen folgen. Diese Einschränkungen finden Sie unter Naming a File (Benennen [einer Datei)](/windows/desktop/FileIO/naming-a-file)und Registry Element Size Limits (Größenbeschränkungen [für Registrierungselemente).](/windows/desktop/SysInfo/registry-element-size-limits)<br/> |
| parameterFileName                   | [**Filepath**](eventmanifestschema-filepath-simpletype.md)       | Der vollständige Pfad zu der Datei, die die Parameterzeichenfolgenressourcen des Anbieters enthält. Die Datei kann eine ausführbare Datei oder DLL-Datei sein. Sie können mehrere Parameterdatei angeben, die durch ein Semikolon getrennt ist. Die Datei wird durchsucht, wenn die Meldungszeichenfolge eines Ereignisses eine Parameterzeichenfolge enthält. Mit Parametern können Sie lokalisierbare Einfügezeichenfolgen bereitstellen. Weitere Informationen finden Sie unter Hinweise.<br/>                                                                                                                                                |
| Resourcefilename                    | [**Filepath**](eventmanifestschema-filepath-simpletype.md)       | Der vollständige Pfad zu der Datei, die die Metadatenressourcen des Anbieters enthält. Die Datei kann eine ausführbare Datei oder DLL-Datei sein.<br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| source                              |                                                                   | Nur zur internen Verwendung.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Symbol                              | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Das Symbol, das verwendet werden soll, um auf die GUID des Anbieters in Ihrer Anwendung zu verweisen. Der [**Nachrichtencompiler (MC.exe)**](message-compiler--mc-exe-.md) verwendet das -Symbol, um eine Konstante für die GUID des Anbieters in der Headerdatei zu erstellen, die der Compiler generiert.<br/>                                                                                                                                                                                                                                                                           |
| warnOnApplicationCompatibilityError | **xs:boolean**                                                    | Nur zur internen Verwendung.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



## <a name="remarks"></a>Hinweise

Die Windows Ereignisanzeige (Eventvwr.exe) verwendet die lokalisierte Meldungszeichenfolge, falls verfügbar. Andernfalls wird die Zeichenfolge aus dem Namensattribut verwendet.

Die Pfade für resourceFileName, messageFileName und parameterFileName können Umgebungsvariablen enthalten. Wenn Sie eine neue Umgebungsvariable definieren, die im Pfad verwendet werden soll, müssen Sie den Computer neu starten, damit der Ereignisprotokolldienst die neue Variable verwenden kann. Andernfalls kann der Dienst die Ressourcen Ihres Anbieters nicht finden.

Die Meldungszeichenfolge eines Ereignisses kann Einfügezeichenfolgen und Parameterzeichenfolgen enthalten. Eine Einfügezeichenfolge hat das Formular %*n,* wobei *n* ein 1-basierter Index ist, der ein Datenelement aus der Datenvorlage des Ereignisses identifiziert, das Sie in die Nachricht einfügen möchten. Eine Parameterzeichenfolge (siehe **parameterFileName-Attribut)** hat das Format %%*n,* wobei n der Bezeichner einer Nachricht in der Meldungstabelle ist. Wenn die Meldungszeichenfolge des Ereignisses "%1 %%11 = %2 %%12" enthält und die Datenelementwerte für %1 bzw. %2 8 bzw. 2 sind und die Parameterzeichenfolgen für %%11 bzw. %%12 "quarts" bzw. "quartns" sind, wäre die formatierte Zeichenfolge "8 quarts = 2 churns".

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

