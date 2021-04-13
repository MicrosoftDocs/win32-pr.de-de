---
description: In den folgenden Tabellen sind die CLSIDs für die DirectShow-Filter Kategorien aufgeführt.
ms.assetid: cab4e2c9-eab9-4836-adfc-870490ca5b6b
title: Filter Kategorien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0c4ccb9443c405abcbd0b9afbd406d6faf2558a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392367"
---
# <a name="filter-categories"></a><span data-ttu-id="1e7a0-103">Filter Kategorien</span><span class="sxs-lookup"><span data-stu-id="1e7a0-103">Filter Categories</span></span>

<span data-ttu-id="1e7a0-104">In den folgenden Tabellen sind die CLSIDs für die DirectShow-Filter Kategorien aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="1e7a0-104">The following tables list the CLSIDs for the DirectShow filter categories.</span></span>

-   [<span data-ttu-id="1e7a0-105">DirectShow-Filter Kategorien</span><span class="sxs-lookup"><span data-stu-id="1e7a0-105">DirectShow Filter Categories</span></span>](#directshow-filter-categories)
-   [<span data-ttu-id="1e7a0-106">Weitere Filter Kategorien</span><span class="sxs-lookup"><span data-stu-id="1e7a0-106">Other Filter Categories</span></span>](#other-filter-categories)
-   [<span data-ttu-id="1e7a0-107">DirectShow-Filter-metakategorie</span><span class="sxs-lookup"><span data-stu-id="1e7a0-107">DirectShow Filter Meta-Category</span></span>](#directshow-filter-meta-category)
-   [<span data-ttu-id="1e7a0-108">DMO-Kategorien</span><span class="sxs-lookup"><span data-stu-id="1e7a0-108">DMO Categories</span></span>](#dmo-categories)
-   [<span data-ttu-id="1e7a0-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1e7a0-109">Related topics</span></span>](#related-topics)

## <a name="directshow-filter-categories"></a><span data-ttu-id="1e7a0-110">DirectShow-Filter Kategorien</span><span class="sxs-lookup"><span data-stu-id="1e7a0-110">DirectShow Filter Categories</span></span>

<span data-ttu-id="1e7a0-111">Die hier aufgeführten Kategorien werden vom [Filter Mapper](filter-mapper.md)aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="1e7a0-111">The categories listed here are enumerated by the [Filter Mapper](filter-mapper.md).</span></span> <span data-ttu-id="1e7a0-112">In der Standardeinstellung ignoriert der Filter Mapper jedoch Kategorien, bei denen Vorzüge von Vorteilen \_ \_ nicht \_ oder weniger verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1e7a0-112">By default, however, the Filter Mapper ignores categories with merits of MERIT\_DO\_NOT\_USE or less.</span></span> <span data-ttu-id="1e7a0-113">Weitere Informationen finden Sie unter [**IFilterMapper2:: enummatchingfilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters).</span><span class="sxs-lookup"><span data-stu-id="1e7a0-113">For more information, see [**IFilterMapper2::EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters).</span></span> <span data-ttu-id="1e7a0-114">Alle hier aufgeführten Kategorien können auch mit dem [Enumerator für System Geräte](system-device-enumerator.md)aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="1e7a0-114">All of the categories listed here can also be enumerated with the [System Device Enumerator](system-device-enumerator.md).</span></span>

<span data-ttu-id="1e7a0-115">Die folgenden Kategorien werden in "UUIDs. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="1e7a0-115">The following categories are declared in Uuids.h.</span></span> <span data-ttu-id="1e7a0-116">Schließen Sie die Header Datei DShow. h ein.</span><span class="sxs-lookup"><span data-stu-id="1e7a0-116">Include the header file Dshow.h.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1e7a0-117">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="1e7a0-117">Friendly Name</span></span></th>
<th><span data-ttu-id="1e7a0-118">CLSID</span><span class="sxs-lookup"><span data-stu-id="1e7a0-118">CLSID</span></span></th>
<th><span data-ttu-id="1e7a0-119">Verdienst</span><span class="sxs-lookup"><span data-stu-id="1e7a0-119">Merit</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1e7a0-120">Audioerfassungs Quellen</span><span class="sxs-lookup"><span data-stu-id="1e7a0-120">Audio Capture Sources</span></span></td>
<td><span data-ttu-id="1e7a0-121"><strong>CLSID_AudioInputDeviceCategory</strong></span><span class="sxs-lookup"><span data-stu-id="1e7a0-121"><strong>CLSID_AudioInputDeviceCategory</strong></span></span></td>
<td><span data-ttu-id="1e7a0-122"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="1e7a0-122"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1e7a0-123">Audiokompressoren</span><span class="sxs-lookup"><span data-stu-id="1e7a0-123">Audio Compressors</span></span></td>
<td><span data-ttu-id="1e7a0-124"><strong>CLSID_AudioCompressorCategory</strong></span><span class="sxs-lookup"><span data-stu-id="1e7a0-124"><strong>CLSID_AudioCompressorCategory</strong></span></span></td>
<td><span data-ttu-id="1e7a0-125"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="1e7a0-125"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1e7a0-126">Audiorenderer</span><span class="sxs-lookup"><span data-stu-id="1e7a0-126">Audio Renderers</span></span></td>
<td><span data-ttu-id="1e7a0-127"><strong>CLSID_AudioRendererCategory</strong></span><span class="sxs-lookup"><span data-stu-id="1e7a0-127"><strong>CLSID_AudioRendererCategory</strong></span></span></td>
<td><span data-ttu-id="1e7a0-128"><strong>MERIT_NORMAL</strong></span><span class="sxs-lookup"><span data-stu-id="1e7a0-128"><strong>MERIT_NORMAL</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1e7a0-129">Geräte Steuerungs Filter</span><span class="sxs-lookup"><span data-stu-id="1e7a0-129">Device Control Filters</span></span></td>
<td><span data-ttu-id="1e7a0-130"><strong>CLSID_DeviceControlCategory</strong></span><span class="sxs-lookup"><span data-stu-id="1e7a0-130"><strong>CLSID_DeviceControlCategory</strong></span></span></td>
<td><span data-ttu-id="1e7a0-131"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="1e7a0-131"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1e7a0-132">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="1e7a0-132">DirectShow Filters</span></span></td>
<td><span data-ttu-id="1e7a0-133"><strong>CLSID_LegacyAmFilterCategory</strong></span><span class="sxs-lookup"><span data-stu-id="1e7a0-133"><strong>CLSID_LegacyAmFilterCategory</strong></span></span></td>
<td><span data-ttu-id="1e7a0-134"><strong>MERIT_NORMAL</strong></span><span class="sxs-lookup"><span data-stu-id="1e7a0-134"><strong>MERIT_NORMAL</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1e7a0-135">Externe Renderer</span><span class="sxs-lookup"><span data-stu-id="1e7a0-135">External Renderers</span></span></td>
<td><span data-ttu-id="1e7a0-136"><strong>CLSID_TransmitCategory</strong></span><span class="sxs-lookup"><span data-stu-id="1e7a0-136"><strong>CLSID_TransmitCategory</strong></span></span></td>
<td><span data-ttu-id="1e7a0-137"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="1e7a0-137"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1e7a0-138">MIDI-Renderer</span><span class="sxs-lookup"><span data-stu-id="1e7a0-138">Midi Renderers</span></span></td>
<td><span data-ttu-id="1e7a0-139"><strong>CLSID_MidiRendererCategory</strong></span><span class="sxs-lookup"><span data-stu-id="1e7a0-139"><strong>CLSID_MidiRendererCategory</strong></span></span></td>
<td><span data-ttu-id="1e7a0-140"><strong>MERIT_NORMAL</strong></span><span class="sxs-lookup"><span data-stu-id="1e7a0-140"><strong>MERIT_NORMAL</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1e7a0-141">Video Erfassungs Quellen</span><span class="sxs-lookup"><span data-stu-id="1e7a0-141">Video Capture Sources</span></span></td>
<td><span data-ttu-id="1e7a0-142"><strong>CLSID_VideoInputDeviceCategory</strong></span><span class="sxs-lookup"><span data-stu-id="1e7a0-142"><strong>CLSID_VideoInputDeviceCategory</strong></span></span></td>
<td><span data-ttu-id="1e7a0-143"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="1e7a0-143"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1e7a0-144">Video-Kompressoren</span><span class="sxs-lookup"><span data-stu-id="1e7a0-144">Video Compressors</span></span></td>
<td><span data-ttu-id="1e7a0-145"><strong>CLSID_VideoCompressorCategory</strong></span><span class="sxs-lookup"><span data-stu-id="1e7a0-145"><strong>CLSID_VideoCompressorCategory</strong></span></span></td>
<td><span data-ttu-id="1e7a0-146"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="1e7a0-146"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1e7a0-147">WDM-streamdekomprimierungsgeräte</span><span class="sxs-lookup"><span data-stu-id="1e7a0-147">WDM Stream Decompression Devices</span></span></td>
<td><span data-ttu-id="1e7a0-148"><strong>CLSID_DVDHWDecodersCategory</strong>
</span><span class="sxs-lookup"><span data-stu-id="1e7a0-148"><strong>CLSID_DVDHWDecodersCategory</strong>
</span></span><blockquote>
[!Note]<br />
<span data-ttu-id="1e7a0-149">Diese Kategorie enthält Hardware-DVD-Decoder.</span><span class="sxs-lookup"><span data-stu-id="1e7a0-149">This category contains hardware DVD decoders.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="1e7a0-150"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="1e7a0-150"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1e7a0-151">WDM-Streaming-Erfassungsgeräte</span><span class="sxs-lookup"><span data-stu-id="1e7a0-151">WDM Streaming Capture Devices</span></span></td>
<td><span data-ttu-id="1e7a0-152"><strong>AM_KSCATEGORY_CAPTURE</strong></span><span class="sxs-lookup"><span data-stu-id="1e7a0-152"><strong>AM_KSCATEGORY_CAPTURE</strong></span></span></td>
<td><span data-ttu-id="1e7a0-153"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="1e7a0-153"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1e7a0-154">WDM-Streaming-Crossbar-Geräte</span><span class="sxs-lookup"><span data-stu-id="1e7a0-154">WDM Streaming Crossbar Devices</span></span></td>
<td><span data-ttu-id="1e7a0-155"><strong>AM_KSCATEGORY_CROSSBAR</strong></span><span class="sxs-lookup"><span data-stu-id="1e7a0-155"><strong>AM_KSCATEGORY_CROSSBAR</strong></span></span></td>
<td><span data-ttu-id="1e7a0-156"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="1e7a0-156"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1e7a0-157">WDM Streaming-renderinggeräte</span><span class="sxs-lookup"><span data-stu-id="1e7a0-157">WDM Streaming Rendering Devices</span></span></td>
<td><span data-ttu-id="1e7a0-158"><strong>AM_KSCATEGORY_RENDER</strong></span><span class="sxs-lookup"><span data-stu-id="1e7a0-158"><strong>AM_KSCATEGORY_RENDER</strong></span></span></td>
<td><span data-ttu-id="1e7a0-159"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="1e7a0-159"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1e7a0-160">WDM-Streaming-Tee/Splitter-Geräte</span><span class="sxs-lookup"><span data-stu-id="1e7a0-160">WDM Streaming Tee/Splitter Devices</span></span></td>
<td><span data-ttu-id="1e7a0-161"><strong>AM_KSCATEGORY_SPLITTER</strong></span><span class="sxs-lookup"><span data-stu-id="1e7a0-161"><strong>AM_KSCATEGORY_SPLITTER</strong></span></span></td>
<td><span data-ttu-id="1e7a0-162"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="1e7a0-162"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1e7a0-163">WDM Streaming TV-Audiogeräte</span><span class="sxs-lookup"><span data-stu-id="1e7a0-163">WDM Streaming TV Audio Devices</span></span></td>
<td><span data-ttu-id="1e7a0-164"><strong>AM_KSCATEGORY_TVAUDIO</strong></span><span class="sxs-lookup"><span data-stu-id="1e7a0-164"><strong>AM_KSCATEGORY_TVAUDIO</strong></span></span></td>
<td><span data-ttu-id="1e7a0-165"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="1e7a0-165"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1e7a0-166">WDM-Streaming TV-Tuner-Geräte</span><span class="sxs-lookup"><span data-stu-id="1e7a0-166">WDM Streaming TV Tuner Devices</span></span></td>
<td><span data-ttu-id="1e7a0-167"><strong>AM_KSCATEGORY_TVTUNER</strong></span><span class="sxs-lookup"><span data-stu-id="1e7a0-167"><strong>AM_KSCATEGORY_TVTUNER</strong></span></span></td>
<td><span data-ttu-id="1e7a0-168"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="1e7a0-168"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1e7a0-169">WDM-Streaming-VBI-Codecs</span><span class="sxs-lookup"><span data-stu-id="1e7a0-169">WDM Streaming VBI Codecs</span></span></td>
<td><span data-ttu-id="1e7a0-170"><strong>AM_KSCATEGORY_VBICODEC</strong></span><span class="sxs-lookup"><span data-stu-id="1e7a0-170"><strong>AM_KSCATEGORY_VBICODEC</strong></span></span></td>
<td><span data-ttu-id="1e7a0-171"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="1e7a0-171"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="1e7a0-172">Die folgenden Kategorien werden in der Header Datei ". h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="1e7a0-172">The following categories are declared in the header file Ks.h.</span></span>



| <span data-ttu-id="1e7a0-173">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="1e7a0-173">Friendly Name</span></span>                          | <span data-ttu-id="1e7a0-174">CLSID</span><span class="sxs-lookup"><span data-stu-id="1e7a0-174">CLSID</span></span>                                   | <span data-ttu-id="1e7a0-175">Verdienst</span><span class="sxs-lookup"><span data-stu-id="1e7a0-175">Merit</span></span>                   |
|----------------------------------------|-----------------------------------------|-------------------------|
| <span data-ttu-id="1e7a0-176">WDM-streamingkommunikationstransformationen</span><span class="sxs-lookup"><span data-stu-id="1e7a0-176">WDM Streaming Communication Transforms</span></span> | <span data-ttu-id="1e7a0-177">**kscategory \_ communicationstransform**</span><span class="sxs-lookup"><span data-stu-id="1e7a0-177">**KSCATEGORY\_COMMUNICATIONSTRANSFORM**</span></span> | <span data-ttu-id="1e7a0-178">**das Verdienst wird \_ \_ nicht \_ verwendet.**</span><span class="sxs-lookup"><span data-stu-id="1e7a0-178">**MERIT\_DO\_NOT\_USE**</span></span> |
| <span data-ttu-id="1e7a0-179">WDM-streamingdatentransformationen</span><span class="sxs-lookup"><span data-stu-id="1e7a0-179">WDM Streaming Data Transforms</span></span>          | <span data-ttu-id="1e7a0-180">**kscategory \_ DataTransform**</span><span class="sxs-lookup"><span data-stu-id="1e7a0-180">**KSCATEGORY\_DATATRANSFORM**</span></span>           | <span data-ttu-id="1e7a0-181">**das Verdienst wird \_ \_ nicht \_ verwendet.**</span><span class="sxs-lookup"><span data-stu-id="1e7a0-181">**MERIT\_DO\_NOT\_USE**</span></span> |
| <span data-ttu-id="1e7a0-182">WDM-Streaming-Schnittstellen Transformationen</span><span class="sxs-lookup"><span data-stu-id="1e7a0-182">WDM Streaming Interface Transforms</span></span>     | <span data-ttu-id="1e7a0-183">**kscategory \_ interfacetransform**</span><span class="sxs-lookup"><span data-stu-id="1e7a0-183">**KSCATEGORY\_INTERFACETRANSFORM**</span></span>      | <span data-ttu-id="1e7a0-184">**das Verdienst wird \_ \_ nicht \_ verwendet.**</span><span class="sxs-lookup"><span data-stu-id="1e7a0-184">**MERIT\_DO\_NOT\_USE**</span></span> |
| <span data-ttu-id="1e7a0-185">WDM-Streaming-Mischgeräte</span><span class="sxs-lookup"><span data-stu-id="1e7a0-185">WDM Streaming Mixer Devices</span></span>            | <span data-ttu-id="1e7a0-186">**kscategory- \_ Mixer**</span><span class="sxs-lookup"><span data-stu-id="1e7a0-186">**KSCATEGORY\_MIXER**</span></span>                   | <span data-ttu-id="1e7a0-187">**das Verdienst wird \_ \_ nicht \_ verwendet.**</span><span class="sxs-lookup"><span data-stu-id="1e7a0-187">**MERIT\_DO\_NOT\_USE**</span></span> |



 

<span data-ttu-id="1e7a0-188">Die folgenden Kategorien werden in der Header Datei bdamedia. h deklariert.</span><span class="sxs-lookup"><span data-stu-id="1e7a0-188">The following categories are declared in the header file Bdamedia.h.</span></span> <span data-ttu-id="1e7a0-189">Fügen Sie die folgenden Header Dateien ein: "KS. h", "ksmedia. h" und "bdamedia. h".</span><span class="sxs-lookup"><span data-stu-id="1e7a0-189">Include the following header files: ks.h, ksmedia.h, and bdamedia.h.</span></span>



| <span data-ttu-id="1e7a0-190">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="1e7a0-190">Friendly Name</span></span>                       | <span data-ttu-id="1e7a0-191">CLSID</span><span class="sxs-lookup"><span data-stu-id="1e7a0-191">CLSID</span></span>                                       | <span data-ttu-id="1e7a0-192">Verdienst</span><span class="sxs-lookup"><span data-stu-id="1e7a0-192">Merit</span></span>                   |
|-------------------------------------|---------------------------------------------|-------------------------|
| <span data-ttu-id="1e7a0-193">BDA-Netzwerkanbieter</span><span class="sxs-lookup"><span data-stu-id="1e7a0-193">BDA Network Providers</span></span>               | <span data-ttu-id="1e7a0-194">**kscategory- \_ BDA- \_ Netzwerk \_ Anbieter**</span><span class="sxs-lookup"><span data-stu-id="1e7a0-194">**KSCATEGORY\_BDA\_NETWORK\_PROVIDER**</span></span>      | <span data-ttu-id="1e7a0-195">**Verdienst \_ Normal**</span><span class="sxs-lookup"><span data-stu-id="1e7a0-195">**MERIT\_NORMAL**</span></span>       |
| <span data-ttu-id="1e7a0-196">BDA-Empfänger Komponenten</span><span class="sxs-lookup"><span data-stu-id="1e7a0-196">BDA Receiver Components</span></span>             | <span data-ttu-id="1e7a0-197">**kscategory- \_ BDA \_ Empfänger \_ Komponente**</span><span class="sxs-lookup"><span data-stu-id="1e7a0-197">**KSCATEGORY\_BDA\_RECEIVER\_COMPONENT**</span></span>    | <span data-ttu-id="1e7a0-198">**das Verdienst wird \_ \_ nicht \_ verwendet.**</span><span class="sxs-lookup"><span data-stu-id="1e7a0-198">**MERIT\_DO\_NOT\_USE**</span></span> |
| <span data-ttu-id="1e7a0-199">BDA-Rendering-Filter</span><span class="sxs-lookup"><span data-stu-id="1e7a0-199">BDA Rendering Filters</span></span>               | <span data-ttu-id="1e7a0-200">**kscategory \_ -IP- \_ Senke**</span><span class="sxs-lookup"><span data-stu-id="1e7a0-200">**KSCATEGORY\_IP\_SINK**</span></span>                    | <span data-ttu-id="1e7a0-201">**das Verdienst wird \_ \_ nicht \_ verwendet.**</span><span class="sxs-lookup"><span data-stu-id="1e7a0-201">**MERIT\_DO\_NOT\_USE**</span></span> |
| <span data-ttu-id="1e7a0-202">BDA-Quell Filter</span><span class="sxs-lookup"><span data-stu-id="1e7a0-202">BDA Source Filters</span></span>                  | <span data-ttu-id="1e7a0-203">**kscategory- \_ BDA- \_ Netzwerk- \_ Tuner**</span><span class="sxs-lookup"><span data-stu-id="1e7a0-203">**KSCATEGORY\_BDA\_NETWORK\_TUNER**</span></span>         | <span data-ttu-id="1e7a0-204">**das Verdienst wird \_ \_ nicht \_ verwendet.**</span><span class="sxs-lookup"><span data-stu-id="1e7a0-204">**MERIT\_DO\_NOT\_USE**</span></span> |
| <span data-ttu-id="1e7a0-205">BDA-Transport Informations Renderer</span><span class="sxs-lookup"><span data-stu-id="1e7a0-205">BDA Transport Information Renderers</span></span> | <span data-ttu-id="1e7a0-206">**kscategory- \_ BDA- \_ Transport \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="1e7a0-206">**KSCATEGORY\_BDA\_TRANSPORT\_INFORMATION**</span></span> | <span data-ttu-id="1e7a0-207">**Verdienst \_ Normal**</span><span class="sxs-lookup"><span data-stu-id="1e7a0-207">**MERIT\_NORMAL**</span></span>       |



 

> [!Note]  
> <span data-ttu-id="1e7a0-208">Decoders werden unter der Kategorie "DirectShow-Filter" (CLSID \_ legacyamfiltercategory) registriert.</span><span class="sxs-lookup"><span data-stu-id="1e7a0-208">Decoders are registered under the "DirectShow Filters" category (CLSID\_LegacyAmFilterCategory).</span></span>

 

## <a name="other-filter-categories"></a><span data-ttu-id="1e7a0-209">Weitere Filter Kategorien</span><span class="sxs-lookup"><span data-stu-id="1e7a0-209">Other Filter Categories</span></span>

<span data-ttu-id="1e7a0-210">Die hier aufgeführten Kategorien können mit dem Enumerator für System Geräte aufgelistet werden, sind aber für die Filter Zuordnung nicht sichtbar und werden nicht von [Intelligent Connect](intelligent-connect.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="1e7a0-210">The categories listed here can be enumerated with the System Device Enumerator, but are not visible to the Filter Mapper and are not used by [Intelligent Connect](intelligent-connect.md).</span></span>

<span data-ttu-id="1e7a0-211">Die folgenden Kategorien sind in der Header Datei "qedit. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="1e7a0-211">The following categories are declared in the header file Qedit.h.</span></span>



| <span data-ttu-id="1e7a0-212">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="1e7a0-212">Friendly Name</span></span>            | <span data-ttu-id="1e7a0-213">CLID</span><span class="sxs-lookup"><span data-stu-id="1e7a0-213">CLID</span></span>                             | <span data-ttu-id="1e7a0-214">Verdienst</span><span class="sxs-lookup"><span data-stu-id="1e7a0-214">Merit</span></span>                   |
|--------------------------|----------------------------------|-------------------------|
| <span data-ttu-id="1e7a0-215">Video Effekte (1 Eingabe)</span><span class="sxs-lookup"><span data-stu-id="1e7a0-215">Video Effects (1 input)</span></span>  | <span data-ttu-id="1e7a0-216">**CLSID- \_ VideoEffects1Category**</span><span class="sxs-lookup"><span data-stu-id="1e7a0-216">**CLSID\_VideoEffects1Category**</span></span> | <span data-ttu-id="1e7a0-217">**das Verdienst wird \_ \_ nicht \_ verwendet.**</span><span class="sxs-lookup"><span data-stu-id="1e7a0-217">**MERIT\_DO\_NOT\_USE**</span></span> |
| <span data-ttu-id="1e7a0-218">Video Effekte (2 Eingaben)</span><span class="sxs-lookup"><span data-stu-id="1e7a0-218">Video Effects (2 inputs)</span></span> | <span data-ttu-id="1e7a0-219">**CLSID- \_ VideoEffects2Category**</span><span class="sxs-lookup"><span data-stu-id="1e7a0-219">**CLSID\_VideoEffects2Category**</span></span> | <span data-ttu-id="1e7a0-220">**das Verdienst wird \_ \_ nicht \_ verwendet.**</span><span class="sxs-lookup"><span data-stu-id="1e7a0-220">**MERIT\_DO\_NOT\_USE**</span></span> |



 

<span data-ttu-id="1e7a0-221">Diese Kategorien enthalten Video Effekte und Übergänge für [DirectShow-Bearbeitungs Dienste](directshow-editing-services.md):</span><span class="sxs-lookup"><span data-stu-id="1e7a0-221">These categories contain video effects and transitions for [DirectShow Editing Services](directshow-editing-services.md):</span></span>

-   <span data-ttu-id="1e7a0-222">"Video Effekte (1 Eingabe)" enthält Video Effekte.</span><span class="sxs-lookup"><span data-stu-id="1e7a0-222">"Video Effects (1 input)" contains video effects.</span></span>
-   <span data-ttu-id="1e7a0-223">"Video Effekte (2 Eingabe)" enthält Video Übergänge.</span><span class="sxs-lookup"><span data-stu-id="1e7a0-223">"Video Effects (2 input)" contains video transitions.</span></span>

<span data-ttu-id="1e7a0-224">Weitere Informationen finden Sie unter [Enumerieren von Effekten und Übergängen](enumerating-effects-and-transitions.md).</span><span class="sxs-lookup"><span data-stu-id="1e7a0-224">For more information, see [Enumerating Effects and Transitions](enumerating-effects-and-transitions.md).</span></span>

<span data-ttu-id="1e7a0-225">Die folgenden Kategorien sind in der Header Datei "UUIDs. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="1e7a0-225">The following categories are declared in the header file Uuids.h.</span></span> <span data-ttu-id="1e7a0-226">Schließen Sie die Header Datei DShow. h ein.</span><span class="sxs-lookup"><span data-stu-id="1e7a0-226">Include the header file Dshow.h.</span></span>



| <span data-ttu-id="1e7a0-227">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="1e7a0-227">Friendly Name</span></span>       | <span data-ttu-id="1e7a0-228">CLID</span><span class="sxs-lookup"><span data-stu-id="1e7a0-228">CLID</span></span>                                | <span data-ttu-id="1e7a0-229">Verdienst</span><span class="sxs-lookup"><span data-stu-id="1e7a0-229">Merit</span></span>                   |
|---------------------|-------------------------------------|-------------------------|
| <span data-ttu-id="1e7a0-230">Umcapi-Encoder</span><span class="sxs-lookup"><span data-stu-id="1e7a0-230">EncAPI Encoders</span></span>     | <span data-ttu-id="1e7a0-231">**CLSID \_ mediaencodercategory**</span><span class="sxs-lookup"><span data-stu-id="1e7a0-231">**CLSID\_MediaEncoderCategory**</span></span>     | <span data-ttu-id="1e7a0-232">**das Verdienst wird \_ \_ nicht \_ verwendet.**</span><span class="sxs-lookup"><span data-stu-id="1e7a0-232">**MERIT\_DO\_NOT\_USE**</span></span> |
| <span data-ttu-id="1e7a0-233">Umcapi-Multiplexer</span><span class="sxs-lookup"><span data-stu-id="1e7a0-233">EncAPI Multiplexers</span></span> | <span data-ttu-id="1e7a0-234">**CLSID \_ mediamultiplexercategory**</span><span class="sxs-lookup"><span data-stu-id="1e7a0-234">**CLSID\_MediaMultiplexerCategory**</span></span> | <span data-ttu-id="1e7a0-235">**das Verdienst wird \_ \_ nicht \_ verwendet.**</span><span class="sxs-lookup"><span data-stu-id="1e7a0-235">**MERIT\_DO\_NOT\_USE**</span></span> |



 

## <a name="directshow-filter-meta-category"></a><span data-ttu-id="1e7a0-236">DirectShow-Filter Meta-Category</span><span class="sxs-lookup"><span data-stu-id="1e7a0-236">DirectShow Filter Meta-Category</span></span>



| <span data-ttu-id="1e7a0-237">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="1e7a0-237">Friendly Name</span></span>                 | <span data-ttu-id="1e7a0-238">CLSID</span><span class="sxs-lookup"><span data-stu-id="1e7a0-238">CLSID</span></span>                            | <span data-ttu-id="1e7a0-239">Verdienst</span><span class="sxs-lookup"><span data-stu-id="1e7a0-239">Merit</span></span>          |
|-------------------------------|----------------------------------|----------------|
| <span data-ttu-id="1e7a0-240">ActiveMovie-Filter Kategorien</span><span class="sxs-lookup"><span data-stu-id="1e7a0-240">ActiveMovie Filter Categories</span></span> | <span data-ttu-id="1e7a0-241">**CLSID \_ activemoviecategories**</span><span class="sxs-lookup"><span data-stu-id="1e7a0-241">**CLSID\_ActiveMovieCategories**</span></span> | <span data-ttu-id="1e7a0-242">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="1e7a0-242">Not applicable</span></span> |



 

<span data-ttu-id="1e7a0-243">Diese metakategorie enthält eine Liste mit Filter Kategorien.</span><span class="sxs-lookup"><span data-stu-id="1e7a0-243">This meta-category contains a list of filter categories.</span></span> <span data-ttu-id="1e7a0-244">Wenn eine Filterkategorie nicht in dieser Liste angezeigt wird, ignoriert der [Filter Mapper](filter-mapper.md) die Kategorie. Dies bedeutet, dass der Filter für eine [intelligente Verbindung](intelligent-connect.md)nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="1e7a0-244">If a filter category does not appear within this list, the [Filter Mapper](filter-mapper.md) ignores the category, which means the filter is not available for [Intelligent Connect](intelligent-connect.md).</span></span>

<span data-ttu-id="1e7a0-245">Um die Liste der Filter Kategorien aufzulisten, nennen Sie [**ikreatedevenum:: kreateclassenumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) mit dem Wert CLSID \_ activemoviecategories.</span><span class="sxs-lookup"><span data-stu-id="1e7a0-245">To enumerate the list of filter categories, call [**ICreateDevEnum::CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) with the value CLSID\_ActiveMovieCategories.</span></span> <span data-ttu-id="1e7a0-246">Die von dieser Methode zurückgegebenen Moniker unterstützen die folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1e7a0-246">The monikers returned by this method support the following properties.</span></span>



| <span data-ttu-id="1e7a0-247">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="1e7a0-247">Property Name</span></span>  | <span data-ttu-id="1e7a0-248">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1e7a0-248">Description</span></span>                                                                            |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e7a0-249">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="1e7a0-249">"FriendlyName"</span></span> | <span data-ttu-id="1e7a0-250">Kategoriename (VT \_ BSTR).</span><span class="sxs-lookup"><span data-stu-id="1e7a0-250">Category name (VT\_BSTR).</span></span>                                                              |
| <span data-ttu-id="1e7a0-251">Verdienst</span><span class="sxs-lookup"><span data-stu-id="1e7a0-251">"Merit"</span></span>        | <span data-ttu-id="1e7a0-252">Kategorie-Verdienst (VT \_ I4).</span><span class="sxs-lookup"><span data-stu-id="1e7a0-252">Category merit (VT\_I4).</span></span> <span data-ttu-id="1e7a0-253">Wenn diese Eigenschaft nicht vorhanden ist, **\_ \_ \_ verwenden Sie als Verdienst nicht**.</span><span class="sxs-lookup"><span data-stu-id="1e7a0-253">If this property is absent, treat as **MERIT\_DO\_NOT\_USE**.</span></span> |
| <span data-ttu-id="1e7a0-254">CLSID</span><span class="sxs-lookup"><span data-stu-id="1e7a0-254">"CLSID"</span></span>        | <span data-ttu-id="1e7a0-255">Kategorie CLSID (VT \_ BSTR).</span><span class="sxs-lookup"><span data-stu-id="1e7a0-255">Category CLSID (VT\_BSTR).</span></span>                                                             |



 

<span data-ttu-id="1e7a0-256">Um dieser Liste eine neue Filterkategorie hinzuzufügen, nennen Sie [**IFilterMapper2:: | atecategory**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-createcategory).</span><span class="sxs-lookup"><span data-stu-id="1e7a0-256">To add a new filter category to this list, call [**IFilterMapper2::CreateCategory**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-createcategory).</span></span>

## <a name="dmo-categories"></a><span data-ttu-id="1e7a0-257">DMO-Kategorien</span><span class="sxs-lookup"><span data-stu-id="1e7a0-257">DMO Categories</span></span>

<span data-ttu-id="1e7a0-258">DirectX Media Objects (DMOs) verwenden einen anderen enumerationsmechanismus als DirectShow-Filter.</span><span class="sxs-lookup"><span data-stu-id="1e7a0-258">DirectX Media Objects (DMOs) use a different enumeration mechanism from DirectShow filters.</span></span> <span data-ttu-id="1e7a0-259">Weitere Informationen finden Sie unter [Registrieren eines DMO](registering-a-dmo.md).</span><span class="sxs-lookup"><span data-stu-id="1e7a0-259">For more information, see [Registering a DMO](registering-a-dmo.md).</span></span> <span data-ttu-id="1e7a0-260">Sie können jedoch den Enumerator "System Geräte" verwenden, um DMO-Kategorien aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="1e7a0-260">However, you can use the System Device Enumerator to enumerate DMO categories.</span></span> <span data-ttu-id="1e7a0-261">Die Moniker binden an den [DMO-Wrapper Filter](dmo-wrapper-filter.md) und initialisieren den Filter automatisch mit dem DMO.</span><span class="sxs-lookup"><span data-stu-id="1e7a0-261">The monikers bind to the [DMO Wrapper Filter](dmo-wrapper-filter.md) and automatically initialize the filter with the DMO.</span></span>

<span data-ttu-id="1e7a0-262">Außerdem werden einige der DMO-Kategorien für die intelligente Verbindung zu den DirectShow-Filter Kategorien zugeordnet:</span><span class="sxs-lookup"><span data-stu-id="1e7a0-262">In addition, some of the DMO categories are mapped to DirectShow filter categories for the purposes of intelligent connect:</span></span>



| <span data-ttu-id="1e7a0-263">DMO-Kategorie</span><span class="sxs-lookup"><span data-stu-id="1e7a0-263">DMO Category</span></span>                    | <span data-ttu-id="1e7a0-264">DirectShow-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="1e7a0-264">DirectShow Equivalent</span></span>              |
|---------------------------------|------------------------------------|
| <span data-ttu-id="1e7a0-265">**dmucategory \_ - \_ Audioencoder**</span><span class="sxs-lookup"><span data-stu-id="1e7a0-265">**DMOCATEGORY\_AUDIO\_ENCODER**</span></span> | <span data-ttu-id="1e7a0-266">**CLSID \_ audiocompressorcategory**</span><span class="sxs-lookup"><span data-stu-id="1e7a0-266">**CLSID\_AudioCompressorCategory**</span></span> |
| <span data-ttu-id="1e7a0-267">**dmucategory \_ - \_ Audiodecoder**</span><span class="sxs-lookup"><span data-stu-id="1e7a0-267">**DMOCATEGORY\_AUDIO\_DECODER**</span></span> | <span data-ttu-id="1e7a0-268">**CLSID \_ legacyamfiltercategory**</span><span class="sxs-lookup"><span data-stu-id="1e7a0-268">**CLSID\_LegacyAmFilterCategory**</span></span>  |
| <span data-ttu-id="1e7a0-269">**dmucategory- \_ Video \_ Encoder**</span><span class="sxs-lookup"><span data-stu-id="1e7a0-269">**DMOCATEGORY\_VIDEO\_ENCODER**</span></span> | <span data-ttu-id="1e7a0-270">**CLSID \_ videocompressorcategory**</span><span class="sxs-lookup"><span data-stu-id="1e7a0-270">**CLSID\_VideoCompressorCategory**</span></span> |
| <span data-ttu-id="1e7a0-271">**dmucategory- \_ Video \_ Decoder**</span><span class="sxs-lookup"><span data-stu-id="1e7a0-271">**DMOCATEGORY\_VIDEO\_DECODER**</span></span> | <span data-ttu-id="1e7a0-272">**CLSID \_ legacyamfiltercategory**</span><span class="sxs-lookup"><span data-stu-id="1e7a0-272">**CLSID\_LegacyAmFilterCategory**</span></span>  |



 

<span data-ttu-id="1e7a0-273">Beachten Sie, dass die Kategorien "Videoeffekt" und "Audioeffekt" keiner DirectShow-Kategorie zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="1e7a0-273">Note that the video effect and audio effect categories are not mapped to any DirectShow categories.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1e7a0-274">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1e7a0-274">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e7a0-275">Konstanten und GUIDs</span><span class="sxs-lookup"><span data-stu-id="1e7a0-275">Constants and GUIDs</span></span>](constants-and-guids.md)
</dt> <dt>

[<span data-ttu-id="1e7a0-276">Auflisten von Geräten und Filtern</span><span class="sxs-lookup"><span data-stu-id="1e7a0-276">Enumerating Devices and Filters</span></span>](enumerating-devices-and-filters.md)
</dt> <dt>

[<span data-ttu-id="1e7a0-277">Intelligent Connect</span><span class="sxs-lookup"><span data-stu-id="1e7a0-277">Intelligent Connect</span></span>](intelligent-connect.md)
</dt> <dt>

[<span data-ttu-id="1e7a0-278">Layout der Registrierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="1e7a0-278">Layout of the Registry Keys</span></span>](layout-of-the-registry-keys.md)
</dt> <dt>

[<span data-ttu-id="1e7a0-279">Verwenden des Filter Mappers</span><span class="sxs-lookup"><span data-stu-id="1e7a0-279">Using the Filter Mapper</span></span>](using-the-filter-mapper.md)
</dt> <dt>

[<span data-ttu-id="1e7a0-280">Verwenden des Enumerators für System Geräte</span><span class="sxs-lookup"><span data-stu-id="1e7a0-280">Using the System Device Enumerator</span></span>](using-the-system-device-enumerator.md)
</dt> </dl>

 

 




