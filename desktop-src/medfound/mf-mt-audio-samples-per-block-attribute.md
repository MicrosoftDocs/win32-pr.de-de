---
description: Anzahl von Audiobeispielen, die in einem komprimierten Block von Audiodaten enthalten sind. Dieses Attribut kann in komprimierten Audioformaten verwendet werden, die über eine festgelegte Anzahl von Stichproben in jedem Block verfügen.
ms.assetid: 6ae31548-4d78-4e38-9cfc-01b611a6022d
title: MF_MT_AUDIO_SAMPLES_PER_BLOCK-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7c453fa4daeaa310b5e41add44b63b0fb45372d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363233"
---
# <a name="mf_mt_audio_samples_per_block-attribute"></a><span data-ttu-id="b334c-104">MF \_ \_ -MT- \_ Audiobeispiele \_ pro Block- \_ Attribut</span><span class="sxs-lookup"><span data-stu-id="b334c-104">MF\_MT\_AUDIO\_SAMPLES\_PER\_BLOCK attribute</span></span>

<span data-ttu-id="b334c-105">Anzahl von Audiobeispielen, die in einem komprimierten Block von Audiodaten enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="b334c-105">Number of audio samples contained in one compressed block of audio data.</span></span> <span data-ttu-id="b334c-106">Dieses Attribut kann in komprimierten Audioformaten verwendet werden, die über eine festgelegte Anzahl von Stichproben in jedem Block verfügen.</span><span class="sxs-lookup"><span data-stu-id="b334c-106">This attribute can be used in compressed audio formats that have a fixed number of samples within each block.</span></span>

## <a name="data-type"></a><span data-ttu-id="b334c-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="b334c-107">Data type</span></span>

<span data-ttu-id="b334c-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="b334c-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="b334c-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b334c-109">Remarks</span></span>

<span data-ttu-id="b334c-110">Dieses Attribut entspricht dem **wsamplesperblock** -Member der [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="b334c-110">This attribute corresponds to the **wSamplesPerBlock** member of the [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) structure.</span></span>

<span data-ttu-id="b334c-111">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="b334c-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b334c-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b334c-112">Requirements</span></span>



| <span data-ttu-id="b334c-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b334c-113">Requirement</span></span> | <span data-ttu-id="b334c-114">Wert</span><span class="sxs-lookup"><span data-stu-id="b334c-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b334c-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b334c-115">Minimum supported client</span></span><br/> | <span data-ttu-id="b334c-116">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="b334c-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="b334c-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b334c-117">Minimum supported server</span></span><br/> | <span data-ttu-id="b334c-118">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="b334c-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="b334c-119">Header</span><span class="sxs-lookup"><span data-stu-id="b334c-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="b334c-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b334c-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b334c-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b334c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b334c-122">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="b334c-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b334c-123">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="b334c-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="b334c-124">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="b334c-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="b334c-125">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="b334c-125">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="b334c-126">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="b334c-126">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
