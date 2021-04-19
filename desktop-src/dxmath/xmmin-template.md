---
description: Vergleicht zwei numerische Datentyp Instanzen oder zwei Instanzen eines Objekts, das eine Überladung von < unterstützt, und gibt die kleinere der beiden-Instanzen zurück. Der Datentyp der Argumente und der Rückgabewert sind identisch.
ms.assetid: m:microsoft.directx_sdk.reference.xmmin(t,t)
title: Xmmin-Vorlage (directxmath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 550fd93c9776ad8547502b50817446e64f9bdd64
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106363210"
---
# <a name="xmmin-template"></a><span data-ttu-id="b19f8-104">Xmmin-Vorlage</span><span class="sxs-lookup"><span data-stu-id="b19f8-104">XMMin template</span></span>

<span data-ttu-id="b19f8-105">Vergleicht zwei numerische Datentyp Instanzen oder zwei Instanzen eines Objekts, das eine Überladung von < unterstützt, und gibt die kleinere der beiden-Instanzen zurück.</span><span class="sxs-lookup"><span data-stu-id="b19f8-105">Compares two numeric data type instances, or two instances of an object which supports an overload of <, and returns the smaller one of the two instances.</span></span> <span data-ttu-id="b19f8-106">Der Datentyp der Argumente und der Rückgabewert sind identisch.</span><span class="sxs-lookup"><span data-stu-id="b19f8-106">The data type of the arguments and the return value is the same.</span></span>

## <a name="syntax"></a><span data-ttu-id="b19f8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b19f8-107">Syntax</span></span>

``` syntax
template<class T> T XMMin(
  [in]  T a,
  [in]  T b
);
```

## <a name="parameters"></a><span data-ttu-id="b19f8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b19f8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b19f8-109"><span id="a"></span><span id="A"></span>*ein*</span><span class="sxs-lookup"><span data-stu-id="b19f8-109"><span id="a"></span><span id="A"></span>*a*</span></span>
</dt> <dd>

<span data-ttu-id="b19f8-110">\[in \] gibt das erste von zwei-Objekten an.</span><span class="sxs-lookup"><span data-stu-id="b19f8-110">\[in\] Specifies the first of two objects.</span></span>

</dd> <dt>

<span data-ttu-id="b19f8-111"><span id="b"></span><span id="B"></span>*b*</span><span class="sxs-lookup"><span data-stu-id="b19f8-111"><span id="b"></span><span id="B"></span>*b*</span></span>
</dt> <dd>

<span data-ttu-id="b19f8-112">\[in \] gibt die zwei von zwei-Objekten an.</span><span class="sxs-lookup"><span data-stu-id="b19f8-112">\[in\] Specifies the two of two objects.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b19f8-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b19f8-113">Return Value</span></span>

<span data-ttu-id="b19f8-114">Gibt die kleinere der beiden Eingabe Objekte zurück.</span><span class="sxs-lookup"><span data-stu-id="b19f8-114">Returns the smaller of the two input objects.</span></span>

## <a name="remarks"></a><span data-ttu-id="b19f8-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b19f8-115">Remarks</span></span>

<span data-ttu-id="b19f8-116">`XMMin` ist eine Vorlage, und der T-Typ wird angegeben, wenn die Vorlage instanziiert wird.</span><span class="sxs-lookup"><span data-stu-id="b19f8-116">`XMMin` is a template and the T type is specified when the template is instantiated.</span></span>

> [!Note]  
> <span data-ttu-id="b19f8-117">Die `XMMin` Vorlage ist neu für directxmath und für xnamath 2. x nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b19f8-117">The `XMMin` template is new for DirectXMath and is not available for XNAMath 2.x.</span></span> <span data-ttu-id="b19f8-118">`XMMin` ist als Makro in xnamath 2. x verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b19f8-118">`XMMin` is available as a macro in XNAMath 2.x.</span></span>

 

> [!Note]  
> <span data-ttu-id="b19f8-119">Verwenden Sie idealerweise Std:: min anstelle von `XMMin` .</span><span class="sxs-lookup"><span data-stu-id="b19f8-119">Ideally use std::min instead of `XMMin`.</span></span> <span data-ttu-id="b19f8-120">Um Konflikte mit Windows-Headern mit Std:: min zu vermeiden, müssen Sie \# nominmax definieren, bevor Sie Windows-Header einschließen.</span><span class="sxs-lookup"><span data-stu-id="b19f8-120">To avoid conflicts with Windows headers with std::min, you need to \#define NOMINMAX before you include Windows headers.</span></span>

 

<span data-ttu-id="b19f8-121">**Namespace**: Verwenden von DirectX</span><span class="sxs-lookup"><span data-stu-id="b19f8-121">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="b19f8-122">Plattformanforderungen</span><span class="sxs-lookup"><span data-stu-id="b19f8-122">Platform Requirements</span></span>

<span data-ttu-id="b19f8-123">Microsoft Visual Studio 2010 oder Microsoft Visual Studio 2012 mit dem Windows SDK für Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b19f8-123">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="b19f8-124">Wird für Win32-Desktop-Apps, Windows Store-Apps und Windows Phone 8-Apps unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b19f8-124">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="b19f8-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b19f8-125">Requirements</span></span>



| <span data-ttu-id="b19f8-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b19f8-126">Requirement</span></span> | <span data-ttu-id="b19f8-127">Wert</span><span class="sxs-lookup"><span data-stu-id="b19f8-127">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b19f8-128">Header</span><span class="sxs-lookup"><span data-stu-id="b19f8-128">Header</span></span><br/> | <dl> <span data-ttu-id="b19f8-129"><dt>Directxmath. h</dt></span><span class="sxs-lookup"><span data-stu-id="b19f8-129"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b19f8-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b19f8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b19f8-131">Directxmath-Bibliotheks Vorlagen Funktionen</span><span class="sxs-lookup"><span data-stu-id="b19f8-131">DirectXMath Library Template Functions</span></span>](ovw-xnamath-templates.md)
</dt> <dt>

[<span data-ttu-id="b19f8-132">**Xmmax**</span><span class="sxs-lookup"><span data-stu-id="b19f8-132">**XMMax**</span></span>](xmmax-template.md)
</dt> </dl>

 

 




