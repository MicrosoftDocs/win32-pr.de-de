---
description: Fordert eine Media Foundation Transformation (MFT) an, um das Streaming zu beenden.
ms.assetid: df313a66-e80f-499c-a9f2-a7cbaaf0a7d4
title: MFT_MESSAGE_NOTIFY_END_STREAMING (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad2f13635b97db0c6d7751d9648f42b2b4ed8acc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527914"
---
# <a name="mft_message_notify_end_streaming"></a><span data-ttu-id="878cd-103">MFT- \_ Nachrichten Nachrichten \_ Ende- \_ \_ Streaming</span><span class="sxs-lookup"><span data-stu-id="878cd-103">MFT\_MESSAGE\_NOTIFY\_END\_STREAMING</span></span>

<span data-ttu-id="878cd-104">Fordert eine Media Foundation Transformation (MFT) an, um das Streaming zu beenden.</span><span class="sxs-lookup"><span data-stu-id="878cd-104">Requests a Media Foundation transform (MFT) to that streaming is about to end.</span></span>

## <a name="message-parameter"></a><span data-ttu-id="878cd-105">Message-Parameter</span><span class="sxs-lookup"><span data-stu-id="878cd-105">Message Parameter</span></span>

<span data-ttu-id="878cd-106">Keine.</span><span class="sxs-lookup"><span data-stu-id="878cd-106">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="878cd-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="878cd-107">Remarks</span></span>

<span data-ttu-id="878cd-108">Um diese Nachricht zu senden, nennen Sie [**imftransform::P rocess Message**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span><span class="sxs-lookup"><span data-stu-id="878cd-108">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="878cd-109">Der Client ist nicht verpflichtet, diese Nachricht zu senden, auch wenn der Client die Meldung zum Starten des Nachrichten Nachrichten dienstanterings zuvor gesendet hat. **\_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="878cd-109">The client is not required to send this message, even if the client previously sent the **MFT\_MESSAGE\_NOTIFY\_BEGIN\_STREAMING** message.</span></span>

### <a name="implementation"></a><span data-ttu-id="878cd-110">Implementierung</span><span class="sxs-lookup"><span data-stu-id="878cd-110">Implementation</span></span>

<span data-ttu-id="878cd-111">Die MFT kann auf diese Nachricht reagieren, indem Puffer und andere Ressourcen freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="878cd-111">The MFT can respond to this message by releasing buffers and other resources.</span></span> <span data-ttu-id="878cd-112">Die MFT leert keine Eingabedaten oder setzt die Medientypen als Reaktion auf diese Nachricht zurück.</span><span class="sxs-lookup"><span data-stu-id="878cd-112">The MFT does not flush input data or reset the media types in response to this message.</span></span> <span data-ttu-id="878cd-113">Ein MFT ist nicht erforderlich, um auf diese Nachricht zu reagieren.</span><span class="sxs-lookup"><span data-stu-id="878cd-113">An MFT is not required to respond to this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="878cd-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="878cd-114">Requirements</span></span>



| <span data-ttu-id="878cd-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="878cd-115">Requirement</span></span> | <span data-ttu-id="878cd-116">Wert</span><span class="sxs-lookup"><span data-stu-id="878cd-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="878cd-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="878cd-117">Minimum supported client</span></span><br/> | <span data-ttu-id="878cd-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="878cd-118">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="878cd-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="878cd-119">Minimum supported server</span></span><br/> | <span data-ttu-id="878cd-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="878cd-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="878cd-121">Header</span><span class="sxs-lookup"><span data-stu-id="878cd-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="878cd-122"><dt>"MF Transform. h"</dt></span><span class="sxs-lookup"><span data-stu-id="878cd-122"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="878cd-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="878cd-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="878cd-124">**MFT \_ - \_ Nachrichtentyp**</span><span class="sxs-lookup"><span data-stu-id="878cd-124">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




