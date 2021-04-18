---
title: Übersicht über Geometrierealisierungen
description: In diesem Thema wird beschrieben, wie Sie mithilfe von Direct2D-Geometrie-neufunktionen in bestimmten Szenarien die Leistung der Geometrie Leistung Ihrer APP verbessern.
ms.assetid: E8C4C4E5-3102-4F53-847E-A4C2D12A6921
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b903e047ee58a803a7584aaca407281fc803e30
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106340911"
---
# <a name="geometry-realizations-overview"></a>Übersicht über Geometrierealisierungen

In diesem Thema wird beschrieben, wie Sie mithilfe von [Direct2D](direct2d-portal.md) -Geometrie-neufunktionen in bestimmten Szenarien die Leistung der Geometrie Leistung Ihrer APP verbessern.

Sie enthält die folgenden Abschnitte:

-   [Was sind Geometrie-neusetzungen?](#what-are-geometry-realizations)
-   [Gründe für die Verwendung von Geometrie-Neumessungen](#why-use-geometry-realizations)
-   [Verwendungszwecke von Geometrie-Neumessungen](#when-to-use-geometry-realizations)
-   [Erstellen von Geometrie-Neumessungen](#creating-geometry-realizations)
-   [Zeichnen von Geometrie-Neumessungen](#drawing-geometry-realizations)
-   [Skalieren von Geometry-Neuerungen](#scaling-geometry-realizations)
    -   [Verwenden von Geometrie-Neuerungen in apps, die nicht skaliert werden](#using-geometry-realizations-in-apps-that-do-not-scale)
    -   [Verwenden von Geometrie-Neuerungen in apps, die sich um eine kleine Menge skalieren](#using-geometry-realizations-in-apps-that-scale-by-a-small-amount)
    -   [Verwenden von Geometrie-Neuerungen in apps, die sich um eine große Menge skalieren](#using-geometry-realizations-in-apps-that-scale-by-a-large-amount)
-   [Zugehörige Themen](#related-topics)

## <a name="what-are-geometry-realizations"></a>Was sind Geometrie-neusetzungen?

In Windows 8.1 eingeführte Geometrie-Real Messungen sind eine neue Art von Zeichnungs primitiven, die es [Direct2D](direct2d-portal.md) -apps erleichtern, die Leistung von Geometrie Rendering in bestimmten Fällen zu verbessern. Geometrie-Neumessungen werden durch die [**ID2D1GeometryRealization**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1geometryrealization) -Schnittstelle dargestellt.

## <a name="why-use-geometry-realizations"></a>Gründe für die Verwendung von Geometrie-Neumessungen

Wenn [Direct2D](direct2d-portal.md) ein [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) -Objekt rendert, muss es diese Geometrie in ein Formular konvertieren, das die Grafikhardware durch einen Prozess mit dem Namen "Mosaik" versteht. In der Regel muss Direct2D die Geometrie jedes Frame, das Sie gezeichnet hat, verändern, auch wenn sich die Geometrie nicht ändert. Wenn Ihre APP die gleiche Geometrie jedes Frame rendert, stellt die wiederholte Wiederholung einen verlorenen Berechnungs Aufwand dar. Es ist rechnerisch effizienter, das Mosaik oder sogar die vollständige rasterisierung der Geometrie zwischenzuspeichern und die zwischengespeicherte Darstellung jedes Frames zu zeichnen, anstatt wiederholt zu werden.

Eine gängige Methode, mit der Entwickler dieses Problem lösen können, ist das Zwischenspeichern der vollständigen rasterisierung der Geometrie. Insbesondere ist es üblich, eine neue Bitmap zu erstellen, die Geometrie auf diese Bitmap zu setzen und diese Bitmap nach Bedarf in die Szene zu zeichnen. (Dieser Ansatz wird im Abschnitt [Geometrie Rendering](improving-direct2d-performance.md) unter Verbessern der Leistung von Direct2D-apps beschrieben.) Dieser Ansatz ist zwar sehr Rechen effizient, hat jedoch einige Nachteile:

-   Die zwischengespeicherte Bitmap ist sensibel für Änderungen in der Transformation, die auf die Szene angewendet wird. Beispielsweise kann das Skalieren der rasterisierung zu merkbaren Skalierungs Artefakten führen. Das Verringern dieser Artefakte mit hochwertigen Skalierungs Algorithmen kann Rechen intensiv sein.
-   Die zwischengespeicherte Bitmap beansprucht eine beträchtliche Menge an Arbeitsspeicher, insbesondere, wenn Sie mit hoher Auflösung gerengt wird.

Geometry-Neueinstellungen stellen eine alternative Möglichkeit zum Zwischenspeichern von Geometrie dar, die die obigen Nachteile vermeidet. Geometrie-Neuberechnungen werden nicht durch Pixel dargestellt (wie bei einer vollständigen rasterisierung), sondern durch Punkte auf einer mathematischen Ebene. Aus diesem Grund sind Sie weniger sensibel als vollständige rasterierungen bei der Skalierung und anderen Manipulationen, und Sie verbrauchen erheblich weniger Arbeitsspeicher.

## <a name="when-to-use-geometry-realizations"></a>Verwendungszwecke von Geometrie-Neumessungen

Sie sollten die Verwendung von Geometrie-Neuerungen in Erwägung ziehen, wenn Ihre APP komplexe Geometrien rendert, deren Formen selten geändert werden, die jedoch veränderliche Transformationen unterliegen

Stellen Sie sich z. b. eine Zuordnungs Anwendung vor, die eine statische Zuordnung anzeigt, die dem Benutzer jedoch das Vergrößern und verkleinern ermöglicht. Diese APP kann von der Verwendung von Geometrie-Neumessungen profitieren. Da die zu rendernden Geometrien statisch bleiben, ist es sinnvoll, Sie zwischenzuspeichern, um Mosaik Vorgänge zu speichern. Da die Zuordnungen jedoch skaliert werden, wenn der Benutzer vergrößert wird, ist das Zwischenspeichern einer vollständigen rasterisierung aufgrund von Skalierungs Artefakten nicht ideal. Durch das Zwischenspeichern von Geometrie Vorgängen kann die APP eine Wiederholung vermeiden, während gleichzeitig eine hohe visuelle Qualität während der Skalierung gewährleisten wird.

Nehmen wir andererseits eine Kaleidoskop-App mit animierter Geometrie, die sich ständig ändert. Diese APP wäre wahrscheinlich nicht von der Verwendung von Geometrie-Neumessungen profitieren. Da sich die Formen selbst von Frame zu Frame ändern, ist es nicht sinnvoll, die Mosaik Vorgänge zwischenzuspeichern. Der beste Ansatz für diese APP besteht darin, [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) -Objekte direkt zu zeichnen.

## <a name="creating-geometry-realizations"></a>Erstellen von Geometrie-Neumessungen

Ein [**ID2D1GeometryRealization**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1geometryrealization) -Objekt muss aus einem vorhandenen [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) -Objekt erstellt werden. Um eine Geometrie zu erstellen, rufen Sie die Methode " [**kreatefilledgeometryrealisation**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1devicecontext1-createfilledgeometryrealization) " oder die Methode " [**kreatestrokedgeometryrealisation**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1devicecontext1-createstrokedgeometryrealization) " auf, und übergeben Sie die **ID2D1Geometry** , um Sie zu realisieren.

-   [**Createfilledgeometryrealisation**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1devicecontext1-createfilledgeometryrealization) erstellt eine Realisierung des Inneren der Form: der Bereich, der durch den Aufruf von [**fillgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry)gezeichnet wird.
-   [**Createstrokedgeometryrealisation**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1devicecontext1-createstrokedgeometryrealization) erstellt eine Realisierung des Strichs der Form: der Bereich, der durch den Aufruf von [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry)gezeichnet wird.

Beide Arten der Geometrie-Realisierung werden durch die [**ID2D1GeometryRealization**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1geometryrealization) -Schnittstelle dargestellt.

Beim Erstellen einer Geometry-Realisierung muss [Direct2D](direct2d-portal.md) alle Kurven in der bereitgestellten Geometrie in polygonale Näherungen vereinfachen. Sie müssen einen vereinfachten Toleranzparameter für die Erstellungs Methode angeben – Dies gibt den maximalen Abstand zwischen der true-Kurve der Geometrie und der polygonalen Näherung in geräteunabhängigen Pixeln (Device-Independent Pixels, Dips) an. Je niedriger die von Ihnen bereitgestellte Vereinfachungs Toleranz ist, desto höher ist die Genauigkeit des resultierenden Geometrie-Realisierungs Objekts. Entsprechend ergibt sich durch die Bereitstellung einer höheren Vereinfachungs Toleranz eine niedrigere Geometrie-Realisierung. Beachten Sie, dass das Zeichnen von Geometrie mit höherer Genauigkeit teurer ist als bei niedrigerer Genauigkeit, aber Sie können auch weiter skaliert werden, bevor sichtbare Artefakte eingeführt werden. Hinweise zur Verwendung von Vereinfachungs Toleranzen finden Sie weiter unten unter [Skalieren von Geometrie](#scaling-geometry-realizations) -Real Messungen.

> [!Note]  
> Geometry-Realisierungs Objekte sind einem bestimmten Grafikgerät zugeordnet: Sie sind Geräte abhängige Ressourcen.

 

## <a name="drawing-geometry-realizations"></a>Zeichnen von Geometrie-Neumessungen

Das Zeichnen von Geometrie-Neuzuordnungen ähnelt dem Zeichnen anderer [Direct2D](direct2d-portal.md) primitiver, wie z. b. Bitmaps. Um dies zu tun, müssen Sie die [**drawgeometryrealisation**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1devicecontext1-drawgeometryrealization) -Methode abrufen und ihr das zu zeichende Geometrie-Geometry-Objekt und den zu verwendenden Pinsel übergeben. Wie bei anderen Direct2D Drawing-Methoden müssen Sie **drawgeometryrealisation** zwischen Aufrufen von [**beginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) und [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw)aufrufen.

## <a name="scaling-geometry-realizations"></a>Skalieren von Geometry-Neuerungen

Geometry-neueinrichtungen, wie andere [Direct2D](direct2d-portal.md) -primitive, berücksichtigen den Transformations Satz für den Gerätekontext. Obwohl Übersetzungs-und Drehungs Transformationen keine Auswirkung auf die visuelle Qualität von Geometrie-neueffekten haben, können Skalierungs Transformationen visuelle Artefakte liefern.

Insbesondere kann das Anwenden einer großen ausreichenden Skala auf eine Geometrie-Realisierung die polygonale Näherung der echten Kurven darstellen. Das Bild hier zeigt ein paar elliptischer Geometrie-Neuerungen (Fill und Stroke), die zu weit hochskaliert wurden. Die Kurven vereinfachen die Elemente.

![ein paar elliptischer Geometrie-Neuerungen (Fill und Stroke), die zu weit hochskaliert wurden. die Kurven vereinfachen die Elemente.](images/zoomed-in.png)

Apps, die für die visuelle Qualität sensibel sind, sollten Maßnahmen ergreifen, um sicherzustellen, dass dies nicht geschieht. Wie Sie die Skalierung handhaben, hängt von den Anforderungen Ihrer APP ab. Im folgenden finden Sie einige empfohlene Vorgehensweisen für verschiedene Arten von apps.

### <a name="using-geometry-realizations-in-apps-that-do-not-scale"></a>Verwenden von Geometrie-Neuerungen in apps, die nicht skaliert werden

Wenn Ihre APP keine Skalierung der Geometrie-Neuerungen ausführt, ist es sicher, die Neuerungen nur einmal zu erstellen, indem Sie eine einzige vereinfachte Toleranz verwenden. (Nicht skalierbare Transformationen wirken sich nicht auf die visuelle Qualität von gerenderten Geometrie-Neuerungen aus.) Verwenden Sie die [**computevereinfachingtolerance**](/previous-versions/windows/desktop/legacy/dn280327(v=vs.85)) -Funktion, um die entsprechende Vereinfachungs Toleranz für den dpi-Vorgang zu berechnen:


```C++
    float dpiX, dpiY;
    deviceContext->GetDpi(&dpiX, &dpiY);

    float flatteningTolerance = D2D1::ComputeFlatteningTolerance(
        D2D1::Matrix3x2F::Identity(),   // apply no additional scaling transform
        dpiX,                           // horizontal DPI
        dpiY                            // vertical DPI
        );
```



### <a name="using-geometry-realizations-in-apps-that-scale-by-a-small-amount"></a>Verwenden von Geometrie-Neuerungen in apps, die sich um eine kleine Menge skalieren

Wenn Ihre APP eine Geometry-Realisierung nur mit einem kleinen Betrag (z. b. bis zu 2 x oder 3 x) skalieren kann, ist es möglicherweise sinnvoll, die Geometrie Realisierung einmalig zu erstellen, und zwar mit einer proportional geringeren reduzierungstoleranz als die Standardeinstellung. Dadurch wird eine Erkenntnis mit höherer Genauigkeit erstellt, die vor dem Einfügen skalieringartefakte erheblich hochskaliert werden kann. der Nachteil ist, dass das Zeichnen der höhere Treue-Erkenntnis mehr Arbeit erfordert.

Angenommen, Sie wissen, dass Ihre APP nie eine Geometry-Realisierung um mehr als 2X skaliert. Ihre APP kann die Geometrie-Realisierung mithilfe einer vereinfachten Toleranz erstellen, die die Hälfte des Standardwerts ist, und die Realisierung einfach nach Bedarf skalieren. Verwenden Sie die [**computevereinfachingtolerance**](/previous-versions/windows/desktop/legacy/dn280327(v=vs.85)) -Funktion, um die entsprechende Vereinfachungs Toleranz zu berechnen, indem Sie 2,0 als *maxzoomfactor* -Parameter übergeben:


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



### <a name="using-geometry-realizations-in-apps-that-scale-by-a-large-amount"></a>Verwenden von Geometrie-Neuerungen in apps, die sich um eine große Menge skalieren

Wenn Ihre APP eine Geometry-Realisierung durch große Mengen zentral hoch-oder Herunterskalieren kann (z. b. um Zehnfache oder mehr), ist die Verarbeitung der Skalierung entsprechend komplizierter.

Bei den meisten dieser apps empfiehlt es sich, die Geometrie Realisierung beim horizontalen hochskalieren der Szene mit progressiver geringer Geschwindigkeit zu erstellen, um die visuelle Genauigkeit aufrechtzuerhalten und Artefakte zu vermeiden. Ebenso, wenn die Szene herunterskaliert wird, sollte die APP die Geometry-Neueinstellungen bei progressiv höheren Vereinfachungs Toleranzen neu erstellen, um das nicht sichtbare Debuggen von Details zu vermeiden. Die APP sollte die Geometrie neustellungen nicht jedes Mal neu erstellen, wenn sich die Skalierung ändert, da dadurch der Zweck der Zwischenspeicherung der Mosaikarbeit nicht mehr besteht. Stattdessen sollte die APP die Geometry-Neuerungen seltener neu erstellen, z. b. nach jeder 2X-Vergrößerung oder-Verkleinerung.

Jedes Mal, wenn sich die Skalierung in einer App als Reaktion auf eine Benutzerinteraktion ändert, könnte die APP die neue Skala mit der Skala vergleichen, bei der die Geometrie-neustellungen zuletzt erstellt wurden (z. b. in einem **m \_ lastscale** -Member). Wenn die beiden Werte close sind (in diesem Fall innerhalb eines Faktors von 2), wird keine weitere Aktion durchgeführt. Wenn die beiden Werte jedoch nicht geschlossen werden, werden die Geometrie-Neueinstellungen neu erstellt. Die [**computevereinfachingtolerance**](/previous-versions/windows/desktop/legacy/dn280327(v=vs.85)) -Funktion wird verwendet, um eine vereinfachte Toleranz für die neue Skalierung zu berechnen, und **m \_ lastscale** wird auf die neue Skalierung aktualisiert.

Außerdem erstellt die APP immer mit einer geringeren Toleranz, als normalerweise für die neue Skala verwendet würde, indem der Wert 2 als *maxzoomfactor* -Parameter an [**computevereinfachingtolerance**](/previous-versions/windows/desktop/legacy/dn280327(v=vs.85))übergeben wird. Dadurch können die neuen Geometrie-Neuerungen um einen zusätzlichen Faktor von 2 zentral hochskaliert werden, ohne dass die Skalierung von Artefakten durchlaufen wird.

> [!Note]  
> Der hier beschriebene Ansatz eignet sich möglicherweise nicht für alle apps. Wenn Ihre APP beispielsweise zulässt, dass die Szene sehr schnell von sehr großen Faktoren skaliert wird (wenn Sie z. b. einen "Zoom"-Schieberegler enthält, der in der Spanne von einigen Frames von 100% auf 1 Million% verschoben werden kann), kann dieser Ansatz zu einer übermäßigen Arbeit führen, indem die Geometrie-neustellungen jedes Frame neu erstellt werden. Ein alternativer Ansatz besteht darin, die Geometrie-neueinrichtungen erst neu zu erstellen, nachdem jede Bearbeitung der Szene der Szene abgeschlossen wurde (z. b. Nachdem der Benutzer eine Pinsel Bewegung abgeschlossen hat).

 

## <a name="related-topics"></a>Zugehörige Themen

[Übersicht über Geometrien](direct2d-geometries-overview.md)

[Verbessern der Leistung von Direct2D-apps](improving-direct2d-performance.md)

[Allgemeine Richtlinien zum Rendern komplexer statischer Inhalte](improving-direct2d-performance.md)

[**ID2D1DeviceContext1**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1devicecontext1)

[**ID2D1GeometryRealization**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1geometryrealization)

[**Computevereinfachingtolerance-Funktion**](/previous-versions/windows/desktop/legacy/dn280327(v=vs.85))