---
description: Anzahl gültiger Bits von Audiodaten in jedem Audiobeispiel.
ms.assetid: b5b97700-c98a-4394-a184-661852add0b4
title: MF_MT_AUDIO_VALID_BITS_PER_SAMPLE-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d4e5efb41bf3b79d4feded2872b601eea43723a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349919"
---
# <a name="mf_mt_audio_valid_bits_per_sample-attribute"></a><span data-ttu-id="ea4e5-103">Zulässige "MF \_ \_ -MT-Audioinhalte" \_ \_ \_ pro \_ Beispiel Attribut</span><span class="sxs-lookup"><span data-stu-id="ea4e5-103">MF\_MT\_AUDIO\_VALID\_BITS\_PER\_SAMPLE attribute</span></span>

<span data-ttu-id="ea4e5-104">Anzahl gültiger Bits von Audiodaten in jedem Audiobeispiel.</span><span class="sxs-lookup"><span data-stu-id="ea4e5-104">Number of valid bits of audio data in each audio sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="ea4e5-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="ea4e5-105">Data type</span></span>

<span data-ttu-id="ea4e5-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="ea4e5-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="ea4e5-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ea4e5-107">Remarks</span></span>

<span data-ttu-id="ea4e5-108">Für Audioformate, die nach jedem Audiosample Auffüll Zeichen enthalten, wird das für die audioformatierung **\_ \_ \_ gültigen \_ Bits \_ pro \_ Beispiel** Attribut verwendet.</span><span class="sxs-lookup"><span data-stu-id="ea4e5-108">The **MF\_MT\_AUDIO\_VALID\_BITS\_PER\_SAMPLE** attribute is used for audio formats that contain padding after each audio sample.</span></span> <span data-ttu-id="ea4e5-109">Die Gesamtgröße der einzelnen Audiobeispiele einschließlich Auffüll Bits ist im [**MF \_ MT \_ - \_ audiobits \_ pro \_ Sample-**](mf-mt-audio-bits-per-sample-attribute.md) Attribut angegeben.</span><span class="sxs-lookup"><span data-stu-id="ea4e5-109">The total size of each audio sample, including padding bits, is given in the [**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**](mf-mt-audio-bits-per-sample-attribute.md) attribute.</span></span>

<span data-ttu-id="ea4e5-110">Wenn das für das **MF \_ \_ -MT-Paket \_ gültige \_ Bits \_ pro \_ Sample-** Attribut nicht festgelegt ist, verwenden Sie das [**MF \_ MT \_ - \_ audiobits \_ pro \_ Sample-**](mf-mt-audio-bits-per-sample-attribute.md) Attribut, um die Anzahl gültiger Bits pro Stichprobe zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="ea4e5-110">If the **MF\_MT\_AUDIO\_VALID\_BITS\_PER\_SAMPLE** attribute is not set, use the [**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**](mf-mt-audio-bits-per-sample-attribute.md) attribute to find the number of valid bits per sample.</span></span>

<span data-ttu-id="ea4e5-111">Wenn ein Audioformat keine Auffüll Bits enthält, sollte dieses Attribut nicht festgelegt werden, oder es sollte auf denselben Wert festgelegt werden wie das [**MF \_ MT \_ - \_ audiobits \_ pro \_ Sample-**](mf-mt-audio-bits-per-sample-attribute.md) Attribut.</span><span class="sxs-lookup"><span data-stu-id="ea4e5-111">If an audio format does not contain any padding bits, then this attribute should not be set, or should be set to the same value as the [**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**](mf-mt-audio-bits-per-sample-attribute.md) attribute.</span></span>

<span data-ttu-id="ea4e5-112">Dieses Attribut entspricht dem **wvalidbitspersample** -Member der [**WAVEFORMATEXTENSIBLE**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="ea4e5-112">This attribute corresponds to the **wValidBitsPerSample** member of the [**WAVEFORMATEXTENSIBLE**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible) structure.</span></span>

<span data-ttu-id="ea4e5-113">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="ea4e5-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea4e5-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ea4e5-114">Requirements</span></span>



| <span data-ttu-id="ea4e5-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ea4e5-115">Requirement</span></span> | <span data-ttu-id="ea4e5-116">Wert</span><span class="sxs-lookup"><span data-stu-id="ea4e5-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ea4e5-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ea4e5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ea4e5-118">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="ea4e5-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="ea4e5-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ea4e5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ea4e5-120">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="ea4e5-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="ea4e5-121">Header</span><span class="sxs-lookup"><span data-stu-id="ea4e5-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea4e5-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea4e5-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea4e5-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ea4e5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea4e5-124">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="ea4e5-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ea4e5-125">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="ea4e5-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="ea4e5-126">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="ea4e5-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="ea4e5-127">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="ea4e5-127">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="ea4e5-128">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="ea4e5-128">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
