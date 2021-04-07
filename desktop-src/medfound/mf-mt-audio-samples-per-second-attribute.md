---
description: Anzahl von Audiobeispielen pro Sekunde in einem audiomedientyp.
ms.assetid: f640016d-595e-4b20-8ce8-23a029c2b064
title: MF_MT_AUDIO_SAMPLES_PER_SECOND-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5080f6df87bafe8d4ee86e7b25332a12214ff3cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863587"
---
# <a name="mf_mt_audio_samples_per_second-attribute"></a><span data-ttu-id="a7db0-103">Attribut für MF \_ \_ -MT- \_ Audiobeispiele \_ pro \_ Sekunde</span><span class="sxs-lookup"><span data-stu-id="a7db0-103">MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND attribute</span></span>

<span data-ttu-id="a7db0-104">Anzahl von Audiobeispielen pro Sekunde in einem audiomedientyp.</span><span class="sxs-lookup"><span data-stu-id="a7db0-104">Number of audio samples per second in an audio media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="a7db0-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="a7db0-105">Data type</span></span>

<span data-ttu-id="a7db0-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="a7db0-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="a7db0-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a7db0-107">Remarks</span></span>

<span data-ttu-id="a7db0-108">Dieses Attribut entspricht dem **nsamplespersec** -Member der [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="a7db0-108">This attribute corresponds to the **nSamplesPerSec** member of the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>

<span data-ttu-id="a7db0-109">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="a7db0-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7db0-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a7db0-110">Requirements</span></span>



| <span data-ttu-id="a7db0-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a7db0-111">Requirement</span></span> | <span data-ttu-id="a7db0-112">Wert</span><span class="sxs-lookup"><span data-stu-id="a7db0-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a7db0-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a7db0-113">Minimum supported client</span></span><br/> | <span data-ttu-id="a7db0-114">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="a7db0-114">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="a7db0-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a7db0-115">Minimum supported server</span></span><br/> | <span data-ttu-id="a7db0-116">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="a7db0-116">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="a7db0-117">Header</span><span class="sxs-lookup"><span data-stu-id="a7db0-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7db0-118"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7db0-118"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7db0-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a7db0-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7db0-120">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="a7db0-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a7db0-121">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="a7db0-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="a7db0-122">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="a7db0-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="a7db0-123">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="a7db0-123">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="a7db0-124">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="a7db0-124">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="a7db0-125">**MF \_ \_ -MT- \_ audiofloat- \_ Beispiele \_ pro \_ Sekunde**</span><span class="sxs-lookup"><span data-stu-id="a7db0-125">**MF\_MT\_AUDIO\_FLOAT\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-float-samples-per-second-attribute.md)
</dt> </dl>

 

 
