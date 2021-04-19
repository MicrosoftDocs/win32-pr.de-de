---
description: Eine Dreiecks Liste ist eine Liste isolierter Dreiecke. Sie sind möglicherweise nah beieinander. Eine Dreiecks Liste muss mindestens drei Scheitel Punkte enthalten, und die Gesamtzahl der Scheitel Punkte muss von drei Scheitel Punkten unterschieden werden.
ms.assetid: e5c3470f-361c-458a-a42a-3549c51d8794
title: Dreiecks Listen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 230cac9b4120d31821d70db022ab50d311d7b73e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346422"
---
# <a name="triangle-lists"></a>Dreiecks Listen

Eine Dreiecks Liste ist eine Liste isolierter Dreiecke. Sie sind möglicherweise nah beieinander. Eine Dreiecks Liste muss mindestens drei Scheitel Punkte enthalten, und die Gesamtzahl der Scheitel Punkte muss von drei Scheitel Punkten unterschieden werden.

Verwenden Sie Dreiecks Listen, um ein Objekt zu erstellen, das aus zusammenhängenden Teilen besteht. Beispielsweise besteht eine Möglichkeit zum Erstellen einer Force-Field-Wand in einem 3D-Spiel darin, eine große Liste kleiner, nicht verbundener Dreiecke anzugeben. Wenden Sie dann ein Material und eine Textur an, mit denen ein Licht an die Dreiecks Liste ausgegeben wird. Jedes Dreieck in der Wand scheint zu leuchten. Die Szene hinter der Wand wird durch die Lücken zwischen den Dreiecken teilweise sichtbar, da ein Spieler bei der Betrachtung eines Force-Felds möglicherweise erwartet.

Dreiecks Listen können auch zum Erstellen primitiver Elemente mit Spitzen Kanten eingesetzt werden, die mit der Gouraud-Schattierung schattiert werden. Siehe [Gesicht-und Scheitelpunkt normale Vektoren (Direct3D 9)](face-and-vertex-normal-vectors.md).

Die folgende Abbildung zeigt eine gerenderte Dreiecks Liste.

![Abbildung einer gerenderten Dreiecks Liste](images/trilist.png)

Der folgende Code zeigt, wie Vertices für diese Dreiecks Liste erstellt werden.


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



Das folgende Codebeispiel zeigt, wie Sie diese Dreiecks Liste in Direct3D 9 mit [**IDirect3DDevice9::D rawprimitiv**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)Renderern.


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, 2 );
```



Sie können auch Dreieck Striche verwenden, um Dreiecke zu Renten, die nicht miteinander verbunden sind. Geben Sie hierzu ein degeneriertes Dreieck (d. h. ein Dreieck mit einer Größe von 0) in der Liste an. Dadurch wird eine Linie zwischen den beiden Dreiecken erstellt, die während des Renderings nicht angezeigt wird. Um z. b. nur das erste und letzte Dreieck aus dem vorherigen Beispiel zu rendern, initialisieren Sie den Vertex-Puffer mit den folgenden Vertices:


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

 

 
