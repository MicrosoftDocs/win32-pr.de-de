---
description: 'Die get \_ Duration-Methode ruft die Dauer des Streams ab. Diese Methode implementiert die imediaposition:: get \_ Duration-Methode.'
ms.assetid: 326a8cd3-d05f-49d0-941d-08f9778e9a06
title: CPosPassThru.get_Duration-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_Duration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: df518a0691a4fe1a6c0443ba93a83e65577efe21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371315"
---
# <a name="cpospassthruget_duration-method"></a><span data-ttu-id="092b2-104">Cpospassthru. get \_ Duration-Methode</span><span class="sxs-lookup"><span data-stu-id="092b2-104">CPosPassThru.get\_Duration method</span></span>

<span data-ttu-id="092b2-105">Die- `get_Duration` Methode ruft die Dauer des Streams ab.</span><span class="sxs-lookup"><span data-stu-id="092b2-105">The `get_Duration` method retrieves the duration of the stream.</span></span> <span data-ttu-id="092b2-106">Diese Methode implementiert die [**imediaposition:: get \_ Duration**](/windows/desktop/api/Control/nf-control-imediaposition-get_duration) -Methode.</span><span class="sxs-lookup"><span data-stu-id="092b2-106">This method implements the [**IMediaPosition::get\_Duration**](/windows/desktop/api/Control/nf-control-imediaposition-get_duration) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="092b2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="092b2-107">Syntax</span></span>


```C++
HRESULT get_Duration(
   REFTIME *plength
);
```



## <a name="parameters"></a><span data-ttu-id="092b2-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="092b2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="092b2-109">*pLength*</span><span class="sxs-lookup"><span data-stu-id="092b2-109">*plength*</span></span> 
</dt> <dd>

<span data-ttu-id="092b2-110">Ein Zeiger auf eine Variable, die die Gesamtlänge des Streams in Sekunden empfängt.</span><span class="sxs-lookup"><span data-stu-id="092b2-110">Pointer to a variable that receives the total stream length, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="092b2-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="092b2-111">Return value</span></span>

<span data-ttu-id="092b2-112">Gibt den **HRESULT** -Wert aus der verbundenen PIN zurück.</span><span class="sxs-lookup"><span data-stu-id="092b2-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="092b2-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="092b2-113">Requirements</span></span>



| <span data-ttu-id="092b2-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="092b2-114">Requirement</span></span> | <span data-ttu-id="092b2-115">Wert</span><span class="sxs-lookup"><span data-stu-id="092b2-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="092b2-116">Header</span><span class="sxs-lookup"><span data-stu-id="092b2-116">Header</span></span><br/>  | <dl> <span data-ttu-id="092b2-117"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="092b2-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="092b2-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="092b2-118">Library</span></span><br/> | <dl> <span data-ttu-id="092b2-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="092b2-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="092b2-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="092b2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="092b2-121">**Cpospassthru-Klasse**</span><span class="sxs-lookup"><span data-stu-id="092b2-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




