---
title: IReferenceClock-advientime-Methode
description: Die AdviseTime-Methode fordert eine asynchrone Benachrichtigung an, dass eine Zeit verstrichen ist.
ms.assetid: 8f3f8713-b53c-4110-ac7a-724bbc49368e
keywords:
- Advi-Time-Methode Windows Media-Format
- Advi-Time-Methode Windows Media-Format, IReferenceClock-Schnittstelle
- IReferenceClock-Schnittstelle Windows Media-Format, advientime-Methode
topic_type:
- apiref
api_name:
- IReferenceClock.AdviseTime
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3fa91338b4bff8f925f00e7159a36089e0de0aa8
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106339246"
---
# <a name="ireferenceclockadvisetime-method"></a><span data-ttu-id="59823-106">IReferenceClock:: advientime-Methode</span><span class="sxs-lookup"><span data-stu-id="59823-106">IReferenceClock::AdviseTime method</span></span>

<span data-ttu-id="59823-107">Die **AdviseTime** -Methode fordert eine asynchrone Benachrichtigung an, dass eine Zeit verstrichen ist.</span><span class="sxs-lookup"><span data-stu-id="59823-107">The **AdviseTime** method requests an asynchronous notification that a time has elapsed.</span></span>

## <a name="syntax"></a><span data-ttu-id="59823-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="59823-108">Syntax</span></span>


```C++
HRESULT AdviseTime(
  [in]  REFERENCE_TIME rtBaseTime,
  [in]  REFERENCE_TIME rtStreamTime,
  [in]  HEVENT         hEvent,
  [out] DWORD          *pdwAdviseCookie
);
```



## <a name="parameters"></a><span data-ttu-id="59823-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="59823-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59823-110">*rtbasetime* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="59823-110">*rtBaseTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59823-111">Basis Verweis Zeit in 100-Nanosecond-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="59823-111">Base reference time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="59823-112">*rtstreamtime* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="59823-112">*rtStreamTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59823-113">Streamoffset Zeit in 100-Nanosecond-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="59823-113">Stream offset time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="59823-114">*hevent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="59823-114">*hEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59823-115">Handle für ein Ereignis, das vom Aufrufer erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="59823-115">Handle to an event, created by the caller.</span></span> <span data-ttu-id="59823-116">Dieses Ereignis wird signalisiert, wenn die angegebene Zeit abgelaufen ist.</span><span class="sxs-lookup"><span data-stu-id="59823-116">This event will be signaled when the time specified elapses.</span></span>

</dd> <dt>

<span data-ttu-id="59823-117">*pdwadviabcookie* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="59823-117">*pdwAdviseCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="59823-118">Ein Zeiger auf eine Variable, die einen Bezeichner für die Anforderung empfängt.</span><span class="sxs-lookup"><span data-stu-id="59823-118">Pointer to a variable that receives an identifier for the request.</span></span> <span data-ttu-id="59823-119">Diese wird verwendet, um den Aufruf von **adviin** der Zukunft zu identifizieren, um beispielsweise die Anforderung abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="59823-119">This is used to identify this call to **AdviseTime** in the future for example, to cancel the request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59823-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="59823-120">Return value</span></span>

<span data-ttu-id="59823-121">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="59823-121">The method returns an **HRESULT**.</span></span> <span data-ttu-id="59823-122">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="59823-122">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="59823-123">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="59823-123">Return code</span></span>                                                                               | <span data-ttu-id="59823-124">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="59823-124">Description</span></span>                                             |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <dl> <span data-ttu-id="59823-125"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="59823-125"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="59823-126">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="59823-126">The method succeeded.</span></span><br/>                        |
| <dl> <span data-ttu-id="59823-127"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="59823-127"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="59823-128">Der *pdwadvietcookie* -Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="59823-128">The *pdwAdviseCookie* parameter is **NULL**.</span></span><br/> |
| <dl> <span data-ttu-id="59823-129"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="59823-129"><dt>**E\_FAIL**</dt></span></span> </dl>    | <span data-ttu-id="59823-130">Nicht spezifizierter Fehler.</span><span class="sxs-lookup"><span data-stu-id="59823-130">Unspecified failure.</span></span><br/>                         |



 

## <a name="see-also"></a><span data-ttu-id="59823-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="59823-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59823-132">**IReferenceClock-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="59823-132">**IReferenceClock Interface**</span></span>](ireferenceclock.md)
</dt> </dl>

 

 





