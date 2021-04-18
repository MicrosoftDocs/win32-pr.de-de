---
title: Text. Value
description: Das value-Attribut gibt den Text an, der im Text Steuerelement angezeigt wird, oder ruft ihn ab.
ms.assetid: dbc50be2-ee18-4661-a343-9e906879aba0
keywords:
- Text. Value-Fenster Media Player
topic_type:
- apiref
api_name:
- TEXT.value
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d87f688f7afffeb588a37ac13ebff4cdc7cc105
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368504"
---
# <a name="textvalue"></a>Text. Value

Das **value** -Attribut gibt den Text an, der im Text Steuerelement angezeigt wird, oder ruft ihn ab.

``` syntax
        elementID.value
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese- **/schreibzeichenfolge**.

## <a name="remarks"></a>Bemerkungen

Wenn die Breite des Text-Steuer Elements unzureichend ist, um den bereitgestellten Text zu enthalten, wird der Text abgeschnitten, und es wird ein Auslassungs Zeichen angezeigt, um die Tatsache zu veranschaulichen. Wenn das **ToolTip** -Attribut nicht festgelegt wurde, wird der vollständige Text dann als QuickInfo angezeigt, wenn der Cursor über das Steuerelement bewegt wird.

Wenn keine Breite angegeben ist, ist die Standardbreite für das-Steuerelement die Breite der Zeichenfolge.

Wenn die Höhe des Steuer Elements nicht angegeben wird, ist die Standardhöhe eine Zeile.

Wenn das **WordWrap** -Attribut auf "true" festgelegt ist und die Höhe des Steuer Elements ausreichend ist, um eine andere Textzeile aufnehmen zu können, wird der Text in eine nachfolgende Zeile umschlossen. Das umwickeln erfolgt nur zwischen Wörtern. Zeilenumbrüche können auch erzwungen werden, wie unter **WordWrap** erläutert.

## <a name="examples"></a>Beispiele

Das folgende Beispiel ist eine vollständige Skin-Definitionsdatei, die veranschaulicht, wie die Attribute des **Text** -Elements verwendet werden. Sie befindet sich im Verzeichnis Samples, das mit dem SDK installiert wurde.


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
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Text-Element**](text-element.md)
</dt> <dt>

[**Text. ToolTip**](text-tooltip.md)
</dt> <dt>

[**Text. WordWrap**](text-wordwrap.md)
</dt> </dl>

 

 





