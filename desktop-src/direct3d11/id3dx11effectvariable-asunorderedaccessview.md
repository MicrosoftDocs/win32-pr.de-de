---
title: ID3DX11EffectVariable asunorderedaccessview-Methode (D3dx11effect. h)
description: Abrufen einer Variablen mit ungeordneter Zugriffs Sicht.
ms.assetid: e8b7c104-09f7-4bfb-9980-a5603550b723
keywords:
- Asunorderedaccessview-Methode Direct3D 11
- Asunorderedaccessview-Methode Direct3D 11, ID3DX11EffectVariable-Schnittstelle
- ID3DX11EffectVariable-Schnittstelle Direct3D 11, asunorderedaccessview-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsUnorderedAccessView
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8b9ce7dbbc99ef16ef3290ec1ba3135a8d2cb05
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762387"
---
# <a name="id3dx11effectvariableasunorderedaccessview-method"></a><span data-ttu-id="70a00-106">ID3DX11EffectVariable:: asunorderedaccessview-Methode</span><span class="sxs-lookup"><span data-stu-id="70a00-106">ID3DX11EffectVariable::AsUnorderedAccessView method</span></span>

<span data-ttu-id="70a00-107">Abrufen einer Variablen mit ungeordneter Zugriffs Sicht.</span><span class="sxs-lookup"><span data-stu-id="70a00-107">Get an unordered-access-view variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="70a00-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="70a00-108">Syntax</span></span>


```C++
ID3DX11EffectUnorderedAccessViewVariable* AsUnorderedAccessView();
```



## <a name="parameters"></a><span data-ttu-id="70a00-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="70a00-109">Parameters</span></span>

<span data-ttu-id="70a00-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="70a00-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="70a00-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="70a00-111">Return value</span></span>

<span data-ttu-id="70a00-112">Typ: **[ **ID3DX11EffectUnorderedAccessViewVariable**](id3dx11effectunorderedaccessviewvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="70a00-112">Type: **[**ID3DX11EffectUnorderedAccessViewVariable**](id3dx11effectunorderedaccessviewvariable.md)\***</span></span>

<span data-ttu-id="70a00-113">Ein Zeiger auf eine ungeordnete Access-View-Variable.</span><span class="sxs-lookup"><span data-stu-id="70a00-113">A pointer to an unordered-access-view variable.</span></span> <span data-ttu-id="70a00-114">Siehe [**ID3DX11EffectUnorderedAccessViewVariable**](id3dx11effectunorderedaccessviewvariable.md).</span><span class="sxs-lookup"><span data-stu-id="70a00-114">See [**ID3DX11EffectUnorderedAccessViewVariable**](id3dx11effectunorderedaccessviewvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="70a00-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="70a00-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="70a00-116">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="70a00-116">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="70a00-117">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="70a00-117">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="70a00-118">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="70a00-118">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="70a00-119">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="70a00-119">Requirements</span></span>



| <span data-ttu-id="70a00-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="70a00-120">Requirement</span></span> | <span data-ttu-id="70a00-121">Wert</span><span class="sxs-lookup"><span data-stu-id="70a00-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70a00-122">Header</span><span class="sxs-lookup"><span data-stu-id="70a00-122">Header</span></span><br/>  | <dl> <span data-ttu-id="70a00-123"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="70a00-123"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="70a00-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="70a00-124">Library</span></span><br/> | <dl> <span data-ttu-id="70a00-125"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="70a00-125"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70a00-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="70a00-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70a00-127">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="70a00-127">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 





