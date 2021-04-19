---
description: Wird von einer audioerfassungs Quelle gesendet, wenn die Verbindung mit der Erfassungs Audiositzung getrennt wird, weil der Audioserver heruntergefahren wird.
ms.assetid: 43284B3E-3018-44F3-8D6C-8C3041DCCD3E
title: Mecaptureaudiosessionservershutdown-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad934f6d60868c1db7c5b5b7907ff720312ea439
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359174"
---
# <a name="mecaptureaudiosessionservershutdown-event"></a><span data-ttu-id="abeff-103">Mecaptureaudiosessionservershutdown-Ereignis</span><span class="sxs-lookup"><span data-stu-id="abeff-103">MECaptureAudioSessionServerShutdown event</span></span>

<span data-ttu-id="abeff-104">Wird von einer audioerfassungs Quelle gesendet, wenn die Verbindung mit der Erfassungs Audiositzung getrennt wird, weil der Audioserver heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="abeff-104">Sent by an audio capture source when the capture audio session is disconnected due to the audio server being shutdown.</span></span>

## <a name="event-values"></a><span data-ttu-id="abeff-105">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="abeff-105">Event values</span></span>

<span data-ttu-id="abeff-106">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="abeff-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="abeff-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="abeff-107">VARTYPE</span></span>               | <span data-ttu-id="abeff-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="abeff-108">Description</span></span>                           |
|-----------------------|---------------------------------------|
| <span data-ttu-id="abeff-109">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="abeff-109">VT\_EMPTY</span></span> <br/> | <span data-ttu-id="abeff-110">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="abeff-110">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="abeff-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="abeff-111">Requirements</span></span>



| <span data-ttu-id="abeff-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="abeff-112">Requirement</span></span> | <span data-ttu-id="abeff-113">Wert</span><span class="sxs-lookup"><span data-stu-id="abeff-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abeff-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="abeff-114">Minimum supported client</span></span><br/> | <span data-ttu-id="abeff-115">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="abeff-115">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="abeff-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="abeff-116">Minimum supported server</span></span><br/> | <span data-ttu-id="abeff-117">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="abeff-117">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="abeff-118">Header</span><span class="sxs-lookup"><span data-stu-id="abeff-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="abeff-119"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="abeff-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abeff-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="abeff-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abeff-121">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="abeff-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




