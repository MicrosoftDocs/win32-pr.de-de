---
description: Fordert eine Media Foundation Transformation (MFT) an, um alle gespeicherten Daten zu leeren.
ms.assetid: c48f3a88-a007-4f30-ac60-9e5a8c24e1ee
title: MFT_MESSAGE_COMMAND_DRAIN (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa533cfddfda53fd8eb0ee512b0535aaf9ad8f88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343424"
---
# <a name="mft_message_command_drain"></a><span data-ttu-id="7174e-103">MFT- \_ Nachrichten \_ Befehls \_ Ableitung</span><span class="sxs-lookup"><span data-stu-id="7174e-103">MFT\_MESSAGE\_COMMAND\_DRAIN</span></span>

<span data-ttu-id="7174e-104">Fordert eine Media Foundation Transformation (MFT) an, um alle gespeicherten Daten zu leeren.</span><span class="sxs-lookup"><span data-stu-id="7174e-104">Requests a Media Foundation transform (MFT) to flush all stored data.</span></span>

## <a name="message-parameter"></a><span data-ttu-id="7174e-105">Message-Parameter</span><span class="sxs-lookup"><span data-stu-id="7174e-105">Message Parameter</span></span>

<span data-ttu-id="7174e-106">Keine.</span><span class="sxs-lookup"><span data-stu-id="7174e-106">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="7174e-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7174e-107">Remarks</span></span>

<span data-ttu-id="7174e-108">Um diese Nachricht zu senden, nennen Sie [**imftransform::P rocess Message**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span><span class="sxs-lookup"><span data-stu-id="7174e-108">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="7174e-109">Nachdem diese Nachricht gesendet wurde, akzeptiert der angegebene Eingabedaten Strom erst dann Eingaben, wenn der MFT alle Daten aus vorherigen Aufrufen von [**imftransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)verarbeitet hat.</span><span class="sxs-lookup"><span data-stu-id="7174e-109">After this message is sent, the specified input stream does not accept input until the MFT processes all data from previous calls to [**IMFTransform::ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).</span></span>

<span data-ttu-id="7174e-110">Der Entleerungsprozess variiert geringfügig zwischen synchronen und asynchronen MFTs:</span><span class="sxs-lookup"><span data-stu-id="7174e-110">The draining process varies slightly between synchronous MFTs and asynchronous MFTs:</span></span>

<span data-ttu-id="7174e-111">**Synchrone MFTs**</span><span class="sxs-lookup"><span data-stu-id="7174e-111">**Synchronous MFTs**</span></span>

1.  <span data-ttu-id="7174e-112">Nachdem der Client diese Nachricht gesendet hat, ruft er [**imftransform::P rocess Output**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) in einer Schleife auf, bis **ProcessOutput** den Fehlercode **MF-E- \_ \_ Transformation \_ benötigt \_ mehr \_ Eingaben** zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="7174e-112">After the client sends this message, it calls [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) in a loop, until **ProcessOutput** returns the error code **MF\_E\_TRANSFORM\_NEED\_MORE\_INPUT**.</span></span>
2.  <span data-ttu-id="7174e-113">Solange die MFT noch Daten verarbeiten kann, schlagen weitere Aufrufe von [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) fehl.</span><span class="sxs-lookup"><span data-stu-id="7174e-113">As long as the MFT still has data to process, further calls to [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) will fail.</span></span> <span data-ttu-id="7174e-114">Der MFT erzeugt die Ausgabe so lange, bis alle gespeicherten Daten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7174e-114">The MFT continues to produce output until it uses all stored data.</span></span> <span data-ttu-id="7174e-115">Der MFT verwirft alle Daten, die nicht verarbeitet werden können, in ein vollständiges Ausgabe Beispiel.</span><span class="sxs-lookup"><span data-stu-id="7174e-115">The MFT discards any data that cannot be processed into a complete output sample.</span></span> <span data-ttu-id="7174e-116">(Sie sollten z. b. einen Teil Videorahmen löschen.)</span><span class="sxs-lookup"><span data-stu-id="7174e-116">(For example, it should drop a partial video frame.)</span></span>

<span data-ttu-id="7174e-117">**Asynchrone MFTs**</span><span class="sxs-lookup"><span data-stu-id="7174e-117">**Asynchronous MFTs**</span></span>

1.  <span data-ttu-id="7174e-118">Der MFT sendet weiterhin [metransformhaveoutput](metransformhaveoutput.md) -Ereignisse, bis keine weiteren Daten mehr verarbeitet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="7174e-118">The MFT continues to send [METransformHaveOutput](metransformhaveoutput.md) events until it has no more data to process.</span></span> <span data-ttu-id="7174e-119">Während dieser Zeit werden keine [metransformneedinput](metransformneedinput.md) -Ereignisse gesendet.</span><span class="sxs-lookup"><span data-stu-id="7174e-119">It does not send [METransformNeedInput](metransformneedinput.md) events during this time.</span></span>
2.  <span data-ttu-id="7174e-120">Nachdem das MFT das letzte [metransformhaveoutput](metransformhaveoutput.md) -Ereignis gesendet hat, sendet es ein [metransformdraunvollständiges](metransformdraincomplete.md) Ereignis.</span><span class="sxs-lookup"><span data-stu-id="7174e-120">After the MFT sends the last [METransformHaveOutput](metransformhaveoutput.md) event, it sends an [METransformDrainComplete](metransformdraincomplete.md) event.</span></span>
3.  <span data-ttu-id="7174e-121">Nachdem das Entpacken vollständig ist, sendet der MFT kein anderes [metransformneedinput](metransformneedinput.md) -Ereignis, bis er eine Nachricht zum [**\_ \_ \_ Starten des Nachrichten Starts \_ von \_ MFT**](mft-message-notify-start-of-stream.md) vom Client empfängt.</span><span class="sxs-lookup"><span data-stu-id="7174e-121">After draining is complete, the MFT does not send another [METransformNeedInput](metransformneedinput.md) event until it receives an [**MFT\_MESSAGE\_NOTIFY\_START\_OF\_STREAM**](mft-message-notify-start-of-stream.md) message from the client.</span></span>

<span data-ttu-id="7174e-122">Nachdem der Client die MFT entladen hat, kann der Client weitere Eingabedaten senden.</span><span class="sxs-lookup"><span data-stu-id="7174e-122">After the client has drained the MFT, the client can send more input data.</span></span> <span data-ttu-id="7174e-123">Das erste Beispiel nach dem Entladen-Vorgang muss das Diskontinuität-Attribut ([**MF SampleExtension \_ Diskontinuität**](mfsampleextension-discontinuity-attribute.md) -Attribut) aufweisen.</span><span class="sxs-lookup"><span data-stu-id="7174e-123">The first sample after the drain operation must have the discontinuity attribute ([**MFSampleExtension\_Discontinuity**](mfsampleextension-discontinuity-attribute.md) attribute).</span></span>

> [!Note]  
> <span data-ttu-id="7174e-124">In früheren Versionen dieser Dokumentation wurde angegeben, dass der *ulparam* -Ereignis Parameter ein Member der Enumeration des [**\_ MFT-Ausgleichs \_ \_ Typs**](/windows/win32/api/mftransform/ne-mftransform-_mft_drain_type) ist.</span><span class="sxs-lookup"><span data-stu-id="7174e-124">Earlier versions of this documentation stated that the *ulParam* event parameter is a member of the [**\_MFT\_DRAIN\_TYPE**](/windows/win32/api/mftransform/ne-mftransform-_mft_drain_type) enumeration.</span></span> <span data-ttu-id="7174e-125">Diese Antwort ist falsch.</span><span class="sxs-lookup"><span data-stu-id="7174e-125">That is not correct.</span></span> <span data-ttu-id="7174e-126">*Ulparam* enthält einen Datenstrom Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="7174e-126">The *ulParam* contains a stream identifier.</span></span>

 

### <a name="implementation"></a><span data-ttu-id="7174e-127">Implementierung</span><span class="sxs-lookup"><span data-stu-id="7174e-127">Implementation</span></span>

<span data-ttu-id="7174e-128">Ein asynchroner MFT muss immer [metransformdraunvollzurück](metransformdraincomplete.md) geben, nachdem er entladen wurde.</span><span class="sxs-lookup"><span data-stu-id="7174e-128">An asynchronous MFT must always return [METransformDrainComplete](metransformdraincomplete.md) after it has drained.</span></span>

<span data-ttu-id="7174e-129">Eine synchrone MFT kann diese Meldung ignorieren und S OK zurückgeben, \_ Wenn die folgenden Bedingungen zutreffen:</span><span class="sxs-lookup"><span data-stu-id="7174e-129">A synchronous MFT can ignore this message and return S\_OK if the following conditions are true:</span></span>

-   <span data-ttu-id="7174e-130">Der MFT speichert niemals mehr als eine Eingabe Stichprobe.</span><span class="sxs-lookup"><span data-stu-id="7174e-130">The MFT never stores more than one input sample at a time.</span></span>
-   <span data-ttu-id="7174e-131">Jedes Eingabe Beispiel erzeugt ein einzelnes Ausgabe Beispiel.</span><span class="sxs-lookup"><span data-stu-id="7174e-131">Each input sample produces a single output sample.</span></span>

<span data-ttu-id="7174e-132">Andernfalls muss eine synchrone MFT diese Meldung implementieren.</span><span class="sxs-lookup"><span data-stu-id="7174e-132">Otherwise, a synchronous MFT must implement this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="7174e-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7174e-133">Requirements</span></span>



| <span data-ttu-id="7174e-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7174e-134">Requirement</span></span> | <span data-ttu-id="7174e-135">Wert</span><span class="sxs-lookup"><span data-stu-id="7174e-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7174e-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7174e-136">Minimum supported client</span></span><br/> | <span data-ttu-id="7174e-137">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7174e-137">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="7174e-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7174e-138">Minimum supported server</span></span><br/> | <span data-ttu-id="7174e-139">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7174e-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="7174e-140">Header</span><span class="sxs-lookup"><span data-stu-id="7174e-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="7174e-141"><dt>"MF Transform. h"</dt></span><span class="sxs-lookup"><span data-stu-id="7174e-141"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7174e-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7174e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7174e-143">**MFT \_ - \_ Nachrichtentyp**</span><span class="sxs-lookup"><span data-stu-id="7174e-143">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> <dt>

[<span data-ttu-id="7174e-144">Asynchrone MFTs</span><span class="sxs-lookup"><span data-stu-id="7174e-144">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> </dl>

 

 




