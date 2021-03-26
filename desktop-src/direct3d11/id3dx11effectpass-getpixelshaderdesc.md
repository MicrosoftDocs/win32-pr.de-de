---
title: ID3DX11EffectPass getpixelshaderdesc-Methode (D3dx11effect. h)
description: Eine Pixel-shaderbeschreibung erhalten.
ms.assetid: 5772f197-7ac5-4492-9a41-eedb1a8b22c9
keywords:
- Getpixelshaderdesc-Methode Direct3D 11
- Getpixelshaderdesc-Methode Direct3D 11, ID3DX11EffectPass-Schnittstelle
- ID3DX11EffectPass-Schnittstelle Direct3D 11, getpixelshaderdesc-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetPixelShaderDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c04479a58eed0aa94616f0ffc092f17d52d9af4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982246"
---
# <a name="id3dx11effectpassgetpixelshaderdesc-method"></a><span data-ttu-id="c5c22-106">ID3DX11EffectPass:: getpixelshaderdesc-Methode</span><span class="sxs-lookup"><span data-stu-id="c5c22-106">ID3DX11EffectPass::GetPixelShaderDesc method</span></span>

<span data-ttu-id="c5c22-107">Eine Pixel-shaderbeschreibung erhalten.</span><span class="sxs-lookup"><span data-stu-id="c5c22-107">Get a pixel-shader description.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5c22-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5c22-108">Syntax</span></span>


```C++
HRESULT GetPixelShaderDesc(
   D3DX11_PASS_SHADER_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="c5c22-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c5c22-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5c22-110">*PDE SC*</span><span class="sxs-lookup"><span data-stu-id="c5c22-110">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="c5c22-111">Typ: **[ **Bibliothek d3dx11 \_ Pass- \_ Shader \_ DESC**](d3dx11-pass-shader-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="c5c22-111">Type: **[**D3DX11\_PASS\_SHADER\_DESC**](d3dx11-pass-shader-desc.md)\***</span></span>

<span data-ttu-id="c5c22-112">Ein Zeiger auf eine Pixel-Shader-Beschreibung (siehe [**Bibliothek d3dx11 \_ Pass \_ Shader \_**](d3dx11-pass-shader-desc.md)Debug).</span><span class="sxs-lookup"><span data-stu-id="c5c22-112">A pointer to a pixel-shader description (see [**D3DX11\_PASS\_SHADER\_DESC**](d3dx11-pass-shader-desc.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5c22-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c5c22-113">Return value</span></span>

<span data-ttu-id="c5c22-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c5c22-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c5c22-115">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="c5c22-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c5c22-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c5c22-116">Remarks</span></span>

<span data-ttu-id="c5c22-117">Ein Effekt Durchlauf kann renderzustandszuweisungen und shaderobjektzuweisungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="c5c22-117">An effect pass can contain render state assignments and shader object assignments.</span></span>

> [!Note]  
> <span data-ttu-id="c5c22-118">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="c5c22-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="c5c22-119">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c5c22-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="c5c22-120">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="c5c22-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c5c22-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="c5c22-121">Requirements</span></span>



| <span data-ttu-id="c5c22-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c5c22-122">Requirement</span></span> | <span data-ttu-id="c5c22-123">Wert</span><span class="sxs-lookup"><span data-stu-id="c5c22-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5c22-124">Header</span><span class="sxs-lookup"><span data-stu-id="c5c22-124">Header</span></span><br/>  | <dl> <span data-ttu-id="c5c22-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5c22-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="c5c22-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c5c22-126">Library</span></span><br/> | <dl> <span data-ttu-id="c5c22-127"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="c5c22-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5c22-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c5c22-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5c22-129">ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="c5c22-129">ID3DX11EffectPass</span></span>](id3dx11effectpass.md)
</dt> </dl>

 

 





