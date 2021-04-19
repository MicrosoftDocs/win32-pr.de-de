---
description: Wird von der Richtlinien-Engine ausgelöst, wenn die Individualisierung fertiggestellt ist. Weitere Informationen finden Sie unter "meindividualizationstart"-Ereignis.
ms.assetid: 44a4956f-19ba-410d-b96c-e7774cbe2d7e
title: Meindividualizationabgeschlossene-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7143274d12a9ad113f714062ff8f88c1fb8277cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348873"
---
# <a name="meindividualizationcompleted-event"></a><span data-ttu-id="31d26-104">Meindividualizationabgeschlossene-Ereignis</span><span class="sxs-lookup"><span data-stu-id="31d26-104">MEIndividualizationCompleted event</span></span>

<span data-ttu-id="31d26-105">Wird von der Richtlinien-Engine ausgelöst, wenn die Individualisierung fertiggestellt ist.</span><span class="sxs-lookup"><span data-stu-id="31d26-105">Raised by the policy engine when individualization is complete.</span></span> <span data-ttu-id="31d26-106">Weitere Informationen finden Sie unter " [meindividualizationstart](meindividualizationstart.md) "-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="31d26-106">For more information, see [MEIndividualizationStart](meindividualizationstart.md) event.</span></span>

## <a name="event-values"></a><span data-ttu-id="31d26-107">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="31d26-107">Event values</span></span>

<span data-ttu-id="31d26-108">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="31d26-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="31d26-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="31d26-109">VARTYPE</span></span>              | <span data-ttu-id="31d26-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="31d26-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="31d26-111">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="31d26-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="31d26-112">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="31d26-112">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="31d26-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="31d26-113">Requirements</span></span>



| <span data-ttu-id="31d26-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="31d26-114">Requirement</span></span> | <span data-ttu-id="31d26-115">Wert</span><span class="sxs-lookup"><span data-stu-id="31d26-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31d26-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="31d26-116">Minimum supported client</span></span><br/> | <span data-ttu-id="31d26-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="31d26-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="31d26-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="31d26-118">Minimum supported server</span></span><br/> | <span data-ttu-id="31d26-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="31d26-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="31d26-120">Header</span><span class="sxs-lookup"><span data-stu-id="31d26-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="31d26-121"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="31d26-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31d26-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="31d26-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31d26-123">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="31d26-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




