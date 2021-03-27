---
title: ID3DX11EffectShaderVariable GetInputSignatureElementDesc-Methode (D3dx11effect. h)
description: Erhalten Sie eine Beschreibung der Eingabe Signatur.
ms.assetid: 45b1fd25-1005-48fd-8a61-561ea2c273e5
keywords:
- GetInputSignatureElementDesc-Methode Direct3D 11
- GetInputSignatureElementDesc-Methode Direct3D 11, ID3DX11EffectShaderVariable-Schnittstelle
- ID3DX11EffectShaderVariable-Schnittstelle Direct3D 11, GetInputSignatureElementDesc-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetInputSignatureElementDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbf788370c26da1ba773d797de544b1a64750d90
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132421"
---
# <a name="id3dx11effectshadervariablegetinputsignatureelementdesc-method"></a><span data-ttu-id="2c01a-106">ID3DX11EffectShaderVariable:: GetInputSignatureElementDesc-Methode</span><span class="sxs-lookup"><span data-stu-id="2c01a-106">ID3DX11EffectShaderVariable::GetInputSignatureElementDesc method</span></span>

<span data-ttu-id="2c01a-107">Erhalten Sie eine Beschreibung der Eingabe Signatur.</span><span class="sxs-lookup"><span data-stu-id="2c01a-107">Get an input-signature description.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c01a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c01a-108">Syntax</span></span>


```C++
HRESULT GetInputSignatureElementDesc(
   UINT                           ShaderIndex,
   UINT                           Element,
   D3D11_SIGNATURE_PARAMETER_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="2c01a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="2c01a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c01a-110">*Shaderindex*</span><span class="sxs-lookup"><span data-stu-id="2c01a-110">*ShaderIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="2c01a-111">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2c01a-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="2c01a-112">Ein NULL basierter shaderindex.</span><span class="sxs-lookup"><span data-stu-id="2c01a-112">A zero-based shader index.</span></span>

</dd> <dt>

<span data-ttu-id="2c01a-113">*Element*</span><span class="sxs-lookup"><span data-stu-id="2c01a-113">*Element*</span></span> 
</dt> <dd>

<span data-ttu-id="2c01a-114">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2c01a-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="2c01a-115">Ein NULL basierter Shader-Element-Index.</span><span class="sxs-lookup"><span data-stu-id="2c01a-115">A zero-based shader-element index.</span></span>

</dd> <dt>

<span data-ttu-id="2c01a-116">*PDE SC*</span><span class="sxs-lookup"><span data-stu-id="2c01a-116">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="2c01a-117">Type: **[ **D3D11 \_ Signature \_ Parameter \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)\***</span><span class="sxs-lookup"><span data-stu-id="2c01a-117">Type: **[**D3D11\_SIGNATURE\_PARAMETER\_DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)\***</span></span>

<span data-ttu-id="2c01a-118">Ein Zeiger auf eine Parameter Beschreibung (siehe [**D3D11 \_ Signature \_ Parameter \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)).</span><span class="sxs-lookup"><span data-stu-id="2c01a-118">A pointer to a parameter description (see [**D3D11\_SIGNATURE\_PARAMETER\_DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c01a-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2c01a-119">Return value</span></span>

<span data-ttu-id="2c01a-120">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2c01a-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2c01a-121">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="2c01a-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2c01a-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2c01a-122">Remarks</span></span>

<span data-ttu-id="2c01a-123">Ein Effekt enthält einen oder mehrere Shader. jeder Shader hat eine Eingabe-und Ausgabe Signatur. Jede Signatur enthält ein oder mehrere-Elemente (oder-Parameter).</span><span class="sxs-lookup"><span data-stu-id="2c01a-123">An effect contains one or more shaders; each shader has an input and output signature; each signature contains one or more elements (or parameters).</span></span> <span data-ttu-id="2c01a-124">Der Shader-Index identifiziert den Shader, und der Element Index identifiziert das Element (oder den Parameter) in der shadersignatur.</span><span class="sxs-lookup"><span data-stu-id="2c01a-124">The shader index identifies the shader and the element index identifies the element (or parameter) in the shader signature.</span></span>

> [!Note]  
> <span data-ttu-id="2c01a-125">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="2c01a-125">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="2c01a-126">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2c01a-126">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="2c01a-127">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="2c01a-127">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2c01a-128">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="2c01a-128">Requirements</span></span>



| <span data-ttu-id="2c01a-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2c01a-129">Requirement</span></span> | <span data-ttu-id="2c01a-130">Wert</span><span class="sxs-lookup"><span data-stu-id="2c01a-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c01a-131">Header</span><span class="sxs-lookup"><span data-stu-id="2c01a-131">Header</span></span><br/>  | <dl> <span data-ttu-id="2c01a-132"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c01a-132"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="2c01a-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2c01a-133">Library</span></span><br/> | <dl> <span data-ttu-id="2c01a-134"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="2c01a-134"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c01a-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2c01a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c01a-136">ID3DX11EffectShaderVariable</span><span class="sxs-lookup"><span data-stu-id="2c01a-136">ID3DX11EffectShaderVariable</span></span>](id3dx11effectshadervariable.md)
</dt> </dl>

 

