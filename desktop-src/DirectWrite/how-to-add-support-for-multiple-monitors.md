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
# <a name="how-to-add-support-for-multiple-monitors"></a>Vorgehensweise beim Hinzufügen von Unterstützung für mehrere Monitore

[DirectWrite](direct-write-portal.md) bietet Unterstützung für Systeme mit mehreren Monitoren. Verschiedene Monitore verfügen möglicherweise über unterschiedliche Pixelgeometrie (RGB, BGR oder Flat) oder andere Attribute. Weitere Informationen zur Pixelgeometrie finden Sie im Thema zum [**dwrite \_ Pixel \_ Geometry**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry) -Referenz Thema. In diesem Thema wird gezeigt, wie Sie Ihrer DirectWrite-Anwendung Unterstützung für mehrere Monitore hinzufügen.

Um mehrere Monitore zu unterstützen, müssen Sie die Fenster Meldung "Fenster des **\_ Windows-fremden** Fensters" verarbeiten. Diese Meldung wird gesendet, wenn das Fenster verschoben wird, daher müssen Sie überprüfen, ob das Fenster auf einen anderen Monitor verschoben wurde, wie im folgenden Code gezeigt.


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



Wenn sich das Fenster auf einem neuen Monitor befindet, müssen Sie Renderingparameter für den neuen Monitor erstellen, indem Sie die [**idschreitefactory:: anatemonitorrenderingparameams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createmonitorrenderingparams) -Methode verwenden.

> [!Note]  
> Verwenden Sie die [**idwrite-Factory::**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createrenderingparams) -Methode zum Erstellen der Renderingparameter nicht, da Sie immer Parameter für den primären Monitor erstellt.

 

Wenn Sie über ein [**idwrite-enderingparameterobjekt**](/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams) verfügen, legen Sie die Renderingparameter für das Renderziel mithilfe der [**ID2DRenderTarget:: settextrenderingparameams**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settextrenderingparams) -Methode fest.

Verwenden Sie abschließend die [**invalidatup**](/windows/win32/api/winuser/nf-winuser-invalidaterect) -Funktion, damit das Fenster mit den neuen Renderingparametern neu gezeichnet wird.

 

 