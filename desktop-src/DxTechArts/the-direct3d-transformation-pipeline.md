---
title: Die Direct3D-Transformations Pipeline
description: Dieser Artikel bietet eine technische Erläuterung für Direct3D-Anwendungsentwickler, wie die Parameter der Direct3D-Transformations Pipeline durch direkte Bearbeitung von Direct3D Matrizen festgelegt werden.
ms.assetid: 48ae49f0-1162-c292-4bd4-34da5aadd2df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2b97a87293a840ccd9641b1418c2005cf73a855
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "103869324"
---
# <a name="the-direct3d-transformation-pipeline"></a>Die Direct3D-Transformations Pipeline

Dieser Artikel bietet eine technische Erläuterung für Direct3D-Anwendungsentwickler, wie die Parameter der Direct3D-Transformations Pipeline durch direkte Bearbeitung von Direct3D Matrizen festgelegt werden.

-   [Übersicht](#overview)
-   [Transformations Pipeline](#the-transformation-pipeline)
-   [Verwendungs Tipps](#usage-tips)

## <a name="overview"></a>Übersicht

Direct3D verwendet drei Transformationen, um die 3D-Modell Koordinaten in Pixelkoordinaten (Bildschirmraum) zu ändern. Diese Transformationen sind Welt Transformation, Ansichts Transformation und Projektions Transformation.

Mit der Welt Transformation wird gesteuert, wie Modell Koordinaten in globale Koordinaten transformiert werden. Die globale Transformation kann Übersetzungen, Drehungen und Skalierungen enthalten, aber Sie gilt nicht für Leuchten. Weitere Informationen zum Arbeiten mit weltweiten Transformationen finden Sie unter [Welt Transformation](/windows/desktop/direct3d9/world-transform).

View Transform steuert den Übergang von den Weltkoordinaten in den "Kamera Raum", um die Kameraposition weltweit zu bestimmen. Ein Beispiel für das Arbeiten mit Ansichts Transformationen finden Sie unter [View Transform (View Transform](/windows/desktop/direct3d9/view-transform)).

Die Projektions Transformation ändert die Geometrie von Kamerabereich in "Clip Space" und wendet perspektivische Verzerrung an. Der Begriff "Clip Space" bezieht sich darauf, wie die Geometrie während dieser Transformation auf das Ansichts Volume zugeschnitten wird. Ein Beispiel für das Arbeiten mit Projektions Transformationen finden Sie unter [Projektions Transformation](/windows/desktop/direct3d9/projection-transform).

Schließlich wird die Geometrie im Clip Bereich in Pixelkoordinaten (Bildschirmraum) transformiert. Diese Transformation wird durch die viewporteinstellungen gesteuert.

Clipping-und transformierende Scheitel Punkte müssen in einem homogenen Raum stattfinden (einfach Leerstellen, in dem das Koordinatensystem ein viertes Element enthält). das Endergebnis für die meisten Anwendungen muss jedoch nicht homogene dreidimensionale (3D-) Koordinaten sein, die im "Bildschirmbereich" definiert sind. Dies bedeutet, dass sowohl die Eingabe Scheitel Punkte als auch das clippingvolume in homogenen Raum übersetzt werden müssen, um das Clipping auszuführen, und dann wieder in nicht homogenen Bereich übersetzt werden, um angezeigt zu werden.

Die drei Transformationen "Direct3D Transformationen-World", "View" und "Projection" werden durch Direct3D Matrices definiert. Eine Direct3D-Matrix ist eine homogene 4 x 4-Matrix, die durch eine [**D3DMATRIX**](/windows/desktop/direct3d9/d3dmatrix) -Struktur definiert ist. Obwohl Direct3D Matrizen keine Standardobjekte sind, werden Sie nicht durch eine COM-Schnittstelle dargestellt. Sie können Sie genauso wie jedes andere Direct3D-Objekt erstellen und festlegen. Weitere Informationen zu Direct3D Matrizen finden Sie unter [Transformationen](/windows/desktop/direct3d9/transforms).

## <a name="the-transformation-pipeline"></a>Transformations Pipeline

Wenn ein Scheitelpunkt in der Modell Koordinate von pm = (XM, YM, ZM, 1) angegeben wird, werden die in der folgenden Abbildung gezeigten Transformationen auf die Compute-Bildschirm Koordinaten PS = (XS, ys, ZS, WS) angewendet.

![Transformation für Modellraum zu Bildschirmraum](images/d3dxfrm61.gif)

Im folgenden finden Sie Beschreibungen der Stufen, die in der obigen Abbildung dargestellt werden:

1.  World Matrix mworld wandelt Scheitel Punkte vom Modellraum in den Raum um. Diese Matrix wird durch Folgendes festgelegt:

    ``` syntax
        d3dDevice->SetTransform (D3DTRANSFORMSTATE_WORLD, matrix address) 
    ```

    Die Direct3D-Implementierung geht davon aus, dass die letzte Spalte dieser Matrix (0,0) ist (0, 0, 0, 1). Wenn der Benutzer eine Matrix mit einer anderen letzten Spalte angibt, wird kein Fehler zurückgegeben, aber die Beleuchtung und der Nebel sind falsch.

2.  Anzeigen von Matrix-MVIEW Transformationen Scheitel Punkte aus dem Raum in der Kamera. Diese Matrix wird durch Folgendes festgelegt:

    ``` syntax
        d3dDevice->SetTransform (D3DTRANSFORMSTATE_VIEW, matrix address) 
    ```

    Die Direct3D-Implementierung geht davon aus, dass die letzte Spalte dieser Matrix (0,0) ist (0, 0, 0, 1). Es wird kein Fehler zurückgegeben, wenn der Benutzer eine Matrix mit unterschiedlichen letzten Spalten angibt, aber die Beleuchtung und der Nebel sind falsch.

3.  Projektions Matrix mproj wandelt Scheitel Punkte vom Kamerabereich in den Projektions Bereich um. Diese Matrix wird durch Folgendes festgelegt:

    ``` syntax
        d3dDevice->SetTransform (D3DTRANSFORMSTATE_PROJECTION, matrix address) 
    ```

    Die letzte Spalte der Projektions Matrix sollte (0, 0, 1, 0) oder (0, 0, a, 0) für korrekte Nebel-und Beleuchtungseffekte lauten. das Formular (0,0) ist bevorzugt.

    Das clippingvolume für alle Punkte XP = (XP, YP, ZP, WP) im Projektions Bereich wird wie folgt definiert:

    ``` syntax
        -Wp < Xp <= Wp 
        -Wp < Yp <= Wp 
        0 < Zp <= Wp 
    ```

    Alle Punkte, die diese Gleichungen nicht erfüllen, werden abgeschnitten.

    Wenn ein Ansichts Volume wie folgt definiert ist:

    -   SW-Bildschirmfenster Breite im Kamerabereich in der Nähe der Clipping-Ebene
    -   Höhe des SH-Screen-Fensters im Kamerabereich in der Nähe der Clipping-Ebene
    -   HLS-Entfernung zur Near Clipping-Ebene entlang Z-Achsen im Kamerabereich
    -   ZF-Entfernung zur weit entfernten Clipping-Ebene entlang Z-Achsen im Kamerabereich

    Anschließend könnte eine perspektivische Projektions Matrix wie folgt geschrieben werden:

    ![Zeigt eine perspektivische Projektions Matrix an.](images/d3dxfrm62.gif)

    Dabei sind mij Mitglieder von mproj.

    Für die orthogonale Projektion haben wir Folgendes:

    ![orthogonale Projektion](images/d3dxfrm63.gif)

    Direct3D geht davon aus, dass die Perspektiven Projektions Matrix folgendes Format aufweist:

    ![Perspektiven Projektions Matrix](images/d3dxfrm64.gif)

    Wenn die perspektivische Projektions Matrix nicht über dieses Formular verfügt, werden einige Artefakte angezeigt. Beispielsweise kann der Tabellen Nebel nicht verwendet werden.

4.  Direct3D ermöglicht dem Benutzer, das Clip Volume wie folgt zu ändern:

    ![Ändern des clippvolumes](images/d3dxfrm65.gif)

    Dies kann wie folgt umgeschrieben werden:

    ![umgeschriebene Clip Volume ändern](images/d3dxfrm66.gif)

    Dabei gilt:

    ``` syntax
        Cx, Cy - dvClipX, dvClipY from D3DVIEWPORT9  
        Cw, Ch - dvClipWidth, dvClipHeight from D3DVIEWPORT9  
        Zmin, Zmax - dvMinZ, dvMaxZ from D3DVIEWPORT9  
    ```

    Diese Transformation kann eine größere Genauigkeit bieten und entspricht der Skalierung und Verschiebung des clippingvolumes.

    Die entsprechende MCLIP-Matrix lautet:

    ![MCLIP-Matrix](images/d3dxfrm67.gif)

    Ein Scheitelpunkt wird transformiert durch:

    ``` syntax
        dvClipWidth = 2   
        dvClipHeight = 2   
        dvClipX = -1   
        dvClipY = 1   
        dvMinZ = 0   
        dvMaxZ = 1   
    ```

    Wenn Sie das Clip Volume nicht skalieren möchten, können Sie Viewport-Parameter auf Standardwerte festlegen:

    ``` syntax
        (Xc, Yc, Zc, Wc) = (Xp, Yp, Zp, Wp) * Mclip   
    ```

5.  Die clippingphase ist optional, wenn der Benutzer das D3DDP \_ DoNotClip-Flag in einem drawprimitiven-Befehl angibt. In diesem Fall können alle Matrizen (einschließlich MVS) kombiniert werden.
6.  Die viewportskalierungsmatrix-MVS skaliert die Koordinaten so, dass Sie innerhalb des viewportfensters liegen, und kippt die Y-Achse von oben nach unten:

    ![Viewport-Skalierungs Matrix-MVS](images/d3dxfrm68.gif)

    Dabei gilt:

    ``` syntax
        dwX, dwY - viewport offsets in pixels from D3DVIEWPORT9 
        dwWidth, dwHeight - viewport width and height in pixels from D3DVIEWPORT9    
    ```

7.  Zum Schluss werden Bildschirm Koordinaten berechnet und an den Rasterizer übermittelt:

    ![Bildschirm Koordinaten berechnet und an den Raster übermittelt](images/d3dxfrm69.gif)

## <a name="usage-tips"></a>Verwendungs Tipps

Im folgenden finden Sie einige Tipps zur Verwendung der Direct3D-Transformations Pipeline:

-   Die letzte Spalte der Welt-und Ansichts Matrizen sollte (0, 0, 0, 1) sein, oder die Beleuchtung ist falsch.
-   Legen Sie die Viewport-Parameter fest, um eine MCLIP-Identitätsmatrix zu erstellen, es sei denn, Sie wissen genau, wofür Sie benötigt wird.

    ``` syntax
        dvClipWidth = 2 
        dvClipHeight = 2
        dvClipX = -1
        dvClipY = 1
        dvMinZ = 0 
        dvMaxZ = 1
    ```

 

 