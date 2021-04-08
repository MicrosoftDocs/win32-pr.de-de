---
description: Gibt das Komplexitäts Profil des codierten Inhalts an.
ms.assetid: 2e238d31-98b2-4c79-96b0-9e6949010a73
title: MFPKEY_DECODERCOMPLEXITYPROFILE-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f39544830a0a05e21779a637da61d3bcb310fcd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864175"
---
# <a name="mfpkey_decodercomplexityprofile-property"></a><span data-ttu-id="d6b13-103">Mfpkey- \_ decodercomplexityprofile-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d6b13-103">MFPKEY\_DECODERCOMPLEXITYPROFILE Property</span></span>

<span data-ttu-id="d6b13-104">Gibt das Komplexitäts Profil des codierten Inhalts an.</span><span class="sxs-lookup"><span data-stu-id="d6b13-104">Specifies the complexity profile of the encoded content.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="d6b13-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="d6b13-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="d6b13-106">g \_ wszwmvcdecodercomplexityprofile</span><span class="sxs-lookup"><span data-stu-id="d6b13-106">g\_wszWMVCDecoderComplexityProfile</span></span>

## <a name="data-type"></a><span data-ttu-id="d6b13-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="d6b13-107">Data Type</span></span>

<span data-ttu-id="d6b13-108">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="d6b13-108">**VT\_BSTR**</span></span>

## <a name="remarks"></a><span data-ttu-id="d6b13-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d6b13-109">Remarks</span></span>

<span data-ttu-id="d6b13-110">Sie können diesen Wert erst lesen, nachdem die Codierung abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="d6b13-110">You can read this value only after encoding is completed.</span></span>

<span data-ttu-id="d6b13-111">Für Audiodaten verfügt diese Eigenschaft über einen der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="d6b13-111">For audio, this property has one of the following values.</span></span>



| <span data-ttu-id="d6b13-112">Wert</span><span class="sxs-lookup"><span data-stu-id="d6b13-112">Value</span></span> | <span data-ttu-id="d6b13-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d6b13-113">Description</span></span>                                                                                    |
|-------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6b13-114">L1</span><span class="sxs-lookup"><span data-stu-id="d6b13-114">"L1"</span></span>  | <span data-ttu-id="d6b13-115">Standard Codierung mit einer Samplingrate von 44,1 kHz und einer maximalen Bitrate von 161 Kbit/s.</span><span class="sxs-lookup"><span data-stu-id="d6b13-115">Standard encoding with a sampling rate of 44.1 KHz and a maximum bit rate of 161 Kbps.</span></span>         |
| <span data-ttu-id="d6b13-116">L2</span><span class="sxs-lookup"><span data-stu-id="d6b13-116">"L2"</span></span>  | <span data-ttu-id="d6b13-117">Standard Codierung mit Samplingrate von bis zu 48 kHz und einer maximalen Bitrate von 161 Kbit/s.</span><span class="sxs-lookup"><span data-stu-id="d6b13-117">Standard encoding with sampling rates up to 48 KHz and a maximum bit rate of 161 Kbps.</span></span>         |
| <span data-ttu-id="d6b13-118">L3</span><span class="sxs-lookup"><span data-stu-id="d6b13-118">"L3"</span></span>  | <span data-ttu-id="d6b13-119">Standard Codierung mit Samplingrate von bis zu 48 kHz und einer maximalen Bitrate von 385 kbit/s.</span><span class="sxs-lookup"><span data-stu-id="d6b13-119">Standard encoding with sampling rates up to 48 KHz and a maximum bit rate of 385 Kbps.</span></span>         |
| <span data-ttu-id="d6b13-120">"M0a"</span><span class="sxs-lookup"><span data-stu-id="d6b13-120">"M0a"</span></span> | <span data-ttu-id="d6b13-121">Professionelle Codierung mit Stichproben Raten von bis zu 48 kHz und Bitraten zwischen 48 und 192 Kbit/s.</span><span class="sxs-lookup"><span data-stu-id="d6b13-121">Professional encoding with sampling rates up to 48 KHz and bit rates between 48 and 192 Kbps.</span></span>  |
| <span data-ttu-id="d6b13-122">"M0b"</span><span class="sxs-lookup"><span data-stu-id="d6b13-122">"M0b"</span></span> | <span data-ttu-id="d6b13-123">Professionelle Codierung mit Stichproben Raten von bis zu 48 kHz und einer maximalen Bitrate von 192 Kbit/s.</span><span class="sxs-lookup"><span data-stu-id="d6b13-123">Professional encoding with sampling rates up to 48 KHz and a maximum bitrate of 192 Kbps.</span></span>      |
| <span data-ttu-id="d6b13-124">M1</span><span class="sxs-lookup"><span data-stu-id="d6b13-124">"M1"</span></span>  | <span data-ttu-id="d6b13-125">Professionelle Codierung mit Stichproben Raten von bis zu 48 kHz und einer maximalen Bitrate von 384 Kbit/s.</span><span class="sxs-lookup"><span data-stu-id="d6b13-125">Professional encoding with sampling rates up to 48 KHz and a maximum bitrate of 384 Kbps.</span></span>      |
| <span data-ttu-id="d6b13-126">Groß</span><span class="sxs-lookup"><span data-stu-id="d6b13-126">"M2"</span></span>  | <span data-ttu-id="d6b13-127">Professionelle Codierung mit Stichproben Raten von bis zu 96 kHz und einer maximalen Bitrate von 768 Kbit/s.</span><span class="sxs-lookup"><span data-stu-id="d6b13-127">Professional encoding with sampling rates up to 96 KHz and a maximum bitrate of 768 Kbps.</span></span>      |
| <span data-ttu-id="d6b13-128">Kubikmeter</span><span class="sxs-lookup"><span data-stu-id="d6b13-128">"M3"</span></span>  | <span data-ttu-id="d6b13-129">Professionelle Codierung mit Stichproben Raten von bis zu 96 kHz und einer maximalen Bitrate von 1,5 MBit/s.</span><span class="sxs-lookup"><span data-stu-id="d6b13-129">Professional encoding with sampling rates up to 96 KHz and a maximum bitrate of 1.5 Mbps.</span></span>      |
| <span data-ttu-id="d6b13-130">N1</span><span class="sxs-lookup"><span data-stu-id="d6b13-130">"N1"</span></span>  | <span data-ttu-id="d6b13-131">Verlust lose Codierung mit Stichproben Raten von bis zu 48 kHz und maximal 2 Kanälen.</span><span class="sxs-lookup"><span data-stu-id="d6b13-131">Lossless encoding with sampling rates up to 48 KHz and a maximum of 2 channels.</span></span>                |
| <span data-ttu-id="d6b13-132">N2</span><span class="sxs-lookup"><span data-stu-id="d6b13-132">"N2"</span></span>  | <span data-ttu-id="d6b13-133">Verlust lose Codierung mit Stichproben Raten von bis zu 96 kHz und maximal 6 Kanälen (5,1-umschließende).</span><span class="sxs-lookup"><span data-stu-id="d6b13-133">Lossless encoding with sampling rates up to 96 KHz and a maximum of 6 channels (5.1 surround).</span></span> |
| <span data-ttu-id="d6b13-134">N3</span><span class="sxs-lookup"><span data-stu-id="d6b13-134">"N3"</span></span>  | <span data-ttu-id="d6b13-135">Verlust lose Codierung mit Stichproben Raten von bis zu 96 kHz und maximal 8 Kanälen (7,1-umschließende).</span><span class="sxs-lookup"><span data-stu-id="d6b13-135">Lossless encoding with sampling rates up to 96 KHz and a maximum of 8 channels (7.1 surround).</span></span> |



 

<span data-ttu-id="d6b13-136">Für das Video weist diese Eigenschaft einen der folgenden Werte auf:</span><span class="sxs-lookup"><span data-stu-id="d6b13-136">For video, this property has one of the following values:</span></span>



| <span data-ttu-id="d6b13-137">Wert</span><span class="sxs-lookup"><span data-stu-id="d6b13-137">Value</span></span> | <span data-ttu-id="d6b13-138">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d6b13-138">Description</span></span>                                                                       |
|-------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="d6b13-139">Unglücks</span><span class="sxs-lookup"><span data-stu-id="d6b13-139">"AP"</span></span>  | <span data-ttu-id="d6b13-140">Erweitertes Profil (nur auf Windows Media Video 9 Advanced Profile Codec verfügbar)</span><span class="sxs-lookup"><span data-stu-id="d6b13-140">advanced profile (available only on Windows Media Video 9 Advanced Profile codec)</span></span> |
| <span data-ttu-id="d6b13-141">Erfolgen</span><span class="sxs-lookup"><span data-stu-id="d6b13-141">"CP"</span></span>  | <span data-ttu-id="d6b13-142">nicht mehr unterstützt</span><span class="sxs-lookup"><span data-stu-id="d6b13-142">no longer supported</span></span>                                                               |
| <span data-ttu-id="d6b13-143">Schlanken</span><span class="sxs-lookup"><span data-stu-id="d6b13-143">"MP"</span></span>  | <span data-ttu-id="d6b13-144">Hauptprofil</span><span class="sxs-lookup"><span data-stu-id="d6b13-144">main profile</span></span>                                                                      |
| <span data-ttu-id="d6b13-145">El</span><span class="sxs-lookup"><span data-stu-id="d6b13-145">"SP"</span></span>  | <span data-ttu-id="d6b13-146">einfaches Profil</span><span class="sxs-lookup"><span data-stu-id="d6b13-146">simple profile</span></span>                                                                    |



 

<span data-ttu-id="d6b13-147">Für Videoinhalte können Sie eine Profil Ebene anfordern, indem Sie [mfpkey \_ decodercomplexityangeforderten](mfpkey-decodercomplexityrequestedproperty.md) festlegen, bevor Sie mit der Codierung beginnen.</span><span class="sxs-lookup"><span data-stu-id="d6b13-147">For video content, you can request a profile level by setting [MFPKEY\_DECODERCOMPLEXITYREQUESTED](mfpkey-decodercomplexityrequestedproperty.md) before you begin encoding.</span></span> <span data-ttu-id="d6b13-148">Der Codec versucht, in den Parametern der angeforderten Komplexitäts Stufe zu codieren, aber die anderen Einstellungen, die Sie konfigurieren, haben Vorrang.</span><span class="sxs-lookup"><span data-stu-id="d6b13-148">The codec will attempt to encode within the parameters of the requested complexity level, but the other settings that you configure will take precedence.</span></span> <span data-ttu-id="d6b13-149">Sie sollten den tatsächlichen Komplexitäts Profil-Wert nach der Codierung immer überprüfen, falls Ihre Anforderung nicht berücksichtigt werden konnte.</span><span class="sxs-lookup"><span data-stu-id="d6b13-149">You should always check the actual complexity profile value after encoding in case your request could not be honored.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6b13-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d6b13-150">Requirements</span></span>



| <span data-ttu-id="d6b13-151">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d6b13-151">Requirement</span></span> | <span data-ttu-id="d6b13-152">Wert</span><span class="sxs-lookup"><span data-stu-id="d6b13-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6b13-153">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d6b13-153">Minimum supported client</span></span><br/> | <span data-ttu-id="d6b13-154">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d6b13-154">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d6b13-155">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d6b13-155">Minimum supported server</span></span><br/> | <span data-ttu-id="d6b13-156">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d6b13-156">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d6b13-157">Header</span><span class="sxs-lookup"><span data-stu-id="d6b13-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6b13-158"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6b13-158"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6b13-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6b13-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6b13-160">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d6b13-160">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




