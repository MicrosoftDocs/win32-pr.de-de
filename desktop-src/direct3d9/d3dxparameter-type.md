---
description: Beschreibt die Daten, die in der-Enumeration enthalten sind.
ms.assetid: 6d494fe6-fcd5-4e71-939c-257978b41499
title: D3DXPARAMETER_TYPE-Enumeration (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPARAMETER_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 16ff89feb694bb6aae550422b6f9546c2268fc07
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354156"
---
# <a name="d3dxparameter_type-enumeration"></a><span data-ttu-id="17c7e-103">D3DXPARAMETER- \_ Typenumeration</span><span class="sxs-lookup"><span data-stu-id="17c7e-103">D3DXPARAMETER\_TYPE enumeration</span></span>

<span data-ttu-id="17c7e-104">Beschreibt die Daten, die in der-Enumeration enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="17c7e-104">Describes the data contained by the enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="17c7e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="17c7e-105">Syntax</span></span>


```C++
typedef enum D3DXPARAMETER_TYPE { 
  D3DXPT_VOID,
  D3DXPT_BOOL,
  D3DXPT_INT,
  D3DXPT_FLOAT,
  D3DXPT_STRING,
  D3DXPT_TEXTURE,
  D3DXPT_TEXTURE1D,
  D3DXPT_TEXTURE2D,
  D3DXPT_TEXTURE3D,
  D3DXPT_TEXTURECUBE,
  D3DXPT_SAMPLER,
  D3DXPT_SAMPLER1D,
  D3DXPT_SAMPLER2D,
  D3DXPT_SAMPLER3D,
  D3DXPT_SAMPLERCUBE,
  D3DXPT_PIXELSHADER,
  D3DXPT_VERTEXSHADER,
  D3DXPT_PIXELFRAGMENT,
  D3DXPT_VERTEXFRAGMENT,
  D3DXPT_UNSUPPORTED,
  D3DXPT_FORCE_DWORD     = 0x7fffffff
} D3DXPARAMETER_TYPE, *LPD3DXPARAMETER_TYPE;
```



## <a name="constants"></a><span data-ttu-id="17c7e-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="17c7e-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="17c7e-107"><span id="D3DXPT_VOID"></span><span id="d3dxpt_void"></span>**D3DXPT \_ void**</span><span class="sxs-lookup"><span data-stu-id="17c7e-107"><span id="D3DXPT_VOID"></span><span id="d3dxpt_void"></span>**D3DXPT\_VOID**</span></span>
</dt> <dd>

<span data-ttu-id="17c7e-108">Der Parameter ist ein void-Zeiger.</span><span class="sxs-lookup"><span data-stu-id="17c7e-108">Parameter is a void pointer.</span></span>

</dd> <dt>

<span data-ttu-id="17c7e-109"><span id="D3DXPT_BOOL"></span><span id="d3dxpt_bool"></span>**D3DXPT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="17c7e-109"><span id="D3DXPT_BOOL"></span><span id="d3dxpt_bool"></span>**D3DXPT\_BOOL**</span></span>
</dt> <dd>

<span data-ttu-id="17c7e-110">Der-Parameter ist ein boolescher Wert.</span><span class="sxs-lookup"><span data-stu-id="17c7e-110">Parameter is a Boolean.</span></span> <span data-ttu-id="17c7e-111">Alle Werte ungleich 0 (null), die an [**ID3DXConstantTable:: SetBool**](id3dxconstanttable--setbool.md), [**ID3DXConstantTable:: setboolarray**](id3dxconstanttable--setboolarray.md), [**ID3DXConstantTable:: SetValue**](id3dxconstanttable--setvalue.md), [**ID3DXConstantTable:: setvector**](id3dxconstanttable--setvector.md)oder [**ID3DXConstantTable:: setvectorarray**](id3dxconstanttable--setvectorarray.md) weitergegeben werden, werden 1 (true) zugeordnet, bevor Sie in die Konstante Tabelle geschrieben werden. Andernfalls wird der Wert in der Konstanten Tabelle auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="17c7e-111">Any non-zero value passed into [**ID3DXConstantTable::SetBool**](id3dxconstanttable--setbool.md), [**ID3DXConstantTable::SetBoolArray**](id3dxconstanttable--setboolarray.md), [**ID3DXConstantTable::SetValue**](id3dxconstanttable--setvalue.md), [**ID3DXConstantTable::SetVector**](id3dxconstanttable--setvector.md), or [**ID3DXConstantTable::SetVectorArray**](id3dxconstanttable--setvectorarray.md) will be mapped to 1 (TRUE) before being written into the constant table; otherwise, the value will be set to 0 in the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="17c7e-112"><span id="D3DXPT_INT"></span><span id="d3dxpt_int"></span>**D3DXPT \_ int**</span><span class="sxs-lookup"><span data-stu-id="17c7e-112"><span id="D3DXPT_INT"></span><span id="d3dxpt_int"></span>**D3DXPT\_INT**</span></span>
</dt> <dd>

<span data-ttu-id="17c7e-113">Der-Parameter ist eine ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="17c7e-113">Parameter is an integer.</span></span> <span data-ttu-id="17c7e-114">Alle Gleit Komma Werte, die an [**ID3DXConstantTable:: SetValue**](id3dxconstanttable--setvalue.md), [**ID3DXConstantTable:: setvector**](id3dxconstanttable--setvector.md)oder [**ID3DXConstantTable:: setvector Array**](id3dxconstanttable--setvectorarray.md) weitergegeben werden, werden vor dem Schreiben in die Konstante Tabelle abgerundet (auf NULL Dezimalstellen).</span><span class="sxs-lookup"><span data-stu-id="17c7e-114">Any floating-point values passed into [**ID3DXConstantTable::SetValue**](id3dxconstanttable--setvalue.md), [**ID3DXConstantTable::SetVector**](id3dxconstanttable--setvector.md), or [**ID3DXConstantTable::SetVectorArray**](id3dxconstanttable--setvectorarray.md) will be rounded off (to zero decimal places) before being written into the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="17c7e-115"><span id="D3DXPT_FLOAT"></span><span id="d3dxpt_float"></span>**D3DXPT \_ float**</span><span class="sxs-lookup"><span data-stu-id="17c7e-115"><span id="D3DXPT_FLOAT"></span><span id="d3dxpt_float"></span>**D3DXPT\_FLOAT**</span></span>
</dt> <dd>

<span data-ttu-id="17c7e-116">Der-Parameter ist eine Gleit Komma Zahl.</span><span class="sxs-lookup"><span data-stu-id="17c7e-116">Parameter is a floating-point number.</span></span>

</dd> <dt>

<span data-ttu-id="17c7e-117"><span id="D3DXPT_STRING"></span><span id="d3dxpt_string"></span>**D3DXPT- \_ Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="17c7e-117"><span id="D3DXPT_STRING"></span><span id="d3dxpt_string"></span>**D3DXPT\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="17c7e-118">Der Parameter ist eine Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="17c7e-118">Parameter is a string.</span></span>

</dd> <dt>

<span data-ttu-id="17c7e-119"><span id="D3DXPT_TEXTURE"></span><span id="d3dxpt_texture"></span>**D3DXPT- \_ Textur**</span><span class="sxs-lookup"><span data-stu-id="17c7e-119"><span id="D3DXPT_TEXTURE"></span><span id="d3dxpt_texture"></span>**D3DXPT\_TEXTURE**</span></span>
</dt> <dd>

<span data-ttu-id="17c7e-120">Der-Parameter ist eine Textur.</span><span class="sxs-lookup"><span data-stu-id="17c7e-120">Parameter is a texture.</span></span>

</dd> <dt>

<span data-ttu-id="17c7e-121"><span id="D3DXPT_TEXTURE1D"></span><span id="d3dxpt_texture1d"></span>**D3DXPT \_ TEXTURE1D**</span><span class="sxs-lookup"><span data-stu-id="17c7e-121"><span id="D3DXPT_TEXTURE1D"></span><span id="d3dxpt_texture1d"></span>**D3DXPT\_TEXTURE1D**</span></span>
</dt> <dd>

<span data-ttu-id="17c7e-122">Der-Parameter ist eine 1D-Textur.</span><span class="sxs-lookup"><span data-stu-id="17c7e-122">Parameter is a 1D texture.</span></span>

</dd> <dt>

<span data-ttu-id="17c7e-123"><span id="D3DXPT_TEXTURE2D"></span><span id="d3dxpt_texture2d"></span>**D3DXPT \_ TEXTURE2D**</span><span class="sxs-lookup"><span data-stu-id="17c7e-123"><span id="D3DXPT_TEXTURE2D"></span><span id="d3dxpt_texture2d"></span>**D3DXPT\_TEXTURE2D**</span></span>
</dt> <dd>

<span data-ttu-id="17c7e-124">Der-Parameter ist eine 2D-Textur.</span><span class="sxs-lookup"><span data-stu-id="17c7e-124">Parameter is a 2D texture.</span></span>

</dd> <dt>

<span data-ttu-id="17c7e-125"><span id="D3DXPT_TEXTURE3D"></span><span id="d3dxpt_texture3d"></span>**D3DXPT \_ TEXTURE3D**</span><span class="sxs-lookup"><span data-stu-id="17c7e-125"><span id="D3DXPT_TEXTURE3D"></span><span id="d3dxpt_texture3d"></span>**D3DXPT\_TEXTURE3D**</span></span>
</dt> <dd>

<span data-ttu-id="17c7e-126">Der-Parameter ist eine 3D-Textur.</span><span class="sxs-lookup"><span data-stu-id="17c7e-126">Parameter is a 3D texture.</span></span>

</dd> <dt>

<span data-ttu-id="17c7e-127"><span id="D3DXPT_TEXTURECUBE"></span><span id="d3dxpt_texturecube"></span>**D3DXPT \_ texturecube**</span><span class="sxs-lookup"><span data-stu-id="17c7e-127"><span id="D3DXPT_TEXTURECUBE"></span><span id="d3dxpt_texturecube"></span>**D3DXPT\_TEXTURECUBE**</span></span>
</dt> <dd>

<span data-ttu-id="17c7e-128">Der-Parameter ist eine Cube-Textur.</span><span class="sxs-lookup"><span data-stu-id="17c7e-128">Parameter is a cube texture.</span></span>

</dd> <dt>

<span data-ttu-id="17c7e-129"><span id="D3DXPT_SAMPLER"></span><span id="d3dxpt_sampler"></span>**D3DXPT- \_ Sampler**</span><span class="sxs-lookup"><span data-stu-id="17c7e-129"><span id="D3DXPT_SAMPLER"></span><span id="d3dxpt_sampler"></span>**D3DXPT\_SAMPLER**</span></span>
</dt> <dd>

<span data-ttu-id="17c7e-130">Der Parameter ist ein Sampler.</span><span class="sxs-lookup"><span data-stu-id="17c7e-130">Parameter is a sampler.</span></span>

</dd> <dt>

<span data-ttu-id="17c7e-131"><span id="D3DXPT_SAMPLER1D"></span><span id="d3dxpt_sampler1d"></span>**D3DXPT \_ SAMPLER1D**</span><span class="sxs-lookup"><span data-stu-id="17c7e-131"><span id="D3DXPT_SAMPLER1D"></span><span id="d3dxpt_sampler1d"></span>**D3DXPT\_SAMPLER1D**</span></span>
</dt> <dd>

<span data-ttu-id="17c7e-132">Der Parameter ist ein 1D-Sampler.</span><span class="sxs-lookup"><span data-stu-id="17c7e-132">Parameter is a 1D sampler.</span></span>

</dd> <dt>

<span data-ttu-id="17c7e-133"><span id="D3DXPT_SAMPLER2D"></span><span id="d3dxpt_sampler2d"></span>**D3DXPT \_ SAMPLER2D**</span><span class="sxs-lookup"><span data-stu-id="17c7e-133"><span id="D3DXPT_SAMPLER2D"></span><span id="d3dxpt_sampler2d"></span>**D3DXPT\_SAMPLER2D**</span></span>
</dt> <dd>

<span data-ttu-id="17c7e-134">Der Parameter ist ein 2D-Sampler.</span><span class="sxs-lookup"><span data-stu-id="17c7e-134">Parameter is a 2D sampler.</span></span>

</dd> <dt>

<span data-ttu-id="17c7e-135"><span id="D3DXPT_SAMPLER3D"></span><span id="d3dxpt_sampler3d"></span>**D3DXPT \_ SAMPLER3D**</span><span class="sxs-lookup"><span data-stu-id="17c7e-135"><span id="D3DXPT_SAMPLER3D"></span><span id="d3dxpt_sampler3d"></span>**D3DXPT\_SAMPLER3D**</span></span>
</dt> <dd>

<span data-ttu-id="17c7e-136">Der Parameter ist ein 3D-Sampler.</span><span class="sxs-lookup"><span data-stu-id="17c7e-136">Parameter is a 3D sampler.</span></span>

</dd> <dt>

<span data-ttu-id="17c7e-137"><span id="D3DXPT_SAMPLERCUBE"></span><span id="d3dxpt_samplercube"></span>**D3DXPT \_ samplercube**</span><span class="sxs-lookup"><span data-stu-id="17c7e-137"><span id="D3DXPT_SAMPLERCUBE"></span><span id="d3dxpt_samplercube"></span>**D3DXPT\_SAMPLERCUBE**</span></span>
</dt> <dd>

<span data-ttu-id="17c7e-138">Der Parameter ist ein Cube-Sampler.</span><span class="sxs-lookup"><span data-stu-id="17c7e-138">Parameter is a cube sampler.</span></span>

</dd> <dt>

<span data-ttu-id="17c7e-139"><span id="D3DXPT_PIXELSHADER"></span><span id="d3dxpt_pixelshader"></span>**D3DXPT \_ Pixelshader**</span><span class="sxs-lookup"><span data-stu-id="17c7e-139"><span id="D3DXPT_PIXELSHADER"></span><span id="d3dxpt_pixelshader"></span>**D3DXPT\_PIXELSHADER**</span></span>
</dt> <dd>

<span data-ttu-id="17c7e-140">Der Parameter ist ein Pixelshader.</span><span class="sxs-lookup"><span data-stu-id="17c7e-140">Parameter is a pixel shader.</span></span>

</dd> <dt>

<span data-ttu-id="17c7e-141"><span id="D3DXPT_VERTEXSHADER"></span><span id="d3dxpt_vertexshader"></span>**D3DXPT \_ Vertexshader**</span><span class="sxs-lookup"><span data-stu-id="17c7e-141"><span id="D3DXPT_VERTEXSHADER"></span><span id="d3dxpt_vertexshader"></span>**D3DXPT\_VERTEXSHADER**</span></span>
</dt> <dd>

<span data-ttu-id="17c7e-142">Der Parameter ist ein Scheitelpunkt-Shader.</span><span class="sxs-lookup"><span data-stu-id="17c7e-142">Parameter is a vertex shader.</span></span>

</dd> <dt>

<span data-ttu-id="17c7e-143"><span id="D3DXPT_PIXELFRAGMENT"></span><span id="d3dxpt_pixelfragment"></span>**D3DXPT \_ Pixel Fragment**</span><span class="sxs-lookup"><span data-stu-id="17c7e-143"><span id="D3DXPT_PIXELFRAGMENT"></span><span id="d3dxpt_pixelfragment"></span>**D3DXPT\_PIXELFRAGMENT**</span></span>
</dt> <dd>

<span data-ttu-id="17c7e-144">Der Parameter ist ein Pixel-Shader-Fragment.</span><span class="sxs-lookup"><span data-stu-id="17c7e-144">Parameter is a pixel shader fragment.</span></span>

</dd> <dt>

<span data-ttu-id="17c7e-145"><span id="D3DXPT_VERTEXFRAGMENT"></span><span id="d3dxpt_vertexfragment"></span>**D3DXPT \_ vertexfragment**</span><span class="sxs-lookup"><span data-stu-id="17c7e-145"><span id="D3DXPT_VERTEXFRAGMENT"></span><span id="d3dxpt_vertexfragment"></span>**D3DXPT\_VERTEXFRAGMENT**</span></span>
</dt> <dd>

<span data-ttu-id="17c7e-146">Der Parameter ist ein Scheitelpunkt-Shader-Fragment.</span><span class="sxs-lookup"><span data-stu-id="17c7e-146">Parameter is a vertex shader fragment.</span></span>

</dd> <dt>

<span data-ttu-id="17c7e-147"><span id="D3DXPT_UNSUPPORTED"></span><span id="d3dxpt_unsupported"></span>**D3DXPT \_ nicht unterstützt**</span><span class="sxs-lookup"><span data-stu-id="17c7e-147"><span id="D3DXPT_UNSUPPORTED"></span><span id="d3dxpt_unsupported"></span>**D3DXPT\_UNSUPPORTED**</span></span>
</dt> <dd>

<span data-ttu-id="17c7e-148">Der-Parameter wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="17c7e-148">Parameter is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="17c7e-149"><span id="D3DXPT_FORCE_DWORD"></span><span id="d3dxpt_force_dword"></span>**D3DXPT \_ Erzwingen von \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="17c7e-149"><span id="D3DXPT_FORCE_DWORD"></span><span id="d3dxpt_force_dword"></span>**D3DXPT\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="17c7e-150">Erzwingt die Kompilierung dieser Enumeration in 32 Bits.</span><span class="sxs-lookup"><span data-stu-id="17c7e-150">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="17c7e-151">Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="17c7e-151">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="17c7e-152">Dieser Wert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="17c7e-152">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="17c7e-153">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="17c7e-153">Requirements</span></span>



| <span data-ttu-id="17c7e-154">Anforderung</span><span class="sxs-lookup"><span data-stu-id="17c7e-154">Requirement</span></span> | <span data-ttu-id="17c7e-155">Wert</span><span class="sxs-lookup"><span data-stu-id="17c7e-155">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="17c7e-156">Header</span><span class="sxs-lookup"><span data-stu-id="17c7e-156">Header</span></span><br/> | <dl> <span data-ttu-id="17c7e-157"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="17c7e-157"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17c7e-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="17c7e-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17c7e-159">D3DX-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="17c7e-159">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="17c7e-160">**D3DXSHADER \_ TypInfo**</span><span class="sxs-lookup"><span data-stu-id="17c7e-160">**D3DXSHADER\_TYPEINFO**</span></span>](d3dxshader-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="17c7e-161">**D3DXCONSTANT- \_ Abteilung**</span><span class="sxs-lookup"><span data-stu-id="17c7e-161">**D3DXCONSTANT\_DESC**</span></span>](d3dxconstant-desc.md)
</dt> </dl>

 

 




