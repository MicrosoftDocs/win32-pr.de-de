---
title: Präsentationszeit
description: Präsentationszeit
ms.assetid: 856e1783-85b4-4195-970f-3d7b5612672b
keywords:
- Windows Media-Format-SDK, Präsentations Zeiten
- Advanced Systems Format (ASF), Präsentations Zeiten
- ASF (Advanced Systems Format), Präsentations Zeiten
- Präsentations Zeiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bc88dbba93d1fc68905a4bfea92328a4ef600eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310895"
---
# <a name="presentation-time"></a><span data-ttu-id="c9cda-107">Präsentationszeit</span><span class="sxs-lookup"><span data-stu-id="c9cda-107">Presentation Time</span></span>

<span data-ttu-id="c9cda-108">Eine Präsentationszeit ist eine Zeitmessung aus dem ersten Beispiel des ersten Datenstroms in einer ASF-Datei.</span><span class="sxs-lookup"><span data-stu-id="c9cda-108">A presentation time is a measurement of time from the first sample of the first stream in an ASF file.</span></span> <span data-ttu-id="c9cda-109">Diese Messung und die meisten anderen Messungen der Zeit, die von den Objekten dieses SDK verwendet werden, liegen in 100-Nanosecond-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="c9cda-109">This measurement, as well as most other measurements of time used by the objects of this SDK, is in 100-nanosecond units.</span></span> <span data-ttu-id="c9cda-110">Präsentations Zeiten sind wichtig, da Sie ermöglichen, dass die verschiedenen Streams in einer Datei synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="c9cda-110">Presentation times are important because they enable the various streams in a file to be synchronized.</span></span> <span data-ttu-id="c9cda-111">Sie müssen für jedes Eingabe Beispiel, das Sie an den Writer übergeben, eine Präsentationszeit angeben.</span><span class="sxs-lookup"><span data-stu-id="c9cda-111">You must supply a presentation time for each input sample you pass to the writer.</span></span> <span data-ttu-id="c9cda-112">Jedem Datenobjekt im Daten Abschnitt einer ASF-Datei ist eine Präsentationszeit zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="c9cda-112">Every data object in the data section of an ASF file has a presentation time associated with it.</span></span> <span data-ttu-id="c9cda-113">Alle Ausgabe Beispiele, die vom Reader abgerufen werden, haben auch eine Präsentationszeit.</span><span class="sxs-lookup"><span data-stu-id="c9cda-113">Every output sample retrieved by the reader also has a presentation time.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c9cda-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c9cda-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9cda-115">**Konzepte**</span><span class="sxs-lookup"><span data-stu-id="c9cda-115">**Concepts**</span></span>](concepts.md)
</dt> <dt>

[<span data-ttu-id="c9cda-116">**Eingaben, Streams und Ausgaben**</span><span class="sxs-lookup"><span data-stu-id="c9cda-116">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> <dt>

[<span data-ttu-id="c9cda-117">**Medien Beispiele**</span><span class="sxs-lookup"><span data-stu-id="c9cda-117">**Media Samples**</span></span>](media-samples.md)
</dt> </dl>

 

 




