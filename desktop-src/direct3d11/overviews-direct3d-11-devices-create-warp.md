---
title: Erstellen eines WARP-Geräts
description: In diesem Thema wird gezeigt, wie Sie ein WARP-Gerät erstellen, das einen Softwarerasterizer mit hoher Geschwindigkeit implementiert.
ms.assetid: 6daf661e-bc24-4b90-83a7-031acb57cf87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f78d3e8b5224018fb9f45df2c6eec5ee6f9d88cdd664715a31050eaab4ddd948
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119407800"
---
# <a name="how-to-create-a-warp-device"></a>Vorgehensweise: Erstellen eines WARP-Geräts

In diesem Thema wird gezeigt, wie Sie ein WARP-Gerät erstellen, das einen Softwarerasterizer mit hoher Geschwindigkeit implementiert. Um ein WARP-Gerät zu erstellen, geben Sie einfach an, dass das gerät, das Sie erstellen, einen WARP-Treiber verwendet. In diesem Beispiel werden ein Gerät und eine Austauschkette gleichzeitig erstellt.

**So erstellen Sie ein WARP-Gerät**

1.  Definieren sie anfängliche Parameter für eine Swapkette.
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

    

2.  Fordern Sie eine Featureebene an, die die Features implementiert, die Ihre Anwendung benötigt. Ein WARP-Gerät kann erfolgreich für die Featureebenen **D3D \_ FEATURE \_ LEVEL \_ 9 \_ 1** bis **D3D \_ FEATURE LEVEL \_ \_ 10 \_ 1** erstellt werden und mit Windows 8 für alle Featureebenen beginnen.

    ```
        D3D_FEATURE_LEVEL FeatureLevels = D3D_FEATURE_LEVEL_10_1;
    ```

    

    Weitere Informationen zu Featureebenen finden Sie in der [**D3D \_ FEATURE \_ LEVEL-Enumeration.**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level)

3.  Erstellen Sie das Gerät, indem [**Sie D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain)aufrufen.


```
    HRESULT hr = S_OK;
    if( FAILED (hr = D3D11CreateDeviceAndSwapChain( NULL, 
                    D3D_DRIVER_TYPE_WARP,
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



Sie müssen den API-Aufruf mit dem WARP-Treibertyp aus der [**D3D \_ DRIVER \_ TYPE-Enumeration**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) bereitstellen. Nachdem die Methode erfolgreich ausgeführt wurde, gibt sie eine Austauschkettenschnittstelle, eine Geräteschnittstelle, einen Zeiger auf die vom Treiber gewährte Featureebene und eine direkte Kontextschnittstelle zurück.

Informationen zu Einschränkungen beim Erstellen eines WARP-Geräts auf bestimmten Featureebenen finden Sie unter [Einschränkungen beim Erstellen von WARP- und Referenzgeräten.](overviews-direct3d-11-devices-limitations.md)

## <a name="new-for-windows-8"></a>Neu für Windows 8

Wenn der primäre Anzeigeadapter eines Computers der "Microsoft Basic Display Adapter" (WARP-Adapter) ist, verfügt dieser Computer auch über einen zweiten Adapter. Bei diesem zweiten Adapter handelt es sich um das rein renderbasierte Gerät ohne Anzeigeausgaben. Weitere Informationen zum reinen Rendergerät finden Sie [unter neue Informationen in Windows 8 zum Aufzählen von Adaptern.](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Geräte](overviews-direct3d-11-devices.md)
</dt> <dt>

[Verwenden von Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 