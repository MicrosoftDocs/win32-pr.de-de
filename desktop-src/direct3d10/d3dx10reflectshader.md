---
description: Diese Funktion, die ein Shader-Reflektionsobjekt zum Abrufen von Informationen über einen kompilierten Shader erstellt, ist nicht mehr vorhanden. Verwenden Sie stattdessen D3DReflect oder D3D11Reflect.
ms.assetid: 7090418c-1940-4f07-b075-937e3399613c
title: D3DX10ReflectShader-Funktion (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10ReflectShader
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 15201bcbde2792bbd31cbf4dad7b87d7ddac5053
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355194"
---
# <a name="d3dx10reflectshader-function"></a><span data-ttu-id="f2606-104">D3DX10ReflectShader-Funktion</span><span class="sxs-lookup"><span data-stu-id="f2606-104">D3DX10ReflectShader function</span></span>

<span data-ttu-id="f2606-105">Diese Funktion, die ein Shader-Reflektionsobjekt zum Abrufen von Informationen über einen kompilierten Shader erstellt, ist nicht mehr vorhanden.</span><span class="sxs-lookup"><span data-stu-id="f2606-105">This function -- which creates a shader-reflection object for retrieving information about a compiled shader -- no longer exists.</span></span> <span data-ttu-id="f2606-106">Verwenden Sie stattdessen [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) oder [**D3D11Reflect**](../direct3dhlsl/d3d11reflect.md).</span><span class="sxs-lookup"><span data-stu-id="f2606-106">Instead, use [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) or [**D3D11Reflect**](../direct3dhlsl/d3d11reflect.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f2606-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2606-107">Syntax</span></span>


```C++
HRESULT D3DX10ReflectShader(
  _In_  const void                    *pShaderBytecode,
  _In_        SIZE_T                  BytecodeLength,
  _Out_       ID3D10ShaderReflection1 **ppReflector
);
```



## <a name="parameters"></a><span data-ttu-id="f2606-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f2606-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2606-109">*pshaderbytecode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f2606-109">*pShaderBytecode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2606-110">Typ: Konstante **void \***</span><span class="sxs-lookup"><span data-stu-id="f2606-110">Type: **const void\***</span></span>

<span data-ttu-id="f2606-111">Ein Zeiger auf den kompilierten Shader.</span><span class="sxs-lookup"><span data-stu-id="f2606-111">A pointer to the compiled shader.</span></span> <span data-ttu-id="f2606-112">Informationen zum Aufrufen dieses Zeigers finden Sie unter [Getting a Pointer to a-kompilierter Shader](../direct3dhlsl/dx-graphics-hlsl-using-shaders-10.md).</span><span class="sxs-lookup"><span data-stu-id="f2606-112">To get this pointer see [Getting a Pointer to a Compiled Shader](../direct3dhlsl/dx-graphics-hlsl-using-shaders-10.md).</span></span>

</dd> <dt>

<span data-ttu-id="f2606-113">*Bytecodelta ength* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f2606-113">*BytecodeLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2606-114">Typ: **[ **Größe \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f2606-114">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f2606-115">Länge von pshaderbytecode.</span><span class="sxs-lookup"><span data-stu-id="f2606-115">Length of pShaderBytecode.</span></span>

</dd> <dt>

<span data-ttu-id="f2606-116">*ppreflector* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f2606-116">*ppReflector* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f2606-117">Typ: **[ **ID3D10ShaderReflection1**](/windows/desktop/api/D3D10_1Shader/nn-d3d10_1shader-id3d10shaderreflection1)\*\***</span><span class="sxs-lookup"><span data-stu-id="f2606-117">Type: **[**ID3D10ShaderReflection1**](/windows/desktop/api/D3D10_1Shader/nn-d3d10_1shader-id3d10shaderreflection1)\*\***</span></span>

<span data-ttu-id="f2606-118">Adresse einer Shader Reflection-Schnittstelle (siehe [**ID3D10ShaderReflection1 Interface**](/windows/desktop/api/D3D10_1Shader/nn-d3d10_1shader-id3d10shaderreflection1).)</span><span class="sxs-lookup"><span data-stu-id="f2606-118">Address of a shader reflection interface (see [**ID3D10ShaderReflection1 Interface**](/windows/desktop/api/D3D10_1Shader/nn-d3d10_1shader-id3d10shaderreflection1).)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2606-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f2606-119">Return value</span></span>

<span data-ttu-id="f2606-120">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f2606-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f2606-121">Gibt einen der folgenden [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="f2606-121">Returns one of the following [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f2606-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f2606-122">Remarks</span></span>

<span data-ttu-id="f2606-123">Im folgenden finden Sie ein Beispiel für das Erstellen eines shaderreflektionsobjekt.</span><span class="sxs-lookup"><span data-stu-id="f2606-123">Here is an example of creating a shader-reflection object.</span></span> <span data-ttu-id="f2606-124">Im Beispiel wird davon ausgegangen, dass Sie mit einem kompilierten Shader beginnen (angezeigt als</span><span class="sxs-lookup"><span data-stu-id="f2606-124">The example assumes you start with a compiled shader (shown as</span></span>


```
pVSBuf
```



<span data-ttu-id="f2606-125">die Sie in [HLSLWithoutFX10 Sample](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)sehen können).</span><span class="sxs-lookup"><span data-stu-id="f2606-125">which you can see in [HLSLWithoutFX10 Sample](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)).</span></span>


```
ID3D10ShaderReflection1* pIShaderReflection1 = NULL;
D3D10_SHADER_DESC desc;
hr = D3D10ReflectShader( (void*) pVSBuf->GetBufferPointer(), pVSBuf->GetBufferSize(),
    &pIShaderReflection1 );
if( pIShaderReflection1 )
{
    pIShaderReflection1->GetDesc( &desc );
}
```



## <a name="requirements"></a><span data-ttu-id="f2606-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f2606-126">Requirements</span></span>



| <span data-ttu-id="f2606-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f2606-127">Requirement</span></span> | <span data-ttu-id="f2606-128">Wert</span><span class="sxs-lookup"><span data-stu-id="f2606-128">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2606-129">Header</span><span class="sxs-lookup"><span data-stu-id="f2606-129">Header</span></span><br/> | <dl> <span data-ttu-id="f2606-130"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2606-130"><dt>D3DX10Core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2606-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f2606-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2606-132">Universell Funktionen</span><span class="sxs-lookup"><span data-stu-id="f2606-132">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
