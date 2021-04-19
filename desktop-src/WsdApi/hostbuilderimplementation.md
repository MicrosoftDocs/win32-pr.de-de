---
description: Generiert eine Funktion, mit der ein typisierter Host erstellt wird.
ms.assetid: 2b4a4016-cc5d-4912-8e08-ce3a11ab0a06
title: hostbuilderimplementation-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c9cfabb9ab4193162044420fc3980f0bbeeb55a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345867"
---
# <a name="hostbuilderimplementation-element"></a>hostbuilderimplementation-Element

Generiert eine Funktion, mit der ein typisierter Host erstellt wird.

## <a name="usage"></a>Verbrauch

``` syntax
<hostBuilderImplementation>
  child elements
</hostBuilderImplementation>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                           | BESCHREIBUNG                                                      |
|---------------------------------------------------|------------------------------------------------------------------|
| [**hostedservice "**](hostedservice.md)<br/> | Der Dienst, der für den Host eingeschlossen werden soll. <br/> <br/> |



### <a name="child-element-sequence"></a>Sequenz untergeordneter Elemente

``` syntax
hostedService+
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



 

 




