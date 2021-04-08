---
description: Gibt an, ob ein Decoder vor anderen Formaten IYUV/I420-Ausgabetypen (für die Transcodierung geeignet) verfügbar macht.
ms.assetid: 8505CFA1-210A-4DA8-B92A-FCE62F0310E5
title: MFT_DECODER_EXPOSE_OUTPUT_TYPES_IN_NATIVE_ORDER-Attribut (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01ecf074fa0767552a48e3238374dbd02f077404
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755280"
---
# <a name="mft_decoder_expose_output_types_in_native_order-attribute"></a><span data-ttu-id="a5665-103">MFT- \_ Decoder macht \_ \_ Ausgabe \_ Typen im systemeigenen \_ \_ \_ Order-Attribut verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a5665-103">MFT\_DECODER\_EXPOSE\_OUTPUT\_TYPES\_IN\_NATIVE\_ORDER attribute</span></span>

<span data-ttu-id="a5665-104">Gibt an, ob ein Decoder vor anderen Formaten IYUV/I420-Ausgabetypen (für die Transcodierung geeignet) verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="a5665-104">Specifies whether a decoder exposes IYUV/I420 output types (suitable for transcoding) before other formats.</span></span>

## <a name="data-type"></a><span data-ttu-id="a5665-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="a5665-105">Data type</span></span>

<span data-ttu-id="a5665-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="a5665-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="a5665-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a5665-107">Remarks</span></span>

<span data-ttu-id="a5665-108">Dieses Attribut ist ein Hinweis für den Decoder, seine Liste der Ausgabetypen in einer bestimmten Reihenfolge anzuordnen, abhängig von der vorgesehenen Verwendung, entweder Wiedergabe oder transcode.</span><span class="sxs-lookup"><span data-stu-id="a5665-108">This attribute is a hint for the decoder to arrange its list of output types in a particular order, depending on the intended use, either playback or transcode.</span></span>

<span data-ttu-id="a5665-109">Bei den meisten Codierungs Formaten (H. 264, MPEG-2, WMV) unterstützen die Video-Decoder in Microsoft Media Foundation mehrere allgemeine YUV-Ausgaben, einschließlich NV12, YV12, im YUY2, IYUV und I420.</span><span class="sxs-lookup"><span data-stu-id="a5665-109">For most encoding formats (H.264, MPEG-2, WMV), the video decoders in Microsoft Media Foundation support several common YUV outputs, including NV12, YV12, YUY2, IYUV, and I420.</span></span> <span data-ttu-id="a5665-110">Der Decoder bietet mithilfe der [**imftransform:: getoutputavailabletype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) -Methode eine geordnete Liste von Ausgabetypen.</span><span class="sxs-lookup"><span data-stu-id="a5665-110">The decoder offers an ordered list of output types through its [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) method.</span></span>

<span data-ttu-id="a5665-111">Für die Wiedergabe ist NV12 das effizienteste und unterschiedlichste Format.</span><span class="sxs-lookup"><span data-stu-id="a5665-111">For playback, NV12 is the most efficient and widely supported format.</span></span> <span data-ttu-id="a5665-112">Daher bieten Decoder standardmäßig NV12 als ersten Ausgabetyp in der Liste an.</span><span class="sxs-lookup"><span data-stu-id="a5665-112">Therefore, by default, decoders typically offer NV12 as the first output type in the list.</span></span> <span data-ttu-id="a5665-113">Dadurch wird die zum Auflösen des Medientyps erforderliche Zeit minimiert, wenn eine Wiedergabe Topologie aufgebaut wird.</span><span class="sxs-lookup"><span data-stu-id="a5665-113">This minimizes the time needed to resolve the media type when building a playback topology.</span></span> <span data-ttu-id="a5665-114">Bei der Transcodierung sind IYUV oder I420 jedoch für die CPU effizienter und werden in der Regel von Encodern bevorzugt.</span><span class="sxs-lookup"><span data-stu-id="a5665-114">For transcoding, however, IYUV or I420 are more efficient for the CPU and are typically preferred by encoders.</span></span>

<span data-ttu-id="a5665-115">Wenn ein Decoder dieses Attribut unterstützt, weist das Attribut folgendes Verhalten auf:</span><span class="sxs-lookup"><span data-stu-id="a5665-115">If a decoder supports this attribute, the attribute has the following behavior:</span></span>

-   <span data-ttu-id="a5665-116">Wenn das Attribut einen Wert ungleich 0 (null) aufweist, werden IYUV und I420 zuerst in der Liste der Ausgabemedien Typen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a5665-116">If the attribute has a non-zero value, IYUV and I420 appear first in the list of output media types.</span></span> <span data-ttu-id="a5665-117">Diese Einstellung ist für die Transcodierung am effizientesten.</span><span class="sxs-lookup"><span data-stu-id="a5665-117">This setting is most efficient for transcoding.</span></span>
-   <span data-ttu-id="a5665-118">Wenn das-Attribut 0 (null) ist, wird NV12 zuerst in der Liste der Ausgabemedien Typen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a5665-118">If the attribute is zero, NV12 appears first in the list of output media types.</span></span> <span data-ttu-id="a5665-119">Diese Einstellung ist für die Wiedergabe am effizientesten und ist die Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="a5665-119">This setting is most efficient for playback, and is the default.</span></span>

<span data-ttu-id="a5665-120">So legen Sie dieses Attribut fest:</span><span class="sxs-lookup"><span data-stu-id="a5665-120">To set this attribute:</span></span>

1.  <span data-ttu-id="a5665-121">Aufrufen von [**imftransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) für den Decoder zum Abrufen eines [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Zeigers.</span><span class="sxs-lookup"><span data-stu-id="a5665-121">Call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) on the decoder to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer.</span></span>
2.  <span data-ttu-id="a5665-122">Zum Hinzufügen des Attributs wird [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="a5665-122">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) to add the attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5665-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a5665-123">Requirements</span></span>



| <span data-ttu-id="a5665-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a5665-124">Requirement</span></span> | <span data-ttu-id="a5665-125">Wert</span><span class="sxs-lookup"><span data-stu-id="a5665-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5665-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a5665-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a5665-127">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="a5665-127">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="a5665-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a5665-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a5665-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a5665-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="a5665-130">Header</span><span class="sxs-lookup"><span data-stu-id="a5665-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5665-131"><dt>"MF Transform. h"</dt></span><span class="sxs-lookup"><span data-stu-id="a5665-131"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5665-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a5665-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5665-133">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="a5665-133">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




