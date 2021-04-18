---
description: Die get- \_ Teilnehmer Methode erhält einen Zeiger auf ein Array von itparticipants-Schnittstellen, die die am Ereignis beteiligten Teilnehmer darstellen.
ms.assetid: 3c650715-b1c3-4f84-976a-2cb0f7f19f52
title: 'Itparticipvorgänger Vent:: get_Participant-Methode (confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc5e9ee84bac69bd77237f1a50b9a008b2830258
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368573"
---
# <a name="itparticipanteventget_participant-method"></a><span data-ttu-id="4cf2d-103">Itparticipvorgänger Vent:: get- \_ Teilnehmer Methode</span><span class="sxs-lookup"><span data-stu-id="4cf2d-103">ITParticipantEvent::get\_Participant method</span></span>

<span data-ttu-id="4cf2d-104">\[**get \_ Der Teilnehmer** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4cf2d-104">\[**get\_Participant** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4cf2d-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="4cf2d-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="4cf2d-106">Die **get- \_ Teilnehmer** Methode erhält einen Zeiger auf ein Array von [**itparticipants**](itparticipant.md) -Schnittstellen, die die am Ereignis beteiligten Teilnehmer darstellen.</span><span class="sxs-lookup"><span data-stu-id="4cf2d-106">The **get\_Participant** method gets a pointer to an array of [**ITParticipant**](itparticipant.md) interfaces representing the participants involved in the event.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cf2d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4cf2d-107">Syntax</span></span>


```C++
HRESULT get_Participant(
  [out] ITParticipant **ppParticipant
);
```



## <a name="parameters"></a><span data-ttu-id="4cf2d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4cf2d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cf2d-109">*ppteilnehmer* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="4cf2d-109">*ppParticipant* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4cf2d-110">Zeiger auf ein Array von [**itteilnehmer**](itparticipant.md) -Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="4cf2d-110">Pointer to array of [**ITParticipant**](itparticipant.md) interfaces.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cf2d-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4cf2d-111">Return value</span></span>

<span data-ttu-id="4cf2d-112">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="4cf2d-112">This method can return one of these values.</span></span>



| <span data-ttu-id="4cf2d-113">Wert</span><span class="sxs-lookup"><span data-stu-id="4cf2d-113">Value</span></span>                                                                                           | <span data-ttu-id="4cf2d-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="4cf2d-114">Meaning</span></span>                                                          |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="4cf2d-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4cf2d-115"><dt>**S\_OK**</dt></span></span> </dl>            | <span data-ttu-id="4cf2d-116">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="4cf2d-116">Method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="4cf2d-117"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="4cf2d-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>   | <span data-ttu-id="4cf2d-118">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="4cf2d-118">Insufficient memory exists to perform the operation.</span></span><br/>  |
| <dl> <span data-ttu-id="4cf2d-119"><dt>**TAPI \_ E \_ noItems**</dt></span><span class="sxs-lookup"><span data-stu-id="4cf2d-119"><dt>**TAPI\_E\_NOITEMS**</dt></span></span> </dl> | <span data-ttu-id="4cf2d-120">Dem Ereignis sind keine Teilnehmer zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="4cf2d-120">There are no participants associated with the event.</span></span><br/>  |
| <dl> <span data-ttu-id="4cf2d-121"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="4cf2d-121"><dt>**E\_POINTER**</dt></span></span> </dl>       | <span data-ttu-id="4cf2d-122">Der *ppparticipants* -Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="4cf2d-122">The *ppParticipant* parameter is not a valid pointer.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4cf2d-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4cf2d-123">Requirements</span></span>



| <span data-ttu-id="4cf2d-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4cf2d-124">Requirement</span></span> | <span data-ttu-id="4cf2d-125">Wert</span><span class="sxs-lookup"><span data-stu-id="4cf2d-125">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4cf2d-126">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="4cf2d-126">TAPI version</span></span><br/> | <span data-ttu-id="4cf2d-127">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="4cf2d-127">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="4cf2d-128">Header</span><span class="sxs-lookup"><span data-stu-id="4cf2d-128">Header</span></span><br/>       | <dl> <span data-ttu-id="4cf2d-129"><dt>"Confpriv. h"</dt></span><span class="sxs-lookup"><span data-stu-id="4cf2d-129"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="4cf2d-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4cf2d-130">Library</span></span><br/>      | <dl> <span data-ttu-id="4cf2d-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4cf2d-131"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="4cf2d-132">DLL</span><span class="sxs-lookup"><span data-stu-id="4cf2d-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="4cf2d-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4cf2d-133"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="4cf2d-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4cf2d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cf2d-135">**Itparticipvorgänger Vent**</span><span class="sxs-lookup"><span data-stu-id="4cf2d-135">**ITParticipantEvent**</span></span>](itparticipantevent.md)
</dt> <dt>

[<span data-ttu-id="4cf2d-136">**Itteilnehmer**</span><span class="sxs-lookup"><span data-stu-id="4cf2d-136">**ITParticipant**</span></span>](itparticipant.md)
</dt> </dl>

 

 




