---
title: Schreiben von bildstreams
description: Schreiben von bildstreams
ms.assetid: 3a017bdd-9723-4b7f-b5e1-22838c0ba4ff
keywords:
- Advanced Systems Format (ASF), Schreiben von bildstreams
- ASF (Advanced Systems Format), Schreiben von bildstreams
- Advanced Systems Format (ASF), bildstreams
- ASF (Advanced Systems Format), bildstreams
- bildstreams, schreiben
- Streams, Schreiben von bildstreams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60daa9b62701c172d127c4cff1fb6c301edf7d86
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103948436"
---
# <a name="writing-image-streams"></a><span data-ttu-id="3da22-109">Schreiben von bildstreams</span><span class="sxs-lookup"><span data-stu-id="3da22-109">Writing Image Streams</span></span>

<span data-ttu-id="3da22-110">Die Eingaben für einen Bildstream müssen RGB-formatierte Bitmap-Bilder sein.</span><span class="sxs-lookup"><span data-stu-id="3da22-110">The inputs for an image stream must be RGB-formatted bitmap images.</span></span> <span data-ttu-id="3da22-111">Der Writer koordiniert die Komprimierung von Eingabebild Beispielen mit dem JPEG-Format.</span><span class="sxs-lookup"><span data-stu-id="3da22-111">The writer coordinates the compression of input image samples using the JPEG format.</span></span> <span data-ttu-id="3da22-112">Bevor Sie mit dem Schreiben einer Datei beginnen, die einen Bildstream enthält, müssen Sie eine Bildqualität für die Eingabe mithilfe der \_ Einstellung g wszjpgcompressionquality festlegen.</span><span class="sxs-lookup"><span data-stu-id="3da22-112">Before you begin writing a file containing an image stream, you must set an image quality for the input, using the g\_wszJPEGCompressionQuality setting.</span></span> <span data-ttu-id="3da22-113">Verwenden Sie [**IWMWriterAdvanced2:: setinputsetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) , um die Qualität auf einen **DWORD** -Wert im Bereich von 1 bis 100 festzulegen.</span><span class="sxs-lookup"><span data-stu-id="3da22-113">Use [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) to set the quality to a **DWORD** value ranging from 1 to 100.</span></span> <span data-ttu-id="3da22-114">Niedrige Werte stellen ein hohes Komprimierungs Verhältnis auf Kosten der Qualität dar, während hohe Werte hochwertige Bilder liefern, die mehr Platz benötigen.</span><span class="sxs-lookup"><span data-stu-id="3da22-114">Low values represent a high compression ratio at the expense of quality, while high values produce high quality images that require more space.</span></span>

<span data-ttu-id="3da22-115">Bildstreams erfordern häufig größere Puffer Fenster als normale Videostreams.</span><span class="sxs-lookup"><span data-stu-id="3da22-115">Image streams often require larger buffer windows than ordinary video streams.</span></span> <span data-ttu-id="3da22-116">Die genaue Größe hängt von der Art des Bilds und der Bildqualität ab, und zwar neben anderen Faktoren.</span><span class="sxs-lookup"><span data-stu-id="3da22-116">The exact size required depends on the type of image and the image quality, among other factors.</span></span> <span data-ttu-id="3da22-117">Verwenden Sie Testversion und Fehler, um die geeignete Größe für die Abbilder zu ermitteln, die Sie verarbeiten möchten.</span><span class="sxs-lookup"><span data-stu-id="3da22-117">Use trial and error to determine the appropriate size for the images you intend to process.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3da22-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3da22-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3da22-119">**Bildstreams**</span><span class="sxs-lookup"><span data-stu-id="3da22-119">**Image Streams**</span></span>](image-streams.md)
</dt> <dt>

[<span data-ttu-id="3da22-120">**So legen Sie Eingabeeinstellungen fest**</span><span class="sxs-lookup"><span data-stu-id="3da22-120">**To Set Input Settings**</span></span>](to-set-input-settings.md)
</dt> <dt>

[<span data-ttu-id="3da22-121">**Schreiben von ASF-Dateien**</span><span class="sxs-lookup"><span data-stu-id="3da22-121">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




