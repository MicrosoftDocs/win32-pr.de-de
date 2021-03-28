---
title: ID3DX11EffectPass computestateblockmask-Methode (D3dx11effect. h)
description: Generiert eine Maske zum zulassen/verhindern von Zustandsänderungen.
ms.assetid: 584be931-0e22-43e6-b852-f0d2ab050bdd
keywords:
- Computestateblockmask-Methode Direct3D 11
- Computestateblockmask-Methode Direct3D 11, ID3DX11EffectPass-Schnittstelle
- ID3DX11EffectPass-Schnittstelle Direct3D 11, computestateblockmask-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.ComputeStateBlockMask
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8fc5cb32ce9e9644d7d5b62868bfa99f150cc94
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982365"
---
# <a name="id3dx11effectpasscomputestateblockmask-method"></a><span data-ttu-id="db57b-106">ID3DX11EffectPass:: computestateblockmask-Methode</span><span class="sxs-lookup"><span data-stu-id="db57b-106">ID3DX11EffectPass::ComputeStateBlockMask method</span></span>

<span data-ttu-id="db57b-107">Generiert eine Maske zum zulassen/verhindern von Zustandsänderungen.</span><span class="sxs-lookup"><span data-stu-id="db57b-107">Generate a mask for allowing/preventing state changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="db57b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="db57b-108">Syntax</span></span>


```C++
HRESULT ComputeStateBlockMask(
   D3DX11_STATE_BLOCK_MASK *pStateBlockMask
);
```



## <a name="parameters"></a><span data-ttu-id="db57b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="db57b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db57b-110">*pstateblockmask*</span><span class="sxs-lookup"><span data-stu-id="db57b-110">*pStateBlockMask*</span></span> 
</dt> <dd>

<span data-ttu-id="db57b-111">Type: **[ **Bibliothek d3dx11 \_ State \_ Block \_ Mask**](d3dx11-state-block-mask.md)\***</span><span class="sxs-lookup"><span data-stu-id="db57b-111">Type: **[**D3DX11\_STATE\_BLOCK\_MASK**](d3dx11-state-block-mask.md)\***</span></span>

<span data-ttu-id="db57b-112">Ein Zeiger auf eine Zustands Block Maske (siehe [**Bibliothek d3dx11 \_ State \_ Block \_ Mask**](d3dx11-state-block-mask.md)).</span><span class="sxs-lookup"><span data-stu-id="db57b-112">A pointer to a state-block mask (see [**D3DX11\_STATE\_BLOCK\_MASK**](d3dx11-state-block-mask.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db57b-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="db57b-113">Return value</span></span>

<span data-ttu-id="db57b-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="db57b-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="db57b-115">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="db57b-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="db57b-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="db57b-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="db57b-117">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="db57b-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="db57b-118">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="db57b-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="db57b-119">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="db57b-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="db57b-120">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="db57b-120">Requirements</span></span>



| <span data-ttu-id="db57b-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="db57b-121">Requirement</span></span> | <span data-ttu-id="db57b-122">Wert</span><span class="sxs-lookup"><span data-stu-id="db57b-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db57b-123">Header</span><span class="sxs-lookup"><span data-stu-id="db57b-123">Header</span></span><br/>  | <dl> <span data-ttu-id="db57b-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="db57b-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="db57b-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="db57b-125">Library</span></span><br/> | <dl> <span data-ttu-id="db57b-126"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="db57b-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db57b-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="db57b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db57b-128">ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="db57b-128">ID3DX11EffectPass</span></span>](id3dx11effectpass.md)
</dt> </dl>

 

 





