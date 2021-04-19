---
description: Benachrichtigt eine Media Foundation Transformation (MFT), dass ein Eingabestream beendet wurde.
ms.assetid: 2d6cdf45-1bb4-4915-bd27-efa041089100
title: MFT_MESSAGE_NOTIFY_END_OF_STREAM (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 476781b149553bec1d48632e0621ff0a38ad8d21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360004"
---
# <a name="mft_message_notify_end_of_stream"></a><span data-ttu-id="7cc6f-103">\_ \_ \_ Ende \_ des Daten \_ Stroms für MFT-Nachricht Benachrichtigen</span><span class="sxs-lookup"><span data-stu-id="7cc6f-103">MFT\_MESSAGE\_NOTIFY\_END\_OF\_STREAM</span></span>

<span data-ttu-id="7cc6f-104">Benachrichtigt eine Media Foundation Transformation (MFT), dass ein Eingabestream beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="7cc6f-104">Notifies a Media Foundation transform (MFT) that an input stream has ended.</span></span>

## <a name="message-parameter"></a><span data-ttu-id="7cc6f-105">Message-Parameter</span><span class="sxs-lookup"><span data-stu-id="7cc6f-105">Message Parameter</span></span>

<span data-ttu-id="7cc6f-106">Der *ulparam* -Parameter enthält den Bezeichner des Eingabedaten Stroms, der als **DWORD** -Wert angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7cc6f-106">The *ulParam* parameter contains the identifier of the input stream, specified as a **DWORD** value.</span></span> <span data-ttu-id="7cc6f-107">Platzieren Sie diesen Wert in 64-Bit-Anwendungen in den unteren 32-Bits des **ulong \_ ptr**.</span><span class="sxs-lookup"><span data-stu-id="7cc6f-107">In 64-bit applications, place this value in the lower 32-bits of the **ULONG\_PTR**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7cc6f-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7cc6f-108">Remarks</span></span>

<span data-ttu-id="7cc6f-109">Um diese Nachricht zu senden, nennen Sie [**imftransform::P rocess Message**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span><span class="sxs-lookup"><span data-stu-id="7cc6f-109">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="7cc6f-110">Der Client muss diese Nachricht nicht senden.</span><span class="sxs-lookup"><span data-stu-id="7cc6f-110">The client is not required to send this message.</span></span>

<span data-ttu-id="7cc6f-111">Nachdem ein Stream beendet wurde, kann der Client erneut [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) aufrufen, um neue Daten für diesen Stream zu senden.</span><span class="sxs-lookup"><span data-stu-id="7cc6f-111">After a stream ends, the client may call [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) again to send new data for that stream.</span></span> <span data-ttu-id="7cc6f-112">Wenn dies der Fall ist, muss der Client das Diskontinuität-Attribut ([**mfsampleextension \_ Diskontinuität**](mfsampleextension-discontinuity-attribute.md) -Attribut) für das erste Eingabe Beispiel festlegen, nachdem der Stream beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="7cc6f-112">If so, the client must set the discontinuity attribute ([**MFSampleExtension\_Discontinuity**](mfsampleextension-discontinuity-attribute.md) attribute) on the first input sample after the stream ends.</span></span> <span data-ttu-id="7cc6f-113">(Der Client sollte dieses Attribut immer auf dem ersten neuen Beispiel festlegen, nachdem ein Stream beendet wurde, unabhängig davon, ob der Client die Nachricht zum **\_ \_ \_ Ende \_ der \_ Nachricht zum Nachrichten Ende der MFT-Nachricht** gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="7cc6f-113">(The client should always set this attribute on the first new sample after a stream ends, regardless of whether the client sent the **MFT\_MESSAGE\_NOTIFY\_END\_OF\_STREAM** message.</span></span> <span data-ttu-id="7cc6f-114">Weitere Informationen zur Behandlung von Diskontinuitäten finden Sie unter [Grundlegendes MFT-Verarbeitungsmodell](basic-mft-processing-model.md).)</span><span class="sxs-lookup"><span data-stu-id="7cc6f-114">For more information about handling discontinuities, see [Basic MFT Processing Model](basic-mft-processing-model.md).)</span></span>

<span data-ttu-id="7cc6f-115">Nachdem diese Nachricht für jeden Eingabestream gesendet wurde, sendet der Client in der Regel einen Befehl zum **leeren der MFT- \_ Nachrichten \_ Befehle \_** und sammelt dann die verbleibende Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="7cc6f-115">After sending this message for every input stream, the client typically sends an **MFT\_MESSAGE\_COMMAND\_DRAIN** command and then collects the remaining output.</span></span> <span data-ttu-id="7cc6f-116">Der Client muss die MFT jedoch nicht entladen.</span><span class="sxs-lookup"><span data-stu-id="7cc6f-116">However, the client is not required to drain the MFT.</span></span> <span data-ttu-id="7cc6f-117">Wenn der Client die MFT nicht abschließt, werden vom MFT in der Regel alle nicht verarbeiteten Daten beim nächsten Aufrufen von [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)verworfen, wenn die Datenstrom Diskontinuität erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="7cc6f-117">If the client does not drain the MFT, the MFT will typically discard any unprocessed data on the next call to [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput), when it detects the stream discontinuity.</span></span> <span data-ttu-id="7cc6f-118">Alternativ kann der Client die MFT leeren, bevor **ProcessInput** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="7cc6f-118">Alternatively, the client might flush the MFT before calling **ProcessInput**.</span></span>

<span data-ttu-id="7cc6f-119">Diese Meldung entfernt den Eingabestream nicht oder setzt den Medientyp zurück.</span><span class="sxs-lookup"><span data-stu-id="7cc6f-119">This message does not remove the input stream or reset the media type.</span></span>

### <a name="implementation"></a><span data-ttu-id="7cc6f-120">Implementierung</span><span class="sxs-lookup"><span data-stu-id="7cc6f-120">Implementation</span></span>

<span data-ttu-id="7cc6f-121">Ein MFT ist nicht erforderlich, um auf diese Nachricht zu reagieren.</span><span class="sxs-lookup"><span data-stu-id="7cc6f-121">An MFT is not required to respond to this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="7cc6f-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7cc6f-122">Requirements</span></span>



| <span data-ttu-id="7cc6f-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7cc6f-123">Requirement</span></span> | <span data-ttu-id="7cc6f-124">Wert</span><span class="sxs-lookup"><span data-stu-id="7cc6f-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cc6f-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7cc6f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="7cc6f-126">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7cc6f-126">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="7cc6f-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7cc6f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="7cc6f-128">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7cc6f-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="7cc6f-129">Header</span><span class="sxs-lookup"><span data-stu-id="7cc6f-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="7cc6f-130"><dt>"MF Transform. h"</dt></span><span class="sxs-lookup"><span data-stu-id="7cc6f-130"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7cc6f-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7cc6f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cc6f-132">**MFT \_ - \_ Nachrichtentyp**</span><span class="sxs-lookup"><span data-stu-id="7cc6f-132">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




