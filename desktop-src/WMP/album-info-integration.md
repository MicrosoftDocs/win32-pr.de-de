---
title: Integration von Album Informationen
description: Integration von Album Informationen
ms.assetid: c59c0c1b-eddc-4061-87cc-a5c44ae0c15d
keywords:
- Windows Media Player Online Stores, Integration von Albuminformationen
- Online Stores, Integration von Album-Informationen
- Typ 2 Online Stores, Integration von Albuminformationen
- Windows Media Player Online Stores, integrieren von Albuminformationen
- Online Stores, integrieren von Albuminformationen
- Typ 2 Online Stores, integrieren von Albuminformationen
- Windows Media Player, integrieren von Albuminformationen
- Windows Media Player, Integration von Albuminformationen
- Integration von Albuminformationen
- Integrieren von Albuminformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b03586217ec0a0eebd9abd0a9acae62790f838f3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036881"
---
# <a name="album-info-integration"></a><span data-ttu-id="4d90c-113">Integration von Album Informationen</span><span class="sxs-lookup"><span data-stu-id="4d90c-113">Album Info Integration</span></span>

<span data-ttu-id="4d90c-114">Windows Media Player ermöglicht es Benutzern, ausführliche Informationen über die CD oder DVD anzufordern, von denen aus Inhalte für digitale Medien stammen, indem Sie auf eine Schaltfläche klicken, z. b. **Weitere Informationen**.</span><span class="sxs-lookup"><span data-stu-id="4d90c-114">Windows Media Player enables users to request detailed information about the CD or DVD from which digital media content originated by clicking a button, such as **More Info**.</span></span> <span data-ttu-id="4d90c-115">Wenn der Benutzer auf die Schaltfläche klickt, ruft Windows Media Player 10 oder höher im aktuellen Musikspeicher auf, um die Details zum Album anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="4d90c-115">When the user clicks the button, Windows Media Player 10 or later calls on the current music store to display the album details.</span></span> <span data-ttu-id="4d90c-116">Wenn dies der Fall ist, öffnet der Spieler den Bereich "Informationen zum Album" und zeigt die Webseite an, die vom Attribut " **URL** " des Elements " **Albuminfo** " des serviceInfo-Dokuments angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4d90c-116">When this happens, the Player opens the album information pane and displays the webpage specified by the **URL** attribute of the **AlbumInfo** element of the ServiceInfo document.</span></span>

<span data-ttu-id="4d90c-117">Windows Media Player Fügt eine Abfrage Zeichenfolge an die URL an, um dem Onlinespeicher Informationen über den vom Benutzer angeforderten Inhalt bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="4d90c-117">Windows Media Player appends a query string to the URL to provide information to the online store about the content the user requested.</span></span> <span data-ttu-id="4d90c-118">Die Abfrage Zeichenfolge enthält Attribute wie " **Title**", " **Album**" und " **Artist**", mit denen der Online Shop das richtige Album zum Anzeigen bestimmen kann.</span><span class="sxs-lookup"><span data-stu-id="4d90c-118">The query string includes attributes like **Title**, **Album**, and **Artist**, which the online store can use to determine the correct album to display.</span></span> <span data-ttu-id="4d90c-119">Die Referenz Dokumentation für das Element " **Albuminfo** " enthält die komplette Liste der Attribute der Abfrage Zeichenfolge und deren Beschreibungen.</span><span class="sxs-lookup"><span data-stu-id="4d90c-119">The reference documentation for the **AlbumInfo** element provides the complete list of query string attributes and their descriptions.</span></span>

## <a name="guidelines-for-album-info"></a><span data-ttu-id="4d90c-120">Richtlinien für die Album Informationen</span><span class="sxs-lookup"><span data-stu-id="4d90c-120">Guidelines for Album Info</span></span>

<span data-ttu-id="4d90c-121">Beachten Sie beim Erstellen der Webseite mit den Albuminformationen die folgenden Richtlinien:</span><span class="sxs-lookup"><span data-stu-id="4d90c-121">When creating your album information webpage, use the following guidelines:</span></span>

-   <span data-ttu-id="4d90c-122">Die Seite muss den Online Store, der die Informationen bereitstellt, eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="4d90c-122">The page must clearly identify the online store providing the information.</span></span> <span data-ttu-id="4d90c-123">Dies ist möglich, indem Sie Ihr Logo hervorgehoben anzeigen, z. b..</span><span class="sxs-lookup"><span data-stu-id="4d90c-123">You can do this by prominently displaying your logo, for example.</span></span>
-   <span data-ttu-id="4d90c-124">Die Seite muss einen Link zu den Datenschutzbestimmungen Ihres Unternehmens enthalten.</span><span class="sxs-lookup"><span data-stu-id="4d90c-124">The page must include a link to your company's privacy statement.</span></span>
-   <span data-ttu-id="4d90c-125">Vermeiden Sie die Seitennavigation innerhalb der Album Informationsfunktion, wenn dies möglich ist.</span><span class="sxs-lookup"><span data-stu-id="4d90c-125">Avoid page navigation within the album information feature whenever possible.</span></span> <span data-ttu-id="4d90c-126">Für die meisten Aktivitäten sollten Sie zu Ihrem Online Store navigieren.</span><span class="sxs-lookup"><span data-stu-id="4d90c-126">You should navigate to your online store for most activities.</span></span>
-   <span data-ttu-id="4d90c-127">Es wird empfohlen, dass Sie wertvolle Informationen bereitstellen, ohne dass der Benutzer Programme installieren oder sich beim Online Shop anmelden muss.</span><span class="sxs-lookup"><span data-stu-id="4d90c-127">We recommend that you provide valuable information without requiring the user to install programs or log in to your online store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4d90c-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4d90c-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d90c-129">**Informationen zu Typ 2 Online Stores**</span><span class="sxs-lookup"><span data-stu-id="4d90c-129">**About Type 2 Online Stores**</span></span>](about-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="4d90c-130">**Albuminfo-Element**</span><span class="sxs-lookup"><span data-stu-id="4d90c-130">**AlbumInfo Element**</span></span>](albuminfo-element.md)
</dt> </dl>

 

 




