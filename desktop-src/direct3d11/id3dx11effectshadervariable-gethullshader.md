---
title: ID3DX11EffectShaderVariable gethullshader-Methode (D3dx11effect. h)
description: Einen Hull-Shader erhalten.
ms.assetid: 18b2a8fc-2c53-4858-9aaa-00d0dc86adee
keywords:
- Gethullshader-Methode Direct3D 11
- Gethullshader-Methode Direct3D 11, ID3DX11EffectShaderVariable-Schnittstelle
- ID3DX11EffectShaderVariable Interface Direct3D 11, gethullshader-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetHullShader
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7eac8e6e095eb1ddbba93d68bec87e85e0c4e22
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996290"
---
# <a name="id3dx11effectshadervariablegethullshader-method"></a><span data-ttu-id="f7e08-106">ID3DX11EffectShaderVariable:: gethullshader-Methode</span><span class="sxs-lookup"><span data-stu-id="f7e08-106">ID3DX11EffectShaderVariable::GetHullShader method</span></span>

<span data-ttu-id="f7e08-107">Einen Hull-Shader erhalten.</span><span class="sxs-lookup"><span data-stu-id="f7e08-107">Get a hull shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7e08-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f7e08-108">Syntax</span></span>


```C++
HRESULT GetHullShader(
   UINT             ShaderIndex,
   ID3D11HullShader **ppPS
);
```



## <a name="parameters"></a><span data-ttu-id="f7e08-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f7e08-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7e08-110">*Shaderindex*</span><span class="sxs-lookup"><span data-stu-id="f7e08-110">*ShaderIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="f7e08-111">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f7e08-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f7e08-112">Der Index des Shaders.</span><span class="sxs-lookup"><span data-stu-id="f7e08-112">Index of the shader.</span></span>

</dd> <dt>

<span data-ttu-id="f7e08-113">*PPPs*</span><span class="sxs-lookup"><span data-stu-id="f7e08-113">*ppPS*</span></span> 
</dt> <dd>

<span data-ttu-id="f7e08-114">Typ: **[ **ID3D11HullShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11hullshader)\*\***</span><span class="sxs-lookup"><span data-stu-id="f7e08-114">Type: **[**ID3D11HullShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11hullshader)\*\***</span></span>

<span data-ttu-id="f7e08-115">Ein Zeiger auf einen [**ID3D11HullShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11hullshader) -Zeiger, der bei der Rückgabe auf den Hull-Shader festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="f7e08-115">A pointer to an [**ID3D11HullShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11hullshader) pointer that will be set to the hull shader on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7e08-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f7e08-116">Return value</span></span>

<span data-ttu-id="f7e08-117">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f7e08-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f7e08-118">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="f7e08-118">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f7e08-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f7e08-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f7e08-120">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="f7e08-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="f7e08-121">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f7e08-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="f7e08-122">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="f7e08-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f7e08-123">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="f7e08-123">Requirements</span></span>



| <span data-ttu-id="f7e08-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f7e08-124">Requirement</span></span> | <span data-ttu-id="f7e08-125">Wert</span><span class="sxs-lookup"><span data-stu-id="f7e08-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7e08-126">Header</span><span class="sxs-lookup"><span data-stu-id="f7e08-126">Header</span></span><br/>  | <dl> <span data-ttu-id="f7e08-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7e08-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="f7e08-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f7e08-128">Library</span></span><br/> | <dl> <span data-ttu-id="f7e08-129"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="f7e08-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7e08-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f7e08-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7e08-131">ID3DX11EffectShaderVariable</span><span class="sxs-lookup"><span data-stu-id="f7e08-131">ID3DX11EffectShaderVariable</span></span>](id3dx11effectshadervariable.md)
</dt> </dl>

 

