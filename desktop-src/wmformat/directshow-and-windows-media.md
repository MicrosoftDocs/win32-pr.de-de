---
title: DirectShow-und Windows-Medien
description: DirectShow-und Windows-Medien
ms.assetid: e2ddc781-9f56-4f77-a191-015018755eff
keywords:
- Windows Media-Format-SDK, DirectShow
- Advanced Systems Format (ASF), DirectShow
- ASF (Advanced Systems Format), DirectShow
- DirectShow, Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd4ca8eb4b1051d6685efa0bf73052ad9e7b31fa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714214"
---
# <a name="directshow-and-windows-media"></a><span data-ttu-id="01013-107">DirectShow-und Windows-Medien</span><span class="sxs-lookup"><span data-stu-id="01013-107">DirectShow and Windows Media</span></span>

<span data-ttu-id="01013-108">Anstatt das Windows Media SDK exklusiv zu verwenden, können Anwendungen auch Windows Media-basierte Inhalte mithilfe der Microsoft® DirectShow® Streaming-Architektur lesen und schreiben, wie in den folgenden Abschnitten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="01013-108">As an alternative to using the Windows Media Format SDK exclusively, applications can also read and write Windows Media-based content by using the Microsoft® DirectShow® streaming architecture, as described in the following sections.</span></span>



| <span data-ttu-id="01013-109">`Section`</span><span class="sxs-lookup"><span data-stu-id="01013-109">Section</span></span>                                                                                   | <span data-ttu-id="01013-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="01013-110">Description</span></span>                                                                                                                                 |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="01013-111">Informationen zu DirectShow</span><span class="sxs-lookup"><span data-stu-id="01013-111">About DirectShow</span></span>](about-directshow.md)                                                  | <span data-ttu-id="01013-112">Beschreibt DirectShow in allgemeinen Begriffen und gibt Aufschluss darüber, wo Sie weitere Informationen erhalten.</span><span class="sxs-lookup"><span data-stu-id="01013-112">Describes DirectShow in general terms and tells where to get more information about it.</span></span>                                                     |
| [<span data-ttu-id="01013-113">Gründe für die Verwendung von DirectShow</span><span class="sxs-lookup"><span data-stu-id="01013-113">Why Use DirectShow?</span></span>](why-use-directshow.md)                                             | <span data-ttu-id="01013-114">Beschreibt, wie DirectShow bestimmte Aufgaben beim Erstellen und Wiedergeben von Windows Media – basierten Inhalten vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="01013-114">Describes how DirectShow simplifies certain tasks in the creation and playback of Windows Media–based content.</span></span>                              |
| [<span data-ttu-id="01013-115">Lesen von ASF-Dateien in DirectShow</span><span class="sxs-lookup"><span data-stu-id="01013-115">Reading ASF Files in DirectShow</span></span>](reading-asf-files-in-directshow.md)                    | <span data-ttu-id="01013-116">Beschreibt die Wiedergabe von ASF-Dateien mithilfe von DirectShow.</span><span class="sxs-lookup"><span data-stu-id="01013-116">Describes how to play ASF files using DirectShow.</span></span>                                                                                           |
| [<span data-ttu-id="01013-117">Erstellen von ASF-Dateien in DirectShow</span><span class="sxs-lookup"><span data-stu-id="01013-117">Creating ASF Files in DirectShow</span></span>](creating-asf-files-in-directshow.md)                  | <span data-ttu-id="01013-118">Beschreibt das Erstellen von ASF-Dateien mithilfe von DirectShow.</span><span class="sxs-lookup"><span data-stu-id="01013-118">Describes how to create ASF files using DirectShow.</span></span>                                                                                         |
| [<span data-ttu-id="01013-119">WMT- \_ Status Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="01013-119">WMT\_STATUS Event Notification in DirectShow</span></span>](wmt-status-notification-in-directshow.md) | <span data-ttu-id="01013-120">Beschreibt, welche **WMT- \_ Status** Ereignisse von den "ASF Reader"-und "ASF Writer"-Filtern behandelt werden und wie Anwendungen diese Ereignisse empfangen können.</span><span class="sxs-lookup"><span data-stu-id="01013-120">Describes which **WMT\_STATUS** events are handled by the ASF Reader and ASF Writer filters, and how applications can receive those events.</span></span> |
| [<span data-ttu-id="01013-121">DRM-Unterstützung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="01013-121">DRM Support in DirectShow</span></span>](drm-support-in-directshow.md)                                | <span data-ttu-id="01013-122">Beschreibt das Lesen und Schreiben von DRM-geschützten Dateien über DirectShow.</span><span class="sxs-lookup"><span data-stu-id="01013-122">Describes how to read and write DRM-protected files through DirectShow.</span></span>                                                                     |
| [<span data-ttu-id="01013-123">DirectShow-qasf-Referenz</span><span class="sxs-lookup"><span data-stu-id="01013-123">DirectShow QASF Reference</span></span>](directshow-qasf-reference.md)                                | <span data-ttu-id="01013-124">Enthält die Referenz Dokumentation für die DirectShow-Komponenten, die Windows-Medien unterstützen.</span><span class="sxs-lookup"><span data-stu-id="01013-124">Contains the reference documentation for the DirectShow components that support Windows Media.</span></span>                                              |



 

<span data-ttu-id="01013-125">Drei Beispielanwendungen im SDK veranschaulichen die Verwendung von DirectShow: dscopy, dsplay und dsseekfm.</span><span class="sxs-lookup"><span data-stu-id="01013-125">Three sample applications in the SDK illustrate the use of DirectShow: DSCopy, DSPlay, and DSSeekFM.</span></span> <span data-ttu-id="01013-126">Weitere Informationen finden Sie unter [Beispielanwendungen](sample-applications.md).</span><span class="sxs-lookup"><span data-stu-id="01013-126">For more information, see [Sample Applications](sample-applications.md).</span></span>

> [!Note]  
> <span data-ttu-id="01013-127">Anwendungen, die die in diesem SDK enthaltenen qasf-Komponenten verwenden, erfordern, dass die SDK-Laufzeit von Microsoft DirectX® 8,1 oder höher unter Windows® 2000, Windows 98 und Windows 95 Systems installiert wird.</span><span class="sxs-lookup"><span data-stu-id="01013-127">Applications that use the QASF components included in this SDK require the Microsoft DirectX® 8.1 or later SDK runtime to be installed on Windows® 2000, Windows 98, and Windows 95 systems.</span></span> <span data-ttu-id="01013-128">Diese Laufzeit ist insbesondere für den DMO-Wrapper Filter erforderlich, der die Windows Media-Codecs in einem DirectShow-Filter Diagramm hostet.</span><span class="sxs-lookup"><span data-stu-id="01013-128">Specifically, this runtime is required by the DMO Wrapper filter which hosts the Windows Media codecs in a DirectShow filter graph.</span></span>

 

 

 




