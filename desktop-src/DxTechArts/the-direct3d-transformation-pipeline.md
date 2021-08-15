---
title: Die Direct3D-Transformationspipeline
description: Dieser Artikel enthält eine technische Erläuterung für Direct3D-Anwendungsentwickler zum Festlegen der Parameter der Direct3D-Transformationspipeline durch die direkte Bearbeitung von Direct3D-Matrizen.
ms.assetid: 48ae49f0-1162-c292-4bd4-34da5aadd2df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6377e3b17cfb4ceb6eda1f4cf59a93c12fd3e6b2f7e43f29f622ed6ee12c271
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118152334"
---
# <a name="the-direct3d-transformation-pipeline"></a>Die Direct3D-Transformationspipeline

Dieser Artikel enthält eine technische Erläuterung für Direct3D-Anwendungsentwickler zum Festlegen der Parameter der Direct3D-Transformationspipeline durch die direkte Bearbeitung von Direct3D-Matrizen.

-   [Übersicht](#overview)
-   [Die Transformationspipeline](#the-transformation-pipeline)
-   [Nutzungs-Tipps](#usage-tips)

## <a name="overview"></a>Übersicht

Direct3D verwendet drei Transformationen, um Ihre 3D-Modellkoordinaten in Pixelkoordinaten (Bildschirmraum) zu ändern. Diese Transformationen sind Welttransformation, Ansichtstransformation und Projektionstransformation.

World Transform steuert, wie Modellkoordinaten in Weltkoordinaten transformiert werden. Die Welttransformation kann Übersetzungen, Drehungen und Skalierungen umfassen, gilt jedoch nicht für Licht. Weitere Informationen zum Arbeiten mit Welttransformationen finden Sie unter [World Transform](/windows/desktop/direct3d9/world-transform).

Die Ansichtstransformation steuert den Übergang von Weltkoordinaten in "Kameraraum", um die Kameraposition in der Welt zu bestimmen. Ein Beispiel für das Arbeiten mit Ansichtstransformationen finden Sie unter [View Transform](/windows/desktop/direct3d9/view-transform).

Die Projektionstransformation ändert die Geometrie aus dem Kameraraum in "Clip Space" und wendet perspektivische Verzerrung an. Der Begriff "Clip space" bezieht sich darauf, wie die Geometrie während dieser Transformation auf das Ansichtsvolumen abgeschnitten wird. Ein Beispiel für die Arbeit mit Projektionstransformationen finden Sie unter [Projektionstransformation.](/windows/desktop/direct3d9/projection-transform)

Schließlich wird die Geometrie im Clipspace in Pixelkoordinaten (Bildschirmraum) transformiert. Diese Transformation wird durch die Viewporteinstellungen gesteuert.

Das Ausschneiden und Transformieren von Scheitelpunkten muss im homogenen Raum erfolgen (einfach ausgedrückt: Im Raum, in dem das Koordinatensystem ein viertes Element enthält), aber das Endergebnis für die meisten Anwendungen müssen nicht homogene dreidimensionale Koordinaten (3D) sein, die im Bildschirmbereich definiert sind. Dies bedeutet, dass sowohl die Eingabevertices als auch das Clippingvolume in einen homogenen Raum übersetzt werden müssen, um den Clipping auszuführen, und dann wieder in einen nicht homogenen Raum übersetzt werden müssen, um angezeigt zu werden.

Die drei Direct3D-Transformationen –Welt-, Ansichts- und Projektionstransformationen – werden durch Direct3D-Matrizen definiert. Eine Direct3D-Matrix ist eine homogene 4x4-Matrix, die durch eine [**D3DMATRIX-Struktur**](/windows/desktop/direct3d9/d3dmatrix) definiert wird. Obwohl Direct3D-Matrizen keine Standardobjekte sind, die nicht durch eine COM-Schnittstelle dargestellt werden, können Sie sie wie jedes andere Direct3D-Objekt erstellen und festlegen. Weitere Informationen zu Direct3D-Matrizen finden Sie unter [Transformationen.](/windows/desktop/direct3d9/transforms)

## <a name="the-transformation-pipeline"></a>Die Transformationspipeline

Wenn ein Scheitelpunkt in der Modellkoordinate von Pm = (Xm, Ym, Zm, 1) angegeben wird, werden die in der folgenden Abbildung gezeigten Transformationen auf die Computebildschirmkoordinaten Ps = (Xs, Ys, Zs, Ws) angewendet.

![Transformation von Modellraum zu Bildschirmbereich](images/d3dxfrm61.gif)

Hier finden Sie Beschreibungen der Phasen, die in der vorherigen Abbildung dargestellt werden:

1.  Die Weltmatrix Mworld transformiert Scheitelpunkte aus dem Modellraum in den Weltraum. Diese Matrix wird wie folgt festgelegt:

    ``` syntax
        d3dDevice->SetTransform (D3DTRANSFORMSTATE_WORLD, matrix address) 
    ```

    Bei der Direct3D-Implementierung wird davon ausgegangen, dass die letzte Spalte dieser Matrix (0, 0, 0, 1) ist. Es wird kein Fehler zurückgegeben, wenn der Benutzer eine Matrix mit einer anderen letzten Spalte angibt, die Beleuchtung und die Beleuchtung jedoch falsch sind.

2.  Die MView-Ansicht der Ansichtsmatrix transformiert Scheitelpunkte aus dem Weltraum in den Kameraraum. Diese Matrix wird wie folgt festgelegt:

    ``` syntax
        d3dDevice->SetTransform (D3DTRANSFORMSTATE_VIEW, matrix address) 
    ```

    Bei der Direct3D-Implementierung wird davon ausgegangen, dass die letzte Spalte dieser Matrix (0, 0, 0, 1) ist. Es wird kein Fehler zurückgegeben, wenn der Benutzer eine Matrix mit einer anderen letzten Spalte angibt, die Beleuchtung und die Beleuchtung jedoch falsch sind.

3.  Die Projektionsmatrix Mproj transformiert Scheitelpunkte aus dem Kameraraum in den Projektionsbereich. Diese Matrix wird wie folgt festgelegt:

    ``` syntax
        d3dDevice->SetTransform (D3DTRANSFORMSTATE_PROJECTION, matrix address) 
    ```

    Die letzte Spalte der Projektionsmatrix sollte (0, 0, 1, 0) oder (0, 0, a, 0) sein, um korrekte Licht- und Lichteffekte zu erzielen. (0, 0, 1, 0) Form wird bevorzugt.

    Clipping volume for all points Xp = (Xp, Yp, Zp, Wp) in the projection space is defined as:

    ``` syntax
        -Wp < Xp <= Wp 
        -Wp < Yp <= Wp 
        0 < Zp <= Wp 
    ```

    Alle Punkte, die diese Gleichungen nicht erfüllen, werden abgeschnitten.

    Wenn ein Ansichtsvolume wie folgt definiert ist:

    -   Breite des Sw-Bildschirmfensters im Kameraraum in der Nähe der Clippingebene
    -   Sh-Screen-Fensterhöhe im Kameraraum in der Nähe der Clippingebene
    -   Zn-Entfernung zur mittleren Clippingebene entlang der Z-Achsen im Kameraraum
    -   Abstand zur weit entfernten Clippingebene entlang der Z-Achsen im Kameraraum

    dann könnte eine perspektivische Projektionsmatrix wie folgt geschrieben werden:

    ![Zeigt eine perspektivische Projektionsmatrix an.](images/d3dxfrm62.gif)

    , wobei Mij Mitglieder von Mproj sind.

    Für die orthogonale Projektion haben wir Folgendes:

    ![Orthogonale Projektion](images/d3dxfrm63.gif)

    Direct3D geht davon aus, dass die perspektivische Projektionsmatrix die folgende Form hat:

    ![Perspektivische Projektionsmatrix](images/d3dxfrm64.gif)

    Wenn die perspektivische Projektionsmatrix nicht über diese Form verfügt, gibt es einige Artefakte. Tabellen werden beispielsweise nicht funktionieren.

4.  Direct3D ermöglicht es dem Benutzer, das Clipvolume wie folgt zu ändern:

    ![Ändern des Clipvolumes](images/d3dxfrm65.gif)

    Dies kann wie hier beschrieben umgeschrieben werden:

    ![Ändern des neu geschriebenen Clipvolumes](images/d3dxfrm66.gif)

    Dabei gilt:

    ``` syntax
        Cx, Cy - dvClipX, dvClipY from D3DVIEWPORT9  
        Cw, Ch - dvClipWidth, dvClipHeight from D3DVIEWPORT9  
        Zmin, Zmax - dvMinZ, dvMaxZ from D3DVIEWPORT9  
    ```

    Diese Transformation kann eine höhere Genauigkeit bieten und entspricht der Skalierung und Verschiebung des Clippingvolumes.

    Die entsprechende Mclipmatrix lautet:

    ![mclip matrix](images/d3dxfrm67.gif)

    Ein Scheitelpunkt wird wie folgt transformiert:

    ``` syntax
        dvClipWidth = 2   
        dvClipHeight = 2   
        dvClipX = -1   
        dvClipY = 1   
        dvMinZ = 0   
        dvMaxZ = 1   
    ```

    Wenn Sie das Clipvolume nicht skalieren möchten, können Sie Viewportparameter auf Standardwerte festlegen:

    ``` syntax
        (Xc, Yc, Zc, Wc) = (Xp, Yp, Zp, Wp) * Mclip   
    ```

5.  Die Clippingphase ist optional, wenn der Benutzer das D3DDP \_ DONOTCLIP-Flag in einem DrawPrimitive-Aufruf angibt. In diesem Fall können alle Matrizen (einschließlich Mvs) kombiniert werden.
6.  Die Viewport-Skalierungsmatrix Mvs skaliert Koordinaten so, dass sie sich innerhalb des Viewportfensters befindet, und dreht die Y-Achse von oben nach unten:

    ![Viewport-Skalierungsmatrix mvs](images/d3dxfrm68.gif)

    Dabei gilt:

    ``` syntax
        dwX, dwY - viewport offsets in pixels from D3DVIEWPORT9 
        dwWidth, dwHeight - viewport width and height in pixels from D3DVIEWPORT9    
    ```

7.  Schließlich werden Bildschirmkoordinaten berechnet und an den Rasterizer übergeben:

    ![Berechnete und an den Rasterizer übergebene Bildschirmkoordinaten](images/d3dxfrm69.gif)

## <a name="usage-tips"></a>Nutzungs-Tipps

Im Folgenden finden Sie einige Tipps zur Verwendung der Direct3D-Transformationspipeline:

-   Die letzte Spalte der Welt- und Ansichtsmatrizen sollte (0, 0, 0, 1) sein, andernfalls ist die Beleuchtung falsch.
-   Legen Sie die Viewportparameter fest, um eine Mclip-Identitätsmatrix zu erstellen, es sei denn, Sie wissen genau, wofür sie benötigt wird.

    ``` syntax
        dvClipWidth = 2 
        dvClipHeight = 2
        dvClipX = -1
        dvClipY = 1
        dvMinZ = 0 
        dvMaxZ = 1
    ```

 

 