---
description: Dreht einen Vektor nach links um eine bestimmte Anzahl von 32-Bit-Komponenten und fügt ausgewählte Elemente dieses Ergebnisses in einen anderen Vektor ein.
ms.assetid: m:microsoft.directx_sdk.template.xmvectorinsert(xmvector,xmvector)
title: Xmvector INSERT-Vorlage (directxmath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3250ad52ab19a127b110b02ecf71543f44708681
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354224"
---
# <a name="xmvectorinsert-template"></a><span data-ttu-id="34365-103">Xmvector INSERT-Vorlage</span><span class="sxs-lookup"><span data-stu-id="34365-103">XMVectorInsert template</span></span>

<span data-ttu-id="34365-104">Dreht einen Vektor nach links um eine bestimmte Anzahl von 32-Bit-Komponenten und fügt ausgewählte Elemente dieses Ergebnisses in einen anderen Vektor ein.</span><span class="sxs-lookup"><span data-stu-id="34365-104">Rotates a vector left by a given number of 32-bit components and insert selected elements of that result into another vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="34365-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="34365-105">Syntax</span></span>

``` syntax
template<uint32_t VSLeftRotateElements, uint32_t Select0, uint32_t Select1, uint32_t Select2, uint32_t Select3> XMVECTOR XMVectorInsert(
  [in]  XMVECTOR VD,
  [in]  XMVECTOR VS
);
```

## <a name="parameters"></a><span data-ttu-id="34365-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="34365-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34365-107"><span id="VD"></span><span id="vd"></span>*Abbiegen*</span><span class="sxs-lookup"><span data-stu-id="34365-107"><span id="VD"></span><span id="vd"></span>*VD*</span></span>
</dt> <dd>

<span data-ttu-id="34365-108">\[in \] Vektor, das in eingefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="34365-108">\[in\] Vector to insert into.</span></span>

</dd> <dt>

<span data-ttu-id="34365-109"><span id="VS"></span><span id="vs"></span>*Jews*</span><span class="sxs-lookup"><span data-stu-id="34365-109"><span id="VS"></span><span id="vs"></span>*VS*</span></span>
</dt> <dd>

<span data-ttu-id="34365-110">\[im \] Vektor zum Drehen nach links.</span><span class="sxs-lookup"><span data-stu-id="34365-110">\[in\] Vector to rotate left.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34365-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="34365-111">Return Value</span></span>

<span data-ttu-id="34365-112">Gibt den [**xmvector**](xmvector-data-type.md) zurück, der sich aus der Drehung und dem Einfügen ergibt.</span><span class="sxs-lookup"><span data-stu-id="34365-112">Returns the [**XMVECTOR**](xmvector-data-type.md) that results from the rotation and insertion.</span></span>

## <a name="remarks"></a><span data-ttu-id="34365-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="34365-113">Remarks</span></span>

<span data-ttu-id="34365-114">Bei dieser Funktion handelt es sich um eine Vorlagen Version von [**xmvectorinsert**](/windows/win32/api/directxmath/nf-directxmath-xmvectorinsert) , bei der die *Select \** -Argumente Vorlagen Werte sind.</span><span class="sxs-lookup"><span data-stu-id="34365-114">This function is a template version of [**XMVectorInsert**](/windows/win32/api/directxmath/nf-directxmath-xmvectorinsert) where the *Select\** arguments are template values.</span></span>

<span data-ttu-id="34365-115">Um die optimale Leistung zu erzielen, sollte das Ergebnis von `XMVectorInsert` zurück zu *VD* zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="34365-115">For best performance, the result of `XMVectorInsert` should be assigned back to *VD*.</span></span>

> [!Note]  
> <span data-ttu-id="34365-116">Die `XMVectorInsert` Vorlage ist neu für directxmath und für xnamath 2. x nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="34365-116">The `XMVectorInsert` template is new for DirectXMath and is not available for XNAMath 2.x.</span></span>

 

<span data-ttu-id="34365-117">**Namespace**: Verwenden von DirectX</span><span class="sxs-lookup"><span data-stu-id="34365-117">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="34365-118">Plattformanforderungen</span><span class="sxs-lookup"><span data-stu-id="34365-118">Platform Requirements</span></span>

<span data-ttu-id="34365-119">Microsoft Visual Studio 2010 oder Microsoft Visual Studio 2012 mit dem Windows SDK für Windows 8.</span><span class="sxs-lookup"><span data-stu-id="34365-119">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="34365-120">Wird für Win32-Desktop-Apps, Windows Store-Apps und Windows Phone 8-Apps unterstützt.</span><span class="sxs-lookup"><span data-stu-id="34365-120">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="34365-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="34365-121">Requirements</span></span>



| <span data-ttu-id="34365-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="34365-122">Requirement</span></span> | <span data-ttu-id="34365-123">Wert</span><span class="sxs-lookup"><span data-stu-id="34365-123">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="34365-124">Header</span><span class="sxs-lookup"><span data-stu-id="34365-124">Header</span></span><br/> | <dl> <span data-ttu-id="34365-125"><dt>Directxmath. h</dt></span><span class="sxs-lookup"><span data-stu-id="34365-125"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34365-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="34365-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34365-127">Directxmath-Bibliotheks Vorlagen Funktionen</span><span class="sxs-lookup"><span data-stu-id="34365-127">DirectXMath Library Template Functions</span></span>](ovw-xnamath-templates.md)
</dt> <dt>

[<span data-ttu-id="34365-128">**Xmvector perstumm Zeichen**</span><span class="sxs-lookup"><span data-stu-id="34365-128">**XMVectorPermute**</span></span>](xmvectorpermute-template.md)
</dt> <dt>

[<span data-ttu-id="34365-129">**Xmvector rotateleft**</span><span class="sxs-lookup"><span data-stu-id="34365-129">**XMVectorRotateLeft**</span></span>](xmvectorrotateleft-template.md)
</dt> <dt>

[<span data-ttu-id="34365-130">**Xmvector rotateright**</span><span class="sxs-lookup"><span data-stu-id="34365-130">**XMVectorRotateRight**</span></span>](xmvectorrotateright-template.md)
</dt> <dt>

[<span data-ttu-id="34365-131">**Xmvector shiftleft**</span><span class="sxs-lookup"><span data-stu-id="34365-131">**XMVectorShiftLeft**</span></span>](xmvectorshiftleft-template.md)
</dt> </dl>

 

 
