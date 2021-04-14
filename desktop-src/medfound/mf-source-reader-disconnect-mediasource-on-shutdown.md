---
description: Gibt an, ob der Quell Leser die Medienquelle herunterfährt.
ms.assetid: c85f5994-8005-48c9-8a05-0316f48f4142
title: MF_SOURCE_READER_DISCONNECT_MEDIASOURCE_ON_SHUTDOWN-Attribut (mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7a9474e7fb19bb6531baf31a97238bbe6b10e46
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351718"
---
# <a name="mf_source_reader_disconnect_mediasource_on_shutdown-attribute"></a><span data-ttu-id="7a9fa-103">Der MF- \_ Quell \_ Leser \_ trennt \_ MediaSource \_ beim \_ Shutdown-Attribut.</span><span class="sxs-lookup"><span data-stu-id="7a9fa-103">MF\_SOURCE\_READER\_DISCONNECT\_MEDIASOURCE\_ON\_SHUTDOWN attribute</span></span>

<span data-ttu-id="7a9fa-104">Gibt an, ob der [Quell Leser](source-reader.md) die Medienquelle herunterfährt.</span><span class="sxs-lookup"><span data-stu-id="7a9fa-104">Specifies whether the [Source Reader](source-reader.md) shuts down the media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="7a9fa-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="7a9fa-105">Data type</span></span>

<span data-ttu-id="7a9fa-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="7a9fa-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="7a9fa-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="7a9fa-107">Get/set</span></span>

<span data-ttu-id="7a9fa-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="7a9fa-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="7a9fa-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="7a9fa-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="7a9fa-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7a9fa-110">Remarks</span></span>

<span data-ttu-id="7a9fa-111">Dieses Attribut gilt nur, wenn die Anwendung den Quell Leser aus einem vorhandenen Medien Quell Objekt erstellt, indem Sie entweder [**mfcreatesourcereaderfrommediasource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource) aufrufen oder [**imfreadschreiteclassfactory:: createinstancefromuject**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromobject)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7a9fa-111">This attribute applies only when the application creates the source reader from an existing media source object, either by calling [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource) or by calling [**IMFReadWriteClassFactory::CreateInstanceFromObject**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromobject).</span></span>

<span data-ttu-id="7a9fa-112">Wenn die Anwendung den Quell Leser freigibt, fährt der Quell Leser standardmäßig die Medienquelle durch Aufrufen von [**imfmediasource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) für die Medienquelle herunter.</span><span class="sxs-lookup"><span data-stu-id="7a9fa-112">By default, when the application releases the source reader, the source reader shuts down the media source by calling [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) on the media source.</span></span> <span data-ttu-id="7a9fa-113">An diesem Punkt kann die Anwendung die Medienquelle nicht mehr verwenden.</span><span class="sxs-lookup"><span data-stu-id="7a9fa-113">At that point, the application can no longer use the media source.</span></span>

<span data-ttu-id="7a9fa-114">Wenn der MF- \_ Quell \_ Leser \_ \_ MediaSource \_ beim Shutdown-Attribut jedoch auf \_ **true** trennt, wird die Medienquelle vom Quell Leser nicht heruntergefahren.</span><span class="sxs-lookup"><span data-stu-id="7a9fa-114">However, if the MF\_SOURCE\_READER\_DISCONNECT\_MEDIASOURCE\_ON\_SHUTDOWN attribute is **TRUE**, the source reader does not shut down the media source.</span></span> <span data-ttu-id="7a9fa-115">Dies bedeutet, dass die Anwendung nach der Veröffentlichung des Quell Readers die Medienquelle weiterhin verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="7a9fa-115">That means the application can still use the media source after the application releases the source reader.</span></span> <span data-ttu-id="7a9fa-116">Dies bedeutet auch, dass die Anwendung für das Aufrufen von [**imfmediasource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) für die Medienquelle zuständig ist.</span><span class="sxs-lookup"><span data-stu-id="7a9fa-116">It also means the application is responsible for calling [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) on the media source.</span></span>

<span data-ttu-id="7a9fa-117">Wenn die Anwendung den Quell Leser aus einer URL oder einem Bytestream erstellt, fährt der Quell Leser die Medienquelle immer herunter.</span><span class="sxs-lookup"><span data-stu-id="7a9fa-117">If the application creates the source reader from a URL or from a byte stream, the source reader always shuts down the media source.</span></span> <span data-ttu-id="7a9fa-118">In diesem Fall wird die Verbindung des MF- \_ Quell \_ Lesers " \_ \_ MediaSource" \_ beim \_ Shutdown-Attribut ignoriert.</span><span class="sxs-lookup"><span data-stu-id="7a9fa-118">The MF\_SOURCE\_READER\_DISCONNECT\_MEDIASOURCE\_ON\_SHUTDOWN attribute is ignored in this case.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a9fa-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7a9fa-119">Requirements</span></span>



| <span data-ttu-id="7a9fa-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7a9fa-120">Requirement</span></span> | <span data-ttu-id="7a9fa-121">Wert</span><span class="sxs-lookup"><span data-stu-id="7a9fa-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a9fa-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7a9fa-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7a9fa-123">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="7a9fa-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="7a9fa-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7a9fa-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7a9fa-125">Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="7a9fa-125">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="7a9fa-126">Header</span><span class="sxs-lookup"><span data-stu-id="7a9fa-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a9fa-127"><dt>"Mfreadwrite. h"</dt></span><span class="sxs-lookup"><span data-stu-id="7a9fa-127"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a9fa-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a9fa-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a9fa-129">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="7a9fa-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7a9fa-130">Quell Leser</span><span class="sxs-lookup"><span data-stu-id="7a9fa-130">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="7a9fa-131">Attribute des Quell Readers</span><span class="sxs-lookup"><span data-stu-id="7a9fa-131">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




