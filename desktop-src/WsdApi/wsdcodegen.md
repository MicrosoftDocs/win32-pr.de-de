---
description: Ist das Stamm Element einer XML-Skriptdatei des WSDAPI-Code-Generators.
ms.assetid: 3d40172b-6ba1-4e42-9a1a-519c8e88c2b1
title: wsdcodegen-Element
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 656f2273926dc3420ec84d6b9f24759f8e3587e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353201"
---
# <a name="wsdcodegen-element"></a>wsdcodegen-Element

Ist das Stamm Element einer XML-Skriptdatei des WSDAPI-Code-Generators.

## <a name="usage"></a>Verbrauch

``` syntax
<wsdCodeGen
  ConfigFileVersion = "Any character string.">
  child elements
</wsdCodeGen>
```

## <a name="attributes"></a>Attribute



| Attribut                        | type                             | Erforderlich       | BESCHREIBUNG                                                                                  |
|----------------------------------|----------------------------------|----------------|----------------------------------------------------------------------------------------------|
| **Configfileversion**<br/> | Eine beliebige Zeichenfolge.<br/> | Ja<br/> | Die Version der Konfigurationsdatei. Der einzige gültige Wert ist "1,0".<br/> <br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                         | BESCHREIBUNG                                                                                                                                                                                                                 |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**automatisch statisch**](autostatic.md)<br/>                     | Gibt an, ob wsdcodegen versuchen soll, bestimmte generierte Felder automatisch als statisch zu kennzeichnen. Diese Einstellung ist standardmäßig aktiviert.<br/> <br/>                                                                 |
| [**Datei**](file.md)<br/>                                 | Weist den Code Generator an, eine Datei zu generieren.<br/> <br/>                                                                                                                                                       |
| [**hostmetadata**](hostmetadata.md)<br/>                 | Die hostingmetadaten für das Gerät, das implementiert werden soll. Dieses Element wird nur für Geräte Implementierungen (Hosts) verwendet.<br/> <br/>                                                                                 |
| [**layernumber**](layernumber.md)<br/>                   | Die Anzahl der zu generierenden Code Schicht. Ebenennummern werden in Lauf Zeit Tabellen verwendet, um eine Codeebene für eine andere zu unterscheiden. WSDAPI selbst verwendet generierten Code mit einer Ebenennummer von 0.<br/> <br/> |
| [**layerprefix**](layerprefix.md)<br/>                   | Das Präfix, das im generierten Code verwendet werden soll, um die Eindeutigkeit generierter Symbole sicherzustellen. WSDAPI verwendet das Präfix "WSD".<br/> <br/>                                                                                     |
| [**Hilfen**](macro.md)<br/>                               | Definiert Text oder CDATA, der vom [**include**](include.md) -Element wieder verwendet werden soll.<br/> <br/>                                                                                                                        |
| [**Namespace**](namespace.md)<br/>                       | Beschreibt einen Namespace, der für die Codegenerierung verwendet werden soll.<br/> <br/>                                                                                                                                                |
| [**relationshipmetadata**](relationshipmetadata.md)<br/> | Beschreibt den Host und die gehosteten Metadaten für das Gerät.<br/> <br/>                                                                                                                                               |
| [**thismodelmetadata**](thismodelmetadata.md)<br/>       | Die Hersteller-und Modell Metadaten für das Gerät, das implementiert werden soll. Dieses Element wird nur für Geräte Implementierungen (Hosts) verwendet.<br/> <br/>                                                                  |
| [**WSDL**](wsdl.md)<br/>                                 | Gibt eine WSDL-Datei an, die für Vertragsinformationen verarbeitet werden soll.<br/> <br/>                                                                                                                                           |
| [**XSD**](xsd.md)<br/>                                   | Gibt eine XSD-Datei an, die für Vertragsinformationen verarbeitet werden soll.<br/> <br/>                                                                                                                                           |



### <a name="child-element-sequence"></a>Sequenz untergeordneter Elemente

``` syntax
(
  layerNumber?, 
  layerPrefix?, 
  autoStatic?, 
  hostMetadata?, 
  thisModelMetadata?, 
  nameSpace*, 
  wsdl*, 
  xsd*, 
  file*, 
  macro*, 
  relationshipMetadata*
)
```

## <a name="parent-elements"></a>Übergeordnete Elemente

Es gibt keine übergeordneten Elemente.

## <a name="remarks"></a>Bemerkungen

Im Allgemeinen sollten [**Datei**](file.md) Elemente zuletzt auftreten, da Sie Code generieren, der die von den anderen Elementen angegebenen Daten verwendet.

## <a name="element-information"></a>Elementinformationen



|                                     |               |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




