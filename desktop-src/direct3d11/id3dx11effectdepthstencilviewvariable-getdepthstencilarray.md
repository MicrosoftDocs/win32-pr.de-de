---
title: ID3DX11EffectDepthStencilViewVariable getdepthstencilarray-Methode (D3dx11effect. h)
description: Sie erhalten ein Array von tiefen Schablone-Ansichts Ressourcen.
ms.assetid: 92b2d9b1-6cf8-4523-88e0-bcd09b95477c
keywords:
- Getdepthstencilarray-Methode Direct3D 11
- Getdepthstencilarray-Methode Direct3D 11, ID3DX11EffectDepthStencilViewVariable-Schnittstelle
- ID3DX11EffectDepthStencilViewVariable-Schnittstelle Direct3D 11, getdepthstencilarray-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilViewVariable.GetDepthStencilArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7b7b886049413be542108257a47a3b1e3899910
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982444"
---
# <a name="id3dx11effectdepthstencilviewvariablegetdepthstencilarray-method"></a><span data-ttu-id="34dde-106">ID3DX11EffectDepthStencilViewVariable:: getdepthstencilarray-Methode</span><span class="sxs-lookup"><span data-stu-id="34dde-106">ID3DX11EffectDepthStencilViewVariable::GetDepthStencilArray method</span></span>

<span data-ttu-id="34dde-107">Sie erhalten ein Array von tiefen Schablone-Ansichts Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="34dde-107">Get an array of depth-stencil-view resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="34dde-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="34dde-108">Syntax</span></span>


```C++
HRESULT GetDepthStencilArray(
   ID3D11DepthStencilView **ppResources,
   UINT                   Offset,
   UINT                   Count
);
```



## <a name="parameters"></a><span data-ttu-id="34dde-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="34dde-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34dde-110">*ppresources*</span><span class="sxs-lookup"><span data-stu-id="34dde-110">*ppResources*</span></span> 
</dt> <dd>

<span data-ttu-id="34dde-111">Typ: **[ **ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)\*\***</span><span class="sxs-lookup"><span data-stu-id="34dde-111">Type: **[**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)\*\***</span></span>

<span data-ttu-id="34dde-112">Ein Zeiger auf ein Array von tiefen Schablone-Ansichts Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="34dde-112">A pointer to an array of depth-stencil-view interfaces.</span></span> <span data-ttu-id="34dde-113">Siehe [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview).</span><span class="sxs-lookup"><span data-stu-id="34dde-113">See [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview).</span></span>

</dd> <dt>

<span data-ttu-id="34dde-114">*Offset*</span><span class="sxs-lookup"><span data-stu-id="34dde-114">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="34dde-115">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="34dde-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="34dde-116">Der null basierte Array Index, um die erste Schnittstelle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="34dde-116">The zero-based array index to get the first interface.</span></span>

</dd> <dt>

<span data-ttu-id="34dde-117">*Count*</span><span class="sxs-lookup"><span data-stu-id="34dde-117">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="34dde-118">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="34dde-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="34dde-119">Die Anzahl der Elemente im Array.</span><span class="sxs-lookup"><span data-stu-id="34dde-119">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34dde-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="34dde-120">Return value</span></span>

<span data-ttu-id="34dde-121">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="34dde-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="34dde-122">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="34dde-122">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="34dde-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="34dde-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="34dde-124">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="34dde-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="34dde-125">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="34dde-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="34dde-126">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="34dde-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="34dde-127">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="34dde-127">Requirements</span></span>



| <span data-ttu-id="34dde-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="34dde-128">Requirement</span></span> | <span data-ttu-id="34dde-129">Wert</span><span class="sxs-lookup"><span data-stu-id="34dde-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34dde-130">Header</span><span class="sxs-lookup"><span data-stu-id="34dde-130">Header</span></span><br/>  | <dl> <span data-ttu-id="34dde-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="34dde-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="34dde-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="34dde-132">Library</span></span><br/> | <dl> <span data-ttu-id="34dde-133"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="34dde-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34dde-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="34dde-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34dde-135">ID3DX11EffectDepthStencilViewVariable</span><span class="sxs-lookup"><span data-stu-id="34dde-135">ID3DX11EffectDepthStencilViewVariable</span></span>](id3dx11effectdepthstencilviewvariable.md)
</dt> </dl>

 

