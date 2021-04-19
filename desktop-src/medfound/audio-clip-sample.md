---
description: Zeigt, wie Microsoft Media Foundation verwendet wird, um Audiodaten aus einer Mediendatei zu decodieren.
ms.assetid: 29822e6b-8598-4133-b181-7fb0854553b7
title: Beispiel für Audioclip
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c0e4a3e515d08e2cafd2ab2ba451a528f3d5677
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346257"
---
# <a name="audio-clip-sample"></a><span data-ttu-id="d65cf-103">Beispiel für Audioclip</span><span class="sxs-lookup"><span data-stu-id="d65cf-103">Audio Clip Sample</span></span>

<span data-ttu-id="d65cf-104">Zeigt, wie Microsoft Media Foundation verwendet wird, um Audiodaten aus einer Mediendatei zu decodieren.</span><span class="sxs-lookup"><span data-stu-id="d65cf-104">Shows how to use Microsoft Media Foundation to decode audio from a media file.</span></span>

<span data-ttu-id="d65cf-105">Die Beispielanwendung Audioclip liest Audiodaten aus einer Mediendatei und schreibt die nicht komprimierte Audiodatei in eine Wave-Datei.</span><span class="sxs-lookup"><span data-stu-id="d65cf-105">The Audio Clip sample application reads audio data from a media file and writes the uncompressed audio to a WAVE file.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="d65cf-106">Gezeigte APIs</span><span class="sxs-lookup"><span data-stu-id="d65cf-106">APIs Demonstrated</span></span>

<span data-ttu-id="d65cf-107">In diesem Beispiel werden die folgenden Media Foundation Schnittstellen veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="d65cf-107">This sample demonstrates the following Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="d65cf-108">**IMFSourceReader**</span><span class="sxs-lookup"><span data-stu-id="d65cf-108">**IMFSourceReader**</span></span>](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader)

## <a name="usage"></a><span data-ttu-id="d65cf-109">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="d65cf-109">Usage</span></span>

<span data-ttu-id="d65cf-110">Bei diesem Beispiel handelt es sich um eine Befehlszeilen Anwendung.</span><span class="sxs-lookup"><span data-stu-id="d65cf-110">This sample is a command-line application.</span></span> <span data-ttu-id="d65cf-111">Es verwendet die folgenden Befehlszeilenargumente:</span><span class="sxs-lookup"><span data-stu-id="d65cf-111">It uses the following command-line arguments:</span></span>

``` syntax
audioclip.exe inputfile outputfile.wav
```

-   <span data-ttu-id="d65cf-112">Input file: der Name einer Datei, die einen Audiostream enthält.</span><span class="sxs-lookup"><span data-stu-id="d65cf-112">inputfile: The name of a file that contains an audio stream.</span></span>
-   <span data-ttu-id="d65cf-113">OutputFile. WAV: der Name der zu schreibenden Wave-Datei.</span><span class="sxs-lookup"><span data-stu-id="d65cf-113">outputfile.wav: The name of the WAVE file to write.</span></span>

## <a name="requirements"></a><span data-ttu-id="d65cf-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d65cf-114">Requirements</span></span>



| <span data-ttu-id="d65cf-115">Produkt</span><span class="sxs-lookup"><span data-stu-id="d65cf-115">Product</span></span>                                                        | <span data-ttu-id="d65cf-116">Version</span><span class="sxs-lookup"><span data-stu-id="d65cf-116">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="d65cf-117">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="d65cf-117">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="d65cf-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d65cf-118">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="d65cf-119">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="d65cf-119">Downloading the Sample</span></span>

<span data-ttu-id="d65cf-120">Dieses Beispiel ist im [GitHub-Repository für klassische Windows-Beispiele](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/AudioClip)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d65cf-120">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/AudioClip).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d65cf-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d65cf-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d65cf-122">Media Foundation-SDK-Beispiele</span><span class="sxs-lookup"><span data-stu-id="d65cf-122">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="d65cf-123">Quell Leser</span><span class="sxs-lookup"><span data-stu-id="d65cf-123">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="d65cf-124">Tutorial: Decodieren von Audiodaten</span><span class="sxs-lookup"><span data-stu-id="d65cf-124">Tutorial: Decoding Audio</span></span>](tutorial--decoding-audio.md)
</dt> </dl>

 

 



