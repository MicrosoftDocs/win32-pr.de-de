---
title: Shaderstrukturen (Direct3D 12-Grafiken)
description: d3d12shader. h deklariert die folgenden Strukturen, die zum Erstellen und Verwenden von Shadern verwendet werden.
ms.assetid: b8ece5c3-5065-4711-b12c-6cf7ea0e1ba0
keywords:
- Strukturen, Direct3D 12-Shader
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 400d50c48b8b94fc9a59d8e48179aae43e14a4f5
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106341573"
---
# <a name="shader-structures-direct3d-12-graphics"></a><span data-ttu-id="13386-104">Shaderstrukturen (Direct3D 12-Grafiken)</span><span class="sxs-lookup"><span data-stu-id="13386-104">Shader Structures (Direct3D 12 Graphics)</span></span>

<span data-ttu-id="13386-105">d3d12shader. h deklariert die folgenden Strukturen, die zum Erstellen und Verwenden von Shadern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="13386-105">d3d12shader.h declares the following structures, which are used to create and use shaders.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="13386-106">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="13386-106">In this section</span></span>



| <span data-ttu-id="13386-107">Thema</span><span class="sxs-lookup"><span data-stu-id="13386-107">Topic</span></span>                                                                                  | <span data-ttu-id="13386-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="13386-108">Description</span></span>                                                             |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="13386-109">**D3D12- \_ Funktion \_**</span><span class="sxs-lookup"><span data-stu-id="13386-109">**D3D12\_FUNCTION\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_function_desc)<br/>                        | <span data-ttu-id="13386-110">Beschreibt eine Funktion.</span><span class="sxs-lookup"><span data-stu-id="13386-110">Describes a function.</span></span> <br/>                                       |
| [<span data-ttu-id="13386-111">**D3D12- \_ Bibliothek \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="13386-111">**D3D12\_LIBRARY\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_library_desc)<br/>                          | <span data-ttu-id="13386-112">Beschreibt eine Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="13386-112">Describes a library.</span></span> <br/>                                        |
| [<span data-ttu-id="13386-113">**D3D12- \_ Parameter \_**</span><span class="sxs-lookup"><span data-stu-id="13386-113">**D3D12\_PARAMETER\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_parameter_desc)<br/>                      | <span data-ttu-id="13386-114">Beschreibt einen Funktionsparameter.</span><span class="sxs-lookup"><span data-stu-id="13386-114">Describes a function parameter.</span></span> <br/>                             |
| [<span data-ttu-id="13386-115">**D3D12- \_ Shader- \_ Puffer \_ Absteigend**</span><span class="sxs-lookup"><span data-stu-id="13386-115">**D3D12\_SHADER\_BUFFER\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_shader_buffer_desc)<br/>             | <span data-ttu-id="13386-116">Beschreibt einen Shader-Konstantenpuffer.</span><span class="sxs-lookup"><span data-stu-id="13386-116">Describes a shader constant-buffer.</span></span> <br/>                         |
| [<span data-ttu-id="13386-117">**D3D12- \_ Shader- \_ Debugger**</span><span class="sxs-lookup"><span data-stu-id="13386-117">**D3D12\_SHADER\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_shader_desc)<br/>                            | <span data-ttu-id="13386-118">Beschreibt einen Shader.</span><span class="sxs-lookup"><span data-stu-id="13386-118">Describes a shader.</span></span> <br/>                                         |
| [<span data-ttu-id="13386-119">**D3D12 \_ Shader \_ input \_ Bind \_ Debug**</span><span class="sxs-lookup"><span data-stu-id="13386-119">**D3D12\_SHADER\_INPUT\_BIND\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_shader_input_bind_desc)<br/>    | <span data-ttu-id="13386-120">Beschreibt, wie eine Shaderressource an eine Shadereingabe gebunden wird.</span><span class="sxs-lookup"><span data-stu-id="13386-120">Describes how a shader resource is bound to a shader input.</span></span> <br/> |
| [<span data-ttu-id="13386-121">**D3D12 \_ \_ shadertyp \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="13386-121">**D3D12\_SHADER\_TYPE\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_shader_type_desc)<br/>                 | <span data-ttu-id="13386-122">Beschreibt einen Shader-Variablentyp.</span><span class="sxs-lookup"><span data-stu-id="13386-122">Describes a shader-variable type.</span></span> <br/>                           |
| [<span data-ttu-id="13386-123">**D3D12- \_ Shader- \_ Variable wird \_ deaktiviert**</span><span class="sxs-lookup"><span data-stu-id="13386-123">**D3D12\_SHADER\_VARIABLE\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_shader_variable_desc)<br/>         | <span data-ttu-id="13386-124">Beschreibt eine shadervariable.</span><span class="sxs-lookup"><span data-stu-id="13386-124">Describes a shader variable.</span></span> <br/>                                |
| [<span data-ttu-id="13386-125">**D3D12 \_ Signatur \_ Parameter \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="13386-125">**D3D12\_SIGNATURE\_PARAMETER\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_signature_parameter_desc)<br/> | <span data-ttu-id="13386-126">Beschreibt eine shadersignatur.</span><span class="sxs-lookup"><span data-stu-id="13386-126">Describes a shader signature.</span></span> <br/>                               |



 

## <a name="related-topics"></a><span data-ttu-id="13386-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="13386-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13386-128">Referenz für Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="13386-128">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> <dt>

[<span data-ttu-id="13386-129">Shader-Referenz</span><span class="sxs-lookup"><span data-stu-id="13386-129">Shader Reference</span></span>](d3d12-graphics-reference-shader-reference.md)
</dt> </dl>

 

 





