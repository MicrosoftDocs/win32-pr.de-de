---
title: Aufgabenbereiche für Dienste
description: Aufgabenbereiche für Dienste
ms.assetid: f626fa85-7590-4e87-bd5c-7ffdcb14be8b
keywords:
- Windows Media Player Online Stores, Aufgabenbereiche für Dienste
- Online Stores, Aufgabenbereiche für Dienste
- Typ 2 Online Stores, Dienstaufgaben Bereiche
- Windows Media Player Online Stores, Aufgabenbereiche
- Online Stores, Aufgabenbereiche
- Typ 2 Online Stores, Aufgabenbereiche
- Aufgabenbereiche für Windows Media Player, Dienste
- Windows Media Player, Aufgabenbereiche
- Aufgabenbereiche für Dienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4f882e46a7252792db5b551b25869c7711f9d31
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037108"
---
# <a name="service-task-panes"></a><span data-ttu-id="d9565-112">Aufgabenbereiche für Dienste</span><span class="sxs-lookup"><span data-stu-id="d9565-112">Service Task Panes</span></span>

<span data-ttu-id="d9565-113">In Windows Media Player 10 können Online Store-Anbieter Windows Media Player so konfigurieren, dass so viele als drei Aufgabenbereiche angezeigt werden, die als Dienstaufgaben Bereiche bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="d9565-113">In Windows Media Player 10, online store providers can configure Windows Media Player to display as many as three task panes, called service task panes.</span></span> <span data-ttu-id="d9565-114">Jeder Dienstaufgaben Bereich wird durch eine anpassbare Schaltfläche dargestellt, die von Windows Media Player auf der rechten Seite der Features-Taskleiste angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d9565-114">Each service task pane is represented by a customizable button that Windows Media Player displays on the right side of the Features taskbar.</span></span>

<span data-ttu-id="d9565-115">Jeder Dienstaufgaben Bereich hostet eine Webseite, bei der es sich um die Benutzeroberfläche für eine bestimmte Online Store-Funktion handelt. Das Erscheinungsbild der Dienstaufgaben Bereiche wird durch das servicinput FO-XML-Dokument definiert.</span><span class="sxs-lookup"><span data-stu-id="d9565-115">Each service task pane hosts a webpage that is the user interface for a particular online store feature.The appearance of the service task panes is defined by the ServiceInfo XML document.</span></span> <span data-ttu-id="d9565-116">In diesem Dokument werden die Dienstaufgaben Bereiche durch drei Elemente dargestellt: **ServiceTask1**, **ServiceTask2** und **ServiceTask3**.</span><span class="sxs-lookup"><span data-stu-id="d9565-116">In this document, the service task panes are represented by three elements: **ServiceTask1**, **ServiceTask2**, and **ServiceTask3**.</span></span> <span data-ttu-id="d9565-117">Diese Dienstaufgaben Bereiche sollen Folgendes bereitstellen:</span><span class="sxs-lookup"><span data-stu-id="d9565-117">These service task panes are intended to provide the following:</span></span>

-   <span data-ttu-id="d9565-118">Ein Musikdienst.</span><span class="sxs-lookup"><span data-stu-id="d9565-118">A music service.</span></span>
-   <span data-ttu-id="d9565-119">Ein Videodienst.</span><span class="sxs-lookup"><span data-stu-id="d9565-119">A video service.</span></span>
-   <span data-ttu-id="d9565-120">Ein Radiodienst.</span><span class="sxs-lookup"><span data-stu-id="d9565-120">A radio service.</span></span>

<span data-ttu-id="d9565-121">Sie können diese Features in einer beliebigen Reihenfolge in Windows Media Player positionieren, aber **ServiceTask1** muss der primäre Aufgabenbereich sein, damit Sie an der kommerziellen Aktivität beteiligt sind.</span><span class="sxs-lookup"><span data-stu-id="d9565-121">You can position these features in Windows Media Player in any order you like, but **ServiceTask1** must be the primary task pane for engaging in commercial activity.</span></span>

<span data-ttu-id="d9565-122">Die in jedem Dienstaufgaben Bereich gehostete Webseite hat Zugriff auf das **externe** Objekt.</span><span class="sxs-lookup"><span data-stu-id="d9565-122">The webpage hosted in each service task pane has access to the **External** object.</span></span> <span data-ttu-id="d9565-123">Dieses Objekt stellt Methoden, Eigenschaften und ein Ereignis bereit, die spezielle Funktionen für Webseiten in Windows Media Player bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="d9565-123">This object provides methods, properties, and an event that provide special functionality for webpages in Windows Media Player.</span></span> <span data-ttu-id="d9565-124">Beispielsweise können Sie das-Ereignis und die-Eigenschaften von **extern** verwenden, damit die Darstellung der Webseite dem Farbschema entspricht, das der Benutzer für Windows Media Player ausgewählt hat.</span><span class="sxs-lookup"><span data-stu-id="d9565-124">For instance, you can use the event and properties from **External** to make the appearance of your webpage match the color scheme that the user has chosen for Windows Media Player.</span></span>

<span data-ttu-id="d9565-125">In Windows Media Player 11 sind keine Dienstaufgaben Bereiche vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d9565-125">In Windows Media Player 11, there are no service task panes.</span></span> <span data-ttu-id="d9565-126">Stattdessen gibt es eine einzelne Registerkarte " **Online Stores** ", die die Hauptwebseite für den aktiven Online Store hostet.</span><span class="sxs-lookup"><span data-stu-id="d9565-126">Instead, there is a single **Online Stores** tab, which hosts the main webpage for the active online store.</span></span> <span data-ttu-id="d9565-127">Im serviceingefo-Dokument wird die Registerkarte " **Online Stores** " durch das **ServiceTask1** -Element dargestellt. die **ServiceTask2** -und **ServiceTask3** -Elemente werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="d9565-127">In the ServiceInfo document, the **Online Stores** tab is represented by the **ServiceTask1** element; the **ServiceTask2** and **ServiceTask3** elements are ignored.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d9565-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d9565-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9565-129">**Informationen zu Typ 2 Online Stores**</span><span class="sxs-lookup"><span data-stu-id="d9565-129">**About Type 2 Online Stores**</span></span>](about-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="d9565-130">**Externes Objekt für den Typ 2-Online Speicher**</span><span class="sxs-lookup"><span data-stu-id="d9565-130">**External Object for Type 2 Online Stores**</span></span>](external-object-for-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="d9565-131">**ServiceInfo-Dokument für einen Typ 2-Online Store**</span><span class="sxs-lookup"><span data-stu-id="d9565-131">**ServiceInfo Document for a Type 2 Online Store**</span></span>](serviceinfo-document-for-a-type-2-online-store.md)
</dt> </dl>

 

 




