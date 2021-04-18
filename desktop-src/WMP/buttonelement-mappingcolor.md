---
title: ButtonElement. mappingColor
description: Das mappingColor-Attribut gibt den Farbschlüssel an, der dieses ButtonElement in der ButtonGroup identifiziert, oder ruft ihn ab.
ms.assetid: e7b1663c-3263-41d5-9a69-4cf1dcf0fc1f
keywords:
- ButtonElement. mappingColor-Fenster Media Player
topic_type:
- apiref
api_name:
- BUTTONELEMENT.mappingColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7318f01246578fe8ff34118427c95afb7b3bb098
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365932"
---
# <a name="buttonelementmappingcolor"></a>ButtonElement. mappingColor

Das **mappingColor** -Attribut gibt den Farbschlüssel an, der dieses **ButtonElement** in der **ButtonGroup** identifiziert, oder ruft ihn ab.

``` syntax
        elementID.mappingColor
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese- **/schreibzeichenfolge** mit einem beliebigen Microsoft Internet Explorer-Farbwert. Er besitzt keinen Standardwert.

## <a name="remarks"></a>Bemerkungen

Dieses Attribut gibt die Farbe des Bereichs in der Schaltflächen Gruppe **mappingImage** an, die diesem Schaltflächen Element entspricht. Alle Klicks in diesem Bereich werden von diesem Schaltflächen Element behandelt.

Wenn eine ungültige Farbe angegeben ist, wird das **ButtonElement** nicht aktiviert.

## <a name="examples"></a>Beispiele

Das folgende Beispiel ist eine komplette Skin-Definitionsdatei, die veranschaulicht, wie einige der **ButtonElement** -Attribute verwendet werden. Sie befindet sich im Verzeichnis Samples, das mit dem SDK installiert wurde.


```
<THEME>
  <VIEW
    backgroundImage = "background.bmp"
    titleBar = "False"
  >
    <PLAYER
      URL = "https://proseware.com/mellow.wma"
    />
    <EFFECTS
      id = "myeffects"
      top = "25"
      left = "88"
      width = "180"
      height = "150"
    />
    <BUTTONGROUP
      mappingImage = "map.bmp"
      hoverImage = "hover.bmp"
    >
      <BUTTONELEMENT
        mappingColor = "#00FF00"
        upToolTip = "Next"
        onClick = "JScript:myeffects.next();"
      />
      <BUTTONELEMENT
        mappingColor = "#FF0000"
        upToolTip = "Previous"
        onClick = "JScript:myeffects.previous();"
      />
    </BUTTONGROUP>
  </VIEW>
</THEME>

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Farb Verweis**](color-reference.md)
</dt> <dt>

[**ButtonElement-Element**](buttonelement-element.md)
</dt> <dt>

[**ButtonGroup. mappingImage**](buttongroup-mappingimage.md)
</dt> </dl>

 

 





