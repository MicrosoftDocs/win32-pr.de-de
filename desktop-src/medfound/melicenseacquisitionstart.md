---
description: Wird von der-Richtlinien-Engine ausgelöst, wenn der Lizenzerwerb beginnt. Der Lizenzerwerb erfolgt mithilfe der Anwendungs Implementierung der imbocontentschutzmanager-Schnittstelle.
ms.assetid: c328743c-a69b-431e-8a05-0e140aad9b4d
title: Melicenmenacquisitionstart-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 914d2580c95cf40986a844a994c1e284c5ad9e22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356606"
---
# <a name="melicenseacquisitionstart-event"></a><span data-ttu-id="e8991-104">Melicenmenacquisitionstart-Ereignis</span><span class="sxs-lookup"><span data-stu-id="e8991-104">MELicenseAcquisitionStart event</span></span>

<span data-ttu-id="e8991-105">Wird von der-Richtlinien-Engine ausgelöst, wenn der Lizenzerwerb beginnt.</span><span class="sxs-lookup"><span data-stu-id="e8991-105">Raised by the policy engine when license acquisition is about to begin.</span></span> <span data-ttu-id="e8991-106">Der Lizenzerwerb erfolgt mithilfe der Implementierung der Anwendung der [**imbocontentschutzmanager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="e8991-106">License acquisition is performed using the application's implementation of the [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) interface.</span></span>

## <a name="event-values"></a><span data-ttu-id="e8991-107">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="e8991-107">Event values</span></span>

<span data-ttu-id="e8991-108">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="e8991-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="e8991-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="e8991-109">VARTYPE</span></span>              | <span data-ttu-id="e8991-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e8991-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="e8991-111">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="e8991-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="e8991-112">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="e8991-112">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="e8991-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e8991-113">Remarks</span></span>

<span data-ttu-id="e8991-114">Wenn die Lizenz Erfassung abgeschlossen ist, löst die Richtlinien-Engine das Ereignis " [melicenabacquisitionabgeschlossene](melicenseacquisitioncompleted.md) " aus.</span><span class="sxs-lookup"><span data-stu-id="e8991-114">When license acquisition is completed, the policy engine raises the [MELicenseAcquisitionCompleted](melicenseacquisitioncompleted.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8991-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e8991-115">Requirements</span></span>



| <span data-ttu-id="e8991-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e8991-116">Requirement</span></span> | <span data-ttu-id="e8991-117">Wert</span><span class="sxs-lookup"><span data-stu-id="e8991-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8991-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e8991-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e8991-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e8991-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e8991-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e8991-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e8991-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e8991-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e8991-122">Header</span><span class="sxs-lookup"><span data-stu-id="e8991-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8991-123"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e8991-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8991-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e8991-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8991-125">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e8991-125">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




