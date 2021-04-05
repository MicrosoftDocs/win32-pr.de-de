---
title: Verwenden einer Metafile-Wiedergabeliste
description: Verwenden einer Metafile-Wiedergabeliste
ms.assetid: e6cbdb76-4405-409e-93c3-38a3baa7c231
keywords:
- Windows Media Metadatei-Wiedergabelisten mit
- Metadatei-Wiedergabelisten, verwenden
- Wiedergabelisten mit
- Windows Media Metadatei-Wiedergabelisten, Informationen zu
- Metadatei-Wiedergabelisten, Informationen
- Wiedergabelisten, Informationen
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a5f1832c0c739874fbbd4db219f2c622fc2debfa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709851"
---
# <a name="using-a-metafile-playlist"></a><span data-ttu-id="83612-109">Verwenden einer Metafile-Wiedergabeliste</span><span class="sxs-lookup"><span data-stu-id="83612-109">Using a Metafile Playlist</span></span>

<span data-ttu-id="83612-110">Da keine direkte Verknüpfung von einer Webseite mit einem Streaming Media-Server möglich ist, verwenden Sie Metadatei-Wiedergabelisten.</span><span class="sxs-lookup"><span data-stu-id="83612-110">Because you cannot link directly from a webpage to a streaming media server, you use metafile playlists.</span></span> <span data-ttu-id="83612-111">Die Metadatei-Wiedergabelisten enthalten die Informationen, die von Windows Media Player benötigt werden und auf einem Webserver gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="83612-111">The metafile playlists contain the information needed by Windows Media Player and are stored on a web server.</span></span> <span data-ttu-id="83612-112">Anschließend können Sie eine Verknüpfung zwischen dem Webdokument und einer Metadatendatei-Wiedergabeliste herstellen.</span><span class="sxs-lookup"><span data-stu-id="83612-112">You can then link from the Web document to a metafile playlist.</span></span> <span data-ttu-id="83612-113">Wenn eine Metadatei-Wiedergabeliste geöffnet wird, Steuern Sie die Übertragung an Windows-Media Player, das die Datei verarbeitet, eine Verbindung mit dem Streamingmedienserver herstellt und den angegebenen Inhalt wieder gibt.</span><span class="sxs-lookup"><span data-stu-id="83612-113">When a metafile playlist is opened, control transfers to Windows Media Player, which processes the file, connects to the streaming media server, and plays the specified content.</span></span>

<span data-ttu-id="83612-114">Der Browser lädt zuerst die Metadatendatei-Wiedergabeliste in das Cache Verzeichnis des Benutzers herunter.</span><span class="sxs-lookup"><span data-stu-id="83612-114">The browser first downloads the metafile playlist to the user's cache directory.</span></span> <span data-ttu-id="83612-115">Da die Metadatendatei-Wiedergabeliste klein ist, ist dies ein sehr schneller Schritt.</span><span class="sxs-lookup"><span data-stu-id="83612-115">Because the metafile playlist is small, this is a very quick step.</span></span> <span data-ttu-id="83612-116">Der Computer des Benutzers findet dann in der Datei Zuordnungs Tabelle die Zuordnung der Metadatei-Wiedergabeliste zu Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="83612-116">The user's computer then finds in its file associations table the association of the metafile playlist with Windows Media Player.</span></span> <span data-ttu-id="83612-117">Windows Media Player öffnet und interpretiert die Skripterstellung in der Metadatei-Wiedergabeliste, die unter anderem die URL des Streaminginhalts enthält.</span><span class="sxs-lookup"><span data-stu-id="83612-117">Windows Media Player opens and interprets the scripting in the metafile playlist, which contains, among other things, the URL of the streaming content.</span></span> <span data-ttu-id="83612-118">Windows Media Player verwendet die URL, um den Inhalt zu suchen und den Stream zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="83612-118">Windows Media Player uses the URL to locate the content and initiate the stream.</span></span> <span data-ttu-id="83612-119">Die metadatenwiedergabe-Wiedergabeliste steuert dann das Streaming.</span><span class="sxs-lookup"><span data-stu-id="83612-119">The metafile playlist scripting then controls the streaming experience.</span></span>

<span data-ttu-id="83612-120">Da Metadatei-Wiedergabelisten über eine Hilfsanwendung funktionieren, die dem asxmime-Typ (Application/Mplayer2 oder Video/x-ms-ASF) zugeordnet ist, sind Sie mit jedem Browser kompatibel, der Hilfsanwendungen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="83612-120">Because metafile playlists work through a helper application associated with the ASXMIME type (application/mplayer2 or video/x-ms-asf), they are compatible with any browser that supports helper applications.</span></span> <span data-ttu-id="83612-121">Die in diesem Dokument gezeigten Beispiele funktionieren mit Microsoft Internet Explorer 4,0 und höher sowie mit Netscape Navigator 4,0 und höher auf Microsoft Win32-® und Apple Macintosh-Plattformen.</span><span class="sxs-lookup"><span data-stu-id="83612-121">The examples shown in this document will work with Microsoft Internet Explorer 4.0 and later, and with Netscape Navigator 4.0 and later on Microsoft Win32® and Apple Macintosh platforms.</span></span> <span data-ttu-id="83612-122">In allen Beispielen müssen Sie sicherstellen, dass alle digitalen Mediendateien, auf die verwiesen wird, über gültige Pfade und Dateinamen für Ihre Umgebung verfügen.</span><span class="sxs-lookup"><span data-stu-id="83612-122">In all examples, you will have to be sure that any digital media files referenced have valid paths and file names for your environment.</span></span>

## <a name="related-topics"></a><span data-ttu-id="83612-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="83612-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83612-124">**Leitfaden für Windows Media-Metadateien**</span><span class="sxs-lookup"><span data-stu-id="83612-124">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> <dt>

[<span data-ttu-id="83612-125">**Referenz zu Windows Media-Metadateien**</span><span class="sxs-lookup"><span data-stu-id="83612-125">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> <dt>

[<span data-ttu-id="83612-126">**Übersicht über Windows Media-Metadatendateien**</span><span class="sxs-lookup"><span data-stu-id="83612-126">**Windows Media Metafiles Overview**</span></span>](windows-media-metafiles-overview.md)
</dt> </dl>

 

 




