---
title: Shader-Modell 5
description: Dieser Abschnitt enthält die Referenzseiten für HLSL-Shader-Modell 5.
ms.assetid: ec646940-8901-45c5-a44c-434c8acae2aa
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f379301008190367a40959a319d01cfad127f6b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390513"
---
# <a name="shader-model-5"></a><span data-ttu-id="dc9b3-103">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="dc9b3-103">Shader Model 5</span></span>

<span data-ttu-id="dc9b3-104">Dieser Abschnitt enthält die Referenzseiten für HLSL-Shader-Modell 5.</span><span class="sxs-lookup"><span data-stu-id="dc9b3-104">This section contains the reference pages for HLSL Shader Model 5.</span></span>

<span data-ttu-id="dc9b3-105">Shader Model 5 ist eine supermenge der untergeordneten Funktionen in [Shader Model 4](dx-graphics-hlsl-sm4.md).</span><span class="sxs-lookup"><span data-stu-id="dc9b3-105">Shader Model 5 is a superset of the capabilites in [Shader Model 4](dx-graphics-hlsl-sm4.md).</span></span> <span data-ttu-id="dc9b3-106">Es wurde mithilfe eines gemeinsamen Shader-Kerns entworfen, der einen gemeinsamen Satz von Features für alle programmierbaren Shader bereitstellt, die nur mit HLSL programmierbar sind.</span><span class="sxs-lookup"><span data-stu-id="dc9b3-106">It has been designed using a common-shader core which provides a common set of features to all programmable shaders, which are only programmable using HLSL.</span></span>



| <span data-ttu-id="dc9b3-107">Feature</span><span class="sxs-lookup"><span data-stu-id="dc9b3-107">Feature</span></span>                   | <span data-ttu-id="dc9b3-108">Funktion</span><span class="sxs-lookup"><span data-stu-id="dc9b3-108">Capability</span></span>                                                                                                                                             |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc9b3-109">Instruktionssatz</span><span class="sxs-lookup"><span data-stu-id="dc9b3-109">Instruction Set</span></span>           | [<span data-ttu-id="dc9b3-110">**Intrinsische HLSL-Funktionen**</span><span class="sxs-lookup"><span data-stu-id="dc9b3-110">**HLSL intrinsic functions**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                                               |
| <span data-ttu-id="dc9b3-111">Vertex-Shader Max</span><span class="sxs-lookup"><span data-stu-id="dc9b3-111">Vertex Shader Max</span></span>         | <span data-ttu-id="dc9b3-112">Keine Einschränkung</span><span class="sxs-lookup"><span data-stu-id="dc9b3-112">No restriction</span></span>                                                                                                                                         |
| <span data-ttu-id="dc9b3-113">Pixel-Shader max.</span><span class="sxs-lookup"><span data-stu-id="dc9b3-113">Pixel Shader Max</span></span>          | <span data-ttu-id="dc9b3-114">Keine Einschränkung</span><span class="sxs-lookup"><span data-stu-id="dc9b3-114">No restriction</span></span>                                                                                                                                         |
| <span data-ttu-id="dc9b3-115">Neue shaderprofile hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="dc9b3-115">New Shader Profiles Added</span></span> | <span data-ttu-id="dc9b3-116">CS \_ 4 \_ 0, GS \_ 4 \_ 0 \* , PS \_ 4 \_ 0 \* , vs \_ 4 \_ 0 \* , CS \_ 4 \_ 1, GS \_ 4 \_ 1 \* , PS \_ 4 \_ 1 \* , vs \_ 4 \_ 1 \* , CS \_ 5 \_ 0, DS \_ 5 \_ 0, GS \_ 5 \_ 0, HS \_ 5 \_ 0, PS \_ 5 \_ 0, vs \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="dc9b3-116">cs\_4\_0, gs\_4\_0\*, ps\_4\_0\*, vs\_4\_0\*, cs\_4\_1, gs\_4\_1\*, ps\_4\_1\*, vs\_4\_1\*, cs\_5\_0, ds\_5\_0, gs\_5\_0, hs\_5\_0, ps\_5\_0, vs\_5\_0</span></span> |



 

<span data-ttu-id="dc9b3-117">\* -GS \_ 4 \_ 0, GS \_ 4 \_ 1, PS \_ 4 \_ 0, PS \_ 4 \_ 1, vs \_ 4 \_ 0 und vs \_ 4 \_ 1 wurden im Shader-Modell 4,0 eingeführt. DirectX 11 fügt jedoch Unterstützung für [strukturierte Puffer](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) und Byte Adress Puffer für Shader Model 4, die auf DirectX 10-Hardware ausgeführt wird, hinzu.</span><span class="sxs-lookup"><span data-stu-id="dc9b3-117">\* - gs\_4\_0, gs\_4\_1, ps\_4\_0, ps\_4\_1, vs\_4\_0 and vs\_4\_1 were introduced in Shader Model 4.0, however, DirectX 11 adds support for [structured buffers](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) and byte address buffers to Shader Model 4 running on DirectX 10 hardware.</span></span>

<span data-ttu-id="dc9b3-118">Shader Model 5 führt den [Compute-Shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader) ein, der hoch Geschwindigkeits Computing für allgemeine Zwecke bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="dc9b3-118">Shader Model 5 introduces the [compute shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader) which provides high-speed general purpose computing.</span></span>

<span data-ttu-id="dc9b3-119">Eine ausführlichere Liste der Shader Model 5-Features finden Sie in einer Auflistung der [Direct3D 11-Features](/windows/desktop/direct3d11/direct3d-11-features).</span><span class="sxs-lookup"><span data-stu-id="dc9b3-119">A more complete listing of Shader Model 5 features is included in a listing of the [Direct3D 11 features](/windows/desktop/direct3d11/direct3d-11-features).</span></span>

<span data-ttu-id="dc9b3-120">Im Abschnitt [Shader Model 5 Assembly](shader-model-5-assembly--directx-hlsl-.md) werden die Assemblyanweisungen beschrieben, die das Shadermodell 5 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dc9b3-120">The [Shader Model 5 Assembly](shader-model-5-assembly--directx-hlsl-.md) section describes the assembly instructions that the Shader Model 5 supports.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="dc9b3-121">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="dc9b3-121">In This Section</span></span>



| <span data-ttu-id="dc9b3-122">Element</span><span class="sxs-lookup"><span data-stu-id="dc9b3-122">Item</span></span>                                                                                                                                                                                                                                                        | <span data-ttu-id="dc9b3-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dc9b3-123">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="dc9b3-124"><span id="Shader_Model_5_Attributes"></span><span id="shader_model_5_attributes"></span><span id="SHADER_MODEL_5_ATTRIBUTES"></span>[Shader Model 5-Attribute](d3d11-graphics-reference-sm5-attributes.md)</span><span class="sxs-lookup"><span data-stu-id="dc9b3-124"><span id="Shader_Model_5_Attributes"></span><span id="shader_model_5_attributes"></span><span id="SHADER_MODEL_5_ATTRIBUTES"></span>[Shader Model 5 Attributes](d3d11-graphics-reference-sm5-attributes.md)</span></span><br/>                                     | <span data-ttu-id="dc9b3-125">Referenzseiten für Shader Model 5-Attribute.</span><span class="sxs-lookup"><span data-stu-id="dc9b3-125">Reference pages for Shader Model 5 attributes.</span></span><br/>          |
| <span data-ttu-id="dc9b3-126"><span id="Shader_Model_5_Intrinsic_Functions"></span><span id="shader_model_5_intrinsic_functions"></span><span id="SHADER_MODEL_5_INTRINSIC_FUNCTIONS"></span>[Intrinsische Funktionen von Shader Model 5](d3d11-graphics-reference-sm5-intrinsics.md)</span><span class="sxs-lookup"><span data-stu-id="dc9b3-126"><span id="Shader_Model_5_Intrinsic_Functions"></span><span id="shader_model_5_intrinsic_functions"></span><span id="SHADER_MODEL_5_INTRINSIC_FUNCTIONS"></span>[Shader Model 5 Intrinsic Functions](d3d11-graphics-reference-sm5-intrinsics.md)</span></span><br/> | <span data-ttu-id="dc9b3-127">Referenzseiten für intrinsische Shader Model 5-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="dc9b3-127">Reference pages for Shader Model 5 intrinsic functions.</span></span><br/> |
| <span data-ttu-id="dc9b3-128"><span id="Shader_Model_5_Objects"></span><span id="shader_model_5_objects"></span><span id="SHADER_MODEL_5_OBJECTS"></span>[Shader Model 5-Objekte](d3d11-graphics-reference-sm5-objects.md)</span><span class="sxs-lookup"><span data-stu-id="dc9b3-128"><span id="Shader_Model_5_Objects"></span><span id="shader_model_5_objects"></span><span id="SHADER_MODEL_5_OBJECTS"></span>[Shader Model 5 Objects](d3d11-graphics-reference-sm5-objects.md)</span></span><br/>                                                    | <span data-ttu-id="dc9b3-129">Referenzseiten für Shader Model 5-Objekte und-Methoden.</span><span class="sxs-lookup"><span data-stu-id="dc9b3-129">Reference pages for Shader Model 5 objects and methods.</span></span><br/> |
| <span data-ttu-id="dc9b3-130"><span id="Shader_Model_5_System_Values"></span><span id="shader_model_5_system_values"></span><span id="SHADER_MODEL_5_SYSTEM_VALUES"></span>[Shader-Modell 5-System Werte](d3d11-graphics-reference-sm5-system-values.md)</span><span class="sxs-lookup"><span data-stu-id="dc9b3-130"><span id="Shader_Model_5_System_Values"></span><span id="shader_model_5_system_values"></span><span id="SHADER_MODEL_5_SYSTEM_VALUES"></span>[Shader Model 5 System Values](d3d11-graphics-reference-sm5-system-values.md)</span></span><br/>                      | <span data-ttu-id="dc9b3-131">Referenzseiten für Shader Model 5-System Werte.</span><span class="sxs-lookup"><span data-stu-id="dc9b3-131">Reference pages for Shader Model 5 system values.</span></span><br/>       |



 

## <a name="related-topics"></a><span data-ttu-id="dc9b3-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dc9b3-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc9b3-133">Shader-Modelle vs shaderprofile</span><span class="sxs-lookup"><span data-stu-id="dc9b3-133">Shader Models vs Shader Profiles</span></span>](dx-graphics-hlsl-models.md)
</dt> </dl>

 

