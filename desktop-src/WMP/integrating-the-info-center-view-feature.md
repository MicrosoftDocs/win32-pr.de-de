---
title: Integrieren der Info Center-Ansichts Funktion
description: Integrieren der Info Center-Ansichts Funktion
ms.assetid: ce6692d2-a780-4aab-809f-c63236edd912
keywords:
- Windows Media Player Online Stores, integrieren der Info Center-Ansicht
- Online Stores, integrieren der Info Center-Ansicht
- Typ 1 Online Stores, Integration der Info Center-Ansicht
- Typ 2 Online Stores, Integration der Info Center-Ansicht
- Windows Media Player Online Stores, Info Center-Ansicht
- Online Stores, Info Center-Ansicht
- Typ 1 Online Stores, Info Center-Ansicht
- Typ 2 Online Stores, Info Center-Ansicht
- Integrieren der Info Center-Ansicht
- Info Center-Ansicht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9564a6210181e0500bd1e447f621568f634817c4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341883"
---
# <a name="integrating-the-info-center-view-feature"></a><span data-ttu-id="6e2a9-113">Integrieren der Info Center-Ansichts Funktion</span><span class="sxs-lookup"><span data-stu-id="6e2a9-113">Integrating the Info Center View Feature</span></span>

<span data-ttu-id="6e2a9-114">Windows Media Player ermöglicht Benutzern das Öffnen und Schließen der Info Center-Ansichts Funktion.</span><span class="sxs-lookup"><span data-stu-id="6e2a9-114">Windows Media Player enables users to open and close the Info Center View feature.</span></span> <span data-ttu-id="6e2a9-115">Die Info Center-Ansicht ist die Funktion, mit der Benutzer umfassende, erweiterte Informationen zu bestimmten digitalen Medieninhalten finden.</span><span class="sxs-lookup"><span data-stu-id="6e2a9-115">Info Center View is the feature where users expect to find rich, extended information about specific digital media content.</span></span> <span data-ttu-id="6e2a9-116">Wenn der Benutzer die InfoCenter-Ansicht öffnet, ruft Windows Media Player auf dem aktuellen Musikspeicher auf, um die InfoCenter-Ansichts Webseite anzuzeigen, die durch das **URL** -Attribut des **Infocenter** -Elements des serviceInfo-Dokuments angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6e2a9-116">When the user chooses to open Info Center View, Windows Media Player calls on the current music store to display the Info Center View webpage specified by the **URL** attribute of the **InfoCenter** element of the ServiceInfo document.</span></span>

<span data-ttu-id="6e2a9-117">Zum Abrufen von Informationen über den Inhalt, der aktuell wiedergegeben wird, müssen Sie eine Instanz des Windows Media Player-Steuer Elements in Ihre Webseite einbetten und das Player-Objektmodell verwenden.</span><span class="sxs-lookup"><span data-stu-id="6e2a9-117">To retrieve information about the currently playing digital media content, you must embed an instance of the Windows Media Player control in your webpage and use the Player object model.</span></span> <span data-ttu-id="6e2a9-118">Zum Abrufen des Titels können Sie z. b. den folgenden JScript-Code verwenden:</span><span class="sxs-lookup"><span data-stu-id="6e2a9-118">For example, to retrieve the title, you could use the following JScript code:</span></span>


```C++
// The control was created with ID = "Player"
var title = Player.currentMedia.getItemInfoByType("Title", "", 0);
```



## <a name="guidelines-for-info-center-view"></a><span data-ttu-id="6e2a9-119">Richtlinien für die Info Center-Ansicht</span><span class="sxs-lookup"><span data-stu-id="6e2a9-119">Guidelines for Info Center View</span></span>

<span data-ttu-id="6e2a9-120">Verwenden Sie beim Erstellen der **Info Center-Ansichts** Webseite die folgenden Richtlinien:</span><span class="sxs-lookup"><span data-stu-id="6e2a9-120">When creating your **Info Center View** webpage, use the following guidelines:</span></span>

-   <span data-ttu-id="6e2a9-121">Die Seite muss den Online Store, der die Informationen bereitstellt, eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="6e2a9-121">The page must clearly identify the online store providing the information.</span></span> <span data-ttu-id="6e2a9-122">Dies ist möglich, indem Sie Ihr Logo hervorgehoben anzeigen, z. b..</span><span class="sxs-lookup"><span data-stu-id="6e2a9-122">You can do this by prominently displaying your logo, for example.</span></span>
-   <span data-ttu-id="6e2a9-123">Die Seite muss einen Link zu den Datenschutzbestimmungen Ihres Unternehmens enthalten.</span><span class="sxs-lookup"><span data-stu-id="6e2a9-123">The page must include a link to your company's privacy statement.</span></span>
-   <span data-ttu-id="6e2a9-124">Vermeiden Sie die Seitennavigation innerhalb der Info Center-Ansichts Funktion, wenn möglich.</span><span class="sxs-lookup"><span data-stu-id="6e2a9-124">Avoid page navigation within the Info Center View feature whenever possible.</span></span> <span data-ttu-id="6e2a9-125">Für die meisten Aktivitäten sollten Sie zu Ihrem Online Store navigieren.</span><span class="sxs-lookup"><span data-stu-id="6e2a9-125">You should navigate to your online store for most activities.</span></span>
-   <span data-ttu-id="6e2a9-126">Es empfiehlt sich, wertvolle Informationen bereitzustellen, ohne dass der Benutzer Programme installieren oder sich beim Online Shop anmelden muss.</span><span class="sxs-lookup"><span data-stu-id="6e2a9-126">It is best to provide valuable information without requiring the user to install programs or log in to your online store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6e2a9-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6e2a9-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e2a9-128">**Extern. navigatetaskpaneurl**</span><span class="sxs-lookup"><span data-stu-id="6e2a9-128">**External.NavigateTaskPaneURL**</span></span>](external-navigatetaskpaneurl.md)
</dt> <dt>

[<span data-ttu-id="6e2a9-129">**InfoCenter-Element**</span><span class="sxs-lookup"><span data-stu-id="6e2a9-129">**InfoCenter Element**</span></span>](infocenter-element.md)
</dt> <dt>

[<span data-ttu-id="6e2a9-130">**Informationen, die von Typ 1 und Typ 2 Online Stores gemeinsam sind**</span><span class="sxs-lookup"><span data-stu-id="6e2a9-130">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="6e2a9-131">**Verwenden des Windows Media Player-Steuer Elements in einer Webseite**</span><span class="sxs-lookup"><span data-stu-id="6e2a9-131">**Using the Windows Media Player Control in a Web Page**</span></span>](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




