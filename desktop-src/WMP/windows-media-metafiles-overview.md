---
title: Übersicht über Windows Media-Metadatendateien
description: Übersicht über Windows Media-Metadatendateien
ms.assetid: 5b7742c0-f416-4bf4-ae03-9554b51fe620
keywords:
- Windows Media-Metadateien, Informationen zu
- Windows Media Player, Metafiles
- Windows Media Player, Windows Media-Metadateien
- Metadatendateien, Informationen zu
- Windows Media, Metafiles
- Windows Media Metadatei-Wiedergabelisten, Informationen zu
- Wiedergabelisten, Informationen
- Windows Media-Metadateien, Syntax
- Metadatendateien, Syntax
- Metadatei-Wiedergabelisten, Informationen
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e7ed86cca023103c044f28141e0212542d83d200
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338185"
---
# <a name="windows-media-metafiles-overview"></a><span data-ttu-id="5d7aa-113">Übersicht über Windows Media-Metadatendateien</span><span class="sxs-lookup"><span data-stu-id="5d7aa-113">Windows Media Metafiles Overview</span></span>

<span data-ttu-id="5d7aa-114">Der wichtigste Teil der erfolgreichen Verwendung von Windows Media-Metadateien ist die Verwendung der korrekten Syntax für die Metadatei-Elemente.</span><span class="sxs-lookup"><span data-stu-id="5d7aa-114">The most important part of successfully using Windows Media metafiles is using the correct syntax for the metafile elements.</span></span> <span data-ttu-id="5d7aa-115">Syntax Fehler in einer Windows Media-Metadatei können dazu führen, dass von einem einzelnen Attribut übersehen wird, dass die Metadatei nicht als gültig erkannt wird und nicht funktioniert.</span><span class="sxs-lookup"><span data-stu-id="5d7aa-115">Syntax errors in a Windows Media metafile can cause anything from a single attribute being overlooked, to the metafile not being recognized as valid and failing to work.</span></span>

<span data-ttu-id="5d7aa-116">Fast ebenso wichtig ist die Reihenfolge, in der die Elemente in einer Windows Media-Metadatei angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="5d7aa-116">Almost as important is the order in which the elements appear in a Windows Media metafile.</span></span> <span data-ttu-id="5d7aa-117">Die Attribute einiger Elemente überschreiben vorübergehend die Attribute ähnlicher Elemente in verschiedenen Abschnitten der Metadatei.</span><span class="sxs-lookup"><span data-stu-id="5d7aa-117">The attributes of some elements temporarily override the attributes of similar elements in different sections of the metafile.</span></span> <span data-ttu-id="5d7aa-118">Es gibt eine definierte [Rangfolge](order-of-precedence.md).</span><span class="sxs-lookup"><span data-stu-id="5d7aa-118">There is a defined [Order of Precedence](order-of-precedence.md).</span></span>

<span data-ttu-id="5d7aa-119">Windows Media Metadatei-Wiedergabelisten sind Windows Media-Metadateien, die Informationen bereitstellen, die Windows Media Player verwendet, um Unicaststreams, Multicast Ströme und andere unterstützte Medien aus einem Intranet oder dem Internet zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="5d7aa-119">Windows Media metafile playlists are Windows Media metafiles that provide information that Windows Media Player uses to receive unicast streams, multicast streams, and other supported media from an intranet or the Internet.</span></span> <span data-ttu-id="5d7aa-120">Eine Metadatei-Wiedergabeliste ist im Grunde eine Verknüpfung mit Medieninhalten.</span><span class="sxs-lookup"><span data-stu-id="5d7aa-120">A metafile playlist is basically a shortcut to media content.</span></span> <span data-ttu-id="5d7aa-121">Eine Metadatei-Wiedergabeliste kann als e-Mail gesendet, als Link Verweis auf einer Webseite verwendet, dynamisch mithilfe von Active Server Seiten (ASP) erstellt oder als eigenständige Datei auf einem lokalen Laufwerk vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="5d7aa-121">A metafile playlist can be sent as email, used as a link reference on a webpage, created dynamically using Active Server Pages (ASP), or exist as a stand-alone file on a local disk drive.</span></span> <span data-ttu-id="5d7aa-122">Eine Metadatei-Wiedergabeliste kann auf eine andere metadatenwiedergabe-Wiedergabeliste, eine ASP-Seite oder eine Windows Media-Stations Datei (mit der Dateinamenerweiterung ". NSC") verweisen.</span><span class="sxs-lookup"><span data-stu-id="5d7aa-122">A metafile playlist can reference another metafile playlist, an ASP page, or a Windows Media station file (with an .nsc file name extension).</span></span> <span data-ttu-id="5d7aa-123">Eine NSC-Datei wird verwendet, um eine Windows Media-Station für Windows Media Player zu definieren.</span><span class="sxs-lookup"><span data-stu-id="5d7aa-123">An .nsc file is used to define a Windows Media station to Windows Media Player.</span></span> <span data-ttu-id="5d7aa-124">Der grundlegende Behandlungsprozess ist für jeden Fall identisch.</span><span class="sxs-lookup"><span data-stu-id="5d7aa-124">The basic handling process is the same for each case.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5d7aa-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5d7aa-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d7aa-126">**Informationen zu Windows Media-Metadateien**</span><span class="sxs-lookup"><span data-stu-id="5d7aa-126">**About Windows Media Metafiles**</span></span>](about-windows-media-metafiles.md)
</dt> </dl>

 

 




