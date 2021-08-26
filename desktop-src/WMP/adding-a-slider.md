---
title: Hinzufügen eines Schiebereglers
description: Hinzufügen eines Schiebereglers
ms.assetid: 7062d580-a9d1-4fd7-bc28-db2615464838
keywords:
- Erstellen von Skins, Schiebereglern
- Windows Media Player Skins, Schieberegler
- Skins, Schieberegler
- Schieberegler in Skins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6c3644e1b243188664295bbc00101a74377cbef17632217ff0a81dac0d377a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004379"
---
# <a name="adding-a-slider"></a>Hinzufügen eines Schiebereglers

Sie können einen Schieberegler hinzufügen, um die aktuelle Position des Mediums zu zeigen, und dem Benutzer ermöglichen, die Position in der aktuellen Mediendatei zu ändern.

Zuerst müssen Sie das **SLIDER-Element** hinzufügen:


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



Dadurch wird ein Maximalwert basierend auf der Dauer der aktuellen Mediendatei definiert. Dabei wird eine kleine Bitmap mit einem Ingerabbild verwendet, die nur ein grünes Quadrat mit 10 Pixeln und 10 Pixeln ist. Der Hintergrund des Schiebereglers ist rot und der Vordergrund blau. Wenn der Benutzer das Ziehbild an eine neue Position zieht und die Maustaste loslässt, ändert sich das Medium in diese Position.

Der Schieberegler wird jedoch nur dann allein bewegt, wenn Sie die aktuelle Position mit dem **currentPosition \_ onchange-Attribut** des **CONTROLS-Elements** messen, das in das **PLAYER-Element eingebettet** ist.


```C++
<PLAYER
    URL = "https://proseware.com/laure.wma">

    <CONTROLS
        currentPosition_onchange = "myslider.value = player.controls.currentPosition; "/>

</PLAYER>

```



Wenn sich die Position des Mediums ändert, wird ein Ereignis mit der Codezeile ausgeführt, die den Wert des Schiebereglers in die aktuelle Position des Mediums ändert.

Eine ähnliche Arbeitsschieberegler-Skin finden Sie im Beispielabschnitt des SDK.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Handbuch zur Erstellung von Skins**](skin-creation-guide.md)
</dt> </dl>

 

 




