---
description: Schwimmt einen Vektor.
ms.assetid: 75608e80-5911-45a8-beca-ceac1f4d2c1c
title: Xmvector Swizzle-Vorlage (directxmath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8e872d76f3251eccc8616c143c645b388e2dca4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352144"
---
# <a name="xmvectorswizzle-template"></a><span data-ttu-id="28599-103">Xmvector Swizzle-Vorlage</span><span class="sxs-lookup"><span data-stu-id="28599-103">XMVectorSwizzle template</span></span>

<span data-ttu-id="28599-104">Schwimmt einen Vektor.</span><span class="sxs-lookup"><span data-stu-id="28599-104">Swizzles a vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="28599-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="28599-105">Syntax</span></span>

``` syntax
template<uint32_t SwizzleX, uint32_t SwizzleY, uint32_t SwizzleZ, uint32_t SwizzleW> XMVECTOR XMVectorSwizzle(
  [in]  XMVECTOR V
);
```

## <a name="parameters"></a><span data-ttu-id="28599-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="28599-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28599-107"><span id="V"></span><span id="v"></span>*Ramelow*</span><span class="sxs-lookup"><span data-stu-id="28599-107"><span id="V"></span><span id="v"></span>*V*</span></span>
</dt> <dd>

<span data-ttu-id="28599-108">\[in \] Vektor zum Schwenken.</span><span class="sxs-lookup"><span data-stu-id="28599-108">\[in\] Vector to swizzle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28599-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="28599-109">Return Value</span></span>

<span data-ttu-id="28599-110">Gibt den von einem Streifen geleiteten [**xmvector**](xmvector-data-type.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="28599-110">Returns the swizzled [**XMVECTOR**](xmvector-data-type.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="28599-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="28599-111">Remarks</span></span>

<span data-ttu-id="28599-112">Bei dieser Funktion handelt es sich um eine Vorlagen Version von [**xmvectorswizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) , bei der die *\* swidgumente* Vorlagen Werte sind.</span><span class="sxs-lookup"><span data-stu-id="28599-112">This function is a template version of [**XMVectorSwizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) where the *Swizzle\** arguments are template values.</span></span>

<span data-ttu-id="28599-113">`XM_SWIZZLE_X`, `XM_SWIZZLE_Y` , `XM_SWIZZLE_Z` und `XM_SWIZZLE_W` sind Konstanten, die für die Verwendung mit 0, 1, 2 bzw. 3 ausgewertet werden `XMVectorSwizzle` .</span><span class="sxs-lookup"><span data-stu-id="28599-113">`XM_SWIZZLE_X`, `XM_SWIZZLE_Y`, `XM_SWIZZLE_Z`, and `XM_SWIZZLE_W` are constants which evaluate to 0, 1, 2, and 3 respectively for use with `XMVectorSwizzle`.</span></span> <span data-ttu-id="28599-114">Dies ist identisch mit `XM_PERMUTE_0X` , `XM_PERMUTE_0Y` , `XM_PERMUTE_0Z` und `XM_PERMUTE_0W` .</span><span class="sxs-lookup"><span data-stu-id="28599-114">This is identical to `XM_PERMUTE_0X`, `XM_PERMUTE_0Y`, `XM_PERMUTE_0Z`, and `XM_PERMUTE_0W`.</span></span>

> [!Note]  
> <span data-ttu-id="28599-115">Die `XMVectorSwizzle` Vorlage ist neu für directxmath und für xnamath 2. x nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="28599-115">The `XMVectorSwizzle` template is new for DirectXMath and is not available for XNAMath 2.x.</span></span>

 

<span data-ttu-id="28599-116">**Namespace**: Verwenden von DirectX</span><span class="sxs-lookup"><span data-stu-id="28599-116">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="28599-117">Plattformanforderungen</span><span class="sxs-lookup"><span data-stu-id="28599-117">Platform Requirements</span></span>

<span data-ttu-id="28599-118">Microsoft Visual Studio 2010 oder Microsoft Visual Studio 2012 mit dem Windows SDK für Windows 8.</span><span class="sxs-lookup"><span data-stu-id="28599-118">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="28599-119">Wird für Win32-Desktop-Apps, Windows Store-Apps und Windows Phone 8-Apps unterstützt.</span><span class="sxs-lookup"><span data-stu-id="28599-119">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="28599-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="28599-120">Requirements</span></span>



| <span data-ttu-id="28599-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="28599-121">Requirement</span></span> | <span data-ttu-id="28599-122">Wert</span><span class="sxs-lookup"><span data-stu-id="28599-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="28599-123">Header</span><span class="sxs-lookup"><span data-stu-id="28599-123">Header</span></span><br/> | <dl> <span data-ttu-id="28599-124"><dt>Directxmath. h</dt></span><span class="sxs-lookup"><span data-stu-id="28599-124"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28599-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="28599-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28599-126">Directxmath-Bibliotheks Vorlagen Funktionen</span><span class="sxs-lookup"><span data-stu-id="28599-126">DirectXMath Library Template Functions</span></span>](ovw-xnamath-templates.md)
</dt> <dt>

[<span data-ttu-id="28599-127">**Xmvector perstumm Zeichen**</span><span class="sxs-lookup"><span data-stu-id="28599-127">**XMVectorPermute**</span></span>](xmvectorpermute-template.md)
</dt> </dl>

 

 
