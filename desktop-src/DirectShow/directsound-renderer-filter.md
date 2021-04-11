---
description: DirectSound-rendererfilter
ms.assetid: ec6cc790-8c1f-4de4-a7ca-a7073894380e
title: DirectSound-rendererfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae932340ea22213e0f9d7234599742d74208f632
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123505"
---
# <a name="directsound-renderer-filter"></a><span data-ttu-id="1835c-103">DirectSound-rendererfilter</span><span class="sxs-lookup"><span data-stu-id="1835c-103">DirectSound Renderer Filter</span></span>

<span data-ttu-id="1835c-104">Mit diesem Filter wird Audio mithilfe von DirectSound gerendert.</span><span class="sxs-lookup"><span data-stu-id="1835c-104">This filter renders audio using DirectSound.</span></span> <span data-ttu-id="1835c-105">Dieser Filter ist derzeit der Standardaudiorenderer für Wellenform Sound.</span><span class="sxs-lookup"><span data-stu-id="1835c-105">This filter is currently the default audio renderer for waveform sound.</span></span>

<span data-ttu-id="1835c-106">Zusätzlich zu den grundlegenden Sound Rendering-Funktionen kann dieser Filter DirectSound-API-Aufrufe verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="1835c-106">In addition to its basic sound-rendering capabilities, this filter can process DirectSound API calls.</span></span> <span data-ttu-id="1835c-107">Verwenden Sie die [**iamdirectsound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound) -Methoden, um das Fenster festzulegen und abzurufen, das die Audiowiedergabe behandelt.</span><span class="sxs-lookup"><span data-stu-id="1835c-107">Use the [**IAMDirectSound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound) methods to set and retrieve the window that will handle the sound playback.</span></span> <span data-ttu-id="1835c-108">Der DirectSound-audiorenderer ist der standardaudiorenderingfilter für DirectShow.</span><span class="sxs-lookup"><span data-stu-id="1835c-108">The DirectSound Audio Renderer is the default audio rendering filter for DirectShow.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1835c-109">Filter Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="1835c-109">Filter Interfaces</span></span></td>
<td><span data-ttu-id="1835c-110"><a href="/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats"><strong>Iamaudiorendererstats</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamclockslave"><strong>iamclockslave</strong></a>, <a href="/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound"><strong>iamdirectsound</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol"><strong>iamresourcecontrol</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>ibasefilter</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ibasicaudio"><strong>ibasicaudio</strong></a>, <strong>IDirectSound3DBuffer</strong>, <strong>IDirectSound3dListener</strong>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>imediaposition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>imediaseeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>iqualitycontrol</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></span><span class="sxs-lookup"><span data-stu-id="1835c-110"><a href="/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats"><strong>IAMAudioRendererStats</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamclockslave"><strong>IAMClockSlave</strong></a>, <a href="/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound"><strong>IAMDirectSound</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol"><strong>IAMResourceControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Control/nn-control-ibasicaudio"><strong>IBasicAudio</strong></a>, <strong>IDirectSound3DBuffer</strong>, <strong>IDirectSound3dListener</strong>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1835c-111">Eingabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="1835c-111">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="1835c-112">Haupttyp: MEDIATYPE_AudioSubtypes:</span><span class="sxs-lookup"><span data-stu-id="1835c-112">Major Type: MEDIATYPE_AudioSubtypes:</span></span><br/>
<ul>
<li><span data-ttu-id="1835c-113">MEDIASUBTYPE_PCM</span><span class="sxs-lookup"><span data-stu-id="1835c-113">MEDIASUBTYPE_PCM</span></span></li>
<li><span data-ttu-id="1835c-114">MEDIASUBTYPE_IEEE_FLOAT</span><span class="sxs-lookup"><span data-stu-id="1835c-114">MEDIASUBTYPE_IEEE_FLOAT</span></span></li>
<li><span data-ttu-id="1835c-115">MEDIASUBTYPE_DOLBY_AC3_SPDIF</span><span class="sxs-lookup"><span data-stu-id="1835c-115">MEDIASUBTYPE_DOLBY_AC3_SPDIF</span></span></li>
<li><span data-ttu-id="1835c-116">MEDIASUBTYPE_RAW_SPORT</span><span class="sxs-lookup"><span data-stu-id="1835c-116">MEDIASUBTYPE_RAW_SPORT</span></span></li>
<li><span data-ttu-id="1835c-117">MEDIASUBTYPE_SPDIF_TAG_241h</span><span class="sxs-lookup"><span data-stu-id="1835c-117">MEDIASUBTYPE_SPDIF_TAG_241h</span></span></li>
<li><span data-ttu-id="1835c-118">MEDIASUBTYPE_DRM_Audio</span><span class="sxs-lookup"><span data-stu-id="1835c-118">MEDIASUBTYPE_DRM_Audio</span></span></li>
</ul>
<span data-ttu-id="1835c-119">Formattyp: FORMAT_WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="1835c-119">Format type: FORMAT_WaveFormatEx</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1835c-120">PIN-Eingabeschnittstellen</span><span class="sxs-lookup"><span data-stu-id="1835c-120">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="1835c-121"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>ipinconnection</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>iqualitycontrol</strong></a></span><span class="sxs-lookup"><span data-stu-id="1835c-121"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1835c-122">Ausgabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="1835c-122">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="1835c-123">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="1835c-123">Not applicable.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1835c-124">PIN-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="1835c-124">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="1835c-125">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="1835c-125">Not applicable.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1835c-126">CLSID Filtern</span><span class="sxs-lookup"><span data-stu-id="1835c-126">Filter CLSID</span></span></td>
<td><span data-ttu-id="1835c-127">CLSID_DSoundRender</span><span class="sxs-lookup"><span data-stu-id="1835c-127">CLSID_DSoundRender</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1835c-128">CLSID der Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="1835c-128">Property Page CLSID</span></span></td>
<td><span data-ttu-id="1835c-129">CLSID_AudioProperties CLSID_AudioRendererAdvancedProperties</span><span class="sxs-lookup"><span data-stu-id="1835c-129">CLSID_AudioProperties, CLSID_AudioRendererAdvancedProperties</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1835c-130">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="1835c-130">Executable</span></span></td>
<td><span data-ttu-id="1835c-131">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="1835c-131">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1835c-132"><a href="merit.md">Verdienst</a></span><span class="sxs-lookup"><span data-stu-id="1835c-132"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="1835c-133">MERIT_PREFERRED</span><span class="sxs-lookup"><span data-stu-id="1835c-133">MERIT_PREFERRED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1835c-134"><a href="filter-categories.md">Filter Kategorie</a></span><span class="sxs-lookup"><span data-stu-id="1835c-134"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="1835c-135">CLSID_AudioRendererCategory</span><span class="sxs-lookup"><span data-stu-id="1835c-135">CLSID_AudioRendererCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="1835c-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1835c-136">Remarks</span></span>

<span data-ttu-id="1835c-137">Dieser Filter fungiert als Wrapper für ein Audiogerät.</span><span class="sxs-lookup"><span data-stu-id="1835c-137">This filter acts as a wrapper for an audio device.</span></span> <span data-ttu-id="1835c-138">Um die auf dem System des Benutzers verfügbaren Audiogeräte aufzulisten, verwenden Sie die [**ikreatedevenum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) -Schnittstelle mit der Kategorie audiorenderer (CLSID \_ audiorenderercategory).</span><span class="sxs-lookup"><span data-stu-id="1835c-138">To enumerate the audio devices available on the user's system, use the [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) interface with the audio renderer category (CLSID\_AudioRendererCategory).</span></span> <span data-ttu-id="1835c-139">Für jedes Audiogerät enthält die Kategorie audiorenderer zwei Filter Instanzen.</span><span class="sxs-lookup"><span data-stu-id="1835c-139">For each audio device, the audio renderer category contains two filter instances.</span></span> <span data-ttu-id="1835c-140">Eine dieser Funktionen entspricht dem DirectSound-Renderer, der andere entspricht dem Filter für [audiorenderer (waveout)](audio-renderer--waveout--filter.md) .</span><span class="sxs-lookup"><span data-stu-id="1835c-140">One of these corresponds to the DirectSound Renderer, and the other corresponds to the [Audio Renderer (WaveOut)](audio-renderer--waveout--filter.md) filter.</span></span> <span data-ttu-id="1835c-141">Die DirectSound-Instanz hat den anzeigen Amen "DirectSound: *DeviceName*", wobei " *DeviceName* " der Name des Geräts ist.</span><span class="sxs-lookup"><span data-stu-id="1835c-141">The DirectSound instance has the friendly name "DirectSound: *DeviceName*," where *DeviceName* is the name of the device.</span></span> <span data-ttu-id="1835c-142">Die waveout-Instanz hat den anzeigen Amen " *DeviceName*".</span><span class="sxs-lookup"><span data-stu-id="1835c-142">The WaveOut instance has the friendly name *DeviceName*.</span></span>

<span data-ttu-id="1835c-143">Die Kategorie audiorenderer enthält zwei zusätzliche Filter Instanzen mit dem Namen "Standard-DirectSound-Gerät" und "standardmäßige Wellen Gerät".</span><span class="sxs-lookup"><span data-stu-id="1835c-143">The audio renderer category contains two additional filter instances, named "Default DirectSound Device" and "Default WaveOut Device."</span></span> <span data-ttu-id="1835c-144">Diese entsprechen dem Standard-Audiogerät, das der Benutzer über die Systemsteuerung ausgewählt hat.</span><span class="sxs-lookup"><span data-stu-id="1835c-144">These correspond to the default sound device, as chosen by the user through the Control Panel.</span></span> <span data-ttu-id="1835c-145">Sie sind tatsächlich Zuordnungen zu einem der im vorherigen Abschnitt beschriebenen Paare.</span><span class="sxs-lookup"><span data-stu-id="1835c-145">They are actually mappings to one of the pairs described in the previous paragraph.</span></span> <span data-ttu-id="1835c-146">Wenn das System beispielsweise über zwei Audiogeräte (Gerät A und Gerät B) verfügt, enthält die Kategorie audiorenderer Folgendes:</span><span class="sxs-lookup"><span data-stu-id="1835c-146">For example, if the system has two audio devices, Device A and Device B, the audio renderer category will contain the following:</span></span>

-   <span data-ttu-id="1835c-147">Gerät A</span><span class="sxs-lookup"><span data-stu-id="1835c-147">Device A</span></span>
-   <span data-ttu-id="1835c-148">DirectSound: Gerät A</span><span class="sxs-lookup"><span data-stu-id="1835c-148">DirectSound: Device A</span></span>
-   <span data-ttu-id="1835c-149">Gerät B</span><span class="sxs-lookup"><span data-stu-id="1835c-149">Device B</span></span>
-   <span data-ttu-id="1835c-150">DirectSound: Gerät B</span><span class="sxs-lookup"><span data-stu-id="1835c-150">DirectSound: Device B</span></span>
-   <span data-ttu-id="1835c-151">DirectSound-Standardgerät</span><span class="sxs-lookup"><span data-stu-id="1835c-151">Default DirectSound Device</span></span>
-   <span data-ttu-id="1835c-152">Standardmäßiges Wellen Gerät</span><span class="sxs-lookup"><span data-stu-id="1835c-152">Default WaveOut Device</span></span>

<span data-ttu-id="1835c-153">Wenn der Benutzergerät a als Standardgerät ausgewählt hat, entspricht "Standard-DirectSound-Gerät" "DirectSound: Device a" und "standardmäßige Wellen Gerät" dem Gerät "a".</span><span class="sxs-lookup"><span data-stu-id="1835c-153">If the user selected Device A as the default device, then "Default DirectSound Device" is equivalent to "DirectSound: Device A," and "Default WaveOut Device" is equivalent to "Device A."</span></span> <span data-ttu-id="1835c-154">Wenn der Benutzergerät B als Standardgerät auswählt, ändern sich diese Zuordnungen.</span><span class="sxs-lookup"><span data-stu-id="1835c-154">If the user selects Device B as the default device, these mappings will change.</span></span>

<span data-ttu-id="1835c-155">"DirectSound-Standardgerät" ist einem bevorzugten Verdienst zugewiesen \_ .</span><span class="sxs-lookup"><span data-stu-id="1835c-155">"Default DirectSound Device" is assigned a merit of MERIT\_PREFERRED.</span></span> <span data-ttu-id="1835c-156">Die anderen haben einen Verdienst, der \_ \_ nicht verwendet werden kann \_ .</span><span class="sxs-lookup"><span data-stu-id="1835c-156">The others have merit MERIT\_DO\_NOT\_USE.</span></span> <span data-ttu-id="1835c-157">Daher wählt Intelligent Connect immer das standardmäßige DirectSound-Gerät aus.</span><span class="sxs-lookup"><span data-stu-id="1835c-157">Therefore, Intelligent Connect will always choose the default DirectSound device.</span></span>

<span data-ttu-id="1835c-158">Der DirectSound-rendererfilter unterstützt 3D-Sound durch die DirectSound **IDirectSound3DBuffer** -und **IDirectSound3dListener** -Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="1835c-158">The DirectSound Renderer filter supports 3D sound through the DirectSound **IDirectSound3DBuffer** and **IDirectSound3dListener** interfaces.</span></span> <span data-ttu-id="1835c-159">Sie können den Filter auch nach den aktuellen Versionen dieser Schnittstellen Abfragen, **IDirectSound3DBuffer8** und **IDirectSound3dListener8**.</span><span class="sxs-lookup"><span data-stu-id="1835c-159">You can also query the filter for the current versions of these interfaces, **IDirectSound3DBuffer8** and **IDirectSound3dListener8**.</span></span> <span data-ttu-id="1835c-160">Führen Sie das Diagramm aus, bevor Sie Methoden für diese Schnittstellen aufrufen.</span><span class="sxs-lookup"><span data-stu-id="1835c-160">Run the graph before calling methods on these interfaces.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1835c-161">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1835c-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1835c-162">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="1835c-162">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




