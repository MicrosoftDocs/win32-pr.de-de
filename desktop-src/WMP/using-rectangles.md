---
title: Verwenden von Rechtecke (Windows Media Player SDK)
description: Verwenden von Rechtecke
ms.assetid: b3fc16b4-dc93-43c0-a97d-5234e36437c8
keywords:
- Visualisierungen, Rechtecke
- benutzerdefinierte Visualisierungen, Rechtecke
- Visualisierungen, Rendering-Funktion
- benutzerdefinierte Visualisierungen, Rendering-Funktion
- Rendering-Funktion, Rechtecke
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b48f16888d8e71c052d216a838683f2b7127e75
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106338705"
---
# <a name="using-rectangles-windows-media-player-sdk"></a><span data-ttu-id="fe4d2-108">Verwenden von Rechtecke (Windows Media Player SDK)</span><span class="sxs-lookup"><span data-stu-id="fe4d2-108">Using Rectangles (Windows Media Player SDK)</span></span>

<span data-ttu-id="fe4d2-109">Rechtecke werden verwendet, um rechteckige Bereiche in Microsoft Windows anzugeben.</span><span class="sxs-lookup"><span data-stu-id="fe4d2-109">Rectangles are used to specify rectangular areas in Microsoft Windows.</span></span> <span data-ttu-id="fe4d2-110">Sie können in Ihrem Fenster viele Rechtecke erstellen, aber Windows Media Player die Werte eines Rechtecks über die [iwmpeffects:: Rendering](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-render) -Funktion bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="fe4d2-110">You can create many rectangles in your window, but Windows Media Player supplies the values of one rectangle through the [IWMPEffects::Render](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-render) function.</span></span> <span data-ttu-id="fe4d2-111">Wenn das Plug-in mithilfe eines Fensters gerendert wird, ist das Rechteck der Client Bereich des Fensters.</span><span class="sxs-lookup"><span data-stu-id="fe4d2-111">If your plug-in renders using a window, the rectangle is the client area of the window.</span></span> <span data-ttu-id="fe4d2-112">Dies wird als PRC-Rechteck bezeichnet und definiert das Rechteck, mit dem die Visualisierung in Windows Media Player angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="fe4d2-112">This is called the prc rectangle, and it defines the rectangle that Windows Media Player will display your visualization through.</span></span> <span data-ttu-id="fe4d2-113">Verwenden Sie dies häufig, um sicherzustellen, dass Sie nicht über die Blöcke der von Windows Media Player bereitgestellten Rechteck hinaus zeichnen.</span><span class="sxs-lookup"><span data-stu-id="fe4d2-113">Use this frequently to be sure you do not draw beyond the extents of the rectangle supplied by Windows Media Player.</span></span>

<span data-ttu-id="fe4d2-114">Ein Rechteck hat vier Werte, die es definieren.</span><span class="sxs-lookup"><span data-stu-id="fe4d2-114">A rectangle has four values that define it.</span></span> <span data-ttu-id="fe4d2-115">Sie sind Links, oben, rechts und unten.</span><span class="sxs-lookup"><span data-stu-id="fe4d2-115">They are left, top, right, and bottom.</span></span> <span data-ttu-id="fe4d2-116">Die obere linke Ecke des Rechtecks wird von Links und oben definiert, und die untere rechte Ecke des Rechtecks wird von unten und rechts definiert.</span><span class="sxs-lookup"><span data-stu-id="fe4d2-116">The top, left corner of the rectangle is defined by left and top, and the bottom, right corner of the rectangle is defined by bottom and right.</span></span>

<span data-ttu-id="fe4d2-117">Verwenden Sie den folgenden Code, um die Blöcke des Zeichnungs Rechtecks zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="fe4d2-117">Use the following code to get the extents of your drawing rectangle.</span></span> <span data-ttu-id="fe4d2-118">Dies ist erforderlich, da der Benutzer die Größe des Fensters ändern kann, und Sie möchten sicher sein, dass Sie immer in einem Bereich zeichnen, den der Benutzer sehen kann.</span><span class="sxs-lookup"><span data-stu-id="fe4d2-118">You need to do this because the user may resize the window, and you want to be sure that you are always drawing in an area the user can see.</span></span>


```C++
int leftside = prc->left;
int rightside = prc->right;
int topside = prc->top;
int bottomside = prc->bottom;

```



<span data-ttu-id="fe4d2-119">Wenn Sie z. b. von links nach rechts am oberen Rand des Fensters zeichnen möchten, verwenden Sie Code wie den folgenden:</span><span class="sxs-lookup"><span data-stu-id="fe4d2-119">For example, to draw from left to right, along the top of the window, use code like this:</span></span>


```C++
::MoveToEx( hdc, prc->left, prc->top, NULL );  
::LineTo(hdc, prc->right, prc->top);

```



## <a name="related-topics"></a><span data-ttu-id="fe4d2-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fe4d2-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe4d2-121">**Implementieren von Rendering**</span><span class="sxs-lookup"><span data-stu-id="fe4d2-121">**Implementing Render**</span></span>](implementing-render.md)
</dt> </dl>

 

 




