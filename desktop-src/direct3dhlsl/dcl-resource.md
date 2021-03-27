---
title: dcl_resource (SM4-ASM)
description: DCL \_ -Ressource (SM4-ASM)
ms.assetid: 045610f0-f7db-4bf2-bfea-501bbee94601
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bb65a8ea83feaf2fec80403fc9ac6c2ab38c1936
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719470"
---
# <a name="dcl_resource-sm4---asm"></a><span data-ttu-id="5db17-103">DCL \_ -Ressource (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="5db17-103">dcl\_resource (sm4 - asm)</span></span>

<span data-ttu-id="5db17-104">Deklariert eine nicht Multisampling-Shader-Input-Ressource.</span><span class="sxs-lookup"><span data-stu-id="5db17-104">Declares a non-multisampled shader-input resource.</span></span>



| <span data-ttu-id="5db17-105">DCL- \_ Ressource *tN*, *ResourceType*, *returnType (e)*</span><span class="sxs-lookup"><span data-stu-id="5db17-105">dcl\_resource *tN*, *resourceType*, *returnType(s)*</span></span> |
|-----------------------------------------------------|



 

<span data-ttu-id="5db17-106">Deklariert eine Multisampling-Ressource "Shader-Input".</span><span class="sxs-lookup"><span data-stu-id="5db17-106">Declares a multisampled shader-input resource.</span></span>



| <span data-ttu-id="5db17-107">DCL- \_ Ressource *tN*, *ResourceType \[ size \] NN*, *returnType (e)*</span><span class="sxs-lookup"><span data-stu-id="5db17-107">dcl\_resource *tN*, *resourceType\[size\]NN*, *returnType(s)*</span></span> |
|---------------------------------------------------------------|



 



| <span data-ttu-id="5db17-108">Element</span><span class="sxs-lookup"><span data-stu-id="5db17-108">Item</span></span>                                                                                                                                                     | <span data-ttu-id="5db17-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5db17-109">Description</span></span>                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5db17-110"><span id="tN"></span><span id="tn"></span><span id="TN"></span>t *N*</span><span class="sxs-lookup"><span data-stu-id="5db17-110"><span id="tN"></span><span id="tn"></span><span id="TN"></span>t *N*</span></span><br/>                                                                           | <span data-ttu-id="5db17-111">\[im \] Textur Register, wobei *N* eine ganze Zahl ist, die die Registernummer bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="5db17-111">\[in\] The texture register, where *N* is an integer that denotes the register number.</span></span><br/>                                                                                                                                                                        |
| <span data-ttu-id="5db17-112"><span id="resourceType"></span><span id="resourcetype"></span><span id="RESOURCETYPE"></span>*ResourceType*</span><span class="sxs-lookup"><span data-stu-id="5db17-112"><span id="resourceType"></span><span id="resourcetype"></span><span id="RESOURCETYPE"></span>*resourceType*</span></span><br/>                                   | <span data-ttu-id="5db17-113">\[in \] jedem Objekttyp, der auf der Seite [Textur Objekt](dx-graphics-hlsl-to-type.md) aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="5db17-113">\[in\] Any object type listed in the [texture-object](dx-graphics-hlsl-to-type.md) page.</span></span><br/>                                                                                                                                                                     |
| <span data-ttu-id="5db17-114"><span id="resourceType_size_NN"></span><span id="resourcetype_size_nn"></span><span id="RESOURCETYPE_SIZE_NN"></span>*ResourceType- \[ Größe \] NN*</span><span class="sxs-lookup"><span data-stu-id="5db17-114"><span id="resourceType_size_NN"></span><span id="resourcetype_size_nn"></span><span id="RESOURCETYPE_SIZE_NN"></span>*resourceType\[size\]NN*</span></span><br/> | <span data-ttu-id="5db17-115">\[in \] einem Texture2D-oder Texture2DArray-Objekttyp (siehe [Textur-Objekt](dx-graphics-hlsl-to-type.md) Seite); *size* ist eine optionale ganze Zahl, die die Anzahl der Elemente im Array bezeichnet. *NN* ist eine ganze Zahl, die die Anzahl der multisamples bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="5db17-115">\[in\] A Texture2D or a Texture2DArray object type (see the [texture-object](dx-graphics-hlsl-to-type.md) page); *size* is an optional integer that denotes the number of elements in the array; *NN* is an integer that denotes the number of multisamples.</span></span><br/> |
| <span data-ttu-id="5db17-116"><span id="returnType_s_"></span><span id="returntype_s_"></span><span id="RETURNTYPE_S_"></span>*ReturnType (e)*</span><span class="sxs-lookup"><span data-stu-id="5db17-116"><span id="returnType_s_"></span><span id="returntype_s_"></span><span id="RETURNTYPE_S_"></span>*returnType(s)*</span></span><br/>                               | <span data-ttu-id="5db17-117">\[der \] Rückgabetyp pro Komponente, der eines der folgenden ist: unorm, snorm, Sint, uint oder float.</span><span class="sxs-lookup"><span data-stu-id="5db17-117">\[in\] Per-component return type which is one of the following: UNORM, SNORM, SINT, UINT, or FLOAT.</span></span> <span data-ttu-id="5db17-118">Die Anzahl der Rückgabe Typen kann bis zu 1 betragen (wenn alle Komponenten denselben Typ aufweisen), kann aber so viele wie vier sein.</span><span class="sxs-lookup"><span data-stu-id="5db17-118">The number of return types can be as few as 1 (if all components are the same type), but can be as many as four.</span></span><br/>                                          |



 

<span data-ttu-id="5db17-119">Der Zugriff auf eine Ressource erfolgt in HLSL mithilfe von " [Load](dx-graphics-hlsl-to-load.md)". auf eine Textur, auf die nicht mehr zugegriffen werden kann, kann auch mithilfe einer beliebigen HLSL- [Textur Objekt](dx-graphics-hlsl-to-type.md) -Beispiel Methode zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="5db17-119">A resource is accessed in HLSL using [load](dx-graphics-hlsl-to-load.md); a non-multisampled texture can also be accessed using any of the HLSL [texture object](dx-graphics-hlsl-to-type.md) sample methods.</span></span>

<span data-ttu-id="5db17-120">Wenn eine Ressource an eine Shader-Stufe gebunden ist, wird das Ressourcen Format mit dem Rückgabetyp überprüft.</span><span class="sxs-lookup"><span data-stu-id="5db17-120">If a resource is bound to a shader stage, the resource format will be validated against the return type.</span></span>

<span data-ttu-id="5db17-121">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="5db17-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="5db17-122">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="5db17-122">Vertex Shader</span></span> | <span data-ttu-id="5db17-123">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="5db17-123">Geometry Shader</span></span> | <span data-ttu-id="5db17-124">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="5db17-124">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="5db17-125">x</span><span class="sxs-lookup"><span data-stu-id="5db17-125">x</span></span>             | <span data-ttu-id="5db17-126">x</span><span class="sxs-lookup"><span data-stu-id="5db17-126">x</span></span>               | <span data-ttu-id="5db17-127">x</span><span class="sxs-lookup"><span data-stu-id="5db17-127">x</span></span>            |



 

<span data-ttu-id="5db17-128">Diese Anweisung ist enthalten, um das Debuggen eines Shaders in der Assembly zu unterstützen. Es ist nicht möglich, einen Shader mit Shadermodell 4 in der Assemblysprache zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5db17-128">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="5db17-129">Beispiel</span><span class="sxs-lookup"><span data-stu-id="5db17-129">Example</span></span>

<span data-ttu-id="5db17-130">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="5db17-130">Here is an example.</span></span>


```
dcl_resource t3, buffer, UNORM
```



## <a name="minimum-shader-model"></a><span data-ttu-id="5db17-131">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="5db17-131">Minimum Shader Model</span></span>

<span data-ttu-id="5db17-132">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5db17-132">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="5db17-133">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="5db17-133">Shader Model</span></span>                                              | <span data-ttu-id="5db17-134">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="5db17-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="5db17-135">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="5db17-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="5db17-136">ja</span><span class="sxs-lookup"><span data-stu-id="5db17-136">yes</span></span>       |
| [<span data-ttu-id="5db17-137">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="5db17-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="5db17-138">ja</span><span class="sxs-lookup"><span data-stu-id="5db17-138">yes</span></span>       |
| [<span data-ttu-id="5db17-139">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="5db17-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="5db17-140">ja</span><span class="sxs-lookup"><span data-stu-id="5db17-140">yes</span></span>       |
| [<span data-ttu-id="5db17-141">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5db17-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="5db17-142">nein</span><span class="sxs-lookup"><span data-stu-id="5db17-142">no</span></span>        |
| [<span data-ttu-id="5db17-143">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5db17-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="5db17-144">nein</span><span class="sxs-lookup"><span data-stu-id="5db17-144">no</span></span>        |
| [<span data-ttu-id="5db17-145">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5db17-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="5db17-146">nein</span><span class="sxs-lookup"><span data-stu-id="5db17-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="5db17-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5db17-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5db17-148">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5db17-148">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





