---
description: Leitet den Codegenerator an, eine Datei zu generieren, und gibt den Namen der Ausgabedatei an.
ms.assetid: d2ee6886-995f-453d-8121-f849b2d910ec
title: file-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41970da9cc6e389f4e45c5e55901ce8eb2e7797f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995867"
---
# <a name="file-element"></a>file-Element

Leitet den Codegenerator an, eine Datei zu generieren, und gibt den Namen der Ausgabedatei an.

## <a name="usage"></a>Verbrauch

``` syntax
<file
  name = "pathname string">
  child elements
</file>
```

## <a name="attributes"></a>Attribute



| Attribut           | type                       | Erforderlich       | BESCHREIBUNG                                                                                                                         |
|---------------------|----------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------|
| **name**<br/> | pathname string<br/> | Ja<br/> | Der Ausgabedateiname für den generierten Inhalt. Die Dateinamenzeichenfolge sollte vollständige Pfadinformationen enthalten.<br/> <br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                                 | BESCHREIBUNG                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Cdata**<br/>                                                                                    | Text- und CDATA-Abschnitte werden ohne Änderung in die Datei kopiert. Quellcode, der keine Funktion der Vertragseingabedaten ist, kann Ausgabedateien mithilfe von Text- und CDATA-Abschnitten hinzugefügt werden.<br/> <br/> |
| [**enumerationValueDeclarations**](enumerationvaluedeclarations.md)<br/>                         | Generiert C-Deklarationen für Werte aller aufzählten Typen.<br/> <br/>                                                                                                                                   |
| [**eventSourceBuilderDeclarations**](eventsourcebuilderdeclarations.md)<br/>                     | Generiert Deklarationen für Funktionen, die Ereignisquellenklassen erstellen.<br/> <br/>                                                                                                                         |
| [**eventSourceBuilderImplementations**](eventsourcebuilderimplementations.md)<br/>               | Generiert Funktionen, die Ereignisquellenklassen erstellen.<br/> <br/>                                                                                                                                          |
| [**functionDeclarations**](functiondeclarations.md)<br/>                                         | Generiert Implementierungsdeklarationen für Proxyfunktionen für Porttypvorgänge.<br/> <br/>                                                                                                            |
| [**hostBuilderDeclaration**](hostbuilderdeclaration.md)<br/>                                     | Generiert eine Deklaration für eine Funktion, die einen typierten Host erstellt.<br/> <br/>                                                                                                                              |
| [**hostBuilderImplementation**](hostbuilderimplementation.md)<br/>                               | Generiert eine Funktion, die einen typierten Host erstellt.<br/> <br/>                                                                                                                                                |
| [**idlFunctionDeclarations**](idlfunctiondeclarations.md)<br/>                                   | Generiert IDL-Deklarationen für Proxyfunktionen für Porttypvorgänge.<br/> <br/>                                                                                                                       |
| [**include**](include.md)<br/>                                                                   | Schließt den Inhalt eines Makros oder einer Datei in die generierte Ausgabe ein.<br/> <br/>                                                                                                                              |
| [**IUnknownDeclarations**](iunknowndeclarations.md)<br/>                                         | Generiert Deklarationen für QueryInterface, AddRef und Release.<br/> <br/>                                                                                                                                 |
| [**IUnknownDefinitions**](iunknowndefinitions.md)<br/>                                           | Generiert Implementierungen für QueryInterface, AddRef und Release.<br/> <br/>                                                                                                                              |
| [**literalInclude**](literalinclude.md)<br/>                                                     | Platziert eine C- oder IDL-Include-Anweisung im generierten Code. <br/> <br/>                                                                                                                                    |
| [**messageStructureDefinitions**](messagestructuredefinitions.md)<br/>                           | Generiert C-Strukturdefinitionen für Nachrichtentypen.<br/> <br/>                                                                                                                                           |
| [**messageTypeDeclarations**](messagetypedeclarations.md)<br/>                                   | Generiert C-Konstantendeklarationen für XML-Schematabellen für Nachrichtentypen.<br/> <br/>                                                                                                                     |
| [**messageTypeDefinitions**](messagetypedefinitions.md)<br/>                                     | Generiert C-Konstanten für XML-Schematabellen für Nachrichtentypen.<br/> <br/>                                                                                                                                 |
| [**namespaceDeclarations**](namespacedeclarations.md)<br/>                                       | Generiert C-Deklarationen für Namespacetabellen.<br/> <br/>                                                                                                                                                 |
| [**namespaceDefinitions**](namespacedefinitions.md)<br/>                                         | Generiert C-Definitionen für Namespacetabellen.<br/> <br/>                                                                                                                                                  |
| [**portTypeDeclarations**](porttypedeclarations.md)<br/>                                         | Generiert C-Konstantendeklarationen für Porttypen.<br/> <br/>                                                                                                                                              |
| [**portTypeDefinitions**](porttypedefinitions.md)<br/>                                           | Generiert C-Konstanten für Porttypen.<br/> <br/>                                                                                                                                                          |
| [**proxyBuilderDeclarations**](proxybuilderdeclarations.md)<br/>                                 | Generiert Deklarationen für Funktionen, um typierte Proxys zu erstellen.<br/> <br/>                                                                                                                                  |
| [**proxyBuilderImplementations**](proxybuilderimplementations.md)<br/>                           | Generiert Funktionen, um typierte Proxys zu erstellen.<br/> <br/>                                                                                                                                                   |
| [**proxyFunctionImplementations**](proxyfunctionimplementations.md)<br/>                         | Generiert Implementierungen für Proxyfunktionen für Porttypvorgänge.<br/> <br/>                                                                                                                        |
| [**relationshipMetadataDeclaration**](relationshipmetadatadeclaration.md)<br/>                   | Generiert eine Vorwärtsdeklaration für die Hostingmetadaten, die im [**hostMetadata-Element angegeben**](hostmetadata.md) sind. <br/> <br/>                                                                       |
| [**relationshipMetadataDefinition**](relationshipmetadatadefinition.md)<br/>                     | Generiert eine C-Konstantendefinition für die Hostingmetadaten, die im [**hostMetadata-Element angegeben**](hostmetadata.md) sind. <br/> <br/>                                                                     |
| [**structDeclarations**](structdeclarations.md)<br/>                                             | Generiert C-Strukturdeklarationen für bekannte Typen.<br/> <br/>                                                                                                                                            |
| [**structDefinitions**](structdefinitions.md)<br/>                                               | Generiert C-Strukturdefinitionen für bekannte Typen.<br/> <br/>                                                                                                                                             |
| [**stubDeclarations**](stubdeclarations.md)<br/>                                                 | Generiert Deklarationen für Stubfunktionen für Porttypvorgänge.<br/> <br/>                                                                                                                            |
| [**stubDefinitions**](stubdefinitions.md)<br/>                                                   | Generiert Implementierungen für Stubfunktionen für Porttypvorgänge.<br/> <br/>                                                                                                                         |
| [**subscriptionFunctionDeclarations**](subscriptionfunctiondeclarations.md)<br/>                 | Generiert Implementierungsdeklarationen für Subscribe/Unsubscribe-Proxyfunktionen für Porttypbenachrichtigungsvorgänge.<br/> <br/>                                                                         |
| [**subscriptionIdlFunctionDeclarations**](subscriptionidlfunctiondeclarations.md)<br/>           | Generiert IDL-Deklarationen für Subscribe/Unsubscribe-Proxyfunktionen für Porttypbenachrichtigungsvorgänge.<br/> <br/>                                                                                    |
| [**subscriptionProxyFunctionImplementations**](subscriptionproxyfunctionimplementations.md)<br/> | Generiert Implementierungen für Subscribe/Unsubscribe-Proxyfunktionen für Porttypbenachrichtigungsvorgänge.<br/> <br/>                                                                                     |
| **text**<br/>                                                                                     | Die Abschnitte Text und CDATA werden ohne Änderungen in die Datei kopiert. Quellcode, der keine Funktion der Vertragseingabedaten ist, kann Ausgabedateien mithilfe von Text- und CDATA-Abschnitten hinzugefügt werden.<br/> <br/> |
| [**thisModelMetadataDeclaration**](thismodelmetadatadeclaration.md)<br/>                         | Generiert eine Vorwärtsdeklaration für die C-Konstante für die im [**thisModelMetadata-Element**](thismodelmetadata.md) angegebenen Herstellermetadaten.<br/> <br/>                                      |
| [**thisModelMetadataDefinition**](thismodelmetadatadefinition.md)<br/>                           | Generiert eine C-Konstante für die im [**thisModelMetadata-Element**](thismodelmetadata.md) angegebenen Herstellermetadaten.<br/> <br/>                                                                  |
| [**typeTableDeclarations**](typetabledeclarations.md)<br/>                                       | Generiert C-Konstantendeklarationen für XML-Schematabellen für bekannte Typen.<br/> <br/>                                                                                                                       |
| [**typeTableDefinitions**](typetabledefinitions.md)<br/>                                         | Generiert C-Konstanten für XML-Schematabellen für bekannte Typen.<br/> <br/>                                                                                                                                   |



### <a name="child-element-sequence"></a>Sequenz untergeordneter Elemente

``` syntax
(
  text, 
  CDATA, 
  namespaceDeclarations*, 
  namespaceDefinitions*, 
  structDeclarations*, 
  structDefinitions*, 
  typeTableDeclarations*, 
  typeTableDefinitions*, 
  thisModelMetadataDeclaration*, 
  thisModelMetadataDefinition*, 
  portTypeDeclarations*, 
  portTypeDefinitions*, 
  messageStructureDefinitions*, 
  messageTypeDeclarations*, 
  messageTypeDefinitions*, 
  idlFunctionDeclarations*, 
  subscriptionIdlFunctionDeclarations*, 
  functionDeclarations*, 
  subscriptionFunctionDeclarations*, 
  proxyFunctionImplementations*, 
  subscriptionProxyFunctionImplementations*, 
  stubDeclarations*, 
  stubDefinitions*, 
  enumerationValueDeclarations*, 
  include*, 
  IUnknownDeclarations*, 
  IUnknownDefinitions*, 
  relationshipMetadataDeclaration*, 
  relationshipMetadataDefinition*, 
  proxyBuilderDeclarations*, 
  proxyBuilderImplementations*, 
  hostBuilderDeclaration*, 
  hostBuilderImplementation*, 
  eventSourceBuilderDeclarations*, 
  eventSourceBuilderImplementations*, 
  literalInclude*
)
```

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                     | BESCHREIBUNG                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [**wsdCodeGen**](wsdcodegen.md)<br/> | Das Stammelement einer WSDAPI-Codegenerator-XML-Skriptdatei.<br/> <br/> |



## <a name="remarks"></a>Hinweise

Der Name der Datei wird durch den Wert des Namensattributs oder untergeordneten Elements bestimmt. Der Inhalt der Datei wird durch die anderen untergeordneten Elemente text und CDATA im **Dateielement** bestimmt. Text und CDATA werden unverändert in die Datei kopiert. Untergeordnete Elemente werden durch generierten Code ersetzt. Text, CDATA und untergeordnete Elemente können in beliebiger Reihenfolge auftreten und unbegrenzt wiederholt werden.

## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Nein            |



 

 




