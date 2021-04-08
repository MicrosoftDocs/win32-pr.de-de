---
title: Erstellen von ASF-Dateien in DirectShow (Windows Media-Format 11 SDK)
description: Erstellen von ASF-Dateien in DirectShow
ms.assetid: 8b7af340-934d-43a9-88e9-7bbb2d3a38e0
keywords:
- Windows Media-Format-SDK, Erstellen von ASF-Dateien in DirectShow
- Windows Media-Format-SDK, DirectShow
- Advanced Systems Format (ASF), DirectShow
- ASF (Advanced Systems Format), DirectShow
- Advanced Systems Format (ASF), erstellen in DirectShow
- ASF (Advanced Systems Format), erstellen in DirectShow
- DirectShow, Erstellen von ASF-Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbe4a6a37a508e5d7c713ae4cf38d771d075cefa
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102663"
---
# <a name="creating-asf-files-in-directshow-windows-media-format-11-sdk"></a><span data-ttu-id="eac21-110">Erstellen von ASF-Dateien in DirectShow (Windows Media-Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="eac21-110">Creating ASF Files in DirectShow (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="eac21-111">Mithilfe von DirectShow können Sie ASF-Dateien direkt aus Erfassungs Quellen, wie z. b. DV-Camcordern, erstellen oder andere Dateien in das Windows Media-Format transcodieren.</span><span class="sxs-lookup"><span data-stu-id="eac21-111">You can use DirectShow to create ASF files directly from capture sources such as DV camcorders or to transcode other files into Windows Media Format.</span></span> <span data-ttu-id="eac21-112">In beiden Szenarien erstellen Anwendungen Filter Diagramme, die den [WM-ASF-Writer](wm-asf-writer-filter.md) -Filter als Renderer enthalten.</span><span class="sxs-lookup"><span data-stu-id="eac21-112">In either scenario, applications create filter graphs that include the [WM ASF Writer](wm-asf-writer-filter.md) filter as the renderer.</span></span>

<span data-ttu-id="eac21-113">Der WM-ASF-Writer stellt einen partiellen Wrapper für das Windows Media-Format-SDK bereit.</span><span class="sxs-lookup"><span data-stu-id="eac21-113">The WM ASF Writer provides a partial wrapper for the Windows Media Format SDK.</span></span> <span data-ttu-id="eac21-114">Anwendungen können die [**iconfigasfwriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) -Schnittstelle des Filters verwenden, um ein Systemprofil (Version 4, 7 oder 8) zu übergeben, oder das Windows Media-Format-SDK direkt verwenden, um ein benutzerdefiniertes Profil zu erstellen, das an den Filter übergeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="eac21-114">Applications can use the [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) interface of the filter to pass in a system profile (versions 4, 7, or 8), or use the Windows Media Format SDK directly to create a custom profile to pass to the filter.</span></span> <span data-ttu-id="eac21-115">Zum Hinzufügen von Metadaten und anderen Header Informationen verwendet die Anwendung die [**iwmheaderinfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) -Schnittstelle, die aus dem Filter abgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="eac21-115">To add metadata and other header information, the application uses the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) interface, which can be obtained from the filter.</span></span> <span data-ttu-id="eac21-116">Nachdem das Profil und die Metadaten konfiguriert wurden, kann die Anwendung einfach das Filter Diagramm ausführen.</span><span class="sxs-lookup"><span data-stu-id="eac21-116">After the profile and metadata have been configured, the application can simply run the filter graph.</span></span> <span data-ttu-id="eac21-117">Intern verwendet der Filter das SDK für den Windows Media-Format, um die Datei zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="eac21-117">Internally, the filter uses the Windows Media Format SDK to write the file.</span></span> <span data-ttu-id="eac21-118">Der Filter behandelt alle Details der audiovideosynchronisierung, die andernfalls für die Anwendung verantwortlich sind.</span><span class="sxs-lookup"><span data-stu-id="eac21-118">The filter handles all the audio-video synchronization details, which would otherwise be the responsibility of the application.</span></span>

<span data-ttu-id="eac21-119">Dieser Prozess wird in den folgenden Abschnitten ausführlicher erläutert.</span><span class="sxs-lookup"><span data-stu-id="eac21-119">This process is explained in more detail in the following sections.</span></span>



| <span data-ttu-id="eac21-120">`Section`</span><span class="sxs-lookup"><span data-stu-id="eac21-120">Section</span></span>                                                                                                           | <span data-ttu-id="eac21-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eac21-121">Description</span></span>                                                                            |
|-------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="eac21-122">Konfigurieren von WM ASF Writer (qasf)</span><span class="sxs-lookup"><span data-stu-id="eac21-122">Configuring the WM ASF Writer (QASF)</span></span>](configuring-the-wm-asf-writer--qasf.md)                                   | <span data-ttu-id="eac21-123">Beschreibt, wie der WM-ASF-Writer-Filter konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="eac21-123">Describes how to configure the WM ASF Writer filter.</span></span>                                   |
| [<span data-ttu-id="eac21-124">Erstellen von Filter Diagrammen zum Schreiben von ASF-Dateien (qasf)</span><span class="sxs-lookup"><span data-stu-id="eac21-124">Building Filter Graphs to Write ASF Files (QASF)</span></span>](building-filter-graphs-to-write-asf-files--qasf.md)           | <span data-ttu-id="eac21-125">Hier wird beschrieben, wie Datei-und Erfassungs Diagramme erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="eac21-125">Describes how to create file-transcoding and capture graphs.</span></span>                           |
| [<span data-ttu-id="eac21-126">Konfigurieren von Profilen und anderen Dateieigenschaften (qasf)</span><span class="sxs-lookup"><span data-stu-id="eac21-126">Configuring Profiles and Other File Properties (QASF)</span></span>](configuring-profiles-and-other-file-properties--qasf.md) | <span data-ttu-id="eac21-127">Hier wird beschrieben, wie verschiedene Aufgaben zur Konfiguration von ASF-Dateien mit dem WM-ASF-Writer ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="eac21-127">Describes how to perform various ASF file-configuration tasks using the WM ASF Writer.</span></span> |



 

 

 
