---
description: Der Webauthentifizierungs Broker basiert auf den gleichen Technologien wie Internet Explorer in Windows.
ms.assetid: 4BBAE30F-63AB-4AB0-9C99-016EF05220E8
title: Überlegungen für die Webseitenentwicklung
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbe7e738616589afc4f7ba4f03d92a12207d189c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346008"
---
# <a name="considerations-for-the-web-page-development"></a><span data-ttu-id="33899-103">Überlegungen für die Webseitenentwicklung</span><span class="sxs-lookup"><span data-stu-id="33899-103">Considerations for the web page development</span></span>

<span data-ttu-id="33899-104">Der Webauthentifizierungs Broker basiert auf den gleichen Technologien wie Internet Explorer in Windows.</span><span class="sxs-lookup"><span data-stu-id="33899-104">Web Authentication Broker is built on the top of the same technologies that power Internet Explorer in Windows.</span></span> <span data-ttu-id="33899-105">Aufgrund eines besonderen zwecks dieser Komponente wurden einige Features von Internet Explorer jedoch deaktiviert oder für eine bestimmte Konfiguration gesperrt.</span><span class="sxs-lookup"><span data-stu-id="33899-105">However, due to a very special purpose of this component some features of the Internet Explorer were disabled or locked to specific configuration.</span></span> <span data-ttu-id="33899-106">Außerdem bietet der Webauthentifizierungs Broker einen dedizierten Ereignis Protokollierungs Kanal, um Probleme mit den von ihm verarbeiteten Seiten zu beheben.</span><span class="sxs-lookup"><span data-stu-id="33899-106">Also, Web Authentication Broker provides a dedicated event logging channel to help troubleshoot issues with pages that it processes.</span></span>

## <a name="internet-explorer-10-standard-document-mode"></a><span data-ttu-id="33899-107">Internet Explorer 10-Standarddokument Modus</span><span class="sxs-lookup"><span data-stu-id="33899-107">Internet Explorer 10 standard document mode</span></span>

<span data-ttu-id="33899-108">Der Webauthentifizierungs Broker zeigt alle Seiten im "IE10-Standards-Modus" an.</span><span class="sxs-lookup"><span data-stu-id="33899-108">The Web Authentication Broker displays all pages in the "IE10 Standards Mode".</span></span> <span data-ttu-id="33899-109">Sie können die Entwicklertools in Internet Explorer verwenden, um zu sehen, wie Ihre Seite unter verschiedenen Dokument Modi funktioniert.</span><span class="sxs-lookup"><span data-stu-id="33899-109">You can use the developer tools in Internet Explorer to see how your page works under different document modes.</span></span> <span data-ttu-id="33899-110">Weitere Informationen zur Kompatibilität mit Internet Explorer 10 finden Sie in den MSDN-Themen für [Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/dev-guides/hh673527(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="33899-110">For more information on Internet Explorer 10 compatibility, see the MSDN topics for [Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/dev-guides/hh673527(v=vs.85)).</span></span>

## <a name="disabled-and-locked-down-features"></a><span data-ttu-id="33899-111">Deaktivierte und gesperrte Features</span><span class="sxs-lookup"><span data-stu-id="33899-111">Disabled and locked down features</span></span>

<span data-ttu-id="33899-112">Einige Features von Internet Explorer sind entweder vollständig deaktiviert oder für bestimmte Werte gesperrt, die in den Internet Optionen des Betriebssystems nicht geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="33899-112">Several features of Internet Explorer are either completely disabled or locked down to specific values that can’t be changed in the Internet Options of the operating system.</span></span>



| <span data-ttu-id="33899-113">Funktion</span><span class="sxs-lookup"><span data-stu-id="33899-113">Feature</span></span>                            | <span data-ttu-id="33899-114">Status</span><span class="sxs-lookup"><span data-stu-id="33899-114">Status</span></span>                                                                                                                                                                                                          |
|------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33899-115">Anwendungscache-API ("AppCache")</span><span class="sxs-lookup"><span data-stu-id="33899-115">Application Cache API ("AppCache")</span></span> | <span data-ttu-id="33899-116">Disabled</span><span class="sxs-lookup"><span data-stu-id="33899-116">Disabled</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="33899-117">Link Verlauf</span><span class="sxs-lookup"><span data-stu-id="33899-117">Link history</span></span>                       | <span data-ttu-id="33899-118">Disabled</span><span class="sxs-lookup"><span data-stu-id="33899-118">Disabled</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="33899-119">Temporäre Dateien</span><span class="sxs-lookup"><span data-stu-id="33899-119">Temporary files</span></span>                    | <span data-ttu-id="33899-120">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="33899-120">Enabled</span></span>                                                                                                                                                                                                         |
| <span data-ttu-id="33899-121">Cookies</span><span class="sxs-lookup"><span data-stu-id="33899-121">Cookies</span></span>                            | <span data-ttu-id="33899-122">Sitzungs Cookies sind aktiviert.</span><span class="sxs-lookup"><span data-stu-id="33899-122">Session cookies are enabled.</span></span> <span data-ttu-id="33899-123">Persistente Cookies sind zulässig, unterliegen jedoch dem automatischen Bereinigung, es sei denn, der Webauthentifizierungs Broker befindet sich im SSO-Modus.</span><span class="sxs-lookup"><span data-stu-id="33899-123">Persisted cookies are allowed, but are subject to automatic cleanup unless the Web Authentication Broker is in the SSO mode.</span></span> <span data-ttu-id="33899-124">Weitere Informationen finden Sie im Abschnitt einmaliges Anmelden.</span><span class="sxs-lookup"><span data-stu-id="33899-124">For more information, see the Single Sign On section.</span></span> |
| <span data-ttu-id="33899-125">Index-DB</span><span class="sxs-lookup"><span data-stu-id="33899-125">Index DB</span></span>                           | <span data-ttu-id="33899-126">Disabled</span><span class="sxs-lookup"><span data-stu-id="33899-126">Disabled</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="33899-127">Dom-Speicher</span><span class="sxs-lookup"><span data-stu-id="33899-127">DOM storage</span></span>                        | <span data-ttu-id="33899-128">Disabled</span><span class="sxs-lookup"><span data-stu-id="33899-128">Disabled</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="33899-129">ActiveX</span><span class="sxs-lookup"><span data-stu-id="33899-129">ActiveX</span></span>                            | <span data-ttu-id="33899-130">Disabled</span><span class="sxs-lookup"><span data-stu-id="33899-130">Disabled</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="33899-131">Dateidownloads</span><span class="sxs-lookup"><span data-stu-id="33899-131">File downloads</span></span>                     | <span data-ttu-id="33899-132">Disabled</span><span class="sxs-lookup"><span data-stu-id="33899-132">Disabled</span></span>                                                                                                                                                                                                        |



 

## <a name="https-requirement"></a><span data-ttu-id="33899-133">HTTPS-Anforderung</span><span class="sxs-lookup"><span data-stu-id="33899-133">HTTPS requirement</span></span>

<span data-ttu-id="33899-134">Die erste URL, die eine Anwendung für die Kommunikation mit dem Online Anbieter verwendet, muss https sein.</span><span class="sxs-lookup"><span data-stu-id="33899-134">The first URL that an application will use to communicate with the online provider is required to be HTTPS.</span></span>

## <a name="dimension-for-different-window-sizes"></a><span data-ttu-id="33899-135">Dimension für verschiedene Fenstergrößen</span><span class="sxs-lookup"><span data-stu-id="33899-135">Dimension for different window sizes</span></span>

<span data-ttu-id="33899-136">Eine Windows 8-App kann in verschiedenen Größen wie z. b. dem Vollbildmodus, einem Fenster mit Größenänderung oder in einem Charm wie dem Teilen-Charm angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="33899-136">A Windows 8 app may appear in several different sizes such as full screen, a resized window, or within a Charm such as Share Charm.</span></span> <span data-ttu-id="33899-137">Abhängig davon, in welchem Fenster Layout der Webauthentifizierungs Broker angezeigt wird, kann die Größe, mit der die Webseiten funktionieren, unterschiedlich sein.</span><span class="sxs-lookup"><span data-stu-id="33899-137">Depending in which window layout the Web Authentication Broker appears, the size with which the web pages have to work could be different.</span></span> <span data-ttu-id="33899-138">Weitere Informationen finden Sie im Thema [Richtlinien für die Größe der Größe in schmale Layouts](/previous-versions/windows/hh465371(v=win.10)) und in den [Richtlinien für die Freigabe von Inhalten](/previous-versions/windows/hh465251(v=win.10)) .</span><span class="sxs-lookup"><span data-stu-id="33899-138">For more information, see the [Guidelines for resizing to narrow layouts](/previous-versions/windows/hh465371(v=win.10)) topic and the [Guidelines for sharing content](/previous-versions/windows/hh465251(v=win.10)) topic.</span></span>

<span data-ttu-id="33899-139">Auf der Webseite sollten CSS-Medien Abfragen verwendet werden, um die zu verwendende Größe zu überprüfen und sich entsprechend auszulagern.</span><span class="sxs-lookup"><span data-stu-id="33899-139">The web page should use CSS media queries to check the size it has to work with and lay itself out accordingly.</span></span> <span data-ttu-id="33899-140">Die Seite sollte jedoch nicht basierend auf den genauen Pixeln entworfen werden, die hier dokumentiert sind, und Sie sollten in der Lage sein, auf unterschiedliche Größen zu skalieren.</span><span class="sxs-lookup"><span data-stu-id="33899-140">However, the page should not be designed based on the exact pixels documented here and should be able to scale to different sizes.</span></span> <span data-ttu-id="33899-141">Die in diesem Dokument angegebenen Größen können in zukünftigen Betriebssystemversionen geändert werden.</span><span class="sxs-lookup"><span data-stu-id="33899-141">The sizes specified in this document are subject to change in future OS versions.</span></span>

<span data-ttu-id="33899-142">Wenn eine Seite nicht alle Informationen im zugewiesenen Speicherplatz enthalten kann (z. b. eine lange Liste von Berechtigungen, die eine Anwendung anfordert), stellt der Webauthentifizierungs Broker Bild Lauf leisten bereit, damit der Benutzer bei Bedarf einen Bildlauf durchführen kann.</span><span class="sxs-lookup"><span data-stu-id="33899-142">If a page can’t fit all of the information in the allotted space (for example, a long list of permissions that an application is requesting), the Web Authentication Broker will provide scroll bars to allow the user to scroll the page as needed.</span></span> <span data-ttu-id="33899-143">Zoom wird auch durch Verkleinern von Zoom für Berührungs basierte Geräte und Strg + Mausrad für Desktop-und Laptop-PCs bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="33899-143">Zooming is also provided by pinch zoom for touch-based devices and Ctrl + mouse wheel for desktop and laptop PCs.</span></span>

<span data-ttu-id="33899-144">Um verschiedene Skalierungsfaktoren zu testen, verwenden Sie die in Microsoft Visual Studio Professional 2012 geladene [Web Authentication Broker SDK-Beispiel-App](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker) , die das Simulieren des voll Bild Status und der Größenänderung ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="33899-144">To test different scaling factors use the [Web Authentication Broker SDK sample app](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker) loaded in Microsoft Visual Studio Professional 2012 which allows simulating the full screen and resized states.</span></span>

<span data-ttu-id="33899-145">Stellen Sie zusätzlich zu den oben beschriebenen unterschiedlichen Layouts sicher, dass Sie Ihre Seite in unterschiedlicher Bildschirm Ausrichtung (z. b. Hochformat und Querformat) und unterschiedlichen Gebiets Schemata und Sprachen sowie mit Barrierefreiheits Features wie der Option "alles größere machen" aktivieren.</span><span class="sxs-lookup"><span data-stu-id="33899-145">In addition to different layouts documented above, make sure to test your page in different screen orientation (for example, portrait and landscape), and different locales and languages as well as with accessibility features such as the "Make everything bigger" option turned on.</span></span>

<span data-ttu-id="33899-146">Die verfügbaren Layouts lauten:</span><span class="sxs-lookup"><span data-stu-id="33899-146">The available layouts are:</span></span>

-   [<span data-ttu-id="33899-147">Vollbild</span><span class="sxs-lookup"><span data-stu-id="33899-147">Full screen</span></span>](#full-screen)
-   [<span data-ttu-id="33899-148">Fenstergröße geändert</span><span class="sxs-lookup"><span data-stu-id="33899-148">Resized window</span></span>](#resized)
-   [<span data-ttu-id="33899-149">Charm Ansicht</span><span class="sxs-lookup"><span data-stu-id="33899-149">Charm view</span></span>](#charm-view)
-   [<span data-ttu-id="33899-150">Dateiauswahl Ansicht</span><span class="sxs-lookup"><span data-stu-id="33899-150">File picker view</span></span>](#file-picker-view)

### <a name="full-screen"></a><span data-ttu-id="33899-151">Vollbildmodus</span><span class="sxs-lookup"><span data-stu-id="33899-151">Full screen</span></span>

<span data-ttu-id="33899-152">Für das voll Bild Layout sind die Webseiten Dimensionen:</span><span class="sxs-lookup"><span data-stu-id="33899-152">For the full screen layout, the web page dimensions are:</span></span>

-   <span data-ttu-id="33899-153">Breite: 566 Pixel</span><span class="sxs-lookup"><span data-stu-id="33899-153">Width: 566 pixels</span></span>
-   <span data-ttu-id="33899-154">Height: Bildschirmhöhe (abhängig von der Bildschirmauflösung)</span><span class="sxs-lookup"><span data-stu-id="33899-154">Height: Screen height (depends on the screen resolution)</span></span>

<span data-ttu-id="33899-155">Das folgende Beispiel zeigt die Benutzeroberfläche des Webauthentifizierungs Brokers im voll Bild Layout.</span><span class="sxs-lookup"><span data-stu-id="33899-155">The following example shows the web authentication broker UI in full screen layout.</span></span>

![ein Beispiel für die Benutzeroberfläche des Webauthentifizierungs Brokers im voll Bild Layout](images/wab-figure2.png)

### <a name="resized"></a><span data-ttu-id="33899-157">Geändert</span><span class="sxs-lookup"><span data-stu-id="33899-157">Resized</span></span>

<span data-ttu-id="33899-158">Bei einem Fenster, das in der Größe geändert wird, können die Webseiten Dimensionen wie folgt lauten:</span><span class="sxs-lookup"><span data-stu-id="33899-158">For a resized window, the web page dimensions can be:</span></span>

-   <span data-ttu-id="33899-159">Breite: 260 Pixel</span><span class="sxs-lookup"><span data-stu-id="33899-159">Width: 260 pixels</span></span>
-   <span data-ttu-id="33899-160">Height: Bildschirmhöhe (abhängig von der Bildschirmauflösung)</span><span class="sxs-lookup"><span data-stu-id="33899-160">Height: Screen height (depends on the screen resolution)</span></span>

<span data-ttu-id="33899-161">Das folgende Beispiel zeigt die Webauthentifizierungs Broker-Benutzeroberfläche in einem Fenster, das in der Größe geändert wurde, auf der Xbox-Webseite.</span><span class="sxs-lookup"><span data-stu-id="33899-161">The following example shows the Web Authentication Broker UI in a resized window on the XBox web page.</span></span> <span data-ttu-id="33899-162">Beachten Sie, dass sich die Benutzeroberfläche des Webauthentifizierungs Brokers nur auf der rechten Seite der Bildschirmaufnahme befindet.</span><span class="sxs-lookup"><span data-stu-id="33899-162">Note that the Web Authentication Broker UI is only on the right side of the screen capture.</span></span>

![ein Beispiel für die Webauthentifizierungs Broker-Benutzeroberfläche in einem Fenster, dessen Größe geändert wurde](images/wab-figure3.png)

### <a name="charm-view"></a><span data-ttu-id="33899-164">Charm Ansicht</span><span class="sxs-lookup"><span data-stu-id="33899-164">Charm view</span></span>

<span data-ttu-id="33899-165">In der Charm Ansicht sind die Webseiten Dimensionen:</span><span class="sxs-lookup"><span data-stu-id="33899-165">For the Charm view, the web page dimensions are:</span></span>

-   <span data-ttu-id="33899-166">Breite: 566 Pixel</span><span class="sxs-lookup"><span data-stu-id="33899-166">Width: 566 pixels</span></span>
-   <span data-ttu-id="33899-167">Height: Bildschirmhöhe (abhängig von der Bildschirmauflösung)</span><span class="sxs-lookup"><span data-stu-id="33899-167">Height: Screen height (depends on the screen resolution)</span></span>

<span data-ttu-id="33899-168">Das folgende Beispiel zeigt die Webauthentifizierungs Broker-Benutzeroberfläche in der Charm Ansicht.</span><span class="sxs-lookup"><span data-stu-id="33899-168">The following example shows the Web Authentication Broker UI in Charm view.</span></span>

![ein Beispiel zeigt die Benutzeroberfläche des Webauthentifizierungs Brokers in der Charm Ansicht](images/wab-figure4.png)

### <a name="file-picker-view"></a><span data-ttu-id="33899-170">Dateiauswahl Ansicht</span><span class="sxs-lookup"><span data-stu-id="33899-170">File picker view</span></span>

<span data-ttu-id="33899-171">Für die Dateiauswahl Ansicht sind die Webseiten Dimensionen:</span><span class="sxs-lookup"><span data-stu-id="33899-171">For the file picker view, the web page dimensions are:</span></span>

-   <span data-ttu-id="33899-172">Breite: 566 Pixel</span><span class="sxs-lookup"><span data-stu-id="33899-172">Width: 566 pixels</span></span>
-   <span data-ttu-id="33899-173">Height: Bildschirmhöhe (abhängig von der Bildschirmauflösung)</span><span class="sxs-lookup"><span data-stu-id="33899-173">Height: Screen height (depends on the screen resolution)</span></span>

<span data-ttu-id="33899-174">Das folgende Beispiel zeigt die Benutzeroberfläche des Webauthentifizierungs Brokers in der Dateiauswahl Ansicht.</span><span class="sxs-lookup"><span data-stu-id="33899-174">The following example shows the Web Authentication Broker UI in file picker view.</span></span>

![ein Beispiel zeigt die Benutzeroberfläche des Webauthentifizierungs Brokers in der Dateiauswahl Ansicht](images/wab-figure5.png)

## <a name="no-new-windows-by-default"></a><span data-ttu-id="33899-176">Standardmäßig keine neuen Fenster</span><span class="sxs-lookup"><span data-stu-id="33899-176">No new windows by default</span></span>

<span data-ttu-id="33899-177">Standardmäßig wird keine URL zum Öffnen eines neuen Fensters, sondern im Fenster "Webauthentifizierungs Broker" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="33899-177">By default, no URLs will result in a new window being opened but will instead be displayed within the Web Authentication Broker window.</span></span> <span data-ttu-id="33899-178">Dies umfasst die Windows. Open JavaScript-Methode, das "target"-Attribut der Hyperlinks oder, wenn der Benutzer den Strg + Klick-Mechanismus verwendet, um das Öffnen eines neuen Fensters zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="33899-178">This includes window.open JavaScript method, "target" attribute of the hyperlinks, or when the user uses the Ctrl+Click mechanism to force a new window to open.</span></span> <span data-ttu-id="33899-179">Eine Ausnahme von dieser Regel ist, wenn eine Webseite einen Link als sicher für die Navigation in einem Browser deklariert, wie im Anpassungs Ziel der Hyperlinks beschrieben.</span><span class="sxs-lookup"><span data-stu-id="33899-179">The exception to this rule is when a web page declares a link as safe to be navigated in a browser as described in the Customizing Target of the Hyperlinks.</span></span>

## <a name="related-topics"></a><span data-ttu-id="33899-180">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="33899-180">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33899-181">Beispiel-App für das Web Authentication Broker SDK</span><span class="sxs-lookup"><span data-stu-id="33899-181">Web Authentication Broker SDK sample app</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[<span data-ttu-id="33899-182">**Windows.Security.Authentication.Web**</span><span class="sxs-lookup"><span data-stu-id="33899-182">**Windows.Security.Authentication.Web**</span></span>](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
