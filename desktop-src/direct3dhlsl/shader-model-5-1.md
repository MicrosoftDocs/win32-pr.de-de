---
title: Shadermodell 5,1
description: Dieser Abschnitt enthält die Referenzseiten für das HLSL-Shader-Modell 5,1, das mit D3D12 eingeführt wurde.
ms.assetid: 814FAC95-7FD5-450F-964B-18E687DBCC56
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5fd2f2a2f4ebe86a090ebade8ebf8a033a7c612
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993047"
---
# <a name="shader-model-51"></a><span data-ttu-id="f18bc-103">Shadermodell 5,1</span><span class="sxs-lookup"><span data-stu-id="f18bc-103">Shader Model 5.1</span></span>

<span data-ttu-id="f18bc-104">Dieser Abschnitt enthält die Referenzseiten für das HLSL-Shader-Modell 5,1, das mit D3D12 eingeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="f18bc-104">This section contains the reference pages for HLSL Shader Model 5.1, introduced with D3D12.</span></span>

<span data-ttu-id="f18bc-105">Das Shader-Modell 5,1 ist mit [Shader Model 5](d3d11-graphics-reference-sm5.md)funktionell vergleichbar. die Haupt Änderung ist eine höhere Flexibilität bei der Ressourcen Auswahl, da in einem Shader eine Indizierung von Deskriptoren ermöglicht wird.</span><span class="sxs-lookup"><span data-stu-id="f18bc-105">Shader Model 5.1 is functionally very similar to [Shader Model 5](d3d11-graphics-reference-sm5.md), the main change is more flexibility in resource selection by allowing indexing of arrays of descriptors from within a shader.</span></span>



| <span data-ttu-id="f18bc-106">Feature</span><span class="sxs-lookup"><span data-stu-id="f18bc-106">Feature</span></span>                   | <span data-ttu-id="f18bc-107">Funktion</span><span class="sxs-lookup"><span data-stu-id="f18bc-107">Capability</span></span>                                                                |
|---------------------------|---------------------------------------------------------------------------|
| <span data-ttu-id="f18bc-108">Instruktionssatz</span><span class="sxs-lookup"><span data-stu-id="f18bc-108">Instruction Set</span></span>           | [<span data-ttu-id="f18bc-109">**Intrinsische HLSL-Funktionen**</span><span class="sxs-lookup"><span data-stu-id="f18bc-109">**HLSL intrinsic functions**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)  |
| <span data-ttu-id="f18bc-110">Vertex-Shader Max</span><span class="sxs-lookup"><span data-stu-id="f18bc-110">Vertex Shader Max</span></span>         | <span data-ttu-id="f18bc-111">Keine Einschränkung</span><span class="sxs-lookup"><span data-stu-id="f18bc-111">No restriction</span></span>                                                            |
| <span data-ttu-id="f18bc-112">Pixel-Shader max.</span><span class="sxs-lookup"><span data-stu-id="f18bc-112">Pixel Shader Max</span></span>          | <span data-ttu-id="f18bc-113">Keine Einschränkung</span><span class="sxs-lookup"><span data-stu-id="f18bc-113">No restriction</span></span>                                                            |
| <span data-ttu-id="f18bc-114">Neue shaderprofile hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="f18bc-114">New Shader Profiles Added</span></span> | <span data-ttu-id="f18bc-115">CS \_ 5 \_ 1, DS \_ 5 \_ 1, GS \_ 5 \_ 1, HS \_ 5 \_ 1, PS \_ 5 \_ 1, vs \_ 5 \_ 1, rootsig \_ 1 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f18bc-115">cs\_5\_1, ds\_5\_1, gs\_5\_1, hs\_5\_1, ps\_5\_1, vs\_5\_1, rootsig\_1\_0</span></span> |



 

## <a name="in-this-section"></a><span data-ttu-id="f18bc-116">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="f18bc-116">In this section</span></span>



| <span data-ttu-id="f18bc-117">Thema</span><span class="sxs-lookup"><span data-stu-id="f18bc-117">Topic</span></span>                                                                           | <span data-ttu-id="f18bc-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f18bc-118">Description</span></span>                                                           |
|---------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="f18bc-119">Shader-Modell 5,1-Objekte</span><span class="sxs-lookup"><span data-stu-id="f18bc-119">Shader Model 5.1 Objects</span></span>](shader-model-5-1-objects.md)<br/>             | <span data-ttu-id="f18bc-120">Die folgenden Objekte wurden dem Shader-Modell 5,1 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f18bc-120">The following objects have been added to shader model 5.1.</span></span><br/> |
| [<span data-ttu-id="f18bc-121">Shader-Modell 5,1 System Werte</span><span class="sxs-lookup"><span data-stu-id="f18bc-121">Shader Model 5.1 System Values</span></span>](shader-model-5-1-system-values.md)<br/> | <span data-ttu-id="f18bc-122">Das Shader-Modell 5,1 fügt die folgenden neuen System Werte hinzu.</span><span class="sxs-lookup"><span data-stu-id="f18bc-122">Shader Model 5.1 adds the following new system values.</span></span><br/>     |



 

## <a name="related-topics"></a><span data-ttu-id="f18bc-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f18bc-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f18bc-124">Shader-Modelle vs shaderprofile</span><span class="sxs-lookup"><span data-stu-id="f18bc-124">Shader Models vs Shader Profiles</span></span>](dx-graphics-hlsl-models.md)
</dt> <dt>

[<span data-ttu-id="f18bc-125">HLSL-Shader-Modell 5,1 Features für Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="f18bc-125">HLSL Shader Model 5.1 Features for Direct3D 12</span></span>](hlsl-shader-model-5-1-features-for-direct3d-12.md)
</dt> </dl>

 

 





