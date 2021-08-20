---
title: VIDEO-Element
description: VIDEO-Element
ms.assetid: 817e0d2e-cbc3-4b61-81c0-876104125f39
keywords:
- Windows Media Player Skins,VIDEO-Element
- skins,VIDEO-Element
- VIDEO-Element
- Referenz für Skins,VIDEO-Element
- elements,VIDEO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7b72df7472829fe9979c9f7a30558e340a69aeb2f7024641623ba6be1a46424
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054198"
---
# <a name="video-element"></a>VIDEO-Element

Das **VIDEO-Element** bietet eine Möglichkeit, ein Videofenster in einer Skin mithilfe der folgenden Attribute und Ereignisse zu bearbeiten. Der Einfachheit halber wird auch ein vordefiniertes **VIDEO-Element** bereitgestellt.

Das **VIDEO-Element** unterstützt die folgenden Attribute.



| attribute                                            | Beschreibung                                                                                                                                                                                                                              |
|------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Backgroundcolor](video-backgroundcolor.md)         | Gibt die Hintergrundfarbe des Video-Steuerelements an oder ruft sie ab.                                                                                                                                                                        |
| [Cursor](video-cursor.md)                           | Gibt den Cursorwert an, der verwendet wird, wenn sich der Mauszeiger über einem klickbaren Bereich des Videos befindet, oder ruft diesen ab.                                                                                                                               |
| [Fullscreen](video-fullscreen.md)                   | Gibt einen Wert an, der angibt, ob das Video im Vollbildmodus angezeigt wird, oder ruft einen Wert ab. Kann nur zur Laufzeit festgelegt werden.                                                                                                               |
| [maintainAspectRatio](video-maintainaspectratio.md) | Gibt einen Wert an oder ruft einen Wert ab, der angibt, ob das Video das Seitenverhältnis beibebespricht, wenn versucht wird, in die für das Steuerelement definierte Breite und Höhe zu passen.                                                                       |
| [shrinkToFit](video-shrinktofit.md)                 | Gibt einen Wert an, der angibt, ob das Video auf die für das Video-Steuerelement definierte Breite und Höhe verkleinert wird, oder ruft einen Wert ab.                                                                                                           |
| [stretchToFit](video-stretchtofit.md)               | Gibt einen Wert an, der angibt, ob sich das Video auf die für das Video-Steuerelement definierte Breite und Höhe erstreckt, oder ruft einen Wert ab.                                                                                                   |
| [Quickinfo](video-tooltip.md)                         | Gibt den QuickInfo-Text für das Videofenster an oder ruft den Text ab.                                                                                                                                                                            |
| [Windowless](video-windowless.md)                   | Gibt einen Wert an, der angibt, ob das Video-Steuerelement fensterlos oder fensterlos ist, oder ruft einen Wert ab. Das heißt, ob das gesamte Rechteck des Steuerelements jederzeit sichtbar ist oder abgeschnitten werden kann. Kann nur zur Entwurfszeit festgelegt werden. |
| [Zoom](video-zoom.md)                               | Gibt den Prozentsatz an, um den das Video skaliert werden soll.                                                                                                                                                                                    |



 

Das **VIDEO-Element** kann die folgenden Ereignishandler implementieren.



| Ereignishandler                          | Beschreibung                                                                  |
|----------------------------------------|------------------------------------------------------------------------------|
| [onvideoend](video-onvideoend.md)     | Behandelt ein Ereignis, das auftritt, wenn das Video das Rendering beendet und entladen wird. |
| [onvideostart](video-onvideostart.md) | Behandelt ein Ereignis, das auftritt, wenn das Video geladen wird und mit dem Rendern beginnt.  |



 

Das **VIDEO-Element** unterstützt die Ambient-Attribute und kann die Ambient-Ereignishandler implementieren, sofern nicht anders angegeben. Weitere Informationen finden Sie unter [Ambient Attributes](ambient-attributes.md) und [Ambient Event Handlers](ambient-event-handlers.md).

Vordefinierte Videoelemente sind normale **VIDEO-Elemente** mit verschiedenen allgemeinen Attributeinstellungen, die standardmäßig angegeben sind. Die folgenden vordefinierten Videoelemente sind verfügbar.



| Vordefiniertes VIDEO         | Beschreibung                                                |
|--------------------------|------------------------------------------------------------|
| [WMPVIDEO](wmpvideo.md) | Ein **VIDEO-Element,** das das Video beim Ändern der Größe streckt. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Referenz zur Skinprogrammierung**](skin-programming-reference.md)
</dt> </dl>

 

 




