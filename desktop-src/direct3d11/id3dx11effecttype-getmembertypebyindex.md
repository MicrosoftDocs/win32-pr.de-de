---
title: ID3DX11EffectType getmembership typebyindex-Methode (D3dx11effect. h)
description: Einen Elementtyp nach Index erhalten.
ms.assetid: 6421f08f-0236-4d8f-b3c2-ef7ec5ffe2a1
keywords:
- Getmembership typebyindex-Methode Direct3D 11
- Getmembership typebyindex-Methode Direct3D 11, ID3DX11EffectType-Schnittstelle
- ID3DX11EffectType Interface Direct3D 11, getmembership typebyindex-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectType.GetMemberTypeByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da5023e064539f57af9998c788385f2a1316433f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530968"
---
# <a name="id3dx11effecttypegetmembertypebyindex-method"></a><span data-ttu-id="e98cc-106">ID3DX11EffectType:: getmembership typebyindex-Methode</span><span class="sxs-lookup"><span data-stu-id="e98cc-106">ID3DX11EffectType::GetMemberTypeByIndex method</span></span>

<span data-ttu-id="e98cc-107">Einen Elementtyp nach Index erhalten.</span><span class="sxs-lookup"><span data-stu-id="e98cc-107">Get a member type by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="e98cc-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e98cc-108">Syntax</span></span>


```C++
ID3DX11EffectType* GetMemberTypeByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="e98cc-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e98cc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e98cc-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="e98cc-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="e98cc-111">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e98cc-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e98cc-112">Ein NULL basierter Index.</span><span class="sxs-lookup"><span data-stu-id="e98cc-112">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e98cc-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e98cc-113">Return value</span></span>

<span data-ttu-id="e98cc-114">Typ: **[ **ID3DX11EffectType**](id3dx11effecttype.md)\***</span><span class="sxs-lookup"><span data-stu-id="e98cc-114">Type: **[**ID3DX11EffectType**](id3dx11effecttype.md)\***</span></span>

<span data-ttu-id="e98cc-115">Ein Zeiger auf eine [**ID3DX11EffectType**](id3dx11effecttype.md).</span><span class="sxs-lookup"><span data-stu-id="e98cc-115">A pointer to an [**ID3DX11EffectType**](id3dx11effecttype.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e98cc-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e98cc-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e98cc-117">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="e98cc-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="e98cc-118">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e98cc-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="e98cc-119">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="e98cc-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e98cc-120">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="e98cc-120">Requirements</span></span>



| <span data-ttu-id="e98cc-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e98cc-121">Requirement</span></span> | <span data-ttu-id="e98cc-122">Wert</span><span class="sxs-lookup"><span data-stu-id="e98cc-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e98cc-123">Header</span><span class="sxs-lookup"><span data-stu-id="e98cc-123">Header</span></span><br/>  | <dl> <span data-ttu-id="e98cc-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="e98cc-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="e98cc-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e98cc-125">Library</span></span><br/> | <dl> <span data-ttu-id="e98cc-126"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="e98cc-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e98cc-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e98cc-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e98cc-128">ID3DX11EffectType</span><span class="sxs-lookup"><span data-stu-id="e98cc-128">ID3DX11EffectType</span></span>](id3dx11effecttype.md)
</dt> </dl>

 

