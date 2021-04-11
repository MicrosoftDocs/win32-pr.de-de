---
description: Verweis auf die durchschnittliche Volumeebene einer Windows Media Audio Datei.
ms.assetid: ea7d4ed1-2a96-4372-9936-abdd6473b57e
title: MF_MT_AUDIO_WMADRC_AVGREF-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cdde0bfb4c2993580d73981e9e121d1f7f18612
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215144"
---
# <a name="mf_mt_audio_wmadrc_avgref-attribute"></a><span data-ttu-id="968a8-103">MF \_ MT \_ - \_ audioattribut wmadrc \_ avgref-Attribut</span><span class="sxs-lookup"><span data-stu-id="968a8-103">MF\_MT\_AUDIO\_WMADRC\_AVGREF attribute</span></span>

<span data-ttu-id="968a8-104">Verweis auf die durchschnittliche Volumeebene einer Windows Media Audio Datei.</span><span class="sxs-lookup"><span data-stu-id="968a8-104">Reference average volume level of a Windows Media Audio file.</span></span>

## <a name="data-type"></a><span data-ttu-id="968a8-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="968a8-105">Data type</span></span>

<span data-ttu-id="968a8-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="968a8-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="968a8-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="968a8-107">Remarks</span></span>

<span data-ttu-id="968a8-108">Dieses Attribut gilt für audiomedientypen für Windows Media Audio Codecs.</span><span class="sxs-lookup"><span data-stu-id="968a8-108">This attribute applies to audio media types for Windows Media Audio codecs.</span></span> <span data-ttu-id="968a8-109">Gibt die ursprüngliche durchschnittliche Volumeebene für den Inhalt an.</span><span class="sxs-lookup"><span data-stu-id="968a8-109">It specifies the original average volume level of the content.</span></span> <span data-ttu-id="968a8-110">Der Decoder kann diesen Wert verwenden, um ein dynamisches Bereichs Steuerelement auszuführen.</span><span class="sxs-lookup"><span data-stu-id="968a8-110">The decoder can use this value to perform dynamic range control.</span></span>

<span data-ttu-id="968a8-111">Die [**imfasfcontentinfo::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) -Methode fügt dieses Attribut dem Medientyp hinzu, wenn der ASF-Header das [**WM/wmadrcaveragereferenzierungsattribut**](../wmformat/wm-wmadrcaveragereference.md) enthält.</span><span class="sxs-lookup"><span data-stu-id="968a8-111">The [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) method adds this attribute to the media type if the ASF header contains the [**WM/WMADRCAverageReference**](../wmformat/wm-wmadrcaveragereference.md) attribute.</span></span> <span data-ttu-id="968a8-112">Dieses Attribut ist in der Dokumentation zum Windows Media-Format SDK dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="968a8-112">This attribute is documented in the Windows Media Format SDK documentation.</span></span>

<span data-ttu-id="968a8-113">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="968a8-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="968a8-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="968a8-114">Requirements</span></span>



| <span data-ttu-id="968a8-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="968a8-115">Requirement</span></span> | <span data-ttu-id="968a8-116">Wert</span><span class="sxs-lookup"><span data-stu-id="968a8-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="968a8-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="968a8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="968a8-118">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="968a8-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="968a8-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="968a8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="968a8-120">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="968a8-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="968a8-121">Header</span><span class="sxs-lookup"><span data-stu-id="968a8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="968a8-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="968a8-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="968a8-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="968a8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="968a8-124">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="968a8-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="968a8-125">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="968a8-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="968a8-126">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="968a8-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="968a8-127">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="968a8-127">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="968a8-128">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="968a8-128">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
