---
description: Benachrichtigt eine Media Foundation Transformation (MFT), dass das erste Beispiel gerade verarbeitet wird.
ms.assetid: 579df695-02c4-4332-b1b4-c7bd9da50c0f
title: MFT_MESSAGE_NOTIFY_START_OF_STREAM (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe0edefdecdf75afbe14c851f33e9726400e490d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041909"
---
# <a name="mft_message_notify_start_of_stream"></a><span data-ttu-id="8eec5-103">\_Nachrichten \_ \_ Anfang \_ für \_ MFT-Nachricht Benachrichtigen</span><span class="sxs-lookup"><span data-stu-id="8eec5-103">MFT\_MESSAGE\_NOTIFY\_START\_OF\_STREAM</span></span>

<span data-ttu-id="8eec5-104">Benachrichtigt eine Media Foundation Transformation (MFT), dass das erste Beispiel gerade verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="8eec5-104">Notifies a Media Foundation transform (MFT) that the first sample is about to be processed.</span></span>

## <a name="message-parameter"></a><span data-ttu-id="8eec5-105">Message-Parameter</span><span class="sxs-lookup"><span data-stu-id="8eec5-105">Message Parameter</span></span>

<span data-ttu-id="8eec5-106">Keine.</span><span class="sxs-lookup"><span data-stu-id="8eec5-106">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="8eec5-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8eec5-107">Remarks</span></span>

<span data-ttu-id="8eec5-108">Um diese Nachricht zu senden, nennen Sie [**imftransform::P rocess Message**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span><span class="sxs-lookup"><span data-stu-id="8eec5-108">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="8eec5-109">Bei synchronen MFTs ist es optional, diese Nachricht zu senden.</span><span class="sxs-lookup"><span data-stu-id="8eec5-109">For synchronous MFTs, it is optional to send this message.</span></span>

<span data-ttu-id="8eec5-110">Für asynchrone MFTs muss der Client diese Nachricht senden.</span><span class="sxs-lookup"><span data-stu-id="8eec5-110">For asynchronous MFTs, the client must send this message.</span></span>

### <a name="implementation"></a><span data-ttu-id="8eec5-111">Implementierung</span><span class="sxs-lookup"><span data-stu-id="8eec5-111">Implementation</span></span>

<span data-ttu-id="8eec5-112">Eine synchrone MFT ist nicht erforderlich, um auf die Meldung zu reagieren.</span><span class="sxs-lookup"><span data-stu-id="8eec5-112">A synchronous MFT is not required to respond to the message.</span></span>

<span data-ttu-id="8eec5-113">Diese Nachricht muss von einem asynchronen MFT implementiert werden, wie in [asynchronen MFTs](asynchronous-mfts.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="8eec5-113">An asynchronous MFT must implement this message, as described in [Asynchronous MFTs](asynchronous-mfts.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8eec5-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8eec5-114">Requirements</span></span>



| <span data-ttu-id="8eec5-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8eec5-115">Requirement</span></span> | <span data-ttu-id="8eec5-116">Wert</span><span class="sxs-lookup"><span data-stu-id="8eec5-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8eec5-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8eec5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8eec5-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8eec5-118">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="8eec5-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8eec5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8eec5-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8eec5-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8eec5-121">Header</span><span class="sxs-lookup"><span data-stu-id="8eec5-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8eec5-122"><dt>"MF Transform. h"</dt></span><span class="sxs-lookup"><span data-stu-id="8eec5-122"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8eec5-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8eec5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8eec5-124">**MFT \_ - \_ Nachrichtentyp**</span><span class="sxs-lookup"><span data-stu-id="8eec5-124">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




