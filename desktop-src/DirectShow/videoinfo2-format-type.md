---
description: VideoInfo2-Formattyp
ms.assetid: edd2013a-f0c5-4176-ba3a-a3af719ce31d
title: VideoInfo2-Formattyp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74b0f435e0e2a1b5b1d948c42a881f19300a9c6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349079"
---
# <a name="videoinfo2-format-type"></a><span data-ttu-id="77b17-103">VideoInfo2-Formattyp</span><span class="sxs-lookup"><span data-stu-id="77b17-103">VideoInfo2 Format Type</span></span>

<span data-ttu-id="77b17-104">Der bevorzugte Medientyp einer Vorschau-PIN kann ein Typ mit einem [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) -Format sein.</span><span class="sxs-lookup"><span data-stu-id="77b17-104">A preview pin's preferred media type might be a type with a [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) format.</span></span> <span data-ttu-id="77b17-105">Diese Format Struktur unterstützt besondere Features, wie z. b. Text-und Bildseiten Verhältnisse.</span><span class="sxs-lookup"><span data-stu-id="77b17-105">This format structure supports special features such as interlaced video and picture aspect ratios.</span></span>

<span data-ttu-id="77b17-106">VMR-7 und VMR-9 unterstützen [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) direkt.</span><span class="sxs-lookup"><span data-stu-id="77b17-106">The VMR-7 and the VMR-9 both support [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) directly.</span></span> <span data-ttu-id="77b17-107">Wenn Sie die VMR mit dem Decoder verbinden, wird das beste Format ausgehandelt.</span><span class="sxs-lookup"><span data-stu-id="77b17-107">When you connect the VMR to the decoder, they will negotiate the best format.</span></span> <span data-ttu-id="77b17-108">Der ältere Videorendererfilter unterstützt jedoch **VIDEOINFOHEADER2** nicht.</span><span class="sxs-lookup"><span data-stu-id="77b17-108">The older Video Renderer filter, however, does not support **VIDEOINFOHEADER2**.</span></span> <span data-ttu-id="77b17-109">Wenn Sie **VIDEOINFOHEADER2** -Format Typen mit dem Videorenderer-Filter verwenden möchten, müssen Sie den [Überlagerungs-Mischungs](overlay-mixer-filter.md) Filter in das Diagramm einfügen.</span><span class="sxs-lookup"><span data-stu-id="77b17-109">To use **VIDEOINFOHEADER2** format types with the Video Renderer filter, you must insert the [Overlay Mixer](overlay-mixer-filter.md) filter into the graph.</span></span>

1.  <span data-ttu-id="77b17-110">Auflisten der bevorzugten Medientypen im Ausgabepin des Decoder-Filters unter Verwendung der [**IPin:: enummediatypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) -Methode.</span><span class="sxs-lookup"><span data-stu-id="77b17-110">Enumerate the preferred media types on the decoder filter's output pin, using the [**IPin::EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) method.</span></span>
2.  <span data-ttu-id="77b17-111">Überprüfen Sie den ersten Medientyp in der enumerationssequenz.</span><span class="sxs-lookup"><span data-stu-id="77b17-111">Check the first media type in the enumeration sequence.</span></span>
3.  <span data-ttu-id="77b17-112">Wenn der Formattyp **Format \_ VideoInfo2** ist, verbinden Sie die Ausgabe-PIN mit dem Überlagerungs-Mixer.</span><span class="sxs-lookup"><span data-stu-id="77b17-112">If the format type is **FORMAT\_VideoInfo2**, connect the output pin to the Overlay Mixer.</span></span> <span data-ttu-id="77b17-113">Verbinden Sie dann den Overlay-Mixer mit dem Videorenderer.</span><span class="sxs-lookup"><span data-stu-id="77b17-113">Then connect the Overlay Mixer to the video renderer.</span></span> <span data-ttu-id="77b17-114">(Siehe [Video Port Pins](video-port-pins.md).)</span><span class="sxs-lookup"><span data-stu-id="77b17-114">(See [Video Port Pins](video-port-pins.md).)</span></span>

<span data-ttu-id="77b17-115">Wenn Sie sich keine Gedanken über diese Features machen, müssen Sie den Overlay-Mixer nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="77b17-115">If you do not care about these features, you do not have to use the Overlay Mixer.</span></span> <span data-ttu-id="77b17-116">Verbinden Sie den Decoder direkt mit dem Videorenderer, und stattdessen wird eine Verbindung mit einem [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Format hergestellt.</span><span class="sxs-lookup"><span data-stu-id="77b17-116">Connect the decoder directly to the Video Renderer, and it will connect with a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) format instead.</span></span>

## <a name="related-topics"></a><span data-ttu-id="77b17-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="77b17-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77b17-118">Erweiterte Erfassungs Themen</span><span class="sxs-lookup"><span data-stu-id="77b17-118">Advanced Capture Topics</span></span>](advanced-capture-topics.md)
</dt> <dt>

[<span data-ttu-id="77b17-119">Verwenden des Overlay-Mischers bei der Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="77b17-119">Using the Overlay Mixer in Video Capture</span></span>](using-the-overlay-mixer-in-video-capture.md)
</dt> </dl>

 

 



