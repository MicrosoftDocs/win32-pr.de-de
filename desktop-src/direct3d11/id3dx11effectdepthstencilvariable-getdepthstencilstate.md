---
title: ID3DX11EffectDepthStencilVariable getdepthstencilstate-Methode (D3dx11effect. h)
description: Einen Zeiger auf eine tiefen Schablone-Schnittstelle erhalten.
ms.assetid: 3e8f7fc6-960c-45f5-9276-9aa2a5e7a6c9
keywords:
- Getdepthstencilstate-Methode Direct3D 11
- Getdepthstencilstate-Methode Direct3D 11, ID3DX11EffectDepthStencilVariable-Schnittstelle
- ID3DX11EffectDepthStencilVariable-Schnittstelle Direct3D 11, getdepthstencilstate-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilVariable.GetDepthStencilState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e9276c7a126d5441361a4d449c4ee2ece70d995
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982456"
---
# <a name="id3dx11effectdepthstencilvariablegetdepthstencilstate-method"></a><span data-ttu-id="c3994-106">ID3DX11EffectDepthStencilVariable:: getdepthstencilstate-Methode</span><span class="sxs-lookup"><span data-stu-id="c3994-106">ID3DX11EffectDepthStencilVariable::GetDepthStencilState method</span></span>

<span data-ttu-id="c3994-107">Einen Zeiger auf eine tiefen Schablone-Schnittstelle erhalten.</span><span class="sxs-lookup"><span data-stu-id="c3994-107">Get a pointer to a depth-stencil interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3994-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3994-108">Syntax</span></span>


```C++
HRESULT GetDepthStencilState(
   UINT                    Index,
   ID3D11DepthStencilState **ppDepthStencilState
);
```



## <a name="parameters"></a><span data-ttu-id="c3994-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3994-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3994-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="c3994-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="c3994-111">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c3994-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c3994-112">Indizieren Sie in ein Array von tiefen Schablonen Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="c3994-112">Index into an array of depth-stencil interfaces.</span></span> <span data-ttu-id="c3994-113">Wenn nur eine tiefen Schablone-Schnittstelle vorhanden ist, verwenden Sie 0.</span><span class="sxs-lookup"><span data-stu-id="c3994-113">If there is only one depth-stencil interface, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="c3994-114">*ppdepthstencilstate*</span><span class="sxs-lookup"><span data-stu-id="c3994-114">*ppDepthStencilState*</span></span> 
</dt> <dd>

<span data-ttu-id="c3994-115">Typ: **[ **ID3D11DepthStencilState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate)\*\***</span><span class="sxs-lookup"><span data-stu-id="c3994-115">Type: **[**ID3D11DepthStencilState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate)\*\***</span></span>

<span data-ttu-id="c3994-116">Die Adresse eines Zeigers auf eine Blend-State-Schnittstelle (siehe [**ID3D11DepthStencilState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate)).</span><span class="sxs-lookup"><span data-stu-id="c3994-116">The address of a pointer to a blend-state interface (see [**ID3D11DepthStencilState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3994-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c3994-117">Return value</span></span>

<span data-ttu-id="c3994-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c3994-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c3994-119">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="c3994-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c3994-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c3994-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c3994-121">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="c3994-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="c3994-122">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c3994-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="c3994-123">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="c3994-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c3994-124">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="c3994-124">Requirements</span></span>



| <span data-ttu-id="c3994-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3994-125">Requirement</span></span> | <span data-ttu-id="c3994-126">Wert</span><span class="sxs-lookup"><span data-stu-id="c3994-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3994-127">Header</span><span class="sxs-lookup"><span data-stu-id="c3994-127">Header</span></span><br/>  | <dl> <span data-ttu-id="c3994-128"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3994-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="c3994-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c3994-129">Library</span></span><br/> | <dl> <span data-ttu-id="c3994-130"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="c3994-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3994-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c3994-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3994-132">ID3DX11EffectDepthStencilVariable</span><span class="sxs-lookup"><span data-stu-id="c3994-132">ID3DX11EffectDepthStencilVariable</span></span>](id3dx11effectdepthstencilvariable.md)
</dt> </dl>

 

