---
description: Wird durch eine streamsenke ausgelöst, nachdem die imfstreamsink::P lacemarker-Methode aufgerufen wurde.
ms.assetid: 40f68352-86e5-4864-9ca0-f30998857fef
title: Mestreamsinkmarker-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 071d6e5b25873739c176d1c808929c26e1e338bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754296"
---
# <a name="mestreamsinkmarker-event"></a><span data-ttu-id="f1e9f-103">Mestreamsinkmarker-Ereignis</span><span class="sxs-lookup"><span data-stu-id="f1e9f-103">MEStreamSinkMarker event</span></span>

<span data-ttu-id="f1e9f-104">Wird durch eine streamsenke ausgelöst, nachdem die [**imfstreamsink::P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) -Methode aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="f1e9f-104">Raised by a stream sink after the [**IMFStreamSink::PlaceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) method is called.</span></span>

## <a name="event-values"></a><span data-ttu-id="f1e9f-105">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="f1e9f-105">Event values</span></span>

<span data-ttu-id="f1e9f-106">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="f1e9f-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="f1e9f-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="f1e9f-107">VARTYPE</span></span>            | <span data-ttu-id="f1e9f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f1e9f-108">Description</span></span>                                                                                                                                                                                           |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1e9f-109">></span><span class="sxs-lookup"><span data-stu-id="f1e9f-109">>Any</span></span><br/> | <span data-ttu-id="f1e9f-110">Der Ereignis Wert ist eine Kopie der **PROPVARIANT** , die der Aufrufer im *pvarcontextvalue* -Parameter der [**Placemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) -Methode angegeben hat.</span><span class="sxs-lookup"><span data-stu-id="f1e9f-110">The event value is a copy of the **PROPVARIANT** that the caller specified in the *pvarContextValue* parameter of the [**PlaceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) method.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="f1e9f-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f1e9f-111">Requirements</span></span>



| <span data-ttu-id="f1e9f-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f1e9f-112">Requirement</span></span> | <span data-ttu-id="f1e9f-113">Wert</span><span class="sxs-lookup"><span data-stu-id="f1e9f-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1e9f-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f1e9f-114">Minimum supported client</span></span><br/> | <span data-ttu-id="f1e9f-115">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f1e9f-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f1e9f-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f1e9f-116">Minimum supported server</span></span><br/> | <span data-ttu-id="f1e9f-117">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f1e9f-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f1e9f-118">Header</span><span class="sxs-lookup"><span data-stu-id="f1e9f-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1e9f-119"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f1e9f-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1e9f-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f1e9f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1e9f-121">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f1e9f-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="f1e9f-122">Medien senken</span><span class="sxs-lookup"><span data-stu-id="f1e9f-122">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 




