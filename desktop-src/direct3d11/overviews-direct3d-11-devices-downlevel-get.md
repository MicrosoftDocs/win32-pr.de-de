---
title: Abrufen der Gerätefunktionsebene
description: In diesem Thema wird gezeigt, wie Sie die höchste von einem Gerät unterstützte Featureebene erhalten.
ms.assetid: 5eb7dd5b-3be3-4b7f-bcc7-20027fdfe6b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac21d00aeef8ae6c82ffd9f55a40415b6af1d0a780cc6878d8c30bf453457eb9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119600"
---
# <a name="how-to-get-the-device-feature-level"></a>Vorgehensweise: Abrufen der Gerätefunktionsebene

In diesem Thema wird gezeigt, wie Sie die höchste [Featureebene](overviews-direct3d-11-devices-downlevel-intro.md) erhalten, die von einem [Gerät](overviews-direct3d-11-devices-intro.md)unterstützt wird. Direct3D 11-Geräte unterstützen einen festen Satz von Featureebenen, die in der [**D3D \_ FEATURE \_ LEVEL-Enumeration**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) definiert sind. Wenn Sie die höchste von einem Gerät unterstützte [Featureebene](overviews-direct3d-11-devices-downlevel-intro.md) kennen, können Sie Codepfade ausführen, die für dieses Gerät geeignet sind.

**So erhalten Sie die Gerätefunktionsebene**

1.  Rufen Sie entweder die [**D3D11CreateDevice-Funktion**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) oder die [**D3D11CreateDeviceAndSwapChain-Funktion**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) auf, während Sie **NULL** für den *ppDevice-Parameter* angeben. Sie können dies vor der Geräteerstellung tun.

    \- oder –

    Rufen Sie [**id3D11Device::GetFeatureLevel**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getfeaturelevel) nach der Geräteerstellung auf.

2.  Untersuchen Sie den Wert der zurückgegebenen [**D3D \_ FEATURE \_ LEVEL-Enumeration**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) aus dem letzten Schritt, um die unterstützte Featureebene zu ermitteln.

Im folgenden Codebeispiel wird veranschaulicht, wie die höchste unterstützte Featureebene durch Aufrufen der [**D3D11CreateDevice-Funktion**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) bestimmt wird. **D3D11CreateDevice** speichert die höchste unterstützte Featureebene in der FeatureLevel-Variablen. Sie können diesen Code verwenden, um den Wert des [**D3D \_ FEATURE LEVEL-Enumerationstyps \_**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) zu untersuchen, den **D3D11CreateDevice** zurückgibt. Beachten Sie, dass dieser Code alle Featureebenen explizit auflistet (für Direct3D 11.1 und Direct3D 11.2).

> [!Note]  
> Wenn die Direct3D 11.1-Runtime auf dem Computer vorhanden ist und *pFeatureLevels* auf **NULL** festgelegt ist, erstellt diese Funktion kein [**D3D \_ FEATURE LEVEL \_ \_ 11-Gerät. \_**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) Um ein **D3D \_ FEATURE LEVEL \_ \_ 11 \_ 1-Gerät** zu erstellen, müssen Sie explizit ein **D3D \_ FEATURE \_ LEVEL-Array** bereitstellen, das **D3D \_ FEATURE LEVEL \_ \_ 11 \_ 1** enthält. Wenn Sie ein **D3D \_ FEATURE \_ LEVEL-Array** bereitstellen, das **D3D \_ FEATURE LEVEL \_ \_ \_ 11 1** auf einem Computer enthält, auf dem die Direct3D 11.1-Runtime nicht installiert ist, schlägt diese Funktion sofort mit E \_ INVALIDARG fehl.

 


```C++
HRESULT hr = E_FAIL;
D3D_FEATURE_LEVEL MaxSupportedFeatureLevel = D3D_FEATURE_LEVEL_9_1;
D3D_FEATURE_LEVEL FeatureLevels[] = {
    D3D_FEATURE_LEVEL_11_1,
    D3D_FEATURE_LEVEL_11_0,
    D3D_FEATURE_LEVEL_10_1,
    D3D_FEATURE_LEVEL_10_0,
    D3D_FEATURE_LEVEL_9_3,
    D3D_FEATURE_LEVEL_9_2,
    D3D_FEATURE_LEVEL_9_1
    };

hr = D3D11CreateDevice(
    NULL,
    D3D_DRIVER_TYPE_HARDWARE,
    NULL, 
    0, 
    &FeatureLevels, 
    ARRAYSIZE(FeatureLevels), 
    D3D11_SDK_VERSION, 
    NULL, 
    &MaxSupportedFeatureLevel, 
    NULL 
    );

if(FAILED(hr))
{
    return hr;
}
```



Im Abschnitt [Referenz zu 10Level9](d3d11-graphics-reference-10level9.md) werden die Unterschiede zwischen den verschiedenen [**Methoden ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) und [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) auf verschiedenen 10Level9-Featureebenen aufgelistet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D 11 auf kompatibler Hardware](overviews-direct3d-11-devices-downlevel.md)
</dt> <dt>

[Verwenden von Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




