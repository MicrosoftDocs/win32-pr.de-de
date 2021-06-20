---
title: Erstellen von ASF-Dateien in DirectShow (Windows Media Format 11 SDK)
description: Erfahren Sie mehr über das Erstellen von ASF-Dateien in DirectShow mit dem Windows Media Format 11 SDK. ASF ist ein Containerformat, das beliebige Datentypen enthalten kann.
ms.assetid: 8b7af340-934d-43a9-88e9-7bbb2d3a38e0
keywords:
- Windows Media Format SDK, Erstellen von ASF-Dateien in DirectShow
- Windows Media Format SDK, DirectShow
- Advanced Systems Format (ASF), DirectShow
- ASF (Advanced Systems Format), DirectShow
- Advanced Systems Format (ASF), erstellen in DirectShow
- ASF (Advanced Systems Format), erstellen in DirectShow
- DirectShow,Erstellen von ASF-Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e06b6deb6dc9f07115f8143309d32dcf4a58a0f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406183"
---
# <a name="creating-asf-files-in-directshow-windows-media-format-11-sdk"></a><span data-ttu-id="a45e6-111">Erstellen von ASF-Dateien in DirectShow (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="a45e6-111">Creating ASF Files in DirectShow (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="a45e6-112">Sie können DirectShow verwenden, um ASF-Dateien direkt aus Erfassungsquellen wie DV-Datenträgern zu erstellen oder andere Dateien in das Windows-Medienformat zu transcodieren.</span><span class="sxs-lookup"><span data-stu-id="a45e6-112">You can use DirectShow to create ASF files directly from capture sources such as DV camcorders or to transcode other files into Windows Media Format.</span></span> <span data-ttu-id="a45e6-113">In beiden Szenarien erstellen Anwendungen Filterdiagramme, die den [WM ASF Writer-Filter](wm-asf-writer-filter.md) als Renderer enthalten.</span><span class="sxs-lookup"><span data-stu-id="a45e6-113">In either scenario, applications create filter graphs that include the [WM ASF Writer](wm-asf-writer-filter.md) filter as the renderer.</span></span>

<span data-ttu-id="a45e6-114">Wm ASF Writer stellt einen Teilwrapper für das Windows Media Format SDK bereit.</span><span class="sxs-lookup"><span data-stu-id="a45e6-114">The WM ASF Writer provides a partial wrapper for the Windows Media Format SDK.</span></span> <span data-ttu-id="a45e6-115">Anwendungen können die [**IConfigAsfWriter-Schnittstelle**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) des Filters verwenden, um ein Systemprofil (Versionen 4, 7 oder 8) zu übergeben, oder das Windows Media Format SDK direkt verwenden, um ein benutzerdefiniertes Profil zu erstellen, das an den Filter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="a45e6-115">Applications can use the [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) interface of the filter to pass in a system profile (versions 4, 7, or 8), or use the Windows Media Format SDK directly to create a custom profile to pass to the filter.</span></span> <span data-ttu-id="a45e6-116">Um Metadaten und andere Headerinformationen hinzuzufügen, verwendet die Anwendung die [**IWMHeaderInfo-Schnittstelle,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) die aus dem Filter abgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="a45e6-116">To add metadata and other header information, the application uses the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) interface, which can be obtained from the filter.</span></span> <span data-ttu-id="a45e6-117">Nachdem das Profil und die Metadaten konfiguriert wurden, kann die Anwendung einfach das Filterdiagramm ausführen.</span><span class="sxs-lookup"><span data-stu-id="a45e6-117">After the profile and metadata have been configured, the application can simply run the filter graph.</span></span> <span data-ttu-id="a45e6-118">Intern verwendet der Filter das Windows Media Format SDK, um die Datei zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="a45e6-118">Internally, the filter uses the Windows Media Format SDK to write the file.</span></span> <span data-ttu-id="a45e6-119">Der Filter verarbeitet alle Details zur Synchronisierung von Audiovideos, die andernfalls in der Verantwortung der Anwendung stehen würden.</span><span class="sxs-lookup"><span data-stu-id="a45e6-119">The filter handles all the audio-video synchronization details, which would otherwise be the responsibility of the application.</span></span>

<span data-ttu-id="a45e6-120">Dieser Prozess wird in den folgenden Abschnitten ausführlicher erläutert.</span><span class="sxs-lookup"><span data-stu-id="a45e6-120">This process is explained in more detail in the following sections.</span></span>



| <span data-ttu-id="a45e6-121">`Section`</span><span class="sxs-lookup"><span data-stu-id="a45e6-121">Section</span></span>                                                                                                           | <span data-ttu-id="a45e6-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a45e6-122">Description</span></span>                                                                            |
|-------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="a45e6-123">Konfigurieren des WM ASF Writer (QASF)</span><span class="sxs-lookup"><span data-stu-id="a45e6-123">Configuring the WM ASF Writer (QASF)</span></span>](configuring-the-wm-asf-writer--qasf.md)                                   | <span data-ttu-id="a45e6-124">Beschreibt, wie der WM ASF Writer-Filter konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="a45e6-124">Describes how to configure the WM ASF Writer filter.</span></span>                                   |
| [<span data-ttu-id="a45e6-125">Erstellen von Filterdiagrammen zum Schreiben von ASF-Dateien (QASF)</span><span class="sxs-lookup"><span data-stu-id="a45e6-125">Building Filter Graphs to Write ASF Files (QASF)</span></span>](building-filter-graphs-to-write-asf-files--qasf.md)           | <span data-ttu-id="a45e6-126">Beschreibt das Erstellen von Dateitranscodierung und Erfassen von Diagrammen.</span><span class="sxs-lookup"><span data-stu-id="a45e6-126">Describes how to create file-transcoding and capture graphs.</span></span>                           |
| [<span data-ttu-id="a45e6-127">Konfigurieren von Profilen und anderen Dateieigenschaften (QASF)</span><span class="sxs-lookup"><span data-stu-id="a45e6-127">Configuring Profiles and Other File Properties (QASF)</span></span>](configuring-profiles-and-other-file-properties--qasf.md) | <span data-ttu-id="a45e6-128">Beschreibt, wie verschiedene ASF-Dateikonfigurationsaufgaben mit dem WM ASF Writer ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a45e6-128">Describes how to perform various ASF file-configuration tasks using the WM ASF Writer.</span></span> |



 

 

 
