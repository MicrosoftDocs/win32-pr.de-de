---
description: Die MFT für die Videostabilisierung ist eine Microsoft Media Foundation Transformation (MFT), die eine Bildstabilisierung für einen Videostream ausführt.
ms.assetid: BBC42190-08E4-4C3B-972A-FD30621A6CC1
title: Videostabilisierung MFT (camerauicontrol. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65eb64b05e41842b1f7b3ad2e49a6c064be08f0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373976"
---
# <a name="video-stabilization-mft"></a><span data-ttu-id="bf8b6-103">Videostabilisierung-MFT</span><span class="sxs-lookup"><span data-stu-id="bf8b6-103">Video Stabilization MFT</span></span>

<span data-ttu-id="bf8b6-104">Die MFT für die Videostabilisierung ist eine Microsoft Media Foundation Transformation (MFT), die eine Bildstabilisierung für einen Videostream ausführt.</span><span class="sxs-lookup"><span data-stu-id="bf8b6-104">The video stabilization MFT is a Microsoft Media Foundation transform (MFT) that performs image stabilization on a video stream.</span></span>

## <a name="clsid"></a><span data-ttu-id="bf8b6-105">CLSID</span><span class="sxs-lookup"><span data-stu-id="bf8b6-105">CLSID</span></span>

<span data-ttu-id="bf8b6-106">CLSID \_ cmsvideodspmft</span><span class="sxs-lookup"><span data-stu-id="bf8b6-106">CLSID\_CMSVideoDSPMFT</span></span>

## <a name="interfaces"></a><span data-ttu-id="bf8b6-107">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="bf8b6-107">Interfaces</span></span>

-   [<span data-ttu-id="bf8b6-108">**IMF-Transformation**</span><span class="sxs-lookup"><span data-stu-id="bf8b6-108">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [<span data-ttu-id="bf8b6-109">**Imfattributes**</span><span class="sxs-lookup"><span data-stu-id="bf8b6-109">**IMFAttributes**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
-   [<span data-ttu-id="bf8b6-110">**IMF-Empfehlung**</span><span class="sxs-lookup"><span data-stu-id="bf8b6-110">**IMFQualityAdvise**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [<span data-ttu-id="bf8b6-111">**IMFQualityAdvise2**</span><span class="sxs-lookup"><span data-stu-id="bf8b6-111">**IMFQualityAdvise2**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [<span data-ttu-id="bf8b6-112">**Imediaextension**</span><span class="sxs-lookup"><span data-stu-id="bf8b6-112">**IMediaExtension**</span></span>](/uwp/api/Windows.Media.IMediaExtension?view=winrt-19041)

## <a name="input-formats"></a><span data-ttu-id="bf8b6-113">Eingabeformate</span><span class="sxs-lookup"><span data-stu-id="bf8b6-113">Input Formats</span></span>

<span data-ttu-id="bf8b6-114">Der Eingabe Medientyp und die Untertypen, die von der Video Stabilisierungs-MFT für unkomprimierte Videos akzeptiert werden, lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="bf8b6-114">The input media type and sub-type combinations accepted by the video stabilization MFT for uncompressed video are:</span></span>

-   <span data-ttu-id="bf8b6-115">**MediaType- \_ Video**</span><span class="sxs-lookup"><span data-stu-id="bf8b6-115">**MEDIATYPE\_VIDEO**</span></span>
-   <span data-ttu-id="bf8b6-116">**Mediasubtype \_ NV12**</span><span class="sxs-lookup"><span data-stu-id="bf8b6-116">**MEDIASUBTYPE\_NV12**</span></span>
-   <span data-ttu-id="bf8b6-117">**Mediasubtype \_ im YUY2**</span><span class="sxs-lookup"><span data-stu-id="bf8b6-117">**MEDIASUBTYPE\_YUY2**</span></span>

## <a name="output-formats"></a><span data-ttu-id="bf8b6-118">Ausgabeformate</span><span class="sxs-lookup"><span data-stu-id="bf8b6-118">Output Formats</span></span>

<span data-ttu-id="bf8b6-119">Der von der Video Stabilisierungs-MFT akzeptierte Ausgabe Medientyp und untergeordnete typkombinationen lauten:</span><span class="sxs-lookup"><span data-stu-id="bf8b6-119">The output media type and sub-type combinations accepted by the video stabilization MFT are:</span></span>

-   <span data-ttu-id="bf8b6-120">**MediaType- \_ Video**</span><span class="sxs-lookup"><span data-stu-id="bf8b6-120">**MEDIATYPE\_VIDEO**</span></span>
-   <span data-ttu-id="bf8b6-121">**Mediasubtype \_ NV12**</span><span class="sxs-lookup"><span data-stu-id="bf8b6-121">**MEDIASUBTYPE\_NV12**</span></span>

<span data-ttu-id="bf8b6-122">Der Eingabe Medientyp muss vor dem Ausgabe Medientyp festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="bf8b6-122">The input media type must be set before the output media type.</span></span> <span data-ttu-id="bf8b6-123">In den meisten Fällen stellt die eingeschränkte Formatunterstützung kein Problem dar, da die Pipeline automatisch die erforderlichen Farb Konvertierungen einfügt.</span><span class="sxs-lookup"><span data-stu-id="bf8b6-123">In most situations, the limited format support is not an issue because the pipeline automatically inserts the necessary color conversions.</span></span>

<span data-ttu-id="bf8b6-124">Die MFT-Komponente für die Videostabilisierung ist in der Lage, sich bei Eingabe Änderungen dynamisch zu ändern.</span><span class="sxs-lookup"><span data-stu-id="bf8b6-124">The video stabilization MFT component is capable of dynamic format change when input changes.</span></span> <span data-ttu-id="bf8b6-125">Wenn sich die Größe des Eingabe Bilds ändert oder der Untertyp geändert wird, löst er eine dynamische Formatänderung im Ausgabestream aus.</span><span class="sxs-lookup"><span data-stu-id="bf8b6-125">When the input picture size changes or the subtype changes, it will trigger a dynamic format change on the output stream.</span></span>

<span data-ttu-id="bf8b6-126">Die MFT für die Videostabilisierung führt in den folgenden Fällen zu einer Farbkonvertierung:</span><span class="sxs-lookup"><span data-stu-id="bf8b6-126">The video stabilization MFT will do color conversion in the following cases:</span></span>

-   <span data-ttu-id="bf8b6-127">Wenn das Eingabeformat **mediasubtype \_ im YUY2** ist.</span><span class="sxs-lookup"><span data-stu-id="bf8b6-127">When the input format is **MEDIASUBTYPE\_YUY2**.</span></span>
-   <span data-ttu-id="bf8b6-128">Wenn der Microsoft DirectX 9,0-Kompatibilitätsmodus verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bf8b6-128">When Microsoft DirectX 9.0 compatibility mode is used.</span></span>

### <a name="attributes"></a><span data-ttu-id="bf8b6-129">Attribute</span><span class="sxs-lookup"><span data-stu-id="bf8b6-129">Attributes</span></span>

<span data-ttu-id="bf8b6-130">Die folgenden Attribute werden von der Video Stabilisierungs-MFT über die [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstelle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bf8b6-130">The following attributes are supported by the video stabilization MFT through the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

-   <span data-ttu-id="bf8b6-131">Das Attribut [MF \_ videodsp \_ Mode](mf-videodsp-mode.md) versetzt die Videostabilisierung in den Stabilisierungs Modus oder den Pass-Through-Modus.</span><span class="sxs-lookup"><span data-stu-id="bf8b6-131">The attribute [MF\_VIDEODSP\_MODE](mf-videodsp-mode.md) puts the video stabilization MFT into either stabilization mode or pass-through mode.</span></span> <span data-ttu-id="bf8b6-132">Die Anwendung sollte [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) für den GUID- **MF- \_ videodsp- \_ Typ** mit einer Ganzzahl aufrufen, die einem der folgenden gültigen Werte entspricht: **mfvideodspmode \_ Stabilisierung** = 4, **mfvideodspmode \_ Passthrough** = 1.</span><span class="sxs-lookup"><span data-stu-id="bf8b6-132">The application should call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) on the GUID **MF\_VIDEODSP\_TYPE** with an integer corresponding to one of the following valid values: **MFVideoDSPMode\_Stabilization** = 4, **MFVideoDSPMode\_Passthrough** = 1.</span></span> <span data-ttu-id="bf8b6-133">Der MF- \_ videodsp- \_ Modus kann jederzeit während der Wiedergabe geändert werden.</span><span class="sxs-lookup"><span data-stu-id="bf8b6-133">MF\_VIDEODSP\_MODE can be changed at any time during playback.</span></span> <span data-ttu-id="bf8b6-134">Dies bewirkt eine Änderung des dynamischen Modus.</span><span class="sxs-lookup"><span data-stu-id="bf8b6-134">This causes a dynamic mode change.</span></span> <span data-ttu-id="bf8b6-135">Die Ausgabe wird nach dem Ändern des Attributs entweder nach einem 16-oder 2-Rahmen (abhängig vom Latenz Modus) zu "stabilisiert" oder "durchlaufen" gewechselt.</span><span class="sxs-lookup"><span data-stu-id="bf8b6-135">The output will switch to either stabilized or pass through after either 16 or 2 frames (depending on the latency mode) after the attribute is changed.</span></span>
-   <span data-ttu-id="bf8b6-136">Das Attribut [MF \_ niedrige \_ Latenz](mf-low-latency.md) versetzt die Videostabilisierung in den Modus mit niedriger Latenz oder den Modus für hohe Qualität.</span><span class="sxs-lookup"><span data-stu-id="bf8b6-136">The attribute [MF\_LOW\_LATENCY](mf-low-latency.md) puts the video stabilization MFT into either low latency mode or high quality mode.</span></span> <span data-ttu-id="bf8b6-137">Die Anwendung sollte [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) für die GUID- **MF- \_ niedrige \_ Latenz** mit einer Ganzzahl, die einem der folgenden gültigen Werte entspricht, anrufen: geringe Latenz = 1 hohe Qualität = 0</span><span class="sxs-lookup"><span data-stu-id="bf8b6-137">The application should call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) on the GUID **MF\_LOW\_LATENCY** with an integer corresponding to one of the following valid values: Low latency = 1 High Quality = 0</span></span>
-   <span data-ttu-id="bf8b6-138">Das Attribut [MF \_ sa \_ D3D11 \_ bindflags](mf-sa-d3d11-bindflags.md) wird von der Pipeline verwendet, um die D3D11-Bindungsflags anzugeben, mit denen die Ausgabe Beispiele erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="bf8b6-138">The attribute [MF\_SA\_D3D11\_BINDFLAGS](mf-sa-d3d11-bindflags.md) is used by the pipeline to specify the D3D11 bind flags to create the output samples with.</span></span> <span data-ttu-id="bf8b6-139">Eine beliebige Kombination von Werten aus der [**D3D11 \_ Bind- \_ Flag**](/windows/win32/api/d3d11/ne-d3d11-d3d11_bind_flag) -Enumeration ist gültig.</span><span class="sxs-lookup"><span data-stu-id="bf8b6-139">Any combination of values from the [**D3D11\_BIND\_FLAG**](/windows/win32/api/d3d11/ne-d3d11-d3d11_bind_flag) enumeration is valid.</span></span>
-   <span data-ttu-id="bf8b6-140">Die **\_ \_ Mindestanzahl von \_ Ausgabe \_ Beispielen \_** für das Attribut MF wird von der Pipeline verwendet, um die Mindestanzahl von Samplings anzugeben, die von dieser Komponente bei der Ausgabe unterstützt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="bf8b6-140">The attribute **MF\_SA\_MINIMUM\_OUTPUT\_SAMPLE\_COUNT** is used by the pipeline to specify the minimum number of samples that this component must support on output.</span></span>
-   <span data-ttu-id="bf8b6-141">Das Attribut [mfsampleextension \_ videodspmode](mfsampleextension-videodspmode.md) wird für jedes durch die Stabilisierung erzeugte Beispiel festgelegt, um den effektiven [MF- \_ videodsp- \_ Modus](mf-videodsp-mode.md) anzugeben, der auf das Beispiel angewendet wurde (unabhängig davon, ob das Beispiel stabilisiert wurde).</span><span class="sxs-lookup"><span data-stu-id="bf8b6-141">The attribute [MFSampleExtension\_VideoDSPMode](mfsampleextension-videodspmode.md) is set on every sample produced by stabilization to indicate the effective [MF\_VIDEODSP\_MODE](mf-videodsp-mode.md) applied to that sample (whether or not the sample was stabilized).</span></span> <span data-ttu-id="bf8b6-142">Unter bestimmten Bedingungen werden Stichproben möglicherweise nicht stabilisiert (aufgrund einer hohen Systemlast oder von Anforderungen des Benutzers).</span><span class="sxs-lookup"><span data-stu-id="bf8b6-142">Under certain conditions, samples may not be stabilized (due to high system load, or requests by the user).</span></span> <span data-ttu-id="bf8b6-143">Dieses Attribut hat die gleichen Werte wie das MF \_ videodsp \_ mode-Attribut (**MF videodspmode- \_ Stabilisierung** und **MF videodspmode \_ Passthrough**).</span><span class="sxs-lookup"><span data-stu-id="bf8b6-143">This attribute has the same values as the MF\_VIDEODSP\_MODE attribute (**MFVideoDSPMode\_Stabilization** and **MFVideoDSPMode\_Passthrough**).</span></span> <span data-ttu-id="bf8b6-144">Wenn Sie den Wert dieses Attributs abrufen möchten, sollten Anwendungen [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) für die GUID **mfsampleextension \_ videodspmode** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="bf8b6-144">To get the value of this attribute applications should call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) on GUID **MFSampleExtension\_VideoDSPMode**.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf8b6-145">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bf8b6-145">Remarks</span></span>

<span data-ttu-id="bf8b6-146">Eine Instanz des Video Stabilisierungs-DSP kann auf eine der folgenden Arten erstellt werden:</span><span class="sxs-lookup"><span data-stu-id="bf8b6-146">An instance of the video stabilization DSP can be created in one of the following ways:</span></span>

-   <span data-ttu-id="bf8b6-147">Durch Aufrufen von [**mftenumex**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span><span class="sxs-lookup"><span data-stu-id="bf8b6-147">By calling [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span></span> <span data-ttu-id="bf8b6-148">Der Video Stabilisierungs-DSP ist unter der Kategorie **\_ \_ Video \_ Effekt der MFT-Kategorie** registriert.</span><span class="sxs-lookup"><span data-stu-id="bf8b6-148">The video stabilization DSP is registered under the **MFT\_CATEGORY\_VIDEO\_EFFECT** category.</span></span>
-   <span data-ttu-id="bf8b6-149">Durch Aufrufen der com-Funktion **CoCreateInstance** , die ihr die CLSID- **CLSID \_ cmsvideodspmft** übergibt.</span><span class="sxs-lookup"><span data-stu-id="bf8b6-149">By calling the COM function **CoCreateInstance** passing it the CLSID **CLSID\_CMSVideoDSPMFT**.</span></span> <span data-ttu-id="bf8b6-150">Um diese Methode verwenden zu können, müssen Sie "wmcodecdsp. h" einschließen und eine Verknüpfung mit "wmcodecdspuuid. lib" herstellen.</span><span class="sxs-lookup"><span data-stu-id="bf8b6-150">To use this method, you must include wmcodecdsp.h and link against wmcodecdspuuid.lib.</span></span>

<span data-ttu-id="bf8b6-151">Darüber hinaus unterstützt der videostabilisierungs-DSP die Instanziierung mithilfe von Windows-Runtime als Windows Media-Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="bf8b6-151">Additionally, the video stabilization DSP supports instantiation using Windows Runtime as a Windows Media Extension.</span></span> <span data-ttu-id="bf8b6-152">Es wird auf [**Windows. Media. videoeffects**](/uwp/api/Windows.Media.VideoEffects?view=winrt-19041)definiert, und der vollständige Name lautet "Windows. Media. videoeffects. videostabilization".</span><span class="sxs-lookup"><span data-stu-id="bf8b6-152">It is defined on the [**Windows.Media.VideoEffects**](/uwp/api/Windows.Media.VideoEffects?view=winrt-19041), and its full name is "Windows.Media.VideoEffects.VideoStabilization".</span></span>

## <a name="requirements"></a><span data-ttu-id="bf8b6-153">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bf8b6-153">Requirements</span></span>



| <span data-ttu-id="bf8b6-154">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bf8b6-154">Requirement</span></span> | <span data-ttu-id="bf8b6-155">Wert</span><span class="sxs-lookup"><span data-stu-id="bf8b6-155">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf8b6-156">Header</span><span class="sxs-lookup"><span data-stu-id="bf8b6-156">Header</span></span><br/> | <dl> <span data-ttu-id="bf8b6-157"><dt>Camerauicontrol. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf8b6-157"><dt>Camerauicontrol.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf8b6-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bf8b6-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf8b6-159">Digitale Signal Prozessoren</span><span class="sxs-lookup"><span data-stu-id="bf8b6-159">Digital Signal Processors</span></span>](windowsmediadigitalsignalprocessors.md)
</dt> <dt>

[<span data-ttu-id="bf8b6-160">**Windows.Media.VideoEffects**</span><span class="sxs-lookup"><span data-stu-id="bf8b6-160">**Windows.Media.VideoEffects**</span></span>](/uwp/api/Windows.Media.VideoEffects?view=winrt-19041)
</dt> </dl>

 

 
