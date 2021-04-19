---
title: Verwenden von Metadatendateien für den nahtlosen Datenstrom Wechsel
description: Verwenden von Metadatendateien für den nahtlosen Datenstrom Wechsel
ms.assetid: e632f670-54c4-4b5b-8396-1d5368f90e6d
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
ms.openlocfilehash: 29496c71c0c849480bae029f246bfd544667071e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341843"
---
# <a name="using-metafiles-for-seamless-stream-switching"></a><span data-ttu-id="13425-118">Verwenden von Metadatendateien für den nahtlosen Datenstrom Wechsel</span><span class="sxs-lookup"><span data-stu-id="13425-118">Using Metafiles for Seamless Stream Switching</span></span>

<span data-ttu-id="13425-119">Sie können den nahtlosen Datenstrom Wechsel mithilfe von Metadatei-Wiedergabelisten vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="13425-119">You can facilitate seamless stream switching using metafile playlists.</span></span> <span data-ttu-id="13425-120">Wenn ein Teil des Inhalts endet, erfolgt in der Regel eine Pufferung für den nächsten Clip oder Stream, bevor er geöffnet wird (wenn es sich um Inhalt handelt, der von einem Streaming Media-Server empfangen wird).</span><span class="sxs-lookup"><span data-stu-id="13425-120">Usually, when a piece of content ends, buffering occurs for the next clip or stream before it opens (if it is content received from a streaming media server).</span></span> <span data-ttu-id="13425-121">Microsoft Windows Media Services ermöglicht es Ihnen, diese Pufferzeit zu eliminieren oder zumindest zu minimieren, und die Wiedergabe eines anderen Streaminginhalts beginnt fast sofort.</span><span class="sxs-lookup"><span data-stu-id="13425-121">Microsoft Windows Media Services enables you to eliminate, or at least minimize, this buffering time and have another piece of streamed content begin playing nearly immediately.</span></span> <span data-ttu-id="13425-122">Der normale Betriebsmodus für Windows-Media Player besteht darin, den nächsten Mediendaten Strom zu öffnen, auf den von der Wiedergabeliste 20 Sekunden vor dem Ende des aktuell gerenderten Streams verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="13425-122">The normal mode of operation for Windows Media Player is to open the next media stream referenced by the playlist 20 seconds before the end of the currently rendered stream.</span></span> <span data-ttu-id="13425-123">Dies ermöglicht im Allgemeinen eine nahtlose Umstellung zwischen Mediendaten strömen, abhängig von anderen Faktoren wie z. b. Webzugriffs Zeiten.</span><span class="sxs-lookup"><span data-stu-id="13425-123">This generally provides a seamless transition between media streams, depending on other factors such as Web access times.</span></span>

<span data-ttu-id="13425-124">Verwenden Sie das **Ereignis** Element in einer Wiedergabeliste zusammen mit OpenEvent-Befehlen aus dem Encoder, um das nahtlose wechseln zwischen Streams oder Dateien zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="13425-124">Use the **EVENT** element in a playlist in conjunction with OPENEVENT commands from the encoder to facilitate seamless switching between streams or files.</span></span> <span data-ttu-id="13425-125">Wenn ein OpenEvent-Befehl 20 Sekunden oder länger vor dem Ereignis Befehl gesendet wird, können Verzögerungen bei der Datenstrom Umstellung minimiert werden.</span><span class="sxs-lookup"><span data-stu-id="13425-125">Sending an OPENEVENT command 20 seconds or more prior to the EVENT command can minimize delays in stream switching.</span></span> <span data-ttu-id="13425-126">Anschließend kann Windows Media Player einen Teil der bevorstehenden Streaming-Inhalte in einen Puffer laden.</span><span class="sxs-lookup"><span data-stu-id="13425-126">Then Windows Media Player is able to preload a portion of the upcoming streaming content into a buffer.</span></span>

<span data-ttu-id="13425-127">Verwenden Sie Windows Media Encoder, um einen Skript Befehl im Stream im folgenden Format zu senden:</span><span class="sxs-lookup"><span data-stu-id="13425-127">Use Windows Media Encoder to send a script command in the stream using the following format:</span></span>


```XML
OPENEVENT eventname 

```



<span data-ttu-id="13425-128">Der Ereignis Name muss der Name sein, der im **Ereignis** Element in der Wiedergabeliste definiert ist.</span><span class="sxs-lookup"><span data-stu-id="13425-128">The event name must be the one defined in the **EVENT** element in the playlist.</span></span> <span data-ttu-id="13425-129">Wenn Windows Media Player einen OpenEvent-Skript Befehl vom Encoder empfängt, wird das **Ereignis** Element in der Wiedergabeliste gesucht, und es wird begonnen, den Clip oder Stream zu puffern, der im **Ereignis** Element definiert ist.</span><span class="sxs-lookup"><span data-stu-id="13425-129">When Windows Media Player receives an OPENEVENT script command from the encoder, it looks to the **EVENT** element in the playlist and begins buffering the clip or stream defined in the **EVENT** element.</span></span> <span data-ttu-id="13425-130">Windows Media Player speichert diese Informationen dann bis zum eigentlichen Ereignis desselben Namens.</span><span class="sxs-lookup"><span data-stu-id="13425-130">Windows Media Player then holds this information until the actual event of the same name.</span></span> <span data-ttu-id="13425-131">Wenn das benannte Ereignis empfangen wird, wechselt Windows Media Player zu diesem zuvor gepufferten Inhalt.</span><span class="sxs-lookup"><span data-stu-id="13425-131">When the named event is received, Windows Media Player switches to that previously buffered content.</span></span>

> [!Note]  
> <span data-ttu-id="13425-132">Sie können keine Unicode-Zeichen für den OpenEvent Script-Befehl in der Mediendatei oder im- **Ereignis** Element in der Wiedergabeliste verwenden.</span><span class="sxs-lookup"><span data-stu-id="13425-132">You cannot use Unicode characters for the OPENEVENT script command in the media file or the **EVENT** element in the playlist.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="13425-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="13425-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13425-134">**Erstellen von Metafile-Wiedergabelisten**</span><span class="sxs-lookup"><span data-stu-id="13425-134">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="13425-135">**Metafile-Wiedergabelisten**</span><span class="sxs-lookup"><span data-stu-id="13425-135">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="13425-136">**Player. ScriptCommand-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="13425-136">**Player.ScriptCommand Event**</span></span>](player-player-scriptcommand.md)
</dt> <dt>

[<span data-ttu-id="13425-137">**Verwenden von Metafile-Wiedergabelisten**</span><span class="sxs-lookup"><span data-stu-id="13425-137">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="13425-138">**Verweis auf Windows Media-Metadateielemente**</span><span class="sxs-lookup"><span data-stu-id="13425-138">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="13425-139">**Leitfaden für Windows Media-Metadateien**</span><span class="sxs-lookup"><span data-stu-id="13425-139">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




