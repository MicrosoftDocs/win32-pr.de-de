---
description: 'Die get \_ prerolltime-Methode ruft die Menge der Daten ab, die vor der Startposition in die Warteschlange eingereiht werden. Diese Methode implementiert die Methode imediaposition:: get \_ prerolltime.'
ms.assetid: 37c12798-eb0d-4859-8b2e-52d6ae147863
title: CPosPassThru.get_PrerollTime-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_PrerollTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 55cb2cc37a18c9ea00b4eb7115590f472b8d467e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370079"
---
# <a name="cpospassthruget_prerolltime-method"></a><span data-ttu-id="d6634-104">Cpospassthru. get \_ prerolltime-Methode</span><span class="sxs-lookup"><span data-stu-id="d6634-104">CPosPassThru.get\_PrerollTime method</span></span>

<span data-ttu-id="d6634-105">Die- `get_PrerollTime` Methode ruft die Menge der Daten ab, die vor der Startposition in die Warteschlange eingereiht werden.</span><span class="sxs-lookup"><span data-stu-id="d6634-105">The `get_PrerollTime` method retrieves the amount of data that will be queued before the start position.</span></span> <span data-ttu-id="d6634-106">Diese Methode implementiert die Methode [**imediaposition:: get \_ prerolltime**](/windows/desktop/api/Control/nf-control-imediaposition-get_prerolltime) .</span><span class="sxs-lookup"><span data-stu-id="d6634-106">This method implements the [**IMediaPosition::get\_PrerollTime**](/windows/desktop/api/Control/nf-control-imediaposition-get_prerolltime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6634-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d6634-107">Syntax</span></span>


```C++
HRESULT get_PrerollTime(
   REFTIME *pllTime
);
```



## <a name="parameters"></a><span data-ttu-id="d6634-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6634-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6634-109">*plltime*</span><span class="sxs-lookup"><span data-stu-id="d6634-109">*pllTime*</span></span> 
</dt> <dd>

<span data-ttu-id="d6634-110">Ein Zeiger auf eine Variable, die die vorab-Zeit (in Sekunden) empfängt.</span><span class="sxs-lookup"><span data-stu-id="d6634-110">Pointer to a variable that receives the preroll time, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6634-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d6634-111">Return value</span></span>

<span data-ttu-id="d6634-112">Gibt den **HRESULT** -Wert aus der verbundenen PIN zurück.</span><span class="sxs-lookup"><span data-stu-id="d6634-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6634-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d6634-113">Requirements</span></span>



| <span data-ttu-id="d6634-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d6634-114">Requirement</span></span> | <span data-ttu-id="d6634-115">Wert</span><span class="sxs-lookup"><span data-stu-id="d6634-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6634-116">Header</span><span class="sxs-lookup"><span data-stu-id="d6634-116">Header</span></span><br/>  | <dl> <span data-ttu-id="d6634-117"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d6634-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d6634-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d6634-118">Library</span></span><br/> | <dl> <span data-ttu-id="d6634-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="d6634-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6634-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6634-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6634-121">**Cpospassthru-Klasse**</span><span class="sxs-lookup"><span data-stu-id="d6634-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




