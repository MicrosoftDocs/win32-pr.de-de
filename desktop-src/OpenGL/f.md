---
title: F (OpenGL)
description: Definitionen von OpenGL-Begriffen, die mit dem Buchstaben F beginnen.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: ba960409-84e0-4ece-967b-97f0e1183956
keywords:
- faces
- Flache Schattierung
- Nebel
- Schriftarten
- fragments
- framebuffers
- Front face (Front-Face)
- Frustum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 748eb0fade84ef76c133453165db53d8540326dae3111ac04f3b7a6819ae825a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118618185"
---
# <a name="f-opengl"></a>F (OpenGL)

[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) F [G](g.md) [H](h.md) [I](i.md) J [K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) U [V](u-v.md) [W](w.md) X [Y Z](x-y-z.md)

<dl> <dt>

<span id="opengl_face"></span><span id="OPENGL_FACE"></span>**Gesicht**
</dt> <dd>

Eine Seite eines Polygons. Jedes Polygon verfügt über zwei Gesichter: ein Vorder- und ein Hintergrundgesicht. Im Fenster ist immer nur ein Gesicht sichtbar. Ob das Hinter- oder Vordergesicht sichtbar ist, wird effektiv bestimmt, nachdem das Polygon auf das Fenster projiziert wurde. Wenn nach dieser Projektion die Ränder des Polygons im Uhrzeigersinn gerichtet sind, ist eines der Gesichter sichtbar. Wenn gegen den Uhrzeigersinn gerichtet, ist das andere Gesicht sichtbar. Ob der Uhrzeigersinn front oder back entspricht (und counterclockwise entspricht back oder front), wird vom OpenGL-Programmierer bestimmt.

</dd> <dt>

<span id="opengl_flat_shading"></span><span id="OPENGL_FLAT_SHADING"></span>**Flache Schattierung**
</dt> <dd>

Bezieht sich auf die Färbung eines Primitivs mit einer einzelnen, konstanten Farbe über seinen Umfang, anstatt farben reibungslos über den Primitiven hinweg zu interpolieren. Weitere Informationen [finden Sie unter Gouraud shading](g.md).

</dd> <dt>

<span id="opengl_fog"></span><span id="OPENGL_FOG"></span>**Nebel**
</dt> <dd>

Eine Renderingtechnik, die verwendet werden kann, um Effekten wie Haze, Brand und Smog zu simulieren, indem Objektfarben basierend auf der Entfernung vom Betrachter in eine Hintergrundfarbe überfingt werden. Außerdem hilft Einschlag bei der Wahrnehmung der Entfernung vom Betrachter und gibt einen tiefen Hinweis. Siehe auch [tiefenorientierte .](d.md)

</dd> <dt>

<span id="opengl_font"></span><span id="OPENGL_FONT"></span>**Schriftart**
</dt> <dd>

Eine Gruppe von grafischen Zeichendarstellungen, die normalerweise zum Anzeigen von Textzeichenfolgen verwendet werden. Bei den Zeichen kann es sich um romanische Buchstaben, mathematische Symbole, asiatische Ideogramme, Hieroglyphen für Diebungen und so weiter werden.

</dd> <dt>

<span id="opengl_fragment"></span><span id="OPENGL_FRAGMENT"></span>**Fragment**
</dt> <dd>

Grafikdaten, die durch die Rasterung von Primitiven generiert werden. Jedes Fragment entspricht einem einzelnen Pixel und enthält Farb-, Tiefen- und manchmal Texturkoordinatenwerte.

</dd> <dt>

<span id="opengl_framebuffer"></span><span id="OPENGL_FRAMEBUFFER"></span>**Framebuffer**
</dt> <dd>

Ein Stapel von Bitebenen. Alle Puffer eines bestimmten Fensters oder Kontexts. Manchmal enthält den pixel-Arbeitsspeicher des Grafikhardwarebeschleunigers. Siehe auch [bitplane](b.md).

</dd> <dt>

<span id="opengl_front_face"></span><span id="OPENGL_FRONT_FACE"></span>**Front face (Front-Face)**
</dt> <dd>

Siehe Gesicht.

</dd> <dt>

<span id="opengl_frustum"></span><span id="OPENGL_FRUSTUM"></span>**Frustum**
</dt> <dd>

Das Ansichtsvolumen, das durch die perspektivische Division getauscht wird.

</dd> </dl>

 

 




