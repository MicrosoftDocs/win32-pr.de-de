---
description: Gibt für einen Medientyp an, ob jede Stichprobe unabhängig von den anderen Beispielen im Stream ist.
ms.assetid: 40434f63-e191-45e1-b788-5f80fe7f49ae
title: MF_MT_ALL_SAMPLES_INDEPENDENT-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f82173e99a30e033b3d90f6cfec0dc2aa8b3af97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354599"
---
# <a name="mf_mt_all_samples_independent-attribute"></a><span data-ttu-id="68503-103">MF \_ MT \_ All \_ Samples \_ Independent Attribute</span><span class="sxs-lookup"><span data-stu-id="68503-103">MF\_MT\_ALL\_SAMPLES\_INDEPENDENT attribute</span></span>

<span data-ttu-id="68503-104">Gibt für einen Medientyp an, ob jede Stichprobe unabhängig von den anderen Beispielen im Stream ist.</span><span class="sxs-lookup"><span data-stu-id="68503-104">Specifies for a media type whether each sample is independent of the other samples in the stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="68503-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="68503-105">Data type</span></span>

<span data-ttu-id="68503-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="68503-106">**UINT32**</span></span>

<span data-ttu-id="68503-107">Als booleschen Wert behandeln.</span><span class="sxs-lookup"><span data-stu-id="68503-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="68503-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="68503-108">Remarks</span></span>

<span data-ttu-id="68503-109">Wenn dieses Attribut **false** ist, können einige Beispiele nicht verwendet werden, ohne auf andere Beispiele im Stream zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="68503-109">If this attribute is **FALSE**, some samples cannot be used without referring to other samples in the stream.</span></span> <span data-ttu-id="68503-110">Wenn ein Videoformat z. b. Delta Rahmen enthält, sollte dieses Attribut " **false**" lauten.</span><span class="sxs-lookup"><span data-stu-id="68503-110">For example, if a video format contains delta frames, this attribute should be **FALSE**.</span></span>

<span data-ttu-id="68503-111">Dieses Attribut entspricht dem Feld **btemporalcompression** in der Struktur des DirectShow [**am- \_ Medien \_ Typs**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="68503-111">This attribute corresponds to the **bTemporalCompression** field in the DirectShow [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

<span data-ttu-id="68503-112">Legen Sie dieses Attribut für alle nicht komprimierten Medientypen auf **true** fest.</span><span class="sxs-lookup"><span data-stu-id="68503-112">Set this attribute to **TRUE** for all uncompressed media types.</span></span>

<span data-ttu-id="68503-113">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="68503-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="68503-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="68503-114">Requirements</span></span>



| <span data-ttu-id="68503-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="68503-115">Requirement</span></span> | <span data-ttu-id="68503-116">Wert</span><span class="sxs-lookup"><span data-stu-id="68503-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="68503-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="68503-117">Minimum supported client</span></span><br/> | <span data-ttu-id="68503-118">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="68503-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="68503-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="68503-119">Minimum supported server</span></span><br/> | <span data-ttu-id="68503-120">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="68503-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="68503-121">Header</span><span class="sxs-lookup"><span data-stu-id="68503-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="68503-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="68503-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68503-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="68503-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68503-124">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="68503-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="68503-125">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="68503-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="68503-126">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="68503-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="68503-127">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="68503-127">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="68503-128">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="68503-128">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
