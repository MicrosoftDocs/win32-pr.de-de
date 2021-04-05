---
title: Verwenden einer Bitmap als Deck Kraft Maske
description: Zeigt, wie Sie einen Bereich mit bitmapmasken Ausschneiden.
ms.assetid: d6ad53a6-5e84-49d0-ab2c-5d6ad9428f9c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2106f43a6845cd724204fbf3e5aa1ec2b866bf46
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948985"
---
# <a name="how-to-use-a-bitmap-as-an-opacity-mask"></a><span data-ttu-id="722b1-103">Verwenden einer Bitmap als Deck Kraft Maske</span><span class="sxs-lookup"><span data-stu-id="722b1-103">How to Use a Bitmap as an Opacity Mask</span></span>

<span data-ttu-id="722b1-104">In diesem Thema wird beschrieben, wie Sie eine Bitmap als eine opacty mask verwenden, indem Sie die [**ID2D1Factory:: fillopacitymask**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="722b1-104">This topic describes how to use a bitmap as an opacty mask by calling the [**ID2D1Factory::FillOpacityMask**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) method.</span></span> <span data-ttu-id="722b1-105">Die Deck Kraft Maske ist eine Bitmap, die die durch den Alphakanal dargestellten Abdeckungs Informationen bereitstellt, die die Transparenz des gerenderten Inhalts steuert.</span><span class="sxs-lookup"><span data-stu-id="722b1-105">The opacity mask is a bitmap that supplies the coverage information that is represented by the alpha channel, which controls the transparency of the content that is rendered.</span></span> <span data-ttu-id="722b1-106">Diese Vorgehensweise ist effizienter als die Verwendung von Ebenen mit einer Deck Kraft Maske.</span><span class="sxs-lookup"><span data-stu-id="722b1-106">This approach is more efficient than using layers with an opacity mask.</span></span> <span data-ttu-id="722b1-107">Weitere Informationen finden Sie unter [Übersicht über Ebenen](direct2d-layers-overview.md).</span><span class="sxs-lookup"><span data-stu-id="722b1-107">For more information, see [Layers Overview](direct2d-layers-overview.md).</span></span>

<span data-ttu-id="722b1-108">**So schneiden Sie einen Bereich ab**</span><span class="sxs-lookup"><span data-stu-id="722b1-108">**To clip a region**</span></span>

1.  <span data-ttu-id="722b1-109">Laden Sie die ursprüngliche Bitmap aus einer Ressource.</span><span class="sxs-lookup"><span data-stu-id="722b1-109">Load the original bitmap from a resource.</span></span> <span data-ttu-id="722b1-110">Weitere Informationen zum Laden einer Bitmap finden Sie unter Gewusst [wie: Laden einer Bitmap aus einer Ressource](how-to-load-a-bitmap-from-a-resource.md).</span><span class="sxs-lookup"><span data-stu-id="722b1-110">For information on how to load a bitmap, see [How to Load a Bitmap from a Resource](how-to-load-a-bitmap-from-a-resource.md).</span></span>
2.  <span data-ttu-id="722b1-111">Laden Sie die bitmapmaske aus einer Ressource.</span><span class="sxs-lookup"><span data-stu-id="722b1-111">Load the bitmap mask from a resource.</span></span>
3.  <span data-ttu-id="722b1-112">Erstellen Sie einen Bitmap-Pinsel mit der ursprünglichen Bitmap.</span><span class="sxs-lookup"><span data-stu-id="722b1-112">Create a bitmap brush with the original bitmap.</span></span> <span data-ttu-id="722b1-113">Informationen zum Erstellen eines Bitmap-Pinsels finden Sie unter [Erstellen eines Bitmap-Pinsels](how-to-create-a-bitmap-brush.md).</span><span class="sxs-lookup"><span data-stu-id="722b1-113">For information on how to create a bitmap brush, see [How to Create a Bitmap Brush](how-to-create-a-bitmap-brush.md).</span></span>
4.  <span data-ttu-id="722b1-114">Aufrufen von [**ID2D1Factory:: setantialiasmode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) , um den AntiAlias Modus für das Renderziel auf den D2D1- \_ Antialias \_ Modus \_ für [**ID2D1Factory:: fillopacitymask**](id2d1rendertarget-fillopacitymask.md) festzulegen, um zu funktionieren.</span><span class="sxs-lookup"><span data-stu-id="722b1-114">Call [**ID2D1Factory::SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) to set antialias mode on the render target to D2D1\_ANTIALIAS\_MODE\_ALIASED for [**ID2D1Factory::FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) to work.</span></span>
5.  <span data-ttu-id="722b1-115">Ruft [**fillopacitymask**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) mit der Bitmap-Maske und dem Bitmap-Pinsel auf dem Renderziel auf, um den Clip auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="722b1-115">Call [**FillOpacityMask**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) with the bitmap mask and the bitmap brush on the render target to fill the clip.</span></span>

<span data-ttu-id="722b1-116">Die folgende Abbildung zeigt die ursprüngliche Bitmap auf der linken Seite, die bitmapmaske in der Mitte und die Bitmap, die auf die Maske auf der rechten Seite abgeschnitten wird.</span><span class="sxs-lookup"><span data-stu-id="722b1-116">The following illustration shows the original bitmap on the left, the bitmap mask in the center, and the bitmap clipped to the mask on the right.</span></span>

![Abbildung einer Goldfisch-Bitmap, einer aus der Bitmap erstellten fischförmigen Maske und der resultierenden fischförmigen Bitmap nach der Maske](images/cliparegion-opacitymask.png)

<span data-ttu-id="722b1-118">Der folgende Code zeigt, wie Sie den Bereich mit der in der vorherigen Abbildung gezeigten Maske Ausschneiden.</span><span class="sxs-lookup"><span data-stu-id="722b1-118">The following code shows how to clip the region with the mask shown in the preceding illustration.</span></span> <span data-ttu-id="722b1-119">Zuerst werden die ursprüngliche Bitmap und die bitmapmaske geladen.</span><span class="sxs-lookup"><span data-stu-id="722b1-119">It first loads the original bitmap and the bitmap mask.</span></span> <span data-ttu-id="722b1-120">Und erstellt dann einen Bitmap-Pinsel mit der ursprünglichen Bitmap.</span><span class="sxs-lookup"><span data-stu-id="722b1-120">And then creates a bitmap brush with the original bitmap.</span></span>


```C++
// Create the bitmap to be used by the bitmap brush
if (SUCCEEDED(hr))
{
    hr = LoadResourceBitmap(
        m_pRenderTarget,
        m_pWICFactory,
        L"GoldFish",
        L"Image",
        &m_pOrigBitmap
        );
}

if (SUCCEEDED(hr))
{
    hr = LoadResourceBitmap(
        m_pRenderTarget,
        m_pWICFactory,
        L"GoldFishMask",
        L"Image",
        &m_pBitmapMask
        );
}

if (SUCCEEDED(hr))
{
    D2D1_BITMAP_BRUSH_PROPERTIES propertiesXClampYClamp = D2D1::BitmapBrushProperties(
        D2D1_EXTEND_MODE_CLAMP,
        D2D1_EXTEND_MODE_CLAMP,
        D2D1_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR
        );

    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pOrigBitmap,
        propertiesXClampYClamp,
        &m_pOriginalBitmapBrush
        );

    if (SUCCEEDED(hr))
    {
        hr = m_pRenderTarget->CreateBitmapBrush(
            m_pBitmapMask,
            propertiesXClampYClamp,
            &m_pBitmapMaskBrush
            );
    }
}
```



<span data-ttu-id="722b1-121">Anschließend wird [**setantialiasmode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) aufgerufen, um den AntiAlias Modus festzulegen.</span><span class="sxs-lookup"><span data-stu-id="722b1-121">It then calls [**SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) to set the antialias mode.</span></span> <span data-ttu-id="722b1-122">Ruft [**fillopacitymask**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) auf, um eine Bitmap-Maske zum Ausschneiden der ursprünglichen Bitmap zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="722b1-122">Call [**FillOpacityMask**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) to use a bitmap mask to clip the original bitmap.</span></span>


```C++
// D2D1_ANTIALIAS_MODE_ALIASED must be set for FillOpacityMask
// to function properly.
m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_ALIASED);

m_pRenderTarget->FillOpacityMask(
    m_pBitmapMask,
    m_pOriginalBitmapBrush,
    D2D1_OPACITY_MASK_CONTENT_GRAPHICS,
    &rcBrushRect,
    NULL
    );

m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_PER_PRIMITIVE);

```



<span data-ttu-id="722b1-123">Weitere Informationen zu Deck Kraft Masken finden Sie unter [Übersicht über die Deckkraft Masken](opacity-masks-overview.md).</span><span class="sxs-lookup"><span data-stu-id="722b1-123">For more information about opacity masks, see the [Opacity Masks Overview](opacity-masks-overview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="722b1-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="722b1-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="722b1-125">Direct2D-Referenz</span><span class="sxs-lookup"><span data-stu-id="722b1-125">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 