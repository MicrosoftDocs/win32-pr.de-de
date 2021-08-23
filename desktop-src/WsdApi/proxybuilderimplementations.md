---
description: Generiert Funktionen zum Erstellen typisierter Proxys.
ms.assetid: 75a686ba-8112-4093-8a1b-13419018aa3a
title: proxyBuilderImplementations-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d18b13ddda25d8fa157b0399c7b9fba070534fb66e11b3fa63a122b1983dea06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118815532"
---
# <a name="proxybuilderimplementations-element"></a>proxyBuilderImplementations-Element

Generiert Funktionen zum Erstellen typisierter Proxys.

## <a name="usage"></a>Verwendung

``` syntax
<proxyBuilderImplementations>
  child elements
</proxyBuilderImplementations>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                     | Beschreibung                                                                                                                                                     |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Codename**](codename.md)<br/>     | Der Name, der für den Porttyp im generierten Code verwendet werden soll. Standardmäßig wird der Codename aus dem qualifizierten Namen des Porttyps generiert.<br/> <br/> |
| [**Porttype**](porttype.md)<br/>     | Porttyp, für den Code generiert werden soll.<br/> <br/>                                                                                             |
| [**proxyClass**](proxyclass.md)<br/> | Klassenname, der aus der Proxy-Generatorfunktion generiert werden soll.<br/> <br/>                                                                                  |



### <a name="child-element-sequence"></a>Sequenz untergeordneter Elemente

``` syntax
(
  proxyClass, 
  portType+, 
  codeName
)
```

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                         | Beschreibung                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**Datei**](file.md)<br/> | Gibt eine Datei aus dem Codegenerator aus.<br/> <br/> |



## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Nein            |



 

 




