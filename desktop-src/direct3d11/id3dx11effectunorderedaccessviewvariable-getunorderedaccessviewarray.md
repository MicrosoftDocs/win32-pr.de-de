---
title: ID3DX11EffectUnorderedAccessViewVariable getunorderedaccessviewarray-Methode (D3dx11effect. h)
description: Abrufen eines Arrays von ungeordneten Access-Ansichten.
ms.assetid: 38f838bb-cdcb-43c2-8b98-a188f479e93d
keywords:
- Getunorderedaccessviewarray-Methode Direct3D 11
- Getunorderedaccessviewarray-Methode Direct3D 11, ID3DX11EffectUnorderedAccessViewVariable-Schnittstelle
- ID3DX11EffectUnorderedAccessViewVariable-Schnittstelle Direct3D 11, getunorderedaccessviewarray-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectUnorderedAccessViewVariable.GetUnorderedAccessViewArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c264b5652287676d0792027f4f0ea8921bdb92f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219589"
---
# <a name="id3dx11effectunorderedaccessviewvariablegetunorderedaccessviewarray-method"></a><span data-ttu-id="629e0-106">ID3DX11EffectUnorderedAccessViewVariable:: getunorderedaccessviewarray-Methode</span><span class="sxs-lookup"><span data-stu-id="629e0-106">ID3DX11EffectUnorderedAccessViewVariable::GetUnorderedAccessViewArray method</span></span>

<span data-ttu-id="629e0-107">Abrufen eines Arrays von ungeordneten Access-Ansichten.</span><span class="sxs-lookup"><span data-stu-id="629e0-107">Get an array of unordered-access-views.</span></span>

## <a name="syntax"></a><span data-ttu-id="629e0-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="629e0-108">Syntax</span></span>


```C++
HRESULT GetUnorderedAccessViewArray(
   ID3D11UnorderedAccessView **ppResources,
   UINT                      Offset,
   UINT                      Count
);
```



## <a name="parameters"></a><span data-ttu-id="629e0-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="629e0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="629e0-110">*ppresources*</span><span class="sxs-lookup"><span data-stu-id="629e0-110">*ppResources*</span></span> 
</dt> <dd>

<span data-ttu-id="629e0-111">Typ: **[ **ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)\*\***</span><span class="sxs-lookup"><span data-stu-id="629e0-111">Type: **[**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)\*\***</span></span>

<span data-ttu-id="629e0-112">Zeiger auf einen [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview) -Zeiger, der bei der Rückgabe auf das UAV-Array festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="629e0-112">Pointer to an [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview) pointer that will be set to the UAV array on return.</span></span>

</dd> <dt>

<span data-ttu-id="629e0-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="629e0-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="629e0-114">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="629e0-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="629e0-115">Index der ersten Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="629e0-115">Index of the first interface.</span></span>

</dd> <dt>

<span data-ttu-id="629e0-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="629e0-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="629e0-117">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="629e0-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="629e0-118">Anzahl der Elemente im Array.</span><span class="sxs-lookup"><span data-stu-id="629e0-118">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="629e0-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="629e0-119">Return value</span></span>

<span data-ttu-id="629e0-120">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="629e0-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="629e0-121">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="629e0-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="629e0-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="629e0-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="629e0-123">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="629e0-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="629e0-124">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="629e0-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="629e0-125">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="629e0-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="629e0-126">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="629e0-126">Requirements</span></span>



| <span data-ttu-id="629e0-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="629e0-127">Requirement</span></span> | <span data-ttu-id="629e0-128">Wert</span><span class="sxs-lookup"><span data-stu-id="629e0-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="629e0-129">Header</span><span class="sxs-lookup"><span data-stu-id="629e0-129">Header</span></span><br/>  | <dl> <span data-ttu-id="629e0-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="629e0-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="629e0-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="629e0-131">Library</span></span><br/> | <dl> <span data-ttu-id="629e0-132"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="629e0-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="629e0-133">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="629e0-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="629e0-134">ID3DX11EffectUnorderedAccessViewVariable</span><span class="sxs-lookup"><span data-stu-id="629e0-134">ID3DX11EffectUnorderedAccessViewVariable</span></span>](id3dx11effectunorderedaccessviewvariable.md)
</dt> </dl>

 

