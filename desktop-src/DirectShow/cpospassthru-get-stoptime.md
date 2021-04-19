---
description: 'Die get \_ stopTime-Methode ruft die Zeit ab, zu der die Wiedergabe in Relation zur Dauer des Streams beendet wird. Diese Methode implementiert die imediaposition:: get \_ stopTime-Methode.'
ms.assetid: 0ca3f047-ac43-419e-a1ed-b406f89f7af7
title: CPosPassThru.get_StopTime-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_StopTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 227b054a9737c06e56f7311acc7e0093766608b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370063"
---
# <a name="cpospassthruget_stoptime-method"></a><span data-ttu-id="a63ab-104">Cpospassthru. get \_ stopTime-Methode</span><span class="sxs-lookup"><span data-stu-id="a63ab-104">CPosPassThru.get\_StopTime method</span></span>

<span data-ttu-id="a63ab-105">Die- `get_StopTime` Methode ruft den Zeitpunkt ab, zu dem die Wiedergabe in Relation zur Dauer des Streams beendet wird.</span><span class="sxs-lookup"><span data-stu-id="a63ab-105">The `get_StopTime` method retrieves the time at which the playback will stop, relative to the duration of the stream.</span></span> <span data-ttu-id="a63ab-106">Diese Methode implementiert die [**imediaposition:: get \_ stopTime**](/windows/desktop/api/Control/nf-control-imediaposition-get_stoptime) -Methode.</span><span class="sxs-lookup"><span data-stu-id="a63ab-106">This method implements the [**IMediaPosition::get\_StopTime**](/windows/desktop/api/Control/nf-control-imediaposition-get_stoptime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a63ab-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a63ab-107">Syntax</span></span>


```C++
HRESULT get_StopTime(
   REFTIME *pllTime
);
```



## <a name="parameters"></a><span data-ttu-id="a63ab-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a63ab-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a63ab-109">*plltime*</span><span class="sxs-lookup"><span data-stu-id="a63ab-109">*pllTime*</span></span> 
</dt> <dd>

<span data-ttu-id="a63ab-110">Ein Zeiger auf eine Variable, die die Endzeit (in Sekunden) empfängt.</span><span class="sxs-lookup"><span data-stu-id="a63ab-110">Pointer to a variable that receives the stop time, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a63ab-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a63ab-111">Return value</span></span>

<span data-ttu-id="a63ab-112">Gibt den **HRESULT** -Wert aus der verbundenen PIN zurück.</span><span class="sxs-lookup"><span data-stu-id="a63ab-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="a63ab-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a63ab-113">Requirements</span></span>



| <span data-ttu-id="a63ab-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a63ab-114">Requirement</span></span> | <span data-ttu-id="a63ab-115">Wert</span><span class="sxs-lookup"><span data-stu-id="a63ab-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a63ab-116">Header</span><span class="sxs-lookup"><span data-stu-id="a63ab-116">Header</span></span><br/>  | <dl> <span data-ttu-id="a63ab-117"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a63ab-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a63ab-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a63ab-118">Library</span></span><br/> | <dl> <span data-ttu-id="a63ab-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="a63ab-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a63ab-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a63ab-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a63ab-121">**Cpospassthru-Klasse**</span><span class="sxs-lookup"><span data-stu-id="a63ab-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




