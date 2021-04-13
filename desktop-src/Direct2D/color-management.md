---
title: Farb Verwaltungs Effekt
description: Verwenden Sie den Farb Verwaltungs Effekt, um ein Bild von einem "ICC"-Farbprofil (International Color Consortium) in ein anderes zu transformieren. Der Effekt wandelt das Bild entsprechend der ICC-Spezifikation um.
ms.assetid: 7351C4B4-F289-4236-BB42-1B3BD8753248
keywords:
- Farb Verwaltungs Effekt
ms.topic: article
ms.date: 02/05/2019
ms.openlocfilehash: 5f3783132e0e2af511a99fd8c44d5f899e577a3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391832"
---
# <a name="color-management-effect"></a><span data-ttu-id="7f128-105">Farb Verwaltungs Effekt</span><span class="sxs-lookup"><span data-stu-id="7f128-105">Color management effect</span></span>

<span data-ttu-id="7f128-106">Verwenden Sie den Farb Verwaltungs Effekt, um ein Bild von einem "ICC"-Farbprofil (International Color Consortium) in ein anderes zu transformieren.</span><span class="sxs-lookup"><span data-stu-id="7f128-106">Use the color management effect to transform an image from one ICC (International Color Consortium) color profile to another.</span></span> <span data-ttu-id="7f128-107">Der Effekt wandelt das Bild entsprechend der [ICC-Spezifikation](https://www.color.org)um.</span><span class="sxs-lookup"><span data-stu-id="7f128-107">The effect transforms the image according to the [ICC specification](https://www.color.org).</span></span>

<span data-ttu-id="7f128-108">Die CLSID für diesen Effekt ist CLSID \_ D2D1ColorManagement.</span><span class="sxs-lookup"><span data-stu-id="7f128-108">The CLSID for this effect is CLSID\_D2D1ColorManagement.</span></span>

- [<span data-ttu-id="7f128-109">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7f128-109">Effect properties</span></span>](#effect-properties)
- [<span data-ttu-id="7f128-110">Renderintent-Modi</span><span class="sxs-lookup"><span data-stu-id="7f128-110">Rendering intent modes</span></span>](#rendering-intent-modes)
- [<span data-ttu-id="7f128-111">Eingabebild-Alpha-Modi</span><span class="sxs-lookup"><span data-stu-id="7f128-111">Input image alpha modes</span></span>](#input-image-alpha-modes)
- [<span data-ttu-id="7f128-112">Konformität mit der ICC-Spezifikation</span><span class="sxs-lookup"><span data-stu-id="7f128-112">Compliance with ICC specification</span></span>](#compliance-with-icc-specification)
- [<span data-ttu-id="7f128-113">Alpha Kanal Verhalten</span><span class="sxs-lookup"><span data-stu-id="7f128-113">Alpha channel behavior</span></span>](#alpha-channel-behavior)
- [<span data-ttu-id="7f128-114">Qualitäts Modi</span><span class="sxs-lookup"><span data-stu-id="7f128-114">Quality modes</span></span>](#quality-modes)
- [<span data-ttu-id="7f128-115">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="7f128-115">Sample code</span></span>](#sample-code)
- [<span data-ttu-id="7f128-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7f128-116">Requirements</span></span>](#requirements)
- [<span data-ttu-id="7f128-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7f128-117">Related topics</span></span>](#related-topics)

## <a name="effect-properties"></a><span data-ttu-id="7f128-118">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7f128-118">Effect properties</span></span>

| <span data-ttu-id="7f128-119">Anzeige Name und indexenumeration</span><span class="sxs-lookup"><span data-stu-id="7f128-119">Display name and index enumeration</span></span> | <span data-ttu-id="7f128-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7f128-120">Description</span></span> |
|-|-|
| <span data-ttu-id="7f128-121">SourceContext</span><span class="sxs-lookup"><span data-stu-id="7f128-121">SourceContext</span></span><br/> <span data-ttu-id="7f128-122">D2D1 \_ Colormanagement- \_ Prop- \_ Quell \_ Farb \_ Kontext</span><span class="sxs-lookup"><span data-stu-id="7f128-122">D2D1\_COLORMANAGEMENT\_PROP\_SOURCE\_COLOR\_CONTEXT</span></span><br/> | <span data-ttu-id="7f128-123">Die Quell Farbraum-Informationen.</span><span class="sxs-lookup"><span data-stu-id="7f128-123">The source color space information.</span></span> <span data-ttu-id="7f128-124">Der Typ ist " [**ID2D1ColorContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext)".</span><span class="sxs-lookup"><span data-stu-id="7f128-124">The type is [**ID2D1ColorContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext).</span></span><br/> <span data-ttu-id="7f128-125">Der Standardwert ist NULL.</span><span class="sxs-lookup"><span data-stu-id="7f128-125">The default value is NULL.</span></span><br/> |
| <span data-ttu-id="7f128-126">Sourceinztent</span><span class="sxs-lookup"><span data-stu-id="7f128-126">SourceIntent</span></span><br/> <span data-ttu-id="7f128-127">D2D1 \_ Colormanagement- \_ Prop- \_ Quell \_ \_ renderabsicht</span><span class="sxs-lookup"><span data-stu-id="7f128-127">D2D1\_COLORMANAGEMENT\_PROP\_SOURCE\_RENDERING\_INTENT</span></span><br/> | <span data-ttu-id="7f128-128">Die zu verwendende ICC-renderingabsicht.</span><span class="sxs-lookup"><span data-stu-id="7f128-128">Which ICC rendering intent to use.</span></span> <span data-ttu-id="7f128-129">Der Typ ist "D2D1 \_ Colormanagement \_ RENDERING \_ INTENT".</span><span class="sxs-lookup"><span data-stu-id="7f128-129">The type is D2D1\_COLORMANAGEMENT\_RENDERING\_INTENT.</span></span><br/> <span data-ttu-id="7f128-130">Der Standardwert ist D2D1 \_ Colormanagement \_ RENDERING \_ INTENT INTENT \_ .</span><span class="sxs-lookup"><span data-stu-id="7f128-130">The default value is D2D1\_COLORMANAGEMENT\_RENDERING\_INTENT\_PERCEPTUAL.</span></span><br/> |
| <span data-ttu-id="7f128-131">Destinationcontext</span><span class="sxs-lookup"><span data-stu-id="7f128-131">DestinationContext</span></span><br/> <span data-ttu-id="7f128-132">D2D1 \_ Colormanagement- \_ Prop- \_ Ziel \_ Farb \_ Kontext</span><span class="sxs-lookup"><span data-stu-id="7f128-132">D2D1\_COLORMANAGEMENT\_PROP\_DESTINATION\_COLOR\_CONTEXT</span></span><br/> | <span data-ttu-id="7f128-133">Die Informationen zum Ziel Farbraum.</span><span class="sxs-lookup"><span data-stu-id="7f128-133">The destination color space information.</span></span> <span data-ttu-id="7f128-134">Der Typ ist " [**ID2D1ColorContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext)".</span><span class="sxs-lookup"><span data-stu-id="7f128-134">The type is [**ID2D1ColorContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext).</span></span><br/> <span data-ttu-id="7f128-135">Der Standardwert ist NULL.</span><span class="sxs-lookup"><span data-stu-id="7f128-135">The default value is NULL.</span></span><br/> |
| <span data-ttu-id="7f128-136">Destinationintent</span><span class="sxs-lookup"><span data-stu-id="7f128-136">DestinationIntent</span></span><br/> <span data-ttu-id="7f128-137">D2D1 \_ Colormanagement- \_ Prop- \_ Ziel \_ \_ renderabsicht</span><span class="sxs-lookup"><span data-stu-id="7f128-137">D2D1\_COLORMANAGEMENT\_PROP\_DESTINATION\_RENDERING\_INTENT</span></span><br/> | <span data-ttu-id="7f128-138">Die zu verwendende ICC-renderingabsicht.</span><span class="sxs-lookup"><span data-stu-id="7f128-138">Which ICC rendering intent to use.</span></span> <span data-ttu-id="7f128-139">Der Typ ist "D2D1 \_ Colormanagement \_ RENDERING \_ INTENT".</span><span class="sxs-lookup"><span data-stu-id="7f128-139">The type is D2D1\_COLORMANAGEMENT\_RENDERING\_INTENT.</span></span><br/> <span data-ttu-id="7f128-140">Der Standardwert ist D2D1 \_ Colormanagement \_ RENDERING \_ INTENT INTENT \_ .</span><span class="sxs-lookup"><span data-stu-id="7f128-140">The default value is D2D1\_COLORMANAGEMENT\_RENDERING\_INTENT\_PERCEPTUAL.</span></span><br/> |
| <span data-ttu-id="7f128-141">Alpha AMODE</span><span class="sxs-lookup"><span data-stu-id="7f128-141">AlphaMode</span></span><br/> <span data-ttu-id="7f128-142">D2D1 \_ Colormanagement- \_ Prop- \_ alpha- \_ Modus</span><span class="sxs-lookup"><span data-stu-id="7f128-142">D2D1\_COLORMANAGEMENT\_PROP\_ALPHA\_MODE</span></span><br/> | <span data-ttu-id="7f128-143">Interpretieren von Alpha-Daten, die im Eingabebild enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="7f128-143">How to interpret alpha data that is contained in the input image.</span></span> <span data-ttu-id="7f128-144">Der Typ ist der D2D1 \_ Colormanagement \_ alpha- \_ Modus.</span><span class="sxs-lookup"><span data-stu-id="7f128-144">The type is D2D1\_COLORMANAGEMENT\_ALPHA\_MODE.</span></span><br/> <span data-ttu-id="7f128-145">Der Standardwert ist "D2D1 \_ Colormanagement \_ Alpha Mode" ( \_ \_ vorab multipliziert).</span><span class="sxs-lookup"><span data-stu-id="7f128-145">The default value is D2D1\_COLORMANAGEMENT\_ALPHA\_MODE\_PREMULTIPLIED.</span></span><br/> |
| <span data-ttu-id="7f128-146">Qualität</span><span class="sxs-lookup"><span data-stu-id="7f128-146">Quality</span></span><br/> <span data-ttu-id="7f128-147">D2D1 \_ Colormanagement- \_ Prop- \_ Qualität</span><span class="sxs-lookup"><span data-stu-id="7f128-147">D2D1\_COLORMANAGEMENT\_PROP\_QUALITY</span></span><br/> | <span data-ttu-id="7f128-148">Die Qualitätsstufe der Transformation.</span><span class="sxs-lookup"><span data-stu-id="7f128-148">The quality level of the transform.</span></span> <span data-ttu-id="7f128-149">Der Typ ist "D2D1 \_ Colormanagement \_ Quality".</span><span class="sxs-lookup"><span data-stu-id="7f128-149">The type is D2D1\_COLORMANAGEMENT\_QUALITY.</span></span><br/> <span data-ttu-id="7f128-150">Der Standardwert ist D2D1 \_ Colormanagement \_ Quality \_ Normal.</span><span class="sxs-lookup"><span data-stu-id="7f128-150">The default value is D2D1\_COLORMANAGEMENT\_QUALITY\_NORMAL.</span></span><br/> |

## <a name="rendering-intent-modes"></a><span data-ttu-id="7f128-151">Renderintent-Modi</span><span class="sxs-lookup"><span data-stu-id="7f128-151">Rendering intent modes</span></span>

| <span data-ttu-id="7f128-152">Enumeration</span><span class="sxs-lookup"><span data-stu-id="7f128-152">Enumeration</span></span> | <span data-ttu-id="7f128-153">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7f128-153">Description</span></span> |
|-|-|
| <span data-ttu-id="7f128-154">D2D1 \_ Colormanagement- \_ RENDERING \_ INTENT INTENT \_</span><span class="sxs-lookup"><span data-stu-id="7f128-154">D2D1\_COLORMANAGEMENT\_RENDERING\_INTENT\_PERCEPTUAL</span></span> | <span data-ttu-id="7f128-155">Der Effekt komprimiert oder erweitert den vollständigen Farb Umfang des Bilds, um den Farb Umfang des Geräts zu füllen, sodass das graue Gleichgewicht beibehalten wird, die farbige metrikgenauigkeit jedoch möglicherweise nicht beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="7f128-155">The effect compresses or expands the full color gamut of the image to fill the color gamut of the device, so that gray balance is preserved but colorimetric accuracy may not be preserved.</span></span> |
| <span data-ttu-id="7f128-156">D2D1 \_ Colormanagement \_ - \_ renderabsicht \_ relative \_ farbige Metrik</span><span class="sxs-lookup"><span data-stu-id="7f128-156">D2D1\_COLORMANAGEMENT\_RENDERING\_INTENT\_RELATIVE\_COLORIMETRIC</span></span> | <span data-ttu-id="7f128-157">Der Effekt bewahrt den Chroma der Farben im Bild auf mögliche Kosten von Hue und Helligkeit.</span><span class="sxs-lookup"><span data-stu-id="7f128-157">The effect preserves the chroma of colors in the image at the possible expense of hue and lightness.</span></span> |
| <span data-ttu-id="7f128-158">D2D1 \_ Colormanagement- \_ renderingabsicht \_ \_</span><span class="sxs-lookup"><span data-stu-id="7f128-158">D2D1\_COLORMANAGEMENT\_RENDERING\_INTENT\_SATURATION</span></span> | <span data-ttu-id="7f128-159">Der Effekt passt Farben an, die außerhalb des Bereichs von Farben liegen, die das Ausgabegerät rendert, bis zur nächstgelegenen verfügbaren Farbe.</span><span class="sxs-lookup"><span data-stu-id="7f128-159">The effect adjusts colors that fall outside the range of colors the output device renders to the closest color available.</span></span> <span data-ttu-id="7f128-160">Der weiße Punkt wird nicht beibehalten.</span><span class="sxs-lookup"><span data-stu-id="7f128-160">It does not preserve the white point.</span></span> |
| <span data-ttu-id="7f128-161">D2D1 \_ Colormanagement \_ - \_ renderabsicht \_ absolute \_ farbige Metrik</span><span class="sxs-lookup"><span data-stu-id="7f128-161">D2D1\_COLORMANAGEMENT\_RENDERING\_INTENT\_ABSOLUTE\_COLORIMETRIC</span></span> | <span data-ttu-id="7f128-162">Der Effekt passt alle Farben an, die außerhalb des Bereichs liegen, den das Ausgabegerät rendern kann, bis zur nächstgelegenen Farbe, die gerendert werden kann.</span><span class="sxs-lookup"><span data-stu-id="7f128-162">The effect adjusts any colors that fall outside the range that the output device can render to the closest color that can be rendered.</span></span> <span data-ttu-id="7f128-163">Der Effekt ändert nicht die anderen Farben und behält den weißen Punkt bei.</span><span class="sxs-lookup"><span data-stu-id="7f128-163">The effect does not change the other colors and preserves the white point.</span></span> |

## <a name="input-image-alpha-modes"></a><span data-ttu-id="7f128-164">Eingabebild-Alpha-Modi</span><span class="sxs-lookup"><span data-stu-id="7f128-164">Input image alpha modes</span></span>

| <span data-ttu-id="7f128-165">Enumeration</span><span class="sxs-lookup"><span data-stu-id="7f128-165">Enumeration</span></span> | <span data-ttu-id="7f128-166">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7f128-166">Description</span></span> |
|-|-|
| <span data-ttu-id="7f128-167">D2D1 \_ Colormanagement- \_ alpha \_ Modus ist \_ vorab multipliziert</span><span class="sxs-lookup"><span data-stu-id="7f128-167">D2D1\_COLORMANAGEMENT\_ALPHA\_MODE\_PREMULTIPLIED</span></span> | <span data-ttu-id="7f128-168">Der Effekt geht davon aus, dass der Alpha-Modus vorab multipliziert ist.</span><span class="sxs-lookup"><span data-stu-id="7f128-168">The effect assumes the alpha mode is premultiplied.</span></span> |
| <span data-ttu-id="7f128-169">D2D1 \_ Colormanagement \_ alpha \_ Modus \_ direkt</span><span class="sxs-lookup"><span data-stu-id="7f128-169">D2D1\_COLORMANAGEMENT\_ALPHA\_MODE\_STRAIGHT</span></span> | <span data-ttu-id="7f128-170">Der Effekt geht davon aus, dass der Alpha-Modus gerade ist.</span><span class="sxs-lookup"><span data-stu-id="7f128-170">The effect assumes the alpha mode is straight.</span></span> |

## <a name="d2d1_gamma1_g2084-behavior-changes"></a><span data-ttu-id="7f128-171">D2D1_GAMMA1_G2084 Verhaltensänderungen</span><span class="sxs-lookup"><span data-stu-id="7f128-171">D2D1_GAMMA1_G2084 behavior changes</span></span>
    
<span data-ttu-id="7f128-172">Wenn Ihre Anwendung den [D2D1_GAMMA1_G2084](/windows/desktop/api/d2d1_3/ne-d2d1_3-d2d1_gamma1) Raum oder einen der [DXGI_COLOR_SPACE_TYPE](/windows/desktop/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) Enumerationswerte verwendet, die den SMPTE St. 2084-Farbraum (perzeptive Quantizer) verwenden, beabsichtigt die Anwendung, mit HDR-Daten zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="7f128-172">If your application uses the [D2D1_GAMMA1_G2084](/windows/desktop/api/d2d1_3/ne-d2d1_3-d2d1_gamma1) space, or one of the [DXGI_COLOR_SPACE_TYPE](/windows/desktop/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) enumeration values that use the SMPTE ST.2084 (Perceptual Quantizer) color space, then the application intends to work with HDR data.</span></span>

<span data-ttu-id="7f128-173">Die [**ID2D1DeviceContext5:::: | atecolorcontextfromsimplecolorprofile**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromsimplecolorprofile(constd2d1_simple_color_profile__id2d1colorcontext1)) -und [**ID2D1DeviceContext5:: roatecolorcontextfromdxgicolorspace**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromdxgicolorspace) -APIs berücksichtigen das nicht. Stattdessen wird der HDR-Inhalt so skaliert, dass er während des G2084 Degamma-Vorgangs in den Bereich 0-1 passt.</span><span class="sxs-lookup"><span data-stu-id="7f128-173">The [**ID2D1DeviceContext5::CreateColorContextFromSimpleColorProfile**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromsimplecolorprofile(constd2d1_simple_color_profile__id2d1colorcontext1)) and [**ID2D1DeviceContext5::CreateColorContextFromDxgiColorSpace**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromdxgicolorspace) APIs don't account for that; rather, the HDR content is scaled to fit in the 0-1 range during the G2084 DeGamma operation.</span></span>

<span data-ttu-id="7f128-174">In der Praxis verwendet der in diesem Gamma Bereich codierte Inhalt eine Verweis whitelevel von 10.000 Nits, die normalerweise in CCCS als 10.000/80 = 125,0 dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="7f128-174">In practice, content that is encoded in this gamma space uses a reference WhiteLevel of 10,000 Nits, which would normally be represented in CCCS as 10,000 / 80 = 125.0.</span></span> <span data-ttu-id="7f128-175">Um Ihre APP besser zu vereinfachen, ist es am einfachsten, dass diese Gamma Konvertierung auch die Helligkeit um den Faktor 125 skaliert.</span><span class="sxs-lookup"><span data-stu-id="7f128-175">So, to better facilitate your app, it's simplest for this gamma conversion to also scale the luminance by a factor of 125.</span></span> <span data-ttu-id="7f128-176">Ab Windows 10, Version 1809 (10,0; Build 17763), das Verhalten des Farb Verwaltungs Effekts bewirkt, dass diese Skalierung angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="7f128-176">As of Windows 10, version 1809 (10.0; Build 17763), the behavior of the color management effect is such that it applies this scaling.</span></span> <span data-ttu-id="7f128-177">Dies bedeutet, dass Sie als Entwickler keinen zweiten [Anpassungs Effekt in der weißen Ebene](white-level-adjustment-effect.md) auf die Pipeline anwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="7f128-177">That means that you, as the developer, don't have to apply a second [White level adjustment effect](white-level-adjustment-effect.md) into the pipeline.</span></span>

## <a name="compliance-with-icc-specification"></a><span data-ttu-id="7f128-178">Konformität mit der ICC-Spezifikation</span><span class="sxs-lookup"><span data-stu-id="7f128-178">Compliance with ICC specification</span></span>

<span data-ttu-id="7f128-179">Der Effekt der Farbverwaltung ist mit den folgenden Einschränkungen mit der Spezifikation von "ICC v 4.3" kompatibel:</span><span class="sxs-lookup"><span data-stu-id="7f128-179">The color management effect is compliant with the ICC v4.3 specification, with these limitations:</span></span>

- <span data-ttu-id="7f128-180">Der Effekt unterstützt 1, 3 und 4 Kanal Farbräume.</span><span class="sxs-lookup"><span data-stu-id="7f128-180">The effect supports 1, 3, and 4 channel color spaces.</span></span>
- <span data-ttu-id="7f128-181">Der Effekt unterstützt keine colorspace-oder Named Color-Profile.</span><span class="sxs-lookup"><span data-stu-id="7f128-181">The effect doesn't support ColorSpace or Named Color profiles.</span></span>

## <a name="alpha-channel-behavior"></a><span data-ttu-id="7f128-182">Alpha Kanal Verhalten</span><span class="sxs-lookup"><span data-stu-id="7f128-182">Alpha channel behavior</span></span>

<span data-ttu-id="7f128-183">Im Allgemeinen legt der Effekt Alpha auf 1 (nicht transparent) fest, wenn keine Alpha Daten im Quell Abbild vorhanden sind und die Alpha Daten verworfen werden, wenn das Ziel Image keinen Platz hat.</span><span class="sxs-lookup"><span data-stu-id="7f128-183">In general, the effect sets alpha to 1 (opaque) if there is no alpha data in the source image and the alpha data is discarded if there is no room in the destination image.</span></span> <span data-ttu-id="7f128-184">In der folgenden Tabelle wird das Alpha Verhalten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="7f128-184">The table here describes the alpha behavior.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="7f128-185">Color Space-Quelle, Pixel Format</span><span class="sxs-lookup"><span data-stu-id="7f128-185">Source colorspace, pixel format</span></span></th>
<th><span data-ttu-id="7f128-186">Color Space-Ziel, Pixel Format</span><span class="sxs-lookup"><span data-stu-id="7f128-186">Destination colorspace, pixel format</span></span></th>
<th><span data-ttu-id="7f128-187">Alpha-Verhalten</span><span class="sxs-lookup"><span data-stu-id="7f128-187">Alpha behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="4"><span data-ttu-id="7f128-188">1 Channel, R-Pixel-Format $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="7f128-188">1 channel, R pixel format ${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="7f128-189">1 Channel, R-Pixel-Format</span><span class="sxs-lookup"><span data-stu-id="7f128-189">1 channel, R pixel format</span></span></td>
<td><span data-ttu-id="7f128-190">(Keine Alpha Daten)</span><span class="sxs-lookup"><span data-stu-id="7f128-190">(No alpha data)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7f128-191">1 Kanal, RGBA-Pixel Format</span><span class="sxs-lookup"><span data-stu-id="7f128-191">1 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="7f128-192">Alpha Daten sind auf 1 (nicht transparent) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7f128-192">Alpha data is set to 1 (opaque)</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="7f128-193">3 Channel, RGBA-Pixel Format</span><span class="sxs-lookup"><span data-stu-id="7f128-193">3 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="7f128-194">Alpha Daten sind auf 1 (nicht transparent) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7f128-194">Alpha data is set to 1 (opaque)</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="7f128-195">4 Channel, RGBA-Pixel Format</span><span class="sxs-lookup"><span data-stu-id="7f128-195">4 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="7f128-196">(Keine Alpha Daten)</span><span class="sxs-lookup"><span data-stu-id="7f128-196">(No alpha data)</span></span></td>

</tr>
<tr class="odd">
<td rowspan="4"><span data-ttu-id="7f128-197">1 Channel, RGBA-Pixel Format $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="7f128-197">1 channel, RGBA pixel format ${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="7f128-198">1 Channel, R-Pixel-Format</span><span class="sxs-lookup"><span data-stu-id="7f128-198">1 channel, R pixel format</span></span></td>
<td><span data-ttu-id="7f128-199">Alpha Daten werden verworfen.</span><span class="sxs-lookup"><span data-stu-id="7f128-199">Alpha data is discarded</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7f128-200">1 Kanal, RGBA-Pixel Format</span><span class="sxs-lookup"><span data-stu-id="7f128-200">1 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="7f128-201">Alpha Daten werden durchlaufen</span><span class="sxs-lookup"><span data-stu-id="7f128-201">Alpha data is passed through</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="7f128-202">3 Channel, RGBA-Pixel Format</span><span class="sxs-lookup"><span data-stu-id="7f128-202">3 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="7f128-203">Alpha Daten werden durchlaufen</span><span class="sxs-lookup"><span data-stu-id="7f128-203">Alpha data is passed through</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="7f128-204">4 Channel, RGBA-Pixel Format</span><span class="sxs-lookup"><span data-stu-id="7f128-204">4 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="7f128-205">Alpha Daten werden verworfen.</span><span class="sxs-lookup"><span data-stu-id="7f128-205">Alpha data is discarded</span></span></td>

</tr>
<tr class="odd">
<td rowspan="4"><span data-ttu-id="7f128-206">3 Channel, RGBA-Pixel Format $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="7f128-206">3 channel, RGBA pixel format ${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="7f128-207">1 Channel, R-Pixel-Format</span><span class="sxs-lookup"><span data-stu-id="7f128-207">1 channel, R pixel format</span></span></td>
<td><span data-ttu-id="7f128-208">Alpha Daten werden verworfen.</span><span class="sxs-lookup"><span data-stu-id="7f128-208">Alpha data is discarded</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7f128-209">1 Kanal, RGBA-Pixel Format</span><span class="sxs-lookup"><span data-stu-id="7f128-209">1 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="7f128-210">Alpha Daten werden durchlaufen</span><span class="sxs-lookup"><span data-stu-id="7f128-210">Alpha data is passed through</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="7f128-211">3 Channel, RGBA-Pixel Format</span><span class="sxs-lookup"><span data-stu-id="7f128-211">3 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="7f128-212">Alpha Daten werden durchlaufen</span><span class="sxs-lookup"><span data-stu-id="7f128-212">Alpha data is passed through</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="7f128-213">4 Channel, RGBA-Pixel Format</span><span class="sxs-lookup"><span data-stu-id="7f128-213">4 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="7f128-214">Alpha Daten werden verworfen.</span><span class="sxs-lookup"><span data-stu-id="7f128-214">Alpha data is discarded</span></span></td>

</tr>
<tr class="odd">
<td rowspan="4"><span data-ttu-id="7f128-215">4 Channel, RGBA-Pixel Format $ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="7f128-215">4 channel, RGBA pixel format ${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="7f128-216">1 Channel, R-Pixel-Format</span><span class="sxs-lookup"><span data-stu-id="7f128-216">1 channel, R pixel format</span></span></td>
<td><span data-ttu-id="7f128-217">(Keine Alpha Daten)</span><span class="sxs-lookup"><span data-stu-id="7f128-217">(No alpha data)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7f128-218">1 Kanal, RGBA-Pixel Format</span><span class="sxs-lookup"><span data-stu-id="7f128-218">1 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="7f128-219">Alpha Daten sind auf 1 (nicht transparent) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7f128-219">Alpha data is set to 1 (opaque)</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="7f128-220">3 Channel, RGBA-Pixel Format</span><span class="sxs-lookup"><span data-stu-id="7f128-220">3 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="7f128-221">Alpha Daten sind auf 1 (nicht transparent) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7f128-221">Alpha data is set to 1 (opaque)</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="7f128-222">4 Channel, RGBA-Pixel Format</span><span class="sxs-lookup"><span data-stu-id="7f128-222">4 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="7f128-223">(Keine Alpha Daten)</span><span class="sxs-lookup"><span data-stu-id="7f128-223">(No alpha data)</span></span></td>

</tr>
</tbody>
</table>

## <a name="quality-modes"></a><span data-ttu-id="7f128-224">Qualitäts Modi</span><span class="sxs-lookup"><span data-stu-id="7f128-224">Quality modes</span></span>

| <span data-ttu-id="7f128-225">Mode</span><span class="sxs-lookup"><span data-stu-id="7f128-225">Mode</span></span> | <span data-ttu-id="7f128-226">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7f128-226">Description</span></span> |
|-|-|
| <span data-ttu-id="7f128-227">D2D1 \_ Colormanagement- \_ Qualitäts \_ Nachweis</span><span class="sxs-lookup"><span data-stu-id="7f128-227">D2D1\_COLORMANAGEMENT\_QUALITY\_PROOF</span></span> | <span data-ttu-id="7f128-228">Der Modus mit der niedrigsten Qualität.</span><span class="sxs-lookup"><span data-stu-id="7f128-228">The lowest quality mode.</span></span> <span data-ttu-id="7f128-229">Für diesen Modus ist die Featureebene 9 \_ 1 oder höher erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7f128-229">This mode requires feature level 9\_1 or above.</span></span> |
| <span data-ttu-id="7f128-230">D2D1 \_ Colormanagement- \_ Qualität \_ Normal</span><span class="sxs-lookup"><span data-stu-id="7f128-230">D2D1\_COLORMANAGEMENT\_QUALITY\_NORMAL</span></span> | <span data-ttu-id="7f128-231">Normaler Qualitäts Modus.</span><span class="sxs-lookup"><span data-stu-id="7f128-231">Normal quality mode.</span></span> <span data-ttu-id="7f128-232">Für diesen Modus ist die Featureebene 9 \_ 1 oder höher erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7f128-232">This mode requires feature level 9\_1 or above.</span></span> |
| <span data-ttu-id="7f128-233">D2D1 \_ Colormanagement- \_ Qualität \_ am besten</span><span class="sxs-lookup"><span data-stu-id="7f128-233">D2D1\_COLORMANAGEMENT\_QUALITY\_BEST</span></span> | <span data-ttu-id="7f128-234">Der Modus für die beste Qualität.</span><span class="sxs-lookup"><span data-stu-id="7f128-234">The best quality mode.</span></span> <span data-ttu-id="7f128-235">Für diesen Modus sind die Featureebene 10 \_ 0 oder höher sowie die Puffer für Gleit Komma Genauigkeit erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7f128-235">This mode requires feature level 10\_0 or above, as well as floating point precision buffers.</span></span> <span data-ttu-id="7f128-236">Dieser Modus unterstützt die Genauigkeit von Gleit Komma Werten und den erweiterten Bereich, wie in der Spezifikation von "ICC v 4.3" definiert.</span><span class="sxs-lookup"><span data-stu-id="7f128-236">This mode supports floating point precision as well as extended range as defined in the ICC v4.3 specification.</span></span> |

<span data-ttu-id="7f128-237">Der Farb Verwaltungs Effekt schlägt fehl, wenn die Anwendung einen Qualitäts Modus anfordert, der von der Hardware nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="7f128-237">The color management effect fails when drawing if the application requests a quality mode that is not supported by the hardware.</span></span> <span data-ttu-id="7f128-238">Sie können die Featureebene ermitteln, wenn Sie [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice)aufgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="7f128-238">You can determine the feature level when you call [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice).</span></span> <span data-ttu-id="7f128-239">Sie können die Unterstützung für Gleit Komma Puffer überprüfen, indem Sie [**ID2D1EffectContext:: isbufferprecisionsupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isbufferprecisionsupported) mit dem Wert [**D2D1 \_ buffer \_ Precision \_ 32bpc \_ float**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_buffer_precision)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7f128-239">You can check for floating point buffer support by calling [**ID2D1EffectContext::IsBufferPrecisionSupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isbufferprecisionsupported) with the value [**D2D1\_BUFFER\_PRECISION\_32BPC\_FLOAT**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_buffer_precision).</span></span>

## <a name="sample-code"></a><span data-ttu-id="7f128-240">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="7f128-240">Sample code</span></span>

<span data-ttu-id="7f128-241">Ein Beispiel für diesen Effekt finden Sie unter Beispiel für die [Photo-Anpassung Direct2D Effects](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/D2DPhotoAdjustment)und in Lektion 4 des Beispiels.</span><span class="sxs-lookup"><span data-stu-id="7f128-241">For an example of this effect, download the [Direct2D effects photo adjustment sample](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/D2DPhotoAdjustment), and see Lesson 4 of the sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f128-242">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7f128-242">Requirements</span></span>

| <span data-ttu-id="7f128-243">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7f128-243">Requirement</span></span> | <span data-ttu-id="7f128-244">Wert</span><span class="sxs-lookup"><span data-stu-id="7f128-244">Value</span></span> |
|-|-|
| <span data-ttu-id="7f128-245">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7f128-245">Minimum supported client</span></span> | <span data-ttu-id="7f128-246">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7f128-246">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="7f128-247">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7f128-247">Minimum supported server</span></span> | <span data-ttu-id="7f128-248">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7f128-248">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="7f128-249">Header</span><span class="sxs-lookup"><span data-stu-id="7f128-249">Header</span></span> | <span data-ttu-id="7f128-250">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="7f128-250">d2d1effects.h</span></span> |
| <span data-ttu-id="7f128-251">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7f128-251">Library</span></span> | <span data-ttu-id="7f128-252">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="7f128-252">d2d1.lib, dxguid.lib</span></span> |

## <a name="related-topics"></a><span data-ttu-id="7f128-253">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7f128-253">Related topics</span></span>

* [<span data-ttu-id="7f128-254">ID2D1Effect-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="7f128-254">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
