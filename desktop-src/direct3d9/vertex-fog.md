---
description: Wenn das System vertexfogging ausführt, wendet es bei jedem Scheitelpunkt in einem Polygon eine Nebel Berechnung an und interpoliert die Ergebnisse während der rasterisierung auf der Vorderseite des Polygons.
ms.assetid: 76989eb3-cd95-4dfc-ba0f-7563860b531c
title: Scheitelpunkt Nebel (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35cd880bda7ebffd36bd95bec5f8565e104eaa15
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123337"
---
# <a name="vertex-fog-direct3d-9"></a>Scheitelpunkt Nebel (Direct3D 9)

Wenn das System vertexfogging ausführt, wendet es bei jedem Scheitelpunkt in einem Polygon eine Nebel Berechnung an und interpoliert die Ergebnisse während der rasterisierung auf der Vorderseite des Polygons. Vertex-Nebeleffekte werden von der Direct3D-Beleuchtungs-und-Transformations-Engine berechnet. Weitere Informationen finden Sie unter " [Fog Parameters" (Direct3D 9)](fog-parameters.md).

Wenn Ihre Anwendung Direct3D nicht für die Transformation und Beleuchtung verwendet, muss die Anwendung Nebel Berechnungen ausführen. Platzieren Sie in diesem Fall den in der Alpha-Komponente berechneten Nebel Faktor der Glanz Farbe für jeden Scheitelpunkt. Sie können beliebige Formeln verwenden, die Sie verwenden möchten: Bereichs basiert, Volumetric oder anderweitig. Direct3D verwendet den angegebenen Nebel Faktor, um das Gesicht jedes Polygons zu interpolieren. Anwendungen, die ihre eigene Transformation und Beleuchtung ausführen, müssen auch eigene Scheitelpunkt Berechnungen ausführen. Daher muss eine solche Anwendung nur eine Nebel Mischung aktivieren und die Nebelfarbe durch die zugehörigen gerengerzustände festlegen, wie unter [Nebel Mischung (Direct3D 9)](fog-blending.md) und [Nebelfarbe (Direct3D 9)](fog-color.md)beschrieben.

> [!Note]  
> Wenn Sie einen Vertex-Shader verwenden, müssen Sie Scheitelpunkt Nebel verwenden. Dies wird erreicht, indem der Vertex-Shader verwendet wird, um die Nebel Intensität pro Scheitelpunkt in das ofog-Register zu schreiben. Nachdem der Pixelshader abgeschlossen ist, werden die onebel-Daten für die lineare interinterpolate mit der Nebelfarbe verwendet. Diese Intensität ist in einem Pixelshader nicht verfügbar.

 

## <a name="range-based-fog"></a>Range-Based Nebel

> [!Note]  
> Direct3D verwendet Bereichs basierte Nebel Berechnungen nur bei Verwendung von Scheitelpunkt Nebel mit der Direct3D-Transformation und der Beleuchtungs-Engine. Der Grund hierfür ist, dass Pixel Nebel im Gerätetreiber implementiert ist und derzeit keine Hardware zur Unterstützung von pro Pixel Bereichs basiertem Nebel vorhanden ist. Wenn Ihre Anwendung ihre eigene Transformation und Beleuchtung durchführt, muss Sie eigene, Bereichs basierte oder andere Nebel Berechnungen durchführen.

 

Manchmal kann die Verwendung von Nebel grafische Artefakte darstellen, die bewirken, dass Objekte in nicht intuitiver Weise mit der Nebelfarbe gemischt werden. Stellen Sie sich z. b. eine Szene vor, in der zwei sichtbare Objekte vorhanden sind: eine Distanz genug, um von einem Nebel betroffen zu sein, und die andere nahe genug, um nicht betroffen zu sein. Wenn sich der Anzeigebereich an Ort und Stelle dreht, können sich die offensichtlichen Nebeleffekte ändern, auch wenn die Objekte stationär sind. Das folgende Diagramm zeigt eine Top-down-Ansicht einer solchen Situation.

![Diagramm mit zwei Standpunkten und deren Auswirkung auf den Nebel für zwei Objekte](images/artifog.png)

Bereichs basierter Nebel ist eine weitere, präzisere Methode zum Ermitteln der Nebeleffekte. Im Bereichs basierten Nebel verwendet Direct3D die tatsächliche Entfernung von der Sicht Ansicht zu einem Scheitelpunkt für seine Nebel Berechnungen. Direct3D vergrößert die Auswirkung von Nebel, da der Abstand zwischen den beiden Punkten zunimmt, und nicht die Tiefe des Scheitel Punkts in der Szene. Dadurch werden Rotelle Artefakte vermieden.

Wenn das aktuelle Gerät Bereichs basierten Nebel unterstützt, wird der D3DPRASTERCAPS \_ fogrange-Wert im RasterCaps-Member von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) festgelegt, wenn Sie die [**IDirect3DDevice9:: GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) -Methode aufrufen. Um Bereichs basierten Nebel zu aktivieren, legen Sie den D3DRS \_ RANGEFOGENABLE-Rendering-Zustand auf **true** fest.

Bereichs basierter Nebel wird während der Transformation und Beleuchtung durch Direct3D berechnet. Anwendungen, die nicht die Direct3D-Transformation und das Beleuchtungs Modul verwenden, müssen auch eigene Scheitelpunkt Berechnungen ausführen. Geben Sie in diesem Fall den Bereichs basierten Nebel Faktor in der Alpha Komponente der Glanz Komponente für jeden Scheitelpunkt an.

## <a name="using-vertex-fog"></a>Verwenden von Scheitelpunkt Nebel

Führen Sie die folgenden Schritte aus, um den Scheitelpunkt in der Anwendung zu aktivieren.

1.  Aktivieren Sie die Schnebel Mischung \_ , indem Sie D3DRS fogenable auf **true** festlegen.
2.  Legen Sie die Nebelfarbe im D3DRS \_ fogcolor-Rendering-Zustand fest.
3.  Wählen Sie die gewünschte Nebel Formel aus, indem Sie den \_ renderzustand D3DRS fogvertexmode auf einen Member des [**D3DFOGMODE**](./d3dfogmode.md) -enumerierten Typs festlegen.
4.  Legen Sie die für die ausgewählte Nebel Formel in den Rendering-Zuständen gewünschten Nebel Parameter fest.

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



Einige Nebel Parameter sind als Gleit Komma Werte erforderlich, auch wenn die [**IDirect3DDevice9:: setrenderstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) -Methode nur DWORD-Werte im zweiten Parameter akzeptiert. In diesem Beispiel werden die Gleit Komma Werte für diese Methoden ohne Daten Übersetzung erfolgreich bereitstellt, indem die Adressen der Gleit Komma Variablen als DWORD-Zeiger umgewandelt und dann dereferenzierend ausgeführt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Nebel Typen](fog-types.md)
</dt> </dl>

 

 
