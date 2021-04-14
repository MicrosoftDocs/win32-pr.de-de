---
title: Architektur (Text Dienste-Framework)
description: Architektur
ms.assetid: 6ef6ba1f-fcbb-4ede-bc6f-3da66135ea69
keywords:
- Text Services-Framework (TSF), Architektur
- TSF (Text Dienst Framework), Architektur
- Text Dienste, Architektur
- TSF-aktivierte Anwendungen, Architektur
- Text Dienst Framework (TSF), Komponenten
- TSF (Text Dienst Framework), Komponenten
- Text Dienste, Komponenten
- TSF-aktivierte Anwendungen, Komponenten
- Text Dienst Framework (TSF), Anwendungen
- TSF (Text Dienst Framework), Anwendungen
- Text Dienste, Anwendungen
- TSF-aktivierte Anwendungen, Informationen zu
- Text Dienste-Framework (TSF), Text Dienste
- TSF (Text Dienst Framework), Text Dienste
- Text Dienste, Info
- TSF-aktivierte Anwendungen, Text Dienste
- Text Services-Framework (TSF), TSF Manager
- TSF (Text Dienst Framework), TSF Manager
- Text Dienste, TSF Manager
- TSF-aktivierte Anwendungen, TSF-Manager
- TSF-Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e0a300307b3099b4a28a883d5c830c4078cd0bb
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104555922"
---
# <a name="architecture-text-services-framework"></a><span data-ttu-id="38bbc-124">Architektur (Text Dienste-Framework)</span><span class="sxs-lookup"><span data-stu-id="38bbc-124">Architecture (Text Services Framework)</span></span>

<span data-ttu-id="38bbc-125">Das Text Dienst-Framework umfasst drei Hauptkomponenten:</span><span class="sxs-lookup"><span data-stu-id="38bbc-125">Text Services Framework includes three primary components:</span></span>

-   <span data-ttu-id="38bbc-126">**Anwendungen:** Anwendungs Vorgänge umfassen in der Regel Anzeige, direkte Bearbeitung und Text Speicherung.</span><span class="sxs-lookup"><span data-stu-id="38bbc-126">**Applications:** Application operations typically include display, direct editing, and storage of text.</span></span> <span data-ttu-id="38bbc-127">Eine Anwendung ermöglicht den Zugriff auf Text durch Implementieren eines COM-Servers, der bestimmte Schnittstellen unterstützt und über Schnittstellen kommuniziert, die der TSF-Manager verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="38bbc-127">An application provides access to text by implementing a COM server that supports certain interfaces and communicates with TSF using interfaces that the TSF manager exposes.</span></span> <span data-ttu-id="38bbc-128">In dieser Dokumentation bezieht sich der Begriff "Anwendung" auf eine TSF-fähige Anwendung, sofern nicht anders angegeben.</span><span class="sxs-lookup"><span data-stu-id="38bbc-128">Throughout this documentation, the term, application, refers to a TSF-enabled application, unless otherwise specified.</span></span>
-   <span data-ttu-id="38bbc-129">**Text Dienste:** Ein Text Dienst fungiert als Text Anbieter für eine Anwendung.</span><span class="sxs-lookup"><span data-stu-id="38bbc-129">**Text Services:** A text service functions as a text provider to an application.</span></span> <span data-ttu-id="38bbc-130">Ein Text Dienst kann Text aus einer Anwendung abrufen und Text in diese schreiben.</span><span class="sxs-lookup"><span data-stu-id="38bbc-130">A text service can obtain text from, and write text to, an application.</span></span> <span data-ttu-id="38bbc-131">Ein Text Dienst kann auch Daten und Eigenschaften einem TextBlock zuordnen.</span><span class="sxs-lookup"><span data-stu-id="38bbc-131">A text service can also associate data and properties with a block of text.</span></span> <span data-ttu-id="38bbc-132">Ein Text Dienst wird als com-in-proc-Server implementiert, der sich bei TSF registriert.</span><span class="sxs-lookup"><span data-stu-id="38bbc-132">A text service is implemented as a COM in-proc server that registers itself with TSF.</span></span> <span data-ttu-id="38bbc-133">Bei der Registrierung interagiert der Benutzer mit dem Text Dienst über die sprach Leiste oder über Tastenkombinationen.</span><span class="sxs-lookup"><span data-stu-id="38bbc-133">When registered, the user interacts with the text service using the language bar or keyboard shortcuts.</span></span> <span data-ttu-id="38bbc-134">Es können mehrere Text Dienste installiert werden.</span><span class="sxs-lookup"><span data-stu-id="38bbc-134">Multiple text services can be installed.</span></span>
-   <span data-ttu-id="38bbc-135">**TSF-Manager:** Der TSF-Manager fungiert als Vermittler zwischen einer Anwendung und mindestens einem Text Dienst.</span><span class="sxs-lookup"><span data-stu-id="38bbc-135">**TSF Manager:** The TSF manager functions as a mediator between an application and one or more text services.</span></span> <span data-ttu-id="38bbc-136">Ein Text Dienst interagiert niemals direkt mit einer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="38bbc-136">A text service never interacts directly with an application.</span></span> <span data-ttu-id="38bbc-137">Die gesamte Kommunikation verläuft über den TSF-Manager.</span><span class="sxs-lookup"><span data-stu-id="38bbc-137">All communication passes through the TSF manager.</span></span> <span data-ttu-id="38bbc-138">Der TSF-Manager wird vom Betriebssystem implementiert und kann nicht ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="38bbc-138">The TSF manager is implemented by the operating system and cannot be replaced.</span></span> <span data-ttu-id="38bbc-139">In dieser Dokumentation bezieht sich der Begriff Manager auf den TSF-Manager, sofern nicht anders angegeben.</span><span class="sxs-lookup"><span data-stu-id="38bbc-139">Throughout this documentation, the term, manager, refers to the TSF manager, unless otherwise specified.</span></span>

<span data-ttu-id="38bbc-140">Die folgende Abbildung zeigt die primären Architektur Elemente von TSF.</span><span class="sxs-lookup"><span data-stu-id="38bbc-140">The following illustration shows the primary architectural elements of TSF.</span></span>

![Architektur des Frameworks für Text Dienste](images/tsf-arch.gif)

<span data-ttu-id="38bbc-142">Mit dieser Architektur stellt der TSF-Manager eine Abstraktionsschicht zwischen Anwendungen und Text Diensten bereit.</span><span class="sxs-lookup"><span data-stu-id="38bbc-142">With this architecture, the TSF manager provides an abstraction layer between applications and text services.</span></span> <span data-ttu-id="38bbc-143">Diese Abstraktions Ebene ermöglicht einer Anwendung und einem oder mehreren Text Diensten das Freigeben von Text, und der TSF-Manager kann Text Dienste verwalten.</span><span class="sxs-lookup"><span data-stu-id="38bbc-143">This abstraction layer enables an application and one or more text services to share text, and it enables the TSF manager to manage text services.</span></span>

 

 




