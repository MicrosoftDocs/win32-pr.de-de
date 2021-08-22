---
description: Gibt eine WSDL-Datei an, die für Vertragsinformationen verarbeitet werden soll.
ms.assetid: d8f630cd-0541-431b-86a8-792846a85ea0
title: wsdl-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 158141fb8afdc216c47639f6bbb50c1d399e25f202ebbdd2f0a2c045859bffb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049518"
---
# <a name="wsdl-element"></a>wsdl-Element

Gibt eine WSDL-Datei an, die für Vertragsinformationen verarbeitet werden soll.

## <a name="usage"></a>Verwendung

``` syntax
<wsdl>
  child elements
</wsdl>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                           | Beschreibung                                                                                                                                       |
|---------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [**excludeImport**](excludeimport.md)<br/> | Verhindert die Generierung von Importanweisungen für angegebene Ziele, die in einem \<wsdl:import> -Element in einer WSDL-Datei benannt sind. <br/> <br/> |
| [**importHint**](importhint.md)<br/>       | Gibt den Downloadspeicherort für eine \<wsdl:import> -Direktive an, die nicht explizit einen Speicherort angibt.<br/> <br/>           |
| [**Pfad**](path.md)<br/>                   | Datei und Pfad der WSDL-Eingabedatei.<br/> <br/>                                                                                      |



### <a name="child-element-sequence"></a>Sequenz untergeordneter Elemente

``` syntax
(
  importHint*, 
  excludeImport*, 
  path
)
```

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                     | Beschreibung                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [**wsdCodeGen**](wsdcodegen.md)<br/> | Das Stammelement einer WSDAPI-Codegenerator-XML-Skriptdatei.<br/> <br/> |



## <a name="remarks"></a>Hinweise

Alle [**importHint-**](importhint.md) oder [**excludeImport-Elemente,**](excludeimport.md) die nach dem [**Path-Element**](path.md) in einer XML-Konfigurationsdatei angezeigt werden, werden ignoriert.

## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Nein            |



 

 




