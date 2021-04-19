---
description: Direct3D bietet die folgenden Funktionen zum Bestimmen der Hardwareunterstützung.
ms.assetid: 63afa799-2c2c-432c-993e-dca8f7433d59
title: Bestimmen der Hardware Unterstützung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc4fbc04343ede671d009054ac3782bbf2563109
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106338860"
---
# <a name="determining-hardware-support-direct3d-9"></a><span data-ttu-id="0b801-103">Bestimmen der Hardware Unterstützung (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0b801-103">Determining Hardware Support (Direct3D 9)</span></span>

<span data-ttu-id="0b801-104">Direct3D bietet die folgenden Funktionen zum Bestimmen der Hardwareunterstützung.</span><span class="sxs-lookup"><span data-stu-id="0b801-104">Direct3D provides the following functions to determine hardware support.</span></span>

-   [<span data-ttu-id="0b801-105">**IDirect3D9:: CheckDeviceFormat**</span><span class="sxs-lookup"><span data-stu-id="0b801-105">**IDirect3D9::CheckDeviceFormat**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat)

    <span data-ttu-id="0b801-106">Wird verwendet, um zu überprüfen, ob ein Oberflächen Format als Textur verwendet werden kann, ob ein Oberflächen Format als Textur-und Renderziel verwendet werden kann oder ob ein Oberflächen Format als tiefen Schablone-Puffer verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="0b801-106">Used to verify whether a surface format can be used as a texture, whether a surface format can be used as a texture and a render target, or whether a surface format can be used as a depth-stencil buffer.</span></span> <span data-ttu-id="0b801-107">Außerdem wird diese Methode verwendet, um die Unterstützung für tiefe Puffer Formate und die Unterstützung für die Unterstützung von tiefen Schablonen Puffer zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="0b801-107">In addition, this method is used to verify depth buffer format support and depth-stencil buffer format support.</span></span>

-   [<span data-ttu-id="0b801-108">**IDirect3D9:: checkabvicetype**</span><span class="sxs-lookup"><span data-stu-id="0b801-108">**IDirect3D9::CheckDeviceType**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype)

    <span data-ttu-id="0b801-109">Wird verwendet, um zu überprüfen, ob das Gerät eine Hardwarebeschleunigung durchführen kann, ob ein Gerät eine Swapkette für die Präsentation erstellen oder ob ein Gerät in das aktuelle Anzeige Format renderfähig ist.</span><span class="sxs-lookup"><span data-stu-id="0b801-109">Used to verify a device's ability to perform hardware acceleration, a device's ability to build a swap chain for presentation, or a device's ability to render to the current display format.</span></span>

-   [<span data-ttu-id="0b801-110">**IDirect3D9:: checkdepthstencilmatch**</span><span class="sxs-lookup"><span data-stu-id="0b801-110">**IDirect3D9::CheckDepthStencilMatch**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdepthstencilmatch)

    <span data-ttu-id="0b801-111">Wird verwendet, um zu überprüfen, ob ein tiefen Schablone-Puffer Format mit einem renderzielformat kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="0b801-111">Used to verify whether a depth-stencil buffer format is compatible with a render-target format.</span></span> <span data-ttu-id="0b801-112">Beachten Sie, dass die Anwendung vor dem Aufruf dieser Methode [**IDirect3D9:: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) sowohl für das tiefen-Schablone-als auch das renderzielformat aufrufen sollte.</span><span class="sxs-lookup"><span data-stu-id="0b801-112">Note that before calling this method, the application should call [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) on both the depth-stencil and render-target formats.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0b801-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0b801-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b801-114">Direct3D-Geräte</span><span class="sxs-lookup"><span data-stu-id="0b801-114">Direct3D Devices</span></span>](direct3d-devices.md)
</dt> </dl>

 

 
