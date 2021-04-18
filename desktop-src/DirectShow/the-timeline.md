---
description: Die Zeitachse
ms.assetid: a3b8bff2-8593-483c-af49-a975ab2dc330
title: Die Zeitachse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e6ac73b84409629f63ad4be469edf6b943f9e64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351153"
---
# <a name="the-timeline"></a><span data-ttu-id="c47eb-103">Die Zeitachse</span><span class="sxs-lookup"><span data-stu-id="c47eb-103">The Timeline</span></span>

<span data-ttu-id="c47eb-104">\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="c47eb-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="c47eb-105">Die Zeitachse macht die [**iamtimeline**](iamtimeline.md) -Schnittstelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c47eb-105">The timeline exposes the [**IAMTimeline**](iamtimeline.md) interface.</span></span> <span data-ttu-id="c47eb-106">Diese Schnittstelle enthält Methoden zum Festlegen von Eigenschaften auf der Zeitachse. zum Hinzufügen von Gruppen zur Zeitachse; und zum Erstellen von Zeitachsen Objekten, wie z. b. Gruppen, Spuren und Quellen.</span><span class="sxs-lookup"><span data-stu-id="c47eb-106">This interface contains methods for setting properties on the timeline; for adding groups to the timeline; and for creating timeline objects, such as groups, tracks, and sources.</span></span> <span data-ttu-id="c47eb-107">Um eine neue Zeitachse zu erstellen, rufen Sie die standardmäßige **cokreateinstance** -Funktion wie folgt auf:</span><span class="sxs-lookup"><span data-stu-id="c47eb-107">To create a new timeline, call the standard **CoCreateInstance** function as follows:</span></span>


```C++
IAMTimeline *pTL = NULL;
hr = CoCreateInstance(CLSID_AMTimeline, NULL, CLSCTX_INPROC_SERVER, 
        IID_IAMTimeline, (void**)&pTL);
```



<span data-ttu-id="c47eb-108">Die neue Zeitachse ist leer.</span><span class="sxs-lookup"><span data-stu-id="c47eb-108">The new timeline is empty.</span></span> <span data-ttu-id="c47eb-109">An diesem Punkt können Sie entweder eine vorhandene Projektdatei laden (siehe [Laden und Anzeigen der Vorschau eines Projekts](loading-and-previewing-a-project.md)) oder die Zeitachse erstellen, indem Sie neue Objekte erstellen und Einfügen (siehe [Erstellen einer Zeitachse](constructing-a-timeline.md)).</span><span class="sxs-lookup"><span data-stu-id="c47eb-109">At this point you can either load an existing project file (see [Loading and Previewing a Project](loading-and-previewing-a-project.md)), or build up the timeline by creating and inserting new objects (see [Constructing a Timeline](constructing-a-timeline.md)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c47eb-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c47eb-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c47eb-111">Übersicht über die Zeitachsen Komponenten</span><span class="sxs-lookup"><span data-stu-id="c47eb-111">Overview of the Timeline Components</span></span>](overview-of-the-timeline-components.md)
</dt> </dl>

 

 



