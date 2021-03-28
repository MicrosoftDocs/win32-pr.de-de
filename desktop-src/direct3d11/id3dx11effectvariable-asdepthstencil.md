---
title: ID3DX11EffectVariable asdepthstencil-Methode (D3dx11effect. h)
description: Eine tiefen Schablone-Variable erhalten.
ms.assetid: 3526812b-6c43-492e-b529-12f61ecd20e3
keywords:
- Asdepthstencil-Methode Direct3D 11
- Asdepthstencil-Methode Direct3D 11, ID3DX11EffectVariable-Schnittstelle
- ID3DX11EffectVariable-Schnittstelle Direct3D 11, asdepthstencil-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsDepthStencil
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 980bd43f51d187252fab1872ba75d04f82820ef8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961650"
---
# <a name="id3dx11effectvariableasdepthstencil-method"></a><span data-ttu-id="b1b85-106">ID3DX11EffectVariable:: asdepthstencil-Methode</span><span class="sxs-lookup"><span data-stu-id="b1b85-106">ID3DX11EffectVariable::AsDepthStencil method</span></span>

<span data-ttu-id="b1b85-107">Eine tiefen Schablone-Variable erhalten.</span><span class="sxs-lookup"><span data-stu-id="b1b85-107">Get a depth-stencil variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1b85-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1b85-108">Syntax</span></span>


```C++
ID3DX11EffectDepthStencilVariable* AsDepthStencil();
```



## <a name="parameters"></a><span data-ttu-id="b1b85-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b1b85-109">Parameters</span></span>

<span data-ttu-id="b1b85-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="b1b85-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b1b85-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b1b85-111">Return value</span></span>

<span data-ttu-id="b1b85-112">Typ: **[ **ID3DX11EffectDepthStencilVariable**](id3dx11effectdepthstencilvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="b1b85-112">Type: **[**ID3DX11EffectDepthStencilVariable**](id3dx11effectdepthstencilvariable.md)\***</span></span>

<span data-ttu-id="b1b85-113">Ein Zeiger auf eine tiefen Schablone-Variable.</span><span class="sxs-lookup"><span data-stu-id="b1b85-113">A pointer to a depth-stencil variable.</span></span> <span data-ttu-id="b1b85-114">Siehe [**ID3DX11EffectDepthStencilVariable**](id3dx11effectdepthstencilvariable.md).</span><span class="sxs-lookup"><span data-stu-id="b1b85-114">See [**ID3DX11EffectDepthStencilVariable**](id3dx11effectdepthstencilvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b1b85-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b1b85-115">Remarks</span></span>

<span data-ttu-id="b1b85-116">Asdepthstencil gibt eine Version der Effekt Variablen zurück, die auf eine tiefen Schablone-Variable spezialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="b1b85-116">AsDepthStencil returns a version of the effect variable that has been specialized to a depth-stencil variable.</span></span> <span data-ttu-id="b1b85-117">Ähnlich wie bei einer Umwandlung gibt diese Spezialisierung ein ungültiges Objekt zurück, wenn die Effekt Variable keine tiefen Schablone-Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="b1b85-117">Similar to a cast, this specialization will return an invalid object if the effect variable does not contain depth-stencil data.</span></span>

<span data-ttu-id="b1b85-118">Anwendungen können das zurückgegebene Objekt auf Gültigkeit testen, indem Sie [**IsValid**](id3dx11effectvariable-isvalid.md)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b1b85-118">Applications can test the returned object for validity by calling [**IsValid**](id3dx11effectvariable-isvalid.md).</span></span>

> [!Note]  
> <span data-ttu-id="b1b85-119">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="b1b85-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="b1b85-120">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b1b85-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="b1b85-121">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="b1b85-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b1b85-122">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="b1b85-122">Requirements</span></span>



| <span data-ttu-id="b1b85-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b1b85-123">Requirement</span></span> | <span data-ttu-id="b1b85-124">Wert</span><span class="sxs-lookup"><span data-stu-id="b1b85-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1b85-125">Header</span><span class="sxs-lookup"><span data-stu-id="b1b85-125">Header</span></span><br/>  | <dl> <span data-ttu-id="b1b85-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1b85-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="b1b85-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b1b85-127">Library</span></span><br/> | <dl> <span data-ttu-id="b1b85-128"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="b1b85-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1b85-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b1b85-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1b85-130">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="b1b85-130">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 





