---
description: Eine Zeilen Liste ist eine Liste isolierter, gerader Liniensegmente.
ms.assetid: bb02b3d6-f30f-4f2b-8b40-a7e37faf524a
title: Linien Listen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b27bd58ea2de6b5944b8511e99154c50f671439
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106341104"
---
# <a name="line-lists"></a>Linien Listen

Eine Zeilen Liste ist eine Liste isolierter, gerader Liniensegmente. Zeilen Listen sind nützlich für Aufgaben wie das Hinzufügen von einem oder hohem Regen zu einer 3D-Szene. Anwendungen erstellen eine Zeilen Liste, indem Sie ein Array von Vertices auffüllen. Beachten Sie, dass die Anzahl der Scheitel Punkte in einer Zeilen Liste eine gerade Zahl größer oder gleich zwei sein muss.

Die folgende Abbildung zeigt eine Liste gerenderter Linien.

![Abbildung einer Zeilen Liste](images/linelst.png)

Sie können Materialien und Texturen auf eine Linien Liste anwenden. Die Farben in dem Material oder der Textur werden nur entlang der gezeichneten Linien angezeigt, nicht an einem Punkt zwischen den Linien.

Der folgende Code zeigt, wie Scheitel Punkte für diese Zeilen Liste erstellt werden.


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



Das folgende Codebeispiel zeigt, wie Sie eine Zeilen Liste in Direct3D 9 mit [**IDirect3DDevice9::D rawprimitiv**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)Rendering.


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_LINELIST, 0, 3 );
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Primitive](primitives.md)
</dt> </dl>

 

 
