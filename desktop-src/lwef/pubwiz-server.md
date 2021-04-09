---
title: Server-Side Design
description: Server seitige Funktionen kommunizieren über das Windows. externe-Objekt mit dem-Client-Assistenten. Server seitiges Skript stellt diese Funktionen bereit, um auf Assistenten Ereignisse zu reagieren und Informationen zum Assistenten abzurufen.
ms.assetid: 7cc8b814-f230-4326-a9df-a491ed35483e
keywords:
- Veröffentlichungs-Assistenten, serverseitiger Entwurf
- Window. extern, Veröffentlichungs-Assistenten
- Veröffentlichungs-Assistenten, Window. extern
- Veröffentlichungs-Assistenten, Navigations Skriptfunktionen
- Skripts, Veröffentlichungs-Assistenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20b3b218bbca297be446016335d90fe717a88bba
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948747"
---
# <a name="server-side-design"></a><span data-ttu-id="b9526-109">Server-Side Design</span><span class="sxs-lookup"><span data-stu-id="b9526-109">Server-Side Design</span></span>

<span data-ttu-id="b9526-110">Server seitige Funktionen kommunizieren über das **Windows. externe** -Objekt mit dem-Client-Assistenten.</span><span class="sxs-lookup"><span data-stu-id="b9526-110">Server-side functions communicate with the client wizard through the **windows.external** object.</span></span> <span data-ttu-id="b9526-111">Server seitiges Skript stellt diese Funktionen bereit, um auf Assistenten Ereignisse zu reagieren und Informationen zum Assistenten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b9526-111">Server-side script provides these functions to respond to wizard events and to retrieve information about the wizard.</span></span>

<span data-ttu-id="b9526-112">In diesem Dokument werden die folgenden Themen behandelt.</span><span class="sxs-lookup"><span data-stu-id="b9526-112">The following topics are covered in this document.</span></span>

-   [<span data-ttu-id="b9526-113">Implementieren von Navigations Skriptfunktionen</span><span class="sxs-lookup"><span data-stu-id="b9526-113">Implementing Navigation Script Functions</span></span>](#implementing-navigation-script-functions)
    -   [<span data-ttu-id="b9526-114">Onback ()</span><span class="sxs-lookup"><span data-stu-id="b9526-114">OnBack()</span></span>](#onback)
    -   [<span data-ttu-id="b9526-115">OnNext ()</span><span class="sxs-lookup"><span data-stu-id="b9526-115">OnNext()</span></span>](#onnext)
    -   [<span data-ttu-id="b9526-116">OnCancel ()</span><span class="sxs-lookup"><span data-stu-id="b9526-116">OnCancel()</span></span>](#oncancel)
-   [<span data-ttu-id="b9526-117">Andere Methoden und Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b9526-117">Other Methods and Properties</span></span>](#other-methods-and-properties)
    -   [<span data-ttu-id="b9526-118">Methoden</span><span class="sxs-lookup"><span data-stu-id="b9526-118">Methods</span></span>](#methods)
    -   [<span data-ttu-id="b9526-119">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b9526-119">Properties</span></span>](#properties)
-   [<span data-ttu-id="b9526-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b9526-120">Related topics</span></span>](#related-topics)

## <a name="implementing-navigation-script-functions"></a><span data-ttu-id="b9526-121">Implementieren von Navigations Skriptfunktionen</span><span class="sxs-lookup"><span data-stu-id="b9526-121">Implementing Navigation Script Functions</span></span>

<span data-ttu-id="b9526-122">Server seitiges Skript in jeder HTML-Seite antwortet auf Navigations Schaltflächen durch Funktionen für **onback**, **OnNext** und **OnCancel**.</span><span class="sxs-lookup"><span data-stu-id="b9526-122">Server-side script in each HTML page responds to navigation buttons through functions for **OnBack**, **OnNext**, and **OnCancel**.</span></span> <span data-ttu-id="b9526-123">Auf diese Funktionen muss über das **IHTMLDocument:: get- \_ Skript** auf dem Client zugegriffen werden können, und es müssen keine Parameter übernommen werden.</span><span class="sxs-lookup"><span data-stu-id="b9526-123">These functions must be accessible through **IHTMLDocument::get\_Script** on the client and take no parameters.</span></span>

### <a name="onback"></a><span data-ttu-id="b9526-124">Onback ()</span><span class="sxs-lookup"><span data-stu-id="b9526-124">OnBack()</span></span>

-   <span data-ttu-id="b9526-125">Reagiert, wenn der Benutzer auf den Assistenten **zurück** klickt.</span><span class="sxs-lookup"><span data-stu-id="b9526-125">Responds when the user clicks **Back** in the wizard.</span></span>
-   <span data-ttu-id="b9526-126">Wenn die aktuelle serverseitige Seite die erste serverseitige Seite ist, rufen Sie **Window. extern. finalback** auf, um den Client anzuweisen, zur vorherigen Client seitigen Seite zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="b9526-126">If the current server-side page is the first server-side page, call **window.external.FinalBack** to instruct the client to navigate to the previous client-side page.</span></span>
-   <span data-ttu-id="b9526-127">Wenn die aktuelle serverseitige Seite nicht die erste serverseitige Seite ist, navigieren Sie zur vorherigen serverseitigen Seite.</span><span class="sxs-lookup"><span data-stu-id="b9526-127">If the current server-side page is not the first server-side page, navigate to the previous server-side page.</span></span>
-   <span data-ttu-id="b9526-128">Diese Funktion muss für jede Seite implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="b9526-128">This function must be implemented for each page.</span></span> <span data-ttu-id="b9526-129">Jede Seite, die nicht ausgeführt werden kann, wird als ungültig betrachtet und zeigt eine Fehlerseite an.</span><span class="sxs-lookup"><span data-stu-id="b9526-129">Any page that fails to do so is considered invalid and displays an error page.</span></span>

### <a name="onnext"></a><span data-ttu-id="b9526-130">OnNext ()</span><span class="sxs-lookup"><span data-stu-id="b9526-130">OnNext()</span></span>

-   <span data-ttu-id="b9526-131">Reagiert, wenn der Benutzer im Assistenten auf **weiter** klickt.</span><span class="sxs-lookup"><span data-stu-id="b9526-131">Responds when the user clicks **Next** in the wizard.</span></span>
-   <span data-ttu-id="b9526-132">Wenn die aktuelle serverseitige Seite die letzte serverseitige Seite ist, rufen Sie **Window. extern. finalnext** auf, um den Client anzuweisen, zur nächsten Client seitigen Seite zu navigieren, oder um den Assistenten abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="b9526-132">If the current server-side page is the last server-side page, call **window.external.FinalNext** to instruct the client to navigate to the next client-side page or to complete the wizard.</span></span>
-   <span data-ttu-id="b9526-133">Wenn die aktuelle serverseitige Seite nicht die letzte serverseitige Seite ist, navigieren Sie zur nächsten serverseitigen Seite.</span><span class="sxs-lookup"><span data-stu-id="b9526-133">If the current server-side page is not the last server-side page, navigate to the next server-side page.</span></span>

### <a name="oncancel"></a><span data-ttu-id="b9526-134">OnCancel ()</span><span class="sxs-lookup"><span data-stu-id="b9526-134">OnCancel()</span></span>

-   <span data-ttu-id="b9526-135">Reagiert, wenn der Benutzer im Assistenten auf **Abbrechen** klickt.</span><span class="sxs-lookup"><span data-stu-id="b9526-135">Responds when the user clicks **Cancel** in the wizard.</span></span>
-   <span data-ttu-id="b9526-136">Die Benutzeroberfläche sollte so entworfen werden, dass der Benutzer Sie jederzeit abbrechen kann.</span><span class="sxs-lookup"><span data-stu-id="b9526-136">The UI should be designed so the user can cancel at any time.</span></span>
-   <span data-ttu-id="b9526-137">Nachdem die Verarbeitung in der **OnCancel** -Funktion verarbeitet wurde, schließt der Client den Assistenten.</span><span class="sxs-lookup"><span data-stu-id="b9526-137">Once any processing in the **OnCancel** function is processed, the client closes the wizard.</span></span>

## <a name="other-methods-and-properties"></a><span data-ttu-id="b9526-138">Andere Methoden und Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b9526-138">Other Methods and Properties</span></span>

<span data-ttu-id="b9526-139">Der Zugriff auf Client implementierte Funktionen erfolgt über **Windows. extern**, ebenso wie Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b9526-139">Client-implemented functions are accessed through **windows.external**, as are properties.</span></span> <span data-ttu-id="b9526-140">Folgende Dienste stehen zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="b9526-140">Available services are as follows:</span></span>

### <a name="methods"></a><span data-ttu-id="b9526-141">Methoden</span><span class="sxs-lookup"><span data-stu-id="b9526-141">Methods</span></span>

-   [<span data-ttu-id="b9526-142">**"Abadertext"**</span><span class="sxs-lookup"><span data-stu-id="b9526-142">**SetHeaderText**</span></span>](/windows/desktop/shell/iwebwizardhost-setheadertext)
-   [<span data-ttu-id="b9526-143">**""-Schaltflächen**</span><span class="sxs-lookup"><span data-stu-id="b9526-143">**SetWizardButtons**</span></span>](/windows/desktop/shell/iwebwizardhost-setwizardbuttons)
-   [<span data-ttu-id="b9526-144">**Passport Authenticate**</span><span class="sxs-lookup"><span data-stu-id="b9526-144">**PassportAuthenticate**</span></span>](/windows/desktop/shell/inewwdevents-passportauthenticate)

### <a name="properties"></a><span data-ttu-id="b9526-145">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b9526-145">Properties</span></span>

-   <span data-ttu-id="b9526-146">[**Caption**](/previous-versions/windows/desktop/legacy/bb774352(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b9526-146">[**Caption**](/previous-versions/windows/desktop/legacy/bb774352(v=vs.85))</span></span>
-   [<span data-ttu-id="b9526-147">**Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="b9526-147">**Property**</span></span>](/windows/desktop/shell/iwebwizardhost-property)

<span data-ttu-id="b9526-148">Das folgende Codebeispiel zeigt serverseitigen Code für eine einfache Assistenten Seite, die die Fehlerseite des Webdiensts implementiert.</span><span class="sxs-lookup"><span data-stu-id="b9526-148">The following code sample shows server-side code for a simple wizard page which implements the web service's error page.</span></span>


```
<html>
    <head>
        <script language="JavaScript">
            function window.onload()
            {
                window.external.SetWizardButtons(1, 0, 0);    
                <!-- Back button enabled -->
            }

            function window.onback()
            {
                window.external.FinalBack();
            }
        </script>
    </head>
.
.
.
</html>
                    
```



## <a name="related-topics"></a><span data-ttu-id="b9526-149">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b9526-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9526-150">Client seitiges Design</span><span class="sxs-lookup"><span data-stu-id="b9526-150">Client-Side Design</span></span>](pubwiz-client.md)
</dt> <dt>

[<span data-ttu-id="b9526-151">Registrieren eines Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="b9526-151">Registering a Service</span></span>](pubwiz-reg.md)
</dt> </dl>

 

 