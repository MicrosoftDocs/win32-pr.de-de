---
title: Shadertyp
description: Die Syntax zum Deklarieren einer shadervariablen in einem Effekt hat sich von Direct3D 9 auf Direct3D 10 geändert.
ms.assetid: d24ae9ad-1b3a-4a05-b28b-b6a0583c3da8
keywords:
- Shadertyp HLSL
topic_type:
- apiref
api_name:
- Shader Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0ca3332c441279d7f9221efe8cfa7638908ddc44
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976792"
---
# <a name="shader-type"></a><span data-ttu-id="de4c5-104">Shadertyp</span><span class="sxs-lookup"><span data-stu-id="de4c5-104">Shader Type</span></span>

<span data-ttu-id="de4c5-105">Die Syntax zum Deklarieren einer shadervariablen in einem Effekt hat sich von Direct3D 9 auf Direct3D 10 geändert.</span><span class="sxs-lookup"><span data-stu-id="de4c5-105">The syntax for declaring a shader variable in an effect changed from Direct3D 9 to Direct3D 10.</span></span>

## <a name="shader-type-for-direct3d-10"></a><span data-ttu-id="de4c5-106">Shadertyp für Direct3D 10</span><span class="sxs-lookup"><span data-stu-id="de4c5-106">Shader Type for Direct3D 10</span></span>

<span data-ttu-id="de4c5-107">Deklarieren Sie eine shadervariable innerhalb eines Effekts (in Direct3D 10) mithilfe der shadertypsyntax:</span><span class="sxs-lookup"><span data-stu-id="de4c5-107">Declare a shader variable within an effect pass (in Direct3D 10) using the shader type syntax:</span></span>



|                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de4c5-108">**Setpixelshader** Compile ( **shadertarget, shaderfunction** ); **Setgeometryshader** Compile ( **shadertarget, shaderfunction** ); **Setvertexshader** Compile ( **shadertarget, shaderfunction** );</span><span class="sxs-lookup"><span data-stu-id="de4c5-108">**SetPixelShader** Compile( **ShaderTarget, ShaderFunction** ); **SetGeometryShader** Compile( **ShaderTarget, ShaderFunction** ); **SetVertexShader** Compile( **ShaderTarget, ShaderFunction** );</span></span> |



 

### <a name="parameters"></a><span data-ttu-id="de4c5-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="de4c5-109">Parameters</span></span>



| <span data-ttu-id="de4c5-110">Element</span><span class="sxs-lookup"><span data-stu-id="de4c5-110">Item</span></span>                                                                                                                             | <span data-ttu-id="de4c5-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="de4c5-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de4c5-112"><span id="SetXXXShader"></span><span id="setxxxshader"></span><span id="SETXXXSHADER"></span>**Setxxxshader**</span><span class="sxs-lookup"><span data-stu-id="de4c5-112"><span id="SetXXXShader"></span><span id="setxxxshader"></span><span id="SETXXXSHADER"></span>**SetXXXShader**</span></span><br/>         | <span data-ttu-id="de4c5-113">Der Direct3D-API-Befehl, der das Shader-Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="de4c5-113">The Direct3D API call that creates the shader object.</span></span> <span data-ttu-id="de4c5-114">Kann wie folgt lauten: **setpixelshader** oder **setgeometryshader** oder **setvertexshader**.</span><span class="sxs-lookup"><span data-stu-id="de4c5-114">Can be either: **SetPixelShader** or **SetGeometryShader** or **SetVertexShader**.</span></span><br/>                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="de4c5-115"><span id="ShaderTarget"></span><span id="shadertarget"></span><span id="SHADERTARGET"></span>**Shadertarget**</span><span class="sxs-lookup"><span data-stu-id="de4c5-115"><span id="ShaderTarget"></span><span id="shadertarget"></span><span id="SHADERTARGET"></span>**ShaderTarget**</span></span><br/>         | <span data-ttu-id="de4c5-116">Das Shader-Modell, mit dem kompiliert werden soll.</span><span class="sxs-lookup"><span data-stu-id="de4c5-116">The shader model to compile against.</span></span> <span data-ttu-id="de4c5-117">Dies gilt für alle Ziele, einschließlich aller Direct3D 9-Ziele plus der [Shader Model 4](dx-graphics-hlsl-sm4.md) -Ziele: vs \_ 4 \_ 0, GS \_ 4 \_ 0 und PS \_ 4 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="de4c5-117">This is valid for any target including all Direct3D 9 targets plus the [shader model 4](dx-graphics-hlsl-sm4.md) targets: vs\_4\_0, gs\_4\_0, and ps\_4\_0.</span></span><br/>                                                                                                                                                                                                                                          |
| <span data-ttu-id="de4c5-118"><span id="ShaderFunction"></span><span id="shaderfunction"></span><span id="SHADERFUNCTION"></span>**Shaderfunction**</span><span class="sxs-lookup"><span data-stu-id="de4c5-118"><span id="ShaderFunction"></span><span id="shaderfunction"></span><span id="SHADERFUNCTION"></span>**ShaderFunction**</span></span><br/> | <span data-ttu-id="de4c5-119">Eine ASCII-Zeichenfolge, die den Namen der Shader-Einstiegspunkt Funktion enthält. Dies ist die Funktion, die mit der Ausführung beginnt, wenn der Shader aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="de4c5-119">An ASCII string that contains the name of the shader entry point function; this is the function that begins execution when the shader is invoked.</span></span> <span data-ttu-id="de4c5-120">Der (...) stellt die Shader-Argumente dar. Dabei handelt es sich um dieselben Argumente, die an die Shader-Erstellungs-API übergeben werden: [**vssetshader**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-vssetshader) oder [**gssetshader**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-gssetshader) oder [**pssetshader**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-pssetshader).</span><span class="sxs-lookup"><span data-stu-id="de4c5-120">The (...) represents the shader arguments; these are the same arguments passed to the shader creation API's: [**VSSetShader**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-vssetshader) or [**GSSetShader**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-gssetshader) or [**PSSetShader**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-pssetshader).</span></span><br/> |



 

### <a name="example"></a><span data-ttu-id="de4c5-121">Beispiel</span><span class="sxs-lookup"><span data-stu-id="de4c5-121">Example</span></span>

<span data-ttu-id="de4c5-122">Es folgt ein Beispiel, das ein Vertex-Shader-und Pixel-Shader-Objekt erstellt, das für ein bestimmtes Shader-Modell kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="de4c5-122">Here is an example that creates a vertex shader and pixel shader object, compiled for a particular shader model.</span></span> <span data-ttu-id="de4c5-123">Im Beispiel Direct3D 10 gibt es keinen Geometry-Shader, sodass der Zeiger auf **null** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="de4c5-123">In the Direct3D 10 example, there is no geometry shader, so the pointer is set to **NULL**.</span></span>


```
// Direct3D 10
technique10 Render
{
    pass P0
    {
        SetVertexShader( CompileShader( vs_4_0, VS() ) );
        SetGeometryShader( NULL );
        SetPixelShader( CompileShader( ps_4_0, PS() ) );
    }
}
```



## <a name="shader-type-for-direct3d-9"></a><span data-ttu-id="de4c5-124">Shadertyp für Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="de4c5-124">Shader Type for Direct3D 9</span></span>

<span data-ttu-id="de4c5-125">Deklarieren Sie eine shadervariable innerhalb eines Effekts (für Direct3D 9) mithilfe der shadertypsyntax:</span><span class="sxs-lookup"><span data-stu-id="de4c5-125">Declare a shader variable within an effect pass (for Direct3D 9) using the shader type syntax:</span></span>



|                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de4c5-126">**Pixelshader** = **shaderziel-shaderfunktion kompilieren (...); Vertexshader** = **shaderziel-shaderfunktion kompilieren (...);**</span><span class="sxs-lookup"><span data-stu-id="de4c5-126">**PixelShader** = compile **ShaderTarget ShaderFunction(...);VertexShader** = compile **ShaderTarget ShaderFunction(...);**</span></span> |



 

### <a name="parameters"></a><span data-ttu-id="de4c5-127">Parameter</span><span class="sxs-lookup"><span data-stu-id="de4c5-127">Parameters</span></span>



| <span data-ttu-id="de4c5-128">Element</span><span class="sxs-lookup"><span data-stu-id="de4c5-128">Item</span></span>                                                                                                                                                 | <span data-ttu-id="de4c5-129">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="de4c5-129">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de4c5-130"><span id="XXXShader"></span><span id="xxxshader"></span><span id="XXXSHADER"></span>**Xxxshader**</span><span class="sxs-lookup"><span data-stu-id="de4c5-130"><span id="XXXShader"></span><span id="xxxshader"></span><span id="XXXSHADER"></span>**XXXShader**</span></span><br/>                                         | <span data-ttu-id="de4c5-131">Eine Shader-Variable, die den kompilierten Shader darstellt.</span><span class="sxs-lookup"><span data-stu-id="de4c5-131">A shader variable, which represents the compiled shader.</span></span> <span data-ttu-id="de4c5-132">Kann entweder " **Pixelshader** " oder " **Vertexshader**" lauten.</span><span class="sxs-lookup"><span data-stu-id="de4c5-132">Can be either: **PixelShader** or **VertexShader**.</span></span><br/>                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="de4c5-133"><span id="ShaderTarget"></span><span id="shadertarget"></span><span id="SHADERTARGET"></span>**Shadertarget**</span><span class="sxs-lookup"><span data-stu-id="de4c5-133"><span id="ShaderTarget"></span><span id="shadertarget"></span><span id="SHADERTARGET"></span>**ShaderTarget**</span></span><br/>                             | <span data-ttu-id="de4c5-134">Das [Shader-Modell](dx-graphics-hlsl-models.md) , mit dem kompiliert werden soll. hängt vom Typ der shadervariablen ab.</span><span class="sxs-lookup"><span data-stu-id="de4c5-134">The [shader model](dx-graphics-hlsl-models.md) to compile against; depends on the type of shader variable.</span></span><br/>                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="de4c5-135"><span id="ShaderFunction_..._"></span><span id="shaderfunction_..._"></span><span id="SHADERFUNCTION_..._"></span>**Shaderfunction (...)**</span><span class="sxs-lookup"><span data-stu-id="de4c5-135"><span id="ShaderFunction_..._"></span><span id="shaderfunction_..._"></span><span id="SHADERFUNCTION_..._"></span>**ShaderFunction(...)**</span></span><br/> | <span data-ttu-id="de4c5-136">Eine ASCII-Zeichenfolge, die den Namen der Shader-Einstiegspunkt Funktion enthält. Dies ist die Funktion, die mit der Ausführung beginnt, wenn der Shader aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="de4c5-136">An ASCII string that contains the name of the shader entry point function; this is the function that begins execution when the shader is invoked.</span></span> <span data-ttu-id="de4c5-137">Der (...) stellt die Shader-Argumente dar. Dabei handelt es sich um dieselben Argumente, die an die Shader-Erstellungs-API ( [**setvertexshader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) oder [**setpixelshader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader)) übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="de4c5-137">The (...) represents the shader arguments; these are the same arguments passed to the shader creation API's: [**SetVertexShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) or [**SetPixelShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader).</span></span><br/> |



 

### <a name="example"></a><span data-ttu-id="de4c5-138">Beispiel</span><span class="sxs-lookup"><span data-stu-id="de4c5-138">Example</span></span>

<span data-ttu-id="de4c5-139">Im folgenden finden Sie ein Beispiel für ein Vertex-Shader-und Pixel-Shader-Objekt, das für ein bestimmtes Shader-Modell kompiliert wurde.</span><span class="sxs-lookup"><span data-stu-id="de4c5-139">Here is an example of a vertex shader and pixel shader object, compiled for a particular shader model.</span></span>


```
// Direct3D 9
technique RenderSceneWithTexture1Light
{
    pass P0
    {          
        VertexShader = compile vs_2_0 RenderSceneVS( 1, true, true );
        PixelShader  = compile ps_2_0 RenderScenePS( true );
    }
}
```



## <a name="see-also"></a><span data-ttu-id="de4c5-140">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="de4c5-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de4c5-141">Datentypen (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="de4c5-141">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

