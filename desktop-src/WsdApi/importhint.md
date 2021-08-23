---
description: Gibt den Downloadspeicherort für eine wsdl:import-Direktive an, die nicht explizit einen Speicherort angibt.
ms.assetid: 81d0a30b-8f15-4518-b833-de57e0dae978
title: importHint-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bff41d5f58e8e3041873d6283afc032409855a53013e721efad6c5986c6c6ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119732240"
---
# <a name="importhint-element"></a>importHint-Element

Gibt den Downloadspeicherort für eine \<wsdl:import> -Direktive an, die nicht explizit einen Speicherort angibt.

## <a name="usage"></a>Verwendung

``` syntax
<importHint>
  child elements
</importHint>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                   | Beschreibung                                                                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**Lage**](location.md)<br/>   | Der Speicherort der zu importierenden Datei. Der Speicherort kann ein relativer Pfad, ein absoluter Pfad oder eine HTTP-URL sein.<br/> <br/> |
| [**Namespace**](namespace.md)<br/> | Der zu importierende Namespace. Dies sollte mit dem im -Element angegebenen Namespace \<wsdl:import> übereinstimmen.<br/> <br/>     |



### <a name="child-element-sequence"></a>Sequenz untergeordneter Elemente

``` syntax
(
  nameSpace, 
  location
)
```

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                         | Beschreibung                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------|
| [**Wsdl**](wsdl.md)<br/> | Gibt eine WSDL-Datei an, die für Vertragsinformationen zu verarbeiten ist.<br/> <br/> |



## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Nein            |



 

 




