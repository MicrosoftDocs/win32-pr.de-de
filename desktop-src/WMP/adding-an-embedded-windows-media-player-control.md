---
title: Hinzufügen eines eingebetteten Windows Media Player-Steuer Elements
description: Hinzufügen eines eingebetteten Windows Media Player-Steuer Elements
ms.assetid: e002bf2a-c51a-448a-80a0-a35d6f32e9c0
keywords:
- Windows Media Metadatei-Wiedergabelisten, Hinzufügen von eingebetteten Fenstern Media Player Steuerelementen
- Wiedergabelisten, Hinzufügen von eingebetteten Windows Media Player-Steuerelementen
- Metadatei-Wiedergabelisten, Hinzufügen von eingebetteten Fenstern Media Player Steuerelementen
- Windows Media Metadatei-Wiedergabelisten, eingebettete Windows Media Player-Steuerelemente
- Wiedergabelisten, eingebettete Windows Media Player-Steuerelemente
- Metadatei-Wiedergabelisten, eingebettete Fenster Media Player
- Hinzufügen von eingebetteten Fenstern Media Player Steuerelementen
- eingebettete Windows Media Player-Steuerelemente
- Windows Media Player, Hinzufügen von eingebetteten Steuerelementen
- Windows Media Player, eingebettete Steuerelemente
- HtmlView, Hinzufügen von eingebetteten Windows-Media Player Steuerelementen
- HtmlView, eingebettete Windows Media Player-Steuerelemente
- HtmlView, Windows Media Player-Objektmodell
- HtmlView, Player-Objektmodell
- Windows Media Player-Objektmodell, Informationen zu
- Objektmodell, Informationen
- Player-Objekt
- Windows Media, Player-Objektmodell
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1dea3b11f59bff2edbcef99f1acda5fd0cfcff46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388511"
---
# <a name="adding-an-embedded-windows-media-player-control"></a><span data-ttu-id="88928-121">Hinzufügen eines eingebetteten Windows Media Player-Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="88928-121">Adding an Embedded Windows Media Player Control</span></span>

<span data-ttu-id="88928-122">Es gibt zwei Gründe, warum Sie in Erwägung gezogen werden, eine eingebettete Instanz von Windows Media Player ihrer HtmlView-Präsentation hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="88928-122">There are two reasons you might consider adding an embedded instance of Windows Media Player to your HTMLView presentation.</span></span> <span data-ttu-id="88928-123">Wenn Sie Videoinhalte anzeigen möchten, müssen Sie zunächst das Windows Media Player ActiveX-Steuerelement verwenden.</span><span class="sxs-lookup"><span data-stu-id="88928-123">First, if you want to display video content, you need to use the Windows Media Player ActiveX control.</span></span> <span data-ttu-id="88928-124">Zweitens: Wenn Sie die Funktionen des Windows Media Player-Objektmodells von der HtmlView-Webseite aus nutzen möchten, müssen Sie hierfür eine Instanz des Player-Steuer Elements verwenden.</span><span class="sxs-lookup"><span data-stu-id="88928-124">Second, if you want to take advantage of features of the Windows Media Player object model from within your HTMLView webpage, you must use an instance the Player control to do so.</span></span>

## <a name="using-the-player-control-to-display-video-in-htmlview-content"></a><span data-ttu-id="88928-125">Verwenden des Player-Steuer Elements zum Anzeigen von Videos im HtmlView-Inhalt</span><span class="sxs-lookup"><span data-stu-id="88928-125">Using the Player control to display video in HTMLView content</span></span>

<span data-ttu-id="88928-126">In der Regel zeigt Windows Media Player Video mit dem Bereich Video und Visualisierung der Funktion **jetzt Wiedergabe** an.</span><span class="sxs-lookup"><span data-stu-id="88928-126">Usually, Windows Media Player displays video using the Video and Visualization pane of the **Now Playing** feature.</span></span> <span data-ttu-id="88928-127">Da HtmlView diesen Bereich verwendet, um Ihre Webseite anzuzeigen, müssen Sie einen zusätzlichen Videoanzeige Bereich angeben, wenn der Player Video abspielen soll.</span><span class="sxs-lookup"><span data-stu-id="88928-127">Since HTMLView uses this area to display your webpage, you must supply an additional video display area if you want the Player to play video.</span></span> <span data-ttu-id="88928-128">Dies ist einfach, wenn Sie das Windows Media Player ActiveX-Steuerelement verwenden.</span><span class="sxs-lookup"><span data-stu-id="88928-128">This is easy to do by using the Windows Media Player ActiveX control.</span></span>

<span data-ttu-id="88928-129">Um das Player-Steuerelement zum Anzeigen von Videos zu verwenden, Betten Sie das Steuerelement mithilfe des **Objekttags** in die HtmlView-Webseite ein.</span><span class="sxs-lookup"><span data-stu-id="88928-129">To use the Player control to display video, embed the control in your HTMLView webpage by using the **OBJECT** tag.</span></span> <span data-ttu-id="88928-130">Dabei handelt es sich um dasselbe Verfahren, das Sie verwenden, um das Player-Steuerelement in eine beliebige Webseite einzubetten, auf der Sie Videos anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="88928-130">This is the same technique you use to embed the Player control into any webpage in which you want to display video.</span></span> <span data-ttu-id="88928-131">Der folgende Beispielcode zeigt die grundlegende Syntax zum Einbetten des Player-Steuer Elements in Internet Explorer:</span><span class="sxs-lookup"><span data-stu-id="88928-131">The following example code shows the basic syntax for embedding the Player control in Internet Explorer:</span></span>


```XML
<OBJECT id = "Player" 
    CLASSID = "CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6"> 
        <PARAM Name = "autoStart"  Value = "true">
        <PARAM Name = "uiMode" Value = "none">
</OBJECT>

```



<span data-ttu-id="88928-132">Der *Autostart* -Parameter stellt sicher, dass der Inhalt automatisch wiedergegeben wird, wenn eine neue URL angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="88928-132">The *autoStart* parameter ensures that content plays automatically whenever a new URL is specified.</span></span> <span data-ttu-id="88928-133">Der Wert, den Sie für *uiMode* angeben, ist für Sie festgelegt, aber Sie möchten bei der Erstellung von Inhalten für HtmlView-Präsentationen normalerweise "None" angeben.</span><span class="sxs-lookup"><span data-stu-id="88928-133">The value you specify for *uiMode* is up to you, but you will usually want to specify "none" when creating content for HTMLView presentations.</span></span> <span data-ttu-id="88928-134">Wenn Sie das Windows Media Player-Steuerelement einbetten, um Videos auf diese Weise anzuzeigen, kann der Benutzer die Wiedergabe mit den Steuerelementen des vollmodusplayers steuern, sodass keine zusätzlichen Transport Steuerelemente auf der Webseite bereitgestellt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="88928-134">When you embed the Windows Media Player control to display video in this manner, the user can control playback using the controls of the full-mode Player, so there's no need to provide additional transport controls in the webpage.</span></span> <span data-ttu-id="88928-135">Sie können den Speicherplatz, den Sie normalerweise für Transport Steuerelemente zuweisen würden, verwenden, um mehr Text, Grafiken oder Links zu anderen Inhalten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="88928-135">You can use the space you would usually allocate for transport controls to display more text, graphics, or links to other content.</span></span>

<span data-ttu-id="88928-136">Geben Sie keinen *URL* -Parameter an, wenn Sie das Windows Media Player-Steuerelement in eine Webseite einbetten, die in einer HtmlView-Präsentation angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="88928-136">Do not specify a *URL* parameter when embedding the Windows Media Player control in a webpage designed to display in an HTMLView presentation.</span></span> <span data-ttu-id="88928-137">Geben Sie stattdessen die digitalen Mediendateien in der. ASX-Datei an, die den Inhalt öffnet.</span><span class="sxs-lookup"><span data-stu-id="88928-137">Instead, specify the digital media files in the .asx file that opens the content.</span></span>

<span data-ttu-id="88928-138">Da Sie den Videoanzeige Bereich auf der HtmlView-Webseite bereitstellen, können Sie entscheiden, wo das Video positioniert werden soll und wie groß der Anzeigebereich sein soll.</span><span class="sxs-lookup"><span data-stu-id="88928-138">Because you provide the video display region in your HTMLView webpage, you can decide where to position the video and how large you want the display region to be.</span></span> <span data-ttu-id="88928-139">Beispielsweise können Sie das **Player** -Objekt in einem HTML **div** -Element enthalten und dann die Position für das **div** -Element angeben, um die Videoanzeige auf der Webseite zu positionieren.</span><span class="sxs-lookup"><span data-stu-id="88928-139">For example, you can contain the **Player** object within an HTML **DIV** element and then specify the position for the **DIV** to situate the video display on the webpage.</span></span> <span data-ttu-id="88928-140">Sie können die Dimensionen der Videoanzeige ändern, indem Sie Werte für die Attribute height und Width des **Object** -Elements angeben.</span><span class="sxs-lookup"><span data-stu-id="88928-140">You can change the dimensions of the video display by specifying values for the height and width attributes of the **OBJECT** element.</span></span> <span data-ttu-id="88928-141">Sie können diese Werte auch mithilfe von Skriptcode angeben.</span><span class="sxs-lookup"><span data-stu-id="88928-141">You can also specify these values using script code.</span></span>

## <a name="using-the-player-object-model"></a><span data-ttu-id="88928-142">Verwenden des Player-Objektmodells</span><span class="sxs-lookup"><span data-stu-id="88928-142">Using the Player object model</span></span>

<span data-ttu-id="88928-143">Das Windows Media Player-Objektmodell macht Eigenschaften, Methoden und Ereignisse verfügbar, die Sie in ihren HtmlView-Webseiten verwenden können.</span><span class="sxs-lookup"><span data-stu-id="88928-143">The Windows Media Player object model exposes properties, methods, and events that you can use in your HTMLView webpages.</span></span> <span data-ttu-id="88928-144">Wenn Sie das Windows Media Player ActiveX-Steuerelement in die HtmlView-Webseite einbetten, haben Sie automatisch Zugriff auf das Player-Objektmodell.</span><span class="sxs-lookup"><span data-stu-id="88928-144">When you embed the Windows Media Player ActiveX control in your HTMLView webpage, you automatically have access to the Player object model.</span></span>

<span data-ttu-id="88928-145">Wenn Sie das Windows Media Player-Steuerelement in die HtmlView-Webseite einbetten, verwenden Sie das Player-Objektmodell nicht, um die zu Wiedergabe Ende digitale Mediendatei anzugeben.</span><span class="sxs-lookup"><span data-stu-id="88928-145">If you embed the Windows Media Player control in your HTMLView webpage, do not use the Player object model to specify the digital media file to be played.</span></span> <span data-ttu-id="88928-146">Wenn Sie z. b. Skriptcode verwenden, um einen Wert für die **URL** -Eigenschaft des eingebetteten Steuer Elements anzugeben, wird die HtmlView-Webseite aus der Funktion " **jetzt** wiedergeben" entladen, wenn die digitale Mediendatei wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="88928-146">For example, if you use script code to specify a value for the **URL** property of the embedded control, your HTMLView webpage will be unloaded from the **Now Playing** feature when the digital media file plays.</span></span> <span data-ttu-id="88928-147">Um dies zu verhindern, öffnen Sie immer die. ASX-Dateien, die HtmlView-Parameter enthalten, wenn Sie das Skript verwenden müssen, um Inhalte digitaler Medien von ihrer HtmlView-Webseite zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="88928-147">To prevent this from happening, always open .asx files that include HTMLView parameters when you need to use script to open digital media content from your HTMLView webpage.</span></span>

## <a name="related-topics"></a><span data-ttu-id="88928-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="88928-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88928-149">**Anzeigen von Webseiten in Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="88928-149">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="88928-150">**Player. uiMode**</span><span class="sxs-lookup"><span data-stu-id="88928-150">**Player.uiMode**</span></span>](player-uimode.md)
</dt> <dt>

[<span data-ttu-id="88928-151">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="88928-151">**Player.URL**</span></span>](player-url.md)
</dt> <dt>

[<span data-ttu-id="88928-152">**Einstellungen. Autostart**</span><span class="sxs-lookup"><span data-stu-id="88928-152">**Settings.autoStart**</span></span>](settings-autostart.md)
</dt> </dl>

 

 




