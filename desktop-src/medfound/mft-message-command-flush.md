---
description: 'MFT_MESSAGE_COMMAND_FLUSH: Fordert eine Media Foundation-Transformation (MFT) an, um alle gespeicherten Daten zu leeren.'
ms.assetid: c799a962-da79-46df-a37f-4016c8c1701e
title: MFT_MESSAGE_COMMAND_FLUSH (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f34959303a2835e67202256341b0f5998b63d16b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092738"
---
# <a name="mft_message_command_flush"></a><span data-ttu-id="b2f39-103">MFT \_ MESSAGE \_ COMMAND \_ FLUSH</span><span class="sxs-lookup"><span data-stu-id="b2f39-103">MFT\_MESSAGE\_COMMAND\_FLUSH</span></span>

<span data-ttu-id="b2f39-104">Fordert eine Media Foundation-Transformation (MFT) an, um alle gespeicherten Daten zu leeren.</span><span class="sxs-lookup"><span data-stu-id="b2f39-104">Requests a Media Foundation transform (MFT) to flush all stored data.</span></span>

## <a name="message-parameter"></a><span data-ttu-id="b2f39-105">Message-Parameter</span><span class="sxs-lookup"><span data-stu-id="b2f39-105">Message Parameter</span></span>

<span data-ttu-id="b2f39-106">Keine.</span><span class="sxs-lookup"><span data-stu-id="b2f39-106">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2f39-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b2f39-107">Remarks</span></span>

<span data-ttu-id="b2f39-108">Um diese Nachricht zu senden, rufen Sie [**ÜBERTRANSFORM::P rocessMessage auf.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage)</span><span class="sxs-lookup"><span data-stu-id="b2f39-108">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="b2f39-109">Nachdem diese Nachricht gesendet wurde, kann der MFT neue Eingabebeispiele akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="b2f39-109">After this message is sent, the MFT can accept new input samples.</span></span> <span data-ttu-id="b2f39-110">Die aktuellen Medientypen werden nicht ungültig.</span><span class="sxs-lookup"><span data-stu-id="b2f39-110">The current media types are not invalidated.</span></span>

### <a name="implementation"></a><span data-ttu-id="b2f39-111">Implementierung</span><span class="sxs-lookup"><span data-stu-id="b2f39-111">Implementation</span></span>

<span data-ttu-id="b2f39-112">Alle MFTs müssen diese Nachricht implementieren.</span><span class="sxs-lookup"><span data-stu-id="b2f39-112">All MFTs must implement this message.</span></span> <span data-ttu-id="b2f39-113">Wenn diese Nachricht empfangen wird, sollte der MFT alle Medienbeispiele verwerfen, die er enthält.</span><span class="sxs-lookup"><span data-stu-id="b2f39-113">When it receives this message, the MFT should discard any media samples it is holding.</span></span>

<span data-ttu-id="b2f39-114">[Asynchrone MFTs:](asynchronous-mfts.md)Der MFT sendet kein weiteres [METransformNeedInput-Ereignis,](metransformneedinput.md) bis er eine [**MFT \_ MESSAGE NOTIFY START OF \_ \_ \_ \_ STREAM-Nachricht**](mft-message-notify-start-of-stream.md) vom Client empfängt.</span><span class="sxs-lookup"><span data-stu-id="b2f39-114">[Asynchronous MFTs](asynchronous-mfts.md): The MFT does not send another [METransformNeedInput](metransformneedinput.md) event until it receives an [**MFT\_MESSAGE\_NOTIFY\_START\_OF\_STREAM**](mft-message-notify-start-of-stream.md) message from the client.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2f39-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b2f39-115">Requirements</span></span>



| <span data-ttu-id="b2f39-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b2f39-116">Requirement</span></span> | <span data-ttu-id="b2f39-117">Wert</span><span class="sxs-lookup"><span data-stu-id="b2f39-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2f39-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b2f39-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b2f39-119">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b2f39-119">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b2f39-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b2f39-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b2f39-121">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b2f39-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b2f39-122">Header</span><span class="sxs-lookup"><span data-stu-id="b2f39-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2f39-123"><dt>Mftransform.h</dt></span><span class="sxs-lookup"><span data-stu-id="b2f39-123"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2f39-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b2f39-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2f39-125">**\_MFT-NACHRICHTENTYP \_**</span><span class="sxs-lookup"><span data-stu-id="b2f39-125">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




