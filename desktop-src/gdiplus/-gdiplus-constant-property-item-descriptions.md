---
description: Die folgende Liste enthält Beschreibungen der Eigenschaften Elemente, die von Windows GDI+ unterstützt werden.
ms.assetid: fc95aa3f-8381-430d-8cbf-6d23816a738d
title: Eigenschaften Element Beschreibungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc2a627ec809bb4f7d7299c522fd0e9d3e1cc05
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/27/2021
ms.locfileid: "105636122"
---
# <a name="property-item-descriptions"></a><span data-ttu-id="d1e65-103">Eigenschaften Element Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="d1e65-103">Property Item Descriptions</span></span>

<span data-ttu-id="d1e65-104">Die folgende Liste enthält Beschreibungen der Eigenschaften Elemente, die von Windows GDI+ unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="d1e65-104">The following list gives descriptions of the property items supported by Windows GDI+.</span></span> <span data-ttu-id="d1e65-105">Die Beschreibungen sind kurz und allgemein, sodass Sie auf eine Vielzahl von Bild Dateiformaten angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="d1e65-105">The descriptions are brief and general so that they apply to a variety of image file formats.</span></span> <span data-ttu-id="d1e65-106">Eine ausführliche Beschreibung der Verwendung eines Eigenschafts Elements in einem bestimmten Dateiformat finden Sie in der Spezifikation für dieses Dateiformat.</span><span class="sxs-lookup"><span data-stu-id="d1e65-106">For a detailed description of how a property item is used by a particular file format, see the specification for that file format.</span></span> <span data-ttu-id="d1e65-107">Links zu mehreren Datei Spezifikationen und anderen Dokumenten, in denen Metadaten ausführlich beschrieben werden, finden Sie unter [Spezifikation von Image Dateiformaten](-gdiplus-constant-image-file-format-specifications.md).</span><span class="sxs-lookup"><span data-stu-id="d1e65-107">For links to several file specifications and other documents that describe metadata in detail, see [Image File Format Specifications](-gdiplus-constant-image-file-format-specifications.md).</span></span>

<span data-ttu-id="d1e65-108">Das EXIF-Format (austauschbar Image File) ist ein JEIDA-Standard (Electronic Electronic Industry Development Association), der vom Juni 1998 als Version 2,1 überarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="d1e65-108">The Exchangeable Image File (EXIF) format is a Japan Electronic Industry Development Association (JEIDA) standard, revised June 1998 as version 2.1.</span></span> <span data-ttu-id="d1e65-109">Teile der EXIF-Spezifikation werden mit der Berechtigung JEIDA verwendet.</span><span class="sxs-lookup"><span data-stu-id="d1e65-109">Portions of the EXIF specification are used with permission of JEIDA.</span></span>

## <a name="propertytaggpsver"></a><span data-ttu-id="d1e65-110">Propertytaggpsver</span><span class="sxs-lookup"><span data-stu-id="d1e65-110">PropertyTagGpsVer</span></span>

<span data-ttu-id="d1e65-111">Version der Global Positionierungs Systems (GPS) IFD, die als 2.0.0.0 angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="d1e65-111">Version of the Global Positioning Systems (GPS) IFD, given as 2.0.0.0.</span></span> <span data-ttu-id="d1e65-112">Dieses Tag ist obligatorisch, wenn das propertytaggpsifd-Tag vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="d1e65-112">This tag is mandatory when the PropertyTagGpsIFD tag is present.</span></span> <span data-ttu-id="d1e65-113">Wenn die Version 2.0.0.0 ist, ist der Tagwert 0x02000000.</span><span class="sxs-lookup"><span data-stu-id="d1e65-113">When the version is 2.0.0.0, the tag value is 0x02000000.</span></span>



| <span data-ttu-id="d1e65-114">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-114">Property info</span></span> | <span data-ttu-id="d1e65-115">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-115">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="d1e65-116">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-116">Tag</span></span>   | <span data-ttu-id="d1e65-117">0x0000</span><span class="sxs-lookup"><span data-stu-id="d1e65-117">0x0000</span></span>              |
| <span data-ttu-id="d1e65-118">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-118">Type</span></span>  | <span data-ttu-id="d1e65-119">Propertytagtypebyte</span><span class="sxs-lookup"><span data-stu-id="d1e65-119">PropertyTagTypeByte</span></span> |
| <span data-ttu-id="d1e65-120">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-120">Count</span></span> | <span data-ttu-id="d1e65-121">4</span><span class="sxs-lookup"><span data-stu-id="d1e65-121">4</span></span>                   |



 

## <a name="propertytaggpslatituderef"></a><span data-ttu-id="d1e65-122">Propertytaggpslatituderef</span><span class="sxs-lookup"><span data-stu-id="d1e65-122">PropertyTagGpsLatitudeRef</span></span>

<span data-ttu-id="d1e65-123">Mit NULL beendete Zeichenfolge, die angibt, ob der Breitengrad "North" oder "South" ist.</span><span class="sxs-lookup"><span data-stu-id="d1e65-123">Null-terminated character string that specifies whether the latitude is north or south.</span></span> <span data-ttu-id="d1e65-124">`N` Gibt die nördliche Breite an und `S` gibt den südlichen Breitengrad an.</span><span class="sxs-lookup"><span data-stu-id="d1e65-124">`N` specifies north latitude, and `S` specifies south latitude.</span></span>



| <span data-ttu-id="d1e65-125">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-125">Property info</span></span> | <span data-ttu-id="d1e65-126">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-126">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="d1e65-127">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-127">Tag</span></span>   | <span data-ttu-id="d1e65-128">0x0001</span><span class="sxs-lookup"><span data-stu-id="d1e65-128">0x0001</span></span>                                     |
| <span data-ttu-id="d1e65-129">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-129">Type</span></span>  | <span data-ttu-id="d1e65-130">Propertytagtybäuercii</span><span class="sxs-lookup"><span data-stu-id="d1e65-130">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="d1e65-131">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-131">Count</span></span> | <span data-ttu-id="d1e65-132">2 (ein Zeichen plus das NULL-Terminator)</span><span class="sxs-lookup"><span data-stu-id="d1e65-132">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpslatitude"></a><span data-ttu-id="d1e65-133">Propertytaggpslatitude</span><span class="sxs-lookup"><span data-stu-id="d1e65-133">PropertyTagGpsLatitude</span></span>

<span data-ttu-id="d1e65-134">Die Breitenkoordinate.</span><span class="sxs-lookup"><span data-stu-id="d1e65-134">Latitude.</span></span> <span data-ttu-id="d1e65-135">Der Breitengrad wird als drei rationale Werte ausgedrückt, die den Grad, die Minuten und die Sekunden geben.</span><span class="sxs-lookup"><span data-stu-id="d1e65-135">Latitude is expressed as three rational values giving the degrees, minutes, and seconds respectively.</span></span> <span data-ttu-id="d1e65-136">Wenn Grad, Minuten und Sekunden ausgedrückt werden, ist das Format dd/1, mm/1, SS/1.</span><span class="sxs-lookup"><span data-stu-id="d1e65-136">When degrees, minutes, and seconds are expressed, the format is dd/1, mm/1, ss/1.</span></span> <span data-ttu-id="d1e65-137">Wenn Grad und Minuten verwendet werden und z. b. ein Bruchteil von Minuten bis zu zwei Dezimalstellen erhalten, ist das Format dd/1, MMMM/100, 0/1.</span><span class="sxs-lookup"><span data-stu-id="d1e65-137">When degrees and minutes are used and, for example, fractions of minutes are given up to two decimal places, the format is dd/1, mmmm/100, 0/1.</span></span>



| <span data-ttu-id="d1e65-138">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-138">Property info</span></span> | <span data-ttu-id="d1e65-139">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-139">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="d1e65-140">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-140">Tag</span></span>   | <span data-ttu-id="d1e65-141">0x0002</span><span class="sxs-lookup"><span data-stu-id="d1e65-141">0x0002</span></span>                  |
| <span data-ttu-id="d1e65-142">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-142">Type</span></span>  | <span data-ttu-id="d1e65-143">Propertytagtyperational</span><span class="sxs-lookup"><span data-stu-id="d1e65-143">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="d1e65-144">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-144">Count</span></span> | <span data-ttu-id="d1e65-145">3</span><span class="sxs-lookup"><span data-stu-id="d1e65-145">3</span></span>                       |



 

## <a name="propertytaggpslongituderef"></a><span data-ttu-id="d1e65-146">Propertytaggpslängs</span><span class="sxs-lookup"><span data-stu-id="d1e65-146">PropertyTagGpsLongitudeRef</span></span>

<span data-ttu-id="d1e65-147">Eine mit NULL endend beendete Zeichenfolge, die angibt, ob der Längengrad Ost-oder West-Längengrad ist.</span><span class="sxs-lookup"><span data-stu-id="d1e65-147">Null-terminated character string that specifies whether the longitude is east or west longitude.</span></span> <span data-ttu-id="d1e65-148">`E` Gibt den Ost-Längengrad an und `W` gibt den West Längengrad an.</span><span class="sxs-lookup"><span data-stu-id="d1e65-148">`E` specifies east longitude, and `W` specifies west longitude.</span></span>



| <span data-ttu-id="d1e65-149">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-149">Property info</span></span> | <span data-ttu-id="d1e65-150">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-150">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="d1e65-151">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-151">Tag</span></span>   | <span data-ttu-id="d1e65-152">0x0003</span><span class="sxs-lookup"><span data-stu-id="d1e65-152">0x0003</span></span>                                     |
| <span data-ttu-id="d1e65-153">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-153">Type</span></span>  | <span data-ttu-id="d1e65-154">Propertytagtybäuercii</span><span class="sxs-lookup"><span data-stu-id="d1e65-154">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="d1e65-155">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-155">Count</span></span> | <span data-ttu-id="d1e65-156">2 (ein Zeichen plus das NULL-Terminator)</span><span class="sxs-lookup"><span data-stu-id="d1e65-156">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpslongitude"></a><span data-ttu-id="d1e65-157">Propertytaggpslängen Grad</span><span class="sxs-lookup"><span data-stu-id="d1e65-157">PropertyTagGpsLongitude</span></span>

<span data-ttu-id="d1e65-158">Die Längenkoordinate.</span><span class="sxs-lookup"><span data-stu-id="d1e65-158">Longitude.</span></span> <span data-ttu-id="d1e65-159">Der Längengrad wird als drei rationale Werte ausgedrückt, die den Grad, die Minuten und die Sekunden geben.</span><span class="sxs-lookup"><span data-stu-id="d1e65-159">Longitude is expressed as three rational values giving the degrees, minutes, and seconds respectively.</span></span> <span data-ttu-id="d1e65-160">Wenn Grad, Minuten und Sekunden ausgedrückt werden, lautet das Format DDD/1, mm/1, SS/1.</span><span class="sxs-lookup"><span data-stu-id="d1e65-160">When degrees, minutes and seconds are expressed, the format is ddd/1, mm/1, ss/1.</span></span> <span data-ttu-id="d1e65-161">Wenn Grad und Minuten verwendet werden und z. b. Bruchteile von Minuten bis zu zwei Dezimalstellen angegeben werden, lautet das Format DDD/1, MMMM/100, 0/1.</span><span class="sxs-lookup"><span data-stu-id="d1e65-161">When degrees and minutes are used and, for example, fractions of minutes are given up to two decimal places, the format is ddd/1, mmmm/100, 0/1.</span></span>



| <span data-ttu-id="d1e65-162">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-162">Property info</span></span> | <span data-ttu-id="d1e65-163">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-163">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="d1e65-164">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-164">Tag</span></span>   | <span data-ttu-id="d1e65-165">0x0004</span><span class="sxs-lookup"><span data-stu-id="d1e65-165">0x0004</span></span>                  |
| <span data-ttu-id="d1e65-166">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-166">Type</span></span>  | <span data-ttu-id="d1e65-167">Propertytagtyperational</span><span class="sxs-lookup"><span data-stu-id="d1e65-167">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="d1e65-168">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-168">Count</span></span> | <span data-ttu-id="d1e65-169">3</span><span class="sxs-lookup"><span data-stu-id="d1e65-169">3</span></span>                       |



 

## <a name="propertytaggpsaltituderef"></a><span data-ttu-id="d1e65-170">Propertytaggpsaltituderef</span><span class="sxs-lookup"><span data-stu-id="d1e65-170">PropertyTagGpsAltitudeRef</span></span>

<span data-ttu-id="d1e65-171">Bezugs Höhe in Meter.</span><span class="sxs-lookup"><span data-stu-id="d1e65-171">Reference altitude, in meters.</span></span>



| <span data-ttu-id="d1e65-172">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-172">Property info</span></span> | <span data-ttu-id="d1e65-173">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-173">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="d1e65-174">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-174">Tag</span></span>   | <span data-ttu-id="d1e65-175">0x0005</span><span class="sxs-lookup"><span data-stu-id="d1e65-175">0x0005</span></span>              |
| <span data-ttu-id="d1e65-176">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-176">Type</span></span>  | <span data-ttu-id="d1e65-177">Propertytagtypebyte</span><span class="sxs-lookup"><span data-stu-id="d1e65-177">PropertyTagTypeByte</span></span> |
| <span data-ttu-id="d1e65-178">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-178">Count</span></span> | <span data-ttu-id="d1e65-179">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-179">1</span></span>                   |



 

## <a name="propertytaggpsaltitude"></a><span data-ttu-id="d1e65-180">Propertytaggpsaltitude</span><span class="sxs-lookup"><span data-stu-id="d1e65-180">PropertyTagGpsAltitude</span></span>

<span data-ttu-id="d1e65-181">Die Höhe in Meter basierend auf der durch propertytaggpsaltituderef angegebenen Bezugs Höhe.</span><span class="sxs-lookup"><span data-stu-id="d1e65-181">Altitude, in meters, based on the reference altitude specified by PropertyTagGpsAltitudeRef.</span></span>



| <span data-ttu-id="d1e65-182">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-182">Property info</span></span> | <span data-ttu-id="d1e65-183">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-183">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="d1e65-184">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-184">Tag</span></span>   | <span data-ttu-id="d1e65-185">0x0006</span><span class="sxs-lookup"><span data-stu-id="d1e65-185">0x0006</span></span>                  |
| <span data-ttu-id="d1e65-186">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-186">Type</span></span>  | <span data-ttu-id="d1e65-187">Propertytagtyperational</span><span class="sxs-lookup"><span data-stu-id="d1e65-187">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="d1e65-188">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-188">Count</span></span> | <span data-ttu-id="d1e65-189">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-189">1</span></span>                       |



 

## <a name="propertytaggpsgpstime"></a><span data-ttu-id="d1e65-190">Propertytaggpsgpstime</span><span class="sxs-lookup"><span data-stu-id="d1e65-190">PropertyTagGpsGpsTime</span></span>

<span data-ttu-id="d1e65-191">Zeit als koordinierte Weltzeit (UTC).</span><span class="sxs-lookup"><span data-stu-id="d1e65-191">Time as Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="d1e65-192">Der Wert wird als drei rationale Zahlen ausgedrückt, die Stunde, Minute und Sekunde.</span><span class="sxs-lookup"><span data-stu-id="d1e65-192">The value is expressed as three rational numbers that give the hour, minute, and second.</span></span>



| <span data-ttu-id="d1e65-193">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-193">Property info</span></span> | <span data-ttu-id="d1e65-194">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-194">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="d1e65-195">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-195">Tag</span></span>   | <span data-ttu-id="d1e65-196">0x0007</span><span class="sxs-lookup"><span data-stu-id="d1e65-196">0x0007</span></span>                  |
| <span data-ttu-id="d1e65-197">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-197">Type</span></span>  | <span data-ttu-id="d1e65-198">Propertytagtyperational</span><span class="sxs-lookup"><span data-stu-id="d1e65-198">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="d1e65-199">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-199">Count</span></span> | <span data-ttu-id="d1e65-200">3</span><span class="sxs-lookup"><span data-stu-id="d1e65-200">3</span></span>                       |



 

## <a name="propertytaggpsgpssatellites"></a><span data-ttu-id="d1e65-201">Propertytaggpsgpssatellites</span><span class="sxs-lookup"><span data-stu-id="d1e65-201">PropertyTagGpsGpsSatellites</span></span>

<span data-ttu-id="d1e65-202">Eine auf NULL endende Zeichenfolge, die die für Messungen verwendeten GPS-Satelliten angibt.</span><span class="sxs-lookup"><span data-stu-id="d1e65-202">Null-terminated character string that specifies the GPS satellites used for measurements.</span></span> <span data-ttu-id="d1e65-203">Dieses Tag kann verwendet werden, um die ID-Nummer, den Winkel der Höhe, die Azimuth, SNR und weitere Informationen zu den einzelnen Satelliten anzugeben.</span><span class="sxs-lookup"><span data-stu-id="d1e65-203">This tag can be used to specify the ID number, angle of elevation, azimuth, SNR, and other information about each satellite.</span></span> <span data-ttu-id="d1e65-204">Das Format ist nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="d1e65-204">The format is not specified.</span></span> <span data-ttu-id="d1e65-205">Wenn der GPS-Empfänger nicht in der Lage ist, Messungen durchzusetzen, muss der Wert des Tags auf **null** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="d1e65-205">If the GPS receiver is incapable of taking measurements, the value of the tag must be set to **NULL**.</span></span>



| <span data-ttu-id="d1e65-206">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-206">Property info</span></span> | <span data-ttu-id="d1e65-207">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-207">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="d1e65-208">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-208">Tag</span></span>   | <span data-ttu-id="d1e65-209">0x0008</span><span class="sxs-lookup"><span data-stu-id="d1e65-209">0x0008</span></span>                                             |
| <span data-ttu-id="d1e65-210">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-210">Type</span></span>  | <span data-ttu-id="d1e65-211">Propertytagtybäuercii</span><span class="sxs-lookup"><span data-stu-id="d1e65-211">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="d1e65-212">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-212">Count</span></span> | <span data-ttu-id="d1e65-213">Länge der Zeichenfolge einschließlich des NULL-Terminator</span><span class="sxs-lookup"><span data-stu-id="d1e65-213">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytaggpsgpsstatus"></a><span data-ttu-id="d1e65-214">Propertytaggpsgpsstatus</span><span class="sxs-lookup"><span data-stu-id="d1e65-214">PropertyTagGpsGpsStatus</span></span>

<span data-ttu-id="d1e65-215">Mit NULL beendete Zeichenfolge, die den Status des GPS-Empfängers angibt, wenn das Bild aufgezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="d1e65-215">Null-terminated character string that specifies the status of the GPS receiver when the image is recorded.</span></span> <span data-ttu-id="d1e65-216">`A` bedeutet, dass die Messung ausgeführt wird, und bedeutet, dass `V` die Messung Interoperabilität ist.</span><span class="sxs-lookup"><span data-stu-id="d1e65-216">`A` means measurement is in progress, and `V` means the measurement is Interoperability.</span></span>



| <span data-ttu-id="d1e65-217">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-217">Property info</span></span> | <span data-ttu-id="d1e65-218">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-218">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="d1e65-219">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-219">Tag</span></span>   | <span data-ttu-id="d1e65-220">0x0009</span><span class="sxs-lookup"><span data-stu-id="d1e65-220">0x0009</span></span>                                     |
| <span data-ttu-id="d1e65-221">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-221">Type</span></span>  | <span data-ttu-id="d1e65-222">Propertytagtybäuercii</span><span class="sxs-lookup"><span data-stu-id="d1e65-222">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="d1e65-223">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-223">Count</span></span> | <span data-ttu-id="d1e65-224">2 (ein Zeichen plus das NULL-Terminator)</span><span class="sxs-lookup"><span data-stu-id="d1e65-224">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpsgpsmeasuremode"></a><span data-ttu-id="d1e65-225">Propertytaggpsgpsmessremode</span><span class="sxs-lookup"><span data-stu-id="d1e65-225">PropertyTagGpsGpsMeasureMode</span></span>

<span data-ttu-id="d1e65-226">Mit NULL beendete Zeichenfolge, die den GPS-Mess Modus angibt.</span><span class="sxs-lookup"><span data-stu-id="d1e65-226">Null-terminated character string that specifies the GPS measurement mode.</span></span> <span data-ttu-id="d1e65-227">`2` Gibt die 2D-Messung an und `3` legt die 3D-Messung fest.</span><span class="sxs-lookup"><span data-stu-id="d1e65-227">`2` specifies 2-D measurement, and `3` specifies 3-D measurement.</span></span>



| <span data-ttu-id="d1e65-228">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-228">Property info</span></span> | <span data-ttu-id="d1e65-229">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-229">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="d1e65-230">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-230">Tag</span></span>   | <span data-ttu-id="d1e65-231">0x000A</span><span class="sxs-lookup"><span data-stu-id="d1e65-231">0x000A</span></span>                                     |
| <span data-ttu-id="d1e65-232">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-232">Type</span></span>  | <span data-ttu-id="d1e65-233">Propertytagtybäuercii</span><span class="sxs-lookup"><span data-stu-id="d1e65-233">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="d1e65-234">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-234">Count</span></span> | <span data-ttu-id="d1e65-235">2 (ein Zeichen plus das NULL-Terminator)</span><span class="sxs-lookup"><span data-stu-id="d1e65-235">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpsgpsdop"></a><span data-ttu-id="d1e65-236">Propertytaggpsgpsdop</span><span class="sxs-lookup"><span data-stu-id="d1e65-236">PropertyTagGpsGpsDop</span></span>

<span data-ttu-id="d1e65-237">GPS-DOP (Daten Genauigkeits Grad).</span><span class="sxs-lookup"><span data-stu-id="d1e65-237">GPS DOP (data degree of precision).</span></span> <span data-ttu-id="d1e65-238">Während der 2D-Messung wird ein HDOP-Wert geschrieben, und bei der 3D-Messung wird ein PDOP-Wert geschrieben.</span><span class="sxs-lookup"><span data-stu-id="d1e65-238">An HDOP value is written during 2-D measurement, and a PDOP value is written during 3-D measurement.</span></span>



| <span data-ttu-id="d1e65-239">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-239">Property info</span></span> | <span data-ttu-id="d1e65-240">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-240">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="d1e65-241">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-241">Tag</span></span>   | <span data-ttu-id="d1e65-242">0x000B</span><span class="sxs-lookup"><span data-stu-id="d1e65-242">0x000B</span></span>                  |
| <span data-ttu-id="d1e65-243">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-243">Type</span></span>  | <span data-ttu-id="d1e65-244">Propertytagtyperational</span><span class="sxs-lookup"><span data-stu-id="d1e65-244">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="d1e65-245">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-245">Count</span></span> | <span data-ttu-id="d1e65-246">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-246">1</span></span>                       |



 

## <a name="propertytaggpsspeedref"></a><span data-ttu-id="d1e65-247">Propertytaggpsspeedref</span><span class="sxs-lookup"><span data-stu-id="d1e65-247">PropertyTagGpsSpeedRef</span></span>

<span data-ttu-id="d1e65-248">Mit NULL endende Zeichenfolge, die die Einheit angibt, die zum Ausdrücken der Geschwindigkeit der Geschwindigkeit des GPS-Empfängers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d1e65-248">Null-terminated character string that specifies the unit used to express the GPS receiver speed of movement.</span></span> <span data-ttu-id="d1e65-249">`K`, `M` und `N` stellen Kilometer pro Stunde, Meilen pro Stunde bzw. Knoten dar.</span><span class="sxs-lookup"><span data-stu-id="d1e65-249">`K`, `M`, and `N` represent kilometers per hour, miles per hour, and knots respectively.</span></span>



| <span data-ttu-id="d1e65-250">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-250">Property info</span></span> | <span data-ttu-id="d1e65-251">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-251">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="d1e65-252">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-252">Tag</span></span>   | <span data-ttu-id="d1e65-253">0x000C</span><span class="sxs-lookup"><span data-stu-id="d1e65-253">0x000C</span></span>                                     |
| <span data-ttu-id="d1e65-254">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-254">Type</span></span>  | <span data-ttu-id="d1e65-255">Propertytagtybäuercii</span><span class="sxs-lookup"><span data-stu-id="d1e65-255">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="d1e65-256">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-256">Count</span></span> | <span data-ttu-id="d1e65-257">2 (ein Zeichen plus das NULL-Terminator)</span><span class="sxs-lookup"><span data-stu-id="d1e65-257">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpsspeed"></a><span data-ttu-id="d1e65-258">Propertytaggpsspeed</span><span class="sxs-lookup"><span data-stu-id="d1e65-258">PropertyTagGpsSpeed</span></span>

<span data-ttu-id="d1e65-259">Geschwindigkeit der GPS-Empfänger Bewegung.</span><span class="sxs-lookup"><span data-stu-id="d1e65-259">Speed of the GPS receiver movement.</span></span>



| <span data-ttu-id="d1e65-260">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-260">Property info</span></span> | <span data-ttu-id="d1e65-261">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-261">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="d1e65-262">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-262">Tag</span></span>   | <span data-ttu-id="d1e65-263">0x000D</span><span class="sxs-lookup"><span data-stu-id="d1e65-263">0x000D</span></span>                  |
| <span data-ttu-id="d1e65-264">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-264">Type</span></span>  | <span data-ttu-id="d1e65-265">Propertytagtyperational</span><span class="sxs-lookup"><span data-stu-id="d1e65-265">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="d1e65-266">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-266">Count</span></span> | <span data-ttu-id="d1e65-267">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-267">1</span></span>                       |



 

## <a name="propertytaggpstrackref"></a><span data-ttu-id="d1e65-268">Propertytaggpstrackref</span><span class="sxs-lookup"><span data-stu-id="d1e65-268">PropertyTagGpsTrackRef</span></span>

<span data-ttu-id="d1e65-269">Mit NULL endende Zeichenfolge, die den Verweis zum Angeben der Richtung der GPS-Empfänger Bewegung angibt.</span><span class="sxs-lookup"><span data-stu-id="d1e65-269">Null-terminated character string that specifies the reference for giving the direction of GPS receiver movement.</span></span> <span data-ttu-id="d1e65-270">`T` Gibt die tatsächliche Richtung an und `M` gibt die Magnet Richtung an.</span><span class="sxs-lookup"><span data-stu-id="d1e65-270">`T` specifies true direction, and `M` specifies magnetic direction.</span></span>



| <span data-ttu-id="d1e65-271">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-271">Property info</span></span> | <span data-ttu-id="d1e65-272">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-272">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="d1e65-273">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-273">Tag</span></span>   | <span data-ttu-id="d1e65-274">0x000e</span><span class="sxs-lookup"><span data-stu-id="d1e65-274">0x000E</span></span>                                     |
| <span data-ttu-id="d1e65-275">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-275">Type</span></span>  | <span data-ttu-id="d1e65-276">Propertytagtybäuercii</span><span class="sxs-lookup"><span data-stu-id="d1e65-276">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="d1e65-277">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-277">Count</span></span> | <span data-ttu-id="d1e65-278">2 (ein Zeichen plus das NULL-Terminator)</span><span class="sxs-lookup"><span data-stu-id="d1e65-278">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpstrack"></a><span data-ttu-id="d1e65-279">Propertytaggpstrack</span><span class="sxs-lookup"><span data-stu-id="d1e65-279">PropertyTagGpsTrack</span></span>

<span data-ttu-id="d1e65-280">Richtung der GPS-Empfänger Bewegung.</span><span class="sxs-lookup"><span data-stu-id="d1e65-280">Direction of GPS receiver movement.</span></span> <span data-ttu-id="d1e65-281">Der Wertebereich liegt zwischen 0,00 und 359,99.</span><span class="sxs-lookup"><span data-stu-id="d1e65-281">The range of values is from 0.00 to 359.99.</span></span>



| <span data-ttu-id="d1e65-282">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-282">Property info</span></span> | <span data-ttu-id="d1e65-283">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-283">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="d1e65-284">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-284">Tag</span></span>   | <span data-ttu-id="d1e65-285">0x000F</span><span class="sxs-lookup"><span data-stu-id="d1e65-285">0x000F</span></span>                  |
| <span data-ttu-id="d1e65-286">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-286">Type</span></span>  | <span data-ttu-id="d1e65-287">Propertytagtyperational</span><span class="sxs-lookup"><span data-stu-id="d1e65-287">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="d1e65-288">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-288">Count</span></span> | <span data-ttu-id="d1e65-289">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-289">1</span></span>                       |



 

## <a name="propertytaggpsimgdirref"></a><span data-ttu-id="d1e65-290">Propertytaggpsimgdirref</span><span class="sxs-lookup"><span data-stu-id="d1e65-290">PropertyTagGpsImgDirRef</span></span>

<span data-ttu-id="d1e65-291">Mit NULL beendete Zeichenfolge, die den Verweis auf die Richtung des Bilds angibt, wenn es aufgezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="d1e65-291">Null-terminated character string that specifies the reference for the direction of the image when it is captured.</span></span> <span data-ttu-id="d1e65-292">`T` Gibt die tatsächliche Richtung an und `M` gibt die Magnet Richtung an.</span><span class="sxs-lookup"><span data-stu-id="d1e65-292">`T` specifies true direction, and `M` specifies magnetic direction.</span></span>



| <span data-ttu-id="d1e65-293">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-293">Property info</span></span> | <span data-ttu-id="d1e65-294">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-294">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="d1e65-295">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-295">Tag</span></span>   | <span data-ttu-id="d1e65-296">0x0010</span><span class="sxs-lookup"><span data-stu-id="d1e65-296">0x0010</span></span>                                     |
| <span data-ttu-id="d1e65-297">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-297">Type</span></span>  | <span data-ttu-id="d1e65-298">Propertytagtybäuercii</span><span class="sxs-lookup"><span data-stu-id="d1e65-298">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="d1e65-299">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-299">Count</span></span> | <span data-ttu-id="d1e65-300">2 (ein Zeichen plus das NULL-Terminator)</span><span class="sxs-lookup"><span data-stu-id="d1e65-300">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpsimgdir"></a><span data-ttu-id="d1e65-301">Propertytaggpsimgdir</span><span class="sxs-lookup"><span data-stu-id="d1e65-301">PropertyTagGpsImgDir</span></span>

<span data-ttu-id="d1e65-302">Richtung des Bilds, wenn es aufgezeichnet wurde.</span><span class="sxs-lookup"><span data-stu-id="d1e65-302">Direction of the image when it was captured.</span></span> <span data-ttu-id="d1e65-303">Der Wertebereich liegt zwischen 0,00 und 359,99.</span><span class="sxs-lookup"><span data-stu-id="d1e65-303">The range of values is from 0.00 to 359.99.</span></span>



| <span data-ttu-id="d1e65-304">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-304">Property info</span></span> | <span data-ttu-id="d1e65-305">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-305">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="d1e65-306">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-306">Tag</span></span>   | <span data-ttu-id="d1e65-307">0x0011</span><span class="sxs-lookup"><span data-stu-id="d1e65-307">0x0011</span></span>                  |
| <span data-ttu-id="d1e65-308">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-308">Type</span></span>  | <span data-ttu-id="d1e65-309">Propertytagtyperational</span><span class="sxs-lookup"><span data-stu-id="d1e65-309">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="d1e65-310">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-310">Count</span></span> | <span data-ttu-id="d1e65-311">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-311">1</span></span>                       |



 

## <a name="propertytaggpsmapdatum"></a><span data-ttu-id="d1e65-312">Propertytaggpsmapdatum</span><span class="sxs-lookup"><span data-stu-id="d1e65-312">PropertyTagGpsMapDatum</span></span>

<span data-ttu-id="d1e65-313">Auf NULL endende Zeichenfolge, die geodätische Umfragedaten angibt, die vom GPS-Empfänger verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d1e65-313">Null-terminated character string that specifies geodetic survey data used by the GPS receiver.</span></span> <span data-ttu-id="d1e65-314">Wenn die Umfragedaten auf Japan beschränkt sind, ist der Wert dieses Tags `TOKYO` oder `WGS-84` .</span><span class="sxs-lookup"><span data-stu-id="d1e65-314">If the survey data is restricted to Japan, the value of this tag is `TOKYO` or `WGS-84`.</span></span>



| <span data-ttu-id="d1e65-315">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-315">Property info</span></span> | <span data-ttu-id="d1e65-316">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-316">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="d1e65-317">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-317">Tag</span></span>   | <span data-ttu-id="d1e65-318">0x0012</span><span class="sxs-lookup"><span data-stu-id="d1e65-318">0x0012</span></span>                                             |
| <span data-ttu-id="d1e65-319">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-319">Type</span></span>  | <span data-ttu-id="d1e65-320">Propertytagtybäuercii</span><span class="sxs-lookup"><span data-stu-id="d1e65-320">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="d1e65-321">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-321">Count</span></span> | <span data-ttu-id="d1e65-322">Länge der Zeichenfolge einschließlich des NULL-Terminator</span><span class="sxs-lookup"><span data-stu-id="d1e65-322">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytaggpsdestlatref"></a><span data-ttu-id="d1e65-323">Propertytaggpsdestlatref</span><span class="sxs-lookup"><span data-stu-id="d1e65-323">PropertyTagGpsDestLatRef</span></span>

<span data-ttu-id="d1e65-324">Eine mit NULL endend beendete Zeichenfolge, die angibt, ob der Breitengrad des Ziel Punkts Nord-oder Südbreite ist.</span><span class="sxs-lookup"><span data-stu-id="d1e65-324">Null-terminated character string that specifies whether the latitude of the destination point is north or south latitude.</span></span> <span data-ttu-id="d1e65-325">`N` Gibt die nördliche Breite an und `S` gibt den südlichen Breitengrad an.</span><span class="sxs-lookup"><span data-stu-id="d1e65-325">`N` specifies north latitude, and `S` specifies south latitude.</span></span>



| <span data-ttu-id="d1e65-326">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-326">Property info</span></span> | <span data-ttu-id="d1e65-327">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-327">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="d1e65-328">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-328">Tag</span></span>   | <span data-ttu-id="d1e65-329">0x0013</span><span class="sxs-lookup"><span data-stu-id="d1e65-329">0x0013</span></span>                                     |
| <span data-ttu-id="d1e65-330">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-330">Type</span></span>  | <span data-ttu-id="d1e65-331">Propertytagtybäuercii</span><span class="sxs-lookup"><span data-stu-id="d1e65-331">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="d1e65-332">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-332">Count</span></span> | <span data-ttu-id="d1e65-333">2 (ein Zeichen plus das NULL-Terminator)</span><span class="sxs-lookup"><span data-stu-id="d1e65-333">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpsdestlat"></a><span data-ttu-id="d1e65-334">Propertytaggpsdestlat</span><span class="sxs-lookup"><span data-stu-id="d1e65-334">PropertyTagGpsDestLat</span></span>

<span data-ttu-id="d1e65-335">Der Breitengrad des Ziel Punkts.</span><span class="sxs-lookup"><span data-stu-id="d1e65-335">Latitude of the destination point.</span></span> <span data-ttu-id="d1e65-336">Der Breitengrad wird als drei rationale Werte ausgedrückt, die den Grad, die Minuten und die Sekunden geben.</span><span class="sxs-lookup"><span data-stu-id="d1e65-336">The latitude is expressed as three rational values giving the degrees, minutes, and seconds respectively.</span></span> <span data-ttu-id="d1e65-337">Wenn Grad, Minuten und Sekunden ausgedrückt werden, ist das Format dd/1, mm/1, SS/1.</span><span class="sxs-lookup"><span data-stu-id="d1e65-337">When degrees, minutes, and seconds are expressed, the format is dd/1, mm/1, ss/1.</span></span> <span data-ttu-id="d1e65-338">Wenn Grad und Minuten verwendet werden und z. b. ein Bruchteil von Minuten bis zu zwei Dezimalstellen erhalten, ist das Format dd/1, MMMM/100, 0/1.</span><span class="sxs-lookup"><span data-stu-id="d1e65-338">When degrees and minutes are used and, for example, fractions of minutes are given up to two decimal places, the format is dd/1, mmmm/100, 0/1.</span></span>



| <span data-ttu-id="d1e65-339">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-339">Property info</span></span> | <span data-ttu-id="d1e65-340">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-340">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="d1e65-341">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-341">Tag</span></span>   | <span data-ttu-id="d1e65-342">0x0014</span><span class="sxs-lookup"><span data-stu-id="d1e65-342">0x0014</span></span>                  |
| <span data-ttu-id="d1e65-343">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-343">Type</span></span>  | <span data-ttu-id="d1e65-344">Propertytagtyperational</span><span class="sxs-lookup"><span data-stu-id="d1e65-344">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="d1e65-345">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-345">Count</span></span> | <span data-ttu-id="d1e65-346">3</span><span class="sxs-lookup"><span data-stu-id="d1e65-346">3</span></span>                       |



 

## <a name="propertytaggpsdestlongref"></a><span data-ttu-id="d1e65-347">Propertytaggpsdestlongref</span><span class="sxs-lookup"><span data-stu-id="d1e65-347">PropertyTagGpsDestLongRef</span></span>

<span data-ttu-id="d1e65-348">Eine mit NULL endend beendete Zeichenfolge, die angibt, ob der Längengrad des Zielpunkts Ost-oder West-Längengrad ist.</span><span class="sxs-lookup"><span data-stu-id="d1e65-348">Null-terminated character string that specifies whether the longitude of the destination point is east or west longitude.</span></span> <span data-ttu-id="d1e65-349">`E` Gibt den Ost-Längengrad an und `W` gibt den West Längengrad an.</span><span class="sxs-lookup"><span data-stu-id="d1e65-349">`E` specifies east longitude, and `W` specifies west longitude.</span></span>



| <span data-ttu-id="d1e65-350">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-350">Property info</span></span> | <span data-ttu-id="d1e65-351">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-351">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="d1e65-352">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-352">Tag</span></span>   | <span data-ttu-id="d1e65-353">0x0015</span><span class="sxs-lookup"><span data-stu-id="d1e65-353">0x0015</span></span>                                     |
| <span data-ttu-id="d1e65-354">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-354">Type</span></span>  | <span data-ttu-id="d1e65-355">Propertytagtybäuercii</span><span class="sxs-lookup"><span data-stu-id="d1e65-355">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="d1e65-356">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-356">Count</span></span> | <span data-ttu-id="d1e65-357">2 (ein Zeichen plus das NULL-Terminator)</span><span class="sxs-lookup"><span data-stu-id="d1e65-357">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpsdestlong"></a><span data-ttu-id="d1e65-358">Propertytaggpsdestlong</span><span class="sxs-lookup"><span data-stu-id="d1e65-358">PropertyTagGpsDestLong</span></span>

<span data-ttu-id="d1e65-359">Längengrad des Ziel Punkts.</span><span class="sxs-lookup"><span data-stu-id="d1e65-359">Longitude of the destination point.</span></span> <span data-ttu-id="d1e65-360">Der Längengrad wird als drei rationale Werte ausgedrückt, die den Grad, die Minuten und die Sekunden geben.</span><span class="sxs-lookup"><span data-stu-id="d1e65-360">The longitude is expressed as three rational values giving the degrees, minutes, and seconds respectively.</span></span> <span data-ttu-id="d1e65-361">Wenn Grad, Minuten und Sekunden ausgedrückt werden, lautet das Format DDD/1, mm/1, SS/1.</span><span class="sxs-lookup"><span data-stu-id="d1e65-361">When degrees, minutes, and seconds are expressed, the format is ddd/1, mm/1, ss/1.</span></span> <span data-ttu-id="d1e65-362">Wenn Grad und Minuten verwendet werden und z. b. Bruchteile von Minuten bis zu zwei Dezimalstellen angegeben werden, lautet das Format DDD/1, MMMM/100, 0/1.</span><span class="sxs-lookup"><span data-stu-id="d1e65-362">When degrees and minutes are used and, for example, fractions of minutes are given up to two decimal places, the format is ddd/1, mmmm/100, 0/1.</span></span>



| <span data-ttu-id="d1e65-363">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-363">Property info</span></span> | <span data-ttu-id="d1e65-364">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-364">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="d1e65-365">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-365">Tag</span></span>   | <span data-ttu-id="d1e65-366">0x0016</span><span class="sxs-lookup"><span data-stu-id="d1e65-366">0x0016</span></span>                  |
| <span data-ttu-id="d1e65-367">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-367">Type</span></span>  | <span data-ttu-id="d1e65-368">Propertytagtyperational</span><span class="sxs-lookup"><span data-stu-id="d1e65-368">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="d1e65-369">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-369">Count</span></span> | <span data-ttu-id="d1e65-370">3</span><span class="sxs-lookup"><span data-stu-id="d1e65-370">3</span></span>                       |



 

## <a name="propertytaggpsdestbearref"></a><span data-ttu-id="d1e65-371">Propertytaggpsdestbearref</span><span class="sxs-lookup"><span data-stu-id="d1e65-371">PropertyTagGpsDestBearRef</span></span>

<span data-ttu-id="d1e65-372">Mit NULL endende Zeichenfolge, die den Verweis angibt, mit dem das-Verhalten an den Zielpunkt übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="d1e65-372">Null-terminated character string that specifies the reference used for giving the bearing to the destination point.</span></span> <span data-ttu-id="d1e65-373">`T` Gibt die tatsächliche Richtung an und `M` gibt die Magnet Richtung an.</span><span class="sxs-lookup"><span data-stu-id="d1e65-373">`T` specifies true direction, and `M` specifies magnetic direction.</span></span>



| <span data-ttu-id="d1e65-374">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-374">Property info</span></span> | <span data-ttu-id="d1e65-375">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-375">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="d1e65-376">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-376">Tag</span></span>   | <span data-ttu-id="d1e65-377">0x0017</span><span class="sxs-lookup"><span data-stu-id="d1e65-377">0x0017</span></span>                                     |
| <span data-ttu-id="d1e65-378">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-378">Type</span></span>  | <span data-ttu-id="d1e65-379">Propertytagtybäuercii</span><span class="sxs-lookup"><span data-stu-id="d1e65-379">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="d1e65-380">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-380">Count</span></span> | <span data-ttu-id="d1e65-381">2 (ein Zeichen plus das NULL-Terminator)</span><span class="sxs-lookup"><span data-stu-id="d1e65-381">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpsdestbear"></a><span data-ttu-id="d1e65-382">Propertytaggpsdestbear</span><span class="sxs-lookup"><span data-stu-id="d1e65-382">PropertyTagGpsDestBear</span></span>

<span data-ttu-id="d1e65-383">Die auf den Zielpunkt zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="d1e65-383">Bearing to the destination point.</span></span> <span data-ttu-id="d1e65-384">Der Wertebereich liegt zwischen 0,00 und 359,99.</span><span class="sxs-lookup"><span data-stu-id="d1e65-384">The range of values is from 0.00 to 359.99.</span></span>



| <span data-ttu-id="d1e65-385">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-385">Property info</span></span> | <span data-ttu-id="d1e65-386">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-386">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="d1e65-387">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-387">Tag</span></span>   | <span data-ttu-id="d1e65-388">0x0018</span><span class="sxs-lookup"><span data-stu-id="d1e65-388">0x0018</span></span>                  |
| <span data-ttu-id="d1e65-389">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-389">Type</span></span>  | <span data-ttu-id="d1e65-390">Propertytagtyperational</span><span class="sxs-lookup"><span data-stu-id="d1e65-390">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="d1e65-391">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-391">Count</span></span> | <span data-ttu-id="d1e65-392">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-392">1</span></span>                       |



 

## <a name="propertytaggpsdestdistref"></a><span data-ttu-id="d1e65-393">Propertytaggpsdestdistref</span><span class="sxs-lookup"><span data-stu-id="d1e65-393">PropertyTagGpsDestDistRef</span></span>

<span data-ttu-id="d1e65-394">Mit NULL endende Zeichenfolge, die die Einheit angibt, mit der die Entfernung zum Zielpunkt ausgedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="d1e65-394">Null-terminated character string that specifies the unit used to express the distance to the destination point.</span></span> <span data-ttu-id="d1e65-395">"K", "M" und "N" stellen jeweils die Kilometer, Meilen und Knoten dar.</span><span class="sxs-lookup"><span data-stu-id="d1e65-395">K, M, and N represent kilometers, miles, and knots respectively.</span></span>



| <span data-ttu-id="d1e65-396">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-396">Property info</span></span> | <span data-ttu-id="d1e65-397">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-397">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="d1e65-398">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-398">Tag</span></span>   | <span data-ttu-id="d1e65-399">0x0019</span><span class="sxs-lookup"><span data-stu-id="d1e65-399">0x0019</span></span>                                     |
| <span data-ttu-id="d1e65-400">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-400">Type</span></span>  | <span data-ttu-id="d1e65-401">Propertytagtybäuercii</span><span class="sxs-lookup"><span data-stu-id="d1e65-401">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="d1e65-402">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-402">Count</span></span> | <span data-ttu-id="d1e65-403">2 (ein Zeichen plus das NULL-Terminator)</span><span class="sxs-lookup"><span data-stu-id="d1e65-403">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpsdestdist"></a><span data-ttu-id="d1e65-404">Propertytaggpsdestdist</span><span class="sxs-lookup"><span data-stu-id="d1e65-404">PropertyTagGpsDestDist</span></span>

<span data-ttu-id="d1e65-405">Entfernung zum Zielpunkt.</span><span class="sxs-lookup"><span data-stu-id="d1e65-405">Distance to the destination point.</span></span>



| <span data-ttu-id="d1e65-406">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-406">Property info</span></span> | <span data-ttu-id="d1e65-407">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-407">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="d1e65-408">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-408">Tag</span></span>   | <span data-ttu-id="d1e65-409">0x001a</span><span class="sxs-lookup"><span data-stu-id="d1e65-409">0x001A</span></span>                  |
| <span data-ttu-id="d1e65-410">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-410">Type</span></span>  | <span data-ttu-id="d1e65-411">Propertytagtyperational</span><span class="sxs-lookup"><span data-stu-id="d1e65-411">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="d1e65-412">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-412">Count</span></span> | <span data-ttu-id="d1e65-413">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-413">1</span></span>                       |



 

## <a name="propertytagnewsubfiletype"></a><span data-ttu-id="d1e65-414">Propertytagnewsubfiletype</span><span class="sxs-lookup"><span data-stu-id="d1e65-414">PropertyTagNewSubfileType</span></span>

<span data-ttu-id="d1e65-415">Der Typ der Daten in einer unter Datei.</span><span class="sxs-lookup"><span data-stu-id="d1e65-415">Type of data in a subfile.</span></span>



| <span data-ttu-id="d1e65-416">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-416">Property info</span></span> | <span data-ttu-id="d1e65-417">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-417">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="d1e65-418">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-418">Tag</span></span>   | <span data-ttu-id="d1e65-419">0x00fe</span><span class="sxs-lookup"><span data-stu-id="d1e65-419">0x00FE</span></span>              |
| <span data-ttu-id="d1e65-420">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-420">Type</span></span>  | <span data-ttu-id="d1e65-421">Propertytagtypelong</span><span class="sxs-lookup"><span data-stu-id="d1e65-421">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="d1e65-422">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-422">Count</span></span> | <span data-ttu-id="d1e65-423">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-423">1</span></span>                   |



 

## <a name="propertytagsubfiletype"></a><span data-ttu-id="d1e65-424">Propertytagsubfiletype</span><span class="sxs-lookup"><span data-stu-id="d1e65-424">PropertyTagSubfileType</span></span>

<span data-ttu-id="d1e65-425">Der Typ der Daten in einer unter Datei.</span><span class="sxs-lookup"><span data-stu-id="d1e65-425">Type of data in a subfile.</span></span>



| <span data-ttu-id="d1e65-426">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-426">Property info</span></span> | <span data-ttu-id="d1e65-427">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-427">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="d1e65-428">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-428">Tag</span></span>   | <span data-ttu-id="d1e65-429">0x00FF</span><span class="sxs-lookup"><span data-stu-id="d1e65-429">0x00FF</span></span>               |
| <span data-ttu-id="d1e65-430">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-430">Type</span></span>  | <span data-ttu-id="d1e65-431">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-431">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="d1e65-432">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-432">Count</span></span> | <span data-ttu-id="d1e65-433">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-433">1</span></span>                    |



 

## <a name="propertytagimagewidth"></a><span data-ttu-id="d1e65-434">PropertyTagImageWidth</span><span class="sxs-lookup"><span data-stu-id="d1e65-434">PropertyTagImageWidth</span></span>

<span data-ttu-id="d1e65-435">Anzahl der Pixel pro Zeile.</span><span class="sxs-lookup"><span data-stu-id="d1e65-435">Number of pixels per row.</span></span>



| <span data-ttu-id="d1e65-436">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-436">Property info</span></span> | <span data-ttu-id="d1e65-437">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-437">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="d1e65-438">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-438">Tag</span></span>   | <span data-ttu-id="d1e65-439">0x0100</span><span class="sxs-lookup"><span data-stu-id="d1e65-439">0x0100</span></span>                                      |
| <span data-ttu-id="d1e65-440">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-440">Type</span></span>  | <span data-ttu-id="d1e65-441">Propertytagtypeshort oder propertytagtypelong</span><span class="sxs-lookup"><span data-stu-id="d1e65-441">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="d1e65-442">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-442">Count</span></span> | <span data-ttu-id="d1e65-443">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-443">1</span></span>                                           |



 

## <a name="propertytagimageheight"></a><span data-ttu-id="d1e65-444">Propertytagimageheight</span><span class="sxs-lookup"><span data-stu-id="d1e65-444">PropertyTagImageHeight</span></span>

<span data-ttu-id="d1e65-445">Anzahl der Pixel Zeilen.</span><span class="sxs-lookup"><span data-stu-id="d1e65-445">Number of pixel rows.</span></span>



| <span data-ttu-id="d1e65-446">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-446">Property info</span></span> | <span data-ttu-id="d1e65-447">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-447">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="d1e65-448">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-448">Tag</span></span>   | <span data-ttu-id="d1e65-449">0x0101</span><span class="sxs-lookup"><span data-stu-id="d1e65-449">0x0101</span></span>                                      |
| <span data-ttu-id="d1e65-450">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-450">Type</span></span>  | <span data-ttu-id="d1e65-451">Propertytagtypeshort oder propertytagtypelong</span><span class="sxs-lookup"><span data-stu-id="d1e65-451">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="d1e65-452">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-452">Count</span></span> | <span data-ttu-id="d1e65-453">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-453">1</span></span>                                           |



 

## <a name="propertytagbitspersample"></a><span data-ttu-id="d1e65-454">Propertytagbitspersample</span><span class="sxs-lookup"><span data-stu-id="d1e65-454">PropertyTagBitsPerSample</span></span>

<span data-ttu-id="d1e65-455">Anzahl der Bits pro Farbkomponente.</span><span class="sxs-lookup"><span data-stu-id="d1e65-455">Number of bits per color component.</span></span> <span data-ttu-id="d1e65-456">Siehe auch [propertytagsamplesperpixel](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="d1e65-456">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="d1e65-457">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-457">Property info</span></span> | <span data-ttu-id="d1e65-458">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-458">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="d1e65-459">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-459">Tag</span></span>   | <span data-ttu-id="d1e65-460">0x0102</span><span class="sxs-lookup"><span data-stu-id="d1e65-460">0x0102</span></span>                                   |
| <span data-ttu-id="d1e65-461">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-461">Type</span></span>  | <span data-ttu-id="d1e65-462">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-462">PropertyTagTypeShort</span></span>                     |
| <span data-ttu-id="d1e65-463">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-463">Count</span></span> | <span data-ttu-id="d1e65-464">Anzahl von Stichproben (Komponenten) pro Pixel</span><span class="sxs-lookup"><span data-stu-id="d1e65-464">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagcompression"></a><span data-ttu-id="d1e65-465">Propertytagcompression</span><span class="sxs-lookup"><span data-stu-id="d1e65-465">PropertyTagCompression</span></span>

<span data-ttu-id="d1e65-466">Das für die Bilddaten verwendete Komprimierungs Schema.</span><span class="sxs-lookup"><span data-stu-id="d1e65-466">Compression scheme used for the image data.</span></span>



| <span data-ttu-id="d1e65-467">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-467">Property info</span></span> | <span data-ttu-id="d1e65-468">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-468">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="d1e65-469">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-469">Tag</span></span>   | <span data-ttu-id="d1e65-470">0x0103</span><span class="sxs-lookup"><span data-stu-id="d1e65-470">0x0103</span></span>               |
| <span data-ttu-id="d1e65-471">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-471">Type</span></span>  | <span data-ttu-id="d1e65-472">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-472">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="d1e65-473">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-473">Count</span></span> | <span data-ttu-id="d1e65-474">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-474">1</span></span>                    |



 

## <a name="propertytagphotometricinterp"></a><span data-ttu-id="d1e65-475">Propertytagphotomepackcinterp</span><span class="sxs-lookup"><span data-stu-id="d1e65-475">PropertyTagPhotometricInterp</span></span>

<span data-ttu-id="d1e65-476">Wie Pixeldaten interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="d1e65-476">How pixel data will be interpreted.</span></span>



| <span data-ttu-id="d1e65-477">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-477">Property info</span></span> | <span data-ttu-id="d1e65-478">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-478">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="d1e65-479">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-479">Tag</span></span>   | <span data-ttu-id="d1e65-480">0x0106</span><span class="sxs-lookup"><span data-stu-id="d1e65-480">0x0106</span></span>               |
| <span data-ttu-id="d1e65-481">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-481">Type</span></span>  | <span data-ttu-id="d1e65-482">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-482">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="d1e65-483">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-483">Count</span></span> | <span data-ttu-id="d1e65-484">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-484">1</span></span>                    |



 

## <a name="propertytagthreshholding"></a><span data-ttu-id="d1e65-485">Propertytagschwelle</span><span class="sxs-lookup"><span data-stu-id="d1e65-485">PropertyTagThreshHolding</span></span>

<span data-ttu-id="d1e65-486">Technik, die verwendet wird, um von grauen Pixeln in schwarze und weiße Pixel zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="d1e65-486">Technique used to convert from gray pixels to black and white pixels.</span></span>



| <span data-ttu-id="d1e65-487">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-487">Property info</span></span> | <span data-ttu-id="d1e65-488">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-488">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="d1e65-489">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-489">Tag</span></span>   | <span data-ttu-id="d1e65-490">0x0107</span><span class="sxs-lookup"><span data-stu-id="d1e65-490">0x0107</span></span>               |
| <span data-ttu-id="d1e65-491">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-491">Type</span></span>  | <span data-ttu-id="d1e65-492">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-492">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="d1e65-493">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-493">Count</span></span> | <span data-ttu-id="d1e65-494">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-494">1</span></span>                    |



 

## <a name="propertytagcellwidth"></a><span data-ttu-id="d1e65-495">Propertytagcellwidth</span><span class="sxs-lookup"><span data-stu-id="d1e65-495">PropertyTagCellWidth</span></span>

<span data-ttu-id="d1e65-496">Breite der Dithering-oder Halftoning-Matrix.</span><span class="sxs-lookup"><span data-stu-id="d1e65-496">Width of the dithering or halftoning matrix.</span></span>



| <span data-ttu-id="d1e65-497">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-497">Property info</span></span> | <span data-ttu-id="d1e65-498">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-498">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="d1e65-499">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-499">Tag</span></span>   | <span data-ttu-id="d1e65-500">0x0108</span><span class="sxs-lookup"><span data-stu-id="d1e65-500">0x0108</span></span>               |
| <span data-ttu-id="d1e65-501">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-501">Type</span></span>  | <span data-ttu-id="d1e65-502">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-502">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="d1e65-503">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-503">Count</span></span> | <span data-ttu-id="d1e65-504">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-504">1</span></span>                    |



 

## <a name="propertytagcellheight"></a><span data-ttu-id="d1e65-505">Propertytagcellheight</span><span class="sxs-lookup"><span data-stu-id="d1e65-505">PropertyTagCellHeight</span></span>

<span data-ttu-id="d1e65-506">Höhe der Dithering-oder Halftoning-Matrix.</span><span class="sxs-lookup"><span data-stu-id="d1e65-506">Height of the dithering or halftoning matrix.</span></span>



| <span data-ttu-id="d1e65-507">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-507">Property info</span></span> | <span data-ttu-id="d1e65-508">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-508">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="d1e65-509">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-509">Tag</span></span>   | <span data-ttu-id="d1e65-510">0x0109</span><span class="sxs-lookup"><span data-stu-id="d1e65-510">0x0109</span></span>               |
| <span data-ttu-id="d1e65-511">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-511">Type</span></span>  | <span data-ttu-id="d1e65-512">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-512">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="d1e65-513">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-513">Count</span></span> | <span data-ttu-id="d1e65-514">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-514">1</span></span>                    |



 

## <a name="propertytagfillorder"></a><span data-ttu-id="d1e65-515">Propertytagfillorder</span><span class="sxs-lookup"><span data-stu-id="d1e65-515">PropertyTagFillOrder</span></span>

<span data-ttu-id="d1e65-516">Logische Reihenfolge von Bits in einem Byte.</span><span class="sxs-lookup"><span data-stu-id="d1e65-516">Logical order of bits in a byte.</span></span>



| <span data-ttu-id="d1e65-517">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-517">Property info</span></span> | <span data-ttu-id="d1e65-518">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-518">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="d1e65-519">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-519">Tag</span></span>   | <span data-ttu-id="d1e65-520">0x010a</span><span class="sxs-lookup"><span data-stu-id="d1e65-520">0x010A</span></span>               |
| <span data-ttu-id="d1e65-521">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-521">Type</span></span>  | <span data-ttu-id="d1e65-522">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-522">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="d1e65-523">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-523">Count</span></span> | <span data-ttu-id="d1e65-524">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-524">1</span></span>                    |



 

## <a name="propertytagdocumentname"></a><span data-ttu-id="d1e65-525">Propertytagdocumentname</span><span class="sxs-lookup"><span data-stu-id="d1e65-525">PropertyTagDocumentName</span></span>

<span data-ttu-id="d1e65-526">Mit NULL beendete Zeichenfolge, die den Namen des Dokuments angibt, aus dem das Bild gescannt wurde.</span><span class="sxs-lookup"><span data-stu-id="d1e65-526">Null-terminated character string that specifies the name of the document from which the image was scanned.</span></span>



| <span data-ttu-id="d1e65-527">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-527">Property info</span></span> | <span data-ttu-id="d1e65-528">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-528">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="d1e65-529">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-529">Tag</span></span>   | <span data-ttu-id="d1e65-530">0x010d</span><span class="sxs-lookup"><span data-stu-id="d1e65-530">0x010D</span></span>                                             |
| <span data-ttu-id="d1e65-531">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-531">Type</span></span>  | <span data-ttu-id="d1e65-532">Propertytagtybäuercii</span><span class="sxs-lookup"><span data-stu-id="d1e65-532">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="d1e65-533">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-533">Count</span></span> | <span data-ttu-id="d1e65-534">Länge der Zeichenfolge einschließlich des NULL-Terminator</span><span class="sxs-lookup"><span data-stu-id="d1e65-534">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagimagedescription"></a><span data-ttu-id="d1e65-535">Propertytagimagedescription</span><span class="sxs-lookup"><span data-stu-id="d1e65-535">PropertyTagImageDescription</span></span>

<span data-ttu-id="d1e65-536">Mit NULL beendete Zeichenfolge, die den Titel des Bilds angibt.</span><span class="sxs-lookup"><span data-stu-id="d1e65-536">Null-terminated character string that specifies the title of the image.</span></span>



| <span data-ttu-id="d1e65-537">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-537">Property info</span></span> | <span data-ttu-id="d1e65-538">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-538">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="d1e65-539">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-539">Tag</span></span>   | <span data-ttu-id="d1e65-540">0x010e</span><span class="sxs-lookup"><span data-stu-id="d1e65-540">0x010E</span></span>                                             |
| <span data-ttu-id="d1e65-541">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-541">Type</span></span>  | <span data-ttu-id="d1e65-542">Propertytagtybäuercii</span><span class="sxs-lookup"><span data-stu-id="d1e65-542">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="d1e65-543">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-543">Count</span></span> | <span data-ttu-id="d1e65-544">Länge der Zeichenfolge einschließlich des NULL-Terminator</span><span class="sxs-lookup"><span data-stu-id="d1e65-544">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagequipmake"></a><span data-ttu-id="d1e65-545">Propertytagequipmake</span><span class="sxs-lookup"><span data-stu-id="d1e65-545">PropertyTagEquipMake</span></span>

<span data-ttu-id="d1e65-546">Mit NULL endende Zeichenfolge, die den Hersteller der Ausrüstung angibt, die zum Aufzeichnen des Bilds verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d1e65-546">Null-terminated character string that specifies the manufacturer of the equipment used to record the image.</span></span>



| <span data-ttu-id="d1e65-547">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-547">Property info</span></span> | <span data-ttu-id="d1e65-548">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-548">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="d1e65-549">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-549">Tag</span></span>   | <span data-ttu-id="d1e65-550">0x010F</span><span class="sxs-lookup"><span data-stu-id="d1e65-550">0x010F</span></span>                                             |
| <span data-ttu-id="d1e65-551">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-551">Type</span></span>  | <span data-ttu-id="d1e65-552">Propertytagtybäuercii</span><span class="sxs-lookup"><span data-stu-id="d1e65-552">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="d1e65-553">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-553">Count</span></span> | <span data-ttu-id="d1e65-554">Länge der Zeichenfolge einschließlich des NULL-Terminator</span><span class="sxs-lookup"><span data-stu-id="d1e65-554">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagequipmodel"></a><span data-ttu-id="d1e65-555">Propertytagequipmodel</span><span class="sxs-lookup"><span data-stu-id="d1e65-555">PropertyTagEquipModel</span></span>

<span data-ttu-id="d1e65-556">Mit NULL endende Zeichenfolge, die den Modellnamen oder die Modellnummer der Ausrüstung angibt, die zum Aufzeichnen des Bilds verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d1e65-556">Null-terminated character string that specifies the model name or model number of the equipment used to record the image.</span></span>



| <span data-ttu-id="d1e65-557">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-557">Property info</span></span> | <span data-ttu-id="d1e65-558">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-558">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="d1e65-559">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-559">Tag</span></span>   | <span data-ttu-id="d1e65-560">0x0110</span><span class="sxs-lookup"><span data-stu-id="d1e65-560">0x0110</span></span>                                             |
| <span data-ttu-id="d1e65-561">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-561">Type</span></span>  | <span data-ttu-id="d1e65-562">Propertytagtybäuercii</span><span class="sxs-lookup"><span data-stu-id="d1e65-562">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="d1e65-563">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-563">Count</span></span> | <span data-ttu-id="d1e65-564">Länge der Zeichenfolge einschließlich des NULL-Terminator</span><span class="sxs-lookup"><span data-stu-id="d1e65-564">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagstripoffsets"></a><span data-ttu-id="d1e65-565">Propertytagstripoffsets</span><span class="sxs-lookup"><span data-stu-id="d1e65-565">PropertyTagStripOffsets</span></span>

<span data-ttu-id="d1e65-566">Für jeden Strip den Byte Offset dieses Streifens.</span><span class="sxs-lookup"><span data-stu-id="d1e65-566">For each strip, the byte offset of that strip.</span></span> <span data-ttu-id="d1e65-567">Siehe auch [propertytagrowsperstrip](#propertytagrowsperstrip) und [propertytagstripbytescount](#propertytagstripbytescount).</span><span class="sxs-lookup"><span data-stu-id="d1e65-567">See also [PropertyTagRowsPerStrip](#propertytagrowsperstrip) and [PropertyTagStripBytesCount](#propertytagstripbytescount).</span></span>



| <span data-ttu-id="d1e65-568">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-568">Property info</span></span> | <span data-ttu-id="d1e65-569">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-569">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="d1e65-570">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-570">Tag</span></span>   | <span data-ttu-id="d1e65-571">0x0111</span><span class="sxs-lookup"><span data-stu-id="d1e65-571">0x0111</span></span>                                      |
| <span data-ttu-id="d1e65-572">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-572">Type</span></span>  | <span data-ttu-id="d1e65-573">Propertytagtypeshort oder propertytagtypelong</span><span class="sxs-lookup"><span data-stu-id="d1e65-573">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="d1e65-574">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-574">Count</span></span> | <span data-ttu-id="d1e65-575">Anzahl von Bändern</span><span class="sxs-lookup"><span data-stu-id="d1e65-575">Number of strips</span></span>                            |



 

## <a name="propertytagorientation"></a><span data-ttu-id="d1e65-576">Propertytagorientation</span><span class="sxs-lookup"><span data-stu-id="d1e65-576">PropertyTagOrientation</span></span>

<span data-ttu-id="d1e65-577">Bild Ausrichtung wird in Form von Zeilen und Spalten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d1e65-577">Image orientation viewed in terms of rows and columns.</span></span>



<span data-ttu-id="d1e65-578">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-578">Tag</span></span>

<span data-ttu-id="d1e65-579">0x0112</span><span class="sxs-lookup"><span data-stu-id="d1e65-579">0x0112</span></span>

<span data-ttu-id="d1e65-580">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-580">Type</span></span>

<span data-ttu-id="d1e65-581">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-581">PropertyTagTypeShort</span></span>

<span data-ttu-id="d1e65-582">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-582">Count</span></span>

<span data-ttu-id="d1e65-583">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-583">1</span></span>

<span data-ttu-id="d1e65-584">1: die Zeile nullten befindet sich am oberen Rand des visuellen Bilds, und die Spalte nullten ist das visuelle Element auf der linken Seite.</span><span class="sxs-lookup"><span data-stu-id="d1e65-584">1 - The 0th row is at the top of the visual image, and the 0th column is the visual left side.</span></span> <span data-ttu-id="d1e65-585">2: die Zeile nullten befindet sich am visuellen oberen Rand des Bilds, und die Spalte nullten ist die visuelle Rechte Seite.</span><span class="sxs-lookup"><span data-stu-id="d1e65-585">2 - The 0th row is at the visual top of the image, and the 0th column is the visual right side.</span></span> <span data-ttu-id="d1e65-586">3: die Zeile nullten befindet sich am visuellen Rand des Bilds, und die nullten-Spalte ist die visuelle Rechte Seite.</span><span class="sxs-lookup"><span data-stu-id="d1e65-586">3 - The 0th row is at the visual bottom of the image, and the 0th column is the visual right side.</span></span> <span data-ttu-id="d1e65-587">4-die Zeile nullten befindet sich am visuellen Rand des Bilds, und die nullten-Spalte ist die visuelle Darstellung Links.</span><span class="sxs-lookup"><span data-stu-id="d1e65-587">4 - The 0th row is at the visual bottom of the image, and the 0th column is the visual left side.</span></span> <span data-ttu-id="d1e65-588">5-die Zeile nullten ist das visuelle Element auf der linken Seite des Bilds, und die Spalte nullten ist der visuelle obere Rand.</span><span class="sxs-lookup"><span data-stu-id="d1e65-588">5 - The 0th row is the visual left side of the image, and the 0th column is the visual top.</span></span> <span data-ttu-id="d1e65-589">6-die Zeile nullten ist die visuelle Rechte Seite des Bilds, und die nullten-Spalte ist der visuelle obere Rand.</span><span class="sxs-lookup"><span data-stu-id="d1e65-589">6 - The 0th row is the visual right side of the image, and the 0th column is the visual top.</span></span> <span data-ttu-id="d1e65-590">7-die Zeile nullten ist die visuelle Rechte Seite des Bilds, und die Spalte nullten ist das visuelle Element unten.</span><span class="sxs-lookup"><span data-stu-id="d1e65-590">7 - The 0th row is the visual right side of the image, and the 0th column is the visual bottom.</span></span> <span data-ttu-id="d1e65-591">8: die Zeile nullten ist das visuelle Element auf der linken Seite des Bilds, und die Spalte nullten ist das visuelle Element unten.</span><span class="sxs-lookup"><span data-stu-id="d1e65-591">8 - The 0th row is the visual left side of the image, and the 0th column is the visual bottom.</span></span>



 

## <a name="propertytagsamplesperpixel"></a><span data-ttu-id="d1e65-592">Propertytagsamplesperpixel</span><span class="sxs-lookup"><span data-stu-id="d1e65-592">PropertyTagSamplesPerPixel</span></span>

<span data-ttu-id="d1e65-593">Anzahl der Farbkomponenten pro Pixel.</span><span class="sxs-lookup"><span data-stu-id="d1e65-593">Number of color components per pixel.</span></span>



| <span data-ttu-id="d1e65-594">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-594">Property info</span></span> | <span data-ttu-id="d1e65-595">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-595">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="d1e65-596">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-596">Tag</span></span>   | <span data-ttu-id="d1e65-597">0x0115</span><span class="sxs-lookup"><span data-stu-id="d1e65-597">0x0115</span></span>               |
| <span data-ttu-id="d1e65-598">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-598">Type</span></span>  | <span data-ttu-id="d1e65-599">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-599">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="d1e65-600">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-600">Count</span></span> | <span data-ttu-id="d1e65-601">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-601">1</span></span>                    |



 

## <a name="propertytagrowsperstrip"></a><span data-ttu-id="d1e65-602">Propertytagrowsperstrip</span><span class="sxs-lookup"><span data-stu-id="d1e65-602">PropertyTagRowsPerStrip</span></span>

<span data-ttu-id="d1e65-603">Anzahl der Zeilen pro Strip.</span><span class="sxs-lookup"><span data-stu-id="d1e65-603">Number of rows per strip.</span></span> <span data-ttu-id="d1e65-604">Siehe auch [propertytagstripbytescount](#propertytagstripbytescount) und [propertytagstripoffsets](#propertytagstripoffsets).</span><span class="sxs-lookup"><span data-stu-id="d1e65-604">See also [PropertyTagStripBytesCount](#propertytagstripbytescount) and [PropertyTagStripOffsets](#propertytagstripoffsets).</span></span>



| <span data-ttu-id="d1e65-605">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-605">Property info</span></span> | <span data-ttu-id="d1e65-606">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-606">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="d1e65-607">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-607">Tag</span></span>   | <span data-ttu-id="d1e65-608">0x0116</span><span class="sxs-lookup"><span data-stu-id="d1e65-608">0x0116</span></span>                                      |
| <span data-ttu-id="d1e65-609">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-609">Type</span></span>  | <span data-ttu-id="d1e65-610">Propertytagtypeshort oder propertytagtypelong</span><span class="sxs-lookup"><span data-stu-id="d1e65-610">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="d1e65-611">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-611">Count</span></span> | <span data-ttu-id="d1e65-612">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-612">1</span></span>                                           |



 

## <a name="propertytagstripbytescount"></a><span data-ttu-id="d1e65-613">Propertytagstripbytescount</span><span class="sxs-lookup"><span data-stu-id="d1e65-613">PropertyTagStripBytesCount</span></span>

<span data-ttu-id="d1e65-614">Für jeden Strip die Gesamtzahl der Bytes in diesem Strip.</span><span class="sxs-lookup"><span data-stu-id="d1e65-614">For each strip, the total number of bytes in that strip.</span></span>



| <span data-ttu-id="d1e65-615">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-615">Property info</span></span> | <span data-ttu-id="d1e65-616">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-616">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="d1e65-617">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-617">Tag</span></span>   | <span data-ttu-id="d1e65-618">0x0117</span><span class="sxs-lookup"><span data-stu-id="d1e65-618">0x0117</span></span>                                      |
| <span data-ttu-id="d1e65-619">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-619">Type</span></span>  | <span data-ttu-id="d1e65-620">Propertytagtypeshort oder propertytagtypelong</span><span class="sxs-lookup"><span data-stu-id="d1e65-620">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="d1e65-621">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-621">Count</span></span> | <span data-ttu-id="d1e65-622">Anzahl von Bändern</span><span class="sxs-lookup"><span data-stu-id="d1e65-622">Number of strips</span></span>                            |



 

## <a name="propertytagminsamplevalue"></a><span data-ttu-id="d1e65-623">Propertytagminsamplevalue</span><span class="sxs-lookup"><span data-stu-id="d1e65-623">PropertyTagMinSampleValue</span></span>

<span data-ttu-id="d1e65-624">Für jede Farbkomponente der minimale Wert, der dieser Komponente zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="d1e65-624">For each color component, the minimum value assigned to that component.</span></span> <span data-ttu-id="d1e65-625">Siehe auch [propertytagsamplesperpixel](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="d1e65-625">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="d1e65-626">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-626">Property info</span></span> | <span data-ttu-id="d1e65-627">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-627">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="d1e65-628">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-628">Tag</span></span>   | <span data-ttu-id="d1e65-629">0x0118</span><span class="sxs-lookup"><span data-stu-id="d1e65-629">0x0118</span></span>                                   |
| <span data-ttu-id="d1e65-630">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-630">Type</span></span>  | <span data-ttu-id="d1e65-631">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-631">PropertyTagTypeShort</span></span>                     |
| <span data-ttu-id="d1e65-632">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-632">Count</span></span> | <span data-ttu-id="d1e65-633">Anzahl von Stichproben (Komponenten) pro Pixel</span><span class="sxs-lookup"><span data-stu-id="d1e65-633">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagmaxsamplevalue"></a><span data-ttu-id="d1e65-634">Propertytagmaxsamplevalue</span><span class="sxs-lookup"><span data-stu-id="d1e65-634">PropertyTagMaxSampleValue</span></span>

<span data-ttu-id="d1e65-635">Für jede Farbkomponente der Maximalwert, der dieser Komponente zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="d1e65-635">For each color component, the maximum value assigned to that component.</span></span> <span data-ttu-id="d1e65-636">Siehe auch [propertytagsamplesperpixel](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="d1e65-636">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="d1e65-637">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-637">Property info</span></span> | <span data-ttu-id="d1e65-638">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-638">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="d1e65-639">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-639">Tag</span></span>   | <span data-ttu-id="d1e65-640">0x0119</span><span class="sxs-lookup"><span data-stu-id="d1e65-640">0x0119</span></span>                                   |
| <span data-ttu-id="d1e65-641">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-641">Type</span></span>  | <span data-ttu-id="d1e65-642">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-642">PropertyTagTypeShort</span></span>                     |
| <span data-ttu-id="d1e65-643">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-643">Count</span></span> | <span data-ttu-id="d1e65-644">Anzahl von Stichproben (Komponenten) pro Pixel</span><span class="sxs-lookup"><span data-stu-id="d1e65-644">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagxresolution"></a><span data-ttu-id="d1e65-645">Propertytagxresolution</span><span class="sxs-lookup"><span data-stu-id="d1e65-645">PropertyTagXResolution</span></span>

<span data-ttu-id="d1e65-646">Die Anzahl der Pixel pro Einheit in der Bild breiten Richtung (x).</span><span class="sxs-lookup"><span data-stu-id="d1e65-646">Number of pixels per unit in the image width (x) direction.</span></span> <span data-ttu-id="d1e65-647">Die Einheit wird durch [propertytagresolutionunit](#propertytagresolutionunit)angegeben.</span><span class="sxs-lookup"><span data-stu-id="d1e65-647">The unit is specified by [PropertyTagResolutionUnit](#propertytagresolutionunit).</span></span>



| <span data-ttu-id="d1e65-648">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-648">Property info</span></span> | <span data-ttu-id="d1e65-649">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-649">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="d1e65-650">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-650">Tag</span></span>   | <span data-ttu-id="d1e65-651">0x011a</span><span class="sxs-lookup"><span data-stu-id="d1e65-651">0x011A</span></span>                  |
| <span data-ttu-id="d1e65-652">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-652">Type</span></span>  | <span data-ttu-id="d1e65-653">Propertytagtyperational</span><span class="sxs-lookup"><span data-stu-id="d1e65-653">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="d1e65-654">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-654">Count</span></span> | <span data-ttu-id="d1e65-655">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-655">1</span></span>                       |



 

## <a name="propertytagyresolution"></a><span data-ttu-id="d1e65-656">Propertytagyresolution</span><span class="sxs-lookup"><span data-stu-id="d1e65-656">PropertyTagYResolution</span></span>

<span data-ttu-id="d1e65-657">Anzahl der Pixel pro Einheit in der Bildhöhe (y).</span><span class="sxs-lookup"><span data-stu-id="d1e65-657">Number of pixels per unit in the image height (y) direction.</span></span> <span data-ttu-id="d1e65-658">Die Einheit wird durch [propertytagresolutionunit](#propertytagresolutionunit)angegeben.</span><span class="sxs-lookup"><span data-stu-id="d1e65-658">The unit is specified by [PropertyTagResolutionUnit](#propertytagresolutionunit).</span></span>



| <span data-ttu-id="d1e65-659">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-659">Property info</span></span> | <span data-ttu-id="d1e65-660">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-660">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="d1e65-661">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-661">Tag</span></span>   | <span data-ttu-id="d1e65-662">0x011b</span><span class="sxs-lookup"><span data-stu-id="d1e65-662">0x011B</span></span>                  |
| <span data-ttu-id="d1e65-663">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-663">Type</span></span>  | <span data-ttu-id="d1e65-664">Propertytagtyperational</span><span class="sxs-lookup"><span data-stu-id="d1e65-664">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="d1e65-665">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-665">Count</span></span> | <span data-ttu-id="d1e65-666">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-666">1</span></span>                       |



 

## <a name="propertytagplanarconfig"></a><span data-ttu-id="d1e65-667">Propertytagplanarconfig</span><span class="sxs-lookup"><span data-stu-id="d1e65-667">PropertyTagPlanarConfig</span></span>

<span data-ttu-id="d1e65-668">Gibt an, ob Pixel Komponenten im segmentierten oder planaren Format aufgezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="d1e65-668">Whether pixel components are recorded in chunky or planar format.</span></span>



| <span data-ttu-id="d1e65-669">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-669">Property info</span></span> | <span data-ttu-id="d1e65-670">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-670">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="d1e65-671">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-671">Tag</span></span>   | <span data-ttu-id="d1e65-672">0x011c</span><span class="sxs-lookup"><span data-stu-id="d1e65-672">0x011C</span></span>               |
| <span data-ttu-id="d1e65-673">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-673">Type</span></span>  | <span data-ttu-id="d1e65-674">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-674">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="d1e65-675">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-675">Count</span></span> | <span data-ttu-id="d1e65-676">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-676">1</span></span>                    |



 

## <a name="propertytagpagename"></a><span data-ttu-id="d1e65-677">Propertytagpagename</span><span class="sxs-lookup"><span data-stu-id="d1e65-677">PropertyTagPageName</span></span>

<span data-ttu-id="d1e65-678">Mit NULL beendete Zeichenfolge, die den Namen der Seite angibt, von der das Bild gescannt wurde.</span><span class="sxs-lookup"><span data-stu-id="d1e65-678">Null-terminated character string that specifies the name of the page from which the image was scanned.</span></span>



| <span data-ttu-id="d1e65-679">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-679">Property info</span></span> | <span data-ttu-id="d1e65-680">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-680">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="d1e65-681">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-681">Tag</span></span>   | <span data-ttu-id="d1e65-682">0x011d</span><span class="sxs-lookup"><span data-stu-id="d1e65-682">0x011D</span></span>                                             |
| <span data-ttu-id="d1e65-683">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-683">Type</span></span>  | <span data-ttu-id="d1e65-684">Propertytagtybäuercii</span><span class="sxs-lookup"><span data-stu-id="d1e65-684">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="d1e65-685">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-685">Count</span></span> | <span data-ttu-id="d1e65-686">Länge der Zeichenfolge einschließlich des NULL-Terminator</span><span class="sxs-lookup"><span data-stu-id="d1e65-686">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagxposition"></a><span data-ttu-id="d1e65-687">Propertytagxposition</span><span class="sxs-lookup"><span data-stu-id="d1e65-687">PropertyTagXPosition</span></span>

<span data-ttu-id="d1e65-688">Offset von der linken Seite der Seite auf die linke Seite des Bilds.</span><span class="sxs-lookup"><span data-stu-id="d1e65-688">Offset from the left side of the page to the left side of the image.</span></span> <span data-ttu-id="d1e65-689">Die Maßeinheit wird durch [propertytagresolutionunit](#propertytagresolutionunit)angegeben.</span><span class="sxs-lookup"><span data-stu-id="d1e65-689">The unit of measure is specified by [PropertyTagResolutionUnit](#propertytagresolutionunit).</span></span>



| <span data-ttu-id="d1e65-690">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-690">Property info</span></span> | <span data-ttu-id="d1e65-691">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-691">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="d1e65-692">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-692">Tag</span></span>   | <span data-ttu-id="d1e65-693">0x011e</span><span class="sxs-lookup"><span data-stu-id="d1e65-693">0x011E</span></span>                  |
| <span data-ttu-id="d1e65-694">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-694">Type</span></span>  | <span data-ttu-id="d1e65-695">Propertytagtyperational</span><span class="sxs-lookup"><span data-stu-id="d1e65-695">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="d1e65-696">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-696">Count</span></span> | <span data-ttu-id="d1e65-697">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-697">1</span></span>                       |



 

## <a name="propertytagyposition"></a><span data-ttu-id="d1e65-698">Propertytagyposition</span><span class="sxs-lookup"><span data-stu-id="d1e65-698">PropertyTagYPosition</span></span>

<span data-ttu-id="d1e65-699">Offset vom oberen Rand der Seite bis zum oberen Rand des Bilds.</span><span class="sxs-lookup"><span data-stu-id="d1e65-699">Offset from the top of the page to the top of the image.</span></span> <span data-ttu-id="d1e65-700">Die Maßeinheit wird durch [propertytagresolutionunit](#propertytagresolutionunit)angegeben.</span><span class="sxs-lookup"><span data-stu-id="d1e65-700">The unit of measure is specified by [PropertyTagResolutionUnit](#propertytagresolutionunit).</span></span>



| <span data-ttu-id="d1e65-701">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-701">Property info</span></span> | <span data-ttu-id="d1e65-702">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-702">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="d1e65-703">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-703">Tag</span></span>   | <span data-ttu-id="d1e65-704">0x011f</span><span class="sxs-lookup"><span data-stu-id="d1e65-704">0x011F</span></span>                  |
| <span data-ttu-id="d1e65-705">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-705">Type</span></span>  | <span data-ttu-id="d1e65-706">Propertytagtyperational</span><span class="sxs-lookup"><span data-stu-id="d1e65-706">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="d1e65-707">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-707">Count</span></span> | <span data-ttu-id="d1e65-708">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-708">1</span></span>                       |



 

## <a name="propertytagfreeoffset"></a><span data-ttu-id="d1e65-709">Propertytagfreoffset</span><span class="sxs-lookup"><span data-stu-id="d1e65-709">PropertyTagFreeOffset</span></span>

<span data-ttu-id="d1e65-710">Für jede Zeichenfolge von zusammenhängenden nicht verwendeten Bytes der Byte Offset dieser Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="d1e65-710">For each string of contiguous unused bytes, the byte offset of that string.</span></span>



| <span data-ttu-id="d1e65-711">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-711">Property info</span></span> | <span data-ttu-id="d1e65-712">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-712">Value</span></span> |
|------|---------------------|
| <span data-ttu-id="d1e65-713">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-713">Tag</span></span>  | <span data-ttu-id="d1e65-714">0x0120</span><span class="sxs-lookup"><span data-stu-id="d1e65-714">0x0120</span></span>              |
| <span data-ttu-id="d1e65-715">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-715">Type</span></span> | <span data-ttu-id="d1e65-716">Propertytagtypelong</span><span class="sxs-lookup"><span data-stu-id="d1e65-716">PropertyTagTypeLong</span></span> |



 

## <a name="propertytagfreebytecounts"></a><span data-ttu-id="d1e65-717">Propertytagfrebytecounts</span><span class="sxs-lookup"><span data-stu-id="d1e65-717">PropertyTagFreeByteCounts</span></span>

<span data-ttu-id="d1e65-718">Die Anzahl von Bytes in dieser Zeichenfolge für jede Zeichenfolge von zusammenhängenden nicht verwendeten Bytes.</span><span class="sxs-lookup"><span data-stu-id="d1e65-718">For each string of contiguous unused bytes, the number of bytes in that string.</span></span>



| <span data-ttu-id="d1e65-719">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-719">Property info</span></span> | <span data-ttu-id="d1e65-720">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-720">Value</span></span> |
|-------|-----------------------------------------------|
| <span data-ttu-id="d1e65-721">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-721">Tag</span></span>   | <span data-ttu-id="d1e65-722">0x0121</span><span class="sxs-lookup"><span data-stu-id="d1e65-722">0x0121</span></span>                                        |
| <span data-ttu-id="d1e65-723">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-723">Type</span></span>  | <span data-ttu-id="d1e65-724">Propertytagtypelong</span><span class="sxs-lookup"><span data-stu-id="d1e65-724">PropertyTagTypeLong</span></span>                           |
| <span data-ttu-id="d1e65-725">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-725">Count</span></span> | <span data-ttu-id="d1e65-726">Anzahl von Zeichen folgen aus zusammenhängenden nicht verwendeten Bytes.</span><span class="sxs-lookup"><span data-stu-id="d1e65-726">Number of strings of contiguous unused bytes.</span></span> |



 

## <a name="propertytaggrayresponseunit"></a><span data-ttu-id="d1e65-727">Propertytaggrayresponseunit</span><span class="sxs-lookup"><span data-stu-id="d1e65-727">PropertyTagGrayResponseUnit</span></span>

<span data-ttu-id="d1e65-728">Genauigkeit der Zahl, die durch propertytaggrayresponsecurve angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d1e65-728">Precision of the number specified by PropertyTagGrayResponseCurve.</span></span> <span data-ttu-id="d1e65-729">1 gibt Zehntel an, 2 gibt Hundertstel an, 3 gibt Tausendstel usw. an.</span><span class="sxs-lookup"><span data-stu-id="d1e65-729">1 specifies tenths, 2 specifies hundredths, 3 specifies thousandths, and so on.</span></span>



| <span data-ttu-id="d1e65-730">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-730">Property info</span></span> | <span data-ttu-id="d1e65-731">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-731">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="d1e65-732">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-732">Tag</span></span>   | <span data-ttu-id="d1e65-733">0x0122</span><span class="sxs-lookup"><span data-stu-id="d1e65-733">0x0122</span></span>               |
| <span data-ttu-id="d1e65-734">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-734">Type</span></span>  | <span data-ttu-id="d1e65-735">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-735">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="d1e65-736">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-736">Count</span></span> | <span data-ttu-id="d1e65-737">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-737">1</span></span>                    |



 

## <a name="propertytaggrayresponsecurve"></a><span data-ttu-id="d1e65-738">Propertytaggrayresponsecurve</span><span class="sxs-lookup"><span data-stu-id="d1e65-738">PropertyTagGrayResponseCurve</span></span>

<span data-ttu-id="d1e65-739">Die optische Dichte dieses Pixel Werts für jeden möglichen Pixelwert in einem Graustufenbild.</span><span class="sxs-lookup"><span data-stu-id="d1e65-739">For each possible pixel value in a grayscale image, the optical density of that pixel value.</span></span>



| <span data-ttu-id="d1e65-740">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-740">Property info</span></span> | <span data-ttu-id="d1e65-741">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-741">Value</span></span> |
|-------|---------------------------------|
| <span data-ttu-id="d1e65-742">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-742">Tag</span></span>   | <span data-ttu-id="d1e65-743">0x0123</span><span class="sxs-lookup"><span data-stu-id="d1e65-743">0x0123</span></span>                          |
| <span data-ttu-id="d1e65-744">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-744">Type</span></span>  | <span data-ttu-id="d1e65-745">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-745">PropertyTagTypeShort</span></span>            |
| <span data-ttu-id="d1e65-746">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-746">Count</span></span> | <span data-ttu-id="d1e65-747">Anzahl möglicher Pixelwerte</span><span class="sxs-lookup"><span data-stu-id="d1e65-747">Number of possible pixel values</span></span> |



 

## <a name="propertytagt4option"></a><span data-ttu-id="d1e65-748">PropertyTagT4Option</span><span class="sxs-lookup"><span data-stu-id="d1e65-748">PropertyTagT4Option</span></span>

<span data-ttu-id="d1e65-749">Ein Satz von Flags, die sich auf die T4-Codierung beziehen.</span><span class="sxs-lookup"><span data-stu-id="d1e65-749">Set of flags that relate to T4 encoding.</span></span>



| <span data-ttu-id="d1e65-750">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-750">Property info</span></span> | <span data-ttu-id="d1e65-751">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-751">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="d1e65-752">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-752">Tag</span></span>   | <span data-ttu-id="d1e65-753">0x0124</span><span class="sxs-lookup"><span data-stu-id="d1e65-753">0x0124</span></span>              |
| <span data-ttu-id="d1e65-754">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-754">Type</span></span>  | <span data-ttu-id="d1e65-755">Propertytagtypelong</span><span class="sxs-lookup"><span data-stu-id="d1e65-755">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="d1e65-756">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-756">Count</span></span> | <span data-ttu-id="d1e65-757">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-757">1</span></span>                   |



 

## <a name="propertytagt6option"></a><span data-ttu-id="d1e65-758">PropertyTagT6Option</span><span class="sxs-lookup"><span data-stu-id="d1e65-758">PropertyTagT6Option</span></span>

<span data-ttu-id="d1e65-759">Ein Satz von Flags, die sich auf die T6-Codierung beziehen.</span><span class="sxs-lookup"><span data-stu-id="d1e65-759">Set of flags that relate to T6 encoding.</span></span>



| <span data-ttu-id="d1e65-760">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-760">Property info</span></span> | <span data-ttu-id="d1e65-761">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-761">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="d1e65-762">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-762">Tag</span></span>   | <span data-ttu-id="d1e65-763">0x0125</span><span class="sxs-lookup"><span data-stu-id="d1e65-763">0x0125</span></span>              |
| <span data-ttu-id="d1e65-764">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-764">Type</span></span>  | <span data-ttu-id="d1e65-765">Propertytagtypelong</span><span class="sxs-lookup"><span data-stu-id="d1e65-765">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="d1e65-766">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-766">Count</span></span> | <span data-ttu-id="d1e65-767">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-767">1</span></span>                   |



 

## <a name="propertytagresolutionunit"></a><span data-ttu-id="d1e65-768">Propertytagresolutionunit</span><span class="sxs-lookup"><span data-stu-id="d1e65-768">PropertyTagResolutionUnit</span></span>

<span data-ttu-id="d1e65-769">Maßeinheit für die horizontale Auflösung und die vertikale Auflösung.</span><span class="sxs-lookup"><span data-stu-id="d1e65-769">Unit of measure for the horizontal resolution and the vertical resolution.</span></span>



<span data-ttu-id="d1e65-770">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-770">Tag</span></span>

<span data-ttu-id="d1e65-771">0x0128</span><span class="sxs-lookup"><span data-stu-id="d1e65-771">0x0128</span></span>

<span data-ttu-id="d1e65-772">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-772">Type</span></span>

<span data-ttu-id="d1e65-773">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-773">PropertyTagTypeShort</span></span>

<span data-ttu-id="d1e65-774">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-774">Count</span></span>

<span data-ttu-id="d1e65-775">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-775">1</span></span>

<span data-ttu-id="d1e65-776">2 Zoll, 3 Zentimeter</span><span class="sxs-lookup"><span data-stu-id="d1e65-776">2 - inch 3 - centimeter</span></span>



 

## <a name="propertytagpagenumber"></a><span data-ttu-id="d1e65-777">Propertytagpagenumber</span><span class="sxs-lookup"><span data-stu-id="d1e65-777">PropertyTagPageNumber</span></span>

<span data-ttu-id="d1e65-778">Die Seitenzahl der Seite, von der das Bild gescannt wurde.</span><span class="sxs-lookup"><span data-stu-id="d1e65-778">Page number of the page from which the image was scanned.</span></span>



| <span data-ttu-id="d1e65-779">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-779">Property info</span></span> | <span data-ttu-id="d1e65-780">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-780">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="d1e65-781">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-781">Tag</span></span>   | <span data-ttu-id="d1e65-782">0x0129</span><span class="sxs-lookup"><span data-stu-id="d1e65-782">0x0129</span></span>               |
| <span data-ttu-id="d1e65-783">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-783">Type</span></span>  | <span data-ttu-id="d1e65-784">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-784">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="d1e65-785">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-785">Count</span></span> | <span data-ttu-id="d1e65-786">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-786">1</span></span>                    |



 

## <a name="propertytagtransferfunction"></a><span data-ttu-id="d1e65-787">Propertytagtransferfunction</span><span class="sxs-lookup"><span data-stu-id="d1e65-787">PropertyTagTransferFunction</span></span>

<span data-ttu-id="d1e65-788">Tabellen, die Übertragungsfunktionen für das Image angeben.</span><span class="sxs-lookup"><span data-stu-id="d1e65-788">Tables that specify transfer functions for the image.</span></span>



| <span data-ttu-id="d1e65-789">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-789">Property info</span></span> | <span data-ttu-id="d1e65-790">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-790">Value</span></span> |
|-------|------------------------------------------------------|
| <span data-ttu-id="d1e65-791">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-791">Tag</span></span>   | <span data-ttu-id="d1e65-792">0x012d</span><span class="sxs-lookup"><span data-stu-id="d1e65-792">0x012D</span></span>                                               |
| <span data-ttu-id="d1e65-793">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-793">Type</span></span>  | <span data-ttu-id="d1e65-794">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-794">PropertyTagTypeShort</span></span>                                 |
| <span data-ttu-id="d1e65-795">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-795">Count</span></span> | <span data-ttu-id="d1e65-796">Die Gesamtanzahl der für die Tabellen erforderlichen 16-Bit-Wörter.</span><span class="sxs-lookup"><span data-stu-id="d1e65-796">Total number of 16-bit words required for the tables</span></span> |



 

## <a name="propertytagsoftwareused"></a><span data-ttu-id="d1e65-797">Propertytagsoftwareused</span><span class="sxs-lookup"><span data-stu-id="d1e65-797">PropertyTagSoftwareUsed</span></span>

<span data-ttu-id="d1e65-798">Mit NULL endende Zeichenfolge, die den Namen und die Version der Software oder Firmware des Geräts angibt, das zum Generieren des Images verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="d1e65-798">Null-terminated character string that specifies the name and version of the software or firmware of the device used to generate the image.</span></span>



| <span data-ttu-id="d1e65-799">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-799">Property info</span></span> | <span data-ttu-id="d1e65-800">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-800">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="d1e65-801">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-801">Tag</span></span>   | <span data-ttu-id="d1e65-802">0x0131</span><span class="sxs-lookup"><span data-stu-id="d1e65-802">0x0131</span></span>                                             |
| <span data-ttu-id="d1e65-803">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-803">Type</span></span>  | <span data-ttu-id="d1e65-804">Propertytagtybäuercii</span><span class="sxs-lookup"><span data-stu-id="d1e65-804">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="d1e65-805">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-805">Count</span></span> | <span data-ttu-id="d1e65-806">Länge der Zeichenfolge einschließlich des NULL-Terminator</span><span class="sxs-lookup"><span data-stu-id="d1e65-806">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagdatetime"></a><span data-ttu-id="d1e65-807">Propertytagdatetime</span><span class="sxs-lookup"><span data-stu-id="d1e65-807">PropertyTagDateTime</span></span>

<span data-ttu-id="d1e65-808">Datum und Uhrzeit der Erstellung des Bilds.</span><span class="sxs-lookup"><span data-stu-id="d1e65-808">Date and time the image was created.</span></span>



| <span data-ttu-id="d1e65-809">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-809">Property info</span></span> | <span data-ttu-id="d1e65-810">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-810">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="d1e65-811">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-811">Tag</span></span>   | <span data-ttu-id="d1e65-812">0x0132</span><span class="sxs-lookup"><span data-stu-id="d1e65-812">0x0132</span></span>               |
| <span data-ttu-id="d1e65-813">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-813">Type</span></span>  | <span data-ttu-id="d1e65-814">Propertytagtybäuercii</span><span class="sxs-lookup"><span data-stu-id="d1e65-814">PropertyTagTypeASCII</span></span> |
| <span data-ttu-id="d1e65-815">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-815">Count</span></span> | <span data-ttu-id="d1e65-816">20</span><span class="sxs-lookup"><span data-stu-id="d1e65-816">20</span></span>                   |



 

## <a name="propertytagartist"></a><span data-ttu-id="d1e65-817">Propertytagartist</span><span class="sxs-lookup"><span data-stu-id="d1e65-817">PropertyTagArtist</span></span>

<span data-ttu-id="d1e65-818">Mit NULL beendete Zeichenfolge, die den Namen der Person angibt, die das Image erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="d1e65-818">Null-terminated character string that specifies the name of the person who created the image.</span></span>



| <span data-ttu-id="d1e65-819">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-819">Property info</span></span> | <span data-ttu-id="d1e65-820">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-820">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="d1e65-821">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-821">Tag</span></span>   | <span data-ttu-id="d1e65-822">0x013b</span><span class="sxs-lookup"><span data-stu-id="d1e65-822">0x013B</span></span>                                             |
| <span data-ttu-id="d1e65-823">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-823">Type</span></span>  | <span data-ttu-id="d1e65-824">Propertytagtybäuercii</span><span class="sxs-lookup"><span data-stu-id="d1e65-824">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="d1e65-825">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-825">Count</span></span> | <span data-ttu-id="d1e65-826">Länge der Zeichenfolge einschließlich des NULL-Terminator</span><span class="sxs-lookup"><span data-stu-id="d1e65-826">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytaghostcomputer"></a><span data-ttu-id="d1e65-827">Propertytaghostcomputer</span><span class="sxs-lookup"><span data-stu-id="d1e65-827">PropertyTagHostComputer</span></span>

<span data-ttu-id="d1e65-828">Mit NULL endende Zeichenfolge, die den Computer und/oder das Betriebssystem angibt, mit dem das Image erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="d1e65-828">Null-terminated character string that specifies the computer and/or operating system used to create the image.</span></span>



| <span data-ttu-id="d1e65-829">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-829">Property info</span></span> | <span data-ttu-id="d1e65-830">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-830">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="d1e65-831">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-831">Tag</span></span>   | <span data-ttu-id="d1e65-832">0x013c</span><span class="sxs-lookup"><span data-stu-id="d1e65-832">0x013C</span></span>                                             |
| <span data-ttu-id="d1e65-833">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-833">Type</span></span>  | <span data-ttu-id="d1e65-834">Propertytagtybäuercii</span><span class="sxs-lookup"><span data-stu-id="d1e65-834">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="d1e65-835">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-835">Count</span></span> | <span data-ttu-id="d1e65-836">Länge der Zeichenfolge einschließlich des NULL-Terminator</span><span class="sxs-lookup"><span data-stu-id="d1e65-836">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagpredictor"></a><span data-ttu-id="d1e65-837">Propertytagvorhertor</span><span class="sxs-lookup"><span data-stu-id="d1e65-837">PropertyTagPredictor</span></span>

<span data-ttu-id="d1e65-838">Der Typ des Vorhersage Schemas, das auf die Bilddaten angewendet wurde, bevor das Codierungsschema angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="d1e65-838">Type of prediction scheme that was applied to the image data before the encoding scheme was applied.</span></span>



| <span data-ttu-id="d1e65-839">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-839">Property info</span></span> | <span data-ttu-id="d1e65-840">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-840">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="d1e65-841">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-841">Tag</span></span>   | <span data-ttu-id="d1e65-842">0x013d</span><span class="sxs-lookup"><span data-stu-id="d1e65-842">0x013D</span></span>               |
| <span data-ttu-id="d1e65-843">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-843">Type</span></span>  | <span data-ttu-id="d1e65-844">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-844">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="d1e65-845">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-845">Count</span></span> | <span data-ttu-id="d1e65-846">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-846">1</span></span>                    |



 

## <a name="propertytagwhitepoint"></a><span data-ttu-id="d1e65-847">Propertytagwhitepoint</span><span class="sxs-lookup"><span data-stu-id="d1e65-847">PropertyTagWhitePoint</span></span>

<span data-ttu-id="d1e65-848">Die Chromatizität des weißen Punkts des Bilds.</span><span class="sxs-lookup"><span data-stu-id="d1e65-848">Chromaticity of the white point of the image.</span></span>



| <span data-ttu-id="d1e65-849">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-849">Property info</span></span> | <span data-ttu-id="d1e65-850">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-850">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="d1e65-851">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-851">Tag</span></span>   | <span data-ttu-id="d1e65-852">0x013e</span><span class="sxs-lookup"><span data-stu-id="d1e65-852">0x013E</span></span>                  |
| <span data-ttu-id="d1e65-853">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-853">Type</span></span>  | <span data-ttu-id="d1e65-854">Propertytagtyperational</span><span class="sxs-lookup"><span data-stu-id="d1e65-854">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="d1e65-855">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-855">Count</span></span> | <span data-ttu-id="d1e65-856">2</span><span class="sxs-lookup"><span data-stu-id="d1e65-856">2</span></span>                       |



 

## <a name="propertytagprimarychromaticities"></a><span data-ttu-id="d1e65-857">Propertytagprimarychromaticities</span><span class="sxs-lookup"><span data-stu-id="d1e65-857">PropertyTagPrimaryChromaticities</span></span>

<span data-ttu-id="d1e65-858">Für jede der drei Primärfarben im Bild die Chromatizität dieser Farbe.</span><span class="sxs-lookup"><span data-stu-id="d1e65-858">For each of the three primary colors in the image, the chromaticity of that color.</span></span>



| <span data-ttu-id="d1e65-859">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-859">Property info</span></span> | <span data-ttu-id="d1e65-860">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-860">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="d1e65-861">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-861">Tag</span></span>   | <span data-ttu-id="d1e65-862">0x013f</span><span class="sxs-lookup"><span data-stu-id="d1e65-862">0x013F</span></span>                  |
| <span data-ttu-id="d1e65-863">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-863">Type</span></span>  | <span data-ttu-id="d1e65-864">Propertytagtyperational</span><span class="sxs-lookup"><span data-stu-id="d1e65-864">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="d1e65-865">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-865">Count</span></span> | <span data-ttu-id="d1e65-866">6</span><span class="sxs-lookup"><span data-stu-id="d1e65-866">6</span></span>                       |



 

## <a name="propertytagcolormap"></a><span data-ttu-id="d1e65-867">Propertytagcolormap</span><span class="sxs-lookup"><span data-stu-id="d1e65-867">PropertyTagColorMap</span></span>

<span data-ttu-id="d1e65-868">Farbpalette (Nachschlage Tabelle) für ein palettenindiziertes Bild.</span><span class="sxs-lookup"><span data-stu-id="d1e65-868">Color palette (lookup table) for a palette-indexed image.</span></span>



| <span data-ttu-id="d1e65-869">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-869">Property info</span></span> | <span data-ttu-id="d1e65-870">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-870">Value</span></span> |
|-------|-------------------------------------------------|
| <span data-ttu-id="d1e65-871">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-871">Tag</span></span>   | <span data-ttu-id="d1e65-872">0x0140</span><span class="sxs-lookup"><span data-stu-id="d1e65-872">0x0140</span></span>                                          |
| <span data-ttu-id="d1e65-873">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-873">Type</span></span>  | <span data-ttu-id="d1e65-874">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-874">PropertyTagTypeShort</span></span>                            |
| <span data-ttu-id="d1e65-875">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-875">Count</span></span> | <span data-ttu-id="d1e65-876">Die Anzahl der für die Palette erforderlichen 16-Bit-Wörter.</span><span class="sxs-lookup"><span data-stu-id="d1e65-876">Number of 16-bit words required for the palette</span></span> |



 

## <a name="propertytaghalftonehints"></a><span data-ttu-id="d1e65-877">Propertytaghalftonehints</span><span class="sxs-lookup"><span data-stu-id="d1e65-877">PropertyTagHalftoneHints</span></span>

<span data-ttu-id="d1e65-878">Von der Funktion "Halbton" verwendete Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-878">Information used by the halftone function</span></span>



| <span data-ttu-id="d1e65-879">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-879">Property info</span></span> | <span data-ttu-id="d1e65-880">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-880">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="d1e65-881">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-881">Tag</span></span>   | <span data-ttu-id="d1e65-882">0x0141</span><span class="sxs-lookup"><span data-stu-id="d1e65-882">0x0141</span></span>               |
| <span data-ttu-id="d1e65-883">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-883">Type</span></span>  | <span data-ttu-id="d1e65-884">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-884">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="d1e65-885">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-885">Count</span></span> | <span data-ttu-id="d1e65-886">2</span><span class="sxs-lookup"><span data-stu-id="d1e65-886">2</span></span>                    |



 

## <a name="propertytagtilewidth"></a><span data-ttu-id="d1e65-887">Propertytagtilewidth</span><span class="sxs-lookup"><span data-stu-id="d1e65-887">PropertyTagTileWidth</span></span>

<span data-ttu-id="d1e65-888">Anzahl der Pixel Spalten in den einzelnen Kacheln.</span><span class="sxs-lookup"><span data-stu-id="d1e65-888">Number of pixel columns in each tile.</span></span>



| <span data-ttu-id="d1e65-889">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-889">Property info</span></span> | <span data-ttu-id="d1e65-890">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-890">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="d1e65-891">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-891">Tag</span></span>   | <span data-ttu-id="d1e65-892">0x0142</span><span class="sxs-lookup"><span data-stu-id="d1e65-892">0x0142</span></span>                                      |
| <span data-ttu-id="d1e65-893">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-893">Type</span></span>  | <span data-ttu-id="d1e65-894">Propertytagtypeshort oder propertytagtypelong</span><span class="sxs-lookup"><span data-stu-id="d1e65-894">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="d1e65-895">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-895">Count</span></span> | <span data-ttu-id="d1e65-896">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-896">1</span></span>                                           |



 

## <a name="propertytagtilelength"></a><span data-ttu-id="d1e65-897">Propertytagtilelength</span><span class="sxs-lookup"><span data-stu-id="d1e65-897">PropertyTagTileLength</span></span>

<span data-ttu-id="d1e65-898">Anzahl der Pixel Zeilen in jeder Kachel.</span><span class="sxs-lookup"><span data-stu-id="d1e65-898">Number of pixel rows in each tile.</span></span>



| <span data-ttu-id="d1e65-899">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-899">Property info</span></span> | <span data-ttu-id="d1e65-900">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-900">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="d1e65-901">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-901">Tag</span></span>   | <span data-ttu-id="d1e65-902">0x0143</span><span class="sxs-lookup"><span data-stu-id="d1e65-902">0x0143</span></span>                                      |
| <span data-ttu-id="d1e65-903">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-903">Type</span></span>  | <span data-ttu-id="d1e65-904">Propertytagtypeshort oder propertytagtypelong</span><span class="sxs-lookup"><span data-stu-id="d1e65-904">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="d1e65-905">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-905">Count</span></span> | <span data-ttu-id="d1e65-906">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-906">1</span></span>                                           |



 

## <a name="propertytagtileoffset"></a><span data-ttu-id="d1e65-907">Propertytagtileoffset</span><span class="sxs-lookup"><span data-stu-id="d1e65-907">PropertyTagTileOffset</span></span>

<span data-ttu-id="d1e65-908">Für jede Kachel der Byte Offset der Kachel.</span><span class="sxs-lookup"><span data-stu-id="d1e65-908">For each tile, the byte offset of that tile.</span></span>



| <span data-ttu-id="d1e65-909">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-909">Property info</span></span> | <span data-ttu-id="d1e65-910">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-910">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="d1e65-911">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-911">Tag</span></span>   | <span data-ttu-id="d1e65-912">0x0144</span><span class="sxs-lookup"><span data-stu-id="d1e65-912">0x0144</span></span>              |
| <span data-ttu-id="d1e65-913">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-913">Type</span></span>  | <span data-ttu-id="d1e65-914">Propertytagtypelong</span><span class="sxs-lookup"><span data-stu-id="d1e65-914">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="d1e65-915">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-915">Count</span></span> | <span data-ttu-id="d1e65-916">Anzahl von Kacheln</span><span class="sxs-lookup"><span data-stu-id="d1e65-916">Number of tiles</span></span>     |



 

## <a name="propertytagtilebytecounts"></a><span data-ttu-id="d1e65-917">Propertytagtilebytecounts</span><span class="sxs-lookup"><span data-stu-id="d1e65-917">PropertyTagTileByteCounts</span></span>

<span data-ttu-id="d1e65-918">Für jede Kachel die Anzahl der Bytes in der Kachel.</span><span class="sxs-lookup"><span data-stu-id="d1e65-918">For each tile, the number of bytes in that tile.</span></span>



| <span data-ttu-id="d1e65-919">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-919">Property info</span></span> | <span data-ttu-id="d1e65-920">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-920">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="d1e65-921">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-921">Tag</span></span>   | <span data-ttu-id="d1e65-922">0x0145</span><span class="sxs-lookup"><span data-stu-id="d1e65-922">0x0145</span></span>                                      |
| <span data-ttu-id="d1e65-923">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-923">Type</span></span>  | <span data-ttu-id="d1e65-924">Propertytagtypeshort oder propertytagtypelong</span><span class="sxs-lookup"><span data-stu-id="d1e65-924">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="d1e65-925">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-925">Count</span></span> | <span data-ttu-id="d1e65-926">Anzahl von Kacheln</span><span class="sxs-lookup"><span data-stu-id="d1e65-926">Number of tiles</span></span>                             |



 

## <a name="propertytaginkset"></a><span data-ttu-id="d1e65-927">Propertytaginkset</span><span class="sxs-lookup"><span data-stu-id="d1e65-927">PropertyTagInkSet</span></span>

<span data-ttu-id="d1e65-928">Eine Reihe von Farben, die in einem getrennten Bild verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d1e65-928">Set of inks used in a separated image.</span></span>



| <span data-ttu-id="d1e65-929">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-929">Property info</span></span> | <span data-ttu-id="d1e65-930">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-930">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="d1e65-931">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-931">Tag</span></span>   | <span data-ttu-id="d1e65-932">0x014c</span><span class="sxs-lookup"><span data-stu-id="d1e65-932">0x014C</span></span>               |
| <span data-ttu-id="d1e65-933">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-933">Type</span></span>  | <span data-ttu-id="d1e65-934">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-934">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="d1e65-935">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-935">Count</span></span> | <span data-ttu-id="d1e65-936">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-936">1</span></span>                    |



 

## <a name="propertytaginknames"></a><span data-ttu-id="d1e65-937">Propertytaginknames</span><span class="sxs-lookup"><span data-stu-id="d1e65-937">PropertyTagInkNames</span></span>

<span data-ttu-id="d1e65-938">Sequenz von verketteten, auf NULL endenden Zeichen folgen, die die Namen der in einem getrennten Bild verwendeten Farben angeben.</span><span class="sxs-lookup"><span data-stu-id="d1e65-938">Sequence of concatenated, null-terminated, character strings that specify the names of the inks used in a separated image.</span></span>



| <span data-ttu-id="d1e65-939">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-939">Property info</span></span> | <span data-ttu-id="d1e65-940">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-940">Value</span></span> |
|-------|------------------------------------------------------------------------|
| <span data-ttu-id="d1e65-941">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-941">Tag</span></span>   | <span data-ttu-id="d1e65-942">0x014d</span><span class="sxs-lookup"><span data-stu-id="d1e65-942">0x014D</span></span>                                                                 |
| <span data-ttu-id="d1e65-943">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-943">Type</span></span>  | <span data-ttu-id="d1e65-944">Propertytagtybäuercii</span><span class="sxs-lookup"><span data-stu-id="d1e65-944">PropertyTagTypeASCII</span></span>                                                   |
| <span data-ttu-id="d1e65-945">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-945">Count</span></span> | <span data-ttu-id="d1e65-946">Gesamtlänge der Sequenz von Zeichen folgen einschließlich der NULL-Abschluss Zeichen</span><span class="sxs-lookup"><span data-stu-id="d1e65-946">Total length of the sequence of strings including the NULL terminators</span></span> |



 

## <a name="propertytagnumberofinks"></a><span data-ttu-id="d1e65-947">Propertytagnumofinert</span><span class="sxs-lookup"><span data-stu-id="d1e65-947">PropertyTagNumberOfInks</span></span>

<span data-ttu-id="d1e65-948">Anzahl der Farben.</span><span class="sxs-lookup"><span data-stu-id="d1e65-948">Number of inks.</span></span>



| <span data-ttu-id="d1e65-949">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-949">Property info</span></span> | <span data-ttu-id="d1e65-950">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-950">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="d1e65-951">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-951">Tag</span></span>   | <span data-ttu-id="d1e65-952">0x014e</span><span class="sxs-lookup"><span data-stu-id="d1e65-952">0x014E</span></span>               |
| <span data-ttu-id="d1e65-953">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-953">Type</span></span>  | <span data-ttu-id="d1e65-954">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-954">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="d1e65-955">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-955">Count</span></span> | <span data-ttu-id="d1e65-956">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-956">1</span></span>                    |



 

## <a name="propertytagdotrange"></a><span data-ttu-id="d1e65-957">Propertytagdotrange</span><span class="sxs-lookup"><span data-stu-id="d1e65-957">PropertyTagDotRange</span></span>

<span data-ttu-id="d1e65-958">Farbkomponenten Werte, die einem Punkt von 0 Prozent und einem Punkt von 100 Prozent entsprechen.</span><span class="sxs-lookup"><span data-stu-id="d1e65-958">Color component values that correspond to a 0 percent dot and a 100 percent dot.</span></span>



| <span data-ttu-id="d1e65-959">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-959">Property info</span></span> | <span data-ttu-id="d1e65-960">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-960">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="d1e65-961">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-961">Tag</span></span>   | <span data-ttu-id="d1e65-962">0x0150</span><span class="sxs-lookup"><span data-stu-id="d1e65-962">0x0150</span></span>                                      |
| <span data-ttu-id="d1e65-963">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-963">Type</span></span>  | <span data-ttu-id="d1e65-964">Propertytagtypebyte oder propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-964">PropertyTagTypeByte or PropertyTagTypeShort</span></span> |
| <span data-ttu-id="d1e65-965">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-965">Count</span></span> | <span data-ttu-id="d1e65-966">2 oder 2 × propertytagsamplesperpixel</span><span class="sxs-lookup"><span data-stu-id="d1e65-966">2 or 2×PropertyTagSamplesPerPixel</span></span>           |



 

## <a name="propertytagtargetprinter"></a><span data-ttu-id="d1e65-967">Propertytagtargetprinter</span><span class="sxs-lookup"><span data-stu-id="d1e65-967">PropertyTagTargetPrinter</span></span>

<span data-ttu-id="d1e65-968">Mit NULL beendete Zeichenfolge, die die vorgesehene Druckumgebung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="d1e65-968">Null-terminated character string that describes the intended printing environment.</span></span>



| <span data-ttu-id="d1e65-969">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-969">Property info</span></span> | <span data-ttu-id="d1e65-970">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-970">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="d1e65-971">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-971">Tag</span></span>   | <span data-ttu-id="d1e65-972">0x0151</span><span class="sxs-lookup"><span data-stu-id="d1e65-972">0x0151</span></span>                                             |
| <span data-ttu-id="d1e65-973">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-973">Type</span></span>  | <span data-ttu-id="d1e65-974">Propertytagtybäuercii</span><span class="sxs-lookup"><span data-stu-id="d1e65-974">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="d1e65-975">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-975">Count</span></span> | <span data-ttu-id="d1e65-976">Länge der Zeichenfolge einschließlich des NULL-Terminator</span><span class="sxs-lookup"><span data-stu-id="d1e65-976">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagextrasamples"></a><span data-ttu-id="d1e65-977">Propertytagextrasamples</span><span class="sxs-lookup"><span data-stu-id="d1e65-977">PropertyTagExtraSamples</span></span>

<span data-ttu-id="d1e65-978">Anzahl der zusätzlichen Farbkomponenten.</span><span class="sxs-lookup"><span data-stu-id="d1e65-978">Number of extra color components.</span></span> <span data-ttu-id="d1e65-979">Beispielsweise kann eine zusätzliche Komponente einen Alpha-Wert enthalten.</span><span class="sxs-lookup"><span data-stu-id="d1e65-979">For example, one extra component might hold an alpha value.</span></span>



| <span data-ttu-id="d1e65-980">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-980">Property info</span></span> | <span data-ttu-id="d1e65-981">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-981">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="d1e65-982">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-982">Tag</span></span>   | <span data-ttu-id="d1e65-983">0x0152</span><span class="sxs-lookup"><span data-stu-id="d1e65-983">0x0152</span></span>               |
| <span data-ttu-id="d1e65-984">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-984">Type</span></span>  | <span data-ttu-id="d1e65-985">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-985">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="d1e65-986">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-986">Count</span></span> | <span data-ttu-id="d1e65-987">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-987">1</span></span>                    |



 

## <a name="propertytagsampleformat"></a><span data-ttu-id="d1e65-988">Propertytagsampleformat</span><span class="sxs-lookup"><span data-stu-id="d1e65-988">PropertyTagSampleFormat</span></span>

<span data-ttu-id="d1e65-989">Für jede Farbkomponente das numerische Format (unsigned, signed, Floating Point) dieser Komponente.</span><span class="sxs-lookup"><span data-stu-id="d1e65-989">For each color component, the numerical format (unsigned, signed, floating point) of that component.</span></span> <span data-ttu-id="d1e65-990">Siehe auch [propertytagsamplesperpixel](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="d1e65-990">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="d1e65-991">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-991">Property info</span></span> | <span data-ttu-id="d1e65-992">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-992">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="d1e65-993">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-993">Tag</span></span>   | <span data-ttu-id="d1e65-994">0x0153</span><span class="sxs-lookup"><span data-stu-id="d1e65-994">0x0153</span></span>                                   |
| <span data-ttu-id="d1e65-995">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-995">Type</span></span>  | <span data-ttu-id="d1e65-996">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-996">PropertyTagTypeShort</span></span>                     |
| <span data-ttu-id="d1e65-997">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-997">Count</span></span> | <span data-ttu-id="d1e65-998">Anzahl von Stichproben (Komponenten) pro Pixel</span><span class="sxs-lookup"><span data-stu-id="d1e65-998">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagsminsamplevalue"></a><span data-ttu-id="d1e65-999">Propertytagsminsamplevalue</span><span class="sxs-lookup"><span data-stu-id="d1e65-999">PropertyTagSMinSampleValue</span></span>

<span data-ttu-id="d1e65-1000">Für jede Farbkomponente der minimale Wert dieser Komponente.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1000">For each color component, the minimum value of that component.</span></span> <span data-ttu-id="d1e65-1001">Siehe auch [propertytagsamplesperpixel](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="d1e65-1001">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="d1e65-1002">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1002">Property info</span></span> | <span data-ttu-id="d1e65-1003">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1003">Value</span></span> |
|-------|-----------------------------------------------------|
| <span data-ttu-id="d1e65-1004">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1004">Tag</span></span>   | <span data-ttu-id="d1e65-1005">0x0154</span><span class="sxs-lookup"><span data-stu-id="d1e65-1005">0x0154</span></span>                                              |
| <span data-ttu-id="d1e65-1006">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1006">Type</span></span>  | <span data-ttu-id="d1e65-1007">Der Typ, der am besten mit den Pixel Komponenten Daten übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1007">The type that best matches the pixel component data</span></span> |
| <span data-ttu-id="d1e65-1008">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1008">Count</span></span> | <span data-ttu-id="d1e65-1009">Anzahl von Stichproben (Komponenten) pro Pixel</span><span class="sxs-lookup"><span data-stu-id="d1e65-1009">Number of samples (components) per pixel</span></span>            |



 

## <a name="propertytagsmaxsamplevalue"></a><span data-ttu-id="d1e65-1010">Propertytagsmaxsamplevalue</span><span class="sxs-lookup"><span data-stu-id="d1e65-1010">PropertyTagSMaxSampleValue</span></span>

<span data-ttu-id="d1e65-1011">Der maximale Wert dieser Komponente für jede Farbkomponente.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1011">For each color component, the maximum value of that component.</span></span> <span data-ttu-id="d1e65-1012">Siehe auch [propertytagsamplesperpixel](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="d1e65-1012">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="d1e65-1013">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1013">Property info</span></span> | <span data-ttu-id="d1e65-1014">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1014">Value</span></span> |
|-------|-----------------------------------------------------|
| <span data-ttu-id="d1e65-1015">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1015">Tag</span></span>   | <span data-ttu-id="d1e65-1016">0x0155</span><span class="sxs-lookup"><span data-stu-id="d1e65-1016">0x0155</span></span>                                              |
| <span data-ttu-id="d1e65-1017">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1017">Type</span></span>  | <span data-ttu-id="d1e65-1018">Der Typ, der am besten mit den Pixel Komponenten Daten übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1018">The type that best matches the pixel component data</span></span> |
| <span data-ttu-id="d1e65-1019">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1019">Count</span></span> | <span data-ttu-id="d1e65-1020">Anzahl von Stichproben (Komponenten) pro Pixel</span><span class="sxs-lookup"><span data-stu-id="d1e65-1020">Number of samples (components) per pixel</span></span>            |



 

## <a name="propertytagtransferrange"></a><span data-ttu-id="d1e65-1021">Propertytagtransferrange</span><span class="sxs-lookup"><span data-stu-id="d1e65-1021">PropertyTagTransferRange</span></span>

<span data-ttu-id="d1e65-1022">Tabelle mit Werten, die den Bereich der Übertragungsfunktion erweitern.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1022">Table of values that extends the range of the transfer function.</span></span>



| <span data-ttu-id="d1e65-1023">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1023">Property info</span></span> | <span data-ttu-id="d1e65-1024">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1024">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="d1e65-1025">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1025">Tag</span></span>   | <span data-ttu-id="d1e65-1026">0x0156</span><span class="sxs-lookup"><span data-stu-id="d1e65-1026">0x0156</span></span>               |
| <span data-ttu-id="d1e65-1027">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1027">Type</span></span>  | <span data-ttu-id="d1e65-1028">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-1028">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="d1e65-1029">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1029">Count</span></span> | <span data-ttu-id="d1e65-1030">6</span><span class="sxs-lookup"><span data-stu-id="d1e65-1030">6</span></span>                    |



 

## <a name="propertytagjpegproc"></a><span data-ttu-id="d1e65-1031">Propertytagjpgproc</span><span class="sxs-lookup"><span data-stu-id="d1e65-1031">PropertyTagJPEGProc</span></span>

<span data-ttu-id="d1e65-1032">JPEG-Komprimierungs Vorgang.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1032">JPEG compression process.</span></span>



| <span data-ttu-id="d1e65-1033">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1033">Property info</span></span> | <span data-ttu-id="d1e65-1034">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1034">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="d1e65-1035">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1035">Tag</span></span>   | <span data-ttu-id="d1e65-1036">0x0200</span><span class="sxs-lookup"><span data-stu-id="d1e65-1036">0x0200</span></span>               |
| <span data-ttu-id="d1e65-1037">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1037">Type</span></span>  | <span data-ttu-id="d1e65-1038">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-1038">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="d1e65-1039">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1039">Count</span></span> | <span data-ttu-id="d1e65-1040">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-1040">1</span></span>                    |



 

## <a name="propertytagjpeginterformat"></a><span data-ttu-id="d1e65-1041">Propertytagjpeer ginterformat</span><span class="sxs-lookup"><span data-stu-id="d1e65-1041">PropertyTagJPEGInterFormat</span></span>

<span data-ttu-id="d1e65-1042">Offset bis zum Anfang eines JPEG-Bitstreams.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1042">Offset to the start of a JPEG bitstream.</span></span>



| <span data-ttu-id="d1e65-1043">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1043">Property info</span></span> | <span data-ttu-id="d1e65-1044">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1044">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="d1e65-1045">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1045">Tag</span></span>   | <span data-ttu-id="d1e65-1046">0x0201</span><span class="sxs-lookup"><span data-stu-id="d1e65-1046">0x0201</span></span>              |
| <span data-ttu-id="d1e65-1047">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1047">Type</span></span>  | <span data-ttu-id="d1e65-1048">Propertytagtypelong</span><span class="sxs-lookup"><span data-stu-id="d1e65-1048">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="d1e65-1049">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1049">Count</span></span> | <span data-ttu-id="d1e65-1050">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-1050">1</span></span>                   |



 

## <a name="propertytagjpeginterlength"></a><span data-ttu-id="d1e65-1051">Propertytagjpeer-interlength</span><span class="sxs-lookup"><span data-stu-id="d1e65-1051">PropertyTagJPEGInterLength</span></span>

<span data-ttu-id="d1e65-1052">Länge des JPEG-Bitstreams in Bytes.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1052">Length, in bytes, of the JPEG bitstream.</span></span>



| <span data-ttu-id="d1e65-1053">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1053">Property info</span></span> | <span data-ttu-id="d1e65-1054">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1054">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="d1e65-1055">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1055">Tag</span></span>   | <span data-ttu-id="d1e65-1056">0x0202</span><span class="sxs-lookup"><span data-stu-id="d1e65-1056">0x0202</span></span>              |
| <span data-ttu-id="d1e65-1057">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1057">Type</span></span>  | <span data-ttu-id="d1e65-1058">Propertytagtypelong</span><span class="sxs-lookup"><span data-stu-id="d1e65-1058">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="d1e65-1059">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1059">Count</span></span> | <span data-ttu-id="d1e65-1060">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-1060">1</span></span>                   |



 

## <a name="propertytagjpegrestartinterval"></a><span data-ttu-id="d1e65-1061">Propertytagjggrestartinterval</span><span class="sxs-lookup"><span data-stu-id="d1e65-1061">PropertyTagJPEGRestartInterval</span></span>

<span data-ttu-id="d1e65-1062">Länge des Neustart Intervalls.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1062">Length of the restart interval.</span></span>



| <span data-ttu-id="d1e65-1063">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1063">Property info</span></span> | <span data-ttu-id="d1e65-1064">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1064">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="d1e65-1065">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1065">Tag</span></span>   | <span data-ttu-id="d1e65-1066">0x0203</span><span class="sxs-lookup"><span data-stu-id="d1e65-1066">0x0203</span></span>               |
| <span data-ttu-id="d1e65-1067">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1067">Type</span></span>  | <span data-ttu-id="d1e65-1068">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-1068">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="d1e65-1069">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1069">Count</span></span> | <span data-ttu-id="d1e65-1070">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-1070">1</span></span>                    |



 

## <a name="propertytagjpeglosslesspredictors"></a><span data-ttu-id="d1e65-1071">Propertytagjpeer glosslesendiktoren</span><span class="sxs-lookup"><span data-stu-id="d1e65-1071">PropertyTagJPEGLosslessPredictors</span></span>

<span data-ttu-id="d1e65-1072">Für jede Farbkomponente ein verlustfreier Wert für die Vorhersage der Komponente.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1072">For each color component, a lossless predictor-selection value for that component.</span></span> <span data-ttu-id="d1e65-1073">Siehe auch [propertytagsamplesperpixel](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="d1e65-1073">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="d1e65-1074">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1074">Property info</span></span> | <span data-ttu-id="d1e65-1075">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1075">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="d1e65-1076">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1076">Tag</span></span>   | <span data-ttu-id="d1e65-1077">0x0205</span><span class="sxs-lookup"><span data-stu-id="d1e65-1077">0x0205</span></span>                                   |
| <span data-ttu-id="d1e65-1078">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1078">Type</span></span>  | <span data-ttu-id="d1e65-1079">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-1079">PropertyTagTypeShort</span></span>                     |
| <span data-ttu-id="d1e65-1080">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1080">Count</span></span> | <span data-ttu-id="d1e65-1081">Anzahl von Stichproben (Komponenten) pro Pixel</span><span class="sxs-lookup"><span data-stu-id="d1e65-1081">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagjpegpointtransforms"></a><span data-ttu-id="d1e65-1082">Propertytagjpgpointtransformationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1082">PropertyTagJPEGPointTransforms</span></span>

<span data-ttu-id="d1e65-1083">Für jede Farbkomponente ein Wert für die Punkt Transformation für diese Komponente.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1083">For each color component, a point transformation value for that component.</span></span> <span data-ttu-id="d1e65-1084">Siehe auch [propertytagsamplesperpixel](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="d1e65-1084">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="d1e65-1085">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1085">Property info</span></span> | <span data-ttu-id="d1e65-1086">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1086">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="d1e65-1087">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1087">Tag</span></span>   | <span data-ttu-id="d1e65-1088">0x0206</span><span class="sxs-lookup"><span data-stu-id="d1e65-1088">0x0206</span></span>                                   |
| <span data-ttu-id="d1e65-1089">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1089">Type</span></span>  | <span data-ttu-id="d1e65-1090">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-1090">PropertyTagTypeShort</span></span>                     |
| <span data-ttu-id="d1e65-1091">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1091">Count</span></span> | <span data-ttu-id="d1e65-1092">Anzahl von Stichproben (Komponenten) pro Pixel</span><span class="sxs-lookup"><span data-stu-id="d1e65-1092">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagjpegqtables"></a><span data-ttu-id="d1e65-1093">Propertytagjpgqtables</span><span class="sxs-lookup"><span data-stu-id="d1e65-1093">PropertyTagJPEGQTables</span></span>

<span data-ttu-id="d1e65-1094">Für jede Farbkomponente der Offset zur quantifizierungstabelle für diese Komponente.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1094">For each color component, the offset to the quantization table for that component.</span></span> <span data-ttu-id="d1e65-1095">Siehe auch [propertytagsamplesperpixel](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="d1e65-1095">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="d1e65-1096">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1096">Property info</span></span> | <span data-ttu-id="d1e65-1097">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1097">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="d1e65-1098">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1098">Tag</span></span>   | <span data-ttu-id="d1e65-1099">0x0207</span><span class="sxs-lookup"><span data-stu-id="d1e65-1099">0x0207</span></span>                                   |
| <span data-ttu-id="d1e65-1100">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1100">Type</span></span>  | <span data-ttu-id="d1e65-1101">Propertytagtypelong</span><span class="sxs-lookup"><span data-stu-id="d1e65-1101">PropertyTagTypeLong</span></span>                      |
| <span data-ttu-id="d1e65-1102">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1102">Count</span></span> | <span data-ttu-id="d1e65-1103">Anzahl von Stichproben (Komponenten) pro Pixel</span><span class="sxs-lookup"><span data-stu-id="d1e65-1103">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagjpegdctables"></a><span data-ttu-id="d1e65-1104">Propertytagjpeer dsctables</span><span class="sxs-lookup"><span data-stu-id="d1e65-1104">PropertyTagJPEGDCTables</span></span>

<span data-ttu-id="d1e65-1105">Für jede Farbkomponente der Offset zur DC-Huffman-Tabelle (oder Verlust lose Huffman-Tabelle) für diese Komponente.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1105">For each color component, the offset to the DC Huffman table (or lossless Huffman table) for that component.</span></span> <span data-ttu-id="d1e65-1106">Siehe auch [propertytagsamplesperpixel](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="d1e65-1106">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="d1e65-1107">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1107">Property info</span></span> | <span data-ttu-id="d1e65-1108">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1108">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="d1e65-1109">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1109">Tag</span></span>   | <span data-ttu-id="d1e65-1110">0x0208</span><span class="sxs-lookup"><span data-stu-id="d1e65-1110">0x0208</span></span>                                   |
| <span data-ttu-id="d1e65-1111">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1111">Type</span></span>  | <span data-ttu-id="d1e65-1112">Propertytagtypelong</span><span class="sxs-lookup"><span data-stu-id="d1e65-1112">PropertyTagTypeLong</span></span>                      |
| <span data-ttu-id="d1e65-1113">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1113">Count</span></span> | <span data-ttu-id="d1e65-1114">Anzahl von Stichproben (Komponenten) pro Pixel</span><span class="sxs-lookup"><span data-stu-id="d1e65-1114">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagjpegactables"></a><span data-ttu-id="d1e65-1115">Propertytagjpeer-Tabellen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1115">PropertyTagJPEGACTables</span></span>

<span data-ttu-id="d1e65-1116">Für jede Farbkomponente der Offset zur AC-Huffman-Tabelle für diese Komponente.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1116">For each color component, the offset to the AC Huffman table for that component.</span></span> <span data-ttu-id="d1e65-1117">Siehe auch [propertytagsamplesperpixel](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="d1e65-1117">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="d1e65-1118">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1118">Property info</span></span> | <span data-ttu-id="d1e65-1119">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1119">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="d1e65-1120">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1120">Tag</span></span>   | <span data-ttu-id="d1e65-1121">0x0209</span><span class="sxs-lookup"><span data-stu-id="d1e65-1121">0x0209</span></span>                                   |
| <span data-ttu-id="d1e65-1122">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1122">Type</span></span>  | <span data-ttu-id="d1e65-1123">Propertytagtypelong</span><span class="sxs-lookup"><span data-stu-id="d1e65-1123">PropertyTagTypeLong</span></span>                      |
| <span data-ttu-id="d1e65-1124">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1124">Count</span></span> | <span data-ttu-id="d1e65-1125">Anzahl von Stichproben (Komponenten) pro Pixel</span><span class="sxs-lookup"><span data-stu-id="d1e65-1125">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagycbcrcoefficients"></a><span data-ttu-id="d1e65-1126">Propertytagycbcrkoefficients</span><span class="sxs-lookup"><span data-stu-id="d1e65-1126">PropertyTagYCbCrCoefficients</span></span>

<span data-ttu-id="d1e65-1127">Koeffizienten für die Transformation von RGB zu YCbCr-Bilddaten.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1127">Coefficients for transformation from RGB to YCbCr image data.</span></span>



| <span data-ttu-id="d1e65-1128">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1128">Property info</span></span> | <span data-ttu-id="d1e65-1129">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1129">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="d1e65-1130">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1130">Tag</span></span>   | <span data-ttu-id="d1e65-1131">0x0211</span><span class="sxs-lookup"><span data-stu-id="d1e65-1131">0x0211</span></span>                  |
| <span data-ttu-id="d1e65-1132">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1132">Type</span></span>  | <span data-ttu-id="d1e65-1133">Propertytagtyperational</span><span class="sxs-lookup"><span data-stu-id="d1e65-1133">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="d1e65-1134">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1134">Count</span></span> | <span data-ttu-id="d1e65-1135">3</span><span class="sxs-lookup"><span data-stu-id="d1e65-1135">3</span></span>                       |



 

## <a name="propertytagycbcrsubsampling"></a><span data-ttu-id="d1e65-1136">Propertytagycbcrsubsampling</span><span class="sxs-lookup"><span data-stu-id="d1e65-1136">PropertyTagYCbCrSubsampling</span></span>

<span data-ttu-id="d1e65-1137">Das Stichproben Verhältnis von Chrominanz-Komponenten im Verhältnis zur Leuchtkraft Komponente.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1137">Sampling ratio of chrominance components in relation to the luminance component.</span></span>



| <span data-ttu-id="d1e65-1138">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1138">Property info</span></span> | <span data-ttu-id="d1e65-1139">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1139">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="d1e65-1140">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1140">Tag</span></span>   | <span data-ttu-id="d1e65-1141">0x0212</span><span class="sxs-lookup"><span data-stu-id="d1e65-1141">0x0212</span></span>               |
| <span data-ttu-id="d1e65-1142">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1142">Type</span></span>  | <span data-ttu-id="d1e65-1143">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-1143">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="d1e65-1144">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1144">Count</span></span> | <span data-ttu-id="d1e65-1145">2</span><span class="sxs-lookup"><span data-stu-id="d1e65-1145">2</span></span>                    |



 

## <a name="propertytagycbcrpositioning"></a><span data-ttu-id="d1e65-1146">Propertytagycbcrpositionierung</span><span class="sxs-lookup"><span data-stu-id="d1e65-1146">PropertyTagYCbCrPositioning</span></span>

<span data-ttu-id="d1e65-1147">Die Position von Chrominanz-Komponenten im Verhältnis zur Leuchtkraft Komponente.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1147">Position of chrominance components in relation to the luminance component.</span></span>



| <span data-ttu-id="d1e65-1148">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1148">Property info</span></span> | <span data-ttu-id="d1e65-1149">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1149">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="d1e65-1150">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1150">Tag</span></span>   | <span data-ttu-id="d1e65-1151">0x0213</span><span class="sxs-lookup"><span data-stu-id="d1e65-1151">0x0213</span></span>               |
| <span data-ttu-id="d1e65-1152">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1152">Type</span></span>  | <span data-ttu-id="d1e65-1153">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-1153">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="d1e65-1154">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1154">Count</span></span> | <span data-ttu-id="d1e65-1155">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-1155">1</span></span>                    |



 

## <a name="propertytagrefblackwhite"></a><span data-ttu-id="d1e65-1156">Propertytagref BlackWhite</span><span class="sxs-lookup"><span data-stu-id="d1e65-1156">PropertyTagREFBlackWhite</span></span>

<span data-ttu-id="d1e65-1157">Verweis-Schwarzpunkt Wert und Referenz-weiß Punkt Wert.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1157">Reference black point value and reference white point value.</span></span>



| <span data-ttu-id="d1e65-1158">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1158">Property info</span></span> | <span data-ttu-id="d1e65-1159">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1159">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="d1e65-1160">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1160">Tag</span></span>   | <span data-ttu-id="d1e65-1161">0x0214</span><span class="sxs-lookup"><span data-stu-id="d1e65-1161">0x0214</span></span>                  |
| <span data-ttu-id="d1e65-1162">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1162">Type</span></span>  | <span data-ttu-id="d1e65-1163">Propertytagtyperational</span><span class="sxs-lookup"><span data-stu-id="d1e65-1163">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="d1e65-1164">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1164">Count</span></span> | <span data-ttu-id="d1e65-1165">6</span><span class="sxs-lookup"><span data-stu-id="d1e65-1165">6</span></span>                       |



 

## <a name="propertytaggamma"></a><span data-ttu-id="d1e65-1166">Propertytaggamma</span><span class="sxs-lookup"><span data-stu-id="d1e65-1166">PropertyTagGamma</span></span>

<span data-ttu-id="d1e65-1167">An das Bild angefügter Gamma Wert.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1167">Gamma value attached to the image.</span></span> <span data-ttu-id="d1e65-1168">Der Gamma Wert wird als eine rationale Zahl ( **Long of Long**) mit einem Zähler von 100000 gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1168">The gamma value is stored as a rational number (pair of **long**) with a numerator of 100000.</span></span> <span data-ttu-id="d1e65-1169">Beispielsweise wird der Gamma Wert 2,2 als Paar (100000, 45455) gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1169">For example, a gamma value of 2.2 is stored as the pair (100000, 45455).</span></span>



| <span data-ttu-id="d1e65-1170">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1170">Property info</span></span> | <span data-ttu-id="d1e65-1171">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1171">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="d1e65-1172">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1172">Tag</span></span>   | <span data-ttu-id="d1e65-1173">0x0301</span><span class="sxs-lookup"><span data-stu-id="d1e65-1173">0x0301</span></span>                  |
| <span data-ttu-id="d1e65-1174">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1174">Type</span></span>  | <span data-ttu-id="d1e65-1175">Propertytagtyperational</span><span class="sxs-lookup"><span data-stu-id="d1e65-1175">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="d1e65-1176">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1176">Count</span></span> | <span data-ttu-id="d1e65-1177">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-1177">1</span></span>                       |



 

## <a name="propertytagiccprofiledescriptor"></a><span data-ttu-id="d1e65-1178">Propertytagiccprofiledescriptor</span><span class="sxs-lookup"><span data-stu-id="d1e65-1178">PropertyTagICCProfileDescriptor</span></span>

<span data-ttu-id="d1e65-1179">Mit NULL beendete Zeichenfolge, die ein ICC-Profil identifiziert.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1179">Null-terminated character string that identifies an ICC profile.</span></span>



| <span data-ttu-id="d1e65-1180">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1180">Property info</span></span> | <span data-ttu-id="d1e65-1181">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1181">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="d1e65-1182">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1182">Tag</span></span>   | <span data-ttu-id="d1e65-1183">0x0302</span><span class="sxs-lookup"><span data-stu-id="d1e65-1183">0x0302</span></span>                                             |
| <span data-ttu-id="d1e65-1184">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1184">Type</span></span>  | <span data-ttu-id="d1e65-1185">Propertytagtybäuercii</span><span class="sxs-lookup"><span data-stu-id="d1e65-1185">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="d1e65-1186">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1186">Count</span></span> | <span data-ttu-id="d1e65-1187">Länge der Zeichenfolge einschließlich des NULL-Terminator</span><span class="sxs-lookup"><span data-stu-id="d1e65-1187">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagsrgbrenderingintent"></a><span data-ttu-id="d1e65-1188">Propertytagsrgbrenderingintent</span><span class="sxs-lookup"><span data-stu-id="d1e65-1188">PropertyTagSRGBRenderingIntent</span></span>

<span data-ttu-id="d1e65-1189">Gibt an, wie das Bild gemäß der Definition durch das International Color Consortium (ICC) angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1189">How the image should be displayed as defined by the International Color Consortium (ICC).</span></span> <span data-ttu-id="d1e65-1190">Wenn ein GDI+-  [**Bild**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) Objekt erstellt wird, wobei der *useembeddebug* -Parameter auf **true** festgelegt ist, wird das Bild von GDI+ entsprechend der angegebenen renderingabsicht gerendert.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1190">If a GDI+  [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object is constructed with the *useEmbeddedColorManagement* parameter set to **TRUE**, then GDI+ renders the image according to the specified rendering intent.</span></span> <span data-ttu-id="d1e65-1191">Die Absicht kann auf "perperell", eine relative farbige Metrik, Sättigung oder absolute farbige Metrik festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1191">The intent can be set to perceptual, relative colorimetric, saturation, or absolute colorimetric.</span></span>

-   <span data-ttu-id="d1e65-1192">Die für Fotos geeignete perzeptive Absicht bietet eine gute Anpassung an die Anzeigegeräte Palette auf Kosten der farmetriegenauigkeit.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1192">Perceptual intent, which is suitable for photographs, gives good adaptation to the display device gamut at the expense of colorimetric accuracy.</span></span>
-   <span data-ttu-id="d1e65-1193">Die relative Farbe für farbige Metriken eignet sich für Bilder (z. b. Logos), für die eine Farbdarstellung in Bezug auf den weißen Punkt des Anzeige Geräts erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1193">Relative colorimetric intent is suitable for images (for example, logos) that require color appearance matching that is relative to the display device white point.</span></span>
-   <span data-ttu-id="d1e65-1194">Die Absicht, die sich für Diagramme und Diagramme eignet, behält die Sättigung auf Kosten von Hue und Helligkeit bei.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1194">Saturation intent, which is suitable for charts and graphs, preserves saturation at the expense of hue and lightness.</span></span>
-   <span data-ttu-id="d1e65-1195">Die absolute farbige Metrik-Absicht eignet sich für Beweise (Vorschau der für ein anderes Anzeigegerät vorgesehenen Bilder), die eine Beibehaltung absoluter farmetriedaten erfordern.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1195">Absolute colorimetric intent is suitable for proofs (previews of images destined for a different display device) that require preservation of absolute colorimetry.</span></span>



<span data-ttu-id="d1e65-1196">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1196">Tag</span></span>

<span data-ttu-id="d1e65-1197">0x0303</span><span class="sxs-lookup"><span data-stu-id="d1e65-1197">0x0303</span></span>

<span data-ttu-id="d1e65-1198">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1198">Type</span></span>

<span data-ttu-id="d1e65-1199">BYTE</span><span class="sxs-lookup"><span data-stu-id="d1e65-1199">BYTE</span></span>

<span data-ttu-id="d1e65-1200">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1200">Count</span></span>

<span data-ttu-id="d1e65-1201">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-1201">1</span></span>

<span data-ttu-id="d1e65-1202">0-perzeptive 1-relative farbige Metrik 2-Sättigung 3-absolute farbige Metrik</span><span class="sxs-lookup"><span data-stu-id="d1e65-1202">0 - perceptual 1 - relative colorimetric 2 - saturation 3 - absolute colorimetric</span></span>



 

## <a name="propertytagimagetitle"></a><span data-ttu-id="d1e65-1203">Propertytagimagetitle</span><span class="sxs-lookup"><span data-stu-id="d1e65-1203">PropertyTagImageTitle</span></span>

<span data-ttu-id="d1e65-1204">Mit NULL beendete Zeichenfolge, die den Titel des Bilds angibt.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1204">Null-terminated character string that specifies the title of the image.</span></span>



| <span data-ttu-id="d1e65-1205">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1205">Property info</span></span> | <span data-ttu-id="d1e65-1206">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1206">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="d1e65-1207">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1207">Tag</span></span>   | <span data-ttu-id="d1e65-1208">0x0320</span><span class="sxs-lookup"><span data-stu-id="d1e65-1208">0x0320</span></span>                                             |
| <span data-ttu-id="d1e65-1209">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1209">Type</span></span>  | <span data-ttu-id="d1e65-1210">Propertytagtybäuercii</span><span class="sxs-lookup"><span data-stu-id="d1e65-1210">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="d1e65-1211">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1211">Count</span></span> | <span data-ttu-id="d1e65-1212">Länge der Zeichenfolge einschließlich des NULL-Terminator</span><span class="sxs-lookup"><span data-stu-id="d1e65-1212">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagresolutionxunit"></a><span data-ttu-id="d1e65-1213">Propertytagresolutionxunit</span><span class="sxs-lookup"><span data-stu-id="d1e65-1213">PropertyTagResolutionXUnit</span></span>

<span data-ttu-id="d1e65-1214">Einheiten, in denen die horizontale Auflösung angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1214">Units in which to display horizontal resolution.</span></span>



<span data-ttu-id="d1e65-1215">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1215">Tag</span></span>

<span data-ttu-id="d1e65-1216">0x5001</span><span class="sxs-lookup"><span data-stu-id="d1e65-1216">0x5001</span></span>

<span data-ttu-id="d1e65-1217">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1217">Type</span></span>

<span data-ttu-id="d1e65-1218">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-1218">PropertyTagTypeShort</span></span>

<span data-ttu-id="d1e65-1219">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1219">Count</span></span>

<span data-ttu-id="d1e65-1220">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-1220">1</span></span>

<span data-ttu-id="d1e65-1221">1-Pixel pro Zoll, 2 Pixel pro Zentimeter</span><span class="sxs-lookup"><span data-stu-id="d1e65-1221">1 - pixels per inch 2 - pixels per centimeter</span></span>



 

## <a name="propertytagresolutionyunit"></a><span data-ttu-id="d1e65-1222">Propertytagresolutionyunit</span><span class="sxs-lookup"><span data-stu-id="d1e65-1222">PropertyTagResolutionYUnit</span></span>

<span data-ttu-id="d1e65-1223">Einheiten, in denen die vertikale Auflösung angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1223">Units in which to display vertical resolution.</span></span>



<span data-ttu-id="d1e65-1224">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1224">Tag</span></span>

<span data-ttu-id="d1e65-1225">0x5002</span><span class="sxs-lookup"><span data-stu-id="d1e65-1225">0x5002</span></span>

<span data-ttu-id="d1e65-1226">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1226">Type</span></span>

<span data-ttu-id="d1e65-1227">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-1227">PropertyTagTypeShort</span></span>

<span data-ttu-id="d1e65-1228">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1228">Count</span></span>

<span data-ttu-id="d1e65-1229">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-1229">1</span></span>

<span data-ttu-id="d1e65-1230">1-Pixel pro Zoll, 2 Pixel pro Zentimeter</span><span class="sxs-lookup"><span data-stu-id="d1e65-1230">1 - pixels per inch 2 - pixels per centimeter</span></span>



 

## <a name="propertytagresolutionxlengthunit"></a><span data-ttu-id="d1e65-1231">Propertytagresolutionxlängen Unit</span><span class="sxs-lookup"><span data-stu-id="d1e65-1231">PropertyTagResolutionXLengthUnit</span></span>

<span data-ttu-id="d1e65-1232">Einheiten, in denen die Bildbreite angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1232">Units in which to display the image width.</span></span>



<span data-ttu-id="d1e65-1233">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1233">Tag</span></span>

<span data-ttu-id="d1e65-1234">0x5003</span><span class="sxs-lookup"><span data-stu-id="d1e65-1234">0x5003</span></span>

<span data-ttu-id="d1e65-1235">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1235">Type</span></span>

<span data-ttu-id="d1e65-1236">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-1236">PropertyTagTypeShort</span></span>

<span data-ttu-id="d1e65-1237">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1237">Count</span></span>

<span data-ttu-id="d1e65-1238">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-1238">1</span></span>

<span data-ttu-id="d1e65-1239">1-Zoll-2-Zentimeter 3-Punkte 4-Picas 5-Spalten</span><span class="sxs-lookup"><span data-stu-id="d1e65-1239">1 - inches 2 - centimeters 3 - points 4 - picas 5 - columns</span></span>



 

## <a name="propertytagresolutionylengthunit"></a><span data-ttu-id="d1e65-1240">Propertytagresolutionyverlängert-Einheit</span><span class="sxs-lookup"><span data-stu-id="d1e65-1240">PropertyTagResolutionYLengthUnit</span></span>

<span data-ttu-id="d1e65-1241">Einheiten, in denen die Bildhöhe angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1241">Units in which to display the image height.</span></span>



<span data-ttu-id="d1e65-1242">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1242">Tag</span></span>

<span data-ttu-id="d1e65-1243">0x5004</span><span class="sxs-lookup"><span data-stu-id="d1e65-1243">0x5004</span></span>

<span data-ttu-id="d1e65-1244">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1244">Type</span></span>

<span data-ttu-id="d1e65-1245">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-1245">PropertyTagTypeShort</span></span>

<span data-ttu-id="d1e65-1246">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1246">Count</span></span>

<span data-ttu-id="d1e65-1247">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-1247">1</span></span>

<span data-ttu-id="d1e65-1248">1-Zoll-2-Zentimeter 3-Punkte 4-Picas 5-Spalten</span><span class="sxs-lookup"><span data-stu-id="d1e65-1248">1 - inches 2 - centimeters 3 - points 4 - picas 5 - columns</span></span>



 

## <a name="propertytagprintflags"></a><span data-ttu-id="d1e65-1249">Propertytagprintflags</span><span class="sxs-lookup"><span data-stu-id="d1e65-1249">PropertyTagPrintFlags</span></span>

<span data-ttu-id="d1e65-1250">Sequenz von booleschen 1-Byte-Werten, die Druckoptionen angeben.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1250">Sequence of one-byte Boolean values that specify printing options.</span></span>



| <span data-ttu-id="d1e65-1251">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1251">Property info</span></span> | <span data-ttu-id="d1e65-1252">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1252">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="d1e65-1253">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1253">Tag</span></span>   | <span data-ttu-id="d1e65-1254">0x5005</span><span class="sxs-lookup"><span data-stu-id="d1e65-1254">0x5005</span></span>               |
| <span data-ttu-id="d1e65-1255">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1255">Type</span></span>  | <span data-ttu-id="d1e65-1256">Propertytagtybäuercii</span><span class="sxs-lookup"><span data-stu-id="d1e65-1256">PropertyTagTypeASCII</span></span> |
| <span data-ttu-id="d1e65-1257">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1257">Count</span></span> | <span data-ttu-id="d1e65-1258">Anzahl von Flags</span><span class="sxs-lookup"><span data-stu-id="d1e65-1258">Number of flags</span></span>      |



 

## <a name="propertytagprintflagsversion"></a><span data-ttu-id="d1e65-1259">Propertytagprintflagsversion</span><span class="sxs-lookup"><span data-stu-id="d1e65-1259">PropertyTagPrintFlagsVersion</span></span>

<span data-ttu-id="d1e65-1260">Versionsflags-Version.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1260">Print flags version.</span></span>



| <span data-ttu-id="d1e65-1261">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1261">Property info</span></span> | <span data-ttu-id="d1e65-1262">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1262">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="d1e65-1263">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1263">Tag</span></span>   | <span data-ttu-id="d1e65-1264">0x5006</span><span class="sxs-lookup"><span data-stu-id="d1e65-1264">0x5006</span></span>               |
| <span data-ttu-id="d1e65-1265">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1265">Type</span></span>  | <span data-ttu-id="d1e65-1266">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-1266">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="d1e65-1267">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1267">Count</span></span> | <span data-ttu-id="d1e65-1268">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-1268">1</span></span>                    |



 

## <a name="propertytagprintflagscrop"></a><span data-ttu-id="d1e65-1269">Propertytagprintflagscrop</span><span class="sxs-lookup"><span data-stu-id="d1e65-1269">PropertyTagPrintFlagsCrop</span></span>

<span data-ttu-id="d1e65-1270">Druckflags Zentrierungs Markierungen zentrieren.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1270">Print flags center crop marks.</span></span>



| <span data-ttu-id="d1e65-1271">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1271">Property info</span></span> | <span data-ttu-id="d1e65-1272">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1272">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="d1e65-1273">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1273">Tag</span></span>   | <span data-ttu-id="d1e65-1274">0x5007</span><span class="sxs-lookup"><span data-stu-id="d1e65-1274">0x5007</span></span>              |
| <span data-ttu-id="d1e65-1275">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1275">Type</span></span>  | <span data-ttu-id="d1e65-1276">Propertytagtypebyte</span><span class="sxs-lookup"><span data-stu-id="d1e65-1276">PropertyTagTypeByte</span></span> |
| <span data-ttu-id="d1e65-1277">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1277">Count</span></span> | <span data-ttu-id="d1e65-1278">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-1278">1</span></span>                   |



 

## <a name="propertytagprintflagsbleedwidth"></a><span data-ttu-id="d1e65-1279">Propertytagprintflagsbleedwidth</span><span class="sxs-lookup"><span data-stu-id="d1e65-1279">PropertyTagPrintFlagsBleedWidth</span></span>

<span data-ttu-id="d1e65-1280">Die ausgabenflags haben die Breite</span><span class="sxs-lookup"><span data-stu-id="d1e65-1280">Print flags bleed width.</span></span>



| <span data-ttu-id="d1e65-1281">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1281">Property info</span></span> | <span data-ttu-id="d1e65-1282">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1282">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="d1e65-1283">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1283">Tag</span></span>   | <span data-ttu-id="d1e65-1284">0x5008</span><span class="sxs-lookup"><span data-stu-id="d1e65-1284">0x5008</span></span>              |
| <span data-ttu-id="d1e65-1285">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1285">Type</span></span>  | <span data-ttu-id="d1e65-1286">Propertytagtypelong</span><span class="sxs-lookup"><span data-stu-id="d1e65-1286">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="d1e65-1287">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1287">Count</span></span> | <span data-ttu-id="d1e65-1288">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-1288">1</span></span>                   |



 

## <a name="propertytagprintflagsbleedwidthscale"></a><span data-ttu-id="d1e65-1289">Propertytagprintflagsbleedwidthscale</span><span class="sxs-lookup"><span data-stu-id="d1e65-1289">PropertyTagPrintFlagsBleedWidthScale</span></span>

<span data-ttu-id="d1e65-1290">Die ausdruckflags haben die Breite skaliert.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1290">Print flags bleed width scale.</span></span>



| <span data-ttu-id="d1e65-1291">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1291">Property info</span></span> | <span data-ttu-id="d1e65-1292">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1292">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="d1e65-1293">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1293">Tag</span></span>   | <span data-ttu-id="d1e65-1294">0x5009</span><span class="sxs-lookup"><span data-stu-id="d1e65-1294">0x5009</span></span>               |
| <span data-ttu-id="d1e65-1295">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1295">Type</span></span>  | <span data-ttu-id="d1e65-1296">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-1296">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="d1e65-1297">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1297">Count</span></span> | <span data-ttu-id="d1e65-1298">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-1298">1</span></span>                    |



 

## <a name="propertytaghalftonelpi"></a><span data-ttu-id="d1e65-1299">Propertytaghalftonelpi</span><span class="sxs-lookup"><span data-stu-id="d1e65-1299">PropertyTagHalftoneLPI</span></span>

<span data-ttu-id="d1e65-1300">Bildschirm Frequenz von frei Hand Eingaben in Zeilen pro Zoll.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1300">Ink's screen frequency, in lines per inch.</span></span>



| <span data-ttu-id="d1e65-1301">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1301">Property info</span></span> | <span data-ttu-id="d1e65-1302">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1302">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="d1e65-1303">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1303">Tag</span></span>   | <span data-ttu-id="d1e65-1304">0x500a</span><span class="sxs-lookup"><span data-stu-id="d1e65-1304">0x500A</span></span>                  |
| <span data-ttu-id="d1e65-1305">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1305">Type</span></span>  | <span data-ttu-id="d1e65-1306">Propertytagtyperational</span><span class="sxs-lookup"><span data-stu-id="d1e65-1306">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="d1e65-1307">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1307">Count</span></span> | <span data-ttu-id="d1e65-1308">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-1308">1</span></span>                       |



 

## <a name="propertytaghalftonelpiunit"></a><span data-ttu-id="d1e65-1309">Propertytaghalftonelpiunit</span><span class="sxs-lookup"><span data-stu-id="d1e65-1309">PropertyTagHalftoneLPIUnit</span></span>

<span data-ttu-id="d1e65-1310">Einheiten für die Bildschirm Frequenz.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1310">Units for the screen frequency.</span></span>



<span data-ttu-id="d1e65-1311">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1311">Tag</span></span>

<span data-ttu-id="d1e65-1312">0x500.000 b</span><span class="sxs-lookup"><span data-stu-id="d1e65-1312">0x500B</span></span>

<span data-ttu-id="d1e65-1313">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1313">Type</span></span>

<span data-ttu-id="d1e65-1314">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-1314">PropertyTagTypeShort</span></span>

<span data-ttu-id="d1e65-1315">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1315">Count</span></span>

<span data-ttu-id="d1e65-1316">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-1316">1</span></span>

<span data-ttu-id="d1e65-1317">1-Zeilen pro Zoll 2-Zeilen pro Zentimeter</span><span class="sxs-lookup"><span data-stu-id="d1e65-1317">1 - lines per inch 2 - lines per centimeter</span></span>



 

## <a name="propertytaghalftonedegree"></a><span data-ttu-id="d1e65-1318">Propertytaghalftonedegree</span><span class="sxs-lookup"><span data-stu-id="d1e65-1318">PropertyTagHalftoneDegree</span></span>

<span data-ttu-id="d1e65-1319">Der Winkel für den Bildschirm.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1319">Angle for screen.</span></span>



| <span data-ttu-id="d1e65-1320">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1320">Property info</span></span> | <span data-ttu-id="d1e65-1321">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1321">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="d1e65-1322">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1322">Tag</span></span>   | <span data-ttu-id="d1e65-1323">0x500.000</span><span class="sxs-lookup"><span data-stu-id="d1e65-1323">0x500C</span></span>                  |
| <span data-ttu-id="d1e65-1324">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1324">Type</span></span>  | <span data-ttu-id="d1e65-1325">Propertytagtyperational</span><span class="sxs-lookup"><span data-stu-id="d1e65-1325">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="d1e65-1326">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1326">Count</span></span> | <span data-ttu-id="d1e65-1327">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-1327">1</span></span>                       |



 

## <a name="propertytaghalftoneshape"></a><span data-ttu-id="d1e65-1328">Propertytaghalftoneshape</span><span class="sxs-lookup"><span data-stu-id="d1e65-1328">PropertyTagHalftoneShape</span></span>

<span data-ttu-id="d1e65-1329">Die Form der halbftone-Punkte.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1329">Shape of the halftone dots.</span></span>



<span data-ttu-id="d1e65-1330">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1330">Tag</span></span>

<span data-ttu-id="d1e65-1331">0x500.000 d</span><span class="sxs-lookup"><span data-stu-id="d1e65-1331">0x500D</span></span>

<span data-ttu-id="d1e65-1332">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1332">Type</span></span>

<span data-ttu-id="d1e65-1333">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-1333">PropertyTagTypeShort</span></span>

<span data-ttu-id="d1e65-1334">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1334">Count</span></span>

<span data-ttu-id="d1e65-1335">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-1335">1</span></span>

<span data-ttu-id="d1e65-1336">0-Runde 1-Ellipse 2-Zeile 3-quadratisches 4-Kreuz 6-Diamant</span><span class="sxs-lookup"><span data-stu-id="d1e65-1336">0 - round 1 - ellipse 2 - line 3 - square 4 - cross 6 - diamond</span></span>



 

## <a name="propertytaghalftonemisc"></a><span data-ttu-id="d1e65-1337">Propertytaghalftonemisc</span><span class="sxs-lookup"><span data-stu-id="d1e65-1337">PropertyTagHalftoneMisc</span></span>

<span data-ttu-id="d1e65-1338">Sonstige Informationen.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1338">Miscellaneous halftone information.</span></span>



| <span data-ttu-id="d1e65-1339">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1339">Property info</span></span> | <span data-ttu-id="d1e65-1340">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1340">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="d1e65-1341">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1341">Tag</span></span>   | <span data-ttu-id="d1e65-1342">0x500e</span><span class="sxs-lookup"><span data-stu-id="d1e65-1342">0x500E</span></span>              |
| <span data-ttu-id="d1e65-1343">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1343">Type</span></span>  | <span data-ttu-id="d1e65-1344">Propertytagtypelong</span><span class="sxs-lookup"><span data-stu-id="d1e65-1344">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="d1e65-1345">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1345">Count</span></span> | <span data-ttu-id="d1e65-1346">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-1346">1</span></span>                   |



 

## <a name="propertytaghalftonescreen"></a><span data-ttu-id="d1e65-1347">Propertytaghalftonescreen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1347">PropertyTagHalftoneScreen</span></span>

<span data-ttu-id="d1e65-1348">Boolescher Wert, der angibt, ob die Standard Bildschirme des Druckers verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1348">Boolean value that specifies whether to use the printer's default screens.</span></span>



<span data-ttu-id="d1e65-1349">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1349">Tag</span></span>

<span data-ttu-id="d1e65-1350">0x500.000 f</span><span class="sxs-lookup"><span data-stu-id="d1e65-1350">0x500F</span></span>

<span data-ttu-id="d1e65-1351">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1351">Type</span></span>

<span data-ttu-id="d1e65-1352">Propertytagtypebyte</span><span class="sxs-lookup"><span data-stu-id="d1e65-1352">PropertyTagTypeByte</span></span>

<span data-ttu-id="d1e65-1353">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1353">Count</span></span>

<span data-ttu-id="d1e65-1354">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-1354">1</span></span>

<span data-ttu-id="d1e65-1355">1. verwenden Sie die Standard Bildschirme von Druckern 2.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1355">1 - use printer's default screens 2 - other</span></span>



 

## <a name="propertytagjpegquality"></a><span data-ttu-id="d1e65-1356">Propertytagjpgquality</span><span class="sxs-lookup"><span data-stu-id="d1e65-1356">PropertyTagJPEGQuality</span></span>

<span data-ttu-id="d1e65-1357">Privates Tag, das vom Adobe Photoshop-Format verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1357">Private tag used by the Adobe Photoshop format.</span></span> <span data-ttu-id="d1e65-1358">Nicht für die öffentliche Verwendung.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1358">Not for public use.</span></span>



| <span data-ttu-id="d1e65-1359">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1359">Property info</span></span> | <span data-ttu-id="d1e65-1360">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1360">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="d1e65-1361">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1361">Tag</span></span>   | <span data-ttu-id="d1e65-1362">0x5010</span><span class="sxs-lookup"><span data-stu-id="d1e65-1362">0x5010</span></span>               |
| <span data-ttu-id="d1e65-1363">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1363">Type</span></span>  | <span data-ttu-id="d1e65-1364">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-1364">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="d1e65-1365">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1365">Count</span></span> | <span data-ttu-id="d1e65-1366">Any</span><span class="sxs-lookup"><span data-stu-id="d1e65-1366">Any</span></span>                  |



 

## <a name="propertytaggridsize"></a><span data-ttu-id="d1e65-1367">Propertytaggridsize</span><span class="sxs-lookup"><span data-stu-id="d1e65-1367">PropertyTagGridSize</span></span>

<span data-ttu-id="d1e65-1368">Informations Block zu Raster und Handbüchern.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1368">Block of information about grids and guides.</span></span>



| <span data-ttu-id="d1e65-1369">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1369">Property info</span></span> | <span data-ttu-id="d1e65-1370">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1370">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="d1e65-1371">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1371">Tag</span></span>   | <span data-ttu-id="d1e65-1372">0x5011</span><span class="sxs-lookup"><span data-stu-id="d1e65-1372">0x5011</span></span>                   |
| <span data-ttu-id="d1e65-1373">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1373">Type</span></span>  | <span data-ttu-id="d1e65-1374">Propertytagtypeundefiniert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1374">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="d1e65-1375">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1375">Count</span></span> | <span data-ttu-id="d1e65-1376">Any</span><span class="sxs-lookup"><span data-stu-id="d1e65-1376">Any</span></span>                      |



 

## <a name="propertytagthumbnailformat"></a><span data-ttu-id="d1e65-1377">Propertytagthumbnailformat</span><span class="sxs-lookup"><span data-stu-id="d1e65-1377">PropertyTagThumbnailFormat</span></span>

<span data-ttu-id="d1e65-1378">Das Format des Miniatur Bilds.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1378">Format of the thumbnail image.</span></span>



<span data-ttu-id="d1e65-1379">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1379">Tag</span></span>

<span data-ttu-id="d1e65-1380">0x5012</span><span class="sxs-lookup"><span data-stu-id="d1e65-1380">0x5012</span></span>

<span data-ttu-id="d1e65-1381">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1381">Type</span></span>

<span data-ttu-id="d1e65-1382">Propertytagtypelong</span><span class="sxs-lookup"><span data-stu-id="d1e65-1382">PropertyTagTypeLong</span></span>

<span data-ttu-id="d1e65-1383">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1383">Count</span></span>

<span data-ttu-id="d1e65-1384">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-1384">1</span></span>

<span data-ttu-id="d1e65-1385">0-Rohdaten RGB 1-JPEG</span><span class="sxs-lookup"><span data-stu-id="d1e65-1385">0 - raw RGB 1 - JPEG</span></span>



 

## <a name="propertytagthumbnailwidth"></a><span data-ttu-id="d1e65-1386">Propertytagthumbnailwidth</span><span class="sxs-lookup"><span data-stu-id="d1e65-1386">PropertyTagThumbnailWidth</span></span>

<span data-ttu-id="d1e65-1387">Breite des Miniatur Bilds in Pixel.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1387">Width, in pixels, of the thumbnail image.</span></span>



| <span data-ttu-id="d1e65-1388">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1388">Property info</span></span> | <span data-ttu-id="d1e65-1389">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1389">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="d1e65-1390">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1390">Tag</span></span>   | <span data-ttu-id="d1e65-1391">0x5013</span><span class="sxs-lookup"><span data-stu-id="d1e65-1391">0x5013</span></span>              |
| <span data-ttu-id="d1e65-1392">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1392">Type</span></span>  | <span data-ttu-id="d1e65-1393">Propertytagtypelong</span><span class="sxs-lookup"><span data-stu-id="d1e65-1393">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="d1e65-1394">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1394">Count</span></span> | <span data-ttu-id="d1e65-1395">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-1395">1</span></span>                   |



 

## <a name="propertytagthumbnailheight"></a><span data-ttu-id="d1e65-1396">Propertytagthumbnailheight</span><span class="sxs-lookup"><span data-stu-id="d1e65-1396">PropertyTagThumbnailHeight</span></span>

<span data-ttu-id="d1e65-1397">Höhe des Miniatur Bilds in Pixel.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1397">Height, in pixels, of the thumbnail image.</span></span>



| <span data-ttu-id="d1e65-1398">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1398">Property info</span></span> | <span data-ttu-id="d1e65-1399">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1399">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="d1e65-1400">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1400">Tag</span></span>   | <span data-ttu-id="d1e65-1401">0x5014</span><span class="sxs-lookup"><span data-stu-id="d1e65-1401">0x5014</span></span>              |
| <span data-ttu-id="d1e65-1402">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1402">Type</span></span>  | <span data-ttu-id="d1e65-1403">Propertytagtypelong</span><span class="sxs-lookup"><span data-stu-id="d1e65-1403">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="d1e65-1404">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1404">Count</span></span> | <span data-ttu-id="d1e65-1405">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-1405">1</span></span>                   |



 

## <a name="propertytagthumbnailcolordepth"></a><span data-ttu-id="d1e65-1406">Propertytagthumbnailcolortiefe</span><span class="sxs-lookup"><span data-stu-id="d1e65-1406">PropertyTagThumbnailColorDepth</span></span>

<span data-ttu-id="d1e65-1407">Bits pro Pixel (BPP) für das Miniaturbild.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1407">bits per pixel (BPP) for the thumbnail image.</span></span>



| <span data-ttu-id="d1e65-1408">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1408">Property info</span></span> | <span data-ttu-id="d1e65-1409">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1409">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="d1e65-1410">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1410">Tag</span></span>   | <span data-ttu-id="d1e65-1411">0x5015</span><span class="sxs-lookup"><span data-stu-id="d1e65-1411">0x5015</span></span>               |
| <span data-ttu-id="d1e65-1412">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1412">Type</span></span>  | <span data-ttu-id="d1e65-1413">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-1413">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="d1e65-1414">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1414">Count</span></span> | <span data-ttu-id="d1e65-1415">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-1415">1</span></span>                    |



 

## <a name="propertytagthumbnailplanes"></a><span data-ttu-id="d1e65-1416">Propertytagthumbnailplane</span><span class="sxs-lookup"><span data-stu-id="d1e65-1416">PropertyTagThumbnailPlanes</span></span>

<span data-ttu-id="d1e65-1417">Anzahl von Farbebenen für das Miniaturbild.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1417">Number of color planes for the thumbnail image.</span></span>



| <span data-ttu-id="d1e65-1418">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1418">Property info</span></span> | <span data-ttu-id="d1e65-1419">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1419">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="d1e65-1420">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1420">Tag</span></span>   | <span data-ttu-id="d1e65-1421">0x5016</span><span class="sxs-lookup"><span data-stu-id="d1e65-1421">0x5016</span></span>               |
| <span data-ttu-id="d1e65-1422">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1422">Type</span></span>  | <span data-ttu-id="d1e65-1423">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-1423">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="d1e65-1424">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1424">Count</span></span> | <span data-ttu-id="d1e65-1425">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-1425">1</span></span>                    |



 

## <a name="propertytagthumbnailrawbytes"></a><span data-ttu-id="d1e65-1426">Propertytagthumbnailrawbytes</span><span class="sxs-lookup"><span data-stu-id="d1e65-1426">PropertyTagThumbnailRawBytes</span></span>

<span data-ttu-id="d1e65-1427">Byte Offset zwischen Zeilen von Pixeldaten.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1427">Byte offset between rows of pixel data.</span></span>



| <span data-ttu-id="d1e65-1428">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1428">Property info</span></span> | <span data-ttu-id="d1e65-1429">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1429">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="d1e65-1430">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1430">Tag</span></span>   | <span data-ttu-id="d1e65-1431">0x5017</span><span class="sxs-lookup"><span data-stu-id="d1e65-1431">0x5017</span></span>              |
| <span data-ttu-id="d1e65-1432">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1432">Type</span></span>  | <span data-ttu-id="d1e65-1433">Propertytagtypelong</span><span class="sxs-lookup"><span data-stu-id="d1e65-1433">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="d1e65-1434">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1434">Count</span></span> | <span data-ttu-id="d1e65-1435">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-1435">1</span></span>                   |



 

## <a name="propertytagthumbnailsize"></a><span data-ttu-id="d1e65-1436">Propertytagthumbnailsize</span><span class="sxs-lookup"><span data-stu-id="d1e65-1436">PropertyTagThumbnailSize</span></span>

<span data-ttu-id="d1e65-1437">Gesamtgröße (in Bytes) des Miniatur Bilds.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1437">Total size, in bytes, of the thumbnail image.</span></span>



| <span data-ttu-id="d1e65-1438">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1438">Property info</span></span> | <span data-ttu-id="d1e65-1439">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1439">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="d1e65-1440">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1440">Tag</span></span>   | <span data-ttu-id="d1e65-1441">0x5018</span><span class="sxs-lookup"><span data-stu-id="d1e65-1441">0x5018</span></span>              |
| <span data-ttu-id="d1e65-1442">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1442">Type</span></span>  | <span data-ttu-id="d1e65-1443">Propertytagtypelong</span><span class="sxs-lookup"><span data-stu-id="d1e65-1443">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="d1e65-1444">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1444">Count</span></span> | <span data-ttu-id="d1e65-1445">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-1445">1</span></span>                   |



 

## <a name="propertytagthumbnailcompressedsize"></a><span data-ttu-id="d1e65-1446">Propertytagthumbnailcompressedsize</span><span class="sxs-lookup"><span data-stu-id="d1e65-1446">PropertyTagThumbnailCompressedSize</span></span>

<span data-ttu-id="d1e65-1447">Komprimierte Größe (in Bytes) des Miniatur Bilds.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1447">Compressed size, in bytes, of the thumbnail image.</span></span>



| <span data-ttu-id="d1e65-1448">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1448">Property info</span></span> | <span data-ttu-id="d1e65-1449">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1449">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="d1e65-1450">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1450">Tag</span></span>   | <span data-ttu-id="d1e65-1451">0x5019</span><span class="sxs-lookup"><span data-stu-id="d1e65-1451">0x5019</span></span>              |
| <span data-ttu-id="d1e65-1452">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1452">Type</span></span>  | <span data-ttu-id="d1e65-1453">Propertytagtypelong</span><span class="sxs-lookup"><span data-stu-id="d1e65-1453">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="d1e65-1454">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1454">Count</span></span> | <span data-ttu-id="d1e65-1455">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-1455">1</span></span>                   |



 

## <a name="propertytagcolortransferfunction"></a><span data-ttu-id="d1e65-1456">Propertytagcolortransferfunction</span><span class="sxs-lookup"><span data-stu-id="d1e65-1456">PropertyTagColorTransferFunction</span></span>

<span data-ttu-id="d1e65-1457">Tabelle mit Werten, die Farb Übertragungsfunktionen angeben.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1457">Table of values that specify color transfer functions.</span></span>



| <span data-ttu-id="d1e65-1458">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1458">Property info</span></span> | <span data-ttu-id="d1e65-1459">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1459">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="d1e65-1460">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1460">Tag</span></span>   | <span data-ttu-id="d1e65-1461">0x501a</span><span class="sxs-lookup"><span data-stu-id="d1e65-1461">0x501A</span></span>                   |
| <span data-ttu-id="d1e65-1462">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1462">Type</span></span>  | <span data-ttu-id="d1e65-1463">Propertytagtypeundefiniert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1463">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="d1e65-1464">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1464">Count</span></span> | <span data-ttu-id="d1e65-1465">Any</span><span class="sxs-lookup"><span data-stu-id="d1e65-1465">Any</span></span>                      |



 

## <a name="propertytagthumbnaildata"></a><span data-ttu-id="d1e65-1466">Propertytagthumbnaildata</span><span class="sxs-lookup"><span data-stu-id="d1e65-1466">PropertyTagThumbnailData</span></span>

<span data-ttu-id="d1e65-1467">Unformatierte Miniatur Ansichts Bits im JPEG-oder RGB-Format</span><span class="sxs-lookup"><span data-stu-id="d1e65-1467">Raw thumbnail bits in JPEG or RGB format.</span></span> <span data-ttu-id="d1e65-1468">Hängt von propertytagthumbnailformat ab.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1468">Depends on PropertyTagThumbnailFormat.</span></span>



| <span data-ttu-id="d1e65-1469">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1469">Property info</span></span> | <span data-ttu-id="d1e65-1470">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1470">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="d1e65-1471">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1471">Tag</span></span>   | <span data-ttu-id="d1e65-1472">0x501b</span><span class="sxs-lookup"><span data-stu-id="d1e65-1472">0x501B</span></span>              |
| <span data-ttu-id="d1e65-1473">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1473">Type</span></span>  | <span data-ttu-id="d1e65-1474">Propertytagtypebyte</span><span class="sxs-lookup"><span data-stu-id="d1e65-1474">PropertyTagTypeByte</span></span> |
| <span data-ttu-id="d1e65-1475">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1475">Count</span></span> | <span data-ttu-id="d1e65-1476">Variable</span><span class="sxs-lookup"><span data-stu-id="d1e65-1476">Variable</span></span>            |



 

## <a name="propertytagthumbnailimagewidth"></a><span data-ttu-id="d1e65-1477">PropertyTagThumbnailImageWidth</span><span class="sxs-lookup"><span data-stu-id="d1e65-1477">PropertyTagThumbnailImageWidth</span></span>

<span data-ttu-id="d1e65-1478">Anzahl der Pixel pro Zeile in der Miniaturansicht.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1478">Number of pixels per row in the thumbnail image.</span></span>



| <span data-ttu-id="d1e65-1479">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1479">Property info</span></span> | <span data-ttu-id="d1e65-1480">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1480">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="d1e65-1481">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1481">Tag</span></span>   | <span data-ttu-id="d1e65-1482">0x5020</span><span class="sxs-lookup"><span data-stu-id="d1e65-1482">0x5020</span></span>                                      |
| <span data-ttu-id="d1e65-1483">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1483">Type</span></span>  | <span data-ttu-id="d1e65-1484">Propertytagtypeshort oder propertytagtypelong</span><span class="sxs-lookup"><span data-stu-id="d1e65-1484">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="d1e65-1485">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1485">Count</span></span> | <span data-ttu-id="d1e65-1486">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-1486">1</span></span>                                           |



 

## <a name="propertytagthumbnailimageheight"></a><span data-ttu-id="d1e65-1487">Propertytagthumbnailimageheight</span><span class="sxs-lookup"><span data-stu-id="d1e65-1487">PropertyTagThumbnailImageHeight</span></span>

<span data-ttu-id="d1e65-1488">Anzahl der Pixel Zeilen in der Miniaturansicht.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1488">Number of pixel rows in the thumbnail image.</span></span>



| <span data-ttu-id="d1e65-1489">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1489">Property info</span></span> | <span data-ttu-id="d1e65-1490">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1490">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="d1e65-1491">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1491">Tag</span></span>   | <span data-ttu-id="d1e65-1492">0x5021</span><span class="sxs-lookup"><span data-stu-id="d1e65-1492">0x5021</span></span>                                      |
| <span data-ttu-id="d1e65-1493">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1493">Type</span></span>  | <span data-ttu-id="d1e65-1494">Propertytagtypeshort oder propertytagtypelong</span><span class="sxs-lookup"><span data-stu-id="d1e65-1494">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="d1e65-1495">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1495">Count</span></span> | <span data-ttu-id="d1e65-1496">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-1496">1</span></span>                                           |



 

## <a name="propertytagthumbnailbitspersample"></a><span data-ttu-id="d1e65-1497">Propertytagthumbnailbitspersample</span><span class="sxs-lookup"><span data-stu-id="d1e65-1497">PropertyTagThumbnailBitsPerSample</span></span>

<span data-ttu-id="d1e65-1498">Anzahl der Bits pro Farbkomponente im Miniaturbild.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1498">Number of bits per color component in the thumbnail image.</span></span> <span data-ttu-id="d1e65-1499">Siehe auch [propertytagthumbnailsamplesperpixel](#propertytagthumbnailsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="d1e65-1499">See also [PropertyTagThumbnailSamplesPerPixel](#propertytagthumbnailsamplesperpixel).</span></span>



| <span data-ttu-id="d1e65-1500">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1500">Property info</span></span> | <span data-ttu-id="d1e65-1501">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1501">Value</span></span> |
|-------|-----------------------------------------------------------------|
| <span data-ttu-id="d1e65-1502">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1502">Tag</span></span>   | <span data-ttu-id="d1e65-1503">0x5022</span><span class="sxs-lookup"><span data-stu-id="d1e65-1503">0x5022</span></span>                                                          |
| <span data-ttu-id="d1e65-1504">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1504">Type</span></span>  | <span data-ttu-id="d1e65-1505">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-1505">PropertyTagTypeShort</span></span>                                            |
| <span data-ttu-id="d1e65-1506">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1506">Count</span></span> | <span data-ttu-id="d1e65-1507">Anzahl der Stichproben (Komponenten) pro Pixel im Miniaturbild</span><span class="sxs-lookup"><span data-stu-id="d1e65-1507">Number of samples (components) per pixel in the thumbnail image</span></span> |



 

## <a name="propertytagthumbnailcompression"></a><span data-ttu-id="d1e65-1508">Propertytagthumbnailcompression</span><span class="sxs-lookup"><span data-stu-id="d1e65-1508">PropertyTagThumbnailCompression</span></span>

<span data-ttu-id="d1e65-1509">Komprimierungs Schema für Miniaturbild Daten.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1509">Compression scheme used for thumbnail image data.</span></span>



| <span data-ttu-id="d1e65-1510">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1510">Property info</span></span> | <span data-ttu-id="d1e65-1511">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1511">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="d1e65-1512">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1512">Tag</span></span>   | <span data-ttu-id="d1e65-1513">0x5023</span><span class="sxs-lookup"><span data-stu-id="d1e65-1513">0x5023</span></span>               |
| <span data-ttu-id="d1e65-1514">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1514">Type</span></span>  | <span data-ttu-id="d1e65-1515">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-1515">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="d1e65-1516">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1516">Count</span></span> | <span data-ttu-id="d1e65-1517">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-1517">1</span></span>                    |



 

## <a name="propertytagthumbnailphotometricinterp"></a><span data-ttu-id="d1e65-1518">Propertytagthumbnailphotomezcinterp</span><span class="sxs-lookup"><span data-stu-id="d1e65-1518">PropertyTagThumbnailPhotometricInterp</span></span>

<span data-ttu-id="d1e65-1519">Wie Miniatur Ansichts Pixeldaten interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1519">How thumbnail pixel data will be interpreted.</span></span>



| <span data-ttu-id="d1e65-1520">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1520">Property info</span></span> | <span data-ttu-id="d1e65-1521">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1521">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="d1e65-1522">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1522">Tag</span></span>   | <span data-ttu-id="d1e65-1523">0x5024</span><span class="sxs-lookup"><span data-stu-id="d1e65-1523">0x5024</span></span>               |
| <span data-ttu-id="d1e65-1524">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1524">Type</span></span>  | <span data-ttu-id="d1e65-1525">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-1525">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="d1e65-1526">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1526">Count</span></span> | <span data-ttu-id="d1e65-1527">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-1527">1</span></span>                    |



 

## <a name="propertytagthumbnailimagedescription"></a><span data-ttu-id="d1e65-1528">Propertytagthumbnailimagedescription</span><span class="sxs-lookup"><span data-stu-id="d1e65-1528">PropertyTagThumbnailImageDescription</span></span>

<span data-ttu-id="d1e65-1529">Mit NULL beendete Zeichenfolge, die den Titel des Bilds angibt.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1529">Null-terminated character string that specifies the title of the image.</span></span>



| <span data-ttu-id="d1e65-1530">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1530">Property info</span></span> | <span data-ttu-id="d1e65-1531">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1531">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="d1e65-1532">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1532">Tag</span></span>   | <span data-ttu-id="d1e65-1533">0x5025</span><span class="sxs-lookup"><span data-stu-id="d1e65-1533">0x5025</span></span>                                             |
| <span data-ttu-id="d1e65-1534">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1534">Type</span></span>  | <span data-ttu-id="d1e65-1535">Propertytagtybäuercii</span><span class="sxs-lookup"><span data-stu-id="d1e65-1535">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="d1e65-1536">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1536">Count</span></span> | <span data-ttu-id="d1e65-1537">Länge der Zeichenfolge einschließlich des NULL-Terminator</span><span class="sxs-lookup"><span data-stu-id="d1e65-1537">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagthumbnailequipmake"></a><span data-ttu-id="d1e65-1538">Propertytagthumbnailequipmake</span><span class="sxs-lookup"><span data-stu-id="d1e65-1538">PropertyTagThumbnailEquipMake</span></span>

<span data-ttu-id="d1e65-1539">Mit NULL endende Zeichenfolge, die den Hersteller der Ausrüstung angibt, die zum Aufzeichnen des Miniatur Bilds verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1539">Null-terminated character string that specifies the manufacturer of the equipment used to record the thumbnail image.</span></span>



| <span data-ttu-id="d1e65-1540">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1540">Property info</span></span> | <span data-ttu-id="d1e65-1541">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1541">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="d1e65-1542">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1542">Tag</span></span>   | <span data-ttu-id="d1e65-1543">0x5026</span><span class="sxs-lookup"><span data-stu-id="d1e65-1543">0x5026</span></span>                                             |
| <span data-ttu-id="d1e65-1544">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1544">Type</span></span>  | <span data-ttu-id="d1e65-1545">Propertytagtybäuercii</span><span class="sxs-lookup"><span data-stu-id="d1e65-1545">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="d1e65-1546">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1546">Count</span></span> | <span data-ttu-id="d1e65-1547">Länge der Zeichenfolge einschließlich des NULL-Terminator</span><span class="sxs-lookup"><span data-stu-id="d1e65-1547">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagthumbnailequipmodel"></a><span data-ttu-id="d1e65-1548">Propertytagthumbnailequipmodel</span><span class="sxs-lookup"><span data-stu-id="d1e65-1548">PropertyTagThumbnailEquipModel</span></span>

<span data-ttu-id="d1e65-1549">Mit NULL endende Zeichenfolge, die den Modellnamen oder die Modellnummer der Ausrüstung angibt, die zum Aufzeichnen des Miniatur Bilds verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1549">Null-terminated character string that specifies the model name or model number of the equipment used to record the thumbnail image.</span></span>



| <span data-ttu-id="d1e65-1550">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1550">Property info</span></span> | <span data-ttu-id="d1e65-1551">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1551">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="d1e65-1552">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1552">Tag</span></span>   | <span data-ttu-id="d1e65-1553">0x5027</span><span class="sxs-lookup"><span data-stu-id="d1e65-1553">0x5027</span></span>                                             |
| <span data-ttu-id="d1e65-1554">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1554">Type</span></span>  | <span data-ttu-id="d1e65-1555">Propertytagtybäuercii</span><span class="sxs-lookup"><span data-stu-id="d1e65-1555">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="d1e65-1556">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1556">Count</span></span> | <span data-ttu-id="d1e65-1557">Länge der Zeichenfolge einschließlich des NULL-Terminator</span><span class="sxs-lookup"><span data-stu-id="d1e65-1557">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagthumbnailstripoffsets"></a><span data-ttu-id="d1e65-1558">Propertytagthumbnailstripoffsets</span><span class="sxs-lookup"><span data-stu-id="d1e65-1558">PropertyTagThumbnailStripOffsets</span></span>

<span data-ttu-id="d1e65-1559">Der Byte Offset dieses Streifens für jeden Strip des Miniatur Bilds.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1559">For each strip in the thumbnail image, the byte offset of that strip.</span></span> <span data-ttu-id="d1e65-1560">Siehe auch [propertytagthumbnailrowsperstrip](#propertytagthumbnailrowsperstrip) und [propertytagthumbnailstripbytescount](#propertytagthumbnailstripbytescount).</span><span class="sxs-lookup"><span data-stu-id="d1e65-1560">See also [PropertyTagThumbnailRowsPerStrip](#propertytagthumbnailrowsperstrip) and [PropertyTagThumbnailStripBytesCount](#propertytagthumbnailstripbytescount).</span></span>



| <span data-ttu-id="d1e65-1561">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1561">Property info</span></span> | <span data-ttu-id="d1e65-1562">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1562">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="d1e65-1563">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1563">Tag</span></span>   | <span data-ttu-id="d1e65-1564">0x5028</span><span class="sxs-lookup"><span data-stu-id="d1e65-1564">0x5028</span></span>                                      |
| <span data-ttu-id="d1e65-1565">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1565">Type</span></span>  | <span data-ttu-id="d1e65-1566">Propertytagtypeshort oder propertytagtypelong</span><span class="sxs-lookup"><span data-stu-id="d1e65-1566">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="d1e65-1567">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1567">Count</span></span> | <span data-ttu-id="d1e65-1568">Anzahl von Bändern</span><span class="sxs-lookup"><span data-stu-id="d1e65-1568">Number of strips</span></span>                            |



 

## <a name="propertytagthumbnailorientation"></a><span data-ttu-id="d1e65-1569">Propertytagthumbnailorientation</span><span class="sxs-lookup"><span data-stu-id="d1e65-1569">PropertyTagThumbnailOrientation</span></span>

<span data-ttu-id="d1e65-1570">Ausrichtung von Miniaturbildern in Bezug auf Zeilen und Spalten.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1570">Thumbnail image orientation in terms of rows and columns.</span></span> <span data-ttu-id="d1e65-1571">Siehe auch [propertytagorientation](#propertytagorientation).</span><span class="sxs-lookup"><span data-stu-id="d1e65-1571">See also [PropertyTagOrientation](#propertytagorientation).</span></span>



| <span data-ttu-id="d1e65-1572">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1572">Property info</span></span> | <span data-ttu-id="d1e65-1573">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1573">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="d1e65-1574">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1574">Tag</span></span>   | <span data-ttu-id="d1e65-1575">0x5029</span><span class="sxs-lookup"><span data-stu-id="d1e65-1575">0x5029</span></span>               |
| <span data-ttu-id="d1e65-1576">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1576">Type</span></span>  | <span data-ttu-id="d1e65-1577">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-1577">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="d1e65-1578">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1578">Count</span></span> | <span data-ttu-id="d1e65-1579">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-1579">1</span></span>                    |



 

## <a name="propertytagthumbnailsamplesperpixel"></a><span data-ttu-id="d1e65-1580">Propertytagthumbnailsamplesperpixel</span><span class="sxs-lookup"><span data-stu-id="d1e65-1580">PropertyTagThumbnailSamplesPerPixel</span></span>

<span data-ttu-id="d1e65-1581">Anzahl der Farbkomponenten pro Pixel in der Miniaturansicht.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1581">Number of color components per pixel in the thumbnail image.</span></span>



| <span data-ttu-id="d1e65-1582">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1582">Property info</span></span> | <span data-ttu-id="d1e65-1583">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1583">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="d1e65-1584">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1584">Tag</span></span>   | <span data-ttu-id="d1e65-1585">0x502a</span><span class="sxs-lookup"><span data-stu-id="d1e65-1585">0x502A</span></span>               |
| <span data-ttu-id="d1e65-1586">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1586">Type</span></span>  | <span data-ttu-id="d1e65-1587">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-1587">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="d1e65-1588">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1588">Count</span></span> | <span data-ttu-id="d1e65-1589">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-1589">1</span></span>                    |



 

## <a name="propertytagthumbnailrowsperstrip"></a><span data-ttu-id="d1e65-1590">Propertytagthumbnailrowsperstrip</span><span class="sxs-lookup"><span data-stu-id="d1e65-1590">PropertyTagThumbnailRowsPerStrip</span></span>

<span data-ttu-id="d1e65-1591">Anzahl der Zeilen pro Strip in der Miniaturansicht.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1591">Number of rows per strip in the thumbnail image.</span></span> <span data-ttu-id="d1e65-1592">Siehe auch [propertytagthumbnailstripbytescount](#propertytagthumbnailstripbytescount) und [propertytagthumbnailstripoffsets](#propertytagthumbnailstripoffsets).</span><span class="sxs-lookup"><span data-stu-id="d1e65-1592">See also [PropertyTagThumbnailStripBytesCount](#propertytagthumbnailstripbytescount) and [PropertyTagThumbnailStripOffsets](#propertytagthumbnailstripoffsets).</span></span>



| <span data-ttu-id="d1e65-1593">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1593">Property info</span></span> | <span data-ttu-id="d1e65-1594">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1594">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="d1e65-1595">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1595">Tag</span></span>   | <span data-ttu-id="d1e65-1596">0x502b</span><span class="sxs-lookup"><span data-stu-id="d1e65-1596">0x502B</span></span>                                      |
| <span data-ttu-id="d1e65-1597">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1597">Type</span></span>  | <span data-ttu-id="d1e65-1598">Propertytagtypeshort oder propertytagtypelong</span><span class="sxs-lookup"><span data-stu-id="d1e65-1598">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="d1e65-1599">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1599">Count</span></span> | <span data-ttu-id="d1e65-1600">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-1600">1</span></span>                                           |



 

## <a name="propertytagthumbnailstripbytescount"></a><span data-ttu-id="d1e65-1601">Propertytagthumbnailstripbytescount</span><span class="sxs-lookup"><span data-stu-id="d1e65-1601">PropertyTagThumbnailStripBytesCount</span></span>

<span data-ttu-id="d1e65-1602">Die Gesamtanzahl der Bytes in diesem Strip für jeden Miniaturbild Streifen.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1602">For each thumbnail image strip, the total number of bytes in that strip.</span></span>



| <span data-ttu-id="d1e65-1603">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1603">Property info</span></span> | <span data-ttu-id="d1e65-1604">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1604">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="d1e65-1605">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1605">Tag</span></span>   | <span data-ttu-id="d1e65-1606">0x502c</span><span class="sxs-lookup"><span data-stu-id="d1e65-1606">0x502C</span></span>                                      |
| <span data-ttu-id="d1e65-1607">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1607">Type</span></span>  | <span data-ttu-id="d1e65-1608">Propertytagtypeshort oder propertytagtypelong</span><span class="sxs-lookup"><span data-stu-id="d1e65-1608">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="d1e65-1609">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1609">Count</span></span> | <span data-ttu-id="d1e65-1610">Anzahl der Bänder im Miniaturbild</span><span class="sxs-lookup"><span data-stu-id="d1e65-1610">Number of strips in the thumbnail image</span></span>     |



 

## <a name="propertytagthumbnailresolutionx"></a><span data-ttu-id="d1e65-1611">Propertytagthumbnailresolutionx</span><span class="sxs-lookup"><span data-stu-id="d1e65-1611">PropertyTagThumbnailResolutionX</span></span>

<span data-ttu-id="d1e65-1612">Auflösung von Miniaturansichten in der breiten Richtung.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1612">Thumbnail resolution in the width direction.</span></span> <span data-ttu-id="d1e65-1613">Die Auflösungs Einheit wird in [propertytagthumbnailresolutionunit](#propertytagthumbnailresolutionunit)angegeben.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1613">The resolution unit is given in [PropertyTagThumbnailResolutionUnit](#propertytagthumbnailresolutionunit).</span></span>



| <span data-ttu-id="d1e65-1614">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1614">Property info</span></span> | <span data-ttu-id="d1e65-1615">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1615">Value</span></span> |
|-----|--------|
| <span data-ttu-id="d1e65-1616">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1616">Tag</span></span> | <span data-ttu-id="d1e65-1617">0x502d</span><span class="sxs-lookup"><span data-stu-id="d1e65-1617">0x502D</span></span> |



 

## <a name="propertytagthumbnailresolutiony"></a><span data-ttu-id="d1e65-1618">Propertytagthumbnailresolutiony</span><span class="sxs-lookup"><span data-stu-id="d1e65-1618">PropertyTagThumbnailResolutionY</span></span>

<span data-ttu-id="d1e65-1619">Miniatur Ansichts Auflösung in der höhenrichtung.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1619">Thumbnail resolution in the height direction.</span></span> <span data-ttu-id="d1e65-1620">Die Auflösungs Einheit wird in [propertytagthumbnailresolutionunit](#propertytagthumbnailresolutionunit)angegeben.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1620">The resolution unit is given in [PropertyTagThumbnailResolutionUnit](#propertytagthumbnailresolutionunit).</span></span>



| <span data-ttu-id="d1e65-1621">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1621">Property info</span></span> | <span data-ttu-id="d1e65-1622">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1622">Value</span></span> |
|-----|--------|
| <span data-ttu-id="d1e65-1623">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1623">Tag</span></span> | <span data-ttu-id="d1e65-1624">0x502e</span><span class="sxs-lookup"><span data-stu-id="d1e65-1624">0x502E</span></span> |



 

## <a name="propertytagthumbnailplanarconfig"></a><span data-ttu-id="d1e65-1625">Propertytagthumbnailplanarconfig</span><span class="sxs-lookup"><span data-stu-id="d1e65-1625">PropertyTagThumbnailPlanarConfig</span></span>

<span data-ttu-id="d1e65-1626">Gibt an, ob Pixel Komponenten in der Miniaturansicht im segmentierten oder planaren Format aufgezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1626">Whether pixel components in the thumbnail image are recorded in chunky or planar format.</span></span> <span data-ttu-id="d1e65-1627">Siehe auch [propertytagplanarconfig](#propertytagplanarconfig).</span><span class="sxs-lookup"><span data-stu-id="d1e65-1627">See also [PropertyTagPlanarConfig](#propertytagplanarconfig).</span></span>



| <span data-ttu-id="d1e65-1628">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1628">Property info</span></span> | <span data-ttu-id="d1e65-1629">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1629">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="d1e65-1630">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1630">Tag</span></span>   | <span data-ttu-id="d1e65-1631">0x502f</span><span class="sxs-lookup"><span data-stu-id="d1e65-1631">0x502F</span></span>               |
| <span data-ttu-id="d1e65-1632">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1632">Type</span></span>  | <span data-ttu-id="d1e65-1633">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-1633">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="d1e65-1634">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1634">Count</span></span> | <span data-ttu-id="d1e65-1635">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-1635">1</span></span>                    |



 

## <a name="propertytagthumbnailresolutionunit"></a><span data-ttu-id="d1e65-1636">Propertytagthumbnailresolutionunit</span><span class="sxs-lookup"><span data-stu-id="d1e65-1636">PropertyTagThumbnailResolutionUnit</span></span>

<span data-ttu-id="d1e65-1637">Maßeinheit für die horizontale Auflösung und die vertikale Auflösung des Miniatur Bilds.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1637">Unit of measure for the horizontal resolution and the vertical resolution of the thumbnail image.</span></span> <span data-ttu-id="d1e65-1638">Siehe auch [propertytagresolutionunit](#propertytagresolutionunit).</span><span class="sxs-lookup"><span data-stu-id="d1e65-1638">See also [PropertyTagResolutionUnit](#propertytagresolutionunit).</span></span>



| <span data-ttu-id="d1e65-1639">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1639">Property info</span></span> | <span data-ttu-id="d1e65-1640">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1640">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="d1e65-1641">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1641">Tag</span></span>   | <span data-ttu-id="d1e65-1642">0x5030</span><span class="sxs-lookup"><span data-stu-id="d1e65-1642">0x5030</span></span>               |
| <span data-ttu-id="d1e65-1643">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1643">Type</span></span>  | <span data-ttu-id="d1e65-1644">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-1644">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="d1e65-1645">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1645">Count</span></span> | <span data-ttu-id="d1e65-1646">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-1646">1</span></span>                    |



 

## <a name="propertytagthumbnailtransferfunction"></a><span data-ttu-id="d1e65-1647">Propertytagthumbnailtransferfunction</span><span class="sxs-lookup"><span data-stu-id="d1e65-1647">PropertyTagThumbnailTransferFunction</span></span>

<span data-ttu-id="d1e65-1648">Tabellen, die Übertragungsfunktionen für das Miniaturbild angeben.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1648">Tables that specify transfer functions for the thumbnail image.</span></span> <span data-ttu-id="d1e65-1649">Siehe auch [propertytagtransferfunction](#propertytagtransferfunction).</span><span class="sxs-lookup"><span data-stu-id="d1e65-1649">See also [PropertyTagTransferFunction](#propertytagtransferfunction).</span></span>



| <span data-ttu-id="d1e65-1650">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1650">Property info</span></span> | <span data-ttu-id="d1e65-1651">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1651">Value</span></span> |
|-------|------------------------------------------------------|
| <span data-ttu-id="d1e65-1652">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1652">Tag</span></span>   | <span data-ttu-id="d1e65-1653">0x5031</span><span class="sxs-lookup"><span data-stu-id="d1e65-1653">0x5031</span></span>                                               |
| <span data-ttu-id="d1e65-1654">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1654">Type</span></span>  | <span data-ttu-id="d1e65-1655">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-1655">PropertyTagTypeShort</span></span>                                 |
| <span data-ttu-id="d1e65-1656">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1656">Count</span></span> | <span data-ttu-id="d1e65-1657">Die Gesamtanzahl der für die Tabellen erforderlichen 16-Bit-Wörter.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1657">Total number of 16-bit words required for the tables</span></span> |



 

## <a name="propertytagthumbnailsoftwareused"></a><span data-ttu-id="d1e65-1658">Propertytagthumbnailsoftwareused</span><span class="sxs-lookup"><span data-stu-id="d1e65-1658">PropertyTagThumbnailSoftwareUsed</span></span>

<span data-ttu-id="d1e65-1659">Mit NULL endende Zeichenfolge, die den Namen und die Version der Software oder Firmware des Geräts angibt, das zum Generieren des Miniatur Bilds verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1659">Null-terminated character string that specifies the name and version of the software or firmware of the device used to generate the thumbnail image.</span></span>



| <span data-ttu-id="d1e65-1660">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1660">Property info</span></span> | <span data-ttu-id="d1e65-1661">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1661">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="d1e65-1662">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1662">Tag</span></span>   | <span data-ttu-id="d1e65-1663">0x5032</span><span class="sxs-lookup"><span data-stu-id="d1e65-1663">0x5032</span></span>                                             |
| <span data-ttu-id="d1e65-1664">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1664">Type</span></span>  | <span data-ttu-id="d1e65-1665">Propertytagtybäuercii</span><span class="sxs-lookup"><span data-stu-id="d1e65-1665">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="d1e65-1666">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1666">Count</span></span> | <span data-ttu-id="d1e65-1667">Länge der Zeichenfolge einschließlich des NULL-Terminator</span><span class="sxs-lookup"><span data-stu-id="d1e65-1667">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagthumbnaildatetime"></a><span data-ttu-id="d1e65-1668">Propertytagthumbnaildatetime</span><span class="sxs-lookup"><span data-stu-id="d1e65-1668">PropertyTagThumbnailDateTime</span></span>

<span data-ttu-id="d1e65-1669">Datum und Uhrzeit der Erstellung des Miniatur Bilds.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1669">Date and time the thumbnail image was created.</span></span> <span data-ttu-id="d1e65-1670">Siehe auch [propertytagdatetime](#propertytagdatetime).</span><span class="sxs-lookup"><span data-stu-id="d1e65-1670">See also [PropertyTagDateTime](#propertytagdatetime).</span></span>



| <span data-ttu-id="d1e65-1671">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1671">Property info</span></span> | <span data-ttu-id="d1e65-1672">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1672">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="d1e65-1673">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1673">Tag</span></span>   | <span data-ttu-id="d1e65-1674">0x5033</span><span class="sxs-lookup"><span data-stu-id="d1e65-1674">0x5033</span></span>               |
| <span data-ttu-id="d1e65-1675">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1675">Type</span></span>  | <span data-ttu-id="d1e65-1676">Propertytagtybäuercii</span><span class="sxs-lookup"><span data-stu-id="d1e65-1676">PropertyTagTypeASCII</span></span> |
| <span data-ttu-id="d1e65-1677">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1677">Count</span></span> | <span data-ttu-id="d1e65-1678">20</span><span class="sxs-lookup"><span data-stu-id="d1e65-1678">20</span></span>                   |



 

## <a name="propertytagthumbnailartist"></a><span data-ttu-id="d1e65-1679">Propertytagthumbnailartist</span><span class="sxs-lookup"><span data-stu-id="d1e65-1679">PropertyTagThumbnailArtist</span></span>

<span data-ttu-id="d1e65-1680">Mit NULL beendete Zeichenfolge, die den Namen der Person angibt, die das Miniaturbild erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1680">Null-terminated character string that specifies the name of the person who created the thumbnail image.</span></span>



| <span data-ttu-id="d1e65-1681">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1681">Property info</span></span> | <span data-ttu-id="d1e65-1682">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1682">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="d1e65-1683">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1683">Tag</span></span>   | <span data-ttu-id="d1e65-1684">0x5034</span><span class="sxs-lookup"><span data-stu-id="d1e65-1684">0x5034</span></span>                                             |
| <span data-ttu-id="d1e65-1685">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1685">Type</span></span>  | <span data-ttu-id="d1e65-1686">Propertytagtybäuercii</span><span class="sxs-lookup"><span data-stu-id="d1e65-1686">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="d1e65-1687">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1687">Count</span></span> | <span data-ttu-id="d1e65-1688">Länge der Zeichenfolge einschließlich des NULL-Terminator</span><span class="sxs-lookup"><span data-stu-id="d1e65-1688">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagthumbnailwhitepoint"></a><span data-ttu-id="d1e65-1689">Propertytagthumbnailwhitepoint</span><span class="sxs-lookup"><span data-stu-id="d1e65-1689">PropertyTagThumbnailWhitePoint</span></span>

<span data-ttu-id="d1e65-1690">Die Chromatizität des weißen Punkts des Miniatur Bilds.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1690">Chromaticity of the white point of the thumbnail image.</span></span> <span data-ttu-id="d1e65-1691">Siehe auch [propertytagwhitepoint](#propertytagwhitepoint).</span><span class="sxs-lookup"><span data-stu-id="d1e65-1691">See also [PropertyTagWhitePoint](#propertytagwhitepoint).</span></span>



| <span data-ttu-id="d1e65-1692">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1692">Property info</span></span> | <span data-ttu-id="d1e65-1693">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1693">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="d1e65-1694">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1694">Tag</span></span>   | <span data-ttu-id="d1e65-1695">0x5035 angezeigt</span><span class="sxs-lookup"><span data-stu-id="d1e65-1695">0x5035</span></span>                  |
| <span data-ttu-id="d1e65-1696">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1696">Type</span></span>  | <span data-ttu-id="d1e65-1697">Propertytagtyperational</span><span class="sxs-lookup"><span data-stu-id="d1e65-1697">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="d1e65-1698">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1698">Count</span></span> | <span data-ttu-id="d1e65-1699">2</span><span class="sxs-lookup"><span data-stu-id="d1e65-1699">2</span></span>                       |



 

## <a name="propertytagthumbnailprimarychromaticities"></a><span data-ttu-id="d1e65-1700">Propertytagthumbnailprimarychromaticities</span><span class="sxs-lookup"><span data-stu-id="d1e65-1700">PropertyTagThumbnailPrimaryChromaticities</span></span>

<span data-ttu-id="d1e65-1701">Für jede der drei Primärfarben im Miniatur Ansichts Bild die Chromatizität dieser Farbe.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1701">For each of the three primary colors in the thumbnail image, the chromaticity of that color.</span></span> <span data-ttu-id="d1e65-1702">Siehe auch [propertytagprimarychromaticities](#propertytagprimarychromaticities).</span><span class="sxs-lookup"><span data-stu-id="d1e65-1702">See also [PropertyTagPrimaryChromaticities](#propertytagprimarychromaticities).</span></span>



| <span data-ttu-id="d1e65-1703">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1703">Property info</span></span> | <span data-ttu-id="d1e65-1704">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1704">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="d1e65-1705">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1705">Tag</span></span>   | <span data-ttu-id="d1e65-1706">0x5036</span><span class="sxs-lookup"><span data-stu-id="d1e65-1706">0x5036</span></span>                  |
| <span data-ttu-id="d1e65-1707">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1707">Type</span></span>  | <span data-ttu-id="d1e65-1708">Propertytagtyperational</span><span class="sxs-lookup"><span data-stu-id="d1e65-1708">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="d1e65-1709">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1709">Count</span></span> | <span data-ttu-id="d1e65-1710">6</span><span class="sxs-lookup"><span data-stu-id="d1e65-1710">6</span></span>                       |



 

## <a name="propertytagthumbnailycbcrcoefficients"></a><span data-ttu-id="d1e65-1711">Propertytagthumbnailycbcrkoefficients</span><span class="sxs-lookup"><span data-stu-id="d1e65-1711">PropertyTagThumbnailYCbCrCoefficients</span></span>

<span data-ttu-id="d1e65-1712">Koeffizienten für die Transformation von RGB zu YCbCr-Daten für das Miniaturbild.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1712">Coefficients for transformation from RGB to YCbCr data for the thumbnail image.</span></span> <span data-ttu-id="d1e65-1713">Siehe auch [propertytagycbcrkoefficients](#propertytagycbcrcoefficients).</span><span class="sxs-lookup"><span data-stu-id="d1e65-1713">See also [PropertyTagYCbCrCoefficients](#propertytagycbcrcoefficients).</span></span>



| <span data-ttu-id="d1e65-1714">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1714">Property info</span></span> | <span data-ttu-id="d1e65-1715">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1715">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="d1e65-1716">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1716">Tag</span></span>   | <span data-ttu-id="d1e65-1717">0x5037</span><span class="sxs-lookup"><span data-stu-id="d1e65-1717">0x5037</span></span>                  |
| <span data-ttu-id="d1e65-1718">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1718">Type</span></span>  | <span data-ttu-id="d1e65-1719">Propertytagtyperational</span><span class="sxs-lookup"><span data-stu-id="d1e65-1719">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="d1e65-1720">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1720">Count</span></span> | <span data-ttu-id="d1e65-1721">3</span><span class="sxs-lookup"><span data-stu-id="d1e65-1721">3</span></span>                       |



 

## <a name="propertytagthumbnailycbcrsubsampling"></a><span data-ttu-id="d1e65-1722">Propertytagthumbnailycbcrsubsampling</span><span class="sxs-lookup"><span data-stu-id="d1e65-1722">PropertyTagThumbnailYCbCrSubsampling</span></span>

<span data-ttu-id="d1e65-1723">Das Stichproben Verhältnis von Chrominanz-Komponenten in Relation zur Leuchtkraft Komponente für das Miniaturbild.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1723">Sampling ratio of chrominance components in relation to the luminance component for the thumbnail image.</span></span> <span data-ttu-id="d1e65-1724">Siehe auch [propertytagycbcrsubsampling](#propertytagycbcrsubsampling).</span><span class="sxs-lookup"><span data-stu-id="d1e65-1724">See also [PropertyTagYCbCrSubsampling](#propertytagycbcrsubsampling).</span></span>



| <span data-ttu-id="d1e65-1725">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1725">Property info</span></span> | <span data-ttu-id="d1e65-1726">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1726">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="d1e65-1727">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1727">Tag</span></span>   | <span data-ttu-id="d1e65-1728">0x5038</span><span class="sxs-lookup"><span data-stu-id="d1e65-1728">0x5038</span></span>               |
| <span data-ttu-id="d1e65-1729">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1729">Type</span></span>  | <span data-ttu-id="d1e65-1730">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-1730">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="d1e65-1731">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1731">Count</span></span> | <span data-ttu-id="d1e65-1732">2</span><span class="sxs-lookup"><span data-stu-id="d1e65-1732">2</span></span>                    |



 

## <a name="propertytagthumbnailycbcrpositioning"></a><span data-ttu-id="d1e65-1733">Propertytagthumbnailycbcrpositionierung</span><span class="sxs-lookup"><span data-stu-id="d1e65-1733">PropertyTagThumbnailYCbCrPositioning</span></span>

<span data-ttu-id="d1e65-1734">Die Position von Chrominanz-Komponenten in Bezug auf die Leuchtkraft Komponente für das Miniaturbild.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1734">Position of chrominance components in relation to the luminance component for the thumbnail image.</span></span> <span data-ttu-id="d1e65-1735">Siehe auch [propertytagycbcrpositionierung](#propertytagycbcrpositioning).</span><span class="sxs-lookup"><span data-stu-id="d1e65-1735">See also [PropertyTagYCbCrPositioning](#propertytagycbcrpositioning).</span></span>



| <span data-ttu-id="d1e65-1736">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1736">Property info</span></span> | <span data-ttu-id="d1e65-1737">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1737">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="d1e65-1738">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1738">Tag</span></span>   | <span data-ttu-id="d1e65-1739">0x5039</span><span class="sxs-lookup"><span data-stu-id="d1e65-1739">0x5039</span></span>               |
| <span data-ttu-id="d1e65-1740">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1740">Type</span></span>  | <span data-ttu-id="d1e65-1741">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-1741">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="d1e65-1742">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1742">Count</span></span> | <span data-ttu-id="d1e65-1743">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-1743">1</span></span>                    |



 

## <a name="propertytagthumbnailrefblackwhite"></a><span data-ttu-id="d1e65-1744">Propertytagthumbnailref BlackWhite</span><span class="sxs-lookup"><span data-stu-id="d1e65-1744">PropertyTagThumbnailRefBlackWhite</span></span>

<span data-ttu-id="d1e65-1745">Verweis-Schwarzpunkt Wert und Referenz-weiß Punkt Wert für das Miniaturbild.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1745">Reference black point value and reference white point value for the thumbnail image.</span></span> <span data-ttu-id="d1e65-1746">Siehe auch [propertytagref BlackWhite](#propertytagrefblackwhite).</span><span class="sxs-lookup"><span data-stu-id="d1e65-1746">See also [PropertyTagREFBlackWhite](#propertytagrefblackwhite).</span></span>



| <span data-ttu-id="d1e65-1747">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1747">Property info</span></span> | <span data-ttu-id="d1e65-1748">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1748">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="d1e65-1749">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1749">Tag</span></span>   | <span data-ttu-id="d1e65-1750">0x503a</span><span class="sxs-lookup"><span data-stu-id="d1e65-1750">0x503A</span></span>                  |
| <span data-ttu-id="d1e65-1751">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1751">Type</span></span>  | <span data-ttu-id="d1e65-1752">Propertytagtyperational</span><span class="sxs-lookup"><span data-stu-id="d1e65-1752">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="d1e65-1753">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1753">Count</span></span> | <span data-ttu-id="d1e65-1754">6</span><span class="sxs-lookup"><span data-stu-id="d1e65-1754">6</span></span>                       |



 

## <a name="propertytagthumbnailcopyright"></a><span data-ttu-id="d1e65-1755">Propertytagthumbnailcopyright</span><span class="sxs-lookup"><span data-stu-id="d1e65-1755">PropertyTagThumbnailCopyRight</span></span>

<span data-ttu-id="d1e65-1756">Mit NULL beendete Zeichenfolge, die Copyright Informationen für das Miniaturbild enthält.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1756">Null-terminated character string that contains copyright information for the thumbnail image.</span></span>



| <span data-ttu-id="d1e65-1757">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1757">Property info</span></span> | <span data-ttu-id="d1e65-1758">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1758">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="d1e65-1759">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1759">Tag</span></span>   | <span data-ttu-id="d1e65-1760">0x503b</span><span class="sxs-lookup"><span data-stu-id="d1e65-1760">0x503B</span></span>                                             |
| <span data-ttu-id="d1e65-1761">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1761">Type</span></span>  | <span data-ttu-id="d1e65-1762">Propertytagtybäuercii</span><span class="sxs-lookup"><span data-stu-id="d1e65-1762">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="d1e65-1763">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1763">Count</span></span> | <span data-ttu-id="d1e65-1764">Länge der Zeichenfolge einschließlich des NULL-Terminator</span><span class="sxs-lookup"><span data-stu-id="d1e65-1764">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagluminancetable"></a><span data-ttu-id="d1e65-1765">Propertytagluminancetable</span><span class="sxs-lookup"><span data-stu-id="d1e65-1765">PropertyTagLuminanceTable</span></span>

<span data-ttu-id="d1e65-1766">Leuchtkraft Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1766">Luminance table.</span></span> <span data-ttu-id="d1e65-1767">Die Tabelle "Leuchtkraft" und die Tabelle Chrominanz werden verwendet, um die JPEG-Qualität zu steuern.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1767">The luminance table and the chrominance table are used to control JPEG quality.</span></span> <span data-ttu-id="d1e65-1768">Eine gültige Tabelle "Leuchtkraft" oder "Chrominanz" weist 64 Einträge vom Typ "propertytagtypeshort" auf.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1768">A valid luminance or chrominance table has 64 entries of type PropertyTagTypeShort.</span></span> <span data-ttu-id="d1e65-1769">Wenn ein Bild entweder eine "Leuchtkraft"-Tabelle oder eine Chrominanz-Tabelle enthält, muss es beide Tabellen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1769">If an image has either a luminance table or a chrominance table, then it must have both tables.</span></span>



| <span data-ttu-id="d1e65-1770">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1770">Property info</span></span> | <span data-ttu-id="d1e65-1771">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1771">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="d1e65-1772">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1772">Tag</span></span>   | <span data-ttu-id="d1e65-1773">0x5090</span><span class="sxs-lookup"><span data-stu-id="d1e65-1773">0x5090</span></span>               |
| <span data-ttu-id="d1e65-1774">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1774">Type</span></span>  | <span data-ttu-id="d1e65-1775">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-1775">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="d1e65-1776">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1776">Count</span></span> | <span data-ttu-id="d1e65-1777">64</span><span class="sxs-lookup"><span data-stu-id="d1e65-1777">64</span></span>                   |



 

## <a name="propertytagchrominancetable"></a><span data-ttu-id="d1e65-1778">Propertytagchrominancetable</span><span class="sxs-lookup"><span data-stu-id="d1e65-1778">PropertyTagChrominanceTable</span></span>

<span data-ttu-id="d1e65-1779">Chrominance-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1779">Chrominance table.</span></span> <span data-ttu-id="d1e65-1780">Die Tabelle "Leuchtkraft" und die Tabelle Chrominanz werden verwendet, um die JPEG-Qualität zu steuern.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1780">The luminance table and the chrominance table are used to control JPEG quality.</span></span> <span data-ttu-id="d1e65-1781">Eine gültige Tabelle "Leuchtkraft" oder "Chrominanz" weist 64 Einträge vom Typ "propertytagtypeshort" auf.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1781">A valid luminance or chrominance table has 64 entries of type PropertyTagTypeShort.</span></span> <span data-ttu-id="d1e65-1782">Wenn ein Bild entweder eine "Leuchtkraft"-Tabelle oder eine Chrominanz-Tabelle enthält, muss es beide Tabellen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1782">If an image has either a luminance table or a chrominance table, then it must have both tables.</span></span>



| <span data-ttu-id="d1e65-1783">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1783">Property info</span></span> | <span data-ttu-id="d1e65-1784">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1784">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="d1e65-1785">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1785">Tag</span></span>   | <span data-ttu-id="d1e65-1786">0x5091</span><span class="sxs-lookup"><span data-stu-id="d1e65-1786">0x5091</span></span>               |
| <span data-ttu-id="d1e65-1787">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1787">Type</span></span>  | <span data-ttu-id="d1e65-1788">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-1788">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="d1e65-1789">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1789">Count</span></span> | <span data-ttu-id="d1e65-1790">64</span><span class="sxs-lookup"><span data-stu-id="d1e65-1790">64</span></span>                   |



 

## <a name="propertytagframedelay"></a><span data-ttu-id="d1e65-1791">Propertytagframedelay</span><span class="sxs-lookup"><span data-stu-id="d1e65-1791">PropertyTagFrameDelay</span></span>

<span data-ttu-id="d1e65-1792">Zeitverzögerung (in Hundertstel Sekunden) zwischen zwei Frames in einem animierten GIF-Bild.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1792">Time delay, in hundredths of a second, between two frames in an animated GIF image.</span></span>



| <span data-ttu-id="d1e65-1793">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1793">Property info</span></span> | <span data-ttu-id="d1e65-1794">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1794">Value</span></span> |
|-------|-------------------------------|
| <span data-ttu-id="d1e65-1795">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1795">Tag</span></span>   | <span data-ttu-id="d1e65-1796">0x5100</span><span class="sxs-lookup"><span data-stu-id="d1e65-1796">0x5100</span></span>                        |
| <span data-ttu-id="d1e65-1797">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1797">Type</span></span>  | <span data-ttu-id="d1e65-1798">Propertytagtypelong</span><span class="sxs-lookup"><span data-stu-id="d1e65-1798">PropertyTagTypeLong</span></span>           |
| <span data-ttu-id="d1e65-1799">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1799">Count</span></span> | <span data-ttu-id="d1e65-1800">Anzahl der Frames im Bild</span><span class="sxs-lookup"><span data-stu-id="d1e65-1800">Number of frames in the image</span></span> |



 

## <a name="propertytagloopcount"></a><span data-ttu-id="d1e65-1801">Propertytagloopcount</span><span class="sxs-lookup"><span data-stu-id="d1e65-1801">PropertyTagLoopCount</span></span>

<span data-ttu-id="d1e65-1802">Gibt an, wie oft die Animation in einem animierten GIF-Bild angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1802">For an animated GIF image, the number of times to display the animation.</span></span> <span data-ttu-id="d1e65-1803">Der Wert 0 gibt an, dass die Animation unendlich angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1803">A value of 0 specifies that the animation should be displayed infinitely.</span></span>



| <span data-ttu-id="d1e65-1804">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1804">Property info</span></span> | <span data-ttu-id="d1e65-1805">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1805">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="d1e65-1806">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1806">Tag</span></span>   | <span data-ttu-id="d1e65-1807">0x5101</span><span class="sxs-lookup"><span data-stu-id="d1e65-1807">0x5101</span></span>               |
| <span data-ttu-id="d1e65-1808">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1808">Type</span></span>  | <span data-ttu-id="d1e65-1809">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-1809">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="d1e65-1810">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1810">Count</span></span> | <span data-ttu-id="d1e65-1811">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-1811">1</span></span>                    |



 

## <a name="propertytagglobalpalette"></a><span data-ttu-id="d1e65-1812">Propertytagglobalpalette</span><span class="sxs-lookup"><span data-stu-id="d1e65-1812">PropertyTagGlobalPalette</span></span>

<span data-ttu-id="d1e65-1813">Farbpalette für eine indizierte Bitmap in einem GIF-Bild.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1813">Color palette for an indexed bitmap in a GIF image.</span></span>



| <span data-ttu-id="d1e65-1814">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1814">Property info</span></span> | <span data-ttu-id="d1e65-1815">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1815">Value</span></span> |
|-------|-------------------------------|
| <span data-ttu-id="d1e65-1816">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1816">Tag</span></span>   | <span data-ttu-id="d1e65-1817">0x5102</span><span class="sxs-lookup"><span data-stu-id="d1e65-1817">0x5102</span></span>                        |
| <span data-ttu-id="d1e65-1818">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1818">Type</span></span>  | <span data-ttu-id="d1e65-1819">Propertytagtypebyte</span><span class="sxs-lookup"><span data-stu-id="d1e65-1819">PropertyTagTypeByte</span></span>           |
| <span data-ttu-id="d1e65-1820">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1820">Count</span></span> | <span data-ttu-id="d1e65-1821">3 x Anzahl von paletteneinträgen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1821">3 x number of palette entries</span></span> |



 

## <a name="propertytagindexbackground"></a><span data-ttu-id="d1e65-1822">Propertytagindexbackground</span><span class="sxs-lookup"><span data-stu-id="d1e65-1822">PropertyTagIndexBackground</span></span>

<span data-ttu-id="d1e65-1823">Der Index der Hintergrundfarbe in der Palette eines GIF-Bilds.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1823">Index of the background color in the palette of a GIF image.</span></span>



| <span data-ttu-id="d1e65-1824">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1824">Property info</span></span> | <span data-ttu-id="d1e65-1825">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1825">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="d1e65-1826">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1826">Tag</span></span>   | <span data-ttu-id="d1e65-1827">0x5103</span><span class="sxs-lookup"><span data-stu-id="d1e65-1827">0x5103</span></span>              |
| <span data-ttu-id="d1e65-1828">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1828">Type</span></span>  | <span data-ttu-id="d1e65-1829">Propertytagtypebyte</span><span class="sxs-lookup"><span data-stu-id="d1e65-1829">PropertyTagTypeByte</span></span> |
| <span data-ttu-id="d1e65-1830">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1830">Count</span></span> | <span data-ttu-id="d1e65-1831">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-1831">1</span></span>                   |



 

## <a name="propertytagindextransparent"></a><span data-ttu-id="d1e65-1832">Propertytagindextransparent</span><span class="sxs-lookup"><span data-stu-id="d1e65-1832">PropertyTagIndexTransparent</span></span>

<span data-ttu-id="d1e65-1833">Der Index der transparenten Farbe in der Palette eines GIF-Bilds.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1833">Index of the transparent color in the palette of a GIF image.</span></span>



| <span data-ttu-id="d1e65-1834">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1834">Property info</span></span> | <span data-ttu-id="d1e65-1835">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1835">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="d1e65-1836">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1836">Tag</span></span>   | <span data-ttu-id="d1e65-1837">0x5104</span><span class="sxs-lookup"><span data-stu-id="d1e65-1837">0x5104</span></span>              |
| <span data-ttu-id="d1e65-1838">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1838">Type</span></span>  | <span data-ttu-id="d1e65-1839">Propertytagtypebyte</span><span class="sxs-lookup"><span data-stu-id="d1e65-1839">PropertyTagTypeByte</span></span> |
| <span data-ttu-id="d1e65-1840">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1840">Count</span></span> | <span data-ttu-id="d1e65-1841">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-1841">1</span></span>                   |



 

## <a name="propertytagpixelunit"></a><span data-ttu-id="d1e65-1842">Propertytagpixelunit</span><span class="sxs-lookup"><span data-stu-id="d1e65-1842">PropertyTagPixelUnit</span></span>

<span data-ttu-id="d1e65-1843">Einheit für propertytagpixelperunitx und propertytagpixelperunity.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1843">Unit for PropertyTagPixelPerUnitX and PropertyTagPixelPerUnitY.</span></span>



<span data-ttu-id="d1e65-1844">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1844">Tag</span></span>

<span data-ttu-id="d1e65-1845">0x5110</span><span class="sxs-lookup"><span data-stu-id="d1e65-1845">0x5110</span></span>

<span data-ttu-id="d1e65-1846">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1846">Type</span></span>

<span data-ttu-id="d1e65-1847">Propertytagtypebyte</span><span class="sxs-lookup"><span data-stu-id="d1e65-1847">PropertyTagTypeByte</span></span>

<span data-ttu-id="d1e65-1848">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1848">Count</span></span>

<span data-ttu-id="d1e65-1849">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-1849">1</span></span>

<span data-ttu-id="d1e65-1850">0-unbekannt</span><span class="sxs-lookup"><span data-stu-id="d1e65-1850">0 - unknown</span></span>



 

## <a name="propertytagpixelperunitx"></a><span data-ttu-id="d1e65-1851">Propertytagpixelperunitx</span><span class="sxs-lookup"><span data-stu-id="d1e65-1851">PropertyTagPixelPerUnitX</span></span>

<span data-ttu-id="d1e65-1852">Pixel pro Einheit in der x-Richtung.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1852">Pixels per unit in the x direction.</span></span>



| <span data-ttu-id="d1e65-1853">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1853">Property info</span></span> | <span data-ttu-id="d1e65-1854">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1854">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="d1e65-1855">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1855">Tag</span></span>   | <span data-ttu-id="d1e65-1856">0x5111</span><span class="sxs-lookup"><span data-stu-id="d1e65-1856">0x5111</span></span>              |
| <span data-ttu-id="d1e65-1857">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1857">Type</span></span>  | <span data-ttu-id="d1e65-1858">Propertytagtypelong</span><span class="sxs-lookup"><span data-stu-id="d1e65-1858">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="d1e65-1859">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1859">Count</span></span> | <span data-ttu-id="d1e65-1860">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-1860">1</span></span>                   |



 

## <a name="propertytagpixelperunity"></a><span data-ttu-id="d1e65-1861">Propertytagpixelperunity</span><span class="sxs-lookup"><span data-stu-id="d1e65-1861">PropertyTagPixelPerUnitY</span></span>

<span data-ttu-id="d1e65-1862">Pixel pro Einheit in y-Richtung.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1862">Pixels per unit in the y direction.</span></span>



| <span data-ttu-id="d1e65-1863">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1863">Property info</span></span> | <span data-ttu-id="d1e65-1864">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1864">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="d1e65-1865">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1865">Tag</span></span>   | <span data-ttu-id="d1e65-1866">0x5112</span><span class="sxs-lookup"><span data-stu-id="d1e65-1866">0x5112</span></span>              |
| <span data-ttu-id="d1e65-1867">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1867">Type</span></span>  | <span data-ttu-id="d1e65-1868">Propertytagtypelong</span><span class="sxs-lookup"><span data-stu-id="d1e65-1868">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="d1e65-1869">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1869">Count</span></span> | <span data-ttu-id="d1e65-1870">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-1870">1</span></span>                   |



 

## <a name="propertytagpalettehistogram"></a><span data-ttu-id="d1e65-1871">Propertytagpalettehistogram</span><span class="sxs-lookup"><span data-stu-id="d1e65-1871">PropertyTagPaletteHistogram</span></span>

<span data-ttu-id="d1e65-1872">Palettenhistogramm.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1872">Palette histogram.</span></span>



| <span data-ttu-id="d1e65-1873">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1873">Property info</span></span> | <span data-ttu-id="d1e65-1874">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1874">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="d1e65-1875">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1875">Tag</span></span>   | <span data-ttu-id="d1e65-1876">0x5113</span><span class="sxs-lookup"><span data-stu-id="d1e65-1876">0x5113</span></span>                  |
| <span data-ttu-id="d1e65-1877">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1877">Type</span></span>  | <span data-ttu-id="d1e65-1878">Propertytagtypebyte</span><span class="sxs-lookup"><span data-stu-id="d1e65-1878">PropertyTagTypeByte</span></span>     |
| <span data-ttu-id="d1e65-1879">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1879">Count</span></span> | <span data-ttu-id="d1e65-1880">Länge des Histogramms</span><span class="sxs-lookup"><span data-stu-id="d1e65-1880">Length of the histogram</span></span> |



 

## <a name="propertytagcopyright"></a><span data-ttu-id="d1e65-1881">Propertytagcopyright</span><span class="sxs-lookup"><span data-stu-id="d1e65-1881">PropertyTagCopyright</span></span>

<span data-ttu-id="d1e65-1882">Mit NULL beendete Zeichenfolge, die Copyright Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1882">Null-terminated character string that contains copyright information.</span></span>



| <span data-ttu-id="d1e65-1883">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1883">Property info</span></span> | <span data-ttu-id="d1e65-1884">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1884">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="d1e65-1885">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1885">Tag</span></span>   | <span data-ttu-id="d1e65-1886">0x8298</span><span class="sxs-lookup"><span data-stu-id="d1e65-1886">0x8298</span></span>                                             |
| <span data-ttu-id="d1e65-1887">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1887">Type</span></span>  | <span data-ttu-id="d1e65-1888">Propertytagtybäuercii</span><span class="sxs-lookup"><span data-stu-id="d1e65-1888">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="d1e65-1889">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1889">Count</span></span> | <span data-ttu-id="d1e65-1890">Länge der Zeichenfolge einschließlich des NULL-Terminator</span><span class="sxs-lookup"><span data-stu-id="d1e65-1890">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagexifexposuretime"></a><span data-ttu-id="d1e65-1891">Propertytagexif ExposureTime</span><span class="sxs-lookup"><span data-stu-id="d1e65-1891">PropertyTagExifExposureTime</span></span>

<span data-ttu-id="d1e65-1892">Die Expositionszeit in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1892">Exposure time, measured in seconds.</span></span>



| <span data-ttu-id="d1e65-1893">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1893">Property info</span></span> | <span data-ttu-id="d1e65-1894">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1894">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="d1e65-1895">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1895">Tag</span></span>   | <span data-ttu-id="d1e65-1896">0x829a</span><span class="sxs-lookup"><span data-stu-id="d1e65-1896">0x829A</span></span>                  |
| <span data-ttu-id="d1e65-1897">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1897">Type</span></span>  | <span data-ttu-id="d1e65-1898">Propertytagtyperational</span><span class="sxs-lookup"><span data-stu-id="d1e65-1898">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="d1e65-1899">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1899">Count</span></span> | <span data-ttu-id="d1e65-1900">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-1900">1</span></span>                       |



 

## <a name="propertytagexiffnumber"></a><span data-ttu-id="d1e65-1901">Propertytagexiffnumber</span><span class="sxs-lookup"><span data-stu-id="d1e65-1901">PropertyTagExifFNumber</span></span>

<span data-ttu-id="d1e65-1902">F-Nummer.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1902">F number.</span></span>



| <span data-ttu-id="d1e65-1903">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1903">Property info</span></span> | <span data-ttu-id="d1e65-1904">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1904">Value</span></span> |
|-------|----------|
| <span data-ttu-id="d1e65-1905">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1905">Tag</span></span>   | <span data-ttu-id="d1e65-1906">0x829d</span><span class="sxs-lookup"><span data-stu-id="d1e65-1906">0x829D</span></span>   |
| <span data-ttu-id="d1e65-1907">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1907">Type</span></span>  | <span data-ttu-id="d1e65-1908">Vernünftige</span><span class="sxs-lookup"><span data-stu-id="d1e65-1908">RATIONAL</span></span> |
| <span data-ttu-id="d1e65-1909">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1909">Count</span></span> | <span data-ttu-id="d1e65-1910">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-1910">1</span></span>        |



 

## <a name="propertytagexififd"></a><span data-ttu-id="d1e65-1911">Propertytagexififd</span><span class="sxs-lookup"><span data-stu-id="d1e65-1911">PropertyTagExifIFD</span></span>

<span data-ttu-id="d1e65-1912">Privates Tag, das von GDI+ verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1912">Private tag used by GDI+.</span></span> <span data-ttu-id="d1e65-1913">Nicht für die öffentliche Verwendung.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1913">Not for public use.</span></span> <span data-ttu-id="d1e65-1914">GDI+ verwendet dieses Tag, um EXIF-spezifische Informationen zu suchen.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1914">GDI+ uses this tag to locate Exif-specific information.</span></span>



| <span data-ttu-id="d1e65-1915">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1915">Property info</span></span> | <span data-ttu-id="d1e65-1916">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1916">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="d1e65-1917">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1917">Tag</span></span>   | <span data-ttu-id="d1e65-1918">0x8769</span><span class="sxs-lookup"><span data-stu-id="d1e65-1918">0x8769</span></span>              |
| <span data-ttu-id="d1e65-1919">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1919">Type</span></span>  | <span data-ttu-id="d1e65-1920">Propertytagtypelong</span><span class="sxs-lookup"><span data-stu-id="d1e65-1920">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="d1e65-1921">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1921">Count</span></span> | <span data-ttu-id="d1e65-1922">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-1922">1</span></span>                   |



 

## <a name="propertytagiccprofile"></a><span data-ttu-id="d1e65-1923">Propertytagiccprofile</span><span class="sxs-lookup"><span data-stu-id="d1e65-1923">PropertyTagICCProfile</span></span>

<span data-ttu-id="d1e65-1924">Das in das Image eingebettete ICC-Profil.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1924">ICC profile embedded in the image.</span></span>



| <span data-ttu-id="d1e65-1925">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1925">Property info</span></span> | <span data-ttu-id="d1e65-1926">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1926">Value</span></span> |
|-------|-----------------------|
| <span data-ttu-id="d1e65-1927">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1927">Tag</span></span>   | <span data-ttu-id="d1e65-1928">0x8773</span><span class="sxs-lookup"><span data-stu-id="d1e65-1928">0x8773</span></span>                |
| <span data-ttu-id="d1e65-1929">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1929">Type</span></span>  | <span data-ttu-id="d1e65-1930">Propertytagtypebyte</span><span class="sxs-lookup"><span data-stu-id="d1e65-1930">PropertyTagTypeByte</span></span>   |
| <span data-ttu-id="d1e65-1931">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1931">Count</span></span> | <span data-ttu-id="d1e65-1932">Länge des Profils</span><span class="sxs-lookup"><span data-stu-id="d1e65-1932">Length of the profile</span></span> |



 

## <a name="propertytagexifexposureprog"></a><span data-ttu-id="d1e65-1933">Propertytagexif exposureproduktionen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1933">PropertyTagExifExposureProg</span></span>

<span data-ttu-id="d1e65-1934">Klasse des Programms, das von der Kamera verwendet wird, um die Verfügbarkeit festzulegen, wenn das Bild übernommen wird.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1934">Class of the program used by the camera to set exposure when the picture is taken.</span></span>



<span data-ttu-id="d1e65-1935">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1935">Tag</span></span>

<span data-ttu-id="d1e65-1936">0x8822</span><span class="sxs-lookup"><span data-stu-id="d1e65-1936">0x8822</span></span>

<span data-ttu-id="d1e65-1937">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1937">Type</span></span>

<span data-ttu-id="d1e65-1938">SHORT</span><span class="sxs-lookup"><span data-stu-id="d1e65-1938">SHORT</span></span>

<span data-ttu-id="d1e65-1939">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1939">Count</span></span>

<span data-ttu-id="d1e65-1940">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-1940">1</span></span>

<span data-ttu-id="d1e65-1941">Standard</span><span class="sxs-lookup"><span data-stu-id="d1e65-1941">Default</span></span>

<span data-ttu-id="d1e65-1942">0</span><span class="sxs-lookup"><span data-stu-id="d1e65-1942">0</span></span>

<span data-ttu-id="d1e65-1943">0-nicht definiert 1-manuelles 2-normales-Programm 3-Aperture-Priorität 4-Rollout Priorität 5-Creative Program (für die Tiefe des Felds voreingenommen) 6-Aktionsprogramm (für die schnelle debuggeschwindigkeit), 7-hoch-Modus (für schließende Fotos mit dem Hintergrund im Fokus), 9 bis 255-reserviert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1943">0 - not defined 1 - manual 2 - normal program 3 - aperture priority 4 - shutter priority 5 - creative program (biased toward depth of field) 6 - action program (biased toward fast shutter speed) 7 - portrait mode (for close-up photos with the background out of focus) 8 - landscape mode (for landscape photos with the background in focus) 9 to 255 - reserved</span></span>



 

## <a name="propertytagexifspectralsense"></a><span data-ttu-id="d1e65-1944">Propertytagexif spectralsense</span><span class="sxs-lookup"><span data-stu-id="d1e65-1944">PropertyTagExifSpectralSense</span></span>

<span data-ttu-id="d1e65-1945">Eine auf NULL endende Zeichenfolge, die die Unterscheidung zwischen den einzelnen Kanälen der verwendeten Kamera angibt.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1945">Null-terminated character string that specifies the spectral sensitivity of each channel of the camera used.</span></span> <span data-ttu-id="d1e65-1946">Die Zeichenfolge ist mit dem vom ASTM Technical Committee entwickelten Standard kompatibel.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1946">The string is compatible with the standard developed by the ASTM Technical Committee.</span></span>



| <span data-ttu-id="d1e65-1947">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1947">Property info</span></span> | <span data-ttu-id="d1e65-1948">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1948">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="d1e65-1949">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1949">Tag</span></span>   | <span data-ttu-id="d1e65-1950">0x8824</span><span class="sxs-lookup"><span data-stu-id="d1e65-1950">0x8824</span></span>                                             |
| <span data-ttu-id="d1e65-1951">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1951">Type</span></span>  | <span data-ttu-id="d1e65-1952">Propertytagtybäuercii</span><span class="sxs-lookup"><span data-stu-id="d1e65-1952">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="d1e65-1953">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1953">Count</span></span> | <span data-ttu-id="d1e65-1954">Länge der Zeichenfolge einschließlich des NULL-Terminator</span><span class="sxs-lookup"><span data-stu-id="d1e65-1954">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytaggpsifd"></a><span data-ttu-id="d1e65-1955">Propertytaggpsifd</span><span class="sxs-lookup"><span data-stu-id="d1e65-1955">PropertyTagGpsIFD</span></span>

<span data-ttu-id="d1e65-1956">Offset zu einem Block von GPS-Eigenschaften Elementen.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1956">Offset to a block of GPS property items.</span></span> <span data-ttu-id="d1e65-1957">Eigenschaften Elemente, deren Tags das Präfix propertytaggps aufweisen, werden im GPS-Block gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1957">Property items whose tags have the prefix PropertyTagGps are stored in the GPS block.</span></span> <span data-ttu-id="d1e65-1958">Die GPS-Eigenschaften Elemente werden in der EXIF-Spezifikation definiert.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1958">The GPS property items are defined in the EXIF specification.</span></span> <span data-ttu-id="d1e65-1959">GDI+ verwendet dieses Tag, um GPS-Informationen zu suchen, aber GDI+ macht dieses Tag nicht für die öffentliche Verwendung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1959">GDI+ uses this tag to locate GPS information, but GDI+ does not expose this tag for public use.</span></span>



| <span data-ttu-id="d1e65-1960">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1960">Property info</span></span> | <span data-ttu-id="d1e65-1961">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1961">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="d1e65-1962">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1962">Tag</span></span>   | <span data-ttu-id="d1e65-1963">0x8825</span><span class="sxs-lookup"><span data-stu-id="d1e65-1963">0x8825</span></span>              |
| <span data-ttu-id="d1e65-1964">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1964">Type</span></span>  | <span data-ttu-id="d1e65-1965">Propertytagtypelong</span><span class="sxs-lookup"><span data-stu-id="d1e65-1965">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="d1e65-1966">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1966">Count</span></span> | <span data-ttu-id="d1e65-1967">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-1967">1</span></span>                   |



 

## <a name="propertytagexifisospeed"></a><span data-ttu-id="d1e65-1968">Propertytagexisospeed</span><span class="sxs-lookup"><span data-stu-id="d1e65-1968">PropertyTagExifISOSpeed</span></span>

<span data-ttu-id="d1e65-1969">ISO-Geschwindigkeit und ISO-Breite der Kamera oder des Eingabe Geräts, wie in ISO 12232 angegeben.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1969">ISO speed and ISO latitude of the camera or input device as specified in ISO 12232.</span></span>



| <span data-ttu-id="d1e65-1970">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1970">Property info</span></span> | <span data-ttu-id="d1e65-1971">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1971">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="d1e65-1972">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1972">Tag</span></span>   | <span data-ttu-id="d1e65-1973">0x8827</span><span class="sxs-lookup"><span data-stu-id="d1e65-1973">0x8827</span></span>               |
| <span data-ttu-id="d1e65-1974">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1974">Type</span></span>  | <span data-ttu-id="d1e65-1975">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-1975">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="d1e65-1976">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1976">Count</span></span> | <span data-ttu-id="d1e65-1977">Any</span><span class="sxs-lookup"><span data-stu-id="d1e65-1977">Any</span></span>                  |



 

## <a name="propertytagexifoecf"></a><span data-ttu-id="d1e65-1978">Propertytagexifoecf</span><span class="sxs-lookup"><span data-stu-id="d1e65-1978">PropertyTagExifOECF</span></span>

<span data-ttu-id="d1e65-1979">Die in ISO 14524 angegebene Funktion für die optoelektronische Konvertierung (oecf).</span><span class="sxs-lookup"><span data-stu-id="d1e65-1979">Optoelectronic conversion function (OECF) specified in ISO 14524.</span></span> <span data-ttu-id="d1e65-1980">Die oecf ist die Beziehung zwischen der optischen Kameraeingabe und den bildwerten.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1980">The OECF is the relationship between the camera optical input and the image values.</span></span>



| <span data-ttu-id="d1e65-1981">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1981">Property info</span></span> | <span data-ttu-id="d1e65-1982">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1982">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="d1e65-1983">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1983">Tag</span></span>   | <span data-ttu-id="d1e65-1984">0x8828</span><span class="sxs-lookup"><span data-stu-id="d1e65-1984">0x8828</span></span>                   |
| <span data-ttu-id="d1e65-1985">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1985">Type</span></span>  | <span data-ttu-id="d1e65-1986">Propertytagtypeundefiniert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1986">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="d1e65-1987">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-1987">Count</span></span> | <span data-ttu-id="d1e65-1988">Any</span><span class="sxs-lookup"><span data-stu-id="d1e65-1988">Any</span></span>                      |



 

## <a name="propertytagexifver"></a><span data-ttu-id="d1e65-1989">Propertytagexifäver</span><span class="sxs-lookup"><span data-stu-id="d1e65-1989">PropertyTagExifVer</span></span>

<span data-ttu-id="d1e65-1990">Die Version des unterstützten EXIF-Standards.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1990">Version of the EXIF standard supported.</span></span> <span data-ttu-id="d1e65-1991">Wenn dieses Feld nicht vorhanden ist, bedeutet dies, dass es nicht mit dem Standard übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1991">Nonexistence of this field is taken to mean nonconformance to the standard.</span></span> <span data-ttu-id="d1e65-1992">Die Übereinstimmung mit dem Standard wird durch Aufzeichnen von 0210 als 4-Byte-ASCII-Zeichenfolge angegeben.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1992">Conformance to the standard is indicated by recording 0210 as a 4-byte ASCII string.</span></span> <span data-ttu-id="d1e65-1993">Da der Typ propertytagtypeundefiniert ist, ist kein NULL-Terminator vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d1e65-1993">Because the type is PropertyTagTypeUndefined, there is no NULL terminator.</span></span>



| <span data-ttu-id="d1e65-1994">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-1994">Property info</span></span> | <span data-ttu-id="d1e65-1995">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1995">Value</span></span> |
|---------|--------------------------|
| <span data-ttu-id="d1e65-1996">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-1996">Tag</span></span>     | <span data-ttu-id="d1e65-1997">0x9000</span><span class="sxs-lookup"><span data-stu-id="d1e65-1997">0x9000</span></span>                   |
| <span data-ttu-id="d1e65-1998">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-1998">Type</span></span>    | <span data-ttu-id="d1e65-1999">Propertytagtypeundefiniert</span><span class="sxs-lookup"><span data-stu-id="d1e65-1999">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="d1e65-2000">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-2000">Count</span></span>   | <span data-ttu-id="d1e65-2001">4</span><span class="sxs-lookup"><span data-stu-id="d1e65-2001">4</span></span>                        |
| <span data-ttu-id="d1e65-2002">Standard</span><span class="sxs-lookup"><span data-stu-id="d1e65-2002">Default</span></span> | <span data-ttu-id="d1e65-2003">0210</span><span class="sxs-lookup"><span data-stu-id="d1e65-2003">0210</span></span>                     |



 

## <a name="propertytagexifdtorig"></a><span data-ttu-id="d1e65-2004">Propertytagexiledtorig</span><span class="sxs-lookup"><span data-stu-id="d1e65-2004">PropertyTagExifDTOrig</span></span>

<span data-ttu-id="d1e65-2005">Datum und Uhrzeit, zu der die ursprünglichen Bilddaten generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2005">Date and time when the original image data was generated.</span></span> <span data-ttu-id="d1e65-2006">Bei einem DSC das Datum und die Uhrzeit der Bild Erstellung.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2006">For a DSC, the date and time when the picture was taken.</span></span> <span data-ttu-id="d1e65-2007">Das Format lautet yyyy: mm: DD hh: mm: SS, wobei die Zeit im 24-Stunden-Format und das Datum und die Uhrzeit durch ein Leerzeichen (0x2000) getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2007">The format is YYYY:MM:DD HH:MM:SS with time shown in 24-hour format and the date and time separated by one blank character (0x2000).</span></span> <span data-ttu-id="d1e65-2008">Die Länge der Zeichenfolge beträgt 20 Bytes, einschließlich des NULL-Terminator.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2008">The character string length is 20 bytes including the NULL terminator.</span></span> <span data-ttu-id="d1e65-2009">Wenn das Feld leer ist, wird es als unbekannt behandelt.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2009">When the field is empty, it is treated as unknown.</span></span>



| <span data-ttu-id="d1e65-2010">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-2010">Property info</span></span> | <span data-ttu-id="d1e65-2011">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-2011">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="d1e65-2012">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-2012">Tag</span></span>   | <span data-ttu-id="d1e65-2013">0x9003</span><span class="sxs-lookup"><span data-stu-id="d1e65-2013">0x9003</span></span>               |
| <span data-ttu-id="d1e65-2014">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-2014">Type</span></span>  | <span data-ttu-id="d1e65-2015">Propertytagtybäuercii</span><span class="sxs-lookup"><span data-stu-id="d1e65-2015">PropertyTagTypeASCII</span></span> |
| <span data-ttu-id="d1e65-2016">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-2016">Count</span></span> | <span data-ttu-id="d1e65-2017">20</span><span class="sxs-lookup"><span data-stu-id="d1e65-2017">20</span></span>                   |



 

## <a name="propertytagexifdtdigitized"></a><span data-ttu-id="d1e65-2018">Propertytagexitdtdigit</span><span class="sxs-lookup"><span data-stu-id="d1e65-2018">PropertyTagExifDTDigitized</span></span>

<span data-ttu-id="d1e65-2019">Datum und Uhrzeit, zu denen das Image als digitale Daten gespeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2019">Date and time when the image was stored as digital data.</span></span> <span data-ttu-id="d1e65-2020">Wenn z. b. ein Image von DSC aufgezeichnet wurde und gleichzeitig die Datei aufgezeichnet wurde, haben DateTimeOriginal und datetimedigitisiert denselben Inhalt.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2020">If, for example, an image was captured by DSC and at the same time the file was recorded, then DateTimeOriginal and DateTimeDigitized will have the same contents.</span></span>

<span data-ttu-id="d1e65-2021">Das Format lautet yyyy: mm: DD hh: mm: SS, wobei die Zeit im 24-Stunden-Format und das Datum und die Uhrzeit durch ein Leerzeichen (0x2000) getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2021">The format is YYYY:MM:DD HH:MM:SS with time shown in 24-hour format and the date and time separated by one blank character (0x2000).</span></span> <span data-ttu-id="d1e65-2022">Die Länge der Zeichenfolge beträgt 20 Bytes, einschließlich des NULL-Terminator.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2022">The character string length is 20 bytes including the NULL terminator.</span></span> <span data-ttu-id="d1e65-2023">Wenn das Feld leer ist, wird es als unbekannt behandelt.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2023">When the field is empty, it is treated as unknown.</span></span>



| <span data-ttu-id="d1e65-2024">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-2024">Property info</span></span> | <span data-ttu-id="d1e65-2025">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-2025">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="d1e65-2026">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-2026">Tag</span></span>   | <span data-ttu-id="d1e65-2027">0x9004</span><span class="sxs-lookup"><span data-stu-id="d1e65-2027">0x9004</span></span>               |
| <span data-ttu-id="d1e65-2028">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-2028">Type</span></span>  | <span data-ttu-id="d1e65-2029">Propertytagtybäuercii</span><span class="sxs-lookup"><span data-stu-id="d1e65-2029">PropertyTagTypeASCII</span></span> |
| <span data-ttu-id="d1e65-2030">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-2030">Count</span></span> | <span data-ttu-id="d1e65-2031">20</span><span class="sxs-lookup"><span data-stu-id="d1e65-2031">20</span></span>                   |



 

## <a name="propertytagexifcompconfig"></a><span data-ttu-id="d1e65-2032">Propertytagexif compconfig</span><span class="sxs-lookup"><span data-stu-id="d1e65-2032">PropertyTagExifCompConfig</span></span>

<span data-ttu-id="d1e65-2033">Informationen, die für komprimierte Daten spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2033">Information specific to compressed data.</span></span> <span data-ttu-id="d1e65-2034">Die Kanäle der einzelnen Komponenten werden in der Reihenfolge von der ersten Komponente zum vierten angeordnet.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2034">The channels of each component are arranged in order from the first component to the fourth.</span></span> <span data-ttu-id="d1e65-2035">Bei nicht komprimierten Daten wird die Daten Anordnung im Tag propertytagphoto ezcinterp angegeben.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2035">For uncompressed data, the data arrangement is given in the PropertyTagPhotometricInterp tag.</span></span>

<span data-ttu-id="d1e65-2036">Da propertytagphoto etricinterp jedoch nur die Reihenfolge von y, CB und CR Ausdrücken kann, wird dieses Tag für Fälle bereitgestellt, in denen komprimierte Daten andere Komponenten als Y, CB und CR verwenden und andere Sequenzen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2036">However, because PropertyTagPhotometricInterp can only express the order of Y, Cb, and Cr, this tag is provided for cases when compressed data uses components other than Y, Cb, and Cr and to support other sequences.</span></span>



<span data-ttu-id="d1e65-2037">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-2037">Tag</span></span>

<span data-ttu-id="d1e65-2038">0x9101</span><span class="sxs-lookup"><span data-stu-id="d1e65-2038">0x9101</span></span>

<span data-ttu-id="d1e65-2039">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-2039">Type</span></span>

<span data-ttu-id="d1e65-2040">Propertytagtypeundefiniert</span><span class="sxs-lookup"><span data-stu-id="d1e65-2040">PropertyTagTypeUndefined</span></span>

<span data-ttu-id="d1e65-2041">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-2041">Count</span></span>

<span data-ttu-id="d1e65-2042">4</span><span class="sxs-lookup"><span data-stu-id="d1e65-2042">4</span></span>

<span data-ttu-id="d1e65-2043">Standard</span><span class="sxs-lookup"><span data-stu-id="d1e65-2043">Default</span></span>

<span data-ttu-id="d1e65-2044">4 5 6 0 (wenn RGB nicht komprimiert ist) 1 2 3 0 (andere Fälle)</span><span class="sxs-lookup"><span data-stu-id="d1e65-2044">4 5 6 0 (if RGB uncompressed) 1 2 3 0 (other cases)</span></span>

<span data-ttu-id="d1e65-2045">0-nicht vorhanden 1-Y 2-CB 3-CR 4-R 5-G 6-B other-reserved</span><span class="sxs-lookup"><span data-stu-id="d1e65-2045">0 - does not exist 1 - Y 2 - Cb 3 - Cr 4 - R 5 - G 6 - B Other - reserved</span></span>



 

## <a name="propertytagexifcompbpp"></a><span data-ttu-id="d1e65-2046">Propertytagexibcompbpp</span><span class="sxs-lookup"><span data-stu-id="d1e65-2046">PropertyTagExifCompBPP</span></span>

<span data-ttu-id="d1e65-2047">Informationen, die für komprimierte Daten spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2047">Information specific to compressed data.</span></span> <span data-ttu-id="d1e65-2048">Der für ein komprimiertes Bild verwendete Komprimierungs Modus wird in der bpp-Einheit angegeben.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2048">The compression mode used for a compressed image is indicated in unit BPP.</span></span>



| <span data-ttu-id="d1e65-2049">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-2049">Property info</span></span> | <span data-ttu-id="d1e65-2050">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-2050">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="d1e65-2051">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-2051">Tag</span></span>   | <span data-ttu-id="d1e65-2052">0x9102</span><span class="sxs-lookup"><span data-stu-id="d1e65-2052">0x9102</span></span>                  |
| <span data-ttu-id="d1e65-2053">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-2053">Type</span></span>  | <span data-ttu-id="d1e65-2054">Propertytagtyperational</span><span class="sxs-lookup"><span data-stu-id="d1e65-2054">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="d1e65-2055">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-2055">Count</span></span> | <span data-ttu-id="d1e65-2056">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-2056">1</span></span>                       |



 

## <a name="propertytagexifshutterspeed"></a><span data-ttu-id="d1e65-2057">Propertytagexifshutterspeed</span><span class="sxs-lookup"><span data-stu-id="d1e65-2057">PropertyTagExifShutterSpeed</span></span>

<span data-ttu-id="d1e65-2058">Die Auslösegeschwindigkeit.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2058">Shutter speed.</span></span> <span data-ttu-id="d1e65-2059">Bei der Einheit handelt es sich um das Additive System of Photo Exposure (APEX)-Werts.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2059">The unit is the Additive System of Photographic Exposure (APEX) value.</span></span>



| <span data-ttu-id="d1e65-2060">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-2060">Property info</span></span> | <span data-ttu-id="d1e65-2061">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-2061">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="d1e65-2062">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-2062">Tag</span></span>   | <span data-ttu-id="d1e65-2063">0x9201</span><span class="sxs-lookup"><span data-stu-id="d1e65-2063">0x9201</span></span>                   |
| <span data-ttu-id="d1e65-2064">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-2064">Type</span></span>  | <span data-ttu-id="d1e65-2065">Propertytagtypesrational</span><span class="sxs-lookup"><span data-stu-id="d1e65-2065">PropertyTagTypeSRational</span></span> |
| <span data-ttu-id="d1e65-2066">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-2066">Count</span></span> | <span data-ttu-id="d1e65-2067">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-2067">1</span></span>                        |



 

## <a name="propertytagexifaperture"></a><span data-ttu-id="d1e65-2068">Propertytagexifaperture</span><span class="sxs-lookup"><span data-stu-id="d1e65-2068">PropertyTagExifAperture</span></span>

<span data-ttu-id="d1e65-2069">Licht blenden.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2069">Lens aperture.</span></span> <span data-ttu-id="d1e65-2070">Die Einheit ist der Apex-Wert.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2070">The unit is the APEX value.</span></span>



| <span data-ttu-id="d1e65-2071">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-2071">Property info</span></span> | <span data-ttu-id="d1e65-2072">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-2072">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="d1e65-2073">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-2073">Tag</span></span>   | <span data-ttu-id="d1e65-2074">0x9202</span><span class="sxs-lookup"><span data-stu-id="d1e65-2074">0x9202</span></span>                  |
| <span data-ttu-id="d1e65-2075">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-2075">Type</span></span>  | <span data-ttu-id="d1e65-2076">Propertytagtyperational</span><span class="sxs-lookup"><span data-stu-id="d1e65-2076">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="d1e65-2077">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-2077">Count</span></span> | <span data-ttu-id="d1e65-2078">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-2078">1</span></span>                       |



 

## <a name="propertytagexifbrightness"></a><span data-ttu-id="d1e65-2079">Propertytagexif-Helligkeit</span><span class="sxs-lookup"><span data-stu-id="d1e65-2079">PropertyTagExifBrightness</span></span>

<span data-ttu-id="d1e65-2080">Wert für Helligkeit.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2080">Brightness value.</span></span> <span data-ttu-id="d1e65-2081">Die Einheit ist der Apex-Wert.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2081">The unit is the APEX value.</span></span> <span data-ttu-id="d1e65-2082">Normalerweise wird Sie im Bereich von-99,99 bis 99,99 angegeben.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2082">Ordinarily it is given in the range of -99.99 to 99.99.</span></span>



| <span data-ttu-id="d1e65-2083">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-2083">Property info</span></span> | <span data-ttu-id="d1e65-2084">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-2084">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="d1e65-2085">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-2085">Tag</span></span>   | <span data-ttu-id="d1e65-2086">0x9203</span><span class="sxs-lookup"><span data-stu-id="d1e65-2086">0x9203</span></span>                   |
| <span data-ttu-id="d1e65-2087">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-2087">Type</span></span>  | <span data-ttu-id="d1e65-2088">Propertytagtypesrational</span><span class="sxs-lookup"><span data-stu-id="d1e65-2088">PropertyTagTypeSRational</span></span> |
| <span data-ttu-id="d1e65-2089">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-2089">Count</span></span> | <span data-ttu-id="d1e65-2090">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-2090">1</span></span>                        |



 

## <a name="propertytagexifexposurebias"></a><span data-ttu-id="d1e65-2091">Propertytagexif exposurebias</span><span class="sxs-lookup"><span data-stu-id="d1e65-2091">PropertyTagExifExposureBias</span></span>

<span data-ttu-id="d1e65-2092">Der Expositions-Bias.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2092">Exposure bias.</span></span> <span data-ttu-id="d1e65-2093">Die Einheit ist der Apex-Wert.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2093">The unit is the APEX value.</span></span> <span data-ttu-id="d1e65-2094">Normalerweise wird Sie im Bereich von-99,99 bis 99,99 angegeben.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2094">Ordinarily it is given in the range -99.99 to 99.99.</span></span>



| <span data-ttu-id="d1e65-2095">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-2095">Property info</span></span> | <span data-ttu-id="d1e65-2096">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-2096">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="d1e65-2097">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-2097">Tag</span></span>   | <span data-ttu-id="d1e65-2098">0x9204</span><span class="sxs-lookup"><span data-stu-id="d1e65-2098">0x9204</span></span>                   |
| <span data-ttu-id="d1e65-2099">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-2099">Type</span></span>  | <span data-ttu-id="d1e65-2100">Propertytagtypesrational</span><span class="sxs-lookup"><span data-stu-id="d1e65-2100">PropertyTagTypeSRational</span></span> |
| <span data-ttu-id="d1e65-2101">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-2101">Count</span></span> | <span data-ttu-id="d1e65-2102">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-2102">1</span></span>                        |



 

## <a name="propertytagexifmaxaperture"></a><span data-ttu-id="d1e65-2103">Propertytagexif-Aperture</span><span class="sxs-lookup"><span data-stu-id="d1e65-2103">PropertyTagExifMaxAperture</span></span>

<span data-ttu-id="d1e65-2104">Kleinste F-Zahl des Lens.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2104">Smallest F number of the lens.</span></span> <span data-ttu-id="d1e65-2105">Die Einheit ist der Apex-Wert.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2105">The unit is the APEX value.</span></span> <span data-ttu-id="d1e65-2106">Normalerweise wird Sie im Bereich von 00,00 bis 99,99 angegeben, ist aber nicht auf diesen Bereich beschränkt.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2106">Ordinarily it is given in the range of 00.00 to 99.99, but it is not limited to this range.</span></span>



| <span data-ttu-id="d1e65-2107">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-2107">Property info</span></span> | <span data-ttu-id="d1e65-2108">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-2108">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="d1e65-2109">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-2109">Tag</span></span>   | <span data-ttu-id="d1e65-2110">0x9205</span><span class="sxs-lookup"><span data-stu-id="d1e65-2110">0x9205</span></span>                  |
| <span data-ttu-id="d1e65-2111">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-2111">Type</span></span>  | <span data-ttu-id="d1e65-2112">Propertytagtyperational</span><span class="sxs-lookup"><span data-stu-id="d1e65-2112">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="d1e65-2113">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-2113">Count</span></span> | <span data-ttu-id="d1e65-2114">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-2114">1</span></span>                       |



 

## <a name="propertytagexifsubjectdist"></a><span data-ttu-id="d1e65-2115">Propertytagexilesubjetdist</span><span class="sxs-lookup"><span data-stu-id="d1e65-2115">PropertyTagExifSubjectDist</span></span>

<span data-ttu-id="d1e65-2116">Abstand zum Betreff, gemessen in Meter.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2116">Distance to the subject, measured in meters.</span></span>



| <span data-ttu-id="d1e65-2117">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-2117">Property info</span></span> | <span data-ttu-id="d1e65-2118">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-2118">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="d1e65-2119">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-2119">Tag</span></span>   | <span data-ttu-id="d1e65-2120">0x9206</span><span class="sxs-lookup"><span data-stu-id="d1e65-2120">0x9206</span></span>                  |
| <span data-ttu-id="d1e65-2121">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-2121">Type</span></span>  | <span data-ttu-id="d1e65-2122">Propertytagtyperational</span><span class="sxs-lookup"><span data-stu-id="d1e65-2122">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="d1e65-2123">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-2123">Count</span></span> | <span data-ttu-id="d1e65-2124">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-2124">1</span></span>                       |



 

## <a name="propertytagexifmeteringmode"></a><span data-ttu-id="d1e65-2125">Propertytagexismeteringmode</span><span class="sxs-lookup"><span data-stu-id="d1e65-2125">PropertyTagExifMeteringMode</span></span>

<span data-ttu-id="d1e65-2126">Messungs Modus.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2126">Metering mode.</span></span>



<span data-ttu-id="d1e65-2127">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-2127">Tag</span></span>

<span data-ttu-id="d1e65-2128">0x9207</span><span class="sxs-lookup"><span data-stu-id="d1e65-2128">0x9207</span></span>

<span data-ttu-id="d1e65-2129">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-2129">Type</span></span>

<span data-ttu-id="d1e65-2130">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-2130">PropertyTagTypeShort</span></span>

<span data-ttu-id="d1e65-2131">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-2131">Count</span></span>

<span data-ttu-id="d1e65-2132">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-2132">1</span></span>

<span data-ttu-id="d1e65-2133">Standard</span><span class="sxs-lookup"><span data-stu-id="d1e65-2133">Default</span></span>

<span data-ttu-id="d1e65-2134">0</span><span class="sxs-lookup"><span data-stu-id="d1e65-2134">0</span></span>

<span data-ttu-id="d1e65-2135">0-unbekannter 1-durchschnittlicher 2-centerweightedaverage 3-Spot 4-multiSpot 5-Pattern 6-partiell 7 bis 254-reserved 255-other</span><span class="sxs-lookup"><span data-stu-id="d1e65-2135">0 - unknown 1 - Average 2 - CenterWeightedAverage 3 - Spot 4 - MultiSpot 5 - Pattern 6 - Partial 7 to 254 - reserved 255 - other</span></span>



 

## <a name="propertytagexiflightsource"></a><span data-ttu-id="d1e65-2136">Propertytagexiflightsource</span><span class="sxs-lookup"><span data-stu-id="d1e65-2136">PropertyTagExifLightSource</span></span>

<span data-ttu-id="d1e65-2137">Der Typ der Lichtquelle.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2137">Type of light source.</span></span>



<span data-ttu-id="d1e65-2138">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-2138">Tag</span></span>

<span data-ttu-id="d1e65-2139">0x9208</span><span class="sxs-lookup"><span data-stu-id="d1e65-2139">0x9208</span></span>

<span data-ttu-id="d1e65-2140">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-2140">Type</span></span>

<span data-ttu-id="d1e65-2141">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-2141">PropertyTagTypeShort</span></span>

<span data-ttu-id="d1e65-2142">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-2142">Count</span></span>

<span data-ttu-id="d1e65-2143">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-2143">1</span></span>

<span data-ttu-id="d1e65-2144">Standard</span><span class="sxs-lookup"><span data-stu-id="d1e65-2144">Default</span></span>

<span data-ttu-id="d1e65-2145">0</span><span class="sxs-lookup"><span data-stu-id="d1e65-2145">0</span></span>

<span data-ttu-id="d1e65-2146">0-unbekanntes 1-Sommer 2-flourescent 3-Wolfram 17-Standard hell a 18 Standard hell B 19-Standard hell C 20-D55 21-D65 22-D75 23 bis 254-reserviert 255-other</span><span class="sxs-lookup"><span data-stu-id="d1e65-2146">0 - unknown 1 - Daylight 2 - Flourescent 3 - Tungsten 17 - Standard Light A 18 - Standard Light B 19 - Standard Light C 20 - D55 21 - D65 22 - D75 23 to 254 - reserved 255 - other</span></span>



 

## <a name="propertytagexifflash"></a><span data-ttu-id="d1e65-2147">Propertytagexifflash</span><span class="sxs-lookup"><span data-stu-id="d1e65-2147">PropertyTagExifFlash</span></span>

<span data-ttu-id="d1e65-2148">Flash Status.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2148">Flash status.</span></span> <span data-ttu-id="d1e65-2149">Dieses Tag wird aufgezeichnet, wenn ein Bild mithilfe eines Strobe Light (Flash) erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2149">This tag is recorded when an image is taken using a strobe light (flash).</span></span> <span data-ttu-id="d1e65-2150">Bit 0 gibt den Status des Flash auslöserstatus an, und Bits 1 und 2 geben den Status der Flash Rückgabe an.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2150">Bit 0 indicates the flash firing status, and bits 1 and 2 indicate the flash return status.</span></span>



<span data-ttu-id="d1e65-2151">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-2151">Tag</span></span>

<span data-ttu-id="d1e65-2152">0x9209</span><span class="sxs-lookup"><span data-stu-id="d1e65-2152">0x9209</span></span>

<span data-ttu-id="d1e65-2153">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-2153">Type</span></span>

<span data-ttu-id="d1e65-2154">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-2154">PropertyTagTypeShort</span></span>

<span data-ttu-id="d1e65-2155">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-2155">Count</span></span>

<span data-ttu-id="d1e65-2156">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-2156">1</span></span>

<span data-ttu-id="d1e65-2157">Werte für Bit 0, die angeben, ob der Flash ausgelöst wurde: 0B-Flash hat nicht ausgelöst: 1B-Flash ausgelöst</span><span class="sxs-lookup"><span data-stu-id="d1e65-2157">Values for bit 0 that indicate whether the flash fired: 0b - flash did not fire 1b - flash fired</span></span>

<span data-ttu-id="d1e65-2158">Werte für Bits 1 und 2, die den Status der zurückgegebenen Beleuchtung angeben: 00B-No Strobe Return Erkennungsfunktion 01B-reserved 10B-Strobe Return Light not erkannt 11b-Strobe Return Light erkannt</span><span class="sxs-lookup"><span data-stu-id="d1e65-2158">Values for bits 1 and 2 that indicate the status of returned light: 00b - no strobe return detection function 01b - reserved 10b - strobe return light not detected 11b - strobe return light detected</span></span>

<span data-ttu-id="d1e65-2159">Resultierende Flash-Tagwerte: 0x0000-Flash hat 0x0001 nicht ausgelöst-Flash ausgelöst 0x0005-Strobe-Rückgabe Licht nicht erkannt.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2159">Resulting flash tag values: 0x0000 - flash did not fire 0x0001 - flash fired 0x0005 - strobe return light not detected</span></span>



 

## <a name="propertytagexiffocallength"></a><span data-ttu-id="d1e65-2160">Propertytagexiffocallength</span><span class="sxs-lookup"><span data-stu-id="d1e65-2160">PropertyTagExifFocalLength</span></span>

<span data-ttu-id="d1e65-2161">Tatsächliche Fokuslänge des-Lens in Millimeter.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2161">Actual focal length, in millimeters, of the lens.</span></span> <span data-ttu-id="d1e65-2162">Die Konvertierung wird nicht auf die Fokuslänge einer 35-Millimeter-Filmkamera durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2162">Conversion is not made to the focal length of a 35 millimeter film camera.</span></span>



| <span data-ttu-id="d1e65-2163">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-2163">Property info</span></span> | <span data-ttu-id="d1e65-2164">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-2164">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="d1e65-2165">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-2165">Tag</span></span>   | <span data-ttu-id="d1e65-2166">0x920a</span><span class="sxs-lookup"><span data-stu-id="d1e65-2166">0x920A</span></span>                  |
| <span data-ttu-id="d1e65-2167">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-2167">Type</span></span>  | <span data-ttu-id="d1e65-2168">Propertytagtyperational</span><span class="sxs-lookup"><span data-stu-id="d1e65-2168">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="d1e65-2169">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-2169">Count</span></span> | <span data-ttu-id="d1e65-2170">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-2170">1</span></span>                       |



 

## <a name="propertytagexifmakernote"></a><span data-ttu-id="d1e65-2171">Propertytagexif Makernote</span><span class="sxs-lookup"><span data-stu-id="d1e65-2171">PropertyTagExifMakerNote</span></span>

<span data-ttu-id="d1e65-2172">Notiz Kennung.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2172">Note tag.</span></span> <span data-ttu-id="d1e65-2173">Ein Tag, das von Herstellern von EXIF-Writern verwendet wird, um Informationen aufzuzeichnen.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2173">A tag used by manufacturers of EXIF writers to record information.</span></span> <span data-ttu-id="d1e65-2174">Der Inhalt ist der Hersteller.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2174">The contents are up to the manufacturer.</span></span>



| <span data-ttu-id="d1e65-2175">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-2175">Property info</span></span> | <span data-ttu-id="d1e65-2176">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-2176">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="d1e65-2177">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-2177">Tag</span></span>   | <span data-ttu-id="d1e65-2178">0x927c</span><span class="sxs-lookup"><span data-stu-id="d1e65-2178">0x927C</span></span>                   |
| <span data-ttu-id="d1e65-2179">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-2179">Type</span></span>  | <span data-ttu-id="d1e65-2180">Propertytagtypeundefiniert</span><span class="sxs-lookup"><span data-stu-id="d1e65-2180">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="d1e65-2181">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-2181">Count</span></span> | <span data-ttu-id="d1e65-2182">Any</span><span class="sxs-lookup"><span data-stu-id="d1e65-2182">Any</span></span>                      |



 

## <a name="propertytagexifusercomment"></a><span data-ttu-id="d1e65-2183">Propertytagexifusercomment</span><span class="sxs-lookup"><span data-stu-id="d1e65-2183">PropertyTagExifUserComment</span></span>

<span data-ttu-id="d1e65-2184">Kommentartag.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2184">Comment tag.</span></span> <span data-ttu-id="d1e65-2185">Ein Tag, das von EXIF-Benutzern verwendet wird, um Schlüsselwörter oder Kommentare zu dem Bild zu schreiben, neben denen in propertytagimagedescription und ohne die Einschränkungen des Zeichen Codes des propertytagimagedescription-Tags.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2185">A tag used by EXIF users to write keywords or comments about the image besides those in PropertyTagImageDescription and without the character-code limitations of the PropertyTagImageDescription tag.</span></span>



| <span data-ttu-id="d1e65-2186">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-2186">Property info</span></span> | <span data-ttu-id="d1e65-2187">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-2187">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="d1e65-2188">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-2188">Tag</span></span>   | <span data-ttu-id="d1e65-2189">0x9286</span><span class="sxs-lookup"><span data-stu-id="d1e65-2189">0x9286</span></span>                   |
| <span data-ttu-id="d1e65-2190">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-2190">Type</span></span>  | <span data-ttu-id="d1e65-2191">Propertytagtypeundefiniert</span><span class="sxs-lookup"><span data-stu-id="d1e65-2191">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="d1e65-2192">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-2192">Count</span></span> | <span data-ttu-id="d1e65-2193">Any</span><span class="sxs-lookup"><span data-stu-id="d1e65-2193">Any</span></span>                      |



 

<span data-ttu-id="d1e65-2194">Der Zeichencode, der im propertytagexifusercomment-Tag verwendet wird, wird basierend auf einem ID-Code in einem fixierten 8-Byte-Bereich am Anfang des Tagdaten Bereichs identifiziert.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2194">The character code used in the PropertyTagExifUserComment tag is identified based on an ID code in a fixed 8-byte area at the start of the tag data area.</span></span> <span data-ttu-id="d1e65-2195">Der nicht verwendete Teil des Bereichs wird mit NULL Zeichen (0) aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2195">The unused portion of the area is padded with null characters (0).</span></span> <span data-ttu-id="d1e65-2196">ID-Codes werden mithilfe der Registrierung zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2196">ID codes are assigned by means of registration.</span></span> <span data-ttu-id="d1e65-2197">Da der Typ nicht ASCII ist, muss kein NULL-Terminator verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2197">Because the type is not ASCII, it is not necessary to use a NULL terminator.</span></span>

## <a name="propertytagexifdtsubsec"></a><span data-ttu-id="d1e65-2198">Propertytagexif-subsec</span><span class="sxs-lookup"><span data-stu-id="d1e65-2198">PropertyTagExifDTSubsec</span></span>

<span data-ttu-id="d1e65-2199">Mit NULL beendete Zeichenfolge, die einen Bruchteil einer Sekunde für das propertytagdatetime-Tag angibt.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2199">Null-terminated character string that specifies a fraction of a second for the PropertyTagDateTime tag.</span></span>



| <span data-ttu-id="d1e65-2200">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-2200">Property info</span></span> | <span data-ttu-id="d1e65-2201">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-2201">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="d1e65-2202">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-2202">Tag</span></span>   | <span data-ttu-id="d1e65-2203">0x9290</span><span class="sxs-lookup"><span data-stu-id="d1e65-2203">0x9290</span></span>                                             |
| <span data-ttu-id="d1e65-2204">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-2204">Type</span></span>  | <span data-ttu-id="d1e65-2205">Propertytagtybäuercii</span><span class="sxs-lookup"><span data-stu-id="d1e65-2205">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="d1e65-2206">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-2206">Count</span></span> | <span data-ttu-id="d1e65-2207">Länge der Zeichenfolge einschließlich des NULL-Terminator</span><span class="sxs-lookup"><span data-stu-id="d1e65-2207">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagexifdtorigss"></a><span data-ttu-id="d1e65-2208">Propertytagexisdtorigss</span><span class="sxs-lookup"><span data-stu-id="d1e65-2208">PropertyTagExifDTOrigSS</span></span>

<span data-ttu-id="d1e65-2209">Eine auf NULL endenden Zeichenfolge, die einen Bruchteil einer Sekunde für das propertytagexiatdtorig-Tag angibt.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2209">Null-terminated character string that specifies a fraction of a second for the PropertyTagExifDTOrig tag.</span></span>



| <span data-ttu-id="d1e65-2210">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-2210">Property info</span></span> | <span data-ttu-id="d1e65-2211">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-2211">Value</span></span> |
|------|----------------------------------------------------|
| <span data-ttu-id="d1e65-2212">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-2212">Tag</span></span>  | <span data-ttu-id="d1e65-2213">0x9291</span><span class="sxs-lookup"><span data-stu-id="d1e65-2213">0x9291</span></span>                                             |
| <span data-ttu-id="d1e65-2214">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-2214">Type</span></span> | <span data-ttu-id="d1e65-2215">Propertytagtybäuercii</span><span class="sxs-lookup"><span data-stu-id="d1e65-2215">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="d1e65-2216">N</span><span class="sxs-lookup"><span data-stu-id="d1e65-2216">N</span></span>    | <span data-ttu-id="d1e65-2217">Länge der Zeichenfolge einschließlich des NULL-Terminator</span><span class="sxs-lookup"><span data-stu-id="d1e65-2217">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagexifdtdigss"></a><span data-ttu-id="d1e65-2218">Propertytagexisdtdigss</span><span class="sxs-lookup"><span data-stu-id="d1e65-2218">PropertyTagExifDTDigSS</span></span>

<span data-ttu-id="d1e65-2219">Eine auf NULL endenden Zeichenfolge, die einen Bruchteil einer Sekunde für das propertytagexiatdtdigittag angibt.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2219">Null-terminated character string that specifies a fraction of a second for the PropertyTagExifDTDigitized tag.</span></span>



| <span data-ttu-id="d1e65-2220">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-2220">Property info</span></span> | <span data-ttu-id="d1e65-2221">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-2221">Value</span></span> |
|------|----------------------------------------------------|
| <span data-ttu-id="d1e65-2222">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-2222">Tag</span></span>  | <span data-ttu-id="d1e65-2223">0x9292</span><span class="sxs-lookup"><span data-stu-id="d1e65-2223">0x9292</span></span>                                             |
| <span data-ttu-id="d1e65-2224">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-2224">Type</span></span> | <span data-ttu-id="d1e65-2225">ASCII</span><span class="sxs-lookup"><span data-stu-id="d1e65-2225">ASCII</span></span>                                              |
| <span data-ttu-id="d1e65-2226">N</span><span class="sxs-lookup"><span data-stu-id="d1e65-2226">N</span></span>    | <span data-ttu-id="d1e65-2227">Länge der Zeichenfolge einschließlich des NULL-Terminator</span><span class="sxs-lookup"><span data-stu-id="d1e65-2227">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagexiffpxver"></a><span data-ttu-id="d1e65-2228">Propertytagexiffpxver</span><span class="sxs-lookup"><span data-stu-id="d1e65-2228">PropertyTagExifFPXVer</span></span>

<span data-ttu-id="d1e65-2229">Die von einer fpxr-Datei unterstützte Version des Flash-Formats.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2229">FlashPix format version supported by an FPXR file.</span></span> <span data-ttu-id="d1e65-2230">Wenn die fpxr-Funktion die Version 1,0 des Flash-Formats unterstützt, wird dies ähnlich wie bei propertytagexifver durch Aufzeichnen von 0100 als 4-Byte-ASCII-Zeichenfolge angegeben.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2230">If the FPXR function supports FlashPix format version 1.0, this is indicated similarly to PropertyTagExifVer by recording 0100 as a 4-byte ASCII string.</span></span> <span data-ttu-id="d1e65-2231">Da der Typ propertytagtypeundefiniert ist, ist kein NULL-Terminator vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2231">Because the type is PropertyTagTypeUndefined, there is no NULL terminator.</span></span>



<span data-ttu-id="d1e65-2232">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-2232">Tag</span></span>

<span data-ttu-id="d1e65-2233">0xa000</span><span class="sxs-lookup"><span data-stu-id="d1e65-2233">0xA000</span></span>

<span data-ttu-id="d1e65-2234">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-2234">Type</span></span>

<span data-ttu-id="d1e65-2235">Propertytagtypeundefiniert</span><span class="sxs-lookup"><span data-stu-id="d1e65-2235">PropertyTagTypeUndefined</span></span>

<span data-ttu-id="d1e65-2236">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-2236">Count</span></span>

<span data-ttu-id="d1e65-2237">4</span><span class="sxs-lookup"><span data-stu-id="d1e65-2237">4</span></span>

<span data-ttu-id="d1e65-2238">Standard</span><span class="sxs-lookup"><span data-stu-id="d1e65-2238">Default</span></span>

<span data-ttu-id="d1e65-2239">0100</span><span class="sxs-lookup"><span data-stu-id="d1e65-2239">0100</span></span>

<span data-ttu-id="d1e65-2240">0100-Flash-Format Version 1,0 andere-reserviert</span><span class="sxs-lookup"><span data-stu-id="d1e65-2240">0100 - FlashPix format version 1.0 Other - reserved</span></span>



 

## <a name="propertytagexifcolorspace"></a><span data-ttu-id="d1e65-2241">Propertytagexilecolorspace</span><span class="sxs-lookup"><span data-stu-id="d1e65-2241">PropertyTagExifColorSpace</span></span>

<span data-ttu-id="d1e65-2242">Farbleerraum-Spezifizierer.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2242">Color space specifier.</span></span> <span data-ttu-id="d1e65-2243">Normalerweise wird sRGB (= 1) verwendet, um den Farbraum basierend auf den PC-Monitor Bedingungen und der Umgebung zu definieren.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2243">Normally sRGB (=1) is used to define the color space based on the PC monitor conditions and environment.</span></span> <span data-ttu-id="d1e65-2244">Wenn ein anderer Farbraum als sRGB verwendet wird, wird unkalibriert (= 0xFFFF) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2244">If a color space other than sRGB is used, Uncalibrated (=0xFFFF) is set.</span></span> <span data-ttu-id="d1e65-2245">Bilddaten, die als nicht kalibriert aufgezeichnet werden, können bei der Konvertierung in "Flash" als sRGB behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2245">Image data recorded as Uncalibrated can be treated as sRGB when it is converted to FlashPix.</span></span>



<span data-ttu-id="d1e65-2246">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-2246">Tag</span></span>

<span data-ttu-id="d1e65-2247">0xa001</span><span class="sxs-lookup"><span data-stu-id="d1e65-2247">0xA001</span></span>

<span data-ttu-id="d1e65-2248">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-2248">Type</span></span>

<span data-ttu-id="d1e65-2249">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-2249">PropertyTagTypeShort</span></span>

<span data-ttu-id="d1e65-2250">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-2250">Count</span></span>

<span data-ttu-id="d1e65-2251">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-2251">1</span></span>

<span data-ttu-id="d1e65-2252">0x1-sRGB 0xFFFF-unkalibrierte andere-reserviert</span><span class="sxs-lookup"><span data-stu-id="d1e65-2252">0x1 - sRGB 0xFFFF - uncalibrated Other - reserved</span></span>



 

## <a name="propertytagexifpixxdim"></a><span data-ttu-id="d1e65-2253">Propertytagexif-xdim</span><span class="sxs-lookup"><span data-stu-id="d1e65-2253">PropertyTagExifPixXDim</span></span>

<span data-ttu-id="d1e65-2254">Informationen, die für komprimierte Daten spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2254">Information specific to compressed data.</span></span> <span data-ttu-id="d1e65-2255">Wenn eine komprimierte Datei aufgezeichnet wird, muss die gültige Breite des aussagekräftigen Bilds in diesem Tag aufgezeichnet werden, unabhängig davon, ob Auffüll Daten oder ein Neustart Marker vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2255">When a compressed file is recorded, the valid width of the meaningful image must be recorded in this tag, whether or not there is padding data or a restart marker.</span></span> <span data-ttu-id="d1e65-2256">Dieses Tag darf in einer nicht komprimierten Datei nicht vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2256">This tag should not exist in an uncompressed file.</span></span>



| <span data-ttu-id="d1e65-2257">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-2257">Property info</span></span> | <span data-ttu-id="d1e65-2258">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-2258">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="d1e65-2259">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-2259">Tag</span></span>   | <span data-ttu-id="d1e65-2260">0xa002</span><span class="sxs-lookup"><span data-stu-id="d1e65-2260">0xA002</span></span>                                      |
| <span data-ttu-id="d1e65-2261">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-2261">Type</span></span>  | <span data-ttu-id="d1e65-2262">Propertytagtypeshort oder propertytagtypelong</span><span class="sxs-lookup"><span data-stu-id="d1e65-2262">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="d1e65-2263">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-2263">Count</span></span> | <span data-ttu-id="d1e65-2264">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-2264">1</span></span>                                           |



 

## <a name="propertytagexifpixydim"></a><span data-ttu-id="d1e65-2265">Propertytagexif pixydim</span><span class="sxs-lookup"><span data-stu-id="d1e65-2265">PropertyTagExifPixYDim</span></span>

<span data-ttu-id="d1e65-2266">Informationen, die für komprimierte Daten spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2266">Information specific to compressed data.</span></span> <span data-ttu-id="d1e65-2267">Wenn eine komprimierte Datei aufgezeichnet wird, muss die gültige Höhe des sinnvollen Bilds in diesem Tag aufgezeichnet werden, unabhängig davon, ob Auffüll Daten oder ein Neustart Marker vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2267">When a compressed file is recorded, the valid height of the meaningful image must be recorded in this tag whether or not there is padding data or a restart marker.</span></span> <span data-ttu-id="d1e65-2268">Dieses Tag darf in einer nicht komprimierten Datei nicht vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2268">This tag should not exist in an uncompressed file.</span></span> <span data-ttu-id="d1e65-2269">Da das Auffüllen von Daten in vertikaler Richtung unnötig ist, ist die Anzahl von Zeilen, die in diesem gültigen Image Height-Tag aufgezeichnet werden, identisch mit der in SOF aufgezeichneten.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2269">Because data padding is unnecessary in the vertical direction, the number of lines recorded in this valid image height tag will be the same as that recorded in the SOF.</span></span>



| <span data-ttu-id="d1e65-2270">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-2270">Property info</span></span> | <span data-ttu-id="d1e65-2271">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-2271">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="d1e65-2272">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-2272">Tag</span></span>   | <span data-ttu-id="d1e65-2273">0xa003</span><span class="sxs-lookup"><span data-stu-id="d1e65-2273">0xA003</span></span>                                      |
| <span data-ttu-id="d1e65-2274">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-2274">Type</span></span>  | <span data-ttu-id="d1e65-2275">Propertytagtypeshort oder propertytagtypelong</span><span class="sxs-lookup"><span data-stu-id="d1e65-2275">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="d1e65-2276">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-2276">Count</span></span> | <span data-ttu-id="d1e65-2277">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-2277">1</span></span>                                           |



 

## <a name="propertytagexifrelatedwav"></a><span data-ttu-id="d1e65-2278">Propertytagexifrelatedwav</span><span class="sxs-lookup"><span data-stu-id="d1e65-2278">PropertyTagExifRelatedWav</span></span>

<span data-ttu-id="d1e65-2279">Der Name einer Audiodatei, die sich auf die Bilddaten bezieht.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2279">The name of an audio file related to the image data.</span></span> <span data-ttu-id="d1e65-2280">Die einzigen als relationalen Informationen aufgezeichneten Informationen sind der Name und die Erweiterung der EXIF-Audiodatei (eine ASCII-Zeichenfolge, die aus 8 Zeichen plus einem Zeitraum (.) und 3 Zeichen besteht).</span><span class="sxs-lookup"><span data-stu-id="d1e65-2280">The only relational information recorded is the EXIF audio file name and extension (an ASCII string that consists of 8 characters plus a period (.), plus 3 characters).</span></span> <span data-ttu-id="d1e65-2281">Der Pfad wird nicht aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2281">The path is not recorded.</span></span> <span data-ttu-id="d1e65-2282">Wenn Sie dieses Tag verwenden, müssen Audiodateien in Übereinstimmung mit dem EXIF-Audioformat aufgezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2282">When you use this tag, audio files must be recorded in conformance with the EXIF audio format.</span></span> <span data-ttu-id="d1e65-2283">Writer können auch Audiodaten innerhalb von APP2 als Daten des Flash-Erweiterungs Datenstroms speichern.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2283">Writers can also store audio data within APP2 as FlashPix extension stream data.</span></span>



| <span data-ttu-id="d1e65-2284">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-2284">Property info</span></span> | <span data-ttu-id="d1e65-2285">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-2285">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="d1e65-2286">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-2286">Tag</span></span>   | <span data-ttu-id="d1e65-2287">0xa004</span><span class="sxs-lookup"><span data-stu-id="d1e65-2287">0xA004</span></span>               |
| <span data-ttu-id="d1e65-2288">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-2288">Type</span></span>  | <span data-ttu-id="d1e65-2289">Propertytagtybäuercii</span><span class="sxs-lookup"><span data-stu-id="d1e65-2289">PropertyTagTypeASCII</span></span> |
| <span data-ttu-id="d1e65-2290">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-2290">Count</span></span> | <span data-ttu-id="d1e65-2291">13</span><span class="sxs-lookup"><span data-stu-id="d1e65-2291">13</span></span>                   |



 

## <a name="propertytagexifinterop"></a><span data-ttu-id="d1e65-2292">Propertytagexifinterop</span><span class="sxs-lookup"><span data-stu-id="d1e65-2292">PropertyTagExifInterop</span></span>

<span data-ttu-id="d1e65-2293">Offset zu einem Block von Eigenschafts Elementen, die Interoperabilitäts Informationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2293">Offset to a block of property items that contain interoperability information.</span></span>



| <span data-ttu-id="d1e65-2294">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-2294">Property info</span></span> | <span data-ttu-id="d1e65-2295">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-2295">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="d1e65-2296">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-2296">Tag</span></span>   | <span data-ttu-id="d1e65-2297">0xa005</span><span class="sxs-lookup"><span data-stu-id="d1e65-2297">0xA005</span></span>              |
| <span data-ttu-id="d1e65-2298">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-2298">Type</span></span>  | <span data-ttu-id="d1e65-2299">Propertytagtypelong</span><span class="sxs-lookup"><span data-stu-id="d1e65-2299">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="d1e65-2300">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-2300">Count</span></span> | <span data-ttu-id="d1e65-2301">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-2301">1</span></span>                   |



 

## <a name="propertytagexifflashenergy"></a><span data-ttu-id="d1e65-2302">Propertytagexifflashenergy</span><span class="sxs-lookup"><span data-stu-id="d1e65-2302">PropertyTagExifFlashEnergy</span></span>

<span data-ttu-id="d1e65-2303">Strobe Energy, in Beam Kerzen Power seconds (BCPS), zu dem Zeitpunkt, als das Image aufgezeichnet wurde.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2303">Strobe energy, in Beam Candle Power Seconds (BCPS), at the time the image was captured.</span></span>



| <span data-ttu-id="d1e65-2304">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-2304">Property info</span></span> | <span data-ttu-id="d1e65-2305">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-2305">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="d1e65-2306">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-2306">Tag</span></span>   | <span data-ttu-id="d1e65-2307">0xa20b</span><span class="sxs-lookup"><span data-stu-id="d1e65-2307">0xA20B</span></span>                  |
| <span data-ttu-id="d1e65-2308">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-2308">Type</span></span>  | <span data-ttu-id="d1e65-2309">Propertytagtyperational</span><span class="sxs-lookup"><span data-stu-id="d1e65-2309">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="d1e65-2310">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-2310">Count</span></span> | <span data-ttu-id="d1e65-2311">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-2311">1</span></span>                       |



 

## <a name="propertytagexifspatialfr"></a><span data-ttu-id="d1e65-2312">Propertytagexilespatialfr</span><span class="sxs-lookup"><span data-stu-id="d1e65-2312">PropertyTagExifSpatialFR</span></span>

<span data-ttu-id="d1e65-2313">Die Tabelle für die räumliche Häufigkeit der Kamera-oder Eingabegeräte und die Werte in der Bildbreite, Bildhöhe und Diagonal Richtung, wie in ISO 12233 angegeben.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2313">Camera or input device spatial frequency table and SFR values in the image width, image height, and diagonal direction, as specified in ISO 12233.</span></span>



| <span data-ttu-id="d1e65-2314">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-2314">Property info</span></span> | <span data-ttu-id="d1e65-2315">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-2315">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="d1e65-2316">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-2316">Tag</span></span>   | <span data-ttu-id="d1e65-2317">0xa20c</span><span class="sxs-lookup"><span data-stu-id="d1e65-2317">0xA20C</span></span>                   |
| <span data-ttu-id="d1e65-2318">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-2318">Type</span></span>  | <span data-ttu-id="d1e65-2319">Propertytagtypeundefiniert</span><span class="sxs-lookup"><span data-stu-id="d1e65-2319">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="d1e65-2320">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-2320">Count</span></span> | <span data-ttu-id="d1e65-2321">Any</span><span class="sxs-lookup"><span data-stu-id="d1e65-2321">Any</span></span>                      |



 

## <a name="propertytagexiffocalxres"></a><span data-ttu-id="d1e65-2322">Propertytagexiffocalxres</span><span class="sxs-lookup"><span data-stu-id="d1e65-2322">PropertyTagExifFocalXRes</span></span>

<span data-ttu-id="d1e65-2323">Die Anzahl der Pixel in der Bild breiten Richtung (x) pro Einheit auf der Kamera-Fokusebene.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2323">Number of pixels in the image width (x) direction per unit on the camera focal plane.</span></span> <span data-ttu-id="d1e65-2324">Die Einheit wird in propertytagexiffocalresunit angegeben.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2324">The unit is specified in PropertyTagExifFocalResUnit.</span></span>



| <span data-ttu-id="d1e65-2325">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-2325">Property info</span></span> | <span data-ttu-id="d1e65-2326">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-2326">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="d1e65-2327">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-2327">Tag</span></span>   | <span data-ttu-id="d1e65-2328">0xa20e</span><span class="sxs-lookup"><span data-stu-id="d1e65-2328">0xA20E</span></span>                  |
| <span data-ttu-id="d1e65-2329">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-2329">Type</span></span>  | <span data-ttu-id="d1e65-2330">Propertytagtyperational</span><span class="sxs-lookup"><span data-stu-id="d1e65-2330">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="d1e65-2331">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-2331">Count</span></span> | <span data-ttu-id="d1e65-2332">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-2332">1</span></span>                       |



 

## <a name="propertytagexiffocalyres"></a><span data-ttu-id="d1e65-2333">Propertytagexiffocalyres</span><span class="sxs-lookup"><span data-stu-id="d1e65-2333">PropertyTagExifFocalYRes</span></span>

<span data-ttu-id="d1e65-2334">Die Anzahl der Pixel in der Bildhöhe (y)-Richtung pro Einheit auf der Kamera-Fokusebene.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2334">Number of pixels in the image height (y) direction per unit on the camera focal plane.</span></span> <span data-ttu-id="d1e65-2335">Die Einheit wird in propertytagexiffocalresunit angegeben.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2335">The unit is specified in PropertyTagExifFocalResUnit.</span></span>



| <span data-ttu-id="d1e65-2336">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-2336">Property info</span></span> | <span data-ttu-id="d1e65-2337">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-2337">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="d1e65-2338">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-2338">Tag</span></span>   | <span data-ttu-id="d1e65-2339">0xa20f</span><span class="sxs-lookup"><span data-stu-id="d1e65-2339">0xA20F</span></span>                  |
| <span data-ttu-id="d1e65-2340">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-2340">Type</span></span>  | <span data-ttu-id="d1e65-2341">Propertytagtyperational</span><span class="sxs-lookup"><span data-stu-id="d1e65-2341">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="d1e65-2342">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-2342">Count</span></span> | <span data-ttu-id="d1e65-2343">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-2343">1</span></span>                       |



 

## <a name="propertytagexiffocalresunit"></a><span data-ttu-id="d1e65-2344">Propertytagexiffocalresunit</span><span class="sxs-lookup"><span data-stu-id="d1e65-2344">PropertyTagExifFocalResUnit</span></span>

<span data-ttu-id="d1e65-2345">Maßeinheit für propertytagexiffocalxres und propertytagexiffocalyres.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2345">Unit of measure for PropertyTagExifFocalXRes and PropertyTagExifFocalYRes.</span></span>



<span data-ttu-id="d1e65-2346">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-2346">Tag</span></span>

<span data-ttu-id="d1e65-2347">0xa210</span><span class="sxs-lookup"><span data-stu-id="d1e65-2347">0xA210</span></span>

<span data-ttu-id="d1e65-2348">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-2348">Type</span></span>

<span data-ttu-id="d1e65-2349">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-2349">PropertyTagTypeShort</span></span>

<span data-ttu-id="d1e65-2350">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-2350">Count</span></span>

<span data-ttu-id="d1e65-2351">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-2351">1</span></span>

<span data-ttu-id="d1e65-2352">2 Zoll, 3 Zentimeter</span><span class="sxs-lookup"><span data-stu-id="d1e65-2352">2 - inch 3 - centimeter</span></span>



 

## <a name="propertytagexifsubjectloc"></a><span data-ttu-id="d1e65-2353">Propertytagexilosubjetloc</span><span class="sxs-lookup"><span data-stu-id="d1e65-2353">PropertyTagExifSubjectLoc</span></span>

<span data-ttu-id="d1e65-2354">Speicherort des Haupt Subjekts in der Szene.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2354">Location of the main subject in the scene.</span></span> <span data-ttu-id="d1e65-2355">Der Wert dieses Tags stellt das Pixel in der Mitte des Haupt Subjekts relativ zum linken Rand dar.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2355">The value of this tag represents the pixel at the center of the main subject relative to the left edge.</span></span> <span data-ttu-id="d1e65-2356">Der erste Wert gibt die Spaltennummer an, und der zweite Wert gibt die Zeilennummer an.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2356">The first value indicates the column number, and the second value indicates the row number.</span></span>



| <span data-ttu-id="d1e65-2357">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-2357">Property info</span></span> | <span data-ttu-id="d1e65-2358">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-2358">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="d1e65-2359">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-2359">Tag</span></span>   | <span data-ttu-id="d1e65-2360">0xa214</span><span class="sxs-lookup"><span data-stu-id="d1e65-2360">0xA214</span></span>               |
| <span data-ttu-id="d1e65-2361">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-2361">Type</span></span>  | <span data-ttu-id="d1e65-2362">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-2362">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="d1e65-2363">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-2363">Count</span></span> | <span data-ttu-id="d1e65-2364">2</span><span class="sxs-lookup"><span data-stu-id="d1e65-2364">2</span></span>                    |



 

## <a name="propertytagexifexposureindex"></a><span data-ttu-id="d1e65-2365">Propertytagexif exposureindex</span><span class="sxs-lookup"><span data-stu-id="d1e65-2365">PropertyTagExifExposureIndex</span></span>

<span data-ttu-id="d1e65-2366">Der auf der Kamera oder dem Eingabegerät zum Zeitpunkt der Erfassung des Abbilds ausgewählte Expositions Index.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2366">Exposure index selected on the camera or input device at the time the image was captured.</span></span>



| <span data-ttu-id="d1e65-2367">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-2367">Property info</span></span> | <span data-ttu-id="d1e65-2368">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-2368">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="d1e65-2369">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-2369">Tag</span></span>   | <span data-ttu-id="d1e65-2370">0xa215</span><span class="sxs-lookup"><span data-stu-id="d1e65-2370">0xA215</span></span>                  |
| <span data-ttu-id="d1e65-2371">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-2371">Type</span></span>  | <span data-ttu-id="d1e65-2372">Propertytagtyperational</span><span class="sxs-lookup"><span data-stu-id="d1e65-2372">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="d1e65-2373">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-2373">Count</span></span> | <span data-ttu-id="d1e65-2374">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-2374">1</span></span>                       |



 

## <a name="propertytagexifsensingmethod"></a><span data-ttu-id="d1e65-2375">Propertytagexif-singmethod</span><span class="sxs-lookup"><span data-stu-id="d1e65-2375">PropertyTagExifSensingMethod</span></span>

<span data-ttu-id="d1e65-2376">Bild Sensortyp auf der Kamera oder dem Eingabegerät.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2376">Image sensor type on the camera or input device.</span></span>



<span data-ttu-id="d1e65-2377">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-2377">Tag</span></span>

<span data-ttu-id="d1e65-2378">0xa217</span><span class="sxs-lookup"><span data-stu-id="d1e65-2378">0xA217</span></span>

<span data-ttu-id="d1e65-2379">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-2379">Type</span></span>

<span data-ttu-id="d1e65-2380">Propertytagtypeshort</span><span class="sxs-lookup"><span data-stu-id="d1e65-2380">PropertyTagTypeShort</span></span>

<span data-ttu-id="d1e65-2381">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-2381">Count</span></span>

<span data-ttu-id="d1e65-2382">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-2382">1</span></span>

<span data-ttu-id="d1e65-2383">1: nicht definiert 2-One-Chip-Farbbereichs Sensor 3-zwei-Chip-Farbbereichs Sensor 4-drei-Chip-Farbbereichs Sensor 5-farbige sequenzieller Bereichs Sensor 7-zweilinearer Sensor 8-farbig sequenzieller linearer Sensor-reserviert</span><span class="sxs-lookup"><span data-stu-id="d1e65-2383">1 - not defined 2 - one-chip color area sensor 3 - two-chip color area sensor 4 - three-chip color area sensor 5 - color sequential area sensor 7 - trilinear sensor 8 - color sequential linear sensor Other - reserved</span></span>



 

## <a name="propertytagexiffilesource"></a><span data-ttu-id="d1e65-2384">Propertytagexiffilesource</span><span class="sxs-lookup"><span data-stu-id="d1e65-2384">PropertyTagExifFileSource</span></span>

<span data-ttu-id="d1e65-2385">Die Bildquelle.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2385">The image source.</span></span> <span data-ttu-id="d1e65-2386">Wenn ein DSC das Image aufgezeichnet hat, ist der Wert dieses Tags 3.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2386">If a DSC recorded the image, the value of this tag is 3.</span></span>



| <span data-ttu-id="d1e65-2387">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-2387">Property info</span></span> | <span data-ttu-id="d1e65-2388">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-2388">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="d1e65-2389">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-2389">Tag</span></span>   | <span data-ttu-id="d1e65-2390">0xa300</span><span class="sxs-lookup"><span data-stu-id="d1e65-2390">0xA300</span></span>                   |
| <span data-ttu-id="d1e65-2391">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-2391">Type</span></span>  | <span data-ttu-id="d1e65-2392">Propertytagtypeundefiniert</span><span class="sxs-lookup"><span data-stu-id="d1e65-2392">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="d1e65-2393">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-2393">Count</span></span> | <span data-ttu-id="d1e65-2394">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-2394">1</span></span>                        |



 

## <a name="propertytagexifscenetype"></a><span data-ttu-id="d1e65-2395">Propertytagexilescenetype</span><span class="sxs-lookup"><span data-stu-id="d1e65-2395">PropertyTagExifSceneType</span></span>

<span data-ttu-id="d1e65-2396">Der Typ der Szene.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2396">The type of scene.</span></span> <span data-ttu-id="d1e65-2397">Wenn ein DSC das Image aufgezeichnet hat, muss der Wert dieses Tags auf 1 festgelegt werden, um anzugeben, dass das Bild direkt fotografiert wurde.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2397">If a DSC recorded the image, the value of this tag must be set to 1, indicating that the image was directly photographed.</span></span>



| <span data-ttu-id="d1e65-2398">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-2398">Property info</span></span> | <span data-ttu-id="d1e65-2399">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-2399">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="d1e65-2400">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-2400">Tag</span></span>   | <span data-ttu-id="d1e65-2401">0xa301</span><span class="sxs-lookup"><span data-stu-id="d1e65-2401">0xA301</span></span>                   |
| <span data-ttu-id="d1e65-2402">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-2402">Type</span></span>  | <span data-ttu-id="d1e65-2403">Propertytagtypeundefiniert</span><span class="sxs-lookup"><span data-stu-id="d1e65-2403">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="d1e65-2404">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-2404">Count</span></span> | <span data-ttu-id="d1e65-2405">1</span><span class="sxs-lookup"><span data-stu-id="d1e65-2405">1</span></span>                        |



 

## <a name="propertytagexifcfapattern"></a><span data-ttu-id="d1e65-2406">Propertytagexifcfapattern</span><span class="sxs-lookup"><span data-stu-id="d1e65-2406">PropertyTagExifCfaPattern</span></span>

<span data-ttu-id="d1e65-2407">Das geometrische Muster des Farbfilter Arrays (CFA) des Bildsensors, wenn ein One-Chip-Farbbereichs Sensor verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2407">The color filter array (CFA) geometric pattern of the image sensor when a one-chip color area sensor is used.</span></span> <span data-ttu-id="d1e65-2408">Es gilt nicht für alle Methoden zur Erkennung.</span><span class="sxs-lookup"><span data-stu-id="d1e65-2408">It does not apply to all sensing methods.</span></span>



| <span data-ttu-id="d1e65-2409">Eigenschafts Informationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-2409">Property info</span></span> | <span data-ttu-id="d1e65-2410">Wert</span><span class="sxs-lookup"><span data-stu-id="d1e65-2410">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="d1e65-2411">Tag</span><span class="sxs-lookup"><span data-stu-id="d1e65-2411">Tag</span></span>   | <span data-ttu-id="d1e65-2412">0xa302</span><span class="sxs-lookup"><span data-stu-id="d1e65-2412">0xA302</span></span>                   |
| <span data-ttu-id="d1e65-2413">type</span><span class="sxs-lookup"><span data-stu-id="d1e65-2413">Type</span></span>  | <span data-ttu-id="d1e65-2414">Propertytagtypeundefiniert</span><span class="sxs-lookup"><span data-stu-id="d1e65-2414">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="d1e65-2415">Anzahl</span><span class="sxs-lookup"><span data-stu-id="d1e65-2415">Count</span></span> | <span data-ttu-id="d1e65-2416">Any</span><span class="sxs-lookup"><span data-stu-id="d1e65-2416">Any</span></span>                      |



 

## <a name="related-topics"></a><span data-ttu-id="d1e65-2417">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d1e65-2417">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1e65-2418">Image File Format-Spezifikationen</span><span class="sxs-lookup"><span data-stu-id="d1e65-2418">Image File Format Specifications</span></span>](-gdiplus-constant-image-file-format-specifications.md)
</dt> <dt>

[<span data-ttu-id="d1e65-2419">Bildeigenschaften-tagkonstanten</span><span class="sxs-lookup"><span data-stu-id="d1e65-2419">Image Property Tag Constants</span></span>](-gdiplus-constant-image-property-tag-constants.md)
</dt> <dt>

[<span data-ttu-id="d1e65-2420">**Bildeigenschaften-Tagtyp Konstanten**</span><span class="sxs-lookup"><span data-stu-id="d1e65-2420">**Image Property Tag Type Constants**</span></span>](-gdiplus-constant-image-property-tag-type-constants.md)
</dt> <dt>

[<span data-ttu-id="d1e65-2421">Eigenschaften Tags in alphabetischer Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="d1e65-2421">Property Tags in Alphabetical Order</span></span>](-gdiplus-constant-property-tags-in-alphabetical-order.md)
</dt> <dt>

[<span data-ttu-id="d1e65-2422">Eigenschaften Tags in numerischer Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="d1e65-2422">Property Tags in Numerical Order</span></span>](-gdiplus-constant-property-tags-in-numerical-order.md)
</dt> <dt>

[<span data-ttu-id="d1e65-2423">Lesen und Schreiben von Metadaten</span><span class="sxs-lookup"><span data-stu-id="d1e65-2423">Reading and Writing Metadata</span></span>](-gdiplus-reading-and-writing-metadata-use.md)
</dt> </dl>

 

 



