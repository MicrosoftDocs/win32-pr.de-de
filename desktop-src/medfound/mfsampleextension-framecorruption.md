---
description: Gibt an, ob ein Videoframe beschädigt ist.
ms.assetid: 0218F6F6-6832-445C-B733-6A99E4EA2A3B
title: MFSampleExtension_FrameCorruption-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0d3618e5d847833b539cdfa7f6f99ae784e96c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131117"
---
# <a name="mfsampleextension_framecorruption-attribute"></a><span data-ttu-id="c2a63-103">Attribut "MF Sample Extension \_ framebeschäbeschädigung"</span><span class="sxs-lookup"><span data-stu-id="c2a63-103">MFSampleExtension\_FrameCorruption attribute</span></span>

<span data-ttu-id="c2a63-104">Gibt an, ob ein Videoframe beschädigt ist.</span><span class="sxs-lookup"><span data-stu-id="c2a63-104">Specifies whether a video frame is corrupted.</span></span>

## <a name="data-type"></a><span data-ttu-id="c2a63-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="c2a63-105">Data type</span></span>

<span data-ttu-id="c2a63-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="c2a63-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="c2a63-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="c2a63-107">Get/set</span></span>

<span data-ttu-id="c2a63-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="c2a63-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="c2a63-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="c2a63-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="c2a63-110">Gilt für:</span><span class="sxs-lookup"><span data-stu-id="c2a63-110">Applies to</span></span>

[<span data-ttu-id="c2a63-111">**IMF Sample**</span><span class="sxs-lookup"><span data-stu-id="c2a63-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="c2a63-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c2a63-112">Remarks</span></span>

<span data-ttu-id="c2a63-113">Ein Video Decoder kann dieses Attribut für seine Ausgabe Beispiele festlegen.</span><span class="sxs-lookup"><span data-stu-id="c2a63-113">A video decoder can set this attribute on its output samples.</span></span> <span data-ttu-id="c2a63-114">Wenn der Wert 1 ist, hat der Decoder Daten Beschädigungen im Frame erkannt.</span><span class="sxs-lookup"><span data-stu-id="c2a63-114">If the value is 1, the decoder detected data corruption in the frame.</span></span> <span data-ttu-id="c2a63-115">Wenn der Wert 0 ist, sind keine Daten beschädigt, oder es wurde kein Fehler erkannt.</span><span class="sxs-lookup"><span data-stu-id="c2a63-115">If the value is 0, there is no data corruption, or none was detected.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2a63-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c2a63-116">Requirements</span></span>



| <span data-ttu-id="c2a63-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c2a63-117">Requirement</span></span> | <span data-ttu-id="c2a63-118">Wert</span><span class="sxs-lookup"><span data-stu-id="c2a63-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c2a63-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c2a63-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c2a63-120">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="c2a63-120">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="c2a63-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c2a63-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c2a63-122">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="c2a63-122">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="c2a63-123">Header</span><span class="sxs-lookup"><span data-stu-id="c2a63-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2a63-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2a63-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2a63-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2a63-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2a63-126">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="c2a63-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c2a63-127">Beispiel Attribute</span><span class="sxs-lookup"><span data-stu-id="c2a63-127">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="c2a63-128">Medien Beispiele</span><span class="sxs-lookup"><span data-stu-id="c2a63-128">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 




