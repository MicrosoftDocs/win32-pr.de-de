---
description: Die get \_ Event-Methode ruft einen Teilnehmer \_ Ereignis Deskriptor für den Ereignistyp ab, der aufgetreten ist.
ms.assetid: 6b5e6358-2ba6-48b5-8d55-bc896fbb9962
title: 'Itparticipvorgänger Vent:: get_Event-Methode (confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b6cbfcf709b1f9f3f49047504bf5d9e8c02b159
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371288"
---
# <a name="itparticipanteventget_event-method"></a><span data-ttu-id="fe6cb-103">Itparticipvorgänger Vent:: get- \_ Ereignismethode</span><span class="sxs-lookup"><span data-stu-id="fe6cb-103">ITParticipantEvent::get\_Event method</span></span>

<span data-ttu-id="fe6cb-104">\[**get \_ Das Ereignis** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fe6cb-104">\[**get\_Event** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="fe6cb-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="fe6cb-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="fe6cb-106">Die **get \_ Event** -Methode ruft einen [**Teilnehmer \_ Ereignis**](participant-event.md) Deskriptor für den Ereignistyp ab, der aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="fe6cb-106">The **get\_Event** method gets a [**PARTICIPANT\_EVENT**](participant-event.md) descriptor of the type of event that has occurred.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe6cb-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe6cb-107">Syntax</span></span>


```C++
HRESULT get_Event(
  [out] PARTICIPANT_EVENT *pParticipantEvent
);
```



## <a name="parameters"></a><span data-ttu-id="fe6cb-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="fe6cb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe6cb-109">*pparticipvorgänger Vent* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="fe6cb-109">*pParticipantEvent* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe6cb-110">Zeiger auf einen [**Teilnehmer \_ Ereignis**](participant-event.md) Deskriptor des Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="fe6cb-110">Pointer to a [**PARTICIPANT\_EVENT**](participant-event.md) descriptor of the event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe6cb-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fe6cb-111">Return value</span></span>

<span data-ttu-id="fe6cb-112">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="fe6cb-112">This method can return one of these values.</span></span>



| <span data-ttu-id="fe6cb-113">Wert</span><span class="sxs-lookup"><span data-stu-id="fe6cb-113">Value</span></span>                                                                                         | <span data-ttu-id="fe6cb-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="fe6cb-114">Meaning</span></span>                                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="fe6cb-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fe6cb-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="fe6cb-116">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="fe6cb-116">Method succeeded.</span></span><br/>                                         |
| <dl> <span data-ttu-id="fe6cb-117"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="fe6cb-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="fe6cb-118">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="fe6cb-118">Insufficient memory exists to perform the operation.</span></span><br/>      |
| <dl> <span data-ttu-id="fe6cb-119"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="fe6cb-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="fe6cb-120">Der *pparticipvorgänger Vent* -Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="fe6cb-120">The *pParticipantEvent* parameter is not a valid pointer.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="fe6cb-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fe6cb-121">Requirements</span></span>



| <span data-ttu-id="fe6cb-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fe6cb-122">Requirement</span></span> | <span data-ttu-id="fe6cb-123">Wert</span><span class="sxs-lookup"><span data-stu-id="fe6cb-123">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fe6cb-124">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="fe6cb-124">TAPI version</span></span><br/> | <span data-ttu-id="fe6cb-125">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="fe6cb-125">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="fe6cb-126">Header</span><span class="sxs-lookup"><span data-stu-id="fe6cb-126">Header</span></span><br/>       | <dl> <span data-ttu-id="fe6cb-127"><dt>"Confpriv. h"</dt></span><span class="sxs-lookup"><span data-stu-id="fe6cb-127"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="fe6cb-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fe6cb-128">Library</span></span><br/>      | <dl> <span data-ttu-id="fe6cb-129"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fe6cb-129"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="fe6cb-130">DLL</span><span class="sxs-lookup"><span data-stu-id="fe6cb-130">DLL</span></span><br/>          | <dl> <span data-ttu-id="fe6cb-131"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe6cb-131"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="fe6cb-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fe6cb-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe6cb-133">**Itparticipvorgänger Vent**</span><span class="sxs-lookup"><span data-stu-id="fe6cb-133">**ITParticipantEvent**</span></span>](itparticipantevent.md)
</dt> <dt>

[<span data-ttu-id="fe6cb-134">**Teilnehmer \_ Ereignis**</span><span class="sxs-lookup"><span data-stu-id="fe6cb-134">**PARTICIPANT\_EVENT**</span></span>](participant-event.md)
</dt> </dl>

 

 




