---
title: Shaderstrukturen (Direct3D 11-Grafiken)
description: Strukturen werden verwendet, um Shaders zu erstellen und zu verwenden.
ms.assetid: 3b8ece5c-5065-4711-b12c-06cf7ea0e1ba
keywords:
- Strukturen, Direct3D 11-Shader
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14739e3db38c075e19e58a90b12bbf7d06b48a4e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739592"
---
# <a name="shader-structures-direct3d-11-graphics"></a><span data-ttu-id="7192c-104">Shaderstrukturen (Direct3D 11-Grafiken)</span><span class="sxs-lookup"><span data-stu-id="7192c-104">Shader Structures (Direct3D 11 Graphics)</span></span>

<span data-ttu-id="7192c-105">Strukturen werden verwendet, um Shaders zu erstellen und zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="7192c-105">Structures are used to create and use shaders.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="7192c-106">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="7192c-106">In this section</span></span>



| <span data-ttu-id="7192c-107">Thema</span><span class="sxs-lookup"><span data-stu-id="7192c-107">Topic</span></span>                                                                                       | <span data-ttu-id="7192c-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7192c-108">Description</span></span>                                                            |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="7192c-109">**D3D11- \_ Klassen \_ Instanz \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="7192c-109">**D3D11\_CLASS\_INSTANCE\_DESC**</span></span>](/windows/desktop/api/D3D11/ns-d3d11-d3d11_class_instance_desc)<br/>                | <span data-ttu-id="7192c-110">Beschreibt eine HLSL-Klasseninstanz.</span><span class="sxs-lookup"><span data-stu-id="7192c-110">Describes an HLSL class instance.</span></span><br/>                           |
| [<span data-ttu-id="7192c-111">**D3D11-Ablauf \_ Verfolgung für Compute- \_ Shader \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7192c-111">**D3D11\_COMPUTE\_SHADER\_TRACE\_DESC**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_compute_shader_trace_desc)<br/>   | <span data-ttu-id="7192c-112">Beschreibt eine Instanz eines Compute-Shaders für die Ablauf Verfolgung.</span><span class="sxs-lookup"><span data-stu-id="7192c-112">Describes an instance of a compute shader to trace.</span></span><br/>         |
| [<span data-ttu-id="7192c-113">**D3D11 \_ Domänen- \_ Shader-Ablauf \_ Verfolgung \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="7192c-113">**D3D11\_DOMAIN\_SHADER\_TRACE\_DESC**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_domain_shader_trace_desc)<br/>     | <span data-ttu-id="7192c-114">Beschreibt eine Instanz eines Domänen-Shaders für die Ablauf Verfolgung.</span><span class="sxs-lookup"><span data-stu-id="7192c-114">Describes an instance of a domain shader to trace.</span></span><br/>          |
| [<span data-ttu-id="7192c-115">**D3D11- \_ Funktion \_**</span><span class="sxs-lookup"><span data-stu-id="7192c-115">**D3D11\_FUNCTION\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_function_desc)<br/>                             | <span data-ttu-id="7192c-116">Beschreibt eine Funktion.</span><span class="sxs-lookup"><span data-stu-id="7192c-116">Describes a function.</span></span><br/>                                       |
| [<span data-ttu-id="7192c-117">**D3D11 \_ Geometry- \_ Shader- \_ \_ Ablaufverfolgungs-Debugger**</span><span class="sxs-lookup"><span data-stu-id="7192c-117">**D3D11\_GEOMETRY\_SHADER\_TRACE\_DESC**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_geometry_shader_trace_desc)<br/> | <span data-ttu-id="7192c-118">Beschreibt eine Instanz eines Geometry-Shaders für die Ablauf Verfolgung.</span><span class="sxs-lookup"><span data-stu-id="7192c-118">Describes an instance of a geometry shader to trace.</span></span><br/>        |
| [<span data-ttu-id="7192c-119">**D3D11 \_ Hull- \_ Shader- \_ \_ Ablaufverfolgungs-Debugger**</span><span class="sxs-lookup"><span data-stu-id="7192c-119">**D3D11\_HULL\_SHADER\_TRACE\_DESC**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_hull_shader_trace_desc)<br/>         | <span data-ttu-id="7192c-120">Beschreibt eine Instanz eines Hull-Shaders für die Ablauf Verfolgung.</span><span class="sxs-lookup"><span data-stu-id="7192c-120">Describes an instance of a hull shader to trace.</span></span><br/>            |
| [<span data-ttu-id="7192c-121">**D3D11- \_ Bibliothek \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="7192c-121">**D3D11\_LIBRARY\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_library_desc)<br/>                               | <span data-ttu-id="7192c-122">Beschreibt eine Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="7192c-122">Describes a library.</span></span><br/>                                        |
| [<span data-ttu-id="7192c-123">**D3D11- \_ Parameter \_**</span><span class="sxs-lookup"><span data-stu-id="7192c-123">**D3D11\_PARAMETER\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_parameter_desc)<br/>                           | <span data-ttu-id="7192c-124">Beschreibt einen Funktionsparameter.</span><span class="sxs-lookup"><span data-stu-id="7192c-124">Describes a function parameter.</span></span> <br/>                            |
| [<span data-ttu-id="7192c-125">**D3D11 \_ Pixel- \_ Shader- \_ \_ Ablaufverfolgungs-Debugger**</span><span class="sxs-lookup"><span data-stu-id="7192c-125">**D3D11\_PIXEL\_SHADER\_TRACE\_DESC**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_pixel_shader_trace_desc)<br/>       | <span data-ttu-id="7192c-126">Beschreibt eine Instanz eines Pixelshaders für die Ablauf Verfolgung.</span><span class="sxs-lookup"><span data-stu-id="7192c-126">Describes an instance of a pixel shader to trace.</span></span><br/>           |
| [<span data-ttu-id="7192c-127">**D3D11- \_ Shader- \_ Puffer \_ Absteigend**</span><span class="sxs-lookup"><span data-stu-id="7192c-127">**D3D11\_SHADER\_BUFFER\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_buffer_desc)<br/>                  | <span data-ttu-id="7192c-128">Beschreibt einen Shader-Konstantenpuffer.</span><span class="sxs-lookup"><span data-stu-id="7192c-128">Describes a shader constant-buffer.</span></span><br/>                         |
| [<span data-ttu-id="7192c-129">**D3D11- \_ Shader- \_ Debugger**</span><span class="sxs-lookup"><span data-stu-id="7192c-129">**D3D11\_SHADER\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_desc)<br/>                                 | <span data-ttu-id="7192c-130">Beschreibt einen Shader.</span><span class="sxs-lookup"><span data-stu-id="7192c-130">Describes a shader.</span></span><br/>                                         |
| [<span data-ttu-id="7192c-131">**D3D11 \_ Shader \_ input \_ Bind \_ Debug**</span><span class="sxs-lookup"><span data-stu-id="7192c-131">**D3D11\_SHADER\_INPUT\_BIND\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_input_bind_desc)<br/>         | <span data-ttu-id="7192c-132">Beschreibt, wie eine Shaderressource an eine Shadereingabe gebunden wird.</span><span class="sxs-lookup"><span data-stu-id="7192c-132">Describes how a shader resource is bound to a shader input.</span></span><br/> |
| [<span data-ttu-id="7192c-133">**D3D11- \_ Shader- \_ \_ Ablaufverfolgungs-Debug**</span><span class="sxs-lookup"><span data-stu-id="7192c-133">**D3D11\_SHADER\_TRACE\_DESC**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_shader_trace_desc)<br/>                    | <span data-ttu-id="7192c-134">Beschreibt ein Shader-Trace-Objekt.</span><span class="sxs-lookup"><span data-stu-id="7192c-134">Describes a shader-trace object.</span></span><br/>                            |
| [<span data-ttu-id="7192c-135">**D3D11 \_ \_ shadertyp \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="7192c-135">**D3D11\_SHADER\_TYPE\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_type_desc)<br/>                      | <span data-ttu-id="7192c-136">Beschreibt einen Shader-Variablentyp.</span><span class="sxs-lookup"><span data-stu-id="7192c-136">Describes a shader-variable type.</span></span><br/>                           |
| [<span data-ttu-id="7192c-137">**D3D11- \_ Shader- \_ Variable wird \_ deaktiviert**</span><span class="sxs-lookup"><span data-stu-id="7192c-137">**D3D11\_SHADER\_VARIABLE\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_variable_desc)<br/>              | <span data-ttu-id="7192c-138">Beschreibt eine shadervariable.</span><span class="sxs-lookup"><span data-stu-id="7192c-138">Describes a shader variable.</span></span><br/>                                |
| [<span data-ttu-id="7192c-139">**D3D11 \_ Signatur \_ Parameter \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="7192c-139">**D3D11\_SIGNATURE\_PARAMETER\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)<br/>      | <span data-ttu-id="7192c-140">Beschreibt eine shadersignatur.</span><span class="sxs-lookup"><span data-stu-id="7192c-140">Describes a shader signature.</span></span><br/>                               |
| [<span data-ttu-id="7192c-141">**D3D11-Ablauf \_ Verfolgungs \_ Register**</span><span class="sxs-lookup"><span data-stu-id="7192c-141">**D3D11\_TRACE\_REGISTER**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_trace_register)<br/>                           | <span data-ttu-id="7192c-142">Beschreibt ein Ablauf Verfolgungs Register.</span><span class="sxs-lookup"><span data-stu-id="7192c-142">Describes a trace register.</span></span><br/>                                 |
| [<span data-ttu-id="7192c-143">**D3D11-Ablauf \_ Verfolgungs \_ Statistik**</span><span class="sxs-lookup"><span data-stu-id="7192c-143">**D3D11\_TRACE\_STATS**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_trace_stats)<br/>                                 | <span data-ttu-id="7192c-144">Gibt Statistiken zu einer Ablauf Verfolgung an.</span><span class="sxs-lookup"><span data-stu-id="7192c-144">Specifies statistics about a trace.</span></span><br/>                         |
| [<span data-ttu-id="7192c-145">**D3D11-Ablauf \_ Verfolgungs \_ Schritt**</span><span class="sxs-lookup"><span data-stu-id="7192c-145">**D3D11\_TRACE\_STEP**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_trace_step)<br/>                                   | <span data-ttu-id="7192c-146">Beschreibt einen Ablauf Verfolgungs Schritt, bei dem es sich um eine Anweisung handelt.</span><span class="sxs-lookup"><span data-stu-id="7192c-146">Describes a trace step, which is an instruction.</span></span><br/>            |
| [<span data-ttu-id="7192c-147">**D3D11-Ablauf \_ Verfolgungs \_ Wert**</span><span class="sxs-lookup"><span data-stu-id="7192c-147">**D3D11\_TRACE\_VALUE**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_trace_value)<br/>                                 | <span data-ttu-id="7192c-148">Beschreibt einen Ablauf Verfolgungs Wert.</span><span class="sxs-lookup"><span data-stu-id="7192c-148">Describes a trace value.</span></span><br/>                                    |
| [<span data-ttu-id="7192c-149">**D3D11 \_ Vertex- \_ Shader-Ablauf \_ Verfolgung \_**</span><span class="sxs-lookup"><span data-stu-id="7192c-149">**D3D11\_VERTEX\_SHADER\_TRACE\_DESC**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_vertex_shader_trace_desc)<br/>     | <span data-ttu-id="7192c-150">Beschreibt eine Instanz eines Vertex-Shaders für die Ablauf Verfolgung.</span><span class="sxs-lookup"><span data-stu-id="7192c-150">Describes an instance of a vertex shader to trace.</span></span><br/>          |



 

## <a name="related-topics"></a><span data-ttu-id="7192c-151">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7192c-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7192c-152">Shader-Referenz</span><span class="sxs-lookup"><span data-stu-id="7192c-152">Shader Reference</span></span>](d3d11-graphics-reference-d3d11-shader.md)
</dt> </dl>

 

 





