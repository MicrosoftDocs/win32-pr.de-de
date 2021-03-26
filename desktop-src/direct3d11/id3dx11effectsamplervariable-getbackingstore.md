---
title: ID3DX11EffectSamplerVariable getbackingstore-Methode (D3dx11effect. h)
description: Einen Zeiger auf eine Variable mit dem samplerstatus erhalten.
ms.assetid: b188fb86-f54b-481e-9110-7b8af70ff303
keywords:
- Getbackingstore-Methode Direct3D 11
- Getbackingstore-Methode Direct3D 11, ID3DX11EffectSamplerVariable-Schnittstelle
- ID3DX11EffectSamplerVariable Interface Direct3D 11, getbackingstore-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectSamplerVariable.GetBackingStore
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03f2d6ac3035d1dd2fd3aee8950135d7b4481862
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355366"
---
# <a name="id3dx11effectsamplervariablegetbackingstore-method"></a><span data-ttu-id="36c52-106">ID3DX11EffectSamplerVariable:: getbackingstore-Methode</span><span class="sxs-lookup"><span data-stu-id="36c52-106">ID3DX11EffectSamplerVariable::GetBackingStore method</span></span>

<span data-ttu-id="36c52-107">Einen Zeiger auf eine Variable mit dem samplerstatus erhalten.</span><span class="sxs-lookup"><span data-stu-id="36c52-107">Get a pointer to a variable that contains sampler state.</span></span>

## <a name="syntax"></a><span data-ttu-id="36c52-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="36c52-108">Syntax</span></span>


```C++
HRESULT GetBackingStore(
   UINT               Index,
   D3D11_SAMPLER_DESC *pSamplerDesc
);
```



## <a name="parameters"></a><span data-ttu-id="36c52-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="36c52-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36c52-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="36c52-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="36c52-111">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="36c52-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="36c52-112">Indizieren Sie in ein Array von Sampler-Beschreibungen.</span><span class="sxs-lookup"><span data-stu-id="36c52-112">Index into an array of sampler descriptions.</span></span> <span data-ttu-id="36c52-113">Wenn nur eine samplervariable vorhanden ist, verwenden Sie 0.</span><span class="sxs-lookup"><span data-stu-id="36c52-113">If there is only one sampler variable in the effect, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="36c52-114">*psamplerdebug*</span><span class="sxs-lookup"><span data-stu-id="36c52-114">*pSamplerDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="36c52-115">Type: **[ **D3D11 \_ Sampler \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)\***</span><span class="sxs-lookup"><span data-stu-id="36c52-115">Type: **[**D3D11\_SAMPLER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)\***</span></span>

<span data-ttu-id="36c52-116">Ein Zeiger auf eine samplerbeschreibung (siehe [**D3D11 \_ Sampler \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)Debug).</span><span class="sxs-lookup"><span data-stu-id="36c52-116">A pointer to a sampler description (see [**D3D11\_SAMPLER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36c52-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="36c52-117">Return value</span></span>

<span data-ttu-id="36c52-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="36c52-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="36c52-119">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="36c52-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="36c52-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="36c52-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="36c52-121">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="36c52-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="36c52-122">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="36c52-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="36c52-123">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="36c52-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="36c52-124">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="36c52-124">Requirements</span></span>



| <span data-ttu-id="36c52-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="36c52-125">Requirement</span></span> | <span data-ttu-id="36c52-126">Wert</span><span class="sxs-lookup"><span data-stu-id="36c52-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36c52-127">Header</span><span class="sxs-lookup"><span data-stu-id="36c52-127">Header</span></span><br/>  | <dl> <span data-ttu-id="36c52-128"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="36c52-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="36c52-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="36c52-129">Library</span></span><br/> | <dl> <span data-ttu-id="36c52-130"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="36c52-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36c52-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="36c52-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36c52-132">ID3DX11EffectSamplerVariable</span><span class="sxs-lookup"><span data-stu-id="36c52-132">ID3DX11EffectSamplerVariable</span></span>](id3dx11effectsamplervariable.md)
</dt> </dl>

 

