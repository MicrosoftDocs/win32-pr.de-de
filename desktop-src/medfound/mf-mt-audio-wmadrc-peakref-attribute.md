---
description: Verweis Spitzen Volume-Ebene einer Windows Media Audio Datei.
ms.assetid: bb762f9c-cf08-4d32-991e-490eb7b1f579
title: MF_MT_AUDIO_WMADRC_PEAKREF-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0074046c79f532a4b63472f8ec22b588b2c4020a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528241"
---
# <a name="mf_mt_audio_wmadrc_peakref-attribute"></a><span data-ttu-id="9379b-103">MF \_ MT \_ -Audiodatei \_ wmadrc- \_ Attribut (Peer)</span><span class="sxs-lookup"><span data-stu-id="9379b-103">MF\_MT\_AUDIO\_WMADRC\_PEAKREF attribute</span></span>

<span data-ttu-id="9379b-104">Verweis Spitzen Volume-Ebene einer Windows Media Audio Datei.</span><span class="sxs-lookup"><span data-stu-id="9379b-104">Reference peak volume level of a Windows Media Audio file.</span></span>

## <a name="data-type"></a><span data-ttu-id="9379b-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="9379b-105">Data type</span></span>

<span data-ttu-id="9379b-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="9379b-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="9379b-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9379b-107">Remarks</span></span>

<span data-ttu-id="9379b-108">Dieses Attribut gilt für audiomedientypen für Windows Media Audio Codecs.</span><span class="sxs-lookup"><span data-stu-id="9379b-108">This attribute applies to audio media types for Windows Media Audio codecs.</span></span> <span data-ttu-id="9379b-109">Gibt die ursprüngliche maximale Volumeebene für den Inhalt an.</span><span class="sxs-lookup"><span data-stu-id="9379b-109">It specifies the original peak volume level of the content.</span></span> <span data-ttu-id="9379b-110">Der Decoder kann diesen Wert verwenden, um ein dynamisches Bereichs Steuerelement auszuführen.</span><span class="sxs-lookup"><span data-stu-id="9379b-110">The decoder can use this value to perform dynamic range control.</span></span>

<span data-ttu-id="9379b-111">Die [**imfasfcontentinfo::P archeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) -Methode fügt dieses Attribut dem Medientyp hinzu, wenn der ASF-Header das [**WM/wmadrcpeer Reference-**](../wmformat/wm-wmadrcpeakreference.md) Attribut enthält.</span><span class="sxs-lookup"><span data-stu-id="9379b-111">The [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) method adds this attribute to the media type if the ASF header contains the [**WM/WMADRCPeakReference**](../wmformat/wm-wmadrcpeakreference.md) attribute.</span></span> <span data-ttu-id="9379b-112">Dieses Attribut ist in der Dokumentation zum Windows Media-Format SDK dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="9379b-112">This attribute is documented in the Windows Media Format SDK documentation.</span></span>

<span data-ttu-id="9379b-113">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="9379b-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="9379b-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9379b-114">Requirements</span></span>



| <span data-ttu-id="9379b-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9379b-115">Requirement</span></span> | <span data-ttu-id="9379b-116">Wert</span><span class="sxs-lookup"><span data-stu-id="9379b-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9379b-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9379b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9379b-118">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="9379b-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="9379b-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9379b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9379b-120">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="9379b-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="9379b-121">Header</span><span class="sxs-lookup"><span data-stu-id="9379b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="9379b-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="9379b-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9379b-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9379b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9379b-124">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="9379b-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="9379b-125">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="9379b-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="9379b-126">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="9379b-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="9379b-127">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="9379b-127">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="9379b-128">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="9379b-128">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
