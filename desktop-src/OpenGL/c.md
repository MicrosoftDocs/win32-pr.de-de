---
title: C (OpenGL)
description: Definitionen von OpenGL-Begriffen, die mit dem Buchstaben C beginnen.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 037c39b1-b728-41d3-a664-c0aa6c487103
keywords:
- Clientcomputer
- Clientspeicher
- Clipkoordinaten
- Clipping
- Farbindex
- Farbindexmodus
- Farbzuordnungen
- components
- Kontexte
- Konvex
- konvexe Hülle
- Koordinatensystem
- Keulung
- Aktuelle Matrix
- Aktuelle Rasterposition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39007e4719e1f4507555bf5aafa3187a897756d1d33580e9facc8fa0f6d8fa3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675990"
---
# <a name="c-opengl"></a>C (OpenGL)

[A](a.md) [B](b.md) C [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) J [K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) U [V](u-v.md) [W](w.md) X [Y Z](x-y-z.md)

<dl> <dt>

<span id="opengl_client_computer"></span><span id="OPENGL_CLIENT_COMPUTER"></span>**Clientcomputer**
</dt> <dd>

Der Computer, von dem OpenGL-Befehle ausgegeben werden. Der Computer, der OpenGL-Befehle ausgibt, kann über ein Netzwerk mit einem anderen Computer verbunden werden, der die Befehle ausführt, oder Befehle können auf demselben Computer ausgegeben und ausgeführt werden. Siehe auch [Server](s.md).

</dd> <dt>

<span id="opengl_client_memory"></span><span id="OPENGL_CLIENT_MEMORY"></span>**Clientspeicher**
</dt> <dd>

Der Hauptspeicher (in dem Programmvariablen gespeichert werden) des Clientcomputers.

</dd> <dt>

<span id="opengl_clip_coordinates"></span><span id="OPENGL_CLIP_COORDINATES"></span>**Clipkoordinaten**
</dt> <dd>

Das Koordinatensystem, das der Transformation durch die Projektionsmatrix folgt und der Perspektiventeilung vorausgeht. Clipping auf dem Anzeigevolume erfolgt in Clipkoordinaten, anwendungsspezifisches Clipping hingegen nicht. Siehe auch [anwendungsspezifisches Clipping.](a.md)

</dd> <dt>

<span id="opengl_clipping"></span><span id="OPENGL_CLIPPING"></span>**Clipping**
</dt> <dd>

Entfernen des Teils eines geometrischen Primitivs, der sich außerhalb des durch eine Clippingebene definierten Halbraums befindet. Punkte werden einfach abgelehnt, wenn sie sich außerhalb befinden. Der Teil einer Linie oder eines Polygons, der sich außerhalb des Halbraums befindet, wird entfernt, und zusätzliche Scheitelpunkte werden nach Bedarf generiert, um den Primitiven innerhalb des clipping-Halbraums zu vervollständigen. Geometrische Primitive und die aktuelle Rasterposition (sofern angegeben) werden immer auf die sechs Halbräume abgeschnitten, die durch die linken, rechten, unteren, oberen, nahen und fernen Ebenen des Ansichtsvolumens definiert werden. Anwendungen können optionale anwendungsspezifische Clippingebenen angeben, die in Augenkoordinaten angewendet werden sollen.

</dd> <dt>

<span id="opengl_color_index"></span><span id="OPENGL_COLOR_INDEX"></span>**Farbindex**
</dt> <dd>

Ein einzelner Wert, der eine Farbe nach Name und nicht nach Wert darstellt. OpenGL-Farbindizes werden als kontinuierliche Werte (z. B. Gleitkommazahlen) behandelt, während Vorgänge wie Interpolation und Dithering für sie ausgeführt werden. Im Framepuffer gespeicherte Farbindizes sind jedoch immer ganzzahlige Werte. Gleitkommaindizes werden in ganze Zahlen konvertiert, indem sie auf den nächsten ganzzahligen Wert gerundet werden.

</dd> <dt>

<span id="opengl_color_index_mode"></span><span id="OPENGL_COLOR_INDEX_MODE"></span>**Farbindexmodus**
</dt> <dd>

Modus eines OpenGL-Kontexts, in dem seine Farbpuffer Farbindizes anstelle von Rot-, Grün-, Blau- und Alphafarbkomponenten speichern.

</dd> <dt>

<span id="opengl_color_map"></span><span id="OPENGL_COLOR_MAP"></span>**Farbkarte**
</dt> <dd>

Eine Tabelle mit Index-zu-RGB-Zuordnungen, auf die von der Anzeigehardware zugegriffen wird. Jeder Farbindex wird aus dem Farbpuffer gelesen, durch Suche in der Farbkarte in ein RGB-Triple konvertiert und an den Monitor gesendet.

</dd> <dt>

<span id="opengl_component"></span><span id="OPENGL_COMPONENT"></span>**Komponente**
</dt> <dd>

Ein einzelner kontinuierlicher Wert (z. B. Gleitkommawert), der eine Intensität oder Menge darstellt. Normalerweise stellt ein Komponentenwert von 0 (null) den Minimalwert oder die Minimale Intensität dar, und ein Komponentenwert von 1 stellt den maximalen Wert oder die Maximale Intensität dar, obwohl manchmal andere Normalisierungen verwendet werden. Da Komponentenwerte in einem normalisierten Bereich interpretiert werden, werden sie unabhängig von der tatsächlichen Auflösung angegeben. Beispielsweise ist das RGB-Triple (1, 1, 1) weiß, unabhängig davon, ob die Farbpuffer jeweils 4, 8 oder 12 Bits speichern. Komponenten außerhalb des Bereichs werden in der Regel an den normalisierten Bereich klammern, nicht abgeschnitten oder anderweitig interpretiert. Beispielsweise wird das RGB-Triple (1,4, 1,5, 0,9) an (1,0, 1,0, 0,9) klammern, bevor es zum Aktualisieren des Farbpuffers verwendet wird. Rot, Grün, Blau, Alpha und Tiefe werden immer als Komponenten und nie als Indizes behandelt.

</dd> <dt>

<span id="opengl_context"></span><span id="OPENGL_CONTEXT"></span>**Kontext**
</dt> <dd>

Ein vollständiger Satz von OpenGL-Zustandsvariablen. Beachten Sie, dass framebuffer-Inhalte nicht Teil des OpenGL-Zustands sind, die Konfiguration des Framepuffers jedoch ist.

</dd> <dt>

<span id="opengl_convex"></span><span id="OPENGL_CONVEX"></span>**Konvex**
</dt> <dd>

Bedingung eines Polygons, bei dem keine gerade Linie auf der Ebene des Polygons das Polygon mehr als zweimal überschneidet.

</dd> <dt>

<span id="opengl_convex_hull"></span><span id="OPENGL_CONVEX_HULL"></span>**Konvexe Hülle**
</dt> <dd>

Der kleinste konvexe Bereich, der eine angegebene Gruppe von Punkten einschließt. In zwei Dimensionen wird die konvexe Hülle konzeptionell gefunden, indem ein Blasenband um die Punkte gestreckt wird, sodass alle Punkte innerhalb des Bands liegen.

</dd> <dt>

<span id="opengl_coordinate_system"></span><span id="OPENGL_COORDINATE_SYSTEM"></span>**Koordinatensystem**
</dt> <dd>

In einem n-dimensionalen Raum ein Satz von n linear unabhängigen Vektoren, die an einem Punkt (Ursprung genannt) verankert sind. Eine Gruppe von Koordinaten gibt einen Punkt im RaumIn n-dimensionaler Raum an, eine Reihe von linear unabhängigen Vektoren, die an einem Punkt (als Ursprung bezeichnet) verankert sind. Anhand einer Gruppe von Koordinaten wird ein Punkt im Raum (oder ein Vektor vom Ursprung) festgelegt. Dazu wird die Strecke zum Punkt (oder zur Spitze des Vektors) entlang des jeweiligen Vektors angegeben. (oder ein Vektor vom Ursprung), indem angegeben wird, wie weit die Einzelnen Vektoren entlang bewegt werden sollen, um den Punkt (oder die Spitze des Vektors) zu erreichen.

</dd> <dt>

<span id="opengl_culling"></span><span id="OPENGL_CULLING"></span>**Keulung**
</dt> <dd>

Der Prozess, bei dem ein Vorder- oder Rückwand eines Polygons beseitigt wird, sodass das Gesicht nicht gezeichnet wird.

</dd> <dt>

<span id="opengl_current_matrix"></span><span id="OPENGL_CURRENT_MATRIX"></span>**Aktuelle Matrix**
</dt> <dd>

Eine Matrix, die Koordinaten in einem Koordinatensystem in Koordinaten eines anderen Systems transformiert. Es gibt drei aktuelle Matrizen in OpenGL: die Modellansichtsmatrix, die Objektkoordinaten (vom Programmierer angegebene Koordinaten) in Augenkoordinaten transformiert; die Perspektivenmatrix, die Augenkoordinaten in Clipkoordinaten transformiert; und die Texturmatrix, die angegebene oder generierte Texturkoordinaten wie in der Matrix beschrieben transformiert. Jede aktuelle Matrix ist das oberste Element in einem Stapel von Matrizen. Jeder der drei Stapel kann mit OpenGL-Matrixbearbeitungsbefehlen bearbeitet werden.

</dd> <dt>

<span id="opengl_current_raster_position"></span><span id="OPENGL_CURRENT_RASTER_POSITION"></span>**Aktuelle Rasterposition**
</dt> <dd>

Eine Fensterkoordinatenposition, die die Platzierung eines Bildprimitiven beim Rastern angibt. Die aktuelle Rasterposition und andere aktuelle Rasterparameter werden aktualisiert, wenn glRasterpos aufgerufen wird.

</dd> </dl>

 

 




