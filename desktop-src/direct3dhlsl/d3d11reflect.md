---
title: D3D11Reflect-Funktion
description: Ruft einen Zeiger auf eine reflektionseschnittstelle ab.
ms.assetid: 855097c7-988b-4ab6-90c5-e5dd0bc9e1e0
keywords:
- D3D11Reflect-Funktion (HLSL)
topic_type:
- apiref
api_name:
- D3D11Reflect
api_location:
- D3dcompiler_47.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e54a1f388ebb122398ad33c3a8d942496fa55393
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132397"
---
# <a name="d3d11reflect-function"></a><span data-ttu-id="eefab-104">D3D11Reflect-Funktion</span><span class="sxs-lookup"><span data-stu-id="eefab-104">D3D11Reflect function</span></span>

<span data-ttu-id="eefab-105">Ruft einen Zeiger auf eine reflektionseschnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="eefab-105">Gets a pointer to a reflection interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="eefab-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="eefab-106">Syntax</span></span>

``` syntax
HRESULT D3D11Reflect(
  in  LPCVOID pSrcData,
  in  SIZE_T SrcDataSize,
  out ID3D11ShaderReflection ppReflector
);
```

## <a name="parameters"></a><span data-ttu-id="eefab-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="eefab-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eefab-108">*pSrcData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eefab-108">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eefab-109">Geben Sie Folgendes ein: **[ **lpcvoid**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="eefab-109">Type: **[**LPCVOID**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="eefab-110">Ein Zeiger auf Quelldaten als kompilierter HLSL-Code.</span><span class="sxs-lookup"><span data-stu-id="eefab-110">A pointer to source data as compiled HLSL code.</span></span>

</dd> <dt>

<span data-ttu-id="eefab-111">*Srcdatasize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eefab-111">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eefab-112">Typ: **[ **Größe \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="eefab-112">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="eefab-113">Länge von *pSrcData*.</span><span class="sxs-lookup"><span data-stu-id="eefab-113">Length of *pSrcData*.</span></span>

</dd> <dt>

<span data-ttu-id="eefab-114">*ppreflector* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="eefab-114">*ppReflector* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eefab-115">Typ: **[ **ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection)\*\***</span><span class="sxs-lookup"><span data-stu-id="eefab-115">Type: **[**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection)\*\***</span></span>

<span data-ttu-id="eefab-116">Die Adresse eines Zeigers auf die [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="eefab-116">The address of a pointer to the [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eefab-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eefab-117">Return value</span></span>

<span data-ttu-id="eefab-118">Typ: **[ **HRESULT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="eefab-118">Type: **[**HRESULT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="eefab-119">Gibt einen der Rückgabecodes zurück, die im Thema [Direct3D 11 Return Codes](/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues)beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="eefab-119">Returns one of the return codes described in the topic [Direct3D 11 Return Codes](/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues).</span></span>

## <a name="remarks"></a><span data-ttu-id="eefab-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eefab-120">Remarks</span></span>

<span data-ttu-id="eefab-121">Die Inline- **D3D11Reflect** -Compilerfunktion ist ein Wrapper für die [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) -Compilerfunktion.</span><span class="sxs-lookup"><span data-stu-id="eefab-121">The inline **D3D11Reflect** compiler function is a wrapper for the [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) compiler function.</span></span> <span data-ttu-id="eefab-122">**D3D11Reflect** kann nur eine [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) -Schnittstelle aus einem Shader abrufen.</span><span class="sxs-lookup"><span data-stu-id="eefab-122">**D3D11Reflect** can retrieve only a [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) interface from a shader.</span></span> <span data-ttu-id="eefab-123">**D3DReflect** kann eine **ID3D11ShaderReflection** -Schnittstelle oder eine Direct3D 10-oder Direct3D 10,1 Reflection-Schnittstelle abrufen, z. b. [**ID3D10ShaderReflection**](/windows/desktop/api/d3d10shader/nn-d3d10shader-id3d10shaderreflection).</span><span class="sxs-lookup"><span data-stu-id="eefab-123">**D3DReflect** can retrieve a **ID3D11ShaderReflection** interface or a Direct3D 10 or Direct3D 10.1 reflection interface, for example, [**ID3D10ShaderReflection**](/windows/desktop/api/d3d10shader/nn-d3d10shader-id3d10shaderreflection).</span></span>

<span data-ttu-id="eefab-124">Shader-Code enthält Metadaten, die mithilfe der reflektionsapis überprüft werden können.</span><span class="sxs-lookup"><span data-stu-id="eefab-124">Shader code contains metadata that can be inspected using the reflection APIs.</span></span>

<span data-ttu-id="eefab-125">Der folgende Code zeigt, wie eine [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) -Schnittstelle aus einem Shader abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="eefab-125">The following code shows how to retrieve a [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) interface from a shader.</span></span>


```C++
pd3dDevice->CreatePixelShader( pPixelShaderBuffer->GetBufferPointer(),
                               pPixelShaderBuffer->GetBufferSize(), g_pPSClassLinkage, &g_pPixelShader );

ID3D11ShaderReflection* pReflector = NULL; 
D3D11Reflect( pPixelShaderBuffer->GetBufferPointer(), pPixelShaderBuffer->GetBufferSize(), 
            &pReflector);
```



## <a name="requirements"></a><span data-ttu-id="eefab-126">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="eefab-126">Requirements</span></span>



| <span data-ttu-id="eefab-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eefab-127">Requirement</span></span> | <span data-ttu-id="eefab-128">Wert</span><span class="sxs-lookup"><span data-stu-id="eefab-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eefab-129">Header</span><span class="sxs-lookup"><span data-stu-id="eefab-129">Header</span></span><br/>  | <dl> <span data-ttu-id="eefab-130"><dt>D3DCompiler. INL</dt></span><span class="sxs-lookup"><span data-stu-id="eefab-130"><dt>D3DCompiler.inl</dt></span></span> </dl>     |
| <span data-ttu-id="eefab-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="eefab-131">Library</span></span><br/> | <dl> <span data-ttu-id="eefab-132"><dt>D3dcompiler \_ 47. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eefab-132"><dt>D3dcompiler\_47.lib</dt></span></span> </dl> |
| <span data-ttu-id="eefab-133">DLL</span><span class="sxs-lookup"><span data-stu-id="eefab-133">DLL</span></span><br/>     | <dl> <span data-ttu-id="eefab-134"><dt>D3dcompiler \_47.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eefab-134"><dt>D3dcompiler\_47.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eefab-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eefab-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eefab-136">Funktionen</span><span class="sxs-lookup"><span data-stu-id="eefab-136">Functions</span></span>](dx-graphics-d3dcompiler-reference-functions.md)
</dt> </dl>

 

