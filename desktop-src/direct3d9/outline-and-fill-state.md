---
description: Primitive, die keine Texturen aufweisen, werden mit der Farbe gerendert, die durch Ihr Material angegeben wird, oder mit den Farben, die für die Scheitel Punkte angegeben sind, falls vorhanden.
ms.assetid: 8a7ed4b1-25a1-4984-baea-6e176f0545ea
title: Umriss und Füll Zustand (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65092fb2e4bfe29ac5e9f9291250a0c78b80626d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106342545"
---
# <a name="outline-and-fill-state-direct3d-9"></a><span data-ttu-id="392f4-103">Umriss und Füll Zustand (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="392f4-103">Outline and Fill State (Direct3D 9)</span></span>

<span data-ttu-id="392f4-104">Primitive, die keine Texturen aufweisen, werden mit der Farbe gerendert, die durch Ihr Material angegeben wird, oder mit den Farben, die für die Scheitel Punkte angegeben sind, falls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="392f4-104">Primitives that have no textures are rendered with the color specified by their material, or with the colors specified for the vertices, if any.</span></span> <span data-ttu-id="392f4-105">Sie können die Methode auswählen, um Sie auszufüllen, indem Sie einen Wert angeben, der vom [**D3DFILLMODE**](./d3dfillmode.md) -Enumerationstyp für den D3DRS \_ FillMode-renderzustand definiert wird.</span><span class="sxs-lookup"><span data-stu-id="392f4-105">You can select the method to fill them by specifying a value defined by the [**D3DFILLMODE**](./d3dfillmode.md) enumerated type for the D3DRS\_FILLMODE render state.</span></span>

<span data-ttu-id="392f4-106">Um das Dithering zu aktivieren, muss die Anwendung den D3DRS \_ ditherenable-Enumerationswert als ersten Parameter an [**IDirect3DDevice9:: setrenderstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)übergeben.</span><span class="sxs-lookup"><span data-stu-id="392f4-106">To enable dithering, your application must pass the D3DRS\_DITHERENABLE enumerated value as the first parameter to [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate).</span></span> <span data-ttu-id="392f4-107">Der zweite Parameter muss auf **true** festgelegt werden, um das Dithering zu aktivieren, und **false** , um es zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="392f4-107">It must set the second parameter to **TRUE** to enable dithering, and **FALSE** to disable it.</span></span>

<span data-ttu-id="392f4-108">Manchmal kann das Zeichnen des letzten Pixels in einer Zeile zu einer unschönen Überschneidung mit umgebenden primitiven führen.</span><span class="sxs-lookup"><span data-stu-id="392f4-108">At times, drawing the last pixel in a line can cause unsightly overlap with surrounding primitives.</span></span> <span data-ttu-id="392f4-109">Dies können Sie mit dem \_ Enumerationswert D3DRS lastpixel steuern.</span><span class="sxs-lookup"><span data-stu-id="392f4-109">You can control this using the D3DRS\_LASTPIXEL enumerated value.</span></span> <span data-ttu-id="392f4-110">Ändern Sie diese Einstellung jedoch nicht, ohne dass dies der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="392f4-110">However, do not alter this setting without some forethought.</span></span> <span data-ttu-id="392f4-111">Unter bestimmten Bedingungen kann das Unterdrücken des Renderings des letzten Pixels zu unansehnlichen Lücken zwischen primitiven führen.</span><span class="sxs-lookup"><span data-stu-id="392f4-111">Under some conditions, suppressing the rendering of the last pixel can cause unsightly gaps between primitives.</span></span>

<span data-ttu-id="392f4-112">Objekt umrissen können durch Festlegen des entsprechenden Linien Zeichnungs Musters gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="392f4-112">Object outlines can be drawn by setting the appropriate line drawing pattern.</span></span> <span data-ttu-id="392f4-113">Der Standardzeilen Zeichnungs Zustand ist das Zeichnen von vollziehen.</span><span class="sxs-lookup"><span data-stu-id="392f4-113">The default line drawing state is to draw solid lines.</span></span> <span data-ttu-id="392f4-114">Weitere Informationen finden Sie [unter Line Drawing Support in D3DX (Direct3D 9)](line-drawing-support-in-d3dx.md) Rendering State.</span><span class="sxs-lookup"><span data-stu-id="392f4-114">For more information, see [Line Drawing Support in D3DX (Direct3D 9)](line-drawing-support-in-d3dx.md) render state.</span></span>

## <a name="related-topics"></a><span data-ttu-id="392f4-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="392f4-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="392f4-116">Rendering-Zustände</span><span class="sxs-lookup"><span data-stu-id="392f4-116">Render States</span></span>](render-states.md)
</dt> </dl>

 

 
