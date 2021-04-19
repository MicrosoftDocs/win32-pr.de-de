---
description: 'Die get- \_ Raten Methode ruft die Wiedergabe Rate ab. Diese Methode implementiert die imediaposition:: get- \_ Raten Methode.'
ms.assetid: 216cbcef-4874-4565-abb0-8c8bf67fe23c
title: CPosPassThru.get_Rate-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_Rate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 46e565f51d7c549f524f9e478b2a8326daf690a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360429"
---
# <a name="cpospassthruget_rate-method"></a><span data-ttu-id="127a7-104">Cpospassthru. get- \_ Raten Methode</span><span class="sxs-lookup"><span data-stu-id="127a7-104">CPosPassThru.get\_Rate method</span></span>

<span data-ttu-id="127a7-105">Die- `get_Rate` Methode ruft die Wiedergabe Rate ab.</span><span class="sxs-lookup"><span data-stu-id="127a7-105">The `get_Rate` method retrieves the playback rate.</span></span> <span data-ttu-id="127a7-106">Diese Methode implementiert die [**imediaposition:: get- \_ Raten**](/windows/desktop/api/Control/nf-control-imediaposition-get_rate) Methode.</span><span class="sxs-lookup"><span data-stu-id="127a7-106">This method implements the [**IMediaPosition::get\_Rate**](/windows/desktop/api/Control/nf-control-imediaposition-get_rate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="127a7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="127a7-107">Syntax</span></span>


```C++
HRESULT get_Rate(
   double *pdRate
);
```



## <a name="parameters"></a><span data-ttu-id="127a7-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="127a7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="127a7-109">*pdrate*</span><span class="sxs-lookup"><span data-stu-id="127a7-109">*pdRate*</span></span> 
</dt> <dd>

<span data-ttu-id="127a7-110">Ein Zeiger auf eine Variable, die die Wiedergabe Rate empfängt.</span><span class="sxs-lookup"><span data-stu-id="127a7-110">Pointer to a variable that receives the playback rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="127a7-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="127a7-111">Return value</span></span>

<span data-ttu-id="127a7-112">Gibt den **HRESULT** -Wert aus der verbundenen PIN zurück.</span><span class="sxs-lookup"><span data-stu-id="127a7-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="127a7-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="127a7-113">Requirements</span></span>



| <span data-ttu-id="127a7-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="127a7-114">Requirement</span></span> | <span data-ttu-id="127a7-115">Wert</span><span class="sxs-lookup"><span data-stu-id="127a7-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="127a7-116">Header</span><span class="sxs-lookup"><span data-stu-id="127a7-116">Header</span></span><br/>  | <dl> <span data-ttu-id="127a7-117"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="127a7-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="127a7-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="127a7-118">Library</span></span><br/> | <dl> <span data-ttu-id="127a7-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="127a7-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="127a7-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="127a7-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="127a7-121">**Cpospassthru-Klasse**</span><span class="sxs-lookup"><span data-stu-id="127a7-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




