---
description: Das Stammelement einer WSDAPI-Codegenerator-XML-Skriptdatei.
ms.assetid: 3d40172b-6ba1-4e42-9a1a-519c8e88c2b1
title: wsdCodeGen-Element
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9861617854e0e75575f2993717f5b2a86515fb0f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994677"
---
# <a name="wsdcodegen-element"></a>wsdCodeGen-Element

Das Stammelement einer WSDAPI-Codegenerator-XML-Skriptdatei.

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
| **ConfigFileVersion**<br/> | Eine beliebige Zeichenfolge.<br/> | Ja<br/> | Die Version der Konfigurationsdatei. Der einzige gültige Wert ist "1.0".<br/> <br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                         | BESCHREIBUNG                                                                                                                                                                                                                 |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**autoStatic**](autostatic.md)<br/>                     | Gibt an, ob WsdCodeGen versuchen soll, bestimmte generierte Felder automatisch als statisch zu kennzeichnen. Diese Einstellung ist standardmäßig aktiviert.<br/> <br/>                                                                 |
| [**Datei**](file.md)<br/>                                 | Weist den Codegenerator an, eine Datei zu generieren.<br/> <br/>                                                                                                                                                       |
| [**hostMetadata**](hostmetadata.md)<br/>                 | Die Hostingmetadaten für das zu implementierende Gerät. Dieses Element wird nur für Geräteimplementierungen (Hosts) verwendet.<br/> <br/>                                                                                 |
| [**layerNumber**](layernumber.md)<br/>                   | Die Nummer der zu generierenden Codeebene. Ebenennummern werden in Laufzeittabellen verwendet, um eine Codeebene für eine andere zu unterscheiden. WSDAPI selbst verwendet generierten Code, der über eine Ebenennummer von 0 verfügt.<br/> <br/> |
| [**layerPrefix**](layerprefix.md)<br/>                   | Das Präfix, das im generierten Code verwendet werden soll, um die Eindeutigkeit generierter Symbole sicherzustellen. WSDAPI verwendet das Präfix "WSD".<br/> <br/>                                                                                     |
| [**Makro**](macro.md)<br/>                               | Definiert Text oder CDATA, der vom include-Element wiederverwendet [**werden**](include.md) soll.<br/> <br/>                                                                                                                        |
| [**Namespace**](namespace.md)<br/>                       | Beschreibt einen Namespace, der für die Codegenerierung verwendet werden soll.<br/> <br/>                                                                                                                                                |
| [**relationshipMetadata**](relationshipmetadata.md)<br/> | Beschreibt den Host und die gehosteten Metadaten für das Gerät.<br/> <br/>                                                                                                                                               |
| [**thisModelMetadata**](thismodelmetadata.md)<br/>       | Die Hersteller- und Modellmetadaten für das zu implementierte Gerät. Dieses Element wird nur für Geräteimplementierungen (Hosts) verwendet.<br/> <br/>                                                                  |
| [**Wsdl**](wsdl.md)<br/>                                 | Gibt eine WSDL-Datei an, die für Vertragsinformationen zu verarbeiten ist.<br/> <br/>                                                                                                                                           |
| [**Xsd**](xsd.md)<br/>                                   | Gibt eine XSD-Datei an, die für Vertragsinformationen zu verarbeiten ist.<br/> <br/>                                                                                                                                           |



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

## <a name="remarks"></a>Hinweise

Im Allgemeinen sollten [**Dateielemente**](file.md) zuletzt auftreten, da sie Code generieren, der die von den anderen Elementen angegebenen Daten verwendet.

## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




