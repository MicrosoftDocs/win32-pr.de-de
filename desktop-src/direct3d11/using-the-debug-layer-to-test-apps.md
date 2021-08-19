---
title: Verwenden der Debugebene zum Debuggen von Apps
description: Hier erfahren Sie, wie Sie die Debugebene aktivieren, und einige der Probleme, die Sie mithilfe der Debugebene verhindern können.
ms.assetid: 3C2B0A12-FB57-4400-BE39-05ED23F552C7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c6ac5492b96c40b4395b2c501b764c646a8edbb06d3a6386a15cbb2534778d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117912734"
---
# <a name="using-the-debug-layer-to-debug-apps"></a>Verwenden der Debugebene zum Debuggen von Apps

Es wird empfohlen, die [Debugebene](overviews-direct3d-11-devices-layers.md) zu verwenden, um Ihre Apps zu debuggen, um sicherzustellen, dass sie von Fehlern und Warnungen bereinigt werden. Die Debugebene unterstützt Sie beim Schreiben von Direct3D-Code. Darüber hinaus kann Ihre Produktivität bei Verwendung der Debugebene gesteigert werden, da Sie sofort die Ursachen für obskure Renderingfehler oder sogar schwarze Bildschirme an der Quelle sehen können. Die Debugebene stellt Warnungen für viele Probleme bereit. Beispielsweise stellt die Debugebene Warnungen für diese Probleme bereit:

-   Vergessen, eine Textur festzulegen, aber aus ihr in Ihrem Pixel-Shader zu lesen
-   Ausgabetiefe, aber keine Begrenzung des Tiefenschablonenzustands
-   Fehler bei der Texturerstellung mit INVALIDARG

Hier erfahren Sie, wie Sie die [Debugebene](overviews-direct3d-11-devices-layers.md) aktivieren, und einige der Probleme, die Sie mithilfe der Debugebene verhindern können.

-   [Aktivieren der Debugebene](#enabling-the-debug-layer)
-   [Verhindern von Fehlern in Ihrer App mit der Debugebene](#preventing-errors-in-your-app-with-the-debug-layer)
    -   [Übergeben Sie keine NULL-Zeiger an Map.](#dont-pass-null-pointers-to-map)
    -   [Beschränken des Felds "Quelle" in Quell- und Zielressourcen](#confine-source-box-within-source-and-destination-resources)
    -   [DiscardResource oder DiscardView nicht löschen](#dont-drop-discardresource-or-discardview)
-   [Zugehörige Themen](#related-topics)

## <a name="enabling-the-debug-layer"></a>Aktivieren der Debugebene

Um die [Debugebene](overviews-direct3d-11-devices-layers.md)zu aktivieren, geben Sie das [**D3D11 \_ CREATE DEVICE \_ \_ DEBUG-Flag**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag) im *Flags-Parameter* an, wenn Sie die [**D3D11CreateDevice-Funktion**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) aufrufen, um das Renderinggerät zu erstellen. Dieser Beispielcode zeigt, wie Sie die Debugebene aktivieren, wenn sich Ihr Microsoft Visual Studio-Projekt in einem Debugbuild befindet:


```C++
        UINT creationFlags = D3D11_CREATE_DEVICE_BGRA_SUPPORT;
#if defined(_DEBUG)
        // If the project is in a debug build, enable the debug layer.
        creationFlags |= D3D11_CREATE_DEVICE_DEBUG;
#endif
        // Define the ordering of feature levels that Direct3D attempts to create.
        D3D_FEATURE_LEVEL featureLevels[] =
        {
            D3D_FEATURE_LEVEL_11_1,
            D3D_FEATURE_LEVEL_11_0,
            D3D_FEATURE_LEVEL_10_1,
            D3D_FEATURE_LEVEL_10_0,
            D3D_FEATURE_LEVEL_9_3,
            D3D_FEATURE_LEVEL_9_1
        };

        ComPtr<ID3D11Device> d3dDevice;
        ComPtr<ID3D11DeviceContext> d3dDeviceContext;
        DX::ThrowIfFailed(
            D3D11CreateDevice(
                nullptr,                    // specify nullptr to use the default adapter
                D3D_DRIVER_TYPE_HARDWARE,
                nullptr,                    // specify nullptr because D3D_DRIVER_TYPE_HARDWARE 
                                            // indicates that this function uses hardware
                creationFlags,              // optionally set debug and Direct2D compatibility flags
                featureLevels,
                ARRAYSIZE(featureLevels),
                D3D11_SDK_VERSION,          // always set this to D3D11_SDK_VERSION
                &d3dDevice,
                nullptr,
                &d3dDeviceContext
                )
            );
```



## <a name="preventing-errors-in-your-app-with-the-debug-layer"></a>Verhindern von Fehlern in Ihrer App mit der Debugebene

Wenn Sie die Direct3D 11-API missbrauchen oder ungültige Parameter übergeben, meldet die Debugausgabe der [Debugebene](overviews-direct3d-11-devices-layers.md) einen Fehler oder eine Warnung. Anschließend können Sie Ihren Fehler beheben. Als Nächstes betrachten wir einige Codierungsprobleme, die dazu führen können, dass nicht definiertes Verhalten oder sogar das Betriebssystem abstürzt. Sie können diese Probleme mithilfe der Debugebene abfangen und verhindern.

### <a name="dont-pass-null-pointers-to-map"></a>Übergeben Sie keine NULL-Zeiger an Map.

Wenn Sie **NULL** an den *pResource-* oder *pMappedResource-Parameter* der [**ID3D11DeviceContext::Map-Methode**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) übergeben, ist das Verhalten von **Map** nicht definiert. Wenn Sie ein Gerät erstellt haben, das nur die [Kernschicht](overviews-direct3d-11-devices-layers.md)unterstützt, **können** ungültige Map-Parameter das Betriebssystem abstürzen. Wenn Sie ein Gerät erstellt haben, das die [Debugebene](overviews-direct3d-11-devices-layers.md)unterstützt, meldet die Debugausgabe einen Fehler bei diesem ungültigen **Map-Aufruf.**

### <a name="confine-source-box-within-source-and-destination-resources"></a>Beschränken des Felds "Quelle" in Quell- und Zielressourcen

Bei einem Aufruf der [**ID3D11DeviceContext::CopySubresourceRegion-Methode**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) muss sich das Quellfeld innerhalb der Quellressource befinden. Mit den Zieloffsets (x, y und z) kann das Quellfeld beim Schreiben in die Zielressource versetzt werden. Die Dimensionen des Quellfelds und der Offsets müssen jedoch innerhalb der Größe der Ressource sein. Wenn Sie versuchen, außerhalb der Zielressource zu kopieren oder ein Quellfeld anzugeben, das größer als die Quellressource ist, ist das Verhalten von **CopySubresourceRegion** nicht definiert. Wenn Sie ein Gerät erstellt haben, das die [Debugebene](overviews-direct3d-11-devices-layers.md)unterstützt, meldet die Debugausgabe einen Fehler bei diesem ungültigen **CopySubresourceRegion-Aufruf.** Ungültige Parameter für **CopySubresourceRegion** verursachen nicht definiertes Verhalten und können zu falschem Rendering, Clipping, keiner Kopie oder sogar zum Entfernen des Renderinggeräts führen.

### <a name="dont-drop-discardresource-or-discardview"></a>DiscardResource oder DiscardView nicht löschen

Die Runtime löscht einen Aufruf von [**ID3D11DeviceContext1::D iscardResource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource) oder [**ID3D11DeviceContext1::D iscardView,**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview) es sei denn, Sie erstellen die Ressource ordnungsgemäß.

Die Ressource, die Sie an [**ID3D11DeviceContext1::D iscardResource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource) übergeben, muss mit [**D3D11 \_ USAGE \_ DEFAULT**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) oder [**D3D11 \_ USAGE \_ DYNAMIC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)erstellt worden sein, andernfalls löscht die Laufzeit den Aufruf von **DiscardResource**.

Die Ressource, die der Ansicht zugrundeliegt, die Sie an [**ID3D11DeviceContext1::D iscardView**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview) übergeben, muss mit [**D3D11 \_ USAGE \_ DEFAULT**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) oder [**D3D11 \_ USAGE \_ DYNAMIC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)erstellt worden sein, andernfalls löscht die Laufzeit den Aufruf von **DiscardView**.

Wenn Sie ein Gerät erstellt haben, das die [Debugebene](overviews-direct3d-11-devices-layers.md)unterstützt, meldet die Debugausgabe einen Fehler in Bezug auf den gelöschten Aufruf.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Softwareebenen](overviews-direct3d-11-devices-layers.md)
</dt> </dl>

 

 




