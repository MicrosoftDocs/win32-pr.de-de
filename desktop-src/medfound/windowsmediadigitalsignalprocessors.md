---
description: Digitale Signal Prozessoren
ms.assetid: cd3952ca-3958-4944-8fde-f0163a47bff9
title: Digitale Signal Prozessoren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0961554d9c9902e68f74c6b2b57662b23846614f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106373415"
---
# <a name="digital-signal-processors"></a><span data-ttu-id="0c317-103">Digitale Signal Prozessoren</span><span class="sxs-lookup"><span data-stu-id="0c317-103">Digital Signal Processors</span></span>

<span data-ttu-id="0c317-104">In diesem Abschnitt werden die von Windows bereitgestellten DSP-Objekte (Digital Signal Processor) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0c317-104">This section describes the digital signal processor (DSP) objects provided by Windows.</span></span>

<span data-ttu-id="0c317-105">Microsoft verwendet den Begriff *Digital Signal Processor* zum Festlegen eines Satzes von COM-Objekten, die Transformationen für nicht komprimierte Audiodaten und Videodaten ausführen.</span><span class="sxs-lookup"><span data-stu-id="0c317-105">Microsoft uses the term *digital signal processor* to designate a set of COM objects that perform transformations on uncompressed audio and video data.</span></span> <span data-ttu-id="0c317-106">Die in diesem SDK beschriebenen DSPs transformieren Audiodaten und Videos in einer Vielzahl von unkomprimierten Formaten.</span><span class="sxs-lookup"><span data-stu-id="0c317-106">The DSPs described in this SDK transform audio and video in a variety of uncompressed formats.</span></span>

<span data-ttu-id="0c317-107">Die DSPs können eigenständig oder in Kombination mit Audio-und Video Codecs verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0c317-107">The DSPs can be used by themselves, or in combination with audio and video codecs.</span></span> <span data-ttu-id="0c317-108">Mit Ausnahme von "Voice Capture DSP" implementiert jeder hier aufgeführte DSP zwei separate, aber ähnliche Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="0c317-108">With the exception of the Voice Capture DSP, each DSP listed here implements two separate but similar interfaces.</span></span>



| <span data-ttu-id="0c317-109">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="0c317-109">Interface</span></span>                              | <span data-ttu-id="0c317-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0c317-110">Description</span></span>                                 |
|----------------------------------------|---------------------------------------------|
| [<span data-ttu-id="0c317-111">**IMF-Transformation**</span><span class="sxs-lookup"><span data-stu-id="0c317-111">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)   | <span data-ttu-id="0c317-112">Kompatibel mit Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="0c317-112">Compatible with Microsoft Media Foundation.</span></span> |
| [<span data-ttu-id="0c317-113">**Imediaobject**</span><span class="sxs-lookup"><span data-stu-id="0c317-113">**IMediaObject**</span></span>](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) | <span data-ttu-id="0c317-114">Kompatibel mit DirectShow.</span><span class="sxs-lookup"><span data-stu-id="0c317-114">Compatible with DirectShow.</span></span>                 |



 

<span data-ttu-id="0c317-115">Sie können die DSPs konfigurieren, indem Sie die [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Schnittstelle verwenden, um Eigenschaften festzulegen.</span><span class="sxs-lookup"><span data-stu-id="0c317-115">You can configure the DSPs by using the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface to set properties.</span></span> <span data-ttu-id="0c317-116">Einige der DSPs verfügen über zusätzliche Schnittstellen, die Eigenschaften festlegen.</span><span class="sxs-lookup"><span data-stu-id="0c317-116">Some of the DSPs have additional interfaces that set properties.</span></span> <span data-ttu-id="0c317-117">Um diese Schnittstellen zu verwenden, nennen Sie die [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) -Methode einer beliebigen anderen Schnittstelle des DSP.</span><span class="sxs-lookup"><span data-stu-id="0c317-117">To use these interfaces, call the [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method of any other interface of the DSP.</span></span> <span data-ttu-id="0c317-118">Das Referenz Thema für die einzelnen DSP listet die unterstützten Eigenschaften, Schnittstellen und andere Funktionen auf.</span><span class="sxs-lookup"><span data-stu-id="0c317-118">The reference topic for each DSP lists the supported properties, interfaces, and other features.</span></span>

<span data-ttu-id="0c317-119">In diesem Abschnitt werden die folgenden Themen behandelt:</span><span class="sxs-lookup"><span data-stu-id="0c317-119">This section contains the following topics.</span></span>



| <span data-ttu-id="0c317-120">DSP</span><span class="sxs-lookup"><span data-stu-id="0c317-120">DSP</span></span>                                                      | <span data-ttu-id="0c317-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0c317-121">Description</span></span>                                          |
|----------------------------------------------------------|------------------------------------------------------|
| [<span data-ttu-id="0c317-122">Audioresampler-DSP</span><span class="sxs-lookup"><span data-stu-id="0c317-122">Audio Resampler DSP</span></span>](audioresampler.md)                | <span data-ttu-id="0c317-123">Konvertiert die Samplingrate eines Audiodatenstroms.</span><span class="sxs-lookup"><span data-stu-id="0c317-123">Converts the sampling rate of an audio stream.</span></span>       |
| [<span data-ttu-id="0c317-124">Farb Steuerungs Transformation (DSP)</span><span class="sxs-lookup"><span data-stu-id="0c317-124">Color Control Transform DSP</span></span>](colorcontroltransform.md) | <span data-ttu-id="0c317-125">Passt die Farbmerkmale eines Videostreams an.</span><span class="sxs-lookup"><span data-stu-id="0c317-125">Adjusts the color characteristics of a video stream.</span></span> |
| [<span data-ttu-id="0c317-126">Farb Konverter-DSP</span><span class="sxs-lookup"><span data-stu-id="0c317-126">Color Converter DSP</span></span>](colorconverter.md)                | <span data-ttu-id="0c317-127">Konvertiert einen Videostream zwischen Farbformaten.</span><span class="sxs-lookup"><span data-stu-id="0c317-127">Converts a video stream between color formats.</span></span>       |
| [<span data-ttu-id="0c317-128">Frame Rate Konverter DSP</span><span class="sxs-lookup"><span data-stu-id="0c317-128">Frame Rate Converter DSP</span></span>](framerateconverter.md)       | <span data-ttu-id="0c317-129">Ändert die Framerate eines Videodaten Stroms.</span><span class="sxs-lookup"><span data-stu-id="0c317-129">Changes the frame rate of a video stream.</span></span>            |
| [<span data-ttu-id="0c317-130">Video Resizer DSP</span><span class="sxs-lookup"><span data-stu-id="0c317-130">Video Resizer DSP</span></span>](videoresizer.md)                    | <span data-ttu-id="0c317-131">Ändert die Größe eines Videodaten Stroms.</span><span class="sxs-lookup"><span data-stu-id="0c317-131">Resizes a video stream.</span></span>                              |
| [<span data-ttu-id="0c317-132">Sprach Erfassungs-DSP</span><span class="sxs-lookup"><span data-stu-id="0c317-132">Voice Capture DSP</span></span>](voicecapturedmo.md)                 | <span data-ttu-id="0c317-133">Kapselt mehrere DSPs, die mit der sprach Erfassung verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="0c317-133">Encapsulates several DSPs related to voice capture.</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="0c317-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0c317-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c317-135">Media Foundation-Programmierreferenz</span><span class="sxs-lookup"><span data-stu-id="0c317-135">Media Foundation Programming Reference</span></span>](media-foundation-programming-reference.md)
</dt> </dl>

 

 
