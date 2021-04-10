---
description: Wird von der Medien Sitzung ausgelöst, wenn sich das Format in einer Medien Senke ändert.
ms.assetid: f56419f8-7f50-4eda-bf4a-fcdbbe46e180
title: Mesessionstreamsinkformatchanged-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bed59b9600cbaf8cb942a42beb6bed46d62fc15f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215163"
---
# <a name="mesessionstreamsinkformatchanged-event"></a><span data-ttu-id="109ed-103">Mesessionstreamsinkformatchanged-Ereignis</span><span class="sxs-lookup"><span data-stu-id="109ed-103">MESessionStreamSinkFormatChanged event</span></span>

<span data-ttu-id="109ed-104">Wird von der Medien Sitzung ausgelöst, wenn sich das Format in einer Medien Senke ändert.</span><span class="sxs-lookup"><span data-stu-id="109ed-104">Raised by the Media Session when the format changes on a media sink.</span></span>

## <a name="event-values"></a><span data-ttu-id="109ed-105">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="109ed-105">Event values</span></span>

<span data-ttu-id="109ed-106">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="109ed-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="109ed-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="109ed-107">VARTYPE</span></span>              | <span data-ttu-id="109ed-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="109ed-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="109ed-109">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="109ed-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="109ed-110">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="109ed-110">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="109ed-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="109ed-111">Attributes</span></span>

<span data-ttu-id="109ed-112">Für dieses Ereignis sind die folgenden Attribute definiert:</span><span class="sxs-lookup"><span data-stu-id="109ed-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="109ed-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="109ed-113">Attribute</span></span>                                                                    | <span data-ttu-id="109ed-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="109ed-114">Description</span></span>                                                                                  |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="109ed-115">**MF- \_ Ereignis \_ Ausgabe \_ Knoten**</span><span class="sxs-lookup"><span data-stu-id="109ed-115">**MF\_EVENT\_OUTPUT\_NODE**</span></span>](mf-event-output-node-attribute.md)<br/> | <span data-ttu-id="109ed-116">Identifiziert den topologieknoten für die Medien Senke, deren Format geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="109ed-116">Identifies the topology node for the media sink whose format changed.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="109ed-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="109ed-117">Requirements</span></span>



| <span data-ttu-id="109ed-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="109ed-118">Requirement</span></span> | <span data-ttu-id="109ed-119">Wert</span><span class="sxs-lookup"><span data-stu-id="109ed-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="109ed-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="109ed-120">Minimum supported client</span></span><br/> | <span data-ttu-id="109ed-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="109ed-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="109ed-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="109ed-122">Minimum supported server</span></span><br/> | <span data-ttu-id="109ed-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="109ed-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="109ed-124">Header</span><span class="sxs-lookup"><span data-stu-id="109ed-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="109ed-125"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="109ed-125"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="109ed-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="109ed-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="109ed-127">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="109ed-127">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




