---
description: Die Put \_ stopTime-Methode legt die Zeit fest, zu der die Wiedergabe in Relation zur Dauer des Streams beendet wird. Diese Methode implementiert die imediaposition::p UT \_ stopTime-Methode.
ms.assetid: 0a344cad-df93-47f1-8c7f-5d5ef775b850
title: CPosPassThru.put_StopTime-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_StopTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f5763700947596a0fb437ba3840df058d4d3239
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371550"
---
# <a name="cpospassthruput_stoptime-method"></a><span data-ttu-id="bdd5b-104">Cpospassthru. Put \_ stopTime-Methode</span><span class="sxs-lookup"><span data-stu-id="bdd5b-104">CPosPassThru.put\_StopTime method</span></span>

<span data-ttu-id="bdd5b-105">Die- `put_StopTime` Methode legt die Uhrzeit fest, zu der die Wiedergabe in Relation zur Dauer des Streams beendet wird.</span><span class="sxs-lookup"><span data-stu-id="bdd5b-105">The `put_StopTime` method sets the time at which the playback will stop, relative to the duration of the stream.</span></span> <span data-ttu-id="bdd5b-106">Diese Methode implementiert die [**imediaposition::p UT \_ stopTime**](/windows/desktop/api/Control/nf-control-imediaposition-put_stoptime) -Methode.</span><span class="sxs-lookup"><span data-stu-id="bdd5b-106">This method implements the [**IMediaPosition::put\_StopTime**](/windows/desktop/api/Control/nf-control-imediaposition-put_stoptime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdd5b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="bdd5b-107">Syntax</span></span>


```C++
HRESULT put_StopTime(
   REFTIME llTime
);
```



## <a name="parameters"></a><span data-ttu-id="bdd5b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bdd5b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdd5b-109">*lltime*</span><span class="sxs-lookup"><span data-stu-id="bdd5b-109">*llTime*</span></span> 
</dt> <dd>

<span data-ttu-id="bdd5b-110">Endzeit als **Double** -Wert in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="bdd5b-110">Stop time as a **double** value, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdd5b-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bdd5b-111">Return value</span></span>

<span data-ttu-id="bdd5b-112">Gibt den **HRESULT** -Wert aus der verbundenen PIN zurück.</span><span class="sxs-lookup"><span data-stu-id="bdd5b-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdd5b-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bdd5b-113">Requirements</span></span>



| <span data-ttu-id="bdd5b-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bdd5b-114">Requirement</span></span> | <span data-ttu-id="bdd5b-115">Wert</span><span class="sxs-lookup"><span data-stu-id="bdd5b-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdd5b-116">Header</span><span class="sxs-lookup"><span data-stu-id="bdd5b-116">Header</span></span><br/>  | <dl> <span data-ttu-id="bdd5b-117"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bdd5b-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bdd5b-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bdd5b-118">Library</span></span><br/> | <dl> <span data-ttu-id="bdd5b-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="bdd5b-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdd5b-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bdd5b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdd5b-121">**Cpospassthru-Klasse**</span><span class="sxs-lookup"><span data-stu-id="bdd5b-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




