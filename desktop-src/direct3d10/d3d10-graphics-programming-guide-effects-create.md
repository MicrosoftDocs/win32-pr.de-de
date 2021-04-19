---
description: Ein Effekt wird erstellt, indem er in das Effects-Framework geladen wird.
ms.assetid: b0a12620-4f8f-44d9-bc73-2c3ab30f80af
title: Erstellen eines Effekts (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b630bae35b8e1390a4be77e5cb5e4aaa3f41d9c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346843"
---
# <a name="create-an-effect-direct3d-10"></a><span data-ttu-id="e83a1-103">Erstellen eines Effekts (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="e83a1-103">Create an Effect (Direct3D 10)</span></span>

<span data-ttu-id="e83a1-104">Ein Effekt wird erstellt, indem er in das Effects-Framework geladen wird.</span><span class="sxs-lookup"><span data-stu-id="e83a1-104">An effect is created by loading it into the effects framework.</span></span> <span data-ttu-id="e83a1-105">Wenn der Effekt noch nie kompiliert wurde, wird er kompiliert, wenn er erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="e83a1-105">If the effect has never been compiled, it will be compiled when it is created.</span></span> <span data-ttu-id="e83a1-106">Effekte, die bereits in den Arbeitsspeicher geladen wurden, können durch Aufrufen von [**D3DX10CreateEffectFromMemory**](d3dx10createeffectfrommemory.md)erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="e83a1-106">Effects that are already loaded into memory can be created by calling [**D3DX10CreateEffectFromMemory**](d3dx10createeffectfrommemory.md).</span></span> <span data-ttu-id="e83a1-107">Im folgenden Codebeispiel wird [**D3DX10CreateEffectFromFile**](d3dx10createeffectfromfile.md) verwendet, um einen Effekt aus einer Datei zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e83a1-107">The following code example uses [**D3DX10CreateEffectFromFile**](d3dx10createeffectfromfile.md) to create an effect from a file.</span></span>


```
ID3D10Effect* g_pEffect10 = NULL; 

// Read the effect file 
D3DX10CreateEffectFromFile( "BasicHLSL10.fx", NULL, NULL,
  D3D10_SHADER_ENABLE_STRICTNESS, 0, pd3dDevice, NULL, NULL, 
  &g_pEffect10, NULL );
```



<span data-ttu-id="e83a1-108">Das Lesen eines Effekts erfordert dieselben Parameter wie das Kompilieren eines Effekts sowie eines Geräts und eines Pools.</span><span class="sxs-lookup"><span data-stu-id="e83a1-108">Reading an effect requires the same parameters as compiling an effect, plus a device and a pool.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e83a1-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e83a1-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e83a1-110">Rendern eines Effekts (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="e83a1-110">Rendering an Effect (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 



