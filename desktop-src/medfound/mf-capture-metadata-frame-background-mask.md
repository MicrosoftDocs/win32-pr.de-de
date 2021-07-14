---
description: Meldet die Metadaten und den Maskenpuffer für eine Hintergrundsegmentierungsmaske, die zwischen Hintergrund und Vordergrund eines Videoframes unterscheidet.
title: MF_CAPTURE_METADATA_FRAME_BACKGROUND_MASK-Attribut (Mfapi.h)
ms.topic: reference
ms.date: 06/01/2021
ms.openlocfilehash: 3dc28d92566b14a44f61fe84bd3f68688c464d4a
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691849"
---
# <a name="mf_capture_metadata_frame_background_mask-attribute"></a><span data-ttu-id="7f867-103">MF \_ CAPTURE METADATA FRAME BACKGROUND \_ \_ \_ \_ MASK-Attribut</span><span class="sxs-lookup"><span data-stu-id="7f867-103">MF\_CAPTURE\_METADATA\_FRAME\_BACKGROUND\_MASK attribute</span></span>

<span data-ttu-id="7f867-104">Meldet die Metadaten und den Maskenpuffer für eine Hintergrundsegmentierungsmaske, die zwischen Hintergrund und Vordergrund eines Videoframes unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="7f867-104">Reports the metadata and mask buffer for a background segmentation mask that distinguishes between the background and foreground of a video frame.</span></span>

## <a name="data-type"></a><span data-ttu-id="7f867-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="7f867-105">Data type</span></span>

<span data-ttu-id="7f867-106">**Blob**</span><span class="sxs-lookup"><span data-stu-id="7f867-106">**BLOB**</span></span>

## <a name="remarks"></a><span data-ttu-id="7f867-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7f867-107">Remarks</span></span>

<span data-ttu-id="7f867-108">Die von diesem Attribut [](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-kscamera_metadata_backgroundsegmentationmask) übertragenen Daten sind eine KSCAMERA_METADATA_BACKGROUNDSEGMENTATIONMASK-Struktur, die Informationen über die Abmessungen der Hintergrundmaske sowie die Abdeckung des Frames enthält, aus dem sie abgeleitet werden. Dies ist der Frame, der vom Stream ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7f867-108">The data carried by this attribute is a [KSCAMERA_METADATA_BACKGROUNDSEGMENTATIONMASK](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-kscamera_metadata_backgroundsegmentationmask) structure that contains information about the dimensions of the background mask as well as its coverage of the frame it is inferred from, which is the frame that is outputted by the stream.</span></span> <span data-ttu-id="7f867-109">Sie enthält auch einen zusammenhängenden Puffer, der die Maske darstellt, die von der nutzenden App genutzt werden soll, um zu definieren, welche Pixel als Teil des Vordergrunds oder Hintergrunds betrachtet werden.</span><span class="sxs-lookup"><span data-stu-id="7f867-109">It also carries a contiguous buffer representing the mask to be leveraged by the consuming app to define which pixels are considered part of the foreground or background.</span></span> <span data-ttu-id="7f867-110">Die Skalierungs- und Bildkoordinatenkorrelation der Maske in Bezug auf den Frame wird von der nutzenden App verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="7f867-110">The scaling and image coordinate correlation of the mask regarding the frame is handled by the consuming app.</span></span> 

## <a name="requirements"></a><span data-ttu-id="7f867-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7f867-111">Requirements</span></span>



| <span data-ttu-id="7f867-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7f867-112">Requirement</span></span> | <span data-ttu-id="7f867-113">Wert</span><span class="sxs-lookup"><span data-stu-id="7f867-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7f867-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7f867-114">Minimum supported client</span></span><br/> | <span data-ttu-id="7f867-115">Windows Build 22000t</span><span class="sxs-lookup"><span data-stu-id="7f867-115">Windows Build 22000t</span></span><br/>                          |
| <span data-ttu-id="7f867-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7f867-116">Minimum supported server</span></span><br/> | <span data-ttu-id="7f867-117">Windows Build 22000</span><span class="sxs-lookup"><span data-stu-id="7f867-117">Windows Build 22000</span></span><br/>                      |
| <span data-ttu-id="7f867-118">Header</span><span class="sxs-lookup"><span data-stu-id="7f867-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f867-119"><dt>Mfapi.h</dt></span><span class="sxs-lookup"><span data-stu-id="7f867-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f867-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7f867-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f867-121">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="7f867-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7f867-122">**ATTRIBUTEAttributes::GetBlob**</span><span class="sxs-lookup"><span data-stu-id="7f867-122">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="7f867-123">**ATTRIBUTEAttributes::SetBlob**</span><span class="sxs-lookup"><span data-stu-id="7f867-123">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="7f867-124">**ARCHEMEDIATYPE**</span><span class="sxs-lookup"><span data-stu-id="7f867-124">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="7f867-125">Medientypattribute</span><span class="sxs-lookup"><span data-stu-id="7f867-125">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 




