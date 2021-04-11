---
description: Wird ausgelöst, wenn eine Medien Senke ungültig wird.
ms.assetid: fa75926e-7cef-44da-9efe-f2f86fd4fd45
title: Mesinkinvalivali-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46807a45e907999b34190f9678bd3dc0051680ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214778"
---
# <a name="mesinkinvalidated-event"></a><span data-ttu-id="0c895-103">Mesinkinvalivalidereignis</span><span class="sxs-lookup"><span data-stu-id="0c895-103">MESinkInvalidated event</span></span>

<span data-ttu-id="0c895-104">Wird ausgelöst, wenn eine Medien Senke ungültig wird.</span><span class="sxs-lookup"><span data-stu-id="0c895-104">Raised when a media sink becomes invalid.</span></span>

## <a name="event-values"></a><span data-ttu-id="0c895-105">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="0c895-105">Event values</span></span>

<span data-ttu-id="0c895-106">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="0c895-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="0c895-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0c895-107">VARTYPE</span></span>              | <span data-ttu-id="0c895-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0c895-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="0c895-109">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="0c895-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="0c895-110">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="0c895-110">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="0c895-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="0c895-111">Attributes</span></span>

<span data-ttu-id="0c895-112">Für dieses Ereignis sind die folgenden Attribute definiert:</span><span class="sxs-lookup"><span data-stu-id="0c895-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="0c895-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="0c895-113">Attribute</span></span>                                                                    | <span data-ttu-id="0c895-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0c895-114">Description</span></span>                                                              |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="0c895-115">**MF- \_ Ereignis \_ Ausgabe \_ Knoten**</span><span class="sxs-lookup"><span data-stu-id="0c895-115">**MF\_EVENT\_OUTPUT\_NODE**</span></span>](mf-event-output-node-attribute.md)<br/> | <span data-ttu-id="0c895-116">Identifiziert den topologieknoten für diese Medien Senke.</span><span class="sxs-lookup"><span data-stu-id="0c895-116">Identifies the topology node for this media sink.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="0c895-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0c895-117">Remarks</span></span>

<span data-ttu-id="0c895-118">Die Medien Sitzung löst dieses Ereignis aus, wenn eines der folgenden Ereignisse von der Medien Senke empfangen wird:</span><span class="sxs-lookup"><span data-stu-id="0c895-118">The Media Session raises this event if it receives any of the following events from the media sink:</span></span>

-   [<span data-ttu-id="0c895-119">Meaudiosessiondeviceremoved</span><span class="sxs-lookup"><span data-stu-id="0c895-119">MEAudioSessionDeviceRemoved</span></span>](meaudiosessiondeviceremoved.md)

-   [<span data-ttu-id="0c895-120">Meaudiosessiontrennt</span><span class="sxs-lookup"><span data-stu-id="0c895-120">MEAudioSessionDisconnected</span></span>](meaudiosessiondisconnected.md)

-   [<span data-ttu-id="0c895-121">Meaudiosessionexclusivemodeoverride</span><span class="sxs-lookup"><span data-stu-id="0c895-121">MEAudioSessionExclusiveModeOverride</span></span>](meaudiosessionexclusivemodeoverride.md)

-   [<span data-ttu-id="0c895-122">Meaudiosessionformatchanged</span><span class="sxs-lookup"><span data-stu-id="0c895-122">MEAudioSessionFormatChanged</span></span>](meaudiosessionformatchanged.md)

-   [<span data-ttu-id="0c895-123">Meaudiosessionservershutdown</span><span class="sxs-lookup"><span data-stu-id="0c895-123">MEAudioSessionServerShutdown</span></span>](meaudiosessionservershutdown.md)

<span data-ttu-id="0c895-124">Eine Medien Senke kann dieses Ereignis auch erhöhen. in diesem Fall legt die Medien Sitzung das Attribut " [**MF \_ Event \_ Output \_ Node**](mf-event-output-node-attribute.md) " für das Ereignis fest und leitet das Ereignis an die Anwendung weiter.</span><span class="sxs-lookup"><span data-stu-id="0c895-124">A media sink can also raise this event, in which case the Media Session sets the [**MF\_EVENT\_OUTPUT\_NODE**](mf-event-output-node-attribute.md) attribute on the event and forwards the event to the application.</span></span>

<span data-ttu-id="0c895-125">Wenn die Anwendung dieses Ereignis empfängt, muss Sie die Medien Senke neu erstellen und die Topologie erneut in die Warteschlange stellen.</span><span class="sxs-lookup"><span data-stu-id="0c895-125">If the application receives this event, it needs to recreate the media sink and queue the topology again.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c895-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0c895-126">Requirements</span></span>



| <span data-ttu-id="0c895-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0c895-127">Requirement</span></span> | <span data-ttu-id="0c895-128">Wert</span><span class="sxs-lookup"><span data-stu-id="0c895-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c895-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0c895-129">Minimum supported client</span></span><br/> | <span data-ttu-id="0c895-130">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0c895-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0c895-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0c895-131">Minimum supported server</span></span><br/> | <span data-ttu-id="0c895-132">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0c895-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0c895-133">Header</span><span class="sxs-lookup"><span data-stu-id="0c895-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c895-134"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0c895-134"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c895-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0c895-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c895-136">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0c895-136">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




