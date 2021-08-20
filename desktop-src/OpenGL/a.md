---
title: A (OpenGL)
description: Definitionen von OpenGL-Begriffen, die mit dem Buchstaben A beginnen.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: e583610f-37da-47bb-bbd6-41d353b88244
keywords:
- Aliasing
- alpha
- Animation
- Antialiasing (antialiasing)
- Anwendungsspezifisches Clipping
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb69307f869031bb9fd176ec85dd20eac5d543ef3e7f63086c6ea0801d1b8b8a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128370"
---
# <a name="a-opengl"></a>A (OpenGL)

A [B](b.md) [C](c.md) [D](d.md) [E](e.md) F [G](f.md) [](g.md) [H](h.md) [I](i.md) J [K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) T [U](t.md) [V](u-v.md) [W](w.md) X [Y Z](x-y-z.md)

<dl> <dt>

<span id="opengl_aliasing"></span><span id="OPENGL_ALIASING"></span>**Aliasing**
</dt> <dd>

Eine Renderingtechnik, die Pixeln die Farbe des zu rendernden Primitivs zuteilt, unabhängig davon, ob dieser Primitiv den Pixelbereich ganz oder teilweise abdeckt. Aliasing führt zu verknoffenen Kanten oder Rändern. Siehe auch [.](jk.md)

</dd> <dt>

<span id="opengl_alpha"></span><span id="OPENGL_ALPHA"></span>**Alpha**
</dt> <dd>

Eine vierte Farbkomponente, die in der Regel zum Steuern der Farbmischung verwendet wird. Die Alphakomponente wird nie direkt angezeigt. Standardmäßig gibt OpenGL Alpha Deckkraft und Transparenz auf einer Skala von 0,0 bis 1,0 an. Ein Alphawert von 1,0 impliziert vollständige Deckkraft, ein Alphawert von 0,0 impliziert vollständige Transparenz.

</dd> <dt>

<span id="opengl_animation"></span><span id="OPENGL_ANIMATION"></span>**Animation**
</dt> <dd>

Die Generierung von wiederholten Renderings einer Szene mit sich nahtlos ändernden Standpunkt- oder Objektpositionen schnell genug, um die Bewegung zu erreichen. OpenGL-Animationen verwenden fast immer doppelte Pufferung.

</dd> <dt>

<span id="opengl_antialiasing"></span><span id="OPENGL_ANTIALIASING"></span>**Antialiasing**
</dt> <dd>

Ein Renderingverfahren, bei dem Pixeln Farben basierend auf dem Bruchteil des Pixelbereichs zugewiesen werden, der von dem zu rendernden Primitiv abgedeckt wird. Antialiased Rendering reduziert oder beseitigt die Ja- oder Nische, die sich aus dem Rendering mit Aliasing ergeben. Weitere Informationen finden [Sie unter jases](jk.md), [rendering](r.md).

</dd> <dt>

<span id="opengl_application_specific_clipping"></span><span id="OPENGL_APPLICATION_SPECIFIC_CLIPPING"></span>**Anwendungsspezifisches Clipping** 
</dt> <dd>

Clipping von Primitiven an Ebenen in Augenkoordinaten. Die Ebenen werden von der Anwendung mit [**glClipPlane angegeben.**](glclipplane.md) Siehe auch [Augenkoordinaten.](e.md)

</dd> </dl>

 

 




