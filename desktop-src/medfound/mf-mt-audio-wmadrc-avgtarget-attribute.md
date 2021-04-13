---
description: Die durchschnittliche zielvolumeebene einer Windows Media Audio Datei.
ms.assetid: f81158c8-b341-4b39-8fa4-b510c93b89fc
title: MF_MT_AUDIO_WMADRC_AVGTARGET-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41956e2e9e6f14e969cade3628f1e88bce98796d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349129"
---
# <a name="mf_mt_audio_wmadrc_avgtarget-attribute"></a><span data-ttu-id="55202-103">MF \_ MT \_ -Audiodatei \_ wmademokratische \_ avgtarget-Attribut</span><span class="sxs-lookup"><span data-stu-id="55202-103">MF\_MT\_AUDIO\_WMADRC\_AVGTARGET attribute</span></span>

<span data-ttu-id="55202-104">Die durchschnittliche zielvolumeebene einer Windows Media Audio Datei.</span><span class="sxs-lookup"><span data-stu-id="55202-104">Target average volume level of a Windows Media Audio file.</span></span>

## <a name="data-type"></a><span data-ttu-id="55202-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="55202-105">Data type</span></span>

<span data-ttu-id="55202-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="55202-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="55202-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="55202-107">Remarks</span></span>

<span data-ttu-id="55202-108">Dieses Attribut gilt für audiomedientypen für Windows Media Audio Codecs.</span><span class="sxs-lookup"><span data-stu-id="55202-108">This attribute applies to audio media types for Windows Media Audio codecs.</span></span> <span data-ttu-id="55202-109">Hiermit wird die durchschnittliche zielvolumeebene des Inhalts angegeben.</span><span class="sxs-lookup"><span data-stu-id="55202-109">It specifies the target average volume level of the content.</span></span> <span data-ttu-id="55202-110">Der Decoder kann diesen Wert verwenden, um ein dynamisches Bereichs Steuerelement auszuführen.</span><span class="sxs-lookup"><span data-stu-id="55202-110">The decoder can use this value to perform dynamic range control.</span></span>

<span data-ttu-id="55202-111">Die [**imfasfcontentinfo::P artsheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) -Methode fügt dieses Attribut dem Medientyp hinzu, wenn der ASF-Header das [**WM/wmadrcaveragetarget-**](../wmformat/wm-wmadrcaveragetarget.md) Attribut enthält.</span><span class="sxs-lookup"><span data-stu-id="55202-111">The [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) method adds this attribute to the media type if the ASF header contains the [**WM/WMADRCAverageTarget**](../wmformat/wm-wmadrcaveragetarget.md) attribute.</span></span> <span data-ttu-id="55202-112">Dieses Attribut ist in der Dokumentation zum Windows Media-Format SDK dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="55202-112">This attribute is documented in the Windows Media Format SDK documentation.</span></span>

<span data-ttu-id="55202-113">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="55202-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="55202-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="55202-114">Requirements</span></span>



| <span data-ttu-id="55202-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="55202-115">Requirement</span></span> | <span data-ttu-id="55202-116">Wert</span><span class="sxs-lookup"><span data-stu-id="55202-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="55202-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="55202-117">Minimum supported client</span></span><br/> | <span data-ttu-id="55202-118">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="55202-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="55202-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="55202-119">Minimum supported server</span></span><br/> | <span data-ttu-id="55202-120">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="55202-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="55202-121">Header</span><span class="sxs-lookup"><span data-stu-id="55202-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="55202-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="55202-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55202-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="55202-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55202-124">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="55202-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="55202-125">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="55202-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="55202-126">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="55202-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="55202-127">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="55202-127">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="55202-128">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="55202-128">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
