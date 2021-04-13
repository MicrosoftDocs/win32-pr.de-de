---
title: Verwenden von Wiedergabelisten in Windows-Medien Download Paketen (veraltet)
description: Verwenden von Wiedergabelisten in Windows-Medien Download Paketen (veraltet)
ms.assetid: c40efe24-aaed-47fc-8a8a-f412dfc36af7
keywords:
- Windows Media-Metadatendateien, Windows-Medien Download Pakete
- Windows Media Player, Windows Media-Download Pakete
- Metafiles, Windows Media Download Packages
- Windows Media, Windows Media Download Packages
- Wiedergabelisten, Windows-Medien Download Pakete
- Metadatei-Wiedergabelisten, Windows-Medien Download Pakete
- Windows Media Metadatei-Wiedergabelisten, Windows Media-Download Pakete
- Windows Media Download Packages, Wiedergabelisten
- Windows Media-Download Pakete, metadateiwiedergabe Listen
- Windows Media-Download Pakete, Windows Media Metadatei-Wiedergabelisten
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 00c4daa26d18294c00aad7b4926a017d2f3f6343
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388567"
---
# <a name="using-playlists-in-windows-media-download-packages-deprecated"></a><span data-ttu-id="55d96-113">Verwenden von Wiedergabelisten in Windows-Medien Download Paketen (veraltet)</span><span class="sxs-lookup"><span data-stu-id="55d96-113">Using Playlists in Windows Media Download Packages (deprecated)</span></span>

<span data-ttu-id="55d96-114">Diese Seite dokumentiert eine Funktion, die in zukünftigen Versionen von Windows Media Player und dem Windows Media Player SDK möglicherweise nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="55d96-114">This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.</span></span>

<span data-ttu-id="55d96-115">Wiedergabelisten sind Windows Media-Metadateien mit der Dateinamenerweiterung ". asx", die Informationen bereitstellen, die Windows Media Player, wie der gepackte Inhalt wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="55d96-115">Playlists are Windows Media metafiles with an .asx file name extension that provide information that tells Windows Media Player how to play the packaged content.</span></span> <span data-ttu-id="55d96-116">Durch die Kombination mehrerer Inhalts Dateien zu einem einzelnen Windows Media Download-Paket können Sie das Windows Media-Downloadpaket mithilfe der Wiedergabeliste Steuern und anpassen.</span><span class="sxs-lookup"><span data-stu-id="55d96-116">By combining multiple content files into a single Windows Media Download package, you can control and customize your Windows Media Download package by using the playlist.</span></span>

> [!Note]  
> <span data-ttu-id="55d96-117">Im Allgemeinen werden Metadatendatei-Wiedergabelisten von Windows Media-Download Paketen verwendet, um auf die Multimedia-Inhalte im Paket und nicht auf einen Stream von einem Server in einem Intranet oder im Internet zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="55d96-117">In general, metafile playlists are used by Windows Media Download packages to reference the multimedia content in the package rather than a stream from a server on an intranet or the Internet.</span></span> <span data-ttu-id="55d96-118">Allerdings werden URL-Verweise innerhalb der. ASX-Datei unterstützt.</span><span class="sxs-lookup"><span data-stu-id="55d96-118">However, URL references within the .asx file are supported.</span></span>

 

<span data-ttu-id="55d96-119">Mithilfe von XML stellt die Metadatei die Informationen bereit, die von Windows Media Player zum wiedergeben und Anzeigen von Inhalten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="55d96-119">Using XML, the metafile provides the information Windows Media Player uses to play and display content.</span></span> <span data-ttu-id="55d96-120">Wiedergabelisten bestehen aus verschiedenen XML-Code Elementen mit ihren zugeordneten Tags und Attributen.</span><span class="sxs-lookup"><span data-stu-id="55d96-120">Playlists are made up of various XML code elements with their associated tags and attributes.</span></span> <span data-ttu-id="55d96-121">Jedes Element in einer Windows Media Metadatei-Wiedergabeliste definiert eine bestimmte Einstellung oder Aktion in Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="55d96-121">Each element in a Windows Media metafile playlist defines a particular setting or action in Windows Media Player.</span></span>

<span data-ttu-id="55d96-122">Auf dem Computer des Benutzers wird eine Windows Media-Metadatendatei mit der Dateinamenerweiterung ". asx" mit Windows Media Player verknüpft.</span><span class="sxs-lookup"><span data-stu-id="55d96-122">The user's computer associates a Windows Media metafile that has an .asx file name extension with Windows Media Player.</span></span> <span data-ttu-id="55d96-123">Windows Media Player öffnet und analysiert den XML-Code in der Metadatendatei, die den Pfad zum Suchen der verpackten Audiodateien oder Videodateien enthält.</span><span class="sxs-lookup"><span data-stu-id="55d96-123">Windows Media Player opens and parses the XML code in the metafile, which contains the path for locating the packaged audio or video files.</span></span> <span data-ttu-id="55d96-124">Das Metadatendatei-Skript steuert dann die Audiodarstellung, das Video und die grafische Darstellung.</span><span class="sxs-lookup"><span data-stu-id="55d96-124">The metafile script then controls the audio, video, and graphical experience.</span></span> <span data-ttu-id="55d96-125">Die Metadatendatei enthält auch Informationen, die von Windows Media Player verarbeitet und im Dropdown Feld Wiedergabeliste angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="55d96-125">The metafile also contains information that Windows Media Player processes and displays in the playlist drop-down box.</span></span> <span data-ttu-id="55d96-126">Unmittelbar nach dem Anzeigen der Liste wird das erste Element in der Liste wiedergegeben.</span><span class="sxs-lookup"><span data-stu-id="55d96-126">Immediately after the list is displayed, the first item in the list is played.</span></span>

<span data-ttu-id="55d96-127">Eine Metadatei-Wiedergabeliste ist eine Verknüpfung zu den Dateien, die ihren verpackten Inhalt enthalten.</span><span class="sxs-lookup"><span data-stu-id="55d96-127">A metafile playlist is a shortcut to the files that contain your packaged content.</span></span> <span data-ttu-id="55d96-128">Der folgende Code ist ein Beispiel für eine Metadatei, die den Rahmen angibt, der mit dem **Skin** -Element angezeigt werden soll, zwei zu Wiedergabe Ende Lieder und die Wiedergabelisten Informationen für die einzelnen Lieder.</span><span class="sxs-lookup"><span data-stu-id="55d96-128">The following code is an example of a metafile that specifies the border to display by using the **SKIN** element, two songs to be played, and the playlist information for each song.</span></span>


```XML
<ASX Version="3.0">
<AUTHOR>Name of content creator goes here</AUTHOR>
<TITLE>Album Title goes here</TITLE>
<PARAM name="Album" value="Album Title "/>
<PARAM name="Artist" value="Artist Name"/>
<PARAM name="Genre" value="Genre"/>
<SKIN HREF="myborder.wmz"/>
    <ENTRY>
        <REF HREF="song1.wma"/>
        <AUTHOR>Creator's name</AUTHOR>
        <COPYRIGHT>Copyright information</COPYRIGHT>
        <TITLE>Song #1 title</TITLE>
    </ENTRY>
    <ENTRY>
        <REF HREF="song2.wma"/>
        <AUTHOR>Creator's name</AUTHOR>
        <COPYRIGHT>Copyright information</COPYRIGHT>
        <TITLE>Song #2 name</TITLE>
    </ENTRY>
</ASX>

```



## <a name="related-topics"></a><span data-ttu-id="55d96-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="55d96-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55d96-130">**Rahmen für Windows-Media Player (veraltet)**</span><span class="sxs-lookup"><span data-stu-id="55d96-130">**Borders for Windows Media Player (deprecated)**</span></span>](borders-for-windows-media-player--deprecated.md)
</dt> <dt>

[<span data-ttu-id="55d96-131">**Windows Media-Download Pakete (veraltet)**</span><span class="sxs-lookup"><span data-stu-id="55d96-131">**Windows Media Download Packages (deprecated)**</span></span>](windows-media-download-packages--deprecated.md)
</dt> <dt>

[<span data-ttu-id="55d96-132">**Windows Media-Metadateien**</span><span class="sxs-lookup"><span data-stu-id="55d96-132">**Windows Media Metafiles**</span></span>](windows-media-metafiles.md)
</dt> </dl>

 

 




