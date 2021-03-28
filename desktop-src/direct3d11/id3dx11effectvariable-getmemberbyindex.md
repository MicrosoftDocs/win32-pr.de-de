---
title: ID3DX11EffectVariable getmembership byindex-Methode (D3dx11effect. h)
description: Einen Strukturmember nach Index erhalten.
ms.assetid: 256f65aa-5f49-4b83-8dde-ddb6b31c581a
keywords:
- Getmembership byindex-Methode Direct3D 11
- Getmembership byindex-Methode Direct3D 11, ID3DX11EffectVariable-Schnittstelle
- ID3DX11EffectVariable-Schnittstelle Direct3D 11, getmembership byindex-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetMemberByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4be490251a83907dcd16231d62d492caf05768f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995979"
---
# <a name="id3dx11effectvariablegetmemberbyindex-method"></a><span data-ttu-id="fb3ff-106">ID3DX11EffectVariable:: getmembership byindex-Methode</span><span class="sxs-lookup"><span data-stu-id="fb3ff-106">ID3DX11EffectVariable::GetMemberByIndex method</span></span>

<span data-ttu-id="fb3ff-107">Einen Strukturmember nach Index erhalten.</span><span class="sxs-lookup"><span data-stu-id="fb3ff-107">Get a structure member by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb3ff-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb3ff-108">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetMemberByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="fb3ff-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb3ff-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb3ff-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="fb3ff-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="fb3ff-111">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fb3ff-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="fb3ff-112">Ein NULL basierter Index.</span><span class="sxs-lookup"><span data-stu-id="fb3ff-112">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb3ff-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fb3ff-113">Return value</span></span>

<span data-ttu-id="fb3ff-114">Typ: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="fb3ff-114">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="fb3ff-115">Ein Zeiger auf eine [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="fb3ff-115">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fb3ff-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fb3ff-116">Remarks</span></span>

<span data-ttu-id="fb3ff-117">Wenn die Effekt Variable eine Struktur ist, verwenden Sie diese Methode, um einen Member nach Index zu suchen.</span><span class="sxs-lookup"><span data-stu-id="fb3ff-117">If the effect variable is an structure, use this method to look up a member by index.</span></span>

> [!Note]  
> <span data-ttu-id="fb3ff-118">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="fb3ff-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="fb3ff-119">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="fb3ff-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="fb3ff-120">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="fb3ff-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fb3ff-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="fb3ff-121">Requirements</span></span>



| <span data-ttu-id="fb3ff-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fb3ff-122">Requirement</span></span> | <span data-ttu-id="fb3ff-123">Wert</span><span class="sxs-lookup"><span data-stu-id="fb3ff-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb3ff-124">Header</span><span class="sxs-lookup"><span data-stu-id="fb3ff-124">Header</span></span><br/>  | <dl> <span data-ttu-id="fb3ff-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb3ff-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="fb3ff-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fb3ff-126">Library</span></span><br/> | <dl> <span data-ttu-id="fb3ff-127"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="fb3ff-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb3ff-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="fb3ff-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb3ff-129">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="fb3ff-129">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

