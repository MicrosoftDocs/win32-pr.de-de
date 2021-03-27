---
title: ID3DX11EffectVariable getElements-Methode (D3dx11effect. h)
description: Ein Array Element erhalten.
ms.assetid: 3edf2084-570a-4423-8205-0b94a2a0cfde
keywords:
- GetElements-Methode Direct3D 11
- GetElements-Methode Direct3D 11, ID3DX11EffectVariable-Schnittstelle
- ID3DX11EffectVariable Interface Direct3D 11, getElements-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetElement
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a5b887bb9e4c1d40f4d3eb0d36b9a7b4d2698b5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982137"
---
# <a name="id3dx11effectvariablegetelement-method"></a><span data-ttu-id="07215-106">ID3DX11EffectVariable:: getElements-Methode</span><span class="sxs-lookup"><span data-stu-id="07215-106">ID3DX11EffectVariable::GetElement method</span></span>

<span data-ttu-id="07215-107">Ein Array Element erhalten.</span><span class="sxs-lookup"><span data-stu-id="07215-107">Get an array element.</span></span>

## <a name="syntax"></a><span data-ttu-id="07215-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="07215-108">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetElement(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="07215-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="07215-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07215-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="07215-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="07215-111">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="07215-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="07215-112">Ein NULL basierter Index; andernfalls 0.</span><span class="sxs-lookup"><span data-stu-id="07215-112">A zero-based index; otherwise 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07215-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="07215-113">Return value</span></span>

<span data-ttu-id="07215-114">Typ: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="07215-114">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="07215-115">Ein Zeiger auf eine [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="07215-115">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="07215-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="07215-116">Remarks</span></span>

<span data-ttu-id="07215-117">Wenn die Effekt Variable ein Array ist, verwenden Sie diese Methode, um eines der-Elemente zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="07215-117">If the effect variable is an array, use this method to return one of the elements.</span></span>

> [!Note]  
> <span data-ttu-id="07215-118">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="07215-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="07215-119">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="07215-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="07215-120">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="07215-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="07215-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="07215-121">Requirements</span></span>



| <span data-ttu-id="07215-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="07215-122">Requirement</span></span> | <span data-ttu-id="07215-123">Wert</span><span class="sxs-lookup"><span data-stu-id="07215-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07215-124">Header</span><span class="sxs-lookup"><span data-stu-id="07215-124">Header</span></span><br/>  | <dl> <span data-ttu-id="07215-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="07215-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="07215-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="07215-126">Library</span></span><br/> | <dl> <span data-ttu-id="07215-127"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="07215-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07215-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="07215-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07215-129">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="07215-129">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

