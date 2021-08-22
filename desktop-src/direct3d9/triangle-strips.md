---
description: Ein Dreiecksstreifen besteht aus einer Reihe verbundener Dreiecke.
ms.assetid: 3923c570-47a4-4b53-a097-731981380ae0
title: Dreiecksstreifen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf229883fa156afc93ca2889a0a97f4f2c3eabbb344fb7551476c98f33905f8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044106"
---
# <a name="triangle-strips"></a>Dreiecksstreifen

Ein Dreiecksstreifen besteht aus einer Reihe verbundener Dreiecke. Da die Dreiecke verbunden sind, muss die Anwendung nicht wiederholt alle drei Scheitelungen für jedes Dreieck angeben. Beispielsweise benötigen Sie nur sieben Scheitelstellen, um den folgenden Dreiecksstreifen zu definieren.

![Abbildung eines Dreiecksstreifens mit sieben Scheitelungen](images/tristrip.png)

Das System verwendet Scheitelungen v1, v2 und v3, um das erste Dreieck zu zeichnen. v2, v4 und v3 zum Zeichnen des zweiten Dreiecks; v3, v4 und v5 zum Zeichnen des dritten; v4, v6 und v5 zum Zeichnen des vierten; Und so weiter. Beachten Sie, dass die Scheitelungen des zweiten und vierten Dreiecks nicht in der Reihenfolge sind. dies ist erforderlich, um sicherzustellen, dass alle Dreiecke im Uhrzeigersinn gezeichnet werden.

Die meisten Objekte in 3D-Szenen bestehen aus Dreiecksstreifen. Dies liegt daran, dass Dreiecksstreifen verwendet werden können, um komplexe Objekte so anzugeben, dass Arbeitsspeicher und Verarbeitungszeit effizient genutzt werden.

Die folgende Abbildung zeigt einen gerenderten Dreiecksstreifen.

![Abbildung eines gerenderten Dreiecksstreifens](images/tstrip2.png)

Der folgende Code zeigt, wie Scheitelungen für diesen Dreiecksstreifen erstellt werden.


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



Das folgende Codebeispiel zeigt, wie Sie diesen Dreiecksstreifen in Direct3D 9 mithilfe von [**IDirect3DDevice9::D rawPrimitive rendern.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_TRIANGLESTRIP, 0, 4);
```



Verwenden Sie einen Dreiecksstreifen, um Dreiecke zu rendern, die nicht miteinander verbunden sind. Geben Sie hierzu ein degeneriertes Dreieck (d. h. ein Dreieck, dessen Bereich 0 (null) ist) in der Dreiecksliste an. Dadurch wird eine Linie zwischen den beiden Dreiecken erstellt, die nicht gerendert wird. Um nur das erste und letzte Dreieck aus dem vorherigen Beispiel zu rendern, ändern Sie den Scheitelpunktpuffer wie hier gezeigt:


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

 

 
