---
description: Video Erfassungs Schnittstellen
ms.assetid: a7ec6607-d6fe-4cf4-b3f2-8636c4d15982
title: Video Erfassungs Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7c88ab86833a3570789dee311b36d49f382c9cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356572"
---
# <a name="video-capture-interfaces"></a><span data-ttu-id="c464f-103">Video Erfassungs Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="c464f-103">Video Capture Interfaces</span></span>

<span data-ttu-id="c464f-104">Diese Schnittstellen unterstützen die Video Erfassung mithilfe von Microsoft® Windows® Driver Model (WDM)-Geräten oder Legacy-Microsoft® Video für Windows® (Vfw)-Geräte.</span><span class="sxs-lookup"><span data-stu-id="c464f-104">These interfaces support video capture, using Microsoft® Windows® Driver Model (WDM) devices or legacy Microsoft® Video for Windows® (VFW) devices.</span></span>



| <span data-ttu-id="c464f-105">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="c464f-105">Interface</span></span>                                                        | <span data-ttu-id="c464f-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c464f-106">Description</span></span>                                                                                                  |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c464f-107">**Iamanalog gvideodecoder**</span><span class="sxs-lookup"><span data-stu-id="c464f-107">**IAMAnalogVideoDecoder**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamanalogvideodecoder)           | <span data-ttu-id="c464f-108">Steuern der Video Digitalisierung auf einer WDM-Video Erfassungs Karte.</span><span class="sxs-lookup"><span data-stu-id="c464f-108">Control video digitization on a WDM video capture card.</span></span>                                                      |
| [<span data-ttu-id="c464f-109">**Iambufferaushandlung**</span><span class="sxs-lookup"><span data-stu-id="c464f-109">**IAMBufferNegotiation**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation)             | <span data-ttu-id="c464f-110">Steuern Sie, wie eine PIN Puffer ordnet.</span><span class="sxs-lookup"><span data-stu-id="c464f-110">Control how a pin allocates buffers.</span></span>                                                                         |
| [<span data-ttu-id="c464f-111">**Iamcopycapturefileprogress**</span><span class="sxs-lookup"><span data-stu-id="c464f-111">**IAMCopyCaptureFileProgress**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamcopycapturefileprogress) | <span data-ttu-id="c464f-112">Rückruf Schnittstelle zum Empfangen des Fortschritts eines Datei Kopiervorgangs.</span><span class="sxs-lookup"><span data-stu-id="c464f-112">Callback interface to receive the progress of a file copy operation.</span></span>                                         |
| [<span data-ttu-id="c464f-113">**Iamcrossbar**</span><span class="sxs-lookup"><span data-stu-id="c464f-113">**IAMCrossbar**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar)                               | <span data-ttu-id="c464f-114">Erstellen Sie eine Hardware Verbindung zwischen einer WDM-Audiodatei oder Videoquelle und einem WDM-Erfassungsgerät.</span><span class="sxs-lookup"><span data-stu-id="c464f-114">Create a hardware connection between a WDM audio or video source and a WDM capture device.</span></span>                   |
| [<span data-ttu-id="c464f-115">**IAMDroppedFrames**</span><span class="sxs-lookup"><span data-stu-id="c464f-115">**IAMDroppedFrames**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes)                     | <span data-ttu-id="c464f-116">Abfragen eines Erfassungs Filters zur Erfassung der Leistung.</span><span class="sxs-lookup"><span data-stu-id="c464f-116">Query a capture filter about capture performance.</span></span>                                                            |
| [<span data-ttu-id="c464f-117">**Iamstreamcontrol**</span><span class="sxs-lookup"><span data-stu-id="c464f-117">**IAMStreamControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol)                     | <span data-ttu-id="c464f-118">Steuern Sie die Start-und Endzeit der einzelnen Streams.</span><span class="sxs-lookup"><span data-stu-id="c464f-118">Control the start and stop times of individual streams.</span></span>                                                      |
| [<span data-ttu-id="c464f-119">**Iamstreamconfig**</span><span class="sxs-lookup"><span data-stu-id="c464f-119">**IAMStreamConfig**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig)                       | <span data-ttu-id="c464f-120">Das Ausgabeformat des Erfassungs Filters wird abgefragt und festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c464f-120">Query and set the capture filter's output format.</span></span>                                                            |
| [<span data-ttu-id="c464f-121">**Iamvfwcapturedialogfelder**</span><span class="sxs-lookup"><span data-stu-id="c464f-121">**IAMVfwCaptureDialogs**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamvfwcapturedialogs)             | <span data-ttu-id="c464f-122">Anzeigen der von VFW-Erfassungs Treibern bereitgestellten Dialogfelder.</span><span class="sxs-lookup"><span data-stu-id="c464f-122">Display the dialog boxes provided by VFW capture drivers.</span></span>                                                    |
| [<span data-ttu-id="c464f-123">**IAMVideoControl**</span><span class="sxs-lookup"><span data-stu-id="c464f-123">**IAMVideoControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamvideocontrol)                       | <span data-ttu-id="c464f-124">Steuern Sie das Bild von einem Erfassungsgerät.</span><span class="sxs-lookup"><span data-stu-id="c464f-124">Control the picture from a capture device.</span></span>                                                                   |
| [<span data-ttu-id="c464f-125">**IAMVideoProcAmp**</span><span class="sxs-lookup"><span data-stu-id="c464f-125">**IAMVideoProcAmp**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp)                       | <span data-ttu-id="c464f-126">Passen Sie die Qualitäten eines Videosignals an, z. b. Helligkeit, Kontrast, Farbton, Sättigung, Gamma und Schärfe.</span><span class="sxs-lookup"><span data-stu-id="c464f-126">Adjust the qualities of a video signal, such as brightness, contrast, hue, saturation, gamma, and sharpness.</span></span> |
| [<span data-ttu-id="c464f-127">**ICaptureGraphBuilder2**</span><span class="sxs-lookup"><span data-stu-id="c464f-127">**ICaptureGraphBuilder2**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2)           | <span data-ttu-id="c464f-128">Buildfilterdiagramme für die Video Erfassung.</span><span class="sxs-lookup"><span data-stu-id="c464f-128">Build filter graphs for video capture.</span></span>                                                                       |
| [<span data-ttu-id="c464f-129">**IFileSinkFilter2**</span><span class="sxs-lookup"><span data-stu-id="c464f-129">**IFileSinkFilter2**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2)                     | <span data-ttu-id="c464f-130">Geben Sie den Namen und die Attribute einer Ausgabedatei an.</span><span class="sxs-lookup"><span data-stu-id="c464f-130">Specify the name and attributes of an output file.</span></span>                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="c464f-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c464f-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c464f-132">Externe Geräte Steuerungs Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="c464f-132">External Device Control Interfaces</span></span>](external-device-control-interfaces.md)
</dt> <dt>

[<span data-ttu-id="c464f-133">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="c464f-133">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



