---
description: Gibt die Größe der einzelnen Stichproben in Bytes in einem Medientyp an.
ms.assetid: 4c28f73d-ff40-4eb9-a45f-57a60df719c6
title: MF_MT_SAMPLE_SIZE-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bb897524dac5f73f4d4553f8e77e02ef473f611
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368199"
---
# <a name="mf_mt_sample_size-attribute"></a><span data-ttu-id="68685-103">Attribut der MF \_ MT- \_ Stichproben \_ Größe</span><span class="sxs-lookup"><span data-stu-id="68685-103">MF\_MT\_SAMPLE\_SIZE attribute</span></span>

<span data-ttu-id="68685-104">Gibt die Größe der einzelnen Stichproben in Bytes in einem Medientyp an.</span><span class="sxs-lookup"><span data-stu-id="68685-104">Specifies the size of each sample, in bytes, in a media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="68685-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="68685-105">Data type</span></span>

<span data-ttu-id="68685-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="68685-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="68685-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="68685-107">Remarks</span></span>

<span data-ttu-id="68685-108">Dieses Attribut ist nur gültig, wenn das MF MT-Attribut " [**\_ \_ Fixed \_ size \_ Samples**](mf-mt-fixed-size-samples-attribute.md) " den Wert **true** hat.</span><span class="sxs-lookup"><span data-stu-id="68685-108">This attribute is valid only if the [**MF\_MT\_FIXED\_SIZE\_SAMPLES**](mf-mt-fixed-size-samples-attribute.md) attribute is **TRUE**.</span></span>

<span data-ttu-id="68685-109">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="68685-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="68685-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="68685-110">Requirements</span></span>



| <span data-ttu-id="68685-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="68685-111">Requirement</span></span> | <span data-ttu-id="68685-112">Wert</span><span class="sxs-lookup"><span data-stu-id="68685-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="68685-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="68685-113">Minimum supported client</span></span><br/> | <span data-ttu-id="68685-114">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="68685-114">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="68685-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="68685-115">Minimum supported server</span></span><br/> | <span data-ttu-id="68685-116">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="68685-116">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="68685-117">Header</span><span class="sxs-lookup"><span data-stu-id="68685-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="68685-118"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="68685-118"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68685-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="68685-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68685-120">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="68685-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="68685-121">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="68685-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="68685-122">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="68685-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="68685-123">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="68685-123">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="68685-124">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="68685-124">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




