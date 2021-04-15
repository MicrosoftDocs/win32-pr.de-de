---
title: Verhindern unerwünschter NULL-Pixel-Shader-Srvs
description: In diesem Thema wird erläutert, wie Sie den Treiber umgehen, der NULL-Shader-Ressourcen Sichten (Srvs) empfängt, auch wenn nicht-NULL-Srvs an die Pixel-Shader-Phase gebunden sind.
ms.assetid: c832c199-59b8-4079-a159-45490a2f6a94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bacacf7704cffe12df44b9b0be667632307adb4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104992863"
---
# <a name="preventing-unwanted-null-pixel-shader-srvs"></a><span data-ttu-id="46f01-103">Verhindern unerwünschter NULL-Pixel-Shader-Srvs</span><span class="sxs-lookup"><span data-stu-id="46f01-103">Preventing Unwanted NULL Pixel Shader SRVs</span></span>

<span data-ttu-id="46f01-104">Direct3D 11-Anwendungen, die auf Direct3D 9-Grafikhardware ausgeführt werden, können versehentlich bewirken, dass der Treiber **null** -Shader-Ressourcen Sichten (Srvs) empfängt, auch wenn die Anwendungen nicht-**null** -Srvs an die Pixel-Shader-Stufe binden.</span><span class="sxs-lookup"><span data-stu-id="46f01-104">Direct3D 11 applications that run on Direct3D 9 graphics hardware could inadvertently cause the driver to receive **NULL** shader-resource views (SRVs) even when the applications bind non-**NULL** SRVs to the pixel shader stage.</span></span> <span data-ttu-id="46f01-105">Diese Situation kann nur auftreten, wenn die Anwendungen Srvs zerstören, während Sie ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="46f01-105">This situation can occur only if the applications destroy SRVs while they execute.</span></span> <span data-ttu-id="46f01-106">In diesem Thema wird erläutert, wie Sie den Treiber umgehen, der **null** -Shader-Ressourcen Sichten (Srvs) empfängt, auch wenn nicht-**null** -Srvs an die Pixel-Shader-Phase gebunden sind.</span><span class="sxs-lookup"><span data-stu-id="46f01-106">This topic discusses how to work around the driver receiving **NULL** shader-resource views (SRVs) even when non-**NULL** SRVs are bound to the pixel shader stage.</span></span>

<span data-ttu-id="46f01-107">Um zu verhindern, dass der Treiber unerwünschte **null** -Srvs empfängt, müssen die Anwendungen [**Verknüpfung id3d11devicecontext aus::P ssetshaderresources**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshaderresources) aufrufen, um alle Srvs vor jedem Aufrufen von [**Verknüpfung id3d11devicecontext aus::P ssetshader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader)zu entlegen.</span><span class="sxs-lookup"><span data-stu-id="46f01-107">To prevent the driver from receiving unwanted **NULL** SRVs, the applications must call [**ID3D11DeviceContext::PSSetShaderResources**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshaderresources) to unset all SRVs before each call to [**ID3D11DeviceContext::PSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader).</span></span> <span data-ttu-id="46f01-108">Wenn die Anwendungen Srvs jedoch bis zum Ende der Codeausführung nicht zerstören, müssen Sie die Srvs nicht entfernen.</span><span class="sxs-lookup"><span data-stu-id="46f01-108">However, if the applications do not destroy SRVs until the end of their code execution, they do not need to unset the SRVs.</span></span>

<span data-ttu-id="46f01-109">Der [Verweis Bereich 10level9](d3d11-graphics-reference-10level9.md) listet die Unterschiede zwischen der Art und Weise, wie sich verschiedene [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) -und [**Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) -Methoden auf verschiedenen 10 Level9-featureebenen</span><span class="sxs-lookup"><span data-stu-id="46f01-109">The [10Level9 Reference](d3d11-graphics-reference-10level9.md) section lists the differences between how various [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) and [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) methods behave at various 10Level9 feature levels.</span></span>

## <a name="related-topics"></a><span data-ttu-id="46f01-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="46f01-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46f01-111">Direct3D 11 auf downlevelhardware</span><span class="sxs-lookup"><span data-stu-id="46f01-111">Direct3D 11 on Downlevel Hardware</span></span>](overviews-direct3d-11-devices-downlevel.md)
</dt> </dl>

 

 




