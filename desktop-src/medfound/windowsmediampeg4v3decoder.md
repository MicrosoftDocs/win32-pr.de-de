---
description: Der Windows Media MPEG-4 V3-Decoder decodiert MPEG-4 V3-Videostreams.
ms.assetid: 5143b0cc-c171-46af-8d7f-4d029af71fb4
title: Windows Media MPEG-4 V3-Decoder (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ee98a0a3c4b221da6f2000e32d4c75bc3e3a93b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106355714"
---
# <a name="windows-media-mpeg-4-v3-decoder"></a><span data-ttu-id="d9772-103">Windows Media MPEG-4 V3-Decoder</span><span class="sxs-lookup"><span data-stu-id="d9772-103">Windows Media MPEG-4 V3 Decoder</span></span>

<span data-ttu-id="d9772-104">Der Windows Media MPEG-4 V3-Decoder decodiert MPEG-4 V3-Videostreams.</span><span class="sxs-lookup"><span data-stu-id="d9772-104">The Windows Media MPEG-4 V3 decoder decodes MPEG-4 V3 video streams.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="d9772-105">Klassen Bezeichner</span><span class="sxs-lookup"><span data-stu-id="d9772-105">Class Identifier</span></span>

<span data-ttu-id="d9772-106">Der Klassen Bezeichner (CLSID) für den Windows MPEG-4 V3-Decoder wird durch die Konstante **CLSID \_ CMpeg43DecMediaObject** dargestellt.</span><span class="sxs-lookup"><span data-stu-id="d9772-106">The class identifier (CLSID) for the Windows MPEG-4 V3 decoder is represented by the constant **CLSID\_CMpeg43DecMediaObject**.</span></span> <span data-ttu-id="d9772-107">Sie können eine Instanz des MPEG-4 V3-Decoders erstellen, indem Sie **CoCreateInstance** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d9772-107">You can create an instance of the MPEG-4 V3 decoder by calling **CoCreateInstance**.</span></span>

## <a name="formats"></a><span data-ttu-id="d9772-108">Formate</span><span class="sxs-lookup"><span data-stu-id="d9772-108">Formats</span></span>

<span data-ttu-id="d9772-109">Der Windows Media MPEG-4 V3-Decoder unterstützt die folgenden Eingabemedien Typen.</span><span class="sxs-lookup"><span data-stu-id="d9772-109">The Windows Media MPEG-4 V3 decoder supports the following input media types.</span></span>

-   <span data-ttu-id="d9772-110">Mediasubtype \_ MP43</span><span class="sxs-lookup"><span data-stu-id="d9772-110">MEDIASUBTYPE\_MP43</span></span>
-   <span data-ttu-id="d9772-111">Mediasubtype \_ MP43</span><span class="sxs-lookup"><span data-stu-id="d9772-111">MEDIASUBTYPE\_mp43</span></span>

<span data-ttu-id="d9772-112">Der Windows Media MPEG-4 V3-Decoder unterstützt die folgenden Ausgabemedien-Untertypen, wenn er als DirectX-Medienobjekt (DMO) fungiert.</span><span class="sxs-lookup"><span data-stu-id="d9772-112">The Windows Media MPEG-4 V3 decoder supports the following output media subtypes when it is acting as a DirectX Media Object (DMO).</span></span>

-   <span data-ttu-id="d9772-113">Mediasubtype \_ im YUY2</span><span class="sxs-lookup"><span data-stu-id="d9772-113">MEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="d9772-114">mediasubtype \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="d9772-114">MEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="d9772-115">Mediasubtype \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="d9772-115">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="d9772-116">Mediasubtype \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="d9772-116">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="d9772-117">Mediasubtype \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="d9772-117">MEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="d9772-118">Mediasubtype \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="d9772-118">MEDIASUBTYPE\_RGB8</span></span>
-   <span data-ttu-id="d9772-119">Mediasubtype \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="d9772-119">MEDIASUBTYPE\_RGB555</span></span>

<span data-ttu-id="d9772-120">Der Windows Media MPEG-4 V3-Decoder unterstützt die folgenden Ausgabemedien-Untertypen, wenn er als Media Foundation Transformation (MFT) fungiert.</span><span class="sxs-lookup"><span data-stu-id="d9772-120">The Windows Media MPEG-4 V3 decoder supports the following output media subtypes when it is acting as a Media Foundation Transform (MFT).</span></span>

-   <span data-ttu-id="d9772-121">MF-Format \_ im YUY2</span><span class="sxs-lookup"><span data-stu-id="d9772-121">MFVideoFormat\_YUY2</span></span>
-   <span data-ttu-id="d9772-122">MF-Format ( \_ UYVY)</span><span class="sxs-lookup"><span data-stu-id="d9772-122">MFVideoFormat\_UYVY</span></span>
-   <span data-ttu-id="d9772-123">MF-Format \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="d9772-123">MFVideoFormat\_RGB32</span></span>
-   <span data-ttu-id="d9772-124">MF-Format \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="d9772-124">MFVideoFormat\_RGB24</span></span>
-   <span data-ttu-id="d9772-125">MF-Format \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="d9772-125">MFVideoFormat\_RGB565</span></span>
-   <span data-ttu-id="d9772-126">MF-Format \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="d9772-126">MFVideoFormat\_RGB8</span></span>
-   <span data-ttu-id="d9772-127">MF-Format \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="d9772-127">MFVideoFormat\_RGB555</span></span>

## <a name="remarks"></a><span data-ttu-id="d9772-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d9772-128">Remarks</span></span>

<span data-ttu-id="d9772-129">Das Windows Media MPEG-4 V3-Decoder-Objekt macht die [**imediaobject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) -Schnittstelle verfügbar, sodass das Objekt als DirectX Media Object (DMO) verwendet werden kann, und stellt die [**imftransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Schnittstelle zur Verfügung, sodass das Objekt als Media Foundation Transformation (MFT) verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="d9772-129">The Windows Media MPEG-4 V3 decoder object exposes the [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface so that the object can be used as a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="d9772-130">Das-Objekt verfügt über denselben Klassen Bezeichner (CLSID), unabhängig davon, ob er als DMO oder MFT fungiert.</span><span class="sxs-lookup"><span data-stu-id="d9772-130">The object has the same class identifier (CLSID) regardless of whether it acts as a DMO or an MFT.</span></span>

<span data-ttu-id="d9772-131">Der MPEG-4 V3-Decoder verhält sich je nachdem, welche Schnittstellen Sie erhalten und welche Version von Windows ausgeführt wird, als DMO oder MFT.</span><span class="sxs-lookup"><span data-stu-id="d9772-131">The MPEG-4 V3 decoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="d9772-132">In der folgenden Tabelle sind die Bedingungen aufgeführt, unter denen sich ein MPEG-4 V3-Decoder als DMO oder MFT verhält.</span><span class="sxs-lookup"><span data-stu-id="d9772-132">The following table shows the conditions under which an MPEG-4 V3 decoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="d9772-133">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="d9772-133">Operating system</span></span>            | <span data-ttu-id="d9772-134">Decoderverhalten</span><span class="sxs-lookup"><span data-stu-id="d9772-134">Decoder behavior</span></span>                                                                                                                                                    |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9772-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d9772-135">Windows XP</span></span>                  | <span data-ttu-id="d9772-136">Der MPEG-4 V3-Decoder verhält sich immer als DMO.</span><span class="sxs-lookup"><span data-stu-id="d9772-136">The MPEG-4 V3 decoder always behaves as a DMO.</span></span>                                                                                                                      |
| <span data-ttu-id="d9772-137">Windows Vista und Windows 7</span><span class="sxs-lookup"><span data-stu-id="d9772-137">Windows Vista and Windows 7</span></span> | <span data-ttu-id="d9772-138">Standardmäßig verhält sich der MPEG-4 V3-Decoder als DMO.</span><span class="sxs-lookup"><span data-stu-id="d9772-138">By default, the MPEG-4 V3 decoder behaves as a DMO.</span></span> <span data-ttu-id="d9772-139">Wenn Sie eine [**imftransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Schnittstelle für den MPEG-4 V3-Decoder erhalten, verhält sie sich wie eine MFT.</span><span class="sxs-lookup"><span data-stu-id="d9772-139">If you obtain an [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface on the MPEG-4 V3 decoder, it behaves as an MFT.</span></span> |



 

<span data-ttu-id="d9772-140">Die global eindeutigen Bezeichner (GUIDs) für RGB-Medien Untertypen unterscheiden sich abhängig davon, ob ein Decoder als DMO oder MFT fungiert.</span><span class="sxs-lookup"><span data-stu-id="d9772-140">The globally unique identifiers (GUIDs) for RGB media subtypes differ depending on whether a decoder is acting as a DMO or an MFT.</span></span> <span data-ttu-id="d9772-141">Die GUIDs für nicht-RGB-Medien Untertypen sind identisch, unabhängig davon, ob ein Decoder als DMO oder MFT fungiert.</span><span class="sxs-lookup"><span data-stu-id="d9772-141">The GUIDs for non-RGB media subtypes are the same, regardless of whether a decoder is acting as a DMO or an MFT.</span></span> <span data-ttu-id="d9772-142">Informationen zu den GUIDs, die Medien Untertypen darstellen, finden Sie [unter Video Untertyp-GUIDs](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="d9772-142">For information about the GUIDs that represent media subtypes, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d9772-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d9772-143">Requirements</span></span>



| <span data-ttu-id="d9772-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d9772-144">Requirement</span></span> | <span data-ttu-id="d9772-145">Wert</span><span class="sxs-lookup"><span data-stu-id="d9772-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d9772-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d9772-146">Minimum supported client</span></span><br/> | <span data-ttu-id="d9772-147">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d9772-147">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d9772-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d9772-148">Minimum supported server</span></span><br/> | <span data-ttu-id="d9772-149">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d9772-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d9772-150">Header</span><span class="sxs-lookup"><span data-stu-id="d9772-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9772-151"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9772-151"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="d9772-152">DLL</span><span class="sxs-lookup"><span data-stu-id="d9772-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9772-153"><dt>MP43DECD.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9772-153"><dt>MP43DECD.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9772-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d9772-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9772-155">Codec-Objekte</span><span class="sxs-lookup"><span data-stu-id="d9772-155">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
