---
description: Beleuchtung wird verwendet, um Objekte in einer Szene zu beleuchten.
ms.assetid: 0751bb76-611a-41c4-aab2-aa6f68b61b0e
title: Beleuchtung und Material (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6f44a12c1be1e7a14f7bfe176d7f391901d2dac
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392349"
---
# <a name="lights-and-materials-direct3d-9"></a>Beleuchtung und Material (Direct3D 9)

Beleuchtung wird verwendet, um Objekte in einer Szene zu beleuchten. Wenn Beleuchtung aktiviert ist, berechnet Direct3D die Farbe jedes Objekt Scheitel Punkts basierend auf einer Kombination aus:

> [!Note]  
> Dieser Abschnitt ist nur für die Pipeline mit fester funktionsfähig. Programmierbare Shader führen die gesamte Beleuchtung explizit aus.

 

-   Die aktuelle Material Farbe und die texeln in einer zugeordneten Textur Zuordnung.
-   Die diffusen und Glanz Farben im Scheitelpunkt, falls angegeben.
-   Die Farbe und Intensität des Lichts, das von Lichtquellen in der Szene oder der Umgebungs hell Ebene der Szene erzeugt wird.

Wenn Sie Direct3D-Beleuchtung und Material verwenden, ermöglichen Sie Direct3D, die Details der Beleuchtung für Sie zu behandeln. Fortgeschrittene Benutzer können bei Bedarf Beleuchtung selbst ausführen.

Die Verwendung von Beleuchtung und Material ist ein großer Unterschied in der Darstellung der gerenderten Szene. Material definiert, wie das Licht aus einer Oberfläche reflektiert wird. Die Licht Ebenen "direkt Licht" und "Ambient" definieren das Licht, das reflektiert wird. Sie müssen Materialien zum Rendering einer Szene verwenden, wenn Beleuchtung aktiviert ist. Beleuchtung ist nicht erforderlich, um eine Szene zu rendern, aber Details in einer Szene ohne Licht sind nicht sichtbar. Das Rendern einer nicht beleuchteten Szene führt bestenfalls zu einer Silhouette der Objekte in der Szene. Dies ist für die meisten Zwecke nicht ausreichend.

## <a name="direct-light-vs-ambient-light"></a>Direktes Licht im Vergleich zu Ambient Light

Obwohl sowohl das direkte als auch das Ambient-Lichtobjekte in einer Szene beleuchtet, sind Sie unabhängig voneinander, Sie haben sehr unterschiedliche Effekte und erfordern, dass Sie mit Ihnen auf ganz unterschiedliche Weise arbeiten.

Direct Light ist genau das: Direct. Direct Light hat immer Richtung und Farbe, und es ist ein Faktor für Schattierungs Algorithmen, wie z. b. die Schattierung von Gouraud. Unterschiedliche Arten von Lichtern geben direktes Licht auf unterschiedliche Weise aus, wodurch besondere Dämpfungseffekte entstehen. Sie erstellen eine Reihe von hellen Parametern für direktes Licht durch Aufrufen der [**IDirect3DDevice9:: setlight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight) -Methode.

Ambient Light ist praktisch überall in einer Szene. Sie können sich dies als allgemeines Maß an Licht vorstellen, das eine ganze Szene, unabhängig von den Objekten und deren Positionen in der Szene, füllt. Ambient Light hat keine Position oder Richtung, sondern nur Farbe und Intensität. Jedes Licht fügt dem gesamten Umgebungslicht in einer Szene hinzu. Legen Sie die lightweightsebene mit einem Aufrufen der [**IDirect3DDevice9:: setrenderstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) -Methode fest, wobei D3DRS \_ Ambient als *State* -Parameter und die gewünschte RGBA-Farbe als Wert Parameter angegeben wird.

Die helle Farbe der Umgebung hat die Form eines RGBA-Werts, wobei jede Komponente ein ganzzahliger Wert zwischen 0 und 255 ist. Dies ist im Gegensatz zu den meisten Farbwerten in Direct3D.

Zum Generieren von RGBA-Werten können Sie das [**D3DCOLOR \_ RGBA**](d3dcolor-rgba.md) -Makro verwenden. Die roten, grünen und blauen Komponenten werden kombiniert, um die endgültige Farbe des Umgebungslichts zu bilden. Die Alpha Komponente steuert die Transparenz der Farbe. Bei Verwendung der Hardwarebeschleunigung oder der RGB-Emulation wird die Alpha Komponente ignoriert.

## <a name="direct3d-light-model-vs-nature"></a>Direct3D Light Model im Vergleich zu Nature

Wenn das Licht aus einer Quelle ausgegeben wird, wird es in der Natur von Hunderten, wenn nicht Tausenden oder Millionen von Objekten, vor dem Erreichen des Benutzers reflektiert. Jedes Mal, wenn es reflektiert wird, wird ein Licht durch eine Oberfläche aufgenommen, einige sind in zufälliger Richtung verteilt, und der Rest geht an eine andere Oberfläche oder an den Benutzer. Dieser Prozess wird fortgesetzt, bis das Licht auf nichts reduziert ist oder ein Benutzer das Licht wahrnimmt.

Natürlich sind die Berechnungen, die erforderlich sind, um das natürliche Verhalten von Licht zu simulieren, zu zeitaufwändig, um für echt Zeit Direct3D-Grafiken zu verwenden. Aus diesem Grund ähnelt das Direct3D Light-Modell der Art und Weise, wie Light in der natürlichen Welt funktioniert. Direct3D beschreibt Licht in Form von roten, grünen und blauen Komponenten, die kombiniert werden, um eine endgültige Farbe zu erstellen.

Wenn in Direct3D eine Oberfläche von Licht reflektiert wird, interagiert die helle Farbe mathematisch mit der Oberfläche, um die Farbe zu erstellen, die schließlich auf dem Bildschirm angezeigt wird. Spezifische Informationen zu den Algorithmen, die Direct3D verwendet, finden Sie unter [Mathematik der Beleuchtung (Direct3D 9)](mathematics-of-lighting.md).

Das Direct3D Light-Modell generalisiert Licht in zwei Typen: Ambient Light und Direct Light. Jede verfügt über unterschiedliche Attribute, und jede interagiert mit dem Material einer-Oberfläche auf unterschiedliche Weise. Ambient Light ist ein Licht, das so weit verstreut ist, dass seine Richtung und Quelle unbestimmt sind: Es wird ein niedriges Maß an Intensität überall aufrechterhalten. Die indirekte Beleuchtung, die von Fotografen verwendet wird, ist ein gutes Beispiel für Ambient Light. Ambient Light in Direct3D hat, wie in der Natur, keine echte Richtung oder Quelle, sondern nur eine Farbe und Intensität. Tatsächlich ist die Umgebungsbeleuchtung vollständig unabhängig von Objekten in einer Szene, die Licht generieren. Ambient Light trägt nicht zur Glanz Betrachtung bei.

Direktes Licht ist das Licht, das von einer Quelle innerhalb einer Szene generiert wird. Sie verfügt immer über Farbe und Intensität und verläuft in einer angegebenen Richtung. Direct Light interagiert mit dem Material einer-Oberfläche, um Glanzlichter zu erstellen, und die Richtung wird als Faktor für Schattierungs Algorithmen verwendet, einschließlich der Schattierung von Gouraud. Wenn Direct Light reflektiert wird, wird es in einer Szene nicht zum Umgebungs hellen Niveau beitragen. Die Quellen in einer Szene, die Direct Light generieren, haben unterschiedliche Eigenschaften, die sich darauf auswirken, wie Sie eine Szene ausleuchten.

Außerdem verfügt das Material eines Polygons über Eigenschaften, die sich darauf auswirken, wie das Polygon das empfangene Licht widerspiegelt. Sie legen ein einzelnes reflectionmerkmal fest, das beschreibt, wie das Material Ambient-Light reflektiert, und legen einzelne Merkmale fest, um die Glanz Fähigkeit und die diffuse Reflektion des Materials zu bestimmen. Weitere Informationen finden Sie unter [Material (Direct3D 9)](materials.md).

## <a name="color-values-for-lights-and-materials"></a>Farbwerte für Leuchten und Materialien

Direct3D beschreibt Farben in Form von vier Komponenten: rot, grün, blau und Alpha, die kombiniert werden, um eine endgültige Farbe zu bilden. Die [**D3DCOLORVALUE**](d3dcolorvalue.md) C++-Struktur ist so definiert, dass Sie Werte für jede Komponente enthält. Jeder Member ist ein Gleit Komma Wert, der in der Regel zwischen 0,0 und 1,0 (einschließlich) liegt. Obwohl sowohl Beleuchtung als auch Material die gleiche Struktur zum Beschreiben von Farben verwenden, werden die Werte in der Struktur jeweils etwas unterschiedlich verwendet.

Farbwerte für helle Quellen stellen die Menge einer bestimmten Licht Komponente dar, die Sie ausgibt. Da Lights keine Alpha Komponente verwendet, sind nur die roten, grünen und blauen Komponenten der Farbe relevant. Sie können die drei Komponenten als die roten, grünen und blauen Linsen in einem Projektions Fernsehen visualisieren. Jeder-Wert ist möglicherweise deaktiviert (ein 0,0-Wert im entsprechenden Member), er kann so hell wie möglich sein (ein 1,0-Wert), oder er kann eine bestimmte Ebene aufweisen. Die Farben, die durch die-Objektive kommen, werden kombiniert, um die endgültige Farbe des Lichts zu bilden. Eine Kombination wie R (1.0), g (1.0), B (1.0) erstellt ein weißes Licht, bei dem R (0,0), g (0,0), B (0,0) überhaupt kein Licht ausgibt. Sie können ein Licht machen, das nur eine Komponente ausgibt, was zu einem reinen roten, grünen oder blauen Licht führt. oder das Licht kann Kombinationen verwenden, um Farben wie gelb oder lila auszugeben. Sie können sogar negative Farbkomponentenwerte festlegen, um ein "dunkles Licht" zu erstellen, das das Licht aus einer Szene entfernt. Oder Sie können die Komponenten auf einen Wert festlegen, der größer als 1,0 ist, um ein extrem helles Licht zu erzeugen.

Mit Materialien hingegen stellen Farbwerte dar, wie viel von einer Licht Komponente durch eine Oberfläche reflektiert wird, die mit diesem Material gerendert wird. Ein Material, dessen Farbkomponenten R (1.0), G (1.0), B (1.0), a (1.0) sind, spiegelt das gesamte Licht wider, das seine Art darstellt. Ebenso spiegelt ein Material mit R (0,0), G (1.0), B (0,0), a (1.0) das gesamte grüne Licht wider, das darauf gerichtet ist. Material verfügen über mehrere Reflektions Werte, um verschiedene Arten von Effekten zu erstellen.

Weitere Informationen finden Sie unter: [Light Types (Direct3D 9)](light-types.md)und [Light Properties (Direct3D 9)](light-properties.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erste Schritte](getting-started.md)
</dt> </dl>

 

 
