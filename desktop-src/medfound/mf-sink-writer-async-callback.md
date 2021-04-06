---
description: Enthält einen Zeiger auf die Anwendungs Rückruf Schnittstelle für den Senke-Writer.
ms.assetid: 22df1fa0-469d-4501-aaf0-a0379b7ed096
title: MF_SINK_WRITER_ASYNC_CALLBACK-Attribut (mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f11bed051df9107ca3a2247b6c3d0cf2058224c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759570"
---
# <a name="mf_sink_writer_async_callback-attribute"></a><span data-ttu-id="0efac-103">\_ \_ \_ Async- \_ Rückruf Attribut für das MF-Sink-Writer</span><span class="sxs-lookup"><span data-stu-id="0efac-103">MF\_SINK\_WRITER\_ASYNC\_CALLBACK attribute</span></span>

<span data-ttu-id="0efac-104">Enthält einen Zeiger auf die Rückruf Schnittstelle der Anwendung für den Senke-Writer.</span><span class="sxs-lookup"><span data-stu-id="0efac-104">Contains a pointer to the application's callback interface for the sink writer.</span></span>

## <a name="data-type"></a><span data-ttu-id="0efac-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="0efac-105">Data type</span></span>

<span data-ttu-id="0efac-106">**[**Imbsinkschreiterrückruf**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback) \** _ als " _*IUnknown \*\* " gespeichert_</span><span class="sxs-lookup"><span data-stu-id="0efac-106">**[**IMFSinkWriterCallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback)\** _ stored as _*IUnknown\*\*_</span></span>

## <a name="getset"></a><span data-ttu-id="0efac-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="0efac-107">Get/set</span></span>

<span data-ttu-id="0efac-108">Um dieses Attribut abzurufen, nennen Sie [_ *imfattributes:: getunknown* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="0efac-108">To get this attribute, call [_ *IMFAttributes::GetUnknown*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="0efac-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="0efac-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="0efac-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0efac-110">Remarks</span></span>

<span data-ttu-id="0efac-111">Der Wert dieses Attributs ist ein Zeiger auf die [**imfsinkschreitercallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback) -Schnittstelle der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="0efac-111">The value of this attribute is a pointer to the application's [**IMFSinkWriterCallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback) interface.</span></span>

<span data-ttu-id="0efac-112">Verwenden Sie dieses Attribut mit den folgenden Funktionen:</span><span class="sxs-lookup"><span data-stu-id="0efac-112">Use this attribute with the following functions:</span></span>

-   [<span data-ttu-id="0efac-113">**Mfkreatesinkschreiterfrommediasink**</span><span class="sxs-lookup"><span data-stu-id="0efac-113">**MFCreateSinkWriterFromMediaSink**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [<span data-ttu-id="0efac-114">**MF | atesinkschreiterfromurl**</span><span class="sxs-lookup"><span data-stu-id="0efac-114">**MFCreateSinkWriterFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

## <a name="requirements"></a><span data-ttu-id="0efac-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0efac-115">Requirements</span></span>



| <span data-ttu-id="0efac-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0efac-116">Requirement</span></span> | <span data-ttu-id="0efac-117">Wert</span><span class="sxs-lookup"><span data-stu-id="0efac-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0efac-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0efac-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0efac-119">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="0efac-119">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="0efac-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0efac-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0efac-121">Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="0efac-121">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="0efac-122">Header</span><span class="sxs-lookup"><span data-stu-id="0efac-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0efac-123"><dt>"Mfreadwrite. h"</dt></span><span class="sxs-lookup"><span data-stu-id="0efac-123"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0efac-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0efac-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0efac-125">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="0efac-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0efac-126">Senkenwriter-Attribute</span><span class="sxs-lookup"><span data-stu-id="0efac-126">Sink Writer Attributes</span></span>](sink-writer-attributes.md)
</dt> </dl>

 

 




