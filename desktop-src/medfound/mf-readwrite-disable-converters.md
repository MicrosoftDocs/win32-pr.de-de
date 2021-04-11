---
description: Aktiviert oder deaktiviert Formatkonvertierungen durch den Quell-oder senkenwriter.
ms.assetid: 282b70c3-c81c-47dd-bfa2-7e77138ccb91
title: MF_READWRITE_DISABLE_CONVERTERS-Attribut (mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8532c45ca3aeb272fa6b6ef422e0d82e40bd3e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218238"
---
# <a name="mf_readwrite_disable_converters-attribute"></a><span data-ttu-id="9289e-103">MF- \_ /Schreib-deaktivierte \_ \_ Konverter</span><span class="sxs-lookup"><span data-stu-id="9289e-103">MF\_READWRITE\_DISABLE\_CONVERTERS attribute</span></span>

<span data-ttu-id="9289e-104">Aktiviert oder deaktiviert Formatkonvertierungen durch den Quell-oder senkenwriter.</span><span class="sxs-lookup"><span data-stu-id="9289e-104">Enables or disables format conversions by the source reader or sink writer.</span></span>

## <a name="data-type"></a><span data-ttu-id="9289e-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="9289e-105">Data type</span></span>

<span data-ttu-id="9289e-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="9289e-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="9289e-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="9289e-107">Get/set</span></span>

<span data-ttu-id="9289e-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="9289e-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="9289e-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="9289e-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="9289e-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9289e-110">Remarks</span></span>

<span data-ttu-id="9289e-111">Standardmäßig können der Quell-und der senkenwriter einige Formatkonvertierungen für unkomprimierte Audiodaten und Videostreams ausführen.</span><span class="sxs-lookup"><span data-stu-id="9289e-111">By default, the source reader and sink writer can perform some format conversions on uncompressed audio and video streams.</span></span> <span data-ttu-id="9289e-112">Um dieses Verhalten zu deaktivieren, legen Sie dieses Attribut auf " **true** " fest, wenn Sie den Quell-oder senderwriter erstellen.</span><span class="sxs-lookup"><span data-stu-id="9289e-112">To disable this behavior, set this attribute to **TRUE** when you create the source reader or sink writer.</span></span>

<span data-ttu-id="9289e-113">Verwenden Sie dieses Attribut mit den folgenden Funktionen:</span><span class="sxs-lookup"><span data-stu-id="9289e-113">Use this attribute with the following functions:</span></span>

-   [<span data-ttu-id="9289e-114">**MF | atesourcereaderfromb-testream**</span><span class="sxs-lookup"><span data-stu-id="9289e-114">**MFCreateSourceReaderFromByteStream**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [<span data-ttu-id="9289e-115">**Mfkreatesourcereaderfrommediasource**</span><span class="sxs-lookup"><span data-stu-id="9289e-115">**MFCreateSourceReaderFromMediaSource**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [<span data-ttu-id="9289e-116">**MF | atesourcereaderfromurl**</span><span class="sxs-lookup"><span data-stu-id="9289e-116">**MFCreateSourceReaderFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)
-   [<span data-ttu-id="9289e-117">**Mfkreatesinkschreiterfrommediasink**</span><span class="sxs-lookup"><span data-stu-id="9289e-117">**MFCreateSinkWriterFromMediaSink**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [<span data-ttu-id="9289e-118">**MF | atesinkschreiterfromurl**</span><span class="sxs-lookup"><span data-stu-id="9289e-118">**MFCreateSinkWriterFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

## <a name="requirements"></a><span data-ttu-id="9289e-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9289e-119">Requirements</span></span>



| <span data-ttu-id="9289e-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9289e-120">Requirement</span></span> | <span data-ttu-id="9289e-121">Wert</span><span class="sxs-lookup"><span data-stu-id="9289e-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9289e-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9289e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9289e-123">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="9289e-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="9289e-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9289e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9289e-125">Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="9289e-125">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="9289e-126">Header</span><span class="sxs-lookup"><span data-stu-id="9289e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9289e-127"><dt>"Mfreadwrite. h"</dt></span><span class="sxs-lookup"><span data-stu-id="9289e-127"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9289e-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9289e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9289e-129">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="9289e-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="9289e-130">Senkenwriter-Attribute</span><span class="sxs-lookup"><span data-stu-id="9289e-130">Sink Writer Attributes</span></span>](sink-writer-attributes.md)
</dt> <dt>

[<span data-ttu-id="9289e-131">Attribute des Quell Readers</span><span class="sxs-lookup"><span data-stu-id="9289e-131">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




