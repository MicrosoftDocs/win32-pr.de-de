---
title: Client-Side Design
description: Skripts in serverseitigen HTML-Seiten kommunizieren mit dem Online-druckstellungs-Assistenten, in dem Sie gehostet werden. Diese Kommunikation erfolgt über Methoden und Eigenschaften, auf die das Window. extern-Objekt zugreift.
ms.assetid: fa76ccee-0b94-41b5-8cc8-eb7e1818dbed
keywords:
- Veröffentlichungs-Assistenten, Client seitiger Entwurf
- Window. extern, Veröffentlichungs-Assistenten
- Veröffentlichungs-Assistenten, Window. extern
- Veröffentlichungs-Assistenten, Entwurfs Überlegungen
- Veröffentlichungs-Assistenten, Assistent für Online-Druck Bestellungen
- Online-druckstellungs-Assistent, Client seitiger Entwurf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f92f794ee5f576077e0523f9a21101205ec789d4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948717"
---
# <a name="client-side-design"></a><span data-ttu-id="c2da8-110">Client-Side Design</span><span class="sxs-lookup"><span data-stu-id="c2da8-110">Client-Side Design</span></span>

<span data-ttu-id="c2da8-111">Skripts in serverseitigen HTML-Seiten kommunizieren mit dem Online-druckstellungs-Assistenten, in dem Sie gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="c2da8-111">Script in server-side HTML pages communicates with the Online Print Ordering Wizard client in which it is hosted.</span></span> <span data-ttu-id="c2da8-112">Diese Kommunikation erfolgt über Methoden und Eigenschaften, auf die das **Window. extern** -Objekt zugreift.</span><span class="sxs-lookup"><span data-stu-id="c2da8-112">This communication is accomplished through methods and properties accessed by the **window.external** object.</span></span>

<span data-ttu-id="c2da8-113">In diesem Dokument werden die folgenden Themen behandelt.</span><span class="sxs-lookup"><span data-stu-id="c2da8-113">The following topics are covered in this document.</span></span>

-   [<span data-ttu-id="c2da8-114">Methoden und Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c2da8-114">Methods and Properties</span></span>](#methods-and-properties)
-   [<span data-ttu-id="c2da8-115">Entwurfsaspekte</span><span class="sxs-lookup"><span data-stu-id="c2da8-115">Design Considerations</span></span>](#design-considerations)
-   [<span data-ttu-id="c2da8-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c2da8-116">Related topics</span></span>](#related-topics)

## <a name="methods-and-properties"></a><span data-ttu-id="c2da8-117">Methoden und Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c2da8-117">Methods and Properties</span></span>

<span data-ttu-id="c2da8-118">Die folgenden Methoden und Eigenschaften sind über das **Window. extern** -Objekt verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c2da8-118">The following methods and properties are available through the **window.external** object.</span></span>

-   [<span data-ttu-id="c2da8-119">**Finalback**</span><span class="sxs-lookup"><span data-stu-id="c2da8-119">**FinalBack**</span></span>](/windows/desktop/shell/iwebwizardhost-finalback)
-   [<span data-ttu-id="c2da8-120">**Finalnext**</span><span class="sxs-lookup"><span data-stu-id="c2da8-120">**FinalNext**</span></span>](/windows/desktop/shell/iwebwizardhost-finalnext)
-   [<span data-ttu-id="c2da8-121">**Abbrechen**</span><span class="sxs-lookup"><span data-stu-id="c2da8-121">**Cancel**</span></span>](/windows/desktop/shell/iwebwizardhost-cancel)
-   [<span data-ttu-id="c2da8-122">**Passport Authenticate**</span><span class="sxs-lookup"><span data-stu-id="c2da8-122">**PassportAuthenticate**</span></span>](/windows/desktop/shell/inewwdevents-passportauthenticate)
-   [<span data-ttu-id="c2da8-123">**"Abadertext"**</span><span class="sxs-lookup"><span data-stu-id="c2da8-123">**SetHeaderText**</span></span>](/windows/desktop/shell/iwebwizardhost-setheadertext)
-   [<span data-ttu-id="c2da8-124">**""-Schaltflächen**</span><span class="sxs-lookup"><span data-stu-id="c2da8-124">**SetWizardButtons**</span></span>](/windows/desktop/shell/iwebwizardhost-setwizardbuttons)
-   <span data-ttu-id="c2da8-125">[**Caption**](/previous-versions/windows/desktop/legacy/bb774352(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c2da8-125">[**Caption**](/previous-versions/windows/desktop/legacy/bb774352(v=vs.85))</span></span>
-   [<span data-ttu-id="c2da8-126">**Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="c2da8-126">**Property**</span></span>](/windows/desktop/shell/iwebwizardhost-property)

<span data-ttu-id="c2da8-127">Das Skript der serverseitigen Seite ruft diese Methoden auf, um den Client über Ereignisse während der Veröffentlichungs Prozedur zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="c2da8-127">The server-side page's script calls these methods to notify the client of events during the publishing procedure.</span></span> <span data-ttu-id="c2da8-128">Betrachten wir als Beispiel den [**finalback**](/windows/desktop/shell/iwebwizardhost-finalback) .</span><span class="sxs-lookup"><span data-stu-id="c2da8-128">Let's look at [**FinalBack**](/windows/desktop/shell/iwebwizardhost-finalback) as an example.</span></span> <span data-ttu-id="c2da8-129">Wenn der Assistent die erste serverseitige HTML-Seite anzeigt, ist er so bewaffnet, dass er die Handles für die Seiten des Assistenten vor und nach den gehosteten HTML-Seiten kennt.</span><span class="sxs-lookup"><span data-stu-id="c2da8-129">When the wizard displays the first server-side HTML page, it does so armed with knowledge of the handles for the wizard pages preceding and following the hosted HTML pages.</span></span> <span data-ttu-id="c2da8-130">An diesem Punkt in unserem Beispiel klickt der Benutzer, der sich auf der ersten HTML-Seite befindet, auf die Schaltfläche " **zurück** ".</span><span class="sxs-lookup"><span data-stu-id="c2da8-130">At this point in our example, the user, sitting at that first HTML page, clicks the **Back** button.</span></span> <span data-ttu-id="c2da8-131">Der Assistent sendet eine Benachrichtigung dieses Ereignisses an den Server.</span><span class="sxs-lookup"><span data-stu-id="c2da8-131">The wizard sends a notification of this event to the server.</span></span> <span data-ttu-id="c2da8-132">Beim Empfang dieser Nachricht bezieht sich das serverseitige Skript auf seinen **onback** -Handler für dieses Ereignis, das, da dies die erste HTML-Seite ist, die **Final Back** -Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="c2da8-132">On receipt of this message, the server-side script refers to its **OnBack** handler for this event, which, as this is the first HTML page, calls the **FinalBack** method.</span></span> <span data-ttu-id="c2da8-133">Dadurch wechselt der Assistent zur Seite des Assistenten, der vor der Eingabe der serverseitigen Benutzeroberfläche angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="c2da8-133">This causes the wizard to navigate to the wizard page displayed before entering the server-side UI.</span></span>

<span data-ttu-id="c2da8-134">Eine ausführliche Erläuterung dieser Methoden und Eigenschaften finden Sie in der Dokumentation zu den Objekten [**webwizardhost**](/windows/desktop/shell/webwizardhost) und [**newwdevents**](/windows/desktop/shell/newwdevents) .</span><span class="sxs-lookup"><span data-stu-id="c2da8-134">For a complete discussion of these methods and properties, see the documentation for the [**WebWizardHost**](/windows/desktop/shell/webwizardhost) and [**NewWDEvents**](/windows/desktop/shell/newwdevents) objects.</span></span>

## <a name="design-considerations"></a><span data-ttu-id="c2da8-135">Entwurfsaspekte</span><span class="sxs-lookup"><span data-stu-id="c2da8-135">Design Considerations</span></span>

<span data-ttu-id="c2da8-136">Der HTML-Code für jede serverseitige Seite wird normalerweise im Assistenten Bereich angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c2da8-136">HTML making up each server-side page is displayed normally in the wizard pane.</span></span> <span data-ttu-id="c2da8-137">Beachten Sie beim Entwerfen dieser Seiten, dass die Größe eines Assistenten Fensters nicht geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="c2da8-137">When designing these pages, bear in mind that a wizard window cannot be resized.</span></span> <span data-ttu-id="c2da8-138">Daher sollten Seiten so erstellt und vergrößert werden, dass Scrollleisten nach Möglichkeit vermieden werden, um dem Benutzer eine reibungslose Navigation durch den Assistenten zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="c2da8-138">Pages should therefore be constructed and sized so that scroll bars are avoided whenever possible to provide the user with smooth navigation through the wizard.</span></span>

<span data-ttu-id="c2da8-139">Jede HTML-Seite muss auch einen Handler für **onback**-, **OnNext**-und **OnCancel** -Ereignisse bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c2da8-139">Each HTML page must also provide a handler for **OnBack**, **OnNext**, and **OnCancel** events.</span></span> <span data-ttu-id="c2da8-140">Der **OnNext** -Handler behandelt außerdem das **Abschluss** Ereignis.</span><span class="sxs-lookup"><span data-stu-id="c2da8-140">The **OnNext** handler will also handle the **Finish** event.</span></span> <span data-ttu-id="c2da8-141">Eine Seite, die keine **onback** -Funktion implementiert, wird als ungültig betrachtet und bewirkt, dass eine Fehlerseite angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="c2da8-141">A page that does not implement an **OnBack** function is considered invalid and will cause an error page to be displayed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c2da8-142">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c2da8-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2da8-143">**Webwizardhost**</span><span class="sxs-lookup"><span data-stu-id="c2da8-143">**WebWizardHost**</span></span>](/windows/desktop/shell/webwizardhost)
</dt> <dt>

[<span data-ttu-id="c2da8-144">**Newwentvents**</span><span class="sxs-lookup"><span data-stu-id="c2da8-144">**NewWDEvents**</span></span>](/windows/desktop/shell/newwdevents)
</dt> <dt>

[<span data-ttu-id="c2da8-145">Server seitiges Design</span><span class="sxs-lookup"><span data-stu-id="c2da8-145">Server-Side Design</span></span>](pubwiz-server.md)
</dt> </dl>

 

 