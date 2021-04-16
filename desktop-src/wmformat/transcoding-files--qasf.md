---
title: Transcoding-Dateien (qasf)
description: Transcoding-Dateien (qasf)
ms.assetid: c6dad6cf-4781-4204-883b-cdb33aff5e27
keywords:
- Windows Media-Format-SDK, Transcoding-Dateien (qasf)
- Windows Media-Format-SDK, DirectShow
- Advanced Systems Format (ASF), Transcoding-Dateien (qasf)
- ASF (Advanced Systems Format), Transcoding-Dateien (qasf)
- Advanced Systems Format (ASF), DirectShow
- ASF (Advanced Systems Format), DirectShow
- DirectShow, Transcoding-Dateien (qasf)
- Windows Media-Format-SDK, qasf
- Advanced Systems Format (ASF), qasf
- ASF (Advanced Systems Format), qasf
- DirectShow, qasf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14387a65538d411bcd41b4b907f2adbab2089f71
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104551128"
---
# <a name="transcoding-files-qasf"></a><span data-ttu-id="38431-114">Transcoding-Dateien (qasf)</span><span class="sxs-lookup"><span data-stu-id="38431-114">Transcoding Files (QASF)</span></span>

<span data-ttu-id="38431-115">Sie können ein Datei-transcodierungsfilterdiagramm mit dem [WM-ASF-Writer](wm-asf-writer-filter.md) auf verschiedene Weise erstellen.</span><span class="sxs-lookup"><span data-stu-id="38431-115">You can build a file-transcoding filter graph using the [WM ASF Writer](wm-asf-writer-filter.md) in various ways.</span></span> <span data-ttu-id="38431-116">Die einfachste Möglichkeit besteht darin, den WM-ASF-Writer im Filter Diagramm zu erstellen, zu konfigurieren und den WM-ASF-Writer hinzuzufügen. Anschließend können Sie das Diagramm mit der **igraphbuilder:: RenderFile** -Methode automatisch erstellen.</span><span class="sxs-lookup"><span data-stu-id="38431-116">The easiest way is to co-create, configure, and add the WM ASF Writer to the filter graph, and then use the **IGraphBuilder::RenderFile** method to build the graph automatically.</span></span>

<span data-ttu-id="38431-117">Eine alternative Möglichkeit besteht darin, jeden Filter manuell dem Diagramm hinzuzufügen und die Pins zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="38431-117">An alternative way is to add each filter manually to the graph and connect the pins.</span></span> <span data-ttu-id="38431-118">Nachdem Sie den WM-ASF-Writer hinzugefügt haben, konfigurieren Sie ihn mithilfe der **iconfigasfwriter** -Methoden, wenn das Standardprofil nicht geeignet ist, und verbinden Sie die WM-ASF-Eingabe Pins mit den entsprechenden Ausgabe Pins in den upstreamfiltern.</span><span class="sxs-lookup"><span data-stu-id="38431-118">After adding the WM ASF Writer, configure it by using the **IConfigAsfWriter** methods if the default profile is not suitable, and connect the WM ASF Writer input pins to the corresponding output pins on the upstream filters.</span></span>

<span data-ttu-id="38431-119">Die folgende Abbildung zeigt die typischen Konfigurationen von "WM-ASF-Writer-Transcodierungs Filter"</span><span class="sxs-lookup"><span data-stu-id="38431-119">The following illustration shows typical WM ASF Writer transcoding filter graph configurations.</span></span>

![Typische Transcodierungs Filter Diagramme](images/asf-transcode.png)

 

 




