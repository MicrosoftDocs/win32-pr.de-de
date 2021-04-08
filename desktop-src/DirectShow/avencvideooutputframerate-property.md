---
description: Gibt die Framerate für den Ausgabestream des Encoders in Frames pro Sekunde an.
ms.assetid: 72e16c7d-977e-4269-9576-afc789e31826
title: Avencvideooutputframerate-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad4cb675c266d146936a3402934e51486ded5b02
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746232"
---
# <a name="avencvideooutputframerate-property"></a><span data-ttu-id="c0066-103">Avencvideooutputframerate (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c0066-103">AVEncVideoOutputFrameRate property</span></span>

<span data-ttu-id="c0066-104">Gibt die Framerate für den Ausgabestream des Encoders in Frames pro Sekunde an.</span><span class="sxs-lookup"><span data-stu-id="c0066-104">Specifies the frame rate on the encoder's output stream, in frames per second.</span></span>

<span data-ttu-id="c0066-105">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="c0066-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="c0066-106">Datentyp</span><span class="sxs-lookup"><span data-stu-id="c0066-106">Data type</span></span>

<span data-ttu-id="c0066-107">**UINT64** (**VT \_ UI8**)</span><span class="sxs-lookup"><span data-stu-id="c0066-107">**UINT64** (**VT\_UI8**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="c0066-108">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="c0066-108">Property GUID</span></span>

<span data-ttu-id="c0066-109">**Codecapi \_ avencvideooutputframerate**</span><span class="sxs-lookup"><span data-stu-id="c0066-109">**CODECAPI\_AVEncVideoOutputFrameRate**</span></span>

## <a name="property-value"></a><span data-ttu-id="c0066-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="c0066-110">Property value</span></span>

<span data-ttu-id="c0066-111">Der Wert dieser Eigenschaft ist ein Verhältnis, das die Framerate definiert.</span><span class="sxs-lookup"><span data-stu-id="c0066-111">The value of this property is a ratio that defines the frame rate.</span></span> <span data-ttu-id="c0066-112">Die oberen 32 Bits enthalten den Zähler, und die unteren 32 Bits enthalten den Nenner.</span><span class="sxs-lookup"><span data-stu-id="c0066-112">The upper 32 bits contain the numerator, and the lower 32 bits contain the denominator.</span></span> <span data-ttu-id="c0066-113">In der folgenden Tabelle werden allgemeine Frameraten in Frames pro Sekunde angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c0066-113">The following table shows common frame rates, in frames per second.</span></span>



| <span data-ttu-id="c0066-114">Bildfrequenz</span><span class="sxs-lookup"><span data-stu-id="c0066-114">Frame rate</span></span> | <span data-ttu-id="c0066-115">Seitenverhältnis</span><span class="sxs-lookup"><span data-stu-id="c0066-115">Ratio</span></span>      |
|------------|------------|
| <span data-ttu-id="c0066-116">23,97</span><span class="sxs-lookup"><span data-stu-id="c0066-116">23.97</span></span>      | <span data-ttu-id="c0066-117">24000/1001</span><span class="sxs-lookup"><span data-stu-id="c0066-117">24000/1001</span></span> |
| <span data-ttu-id="c0066-118">24</span><span class="sxs-lookup"><span data-stu-id="c0066-118">24</span></span>         | <span data-ttu-id="c0066-119">24/1</span><span class="sxs-lookup"><span data-stu-id="c0066-119">24/1</span></span>       |
| <span data-ttu-id="c0066-120">25</span><span class="sxs-lookup"><span data-stu-id="c0066-120">25</span></span>         | <span data-ttu-id="c0066-121">25/1</span><span class="sxs-lookup"><span data-stu-id="c0066-121">25/1</span></span>       |
| <span data-ttu-id="c0066-122">29,97</span><span class="sxs-lookup"><span data-stu-id="c0066-122">29.97</span></span>      | <span data-ttu-id="c0066-123">30000/1001</span><span class="sxs-lookup"><span data-stu-id="c0066-123">30000/1001</span></span> |
| <span data-ttu-id="c0066-124">30</span><span class="sxs-lookup"><span data-stu-id="c0066-124">30</span></span>         | <span data-ttu-id="c0066-125">30/1</span><span class="sxs-lookup"><span data-stu-id="c0066-125">30/1</span></span>       |
| <span data-ttu-id="c0066-126">50</span><span class="sxs-lookup"><span data-stu-id="c0066-126">50</span></span>         | <span data-ttu-id="c0066-127">50/1</span><span class="sxs-lookup"><span data-stu-id="c0066-127">50/1</span></span>       |
| <span data-ttu-id="c0066-128">59,94</span><span class="sxs-lookup"><span data-stu-id="c0066-128">59.94</span></span>      | <span data-ttu-id="c0066-129">60000/1001</span><span class="sxs-lookup"><span data-stu-id="c0066-129">60000/1001</span></span> |
| <span data-ttu-id="c0066-130">60</span><span class="sxs-lookup"><span data-stu-id="c0066-130">60</span></span>         | <span data-ttu-id="c0066-131">60/1</span><span class="sxs-lookup"><span data-stu-id="c0066-131">60/1</span></span>       |



 

## <a name="remarks"></a><span data-ttu-id="c0066-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c0066-132">Remarks</span></span>

<span data-ttu-id="c0066-133">Anwendungen können diese Eigenschaft festlegen, um die Ausgabe Frame Rate anzugeben.</span><span class="sxs-lookup"><span data-stu-id="c0066-133">Applications can set this property to specify the output frame rate.</span></span> <span data-ttu-id="c0066-134">Encoder können diese Eigenschaft auch als Funktion zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="c0066-134">Encoders can also return this property as a capability.</span></span> <span data-ttu-id="c0066-135">Abhängig vom Encoder ist der Wert möglicherweise auf die Eingabe Frame Rate beschränkt.</span><span class="sxs-lookup"><span data-stu-id="c0066-135">Depending on the encoder, the value might be restricted to the input frame rate.</span></span> <span data-ttu-id="c0066-136">Wenn dies nicht der Fall ist, kann der Encoder die Framerate intern konvertieren.</span><span class="sxs-lookup"><span data-stu-id="c0066-136">If not, the encoder is able to convert the frame rate internally.</span></span> <span data-ttu-id="c0066-137">Siehe die [**Eigenschaft "avencvideooutputframerateconversion**](avencvideooutputframerateconversion-property.md)".</span><span class="sxs-lookup"><span data-stu-id="c0066-137">See [**AVEncVideoOutputFrameRateConversion Property**](avencvideooutputframerateconversion-property.md).</span></span>

<span data-ttu-id="c0066-138">Diese Eigenschaft wird auch mit [H. 264 UVC 1,5-Kamera Codierern](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5)verwendet.</span><span class="sxs-lookup"><span data-stu-id="c0066-138">This property is also used with [H.264 UVC 1.5 camera encoders](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).</span></span>

## <a name="requirements"></a><span data-ttu-id="c0066-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c0066-139">Requirements</span></span>



| <span data-ttu-id="c0066-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c0066-140">Requirement</span></span> | <span data-ttu-id="c0066-141">Wert</span><span class="sxs-lookup"><span data-stu-id="c0066-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c0066-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c0066-142">Minimum supported client</span></span><br/> | <span data-ttu-id="c0066-143">Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="c0066-143">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="c0066-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c0066-144">Minimum supported server</span></span><br/> | <span data-ttu-id="c0066-145">Windows 2000 Server \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="c0066-145">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="c0066-146">Header</span><span class="sxs-lookup"><span data-stu-id="c0066-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0066-147"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0066-147"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0066-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c0066-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0066-149">Eigenschaften der Codec-API</span><span class="sxs-lookup"><span data-stu-id="c0066-149">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="c0066-150">**Icodecapi-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="c0066-150">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

