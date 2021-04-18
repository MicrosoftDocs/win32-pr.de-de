---
title: Verwenden von Ankündigungen
description: Verwenden von Ankündigungen
ms.assetid: c372a4f8-2355-4c69-bba2-72b224879c4d
keywords:
- Windows Media Metadatei-Wiedergabelisten, Ankündigungen
- Wiedergabelisten, Ankündigungen
- Metadatei-Wiedergabelisten, Ankündigungen
- Windows-Media Player, Ankündigungen
- Ankündigungen
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0c16fafee1984d08992b96c39d7c3893ea54f682
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340825"
---
# <a name="using-announcements"></a><span data-ttu-id="33485-108">Verwenden von Ankündigungen</span><span class="sxs-lookup"><span data-stu-id="33485-108">Using Announcements</span></span>

<span data-ttu-id="33485-109">Eine Ankündigung ist eine Datei, die Informationen über die URL für einen Medienstrom enthält, einschließlich der Multicast-IP-Adresse, des Ports, des streamformats und anderer Stations Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="33485-109">An announcement is a file that contains information about the URL for a media stream, including the multicast IP address, port, stream format, and other station settings.</span></span> <span data-ttu-id="33485-110">Ankündigungen werden vom Windows Media-Administrator erstellt, wenn ein Unicast-oder Multicast-Veröffentlichungsdaten Strom erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="33485-110">Announcements are created by Windows Media Administrator when a unicast or multicast publishing stream is created.</span></span> <span data-ttu-id="33485-111">Der Client kann die Ankündigungs Datei schnell laden und dann mit dem Zugriff auf die streamingmediendatei fortfahren.</span><span class="sxs-lookup"><span data-stu-id="33485-111">The client can quickly load the announcement file, then proceed to access the streaming media file.</span></span>

<span data-ttu-id="33485-112">Bei einem unicastpublishing Point wird der Mediendaten Strom des Publishing Points geöffnet.</span><span class="sxs-lookup"><span data-stu-id="33485-112">For a unicast publishing point, the publishing point media stream is opened.</span></span> <span data-ttu-id="33485-113">Bei einem Multicast Publishing Point wird die URL aus einer Broadcast Stations Datei mit der Erweiterung. NSC extrahiert, und auf die Streamingmedien wird zugegriffen.</span><span class="sxs-lookup"><span data-stu-id="33485-113">For a multicast publishing point, the URL is extracted from a broadcast station file with an .nsc extension, and the streaming media is accessed.</span></span> <span data-ttu-id="33485-114">Im Gegensatz zu einem unicaststream sind keine Header Informationen in einem Multicast-Stream enthalten.</span><span class="sxs-lookup"><span data-stu-id="33485-114">Unlike a unicast stream, no header information is contained in a multicast stream.</span></span> <span data-ttu-id="33485-115">Diese Informationen stammen aus der Broadcast Stations Datei mit der Erweiterung. NSC.</span><span class="sxs-lookup"><span data-stu-id="33485-115">That information comes from the broadcast station file with an .nsc extension.</span></span> <span data-ttu-id="33485-116">Windows Media Player öffnet in der Regel zuerst eine Ankündigungs Datei. Dies ist eine Verwendung für Metadatei-Wiedergabelisten, die auf den Speicherort der Broadcast Stations Datei zeigt.</span><span class="sxs-lookup"><span data-stu-id="33485-116">Windows Media Player usually first opens an announcement file, which is one use for metafile playlists, that points to the location of the broadcast station file.</span></span>

<span data-ttu-id="33485-117">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="33485-117">Example Code</span></span>


```XML
<ASX VERSION="3.0">
    <TITLE>title</TITLE>
    <ENTRY>
        <REF HREF="mms://proseware.com/pubpoint"/>
    </ENTRY>
</ASX>

```



## <a name="related-topics"></a><span data-ttu-id="33485-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="33485-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33485-119">**Erstellen von Metafile-Wiedergabelisten**</span><span class="sxs-lookup"><span data-stu-id="33485-119">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="33485-120">**Verwenden von Metafile-Wiedergabelisten**</span><span class="sxs-lookup"><span data-stu-id="33485-120">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> </dl>

 

 




