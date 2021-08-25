---
title: Hinzufügen von Unterstützung für mehrere Monitore
description: DirectWrite bietet Unterstützung für Systeme mit mehreren Monitoren.
ms.assetid: 62274126-49da-4166-8482-73aac2b29c26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12bbfb2c803372e52128cd62dddeec407985e4180039d84f9aed66092149911b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048890"
---
# <a name="how-to-add-support-for-multiple-monitors"></a>Hinzufügen von Unterstützung für mehrere Monitore

[DirectWrite](direct-write-portal.md) bietet Unterstützung für Systeme mit mehreren Monitoren. Verschiedene Monitore können unterschiedliche Pixelgeometrien (RGB, BGR oder FLAT) oder andere Attribute aufweisen. Weitere Informationen zur Pixelgeometrie finden Sie im [**Referenzthema DWRITE \_ PIXEL \_ GEOMETRY.**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry) In diesem Thema erfahren Sie, wie Sie Ihrer DirectWrite-Anwendung Unterstützung für mehrere Monitore hinzufügen.

Um mehrere Monitore zu unterstützen, müssen Sie die **WM \_ WINDOWPOSCHANGED-Fenstermeldung** verarbeiten. Diese Meldung wird gesendet, wenn das Fenster verschoben wird. Daher müssen Sie überprüfen, ob das Fenster auf einen anderen Monitor verschoben wurde, wie im folgenden Code gezeigt.


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



Wenn sich das Fenster auf einem neuen Monitor befindet, müssen Sie Renderingparameter für den neuen Monitor erstellen, indem Sie die [**IDWriteFactory::CreateMonitorRenderingParams-Methode**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createmonitorrenderingparams) verwenden.

> [!Note]  
> Verwenden Sie nicht die [**IDWriteFactory::CreateRenderingParams-Methode,**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createrenderingparams) um die Renderingparameter zu erstellen, da sie immer Parameter für den primären Monitor erstellt.

 

Wenn Sie über ein [**IDWriteRenderingParams-Objekt**](/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams) verfügen, legen Sie die Renderingparameter für das Renderziel mithilfe der [**ID2DRenderTarget::SetTextRenderingParams-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settextrenderingparams) fest.

Verwenden Sie abschließend die [**InvalidateRect-Funktion,**](/windows/win32/api/winuser/nf-winuser-invalidaterect) um das Fenster mit den neuen Renderingparametern neu zu zeichnen.

 

 