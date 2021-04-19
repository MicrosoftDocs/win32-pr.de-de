---
description: Beispiel für wavsink
ms.assetid: 9e1af25f-d55c-45db-8c76-abf814e16700
title: Beispiel für wavsink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e96ecca551b6ea3e6837f211f0afcb34818d635
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359999"
---
# <a name="wavsink-sample"></a><span data-ttu-id="1ba93-103">Beispiel für wavsink</span><span class="sxs-lookup"><span data-stu-id="1ba93-103">WavSink Sample</span></span>

<span data-ttu-id="1ba93-104">Zeigt, wie eine benutzerdefinierte Medien Senke in Microsoft Media Foundation implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="1ba93-104">Shows how to implement a custom media sink in Microsoft Media Foundation.</span></span> <span data-ttu-id="1ba93-105">Das Beispiel implementiert eine Archive-Senke, die unkomprimierte PCM-Audiodaten in eine WAV-Datei schreibt.</span><span class="sxs-lookup"><span data-stu-id="1ba93-105">The sample implements an archive sink that writes uncompressed PCM audio to a .wav file.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="1ba93-106">Gezeigte APIs</span><span class="sxs-lookup"><span data-stu-id="1ba93-106">APIs Demonstrated</span></span>

<span data-ttu-id="1ba93-107">In diesem Beispiel werden die folgenden Media Foundation Schnittstellen veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="1ba93-107">This sample demonstrates the following Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="1ba93-108">**IMF-staatink**</span><span class="sxs-lookup"><span data-stu-id="1ba93-108">**IMFClockStateSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)
-   [<span data-ttu-id="1ba93-109">**Imffinalizablemediasink**</span><span class="sxs-lookup"><span data-stu-id="1ba93-109">**IMFFinalizableMediaSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink)
-   [<span data-ttu-id="1ba93-110">**Imfmediasink**</span><span class="sxs-lookup"><span data-stu-id="1ba93-110">**IMFMediaSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)
-   [<span data-ttu-id="1ba93-111">**IMF mediatypeer Handler**</span><span class="sxs-lookup"><span data-stu-id="1ba93-111">**IMFMediaTypeHandler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler)
-   [<span data-ttu-id="1ba93-112">**IMF-Senke**</span><span class="sxs-lookup"><span data-stu-id="1ba93-112">**IMFStreamSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink)

## <a name="usage"></a><span data-ttu-id="1ba93-113">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="1ba93-113">Usage</span></span>

<span data-ttu-id="1ba93-114">Das Beispiel wavsink enthält zwei Visual Studio-Projekte:</span><span class="sxs-lookup"><span data-stu-id="1ba93-114">The WavSink sample contains two Visual Studio projects:</span></span>

-   <span data-ttu-id="1ba93-115">Wavsink. vcproj erstellt eine statische Bibliothek, die die Medien Senke-Implementierung enthält.</span><span class="sxs-lookup"><span data-stu-id="1ba93-115">WavSink.vcproj builds a static library that contains the media sink implementation.</span></span>
-   <span data-ttu-id="1ba93-116">"Writewavfile. vcproj" erstellt eine Konsolenanwendung, die die Medien Senke verwendet, um eine WAV-Datei zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1ba93-116">WriteWavFile.vcproj builds a console application that uses the media sink to produce a .wav file.</span></span> <span data-ttu-id="1ba93-117">Diese Anwendung ist mit der Bibliothek verknüpft, die vom wavsink-Projekt erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="1ba93-117">This application links to the library created by the WavSink project.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ba93-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1ba93-118">Requirements</span></span>



| <span data-ttu-id="1ba93-119">Produkt</span><span class="sxs-lookup"><span data-stu-id="1ba93-119">Product</span></span>                                                        | <span data-ttu-id="1ba93-120">Version</span><span class="sxs-lookup"><span data-stu-id="1ba93-120">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="1ba93-121">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="1ba93-121">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="1ba93-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1ba93-122">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="1ba93-123">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="1ba93-123">Downloading the Sample</span></span>

<span data-ttu-id="1ba93-124">Dieses Beispiel ist im [GitHub-Repository für klassische Windows-Beispiele](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/wavsink)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1ba93-124">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/wavsink).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1ba93-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1ba93-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ba93-126">Media Foundation-SDK-Beispiele</span><span class="sxs-lookup"><span data-stu-id="1ba93-126">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="1ba93-127">Medien senken</span><span class="sxs-lookup"><span data-stu-id="1ba93-127">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 



