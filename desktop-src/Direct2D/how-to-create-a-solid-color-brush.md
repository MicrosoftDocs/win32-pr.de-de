---
title: Erstellen eines Pinsel mit voll Tonfarbe
description: Zeigt, wie ein vollfarbiger Farbpinsel mit Direct2D erstellt wird.
ms.assetid: 70700b82-2294-46be-b1c0-fc89def441e2
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: bc6fbf5df42386f5e0e5a843a1906d36d4fc8c71
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948823"
---
# <a name="how-to-create-a-solid-color-brush"></a><span data-ttu-id="478c6-103">Erstellen eines Pinsel mit voll Tonfarbe</span><span class="sxs-lookup"><span data-stu-id="478c6-103">How to Create a Solid Color Brush</span></span>

<span data-ttu-id="478c6-104">Um einen Pinsel mit voll Tonfarbe zu erstellen, verwenden Sie die [**ID2DRenderTarget:: froatesolidcolorbrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) -Methode, und geben Sie die Farbe an, mit der Sie zeichnen möchten.</span><span class="sxs-lookup"><span data-stu-id="478c6-104">To create a solid color brush, use the [**ID2DRenderTarget::CreateSolidColorBrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) method and specify the color with which you want to paint.</span></span> <span data-ttu-id="478c6-105">Einige der " **kreatesolidcolorbrush** "-über Ladungen ermöglichen auch die Angabe der Deckkraft des Pinsels.</span><span class="sxs-lookup"><span data-stu-id="478c6-105">Some of the **CreateSolidColorBrush** overloads also enable you to specify the opacity of the brush.</span></span>

<span data-ttu-id="478c6-106">Der folgende Code zeigt, wie Sie einen soliden gelben grünen Pinsel zum Auffüllen eines Quadrats erstellen, und einen Pinsel mit einem Pinsel, um die Kontur des Quadrats zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="478c6-106">The following code shows how to create a solid yellow-green brush to fill a square, and a solid black brush to draw the outline of the square.</span></span> <span data-ttu-id="478c6-107">Der Code erzeugt die in der folgenden Abbildung gezeigte Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="478c6-107">The code produces the output shown in the following illustration.</span></span>

![Abbildung eines Rechtecks, das mit einer grünen gelb grünen Farbe gefüllt ist](images/brushes-ovw-solidcolor.png)

1.  <span data-ttu-id="478c6-109">Deklarieren Sie zwei [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) -Zeiger: einen zum Zeichnen von schwarz und einen für das gelbe grün.</span><span class="sxs-lookup"><span data-stu-id="478c6-109">Declare two [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) pointers: one for painting black and one for painting yellow green.</span></span>
    ```C++
        ID2D1SolidColorBrush *m_pBlackBrush;
        ID2D1SolidColorBrush *m_pYellowGreenBrush;
    ```

    

2.  <span data-ttu-id="478c6-110">Rufen Sie die Methode " [**kreatesolidcolorbrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) " auf, um die Pinsel zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="478c6-110">Call the [**CreateSolidColorBrush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) method to create the brushes:</span></span>
    ```C++
    if (SUCCEEDED(hr))
    {
        hr = m_pRenderTarget->CreateSolidColorBrush(
            D2D1::ColorF(D2D1::ColorF::Black, 1.0f),
            &m_pBlackBrush
            );
    }

    // Create a solid color brush with its rgb value 0x9ACD32.
    if (SUCCEEDED(hr))
    {
        hr = m_pRenderTarget->CreateSolidColorBrush(
            D2D1::ColorF(D2D1::ColorF(0x9ACD32, 1.0f)),  
            &m_pYellowGreenBrush
            );
    }
    ```

    

3.  <span data-ttu-id="478c6-111">Wenn Sie die [**fillrechteck**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f__id2d1brush)) -Methode aufzeichnen, zeichnen Sie das Innere des Rechtecks mit dem gelben grünen Pinsel und der [**drawrechteck**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) -Methode, um die Kontur des Rechtecks mit dem schwarzen Pinsel zu zeichnen:</span><span class="sxs-lookup"><span data-stu-id="478c6-111">Call the [**FillRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f__id2d1brush)) method to paint the interior of the rectangle with the yellow green brush and the [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) method to paint the outline of the rectangle with the black brush:</span></span>
    ```C++
    m_pRenderTarget->FillRectangle(&rcBrushRect, m_pYellowGreenBrush);
    m_pRenderTarget->DrawRectangle(&rcBrushRect, m_pBlackBrush, 1, NULL);
    ```

    

## <a name="related-topics"></a><span data-ttu-id="478c6-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="478c6-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="478c6-113">Direct2D-Referenz</span><span class="sxs-lookup"><span data-stu-id="478c6-113">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 