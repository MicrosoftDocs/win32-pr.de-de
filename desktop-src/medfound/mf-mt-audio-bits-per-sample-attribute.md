---
description: Anzahl von Bits pro audiostich Probe in einem audiomedientyp.
ms.assetid: d78a8c4d-377e-45eb-9cf6-2d61b34e82d6
title: MF_MT_AUDIO_BITS_PER_SAMPLE-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 896e77c937269b63208cb4bff73482a8df8596aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357451"
---
# <a name="mf_mt_audio_bits_per_sample-attribute"></a><span data-ttu-id="0ef4b-103">MF \_ \_ -MT- \_ audiobits \_ pro Sample- \_ Attribut</span><span class="sxs-lookup"><span data-stu-id="0ef4b-103">MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE attribute</span></span>

<span data-ttu-id="0ef4b-104">Anzahl von Bits pro audiostich Probe in einem audiomedientyp.</span><span class="sxs-lookup"><span data-stu-id="0ef4b-104">Number of bits per audio sample in an audio media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="0ef4b-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="0ef4b-105">Data type</span></span>

<span data-ttu-id="0ef4b-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="0ef4b-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="0ef4b-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0ef4b-107">Remarks</span></span>

<span data-ttu-id="0ef4b-108">Dieses Attribut entspricht dem **wbitspersample** -Member der [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="0ef4b-108">This attribute corresponds to the **wBitsPerSample** member of the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>

<span data-ttu-id="0ef4b-109">Wenn einige Bits Auffüll Zeichen enthalten, legen Sie die für die [**MF \_ \_ -MT-Audiodatei \_ gültigen \_ Bits \_ pro \_ Sample-**](mf-mt-audio-valid-bits-per-sample-attribute.md) Attribut fest, um die Anzahl der Bits gültiger Audiodaten in jedem Beispiel anzugeben.</span><span class="sxs-lookup"><span data-stu-id="0ef4b-109">If some bits contain padding, set the [**MF\_MT\_AUDIO\_VALID\_BITS\_PER\_SAMPLE**](mf-mt-audio-valid-bits-per-sample-attribute.md) attribute to specify the number of bits of valid audio data in each sample.</span></span>

<span data-ttu-id="0ef4b-110">Wenn die Audiodatei 8 Bits pro Stichprobe enthält, sind die Audiobeispiele nicht signierte Werte.</span><span class="sxs-lookup"><span data-stu-id="0ef4b-110">If the audio contains 8 bits per sample, the audio samples are unsigned values.</span></span> <span data-ttu-id="0ef4b-111">(Jedes Audiobeispiel hat den Bereich 0 – 255.) Wenn die Audiodatei 16 Bits pro Stichprobe oder höher enthält, sind die Audiobeispiele signierte Werte.</span><span class="sxs-lookup"><span data-stu-id="0ef4b-111">(Each audio sample has the range 0–255.) If the audio contains 16 bits per sample or higher, the audio samples are signed values.</span></span>

<span data-ttu-id="0ef4b-112">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="0ef4b-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ef4b-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0ef4b-113">Requirements</span></span>



| <span data-ttu-id="0ef4b-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0ef4b-114">Requirement</span></span> | <span data-ttu-id="0ef4b-115">Wert</span><span class="sxs-lookup"><span data-stu-id="0ef4b-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0ef4b-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0ef4b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0ef4b-117">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="0ef4b-117">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="0ef4b-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0ef4b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0ef4b-119">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="0ef4b-119">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="0ef4b-120">Header</span><span class="sxs-lookup"><span data-stu-id="0ef4b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ef4b-121"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ef4b-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ef4b-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0ef4b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ef4b-123">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="0ef4b-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0ef4b-124">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="0ef4b-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="0ef4b-125">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="0ef4b-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="0ef4b-126">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="0ef4b-126">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="0ef4b-127">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="0ef4b-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
