---
description: C++-Anwendungen können Alpha Tests verwenden, um zu steuern, wann Pixel auf die renderzieloberfläche geschrieben werden.
ms.assetid: 368c3d12-2c8b-43e3-94c3-bccfe6c73e66
title: Alpha Test Status (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 020322ee31bc08352dbb2796ea5e7141d03c77c3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346449"
---
# <a name="alpha-testing-state-direct3d-9"></a><span data-ttu-id="ab17f-103">Alpha Test Status (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="ab17f-103">Alpha Testing State (Direct3D 9)</span></span>

<span data-ttu-id="ab17f-104">C++-Anwendungen können Alpha Tests verwenden, um zu steuern, wann Pixel auf die renderzieloberfläche geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="ab17f-104">C++ applications can use alpha testing to control when pixels are written to the render-target surface.</span></span> <span data-ttu-id="ab17f-105">Wenn Sie den renderzustand [**D3DRS \_ Alpha atestenable**](./d3drenderstatetype.md) verwenden, legt ihre Anwendung das aktuelle Direct3D-Gerät so fest, dass jedes Pixel gemäß einer Alpha-Testfunktion getestet wird.</span><span class="sxs-lookup"><span data-stu-id="ab17f-105">By using the [**D3DRS\_ALPHATESTENABLE**](./d3drenderstatetype.md) render state, your application sets the current Direct3D device so that it tests each pixel according to an alpha test function.</span></span> <span data-ttu-id="ab17f-106">Wenn der Test erfolgreich ist, wird das Pixel auf die-Oberfläche geschrieben.</span><span class="sxs-lookup"><span data-stu-id="ab17f-106">If the test succeeds, the pixel is written to the surface.</span></span> <span data-ttu-id="ab17f-107">Wenn dies nicht der Fall ist, wird das Pixel von Direct3D ignoriert.</span><span class="sxs-lookup"><span data-stu-id="ab17f-107">If it does not, Direct3D ignores the pixel.</span></span> <span data-ttu-id="ab17f-108">Wählen Sie die Alpha-Testfunktion mit dem **D3DRS \_ alphafunc** -gerengerzustand aus.</span><span class="sxs-lookup"><span data-stu-id="ab17f-108">Select the alpha test function with the **D3DRS\_ALPHAFUNC** render state.</span></span> <span data-ttu-id="ab17f-109">Die Anwendung kann einen Referenz-Alpha-Wert für alle Pixel festlegen, mit denen der **D3DRS- \_ Alpha Aref** -Rendering-Zustand verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="ab17f-109">Your application can set a reference alpha value for all pixels to compare against by using the **D3DRS\_ALPHAREF** render state.</span></span>

<span data-ttu-id="ab17f-110">Die häufigste Verwendung für Alpha Tests ist die Verbesserung der Leistung bei der fast transparenten rasterisierung von Objekten.</span><span class="sxs-lookup"><span data-stu-id="ab17f-110">The most common use for alpha testing is to improve performance when rasterizing objects that are nearly transparent.</span></span> <span data-ttu-id="ab17f-111">Wenn die zu ragenden Farbdaten transparenter sind als die Farbe an einem bestimmten Pixel (D3DPCMPCAPS \_ greaterequal), wird das Pixel geschrieben.</span><span class="sxs-lookup"><span data-stu-id="ab17f-111">If the color data being rasterized is more opaque than the color at a given pixel (D3DPCMPCAPS\_GREATEREQUAL), then the pixel is written.</span></span> <span data-ttu-id="ab17f-112">Andernfalls ignoriert der Raster das Pixel vollständig und speichert die Verarbeitung, die zum Mischen der beiden Farben erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="ab17f-112">Otherwise, the rasterizer ignores the pixel altogether, saving the processing required to blend the two colors.</span></span> <span data-ttu-id="ab17f-113">Im folgenden Codebeispiel wird überprüft, ob eine angegebene Vergleichsfunktion unterstützt wird, und wenn dies der Fall ist, werden die Vergleichs Funktionsparameter festgelegt, die zum Verbessern der Leistung beim Rendern</span><span class="sxs-lookup"><span data-stu-id="ab17f-113">The following code example checks if a given comparison function is supported and, if so, it sets the comparison function parameters required to improve performance during rendering.</span></span>


```
// This code example assumes that pCaps is a
// D3DCAPS9 structure that was filled with a 
// previous call to IDirect3D9::GetDeviceCaps.

if (pCaps.AlphaCmpCaps & D3DPCMPCAPS_GREATEREQUAL)
{
    dev->SetRenderState(D3DRS_ALPHAREF, (DWORD)0x00000001);
    dev->SetRenderState(D3DRS_ALPHATESTENABLE, TRUE); 
    dev->SetRenderState(D3DRS_ALPHAFUNC, D3DCMP_GREATEREQUAL);
}

// If the comparison is not supported, render anyway. 
// The only drawback is no performance gain.
```



<span data-ttu-id="ab17f-114">Nicht alle Hardware unterstützt alle Alpha Test Features.</span><span class="sxs-lookup"><span data-stu-id="ab17f-114">Not all hardware supports all alpha-testing features.</span></span> <span data-ttu-id="ab17f-115">Sie können die Gerätefunktionen überprüfen, indem Sie die [**IDirect3D9:: GetDeviceCaps**](/windows/desktop/api) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ab17f-115">You can check the device capabilities by calling the [**IDirect3D9::GetDeviceCaps**](/windows/desktop/api) method.</span></span> <span data-ttu-id="ab17f-116">Überprüfen Sie nach dem Abrufen der Gerätefunktionen den Alpha acmpcaps-Member der zugeordneten [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) -Struktur auf die gewünschte Vergleichsfunktion.</span><span class="sxs-lookup"><span data-stu-id="ab17f-116">After retrieving the device capabilities, check the associated [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure's AlphaCmpCaps member for the desired comparison function.</span></span> <span data-ttu-id="ab17f-117">Wenn das Alpha acmpcaps-Element nur die Funktion "D3DPCMPCAPS \_ Always" oder nur die Funktion "D3DPCMPCAPS Never" enthält \_ , unterstützt der Treiber keine Alpha Tests.</span><span class="sxs-lookup"><span data-stu-id="ab17f-117">If the AlphaCmpCaps member contains only the D3DPCMPCAPS\_ALWAYS capability or only the D3DPCMPCAPS\_NEVER capability, the driver does not support alpha tests.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ab17f-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ab17f-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab17f-119">Rendering-Zustände</span><span class="sxs-lookup"><span data-stu-id="ab17f-119">Render States</span></span>](render-states.md)
</dt> </dl>

 

 
