---
title: ID3DX11EffectUnorderedAccessViewVariable-Methode für die Methode "stunorderedaccessviewarray" (D3dx11effect. h)
description: Legen Sie ein Array von ungeordneten Zugriffs Ansichten fest.
ms.assetid: 12d0da06-990a-42b2-9566-cc5136f48781
keywords:
- Methode "stunorderedaccessviewarray" Direct3D 11
- Methode "stunorderedaccessviewarray" Direct3D 11, ID3DX11EffectUnorderedAccessViewVariable-Schnittstelle
- ID3DX11EffectUnorderedAccessViewVariable Interface Direct3D 11, Methode "stunorderedaccessviewarray"
topic_type:
- apiref
api_name:
- ID3DX11EffectUnorderedAccessViewVariable.SetUnorderedAccessViewArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 053856f294906cf56acf1f38ca90663ebcc34051
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995829"
---
# <a name="id3dx11effectunorderedaccessviewvariablesetunorderedaccessviewarray-method"></a><span data-ttu-id="c438b-106">ID3DX11EffectUnorderedAccessViewVariable:: stunorderedaccessviewarray-Methode</span><span class="sxs-lookup"><span data-stu-id="c438b-106">ID3DX11EffectUnorderedAccessViewVariable::SetUnorderedAccessViewArray method</span></span>

<span data-ttu-id="c438b-107">Legen Sie ein Array von ungeordneten Zugriffs Ansichten fest.</span><span class="sxs-lookup"><span data-stu-id="c438b-107">Set an array of unordered-access-views.</span></span>

## <a name="syntax"></a><span data-ttu-id="c438b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c438b-108">Syntax</span></span>


```C++
HRESULT SetUnorderedAccessViewArray(
   ID3D11UnorderedAccessView **ppResources,
   UINT                      Offset,
   UINT                      Count
);
```



## <a name="parameters"></a><span data-ttu-id="c438b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c438b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c438b-110">*ppresources*</span><span class="sxs-lookup"><span data-stu-id="c438b-110">*ppResources*</span></span> 
</dt> <dd>

<span data-ttu-id="c438b-111">Typ: **[ **ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)\*\***</span><span class="sxs-lookup"><span data-stu-id="c438b-111">Type: **[**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)\*\***</span></span>

<span data-ttu-id="c438b-112">Ein Array von [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview) -Zeigern.</span><span class="sxs-lookup"><span data-stu-id="c438b-112">An array of [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview) pointers.</span></span>

</dd> <dt>

<span data-ttu-id="c438b-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="c438b-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="c438b-114">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c438b-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c438b-115">Index der ersten ungeordneten Zugriffs Ansicht.</span><span class="sxs-lookup"><span data-stu-id="c438b-115">Index of the first unordered-access-view.</span></span>

</dd> <dt>

<span data-ttu-id="c438b-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="c438b-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="c438b-117">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c438b-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c438b-118">Anzahl der Elemente im Array.</span><span class="sxs-lookup"><span data-stu-id="c438b-118">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c438b-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c438b-119">Return value</span></span>

<span data-ttu-id="c438b-120">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c438b-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c438b-121">Gibt einen der folgenden [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="c438b-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c438b-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c438b-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c438b-123">Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit.</span><span class="sxs-lookup"><span data-stu-id="c438b-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="c438b-124">Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c438b-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="c438b-125">Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="c438b-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c438b-126">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="c438b-126">Requirements</span></span>



| <span data-ttu-id="c438b-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c438b-127">Requirement</span></span> | <span data-ttu-id="c438b-128">Wert</span><span class="sxs-lookup"><span data-stu-id="c438b-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c438b-129">Header</span><span class="sxs-lookup"><span data-stu-id="c438b-129">Header</span></span><br/>  | <dl> <span data-ttu-id="c438b-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="c438b-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="c438b-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c438b-131">Library</span></span><br/> | <dl> <span data-ttu-id="c438b-132"><dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt></span><span class="sxs-lookup"><span data-stu-id="c438b-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c438b-133">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c438b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c438b-134">ID3DX11EffectUnorderedAccessViewVariable</span><span class="sxs-lookup"><span data-stu-id="c438b-134">ID3DX11EffectUnorderedAccessViewVariable</span></span>](id3dx11effectunorderedaccessviewvariable.md)
</dt> </dl>

 

