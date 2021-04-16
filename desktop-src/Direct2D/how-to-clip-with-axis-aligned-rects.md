---
title: Vorgehensweise beim Abschneiden mit einem Axis-Aligned Clip-Rechteck
description: Zeigt, wie Sie einen Bereich mit einem Achsen ausgerichteten Clip Rechteck ausschneiden.
ms.assetid: 4196653a-9177-4a41-9db9-4738a41313aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d9fea904f9df396918d2cdfdb5205f6dd0197d0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104564076"
---
# <a name="how-to-clip-with-an-axis-aligned-clip-rectangle"></a><span data-ttu-id="4f7f0-103">Vorgehensweise beim Abschneiden mit einem Axis-Aligned Clip-Rechteck</span><span class="sxs-lookup"><span data-stu-id="4f7f0-103">How to Clip with an Axis-Aligned Clip Rectangle</span></span>

<span data-ttu-id="4f7f0-104">In diesem Thema wird beschrieben, wie Sie ein Bild mithilfe eines Achsen ausgerichteten Clip Rechtecks Ausschneiden.</span><span class="sxs-lookup"><span data-stu-id="4f7f0-104">This topic describes how to clip an image with an axis-aligned clip rectangle.</span></span> <span data-ttu-id="4f7f0-105">Bei diesem Ansatz werden nur rechteckige Clips erzeugt, da die Inhalts Begrenzungen an der Achse des Rechtecks ausgerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="4f7f0-105">This approach produces only rectangular clips, because the content bounds are aligned to the axis of the rectangle.</span></span> <span data-ttu-id="4f7f0-106">Diese Vorgehensweise ist effizienter als die Verwendung von Ebenen mit den Inhalts Begrenzungen.</span><span class="sxs-lookup"><span data-stu-id="4f7f0-106">This approach is more efficient than using layers with the content bounds.</span></span> <span data-ttu-id="4f7f0-107">Weitere Informationen finden Sie unter[Übersicht über Ebenen](direct2d-layers-overview.md).</span><span class="sxs-lookup"><span data-stu-id="4f7f0-107">For more information, see[Layers Overview](direct2d-layers-overview.md).</span></span>

<span data-ttu-id="4f7f0-108">**So schneiden Sie mithilfe eines Achsen ausgerichteten Clip Rechtecks ab**</span><span class="sxs-lookup"><span data-stu-id="4f7f0-108">**To clip with an axis-aligned clip rectangle**</span></span>

1.  <span data-ttu-id="4f7f0-109">Laden Sie das ursprüngliche Bild aus einer Ressource.</span><span class="sxs-lookup"><span data-stu-id="4f7f0-109">Load the original image from a resource.</span></span> <span data-ttu-id="4f7f0-110">Weitere Informationen zum Laden einer Bitmap finden Sie unter Gewusst [wie: Laden einer Bitmap aus einer Ressource](how-to-load-a-bitmap-from-a-resource.md).</span><span class="sxs-lookup"><span data-stu-id="4f7f0-110">For information on how to load a bitmap, see [How to Load a Bitmap from a Resource](how-to-load-a-bitmap-from-a-resource.md).</span></span>
2.  <span data-ttu-id="4f7f0-111">[**ID2D1RenderTarget::P ushaxisalignedclip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) zum Angeben eines Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="4f7f0-111">Call [**ID2D1RenderTarget::PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) to specify a rectangle.</span></span> <span data-ttu-id="4f7f0-112">Die renderingbefehle werden auf das Rechteck zugeschnitten.</span><span class="sxs-lookup"><span data-stu-id="4f7f0-112">The rendering commands are clipped to the rectangle.</span></span>

3.  <span data-ttu-id="4f7f0-113">Zeichnen Sie das ursprüngliche Bild.</span><span class="sxs-lookup"><span data-stu-id="4f7f0-113">Paint the original image.</span></span>
4.  <span data-ttu-id="4f7f0-114">[**ID2D1RenderTarget::P opaxisalignedclip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) aufgerufen, um den letzten an der Achse ausgerichteten Clip aus dem Renderziel zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="4f7f0-114">Call [**ID2D1RenderTarget::PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) to remove the last axis-aligned clip from the render target.</span></span>

<span data-ttu-id="4f7f0-115">In der folgenden Abbildung ist beispielsweise die ursprüngliche Bitmap auf der linken Seite 200 \* 130 Pixel.</span><span class="sxs-lookup"><span data-stu-id="4f7f0-115">For example, in the following illustration, the original bitmap on the left is 200\*130 pixels.</span></span> <span data-ttu-id="4f7f0-116">Die Bitmap auf der rechten Seite ist die ursprüngliche Bitmap, die auf das Achsen ausgerichtete Clip Rechteck zugeschnitten ist.</span><span class="sxs-lookup"><span data-stu-id="4f7f0-116">The bitmap on the right is the original bitmap clipped to the axis-aligned clip rectangle.</span></span> <span data-ttu-id="4f7f0-117">Die Abmessungen sind (20, 20) bis (100, 100).</span><span class="sxs-lookup"><span data-stu-id="4f7f0-117">The dimensions are (20, 20) to (100, 100).</span></span>

![Abbildung einer Goldfisch-Bitmap vor und nach dem abgeschnitten der Bitmap](images/cliparegion-axisalignedclip.png)

<span data-ttu-id="4f7f0-119">Um das abgeschnittene Bild zu erstellen, erstellen Sie eine Rechteck Struktur als Clippingbereich.</span><span class="sxs-lookup"><span data-stu-id="4f7f0-119">To create the clipped image, create a rectangle structure as the clipping area.</span></span> <span data-ttu-id="4f7f0-120">Nennen Sie [**pushaxisalignedclip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) mit dem Clippingbereich, und zeichnen Sie das ursprüngliche Bild.</span><span class="sxs-lookup"><span data-stu-id="4f7f0-120">Call [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) with the clipping area and paint the original image.</span></span> <span data-ttu-id="4f7f0-121">Nennen Sie [**popaxisalignedclip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) , um den Clip aus dem Renderziel zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="4f7f0-121">Call [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) to remove the clip from the render target.</span></span> <span data-ttu-id="4f7f0-122">Dies wird im folgenden Code veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="4f7f0-122">The following code shows how to do this.</span></span>


```C++
pRT->PushAxisAlignedClip(
    D2D1::RectF(20, 20, 100, 100),
    D2D1_ANTIALIAS_MODE_PER_PRIMITIVE
    );

pRT->FillRectangle(D2D1::RectF(0, 0, 200, 133), m_pOriginalBitmapBrush);
pRT->PopAxisAlignedClip();
```



## <a name="related-topics"></a><span data-ttu-id="4f7f0-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4f7f0-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f7f0-124">Direct2D-Referenz</span><span class="sxs-lookup"><span data-stu-id="4f7f0-124">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 