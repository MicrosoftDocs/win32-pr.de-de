---
description: Benachrichtigt eine Media Foundation Transform (MFT), dass das Streaming im Begriff ist.
ms.assetid: a7f02e92-a747-4ac6-aa83-60897acb2bc5
title: MFT_MESSAGE_NOTIFY_BEGIN_STREAMING (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1aa67f58c7246b50292f4b34711e0149eb8f3377
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215035"
---
# <a name="mft_message_notify_begin_streaming"></a><span data-ttu-id="09ef3-103">MFT- \_ Nachrichten \_ Benachrichtigung zum Starten des \_ \_ Streamings</span><span class="sxs-lookup"><span data-stu-id="09ef3-103">MFT\_MESSAGE\_NOTIFY\_BEGIN\_STREAMING</span></span>

<span data-ttu-id="09ef3-104">Benachrichtigt eine Media Foundation Transform (MFT), dass das Streaming im Begriff ist.</span><span class="sxs-lookup"><span data-stu-id="09ef3-104">Notifies a Media Foundation transform (MFT) that streaming is about to begin.</span></span>

## <a name="message-parameter"></a><span data-ttu-id="09ef3-105">Message-Parameter</span><span class="sxs-lookup"><span data-stu-id="09ef3-105">Message Parameter</span></span>

<span data-ttu-id="09ef3-106">Keine.</span><span class="sxs-lookup"><span data-stu-id="09ef3-106">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="09ef3-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="09ef3-107">Remarks</span></span>

<span data-ttu-id="09ef3-108">Um diese Nachricht zu senden, nennen Sie [**imftransform::P rocess Message**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span><span class="sxs-lookup"><span data-stu-id="09ef3-108">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="09ef3-109">Der Client muss diese Nachricht nicht senden.</span><span class="sxs-lookup"><span data-stu-id="09ef3-109">The client is not required to send this message.</span></span> <span data-ttu-id="09ef3-110">Wenn der Client diese Nachricht sendet, muss dies nach dem Festlegen aller Medientypen auf der MFT und vor dem Aufrufen von [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="09ef3-110">If the client sends this message, it must do so after setting all of the media types on the MFT, and before calling [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).</span></span> <span data-ttu-id="09ef3-111">Die MFT kann Antworten, indem Puffer oder andere Ressourcen zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="09ef3-111">The MFT can respond by allocating buffers or other resources.</span></span> <span data-ttu-id="09ef3-112">Wenn der Client diese Nachricht nicht sendet, ordnet der MFT beim ersten Aufrufen von **ProcessInput** Ressourcen zu.</span><span class="sxs-lookup"><span data-stu-id="09ef3-112">If the client does not send this message, the MFT allocates resources on the first call to **ProcessInput**.</span></span> <span data-ttu-id="09ef3-113">Daher kann das Senden dieser Nachricht die anfängliche Latenz verringern, wenn das Streaming beginnt.</span><span class="sxs-lookup"><span data-stu-id="09ef3-113">Therefore, sending this message can reduce the initial latency when streaming begins.</span></span>

### <a name="implementation"></a><span data-ttu-id="09ef3-114">Implementierung</span><span class="sxs-lookup"><span data-stu-id="09ef3-114">Implementation</span></span>

<span data-ttu-id="09ef3-115">Ein MFT ist nicht erforderlich, um auf diese Nachricht zu reagieren.</span><span class="sxs-lookup"><span data-stu-id="09ef3-115">An MFT is not required to respond to this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="09ef3-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="09ef3-116">Requirements</span></span>



| <span data-ttu-id="09ef3-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="09ef3-117">Requirement</span></span> | <span data-ttu-id="09ef3-118">Wert</span><span class="sxs-lookup"><span data-stu-id="09ef3-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="09ef3-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="09ef3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="09ef3-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="09ef3-120">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="09ef3-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="09ef3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="09ef3-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="09ef3-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="09ef3-123">Header</span><span class="sxs-lookup"><span data-stu-id="09ef3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="09ef3-124"><dt>"MF Transform. h"</dt></span><span class="sxs-lookup"><span data-stu-id="09ef3-124"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09ef3-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="09ef3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09ef3-126">**MFT \_ - \_ Nachrichtentyp**</span><span class="sxs-lookup"><span data-stu-id="09ef3-126">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




