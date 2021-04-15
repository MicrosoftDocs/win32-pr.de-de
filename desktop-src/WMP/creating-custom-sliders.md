---
title: Erstellen benutzerdefinierter Schieberegler
description: Erstellen benutzerdefinierter Schieberegler
ms.assetid: eb26ba44-a891-4cb6-be74-5acf881e896f
keywords:
- Erstellen von Skins, Schieberegler
- Windows Media Player Skins, Schieberegler
- Skins, Schieberegler
- Schieberegler in Skins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0f205d46af003589fcc2c3b741a253ea08fae12
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515914"
---
# <a name="creating-custom-sliders"></a>Erstellen benutzerdefinierter Schieberegler

Sie können benutzerdefinierte Schieberegler in jeder beliebigen Form erstellen. In diesem Beispiel wird ein einfacher Strip ausgewählt, aber die tatsächliche Form kann etwas sein. Dies ist der Code für das **customslider** -Element:


```C++
<CustomSlider 
  top="160"
  left="130"
  min="0"
  max="100"
  toolTip="volume control"
  image="slider.bmp"
  positionImage="graymap.bmp"
  enabled="true"
  value="wmpprop:player.settings.volume"
  value_onchange="player.settings.volume = value" />

```



Dadurch wird ein Anfangswert für den Schieberegler festgelegt. Es werden zwei neue Bitmaps eingeführt. Eine ist die Graustufen Bitmap (slider.bmp), die definiert, welche Werte verwendet werden, wenn darauf geklickt wird, und die andere (slider.bmp), die bestimmt, welches Bild angezeigt wird, wenn auf einen bestimmten Teil der grau Skala geklickt wird.

Der Anfangswert wird durch lauschen auf dem Volume mit wmpprop festgelegt, und das Volume kann geändert werden, wenn der Benutzer auf einen Teil des Schiebereglers klickt, der eine Änderung des Werts auslöst.

Sie können im Abschnitt "Sample" des SDK einen ähnlichen Schieberegler für den Schieberegler sehen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Leitfaden zum Erstellen von Skin**](skin-creation-guide.md)
</dt> </dl>

 

 




