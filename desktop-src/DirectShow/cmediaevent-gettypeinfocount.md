---
description: Ruft die Anzahl der von einem-Objekt bereitgestellten Typ-Informations Schnittstellen ab.
ms.assetid: e16bc324-bb49-4df2-afeb-2c2cd1620693
title: Cmediaevent. gettypeingefocount-Methode (ctlutil. h)
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
ms.openlocfilehash: 4de7a79251f2d25c1c55642050ad06513a1bfe6f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369624"
---
# <a name="cmediaeventgettypeinfocount-method"></a><span data-ttu-id="ddf56-103">Cmediaevent. gettypeingefocount-Methode</span><span class="sxs-lookup"><span data-stu-id="ddf56-103">CMediaEvent.GetTypeInfoCount method</span></span>

<span data-ttu-id="ddf56-104">Ruft die Anzahl der von einem-Objekt bereitgestellten Typ-Informations Schnittstellen ab.</span><span class="sxs-lookup"><span data-stu-id="ddf56-104">Retrieves the number of type-information interfaces provided by an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddf56-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ddf56-105">Syntax</span></span>


```C++
HRESULT GetTypeInfoCount(
   UINT *pctinfo
);
```



## <a name="parameters"></a><span data-ttu-id="ddf56-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ddf56-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ddf56-107">*pctinfo*</span><span class="sxs-lookup"><span data-stu-id="ddf56-107">*pctinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="ddf56-108">Zeiger auf die Anzahl von Typ-Informations Schnittstellen, die das Objekt bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="ddf56-108">Pointer to number of type-information interfaces that the object provides.</span></span> <span data-ttu-id="ddf56-109">Wenn das Objekt Typinformationen bereitstellt, ist diese Zahl 1. Andernfalls ist die Zahl 0 (null).</span><span class="sxs-lookup"><span data-stu-id="ddf56-109">If the object provides type information, this number is 1; otherwise, the number is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ddf56-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ddf56-110">Return value</span></span>

<span data-ttu-id="ddf56-111">Gibt einen E- \_ Zeiger zurück, wenn *pctinfo* ungültig ist; andernfalls gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="ddf56-111">Returns E\_POINTER if *pctinfo* is invalid; otherwise, returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="ddf56-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ddf56-112">Requirements</span></span>



| <span data-ttu-id="ddf56-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ddf56-113">Requirement</span></span> | <span data-ttu-id="ddf56-114">Wert</span><span class="sxs-lookup"><span data-stu-id="ddf56-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ddf56-115">Header</span><span class="sxs-lookup"><span data-stu-id="ddf56-115">Header</span></span><br/>  | <dl> <span data-ttu-id="ddf56-116"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ddf56-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ddf56-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ddf56-117">Library</span></span><br/> | <dl> <span data-ttu-id="ddf56-118">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="ddf56-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ddf56-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ddf56-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddf56-120">**Cmediaevent-Klasse**</span><span class="sxs-lookup"><span data-stu-id="ddf56-120">**CMediaEvent Class**</span></span>](cmediaevent.md)
</dt> </dl>

 

 




