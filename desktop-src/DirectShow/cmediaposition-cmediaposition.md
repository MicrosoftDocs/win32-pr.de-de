---
description: Erfahren Sie mehr über die Konstruktormethode cmediaposition. cmediaposition (ctlutil. h). Diese Methode verwendet die Parameter "pname" und "Punk".
ms.assetid: 18a7785c-30c6-43b8-9a41-542a8424522c
title: Cmediaposition. cmediaposition-Konstruktor (ctlutil. h)-pName, Punk-Parameter
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
ms.openlocfilehash: e65f034e5f8857b21bc706bce45aa74c3c3cf966
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "106369345"
---
# <a name="cmediapositioncmediaposition-constructor-ctlutilh---pname-punk-parameters"></a><span data-ttu-id="756a1-104">Cmediaposition. cmediaposition-Konstruktor (ctlutil. h)-pName, Punk-Parameter</span><span class="sxs-lookup"><span data-stu-id="756a1-104">CMediaPosition.CMediaPosition constructor (Ctlutil.h) - pName, pUnk parameters</span></span>

<span data-ttu-id="756a1-105">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="756a1-105">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="756a1-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="756a1-106">Syntax</span></span>


```C++
CMediaPosition(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a><span data-ttu-id="756a1-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="756a1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="756a1-108">*pName*</span><span class="sxs-lookup"><span data-stu-id="756a1-108">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="756a1-109">Zeiger auf den Namen des Objekts, zu Debuggingzwecken.</span><span class="sxs-lookup"><span data-stu-id="756a1-109">Pointer to the name of the object, for debugging purposes.</span></span> <span data-ttu-id="756a1-110">Weisen Sie diesen Parameter im statischen Arbeitsspeicher zu.</span><span class="sxs-lookup"><span data-stu-id="756a1-110">Allocate this parameter in static memory.</span></span>

</dd> <dt>

<span data-ttu-id="756a1-111">*Kro*</span><span class="sxs-lookup"><span data-stu-id="756a1-111">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="756a1-112">Zeiger auf den Besitzer dieses Objekts oder **null** , wenn das Objekt nicht aggregiert wird.</span><span class="sxs-lookup"><span data-stu-id="756a1-112">Pointer to the owner of this object, or **NULL** if the object is not aggregated.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="756a1-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="756a1-113">Requirements</span></span>

| <span data-ttu-id="756a1-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="756a1-114">Requirement</span></span> | <span data-ttu-id="756a1-115">Wert</span><span class="sxs-lookup"><span data-stu-id="756a1-115">Value</span></span> |
|-|-|
| <span data-ttu-id="756a1-116">Header</span><span class="sxs-lookup"><span data-stu-id="756a1-116">Header</span></span> | <span data-ttu-id="756a1-117">Ctlutil. h (Include Streams. h)</span><span class="sxs-lookup"><span data-stu-id="756a1-117">Ctlutil.h (include Streams.h)</span></span> |
| <span data-ttu-id="756a1-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="756a1-118">Library</span></span>| <span data-ttu-id="756a1-119">"Straumbase. lib" (Einzelhandels Builds); "Straumbasd. lib" (Debugbuilds)</span><span class="sxs-lookup"><span data-stu-id="756a1-119">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="756a1-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="756a1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="756a1-121">**Cmediaposition-Klasse**</span><span class="sxs-lookup"><span data-stu-id="756a1-121">**CMediaPosition Class**</span></span>](cmediaposition.md)
</dt> </dl>

 

 




