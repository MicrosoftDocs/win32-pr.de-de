---
title: Funktionen zum Schreiben von Dateien
description: Funktionen zum Schreiben von Dateien
ms.assetid: 4514f463-26cf-48a4-aa0c-c25fc5a1979f
keywords:
- Windows Media-Format-SDK, Datei Schreibfunktionen
- Windows Media-Format-SDK, Features
- Advanced Systems Format (ASF), Datei Schreibfunktionen
- ASF (Advanced Systems Format), Datei Schreibfunktionen
- Advanced Systems Format (ASF), Features
- ASF (Advanced Systems Format), Features
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a4764a318ac7cd420296b15bb4a5818ded06384
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036932"
---
# <a name="file-writing-features"></a><span data-ttu-id="527c8-109">Funktionen zum Schreiben von Dateien</span><span class="sxs-lookup"><span data-stu-id="527c8-109">File Writing Features</span></span>

<span data-ttu-id="527c8-110">Eines der Haupt Features des Windows Media SDK ist die Möglichkeit, Dateien im Advanced Systems-Format (ASF) zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="527c8-110">One of the primary features of the Windows Media Format SDK is the ability to write files in the Advanced Systems Format (ASF).</span></span> <span data-ttu-id="527c8-111">Das Writer-Objekt wird zum Schreiben von ASF-Dateien verwendet.</span><span class="sxs-lookup"><span data-stu-id="527c8-111">The writer object is used to write ASF files.</span></span> <span data-ttu-id="527c8-112">Weitere Informationen finden Sie unter [Writer-Objekt](writer-object.md).</span><span class="sxs-lookup"><span data-stu-id="527c8-112">For more information see, [Writer Object](writer-object.md).</span></span>

<span data-ttu-id="527c8-113">Im grundlegendsten Szenario zum Schreiben von Dateien weisen Sie ein zu verwendende Profil und den Namen der zu erstellenden Datei zu.</span><span class="sxs-lookup"><span data-stu-id="527c8-113">In the most basic file writing scenario, you assign a profile to use and a name of the file to create.</span></span> <span data-ttu-id="527c8-114">Sie übergeben Beispiele nacheinander an den Writer.</span><span class="sxs-lookup"><span data-stu-id="527c8-114">You pass samples to the writer one at a time.</span></span> <span data-ttu-id="527c8-115">Wenn Sie die Übergabe von Beispielen an den Writer abgeschlossen haben, werden die zugehörigen Vorgänge abgeschlossen und die ASF-Datei abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="527c8-115">When you have finished passing samples to the writer, it finishes its operations and completes the ASF file.</span></span> <span data-ttu-id="527c8-116">Weitere Informationen zum Schreiben von grundlegenden Dateien finden Sie unter [Schreiben von ASF-Dateien](writing-asf-files.md).</span><span class="sxs-lookup"><span data-stu-id="527c8-116">For more information about basic file writing, see [Writing ASF Files](writing-asf-files.md).</span></span>

<span data-ttu-id="527c8-117">Der Writer unterstützt mehrere erweiterte Features, die in den folgenden Abschnitten erläutert werden.</span><span class="sxs-lookup"><span data-stu-id="527c8-117">The writer supports several advanced features, which are discussed in the following sections.</span></span>

-   [<span data-ttu-id="527c8-118">Ändern der Größe von Videos</span><span class="sxs-lookup"><span data-stu-id="527c8-118">Video Resizing</span></span>](video-resizing.md)
-   [<span data-ttu-id="527c8-119">Farb Raum Konvertierung</span><span class="sxs-lookup"><span data-stu-id="527c8-119">Color Space Conversion</span></span>](color-space-conversion.md)
-   [<span data-ttu-id="527c8-120">Audioprobennahme</span><span class="sxs-lookup"><span data-stu-id="527c8-120">Audio Resampling</span></span>](audio-resampling.md)
-   [<span data-ttu-id="527c8-121">Senken</span><span class="sxs-lookup"><span data-stu-id="527c8-121">Sinks</span></span>](sinks.md)
-   [<span data-ttu-id="527c8-122">Unterstützung von Wasserzeichen</span><span class="sxs-lookup"><span data-stu-id="527c8-122">Watermarking Support</span></span>](watermarking-support.md)
-   [<span data-ttu-id="527c8-123">Eingabeformate, Eingabeeinstellungen und Dateneinheiten Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="527c8-123">Input Formats, Input Settings, and Data Unit Extensions</span></span>](input-formats-input-settings-and-data-unit-extensions.md)
-   [<span data-ttu-id="527c8-124">Eingabe Format-Enumeration</span><span class="sxs-lookup"><span data-stu-id="527c8-124">Input Format Enumeration</span></span>](input-format-enumeration.md)

## <a name="related-topics"></a><span data-ttu-id="527c8-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="527c8-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="527c8-126">**Features**</span><span class="sxs-lookup"><span data-stu-id="527c8-126">**Features**</span></span>](features.md)
</dt> </dl>

 

 




