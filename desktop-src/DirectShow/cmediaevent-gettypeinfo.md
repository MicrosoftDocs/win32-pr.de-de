---
description: Ruft ein Type-Information-Objekt ab, das die Typinformationen für eine Schnittstelle abrufen kann.
ms.assetid: d54042d5-e9d3-415c-b90d-1fe7d38164f5
title: Cmediaevent. gettypeingefo-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent.GetTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e351d3b8b06bea4f6f9a1a160802972a8fa50f82
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361462"
---
# <a name="cmediaeventgettypeinfo-method"></a><span data-ttu-id="03ea1-103">Cmediaevent. gettypeingefo-Methode</span><span class="sxs-lookup"><span data-stu-id="03ea1-103">CMediaEvent.GetTypeInfo method</span></span>

<span data-ttu-id="03ea1-104">Ruft ein Type-Information-Objekt ab, das die Typinformationen für eine Schnittstelle abrufen kann.</span><span class="sxs-lookup"><span data-stu-id="03ea1-104">Retrieves a type-information object, which can retrieve the type information for an interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="03ea1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="03ea1-105">Syntax</span></span>


```C++
HRESULT GetTypeInfo(
   UINT      itinfo,
   LCID      lcid,
   ITypeInfo **pptinfo
);
```



## <a name="parameters"></a><span data-ttu-id="03ea1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="03ea1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03ea1-107">*itinfo*</span><span class="sxs-lookup"><span data-stu-id="03ea1-107">*itinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="03ea1-108">Typinformationen, die zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="03ea1-108">Type information to return.</span></span> <span data-ttu-id="03ea1-109">Übergeben Sie NULL, um Typinformationen für die **IDispatch** -Implementierung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="03ea1-109">Pass zero to retrieve type information for the **IDispatch** implementation.</span></span>

</dd> <dt>

<span data-ttu-id="03ea1-110">*lcid*</span><span class="sxs-lookup"><span data-stu-id="03ea1-110">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="03ea1-111">Die Gebiets Schema-ID für die Typinformationen.</span><span class="sxs-lookup"><span data-stu-id="03ea1-111">Locale ID for the type information.</span></span> <span data-ttu-id="03ea1-112">Bei Klassen, die lokalisierte Elementnamen unterstützen, kann ein Objekt möglicherweise unterschiedliche Typinformationen für verschiedene Sprachen zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="03ea1-112">For classes that support localized member names, an object might be able to return different type information for different languages.</span></span> <span data-ttu-id="03ea1-113">Für Klassen, die keine lokalisierten Elementnamen unterstützen, kann dieser Parameter ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="03ea1-113">For classes that do not support localized member names, this parameter can be ignored.</span></span>

</dd> <dt>

<span data-ttu-id="03ea1-114">*pptinfo*</span><span class="sxs-lookup"><span data-stu-id="03ea1-114">*pptinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="03ea1-115">Adresse eines Zeigers auf das angeforderte Type-Information-Objekt.</span><span class="sxs-lookup"><span data-stu-id="03ea1-115">Address of a pointer to the type-information object requested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03ea1-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="03ea1-116">Return value</span></span>

<span data-ttu-id="03ea1-117">Gibt einen E-Zeiger zurück, \_ Wenn *pptinfo* ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="03ea1-117">Returns an E\_POINTER if *pptinfo* is invalid.</span></span> <span data-ttu-id="03ea1-118">Gibt den Typ \_ E \_ elementnotfound zurück, wenn *itinfo* nicht 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="03ea1-118">Returns TYPE\_E\_ELEMENTNOTFOUND if *itinfo* is not zero.</span></span> <span data-ttu-id="03ea1-119">Gibt S \_ OK zurück, wenn erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="03ea1-119">Returns S\_OK if is successful.</span></span> <span data-ttu-id="03ea1-120">Andernfalls wird ein **HRESULT** von einem der Aufrufe zurückgegeben, um den Typ abzurufen.</span><span class="sxs-lookup"><span data-stu-id="03ea1-120">Otherwise, returns an **HRESULT** from one of the calls to retrieve the type.</span></span>

## <a name="requirements"></a><span data-ttu-id="03ea1-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="03ea1-121">Requirements</span></span>



| <span data-ttu-id="03ea1-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="03ea1-122">Requirement</span></span> | <span data-ttu-id="03ea1-123">Wert</span><span class="sxs-lookup"><span data-stu-id="03ea1-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03ea1-124">Header</span><span class="sxs-lookup"><span data-stu-id="03ea1-124">Header</span></span><br/>  | <dl> <span data-ttu-id="03ea1-125"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="03ea1-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="03ea1-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="03ea1-126">Library</span></span><br/> | <dl> <span data-ttu-id="03ea1-127">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="03ea1-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03ea1-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="03ea1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03ea1-129">**Cmediaevent-Klasse**</span><span class="sxs-lookup"><span data-stu-id="03ea1-129">**CMediaEvent Class**</span></span>](cmediaevent.md)
</dt> </dl>

 

 




