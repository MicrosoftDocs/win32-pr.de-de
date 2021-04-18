---
description: 'Gibt den Download Speicherort für eine <WSDL: Import-> Direktive an, die nicht explizit einen Speicherort angibt.'
ms.assetid: 81d0a30b-8f15-4518-b833-de57e0dae978
title: importhint-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce8da0a7fa45ed00489d405aaba8f1f6d7ab8fdf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347911"
---
# <a name="importhint-element"></a>importhint-Element

Gibt den Download Speicherort für eine <WSDL: Import-> Direktive an, die nicht explizit einen Speicherort angibt.

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
| [**location**](location.md)<br/>   | Der Speicherort der zu importierenden Datei. Der Speicherort kann ein relativer Pfad, ein absoluter Pfad oder eine HTTP-URL sein.<br/> <br/> |
| [**Namespace**](namespace.md)<br/> | Der zu importierende Namespace. Dies sollte dem im <WSDL: Import>-Element angegebenen Namespace entsprechen.<br/> <br/>     |



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
| [**WSDL**](wsdl.md)<br/> | Gibt eine WSDL-Datei an, die für Vertragsinformationen verarbeitet werden soll.<br/> <br/> |



## <a name="element-information"></a>Elementinformationen



|                                     |               |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Nein            |



 

 




