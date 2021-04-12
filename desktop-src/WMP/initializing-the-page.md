---
title: Die Seite wird initialisiert.
description: Die Seite wird initialisiert.
ms.assetid: 66bd3810-01a3-4413-9dad-12cf71e72ed1
keywords:
- Windows Media Player Online Stores, Download-Manager
- Online Stores, Download-Manager
- Typ 2 Online Stores, Download-Manager
- Windows Media Player Online Stores, Initialisieren von Seiten
- Online Stores, Initialisieren von Seiten
- Typ 2 Online Stores, Initialisieren von Seiten
- Windows Media Player, Download-Manager
- Windows Media Player Download-Manager
- Download-Manager
- Initialisieren von Seiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1570d1b77abdc99ba2aee613ed8ddb88fc8097c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207061"
---
# <a name="initializing-the-page"></a><span data-ttu-id="d7e2f-113">Die Seite wird initialisiert.</span><span class="sxs-lookup"><span data-stu-id="d7e2f-113">Initializing the Page</span></span>

<span data-ttu-id="d7e2f-114">Wenn die Webseite geladen wird, wird die **Init** -Funktion ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d7e2f-114">When the webpage loads, the **Init** function runs.</span></span> <span data-ttu-id="d7e2f-115">Mit diesem Code werden zuerst alle in einer vorherigen Sitzung gespeicherten Daten abgerufen.</span><span class="sxs-lookup"><span data-stu-id="d7e2f-115">This code first retrieves any data stored in a previous session.</span></span> <span data-ttu-id="d7e2f-116">Weitere Informationen finden Sie unter Verwalten von [Sitzungsinformationen](maintaining-session-information.md).</span><span class="sxs-lookup"><span data-stu-id="d7e2f-116">For details, see [Maintaining Session Information](maintaining-session-information.md).</span></span> <span data-ttu-id="d7e2f-117">Anschließend wird das **Download Manager** -Objekt erstellt und in der globalen Variablen "g \_ omanager" gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d7e2f-117">It then creates the **DownloadManager** object and stores it in the global variable named g\_oManager.</span></span>


```C++
g_oManager = external.DownloadManager;

```



<span data-ttu-id="d7e2f-118">Als nächstes verbindet die-Funktion das **oncolorchange** -Ereignis mit der-Funktion mit dem Namen " **onappcolor** " und ruft dann die Funktion direkt auf, um die Hintergrundfarbe zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="d7e2f-118">Next, the function connects the **OnColorChange** event to the function named **OnAppColor** and then calls the function directly to initialize the background color.</span></span> <span data-ttu-id="d7e2f-119">Weitere Informationen finden Sie [unter Übereinstimmung der Windows Media Player Farben](matching-the-windows-media-player-colors.md).</span><span class="sxs-lookup"><span data-stu-id="d7e2f-119">See [Matching the Windows Media Player Colors](matching-the-windows-media-player-colors.md).</span></span>

<span data-ttu-id="d7e2f-120">Schließlich startet die Funktion einen Timer mit einem Intervall von einer Sekunde und initialisiert die Listenfelder, in denen die ausstehenden Download Sammlungen und Download Elemente angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d7e2f-120">Finally, the function starts a timer with a one-second interval and initializes the list boxes that display the pending download collections and download items.</span></span> <span data-ttu-id="d7e2f-121">Dies ist wichtig, da während der letzten Schließung des Online Ladens Sitzungen ausgeführt wurden. diese Informationen müssen erneut angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d7e2f-121">This is important because there may have been sessions in progress the last time the online store closed and this information needs to be displayed again.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d7e2f-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d7e2f-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7e2f-123">**Verwenden des Download-Managers**</span><span class="sxs-lookup"><span data-stu-id="d7e2f-123">**Using the Download Manager**</span></span>](using-the-download-manager.md)
</dt> </dl>

 

 




