---
title: ID3DX11EffectDepthStencilViewVariable setdepthstencilarray-Methode (D3dx11effect. h)
description: Legen Sie ein Array von tiefen Schablone-Ansichts Ressourcen fest.
ms.assetid: 7a00ca3e-fb07-4185-a361-36228f72dcea
keywords:
- Setdepthstencilarray-Methode Direct3D 11
- Setdepthstencilarray-Methode Direct3D 11, ID3DX11EffectDepthStencilViewVariable-Schnittstelle
- ID3DX11EffectDepthStencilViewVariable-Schnittstelle Direct3D 11, setdepthstencilarray-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilViewVariable.SetDepthStencilArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 329f91fff70d78c51475b799a08dec1c6d34a157
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982300"
---
# <a name="id3dx11effectdepthstencilviewvariablesetdepthstencilarray-method"></a><span data-ttu-id="3ba75-106">ID3DX11EffectDepthStencilViewVariable:: setdepthstencilarray-Methode</span><span class="sxs-lookup"><span data-stu-id="3ba75-106">ID3DX11EffectDepthStencilViewVariable::SetDepthStencilArray method</span></span>

<span data-ttu-id="3ba75-107">Legen Sie ein Array von tiefen Schablone-Ansichts Ressourcen fest.</span><span class="sxs-lookup"><span data-stu-id="3ba75-107">Set an array of depth-stencil-view resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ba75-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3ba75-108">Syntax</span></span>


```C++
HRESULT SetDepthStencilArray(
   ID3D11DepthStencilView **ppResources,
   UINT                   Offset,
   UINT                   Count
);
```



## <a name="parameters"></a><span data-ttu-id="3ba75-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="3ba75-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ba75-110">*ppresources*</span><span class="sxs-lookup"><span data-stu-id="3ba75-110">*ppResources*</span></span> 
</dt> <dd>

<span data-ttu-id="3ba75-111">Typ: **[ **ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)\*\***</span><span class="sxs-lookup"><span data-stu-id="3ba75-111">Type: **[**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)\*\***</span></span>

<span data-ttu-id="3ba75-112">Ein Zeiger auf ein Array von tiefen Schablone-Ansichts Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="3ba75-112">A pointer to an array of depth-stencil-view interfaces.</span></span> <span data-ttu-id="3ba75-113">Siehe [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview).</span><span class="sxs-lookup"><span data-stu-id="3ba75-113">See [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview).</span></span>

</dd> <dt>

<span data-ttu-id="3ba75-114">*Offset*</span><span class="sxs-lookup"><span data-stu-id="3ba75-114">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="3ba75-115">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3ba75-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3ba75-116">Der null basierte Array Index zum Festlegen der ersten Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="3ba75-116">The zero-based array index to set the first interface.</span></span>

</dd> <dt>

<span data-ttu-id="3ba75-117">*Count*</span><span class="sxs-lookup"><span data-stu-id="3ba75-117">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="3ba75-118">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3ba75-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3ba75-119">Die Anzahl der Elemente im Array.</span><span class="sxs-lookup"><span data-stu-id="3ba75-119">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ba75-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3ba75-120">Return value</span></span>

<span data-ttu-id="3ba75-121">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3ba75-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3ba75-122">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="3ba75-122">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3ba75-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3ba75-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3ba75-124">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="3ba75-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="3ba75-125">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3ba75-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="3ba75-126">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="3ba75-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3ba75-127">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="3ba75-127">Requirements</span></span>



| <span data-ttu-id="3ba75-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3ba75-128">Requirement</span></span> | <span data-ttu-id="3ba75-129">Wert</span><span class="sxs-lookup"><span data-stu-id="3ba75-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ba75-130">Header</span><span class="sxs-lookup"><span data-stu-id="3ba75-130">Header</span></span><br/>  | <dl> <span data-ttu-id="3ba75-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ba75-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="3ba75-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3ba75-132">Library</span></span><br/> | <dl> <span data-ttu-id="3ba75-133"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="3ba75-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ba75-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3ba75-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ba75-135">ID3DX11EffectDepthStencilViewVariable</span><span class="sxs-lookup"><span data-stu-id="3ba75-135">ID3DX11EffectDepthStencilViewVariable</span></span>](id3dx11effectdepthstencilviewvariable.md)
</dt> </dl>

 

