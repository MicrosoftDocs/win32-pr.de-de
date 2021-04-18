---
description: Markiert einen Punkt im Stream. Diese Meldung gilt nur für asynchrone MFTs.
ms.assetid: eae1d066-64af-45e2-b8bb-eddf9147ad8b
title: MFT_MESSAGE_COMMAND_MARKER (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3802cb94c9183d4f392fbcedcf48c0c01071298e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368231"
---
# <a name="mft_message_command_marker"></a><span data-ttu-id="db49c-104">MFT- \_ Nachrichten \_ Befehls \_ Marker</span><span class="sxs-lookup"><span data-stu-id="db49c-104">MFT\_MESSAGE\_COMMAND\_MARKER</span></span>

<span data-ttu-id="db49c-105">Markiert einen Punkt im Stream.</span><span class="sxs-lookup"><span data-stu-id="db49c-105">Marks a point in the stream.</span></span> <span data-ttu-id="db49c-106">Diese Meldung gilt nur für [asynchrone MFTs](asynchronous-mfts.md).</span><span class="sxs-lookup"><span data-stu-id="db49c-106">This message applies only to [Asynchronous MFTs](asynchronous-mfts.md).</span></span>

## <a name="message-parameter"></a><span data-ttu-id="db49c-107">Message-Parameter</span><span class="sxs-lookup"><span data-stu-id="db49c-107">Message Parameter</span></span>

<span data-ttu-id="db49c-108">Ein beliebiger Wert.</span><span class="sxs-lookup"><span data-stu-id="db49c-108">An arbitrary value.</span></span> <span data-ttu-id="db49c-109">Der MFT gibt den Wert im [metransformmarker](metransformmarker.md) -Ereignis an den Client zurück.</span><span class="sxs-lookup"><span data-stu-id="db49c-109">The MFT returns the value to the client in the [METransformMarker](metransformmarker.md) event.</span></span>

## <a name="remarks"></a><span data-ttu-id="db49c-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="db49c-110">Remarks</span></span>

<span data-ttu-id="db49c-111">Um diese Nachricht zu senden, nennen Sie [**imftransform::P rocess Message**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span><span class="sxs-lookup"><span data-stu-id="db49c-111">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="db49c-112">Die MFT antwortet auf diese messageas:</span><span class="sxs-lookup"><span data-stu-id="db49c-112">The MFT responds to this messageas follows:</span></span>

1.  <span data-ttu-id="db49c-113">Der MFT generiert so viele Ausgabe Beispiele wie aus den vorhandenen Eingabedaten und sendet ein [metransformhaveoutput](metransformhaveoutput.md) -Ereignis für jedes Ausgabe Beispiel.</span><span class="sxs-lookup"><span data-stu-id="db49c-113">The MFT generates as many output samples as it can from the existing input data, sending an [METransformHaveOutput](metransformhaveoutput.md) event for each output sample.</span></span>
2.  <span data-ttu-id="db49c-114">Nachdem die gesamte Ausgabe generiert wurde, sendet der MFT ein [metransformmarker](metransformmarker.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="db49c-114">After all of the output is generated, the MFT sends an [METransformMarker](metransformmarker.md) event.</span></span> <span data-ttu-id="db49c-115">Dieses Ereignis muss nach allen [metransformhaveoutput](metransformhaveoutput.md) -Ereignissen gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="db49c-115">This event must be sent after all of the [METransformHaveOutput](metransformhaveoutput.md) events.</span></span>

<span data-ttu-id="db49c-116">Der Client muss diese Nachricht nicht senden und sollte diese Nachricht nur an asynchrone MFTs senden.</span><span class="sxs-lookup"><span data-stu-id="db49c-116">The client is not required to send this message, and should send this message only to asynchronous MFTs.</span></span> <span data-ttu-id="db49c-117">Ein synchrones MFT sendet kein [metransformmarker](metransformmarker.md) -Ereignis als Antwort auf diese Meldung.</span><span class="sxs-lookup"><span data-stu-id="db49c-117">A synchronous MFT will not send an [METransformMarker](metransformmarker.md) event in response to this message.</span></span>

### <a name="implementation"></a><span data-ttu-id="db49c-118">Implementierung</span><span class="sxs-lookup"><span data-stu-id="db49c-118">Implementation</span></span>

<span data-ttu-id="db49c-119">Asynchrone MFTs müssen wie beschrieben auf diese Meldung Antworten.</span><span class="sxs-lookup"><span data-stu-id="db49c-119">Asynchronous MFTs must respond to this message as described.</span></span> <span data-ttu-id="db49c-120">Diese Meldung sollte durch synchrone MFTs ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="db49c-120">Synchronous MFTs should ignore this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="db49c-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="db49c-121">Requirements</span></span>



| <span data-ttu-id="db49c-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="db49c-122">Requirement</span></span> | <span data-ttu-id="db49c-123">Wert</span><span class="sxs-lookup"><span data-stu-id="db49c-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="db49c-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="db49c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="db49c-125">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="db49c-125">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="db49c-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="db49c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="db49c-127">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="db49c-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="db49c-128">Header</span><span class="sxs-lookup"><span data-stu-id="db49c-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="db49c-129"><dt>"MF Transform. h"</dt></span><span class="sxs-lookup"><span data-stu-id="db49c-129"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db49c-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="db49c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db49c-131">**MFT \_ - \_ Nachrichtentyp**</span><span class="sxs-lookup"><span data-stu-id="db49c-131">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




