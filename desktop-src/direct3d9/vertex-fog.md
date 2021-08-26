---
description: Wenn das System Scheitelpunkt-Schwischen ausführt, wendet es Aufschlussberechnungen an jedem Scheitelpunkt in einem Polygon an und interpoliert dann die Ergebnisse während der Rasterung über das Gesicht des Polygons.
ms.assetid: 76989eb3-cd95-4dfc-ba0f-7563860b531c
title: Scheitelpunkt(Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76196ba0489ac58529bcb5c0500a269c8ee27b87040ec96f64ef228377dc8abd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068975"
---
# <a name="vertex-fog-direct3d-9"></a>Scheitelpunkt(Direct3D 9)

Wenn das System Scheitelpunkt-Schwischen ausführt, wendet es Aufschlussberechnungen an jedem Scheitelpunkt in einem Polygon an und interpoliert dann die Ergebnisse während der Rasterung über das Gesicht des Polygons. Scheitelpunkteffekte werden von der Direct3D-Beleuchtungs- und Transformations-Engine berechnet. Weitere Informationen finden Sie unter [Parameters (Direct3D 9)](fog-parameters.md).

Wenn Ihre Anwendung Direct3D nicht für Die Transformation und Beleuchtung verwendet, muss die Anwendung Berechnungsberechnungen durchführen. Platzieren Sie in diesem Fall den 10-Faktor, der in der Alphakomponente der Specularfarbe für jeden Scheitelpunkt berechnet wird. Sie können die formeln verwenden, die Sie wünschen – bereichsbasierte, volumetrisch oder anderweitige Formeln. Direct3D verwendet den angegebenen Fügefaktor, um die Gesichtserkennung jedes Polygons zu interpolieren. Anwendungen, die ihre eigene Transformation und Beleuchtung durchführen, müssen auch eigene Scheitelpunktberechnungen durchführen. Daher muss eine solche Anwendung nur blending aktivieren und die Farbe über die zugeordneten Renderzustände festlegen, wie in [Blending (Direct3D 9)](fog-blending.md) und [Color Color (Direct3D 9)](fog-color.md)beschrieben.

> [!Note]  
> Wenn Sie einen Scheitelpunkt-Shader verwenden, müssen Sie Scheitelpunkt-Scheitelpunkt verwenden. Dies wird erreicht, indem der Vertex-Shader verwendet wird, um die Intensität pro Scheitelpunkt in das oFog-Register zu schreiben. Nachdem der Pixel-Shader abgeschlossen ist, werden die oFog-Daten verwendet, um linear mit der Farbe des Farbtons zu interpolieren. Diese Intensität ist in einem Pixel-Shader nicht verfügbar.

 

## <a name="range-based-fog"></a>Range-Based Soll

> [!Note]  
> Direct3D verwendet bereichsbasierte Berechnungsberechnungen nur, wenn Scheitelpunkts mit der Direct3D-Transformation und dem Beleuchtungsmodul verwendet werden. Dies liegt daran, dass Pixelpixel im Gerätetreiber implementiert sind und derzeit keine Hardware vorhanden ist, die bereichsbasierte Zählpixel unterstützt. Wenn Ihre Anwendung eine eigene Transformation und Beleuchtung ausführt, muss sie eigene Berechnungsberechnungen durchführen, die bereichsbasierte oder andere Berechnungen durchführen.

 

Manchmal kann die Verwendung von Ziehsteinen zu grafischen Artefakten führen, die dazu führen, dass Objekte auf nicht inintuitive Weise mit der Farbfarbe der Farbe der Farbe kombiniert werden. Stellen Sie sich z. B. eine Szene vor, in der zwei sichtbare Objekte vorhanden sind: eins, das weit genug entfernt ist, um von Derbe betroffen zu sein, und das andere nahe genug, um nicht betroffen zu sein. Wenn sich der Anzeigebereich an Ort und Stelle dreht, können sich die offensichtlichen Effekten ändern, auch wenn die Objekte fest sind. Das folgende Diagramm zeigt eine top-down-Ansicht einer solchen Situation.

![Diagramm von zwei Standpunkten und deren Auswirkung auf zwei Objekte](images/artifog.png)

Die bereichsbasierte Spanne ist eine weitere, genauere Möglichkeit, die Effekten des Effekts zu bestimmen. In bereichsbasierten Abständen verwendet Direct3D den tatsächlichen Abstand vom Blickpunkt zu einem Scheitelpunkt für seine Berechnung der Abstände. Direct3D erhöht den Effekt von 3D, wenn der Abstand zwischen den beiden Punkten zunimmt, anstatt die Tiefe des Scheitelpunkts innerhalb der Szene zu erhöhen, wodurch Drehartefakte vermieden werden.

Wenn das aktuelle Gerät bereichsbasiertes Kapseln unterstützt, wird beim Aufrufen der \_ [**IDirect3DDevice9::GetDeviceCaps-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) der D3DPRASTERCAPS-WERT DESRANGERANGE-Werts im RasterCaps-Member von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) festgelegt. Legen Sie den D3DRS RANGEFOGENABLE-Renderzustand auf TRUE fest, um bereichsbasiertes \_ Generiert zu **aktivieren.**

Bereichsbasiertes Computing wird von Direct3D während der Transformation und Beleuchtung berechnet. Anwendungen, die nicht die Direct3D-Transformation und das Beleuchtungsmodul verwenden, müssen auch eigene Scheitelpunktberechnungen durchführen. Geben Sie in diesem Fall den bereichsbasierten Faktor für die Alphakomponente der Specularkomponente für jeden Scheitelpunkt an.

## <a name="using-vertex-fog"></a>Verwenden von Scheitelpunkt

Verwenden Sie die folgenden Schritte, um Scheitelpunktverschluss in Ihrer Anwendung zu aktivieren.

1.  Aktivieren Sie blending, indem Sie D3DRS \_ LESBAR AUF **TRUE festlegen.**
2.  Legen Sie die Farbe der Farbe im \_ D3DRS-RENDERCOLOR-Renderzustand fest.
3.  Wählen Sie die gewünschte Formel aus, indem Sie den D3DRS-RENDERRVERTEXMODE-Renderzustand auf einen Member des \_ [**aufzählten D3DFOGMODE-Typs**](./d3dfogmode.md) festlegen.
4.  Legen Sie die Parameter für die ausgewählte Formel in den Renderzuständen wie gewünscht fest.

Das folgende in C++ geschriebene Beispiel zeigt, wie diese Schritte im Code aussehen können.


```
// For brevity, error values in this example are not checked 
//   after each call. A real-world application should check 
//   these values appropriately.
//
// For the purposes of this example, g_pDevice is a valid
//   pointer to an IDirect3DDevice9 interface.
void SetupVertexFog(DWORD Color, DWORD Mode, BOOL UseRange, FLOAT Density)
{
    float Start = 0.5f,    // Linear fog distances
          End   = 0.8f;
 
    // Enable fog blending.
    g_pDevice->SetRenderState(D3DRS_FOGENABLE, TRUE);
 
    // Set the fog color.
    g_pDevice->SetRenderState(D3DRS_FOGCOLOR, Color);
    
    // Set fog parameters.
    if(D3DFOG_LINEAR == Mode)
    {
        g_pDevice->SetRenderState(D3DRS_FOGVERTEXMODE, Mode);
        g_pDevice->SetRenderState(D3DRS_FOGSTART, *(DWORD *)(&Start));
        g_pDevice->SetRenderState(D3DRS_FOGEND,   *(DWORD *)(&End));
    }
    else
    {
        g_pDevice->SetRenderState(D3DRS_FOGVERTEXMODE, Mode);
        g_pDevice->SetRenderState(D3DRS_FOGDENSITY, *(DWORD *)(&Density));
    }

    // Enable range-based fog if desired (only supported for
    //   vertex fog). For this example, it is assumed that UseRange
    //   is set to a nonzero value only if the driver exposes the 
    //   D3DPRASTERCAPS_FOGRANGE capability.
    // Note: This is slightly more performance intensive
    //   than non-range-based fog.
    if(UseRange)
        g_pDevice->SetRenderState(D3DRS_RANGEFOGENABLE, TRUE);
}
```



Einige Parameter sind als Gleitkommawerte erforderlich, obwohl die [**IDirect3DDevice9::SetRenderState-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) nur DWORD-Werte im zweiten Parameter akzeptiert. Dieses Beispiel stellt diesen Methoden die Gleitkommawerte ohne Datenübersetzung erfolgreich zur Auswahl, indem die Adressen der Gleitkommavariablen in DWORD-Zeiger umgeformt und anschließend deferiert werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Typen von Typen](fog-types.md)
</dt> </dl>

 

 
