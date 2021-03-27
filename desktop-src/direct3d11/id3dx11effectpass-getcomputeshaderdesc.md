---
title: ID3DX11EffectPass getcomputeshaderdesc-Methode (D3dx11effect. h)
description: Eine COMPUTE-shaderbeschreibung erhalten.
ms.assetid: 9c3a702f-2016-4b1a-a832-d1bb968aec2d
keywords:
- Getcomputeshaderdesc-Methode Direct3D 11
- Getcomputeshaderdesc-Methode Direct3D 11, ID3DX11EffectPass-Schnittstelle
- ID3DX11EffectPass-Schnittstelle Direct3D 11, getcomputeshaderdesc-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetComputeShaderDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21cc13699553b0da60498209ddffd31a56607809
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961713"
---
# <a name="id3dx11effectpassgetcomputeshaderdesc-method"></a><span data-ttu-id="1f650-106">ID3DX11EffectPass:: getcomputeshaderdesc-Methode</span><span class="sxs-lookup"><span data-stu-id="1f650-106">ID3DX11EffectPass::GetComputeShaderDesc method</span></span>

<span data-ttu-id="1f650-107">Eine COMPUTE-shaderbeschreibung erhalten.</span><span class="sxs-lookup"><span data-stu-id="1f650-107">Get a compute-shader description.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f650-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f650-108">Syntax</span></span>


```C++
HRESULT GetComputeShaderDesc(
   D3DX11_PASS_SHADER_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="1f650-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="1f650-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f650-110">*PDE SC*</span><span class="sxs-lookup"><span data-stu-id="1f650-110">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="1f650-111">Typ: **[ **Bibliothek d3dx11 \_ Pass- \_ Shader \_ DESC**](d3dx11-pass-shader-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="1f650-111">Type: **[**D3DX11\_PASS\_SHADER\_DESC**](d3dx11-pass-shader-desc.md)\***</span></span>

<span data-ttu-id="1f650-112">Ein Zeiger auf eine COMPUTE-shaderbeschreibung (siehe [**Bibliothek d3dx11 \_ Pass \_ Shader \_**](d3dx11-pass-shader-desc.md)Debug).</span><span class="sxs-lookup"><span data-stu-id="1f650-112">A pointer to a compute-shader description (see [**D3DX11\_PASS\_SHADER\_DESC**](d3dx11-pass-shader-desc.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f650-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1f650-113">Return value</span></span>

<span data-ttu-id="1f650-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1f650-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1f650-115">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="1f650-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1f650-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1f650-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1f650-117">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="1f650-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="1f650-118">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1f650-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="1f650-119">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="1f650-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1f650-120">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="1f650-120">Requirements</span></span>



| <span data-ttu-id="1f650-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1f650-121">Requirement</span></span> | <span data-ttu-id="1f650-122">Wert</span><span class="sxs-lookup"><span data-stu-id="1f650-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f650-123">Header</span><span class="sxs-lookup"><span data-stu-id="1f650-123">Header</span></span><br/>  | <dl> <span data-ttu-id="1f650-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f650-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="1f650-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1f650-125">Library</span></span><br/> | <dl> <span data-ttu-id="1f650-126"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="1f650-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f650-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1f650-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f650-128">ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="1f650-128">ID3DX11EffectPass</span></span>](id3dx11effectpass.md)
</dt> </dl>

 

 





