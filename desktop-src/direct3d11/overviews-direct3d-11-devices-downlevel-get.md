---
title: Vorgehensweise beim erhalten der Geräte Funktionsebene
description: In diesem Thema wird gezeigt, wie Sie die höchste von einem Gerät unterstützte Funktionsebene erhalten.
ms.assetid: 5eb7dd5b-3be3-4b7f-bcc7-20027fdfe6b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e587ad488a84641a92f0058d201014030e3467e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856700"
---
# <a name="how-to-get-the-device-feature-level"></a>Gewusst wie: erhalten der Geräte Funktionsebene

In diesem Thema wird gezeigt, wie Sie die höchste von einem [Gerät](overviews-direct3d-11-devices-intro.md)unterstützte [Funktionsebene](overviews-direct3d-11-devices-downlevel-intro.md) erhalten. Direct3D 11-Geräte unterstützen einen festgelegten Satz von featureebenen, die in der [**D3D- \_ Funktions \_ Ebene**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) -Enumeration definiert sind. Wenn Sie die höchste von einem Gerät unterstützte [Funktionsebene](overviews-direct3d-11-devices-downlevel-intro.md) kennen, können Sie Codepfade ausführen, die für dieses Gerät geeignet sind.

**So erhalten Sie die Featureebene des Geräts**

1.  Aufrufen der [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) -Funktion oder der [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) -Funktionen beim Angeben von **null** für den *ppdevice* -Parameter. Sie können dies vor der Erstellung des Geräts durchführen.

    \- oder -

    Aufrufen von [**ID3D11Device:: getfeaturelevel**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getfeaturelevel) nach der Erstellung des Geräts.

2.  Überprüfen Sie den Wert der zurückgegebenen [**D3D- \_ Merkmals \_ Ebene**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) -Enumeration aus dem letzten Schritt, um die unterstützte Funktionsebene zu bestimmen.

Im folgenden Codebeispiel wird veranschaulicht, wie die höchste unterstützte Funktionsebene durch Aufrufen der [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) -Funktion bestimmt wird. **D3D11CreateDevice** speichert die höchste unterstützte Funktionsebene in der featurelevel-Variablen. Mit diesem Code können Sie den Wert des enumerierten Typs der [**D3D- \_ Funktions \_ Ebene**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) untersuchen, der von **D3D11CreateDevice** zurückgegeben wird. Beachten Sie, dass dieser Code alle Funktionsebenen explizit auflistet (für Direct3D 11,1 und Direct3D 11,2).

> [!Note]  
> Wenn die Direct3D 11,1-Laufzeit auf dem Computer vorhanden ist und *pfeaturelevels* auf **null** festgelegt ist, erstellt diese Funktion kein Gerät der [**D3D- \_ Funktions \_ Ebene \_ 11 \_ 1**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) . Zum Erstellen eines Geräts der **D3D- \_ Funktions \_ Ebene \_ 11 \_ 1** müssen Sie explizit ein **D3D \_ Feature \_ Level** -Array bereitstellen, das **D3D-Funktionsebene \_ \_ \_ 11 \_ 1** umfasst. Wenn Sie auf einem Computer, auf dem die Direct3D 11,1-Laufzeit nicht installiert ist, ein **D3D \_ Feature \_ Level** -Array bereitstellen, das D3D-Funktions **\_ \_ Ebene \_ 11 \_ 1** enthält, schlägt diese Funktion mit E \_ invalidArg sofort fehl.

 


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



Der [Verweis Bereich 10level9](d3d11-graphics-reference-10level9.md) listet die Unterschiede zwischen der Art und Weise, wie sich verschiedene [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) -und [**Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) -Methoden auf verschiedenen 10 Level9-featureebenen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D 11 auf downlevelhardware](overviews-direct3d-11-devices-downlevel.md)
</dt> <dt>

[Verwendung von Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




