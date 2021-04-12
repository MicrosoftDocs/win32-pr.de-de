---
description: Wird von einem asynchronen Media Foundation Transform (MFT) gesendet, wenn ein Ausgleichs Vorgang beendet ist.
ms.assetid: 923055e5-a09a-402e-983b-6fa3cebb1b3a
title: Metransformdraunvollereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed291f9edacb11ba6edf7f5bd50a0715ae61a281
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348748"
---
# <a name="metransformdraincomplete-event"></a><span data-ttu-id="2d187-103">Metransformdraunvollständiges Ereignis</span><span class="sxs-lookup"><span data-stu-id="2d187-103">METransformDrainComplete event</span></span>

<span data-ttu-id="2d187-104">Wird von einem asynchronen Media Foundation Transform (MFT) gesendet, wenn ein Ausgleichs Vorgang beendet ist.</span><span class="sxs-lookup"><span data-stu-id="2d187-104">Sent by an asynchronous Media Foundation transform (MFT) when a drain operation is complete.</span></span>

## <a name="event-values"></a><span data-ttu-id="2d187-105">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="2d187-105">Event values</span></span>

<span data-ttu-id="2d187-106">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="2d187-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="2d187-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="2d187-107">VARTYPE</span></span>              | <span data-ttu-id="2d187-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2d187-108">Description</span></span>               |
|----------------------|---------------------------|
| <span data-ttu-id="2d187-109">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="2d187-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="2d187-110">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="2d187-110">No event data.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="2d187-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="2d187-111">Attributes</span></span>

<span data-ttu-id="2d187-112">Für dieses Ereignis sind die folgenden Attribute definiert:</span><span class="sxs-lookup"><span data-stu-id="2d187-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="2d187-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="2d187-113">Attribute</span></span>                                                                        | <span data-ttu-id="2d187-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2d187-114">Description</span></span>                                                                      |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="2d187-115">\_ \_ MFT- \_ Eingabedaten \_ Strom- \_ ID des MF-Ereignisses</span><span class="sxs-lookup"><span data-stu-id="2d187-115">MF\_EVENT\_MFT\_INPUT\_STREAM\_ID</span></span>](mf-event-mft-input-stream-id.md)<br/> | <span data-ttu-id="2d187-116">Der Bezeichner des Datenstroms, der entladen wurde.</span><span class="sxs-lookup"><span data-stu-id="2d187-116">The identifier of the stream that was drained.</span></span><br/><span data-ttu-id="2d187-117">*Benötigten*</span><span class="sxs-lookup"><span data-stu-id="2d187-117">*(Required)*</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="2d187-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2d187-118">Remarks</span></span>

<span data-ttu-id="2d187-119">Asynchrone MFTs Senden dieses Ereignis über die [**IMF mediaeventgenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="2d187-119">Asynchronous MFTs send this event through the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="2d187-120">Dieses Ereignis wird von synchronen MFTs niemals gesendet.</span><span class="sxs-lookup"><span data-stu-id="2d187-120">Synchronous MFTs never send this event.</span></span>

<span data-ttu-id="2d187-121">Um einen MFT zu entleeren, wenden Sie [**imftransform::P rocess Message**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) mit der **MFT- \_ Nachrichten \_ Befehls \_** Ausgleichs Meldung an.</span><span class="sxs-lookup"><span data-stu-id="2d187-121">To drain an MFT, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) with the **MFT\_MESSAGE\_COMMAND\_DRAIN** message.</span></span> <span data-ttu-id="2d187-122">Geben Sie den Eingabedaten Strom an, der im *ulparam* -Parameter geleert werden soll.</span><span class="sxs-lookup"><span data-stu-id="2d187-122">Specify the input stream to drain in the *ulParam* parameter.</span></span> <span data-ttu-id="2d187-123">Wenn der Ausgleichs Vorgang abgeschlossen ist, sendet eine asynchrone MFT das metransformdraunvoll-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="2d187-123">When the drain operation is completed, an asynchronous MFT sends the METransformDrainComplete event.</span></span> <span data-ttu-id="2d187-124">Das [MF- \_ Ereignis \_ MFT-Eingabedaten Strom- \_ \_ \_ ID](mf-event-mft-input-stream-id.md) -Attribut des Ereignisses enthält den im *ulparam* -Parameter angegebenen Datenstrom Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="2d187-124">The [MF\_EVENT\_MFT\_INPUT\_STREAM\_ID](mf-event-mft-input-stream-id.md) attribute of the event contains the stream identifier given in the *ulParam* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d187-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2d187-125">Requirements</span></span>



| <span data-ttu-id="2d187-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2d187-126">Requirement</span></span> | <span data-ttu-id="2d187-127">Wert</span><span class="sxs-lookup"><span data-stu-id="2d187-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d187-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2d187-128">Minimum supported client</span></span><br/> | <span data-ttu-id="2d187-129">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2d187-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="2d187-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2d187-130">Minimum supported server</span></span><br/> | <span data-ttu-id="2d187-131">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2d187-131">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="2d187-132">Header</span><span class="sxs-lookup"><span data-stu-id="2d187-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d187-133"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2d187-133"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d187-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2d187-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d187-135">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2d187-135">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="2d187-136">Asynchrone MFTs</span><span class="sxs-lookup"><span data-stu-id="2d187-136">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> </dl>

 

 




