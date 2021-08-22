---
description: Eine Linienliste ist eine Liste isolierter, gerader Segmente.
ms.assetid: bb02b3d6-f30f-4f2b-8b40-a7e37faf524a
title: Zeilenlisten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f06ca68e3fefab1217e77bbf41bc30aa42dac9631b70480fe4bf0a98d38d913
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606795"
---
# <a name="line-lists"></a>Zeilenlisten

Eine Linienliste ist eine Liste isolierter, gerader Segmente. Linienlisten sind nützlich für Aufgaben wie das Hinzufügen von Sleet oder starkem Regen zu einer 3D-Szene. Anwendungen erstellen eine Zeilenliste, indem sie ein Array von Scheitelpunkten auffüllen. Beachten Sie, dass die Anzahl der Scheitelpunkte in einer Zeilenliste eine gerade Zahl größer oder gleich zwei sein muss.

Die folgende Abbildung zeigt eine gerenderte Zeilenliste.

![Abbildung einer Zeilenliste](images/linelst.png)

Sie können Materialien und Texturen auf eine Linienliste anwenden. Die Farben im Material oder der Textur werden nur entlang der gezeichneten Linien angezeigt, nicht an einem Punkt zwischen den Linien.

Der folgende Code zeigt, wie Scheitelpunkte für diese Zeilenliste erstellt werden.


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



Das folgende Codebeispiel zeigt, wie Sie eine Zeilenliste in Direct3D 9 mit [**IDirect3DDevice9::D rawPrimitive rendern.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)


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

 

 
