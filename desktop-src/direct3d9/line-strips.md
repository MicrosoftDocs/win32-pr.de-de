---
description: Ein Linienstreifen ist ein Primitiver, der aus verbundenen Liniensegmenten besteht.
ms.assetid: 73905718-a4c6-4f73-beef-4cccac7eea8c
title: Linienstreifen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dd8ba98518cac542a9b8272e4f96494889ef24f269744626aa24e882c7af509
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118799631"
---
# <a name="line-strips"></a>Linienstreifen

Ein Linienstreifen ist ein Primitiver, der aus verbundenen Liniensegmenten besteht. Ihre Anwendung kann Linienstreifen zum Erstellen von Polygonen verwenden, die nicht geschlossen sind. Ein geschlossenes Polygon ist ein Polygon, dessen letzter Scheitelpunkt durch ein Liniensegment mit seinem ersten Scheitelpunkt verbunden ist. Wenn Ihre Anwendung Polygone basierend auf Linienstreifen macht, ist nicht garantiert, dass die Scheitelpunkte koplanar sind.

Die folgende Abbildung zeigt einen gerenderten Zeilenstreifen.

![Abbildung eines Linienstreifens](images/linstrip.gif)

Der folgende Code zeigt, wie Scheitelpunkte für diesen Zeilenstreifen erstellt werden.


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



Das folgende Codebeispiel zeigt, wie sie einen Zeilenstreifen in Direct3D 9 mithilfe von [**IDirect3DDevice9::D rawPrimitive rendern.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)


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

 

 
