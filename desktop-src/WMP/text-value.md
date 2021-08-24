---
title: TEXT.value
description: Das Wertattribut gibt den Text an, der im Text-Steuerelement angezeigt wird, oder ruft diesen ab.
ms.assetid: dbc50be2-ee18-4661-a343-9e906879aba0
keywords:
- TEXT.value Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.value
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eef6b17428831a52a0e3cf5b8f8ec3dd7f795d5d4b78e2c4700a6274b877820
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119762860"
---
# <a name="textvalue"></a>TEXT.value

Das  Wertattribut gibt den Text an, der im Text-Steuerelement angezeigt wird, oder ruft diesen ab.

``` syntax
        elementID.value
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine **Zeichenfolge** mit Lese-/Schreibzugriff.

## <a name="remarks"></a>Hinweise

Wenn die Breite des Text-Steuerelements nicht ausreicht, um den bereitgestellten Text zu enthalten, wird der Text zugeschnitten, und es wird eine Auslassungszeichen angezeigt, um die Tatsache zu veranschaulichen. Wenn das **toolTip-Attribut** nicht festgelegt wurde, wird der vollständige Text als QuickInfo angezeigt, wenn der Cursor auf das Steuerelement zeigen soll.

Wenn keine Breite angegeben wird, ist die Standardbreite für das Steuerelement die Breite der Zeichenfolge.

Wenn die Höhe des Steuerelements nicht angegeben ist, beträgt die Standardhöhe eine Zeile.

Wenn das **wordWrap-Attribut** auf TRUE festgelegt ist und die Höhe des Steuerelements ausreicht, um eine andere Textzeile aufzunehmen, wird der Text in eine nachfolgende Zeile umbrochen. Das Umschließen erfolgt nur zwischen Wörtern. Zeilenumbrüche können auch erzwungen werden, wie unter **wordWrap** erläutert.

## <a name="examples"></a>Beispiele

Das folgende Beispiel ist eine vollständige Skindefinitionsdatei, die veranschaulicht, wie die Attribute des **TEXT-Elements** verwendet werden. Sie finden sie im Beispielverzeichnis, das mit dem SDK installiert wurde.


```C++
<THEME>
  <VIEW
    height = "175"
  >
    <TEXT 
      width = "150"
      fontSize = "30"
      hoverFontStyle = "Bold"
      hoverForegroundColor = "red"
      disabledForegroundColor = "#CCCCCC"
      justification = "Center"
      value = "Play"
      cursor = "hand"
      enabled = "wmpenabled:player.controls.play"
      onClick = "JScript: player.URL='https://proseware.com/laure.wma';"
    />
    <TEXT
      top = "50"
      width = "150"
      fontSize = "30"
      hoverFontStyle = "Bold"
      hoverForegroundColor = "red"
      disabledForegroundColor = "#CCCCCC"
      justification = "Center"
      value = "Stop"
      cursor = "hand"
      enabled = "wmpenabled:player.controls.stop"
      onClick = "JScript: player.controls.stop();"
    />
    <TEXT
      top = "100"
      width = "150"
      fontSize = "30"
      hoverFontStyle = "Bold"
      hoverForegroundColor = "red"
      justification = "Center"
      value = "Close"
      cursor = "hand"
      onClick = "JScript: view.close();"
    />
    <TEXT
      top = "30"
      left = "120"
      width = "200"
      fontSize = "20"
      fontStyle = "Underline"
      justification = "Center"
      value = "Volume"
    />
    <TEXT
      top = "60"
      left = "120"
      width = "200"
      fontSize = "40"
      justification = "Center"
      value = "wmpprop:player.settings.volume"
    />
    <TEXT
      top = "65"
      left = "142"
      width = "40"
      fontSize = "30"
      hoverFontStyle = "Bold"
      hoverForegroundColor = "red"
      justification = "Center"
      value = "-"
      cursor = "hand"
      toolTip = "decrease volume"
      onClick = "player.settings.volume = player.settings.volume - 5"
    />
    <TEXT
      top = "65"
      left = "260"
      width = "40"
      fontSize = "30"
      hoverFontStyle = "Bold"
      hoverForegroundColor = "red"
      justification = "Center"
      value = "+"
      cursor = "hand"
      toolTip = "increase volume"
      onClick = "player.settings.volume = player.settings.volume + 5"
    />
    <TEXT
      top = "155"
      width = "300"
      height = "30"
      fontFace = "System"
      backgroundColor = "blue"
      foregroundColor = "white"
      justification = "Center"
      scrolling = "true"
      scrollingAmount = "1"
      scrollingDelay = "50"
      value = "wmpprop:player.status"
    />
  </VIEW>
</THEME>

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**TEXT-Element**](text-element.md)
</dt> <dt>

[**TEXT.toolTip**](text-tooltip.md)
</dt> <dt>

[**TEXT.wordWrap**](text-wordwrap.md)
</dt> </dl>

 

 





