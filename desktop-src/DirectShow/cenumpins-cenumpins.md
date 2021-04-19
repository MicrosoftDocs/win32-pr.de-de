---
description: Konstruktormethode.
ms.assetid: f696e433-b051-4de0-80e5-f9cd31fd0f23
title: Cenumpins. cenumpins-Konstruktor (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins.CEnumPins
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 536782de6992acfc1613d5866f13af658fba6e71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355955"
---
# <a name="cenumpinscenumpins-constructor"></a><span data-ttu-id="3e361-103">Cenumpins. cenumpins-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="3e361-103">CEnumPins.CEnumPins constructor</span></span>

<span data-ttu-id="3e361-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="3e361-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e361-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e361-105">Syntax</span></span>


```C++
CEnumPins(
   CBaseFilter *pFilter,
   CEnumPins   *pEnumPins
);
```



## <a name="parameters"></a><span data-ttu-id="3e361-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3e361-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e361-107">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="3e361-107">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="3e361-108">Zeiger auf den Filter, für den die Pins aufgelistet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3e361-108">Pointer to the filter on which to enumerate the pins.</span></span>

</dd> <dt>

<span data-ttu-id="3e361-109">*Anmeldungen*</span><span class="sxs-lookup"><span data-stu-id="3e361-109">*pEnumPins*</span></span> 
</dt> <dd>

<span data-ttu-id="3e361-110">Ein Zeiger auf die [**iumumpins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) -Schnittstelle eines Enumerators, der geklont werden soll, oder **null**.</span><span class="sxs-lookup"><span data-stu-id="3e361-110">Pointer to the [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) interface of an enumerator to clone, or **NULL**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3e361-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3e361-111">Remarks</span></span>

<span data-ttu-id="3e361-112">Wenn die *penumpins* **null** sind, initialisiert diese Methode den Enumerator bis zum Anfang der enumerationssequenz.</span><span class="sxs-lookup"><span data-stu-id="3e361-112">If *pEnumPins* is **NULL**, this method initializes the enumerator to the beginning of the enumeration sequence.</span></span> <span data-ttu-id="3e361-113">Andernfalls dupliziert Sie den internen Zustand des Enumerators, der durch *penumpins* angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3e361-113">Otherwise, it duplicates the internal state of the enumerator specified by *pEnumPins*.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e361-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3e361-114">Requirements</span></span>



| <span data-ttu-id="3e361-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3e361-115">Requirement</span></span> | <span data-ttu-id="3e361-116">Wert</span><span class="sxs-lookup"><span data-stu-id="3e361-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e361-117">Header</span><span class="sxs-lookup"><span data-stu-id="3e361-117">Header</span></span><br/>  | <dl> <span data-ttu-id="3e361-118"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3e361-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="3e361-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3e361-119">Library</span></span><br/> | <dl> <span data-ttu-id="3e361-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="3e361-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e361-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3e361-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e361-122">**Cenumpins-Klasse**</span><span class="sxs-lookup"><span data-stu-id="3e361-122">**CEnumPins Class**</span></span>](cenumpins.md)
</dt> </dl>

 

 




