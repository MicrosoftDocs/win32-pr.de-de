---
description: Gibt die Breite und Höhe des codierten Videos an, wenn das Video zugeschnitten ist.
ms.assetid: d6217250-63ff-4dff-a357-ff4aaa764695
title: Avencvideoencodedimension-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f63d0a5c0d1c6af7c20620c315ad25c16eac528
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106341090"
---
# <a name="avencvideoencodedimension-property"></a><span data-ttu-id="1e4d1-103">Avencvideoencodedimension (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="1e4d1-103">AVEncVideoEncodeDimension property</span></span>

<span data-ttu-id="1e4d1-104">Gibt die Breite und Höhe des codierten Videos an, wenn das Video zugeschnitten ist.</span><span class="sxs-lookup"><span data-stu-id="1e4d1-104">Specifies the width and height of the encoded video, if the video is cropped.</span></span>

<span data-ttu-id="1e4d1-105">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="1e4d1-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="1e4d1-106">Datentyp</span><span class="sxs-lookup"><span data-stu-id="1e4d1-106">Data type</span></span>

<span data-ttu-id="1e4d1-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="1e4d1-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="1e4d1-108">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="1e4d1-108">Property GUID</span></span>

<span data-ttu-id="1e4d1-109">**Codecapi \_ avencvideoencodedimension**</span><span class="sxs-lookup"><span data-stu-id="1e4d1-109">**CODECAPI\_AVEncVideoEncodeDimension**</span></span>

## <a name="property-value"></a><span data-ttu-id="1e4d1-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="1e4d1-110">Property value</span></span>

<span data-ttu-id="1e4d1-111">Die oberen 16 Bits des Werts enthalten die Breite in Pixel, die unteren 16 Bits enthalten die Höhe in Pixel.</span><span class="sxs-lookup"><span data-stu-id="1e4d1-111">The upper 16 bits of the value contain the width in pixels, and the lower 16 bits contain the height in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e4d1-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1e4d1-112">Remarks</span></span>

<span data-ttu-id="1e4d1-113">Anwendungen können diese Eigenschaft festlegen, um das Eingabe Video Zuschneiden.</span><span class="sxs-lookup"><span data-stu-id="1e4d1-113">Applications can set this property to crop the input video.</span></span> <span data-ttu-id="1e4d1-114">Die angegebene Größe muss kleiner sein als die Größe der Eingabe Video Frames.</span><span class="sxs-lookup"><span data-stu-id="1e4d1-114">The specified size must be less than the size of the input video frames.</span></span> <span data-ttu-id="1e4d1-115">Verwenden Sie die Eigenschaft " [**avencvideoencodeoffsetorigin**](avencvideoencodeoffsetorigin-property.md) ", um die linke und die obere Ecke des clippingrechtecks anzugeben.</span><span class="sxs-lookup"><span data-stu-id="1e4d1-115">Use the [**AVEncVideoEncodeOffsetOrigin**](avencvideoencodeoffsetorigin-property.md) property to specify the left and top corners of the clipping rectangle.</span></span>

<span data-ttu-id="1e4d1-116">Encoder können diese Eigenschaft als Funktion zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="1e4d1-116">Encoders can return this property as a capability.</span></span>

<span data-ttu-id="1e4d1-117">Diese Eigenschaft wird auch mit [H. 264 UVC 1,5-Kamera Codierern](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5)verwendet.</span><span class="sxs-lookup"><span data-stu-id="1e4d1-117">This property is also used with [H.264 UVC 1.5 camera encoders](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).</span></span>

<span data-ttu-id="1e4d1-118">Für UVC 1,5-Kamera Encoder wird " [avencvideoencodeoffot torigin](avencvideoencodeoffsetorigin-property.md) " nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1e4d1-118">For UVC 1.5 camera encoders, [AVEncVideoEncodeOffsetOrigin](avencvideoencodeoffsetorigin-property.md) is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e4d1-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1e4d1-119">Requirements</span></span>



| <span data-ttu-id="1e4d1-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1e4d1-120">Requirement</span></span> | <span data-ttu-id="1e4d1-121">Wert</span><span class="sxs-lookup"><span data-stu-id="1e4d1-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1e4d1-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1e4d1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1e4d1-123">Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="1e4d1-123">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="1e4d1-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1e4d1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1e4d1-125">Windows 2000 Server \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="1e4d1-125">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="1e4d1-126">Header</span><span class="sxs-lookup"><span data-stu-id="1e4d1-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e4d1-127"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e4d1-127"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e4d1-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e4d1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e4d1-129">Eigenschaften der Codec-API</span><span class="sxs-lookup"><span data-stu-id="1e4d1-129">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="1e4d1-130">**Icodecapi-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="1e4d1-130">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

