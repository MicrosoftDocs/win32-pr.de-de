---
description: Zeilen 21-Decoderfilter
ms.assetid: 48fa5484-1f8c-4133-b2e1-888cb1834402
title: Zeilen 21-Decoderfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 839a6ff8e77f4815b74f5de65b8f0e2a565cdc2a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344318"
---
# <a name="line-21-decoder-filter"></a><span data-ttu-id="63108-103">Zeilen 21-Decoderfilter</span><span class="sxs-lookup"><span data-stu-id="63108-103">Line 21 Decoder Filter</span></span>

<span data-ttu-id="63108-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="63108-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="63108-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="63108-105">It may be altered or unavailable in subsequent versions.</span></span>

<span data-ttu-id="63108-106">Dieser Zeile 21-Decoderfilter decodiert Daten der Zeile 21 und zeichnet den Beschriftungs Text auf Bitmaps.</span><span class="sxs-lookup"><span data-stu-id="63108-106">This Line 21 Decoder filter decodes line 21 data and draws the caption text onto bitmaps.</span></span>

<span data-ttu-id="63108-107">Die eingabepin stellt eine Verbindung mit einem beliebigen Zeilen 21-Datenanbieter her, in der Regel entweder ein DVD-Video Decoder oder der [CC-Decoder](cc-decoder-filter.md)</span><span class="sxs-lookup"><span data-stu-id="63108-107">The input pin connects to any line 21 data provider, typically either a DVD video decoder or the [CC Decoder](cc-decoder-filter.md) filter.</span></span> <span data-ttu-id="63108-108">Der CC-Decoder stellt Zeilen 21-Daten aus der VBI eines analogen Fernsehsignals bereit.</span><span class="sxs-lookup"><span data-stu-id="63108-108">The CC Decoder provides line 21 data from the VBI of an analog television signal.</span></span> <span data-ttu-id="63108-109">Die Ausgabepin stellt eine Verbindung mit einer sekundären PIN auf dem [Overlay-Mixer](overlay-mixer-filter.md) oder einem anderen Videorenderer her, z. b. VMR.</span><span class="sxs-lookup"><span data-stu-id="63108-109">The output pin connects to a secondary pin on the [Overlay Mixer](overlay-mixer-filter.md) or to another video renderer, such as the VMR.</span></span>

<span data-ttu-id="63108-110">Dieser Filter akzeptiert Zeile 21-Daten im Standard Byte-paar-Format oder als Paket für die ganze Gruppe von Bildern (GOP) als Paket.</span><span class="sxs-lookup"><span data-stu-id="63108-110">This filter accepts line 21 data in the standard byte-pair format or, for DVD, as a packet for the whole group of pictures (GOP).</span></span> <span data-ttu-id="63108-111">Für jeden GOP im DVD-Videodaten Strom kann ein Benutzerdaten Paket vorhanden sein, das über die Header Informationen des jeweiligen GOP und die Zeile 21 verfügt.</span><span class="sxs-lookup"><span data-stu-id="63108-111">For every GOP in the DVD video stream, there can be a user data packet that has that particular GOP's header information and line 21 data.</span></span> <span data-ttu-id="63108-112">Das Format der Byte-Paare wird im Standardwert von "EIA/CEA-608-B" definiert. Weitere Informationen finden Sie unter diesem Standard.</span><span class="sxs-lookup"><span data-stu-id="63108-112">The format of the byte pairs is defined in the EIA/CEA-608-B standard; please refer to that standard for more information.</span></span>

<span data-ttu-id="63108-113">Zwei Versionen dieses Filters sind verfügbar:</span><span class="sxs-lookup"><span data-stu-id="63108-113">Two versions of this filter are available:</span></span>



| <span data-ttu-id="63108-114">Filter</span><span class="sxs-lookup"><span data-stu-id="63108-114">Filter</span></span>            | <span data-ttu-id="63108-115">CLSID</span><span class="sxs-lookup"><span data-stu-id="63108-115">CLSID</span></span>                 |
|-------------------|-----------------------|
| <span data-ttu-id="63108-116">Zeile 21-Decoder</span><span class="sxs-lookup"><span data-stu-id="63108-116">Line 21 Decoder</span></span>   | <span data-ttu-id="63108-117">CLSID- \_ Line21Decoder</span><span class="sxs-lookup"><span data-stu-id="63108-117">CLSID\_Line21Decoder</span></span>  |
| <span data-ttu-id="63108-118">Zeile 21-Decoder 2</span><span class="sxs-lookup"><span data-stu-id="63108-118">Line 21 Decoder 2</span></span> | <span data-ttu-id="63108-119">CLSID- \_ Line21Decoder2</span><span class="sxs-lookup"><span data-stu-id="63108-119">CLSID\_Line21Decoder2</span></span> |



 

<span data-ttu-id="63108-120">Der Filter Version 1 wird auf den Plattformen Microsoft® Windows® 95/98/Me und Windows 2000 verwendet.</span><span class="sxs-lookup"><span data-stu-id="63108-120">The version 1 filter is used on Microsoft® Windows® 95/98/Me and Windows 2000 platforms.</span></span> <span data-ttu-id="63108-121">Der Filter Version 2 ist in Microsoft Windows XP und höher verfügbar und wird immer dann verwendet, wenn der Video Mischungs-Renderer im Diagramm angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="63108-121">The version 2 filter is available in Microsoft Windows XP and later, and is used whenever the Video Mixing Renderer is in the graph.</span></span>

<span data-ttu-id="63108-122">Die Informationen in der folgenden Tabelle gelten für beide Versionen des Filters:</span><span class="sxs-lookup"><span data-stu-id="63108-122">The information in the following table applies to both versions of the filter:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="63108-123">Filter Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="63108-123">Filter Interfaces</span></span></td>
<td><span data-ttu-id="63108-124"><a href="/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder"><strong>IAMLine21Decoder</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"> <strong>ibasefilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="63108-124"><a href="/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder"><strong>IAMLine21Decoder</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63108-125">Eingabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="63108-125">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="63108-126">Haupttyp: MEDIATYPE_AUXLine21DataSubtype:</span><span class="sxs-lookup"><span data-stu-id="63108-126">Major Type: MEDIATYPE_AUXLine21DataSubtype:</span></span><br/>
<ul>
<li><span data-ttu-id="63108-127">MEDIASUBTYPE_Line21_BytePair (Standardzeile 21)</span><span class="sxs-lookup"><span data-stu-id="63108-127">MEDIASUBTYPE_Line21_BytePair (standard line 21)</span></span></li>
<li><span data-ttu-id="63108-128">MEDIASUBTYPE_Line21_GOPPacket (DVD-Zeile 21)</span><span class="sxs-lookup"><span data-stu-id="63108-128">MEDIASUBTYPE_Line21_GOPPacket (DVD line 21)</span></span></li>
</ul>
<span data-ttu-id="63108-129">Formattyp: FORMAT_VideoInfo oder GUID_NULL</span><span class="sxs-lookup"><span data-stu-id="63108-129">Format Type: FORMAT_VideoInfo or GUID_NULL</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63108-130">PIN-Eingabeschnittstellen</span><span class="sxs-lookup"><span data-stu-id="63108-130">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="63108-131"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>iqualitycontrol</strong></a></span><span class="sxs-lookup"><span data-stu-id="63108-131"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63108-132">Ausgabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="63108-132">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="63108-133">Haupttyp: MEDIATYPE_VideoSubtype:</span><span class="sxs-lookup"><span data-stu-id="63108-133">Major type: MEDIATYPE_VideoSubtype:</span></span><br/>
<ul>
<li><span data-ttu-id="63108-134">MEDIASUBTYPE_RGB8</span><span class="sxs-lookup"><span data-stu-id="63108-134">MEDIASUBTYPE_RGB8</span></span></li>
<li><span data-ttu-id="63108-135">MEDIASUBTYPE_RGB555</span><span class="sxs-lookup"><span data-stu-id="63108-135">MEDIASUBTYPE_RGB555</span></span></li>
<li><span data-ttu-id="63108-136">MEDIASUBTYPE_RGB565</span><span class="sxs-lookup"><span data-stu-id="63108-136">MEDIASUBTYPE_RGB565</span></span></li>
<li><span data-ttu-id="63108-137">MEDIASUBTYPE_RGB24</span><span class="sxs-lookup"><span data-stu-id="63108-137">MEDIASUBTYPE_RGB24</span></span></li>
<li><span data-ttu-id="63108-138">MEDIASUBTYPE_RGB32</span><span class="sxs-lookup"><span data-stu-id="63108-138">MEDIASUBTYPE_RGB32</span></span></li>
</ul>
<span data-ttu-id="63108-139">Formattyp: FORMAT_VideoInfo</span><span class="sxs-lookup"><span data-stu-id="63108-139">Format Type: FORMAT_VideoInfo</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63108-140">PIN-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="63108-140">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="63108-141"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>Imediaposition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>imediaseeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>iqualitycontrol</strong></a></span><span class="sxs-lookup"><span data-stu-id="63108-141"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63108-142">CLSID Filtern</span><span class="sxs-lookup"><span data-stu-id="63108-142">Filter CLSID</span></span></td>
<td><span data-ttu-id="63108-143">Siehe vorherige Tabelle</span><span class="sxs-lookup"><span data-stu-id="63108-143">See previous table</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63108-144">CLSID der Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="63108-144">Property Page CLSID</span></span></td>
<td><span data-ttu-id="63108-145">Keine</span><span class="sxs-lookup"><span data-stu-id="63108-145">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63108-146">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="63108-146">Executable</span></span></td>
<td><span data-ttu-id="63108-147">qdvd.dll</span><span class="sxs-lookup"><span data-stu-id="63108-147">qdvd.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="63108-148"><a href="merit.md">Verdienst</a></span><span class="sxs-lookup"><span data-stu-id="63108-148"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="63108-149">Zeile 21-Decoder: MERIT_NORMALLine 21 Decoder 2: MERIT_NORMAL + 2</span><span class="sxs-lookup"><span data-stu-id="63108-149">Line 21 Decoder: MERIT_NORMALLine 21 Decoder 2: MERIT_NORMAL + 2</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="63108-150"><a href="filter-categories.md">Filter Kategorie</a></span><span class="sxs-lookup"><span data-stu-id="63108-150"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="63108-151">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="63108-151">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="63108-152">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="63108-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63108-153">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="63108-153">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="63108-154">Untertitel und Teletext</span><span class="sxs-lookup"><span data-stu-id="63108-154">Closed Captions and Teletext</span></span>](closed-captions-and-teletext.md)
</dt> <dt>

[<span data-ttu-id="63108-155">Konfiguration des DVD-Filter Diagramms</span><span class="sxs-lookup"><span data-stu-id="63108-155">DVD Filter Graph Configuration</span></span>](dvd-filter-graph-configuration.md)
</dt> </dl>

 

 




