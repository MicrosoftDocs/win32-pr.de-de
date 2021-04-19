---
description: Die itparticipvorgänger Vent-Schnittstelle enthält Methoden, mit denen die Beschreibung der Teilnehmer Ereignisse abgerufen wird.
ms.assetid: 1199ec91-ee06-4e6c-8d8f-1585a3da3db0
title: Itparticipvorgänger Vent-Schnittstelle (confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ac6e2b43a528bc041a71962e84b4e1be62152a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355909"
---
# <a name="itparticipantevent-interface"></a><span data-ttu-id="5dbe8-103">Itparticipvorgänger Vent-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="5dbe8-103">ITParticipantEvent interface</span></span>

<span data-ttu-id="5dbe8-104">\[**Itparticipvorgänger Vent** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5dbe8-104">\[**ITParticipantEvent** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="5dbe8-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="5dbe8-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="5dbe8-106">Die **itparticipvorgänger Vent** -Schnittstelle enthält Methoden, mit denen die Beschreibung der Teilnehmer Ereignisse abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="5dbe8-106">The **ITParticipantEvent** interface contains methods that retrieve the description of participant events.</span></span> <span data-ttu-id="5dbe8-107">Wenn die Implementierung der [**ittapieventnotification:: Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) -Methode der Anwendung ein [**TAPI- \_ Ereignis**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event) angibt, das gleich " **te \_ private**" ist, ist der " *Peer* Event"-Parameter der Methode ein **IDispatch** -Zeiger für die **itparticipvorgänger Vent** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="5dbe8-107">When the application's implementation of the [**ITTAPIEventNotification::Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) method indicates a [**TAPI\_EVENT**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event) equal to **TE\_PRIVATE**, the method's *pEvent* parameter is an **IDispatch** pointer for the **ITParticipantEvent** interface.</span></span> <span data-ttu-id="5dbe8-108">Die Methoden dieser Schnittstelle können zum Abrufen von Informationen über eine geänderte Teilnehmer Änderung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5dbe8-108">The methods of this interface can be used to retrieve information concerning a participant change that has occurred.</span></span>

> [!Note]  
> <span data-ttu-id="5dbe8-109">Sie müssen die Ereignis [**\_ Filter-Methode ittapi::p UT**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) und eine Ereignis Filtermaske mit dem privaten Ereignis **te \_** festlegen, um den Empfang von Teilnehmer Ereignissen zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="5dbe8-109">You must call the [**ITTAPI::put\_EventFilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) method and set an event filter mask that includes the **TE\_PRIVATE** event to enable reception of participant events.</span></span> <span data-ttu-id="5dbe8-110">Wenn Sie **ittapi::p UT \_ EventFilter** nicht anrufen, empfängt Ihre Anwendung keine Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="5dbe8-110">If you do not call **ITTAPI::put\_EventFilter**, your application will not receive any events.</span></span> <span data-ttu-id="5dbe8-111">Weitere Informationen finden Sie in der Übersicht über [Ereignisse](events.md) .</span><span class="sxs-lookup"><span data-stu-id="5dbe8-111">For more information, see the [Events](events.md) overview.</span></span>

 

## <a name="members"></a><span data-ttu-id="5dbe8-112">Member</span><span class="sxs-lookup"><span data-stu-id="5dbe8-112">Members</span></span>

<span data-ttu-id="5dbe8-113">Die **itparticipvorgänger Vent** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="5dbe8-113">The **ITParticipantEvent** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="5dbe8-114">**Itparticipvorgänger Vent** verfügt auch über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="5dbe8-114">**ITParticipantEvent** also has these types of members:</span></span>

-   [<span data-ttu-id="5dbe8-115">Methoden</span><span class="sxs-lookup"><span data-stu-id="5dbe8-115">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5dbe8-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="5dbe8-116">Methods</span></span>

<span data-ttu-id="5dbe8-117">Die **itparticipvorgänger Vent** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="5dbe8-117">The **ITParticipantEvent** interface has these methods.</span></span>



| <span data-ttu-id="5dbe8-118">Methode</span><span class="sxs-lookup"><span data-stu-id="5dbe8-118">Method</span></span>                                                         | <span data-ttu-id="5dbe8-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5dbe8-119">Description</span></span>                                                                                                                                     |
|:---------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5dbe8-120">**get- \_ Ereignis**</span><span class="sxs-lookup"><span data-stu-id="5dbe8-120">**get\_Event**</span></span>](itparticipantevent-get-event.md)             | <span data-ttu-id="5dbe8-121">Ruft den [**Teilnehmer \_ Ereignis**](participant-event.md) Deskriptor des Ereignisses ab.</span><span class="sxs-lookup"><span data-stu-id="5dbe8-121">Gets the [**PARTICIPANT\_EVENT**](participant-event.md) descriptor of the event.</span></span><br/>                                                    |
| [<span data-ttu-id="5dbe8-122">**\_Teilnehmer erhalten**</span><span class="sxs-lookup"><span data-stu-id="5dbe8-122">**get\_Participant**</span></span>](itparticipantevent-get-participant.md) | <span data-ttu-id="5dbe8-123">Ruft einen Zeiger auf ein Array von [**itteilnehmer**](itparticipant.md) -Schnittstellen ab, die die am Ereignis beteiligten Teilnehmer darstellen.</span><span class="sxs-lookup"><span data-stu-id="5dbe8-123">Gets a pointer to an array of [**ITParticipant**](itparticipant.md) interfaces representing the participants involved in the event.</span></span><br/> |
| [<span data-ttu-id="5dbe8-124">**\_substream erhalten**</span><span class="sxs-lookup"><span data-stu-id="5dbe8-124">**get\_SubStream**</span></span>](itparticipantevent-get-substream.md)     | <span data-ttu-id="5dbe8-125">Ruft einen Zeiger auf ein Array von [**itsubstream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) -Schnittstellen ab, die die untergeordneten Datenströme darstellen.</span><span class="sxs-lookup"><span data-stu-id="5dbe8-125">Gets a pointer to an array of [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) interfaces representing the substreams involved in the event.</span></span><br/>       |



 

## <a name="requirements"></a><span data-ttu-id="5dbe8-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5dbe8-126">Requirements</span></span>



| <span data-ttu-id="5dbe8-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5dbe8-127">Requirement</span></span> | <span data-ttu-id="5dbe8-128">Wert</span><span class="sxs-lookup"><span data-stu-id="5dbe8-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5dbe8-129">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="5dbe8-129">TAPI version</span></span><br/> | <span data-ttu-id="5dbe8-130">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="5dbe8-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="5dbe8-131">Header</span><span class="sxs-lookup"><span data-stu-id="5dbe8-131">Header</span></span><br/>       | <dl> <span data-ttu-id="5dbe8-132"><dt>"Confpriv. h"</dt></span><span class="sxs-lookup"><span data-stu-id="5dbe8-132"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="5dbe8-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5dbe8-133">Library</span></span><br/>      | <dl> <span data-ttu-id="5dbe8-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5dbe8-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="5dbe8-135">DLL</span><span class="sxs-lookup"><span data-stu-id="5dbe8-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="5dbe8-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5dbe8-136"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="5dbe8-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5dbe8-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5dbe8-138">**Itteilnehmer**</span><span class="sxs-lookup"><span data-stu-id="5dbe8-138">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="5dbe8-139">**Itsubstream**</span><span class="sxs-lookup"><span data-stu-id="5dbe8-139">**ITSubStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> <dt>

[<span data-ttu-id="5dbe8-140">**Itcallinfo**</span><span class="sxs-lookup"><span data-stu-id="5dbe8-140">**ITCallInfo**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)
</dt> <dt>

[<span data-ttu-id="5dbe8-141">**Teilnehmer \_ Ereignis**</span><span class="sxs-lookup"><span data-stu-id="5dbe8-141">**PARTICIPANT\_EVENT**</span></span>](participant-event.md)
</dt> <dt>

[<span data-ttu-id="5dbe8-142">**Ittapieventnotification:: Event**</span><span class="sxs-lookup"><span data-stu-id="5dbe8-142">**ITTAPIEventNotification::Event**</span></span>](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event)
</dt> <dt>

[<span data-ttu-id="5dbe8-143">**TAPI- \_ Ereignis**</span><span class="sxs-lookup"><span data-stu-id="5dbe8-143">**TAPI\_EVENT**</span></span>](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event)
</dt> <dt>

[<span data-ttu-id="5dbe8-144">Code Ausschnitt für das Registrieren von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="5dbe8-144">Register Events code snippet</span></span>](register-events.md)
</dt> </dl>

 

