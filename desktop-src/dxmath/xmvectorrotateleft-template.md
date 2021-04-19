---
description: Dreht den Vektor um eine angegebene Anzahl von 32-Bit-Elementen nach links.
ms.assetid: ba3698ed-212d-4ef0-846a-4099d0e1abec
title: Xmvector rotateleft-Vorlage (directxmath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e5b52fccebeb93803fdc33346fa4ee5e873c1d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368577"
---
# <a name="xmvectorrotateleft-template"></a><span data-ttu-id="bdd48-103">Xmvector rotateleft-Vorlage</span><span class="sxs-lookup"><span data-stu-id="bdd48-103">XMVectorRotateLeft template</span></span>

<span data-ttu-id="bdd48-104">Dreht den Vektor um eine angegebene Anzahl von 32-Bit-Elementen nach links.</span><span class="sxs-lookup"><span data-stu-id="bdd48-104">Rotates the vector left by a given number of 32-bit elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdd48-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bdd48-105">Syntax</span></span>

``` syntax
template<uint32_t Elements> XMVECTOR XMVectorRotateLeft(
  [in]  XMVECTOR V
);
```

## <a name="parameters"></a><span data-ttu-id="bdd48-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bdd48-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdd48-107"><span id="V"></span><span id="v"></span>*Ramelow*</span><span class="sxs-lookup"><span data-stu-id="bdd48-107"><span id="V"></span><span id="v"></span>*V*</span></span>
</dt> <dd>

<span data-ttu-id="bdd48-108">\[im \] Vektor zum Drehen nach links.</span><span class="sxs-lookup"><span data-stu-id="bdd48-108">\[in\] Vector to rotate left.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdd48-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bdd48-109">Return Value</span></span>

<span data-ttu-id="bdd48-110">Gibt den gedrehten [**xmvector**](xmvector-data-type.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="bdd48-110">Returns the rotated [**XMVECTOR**](xmvector-data-type.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="bdd48-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bdd48-111">Remarks</span></span>

<span data-ttu-id="bdd48-112">Bei dieser Funktion handelt es sich um eine Vorlagen Version von [**xmvectorrotateleft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateleft) , bei der das *Elements* -Argument ein Vorlagen Wert ist.</span><span class="sxs-lookup"><span data-stu-id="bdd48-112">This function is a template version of [**XMVectorRotateLeft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateleft) where the *Elements* argument is a template value.</span></span>

> [!Note]  
> <span data-ttu-id="bdd48-113">Die `XMVectorRotateLeft` Vorlage ist neu für directxmath und für xnamath 2. x nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bdd48-113">The `XMVectorRotateLeft` template is new for DirectXMath and is not available for XNAMath 2.x.</span></span>

 

<span data-ttu-id="bdd48-114">**Namespace**: Verwenden von DirectX</span><span class="sxs-lookup"><span data-stu-id="bdd48-114">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="bdd48-115">Plattformanforderungen</span><span class="sxs-lookup"><span data-stu-id="bdd48-115">Platform Requirements</span></span>

<span data-ttu-id="bdd48-116">Microsoft Visual Studio 2010 oder Microsoft Visual Studio 2012 mit dem Windows SDK für Windows 8.</span><span class="sxs-lookup"><span data-stu-id="bdd48-116">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="bdd48-117">Wird für Win32-Desktop-Apps, Windows Store-Apps und Windows Phone 8-Apps unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bdd48-117">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdd48-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bdd48-118">Requirements</span></span>



| <span data-ttu-id="bdd48-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bdd48-119">Requirement</span></span> | <span data-ttu-id="bdd48-120">Wert</span><span class="sxs-lookup"><span data-stu-id="bdd48-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdd48-121">Header</span><span class="sxs-lookup"><span data-stu-id="bdd48-121">Header</span></span><br/> | <dl> <span data-ttu-id="bdd48-122"><dt>Directxmath. h</dt></span><span class="sxs-lookup"><span data-stu-id="bdd48-122"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdd48-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bdd48-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdd48-124">Directxmath-Bibliotheks Vorlagen Funktionen</span><span class="sxs-lookup"><span data-stu-id="bdd48-124">DirectXMath Library Template Functions</span></span>](ovw-xnamath-templates.md)
</dt> <dt>

[<span data-ttu-id="bdd48-125">**Xmvector perstumm Zeichen**</span><span class="sxs-lookup"><span data-stu-id="bdd48-125">**XMVectorPermute**</span></span>](xmvectorpermute-template.md)
</dt> <dt>

[<span data-ttu-id="bdd48-126">**Xmvector rotateright**</span><span class="sxs-lookup"><span data-stu-id="bdd48-126">**XMVectorRotateRight**</span></span>](xmvectorrotateright-template.md)
</dt> <dt>

[<span data-ttu-id="bdd48-127">**Xmvector shiftleft**</span><span class="sxs-lookup"><span data-stu-id="bdd48-127">**XMVectorShiftLeft**</span></span>](xmvectorshiftleft-template.md)
</dt> </dl>

 

 
