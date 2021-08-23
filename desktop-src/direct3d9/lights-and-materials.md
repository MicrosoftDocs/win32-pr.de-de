---
description: Beleuchtung wird verwendet, um Objekte in einer Szene zu beleuchten.
ms.assetid: 0751bb76-611a-41c4-aab2-aa6f68b61b0e
title: Lights and Materials (Direct3D 9) (Beleuchtung und Materialien (Direct3D 9))
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a5ace2a80bb79d192fadc5376256eedf9229be9a36fa1d200341ccf28e961fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119277520"
---
# <a name="lights-and-materials-direct3d-9"></a>Lights and Materials (Direct3D 9) (Beleuchtung und Materialien (Direct3D 9))

Beleuchtung wird verwendet, um Objekte in einer Szene zu beleuchten. Wenn die Beleuchtung aktiviert ist, berechnet Direct3D die Farbe jedes Objektvertex basierend auf einer Kombination aus:

> [!Note]  
> Dieser Abschnitt gilt nur für die Pipeline mit fester Funktion. Programmierbare Shader führen die gesamte Beleuchtung explizit aus.

 

-   Die aktuelle Materialfarbe und die Texel in einer zugeordneten Texturkarte.
-   Die diffusen und specularen Farben am Scheitelpunkt, sofern angegeben.
-   Die Farbe und Intensität des Lichts, die von Lichtquellen in der Szene oder dem Umgebungslichtpegel der Szene erzeugt werden.

Wenn Sie Direct3D-Beleuchtung und -Materialien verwenden, ermöglichen Sie Direct3D, die Details der Beleuchtung für Sie zu verarbeiten. Fortgeschrittene Benutzer können die Beleuchtung bei Bedarf selbst durchführen.

Wie Sie mit Beleuchtung und Materialien arbeiten, macht einen großen Unterschied in der Darstellung der gerenderten Szene aus. Materialien definieren, wie Licht von einer Oberfläche reflektiert wird. Direktes Licht und Umgebungslichtpegel definieren das Licht, das reflektiert wird. Sie müssen Materialien verwenden, um eine Szene zu rendern, wenn die Beleuchtung aktiviert ist. Licht ist nicht erforderlich, um eine Szene zu rendern, aber Details in einer Szene, die ohne Licht gerendert wird, sind nicht sichtbar. Im besten Fall führt das Rendern einer unliterten Szene zu einem Bündel der Objekte in der Szene. Für die meisten Zwecke reicht dies nicht aus.

## <a name="direct-light-vs-ambient-light"></a>Direktes Licht im Vergleich zu Umgebungslicht

Obwohl sowohl direktes als auch Umgebungslicht Objekte in einer Szene beleuchten, sind sie unabhängig voneinander, sie haben sehr unterschiedliche Effekte und erfordern, dass Sie mit ihnen auf völlig unterschiedliche Weise arbeiten.

Direktes Licht ist genau das: direkt. Direktes Licht hat immer Die Richtung und Farbe und ist ein Faktor für Schattierungsalgorithmen, z. B. Gouraud-Schattierung. Verschiedene Arten von Beleuchtung geben auf unterschiedliche Weise direktes Licht aus, wodurch besondere Dämpfungseffekte entstehen. Sie erstellen einen Satz von Lichtparametern für direktes Licht, indem Sie die [**IDirect3DDevice9::SetLight-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight) aufrufen.

Umgebungslicht ist effektiv überall in einer Szene. Sie können sich dies als allgemeine Lichtebene vorstellen, die eine ganze Szene ausfüllt, unabhängig von den Objekten und ihren Positionen in dieser Szene. Umgebungslicht hat keine Position oder Richtung, sondern nur Farbe und Intensität. Jedes Licht fügt dem gesamten Umgebungslicht in einer Szene hinzu. Legen Sie die Umgebungslichtebene mit einem Aufruf der [**IDirect3DDevice9::SetRenderState-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) fest, und geben Sie D3DRS \_ AMBIENT als *State-Parameter* und die gewünschte RGBA-Farbe als Value-Parameter an.

Umgebungslichtfarbe hat die Form eines RGBA-Werts, wobei jede Komponente ein ganzzahliger Wert zwischen 0 und 255 ist. Dies unterscheidet sich von den meisten Farbwerten in Direct3D.

Sie können das [**D3DCOLOR \_ RGBA-Makro**](d3dcolor-rgba.md) verwenden, um RGBA-Werte zu generieren. Die roten, grünen und blauen Komponenten werden kombiniert, um die endgültige Farbe des Umgebungslichts zu bilden. Die Alphakomponente steuert die Transparenz der Farbe. Bei Verwendung der Hardwarebeschleunigung oder RGB-Emulation wird die Alphakomponente ignoriert.

## <a name="direct3d-light-model-vs-nature"></a>Direct3D Light Model im Vergleich zur Natur

Wenn Licht von einer Quelle ausgegeben wird, wird es in der Natur von Hunderten, wenn nicht Tausenden oder Millionen von Objekten reflektiert, bevor das Auge des Benutzers erreicht wird. Jedes Mal, wenn es reflektiert wird, wird etwas Licht von einer Oberfläche aufgenommen, einige werden in zufällige Richtungen verteilt, und der Rest geht auf eine andere Oberfläche oder auf das Auge des Benutzers über. Dieser Prozess wird fortgesetzt, bis das Licht auf nichts reduziert wird oder ein Benutzer das Licht wahrnimmt.

Natürlich sind die Berechnungen, die erforderlich sind, um das natürliche Verhalten von Licht perfekt zu simulieren, zu zeitaufwändig, um für Direct3D-Grafiken in Echtzeit zu verwenden. Daher entspricht das Direct3D-Lichtmodell im Hinblick auf die Geschwindigkeit der Funktionsweise von Licht in der natürlichen Welt. Direct3D beschreibt Licht in Bezug auf rote, grüne und blaue Komponenten, die kombiniert werden, um eine endgültige Farbe zu erstellen.

Wenn in Direct3D Licht von einer Oberfläche reflektiert wird, interagiert die helle Farbe mathematisch mit der Oberfläche selbst, um die Farbe zu erstellen, die schließlich auf dem Bildschirm angezeigt wird. Spezifische Informationen zu den Algorithmen, die Direct3D verwendet, finden Sie unter [Mathematik der Beleuchtung (Direct3D 9).](mathematics-of-lighting.md)

Das Direct3D-Lichtmodell generalisiert Licht in zwei Typen: Umgebungslicht und direktes Licht. Jede verfügt über unterschiedliche Attribute, und jede interagiert auf unterschiedliche Weise mit dem Material einer Oberfläche. Umgebungslicht ist Licht, das so weit verteilt wurde, dass seine Richtung und Quelle unbestimmt sind: Es behält überall ein niedriges Maß an Intensität bei. Die indirekte Beleuchtung, die von Beleuchtungen verwendet wird, ist ein gutes Beispiel für Umgebungslicht. Umgebungslicht in Direct3D hat, wie in der Natur, keine echte Richtung oder Quelle, sondern nur eine Farbe und Intensität. Tatsächlich ist der Umgebungslichtpegel vollständig unabhängig von Objekten in einer Szene, die Licht erzeugen. Umgebungslicht trägt nicht zur Glanzreflektion bei.

Direktes Licht ist das Licht, das von einer Quelle innerhalb einer Szene generiert wird. sie weist immer Farbe und Intensität auf und bewegt sich in einer bestimmten Richtung. Direktes Licht interagiert mit dem Material einer Oberfläche, um Glanzlichter zu erstellen, und seine Richtung wird als Faktor bei Schattierungsalgorithmen verwendet, einschließlich Gouraud-Schattierung. Wenn direktes Licht reflektiert wird, trägt es nicht zum Umgebungslichtpegel in einer Szene bei. Die Quellen in einer Szene, die direktes Licht generieren, weisen unterschiedliche Merkmale auf, die beeinflussen, wie sie eine Szene beleuchten.

Darüber hinaus verfügt das Material eines Polygons über Eigenschaften, die beeinflussen, wie dieses Polygon das empfangene Licht widerspiegelt. Sie legen ein einzelnes Reflektionsmerkmal fest, das beschreibt, wie das Material Umgebungslicht widerspiegelt, und Sie legen einzelne Merkmale fest, um die Glanz- und diffuse Reflexion des Materials zu bestimmen. Weitere Informationen finden Sie unter [Materials (Direct3D 9) (Materialien (Direct3D 9)).](materials.md)

## <a name="color-values-for-lights-and-materials"></a>Farbwerte für Beleuchtung und Materialien

Direct3D beschreibt die Farbe in Form von vier Komponenten : Rot, Grün, Blau und Alpha, die zu einer endgültigen Farbe kombiniert werden. Die C++-Struktur [**D3DCOLORVALUE**](d3dcolorvalue.md) ist so definiert, dass sie Werte für jede Komponente enthält. Jedes Element ist ein Gleitkommawert, der in der Regel von 0,0 bis einschließlich 1,0 reicht. Obwohl sowohl Licht als auch Materialien die gleiche Struktur verwenden, um Die Farbe zu beschreiben, werden die Werte in der Struktur jeweils etwas anders verwendet.

Farbwerte für Datenquellen stellen die Menge einer bestimmten Lichtkomponente dar, die sie ausgibt. Da Die Beleuchtung keine Alphakomponente verwendet, sind nur die roten, grünen und blauen Komponenten der Farbe relevant. Sie können die drei Komponenten als rote, grüne und blaue Brillen auf einem Projektionslichter visualisieren. Jede Brille kann ausgeschaltet sein (ein 0,0-Wert im entsprechenden Member), sie kann so hell wie möglich sein (ein Wert von 1,0) oder eine Ebene dazwischen. Die Farben, die durch die Brillen kommen, werden kombiniert, um die endgültige Farbe des Lichts zu bilden. Eine Kombination wie R(1.0), G(1.0), B(1.0) erstellt ein weißes Licht, wobei R(0.0), G(0.0), B(0.0) überhaupt kein Licht ausgibt. Sie können ein Licht erstellen, das nur eine Komponente ausgibt, was zu einem reinen roten, grünen oder blauen Licht führt. oder das Licht kann Kombinationen verwenden, um Farben wie Gelb oder Violett auszugeben. Sie können sogar negative Farbkomponentenwerte festlegen, um ein "dunkles Licht" zu erstellen, das tatsächlich Licht aus einer Szene entfernt. Oder Sie können die Komponenten auf einen Wert größer als 1,0 festlegen, um ein extrem helles Licht zu erzeugen.

Bei Materialien stellen farbliche Werte dagegen dar, wie viel von einer lichten Komponente von einer Oberfläche reflektiert wird, die mit diesem Material gerendert wird. Ein Material, dessen Farbkomponenten R(1.0), G(1.0), B(1.0), A(1.0) sind, spiegelt das gesamte Licht wider, das in den Weg kommt. Ebenso spiegelt ein Material mit R(0.0), G(1.0), B(0.0), A(1.0) das gesamte grüne Licht wider, das darauf gerichtet ist. Materialien verfügen über mehrere Reflexionswerte, um verschiedene Arten von Effekten zu erzeugen.

Weitere Informationen finden Sie in: [Light Types (Direct3D 9)](light-types.md)und [Light Properties (Direct3D 9)](light-properties.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erste Schritte](getting-started.md)
</dt> </dl>

 

 
