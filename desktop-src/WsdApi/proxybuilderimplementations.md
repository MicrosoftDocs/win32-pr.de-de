---
description: Generiert Funktionen zum Erstellen typisierter Proxys.
ms.assetid: 75a686ba-8112-4093-8a1b-13419018aa3a
title: proxybuilderimplementierungen-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d2cb64a6ea87b1083871931359a4f7c01ece9b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352234"
---
# <a name="proxybuilderimplementations-element"></a>proxybuilderimplementierungen-Element

Generiert Funktionen zum Erstellen typisierter Proxys.

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
| [**codeName**](codename.md)<br/>     | Der Name, der für den Porttyp im generierten Code verwendet werden soll. Standardmäßig wird der Codename aus dem qualifizierten Namen des Porttyps generiert.<br/> <br/> |
| [**PortType**](porttype.md)<br/>     | Der Porttyp, für den Code generiert werden soll.<br/> <br/>                                                                                             |
| [**proxyClass**](proxyclass.md)<br/> | Der Klassenname, der aus der Proxy Generatorfunktion generiert werden soll.<br/> <br/>                                                                                  |



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
| [**Datei**](file.md)<br/> | Gibt eine Datei aus dem Code-Generator aus.<br/> <br/> |



## <a name="element-information"></a>Elementinformationen



|                                     |               |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Nein            |



 

 




