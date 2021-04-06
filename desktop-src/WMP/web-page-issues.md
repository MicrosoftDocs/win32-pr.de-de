---
title: Webseiten Probleme
description: Webseiten Probleme
ms.assetid: fd97540e-21e9-443e-99ec-ed29f4a2570a
keywords:
- Windows Media Metadatei-Wiedergabelisten, Webseiten
- Wiedergabelisten, Webseiten
- Metadatei-Wiedergabelisten, Webseiten
- Windows Media Metadatei-Wiedergabelisten, Anpassen von HtmlView
- Wiedergabelisten, Anpassen von HtmlView
- Metadatei-Wiedergabelisten, Anpassen von HtmlView
- Windows Media Metadatei-Wiedergabelisten, HtmlView-Anpassung
- Wiedergabelisten, HtmlView-Anpassung
- Metadatei-Wiedergabelisten, HtmlView-Anpassung
- Anpassen von HtmlView
- Windows Media Player, Webseiten
- Windows Media Player, Anpassen von HtmlView
- Windows Media Player, HtmlView-Anpassung
- HtmlView, anpassen
- HtmlView, Webseiten
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 882d8993ba3690cf8c4a068f9861ccf39cd1a95c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713403"
---
# <a name="web-page-issues"></a><span data-ttu-id="16114-118">Webseiten Probleme</span><span class="sxs-lookup"><span data-stu-id="16114-118">Web Page Issues</span></span>

<span data-ttu-id="16114-119">Beim Erstellen einer Webseite, die in der Funktion "Windows-Media Player **jetzt spielen** " angezeigt wird, müssen Sie einige Punkte beachten.</span><span class="sxs-lookup"><span data-stu-id="16114-119">There are some things to consider when you create a webpage to be displayed in the Windows Media Player **Now Playing** feature.</span></span> <span data-ttu-id="16114-120">In diesem Abschnitt werden einige der Probleme erläutert, die beim Erstellen des webbasierten Inhalts auftreten können.</span><span class="sxs-lookup"><span data-stu-id="16114-120">This section discusses some of the issues you might encounter when creating your Web-based content.</span></span>

## <a name="customizing-htmlview"></a><span data-ttu-id="16114-121">Anpassen von HtmlView</span><span class="sxs-lookup"><span data-stu-id="16114-121">Customizing HTMLView</span></span>

<span data-ttu-id="16114-122">Ihre HtmlView-Webseite kann so einfach oder komplex sein, wie Sie möchten.</span><span class="sxs-lookup"><span data-stu-id="16114-122">Your HTMLView webpage can be as simple or complex as you want.</span></span> <span data-ttu-id="16114-123">Sie können alle Elemente einschließen, die Sie normalerweise in Ihrem webbasierten Inhalt verwenden.</span><span class="sxs-lookup"><span data-stu-id="16114-123">You can include any of the elements you usually use in your Web-based content.</span></span> <span data-ttu-id="16114-124">Wenn Sie das Windows Media Player-Steuerelement einbetten, können Sie eine der vom Steuerelement bereitgestellten Benutzeroberflächen anzeigen, eine eigene Benutzeroberfläche mithilfe von HTML-und Skriptcode erstellen oder überhaupt keine Benutzeroberfläche bereitstellen (was bedeutet, dass der Benutzer die Transport Steuerelemente des Vollmodus-Players verwenden kann).</span><span class="sxs-lookup"><span data-stu-id="16114-124">If you embed the Windows Media Player control, you can display one of the user interfaces supplied by the control, create your own user interface using HTML and script code, or provide no UI at all (which means that the user can use the transport controls of the full-mode Player).</span></span>

<span data-ttu-id="16114-125">Die empfohlene Größe für Webseiten, die mithilfe der HtmlView-Funktion angezeigt werden, beträgt 575 x 345 Pixel.</span><span class="sxs-lookup"><span data-stu-id="16114-125">The recommended size for webpages displayed by using the HTMLView feature is 575 x 345 pixels.</span></span> <span data-ttu-id="16114-126">Der Benutzer hat jedoch die Möglichkeit, die Größe des Windows-Media Player zu ändern und die Bildschirmauflösung auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="16114-126">The user, however, has the ability to resize Windows Media Player and choose the screen resolution.</span></span> <span data-ttu-id="16114-127">Wenn die HtmlView-Webseite größer ist als die Größe, die von der Funktion " **jetzt** wiedergeben" untergebracht wird, zeigt der Player horizontale und vertikale Schiebe leisten an, mit denen der Benutzer die gesamte Seite anzeigen kann.</span><span class="sxs-lookup"><span data-stu-id="16114-127">If the HTMLView webpage is larger than the size accommodated by the **Now Playing** feature, the Player displays horizontal and vertical scroll bars that enable the user to see the entire page.</span></span> <span data-ttu-id="16114-128">Testen Sie den HtmlView-Inhalt mithilfe verschiedener Bildschirmauflösungen und Player Größen, um die beste Größe für Ihre Webseite zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="16114-128">You should test your HTMLView content using a variety of screen resolutions and Player sizes to determine the best size for your webpage.</span></span>

<span data-ttu-id="16114-129">Windows Media Player bietet keine Methode, mit der Sie eine Größe für den vollmodusplayer angeben können.</span><span class="sxs-lookup"><span data-stu-id="16114-129">Windows Media Player does not provide a method that enables you to specify a size for the full-mode Player.</span></span>

## <a name="web-page-navigation"></a><span data-ttu-id="16114-130">Webseiten Navigation</span><span class="sxs-lookup"><span data-stu-id="16114-130">Web page navigation</span></span>

<span data-ttu-id="16114-131">Windows Media Player bietet keine Navigations Symbolleiste für Webseiten, die im Feature " **jetzt** wiedergeben" angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="16114-131">Windows Media Player does not provide a navigation toolbar for webpages displayed in the **Now Playing** feature.</span></span> <span data-ttu-id="16114-132">Dies bedeutet, dass Sie über die gesamte Kontrolle verfügen, ob Benutzer von ihrer HtmlView-Webseite Weg navigieren können.</span><span class="sxs-lookup"><span data-stu-id="16114-132">This means that you have complete control over whether users can navigate away from your HTMLView webpage.</span></span> <span data-ttu-id="16114-133">Wenn Sie es Benutzern ermöglichen möchten, zu anderen Webseiten zu navigieren, müssen Sie Elemente in Ihren HTML-Code einschließen, um diese Funktionalität bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="16114-133">If you want to enable users to navigate to other webpages, you must include elements in your HTML code to provide that functionality.</span></span>

## <a name="retrieving-the-parent-window"></a><span data-ttu-id="16114-134">Abrufen des übergeordneten Fensters</span><span class="sxs-lookup"><span data-stu-id="16114-134">Retrieving the parent window</span></span>

<span data-ttu-id="16114-135">Wenn Ihr vorhandener Skriptcode **Window. Parent** verwendet, um das übergeordnete Fenster Objekt abzurufen, funktioniert dieser Code auf der HtmlView-Webseite nicht.</span><span class="sxs-lookup"><span data-stu-id="16114-135">If your existing script code uses **window.parent** to retrieve the parent window object, this code will not work in your HTMLView webpage.</span></span> <span data-ttu-id="16114-136">Wenn Sie HtmlView verwenden, ist kein übergeordnetes Fenster Objekt vorhanden. Diese Skriptfunktion ist daher nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="16114-136">When you use HTMLView, there is no parent window object; therefore, this scripting feature is unavailable.</span></span>

## <a name="about-the-embedded-browser"></a><span data-ttu-id="16114-137">Informationen zum eingebetteten Browser</span><span class="sxs-lookup"><span data-stu-id="16114-137">About the embedded browser</span></span>

<span data-ttu-id="16114-138">Da Windows Media Player eine eingebettete Instanz von Internet Explorer zum Anzeigen von HtmlView-Inhalten verwendet, gelten die Benutzereinstellungen und-Richtlinien für Internet Explorer für alle Webseiten, die im Player angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="16114-138">Because Windows Media Player uses an embedded instance of Internet Explorer to display HTMLView content, the user settings and policies for Internet Explorer apply to any webpages displayed in the Player.</span></span> <span data-ttu-id="16114-139">Wenn der Benutzer z. b. Internet Explorer so konfiguriert hat, dass Webseiten nicht auf den Computer heruntergeladen werden, wird die HtmlView-Webseite ebenfalls verhindert.</span><span class="sxs-lookup"><span data-stu-id="16114-139">For example, if the user has configured Internet Explorer to prevent webpages from downloading cookies to the computer, your HTMLView webpage is also prevented from doing this.</span></span>

<span data-ttu-id="16114-140">Webseiten, die mithilfe der HtmlView-Funktion geöffnet wurden, werden immer in Internet Explorer **Internet** Security Zone ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="16114-140">Web pages opened by using the HTMLView feature always run in the Internet Explorer **Internet** security zone.</span></span>

<span data-ttu-id="16114-141">Im eingebetteten Webbrowser-Steuerelement werden die gleichen Regeln zum Zwischenspeichern von Webseiten als eigenständige Version von Internet Explorer verwendet.</span><span class="sxs-lookup"><span data-stu-id="16114-141">The embedded Web browser control uses the same rules to cache webpages as the stand-alone version of Internet Explorer.</span></span> <span data-ttu-id="16114-142">Beim Erstellen Ihrer Inhalte empfiehlt es sich, Active Server Pages (ASP) zu verwenden, um sicherzustellen, dass der Inhalt jedes Mal vom Webserver übermittelt wird, wenn Windows Media Player auf die HtmlView-Webseite zugreift.</span><span class="sxs-lookup"><span data-stu-id="16114-142">It's a good idea to use Active Server Pages (ASP) when creating your content to ensure that the content is delivered from your web server each time Windows Media Player accesses the HTMLView webpage.</span></span> <span data-ttu-id="16114-143">Die Verwendung von ASP-Seiten kann so einfach sein wie das Umbenennen der Webseite zur Verwendung der Dateinamenerweiterung ". asp".</span><span class="sxs-lookup"><span data-stu-id="16114-143">Using ASP pages can be as simple as renaming your webpage to use an .asp file name extension.</span></span>

## <a name="about-local-web-content"></a><span data-ttu-id="16114-144">Informationen zu lokalem Webinhalt</span><span class="sxs-lookup"><span data-stu-id="16114-144">About local Web content</span></span>

<span data-ttu-id="16114-145">Mit der HtmlView-Funktion können Sie keine Webseiten öffnen, die auf dem Computer des Benutzers gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="16114-145">The HTMLView feature does not allow you to open webpages that are stored on the user's computer.</span></span>

## <a name="prompting-the-user"></a><span data-ttu-id="16114-146">Auffordern des Benutzers</span><span class="sxs-lookup"><span data-stu-id="16114-146">Prompting the user</span></span>

<span data-ttu-id="16114-147">Sie können " **Window. prompt** " verwenden, um den Benutzer zur Eingabe von Informationen aufzufordern.</span><span class="sxs-lookup"><span data-stu-id="16114-147">You can use **window.prompt** to prompt the user for information.</span></span> <span data-ttu-id="16114-148">**Window. Alert** und **Window. Confirm** sind jedoch bei der Verwendung von HtmlView nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="16114-148">However, **window.alert** and **window.confirm** are not available when using HTMLView.</span></span>

## <a name="timing-issues"></a><span data-ttu-id="16114-149">Zeit Steuerungsprobleme</span><span class="sxs-lookup"><span data-stu-id="16114-149">Timing issues</span></span>

<span data-ttu-id="16114-150">Bei der Verwendung eines eingebetteten Windows Media Player-Steuer Elements auf der HtmlView-Webseite können Zeit Steuerungsprobleme auftreten.</span><span class="sxs-lookup"><span data-stu-id="16114-150">You may encounter timing issues when using an embedded Windows Media Player control in your HTMLView webpage.</span></span> <span data-ttu-id="16114-151">In HtmlView teilt ein eingebettetes Player-Steuerelement seine Wiedergabe-Engine mit dem eigenständigen Windows-Media Player.</span><span class="sxs-lookup"><span data-stu-id="16114-151">In HTMLView, an embedded Player control shares its playback engine with the stand-alone Windows Media Player.</span></span> <span data-ttu-id="16114-152">Es ist möglich, dass der eigenständige Player geöffnet wird und mit der Wiedergabe des ersten Wiedergabelisten Eintrags beginnt, bevor die Webseite (und damit das Player-Steuerelement) geladen wird.</span><span class="sxs-lookup"><span data-stu-id="16114-152">It is possible that the stand-alone Player may open and begin playing the first playlist entry before the webpage (and, therefore, the Player control) finishes loading.</span></span> <span data-ttu-id="16114-153">Dies bedeutet Folgendes: Wenn Sie die Ereignisse **OpenStateChange** oder **PlayStateChange** behandeln, empfängt der Skriptcode keine Ereignis Benachrichtigungen für diese Ereignisse, bis das Player-Steuerelement und die zugehörigen Objekte geladen sind.</span><span class="sxs-lookup"><span data-stu-id="16114-153">This means that if you handle the **OpenStateChange** or **PlayStateChange** events, the script code will not receive event notifications for these events until the Player control and its associated objects are loaded.</span></span>

<span data-ttu-id="16114-154">Sie können Schritte im Code ausführen, um die Wiedergabe zu verzögern, bis das Windows Media Player-Steuerelement instanziiert wird.</span><span class="sxs-lookup"><span data-stu-id="16114-154">You can take steps in your code to delay playback until the Windows Media Player control is instantiated.</span></span> <span data-ttu-id="16114-155">Eine Möglichkeit hierfür besteht darin, den ersten Eintrag in der Metadatei-Wiedergabeliste auf eine Bilddatei zu verweisen und die Dauer der Datei auf eine Zeitspanne festzulegen, die dem Player-Steuerelement das Laden ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="16114-155">One way to do this is to make the first entry in your metafile playlist point to an image file and set the duration of the file to a length of time that allows the Player control to load.</span></span> <span data-ttu-id="16114-156">Der folgende Beispielcode veranschaulicht diese Option:</span><span class="sxs-lookup"><span data-stu-id="16114-156">The following example code demonstrates this option:</span></span>


```XML
<ASX version="3.0">
   <PARAM name="HTMLView" value="https://www.proseware.com/htmlview1.htm"/>

<ENTRY>
   <REF href="https://www.proseware.com/blank.jpg"/>
   <DURATION  VALUE = "1:00"/>
</ENTRY>

<ENTRY>
   <REF href="rtsp://www.proseware.com/content1.wma"/>
</ENTRY>

</ASX>

```



<span data-ttu-id="16114-157">Wenn die vorherige Wiedergabeliste geöffnet wird, wartet Windows Media Player auf den ersten Eintrag in der Wiedergabeliste bis zu einer Minute, während der Spieler die HtmlView-Webseite lädt.</span><span class="sxs-lookup"><span data-stu-id="16114-157">When the preceding playlist opens, Windows Media Player waits at the first entry in the playlist for up to one minute while the Player loads the HTMLView webpage.</span></span>

<span data-ttu-id="16114-158">Schreiben Sie als nächstes in der HtmlView-Webseite Skriptcode, um das **OnLoad** -Ereignis für das **Body** -Element zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="16114-158">Next, in your HTMLView webpage, write script code to handle the **onload** event for the **BODY** element.</span></span> <span data-ttu-id="16114-159">In der Ereignishandlerfunktion wird die Player **Controls. Next** -Methode aufgerufen, um die Wiedergabe des zweiten Eintrags in der Wiedergabeliste zu starten.</span><span class="sxs-lookup"><span data-stu-id="16114-159">In the event handler function, call the Player **Controls.Next** method to begin playback of the second entry in the playlist.</span></span>


```XML
<HTML>
<!-- Define the event handler function. -->
<BODY  onload = "OnLoad();">

<OBJECT id = "Player" 
    CLASSID = "CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6"> 
        <PARAM Name = "autoStart"  Value = "true">
        <PARAM Name = "uiMode" Value = "none">

</OBJECT>

<!-- Handle the BODY onload event. -->
<SCRIPT>
function OnLoad()
{
   // Advance to the second entry in the playlist.
   Player.controls.next();
}
</SCRIPT>

</BODY>
</HTML>

```



<span data-ttu-id="16114-160">Wenn die Webseite im vorherigen Beispiel den Lade Zeitpunkt abgeschlossen hat, wechselt Windows Media Player sofort zum zweiten Eintrag in der Wiedergabeliste.</span><span class="sxs-lookup"><span data-stu-id="16114-160">When the webpage in the preceding example finishes loading, Windows Media Player immediately advances to the second entry in the playlist.</span></span> <span data-ttu-id="16114-161">Dadurch wird die für das erste Element in der Wiedergabeliste angegebene Dauer überschrieben. Dies bedeutet, dass der Benutzer nicht vollständig eine Minute warten muss, bevor der gewünschte Inhalt angezeigt wird. Er muss nur warten, bis die Webseite geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="16114-161">This overrides the duration specified for the first element in the playlist, meaning that the user doesn't have to wait the full one minute before seeing the desired content; he or she only has to wait for the webpage to finish loading.</span></span> <span data-ttu-id="16114-162">Da das Player-Steuerelement zu diesem Zeitpunkt vollständig instanziiert wird, können die Ereignisse **OpenStateChange** und **PlayStateChange** auf die übliche Weise behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="16114-162">Because the Player control is completely instantiated at this point, the **OpenStateChange** and **PlayStateChange** events can be handled in the usual manner.</span></span>

## <a name="related-topics"></a><span data-ttu-id="16114-163">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="16114-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16114-164">**Anzeigen von Webseiten in Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="16114-164">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="16114-165">**Player. PlayStateChange-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="16114-165">**Player.PlayStateChange Event**</span></span>](player-player-playstatechange.md)
</dt> <dt>

[<span data-ttu-id="16114-166">**Player. OpenStateChange-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="16114-166">**Player.OpenStateChange Event**</span></span>](player-player-openstatechange.md)
</dt> </dl>

 

 




