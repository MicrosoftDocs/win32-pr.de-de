---
title: BUTTONELEMENT.mappingColor
description: Das attribut mappingColor gibt den Farbschlüssel an, der dieses BUTTONELEMENT in BUTTONGROUP identifiziert, oder ruft diesen ab.
ms.assetid: e7b1663c-3263-41d5-9a69-4cf1dcf0fc1f
keywords:
- BUTTONELEMENT.mappingColor Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONELEMENT.mappingColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29badef71eda70782203effb7098c7ee5bc7a62b67d28ccbc9428c74e9473012
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764340"
---
# <a name="buttonelementmappingcolor"></a>BUTTONELEMENT.mappingColor

Das **attribut mappingColor** gibt den Farbschlüssel an, der dieses **BUTTONELEMENT** in **buttongroup** identifiziert, oder ruft diesen ab.

``` syntax
        elementID.mappingColor
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine **Zeichenfolge** mit Lese-/Schreibzugriff, die einen beliebigen Microsoft Internet Explorer Farbwert enthält. Er besitzt keinen Standardwert.

## <a name="remarks"></a>Hinweise

Dieses Attribut gibt die Farbe des Bereichs  in der Zuordnung der SchaltflächengruppeImage an, die diesem Schaltflächenelement entspricht. Alle Klicks auf diesen Bereich werden von diesem Schaltflächenelement verarbeitet.

Wenn eine ungültige Farbe angegeben wird, wird **BUTTONELEMENT** nicht aktiviert.

## <a name="examples"></a>Beispiele

Das folgende Beispiel ist eine vollständige Skindefinitionsdatei, die veranschaulicht, wie einige der **BUTTONELEMENT-Attribute** verwendet werden. Sie finden sie im Beispielverzeichnis, das mit dem SDK installiert wurde.


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
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Farbreferenz**](color-reference.md)
</dt> <dt>

[**BUTTONELEMENT-Element**](buttonelement-element.md)
</dt> <dt>

[**BUTTONGROUP.mappingImage**](buttongroup-mappingimage.md)
</dt> </dl>

 

 





