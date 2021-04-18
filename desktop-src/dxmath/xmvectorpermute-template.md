---
description: Permutes die Komponenten von zwei Vektoren, um einen neuen Vektor zu erstellen.
ms.assetid: m:microsoft.directx_sdk.template.xmvectorpermute(xmvector,xmvector)
title: Xmvector perstumm-Vorlage (directxmath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37271cbb165f1e9c1769ef3a55e47f1e07310a81
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352145"
---
# <a name="xmvectorpermute-template"></a><span data-ttu-id="7b0db-103">Xmvector perstumm-Vorlage</span><span class="sxs-lookup"><span data-stu-id="7b0db-103">XMVectorPermute template</span></span>

<span data-ttu-id="7b0db-104">Permutes die Komponenten von zwei Vektoren, um einen neuen Vektor zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7b0db-104">Permutes the components of two vectors to create a new vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b0db-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b0db-105">Syntax</span></span>

``` syntax
template<uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW> XMVECTOR XMVectorPermute(
  [in]  XMVECTOR V1,
  [in]  XMVECTOR V2
);
```

## <a name="parameters"></a><span data-ttu-id="7b0db-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7b0db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b0db-107"><span id="V1"></span><span id="v1"></span>*V1*</span><span class="sxs-lookup"><span data-stu-id="7b0db-107"><span id="V1"></span><span id="v1"></span>*V1*</span></span>
</dt> <dd>

<span data-ttu-id="7b0db-108">\[im \] ersten Vektor.</span><span class="sxs-lookup"><span data-stu-id="7b0db-108">\[in\] First vector.</span></span>

</dd> <dt>

<span data-ttu-id="7b0db-109"><span id="V2"></span><span id="v2"></span>*V2*</span><span class="sxs-lookup"><span data-stu-id="7b0db-109"><span id="V2"></span><span id="v2"></span>*V2*</span></span>
</dt> <dd>

<span data-ttu-id="7b0db-110">\[im \] zweiten Vektor.</span><span class="sxs-lookup"><span data-stu-id="7b0db-110">\[in\] Second vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b0db-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7b0db-111">Return Value</span></span>

<span data-ttu-id="7b0db-112">Gibt den permutierten Vektor zurück, der durch Kombinieren der Quell Vektoren entstanden ist.</span><span class="sxs-lookup"><span data-stu-id="7b0db-112">Returns the permuted vector that resulted from combining the source vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b0db-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7b0db-113">Remarks</span></span>

<span data-ttu-id="7b0db-114">Wenn alle 4 Indizes nur auf einen einzelnen Vektor verweisen (d. h., Sie befinden sich alle im Bereich von 0-3 oder alle im Bereich 4-7), verwenden Sie stattdessen [**xmvector Swizzle**](xmvectorswizzle-template.md) , um die Leistung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="7b0db-114">If all 4 indices reference only a single vector (i.e. they are all in the range 0-3 or all in the range 4-7), use [**XMVectorSwizzle**](xmvectorswizzle-template.md) instead for better performance.</span></span>

<span data-ttu-id="7b0db-115">Beachten Sie, dass die Bibliothek auf einigen Plattformen Vorlagen Spezialisierungs Vorlagen verwendet, um die Leistung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="7b0db-115">Note the library makes use of template specializations on some platforms to improve performance.</span></span> <span data-ttu-id="7b0db-116">Nicht jeder mögliche Spiegelungs Fall wird für diese besonderen Fälle implementiert. bevorzugen Sie daher permutes, bei denen das X-Element des resultierenden Vektors aus dem V1-Parameter und nicht aus dem V2-Parameter stammt.</span><span class="sxs-lookup"><span data-stu-id="7b0db-116">Not every possible mirror case is implemented for these special cases, so prefer permutes where the X element of the resulting vector comes from the V1 parameter rather than the V2 parameter.</span></span> <span data-ttu-id="7b0db-117">Verwenden Sie beispielsweise, `XMVectorPermute<0,1,4,5>(A,B);` um zu verwenden `XMVectorPermute(4,5,0,1)(B,A);` .</span><span class="sxs-lookup"><span data-stu-id="7b0db-117">For example, prefer using `XMVectorPermute<0,1,4,5>(A,B);` to `XMVectorPermute(4,5,0,1)(B,A);`.</span></span>

<span data-ttu-id="7b0db-118">Bei dieser Funktion handelt es sich um eine Vorlagen Version von [**xmvectorperstumm**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) , bei der die *perstumm \** Argumente Vorlagen Werte sind.</span><span class="sxs-lookup"><span data-stu-id="7b0db-118">This function is a template version of [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) where the *Permute\** arguments are template values.</span></span>

<span data-ttu-id="7b0db-119">Die [XM- \_ perstumm \_](ovw-xnamath-reference-constants.md) Konstanten werden zur Verwendung als Eingabewerte für *permutex*,*permutey*,*permutez* und *permutew* bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="7b0db-119">The [XM\_PERMUTE\_](ovw-xnamath-reference-constants.md) constants are provided to use as input values for *PermuteX*,*PermuteY*,*PermuteZ*, and *PermuteW*.</span></span>

> [!Note]  
> <span data-ttu-id="7b0db-120">Die `XMVectorPermute` Vorlage ist neu für directxmath und für xnamath 2. x nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7b0db-120">The `XMVectorPermute` template is new for DirectXMath and is not available for XNAMath 2.x.</span></span>

 

<span data-ttu-id="7b0db-121">**Namespace**: Verwenden von DirectX</span><span class="sxs-lookup"><span data-stu-id="7b0db-121">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="7b0db-122">Plattformanforderungen</span><span class="sxs-lookup"><span data-stu-id="7b0db-122">Platform Requirements</span></span>

<span data-ttu-id="7b0db-123">Microsoft Visual Studio 2010 oder Microsoft Visual Studio 2012 mit dem Windows SDK für Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7b0db-123">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="7b0db-124">Wird für Win32-Desktop-Apps, Windows Store-Apps und Windows Phone 8-Apps unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7b0db-124">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b0db-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7b0db-125">Requirements</span></span>



| <span data-ttu-id="7b0db-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7b0db-126">Requirement</span></span> | <span data-ttu-id="7b0db-127">Wert</span><span class="sxs-lookup"><span data-stu-id="7b0db-127">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b0db-128">Header</span><span class="sxs-lookup"><span data-stu-id="7b0db-128">Header</span></span><br/> | <dl> <span data-ttu-id="7b0db-129"><dt>Directxmath. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b0db-129"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b0db-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7b0db-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b0db-131">Directxmath-Bibliotheks Vorlagen Funktionen</span><span class="sxs-lookup"><span data-stu-id="7b0db-131">DirectXMath Library Template Functions</span></span>](ovw-xnamath-templates.md)
</dt> <dt>

[<span data-ttu-id="7b0db-132">**Xmvector Swizzle**</span><span class="sxs-lookup"><span data-stu-id="7b0db-132">**XMVectorSwizzle**</span></span>](xmvectorswizzle-template.md)
</dt> </dl>

 

 
