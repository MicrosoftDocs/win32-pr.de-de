---
description: Gibt die linke und die obere Ecke des clippingrechtecks an, wenn das Video zugeschnitten ist.
ms.assetid: 8ce8b3b8-dd91-41e1-a4ba-b0c2d9d0edd2
title: Avencvideoencodeoffctorigin-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7db4d685942b8c21f2d5047003f2172c54b1d50d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124226"
---
# <a name="avencvideoencodeoffsetorigin-property"></a><span data-ttu-id="12d05-103">Avencvideoencodeoffctorigin (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="12d05-103">AVEncVideoEncodeOffsetOrigin property</span></span>

<span data-ttu-id="12d05-104">Gibt die linke und die obere Ecke des clippingrechtecks an, wenn das Video zugeschnitten ist.</span><span class="sxs-lookup"><span data-stu-id="12d05-104">Specifies the left and top corners of the clipping rectangle, if the video is cropped.</span></span>

<span data-ttu-id="12d05-105">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="12d05-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="12d05-106">Datentyp</span><span class="sxs-lookup"><span data-stu-id="12d05-106">Data type</span></span>

<span data-ttu-id="12d05-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="12d05-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="12d05-108">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="12d05-108">Property GUID</span></span>

<span data-ttu-id="12d05-109">**Codecapi \_ avencvideoencodeoffantorigin**</span><span class="sxs-lookup"><span data-stu-id="12d05-109">**CODECAPI\_AVEncVideoEncodeOffsetOrigin**</span></span>

## <a name="property-value"></a><span data-ttu-id="12d05-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="12d05-110">Property value</span></span>

<span data-ttu-id="12d05-111">Die oberen 16 Bits des Werts enthalten den Offset vom linken Rand des Eingabe Rahmens in Pixel.</span><span class="sxs-lookup"><span data-stu-id="12d05-111">The upper 16 bits of the value contain the offset from the left edge of the input frame, in pixels.</span></span> <span data-ttu-id="12d05-112">Die unteren 16 Bits enthalten den Offset vom oberen Rand des Eingabe Rahmens in Pixel.</span><span class="sxs-lookup"><span data-stu-id="12d05-112">The lower 16 bits contain the offset from the top edge of the input frame, in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="12d05-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="12d05-113">Remarks</span></span>

<span data-ttu-id="12d05-114">Anwendungen können diese Eigenschaft festlegen, um das Eingabe Video Zuschneiden.</span><span class="sxs-lookup"><span data-stu-id="12d05-114">Applications can set this property to crop the input video.</span></span> <span data-ttu-id="12d05-115">Verwenden Sie die Eigenschaft " [**avencvideoencodedimension**](avencvideoencodedimension-property.md) ", um die Breite und Höhe des clippingrechtecks anzugeben.</span><span class="sxs-lookup"><span data-stu-id="12d05-115">Use the [**AVEncVideoEncodeDimension**](avencvideoencodedimension-property.md) property to specify the width and height of the clipping rectangle.</span></span>

## <a name="requirements"></a><span data-ttu-id="12d05-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="12d05-116">Requirements</span></span>



| <span data-ttu-id="12d05-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="12d05-117">Requirement</span></span> | <span data-ttu-id="12d05-118">Wert</span><span class="sxs-lookup"><span data-stu-id="12d05-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="12d05-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="12d05-119">Minimum supported client</span></span><br/> | <span data-ttu-id="12d05-120">Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="12d05-120">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="12d05-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="12d05-121">Minimum supported server</span></span><br/> | <span data-ttu-id="12d05-122">Windows 2000 Server \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="12d05-122">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="12d05-123">Header</span><span class="sxs-lookup"><span data-stu-id="12d05-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="12d05-124"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="12d05-124"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12d05-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="12d05-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12d05-126">Eigenschaften der Codec-API</span><span class="sxs-lookup"><span data-stu-id="12d05-126">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="12d05-127">**Icodecapi-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="12d05-127">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




