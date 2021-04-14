---
title: Vorgehensweise beim Hinzufügen von Unterstützung für mehrere Monitore
description: DirectWrite bietet Unterstützung für Systeme mit mehreren Monitoren.
ms.assetid: 62274126-49da-4166-8482-73aac2b29c26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74c5d95d0e727b4184a2dcce1720379231ce22a8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390602"
---
# <a name="how-to-add-support-for-multiple-monitors"></a><span data-ttu-id="8cdd7-103">Vorgehensweise beim Hinzufügen von Unterstützung für mehrere Monitore</span><span class="sxs-lookup"><span data-stu-id="8cdd7-103">How to Add Support for Multiple Monitors</span></span>

<span data-ttu-id="8cdd7-104">[DirectWrite](direct-write-portal.md) bietet Unterstützung für Systeme mit mehreren Monitoren.</span><span class="sxs-lookup"><span data-stu-id="8cdd7-104">[DirectWrite](direct-write-portal.md) includes support for systems with multiple monitors.</span></span> <span data-ttu-id="8cdd7-105">Verschiedene Monitore verfügen möglicherweise über unterschiedliche Pixelgeometrie (RGB, BGR oder Flat) oder andere Attribute.</span><span class="sxs-lookup"><span data-stu-id="8cdd7-105">Different monitors may have different pixel geometry (RGB, BGR, or FLAT) or other attributes.</span></span> <span data-ttu-id="8cdd7-106">Weitere Informationen zur Pixelgeometrie finden Sie im Thema zum [**dwrite \_ Pixel \_ Geometry**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry) -Referenz Thema.</span><span class="sxs-lookup"><span data-stu-id="8cdd7-106">For more information about pixel geometry, see the [**DWRITE\_PIXEL\_GEOMETRY**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry) reference topic.</span></span> <span data-ttu-id="8cdd7-107">In diesem Thema wird gezeigt, wie Sie Ihrer DirectWrite-Anwendung Unterstützung für mehrere Monitore hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8cdd7-107">This topic will show you how to add support for multiple monitors to your DirectWrite application.</span></span>

<span data-ttu-id="8cdd7-108">Um mehrere Monitore zu unterstützen, müssen Sie die Fenster Meldung "Fenster des **\_ Windows-fremden** Fensters" verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="8cdd7-108">In order to support multiple monitors, you must handle the **WM\_WINDOWPOSCHANGED** window message.</span></span> <span data-ttu-id="8cdd7-109">Diese Meldung wird gesendet, wenn das Fenster verschoben wird, daher müssen Sie überprüfen, ob das Fenster auf einen anderen Monitor verschoben wurde, wie im folgenden Code gezeigt.</span><span class="sxs-lookup"><span data-stu-id="8cdd7-109">This message is sent when the window is moved, so you must check if the window has moved to a different monitor as shown in the following code.</span></span>


```C++
case WM_WINDOWPOSCHANGED:
    {
        HMONITOR monitor = MonitorFromWindow(hwnd, MONITOR_DEFAULTTONULL);
        if (monitor != g_monitor)
        {
            g_monitor = monitor;
            if (g_spRenderTarget != NULL)
            {
                IDWriteRenderingParams* pRenderingParams = NULL;
                g_spDWriteFactory->CreateMonitorRenderingParams(monitor, &pRenderingParams);

                g_spRenderTarget->SetTextRenderingParams(pRenderingParams);

                SafeRelease(&pRenderingParams);
            }

            InvalidateRect(hwnd, NULL, TRUE);
        }
    }
    break;
```



<span data-ttu-id="8cdd7-110">Wenn sich das Fenster auf einem neuen Monitor befindet, müssen Sie Renderingparameter für den neuen Monitor erstellen, indem Sie die [**idschreitefactory:: anatemonitorrenderingparameams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createmonitorrenderingparams) -Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="8cdd7-110">If the window is located on a new monitor, then you must create rendering parameters for the new monitor by using the [**IDWriteFactory::CreateMonitorRenderingParams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createmonitorrenderingparams) method.</span></span>

> [!Note]  
> <span data-ttu-id="8cdd7-111">Verwenden Sie die [**idwrite-Factory::**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createrenderingparams) -Methode zum Erstellen der Renderingparameter nicht, da Sie immer Parameter für den primären Monitor erstellt.</span><span class="sxs-lookup"><span data-stu-id="8cdd7-111">Do not use the [**IDWriteFactory::CreateRenderingParams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createrenderingparams) method to create the rendering parameters, because it always creates parameters for the primary monitor.</span></span>

 

<span data-ttu-id="8cdd7-112">Wenn Sie über ein [**idwrite-enderingparameterobjekt**](/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams) verfügen, legen Sie die Renderingparameter für das Renderziel mithilfe der [**ID2DRenderTarget:: settextrenderingparameams**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settextrenderingparams) -Methode fest.</span><span class="sxs-lookup"><span data-stu-id="8cdd7-112">When you have an [**IDWriteRenderingParams**](/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams) object, set the rendering parameters for the render target by using the [**ID2DRenderTarget::SetTextRenderingParams**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settextrenderingparams) method.</span></span>

<span data-ttu-id="8cdd7-113">Verwenden Sie abschließend die [**invalidatup**](/windows/win32/api/winuser/nf-winuser-invalidaterect) -Funktion, damit das Fenster mit den neuen Renderingparametern neu gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="8cdd7-113">Finally, use the [**InvalidateRect**](/windows/win32/api/winuser/nf-winuser-invalidaterect) function to cause the window to redraw with the new rendering parameters.</span></span>

 

 