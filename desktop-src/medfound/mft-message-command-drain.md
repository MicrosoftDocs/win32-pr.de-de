---
description: 'MFT_MESSAGE_COMMAND_DRAIN: Fordert eine Media Foundation-Transformation (MFT) an, um alle gespeicherten Daten zu leeren.'
ms.assetid: c48f3a88-a007-4f30-ac60-9e5a8c24e1ee
title: MFT_MESSAGE_COMMAND_DRAIN (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 907bfbd888b1eccbe7336c0d8f386d3266fd8e9b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092748"
---
# <a name="mft_message_command_drain"></a><span data-ttu-id="43702-103">MFT \_ MESSAGE \_ COMMAND \_ DRAIN</span><span class="sxs-lookup"><span data-stu-id="43702-103">MFT\_MESSAGE\_COMMAND\_DRAIN</span></span>

<span data-ttu-id="43702-104">Fordert eine Media Foundation-Transformation (MFT) an, um alle gespeicherten Daten zu leeren.</span><span class="sxs-lookup"><span data-stu-id="43702-104">Requests a Media Foundation transform (MFT) to flush all stored data.</span></span>

## <a name="message-parameter"></a><span data-ttu-id="43702-105">Message-Parameter</span><span class="sxs-lookup"><span data-stu-id="43702-105">Message Parameter</span></span>

<span data-ttu-id="43702-106">Keine.</span><span class="sxs-lookup"><span data-stu-id="43702-106">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="43702-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="43702-107">Remarks</span></span>

<span data-ttu-id="43702-108">Um diese Nachricht zu senden, rufen Sie [**ÜBERTRANSFORM::P rocessMessage auf.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage)</span><span class="sxs-lookup"><span data-stu-id="43702-108">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="43702-109">Nachdem diese Nachricht gesendet wurde, akzeptiert der angegebene Eingabestream keine Eingaben, bis der MFT alle Daten aus vorherigen Aufrufen von [**ÜBERTRANSFORM::P rocessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="43702-109">After this message is sent, the specified input stream does not accept input until the MFT processes all data from previous calls to [**IMFTransform::ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).</span></span>

<span data-ttu-id="43702-110">Der Ausgleichsprozess variiert geringfügig zwischen synchronen und asynchronen MFTs:</span><span class="sxs-lookup"><span data-stu-id="43702-110">The draining process varies slightly between synchronous MFTs and asynchronous MFTs:</span></span>

<span data-ttu-id="43702-111">**Synchrone MFTs**</span><span class="sxs-lookup"><span data-stu-id="43702-111">**Synchronous MFTs**</span></span>

1.  <span data-ttu-id="43702-112">Nachdem der Client diese Nachricht gesendet hat, ruft er [**ÜBERTRANSFORM::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) in einer Schleife auf, bis **ProcessOutput** den Fehlercode **MF E TRANSFORM NEED MORE \_ \_ \_ \_ \_ INPUT** zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="43702-112">After the client sends this message, it calls [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) in a loop, until **ProcessOutput** returns the error code **MF\_E\_TRANSFORM\_NEED\_MORE\_INPUT**.</span></span>
2.  <span data-ttu-id="43702-113">Solange der MFT noch über zu verarbeitende Daten verfügt, schlagen weitere Aufrufe von [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) fehl.</span><span class="sxs-lookup"><span data-stu-id="43702-113">As long as the MFT still has data to process, further calls to [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) will fail.</span></span> <span data-ttu-id="43702-114">Der MFT erzeugt weiterhin Eine Ausgabe, bis alle gespeicherten Daten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="43702-114">The MFT continues to produce output until it uses all stored data.</span></span> <span data-ttu-id="43702-115">Der MFT verwirft alle Daten, die nicht in einem vollständigen Ausgabebeispiel verarbeitet werden können.</span><span class="sxs-lookup"><span data-stu-id="43702-115">The MFT discards any data that cannot be processed into a complete output sample.</span></span> <span data-ttu-id="43702-116">(Es sollte z. B. ein Teilvideorahmen fallen.)</span><span class="sxs-lookup"><span data-stu-id="43702-116">(For example, it should drop a partial video frame.)</span></span>

<span data-ttu-id="43702-117">**Asynchrone MFTs**</span><span class="sxs-lookup"><span data-stu-id="43702-117">**Asynchronous MFTs**</span></span>

1.  <span data-ttu-id="43702-118">Der MFT sendet weiterhin [METransformHaveOutput-Ereignisse,](metransformhaveoutput.md) bis keine daten mehr verarbeitet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="43702-118">The MFT continues to send [METransformHaveOutput](metransformhaveoutput.md) events until it has no more data to process.</span></span> <span data-ttu-id="43702-119">Während dieser Zeit werden keine [METransformNeedInput-Ereignisse](metransformneedinput.md) gesendet.</span><span class="sxs-lookup"><span data-stu-id="43702-119">It does not send [METransformNeedInput](metransformneedinput.md) events during this time.</span></span>
2.  <span data-ttu-id="43702-120">Nachdem der MFT das letzte [METransformHaveOutput-Ereignis](metransformhaveoutput.md) gesendet hat, sendet er ein [METransformDrainComplete-Ereignis.](metransformdraincomplete.md)</span><span class="sxs-lookup"><span data-stu-id="43702-120">After the MFT sends the last [METransformHaveOutput](metransformhaveoutput.md) event, it sends an [METransformDrainComplete](metransformdraincomplete.md) event.</span></span>
3.  <span data-ttu-id="43702-121">Nach Abschluss der Entleerung sendet der MFT erst dann ein weiteres [METransformNeedInput-Ereignis,](metransformneedinput.md) wenn er eine [**MFT \_ MESSAGE NOTIFY START OF \_ \_ \_ \_ STREAM-Nachricht**](mft-message-notify-start-of-stream.md) vom Client empfängt.</span><span class="sxs-lookup"><span data-stu-id="43702-121">After draining is complete, the MFT does not send another [METransformNeedInput](metransformneedinput.md) event until it receives an [**MFT\_MESSAGE\_NOTIFY\_START\_OF\_STREAM**](mft-message-notify-start-of-stream.md) message from the client.</span></span>

<span data-ttu-id="43702-122">Nachdem der Client den MFT entladen hat, kann der Client weitere Eingabedaten senden.</span><span class="sxs-lookup"><span data-stu-id="43702-122">After the client has drained the MFT, the client can send more input data.</span></span> <span data-ttu-id="43702-123">Das erste Beispiel nach dem Entleerungsvorgang muss über das Diskontinuitätsattribut ([**MFSampleExtension \_ Discontinuity-Attribut)**](mfsampleextension-discontinuity-attribute.md) verfügen.</span><span class="sxs-lookup"><span data-stu-id="43702-123">The first sample after the drain operation must have the discontinuity attribute ([**MFSampleExtension\_Discontinuity**](mfsampleextension-discontinuity-attribute.md) attribute).</span></span>

> [!Note]  
> <span data-ttu-id="43702-124">In früheren Versionen dieser Dokumentation wurde angegeben, dass *der ulParam-Ereignisparameter* ein Member der [**\_ MFT \_ DRAIN \_ TYPE-Enumeration**](/windows/win32/api/mftransform/ne-mftransform-_mft_drain_type) ist.</span><span class="sxs-lookup"><span data-stu-id="43702-124">Earlier versions of this documentation stated that the *ulParam* event parameter is a member of the [**\_MFT\_DRAIN\_TYPE**](/windows/win32/api/mftransform/ne-mftransform-_mft_drain_type) enumeration.</span></span> <span data-ttu-id="43702-125">Diese Antwort ist falsch.</span><span class="sxs-lookup"><span data-stu-id="43702-125">That is not correct.</span></span> <span data-ttu-id="43702-126">*UlParam enthält* einen Streambezeichner.</span><span class="sxs-lookup"><span data-stu-id="43702-126">The *ulParam* contains a stream identifier.</span></span>

 

### <a name="implementation"></a><span data-ttu-id="43702-127">Implementierung</span><span class="sxs-lookup"><span data-stu-id="43702-127">Implementation</span></span>

<span data-ttu-id="43702-128">Ein asynchrones MFT muss nach dem [Entleeren immer METransformDgreifComplete](metransformdraincomplete.md) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="43702-128">An asynchronous MFT must always return [METransformDrainComplete](metransformdraincomplete.md) after it has drained.</span></span>

<span data-ttu-id="43702-129">Ein synchroner MFT kann diese Meldung ignorieren und S \_ OK zurückgeben, wenn die folgenden Bedingungen erfüllt sind:</span><span class="sxs-lookup"><span data-stu-id="43702-129">A synchronous MFT can ignore this message and return S\_OK if the following conditions are true:</span></span>

-   <span data-ttu-id="43702-130">MFT speichert nie mehr als ein Eingabebeispiel gleichzeitig.</span><span class="sxs-lookup"><span data-stu-id="43702-130">The MFT never stores more than one input sample at a time.</span></span>
-   <span data-ttu-id="43702-131">Jedes Eingabebeispiel erzeugt ein einzelnes Ausgabebeispiel.</span><span class="sxs-lookup"><span data-stu-id="43702-131">Each input sample produces a single output sample.</span></span>

<span data-ttu-id="43702-132">Andernfalls muss eine synchrone MFT diese Meldung implementieren.</span><span class="sxs-lookup"><span data-stu-id="43702-132">Otherwise, a synchronous MFT must implement this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="43702-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="43702-133">Requirements</span></span>



| <span data-ttu-id="43702-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="43702-134">Requirement</span></span> | <span data-ttu-id="43702-135">Wert</span><span class="sxs-lookup"><span data-stu-id="43702-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="43702-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="43702-136">Minimum supported client</span></span><br/> | <span data-ttu-id="43702-137">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="43702-137">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="43702-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="43702-138">Minimum supported server</span></span><br/> | <span data-ttu-id="43702-139">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="43702-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="43702-140">Header</span><span class="sxs-lookup"><span data-stu-id="43702-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="43702-141"><dt>Mftransform.h</dt></span><span class="sxs-lookup"><span data-stu-id="43702-141"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43702-142">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="43702-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43702-143">**\_MFT-NACHRICHTENTYP \_**</span><span class="sxs-lookup"><span data-stu-id="43702-143">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> <dt>

[<span data-ttu-id="43702-144">Asynchrone MFTs</span><span class="sxs-lookup"><span data-stu-id="43702-144">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> </dl>

 

 




