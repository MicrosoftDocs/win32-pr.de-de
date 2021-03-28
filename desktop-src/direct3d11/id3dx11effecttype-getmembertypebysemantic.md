---
title: ID3DX11EffectType getmembership typebysemantic-Methode (D3dx11effect. h)
description: Einen Elementtyp nach Semantik erhalten.
ms.assetid: d5fea2d9-8d08-4e02-a9c6-dbcfaaf4a7d1
keywords:
- Getmembership typebysemantic-Methode Direct3D 11
- Getmembership typebysemantic-Methode Direct3D 11, ID3DX11EffectType-Schnittstelle
- ID3DX11EffectType-Schnittstelle Direct3D 11, getmembership typebysemantic-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectType.GetMemberTypeBySemantic
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de5f0894c83ff2d0885ae3b951e0e324343fae8e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996187"
---
# <a name="id3dx11effecttypegetmembertypebysemantic-method"></a><span data-ttu-id="70fd2-106">ID3DX11EffectType:: getmembership typebysemantic-Methode</span><span class="sxs-lookup"><span data-stu-id="70fd2-106">ID3DX11EffectType::GetMemberTypeBySemantic method</span></span>

<span data-ttu-id="70fd2-107">Einen Elementtyp nach Semantik erhalten.</span><span class="sxs-lookup"><span data-stu-id="70fd2-107">Get a member type by semantic.</span></span>

## <a name="syntax"></a><span data-ttu-id="70fd2-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="70fd2-108">Syntax</span></span>


```C++
ID3DX11EffectType* GetMemberTypeBySemantic(
   LPCSTR Semantic
);
```



## <a name="parameters"></a><span data-ttu-id="70fd2-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="70fd2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70fd2-110">*Tischer*</span><span class="sxs-lookup"><span data-stu-id="70fd2-110">*Semantic*</span></span> 
</dt> <dd>

<span data-ttu-id="70fd2-111">Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="70fd2-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="70fd2-112">Eine Semantik.</span><span class="sxs-lookup"><span data-stu-id="70fd2-112">A semantic.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70fd2-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="70fd2-113">Return value</span></span>

<span data-ttu-id="70fd2-114">Typ: **[ **ID3DX11EffectType**](id3dx11effecttype.md)\***</span><span class="sxs-lookup"><span data-stu-id="70fd2-114">Type: **[**ID3DX11EffectType**](id3dx11effecttype.md)\***</span></span>

<span data-ttu-id="70fd2-115">Ein Zeiger auf eine [**ID3DX11EffectType**](id3dx11effecttype.md).</span><span class="sxs-lookup"><span data-stu-id="70fd2-115">A pointer to an [**ID3DX11EffectType**](id3dx11effecttype.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="70fd2-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="70fd2-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="70fd2-117">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="70fd2-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="70fd2-118">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="70fd2-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="70fd2-119">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="70fd2-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="70fd2-120">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="70fd2-120">Requirements</span></span>



| <span data-ttu-id="70fd2-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="70fd2-121">Requirement</span></span> | <span data-ttu-id="70fd2-122">Wert</span><span class="sxs-lookup"><span data-stu-id="70fd2-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70fd2-123">Header</span><span class="sxs-lookup"><span data-stu-id="70fd2-123">Header</span></span><br/>  | <dl> <span data-ttu-id="70fd2-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="70fd2-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="70fd2-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="70fd2-125">Library</span></span><br/> | <dl> <span data-ttu-id="70fd2-126"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="70fd2-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70fd2-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="70fd2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70fd2-128">ID3DX11EffectType</span><span class="sxs-lookup"><span data-stu-id="70fd2-128">ID3DX11EffectType</span></span>](id3dx11effecttype.md)
</dt> </dl>

 

