---
title: ID3DX11EffectRenderTargetViewVariable-Methode für die Methode "*" (D3dx11effect. h)
description: Legen Sie ein Array von Renderingzielen fest.
ms.assetid: 03e1c4ea-292c-439f-a647-070b9e91a044
keywords:
- Methode "tartrendertargetarray" Direct3D 11
- Die Methode "tartrendertargetarray" Direct3D 11, ID3DX11EffectRenderTargetViewVariable Interface
- ID3DX11EffectRenderTargetViewVariable-Schnittstelle Direct3D 11, Methode "strendertargetarray"
topic_type:
- apiref
api_name:
- ID3DX11EffectRenderTargetViewVariable.SetRenderTargetArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6ff8a1931e95df4fd78d67a3a71d53150875400
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982167"
---
# <a name="id3dx11effectrendertargetviewvariablesetrendertargetarray-method"></a><span data-ttu-id="3a5fe-106">ID3DX11EffectRenderTargetViewVariable:: strendertargetarray-Methode</span><span class="sxs-lookup"><span data-stu-id="3a5fe-106">ID3DX11EffectRenderTargetViewVariable::SetRenderTargetArray method</span></span>

<span data-ttu-id="3a5fe-107">Legen Sie ein Array von Renderingzielen fest.</span><span class="sxs-lookup"><span data-stu-id="3a5fe-107">Set an array of render-targets.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a5fe-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a5fe-108">Syntax</span></span>


```C++
HRESULT SetRenderTargetArray(
   ID3D11RenderTargetView **ppResources,
   UINT                   Offset,
   UINT                   Count
);
```



## <a name="parameters"></a><span data-ttu-id="3a5fe-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="3a5fe-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a5fe-110">*ppresources*</span><span class="sxs-lookup"><span data-stu-id="3a5fe-110">*ppResources*</span></span> 
</dt> <dd>

<span data-ttu-id="3a5fe-111">Typ: **[ **ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)\*\***</span><span class="sxs-lookup"><span data-stu-id="3a5fe-111">Type: **[**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)\*\***</span></span>

<span data-ttu-id="3a5fe-112">Legen Sie ein Array von Renderziel-View-Schnittstellen fest.</span><span class="sxs-lookup"><span data-stu-id="3a5fe-112">Set an array of render-target-view interfaces.</span></span> <span data-ttu-id="3a5fe-113">Siehe [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview).</span><span class="sxs-lookup"><span data-stu-id="3a5fe-113">See [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview).</span></span>

</dd> <dt>

<span data-ttu-id="3a5fe-114">*Offset*</span><span class="sxs-lookup"><span data-stu-id="3a5fe-114">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="3a5fe-115">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3a5fe-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3a5fe-116">Der null basierte Array Index zum Speichern der ersten Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="3a5fe-116">The zero-based array index to store the first interface.</span></span>

</dd> <dt>

<span data-ttu-id="3a5fe-117">*Count*</span><span class="sxs-lookup"><span data-stu-id="3a5fe-117">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="3a5fe-118">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3a5fe-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3a5fe-119">Die Anzahl der Elemente im Array.</span><span class="sxs-lookup"><span data-stu-id="3a5fe-119">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a5fe-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3a5fe-120">Return value</span></span>

<span data-ttu-id="3a5fe-121">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3a5fe-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3a5fe-122">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="3a5fe-122">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3a5fe-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3a5fe-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3a5fe-124">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="3a5fe-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="3a5fe-125">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3a5fe-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="3a5fe-126">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="3a5fe-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3a5fe-127">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="3a5fe-127">Requirements</span></span>



| <span data-ttu-id="3a5fe-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3a5fe-128">Requirement</span></span> | <span data-ttu-id="3a5fe-129">Wert</span><span class="sxs-lookup"><span data-stu-id="3a5fe-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a5fe-130">Header</span><span class="sxs-lookup"><span data-stu-id="3a5fe-130">Header</span></span><br/>  | <dl> <span data-ttu-id="3a5fe-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a5fe-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="3a5fe-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3a5fe-132">Library</span></span><br/> | <dl> <span data-ttu-id="3a5fe-133"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="3a5fe-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a5fe-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3a5fe-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a5fe-135">ID3DX11EffectRenderTargetViewVariable</span><span class="sxs-lookup"><span data-stu-id="3a5fe-135">ID3DX11EffectRenderTargetViewVariable</span></span>](id3dx11effectrendertargetviewvariable.md)
</dt> </dl>

 

