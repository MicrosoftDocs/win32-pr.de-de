---
description: Gibt den Downloadspeicherort für eine wsdl:import-Direktive an, die keinen Speicherort explizit angibt.
ms.assetid: 81d0a30b-8f15-4518-b833-de57e0dae978
title: importHint-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a29fcd65f9af02b8077ba828081ac9ed767d64e3
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380654"
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
| [**Lage**](location.md)<br/>   | Der Speicherort der zu importierende Datei. Der Speicherort kann ein relativer Pfad, ein absoluter Pfad oder eine HTTP-URL sein.<br/> <br/> |
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
| [**Wsdl**](wsdl.md)<br/> | Gibt eine WSDL-Datei an, die für Vertragsinformationen verarbeitet werden soll.<br/> <br/> |



## <a name="element-information"></a>Elementinformationen



|                                     |               |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Nein            |



 

 




