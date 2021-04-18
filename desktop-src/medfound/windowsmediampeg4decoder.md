---
description: Der Windows Media MPEG4 V1/V2-Decoder decodiert die Videostreams von MPEG4 v1/v2.
ms.assetid: 63b32972-1003-4291-bfdd-cc0cb8d65430
title: Windows Media MPEG4 V1/V2-Decoder (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b14cf22e29c1266ac9bb3593375ee4485d79df2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106365224"
---
# <a name="windows-media-mpeg4-v1v2-decoder"></a><span data-ttu-id="9b119-103">Windows Media MPEG4 V1/V2-Decoder</span><span class="sxs-lookup"><span data-stu-id="9b119-103">Windows Media MPEG4 V1/V2 Decoder</span></span>

<span data-ttu-id="9b119-104">Der Windows Media MPEG4 V1/V2-Decoder decodiert die Videostreams von MPEG4 v1/v2.</span><span class="sxs-lookup"><span data-stu-id="9b119-104">The Windows Media MPEG4 V1/V2 decoder decodes MPEG4 V1/V2 video streams.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="9b119-105">Klassen Bezeichner</span><span class="sxs-lookup"><span data-stu-id="9b119-105">Class Identifier</span></span>

<span data-ttu-id="9b119-106">Der Klassen Bezeichner (CLSID) für den Windows Media MPEG4 V1/V2-Decoder wird durch die Konstante **CLSID \_ CMpeg4DecMediaObject** dargestellt.</span><span class="sxs-lookup"><span data-stu-id="9b119-106">The class identifier (CLSID) for the Windows Media MPEG4 V1/V2 decoder is represented by the constant **CLSID\_CMpeg4DecMediaObject**.</span></span> <span data-ttu-id="9b119-107">Sie können eine Instanz des MPEG4 V1/V2-Decoders erstellen, indem Sie **CoCreateInstance** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="9b119-107">You can create an instance of the MPEG4 V1/V2 decoder by calling **CoCreateInstance**.</span></span>

## <a name="formats"></a><span data-ttu-id="9b119-108">Formate</span><span class="sxs-lookup"><span data-stu-id="9b119-108">Formats</span></span>

<span data-ttu-id="9b119-109">Der Windows Media MPEG4 V1/V2-Decoder unterstützt die folgenden Eingabemedien Typen.</span><span class="sxs-lookup"><span data-stu-id="9b119-109">The Windows Media MPEG4 V1/V2 decoder supports the following input media types.</span></span>

-   <span data-ttu-id="9b119-110">Mediasubtype \_ MPG4</span><span class="sxs-lookup"><span data-stu-id="9b119-110">MEDIASUBTYPE\_MPG4</span></span>
-   <span data-ttu-id="9b119-111">Mediasubtype \_ MPG4</span><span class="sxs-lookup"><span data-stu-id="9b119-111">MEDIASUBTYPE\_mpg4</span></span>
-   <span data-ttu-id="9b119-112">Mediasubtype \_ MP42</span><span class="sxs-lookup"><span data-stu-id="9b119-112">MEDIASUBTYPE\_MP42</span></span>
-   <span data-ttu-id="9b119-113">Mediasubtype \_ mp42</span><span class="sxs-lookup"><span data-stu-id="9b119-113">MEDIASUBTYPE\_mp42</span></span>

<span data-ttu-id="9b119-114">Der Windows Media MPEG4 V1/V2-Decoder unterstützt die folgenden Ausgabemedien-Untertypen, wenn er als DirectX-Medienobjekt (DMO) fungiert.</span><span class="sxs-lookup"><span data-stu-id="9b119-114">The Windows Media MPEG4 V1/V2 decoder supports the following output media subtypes when it is acting as a DirectX Media Object (DMO).</span></span>

-   <span data-ttu-id="9b119-115">Mediasubtype \_ im YUY2</span><span class="sxs-lookup"><span data-stu-id="9b119-115">MEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="9b119-116">mediasubtype \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="9b119-116">MEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="9b119-117">Mediasubtype \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="9b119-117">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="9b119-118">Mediasubtype \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="9b119-118">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="9b119-119">Mediasubtype \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="9b119-119">MEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="9b119-120">Mediasubtype \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="9b119-120">MEDIASUBTYPE\_RGB8</span></span>
-   <span data-ttu-id="9b119-121">Mediasubtype \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="9b119-121">MEDIASUBTYPE\_RGB555</span></span>

<span data-ttu-id="9b119-122">Der Windows Media MPEG4 V1/V2-Decoder unterstützt die folgenden Ausgabemedien-Untertypen, wenn er als Media Foundation Transformation (MFT) fungiert.</span><span class="sxs-lookup"><span data-stu-id="9b119-122">The Windows Media MPEG4 V1/V2 decoder supports the following output media subtypes when it is acting as a Media Foundation Transform (MFT).</span></span>

-   <span data-ttu-id="9b119-123">MF-Format \_ im YUY2</span><span class="sxs-lookup"><span data-stu-id="9b119-123">MFVideoFormat\_YUY2</span></span>
-   <span data-ttu-id="9b119-124">MF-Format ( \_ UYVY)</span><span class="sxs-lookup"><span data-stu-id="9b119-124">MFVideoFormat\_UYVY</span></span>
-   <span data-ttu-id="9b119-125">MF-Format \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="9b119-125">MFVideoFormat\_RGB32</span></span>
-   <span data-ttu-id="9b119-126">MF-Format \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="9b119-126">MFVideoFormat\_RGB24</span></span>
-   <span data-ttu-id="9b119-127">MF-Format \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="9b119-127">MFVideoFormat\_RGB565</span></span>
-   <span data-ttu-id="9b119-128">MF-Format \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="9b119-128">MFVideoFormat\_RGB8</span></span>
-   <span data-ttu-id="9b119-129">MF-Format \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="9b119-129">MFVideoFormat\_RGB555</span></span>

## <a name="remarks"></a><span data-ttu-id="9b119-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9b119-130">Remarks</span></span>

<span data-ttu-id="9b119-131">Das Windows Media MPEG4 V1/V2-Decoderobjekt macht die [**imediaobject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) -Schnittstelle verfügbar, sodass das Objekt als DirectX Media Object (DMO) verwendet werden kann, und stellt die [**imftransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Schnittstelle zur Verfügung, sodass das Objekt als Media Foundation Transformation (MFT) verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="9b119-131">The Windows Media MPEG4 V1/V2 decoder object exposes the [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface so that the object can be used as a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="9b119-132">Das-Objekt verfügt über denselben Klassen Bezeichner (CLSID), unabhängig davon, ob er als DMO oder MFT fungiert.</span><span class="sxs-lookup"><span data-stu-id="9b119-132">The object has the same class identifier (CLSID) regardless of whether it acts as a DMO or an MFT.</span></span>

<span data-ttu-id="9b119-133">Ein MPEG4 V1/V2-Decoder verhält sich als DMO oder MFT, je nachdem, welche Schnittstellen Sie erhalten und welche Version von Windows ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9b119-133">An MPEG4 V1/V2 decoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="9b119-134">In der folgenden Tabelle sind die Bedingungen aufgeführt, unter denen sich ein MPEG4 V1/V2-Decoder als DMO oder MFT verhält.</span><span class="sxs-lookup"><span data-stu-id="9b119-134">The following table shows the conditions under which an MPEG4 V1/V2 decoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="9b119-135">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="9b119-135">Operating system</span></span>            | <span data-ttu-id="9b119-136">Decoderverhalten</span><span class="sxs-lookup"><span data-stu-id="9b119-136">Decoder behavior</span></span>                                                                                                                                                                |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b119-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="9b119-137">Windows XP</span></span>                  | <span data-ttu-id="9b119-138">Ein MPEG4 V1/V2-Decoder verhält sich immer als DMO.</span><span class="sxs-lookup"><span data-stu-id="9b119-138">An MPEG4 V1/V2 decoder always behaves as a DMO.</span></span>                                                                                                                                 |
| <span data-ttu-id="9b119-139">Windows Vista und Windows 7</span><span class="sxs-lookup"><span data-stu-id="9b119-139">Windows Vista and Windows 7</span></span> | <span data-ttu-id="9b119-140">Standardmäßig verhält sich ein MPEG4 V1/V2-Decoder als DMO.</span><span class="sxs-lookup"><span data-stu-id="9b119-140">By default, an MPEG4 V1/V2 decoder behaves as a DMO.</span></span> <span data-ttu-id="9b119-141">Wenn Sie in einem MPEG4 V1/V2-Decoder eine Schnittstelle für den [Video Untertyp "GUIDs](video-subtype-guids.md) " erhalten, verhält sie sich wie eine MFT.</span><span class="sxs-lookup"><span data-stu-id="9b119-141">If you obtain an [Video Subtype GUIDs](video-subtype-guids.md) interface on an MPEG4 V1/V2 decoder, it behaves as an MFT.</span></span> |



 

<span data-ttu-id="9b119-142">Die global eindeutigen Bezeichner (GUIDs) für RGB-Medien Untertypen unterscheiden sich abhängig davon, ob ein Decoder als DMO oder MFT fungiert.</span><span class="sxs-lookup"><span data-stu-id="9b119-142">The globally unique identifiers (GUIDs) for RGB media subtypes differ depending on whether a decoder is acting as a DMO or an MFT.</span></span> <span data-ttu-id="9b119-143">Die GUIDs für nicht-RGB-Medien Untertypen sind identisch, unabhängig davon, ob ein Decoder als DMO oder MFT fungiert.</span><span class="sxs-lookup"><span data-stu-id="9b119-143">The GUIDs for non-RGB media subtypes are the same, regardless of whether a decoder is acting as a DMO or an MFT.</span></span> <span data-ttu-id="9b119-144">Informationen zu den GUIDs, die Video Untertypen darstellen, finden Sie [unter Video Untertyp-GUIDs](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="9b119-144">For information about the GUIDs that represent video subtypes, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9b119-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9b119-145">Requirements</span></span>



| <span data-ttu-id="9b119-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9b119-146">Requirement</span></span> | <span data-ttu-id="9b119-147">Wert</span><span class="sxs-lookup"><span data-stu-id="9b119-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b119-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9b119-148">Minimum supported client</span></span><br/> | <span data-ttu-id="9b119-149">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9b119-149">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="9b119-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9b119-150">Minimum supported server</span></span><br/> | <span data-ttu-id="9b119-151">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9b119-151">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9b119-152">Header</span><span class="sxs-lookup"><span data-stu-id="9b119-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b119-153"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b119-153"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="9b119-154">DLL</span><span class="sxs-lookup"><span data-stu-id="9b119-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b119-155"><dt>MPG4DECD.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b119-155"><dt>MPG4DECD.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b119-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9b119-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b119-157">Codec-Objekte</span><span class="sxs-lookup"><span data-stu-id="9b119-157">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
