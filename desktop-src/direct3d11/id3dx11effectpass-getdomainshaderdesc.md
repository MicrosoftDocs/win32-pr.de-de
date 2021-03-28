---
title: ID3DX11EffectPass getdomainshaderdesc-Methode (D3dx11effect. h)
description: Eine Domänen-Shader-Beschreibung erhalten.
ms.assetid: 02109930-0922-46b8-9381-bb75abd0c4a0
keywords:
- Getdomainshaderdesc-Methode Direct3D 11
- Getdomainshaderdesc-Methode Direct3D 11, ID3DX11EffectPass-Schnittstelle
- ID3DX11EffectPass-Schnittstelle Direct3D 11, getdomainshaderdesc-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetDomainShaderDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2157134d97332fc9c76267f5e0db49d2c40e96a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982432"
---
# <a name="id3dx11effectpassgetdomainshaderdesc-method"></a><span data-ttu-id="a8766-106">ID3DX11EffectPass:: getdomainshaderdesc-Methode</span><span class="sxs-lookup"><span data-stu-id="a8766-106">ID3DX11EffectPass::GetDomainShaderDesc method</span></span>

<span data-ttu-id="a8766-107">Eine Domänen-Shader-Beschreibung erhalten.</span><span class="sxs-lookup"><span data-stu-id="a8766-107">Get a domain-shader description.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8766-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8766-108">Syntax</span></span>


```C++
HRESULT GetDomainShaderDesc(
   D3DX11_PASS_SHADER_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="a8766-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8766-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8766-110">*PDE SC*</span><span class="sxs-lookup"><span data-stu-id="a8766-110">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="a8766-111">Typ: **[ **Bibliothek d3dx11 \_ Pass- \_ Shader \_ DESC**](d3dx11-pass-shader-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="a8766-111">Type: **[**D3DX11\_PASS\_SHADER\_DESC**](d3dx11-pass-shader-desc.md)\***</span></span>

<span data-ttu-id="a8766-112">Ein Zeiger auf eine Domänen-Shader-Beschreibung (siehe [**Bibliothek d3dx11 \_ Pass \_ Shader \_ DESC**](d3dx11-pass-shader-desc.md)).</span><span class="sxs-lookup"><span data-stu-id="a8766-112">A pointer to a domain-shader description (see [**D3DX11\_PASS\_SHADER\_DESC**](d3dx11-pass-shader-desc.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8766-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a8766-113">Return value</span></span>

<span data-ttu-id="a8766-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a8766-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a8766-115">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="a8766-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a8766-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a8766-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a8766-117">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="a8766-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="a8766-118">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a8766-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="a8766-119">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="a8766-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a8766-120">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="a8766-120">Requirements</span></span>



| <span data-ttu-id="a8766-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a8766-121">Requirement</span></span> | <span data-ttu-id="a8766-122">Wert</span><span class="sxs-lookup"><span data-stu-id="a8766-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8766-123">Header</span><span class="sxs-lookup"><span data-stu-id="a8766-123">Header</span></span><br/>  | <dl> <span data-ttu-id="a8766-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8766-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="a8766-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a8766-125">Library</span></span><br/> | <dl> <span data-ttu-id="a8766-126"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="a8766-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8766-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a8766-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8766-128">ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="a8766-128">ID3DX11EffectPass</span></span>](id3dx11effectpass.md)
</dt> </dl>

 

 





