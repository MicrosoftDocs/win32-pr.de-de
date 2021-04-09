---
description: Gibt die Frame Typen (I, P oder B) an, auf die der quantifizierungsparameter (QP) angewendet wird.
ms.assetid: 6331033F-7EEB-41B3-B166-29686D4AADB6
title: CODECAPI_AVEncVideoEncodeFrameTypeQP-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76e68e0cb6cbdc076dbf523f3ae9dfd7b5870f47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127976"
---
# <a name="codecapi_avencvideoencodeframetypeqp-property"></a><span data-ttu-id="93685-103">Codecapi \_ avencvideoencodeframetypeqp (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="93685-103">CODECAPI\_AVEncVideoEncodeFrameTypeQP property</span></span>

<span data-ttu-id="93685-104">Gibt die Frame Typen (I, P oder B) an, auf die der quantifizierungsparameter (QP) angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="93685-104">Specifies the frame types (I, P, or B) that the quantization parameter (QP) is applied to.</span></span>

## <a name="data-type"></a><span data-ttu-id="93685-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="93685-105">Data type</span></span>

<span data-ttu-id="93685-106">**Ulongulong** (VT \_ UI8)</span><span class="sxs-lookup"><span data-stu-id="93685-106">**ULONGULONG** (VT\_UI8)</span></span>

## <a name="property-guid"></a><span data-ttu-id="93685-107">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="93685-107">Property GUID</span></span>

<span data-ttu-id="93685-108">**Codecapi \_ avencvideoencodeframetypeqp**</span><span class="sxs-lookup"><span data-stu-id="93685-108">**CODECAPI\_AVEncVideoEncodeFrameTypeQP**</span></span>

## <a name="remarks"></a><span data-ttu-id="93685-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="93685-109">Remarks</span></span>

<span data-ttu-id="93685-110">Bei Encodern, die das Festlegen eines quantisierungsparameters (QP) für verschiedene Frame Typen (I, P, B) unterstützen, müssen Sie diese API zusätzlich zu [codecapi \_ avencvideoencodeqp](codecapi-avencvideoencodeqp.md)verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="93685-110">For encoders which support setting a quantization parameter (QP) for different frame types (I, P, B), they shall expose this API in addition to [CODECAPI\_AVEncVideoEncodeQP](codecapi-avencvideoencodeqp.md).</span></span> <span data-ttu-id="93685-111">Wenn ein Encoder nur ein einzelnes QP für alle Frame Typen unterstützt, darf er nur codecapi \_ avencvideoencodeqp unterstützen.</span><span class="sxs-lookup"><span data-stu-id="93685-111">If an encoder supports only a single QP for all frame types, they shall support only CODECAPI\_AVEncVideoEncodeQP.</span></span>

<span data-ttu-id="93685-112">Dies ist eine dynamische Codierungs Eigenschaft, die bedeutet, dass ein neuer Wert während der Codierungs Sitzung jederzeit festgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="93685-112">This is a dynamic encoding property meaning that a new value can be set any time during the encoding session.</span></span>

<span data-ttu-id="93685-113">**H. 264/AVC-Encoder:**</span><span class="sxs-lookup"><span data-stu-id="93685-113">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="93685-114">Der Encoder muss " [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue)", " [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)" und " [**getparameterrange**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange)" unterstützen.</span><span class="sxs-lookup"><span data-stu-id="93685-114">Encoder shall support [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue), and [**GetParameterRange**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

<span data-ttu-id="93685-115">Ein Satz von 4 16-Bit-Feldern wird verwendet, um die Frame-QPS in der Fixed-QP-Codierung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="93685-115">A set of four 16-bit fields are used to specify the frame QPs in fixed-QP encoding.</span></span> <span data-ttu-id="93685-116">Die Felder lauten:</span><span class="sxs-lookup"><span data-stu-id="93685-116">The fields are:</span></span>

-   <span data-ttu-id="93685-117">**Bits 0-15:** Für I-Frames verwendeter QP, gültiger Bereich von \[ 0, 51 \] .</span><span class="sxs-lookup"><span data-stu-id="93685-117">**Bits 0-15:** QP used for I frames, valid range \[0, 51\].</span></span>
-   <span data-ttu-id="93685-118">**Bits 16-31:** Für P-Frames verwendeter QP, gültiger Bereich von \[ 0, 51 \] .</span><span class="sxs-lookup"><span data-stu-id="93685-118">**Bits 16-31:** QP used for P frames, valid range \[0, 51\].</span></span>
-   <span data-ttu-id="93685-119">**Bits 32-47:** Für B-Frames verwendeter QP, gültiger Bereich von \[ 0, 51\]</span><span class="sxs-lookup"><span data-stu-id="93685-119">**Bits 32-47:** QP used for B frames, valid range \[0, 51\]</span></span>
-   <span data-ttu-id="93685-120">**Bits 48-63:** reserviert</span><span class="sxs-lookup"><span data-stu-id="93685-120">**Bits 48-63:** reserved</span></span>

<span data-ttu-id="93685-121">Wenn diese codecapi unterstützt wird, unterstützen Encoder die QP-Einstellungen für den Frame-Typ I, P und B.</span><span class="sxs-lookup"><span data-stu-id="93685-121">When this CodecAPI is supported, encoders shall support QP setting on frame type of I, P, and B.</span></span>

<span data-ttu-id="93685-122">Der Standardwert muss 0x0000001a001a001a lauten.</span><span class="sxs-lookup"><span data-stu-id="93685-122">Default value shall be 0x0000001a001a001a.</span></span> <span data-ttu-id="93685-123">QP ist gleich 26 für I, P und B.</span><span class="sxs-lookup"><span data-stu-id="93685-123">QP equal to 26 for I, P and B.</span></span>

<span data-ttu-id="93685-124">Wenn [codecapi \_ avencvideoselectlayer](codecapi-avencvideoselectlayer.md) eine bestimmte temporale Ebene auswählt, muss [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue) von codecapi \_ avencvideoencodeframetypeqp QP für I-, P-und B-Frames auf dieser temporalen Ebene festlegen.</span><span class="sxs-lookup"><span data-stu-id="93685-124">When [CODECAPI\_AVEncVideoSelectLayer](codecapi-avencvideoselectlayer.md) selects a specific temporal layer, [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue) of CODECAPI\_AVEncVideoEncodeFrameTypeQP shall set QP for I, P, and B frames on that temporal layer.</span></span> <span data-ttu-id="93685-125">Standardmäßig wird QP für I-, P-und B-Frames auf der temporalen Ebene 0 für temporale Temporale Ebenen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="93685-125">By default, it sets QP for I, P, and B frames on base temporal layer temporal layer 0.</span></span>

<span data-ttu-id="93685-126">[Codecapi \_ Mithilfe von "avencvideomaxqp](codecapi-avencvideomaxqp.md) " und " [codecapi \_ avencvideominqp](codecapi-avencvideominqp.md) " können Sie den QP-Bereich für QPS aller Bildtypen (I, P und B) definieren und begrenzen.</span><span class="sxs-lookup"><span data-stu-id="93685-126">[CODECAPI\_AVEncVideoMaxQP](codecapi-avencvideomaxqp.md) and [CODECAPI\_AVEncVideoMinQP](codecapi-avencvideominqp.md) shall be used to define and limit the QP range for QPs of all picture types, I, P and B.</span></span>

## <a name="requirements"></a><span data-ttu-id="93685-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="93685-127">Requirements</span></span>



| <span data-ttu-id="93685-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="93685-128">Requirement</span></span> | <span data-ttu-id="93685-129">Wert</span><span class="sxs-lookup"><span data-stu-id="93685-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="93685-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="93685-130">Minimum supported client</span></span><br/> | <span data-ttu-id="93685-131">Windows 8.1 \[ Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="93685-131">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="93685-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="93685-132">Minimum supported server</span></span><br/> | <span data-ttu-id="93685-133">Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="93685-133">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="93685-134">Header</span><span class="sxs-lookup"><span data-stu-id="93685-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="93685-135"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="93685-135"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93685-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="93685-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93685-137">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="93685-137">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

