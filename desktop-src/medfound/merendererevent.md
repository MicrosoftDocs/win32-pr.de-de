---
description: Signalisiert ein Ereignis aus einer Medien Senke, die Mediendaten rendert.
ms.assetid: bb7db7c9-c39f-4bf4-9412-42525c4f2ea3
title: Merendererevent-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c52e15bfbe97743e8af10a79cf3ef1d94626a877
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215166"
---
# <a name="merendererevent-event"></a><span data-ttu-id="44fa9-103">Merendererevent-Ereignis</span><span class="sxs-lookup"><span data-stu-id="44fa9-103">MERendererEvent event</span></span>

<span data-ttu-id="44fa9-104">Signalisiert ein Ereignis aus einer Medien Senke, die Mediendaten rendert.</span><span class="sxs-lookup"><span data-stu-id="44fa9-104">Signals an event from a media sink that renders media data.</span></span>

<span data-ttu-id="44fa9-105">Der [Erweiterte Videorenderer](enhanced-video-renderer.md) (EVR) sendet dieses Ereignis, wenn es ein Benutzer Ereignis aus dem EVR Presenter empfängt.</span><span class="sxs-lookup"><span data-stu-id="44fa9-105">The [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR) sends this event when it receives a user event from the EVR presenter.</span></span>

## <a name="event-values"></a><span data-ttu-id="44fa9-106">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="44fa9-106">Event values</span></span>

<span data-ttu-id="44fa9-107">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="44fa9-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="44fa9-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="44fa9-108">VARTYPE</span></span>           | <span data-ttu-id="44fa9-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="44fa9-109">Description</span></span>                        |
|-------------------|------------------------------------|
| <span data-ttu-id="44fa9-110">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="44fa9-110">VT\_I4</span></span><br/> | <span data-ttu-id="44fa9-111">Ereignis Code.</span><span class="sxs-lookup"><span data-stu-id="44fa9-111">Event code.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="44fa9-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="44fa9-112">Remarks</span></span>

<span data-ttu-id="44fa9-113">Wenn der Presenter die **imediaeventsink:: notify** -Methode von EVR mit einem Ereignis Code im Bereich EC \_ User oder höher aufruft, sendet der EVR dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="44fa9-113">If the presenter calls the EVR's **IMediaEventSink::Notify** method with an event code in the range EC\_USER or higher, the EVR sends this event.</span></span> <span data-ttu-id="44fa9-114">Bei den Ereignisdaten handelt es sich um den Ereignis Code, der an die **Benachrichtigungs** Methode übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="44fa9-114">The event data is the event code that was passed to the **Notify** method.</span></span>

<span data-ttu-id="44fa9-115">Die ursprünglichen Ereignis Parameter (*EventParam1* und *EventParam2* in der **imediaeventsink:: notify** -Methode) werden ignoriert, daher sollte der Presenter diese Werte auf **null** festlegen.</span><span class="sxs-lookup"><span data-stu-id="44fa9-115">The original event parameters (*EventParam1* and *EventParam2* in the **IMediaEventSink::Notify** method) are ignored, so the presenter should set these values to **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="44fa9-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="44fa9-116">Requirements</span></span>



| <span data-ttu-id="44fa9-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="44fa9-117">Requirement</span></span> | <span data-ttu-id="44fa9-118">Wert</span><span class="sxs-lookup"><span data-stu-id="44fa9-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44fa9-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="44fa9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="44fa9-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="44fa9-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="44fa9-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="44fa9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="44fa9-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="44fa9-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="44fa9-123">Header</span><span class="sxs-lookup"><span data-stu-id="44fa9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="44fa9-124"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="44fa9-124"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44fa9-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="44fa9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44fa9-126">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="44fa9-126">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




