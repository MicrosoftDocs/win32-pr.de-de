---
description: .
ms.assetid: BE89E2E0-711F-4BD5-BB86-AA4CCA2D3E7F
title: Verwenden des Senke Writers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e46157eae6fe851468515f9d9653adb33918ebb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959367"
---
# <a name="using-the-sink-writer"></a><span data-ttu-id="e2cdd-103">Verwenden des Senke Writers</span><span class="sxs-lookup"><span data-stu-id="e2cdd-103">Using the Sink Writer</span></span>

## <a name="overview"></a><span data-ttu-id="e2cdd-104">Übersicht</span><span class="sxs-lookup"><span data-stu-id="e2cdd-104">Overview</span></span>

### <a name="file-container-types"></a><span data-ttu-id="e2cdd-105">Datei Container Typen</span><span class="sxs-lookup"><span data-stu-id="e2cdd-105">File Container Types</span></span>

<span data-ttu-id="e2cdd-106">Der senkwriter verfügt über integrierte Unterstützung für mehrere Datei Containertypen.</span><span class="sxs-lookup"><span data-stu-id="e2cdd-106">The sink writer has built-in support for several file container types.</span></span> <span data-ttu-id="e2cdd-107">Eine komplette Liste finden Sie unter [MF \_ transcode \_ ContainerType](mf-transcode-containertype.md).</span><span class="sxs-lookup"><span data-stu-id="e2cdd-107">For a complete list, see [MF\_TRANSCODE\_CONTAINERTYPE](mf-transcode-containertype.md).</span></span> <span data-ttu-id="e2cdd-108">Sie können zusätzliche Containertypen unterstützen, indem Sie eine benutzerdefinierte [Medien Senke](media-sinks.md)schreiben.</span><span class="sxs-lookup"><span data-stu-id="e2cdd-108">You can support additional container types by writing a custom [media sink](media-sinks.md).</span></span> <span data-ttu-id="e2cdd-109">Der Datei Container wird beim Erstellen einer neuen Instanz des Senke Writers angegeben.</span><span class="sxs-lookup"><span data-stu-id="e2cdd-109">The file container is specified when you create a new instance of the sink writer.</span></span>

### <a name="stream-formats"></a><span data-ttu-id="e2cdd-110">Streamformate</span><span class="sxs-lookup"><span data-stu-id="e2cdd-110">Stream Formats</span></span>

<span data-ttu-id="e2cdd-111">Die Anwendung muss für jeden Stream Folgendes angeben:</span><span class="sxs-lookup"><span data-stu-id="e2cdd-111">For each stream, the application must specify the following.</span></span>

-   <span data-ttu-id="e2cdd-112">Das *Eingabeformat* ist das Format, das die Anwendung an den senkenwriter sendet.</span><span class="sxs-lookup"><span data-stu-id="e2cdd-112">The *input format* is the format that the application sends to the sink writer.</span></span>
-   <span data-ttu-id="e2cdd-113">Das *Ausgabeformat* ist das Format, das in die Datei geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="e2cdd-113">The *output format* is the format that will be written to the file.</span></span>

<span data-ttu-id="e2cdd-114">Die Eingabe-und Ausgabeformate können entweder komprimiert oder unkomprimiert sein.</span><span class="sxs-lookup"><span data-stu-id="e2cdd-114">The input and output formats can be either compressed or uncompressed.</span></span> <span data-ttu-id="e2cdd-115">Der Senke Writer unterstützt die folgenden Kombinationen:</span><span class="sxs-lookup"><span data-stu-id="e2cdd-115">The sink writer supports the following combinations:</span></span>

-   <span data-ttu-id="e2cdd-116">Unkomprimierte Eingabe mit komprimierter Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="e2cdd-116">Uncompressed input with compressed output.</span></span> <span data-ttu-id="e2cdd-117">Dies ist der typische Fall, der zum Codieren oder transcodieren von Szenarien verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e2cdd-117">This is the typical case, and is used for encoding or transcoding scenarios.</span></span> <span data-ttu-id="e2cdd-118">Es muss ein Microsoft Media Foundation Encoder verfügbar sein, der den Eingabetyp akzeptiert und in den Ausgabetyp codiert.</span><span class="sxs-lookup"><span data-stu-id="e2cdd-118">A Microsoft Media Foundation encoder must be available that accepts the input type and encodes to the output type.</span></span>
-   <span data-ttu-id="e2cdd-119">Komprimierte Eingabe mit identischer Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="e2cdd-119">Compressed input with identical output.</span></span> <span data-ttu-id="e2cdd-120">Verwenden Sie diese Kombination, um eine Datei ohne Transcodierung zu reaktivieren.</span><span class="sxs-lookup"><span data-stu-id="e2cdd-120">Use this combination to remux a file without transcoding.</span></span>
-   <span data-ttu-id="e2cdd-121">Unkomprimierte Eingabe mit identischer Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="e2cdd-121">Uncompressed input with identical output.</span></span> <span data-ttu-id="e2cdd-122">Verwenden Sie diese Kombination, um unkomprimierte Audiodaten oder Videos in einen Datei Container zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="e2cdd-122">Use this combination to write uncompressed audio or video to a file container.</span></span>

<span data-ttu-id="e2cdd-123">Der sendende Writer unterstützt keine Videogröße, keine Frame-Raten-Konvertierung oder audioprobennahme, es sei denn, diese Funktionen werden vom Encoder bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="e2cdd-123">The sink writer does not support video resizing, frame-rate conversion, or audio resampling, unless these functions are provided by the encoder.</span></span> <span data-ttu-id="e2cdd-124">Andernfalls kann die Anwendung [digitale Signal Prozessoren](windowsmediadigitalsignalprocessors.md) verwenden, um die Eingabedaten zu konvertieren, bevor die Daten an das</span><span class="sxs-lookup"><span data-stu-id="e2cdd-124">Otherwise, the application can use [Digital Signal Processors](windowsmediadigitalsignalprocessors.md) to convert the input data, before sending the data to the</span></span>

## <a name="creating-the-sink-writer"></a><span data-ttu-id="e2cdd-125">Erstellen des Senke Writers</span><span class="sxs-lookup"><span data-stu-id="e2cdd-125">Creating the Sink Writer</span></span>

<span data-ttu-id="e2cdd-126">Es gibt zwei Funktionen, die den Senke-Writer erstellen:</span><span class="sxs-lookup"><span data-stu-id="e2cdd-126">There are two functions that create the sink writer:</span></span>

-   <span data-ttu-id="e2cdd-127">[**Mfkreatesinkschreiterfromurl**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) übernimmt die URL einer Ausgabedatei oder einen Zeiger auf einen Bytestream.</span><span class="sxs-lookup"><span data-stu-id="e2cdd-127">[**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) takes the URL of an output file or a pointer to a byte stream.</span></span> <span data-ttu-id="e2cdd-128">Diese Funktion erstellt die Medien Senke intern.</span><span class="sxs-lookup"><span data-stu-id="e2cdd-128">This function creates the media sink internally.</span></span>
-   <span data-ttu-id="e2cdd-129">[**Mfkreatesinkschreiterfrommediasink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink) übernimmt einen Zeiger auf eine Medien Senke, die bereits von der Anwendung erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="e2cdd-129">[**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink) takes a pointer to a media sink that has already been created by the application.</span></span>

<span data-ttu-id="e2cdd-130">Wenn Sie eine der integrierten Medien senken verwenden, ist die [**mfkreatesinkschreiterfromurl**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) -Funktion vorzuziehen, da der Aufrufer die Medien Senke nicht konfigurieren muss.</span><span class="sxs-lookup"><span data-stu-id="e2cdd-130">If you are using one of the built-in media sinks, the [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) function is preferable, because the caller does not need to configure the media sink.</span></span>

<span data-ttu-id="e2cdd-131">Die [**MF | atesinkschreiterfromurl**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) -Methode bietet verschiedene Optionen zum Angeben des Typs des Datei Containers.</span><span class="sxs-lookup"><span data-stu-id="e2cdd-131">The [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) method provides several options for specifying the type of file container.</span></span> <span data-ttu-id="e2cdd-132">Im einfachsten Fall verwendet die-Funktion die Dateinamenerweiterung in der URL, um den Datei Container auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="e2cdd-132">In the simplest case, the function uses the file name extension in the URL to select the file container.</span></span> <span data-ttu-id="e2cdd-133">Weitere Informationen finden Sie auf der Seite Funktionsreferenz.</span><span class="sxs-lookup"><span data-stu-id="e2cdd-133">For details, refer to the function reference page.</span></span>

<span data-ttu-id="e2cdd-134">Der folgende Code gibt z. b. den Dateinamen "Output. wmv" für die URL an.</span><span class="sxs-lookup"><span data-stu-id="e2cdd-134">For example, the following code specifies the file name "output.wmv" for the URL.</span></span> <span data-ttu-id="e2cdd-135">Basierend auf der Dateinamenerweiterung lädt der senkenwriter die [ASF-Medien Senke](asf-media-sinks.md) , um eine ASF-Datei (Advanced Systems Format) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e2cdd-135">Based on the file name extension, the sink writer will load the [ASF Media Sink](asf-media-sinks.md) to create an Advanced Systems Format (ASF) file.</span></span>


```C++
    HRESULT hr = MFCreateSinkWriterFromURL(L"output.wmv", NULL, NULL, &pSinkWriter);
```



<span data-ttu-id="e2cdd-136">Im Fall von [**mfkreatesinkschreibfrommediasink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)wird der Dateityp von der Medien Senke bestimmt.</span><span class="sxs-lookup"><span data-stu-id="e2cdd-136">In the case of [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink), the file type is determined by the media sink.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e2cdd-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e2cdd-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2cdd-138">Senke-Writer</span><span class="sxs-lookup"><span data-stu-id="e2cdd-138">Sink Writer</span></span>](sink-writer.md)
</dt> </dl>

 

 



