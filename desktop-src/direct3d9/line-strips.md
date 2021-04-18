---
description: Ein Zeilen Streifen ist ein primitiver, der aus verbundenen Liniensegmenten besteht.
ms.assetid: 73905718-a4c6-4f73-beef-4cccac7eea8c
title: Zeilen Streifen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dee7eb79b583ad04dc0ed576a7d9426e8dda9fa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521952"
---
# <a name="line-strips"></a>Zeilen Streifen

Ein Zeilen Streifen ist ein primitiver, der aus verbundenen Liniensegmenten besteht. Die Anwendung kann Zeilen Streifen zum Erstellen von Polygonen verwenden, die nicht geschlossen sind. Ein geschlossenes Polygon ist ein Polygon, dessen letzter Scheitelpunkt durch ein Liniensegment mit dem ersten Scheitelpunkt verbunden ist. Wenn Ihre Anwendung Polygone auf Basis von Zeilen Streifen erstellt, sind die Scheitel Punkte nicht garantiert Coplanar.

Die folgende Abbildung zeigt einen gerenderten Zeilen Streifen.

![Abbildung eines Zeilen Streifens](images/linstrip.gif)

Der folgende Code zeigt, wie Vertices für diesen Zeilen Streifen erstellt werden.


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



Das folgende Codebeispiel zeigt, wie Sie einen Zeilen Streifen in Direct3D 9 mit [**IDirect3DDevice9::D rawprimitiv**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) Renderern.


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_LINESTRIP, 0, 5 );
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Primitive](primitives.md)
</dt> </dl>

 

 
