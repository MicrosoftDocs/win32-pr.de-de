---
description: Wird von einem Mediendaten Strom ausgelöst, wenn sich der Medientyp des Streams ändert.
ms.assetid: 14786a9b-413e-4fb4-b267-bfd0ccd4631b
title: Mestreamformatchanged-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd48e7abc8121707b150af5bc8968a50c1eb44e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863603"
---
# <a name="mestreamformatchanged-event"></a><span data-ttu-id="53f02-103">Mestreamformatchanged-Ereignis</span><span class="sxs-lookup"><span data-stu-id="53f02-103">MEStreamFormatChanged event</span></span>

<span data-ttu-id="53f02-104">Wird von einem Mediendaten Strom ausgelöst, wenn sich der Medientyp des Streams ändert.</span><span class="sxs-lookup"><span data-stu-id="53f02-104">Raised by a media stream when the media type of the stream changes.</span></span>

## <a name="event-values"></a><span data-ttu-id="53f02-105">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="53f02-105">Event values</span></span>

<span data-ttu-id="53f02-106">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="53f02-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="53f02-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="53f02-107">VARTYPE</span></span>                | <span data-ttu-id="53f02-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="53f02-108">Description</span></span>                                                                                                 |
|------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53f02-109">VT \_ unbekannt</span><span class="sxs-lookup"><span data-stu-id="53f02-109">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="53f02-110">Ein Zeiger auf die [**imfmediatype**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) -Schnittstelle des neuen Medientyps.</span><span class="sxs-lookup"><span data-stu-id="53f02-110">Pointer to the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface of the new media type.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="53f02-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="53f02-111">Remarks</span></span>

<span data-ttu-id="53f02-112">Verwenden Sie dieses Ereignis, um Formatänderungen im Stream zu signalisieren.</span><span class="sxs-lookup"><span data-stu-id="53f02-112">Use this event to signal format changes in the stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="53f02-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="53f02-113">Requirements</span></span>



| <span data-ttu-id="53f02-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="53f02-114">Requirement</span></span> | <span data-ttu-id="53f02-115">Wert</span><span class="sxs-lookup"><span data-stu-id="53f02-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53f02-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="53f02-116">Minimum supported client</span></span><br/> | <span data-ttu-id="53f02-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="53f02-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="53f02-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="53f02-118">Minimum supported server</span></span><br/> | <span data-ttu-id="53f02-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="53f02-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="53f02-120">Header</span><span class="sxs-lookup"><span data-stu-id="53f02-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="53f02-121"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="53f02-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53f02-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="53f02-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53f02-123">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="53f02-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




