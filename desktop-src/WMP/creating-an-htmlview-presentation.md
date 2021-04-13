---
title: Erstellen einer HtmlView-Präsentation
description: Erstellen einer HtmlView-Präsentation
ms.assetid: 70203160-2dd9-4096-be6a-c704db757f7f
keywords:
- Windows Media Metadatei-Wiedergabelisten, HtmlView-Präsentationen
- Wiedergabelisten, HtmlView-Präsentationen
- Metadatei-Wiedergabelisten, HtmlView-Präsentationen
- Windows Media Metadatei-Wiedergabelisten, Erstellen von HtmlView-Präsentationen
- Wiedergabelisten, Erstellen von HtmlView-Präsentationen
- Metadatei-Wiedergabelisten, Erstellen von HtmlView-Präsentationen
- Erstellen von HtmlView-Präsentationen
- Windows Media Player, Erstellen von HtmlView-Präsentationen
- Windows Media Player, HtmlView-Präsentationen
- HtmlView, Erstellen von Präsentationen
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1094ce787e55fbeb98e628389b5fd51ab94ab415
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388464"
---
# <a name="creating-an-htmlview-presentation"></a><span data-ttu-id="eb85e-113">Erstellen einer HtmlView-Präsentation</span><span class="sxs-lookup"><span data-stu-id="eb85e-113">Creating an HTMLView Presentation</span></span>

<span data-ttu-id="eb85e-114">Zum Erstellen einer grundlegenden HtmlView-Präsentation benötigen Sie mindestens drei Elemente:</span><span class="sxs-lookup"><span data-stu-id="eb85e-114">To create a basic HTMLView presentation, you need at least three elements:</span></span>

-   <span data-ttu-id="eb85e-115">**Digitaler Medieninhalt.**</span><span class="sxs-lookup"><span data-stu-id="eb85e-115">**Digital media content.**</span></span> <span data-ttu-id="eb85e-116">Dies ist eine oder mehrere Audiodateien oder Videodateien, die von Windows Media Player abgespielt werden.</span><span class="sxs-lookup"><span data-stu-id="eb85e-116">This is one or more audio or video files that Windows Media Player plays.</span></span>
-   <span data-ttu-id="eb85e-117">**Eine Webseite.**</span><span class="sxs-lookup"><span data-stu-id="eb85e-117">**A webpage.**</span></span> <span data-ttu-id="eb85e-118">Dies ist der webbasierte Inhalt, der im Feature " **jetzt** wiedergeben" der Player-Benutzeroberfläche angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="eb85e-118">This is the Web-based content that displays in the **Now Playing** feature of the Player UI.</span></span>
-   <span data-ttu-id="eb85e-119">**Eine Windows Media-Metadatendatei.**</span><span class="sxs-lookup"><span data-stu-id="eb85e-119">**A Windows Media metafile.**</span></span> <span data-ttu-id="eb85e-120">Dies ist die Metadatei-Wiedergabeliste, die Windows Media Player anweist, den Inhalt digitaler Medien mit der Webseite zu kombinieren.</span><span class="sxs-lookup"><span data-stu-id="eb85e-120">This is the metafile playlist that directs Windows Media Player to combine the digital media content with the webpage.</span></span>

<span data-ttu-id="eb85e-121">Eine. ASX-Datei ist eine Textdatei, die Informationen über einen Dateistream und seine Präsentation bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="eb85e-121">An .asx file is a text file that provides information about a file stream and its presentation.</span></span> <span data-ttu-id="eb85e-122">Basierend auf der Syntax von Extensible Markup Language (XML) können. ASX-Dateien eine Vielzahl von Elementen enthalten, die jeweils durch ein Tag mit zugeordneten Attributen identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="eb85e-122">Based on Extensible Markup Language (XML) syntax, .asx files can contain a variety of elements, each identified by a tag with associated attributes.</span></span> <span data-ttu-id="eb85e-123">Das **param** -Element bietet eine Möglichkeit, einen benutzerdefinierten Parameter entweder einem bestimmten Eintrag in einer metadateiwiedergabe Liste oder der gesamten Metadatendatei zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="eb85e-123">The **PARAM** element provides a way to associate a custom parameter with either a particular entry in a metafile playlist or the entire metafile.</span></span> <span data-ttu-id="eb85e-124">Einer der für ihre Verwendung verfügbaren vordefinierten Parameternamen ist "HtmlView".</span><span class="sxs-lookup"><span data-stu-id="eb85e-124">One of the predefined parameter names available for your use is "HTMLView".</span></span> <span data-ttu-id="eb85e-125">Dies ist der Parameter, der bewirkt, dass die durch den URL-Wert angegebene Webseite in Windows Media Player angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="eb85e-125">This is the parameter that causes the webpage specified by the URL value to be displayed in Windows Media Player.</span></span>

<span data-ttu-id="eb85e-126">Der folgende Beispielcode zeigt eine. ASX-Datei, die eine einzelne digitale Mediendatei mit einer einzelnen Webseite kombiniert:</span><span class="sxs-lookup"><span data-stu-id="eb85e-126">The following example code shows an .asx file that combines a single digital media file with a single webpage:</span></span>


```XML
<ASX version="3.0">
<PARAM name="HTMLView" value="https://www.proseware.com/htmlview.htm"/>

<ENTRY>
   <REF href="rtsp://www.proseware.com/content1.wma"/>
</ENTRY>

</ASX>

```



<span data-ttu-id="eb85e-127">Wenn Windows Media Player die. ASX-Datei im vorangehenden Beispiel öffnet, wird die Audiodatei aus der Datei mit dem Namen Content1. WMA abgespielt und die Webseite mit **dem Namen** htmlview.htm in der Funktion zum Wiedergeben des vollmodusplayers geöffnet.</span><span class="sxs-lookup"><span data-stu-id="eb85e-127">When Windows Media Player opens the .asx file in the preceding example, it plays the audio from the file named content1.wma and opens the webpage named htmlview.htm in the **Now Playing** feature of the full-mode Player.</span></span> <span data-ttu-id="eb85e-128">Der Benutzer kann den Audioinhalt mithilfe der Windows Media Player-Steuerelemente anhalten, suchen und anhalten.</span><span class="sxs-lookup"><span data-stu-id="eb85e-128">The user can pause, seek, and stop the audio content using the Windows Media Player controls.</span></span>

<span data-ttu-id="eb85e-129">Sie können die Webseite, die für jeden Inhalt angezeigt wird, ganz einfach ändern, indem Sie jedem Eintrag ein **param** -Element zuordnen, wie im folgenden Codebeispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="eb85e-129">You can easily change the webpage that is displayed for each piece of content by associating a **PARAM** element with each entry, as the following code example shows:</span></span>


```XML
<ASX version="3.0">

<ENTRY>
   <PARAM name="HTMLView" value="https://www.proseware.com/htmlview1.htm"/>
   <REF href="rtsp://www.proseware.com/content1.wma"/>
</ENTRY>

<ENTRY>
   <PARAM name="HTMLView" value="https://www.proseware.com/htmlview2.htm"/>
   <REF href="rtsp://www.proseware.com/content2.wma"/>
</ENTRY>

</ASX>

```



<span data-ttu-id="eb85e-130">Im vorherigen Beispiel zeigt Windows Media Player zuerst die Webseite htmlview1.htm bei der Wiedergabe der digitalen Audiodatei Content1. WMA an.</span><span class="sxs-lookup"><span data-stu-id="eb85e-130">In the preceding example, Windows Media Player first displays the webpage htmlview1.htm while playing the digital audio file content1.wma.</span></span> <span data-ttu-id="eb85e-131">Wenn der Spieler den nächsten Eintrag in der Wiedergabeliste, Content2. WMA, öffnet, gibt die in angezeigte Webseite **nun** Änderungen an htmlview2.htm.</span><span class="sxs-lookup"><span data-stu-id="eb85e-131">When the Player opens the next entry in the playlist, content2.wma, the webpage displayed in **Now Playing** changes to htmlview2.htm.</span></span> <span data-ttu-id="eb85e-132">Auf diese Weise können Sie angeben, welche Webseite der Benutzer für die einzelnen Digital Media-Inhalte sehen soll.</span><span class="sxs-lookup"><span data-stu-id="eb85e-132">In this way, you can specify which webpage the user sees for each piece of digital media content.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eb85e-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="eb85e-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb85e-134">**Anzeigen von Webseiten in Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="eb85e-134">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="eb85e-135">**Param-Element**</span><span class="sxs-lookup"><span data-stu-id="eb85e-135">**PARAM Element**</span></span>](param-element.md)
</dt> </dl>

 

 




