---
description: Eine Dreiecksliste ist eine Liste isolierter Dreiecke. Sie können sich nahe beieinander oder nicht nähern. Eine Dreiecksliste muss mindestens drei Scheitelpunkte enthalten, und die Gesamtzahl der Scheitelpunkte muss durch drei teilbar sein.
ms.assetid: e5c3470f-361c-458a-a42a-3549c51d8794
title: Dreieckslisten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d0f9df4d9a0a6d883abd2ccf6b4f3e86c03bb54bcc404901b3c3fa6d10ede03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118797437"
---
# <a name="triangle-lists"></a>Dreieckslisten

Eine Dreiecksliste ist eine Liste isolierter Dreiecke. Sie können sich nahe beieinander oder nicht nähern. Eine Dreiecksliste muss mindestens drei Scheitelpunkte enthalten, und die Gesamtzahl der Scheitelpunkte muss durch drei teilbar sein.

Verwenden Sie Dreieckslisten, um ein Objekt zu erstellen, das aus unzusammenhängenden Teilen besteht. Eine Möglichkeit zum Erstellen einer Force-Field-Wall in einem 3D-Spiel besteht beispielsweise darin, eine große Liste kleiner, nicht verbundener Dreiecke anzugeben. Wenden Sie dann ein Material und eine Textur an, die scheinbar Licht auf die Dreiecksliste ausgibt. Jedes Dreieck in der Wand scheint zu leuchten. Die Szene hinter der Wand wird durch die Lücken zwischen den Dreiecken teilweise sichtbar, wie ein Spieler beim Betrachten eines Kraftfelds erwarten könnte.

Dreieckslisten eignen sich auch zum Erstellen von Primitiven, die spitze Kanten aufweisen und mit Gouraud-Schattierung schattiert sind. Siehe [Face and Vertex Normal Vectors (Direct3D 9) (Normale Vektoren für Gesicht und Scheitelpunkt (Direct3D 9)).](face-and-vertex-normal-vectors.md)

Die folgende Abbildung zeigt eine gerenderte Dreiecksliste.

![Abbildung einer gerenderten Dreiecksliste](images/trilist.png)

Der folgende Code zeigt, wie Scheitelpunkte für diese Dreiecksliste erstellt werden.


```
struct CUSTOMVERTEX
{
    float x,y,z;
};

CUSTOMVERTEX Vertices[] = 
{
    {-5.0, -5.0, 0.0},
    { 0.0,  5.0, 0.0},
    { 5.0, -5.0, 0.0},
    {10.0,  5.0, 0.0},
    {15.0, -5.0, 0.0},
    {20.0,  5.0, 0.0}

};
```



Das folgende Codebeispiel zeigt, wie diese Dreiecksliste in Direct3D 9 mithilfe von [**IDirect3DDevice9::D rawPrimitive gerendert wird.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, 2 );
```



Sie können auch Dreiecksstreifen verwenden, um Dreiecke zu rendern, die nicht miteinander verbunden sind. Geben Sie hierzu ein degenerates Dreieck (d. amp;n.b. ein Dreieck mit einer Größe von 0 ) in der Liste an. Dadurch wird eine Linie zwischen den beiden Dreiecken erstellt, die während des Renderings nicht angezeigt wird. Um beispielsweise nur das erste und letzte Dreieck aus dem vorherigen Beispiel zu rendern, initialisieren Sie den Scheitelpunktpuffer mit den folgenden Scheitelpunkten:


```
CUSTOMVERTEX Vertices[] =
{
    {-5.0, -5.0, 0.0},
    { 0.0,  5.0, 0.0},
    { 5.0, -5.0, 0.0},
    { 5.0, -5.0, 0.0}, // degenerate triangle
    {10.0,  5.0, 0.0}, // degenerate triangle
    {10.0,  5.0, 0.0},
    {15.0, -5.0, 0.0},
    {20.0,  5.0, 0.0}
};
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Primitive](primitives.md)
</dt> </dl>

 

 
