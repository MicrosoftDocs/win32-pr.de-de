---
description: Ermöglicht es dem Quell Leser, Media Foundation Transformationen (MFTs) zu verwenden, die für die Transcodierung optimiert sind.
ms.assetid: 9463EB8C-2CA3-4F8F-8A2A-B1292879DD1B
title: MF_SOURCE_READER_ENABLE_TRANSCODE_ONLY_TRANSFORMS-Attribut (mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04a9559254216a102613d97824601c004c71bfd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525991"
---
# <a name="mf_source_reader_enable_transcode_only_transforms-attribute"></a><span data-ttu-id="16420-103">MF- \_ Quell \_ Leser Aktivieren von \_ \_ transcode \_ only- \_ Attribut Transformationen</span><span class="sxs-lookup"><span data-stu-id="16420-103">MF\_SOURCE\_READER\_ENABLE\_TRANSCODE\_ONLY\_TRANSFORMS attribute</span></span>

<span data-ttu-id="16420-104">Ermöglicht es dem [Quell Leser](source-reader.md) , Media Foundation Transformationen (MFTs) zu verwenden, die für die Transcodierung optimiert sind.</span><span class="sxs-lookup"><span data-stu-id="16420-104">Enables the [Source Reader](source-reader.md) to use Media Foundation transforms (MFTs) that are optimized for transcoding.</span></span>

## <a name="data-type"></a><span data-ttu-id="16420-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="16420-105">Data type</span></span>

<span data-ttu-id="16420-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="16420-106">**UINT32**</span></span>

<span data-ttu-id="16420-107">Als booleschen Wert behandeln.</span><span class="sxs-lookup"><span data-stu-id="16420-107">Treat as Boolean.</span></span>

## <a name="remarks"></a><span data-ttu-id="16420-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="16420-108">Remarks</span></span>

<span data-ttu-id="16420-109">Einige MFTs, insbesondere Decoder, sind für die Transcodierung und nicht für die Wiedergabe optimiert.</span><span class="sxs-lookup"><span data-stu-id="16420-109">Some MFTs, particularly decoders, are optimized for transcoding rather than playback.</span></span> <span data-ttu-id="16420-110">Standardmäßig lädt der Quell Leser diese Transformationen nicht.</span><span class="sxs-lookup"><span data-stu-id="16420-110">By default, the Source Reader will not load such transforms.</span></span> <span data-ttu-id="16420-111">Legen Sie dieses Attribut auf " **true** " fest, wenn Sie Transcodierung-MFTs mit dem Quell Leser verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="16420-111">Set this attribute to **TRUE** if you want to use transcoding MFTs with the Source Reader.</span></span>

<span data-ttu-id="16420-112">Eine Anwendung kann dieses Attribut festlegen, wenn Sie die Daten nicht in Echtzeit verarbeitet (für die Transcodierung oder ähnliche Szenarien).</span><span class="sxs-lookup"><span data-stu-id="16420-112">An application might set this attribute if it does not process the data in real time (for transcoding or similar scenarios).</span></span> <span data-ttu-id="16420-113">Verwenden Sie andernfalls für die Echt Zeit Wiedergabe das Standardverhalten.</span><span class="sxs-lookup"><span data-stu-id="16420-113">Otherwise, for real-time playback, use the default behavior.</span></span>

<span data-ttu-id="16420-114">Intern bewirkt dieses Attribut, dass der Quell Leser beim Aufrufen von [**mftenumex**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)das Flag **\_ \_ \_ transcode \_ only für das MFT-Enum-Flag** einschließt.</span><span class="sxs-lookup"><span data-stu-id="16420-114">Internally, this attribute causes the Source Reader to include the **MFT\_ENUM\_FLAG\_TRANSCODE\_ONLY** flag when it calls [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span></span>

## <a name="requirements"></a><span data-ttu-id="16420-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="16420-115">Requirements</span></span>



| <span data-ttu-id="16420-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="16420-116">Requirement</span></span> | <span data-ttu-id="16420-117">Wert</span><span class="sxs-lookup"><span data-stu-id="16420-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="16420-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="16420-118">Minimum supported client</span></span><br/> | <span data-ttu-id="16420-119">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="16420-119">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="16420-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="16420-120">Minimum supported server</span></span><br/> | <span data-ttu-id="16420-121">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="16420-121">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="16420-122">Header</span><span class="sxs-lookup"><span data-stu-id="16420-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="16420-123"><dt>"Mfreadwrite. h"</dt></span><span class="sxs-lookup"><span data-stu-id="16420-123"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16420-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="16420-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16420-125">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="16420-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="16420-126">Quell Leser</span><span class="sxs-lookup"><span data-stu-id="16420-126">Source Reader</span></span>](source-reader.md)
</dt> </dl>

 

 




