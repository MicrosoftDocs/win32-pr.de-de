---
description: Generiert Implementierungen für die Funktionen QueryInterface, adressf und Release.
ms.assetid: 4b6abd0b-7570-4ae0-a727-cdb6cec58daf
title: Iunknowndefinitions-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57ca92338e3dc97a12e04228510fc17eb2ef2483
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348912"
---
# <a name="iunknowndefinitions-element"></a>Iunknowndefinitions-Element

Generiert Implementierungen für die Funktionen QueryInterface, adressf und Release.

## <a name="usage"></a>Verbrauch

``` syntax
<IUnknownDefinitions
  proxyClass = "character_string"
  refCountVar = "character_string">
  child elements
</IUnknownDefinitions>
```

## <a name="attributes"></a>Attribute



| Attribut                  | type                         | Erforderlich       | BESCHREIBUNG                                                |
|----------------------------|------------------------------|----------------|------------------------------------------------------------|
| **proxyClass**<br/>  | Zeichen \_ Folge<br/> | Ja<br/> | Der Name der implementierenden Klasse.<br/> <br/> |
| **Ref-Datei**<br/> | Zeichen \_ Folge<br/> | Ja<br/> | Der Verweis Zähler-Variablenname.<br/> <br/>  |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                   | BESCHREIBUNG                                                                        |
|-------------------------------------------|------------------------------------------------------------------------------------|
| [**Schnittstelle**](interface.md)<br/> | Der Name der Schnittstelle, die von QueryInterface zurückgegeben werden soll.<br/> <br/> |



### <a name="child-element-sequence"></a>Sequenz untergeordneter Elemente

``` syntax
interface
```

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                         | BESCHREIBUNG                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**Datei**](file.md)<br/> | Gibt eine Datei aus dem Code-Generator aus.<br/> <br/> |



## <a name="element-information"></a>Elementinformationen



|                                     |               |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Nein            |



 

 




