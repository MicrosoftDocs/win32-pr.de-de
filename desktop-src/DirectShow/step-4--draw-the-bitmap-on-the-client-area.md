---
description: 'Schritt 4: Zeichnen der Bitmap im Client Bereich'
ms.assetid: fb22468c-9113-46ff-a576-8dee30c458be
title: 'Schritt 4: Zeichnen der Bitmap im Client Bereich'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4975215e5d75de9909f029a3378bd6cc8bc60916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104393814"
---
# <a name="step-4-draw-the-bitmap-on-the-client-area"></a><span data-ttu-id="4c74a-103">Schritt 4: Zeichnen der Bitmap im Client Bereich</span><span class="sxs-lookup"><span data-stu-id="4c74a-103">Step 4: Draw the Bitmap on the Client Area</span></span>

<span data-ttu-id="4c74a-104">\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="4c74a-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="4c74a-105">In diesem Thema wird Schritt 4 beschrieben, wie [ein Poster-Frame gepackt](grabbing-a-poster-frame.md)wird.</span><span class="sxs-lookup"><span data-stu-id="4c74a-105">This topic is Step 4 of [Grabbing a Poster Frame](grabbing-a-poster-frame.md).</span></span>

<span data-ttu-id="4c74a-106">Der letzte Schritt besteht darin, die Bitmap mithilfe der [**SetDIBitsToDevice**](/windows/win32/api/wingdi/nf-wingdi-setdibitstodevice) -Funktion auf den Client Bereich des Anwendungsfensters zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="4c74a-106">The final step is to draw the bitmap onto the client area of the application window, using the [**SetDIBitsToDevice**](/windows/win32/api/wingdi/nf-wingdi-setdibitstodevice) function.</span></span> <span data-ttu-id="4c74a-107">In diesem Beispiel wird die Bitmap einfach in der oberen linken Ecke des Client Bereichs ohne Berücksichtigung der Fenstergröße gezeichnet:</span><span class="sxs-lookup"><span data-stu-id="4c74a-107">This example simply paints the bitmap in the upper-left corner of the client area, without regard to the window size:</span></span>


```C++
case WM_PAINT:
    {
        PAINTSTRUCT ps;
        HDC hdc = BeginPaint(hwnd, &ps);
        if (pbmi)
        {
            int result = SetDIBitsToDevice(hdc, 0, 0, 
                pbmi->biWidth,
                pbmi->biHeight,
                0, 0, 0,
                pbmi->biHeight,
                pBuffer,
                reinterpret_cast<BITMAPINFO*>(pbmi),
                DIB_RGB_COLORS);
        }
        EndPaint(hwnd, &ps);
    }
    break;
```



<span data-ttu-id="4c74a-108">Die Variablen *pbuffer* und *pbmi* werden in [Schritt 1: Erstellen des Windows-Frameworks](step-1--create-the-windows-framework.md)deklariert, und ihre Werte werden in [Schritt 3: Implementieren der Frame-Grabbing-Funktion](step-3--implement-the-frame-grabbing-function.md)abgerufen.</span><span class="sxs-lookup"><span data-stu-id="4c74a-108">The *pBuffer* and *pbmi* variables are declared in [Step 1: Create the Windows Framework](step-1--create-the-windows-framework.md), and their values are obtained in [Step 3: Implement the Frame-Grabbing Function](step-3--implement-the-frame-grabbing-function.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4c74a-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4c74a-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c74a-110">Ein Poster-Frame wird gepackt.</span><span class="sxs-lookup"><span data-stu-id="4c74a-110">Grabbing a Poster Frame</span></span>](grabbing-a-poster-frame.md)
</dt> </dl>

 

 
