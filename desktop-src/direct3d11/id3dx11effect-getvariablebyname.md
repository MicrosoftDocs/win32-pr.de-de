---
title: ID3DX11Effect getvariablebyname-Methode (D3dx11effect. h)
description: Eine Variable anhand ihres Namens erhalten.
ms.assetid: d20c5a85-51a5-482f-b5b0-197d8e993910
keywords:
- Getvariablebyname-Methode Direct3D 11
- Getvariablebyname-Methode Direct3D 11, ID3DX11Effect-Schnittstelle
- ID3DX11Effect Interface Direct3D 11, getvariablebyname-Methode
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetVariableByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e6079e7f45c21d9d7326021b2c439ab12e4e031
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996094"
---
# <a name="id3dx11effectgetvariablebyname-method"></a><span data-ttu-id="dc887-106">ID3DX11Effect:: getvariablebyname-Methode</span><span class="sxs-lookup"><span data-stu-id="dc887-106">ID3DX11Effect::GetVariableByName method</span></span>

<span data-ttu-id="dc887-107">Eine Variable anhand ihres Namens erhalten.</span><span class="sxs-lookup"><span data-stu-id="dc887-107">Get a variable by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc887-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc887-108">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetVariableByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="dc887-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="dc887-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc887-110">*Name*</span><span class="sxs-lookup"><span data-stu-id="dc887-110">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="dc887-111">Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="dc887-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="dc887-112">Der Variablenname.</span><span class="sxs-lookup"><span data-stu-id="dc887-112">The variable name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc887-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dc887-113">Return value</span></span>

<span data-ttu-id="dc887-114">Typ: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="dc887-114">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="dc887-115">Ein Zeiger auf eine [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="dc887-115">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="dc887-116">Gibt eine ungültige Variable zurück, wenn der angegebene Name nicht gefunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="dc887-116">Returns an invalid variable if the specified name cannot be found.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc887-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dc887-117">Remarks</span></span>

<span data-ttu-id="dc887-118">Ein Effekt kann eine oder mehrere Variablen enthalten.</span><span class="sxs-lookup"><span data-stu-id="dc887-118">An effect may contain one or more variables.</span></span> <span data-ttu-id="dc887-119">Variablen außerhalb eines Verfahrens werden als Global für alle Effekte betrachtet, die sich innerhalb eines Verfahrens vor Ort befinden.</span><span class="sxs-lookup"><span data-stu-id="dc887-119">Variables outside of a technique are considered global to all effects, those located inside of a technique are local to that technique.</span></span> <span data-ttu-id="dc887-120">Sie können auf eine Effekt Variable mithilfe Ihres Namens oder mit einem Index zugreifen.</span><span class="sxs-lookup"><span data-stu-id="dc887-120">You can access an effect variable using its name or with an index.</span></span>

<span data-ttu-id="dc887-121">Die-Methode gibt einen Zeiger auf eine [**Effekt Variable-Schnittstelle**](id3dx11effectvariable.md) zurück, unabhängig davon, ob eine Variable gefunden wird oder nicht.</span><span class="sxs-lookup"><span data-stu-id="dc887-121">The method returns a pointer to an [**effect-variable interface**](id3dx11effectvariable.md) whether or not a variable is found.</span></span> <span data-ttu-id="dc887-122">[**ID3DX11Effect:: IsValid**](id3dx11effect-isvalid.md) sollte aufgerufen werden, um zu überprüfen, ob der Name vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="dc887-122">[**ID3DX11Effect::IsValid**](id3dx11effect-isvalid.md) should be called to verify whether or not the name exists.</span></span>

> [!Note]  
> <span data-ttu-id="dc887-123">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="dc887-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="dc887-124">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="dc887-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="dc887-125">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="dc887-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="dc887-126">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="dc887-126">Requirements</span></span>



| <span data-ttu-id="dc887-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dc887-127">Requirement</span></span> | <span data-ttu-id="dc887-128">Wert</span><span class="sxs-lookup"><span data-stu-id="dc887-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc887-129">Header</span><span class="sxs-lookup"><span data-stu-id="dc887-129">Header</span></span><br/>  | <dl> <span data-ttu-id="dc887-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc887-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="dc887-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="dc887-131">Library</span></span><br/> | <dl> <span data-ttu-id="dc887-132"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="dc887-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc887-133">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="dc887-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc887-134">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="dc887-134">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

