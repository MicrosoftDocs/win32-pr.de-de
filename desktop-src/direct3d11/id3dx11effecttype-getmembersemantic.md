---
title: ID3DX11EffectType getmembership Semantic-Methode (D3dx11effect. h)
description: Die an einen Member angefügte Semantik wird angezeigt.
ms.assetid: e0666d4e-7510-4496-849e-a0531238b5f8
keywords:
- Getmembership Semantic-Methode Direct3D 11
- Getmembership Semantic-Methode Direct3D 11, ID3DX11EffectType-Schnittstelle
- ID3DX11EffectType-Schnittstelle Direct3D 11, getmembership Semantic-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectType.GetMemberSemantic
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6255860dc9f7dc5cf12742e6f40b7e5148a3f27c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995871"
---
# <a name="id3dx11effecttypegetmembersemantic-method"></a><span data-ttu-id="33ea8-106">ID3DX11EffectType:: getmembership Semantic-Methode</span><span class="sxs-lookup"><span data-stu-id="33ea8-106">ID3DX11EffectType::GetMemberSemantic method</span></span>

<span data-ttu-id="33ea8-107">Die an einen Member angefügte Semantik wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="33ea8-107">Get the semantic attached to a member.</span></span>

## <a name="syntax"></a><span data-ttu-id="33ea8-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="33ea8-108">Syntax</span></span>


```C++
LPCSTR GetMemberSemantic(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="33ea8-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="33ea8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33ea8-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="33ea8-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="33ea8-111">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="33ea8-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="33ea8-112">Ein NULL basierter Index.</span><span class="sxs-lookup"><span data-stu-id="33ea8-112">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33ea8-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="33ea8-113">Return value</span></span>

<span data-ttu-id="33ea8-114">Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="33ea8-114">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="33ea8-115">Eine Zeichenfolge, die die Semantik enthält.</span><span class="sxs-lookup"><span data-stu-id="33ea8-115">A string that contains the semantic.</span></span>

## <a name="remarks"></a><span data-ttu-id="33ea8-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="33ea8-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="33ea8-117">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="33ea8-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="33ea8-118">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="33ea8-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="33ea8-119">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="33ea8-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="33ea8-120">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="33ea8-120">Requirements</span></span>



| <span data-ttu-id="33ea8-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="33ea8-121">Requirement</span></span> | <span data-ttu-id="33ea8-122">Wert</span><span class="sxs-lookup"><span data-stu-id="33ea8-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33ea8-123">Header</span><span class="sxs-lookup"><span data-stu-id="33ea8-123">Header</span></span><br/>  | <dl> <span data-ttu-id="33ea8-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="33ea8-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="33ea8-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="33ea8-125">Library</span></span><br/> | <dl> <span data-ttu-id="33ea8-126"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="33ea8-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33ea8-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="33ea8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33ea8-128">ID3DX11EffectType</span><span class="sxs-lookup"><span data-stu-id="33ea8-128">ID3DX11EffectType</span></span>](id3dx11effecttype.md)
</dt> </dl>

 

