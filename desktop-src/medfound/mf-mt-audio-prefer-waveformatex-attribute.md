---
description: Gibt die bevorzugte Legacy Format Struktur an, die beim Umrechnen eines audiomedientyps verwendet werden soll.
ms.assetid: 9bb045a2-be5b-468b-b30b-aedcb7849945
title: MF_MT_AUDIO_PREFER_WAVEFORMATEX-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7be5f5ac0aadfb2a4d8d2b8394a06f270e1b4d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528244"
---
# <a name="mf_mt_audio_prefer_waveformatex-attribute"></a><span data-ttu-id="33b9d-103">MF \_ \_ -MT-Audiodatei \_ bevorzugt \_ WaveFormatEx-Attribut</span><span class="sxs-lookup"><span data-stu-id="33b9d-103">MF\_MT\_AUDIO\_PREFER\_WAVEFORMATEX attribute</span></span>

<span data-ttu-id="33b9d-104">Gibt die bevorzugte Legacy Format Struktur an, die beim Umrechnen eines audiomedientyps verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="33b9d-104">Specifies the preferred legacy format structure to use when converting an audio media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="33b9d-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="33b9d-105">Data type</span></span>

<span data-ttu-id="33b9d-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="33b9d-106">**UINT32**</span></span>

<span data-ttu-id="33b9d-107">Als booleschen Wert behandeln.</span><span class="sxs-lookup"><span data-stu-id="33b9d-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="33b9d-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="33b9d-108">Remarks</span></span>

<span data-ttu-id="33b9d-109">Dieses Attribut stellt einen Hinweis für die Funktion [**mfkreatewaveformatexfrommfmediatype**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype) bereit.</span><span class="sxs-lookup"><span data-stu-id="33b9d-109">This attribute provides a hint to the [**MFCreateWaveFormatExFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype) function.</span></span> <span data-ttu-id="33b9d-110">Wenn das Attribut **true** ist, konvertiert die-Funktion den audiomedientyp nach Möglichkeit in eine [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Struktur, anstatt Sie in eine [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) -Struktur zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="33b9d-110">If the attribute is **TRUE**, the function converts the audio media type to a [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure whenever possible, instead of converting it to a [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) structure.</span></span>

<span data-ttu-id="33b9d-111">Die Funktion " [**mfinitmediatypeer fromwaveformatex**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex) " legt dieses Attribut fest.</span><span class="sxs-lookup"><span data-stu-id="33b9d-111">The [**MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex) function sets this attribute.</span></span> <span data-ttu-id="33b9d-112">Sie können den Wert dieses Attributs überschreiben. Wenn Sie dieses Attribut auf " **true** " festlegen, wird jedoch nicht sichergestellt, dass ein audiomedientyp in das [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Formular konvertiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="33b9d-112">You can override the value of this attribute, but setting this attribute to **TRUE** does not guarantee that an audio media type can be converted to [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) form.</span></span>

<span data-ttu-id="33b9d-113">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="33b9d-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="33b9d-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="33b9d-114">Requirements</span></span>



| <span data-ttu-id="33b9d-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="33b9d-115">Requirement</span></span> | <span data-ttu-id="33b9d-116">Wert</span><span class="sxs-lookup"><span data-stu-id="33b9d-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="33b9d-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="33b9d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="33b9d-118">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="33b9d-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="33b9d-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="33b9d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="33b9d-120">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="33b9d-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="33b9d-121">Header</span><span class="sxs-lookup"><span data-stu-id="33b9d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="33b9d-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="33b9d-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33b9d-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="33b9d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33b9d-124">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="33b9d-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="33b9d-125">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="33b9d-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="33b9d-126">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="33b9d-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="33b9d-127">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="33b9d-127">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="33b9d-128">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="33b9d-128">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
