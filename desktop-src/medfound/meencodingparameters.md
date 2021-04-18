---
description: Gesendet von der Pipeline an Encoder-MFTs serialisiert mit Medien Beispielen über imftransform::P rocesabvent.
ms.assetid: D5D4544B-CD8D-4C94-B050-7BA1944800CC
title: Meencodingparameters-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e193044b25eb1d333182a2593fcf2248fba2366
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215170"
---
# <a name="meencodingparameters-event"></a><span data-ttu-id="4afe4-103">Meencodingparameters-Ereignis</span><span class="sxs-lookup"><span data-stu-id="4afe4-103">MEEncodingParameters event</span></span>

<span data-ttu-id="4afe4-104">Gesendet von der Pipeline an Encoder-MFTs serialisiert mit Medien Beispielen über [**imftransform::P rocesabvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent).</span><span class="sxs-lookup"><span data-stu-id="4afe4-104">Sent by the pipeline to encoder MFTs serially with media samples via [**IMFTransform::ProcessEvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent).</span></span>

## <a name="event-values"></a><span data-ttu-id="4afe4-105">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="4afe4-105">Event values</span></span>

<span data-ttu-id="4afe4-106">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="4afe4-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="4afe4-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="4afe4-107">VARTYPE</span></span>              | <span data-ttu-id="4afe4-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4afe4-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="4afe4-109">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="4afe4-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="4afe4-110">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="4afe4-110">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="4afe4-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="4afe4-111">Attributes</span></span>

<span data-ttu-id="4afe4-112">Für dieses Ereignis sind die folgenden Attribute definiert:</span><span class="sxs-lookup"><span data-stu-id="4afe4-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="4afe4-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="4afe4-113">Attribute</span></span>                                         | <span data-ttu-id="4afe4-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4afe4-114">Description</span></span>                                                                                                                    |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4afe4-115">**Imfattributes**</span><span class="sxs-lookup"><span data-stu-id="4afe4-115">**IMFAttributes**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)<br/> | <span data-ttu-id="4afe4-116">Enthält die neuen icodecapi-basierten Einstellungen, die der Encoder auf nachfolgende eingehende Stichproben anwenden soll.</span><span class="sxs-lookup"><span data-stu-id="4afe4-116">Contains the new ICodecAPI-based settings that the encoder should apply on subsequent incoming samples.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="4afe4-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4afe4-117">Remarks</span></span>

<span data-ttu-id="4afe4-118">Die Ereignis Nutzlast ist ein Attribut Speicher (imfattributes-Zeiger), der die neuen icodecapi-basierten///-Einstellungen enthält, die der Encoder auf nachfolgende eingehende Beispiele anwenden soll.</span><span class="sxs-lookup"><span data-stu-id="4afe4-118">Event payload is an attribute store (IMFAttributes pointer) that contains the new ICodecAPI-based /// settings that the encoder should apply on subsequent incoming samples.</span></span>

## <a name="requirements"></a><span data-ttu-id="4afe4-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4afe4-119">Requirements</span></span>



| <span data-ttu-id="4afe4-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4afe4-120">Requirement</span></span> | <span data-ttu-id="4afe4-121">Wert</span><span class="sxs-lookup"><span data-stu-id="4afe4-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4afe4-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4afe4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4afe4-123">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="4afe4-123">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="4afe4-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4afe4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4afe4-125">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4afe4-125">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="4afe4-126">Header</span><span class="sxs-lookup"><span data-stu-id="4afe4-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4afe4-127"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4afe4-127"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4afe4-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4afe4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4afe4-129">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4afe4-129">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




