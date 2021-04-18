---
title: Verwenden von Live ereignisstreamumschaltung
description: Verwenden von Live ereignisstreamumschaltung
ms.assetid: fa8af007-2db6-438f-9551-8e748bb79ef4
keywords:
- Windows Media Metadatei-Wiedergabelisten, Live ereignisstreamwechsel
- Wiedergabelisten, Live ereignisstreamwechsel
- Metadatei-Wiedergabelisten, Live ereignisstreamwechsel
- Windows Media Metadatei-Wiedergabelisten, ereignisstreamwechsel
- Wiedergabelisten, ereignisstreamwechsel
- Metadatei-Wiedergabelisten, ereignisstreamwechsel
- Windows Media Metadatei-Wiedergabelisten, AD-Einfügung
- Wiedergabelisten, Werbe Einfügung
- Metadatei-Wiedergabelisten, AD-Einfügung
- Windows Media Player, Live ereignisstreamwechsel
- Windows Media Player, ereignisstreamwechsel
- Windows Media Player, Werbe Einfügung
- Live ereignisstreamwechsel
- ereignisstreamwechsel
- Werbe Einfügung
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fd5c586e0f1ef2b36913dee822e461daeffbfcbf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206465"
---
# <a name="using-live-event-stream-switching"></a><span data-ttu-id="6b618-118">Verwenden von Live ereignisstreamumschaltung</span><span class="sxs-lookup"><span data-stu-id="6b618-118">Using Live Event Stream Switching</span></span>

<span data-ttu-id="6b618-119">Streamingmedien können auch durch die Interaktion von Skript Befehlen gesteuert werden, die in einem Mediendaten Strom mit Windows Media-Metadatei-Elementen in einer Metadatei-Wiedergabeliste eingebettet sind.</span><span class="sxs-lookup"><span data-stu-id="6b618-119">Streaming media can also be controlled by the interaction of script commands embedded in a media stream with Windows Media metafile elements in a metafile playlist.</span></span>

<span data-ttu-id="6b618-120">Ein Ereignis ist eine bestimmte Art von Skript Befehl, der in einen Mediendaten Strom oder eine Mediendatei eingebettet ist.</span><span class="sxs-lookup"><span data-stu-id="6b618-120">An event is a particular type of script command embedded in a media stream or media file.</span></span> <span data-ttu-id="6b618-121">Wenn das Windows Media Player-Steuerelement den Skript Befehl empfängt, verarbeitet es das Ereignis gemäß der Definition durch das **Ereignis** Element in der Metadatendatei-Wiedergabeliste.</span><span class="sxs-lookup"><span data-stu-id="6b618-121">When the Windows Media Player control receives the script command, it processes the event as defined by the **EVENT** element in the metafile playlist.</span></span> <span data-ttu-id="6b618-122">Windows Media Player schaltet aus dem aktuellen Stream, der gerendert wird, und rendert den Inhalt, auf den im metadatenwiedergabe- **Ereignis** Element verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="6b618-122">Windows Media Player switches from the current stream it is rendering and renders the content referenced in the metafile playlist **EVENT** element.</span></span> <span data-ttu-id="6b618-123">Das **Ereignis** Element wird in der Regel in der aktiven Produktion verwendet.</span><span class="sxs-lookup"><span data-stu-id="6b618-123">The **EVENT** element is usually used in live production.</span></span>

<span data-ttu-id="6b618-124">Ein **Ereignis** Element ähnelt einem **Entry** -Element, aber jedes behandelt die Wiedergabe von Streams und Mediendateien anders.</span><span class="sxs-lookup"><span data-stu-id="6b618-124">An **EVENT** element looks similar to an **ENTRY** element, but each handles the playback of streams and media files differently.</span></span> <span data-ttu-id="6b618-125">Das **Entry** -Element dient zum Erstellen von Wiedergabelisten.</span><span class="sxs-lookup"><span data-stu-id="6b618-125">The **ENTRY** element is used to create playlists.</span></span> <span data-ttu-id="6b618-126">Ein Stream oder eine Mediendatei, auf die in einem **Entry** -Element verwiesen wird, beginnt, wenn der Stream oder die Mediendatei, auf die im vorherigen **Eintrag** verwiesen wird</span><span class="sxs-lookup"><span data-stu-id="6b618-126">A stream or media file referenced in an **ENTRY** element starts playing when the stream or media file referenced in the previous **ENTRY** finishes.</span></span> <span data-ttu-id="6b618-127">Ein in einem **Ereignis** referenzierter Stream wird nur wiedergegeben, wenn ein bestimmter Skript Befehl empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="6b618-127">A stream referenced in an **EVENT** plays only when a specific script command is received.</span></span> <span data-ttu-id="6b618-128">Wenn Windows Media Player z. b. einen Skript Befehl mit dem Typ String "Event" und der Befehls Zeichenfolge "AdLINK" empfängt, wird die Wiedergabeliste nach den folgenden Elementen durchsucht.</span><span class="sxs-lookup"><span data-stu-id="6b618-128">For example, when Windows Media Player receives a script command with type string "EVENT" and the command string "Adlink", it searches the playlist for the following elements.</span></span>


```XML
<EVENT NAME="Adlink" WHENDONE="RESUME"> 
    <ENTRY HREF=mms://www.proseware.com/adlink.wma />
</EVENT>

```



<span data-ttu-id="6b618-129">Windows Media Player wechselt dann aus dem Livestream zum Wiedergeben des Streams oder der Mediendatei, die im **Ereignis** enthalten ist, in diesem Fall "AdLINK. wma".</span><span class="sxs-lookup"><span data-stu-id="6b618-129">Windows Media Player then switches from the live stream to play the stream or media file contained in the **EVENT**, in this case Adlink.wma.</span></span> <span data-ttu-id="6b618-130">Der Code `WHENDONE="RESUME"` weist Windows Media Player an, die Wiedergabe des vorherigen Streams fortzusetzen, wenn "AdLINK. wma" abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="6b618-130">The code `WHENDONE="RESUME"` instructs Windows Media Player to resume playing the previous stream when Adlink.wma is finished.</span></span>

> [!Note]  
> <span data-ttu-id="6b618-131">Fehler bei der Behandlung von Ereignissen, die in einen Medienstrom oder eine Mediendatei eingebettet sind, können zu unerwarteten Ergebnissen führen.</span><span class="sxs-lookup"><span data-stu-id="6b618-131">Failure to handle every event embedded in a media stream or media file may yield unexpected results.</span></span>

 

<span data-ttu-id="6b618-132">Wenn Sie Live-ereignisstreamwechsel verwenden möchten, müssen Sie ein- **Ereignis** Element in die Wiedergabeliste einschließen, um jeden in den Mediendaten Strömen oder in den Mediendateien in der Wiedergabeliste eingebetteten Ereignis Skript Befehl zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="6b618-132">If you want to use live event stream switching, you must include one **EVENT** element in your playlist to handle each event script command embedded in the media streams or media files in your playlist.</span></span> <span data-ttu-id="6b618-133">Bevor Sie die Wiedergabeliste erstellen, müssen Sie die Details darüber kennen, welche Skript Befehle in Ihren digitalen Medieninhalt eingebettet sind.</span><span class="sxs-lookup"><span data-stu-id="6b618-133">Before you create your playlist, you must know the details about which script commands are embedded in your digital media content.</span></span> <span data-ttu-id="6b618-134">Wenn ein Ereignis Skript Befehl ignoriert werden soll, der von Windows Media Player ignoriert werden soll, fügen Sie ein **Ereignis** Element in die Wiedergabeliste ein, um das Ereignis zu behandeln, aber verweisen Sie im Ereignishandler auf eine Pseudo-URL.</span><span class="sxs-lookup"><span data-stu-id="6b618-134">If there is an event script command that you want Windows Media Player to ignore, include an **EVENT** element in your playlist to handle the event, but reference a dummy URL in the event handler.</span></span>

## <a name="ad-insertion"></a><span data-ttu-id="6b618-135">Werbe Einfügung</span><span class="sxs-lookup"><span data-stu-id="6b618-135">Ad Insertion</span></span>

<span data-ttu-id="6b618-136">Diese Technik kann für Werbe Einfügungs Vorgänge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6b618-136">This technique can be used for ad insertion.</span></span> <span data-ttu-id="6b618-137">Beispielsweise kann während eines Live-Internet Broadcast eines Ballspiels ein Befehl an den Anfang jeder kommerziellen Pause gesendet werden, der jeden Client (Windows Media Player) anweist, in der Wiedergabeliste aufgeführten Werbespots zu spielen.</span><span class="sxs-lookup"><span data-stu-id="6b618-137">For example, during a live Internet broadcast of a ball game, a command can be sent at the beginning of every commercial break that instructs each client (Windows Media Player) to play commercials listed in its playlist.</span></span> <span data-ttu-id="6b618-138">Wenn die Wiedergabe der Werbespots durch Clients abgeschlossen ist, weist die Wiedergabeliste jeden Client an, zur Liveübertragung zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="6b618-138">When clients finish playing the commercials, the playlist instructs each client to cut back to the live broadcast.</span></span> <span data-ttu-id="6b618-139">Der Inhalt der **Ereignis** Medien wird nur dann gerendert, wenn die Streamingmedien, auf die zugegriffen wird, eingebettetes Skript mit dem passenden **Ereignis** Namen überträgt</span><span class="sxs-lookup"><span data-stu-id="6b618-139">The **EVENT** media content will be rendered only when the streaming media being accessed broadcasts embedded scripting with the matching **EVENT** name.</span></span>

<span data-ttu-id="6b618-140">Die Möglichkeiten für den **Ereignis** Wechsel sind am besten zu schätzen, indem Sie den Betrachter über den standardmäßigen Broadcast Übertragungen erreichen, um zu erfahren, wie ADS mithilfe von Windows Media-Technologien Betrachter erreichen können.</span><span class="sxs-lookup"><span data-stu-id="6b618-140">The possibilities inherent in **EVENT** switching are best appreciated by contrasting how ads reach viewers through standard, over-the-air broadcasting with how ads can reach viewers using Windows Media Technologies.</span></span> <span data-ttu-id="6b618-141">In der Vergangenheit konnten Broadcast-Werbeeinblendungen nur annähernd an Betrachter gerichtet sein, wobei die Bewertungsdaten als primäre Kriterien verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6b618-141">Historically, broadcast ads could only be roughly targeted at viewers, using ratings data as the primary criteria.</span></span> <span data-ttu-id="6b618-142">Mithilfe von Windows Media-Technologien gesendete anzeigen können direkt auf den Ziel Benutzer ausgerichtet werden, da **Ereignisse** und Wiedergabelisten basierend auf Benutzereingaben dynamisch erstellt werden können.</span><span class="sxs-lookup"><span data-stu-id="6b618-142">Ads sent using Windows Media Technologies can be aimed directly at the target user because **EVENTs** and playlists can be built on the fly based on user input.</span></span> <span data-ttu-id="6b618-143">Weitere Informationen finden Sie unter [Personalisieren der Medien Bereitstellung](personalizing-media-delivery.md).</span><span class="sxs-lookup"><span data-stu-id="6b618-143">For more information, see [Personalizing Media Delivery](personalizing-media-delivery.md).</span></span>

<span data-ttu-id="6b618-144">Sie können auch Metadatei-Wiedergabelisten verwenden, um angepasste Grafiken, Audiodaten und Text für Werbung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="6b618-144">You can also use metafile playlists to display customized graphics, audio and text for advertising.</span></span> <span data-ttu-id="6b618-145">Sie können das **Banner** -Element als untergeordnetes Element eines **Ereignisses** verwenden, um eine Werbe Meldungs Grafik anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="6b618-145">You can use the **BANNER** element as a child element of an **EVENT** to display an advertising message graphic.</span></span> <span data-ttu-id="6b618-146">Das **Banner** -Element enthält den Pfad und die Datei mit den Grafiken für Ihr Werbe Banner.</span><span class="sxs-lookup"><span data-stu-id="6b618-146">The **BANNER** element provides the path and file containing the graphics for your advertising banner.</span></span> <span data-ttu-id="6b618-147">Mithilfe des untergeordneten **moreinfo** -Elements können Sie auch einen Link zu einer Website oder Datei bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="6b618-147">You can also provide a link to a site or file using the **MOREINFO** child element.</span></span> <span data-ttu-id="6b618-148">Die URL im **moreingefo** -Element kann einen Link zu weiteren Ankündigungen im Internet bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="6b618-148">The URL in the **MOREINFO** element can provide a link to even more advertisements on the Web.</span></span> <span data-ttu-id="6b618-149">Im folgenden Beispiel wird die Verwendung dieser Elemente veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="6b618-149">The following example demonstrates using these elements.</span></span>

<span data-ttu-id="6b618-150">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="6b618-150">Example Code</span></span>


```XML
<BANNER HREF="SomePath\2.gif">
    <ABSTRACT>Read This Ad and Buy.</ABSTRACT>
    <MOREINFO HREF="https://www.proseware.com" />
</BANNER>

```



<span data-ttu-id="6b618-151">Im folgenden Beispiel wird die Werbe Einblendungs-Datei "AD" in den Broadcast-Unicastdatenstrom eingefügt, wenn ein Client ein Skript Befehls **Ereignis** empfängt, bei dem das Attribut " **Name** " auf "Timeout" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="6b618-151">The following example inserts the ad Advert.wma into the broadcast unicast stream BallGame when a client receives a script command **EVENT** with the **NAME** attribute set to "Time-Out".</span></span> <span data-ttu-id="6b618-152">**Clientskip** ist auf "Nein" festgelegt, um zu verhindern, dass die gestreamte Werbung ausgelassen wird.</span><span class="sxs-lookup"><span data-stu-id="6b618-152">**CLIENTSKIP** is set to NO to prevent the streamed ad from being skipped.</span></span> <span data-ttu-id="6b618-153">In diesem Beispiel muss die gestreamte-Werbe Einblendung vor dem zurückkehren zum ursprünglichen Stream abgespielt werden.</span><span class="sxs-lookup"><span data-stu-id="6b618-153">In this example, the streamed ad must be played before returning to the original stream.</span></span> <span data-ttu-id="6b618-154">Wenn die Werbe Einstellung abgeschlossen ist, setzt der Client die Wiedergabe des ursprünglichen Streams fort.</span><span class="sxs-lookup"><span data-stu-id="6b618-154">When the ad is finished, the client resumes playing the original stream.</span></span>

<span data-ttu-id="6b618-155">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="6b618-155">Example Code</span></span>


```XML
<ASX VERSION="3.0">
    <ENTRY>
        <REF HREF="mms://proseware.com/BallGame" />
    </ENTRY>
    <EVENT NAME="Time-Out" WHENDONE="RESUME">
        <ENTRY>
            <REF HREF = "mms://proseware.com/Advert.wma" 
                CLIENTSKIP = "NO" />
       </ENTRY>
    </EVENT>
</ASX>

```



## <a name="related-topics"></a><span data-ttu-id="6b618-156">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6b618-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b618-157">**Metafile-Wiedergabelisten**</span><span class="sxs-lookup"><span data-stu-id="6b618-157">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="6b618-158">**Verwenden von Metafile-Wiedergabelisten**</span><span class="sxs-lookup"><span data-stu-id="6b618-158">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="6b618-159">**Verweis auf Windows Media-Metadateielemente**</span><span class="sxs-lookup"><span data-stu-id="6b618-159">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="6b618-160">**Leitfaden für Windows Media-Metadateien**</span><span class="sxs-lookup"><span data-stu-id="6b618-160">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




