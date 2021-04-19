---
description: Wird von einem Medienstream ausgelöst, wenn der Stream gestartet oder beendet wird. Weitere Informationen zur Daten Verdünnung finden Sie unter Informationen zur Raten Kontrolle.
ms.assetid: 7de8cb64-122a-475f-990c-c19590a9d9d8
title: Mestreamthinmode-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7e19d25e5ab0430d96a9d431c941288e260092b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350554"
---
# <a name="mestreamthinmode-event"></a><span data-ttu-id="4cd90-104">Mestreamthinmode-Ereignis</span><span class="sxs-lookup"><span data-stu-id="4cd90-104">MEStreamThinMode event</span></span>

<span data-ttu-id="4cd90-105">Wird von einem Medienstream ausgelöst, wenn der Stream gestartet oder beendet wird.</span><span class="sxs-lookup"><span data-stu-id="4cd90-105">Raised by a media stream when it starts or stops thinning the stream.</span></span> <span data-ttu-id="4cd90-106">Weitere Informationen zur Daten *Verdünnung* finden Sie unter Informationen [zur Raten Kontrolle](about-rate-control.md).</span><span class="sxs-lookup"><span data-stu-id="4cd90-106">For information about *thinning*, see [About Rate Control](about-rate-control.md).</span></span>

<span data-ttu-id="4cd90-107">Dieses Ereignis kann als Reaktion auf die [**imfratecontrol:: setRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) -Methode oder die [**imfqualityempfehlung:: setdropmode**](/windows/desktop/api/mfidl/nf-mfidl-imfqualityadvise-setdropmode) -Methode gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="4cd90-107">This event can be sent in response to the [**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) method or the [**IMFQualityAdvise::SetDropMode**](/windows/desktop/api/mfidl/nf-mfidl-imfqualityadvise-setdropmode) method.</span></span>

## <a name="event-values"></a><span data-ttu-id="4cd90-108">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="4cd90-108">Event values</span></span>

<span data-ttu-id="4cd90-109">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="4cd90-109">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4cd90-110">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="4cd90-110">VARTYPE</span></span></th>
<th><span data-ttu-id="4cd90-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4cd90-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4cd90-112">VT_BOOL</span><span class="sxs-lookup"><span data-stu-id="4cd90-112">VT_BOOL</span></span><br/></td>
<td><span data-ttu-id="4cd90-113">Gibt an, ob die Verdünnung gestartet oder beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="4cd90-113">Indicates whether thinning has started or stopped.</span></span><br/>
<ul>
<li><span data-ttu-id="4cd90-114">VARIANT_TRUE: die nach diesem Ereignis übermittelten Beispiele sind dünn.</span><span class="sxs-lookup"><span data-stu-id="4cd90-114">VARIANT_TRUE: Samples delivered after this event are thinned.</span></span></li>
<li><span data-ttu-id="4cd90-115">VARIANT_FALSE: die nach diesem Ereignis übermittelten Beispiele sind nicht dünn.</span><span class="sxs-lookup"><span data-stu-id="4cd90-115">VARIANT_FALSE: Samples delivered after this event are not thinned.</span></span></li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="4cd90-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4cd90-116">Requirements</span></span>



| <span data-ttu-id="4cd90-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4cd90-117">Requirement</span></span> | <span data-ttu-id="4cd90-118">Wert</span><span class="sxs-lookup"><span data-stu-id="4cd90-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cd90-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4cd90-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4cd90-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4cd90-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4cd90-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4cd90-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4cd90-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4cd90-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4cd90-123">Header</span><span class="sxs-lookup"><span data-stu-id="4cd90-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4cd90-124"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4cd90-124"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cd90-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4cd90-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cd90-126">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4cd90-126">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




