---
title: ID3DX11EffectDepthStencilViewVariable setdepthstencil-Methode (D3dx11effect. h)
description: Legen Sie eine tiefen Schablone-Ansichts Ressource fest.
ms.assetid: 35cbcd3b-6fc8-448d-a82e-724f91038d07
keywords:
- Setdepthstencil-Methode Direct3D 11
- Setdepthstencil-Methode Direct3D 11, ID3DX11EffectDepthStencilViewVariable-Schnittstelle
- ID3DX11EffectDepthStencilViewVariable-Schnittstelle Direct3D 11, setdepthstencil-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilViewVariable.SetDepthStencil
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 723be51bc769982acf43c19482978bd581cafa13
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995962"
---
# <a name="id3dx11effectdepthstencilviewvariablesetdepthstencil-method"></a><span data-ttu-id="e8c4f-106">ID3DX11EffectDepthStencilViewVariable:: setdepthstencil-Methode</span><span class="sxs-lookup"><span data-stu-id="e8c4f-106">ID3DX11EffectDepthStencilViewVariable::SetDepthStencil method</span></span>

<span data-ttu-id="e8c4f-107">Legen Sie eine tiefen Schablone-Ansichts Ressource fest.</span><span class="sxs-lookup"><span data-stu-id="e8c4f-107">Set a depth-stencil-view resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8c4f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8c4f-108">Syntax</span></span>


```C++
HRESULT SetDepthStencil(
   ID3D11DepthStencilView *pResource
);
```



## <a name="parameters"></a><span data-ttu-id="e8c4f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e8c4f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8c4f-110">*vorab Quelle*</span><span class="sxs-lookup"><span data-stu-id="e8c4f-110">*pResource*</span></span> 
</dt> <dd>

<span data-ttu-id="e8c4f-111">Typ: **[ **ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)\***</span><span class="sxs-lookup"><span data-stu-id="e8c4f-111">Type: **[**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)\***</span></span>

<span data-ttu-id="e8c4f-112">Ein Zeiger auf eine tiefen Schablone-View-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="e8c4f-112">A pointer to a depth-stencil-view interface.</span></span> <span data-ttu-id="e8c4f-113">Siehe [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview).</span><span class="sxs-lookup"><span data-stu-id="e8c4f-113">See [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8c4f-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e8c4f-114">Return value</span></span>

<span data-ttu-id="e8c4f-115">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e8c4f-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e8c4f-116">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="e8c4f-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e8c4f-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e8c4f-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e8c4f-118">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="e8c4f-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="e8c4f-119">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e8c4f-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="e8c4f-120">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="e8c4f-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e8c4f-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="e8c4f-121">Requirements</span></span>



| <span data-ttu-id="e8c4f-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e8c4f-122">Requirement</span></span> | <span data-ttu-id="e8c4f-123">Wert</span><span class="sxs-lookup"><span data-stu-id="e8c4f-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8c4f-124">Header</span><span class="sxs-lookup"><span data-stu-id="e8c4f-124">Header</span></span><br/>  | <dl> <span data-ttu-id="e8c4f-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8c4f-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="e8c4f-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e8c4f-126">Library</span></span><br/> | <dl> <span data-ttu-id="e8c4f-127"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="e8c4f-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8c4f-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e8c4f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8c4f-129">ID3DX11EffectDepthStencilViewVariable</span><span class="sxs-lookup"><span data-stu-id="e8c4f-129">ID3DX11EffectDepthStencilViewVariable</span></span>](id3dx11effectdepthstencilviewvariable.md)
</dt> </dl>

 

 





