---
description: 'CMediaEvent.GetTypeInfoCount-Methode: Ruft die Anzahl der Typinformationsschnittstellen ab, die von einem -Objekt bereitgestellt werden.'
ms.assetid: e16bc324-bb49-4df2-afeb-2c2cd1620693
title: CMediaEvent.GetTypeInfoCount-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent.GetTypeInfoCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c9402ad973a08afed4d338cfdc7b5df7fb14b9f0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099118"
---
# <a name="cmediaeventgettypeinfocount-method"></a><span data-ttu-id="88ee5-103">CMediaEvent.GetTypeInfoCount-Methode</span><span class="sxs-lookup"><span data-stu-id="88ee5-103">CMediaEvent.GetTypeInfoCount method</span></span>

<span data-ttu-id="88ee5-104">Ruft die Anzahl der Typinformationsschnittstellen ab, die von einem -Objekt bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="88ee5-104">Retrieves the number of type-information interfaces provided by an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="88ee5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="88ee5-105">Syntax</span></span>


```C++
HRESULT GetTypeInfoCount(
   UINT *pctinfo
);
```



## <a name="parameters"></a><span data-ttu-id="88ee5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="88ee5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88ee5-107">*pctinfo*</span><span class="sxs-lookup"><span data-stu-id="88ee5-107">*pctinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="88ee5-108">Zeiger auf die Anzahl der Typinformationsschnittstellen, die das -Objekt bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="88ee5-108">Pointer to number of type-information interfaces that the object provides.</span></span> <span data-ttu-id="88ee5-109">Wenn das Objekt Typinformationen bereitstellt, ist diese Zahl 1. Andernfalls ist die Zahl 0.</span><span class="sxs-lookup"><span data-stu-id="88ee5-109">If the object provides type information, this number is 1; otherwise, the number is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88ee5-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="88ee5-110">Return value</span></span>

<span data-ttu-id="88ee5-111">Gibt E \_ POINTER zurück, wenn *pctinfo* ungültig ist, andernfalls S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="88ee5-111">Returns E\_POINTER if *pctinfo* is invalid; otherwise, returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="88ee5-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="88ee5-112">Requirements</span></span>



| <span data-ttu-id="88ee5-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="88ee5-113">Requirement</span></span> | <span data-ttu-id="88ee5-114">Wert</span><span class="sxs-lookup"><span data-stu-id="88ee5-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88ee5-115">Header</span><span class="sxs-lookup"><span data-stu-id="88ee5-115">Header</span></span><br/>  | <dl> <span data-ttu-id="88ee5-116"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="88ee5-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="88ee5-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="88ee5-117">Library</span></span><br/> | <dl> <span data-ttu-id="88ee5-118"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="88ee5-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88ee5-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="88ee5-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88ee5-120">**CMediaEvent-Klasse**</span><span class="sxs-lookup"><span data-stu-id="88ee5-120">**CMediaEvent Class**</span></span>](cmediaevent.md)
</dt> </dl>

 

 




