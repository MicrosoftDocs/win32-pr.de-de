---
description: Generiert C-Strukturdefinitionen für bekannte Typen.
ms.assetid: 38ba2e8a-d5b1-47b2-b410-ae161f5039bf
title: structDefinitions-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c4c8ad894a42bbafd183031849e458ad5f3bf155a9ccba4e704321e875163c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119611560"
---
# <a name="structdefinitions-element"></a>structDefinitions-Element

Generiert C-Strukturdefinitionen für bekannte Typen.

## <a name="usage"></a>Verwendung

``` syntax
<structDefinitions/>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente

Es gibt keine untergeordneten Elemente.

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                         | Beschreibung                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**Datei**](file.md)<br/> | Gibt eine Datei aus dem Codegenerator aus.<br/> <br/> |



## <a name="remarks"></a>Hinweise

Auf Strukturen für bekannte Typen wird durch einen großen Teil des generierten Codes und durch Anwendungscode verwiesen. Dieses Element wird verwendet, um Includedateien zu generieren. Dieses Element sollte nach einem [**structDeclarations-Element**](structdeclarations.md) auftreten, damit Verweise zwischen Strukturen ordnungsgemäß behandelt werden.

## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




