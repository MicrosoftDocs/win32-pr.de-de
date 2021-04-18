---
title: Informationen zu Typ 1 Online Stores
description: Informationen zu Typ 1 Online Stores
ms.assetid: 754b0097-5d28-4c1f-9847-a19cf23beaea
keywords:
- Windows Media Player Online Stores, geben Sie 1 Online Stores ein.
- Online Stores, Typ 1 Online Stores
- Geben Sie 1 Online Stores ein, Informationen zu
- Windows Media Player, geben Sie 1 Online Stores ein.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10ecd939a03734fed121dcaa22c0d7ae89127476
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106341506"
---
# <a name="about-type-1-online-stores"></a><span data-ttu-id="b0602-107">Informationen zu Typ 1 Online Stores</span><span class="sxs-lookup"><span data-stu-id="b0602-107">About Type 1 Online Stores</span></span>

> [!Note]  
> <span data-ttu-id="b0602-108">In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores</span><span class="sxs-lookup"><span data-stu-id="b0602-108">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="b0602-109">Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b0602-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="b0602-110">Microsoft Windows Media Player 11 unterstützt zwei Arten von Online Stores: Typ 1 und Typ 2.</span><span class="sxs-lookup"><span data-stu-id="b0602-110">Microsoft Windows Media Player 11 supports two kinds of online stores: type 1 and type 2.</span></span> <span data-ttu-id="b0602-111">Die Speicher vom Typ 1 sind tiefer in Windows Media Player als die Speicher vom Typ 2 integriert.</span><span class="sxs-lookup"><span data-stu-id="b0602-111">Type 1 stores are more deeply integrated into Windows Media Player than type 2 stores.</span></span> <span data-ttu-id="b0602-112">Ein Online Store vom Typ 1 stellt einen herunterladbaren Musikkatalog bereit, damit Windows Media Player dem Benutzer den Inhalt des Stores zur Verfügung stellen kann, als ob der Inhalt in der lokalen Medienbibliothek des Benutzers enthalten wäre.</span><span class="sxs-lookup"><span data-stu-id="b0602-112">A type 1 online store provides a downloadable music catalog so that Windows Media Player can make the store's content available to the user as if the content were in the user's local media library.</span></span>

<span data-ttu-id="b0602-113">Ein Onlinespeicher vom Typ 1 muss ein Plug-in bereitstellen, das die [iwmpcontentpartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) -Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="b0602-113">A type 1 online store must provide a plug-in that implements the [IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) interface.</span></span> <span data-ttu-id="b0602-114">Wenn der Benutzer in der Windows Media Player-Benutzeroberfläche navigiert, ruft der Player das Plug-in auf, damit der Online Shop die Benutzerfreundlichkeit durch Bereitstellen von Webseiten verbessern kann, die im Player angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="b0602-114">As the user navigates in the Windows Media Player user interface, the Player calls the plug-in so that the online store can enhance the user's experience by providing webpages that are displayed in the Player.</span></span>

<span data-ttu-id="b0602-115">Zu den Features vom Typ 1 Online Stores, die Sie von den Geschäften vom Typ 2 unterscheiden, gehören die folgenden:</span><span class="sxs-lookup"><span data-stu-id="b0602-115">Features of type 1 online stores that distinguish them from type 2 stores include the following:</span></span>

-   <span data-ttu-id="b0602-116">**Einfache Verwendung.**</span><span class="sxs-lookup"><span data-stu-id="b0602-116">**Ease of use.**</span></span> <span data-ttu-id="b0602-117">Benutzer können mit der gleichen, vertrauten Windows Media Player-Benutzeroberfläche, die Sie zurzeit zum Verwalten Ihrer persönlichen Bibliothek verwenden, nach Musik aus dem Online Store-Katalog suchen.</span><span class="sxs-lookup"><span data-stu-id="b0602-117">Users can browse for music from the online store catalog using the same, familiar Windows Media Player user interface that they currently use to manage their personal library.</span></span> <span data-ttu-id="b0602-118">Benutzer können zu einem bestimmten Zeitpunkt nur einen einzelnen Online Store-Katalog in der Funktion zum Durchsuchen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="b0602-118">Users can view only a single online store catalog in the Browse feature at any particular time.</span></span>
-   <span data-ttu-id="b0602-119">**Komforts.**</span><span class="sxs-lookup"><span data-stu-id="b0602-119">**Convenience.**</span></span> <span data-ttu-id="b0602-120">Benutzer können eine Stichprobe oder eine Musik erwerben, ohne von der Funktion zum Durchsuchen auf einen anderen Teil der Windows Media Player-Benutzeroberfläche zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="b0602-120">Users can sample or purchase music without switching from the Browse feature to another part of the Windows Media Player user interface.</span></span>
-   <span data-ttu-id="b0602-121">**Umfassende Features.**</span><span class="sxs-lookup"><span data-stu-id="b0602-121">**Rich features.**</span></span> <span data-ttu-id="b0602-122">Da der Online Store-Katalog ähnlich wie die Bibliothek des Benutzers gespeichert ist, können viele der Features der Windows Media Player-Bibliothek auf den Katalog angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="b0602-122">Because the online store catalog is stored in a fashion similar to the user's library, many of the Windows Media Player library features can be applied to the catalog.</span></span> <span data-ttu-id="b0602-123">Benutzer können z. b. das Word-Rad der Funktion zum Durchsuchen verwenden, um den Online Store-Katalog zu filtern.</span><span class="sxs-lookup"><span data-stu-id="b0602-123">For example, users can use the Browse feature's word wheel to filter the online store catalog.</span></span>

<span data-ttu-id="b0602-124">Bei einem Online Store-Anbieter haben die Vorteile der Bereitstellung eines Typs vom Typ 1 anstelle eines Typs 2 den folgenden Wert:</span><span class="sxs-lookup"><span data-stu-id="b0602-124">For an online store provider, the advantages of providing a type 1 store rather than a type 2 store include the following:</span></span>

-   <span data-ttu-id="b0602-125">Ein stark sichtbarer benutzerdefinierter Knoten in der Windows Media Player-Bibliotheksstruktur.</span><span class="sxs-lookup"><span data-stu-id="b0602-125">A highly visible custom node in the Windows Media Player library tree.</span></span>
-   <span data-ttu-id="b0602-126">Ein System, das für den Erwerb von Musik konzipiert ist.</span><span class="sxs-lookup"><span data-stu-id="b0602-126">A system designed for music purchases.</span></span>
-   <span data-ttu-id="b0602-127">Verbesserte Verbindungen mit Player-Prozessen.</span><span class="sxs-lookup"><span data-stu-id="b0602-127">Improved connections to Player processes.</span></span>
-   <span data-ttu-id="b0602-128">Ein besserer, einfacher zu verwendenden Download-Manager.</span><span class="sxs-lookup"><span data-stu-id="b0602-128">A better, easier-to-use download manager.</span></span>
-   <span data-ttu-id="b0602-129">Die Möglichkeit, zwischen verschiedenen Features im Player zu navigieren (einschließlich des Öffnens bestimmter Bibliotheksstruktur Knoten).</span><span class="sxs-lookup"><span data-stu-id="b0602-129">The ability to navigate between various features in the Player (including opening specific library tree nodes).</span></span>
-   <span data-ttu-id="b0602-130">Benachrichtigungen über den Ablauf der Lizenz für Abonnement Inhalte.</span><span class="sxs-lookup"><span data-stu-id="b0602-130">Notifications about license expiration for subscription content.</span></span>
-   <span data-ttu-id="b0602-131">Benachrichtigungen zum Arbeiten mit verbundenen portablen Musik Playern.</span><span class="sxs-lookup"><span data-stu-id="b0602-131">Notifications for working with connected portable music players.</span></span>

<span data-ttu-id="b0602-132">In den folgenden Abschnitten finden Sie eine Übersicht über den Typ 1 Online Stores.</span><span class="sxs-lookup"><span data-stu-id="b0602-132">The following sections provide overview information about type 1 online stores.</span></span>



| <span data-ttu-id="b0602-133">`Section`</span><span class="sxs-lookup"><span data-stu-id="b0602-133">Section</span></span>                                                                                              | <span data-ttu-id="b0602-134">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b0602-134">Description</span></span>                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b0602-135">Musikkatalog</span><span class="sxs-lookup"><span data-stu-id="b0602-135">Music Catalog</span></span>](music-catalog.md)                                                                   | <span data-ttu-id="b0602-136">Beschreibt den Musikkatalog, der vom Online Shop bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="b0602-136">Describes the music catalog provided by the online store.</span></span> <span data-ttu-id="b0602-137">Beschreibt den von Microsoft bereitgestellten Katalog Compiler.</span><span class="sxs-lookup"><span data-stu-id="b0602-137">Describes the catalog compiler provided by Microsoft.</span></span>                                                                     |
| [<span data-ttu-id="b0602-138">Inhalts Container</span><span class="sxs-lookup"><span data-stu-id="b0602-138">Content Containers</span></span>](content-containers.md)                                                         | <span data-ttu-id="b0602-139">Beschreibt die Content Container Interface ([iwmpcontentcontainer](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainer)), die zum Darstellen einer Auflistung von zu erwerbenden oder herunter zuladenden Medienobjekten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b0602-139">Describes the content container interface ([IWMPContentContainer](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainer)), which is used to represent a collection of media items to be purchased or downloaded.</span></span> |
| [<span data-ttu-id="b0602-140">Bibliotheks Integration</span><span class="sxs-lookup"><span data-stu-id="b0602-140">Library Integration</span></span>](library-integration.md)                                                       | <span data-ttu-id="b0602-141">Beschreibt, wie der Musikkatalog des Online Stores in die Bibliotheks Ansicht des Players integriert ist.</span><span class="sxs-lookup"><span data-stu-id="b0602-141">Describes how the online store's music catalog is integrated into the Player's library view.</span></span>                                                                                        |
| [<span data-ttu-id="b0602-142">Ermittlungs Seiten</span><span class="sxs-lookup"><span data-stu-id="b0602-142">Discovery Pages</span></span>](discovery-pages.md)                                                               | <span data-ttu-id="b0602-143">Beschreibt die Interaktion zwischen Windows Media Player und Webseiten, die vom Online Store bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="b0602-143">Describes the interaction between Windows Media Player and webpages provided by the online store.</span></span>                                                                                   |
| [<span data-ttu-id="b0602-144">Kontextmenüs</span><span class="sxs-lookup"><span data-stu-id="b0602-144">Context Menus</span></span>](context-menus.md)                                                                   | <span data-ttu-id="b0602-145">Beschreibt, wie der Online Shop Kontextmenüs bereitstellen kann, während der Benutzer die Benutzeroberfläche des Players navigiert.</span><span class="sxs-lookup"><span data-stu-id="b0602-145">Describes how the online store can provide context menus as the user navigates the Player's user interface.</span></span>                                                                         |
| [<span data-ttu-id="b0602-146">Audiodatenströme</span><span class="sxs-lookup"><span data-stu-id="b0602-146">Audio Streams</span></span>](audio-streams.md)                                                                   | <span data-ttu-id="b0602-147">Beschreibt, wie der Online Shop Windows Media Player mit der URL für das Streamen von Audioinhalten bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="b0602-147">Describes how the online store provides Windows Media Player with the URL for streaming audio content.</span></span>                                                                              |
| [<span data-ttu-id="b0602-148">ServiceInfo-Dokument für einen Typ-1-Online Store</span><span class="sxs-lookup"><span data-stu-id="b0602-148">ServiceInfo Document for a Type 1 Online Store</span></span>](serviceinfo-document-for-a-type-1-online-store.md) | <span data-ttu-id="b0602-149">Beschreibt das serviceInfo-XML-Dokument, das von einem Online Store vom Typ 1 bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="b0602-149">Describes the ServiceInfo XML document provided by a type 1 online store.</span></span>                                                                                                           |
| [<span data-ttu-id="b0602-150">Typ 1 Online Store-Plug-in</span><span class="sxs-lookup"><span data-stu-id="b0602-150">Type 1 Online Store Plug-in</span></span>](type-1-online-store-plug-in.md)                                       | <span data-ttu-id="b0602-151">Beschreibt das Plug-in, das von einem Online Store vom Typ 1 bereitgestellt werden muss.</span><span class="sxs-lookup"><span data-stu-id="b0602-151">Describes the plug-in that a type 1 online store must provide.</span></span>                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="b0602-152">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b0602-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0602-153">**Typ 1 Online Stores**</span><span class="sxs-lookup"><span data-stu-id="b0602-153">**Type 1 Online Stores**</span></span>](type-1-online-stores.md)
</dt> </dl>

 

 




