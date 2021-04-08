---
title: Fügen eines Schiebereglers
description: Fügen eines Schiebereglers
ms.assetid: 7062d580-a9d1-4fd7-bc28-db2615464838
keywords:
- Erstellen von Skins, Schieberegler
- Windows Media Player Skins, Schieberegler
- Skins, Schieberegler
- Schieberegler in Skins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3efcae55b3826b69a7c88fed5a23a262526c9dd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037216"
---
# <a name="adding-a-slider"></a>Fügen eines Schiebereglers

Sie können einen Schieberegler hinzufügen, um die aktuelle Position des Mediums anzuzeigen. Außerdem können Sie den Benutzer aktivieren, um die Position in der aktuellen Mediendatei zu ändern.

Zuerst müssen Sie das **Slider** -Element hinzufügen:


```C++
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
  thumbImage = "thumb.bmp"/>

```



Dadurch wird ein Maximalwert basierend auf der Dauer der aktuellen Mediendatei festgelegt. Hierbei wird ein kleines Ziehpunkt für das Ziehpunkt-Bild verwendet Der Hintergrund des Schiebereglers wird rot angezeigt, und der Vordergrund wird blau dargestellt. Wenn der Benutzer das Ziehpunkt Bild an eine neue Position zieht und die Maustaste loslässt, werden die Medien an diese Position geändert.

Der Schieberegler wird jedoch nicht von sich selbst verschoben, es sei denn, Sie messen die aktuelle Position mit dem **CurrentPosition \_ OnChange** -Attribut des **Controls** -Elements, das in das **Player** -Element eingebettet ist.


```C++
<PLAYER
    URL = "https://proseware.com/laure.wma">

    <CONTROLS
        currentPosition_onchange = "myslider.value = player.controls.currentPosition; "/>

</PLAYER>

```



Wenn sich die Position des Mediums ändert, wird ein Ereignis ausgelöst, das dann die Codezeile ausführt, die den Wert des Schiebereglers an die aktuelle Position des Mediums ändert.

Sie können im Abschnitt "Sample" des SDK einen ähnlichen Schieberegler für den Schieberegler sehen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Leitfaden zum Erstellen von Skin**](skin-creation-guide.md)
</dt> </dl>

 

 




