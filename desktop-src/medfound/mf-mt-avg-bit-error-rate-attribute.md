---
description: Datenfehler Rate in Bitfehlern pro Sekunde für einen Video Medientyp.
ms.assetid: 90433ff4-a563-4751-86d9-caac0cc58194
title: MF_MT_AVG_BIT_ERROR_RATE-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21eb33d1bc1636dd047dbd56ce6b7ad3a683f356
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215143"
---
# <a name="mf_mt_avg_bit_error_rate-attribute"></a><span data-ttu-id="f93cd-103">\_ \_ \_ \_ Fehler \_ Raten Attribut für MF MT-Durchschnittl.</span><span class="sxs-lookup"><span data-stu-id="f93cd-103">MF\_MT\_AVG\_BIT\_ERROR\_RATE attribute</span></span>

<span data-ttu-id="f93cd-104">Datenfehler Rate in Bitfehlern pro Sekunde für einen Video Medientyp.</span><span class="sxs-lookup"><span data-stu-id="f93cd-104">Data error rate, in bit errors per second, for a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="f93cd-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="f93cd-105">Data type</span></span>

<span data-ttu-id="f93cd-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="f93cd-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="f93cd-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f93cd-107">Remarks</span></span>

<span data-ttu-id="f93cd-108">Dieses Attribut entspricht dem **dwbiterrorrate** -Member der [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -und [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="f93cd-108">This attribute corresponds to the **dwBitErrorRate** member of the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) and [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) structures.</span></span>

<span data-ttu-id="f93cd-109">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="f93cd-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="f93cd-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f93cd-110">Requirements</span></span>



| <span data-ttu-id="f93cd-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f93cd-111">Requirement</span></span> | <span data-ttu-id="f93cd-112">Wert</span><span class="sxs-lookup"><span data-stu-id="f93cd-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f93cd-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f93cd-113">Minimum supported client</span></span><br/> | <span data-ttu-id="f93cd-114">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="f93cd-114">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="f93cd-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f93cd-115">Minimum supported server</span></span><br/> | <span data-ttu-id="f93cd-116">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="f93cd-116">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="f93cd-117">Header</span><span class="sxs-lookup"><span data-stu-id="f93cd-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="f93cd-118"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f93cd-118"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f93cd-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f93cd-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f93cd-120">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="f93cd-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f93cd-121">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="f93cd-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="f93cd-122">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="f93cd-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="f93cd-123">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="f93cd-123">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="f93cd-124">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="f93cd-124">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
