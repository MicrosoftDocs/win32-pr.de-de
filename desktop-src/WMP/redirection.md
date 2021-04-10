---
title: Umleitung
description: Umleitung
ms.assetid: c8e3b43f-c11a-4ca7-b85c-038f0bfc3eb3
keywords:
- Windows Media Metadatei-Wiedergabelisten, Umleitung
- Wiedergabelisten, Umleitung
- Metadatei-Wiedergabelisten, Umleitung
- Windows-Media Player, Umleitung
- Umleiten
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bf1bb4d690c8aa6808e009a45a7bff1d6efada72
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309327"
---
# <a name="redirection"></a><span data-ttu-id="f4df3-108">Umleitung</span><span class="sxs-lookup"><span data-stu-id="f4df3-108">Redirection</span></span>

<span data-ttu-id="f4df3-109">Die Wiedergabeliste leitet den Browser an Windows Media Player, um den festgelegten Mediendaten Strom oder die angegebene Mediendatei wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="f4df3-109">The playlist will redirect the browser to Windows Media Player to play the designated media stream or media file.</span></span> <span data-ttu-id="f4df3-110">Die einfachste Metadatendatei-Wiedergabeliste enthält nur die Uniform Resource Locator (URL) einer Mediendatei.</span><span class="sxs-lookup"><span data-stu-id="f4df3-110">The most basic metafile playlist contains only the Uniform Resource Locator (URL) of a media file.</span></span>

<span data-ttu-id="f4df3-111">Öffnen Sie zum Erstellen einer einfachen Metadatei-Wiedergabeliste Ihren bevorzugten Text-Editor, z. b. Microsoft Notepad, und geben Sie den folgenden Beispielcode ein.</span><span class="sxs-lookup"><span data-stu-id="f4df3-111">To create a basic metafile playlist, open your favorite text editor, such as Microsoft Notepad, and type the following example code.</span></span>


```XML
<ASX version="3.0">
   <ENTRY>
      <REF HREF="PathToYourFile"/>
   </ENTRY>
</ASX>

```



<span data-ttu-id="f4df3-112">Ersetzen Sie mithilfe der in der folgenden Tabelle aufgeführten Syntax einen gültigen Pfad zu Ihrer Windows-Mediendatei.</span><span class="sxs-lookup"><span data-stu-id="f4df3-112">Substitute a valid path to your Windows Media file using the syntax in the following table.</span></span>



| <span data-ttu-id="f4df3-113">Quelle des Inhalts</span><span class="sxs-lookup"><span data-stu-id="f4df3-113">Source of content</span></span>                                                                                 | <span data-ttu-id="f4df3-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="f4df3-114">Syntax</span></span>                                    |
|---------------------------------------------------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="f4df3-115">Der Inhalt ist eine Datei auf einem Windows Media-Server.</span><span class="sxs-lookup"><span data-stu-id="f4df3-115">Content is a file on a Windows Media server</span></span>                                                       | <span data-ttu-id="f4df3-116">mms://ServerName/Path/FileName.wma</span><span class="sxs-lookup"><span data-stu-id="f4df3-116">mms://ServerName/Path/FileName.wma</span></span>        |
| <span data-ttu-id="f4df3-117">Inhalt ist ein Broadcast-Multicast, auf den von einer Windows-Medienstation aus zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="f4df3-117">Content is a broadcast multicast that is accessed from a Windows Media station</span></span>                    | https://WebServerName/Stations/kxyz.nsc    |
| <span data-ttu-id="f4df3-118">Der Inhalt ist ein Broadcast-Unicast, auf den von einem Publishing Point auf einem Windows Media-Server zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="f4df3-118">Content is a broadcast unicast that is accessed from a publishing point on a Windows Media server</span></span> | <span data-ttu-id="f4df3-119">mms://ServerName/PublishingPointAlias</span><span class="sxs-lookup"><span data-stu-id="f4df3-119">mms://ServerName/PublishingPointAlias</span></span>     |
| <span data-ttu-id="f4df3-120">Der Inhalt ist eine Datei auf einem Webserver.</span><span class="sxs-lookup"><span data-stu-id="f4df3-120">Content is a file on a web server</span></span>                                                                 | https://WebServerName/Path/Filename.wma    |
| <span data-ttu-id="f4df3-121">Der Inhalt ist eine Datei auf einer lokalen Festplatte.</span><span class="sxs-lookup"><span data-stu-id="f4df3-121">Content is a file on a local hard disk</span></span>                                                            | <span data-ttu-id="f4df3-122">file://c: \\ Pfad \\ Dateiname. WMA</span><span class="sxs-lookup"><span data-stu-id="f4df3-122">file://c:\\Path\\Filename.wma</span></span>             |
| <span data-ttu-id="f4df3-123">Der Inhalt ist eine Datei auf einer Netzwerkfreigabe.</span><span class="sxs-lookup"><span data-stu-id="f4df3-123">Content is a file on a network share</span></span>                                                              | <span data-ttu-id="f4df3-124">file:// \\ \\ Servername \\ Pfad \\ Dateiname. WMA</span><span class="sxs-lookup"><span data-stu-id="f4df3-124">file://\\\\ServerName\\Path\\Filename.wma</span></span> |
| <span data-ttu-id="f4df3-125">Der Inhalt ist eine Datei auf einem Windows Media-Server.</span><span class="sxs-lookup"><span data-stu-id="f4df3-125">Content is a file on a Windows Media server</span></span>                                                       | <span data-ttu-id="f4df3-126">mms://ServerName/Path/FileName.wmv</span><span class="sxs-lookup"><span data-stu-id="f4df3-126">mms://ServerName/Path/FileName.wmv</span></span>        |



 

<span data-ttu-id="f4df3-127">Speichern Sie die Datei, die Sie erstellt haben, mit einem Dateinamen und einer Erweiterung, wie in [Dateinamen Erweiterungen](file-name-extensions.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f4df3-127">Save the file you have created with a file name and extension as described in [File Name Extensions](file-name-extensions.md).</span></span> <span data-ttu-id="f4df3-128">Doppelklicken Sie in Windows-Explorer auf die Datei.</span><span class="sxs-lookup"><span data-stu-id="f4df3-128">Double-click it in Windows Explorer.</span></span> <span data-ttu-id="f4df3-129">Windows Media Player sollte geöffnet werden und mit dem Streamen der Inhalte beginnen.</span><span class="sxs-lookup"><span data-stu-id="f4df3-129">Windows Media Player should open and start streaming the content.</span></span> <span data-ttu-id="f4df3-130">Sie können die Datei zusammen mit ihren Webseiten auf dem Webserver speichern und mit einem **href** -Element verknüpfen oder Sie mithilfe des Windows-Media Player **Objekttags** in eine Webseite einbetten.</span><span class="sxs-lookup"><span data-stu-id="f4df3-130">You can save the file to your web server, along with your webpages, and link to it with an **HREF** element, or embed it in a webpage using the Windows Media Player **OBJECT** tag.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f4df3-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f4df3-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4df3-132">**Metafile-Wiedergabelisten**</span><span class="sxs-lookup"><span data-stu-id="f4df3-132">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="f4df3-133">**Verwenden von Metafile-Wiedergabelisten**</span><span class="sxs-lookup"><span data-stu-id="f4df3-133">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="f4df3-134">**Verweis auf Windows Media-Metadateielemente**</span><span class="sxs-lookup"><span data-stu-id="f4df3-134">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="f4df3-135">**Leitfaden für Windows Media-Metadateien**</span><span class="sxs-lookup"><span data-stu-id="f4df3-135">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




