---
description: Weist den Code Generator an, eine Datei zu generieren, und gibt den Namen der Ausgabedatei an.
ms.assetid: d2ee6886-995f-453d-8121-f849b2d910ec
title: file-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bc20f7d6853ccd52b231e19c99d60fe4b71d15b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358817"
---
# <a name="file-element"></a>file-Element

Weist den Code Generator an, eine Datei zu generieren, und gibt den Namen der Ausgabedatei an.

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
| **name**<br/> | Pfadnamen-Zeichenfolge<br/> | Ja<br/> | Der Ausgabe Dateiname für den generierten Inhalt. Die Dateinamen Zeichenfolge muss Informationen zum kompletten Pfad enthalten.<br/> <br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                                 | BESCHREIBUNG                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CDATA**<br/>                                                                                    | Text-und CDATA-Abschnitte werden ohne Änderung in die Datei kopiert. Der Quellcode, der keine Funktion der Vertrags Eingabedaten ist, kann Ausgabedateien mithilfe von Text-und CDATA-Abschnitten hinzugefügt werden.<br/> <br/> |
| [**enumerationvaluedeklarationen**](enumerationvaluedeclarations.md)<br/>                         | Generiert C-Deklarationen für Werte aller Enumerationstypen.<br/> <br/>                                                                                                                                   |
| [**eventsourcebuilderdeklarationen**](eventsourcebuilderdeclarations.md)<br/>                     | Generiert Deklarationen für Funktionen, die Ereignis Quell Klassen erstellen.<br/> <br/>                                                                                                                         |
| [**eventsourcebuilderimplementierungen**](eventsourcebuilderimplementations.md)<br/>               | Generiert Funktionen, die Ereignis Quell Klassen erstellen.<br/> <br/>                                                                                                                                          |
| [**functiondeklarationen**](functiondeclarations.md)<br/>                                         | Generiert Implementierungs Deklarationen für Proxy Funktionen für Porttyp Vorgänge.<br/> <br/>                                                                                                            |
| [**hostbuilderdeclaration**](hostbuilderdeclaration.md)<br/>                                     | Generiert eine Deklaration für eine Funktion, mit der ein typisierter Host erstellt wird.<br/> <br/>                                                                                                                              |
| [**hostbuilderimplementation**](hostbuilderimplementation.md)<br/>                               | Generiert eine Funktion, mit der ein typisierter Host erstellt wird.<br/> <br/>                                                                                                                                                |
| [**idlfunctiondeklarationen**](idlfunctiondeclarations.md)<br/>                                   | Generiert IDL-Deklarationen für Proxy Funktionen für Porttyp Vorgänge.<br/> <br/>                                                                                                                       |
| [**darunter**](include.md)<br/>                                                                   | Schließt den Inhalt eines Makros oder einer Datei in die generierte Ausgabe ein.<br/> <br/>                                                                                                                              |
| [**Iunknowndeklarationen**](iunknowndeclarations.md)<br/>                                         | Generiert Deklarationen für QueryInterface, adressf und Release.<br/> <br/>                                                                                                                                 |
| [**Iunknowndefinitions**](iunknowndefinitions.md)<br/>                                           | Generiert Implementierungen für QueryInterface, adressf und Release.<br/> <br/>                                                                                                                              |
| [**literalinclude**](literalinclude.md)<br/>                                                     | Fügt eine C-oder IDL-include-Anweisung in den generierten Code ein. <br/> <br/>                                                                                                                                    |
| [**messagestructuredefinitions**](messagestructuredefinitions.md)<br/>                           | Generiert C-Strukturdefinitionen für Nachrichten Typen.<br/> <br/>                                                                                                                                           |
| [**messagetypedeklarationen**](messagetypedeclarations.md)<br/>                                   | Generiert C-Konstante Deklarationen für XML-Schema Tabellen für Nachrichten Typen.<br/> <br/>                                                                                                                     |
| [**messagetypedefinitions**](messagetypedefinitions.md)<br/>                                     | Generiert C-Konstanten für XML-Schema Tabellen für Nachrichten Typen.<br/> <br/>                                                                                                                                 |
| [**Namespacedeklarationen**](namespacedeclarations.md)<br/>                                       | Generiert C-Deklarationen für Namespace Tabellen.<br/> <br/>                                                                                                                                                 |
| [**namespacedefinitions**](namespacedefinitions.md)<br/>                                         | Generiert C-Definitionen für Namespace Tabellen.<br/> <br/>                                                                                                                                                  |
| [**porttypeer-Deklarationen**](porttypedeclarations.md)<br/>                                         | Generiert C-Konstante Deklarationen für Porttypen.<br/> <br/>                                                                                                                                              |
| [**porttypeer Definitionen**](porttypedefinitions.md)<br/>                                           | Generiert C-Konstanten für Porttypen.<br/> <br/>                                                                                                                                                          |
| [**proxybuilderdeklarationen**](proxybuilderdeclarations.md)<br/>                                 | Generiert Deklarationen für Funktionen zum Erstellen typisierter Proxys.<br/> <br/>                                                                                                                                  |
| [**proxybuilderimplementierungen**](proxybuilderimplementations.md)<br/>                           | Generiert Funktionen zum Erstellen typisierter Proxys.<br/> <br/>                                                                                                                                                   |
| [**proxyfunctionimplementierungen**](proxyfunctionimplementations.md)<br/>                         | Generiert Implementierungen für Proxy Funktionen für Porttyp Vorgänge.<br/> <br/>                                                                                                                        |
| [**relationshipMetadataDeclaration**](relationshipmetadatadeclaration.md)<br/>                   | Generiert eine vorwärts Deklaration für die hostmetadatenelemente, die im [**hostmetadata**](hostmetadata.md) -Element angegeben sind. <br/> <br/>                                                                       |
| [**relationshipMetadataDefinition**](relationshipmetadatadefinition.md)<br/>                     | Generiert eine C-Konstantendefinition für die hostmetadatenelemente, die im [**hostmetadata**](hostmetadata.md) -Element angegeben sind. <br/> <br/>                                                                     |
| [**structdeklarationen**](structdeclarations.md)<br/>                                             | Generiert C-Struktur Deklarationen für bekannte Typen.<br/> <br/>                                                                                                                                            |
| [**structdefinitions**](structdefinitions.md)<br/>                                               | Generiert C-Strukturdefinitionen für bekannte Typen.<br/> <br/>                                                                                                                                             |
| [**stubdeklarationen**](stubdeclarations.md)<br/>                                                 | Generiert Deklarationen für Stub-Funktionen für Porttyp Vorgänge.<br/> <br/>                                                                                                                            |
| [**stubdefinitionen**](stubdefinitions.md)<br/>                                                   | Generiert Implementierungen für Stub-Funktionen für Porttyp Vorgänge.<br/> <br/>                                                                                                                         |
| [**"abonnemenfunctiondeklarationen"**](subscriptionfunctiondeclarations.md)<br/>                 | Generiert Implementierungs Deklarationen für Abonnement-/abonnementproxyfunktionen für Porttyp-Benachrichtigungs Vorgänge.<br/> <br/>                                                                         |
| [**"abonnemenidlfunctiondeklarationen"**](subscriptionidlfunctiondeclarations.md)<br/>           | Generiert IDL-Deklarationen für Abonnement-/abonnementproxyfunktionen für Port-Benachrichtigungs Vorgänge.<br/> <br/>                                                                                    |
| [**abonnemenproxyfunctionimplementierungen**](subscriptionproxyfunctionimplementations.md)<br/> | Generiert Implementierungen für Abonnement-/Abonnement-Proxyfunktionen für Porttyp-Benachrichtigungs Vorgänge.<br/> <br/>                                                                                     |
| **text**<br/>                                                                                     | Text-und CDATA-Abschnitte werden ohne Änderung in die Datei kopiert. Der Quellcode, der keine Funktion der Vertrags Eingabedaten ist, kann Ausgabedateien mithilfe von Text-und CDATA-Abschnitten hinzugefügt werden.<br/> <br/> |
| [**thisModelMetadataDeclaration**](thismodelmetadatadeclaration.md)<br/>                         | Generiert eine vorwärts Deklaration für die C-Konstante für die im [**thismodelmetadata**](thismodelmetadata.md) -Element angegebenen Hersteller Metadaten.<br/> <br/>                                      |
| [**thisModelMetadataDefinition**](thismodelmetadatadefinition.md)<br/>                           | Generiert eine C-Konstante für die im [**thismodelmetadata**](thismodelmetadata.md) -Element angegebenen Hersteller Metadaten.<br/> <br/>                                                                  |
| [**typetable-Deklarationen**](typetabledeclarations.md)<br/>                                       | Generiert C-Konstante Deklarationen für XML-Schema Tabellen für bekannte Typen.<br/> <br/>                                                                                                                       |
| [**typetabledefinitions**](typetabledefinitions.md)<br/>                                         | Generiert C-Konstanten für XML-Schema Tabellen für bekannte Typen.<br/> <br/>                                                                                                                                   |



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
| [**wsdcodegen**](wsdcodegen.md)<br/> | Das Stamm Element einer XML-Skriptdatei des WSDAPI-Code-Generators.<br/> <br/> |



## <a name="remarks"></a>Bemerkungen

Der Name der Datei wird durch den Wert des Namens Attributs oder untergeordneten Elements bestimmt. Der Inhalt der Datei wird von den anderen untergeordneten Elementen, Text und CDATA im **File** -Element bestimmt. Text und CDATA werden unverändert in die Datei kopiert. Untergeordnete Elemente werden durch generierten Code ersetzt. Text, CDATA und untergeordnete Elemente können in beliebiger Reihenfolge auftreten und können unbegrenzt wiederholt werden.

## <a name="element-information"></a>Elementinformationen



|                                     |               |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Nein            |



 

 




