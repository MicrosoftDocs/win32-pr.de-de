---
title: Verwenden relativer Verknüpfungen in Metadateien
description: Verwenden relativer Verknüpfungen in Metadateien
ms.assetid: 8f6c40fc-e025-43d5-a43a-c162f28bbd71
keywords:
- Windows Media Metadatei-Wiedergabelisten, relative Links
- Wiedergabelisten, relative Links
- Metadatei-Wiedergabelisten, relative Links
- Metadatendateien, relative Links
- Windows Media-Metadateien, relative Links
- Relative Links
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9f9fe000ec071b0e54b9c6699a8a560ee4a26051
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855843"
---
# <a name="using-relative-links-in-metafiles"></a><span data-ttu-id="4cbb6-109">Verwenden relativer Verknüpfungen in Metadateien</span><span class="sxs-lookup"><span data-stu-id="4cbb6-109">Using Relative Links in Metafiles</span></span>

<span data-ttu-id="4cbb6-110">Relative Links sind eine vollständig unterstützte Funktion von Windows Media-Metadatendateien.</span><span class="sxs-lookup"><span data-stu-id="4cbb6-110">Relative links are a fully supported feature of Windows Media metafiles.</span></span> <span data-ttu-id="4cbb6-111">Sie können relative Links in Metadateien verwenden, ähnlich wie Sie in HTML-Dokumenten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4cbb6-111">You can use relative links in metafiles much like you use them in HTML documents.</span></span> <span data-ttu-id="4cbb6-112">Durch die Verwendung relativer Verknüpfungen können Sie Metadateien erstellen, die portabel sind, d. h., Sie können eine gesamte Verzeichnisstruktur auf einen anderen Server kopieren oder verschieben, ohne die Pfade zu Grafikdateien zu aktualisieren, die als Banner oder die **href** -Attribute der **moreinfo** -Elemente verwendet werden (wenn Sie auf Dateien auf demselben Webserver wie die gespeicherte Metadatendatei verweisen).</span><span class="sxs-lookup"><span data-stu-id="4cbb6-112">The use of relative links enables you to create metafiles that are portable, meaning you can copy or move an entire directory structure to another server without updating the paths to graphic files used as banners or the **HREF** attributes of **MOREINFO** elements (if they reference files on the same web server as the stored metafile).</span></span> <span data-ttu-id="4cbb6-113">Relative Verknüpfungen funktionieren in jeder Anwendung, die Sie unterstützt, da die Teile der URL, die nicht im **href** -Attribut eines Elements enthalten sind, in der URL enthalten sind, die von der Anwendung an den Server gesendet wird, wenn diese URL angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="4cbb6-113">Relative links work, in any application that supports them, because the parts of the URL not included in the **HREF** attribute of an element are included in the URL sent by the application to the server when that URL is requested.</span></span> <span data-ttu-id="4cbb6-114">Dies bedeutet, dass das Protokoll (z. b. https://), der Servername und das virtuelle Verzeichnis, in dem sich die Datei befindet, die den relativen Link enthält, alle in der URL enthalten sind, die an den Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="4cbb6-114">This means that the protocol (such as https://), the server name, and the virtual directory in which the file containing the relative link is located are all included in the URL that is sent to the server.</span></span> <span data-ttu-id="4cbb6-115">Wenn sich die Mediendatei oder URL, die Sie mit einem relativen Link verknüpfen, nicht auf demselben Server wie die Metadatendatei befindet, ist der relative Link ungültig.</span><span class="sxs-lookup"><span data-stu-id="4cbb6-115">If the media file, or URL you link to using a relative link does not reside on the same server as the metafile, the relative link is not valid.</span></span>

> [!Note]  
> <span data-ttu-id="4cbb6-116">Diese Informationen über relative Links sind nur dann korrekt, wenn Sie einen Link zu Metadateien verwenden, die im eigenständigen Windows-Media Player geöffnet sind.</span><span class="sxs-lookup"><span data-stu-id="4cbb6-116">This information on relative links is correct only when using a link to metafiles that are opened in the stand-alone Windows Media Player.</span></span> <span data-ttu-id="4cbb6-117">Wenn Sie das eingebettete Windows Media Player-Steuerelement verwenden, sind alle Verknüpfungen relativ zu der Seite, auf der das-Steuerelement gehostet wird, es sei denn, das untergeordnete **Basis** Element des **-Elements wird** verwendet, um den relativen Pfad umzuleiten.</span><span class="sxs-lookup"><span data-stu-id="4cbb6-117">When you use the embedded Windows Media Player control, all links are relative to the page on which the control is hosted, unless the **BASE** child element of the **ASX** element is used to redirect the relative path.</span></span>

 

<span data-ttu-id="4cbb6-118">Alle relativen Verknüpfungen in der Metadatei müssen für Streamingmedien vollständig relativ und nicht als Laufwerks bezogen sein.</span><span class="sxs-lookup"><span data-stu-id="4cbb6-118">All relative links in the metafile must be fully relative, not drive-relative, for streaming media.</span></span> <span data-ttu-id="4cbb6-119">Wenn eine URL mit einem " \\ "-Zeichen beginnt, ist der Link "Drive-relative".</span><span class="sxs-lookup"><span data-stu-id="4cbb6-119">When a URL begins with a "\\" character, the link is drive-relative.</span></span> <span data-ttu-id="4cbb6-120">Windows Media Player versucht, die Datei zu öffnen, mit der auf dem Laufwerk, auf dem die Metadatendatei geöffnet wurde, und in der Regel ein Webserver geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="4cbb6-120">Windows Media Player attempts to open the file linked to on the drive where the metafile was opened from, usually a web server.</span></span> <span data-ttu-id="4cbb6-121">Da Webserver virtuelle Verzeichnisse verwenden, versucht Windows Media Player, den angegebenen Stream oder die angegebene Mediendatei in einem Unterverzeichnis eines virtuellen Verzeichnisses auf dem Webserver zu finden, von dem aus die Metadatendatei geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="4cbb6-121">Because web servers use virtual directories, Windows Media Player tries to find the specified stream or media file in a subdirectory of a virtual directory on the web server where the metafile was opened from.</span></span> <span data-ttu-id="4cbb6-122">Ein Benutzer hat keinen Zugriff auf ein Serververzeichnis.</span><span class="sxs-lookup"><span data-stu-id="4cbb6-122">A user would not have access to a server directory.</span></span> <span data-ttu-id="4cbb6-123">Das Beispiel in diesem Abschnitt veranschaulicht die Verwendung eines vollständig relativen Links.</span><span class="sxs-lookup"><span data-stu-id="4cbb6-123">The example in this section illustrates the use of a fully relative link.</span></span>

<span data-ttu-id="4cbb6-124">Sie können auf einem einzelnen Computer, auf dem sich alle Mediendateien, mit denen in der Metadatei-Wiedergabeliste verknüpft ist, auf einem Speichergerät auf dem Computer verwenden.</span><span class="sxs-lookup"><span data-stu-id="4cbb6-124">You can use drive-relative links when using metafiles on a single computer where all media files linked to in the metafile playlist exist on a storage device in that computer.</span></span> <span data-ttu-id="4cbb6-125">Medien können jedoch nicht auf diese Weise gestreamt werden.</span><span class="sxs-lookup"><span data-stu-id="4cbb6-125">However, you cannot stream media in this manner.</span></span>

<span data-ttu-id="4cbb6-126">Wenn Sie einen Link zu einer anderen Metadatei verwenden, um relative Verknüpfungen zuzulassen, ist der Name, der als Titel von Windows Media Player angezeigt wird, der Titel in der ursprünglichen Metadatendatei.</span><span class="sxs-lookup"><span data-stu-id="4cbb6-126">When you use a link to another metafile to allow for relative links, the name displayed as the Title by Windows Media Player is the Title in the original metafile.</span></span>

<span data-ttu-id="4cbb6-127">Relative Links können nicht für URLs zu einem Streaming Media-Server verwendet werden, da für den Zugriff auf Streamingmedieninhalte unterschiedliche Protokolle verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4cbb6-127">Relative links cannot be used for URLs to a streaming media server because different protocols are used for accessing streaming media content.</span></span>

<span data-ttu-id="4cbb6-128">In der folgenden Beispiel Wiedergabeliste enthält der erste **ENTRYREF** eine URL für eine andere Wiedergabeliste (relative. Wax).</span><span class="sxs-lookup"><span data-stu-id="4cbb6-128">In the following example playlist, the first **ENTRYREF** contains a URL for another playlist, relative.wax.</span></span>


```XML
<ASX>
    <ENTRYREF HREF="https://example.microsoft.com/metafiles/relative.wax"/>
</ASX>

```



<span data-ttu-id="4cbb6-129">Das folgende Beispiel zeigt die Datei relative. Wax, die relative Links enthält.</span><span class="sxs-lookup"><span data-stu-id="4cbb6-129">The following example is the file relative.wax, which contains relative links.</span></span>


```XML
<ASX version = "3.0">
    <BANNER HREF = "graphics/logo1.jpg">
        <MOREINFO HREF = "category1/category1.htm" />
    </BANNER>
    <ENTRY>
        <REF HREF = "mms://samples.microsoft.com/myfile.wma" />
    </ENTRY>
</ASX>

```



<span data-ttu-id="4cbb6-130">Die URL, die den Verweis auf die Wiedergabeliste (relative. Wax) enthält, kann in einer Metadatei-Wiedergabeliste vorhanden sein, auf die der Benutzer zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="4cbb6-130">The URL containing the reference to the playlist, relative.wax, can exist in a metafile playlist anywhere that is accessible to the user.</span></span> <span data-ttu-id="4cbb6-131">Damit die URL erfolgreich verarbeitet werden kann, muss ein Webserver mit dem Namen "example.Microsoft.com" vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="4cbb6-131">For the URL to be processed successfully, there must be a web server named "example.microsoft.com".</span></span> <span data-ttu-id="4cbb6-132">Dieser Webserver muss über ein virtuelles Verzeichnis verfügen, das als "Metafiles" definiert ist.</span><span class="sxs-lookup"><span data-stu-id="4cbb6-132">That web server must have a virtual directory defined as "metafiles".</span></span> <span data-ttu-id="4cbb6-133">Die referenzierte Wiedergabeliste (relative. Wax) muss auf dem Webserver mit dem Namen "example.Microsoft.com" im virtuellen Verzeichnis "Metafiles" vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="4cbb6-133">The referenced playlist, relative.wax, must exist on the web server named "example.microsoft.com" in the virtual directory "metafiles".</span></span>

<span data-ttu-id="4cbb6-134">Damit auf die Mediendateien, auf die verwiesen wird, in der Wiedergabeliste relative. Wax erfolgreich zugreifen und wiedergegeben wird, muss ein Verzeichnis mit dem Namen "graphics" vorhanden sein, bei dem es sich um ein Unterverzeichnis des virtuellen Verzeichnisses "Metafiles" des Servers handelt.</span><span class="sxs-lookup"><span data-stu-id="4cbb6-134">For the referenced media files in the playlist relative.wax to be successfully accessed and played, there must be a directory named "Graphics" which is a subdirectory of the server's virtual directory "metafiles".</span></span> <span data-ttu-id="4cbb6-135">Die Grafikdatei Logo1.jpg, auf die im **Banner** Element verwiesen wird, muss das Unterverzeichnis mit dem Namen Grafiken sein.</span><span class="sxs-lookup"><span data-stu-id="4cbb6-135">The graphics file Logo1.jpg, referenced in the **BANNER** element, must be the subdirectory named Graphics.</span></span>

<span data-ttu-id="4cbb6-136">Ähnlich muss sich ein Dokument mit dem Namen Category1.htm in einem Unterverzeichnis mit dem Namen Category1 befinden.</span><span class="sxs-lookup"><span data-stu-id="4cbb6-136">Similarly a document named Category1.htm must reside in a subdirectory named Category1.</span></span> <span data-ttu-id="4cbb6-137">Das Verzeichnis mit dem Namen Category1 muss als Unterverzeichnis des virtuellen Verzeichnisses "Metafiles" auf dem Webserver example.Microsoft.com vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="4cbb6-137">The directory named Category1 must exist as a subdirectory of the virtual directory "metafiles" on the web server example.microsoft.com.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4cbb6-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4cbb6-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4cbb6-139">**Erstellen von Metafile-Wiedergabelisten**</span><span class="sxs-lookup"><span data-stu-id="4cbb6-139">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="4cbb6-140">**Metafile-Wiedergabelisten**</span><span class="sxs-lookup"><span data-stu-id="4cbb6-140">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="4cbb6-141">**Verweis auf Windows Media-Metadateielemente**</span><span class="sxs-lookup"><span data-stu-id="4cbb6-141">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="4cbb6-142">**Leitfaden für Windows Media-Metadateien**</span><span class="sxs-lookup"><span data-stu-id="4cbb6-142">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




