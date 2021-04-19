---
description: Generiert C-Strukturdefinitionen für bekannte Typen.
ms.assetid: 38ba2e8a-d5b1-47b2-b410-ae161f5039bf
title: structdefinitions-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e33ca9ac9ce3f9e868646c0bfff260238c30e572
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373110"
---
# <a name="structdefinitions-element"></a>structdefinitions-Element

Generiert C-Strukturdefinitionen für bekannte Typen.

## <a name="usage"></a>Verbrauch

``` syntax
<structDefinitions/>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente

Es gibt keine untergeordneten Elemente.

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                         | BESCHREIBUNG                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**Datei**](file.md)<br/> | Gibt eine Datei aus dem Code-Generator aus.<br/> <br/> |



## <a name="remarks"></a>Bemerkungen

Auf Strukturen für bekannte Typen wird von einem Großteil des generierten Codes und des Anwendungs Codes verwiesen. Dieses Element wird zum Generieren von Include-Dateien verwendet. Dieses Element sollte nach einem [**struct-Deklarations**](structdeclarations.md) Element auftreten, sodass Verweise zwischen Strukturen ordnungsgemäß behandelt werden.

## <a name="element-information"></a>Elementinformationen



|                                     |               |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




