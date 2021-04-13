---
description: Mehrere Renderziele (MRT) bezieht sich auf die Fähigkeit zum renderingzeichen auf mehreren Oberflächen (siehe IDirect3D9Surface) mit einem einzelnen zeichnen-Befehl.
ms.assetid: ae48c5ce-b7f5-4189-8b04-880836be3fe0
title: Mehrere Renderziele (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bb7aafeedb621e43abb288eb9bbceb17ddb0cc0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482046"
---
# <a name="multiple-render-targets-direct3d-9"></a><span data-ttu-id="07954-103">Mehrere Renderziele (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="07954-103">Multiple Render Targets (Direct3D 9)</span></span>

<span data-ttu-id="07954-104">Mehrere Renderziele (MRT) bezieht sich auf die Fähigkeit zum renderingzeichen auf mehreren Oberflächen (siehe [**IDirect3D9Surface**](/windows/desktop/api)) mit einem einzelnen zeichnen-Befehl.</span><span class="sxs-lookup"><span data-stu-id="07954-104">Multiple Render Targets (MRT) refers to the ability to render to multiple surfaces (see [**IDirect3D9Surface**](/windows/desktop/api)) with a single draw call.</span></span> <span data-ttu-id="07954-105">Diese Oberflächen können unabhängig voneinander erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="07954-105">These surfaces can be created independently of each other.</span></span> <span data-ttu-id="07954-106">Renderziele können mithilfe von [**IDirect3DDevice9:: SetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget)festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="07954-106">Render targets can be set using [**IDirect3DDevice9::SetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget).</span></span>

<span data-ttu-id="07954-107">Mehrere Renderziele weisen die folgenden Einschränkungen auf:</span><span class="sxs-lookup"><span data-stu-id="07954-107">Multiple render targets have the following restrictions:</span></span>

-   <span data-ttu-id="07954-108">Alle gemeinsamen renderzieloberflächen müssen die gleiche Bittiefe aufweisen, können jedoch unterschiedliche Formate aufweisen, es sei denn, das D3DPMISCCAPS \_ mrtindependentbittiefen-Cap ist festgelegt.</span><span class="sxs-lookup"><span data-stu-id="07954-108">All render target surfaces used together must have the same bit depth but can be of different formats, unless the D3DPMISCCAPS\_MRTINDEPENDENTBITDEPTHS cap is set.</span></span>
-   <span data-ttu-id="07954-109">Alle Oberflächen eines multirenderziels sollten dieselbe Breite und Höhe aufweisen.</span><span class="sxs-lookup"><span data-stu-id="07954-109">All surfaces of a multiple render target should have the same width and height.</span></span>
-   <span data-ttu-id="07954-110">Einige Implementierungen können keine Post-Pixel-Shader-Vorgänge für mehrere Renderziele ausführen, wie z. b. "keine Dithering", "Alpha Test", "kein erstellen", "keine Vermischung" und Maskierung, außer dem z-Test und dem Schablone</span><span class="sxs-lookup"><span data-stu-id="07954-110">Some implementations cannot perform post-pixel shader operations on multiple render targets, including: no dithering, alpha test, no fogging, no blending or masking, except the z-test and stencil test.</span></span> <span data-ttu-id="07954-111">Geräte, die Post-Pixel-Shader-Vorgänge unterstützen können, legen das Cap-Bit auf D3DPMISCCAPS \_ mrtpostpixelshaderblending fest.</span><span class="sxs-lookup"><span data-stu-id="07954-111">Devices that can support post-pixel shader operations set the cap bit to D3DPMISCCAPS\_MRTPOSTPIXELSHADERBLENDING.</span></span>

    <span data-ttu-id="07954-112">Wenn das D3DPMISCCAPS \_ mrtpostpixelshaderblending-Cap festgelegt ist, müssen Sie zuerst das [**IDirect3D9:: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) mit der Verwendungs \_ Abfrage \_ postpixelshader- \_ Mischungs Ergebnis für das jeweilige Oberflächen Format überprüfen.</span><span class="sxs-lookup"><span data-stu-id="07954-112">When the D3DPMISCCAPS\_MRTPOSTPIXELSHADERBLENDING cap is set, you must first consult the [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) with the USAGE\_QUERY\_POSTPIXELSHADER\_BLENDING result for the specific surface format.</span></span> <span data-ttu-id="07954-113">Wenn der Wert false ist, sind keine Mischungs Vorgänge nach Pixel-Shader für dieses bestimmte Oberflächen Format verfügbar.</span><span class="sxs-lookup"><span data-stu-id="07954-113">If false, no post-pixel shader blending operations will be available for that specific surface format.</span></span> <span data-ttu-id="07954-114">Wenn der Wert true ist, wird erwartet, dass das Gerät denselben Status auf alle gleichzeitigen Renderziele anwendet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="07954-114">If true, the device is expected to apply the same state to all simultaneous render targets as follows:</span></span>

    -   <span data-ttu-id="07954-115">Alpha Blend: der Farbwert in OCI wird mit dem ITH-Renderziel gemischt.</span><span class="sxs-lookup"><span data-stu-id="07954-115">Alpha blend: The color value in oCi is blended with the ith render target.</span></span>
    -   <span data-ttu-id="07954-116">Alpha-Test: der Vergleich erfolgt mit oC0.</span><span class="sxs-lookup"><span data-stu-id="07954-116">Alpha test: Comparison will happen with oC0.</span></span> <span data-ttu-id="07954-117">Wenn der Vergleich fehlschlägt, wird der Pixel Test für alle Renderziele beendet.</span><span class="sxs-lookup"><span data-stu-id="07954-117">If the comparison fails, the pixel test is terminated for all render targets.</span></span>
    -   <span data-ttu-id="07954-118">Nebel: Renderziel 0 wird gefoppt.</span><span class="sxs-lookup"><span data-stu-id="07954-118">Fog: Render target 0 will get fogged.</span></span> <span data-ttu-id="07954-119">Andere Renderziele sind nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="07954-119">Other render targets are undefined.</span></span> <span data-ttu-id="07954-120">Implementierungen können alle mit dem gleichen Zustand ein Nebel durch die Auswahl treffen.</span><span class="sxs-lookup"><span data-stu-id="07954-120">Implementations can choose to fog them all using the same state.</span></span>
    -   <span data-ttu-id="07954-121">Dithering: nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="07954-121">Dithering: Undefined.</span></span>

-   <span data-ttu-id="07954-122">Es wird kein Antialiasing unterstützt.</span><span class="sxs-lookup"><span data-stu-id="07954-122">No antialiasing is supported.</span></span>
-   <span data-ttu-id="07954-123">Einige Implementierungen wenden nicht die Ausgabe Schreib Maske an (D3DRS \_ colorschreiteenable).</span><span class="sxs-lookup"><span data-stu-id="07954-123">Some of the implementations do not apply the output write mask (D3DRS\_COLORWRITEENABLE).</span></span> <span data-ttu-id="07954-124">Solche, die über unabhängige Farb Schreib Masken verfügen können.</span><span class="sxs-lookup"><span data-stu-id="07954-124">Those that can, have independent color write masks.</span></span> <span data-ttu-id="07954-125">Dies wird mithilfe eines neuen Funktionsbits ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="07954-125">This is expressed using a new capability bit.</span></span> <span data-ttu-id="07954-126">Die Anzahl der verfügbaren unabhängigen Farb Schreib Masken ist gleich der maximalen Anzahl von Elementen, für die das Gerät geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="07954-126">The number of independent color write masks available will be equal to the maximum number of elements the device is capable of.</span></span>

<span data-ttu-id="07954-127">Neue Hardware Obergrenzen:</span><span class="sxs-lookup"><span data-stu-id="07954-127">New hardware caps:</span></span>


```
D3DCAPS9.NumSimultaneousRTs         
// The value is 1 for all hardware except those that  
//   can support this feature. It is never 0.
D3DPMISCCAPS_MRTINDEPENDENTBITDEPTHS - True if the hardware can support it
D3DPMISCCAPS_MRTPOSTPIXELSHADERBLENDING - True if the hardware can support it
```



## <a name="related-topics"></a><span data-ttu-id="07954-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="07954-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07954-129">Pixel Pipeline</span><span class="sxs-lookup"><span data-stu-id="07954-129">Pixel Pipeline</span></span>](pixel-pipeline.md)
</dt> </dl>

 

 
