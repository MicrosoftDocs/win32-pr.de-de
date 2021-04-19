---
description: Die findpinnumber-Methode ruft die Nummer einer angegebenen PIN für den Filter ab.
ms.assetid: c9366fcc-7b13-4e43-883e-6003c32fadec
title: CSource. findpinnumber-Methode (Quelle. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.FindPinNumber
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a6a71c65efd97c48eed58fb7d0b5aa8fcc2f178e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369380"
---
# <a name="csourcefindpinnumber-method"></a><span data-ttu-id="4f70b-103">CSource. findpinnumber-Methode</span><span class="sxs-lookup"><span data-stu-id="4f70b-103">CSource.FindPinNumber method</span></span>

<span data-ttu-id="4f70b-104">Die- `FindPinNumber` Methode ruft die Nummer einer angegebenen PIN für den Filter ab.</span><span class="sxs-lookup"><span data-stu-id="4f70b-104">The `FindPinNumber` method retrieves the number of a specified pin on the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f70b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f70b-105">Syntax</span></span>


```C++
int FindPinNumber(
   IPin *iPin
);
```



## <a name="parameters"></a><span data-ttu-id="4f70b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4f70b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f70b-107">*IPin*</span><span class="sxs-lookup"><span data-stu-id="4f70b-107">*iPin*</span></span> 
</dt> <dd>

<span data-ttu-id="4f70b-108">Ein Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der PIN.</span><span class="sxs-lookup"><span data-stu-id="4f70b-108">Pointer to the pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f70b-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4f70b-109">Return value</span></span>

<span data-ttu-id="4f70b-110">Gibt die PIN-Nummer oder 1 zurück, wenn die PIN in diesem Filter nicht gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="4f70b-110">Returns the pin number, or  1 if the pin is not found on this filter.</span></span> <span data-ttu-id="4f70b-111">Die erste PIN ist mit 0 nummeriert.</span><span class="sxs-lookup"><span data-stu-id="4f70b-111">The first pin is numbered zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f70b-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4f70b-112">Requirements</span></span>



| <span data-ttu-id="4f70b-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4f70b-113">Requirement</span></span> | <span data-ttu-id="4f70b-114">Wert</span><span class="sxs-lookup"><span data-stu-id="4f70b-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f70b-115">Header</span><span class="sxs-lookup"><span data-stu-id="4f70b-115">Header</span></span><br/>  | <dl> <span data-ttu-id="4f70b-116"><dt>Source. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4f70b-116"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="4f70b-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4f70b-117">Library</span></span><br/> | <dl> <span data-ttu-id="4f70b-118">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="4f70b-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f70b-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f70b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f70b-120">**CSource-Klasse**</span><span class="sxs-lookup"><span data-stu-id="4f70b-120">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 




