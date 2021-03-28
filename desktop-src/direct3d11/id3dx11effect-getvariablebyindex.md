---
title: ID3DX11Effect getvariablebyindex-Methode (D3dx11effect. h)
description: Eine Variable nach Index erhalten.
ms.assetid: af25b945-9526-45c2-8746-8b62f8166de7
keywords:
- Getvariablebyindex-Methode Direct3D 11
- Getvariablebyindex-Methode Direct3D 11, ID3DX11Effect-Schnittstelle
- ID3DX11Effect Interface Direct3D 11, getvariablebyindex-Methode
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetVariableByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd262ea0aa778f03c2d723dec99f531f3419f3be
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996100"
---
# <a name="id3dx11effectgetvariablebyindex-method"></a><span data-ttu-id="62f79-106">ID3DX11Effect:: getvariablebyindex-Methode</span><span class="sxs-lookup"><span data-stu-id="62f79-106">ID3DX11Effect::GetVariableByIndex method</span></span>

<span data-ttu-id="62f79-107">Eine Variable nach Index erhalten.</span><span class="sxs-lookup"><span data-stu-id="62f79-107">Get a variable by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="62f79-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="62f79-108">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetVariableByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="62f79-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="62f79-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62f79-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="62f79-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="62f79-111">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="62f79-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="62f79-112">Ein NULL basierter Index.</span><span class="sxs-lookup"><span data-stu-id="62f79-112">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62f79-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="62f79-113">Return value</span></span>

<span data-ttu-id="62f79-114">Typ: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="62f79-114">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="62f79-115">Ein Zeiger auf eine [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="62f79-115">A pointer to a [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="62f79-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="62f79-116">Remarks</span></span>

<span data-ttu-id="62f79-117">Ein Effekt kann eine oder mehrere Variablen enthalten.</span><span class="sxs-lookup"><span data-stu-id="62f79-117">An effect may contain one or more variables.</span></span> <span data-ttu-id="62f79-118">Variablen außerhalb eines Verfahrens werden als Global für alle Effekte betrachtet, die sich innerhalb eines Verfahrens vor Ort befinden.</span><span class="sxs-lookup"><span data-stu-id="62f79-118">Variables outside of a technique are considered global to all effects, those located inside of a technique are local to that technique.</span></span> <span data-ttu-id="62f79-119">Sie können auf eine beliebige lokale nicht statische Effekt Variable mithilfe Ihres Namens oder mit einem Index zugreifen.</span><span class="sxs-lookup"><span data-stu-id="62f79-119">You can access any local non-static effect variable using its name or with an index.</span></span>

<span data-ttu-id="62f79-120">Die-Methode gibt einen Zeiger auf eine [**Effekt Variable-Schnittstelle**](id3dx11effectvariable.md) zurück, wenn eine Variable nicht gefunden wird. Sie können [**ID3DX11Effect:: IsValid**](id3dx11effect-isvalid.md) aufgerufen, um zu überprüfen, ob der Index vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="62f79-120">The method returns a pointer to an [**effect-variable interface**](id3dx11effectvariable.md) if a variable is not found; you can call [**ID3DX11Effect::IsValid**](id3dx11effect-isvalid.md) to verify whether or not the index exists.</span></span>

> [!Note]  
> <span data-ttu-id="62f79-121">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="62f79-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="62f79-122">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="62f79-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="62f79-123">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="62f79-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="62f79-124">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="62f79-124">Requirements</span></span>



| <span data-ttu-id="62f79-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="62f79-125">Requirement</span></span> | <span data-ttu-id="62f79-126">Wert</span><span class="sxs-lookup"><span data-stu-id="62f79-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62f79-127">Header</span><span class="sxs-lookup"><span data-stu-id="62f79-127">Header</span></span><br/>  | <dl> <span data-ttu-id="62f79-128"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="62f79-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="62f79-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="62f79-129">Library</span></span><br/> | <dl> <span data-ttu-id="62f79-130"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="62f79-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62f79-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="62f79-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62f79-132">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="62f79-132">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

