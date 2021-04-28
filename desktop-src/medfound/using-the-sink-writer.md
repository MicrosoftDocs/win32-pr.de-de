---
description: Verwenden des Senkenschreibers
ms.assetid: BE89E2E0-711F-4BD5-BB86-AA4CCA2D3E7F
title: Verwenden des Senkenschreibers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa4fa472bd1a5121454b3ffb06def7082508432b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110488"
---
# <a name="using-the-sink-writer"></a><span data-ttu-id="b98fc-103">Verwenden des Senkenschreibers</span><span class="sxs-lookup"><span data-stu-id="b98fc-103">Using the Sink Writer</span></span>

## <a name="overview"></a><span data-ttu-id="b98fc-104">Übersicht</span><span class="sxs-lookup"><span data-stu-id="b98fc-104">Overview</span></span>

### <a name="file-container-types"></a><span data-ttu-id="b98fc-105">Dateicontainertypen</span><span class="sxs-lookup"><span data-stu-id="b98fc-105">File Container Types</span></span>

<span data-ttu-id="b98fc-106">Der Senkenwriter verfügt über integrierte Unterstützung für mehrere Dateicontainertypen.</span><span class="sxs-lookup"><span data-stu-id="b98fc-106">The sink writer has built-in support for several file container types.</span></span> <span data-ttu-id="b98fc-107">Eine vollständige Liste finden Sie unter [MF \_ TRANSCODE \_ CONTAINERTYPE](mf-transcode-containertype.md).</span><span class="sxs-lookup"><span data-stu-id="b98fc-107">For a complete list, see [MF\_TRANSCODE\_CONTAINERTYPE](mf-transcode-containertype.md).</span></span> <span data-ttu-id="b98fc-108">Sie können zusätzliche Containertypen unterstützen, indem Sie eine benutzerdefinierte [Mediensenke schreiben.](media-sinks.md)</span><span class="sxs-lookup"><span data-stu-id="b98fc-108">You can support additional container types by writing a custom [media sink](media-sinks.md).</span></span> <span data-ttu-id="b98fc-109">Der Dateicontainer wird angegeben, wenn Sie eine neue Instanz des Senkenwriters erstellen.</span><span class="sxs-lookup"><span data-stu-id="b98fc-109">The file container is specified when you create a new instance of the sink writer.</span></span>

### <a name="stream-formats"></a><span data-ttu-id="b98fc-110">Streamformate</span><span class="sxs-lookup"><span data-stu-id="b98fc-110">Stream Formats</span></span>

<span data-ttu-id="b98fc-111">Für jeden Stream muss die Anwendung Folgendes angeben.</span><span class="sxs-lookup"><span data-stu-id="b98fc-111">For each stream, the application must specify the following.</span></span>

-   <span data-ttu-id="b98fc-112">Das *Eingabeformat ist* das Format, das die Anwendung an den Senkenwriter sendet.</span><span class="sxs-lookup"><span data-stu-id="b98fc-112">The *input format* is the format that the application sends to the sink writer.</span></span>
-   <span data-ttu-id="b98fc-113">Das *Ausgabeformat* ist das Format, das in die Datei geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="b98fc-113">The *output format* is the format that will be written to the file.</span></span>

<span data-ttu-id="b98fc-114">Die Eingabe- und Ausgabeformate können entweder komprimiert oder unkomprimiert werden.</span><span class="sxs-lookup"><span data-stu-id="b98fc-114">The input and output formats can be either compressed or uncompressed.</span></span> <span data-ttu-id="b98fc-115">Der Senkenwriter unterstützt die folgenden Kombinationen:</span><span class="sxs-lookup"><span data-stu-id="b98fc-115">The sink writer supports the following combinations:</span></span>

-   <span data-ttu-id="b98fc-116">Unkomprimierte Eingabe mit komprimierter Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="b98fc-116">Uncompressed input with compressed output.</span></span> <span data-ttu-id="b98fc-117">Dies ist der typische Fall und wird für Codierungs- oder Transcodierungsszenarien verwendet.</span><span class="sxs-lookup"><span data-stu-id="b98fc-117">This is the typical case, and is used for encoding or transcoding scenarios.</span></span> <span data-ttu-id="b98fc-118">Ein Microsoft Media Foundation encoder muss verfügbar sein, der den Eingabetyp akzeptiert und in den Ausgabetyp codiert.</span><span class="sxs-lookup"><span data-stu-id="b98fc-118">A Microsoft Media Foundation encoder must be available that accepts the input type and encodes to the output type.</span></span>
-   <span data-ttu-id="b98fc-119">Komprimierte Eingabe mit identischer Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="b98fc-119">Compressed input with identical output.</span></span> <span data-ttu-id="b98fc-120">Verwenden Sie diese Kombination, um eine Datei ohne Transcodierung neu zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b98fc-120">Use this combination to remux a file without transcoding.</span></span>
-   <span data-ttu-id="b98fc-121">Unkomprimierte Eingabe mit identischer Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="b98fc-121">Uncompressed input with identical output.</span></span> <span data-ttu-id="b98fc-122">Verwenden Sie diese Kombination, um unkomprimierte Audio- oder Videodaten in einen Dateicontainer zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="b98fc-122">Use this combination to write uncompressed audio or video to a file container.</span></span>

<span data-ttu-id="b98fc-123">Der Senkenwriter unterstützt keine Videoänderung, Bildfrequenzkonvertierung oder Audio-Resampling, es sei denn, diese Funktionen werden vom Encoder bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="b98fc-123">The sink writer does not support video resizing, frame-rate conversion, or audio resampling, unless these functions are provided by the encoder.</span></span> <span data-ttu-id="b98fc-124">Andernfalls kann die Anwendung [Digital Signal Processors](windowsmediadigitalsignalprocessors.md) verwenden, um die Eingabedaten zu konvertieren, bevor die Daten an gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="b98fc-124">Otherwise, the application can use [Digital Signal Processors](windowsmediadigitalsignalprocessors.md) to convert the input data, before sending the data to the</span></span>

## <a name="creating-the-sink-writer"></a><span data-ttu-id="b98fc-125">Erstellen des Senkenwriters</span><span class="sxs-lookup"><span data-stu-id="b98fc-125">Creating the Sink Writer</span></span>

<span data-ttu-id="b98fc-126">Es gibt zwei Funktionen, die den Senkenwriter erstellen:</span><span class="sxs-lookup"><span data-stu-id="b98fc-126">There are two functions that create the sink writer:</span></span>

-   <span data-ttu-id="b98fc-127">[**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) verwendet die URL einer Ausgabedatei oder einen Zeiger auf einen Bytestream.</span><span class="sxs-lookup"><span data-stu-id="b98fc-127">[**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) takes the URL of an output file or a pointer to a byte stream.</span></span> <span data-ttu-id="b98fc-128">Diese Funktion erstellt die Mediensenke intern.</span><span class="sxs-lookup"><span data-stu-id="b98fc-128">This function creates the media sink internally.</span></span>
-   <span data-ttu-id="b98fc-129">[**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink) verwendet einen Zeiger auf eine Mediensenke, die bereits von der Anwendung erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="b98fc-129">[**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink) takes a pointer to a media sink that has already been created by the application.</span></span>

<span data-ttu-id="b98fc-130">Wenn Sie eine der integrierten Mediensenken verwenden, ist die [**MFCreateSinkWriterFromURL-Funktion**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) vorzuziehen, da der Aufrufer die Mediensenke nicht konfigurieren muss.</span><span class="sxs-lookup"><span data-stu-id="b98fc-130">If you are using one of the built-in media sinks, the [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) function is preferable, because the caller does not need to configure the media sink.</span></span>

<span data-ttu-id="b98fc-131">Die [**MFCreateSinkWriterFromURL-Methode**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) bietet mehrere Optionen zum Angeben des Dateicontainertyps.</span><span class="sxs-lookup"><span data-stu-id="b98fc-131">The [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) method provides several options for specifying the type of file container.</span></span> <span data-ttu-id="b98fc-132">Im einfachsten Fall verwendet die Funktion die Dateinamenerweiterung in der URL, um den Dateicontainer auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="b98fc-132">In the simplest case, the function uses the file name extension in the URL to select the file container.</span></span> <span data-ttu-id="b98fc-133">Weitere Informationen finden Sie auf der Funktionsreferenzseite.</span><span class="sxs-lookup"><span data-stu-id="b98fc-133">For details, refer to the function reference page.</span></span>

<span data-ttu-id="b98fc-134">Der folgende Code gibt beispielsweise den Dateinamen "output.wmv" für die URL an.</span><span class="sxs-lookup"><span data-stu-id="b98fc-134">For example, the following code specifies the file name "output.wmv" for the URL.</span></span> <span data-ttu-id="b98fc-135">Basierend auf der Dateinamenerweiterung lädt der Senkenwriter die [ASF-Mediensenke,](asf-media-sinks.md) um eine ASF-Datei (Advanced Systems Format) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b98fc-135">Based on the file name extension, the sink writer will load the [ASF Media Sink](asf-media-sinks.md) to create an Advanced Systems Format (ASF) file.</span></span>


```C++
    HRESULT hr = MFCreateSinkWriterFromURL(L"output.wmv", NULL, NULL, &pSinkWriter);
```



<span data-ttu-id="b98fc-136">Im Fall von [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)wird der Dateityp durch die Mediensenke bestimmt.</span><span class="sxs-lookup"><span data-stu-id="b98fc-136">In the case of [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink), the file type is determined by the media sink.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b98fc-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b98fc-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b98fc-138">Sink Writer</span><span class="sxs-lookup"><span data-stu-id="b98fc-138">Sink Writer</span></span>](sink-writer.md)
</dt> </dl>

 

 



