---
description: Ein Dreiecks Streifen ist eine Reihe verbundener Dreiecke.
ms.assetid: 3923c570-47a4-4b53-a097-731981380ae0
title: Dreiecks Streifen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2766529a37b994e5fe30815ca6300476f06c7d4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104556171"
---
# <a name="triangle-strips"></a>Dreiecks Streifen

Ein Dreiecks Streifen ist eine Reihe verbundener Dreiecke. Da die Dreiecke verbunden ist, muss die Anwendung nicht wiederholt alle drei Scheitel Punkte für jedes Dreieck angeben. Beispielsweise benötigen Sie nur sieben Scheitel Punkte, um den folgenden Dreieck Streifen zu definieren.

![Abbildung eines Dreiecks Streifens mit sieben Vertices](images/tristrip.png)

Das System verwendet Vertices v1, v2 und V3 zum Zeichnen des ersten Dreiecks. v2, v4 und V3 zum Zeichnen des zweiten Dreiecks. v3, v4 und V5 zum Zeichnen des dritten. V4, V6 und V5 zum Zeichnen des vierten; Und so weiter. Beachten Sie, dass die Scheitel Punkte des zweiten und vierten Dreiecke nicht in der richtigen Reihenfolge sind. Dies ist erforderlich, um sicherzustellen, dass alle Dreiecke in einer Ausrichtung im Uhrzeigersinn gezeichnet werden.

Die meisten Objekte in 3D-Szenen bestehen aus Dreiecks Streifen. Dies liegt daran, dass mithilfe von Dreiecks Streifen komplexe Objekte auf eine Weise festgelegt werden können, die die Speicher-und Verarbeitungszeit effizient verwendet.

In der folgenden Abbildung ist ein gerenderter Dreiecks Streifen dargestellt.

![Abbildung eines gerenderten Dreiecks Streifens](images/tstrip2.png)

Der folgende Code zeigt, wie Scheitel Punkte für diesen Dreiecks Streifen erstellt werden.


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



Das folgende Codebeispiel zeigt, wie Sie diesen Dreiecks Streifen in Direct3D 9 mit [**IDirect3DDevice9::D rawprimitiv**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)Renderern.


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_TRIANGLESTRIP, 0, 4);
```



Verwenden Sie einen Dreiecks Streifen, um Dreiecke zu Renten, die nicht miteinander verbunden sind. Geben Sie zu diesem Zweck ein degeneriertes Dreieck (d. h. ein Dreieck, dessen Bereich NULL ist) in der Dreiecks Liste an. Dadurch wird eine Linie zwischen den beiden Dreiecken erstellt, die nicht dargestellt wird. Um nur den ersten und den letzten Dreiecke aus dem vorherigen Beispiel zu erstellen, ändern Sie den Vertex-Puffer, wie hier gezeigt:


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

 

 
