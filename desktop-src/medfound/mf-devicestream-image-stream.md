---
description: Gibt an, ob ein Stream in einer Video Erfassungs Quelle ein Bild Datenstrom ist.
ms.assetid: 52251A45-3603-41C7-A869-7F6319BD337F
title: MF_DEVICESTREAM_IMAGE_STREAM-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 382ce587574d6ec46509a460dfb964e23dd416d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752448"
---
# <a name="mf_devicestream_image_stream-attribute"></a><span data-ttu-id="5d93a-103">MF- \_ devicestream \_ Image-Daten \_ Strom Attribut</span><span class="sxs-lookup"><span data-stu-id="5d93a-103">MF\_DEVICESTREAM\_IMAGE\_STREAM attribute</span></span>

<span data-ttu-id="5d93a-104">Gibt an, ob ein Stream in einer Video Erfassungs Quelle ein Bild Datenstrom ist.</span><span class="sxs-lookup"><span data-stu-id="5d93a-104">Specifies whether a stream on a video capture source is a still-image stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="5d93a-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="5d93a-105">Data type</span></span>

<span data-ttu-id="5d93a-106">**Bool** gespeichert als **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5d93a-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="5d93a-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5d93a-107">Remarks</span></span>

<span data-ttu-id="5d93a-108">Einige Videokameras machen einen noch Bild Datenstrom verfügbar, der hochauflösende Bilder erzeugt.</span><span class="sxs-lookup"><span data-stu-id="5d93a-108">Some video cameras expose a still-image stream that produces high-resolution images.</span></span> <span data-ttu-id="5d93a-109">Der Bildstream erzeugt möglicherweise unkomprimierte Bilder oder JPEG-Bilder.</span><span class="sxs-lookup"><span data-stu-id="5d93a-109">The image stream might produce uncompressed images or JPEG images.</span></span> <span data-ttu-id="5d93a-110">Wenn die Kamera über einen Bildstream verfügt, legt die Medienquelle für das Erfassungsgerät dieses Attribut für den Bildstream auf **true** fest.</span><span class="sxs-lookup"><span data-stu-id="5d93a-110">If the camera has an image stream, the media source for the capture device sets this attribute to **TRUE** on the image stream.</span></span>

<span data-ttu-id="5d93a-111">Gehen Sie folgendermaßen vor, um dieses Attribut zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="5d93a-111">To get this attribute, do the following:</span></span>

1.  <span data-ttu-id="5d93a-112">Fragen Sie die Medienquelle für die [**imfmediasourceex**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="5d93a-112">Query the media source for the [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) interface.</span></span>
2.  <span data-ttu-id="5d93a-113">Aufrufen von [**imfmediasourceex:: getstreamattributs**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) , um einen [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Zeiger für den Stream zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5d93a-113">Call [**IMFMediaSourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer for the stream.</span></span>
3.  <span data-ttu-id="5d93a-114">Zum Abrufen des Attributs muss [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="5d93a-114">Call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) to get the attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d93a-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5d93a-115">Requirements</span></span>



| <span data-ttu-id="5d93a-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5d93a-116">Requirement</span></span> | <span data-ttu-id="5d93a-117">Wert</span><span class="sxs-lookup"><span data-stu-id="5d93a-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5d93a-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5d93a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5d93a-119">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5d93a-119">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5d93a-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5d93a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5d93a-121">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5d93a-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5d93a-122">Header</span><span class="sxs-lookup"><span data-stu-id="5d93a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d93a-123"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d93a-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d93a-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5d93a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d93a-125">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="5d93a-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




