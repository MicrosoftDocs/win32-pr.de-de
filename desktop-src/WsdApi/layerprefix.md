---
description: Definiert das Präfix, das im generierten Code verwendet werden soll, um die Eindeutigkeit der generierten Symbole sicherzustellen.
ms.assetid: 50cb443a-15ae-4f8f-b5f7-b8708810a6c3
title: layerPrefix-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98970013c72600affd7d4d9e7a71781f477cd87d
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994697"
---
# <a name="layerprefix-element"></a>layerPrefix-Element

Definiert das Präfix, das im generierten Code verwendet werden soll, um die Eindeutigkeit der generierten Symbole sicherzustellen.

## <a name="usage"></a>Verbrauch

``` syntax
<layerPrefix/>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente

Es gibt keine untergeordneten Elemente.

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                     | BESCHREIBUNG                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [**wsdCodeGen**](wsdcodegen.md)<br/> | Das Stammelement einer WSDAPI-Codegenerator-XML-Skriptdatei.<br/> <br/> |



## <a name="remarks"></a>Hinweise

Jedes Codegeneratorskript sollte eine eindeutige Präfixzeichenfolge für die erstellten Module definieren. Beispielsweise verwenden die Picture Frame-Skripts das Präfix "PFDEMO".

WSDAPI verwendet das Präfix "WSD".

## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




