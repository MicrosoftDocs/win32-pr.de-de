---
title: ID3DX11EffectVariable getmembership bysemantic-Methode (D3dx11effect. h)
description: Einen Strukturmember nach Semantik erhalten.
ms.assetid: e4ae1f6a-43d2-45df-9dba-833d4f767818
keywords:
- Getmembership bysemantic-Methode Direct3D 11
- Getmembership bysemantic-Methode Direct3D 11, ID3DX11EffectVariable-Schnittstelle
- ID3DX11EffectVariable-Schnittstelle Direct3D 11, getmembership bysemantic-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetMemberBySemantic
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5af8b628247dcc89f8df99c6ffebb04d500e76a1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996218"
---
# <a name="id3dx11effectvariablegetmemberbysemantic-method"></a><span data-ttu-id="f6e8d-106">ID3DX11EffectVariable:: getmembership bysemantic-Methode</span><span class="sxs-lookup"><span data-stu-id="f6e8d-106">ID3DX11EffectVariable::GetMemberBySemantic method</span></span>

<span data-ttu-id="f6e8d-107">Einen Strukturmember nach Semantik erhalten.</span><span class="sxs-lookup"><span data-stu-id="f6e8d-107">Get a structure member by semantic.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6e8d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f6e8d-108">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetMemberBySemantic(
   LPCSTR Semantic
);
```



## <a name="parameters"></a><span data-ttu-id="f6e8d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f6e8d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6e8d-110">*Tischer*</span><span class="sxs-lookup"><span data-stu-id="f6e8d-110">*Semantic*</span></span> 
</dt> <dd>

<span data-ttu-id="f6e8d-111">Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f6e8d-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f6e8d-112">Die Semantik.</span><span class="sxs-lookup"><span data-stu-id="f6e8d-112">The semantic.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6e8d-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f6e8d-113">Return value</span></span>

<span data-ttu-id="f6e8d-114">Typ: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="f6e8d-114">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="f6e8d-115">Ein Zeiger auf eine [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="f6e8d-115">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f6e8d-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f6e8d-116">Remarks</span></span>

<span data-ttu-id="f6e8d-117">Wenn die Effekt Variable eine Struktur ist, verwenden Sie diese Methode, um ein Element nach angefügter Semantik zu suchen.</span><span class="sxs-lookup"><span data-stu-id="f6e8d-117">If the effect variable is an structure, use this method to look up a member by attached semantic.</span></span>

> [!Note]  
> <span data-ttu-id="f6e8d-118">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="f6e8d-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="f6e8d-119">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f6e8d-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="f6e8d-120">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="f6e8d-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f6e8d-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="f6e8d-121">Requirements</span></span>



| <span data-ttu-id="f6e8d-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f6e8d-122">Requirement</span></span> | <span data-ttu-id="f6e8d-123">Wert</span><span class="sxs-lookup"><span data-stu-id="f6e8d-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6e8d-124">Header</span><span class="sxs-lookup"><span data-stu-id="f6e8d-124">Header</span></span><br/>  | <dl> <span data-ttu-id="f6e8d-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6e8d-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="f6e8d-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f6e8d-126">Library</span></span><br/> | <dl> <span data-ttu-id="f6e8d-127"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="f6e8d-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6e8d-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f6e8d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6e8d-129">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="f6e8d-129">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

