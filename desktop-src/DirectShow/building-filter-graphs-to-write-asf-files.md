---
description: Erstellen von Filter Diagrammen zum Schreiben von ASF-Dateien
ms.assetid: c4885152-d7d2-4749-a79a-e0effd38837d
title: Erstellen von Filter Diagrammen zum Schreiben von ASF-Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0581672f9fd3e4bfa5e2c678c3bd3c0d3ea22fa0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482270"
---
# <a name="building-filter-graphs-to-write-asf-files"></a><span data-ttu-id="7083b-103">Erstellen von Filter Diagrammen zum Schreiben von ASF-Dateien</span><span class="sxs-lookup"><span data-stu-id="7083b-103">Building Filter Graphs to Write ASF Files</span></span>

<span data-ttu-id="7083b-104">Beim Erstellen von Windows Media – basierten Inhalten verwenden Anwendungen in der Regel eines der folgenden Szenarien:</span><span class="sxs-lookup"><span data-stu-id="7083b-104">When creating Windows Media–based content, applications typically use one of the following scenarios:</span></span>

-   <span data-ttu-id="7083b-105">Umwandeln oder transcodieren von Inhalten aus einem anderen Format in das Windows Media-Format.</span><span class="sxs-lookup"><span data-stu-id="7083b-105">Converting or transcoding content from some other format into Windows Media Format.</span></span>
-   <span data-ttu-id="7083b-106">Einfügen von Inhalten, bei denen es sich nicht um Windows Media-basierte (Native Streamformate) handelt, in ASF-Dateien</span><span class="sxs-lookup"><span data-stu-id="7083b-106">Inserting content that is not Windows Media-based (native stream formats) into ASF files.</span></span>
-   <span data-ttu-id="7083b-107">Die Erfassung von Livedaten und die direkte Codierung im Windows Media-Format.</span><span class="sxs-lookup"><span data-stu-id="7083b-107">Capturing live data and encoding it immediately into Windows Media Format.</span></span>

<span data-ttu-id="7083b-108">Transcodierung von ASF-Dateien</span><span class="sxs-lookup"><span data-stu-id="7083b-108">Transcoding ASF Files</span></span>

<span data-ttu-id="7083b-109">Sie können ein Datei-transcodierungsfilterdiagramm mit dem [WM-ASF-Writer](wm-asf-writer-filter.md) auf verschiedene Weise erstellen.</span><span class="sxs-lookup"><span data-stu-id="7083b-109">You can build a file-transcoding filter graph using the [WM ASF Writer](wm-asf-writer-filter.md) in various ways.</span></span> <span data-ttu-id="7083b-110">Die einfachste Möglichkeit besteht darin, den WM-ASF-Writer dem Filter Diagramm hinzuzufügen und dann mit der igraphbuilder:: RenderFile-Methode automatisch das Diagramm zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7083b-110">The easiest way is to add the WM ASF Writer to the filter graph and then use the IGraphBuilder::RenderFile method to build the graph automatically.</span></span>

<span data-ttu-id="7083b-111">Eine alternative Möglichkeit besteht darin, jeden Filter manuell dem Diagramm hinzuzufügen und die Pins zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="7083b-111">An alternative way is to add each filter manually to the graph and connect the pins.</span></span> <span data-ttu-id="7083b-112">Nachdem Sie den WM-ASF-Writer hinzugefügt haben, konfigurieren Sie ihn mithilfe der iconfigasfwriter-Methoden, wenn das Standardprofil nicht geeignet ist, und verbinden Sie die WM-ASF-Eingabe Pins mit den entsprechenden Ausgabe Pins in den upstreamfiltern.</span><span class="sxs-lookup"><span data-stu-id="7083b-112">After adding the WM ASF Writer, configure it by using the IConfigAsfWriter methods if the default profile is not suitable, and connect the WM ASF Writer input pins to the corresponding output pins on the upstream filters.</span></span>

<span data-ttu-id="7083b-113">Die folgende Abbildung zeigt die typischen Konfigurationen von "WM-ASF-Writer-Transcodierungs Filter"</span><span class="sxs-lookup"><span data-stu-id="7083b-113">The following illustration shows typical WM ASF Writer transcoding filter graph configurations.</span></span>

![Transcodierungs Filter Diagramm](images/asf-transcode.png)

<span data-ttu-id="7083b-115">Einfügen von nativen streamformaten in ASF-Dateien</span><span class="sxs-lookup"><span data-stu-id="7083b-115">Inserting Native Stream Formats Into ASF Files</span></span>

<span data-ttu-id="7083b-116">Standardmäßig erwartet der WM-ASF-Writer-Filter unkomprimierte Audiodaten und Videostreams auf den Eingabe Pins und verwendet die Windows Media Audio und Windows Media Video Codecs, um die Streams zu komprimieren.</span><span class="sxs-lookup"><span data-stu-id="7083b-116">By default, the WM ASF Writer filter expects uncompressed audio and video streams on its input pins, and uses the Windows Media Audio and Windows Media Video codecs to compress the streams.</span></span> <span data-ttu-id="7083b-117">Allerdings kann der ASF-Datei Container für beliebige Datentypen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7083b-117">However, the ASF file container can be used for any type of data.</span></span> <span data-ttu-id="7083b-118">Durch das Platzieren digitaler Mediendaten in einem ASF-Datei Container können Sie Features hinzufügen, die von ASF bereitgestellt werden, wie z. b. Metadaten und Digital Rights Management (DRM), ohne dass Sie Ihre Inhalte transcodieren müssen.</span><span class="sxs-lookup"><span data-stu-id="7083b-118">By placing digital media data into an ASF file container, you can add features provided by ASF, such as metadata and digital rights management (DRM), without having to transcode your content.</span></span>

<span data-ttu-id="7083b-119">Zum Erstellen einer ASF-Datei, die Inhalte enthält, die nicht auf Windows Media – basieren, muss die Anwendung den Datenstrom im Filter Diagramm Upstream des WM-ASF-Writers komprimieren und den Komprimierungs Mechanismus des WM-ASF-Writers durch Aufrufen von [**IConfigAsfWriter2:: SetParam**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-setparam) wie folgt umgehen:</span><span class="sxs-lookup"><span data-stu-id="7083b-119">To create an ASF file that contains content that is not Windows Media–based, the application must compress the stream in the filter graph upstream of the WM ASF Writer and bypass the WM ASF Writer's compression mechanism by calling [**IConfigAsfWriter2::SetParam**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-setparam) as follows:</span></span>


```C++
pConfigAsfWriter2->SetParam(AM_CONFIGASFWRITER_PARAM_DONTCOMPRESS,TRUE,0)
```



<span data-ttu-id="7083b-120">Konfigurieren Sie dann den Filter mit dem gewünschten Profil.</span><span class="sxs-lookup"><span data-stu-id="7083b-120">Then configure the filter with the desired profile.</span></span> <span data-ttu-id="7083b-121">Es ist von entscheidender Bedeutung, dass der Medientyp des Eingabestreams genau mit dem Format im Profil übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="7083b-121">It is essential that the media type of the input stream exactly matches the format in the profile.</span></span> <span data-ttu-id="7083b-122">In einigen Fällen kann es erforderlich sein, das Format des Eingabestreams zu untersuchen und ein benutzerdefiniertes Profil zu erstellen, um es abzugleichen.</span><span class="sxs-lookup"><span data-stu-id="7083b-122">In some cases, it may be necessary to examine the input stream's format, and create a custom profile to match it.</span></span>

<span data-ttu-id="7083b-123">Wenn Sie den WM-ASF-Writer mit dem upstreamfilter verbinden, verwenden Sie die igraphbuilder:: connectdirect-Methode.</span><span class="sxs-lookup"><span data-stu-id="7083b-123">When you connect the WM ASF Writer to the upstream filter, use the IGraphBuilder::ConnectDirect method.</span></span> <span data-ttu-id="7083b-124">Verwenden Sie keine "Intelligent Connect"-Methoden wie z. b. igraphbuilder:: Connect oder igraphbuilder:: RenderFile, um den Filter zu verbinden, da dadurch der Modus "Umgehung der Umgehungs Komprimierung" deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="7083b-124">Do not use any "intelligent connect" methods such as IGraphBuilder::Connect or IGraphBuilder::RenderFile to connect the filter because this will disable the filter's "bypass compression" mode.</span></span>

<span data-ttu-id="7083b-125">Direkte Erfassung von einem Gerät in einer ASF-Datei</span><span class="sxs-lookup"><span data-stu-id="7083b-125">Capturing Directly from a Device to an ASF File</span></span>

<span data-ttu-id="7083b-126">Wenn Sie Audiodaten oder Videos direkt in einer ASF-Datei erfassen, sieht das Filter Diagramm in etwa wie folgt aus, je nach Art des verwendeten Erfassungs Geräts.</span><span class="sxs-lookup"><span data-stu-id="7083b-126">When capturing audio or video directly to an ASF file, the filter graph will look similar to the following, depending on the type of capture device being used.</span></span>

![Windows Media Video Capture Graph](images/asf-webcam.png)

<span data-ttu-id="7083b-128">Weitere Informationen zum Erstellen von Video-und audioerfassungs Diagrammen finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="7083b-128">For more information about creating video and audio capture graphs, see the following topics:</span></span>

-   [<span data-ttu-id="7083b-129">Audioerfassung</span><span class="sxs-lookup"><span data-stu-id="7083b-129">Audio Capture</span></span>](audio-capture.md)
-   [<span data-ttu-id="7083b-130">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="7083b-130">Video Capture</span></span>](video-capture.md)

<span data-ttu-id="7083b-131">Der WM-ASF-Writer wird nicht ausgeführt, es sei denn, alle seine Pins sind verbunden.</span><span class="sxs-lookup"><span data-stu-id="7083b-131">The WM ASF Writer will not run unless all of its pins are connected.</span></span> <span data-ttu-id="7083b-132">Wenn Sie den WM-ASF-Writer mit dem Standardsystem Profil (nicht empfohlen) oder einem beliebigen Profil mit Audio-und Videostreams konfigurieren, wird eine Eingabe-PIN für jeden Stream erstellt, und jeder dieser Pins muss verbunden sein.</span><span class="sxs-lookup"><span data-stu-id="7083b-132">If you configure the WM ASF Writer with the default system profile (not recommended), or any profile with audio and video streams, then it will create an input pin for each stream and each of those pins must be connected.</span></span> <span data-ttu-id="7083b-133">Wenn Sie z. b. keine Audiodaten erfassen möchten, stellen Sie sicher, dass Sie den Filter mit einem nur-Video-Profil konfigurieren, sodass keine audiopin erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="7083b-133">If you do not intend to capture audio, for example, then be sure to configure the filter with a video-only profile so that no audio pin is created.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7083b-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7083b-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7083b-135">Erstellen von ASF-Dateien in DirectShow</span><span class="sxs-lookup"><span data-stu-id="7083b-135">Creating ASF Files in DirectShow</span></span>](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 



