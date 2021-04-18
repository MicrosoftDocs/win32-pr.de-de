---
description: Msyuv ist ein YUV-zu-RGB-Farb Raum Konverter-Codec.
ms.assetid: 77b00937-ac63-4b23-b546-c0896b3c57ba
title: Msyuv Color Space Converter-Codec
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 838e7cd749042b2fb97adaf0b2b4cd0378a81c07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371316"
---
# <a name="msyuv-color-space-converter-codec"></a><span data-ttu-id="fff27-103">Msyuv Color Space Converter-Codec</span><span class="sxs-lookup"><span data-stu-id="fff27-103">MSYUV Color Space Converter Codec</span></span>

<span data-ttu-id="fff27-104">Msyuv ist ein YUV-zu-RGB-Farb Raum Konverter-Codec.</span><span class="sxs-lookup"><span data-stu-id="fff27-104">MSYUV is a YUV-to-RGB color space converter codec.</span></span> <span data-ttu-id="fff27-105">Sie ermöglicht die Wiedergabe von Video Quelldaten in YUV-Formaten auf Clients, deren Videoanzeige Adapter nicht für YUV-zu-RGB-Konvertierungen in der Hardware verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="fff27-105">It enables playback of video source data in YUV formats on clients whose video display adapter cannot be used for YUV-to-RGB conversions in hardware.</span></span> <span data-ttu-id="fff27-106">Der Codec ist an Filter Diagrammen über den [AVI](avi-decompressor-filter.md) -Debug-Wrapper Filter beteiligt.</span><span class="sxs-lookup"><span data-stu-id="fff27-106">The codec participates in filter graphs through the [AVI Decompressor](avi-decompressor-filter.md) wrapper filter.</span></span>

<span data-ttu-id="fff27-107">Digitale Konferenz Kameras mit 1394-oder USB-Schnittstellen können Bilddaten in verschiedenen YUV-Formaten liefern.</span><span class="sxs-lookup"><span data-stu-id="fff27-107">Digital conferencing cameras with 1394 or USB interfaces can produce image data in various YUV formats.</span></span> <span data-ttu-id="fff27-108">Wenn die Anzeige Hardware die Konvertierung von YUV zu RGB nicht unterstützt, oder wenn die Hardware Konvertierungs Funktion aus einem anderen Grund nicht verwendet werden kann, müssen die YUV-Bilddaten in das RGB-Format konvertiert werden, bevor Sie an den Videorenderer gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="fff27-108">If the display hardware does not support on-board YUV-to-RGB conversion, or if the hardware conversion capability cannot be used for some other reason, then the YUV image data must be converted to RGB format before it is sent to the Video Renderer.</span></span>

<span data-ttu-id="fff27-109">Aufgrund der Anforderung eines [Video-Renderers](video-renderer-filter.md)für einen RGB-Eingabetyp zur Verbindungszeit kann dieser Filter während des automatischen Diagramms in ein Diagramm vom Videorenderer eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="fff27-109">Because of the [Video Renderer](video-renderer-filter.md)'s requirement for an RGB input type at connection time, this filter might be inserted into a graph upstream from the Video Renderer during automatic graph building.</span></span> <span data-ttu-id="fff27-110">Insbesondere wenn der Graph-Generator ein YUV-Format im Medientyp der Ausgabepin des Upstream-Filters erkennt, fügt der Graph-Generator den AVI-Dekompressor ein, der dann den msyuv-Codec lädt und ihn anfänglich für die Konvertierung in RGB konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="fff27-110">Specifically, if the Graph Builder detects a YUV format in the media type of the upstream filter's output pin, the Graph Builder will insert the AVI Decompressor, which will then load the MSYUV codec and configure it initially to perform the conversion to RGB.</span></span> <span data-ttu-id="fff27-111">Nachdem das Diagramm zum ersten Mal in den Zustand "wird ausgeführt" oder "angehalten" übergeht, kann der Videorendererfilter erkennen, ob der Videoanzeige Adapter die Konvertierung in die Hardware durchführen kann.</span><span class="sxs-lookup"><span data-stu-id="fff27-111">After the graph first transitions to a run or paused state, the Video Renderer filter can detect whether the video display adapter can perform the conversion in hardware.</span></span> <span data-ttu-id="fff27-112">Wenn dies der Fall ist, wird der AVI-Dekompressor benachrichtigt und der msyuv-Dienst für den Betrieb im "Pass-Through-Modus" neu konfiguriert. Dies bewirkt, dass der Codec die Konvertierung überspringt und die YUV-Bilddaten direkt auf eine DirectDraw-Overlay-Oberfläche im Videospeicher kopiert.</span><span class="sxs-lookup"><span data-stu-id="fff27-112">If it can, then the AVI Decompressor is notified and it reconfigures MSYUV to operate in "pass-through mode," which causes the codec to skip the conversion and copy the YUV image data directly onto a DirectDraw overlay surface in video memory.</span></span>

<span data-ttu-id="fff27-113">Da die Video Mischungs Renderer (VMR-7 und VMR-9) niemals GDI verwenden, benötigen Sie zum Zeitpunkt der Verbindungs Herstellung keinen RGB-Typ, und der msyuv Color Space Converter wird nie vor dem VMR in einem Diagramm eingefügt.</span><span class="sxs-lookup"><span data-stu-id="fff27-113">Because the Video Mixing Renderers (VMR-7 and VMR-9) never use GDI, they do not require an RGB type at connect time, and the MSYUV Color Space Converter is never inserted before the VMR in a graph.</span></span>

<span data-ttu-id="fff27-114">Msyuv konvertiert gepackte YUV-Formate in RGB, wie in der folgenden Liste gezeigt:</span><span class="sxs-lookup"><span data-stu-id="fff27-114">MSYUV converts packed YUV formats to RGB, as shown in the following list:</span></span>

-   <span data-ttu-id="fff27-115">Eingabeformate: UYVY, im YUY2, yvyu</span><span class="sxs-lookup"><span data-stu-id="fff27-115">Input formats: UYVY, YUY2, YVYU</span></span>
-   <span data-ttu-id="fff27-116">Ausgabeformate: RGB 8, RGB 16, RGB 24, RGB 32</span><span class="sxs-lookup"><span data-stu-id="fff27-116">Output formats: RGB 8, RGB 16, RGB 24, RGB 32</span></span>

<span data-ttu-id="fff27-117">Der msyuv Color Space Converter Codec ist ein Video Komprimierungs-Manager-Codec (VCM).</span><span class="sxs-lookup"><span data-stu-id="fff27-117">The MSYUV Color Space Converter Codec is a Video Compression Manager (VCM) codec.</span></span> <span data-ttu-id="fff27-118">Sie wird in DirectShow über den [AVI](avi-decompressor-filter.md) -Debug-Filter verwendet.</span><span class="sxs-lookup"><span data-stu-id="fff27-118">It is used in DirectShow through the [AVI Decompressor](avi-decompressor-filter.md) filter.</span></span> <span data-ttu-id="fff27-119">Verwenden Sie für einen allgemeineren Farb Konverter den [**Farb Konverter DSP**](../medfound/colorconverter.md).</span><span class="sxs-lookup"><span data-stu-id="fff27-119">For a more general-purpose color converter, use the [**Color Converter DSP**](../medfound/colorconverter.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fff27-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fff27-120">Requirements</span></span>



| <span data-ttu-id="fff27-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fff27-121">Requirement</span></span> | <span data-ttu-id="fff27-122">Wert</span><span class="sxs-lookup"><span data-stu-id="fff27-122">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fff27-123">DLL</span><span class="sxs-lookup"><span data-stu-id="fff27-123">DLL</span></span><br/> | <dl> <span data-ttu-id="fff27-124"><dt>Msyuv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fff27-124"><dt>Msyuv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fff27-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fff27-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fff27-126">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="fff27-126">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 
