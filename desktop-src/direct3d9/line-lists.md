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
# <a name="line-lists"></a><span data-ttu-id="99871-103">Linien Listen</span><span class="sxs-lookup"><span data-stu-id="99871-103">Line Lists</span></span>

<span data-ttu-id="99871-104">Eine Zeilen Liste ist eine Liste isolierter, gerader Liniensegmente.</span><span class="sxs-lookup"><span data-stu-id="99871-104">A line list is a list of isolated, straight line segments.</span></span> <span data-ttu-id="99871-105">Zeilen Listen sind nützlich für Aufgaben wie das Hinzufügen von einem oder hohem Regen zu einer 3D-Szene.</span><span class="sxs-lookup"><span data-stu-id="99871-105">Line lists are useful for such tasks as adding sleet or heavy rain to a 3D scene.</span></span> <span data-ttu-id="99871-106">Anwendungen erstellen eine Zeilen Liste, indem Sie ein Array von Vertices auffüllen.</span><span class="sxs-lookup"><span data-stu-id="99871-106">Applications create a line list by filling an array of vertices.</span></span> <span data-ttu-id="99871-107">Beachten Sie, dass die Anzahl der Scheitel Punkte in einer Zeilen Liste eine gerade Zahl größer oder gleich zwei sein muss.</span><span class="sxs-lookup"><span data-stu-id="99871-107">Note that the number of vertices in a line list must be an even number greater than or equal to two.</span></span>

<span data-ttu-id="99871-108">Die folgende Abbildung zeigt eine Liste gerenderter Linien.</span><span class="sxs-lookup"><span data-stu-id="99871-108">The following illustration shows a rendered line list.</span></span>

![Abbildung einer Zeilen Liste](images/linelst.png)

<span data-ttu-id="99871-110">Sie können Materialien und Texturen auf eine Linien Liste anwenden.</span><span class="sxs-lookup"><span data-stu-id="99871-110">You can apply materials and textures to a line list.</span></span> <span data-ttu-id="99871-111">Die Farben in dem Material oder der Textur werden nur entlang der gezeichneten Linien angezeigt, nicht an einem Punkt zwischen den Linien.</span><span class="sxs-lookup"><span data-stu-id="99871-111">The colors in the material or texture appear only along the lines drawn, not at any point in between the lines.</span></span>

<span data-ttu-id="99871-112">Der folgende Code zeigt, wie Scheitel Punkte für diese Zeilen Liste erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="99871-112">The following code shows how to create vertices for this line list.</span></span>


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



<span data-ttu-id="99871-113">Das folgende Codebeispiel zeigt, wie Sie eine Zeilen Liste in Direct3D 9 mit [**IDirect3DDevice9::D rawprimitiv**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)Rendering.</span><span class="sxs-lookup"><span data-stu-id="99871-113">The code example below shows how to render a line list in Direct3D 9 using [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span></span>


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_LINELIST, 0, 3 );
```



## <a name="related-topics"></a><span data-ttu-id="99871-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="99871-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99871-115">Primitive</span><span class="sxs-lookup"><span data-stu-id="99871-115">Primitives</span></span>](primitives.md)
</dt> </dl>

 

 
