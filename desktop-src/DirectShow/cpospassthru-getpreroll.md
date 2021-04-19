---
description: 'Die getpreroll-Methode ruft die Menge der Daten ab, die vor der Startposition in die Warteschlange eingereiht werden. Diese Methode implementiert die imediaseeking:: getpreroll-Methode.'
ms.assetid: b00de2fa-ba3c-4a16-ad67-adf3df52ef9a
title: Cpospassthru. getpreroll-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetPreroll
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e72d7c83c8cdb0fa08a4b395fd65c80edbe3fb05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369134"
---
# <a name="cpospassthrugetpreroll-method"></a><span data-ttu-id="b30ab-104">Cpospassthru. getpreroll-Methode</span><span class="sxs-lookup"><span data-stu-id="b30ab-104">CPosPassThru.GetPreroll method</span></span>

<span data-ttu-id="b30ab-105">Die- `GetPreroll` Methode ruft die Menge der Daten ab, die vor der Startposition in die Warteschlange eingereiht werden.</span><span class="sxs-lookup"><span data-stu-id="b30ab-105">The `GetPreroll` method retrieves the amount of data that will be queued before the start position.</span></span> <span data-ttu-id="b30ab-106">Diese Methode implementiert die [**imediaseeking:: getpreroll**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpreroll) -Methode.</span><span class="sxs-lookup"><span data-stu-id="b30ab-106">This method implements the [**IMediaSeeking::GetPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpreroll) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b30ab-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b30ab-107">Syntax</span></span>


```C++
HRESULT GetPreroll(
   LONGLONG *pllPreroll
);
```



## <a name="parameters"></a><span data-ttu-id="b30ab-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b30ab-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b30ab-109">*pllpreroll*</span><span class="sxs-lookup"><span data-stu-id="b30ab-109">*pllPreroll*</span></span> 
</dt> <dd>

<span data-ttu-id="b30ab-110">Ein Zeiger auf eine Variable, die die vorab Zeit in Einheiten des aktuellen Zeit Formats empfängt.</span><span class="sxs-lookup"><span data-stu-id="b30ab-110">Pointer to a variable that receives the preroll time, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b30ab-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b30ab-111">Return value</span></span>

<span data-ttu-id="b30ab-112">Gibt den **HRESULT** -Wert aus der verbundenen PIN zurück.</span><span class="sxs-lookup"><span data-stu-id="b30ab-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="b30ab-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b30ab-113">Requirements</span></span>



| <span data-ttu-id="b30ab-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b30ab-114">Requirement</span></span> | <span data-ttu-id="b30ab-115">Wert</span><span class="sxs-lookup"><span data-stu-id="b30ab-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b30ab-116">Header</span><span class="sxs-lookup"><span data-stu-id="b30ab-116">Header</span></span><br/>  | <dl> <span data-ttu-id="b30ab-117"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b30ab-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b30ab-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b30ab-118">Library</span></span><br/> | <dl> <span data-ttu-id="b30ab-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="b30ab-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b30ab-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b30ab-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b30ab-121">**Cpospassthru-Klasse**</span><span class="sxs-lookup"><span data-stu-id="b30ab-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




