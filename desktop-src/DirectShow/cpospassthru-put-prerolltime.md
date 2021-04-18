---
description: Mit der Put \_ prerolltime-Methode wird die Datenmenge festgelegt, die vor der Startposition in die Warteschlange eingereiht wird. Diese Methode implementiert die imediaposition::p UT- \_ prerolltime-Methode.
ms.assetid: 5c35fb1d-2296-493f-8104-601127d7dd9f
title: CPosPassThru.put_PrerollTime-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_PrerollTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 60bd4eddc7688373386147ea7999fdbd17f9af6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371622"
---
# <a name="cpospassthruput_prerolltime-method"></a><span data-ttu-id="1a4b7-104">Cpospassthru. Put \_ prerolltime-Methode</span><span class="sxs-lookup"><span data-stu-id="1a4b7-104">CPosPassThru.put\_PrerollTime method</span></span>

<span data-ttu-id="1a4b7-105">Die- `put_PrerollTime` Methode legt die Menge der Daten fest, die vor der Startposition in die Warteschlange eingereiht werden.</span><span class="sxs-lookup"><span data-stu-id="1a4b7-105">The `put_PrerollTime` method sets the amount of data that will be queued before the start position.</span></span> <span data-ttu-id="1a4b7-106">Diese Methode implementiert die [**imediaposition::p UT- \_ prerolltime**](/windows/desktop/api/Control/nf-control-imediaposition-put_prerolltime) -Methode.</span><span class="sxs-lookup"><span data-stu-id="1a4b7-106">This method implements the [**IMediaPosition::put\_PrerollTime**](/windows/desktop/api/Control/nf-control-imediaposition-put_prerolltime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a4b7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1a4b7-107">Syntax</span></span>


```C++
HRESULT put_PrerollTime(
   REFTIME llTime
);
```



## <a name="parameters"></a><span data-ttu-id="1a4b7-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a4b7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a4b7-109">*lltime*</span><span class="sxs-lookup"><span data-stu-id="1a4b7-109">*llTime*</span></span> 
</dt> <dd>

<span data-ttu-id="1a4b7-110">Vorab-Zeit in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="1a4b7-110">Preroll time, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a4b7-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1a4b7-111">Return value</span></span>

<span data-ttu-id="1a4b7-112">Gibt den **HRESULT** -Wert aus der verbundenen PIN zurück.</span><span class="sxs-lookup"><span data-stu-id="1a4b7-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a4b7-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1a4b7-113">Requirements</span></span>



| <span data-ttu-id="1a4b7-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1a4b7-114">Requirement</span></span> | <span data-ttu-id="1a4b7-115">Wert</span><span class="sxs-lookup"><span data-stu-id="1a4b7-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a4b7-116">Header</span><span class="sxs-lookup"><span data-stu-id="1a4b7-116">Header</span></span><br/>  | <dl> <span data-ttu-id="1a4b7-117"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1a4b7-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1a4b7-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1a4b7-118">Library</span></span><br/> | <dl> <span data-ttu-id="1a4b7-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="1a4b7-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a4b7-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1a4b7-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a4b7-121">**Cpospassthru-Klasse**</span><span class="sxs-lookup"><span data-stu-id="1a4b7-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




