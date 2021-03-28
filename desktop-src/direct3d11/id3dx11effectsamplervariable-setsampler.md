---
title: ID3DX11EffectSamplerVariable setsampler-Methode (D3dx11effect. h)
description: Festlegen des samplerstatus
ms.assetid: 1826923d-d770-4d79-818a-a42a279f0a8c
keywords:
- Setsampler-Methode Direct3D 11
- Setsampler-Methode Direct3D 11, ID3DX11EffectSamplerVariable-Schnittstelle
- ID3DX11EffectSamplerVariable-Schnittstelle Direct3D 11, setsampler-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectSamplerVariable.SetSampler
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77a68adef00ac980b532e2fcd877e71eb63dc470
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355197"
---
# <a name="id3dx11effectsamplervariablesetsampler-method"></a><span data-ttu-id="4d8f8-106">ID3DX11EffectSamplerVariable:: setsampler-Methode</span><span class="sxs-lookup"><span data-stu-id="4d8f8-106">ID3DX11EffectSamplerVariable::SetSampler method</span></span>

<span data-ttu-id="4d8f8-107">Festlegen des samplerstatus</span><span class="sxs-lookup"><span data-stu-id="4d8f8-107">Set sampler state.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d8f8-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d8f8-108">Syntax</span></span>


```C++
HRESULT SetSampler(
   UINT               Index,
   ID3D11SamplerState *pSampler
);
```



## <a name="parameters"></a><span data-ttu-id="4d8f8-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d8f8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d8f8-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="4d8f8-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="4d8f8-111">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4d8f8-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="4d8f8-112">Indizieren Sie in ein Array von samplingschnittstellen.</span><span class="sxs-lookup"><span data-stu-id="4d8f8-112">Index into an array of sampler interfaces.</span></span> <span data-ttu-id="4d8f8-113">Wenn nur eine samplerschnittstelle vorhanden ist, verwenden Sie 0.</span><span class="sxs-lookup"><span data-stu-id="4d8f8-113">If there is only one sampler interface, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="4d8f8-114">*psampler*</span><span class="sxs-lookup"><span data-stu-id="4d8f8-114">*pSampler*</span></span> 
</dt> <dd>

<span data-ttu-id="4d8f8-115">Typ: **[ **ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate)\***</span><span class="sxs-lookup"><span data-stu-id="4d8f8-115">Type: **[**ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate)\***</span></span>

<span data-ttu-id="4d8f8-116">Zeiger auf eine [**ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate) -Schnittstelle mit dem samplerzustand.</span><span class="sxs-lookup"><span data-stu-id="4d8f8-116">Pointer to an [**ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate) interface containing the sampler state.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d8f8-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4d8f8-117">Return value</span></span>

<span data-ttu-id="4d8f8-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4d8f8-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4d8f8-119">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="4d8f8-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4d8f8-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4d8f8-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4d8f8-121">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="4d8f8-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="4d8f8-122">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4d8f8-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="4d8f8-123">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="4d8f8-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4d8f8-124">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="4d8f8-124">Requirements</span></span>



| <span data-ttu-id="4d8f8-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4d8f8-125">Requirement</span></span> | <span data-ttu-id="4d8f8-126">Wert</span><span class="sxs-lookup"><span data-stu-id="4d8f8-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d8f8-127">Header</span><span class="sxs-lookup"><span data-stu-id="4d8f8-127">Header</span></span><br/>  | <dl> <span data-ttu-id="4d8f8-128"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d8f8-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="4d8f8-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4d8f8-129">Library</span></span><br/> | <dl> <span data-ttu-id="4d8f8-130"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="4d8f8-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d8f8-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4d8f8-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d8f8-132">ID3DX11EffectSamplerVariable</span><span class="sxs-lookup"><span data-stu-id="4d8f8-132">ID3DX11EffectSamplerVariable</span></span>](id3dx11effectsamplervariable.md)
</dt> </dl>

 

