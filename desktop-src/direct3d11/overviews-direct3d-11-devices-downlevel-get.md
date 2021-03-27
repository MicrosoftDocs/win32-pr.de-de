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
# <a name="how-to-get-the-device-feature-level"></a><span data-ttu-id="789f7-103">Gewusst wie: erhalten der Geräte Funktionsebene</span><span class="sxs-lookup"><span data-stu-id="789f7-103">How To: Get the Device Feature Level</span></span>

<span data-ttu-id="789f7-104">In diesem Thema wird gezeigt, wie Sie die höchste von einem [Gerät](overviews-direct3d-11-devices-intro.md)unterstützte [Funktionsebene](overviews-direct3d-11-devices-downlevel-intro.md) erhalten.</span><span class="sxs-lookup"><span data-stu-id="789f7-104">This topics shows how to get the highest [feature level](overviews-direct3d-11-devices-downlevel-intro.md) supported by a [device](overviews-direct3d-11-devices-intro.md).</span></span> <span data-ttu-id="789f7-105">Direct3D 11-Geräte unterstützen einen festgelegten Satz von featureebenen, die in der [**D3D- \_ Funktions \_ Ebene**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) -Enumeration definiert sind.</span><span class="sxs-lookup"><span data-stu-id="789f7-105">Direct3D 11 devices support a fixed set of feature levels that are defined in the [**D3D\_FEATURE\_LEVEL**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) enumeration.</span></span> <span data-ttu-id="789f7-106">Wenn Sie die höchste von einem Gerät unterstützte [Funktionsebene](overviews-direct3d-11-devices-downlevel-intro.md) kennen, können Sie Codepfade ausführen, die für dieses Gerät geeignet sind.</span><span class="sxs-lookup"><span data-stu-id="789f7-106">When you know the highest [feature level](overviews-direct3d-11-devices-downlevel-intro.md) supported by a device, you can run code paths that are appropriate for that device.</span></span>

<span data-ttu-id="789f7-107">**So erhalten Sie die Featureebene des Geräts**</span><span class="sxs-lookup"><span data-stu-id="789f7-107">**To get the device feature level**</span></span>

1.  <span data-ttu-id="789f7-108">Aufrufen der [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) -Funktion oder der [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) -Funktionen beim Angeben von **null** für den *ppdevice* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="789f7-108">Call either the [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) function or the [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) functions while specifying **NULL** for the *ppDevice* parameter.</span></span> <span data-ttu-id="789f7-109">Sie können dies vor der Erstellung des Geräts durchführen.</span><span class="sxs-lookup"><span data-stu-id="789f7-109">You can do this before device creation.</span></span>

    <span data-ttu-id="789f7-110">\- oder -</span><span class="sxs-lookup"><span data-stu-id="789f7-110">\- or -</span></span>

    <span data-ttu-id="789f7-111">Aufrufen von [**ID3D11Device:: getfeaturelevel**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getfeaturelevel) nach der Erstellung des Geräts.</span><span class="sxs-lookup"><span data-stu-id="789f7-111">Call [**ID3D11Device::GetFeatureLevel**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getfeaturelevel) after device creation.</span></span>

2.  <span data-ttu-id="789f7-112">Überprüfen Sie den Wert der zurückgegebenen [**D3D- \_ Merkmals \_ Ebene**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) -Enumeration aus dem letzten Schritt, um die unterstützte Funktionsebene zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="789f7-112">Examine the value of the returned [**D3D\_FEATURE\_LEVEL**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) enumeration from the last step to determine the supported feature level.</span></span>

<span data-ttu-id="789f7-113">Im folgenden Codebeispiel wird veranschaulicht, wie die höchste unterstützte Funktionsebene durch Aufrufen der [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) -Funktion bestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="789f7-113">The following code example demonstrates how to determine the highest supported feature level by calling the [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) function.</span></span> <span data-ttu-id="789f7-114">**D3D11CreateDevice** speichert die höchste unterstützte Funktionsebene in der featurelevel-Variablen.</span><span class="sxs-lookup"><span data-stu-id="789f7-114">**D3D11CreateDevice** stores the highest supported feature level in the FeatureLevel variable.</span></span> <span data-ttu-id="789f7-115">Mit diesem Code können Sie den Wert des enumerierten Typs der [**D3D- \_ Funktions \_ Ebene**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) untersuchen, der von **D3D11CreateDevice** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="789f7-115">You can use this code to examine the value of the [**D3D\_FEATURE\_LEVEL**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) enumerated type that **D3D11CreateDevice** returns.</span></span> <span data-ttu-id="789f7-116">Beachten Sie, dass dieser Code alle Funktionsebenen explizit auflistet (für Direct3D 11,1 und Direct3D 11,2).</span><span class="sxs-lookup"><span data-stu-id="789f7-116">Note that this code lists all feature levels explicitly (for Direct3D 11.1 and Direct3D 11.2).</span></span>

> [!Note]  
> <span data-ttu-id="789f7-117">Wenn die Direct3D 11,1-Laufzeit auf dem Computer vorhanden ist und *pfeaturelevels* auf **null** festgelegt ist, erstellt diese Funktion kein Gerät der [**D3D- \_ Funktions \_ Ebene \_ 11 \_ 1**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) .</span><span class="sxs-lookup"><span data-stu-id="789f7-117">If the Direct3D 11.1 runtime is present on the computer and *pFeatureLevels* is set to **NULL**, this function won't create a [**D3D\_FEATURE\_LEVEL\_11\_1**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) device.</span></span> <span data-ttu-id="789f7-118">Zum Erstellen eines Geräts der **D3D- \_ Funktions \_ Ebene \_ 11 \_ 1** müssen Sie explizit ein **D3D \_ Feature \_ Level** -Array bereitstellen, das **D3D-Funktionsebene \_ \_ \_ 11 \_ 1** umfasst.</span><span class="sxs-lookup"><span data-stu-id="789f7-118">To create a **D3D\_FEATURE\_LEVEL\_11\_1** device, you must explicitly provide a **D3D\_FEATURE\_LEVEL** array that includes **D3D\_FEATURE\_LEVEL\_11\_1**.</span></span> <span data-ttu-id="789f7-119">Wenn Sie auf einem Computer, auf dem die Direct3D 11,1-Laufzeit nicht installiert ist, ein **D3D \_ Feature \_ Level** -Array bereitstellen, das D3D-Funktions **\_ \_ Ebene \_ 11 \_ 1** enthält, schlägt diese Funktion mit E \_ invalidArg sofort fehl.</span><span class="sxs-lookup"><span data-stu-id="789f7-119">If you provide a **D3D\_FEATURE\_LEVEL** array that contains **D3D\_FEATURE\_LEVEL\_11\_1** on a computer that doesn't have the Direct3D 11.1 runtime installed, this function immediately fails with E\_INVALIDARG.</span></span>

 


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



<span data-ttu-id="789f7-120">Der [Verweis Bereich 10level9](d3d11-graphics-reference-10level9.md) listet die Unterschiede zwischen der Art und Weise, wie sich verschiedene [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) -und [**Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) -Methoden auf verschiedenen 10 Level9-featureebenen</span><span class="sxs-lookup"><span data-stu-id="789f7-120">The [10Level9 Reference](d3d11-graphics-reference-10level9.md) section lists the differences between how various [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) and [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) methods behave at various 10Level9 feature levels.</span></span>

## <a name="related-topics"></a><span data-ttu-id="789f7-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="789f7-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="789f7-122">Direct3D 11 auf downlevelhardware</span><span class="sxs-lookup"><span data-stu-id="789f7-122">Direct3D 11 on Downlevel Hardware</span></span>](overviews-direct3d-11-devices-downlevel.md)
</dt> <dt>

[<span data-ttu-id="789f7-123">Verwendung von Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="789f7-123">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




