---
title: ID3DX11EffectRenderTargetViewVariable GetRenderTargetArray-Methode (D3dx11effect. h)
description: Ein Array von renderzielen erhalten.
ms.assetid: cc98a3b3-c2a2-48d0-86a8-77b914a199ec
keywords:
- GetRenderTargetArray-Methode Direct3D 11
- GetRenderTargetArray-Methode Direct3D 11, ID3DX11EffectRenderTargetViewVariable-Schnittstelle
- ID3DX11EffectRenderTargetViewVariable-Schnittstelle Direct3D 11, GetRenderTargetArray-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectRenderTargetViewVariable.GetRenderTargetArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3521b05bbc4e603264b993b6fe7b677a5cf46aee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996251"
---
# <a name="id3dx11effectrendertargetviewvariablegetrendertargetarray-method"></a><span data-ttu-id="3a070-106">ID3DX11EffectRenderTargetViewVariable:: GetRenderTargetArray-Methode</span><span class="sxs-lookup"><span data-stu-id="3a070-106">ID3DX11EffectRenderTargetViewVariable::GetRenderTargetArray method</span></span>

<span data-ttu-id="3a070-107">Ein Array von renderzielen erhalten.</span><span class="sxs-lookup"><span data-stu-id="3a070-107">Get an array of render-targets.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a070-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a070-108">Syntax</span></span>


```C++
HRESULT GetRenderTargetArray(
   ID3D11RenderTargetView **ppResources,
   UINT                   Offset,
   UINT                   Count
);
```



## <a name="parameters"></a><span data-ttu-id="3a070-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="3a070-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a070-110">*ppresources*</span><span class="sxs-lookup"><span data-stu-id="3a070-110">*ppResources*</span></span> 
</dt> <dd>

<span data-ttu-id="3a070-111">Typ: **[ **ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)\*\***</span><span class="sxs-lookup"><span data-stu-id="3a070-111">Type: **[**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)\*\***</span></span>

<span data-ttu-id="3a070-112">Ein Zeiger auf ein Array von "Rendering-Target-View"-Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="3a070-112">A pointer to an array of render-target-view interfaces.</span></span> <span data-ttu-id="3a070-113">Siehe [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview).</span><span class="sxs-lookup"><span data-stu-id="3a070-113">See [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview).</span></span>

</dd> <dt>

<span data-ttu-id="3a070-114">*Offset*</span><span class="sxs-lookup"><span data-stu-id="3a070-114">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="3a070-115">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3a070-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3a070-116">Der null basierte Array Index, um die erste Schnittstelle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="3a070-116">The zero-based array index to get the first interface.</span></span>

</dd> <dt>

<span data-ttu-id="3a070-117">*Count*</span><span class="sxs-lookup"><span data-stu-id="3a070-117">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="3a070-118">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3a070-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3a070-119">Die Anzahl der Elemente im Array.</span><span class="sxs-lookup"><span data-stu-id="3a070-119">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a070-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3a070-120">Return value</span></span>

<span data-ttu-id="3a070-121">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3a070-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3a070-122">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="3a070-122">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3a070-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3a070-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3a070-124">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="3a070-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="3a070-125">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3a070-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="3a070-126">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="3a070-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3a070-127">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="3a070-127">Requirements</span></span>



| <span data-ttu-id="3a070-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3a070-128">Requirement</span></span> | <span data-ttu-id="3a070-129">Wert</span><span class="sxs-lookup"><span data-stu-id="3a070-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a070-130">Header</span><span class="sxs-lookup"><span data-stu-id="3a070-130">Header</span></span><br/>  | <dl> <span data-ttu-id="3a070-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a070-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="3a070-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3a070-132">Library</span></span><br/> | <dl> <span data-ttu-id="3a070-133"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="3a070-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a070-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3a070-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a070-135">ID3DX11EffectRenderTargetViewVariable</span><span class="sxs-lookup"><span data-stu-id="3a070-135">ID3DX11EffectRenderTargetViewVariable</span></span>](id3dx11effectrendertargetviewvariable.md)
</dt> </dl>

 

