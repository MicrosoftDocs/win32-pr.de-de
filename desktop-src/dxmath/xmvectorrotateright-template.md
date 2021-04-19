---
description: Dreht den Vektor nach rechts um eine angegebene Anzahl von 32-Bit-Elementen.
ms.assetid: 7493c1fe-2c3d-4eb6-bec1-02c066a70b9f
title: Xmvector rotateright-Vorlage (directxmath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa2c4e623a75015e8051a5a9ccf32f4715016b73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359819"
---
# <a name="xmvectorrotateright-template"></a><span data-ttu-id="29902-103">Xmvector rotateright-Vorlage</span><span class="sxs-lookup"><span data-stu-id="29902-103">XMVectorRotateRight template</span></span>

<span data-ttu-id="29902-104">Dreht den Vektor nach rechts um eine angegebene Anzahl von 32-Bit-Elementen.</span><span class="sxs-lookup"><span data-stu-id="29902-104">Rotates the vector right by a given number of 32-bit elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="29902-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="29902-105">Syntax</span></span>

``` syntax
template<uint32_t Elements> XMVECTOR XMVectorRotateRight(
  [in]  XMVECTOR V
);
```

## <a name="parameters"></a><span data-ttu-id="29902-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="29902-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29902-107"><span id="V"></span><span id="v"></span>*Ramelow*</span><span class="sxs-lookup"><span data-stu-id="29902-107"><span id="V"></span><span id="v"></span>*V*</span></span>
</dt> <dd>

<span data-ttu-id="29902-108">\[in \] Vektor zum Drehen nach rechts.</span><span class="sxs-lookup"><span data-stu-id="29902-108">\[in\] Vector to rotate right.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29902-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="29902-109">Return Value</span></span>

<span data-ttu-id="29902-110">Gibt den gedrehten [**xmvector**](xmvector-data-type.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="29902-110">Returns the rotated [**XMVECTOR**](xmvector-data-type.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="29902-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="29902-111">Remarks</span></span>

<span data-ttu-id="29902-112">Bei dieser Funktion handelt es sich um eine Vorlagen Version von [**xmvectorrotateright**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateright) , bei der das *Elements* -Argument ein Vorlagen Wert ist.</span><span class="sxs-lookup"><span data-stu-id="29902-112">This function is a template version of [**XMVectorRotateRight**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateright) where the *Elements* argument is a template value.</span></span>

> [!Note]  
> <span data-ttu-id="29902-113">Die `XMVectorRotateRight` Vorlage ist neu für directxmath und für xnamath 2. x nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="29902-113">The `XMVectorRotateRight` template is new for DirectXMath and is not available for XNAMath 2.x.</span></span>

 

<span data-ttu-id="29902-114">**Namespace**: Verwenden von DirectX</span><span class="sxs-lookup"><span data-stu-id="29902-114">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="29902-115">Plattformanforderungen</span><span class="sxs-lookup"><span data-stu-id="29902-115">Platform Requirements</span></span>

<span data-ttu-id="29902-116">Microsoft Visual Studio 2010 oder Microsoft Visual Studio 2012 mit dem Windows SDK für Windows 8.</span><span class="sxs-lookup"><span data-stu-id="29902-116">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="29902-117">Wird für Win32-Desktop-Apps, Windows Store-Apps und Windows Phone 8-Apps unterstützt.</span><span class="sxs-lookup"><span data-stu-id="29902-117">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="29902-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="29902-118">Requirements</span></span>



| <span data-ttu-id="29902-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="29902-119">Requirement</span></span> | <span data-ttu-id="29902-120">Wert</span><span class="sxs-lookup"><span data-stu-id="29902-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="29902-121">Header</span><span class="sxs-lookup"><span data-stu-id="29902-121">Header</span></span><br/> | <dl> <span data-ttu-id="29902-122"><dt>Directxmath. h</dt></span><span class="sxs-lookup"><span data-stu-id="29902-122"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29902-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="29902-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29902-124">Directxmath-Bibliotheks Vorlagen Funktionen</span><span class="sxs-lookup"><span data-stu-id="29902-124">DirectXMath Library Template Functions</span></span>](ovw-xnamath-templates.md)
</dt> <dt>

[<span data-ttu-id="29902-125">**Xmvector perstumm Zeichen**</span><span class="sxs-lookup"><span data-stu-id="29902-125">**XMVectorPermute**</span></span>](xmvectorpermute-template.md)
</dt> <dt>

[<span data-ttu-id="29902-126">**Xmvector rotateleft**</span><span class="sxs-lookup"><span data-stu-id="29902-126">**XMVectorRotateLeft**</span></span>](xmvectorrotateleft-template.md)
</dt> <dt>

[<span data-ttu-id="29902-127">**Xmvector shiftleft**</span><span class="sxs-lookup"><span data-stu-id="29902-127">**XMVectorShiftLeft**</span></span>](xmvectorshiftleft-template.md)
</dt> </dl>

 

 
