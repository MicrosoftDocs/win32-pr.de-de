---
description: Erfahren Sie mehr über die Konstruktormethode cmediaposition. cmediaposition (ctlutil. h). Diese Methode verwendet die Parameter "pname", "Punk" und "PHR".
ms.assetid: 4074f513-d1e7-4311-8732-4d755e621e55
title: Cmediaposition. cmediaposition-Konstruktor (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.CMediaPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cb9d86a2403cd0e2e71130b51cdb87bad15c4e95
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "106363191"
---
# <a name="cmediapositioncmediaposition-constructor-ctlutilh---pname-punk-phr-parameters"></a><span data-ttu-id="49b39-104">Cmediaposition. cmediaposition-Konstruktor (ctlutil. h)-pName, Punk, PHR-Parameter</span><span class="sxs-lookup"><span data-stu-id="49b39-104">CMediaPosition.CMediaPosition constructor (Ctlutil.h) - pName, pUnk, phr parameters</span></span>

<span data-ttu-id="49b39-105">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="49b39-105">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="49b39-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="49b39-106">Syntax</span></span>


```C++
CMediaPosition(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="49b39-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="49b39-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49b39-108">*pName*</span><span class="sxs-lookup"><span data-stu-id="49b39-108">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="49b39-109">Zeiger auf den Namen des Objekts, zu Debuggingzwecken.</span><span class="sxs-lookup"><span data-stu-id="49b39-109">Pointer to the name of the object, for debugging purposes.</span></span> <span data-ttu-id="49b39-110">Weisen Sie diesen Parameter im statischen Arbeitsspeicher zu.</span><span class="sxs-lookup"><span data-stu-id="49b39-110">Allocate this parameter in static memory.</span></span>

</dd> <dt>

<span data-ttu-id="49b39-111">*Kro*</span><span class="sxs-lookup"><span data-stu-id="49b39-111">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="49b39-112">Zeiger auf den Besitzer dieses Objekts oder **null** , wenn das Objekt nicht aggregiert wird.</span><span class="sxs-lookup"><span data-stu-id="49b39-112">Pointer to the owner of this object, or **NULL** if the object is not aggregated.</span></span>

</dd> <dt>

<span data-ttu-id="49b39-113">*PHR*</span><span class="sxs-lookup"><span data-stu-id="49b39-113">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="49b39-114">Zeiger auf einen **HRESULT** -Wert.</span><span class="sxs-lookup"><span data-stu-id="49b39-114">Pointer to an **HRESULT** value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="49b39-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="49b39-115">Requirements</span></span>

| <span data-ttu-id="49b39-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="49b39-116">Requirement</span></span> | <span data-ttu-id="49b39-117">Wert</span><span class="sxs-lookup"><span data-stu-id="49b39-117">Value</span></span> |
|-|-|
| <span data-ttu-id="49b39-118">Header</span><span class="sxs-lookup"><span data-stu-id="49b39-118">Header</span></span> | <span data-ttu-id="49b39-119">Ctlutil. h (Include Streams. h)</span><span class="sxs-lookup"><span data-stu-id="49b39-119">Ctlutil.h (include Streams.h)</span></span> |
| <span data-ttu-id="49b39-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="49b39-120">Library</span></span>| <span data-ttu-id="49b39-121">"Straumbase. lib" (Einzelhandels Builds); "Straumbasd. lib" (Debugbuilds)</span><span class="sxs-lookup"><span data-stu-id="49b39-121">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="49b39-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="49b39-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49b39-123">**Cmediaposition-Klasse**</span><span class="sxs-lookup"><span data-stu-id="49b39-123">**CMediaPosition Class**</span></span>](cmediaposition.md)
</dt> </dl>

 

 




