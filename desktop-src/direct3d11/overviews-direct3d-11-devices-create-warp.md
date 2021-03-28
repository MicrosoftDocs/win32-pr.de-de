---
title: Erstellen eines Warp-Geräts
description: In diesem Thema wird gezeigt, wie ein Warp-Gerät erstellt wird, das einen hoch Geschwindigkeits Software-Rasterizer implementiert.
ms.assetid: 6daf661e-bc24-4b90-83a7-031acb57cf87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deda409971d22f46132a1cb9b008d3dd1eb7c407
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993486"
---
# <a name="how-to-create-a-warp-device"></a>Vorgehensweise: Erstellen eines Warp-Geräts

In diesem Thema wird gezeigt, wie ein Warp-Gerät erstellt wird, das einen hoch Geschwindigkeits Software-Rasterizer implementiert. Zum Erstellen eines Warp-Geräts geben Sie einfach an, dass das Gerät, das Sie erstellen, einen Warp-Treiber verwendet. In diesem Beispiel werden gleichzeitig ein Gerät und eine SwapChain erstellt.

**So erstellen Sie ein Warp-Gerät**

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

    

2.  Fordern Sie eine Funktionsebene an, die die Features implementiert, die Ihre Anwendung benötigt. Ein Warp-Gerät kann für featureebenen erfolgreich erstellt werden **D3D \_ Featureebene \_ \_ 9 \_ 1** bis **D3D \_ Funktions \_ Ebene \_ 10 \_ 1** und ab Windows 8 für alle featureebenen.

    ```
        D3D_FEATURE_LEVEL FeatureLevels = D3D_FEATURE_LEVEL_10_1;
    ```

    

    Weitere Informationen zu featureebenen finden Sie in der Enumeration der [**D3D- \_ Funktions \_ Ebene**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) .

3.  Erstellen Sie das Gerät durch Aufrufen von [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).


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



Sie müssen den API-Befehl mit dem Warp-Treibertyp aus der [**D3D \_ Driver \_ Type**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) -Enumeration bereitstellen. Nachdem die Methode erfolgreich ausgeführt wurde, gibt Sie eine Austausch Ketten Schnittstelle, eine Geräteschnittstelle, einen Zeiger auf die Featureebene, die vom Treiber erteilt wurde, und eine unmittelbare Kontext Schnittstelle zurück.

Informationen zu Einschränkungen bei der Erstellung eines Warp-Geräts auf bestimmten featureebenen finden Sie unter [Einschränkungen beim Erstellen von Warp-und Referenz Geräten](overviews-direct3d-11-devices-limitations.md).

## <a name="new-for-windows-8"></a>Neu für Windows 8

Wenn der primäre Anzeige Adapter eines Computers der "Microsoft Basic Display Adapter" (Warp-Adapter) ist, verfügt dieser Computer auch über einen zweiten Adapter. Bei diesem zweiten Adapter handelt es sich um das reine Rendering-Gerät ohne Anzeige Ausgaben. Weitere Informationen zum reinen Rendering-Gerät finden Sie unter [neue Informationen in Windows 8 zum Auflisten von Adaptern](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Geräte](overviews-direct3d-11-devices.md)
</dt> <dt>

[Verwendung von Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 