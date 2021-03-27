---
title: Erstellen eines Hull-Shaders
description: In diesem Thema wird gezeigt, wie ein Hull-Shader erstellt wird.
ms.assetid: 221cb578-fcfc-411a-8515-7880a96e32ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1a1eea7d2e6e70377028976f9576790ce3b64ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708183"
---
# <a name="how-to-create-a-hull-shader"></a><span data-ttu-id="ebb3b-103">Gewusst wie: Erstellen eines Hull-Shaders</span><span class="sxs-lookup"><span data-stu-id="ebb3b-103">How To: Create a Hull Shader</span></span>

<span data-ttu-id="ebb3b-104">Ein Hull-Shader ist die erste von drei Phasen, die zusammenarbeiten, um Mosaik Vorgänge [zu implementieren.](direct3d-11-advanced-stages-tessellation.md)</span><span class="sxs-lookup"><span data-stu-id="ebb3b-104">A hull shader is the first of three stages that work together to implement [tessellation](direct3d-11-advanced-stages-tessellation.md).</span></span> <span data-ttu-id="ebb3b-105">Die Hull-Shader-Ausgaben steuern die Mosaik Phase sowie die Domäne-Shader-Stufe.</span><span class="sxs-lookup"><span data-stu-id="ebb3b-105">The hull-shader outputs drive the tessellator stage, as well as the domain-shader stage.</span></span> <span data-ttu-id="ebb3b-106">In diesem Thema wird gezeigt, wie ein Hull-Shader erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="ebb3b-106">This topic shows how to create a hull shader.</span></span>

<span data-ttu-id="ebb3b-107">Ein Hull-Shader wandelt eine Reihe von Eingabe Steuerungs Punkten (von einem Vertex-Shader) in einen Satz von Ausgabe Steuerungs Punkten um.</span><span class="sxs-lookup"><span data-stu-id="ebb3b-107">A hull shader transforms a set of input control points (from a vertex shader) into a set of output control points.</span></span> <span data-ttu-id="ebb3b-108">Die Anzahl von Eingabe-und Ausgabe Punkten kann in Abhängigkeit von der Transformation (bei einer typischen Transformation eine Basis Transformation) variieren.</span><span class="sxs-lookup"><span data-stu-id="ebb3b-108">The number of input and output points can vary in contents and number depending on the transform (a typical transformation would be a basis transformation).</span></span>

<span data-ttu-id="ebb3b-109">Ein Hull-Shader gibt auch patchkonstante Informationen wie Mosaik Faktoren für einen Domänen-Shader und den Mosaik Ausdruck aus.</span><span class="sxs-lookup"><span data-stu-id="ebb3b-109">A hull shader also outputs patch constant information, such as tessellation factors, for a domain shader and the tessellator.</span></span> <span data-ttu-id="ebb3b-110">Die Mosaik Stufe Fixed-Function verwendet die Mosaik Faktoren sowie einen anderen Zustand, der in einem Hull-Shader deklariert wurde, um zu bestimmen, wie viel der Mosaik Prozess ist.</span><span class="sxs-lookup"><span data-stu-id="ebb3b-110">The fixed-function tessellator stage uses the tessellation factors as well as other state declared in a hull shader to determine how much to tessellate.</span></span>

<span data-ttu-id="ebb3b-111">**So erstellen Sie einen Hull-Shader**</span><span class="sxs-lookup"><span data-stu-id="ebb3b-111">**To create a hull shader**</span></span>

1.  <span data-ttu-id="ebb3b-112">Entwerfen Sie einen Hull-Shader.</span><span class="sxs-lookup"><span data-stu-id="ebb3b-112">Design a hull shader.</span></span> <span data-ttu-id="ebb3b-113">Weitere Informationen finden [Sie unter Gewusst wie: Entwerfen eines Hull-Shaders](direct3d-11-advanced-stages-hull-shader-design.md).</span><span class="sxs-lookup"><span data-stu-id="ebb3b-113">See [How To: Design a Hull Shader](direct3d-11-advanced-stages-hull-shader-design.md).</span></span>
2.  <span data-ttu-id="ebb3b-114">Kompilieren des Shader-Codes</span><span class="sxs-lookup"><span data-stu-id="ebb3b-114">Compile the shader code</span></span>
3.  <span data-ttu-id="ebb3b-115">Erstellen Sie ein Hull-Shader-Objekt mit [**ID3D11Device:: kreatehullshader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader).</span><span class="sxs-lookup"><span data-stu-id="ebb3b-115">Create a hull-shader object using [**ID3D11Device::CreateHullShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader).</span></span>
    ```
    HRESULT CreateHullShader(
      const void *pShaderBytecode,  
      SIZE_T BytecodeLength,  
      ID3D11ClassLinkage *pClassLinkage,  
      ID3D11HullShader **ppHullShader
    );
    ```

    

4.  <span data-ttu-id="ebb3b-116">Initialisieren Sie die Pipeline Phase mithilfe von [**Verknüpfung id3d11devicecontext aus:: hssetshader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader).</span><span class="sxs-lookup"><span data-stu-id="ebb3b-116">Initialize the pipeline stage using [**ID3D11DeviceContext::HSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader).</span></span>
    ```
    void HSSetShader(
      ID3D11HullShader *pHullShader,  
      ID3D11ClassInstance *const *ppClassInstances,
      UINT NumClassInstances
    );
    ```

    

<span data-ttu-id="ebb3b-117">Wenn ein Hull-Shader gebunden ist, muss ein Domänen-Shader an die Pipeline gebunden werden.</span><span class="sxs-lookup"><span data-stu-id="ebb3b-117">A domain shader must be bound to the pipeline if a hull shader is bound.</span></span> <span data-ttu-id="ebb3b-118">Insbesondere ist es nicht zulässig, Hull-Shader-Steuerungs Punkte direkt mit dem Geometry-Shader zu streamen.</span><span class="sxs-lookup"><span data-stu-id="ebb3b-118">In particular, it is not valid to directly stream out hull shader control points with the geometry shader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ebb3b-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ebb3b-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ebb3b-120">Verwendung von Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="ebb3b-120">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> <dt>

[<span data-ttu-id="ebb3b-121">Mosaik Übersicht</span><span class="sxs-lookup"><span data-stu-id="ebb3b-121">Tessellation Overview</span></span>](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 




