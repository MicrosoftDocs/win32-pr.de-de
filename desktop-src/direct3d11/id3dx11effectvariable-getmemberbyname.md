---
title: ID3DX11EffectVariable getmembership byname-Methode (D3dx11effect. h)
description: Einen Strukturmember anhand des Namens erhalten.
ms.assetid: 09f7f2f8-f55f-411c-8130-6ae44015d58a
keywords:
- Getmembership byname-Methode Direct3D 11
- Getmembership byname-Methode Direct3D 11, ID3DX11EffectVariable-Schnittstelle
- ID3DX11EffectVariable Interface Direct3D 11, getmembership byname-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetMemberByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9851a2f74502a79b5cc85c494e468c4a346798f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996282"
---
# <a name="id3dx11effectvariablegetmemberbyname-method"></a><span data-ttu-id="f77c1-106">ID3DX11EffectVariable:: getmembership byname-Methode</span><span class="sxs-lookup"><span data-stu-id="f77c1-106">ID3DX11EffectVariable::GetMemberByName method</span></span>

<span data-ttu-id="f77c1-107">Einen Strukturmember anhand des Namens erhalten.</span><span class="sxs-lookup"><span data-stu-id="f77c1-107">Get a structure member by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="f77c1-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f77c1-108">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetMemberByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="f77c1-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f77c1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f77c1-110">*Name*</span><span class="sxs-lookup"><span data-stu-id="f77c1-110">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="f77c1-111">Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f77c1-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f77c1-112">Elementname.</span><span class="sxs-lookup"><span data-stu-id="f77c1-112">Member name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f77c1-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f77c1-113">Return value</span></span>

<span data-ttu-id="f77c1-114">Typ: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="f77c1-114">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="f77c1-115">Ein Zeiger auf eine [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="f77c1-115">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f77c1-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f77c1-116">Remarks</span></span>

<span data-ttu-id="f77c1-117">Wenn die Effekt Variable eine Struktur ist, verwenden Sie diese Methode, um einen Member nach Namen zu suchen.</span><span class="sxs-lookup"><span data-stu-id="f77c1-117">If the effect variable is an structure, use this method to look up a member by name.</span></span>

> [!Note]  
> <span data-ttu-id="f77c1-118">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="f77c1-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="f77c1-119">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f77c1-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="f77c1-120">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="f77c1-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f77c1-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="f77c1-121">Requirements</span></span>



| <span data-ttu-id="f77c1-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f77c1-122">Requirement</span></span> | <span data-ttu-id="f77c1-123">Wert</span><span class="sxs-lookup"><span data-stu-id="f77c1-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f77c1-124">Header</span><span class="sxs-lookup"><span data-stu-id="f77c1-124">Header</span></span><br/>  | <dl> <span data-ttu-id="f77c1-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="f77c1-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="f77c1-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f77c1-126">Library</span></span><br/> | <dl> <span data-ttu-id="f77c1-127"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="f77c1-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f77c1-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f77c1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f77c1-129">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="f77c1-129">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

