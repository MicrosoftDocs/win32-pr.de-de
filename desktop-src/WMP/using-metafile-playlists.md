---
title: Verwenden von Metafile-Wiedergabelisten
description: Verwenden von Metafile-Wiedergabelisten
ms.assetid: f5711a7f-7674-4b92-8262-cee8bac4aa77
keywords:
- Windows Media Metadatei-Wiedergabelisten, Informationen zu
- Wiedergabelisten, Informationen
- Metadatei-Wiedergabelisten, Informationen
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 71f245d1fc1610174f842347a15dfcfaa13286e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855675"
---
# <a name="using-metafile-playlists"></a><span data-ttu-id="403fa-106">Verwenden von Metafile-Wiedergabelisten</span><span class="sxs-lookup"><span data-stu-id="403fa-106">Using Metafile Playlists</span></span>

<span data-ttu-id="403fa-107">Wiedergabelisten geben an, wie die Streamingmedien oder Mediendateien abgespielt werden und welche Metadatenfenster Media Player angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="403fa-107">Playlists specify how the streaming media or media files will be played and what metadata Windows Media Player will display.</span></span>

<span data-ttu-id="403fa-108">In diesem Abschnitt werden verschiedene Möglichkeiten erläutert, wie Sie Wiedergabelisten verwenden können.</span><span class="sxs-lookup"><span data-stu-id="403fa-108">This section explains several ways you can use playlists.</span></span> <span data-ttu-id="403fa-109">Der Abschnitt ist in folgende Themen unterteilt:</span><span class="sxs-lookup"><span data-stu-id="403fa-109">The section is divided into the following topics.</span></span>



| <span data-ttu-id="403fa-110">Thema</span><span class="sxs-lookup"><span data-stu-id="403fa-110">Topic</span></span>                                                                                              | <span data-ttu-id="403fa-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="403fa-111">Description</span></span>                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="403fa-112">Ändern der Anzeige</span><span class="sxs-lookup"><span data-stu-id="403fa-112">Modifying the Display</span></span>](modifying-the-display.md)                                                 | <span data-ttu-id="403fa-113">Hinzufügen von Text, Links und Bildern.</span><span class="sxs-lookup"><span data-stu-id="403fa-113">Adding text, links, and images.</span></span>                                                                                                                                |
| [<span data-ttu-id="403fa-114">Umleitung</span><span class="sxs-lookup"><span data-stu-id="403fa-114">Redirection</span></span>](redirection.md)                                                                     | <span data-ttu-id="403fa-115">Verwenden von Wiedergabelisten zum Umleiten des Browsers an Windows Media Player und angeben der URL eines zu Wiedergabe enden Streams oder einer Mediendatei.</span><span class="sxs-lookup"><span data-stu-id="403fa-115">Using playlists to redirect the browser to Windows Media Player and specifying the URL of a stream or media file to play.</span></span>                                      |
| [<span data-ttu-id="403fa-116">Zugreifen auf Medien</span><span class="sxs-lookup"><span data-stu-id="403fa-116">Accessing Media</span></span>](accessing-media.md)                                                             | <span data-ttu-id="403fa-117">Verwenden Sie Metadatei-Elemente und ihre untergeordneten Elemente, um den Zugriff auf die Inhalte und die Reihenfolge und Dauer ihrer Wiedergabe anzugeben.</span><span class="sxs-lookup"><span data-stu-id="403fa-117">Using metafile elements and their child elements to specify the content to access, and the order and duration of their playback.</span></span>                               |
| [<span data-ttu-id="403fa-118">Verwenden von Live ereignisstreamumschaltung</span><span class="sxs-lookup"><span data-stu-id="403fa-118">Using Live Event Stream Switching</span></span>](using-live-event-stream-switching.md)                         | <span data-ttu-id="403fa-119">Verwenden Sie das **Ereignis** Element, um einen Mediendaten Strom anzugeben, auf den zugegriffen werden soll, und setzen Sie dann den ursprünglichen Stream wieder</span><span class="sxs-lookup"><span data-stu-id="403fa-119">Using the **EVENT** element to specify a media stream to access and then resume playing the original stream.</span></span> <span data-ttu-id="403fa-120">Wird zum Einfügen von Werbe Einfügungs</span><span class="sxs-lookup"><span data-stu-id="403fa-120">Used for ad insertion.</span></span>                            |
| [<span data-ttu-id="403fa-121">Verwenden von Metadatendateien für den nahtlosen Datenstrom Wechsel</span><span class="sxs-lookup"><span data-stu-id="403fa-121">Using Metafiles for Seamless Stream Switching</span></span>](using-metafiles-for-seamless-stream-switching.md) | <span data-ttu-id="403fa-122">Verwenden des- **Ereignis** Elements, um den nächsten Mediendaten Strom für den Zugriff vorab zu laden, um Lücken in der Präsentation zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="403fa-122">Using the **EVENT** element to preload the next media stream to access to avoid gaps in the presentation.</span></span>                                                      |
| [<span data-ttu-id="403fa-123">Verwenden von Ankündigungen</span><span class="sxs-lookup"><span data-stu-id="403fa-123">Using Announcements</span></span>](using-announcements.md)                                                     | <span data-ttu-id="403fa-124">Verwenden einer Metadatei zum Bereitstellen von Informationen über die URL für einen Medienstrom, einschließlich der Multicast-IP-Adresse, des Ports, des streamformats und anderer Stations Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="403fa-124">Using a metafile to provide information about the URL for a media stream, including the multicast IP address, port, stream format, and other station settings.</span></span> |
| [<span data-ttu-id="403fa-125">Verwenden von URL-und Serverrollover</span><span class="sxs-lookup"><span data-stu-id="403fa-125">Using URL and Server Rollover</span></span>](using-url-and-server-rollover.md)                                 | <span data-ttu-id="403fa-126">Verwenden von Metadatei-Wiedergabelisten, um ein automatisches Rollback zu alternativen Inhalts Quellen bereitzustellen, wenn auf einen Stream nicht zugegriffen werden kann oder wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="403fa-126">Using metafile playlists to provide a means of automatically rolling over to alternate content sources when a stream cannot be accessed or played.</span></span>             |
| [<span data-ttu-id="403fa-127">Verwenden von benutzerdefinierten Parametern und Befehlen</span><span class="sxs-lookup"><span data-stu-id="403fa-127">Using Custom Parameters and Commands</span></span>](using-custom-parameters-and-commands.md)                   | <span data-ttu-id="403fa-128">Verwenden des **param** -Elements zum Definieren benutzerdefinierter Elemente, um zusätzliche Metadaten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="403fa-128">Using the **PARAM** element to define custom elements to provide additional metadata.</span></span>                                                                          |
| [<span data-ttu-id="403fa-129">Personalisieren der Medien Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="403fa-129">Personalizing Media Delivery</span></span>](personalizing-media-delivery.md)                                   | <span data-ttu-id="403fa-130">Verwenden von Benutzereinstellungen zum Ermitteln von Broadcast Inhalten</span><span class="sxs-lookup"><span data-stu-id="403fa-130">Using user preferences to determine broadcast content.</span></span>                                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="403fa-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="403fa-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="403fa-132">**Metafile-Wiedergabelisten**</span><span class="sxs-lookup"><span data-stu-id="403fa-132">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="403fa-133">**Verweis auf Windows Media-Metadateielemente**</span><span class="sxs-lookup"><span data-stu-id="403fa-133">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="403fa-134">**Leitfaden für Windows Media-Metadateien**</span><span class="sxs-lookup"><span data-stu-id="403fa-134">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




