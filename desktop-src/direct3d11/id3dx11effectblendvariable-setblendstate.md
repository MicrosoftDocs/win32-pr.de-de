---
title: ID3DX11EffectBlendVariable setblendstate-Methode (D3dx11effect. h)
description: Legt den Blend-Status eines Effekts fest.
ms.assetid: 46100721-65a3-46de-aa22-3e7e2fb7b960
keywords:
- Setblendstate-Methode Direct3D 11
- Setblendstate-Methode Direct3D 11, ID3DX11EffectBlendVariable-Schnittstelle
- ID3DX11EffectBlendVariable-Schnittstelle Direct3D 11, setblendstate-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectBlendVariable.SetBlendState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ce781f29c521df7b81821cb19a56e6fd3999310
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762216"
---
# <a name="id3dx11effectblendvariablesetblendstate-method"></a><span data-ttu-id="9595f-106">ID3DX11EffectBlendVariable:: setblendstate-Methode</span><span class="sxs-lookup"><span data-stu-id="9595f-106">ID3DX11EffectBlendVariable::SetBlendState method</span></span>

<span data-ttu-id="9595f-107">Legt den Blend-Status eines Effekts fest.</span><span class="sxs-lookup"><span data-stu-id="9595f-107">Sets an effect's blend-state.</span></span>

## <a name="syntax"></a><span data-ttu-id="9595f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9595f-108">Syntax</span></span>


```C++
HRESULT SetBlendState(
   UINT             Index,
   ID3D11BlendState *pBlendState
);
```



## <a name="parameters"></a><span data-ttu-id="9595f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9595f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9595f-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="9595f-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="9595f-111">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="9595f-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="9595f-112">Indizieren Sie in ein Array von Blend-State-Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="9595f-112">Index into an array of blend-state interfaces.</span></span> <span data-ttu-id="9595f-113">Wenn nur eine Blend-State-Schnittstelle vorhanden ist, verwenden Sie 0.</span><span class="sxs-lookup"><span data-stu-id="9595f-113">If there is only one blend-state interface, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="9595f-114">*pblendstate*</span><span class="sxs-lookup"><span data-stu-id="9595f-114">*pBlendState*</span></span> 
</dt> <dd>

<span data-ttu-id="9595f-115">Typ: **[ **ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate)\***</span><span class="sxs-lookup"><span data-stu-id="9595f-115">Type: **[**ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate)\***</span></span>

<span data-ttu-id="9595f-116">Ein Zeiger auf eine [**ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate) -Schnittstelle, die den festzulegenden Blend-Zustand enthält.</span><span class="sxs-lookup"><span data-stu-id="9595f-116">A pointer to an [**ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate) interface containing the blend-state to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9595f-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9595f-117">Return value</span></span>

<span data-ttu-id="9595f-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9595f-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9595f-119">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="9595f-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9595f-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9595f-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9595f-121">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="9595f-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="9595f-122">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9595f-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="9595f-123">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="9595f-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9595f-124">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="9595f-124">Requirements</span></span>



| <span data-ttu-id="9595f-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9595f-125">Requirement</span></span> | <span data-ttu-id="9595f-126">Wert</span><span class="sxs-lookup"><span data-stu-id="9595f-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9595f-127">Header</span><span class="sxs-lookup"><span data-stu-id="9595f-127">Header</span></span><br/>  | <dl> <span data-ttu-id="9595f-128"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="9595f-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="9595f-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9595f-129">Library</span></span><br/> | <dl> <span data-ttu-id="9595f-130"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="9595f-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9595f-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9595f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9595f-132">ID3DX11EffectBlendVariable</span><span class="sxs-lookup"><span data-stu-id="9595f-132">ID3DX11EffectBlendVariable</span></span>](id3dx11effectblendvariable.md)
</dt> </dl>

 

