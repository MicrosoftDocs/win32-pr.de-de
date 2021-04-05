---
title: Ablauf Steuerung
description: Ablauf Steuerung
ms.assetid: b91c0191-1908-4d62-96ce-927d09c70f9a
keywords:
- Visualisierungen, Programmfluss
- benutzerdefinierte Visualisierungen, Programmfluss
- Visualisierungen, Ablauf Steuerung
- benutzerdefinierte Visualisierungen, Ablauf Steuerung
- Visualisierungen, zeitgesteuerte Ereignisse
- benutzerdefinierte Visualisierungen, zeitgesteuerte Ereignisse
- Visualisierungen, Rendering-Funktion
- benutzerdefinierte Visualisierungen, Rendering-Funktion
- Visualisierungen, renderwindow-Funktion
- benutzerdefinierte Visualisierungen, renderwindow-Funktion
- Renderfunktion, Visualisierungsprogramm Fluss
- Renderwindow-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bca09760d958da045c4bbf60ae122a9d0ae4c71c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947476"
---
# <a name="flow-of-control"></a><span data-ttu-id="d46d9-115">Ablauf Steuerung</span><span class="sxs-lookup"><span data-stu-id="d46d9-115">Flow of Control</span></span>

<span data-ttu-id="d46d9-116">Audiodaten kommen in Windows Media Player fortlaufend über eine Datei oder einen Stream.</span><span class="sxs-lookup"><span data-stu-id="d46d9-116">Audio data comes into Windows Media Player continuously through a file or a stream.</span></span> <span data-ttu-id="d46d9-117">Diese Daten werden an ihre Visualisierung übermittelt.</span><span class="sxs-lookup"><span data-stu-id="d46d9-117">That data is passed to your visualization.</span></span> <span data-ttu-id="d46d9-118">Sie zeichnen eine definierte Oberfläche und übergeben diese wieder an Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="d46d9-118">You draw on a defined surface and pass that surface back to Windows Media Player.</span></span> <span data-ttu-id="d46d9-119">Dieser Austausch erfolgt mehrmals pro Sekunde, und für den Benutzer ist das Ergebnis eine angenehme Animation, die sich in der Zeit auf die Musik verschiebt.</span><span class="sxs-lookup"><span data-stu-id="d46d9-119">This interchange happens several times a second, and to the user, the result is a pleasing animation that moves in time to the music.</span></span>

<span data-ttu-id="d46d9-120">Im folgenden finden Sie eine bestimmte Abfolge des Visualisierungsprogramm Flusses:</span><span class="sxs-lookup"><span data-stu-id="d46d9-120">Here is the specific sequence of the visualization program flow:</span></span>

1.  <span data-ttu-id="d46d9-121">In einem zeitgesteuerten Intervall nimmt Windows Media Player eine Momentaufnahme der wiedergegebenen Audiodatei an.</span><span class="sxs-lookup"><span data-stu-id="d46d9-121">At a timed interval, Windows Media Player takes a snapshot of the audio that is playing.</span></span>
2.  <span data-ttu-id="d46d9-122">Windows Media Player stellt die Daten aus dieser Momentaufnahme über die Funktion " **Rendering** " und die **renderwindowed** -Funktion für die Visualisierung bereit.</span><span class="sxs-lookup"><span data-stu-id="d46d9-122">Windows Media Player supplies the data from that snapshot to your visualization through the **Render** function and the **RenderWindowed** function.</span></span>
3.  <span data-ttu-id="d46d9-123">Sie müssen Code schreiben, der ausgeführt wird, wenn " **Rendering** " und " **renderwindowed** " aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d46d9-123">You must write code that will run when **Render** and **RenderWindowed** is called.</span></span> <span data-ttu-id="d46d9-124">Der Code zeichnet mithilfe eines Geräte Kontexts, der von Windows Media Player beim Rendern von fensterlosen Funktionen definiert wird, oder mithilfe eines Fensters, das Sie beim Rendern des Fensters erstellen.</span><span class="sxs-lookup"><span data-stu-id="d46d9-124">Your code draws by using a device context defined by Windows Media Player when rendering windowless, or by using a window that you create when rendering windowed.</span></span>
4.  <span data-ttu-id="d46d9-125">In einer von der aktuellen Skin angegebenen Region zeigt Windows Media Player an, was Ihr Code gezeichnet hat.</span><span class="sxs-lookup"><span data-stu-id="d46d9-125">In a region specified by the current skin, Windows Media Player displays what your code drew.</span></span>
5.  <span data-ttu-id="d46d9-126">Dieser Vorgang wird mehrmals pro Sekunde wiederholt, wobei grafische Animationen erstellt werden, für die die Musik Zeitüberschreitung hat.</span><span class="sxs-lookup"><span data-stu-id="d46d9-126">This process repeats several times a second, creating graphical animations that are timed to the music.</span></span> <span data-ttu-id="d46d9-127">Wenn die Musik angehalten wird, wird die Visualisierung angehalten.</span><span class="sxs-lookup"><span data-stu-id="d46d9-127">When the music stops playing, the visualization stops.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d46d9-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d46d9-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d46d9-129">**Entwickler Übersicht**</span><span class="sxs-lookup"><span data-stu-id="d46d9-129">**Developer Overview**</span></span>](developer-overview.md)
</dt> </dl>

 

 




