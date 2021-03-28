---
title: ID3DX11EffectShaderVariable getvertexshader-Methode (D3dx11effect. h)
description: Einen Vertex-Shader erhalten.
ms.assetid: 31a250ae-154b-43ce-97e3-6480f23dc4e2
keywords:
- Getvertexshader-Methode Direct3D 11
- Getvertexshader-Methode Direct3D 11, ID3DX11EffectShaderVariable-Schnittstelle
- ID3DX11EffectShaderVariable-Schnittstelle Direct3D 11, getvertexshader-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetVertexShader
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7977da5fc36a0c339069526db723e2c479b49d55
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104531022"
---
# <a name="id3dx11effectshadervariablegetvertexshader-method"></a><span data-ttu-id="889ac-106">ID3DX11EffectShaderVariable:: getvertexshader-Methode</span><span class="sxs-lookup"><span data-stu-id="889ac-106">ID3DX11EffectShaderVariable::GetVertexShader method</span></span>

<span data-ttu-id="889ac-107">Einen Vertex-Shader erhalten.</span><span class="sxs-lookup"><span data-stu-id="889ac-107">Get a vertex shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="889ac-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="889ac-108">Syntax</span></span>


```C++
HRESULT GetVertexShader(
   UINT               ShaderIndex,
   ID3D11VertexShader **ppVS
);
```



## <a name="parameters"></a><span data-ttu-id="889ac-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="889ac-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="889ac-110">*Shaderindex*</span><span class="sxs-lookup"><span data-stu-id="889ac-110">*ShaderIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="889ac-111">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="889ac-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="889ac-112">Ein NULL basierter Index.</span><span class="sxs-lookup"><span data-stu-id="889ac-112">A zero-based index.</span></span>

</dd> <dt>

<span data-ttu-id="889ac-113">*PPVs*</span><span class="sxs-lookup"><span data-stu-id="889ac-113">*ppVS*</span></span> 
</dt> <dd>

<span data-ttu-id="889ac-114">Typ: **[ **ID3D11VertexShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11vertexshader)\*\***</span><span class="sxs-lookup"><span data-stu-id="889ac-114">Type: **[**ID3D11VertexShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11vertexshader)\*\***</span></span>

<span data-ttu-id="889ac-115">Ein Zeiger auf einen [**ID3D11VertexShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11vertexshader) -Zeiger, der bei der Rückgabe auf den Scheitelpunkt-Shader festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="889ac-115">A pointer to an [**ID3D11VertexShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11vertexshader) pointer that will be set to the vertex shader on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="889ac-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="889ac-116">Return value</span></span>

<span data-ttu-id="889ac-117">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="889ac-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="889ac-118">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="889ac-118">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="889ac-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="889ac-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="889ac-120">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="889ac-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="889ac-121">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="889ac-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="889ac-122">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="889ac-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="889ac-123">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="889ac-123">Requirements</span></span>



| <span data-ttu-id="889ac-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="889ac-124">Requirement</span></span> | <span data-ttu-id="889ac-125">Wert</span><span class="sxs-lookup"><span data-stu-id="889ac-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="889ac-126">Header</span><span class="sxs-lookup"><span data-stu-id="889ac-126">Header</span></span><br/>  | <dl> <span data-ttu-id="889ac-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="889ac-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="889ac-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="889ac-128">Library</span></span><br/> | <dl> <span data-ttu-id="889ac-129"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="889ac-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="889ac-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="889ac-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="889ac-131">ID3DX11EffectShaderVariable</span><span class="sxs-lookup"><span data-stu-id="889ac-131">ID3DX11EffectShaderVariable</span></span>](id3dx11effectshadervariable.md)
</dt> </dl>

 

