---
description: Eine Punkt Liste ist eine Sammlung von Vertices, die als isolierte Punkte gerendert werden. Die Anwendung kann Sie in 3D-Szenen für sternfelder oder gepunktete Linien auf der Oberfläche eines Polygons verwenden.
ms.assetid: 82866b07-5043-433f-974a-0a301d4b5491
title: Punkt Listen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57086a445209d9e60173910e07166a6149e0b8d2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746777"
---
# <a name="point-lists"></a>Punkt Listen

Eine Punkt Liste ist eine Sammlung von Vertices, die als isolierte Punkte gerendert werden. Die Anwendung kann Sie in 3D-Szenen für sternfelder oder gepunktete Linien auf der Oberfläche eines Polygons verwenden.

In der folgenden Abbildung wird eine Liste gerenderter Punkte dargestellt.

![Abbildung einer Punkt Liste](images/pointlst.png)

Die Anwendung kann Materialien und Texturen auf eine Punkt Liste anwenden. Die Farben in dem Material oder der Textur werden nur an den Punkten angezeigt, die gezeichnet werden, und nicht an einer beliebigen Stelle zwischen den Punkten.

Der folgende Code zeigt, wie Scheitel Punkte für diese Punkt Liste erstellt werden.


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



Das folgende Codebeispiel zeigt, wie Sie diese Punkt Liste in Direct3D 9 mit [**IDirect3DDevice9::D rawprimitiv**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)Rendering.


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_POINTLIST, 0, 6 );
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Primitive](primitives.md)
</dt> </dl>

 

 
