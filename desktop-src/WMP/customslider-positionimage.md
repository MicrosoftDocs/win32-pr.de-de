---
title: LIDER.positionImage
description: Das attribut positionImage gibt die Bildzuordnung an oder ruft sie ab, die verwendet wird, um zu bestimmen, welches Positionsbild aus der Bilddatei angezeigt werden soll.
ms.assetid: 7e99dc21-ebba-438a-a983-190dbe429578
keywords:
- LIDER.positionImage-Windows Media Player
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.positionImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 727601ceb7ed078e40a284ab291f2e182a4270682b5f1db104515e31d3dbe2ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117749991"
---
# <a name="customsliderpositionimage"></a>LIDER.positionImage

Das **attribut positionImage** gibt die Bildzuordnung an oder ruft sie ab, die verwendet wird, um zu bestimmen, welches Positionsbild aus der Bilddatei angezeigt werden soll.

``` syntax
        elementID.positionImage
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine  Zeichenfolge mit Lese-/Schreibzugriff, die den Namen einer Bilddatei enthält.

## <a name="remarks"></a>Hinweise

Dieses Attribut ist erforderlich und muss angegeben werden.

**PositionImage** wird nicht angezeigt. Stattdessen dient sie als Karte, die die klickbaren Bereiche des angezeigten Bilds definiert. Das angezeigte Bild ist eines der Unterbilder der Bilddatei und stellt den tatsächlichen Zustand des Schiebereglers dar. PositionImage **enthält** eine Reihe von grauen Skalierungsregionen, die der Anzahl dieser Unterbilder entspricht. Die Untergeordneten Bilder müssen die gleichen Dimensionen wie **positionImage** haben, da der benutzerdefinierte Schieberegler nicht ordnungsgemäß funktioniert.

Auf regionen, die nicht grau skaliert sind, kann nicht geklickt werden. Die klickbaren Bereiche sollten auf Farbwerte festgelegt werden, die gleichmäßig über das graue Skalierungsspektrum von Schwarz bis Weiß reichen, während die erste Region rein schwarz und die letzte Region rein weiß ist. Die Farbwerte der einzelnen aufeinander folgenden Regionen sollten um einen Wert von 255 dividiert durch die Gesamtzahl der Regionen minus 1 erhöht werden, was auf die nächste ganze Zahl gerundet wird.

Wenn es beispielsweise sechs Regionen gibt, wäre das Inkrement 51 (255 geteilt durch 5), und die sechs grauen Skalierungswerte wären 0, 51, 102, 153, 204 und 255. Die hexadezimalen Farbwerte für die sechs Regionen wären dann \# 000000, \# 333333, \# 666666, \# \# 999999,ÖFFCCC und \# FFFFFF.

Auf diese Weise wird für die Regionen eine Sequenz durch ihre Graustufenfarbwerte bestimmt, und diese Sequenz entspricht der Sequenz von Unterbildern in der Bilddatei. Wenn auf einen der Bereiche geklickt wird, wird das  entsprechende Unterbild angezeigt, und der Wert des benutzerdefinierten Schiebereglers wird entsprechend aktualisiert.

Die unterstützten Bilddateitypen sind BMP, JPG, PNG und GIF (ohne animierte GIFs).

## <a name="examples"></a>Beispiele

Im Folgenden finden Sie ein Beispiel für eine benutzerdefinierte Position des **SchiebereglersImage**. Das entsprechende Bild wird im Beispielabschnitt der **image-Eigenschaft** angezeigt.

![BeispielpositionBildgrafik](images/dialmap.png)

Der folgende Code veranschaulicht die Verwendung von **ATTRIBUTEn DESTLIDER-Attributs.**


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
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**LIDER-Element**](customslider-element.md)
</dt> <dt>

[**LIDER.image**](customslider-image.md)
</dt> </dl>

 

 





