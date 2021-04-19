---
description: Gibt an, ob der Bildstream in einer Video Erfassungs Quelle unabhängig vom Videostream ist.
ms.assetid: DC4ED612-593B-40BF-BB42-946149042D1F
title: MF_DEVICESTREAM_INDEPENDENT_IMAGE_STREAM-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 174e62a1bdd178ad2d8dce7fab5bf9ce3104d834
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353196"
---
# <a name="mf_devicestream_independent_image_stream-attribute"></a><span data-ttu-id="73c11-103">Das MF- \_ Attribut "devicestream \_ Independent \_ Image \_ Stream"</span><span class="sxs-lookup"><span data-stu-id="73c11-103">MF\_DEVICESTREAM\_INDEPENDENT\_IMAGE\_STREAM attribute</span></span>

<span data-ttu-id="73c11-104">Gibt an, ob der Bildstream in einer Video Erfassungs Quelle unabhängig vom Videostream ist.</span><span class="sxs-lookup"><span data-stu-id="73c11-104">Specifies whether the image stream on a video capture source is independent of the video stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="73c11-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="73c11-105">Data type</span></span>

<span data-ttu-id="73c11-106">**Bool** gespeichert als **UInt32**</span><span class="sxs-lookup"><span data-stu-id="73c11-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="73c11-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="73c11-107">Remarks</span></span>

<span data-ttu-id="73c11-108">Einige USB-Videokameras machen einen Stream verfügbar, der weiterhin Bilder erzeugt.</span><span class="sxs-lookup"><span data-stu-id="73c11-108">Some USB video cameras expose a stream that produces still images.</span></span> <span data-ttu-id="73c11-109">In einigen Kameras gibt der Bildstream einfach den nächsten Frame aus dem Videostream zurück.</span><span class="sxs-lookup"><span data-stu-id="73c11-109">In some cameras, the image stream simply returns the next frame from the video stream.</span></span> <span data-ttu-id="73c11-110">In anderen Kameras funktioniert der Bildstream unabhängig vom Videostream.</span><span class="sxs-lookup"><span data-stu-id="73c11-110">In other cameras, the image stream functions independently of the video stream.</span></span> <span data-ttu-id="73c11-111">Wenn die Kamera über einen unabhängigen Bildstream verfügt, legt die Medienquelle für das Erfassungsgerät dieses Attribut für den Bildstream auf **true** fest.</span><span class="sxs-lookup"><span data-stu-id="73c11-111">If the camera has an independent image stream, the media source for the capture device sets this attribute to **TRUE** on the image stream.</span></span>

<span data-ttu-id="73c11-112">Gehen Sie folgendermaßen vor, um dieses Attribut zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="73c11-112">To get this attribute, do the following:</span></span>

1.  <span data-ttu-id="73c11-113">Fragen Sie die Medienquelle für die [**imfmediasourceex**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="73c11-113">Query the media source for the [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) interface.</span></span>
2.  <span data-ttu-id="73c11-114">Aufrufen von [**imfmediasourceex:: getstreamattributs**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) , um einen [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Zeiger für den Stream zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="73c11-114">Call [**IMFMediaSourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer for the stream.</span></span>
3.  <span data-ttu-id="73c11-115">Zum Abrufen des Attributs muss [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="73c11-115">Call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) to get the attribute.</span></span>

<span data-ttu-id="73c11-116">Dieses Attribut gilt nur, wenn das MF-Attribut " [ \_ devicestream \_ Image \_ Stream](mf-devicestream-image-stream.md) " den Wert **true** hat.</span><span class="sxs-lookup"><span data-stu-id="73c11-116">This attribute applies only when the [MF\_DEVICESTREAM\_IMAGE\_STREAM](mf-devicestream-image-stream.md) attribute is **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="73c11-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="73c11-117">Requirements</span></span>



| <span data-ttu-id="73c11-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="73c11-118">Requirement</span></span> | <span data-ttu-id="73c11-119">Wert</span><span class="sxs-lookup"><span data-stu-id="73c11-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="73c11-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="73c11-120">Minimum supported client</span></span><br/> | <span data-ttu-id="73c11-121">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="73c11-121">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="73c11-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="73c11-122">Minimum supported server</span></span><br/> | <span data-ttu-id="73c11-123">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="73c11-123">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="73c11-124">Header</span><span class="sxs-lookup"><span data-stu-id="73c11-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="73c11-125"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="73c11-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73c11-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="73c11-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73c11-127">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="73c11-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




