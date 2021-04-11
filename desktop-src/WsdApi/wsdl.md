---
description: Gibt eine WSDL-Datei an, die für Vertragsinformationen verarbeitet werden soll.
ms.assetid: d8f630cd-0541-431b-86a8-792846a85ea0
title: WSDL-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb54f946f32fb4962b8384dea7c6cf4b3c0ebe3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216151"
---
# <a name="wsdl-element"></a>WSDL-Element

Gibt eine WSDL-Datei an, die für Vertragsinformationen verarbeitet werden soll.

## <a name="usage"></a>Verbrauch

``` syntax
<wsdl>
  child elements
</wsdl>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                           | BESCHREIBUNG                                                                                                                                       |
|---------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [**excludeimport**](excludeimport.md)<br/> | Verhindert die Generierung von Import-Anweisungen für angegebene Ziele, die in einem <WSDL: Import>-Element in einer WSDL-Datei genannt werden. <br/> <br/> |
| [**importhint**](importhint.md)<br/>       | Gibt den Download Speicherort für eine <WSDL: Import-> Direktive an, die nicht explizit einen Speicherort angibt.<br/> <br/>           |
| [**path**](path.md)<br/>                   | Die Datei und der Pfad der WSDL-Eingabedatei.<br/> <br/>                                                                                      |



### <a name="child-element-sequence"></a>Sequenz untergeordneter Elemente

``` syntax
(
  importHint*, 
  excludeImport*, 
  path
)
```

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                     | BESCHREIBUNG                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [**wsdcodegen**](wsdcodegen.md)<br/> | Das Stamm Element einer XML-Skriptdatei des WSDAPI-Code-Generators.<br/> <br/> |



## <a name="remarks"></a>Bemerkungen

Alle [**importhint**](importhint.md) -oder [**excludeimport**](excludeimport.md) -Elemente, die nach dem [**path**](path.md) -Element in einer XML-Konfigurationsdatei angezeigt werden, werden ignoriert.

## <a name="element-information"></a>Elementinformationen



|                                     |               |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Nein            |



 

 




