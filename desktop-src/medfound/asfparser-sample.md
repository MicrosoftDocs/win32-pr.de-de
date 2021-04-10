---
description: Asfparser-Beispiel
ms.assetid: 6be1e12f-7d4a-4564-88ae-14fd71fd2cf9
title: Asfparser-Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c159b481e22d77b0bee9adccbbb74073398c12b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214344"
---
# <a name="asfparser-sample"></a><span data-ttu-id="77015-103">Asfparser-Beispiel</span><span class="sxs-lookup"><span data-stu-id="77015-103">ASFParser Sample</span></span>

<span data-ttu-id="77015-104">Zeigt, wie Sie Daten aus einer ASF-Datei (Advanced Systems Format) mithilfe der-ASF-Komponenten auf niedriger Ebene in Media Foundation analysieren.</span><span class="sxs-lookup"><span data-stu-id="77015-104">Shows how to parse data from an Advanced Systems Format (ASF) file by using the low-level ASF components in Media Foundation.</span></span> <span data-ttu-id="77015-105">Das Beispiel veranschaulicht die folgenden Aufgaben:</span><span class="sxs-lookup"><span data-stu-id="77015-105">The sample demonstrates the following tasks:</span></span>

-   <span data-ttu-id="77015-106">Auflisten der Audiodaten und Videostreams in einer ASF-Datei.</span><span class="sxs-lookup"><span data-stu-id="77015-106">Enumerating the audio and video streams in an ASF file.</span></span>
-   <span data-ttu-id="77015-107">Auswählen eines Audiodaten-oder Videodaten Stroms für die Analyse.</span><span class="sxs-lookup"><span data-stu-id="77015-107">Selecting an audio or a video stream for parsing.</span></span>
-   <span data-ttu-id="77015-108">Es wird versucht, ein Paket zu einer gewünschten Wiedergabezeit zu suchen.</span><span class="sxs-lookup"><span data-stu-id="77015-108">Seeking to a packet at a desired playback time.</span></span>
-   <span data-ttu-id="77015-109">Komprimierte Beispiele für den ausgewählten Stream werden erzeugt.</span><span class="sxs-lookup"><span data-stu-id="77015-109">Generating compressed samples for the selected stream.</span></span>
-   <span data-ttu-id="77015-110">Decodieren von Audio-und Videobeispielen.</span><span class="sxs-lookup"><span data-stu-id="77015-110">Decoding audio and video samples.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="77015-111">Gezeigte APIs</span><span class="sxs-lookup"><span data-stu-id="77015-111">APIs Demonstrated</span></span>

<span data-ttu-id="77015-112">In diesem Beispiel werden die folgenden Microsoft Media Foundation Schnittstellen veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="77015-112">This sample demonstrates the following Microsoft Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="77015-113">**Imfasf ContentInfo**</span><span class="sxs-lookup"><span data-stu-id="77015-113">**IMFASFContentInfo**</span></span>](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo)
-   [<span data-ttu-id="77015-114">**Imfasfindexer**</span><span class="sxs-lookup"><span data-stu-id="77015-114">**IMFASFIndexer**</span></span>](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer)
-   [<span data-ttu-id="77015-115">**Imfasfäsplitter**</span><span class="sxs-lookup"><span data-stu-id="77015-115">**IMFASFSplitter**</span></span>](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter)

## <a name="usage"></a><span data-ttu-id="77015-116">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="77015-116">Usage</span></span>

1.  <span data-ttu-id="77015-117">Um eine ASF-Datei zu öffnen, klicken Sie auf die Schaltfläche **Mediendatei öffnen...** .</span><span class="sxs-lookup"><span data-stu-id="77015-117">To open an ASF file, click the **Open Media File...** button.</span></span>
2.  <span data-ttu-id="77015-118">Wählen Sie eine ASF-Datei und klicken Sie auf **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="77015-118">Select an ASF file and click **Open**.</span></span> <span data-ttu-id="77015-119">Informationen zur Datei werden im **Informations** Bereich angezeigt.</span><span class="sxs-lookup"><span data-stu-id="77015-119">Information about the file is shown on the **Information** pane.</span></span>
3.  <span data-ttu-id="77015-120">Wählen Sie unter **parserkonfiguration** einen zu testenden Stream aus.</span><span class="sxs-lookup"><span data-stu-id="77015-120">Under **Parser Configuration**, select a stream to parse.</span></span>
4.  <span data-ttu-id="77015-121">Um Beispiele in umgekehrter Reihenfolge zu generieren, wählen Sie **umkehren**.</span><span class="sxs-lookup"><span data-stu-id="77015-121">To generate samples in reverse, select **Reverse**.</span></span>
5.  <span data-ttu-id="77015-122">Um den Startpunkt anzugeben, ziehen Sie den Schieberegler an den gewünschten Speicherort.</span><span class="sxs-lookup"><span data-stu-id="77015-122">To specify the start point, drag the slider to the desired location.</span></span>
6.  <span data-ttu-id="77015-123">Um mit der Verarbeitung zu beginnen, klicken Sie auf die Schaltfläche **Beispiele generieren** .</span><span class="sxs-lookup"><span data-stu-id="77015-123">To begin parsing, click the **Generate Samples** button.</span></span> <span data-ttu-id="77015-124">Informationen zu den Beispielen werden im **Informations** Bereich angezeigt.</span><span class="sxs-lookup"><span data-stu-id="77015-124">Information about the samples is shown on the **Information** pane.</span></span>
7.  <span data-ttu-id="77015-125">Um die Beispiele für den Audiostream zu testen, klicken Sie auf die Schaltfläche " **Testdatei** ".</span><span class="sxs-lookup"><span data-stu-id="77015-125">To test the samples for the audio stream, click the **Test Audio** button.</span></span>
8.  <span data-ttu-id="77015-126">Um die Beispiele für den Videostream zu testen, klicken Sie auf die Schaltfläche **Bitmap anzeigen** .</span><span class="sxs-lookup"><span data-stu-id="77015-126">To test the samples for the video stream, click the **Show Bitmap** button.</span></span>

## <a name="requirements"></a><span data-ttu-id="77015-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="77015-127">Requirements</span></span>



| <span data-ttu-id="77015-128">Produkt</span><span class="sxs-lookup"><span data-stu-id="77015-128">Product</span></span>                                                        | <span data-ttu-id="77015-129">Version</span><span class="sxs-lookup"><span data-stu-id="77015-129">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="77015-130">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="77015-130">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="77015-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="77015-131">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="77015-132">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="77015-132">Downloading the Sample</span></span>

<span data-ttu-id="77015-133">Dieses Beispiel ist im [GitHub-Repository für klassische Windows-Beispiele](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/asfparser)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="77015-133">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/asfparser).</span></span>

## <a name="related-topics"></a><span data-ttu-id="77015-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="77015-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77015-135">Media Foundation-SDK-Beispiele</span><span class="sxs-lookup"><span data-stu-id="77015-135">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="77015-136">Unterstützung von ASF in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="77015-136">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="77015-137">Tutorial: Lesen einer ASF-Datei</span><span class="sxs-lookup"><span data-stu-id="77015-137">Tutorial: Reading an ASF File</span></span>](tutorial--reading-an-asf-file.md)
</dt> <dt>

[<span data-ttu-id="77015-138">Wmcontainer-ASF-Komponenten</span><span class="sxs-lookup"><span data-stu-id="77015-138">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> </dl>

 

 



