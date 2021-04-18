---
title: Customslider. positionImage
description: Das positionImage-Attribut gibt die ImageMap an oder ruft Sie ab, um zu bestimmen, welches Positions Bild aus der Bilddatei angezeigt werden soll.
ms.assetid: 7e99dc21-ebba-438a-a983-190dbe429578
keywords:
- Windows-Media Player "customslider. positionImage"
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.positionImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dc92a9c263e2b450e64d526ccfc7976fdd6227a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365373"
---
# <a name="customsliderpositionimage"></a>Customslider. positionImage

Das **positionImage** -Attribut gibt die ImageMap an oder ruft Sie ab, um zu bestimmen, welches Positions Bild aus der Bilddatei angezeigt werden soll.

``` syntax
        elementID.positionImage
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese- **/schreibzeichenfolge** , die den Namen einer Bilddatei enthält.

## <a name="remarks"></a>Bemerkungen

Dieses Attribut ist erforderlich und muss angegeben werden.

Das **positionImage** wird nicht angezeigt. Stattdessen dient sie als Karte, die die durch Klicken aktivierbaren Bereiche des angezeigten Bilds definiert. Das angezeigte Bild ist eines der untergeordneten Bilder der Bilddatei und stellt den tatsächlichen Zustand des Schiebereglers dar. Das **positionImage** enthält eine Reihe von grauen Skalierungs Regionen, die der Anzahl dieser untergeordneten Images entsprechen. Die untergeordneten Bilder müssen die gleichen Dimensionen wie das **positionImage** aufweisen, oder der benutzerdefinierte Schieberegler funktioniert nicht ordnungsgemäß.

Alle Regionen, die nicht Graustufen sind, können nicht geklickt werden. Die durch Klicken aktivierbaren Bereiche sollten auf Farbwerte festgelegt werden, die gleichmäßig über das graue Skalierungs Spektrum reichen, von Schwarz bis weiß, wobei die erste Region rein schwarz und die letzte Region rein weiß ist. Die Farbwerte für jeden aufeinander folgenden Bereich sollten um einen Wert von 255 (dividiert durch die Gesamtzahl der Regionen minus 1) erhöht werden, wobei auf die nächste ganze Zahl gerundet wird.

Wenn z. b. sechs Regionen vorhanden sind, ist das Inkrement 51 (255 dividiert durch 5), und die sechs Graustufen Werte lauten 0, 51, 102, 153, 204 und 255. Bei den hexadezimalen Farbwerten für die sechs Regionen handelt es sich dann um \# 000000, \# 333333, \# 666666, \# 999999, \# cccccc und \# FFFFFF.

Auf diese Weise wird für die Regionen eine Sequenz durch ihre Graustufen Farbwerte vorgegeben, und diese Sequenz entspricht der Sequenz von Unterbildern in der Bilddatei. Wenn auf eine der Regionen geklickt wird, wird das entsprechende untergeordnete Bild angezeigt, und der **Wert** des benutzerdefinierten Schiebereglers wird entsprechend aktualisiert.

Die unterstützten Bild Dateitypen sind BMP, JPG, PNG und GIF (keine animierten GIFs).

## <a name="examples"></a>Beispiele

Im folgenden finden Sie ein Beispiel für ein benutzerdefiniertes **Positions Bild** für den Schieberegler. Das entsprechende Bild wird im Beispiel Abschnitt der **Image** -Eigenschaft angezeigt.

![Beispiel Grafik für "positionImage"](images/dialmap.png)

Der folgende Code veranschaulicht die Verwendung von **customslider** -Attributen.


```XML
<THEME>
  <VIEW
    backgroundImage = "background.bmp"
    titleBar = "False"
  >

    <PLAYER
      URL = "https://proseware.com/mellow.wma"
    >
      <CONTROLS
        currentPosition_onchange = "myslider.value = player.controls.currentPosition;"
      />
    </PLAYER>

    <SLIDER
      id = "myslider"
      min = "0"
      max = "wmpprop:player.currentMedia.duration"
      onmouseup = "player.controls.currentPosition = myslider.value; "
      tooltip = "current position"
      height = "10"
      width = "180"
      top = "150"
      left = "88"
      backgroundColor = "red"
      foregroundColor = "blue"
      thumbImage = "thumb.bmp"
    />

    <CUSTOMSLIDER
      top = "120"
      left = "23"
      min = "0"
      max = "100"
      borderSize = "10"
      toolTip = "volume control"
      image = "dial.bmp"
      transparencyColor = "#00FFFF"
      positionImage = "dialmap.bmp"
      enabled = "true"
      value = "wmpprop:player.settings.volume"
      value_onchange = "player.settings.volume = value"
    />

    <EFFECTS
      id = "myeffects"
      top = "25"
      left = "88"
      width = "180"
      height = "100"
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

[**Customslider-Element**](customslider-element.md)
</dt> <dt>

[**Customslider. Image**](customslider-image.md)
</dt> </dl>

 

 





