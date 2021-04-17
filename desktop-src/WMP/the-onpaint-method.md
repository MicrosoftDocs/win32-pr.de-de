---
title: Die OnPaint-Methode
description: Die OnPaint-Methode
ms.assetid: 4b335362-4430-4b05-8aea-7de8df9cc91f
keywords:
- Windows Media Player-Plug-ins, OnPaint-Methode
- Plug-ins, OnPaint-Methode
- Benutzeroberflächen-Plug-ins, OnPaint-Methode
- UI-Plug-ins, OnPaint-Methode
- OnPaint-Methode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22641c34bb2edab30c1bf97011e893bc1d9d44a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471628"
---
# <a name="the-onpaint-method"></a><span data-ttu-id="c69d5-108">Die OnPaint-Methode</span><span class="sxs-lookup"><span data-stu-id="c69d5-108">The OnPaint Method</span></span>

<span data-ttu-id="c69d5-109">Die OnPaint-Methode wird immer dann aufgerufen, wenn sich das Plug-in-Fenster selbst zeichnen soll.</span><span class="sxs-lookup"><span data-stu-id="c69d5-109">The OnPaint method is called whenever the plug-in window should paint itself.</span></span> <span data-ttu-id="c69d5-110">Dies tritt auf, wenn das Plug-in-Fenster eine WM \_ Paint-Meldung empfängt, die der OnPaint-Methode in der zuvor beschriebenen Meldungs Zuordnung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c69d5-110">This occurs when the plug-in window receives a WM\_PAINT message, which is mapped to the OnPaint method in the message map described earlier.</span></span> <span data-ttu-id="c69d5-111">Der Assistent stellt eine Implementierung dieser Methode bereit, die den Hintergrund schwarz zeichnet und den Namen des Plug-ins im Plug-in-Fenster platziert.</span><span class="sxs-lookup"><span data-stu-id="c69d5-111">The wizard provides an implementation of this method that paints the background black and places the name of the plug-in in the plug-in window.</span></span> <span data-ttu-id="c69d5-112">Die einzige Änderung, die für das Such Benutzeroberflächen-Plug-in erforderlich ist, ist das Entfernen des Codes, in dem der Text angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="c69d5-112">The only modification that is necessary for the Search UI plug-in is the removal of the code that displays the text.</span></span>

<span data-ttu-id="c69d5-113">Der folgende Code wird verwendet, um diese Methode zu implementieren:</span><span class="sxs-lookup"><span data-stu-id="c69d5-113">The following code is used to implement this method:</span></span>


```C++
LRESULT OnPaint(UINT nMsg, WPARAM wParam, 
                         LPARAM lParam, BOOL& bHandled)
{
    PAINTSTRUCT ps;

    HDC hDC = BeginPaint(&ps);

    RECT rc;
    GetClientRect(&rc);

    HBRUSH hNewBrush = ::CreateSolidBrush( RGB(0, 0, 0) );

    if (hNewBrush)
    {
        ::FillRect(hDC, &rc, hNewBrush );
        ::DeleteObject( hNewBrush );
    }

    EndPaint(&ps);
    return 0;
}

```



## <a name="related-topics"></a><span data-ttu-id="c69d5-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c69d5-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c69d5-115">**Implementieren von cpluginwindow**</span><span class="sxs-lookup"><span data-stu-id="c69d5-115">**Implementing CPluginWindow**</span></span>](implementing-cpluginwindow.md)
</dt> </dl>

 

 




