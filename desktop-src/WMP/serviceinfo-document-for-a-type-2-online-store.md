---
title: ServiceInfo-Dokument für einen Typ 2-Online Store
description: ServiceInfo-Dokument für einen Typ 2-Online Store
ms.assetid: ca83e9bf-c7fb-4212-8fa2-1fae11ed26e9
keywords:
- Windows Media Player Online Stores, serviceingefo-Dokument
- Online Stores, serviceingefo-Dokument
- Typ 2 Online Stores, serviceInfo-Dokument
- Servicinfo-Dokument
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fb558661332ab08edd2057fa024a1a0e2034b9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037107"
---
# <a name="serviceinfo-document-for-a-type-2-online-store"></a><span data-ttu-id="4db26-107">ServiceInfo-Dokument für einen Typ 2-Online Store</span><span class="sxs-lookup"><span data-stu-id="4db26-107">ServiceInfo Document for a Type 2 Online Store</span></span>

<span data-ttu-id="4db26-108">Typ 2 Online Store-Anbieter müssen Microsoft die URL eines XML-Dokuments bereitstellen, das den Online Shop beschreibt.</span><span class="sxs-lookup"><span data-stu-id="4db26-108">Type 2 online store providers must provide Microsoft with the URL of an XML document that describes the online store.</span></span> <span data-ttu-id="4db26-109">Windows Media Player 10 und Windows Media Player 11 verwenden Sie dieses Dokument, um zu bestimmen, wie die Benutzeroberfläche zum Hosten des Online Stores konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="4db26-109">Windows Media Player 10 and Windows Media Player 11 use this document to determine how to configure the user interface to host the online store.</span></span>

<span data-ttu-id="4db26-110">In Windows Media Player 10 bietet das servicinput Info-Dokument Folgendes:</span><span class="sxs-lookup"><span data-stu-id="4db26-110">In Windows Media Player 10, the ServiceInfo document provides the following:</span></span>

-   <span data-ttu-id="4db26-111">Informationen zum Konfigurieren der Aufgabenbereiche, die von Windows Media Player angezeigt werden, wenn der Online Store aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="4db26-111">Information about how to configure the task panes that Windows Media Player displays when the online store is active.</span></span> <span data-ttu-id="4db26-112">Ein Online Store kann über einen, zwei oder drei Aufgabenbereiche verfügen.</span><span class="sxs-lookup"><span data-stu-id="4db26-112">An online store can have one, two, or three task panes.</span></span>
-   <span data-ttu-id="4db26-113">Informationen, die zum Konfigurieren der Aufgabenbereichs Schaltflächen verwendet werden, z. b. der Schaltflächen Text, die Schaltflächen Farbe und Quick Infos für die Schaltflächen.</span><span class="sxs-lookup"><span data-stu-id="4db26-113">Information used to configure the task pane buttons, such as the button text, the button color, and tool tips for the buttons.</span></span>
-   <span data-ttu-id="4db26-114">URLs für Images, die von Windows Media Player angezeigt werden, um den Online Store zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="4db26-114">URLs for images that Windows Media Player displays to identify the online store.</span></span>
-   <span data-ttu-id="4db26-115">URLs von Webseiten, die vom Online Store bereitgestellt werden, die von Windows Media Player in der Benutzeroberfläche gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="4db26-115">URLs of webpages, provided by the online store, that Windows Media Player hosts in its user interface.</span></span>
-   <span data-ttu-id="4db26-116">Informationen dazu, wie das Windows Media Player-Setup den ersten Online Store konfigurieren soll, den der Benutzer sieht.</span><span class="sxs-lookup"><span data-stu-id="4db26-116">Information about how Windows Media Player setup should configure the first online store the user sees.</span></span>

<span data-ttu-id="4db26-117">In Windows Media Player 11 bietet das servicinput Info-Dokument Folgendes:</span><span class="sxs-lookup"><span data-stu-id="4db26-117">In Windows Media Player 11, the ServiceInfo document provides the following:</span></span>

-   <span data-ttu-id="4db26-118">Informationen, die verwendet werden, um die Schaltfläche für die Registerkarte "Online Stores" zu konfigurieren, z. b. den Schaltflächen Text und die QuickInfo</span><span class="sxs-lookup"><span data-stu-id="4db26-118">Information used to configure the button for Online Stores tab, such as the button text and the tool tip for the button.</span></span>
-   <span data-ttu-id="4db26-119">URLs für Images, die von Windows Media Player angezeigt werden, um den Online Store zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="4db26-119">URLs for images that Windows Media Player displays to identify the online store.</span></span>
-   <span data-ttu-id="4db26-120">URLs von Webseiten, die vom Online Store bereitgestellt werden, die von Windows Media Player in der Benutzeroberfläche gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="4db26-120">URLs of webpages, provided by the online store, that Windows Media Player hosts in its user interface.</span></span>

<span data-ttu-id="4db26-121">Wenn Sie mit der Entwicklung Ihres Online Stores beginnen, müssen Sie Microsoft die URL Ihres serviceInfo-Dokuments bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="4db26-121">When you start developing your online store, you must provide Microsoft with the URL to your ServiceInfo document.</span></span> <span data-ttu-id="4db26-122">Während der Entwicklungsphase wird der Online Shop in Windows Media Player nur angezeigt, wenn ein spezieller Registrierungsschlüssel festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="4db26-122">During the development phase, your online store will appear in Windows Media Player only when a special registry key is set.</span></span>

<span data-ttu-id="4db26-123">Nach der Veröffentlichung des Online Stores ist das Szenario, in dem Windows Media Player das serviceInfo-Dokument automatisch aus dem Internet abruft.</span><span class="sxs-lookup"><span data-stu-id="4db26-123">After your online store is published, the ususal scenario is that Windows Media Player retrieves your ServiceInfo document from the Web automatically.</span></span> <span data-ttu-id="4db26-124">In einigen Fällen ruft Windows Media Player jedoch das serviceInfo-Dokument vom Computer des Benutzers ab.</span><span class="sxs-lookup"><span data-stu-id="4db26-124">In some cases, however, Windows Media Player retrieves the ServiceInfo document from the user's computer.</span></span> <span data-ttu-id="4db26-125">Weitere Informationen finden Sie unter [Festlegen des ersten Online Stores](setting-the-initial-online-store.md).</span><span class="sxs-lookup"><span data-stu-id="4db26-125">For more information, see [Setting the Initial Online Store](setting-the-initial-online-store.md).</span></span>

<span data-ttu-id="4db26-126">Wenn Windows Media Player das servicanfo-Dokument aus dem Web abruft, fügt es eine Abfrage Zeichenfolge an die URL an.</span><span class="sxs-lookup"><span data-stu-id="4db26-126">When Windows Media Player retrieves the ServiceInfo document from the Web, it appends a query string to the URL.</span></span> <span data-ttu-id="4db26-127">Die Abfrage Zeichenfolge enthält Parameter, die Informationen über das Gebiets Schema des Benutzers und die Windows-Media Player Version bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="4db26-127">The query string contains parameters that provide information about the user's locale and the Windows Media Player version.</span></span>

<span data-ttu-id="4db26-128">Sie können statische oder dynamische serviceingefo-Dokumente erstellen.</span><span class="sxs-lookup"><span data-stu-id="4db26-128">You can create static or dynamic ServiceInfo documents.</span></span> <span data-ttu-id="4db26-129">Ein statisches serviceInfo-Dokument verfügt über die Dateinamenerweiterung. Xml.</span><span class="sxs-lookup"><span data-stu-id="4db26-129">A static ServiceInfo document has an .xml file name extension.</span></span> <span data-ttu-id="4db26-130">Ein dynamisches serviceInfo-Dokument ist eine ASP-Seite mit der Dateinamenerweiterung ". asp" oder ". aspx".</span><span class="sxs-lookup"><span data-stu-id="4db26-130">A dynamic ServiceInfo document is an ASP page and has an .asp or .aspx file name extension.</span></span>

<span data-ttu-id="4db26-131">Nicht alle Elemente, die für die Verwendung im serviceInfo-Dokument verfügbar sind, können von jedem Online Store verwendet werden, und einige Elemente sind für alle Online Stores optional.</span><span class="sxs-lookup"><span data-stu-id="4db26-131">Not all the elements available for use in the ServiceInfo document can be used by every online store, and some elements are optional for all online stores.</span></span> <span data-ttu-id="4db26-132">Informationen zu den von Ihnen erstellten online speichern und den verfügbaren Funktionen für die einzelnen Typen finden Sie unter [Windows Media Player Online Stores](windows-media-player-online-stores.md).</span><span class="sxs-lookup"><span data-stu-id="4db26-132">For information about the types of online stores you can create and the features available for each type, see [Windows Media Player Online Stores](windows-media-player-online-stores.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4db26-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4db26-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4db26-134">**Informationen zu Typ 2 Online Stores**</span><span class="sxs-lookup"><span data-stu-id="4db26-134">**About Type 2 Online Stores**</span></span>](about-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="4db26-135">**Dynamisches Erstellen des serviceingefo-Dokuments**</span><span class="sxs-lookup"><span data-stu-id="4db26-135">**Creating the ServiceInfo Document Dynamically**</span></span>](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[<span data-ttu-id="4db26-136">**Beispiel eines serviceInfo-Dokuments für einen Typ 2-Online Store**</span><span class="sxs-lookup"><span data-stu-id="4db26-136">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="4db26-137">**Servicinfo-Dokument**</span><span class="sxs-lookup"><span data-stu-id="4db26-137">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 




