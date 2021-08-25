---
title: Erstellen benutzerdefinierter Schieberegler
description: Erstellen benutzerdefinierter Schieberegler
ms.assetid: eb26ba44-a891-4cb6-be74-5acf881e896f
keywords:
- Erstellen von Skins, Schiebereglern
- Windows Media Player Skins, Schieberegler
- Skins, Schieberegler
- Schieberegler in Skins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d85a789bbd90003b59e1a9b9dcf8fffcf4a126c38138f7a051c24125780f8c83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902330"
---
# <a name="creating-custom-sliders"></a>Erstellen benutzerdefinierter Schieberegler

Sie können benutzerdefinierte Schieberegler in beliebiger Form erstellen. In diesem Beispiel wird ein einfacher Strip ausgewählt, aber die tatsächliche Form kann eine andere sein. Im Folgenden finden Sie den Code für das ELEMENT 1000111111111111111111111 


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



Dadurch wird ein Anfangswert für den Schieberegler eingerichtet. Zwei neue Bitmaps werden eingeführt. Eine ist die Graustufenbitmap (slider.bmp), die definiert, welche Werte beim Klicken auf verwendet werden, und die andere (slider.bmp), die bestimmt, welches Bild angezeigt wird, wenn auf einen bestimmten Teil der Graustufen geklickt wird.

Der Anfangswert wird durch Lauschen auf das Volume mit wmpprop bestimmt. Anschließend kann das Volume geändert werden, wenn der Benutzer auf einen Teil des Schiebereglers klickt, der eine Änderung des Werts auslöst.

Eine ähnliche Arbeitsschieberegler-Skin finden Sie im Beispielabschnitt des SDK.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Handbuch zur Erstellung von Skins**](skin-creation-guide.md)
</dt> </dl>

 

 




