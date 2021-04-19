---
description: Gibt das Audioprofil und die Ebene eines AAC-Streams (Advanced audiocoding) an.
ms.assetid: 87fa1127-46ca-4b83-a3b5-99253af22ba0
title: MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 116bfc2b41cff3cbd92fc9a60be150ea598e1cc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359774"
---
# <a name="mf_mt_aac_audio_profile_level_indication-attribute"></a><span data-ttu-id="c716b-103">Attribut der MF \_ \_ \_ -AAC- \_ \_ audioprofilebene- \_ Anzeige</span><span class="sxs-lookup"><span data-stu-id="c716b-103">MF\_MT\_AAC\_AUDIO\_PROFILE\_LEVEL\_INDICATION attribute</span></span>

<span data-ttu-id="c716b-104">Gibt das Audioprofil und die Ebene eines AAC-Streams (Advanced audiocoding) an.</span><span class="sxs-lookup"><span data-stu-id="c716b-104">Specifies the audio profile and level of an Advanced Audio Coding (AAC) stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="c716b-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="c716b-105">Data type</span></span>

<span data-ttu-id="c716b-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="c716b-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="c716b-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="c716b-107">Get/set</span></span>

<span data-ttu-id="c716b-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="c716b-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="c716b-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="c716b-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="c716b-110">Gilt für</span><span class="sxs-lookup"><span data-stu-id="c716b-110">Applies To</span></span>

[<span data-ttu-id="c716b-111">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="c716b-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="c716b-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c716b-112">Remarks</span></span>

<span data-ttu-id="c716b-113">Dieses Attribut enthält den Wert des **audioprofilelevelindikation** -Felds gemäß ISO/IEC 14496-3.</span><span class="sxs-lookup"><span data-stu-id="c716b-113">This attribute contains the value of the **audioProfileLevelIndication** field, as defined by ISO/IEC 14496-3.</span></span>

<span data-ttu-id="c716b-114">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="c716b-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="c716b-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c716b-115">Requirements</span></span>



| <span data-ttu-id="c716b-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c716b-116">Requirement</span></span> | <span data-ttu-id="c716b-117">Wert</span><span class="sxs-lookup"><span data-stu-id="c716b-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c716b-118">Header</span><span class="sxs-lookup"><span data-stu-id="c716b-118">Header</span></span><br/> | <dl> <span data-ttu-id="c716b-119"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c716b-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c716b-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c716b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c716b-121">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="c716b-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c716b-122">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="c716b-122">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




