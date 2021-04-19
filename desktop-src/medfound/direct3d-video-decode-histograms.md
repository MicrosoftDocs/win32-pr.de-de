---
description: Dieser Artikel enthält Anleitungen zum Erstellen von Histogrammen beim Decodieren von Videos mit Direct3D 11-oder 12-Video-APIs.
ms.assetid: ''
title: Direct3D-Video-Decodieren von Histogrammen
ms.topic: article
ms.date: 08/19/2019
ms.openlocfilehash: 6e25abd39ba95b669c2d76ced5f825ea80c4e3c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342789"
---
# <a name="direct3d-video-decode-histograms"></a><span data-ttu-id="719de-103">Direct3D-Video-Decodieren von Histogrammen</span><span class="sxs-lookup"><span data-stu-id="719de-103">Direct3D video decode histograms</span></span>

<span data-ttu-id="719de-104">Dieser Artikel enthält Anleitungen zum Erstellen von Histogrammen beim Decodieren von Videos mit Direct3D 11-oder 12-Video-APIs.</span><span class="sxs-lookup"><span data-stu-id="719de-104">This article contains guidance for generating histograms while decoding video using Direct3D 11 or 12 video APIs.</span></span>

## <a name="checking-the-video-device-for-histogram-capabilities"></a><span data-ttu-id="719de-105">Überprüfen des Videogeräts auf histogrammfunktionen</span><span class="sxs-lookup"><span data-stu-id="719de-105">Checking the video device for histogram capabilities</span></span>

<span data-ttu-id="719de-106">Bevor Sie versuchen, Histogramme zu generieren, müssen Sie überprüfen, ob das aktuelle Videogerät das Feature zum Decodieren von Video decodieren unterstützt.</span><span class="sxs-lookup"><span data-stu-id="719de-106">Before attempting to generated histograms, you must check to see if the current video device supports the video decode histogram feature.</span></span>

### <a name="direct3d-12"></a><span data-ttu-id="719de-107">Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="719de-107">Direct3D 12</span></span>

<span data-ttu-id="719de-108">Wenden Sie sich an [ID3D12VideoDevice:: checkfeaturesupport](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) , um die Support Details für Direct3D 12-Video Decodierungs Vorgänge zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="719de-108">Call [ID3D12VideoDevice::CheckFeatureSupport](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) to check for the support details for Direct3D 12 video decoding operations.</span></span> <span data-ttu-id="719de-109">Übergeben Sie den **D3D12_FEATURE_VIDEO_DECODE_HISTOGRAM** Wert aus der [D3D12_FEATURE_VIDEO](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_feature_video) -Enumeration, um anzugeben, dass Sie Unterstützung für Histogramme zum Decodieren von Videos anfordern.</span><span class="sxs-lookup"><span data-stu-id="719de-109">Pass the **D3D12_FEATURE_VIDEO_DECODE_HISTOGRAM** value from the [D3D12_FEATURE_VIDEO](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_feature_video) enumeration to specify that you are requesting support for video decode histograms.</span></span>

### <a name="direct3d-11"></a><span data-ttu-id="719de-110">Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="719de-110">Direct3D 11</span></span>

<span data-ttu-id="719de-111">Wenden Sie [ID3D11VideoDevice2:: checkfeaturesupport](/windows/win32/api/d3d11_4/nf-d3d11_4-id3d11videodevice2-checkfeaturesupport) an, und übergeben Sie den **D3D11_FEATURE_VIDEO_DECODER_HISTOGRAM** Wert des [D3D11_FEATURE_VIDEO](/windows/win32/api/d3d11_4/ne-d3d11_4-d3d11_feature_video) , um zu ermitteln, ob Histogramme für das aktuelle Gerät unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="719de-111">Call [ID3D11VideoDevice2::CheckFeatureSupport](/windows/win32/api/d3d11_4/nf-d3d11_4-id3d11videodevice2-checkfeaturesupport) and pass in the **D3D11_FEATURE_VIDEO_DECODER_HISTOGRAM** value of the [D3D11_FEATURE_VIDEO](/windows/win32/api/d3d11_4/ne-d3d11_4-d3d11_feature_video) to determine if histograms are supported for the current device.</span></span>

## <a name="enabling-histogram-during-decode"></a><span data-ttu-id="719de-112">Aktivieren von Histogramm während der Decodierung</span><span class="sxs-lookup"><span data-stu-id="719de-112">Enabling histogram during decode</span></span>

<span data-ttu-id="719de-113">Die Sammlung der Histogrammdaten wird vom Aufrufer aktiviert, der die Puffer bereitstellt, in denen die Histogrammdaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="719de-113">The collection of histogram data is enabled by the caller providing the buffers in which the histogram data is stored.</span></span>  <span data-ttu-id="719de-114">Ein NULL-histogrammausgabepuffer für eine bestimmte Komponente gibt an, dass die histogrammauflistung deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="719de-114">A null histogram output buffer for a given component indicates that histogram collection is disabled.</span></span>

### <a name="direct3d-12"></a><span data-ttu-id="719de-115">Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="719de-115">Direct3D 12</span></span>

<span data-ttu-id="719de-116">Um Ausgabepuffer zum Empfangen von Histogrammdaten mithilfe von Direct3D 12 bereitzustellen, sollten Sie die decodierbefehlsliste mithilfe der [ID3D12VideoDecodeCommandList1::D ecodeframe1](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist1-decodeframe1) -Methode erstellen.</span><span class="sxs-lookup"><span data-stu-id="719de-116">In order to provide output buffers to receive histogram data using Direct3D 12, you should create your decode command list using the [ID3D12VideoDecodeCommandList1::DecodeFrame1](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist1-decodeframe1) method.</span></span> <span data-ttu-id="719de-117">Diese Methode nimmt eine [D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_stream_arguments1) Struktur als Argument an.</span><span class="sxs-lookup"><span data-stu-id="719de-117">This method takes a [D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_stream_arguments1) structure as an argument.</span></span> <span data-ttu-id="719de-118">**D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1** verfügt über ein Feld vom Typ [D3D12_VIDEO_DECODE_OUTPUT_HISTOGRAM](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_histogram), mit dem Sie ein [ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) angeben können, in das Histogrammdaten ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="719de-118">**D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1** has a field of type [D3D12_VIDEO_DECODE_OUTPUT_HISTOGRAM](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_histogram), which allows you to specify an [ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) into which histogram data is output.</span></span>

### <a name="direct3d-11"></a><span data-ttu-id="719de-119">Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="719de-119">Direct3D 11</span></span>

<span data-ttu-id="719de-120">Die [ID3D11VideoContext3](/windows/win32/api/d3d11_4/nn-d3d11_4-id3d11videocontext3) -Schnittstelle stellt die [DecoderBeginFrame1](/windows/win32/api/d3d11_4/nf-d3d11_4-id3d11videocontext3-decoderbeginframe1) -Methode bereit, mit der Sie eine oder mehrere [ID3D11Buffer](/windows/win32/api/d3d11/nn-d3d11-id3d11buffer) -Schnittstellen bereitstellen können, in die die Histogrammdaten ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="719de-120">The [ID3D11VideoContext3](/windows/win32/api/d3d11_4/nn-d3d11_4-id3d11videocontext3) interface provides the [DecoderBeginFrame1](/windows/win32/api/d3d11_4/nf-d3d11_4-id3d11videocontext3-decoderbeginframe1) method, which allows you to provide one or more [ID3D11Buffer](/windows/win32/api/d3d11/nn-d3d11-id3d11buffer) interfaces into which the histogram data will be output.</span></span> <span data-ttu-id="719de-121">Der [D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT](/windows/win32/api/d3d11_4/ne-d3d11_4-d3d11_video_decoder_histogram_component) , um die Komponenten anzugeben, für die Histogrammdaten generiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="719de-121">The [D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT](/windows/win32/api/d3d11_4/ne-d3d11_4-d3d11_video_decoder_histogram_component) to specify the components for which you want histogram data to be generated.</span></span>


## <a name="buffer-format"></a><span data-ttu-id="719de-122">Puffer Format</span><span class="sxs-lookup"><span data-stu-id="719de-122">Buffer format</span></span>

<span data-ttu-id="719de-123">Die Decodierung der histogrammausgabe wird als ganzzahliger Leistungs-Counter pro Komponente in einen Puffer geschrieben.</span><span class="sxs-lookup"><span data-stu-id="719de-123">The decode histogram output is written to a buffer as an integer counter per component.</span></span>  <span data-ttu-id="719de-124">Das Puffer Format ist ein 32-Bit-Wert pro bin.</span><span class="sxs-lookup"><span data-stu-id="719de-124">The buffer format is a 32-bit value per bin.</span></span>  <span data-ttu-id="719de-125">Ein Gerät verwendet möglicherweise eine ganzzahlige Bittiefe, die kleiner als 32 Bits ist, aber 16, 24 oder 32 Bits betragen muss.</span><span class="sxs-lookup"><span data-stu-id="719de-125">A device may use an integer counter bit depth that is smaller than 32 bits, but must be 16, 24, or 32 bits.</span></span>  <span data-ttu-id="719de-126">Wenn dies der Fall ist, wird der Leistungswert in den unteren Bits gespeichert, und die oberen nicht verwendeten Bits sind 0 (null).</span><span class="sxs-lookup"><span data-stu-id="719de-126">If so, the counter value is stored in the lower bits and the upper unused bits are zero.</span></span>  <span data-ttu-id="719de-127">Wenn die Anzahl für einen "bin" den maximalen Wert überschreitet, legt das Gerät stattdessen den maximalen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="719de-127">When the count for a bin would exceed the max value, the device sets the max value instead.</span></span> <span data-ttu-id="719de-128">Von den Geräten wird die Anzahl der unterstützten Behälter gemeldet, bei der es sich um einen Wert von 2 handeln muss.</span><span class="sxs-lookup"><span data-stu-id="719de-128">Devices report the number of bins supported, which must be a value that is a power of 2.</span></span>  <span data-ttu-id="719de-129">Die Mindestanzahl von Containern, die für Geräte erforderlich sind, die dieses Feature unterstützen, ist 64.</span><span class="sxs-lookup"><span data-stu-id="719de-129">The minimum number of bins required for devices that support this feature is 64.</span></span> 

<span data-ttu-id="719de-130">Sie müssen einen Puffer mit einem abgeglichen 256-Byte-Offset und einer Größe angeben, die die unterstützte Anzahl von Containern multipliziert mit der bin-Größe (4 Bytes) für jede angeforderte Komponente ist.</span><span class="sxs-lookup"><span data-stu-id="719de-130">You must supply a buffer with a 256-byte aligned offset and a size that is the supported number of bins multiplied by the bin size (4 bytes) for each component requested.</span></span>  <span data-ttu-id="719de-131">Die bin-Platzierung wird durch Folgendes bestimmt:</span><span class="sxs-lookup"><span data-stu-id="719de-131">Bin placement is determined by:</span></span>

`binIndex = floor(value / [max value of channel + 1] * (countBins))`


<span data-ttu-id="719de-132">Wenn ein Format die nützlichen Bits einer Komponente als kleiner als die Anzahl der Speicher Bits definiert (z. b. P010 verwendet die ersten 10 Bits von 16 Bits des Komponenten Speichers), werden nur die nützlichen Bits berücksichtigt (P010 wird als 10-Bit-Wert behandelt).</span><span class="sxs-lookup"><span data-stu-id="719de-132">When a format defines the useful bits of a component as less than the number of storage bits (for example, P010 uses the top 10 bits of 16 bits of component storage), only the useful bits are considered (P010 is treated as a 10 bit value).</span></span> 

<span data-ttu-id="719de-133">Das Videogerät meldet, welche Komponenten unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="719de-133">The video device reports which components are supported.</span></span>  <span data-ttu-id="719de-134">Wenn der Aufrufer kein Histogramm für eine bestimmte Komponente wünschen, geben Sie nullptr an.</span><span class="sxs-lookup"><span data-stu-id="719de-134">If the caller does not want a histogram for a given component, they specify nullptr.</span></span>  <span data-ttu-id="719de-135">Wenn der Treiber ein Histogramm für eine bestimmte Komponente nicht unterstützt, muss der histogrammpuffer der Komponente "nullptr" lauten.</span><span class="sxs-lookup"><span data-stu-id="719de-135">If the driver does not support a histogram for a given component, that component's histogram buffer must be nullptr.</span></span>

<span data-ttu-id="719de-136">Wenn mehrere Komponenten unterstützt werden, kann die Anwendung jede beliebige Kombination von Komponenten pro Frame-Decodierung anfordern.</span><span class="sxs-lookup"><span data-stu-id="719de-136">When multiple components are supported, the application may request any combination of components per frame decode.</span></span>  <span data-ttu-id="719de-137">Wenn die Hardware z. b. die Unterstützung für y-, U-und v-Komponenten meldet, kann die Anwendung das Y-Histogramm nur für Frame 1, das U-Histogramm nur für Frame 2 und das V-Histogramm nur für Frame 3 anfordern.</span><span class="sxs-lookup"><span data-stu-id="719de-137">For example,if the hardware reports support for Y, U, and V components, the application may request the Y histogram only for frame one, the U histogram only for frame two, and the V histogram only for frame 3.</span></span>  <span data-ttu-id="719de-138">Sie können auch eine beliebige Kombination von zwei Komponenten oder alle drei Komponenten anfordern.</span><span class="sxs-lookup"><span data-stu-id="719de-138">They may also request any combination of two components or all three components.</span></span>

<span data-ttu-id="719de-139">Anwendungen stellen für jede angeforderte Komponente einen separaten Offset-und Puffer Zeiger bzw.-handle bereit.</span><span class="sxs-lookup"><span data-stu-id="719de-139">Applications supply a separate offset and buffer pointer/handle for each component requested.</span></span>  <span data-ttu-id="719de-140">Dieser Zeiger weist möglicherweise auf dieselbe Ressource wie eine andere Komponente oder eine separate Ressource hin.</span><span class="sxs-lookup"><span data-stu-id="719de-140">This pointer may point to the same resource as another component or a separate resource.</span></span>  <span data-ttu-id="719de-141">Der Offset ermöglicht das Platzieren mehrerer Komponenten im gleichen Puffer, aber der vom Offset und der histogrammgröße angegebene Ausgabebereich darf sich nicht überlappen.</span><span class="sxs-lookup"><span data-stu-id="719de-141">The offset allows placing multiple components in the same buffer, but the output region specified by the offset and the histogram size must not overlap another histogram component output.</span></span>  <span data-ttu-id="719de-142">Das Histogramm kann auch in denselben Puffer wie andere nicht zusammenhängende Inhalte geschrieben werden, z. b. bei der Verwendung in einer Ressourcen-unter Zuordnungs Strategie.</span><span class="sxs-lookup"><span data-stu-id="719de-142">The histogram may also be written to the same buffer as other unrelated content such as when being used in a resource sub-allocation strategy.</span></span>


<span data-ttu-id="719de-143">Die D3D-Laufzeit überprüft, ob Aufrufer nur das Histogramm für unterstützte Komponenten aktivieren, ob der Puffer Offset ausgerichtet ist, und dass die Puffergröße für die gemeldete Anzahl von Containern ausreichend ist.</span><span class="sxs-lookup"><span data-stu-id="719de-143">The D3D runtime validates that callers only enable histogram for supported components, that the buffer offset is aligned, and that buffer size is sufficient for the reported number of bins.</span></span>


## <a name="protected-content"></a><span data-ttu-id="719de-144">Geschützter Inhalt</span><span class="sxs-lookup"><span data-stu-id="719de-144">Protected content</span></span>

<span data-ttu-id="719de-145">Die histogrammpuffer benötigen denselben Oberflächenschutz wie die decodierausgabeoberfläche.</span><span class="sxs-lookup"><span data-stu-id="719de-145">The Histogram buffers are required to have the same surface protection as the decode output surface.</span></span> <span data-ttu-id="719de-146">Wenn die Decodierung der Ausgabe Oberfläche keine geschützte Ressource ist, darf der histogrammpuffer keine geschützte Ressource sein.</span><span class="sxs-lookup"><span data-stu-id="719de-146">If the decode output surface is not a protected resource, the histogram buffer must not be a protected resource.</span></span> <span data-ttu-id="719de-147">Wenn die Decodierung der Ausgabe Oberfläche eine geschützte Ressource ist, muss es sich bei dem Histogramm um eine geschützte Ressource handeln.</span><span class="sxs-lookup"><span data-stu-id="719de-147">If the decode output surface is protected resource, the histogram must be a protected resource.</span></span>








## <a name="related-topics"></a><span data-ttu-id="719de-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="719de-148">Related topics</span></span>

<dl> <span data-ttu-id="719de-149"><dt>
[Direct3D 12-Video-APIs](direct3d-12-video-apis.md) 
 [Media Foundation-Programmier Handbuch](media-foundation-programming-guide.md)
</dt> </span><span class="sxs-lookup"><span data-stu-id="719de-149"><dt>
[Direct3D 12 Video APIs](direct3d-12-video-apis.md)
[Media Foundation Programming Guide](media-foundation-programming-guide.md)
</dt> </span></span></dl>

 

 




