---
description: Block Ausrichtung (in Byte) für einen audiomedientyp. Die Block Ausrichtung ist die minimale atomarische Einheit von Daten für das Audioformat.
ms.assetid: 7d304826-ad81-4243-a675-2f55b668b348
title: MF_MT_AUDIO_BLOCK_ALIGNMENT-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21efb14cbb89d1773fe9bc3b5ade8d0a50555a1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356243"
---
# <a name="mf_mt_audio_block_alignment-attribute"></a><span data-ttu-id="691d8-104">Das MF \_ MT \_ - \_ Audioblock- \_ Ausrichtungs Attribut</span><span class="sxs-lookup"><span data-stu-id="691d8-104">MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT attribute</span></span>

<span data-ttu-id="691d8-105">Block Ausrichtung (in Byte) für einen audiomedientyp.</span><span class="sxs-lookup"><span data-stu-id="691d8-105">Block alignment, in bytes, for an audio media type.</span></span> <span data-ttu-id="691d8-106">Die Block Ausrichtung ist die minimale atomarische Einheit von Daten für das Audioformat.</span><span class="sxs-lookup"><span data-stu-id="691d8-106">The block alignment is the minimum atomic unit of data for the audio format.</span></span>

## <a name="data-type"></a><span data-ttu-id="691d8-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="691d8-107">Data type</span></span>

<span data-ttu-id="691d8-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="691d8-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="691d8-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="691d8-109">Remarks</span></span>

<span data-ttu-id="691d8-110">Bei PCM-Audioformaten ist die Block Ausrichtung gleich der Anzahl der Audiokanäle multipliziert mit der Anzahl der Bytes pro audiostich Probe.</span><span class="sxs-lookup"><span data-stu-id="691d8-110">For PCM audio formats, the block alignment is equal to the number of audio channels multiplied by the number of bytes per audio sample.</span></span>

<span data-ttu-id="691d8-111">Dieses Attribut entspricht dem **nBlockAlign** -Member der [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="691d8-111">This attribute corresponds to the **nBlockAlign** member of the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>

<span data-ttu-id="691d8-112">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="691d8-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="691d8-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="691d8-113">Requirements</span></span>



| <span data-ttu-id="691d8-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="691d8-114">Requirement</span></span> | <span data-ttu-id="691d8-115">Wert</span><span class="sxs-lookup"><span data-stu-id="691d8-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="691d8-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="691d8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="691d8-117">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="691d8-117">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="691d8-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="691d8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="691d8-119">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="691d8-119">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="691d8-120">Header</span><span class="sxs-lookup"><span data-stu-id="691d8-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="691d8-121"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="691d8-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="691d8-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="691d8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="691d8-123">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="691d8-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="691d8-124">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="691d8-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="691d8-125">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="691d8-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="691d8-126">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="691d8-126">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="691d8-127">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="691d8-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
