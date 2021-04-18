---
description: Wird durch eine asynchrone Media Foundation Transformation (MFT) als Antwort auf eine MFT- \_ Nachrichten \_ Befehls \_ markernachricht gesendet.
ms.assetid: d0c0d62d-9133-4d4b-8606-c2ae1d4c9f0a
title: Metransformmarker-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab79c47e2ddb26f2366aff075548f7905807df1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354602"
---
# <a name="metransformmarker-event"></a><span data-ttu-id="a9df4-103">Metransformmarker-Ereignis</span><span class="sxs-lookup"><span data-stu-id="a9df4-103">METransformMarker event</span></span>

<span data-ttu-id="a9df4-104">Wird durch eine asynchrone Media Foundation Transformation (MFT) als Antwort auf eine **MFT- \_ Nachrichten \_ Befehls \_ markernachricht** gesendet.</span><span class="sxs-lookup"><span data-stu-id="a9df4-104">Sent by an asynchronous Media Foundation transform (MFT) in response to an **MFT\_MESSAGE\_COMMAND\_MARKER** message.</span></span>

## <a name="event-values"></a><span data-ttu-id="a9df4-105">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="a9df4-105">Event values</span></span>

<span data-ttu-id="a9df4-106">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="a9df4-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="a9df4-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="a9df4-107">VARTYPE</span></span>              | <span data-ttu-id="a9df4-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a9df4-108">Description</span></span>               |
|----------------------|---------------------------|
| <span data-ttu-id="a9df4-109">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="a9df4-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="a9df4-110">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="a9df4-110">No event data.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="a9df4-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="a9df4-111">Attributes</span></span>

<span data-ttu-id="a9df4-112">Für dieses Ereignis sind die folgenden Attribute definiert:</span><span class="sxs-lookup"><span data-stu-id="a9df4-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="a9df4-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="a9df4-113">Attribute</span></span>                                                      | <span data-ttu-id="a9df4-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a9df4-114">Description</span></span>                                                                                                                |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a9df4-115">\_ \_ MFT- \_ Kontext für MF-Ereignis</span><span class="sxs-lookup"><span data-stu-id="a9df4-115">MF\_EVENT\_MFT\_CONTEXT</span></span>](mf-event-mft-context.md)<br/> | <span data-ttu-id="a9df4-116">Der Wert des *ulparam* -Parameters aus der **MFT- \_ Nachrichten \_ Befehls \_ markernachricht** .</span><span class="sxs-lookup"><span data-stu-id="a9df4-116">The value of the *ulParam* parameter from the **MFT\_MESSAGE\_COMMAND\_MARKER** message.</span></span><br/><span data-ttu-id="a9df4-117">*Benötigten*</span><span class="sxs-lookup"><span data-stu-id="a9df4-117">*(Required)*</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a9df4-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a9df4-118">Remarks</span></span>

<span data-ttu-id="a9df4-119">Asynchrone MFTs Senden dieses Ereignis über die [**IMF mediaeventgenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="a9df4-119">Asynchronous MFTs send this event through the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="a9df4-120">Dieses Ereignis wird von synchronen MFTs niemals gesendet.</span><span class="sxs-lookup"><span data-stu-id="a9df4-120">Synchronous MFTs never send this event.</span></span>

<span data-ttu-id="a9df4-121">Der Client einer asynchronen MFT kann einen Marker im Stream platzieren, indem er [**imftransform::P rocess Message**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) mit der **MFT- \_ Nachrichten \_ Befehls \_ markernachricht** aufruft.</span><span class="sxs-lookup"><span data-stu-id="a9df4-121">The client of an asynchronous MFT can place a marker in the stream by calling [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) with the **MFT\_MESSAGE\_COMMAND\_MARKER** message.</span></span> <span data-ttu-id="a9df4-122">Der *ulparam* -Parameter enthält Anwendungs definierte Daten.</span><span class="sxs-lookup"><span data-stu-id="a9df4-122">The *ulParam* parameter contains application-defined data.</span></span>

<span data-ttu-id="a9df4-123">Wenn die MFT die Verarbeitung aller Eingabedaten abgeschlossen hat, die zum Zeitpunkt des [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) -Aufrufes aufgerufen wurden, fügt die MFT ein metransformmarker-Ereignis in die Warteschlange ein.</span><span class="sxs-lookup"><span data-stu-id="a9df4-123">When the MFT finishes processing all of the input data that was available at the time of the [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) call, the MFT queues an METransformMarker event.</span></span> <span data-ttu-id="a9df4-124">Das [ \_ \_ MFT- \_ Kontext](mf-event-mft-context.md) Attribut des MF-Ereignisses des Ereignisses enthält den Wert des *ulparam* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="a9df4-124">The [MF\_EVENT\_MFT\_CONTEXT](mf-event-mft-context.md) attribute of the event contains the value of the *ulParam* parameter.</span></span> <span data-ttu-id="a9df4-125">Weitere Informationen finden Sie unter [asynchrone MFTs](asynchronous-mfts.md).</span><span class="sxs-lookup"><span data-stu-id="a9df4-125">For more information, see [Asynchronous MFTs](asynchronous-mfts.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a9df4-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a9df4-126">Requirements</span></span>



| <span data-ttu-id="a9df4-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a9df4-127">Requirement</span></span> | <span data-ttu-id="a9df4-128">Wert</span><span class="sxs-lookup"><span data-stu-id="a9df4-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9df4-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a9df4-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a9df4-130">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a9df4-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="a9df4-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a9df4-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a9df4-132">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a9df4-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="a9df4-133">Header</span><span class="sxs-lookup"><span data-stu-id="a9df4-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9df4-134"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a9df4-134"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9df4-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a9df4-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9df4-136">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a9df4-136">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="a9df4-137">Asynchrone MFTs</span><span class="sxs-lookup"><span data-stu-id="a9df4-137">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> </dl>

 

 




