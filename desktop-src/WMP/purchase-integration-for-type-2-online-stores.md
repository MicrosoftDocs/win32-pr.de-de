---
title: Kauf Integration für den Typ 2-Online Speicher
description: Kauf Integration für den Typ 2-Online Speicher
ms.assetid: aedaa6a0-d559-44b7-9c14-2abf44478b1c
keywords:
- Windows Media Player Online Stores, Kauf Integration
- Online Stores, Kauf Integration
- Typ 2 Online Stores, Kauf Integration
- Windows Media Player Online Stores, integrieren von Käufen
- Online Stores, integrieren von Käufen
- Typ 2 Online Stores, integrieren von Käufen
- Windows Media Player, Kauf Integration
- Windows Media Player, integrieren von Käufen
- Kauf Integration
- Integrieren von Käufen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3d8fb56b286b66de12bb59412e7f9077eb398f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338398"
---
# <a name="purchase-integration-for-type-2-online-stores"></a><span data-ttu-id="de4aa-113">Kauf Integration für den Typ 2-Online Speicher</span><span class="sxs-lookup"><span data-stu-id="de4aa-113">Purchase Integration for Type 2 Online Stores</span></span>

<span data-ttu-id="de4aa-114">Wenn Windows Media Player Inhalt digitaler Medien wieder gibt oder der Benutzer die **Suche nach Album Informationen** auswählt, bietet der Player dem Benutzer einen Link, um die CD oder DVD zu kaufen, von der der Inhalt stammt, wenn ein solcher Link verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="de4aa-114">When Windows Media Player plays digital media content or the user chooses **Find Album Info**, the Player offers the user a link to buy the CD or DVD from which the content originated if such a link is available.</span></span> <span data-ttu-id="de4aa-115">Wenn der Benutzer auf den Link klickt, ruft Windows Media Player 10 oder höher den aktuellen Musikspeicher auf, um die Kauf Anforderung zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="de4aa-115">When the user clicks the link, Windows Media Player 10 or later calls on the current music store to handle the purchase request.</span></span> <span data-ttu-id="de4aa-116">In diesem Fall navigiert der Player zum ersten Dienstaufgaben Bereich (in Windows Media Player 10) oder der Registerkarte "Online Stores" (in Windows Media Player 11) und zeigt die Webseite an, die vom Attribut " **mediaplayerurl** " des Elements " **buycd** " des serviceInfo-Dokuments angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="de4aa-116">When this happens, the Player navigates to the first service task pane (in Windows Media Player 10) or the Online Stores tab (in Windows Media Player 11) and displays the webpage specified by the **MediaPlayerURL** attribute of the **BuyCD** element of the ServiceInfo document.</span></span> <span data-ttu-id="de4aa-117">(Die Attribute " **mediacenterurl** " und " **browserurl** " werden auf ähnliche Weise verwendet, um Aufrufe von Windows XP Media Center Edition 2004 und Windows XP Service Pack 2) zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="de4aa-117">(The **MediaCenterURL** and **BrowserURL** attributes are used in a similar manner to handle calls from Windows XP Media Center Edition 2004 and Windows XP Service Pack 2).</span></span>

<span data-ttu-id="de4aa-118">Windows Media Player Fügt eine Abfrage Zeichenfolge an die URL an, um dem Online Shop Informationen zu den Inhalten bereitzustellen, die der Benutzer erworben hat.</span><span class="sxs-lookup"><span data-stu-id="de4aa-118">Windows Media Player appends a query string to the URL to provide information to the online store about the content the user chose to purchase.</span></span> <span data-ttu-id="de4aa-119">Die Abfrage Zeichenfolge enthält Attribute wie " **Title**", " **Album**" und " **Artist**", die der Online Shop zum Ermitteln des richtigen zu verkaufenden Albums verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="de4aa-119">The query string includes attributes like **Title**, **Album**, and **Artist**, which the online store can use to determine the correct album to sell.</span></span> <span data-ttu-id="de4aa-120">Die Referenz Dokumentation für das **buycd** -Element enthält die komplette Liste der Attribute der Abfrage Zeichenfolge und deren Beschreibungen.</span><span class="sxs-lookup"><span data-stu-id="de4aa-120">The reference documentation for the **BuyCD** element provides the complete list of query string attributes and their descriptions.</span></span>

## <a name="guidelines-for-the-buycd-page"></a><span data-ttu-id="de4aa-121">Richtlinien für die Seite "buycd"</span><span class="sxs-lookup"><span data-stu-id="de4aa-121">Guidelines for the BuyCD Page</span></span>

<span data-ttu-id="de4aa-122">Verwenden Sie beim Erstellen der Webseite für die buycd die folgenden Richtlinien:</span><span class="sxs-lookup"><span data-stu-id="de4aa-122">When creating your BuyCD webpage, use the following guidelines:</span></span>

-   <span data-ttu-id="de4aa-123">Die Seite muss den Online Store, der die Informationen bereitstellt, eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="de4aa-123">The page must clearly identify the online store providing the information.</span></span> <span data-ttu-id="de4aa-124">Dies ist möglich, indem Sie Ihr Logo hervorgehoben anzeigen, z. b..</span><span class="sxs-lookup"><span data-stu-id="de4aa-124">You can do this by prominently displaying your logo, for example.</span></span>
-   <span data-ttu-id="de4aa-125">Die Seite muss einen Link zu den Datenschutzbestimmungen Ihres Unternehmens enthalten.</span><span class="sxs-lookup"><span data-stu-id="de4aa-125">The page must include a link to your company's privacy statement.</span></span>
-   <span data-ttu-id="de4aa-126">Es empfiehlt sich, anfängliche Kauf Informationen bereitzustellen, ohne dass der Benutzer Programme installieren oder sich beim Online Shop anmelden muss.</span><span class="sxs-lookup"><span data-stu-id="de4aa-126">It is best to provide initial purchasing information without requiring the user to install programs or log in to your online store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="de4aa-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="de4aa-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de4aa-128">**Informationen zu Typ 2 Online Stores**</span><span class="sxs-lookup"><span data-stu-id="de4aa-128">**About Type 2 Online Stores**</span></span>](about-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="de4aa-129">**Buycd-Element**</span><span class="sxs-lookup"><span data-stu-id="de4aa-129">**BuyCD Element**</span></span>](buycd-element.md)
</dt> </dl>

 

 




