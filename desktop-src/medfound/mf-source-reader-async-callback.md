---
description: Enthält einen Zeiger auf die Anwendungs Rückruf Schnittstelle für den Quell Reader.
ms.assetid: de226a5a-03c0-4bfe-bb20-8969ce43cf53
title: MF_SOURCE_READER_ASYNC_CALLBACK-Attribut (mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66542a155fbb6fa3e56958733626b1d0b750ab9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216876"
---
# <a name="mf_source_reader_async_callback-attribute"></a><span data-ttu-id="c4264-103">\_ \_ \_ Async- \_ Rückruf Attribut des MF-Quell Readers</span><span class="sxs-lookup"><span data-stu-id="c4264-103">MF\_SOURCE\_READER\_ASYNC\_CALLBACK attribute</span></span>

<span data-ttu-id="c4264-104">Enthält einen Zeiger auf die Rückruf Schnittstelle der Anwendung für den [Quell Reader](source-reader.md).</span><span class="sxs-lookup"><span data-stu-id="c4264-104">Contains a pointer to the application's callback interface for the [Source Reader](source-reader.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="c4264-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="c4264-105">Data type</span></span>

<span data-ttu-id="c4264-106">**IMF sourcereadercallback \** _ als " _*IUnknown \*\* " gespeichert_</span><span class="sxs-lookup"><span data-stu-id="c4264-106">**IMFSourceReaderCallback\** _ stored as _*IUnknown\*\*_</span></span>

## <a name="getset"></a><span data-ttu-id="c4264-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="c4264-107">Get/set</span></span>

<span data-ttu-id="c4264-108">Um dieses Attribut abzurufen, nennen Sie [_ *imfattributes:: getunknown* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="c4264-108">To get this attribute, call [_ *IMFAttributes::GetUnknown*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="c4264-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="c4264-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="c4264-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c4264-110">Remarks</span></span>

<span data-ttu-id="c4264-111">Der Wert dieses Attributs ist ein Zeiger auf die [**imfsourcereadercallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback) -Schnittstelle der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="c4264-111">The value of this attribute is a pointer to the application's [**IMFSourceReaderCallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback) interface.</span></span>

<span data-ttu-id="c4264-112">Verwenden Sie dieses Attribut mit den folgenden Funktionen:</span><span class="sxs-lookup"><span data-stu-id="c4264-112">Use this attribute with the following functions:</span></span>

-   [<span data-ttu-id="c4264-113">**MF | atesourcereaderfromb-testream**</span><span class="sxs-lookup"><span data-stu-id="c4264-113">**MFCreateSourceReaderFromByteStream**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [<span data-ttu-id="c4264-114">**Mfkreatesourcereaderfrommediasource**</span><span class="sxs-lookup"><span data-stu-id="c4264-114">**MFCreateSourceReaderFromMediaSource**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [<span data-ttu-id="c4264-115">**MF | atesourcereaderfromurl**</span><span class="sxs-lookup"><span data-stu-id="c4264-115">**MFCreateSourceReaderFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)

## <a name="requirements"></a><span data-ttu-id="c4264-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c4264-116">Requirements</span></span>



| <span data-ttu-id="c4264-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c4264-117">Requirement</span></span> | <span data-ttu-id="c4264-118">Wert</span><span class="sxs-lookup"><span data-stu-id="c4264-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4264-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c4264-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c4264-120">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="c4264-120">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="c4264-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c4264-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c4264-122">Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="c4264-122">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="c4264-123">Header</span><span class="sxs-lookup"><span data-stu-id="c4264-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4264-124"><dt>"Mfreadwrite. h"</dt></span><span class="sxs-lookup"><span data-stu-id="c4264-124"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4264-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c4264-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4264-126">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="c4264-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c4264-127">Quell Leser</span><span class="sxs-lookup"><span data-stu-id="c4264-127">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="c4264-128">Attribute des Quell Readers</span><span class="sxs-lookup"><span data-stu-id="c4264-128">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




