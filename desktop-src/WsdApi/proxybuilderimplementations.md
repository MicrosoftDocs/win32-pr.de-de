---
description: Generiert Funktionen, um typierte Proxys zu erstellen.
ms.assetid: 75a686ba-8112-4093-8a1b-13419018aa3a
title: proxyBuilderImplementations-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ad22348b33c60689adf60c029e3a08c2f4d417c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996467"
---
# <a name="proxybuilderimplementations-element"></a>proxyBuilderImplementations-Element

Generiert Funktionen, um typierte Proxys zu erstellen.

## <a name="usage"></a>Verbrauch

``` syntax
<proxyBuilderImplementations>
  child elements
</proxyBuilderImplementations>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                     | BESCHREIBUNG                                                                                                                                                     |
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



| Element                         | BESCHREIBUNG                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**Datei**](file.md)<br/> | Gibt eine Datei aus dem Codegenerator aus.<br/> <br/> |



## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Nein            |



 

 




