---
description: Um auf dem Bildschirm zu verfassen oder Gleit Komma Vorgänge auszuführen, müssen Sie im richtigen Farbraum arbeiten.
ms.assetid: 1DD8E2D3-430F-4EE4-9C41-78736C904920
title: Daten für den Farbraum werden umgerechnet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91b5dbec2f826c40d5274cbddb3b54d1cdd9f695
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745936"
---
# <a name="converting-data-for-the-color-space"></a><span data-ttu-id="c4140-103">Daten für den Farbraum werden umgerechnet</span><span class="sxs-lookup"><span data-stu-id="c4140-103">Converting data for the color space</span></span>

<span data-ttu-id="c4140-104">Um auf dem Bildschirm zu verfassen oder Gleit Komma Vorgänge auszuführen, müssen Sie im richtigen Farbraum arbeiten.</span><span class="sxs-lookup"><span data-stu-id="c4140-104">To compose to the screen or perform floating-point operations, you need to work in the correct color space.</span></span> <span data-ttu-id="c4140-105">Es wird empfohlen, Gleit Komma Operationen in einem linearen Farbraum auszuführen.</span><span class="sxs-lookup"><span data-stu-id="c4140-105">We recommend that you perform floating point operations in a linear color space.</span></span> <span data-ttu-id="c4140-106">Konvertieren Sie dann die Daten in Standard-RGB-Daten (sRGB, Gamma 2,2-korrigiert), um die Bilder auf dem Bildschirm darzustellen.</span><span class="sxs-lookup"><span data-stu-id="c4140-106">Then, to present your images to the screen, convert the data to standard RGB data (sRGB, gamma 2.2-corrected) color space.</span></span> <span data-ttu-id="c4140-107">Die Darstellung des Bildschirms im sRGB-Farbraum ist wichtig für die Farbgenauigkeit.</span><span class="sxs-lookup"><span data-stu-id="c4140-107">Presenting to the screen in sRGB color space is important for color accuracy.</span></span> <span data-ttu-id="c4140-108">Wenn Bilder nicht Gamma 2,2-korrigiert sind, weisen Sie zu viele Bits oder zu viel Bandbreite zu, um zu kennzeichnet, dass Benutzer nicht unterscheiden können, und zu wenige Bits oder Bandbreite, um Schatten Werte zu verwenden, die von den Personen abhängig sind, und somit mehr Bits oder Bandbreite benötigen, um dieselbe visuelle Qualität beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="c4140-108">If images are not gamma 2.2-corrected, they allocate too many bits or too much bandwidth to highlights that people can't differentiate, and too few bits or bandwidth to shadow values that people are sensitive to, and so would require more bits or bandwidth to maintain the same visual quality.</span></span> <span data-ttu-id="c4140-109">Stellen Sie daher Bilder auf dem Bildschirm dar, die Gamma 2,2-korrigiert sind, um die beste Farbgenauigkeit sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="c4140-109">Therefore, to ensure the best color accuracy, present images to the screen that are gamma 2.2-corrected.</span></span>

-   [<span data-ttu-id="c4140-110">Farbgenauigkeit</span><span class="sxs-lookup"><span data-stu-id="c4140-110">Color accuracy</span></span>](#color-accuracy)
-   [<span data-ttu-id="c4140-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c4140-111">Related topics</span></span>](#related-topics)

## <a name="color-accuracy"></a><span data-ttu-id="c4140-112">Farbgenauigkeit</span><span class="sxs-lookup"><span data-stu-id="c4140-112">Color accuracy</span></span>

<span data-ttu-id="c4140-113">Für die Darstellung enthalten Anzeige Formate mit ganzzahligen Werten (z. b. [**DXGI- \_ Format \_ B8G8R8A8 \_ unorm \_ sRGB**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), [**DXGI \_ Format \_ R10G10B10 \_ XR \_ Bias \_ a2 \_ unorm**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)usw.) immer sRGB-Daten, die von Gamma korrigiert wurden.</span><span class="sxs-lookup"><span data-stu-id="c4140-113">For presentation, integer-valued display formats (such as [**DXGI\_FORMAT\_B8G8R8A8\_UNORM\_SRGB**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), [**DXGI\_FORMAT\_R10G10B10\_XR\_BIAS\_A2\_UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), and so on) always contain sRGB gamma-corrected data.</span></span> <span data-ttu-id="c4140-114">Gleit Komma Wert-Anzeige Formate (derzeit nur [**DXGI- \_ Format \_ R16G16B16A16 \_ float**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)) enthalten Daten mit linearen Werten.</span><span class="sxs-lookup"><span data-stu-id="c4140-114">Float-valued display formats (currently only [**DXGI\_FORMAT\_R16G16B16A16\_FLOAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)) contain linear-valued data.</span></span>

<span data-ttu-id="c4140-115">Der \_ sRGB- [formatmodifizierer](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) gibt dem Betriebssystem an, dass die APP sRGB-Daten auf dem Bildschirm platzieren soll.</span><span class="sxs-lookup"><span data-stu-id="c4140-115">The \_SRGB [format modifier](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) indicates to the operating system to help the app place sRGB data on the screen.</span></span> <span data-ttu-id="c4140-116">Die APP muss sRGB-Daten immer in Back-Puffer mit ganzzahligen Werten platzieren, um die sRGB-Daten auf dem Bildschirm darzustellen, auch wenn die Daten nicht über diesen formatmodifizierer im Format Namen verfügen.</span><span class="sxs-lookup"><span data-stu-id="c4140-116">The app must always place sRGB data into back buffers with integer-valued formats to present the sRGB data to the screen, even if the data doesn't have this format modifier in its format name.</span></span> <span data-ttu-id="c4140-117">Eine komplette Liste der Formate zum Anzeigen von Scans:</span><span class="sxs-lookup"><span data-stu-id="c4140-117">For a complete list of display scan-out formats:</span></span>

-   [<span data-ttu-id="c4140-118">DXGI-Format Unterstützung für Direct3D Featureebene 12,1 Hardware</span><span class="sxs-lookup"><span data-stu-id="c4140-118">DXGI Format Support for Direct3D Feature Level 12.1 Hardware</span></span>](hardware-support-for-direct3d-12-1-formats.md)
-   [<span data-ttu-id="c4140-119">DXGI-Format Unterstützung für Direct3D Featureebene 12,0 Hardware</span><span class="sxs-lookup"><span data-stu-id="c4140-119">DXGI Format Support for Direct3D Feature Level 12.0 Hardware</span></span>](hardware-support-for-direct3d-12-0-formats.md)
-   [<span data-ttu-id="c4140-120">DXGI-Format Unterstützung für Direct3D Featureebene 11,1 Hardware</span><span class="sxs-lookup"><span data-stu-id="c4140-120">DXGI Format Support for Direct3D Feature Level 11.1 Hardware</span></span>](format-support-for-direct3d-11-1-feature-level-hardware.md)
-   [<span data-ttu-id="c4140-121">DXGI-Format Unterstützung für Direct3D Featureebene 11,0 Hardware</span><span class="sxs-lookup"><span data-stu-id="c4140-121">DXGI Format Support for Direct3D Feature Level 11.0 Hardware</span></span>](format-support-for-direct3d-11-0-feature-level-hardware.md)
-   <span data-ttu-id="c4140-122">[Hardware Unterstützung für Direct3D 10level9-Formate](/previous-versions//ff471324(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c4140-122">[Hardware Support for Direct3D 10Level9 Formats](/previous-versions//ff471324(v=vs.85))</span></span>
-   <span data-ttu-id="c4140-123">[Hardware Unterstützung für Direct3D 10,1-Formate](/previous-versions//cc627091(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c4140-123">[Hardware Support for Direct3D 10.1 Formats](/previous-versions//cc627091(v=vs.85))</span></span>
-   <span data-ttu-id="c4140-124">[Hardware Unterstützung für Direct3D 10-Formate](/previous-versions//cc627090(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c4140-124">[Hardware Support for Direct3D 10 Formats](/previous-versions//cc627090(v=vs.85))</span></span>

<span data-ttu-id="c4140-125">Wenn Sie Gleit Komma Ausgabewerte aus dem Pixelshader in **renderzielsichten (rendertargetview** s) mit dem \_ sRGB- [formatmodifizierer](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) schreiben, der an die [Pipeline](/windows/desktop/direct3d11/overviews-direct3d-11-graphics-pipeline)gebunden ist, konvertieren Sie Sie in den in Gamma 2,2 korrigierten Farbraum.</span><span class="sxs-lookup"><span data-stu-id="c4140-125">When you write floating-point output values from the pixel shader into render-target views (**RenderTargetView** s) with the \_SRGB [format modifier](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) that are bound to the [pipeline](/windows/desktop/direct3d11/overviews-direct3d-11-graphics-pipeline), you convert them to gamma 2.2-corrected color space.</span></span> <span data-ttu-id="c4140-126">Ebenso, wenn Shader-Resource-Sichten (**shaderresourceview** s) mit dem \_ sRGB-formatmodifizierer an die Pipeline gebunden sind, konvertieren Sie die Werte aus dem Gamma 2,2-korrigierten Farbraum in den linearen Farbraum, wenn Sie Sie aus den **shaderresourceview** s lesen.</span><span class="sxs-lookup"><span data-stu-id="c4140-126">Similarly, when shader-resource views (**ShaderResourceView** s) with the \_SRGB format modifier are bound to the pipeline, you convert the values from gamma 2.2-corrected color space to linear color space when you read them from the **ShaderResourceView** s.</span></span> <span data-ttu-id="c4140-127">Der Shader kann dann Vorgänge für Sie ausführen.</span><span class="sxs-lookup"><span data-stu-id="c4140-127">The shader can then perform operations on them.</span></span>

<span data-ttu-id="c4140-128">Verwenden Sie z. b. Code, der diesem ähnelt, um Gleit Komma-Ausgabewerte aus einem Shader in ein **rendertargetview** -Format zu schreiben:</span><span class="sxs-lookup"><span data-stu-id="c4140-128">For example, use code similar to this to write floating-point output values from a shader into a **RenderTargetView** format:</span></span>


```
struct PSOut
{
    float4 color : SV_Target;
};

PSOut S( PSIn input )
{
    PSOut output;
    output.color = float4( 1.0, 0.0, 0.0, 1.0 );
    return output;
}
```



<span data-ttu-id="c4140-129">Wenn die-Routine des s zurückgibt, werden die Gleit Komma Werte (1, 0, 0, 1) in das **rendertargetview** -Format konvertiert.</span><span class="sxs-lookup"><span data-stu-id="c4140-129">When the 'S' routine returns, the floating point (1, 0, 0, 1) values are converted to the **RenderTargetView** format.</span></span> <span data-ttu-id="c4140-130">Wenn Sie dann der \_ **rendertargetview** den sRGB- [formatmodifizierer](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) zuweisen, erfolgt die Gamma Konvertierung.</span><span class="sxs-lookup"><span data-stu-id="c4140-130">Then, if you assign the \_SRGB [format modifier](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) to the **RenderTargetView**, the gamma conversion occurs.</span></span>

<span data-ttu-id="c4140-131">Diese Schritte müssen ausgeführt werden, um sicherzustellen, dass der auf dem Bildschirm angezeigte Inhalt über die beste Farbgenauigkeit verfügt.</span><span class="sxs-lookup"><span data-stu-id="c4140-131">These are steps to follow to ensure that the content that is displayed on the screen has the best color accuracy.</span></span>

<span data-ttu-id="c4140-132">**So sorgen Sie für eine Farbgenauigkeit in der Pipeline**</span><span class="sxs-lookup"><span data-stu-id="c4140-132">**To ensure color accuracy in the pipeline**</span></span>

1.  <span data-ttu-id="c4140-133">Wenn eine Textur über sRGB-Inhalt verfügt, stellen Sie sicher, dass **shaderresourceview** den \_ sRGB- [formatmodifizierer](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) aufweist, sodass Sie den Textur Inhalt von Gamma 2,2-korrigierter Farbraum in den linearen Farbraum konvertieren, wenn Sie aus der **shaderresourceview** in den Shader lesen.</span><span class="sxs-lookup"><span data-stu-id="c4140-133">If a texture has sRGB content, ensure the **ShaderResourceView** has the \_SRGB [format modifier](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) so when you read from the **ShaderResourceView** into the shader, you convert the texture content from gamma 2.2-corrected color space to linear color space.</span></span>
2.  <span data-ttu-id="c4140-134">Stellen Sie sicher, dass **rendertargetview** auch den \_ sRGB- [formatmodifizierer](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) aufweist, damit die Shader-Ausgabewerte Gamma konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="c4140-134">Ensure the **RenderTargetView** also has the \_SRGB [format modifier](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) so the shader output values are gamma converted.</span></span>

<span data-ttu-id="c4140-135">Wenn Sie die obigen Schritte ausführen und die [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) -Methode aufruft, hat der auf dem Bildschirm angezeigte Inhalt die beste Farbgenauigkeit.</span><span class="sxs-lookup"><span data-stu-id="c4140-135">If you follow the preceding steps, when you call the [**IDXGISwapChain1::Present1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) method, the content that is displayed on the screen has the best color accuracy.</span></span>

<span data-ttu-id="c4140-136">Mit der [**ID3D11Device:: samaterendertargetview**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createrendertargetview) -Methode können Sie **\_ \_ \* \_ sRGB-Sichten im DXGI-Format** auf Back Puffern aus einer Swapkette erstellen, die Sie nur mit dem **\_ \_ \* \_ unorm-Format DXGI-Format** erstellen.</span><span class="sxs-lookup"><span data-stu-id="c4140-136">You can use the [**ID3D11Device::CreateRenderTargetView**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createrendertargetview) method to create **DXGI\_FORMAT\_\*\_SRGB** views on back buffers from a swap chain that you create only with a **DXGI\_FORMAT\_\*\_UNORM** format.</span></span> <span data-ttu-id="c4140-137">Dies ist eine besondere Ausnahme von der Regel zum Erstellen von renderzielsichten, die besagt, dass Sie ein anderes Format mit **ID3D11Device:: ":: angetview** " verwenden können, nur wenn Sie die Ressource erstellt haben, die Sie mit **\_ \_ \* \_ typlosen DXGI-Format** anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="c4140-137">This is a special exception to the rule for creating render-target views, which states that you can use a different format with **ID3D11Device::CreateRenderTargetView** only if you created the resource that you want to view with **DXGI\_FORMAT\_\*\_TYPELESS**.</span></span>

<span data-ttu-id="c4140-138">Weitere Informationen zu Regeln für das Konvertieren von Daten finden Sie unter [Daten Konvertierungsregeln](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-data-conversion).</span><span class="sxs-lookup"><span data-stu-id="c4140-138">For more info about rules for converting data, see [Data Conversion Rules](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-data-conversion).</span></span>

<span data-ttu-id="c4140-139">Informationen zum gleichzeitigen Lesen aus einer Textur und zum Schreiben in eine Textur finden Sie unter [entpacken und Verpacken des DXGI- \_ Formats für In-Place Bildbearbeitung](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-unpacking-packing-dxgi-format).</span><span class="sxs-lookup"><span data-stu-id="c4140-139">For info about how to simultaneously both read from and write to a texture, see [Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-unpacking-packing-dxgi-format).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c4140-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c4140-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4140-141">Verbessern der Präsentation mit dem Flip-Modell, den geänderten Rechtecke und den Bereichen</span><span class="sxs-lookup"><span data-stu-id="c4140-141">Enhancing presentation with the flip model, dirty rectangles, and scrolled areas</span></span>](dxgi-1-2-presentation-improvements.md)
</dt> </dl>

 

 
