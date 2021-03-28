---
title: ID3DX11EffectShaderVariable GetPatchConstantSignatureElementDesc-Methode (D3dx11effect. h)
description: Hier erhalten Sie eine Beschreibung für eine patchkonstante Signatur.
ms.assetid: 72a86cf6-ace2-4306-ac5c-37d888c087f7
keywords:
- GetPatchConstantSignatureElementDesc-Methode Direct3D 11
- GetPatchConstantSignatureElementDesc-Methode Direct3D 11, ID3DX11EffectShaderVariable-Schnittstelle
- ID3DX11EffectShaderVariable-Schnittstelle Direct3D 11, GetPatchConstantSignatureElementDesc-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetPatchConstantSignatureElementDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4fcbc8f7c1bc34b0da42dd08c255a04a6d2fc83
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996162"
---
# <a name="id3dx11effectshadervariablegetpatchconstantsignatureelementdesc-method"></a><span data-ttu-id="c2a6d-106">ID3DX11EffectShaderVariable:: GetPatchConstantSignatureElementDesc-Methode</span><span class="sxs-lookup"><span data-stu-id="c2a6d-106">ID3DX11EffectShaderVariable::GetPatchConstantSignatureElementDesc method</span></span>

<span data-ttu-id="c2a6d-107">Hier erhalten Sie eine Beschreibung für eine patchkonstante Signatur.</span><span class="sxs-lookup"><span data-stu-id="c2a6d-107">Get a patch constant signature description.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2a6d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2a6d-108">Syntax</span></span>


```C++
HRESULT GetPatchConstantSignatureElementDesc(
   UINT                           ShaderIndex,
   UINT                           Element,
   D3D11_SIGNATURE_PARAMETER_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="c2a6d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c2a6d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2a6d-110">*Shaderindex*</span><span class="sxs-lookup"><span data-stu-id="c2a6d-110">*ShaderIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="c2a6d-111">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c2a6d-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c2a6d-112">Ein NULL basierter shaderindex.</span><span class="sxs-lookup"><span data-stu-id="c2a6d-112">A zero-based shader index.</span></span>

</dd> <dt>

<span data-ttu-id="c2a6d-113">*Element*</span><span class="sxs-lookup"><span data-stu-id="c2a6d-113">*Element*</span></span> 
</dt> <dd>

<span data-ttu-id="c2a6d-114">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c2a6d-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c2a6d-115">Ein NULL basierter Element Index.</span><span class="sxs-lookup"><span data-stu-id="c2a6d-115">A zero-based element index.</span></span>

</dd> <dt>

<span data-ttu-id="c2a6d-116">*PDE SC*</span><span class="sxs-lookup"><span data-stu-id="c2a6d-116">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="c2a6d-117">Type: **[ **D3D11 \_ Signature \_ Parameter \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)\***</span><span class="sxs-lookup"><span data-stu-id="c2a6d-117">Type: **[**D3D11\_SIGNATURE\_PARAMETER\_DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)\***</span></span>

<span data-ttu-id="c2a6d-118">Ein Zeiger auf eine Parameter Beschreibung (siehe [**D3D11 \_ Signature \_ Parameter \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)).</span><span class="sxs-lookup"><span data-stu-id="c2a6d-118">A pointer to a parameter description (see [**D3D11\_SIGNATURE\_PARAMETER\_DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2a6d-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c2a6d-119">Return value</span></span>

<span data-ttu-id="c2a6d-120">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c2a6d-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c2a6d-121">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="c2a6d-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c2a6d-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c2a6d-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c2a6d-123">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="c2a6d-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="c2a6d-124">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c2a6d-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="c2a6d-125">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="c2a6d-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c2a6d-126">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="c2a6d-126">Requirements</span></span>



| <span data-ttu-id="c2a6d-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c2a6d-127">Requirement</span></span> | <span data-ttu-id="c2a6d-128">Wert</span><span class="sxs-lookup"><span data-stu-id="c2a6d-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2a6d-129">Header</span><span class="sxs-lookup"><span data-stu-id="c2a6d-129">Header</span></span><br/>  | <dl> <span data-ttu-id="c2a6d-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2a6d-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="c2a6d-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c2a6d-131">Library</span></span><br/> | <dl> <span data-ttu-id="c2a6d-132"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="c2a6d-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2a6d-133">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c2a6d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2a6d-134">ID3DX11EffectShaderVariable</span><span class="sxs-lookup"><span data-stu-id="c2a6d-134">ID3DX11EffectShaderVariable</span></span>](id3dx11effectshadervariable.md)
</dt> </dl>

 

