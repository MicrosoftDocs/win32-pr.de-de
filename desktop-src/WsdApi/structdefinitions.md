---
description: Generiert C-Strukturdefinitionen für bekannte Typen.
ms.assetid: 38ba2e8a-d5b1-47b2-b410-ae161f5039bf
title: structDefinitions-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26f680db18b06253362f932cc7d34d5b85f7c1b5
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996457"
---
# <a name="structdefinitions-element"></a>structDefinitions-Element

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
| [**Datei**](file.md)<br/> | Gibt eine Datei aus dem Codegenerator aus.<br/> <br/> |



## <a name="remarks"></a>Hinweise

Auf Strukturen für bekannte Typen wird von einem Großteil des generierten Codes und von Anwendungscode verwiesen. Dieses Element wird verwendet, um Includedateien zu generieren. Dieses Element sollte nach einem [**structDeclarations-Element**](structdeclarations.md) auftreten, damit Verweise zwischen Strukturen ordnungsgemäß behandelt werden.

## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




