---
title: Erstellen eines Domänen-Shader
description: In diesem Thema wird gezeigt, wie ein Domänen-Shader erstellt wird.
ms.assetid: 7d02fee4-2d7c-434b-86ab-e5ee615ae93b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f89b7f3d7ec6cf801432a5745520fcbd924d139
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036487"
---
# <a name="how-to-create-a-domain-shader"></a><span data-ttu-id="1e760-103">Vorgehensweise: Erstellen eines Domänen-Shader</span><span class="sxs-lookup"><span data-stu-id="1e760-103">How To: Create a Domain Shader</span></span>

<span data-ttu-id="1e760-104">Ein Domänen-Shader ist der dritte von drei Phasen, die zusammenarbeiten, um Mosaik Vorgänge [zu implementieren.](direct3d-11-advanced-stages-tessellation.md)</span><span class="sxs-lookup"><span data-stu-id="1e760-104">A domain shader is the third of three stages that work together to implement [tessellation](direct3d-11-advanced-stages-tessellation.md).</span></span> <span data-ttu-id="1e760-105">Die Eingaben für die Domäne-Shader-Phase stammen aus einem Hull-Shader.</span><span class="sxs-lookup"><span data-stu-id="1e760-105">The inputs for the domain-shader stage come from a hull shader.</span></span> <span data-ttu-id="1e760-106">In diesem Thema wird gezeigt, wie ein Domänen-Shader erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="1e760-106">This topic shows how to create a domain shader.</span></span>

<span data-ttu-id="1e760-107">Ein Domänen-Shader transformiert Oberflächengeometrie (erstellt durch die Mosaik Phase "Fixed-Function") mithilfe von Hull-Shader-Ausgabe Steuerungs Punkten, Hull-Shader-Ausgabe Patch-konstantendaten und einem einzelnen Satz von Mosaik-UV-Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="1e760-107">A domain shader transforms surface geometry (created by the fixed-function tessellator stage) using hull shader output-control points, hull shader output patch-constant data, and a single set of tessellator uv coordinates.</span></span>

<span data-ttu-id="1e760-108">**So erstellen Sie einen Domänen-Shader**</span><span class="sxs-lookup"><span data-stu-id="1e760-108">**To create a domain shader**</span></span>

1.  <span data-ttu-id="1e760-109">Entwerfen Sie einen Domänen-Shader.</span><span class="sxs-lookup"><span data-stu-id="1e760-109">Design a domain shader.</span></span> <span data-ttu-id="1e760-110">Weitere Informationen finden [Sie unter Gewusst wie: Entwerfen eines Domänen Shaders](direct3d-11-advanced-stages-domain-shader-design.md).</span><span class="sxs-lookup"><span data-stu-id="1e760-110">See [How To: Design a Domain Shader](direct3d-11-advanced-stages-domain-shader-design.md).</span></span>
2.  <span data-ttu-id="1e760-111">Kompilieren Sie den Shader-Code.</span><span class="sxs-lookup"><span data-stu-id="1e760-111">Compile the shader code.</span></span>
3.  <span data-ttu-id="1e760-112">Erstellen Sie ein Domänen-Shader-Objekt mit [**ID3D11Device:: kreatedomainshader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader).</span><span class="sxs-lookup"><span data-stu-id="1e760-112">Create a domain-shader object using [**ID3D11Device::CreateDomainShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader).</span></span>
    ```
    HRESULT CreateDomainShader(
      const void *pShaderBytecode, // 
      SIZE_T BytecodeLength, // 
      ID3D11ClassLinkage *pClassLinkage, // 
      ID3D11DomainShader **ppDomainShader
    );
    ```

    

4.  <span data-ttu-id="1e760-113">Initialisieren Sie die Pipeline Phase mithilfe von [**Verknüpfung id3d11devicecontext aus::D ssetshader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader).</span><span class="sxs-lookup"><span data-stu-id="1e760-113">Initialize the pipeline stage using [**ID3D11DeviceContext::DSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader).</span></span>
    ```
    void DSSetShader(
      ID3D11DomainShader *pDomainShader, // 
      ID3D11ClassInstance *const *ppClassInstances,
      UINT NumClassInstances
    );
    ```

    

<span data-ttu-id="1e760-114">Wenn ein Hull-Shader gebunden ist, muss ein Domänen-Shader an die Pipeline gebunden werden.</span><span class="sxs-lookup"><span data-stu-id="1e760-114">A domain shader must be bound to the pipeline if a hull shader is bound.</span></span> <span data-ttu-id="1e760-115">Insbesondere ist es nicht zulässig, Hull-Shader-Steuerungs Punkte direkt mit dem Geometry-Shader zu streamen.</span><span class="sxs-lookup"><span data-stu-id="1e760-115">In particular, it is not valid to directly stream out hull shader control points with the geometry shader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1e760-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1e760-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e760-117">Verwendung von Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="1e760-117">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> <dt>

[<span data-ttu-id="1e760-118">Mosaik Übersicht</span><span class="sxs-lookup"><span data-stu-id="1e760-118">Tessellation Overview</span></span>](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 




