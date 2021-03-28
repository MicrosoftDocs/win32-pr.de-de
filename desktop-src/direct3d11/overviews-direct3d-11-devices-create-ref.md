---
title: Erstellen eines Referenz Geräts
description: In diesem Thema wird gezeigt, wie ein Referenzgerät erstellt wird, das eine äußerst genaue Software Implementierung der Laufzeit implementiert.
ms.assetid: 00d3f5f2-02c6-4ff4-82a9-0726ad4a8cb3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dec5f3834bf1f10027da2a3f3a8e22acdee742b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388596"
---
# <a name="how-to-create-a-reference-device"></a>Vorgehensweise: Erstellen eines Referenz Geräts

In diesem Thema wird gezeigt, wie ein Referenzgerät erstellt wird, das eine äußerst genaue Software Implementierung der Laufzeit implementiert. Um ein Referenzgerät zu erstellen, geben Sie einfach an, dass das Gerät, das Sie erstellen, einen Referenz Treiber verwendet. In diesem Beispiel werden gleichzeitig ein Gerät und eine SwapChain erstellt.

**So erstellen Sie ein Referenzgerät**

1.  Definieren Sie anfängliche Parameter für eine SwapChain.
    ```
        DXGI_SWAP_CHAIN_DESC sd;
        ZeroMemory( &sd, sizeof( sd ) );
        sd.BufferCount = 1;
        sd.BufferDesc.Width = 640;
        sd.BufferDesc.Height = 480;
        sd.BufferDesc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
        sd.BufferDesc.RefreshRate.Numerator = 60;
        sd.BufferDesc.RefreshRate.Denominator = 1;
        sd.BufferUsage = DXGI_USAGE_RENDER_TARGET_OUTPUT;
        sd.OutputWindow = g_hWnd;
        sd.SampleDesc.Count = 1;
        sd.SampleDesc.Quality = 0;
        sd.Windowed = TRUE;
    ```

    

2.  Fordern Sie eine Funktionsebene an, die die Features implementiert, die Ihre Anwendung benötigt. Ein Referenzgerät kann für die Direct3D 11-Laufzeit erfolgreich erstellt werden.

    ```
        D3D_FEATURE_LEVEL FeatureLevels = D3D_FEATURE_LEVEL_11_0;
    ```

    

    Weitere Informationen zu featureebenen finden Sie in der Enumeration der [**D3D- \_ Funktions \_ Ebene**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) .

3.  Erstellen Sie das Gerät durch Aufrufen von [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).


```
    HRESULT hr = S_OK;
    D3D_FEATURE_LEVEL FeatureLevel;

    if( FAILED (hr = D3D11CreateDeviceAndSwapChain( NULL, 
                    D3D_DRIVER_TYPE_REFERENCE,
                    NULL, 
                    0,
                    &FeatureLevels, 
                    1, 
                    D3D11_SDK_VERSION, 
                    &sd, 
                    &g_pSwapChain, 
                    &g_pd3dDevice, 
                    &FeatureLevel,
                    &g_pImmediateContext )))
    {
        return hr;
    }
```



Sie müssen den API-Befehl mit dem Verweis Treibertyp aus der [**D3D \_ Driver \_ Type**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) -Enumeration bereitstellen. Nachdem die Methode erfolgreich ausgeführt wurde, gibt Sie eine Austausch Ketten Schnittstelle, eine Geräteschnittstelle, einen Zeiger auf die Featureebene, die vom Treiber erteilt wurde, und eine unmittelbare Kontext Schnittstelle zurück.

Informationen zu Einschränkungen bei der Erstellung eines Referenz Geräts auf bestimmten featureebenen finden Sie unter [Einschränkungen beim Erstellen von Warp-und Referenz Geräten](overviews-direct3d-11-devices-limitations.md). [Verwendung von Direct3D 11](how-to-use-direct3d-11.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Geräte](overviews-direct3d-11-devices.md)
</dt> <dt>

[Verwendung von Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




