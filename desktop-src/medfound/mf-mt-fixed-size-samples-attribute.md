---
description: Gibt für einen Medientyp an, ob die Stichproben eine festgelegte Größe aufweisen.
ms.assetid: 2d67864a-fd2f-400d-8a1e-e71dc1920593
title: MF_MT_FIXED_SIZE_SAMPLES-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d1bb5bdd4e1330e4744902ed1b37cc55b7a67a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368200"
---
# <a name="mf_mt_fixed_size_samples-attribute"></a><span data-ttu-id="70bd7-103">Das MF \_ MT- \_ Attribut mit fester \_ Größe \_ Samples</span><span class="sxs-lookup"><span data-stu-id="70bd7-103">MF\_MT\_FIXED\_SIZE\_SAMPLES attribute</span></span>

<span data-ttu-id="70bd7-104">Gibt für einen Medientyp an, ob die Stichproben eine festgelegte Größe aufweisen.</span><span class="sxs-lookup"><span data-stu-id="70bd7-104">Specifies for a media type whether the samples have a fixed size.</span></span>

## <a name="data-type"></a><span data-ttu-id="70bd7-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="70bd7-105">Data type</span></span>

<span data-ttu-id="70bd7-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="70bd7-106">**UINT32**</span></span>

<span data-ttu-id="70bd7-107">Als booleschen Wert behandeln.</span><span class="sxs-lookup"><span data-stu-id="70bd7-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="70bd7-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="70bd7-108">Remarks</span></span>

<span data-ttu-id="70bd7-109">Wenn dieses Attribut den Wert **true** hat, ist jede Stichprobe im Stream identisch mit der Größe (in Bytes).</span><span class="sxs-lookup"><span data-stu-id="70bd7-109">If this attribute is **TRUE**, every sample in the stream is the same size (in bytes).</span></span> <span data-ttu-id="70bd7-110">Andernfalls können sich die Größe von Beispielen unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="70bd7-110">Otherwise, samples might vary in size.</span></span>

<span data-ttu-id="70bd7-111">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="70bd7-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="70bd7-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="70bd7-112">Requirements</span></span>



| <span data-ttu-id="70bd7-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="70bd7-113">Requirement</span></span> | <span data-ttu-id="70bd7-114">Wert</span><span class="sxs-lookup"><span data-stu-id="70bd7-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="70bd7-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="70bd7-115">Minimum supported client</span></span><br/> | <span data-ttu-id="70bd7-116">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="70bd7-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="70bd7-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="70bd7-117">Minimum supported server</span></span><br/> | <span data-ttu-id="70bd7-118">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="70bd7-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="70bd7-119">Header</span><span class="sxs-lookup"><span data-stu-id="70bd7-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="70bd7-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="70bd7-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70bd7-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="70bd7-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70bd7-122">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="70bd7-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="70bd7-123">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="70bd7-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="70bd7-124">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="70bd7-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="70bd7-125">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="70bd7-125">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="70bd7-126">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="70bd7-126">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




