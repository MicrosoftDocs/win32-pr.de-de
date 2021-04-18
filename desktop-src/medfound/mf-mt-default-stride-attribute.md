---
description: Standard Oberflächen Stride für einen unkomprimierten Video Medientyp. Stride ist die Anzahl der Bytes, die erforderlich sind, um von einer Zeile aus Pixel zum nächsten zu wechseln.
ms.assetid: 71fda231-3497-49db-b82e-2fd79f6ade66
title: MF_MT_DEFAULT_STRIDE-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7b2b9633e14c8d414355ca41be29a9c6c2f8886
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215142"
---
# <a name="mf_mt_default_stride-attribute"></a><span data-ttu-id="b8138-104">MF \_ MT- \_ Standard-Stride- \_ Attribut</span><span class="sxs-lookup"><span data-stu-id="b8138-104">MF\_MT\_DEFAULT\_STRIDE attribute</span></span>

<span data-ttu-id="b8138-105">Standard Oberflächen Stride für einen unkomprimierten Video Medientyp.</span><span class="sxs-lookup"><span data-stu-id="b8138-105">Default surface stride, for an uncompressed video media type.</span></span> <span data-ttu-id="b8138-106">Stride ist die Anzahl der Bytes, die erforderlich sind, um von einer Zeile aus Pixel zum nächsten zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="b8138-106">Stride is the number of bytes needed to go from one row of pixels to the next.</span></span>

## <a name="data-type"></a><span data-ttu-id="b8138-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="b8138-107">Data type</span></span>

<span data-ttu-id="b8138-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="b8138-108">**UINT32**</span></span>

<span data-ttu-id="b8138-109">Als **Int32** -Wert behandeln.</span><span class="sxs-lookup"><span data-stu-id="b8138-109">Treat as a **INT32** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8138-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b8138-110">Remarks</span></span>

<span data-ttu-id="b8138-111">Der Attribut Wert wird als **UInt32** gespeichert, sollte jedoch in einen ganzzahligen Wert von 32-Bit-Ganzzahl umgewandelt werden.</span><span class="sxs-lookup"><span data-stu-id="b8138-111">The attribute value is stored as a **UINT32**, but should be cast to a 32-bit signed integer value.</span></span> <span data-ttu-id="b8138-112">Stride kann negativ sein.</span><span class="sxs-lookup"><span data-stu-id="b8138-112">Stride can be negative.</span></span>

<span data-ttu-id="b8138-113">Stride ist für Top-Down-Bilder positiv und negativ für Bild von unten nach oben.</span><span class="sxs-lookup"><span data-stu-id="b8138-113">Stride is positive for top-down images, and negative for bottom-up images.</span></span>

<span data-ttu-id="b8138-114">Dieses Attribut liefert den Schritt für eine zusammen *hängende* Darstellung des Bilds im Arbeitsspeicher. Das heißt, eine Darstellung ohne zusätzliche Auffüll Bytes nach jeder Zeile.</span><span class="sxs-lookup"><span data-stu-id="b8138-114">This attribute gives the stride for a *contiguous* representation of the image in memory; that is, a representation with no additional padding bytes after each row.</span></span> <span data-ttu-id="b8138-115">Wenn ein Medien Puffer die [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) -Schnittstelle unterstützt, verwenden Sie die [**IMF2DBuffer:: Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) -Methode, um den tatsächlichen Schritt der Oberfläche zu erhalten, der möglicherweise zusätzliche Leerzeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="b8138-115">If a media buffer supports the [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) interface, use the [**IMF2DBuffer::Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) method to get the actual stride of the surface, which might include extra padding bytes.</span></span>

<span data-ttu-id="b8138-116">Weitere Informationen zu Surface Stride finden Sie unter [Image Stride](image-stride.md).</span><span class="sxs-lookup"><span data-stu-id="b8138-116">For more information about surface stride, see [Image Stride](image-stride.md).</span></span>

<span data-ttu-id="b8138-117">Ein Beispiel für die Berechnung des Standard Schrittes finden Sie unter [nicht komprimierte Video Puffer](uncompressed-video-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="b8138-117">For an example of how to calculate the default stride, see [Uncompressed Video Buffers](uncompressed-video-buffers.md).</span></span>

<span data-ttu-id="b8138-118">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="b8138-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8138-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b8138-119">Requirements</span></span>



| <span data-ttu-id="b8138-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b8138-120">Requirement</span></span> | <span data-ttu-id="b8138-121">Wert</span><span class="sxs-lookup"><span data-stu-id="b8138-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b8138-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b8138-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b8138-123">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="b8138-123">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="b8138-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b8138-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b8138-125">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="b8138-125">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="b8138-126">Header</span><span class="sxs-lookup"><span data-stu-id="b8138-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8138-127"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8138-127"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8138-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b8138-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8138-129">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="b8138-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b8138-130">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="b8138-130">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="b8138-131">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="b8138-131">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="b8138-132">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="b8138-132">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="b8138-133">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="b8138-133">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="b8138-134">Bild Schritt</span><span class="sxs-lookup"><span data-stu-id="b8138-134">Image Stride</span></span>](image-stride.md)
</dt> </dl>

 

 




