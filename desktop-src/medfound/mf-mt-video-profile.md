---
description: Gibt das Profil der Videocodierung für den Ausgabe Medientyp an. Dies ist ein Alias des MF \_ MT \_ \_
ms.assetid: 29D1CCCA-CC11-46F1-A094-8BA8F74F7EE9
title: MF_MT_VIDEO_PROFILE-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf6dbf8d324c7a451c1d2affb9f348a3ef2e1806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364235"
---
# <a name="mf_mt_video_profile-attribute"></a><span data-ttu-id="0ed3c-104">MF \_ MT- \_ Video \_ Profil Attribut</span><span class="sxs-lookup"><span data-stu-id="0ed3c-104">MF\_MT\_VIDEO\_PROFILE attribute</span></span>

<span data-ttu-id="0ed3c-105">Gibt das Profil der Videocodierung für den Ausgabe Medientyp an.</span><span class="sxs-lookup"><span data-stu-id="0ed3c-105">Specifies the profile of video encoding on the output media type.</span></span> <span data-ttu-id="0ed3c-106">Dies ist ein Alias des [MF \_ MT \_ \_ ](mf-mt-mpeg2-profile-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="0ed3c-106">This is an alias of [MF\_MT\_MPEG2\_PROFILE](mf-mt-mpeg2-profile-attribute.md) attribute.</span></span>

## <a name="data-type"></a><span data-ttu-id="0ed3c-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="0ed3c-107">Data type</span></span>

<span data-ttu-id="0ed3c-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="0ed3c-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="0ed3c-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0ed3c-109">Remarks</span></span>

<span data-ttu-id="0ed3c-110">**H. 264-Encoder:**</span><span class="sxs-lookup"><span data-stu-id="0ed3c-110">**H.264 encoders:**</span></span>

<span data-ttu-id="0ed3c-111">Unterstützte Profile werden mit [**eAVEncH264VProfile \_ einschränieedbase**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) und **eAVEncH264VProfile \_ einschräninedhigh** überschritten.</span><span class="sxs-lookup"><span data-stu-id="0ed3c-111">Supported profiles are exceeded to include [**eAVEncH264VProfile\_ConstrainedBase**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) and **eAVEncH264VProfile\_ConstrainedHigh**.</span></span>

<span data-ttu-id="0ed3c-112">Encoder müssen sowohl [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) als auch [**SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) für dieses Attribut unterstützen.</span><span class="sxs-lookup"><span data-stu-id="0ed3c-112">Encoders shall support both [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) and [**SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) for this attribute.</span></span>

<span data-ttu-id="0ed3c-113">Dies ist statisch, sodass Video Encoder konfiguriert werden müssen, bevor das Streaming gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="0ed3c-113">This is static, so video encoders must be configured before the streaming starts.</span></span> <span data-ttu-id="0ed3c-114">Wenn von der Anwendung ein Profil festgelegt wird, das der Encoder nicht unterstützt, lehnt der Encoder den Medientyp ab.</span><span class="sxs-lookup"><span data-stu-id="0ed3c-114">If the application sets a profile which the encoder does not support, the encoder shall reject the media type.</span></span>

<span data-ttu-id="0ed3c-115">Empfohlene Standardeinstellung: [**eAVEncH264VProfile \_ Main**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) Profile.</span><span class="sxs-lookup"><span data-stu-id="0ed3c-115">Recommended default: [**eAVEncH264VProfile\_Main**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) profile.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ed3c-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0ed3c-116">Requirements</span></span>



| <span data-ttu-id="0ed3c-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0ed3c-117">Requirement</span></span> | <span data-ttu-id="0ed3c-118">Wert</span><span class="sxs-lookup"><span data-stu-id="0ed3c-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0ed3c-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0ed3c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0ed3c-120">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="0ed3c-120">Windows 8.1 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="0ed3c-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0ed3c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0ed3c-122">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0ed3c-122">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="0ed3c-123">Header</span><span class="sxs-lookup"><span data-stu-id="0ed3c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ed3c-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ed3c-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ed3c-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0ed3c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ed3c-126">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="0ed3c-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
