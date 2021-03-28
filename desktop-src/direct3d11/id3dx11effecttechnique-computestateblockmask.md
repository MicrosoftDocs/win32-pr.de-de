---
title: ID3DX11EffectTechnique computestateblockmask-Methode (D3dx11effect. h)
description: Berechnen Sie eine Zustands Block Maske, um Zustandsänderungen zuzulassen/zu verhindern.
ms.assetid: 4fd6061d-6ca5-4e3f-b031-fae98f3de057
keywords:
- Computestateblockmask-Methode Direct3D 11
- Computestateblockmask-Methode Direct3D 11, ID3DX11EffectTechnique-Schnittstelle
- ID3DX11EffectTechnique-Schnittstelle Direct3D 11, computestateblockmask-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.ComputeStateBlockMask
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d15a159c15f35d530559b4ad6d84dd815e5964a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219459"
---
# <a name="id3dx11effecttechniquecomputestateblockmask-method"></a><span data-ttu-id="4ffde-106">ID3DX11EffectTechnique:: computestateblockmask-Methode</span><span class="sxs-lookup"><span data-stu-id="4ffde-106">ID3DX11EffectTechnique::ComputeStateBlockMask method</span></span>

<span data-ttu-id="4ffde-107">Berechnen Sie eine Zustands Block Maske, um Zustandsänderungen zuzulassen/zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="4ffde-107">Compute a state-block mask to allow/prevent state changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ffde-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ffde-108">Syntax</span></span>


```C++
HRESULT ComputeStateBlockMask(
   D3DX11_STATE_BLOCK_MASK *pStateBlockMask
);
```



## <a name="parameters"></a><span data-ttu-id="4ffde-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="4ffde-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ffde-110">*pstateblockmask*</span><span class="sxs-lookup"><span data-stu-id="4ffde-110">*pStateBlockMask*</span></span> 
</dt> <dd>

<span data-ttu-id="4ffde-111">Type: **[ **Bibliothek d3dx11 \_ State \_ Block \_ Mask**](d3dx11-state-block-mask.md)\***</span><span class="sxs-lookup"><span data-stu-id="4ffde-111">Type: **[**D3DX11\_STATE\_BLOCK\_MASK**](d3dx11-state-block-mask.md)\***</span></span>

<span data-ttu-id="4ffde-112">Ein Zeiger auf eine Zustands Block Maske (siehe [**Bibliothek d3dx11 \_ State \_ Block \_ Mask**](d3dx11-state-block-mask.md)).</span><span class="sxs-lookup"><span data-stu-id="4ffde-112">A pointer to a state-block mask (see [**D3DX11\_STATE\_BLOCK\_MASK**](d3dx11-state-block-mask.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ffde-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4ffde-113">Return value</span></span>

<span data-ttu-id="4ffde-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4ffde-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4ffde-115">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="4ffde-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4ffde-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4ffde-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4ffde-117">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="4ffde-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="4ffde-118">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4ffde-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="4ffde-119">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="4ffde-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4ffde-120">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="4ffde-120">Requirements</span></span>



| <span data-ttu-id="4ffde-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4ffde-121">Requirement</span></span> | <span data-ttu-id="4ffde-122">Wert</span><span class="sxs-lookup"><span data-stu-id="4ffde-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ffde-123">Header</span><span class="sxs-lookup"><span data-stu-id="4ffde-123">Header</span></span><br/>  | <dl> <span data-ttu-id="4ffde-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ffde-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="4ffde-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4ffde-125">Library</span></span><br/> | <dl> <span data-ttu-id="4ffde-126"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="4ffde-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ffde-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4ffde-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ffde-128">ID3DX11EffectTechnique</span><span class="sxs-lookup"><span data-stu-id="4ffde-128">ID3DX11EffectTechnique</span></span>](id3dx11effecttechnique.md)
</dt> </dl>

 

 





