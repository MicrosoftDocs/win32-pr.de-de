---
description: Gibt eine Zwischenrahmen Höhe für codiertes Video an.
ms.assetid: 7382ec31-6d59-4e8c-94eb-804786074038
title: MFPKEY_FORCEFRAMEHEIGHT-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8e4662ce56ea4c20d44abdd05641219bc6b94ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215515"
---
# <a name="mfpkey_forceframeheight-property"></a><span data-ttu-id="31e6f-103">Mfpkey \_ forceframeheight-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="31e6f-103">MFPKEY\_FORCEFRAMEHEIGHT Property</span></span>

<span data-ttu-id="31e6f-104">Gibt eine Zwischenrahmen Höhe für codiertes Video an.</span><span class="sxs-lookup"><span data-stu-id="31e6f-104">Specifies an intermediate frame height for encoded video.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="31e6f-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="31e6f-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="31e6f-106">g \_ wszwmvcforceframeheight</span><span class="sxs-lookup"><span data-stu-id="31e6f-106">g\_wszWMVCForceFrameHeight</span></span>

## <a name="data-type"></a><span data-ttu-id="31e6f-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="31e6f-107">Data Type</span></span>

<span data-ttu-id="31e6f-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="31e6f-108">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="31e6f-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="31e6f-109">Remarks</span></span>

<span data-ttu-id="31e6f-110">Sie können diesen Wert und die Eigenschaft [mfpkey \_ forceframewidth](mfpkey-forceframewidthproperty.md) festlegen, um zu erzwingen, dass der Encoder den Videostream mit einer Frame Größe codiert, die kleiner als die Eingabe-oder Ausgabe Frame Größen ist.</span><span class="sxs-lookup"><span data-stu-id="31e6f-110">You can set this value and the [MFPKEY\_FORCEFRAMEWIDTH](mfpkey-forceframewidthproperty.md) property to force the encoder to encode the video stream with a frame size that is smaller than the input or output frame sizes.</span></span> <span data-ttu-id="31e6f-111">Beim decodierten wird die Größe des Videos an die ursprüngliche Eingabe Auflösung angepasst.</span><span class="sxs-lookup"><span data-stu-id="31e6f-111">When decoded, the video will be resized to its original input resolution.</span></span>

<span data-ttu-id="31e6f-112">Gültige Frame Dimensionen auf beiden Achsen sind 2 bis 8192 Pixel.</span><span class="sxs-lookup"><span data-stu-id="31e6f-112">Valid frame dimensions on either axis are 2 to 8192 pixels.</span></span> <span data-ttu-id="31e6f-113">Frame Dimensionen müssen durch 2 teilbar sein.</span><span class="sxs-lookup"><span data-stu-id="31e6f-113">Frame dimensions must be divisible by 2.</span></span>

## <a name="requirements"></a><span data-ttu-id="31e6f-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="31e6f-114">Requirements</span></span>



| <span data-ttu-id="31e6f-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="31e6f-115">Requirement</span></span> | <span data-ttu-id="31e6f-116">Wert</span><span class="sxs-lookup"><span data-stu-id="31e6f-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="31e6f-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="31e6f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="31e6f-118">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="31e6f-118">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="31e6f-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="31e6f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="31e6f-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="31e6f-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="31e6f-121">Header</span><span class="sxs-lookup"><span data-stu-id="31e6f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="31e6f-122"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="31e6f-122"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31e6f-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="31e6f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31e6f-124">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="31e6f-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




