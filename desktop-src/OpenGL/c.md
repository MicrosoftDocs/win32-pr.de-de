---
title: C (OpenGL)
description: Definitionen von OpenGL-Begriffen, die mit dem Buchstaben C beginnen.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 037c39b1-b728-41d3-a664-c0aa6c487103
keywords:
- Client Computer
- Client Arbeitsspeicher
- Clip Koordinaten
- Clipping
- Farbindex
- Farb Index Modus
- Farb Zuordnungen
- components
- Kontexte
- konvexe
- konvexe Hülle
- Koordinatensystem
- cullingfunktionsgruppe
- aktuelle Matrix
- aktuelle Raster Position
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73c9534052533745b1037aa80f26f435a163ee46
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104040000"
---
# <a name="c-opengl"></a>C (OpenGL)

[a](a.md) [B](b.md) C [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)

<dl> <dt>

<span id="opengl_client_computer"></span><span id="OPENGL_CLIENT_COMPUTER"></span>**Client Computer**
</dt> <dd>

Der Computer, von dem OpenGL-Befehle ausgestellt werden. Der Computer, von dem OpenGL-Befehle ausgestellt werden, kann über ein Netzwerk mit einem anderen Computer verbunden werden, auf dem die Befehle ausgeführt werden, oder es können Befehle ausgestellt und auf dem gleichen Computer ausgeführt werden. Siehe auch [Server](s.md).

</dd> <dt>

<span id="opengl_client_memory"></span><span id="OPENGL_CLIENT_MEMORY"></span>**Client Arbeitsspeicher**
</dt> <dd>

Der Hauptspeicher (in dem Programmvariablen gespeichert werden) des Client Computers.

</dd> <dt>

<span id="opengl_clip_coordinates"></span><span id="OPENGL_CLIP_COORDINATES"></span>**Clip Koordinaten**
</dt> <dd>

Das Koordinatensystem, das der Transformation durch die Projektions Matrix folgt und der Perspektiven Division vorangestellt ist. Ansichts Volumen Clipping erfolgt in Clip Koordinaten, aber das anwendungsspezifische Clipping ist nicht. Siehe auch [anwendungsspezifisches Clipping](a.md).

</dd> <dt>

<span id="opengl_clipping"></span><span id="OPENGL_CLIPPING"></span>**Clipping**
</dt> <dd>

Entfernen des Teils eines geometrischen primitiven, der sich außerhalb des halb Raums befindet, der durch eine Clippingebene definiert ist. Punkte werden einfach abgelehnt, wenn außerhalb von. Der Teil einer Zeile oder eines Polygons, das sich außerhalb des halb Raums befindet, wird entfernt, und zusätzliche Scheitel Punkte werden nach Bedarf generiert, um die primitive innerhalb des Clipping-halb Raums abzuschließen. Geometrische Primitive und die aktuelle Raster Position (sofern angegeben) werden immer für die sechs halben Leerzeichen abgeschnitten, die durch die linke, Rechte, untere, obere, nahe und weite Ebene des Ansichts Volumens definiert werden. Anwendungen können optionale anwendungsspezifische Clippingebenen angeben, die in den Augen Koordinaten angewendet werden sollen.

</dd> <dt>

<span id="opengl_color_index"></span><span id="OPENGL_COLOR_INDEX"></span>**Farbindex**
</dt> <dd>

Ein einzelner Wert, der eine Farbe anhand des Namens anstelle des Werts darstellt. OpenGL-Farbindizes werden als kontinuierliche Werte (z. b. Gleit Komma Zahlen) behandelt, während Vorgänge wie Interpolations-und Dithering für Sie ausgeführt werden. Im Frame Puffer gespeicherte Farbindizes sind jedoch immer ganzzahlige Werte. Gleit Komma Indizes werden in ganze Zahlen konvertiert, indem auf den nächstgelegenen ganzzahligen Wert gerundet wird.

</dd> <dt>

<span id="opengl_color_index_mode"></span><span id="OPENGL_COLOR_INDEX_MODE"></span>**Farb Index Modus**
</dt> <dd>

Der Modus eines OpenGL-Kontexts, in dem die Farb Puffer Farbindizes anstelle von rot-, grün-, blau-und Alpha Farbkomponenten speichern.

</dd> <dt>

<span id="opengl_color_map"></span><span id="OPENGL_COLOR_MAP"></span>**Farbzuordnung**
</dt> <dd>

Eine Tabelle mit Index-zu-RGB-Zuordnungen, auf die von der Anzeige Hardware zugegriffen wird. Jeder Farbindex wird aus dem Farb Puffer gelesen, von der Suche in der Farb Map in ein RGB-Triple konvertiert und an den Monitor gesendet.

</dd> <dt>

<span id="opengl_component"></span><span id="OPENGL_COMPONENT"></span>**Zulieferern**
</dt> <dd>

Ein einzelner, kontinuierlicher (z. b. Gleit Komma Wert), der eine Intensität oder Menge darstellt. Normalerweise stellt ein Komponenten Wert von NULL den minimalen Wert bzw. die minimale Intensität dar, und der Komponenten Wert 1 stellt den maximalen Wert bzw. die maximale Intensität dar, obwohl andere Normalisierungen manchmal verwendet werden. Da Komponenten Werte in einem normalisierten Bereich interpretiert werden, werden Sie unabhängig von der eigentlichen Auflösung angegeben. Der RGB-Triple (1, 1, 1) ist z. b. weiß, unabhängig davon, ob die Farb Puffer jeweils 4, 8 oder 12 Bits speichern. Außerhalb des gültigen Bereichs befindlichen Komponenten werden in der Regel an den normalisierten Bereich gebunden, nicht abgeschnitten oder anderweitig interpretiert. Beispielsweise wird das RGB-Triple (1,4, 1,5, 0,9) an (1,0, 1,0, 0,9) gebunden, bevor es zum Aktualisieren des Farb Puffers verwendet wird. Rot, grün, blau, Alpha und Tiefe werden immer als Komponenten und nie als Indizes behandelt.

</dd> <dt>

<span id="opengl_context"></span><span id="OPENGL_CONTEXT"></span>**Kontext**
</dt> <dd>

Ein kompletter Satz von OpenGL-Zustandsvariablen. Beachten Sie, dass der Frame Puffer-Inhalt nicht Teil des OpenGL-Zustands ist, sondern dass die Konfiguration des Frame Puffer ist.

</dd> <dt>

<span id="opengl_convex"></span><span id="OPENGL_CONVEX"></span>**konvexe**
</dt> <dd>

Bedingung eines Polygons, bei dem keine gerade Linie in der Ebene des Polygons mehr als zwei Punkte schneidet.

</dd> <dt>

<span id="opengl_convex_hull"></span><span id="OPENGL_CONVEX_HULL"></span>**konforme Hülle**
</dt> <dd>

Der kleinste konforme Bereich, der eine angegebene Gruppe von Punkten einschließt. In zwei Dimensionen ist die konforme Hülle konzeptionell durch Streckung eines Gummibandes um die Punkte zu finden, sodass alle Punkte innerhalb des Bands liegen.

</dd> <dt>

<span id="opengl_coordinate_system"></span><span id="OPENGL_COORDINATE_SYSTEM"></span>**Koordinatensystem**
</dt> <dd>

In einem n-dimensionalen Raum ein Satz von n linear unabhängigen Vektoren, die an einem Punkt (Ursprung genannt) verankert sind. Eine Gruppe von Koordinaten gibt einen Punkt im ndimensionalen Spacein-Bereich an, einen Satz von n linear unabhängigen Vektoren, die an einem Punkt (dem Ursprungs Ursprung) verankert sind. Anhand einer Gruppe von Koordinaten wird ein Punkt im Raum (oder ein Vektor vom Ursprung) festgelegt. Dazu wird die Strecke zum Punkt (oder zur Spitze des Vektors) entlang des jeweiligen Vektors angegeben. (oder ein Vektor vom Ursprung), indem Sie angibt, wie weit die einzelnen Vektoren bewegt werden sollen, um den Punkt (oder die Spitze des Vektors) zu erreichen.

</dd> <dt>

<span id="opengl_culling"></span><span id="OPENGL_CULLING"></span>**cullingfunktionsgruppe**
</dt> <dd>

Der Prozess, bei dem eine Vorder-oder Rückseite eines Polygons eliminiert wird, sodass das Gesicht nicht gezeichnet wird.

</dd> <dt>

<span id="opengl_current_matrix"></span><span id="OPENGL_CURRENT_MATRIX"></span>**aktuelle Matrix**
</dt> <dd>

Eine Matrix, die Koordinaten in einem Koordinatensystem in Koordinaten eines anderen Systems umwandelt. OpenGL enthält drei aktuelle Matrizen: die Modelview-Matrix, die Objekt Koordinaten (vom Programmierer angegebene Koordinaten) in die Augen Koordinaten umwandelt. die Perspektiven Matrix, die Eye-Koordinaten in Clip Koordinaten umwandelt. und die Textur Matrix, die angegebene oder generierte Texturkoordinaten transformiert, wie in der Matrix beschrieben. Jede aktuelle Matrix ist das oberste Element in einem Stapel von Matrizen. Die drei Stapel können mit OpenGL-matrixbearbeitungs Befehlen manipuliert werden.

</dd> <dt>

<span id="opengl_current_raster_position"></span><span id="OPENGL_CURRENT_RASTER_POSITION"></span>**aktuelle Raster Position**
</dt> <dd>

Eine Fenster Koordinaten Position, die die Platzierung eines bilprimitivs angibt, wenn es rasteriert wird. Die aktuelle Raster Position und andere aktuelle Raster Parameter werden aktualisiert, wenn glRasterPos aufgerufen wird.

</dd> </dl>

 

 




