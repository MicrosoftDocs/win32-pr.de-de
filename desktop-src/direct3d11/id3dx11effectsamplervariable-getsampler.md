---
title: ID3DX11EffectSamplerVariable getsampler-Methode (D3dx11effect. h)
description: Einen Zeiger auf eine samplerschnittstelle erhalten.
ms.assetid: ac2a05f1-e3ca-4ebf-b655-34133c4e50ac
keywords:
- Getsampler-Methode Direct3D 11
- Getsampler-Methode Direct3D 11, ID3DX11EffectSamplerVariable-Schnittstelle
- ID3DX11EffectSamplerVariable Interface Direct3D 11, getsampler-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectSamplerVariable.GetSampler
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f53260a07e544d5f69a9575851614f694b778619
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961746"
---
# <a name="id3dx11effectsamplervariablegetsampler-method"></a><span data-ttu-id="0fadc-106">ID3DX11EffectSamplerVariable:: getsampler-Methode</span><span class="sxs-lookup"><span data-stu-id="0fadc-106">ID3DX11EffectSamplerVariable::GetSampler method</span></span>

<span data-ttu-id="0fadc-107">Einen Zeiger auf eine samplerschnittstelle erhalten.</span><span class="sxs-lookup"><span data-stu-id="0fadc-107">Get a pointer to a sampler interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fadc-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0fadc-108">Syntax</span></span>


```C++
HRESULT GetSampler(
   UINT               Index,
   ID3D11SamplerState **ppSampler
);
```



## <a name="parameters"></a><span data-ttu-id="0fadc-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0fadc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fadc-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="0fadc-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="0fadc-111">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0fadc-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="0fadc-112">Indizieren Sie in ein Array von samplingschnittstellen.</span><span class="sxs-lookup"><span data-stu-id="0fadc-112">Index into an array of sampler interfaces.</span></span> <span data-ttu-id="0fadc-113">Wenn nur eine samplerschnittstelle vorhanden ist, verwenden Sie 0.</span><span class="sxs-lookup"><span data-stu-id="0fadc-113">If there is only one sampler interface, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="0fadc-114">*ppsampler*</span><span class="sxs-lookup"><span data-stu-id="0fadc-114">*ppSampler*</span></span> 
</dt> <dd>

<span data-ttu-id="0fadc-115">Typ: **[ **ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate)\*\***</span><span class="sxs-lookup"><span data-stu-id="0fadc-115">Type: **[**ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate)\*\***</span></span>

<span data-ttu-id="0fadc-116">Die Adresse eines Zeigers auf eine samplerschnittstelle (siehe [**ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate)).</span><span class="sxs-lookup"><span data-stu-id="0fadc-116">The address of a pointer to a sampler interface (see [**ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fadc-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0fadc-117">Return value</span></span>

<span data-ttu-id="0fadc-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0fadc-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0fadc-119">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="0fadc-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0fadc-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0fadc-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0fadc-121">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="0fadc-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="0fadc-122">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0fadc-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="0fadc-123">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="0fadc-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0fadc-124">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="0fadc-124">Requirements</span></span>



| <span data-ttu-id="0fadc-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0fadc-125">Requirement</span></span> | <span data-ttu-id="0fadc-126">Wert</span><span class="sxs-lookup"><span data-stu-id="0fadc-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fadc-127">Header</span><span class="sxs-lookup"><span data-stu-id="0fadc-127">Header</span></span><br/>  | <dl> <span data-ttu-id="0fadc-128"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="0fadc-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="0fadc-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0fadc-129">Library</span></span><br/> | <dl> <span data-ttu-id="0fadc-130"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="0fadc-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fadc-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0fadc-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fadc-132">ID3DX11EffectSamplerVariable</span><span class="sxs-lookup"><span data-stu-id="0fadc-132">ID3DX11EffectSamplerVariable</span></span>](id3dx11effectsamplervariable.md)
</dt> </dl>

 

