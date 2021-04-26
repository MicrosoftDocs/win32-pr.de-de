---
description: Generiert Implementierungen für die Funktionen QueryInterface, AddRef und Release.
ms.assetid: 4b6abd0b-7570-4ae0-a727-cdb6cec58daf
title: IUnknownDefinitions-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb3a4f76145e585411e64c10ea7af922db931846
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995147"
---
# <a name="iunknowndefinitions-element"></a>IUnknownDefinitions-Element

Generiert Implementierungen für die Funktionen QueryInterface, AddRef und Release.

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
| **proxyClass**<br/>  | \_Zeichenfolge<br/> | Ja<br/> | Der Name der implementierenden Klasse.<br/> <br/> |
| **refCountVar**<br/> | \_Zeichenfolge<br/> | Ja<br/> | Der Name der Verweisanzahlvariablen.<br/> <br/>  |



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
| [**Datei**](file.md)<br/> | Gibt eine Datei aus dem Codegenerator aus.<br/> <br/> |



## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Nein            |



 

 




