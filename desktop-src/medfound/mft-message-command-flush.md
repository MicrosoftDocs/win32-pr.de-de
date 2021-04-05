---
description: Fordert eine Media Foundation Transformation (MFT) an, um alle gespeicherten Daten zu leeren.
ms.assetid: c799a962-da79-46df-a37f-4016c8c1701e
title: MFT_MESSAGE_COMMAND_FLUSH (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd68f5e52cda9cca3470fb1dd903b5083a0cbc4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753952"
---
# <a name="mft_message_command_flush"></a><span data-ttu-id="f4db4-103">MFT- \_ Nachrichten \_ Befehls Leerung \_</span><span class="sxs-lookup"><span data-stu-id="f4db4-103">MFT\_MESSAGE\_COMMAND\_FLUSH</span></span>

<span data-ttu-id="f4db4-104">Fordert eine Media Foundation Transformation (MFT) an, um alle gespeicherten Daten zu leeren.</span><span class="sxs-lookup"><span data-stu-id="f4db4-104">Requests a Media Foundation transform (MFT) to flush all stored data.</span></span>

## <a name="message-parameter"></a><span data-ttu-id="f4db4-105">Message-Parameter</span><span class="sxs-lookup"><span data-stu-id="f4db4-105">Message Parameter</span></span>

<span data-ttu-id="f4db4-106">Keine.</span><span class="sxs-lookup"><span data-stu-id="f4db4-106">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4db4-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f4db4-107">Remarks</span></span>

<span data-ttu-id="f4db4-108">Um diese Nachricht zu senden, nennen Sie [**imftransform::P rocess Message**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span><span class="sxs-lookup"><span data-stu-id="f4db4-108">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="f4db4-109">Nachdem diese Nachricht gesendet wurde, kann die MFT neue Eingabe Beispiele akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="f4db4-109">After this message is sent, the MFT can accept new input samples.</span></span> <span data-ttu-id="f4db4-110">Die aktuellen Medientypen werden nicht für ungültig erklärt.</span><span class="sxs-lookup"><span data-stu-id="f4db4-110">The current media types are not invalidated.</span></span>

### <a name="implementation"></a><span data-ttu-id="f4db4-111">Implementierung</span><span class="sxs-lookup"><span data-stu-id="f4db4-111">Implementation</span></span>

<span data-ttu-id="f4db4-112">Diese Nachricht muss von allen MFTs implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="f4db4-112">All MFTs must implement this message.</span></span> <span data-ttu-id="f4db4-113">Wenn diese Nachricht empfangen wird, sollte der MFT alle darin enthaltenen Medien Beispiele verwerfen.</span><span class="sxs-lookup"><span data-stu-id="f4db4-113">When it receives this message, the MFT should discard any media samples it is holding.</span></span>

<span data-ttu-id="f4db4-114">[Asynchrone MFTs](asynchronous-mfts.md): der MFT sendet erst dann ein anderes [metransformneedinput](metransformneedinput.md) -Ereignis, wenn eine Nachricht zum [**\_ \_ \_ Starten \_ des Nachrichten \_ Starts**](mft-message-notify-start-of-stream.md) vom Client empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="f4db4-114">[Asynchronous MFTs](asynchronous-mfts.md): The MFT does not send another [METransformNeedInput](metransformneedinput.md) event until it receives an [**MFT\_MESSAGE\_NOTIFY\_START\_OF\_STREAM**](mft-message-notify-start-of-stream.md) message from the client.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4db4-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f4db4-115">Requirements</span></span>



| <span data-ttu-id="f4db4-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f4db4-116">Requirement</span></span> | <span data-ttu-id="f4db4-117">Wert</span><span class="sxs-lookup"><span data-stu-id="f4db4-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4db4-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f4db4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f4db4-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f4db4-119">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f4db4-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f4db4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f4db4-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f4db4-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f4db4-122">Header</span><span class="sxs-lookup"><span data-stu-id="f4db4-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4db4-123"><dt>"MF Transform. h"</dt></span><span class="sxs-lookup"><span data-stu-id="f4db4-123"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4db4-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f4db4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4db4-125">**MFT \_ - \_ Nachrichtentyp**</span><span class="sxs-lookup"><span data-stu-id="f4db4-125">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




