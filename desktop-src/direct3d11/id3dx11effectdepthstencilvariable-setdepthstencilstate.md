---
title: ID3DX11EffectDepthStencilVariable setdepthstencilstate-Methode (D3dx11effect. h)
description: Legt den Status der tiefen Schablone fest.
ms.assetid: 4ece246f-4466-4790-8f38-450b67fff7c6
keywords:
- Setdepthstencilstate-Methode Direct3D 11
- Setdepthstencilstate-Methode Direct3D 11, ID3DX11EffectDepthStencilVariable-Schnittstelle
- ID3DX11EffectDepthStencilVariable-Schnittstelle Direct3D 11, setdepthstencilstate-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilVariable.SetDepthStencilState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64b82fac869cb15bced76fdc1335967c6f7d017f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982455"
---
# <a name="id3dx11effectdepthstencilvariablesetdepthstencilstate-method"></a><span data-ttu-id="0473b-106">ID3DX11EffectDepthStencilVariable:: setdepthstencilstate-Methode</span><span class="sxs-lookup"><span data-stu-id="0473b-106">ID3DX11EffectDepthStencilVariable::SetDepthStencilState method</span></span>

<span data-ttu-id="0473b-107">Legt den Status der tiefen Schablone fest.</span><span class="sxs-lookup"><span data-stu-id="0473b-107">Sets the depth stencil state.</span></span>

## <a name="syntax"></a><span data-ttu-id="0473b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0473b-108">Syntax</span></span>


```C++
HRESULT SetDepthStencilState(
   UINT                    Index,
   ID3D11DepthStencilState *pDepthStencilState
);
```



## <a name="parameters"></a><span data-ttu-id="0473b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0473b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0473b-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="0473b-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="0473b-111">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0473b-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="0473b-112">Indizieren Sie in ein Array von tiefen Schablonen Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="0473b-112">Index into an array of depth-stencil interfaces.</span></span> <span data-ttu-id="0473b-113">Wenn nur eine tiefen Schablone-Schnittstelle vorhanden ist, verwenden Sie 0.</span><span class="sxs-lookup"><span data-stu-id="0473b-113">If there is only one depth-stencil interface, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="0473b-114">*pdepthstencilstate*</span><span class="sxs-lookup"><span data-stu-id="0473b-114">*pDepthStencilState*</span></span> 
</dt> <dd>

<span data-ttu-id="0473b-115">Typ: **[ **ID3D11DepthStencilState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate)\***</span><span class="sxs-lookup"><span data-stu-id="0473b-115">Type: **[**ID3D11DepthStencilState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate)\***</span></span>

<span data-ttu-id="0473b-116">Zeiger auf eine [**ID3D11DepthStencilState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate) -Schnittstelle, die den neuen Zustand der tiefen Schablone enthält.</span><span class="sxs-lookup"><span data-stu-id="0473b-116">Pointer to an [**ID3D11DepthStencilState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate) interface containing the new depth stencil state.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0473b-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0473b-117">Return value</span></span>

<span data-ttu-id="0473b-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0473b-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0473b-119">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="0473b-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0473b-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0473b-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0473b-121">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="0473b-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="0473b-122">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0473b-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="0473b-123">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="0473b-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0473b-124">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="0473b-124">Requirements</span></span>



| <span data-ttu-id="0473b-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0473b-125">Requirement</span></span> | <span data-ttu-id="0473b-126">Wert</span><span class="sxs-lookup"><span data-stu-id="0473b-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0473b-127">Header</span><span class="sxs-lookup"><span data-stu-id="0473b-127">Header</span></span><br/>  | <dl> <span data-ttu-id="0473b-128"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="0473b-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="0473b-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0473b-129">Library</span></span><br/> | <dl> <span data-ttu-id="0473b-130"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="0473b-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0473b-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0473b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0473b-132">ID3DX11EffectDepthStencilVariable</span><span class="sxs-lookup"><span data-stu-id="0473b-132">ID3DX11EffectDepthStencilVariable</span></span>](id3dx11effectdepthstencilvariable.md)
</dt> </dl>

 

