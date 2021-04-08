---
title: Einfügen von nativen streamformaten in ASF-Dateien (qasf)
description: Einfügen von nativen streamformaten in ASF-Dateien (qasf)
ms.assetid: ec7a69f3-0d4c-43dd-8d4b-fe066329a98f
keywords:
- Windows Media-Format-SDK, Native Streamformate (qasf)
- Windows Media-Format-SDK, Einfügen von nativen streamformaten in ASF-Dateien (qasf)
- Windows Media-Format-SDK, DirectShow
- Advanced Systems Format (ASF), Einfügen von nativen streamformaten (qasf)
- ASF (Advanced Systems Format), Einfügen von nativen streamformaten (qasf)
- Advanced Systems Format (ASF), Native Streamformate (qasf)
- ASF (Advanced Systems Format), Native Stream-Formate (qasf)
- Advanced Systems Format (ASF), DirectShow
- ASF (Advanced Systems Format), DirectShow
- DirectShow, Native Streamformate (qasf)
- DirectShow, Einfügen von nativen streamformaten in ASF-Dateien (qasf)
- Windows Media-Format-SDK, qasf
- Advanced Systems Format (ASF), qasf
- ASF (Advanced Systems Format), qasf
- DirectShow, qasf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af4736c450b3620a05fe01dcc1808adc297ebbd1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856692"
---
# <a name="inserting-native-stream-formats-into-asf-files-qasf"></a><span data-ttu-id="9917a-118">Einfügen von nativen streamformaten in ASF-Dateien (qasf)</span><span class="sxs-lookup"><span data-stu-id="9917a-118">Inserting Native Stream Formats Into ASF Files (QASF)</span></span>

<span data-ttu-id="9917a-119">Standardmäßig erwartet der [WM-ASF-Writer](wm-asf-writer-filter.md) unkomprimierte Audiodaten und Videostreams auf den Eingabe Pins und verwendet das SDK für den Windows Media-Format, um auf die Windows Media Audio und Windows Media Video Codecs zuzugreifen, die die Streams komprimieren.</span><span class="sxs-lookup"><span data-stu-id="9917a-119">By default, the [WM ASF Writer](wm-asf-writer-filter.md) expects uncompressed audio and video streams on its input pins, and uses the Windows Media Format SDK to access the Windows Media Audio and Windows Media Video codecs, which compress the streams.</span></span> <span data-ttu-id="9917a-120">Der ASF-Datei Container kann jedoch für beliebige Datentypen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9917a-120">But the ASF file container can be used for any type of data.</span></span> <span data-ttu-id="9917a-121">Durch das Platzieren digitaler Mediendaten in einem ASF-Datei Container können Sie Features hinzufügen, die von ASF bereitgestellt werden, wie z. b. Metadaten und Digital Rights Management (DRM), ohne dass Sie Ihre Inhalte transcodieren müssen.</span><span class="sxs-lookup"><span data-stu-id="9917a-121">By placing digital media data into an ASF file container, you can add features provided by ASF, such as metadata and digital rights management (DRM), without having to transcode your content.</span></span>

<span data-ttu-id="9917a-122">Zum Erstellen einer ASF-Datei, die Inhalte enthält, die nicht auf Windows Media – basieren, muss die Anwendung den Datenstrom im Filter Diagramm Upstream des WM-ASF-Writers komprimieren und den Komprimierungs Mechanismus des WM-ASF-Writers durch Aufrufen von [**IConfigAsfWriter2:: SetParam**](iconfigasfwriter2-setparam.md) wie folgt umgehen:</span><span class="sxs-lookup"><span data-stu-id="9917a-122">To create an ASF file that contains content that is not Windows Media–based, the application must compress the stream in the filter graph upstream of the WM ASF Writer and bypass the WM ASF Writer's compression mechanism by calling [**IConfigAsfWriter2::SetParam**](iconfigasfwriter2-setparam.md) as follows:</span></span>


```C++
pConfigAsfWriter2->SetParam(AM_CONFIGASFWRITER_PARAM_DONTCOMPRESS,TRUE,0)

```



<span data-ttu-id="9917a-123">Konfigurieren Sie dann den Filter mit dem gewünschten Profil.</span><span class="sxs-lookup"><span data-stu-id="9917a-123">Then configure the filter with the desired profile.</span></span> <span data-ttu-id="9917a-124">Es ist von entscheidender Bedeutung, dass der Medientyp des Eingabestreams genau mit dem Format im Profil übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="9917a-124">It is essential that the media type of the input stream exactly matches the format in the profile.</span></span> <span data-ttu-id="9917a-125">In einigen Fällen kann es erforderlich sein, das Format des Eingabestreams zu untersuchen und ein benutzerdefiniertes Profil zu erstellen, um es abzugleichen.</span><span class="sxs-lookup"><span data-stu-id="9917a-125">In some cases, it may be necessary to examine the input stream's format, and create a custom profile to match it.</span></span> <span data-ttu-id="9917a-126">Weitere Informationen finden Sie [unter So erstellen Sie ASF-Dateien mithilfe von Drittanbieter-Codecs](to-create-asf-files-using-third-party-codecs.md).</span><span class="sxs-lookup"><span data-stu-id="9917a-126">For more information, see [To Create ASF Files Using Third-Party Codecs](to-create-asf-files-using-third-party-codecs.md).</span></span>

<span data-ttu-id="9917a-127">Wenn Sie den WM-ASF-Writer mit dem upstreamfilter verbinden, verwenden Sie die **igraphbuilder:: connectdirect** -Methode.</span><span class="sxs-lookup"><span data-stu-id="9917a-127">When you connect the WM ASF Writer to the upstream filter, use the **IGraphBuilder::ConnectDirect** method.</span></span> <span data-ttu-id="9917a-128">Verwenden Sie keine "Intelligent Connect"-Methoden wie z. b. **igraphbuilder:: Connect** oder **igraphbuilder:: RenderFile** , um den Filter zu verbinden, da dadurch der Modus "Umgehung der Umgehungs Komprimierung" deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="9917a-128">Do not use any "intelligent connect" methods such as **IGraphBuilder::Connect** or **IGraphBuilder::RenderFile** to connect the filter because this will disable the filter's "bypass compression" mode.</span></span>

 

 




