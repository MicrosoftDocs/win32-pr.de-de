---
description: Signalisiert den Fortschritt eines Inhalts Wegbereiter-Objekts. Objekte, die die imfcontentenabler-Schnittstelle verfügbar machen, können dieses Ereignis ausgeben, um die Anwendung über den Fortschritt der Aktionen des Inhalts Virtualisierungsebene zählt zu benachrichtigen.
ms.assetid: ec14ba9b-cfb6-4e32-870e-2436e11c308b
title: Meenablerprogress-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58303835113408a7fe09436967286d5ff988acdc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215171"
---
# <a name="meenablerprogress-event"></a><span data-ttu-id="ccabd-104">Meenablerprogress-Ereignis</span><span class="sxs-lookup"><span data-stu-id="ccabd-104">MEEnablerProgress event</span></span>

<span data-ttu-id="ccabd-105">Signalisiert den Fortschritt eines Inhalts Wegbereiter-Objekts.</span><span class="sxs-lookup"><span data-stu-id="ccabd-105">Signals the progress of a content enabler object.</span></span> <span data-ttu-id="ccabd-106">Objekte, die die [**imfcontentenabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) -Schnittstelle verfügbar machen, können dieses Ereignis ausgeben, um die Anwendung über den Fortschritt der Aktionen des Inhalts Enablers zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="ccabd-106">Objects that expose the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface can raise this event to notify the application about the progress of the content enabler's actions.</span></span>

## <a name="event-values"></a><span data-ttu-id="ccabd-107">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="ccabd-107">Event values</span></span>

<span data-ttu-id="ccabd-108">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="ccabd-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="ccabd-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="ccabd-109">VARTYPE</span></span>               | <span data-ttu-id="ccabd-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ccabd-110">Description</span></span>                                                               |
|-----------------------|---------------------------------------------------------------------------|
| <span data-ttu-id="ccabd-111">VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="ccabd-111">VT\_LPWSTR</span></span><br/> | <span data-ttu-id="ccabd-112">Breit Zeichen-Zeichenfolge, die den Fortschritt beschreibt.</span><span class="sxs-lookup"><span data-stu-id="ccabd-112">Wide-character string that describes the progress.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="ccabd-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ccabd-113">Remarks</span></span>

<span data-ttu-id="ccabd-114">Um dieses Ereignis zu erhalten, Fragen Sie die [**imfcontentenabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) -Schnittstelle für die [**imfmediaeventgenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="ccabd-114">To receive this event, query the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface for the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="ccabd-115">Aufrufen Sie dann [**imfmediaeventgenerator:: begingetevent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent), wie im Thema [Medienereignis-Generatoren](media-event-generators.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ccabd-115">Then call [**IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent), as described in the topic [Media Event Generators](media-event-generators.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ccabd-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ccabd-116">Requirements</span></span>



| <span data-ttu-id="ccabd-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ccabd-117">Requirement</span></span> | <span data-ttu-id="ccabd-118">Wert</span><span class="sxs-lookup"><span data-stu-id="ccabd-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccabd-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ccabd-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ccabd-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ccabd-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ccabd-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ccabd-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ccabd-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ccabd-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ccabd-123">Header</span><span class="sxs-lookup"><span data-stu-id="ccabd-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ccabd-124"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ccabd-124"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccabd-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ccabd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccabd-126">**IMF contentenabler**</span><span class="sxs-lookup"><span data-stu-id="ccabd-126">**IMFContentEnabler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler)
</dt> <dt>

[<span data-ttu-id="ccabd-127">Medienereignis Generatoren</span><span class="sxs-lookup"><span data-stu-id="ccabd-127">Media Event Generators</span></span>](media-event-generators.md)
</dt> <dt>

[<span data-ttu-id="ccabd-128">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ccabd-128">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




