---
title: Übersicht über Geometrierealisierungen
description: In diesem Thema wird beschrieben, wie Direct2D-Geometrierealisierungen verwendet werden, um die Leistung des Geometrierenderings Ihrer App in bestimmten Szenarien zu verbessern.
ms.assetid: E8C4C4E5-3102-4F53-847E-A4C2D12A6921
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5108537e9ea9b38bebaab590178d990b44e611e56e82690e9d91ad9b56c19372
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119260134"
---
# <a name="geometry-realizations-overview"></a>Übersicht über Geometrierealisierungen

In diesem Thema wird beschrieben, wie [Direct2D-Geometrierealisierungen](direct2d-portal.md) verwendet werden, um die Leistung des Geometrierenderings Ihrer App in bestimmten Szenarien zu verbessern.

Sie enthält die folgenden Abschnitte:

-   [Was sind Geometrierealisierungen?](#what-are-geometry-realizations)
-   [Gründe für die Verwendung von Geometrierealisierungen](#why-use-geometry-realizations)
-   [Einsatz von Geometrierealisierungen](#when-to-use-geometry-realizations)
-   [Erstellen von Geometrierealisierungen](#creating-geometry-realizations)
-   [Zeichnungsgeometrierealisierungen](#drawing-geometry-realizations)
-   [Skalierung von Geometrierealisierungen](#scaling-geometry-realizations)
    -   [Verwenden von Geometrierealisierungen in Apps, die nicht skaliert werden](#using-geometry-realizations-in-apps-that-do-not-scale)
    -   [Verwenden von Geometrierealisierungen in Apps, die um eine kleine Menge skaliert werden](#using-geometry-realizations-in-apps-that-scale-by-a-small-amount)
    -   [Verwenden von Geometrierealisierungen in Apps, die um eine große Menge skaliert werden](#using-geometry-realizations-in-apps-that-scale-by-a-large-amount)
-   [Zugehörige Themen](#related-topics)

## <a name="what-are-geometry-realizations"></a>Was sind Geometrierealisierungen?

Geometrierealisierungen, die in Windows 8.1 eingeführt wurden, sind eine neue Art von Zeichnungsprimitive, die [es Direct2D-Apps](direct2d-portal.md) einfach macht, die Leistung des Geometrierenderings in bestimmten Fällen zu verbessern. Geometrierealisierungen werden durch die [**ID2D1GeometryRealization-Schnittstelle**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1geometryrealization) dargestellt.

## <a name="why-use-geometry-realizations"></a>Gründe für die Verwendung von Geometrierealisierungen

Wenn [Direct2D](direct2d-portal.md) ein [**ID2D1Geometry-Objekt**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) rendert, muss es diese Geometrie in eine Form konvertieren, die die Grafikhardware durch einen Prozess namens Mosaik versteht. In der Regel muss Direct2D für jeden gezeichneten Rahmen geometrietesseln, auch wenn sich die Geometrie nicht ändert. Wenn Ihre App bei jedem Frame die gleiche Geometrie rendert, stellt das wiederholte Neusesseln verschwendeten Rechenaufwand dar. Es ist recheneffizienter, das Mosaik oder sogar die vollständige Rasterung der Geometrie zwischenspeichern und diese zwischengespeicherte Darstellung für jeden Frame zu zeichnen, anstatt das Mosaik wiederholt neu zu erstellen.

Entwickler lösen dieses Problem häufig, wenn sie die vollständige Rasterung der Geometrie zwischenspeichern. Insbesondere ist es üblich, eine neue Bitmap zu erstellen, die Geometrie in diese Bitmap zu rastern und diese Bitmap dann bei Bedarf in die Szene zu zeichnen. (Dieser Ansatz wird im Abschnitt [Geometrierendering](improving-direct2d-performance.md) unter Verbessern der Leistung von Direct2D-Apps beschrieben.) Dieser Ansatz ist zwar sehr recheneffizient, hat jedoch einige Nachteile:

-   Die zwischengespeicherte Bitmap ist empfindlich auf Änderungen in der Transformation, die auf die Szene angewendet wird. Beispielsweise kann das Skalieren der Rasterung zu einer spürbaren Skalierung von Artefakten führen. Das Abmildern dieser Artefakte mit hochwertigen Skalierungsalgorithmen kann rechenintensiv sein.
-   Die zwischengespeicherte Bitmap verbraucht viel Arbeitsspeicher, insbesondere, wenn sie mit hoher Auflösung rastert wird.

Geometrierealisierungen stellen eine alternative Möglichkeit zum Zwischenspeichern der Geometrie dar, die die oben genannten Nachteile vermeidet. Geometrierealisierungen werden nicht durch Pixel dargestellt (wie bei einer vollständigen Rasterung), sondern durch Punkte auf einer mathematischen Ebene. Aus diesem Grund sind sie weniger empfindlich als vollständige Rasterungen für Skalierung und andere Bearbeitungen und verbrauchen deutlich weniger Arbeitsspeicher.

## <a name="when-to-use-geometry-realizations"></a>Einsatz von Geometrierealisierungen

Erwägen Sie die Verwendung von Geometrierealisierungen, wenn Ihre App komplexe Geometrien rendert, deren Formen sich selten ändern, die jedoch möglicherweise sich ändernden Transformationen unterliegen.

Stellen Sie sich beispielsweise eine Zuordnungsanwendung vor, die eine statische Karte zeigt, der Benutzer jedoch das Vergrößern und Verkleinern ermöglicht. Diese App kann von der Verwendung von Geometrierealisierungen profitieren. Da die gerenderten Geometrien statisch bleiben, ist es hilfreich, sie zwischenspeichern, um Mosaikarbeit zu sparen. Da die Karten jedoch skaliert werden, wenn der Benutzer zoomt, ist das Zwischenspeichern einer vollständigen Rasterung aufgrund von Skalierungsartefakten nicht ideal. Durch das Zwischenspeichern von Geometrierealisierungen kann die App Neusesseln vermeiden und gleichzeitig während der Skalierung eine hohe visuelle Qualität aufrechterhalten.

Betrachten Sie andererseits eine Idoscope-App mit animierter Geometrie, die sich ständig ändert. Diese App würde wahrscheinlich nicht von der Verwendung von Geometrierealisierungen profitieren. Da sich die Formen selbst von Frame zu Frame ändern, ist es nicht sinnvoll, ihre Mosaiken zwischenspeichern. Der beste Ansatz für diese App ist das direkte [**Zeichnen von ID2D1Geometry-Objekten.**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)

## <a name="creating-geometry-realizations"></a>Erstellen von Geometrierealisierungen

Ein [**ID2D1GeometryRealization-Objekt**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1geometryrealization) muss aus einem vorhandenen [**ID2D1Geometry-Objekt erstellt**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) werden. Rufen Sie zum Erstellen einer Geometrierealisierung die [**CreateFilledGeometryRealization-Methode**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1devicecontext1-createfilledgeometryrealization) oder die [**CreateStrokedGeometryRealization-Methode**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1devicecontext1-createstrokedgeometryrealization) auf, und übergeben Sie die zu realisierende **ID2D1Geometry.**

-   [**CreateFilledGeometryRealization**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1devicecontext1-createfilledgeometryrealization) erstellt eine Realisierung des Inneren der Form: der Bereich, der durch Aufrufen von [**FillGeometry gezeichnet wird.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry)
-   [**CreateStrokedGeometryRealization**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1devicecontext1-createstrokedgeometryrealization) erstellt eine Realisierung des Strichs der Form: der Bereich, der durch Aufrufen von [**DrawGeometry gezeichnet wird.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry)

Beide Arten der Geometrierealisierung werden durch die [**ID2D1GeometryRealization-Schnittstelle**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1geometryrealization) dargestellt.

Beim Erstellen einer Geometrierealisierung muss [Direct2D](direct2d-portal.md) alle Kurven in der bereitgestellten Geometrie auf polygonale Näherungen abflachen. Sie müssen einen Flachungstoleranzparameter für die Erstellungsmethode bereitstellen. Dadurch wird der maximale Abstand in geräteunabhängigen Pixeln (DEVICE-Independent Pixels, DIPs) zwischen der wahren Kurve der Geometrie und ihrer polygonalen Näherung angegeben. Je niedriger die von Ihnen zur Verfügung stellende Flachkeitstoleranz, desto höher ist die Genauigkeit des resultierenden Geometrierealisierungsobjekts. Auf ähnliche Weise führt die Bereitstellung einer höheren Flachkeitstoleranz zu einer Geometrieerreichung mit geringerer Genauigkeit. Beachten Sie, dass Geometrierealisierungen mit höherer Genauigkeit teurer zu zeichnen sind als diejenigen mit geringerer Genauigkeit, aber sie können vor der Einführung sichtbarer Artefakte weiter skaliert werden. Eine Anleitung zur Verwendung von Flachkeitstoleranzen finden Sie weiter unten unter [Skalieren von Geometrierealisierungen.](#scaling-geometry-realizations)

> [!Note]  
> Geometrierealisierungsobjekte sind einem bestimmten Grafikgerät zugeordnet: Es handelt sich um geräteabhängige Ressourcen.

 

## <a name="drawing-geometry-realizations"></a>Zeichnungsgeometrierealisierungen

Das Zeichnen von Geometrierealisierungen ähnelt dem Zeichnen anderer [Direct2D-Primitive](direct2d-portal.md) wie Bitmaps. Rufen Sie dazu die [**DrawGeometryRealization-Methode**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1devicecontext1-drawgeometryrealization) auf, und übergeben Sie ihr das zu zeichnende Geometrierealisierungsobjekt und den zu verwendenden Pinsel. Wie bei anderen Direct2D-Zeichnungsmethoden müssen Sie **DrawGeometryRealization** zwischen Aufrufen von [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) und [**EndDraw aufrufen.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw)

## <a name="scaling-geometry-realizations"></a>Skalierung von Geometrierealisierungen

Geometrierealisierungen, wie andere [Direct2D-Primitive,](direct2d-portal.md) achten auf den Transformationssatz im Gerätekontext. Obwohl Übersetzungs- und Drehungstransformationen keine Auswirkungen auf die visuelle Qualität von Geometrierealisierungen haben, können Skalierungstransformationen visuelle Artefakte erzeugen.

Insbesondere kann das Anwenden einer ausreichend großen Skala auf jede Geometrierealisierung die polygonale Näherung der wahren Kurven zeigen. Die Abbildung zeigt ein Paar elliptischer Geometrierealisierungen (Füllung und Strich), die zu weit hochskaliert wurden. Kurvenflachende Artefakte sind sichtbar.

![ein Paar elliptischer Geometrierealisierungen (Füllung und Strich), die zu weit hochskaliert wurden. Kurvenverflachende Artefakte sind sichtbar.](images/zoomed-in.png)

Apps, die für die visuelle Qualität sensibel sind, sollten Maßnahmen ergreifen, um sicherzustellen, dass dies nicht geschieht. Wie Sie die Skalierung handhaben, hängt von den Anforderungen Ihrer App ab. Im Folgenden finden Sie mehrere empfohlene Ansätze für verschiedene App-Typen.

### <a name="using-geometry-realizations-in-apps-that-do-not-scale"></a>Verwenden von Geometrierealisierungen in Apps, die nicht skaliert werden

Wenn Ihre App keine Skalierung der Geometrierealisierungen vor sich geht, ist es sicher, die Realisierungen nur einmal mithilfe einer einzelnen Flachungstoleranz zu erstellen. (Transformationen ohne Skalierung wirken sich nicht auf die visuelle Qualität gerenderter Geometrierealisierungen aus.) Verwenden Sie [**die ComputeFlatteningTolerance-Funktion,**](/previous-versions/windows/desktop/legacy/dn280327(v=vs.85)) um die entsprechende Flatteningtoleranz für den DPI zu berechnen:


```C++
    float dpiX, dpiY;
    deviceContext->GetDpi(&dpiX, &dpiY);

    float flatteningTolerance = D2D1::ComputeFlatteningTolerance(
        D2D1::Matrix3x2F::Identity(),   // apply no additional scaling transform
        dpiX,                           // horizontal DPI
        dpiY                            // vertical DPI
        );
```



### <a name="using-geometry-realizations-in-apps-that-scale-by-a-small-amount"></a>Verwenden von Geometrierealisierungen in Apps, die um eine kleine Menge skaliert werden

Wenn Ihre App eine Geometrierealisierung nur um einen kleinen Betrag hochskalieren kann (z. B. bis zu 2x oder 3x), kann es sinnvoll sein, einfach einmal die Geometrierealisierung zu erstellen, mit einer proportional geringeren Vereinfachttoleranz als der Standard. Dies führt zu einer höheren Genauigkeitsrealisierung, die vor dem Auftreten von Skalierungsartefakten erheblich hochskaliert werden kann. der Vor- und Abkniff ist, dass das Zeichnen der höheren Genauigkeitsrealisierung mehr Arbeit erfordert.

Angenommen, Sie wissen, dass Ihre App eine Geometrierealisierung nie um mehr als das 2-Fache skalieren wird. Ihre App kann die Geometrierealisierung mithilfe einer vereinfachten Toleranz erstellen, die die Hälfte des Standardwerts ist, und die Umsetzung einfach nach Bedarf auf das 2-fache skalieren. Verwenden Sie [**die ComputeFlatteningTolerance-Funktion,**](/previous-versions/windows/desktop/legacy/dn280327(v=vs.85)) um die entsprechende Flatteningtoleranz zu berechnen, indem Sie 2,0 als *maxZoomFactor-Parameter* übergeben:


```C++
    float dpiX, dpiY;
    deviceContext->GetDpi(&dpiX, &dpiY);
    
    float flatteningTolerance = D2D1::ComputeFlatteningTolerance(
        D2D1::Matrix3x2F::Identity(),   // apply no additional scaling transform
        dpiX,                           // horizontal DPI
        dpiY,                           // vertical DPI
        2.0f                            // realization can be scaled by an additional 2x
        );
```



### <a name="using-geometry-realizations-in-apps-that-scale-by-a-large-amount"></a>Verwenden von Geometrierealisierungen in Apps, die um eine große Menge skaliert werden

Wenn Ihre App eine Geometrierealisierung um große Mengen hoch- oder herunterskalieren kann (z. B. um das Zehn- oder Mehr), ist die entsprechende Skalierung komplizierter.

Für die meisten dieser Apps wird empfohlen, die Geometrierealisierung bei progressiv niedrigeren Flatteningtoleranzen neu zu erstellen, während die Szene hochskaliert wird, um die visuelle Genauigkeit zu erhalten und die Skalierung von Artefakten zu vermeiden. Ebenso sollte die App beim herunterskalierten Herunterskalieren der Szene die Geometrierealisierungen bei progressiv höheren Flatteningtoleranzen neu erstellen, um zu vermeiden, dass Details verschwendet gerendert werden, die nicht sichtbar sind. Die App sollte die Geometrierealisierungen nicht bei jeder Skalierungsänderung neu erstellen, da dies den Zweck der Zwischenspeicherung der Mosaikarbeit verfängt. Stattdessen sollte die App die Geometrierealisierungen seltener neu erstellen, z. B. nach jeder 2-fachen Erhöhung oder Verringerung der Skalierung.

Jedes Mal, wenn sich die Skalierung in einer App als Reaktion auf die Benutzerinteraktion ändert, könnte die App die neue Skala mit der Skala vergleichen, auf der die Geometrierealisierungen zuletzt erstellt wurden (z. B. in einem **m \_ lastScale-Member** gespeichert). Wenn die beiden Werte nahe liegen (in diesem Fall innerhalb des Faktors 2), wird keine weitere Aktion ergriffen. Wenn die beiden Werte jedoch nicht nahe liegen, werden die Geometrierealisierungen neu erstellt. Die [**ComputeFlatteningTolerance-Funktion**](/previous-versions/windows/desktop/legacy/dn280327(v=vs.85)) wird verwendet, um eine für die neue Skalierung geeignete Flatteningtoleranz zu berechnen, und **m \_ lastScale** wird auf die neue Skala aktualisiert.

Darüber hinaus erstellt die App immer Mithilfe einer geringeren Toleranz als die, die normalerweise für die neue Skala verwendet wird, indem sie den Wert 2 als *maxZoomFactor-Parameter* an [**ComputeFlatteningTolerance übergibt.**](/previous-versions/windows/desktop/legacy/dn280327(v=vs.85)) Dadurch können die neuen Geometrierealisierungen um einen zusätzlichen Faktor von 2 hochskaliert werden, ohne dass Skalierungsartefakte entstehen.

> [!Note]  
> Der hier beschriebene Ansatz ist möglicherweise nicht für alle Apps geeignet. Wenn Ihre App beispielsweise zulässt, dass die Szene sehr schnell um sehr große Faktoren skaliert werden kann (z. B. wenn sie einen Schieberegler "Zoom" enthält, der von 100 % auf 1.000.000 % in der Spanne von einigen Frames verschoben werden kann), kann dieser Ansatz zu übermäßiger Arbeit führen, indem die Geometrierealisierungen jedes Frames neu erstellen. Ein alternativer Ansatz besteht in der Neuerstellung der Geometrierealisierungen erst, nachdem jede Bearbeitung der Skalierung der Szene abgeschlossen wurde (z. B. nachdem der Benutzer eine Heftbewegung abgeschlossen hat).

 

## <a name="related-topics"></a>Zugehörige Themen

[Übersicht über Geometrien](direct2d-geometries-overview.md)

[Verbessern der Leistung von Direct2D-Apps](improving-direct2d-performance.md)

[Allgemeine Richtlinien zum Rendern komplexer statischer Inhalte](improving-direct2d-performance.md)

[**ID2D1DeviceContext1**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1devicecontext1)

[**ID2D1GeometryRealization**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1geometryrealization)

[**ComputeFlatteningTolerance-Funktion**](/previous-versions/windows/desktop/legacy/dn280327(v=vs.85))