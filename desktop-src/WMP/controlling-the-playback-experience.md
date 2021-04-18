---
title: Steuern des Wiedergabe Erlebnisses
description: Steuern des Wiedergabe Erlebnisses
ms.assetid: f130eee1-10ef-4cbe-b6ac-8ad24e1f0f34
keywords:
- Windows Media Metadatei-Wiedergabelisten, Steuern der Wiedergabe
- Wiedergabelisten, Steuern der Wiedergabe
- Metadatei-Wiedergabelisten, Steuern der Wiedergabe
- Windows Media Metadatei-Wiedergabelisten, Wiedergabe Probleme
- Wiedergabelisten, Wiedergabe Probleme
- Metadatei-Wiedergabelisten, Wiedergabe Probleme
- Steuern der Wiedergabe
- Windows Media Player, Steuern der Wiedergabe
- Windows Media Player, Wiedergabe Probleme
- HtmlView, Wiedergabe Probleme
- HtmlView, Steuern der Wiedergabe
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6877b869be8ca38ef9266aedf9318103d0e547ca
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340633"
---
# <a name="controlling-the-playback-experience"></a><span data-ttu-id="632e9-114">Steuern des Wiedergabe Erlebnisses</span><span class="sxs-lookup"><span data-stu-id="632e9-114">Controlling the Playback Experience</span></span>

<span data-ttu-id="632e9-115">In diesem Abschnitt werden einige der Wiedergabe Probleme erläutert, die beim Verwenden der HtmlView-Funktion auftreten können.</span><span class="sxs-lookup"><span data-stu-id="632e9-115">This section discusses some of the playback issues you may encounter when using the HTMLView feature.</span></span>

## <a name="requiring-the-user-to-view-web-based-content"></a><span data-ttu-id="632e9-116">Der Benutzer muss webbasierten Inhalt anzeigen.</span><span class="sxs-lookup"><span data-stu-id="632e9-116">Requiring the user to view Web-based content</span></span>

<span data-ttu-id="632e9-117">Sie können sich entscheiden, dass Benutzer nur in der Lage sein sollen, Ihre digitalen Medieninhalte zu nutzen, wenn der webbasierte HtmlView-Inhalt ebenfalls angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="632e9-117">You may decide that you only want users to be able to enjoy your digital media content when the HTMLView Web-based content is also displayed.</span></span> <span data-ttu-id="632e9-118">Sie können Skriptcode in Ihre HtmlView-Webseite einschließen, der die Wiedergabe des digitalen Medien Inhalts beendet, wenn der Benutzer von der Funktion " **jetzt** Wiedergabe" entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="632e9-118">You can include script code in your HTMLView webpage that stops playback of the digital media content if the user switches away from the **Now Playing** feature.</span></span> <span data-ttu-id="632e9-119">Zu diesem Zweck können Sie einen Ereignishandler für das **Entlade** Ereignis als Teil des **Body** -Elements angeben, wie der folgende HTML-Code veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="632e9-119">To do this, you can specify an event handler for the **unload** event as part of the **BODY** element, as the following HTML code demonstrates:</span></span>


```XML
<BODY onunload = "UnloadMe();">

```



<span data-ttu-id="632e9-120">Anschließend können Sie Skriptcode in die Ereignishandlerfunktion einschließen, um die Datei im Player zu schließen.</span><span class="sxs-lookup"><span data-stu-id="632e9-120">Then you can include script code in your event handler function to close the file in the Player.</span></span> <span data-ttu-id="632e9-121">Der folgende Beispielcode bewirkt Folgendes:</span><span class="sxs-lookup"><span data-stu-id="632e9-121">The following example code does this:</span></span>


```XML
function UnloadMe()
{
   Player.close();
}

```



<span data-ttu-id="632e9-122">Wenn der Benutzer **nun** durch Klicken auf eine Schaltfläche zum Öffnen einer anderen Windows Media Player-Funktion wechselt, z. b. der Bibliothek, schließt der Spieler den eingebetteten Browser.</span><span class="sxs-lookup"><span data-stu-id="632e9-122">When the user switches away from **Now Playing** by clicking a button to open another Windows Media Player feature, such as the library, the Player closes the embedded browser.</span></span> <span data-ttu-id="632e9-123">Dies bewirkt, dass das **onentlade** -Ereignis stattfindet, wobei das Skript in der Funktion mit dem Namen **unloadme** ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="632e9-123">This causes the **onunload** event to occur, running the script in the function named **UnloadMe**.</span></span> <span data-ttu-id="632e9-124">Die [Player. Close](player-close.md) -Methode beendet die Wiedergabe und entlädt die aktuelle digitale Mediendatei.</span><span class="sxs-lookup"><span data-stu-id="632e9-124">The [Player.close](player-close.md) method stops playback and unloads the current digital media file.</span></span> <span data-ttu-id="632e9-125">Um den Inhalt erneut anzuzeigen, muss der Benutzer die ursprüngliche. ASX-Datei erneut öffnen.</span><span class="sxs-lookup"><span data-stu-id="632e9-125">To view the content again, the user must reopen the original .asx file.</span></span> <span data-ttu-id="632e9-126">Diese Technik hält auch die Wiedergabe an, wenn der Benutzer von der HtmlView-Webseite weg navigiert.</span><span class="sxs-lookup"><span data-stu-id="632e9-126">This technique also stops playback when the user navigates away from the HTMLView webpage.</span></span> <span data-ttu-id="632e9-127">Beachten Sie, dass diese Technik nicht verhindern kann, dass der Benutzer den Inhalt digitaler Medien anzeigen kann, wenn er zum Skin-Modus wechselt.</span><span class="sxs-lookup"><span data-stu-id="632e9-127">Note that this technique cannot prevent the user from viewing the digital media content when he or she switches to skin mode.</span></span>

<span data-ttu-id="632e9-128">Sie erinnern sich, dass der HtmlView-Parameter auf jedes **Entry** -Element in einer. ASX-Datei angewendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="632e9-128">You will recall that the HTMLView parameter can be applied to each **ENTRY** element in an .asx file.</span></span> <span data-ttu-id="632e9-129">Sie können diese Funktion nutzen, um sicherzustellen, dass Ihr HtmlView-Inhalt jedes Mal angezeigt wird, wenn eine neue digitale Mediendatei gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="632e9-129">You can take advantage of this feature to ensure that your HTMLView content is displayed each time a new digital media file starts.</span></span> <span data-ttu-id="632e9-130">Ordnen Sie zu diesem Zweck jedem Eintrag in Ihrer. ASX-Wiedergabeliste ein **param** -Element für HtmlView zu.</span><span class="sxs-lookup"><span data-stu-id="632e9-130">To do this, associate a **PARAM** element for HTMLView with each entry in your .asx playlist.</span></span> <span data-ttu-id="632e9-131">Wenn jeder Eintrag abgespielt wird, wechselt der Spieler in den vollständigen Modus und zeigt den HtmlView-Inhalt an, den Sie in der Wiedergabeliste angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="632e9-131">When each entry plays, the Player returns to full mode and displays the HTMLView content you specified in the playlist.</span></span>

## <a name="url-and-file-script-command-types-are-disabled-by-default"></a><span data-ttu-id="632e9-132">URL-und Datei Skript-Befehls Typen sind standardmäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="632e9-132">URL and FILE script command types are disabled by default</span></span>

<span data-ttu-id="632e9-133">Windows Media Player 9 oder höher stellt Einstellungen bereit, die es dem Benutzer ermöglichen, anzugeben, ob URL-und Dateityp-Skript Befehle ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="632e9-133">Windows Media Player 9 Series or later provides settings that enable the user to specify whether URL and FILE type script commands are able to run.</span></span> <span data-ttu-id="632e9-134">Beide Skript Befehls Typen werden standardmäßig nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="632e9-134">By default, both of these script command types do not run.</span></span> <span data-ttu-id="632e9-135">Wenn Sie benutzerdefinierte Skript Befehls Typen verwenden, werden Sie unabhängig von der Benutzereinstellung weiterhin ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="632e9-135">If you use custom script command types, they will continue to run, regardless of the user setting.</span></span> <span data-ttu-id="632e9-136">Wenn Sie URL-und Dateityp Skript Befehle verwenden müssen, müssen Sie den Benutzer auffordern, die Einstellungen zu ändern.</span><span class="sxs-lookup"><span data-stu-id="632e9-136">If you must use URL and FILE type script commands, you must prompt the user to change the settings.</span></span> <span data-ttu-id="632e9-137">Um die Einstellungen zu ändern, **Klicken Sie auf Extras**, dann auf **Optionen** und dann auf **Sicherheit**.</span><span class="sxs-lookup"><span data-stu-id="632e9-137">To change the settings, click **Tools**, then **Options**, and then **Security**.</span></span>

## <a name="reopening-an-htmlview-does-not-reload-the-webpage"></a><span data-ttu-id="632e9-138">Beim erneuten Öffnen einer HtmlView wird die Webseite nicht neu geladen.</span><span class="sxs-lookup"><span data-stu-id="632e9-138">Reopening an HTMLView does not reload the webpage</span></span>

<span data-ttu-id="632e9-139">Wenn der Benutzer eine. ASX-Datei öffnet, die einen HtmlView-Parameter enthält, und dann dieselbe Datei erneut öffnet, aktualisiert Windows Media Player die HtmlView-Webseite nicht.</span><span class="sxs-lookup"><span data-stu-id="632e9-139">When the user opens an .asx file that includes an HTMLView parameter and subsequently reopens the same file, Windows Media Player does not refresh the HTMLView webpage.</span></span> <span data-ttu-id="632e9-140">Dies bedeutet auch, dass der Player den eingebetteten Browser nicht an die anfängliche HtmlView-Webseite zurückgibt, wenn Sie Benutzern ermöglicht haben, von ihrer HtmlView-Webseite zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="632e9-140">This also means that if you have allowed users to navigate away from your HTMLView webpage, the Player does not return the embedded browser to the initial HTMLView webpage.</span></span>

## <a name="hiding-the-content-location"></a><span data-ttu-id="632e9-141">Ausblenden des Inhalts Speicher Orts</span><span class="sxs-lookup"><span data-stu-id="632e9-141">Hiding the content location</span></span>

<span data-ttu-id="632e9-142">Möglicherweise möchten Sie, dass Windows Media Player den Speicherort der digitalen Medieninhalte nicht anzeigt, während eine. ASX-Datei wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="632e9-142">You might decide that you don't want Windows Media Player to display the location of your digital media content while it is playing an .asx file.</span></span> <span data-ttu-id="632e9-143">Normalerweise zeigt Windows Media Player nur Informationen über die Wiedergabeliste selbst an, wenn Inhalte aus dem Internet gestreamt werden.</span><span class="sxs-lookup"><span data-stu-id="632e9-143">Usually, Windows Media Player only shows information about the playlist itself when streaming content from the Internet.</span></span> <span data-ttu-id="632e9-144">Es gibt jedoch weitere Schritte, die Sie durchführen können, um zu verhindern, dass Benutzer den Speicherort der Inhalte ermitteln.</span><span class="sxs-lookup"><span data-stu-id="632e9-144">However, there are further steps you can take to prevent users from determining the location of your content.</span></span> <span data-ttu-id="632e9-145">Eine Möglichkeit, um sicherzustellen, dass der Player den Pfad zu ihren Inhalten nicht anzeigt, besteht beispielsweise darin, ihre Inhalte mithilfe von Windows Media Services serverseitigen Wiedergabelisten zu streamen.</span><span class="sxs-lookup"><span data-stu-id="632e9-145">For example, one way to ensure that the Player does not display the path to your content is to stream your content using Windows Media Services server-side playlists.</span></span> <span data-ttu-id="632e9-146">Auf diese Weise wird, wenn der Benutzer die Eigenschaften für den Inhalt anzeigt, die URL des Servers und nicht die URL Ihres Inhalts angezeigt.</span><span class="sxs-lookup"><span data-stu-id="632e9-146">That way, when the user views the properties for the content, he or she sees the URL of the server and not the URL of your content.</span></span>

## <a name="related-topics"></a><span data-ttu-id="632e9-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="632e9-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="632e9-148">**Anzeigen von Webseiten in Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="632e9-148">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="632e9-149">**Param-Element**</span><span class="sxs-lookup"><span data-stu-id="632e9-149">**PARAM Element**</span></span>](param-element.md)
</dt> </dl>

 

 




