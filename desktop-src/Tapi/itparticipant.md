---
description: Die itteilnehmer-Schnittstelle wird von ipconf MSP implementiert. Sie ermöglicht einer Anwendung das Abrufen von Informationen zu Konferenzteilnehmern und das Abrufen von Zeigern auf die Streams, die diesen Teilnehmern zugeordnet sind.
ms.assetid: 8c3edfc1-3165-48b7-9d83-8892c192498b
title: Itteilnehmer-Schnittstelle (ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8b7aa9d845d8d2489be0850bcc3fcf3f93ccdac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371676"
---
# <a name="itparticipant-interface"></a><span data-ttu-id="919a5-104">Itteilnehmer-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="919a5-104">ITParticipant interface</span></span>

<span data-ttu-id="919a5-105">\[Der **itteilnehmer** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="919a5-105">\[**ITParticipant** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="919a5-106">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="919a5-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="919a5-107">Die **itteilnehmer** -Schnittstelle wird von [ipconf MSP](ipconf-msp.md)implementiert.</span><span class="sxs-lookup"><span data-stu-id="919a5-107">The **ITParticipant** interface is implemented by the [IPConf MSP](ipconf-msp.md).</span></span> <span data-ttu-id="919a5-108">Sie ermöglicht einer Anwendung das Abrufen von Informationen zu Konferenzteilnehmern und das Abrufen von Zeigern auf die Streams, die diesen Teilnehmern zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="919a5-108">It allows an application to retrieve information on conference participants, and get pointers to the streams associated with those participants.</span></span>

<span data-ttu-id="919a5-109">Diese Schnittstelle wird für das-Objekt aufgerufen, wenn ein-Rückruf die IP-Konferenzen verwendet.</span><span class="sxs-lookup"><span data-stu-id="919a5-109">This interface is exposed on the call object when a call uses the IP Conferencing.</span></span> <span data-ttu-id="919a5-110">Ein Zeiger kann durch Aufrufen von **QueryInterface** mithilfe eines [**itcallinfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) -Zeigers abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="919a5-110">A pointer can be obtained by calling **QueryInterface** using an [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) pointer.</span></span>

## <a name="members"></a><span data-ttu-id="919a5-111">Member</span><span class="sxs-lookup"><span data-stu-id="919a5-111">Members</span></span>

<span data-ttu-id="919a5-112">Die **itteilnehmer** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="919a5-112">The **ITParticipant** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="919a5-113">Der **itparticipants** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="919a5-113">**ITParticipant** also has these types of members:</span></span>

-   [<span data-ttu-id="919a5-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="919a5-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="919a5-115">Methoden</span><span class="sxs-lookup"><span data-stu-id="919a5-115">Methods</span></span>

<span data-ttu-id="919a5-116">Die **itparticipants** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="919a5-116">The **ITParticipant** interface has these methods.</span></span>



| <span data-ttu-id="919a5-117">Methode</span><span class="sxs-lookup"><span data-stu-id="919a5-117">Method</span></span>                                                                      | <span data-ttu-id="919a5-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="919a5-118">Description</span></span>                                                                                                                                                             |
|:----------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="919a5-119">**Enumeratestreams**</span><span class="sxs-lookup"><span data-stu-id="919a5-119">**EnumerateStreams**</span></span>](itparticipant-enumeratestreams.md)                  | <span data-ttu-id="919a5-120">Listet Streams auf, die dem aktuellen Teilnehmer zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="919a5-120">Enumerates streams associated with the current participant.</span></span><br/>                                                                                                  |
| [<span data-ttu-id="919a5-121">**\_mediatypes erhalten**</span><span class="sxs-lookup"><span data-stu-id="919a5-121">**get\_MediaTypes**</span></span>](itparticipant-get-mediatypes.md)                     | <span data-ttu-id="919a5-122">Ruft die einem Teilnehmer zugeordneten [**Medientypen**](tapimediatype--constants.md) ab.</span><span class="sxs-lookup"><span data-stu-id="919a5-122">Gets the [**media types**](tapimediatype--constants.md) associated with a participant.</span></span><br/>                                                                      |
| [<span data-ttu-id="919a5-123">**Informationen zu " \_ participanttypeer" erhalten**</span><span class="sxs-lookup"><span data-stu-id="919a5-123">**get\_ParticipantTypedInfo**</span></span>](itparticipant-get-participanttypedinfo.md) | <span data-ttu-id="919a5-124">Ruft eine BSTR-Darstellung des benötigten Informations Typs, z. b. PTI \_ EmailAddress, ab.</span><span class="sxs-lookup"><span data-stu-id="919a5-124">Gets a BSTR representation of the needed type of information, such as PTI\_EMAILADDRESS.</span></span><br/>                                                                     |
| [<span data-ttu-id="919a5-125">**\_Status erhalten**</span><span class="sxs-lookup"><span data-stu-id="919a5-125">**get\_Status**</span></span>](itparticipant-get-status.md)                             | <span data-ttu-id="919a5-126">Ruft den Status des Teilnehmers ab.</span><span class="sxs-lookup"><span data-stu-id="919a5-126">Gets the status of the participant.</span></span><br/>                                                                                                                          |
| [<span data-ttu-id="919a5-127">**Daten \_ Ströme erhalten**</span><span class="sxs-lookup"><span data-stu-id="919a5-127">**get\_Streams**</span></span>](itparticipant-get-streams.md)                           | <span data-ttu-id="919a5-128">Erstellt eine Auflistung von Streams, die dem aktuellen Teilnehmer zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="919a5-128">Creates a collection of streams associated with the current participant.</span></span> <span data-ttu-id="919a5-129">Wird für Automatisierungs Client Anwendungen bereitgestellt, wie z. b. die in Visual Basic geschriebenen.</span><span class="sxs-lookup"><span data-stu-id="919a5-129">Provided for Automation client applications, such as those written in Visual Basic.</span></span><br/> |
| [<span data-ttu-id="919a5-130">**Put- \_ Status**</span><span class="sxs-lookup"><span data-stu-id="919a5-130">**put\_Status**</span></span>](itparticipant-put-status.md)                             | <span data-ttu-id="919a5-131">Legt fest, ob ein dem Teilnehmer zugeordneter Stream aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="919a5-131">Sets whether a stream associated with the participant is enabled.</span></span><br/>                                                                                            |



 

## <a name="requirements"></a><span data-ttu-id="919a5-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="919a5-132">Requirements</span></span>



| <span data-ttu-id="919a5-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="919a5-133">Requirement</span></span> | <span data-ttu-id="919a5-134">Wert</span><span class="sxs-lookup"><span data-stu-id="919a5-134">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="919a5-135">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="919a5-135">TAPI version</span></span><br/> | <span data-ttu-id="919a5-136">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="919a5-136">Requires TAPI 3.0 or later</span></span><br/>                                                |
| <span data-ttu-id="919a5-137">Header</span><span class="sxs-lookup"><span data-stu-id="919a5-137">Header</span></span><br/>       | <dl> <span data-ttu-id="919a5-138"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="919a5-138"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="919a5-139">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="919a5-139">Library</span></span><br/>      | <dl> <span data-ttu-id="919a5-140"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="919a5-140"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="919a5-141">DLL</span><span class="sxs-lookup"><span data-stu-id="919a5-141">DLL</span></span><br/>          | <dl> <span data-ttu-id="919a5-142"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="919a5-142"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="919a5-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="919a5-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="919a5-144">Ipconf-msp</span><span class="sxs-lookup"><span data-stu-id="919a5-144">IPConf MSP</span></span>](ipconf-msp.md)
</dt> <dt>

[<span data-ttu-id="919a5-145">Ipconf-MSP-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="919a5-145">IPConf MSP Interfaces</span></span>](ipconf-msp-interfaces.md)
</dt> <dt>

[<span data-ttu-id="919a5-146">**Itcallinfo**</span><span class="sxs-lookup"><span data-stu-id="919a5-146">**ITCallInfo**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)
</dt> </dl>

 

