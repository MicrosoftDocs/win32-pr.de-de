---
title: Video-Element
description: Video-Element
ms.assetid: 817e0d2e-cbc3-4b61-81c0-876104125f39
keywords:
- Windows Media Player Skins, Video-Element
- Skins, Video-Element
- Video-Element
- Verweis für Skins, Video-Element
- Elemente, Video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbd8ab6bd014d2968483120fd1dd98804905faa4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711105"
---
# <a name="video-element"></a>Video-Element

Das **Video** -Element bietet eine Möglichkeit, ein Video Fenster in einer Skin zu bearbeiten, indem die folgenden Attribute und Ereignisse verwendet werden. Ein vordefiniertes **Video** Element wird auch zur einfacheren Bereitstellung bereitgestellt.

Das **Video** -Element unterstützt die folgenden Attribute.



| Attribut                                            | BESCHREIBUNG                                                                                                                                                                                                                              |
|------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Background Color](video-backgroundcolor.md)         | Gibt die Hintergrundfarbe des Video Steuer Elements an oder ruft diese ab.                                                                                                                                                                        |
| [Cursor](video-cursor.md)                           | Gibt den Cursor Wert an, der verwendet wird, wenn sich der Mauszeiger über einem klickbaren Bereich des Videos befindet, oder ruft ihn ab.                                                                                                                               |
| [Vollbild](video-fullscreen.md)                   | Gibt einen Wert an, der angibt, ob das Video im Vollbildmodus angezeigt wird, oder ruft diesen ab. Kann nur zur Laufzeit festgelegt werden.                                                                                                               |
| [wart AspectRatio](video-maintainaspectratio.md) | Gibt einen Wert an bzw. Ruft einen Wert ab, der angibt, ob im Video das Seitenverhältnis beibehalten wird, wenn versucht wird, die Breite und Höhe des Steuer Elements anzupassen.                                                                       |
| [ShrinkToFit](video-shrinktofit.md)                 | Gibt einen Wert an, der angibt, ob das Video auf die für das Video Steuerelement definierte Breite und Höhe verkleinert wird, oder ruft diesen Wert ab.                                                                                                           |
| [stretchdefit](video-stretchtofit.md)               | Gibt einen Wert an, der angibt, ob sich das Video auf die für das Video Steuerelement definierte Breite und Höhe erstreckt, oder ruft diesen Wert ab.                                                                                                   |
| [QuickInfo](video-tooltip.md)                         | Gibt den QuickInfo-Text für das Videofenster an oder ruft ihn ab.                                                                                                                                                                            |
| [Windowless](video-windowless.md)                   | Gibt einen Wert an bzw. Ruft einen Wert ab, der angibt, ob das Video Steuerelement Fenster oder Windows-los ist. Das heißt, ob das gesamte Rechteck des Steuer Elements jederzeit sichtbar ist oder abgeschnitten werden kann. Kann nur zur Entwurfszeit festgelegt werden. |
| [Skala](video-zoom.md)                               | Gibt den Prozentsatz an, um den das Video skaliert werden soll.                                                                                                                                                                                    |



 

Das **Video** -Element kann die folgenden Ereignishandler implementieren.



| Ereignishandler                          | BESCHREIBUNG                                                                  |
|----------------------------------------|------------------------------------------------------------------------------|
| [onvideoend](video-onvideoend.md)     | Behandelt ein Ereignis, das auftritt, wenn das Video das Rendering beendet und entladen wird. |
| [onvideostart](video-onvideostart.md) | Behandelt ein Ereignis, das auftritt, wenn das Video geladen und mit dem Rendering beginnt.  |



 

Das **Video** -Element unterstützt die Ambient-Attribute und kann die Umgebungs Ereignishandler implementieren, sofern nicht angegeben. Weitere Informationen finden Sie unter [Ambient-Attribute](ambient-attributes.md) und [Ambient-Ereignishandler](ambient-event-handlers.md).

Vordefinierte Video Elemente sind normale **Video** Elemente mit verschiedenen allgemeinen Attribut Einstellungen, die standardmäßig angegeben werden. Die folgenden vordefinierten Video Elemente sind verfügbar.



| Vordefiniertes Video         | BESCHREIBUNG                                                |
|--------------------------|------------------------------------------------------------|
| [Wmpvideo](wmpvideo.md) | Ein **Video** Element, das das Video beim Ändern der Größe ausdehnt. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Referenz zur Skin-Programmierung**](skin-programming-reference.md)
</dt> </dl>

 

 




