---
title: ID3DX11EffectShaderVariable getdomainshader-Methode (D3dx11effect. h)
description: Einen Domänen-Shader erhalten.
ms.assetid: fd95a4f0-7df3-4098-843f-0a1e22209603
keywords:
- Getdomainshader-Methode Direct3D 11
- Getdomainshader-Methode Direct3D 11, ID3DX11EffectShaderVariable-Schnittstelle
- ID3DX11EffectShaderVariable-Schnittstelle Direct3D 11, getdomainshader-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetDomainShader
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b7f097fb950b60aaa9c7fa2d5b763b393d5e275
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219719"
---
# <a name="id3dx11effectshadervariablegetdomainshader-method"></a><span data-ttu-id="ff944-106">ID3DX11EffectShaderVariable:: getdomainshader-Methode</span><span class="sxs-lookup"><span data-stu-id="ff944-106">ID3DX11EffectShaderVariable::GetDomainShader method</span></span>

<span data-ttu-id="ff944-107">Einen Domänen-Shader erhalten.</span><span class="sxs-lookup"><span data-stu-id="ff944-107">Get a domain shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff944-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ff944-108">Syntax</span></span>


```C++
HRESULT GetDomainShader(
   UINT               ShaderIndex,
   ID3D11DomainShader **ppPS
);
```



## <a name="parameters"></a><span data-ttu-id="ff944-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ff944-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff944-110">*Shaderindex*</span><span class="sxs-lookup"><span data-stu-id="ff944-110">*ShaderIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="ff944-111">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ff944-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ff944-112">Der Index des Domänen-Shader.</span><span class="sxs-lookup"><span data-stu-id="ff944-112">Index of the domain shader.</span></span>

</dd> <dt>

<span data-ttu-id="ff944-113">*PPPs*</span><span class="sxs-lookup"><span data-stu-id="ff944-113">*ppPS*</span></span> 
</dt> <dd>

<span data-ttu-id="ff944-114">Typ: **[ **ID3D11DomainShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11domainshader)\*\***</span><span class="sxs-lookup"><span data-stu-id="ff944-114">Type: **[**ID3D11DomainShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11domainshader)\*\***</span></span>

<span data-ttu-id="ff944-115">Zeiger auf einen [**ID3D11DomainShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11domainshader) -Zeiger, der bei der Rückgabe auf den Domänen-Shader festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="ff944-115">Pointer to an [**ID3D11DomainShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11domainshader) pointer that will be set to the domain shader on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff944-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ff944-116">Return value</span></span>

<span data-ttu-id="ff944-117">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ff944-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ff944-118">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="ff944-118">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ff944-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ff944-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ff944-120">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="ff944-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="ff944-121">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ff944-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="ff944-122">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="ff944-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ff944-123">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="ff944-123">Requirements</span></span>



| <span data-ttu-id="ff944-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ff944-124">Requirement</span></span> | <span data-ttu-id="ff944-125">Wert</span><span class="sxs-lookup"><span data-stu-id="ff944-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff944-126">Header</span><span class="sxs-lookup"><span data-stu-id="ff944-126">Header</span></span><br/>  | <dl> <span data-ttu-id="ff944-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff944-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="ff944-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ff944-128">Library</span></span><br/> | <dl> <span data-ttu-id="ff944-129"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="ff944-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff944-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ff944-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff944-131">ID3DX11EffectShaderVariable</span><span class="sxs-lookup"><span data-stu-id="ff944-131">ID3DX11EffectShaderVariable</span></span>](id3dx11effectshadervariable.md)
</dt> </dl>

 

