---
description: Gibt den Downloadspeicherort für eine wsdl:import-Direktive an, die keinen Speicherort explizit angibt.
ms.assetid: 81d0a30b-8f15-4518-b833-de57e0dae978
title: importHint-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c874879ee0a608c100f32a0520a85efe76080cc2
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998757"
---
# <a name="importhint-element"></a>importHint-Element

Gibt den Downloadspeicherort für eine \<wsdl:import> -Direktive an, die nicht explizit einen Speicherort angibt.

## <a name="usage"></a>Verbrauch

``` syntax
<importHint>
  child elements
</importHint>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                   | BESCHREIBUNG                                                                                                                       |
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



| Element                         | BESCHREIBUNG                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------|
| [**Wsdl**](wsdl.md)<br/> | Gibt eine WSDL-Datei an, die für Vertragsinformationen verarbeitet werden soll.<br/> <br/> |



## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Nein            |



 

 




