---
description: Verschiebt einen Vektor um eine bestimmte Anzahl von 32-Bit-Elementen nach links und füllt die freigegebenen Elemente mit Elementen aus einem zweiten Vektor.
ms.assetid: m:microsoft.directx_sdk.template.xmvectorshiftleft(xmvector,xmvector)
title: Xmvector shiftleft-Vorlage (directxmath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 115604871d9e8402157a82bf3c420e5762b3a424
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371595"
---
# <a name="xmvectorshiftleft-template"></a><span data-ttu-id="a12f5-103">Xmvector shiftleft-Vorlage</span><span class="sxs-lookup"><span data-stu-id="a12f5-103">XMVectorShiftLeft template</span></span>

<span data-ttu-id="a12f5-104">Verschiebt einen Vektor um eine bestimmte Anzahl von 32-Bit-Elementen nach links und füllt die freigegebenen Elemente mit Elementen aus einem zweiten Vektor.</span><span class="sxs-lookup"><span data-stu-id="a12f5-104">Shifts a vector left by a given number of 32-bit elements, filling the vacated elements with elements from a second vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="a12f5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a12f5-105">Syntax</span></span>

``` syntax
template<uint32_t Elements> XMVECTOR XMVectorShiftLeft(
  [in]  XMVECTOR V1,
  [in]  XMVECTOR V2
);
```

## <a name="parameters"></a><span data-ttu-id="a12f5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a12f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a12f5-107"><span id="V1"></span><span id="v1"></span>*V1*</span><span class="sxs-lookup"><span data-stu-id="a12f5-107"><span id="V1"></span><span id="v1"></span>*V1*</span></span>
</dt> <dd>

<span data-ttu-id="a12f5-108">\[im \] Vektor nach links verschieben.</span><span class="sxs-lookup"><span data-stu-id="a12f5-108">\[in\] Vector to shift left.</span></span>

</dd> <dt>

<span data-ttu-id="a12f5-109"><span id="V2"></span><span id="v2"></span>*V2*</span><span class="sxs-lookup"><span data-stu-id="a12f5-109"><span id="V2"></span><span id="v2"></span>*V2*</span></span>
</dt> <dd>

<span data-ttu-id="a12f5-110">\[in \] Vector, das verwendet wird, um die frei gewordenen Komponenten von v1 auszufüllen, nachdem es nach links verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="a12f5-110">\[in\] Vector used to fill in the vacated components of V1 after it is shifted left.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a12f5-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a12f5-111">Return Value</span></span>

<span data-ttu-id="a12f5-112">Gibt den verschobenen und gefüllten [**xmvector**](xmvector-data-type.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="a12f5-112">Returns the shifted and filled in [**XMVECTOR**](xmvector-data-type.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a12f5-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a12f5-113">Remarks</span></span>

<span data-ttu-id="a12f5-114">Bei dieser Funktion handelt es sich um eine Vorlagen Version von [**xmvectorshiftleft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorshiftleft) , wobei das *Element* -Argument ein Vorlagen Wert ist.</span><span class="sxs-lookup"><span data-stu-id="a12f5-114">This function is a template version of [**XMVectorShiftLeft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorshiftleft) where the *Elements* argument is a template value.</span></span>

> [!Note]  
> <span data-ttu-id="a12f5-115">Die `XMVectorShiftLeft` Vorlage ist neu für directxmath und für xnamath 2. x nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a12f5-115">The `XMVectorShiftLeft` template is new for DirectXMath and is not available for XNAMath 2.x.</span></span>

 

<span data-ttu-id="a12f5-116">**Namespace**: Verwenden von DirectX</span><span class="sxs-lookup"><span data-stu-id="a12f5-116">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="a12f5-117">Plattformanforderungen</span><span class="sxs-lookup"><span data-stu-id="a12f5-117">Platform Requirements</span></span>

<span data-ttu-id="a12f5-118">Microsoft Visual Studio 2010 oder Microsoft Visual Studio 2012 mit dem Windows SDK für Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a12f5-118">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="a12f5-119">Wird für Win32-Desktop-Apps, Windows Store-Apps und Windows Phone 8-Apps unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a12f5-119">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="a12f5-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a12f5-120">Requirements</span></span>



| <span data-ttu-id="a12f5-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a12f5-121">Requirement</span></span> | <span data-ttu-id="a12f5-122">Wert</span><span class="sxs-lookup"><span data-stu-id="a12f5-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a12f5-123">Header</span><span class="sxs-lookup"><span data-stu-id="a12f5-123">Header</span></span><br/> | <dl> <span data-ttu-id="a12f5-124"><dt>Directxmath. h</dt></span><span class="sxs-lookup"><span data-stu-id="a12f5-124"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a12f5-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a12f5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a12f5-126">Directxmath-Bibliotheks Vorlagen Funktionen</span><span class="sxs-lookup"><span data-stu-id="a12f5-126">DirectXMath Library Template Functions</span></span>](ovw-xnamath-templates.md)
</dt> <dt>

[<span data-ttu-id="a12f5-127">**Xmvector perstumm Zeichen**</span><span class="sxs-lookup"><span data-stu-id="a12f5-127">**XMVectorPermute**</span></span>](xmvectorpermute-template.md)
</dt> <dt>

[<span data-ttu-id="a12f5-128">**Xmvector rotateleft**</span><span class="sxs-lookup"><span data-stu-id="a12f5-128">**XMVectorRotateLeft**</span></span>](xmvectorrotateleft-template.md)
</dt> <dt>

[<span data-ttu-id="a12f5-129">**Xmvector rotateright**</span><span class="sxs-lookup"><span data-stu-id="a12f5-129">**XMVectorRotateRight**</span></span>](xmvectorrotateright-template.md)
</dt> </dl>

 

 
