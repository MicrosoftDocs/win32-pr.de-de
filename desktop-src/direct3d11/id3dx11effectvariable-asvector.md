---
title: ID3DX11EffectVariable asvector-Methode (D3dx11effect. h)
description: Eine Vektor Variable erhalten.
ms.assetid: 995bd9f3-1417-4048-9a23-4dcb3864c77d
keywords:
- Asvector-Methode Direct3D 11
- Asvector-Methode Direct3D 11, ID3DX11EffectVariable-Schnittstelle
- ID3DX11EffectVariable-Schnittstelle Direct3D 11, asvector-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsVector
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8df994536c818461b0307cdee726e704aaaf8a43
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996234"
---
# <a name="id3dx11effectvariableasvector-method"></a><span data-ttu-id="d0969-106">ID3DX11EffectVariable:: asvector-Methode</span><span class="sxs-lookup"><span data-stu-id="d0969-106">ID3DX11EffectVariable::AsVector method</span></span>

<span data-ttu-id="d0969-107">Eine Vektor Variable erhalten.</span><span class="sxs-lookup"><span data-stu-id="d0969-107">Get a vector variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0969-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d0969-108">Syntax</span></span>


```C++
ID3DX11EffectVectorVariable* AsVector();
```



## <a name="parameters"></a><span data-ttu-id="d0969-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d0969-109">Parameters</span></span>

<span data-ttu-id="d0969-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="d0969-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d0969-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d0969-111">Return value</span></span>

<span data-ttu-id="d0969-112">Typ: **[ **ID3DX11EffectVectorVariable**](id3dx11effectvectorvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="d0969-112">Type: **[**ID3DX11EffectVectorVariable**](id3dx11effectvectorvariable.md)\***</span></span>

<span data-ttu-id="d0969-113">Ein Zeiger auf eine Vektor Variable.</span><span class="sxs-lookup"><span data-stu-id="d0969-113">A pointer to a vector variable.</span></span> <span data-ttu-id="d0969-114">Siehe [**ID3DX11EffectVectorVariable**](id3dx11effectvectorvariable.md).</span><span class="sxs-lookup"><span data-stu-id="d0969-114">See [**ID3DX11EffectVectorVariable**](id3dx11effectvectorvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d0969-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d0969-115">Remarks</span></span>

<span data-ttu-id="d0969-116">Asvector gibt eine Version der Effekt Variablen zurück, die auf eine Vektor Variable spezialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="d0969-116">AsVector returns a version of the effect variable that has been specialized to a vector variable.</span></span> <span data-ttu-id="d0969-117">Ähnlich wie bei einer Umwandlung gibt diese Spezialisierung ein ungültiges Objekt zurück, wenn die Effekt Variable keine Vektordaten enthält.</span><span class="sxs-lookup"><span data-stu-id="d0969-117">Similar to a cast, this specialization will return an invalid object if the effect variable does not contain vector data.</span></span>

<span data-ttu-id="d0969-118">Anwendungen können das zurückgegebene Objekt auf Gültigkeit testen, indem Sie [**IsValid**](id3dx11effectvariable-isvalid.md)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d0969-118">Applications can test the returned object for validity by calling [**IsValid**](id3dx11effectvariable-isvalid.md).</span></span>

> [!Note]  
> <span data-ttu-id="d0969-119">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="d0969-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="d0969-120">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d0969-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="d0969-121">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="d0969-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d0969-122">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="d0969-122">Requirements</span></span>



| <span data-ttu-id="d0969-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d0969-123">Requirement</span></span> | <span data-ttu-id="d0969-124">Wert</span><span class="sxs-lookup"><span data-stu-id="d0969-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0969-125">Header</span><span class="sxs-lookup"><span data-stu-id="d0969-125">Header</span></span><br/>  | <dl> <span data-ttu-id="d0969-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0969-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="d0969-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d0969-127">Library</span></span><br/> | <dl> <span data-ttu-id="d0969-128"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="d0969-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0969-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d0969-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0969-130">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="d0969-130">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 





