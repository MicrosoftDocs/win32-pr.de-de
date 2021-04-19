---
description: Eine Reihe von Untertypen sind für das DV-Video definiert. Jede verfügt über einen FourCC-Code und einen entsprechenden GUID-Wert. Nicht alle diese Formate werden unterstützt. Weitere Informationen finden Sie im Abschnitt "Hinweise".
ms.assetid: d8390bd4-0339-4955-992c-92b8c9f6bf88
title: DV-Video Untertypen (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbacb15f5801d959fbc5150546cff04dea687753
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356003"
---
# <a name="dv-video-subtypes"></a><span data-ttu-id="af8e1-105">DV-Video Untertypen</span><span class="sxs-lookup"><span data-stu-id="af8e1-105">DV Video Subtypes</span></span>

<span data-ttu-id="af8e1-106">Eine Reihe von Untertypen sind für das DV-Video definiert.</span><span class="sxs-lookup"><span data-stu-id="af8e1-106">A number of subtypes are defined for DV video.</span></span> <span data-ttu-id="af8e1-107">Jede verfügt über einen FourCC-Code und einen entsprechenden GUID-Wert.</span><span class="sxs-lookup"><span data-stu-id="af8e1-107">Each has a FOURCC code and a corresponding GUID value.</span></span> <span data-ttu-id="af8e1-108">Nicht alle diese Formate werden unterstützt. Weitere Informationen finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="af8e1-108">Not all of these formats are supported; see the Remarks section for more information.</span></span>

## <a name="consumer-formats"></a><span data-ttu-id="af8e1-109">Consumerformate</span><span class="sxs-lookup"><span data-stu-id="af8e1-109">Consumer Formats</span></span>



| <span data-ttu-id="af8e1-110">FOURCC</span><span class="sxs-lookup"><span data-stu-id="af8e1-110">FOURCC</span></span> | <span data-ttu-id="af8e1-111">GUID</span><span class="sxs-lookup"><span data-stu-id="af8e1-111">GUID</span></span>               | <span data-ttu-id="af8e1-112">Datenrate</span><span class="sxs-lookup"><span data-stu-id="af8e1-112">Data Rate</span></span> | <span data-ttu-id="af8e1-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="af8e1-113">Description</span></span>                  |
|--------|--------------------|-----------|------------------------------|
| <span data-ttu-id="af8e1-114">"dvsl"</span><span class="sxs-lookup"><span data-stu-id="af8e1-114">'dvsl'</span></span> | <span data-ttu-id="af8e1-115">Mediasubtype \_ dvsl</span><span class="sxs-lookup"><span data-stu-id="af8e1-115">MEDIASUBTYPE\_dvsl</span></span> | <span data-ttu-id="af8e1-116">12,5 MBit/s</span><span class="sxs-lookup"><span data-stu-id="af8e1-116">12.5 Mbps</span></span> | <span data-ttu-id="af8e1-117">SD-dvcr (525-60 oder 625-50)</span><span class="sxs-lookup"><span data-stu-id="af8e1-117">SD-DVCR (525-60 or 625-50)</span></span>   |
| <span data-ttu-id="af8e1-118">"DVSD"</span><span class="sxs-lookup"><span data-stu-id="af8e1-118">'dvsd'</span></span> | <span data-ttu-id="af8e1-119">Mediasubtype \_ DVSD</span><span class="sxs-lookup"><span data-stu-id="af8e1-119">MEDIASUBTYPE\_dvsd</span></span> | <span data-ttu-id="af8e1-120">25 Mbit/s</span><span class="sxs-lookup"><span data-stu-id="af8e1-120">25 Mbps</span></span>   | <span data-ttu-id="af8e1-121">SDL-dvcr (525-60 oder 625-50)</span><span class="sxs-lookup"><span data-stu-id="af8e1-121">SDL-DVCR (525-60 or 625-50)</span></span>  |
| <span data-ttu-id="af8e1-122">"dvhd"</span><span class="sxs-lookup"><span data-stu-id="af8e1-122">'dvhd'</span></span> | <span data-ttu-id="af8e1-123">Mediasubtype \_ dvhd</span><span class="sxs-lookup"><span data-stu-id="af8e1-123">MEDIASUBTYPE\_dvhd</span></span> | <span data-ttu-id="af8e1-124">50 MBit/s</span><span class="sxs-lookup"><span data-stu-id="af8e1-124">50 Mbps</span></span>   | <span data-ttu-id="af8e1-125">HD-dvcr (1125-60 oder 1250-50)</span><span class="sxs-lookup"><span data-stu-id="af8e1-125">HD-DVCR (1125-60 or 1250-50)</span></span> |



 

<span data-ttu-id="af8e1-126">Weitere Informationen zu diesen Formaten finden Sie unter IEC-61834.</span><span class="sxs-lookup"><span data-stu-id="af8e1-126">Refer to IEC-61834 for more information about these formats.</span></span>

## <a name="professional-formats"></a><span data-ttu-id="af8e1-127">Professionelle Formate</span><span class="sxs-lookup"><span data-stu-id="af8e1-127">Professional Formats</span></span>



| <span data-ttu-id="af8e1-128">FOURCC</span><span class="sxs-lookup"><span data-stu-id="af8e1-128">FOURCC</span></span> | <span data-ttu-id="af8e1-129">GUID</span><span class="sxs-lookup"><span data-stu-id="af8e1-129">GUID</span></span>               | <span data-ttu-id="af8e1-130">Datenrate</span><span class="sxs-lookup"><span data-stu-id="af8e1-130">Data Rate</span></span> | <span data-ttu-id="af8e1-131">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="af8e1-131">Description</span></span>                                 |
|--------|--------------------|-----------|---------------------------------------------|
| <span data-ttu-id="af8e1-132">'dv25'</span><span class="sxs-lookup"><span data-stu-id="af8e1-132">'dv25'</span></span> | <span data-ttu-id="af8e1-133">Mediasubtype \_ DV25</span><span class="sxs-lookup"><span data-stu-id="af8e1-133">MEDIASUBTYPE\_dv25</span></span> | <span data-ttu-id="af8e1-134">25 Mbit/s</span><span class="sxs-lookup"><span data-stu-id="af8e1-134">25 Mbps</span></span>   | <span data-ttu-id="af8e1-135">DVCPro 25 (525-60 oder 625-50).</span><span class="sxs-lookup"><span data-stu-id="af8e1-135">DVCPRO 25 (525-60 or 625-50).</span></span>               |
| <span data-ttu-id="af8e1-136">'dv50'</span><span class="sxs-lookup"><span data-stu-id="af8e1-136">'dv50'</span></span> | <span data-ttu-id="af8e1-137">Mediasubtype \_ DV50</span><span class="sxs-lookup"><span data-stu-id="af8e1-137">MEDIASUBTYPE\_dv50</span></span> | <span data-ttu-id="af8e1-138">50 MBit/s</span><span class="sxs-lookup"><span data-stu-id="af8e1-138">50 Mbps</span></span>   | <span data-ttu-id="af8e1-139">DVCPRO 50 (525-60 oder 625-50)</span><span class="sxs-lookup"><span data-stu-id="af8e1-139">DVCPRO 50 (525-60 or 625-50)</span></span>                |
| <span data-ttu-id="af8e1-140">'dvh1'</span><span class="sxs-lookup"><span data-stu-id="af8e1-140">'dvh1'</span></span> | <span data-ttu-id="af8e1-141">Mediasubtype \_ dvh1</span><span class="sxs-lookup"><span data-stu-id="af8e1-141">MEDIASUBTYPE\_dvh1</span></span> | <span data-ttu-id="af8e1-142">100 MBit/s</span><span class="sxs-lookup"><span data-stu-id="af8e1-142">100 Mbps</span></span>  | <span data-ttu-id="af8e1-143">DVCPRO 100 (1080/60i, 1080/50i oder 720/60p)</span><span class="sxs-lookup"><span data-stu-id="af8e1-143">DVCPRO 100 (1080/60i, 1080/50i, or 720/60P)</span></span> |



 

<span data-ttu-id="af8e1-144">Weitere Informationen zu DV25 und DV50 sowie zu SMPTE 370m finden Sie unter SMPTE 314m.</span><span class="sxs-lookup"><span data-stu-id="af8e1-144">Refer to SMPTE 314M for more information about dv25 and dv50, and SMPTE 370M for more information about dvh1.</span></span>

## <a name="miscellaneous"></a><span data-ttu-id="af8e1-145">Verschiedenes</span><span class="sxs-lookup"><span data-stu-id="af8e1-145">Miscellaneous</span></span>

<span data-ttu-id="af8e1-146">Zwei weitere DV-Untertypen sind in der Header Datei "UUIDs. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="af8e1-146">Two additional DV subtypes are defined in the header file Uuids.h.</span></span> <span data-ttu-id="af8e1-147">Diese entsprechen den FourCC-Codes, die von bestimmten DV-Codecs erstellt werden. Sie entsprechen keinen definierten DV-Standards.</span><span class="sxs-lookup"><span data-stu-id="af8e1-147">These correspond to FOURCC codes that are produced by certain DV codecs; they do not correspond to any defined DV standards.</span></span> <span data-ttu-id="af8e1-148">Diese Untertypen sind veraltet und sollten nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="af8e1-148">These subtypes are obsolete and should not be used.</span></span>



| <span data-ttu-id="af8e1-149">FOURCC</span><span class="sxs-lookup"><span data-stu-id="af8e1-149">FOURCC</span></span> | <span data-ttu-id="af8e1-150">GUID</span><span class="sxs-lookup"><span data-stu-id="af8e1-150">GUID</span></span>               |
|--------|--------------------|
| <span data-ttu-id="af8e1-151">DVCS</span><span class="sxs-lookup"><span data-stu-id="af8e1-151">'DVCS'</span></span> | <span data-ttu-id="af8e1-152">mediasubtype- \_ dvcs</span><span class="sxs-lookup"><span data-stu-id="af8e1-152">MEDIASUBTYPE\_DVCS</span></span> |
| <span data-ttu-id="af8e1-153">"DVSD"</span><span class="sxs-lookup"><span data-stu-id="af8e1-153">'DVSD'</span></span> | <span data-ttu-id="af8e1-154">mediasubtype \_ DVSD</span><span class="sxs-lookup"><span data-stu-id="af8e1-154">MEDIASUBTYPE\_DVSD</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="af8e1-155">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="af8e1-155">Remarks</span></span>

<span data-ttu-id="af8e1-156">In der folgenden Tabelle werden die unterstützten Datenraten für die msdv-und UVC-Treiber in meits pro Sekunde (Mbit/s) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="af8e1-156">The following table shows the supported data rates, in megabits per second (Mbps), for the MSDV and UVC drivers.</span></span>



| <span data-ttu-id="af8e1-157">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="af8e1-157">Operating System</span></span>                                                                 | <span data-ttu-id="af8e1-158">Msdv-Treiber (IEEE 1394)</span><span class="sxs-lookup"><span data-stu-id="af8e1-158">MSDV (IEEE 1394) Driver</span></span> | <span data-ttu-id="af8e1-159">UVC-Treiber</span><span class="sxs-lookup"><span data-stu-id="af8e1-159">UVC Driver</span></span>    |
|----------------------------------------------------------------------------------|-------------------------|---------------|
| <span data-ttu-id="af8e1-160">Windows XP Service Pack 1 oder früher</span><span class="sxs-lookup"><span data-stu-id="af8e1-160">Windows XP Service Pack 1 or earlier</span></span>                                             | <span data-ttu-id="af8e1-161">12,5, 25</span><span class="sxs-lookup"><span data-stu-id="af8e1-161">12.5, 25</span></span>                | <span data-ttu-id="af8e1-162">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="af8e1-162">Not available</span></span> |
| <span data-ttu-id="af8e1-163">Windows XP Service Pack 2 oder höher, Windows Server 2003 Service Pack 1 oder höher.</span><span class="sxs-lookup"><span data-stu-id="af8e1-163">Windows XP Service Pack 2 or later, Windows Server 2003 Service Pack 1 or later.</span></span> | <span data-ttu-id="af8e1-164">12,5, 25, 50, 100</span><span class="sxs-lookup"><span data-stu-id="af8e1-164">12.5, 25, 50, 100</span></span>       | <span data-ttu-id="af8e1-165">12,5, 25</span><span class="sxs-lookup"><span data-stu-id="af8e1-165">12.5, 25</span></span>      |



 

<span data-ttu-id="af8e1-166">Für Datenströme mit 25 Mbit/s hat sich das Verhalten des msdv-Treibers in Windows Vista vor Windows Vista geändert. der msdv-Treiber hat den Medientyp immer auf mediasubtype \_ DVSD für 25 Mbit/s-Streams festgelegt, unabhängig davon, ob die Quelle SDL-dvcr oder DVCPro 25 war.</span><span class="sxs-lookup"><span data-stu-id="af8e1-166">For 25-Mbps streams, the behavior of the MSDV driver has changed in Windows Vista Prior to Windows Vista, the MSDV driver always set the media type to MEDIASUBTYPE\_dvsd for 25-Mbps streams, regardless of whether the source was SDL-DVCR or DVCPRO 25.</span></span> <span data-ttu-id="af8e1-167">Der Medientyp ' DV25 ' wurde nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="af8e1-167">The 'dv25' media type was not used.</span></span> <span data-ttu-id="af8e1-168">Ab Windows Vista unterscheidet der msdv-Treiber nun zwischen diesen beiden Formaten.</span><span class="sxs-lookup"><span data-stu-id="af8e1-168">Starting with Windows Vista, the MSDV driver now distinguishes between these two formats.</span></span> <span data-ttu-id="af8e1-169">Für SDL-dvcr wird weiterhin der "DVSD"-Untertyp verwendet.</span><span class="sxs-lookup"><span data-stu-id="af8e1-169">For SDL-DVCR, it continues to use the 'dvsd' subtype.</span></span> <span data-ttu-id="af8e1-170">Bei DVCPro 25 wird nun der Untertyp "DV25" verwendet.</span><span class="sxs-lookup"><span data-stu-id="af8e1-170">For DVCPRO 25, it now uses the 'dv25' subtype.</span></span>

<span data-ttu-id="af8e1-171">Die Filter "DirectShow [DV Splitter](dv-splitter-filter.md) " und " [DV Video Decoder](dv-video-decoder-filter.md) " unterstützen nur SDL-dvcr-Formate.</span><span class="sxs-lookup"><span data-stu-id="af8e1-171">The DirectShow [DV Splitter](dv-splitter-filter.md) and [DV Video Decoder](dv-video-decoder-filter.md) filters support SDL-DVCR formats only.</span></span> <span data-ttu-id="af8e1-172">Die Daten können PAL oder NTSC sein.</span><span class="sxs-lookup"><span data-stu-id="af8e1-172">The data can be PAL or NTSC.</span></span> <span data-ttu-id="af8e1-173">Möglicherweise sind Filter oder Codecs von Drittanbietern verfügbar, mit denen andere DV-Formate analysiert werden können, solange die Datenmenge vom msdv-oder UVC-Treiber unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="af8e1-173">Third-party filters or codecs may be available that can parse other DV formats, as long as the data rate is supported by the MSDV or UVC driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="af8e1-174">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="af8e1-174">Requirements</span></span>



| <span data-ttu-id="af8e1-175">Anforderung</span><span class="sxs-lookup"><span data-stu-id="af8e1-175">Requirement</span></span> | <span data-ttu-id="af8e1-176">Wert</span><span class="sxs-lookup"><span data-stu-id="af8e1-176">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="af8e1-177">Header</span><span class="sxs-lookup"><span data-stu-id="af8e1-177">Header</span></span><br/> | <dl> <span data-ttu-id="af8e1-178"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="af8e1-178"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af8e1-179">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="af8e1-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af8e1-180">Digitales Video in DirectShow</span><span class="sxs-lookup"><span data-stu-id="af8e1-180">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="af8e1-181">Msdv-Treiber</span><span class="sxs-lookup"><span data-stu-id="af8e1-181">MSDV Driver</span></span>](msdv-driver.md)
</dt> <dt>

[<span data-ttu-id="af8e1-182">Video Untertypen</span><span class="sxs-lookup"><span data-stu-id="af8e1-182">Video Subtypes</span></span>](video-subtypes.md)
</dt> </dl>

 

 




