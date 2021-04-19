---
title: F (OpenGL)
description: Definitionen von OpenGL-Begriffen, die mit dem Buchstaben F beginnen.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: ba960409-84e0-4ece-967b-97f0e1183956
keywords:
- faces
- flatschattierung
- Nebel
- Schriftarten
- fragments
- framebuffers
- Vorderseite
- Frustum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7085765a5585268acb2f20a77c72bdd7cf1b4b81
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106337278"
---
# <a name="f-opengl"></a>F (OpenGL)

[a](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) F [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)

<dl> <dt>

<span id="opengl_face"></span><span id="OPENGL_FACE"></span>**mit**
</dt> <dd>

Eine Seite eines Polygons. Jedes Polygon hat zwei Gesichter: eine Vorderseite und eine Rückseite. Im Fenster ist immer nur ein Gesicht sichtbar. Ob das hintere oder das vordere Gesicht sichtbar ist, wird effektiv festgelegt, nachdem das Polygon auf das Fenster projiziert wurde. Wenn die Ränder des Polygons nach dieser Projektion im Uhrzeigersinn weitergeleitet werden, ist eine der Gesichter sichtbar. Wenn das andere Gesicht gegen den Uhrzeigersinn gerichtet ist, ist es sichtbar. Ob der Uhrzeigersinn dem Vordergrund oder dem Hintergrund entspricht (und gegen den Uhrzeigersinn entsprechen), wird vom OpenGL-Programmierer bestimmt.

</dd> <dt>

<span id="opengl_flat_shading"></span><span id="OPENGL_FLAT_SHADING"></span>**flatschattierung**
</dt> <dd>

Bezieht sich auf die Farbgebung eines Primitivs mit einer einzelnen, Konstanten Farbe in seinem Block, anstatt Farben über das primitive hinweg zu interpolieren. Siehe [Gouraud-Schattierung](g.md).

</dd> <dt>

<span id="opengl_fog"></span><span id="OPENGL_FOG"></span>**Neben**
</dt> <dd>

Eine renderingtechnik, die verwendet werden kann, um atmosphärische Effekte wie z. b. Dunst, Nebel und Smog zu simulieren, indem Objekt Farben auf Grundlage der Entfernung vom Viewer auf eine Hintergrundfarbe ausgeblendet werden. Der Nebel unterstützt auch die Wahrnehmung der Entfernung vom Viewer und bietet einen tiefen Hinweis. Siehe auch [ausführlichere](d.md)Informationen.

</dd> <dt>

<span id="opengl_font"></span><span id="OPENGL_FONT"></span>**Raster**
</dt> <dd>

Eine Gruppe grafischer Zeichen Darstellungen, die normalerweise zum Anzeigen von Text Zeichenfolgen verwendet wird. Bei den Zeichen kann es sich um römische Buchstaben, mathematische Symbole, asiatische Ideogramme, ägyptische Hieroglyphen usw. handeln.

</dd> <dt>

<span id="opengl_fragment"></span><span id="OPENGL_FRAGMENT"></span>**Bruch**
</dt> <dd>

Grafikdaten, die von der Rasterung von primitiven generiert werden. Jedes Fragment entspricht einem einzelnen Pixel und umfasst Farben, Tiefe und manchmal Texturkoordinaten Werte.

</dd> <dt>

<span id="opengl_framebuffer"></span><span id="OPENGL_FRAMEBUFFER"></span>**Frame Puffer**
</dt> <dd>

Ein Stapel von bitflächen. Alle Puffer eines bestimmten Fensters oder Kontexts. Umfasst manchmal den gesamten Pixel Speicher des Grafikhardware-Accelerators. Siehe auch [bitplane](b.md).

</dd> <dt>

<span id="opengl_front_face"></span><span id="OPENGL_FRONT_FACE"></span>**Vorderseite**
</dt> <dd>

Siehe Gesicht.

</dd> <dt>

<span id="opengl_frustum"></span><span id="OPENGL_FRUSTUM"></span>**Frustum**
</dt> <dd>

Das Ansichts Volume, das von der Perspektiven Division zurückgeleitet wurde.

</dd> </dl>

 

 




